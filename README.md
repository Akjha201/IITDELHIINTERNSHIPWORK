# IITDELHIINTERNSHIPWORK
This will contain all the work that I do during the course of one month onsite internship at IIT Delhi.

# NIST Randomness Tests: 
1. Frequency (Monobit) TestLogic: A truly random binary sequence should have roughly the same number of 0s and 1s. This test quantifies the difference between the observed number of 1s and the expected number (which is N/2, where N is the sequence length).
   Key Concept: Calculate the test statistic S_1 (a normalized count based on the number of 1s), which is then compared against the chi^2 distribution or transformed into a P-value using the complementary error function.
   Implementation Note: Convert the 0s to -1s and the 1s to 1s. The sum of this sequence gives a measure of the bias. The normalized absolute value of this sum is the statistic.

2. Runs TestLogic: A run is an uninterrupted sequence of identical bits (e.g., 111 or 00). This test checks if the number of runs observed (of both 0s and 1s) is consistent with the number expected in a random sequence. If there are too many or too few runs, the sequence is non-random.
   Key Concept: The expected number of runs, V, is based on the proportion of 0s and 1s in the sequence (pi_0 and pi_1). The test statistic is based on the squared difference between the observed number of runs and the expected number, leading to a chi^2 statistic.
   Implementation Note: The test must first pass the Frequency (Monobit) Test. Count the number of runs by detecting transitions (e.g., 0 to 1 or 1 to 0).
