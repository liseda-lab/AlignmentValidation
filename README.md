# AlignmentValidation

The Alignment API use a Alignment RDF Format that express alignments in a consensual format. We present an extension of the Alignment RDF Format described in https://moex.gitlabpages.inria.fr/alignapi/format.html to allow the revision and validation of alignments.


## Formal description

### *revision* element

The *revision* element is an attribute of the *Cell* element, and contains the information resulting from the revision or validation of a specific correspondence between entities of the ontologies. It contains one attribute:

* ***status* element**

  (value: String; default: unreviewed) contains a string identifying the result from the revision or validation of the relation between the first and the second entity. This may be given by four different values: unreviewed (default), correct, incorrect and unsure.

~~~
<Cell>
	<entity1 rdf:resource="http://mouse.owl#MA_0001705"/>
	<entity2 rdf:resource="http://human.owl#NCI_C33487"/>
	<measure rdf:datatype="http://www.w3.org/2001/XMLSchema#float">0.94</measure>
	<relation>=</relation>
	<revision>
		<status>unreviewed</status>
	</revision>
</Cell>

~~~

* ***author* element**

  (value: String;) contains a string identifying the author of that revision or validation.
  
  ~~~
<Cell>
	...
	<revision>
		<status>unreviewed</status>
		<author>John</author>
	</revision>
</Cell>

~~~
  
  
* ***timestamp* element**

  (value: String;) contains a string identifying the time that that revision or validation occurred.
  
    ~~~
<Cell>
	...
	<revision>
		<status>unreviewed</status>
		<author>John</author>
		<timestamp>2021-09-04*13:23:55</timestamp>
	</revision>
</Cell>

~~~
