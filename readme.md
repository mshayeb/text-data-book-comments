# Text Data Analysis and Management: A Practical Introduction to Text Mining and Information Retrieval

[ChengXiang Zhai](http://web.engr.illinois.edu/~czhai/) and [Sean
Massung](http://web.engr.illinois.edu/~massung1/), [UIUC Computer Science Department](http://cs.illinois.edu/)

## This GitHub Page

This page has been created for two purposes:

### Hold links to draft chapters

Once a draft chapter is completed, we will link to it in the chapter
titles and descriptions below. All are welcome to watch the book as it
progresses.

### Receive feedback from readers

We'd like to hear your comments, fix errors you spot, listen to your
suggestions, and address issues you find with our book. We will keep track of
your comments via [GitHub
issues](https://github.com/smassung/text-data-book-comments/issues) on this
page.

On the right side of this page, click the Issues link. It will take you to a
screen where you can open a new issue or comment on existing issues. If creating
a new issue, you can select one or more of the following labels for it:

 - Typo: a typing error in the book text such as "infromation retreival"
 - Error: a factual error such as "NDCG only operates on binary relevance
   values"
 - Comment: a general comment about part of the book, such as "I really like the
   chapter on X"
 - Suggestion: such as, "could you expand a little more on the Rocchio feedback
   method?"

We will add more issue labels if necessary. Thanks for your help in creating
this book!

## Introduction

Recent years have seen a dramatic growth of natural language text data,
including web pages, news articles, scientific literature, emails, enterprise
documents, and social media such as blog articles, forum posts, product reviews,
and tweets. This has led to an increasing demand for powerful software tools to
help people analyze and manage vast amounts of text data effectively and
efficiently. Unlike data generated by a computer system or sensors, text data
are usually generated directly by humans, and are accompanied by semantically
rich content. As such, text data are especially valuable for discovering
knowledge about human opinions and preferences, in addition to many other kinds
of knowledge that we encode in text. In contrast to structured data, which
conform to well-defined schemas (thus are relatively easy for computers to
handle), text has less explicit structure, requiring computer processing toward
understanding of the content encoded in text. The current technology of natural
language processing has not yet reached a point to enable a computer to
precisely understand natural language text, but a wide range of statistical and
heuristic approaches to analysis and management of text data have been developed
over the past few decades. They are usually very robust and can be applied to
analyze and manage text data in any natural language, and about any topic.

This book provides a systematic introduction to all these approaches, with an
emphasis on covering the most useful knowledge and skills required to build a
variety of practically useful text information systems. The focus is on text
mining applications that can help users analyze patterns in text data to extract
and reveal useful knowledge. Information retrieval systems, including search
engines and recommender systems, are also covered as supporting technology for
text mining applications. The book covers the major concepts, techniques, and
ideas in text data mining and information retrieval from a practical viewpoint,
and includes many hands-on exercises designed with a companion software toolkit
(i.e., [MeTA](http://meta-toolkit.github.io/meta/)) to help readers learn how to
apply techniques of text mining and information retrieval to real-world text
data and how to experiment with and improve some of the algorithms for
interesting application tasks. The book can be used as a textbook for a computer
science undergraduate course or a reference book for practitioners working on
relevant problems in analyzing and managing text data.

## Part I: Overview and Background

This part provides an overview of the motivation and high-level concepts of the
book, and gives readers a roadmap for navigating through the chapters in the
later parts. It also includes a background chapter where basic concepts in
probability and statistics and natural language processing are introduced so
that readers without any knowledge in these areas will have the necessary
background to understand the materials later. This part further includes one
chapter on the [MeTA](http://meta-toolkit.github.io/meta/) toolkit, which will
be the basis for many exercises later. We use this chapter to introduce the
typical architecture of a text mining system, where the search engines will be
shown as a basis for supporting text analysis. Readers with sufficient
background knowledge about these topics can skip part or all of this section.

 - [Introduction](http://sifaka.cs.uiuc.edu/ir/textdatabook/chapters/text-data-book-draft-chapter01-Intro.pdf) (Draft from 4 April 2015)
   * Text data *vs* structured data
   * Functions of text information systems
   * Conceptual framework for text information systems
   * How to use this book

 - [Background](http://sifaka.cs.uiuc.edu/ir/textdatabook/chapters/text-data-book-draft-chapter02-Background.pdf) (Draft from 2 May 2015)
   * Basics of probability and statistics
   * Basics of natural language processing
   * Statistical language models
   * Exercises

 - [MeTA: A Modern Data Sciences
   Toolkit](http://sifaka.cs.uiuc.edu/ir/textdatabook/chapters/text-data-book-draft-chapter03-MeTA.pdf) (Draft from 8 April 2015)
   * Design philosophy
   * Setting up MeTA
   * Architecture
   * Tokenization with MeTA
   * Exercises

## Part II: Text Data Access

Text data access is the foundation for text analysis. Text access technology
plays two important roles in text analysis and management applications. First,
it enables retrieval of the most relevant text data to a particular analysis
problem, thus avoiding unnecessary overhead from processing a large amount of
non-relevant data. Second, it enables interpretation of any analysis results or
discovered knowledge in appropriate context and provides data provenance. The
general goal of text data access is to connect users with the right information
at the right time. This connection can be done in two ways: *pull*, where the
users take the initiative to fetch relevant information out from the system, and
*push*, where the system takes the initiative to offer relevant information to
users. The main technology supporting *pull* is search engines which are covered
in detail in one long chapter. The main technology supporting *push* is
recommender systems, covered in a later chapter.

 - [Overview of Text Data
   Access](http://sifaka.cs.uiuc.edu/ir/textdatabook/chapters/text-data-book-draft-chapter04-Access.pdf) (Draft from 19 April 2015. *This short chapter will most likely be merged into another chapter*)
   * Access mode: pull *vs* push
   * Multimode interactive access
   * Exercises

 - Text Retrieval
   * Overview
   * Text retrieval *vs* database retrieval
   * Document selection *vs* document ranking
   * Vector space models
   * Probabilistic retrieval models
   * Feedback
   * Exercises

 - [Search Engine
   Implementation](http://sifaka.cs.uiuc.edu/ir/textdatabook/chapters/text-data-book-draft-chapter06-Search-Engine-Implementation.pdf)
   (Draft from 15 May 2015)
   * Tokenizer
   * Indexer
   * Scorer
   * Feedback
   * Compression
   * Caching
   * Exercises

 - Search Engine Evaluation
   * Overview
   * Cranfield evaluation methodology
   * Evaluation of set retrieval
   * Evaluation of a ranked list
   * Evaluation with multi-level judgements
   * Practical issues in evaluation
   * Exercises

 - Web Search Engines
   * Overview
   * Web crawling
   * Web indexing
   * Link analysis
   * Learning to rank
   * Other Web search techniques
   * Exercises

 - Recommender Systems
   * Content-based recommendation
   * Collaborative filtering
   * Hybrid recommender systems
   * Evaluation
   * Applications
   * Exercises

## Part III: Text Data Analysis

This part covers a variety of techniques for text data analysis, where the goal
is to analyze text data to find interesting semantic patterns and extract
useful knowledge. We cover algorithms for four basic text analysis tasks,
including text clustering, text categorization, text summarization, and topic
analysis, each covered in one chapter. The last chapter of this part takes a
broader view of the problem of text analysis by placing it in the context of
joint analysis of text and structured data, which is generally needed in an
application scenario where we have available both unstructured text data and
companion structured data, and would prefer analyzing all the data for solving
a particular application problem.

 - Overview of Text Data Analysis
   * Text analysis *vs* text management
   * Deep analysis *vs* shallow analysis
   * A conceptual framework for text analytics

 - Text Clustering
   * Overview of clustering techniques
   * Document clustering
   * Term clustering
   * Evaluation
   * Applications
   * Exercises

 - [Text
   Categorization](http://sifaka.cs.uiuc.edu/ir/textdatabook/chapters/text-data-book-draft-chapter12-Categorization.pdf) (Draft from 7 June 2015)
   * Overview of text categorization
   * Features for text categorization
   * Classification algorithms
   * Evaluation
   * Exercises

 - Topic Analysis
   * Overview of topic analysis techniques
   * Basic topic models
   * Advanced topic models
   * Evaluation
   * Applications
   * Exercises

 - Text Summarization
   * Overview of text summarization techniques
   * Extractive text summarization
   * Abstractive text summarization
   * Query-specific text summarization
   * Evaluation
   * Applications
   * Exercises

 - Joint Analysis of Text and Structured Data
   * Context and companion structured data of text
   * Contextualized text analysis
   * Integrated analysis of text and structured data
   * Evaluation
   * Applications
   * Exercises

## Part IV: Application System Development with MeTA

This last part of the book discusses how to use MeTA to develop an application
system for text analysis and management. It has two chapters. The first is
about a unified conceptual framework for integrating text data access and text
data analysis and preliminary ideas about how to design an algebra for text
analysis with multiple analysis operators that can be combined in a flexible
way to support different analysis workflows. The second is a detailed
discussion of how different components in MeTA can be combined in interesting
ways to support complex analysis workflows; it helps readers learn how to use
or adapt MeTA to develop useful text information systems to solve their
specific application problems. The last chapter provides information about how
people can contribute to the development of MeTA, which we expect to be an
ongoing effort with a dedicated website and regular open source releases.

 - A Unified Conceptual Framework for Text Analysis
   * An algebra for text analytics
   * Implementation of analysis operators
   * Workspace management
   * Workflow support and optimization

 - MeTA for Text Analysis and Management
   * Overview of MeTA modules
   * MeTA API
   * Other text analysis and management toolkits
   * Sample applications

 - Contributing to MeTA
