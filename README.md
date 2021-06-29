# AlignmentValidation

The Alignment API use a Alignment RDF Format that express alignments in a consensual format. We present an extension of the Alignment RDF Format described in https://moex.gitlabpages.inria.fr/alignapi/format.html to allow the revision and validation of alignments.


## Formal description

### *revision* element

The *revision* element is an attribute of the *Cell* element, and contains the information resulting from the revision or validation of a specific correspondence between entities of the ontologies. It contains one attribute:

* ***status* element**

  (value: String; default: unreviewed) contains a string identifying the result from the revision or validation of the relation between the first and the second entity. This may be given by four different values: unreviewed (default), correct, incorrect and unsure.

~~~
<Cell>
	...
	<revision>
		<status>unreviewed</status>
	</revision>
</Cell>

~~~
