# Keyword annotation task

## Purpose

Picture yourself as the author of a scientific paper. In academic writing, it is essential to support the claims you make, either with evidence or by citing other scientific articles that have already been published. The purpose of this annotation exercise is to research what _keywords_ found in the text of a draft academic paper are more helpful for finding the most appropriate references from an existing collection of documents, using a search engine.

You will be provided with a number of _citation contexts,_ which are paragraphs of text extracted from scientific articles. These paragraphs originally had citations to other articles in them, which for the purposes of this annotation have been replaced with placeholders. These placeholders are of two types:

- --**[CITATION HERE]** the citation we are interested in finding, based on the text around it
- --**[other cit]**: another citation that was present in the original text but which we do not concern ourselves with.

You will also see other placeholders that read **\_\_author**. In this location, the name of the author of a paper has been anonymised and you should ignore this token. Keep in mind that several **\_\_author** tokens in one context can refer to different author names, or to the same one: this is not known.

## Task

The task can be summarised as: if, using a search engine (e.g. Google Scholar), you are trying to find the original paper cited where [CITATION HERE] appears, which words from the text would you select?

Think only of the document contents: _which words in the citation&#39;s context are likely to appear in the cited paper?_

We are exploring documents in two different domains: computational linguistics (labeled **AAC** ) and biomedical science (labeled **PMC** ). These domains have their important differences, which you should be aware of, so to familiarise yourself with these, please skim read through both files first.

You will receive one file to annotate for each domain, and each contains a total of 100 different paragraphs (citation contexts) to annotate: **keywords\_aac.txt** and **keywords\_pmc.txt**.

Please save these files as **keywords\_aac\_annotated.txt** and **keywords\_pmc\_annotated.txt** and save your changes in them, as documented below.

## Examples

Each file contains 100 _contexts_. Here is one example context from the AAC set that you will not need to annotate and is only provided for illustration. Please avoid modifying the text on the lines that start with #ID, #NUM, and #WORDS.

Simply copy the words or span of text from the line starting with #WORDS and paste them after #KEYWORDS: leaving a space between &quot;#KEYWORDS&quot; and the text you paste. Please make sure to only copy and paste full words, not parts of them.

| **#ID:** 06d161b0-c1b2-471a-80e4-7995137b40eb\_cit12 **#NUM:** 84  **#WORDS:** This type of error is caused by improper handling of relation phrases that are expressed by a combination of a verb with a noun, such as light verb constructions ( LVCs ). An LVC is a multi-word expression composed of a verb and a noun, with the noun carrying the semantic content of the predicate **[CITATION HERE]**. Table 2 illustrates the wide range of relations expressed this way, which are not captured by existing open extractors.  **#KEYWORDS:**  **\&lt;insert keywords here\&gt;** |
| --- |

In this example, without knowing anything about the subject matter or which paper was cited, we can glean that the citation that is missing where [CITATION HERE] appears is related to &quot;light verb constructions&quot;.

One example of a full set of keywords we could extract to reflect this would be: &quot;light verb constructions LVCs LVC multi-word expression verb noun semantic content predicate&quot;. Note that we select both &quot;LVCs&quot; and &quot;LVC&quot;, as these are different words. The word &quot;noun&quot; appears twice, but selecting it once is sufficient. We can also select it several times, as this does not matter. We would simply copy and paste this list of words after #KEYWORDS:

**#KEYWORDS:** light verb constructions LVCs LVC multi-word expression verb noun semantic content predicate

Another way to do this is to simply copy and paste the whole relevant span of text, for example:

**#KEYWORDS:** light verb constructions ( LVCs ). An LVC is a multi-word expression, verb and a noun, with the noun carrying the semantic content of the predicate

See how we have omitted the span of text &quot;_composed of a_&quot; and copied and pasted what came before and after that. Note that this is merely an example of what we could annotate, and not an authoritative annotation. For example, we may decide that the words &quot;relation phrases&quot; found earlier in the text are also relevant to the citation. What exactly to include is up to you to decide as the annotator.

The AAC and PMC domains differ substantially in vocabulary and style, as can be seen in this example from PMC (again, not appearing in the corpus to annotate):

