# ECSE3038 Lab 2

This Lab tested our ability to make HTTP Requests via an API platform. 

## Aim

To become more familiar with the FastAPI python framework. Students will be asked to create functions that will used to handle incoming HTTP requests.

## Requirements

Students should create a repository on GitHub and push code to this repository. Students should also make changes to the code on their local machine and commit these changes to the repository.

The server side application that students will build should allow for the functionality of the demo site at [https://ecse-week3-demo.netlify.app/](https://ecse-week3-demo.netlify.app/).

## Outline

In the Python programming language, you are expected to design and implement a simple script that performs actions as defined be the requirements below. 

Addition of any further functionality is up to you but the following functions must be included:

A todo object looks like this

```json
{
	"id": {auto generated id: int},
	"todoText": {text describing todo item: str},
	"isDone": {status of the todo: bool}
}
```

1. Write a function, `update_todo_by_id()`, that handles incoming `PATCH` requests from the demo site. The function should accept the ID of the todo that should be updated and a todo request object that has the desired changes. Your function should then search for the matching todo object in your todo list and update it with the received changes.
    
    The frontend application sends a request that follows this format:
    
    ```
    PATCH /todos/{id} HTTP/1.1
    Host: http://localhost:8000
    Content-Type: application/json
    Content-Length: 18
    
    { "isDone": true }
    ```
    
    Your PATCH handler should respond with the entire todo object as it exists after being updated along with the `200 OK` status code. 
    
    If there exists no todo object with the provided ID, the PATCH handler should respond with a `404 Not Found` status code.
    
2. Write a function, `delete_todo_by_id()`, that handles incoming `DELETE` requests from the demo site. The function should accept the ID of the todo that should be deleted. Your function should then search for the matching todo object in your todo list and remove it.
    
    The frontend application sends a request that follows this format:
    
    ```
    DELETE /todos/{id} HTTP/1.1
    Host: http://localhost:8000
    Content-Type: application/json
    ```
    
    Your DELETE handler should respond with a JSON object indicating that an object has been successfully deleted along with the `200 OK` status code. 
    
    If there exists no todo object with the provided ID, the DELETE handler should respond with a `404 Not Found` status code.
    

## Note

The inclusion of a README.md is mandatory. Your README.md should be located in the root of your repository.  

The README should contain: 

- A summary the expected behaviour of each function included in your code.
- The reason the code was written (eg. for the purpose of an assignment, etc).
- The name and a short description of your favourite pokémon.

The README.md should be properly formatted with the markdown syntax.

A .gitignore is mandatory. Your .gitignore should be located in the root of your repository. 

The .gitignore should contain rules that prevent unwanted or unnecessary files and folders from being uploaded to GitHub. If no such files exist in the repo, the file may be let blank but should still be included in the repo.

A file called `requirements.txt` must also be included in your repository. This file should outline a list of python packages used in your script along with the version of each package.

There is no maximum number of commits that can be made the repo. There should, however, be at least 2 commits since each function after the first should be implemented and commit one at a time. 

Each commit should be accompanied by a short and meaningful commit message that outlines what changes were made.

## My Favourite Pokémon

# Torchic
![Alt text](https://assets.pokemon.com/assets/cms2/img/pokedex/full/255.png "Torchic")

orchic (Japanese: アチャモ Achamo) is a Fire-type Pokémon introduced in Generation III.

It evolves into Combusken starting at level 16, which evolves into Blaziken starting at level 36.

Along with Treecko and Mudkip, Torchic is one of three starter Pokémon of Hoenn available at the beginning of Pokémon Ruby, Sapphire, Emerald, Omega Ruby, and Alpha Sapphire.