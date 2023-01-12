## `eclipse-temurin:17-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:b90cb195a9b8a586b211fe93ba5ec48faae1fd47b831747c68e55ae9441829e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1487; amd64
	-	windows version 10.0.17763.3887; amd64

### `eclipse-temurin:17-jre-nanoserver` - windows version 10.0.20348.1487; amd64

```console
$ docker pull eclipse-temurin@sha256:fb4792052ebba3597430b9782369a90a92e8549c0f057872e43ba89388fac440
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.5 MB (165534881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:399cf19942c543de93ef62df42766016ff30d3e334a156b6acbc819fdbdebb9f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Jan 2023 23:36:49 GMT
RUN Apply image 10.0.20348.1487
# Thu, 12 Jan 2023 02:19:48 GMT
SHELL [cmd /s /c]
# Thu, 12 Jan 2023 02:23:38 GMT
ENV JAVA_VERSION=jdk-17.0.5+8
# Thu, 12 Jan 2023 02:23:39 GMT
ENV JAVA_HOME=C:\openjdk-17
# Thu, 12 Jan 2023 02:23:40 GMT
USER ContainerAdministrator
# Thu, 12 Jan 2023 02:23:52 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 12 Jan 2023 02:23:53 GMT
USER ContainerUser
# Thu, 12 Jan 2023 02:24:49 GMT
COPY dir:20852dc87397947f41c5a6f7f30dc526aa127dbd27640e91343bc06b34d57a7f in C:\openjdk-17 
# Thu, 12 Jan 2023 02:25:26 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:83e9437e818022c1c28f0e07002dd46995c8614e62b9366138fa23b94f43d9ad`  
		Last Modified: Thu, 12 Jan 2023 02:51:06 GMT  
		Size: 122.1 MB (122099566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbebbf572ebe7984b715b8dfe99bc1273403a831c0079b95afa12162b7266f16`  
		Last Modified: Thu, 12 Jan 2023 02:50:38 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d6f45b3aeb713e90b16953d34b61fb78e87c6155d507fba1a45f9961f6ccd9`  
		Last Modified: Thu, 12 Jan 2023 02:52:19 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3fd926487da848d823b4941c4fe12f5f4da46397b110eff960b984af540710b`  
		Last Modified: Thu, 12 Jan 2023 02:52:19 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007ebd27f3fc1ff2dc3d698699a79150001e6baa2fa21fa90f22cb46ae486d45`  
		Last Modified: Thu, 12 Jan 2023 02:52:19 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59689ef04994653d6bf51b01b71ddaa681ad309035dccc725d5a6f52ca6fea30`  
		Last Modified: Thu, 12 Jan 2023 02:52:18 GMT  
		Size: 86.2 KB (86221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870d55487b8f6793d3a29816a146e65adfbde42c004b32e886e2fab4701999d7`  
		Last Modified: Thu, 12 Jan 2023 02:52:17 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f09389c5d4d45c2eef29f802a47b694b24ed504a26de5c63d4efe75a73f00630`  
		Last Modified: Thu, 12 Jan 2023 02:52:57 GMT  
		Size: 43.3 MB (43283363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc2cddab22c9918902bb28e1bd8bff6479a87debbd3e12a370de60cd2414f47`  
		Last Modified: Thu, 12 Jan 2023 02:52:48 GMT  
		Size: 59.9 KB (59896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jre-nanoserver` - windows version 10.0.17763.3887; amd64

```console
$ docker pull eclipse-temurin@sha256:528414728ba3bbfbe6bb99c1ea505f7ec79bf9e8b539d2c4113663eaa6f61be8
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153082738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:056abe0b305a0bb62b591273d907a2dcdd8e6536250c1263581ea77576cdbecf`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 07 Jan 2023 05:17:01 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:45:31 GMT
SHELL [cmd /s /c]
# Thu, 12 Jan 2023 02:05:45 GMT
ENV JAVA_VERSION=jdk-17.0.5+8
# Thu, 12 Jan 2023 02:05:46 GMT
ENV JAVA_HOME=C:\openjdk-17
# Thu, 12 Jan 2023 02:05:47 GMT
USER ContainerAdministrator
# Thu, 12 Jan 2023 02:05:56 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 12 Jan 2023 02:05:57 GMT
USER ContainerUser
# Thu, 12 Jan 2023 02:09:40 GMT
COPY dir:20852dc87397947f41c5a6f7f30dc526aa127dbd27640e91343bc06b34d57a7f in C:\openjdk-17 
# Thu, 12 Jan 2023 02:09:57 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:e58f9ad3b15a2a4882ab0a845e8e619cc8c3c411ddbe8b50046c1618a95c1397`  
		Last Modified: Thu, 12 Jan 2023 02:40:44 GMT  
		Size: 106.7 MB (106666138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea67a6bd980bdee35399883e5abcc31c738b338ad384b2f92d91a15cf09d9df`  
		Last Modified: Thu, 12 Jan 2023 02:40:16 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13b3ff36141248d5c515de7da07b130392186ce2d1abe71f5dc755b2773aaae4`  
		Last Modified: Thu, 12 Jan 2023 02:46:14 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760cb0d1240fabb82ff32d1196d41015aa5139ad34709d02c131012ae7ec3c0f`  
		Last Modified: Thu, 12 Jan 2023 02:46:13 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97a276723df58e8dba1df3bcada32f101203f6e683ddc7cd325d1e90539bc210`  
		Last Modified: Thu, 12 Jan 2023 02:46:13 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25ab331f221205fddf18bb195ad81997120fa53007421c5c73a62a2b945b51f`  
		Last Modified: Thu, 12 Jan 2023 02:46:12 GMT  
		Size: 71.0 KB (71031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e907af4176d44f2c0e2445f445b7f8696a7277670b4b00232b7831bb9158f6e`  
		Last Modified: Thu, 12 Jan 2023 02:46:11 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ae5707b1772fcfaf4b6d47d22ace1bcc76ac2c38b9ad225751f1d4e163f974`  
		Last Modified: Thu, 12 Jan 2023 02:47:30 GMT  
		Size: 43.3 MB (43280829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0de48ac6e7d75ca1e506ed94547011cc9bca1d06b1d917dcc13edc983f9d1c`  
		Last Modified: Thu, 12 Jan 2023 02:47:22 GMT  
		Size: 3.1 MB (3059439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
