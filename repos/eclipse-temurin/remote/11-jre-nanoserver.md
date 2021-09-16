## `eclipse-temurin:11-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:b29976340c20e4e2c75a95c4751b79b9bfe27c3d0b46db690c1080c3ccfe2255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2183; amd64

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.17763.2183; amd64

```console
$ docker pull eclipse-temurin@sha256:fc82379fe3a3382b330b2d5c1d21457332b2ece03a616a5800ddb49627ef4ab1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.5 MB (145516740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5234568421f98af929abe24bb58eb1214b61cd5f1c74740dad5f3b1c81c7a06b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Sep 2021 03:45:12 GMT
RUN Apply image 1809-amd64
# Wed, 15 Sep 2021 00:38:23 GMT
SHELL [cmd /s /c]
# Wed, 15 Sep 2021 16:30:46 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Wed, 15 Sep 2021 16:30:46 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 15 Sep 2021 16:30:47 GMT
USER ContainerAdministrator
# Wed, 15 Sep 2021 16:30:54 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 Sep 2021 16:30:55 GMT
USER ContainerUser
# Thu, 16 Sep 2021 19:21:54 GMT
COPY dir:37196d51db7ddeb5d9f84ac7a3abd0b4eaec3c6dcffe01db917f682d6ae15f0d in C:\openjdk-11 
# Thu, 16 Sep 2021 19:22:08 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:3585a81ca503e6c63dce938a5606f4171d7461e51000a92054b3f5692786d6c9`  
		Size: 102.7 MB (102703785 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:807d06303c39b2317729754a4c7ad6501e59c16ee464f8f671f9947774f62f72`  
		Last Modified: Wed, 15 Sep 2021 01:10:56 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f0b46abc08dd348231f30302591eb106f2509c46e439c7735e18ffc04a3745`  
		Last Modified: Wed, 15 Sep 2021 16:51:52 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e03a155046076cc9ecbc1c5926012b18963df9b9df8ba86ff3ae4fb54efbbf6`  
		Last Modified: Wed, 15 Sep 2021 16:51:52 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4fdd1cbc2a15e3bb42a7a8c1a542472bcbd16a3c372e40cf219996050315fa3`  
		Last Modified: Wed, 15 Sep 2021 16:51:52 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9056cfe69fb43064c5f5849e7f4328d6cffb416bfa2fdfc39b124fcf2f4cdce0`  
		Last Modified: Wed, 15 Sep 2021 16:51:50 GMT  
		Size: 72.3 KB (72298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0a8abfaee4320d08e0142a1a43aa4330b43ed44f42af47dde036d39183459e`  
		Last Modified: Wed, 15 Sep 2021 16:51:49 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00c270c8e55cb2f330129ec575c15c28347bad20bbd03bf222ee9b358df7eb7`  
		Last Modified: Thu, 16 Sep 2021 19:26:36 GMT  
		Size: 42.7 MB (42686554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23931c2a7aca273b201b83b8274a5217135323ff97aadae7dba4e6aa59f57413`  
		Last Modified: Thu, 16 Sep 2021 19:25:51 GMT  
		Size: 48.4 KB (48366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
