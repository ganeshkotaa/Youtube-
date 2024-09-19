YouTube Transcript Analysis and Chaptering
This project retrieves the transcript of a YouTube video, performs various analyses, and generates readable chapters based on the transcript's content. Using natural language processing (NLP) techniques such as word frequency analysis, topic modeling, and key phrase extraction, this script organizes the transcript into chapters and assigns meaningful names to each section.

Features

Transcript Retrieval:
Automatically fetches the transcript of a YouTube video using the youtube-transcript-api.
Word Frequency Analysis: Visualizes the most common words used in the video.
Topic Modeling: 
Uses Non-negative Matrix Factorization (NMF) to identify the main topics discussed in the video.
Chapter Generation: Identifies logical breaks in the transcript and generates chapter points with descriptive titles based on key phrases.
CSV Export:
Saves the transcript and its corresponding chapter data in a CSV file.
Prerequisites

To run this project, you will need the following:
Python 3.x
Google YouTube Data API Key

Required Python libraries (can be installed using pip):
pip install google-api-python-client youtube-transcript-api pandas numpy matplotlib scikit-learn
Installation

Clone the repository:
git clone https://github.com/your-repo/youtube-transcript-analysis.git
cd youtube-transcript-analysis

Install the required packages:
pip install -r requirements.txt

Set up your API key:
Obtain a YouTube Data API key from the Google Cloud Console.
Replace the placeholder API_KEY in the script with your actual API key.
Usage

Run the script:
python main.py
Enter the YouTube video URL when prompted.

The script will:
Retrieve the transcript of the video.
Save the transcript to a CSV file named after the video ID.
Perform word frequency analysis and topic modeling on the transcript.
Generate readable chapters and output them with time points.
After running the script, check the console output for the generated chapter points and names.

Example
Enter the YouTube video link: https://www.youtube.com/watch?v=4QkYy1wANXA&list=PLeo1K3hjS3utcb9nKtanhcn8jd2E0Hp9b&index=2
Transcript saved to 4QkYy1wANXA_transcript.csv


Project Structure
main.py: The main script that retrieves the transcript, analyzes the text, and generates chapters.
requirements.txt: Lists all the dependencies for this project.
README.md: This file.

Functions Overview
get_video_id(url): Extracts the video ID from a YouTube URL.
get_video_title(video_id): Retrieves the video title using the YouTube API.
get_video_transcript(video_id): Fetches the transcript for the given video.
save_to_csv(title, transcript, filename): Saves the transcript along with the video title to a CSV file.
display_topics(model, feature_names, no_top_words): Extracts and displays the top words for each topic identified by the NMF model.
main(): Orchestrates the entire process from URL input to transcript saving and analysis.

Output
Transcript CSV: A CSV file containing the transcript with time stamps and text.
Word Frequency Plot: A histogram showing the distribution of word counts in the transcript.
Topic Modeling: A list of the top 10 topics discussed in the video.
Chapters: Readable chapter points with times and descriptive titles.

Visualization
The project generates visualizations such as:
Histogram of text lengths in the transcript.
Bar chart of the top 20 most frequent words.
Future Improvements
Add support for videos without transcripts using speech-to-text.
Enhance chapter naming by using more sophisticated keyphrase extraction methods.
Integrate support for different languages.

License
This project is licensed under the MIT License - see the LICENSE file for details.






