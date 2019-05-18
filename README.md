# The State of the Art of Scene Text End-to-end (Detection and Recognition) 


* 1 [Datasets](#Datasets)
* 2 [End-to-end Results](#Results)
* 3 [Reference (paper, code)](#Reference)

## Datasets
- **Street View Text (SVT)** [SVT-download](http://vision.ucsd.edu/~kai/grocr/)

  **Introduction:** There are 100 training images and 250 testing images downloaded from Google Street View of road-side scenes. The labelled text can be very challenging with a wide variety of fonts, orientations, and lighting conditions. A lexicon containing 50 words (SVT-50) is also provided for each image. 

  * K. Wang, B. Babenko, and S. Belongie, “End-to-end scene text recognition,” in Proc. IEEE ICCV, Nov. 2011, pp. 1457–1464.

- **ICDAR 2003(IC03)** [IC03-download](http://www.iapr-tc11.org/mediawiki/index.php?title=ICDAR_2003_Robust_Reading_Competitions)

  **Introduction:** The dataset contains a varied array of photos of the world that contain scene text. There are 251 testing images with 50 word lexicons (IC03-50) and a lexicon of all test groundtruth words (IC03-Full). 
  * S. M. Lucas, A. Panaretos, L. Sosa, A. Tang, S. Wong, and R. Young, “ICDAR 2003 robust reading competitions,” in Proc. 7th ICDAR, Aug. 2003, pp. 682–687.

- **ICDAR 2011(IC11)** [IC11-download](http://robustreading.opendfki.de/trac/wiki/SceneText)

  **Introduction:** The dataset is an extension to the dataset used for the text locating competitions of ICDAR 2003.It includes 485 natural images in total. 

  * A. Shahab, F. Shafait, and A. Dengel, “ICDAR 2011 robust reading competition challenge 2: Reading text in scene images,” in Proc. ICDAR, 2011, pp. 1491–1496.


- **ICDAR 2013 (IC13)** [IC13-download](http://dagdata.cvc.uab.es/icdar2013competition/?ch=2&com=downloads)

  **Introduction:** The dataset consists of 229 training images and 233 testing images. Most text are horizontal. Three speciﬁc lexicons are provided, named as “Strong(S)”, “Weak(W)” and “Generic(G)”. “Strong(S)” lexicon provides 100 words per-image including all words that appear in the image. “Weak(W)” lexicon includes all words that appear in the entire test set. And “Generic(G)” lexicon is a 90k word vocabulary. 
  * D. Karatzas, F. Shafait, S. Uchida, M. Iwamura, L. G. i Bigorda, S. R. Mestre, J. Mas, D. F. Mota, J. A. Almazan, and L. P. de las Heras. "ICDAR 2013 robust reading competition," in Proc. ICDAR, 2013, pp. 1484–1493.

- **ICDAR 2015 (IC15)** [IC15-download](http://rrc.cvc.uab.es/?ch=4&com=downloads)

  **Introduction:** The dataset includes 1000 training images and 500 testing images captured by Google glasses. The text in the scene is in arbitrary orientations. Similar to ICDAR 2013, it also provides “Strong(S)”, “Weak(W)” and “Generic(G)” lexicons. 

  * D. Karatzas, L. Gomez-Bigorda, A. Nicolaou, S. Ghosh, A. Bagdanov, M. Iwamura, J. Matas, L. Neumann, V. R. Chandrasekhar, S. Lu, et al. "ICDAR 2015 competition on robust reading," in Proc. ICDAR, 2015, pp. 1156–1160. 

- **Total-Text** [Total-Text-download](https://github.com/cs-chan/Total-Text-Dataset)

  **Introduction:** Except for the horizontal text and oriented text, Total-Text also consists of a lot of curved text. Total-Text contains 1255 training images and 300 test images. All images are annotated with polygons and transcriptions in word-level. A “Full” lexicon contains all words in test set is provided. 

  * Chng, C.K., Chan, C.S. "Total-text: A comprehensive dataset for scene text detection and recognition," in: Proc. ICDAR, 2017, pp. 935–942.

## Results

<table cellspacing="0" border="0" style='white-space: nowrap;'>
	<colgroup width="157"></colgroup>
	<colgroup width="132"></colgroup>
	<colgroup width="764"></colgroup>
	<colgroup width="246"></colgroup>
	<colgroup width="296"></colgroup>
	<colgroup width="98"></colgroup>
	<colgroup span="3" width="62"></colgroup>
	<colgroup width="57"></colgroup>
	<colgroup width="44"></colgroup>
	<colgroup width="38"></colgroup>
	<colgroup width="40"></colgroup>
	<colgroup width="38"></colgroup>
	<colgroup width="40"></colgroup>
	<colgroup width="44"></colgroup>
	<colgroup width="40"></colgroup>
	<colgroup span="6" width="35"></colgroup>
	<colgroup width="38"></colgroup>
	<colgroup width="41"></colgroup>
	<colgroup width="47"></colgroup>
	<colgroup width="63"></colgroup>
	<tr>
		<td colspan=27 height="33" align="center" valign=middle>Scene Text End-to-end Results</td>
		</tr>
	<tr>
		<td rowspan=3 height="57" align="center" valign=middle>Method</td>
		<td rowspan=3 align="center" valign=middle>Model</td>
		<td rowspan=3 align="center" valign=middle>Highlight</td>
		<td rowspan=3 align="center" valign=middle>Detection</td>
		<td rowspan=3 align="center" valign=middle>Recognition</td>
		<td rowspan=3 align="center" valign=middle>SVT</td>
		<td rowspan=3 align="center" valign=middle>SVT-50</td>
		<td colspan=3 rowspan=2 align="center" valign=middle>IC03</td>
		<td rowspan=3 align="center" valign=middle>IC11</td>
		<td colspan=6 align="center" valign=middle>IC13</td>
		<td colspan=6 align="center" valign=middle>IC15</td>
		<td colspan=2 align="center" valign=middle>Total-text</td>
		<td rowspan=3 align="center" valign=middle>Time</td>
		<td rowspan=3 align="center" valign=middle>Source</td>
	</tr>
	<tr>
		<td colspan=3 align="center" valign=middle>End-to-end</td>
		<td colspan=3 align="center" valign=middle>Spotting</td>
		<td colspan=3 align="center" valign=middle>End-to-end</td>
		<td colspan=3 align="center" valign=middle>Spotting</td>
		<td rowspan=2 align="center" valign=middle>None</td>
		<td rowspan=2 align="center" valign=middle>Full</td>
		</tr>
	<tr>
		<td align="center" valign=middle sdval="50" sdnum="1033;">50</td>
		<td align="center" valign=middle>Full</td>
		<td align="center" valign=middle>None</td>
		<td align="center" valign=middle>S</td>
		<td align="center" valign=middle>W </td>
		<td align="center" valign=middle>G</td>
		<td align="center" valign=middle>S</td>
		<td align="center" valign=middle>W </td>
		<td align="center" valign=middle>G</td>
		<td align="center" valign=middle>S</td>
		<td align="center" valign=middle>W </td>
		<td align="center" valign=middle>G</td>
		<td align="center" valign=middle>S</td>
		<td align="center" valign=middle>W </td>
		<td align="center" valign=middle>G</td>
		</tr>
	<tr>
		<td height="19" align="center" valign=middle>Wang et al. [1]</td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle>Word Re-scoring for NMS</td>
		<td align="center" valign=middle>Sliding windows and Random Ferns</td>
		<td align="center" valign=middle>Pictorial Structures</td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle sdval="51" sdnum="1033;">51</td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle sdval="2011" sdnum="1033;">2011</td>
		<td align="center" valign=middle>ICCV</td>
	</tr>
	<tr>
		<td height="19" align="center" valign=middle>Wang et al. [2]</td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle>CNN architecture</td>
		<td align="center" valign=middle>CNN-based</td>
		<td align="center" valign=middle>Sliding windows for classification</td>
		<td align="center" valign=middle sdval="46" sdnum="1033;">46</td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle sdval="72" sdnum="1033;">72</td>
		<td align="center" valign=middle sdval="67" sdnum="1033;">67</td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle sdval="2012" sdnum="1033;">2012</td>
		<td align="center" valign=middle>ICPR</td>
	</tr>
	<tr>
		<td height="19" align="center" valign=middle>Jaderberg et al. [3]</td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle>Data mining and annotation</td>
		<td align="center" valign=middle>CNN-based and saliency maps</td>
		<td align="center" valign=middle>CNN classifier</td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle sdval="56" sdnum="1033;">56</td>
		<td align="center" valign=middle sdval="80" sdnum="1033;">80</td>
		<td align="center" valign=middle sdval="75" sdnum="1033;">75</td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle sdval="2014" sdnum="1033;">2014</td>
		<td align="center" valign=middle>ECCV</td>
	</tr>
	<tr>
		<td height="19" align="center" valign=middle>Alsharif et al. [4]</td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle>Hybrid HMM maxout models</td>
		<td align="center" valign=middle>CNN and hybrid HMM maxout models</td>
		<td align="center" valign=middle>Segmentation-based</td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle sdval="48" sdnum="1033;">48</td>
		<td align="center" valign=middle sdval="77" sdnum="1033;">77</td>
		<td align="center" valign=middle sdval="70" sdnum="1033;">70</td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle sdval="2014" sdnum="1033;">2014</td>
		<td align="center" valign=middle>ICLR</td>
	</tr>
	<tr>
		<td height="19" align="center" valign=middle>Yao et al. [5]</td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle>(1) Detection and recognition features sharing. (2) Oriented-text. (3) A new dictionary search method</td>
		<td align="center" valign=middle>Random Forest</td>
		<td align="center" valign=middle>Component Linking and Word Partition</td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle sdval="48.6" sdnum="1033;">48.6</td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle sdval="2014" sdnum="1033;">2014</td>
		<td align="center" valign=middle>TIP</td>
	</tr>
	<tr>
		<td height="19" align="center" valign=middle>Neumann et al. [6]</td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle>Real-time performance(1.6s/image)</td>
		<td align="center" valign=middle>Extremal Regions</td>
		<td align="center" valign=middle>Clustering algorithm to group characters</td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle sdval="68.1" sdnum="1033;">68.1</td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle sdval="45.2" sdnum="1033;">45.2</td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle sdval="35" sdnum="1033;">35</td>
		<td align="center" valign=middle sdval="19.9" sdnum="1033;">19.9</td>
		<td align="center" valign=middle sdval="15.6" sdnum="1033;">15.6</td>
		<td align="center" valign=middle sdval="35" sdnum="1033;">35</td>
		<td align="center" valign=middle sdval="19.9" sdnum="1033;">19.9</td>
		<td align="center" valign=middle sdval="15.6" sdnum="1033;">15.6</td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle sdval="2015" sdnum="1033;">2015</td>
		<td align="center" valign=middle>TPAMI</td>
	</tr>
	<tr>
		<td height="19" align="center" valign=middle>Jaderberg et al. [7]</td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle>Trained only on data produced by a synthetic text generation engine, requiring no human labelled data</td>
		<td align="center" valign=middle>Region proposal mechanism</td>
		<td align="center" valign=middle>Word-level classification</td>
		<td align="center" valign=middle sdval="53" sdnum="1033;">53</td>
		<td align="center" valign=middle sdval="76" sdnum="1033;">76</td>
		<td align="center" valign=middle sdval="90" sdnum="1033;">90</td>
		<td align="center" valign=middle sdval="86" sdnum="1033;">86</td>
		<td align="center" valign=middle sdval="78" sdnum="1033;">78</td>
		<td align="center" valign=middle sdval="76" sdnum="1033;">76</td>
		<td align="center" valign=middle sdval="76" sdnum="1033;">76</td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle sdval="2016" sdnum="1033;">2016</td>
		<td align="center" valign=middle>IJCV</td>
	</tr>
	<tr>
		<td height="19" align="center" valign=middle>Liao et al. [8]</td>
		<td align="center" valign=middle>TextBoxes</td>
		<td align="center" valign=middle>An end-to-end trainable fast scene text detector</td>
		<td align="center" valign=middle>SSD-based framework</td>
		<td align="center" valign=middle>CRNN</td>
		<td align="center" valign=middle sdval="64" sdnum="1033;">64</td>
		<td align="center" valign=middle sdval="84" sdnum="1033;">84</td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle sdval="87" sdnum="1033;">87</td>
		<td align="center" valign=middle sdval="91" sdnum="1033;">91</td>
		<td align="center" valign=middle sdval="89" sdnum="1033;">89</td>
		<td align="center" valign=middle sdval="84" sdnum="1033;">84</td>
		<td align="center" valign=middle sdval="94" sdnum="1033;">94</td>
		<td align="center" valign=middle sdval="92" sdnum="1033;">92</td>
		<td align="center" valign=middle sdval="87" sdnum="1033;">87</td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle sdval="36.3" sdnum="1033;">36.3</td>
		<td align="center" valign=middle sdval="48.9" sdnum="1033;">48.9</td>
		<td align="center" valign=middle sdval="2017" sdnum="1033;">2017</td>
		<td align="center" valign=middle>AAAI</td>
	</tr>
	<tr>
		<td height="19" align="center" valign=middle>Bŭsta et al. [9]</td>
		<td align="center" valign=middle>Deep TextSpotter</td>
		<td align="center" valign=middle>First end-to-end trainable detection and recognition system</td>
		<td align="center" valign=middle>Yolo v2</td>
		<td align="center" valign=middle>CTC</td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle sdval="89" sdnum="1033;">89</td>
		<td align="center" valign=middle sdval="86" sdnum="1033;">86</td>
		<td align="center" valign=middle sdval="77" sdnum="1033;">77</td>
		<td align="center" valign=middle sdval="92" sdnum="1033;">92</td>
		<td align="center" valign=middle sdval="89" sdnum="1033;">89</td>
		<td align="center" valign=middle sdval="81" sdnum="1033;">81</td>
		<td align="center" valign=middle sdval="54" sdnum="1033;">54</td>
		<td align="center" valign=middle sdval="51" sdnum="1033;">51</td>
		<td align="center" valign=middle sdval="47" sdnum="1033;">47</td>
		<td align="center" valign=middle sdval="58" sdnum="1033;">58</td>
		<td align="center" valign=middle sdval="53" sdnum="1033;">53</td>
		<td align="center" valign=middle sdval="51" sdnum="1033;">51</td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle sdval="2017" sdnum="1033;">2017</td>
		<td align="center" valign=middle>ICCV</td>
	</tr>
	<tr>
		<td height="19" align="center" valign=middle>Li et al. [10]</td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle>First end-to-end trainable detection and recognition system</td>
		<td align="center" valign=middle>Text Proposal Network</td>
		<td align="center" valign=middle>Attention</td>
		<td align="center" valign=middle sdval="66.18" sdnum="1033;">66.18</td>
		<td align="center" valign=middle sdval="84.91" sdnum="1033;">84.91</td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle sdval="87.7" sdnum="1033;">87.7</td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle sdval="91.08" sdnum="1033;">91.08</td>
		<td align="center" valign=middle sdval="89.8" sdnum="1033;">89.8</td>
		<td align="center" valign=middle sdval="84.6" sdnum="1033;">84.6</td>
		<td align="center" valign=middle sdval="94.2" sdnum="1033;">94.2</td>
		<td align="center" valign=middle sdval="92.4" sdnum="1033;">92.4</td>
		<td align="center" valign=middle sdval="88.2" sdnum="1033;">88.2</td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle sdval="2017" sdnum="1033;">2017</td>
		<td align="center" valign=middle>ICCV</td>
	</tr>
	<tr>
		<td height="19" align="center" valign=middle>Lyu et al. [11]</td>
		<td align="center" valign=middle>Mask TextSpotter</td>
		<td align="center" valign=middle>Precise text detection and recognition are acquired via semantic segmentation</td>
		<td align="center" valign=middle>Fast R-CNN with mask branch</td>
		<td align="center" valign=middle>Character segmentation</td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle sdval="92.2" sdnum="1033;">92.2</td>
		<td align="center" valign=middle sdval="91.1" sdnum="1033;">91.1</td>
		<td align="center" valign=middle sdval="86.5" sdnum="1033;">86.5</td>
		<td align="center" valign=middle sdval="92.5" sdnum="1033;">92.5</td>
		<td align="center" valign=middle sdval="92" sdnum="1033;">92</td>
		<td align="center" valign=middle sdval="88.2" sdnum="1033;">88.2</td>
		<td align="center" valign=middle sdval="79.3" sdnum="1033;">79.3</td>
		<td align="center" valign=middle sdval="73" sdnum="1033;">73</td>
		<td align="center" valign=middle sdval="62.4" sdnum="1033;">62.4</td>
		<td align="center" valign=middle sdval="79.3" sdnum="1033;">79.3</td>
		<td align="center" valign=middle sdval="74.5" sdnum="1033;">74.5</td>
		<td align="center" valign=middle sdval="64.2" sdnum="1033;">64.2</td>
		<td align="center" valign=middle sdval="52.9" sdnum="1033;">52.9</td>
		<td align="center" valign=middle sdval="71.8" sdnum="1033;">71.8</td>
		<td align="center" valign=middle sdval="2018" sdnum="1033;">2018</td>
		<td align="center" valign=middle>ECCV</td>
	</tr>
	<tr>
		<td height="19" align="center" valign=middle>He et al. [12]</td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle>Character attention mechanism: use character spatial information as explicit supervision</td>
		<td align="center" valign=middle>Text-Alignment Layer</td>
		<td align="center" valign=middle>Attention</td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle sdval="91" sdnum="1033;">91</td>
		<td align="center" valign=middle sdval="89" sdnum="1033;">89</td>
		<td align="center" valign=middle sdval="86" sdnum="1033;">86</td>
		<td align="center" valign=middle sdval="93" sdnum="1033;">93</td>
		<td align="center" valign=middle sdval="92" sdnum="1033;">92</td>
		<td align="center" valign=middle sdval="87" sdnum="1033;">87</td>
		<td align="center" valign=middle sdval="82" sdnum="1033;">82</td>
		<td align="center" valign=middle sdval="77" sdnum="1033;">77</td>
		<td align="center" valign=middle sdval="63" sdnum="1033;">63</td>
		<td align="center" valign=middle sdval="85" sdnum="1033;">85</td>
		<td align="center" valign=middle sdval="80" sdnum="1033;">80</td>
		<td align="center" valign=middle sdval="65" sdnum="1033;">65</td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle sdval="2018" sdnum="1033;">2018</td>
		<td align="center" valign=middle>CVPR</td>
	</tr>
	<tr>
		<td height="19" align="center" valign=middle>Liu et al. [13]</td>
		<td align="center" valign=middle>FOTS</td>
		<td align="center" valign=middle>Little computation overhead compared to baseline text detection network (22.6fps)</td>
		<td align="center" valign=middle>EAST with RoIRotate</td>
		<td align="center" valign=middle>CTC</td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle sdval="91.99" sdnum="1033;">91.99</td>
		<td align="center" valign=middle sdval="90.11" sdnum="1033;">90.11</td>
		<td align="center" valign=middle sdval="84.77" sdnum="1033;">84.77</td>
		<td align="center" valign=middle sdval="95.94" sdnum="1033;">95.94</td>
		<td align="center" valign=middle sdval="93.9" sdnum="1033;">93.9</td>
		<td align="center" valign=middle sdval="87.76" sdnum="1033;">87.76</td>
		<td align="center" valign=middle sdval="83.55" sdnum="1033;">83.55</td>
		<td align="center" valign=middle sdval="79.11" sdnum="1033;">79.11</td>
		<td align="center" valign=middle sdval="65.33" sdnum="1033;">65.33</td>
		<td align="center" valign=middle sdval="87.01" sdnum="1033;">87.01</td>
		<td align="center" valign=middle sdval="82.39" sdnum="1033;">82.39</td>
		<td align="center" valign=middle sdval="67.97" sdnum="1033;">67.97</td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle sdval="2018" sdnum="1033;">2018</td>
		<td align="center" valign=middle>CVPR</td>
	</tr>
	<tr>
		<td height="19" align="center" valign=middle>Liao et al. [14]</td>
		<td align="center" valign=middle>TextBoxes++</td>
		<td align="center" valign=middle>Journal version of TextBoxes (oriented scene text support)</td>
		<td align="center" valign=middle>SSD-based framework</td>
		<td align="center" valign=middle>CRNN</td>
		<td align="center" valign=middle sdval="64" sdnum="1033;">64</td>
		<td align="center" valign=middle sdval="84" sdnum="1033;">84</td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle sdval="93" sdnum="1033;">93</td>
		<td align="center" valign=middle sdval="92" sdnum="1033;">92</td>
		<td align="center" valign=middle sdval="85" sdnum="1033;">85</td>
		<td align="center" valign=middle sdval="96" sdnum="1033;">96</td>
		<td align="center" valign=middle sdval="95" sdnum="1033;">95</td>
		<td align="center" valign=middle sdval="87" sdnum="1033;">87</td>
		<td align="center" valign=middle sdval="73.3" sdnum="1033;">73.3</td>
		<td align="center" valign=middle sdval="65.9" sdnum="1033;">65.9</td>
		<td align="center" valign=middle sdval="51.9" sdnum="1033;">51.9</td>
		<td align="center" valign=middle sdval="76.5" sdnum="1033;">76.5</td>
		<td align="center" valign=middle sdval="69" sdnum="1033;">69</td>
		<td align="center" valign=middle sdval="54.4" sdnum="1033;">54.4</td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle sdval="2018" sdnum="1033;">2018</td>
		<td align="center" valign=middle>TIP</td>
	</tr>
	<tr>
</table>

## Reference

[1] Wang K, Babenko B, Belongie S. End-to-end scene text recognition[C]//2011 International Conference on Computer Vision. IEEE, 2011: 1457-1464. [paper](http://www.iapr-tc11.org/dataset/SVT/wang_iccv2011.pdf)

[2] Wang T, Wu D J, Coates A, et al. End-to-end text recognition with convolutional neural networks[C]//Proceedings of the 21st International Conference on Pattern Recognition (ICPR2012). IEEE, 2012: 3304-3308. [paper](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.664.6212&rep=rep1&type=pdf)

[3] Jaderberg M, Vedaldi A, Zisserman A. Deep features for text spotting[C]//European conference on computer vision. Springer, Cham, 2014: 512-528. [paper](http://www.robots.ox.ac.uk/~vedaldi/assets/pubs/jaderberg14deep.pdf)

[4] Alsharif O, Pineau J. End-to-End Text Recognition with Hybrid HMM Maxout Models[C]//2014  ICLR. [paper](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.740.1108&rep=rep1&type=pdf)

[5] Yao C, Bai X, Liu W. A unified framework for multioriented text detection and recognition[J]. IEEE Transactions on Image Processing, 2014, 23(11): 4737-4749. [paper](http://www.vlrlab.net/admin/uploads/avatars/A_Unified_Framework_for_Multi-Oriented_Text_Detection_and_Recognition.pdf)

[6] Neumann L, Matas J. Real-time lexicon-free scene text localization and recognition[J]. IEEE transactions on pattern analysis and machine intelligence, 2015, 38(9): 1872-1885. [paper](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.717.4947&rep=rep1&type=pdf)

[7] Jaderberg M, Simonyan K, Vedaldi A, et al. Reading text in the wild with convolutional neural networks[J]. International Journal of Computer Vision, 2016, 116(1): 1-20. [paper](http://www.academia.edu/download/43938680/jaderberg16.pdf)

[8] Liao M, Shi B, Bai X, et al. Textboxes: A fast text detector with a single deep neural network[C]//Thirty-First AAAI Conference on Artificial Intelligence. 2017. [paper](https://www.aaai.org/ocs/index.php/AAAI/AAAI17/paper/viewPDFInterstitial/14202/14295) [code](https://github.com/MhLiao/TextBoxes)

[9] Busta M, Neumann L, Matas J. Deep textspotter: An end-to-end trainable scene text localization and recognition framework[C]//Proceedings of the IEEE International Conference on Computer Vision. 2017: 2204-2212. [paper](http://openaccess.thecvf.com/content_ICCV_2017/papers/Busta_Deep_TextSpotter_An_ICCV_2017_paper.pdf)
  
[10] Li H, Wang P,  Shen C. Towards end-to-end text spotting with convolutional recurrent neural networks[C]//Proceedings of the IEEE International Conference on Computer Vision. 2017: 5238-5246. [paper](http://openaccess.thecvf.com/content_ICCV_2017/papers/Li_Towards_End-To-End_Text_ICCV_2017_paper.pdf)
  
[11] Lyu P, Liao M, Yao C, et al. Mask textspotter: An end-to-end trainable neural network for spotting text with arbitrary shapes[C]//Proceedings of the European Conference on Computer Vision (ECCV). 2018: 67-83. [paper](http://openaccess.thecvf.com/content_ECCV_2018/papers/Pengyuan_Lyu_Mask_TextSpotter_An_ECCV_2018_paper.pdf) [code](https://github.com/lvpengyuan/masktextspotter.caffe2)

[12] He T, Tian Z, Huang W, et al. An end-to-end textspotter with explicit alignment and attention[C]//Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition. 2018: 5020-5029. [paper](http://openaccess.thecvf.com/content_cvpr_2018/papers/He_An_End-to-End_TextSpotter_CVPR_2018_paper.pdf) [code](https://github.com/tonghe90/textspotter)

[13] Liu X, Liang D, Yan S, et al. FOTS: Fast oriented text spotting with a unified network[C]//Proceedings of the IEEE conference on computer vision and pattern recognition. 2018: 5676-5685. [paper](http://openaccess.thecvf.com/content_cvpr_2018/papers/Liu_FOTS_Fast_Oriented_CVPR_2018_paper.pdf) [code](https://github.com/jiangxiluning/FOTS.PyTorch)

[14] Liao M, Shi B, Bai X. Textboxes++: A single-shot oriented scene text detector[J]. IEEE transactions on image processing, 2018, 27(8): 3676-3690. [paper](https://ieeexplore.ieee.org/abstract/document/8334248) [code](https://github.com/MhLiao/TextBoxes_plusplus)
