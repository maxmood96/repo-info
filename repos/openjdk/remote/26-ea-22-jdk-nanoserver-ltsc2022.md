## `openjdk:26-ea-22-jdk-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:4b1d123a17c4a424c6582cd9e891e64ccba19517e3c7e1941a92956d380bb071
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `openjdk:26-ea-22-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull openjdk@sha256:adaefb80f05e1271ef29346ee472190ea25a14bb024a07adccc0d94e4ec42f9f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.2 MB (344169959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6adbe427c308cf8bc662fef99049565b454263651b1a06e5ac9f3f329401e1f1`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 22 Oct 2025 21:38:30 GMT
RUN Apply image 10.0.20348.4297
# Mon, 03 Nov 2025 23:32:38 GMT
SHELL [cmd /s /c]
# Mon, 03 Nov 2025 23:32:40 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 03 Nov 2025 23:32:41 GMT
USER ContainerAdministrator
# Mon, 03 Nov 2025 23:32:49 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 03 Nov 2025 23:32:50 GMT
USER ContainerUser
# Mon, 03 Nov 2025 23:32:50 GMT
ENV JAVA_VERSION=26-ea+22
# Mon, 03 Nov 2025 23:33:39 GMT
COPY dir:c90d7d97d7a92e44aebce14c599d37116856dad8a1bf4d9fcb77de537cf1c0aa in C:\openjdk-26 
# Mon, 03 Nov 2025 23:33:46 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 03 Nov 2025 23:33:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2ac1abee018ad49a2f67a19d7f82901aac546affca76c86382db1a855dfcdaa1`  
		Last Modified: Fri, 24 Oct 2025 03:12:47 GMT  
		Size: 122.7 MB (122684063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d39aa1a79c13a1b5dcb0988b9ae98260625673226dddb315b0251ae3a8fec1`  
		Last Modified: Mon, 03 Nov 2025 23:34:15 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a828ff4109bcf661d5cb44fc891554994f740e2cdd7c33c64c511da6fb0737ca`  
		Last Modified: Mon, 03 Nov 2025 23:34:15 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa08519044bb3fdfcce06a4f841ecac205e7d09b3137b70c11901250f85dc45`  
		Last Modified: Mon, 03 Nov 2025 23:34:14 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdd59a7c13f86b6227af3ca276acb9f48e775585555e1286e14fc5b6c8e6f2b`  
		Last Modified: Mon, 03 Nov 2025 23:34:14 GMT  
		Size: 85.0 KB (85032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632988b84057309c9b2c237512b872a66e508b8e979a7a925af1654a089d6c4f`  
		Last Modified: Mon, 03 Nov 2025 23:34:15 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfbe1dce0f6f9014fdf8ce9406e4e51f5d2c6a40dba165ed860415148b72cdda`  
		Last Modified: Mon, 03 Nov 2025 23:34:14 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df99565bccbb691b010cc366f48a1c59fffd8628f9badd728fe5be19f6e662d9`  
		Last Modified: Tue, 04 Nov 2025 01:24:28 GMT  
		Size: 221.3 MB (221284969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6cb1a1e1ce1dcf39fbd59dff5648273b01d254bc0b29b6919b2ff357e27d195`  
		Last Modified: Mon, 03 Nov 2025 23:34:14 GMT  
		Size: 109.5 KB (109490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18f29e29b725c82103f175f720647d67c9830ac89574fd162265ee23ad6cfab8`  
		Last Modified: Mon, 03 Nov 2025 23:34:14 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
