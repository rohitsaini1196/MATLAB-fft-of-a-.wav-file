# MATLAB-fft-of-a-.wav-file
Let's Take any music audio file in ‘wav’ format and compute its Fourier Transform using the MATLAB commands.


Commands are:-

[audio_in,audio_freq_sampl]=audioread('audio_signal');

Length_audio=length(audio_in);

df=audio_freq_sampl/Length_audio;

frequency_audio=-audio_freq_sampl/2:df:audio_freq_sampl/2-df;

figure

FFT_audio_in=fftshift(fft(audio_in))/length(fft(audio_in));

plot(frequency_audio,abs(FFT_audio_in));

title('FFT of Input Audio');

xlabel('Frequency(Hz)');

ylabel('Amplitude');







