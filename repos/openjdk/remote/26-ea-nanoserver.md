## `openjdk:26-ea-nanoserver`

```console
$ docker pull openjdk@sha256:660a775ae91097c4f91718e40b9e641f145b838df9fee7f00e9b3795cff02cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6905; amd64
	-	windows version 10.0.20348.4297; amd64

### `openjdk:26-ea-nanoserver` - windows version 10.0.26100.6905; amd64

```console
$ docker pull openjdk@sha256:10cf4642ed39691634dcb5eb5e13c1ff5ebe46a361b961daba33a0a245760f00
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.5 MB (415493350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aaf7ed1604c8a547de3c5f9ab8851b8fa2605ce04992101c9c4f212a0014d37`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 22 Oct 2025 07:22:01 GMT
RUN Apply image 10.0.26100.6905
# Mon, 03 Nov 2025 23:12:26 GMT
SHELL [cmd /s /c]
# Mon, 03 Nov 2025 23:12:27 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 03 Nov 2025 23:12:27 GMT
USER ContainerAdministrator
# Mon, 03 Nov 2025 23:12:38 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 03 Nov 2025 23:12:38 GMT
USER ContainerUser
# Mon, 03 Nov 2025 23:12:39 GMT
ENV JAVA_VERSION=26-ea+22
# Mon, 03 Nov 2025 23:13:21 GMT
COPY dir:c90d7d97d7a92e44aebce14c599d37116856dad8a1bf4d9fcb77de537cf1c0aa in C:\openjdk-26 
# Mon, 03 Nov 2025 23:13:28 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 03 Nov 2025 23:13:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9188956580c47f583c927f17e42f8825823890544237141f21ca4ef10ea55e60`  
		Last Modified: Fri, 24 Oct 2025 11:13:56 GMT  
		Size: 194.0 MB (194029378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a5120a421c2f9dc1a3e48a8c123c321633009cb902a8d361406c1be69b9ca9`  
		Last Modified: Mon, 03 Nov 2025 23:13:54 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8f78e528bb11641cdc411b1c941ac293654bdf1ea657f844dab44e6c6f76e1`  
		Last Modified: Mon, 03 Nov 2025 23:13:54 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:163f3e483e56468b07f8679c83792f88a26d6e5da124a46ac854b8bfbae34867`  
		Last Modified: Mon, 03 Nov 2025 23:13:54 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb073090ae38dbceff4e8212a2f1b534c12e2ebc36afd51184f9090af3edd9da`  
		Last Modified: Mon, 03 Nov 2025 23:13:54 GMT  
		Size: 70.6 KB (70629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d9455c85387ecde22e9e90f728c03f0f056b3d3169a445b38d88f21949e840`  
		Last Modified: Mon, 03 Nov 2025 23:13:54 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b2c8a2718374c880eb8026a5159e44fa6513e6e7aee5852ad0bcddd637945a`  
		Last Modified: Mon, 03 Nov 2025 23:13:54 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e455d72a60c01996d736f8155b3ec5110589d0dcc4eaf03fcafcf4d5f226727a`  
		Last Modified: Tue, 04 Nov 2025 01:23:42 GMT  
		Size: 221.3 MB (221284776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fae4ce72fe5a82b109eb5d016a212f71ef5f1cb3f610214953c3077a4828050a`  
		Last Modified: Mon, 03 Nov 2025 23:13:54 GMT  
		Size: 102.2 KB (102202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30e1919af35e1339fd79914728ae1642c4a9ef1913ed1529acb71cf0f6eabea7`  
		Last Modified: Mon, 03 Nov 2025 23:13:54 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:26-ea-nanoserver` - windows version 10.0.20348.4297; amd64

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
