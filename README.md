# ForwardQuestions Dataset
## Content of the directories and files
- `mapping.json` : this file contains a mapping between DBPedia predicates and Wikidata predicates. The key is the DBPedia predicate and the value represents the code that corresponds to the Wikidata equivalent predicate. A part of them are were already mapped and are available through a SparQL requests, but all the predicates from `"nationality": "P495"` were manually mapped.
- `questions` : this directory contains several files with questions that were automatically generated on a specific topic. The name of each file is the topic of the questions. All the questions were generated from templates build from questions sets that were provided by SimpleQuestionsWikidata (https://github.com/askplatypus/wikidata-simplequestions) and SimpleDBPediaQA (https://github.com/castorini/SimpleDBpediaQA).
- `all_questions` : this file contains a collection of the distinct questions from both SimpleQuestionsWikidata and SimpleDBPediaQA. Each entry contains:
	- The question as proposed in the original file
	- The question with its subject replaced by a placeholder
	- The extracted subject of the question
	- The Wikidata code of the subject as proposed in the original file or mapped from the DBPedia subject
	- The extracted predicate of the question
	- The Wikidata code of the predicate as proposed in the original file or mapped from the DBPedia predicate
	- The extracted object of the question (if the question come from the SimpleQuestionsWikidata set, as the object of the question is not specified in the SimpleDBPediaQA set)
	- The Wikidata code of the object as proposed in the original file (if the question come from the SimpleQuestionsWikidata set)
- `predicates_distribution.pdf` : this file contains all the different predicates that can be found in the dataset, ordered by frequency
