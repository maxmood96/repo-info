## `eclipse-temurin:21-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:5be03393e8fc75ece1e7bfb51b36d313cd563de83b28fc8145e2f5322a2cc5ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32860; amd64
	-	windows version 10.0.20348.5139; amd64

### `eclipse-temurin:21-jdk-nanoserver` - windows version 10.0.26100.32860; amd64

```console
$ docker pull eclipse-temurin@sha256:2f0b3a7db0839b2d9c915e55436b055fe051bd9989994ac0d0cf0b7364d845e5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.8 MB (401799718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f461aeed653e2463d2abb3aa48451189219f9162730db9770d8bac42e6544ab`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 10 May 2026 09:46:02 GMT
RUN Apply image 10.0.26100.32860
# Wed, 13 May 2026 00:29:19 GMT
SHELL [cmd /s /c]
# Wed, 13 May 2026 00:29:20 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Wed, 13 May 2026 00:29:20 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 13 May 2026 00:29:21 GMT
USER ContainerAdministrator
# Wed, 13 May 2026 00:29:24 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 May 2026 00:29:24 GMT
USER ContainerUser
# Wed, 13 May 2026 00:29:35 GMT
COPY dir:be4fce80d476aa164b4bdafca77eddb646da4c27d929101014e2067a583f974e in C:\openjdk-21 
# Wed, 13 May 2026 00:29:40 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 13 May 2026 00:29:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:34ab6476d71f2d23d05a00ac439000ba4c19d17e5c66f15efbe329ed79bba2bf`  
		Last Modified: Tue, 12 May 2026 22:29:47 GMT  
		Size: 199.7 MB (199739001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4035ec944d63267a8e4aa5146a939b10f7a9d491c5a3495bfa8c55ce5767b0f4`  
		Last Modified: Wed, 13 May 2026 00:29:47 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdd5dd9173397197d6504dbd9b90d30570fe6f9ced841ba8fdcfcdc57131f29b`  
		Last Modified: Wed, 13 May 2026 00:29:47 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01850fd519469e9c93610ebeae645ad6c7f01a109de4ddfd921b8af3e82bf279`  
		Last Modified: Wed, 13 May 2026 00:29:46 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127c1f52dc33ea63e5d5bae0d22839e0479c869d1245a3aa1f6e043fc6abf727`  
		Last Modified: Wed, 13 May 2026 00:29:46 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79e2bd196a4c79243b8f32caa003ad67755243b1aa7c7811c8703a929a043740`  
		Last Modified: Wed, 13 May 2026 00:29:45 GMT  
		Size: 75.8 KB (75845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fb683ad1a0e16d506447c1ca1f07ffb9615509bb51ea3a05032d1183b5b05dd`  
		Last Modified: Wed, 13 May 2026 00:29:45 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a937f3089b19344664f2c870edfc59a179181449b8d3f6464d4189b331ab2f0`  
		Last Modified: Wed, 13 May 2026 00:30:00 GMT  
		Size: 201.9 MB (201875807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05de6d05129f18ebebc7f77fed544a9fe6ed178f91a0a9bf23d8f43ca515c5ac`  
		Last Modified: Wed, 13 May 2026 00:29:45 GMT  
		Size: 102.6 KB (102636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18baf1047a73887ce529bdb2d37257f31726857e232581abc93761eae4e7d9cf`  
		Last Modified: Wed, 13 May 2026 00:29:45 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jdk-nanoserver` - windows version 10.0.20348.5139; amd64

```console
$ docker pull eclipse-temurin@sha256:3fa098f8e9cbd9db4f63beff17b8db60f0dee138dfa992c46028a15ff7147abf
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.1 MB (329108473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c35d640f9532b8264d9802de5eec29c4f9dbe5fb784b911d795a6c9e7ffe1104`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 13 May 2026 00:23:39 GMT
SHELL [cmd /s /c]
# Wed, 13 May 2026 00:24:38 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Wed, 13 May 2026 00:24:38 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 13 May 2026 00:24:38 GMT
USER ContainerAdministrator
# Wed, 13 May 2026 00:24:40 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 May 2026 00:24:40 GMT
USER ContainerUser
# Wed, 13 May 2026 00:24:48 GMT
COPY dir:be4fce80d476aa164b4bdafca77eddb646da4c27d929101014e2067a583f974e in C:\openjdk-21 
# Wed, 13 May 2026 00:24:54 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 13 May 2026 00:24:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d60ed370d326231e88b53b9eb83b5e7c2a02f147b495f0751da4e9072d5d7a91`  
		Last Modified: Wed, 13 May 2026 00:23:57 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d26628cd2eb72d3d84e9013d08cd50adee081f0fe988c2e3b3f0c2672f8d70b`  
		Last Modified: Wed, 13 May 2026 00:24:59 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7efeb7ef5a010d14b572d8c37f1c896d67d879540e32f63d89b2e8d4fb2f46`  
		Last Modified: Wed, 13 May 2026 00:25:00 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b26541c4b87cf6cd752644ffc2c5f99c7697a01c97d9acff2b19114593ae3af3`  
		Last Modified: Wed, 13 May 2026 00:24:59 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ddbdf2ffd9bee9dca81f43938845dcb4af4d2f47ed65279390823d973361b05`  
		Last Modified: Wed, 13 May 2026 00:24:58 GMT  
		Size: 77.5 KB (77528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a077e04e1f65ab0c1fa951f19316c7f3c842f244c8651cbf096ba0393daf6de`  
		Last Modified: Wed, 13 May 2026 00:24:58 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae80faea77e1ee233aba063a8b43b042846a59a1dc47e2f0a4bd71c67158469`  
		Last Modified: Wed, 13 May 2026 00:25:11 GMT  
		Size: 201.9 MB (201874389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:776c728d2950ac9d54a33c802a3f907b5df4e504ac573cfe74552091d240c5b1`  
		Last Modified: Wed, 13 May 2026 00:24:58 GMT  
		Size: 111.4 KB (111443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85192535cd90baa5ffa58da7fb0050ea8cb058a5a1d16fa587f023d0c1e509d0`  
		Last Modified: Wed, 13 May 2026 00:24:58 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
