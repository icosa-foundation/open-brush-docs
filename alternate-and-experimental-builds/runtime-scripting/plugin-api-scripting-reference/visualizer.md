
# Visualizer

## Summary
Settings and controls for audio visualization mode

## Class Properties

<table>
<thead><tr><th width="225">Name</th><th width="160">Return Type</th><th width="80">Read/Write?</th><th>Description</th></tr></thead>
<tbody>
<tr><td>sampleRate</td><td>number</td><td>Read-only</td><td>The current audio sample rate</td></tr>
<tr><td>duration</td><td>number</td><td>Read-only</td><td>The current duration of the audio buffer</td></tr>
</tbody></table>




## Class Methods

        
### Visualizer:EnableScripting(name)

Enables scripted access to the audio visualization buffer

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>name</td><td>string</td><td></td></tr></tbody></table>






### Visualizer:DisableScripting()

Disables scripted access to the audio visualization buffer

**Returns:** nil






### Visualizer:SetWaveform(data)

Passes the given waveform data to the audio visualizer

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>data</td><td>number[]</td><td></td></tr></tbody></table>






### Visualizer:SetFft(data1, data2, data3, data4)

Passes the given FFT data to the audio visualizer

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>data1</td><td>number[]</td><td></td></tr>
<tr><td>data2</td><td>number[]</td><td></td></tr>
<tr><td>data3</td><td>number[]</td><td></td></tr>
<tr><td>data4</td><td>number[]</td><td></td></tr></tbody></table>






### Visualizer:SetBeats(x, y, z, w)

Passes the given beat data to the audio visualizer

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>x</td><td>number</td><td></td></tr>
<tr><td>y</td><td>number</td><td></td></tr>
<tr><td>z</td><td>number</td><td></td></tr>
<tr><td>w</td><td>number</td><td></td></tr></tbody></table>






### Visualizer:SetBeatAccumulators(x, y, z, w)

Passes the given beat accumulator data to the audio visualizer

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>x</td><td>number</td><td></td></tr>
<tr><td>y</td><td>number</td><td></td></tr>
<tr><td>z</td><td>number</td><td></td></tr>
<tr><td>w</td><td>number</td><td></td></tr></tbody></table>






### Visualizer:SetBandPeak(peak)

Passes the given band peak data to the audio visualizer

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>peak</td><td>number</td><td></td></tr></tbody></table>





    

