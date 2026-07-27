# Receiving strokes in another app

Open Brush can send information about each brush stroke to another app. This happens when you finish drawing the stroke.

There are two ways to receive this information:

* A **normal listener** receives the information as soon as it is ready.
* A **polling listener** lets the other app check for new information when it is ready.

## Which one should I use?

Use a **normal listener** if the other app can receive messages from Open Brush. This is usually the better choice for an app that runs for a long time or receives a lot of drawing.

Use a **polling listener** if it is easier for the other app to ask Open Brush for new strokes. This can be useful for a small tool that checks regularly while it is running.

{% hint style="warning" %}
A polling listener keeps new stroke information inside Open Brush until the other app collects it. The app should check regularly and unregister when it has finished. If it stops checking, Open Brush will continue storing the information and may use more memory.

If you are unsure which type to use, use a normal listener.
{% endhint %}

## Using a normal listener

First, start the app that will receive the stroke information. Then give Open Brush the address of that app:

```
http://localhost:40074/api/v1?listenfor.strokes=http://localhost:8000/
```

Replace `http://localhost:8000/` with the address used by your app.

Open Brush will send several messages for each finished stroke. Together, these messages describe the brush, size, colour and shape of the stroke.

## Using a polling listener

A polling listener needs a client ID. This is simply a name chosen by the other app. The examples below use `my-app`.

### 1. Register

Register the client ID before asking for strokes:

```
http://localhost:40074/api/v1?listenfor.strokes.poll=my-app
```

### 2. Check for new strokes

Use the same client ID each time the app checks:

```
http://localhost:40074/api/v1?query.outgoing.poll=my-app
```

The response contains the new stroke information collected since the previous check. A blank response means that there are no new strokes.

If Open Brush says that the polling listener is not registered, check that the client ID is correct and register it again.

{% hint style="info" %}
Checking collects the waiting information. The next check will only return information from newer strokes.
{% endhint %}

### 3. Unregister

When the app has finished, unregister the client ID:

```
http://localhost:40074/api/v1?listenfor.strokes.poll.unregister=my-app
```

This tells Open Brush that it no longer needs to keep stroke information for that app.

{% hint style="info" %}
If the client ID contains spaces or special characters, the app must encode them correctly when adding the ID to a web address.
{% endhint %}
