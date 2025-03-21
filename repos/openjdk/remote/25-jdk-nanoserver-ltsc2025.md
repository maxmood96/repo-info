## `openjdk:25-jdk-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:aaa2f81b3af727f5f985848d14df141c1d4b5b51d4f86e84e6930a05fa0c0dab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3476; amd64

### `openjdk:25-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.3476; amd64

```console
$ docker pull openjdk@sha256:519c8fb2b9438b93c5d924f276146eed307ee343161ecf7274187a4caa07a355
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.0 MB (414017991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f3866e2acef58a78f7cb0877767352f40d9c4f7b95b2deefde7c645cd02b793`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Mar 2025 05:48:38 GMT
RUN Apply image 10.0.26100.3476
# Fri, 21 Mar 2025 18:13:12 GMT
SHELL [cmd /s /c]
# Fri, 21 Mar 2025 18:13:13 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 21 Mar 2025 18:13:14 GMT
USER ContainerAdministrator
# Fri, 21 Mar 2025 18:13:17 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 21 Mar 2025 18:13:19 GMT
USER ContainerUser
# Fri, 21 Mar 2025 18:13:20 GMT
ENV JAVA_VERSION=25-ea+15
# Fri, 21 Mar 2025 18:13:27 GMT
COPY dir:e950963f28ad2c857b90aa9d6a65c8fd16c501192e94c7e71046153717554da9 in C:\openjdk-25 
# Fri, 21 Mar 2025 18:13:34 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 21 Mar 2025 18:13:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6008a43ec9274f69b461027b7f4e2fe6a71387d40072c0b5b4f0dbbfa688d8a5`  
		Last Modified: Wed, 12 Mar 2025 18:43:31 GMT  
		Size: 206.3 MB (206302205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:735775f52d6eaaa6628c87a3ef88b136a7c710c7efe206f53589f81cb05469c1`  
		Last Modified: Fri, 21 Mar 2025 18:13:41 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9111da4106e55db039829e713d5d3f4773afbee5a6fd369f3b3c1e74ff848f8`  
		Last Modified: Fri, 21 Mar 2025 18:13:41 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12bb35d737f68628f448f7b0c1518661fcdff1aaf666970600421b042ef47292`  
		Last Modified: Fri, 21 Mar 2025 18:13:41 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:711c349e58374c2e0699900395f3709c8c2449d81d031e6f10b63b87d1c9be93`  
		Last Modified: Fri, 21 Mar 2025 18:13:41 GMT  
		Size: 75.9 KB (75904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0a8476a77a928f4ce439d0c5efbe80204e4251e6d5cbbcd9083e88f12eb5fb`  
		Last Modified: Fri, 21 Mar 2025 18:13:39 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc974b6e37408dd189909ee6d445cb7227f272eb95b72466ca4dfca593272f48`  
		Last Modified: Fri, 21 Mar 2025 18:13:39 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e186b2735601841540165648cf5d4aeeaf68718f9df674e2c46b534bd704513`  
		Last Modified: Fri, 21 Mar 2025 18:13:51 GMT  
		Size: 207.5 MB (207501808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89d029cf565449debf2a0cf9f0a972d8742685d7f18ba2d7c17f2a6633c38079`  
		Last Modified: Fri, 21 Mar 2025 18:13:39 GMT  
		Size: 131.8 KB (131751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3ca1a2f60e1303d192ef4a2b44957c0ff3d1f4a3aa9d68498cd6cf1ce80e9f1`  
		Last Modified: Fri, 21 Mar 2025 18:13:39 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
