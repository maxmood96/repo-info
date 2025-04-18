## `openjdk:25-ea-nanoserver`

```console
$ docker pull openjdk@sha256:7024bb77660b91c3d2d3c62bd65dd29623fe5212631b8d96f7bf836f9973a969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3781; amd64
	-	windows version 10.0.20348.3566; amd64
	-	windows version 10.0.17763.7249; amd64

### `openjdk:25-ea-nanoserver` - windows version 10.0.26100.3781; amd64

```console
$ docker pull openjdk@sha256:b3c5a529289e1521ff10faa8147cf2c920d7613c4b96f20c13c591f1bf973054
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.9 MB (397924933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6371399bead54ce7ffeac9995775b6dad7b2207b45b431cf54ee0327d7ee120`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 15 Apr 2025 09:41:29 GMT
RUN Apply image 10.0.26100.3781
# Fri, 18 Apr 2025 04:14:50 GMT
SHELL [cmd /s /c]
# Fri, 18 Apr 2025 04:14:52 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 18 Apr 2025 04:14:53 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:14:56 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 18 Apr 2025 04:14:57 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:14:59 GMT
ENV JAVA_VERSION=25-ea+18
# Fri, 18 Apr 2025 04:15:06 GMT
COPY dir:98e2e7765cda338b9693b53f1f8eb40deb194d41cda93e2a54447c0586fe61ce in C:\openjdk-25 
# Fri, 18 Apr 2025 04:15:13 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 18 Apr 2025 04:15:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c012166dfdb57168c954f830d80f494e556a2c597b84901e39aefb605b5e1a02`  
		Last Modified: Thu, 17 Apr 2025 02:52:17 GMT  
		Size: 190.1 MB (190142038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5af37f8ec4ce4332917e40bd09ce21423c309e44af78f581aab39617a99f28d4`  
		Last Modified: Fri, 18 Apr 2025 04:15:21 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb22ef40406d0c0f5f3d054550d9479aede7a89791285369897a587dc091892`  
		Last Modified: Fri, 18 Apr 2025 04:15:21 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b53bfc286c6381f55eaec0263fbb79ae7f0e2a943f810904755de466dd1c2b1`  
		Last Modified: Fri, 18 Apr 2025 04:15:21 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bed770423a284d4616929e06e8c18504476d7d560630d489ca2e764c8b7bf15`  
		Last Modified: Fri, 18 Apr 2025 04:15:21 GMT  
		Size: 76.4 KB (76352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53dbb188c4e58ee41f4b07bcd599a547d6b265892fc1cd9b88929484dcee03d5`  
		Last Modified: Fri, 18 Apr 2025 04:15:19 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce946e80764c13f027343f994c15dc99a9f428b86aa8d90ae0ccd520ed29614a`  
		Last Modified: Fri, 18 Apr 2025 04:15:19 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feed1123be70f61eacd9a02360d8928ef497253ba59c69a27908a8eb62988248`  
		Last Modified: Fri, 18 Apr 2025 04:15:30 GMT  
		Size: 207.6 MB (207583705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a3b21258869107c64db35c9d1c7881a74a1cf9a95c1ef975f2d2aa8f8cdbd85`  
		Last Modified: Fri, 18 Apr 2025 04:15:19 GMT  
		Size: 116.5 KB (116463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0265cb58d1c222e06fcceafb74de3a959a8d3a0401dcd273c69a81c6b0513e6`  
		Last Modified: Fri, 18 Apr 2025 04:15:19 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-nanoserver` - windows version 10.0.20348.3566; amd64

```console
$ docker pull openjdk@sha256:04aed2599f401ce668e22d440b6f117b70752c6cc569d32293dfa39525e11ae0
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.3 MB (330311687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bb71343c4a79c914a36696213d3ed541c628fbbc7ecfbbad08b324f1f430dd0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 16 Apr 2025 03:28:26 GMT
RUN Apply image 10.0.20348.3566
# Fri, 18 Apr 2025 04:20:48 GMT
SHELL [cmd /s /c]
# Fri, 18 Apr 2025 04:20:48 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 18 Apr 2025 04:20:49 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:20:52 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 18 Apr 2025 04:20:52 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:20:53 GMT
ENV JAVA_VERSION=25-ea+18
# Fri, 18 Apr 2025 04:21:00 GMT
COPY dir:98e2e7765cda338b9693b53f1f8eb40deb194d41cda93e2a54447c0586fe61ce in C:\openjdk-25 
# Fri, 18 Apr 2025 04:21:06 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 18 Apr 2025 04:21:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:905464f5b09ec7543cfd4984311153c5e327937892d0e49e145f6b363cf68441`  
		Last Modified: Wed, 16 Apr 2025 23:30:29 GMT  
		Size: 122.5 MB (122539088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:971116681bc5a412624e3675fed90ba346c532e8f8ecf0a3499e75f70e906750`  
		Last Modified: Fri, 18 Apr 2025 04:21:10 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f2173b849b2cc48e171f6dd62c52fee1d459354f513868476e9fd9b607fc020`  
		Last Modified: Fri, 18 Apr 2025 04:21:09 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:356828e71f6c7a6fed76e22b4eea3c78f889237e2ddb8b09bb8b410da8b4744c`  
		Last Modified: Fri, 18 Apr 2025 04:21:10 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f520235c58ac1751f677a943e6e6f9d1d4030b5158fdd05c57a130927b7b52dd`  
		Last Modified: Fri, 18 Apr 2025 04:21:09 GMT  
		Size: 78.6 KB (78574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32f3761ed34dd20da76c57dabd27cbead6161e2c5b13b0f6a823c632aa096b2f`  
		Last Modified: Fri, 18 Apr 2025 04:21:08 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd8b5a63e6faecc493b33219bec94fd4b909a448a294874dd90ac58911d02e4`  
		Last Modified: Fri, 18 Apr 2025 04:21:09 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf56b06ae546ad25f292d8835a191b64a18de2a110eb64349dc50f0da9cc7330`  
		Last Modified: Fri, 18 Apr 2025 04:21:20 GMT  
		Size: 207.6 MB (207580721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a6dbfa0b5d96247cfa4ac77f3b097a214aba6a67c9b61f0dae4a3d929d52d55`  
		Last Modified: Fri, 18 Apr 2025 04:21:09 GMT  
		Size: 107.1 KB (107106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b5391cc228baae84dda5bbbe553c4b329505c9d8c9652604689032700074b8`  
		Last Modified: Fri, 18 Apr 2025 04:21:09 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-nanoserver` - windows version 10.0.17763.7249; amd64

```console
$ docker pull openjdk@sha256:9b388e7725fafec8753b8b92cdc9af283d1146f683470f0fa6d98cbb672e048b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.8 MB (320796212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:275fe6456e565d46c934bfcb153dfc4defc72d214799c38f19ded31f65376bff`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Fri, 18 Apr 2025 04:17:23 GMT
SHELL [cmd /s /c]
# Fri, 18 Apr 2025 04:17:26 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 18 Apr 2025 04:17:26 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:17:29 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 18 Apr 2025 04:17:29 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:17:30 GMT
ENV JAVA_VERSION=25-ea+18
# Fri, 18 Apr 2025 04:17:38 GMT
COPY dir:98e2e7765cda338b9693b53f1f8eb40deb194d41cda93e2a54447c0586fe61ce in C:\openjdk-25 
# Fri, 18 Apr 2025 04:17:43 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 18 Apr 2025 04:17:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885fd0b971cd1883e07073a568e6a4db87086d429cb77fb87ba0aa67e53dfa2a`  
		Last Modified: Fri, 18 Apr 2025 04:17:48 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:630c3b2d0276c33b7a1854c6fe882adbee1317d5ebc90b9a13e408f8a41e2f95`  
		Last Modified: Fri, 18 Apr 2025 04:17:48 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a33eb6aa9ab958edc4c57f1d615b7d585e441c966e020c18ef977d53704557`  
		Last Modified: Fri, 18 Apr 2025 04:17:48 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5062dcb4eafdd7ba4225403a9647e19e9791470dcc81a903547eaf2436efc7`  
		Last Modified: Fri, 18 Apr 2025 04:17:47 GMT  
		Size: 68.8 KB (68805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ea2ac73a1012f89d7a69e763dc0288ce2cca0e0b7da234793299f5e10d257b7`  
		Last Modified: Fri, 18 Apr 2025 04:17:47 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5fced26a42a912cc1d422500f5fae0c3ce0746a45536c179fad22c6a5b023b2`  
		Last Modified: Fri, 18 Apr 2025 04:17:47 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b6229edc3c16e0bf16ca091b0bd654c3edea02427048a87fe7a0ce250215e5a`  
		Last Modified: Fri, 18 Apr 2025 04:17:58 GMT  
		Size: 207.6 MB (207580763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e125292c3d545563f628e838e030096a90a0fd52f1ad70ac36eda2b5a8c8da07`  
		Last Modified: Fri, 18 Apr 2025 04:17:47 GMT  
		Size: 4.4 MB (4388151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:475cd108a90f65bd5b62282feeea97004c46ffaa32628881fc99eeb9e1ef56f8`  
		Last Modified: Fri, 18 Apr 2025 04:17:47 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
