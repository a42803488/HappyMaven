# HappyMaven
> Provide an easy way to publish your library(AARS or JARS) to Maven repositories

### full module config in library `build.gradle`

```
apply plugin: 'happy-maven'

HappyMaven {
    //Main
    groupId = "engineer.echo"
    artifactId = "happymaven"
    version = "0.0.1"

    packaging = "aar"
    //Repo
    releaseRepoUrl = "https://oss.sonatype.org/service/local/staging/deploy/maven2/"
    snapshotRepoUrl = "https://oss.sonatype.org/content/repositories/snapshots/"
    nexusUserName = "plucky"
    nexusPassword = "xxxxxx"
    //Sign
    signKeyId = "xxx"
    signPassword = "xxxxxx"
    signFile = "~/.gradle/xxx"
    //Pom
    pomName = "HappyMaven"
    pomDesc = "Easy to publish android library."
    pomUrl = "https://github.com/Pluckypan/HappyMaven"
    //Scm
    scmUrl = "https://github.com/Pluckypan/HappyMaven"
    scmConnection = "scm:git@github.com:Pluckypan/HappyMaven.git"
    scmDevConnection = "scm:git@github.com:Pluckypan/HappyMaven.git"
    //License
    licenseName = "The Apache Software License, Version 2.0"
    licenseUrl = "http://www.apache.org/licenses/LICENSE-2.0.txt"
    licenseDist = "repo"
    //Developer
    developerId = "pluckypan"
    developerName = "Plucky Pan"
}
```

### full global config in rootProject `build.gradle`

```
ext.HappyMaven = [
        "GROUP_ID": "engineer.echo",
        "ARTIFACT_ID": "happymaven",
        "VERSION": "0.0.1",

        "PACKAGING": "aar",

        "RELEASE_REPO_URL": "https://oss.sonatype.org/service/local/staging/deploy/maven2/",
        "SNAPSHOT_REPO_URL": "https://oss.sonatype.org/content/repositories/snapshots/",
        "NEXUS_USER_NAME": "plucky",
        "NEXUS_PASSWORD": "xxxxxx",

        "SIGN_KEY_ID": "xxx",
        "SIGN_PASSWORD": "xxxxxx",
        "SIGN_FILE": "~/.gradle/xxx",

        "POM_NAME": "HappyMaven",
        "POM_DESC": "Easy to publish android library.",
        "POM_URL": "https://github.com/Pluckypan/HappyMaven",

        "SCM_URL": "https://github.com/Pluckypan/HappyMaven",
        "SCM_CONNECTION": "scm:git@github.com:Pluckypan/HappyMaven.git",
        "SCM_DEV_CONNECTION": "scm:git@github.com:Pluckypan/HappyMaven.git",

        "LICENSE_NAME": "The Apache Software License, Version 2.0",
        "LICENSE_URL": "http://www.apache.org/licenses/LICENSE-2.0.txt",
        "LICENSE_DIST": "repo",

        "DEVELOPER_ID": "pluckypan",
        "DEVELOPER_NAME": "Plucky Pan"
]
```

### usage
### thanks