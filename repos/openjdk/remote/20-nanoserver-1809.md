## `openjdk:20-nanoserver-1809`

```console
$ docker pull openjdk@sha256:4cb16cea67b065b87f3276866c45773a1d92f42ef749c80f67c7b17c36cd5dbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3770; amd64

### `openjdk:20-nanoserver-1809` - windows version 10.0.17763.3770; amd64

```console
$ docker pull openjdk@sha256:46bf2fc7de97949caee65805839efde844da21039fdd01c20e5572438fa47561
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.5 MB (303548204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f1aefdecc2316faa960f0cb47e32997b4856c242c444b7797959992257d1b9`
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
# Wed, 14 Dec 2022 03:06:51 GMT
ENV JAVA_VERSION=20-ea+27
# Wed, 14 Dec 2022 03:07:10 GMT
COPY dir:7181a2a10d47fabf483d77137a76741fae853a881eba147494ac530a6ec1d48a in C:\openjdk-20 
# Wed, 14 Dec 2022 03:07:36 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 14 Dec 2022 03:07:37 GMT
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
	-	`sha256:24f406e64c4682939005a0a04e310a446dd0f4781c82e68dd988d749e71197b5`  
		Last Modified: Wed, 14 Dec 2022 08:49:23 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99c399c10876db27c792da9ab8e65e5cd491c18c2eab64016ba73403e1472e2a`  
		Last Modified: Wed, 14 Dec 2022 08:49:46 GMT  
		Size: 193.0 MB (193040578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e259ddb82a3a1f154f82546af9e49cb23fdad8f466b9897a4ad5d3a97d180361`  
		Last Modified: Wed, 14 Dec 2022 08:49:24 GMT  
		Size: 3.8 MB (3764638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c639705848f1284e90e80749a9ff23d7c1211347439d6172b9f52e454711839`  
		Last Modified: Wed, 14 Dec 2022 08:49:23 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
