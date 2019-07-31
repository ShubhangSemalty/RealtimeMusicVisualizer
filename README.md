# RealtimeMusicVisualizer

Music visualization or music visualisation, a feature found in electronic music visualizers and media player software, generates animated imagery based on a piece of music. The imagery is usually generated and rendered in real time and in a way synchronized with the music as it is played.

Visualization techniques range from simple ones (e.g., a simulation of an oscilloscope display) to elaborate ones, which often include a number of composited effects. The changes in the music's loudness and frequency spectrum are among the properties used as input to the visualization.Effective music visualization aims to attain a high degree of visual correlation between a musical track's spectral characteristics such as frequency and amplitude and the objects or components of the visual image being rendered and displayed. 

The Visualizer class enables application to retrieve part of the currently playing audio for visualization purpose. It is not an audio recording interface and only returns partial and low quality audio content. However, to protect privacy of certain audio data (e.g voice mail) the use of the visualizer requires the permission android.permission.RECORD_AUDIO.

The audio session ID passed to the constructor indicates which audio content should be visualized:

    If the session is 0, the audio output mix is visualized
    If the session is not 0, the audio from a particular MediaPlayer or AudioTrack using this audio session is visualized

Two types of representation of audio content can be captured:

    Waveform data: consecutive 8-bit (unsigned) mono samples by using the getWaveForm(byte[]) method
    Frequency data: 8-bit magnitude FFT by using the getFft(byte[]) method

The length of the capture can be retrieved or specified by calling respectively getCaptureSize() and setCaptureSize(int) methods. The capture size must be a power of 2 in the range returned by getCaptureSizeRange().
