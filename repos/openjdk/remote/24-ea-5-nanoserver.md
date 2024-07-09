## `openjdk:24-ea-5-nanoserver`

```console
$ docker pull openjdk@sha256:6dda014b0640dd37cb2872c5bc0ef92609c990c1c6de174e036193e7b172841d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `openjdk:24-ea-5-nanoserver` - windows version 10.0.17763.5936; amd64

```console
$ docker pull openjdk@sha256:c4c4bcb6e1f511777354236ae546f0741689630205eaf59cd8dafa012de8e0c6
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.4 MB (366440305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad1e4ef1ab99b03484ec7f46681fd03b150aac71866b89b40cdcd601303857a8`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Mon, 08 Jul 2024 21:49:33 GMT
SHELL [cmd /s /c]
# Mon, 08 Jul 2024 21:49:34 GMT
ENV JAVA_HOME=C:\openjdk-24
# Mon, 08 Jul 2024 21:49:35 GMT
USER ContainerAdministrator
# Mon, 08 Jul 2024 21:49:38 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 08 Jul 2024 21:49:39 GMT
USER ContainerUser
# Mon, 08 Jul 2024 21:49:40 GMT
ENV JAVA_VERSION=24-ea+5
# Mon, 08 Jul 2024 21:49:48 GMT
COPY dir:42629391e472e10c3a5c0e61498da2606abe04ae5ffbc2871bee3fab2500b46f in C:\openjdk-24 
# Mon, 08 Jul 2024 21:49:57 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 08 Jul 2024 21:49:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4f703ea968d7f7434cf61e5d835cb3c507a6364ff8c7b3b96b73391b22115615`  
		Last Modified: Tue, 11 Jun 2024 20:35:02 GMT  
		Size: 155.0 MB (155033193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:313211b46d9945106691743dd4e3912c9a7db72db663ae117a253379cc67c40c`  
		Last Modified: Mon, 08 Jul 2024 21:50:05 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c5acbc73129aa6ca80a21a8c3f771919f08be342af65497f2acdd4bf176821`  
		Last Modified: Mon, 08 Jul 2024 21:50:04 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b1562533dc54635a923d4be62f03cfed076df6aa2e5678f13cde88932fc7f6`  
		Last Modified: Mon, 08 Jul 2024 21:50:04 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9bcb2060441834b612a70df2f0df11d3a7e5dc186ffa2f993d6ca7e6590f20`  
		Last Modified: Mon, 08 Jul 2024 21:50:04 GMT  
		Size: 67.1 KB (67124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f8d38ef8b5b67880b6f7973b1c986601702358dd99b70bd80e03dc1126e7049`  
		Last Modified: Mon, 08 Jul 2024 21:50:02 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf3ace8c25c86337ebbd1241f0959db48357e8b5040edd1d8e3c7f9ebdf4f20a`  
		Last Modified: Mon, 08 Jul 2024 21:50:02 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65842f0258e139cbf2236c64bfe0e7e7f5276fa120b222a62e14772870177de2`  
		Last Modified: Mon, 08 Jul 2024 21:50:13 GMT  
		Size: 206.2 MB (206202782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf65272b9dad67a942b8deddee941d6bb062c5dcd0dc5872739f8ddb1353c25`  
		Last Modified: Mon, 08 Jul 2024 21:50:03 GMT  
		Size: 5.1 MB (5130971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc67526b718876e98faa1a0e0daf9f982a87bc7eb07122cf06fadbacbdd444c`  
		Last Modified: Mon, 08 Jul 2024 21:50:02 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
