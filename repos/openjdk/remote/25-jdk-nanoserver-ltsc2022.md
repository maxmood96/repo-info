## `openjdk:25-jdk-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:bfc8cfdcfae3113c3247faf1b61d278be609760d7131684041963a0984d54a74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `openjdk:25-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull openjdk@sha256:c77dbb3053fb47b73f9731046399d0489984ea983bca79fa673131e950bb39ea
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.4 MB (328356691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7870d05b6185e4472da52f0dcb479b9d19cd290e19b2f7eebf4173eae11f387`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 06 Mar 2025 10:30:39 GMT
RUN Apply image 10.0.20348.3328
# Mon, 17 Mar 2025 22:24:28 GMT
SHELL [cmd /s /c]
# Mon, 17 Mar 2025 22:24:29 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 17 Mar 2025 22:24:30 GMT
USER ContainerAdministrator
# Mon, 17 Mar 2025 22:24:33 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 17 Mar 2025 22:24:34 GMT
USER ContainerUser
# Mon, 17 Mar 2025 22:24:34 GMT
ENV JAVA_VERSION=25-ea+14
# Mon, 17 Mar 2025 22:24:43 GMT
COPY dir:3bbdecdaf44fd794a45fa39cf7b31efe4cc2d91c5e3e7c4c5333407317959149 in C:\openjdk-25 
# Mon, 17 Mar 2025 22:24:48 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 17 Mar 2025 22:24:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:47ec0d45ee7716f773dfebb62d84eb3893d3af9baf9c799960566b016a17e330`  
		Last Modified: Wed, 12 Mar 2025 02:22:56 GMT  
		Size: 120.7 MB (120695547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d56818458d0087e4b37795636958615ab9394e7ae440b701fe494df5f72c06`  
		Last Modified: Mon, 17 Mar 2025 22:24:56 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acd0c7d30d7e41d27ba9c6e225f08596dfb466b767e9ee422763d030a09833ab`  
		Last Modified: Mon, 17 Mar 2025 22:24:55 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2117d53188dda548dba210953c298809c8030a7cc4d29c07d43296581b00b68`  
		Last Modified: Mon, 17 Mar 2025 22:24:55 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ce3d0bcaa9bb541698d77e9b873eeb2e07fa7e64a8602cef452d9764c050a5`  
		Last Modified: Mon, 17 Mar 2025 22:24:55 GMT  
		Size: 78.1 KB (78136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b173a73312a2a4ba227df7bd5f7bfeeea243c6f40b79518909c50eececd36341`  
		Last Modified: Mon, 17 Mar 2025 22:24:53 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8e9d21af0e47e5724fc827df149dcf485282a9a1c615b4ab115113a3c980d2c`  
		Last Modified: Mon, 17 Mar 2025 22:24:53 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf593ddf7ee51a09389814b30562662aec6d4383b582ff6c3e877191567d373b`  
		Last Modified: Mon, 17 Mar 2025 22:25:05 GMT  
		Size: 207.5 MB (207469416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe50f2590900ffcf1afc6ece81affcd587b6b68ddc54c340efa81c06eb6a646`  
		Last Modified: Mon, 17 Mar 2025 22:24:54 GMT  
		Size: 107.2 KB (107153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aac09d8e0f0d5ae5926ae0811524df6530f8e6c58d572e59f164139806ef9294`  
		Last Modified: Mon, 17 Mar 2025 22:24:53 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
