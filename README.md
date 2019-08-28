# End-to-End Scene Text Detection and Recognition System Resources

<p align='right'>Author: Canjie Luo</p>

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
		<td height="20" align="left" valign=middle><font face="Arial">Wang et al. [1]</font></td>
		<td align="left" valign=middle><br></td>
		<td align="left" sdnum="2052;0;@">✕</td>
		<td align="left" valign=middle><font face="Arial">Sliding windows and Random Ferns</font></td>
		<td align="left" valign=middle><font face="Arial">Pictorial Structures</font></td>
		<td align="left" valign=middle><font face="Arial">ICCV</font></td>
		<td align="left" valign=middle sdval="2011" sdnum="2052;"><font face="Arial">2011</font></td>
		<td align="left" valign=middle><font face="Arial">Word Re-scoring for NMS</font></td>
	</tr>
	<tr>
		<td height="20" align="left" valign=middle><font face="Arial">Wang et al. [2]</font></td>
		<td align="left" valign=middle><br></td>
		<td align="left" sdnum="2052;0;@">✕</td>
		<td align="left" valign=middle><font face="Arial">CNN-based</font></td>
		<td align="left" valign=middle><font face="Arial">Sliding windows for classification</font></td>
		<td align="left" valign=middle><font face="Arial">ICPR</font></td>
		<td align="left" valign=middle sdval="2012" sdnum="2052;"><font face="Arial">2012</font></td>
		<td align="left" valign=middle><font face="Arial">CNN architecture</font></td>
	</tr>
	<tr>
		<td height="20" align="left" valign=middle><font face="Arial">Jaderberg et al. [3]</font></td>
		<td align="left" valign=middle><br></td>
		<td align="left" sdnum="2052;0;@">✕</td>
		<td align="left" valign=middle><font face="Arial">CNN-based and saliency maps</font></td>
		<td align="left" valign=middle><font face="Arial">CNN classifier</font></td>
		<td align="left" valign=middle><font face="Arial">ECCV</font></td>
		<td align="left" valign=middle sdval="2014" sdnum="2052;"><font face="Arial">2014</font></td>
		<td align="left" valign=middle><font face="Arial">Data mining and annotation</font></td>
	</tr>
	<tr>
		<td height="20" align="left" valign=middle><font face="Arial">Alsharif et al. [4]</font></td>
		<td align="left" valign=middle><br></td>
		<td align="left" sdnum="2052;0;@">✕</td>
		<td align="left" valign=middle><font face="Arial">CNN and hybrid HMM maxout models</font></td>
		<td align="left" valign=middle><font face="Arial">Segmentation-based</font></td>
		<td align="left" valign=middle><font face="Arial">ICLR</font></td>
		<td align="left" valign=middle sdval="2014" sdnum="2052;"><font face="Arial">2014</font></td>
		<td align="left" valign=middle><font face="Arial">Hybrid HMM maxout models</font></td>
	</tr>
	<tr>
		<td height="20" align="left" valign=middle><font face="Arial">Yao et al. [5]</font></td>
		<td align="left" valign=middle><br></td>
		<td align="left" sdnum="2052;0;@">✕</td>
		<td align="left" valign=middle><font face="Arial">Random Forest</font></td>
		<td align="left" valign=middle><font face="Arial">Component Linking and Word Partition</font></td>
		<td align="left" valign=middle><font face="Arial">TIP</font></td>
		<td align="left" valign=middle sdval="2014" sdnum="2052;"><font face="Arial">2014</font></td>
		<td align="left" valign=middle><font face="Arial">(1) Detection and recognition features sharing. (2) Oriented-text. (3) A new dictionary search method</font></td>
	</tr>
	<tr>
		<td height="20" align="left" valign=middle><font face="Arial">Neumann et al. [6]</font></td>
		<td align="left" valign=middle><br></td>
		<td align="left" sdnum="2052;0;@">✕</td>
		<td align="left" valign=middle><font face="Arial">Extremal Regions</font></td>
		<td align="left" valign=middle><font face="Arial">Clustering algorithm to group characters</font></td>
		<td align="left" valign=middle><font face="Arial">TPAMI</font></td>
		<td align="left" valign=middle sdval="2015" sdnum="2052;"><font face="Arial">2015</font></td>
		<td align="left" valign=middle><font face="Arial">Real-time performance(1.6s/image)</font></td>
	</tr>
	<tr>
		<td height="20" align="left" valign=middle><font face="Arial">Jaderberg et al. [7]</font></td>
		<td align="left" valign=middle><br></td>
		<td align="left" sdnum="2052;0;@">✕</td>
		<td align="left" valign=middle><font face="Arial">Region proposal mechanism</font></td>
		<td align="left" valign=middle><font face="Arial">Word-level classification</font></td>
		<td align="left" valign=middle><font face="Arial">IJCV</font></td>
		<td align="left" valign=middle sdval="2016" sdnum="2052;"><font face="Arial">2016</font></td>
		<td align="left" valign=middle><font face="Arial">Trained only on data produced by a synthetic text generation engine, requiring no human labelled data</font></td>
	</tr>
	<tr>
		<td height="20" align="left" valign=middle><font face="Arial">Liao et al. [8]</font></td>
		<td align="left" valign=middle><font face="Arial">TextBoxes</font></td>
		<td align="left" sdnum="2052;0;@">✓</td>
		<td align="left" valign=middle><font face="Arial">SSD-based framework</font></td>
		<td align="left" valign=middle><font face="Arial">CRNN</font></td>
		<td align="left" valign=middle><font face="Arial">AAAI</font></td>
		<td align="left" valign=middle sdval="2017" sdnum="2052;"><font face="Arial">2017</font></td>
		<td align="left" valign=middle><font face="Arial">An end-to-end trainable fast scene text detector</font></td>
	</tr>
	<tr>
		<td height="20" align="left" valign=middle><font face="Arial">Bŭsta et al. [9]</font></td>
		<td align="left" valign=middle><font face="Arial">Deep TextSpotter</font></td>
		<td align="left" sdnum="2052;0;@">✕</td>
		<td align="left" valign=middle><font face="Arial">Yolo v2</font></td>
		<td align="left" valign=middle><font face="Arial">CTC</font></td>
		<td align="left" valign=middle><font face="Arial">ICCV</font></td>
		<td align="left" valign=middle sdval="2017" sdnum="2052;"><font face="Arial">2017</font></td>
		<td align="left" valign=middle><font face="Arial">Yolov2 + RPN, RNN + CTC. It is the first end-to-end trainable detection and recognition system with high speed.</font></td>
	</tr>
	<tr>
		<td height="20" align="left" valign=middle><font face="Arial">Li et al. [10]</font></td>
		<td align="left" valign=middle><br></td>
		<td align="left" sdnum="2052;0;@">✕</td>
		<td align="left" valign=middle><font face="Arial">Text Proposal Network</font></td>
		<td align="left" valign=middle><font face="Arial">Attention</font></td>
		<td align="left" valign=middle><font face="Arial">ICCV</font></td>
		<td align="left" valign=middle sdval="2017" sdnum="2052;"><font face="Arial">2017</font></td>
		<td align="left" valign=middle><font face="Arial">TPN + RNN encoder + attention-based RNN</font></td>
	</tr>
	<tr>
		<td height="20" align="left" valign=middle><font face="Arial">Lyu et al. [11]</font></td>
		<td align="left" valign=middle><font face="Arial">Mask TextSpotter</font></td>
		<td align="left" sdnum="2052;0;@">✓</td>
		<td align="left" valign=middle><font face="Arial">Fast R-CNN with mask branch</font></td>
		<td align="left" valign=middle><font face="Arial">Character segmentation</font></td>
		<td align="left" valign=middle><font face="Arial">ECCV</font></td>
		<td align="left" valign=middle sdval="2018" sdnum="2052;"><font face="Arial">2018</font></td>
		<td align="left" valign=middle><font face="Arial">Precise text detection and recognition are acquired via semantic segmentation</font></td>
	</tr>
	<tr>
		<td height="20" align="left" valign=middle><font face="Arial">He et al. [12]</font></td>
		<td align="left" valign=middle><br></td>
		<td align="left" sdnum="2052;0;@">✓</td>
		<td align="left" valign=middle><font face="Arial">Text-Alignment Layer</font></td>
		<td align="left" valign=middle><font face="Arial">Attention</font></td>
		<td align="left" valign=middle><font face="Arial">CVPR</font></td>
		<td align="left" valign=middle sdval="2018" sdnum="2052;"><font face="Arial">2018</font></td>
		<td align="left" valign=middle><font face="Arial">Character attention mechanism: use character spatial information as explicit supervision</font></td>
	</tr>
	<tr>
		<td height="20" align="left" valign=middle><font face="Arial">Liu et al. [13]</font></td>
		<td align="left" valign=middle><font face="Arial">FOTS</font></td>
		<td align="left" sdnum="2052;0;@">✓</td>
		<td align="left" valign=middle><font face="Arial">EAST with RoIRotate</font></td>
		<td align="left" valign=middle><font face="Arial">CTC</font></td>
		<td align="left" valign=middle><font face="Arial">CVPR</font></td>
		<td align="left" valign=middle sdval="2018" sdnum="2052;"><font face="Arial">2018</font></td>
		<td align="left" valign=middle><font face="Arial">Little computation overhead compared to baseline text detection network (22.6fps)</font></td>
	</tr>
	<tr>
		<td height="20" align="left" valign=middle><font face="Arial">Liao et al. [14]</font></td>
		<td align="left" valign=middle><font face="Arial">TextBoxes++</font></td>
		<td align="left" sdnum="2052;0;@">✓</td>
		<td align="left" valign=middle><font face="Arial">SSD-based framework</font></td>
		<td align="left" valign=middle><font face="Arial">CRNN</font></td>
		<td align="left" valign=middle><font face="Arial">TIP</font></td>
		<td align="left" valign=middle sdval="2018" sdnum="2052;"><font face="Arial">2018</font></td>
		<td align="left" valign=middle><font face="Arial">Journal version of TextBoxes (multi-oriented scene text support)</font></td>
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
		<td colspan=3 align="center" valign=middle><b><font face="Arial">End-to-end</font></b></td>
		<td colspan=3 align="center" valign=middle><b><font face="Arial">Spotting</font></b></td>
		<td colspan=3 align="center" valign=middle><b><font face="Arial">End-to-end</font></b></td>
		<td colspan=3 align="center" valign=middle><b><font face="Arial">Spotting</font></b></td>
		<td rowspan=2 align="center" valign=middle><b><font face="Arial">None</font></b></td>
		<td rowspan=2 align="center" valign=middle><b><font face="Arial">Full</font></b></td>
	</tr>
	<tr>
		<td align="center" valign=middle sdval="50" sdnum="2052;"><b><font face="Arial">50</font></b></td>
		<td align="center" valign=middle><b><font face="Arial">Full</font></b></td>
		<td align="center" valign=middle><b><font face="Arial">None</font></b></td>
		<td align="center" valign=middle><b><font face="Arial">S</font></b></td>
		<td align="center" valign=middle><b><font face="Arial">W </font></b></td>
		<td align="center" valign=middle><b><font face="Arial">G</font></b></td>
		<td align="center" valign=middle><b><font face="Arial">S</font></b></td>
		<td align="center" valign=middle><b><font face="Arial">W </font></b></td>
		<td align="center" valign=middle><b><font face="Arial">G</font></b></td>
		<td align="center" valign=middle><b><font face="Arial">S</font></b></td>
		<td align="center" valign=middle><b><font face="Arial">W </font></b></td>
		<td align="center" valign=middle><b><font face="Arial">G</font></b></td>
		<td align="center" valign=middle><b><font face="Arial">S</font></b></td>
		<td align="center" valign=middle><b><font face="Arial">W </font></b></td>
		<td align="center" valign=middle><b><font face="Arial">G</font></b></td>
		</tr>
	<tr>
		<td height="20" align="center" valign=middle><font face="Arial">Wang et al. [1]</font></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><font face="Arial">ICCV</font></td>
		<td align="center" valign=middle sdval="2011" sdnum="2052;"><font face="Arial">2011</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" valign=middle sdval="51" sdnum="2052;"><font face="Arial">51</font></td>
		<td align="center" valign=middle><br></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
	</tr>
	<tr>
		<td height="20" align="center" valign=middle><font face="Arial">Wang et al. [2]</font></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><font face="Arial">ICPR</font></td>
		<td align="center" valign=middle sdval="2012" sdnum="2052;"><font face="Arial">2012</font></td>
		<td align="center" valign=middle sdval="46" sdnum="2052;"><font face="Arial">46</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" valign=middle sdval="72" sdnum="2052;"><font face="Arial">72</font></td>
		<td align="center" valign=middle sdval="67" sdnum="2052;"><font face="Arial">67</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
	</tr>
	<tr>
		<td height="20" align="center" valign=middle><font face="Arial">Jaderberg et al. [3]</font></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><font face="Arial">ECCV</font></td>
		<td align="center" valign=middle sdval="2014" sdnum="2052;"><font face="Arial">2014</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" valign=middle sdval="56" sdnum="2052;"><font face="Arial">56</font></td>
		<td align="center" valign=middle sdval="80" sdnum="2052;"><font face="Arial">80</font></td>
		<td align="center" valign=middle sdval="75" sdnum="2052;"><font face="Arial">75</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
	</tr>
	<tr>
		<td height="20" align="center" valign=middle><font face="Arial">Alsharif et al. [4]</font></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><font face="Arial">ICLR</font></td>
		<td align="center" valign=middle sdval="2014" sdnum="2052;"><font face="Arial">2014</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" valign=middle sdval="48" sdnum="2052;"><font face="Arial">48</font></td>
		<td align="center" valign=middle sdval="77" sdnum="2052;"><font face="Arial">77</font></td>
		<td align="center" valign=middle sdval="70" sdnum="2052;"><font face="Arial">70</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
	</tr>
	<tr>
		<td height="20" align="center" valign=middle><font face="Arial">Yao et al. [5]</font></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><font face="Arial">TIP</font></td>
		<td align="center" valign=middle sdval="2014" sdnum="2052;"><font face="Arial">2014</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle sdval="48.6" sdnum="2052;"><font face="Arial">48.6</font></td>
		<td align="center" valign=middle><br></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
	</tr>
	<tr>
		<td height="20" align="center" valign=middle><font face="Arial">Neumann et al. [6]</font></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><font face="Arial">TPAMI</font></td>
		<td align="center" valign=middle sdval="2015" sdnum="2052;"><font face="Arial">2015</font></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle sdval="68.1" sdnum="2052;"><font face="Arial">68.1</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" valign=middle sdval="45.2" sdnum="2052;"><font face="Arial">45.2</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" valign=middle sdval="35" sdnum="2052;"><font face="Arial">35</font></td>
		<td align="center" valign=middle sdval="19.9" sdnum="2052;"><font face="Arial">19.9</font></td>
		<td align="center" valign=middle sdval="15.6" sdnum="2052;"><font face="Arial">15.6</font></td>
		<td align="center" valign=middle sdval="35" sdnum="2052;"><font face="Arial">35</font></td>
		<td align="center" valign=middle sdval="19.9" sdnum="2052;"><font face="Arial">19.9</font></td>
		<td align="center" valign=middle sdval="15.6" sdnum="2052;"><font face="Arial">15.6</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
	</tr>
	<tr>
		<td height="20" align="center" valign=middle><font face="Arial">Jaderberg et al. [7]</font></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><font face="Arial">IJCV</font></td>
		<td align="center" valign=middle sdval="2016" sdnum="2052;"><font face="Arial">2016</font></td>
		<td align="center" valign=middle sdval="53" sdnum="2052;"><font face="Arial">53</font></td>
		<td align="center" valign=middle sdval="76" sdnum="2052;"><font face="Arial">76</font></td>
		<td align="center" valign=middle sdval="90" sdnum="2052;"><font face="Arial">90</font></td>
		<td align="center" valign=middle sdval="86" sdnum="2052;"><font face="Arial">86</font></td>
		<td align="center" valign=middle sdval="78" sdnum="2052;"><font face="Arial">78</font></td>
		<td align="center" valign=middle sdval="76" sdnum="2052;"><font face="Arial">76</font></td>
		<td align="center" valign=middle sdval="76" sdnum="2052;"><font face="Arial">76</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
	</tr>
	<tr>
		<td height="20" align="center" valign=middle><font face="Arial">Liao et al. [8]</font></td>
		<td align="center" valign=middle><font face="Arial">TextBoxes</font></td>
		<td align="center" valign=middle><font face="Arial">AAAI</font></td>
		<td align="center" valign=middle sdval="2017" sdnum="2052;"><font face="Arial">2017</font></td>
		<td align="center" valign=middle sdval="64" sdnum="2052;"><font face="Arial">64</font></td>
		<td align="center" valign=middle sdval="84" sdnum="2052;"><font face="Arial">84</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" valign=middle sdval="87" sdnum="2052;"><font face="Arial">87</font></td>
		<td align="center" valign=middle sdval="91" sdnum="2052;"><font face="Arial">91</font></td>
		<td align="center" valign=middle sdval="89" sdnum="2052;"><font face="Arial">89</font></td>
		<td align="center" valign=middle sdval="84" sdnum="2052;"><font face="Arial">84</font></td>
		<td align="center" valign=middle sdval="94" sdnum="2052;"><font face="Arial">94</font></td>
		<td align="center" valign=middle sdval="92" sdnum="2052;"><font face="Arial">92</font></td>
		<td align="center" valign=middle sdval="87" sdnum="2052;"><font face="Arial">87</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" valign=middle sdval="36.3" sdnum="2052;"><font face="Arial">36.3</font></td>
		<td align="center" valign=middle sdval="48.9" sdnum="2052;"><font face="Arial">48.9</font></td>
	</tr>
	<tr>
		<td height="20" align="center" valign=middle><font face="Arial">Bŭsta et al. [9]</font></td>
		<td align="center" valign=middle><font face="Arial">Deep TextSpotter</font></td>
		<td align="center" valign=middle><font face="Arial">ICCV</font></td>
		<td align="center" valign=middle sdval="2017" sdnum="2052;"><font face="Arial">2017</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" valign=middle sdval="89" sdnum="2052;"><font face="Arial">89</font></td>
		<td align="center" valign=middle sdval="86" sdnum="2052;"><font face="Arial">86</font></td>
		<td align="center" valign=middle sdval="77" sdnum="2052;"><font face="Arial">77</font></td>
		<td align="center" valign=middle sdval="92" sdnum="2052;"><font face="Arial">92</font></td>
		<td align="center" valign=middle sdval="89" sdnum="2052;"><font face="Arial">89</font></td>
		<td align="center" valign=middle sdval="81" sdnum="2052;"><font face="Arial">81</font></td>
		<td align="center" valign=middle sdval="54" sdnum="2052;"><font face="Arial">54</font></td>
		<td align="center" valign=middle sdval="51" sdnum="2052;"><font face="Arial">51</font></td>
		<td align="center" valign=middle sdval="47" sdnum="2052;"><font face="Arial">47</font></td>
		<td align="center" valign=middle sdval="58" sdnum="2052;"><font face="Arial">58</font></td>
		<td align="center" valign=middle sdval="53" sdnum="2052;"><font face="Arial">53</font></td>
		<td align="center" valign=middle sdval="51" sdnum="2052;"><font face="Arial">51</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
	</tr>
	<tr>
		<td height="20" align="center" valign=middle><font face="Arial">Li et al. [10]</font></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><font face="Arial">ICCV</font></td>
		<td align="center" valign=middle sdval="2017" sdnum="2052;"><font face="Arial">2017</font></td>
		<td align="center" valign=middle sdval="66.18" sdnum="2052;"><font face="Arial">66.18</font></td>
		<td align="center" valign=middle sdval="84.91" sdnum="2052;"><font face="Arial">84.91</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" valign=middle sdval="87.7" sdnum="2052;"><font face="Arial">87.7</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" valign=middle sdval="91.08" sdnum="2052;"><font face="Arial">91.08</font></td>
		<td align="center" valign=middle sdval="89.8" sdnum="2052;"><font face="Arial">89.8</font></td>
		<td align="center" valign=middle sdval="84.6" sdnum="2052;"><font face="Arial">84.6</font></td>
		<td align="center" valign=middle sdval="94.2" sdnum="2052;"><font face="Arial">94.2</font></td>
		<td align="center" valign=middle sdval="92.4" sdnum="2052;"><font face="Arial">92.4</font></td>
		<td align="center" valign=middle sdval="88.2" sdnum="2052;"><font face="Arial">88.2</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
	</tr>
	<tr>
		<td height="20" align="center" valign=middle><font face="Arial">Lyu et al. [11]</font></td>
		<td align="center" valign=middle><font face="Arial">Mask TextSpotter</font></td>
		<td align="center" valign=middle><font face="Arial">ECCV</font></td>
		<td align="center" valign=middle sdval="2018" sdnum="2052;"><font face="Arial">2018</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" valign=middle sdval="92.2" sdnum="2052;"><font face="Arial">92.2</font></td>
		<td align="center" valign=middle sdval="91.1" sdnum="2052;"><font face="Arial">91.1</font></td>
		<td align="center" valign=middle sdval="86.5" sdnum="2052;"><font face="Arial">86.5</font></td>
		<td align="center" valign=middle sdval="92.5" sdnum="2052;"><font face="Arial">92.5</font></td>
		<td align="center" valign=middle sdval="92" sdnum="2052;"><font face="Arial">92</font></td>
		<td align="center" valign=middle sdval="88.2" sdnum="2052;"><font face="Arial">88.2</font></td>
		<td align="center" valign=middle sdval="79.3" sdnum="2052;"><font face="Arial">79.3</font></td>
		<td align="center" valign=middle sdval="73" sdnum="2052;"><font face="Arial">73</font></td>
		<td align="center" valign=middle sdval="62.4" sdnum="2052;"><font face="Arial">62.4</font></td>
		<td align="center" valign=middle sdval="79.3" sdnum="2052;"><font face="Arial">79.3</font></td>
		<td align="center" valign=middle sdval="74.5" sdnum="2052;"><font face="Arial">74.5</font></td>
		<td align="center" valign=middle sdval="64.2" sdnum="2052;"><font face="Arial">64.2</font></td>
		<td align="center" valign=middle sdval="52.9" sdnum="2052;"><font face="Arial">52.9</font></td>
		<td align="center" valign=middle sdval="71.8" sdnum="2052;"><font face="Arial">71.8</font></td>
	</tr>
	<tr>
		<td height="20" align="center" valign=middle><font face="Arial">He et al. [12]</font></td>
		<td align="center" valign=middle><br></td>
		<td align="center" valign=middle><font face="Arial">CVPR</font></td>
		<td align="center" valign=middle sdval="2018" sdnum="2052;"><font face="Arial">2018</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" valign=middle sdval="91" sdnum="2052;"><font face="Arial">91</font></td>
		<td align="center" valign=middle sdval="89" sdnum="2052;"><font face="Arial">89</font></td>
		<td align="center" valign=middle sdval="86" sdnum="2052;"><font face="Arial">86</font></td>
		<td align="center" valign=middle sdval="93" sdnum="2052;"><font face="Arial">93</font></td>
		<td align="center" valign=middle sdval="92" sdnum="2052;"><font face="Arial">92</font></td>
		<td align="center" valign=middle sdval="87" sdnum="2052;"><font face="Arial">87</font></td>
		<td align="center" valign=middle sdval="82" sdnum="2052;"><font face="Arial">82</font></td>
		<td align="center" valign=middle sdval="77" sdnum="2052;"><font face="Arial">77</font></td>
		<td align="center" valign=middle sdval="63" sdnum="2052;"><font face="Arial">63</font></td>
		<td align="center" valign=middle sdval="85" sdnum="2052;"><font face="Arial">85</font></td>
		<td align="center" valign=middle sdval="80" sdnum="2052;"><font face="Arial">80</font></td>
		<td align="center" valign=middle sdval="65" sdnum="2052;"><font face="Arial">65</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
	</tr>
	<tr>
		<td height="20" align="center" valign=middle><font face="Arial">Liu et al. [13]</font></td>
		<td align="center" valign=middle><font face="Arial">FOTS</font></td>
		<td align="center" valign=middle><font face="Arial">CVPR</font></td>
		<td align="center" valign=middle sdval="2018" sdnum="2052;"><font face="Arial">2018</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" valign=middle sdval="91.99" sdnum="2052;"><font face="Arial">91.99</font></td>
		<td align="center" valign=middle sdval="90.11" sdnum="2052;"><font face="Arial">90.11</font></td>
		<td align="center" valign=middle sdval="84.77" sdnum="2052;"><font face="Arial">84.77</font></td>
		<td align="center" valign=middle sdval="95.94" sdnum="2052;"><font face="Arial">95.94</font></td>
		<td align="center" valign=middle sdval="93.9" sdnum="2052;"><font face="Arial">93.9</font></td>
		<td align="center" valign=middle sdval="87.76" sdnum="2052;"><font face="Arial">87.76</font></td>
		<td align="center" valign=middle sdval="83.55" sdnum="2052;"><font face="Arial">83.55</font></td>
		<td align="center" valign=middle sdval="79.11" sdnum="2052;"><font face="Arial">79.11</font></td>
		<td align="center" valign=middle sdval="65.33" sdnum="2052;"><font face="Arial">65.33</font></td>
		<td align="center" valign=middle sdval="87.01" sdnum="2052;"><font face="Arial">87.01</font></td>
		<td align="center" valign=middle sdval="82.39" sdnum="2052;"><font face="Arial">82.39</font></td>
		<td align="center" valign=middle sdval="67.97" sdnum="2052;"><font face="Arial">67.97</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
	</tr>
	<tr>
		<td height="20" align="center" valign=middle><font face="Arial">Liao et al. [14]</font></td>
		<td align="center" valign=middle><font face="Arial">TextBoxes++</font></td>
		<td align="center" valign=middle><font face="Arial">TIP</font></td>
		<td align="center" valign=middle sdval="2018" sdnum="2052;"><font face="Arial">2018</font></td>
		<td align="center" valign=middle sdval="64" sdnum="2052;"><font face="Arial">64</font></td>
		<td align="center" valign=middle sdval="84" sdnum="2052;"><font face="Arial">84</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" valign=middle sdval="93" sdnum="2052;"><font face="Arial">93</font></td>
		<td align="center" valign=middle sdval="92" sdnum="2052;"><font face="Arial">92</font></td>
		<td align="center" valign=middle sdval="85" sdnum="2052;"><font face="Arial">85</font></td>
		<td align="center" valign=middle sdval="96" sdnum="2052;"><font face="Arial">96</font></td>
		<td align="center" valign=middle sdval="95" sdnum="2052;"><font face="Arial">95</font></td>
		<td align="center" valign=middle sdval="87" sdnum="2052;"><font face="Arial">87</font></td>
		<td align="center" valign=middle sdval="73.3" sdnum="2052;"><font face="Arial">73.3</font></td>
		<td align="center" valign=middle sdval="65.9" sdnum="2052;"><font face="Arial">65.9</font></td>
		<td align="center" valign=middle sdval="51.9" sdnum="2052;"><font face="Arial">51.9</font></td>
		<td align="center" valign=middle sdval="76.5" sdnum="2052;"><font face="Arial">76.5</font></td>
		<td align="center" valign=middle sdval="69" sdnum="2052;"><font face="Arial">69</font></td>
		<td align="center" valign=middle sdval="54.4" sdnum="2052;"><font face="Arial">54.4</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
		<td align="center" sdnum="2052;0;@"><font face="Arial">~</font></td>
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

