The following repo used Github actions to automatically build a project in go and creates a release with release notes.

Usage:
    Any commit that is tagged using semantic versioning convention will trigger the auto build and release. 
    For example, tagging a commit as v1.3, v2.0, v6 ect. Note that the v must be lowercase. 

Builds:
    Once a commit is tagged and pushed, the github action file will run, which will build three files
        1) A windows build
        2) A linux build
        3) A mac build
    There are two versions of the go.yml file. Each uses different commands in the build section. One is for windows powershell commands, and one is for bash commands. 

Automatic Release:
    The go.yml file contains all the github actions for the build and release process. The release portion of the file is created using the comunity action actions/setup-go@v4 (https://github.com/actions/setup-go).

    generate_release_notes is set to true which creates a change log in the release.

