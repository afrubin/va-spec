**Computational Definition**

A Statement reporting a conclusion from a single study about the role of a variant in modulating the response of a neoplasm to drug administration or other therapeutic procedures - based on interpretation of the study's results.

**Information Model**

Some VariantTherapeuticResponseStudyStatement attributes are inherited from :ref:`gks.core-im:Statement`.

.. list-table::
   :class: clean-wrap
   :header-rows: 1
   :align: left
   :widths: auto

   *  - Field
      - Type
      - Limits
      - Description
   *  - id
      - string
      - 0..1
      - The 'logical' identifier of the Entity in the system of record, e.g. a UUID.  This 'id' is unique within a given system, but may or may not be globally unique outside the system. It is used within a system to reference an object from another.
   *  - label
      - string
      - 0..1
      - A primary name for the entity.
   *  - description
      - string
      - 0..1
      - A free-text description of the Entity.
   *  - alternativeLabels
      - string
      - 0..m
      - Alternative name(s) for the Entity.
   *  - extensions
      - :ref:`Extension`
      - 0..m
      - A list of extensions to the Entity, that allow for capture of information not directly supported by elements defined in the model.
   *  - specifiedBy
      - :ref:`Method` | :ref:`IRI`
      - 0..1
      - A specification that describes all or part of the process that led to creation of the Information Entity 
   *  - contributions
      - :ref:`Contribution`
      - 0..m
      - Specific actions taken by an Agent toward the creation, modification, validation, or deprecation of an Information Entity.
   *  - reportedIn
      - :ref:`Document` | :ref:`IRI`
      - 0..m
      - A document in which the the Information Entity is reported.
   *  - dateAuthored
      - string
      - 0..1
      - Indicates when the information content expressed in the Information Entity was generated.
   *  - derivedFrom
      - :ref:`InformationEntity`
      - 0..m
      - Another Information Entity from which this Information Entity is derived, in whole or in part.
   *  - recordMetadata
      - :ref:`RecordMetadata`
      - 0..1
      - Provenance metadata about a specific concrete record of information as encoded/serialized in a particular data set or object (as opposed to provenance about the abstract information content the encoding carries).
   *  - direction
      - string
      - 0..1
      - A term indicating whether the Statement supports, disputes, or remains neutral w.r.t. the validity of the Proposition it evaluates.
   *  - strength
      - :ref:`Coding` | :ref:`IRI`
      - 0..1
      - A term used to report the strength of a Proposition's assessment in the direction indicated (i.e. how strongly supported or disputed the Proposition is believed to be).  Implementers may choose to frame a strength assessment in terms of how *confident* an agent is that the Proposition is true or false, or in terms of the *strength of all evidence* they believe supports or disputes it.
   *  - score
      - number
      - 0..1
      - A quantitative score that indicates the strength of a Proposition's assessment in the direction indicated (i.e. how strongly supported or disputed the Proposition is believed to be).  Depending on its implementation, a score may reflect how *confident* that agent is that the Proposition is true or false, or the *strength of evidence* they believe supports or disputes it.
   *  - statementText
      - string
      - 0..1
      - A natural-language expression of what a Statement asserts to be true.
   *  - classification
      - :ref:`Coding` | :ref:`IRI`
      - 0..1
      - A single term or phrase summarizing the outcome of direction and strength assessments of a Statement's proposition, in terms of a classification of its subject.
   *  - hasEvidenceLines
      - :ref:`EvidenceLine`
      - 0..m
      - An evidence-based argument that supports or disputes the validity of the proposition that a Statement assesses or puts forth as true. The strength and direction of this argument (whether it supports or disputes the proposition, and how strongly) is based on an interpretation of one or more pieces of information as evidence (i.e. 'Evidence Items).
   *  - type
      - string
      - 1..1
      - MUST be "VariantTherapeuticResponseStudyStatement".
   *  - subjectVariant
      - :ref:`Variation` | :ref:`CategoricalVariant` | :ref:`IRI`
      - 1..1
      - A variant that is the subject of the Statement.
   *  - predicate
      - string
      - 1..1
      - The relationship declared to hold between the subject and the object of the Statement.
   *  - objectTherapeutic
      - :ref:`TherapeuticProcedure` | :ref:`IRI`
      - 1..1
      - A drug administration or other therapeutic procedure that the neoplasm is intended to respond to.
   *  - diseaseQualifier
      - :ref:`Condition` | :ref:`IRI`
      - 1..1
      - Reports the disease context in which the variant's association with therapeutic sensitivity or resistance is evaluated. Note that this is a required qualifier in therapeutic response statements.
   *  - alleleOriginQualifier
      - string
      - 0..1
      - Reports whether the statement should be interpreted in the context of an inherited (germline) variant, an acquired (somatic) mutation, or both (combined).
   *  - allelePrevalenceQualifier
      - string
      - 0..1
      - Reports whether the statement should be interpreted in the context of the variant being rare or common.
   *  - geneContextQualifier
      - :ref:`Gene`
      - 0..1
      - Reports a gene impacted by the variant, which may contribute to the therapeutic sensitivity or resistance reported in the Statement.

