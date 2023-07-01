
# Waveform

## Summary
Functions to generate a variety of waveforms



## Class Methods

        
### Waveform:Sine(time, frequency)

Returns the value of a sine wave at the given time and frequency

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>time</td><td>number</td><td></td></tr>
<tr><td>frequency</td><td>number</td><td></td></tr></tbody></table>






### Waveform:Cosine(time, frequency)

Returns the value of a cosine wave at the given time and frequency

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>time</td><td>number</td><td></td></tr>
<tr><td>frequency</td><td>number</td><td></td></tr></tbody></table>






### Waveform:Triangle(time, frequency)

Returns the value of a triangle wave at the given time and frequency

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>time</td><td>number</td><td></td></tr>
<tr><td>frequency</td><td>number</td><td></td></tr></tbody></table>






### Waveform:Sawtooth(time, frequency)

Returns the value of a sawtooth wave at the given time and frequency

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>time</td><td>number</td><td></td></tr>
<tr><td>frequency</td><td>number</td><td></td></tr></tbody></table>






### Waveform:Square(time, frequency)

Returns the value of a square wave at the given time and frequency

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>time</td><td>number</td><td></td></tr>
<tr><td>frequency</td><td>number</td><td></td></tr></tbody></table>






### Waveform:Pulse(time, frequency, pulseWidth)

Returns the value of a pulse wave with a specified pulse width at the given time, frequency

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>time</td><td>number</td><td></td></tr>
<tr><td>frequency</td><td>number</td><td></td></tr>
<tr><td>pulseWidth</td><td>number</td><td></td></tr></tbody></table>






### Waveform:Exponent(time, frequency)

Returns the value of an exponential wave at the given time and frequency

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>time</td><td>number</td><td></td></tr>
<tr><td>frequency</td><td>number</td><td></td></tr></tbody></table>






### Waveform:Power(time, frequency, power)

Returns the value of a power wave at the given time, frequency, and power

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>time</td><td>number</td><td></td></tr>
<tr><td>frequency</td><td>number</td><td></td></tr>
<tr><td>power</td><td>number</td><td></td></tr></tbody></table>






### Waveform:Parabolic(time, frequency)

Returns the value of a parabolic wave at the given time and frequency

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>time</td><td>number</td><td></td></tr>
<tr><td>frequency</td><td>number</td><td></td></tr></tbody></table>






### Waveform:ExponentialSawtooth(time, frequency, exponent)

Returns the value of an exponential sawtooth wave with the specified exponent at the given time, frequency

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>time</td><td>number</td><td></td></tr>
<tr><td>frequency</td><td>number</td><td></td></tr>
<tr><td>exponent</td><td>number</td><td></td></tr></tbody></table>






### Waveform:PerlinNoise(time, frequency)

Returns the value of a perlin noise function at the given time and frequency

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>time</td><td>number</td><td></td></tr>
<tr><td>frequency</td><td>number</td><td></td></tr></tbody></table>






### Waveform:WhiteNoise()

Returns the value of a white noise function

**Returns:** number






### Waveform:BrownNoise(previous)

Returns the value of a brown noise function

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>previous</td><td>number</td><td></td></tr></tbody></table>






### Waveform:BlueNoise(previous)

Returns the value of a blue noise function

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>previous</td><td>number</td><td></td></tr></tbody></table>






### Waveform:Sine(time, frequency, duration, sampleRate, amplitude)

Returns a sine wave with the given frequency, duration, and sample rate

**Returns:** number[]


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>time</td><td>number</td><td></td></tr>
<tr><td>frequency</td><td>number</td><td></td></tr>
<tr><td>duration</td><td>number</td><td></td></tr>
<tr><td>sampleRate</td><td>number</td><td></td></tr>
<tr><td>amplitude</td><td>number</td><td></td></tr></tbody></table>






### Waveform:Cosine(time, frequency, duration, sampleRate, amplitude)

Returns a cosine wave with the given frequency, duration, and sample rate

**Returns:** number[]


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>time</td><td>number</td><td></td></tr>
<tr><td>frequency</td><td>number</td><td></td></tr>
<tr><td>duration</td><td>number</td><td></td></tr>
<tr><td>sampleRate</td><td>number</td><td></td></tr>
<tr><td>amplitude</td><td>number</td><td></td></tr></tbody></table>






### Waveform:Triangle(time, frequency, duration, sampleRate, amplitude)

Returns a triangle wave with the given frequency, duration, and sample rate

**Returns:** number[]


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>time</td><td>number</td><td></td></tr>
<tr><td>frequency</td><td>number</td><td></td></tr>
<tr><td>duration</td><td>number</td><td></td></tr>
<tr><td>sampleRate</td><td>number</td><td></td></tr>
<tr><td>amplitude</td><td>number</td><td></td></tr></tbody></table>






### Waveform:Sawtooth(time, frequency, duration, sampleRate, amplitude)

Returns a sawtooth wave with the given frequency, duration, and sample rate

**Returns:** number[]


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>time</td><td>number</td><td></td></tr>
<tr><td>frequency</td><td>number</td><td></td></tr>
<tr><td>duration</td><td>number</td><td></td></tr>
<tr><td>sampleRate</td><td>number</td><td></td></tr>
<tr><td>amplitude</td><td>number</td><td></td></tr></tbody></table>






