# Crudox: An open-source CRUD generator

## What is it about?
It's an command-line application that will allow developers to solve actual problems. This application generates APIs, creates SQL data dumps and a fully functional web portal to manage your data.

## Why build this project?
I'm tired of writing custom web portals and APIs that would have similar functionalities to manage data. I found this process to be extremely time consuming and thought that I can focus this energy on solving actual problems.

## Aim of this project
- An application that minimize redundant backend development.
- Increased developer productivity.
- Provide flexibility for developer to generate what's required.

## How it works?
The project will only have a `.json` file that consists of the project's backend specifications.

```json
{
    "project_name": "",
    "project_dir": "",
    "project_logo": "",

    "build_config": {
        "base_lang": "",
        "version": "",
        
        "api_config": {
            "is_gen": false,
            "framework": "",
        },

        "data_config": {
            "db_connector": "",
            "db_hostname": "",
            "schema_name": "",
            "is_schema_exists": false,
            "connect_to_db": false,
            "username": "",
            "password": "",
            "gen_tables": false,
            "gen_dump": false,
         },

        "gen_portal": false,
    }
    
    "sections": [
        {
            "section_name": "",
            "table_name": "",
            "is_table_exists": false,
            "fields": [
                {
                    "field_name": "",
                    "data_type": "",
                    "ui_label": "",
                    "el_type": "",
                    "is_editable": false,
                    "is_pk": false,
                    "fk_info": {
                        "is_fk": false,
                        "rel_tbl": "",
                    },
                },
                {...}
            ],
            "options": {
                "create": false,
                "read": false,
                "update": false,
                "delete": false,
            },
        },
        {...}
    ],
}
```

## Tech Stack
This application will be split into two parts.

### Front End
- Electron.js
- HTML
- Javascript
- CSS

### Back End
- Python
- Bash
- Vagrant (For testing purposes)
- LAMP Stack

## Note
Though, this is meant to shave off most of the developer's work, this is not a website builder. It's designed to create a boilerplate version of your backend application. However, the developer can make any changes they wanted to their boilerplate by adding/removing/modifiying functionalities.

## TODO
This list is for me to keep track of my tasks.

### Frontend tasks
- [ ] Create UI Components
- [ ] Generate JSON template with complete specs
- [ ] Execute backend application via system calls

### Backend tasks
- [ ] Parse and test JSON template
- [ ] Create SQL dump
- [ ] Automatically create tables in SQL database
- [ ] Generate API based on language and framework
- [ ] Generate Web Portal with CRUD functionalities