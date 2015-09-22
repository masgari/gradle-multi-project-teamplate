# gradle-multi-project-teamplate
A template for creating Gradle multi projects / multi git-repo with initialiser tasks

## Quick start

* Clone the repository
* Run `./gradlew` to see available tasks
* Edit `settings.gradle`, change project name, modules, etc
  * You can add multiple sub directories (e.g. `'workspace:lib:android:actionbar'`)
* Edit `.gitignore`, add parent folders of sub-projects according to your project layout in `settings.gradle`  
* Run `./gradlew inP`, it will create sub projects with default files
* Run `./gradlew idea` to create idea project

## Customisation
Need more default files? add it to the following map in `initProject` task in `build.gradle`
```groovy
['build.gradle': ["description 'todo:write description for $task.project.name'"],
 'README.md'   : ["# $task.project.name", "Write a short description for `$task.project.name`"],
 '.gitignore'  : ['*.iml', '*.ipr', '*.iws', 'build']
]
```


## TODOs

* Tasks for creating GitHub and BitBucket repositories
* Initialise git repository for each sub project, add remote, commit default files and push "initial commit" to remote
