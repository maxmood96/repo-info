## `openjdk:20-nanoserver`

```console
$ docker pull openjdk@sha256:1c9343894888dec9d462ac3f24512322ab50bfc68db73da1f1b23d34daeb552e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3770; amd64

### `openjdk:20-nanoserver` - windows version 10.0.17763.3770; amd64

```console
$ docker pull openjdk@sha256:d18070c9bf7d7fd6db8469ecd8978749b3e3f4e641290f70eae150da6711bdfa
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.6 MB (303575933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4e20f9d684b354abf49704f3c8cf33be4e884a4944ec001062d712374c5727c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 11 Dec 2022 07:45:27 GMT
RUN Apply image 10.0.17763.3770
# Tue, 13 Dec 2022 22:53:34 GMT
SHELL [cmd /s /c]
# Wed, 14 Dec 2022 03:06:29 GMT
ENV JAVA_HOME=C:\openjdk-20
# Wed, 14 Dec 2022 03:06:30 GMT
USER ContainerAdministrator
# Wed, 14 Dec 2022 03:06:49 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 14 Dec 2022 03:06:50 GMT
USER ContainerUser
# Fri, 23 Dec 2022 01:26:20 GMT
ENV JAVA_VERSION=20-ea+29
# Fri, 23 Dec 2022 01:26:42 GMT
COPY dir:0607ae4550c43cbf3109fc2f0d804df5cbc254c5417640a86403cfd5b37f4207 in C:\openjdk-20 
# Fri, 23 Dec 2022 01:27:10 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 23 Dec 2022 01:27:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7442c6014cd8a0820e2009cde1268b6ce4b8f86bc314ba287cc01fab93174fd6`  
		Last Modified: Tue, 13 Dec 2022 23:57:28 GMT  
		Size: 106.7 MB (106671057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8fe06cbef5ac46e54edd743daf1bc2bfa36b294c7ce9104837061c41a4bde7b`  
		Last Modified: Tue, 13 Dec 2022 23:57:01 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8407ccbdbd1b98118842fe985781ff7ccce1a4a02763ce3c7bc5182f0a6cd7be`  
		Last Modified: Wed, 14 Dec 2022 08:49:25 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d10a11487b55c583a71e65de52b66756da77520bd91e60c286f53bc275c4776e`  
		Last Modified: Wed, 14 Dec 2022 08:49:25 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b8c7b08a7b6bda536e75dce577a2de479c5b5ac157ae753b5d69a3246b69fc`  
		Last Modified: Wed, 14 Dec 2022 08:49:25 GMT  
		Size: 65.0 KB (65047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4410bf6b8361419a87afad95e1191ea2013d36ec41631d7c8a157b17687c9da4`  
		Last Modified: Wed, 14 Dec 2022 08:49:23 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cbaf6f6e632913a87d9412b546388bdc4ed61492cefd58d77b0a1af6d9b9518`  
		Last Modified: Fri, 23 Dec 2022 02:23:12 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:279ffdbe152b99b6e2754f4fd280ee3d156c74ade98e8a6f6438b123635658c0`  
		Last Modified: Fri, 23 Dec 2022 02:23:37 GMT  
		Size: 193.1 MB (193068026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d8f586d32b074914deeea7381c2a5ef503a4cdc823825626e0646bf531673a`  
		Last Modified: Fri, 23 Dec 2022 02:23:14 GMT  
		Size: 3.8 MB (3764895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5047c802d5e94abf1d7fcca99647c1849756d47f39dcc0d7c7ff7be0758324fb`  
		Last Modified: Fri, 23 Dec 2022 02:23:12 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
