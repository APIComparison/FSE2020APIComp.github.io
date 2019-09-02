# Replication Package of Generating Concept based API Element Comparison Using a Knowledge Graph

## Empirical Study

- To retrieve questions about API comparison, we selected questions from the Stack Overflow data dump. 1487 selected questions from the Stack Overflow had either of the strings "difference between" or “vs” in the title. "Id" represent Stack Overflow post ID, "Title" represent Stack Overflow question title, "Score" represent Stack Overflow question vote. [Questions File](https://github.com/ICSE2020APIComp/ICSE2020APIComp.github.io/blob/master/question_select/1487_all_questions.json)


- The manual removal was conducted by two students independently (one PhD and one MS student, both with more than five years Java experience), this is 1487 questions two students independently annotated result. The column "Stack Overflow Post ID" represent post ID in Stack Overflow. And the column "User 1", "User 2", represent two students annotated result, "T" means that question is related to the JDK API comparison, "F" means not. [1487 Question Select Annotated Result](https://github.com/ICSE2020APIComp/ICSE2020APIComp.github.io/blob/master/question_select/1487_Question_Select_annotated_result.xlsx)

- We only kept questions that had been annotated as relevant by both students, resulting in 215 questions. [215 questions](https://github.com/ICSE2020APIComp/ICSE2020APIComp.github.io/blob/master/question_select/100_select_question.xlsx)

- [100 select questions](https://github.com/ICSE2020APIComp/ICSE2020APIComp.github.io/blob/master/question_select/100_select_question.xlsx)


- [115 unselect questions](https://github.com/ICSE2020APIComp/ICSE2020APIComp.github.io/blob/master/question_select/115_unselect_question.xlsx)

- [100 threads label result](https://github.com/ICSE2020APIComp/ICSE2020APIComp.github.io/blob/master/question_select/all_statement_template_label_with_Kappa.xlsx)

## Approach

- [25 linguistic patterns](https://github.com/ICSE2020APIComp/ICSE2020APIComp.github.io/blob/master/template/template.md)

## Evaluation
### RQ1 Related Data
- randomly selected 384 API statements for each of the three aspects (i.e., category, functionality, characteristic) and each of the two sources, students labeled result and arbitrate result.[student 1](https://github.com/ICSE2020APIComp/ICSE2020APIComp.github.io/blob/master/RQ1/extract_relations_Integration_user_1.xlsx) [student 2](https://github.com/ICSE2020APIComp/ICSE2020APIComp.github.io/blob/master/RQ1/extract_relations_integration_user_2.xlsx)

- [equal/opposite characteristics label reuslt](https://github.com/ICSE2020APIComp/ICSE2020APIComp.github.io/blob/master/RQ1/384_synonyms_antonym_arbitrate.xlsx)

- [noun concept categorization](https://github.com/ICSE2020APIComp/ICSE2020APIComp.github.io/blob/master/RQ1/384_np_suffix_prefix_with_arbitrate.xlsx)


- general concept linking data [student 1](https://github.com/ICSE2020APIComp/ICSE2020APIComp.github.io/blob/master/RQ1/384_random_select_wikidata_1.json); [student 2](https://github.com/ICSE2020APIComp/ICSE2020APIComp.github.io/blob/master/RQ1/384_random_select_wikidata_2.json); [arbitrate result](https://github.com/ICSE2020APIComp/ICSE2020APIComp.github.io/blob/master/RQ1/384_random_select_wikidata_Arbitrate.json)

### RQ2 Related Data
- completeness and conciseness understandability score and answer point covered. [student 1](https://github.com/ICSE2020APIComp/ICSE2020APIComp.github.io/blob/master/RQ2/rq_2_1.xlsx) [student 2](https://github.com/ICSE2020APIComp/ICSE2020APIComp.github.io/blob/master/RQ2/rq_2_2.xlsx) [student 3](https://github.com/ICSE2020APIComp/ICSE2020APIComp.github.io/blob/master/RQ2/rq_2_3.xlsx) [student 4](https://github.com/ICSE2020APIComp/ICSE2020APIComp.github.io/blob/master/RQ2/rq_2_4.xlsx)

- [arbitrate result](https://github.com/ICSE2020APIComp/ICSE2020APIComp.github.io/blob/master/RQ2/RQ2_Arbitrate.xlsx)

### RQ3 Related Data
- [Participant experience statistics](https://github.com/ICSE2020APIComp/ICSE2020APIComp.github.io/blob/master/RQ3/experience.xlsx) 
- [GA reuslt](https://github.com/ICSE2020APIComp/ICSE2020APIComp.github.io/blob/master/RQ3/result/GA/) 
- [GB reuslt](https://github.com/ICSE2020APIComp/ICSE2020APIComp.github.io/blob/master/RQ3/result/GB/)
