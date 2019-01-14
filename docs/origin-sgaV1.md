# Origin SGA API::V1

Todas URIs são relativas à: *http://localhost:3001/v1* no ambiente de desenvolvimento.

### Autorização

Não é requerida autorização.

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

## End-points

HTTP requisição | Descrição | Exemplo
------------- | ------------- | -------------
**GET** /student/{id} | Exibe o estudante pelo id | *http://localhost:3001/v1/student/1*
**GET** /course/student/{id} | Exibe o curso em que o estudante está matriculado pelo seu respectivo id| *http://localhost:3001/v1/course/student/1*
**GET** /employee/student/{id} | Exibe o professor responsável pela turma de acordo com o id do aluno | *http://localhost:3001/v1/employee/student/1*


## Student

**GET** /student/{id}
---
Exibe o estudante

Exibe o estudante pelo seu id

### Parâmetros

Nome | Tipo | Descrição | Exemplo
------------- | ------------- | ------------- | -------------
 **id** | **Integer** | requerido no PATH | *http://localhost:3001/v1/student/1*

### Status Code

**200** ```OK```

### Exemplo de resposta
```json
{
    "student": {
        "id": 1,
        "class_id": 1515,
        "ethnicity_id": null,
        "marital_status_id": null,
        "countriy_id": null,
        "address_id": 130,
        "city_id": null,
        "name": "Cezar Tramontina Martins",
        "last_name": null,
        "cpf": "01045412202",
        "academic_register": 1829070,
        "birth_date": "1982-08-16",
        "flag_on": 1,
        "blood_type": null,
        "organ_donor": null,
        "assumed_name": null,
        "gender": "M",
        "students_type": "regular",
        "current_status": "enrolled",
        "flag_pwd": 0,
        "flag_blindness": 0,
        "flag_vision_impairment": 0,
        "flag_deafness": 0,
        "flag_hearing": 0,
        "flag_physical_disability": 0,
        "flag_deafblindness": 0,
        "flag_multiple": 0,
        "flag_intellectual": 0,
        "flag_autism": 0,
        "flag_asperger": 0,
        "flag_rett": 0,
        "flag_childhood_disintegrative_disease": 0,
        "flag_giftedness": 0,
        "created_at": null,
        "updated_at": null,
        "deleted_at": null,
        "flag_ppi": 0,
        "id_legacy": 52045
    }
}
```
**404** ```Not Found```

**500** ```Erro interno no servidor```

## Course

**GET** /course/student/{id}
---
Exibe o curso

Exibe o curso em que o estudante está matriculado pelo seu respectivo id

### Parâmetros

Nome | Tipo | Descrição | Exemplo
------------- | ------------- | ------------- | -------------
 **id** | **Integer** | requerido no PATH | *http://localhost:3001/v1/course/student/7*

### Status Code

**200** ```OK```

### Exemplo de resposta
```json
{
    "course": [
        {
            "id": 7,
            "name": "Engenharia de Produção",
            "duration_semesters": "6",
            "course_type": "Undergraduation",
            "created_at": "2018-12-13T18:54:38.000Z",
            "updated_at": null,
            "deleted_at": null
        }
    ]
}
```
**404** ```Not Found```

**500** ```Erro interno no servidor```

## Employee

**GET** /employee/student/{id}
---
Exibe o professor

Exibe o professor responsável pela turma de acordo com o id do aluno

### Parâmetros

Nome | Tipo | Descrição | Exemplo
------------- | ------------- | ------------- | -------------
 **id** | **Integer** | requerido no PATH | *http://localhost:3001/v1/employee/student/7*

### Status Code

**200** ```OK```

### Exemplo de resposta
```json
{
    "employee": [
        {
            "id": 7,
            "department_id": 1,
            "occupation_id": 1,
            "ethnicity_id": 1,
            "marital_status_id": 1,
            "country_id": 1,
            "address_id": 140,
            "city_id": 1,
            "name": "teste",
            "last_name": "testando",
            "birth_date": null,
            "gender": null,
            "flag_on": null,
            "cpf": null,
            "blood_type": null,
            "organ_donor": null,
            "assumed_name": null,
            "flag_pwd": null,
            "flag_visually": null,
            "flag_hearing": null,
            "flag_physically": null,
            "flag_intellectually": null,
            "description_other_pwd": null,
            "first_job_ctps": null,
            "first_job_public": null,
            "icd": null,
            "created_at": null,
            "updated_at": null,
            "deleted_at": null
        }
    ]
}
```
**404** ```Not Found```

**500** ```Erro interno no servidor```