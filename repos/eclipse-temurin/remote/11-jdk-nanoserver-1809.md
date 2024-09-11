## `eclipse-temurin:11-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:ab15af79e108284c83592a16020a24fb1027cd51ddb2098be564c4ec2f252d04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `eclipse-temurin:11-jdk-nanoserver-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull eclipse-temurin@sha256:6c0681fe6cbf5ddb0b5859abe78653efe8b4046938243a8b2ef54c83f80a00d5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.9 MB (348903230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92023fed24dafd4515e6f604447fa80343633eda17a307d9ff9c2ca0a887f330`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Sep 2024 01:02:10 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 00:38:01 GMT
SHELL [cmd /s /c]
# Wed, 11 Sep 2024 00:44:14 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Wed, 11 Sep 2024 00:44:15 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 11 Sep 2024 00:44:16 GMT
USER ContainerAdministrator
# Wed, 11 Sep 2024 00:44:23 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 11 Sep 2024 00:44:23 GMT
USER ContainerUser
# Wed, 11 Sep 2024 00:44:35 GMT
COPY dir:b5e9d6d7234e205f01359f52140171f1743cc309a4dc5e4224755ced7d18fbfc in C:\openjdk-11 
# Wed, 11 Sep 2024 00:44:46 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 11 Sep 2024 00:44:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a8b325bcb6d89afa770bc0d80d724a7529f3c8bdf940ab5418ad8d6b94fb07f0`  
		Last Modified: Tue, 10 Sep 2024 17:40:58 GMT  
		Size: 155.1 MB (155080848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340318059288cbbdb326eea5b7079e789361251409038a37867d4e395c9404a5`  
		Last Modified: Wed, 11 Sep 2024 01:21:36 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e53aeceeae01cd2700bfa285adb4e8aea90874ae765eb4010292810b4fc66f43`  
		Last Modified: Wed, 11 Sep 2024 01:24:08 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:640dce13e93cb7fa86dee88df1ab878949bb33d05dc627cbafb56cb3d5bb1c4f`  
		Last Modified: Wed, 11 Sep 2024 01:24:08 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07e128bf684c16039994e9b0775db685540cf3f80d2551c91d773b6c2310282`  
		Last Modified: Wed, 11 Sep 2024 01:24:08 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7a9265b2317abc57266c983508810fdd20ea5991b90b5052b5049d2b68767a`  
		Last Modified: Wed, 11 Sep 2024 01:24:06 GMT  
		Size: 68.4 KB (68375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a505867a89571724a5bb7e0d3f76f5ba0e5a65e75970b028efd064065b82102`  
		Last Modified: Wed, 11 Sep 2024 01:24:06 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed645f1632fb08eea9317e04ee61110e60eb61a8bd212be54cc73fa9cf61eb48`  
		Last Modified: Wed, 11 Sep 2024 01:24:22 GMT  
		Size: 193.7 MB (193658298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d176d829920d07b9308f1abf5b52fb0f31950b40266a8e3de70011fea118a9fa`  
		Last Modified: Wed, 11 Sep 2024 01:24:06 GMT  
		Size: 88.9 KB (88865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ac2834b08033380897977b6f29e3937ce1799e9ab02a4d1c4a651d6e2c32681`  
		Last Modified: Wed, 11 Sep 2024 01:24:06 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
