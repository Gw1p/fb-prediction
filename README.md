# Using Non-Standard Models for Football Predictions: Elo, TrueSkill, Neural Networks
**by Anton Bendrikov**

**Supervisor: Prof Paul Krause**

All the code is within a single Jupyter Notebook `ab01719.ipynb`.

The file should be followed from the top to bottom. It starts by importing all the data, running tests and pre-processing.

Then, the file is split in sections with appropriate headings:

- Elo-related operations can be found under Elo
- TrueSkill model is developed under TrueSkill
- Neural Network is the largest section and contains all the workings for developing an MLP


Models' sections generally parse the data into correct format and setup the required dependencies, then grid-search the relevant parameters before presenting final evaluation.


## Set Up

### Data

In this project, data for England Premiership, France Championnat, Germany Bundesliga and Italy Serie A is used. Additionally, NBL, NFL, Super Rugby and Twenty20 Big Bash data is utilised when evaluating the Neural Network.

The relevant data can be downloaded from:

- England Premiership (seasons 2008/09 - 2018/19) [https://www.football-data.co.uk/englandm.php](https://www.football-data.co.uk/englandm.php)
- France Championnat (seasons 2008/09 - 2018/19) [https://www.football-data.co.uk/francem.php](https://www.football-data.co.uk/francem.php)
- Germany Bundesliga (seasons 2008/09 - 2018/19) [https://www.football-data.co.uk/germanym.php](https://www.football-data.co.uk/germanym.php)
- Italy Serie A (seasons 2008/09 - 2018/19) [https://www.football-data.co.uk/italym.php](https://www.football-data.co.uk/italym.php)
- NBL (seasons seasons 2009/10 - 2018/19) [http://www.aussportsbetting.com/data/historical-nbl-results-and-odds-data/](http://www.aussportsbetting.com/data/historical-nbl-results-and-odds-data/)
- NFL (seasons 2008 - 2018) [http://www.aussportsbetting.com/2013/07/01/nfl-historical-odds-data/](http://www.aussportsbetting.com/2013/07/01/nfl-historical-odds-data/)
- Twenty20 Big Bash (seasons 2009 - 2019) [http://www.aussportsbetting.com/data/historical-twenty20-big-bash-results-and-odds-data/](http://www.aussportsbetting.com/data/historical-twenty20-big-bash-results-and-odds-data/)
- Super Rugby (seasons 2011/12 - 2018/19) [http://www.aussportsbetting.com/data/historical-super-rugby-results-and-odds-data/](http://www.aussportsbetting.com/data/historical-super-rugby-results-and-odds-data/)

### Formatting the Data

Once the relevant data is downloaded, it should be placed in the relevant folder under `source/Data/<competition_name>`.


The file names need to be formatted as follows:

- England Premiership: `Permier20XX-20YY.csv`
- France Championnat: `Championnat20XX-20XX.csv`
- Germany Bundesliga: `Bundesliga20XX-20XX.csv`
- Italy Serie A: `SerieA20XX-20XX.csv`
- NBL: `NBL20XX-20XX.csv`
- NFL: `NFL20XX-20XX.csv`
- Twenty20 Big Bash: `TwentyBigBash20XX-20XX.csv`
- Super Rugby: `SuperRugby20XX-20XX.csv`


Alternatively, modify calls to `get_sport_data` to format file names according to a different format.

## Dependencies

See `requirements.txt`
