# Fetching all data in a fragment

Steps: to ensure that a client has retrieved all data in a fragment:

- retrieve the data in the fragment's representation
- iteratively follow `ldf:more` links while they exist
- iteratively follow `ldf:subFragment` links while they exist

`ldf:more` might lead to a data dump, because the fragment could just be metadata for an existing dump.

# Fragment class inheritance

Currently, `ldf:subFragmentClassOf` means that the sub-fragment-class inherits the following properties:

- `ldf:hasPattern`
- `ldf:optionalParameter`
- `ldf:requiredParameter`
- `ldf:hasQuery`

Maybe we should investigate whether these properties could (additionally) be defined on the instances with OWL property restrictions; this could allow an easier inheritance mechanism.
