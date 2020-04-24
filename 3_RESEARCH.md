---
layout: page
title: RESEARCH
---

Here are some of the projects in which I participate(d). For papers that resulted from some of them, see the tab [**PUBLICATIONS**](/2_PUBLICATIONS).

Rather than in a particular subject or model organism, I specialise in a set of research methods: [agent-based modelling](https://link.springer.com/content/pdf/10.1057/jos.2010.3.pdf) and computer analysis of vast volumes of data. My favourite field of research is the boundary of ecology and evolutionary biology.

---------------------------------------------------------------

#### <span style="color:#AC4142">ADVANCED COMPUTATIONAL APPROACHES FOR THE INTEGRATIVE STUDY OF VIROLOGICAL, EPIDEMIOLOGICAL AND SOCIO-DEMOGRAPHIC DRIVERS OF INFLUENZA</span>

The influenza virus is a small RNA virus that causes seasonal flu epidemics, e.g. in France they occur around winter. Flu may pose a risk of severe complications and even death in vulnerable individuals. Influenza vaccines exist, but due to the fast evolution of the virus, their efficiency is limited only to several similar strains of the virus. And the dominant strains change annually. The project (conceived by [Chiara Poletto](http://chiara-poletto.weebly.com/)) aims at understanding how population structure of France and travel patterns influence the dynamic of the epidemics and evolution of the influenza virus.

We use an agent-based and data-driven ([INSEE](https://www.insee.fr/fr/accueil) census) model simulating the spread of influenza in France developed before (by [Livio Bioglio](http://www.di.unito.it/~biogliol/)) and modified by us to record detailed information on who-infected-who. That allows for precise tracking of the epidemic demographics and the spread of the virus. We validate the model with the [Réseau Sentinelles’ (RS)](https://www.sentiweb.fr/france/fr/?page=maladies) disease surveillance data.

My job is to modify the original ABM model (written in C++11) to meet the project's needs, process the INSEE and RS data to feed them into the model, calibrate parameters using the data and analyse the output. There's a lot of Python scripting for automated data processing (including scripts choosing parameters and launching simulations on their own).

---------------------------------------------------------------

#### <span style="color:#AC4142">EVOLUTION OF THE COPY NUMBER VARIATION OF THE MAJOR HISTOCOMATIBILITY COMPLEX (MHC) GENES : THEORETICAL MODELLING</span>

The major [histocompatibility complex (MHC)](https://www.britannica.com/science/major-histocompatibility-complex) proteins are responsible for self-non-self recognition of molecules, thus play a crucial role in the defence against pathogens in all vertebrates. That triggers a co-evolution race between hosts and pathogens (the '[Red-Queen race](http://evolutionbiology.com/evolutionary-principles/red-queen-principle/)') what, as many believe, leads to the observed massive variation of the MHC genes, making them the most polymorphic gene family in vertebrates. Among humans, there are ~17,000 alleles known, but the human genome has only 6-7 loci to harbour MHC genes - it's a surprisingly low number! Some species, e.g. rodents like voles, passerine birds, fish called sticklebacks have their number of MHC loci varying between individuals. The model I coded investigates how the number of pathogens in the environment and sexual selection impact the individual copy number variation in species.

We were using prof [Jacek Radwan](http://evobio.home.amu.edu.pl/?team=prof-jacek-radwan) many years of experience researching the MHC genes to design an [agent-based model simulating MHC evolution in host-pathogen Red-Queen race](https://github.com/pbentkowski/MHC_Evolution). The model implements a simplified mechanism of binding of the pathogenic antigens by the MHC protein-binding region. We simulate each host and pathogen individual with its unique genome. MHC population diversity and individual copy number variations emerge as a result of hosts being selected for pathogen recognition abilities, thus avoiding infection. Also, we used this framework to test how different mating rules may impact MHC diversity if we add sexual selection among hosts.

My job was to participate in the model design, implemented it, run all the required simulations, analyse and interpret the results. The model is written in C++11 and it's designed to run on cluster computers. The analysis is done using Python scripts.

---------------------------------------------------------------

#### <span style="color:#AC4142">HOW DIFFERENT LEVELS OF ENVIRONMENTAL PERTURBATION IMPACT THE EVOLUTION OF GENOME SIZE AND ADAPTATION ABILITY IN PROKARYOTES : THEORETICAL MODELLING</span>

The size of the genomes of known free-living prokaryotes varies from ~1.3 mega base-pairs (Mbp) to ~13.0 Mbp, an order of magnitude. I proposed a possible [explanation of this variation due to the variability of the physical conditions of the environment](https://ueaeprints.uea.ac.uk/50553/). In a stable environment, competition for the resource becomes the main force of selection and smaller (thus energetically cheaper) genomes are favoured. In more variable conditions, larger genomes will dominate, as they have a wider range of response to a less predictable environment.

I devolpped an [agent-based model of genome evolution in a free-living prokaryotic population](https://github.com/pbentkowski/GenomeSizeEvolution). Using the classic Hutchinson niche space model, I defined a gene as a Gaussian function over a corresponding niche dimension. The single cell can have more than one gene along a given dimension, and the envelope of all the corresponding responses is considered a full description of a cell’s phenotype over that dimension. Gene deletion, gene duplication, and modifying mutations are permitted during reproduction, so the number of genes and their phenotypic effect (height and position of the Gaussian envelope) are free to evolve. The surface under the curve of a gene is fixed to prevent ‘supergenes’ from occurring. Change of the environmental conditions is simulated as a bounded random walk with a varying length of the step (a parameter representing the variability of the environment). By employing this approach I can reproduce the phenomenon of genome streamlining in more stable environments (analogical to, e.g. oligotrophic gyre regions of the ocean) and genome complexification in variable environments.

The model is written in C++ and Python is used to analyse the results. This was my Ph.D. thesis completed in [prof Thomas Mock's](http://mocklab.com/) laboratory of marine microbial genomics.

---------------------------------------------------------------

#### <span style="color:#AC4142">IMPACT OF PHARMACEUTICALS AND EXOGENIC HORMONES ON LAKE ZOOPLANKTON : LAB EXPERIMENTS IN ECOTOXICOLOGY</span>

The drugs used by humans also have a biological impact on other organism sharing similar biochemical pathways (due to shared evolutionary history). And we're releasing then into the environment. We tested how hormone melatonin (my M.Sc. project) impacts the diurnal migration and life-history traits of a freshwater crustacean Daphnia magna (water flea). I also took part in investigating how antidepressant drugs impact freshwater fish anti-predatory behaviour.
 
I took part in the design of the experiments and later set them up. I developed an experimental setup that allowed for [night time surveillance of animals using IR light](https://www.researchgate.net/publication/226083801_Role_of_melatonin_in_the_control_of_depth_distribution_of_Daphnia_magna) invisible to them. Part of my studies under prof [Joanna Pijanowska](http://www.hydro.biol.uw.edu.pl/en/joanna-pijanowska-prof-dr-hab.html).