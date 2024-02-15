## `eclipse-temurin:8-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:f56d7902980ef33aacad71b26f0fbd27f03bdd70a1aa04509f5f0226efa9e831
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2322; amd64
	-	windows version 10.0.17763.5458; amd64

### `eclipse-temurin:8-jdk-nanoserver` - windows version 10.0.20348.2322; amd64

```console
$ docker pull eclipse-temurin@sha256:353c4288a347c8ae6ed649736956ebb2dcc53e6d5f0b639d37d07a69063d2466
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.6 MB (222581502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fd5226fa57a8319fc2effefc1bc4eb991591e130db2cc2c54dec323edf18876`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 07 Feb 2024 06:29:10 GMT
RUN Apply image 10.0.20348.2322
# Wed, 14 Feb 2024 20:21:03 GMT
SHELL [cmd /s /c]
# Wed, 14 Feb 2024 20:21:04 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Wed, 14 Feb 2024 20:21:05 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 14 Feb 2024 20:21:05 GMT
USER ContainerAdministrator
# Wed, 14 Feb 2024 20:21:19 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 14 Feb 2024 20:21:19 GMT
USER ContainerUser
# Wed, 14 Feb 2024 20:21:31 GMT
COPY dir:9ab35a15e19e8247451d444f7de2a75fe407ec1749c1b49082dcaaef6c80dafd in C:\openjdk-8 
# Wed, 14 Feb 2024 20:21:46 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:ccff18da882d371921351307d169380d3ac22ef981f2bb4f14fb2b332b395439`  
		Last Modified: Tue, 13 Feb 2024 23:39:47 GMT  
		Size: 120.7 MB (120735093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d61a8b9610542d9f544621b5b605f3c73832b279a3681d70286c37473fec95b2`  
		Last Modified: Thu, 15 Feb 2024 00:16:30 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320c7f4aec5883a29011e6e9f92ddb22af540f7c4ffea76399db2f2e482da79a`  
		Last Modified: Thu, 15 Feb 2024 00:16:30 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b236d5717e24cb1456735c67ed3334020e2dfb2d9b085f9908382d2b644f523`  
		Last Modified: Thu, 15 Feb 2024 00:16:30 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ab249bb6a4cb870af2fcc419628a502aa14f8335ad1e8c860421de5ac822d80`  
		Last Modified: Thu, 15 Feb 2024 00:16:28 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a8d029d4a51c18b6e328ce712709d3a800ffd3838d1405bb11039e7b50db11a`  
		Last Modified: Thu, 15 Feb 2024 00:16:28 GMT  
		Size: 80.4 KB (80434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de18572ccdee2cf25d4ca67517fc6a7d6cd78cfdd2f34fde0b0ed0a959d57c0`  
		Last Modified: Thu, 15 Feb 2024 00:16:28 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b6f43eed8ab6412f807865eb849181f48eb9f5b8d249099bc264699ef1b60a`  
		Last Modified: Thu, 15 Feb 2024 00:16:39 GMT  
		Size: 101.7 MB (101699111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc62a9b8420beef74005d3f5dabf4d4f0e0ad50ce484a5dc4b445361ef330ce`  
		Last Modified: Thu, 15 Feb 2024 00:16:28 GMT  
		Size: 61.1 KB (61071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jdk-nanoserver` - windows version 10.0.17763.5458; amd64

```console
$ docker pull eclipse-temurin@sha256:7116b52c44f82695b001ca2f3ce0e9c130f00527712b819e33d5b3f7990bd26e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.5 MB (206498937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0ab3537f5db144ba71f37a4fcf5ab90a77ecd6a1b8dfcb5d76e935af15d0243`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 04 Feb 2024 03:35:01 GMT
RUN Apply image 10.0.17763.5458
# Wed, 14 Feb 2024 19:41:52 GMT
SHELL [cmd /s /c]
# Wed, 14 Feb 2024 19:41:53 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Wed, 14 Feb 2024 19:41:54 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 14 Feb 2024 19:41:54 GMT
USER ContainerAdministrator
# Wed, 14 Feb 2024 19:42:05 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 14 Feb 2024 19:42:06 GMT
USER ContainerUser
# Wed, 14 Feb 2024 19:42:17 GMT
COPY dir:9ab35a15e19e8247451d444f7de2a75fe407ec1749c1b49082dcaaef6c80dafd in C:\openjdk-8 
# Wed, 14 Feb 2024 19:42:30 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:81be0bec766f944241448cd25317f59edcb12514e41b43288302e3e88d5462ad`  
		Last Modified: Tue, 13 Feb 2024 20:17:19 GMT  
		Size: 104.6 MB (104621606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cddfc54d18bb5861232283d3ff2ca5e214ade28a46dfcf6c1e7c7243809e5e85`  
		Last Modified: Thu, 15 Feb 2024 00:06:58 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50de6bbc468ce67f5c06aec96ce768f0701699d3e2e0b0f624f2414d51118ab7`  
		Last Modified: Thu, 15 Feb 2024 00:06:59 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4981285aad162eb35c182a94596307747ddb88a060134c126e380584659b091a`  
		Last Modified: Thu, 15 Feb 2024 00:06:58 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bcbefbe80e1c3c4fe2a0ce3b1475bc3f49b412b16db693ec97a04d8e952ad4f`  
		Last Modified: Thu, 15 Feb 2024 00:06:56 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d995837ef866fa986b862cf38eba7d9b6919e0841be54a8c8507bcc20429eda3`  
		Last Modified: Thu, 15 Feb 2024 00:06:56 GMT  
		Size: 75.9 KB (75858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b0ab688df4f030d11a95f25383a65f0b25a81897dfcecfe28ebdf93224e21b`  
		Last Modified: Thu, 15 Feb 2024 00:06:56 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:680cc5e91a9451783c3a9929194b11f0556803228d30b8cfe3815c5decd0b55a`  
		Last Modified: Thu, 15 Feb 2024 00:07:08 GMT  
		Size: 101.7 MB (101701527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e281a5a246ff148c8a7103f3053bc1f4e0543010ff3fb2cc80beafe289ebe196`  
		Last Modified: Thu, 15 Feb 2024 00:06:56 GMT  
		Size: 94.1 KB (94109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
