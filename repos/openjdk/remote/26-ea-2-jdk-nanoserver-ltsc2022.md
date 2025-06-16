## `openjdk:26-ea-2-jdk-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:34482a4296b7e84fa624a95f322c9154c300d51ea5136b8d1ce87465a5a88c18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `openjdk:26-ea-2-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull openjdk@sha256:440479ddb5224bad39d3ed6fdd7e884561a05c334e32af18278d67ead3a71128
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.1 MB (341079437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b81f541cc9bfa28e5c64f4d98385944f9c822bbedd127b3b9e7303a96415600a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Jun 2025 00:43:46 GMT
RUN Apply image 10.0.20348.3807
# Mon, 16 Jun 2025 19:18:26 GMT
SHELL [cmd /s /c]
# Mon, 16 Jun 2025 19:18:27 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 16 Jun 2025 19:18:28 GMT
USER ContainerAdministrator
# Mon, 16 Jun 2025 19:18:30 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 16 Jun 2025 19:18:30 GMT
USER ContainerUser
# Mon, 16 Jun 2025 19:18:31 GMT
ENV JAVA_VERSION=26-ea+2
# Mon, 16 Jun 2025 19:18:39 GMT
COPY dir:fc8b81948364d0e39d95d5a838d5c247253584bf16df7749b143abef5cfa930b in C:\openjdk-26 
# Mon, 16 Jun 2025 19:18:44 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 16 Jun 2025 19:18:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:96acbf1c6d5b6cc37517502ecbb6a1d2eb55b7615b696401ead868c97a971964`  
		Last Modified: Tue, 10 Jun 2025 20:17:56 GMT  
		Size: 122.5 MB (122540534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260398586abcb9848f4fd97ee01274c7f526e8a01cfa0470a28b5bf6995d69cd`  
		Last Modified: Mon, 16 Jun 2025 19:19:23 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48609599baa2ae25f12468db25e25e354ee5aff2cbe52a47d7b291ed9441f298`  
		Last Modified: Mon, 16 Jun 2025 19:19:24 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5223daad8a11a29eac07afd6db5b93bac6ca30ed6db3157e210c8a68842932ff`  
		Last Modified: Mon, 16 Jun 2025 19:19:25 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c8a0113cfb97d8ed842dc75bb216e5961469da74f97a022d2ac123676b406f`  
		Last Modified: Mon, 16 Jun 2025 19:19:25 GMT  
		Size: 78.4 KB (78437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d96cc896b96475ee28d6968df16a98b1f45ce3767898f91074d65faf1043b526`  
		Last Modified: Mon, 16 Jun 2025 19:19:25 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f3c591eb7d7e0c0a7fa9dd1d1a12269730010b282c2115ec58360ca1f2acb84`  
		Last Modified: Mon, 16 Jun 2025 19:19:25 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb1672229c0635001d9242e44fa60c777235af12fdd90783984a499183796ab`  
		Last Modified: Mon, 16 Jun 2025 21:24:51 GMT  
		Size: 218.3 MB (218347405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2ee912110c2079da782ebc2c7a405910214797a9344fb2c2c2d41ed4d22d33b`  
		Last Modified: Mon, 16 Jun 2025 19:19:20 GMT  
		Size: 106.9 KB (106896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef1ad13bf95d10b862d8cf1244710ec5e4b27e2f65c88d36b4bff4517be6980`  
		Last Modified: Mon, 16 Jun 2025 19:19:20 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
