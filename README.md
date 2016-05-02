# GeneticPy
Genetic solver written in Python

## Usage

    import genetic

    best = genetic.getBest(get_fitness, display, minLen, optimalFitness,
            geneSet=None, createGene=None, maxLen=None,
            customMutate=None, customCrossover=None)

### Output:

 an Individual with attributes:
 - Genes: list of genes
 - Fitness: fitness value for those genes
 - Strategy: strategy that produced the gene sequence (mutate, crossover, or random)

### Inputs:
 -  get_fitness: takes a list of genes and returns an integer value representing how close that particular candidate comes to the optimal solution.  Higher values are better.
 -  display: takes an Individual.  Called to provide visual output of better candidates as they are discovered.
 -  minLen: minimum valid length for an Individual's genes.
 -  maxLen: optional maximum valid length for an Individual's genes.  Defaults to minLen.
 -  optimalFitness: expected fitness value for the best solution.
 -  geneSet: optional list of gene values for generating new gene sequences.  If not provided, createGene must be provided.
 -  createGene: optional function to create a random gene.  Called with the gene sequence index into which it will be placed, and the length of that gene sequence.  If not provided, geneSet must be provided.
 -  customMutate: optional replacement for the built in mutate function.  Called with the new child genes.  Changes should be made to the child genes.
 -  customCrossover: optional replacement for the built in crossover function. Called with the new child genes, and a copy of a second parent's genes.  Changes should be made to the child genes.

## Sample projects (in order of genetic complexity)

 - stringDuplicationTests.py - duplicates a string, see [related blog post](https://handcraftsman.wordpress.com/2015/06/09/evolving-a-genetic-solver-in-python-part-1/)

 - 8queensTests.py - solves the 8 Queens Puzzle, see [related blog post](https://handcraftsman.wordpress.com/2015/06/20/evolving-a-genetic-solver-in-python-part-2/)

 - graphColoringTests.py - 4-coloring maps, see [related blog post](https://handcraftsman.wordpress.com/2015/06/21/four-coloring-a-graph-of-u-s-states-with-python-and-a-ga/)

## Obsolete samples

The following sample projects included in this repository work but no longer have a related blog post because I've changed my implementation approach.

 - equationGenerationTests.py - equation discovery

 - operationGenerationTests.py - generating OR and XOR with only AND and NOT

## e-book

The code and examples in ths repository work as is and you are welcome to use them.  In late 2015 I restarted from scratch with a slower feature progression to resolve some performance issues with more advanced genetic programming topics.  That has evolved into an e-book entitled [Genetic Algorithms with Python](https://leanpub.com/genetic_algorithms_with_python) that I'm writing on Leanpub.  Try the sample chapter.

## License

[MIT License](http://www.opensource.org/licenses/mit-license.php)
