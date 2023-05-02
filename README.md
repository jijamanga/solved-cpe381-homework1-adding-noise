Download Link: https://assignmentchef.com/product/solved-cpe381-homework1-adding-noise
<br>
Write a program in C/C++ to perform real-time audio signal processing. The program will read audio record from WAV file, perform the processing <u>sample-by-sample</u>, and store the result back to the new WAV file. All necessary functions must be implemented, external libraries are not allowed, except for the Bonus Assignment.

<strong> Phase I </strong>

Please follow the following steps:

<ol>

 <li>Record your own voice in wave file (.WAV). The record must start with your introduction of yourself, followed with additional content (e.g. music). The record length must be 16 s&lt; T<sub>rec </sub>&lt;18 s.</li>

 <li>Read WAV file in Matlab and replace signal from time <em>t</em>=10sec to the end of the file with the sine wave <em>f=</em>2,500 Hz and amplitude equal to 10% of the maximum possible amplitude of the signal, and initial phase of π/6. Save modified WAV file. When you play the file you will be able to hear your original recording for 10 seconds followed by annoying sine wave @2,500 Hz for the rest of the file.</li>

 <li>Write C/C++ program to read the file from previous step and write modified WAV file. Program should process file sample by sample, and write the output at time <em>t </em>as                <em>out(t)</em> = <em>in(t)</em> + 0.1*<em>n(t)</em> + 0.05*<em>rn(t) </em>where:

  <ul>

   <li><em>in(t)</em> is input from WAV file at time <em>t, </em></li>

   <li><em>n(t)</em> is added “noise” sine wave with amplitude equal to the maximum amplitude of the signal and frequency of 2,000 Hz (check size of your sample to determine maximum amplitude of the signal), and</li>

   <li><em>rn(t) </em>is random noise.</li>

  </ul></li>

</ol>

Please note that the processing may create overflow that you must compensate for. Measure the performance of the program (<em>end-time – start_time</em>) with minimum resolution of 1 ms.

<ol start="4">

 <li>Write another summary text file that outputs: filename, the sampling frequency, number of channels, number of bits per sample, record length in seconds calculated from the number of samples, maximum absolute value of the sample in input file, channel that has the maximum absolute value of the sample, and execution time of the program.</li>

</ol>




Prepare Report and submit both hard and soft copy of the report. The report must contain the following numbered sections:

<ol>

 <li>Short description of the problem and proposed solution.</li>

 <li>Short description of WAV file format. What control fields do you have in the header? What is their location?</li>

 <li>Summary text file. Explain if your program can work in real-time.</li>

</ol>

<h1>Deliverables</h1>

<ul>

 <li>Complete source code of your project (MS Visual Studio or Linux gcc/g++ with all files necessary to compile the project &amp; make file in the single ZIP file).</li>

 <li>Projects that can not be compiled and run in either environment will lose 40% of the grade. Only original and independent work will be graded. Plagiarized work will not receive any credit.</li>

 <li>PDF or DOC/DOCX file of your Report with the following format of the filename: Lastname_first-initial.DOC or PDF</li>

 <li>Summary file in the following format:            txt •         Sound files in the following format (use your last name and first initial): o LastName_FirstInitial_orig.WAV    – original record</li>

</ul>

o LastName_FirstInitial_mod.WAV              – processed record

<strong>          </strong>

<strong>Phase II</strong> Please follow the following steps:

<ol>

 <li>Use wave file from Phase I.</li>

 <li>Read WAV file in Matlab and find the dominant spectral component in the signal (frequency and amplitude) for t&lt;10s and t&gt;10s.</li>

 <li>Design a filter to eliminate added sine wave @2,000 Hz from Phase I with minimum attenuation of 60dB. Pay attention to trade-off between real-time performance and the quality of the filter. Describe implementation of your filter. Discuss your decisions in the report.</li>

 <li>Write C/C++ program to read the file, check the sampling frequency from the file header and select appropriate filter for that frequency. It is acceptable to assume that you will have only two standard sampling frequencies (Fs), but you must process the signal according to the sampling frequency of the record. Measure the performance of the program (<em>end-time – start_time</em>).</li>

</ol>

Prepare Report and submit hard and soft copy of the report. The report must contain the following numbered sections:

<ol>

 <li>Short description of the problem and proposed solution.</li>

 <li>Documented design of the filter in Matlab that includes

  <ol>

   <li>Plot of filter characteristics (magnitude and phase) for both filters/sampling frequencies</li>

   <li>Type of filter (FIR/IIR) and reasons for choosing that particular filter.</li>

   <li>Organization of processing; how do you perform your processing in C/C++.</li>

  </ol></li>

 <li>Spectrum of the input WAV file and spectrum of the processed file for t&lt;10s and t&gt;10s.</li>

 <li>Performance of the program (execution time). Explain if your program can work in real-time.</li>

 <li>Short description of your experience and “lessons learned”</li>

</ol>







<h1>Deliverables</h1>

<ul>

 <li>Complete source code of your project (MS Visual Studio or Linux gcc/g++ with all files necessary to compile the project &amp; make file in the single ZIP file).</li>

 <li>Projects that can not be compiled and run in either environment will lose 40% of the grade. Only original and independent work will be graded. Plagiarized work will not receive any credit.</li>

 <li>PDF or DOC file of your Report with the following format of the filename: LastName_FirstInitial.DOC or PDF</li>

 <li>Matlab script used to prepare the assignment.</li>

 <li>Sound files in the following format (use your last name and first initial):</li>

</ul>

o LastName_FirstInitial_orig.WAV – original record o LastName_FirstInitial_mod.WAV – modified record o LastName_FirstInitial_filt.WAV          – filtered output

<strong>Bonus Assignment </strong>

Write a C/C++ program to determine the dominant spectral component in WAV file using FFT analysis and total power of the signal (RMS value) for each one second window with 50% window overlap. Save CSV text file with “LastName_FirstInitial_bonus.csv”. The file must have first line representing names of variables: “time, fmax,power” followed with results in each window.

Full credit (20% bonus) can be received if you provide the same documentation of the design and performance of the additional solution.


