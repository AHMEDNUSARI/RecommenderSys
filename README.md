# **Course Recommender System**

# **Overview**

The Course Recommender System helps users find the most suitable courses based on specific criteria such as course title, skill to be gained, or keywords. With a comprehensive dataset containing various details about thousands of courses, users can easily search for courses that match their learning preferences and goals.

The recommender system leverages data such as course ratings, duration, level, and topics to guide users in selecting the best courses. It also integrates a Large Language Model (LLM), Ollama2, to enhance the recommendation experience and provide more intuitive suggestions.

# **Dataset**

The dataset used in this project includes the following columns:

Course Title: Name of the course.
Rating: Course rating, represented as a floating point number.
Level: Difficulty level of the course (e.g., Beginner, Intermediate, Advanced).
Duration: Duration of the course in hours.
Schedule: Schedule type (e.g., Flexible).
Review: Number of reviews the course has received.
What You Will Learn: Main topics or skills covered by the course.
Skill Gain: Specific skills that users will gain from completing the course.
Modules: Overview of the course modules.
Instructor: Instructor(s) delivering the course.
Offered By: Organization or institution offering the course.
Keyword: Keywords associated with the course.
Course URL: URL link to the course.
Duration in Hours: Duration of the course represented in hours as a numerical value.
Functionalities
The recommender system enables users to:

Search for courses by title, skill gain, keywords, or any other attributes.
Filter courses based on specific criteria such as duration, level, or rating.
Visualize course distributions and trends using various libraries like Matplotlib, Seaborn, and Plotly.
Libraries Used
The following libraries are used for data processing, visualization, and LLM integration:

python
Copy code
import pandas as pd
import ast
import matplotlib.pyplot as plt
import seaborn as sns
from wordcloud import WordCloud
import plotly.express as px
import plotly.graph_objects as go
import plotly.io as pio
from tqdm import tqdm
The recommender system utilizes the Ollama2 LLM model to provide enhanced search and recommendation capabilities.

Usage Example

Suppose a user wants to find all courses that have a duration of exactly 20 hours. They can achieve this using the following command:


python

Copy code

filtered_courses = Data[Data['duration_in_hours'].astype(str).str.contains('20.0')]

Output:

Course Title	Rating	Level	Duration	Schedule	Review	What You Will Learn	Skill Gain	Modules	Instructor	Offered By	Keyword	Course URL	Duration in Hours
Fashion as Design	4.8	Beginner	20 hours (approximately)	Flexible schedule	2813	Art History, Art, History, Creativity Arts and...	Art History, Art, History, Creativity	Introduction, Heroes, Silhouettes, ...	Anna Burckhardt, Paola Antonelli ...	The Museum of Modern Art	Arts and Humanities	Course Link	20.0
The filtered courses will be displayed with all columns, making it easy for users to explore options.

# **Future Enhancements**

Some potential future improvements include:

Integration with Additional LLM Models: Exploring other models to provide deeper insights.

Personalized Recommendations: Implementing user profile-based recommendations for more personalized results.

Advanced Filtering Options: Allowing users to filter based on multiple attributes simultaneously.
