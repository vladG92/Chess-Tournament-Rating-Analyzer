# Chess-Tournament-Rating-Analyzer

This project came to me as an idea while I was reading the proposed FIDE Rating Changes for Jan 2024. I had known for a long time that junior players were very underrated, and invariably consulted the URS ratings in conjunction with published FIDE ratings to understand their reliability. Then, it occurred to me that I could potentially write an automated tool that parses URS data each month, then takes a single chess-results tournament link as an input to check two main things:

1) **FUTURE LOOKING**: How underrated/overrated a particular tournament might be, by comparing the average Elo to the average URS. This should help any amateur or professional player **decide on which tournament to play**, and which ones to avoid. My findings passed the eye test here, but use the tool at your own leisure and let me know what you find! The input takes the form of a single chess-results tournament link (make sure you pass the correct URL by selecting the English language in the interface, then navigating to the Starting List).

2) **PAST LOOKING**: How much do the final standings of a Swiss tournament correlate to the initial "seed numbers", as assigned to the players either by Elo or by URS. Here, we are talking about a simple R^2 correlation coefficient assuming a linear fit. Moreover, I have attempted to print a nice-looking table that's color coded to highlight outliers (overperforming or underperforming significantly), hence why I am providing .ipynb files, rather than .py scripts. The input here is again a single chess-results tournament link - the correct input should have the html page in English and the "Final Ranking after N rounds" as the selector.

To the extent that you're more curious about the methodology used and you want to get to work immediately:

-Run the 'URS ratings scraper and parser', which will access a webpage, download the monthly URS ratings Excel file, then store the FIDE ID, Name, and URS rating in a pickled Pandas   DataFrame (storing some tabulated data for easy future retrieval). Before you execute the code, please make sure you CHANGE the directory of the file download to match your desired one!     The estimated runtime of this program varies between 30 seconds to 2 minutes, depending on your hardware.

-Run either of the other two Jupyter Notebook files once you have stored the relevant URS dataframe locally. The output should be self-explanatory and the code should take less than   5 seconds to execute fully.

If you are curious about what the code actually accomplishes, or you want to learn more about Python, I suggest copying and pasting some code blocks into your favorite AI chatbot and asking it to elucidate the mystery. Truthfully, it helped me tremendously during the development of this little tool. If you don't know how to run the code, ask an AI chatbot to assist with installing Python on your machine, and specifically Jupyter Notebook, where the files should be run.

For any serious inquiries, you can reach me at https://twitter.com/vlad_chess. For not so serious inquiries, I shall once again recommend discussing with your favorite AI chatbot, who is infinitely more knowledgeable than the author of this repo.
