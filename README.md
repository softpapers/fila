% !TEX TS-program = xelatex
%  For support, please attach all files needed for compiling as well as the log file, and specify your operating system, LaTeX version, and LaTeX editor.

%=================================================================
\documentclass[scifiniti,article,submit,moreauthors,twocolumn,twoside]{Definitions/scifiniti_jams} 

%----------
% submit
%----------
% The class option "submit" will be changed to "accept" by the Editorial Office when the paper is accepted. This will only make changes to the frontpage (e.g., the logo of the journal will get visible), the headings, and the copyright information. Also, line numbering will be removed. Journal info and pagination for accepted papers will also be assigned by the Editorial Office.

%=================================================================
% JAMS internal commands - do not modify
\firstpage{1} 
\makeatletter 
\setcounter{page}{\@firstpage} 
%\makeatother
%\pubvolume{1}
%\issuenum{1}
%\pubyear{2025}
%\datesubmitted{August 01, 2025} % Comment out if no revised date
%\dateaccepted{August 23, 2025} 
%\datepublished{September 14, 2025} 
\doinum{10.199.212/journal.0.0.1}
%\pdfoutput=1 % Uncommented for upload to arXiv.org

%=================================================================
% Add packages and commands here. The following packages are loaded in our class file: fontenc, inputenc, calc, indentfirst, fancyhdr, graphicx, epstopdf, lastpage, ifthen, float, amsmath, amssymb, lineno, setspace, enumitem, mathpazo, booktabs, titlesec, etoolbox, tabto, xcolor, colortbl, soul, multirow, microtype, tikz, totcount, changepage, attrib, upgreek, array, tabularx, pbox, ragged2e, tocloft, marginnote, marginfix, enotez, amsthm, natbib, hyperref, cleveref, scrextend, url, geometry, newfloat, caption, draftwatermark, seqsplit
% cleveref: load \crefname definitions after \begin{document}

%=================================================================
% Please use the following mathematics environments: Theorem, Lemma, Corollary, Proposition, Characterization, Property, Problem, Example, ExamplesandDefinitions, Hypothesis, Remark, Definition, Notation, Assumption
%% For proofs, please use the proof environment (the amsthm package is loaded by the JAMS class).

%=================================================================
% Full title of the paper (Capitalised)

\Title{
 First and Last Neighbours Ultracentrifugation Model
}

% Author Orchid ID: enter ID or remove command
\newcommand{\orcidauthorA}{0000-0000-0000-000X} % Add \orcidA{} behind the author's name
%\newcommand{\orcidauthorB}{0000-0000-0000-000X} % Add \orcidB{} behind the author's name

% Authors, for the paper (add full first names)
\Author{Amuda Adeolu\textsuperscript{\changeurlcolor{black}\href{mailto:amuda@sapafy.com}{\Letter}}\textsuperscript{1},Salmaan .B\textsuperscript{\changeurlcolor{black}\href{mailto:salmaan.b@sapafy.com}{\Letter}}\textsuperscript{2},Muhammad.B\textsuperscript{\changeurlcolor{black}\href{mailto:muhammad.b@sapafy.com}{\Letter}}\textsuperscript{4}
}

%\longauthorlist{yes}

% JAMS internal command: Authors, for metadata in PDF
\AuthorNames{Firstname Lastname, Firstname Lastname and Firstname Lastname}

% JAMS internal command: Authors, for citation in the left column
\ShortAuthorName{Author et al.}
% If this is a Chicago style journal: Lastname, Firstname, Firstname Lastname, and Firstname Lastname.


% Contact information of the corresponding author
\corres{Sapafy, affiliation, 
amuda@sapafy.com;\\
Tel.: +xx-xxx-xxx-xxxx}

%% Current address and/or shared authorship
%\firstnote{Current address: Affiliation.} % Current address should not be the same as any items in the Affiliation section.
%\secondnote{These authors contributed equally to this work.}
% The commands \thirdnote{} till \eighthnote{} are available for further notes

