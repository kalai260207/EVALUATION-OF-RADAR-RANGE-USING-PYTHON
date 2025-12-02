# EVALUATION-OF-RADAR-RANGE-USING-PYTHON

Aim
To calculate the maximum range of a radar system using the Radar Range Equation and verify the results through Python programming.
Theory
The Radar Range Equation is a fundamental formula used in radar system design to determine the maximum range at which a radar can detect a target. It is given by:

<img width="462" height="427" alt="image" src="https://github.com/user-attachments/assets/c0f2a37e-9944-4c91-a605-ef4c6a4995f9" />

Procedure
1.Set Up the Python Environment: Ensure that Python is installed on your system. You can use Anaconda for managing Python packages and environments, or any other Python IDE of your choice. 2.Import Necessary Libraries: Import the math library in Python. 3.Define the Radar Range Equation Function: Create a function to calculate the maximum range using the Radar Range Equation. 4.Input Parameters for the Radar System: Define the input parameters such as transmitted power, transmitter gain, receiver gain, radar frequency, radar cross section, and minimum detectable power. 5.Calculate the Maximum Range: Use the function to calculate the maximum range of the radar. 6.Execute the Program: Run the Python script to calculate and display the maximum range of the radar.

Program
```
Pt = 1000;
G = 1000;
sigma = 1;
Ae = 10;

Smin = logspace(-12, -6, 100);
Rmax = ((Pt * G * sigma * Ae) ./ (16 * %pi^2 .* Smin)).^(1/4);
subplot(3,1,1);
plot(Smin, Rmax);

Ppeak = linspace(100, 10000, 100);
Rmax2 = ((Ppeak * G * sigma * Ae) ./ (16 * %pi^2 * 1e-10)).^(1/4);
subplot(3,1,2);
plot(Ppeak, Rmax2);

Gt = linspace(100, 2000, 100);
Rmax3 = ((Pt * Gt * sigma * Ae) ./ (16 * %pi^2 * 1e-10)).^(1/4);
subplot(3,1,3);
plot(Gt, Rmax3);
```

Output

![WhatsApp Image 2025-11-26 at 12 21 49 AM](https://github.com/user-attachments/assets/16270b5c-4dc1-4e61-b125-f4009e48f8a3)

Tabulation

![WhatsApp Image 2025-12-02 at 4 36 06 PM](https://github.com/user-attachments/assets/a20c3a46-bf1a-47cf-81de-db65b35a7fc4)


Result

Thus, the maximum range of a radar system calculated using the Radar Range Equation is successfully verified using Scilab programming.
