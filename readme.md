# API Tests

This project contains automated API tests for list endpoint [TMDB](https://developers.themoviedb.org/4/list/get-list) api. The tool used to write the tests is [Tavern](https://tavern.readthedocs.io/en/latest/)

## Prerequisites

Docker and docker compose should be installed

## Steps to run

1. Clone this repository.
2. Open terminal and navigate to the project root directory. Run the below command.

```bash
docker-compose run api-tests
```
3. The results of the tests would be visible in terminal window after test run is finished.

## Framework Explanation

This framework is built in [tavern](https://tavern.readthedocs.io/en/latest/)
Tavern is very lightweight and easy to use tool for Rest Api test automation, it uses pytest under the hood and all the capabilities of pytest can be extended by tavern.  
In tavern, the tests follow simple yaml syntax where request is sent and response is validated. The command to run the tests in given in docker-compose.yaml file in “api-tests” service.  
By default all the files which are named in the format “test_*.tavern.yaml” will be run by tavern.
## Directory Structure

In this project the tests are present inside ApiTests directory.  
The tests are designed in yaml files and those are names in the format "test_*.tavern.yaml".  
The "common.yaml" file contains the list if global variables which are used in the tests.  
The "requirements.txt" file contains list of python modules which are required to run the project.  
In project root there is a docker-compose.yaml file which conta