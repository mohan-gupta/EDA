# Spotify Song Popularity EDA

<img src="https://github.com/mohan-gupta/EDA/blob/main/Spotify%20song%20Popularity/plots/Spotify.jpg">
For this project, I have gathered data from Spotify web API.
[Spotipy](https://spotipy.readthedocs.io/en/2.19.0/) is a python library for making API calls to Spotify which makes the task al little easier.

### Data Collection Process
- First, I gathered the names of Top 100 artists.
- Then, using spotipy's search method, collected the Spotify ID of the artists.
- Using the artist's ID, gathered their album's ID.
- Then, collected the track ID of all the tracks in each album.
- Using track ID, I gathered the features and analysis of each track.

### Results from the Analysis

<img src = "https://github.com/mohan-gupta/EDA/blob/main/Spotify%20song%20Popularity/plots/data_dist.png"><br><br>
```instrumentalness```: Predicts whether a track contains no vocals. "Ooh" and "aah" sounds are treated as<br>
instrumental in this context. Rap or spoken word tracks are clearly "vocal". The closer the instrumentalness value<br>
is to 1.0, the greater likelihood the track contains no vocal content. Values above 0.5 are intended to represent<br>
instrumental tracks, but confidence is higher as the value approaches 1.0.<br>

```liveness```: Detects the presence of an audience in the recording. Higher liveness values represent an increased<br>
probability that the track was performed live. A value above 0.8 provides strong likelihood that the track is live.
<br><br>
<img src="https://github.com/mohan-gupta/EDA/blob/main/Spotify%20song%20Popularity/plots/corr_heatmap.png"><br><br>
- `num_samples` is completely correlated with `duration`, `start_of_fade_out`
- `loudness` has strong positive correlation with `energy` and negative correlation with `acousticness`
<br>Hence, we can also observe that energy is negatively correlated with acousticness
<br><br>

<img src="https://github.com/mohan-gupta/EDA/blob/main/Spotify%20song%20Popularity/plots/pop_cat.png"><br><br>
```time_signature```: An estimated time signature. The time signature (meter) is a notational convention to specify how many beats are in each bar (or measure). The time signature ranges from 3 to 7 indicating time signatures of "3/4", to "7/4".>= 3 <= 7
- time_signature = 4 has the highest median popularity

```key```: The key the track is in. Integers map to pitches using standard Pitch Class notation. E.g. 0 = C, 1 = C♯/D♭, 2 = D, and so on. If no key was detected, the value is -1. Ranging from -1 to 11.
- All keys have similar median value for popularity

```mode```: Mode indicates the modality (major or minor) of a track, the type of scale from which its melodic content is derived. Major is represented by 1 and minor is 0.
- Mode (Minor / Major) doesn't show any significant distinction 

```explicit```: It indicates the explicitness(explicit or not explicit) of the track. explicit is represented by 1 and not explicit by 0
- explicit = 1 has higher popularity than the explicit = 0
<br><br>

<img src="https://github.com/mohan-gupta/EDA/blob/main/Spotify%20song%20Popularity/plots/pop_cont.png"><br><br>
- The distribution of loudness is from -10 to 0 in which popularity is peaked around 25 to 65
- High energy Songs have higher popularity
- Non acoustic songs are more popluar
- Tracks have a tempo around 100-150 and their popularity ranges from 20-50. Hence, most of the popular songs are medium paced
- Songs with medium valence are more popular i.e., songs that are neither too cheerful nor too sad.
- Most of the songs in the data have a duration around 180 to 240 seconds and popularity of these songs is around 25 to 50
- The dataset consists of Medium Danceable songs with a popularity around 40
<br><br>

<img src="https://github.com/mohan-gupta/EDA/blob/main/Spotify%20song%20Popularity/plots/artist_songs.png"><br><br>
With Number of Songs equal to 540, `The Beatles` have the most songs
<br><br>

<img src="https://github.com/mohan-gupta/EDA/blob/main/Spotify%20song%20Popularity/plots/artist_popularity.png"><br><br>
Top 3 Artists with Highest avg Popularity are Bad Bunny, Harry Styles, Billie Eillish
<br><br>

<img src="https://github.com/mohan-gupta/EDA/blob/main/Spotify%20song%20Popularity/plots/artist_danceability.png"><br><br>
```danceability```: Danceability describes how suitable a track is for dancing based on a combination of musical elements<br>
including tempo, rhythm stability, beat strength, and overall regularity.<br>
A value of 0.0 is least danceable and 1.0 is most danceable.<br>
<b>On an average 21 Savage have 83% danceability in their songs, Cardi B and Young Thug both 79% danceability in 
their songs</b>
<br><br>

<img src="https://github.com/mohan-gupta/EDA/blob/main/Spotify%20song%20Popularity/plots/artist_energy.png"><br><br>
```energy```: Energy is a measure from 0.0 to 1.0 and represents a perceptual measure of intensity and activity. 
Typically, energetic tracks feel fast, loud, and noisy. For example, death metal has high energy, while a Bach 
prelude scores low on the scale. Perceptual features contributing to this attribute include dynamic range, perceived 
loudness, timbre, onset rate, and general entropy.<br>
<b>Marshmello, Fall Out Boy, Pitbull, and Metallica have the highest percentage of energy in their songs</b>
<br><br>

<img src="https://github.com/mohan-gupta/EDA/blob/main/Spotify%20song%20Popularity/plots/artist_valence.png"><br><br>
```valence```: A measure from 0.0 to 1.0 describing the musical positiveness conveyed by a track.<br>
Tracks with high valence sound more positive (e.g. happy, cheerful, euphoric), while tracks with<br>
low valence sound more negative (e.g. sad, depressed, angry). >= 0 <= 1.
<b>Artists with highest valence in their songs are J Balvin, Pitbull, Anuel AA</b>
<br><br>

<img src="https://github.com/mohan-gupta/EDA/blob/main/Spotify%20song%20Popularity/plots/artist_duration.png"><br><br>
```duration```: Length of the track.
<b>Metallica have the songs with higest avg duration equal to 5.8 minutes.</b>
<br><br>

<img src="https://github.com/mohan-gupta/EDA/blob/main/Spotify%20song%20Popularity/plots/artist_acoustic.png"><br><br>
```acousticness```: A confidence measure from 0.0 to 1.0 of whether the track is acoustic. 1.0 represents high confidence the track is acoustic. Ranging from 0 to 1.

<b>Billie Eillish, Sam Smith, Lana Del Rey and Adele have the highest acusticness in their songs</b>
<br><br>

<img src="https://github.com/mohan-gupta/EDA/blob/main/Spotify%20song%20Popularity/plots/artist_loudness.png"><br><br>
```loudness```: The overall loudness of a track in decibels (dB). Loudness values are averaged across the entire track and are useful for comparing relative loudness of tracks. Loudness is the quality of a sound that is the primary psychological correlate of physical strength (amplitude). Values typically range between -60 and 0 db.

<b>Marshmello, Anuel AA and Rauw Alejandro,their songs are more louder then any other artist's songs</b>
<br><br>

<img src="https://github.com/mohan-gupta/EDA/blob/main/Spotify%20song%20Popularity/plots/artist_tempo.png"><br><br>
```tempo```: The overall estimated tempo of a track in beats per minute (BPM).<br>
In musical terminology, tempo is the speed or pace of a given piece and derives directly from the average beat duration.

<b>Lil Nas X, Marshmello and Fall Out Boy have higher tempo in their songs</b>
<br><br>

To checkout the code refer to the [notebook](http://nbviewer.org/github/mohan-gupta/EDA/blob/main/Spotify%20song%20Popularity/Spotify%20song%20popularity.ipynb)
