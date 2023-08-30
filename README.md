# Matching Job Descriptions with Resumes

This script is designed to match job descriptions with resumes and calculate a percentage match based on the skills mentioned in both the job description and the resume. It uses the concept of cosine similarity to quantify the match between the text data.

## How it works

1. **Vectorization**: It starts by vectorizing the job description and each resume. Vectorization is the process of converting text data into numerical vectors. In this case, it uses the `CountVectorizer` from the scikit-learn library to convert the text into a numerical format.

2. **Cosine Similarity**: After vectorization, it calculates the cosine similarity between the job description and each resume. Cosine similarity measures the cosine of the angle between two non-zero vectors in an inner product space. In simpler terms, it quantifies how similar two vectors (in this case, text vectors) are. The closer the cosine similarity is to 1, the more similar the vectors are.

3. **Skill Matching**: It also checks for matching skills between the job description and the resume. It splits the skills mentioned in the job description and compares them with the skills mentioned in the resume, ignoring case sensitivity. If there are matching skills, it proceeds to calculate the match percentage.

4. **Recording Matches**: If there are matches found between the job description and the resume, it records the job description index, resume index, and the rounded match percentage in a list.

5. **Exporting Results**: If there are any matches found, it exports the results to a CSV file named 'matched_data_CS.csv', which contains columns for job description index, resume index, and rounded match percentage.

6. **No Matches**: If no matches are found between job descriptions and resumes, it prints a message indicating that no matches were found.

## How to Use

To use this script, follow these steps:

1. Ensure you have the required libraries installed, including `pandas` and `scikit-learn`.

2. Prepare your data in two DataFrames (`df1` and `df2`) with columns 'Skills', 'Job Description', and 'Resume'. `df1` should contain job descriptions, and `df2` should contain resumes.

3. Run the script.

4. Check the output message. If matches are found, the script will export the results to a CSV file named 'matched_data_CS.csv'.

5. You can further analyze the results using the CSV file to identify the best-matched resumes for each job description.

Feel free to modify the script to suit your specific use case or integrate it into your project as needed.
