Welcome to Lesson 3 of Module 6 on Notation for Entity Relationship Diagrams. I'm going to start with a question about the difference between two data modeling concepts.
Play video starting at ::22 and follow transcript0:22
What is the difference between existence dependency and identification dependency?
Play video starting at ::28 and follow transcript0:28
Lesson 3 expounds on the basics of ERDs provided in Lesson 2 to some specialized but important relationship variations.
Play video starting at ::38 and follow transcript0:38
These relationship variations do not occur often in practice. However, when occurring, these variations are important parts of a data model.
Play video starting at ::47 and follow transcript0:47
The objectives in this lesson involve two specialized types of relationships, identification dependency and many-to-many relationships with attributes.
Play video starting at ::57 and follow transcript0:57
You should be able to articulate the elements of identification dependency in an example. To demonstrate understanding of many-to-many relationships, you should be able to apply the many-to-many relationship equivalency rule to an example.
Play video starting at :1:12 and follow transcript1:12
The most important objective is to appreciate specialized relationships, but avoid temptation to overuse them.
Play video starting at :1:19 and follow transcript1:19
Typical novice mistakes in data modeling are to overuse specialized relationships.
Play video starting at :1:25 and follow transcript1:25
In some business situations, an entity type may not have its own primary key.
Play video starting at :1:31 and follow transcript1:31
Entity types without their own primary key must borrow part or all of their primary key from other entity types. Entity types that borrow part or their entire primary key are known as weak entity types.
Play video starting at :1:46 and follow transcript1:46
A relationship that provides a component of the primary key is known as an identifying relationship. Thus, an identification dependency involves a weak entity type in one or more identifying relationships.
Play video starting at :2:1 and follow transcript2:01
Identification dependency occurs because some entities are closely associated with other entities. For example, a room does not have an identity separate from its building, because a room is physically contained in a building.
Play video starting at :2:15 and follow transcript2:15
You can reference a room only by providing its associated building identifier. In the ERD for buildings and rooms, the room entity type is identification-dependent on the building entity type in the contains relationship.
Play video starting at :2:30 and follow transcript2:30
A solid relationship line indicates an identifying relationship.
Play video starting at :2:35 and follow transcript2:35
For weak entity types, the underlying attribute, if present, is part of the primary key, but not the entire primary key. Thus, the primary key of room is a combination of BldgId from the building entity type and RoomNo from the room entity type. One of the differences between an ERD and a relational database diagram is that relationships in ERD can have attributes. This situation typically occurs with many-to-many relationships.
Play video starting at :3:5 and follow transcript3:05
In a many-to-many relationship, attributes are associated with a combination of entity types, not just one of the entity types.
Play video starting at :3:13 and follow transcript3:13
If an attribute is associated with only one entity type, then it should be part of that entity type, not the relationship.
Play video starting at :3:20 and follow transcript3:20
In this ERD the attribute EnrGrade is associated with a combination of a student offering, not either one alone.
Play video starting at :3:29 and follow transcript3:29
For example, the EnrolsIn relationship records the fact that student with student number 123779993 has a grade of 3.5 in the offering with offer number of 1256. To provide clarification about many-to-many relationships with attributes, these partial ERDs show more examples.
Play video starting at :3:53 and follow transcript3:53
In Example A, the attribute quantity, or Qty, represents the quantity of a part supplied by a given supplier.
Play video starting at :4:1 and follow transcript4:01
In Example B, the attribute AuthOrder represents the order in which the author's name appears in a title of the book. To improve your understanding of many-to-many relationships, you should know an important equivalence for many-to-many relationships. An M-N, or many-to-many relationship, can be replaced by an associative entity type and two identifying one-to-many relationships. This associative entity type style is similar to the representation in a relational database diagram with an associative table containing the combined primary key, consisting of two foreign keys.
Play video starting at :4:39 and follow transcript4:39
If you feel more comfortable with the one-to-many style, then use it. In terms of the ERD, the many-to-many and one-to-many styles have the same meaning. As an example of the many-to-many relationship equivalency role, the EnrolsIn relationship is replaced by two identifying relationships, registers and grants, and an associative entity type enrollment.
Play video starting at :5:2 and follow transcript5:02
The relationship name EnrolsIn has been changed to a now enrollment to follow the convention for nouns for entity type names.
Play video starting at :5:12 and follow transcript5:12
There is one situation when the one-to-many style is preferred to many-to-many style.
Play video starting at :5:18 and follow transcript5:18
When a many-to-many relationship must be related to other entity types and relationships, you must use the one-to-many style.
Play video starting at :5:25 and follow transcript5:25
Since this situation is not common, the choice of a many-to-many relationship or an associative entity type is largely a matter of preference.
Play video starting at :5:34 and follow transcript5:34
Now, let's wrap up Lesson 3 about relationship variations for ERDs.
Play video starting at :5:40 and follow transcript5:40
This lesson covered two important variations, identification dependency and many-to-many relationships with attributes. You learned about an important equivalency rule to transform many-to-many relationships with attributes into an associative entity type and two one-to-many relationships.
Play video starting at :5:59 and follow transcript5:59
This transformation is largely a matter of personal preference.
Play video starting at :6:3 and follow transcript6:03
Most students prefer the associative entity type representation, because it is similar to the representation in a relational database diagram.
Play video starting at :6:12 and follow transcript6:12
These relationship variations are not common in practice but important when they occur.
Play video starting at :6:18 and follow transcript6:18
However, typical novice mistakes are to overuse specialized relationships. So make sure that you understand them before using them in practice.
Play video starting at :6:27 and follow transcript6:27
For Modules 6 and 7, you should focus on understanding notation in ERD for both kinds of specialized relationships. Modules 8 and 9 will give you practice with analyzing narrative problem statements to determine when these specialized kinds of relationships are appropriate in business situations.
Play video starting at :6:46 and follow transcript6:46
An answer to the opening question, identification dependency is a specialized kind of existence dependency.
Play video starting at :6:54 and follow transcript6:54
Recall that an existent dependent entity type has a mandatory relationship that is of minimum cardinality one.
Play video starting at :7:1 and follow transcript7:01
Weak entity types are existent dependent on the identifying relationships.
Play video starting at :7:6 and follow transcript7:06
In addition to the existence dependency, a weak entity type borrows at least part of its primary key.
Play video starting at :7:12 and follow transcript7:12
Because of the existence dependency in the primary key borrowing, the minimum/maximum cardinalities and weak entity type are always one.
Play video starting at :7:21 and follow transcript7:21
Thus, identification dependency implies existence dependency. Existence dependency is a common situation in business databases. In contrast, identification dependency is much less common, even rare, in business databases.


