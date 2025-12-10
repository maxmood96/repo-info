## `eclipse-temurin:17-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:88aeef84cb9acf4ec0b7bc1b6649eb0a0e0ebe9d9bd664f35b339ff47403bb48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7462; amd64
	-	windows version 10.0.20348.4529; amd64

### `eclipse-temurin:17-nanoserver` - windows version 10.0.26100.7462; amd64

```console
$ docker pull eclipse-temurin@sha256:0f9fa3c0b85ec14d13ec6791cd496d14b01ce74c01a84468d5cb7bbd5bae298e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.6 MB (386575356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e206f3ea1e682eb11d0af5486ec6f26a2de4e0c40aab4ae157afb46728b92c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Dec 2025 21:31:34 GMT
RUN Apply image 10.0.26100.7462
# Tue, 09 Dec 2025 21:12:53 GMT
SHELL [cmd /s /c]
# Tue, 09 Dec 2025 21:14:34 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Tue, 09 Dec 2025 21:14:35 GMT
ENV JAVA_HOME=C:\openjdk-17
# Tue, 09 Dec 2025 21:14:36 GMT
USER ContainerAdministrator
# Tue, 09 Dec 2025 21:14:37 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 09 Dec 2025 21:14:37 GMT
USER ContainerUser
# Tue, 09 Dec 2025 21:14:52 GMT
COPY dir:2018c1c9eb6dc671bed9b2018ab32e648d405ad10a017a184613d399d49818ed in C:\openjdk-17 
# Tue, 09 Dec 2025 21:14:57 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 09 Dec 2025 21:14:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1a092205b76ca656d8483e99445def9f0619cb3acb2688bf9a33244c43ad44ce`  
		Last Modified: Tue, 09 Dec 2025 22:15:12 GMT  
		Size: 198.9 MB (198873947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba3aa2fd9c43d5870304ea449c22f4fbf73f16c064a13e04297c92a2a200461b`  
		Last Modified: Tue, 09 Dec 2025 21:14:09 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9e89706b6f32a44908cec4e6210043fbe5fa5031525f314c3b83fb83bcafa7c`  
		Last Modified: Tue, 09 Dec 2025 21:15:30 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fec0a2242ec1c912c028ab0fdc2b85bdf25cdcac51e4184563a44c5daf8f3b0`  
		Last Modified: Tue, 09 Dec 2025 21:15:30 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3254eb37855a76501b150c8d78408b9941900f20a865ece2923dd378c115c52e`  
		Last Modified: Tue, 09 Dec 2025 21:15:30 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e629f8b10edf40dc4757c5f6ceebc4cce99cc13477770a1e9f6b2fb5e5976972`  
		Last Modified: Tue, 09 Dec 2025 21:15:31 GMT  
		Size: 71.9 KB (71928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f56e6a12bc9f6c9ca6878fac8e4fc80ea2d72b11e74994ef51dba6394af089b9`  
		Last Modified: Tue, 09 Dec 2025 21:15:30 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e2d335f904eb9cfed57098659ddaadc645d3b572c4f19d8bea4e99d97d6b12f`  
		Last Modified: Tue, 09 Dec 2025 21:15:45 GMT  
		Size: 187.5 MB (187511029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50a2e242c83316d1146395b849323c674d1008126c3d1cbc9c17a1c7c71b24e`  
		Last Modified: Tue, 09 Dec 2025 21:15:30 GMT  
		Size: 112.1 KB (112123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:721f40ebb999508bc9aa89301d5bc205c10aa6f536207474eff0cde0362900b0`  
		Last Modified: Tue, 09 Dec 2025 21:15:30 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-nanoserver` - windows version 10.0.20348.4529; amd64

```console
$ docker pull eclipse-temurin@sha256:375eafa2e02e31a9491b5d517e7662808c29751ff89187d6b55b0e5c0556efce
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.1 MB (314070388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b34df60b1fb9da8d9c8b842a3b97879c552083945b7ae9fd920aa8a2a40928c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Tue, 09 Dec 2025 21:12:58 GMT
SHELL [cmd /s /c]
# Tue, 09 Dec 2025 21:12:58 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Tue, 09 Dec 2025 21:12:59 GMT
ENV JAVA_HOME=C:\openjdk-17
# Tue, 09 Dec 2025 21:12:59 GMT
USER ContainerAdministrator
# Tue, 09 Dec 2025 21:13:00 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 09 Dec 2025 21:13:01 GMT
USER ContainerUser
# Tue, 09 Dec 2025 21:13:08 GMT
COPY dir:2018c1c9eb6dc671bed9b2018ab32e648d405ad10a017a184613d399d49818ed in C:\openjdk-17 
# Tue, 09 Dec 2025 21:13:13 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 09 Dec 2025 21:13:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6081bd6804178009789fc41fc7b5b028534888b64e10cd0ca092b3f3c75127c3`  
		Last Modified: Tue, 09 Dec 2025 21:13:37 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b7fdd2b791f338238da4b276ca4940b2299ab4527f7f75f5a490633541c898`  
		Last Modified: Tue, 09 Dec 2025 21:13:37 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73358df318e7799470cc73b06da29fe0887a82582d6f307abcb79556daa1dc25`  
		Last Modified: Tue, 09 Dec 2025 21:13:37 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee69fcb07bd76ece3d3e752a3618abfd202e309bfc86686fd584b57e3716ce5`  
		Last Modified: Tue, 09 Dec 2025 21:13:37 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23ed029240da3a6c65445259ab3b49d7cfd3cbc4a93640b0f35f0bba0584fda`  
		Last Modified: Tue, 09 Dec 2025 21:13:37 GMT  
		Size: 76.6 KB (76592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad819d103429df1ab3f3fe8bf7b0a4f2df07416fd191affb0cb74fbf44fdae4`  
		Last Modified: Tue, 09 Dec 2025 21:13:37 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0f60f444d406ae990002c5b1c286ec5ab7255e5c1cbd745e0c1a337dc1244c`  
		Last Modified: Tue, 09 Dec 2025 21:13:50 GMT  
		Size: 187.5 MB (187511015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb7646e0baa7104bcd94b3832ee561daf131ae1b02a366b5af6eef888fed789`  
		Last Modified: Tue, 09 Dec 2025 21:13:37 GMT  
		Size: 118.1 KB (118070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ee39ed10d35941b33b676875246c0f8d62b9fea31c66190adbfedb048221ae`  
		Last Modified: Tue, 09 Dec 2025 21:13:37 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
