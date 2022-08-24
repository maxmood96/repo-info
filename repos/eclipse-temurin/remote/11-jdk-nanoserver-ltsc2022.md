## `eclipse-temurin:11-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:f5aa84fb0c3c866859aaa1e9177becf38088660e263a03a43c119fb4c99ca038
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.887; amd64

### `eclipse-temurin:11-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.887; amd64

```console
$ docker pull eclipse-temurin@sha256:f62140294f532014b035964278811687e8544f3f940526a75eaf26aecc77b1dd
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 MB (310627166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:492fc7d14d11d2bbcc2aeeea4a4d1a4c37e2c8679d3f1231656e567dc9e08210`
-	Default Command: `["jshell"]`
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
# Wed, 24 Aug 2022 19:39:28 GMT
COPY dir:b7b3112beefc8be2dd5c6a3897a52ba756c9a344294f20db387fa022b341211c in C:\openjdk-11 
# Wed, 24 Aug 2022 19:39:49 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 24 Aug 2022 19:39:51 GMT
CMD ["jshell"]
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
	-	`sha256:8172543552474ca4dda8935d13c0f0b01e5299581a4f13ab26192f0760485bb7`  
		Last Modified: Wed, 24 Aug 2022 19:52:10 GMT  
		Size: 192.4 MB (192371224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b69400d0d37e581a7007cd39970ca0414f27460e8501d72e09fbb5b7b85c8e`  
		Last Modified: Wed, 24 Aug 2022 19:51:47 GMT  
		Size: 75.9 KB (75902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84661da252ae3c82036acbf2f07fe606fdf1fa7effe62d56bd8399007f46cdbf`  
		Last Modified: Wed, 24 Aug 2022 19:51:47 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
