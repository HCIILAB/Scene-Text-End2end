# End-to-End Scene Text Detection and Recognition System Resources

<p align='right'>Author: Canjie Luo, Chongyu Liu</p>

<!-- MarkdownTOC -->

- [1.Datasets](#1-datasets)
    - [1.1 Introduction](#1-1intro)
    - [1.2 Comparison of Datasets](#1-2-dataset)
- [2. Summary of End-to-end Scene Text Detection and Recognition Methods](#2-summary-of-end2end-results)
    - [2.1 Comparison of methods](#21-comparison-of-methods)
    - [2.2 End-to-end scene text detection and recognition results](#22-end2end-result)
- [3. Survey](#3-field-survey)
- [4. OCR Service](#4-ocr-service)
- [5. References and codes](#5-references)

<!-- /MarkdownTOC -->

------

<a id="1-datasets"></a>
## 1. Datasets

<a id="1-1intro"></a>
### 1.1 Introduction
- SVT [15]：
  * **Introduction:** There are 100 training images and 250 testing images downloaded from Google Street View of road-side scenes. The labelled text can be very challenging with a wide variety of fonts, orientations, and lighting conditions. A lexicon containing 50 words (SVT-50) is also provided for each image.
  * **Link:** [SVT-download](http://vision.ucsd.edu/~kai/grocr/)

- ICDAR 2003(IC03) [16]：
  * **Introduction:** The dataset contains a varied array of photos of the world that contain scene text. There are 251 testing images with 50 word lexicons (IC03-50) and a lexicon of all test groundtruth words (IC03-Full).
  * **Link:** [IC03-download](http://www.iapr-tc11.org/mediawiki/index.php?title=ICDAR_2003_Robust_Reading_Competitions)

- ICDAR 2011(IC11) [17] :
  * **Introduction:** The dataset is an extension to the dataset used for the text locating competitions of ICDAR 2003.It includes 485 natural images in total.
  * **Link:** [IC11-download](http://www.cvc.uab.es/icdar2011competition/?com=downloads)   

- ICDAR 2013(IC13) [18]：
  * **Introduction:** The dataset consists of 229 training images and 233 testing images. Most text are horizontal. Three speciﬁc lexicons are provided, named as “Strong(S)”, “Weak(W)” and “Generic(G)”. “Strong(S)” lexicon provides 100 words per-image including all words that appear in the image. “Weak(W)” lexicon includes all words that appear in the entire test set. And “Generic(G)” lexicon is a 90k word vocabulary.
  * **Link:** [IC13-download](http://dagdata.cvc.uab.es/icdar2013competition/?ch=2&com=downloads)

- ICDAR 2015(IC15) [19]：
  - **Introduction:** The dataset includes 1000 training images and 500 testing images captured by Google glasses. The text in the scene is in arbitrary orientations. Similar to ICDAR 2013, it also provides “Strong(S)”, “Weak(W)” and “Generic(G)” lexicons.
  - **Link:** [IC15-download](http://rrc.cvc.uab.es/?ch=4&com=downloads)

- Total-Text [20]：
  - **Introduction:** Except for the horizontal text and oriented text, Total-Text also consists of a lot of curved text. Total-Text contains 1255 training images and 300 test images. All images are annotated with polygons and transcriptions in word-level. A “Full” lexicon contains all words in test set is provided.
  - **Link:** [Total-Text-download](https://github.com/cs-chan/Total-Text-Dataset)

<a id="1-2-dataset"></a>
### 1.2 Comparison of Datasets

<table cellspacing="0" border="0">
	<colgroup span="18" width="85"></colgroup>
	<tr>
		<td colspan=18 height="20" align="center" valign=middle><b>Comparison of Datasets</b></td>
		</tr>
	<tr>
		<td rowspan=2 height="39" align="center" valign=top><b>Datasets</b></td>
		<td rowspan=2 align="center" valign=top><b>Language</b></td>
		<td colspan=3 align="center"><b>Image</b></td>
		<td colspan=3 align="center"><b>Text instance </b></td>
		<td colspan=3 align="center"><b>Text Shape</b></td>
		<td colspan=3 align="center"><b>Annotation level</b></td>
		<td colspan=4 align="center"><b><font face="Liberation Sans">Lexicon</font></b></td>
		</tr>
	<tr>
		<td align="center"><b>Total</b></td>
		<td align="center"><b>Train</b></td>
		<td align="center"><b>Test</b></td>
		<td align="center"><b>Total</b></td>
		<td align="center"><b>Train</b></td>
		<td align="center"><b>Test</b></td>
		<td align="center"><b>Horizontal</b></td>
		<td align="center"><b>Arbitrary-Quadrilateral</b></td>
		<td align="center"><b>Multi-oriented</b></td>
		<td align="center"><b>Char</b></td>
		<td align="center"><b>Word</b></td>
		<td align="center"><b>Text-Line</b></td>
		<td align="center" sdval="50" sdnum="2052;"><b><font face="Liberation Sans">50</font></b></td>
		<td align="center"><b><font face="Liberation Sans">1k</font></b></td>
		<td align="center"><b><font face="Liberation Sans">Full</font></b></td>
		<td align="center"><b><font face="Liberation Sans">None</font></b></td>
	</tr>
	<tr>
		<td height="20" align="center"><b>IC03</b></td>
		<td align="center"><font face="Liberation Sans">English</font></td>
		<td align="center" sdval="509" sdnum="2052;"><font face="Liberation Sans">509</font></td>
		<td align="center" sdval="258" sdnum="2052;"><font face="Liberation Sans">258</font></td>
		<td align="center" sdval="251" sdnum="2052;"><font face="Liberation Sans">251</font></td>
		<td align="center" sdval="2266" sdnum="2052;"><font face="Liberation Sans">2266</font></td>
		<td align="center" sdval="1110" sdnum="2052;"><font face="Liberation Sans">1110</font></td>
		<td align="center" sdval="1156" sdnum="2052;"><font face="Liberation Sans">1156</font></td>
		<td align="center">✓</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center">✓</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center">✓</td>
		<td align="center">✓</td>
		<td align="center">✓</td>
		<td align="center" sdnum="2052;0;@">✕</td>
	</tr>
	<tr>
		<td height="20" align="center"><b>IC11</b></td>
		<td align="center">English</td>
		<td align="center" sdval="484" sdnum="2052;"><font face="Liberation Sans">484</font></td>
		<td align="center" sdval="229" sdnum="2052;"><font face="Liberation Sans">229</font></td>
		<td align="center" sdval="255" sdnum="2052;"><font face="Liberation Sans">255</font></td>
		<td align="center" sdval="1564" sdnum="2052;"><font face="Liberation Sans">1564</font></td>
		<td align="center">～</td>
		<td align="center">～</td>
		<td align="center">✓</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center">✓</td>
		<td align="center">✓</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center">✓</td>
	</tr>
	<tr>
		<td height="20" align="center"><b>IC13</b></td>
		<td align="center">English</td>
		<td align="center" sdval="462" sdnum="2052;"><font face="Liberation Sans">462</font></td>
		<td align="center" sdval="229" sdnum="2052;"><font face="Liberation Sans">229</font></td>
		<td align="center" sdval="233" sdnum="2052;"><font face="Liberation Sans">233</font></td>
		<td align="center" sdval="1944" sdnum="2052;"><font face="Liberation Sans">1944</font></td>
		<td align="center" sdval="849" sdnum="2052;"><font face="Liberation Sans">849</font></td>
		<td align="center" sdval="1095" sdnum="2052;"><font face="Liberation Sans">1095</font></td>
		<td align="center">✓</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center">✓</td>
		<td align="center">✓</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center">✓</td>
	</tr>
	<tr>
		<td height="20" align="center"><b>SVT</b></td>
		<td align="center">English</td>
		<td align="center" sdval="350" sdnum="2052;"><font face="Liberation Sans">350</font></td>
		<td align="center" sdval="100" sdnum="2052;"><font face="Liberation Sans">100</font></td>
		<td align="center" sdval="250" sdnum="2052;"><font face="Liberation Sans">250</font></td>
		<td align="center" sdval="725" sdnum="2052;"><font face="Liberation Sans">725</font></td>
		<td align="center" sdval="211" sdnum="2052;"><font face="Liberation Sans">211</font></td>
		<td align="center" sdval="514" sdnum="2052;"><font face="Liberation Sans">514</font></td>
		<td align="center">✓</td>
		<td align="center">✓</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center">✓</td>
		<td align="center">✓</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center">✓</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center" sdnum="2052;0;@">✕</td>
	</tr>
	<tr>
		<td height="20" align="center"><b>SVT-P</b></td>
		<td align="center">English</td>
		<td align="center" sdval="238" sdnum="2052;"><font face="Liberation Sans">238</font></td>
		<td align="center">～</td>
		<td align="center">～</td>
		<td align="center" sdval="639" sdnum="2052;"><font face="Liberation Sans">639</font></td>
		<td align="center">～</td>
		<td align="center">～</td>
		<td align="center">✓</td>
		<td align="center">✓</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center">✓</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center">✓</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center">✓</td>
		<td align="center" sdnum="2052;0;@">✕</td>
	</tr>
	<tr>
		<td height="20" align="center"><b>IC15</b></td>
		<td align="center">English</td>
		<td align="center" sdval="1500" sdnum="2052;"><font face="Liberation Sans">1500</font></td>
		<td align="center" sdval="1000" sdnum="2052;"><font face="Liberation Sans">1000</font></td>
		<td align="center" sdval="500" sdnum="2052;"><font face="Liberation Sans">500</font></td>
		<td align="center" sdval="17548" sdnum="2052;"><font face="Liberation Sans">17548</font></td>
		<td align="center" sdval="122318" sdnum="2052;"><font face="Liberation Sans">122318</font></td>
		<td align="center" sdval="5230" sdnum="2052;"><font face="Liberation Sans">5230</font></td>
		<td align="center">✓</td>
		<td align="center">✓</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center">✓</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center">✓</td>
	</tr>
	<tr>
		<td height="20" align="center"><b>Total-Text</b></td>
		<td align="center"><font face="Liberation Sans">English</font></td>
		<td align="center" sdval="1525" sdnum="2052;"><font face="Liberation Sans">1525</font></td>
		<td align="center" sdval="1225" sdnum="2052;"><font face="Liberation Sans">1225</font></td>
		<td align="center" sdval="300" sdnum="2052;"><font face="Liberation Sans">300</font></td>
		<td align="center" sdval="9330" sdnum="2052;"><font face="Liberation Sans">9330</font></td>
		<td align="center">～</td>
		<td align="center">～</td>
		<td align="center">✓</td>
		<td align="center">✓</td>
		<td align="center">✓</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center">✓</td>
		<td align="center">✓</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center">✓</td>
	</tr>
</table>


<a id="2-summary-of-end2end-results"></a>
## 2. Summary of End-to-end Scene Text Detection and Recognition Methods



<a id="21-comparison-of-methods"></a>
### 2.1 Comparison of methods

<table cellspacing="0" border="0">
	<colgroup width="152"></colgroup>
	<colgroup width="131"></colgroup>
	<colgroup width="85"></colgroup>
	<colgroup width="252"></colgroup>
	<colgroup width="250"></colgroup>
	<colgroup span="2" width="85"></colgroup>
	<colgroup width="646"></colgroup>
	<tr>
		<td height="20" align="left"><b><font face="Arial">Method&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</font></b></td>
		<td align="left"><b><font face="Arial">Model&nbsp;&nbsp;&nbsp;&nbsp;</font></b></td>
		<td align="left"><b><font face="Arial">Code</font></b></td>
		<td align="left"><b><font face="Arial">Detection&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</font></b></td>
		<td align="left"><b><font face="Arial">Recognition&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</font></b></td>
		<td align="left"><b><font face="Arial">Source </font></b></td>
		<td align="left"><b><font face="Arial">Time</font></b></td>
		<td align="left"><b><font face="Arial">Highlight&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</font></b></td>
	</tr>
	<tr>
		<td height="20" align="left" valign=middle><font face="Times New Roman">Wang et al. [1]</font></td>
		<td align="left" valign=middle><br></td>
		<td align="left" sdnum="2052;0;@">✕</td>
		<td align="left" valign=middle><font face="Times New Roman">Sliding windows and Random Ferns</font></td>
		<td align="left" valign=middle><font face="Times New Roman">Pictorial Structures</font></td>
		<td align="left" valign=middle><font face="Times New Roman">ICCV</font></td>
		<td align="left" valign=middle sdval="2011" sdnum="2052;"><font face="Times New Roman">2011</font></td>
		<td align="left" valign=middle><font face="Times New Roman">Word Re-scoring for NMS</font></td>
	</tr>
	<tr>
		<td height="20" align="left" valign=middle><font face="Times New Roman">Wang et al. [2]</font></td>
		<td align="left" valign=middle><br></td>
		<td align="left" sdnum="2052;0;@">✕</td>
		<td align="left" valign=middle><font face="Times New Roman">CNN-based</font></td>
		<td align="left" valign=middle><font face="Times New Roman">Sliding windows for classification</font></td>
		<td align="left" valign=middle><font face="Times New Roman">ICPR</font></td>
		<td align="left" valign=middle sdval="2012" sdnum="2052;"><font face="Times New Roman">2012</font></td>
		<td align="left" valign=middle><font face="Times New Roman">CNN architecture</font></td>
	</tr>
	<tr>
		<td height="20" align="left" valign=middle><font face="Times New Roman">Jaderberg et al. [3]</font></td>
		<td align="left" valign=middle><br></td>
		<td align="left" sdnum="2052;0;@">✕</td>
		<td align="left" valign=middle><font face="Times New Roman">CNN-based and saliency maps</font></td>
		<td align="left" valign=middle><font face="Times New Roman">CNN classifier</font></td>
		<td align="left" valign=middle><font face="Times New Roman">ECCV</font></td>
		<td align="left" valign=middle sdval="2014" sdnum="2052;"><font face="Times New Roman">2014</font></td>
		<td align="left" valign=middle><font face="Times New Roman">Data mining and annotation</font></td>
	</tr>
	<tr>
		<td height="20" align="left" valign=middle><font face="Times New Roman">Alsharif et al. [4]</font></td>
		<td align="left" valign=middle><br></td>
		<td align="left" sdnum="2052;0;@">✕</td>
		<td align="left" valign=middle><font face="Times New Roman">CNN and hybrid HMM maxout models</font></td>
		<td align="left" valign=middle><font face="Times New Roman">Segmentation-based</font></td>
		<td align="left" valign=middle><font face="Times New Roman">ICLR</font></td>
		<td align="left" valign=middle sdval="2014" sdnum="2052;"><font face="Times New Roman">2014</font></td>
		<td align="left" valign=middle><font face="Times New Roman">Hybrid HMM maxout models</font></td>
	</tr>
	<tr>
		<td height="20" align="left" valign=middle><font face="Times New Roman">Yao et al. [5]</font></td>
		<td align="left" valign=middle><br></td>
		<td align="left" sdnum="2052;0;@">✕</td>
		<td align="left" valign=middle><font face="Times New Roman">Random Forest</font></td>
		<td align="left" valign=middle><font face="Times New Roman">Component Linking and Word Partition</font></td>
		<td align="left" valign=middle><font face="Times New Roman">TIP</font></td>
		<td align="left" valign=middle sdval="2014" sdnum="2052;"><font face="Times New Roman">2014</font></td>
		<td align="left" valign=middle><font face="Times New Roman">(1) Detection and recognition features sharing. (2) Oriented-text. (3) A new dictionary search method</font></td>
	</tr>
	<tr>
		<td height="20" align="left" valign=middle><font face="Times New Roman">Neumann et al. [6]</font></td>
		<td align="left" valign=middle><br></td>
		<td align="left" sdnum="2052;0;@">✕</td>
		<td align="left" valign=middle><font face="Times New Roman">Extremal Regions</font></td>
		<td align="left" valign=middle><font face="Times New Roman">Clustering algorithm to group characters</font></td>
		<td align="left" valign=middle><font face="Times New Roman">TPAMI</font></td>
		<td align="left" valign=middle sdval="2015" sdnum="2052;"><font face="Times New Roman">2015</font></td>
		<td align="left" valign=middle><font face="Times New Roman">Real-time performance(1.6s/image)</font></td>
	</tr>
	<tr>
		<td height="20" align="left" valign=middle><font face="Times New Roman">Jaderberg et al. [7]</font></td>
		<td align="left" valign=middle><br></td>
		<td align="left" sdnum="2052;0;@">✕</td>
		<td align="left" valign=middle><font face="Times New Roman">Region proposal mechanism</font></td>
		<td align="left" valign=middle><font face="Times New Roman">Word-level classification</font></td>
		<td align="left" valign=middle><font face="Times New Roman">IJCV</font></td>
		<td align="left" valign=middle sdval="2016" sdnum="2052;"><font face="Times New Roman">2016</font></td>
		<td align="left" valign=middle><font face="Times New Roman">Trained only on data produced by a synthetic text generation engine, requiring no human labelled data</font></td>
	</tr>
	<tr>
		<td height="20" align="left" valign=middle><font face="Times New Roman">Liao et al. [8]</font></td>
		<td align="left" valign=middle><font face="Times New Roman">TextBoxes</font></td>
		<td align="left" sdnum="2052;0;@">✓</td>
		<td align="left" valign=middle><font face="Times New Roman">SSD-based framework</font></td>
		<td align="left" valign=middle><font face="Times New Roman">CRNN</font></td>
		<td align="left" valign=middle><font face="Times New Roman">AAAI</font></td>
		<td align="left" valign=middle sdval="2017" sdnum="2052;"><font face="Times New Roman">2017</font></td>
		<td align="left" valign=middle><font face="Times New Roman">An end-to-end trainable fast scene text detector</font></td>
	</tr>
	<tr>
		<td height="20" align="left" valign=middle><font face="Times New Roman">Bŭsta et al. [9]</font></td>
		<td align="left" valign=middle><font face="Times New Roman">Deep TextSpotter</font></td>
		<td align="left" sdnum="2052;0;@">✕</td>
		<td align="left" valign=middle><font face="Times New Roman">Yolo v2</font></td>
		<td align="left" valign=middle><font face="Times New Roman">CTC</font></td>
		<td align="left" valign=middle><font face="Times New Roman">ICCV</font></td>
		<td align="left" valign=middle sdval="2017" sdnum="2052;"><font face="Times New Roman">2017</font></td>
		<td align="left" valign=middle><font face="Times New Roman">Yolov2 + RPN, RNN + CTC. It is the first end-to-end trainable detection and recognition system with high speed.</font></td>
	</tr>
	<tr>
		<td height="20" align="left" valign=middle><font face="Times New Roman">Li et al. [10]</font></td>
		<td align="left" valign=middle><br></td>
		<td align="left" sdnum="2052;0;@">✕</td>
		<td align="left" valign=middle><font face="Times New Roman">Text Proposal Network</font></td>
		<td align="left" valign=middle><font face="Times New Roman">Attention</font></td>
		<td align="left" valign=middle><font face="Times New Roman">ICCV</font></td>
		<td align="left" valign=middle sdval="2017" sdnum="2052;"><font face="Times New Roman">2017</font></td>
		<td align="left" valign=middle><font face="Times New Roman">TPN + RNN encoder + attention-based RNN</font></td>
	</tr>
	<tr>
		<td height="20" align="left" valign=middle><font face="Times New Roman">Sun et al. [22]</font></td>
		<td align="left" valign=middle><font face="Times New Roman">TextNet </font></td>
		<td align="left" sdnum="2052;0;@">✕</td>
		<td align="left" valign=middle><font face="Times New Roman">Scale-aware attention backbone and Perspective RoI Transform </font></td>
		<td align="left" valign=middle><font face="Times New Roman">Attention</font></td>
		<td align="left" valign=middle><font face="Times New Roman">ACCV</font></td>
		<td align="left" valign=middle sdval="2018" sdnum="2052;"><font face="Times New Roman">2018</font></td>
		<td align="left" valign=middle><font face="Times New Roman">Perspective RoI Transform for Irregular text recognition</font></td>
	</tr>
	<tr>
		<td height="20" align="left" valign=middle><font face="Times New Roman">Lyu et al. [11]</font></td>
		<td align="left" valign=middle><font face="Times New Roman">Mask TextSpotter</font></td>
		<td align="left" sdnum="2052;0;@">✓</td>
		<td align="left" valign=middle><font face="Times New Roman">Fast R-CNN with mask branch</font></td>
		<td align="left" valign=middle><font face="Times New Roman">Character segmentation</font></td>
		<td align="left" valign=middle><font face="Times New Roman">ECCV</font></td>
		<td align="left" valign=middle sdval="2018" sdnum="2052;"><font face="Times New Roman">2018</font></td>
		<td align="left" valign=middle><font face="Times New Roman">Precise text detection and recognition are acquired via semantic segmentation</font></td>
	</tr>
	<tr>
		<td height="20" align="left" valign=middle><font face="Times New Roman">He et al. [12]</font></td>
		<td align="left" valign=middle><br></td>
		<td align="left" sdnum="2052;0;@">✓</td>
		<td align="left" valign=middle><font face="Times New Roman">Text-Alignment Layer</font></td>
		<td align="left" valign=middle><font face="Times New Roman">Attention</font></td>
		<td align="left" valign=middle><font face="Times New Roman">CVPR</font></td>
		<td align="left" valign=middle sdval="2018" sdnum="2052;"><font face="Times New Roman">2018</font></td>
		<td align="left" valign=middle><font face="Times New Roman">Character attention mechanism: use character spatial information as explicit supervision</font></td>
	</tr>
	<tr>
		<td height="20" align="left" valign=middle><font face="Times New Roman">Liu et al. [13]</font></td>
		<td align="left" valign=middle><font face="Times New Roman">FOTS</font></td>
		<td align="left" sdnum="2052;0;@">✓</td>
		<td align="left" valign=middle><font face="Times New Roman">EAST with RoIRotate</font></td>
		<td align="left" valign=middle><font face="Times New Roman">CTC</font></td>
		<td align="left" valign=middle><font face="Times New Roman">CVPR</font></td>
		<td align="left" valign=middle sdval="2018" sdnum="2052;"><font face="Times New Roman">2018</font></td>
		<td align="left" valign=middle><font face="Times New Roman">Little computation overhead compared to baseline text detection network (22.6fps)</font></td>
	</tr>
	<tr>
		<td height="20" align="left" valign=middle><font face="Times New Roman">Liao et al. [14]</font></td>
		<td align="left" valign=middle><font face="Times New Roman">TextBoxes++</font></td>
		<td align="left" sdnum="2052;0;@">✓</td>
		<td align="left" valign=middle><font face="Times New Roman">SSD-based framework</font></td>
		<td align="left" valign=middle><font face="Times New Roman">CRNN</font></td>
		<td align="left" valign=middle><font face="Times New Roman">TIP</font></td>
		<td align="left" valign=middle sdval="2018" sdnum="2052;"><font face="Times New Roman">2018</font></td>
		<td align="left" valign=middle><font face="Times New Roman">Journal version of TextBoxes (multi-oriented scene text support)</font></td>
	</tr>
	<tr>
		<td height="20" align="left"><font face="Times New Roman">Liao et al. [15]</font></td>
		<td align="left"><font face="Times New Roman">Mask TextSpotter</font></td>
		<td align="left" sdnum="2052;0;@">✓</td>
		<td align="left"><font face="Times New Roman">Mask R-CNN</font></td>
		<td align="left"><font face="Times New Roman">Character segmentation + Spatial Attention Module</font></td>
		<td align="left"><font face="Times New Roman">TPAMI</font></td>
		<td align="left" sdval="2019" sdnum="2052;"><font face="Times New Roman">2019</font></td>
		<td align="left"><font face="Times New Roman">Journal version of Mask TextSpotter(proposes Spatial Attention Module)</font></td>
	</tr>
	<tr>
		<td height="20" align="left" valign=middle><font face="Times New Roman">Xing et al. [23]</font></td>
		<td align="left"><font face="Times New Roman">CharNet</font></td>
		<td align="left" sdnum="2052;0;@">✓</td>
		<td align="left"><font face="Times New Roman">A character branch and a detection branch </font></td>
		<td align="left"><font face="Times New Roman">Character level</font></td>
		<td align="left"><font face="Times New Roman">ICCV</font></td>
		<td align="left" sdval="2019" sdnum="2052;"><font face="Times New Roman">2019</font></td>
		<td align="left"><font face="Times New Roman">Utilizing a character as basic element to overcome the main difficulty of joint optimization of  text detection and RNN-based recognition</font></td>
	</tr>
	<tr>
		<td height="20" align="left"><font face="Times New Roman">Feng et al. [24]</font></td>
		<td align="left"><font face="Times New Roman">TextDragon </font></td>
		<td align="left" sdnum="2052;0;@">✕</td>
		<td align="left"><font face="Times New Roman">Local box regression, center line segmentation and RoI Sliding</font></td>
		<td align="left" valign=middle><font face="Times New Roman">CTC</font></td>
		<td align="left"><font face="Times New Roman">ICCV</font></td>
		<td align="left" sdval="2019" sdnum="2052;"><font face="Times New Roman">2019</font></td>
		<td align="left"><font face="Times New Roman">A new differentiable operator named RoISlide connect arbitrary shaped text detection and recognition</font></td>
	</tr>
	<tr>
		<td height="20" align="left"><font face="Times New Roman">Qin et al. [25]</font></td>
		<td align="left"><br></td>
		<td align="left" sdnum="2052;0;@">✕</td>
		<td align="left"><font face="Times New Roman">Mask R-CNN with RoI masking</font></td>
		<td align="left" valign=middle><font face="Times New Roman">Attention</font></td>
		<td align="left"><font face="Times New Roman">ICCV</font></td>
		<td align="left" sdval="2019" sdnum="2052;"><font face="Times New Roman">2019</font></td>
		<td align="left"><font face="Times New Roman">A simple yet effective RoI masking step to extract useful irregularly shaped text instance features</font></td>
	</tr>
	<tr>
		<td height="20" align="left"><font face="Times New Roman">Qiao et al. [26]</font></td>
		<td align="left"><font face="Times New Roman">Text Perceptron </font></td>
		<td align="left" sdnum="2052;0;@">✕</td>
		<td align="left"><font face="Times New Roman">Mask R-CNN with Order-aware Semantic Segmentation and Boundary Regressions</font></td>
		<td align="left" valign=middle><font face="Times New Roman">Attention</font></td>
		<td align="left"><font face="Times New Roman">AAAI</font></td>
		<td align="left" sdval="2020" sdnum="2052;"><font face="Times New Roman">2020</font></td>
		<td align="left"><font face="Times New Roman">A novel Shape Transform Module to transform the feature regions into regular morphologies</font></td>
	</tr>
	<tr>
		<td height="20" align="left"><font face="Times New Roman">Wang et al. [27]</font></td>
		<td align="left"><br></td>
		<td align="left" sdnum="2052;0;@">✕</td>
		<td align="left"><font face="Times New Roman">Oriented Rectangular Box Detector and Boundary Point Detector</font></td>
		<td align="left" valign=middle><font face="Times New Roman">Attention</font></td>
		<td align="left"><font face="Times New Roman">AAAI</font></td>
		<td align="left" sdval="2020" sdnum="2052;"><font face="Times New Roman">2020</font></td>
		<td align="left"><font face="Times New Roman">A set of points on the boundary of each text instance represents arbitrary shapes</font></td>
	</tr>
	<tr>
		<td height="20" align="left"><font face="Times New Roman">Liu et al. [28]</font></td>
		<td align="left"><font face="Times New Roman">ABCNet</font></td>
		<td align="left" sdnum="2052;0;@">✓</td>
		<td align="left"><font face="Times New Roman">Bezier Curve Detection and BezierAlign</font></td>
		<td align="left"><font face="Times New Roman">CTC</font></td>
		<td align="left"><font face="Times New Roman">CVPR</font></td>
		<td align="left" sdval="2020" sdnum="2052;"><font face="Times New Roman">2020</font></td>
		<td align="left"><font face="Times New Roman">10 times faster than re-cent state-of-the-art methods with a competitive scene text spotting accuracy</font></td>
	</tr>
</table>



<a id="22-end2end-result"></a>
### 2.2 End-to-end scene text detection and recognition results

<table cellspacing="0" border="0">
	<colgroup width="193"></colgroup>
	<colgroup width="169"></colgroup>
	<colgroup span="22" width="85"></colgroup>
	<tr>
		<td rowspan=3 height="59" align="center" valign=middle><b><font face="Arial">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Method&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</font></b></td>
		<td rowspan=3 align="center" valign=middle><b><font face="Arial">Model</font></b></td>
		<td rowspan=3 align="center" valign=middle><b><font face="Arial">Source </font></b></td>
		<td rowspan=3 align="center" valign=middle><b><font face="Arial">Time</font></b></td>
		<td rowspan=3 align="center" valign=middle><b><font face="Arial">SVT</font></b></td>
		<td rowspan=3 align="center" valign=middle><b><font face="Arial">SVT-50</font></b></td>
		<td colspan=3 rowspan=2 align="center" valign=middle><b><font face="Arial">IC03</font></b></td>
		<td rowspan=3 align="center" valign=middle><b><font face="Arial">IC11</font></b></td>
		<td colspan=6 align="center" valign=middle><b><font face="Arial">IC13</font></b></td>
		<td colspan=6 align="center" valign=middle><b><font face="Arial">IC15</font></b></td>
		<td colspan=2 align="center" valign=middle><b><font face="Arial">Total-text</font></b></td>
		</tr>
	<tr>
		<td colspan=3 align="center" valign=middle><font face="Times New Roman">End-to-end</font></td>
		<td colspan=3 align="center" valign=middle><font face="Times New Roman">Spotting</font></td>
		<td colspan=3 align="center" valign=middle><font face="Times New Roman">End-to-end</font></td>
		<td colspan=3 align="center" valign=middle><font face="Times New Roman">Spotting</font></td>
		<td rowspan=2 align="center" valign=middle><font face="Times New Roman">None</font></td>
		<td rowspan=2 align="center" valign=middle><font face="Times New Roman">Full</font></td>
		<td rowspan=2 align="center" valign=middle><font face="Times New Roman">None</font></td>
		<td rowspan=2 align="center" valign=middle><font face="Times New Roman">Full</font></td>
		</tr>
	<tr>
		<td align="center" valign=middle sdval="50" sdnum="2052;"><font face="Times New Roman">50</font></td>
		<td align="center" valign=middle><font face="Times New Roman">Full</font></td>
		<td align="center" valign=middle><font face="Times New Roman">None</font></td>
		<td align="center" valign=middle><font face="Times New Roman">S</font></td>
		<td align="center" valign=middle><font face="Times New Roman">W </font></td>
		<td align="center" valign=middle><font face="Times New Roman">G</font></td>
		<td align="center" valign=middle><font face="Times New Roman">S</font></td>
		<td align="center" valign=middle><font face="Times New Roman">W </font></td>
		<td align="center" valign=middle><font face="Times New Roman">G</font></td>
		<td align="center" valign=middle><font face="Times New Roman">S</font></td>
		<td align="center" valign=middle><font face="Times New Roman">W </font></td>
		<td align="center" valign=middle><font face="Times New Roman">G</font></td>
		<td align="center" valign=middle><font face="Times New Roman">S</font></td>
		<td align="center" valign=middle><font face="Times New Roman">W </font></td>
		<td align="center" valign=middle><font face="Times New Roman">G</font></td>
		</tr>
	<tr>
		<td height="20" align="center" valign=middle><font face="Times New Roman">Wang et al. [1]</font></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><font face="Times New Roman">ICCV</font></td>
		<td align="center" valign=middle sdval="2011" sdnum="2052;"><font face="Times New Roman">2011</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" valign=middle sdval="51" sdnum="2052;"><font face="Times New Roman">51</font></td>
		<td align="center" valign=middle><br></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
	</tr>
	<tr>
		<td height="20" align="center" valign=middle><font face="Times New Roman">Wang et al. [2]</font></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><font face="Times New Roman">ICPR</font></td>
		<td align="center" valign=middle sdval="2012" sdnum="2052;"><font face="Times New Roman">2012</font></td>
		<td align="center" valign=middle sdval="46" sdnum="2052;"><font face="Times New Roman">46</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" valign=middle sdval="72" sdnum="2052;"><font face="Times New Roman">72</font></td>
		<td align="center" valign=middle sdval="67" sdnum="2052;"><font face="Times New Roman">67</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
	</tr>
	<tr>
		<td height="20" align="center" valign=middle><font face="Times New Roman">Jaderberg et al. [3]</font></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><font face="Times New Roman">ECCV</font></td>
		<td align="center" valign=middle sdval="2014" sdnum="2052;"><font face="Times New Roman">2014</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" valign=middle sdval="56" sdnum="2052;"><font face="Times New Roman">56</font></td>
		<td align="center" valign=middle sdval="80" sdnum="2052;"><font face="Times New Roman">80</font></td>
		<td align="center" valign=middle sdval="75" sdnum="2052;"><font face="Times New Roman">75</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
	</tr>
	<tr>
		<td height="20" align="center" valign=middle><font face="Times New Roman">Alsharif et al. [4]</font></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><font face="Times New Roman">ICLR</font></td>
		<td align="center" valign=middle sdval="2014" sdnum="2052;"><font face="Times New Roman">2014</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" valign=middle sdval="48" sdnum="2052;"><font face="Times New Roman">48</font></td>
		<td align="center" valign=middle sdval="77" sdnum="2052;"><font face="Times New Roman">77</font></td>
		<td align="center" valign=middle sdval="70" sdnum="2052;"><font face="Times New Roman">70</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
	</tr>
	<tr>
		<td height="20" align="center" valign=middle><font face="Times New Roman">Yao et al. [5]</font></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><font face="Times New Roman">TIP</font></td>
		<td align="center" valign=middle sdval="2014" sdnum="2052;"><font face="Times New Roman">2014</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle sdval="48.6" sdnum="2052;"><font face="Times New Roman">48.6</font></td>
		<td align="center" valign=middle><br></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
	</tr>
	<tr>
		<td height="20" align="center" valign=middle><font face="Times New Roman">Neumann et al. [6]</font></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><font face="Times New Roman">TPAMI</font></td>
		<td align="center" valign=middle sdval="2015" sdnum="2052;"><font face="Times New Roman">2015</font></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle sdval="68.1" sdnum="2052;"><font face="Times New Roman">68.1</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" valign=middle sdval="45.2" sdnum="2052;"><font face="Times New Roman">45.2</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" valign=middle sdval="35" sdnum="2052;"><font face="Times New Roman">35</font></td>
		<td align="center" valign=middle sdval="19.9" sdnum="2052;"><font face="Times New Roman">19.9</font></td>
		<td align="center" valign=middle sdval="15.6" sdnum="2052;"><font face="Times New Roman">15.6</font></td>
		<td align="center" valign=middle sdval="35" sdnum="2052;"><font face="Times New Roman">35</font></td>
		<td align="center" valign=middle sdval="19.9" sdnum="2052;"><font face="Times New Roman">19.9</font></td>
		<td align="center" valign=middle sdval="15.6" sdnum="2052;"><font face="Times New Roman">15.6</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
	</tr>
	<tr>
		<td height="20" align="center" valign=middle><font face="Times New Roman">Jaderberg et al. [7]</font></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><font face="Times New Roman">IJCV</font></td>
		<td align="center" valign=middle sdval="2016" sdnum="2052;"><font face="Times New Roman">2016</font></td>
		<td align="center" valign=middle sdval="53" sdnum="2052;"><font face="Times New Roman">53</font></td>
		<td align="center" valign=middle sdval="76" sdnum="2052;"><font face="Times New Roman">76</font></td>
		<td align="center" valign=middle sdval="90" sdnum="2052;"><font face="Times New Roman">90</font></td>
		<td align="center" valign=middle sdval="86" sdnum="2052;"><font face="Times New Roman">86</font></td>
		<td align="center" valign=middle sdval="78" sdnum="2052;"><font face="Times New Roman">78</font></td>
		<td align="center" valign=middle sdval="76" sdnum="2052;"><font face="Times New Roman">76</font></td>
		<td align="center" valign=middle sdval="76" sdnum="2052;"><font face="Times New Roman">76</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
	</tr>
	<tr>
		<td height="20" align="center" valign=middle><font face="Times New Roman">Liao et al. [8]</font></td>
		<td align="center" valign=middle><font face="Times New Roman">TextBoxes</font></td>
		<td align="center" valign=middle><font face="Times New Roman">AAAI</font></td>
		<td align="center" valign=middle sdval="2017" sdnum="2052;"><font face="Times New Roman">2017</font></td>
		<td align="center" valign=middle sdval="64" sdnum="2052;"><font face="Times New Roman">64</font></td>
		<td align="center" valign=middle sdval="84" sdnum="2052;"><font face="Times New Roman">84</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" valign=middle sdval="87" sdnum="2052;"><font face="Times New Roman">87</font></td>
		<td align="center" valign=middle sdval="91" sdnum="2052;"><font face="Times New Roman">91</font></td>
		<td align="center" valign=middle sdval="89" sdnum="2052;"><font face="Times New Roman">89</font></td>
		<td align="center" valign=middle sdval="84" sdnum="2052;"><font face="Times New Roman">84</font></td>
		<td align="center" valign=middle sdval="94" sdnum="2052;"><font face="Times New Roman">94</font></td>
		<td align="center" valign=middle sdval="92" sdnum="2052;"><font face="Times New Roman">92</font></td>
		<td align="center" valign=middle sdval="87" sdnum="2052;"><font face="Times New Roman">87</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" valign=middle sdval="36.3" sdnum="2052;"><font face="Times New Roman">36.3</font></td>
		<td align="center" valign=middle sdval="48.9" sdnum="2052;"><font face="Times New Roman">48.9</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
	</tr>
	<tr>
		<td height="20" align="center" valign=middle><font face="Times New Roman">Bŭsta et al. [9]</font></td>
		<td align="center" valign=middle><font face="Times New Roman">Deep TextSpotter</font></td>
		<td align="center" valign=middle><font face="Times New Roman">ICCV</font></td>
		<td align="center" valign=middle sdval="2017" sdnum="2052;"><font face="Times New Roman">2017</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" valign=middle sdval="89" sdnum="2052;"><font face="Times New Roman">89</font></td>
		<td align="center" valign=middle sdval="86" sdnum="2052;"><font face="Times New Roman">86</font></td>
		<td align="center" valign=middle sdval="77" sdnum="2052;"><font face="Times New Roman">77</font></td>
		<td align="center" valign=middle sdval="92" sdnum="2052;"><font face="Times New Roman">92</font></td>
		<td align="center" valign=middle sdval="89" sdnum="2052;"><font face="Times New Roman">89</font></td>
		<td align="center" valign=middle sdval="81" sdnum="2052;"><font face="Times New Roman">81</font></td>
		<td align="center" valign=middle sdval="54" sdnum="2052;"><font face="Times New Roman">54</font></td>
		<td align="center" valign=middle sdval="51" sdnum="2052;"><font face="Times New Roman">51</font></td>
		<td align="center" valign=middle sdval="47" sdnum="2052;"><font face="Times New Roman">47</font></td>
		<td align="center" valign=middle sdval="58" sdnum="2052;"><font face="Times New Roman">58</font></td>
		<td align="center" valign=middle sdval="53" sdnum="2052;"><font face="Times New Roman">53</font></td>
		<td align="center" valign=middle sdval="51" sdnum="2052;"><font face="Times New Roman">51</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">21.85</font></td>
	</tr>
	<tr>
		<td height="20" align="center" valign=middle><font face="Times New Roman">Li et al. [10]</font></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><font face="Times New Roman">ICCV</font></td>
		<td align="center" valign=middle sdval="2017" sdnum="2052;"><font face="Times New Roman">2017</font></td>
		<td align="center" valign=middle sdval="66.18" sdnum="2052;"><font face="Times New Roman">66.18</font></td>
		<td align="center" valign=middle sdval="84.91" sdnum="2052;"><font face="Times New Roman">84.91</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" valign=middle sdval="87.7" sdnum="2052;"><font face="Times New Roman">87.7</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" valign=middle sdval="91.08" sdnum="2052;"><font face="Times New Roman">91.08</font></td>
		<td align="center" valign=middle sdval="89.8" sdnum="2052;"><font face="Times New Roman">89.8</font></td>
		<td align="center" valign=middle sdval="84.6" sdnum="2052;"><font face="Times New Roman">84.6</font></td>
		<td align="center" valign=middle sdval="94.2" sdnum="2052;"><font face="Times New Roman">94.2</font></td>
		<td align="center" valign=middle sdval="92.4" sdnum="2052;"><font face="Times New Roman">92.4</font></td>
		<td align="center" valign=middle sdval="88.2" sdnum="2052;"><font face="Times New Roman">88.2</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
	</tr>
	<tr>
		<td height="20" align="center" valign=middle><font face="Times New Roman">Sun et al. [22]</font></td>
		<td align="center" valign=middle><font face="Times New Roman">TextNet </font></td>
		<td align="center" valign=middle><font face="Times New Roman">ACCV</font></td>
		<td align="center" valign=middle sdval="2018" sdnum="2052;"><font face="Times New Roman">2018</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">89.77</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">88.80</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">82.96</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">94.59</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">93.48</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">86.99</font></td>
		<td align="center" valign=middle sdval="78.66" sdnum="2052;"><font face="Times New Roman">78.66</font></td>
		<td align="center" valign=middle sdval="74.9" sdnum="2052;"><font face="Times New Roman">74.9</font></td>
		<td align="center" valign=middle sdval="60.45" sdnum="2052;"><font face="Times New Roman">60.45</font></td>
		<td align="center" valign=middle sdval="82.38" sdnum="2052;"><font face="Times New Roman">82.38</font></td>
		<td align="center" valign=middle sdval="78.43" sdnum="2052;"><font face="Times New Roman">78.43</font></td>
		<td align="center" valign=middle sdval="62.36" sdnum="2052;"><font face="Times New Roman">62.36</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">54.02</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
	</tr>
	<tr>
		<td height="20" align="center" valign=middle><font face="Times New Roman">Lyu et al. [11]</font></td>
		<td align="center" valign=middle><font face="Times New Roman">Mask TextSpotter</font></td>
		<td align="center" valign=middle><font face="Times New Roman">ECCV</font></td>
		<td align="center" valign=middle sdval="2018" sdnum="2052;"><font face="Times New Roman">2018</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" valign=middle sdval="92.2" sdnum="2052;"><font face="Times New Roman">92.2</font></td>
		<td align="center" valign=middle sdval="91.1" sdnum="2052;"><font face="Times New Roman">91.1</font></td>
		<td align="center" valign=middle sdval="86.5" sdnum="2052;"><font face="Times New Roman">86.5</font></td>
		<td align="center" valign=middle sdval="92.5" sdnum="2052;"><font face="Times New Roman">92.5</font></td>
		<td align="center" valign=middle sdval="92" sdnum="2052;"><font face="Times New Roman">92</font></td>
		<td align="center" valign=middle sdval="88.2" sdnum="2052;"><font face="Times New Roman">88.2</font></td>
		<td align="center" valign=middle sdval="79.3" sdnum="2052;"><font face="Times New Roman">79.3</font></td>
		<td align="center" valign=middle sdval="73" sdnum="2052;"><font face="Times New Roman">73</font></td>
		<td align="center" valign=middle sdval="62.4" sdnum="2052;"><font face="Times New Roman">62.4</font></td>
		<td align="center" valign=middle sdval="79.3" sdnum="2052;"><font face="Times New Roman">79.3</font></td>
		<td align="center" valign=middle sdval="74.5" sdnum="2052;"><font face="Times New Roman">74.5</font></td>
		<td align="center" valign=middle sdval="64.2" sdnum="2052;"><font face="Times New Roman">64.2</font></td>
		<td align="center" valign=middle sdval="52.9" sdnum="2052;"><font face="Times New Roman">52.9</font></td>
		<td align="center" valign=middle sdval="71.8" sdnum="2052;"><font face="Times New Roman">71.8</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
	</tr>
	<tr>
		<td height="20" align="center" valign=middle><font face="Times New Roman">He et al. [12]</font></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><font face="Times New Roman">CVPR</font></td>
		<td align="center" valign=middle sdval="2018" sdnum="2052;"><font face="Times New Roman">2018</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" valign=middle sdval="91" sdnum="2052;"><font face="Times New Roman">91</font></td>
		<td align="center" valign=middle sdval="89" sdnum="2052;"><font face="Times New Roman">89</font></td>
		<td align="center" valign=middle sdval="86" sdnum="2052;"><font face="Times New Roman">86</font></td>
		<td align="center" valign=middle sdval="93" sdnum="2052;"><font face="Times New Roman">93</font></td>
		<td align="center" valign=middle sdval="92" sdnum="2052;"><font face="Times New Roman">92</font></td>
		<td align="center" valign=middle sdval="87" sdnum="2052;"><font face="Times New Roman">87</font></td>
		<td align="center" valign=middle sdval="82" sdnum="2052;"><font face="Times New Roman">82</font></td>
		<td align="center" valign=middle sdval="77" sdnum="2052;"><font face="Times New Roman">77</font></td>
		<td align="center" valign=middle sdval="63" sdnum="2052;"><font face="Times New Roman">63</font></td>
		<td align="center" valign=middle sdval="85" sdnum="2052;"><font face="Times New Roman">85</font></td>
		<td align="center" valign=middle sdval="80" sdnum="2052;"><font face="Times New Roman">80</font></td>
		<td align="center" valign=middle sdval="65" sdnum="2052;"><font face="Times New Roman">65</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
	</tr>
	<tr>
		<td height="20" align="center" valign=middle><font face="Times New Roman">Liu et al. [13]</font></td>
		<td align="center" valign=middle><font face="Times New Roman">FOTS</font></td>
		<td align="center" valign=middle><font face="Times New Roman">CVPR</font></td>
		<td align="center" valign=middle sdval="2018" sdnum="2052;"><font face="Times New Roman">2018</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" valign=middle sdval="91.99" sdnum="2052;"><font face="Times New Roman">91.99</font></td>
		<td align="center" valign=middle sdval="90.11" sdnum="2052;"><font face="Times New Roman">90.11</font></td>
		<td align="center" valign=middle sdval="84.77" sdnum="2052;"><font face="Times New Roman">84.77</font></td>
		<td align="center" valign=middle sdval="95.94" sdnum="2052;"><font face="Times New Roman">95.94</font></td>
		<td align="center" valign=middle sdval="93.9" sdnum="2052;"><font face="Times New Roman">93.9</font></td>
		<td align="center" valign=middle sdval="87.76" sdnum="2052;"><font face="Times New Roman">87.76</font></td>
		<td align="center" valign=middle sdval="83.55" sdnum="2052;"><font face="Times New Roman">83.55</font></td>
		<td align="center" valign=middle sdval="79.11" sdnum="2052;"><font face="Times New Roman">79.11</font></td>
		<td align="center" valign=middle sdval="65.33" sdnum="2052;"><font face="Times New Roman">65.33</font></td>
		<td align="center" valign=middle sdval="87.01" sdnum="2052;"><font face="Times New Roman">87.01</font></td>
		<td align="center" valign=middle sdval="82.39" sdnum="2052;"><font face="Times New Roman">82.39</font></td>
		<td align="center" valign=middle sdval="67.97" sdnum="2052;"><font face="Times New Roman">67.97</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
	</tr>
	<tr>
		<td height="20" align="center" valign=middle><font face="Times New Roman">Liao et al. [14]</font></td>
		<td align="center" valign=middle><font face="Times New Roman">TextBoxes++</font></td>
		<td align="center" valign=middle><font face="Times New Roman">TIP</font></td>
		<td align="center" valign=middle sdval="2018" sdnum="2052;"><font face="Times New Roman">2018</font></td>
		<td align="center" valign=middle sdval="64" sdnum="2052;"><font face="Times New Roman">64</font></td>
		<td align="center" valign=middle sdval="84" sdnum="2052;"><font face="Times New Roman">84</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" valign=middle sdval="93" sdnum="2052;"><font face="Times New Roman">93</font></td>
		<td align="center" valign=middle sdval="92" sdnum="2052;"><font face="Times New Roman">92</font></td>
		<td align="center" valign=middle sdval="85" sdnum="2052;"><font face="Times New Roman">85</font></td>
		<td align="center" valign=middle sdval="96" sdnum="2052;"><font face="Times New Roman">96</font></td>
		<td align="center" valign=middle sdval="95" sdnum="2052;"><font face="Times New Roman">95</font></td>
		<td align="center" valign=middle sdval="87" sdnum="2052;"><font face="Times New Roman">87</font></td>
		<td align="center" valign=middle sdval="73.3" sdnum="2052;"><font face="Times New Roman">73.3</font></td>
		<td align="center" valign=middle sdval="65.9" sdnum="2052;"><font face="Times New Roman">65.9</font></td>
		<td align="center" valign=middle sdval="51.9" sdnum="2052;"><font face="Times New Roman">51.9</font></td>
		<td align="center" valign=middle sdval="76.5" sdnum="2052;"><font face="Times New Roman">76.5</font></td>
		<td align="center" valign=middle sdval="69" sdnum="2052;"><font face="Times New Roman">69</font></td>
		<td align="center" valign=middle sdval="54.4" sdnum="2052;"><font face="Times New Roman">54.4</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
	</tr>
	<tr>
		<td height="20" align="center"><font face="Times New Roman">Liao et al. [15]</font></td>
		<td align="center" valign=middle><font face="Times New Roman">Mask TextSpotter</font></td>
		<td align="center"><font face="Times New Roman">TPAMI</font></td>
		<td align="center" sdval="2019" sdnum="2052;">2019</td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdval="93.3" sdnum="2052;">93.3</td>
		<td align="center" sdval="91.3" sdnum="2052;">91.3</td>
		<td align="center" sdval="88.2" sdnum="2052;">88.2</td>
		<td align="center" sdval="92.7" sdnum="2052;">92.7</td>
		<td align="center" sdval="91.7" sdnum="2052;">91.7</td>
		<td align="center" sdval="87.7" sdnum="2052;">87.7</td>
		<td align="center" sdval="83" sdnum="2052;">83</td>
		<td align="center" sdval="77.7" sdnum="2052;">77.7</td>
		<td align="center" sdval="73.5" sdnum="2052;">73.5</td>
		<td align="center" sdval="82.4" sdnum="2052;">82.4</td>
		<td align="center" sdval="78.1" sdnum="2052;">78.1</td>
		<td align="center" sdval="73.6" sdnum="2052;">73.6</td>
		<td align="center" sdval="65.3" sdnum="2052;">65.3</td>
		<td align="center" sdval="77.4" sdnum="2052;">77.4</td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
	</tr>
	<tr>
		<td height="20" align="center"><font face="Times New Roman">Xing et al. [23]</font></td>
		<td align="center"><font face="Times New Roman">CharNet</font></td>
		<td align="center"><font face="Times New Roman">ICCV</font></td>
		<td align="center" sdval="2019" sdnum="2052;">2019</td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdval="85.05" sdnum="2052;">85.05</td>
		<td align="center" sdval="81.25" sdnum="2052;">81.25</td>
		<td align="center" sdval="71.08" sdnum="2052;">71.08</td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdval="69.2" sdnum="2052;">69.2</td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
	</tr>
	<tr>
		<td height="20" align="center"><font face="Times New Roman">Feng et al. [24]</font></td>
		<td align="center"><font face="Times New Roman">TextDragon </font></td>
		<td align="center"><font face="Times New Roman">ICCV</font></td>
		<td align="center" sdval="2019" sdnum="2052;">2019</td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdval="82.54" sdnum="2052;">82.54</td>
		<td align="center" sdval="78.34" sdnum="2052;">78.34</td>
		<td align="center" sdval="65.15" sdnum="2052;">65.15</td>
		<td align="center" sdval="86.22" sdnum="2052;">86.22</td>
		<td align="center" sdval="81.62" sdnum="2052;">81.62</td>
		<td align="center" sdval="68.03" sdnum="2052;">68.03</td>
		<td align="center" sdval="48.8" sdnum="2052;">48.8</td>
		<td align="center" sdval="74.8" sdnum="2052;">74.8</td>
		<td align="center" sdval="39.7" sdnum="2052;">39.7</td>
		<td align="center" sdval="72.4" sdnum="2052;">72.4</td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
	</tr>
	<tr>
		<td height="20" align="center"><font face="Times New Roman">Qin et al. [25]</font></td>
		<td align="center"><br></td>
		<td align="center"><font face="Times New Roman">ICCV</font></td>
		<td align="center" sdval="2019" sdnum="2052;">2019</td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdval="85.51" sdnum="2052;">85.51</td>
		<td align="center" sdval="81.91" sdnum="2052;">81.91</td>
		<td align="center" sdval="69.94" sdnum="2052;">69.94</td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdval="70.7" sdnum="2052;">70.7</td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
	</tr>
	<tr>
		<td height="20" align="center"><font face="Times New Roman">Qiao et al. [26]</font></td>
		<td align="center"><font face="Times New Roman">Text Perceptron </font></td>
		<td align="center"><font face="Times New Roman">AAAI</font></td>
		<td align="center" sdval="2020" sdnum="2052;">2020</td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdval="91.4" sdnum="2052;">91.4</td>
		<td align="center" sdval="90.7" sdnum="2052;">90.7</td>
		<td align="center" sdval="85.8" sdnum="2052;">85.8</td>
		<td align="center" sdval="94.9" sdnum="2052;">94.9</td>
		<td align="center" sdval="94" sdnum="2052;">94</td>
		<td align="center" sdval="88.5" sdnum="2052;">88.5</td>
		<td align="center" sdval="80.5" sdnum="2052;">80.5</td>
		<td align="center" sdval="76.6" sdnum="2052;">76.6</td>
		<td align="center" sdval="65.1" sdnum="2052;">65.1</td>
		<td align="center" sdval="84.1" sdnum="2052;">84.1</td>
		<td align="center" sdval="79.4" sdnum="2052;">79.4</td>
		<td align="center" sdval="67.9" sdnum="2052;">67.9</td>
		<td align="center" sdval="69.7" sdnum="2052;">69.7</td>
		<td align="center" sdval="78.3" sdnum="2052;">78.3</td>
		<td align="center" sdval="57" sdnum="2052;">57</td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
	</tr>
	<tr>
		<td height="20" align="center"><font face="Times New Roman">Wang et al. [27]</font></td>
		<td align="center"><br></td>
		<td align="center"><font face="Times New Roman">AAAI</font></td>
		<td align="center" sdval="2020" sdnum="2052;">2020</td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdval="88.2" sdnum="2052;">88.2</td>
		<td align="center" sdval="87.7" sdnum="2052;">87.7</td>
		<td align="center" sdval="84.1" sdnum="2052;">84.1</td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdval="79.7" sdnum="2052;">79.7</td>
		<td align="center" sdval="75.2" sdnum="2052;">75.2</td>
		<td align="center" sdval="64.1" sdnum="2052;">64.1</td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdval="65" sdnum="2052;">65</td>
		<td align="center" sdval="76.1" sdnum="2052;">76.1</td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdval="41.3" sdnum="2052;">41.3</td>
	</tr>
	<tr>
		<td height="20" align="center"><font face="Times New Roman">Liu et al. [28]</font></td>
		<td align="center"><font face="Times New Roman">ABCNet</font></td>
		<td align="center"><font face="Times New Roman">CVPR</font></td>
		<td align="center" sdval="2020" sdnum="2052;">2020</td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
		<td align="center" sdval="69.5" sdnum="2052;">69.5</td>
		<td align="center" sdval="78.4" sdnum="2052;">78.4</td>
		<td align="center" sdval="45.2" sdnum="2052;">45.2</td>
		<td align="center" sdval="74.1" sdnum="2052;">74.1</td>
		<td align="center" sdnum="2052;0;@"><font face="Times New Roman">~</font></td>
	</tr>
</table>

<a id="3-field-survey"></a>
## 3. Survey

**[A] \[TPAMI-2015]** Ye Q, Doermann D. **Text detection and recognition in imagery: A survey**[J]. IEEE transactions on pattern analysis and machine intelligence, 2015, 37(7): 1480-1500. [paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=6945320)

**[B] \[Frontiers-Comput. Sci-2016]** Zhu Y, Yao C, Bai X. **Scene text detection and recognition: Recent advances and future trends**[J]. Frontiers of Computer Science, 2016, 10(1): 19-36. [paper](https://link.springer.com/article/10.1007/s11704-015-4488-0)

**[C] \[arXiv-2018]** Long S, He X, Ya C. **Scene Text Detection and Recognition: The Deep Learning Era**[J]. arXiv preprint arXiv:1811.04256, 2018. [paper](https://arxiv.org/pdf/1811.04256.pdf)

<a id="4-ocr-service"></a>
## 4. OCR Service

|                             OCR                              | API  | Free |
| :----------------------------------------------------------: | :--: | :--: |
| [Tesseract OCR Engine](https://github.com/tesseract-ocr/tesseract) |  ×   |  √   |
| [Azure](https://azure.microsoft.com/zh-cn/services/cognitive-services/computer-vision/#Analysis) |  √   |  √   |
| [ABBYY](https://www.abbyy.cn/real-time-recognition-sdk/technical-specifications/) |  √   |  √   |
|               [OCR Space](https://ocr.space/)                |  √   |  √   |
|       [SODA PDF OCR](https://www.sodapdf.com/ocr-pdf/)       |  √   |  √   |
|          [Free Online OCR](https://www.newocr.com/)          |  √   |  √   |
|           [Online OCR](https://www.onlineocr.net/)           |  √   |  √   |
|             [Super Tools](https://www.wdku.net/)             |  √   |  √   |
|          [Online Chinese Recognition](http://chongdata.com/ocr/)           |  √   |  √   |
|   [Calamari OCR](https://github.com/Calamari-OCR/calamari)   |  ×   |  √   |
|   [Tencent OCR](https://cloud.tencent.com/product/ocr?lang=cn)   |  √   |  ×   |


<a id="5-references"></a>
## 5. References and codes

- [1] Wang K, Babenko B, Belongie S. **End-to-end scene text recognition**[C].2011 International Conference on Computer Vision. IEEE, 2011: 1457-1464. [paper](http://www.iapr-tc11.org/dataset/SVT/wang_iccv2011.pdf)

- [2] Wang T, Wu D J, Coates A, et al. **End-to-end text recognition with convolutional neural networks**[C]. Proceedings of the 21st International Conference on Pattern Recognition (ICPR2012). IEEE, 2012: 3304-3308. [paper](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.664.6212&rep=rep1&type=pdf)

- [3] Jaderberg M, Vedaldi A, Zisserman A. **Deep features for text spotting**[C]. European conference on computer vision. Springer, Cham, 2014: 512-528. [paper](http://www.robots.ox.ac.uk/~vedaldi/assets/pubs/jaderberg14deep.pdf)

- [4] Alsharif O, Pineau J. **End-to-End Text Recognition with Hybrid HMM Maxout Models**[C]. In ICLR 2014. [paper](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.740.1108&rep=rep1&type=pdf)

- [5] Yao C, Bai X, Liu W. **A unified framework for multioriented text detection and recognition**[J]. IEEE Transactions on Image Processing, 2014, 23(11): 4737-4749. [paper](http://www.vlrlab.net/admin/uploads/avatars/A_Unified_Framework_for_Multi-Oriented_Text_Detection_and_Recognition.pdf)

- [6] Neumann L, Matas J. **Real-time lexicon-free scene text localization and recognition**[J]. IEEE transactions on pattern analysis and machine intelligence, 2015, 38(9): 1872-1885. [paper](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.717.4947&rep=rep1&type=pdf)

- [7] Jaderberg M, Simonyan K, Vedaldi A, et al. **Reading text in the wild with convolutional neural networks**[J]. International Journal of Computer Vision, 2016, 116(1): 1-20. [paper](http://www.academia.edu/download/43938680/jaderberg16.pdf)

- [8] Liao M, Shi B, Bai X, et al. **Textboxes: A fast text detector with a single deep neural network**[C]. In AAAI 2017. [paper](https://www.aaai.org/ocs/index.php/AAAI/AAAI17/paper/viewPDFInterstitial/14202/14295) [code](https://github.com/MhLiao/TextBoxes)

- [9] Busta M, Neumann L, Matas J. **Deep textspotter: An end-to-end trainable scene text localization and recognition framework**[C]. Proceedings of the IEEE International Conference on Computer Vision. 2017: 2204-2212. [paper](http://openaccess.thecvf.com/content_ICCV_2017/papers/Busta_Deep_TextSpotter_An_ICCV_2017_paper.pdf)

- [10] Li H, Wang P,  Shen C. **Towards end-to-end text spotting with convolutional recurrent neural networks**[C]. Proceedings of the IEEE International Conference on Computer Vision. 2017: 5238-5246. [paper](http://openaccess.thecvf.com/content_ICCV_2017/papers/Li_Towards_End-To-End_Text_ICCV_2017_paper.pdf)

- [11] Lyu P, Liao M, Yao C, et al. **Mask textspotter: An end-to-end trainable neural network for spotting text with arbitrary shapes**[C]. Proceedings of the European Conference on Computer Vision (ECCV). 2018: 67-83. [paper](http://openaccess.thecvf.com/content_ECCV_2018/papers/Pengyuan_Lyu_Mask_TextSpotter_An_ECCV_2018_paper.pdf) [code](https://github.com/lvpengyuan/masktextspotter.caffe2)

- [12] He T, Tian Z, Huang W, et al. **An end-to-end textspotter with explicit alignment and attention**[C]. Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition. 2018: 5020-5029. [paper](http://openaccess.thecvf.com/content_cvpr_2018/papers/He_An_End-to-End_TextSpotter_CVPR_2018_paper.pdf) [code](https://github.com/tonghe90/textspotter)

- [13] Liu X, Liang D, Yan S, et al. **FOTS: Fast oriented text spotting with a unified network**[C]. Proceedings of the IEEE conference on computer vision and pattern recognition. 2018: 5676-5685. [paper](http://openaccess.thecvf.com/content_cvpr_2018/papers/Liu_FOTS_Fast_Oriented_CVPR_2018_paper.pdf) [code](https://github.com/jiangxiluning/FOTS.PyTorch)

- [14] Liao M, Shi B, Bai X. **Textboxes++: A single-shot oriented scene text detector**[J]. IEEE transactions on image processing, 2018, 27(8): 3676-3690. [paper](https://ieeexplore.ieee.org/abstract/document/8334248) [code](https://github.com/MhLiao/TextBoxes_plusplus)

- [15] Minghui Liao, Pengyuan Lyu, Minghang He. **Mask TextSpotter: An End-to-End Trainable Neural Network for Spotting Text with Arbitrary Shapes**[J]. IEEE transactions on pattern analysis and machine intelligence, 2019. [paper](https://arxiv.org/abs/1908.08207) [code](https://github.com/MhLiao/TextBoxes_plusplus)

- [16] Wang,Kai, and S. Belongie. **Word Spotting in the Wild**. European Conference on Computer Vision(ECCV), 2010: 591-604.  [Paper](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.168.4897&rep=rep1&type=pdf)

- [17] S. M. Lucas, A. Panaretos, L. Sosa, A. Tang, S. Wong, R. Young,K. Ashida, H. Nagai, M. Okamoto, H. Yamamoto, H. Miyao,J. Zhu, W. Ou, C. Wolf, J. Jolion, L. Todoran, M. Worring, and X. Lin. **ICDAR 2003 robust reading competitions:entries, results,and future directions**. IJDAR, 7(2-3):105–122, 2005. [paper](https://link.springer.com/content/pdf/10.1007%2Fs10032-004-0134-3.pdf)

- [18] Shahab, A, Shafait, F, Dengel, A: **ICDAR 2011 robust reading competition challenge 2: Reading text in scene images**. In: ICDAR, 2011. [Paper](https://ieeexplore.ieee.org/document/6065556)

- [19] D. Karatzas, F. Shafait, S. Uchida, et al. **ICDAR 2013 robust reading competition**. In ICDAR, 2013. [Paper](https://ieeexplore.ieee.org/document/6628859)

- [20] D. Karatzas, L. Gomez-Bigorda, A. Nicolaou, S. K. Ghosh, A. D.Bagdanov, M. Iwamura, J. Matas, L. Neumann, V. R. Chandrasekhar, S. Lu, F. Shafait, S. Uchida, and E. Valveny. **ICDAR 2015 competition on robust reading**. In ICDAR, pages 1156–1160, 2015. [Paper](https://ieeexplore.ieee.org/document/7333942)

- [21] Chee C K, Chan C S. **Total-text: A comprehensive dataset for scene text detection and recognition**.Document Analysis and Recognition (ICDAR), 2017 14th IAPR International Conference on. IEEE, 2017, 1: 935-942.[Paper](https://arxiv.org/abs/1710.10400)


- [22] Y. Sun, C. Zhang, Z. Huang, J. Liu, J. Han, and E. Ding, **TextNet: Irregular Text Reading from Images with an End-to-End Trainable Network**, Asian Conference on Computer Vision (ACCV), Cham, 2018, vol. 11363, no. 1, pp. 83–99.[Paper](https://link.springer.com/chapter/10.1007/978-3-030-20893-6_6)

- [23] Xing L, Tian Z, Huang W, **Convolutional character networks**.In ICCV, 2019.[Paper](http://openaccess.thecvf.com/content_ICCV_2019/papers/Xing_Convolutional_Character_Networks_ICCV_2019_paper.pdf) [code](https://github.com/MalongTech/research-charnet)

- [24] Feng W, He W, Yin F, et al. **TextDragon: An End-to-End Framework for Arbitrary Shaped Text Spotting**.In ICCV, 2019.[Paper](http://openaccess.thecvf.com/content_ICCV_2019/papers/Feng_TextDragon_An_End-to-End_Framework_for_Arbitrary_Shaped_Text_Spotting_ICCV_2019_paper.pdf)

- [25] Qin S, Bissacco A, Raptis M, et al. **Towards unconstrained end-to-end text spotting**.In ICCV, 2019.[Paper](http://openaccess.thecvf.com/content_ICCV_2019/papers/Qin_Towards_Unconstrained_End-to-End_Text_Spotting_ICCV_2019_paper.pdf)

- [26] Qiao L, Tang S, Cheng Z, et al. **Text Perceptron: Towards End-to-End Arbitrary-Shaped Text Spotting**.In AAAI 2020.[Paper](https://www.aaai.org/Papers/AAAI/2020GB/AAAI-QiaoL.893.pdf)

- [27] Wang H, Lu P, Zhang H, et al. **All You Need Is Boundary: Toward Arbitrary-Shaped Text Spotting.** In AAAI 2020.[Paper](https://arxiv.org/abs/1911.09550)

- [28] Liu Y, Chen H, Shen C, et al. **ABCNet: Real-time Scene Text Spotting with Adaptive Bezier-Curve Network** In CVPR, 2020.[Paper](https://arxiv.org/abs/2002.10200)
[code](https://github.com/Yuliang-Liu/bezier_curve_text_spotting)
###

If you find any problems in our resources, or any good papers/codes we have missed, please inform us at    **liuchongyu1996@gmail.com**. Thank you for your contribution.



### Copyright

Copyright © 2019 SCUT-DLVC. All Rights Reserved.

<p align="center">
    <img src="scut-dlvc.jpeg" alt="Sample"  width="150" height="75">
    <p align="center">
        <em></em>
    </p>
</p>