% Abstract (Do not insert blank lines, i.e. \\) 
\abstract{We introduce a fully unsupervised, from-scratch semantic information retrieval model with function calling capabilities named "FiLA" that achieves "deterministic" task-question-level semantic retrieval accuracy on an equivalent of ~ 222,000-page (of 896,000 documents, 128,278,452 tokens) corpus while operating within 4 GB working memory, and supporting instant incremental updates without supervision. This method departs from both classical sparse IR (BM25)\textsuperscript{\href{https://itenterprise.co.uk/how-does-googles-did-you-mean-algorithm-work/}1} and modern dense retrievers (learned sentence encoders + ANN)\textsuperscript{\href{https://itenterprise.co.uk/how-does-googles-did-you-mean-algorithm-work/}2} by paying attention to the Last Neighbours patterns through the Material Balancing of closest adjacent tokens, and the COEMA(Content Organisation Efficiency Mechanical Accuracy) ratings.}


% Keywords
\keyword{COEMA, Last Neighbours , BM25, ANN, sparse IR, in-memory, encoders, FiLA} 

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
\begin{document}

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

\section{Introduction}
Modern information retrieval systems face a fundamental trade-off between semantic understanding and computational efficiency. Dense retrieval methods based on transformer architectures [Karpukhin et al., 2020; Khattab \& Zaharia, 2020] achieve high accuracy but always require substantial computational resources and extensive pre-training. Traditional sparse methods like BM25 [Robertson \& Zaragoza, 2009] are equallly efficient but lack semantic understanding.

This paper introduces a paradigm that achieves both semantic accuracy and computational efficiency through material balancing alongside COEMA modelling. The core insight is that semantic relationships can be discovered through the material balance, and geometric properties of high-dimensional spaces without external supervision.

{We propose "First and Last Neighbours Ultracentrifugation Model! (FiLA)", a retrieval system that:}
\begin{enumerate}
\item Constructs semantic representations using material balancing and COEMA
\item Operates with sub-gigabyte memory requirements 
\item Achieves high semantic accuracy without supervision
\item Enables real-time adaptation to new documents and domains
\item Provides interpretable retrieval mechanisms
\end{enumerate}


\subsection{Our contributions are in fourfold:}

\begin{enumerate}
\item	Token Segmentation with  Law of Conservation of Energy: A material balance approach that divides a given token into three forms, namely: tail, left, and right segments which helps to determine the correctness of a given token.

\item	Last Neighbours Evaluation: A multi-level frequency-distance approach that determines the relativity and usefulness of every tokens of the trained data with a given query.

\item	Shortest Adjacental Distance: An approach that determines the true semantic nature of a given query by measuring the shortest adjacental distance alongside the COEMA(Content Organisation Machanical Accuracy) ratings of each document.

\item HippoCampus: A modelled brain-like structure that models new documents alongside unknown terms.
\end{enumerate}

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
\section{Related Work}

\subsection{Traditional Information Retrieval}

Classical IR methods rely on term-based matching using TF-IDF [Salton & McGill, 1986] or BM25 [Robertson & Zaragoza, 2009] scoring functions. While computationally efficient, these approaches struggle with semantic similarity, synonymy, and conceptual queries.

Probabilistic models like the Language Model approach [Ponte & Croft, 1998] and divergence-based methods [Lafferty & Zhai, 2001]\cite{ref-book1} improved ranking quality but remained fundamentally lexical.

Dimensionality reduction techniques including Latent Semantic Analysis (LSA) [Deerwester et al., 1990] and Latent Dirichlet Allocation (LDA) [Blei et al., 2003] attempted to capture latent semantic structures through matrix factorization and probabilistic topic modeling, respectively equally lack true semantic evaluation of a given text.

\subsection{Neural Information Retrieval}

The advent of neural methods transformed IR through learned representations. Distributed word embeddings from Word2Vec [Mikolov et al., 2013] and GloVe [Pennington et al., 2014] enabled semantic similarity computation.

Sentence-level methods like SIF [Arora et al., 2017] and Universal Sentence Encoder [Cer et al., 2018] extended semantic representation to longer texts. Recent dense retrieval approaches using BERT-based architectures [Reimers & Gurevych, 2019], DPR [Karpukhin et al., 2020], and ColBERT [Khattab & Zaharia, 2020] claims to have achieved state-of-the-art performance through extensive pre-training and fine-tuning, but truly doesn't comes near the real defintion of SOTA.

\subsection{Hyperdimensional Computing}

Hyperdimensional computing (HDC) [Kanerva, 2009; Rahimi et al., 2016] represents information in high-dimensional binary vectors, leveraging mathematical properties of high-dimensional spaces for robust computation. HDC has been applied to classification [Imani et al., 2019], associative memory [Neubert et al., 2019], and brain-computer interfaces [Rahimi et al., 2016] but not to large-scale information retrieval.

\subsection{Gap Analysis}

Existing methods present a false dichotomy: either sacrifice semantic understanding for efficiency (sparse methods) or require substantial resources and supervision (dense methods). No prior work achieves high semantic accuracy with extreme efficiency in a truly unsupervised setting.


%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
\section{Methodology}

\subsection{Token to Weights Conversion} 
Each token is converted to a 8-bit floating point value through TFP(Tokens to Floating Point), and it ensures no token is repeated twice for any datset.

\vspace{0.50cm}

\usetikzlibrary{arrows.meta, positioning, shadows}

\begin{document}
\begin{figure}[h]
\centering
\begin{tikzpicture}[
  node distance=4cm,
  box/.style={
    rectangle,
    draw=black,
    line width=0.8pt,
    minimum width=2.8cm,
    minimum height=1cm,
    font=\sffamily
  },
  arrow/.style={
    line width=0.7pt,
    -{Stealth[length=2.5mm, width=2mm]}
  },
  label/.style={
    font=\small\itshape
  }
]

% Nodes
\node[box] (andela) {Andela};
\node[box, right=of andela] (ball) {0.123456};

% Forward arrow (top)
\draw[arrow] ([yshift=3mm]andela.east) -- ([yshift=3mm]ball.west) 
  node[midway, above=2pt, label] {TFP};

% Reverse arrow (bottom)
\draw[arrow] ([yshift=-3mm]ball.west) -- ([yshift=-3mm]andela.east)
  node[midway, below=2pt, label] {FPT};

\end{tikzpicture}
\caption{Token to Weights Conversion}
\label{fig:token_to_weights_conversion}
\end{figure}

\vspace{0.50cm}

Each token is converted using
\begin{itemize}
    \item​ Post incremental: where the starting point is 0.00001 and increases by the same value.
    $$i_n = \sum_{k=0}^{n} 0.000001 = 0.000001(n + 1)$$

    \item​ Bijective BaseK of token to floating point value

$$n = \sum_{i=0}^{L-1} c_i \cdot 256^{L-1-i}$$

$$f = \frac{n}{256^L}$$
    \item​ Bijective BaseK of floating point value to token

$$n = \left\lfloor f \cdot 256^L \right\rfloor$$

$$c_i = \left\lfloor \frac{n}{256^{L-1-i}} \right\rfloor \bmod 256$$    
\end{itemize}

For example: "Andela" is assigned a floating point value of 0.000001, and "Andelan" is assigned with [0.000002] i.e {lastValue}+ 0.00001
\vspace{0.50cm}
Before Andela is discarded, we obtain the Bijective BaseK value where Andela is converted to it actual numerical value.

"Andela" BBK values = 0.25559070 and 0.25559070 is converted back to "Andela"

\subsection{Token Segmentation with  Law of Conservation of Energy} 
Energy is assumed to either not be created or destroyed, but should only be converted from one form to another or transferred between systems[2].

For example: When crude oil is fed into a reactor(input), it must return all the expected products(petroleum, diesel, gasoline,...) (output), and failure to have such returned is classified as "system accumulation/malfunctioning", and whatever goes into a system must come out, and if that doesn't happen, then the system is not working as expected.

Material Balance concept: ​ There must not be any accumulation of materials within a given feed(i.e., input) in a system. Whatever (feed or input) goes into a system must come out(i.e input must equal output), and if not, something is wrong.

1. Every data will have three material weight properties
\begin{itemize}
    \item​ fx → representing the head ASCII value 
    \item​ fy → representing the left material weight
    \item​ fz → representing the right material weight
\end{itemize}
​'innovation' for example would have(using the above Token to Weight conversion)
\begin{itemize}
   \item​ fx = 105 "i"
   \item​ fy = 64.100 "nov"
   \item​ fx = 48.641 "ati"
\end{itemize}   

\vspace{0.50cm}
\begin{figure}[h]
\centering
\begin{tikzpicture}[
  node distance=2cm,
  box/.style={
    rectangle,
    draw=black,
    line width=1pt,
    minimum width=3cm,
    minimum height=2cm,
    font=\sffamily
  },
  arrow/.style={
    line width=0.8pt,
    -{Stealth[length=2.5mm, width=2mm]}
  },
  label/.style={
    font=\small
  }
]

% Main reactor box
\node[box] (reactor) {Innovation\\(0.1213456)};

% Input arrow
\draw[arrow] ([xshift=-2cm]reactor.west) -- (reactor.west)
  node[midway, above, label] {Input};

% Output arrows
% Top
\draw[arrow] (reactor.north) -- ++(0,1.5cm)
  node[above, label] {nov (0.0001)};

% Bottom
\draw[arrow] (reactor.south) -- ++(0,-1.5cm)
  node[below, label] {ation (18.02)};

% Exit (right)
\draw[arrow] (reactor.east) -- ++(2cm,0)
  node[midway, above, label] {i (110)};

\end{tikzpicture}
\caption{Token Segmentation of "Innovation"}
\label{fig:reaction}
\end{figure}
A material balance approach that divides a given token into three forms, namely: head, left, and right segments. 

This ensures misspelt words are recognisable.
        
For example: When "ennoavtion" is provided, the same approach is applies

\begin{itemize}
    \item If the word "ennoavtion" does not exist in its memory, and that signifies the law of conservation of energy will be considered
    \item It extract the head value = "e"
    \item Left weight = "noa" (64.100)
    \item Right weight = "tio"  48.641
    \item Then compares(using Jarowinkler algorithm) all tokens with similar weights and provides a suggestion

\end{itemize}
For complete conversion with no accumulation, the mass balance requires 
$\sum \dot{m}_{\text{in}} = \sum \dot{m}_{\text{out}}$ and 
$\frac{dM}{dt} = 0$ at steady state.

\vspace{1cm}

In our example, the word "Innovation" alongside other tokens of the same pattern will be retrieved, and the tokens with the highest similarity threshold will be suggested

\subsection{Document to Multi-Dimensional Weights} 
It started by identifying the most common tokens[, > . ' \n] within a document.
Then proceed to tokenising the document and chunks the document into 10WPL(Ten Words Per Line) max, and 25LPP(25 Lines Per Page) maximum.

\vspace{1cm}

A given text of 

\vspace{1cm}
Title: Straight to Late

\vspace{1cm}

Document: 
"To be great, you need to be straight and to be straight in thinking, you need to work late, and to work late you must ensure no lateness with your goals."

\vspace{1cm}

Source: Straight-to-Late.com

\centering
\begin{tikzpicture}[
  node distance=2.5cm,
  keybox/.style={
    rectangle,
    draw=blue!70,
    line width=1.2pt,
    minimum width=2.5cm,
    minimum height=1cm,
    font=\ttfamily\Large,
    fill=blue!5,
    rounded corners=3pt,
    drop shadow
  },
  mapbox/.style={
    rectangle,
    draw=gray!60,
    line width=1.2pt,
    minimum width=6.5cm,
    minimum height=5cm,
    fill=gray!3,
    rounded corners=4pt,
    drop shadow
  },
  entry/.style={
    font=\ttfamily\normalsize,
    anchor=west
  },
  arrow/.style={
    line width=1.5pt,
    -{Stealth[length=4mm, width=3mm]},
    blue!70
  }
]

% Input key at top with label
\node[keybox] (key) {0.1234};
\node[above=0.2cm of key, font=\sffamily\small\bfseries, blue!70] {Title};

% Map container below
\node[mapbox, below=of key] (map) {};
\node[above=0.15cm of map.north, font=\sffamily\large\bfseries] {DocToWieghts};

% Map entries with better formatting
\node[entry] at ([xshift=0.4cm, yshift=1.8cm]map.west) (e1) {\textbf{1} $\rightarrow$ [\,1.2,\,3.4,\,5.6,\,7.8\,]};
\node[entry, below=0.5cm of e1] (e2) {\textbf{2} $\rightarrow$ [\,0.1,\,2.3,\,4.5\,]};
\node[entry, below=0.5cm of e2] (e3) {\textbf{5} $\rightarrow$ [\,9.8,\,7.6,\,5.4,\,3.2,\,1.0\,]};
\node[entry, below=0.5cm of e3] (e4) {\textbf{7} $\rightarrow$ [\,6.7,\,8.9\,]};
\node[entry, below=0.5cm of e4] (e5) {\textbf{...}};

% Vertical arrow pointing down
\draw[arrow] (key.south) -- (map.north) 
  node[midway, right=0.2cm, font=\sffamily\small\itshape] {D2W};

% Subtle grid lines for entries
\draw[gray!20, line width=0.5pt] 
  ([xshift=0.3cm]map.west) ++(0,1.3cm) -- ++(5.9cm,0);
\draw[gray!20, line width=0.5pt] 
  ([xshift=0.3cm]map.west) ++(0,0.8cm) -- ++(5.9cm,0);
\draw[gray!20, line width=0.5pt] 
  ([xshift=0.3cm]map.west) ++(0,0.3cm) -- ++(5.9cm,0);
\draw[gray!20, line width=0.5pt] 
  ([xshift=0.3cm]map.west) ++(0,-0.2cm) -- ++(5.9cm,0);

\end{tikzpicture}
\caption{Document to Weights conversion}
\label{fig:hash_mapping}

\begin{itemize}

\item Step 1: The title is split with a white space " ", converted to a floating-point value, and stored into the weights table.

\item "Straight to Late" [0.0002=straight[4.57868948],0.0003=
to[1.23455],000005=late[2.35556]]

\item Step 2: The title is assigned an  ownership index

   \item   owner 1: [4.578689481.234552.35556]

\item Step 3: The Actual sentence is converted to a set of mapped weights, and the source text is discarded afterwards

    \item owner1: 1: [0.0121.....0.12912]
   
\end{itemize}
\subsection{Last Neighbours Evaluation} An inverse document frequency approach that eliminates persistent tokens from a given query.
Each semantic atom $s_i$ maps to a sparse binary vector $\mathbf{v}_i \in \{0,1\}^d$ where $d \gg 10^4$ and $\|\mathbf{v}_i\|_0 = \sqrt{d}$, ensuring approximate orthogonality in high dimensions.

\subsection{Shortest Adjacental Distance} An approach that determines the true semantic nature of a given query by measuring the shortest adjacental distance of each documents COEMA(Content Organisation Machanical Accuracy).

For random binary vectors $\mathbf{u}, \mathbf{v} \in \{0,1\}^d$ with exactly $k = \sqrt{d}$ ones, the probability of approximate orthogonality is:

$$P\left(\left|\frac{\mathbf{u} \cdot \mathbf{v}}{k}\right| < \epsilon\right) \geq 1 - 2e^{-\epsilon^2 k/2}$$


\subsection{HippoCampus} A modelled brain-like structure that models new `documents alongside unknown terms

Bulleted lists look like this:
\begin{itemize}
\item	First bullet;
\item	Second bullet;
\item	Third bullet.
\end{itemize}
\subsubsection{Subsubsection}

Numbered lists can be added as follows:
\begin{enumerate}
\item	First item; 
\item	Second item;
\item	Third item.
\end{enumerate}

The text continues here. 

\subsection{Figures, Tables and Schemes}

All figures and tables should be cited in the main text as Figure~\ref{fig1}, Table~\ref{tab1}, etc.

\begin{figure}[H]
\caption{This is a ﬁgure, Schemes follow the same formatting.\\
If there are multiple panels, they should be listed as: (\textbf{a}) Description of what is contained in the ﬁrst panel. (\textbf{b}) Description of what is contained in the second panel. Figures should be placed in the main text near to the ﬁrst time they are cited. A caption on a single line should be centered.

\label{fig1}}
\includegraphics[width=4.5 cm]{Definitions/logo-scifiniti}
\end{figure}   

\begin{table}[H]
\caption{This is a table caption. Tables should be placed in the main text near to the ﬁrst time they are cited.\label{tab1}}
		\begin{tabular}{cccc}
			\toprule
			\textbf{Title 1}	& \textbf{Title 2}	& \textbf{Title 3}     & \textbf{Title 4}\\
			\midrule
\multirow[m]{3}{*}{Entry 1 *}	& Data			& Data			& Data\\
			  	                   & Data			& Data			& Data\\
			             	      & Data			& Data			& Data\\
                   \midrule
\multirow[m]{3}{*}{Entry 2}    & Data			& Data			& Data\\
			  	                  & Data			& Data			& Data\\
			             	     & Data			& Data			& Data\\
                   \midrule
\multirow[m]{3}{*}{Entry 3}    & Data			& Data			& Data\\
			  	                 & Data			& Data			& Data\\
			             	    & Data			& Data			& Data\\
			\bottomrule
		\end{tabular}\\
	\noindent{\footnotesize{* Tables may have a footer.}}
\end{table}

%\begin{table*}[htbp]
%\caption{This is a table caption. Tables should be placed in the main text near to the ﬁrst time they are cited.\\
%If there are multiple panels, they should be listed as: (a) Description of what is contained in the ﬁrst panel. (b) Description of what is contained in the second panel. Figures should be placed in the main text near to the ﬁrst time they are cited. A caption on a single line should be centered.\label{tab1}}
%		\begin{tabular}{cccc}
%			\toprule
%			\textbf{Title 1}	& \textbf{Title 2}	& \textbf{Title 3}     & \textbf{Title 4}\\
%			\midrule
%\multirow[m]{3}{*}{Entry 1 *}	& Data			& Data			& Data\\
%			  	                   & Data			& Data			& Data\\
%			             	      & Data			& Data			& Data\\
%                   \midrule
%\multirow[m]{3}{*}{Entry 2}    & Data			& Data			& Data\\
%			  	                  & Data			& Data			& Data\\
%			             	     & Data			& Data			& Data\\
%                   \midrule
%\multirow[m]{3}{*}{Entry 3}    & Data			& Data			& Data\\
%			  	                 & Data			& Data			& Data\\
%			             	    & Data			& Data			& Data\\
%                  \midrule
%\multirow[m]{3}{*}{Entry 4}   & Data			& Data			& Data\\
%			  	                 & Data			& Data			& Data\\
%			             	    & Data			& Data			& Data\\
%			\bottomrule
%		\end{tabular}\\
%	\noindent{\footnotesize{* Tables may have a footer.}}
%\end{table*}
%
%\begin{figure*}
%\caption{This is a ﬁgure, Schemes follow the same formatting.\\
%If there are multiple panels, they should be listed as: (a) Description of what is contained in the ﬁrst panel. (b) Description of what is contained in the second panel. Figures should be placed in the main text near to the ﬁrst time they are cited. A caption on a single line should be centered.\label{fig1}}
%\includegraphics[width=6.5 cm]{Definitions/logo-scifiniti}
%\end{figure*}   

%\begin{listing}[H]
%\caption{Title of the listing}
%\rule{\columnwidth}{1pt}
%\raggedright Text of the listing. In font size footnotesize, small, or normalsize. Preferred format: left aligned and single spaced. Preferred border format: top border line and bottom border line.
%\rule{\columnwidth}{1pt}
%\end{listing}


% Example of a page in landscape format (with table and table footnote).
%\startlandscape
%\begin{table}[H] %% Table in wide page
%\caption{This is a very wide table.\label{tab3}}
%	\begin{tabularx}{\textwidth}{CCCC}
%		\toprule
%		\textbf{Title 1}	& \textbf{Title 2}	& \textbf{Title 3}	& \textbf{Title 4}\\
%		\midrule
%		Entry 1		& Data			& Data			& This cell has some longer content that runs over two lines.\\
%		Entry 2		& Data			& Data			& Data\textsuperscript{1}\\
%		\bottomrule
%	\end{tabularx}
%	\begin{adjustwidth}{+\extralength}{0cm}
%		\noindent\footnotesize{\textsuperscript{1} This is a table footnote.}
%	\end{adjustwidth}
%\end{table}
%\finishlandscape


%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
\section{Discussion}

Authors should discuss the results and how they can be interpreted in perspective of previous studies and of the working hypotheses. The ﬁndings and their implications should be discussed in the broadest context possible. Future research directions may also be highlighted.

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
\section{Conclusions}

This section is not mandatory, but can be added to the manuscript if the discussion is unusually long or complex.

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
\section{List of abbreviations}

The content here.

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
%% Optional

\section{Notes}
\printendnotes[custom]

\section{Funding}

The content here.

\section{Acknowledgments}

The content here.

\section{Data and materials availability statement}

The content here.

\section{Declarations and conflicts of interest}

The content here.



%\appendixtitles{no} % Leave argument "no" if all appendix headings stay EMPTY (then no dot is printed after "Appendix A"). If the appendix sections contain a heading then change the argument to "yes".
%\appendixstart
%\appendix
%\section[\appendixname~\thesection]{}
%\subsection[\appendixname~\thesubsection]{}
%The appendix is an optional section that can contain details and data supplemental to the main text---for example, explanations of experimental details that would disrupt the flow of the main text but nonetheless remain crucial to understanding and reproducing the research shown; figures of replicates for experiments of which representative data are shown in the main text can be added here if brief, or as Supplementary Data. Mathematical proofs of results not central to the paper can be added as an appendix.
%
%\begin{table}[H] 
%\caption{This is a table caption.\label{tab5}}
%\newcolumntype{C}{>{\centering\arraybackslash}X}
%\begin{tabularx}{\textwidth}{CCC}
%\toprule
%\textbf{Title 1}	& \textbf{Title 2}	& \textbf{Title 3}\\
%\midrule
%Entry 1		& Data			& Data\\
%Entry 2		& Data			& Data\\
%\bottomrule
%\end{tabularx}
%\end{table}
%
%\section[\appendixname~\thesection]{}
%All appendix sections must be cited in the main text. In the appendices, Figures, Tables, etc. should be labeled, starting with ``A''---e.g., Figure A1, Figure A2, etc.



\reftitle{References}

% Please provide either the correct journal abbreviation (e.g. according to the “List of Title Word Abbreviations” http://www.issn.org/services/online-services/access-to-the-ltwa/) or the full name of the journal.
% Citations and References in Supplementary files are permitted provided that they also appear in the reference list here. 

%=====================================
% References, variant A: external bibliography
%=====================================
%\bibliography{your_external_BibTeX_file}

%=====================================
% References, variant B: internal bibliography
%=====================================
\begin{thebibliography}{999}
% Reference 1
\bibitem[Author1(year)]{ref-book1}
A. Author, ``Article Title," \emph{Journal} (abbreviated), vol., no., pp., Month (Abbrev.)., Year. doi:.
% Reference 2
\bibitem[Author2(year)]{ref-book2}
A. Author, \emph{Book Title}. Place: Publisher, Date of orig-inal publication. Available from Source [Link].
% Reference 3
\bibitem[Author3(year)]{ref-journal}
A. Author and B. Author of paper, “Title of paper,” in Title of Published Proceedings: Proceedings of the Title of Conf.: Subtitle of conference, Month Day, Year, Location, [Format]. Available from Data-base Name (if appropriate), doi:..
% Reference 4
\bibitem[Author4(year)]{ref-website}
A. A. Author, ``\emph{Title of Thesis: Subtitle}," Thesis type [Format]. Location of University: Abbrev. Univ., Year. Available from Database Name.
\end{thebibliography}

% If authors have biography, please use the format below
%\section*{Short Biography of Authors}
%\bio
%{\raisebox{-0.35cm}{\includegraphics[width=3.5cm,height=5.3cm,clip,keepaspectratio]{Definitions/author1.pdf}}}
%{\textbf{Firstname Lastname} Biography of first author}
%
%\bio
%{\raisebox{-0.35cm}{\includegraphics[width=3.5cm,height=5.3cm,clip,keepaspectratio]{Definitions/author2.jpg}}}
%{\textbf{Firstname Lastname} Biography of second author}


% To cite two works by the same author: \citeauthor{ref-journal-1a} (\citeyear{ref-journal-1a}, \citeyear{ref-journal-1b}). This produces: Whittaker (1967, 1975)
% To cite two works by the same author with specific pages: \citeauthor{ref-journal-3a} (\citeyear{ref-journal-3a}, p. 328; \citeyear{ref-journal-3b}, p.475). This produces: Wong (1999, p. 328; 2000, p. 475)

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
%% for journal Sci
%\reviewreports{\\
%Reviewer 1 comments and authors’ response\\
%Reviewer 2 comments and authors’ response\\
%Reviewer 3 comments and authors’ response
%}
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
\end{document}


![Document Preview](abc.png)
