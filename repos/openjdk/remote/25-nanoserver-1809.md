## `openjdk:25-nanoserver-1809`

```console
$ docker pull openjdk@sha256:51e5cda9e50e67efd404f2ab6a3182cabf8316109597ad21d8c72f921b2c0ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `openjdk:25-nanoserver-1809` - windows version 10.0.17763.7249; amd64

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
