# Unity shader examples

Use these with geometry you export from Open Brush and import into Unity. However, you should prefer to use the [Open Brush Toolkit](https://github.com/icosa-gallery/open-brush-toolkit), which comes with all the Open Brush shaders.

#### Opaque shader

```text
Shader "Brush/Standard"
{
    Properties
    {
        _Color ("Main Color", Color) = (1,1,1,1)
        _SpecColor ("Specular Color", Color) = (0.5, 0.5, 0.5, 0)
        _Shininess ("Shininess", Range (0.01, 1)) = 0.078125
        _MainTex ("Base (RGBA)", 2D) = "white" {}
        _BumpMap ("Normalmap", 2D) = "bump" {}
        _Cutoff ("Alpha cutoff", Range(0,1)) = 0.5
    }
    SubShader
    {
        Tags
        {
            "Queue"="AlphaTest" "IgnoreProjector"="True" "RenderType"="TransparentCutout"
        }
        LOD 400
        CGPROGRAM
        #pragma target 3.0
        #pragma surface surf StandardSpecular vertex:vert alphatest:_Cutoff addshadow
        struct Input
        {
            float2 uv_MainTex;
            float2 uv_BumpMap;
            float4 color : Color;
        };

        sampler2D _MainTex;
        sampler2D _BumpMap;
        fixed4 _Color;
        half _Shininess;

        void vert(inout appdata_full i)
        {
        }

        void surf(Input IN, inout SurfaceOutputStandardSpecular o)
        {
            fixed4 tex = tex2D(_MainTex, IN.uv_MainTex);
            o.Albedo = tex.rgb * _Color.rgb * IN.color.rgb;
            o.Smoothness = _Shininess;
            o.Specular = _SpecColor;
            o.Normal = UnpackNormal(tex2D(_BumpMap, IN.uv_BumpMap));
            o.Alpha = tex.a * IN.color.a;
        }
        ENDCG
    }
    FallBack "Transparent/Cutout/VertexLit"
}
```

#### Additive shader

```text
Shader "Brush/Additive"
{
    Properties
    {
        _MainTex ("Texture", 2D) = "white" {}
    }
    Category
    {
        Tags
        {
            "Queue"="Transparent" "IgnoreProjector"="True" "RenderType"="Transparent"
        }
        Blend SrcAlpha One
        AlphaTest Greater .01
        ColorMask RGB
        Cull Off Lighting Off ZWrite Off Fog
        {
            Color (0,0,0,0)
        }
        SubShader
        {
            Pass
            {
                CGPROGRAM
                #pragma vertex vert
                #pragma fragment frag
                #include "UnityCG.cginc"
                sampler2D _MainTex;

                struct appdata_t
                {
                    float4 vertex : POSITION;
                    fixed4 color : COLOR;
                    float3 normal : NORMAL;
                    float2 texcoord : TEXCOORD0;
                };

                struct v2f
                {
                    float4 vertex : POSITION;
                    fixed4 color : COLOR;
                    float2 texcoord : TEXCOORD0;
                };

                float4 _MainTex_ST;

                v2f vert(appdata_t v)
                {
                    v2f o;
                    o.vertex = mul(UNITY_MATRIX_MVP, v.vertex);
                    o.texcoord = TRANSFORM_TEX(v.texcoord, _MainTex);
                    o.color = v.color;
                    return o;
                }

                fixed4 frag(v2f i) : COLOR
                {
                    half4 c = tex2D(_MainTex, i.texcoord);
                    return i.color * c;
                }
                ENDCG
            }
        }
```

