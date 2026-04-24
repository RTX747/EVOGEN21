# EVOGEN21
Custom dataset created for music genre classification and music genre evolution tasks.
It was originally created and utilized in the research paper "Beyond the Decision Boundary: Genre Evolution," published in TBD Conference, 2026. Please cite the associated publication if this dataset is used in your work.

## Copyright Disclaimer
This dataset is provided for academic research purposes only. Any commercial use is strictly prohibited.
Song titles and artist names belong to their respective copyright holders.
Dataset does not contain audio files or lyrics of the songs.

## Dataset Description
The dataset comprises 2100 hit songs from 5 mainstream genres (Rock, Hip-hop, EDM, Indie-folk, Country). Songs were manually selected from U.S.-based sources such as Billboard hit charts and Spotify/Apple Music curated annual/decade genre playlists, covering a 21-year period (2005-2025). The dataset is temporally balanced, containing 20 songs per genre for each year. Our song selection criteria ensured that each genre’s musical trends are correctly represented by its most popular songs from each year. While some songs stay in the charts for several years, we only picked the songs that were released either within the chart year or the year before.

Audio features are extracted using Librosa library. All audio features are mean-aggregated. Parameters used for audio signal preprocessing and feature extraction are : 48000 sampling rate, 4096 window size, 8192 FFT size, 1024 hop size, 128 n_mels, 24000 f_max.

Lyrics features are extracted using Python's built-in modules. The standard preprocessing steps (symbol and whitespace removal) are applied to raw song lyrics, while tokenization was intentionally avoided to retain the original forms of slightly different rhyming phrases. 

## Dataset Content
The dataset includes 44 features (40 audio features, 4 lyrics features) extracted from full-length audio files and lyrics. Except the song duration feature, the selected audio features were focused on harmonic and timbral content of the audio in order to capture genre-specific tonal and spectral characteristics.

### AUDIO FEATURES:

A. Timbral Audio Features Group:

Zero Crossing Rate (ZCR), Root Mean Square (RMS), Spectral Centroid, Spectral Flatness, Spectral Bandwidth, Spectral Rolloff, Spectral Contrast Band (0 to 6), Mel-frequency Cepstral Coefficients (MFCCs from 0 to 19)

B. Harmonic Audio Features Group:

Tonnetz (X and Y for fifth, minor, major types)

### LYRICS FEATURES:

A. Lexical Statistics Lyrics Features Group:

Lyrics Word Count, Words Per Second

B. Repetitiveness Lyrics Features Group:

Unique Words Ratio, LZW Compression Ratio

### SONG DETAILS FEATURES:

Duration Seconds, Chart Year, Artist, Song, Sample No, Genre
