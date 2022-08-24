## `eclipse-temurin:11-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:b3ce75ea5b37b317a9acd05c591fefef12b645ebfa151ecdbe30e1a675aa543f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.887; amd64

### `eclipse-temurin:11-jre-nanoserver-ltsc2022` - windows version 10.0.20348.887; amd64

```console
$ docker pull eclipse-temurin@sha256:2c8fd525d284e274080fa28082570a2a24e547fac76cf96dce85e89222dcbdee
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.1 MB (161145466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ae19e014fcebde704a2fd1f16ee4511f3052c4f7312699802c8dd1aa64142b6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Aug 2022 18:05:23 GMT
RUN Apply image 10.0.20348.887
# Wed, 10 Aug 2022 16:28:17 GMT
SHELL [cmd /s /c]
# Wed, 24 Aug 2022 19:38:52 GMT
ENV JAVA_VERSION=jdk-11.0.16.1+1
# Wed, 24 Aug 2022 19:38:54 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 24 Aug 2022 19:38:55 GMT
USER ContainerAdministrator
# Wed, 24 Aug 2022 19:39:10 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 24 Aug 2022 19:39:12 GMT
USER ContainerUser
# Wed, 24 Aug 2022 19:40:12 GMT
COPY dir:b650de7fc0e3b0755f26a7348890f8f5a4e1b6ed07c2d2df82fc07e7eb59e165 in C:\openjdk-11 
# Wed, 24 Aug 2022 19:40:28 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:2ebf439f800cd4c1fccaf4a0545e6bff60caa5141295c8ab81f6c525073c423d`  
		Size: 118.1 MB (118088450 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5f1e06146ab0490d235fe89786637467a4b71853ee428e8740ea6efbc536c47c`  
		Last Modified: Wed, 10 Aug 2022 16:48:40 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:552df7312ccb2e6d922d6f01e4724f3b3d6476ea66250954b2fca74f99cbef64`  
		Last Modified: Wed, 24 Aug 2022 19:51:49 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736c1676086df0f6671638cbaffea34375022178641fa815899599219e34505d`  
		Last Modified: Wed, 24 Aug 2022 19:51:49 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad4bf431c912d3f6a0ac493da931e2511889e92c89cca4fb739323c81e786c4a`  
		Last Modified: Wed, 24 Aug 2022 19:51:49 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:050e66f4a83838f72987c29f696c98c331ffbc0eba773d77b29d81b6c63c2024`  
		Last Modified: Wed, 24 Aug 2022 19:51:47 GMT  
		Size: 84.6 KB (84612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b38c9bea5c240256e7483d2c0b07d7404ec0d1681ff4707c11583372a76524`  
		Last Modified: Wed, 24 Aug 2022 19:51:47 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5801b2f910ad64ac19a0193fa30210b2bec4d3de472669e47db520304158f7`  
		Last Modified: Wed, 24 Aug 2022 19:52:32 GMT  
		Size: 42.9 MB (42904502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12aa788296ebdeb3e377f981c12c714e70fdaffd6908fab68b8ca9b14113679a`  
		Last Modified: Wed, 24 Aug 2022 19:52:23 GMT  
		Size: 62.1 KB (62084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
