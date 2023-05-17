
# Api doc
## Api url
```
/api/todo
```
## 1.1 Login
```
POST /api/todo
```
### Params:
```
(null)
```
### Body:
```
{
  "login": "test",
  "password": "test"
}
```
### Response: 
```
{
  "error": false,
  "message": null,
  "token": "50x9v0uqxvLsBctrX1brKOL1TRhw5oDt",
  "userId": 11
}
```
## 1.2 Logout
```
DELETE /api/todo
```
### Params:
```
(null)
```
### Body:
```
(null)
```
### Response: 
```
{
  "error":false,
  "message": null
}
```
## 1.3 Register
```
POST /api/todo/register
```
### Params:
```
(null)
```
### Body:
```
{
  "login": "admin",
  "password": "admin",
  "name": "jan",
  "last_name: "kowalski"
}
```
### Response: 
```
{
  "error":false,
  "message": null
}
```
## 2.1 Get projects list
```
GET /api/todo
```
### Params:
```
(null)
```
### Body:
```
(null)
```
### Response: 
```
{
  "error": false,
  "message": null,
  "projects": [
    {
      "id": 1,
      "project_name": "project1",
      "user_id": 1
    },
    {
      "id": 2,
      "project_name": "project2",
      "user_id": 2
    }
  ]
}
```
## 2.2 Create new project
```
POST /api/todo/createproject
```
### Params:
```
(null)
```
### Body:
```
{
  "project_name":"project name",
  "user_id": 2
}
```
### Response: 
```
{
  "error": false,
  "message": null
}
```
## 2.3 Delete project
```
DELETE /api/todo/{project_id}
```
### Params:
```
project_id - unique id of the project
```
### Body:
```
(null)
```
### Response: 
```
{
  "error": false,
  "message": null
}
```
## 2.4 Rename project
```
PUT /api/todo/{project_id}
```
### Params:
```
project_id - unique id of the project
```
### Body:
```
}
  "project_name": "new name"
}
```
### Response: 
```
{
  "error": false,
  "message": null
}
```
## 3.1 Add task to project
```
POST /api/todo/{project_id}
```
### Params:
```
project_id - unique id of the project
```
### Body:
```
{
  "description":"sample text"
}
```
### Response: 
```
{
  "error": false,
  "message": null
}
```
## 3.2 Remove task from project
```
DELETE /api/todo/project/{task_id}
```
### Params:
```
task_id - unique id of the task
```
### Body:
```
(null)
```
### Response: 
```
{
  "error": false,
  "message": null
}
```
## 3.3 Editing task
```
PUT /api/todo/project/{task_id}
```
### Params:
```
task_id - unique id of the task
```
### Body:
```
{
  "description": "new text"
}
```
### Response: 
```
{
  "error": false,
  "message": null
}
```
## 3.4 Marked task as done
```
POST /api/todo/project/{task_id}
```
### Params:
```
task_id - unique id of the task
```
### Body:
```
{
  "done": 1
}
```
### Response: 
```
{
  "error": false,
  "message": null
}
```

## 3.5 Get tasks list
```
GET /api/todo/{project_id}
```
### Params:
```
project_id - unique id of the project
```
### Body:
```
(null)
```
### Response: 
```
{
  "error": false,
  "message": null,
  "tasks": [
    {
      "id": 1,
      "description": "task1"
    },
    {
      "id": 2,
      "description": "task2"
    }
  ]
}
```