- [15] Wang,Kai, and S. Belongie. **Word Spotting in the Wild**. European Conference on Computer Vision(ECCV), 2010: 591-604.  [Paper](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.168.4897&rep=rep1&type=pdf)

- [16] S. M. Lucas, A. Panaretos, L. Sosa, A. Tang, S. Wong, R. Young,K. Ashida, H. Nagai, M. Okamoto, H. Yamamoto, H. Miyao,J. Zhu, W. Ou, C. Wolf, J. Jolion, L. Todoran, M. Worring, and X. Lin. **ICDAR 2003 robust reading competitions:entries, results,and future directions**. IJDAR, 7(2-3):105–122, 2005. [paper](https://link.springer.com/content/pdf/10.1007%2Fs10032-004-0134-3.pdf)

- [17] Shahab, A, Shafait, F, Dengel, A: **ICDAR 2011 robust reading competition challenge 2: Reading text in scene images**. In: ICDAR, 2011. [Paper](https://ieeexplore.ieee.org/document/6065556)

- [18] D. Karatzas, F. Shafait, S. Uchida, et al. **ICDAR 2013 robust reading competition**. In ICDAR, 2013. [Paper](https://ieeexplore.ieee.org/document/6628859)

- [19] D. Karatzas, L. Gomez-Bigorda, A. Nicolaou, S. K. Ghosh, A. D.Bagdanov, M. Iwamura, J. Matas, L. Neumann, V. R. Chandrasekhar, S. Lu, F. Shafait, S. Uchida, and E. Valveny. **ICDAR 2015 competition on robust reading**. In ICDAR, pages 1156–1160, 2015. [Paper](https://ieeexplore.ieee.org/document/7333942)

- [20] Chee C K, Chan C S. **Total-text: A comprehensive dataset for scene text detection and recognition**.Document Analysis and Recognition (ICDAR), 2017 14th IAPR International Conference on. IEEE, 2017, 1: 935-942.[Paper](https://arxiv.org/abs/1710.10400)


If you find any problems in our resources, or any good papers/codes we have missed, please inform us at    **liuchongyu1996@gmail.com**. Thank you for your contribution. 



### Copyright

Copyright © 2019 SCUT-DLVC. All Rights Reserved.

<p align="center">
    <img src="scut-dlvc.jpeg" alt="Sample"  width="150" height="75">
    <p align="center">
        <em></em>
    </p>
</p>

