---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

// THE PYTHON SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
client =  GraphServiceClient(request_adapter)

request_body = LearningCourseActivity()
request_body.@odata_type = '#microsoft.graph.learningSelfInitiatedCourse'

request_body.completedDateTime=null

request_body.CompletionPercentage = 20

request_body.external_course_activity_id = '12a2228a-e020-11ec-9d64-0242ac120002'

request_body.learning_content_id = '57baf9dc-e020-11ec-9d64-0242ac120002'

request_body.learner_user_id = '7ba2228a-e020-11ec-9d64-0242ac120002'

request_body.status(CourseStatus.InProgress('coursestatus.inprogress'))

additional_data = [
'started_date_time' => '2021-05-21T22:57:17+00:00', 
];
request_body.additional_data(additional_data)





result = await client.employee_experience.learning_providers.by_learning_provider_id('learningProvider-id').learning_course_activities.post(request_body = request_body)


```