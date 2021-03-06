# Git

Functions related to [Git](https://git-scm.com/)


## setGitEnvironmentVariables

Set `GIT_COMMIT` and `GIT_COMMIT_SHORT` environment variables.

#### Example

```groovy
setGitEnvironmentVariables()
```

## getGitBranch
Get name of the current Git Branch.

Returns a Groovy String.

#### Usage

```groovy
def name = getGitBranch()
```

## getGitTags
Get Git Tags for the current commit.

Returns a Groovy Array.

#### Usage

```groovy
def tags = getGitTags()
```

## skipTheBuild

Returns True if the build should be skipped because the string 
"[ci skip]" appears in the HEAD git commit message.

#### Usage

```groovy
if ( skipTheBuild() ) {
    println "Skipping this build"
    return
}
```
