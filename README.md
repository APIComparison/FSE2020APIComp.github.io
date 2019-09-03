# Replication Package of Generating Concept based API Element Comparison Using a Knowledge Graph

## Empirical Study

### API Comparison Question Select

- To retrieve questions about API comparison, we selected questions from the Stack Overflow data dump. 1487 selected questions from the Stack Overflow had either of the strings "difference between" or “vs” in the title. [Questions File](https://github.com/ICSE2020APIComp/ICSE2020APIComp.github.io/blob/master/question_select/1487_all_questions.json). In the json file, "Id" represent Stack Overflow post ID, "Title" represent Stack Overflow question title, "Score" represent Stack Overflow question vote.


- The manual removal was conducted by two students independently (one PhD and one MS student, both with more than five years Java experience), this is 1487 questions two students independently annotated result. [1487 Question Select Annotated Result](https://github.com/ICSE2020APIComp/ICSE2020APIComp.github.io/blob/master/question_select/1487_Question_Select_annotated_result.xlsx). In this excel file, the column "Stack Overflow Post ID" represent post ID in Stack Overflow. And the column "User 1", "User 2", represent two students annotated result, "T" means that question is related to the JDK API comparison, "F" means not.

- We only kept questions that had been annotated as relevant by both students, resulting in 215 questions. [215 questions](https://github.com/ICSE2020APIComp/ICSE2020APIComp.github.io/blob/master/question_select/215_questions), In this excel file, the column "id" represent post ID in Stack Overflow, "title" represent Stack Overflow question title, "url" represent corresponding Stack Overflow URL, "question_vote" represent the Stack Overflow question votes when we got.

- We randomly selected 100 API comparison questions out of the 215. [100 select questions](https://github.com/ICSE2020APIComp/ICSE2020APIComp.github.io/blob/master/question_select/100_select_question.xlsx). [115 unselect questions](https://github.com/ICSE2020APIComp/ICSE2020APIComp.github.io/blob/master/question_select/115_unselect_question.xlsx), In the excel files, the column "id" represent post ID in Stack Overflow, "title" represent Stack Overflow question title, "url" represent corresponding Stack Overflow URL, "question_vote" represent the Stack Overflow question votes when we got.


### Answer Point

- Where answer point can be found in API document for 100 selected API comparison questions?[answer point info](https://github.com/ICSE2020APIComp/ICSE2020APIComp.github.io/blob/master/question_select/answer_point.xlsx), in this excel file, in the column "class or method", "M" represent Method, "C" represent Class/Interface, column "answer point" is atomic answer point, column "Compare APIs" is all APIs involved in one answer point, "Is this information available in some form in the API documentation? yes/no" means whether we can infer answer point from JDK documentation. "Which API documentation page contained this information?" means all places we can find, "where in API doc?first sentence of class/first paragraph of class/full text of class/class hierarchical structure/class declaration/first sentence of method/full text of method/method declaration" record where we can find. "statements in API doc?" record which statement we infer this answer point.

### Statement Types

- eight statement types[Statement Types](https://github.com/ICSE2020APIComp/ICSE2020APIComp.github.io/blob/master/classification_of_knowledge_types.xlsx), in this excel file, in the column "template in SO", answer point can be classified into eight types.


## Approach

- We manually analyzed the description sentences of two API packages java.io and java.util and summarized 25 linguistic patterns.[25 linguistic patterns](https://github.com/ICSE2020APIComp/ICSE2020APIComp.github.io/blob/master/template/template.md)

## Evaluation
### RQ1 Related Data
- Randomly selected 384 API statements for each of the three aspects (i.e., category, functionality, characteristic) and each of the two sources, students labeled result and arbitrate result.[student 1](https://github.com/ICSE2020APIComp/ICSE2020APIComp.github.io/blob/master/RQ1/extract_relations_Integration_user_1.xlsx), [student 2](https://github.com/ICSE2020APIComp/ICSE2020APIComp.github.io/blob/master/RQ1/extract_relations_integration_user_2.xlsx), [arbitrate result](https://github.com/ICSE2020APIComp/ICSE2020APIComp.github.io/blob/master/RQ1/extract_relations_Integration_arbitrate.xlsx). In the sheet "func_text_relation", they are 384 API statements of functionality extracted from the text, in the sheet "func_name_relation", they are 384 API statements of functionality extracted from API name, in the sheet "character_text_relation", they are 384 API statements of characteristic extracted from text, in the sheet "character_name_relation", they are 384 API statements of characteristic extracted from API name, in the sheet "category_text_relation", they are 384 API statements of category extracted from text, in the sheet "category_name_relation", they are 384 API statements of category extracted from API name or API structure. The column "s_name" means start name, "e_name" means end name, "r_name" is the relation name, column "other_info" show where we extract this API statement. column "T/F" means whether the extract statement is valid, "T" for valid, "F" for invalid.  

- [equal/opposite characteristics label reuslt](https://github.com/ICSE2020APIComp/ICSE2020APIComp.github.io/blob/master/RQ1/384_synonyms_antonym_arbitrate.xlsx), there are 3 sheets, "user_1" sheet is the first student labeled result, "user_2" sheet is the second student labeled result, the column "start" means the start name in relation tuple, "end" means the end name in relation tuple, "relation" means the relation name, result means whether the extract statement is valid, "1" for valid, "0" for invalid.  

- [noun concept categorization](https://github.com/ICSE2020APIComp/ICSE2020APIComp.github.io/blob/master/RQ1/384_np_suffix_prefix_with_arbitrate.xlsx), there are 3 sheets, "user_1" sheet is the first student labeled result, "user_2" sheet is the second student labeled result, the column "start" means the start name in relation tuple, "end" means the end name in relation tuple, "relation" means the relation name, result means whether the extract statement is valid, "1" for valid, "0" for invalid.


- General concept linking data [student 1](https://github.com/ICSE2020APIComp/ICSE2020APIComp.github.io/blob/master/RQ1/384_random_select_wikidata_1.json); [student 2](https://github.com/ICSE2020APIComp/ICSE2020APIComp.github.io/blob/master/RQ1/384_random_select_wikidata_2.json); [arbitrate result](https://github.com/ICSE2020APIComp/ICSE2020APIComp.github.io/blob/master/RQ1/384_random_select_wikidata_Arbitrate.json). In these json files, "name" means the wikidata name, "alias" means all alias name for this wikidata, "description" means the wikidatga description, "domain term" means the category name, "link" means whether we linked this wikidata to the category name. "result" means whether the result of the link is correct?

### RQ2 Related Data
- Completeness and conciseness understandability score and answer point covered. There are 2 sheet, "base_line" sheet shows the result for baseline approach, "difference" sheet shows the result for APIComp. [student 1](https://github.com/ICSE2020APIComp/ICSE2020APIComp.github.io/blob/master/RQ2/rq_2_1.xlsx) [student 2](https://github.com/ICSE2020APIComp/ICSE2020APIComp.github.io/blob/master/RQ2/rq_2_2.xlsx) [student 3](https://github.com/ICSE2020APIComp/ICSE2020APIComp.github.io/blob/master/RQ2/rq_2_3.xlsx) [student 4](https://github.com/ICSE2020APIComp/ICSE2020APIComp.github.io/blob/master/RQ2/rq_2_4.xlsx). column "compare API_1" and "compare API_2" represent the two compare APIs, column "answer point" is how many answer point covered, column "concise" is concise score, column "complete" is completeness score, column "understandable" is understandability score.


### RQ3 Related Data
- There are two sheet, "GA" and "GB", indicates the two participant groups. [Participant experience statistics](https://github.com/ICSE2020APIComp/ICSE2020APIComp.github.io/blob/master/RQ3/experience.xlsx), the column "experience/year" represent the age of the participants using java.
- Group A result[GA reuslt](https://github.com/ICSE2020APIComp/ICSE2020APIComp.github.io/blob/master/RQ3/result/GA/) 
- Group B result[GB reuslt](https://github.com/ICSE2020APIComp/ICSE2020APIComp.github.io/blob/master/RQ3/result/GB/)
- In these result files, column "tool/search engine" represent which method the participant use, column "answer (1-API_1,  2-API_2, 3-unknown)" represent which API the participant select, column "cost_time_v1:" represent the total time cost to make the decision,the unit is seconds. 