| **#ID:** 3244bfe6-9f77-4628-9cdf-24e446405183\_cit36 **#NUM:** 203 **#WORDS:** As for HAM/TSP, there were many reports dealing with HAM/TSP treatment, although they included a limited number of patients and need further studies. Such examples are listed : safety and efficacy of a humanized monoclonal anti-IL15Rβ antibody ( CD122 ) \_\_author **[other cit]** potential use of BNZ-gamma peptide ( selectively blocking binding and downstream signaling of IL-2, IL-9 and IL-15 ) as a new drug \_\_author **[other cit]** clinical study using Infliximab ( anti-TNF-α monoclonal antibody ) \_\_author **[CITATION HERE]** efficacy of Methotrexate \_\_author **[other cit]** and efficacy of Fampridine ( a selective neuronal potassium channel blocker ) \_\_author **[other cit]**. One of the problems in these reports is the lack of standard criteria for treatment efficacy, which makes it difficult to compare the results from the different clinical research teams. **#KEYWORDS:**   |
| --- |

Here we see a number of papers cited, all around the same theme: &quot;HAM/TSP treatment&quot;. The citation we are interested in seems to be about &quot;Infliximab&quot;, so one potential set of keywords to extract would be:

**#KEYWORDS:** HAM/TSP treatment clinical study using Infliximab ( anti-TNF-α monoclonal antibody )

## Instructions

- It is recommended that you first skim read through each of the two files before starting the annotation task, to familiarise yourself with each textual domain and acquire an awareness of the differences between them.
- For each citation context (paragraph):
  - **INCLUDE** : all the words as you think are likely to be present in the paper that was originally cited.
  - **EXCLUDE:** words that you think are unrelated to the missing citation and unlikely to appear in that paper, and therefore would add less relevant search results.
  - **WHEN IN DOUBT:** err on the side of selecting **more** keywords rather than fewer **.**
- For consistency, please make sure to copy/paste from the text rather than type. Only copy full words, not parts of them. In the cases where words are hyphenated, e.g. &quot;_multi-word_&quot; in the example above, or &quot;_anti-TNF-α_&quot; in the PMC text, count this as a single word and copy it including the hyphen.
- For ease of annotation, feel free to copy/paste any length of text directly from #WORDS , with or without punctuation in it. Stopwords (grammar words) such as &quot;for&quot;, &quot;and&quot; and &quot;to&quot; will be automatically filtered out later on, as well as all punctuation such as commas, parentheses and full stops, so you need not worry about including them or not.
- All the keywords you select will be used as part of a single query.  Don&#39;t be afraid to select a larger query: the more specific the query, the more likely it will be to find the originally cited paper. But keep in mind the rules above and avoid including what you think is not relevant.
- Keywords only count once: there is no harm in adding a single word several times, but it will not count more than once either.
- Be aware of editorial conventions: in the PMC corpus, when you see _&quot;, [CITATION HERE]&quot;_, the citation refers to the text that precedes the comma.
- Pay attention to the function of the citation. Sometimes a citation backs up a specific claim, for example:

_&quot;The authors studied whether CMR improves outcomes prediction after contemporaneous echocardiography in a prospective study of 444 patients clinically referred for CMR_ **[CITATION HERE]**_.&quot;_

-
  - Here, it is likely that the full span of text &quot;CMR improves outcomes prediction after contemporaneous echocardiography in a prospective study of 444 patients clinically referred for CMR&quot; is relevant to finding the originally cited paper
  - Citing expressions like &quot;The authors studied&quot; or &quot;According to a study by&quot; should never be included as keywords to extract.
- Other times, a citation simply acknowledges work that has defined or popularised a technique or approach, for example:

_&quot;The raw sentences in all the training and test documents were preprocessed using MXPOST_ **[CITATION HERE]** _and the MST dependency parser_ **[other cit]** _following \_\_author et al. ( 2010a ).&quot;_

-
  - Here, the only intuitively relevant part of text seems to be the unique name &quot;MXPOST&quot; which refers to a particular system that the cited paper presents and describes. This paper will be very uniquely identifiable in the whole collection just through this one word.

_&quot;The raw sentences in all the training and test documents were preprocessed using MXPOST_ **[other cit]** _and the MST dependency parser_ **[CITATION HERE]** _following \_\_author et al. ( 2010a ).&quot;_

-
  - For this other citation, we have a similar situation where &quot;MST dependency parser&quot; seems to be the only relevant part of the text to extract. But again, this is only an example and not authoritative. What to ultimately extract is your decision.
- Once you have chosen the keywords, please have a _second read_ of the paragraph and the keywords you selected! It is easy to miss out on relevant content.