### Waveform:Square(time, frequency, duration, sampleRate, amplitude)

Returns a square wave with the given frequency, duration, and sample rate

**Returns:** number[]


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>time</td><td>number</td><td></td></tr>
<tr><td>frequency</td><td>number</td><td></td></tr>
<tr><td>duration</td><td>number</td><td></td></tr>
<tr><td>sampleRate</td><td>number</td><td></td></tr>
<tr><td>amplitude</td><td>number</td><td></td></tr></tbody></table>






### Waveform:Exponent(time, frequency, duration, sampleRate, amplitude)

Returns an exponential wave with the given frequency, duration, and sample rate

**Returns:** number[]


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>time</td><td>number</td><td></td></tr>
<tr><td>frequency</td><td>number</td><td></td></tr>
<tr><td>duration</td><td>number</td><td></td></tr>
<tr><td>sampleRate</td><td>number</td><td></td></tr>
<tr><td>amplitude</td><td>number</td><td></td></tr></tbody></table>






### Waveform:Parabolic(time, frequency, duration, sampleRate, amplitude)

Returns a parabolic wave with the given frequency, duration, and sample rate

**Returns:** number[]


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>time</td><td>number</td><td></td></tr>
<tr><td>frequency</td><td>number</td><td></td></tr>
<tr><td>duration</td><td>number</td><td></td></tr>
<tr><td>sampleRate</td><td>number</td><td></td></tr>
<tr><td>amplitude</td><td>number</td><td></td></tr></tbody></table>






### Waveform:Pulse(time, frequency, pulseWidth, duration, sampleRate, amplitude)

Returns a pulse wave with the given frequency, pulse width, duration, and sample rate

**Returns:** number[]


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>time</td><td>number</td><td></td></tr>
<tr><td>frequency</td><td>number</td><td></td></tr>
<tr><td>pulseWidth</td><td>number</td><td></td></tr>
<tr><td>duration</td><td>number</td><td></td></tr>
<tr><td>sampleRate</td><td>number</td><td></td></tr>
<tr><td>amplitude</td><td>number</td><td></td></tr></tbody></table>






### Waveform:Power(time, frequency, power, duration, sampleRate, amplitude)

Returns a power wave with the given frequency, power, duration, and sample rate

**Returns:** number[]


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>time</td><td>number</td><td></td></tr>
<tr><td>frequency</td><td>number</td><td></td></tr>
<tr><td>power</td><td>number</td><td></td></tr>
<tr><td>duration</td><td>number</td><td></td></tr>
<tr><td>sampleRate</td><td>number</td><td></td></tr>
<tr><td>amplitude</td><td>number</td><td></td></tr></tbody></table>






### Waveform:ExponentialSawtoothWave(time, frequency, exponent, duration, sampleRate, amplitude)

Returns an exponential sawtooth wave with the given frequency, exponent, duration, and sample rate

**Returns:** number[]


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>time</td><td>number</td><td></td></tr>
<tr><td>frequency</td><td>number</td><td></td></tr>
<tr><td>exponent</td><td>number</td><td></td></tr>
<tr><td>duration</td><td>number</td><td></td></tr>
<tr><td>sampleRate</td><td>number</td><td></td></tr>
<tr><td>amplitude</td><td>number</td><td></td></tr></tbody></table>






### Waveform:PerlinNoise(time, frequency, duration, sampleRate, amplitude)

Returns a perlin noise wave with the given frequency, duration, and sample rate

**Returns:** number[]


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>time</td><td>number</td><td></td></tr>
<tr><td>frequency</td><td>number</td><td></td></tr>
<tr><td>duration</td><td>number</td><td></td></tr>
<tr><td>sampleRate</td><td>number</td><td></td></tr>
<tr><td>amplitude</td><td>number</td><td></td></tr></tbody></table>






### Waveform:WhiteNoise(duration, sampleRate, amplitude)

Returns a white noise wave with the given duration and sample rate

**Returns:** number[]


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>duration</td><td>number</td><td></td></tr>
<tr><td>sampleRate</td><td>number</td><td></td></tr>
<tr><td>amplitude</td><td>number</td><td></td></tr></tbody></table>






### Waveform:BrownNoise(previous, duration, sampleRate, amplitude)

Returns a brown noise wave with the given duration and sample rate

**Returns:** number[]


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>previous</td><td>number</td><td></td></tr>
<tr><td>duration</td><td>number</td><td></td></tr>
<tr><td>sampleRate</td><td>number</td><td></td></tr>
<tr><td>amplitude</td><td>number</td><td></td></tr></tbody></table>






### Waveform:BlueNoise(previous, duration, sampleRate, amplitude)

Returns a blue noise wave with the given duration and sample rate

**Returns:** number[]


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>previous</td><td>number</td><td></td></tr>
<tr><td>duration</td><td>number</td><td></td></tr>
<tr><td>sampleRate</td><td>number</td><td></td></tr>
<tr><td>amplitude</td><td>number</td><td></td></tr></tbody></table>





    

