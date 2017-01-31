## Contents

- [Image data](#image)
- [Natural language processing](#nlp)
- [Genetic data](#genetic)
- [Geospatial & volumetric data](#geo)
- [Time series data](#time)
- [Interface design](#interface)
- [Non-independent data](#nonindependent)
- [Graphs and graph databases](#graphs)

<a name="image"></a>

## Image data

_names removed_

Questions / discussion goals: 

- What are the mechanisms involved between sparse and non-sparse imaging data? X 2
- Simulated images?

Multidimensional image analysis:

- There are multiple people doing research on our data sources, but do we store sparsely to alleviate storage requirements? X says his lab and astronomers in general keep the raw images for other analysis. Y stores a sparse representation and occasionally throws out the rest. His data has some localized areas of interest, so they feel comfortable doing so mostly to improve processing time.

Regarding X's work, there are stars of fixed brightness that allow calibration.

- Simulated image data:
	We need to know that our simulated images contain similar features to that of our real data. One idea is a non-parametric way of measuring moments to confirm that our simulated images are similar. Another discussion point was methods for finding features unique to either set of data. Lastly, we discussed the use of adversarial models -- similar to the Generative Adversarial Network (GAN) approach.

Deep Learning for Scientific Images:

- Neural network architectures in computer vision conferences are focused on natural images, often with a single object of interest. This differs from our research, where we’re dealing with scientific images.

<a name="nlp"></a>

## Natural language processing

Tools:

- Information extraction from unstructured data: http://hazyresearch.github.io/snorkel/
	- Jupyter notebook interface, written in Python
	- UI mostly around loading the data
	- Visual interface that requires you to label data initially, noisy labeling to create a larger training set
	- Uses core NLP functions
	- Can potentially be used to identify event data in text, better than GDELT
- Event Registry can also be used to identify relative dates in text-based data: http://eventregistry.org/ 
W- ord Mover’s Distance (WMD) as a way of measure the similarities between two texts (link is pdf). See also here for more information on WMD.
- Distributed Gradient Boosting - deep learning for classification. Has won many Kaggle competitions.

Papers:

- Predicting socio-economic indicators using news events. Co-written by DDD scholar Sunandan Chakraborty
- SourceSeer: Forecasting Rare Disease Outbreaks Using Multiple Data Sources. Co-written by DDD scholar Theo Rekatsinas

Datasets: 

- Signal Media: http://research.signalmedia.co/datasets.html
- Event Registry: http://eventregistry.org/ 

Research Puzzles:

- How do social movements spread from newspaper data: Black Lives Matter and Occupy Wallstreet
	- Question: how do you identify size of event? Snorkel can maybe do this.
- How are politician’s tweets covered in the media? Text analysis problem: find mentions of the tweet from a news corpus. WMD can maybe do this.
- Identifying conceptually fuzzy categories in text, such as texts that discuss inequality versus those that discuss relative economic groups that are not unequal.
	- Try Distributed Gradient Boosting
	- Similar to random forest but different optimization.
- Predict where the next disease outbreak will be based on discussion of disease in tweets, blogs, and news articles.
- Puzzles: 
	- for some diseases outbreaks are very rare
	- National newspapers are accurate but not timely, local newspapers are timely but not accurate
	- How to find accurate, local newspapers that are more timely
	- Can get accurate prediction at the country level, was able to get city level
- Paper: http://linqs.cs.umd.edu/basilic/web/Publications/2015/rekatsinas:sdm15/


<a name="genetic"></a>

## Genetic data

- Half of the people are from genetic/biology side
- Half of the people are from CS/Machine learning/statistics side

Topics:

- Benchmarking/comparing the tools
	- Not enough attention is paid currently
	- Benchmarking the tools can be difficult and biased
	- Requires more than one labs
- Have to know how the data is generated 
	- visiting a wet lab
	- Adaptive data visualization can help to understand the genetic data
	- Online tools like DNAnexus/galaxy can help to share the data processing pipeline
- Validation of analysis results
	- Code review
	- Simulations
	- Wet lab experiment
- Best practice
	- Have to understand and validate every step of the pipeline
	- Quality control of the data in every step of the pipeline
	- Accompanied with every paper, there should be not just the raw data but also the pipeline (possibly temporary data in every step) 
- The pipeline sharing platforms are we using
	- cyverse
	- galaxy
	- DNAnexus
	- snakemake
	- [script of scripts](http://vatlab.github.io/SOS/doc/tutorials/Using_SoS_with_Jupyter_Notebook.html)

<a name="geo"></a>

## Geospatial and volumetric data

Introduction round

- Adaptive meshes
- Particle data / LiDAR

Problems / Challenges

- Heterogeneous data formats presenting a barrier of entry
- Supporting data of all possible sizes (out-of-core rendering)
- Finding interesting aspects of the data

Organization of data

- Octree
- KD tree
- Efficient indexing (morton indices)
- Streaming datasets
- Efficient rendering:  Falk, Martin: Visualization and mesoscopic simulation in systems biology. Diss., Visualization Research Center, Universität Stuttgart, 2013

Modelling for topological analysis

Softwares / frameworks

- Yt
- Urbane
- Custom software
- OpenSpace
- Inviwo
- D3
- Paraview / Visit
- VisTrails
- Blender / Houdini
- Unity

Graphical User Interface

- Qt
- ImGui

Virtual Reality

- OpenVR
- PyOpenVR
- Oculus & HTC Vive & ...

Astronomical datasets

- Sparse point cloud data
- Multi-variate

Urban datasets

- Taxi datasets
- Efficient database access in specialized databases

<a name="time"></a>

## Time series data

- Economists-mostly cross sectional or panel data
- Fluid dynamics (ie pressure sensor to control flow, control theory problems, or vaccination rates). Mostly method development
- Astronomy--”no hope of influencing anything ever” measuring brightness over time. Detect period lengths that will tell you about underlying physical process. Works with ARMA.
- Two time series at different wavelengths
- Difficulty: data are not regularly sampled (telescope not available, bad weather, etc.) 
- Natural Language Processing--reduce communication to a time series. Non linear time series to deal with non-stationarity issues. Windowed cross correlation. Cross recurrence quantification analysis. Growth curve analysis.
- Measuring sound at different frequency. Pitch/rhythm/song/playlist Bayesian models for sequence prediction. 
- fMRI time series data of voxel and stimulus (story or music). Linearized models. All voxels analyzed independently. MVPA analyzes the voxels in a volumetric region of interest around a center together. “Smoothing the data makes your conclusions wrong” (though it hits the news a lot) 1 image of entire brain every 2 seconds.

- Periodicity in human behavior (humans in conversation maybe sync up?) So how do we identify periodicity--do a fourier transform and look for spikes. Problems: that works if you have a constant background, and if the noise is additive. Counting occurrences, so use Poisson statistics. 

- Scale transform, like fourier transform after doing resampling on an exponential grid. Used on rhythm, could be used elsewhere.

Software:

- Tetraflow, audio (Librosa Python library)
- R (CRQA, lme4)
- Python Fourier transform from SciPy, new library Stingray
- Nltk, spacy, python NLP toolkits
- For Gaussian processes--George
- Matlab & Fortran & Stata: because our collaborators do it.

Ridge regression with bootstrapping for regularization parameters


<a name="interface"></a>

## Interface design

- Useful paper: Cognitive Dimensions of Notation
	- Introducing dependencies?
	- viscosity 
	- Theoretical framework to evaluate design decisions
- Figuring out how to strike a balance
	- Low threshold / high ceiling 
- GitHub’s interface
	- Doesn’t work as well across organizations
	- Single-level hierarchy doesn’t scale well (org/repo)
- Project management tools:
	- Waffle.io (view on issues), trello, github’s projects
	- Integrating project management into open source is hard
- Dependency hell, the stack is an interface
- API design, how to make programming more learnable, e.g. Andy Ko at UW
	- Declarative models, more decoupled 
	- Visualization recommenders, viz recommenders
- For repro, you want a wysiwyg interface to generate code. That does mechanical repro, but not the kind of repro where you can understand and replicate
- Lyra: wysywig viz
	- Area of study: best ways to facilitate domain experts producing efficient visualizations
- Crowd annotation for labeling for machine learning, with auditing for untrusted input
- The fast pace of new languages/libraries/APIs can be hard for learners and domain scientists
- Danger in thinking the GUI perfectly abstracts

<a name="nonindependent"></a>

## Non-independent data

Examples:

- Ecological systems, hydrological systems: humidity, precipitation, water flow
One thing drives another, hidden variables, two-way interactions

Radio astronomy: measurements in a sparse Fourier Space mean lots of correlated
data and error bars

Spatial, tabular data -- help people access data / make it publically available

- Data sets described by json formats, download it into databases
	Be able to combine separate tables by joining along columns

Environment in space and time

- Estimates from remote sensing weather stations
- Human observers identify species 
- Species interact with eachother & environment non-linearly
- Human observers vary in their abilities/biases

Talked about how to improve monte carlo simulations to explore high dimensional spaces

- Gibb’s sampling, hamiltonian monte carlo
- Non-linearites makes Gibb’s sampling hard

<a name="graphs"></a>

## Graphs and graph databases

**Neo4j -- makes graph queries much**

- Doing graph queries in SQL is unpleasant
- Using JSON, having to write your own programs is often necessary and not ideal, and sometimes not practical
- Neo4j, a database, has “cipher” a querying language run on neo4j
- That makes querying graphs much easier
- Neo4j queries allow for querying “find node such that all its neighbors have property X” or “find all nodes such that that node has at least one neighbor with property X”
- D Himmelstein’s database:
	- Millions of relationships among tens of thousands of nodes
	- Example: want to find paths inside the database such that one end point has label A, the other endpoint has label B, and you’re querying the database to find such kinds of paths.
- “Owl”, “triple store”, “rdf”
	- An object, relates somehow, to a predicate
	- These three components constitute an element of the database
	- This layout doesn’t force the database to have any graph structure, the format of a triple doesn’t lend itself to node-edge structure
- Orgango DB and Orient DB
- Use one database as a document store, without any graph structure,
- And then at the same time use that same database to also impose a graph structure for separate purposes
- Neo4j -- can work with databases that are so big that they don’t entirely fit on one computer.
- Relational databases

**Graph visualization**

- What to do for visualizing graph layouts
- Graph viz -- pay all the cost upfront, run it for hours, then read that in to another viewer that does no layout work at all, purely rendering
- Hive-plot -- nodes in a line coming  off of an origin point
	- different axes of nodes
	- Don’t work well when the nodes don’t connect themselves or you have too many different kinds of nodes
	- A very cool tool for a precise set of circumstances
- What about some kind of down sampling for your graph?
- “circos”
	- Plotting nodes in a circle around the outside
	- Relationships drawn inbetween
- Gephy
- Cite escape

**typesetting**

- Latex. Or, write in markdown, use pan-doc to convert to latex
- DOI to bibtex converter tool?
- Pan-doc is the starting place -- a document swiss army knife
- One of the ideas here is separating the content from the format of your work -- latex contains both, but in this system you can write just the content in a simple way (in markdown), and then port it to different media (blog post, academic paper, chapter of book or thesis) by compiling using different formatting tools
