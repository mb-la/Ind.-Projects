# Emotion Analysis Datasets

**1.** https://data.world/crowdflower/sentiment-analysis-in-text

This dataset contains labels for the emotional content (such as happiness, enthusiasm, sadness, and anger) of texts. Hundreds to thousands of examples across 13 labels. There are 40,000 rows and 4 columns. (text_emotion.csv)<br>

**Sample:**

1956967666	sadness	wannamama	Layin n bed with a headache  ughhhh...waitin on your call...

**2.** http://saifmohammad.com/WebPages/EmotionIntensity-SharedTask.html

Training and test datasets are provided for four emotions: joy, sadness, fear, and anger. For example, the anger training dataset has tweets along with a real-valued score between 0 and 1 indicating the degree of anger felt by the speaker. The test data includes only the tweet text.

**Sample:**

30015	@iamTinaDatta love you so much #smile ðŸ˜ŠðŸ˜Š	joy	0.896

20012	Im not a #nervouswreck, Im a #nervous #pileup. #GoingCrazy #HelpMe #Insane #Antisocial	fear	0.917

**3.** http://www.site.uottawa.ca/~diana/resources/emotion_stimulus_data/

The Emotion Cause dataset contains 820 sentences with both an emotion cause and an emotion tag. The tags are in the XML format: <cause> marks the beginning of the emotion stimulus span and <\cause> marks the end of the span. <br>
The No Cause dataset contains sentences marked with an emotion tag, which do not carry any emotion cause. This dataset contains 1594 instances marked with their emotion tag.
In both datasets, each sentence belongs to one of seven emotions: Happiness, Sadness, Anger, Fear, Surprise, Disgust and Shame.

**Sample:**

emotions and cause:
<happy>This did the trick : the boys now have a more distant friendship and David is much happier . <\happy>

emotions only:
<anger>Bernice was so angry she could hardly speak . <\anger>

**4.** http://web.eecs.umich.edu/~mihalcea/downloads/AffectiveText.Semeval.2007.tar.gz

 Affective Text: Classification of emotions in news headlines(Semeval  2007). There are 250 headlines. Categories:  0: anger, 1: disgust, 2: fear, 3: joy, 4: happiness, 5: sadness, 6: surprise. Annotation: emotions (anger disgust fear joy sadness surprise) + valence.

**Sample:**

emotions (id anger disgust fear joy sadness surprise): 245 0 0 0 54 0 6
valence (id valence): 245 52
corpus: <instance id="245">Melua's deep sea gig sets record </instance>

**5.** http://yanran.li/dailydialog.html

A manually labelled conversations dataset. It contains 13118 sentences. Categories: 0: no emotion, 1: anger, 2: disgust, 3:fear, 4: happiness, 5: sadness, 6: surprise.  
Annotation: topic number {1..10} (where 4 stands for Attitude&Emotion) + act number {1..4} + emotion number {0..6}.  

**Sample:**

corpus: dialogues_text.txt The kitchen stinks . __eou__ I'll throw out the garbage . __eou__
topic: dialogues_topic.txt 1
act: dialogues_act.txt 3 4
emotion: dialogues_emotion.txt 2 0

**6.** http://www.affective-sciences.org/index.php/download_file/view/395/296/

 Description: Over a period of many years during the 1990s, a large group of psychologists all over the world collected data in the ISEAR project, directed by Klaus R. Scherer and Harald Wallbott. Student respondents, both psychologists and non-psychologists, were asked to report situations in which they had experienced all of 7 major emotions (joy, fear, anger, sadness, disgust, shame, and guilt). In each case, the questions covered the way they had appraised the situation and how they reacted. The final data set thus contained reports on seven emotions each by close to 3000 respondents in 37 countries on all 5 continents. Size: 3000 respondents. Categories: joy, fear, anger, sadness, disgust, shame, guilt.  

**7.** http://people.rc.rit.edu/~coagla/affectdata/index.html

Tales emotion: Authors: Cecilia Ovesdotter Alm. Description: document classification task --classify the emotional affinity of sentences in the narrative domain of children's fairy tales. Size: 185 fairytales, 15292 sentences.
Annotation: emotions (Angry, Disgusted, Fearful, Happy, Sad) + moods (Positively surprised / Negatively surprised) + Neutral. Contact: ebbaalm@uiuc.edu

**Format:**

The document tales.txt lists the basenames of the story files.

The files ending in .emmod have the following format: SentID:SentID 1emLabelA:1emLabelB MoodLabelA:MoodLabelB Sent

They contain sentences with unmerged labels for the the annotators (A and B). The labels are: A: Angry, D: Disgusted, F: Fearful, H: Happy, N: Neutral, Sa: Sad for Primary emotion (1em) or S: Sad when is Mood, Su+: Positively Surprised for 1em, or + for Mood, Su- for 1em, or - for Mood.

The files ending in .sent.okpuncs contain the sentences and have the following format: sent

The files ending in .sent.okpuncs.props.pos contain the sentences pos tagged and have the following format: (Tag word):(Tag word) [...]

The files ending in .agreeID contain the IDs (numbers) of the sentences with full agreement on the affect. The labels used here are: Angry-Disgusted (merged), Fearful, Happy, Sad, and Surprised (merged). Neutral labels are not in!

The files ending in .agree contains only sentences with AFFECTIVE HIGH AGGREMENTS (see description for corresponding agreeID directory). The label codes are: 2=Angry-Disgusted, 3=Fearful, 4=Happy, 6=Sad, 7=Surprised and have the following format: SentID@AffectiveLabelCode@Sentence

**Sample:**

emmood: 0:0 N:N N:N Once upon a time there was a village shop.

sent.okpuncs: Once upon a time there was a village shop.

sent.okpuncs.props.pos: (RB Once):(IN upon):(DT a):(NN time):(EX there):(AUX was):(DT a):(NN village):(NN shop):(. .)

agreeID: 35

agree: 35@3@"It is very unpleasant, I am afraid of the police," said Pickles.
