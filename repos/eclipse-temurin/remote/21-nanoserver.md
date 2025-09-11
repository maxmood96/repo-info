## `eclipse-temurin:21-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:6590c57c6c06395e35c3e0b2f5f98accb2b6ee13f07bfaeac099293081132199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `eclipse-temurin:21-nanoserver` - windows version 10.0.26100.6584; amd64

```console
$ docker pull eclipse-temurin@sha256:884dfc0a7f56de016fa1c2970db77859de78a4d9fbebbccf71ad4b078e395efb
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.4 MB (395393510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd06ee821fbba10ac23dd0f59fe0ff73838799e4bab97bf8865244e1b01dd14`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Sep 2025 02:12:39 GMT
RUN Apply image 10.0.26100.6584
# Wed, 10 Sep 2025 22:19:45 GMT
SHELL [cmd /s /c]
# Wed, 10 Sep 2025 22:19:45 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Wed, 10 Sep 2025 22:19:46 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 10 Sep 2025 22:19:46 GMT
USER ContainerAdministrator
# Wed, 10 Sep 2025 22:19:50 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Sep 2025 22:19:50 GMT
USER ContainerUser
# Wed, 10 Sep 2025 22:19:58 GMT
COPY dir:a3fe1d88014e165c39b52565bb4587e5a787fc090e6660a0edced9167c6512ac in C:\openjdk-21 
# Wed, 10 Sep 2025 22:20:03 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 10 Sep 2025 22:20:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a75a4ab04983f989d9a1442633d6c3952b863719a00dd77cf160f7055beaded9`  
		Last Modified: Tue, 09 Sep 2025 22:28:08 GMT  
		Size: 193.6 MB (193550846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a879f436d837a2b288893b482e02b87f8d8f98f0f4343ff630a85352370cc334`  
		Last Modified: Wed, 10 Sep 2025 22:20:54 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea347919ad67858602c006e12e1cf532c2aff2a50ee5897ec50a8ec43507dab`  
		Last Modified: Wed, 10 Sep 2025 22:20:54 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33efc8c2e7c922e361a26b9e89eb2173112ea22c458afc9028333be992cab2c`  
		Last Modified: Wed, 10 Sep 2025 22:20:55 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b6b50c62bce22472fbada35a7b8d1d032717c8a64de6591ce232a9594b464d`  
		Last Modified: Wed, 10 Sep 2025 22:20:55 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e972cc0a8d0c3af83d1cb5e52bab47f31f1b2c5b2e29c980394a33369f8774`  
		Last Modified: Wed, 10 Sep 2025 22:20:55 GMT  
		Size: 71.4 KB (71443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4d1d3a6fefda51f1f7f779d2efb5649ae9aca08b6b3c659d1c5de3a64aea02`  
		Last Modified: Wed, 10 Sep 2025 22:20:55 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741a344efba588616d1d540b335cb4ecc161b7b3c0ec7c2d4e07ebc6f0cb001b`  
		Last Modified: Thu, 11 Sep 2025 00:16:36 GMT  
		Size: 201.7 MB (201671756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df062406cf9863a33e092c79609399de9cd6878e594d4da273dde16fd8f9ccfa`  
		Last Modified: Wed, 10 Sep 2025 22:20:55 GMT  
		Size: 93.1 KB (93077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f44de5f49856bf66b91af3649b62b1b7abd1e3ac0270cd16aa93ea0f053d81d`  
		Last Modified: Wed, 10 Sep 2025 22:20:55 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-nanoserver` - windows version 10.0.20348.4171; amd64

```console
$ docker pull eclipse-temurin@sha256:10111ea6ca7b029b7f9c1e7c357fd60a993693ef8526e0228e14d7a9692578f8
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.6 MB (324583968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c921ba4983ad275040b34d84ff3bd681c70b67632d5aa678058b200e5563f8ee`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Wed, 10 Sep 2025 22:18:16 GMT
SHELL [cmd /s /c]
# Wed, 10 Sep 2025 22:19:05 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Wed, 10 Sep 2025 22:19:05 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 10 Sep 2025 22:19:06 GMT
USER ContainerAdministrator
# Wed, 10 Sep 2025 22:19:07 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Sep 2025 22:19:08 GMT
USER ContainerUser
# Wed, 10 Sep 2025 22:19:15 GMT
COPY dir:a3fe1d88014e165c39b52565bb4587e5a787fc090e6660a0edced9167c6512ac in C:\openjdk-21 
# Wed, 10 Sep 2025 22:19:19 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 10 Sep 2025 22:19:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61cbb86931614a5d803cf00ed301ed322ace890beae852523d46150a851ed2e7`  
		Last Modified: Wed, 10 Sep 2025 23:02:50 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8081ad48fe3c07eda03b3f94db1c5f7d4230f7ab86dc98ce967d2f29c5737c79`  
		Last Modified: Wed, 10 Sep 2025 22:19:46 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83e2bbb04876813d808ff5c5f8e2614636c32dc8c310291baa43fb7506b2f61e`  
		Last Modified: Wed, 10 Sep 2025 22:19:46 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a4b4d39d96fac6281a9500d19b8c487f09e63ae529f5a198f8ac42e3e1bb76`  
		Last Modified: Wed, 10 Sep 2025 22:19:47 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e7f5fa4dd9d9b1663648d0aad725d7bcdb75dc2b0bc60f647308f55fb23f4f`  
		Last Modified: Wed, 10 Sep 2025 22:19:47 GMT  
		Size: 77.4 KB (77447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2255199184898186dcf7b105d3b7b8d9219ccbf825978a48f901146051688678`  
		Last Modified: Wed, 10 Sep 2025 22:19:47 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de231828d1d6c62f5a45fb10abd78b2953ae716af57c577beba53e527eacebcc`  
		Last Modified: Thu, 11 Sep 2025 02:26:34 GMT  
		Size: 201.7 MB (201671867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d91147d9e82200962c5211f8ed106702c21f5b7681c59386d3b542ba279239`  
		Last Modified: Wed, 10 Sep 2025 22:19:47 GMT  
		Size: 108.4 KB (108362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6e8c0938467340d5e2cee280f0ef3f56a963c301ba73475107fe83542bcfa5`  
		Last Modified: Wed, 10 Sep 2025 22:19:48 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
