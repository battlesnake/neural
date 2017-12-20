***NOTE*** CTAN isn't letting me update their copy of the package and I don't have time to waste chasing it.

** The CTAN version is *out of date. **

** The Github repository has the most up-to-date version. **


Title:
	Neural Network

Author:
	Mark K Cowan, mark@battlesnake.co.uk

Installation:
	The most up-to-date version of this package is available as a git repository:
		battlesnake/neural
		https://github.com/battlesnake/neural
		
	This package is also available on CTAN as `neuralnetwork`:
		/graphics/pgf/contrib/neuralnetwork
		http://www.ctan.org/tex-archive/graphics/pgf/contrib/neuralnetwork

Description:
	LaTeX package for drawing graphs, particularly neural network diagrams.

	% Diagram is created via the neuralnetwork environment
	\begin{neuralnetwork} [nodespacing=10mm, layerspacing=25mm,
			maintitleheight=2.5em, layertitleheight=2.5em,
			height=5, toprow=false, nodesize=17pt, style={},
			title={}, titlestyle={}]
		% nodespacing = vertical spacing between nodes
		% layerspacing = horizontal spacing between layers
		% maintitleheight = space reserved for main title
		% layertitleheight = space reserved for layer titles
		% height = max nodes in any one layer [REQUIRED]
		% toprow = top row in node space reserved for bias nodes
		% nodesize = size of nodes
		% style = style for internal "tikzpicture" environment
		% titlestyle = style for main title

		% To customize the text within nodes, define a macro like:
		\newcommand{\mynodetext}[2] {
			% layer=#1, node=#2
		}
		% The assign it:
		\setdefaultnodetext{\mynodetext}

		% To draw a layer (advanced):
		\layer[title={}, titlestyle={}, count=5,
				nodeclass={hidden neuron}, biaspos=top
				top=false, exclude={}, widetitle=false,
				bias={}]
		% title = layer title
		% titlestyle = style for layer title
		% count = nodes in this layer (excl. bias node)
		% nodeclass = class of node: 
		%		"neuron", which is base class for:
		%		"input neuron"
		%		"output neuron"
		%		"hidden neuron"
		% biaspos = position of bias node:
		%		"top" - immediately above other nodes
		%		"top row" - at the top of the node space, in
		%			the area reserved by setting parameter
		%			"toprow = true" on the "neuralnetwork"
		%			environment
		%		"center" - center of layer
		%		"center left" - left of "center"
		%		"center right" - right of "center"
		%		"center left left" - left of "center left"
		%		"center right right" - right of "center right"
		% top = layer is vertically aligned to the top, not the middle
		% exclude = one-based indices of nodes to avoid drawing
		% widetitle = allocate extra horizontal space for layer title
		% bias = true to add a bias node, false otherwise [REQUIRED]

		% To draw a layer (simpler):
		% "\layer" is wrapped up into some simpler macros, which can
		% accept the same parameters as "\layer"
		\inputlayer[count=16]	% bias=true, nodeclass={input neuron}
		\hiddenlayer[count=12]	% bias=true, nodeclass={hidden neuron}
		\linklayers
		\hiddenlayer[count=12]	% bias=true, nodeclass={hidden neuron}
		\linklayers
		\outputlayer[count=3]	% bias=false, nodeclass={output neuron}
		\linklayers

		% "\linklayers" links every node in the previous layer to the
		% layer before it.

		% To customize the text on the links, define a macro like:
		\newcommand{\mylinktext}[4] {
			% from layer=#1, from node=#2
			% to layer=#3, to node=#4
		}
		% Then assign it:
		\setdefaultlinklabel{\mylinktext}

		% To link the nodes of the previous two layers together:
		\linklayers[title={}, style={}, not from={}, not to={}]
		% title = title to put above the links (i.e. between layers)
		% style = passed to "style" param of "\link"
		% not from = one-based indices of nodes to NOT link from
		% not to = one-based indices of nodes to NOT link to

		% To draw a link from one node to another:
		\link[style={}, labelpos=midway, from layer, from node,
				to layer, to node]
		% style = style for the link path
		% labelpos = TikZ position of the label node along the path:
				"midway", "near end", "very near start",
				"at start", "pos=0.35", etc
		% from layer = layer to link from [REQUIRED]
		% from node = node to link from [REQUIRED]
		% to layer = layer to link to [REQUIRED]
		% to node = node to link to [REQUIRED]

	\end{neuralnetwork}