Welcome to Lesson 4 of Module 6, a Notation for Entity Relationship Diagrams. I'm going to start with a hot trivia question about one of the data modeling concepts covered in this lesson.
Play video starting at ::24 and follow transcript0:24
What data modeling concept reminds me of Cincinnati chili? Lesson 4 continues on the relationship variations theme that was started in Lesson 3. The relationship variations covered in Lesson 4 do not occur often in practice. However, when occurring, these variations are important parts of a data model.
Play video starting at ::45 and follow transcript0:45
The objectives in this lesson involve two specialized types of relationships, self-identifying relationships and M-way relationships. You should be able to draw an instance diagram to depict a self-referencing relationship.
Play video starting at ::59 and follow transcript0:59
You should be able to explain the example of an M-way relationship situation in ERD.
Play video starting at :1:4 and follow transcript1:04
The most important objective is to appreciate specialized relationships but avoid temptation to overuse them.
Play video starting at :1:12 and follow transcript1:12
Typical novice mistakes in data modeling are to overuse specialized relationships. A self-referencing relationship involves connections among members of the same set.
Play video starting at :1:23 and follow transcript1:23
Self-referencing relationships are sometimes called reflexive relationships, because they are like a reflection in a mirror.
Play video starting at :1:30 and follow transcript1:30
This partial ERD shows two self-referencing relationships involving the faculty and course entity types.
Play video starting at :1:39 and follow transcript1:39
Both relationships involve two entity types that are the same, faculty for supervises and course for prerequisite tool. Note both relationships start and terminate with the same entity type.
Play video starting at :1:52 and follow transcript1:52
These relationships depict important concepts in the university database. The supervises relationship depicts an organizational chart, while the prerequisite relationship depicts course dependencies that can affect a student's course planning. Self-referencing relationships occur in a variety of business situations. Any set that can be visualized as a hierarchy can be represented as a self-referencing relationship. Typical examples include hierarchical charts of accounts, genealogical charts, part designs, and transportation routes. In these examples, self-referencing relationships are an important part of the database. For self-referencing relationships, it is important to distinguish between one-to-many and many-to-many relationships. An instance diagram can help you understand the difference. The hierarchy in Part A shows an instance diagram for the supervises relationship.
Play video starting at :2:49 and follow transcript2:49
Notice that each faculty has at most one superior. For example, Faculty 2 and Faculty 3 have Faculty 1 as a superior. Therefore, supervises is a one-to-many relationship, because each faculty can't have at most one supervisor.
Play video starting at :3:6 and follow transcript3:06
In contrast, there is no such restriction in the instance diagram for the prerequisite relationship shown in Part B. For example, IS461 has two prerequisites, IS480 and IS460, while IS320 is a prerequisite to both IS480 and IS460.
Play video starting at :3:26 and follow transcript3:26
Therefore, PreReqTo is a many-to-many relationship, because a course can be a prerequisite to many courses, and a course can have many prerequisites. An M-way relationship involves an association of more than two entity types. The crow's foot notation only supports binary relationships, so M-way relationships cannot be directly represented. Instead, an M-way relationship is indirectly represented as an associated entity type and a collection of one-to-many relationships.
Play video starting at :3:58 and follow transcript3:58
The typical value for M is three, as relationships involving more than three entity types are very rare in practice.
Play video starting at :4:6 and follow transcript4:06
Three-way relationships are not common practice either but important when occurring.
Play video starting at :4:12 and follow transcript4:12
In this ERD, three one-to-many relationships link the associative entity type uses to the part, supplier, and project entity types. The uses entity type is associative, because its role is to connect other entity types. Because associative entity types provide a connecting role, they are sometimes given names using active verbs. In addition, associative entity types are always weak as they must borrow the entire primary key.
Play video starting at :4:38 and follow transcript4:38
For example, the uses entity type obtains its primary key through the three identifying relationships.
Play video starting at :4:46 and follow transcript4:46
The issue of when to use an M-way associative entity type can be difficult to understand.
Play video starting at :4:52 and follow transcript4:52
If a database only needs to record pairs of facts, an M-way associative entity type is not needed.
Play video starting at :4:59 and follow transcript4:59
For example, if a database only needs to record who supplies a part and what projects use a part, then the M-way associative entity type should not be used.
Play video starting at :5:9 and follow transcript5:09
In this case, there should be binary relationships between supplier and part and between project and part.
Play video starting at :5:17 and follow transcript5:17
You should use an M-way associative entity type when the database should record combinations of three or more entities rather than just combinations of two entities.
Play video starting at :5:27 and follow transcript5:27
For example, if the database needs to record which supplier provide parts on specific projects, an M-way associative type is needed. Now, let's wrap up Lesson 4 about relationship variations for ERDs.
Play video starting at :5:42 and follow transcript5:42
This lesson covered two important variations, self-identifying relationships and M-way relationships. Self-referencing relationships support business requirements in which members of a set are represented as a hierarchy. Typical examples include hierarchical charts of accounts, genealogical charts, part designs, and transportation routes. An M-way relationship represents a business situation involving a combination of more than two entities. Because the crow's foot notation only represents binary relationships in a social entity type in a collection of one-to-many, identifying relationships are used.
Play video starting at :6:21 and follow transcript6:21
These relationships are not common in practice but important when they occur. However, typical novice mistakes are to overuse specialized relationships, so make sure you understand them before using them in practice. M-way relationships are especially error-prone because of the complexity of the business situations involving more than two entities.
Play video starting at :6:43 and follow transcript6:43
For Modules 6 and 7, you should focus on understanding the notation in the ERD for both kinds of specialized relationships.
Play video starting at :6:51 and follow transcript6:51
Modules 8 and 9 will give you practice with analyzing narrative problem statements to identify these specialized kinds of relationships in business requirements. Lesson 4 concludes Module 6. Module 7 refined your background about the notation of ERDs covering diagram rules and practice problems. Now, in answer to the opening question, an M-way relationship reminds me of Cincinnati chili, a favorite comfort food found in chili parlor restaurants in Cincinnati, Ohio.
Play video starting at :7:23 and follow transcript7:23
Cincinnati chili comes in two to five varieties. The basic two-way involves spaghetti topped with chili sauce.
Play video starting at :7:31 and follow transcript7:31
For a three-way, cheese is also added. For a four-way, onions are added. For a five-way, beans are added. So that a five-way contains spaghetti, chili sauce, cheese, onions, and beans. M-way relationships in ERD involve M greater than two. The most common value for M in an M-way relationship is three.
Play video starting at :7:52 and follow transcript7:52
If you ever visit Cincinnati, Ohio, USA, and eat chili, think about M-way relationships in data modeling.