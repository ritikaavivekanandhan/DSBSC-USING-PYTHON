# DSBSC-USING-PYTHON
AIM

To generate and plot the message signal, carrier signal, and Amplitude Modulated (AM) signal using MATLAB, and to understand the waveform characteristics of AM.

EQUIPMENTS REQUIRED

• Computer with i3 Processor

• Colab

THEORY

Amplitude Modulation (AM) is a modulation technique in which the amplitude of a high-frequency carrier wave is varied in proportion to the instantaneous amplitude of the message (modulating) signal, while the frequency and phase of the carrier remain constant.

In AM, a low-frequency message signal (such as an audio signal) is superimposed on a high-frequency carrier wave to enable efficient transmission over long distances. The amplitude of the carrier changes according to the strength of the message signal, whereas the frequency and phase are unchanged.

ALGORITHM (Brief)

Start the program.

Initialize the parameters:

Message amplitude (Am)

Carrier amplitude (Ac)

Message frequency (fm)

Carrier frequency (fc)

Sampling frequency (fs)

Generate a time vector t using the sampling frequency and signal duration.

Generate the message signal using:

m(t)=Amcos⁡(2πfmt)
m(t)=Amcos(2πfmt)
Generate the carrier signal using:
c(t)=Accos⁡(2πfct)
c(t)=Accos(2πfct)

Multiply the message and carrier signals to obtain the DSB-SC modulated signal:

s(t)=m(t)×c(t)
s(t)=m(t)×c(t)

Plot the message signal, carrier signal, and modulated signal using matplotlib.

Display the waveforms.

Stop the program.

Program
~~~~~~~~
Am=3.0;
fm=194;
Ac=6.0;
fc=1940;
fs=19400;
t=0:1/fs:2/fm;
m=Am*cos(2*3.14*fm*t);
subplot(3,1,1);
plot(t,m);
c=Ac*cos(2*3.14*fc*t);
subplot(3,1,2);
plot(t,c);
s1=(Ac+m).*cos(2*3.14*fc*t);
s2=(Ac-m).*cos(2*3.14*fc*t);
s=s1-s2;
subplot(3,1,3);
plot(t,s);
~~~~~~~~

OUTPUT WAVEFORM
 
 <img width="1920" height="1200" alt="Screenshot (105)" src="https://github.com/user-attachments/assets/89799486-fc5a-40df-b17e-84816bed693b" />

TABULATION

![WhatsApp Image 2025-10-24 at 16 11 49_c4e57dd2](https://github.com/user-attachments/assets/15e80e2c-44aa-44c7-811f-d59966ea91fd)

MODEL GRAPH

<img width="703" height="679" alt="image" src="https://github.com/user-attachments/assets/9642d21b-efd0-45e7-8ffd-dc7596f62e20" />

RESULT

The experiment successfully generates and displays the message, carrier, and amplitude-modulated signals, demonstrating the concept of amplitude modulation.

