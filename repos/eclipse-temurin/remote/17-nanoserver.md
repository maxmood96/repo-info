## `eclipse-temurin:17-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:5f16dab4c2658f134d7bf686302663fdd5cccd009e8f8efe8444f935ae7c57a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1487; amd64
	-	windows version 10.0.17763.3887; amd64

### `eclipse-temurin:17-nanoserver` - windows version 10.0.20348.1487; amd64

```console
$ docker pull eclipse-temurin@sha256:ab41471ec0082c2f772701de2657210dae023b83845518892c9fb45479635453
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.7 MB (307681787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fcdc52dd7df470ad9fce99ee488f1b61904fe91dd10d89fa06c17822bbce55c`
-	Default Command: `["jshell"]`
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
# Thu, 12 Jan 2023 02:24:09 GMT
COPY dir:a12ba5a18c812bc88dc6c1e12f0d0bdbacab70db88697cd6bad273d4570ac4fb in C:\openjdk-17 
# Thu, 12 Jan 2023 02:24:33 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 12 Jan 2023 02:24:34 GMT
CMD ["jshell"]
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
	-	`sha256:81e85448d53b7eadccbe73282ff3b2ae255c72938da050a8be77665f53734d49`  
		Last Modified: Thu, 12 Jan 2023 02:52:37 GMT  
		Size: 185.4 MB (185429302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a721a6bdc6a018d26b9408d5da41a552fde1e966dabd515c3a65625160b88c`  
		Last Modified: Thu, 12 Jan 2023 02:52:18 GMT  
		Size: 59.7 KB (59688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a2310ce238704d8e5437f0f7d01c4105944df9c4d220b948f7138aa221dcc0`  
		Last Modified: Thu, 12 Jan 2023 02:52:18 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-nanoserver` - windows version 10.0.17763.3887; amd64

```console
$ docker pull eclipse-temurin@sha256:39c2a171835f4e43b2b12fa47a574a0d15058611be786daae9dae832629ce782
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.8 MB (295840982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ada9b0a6026b65377512938ac93824e6b9824329eb3e38b7c7f63d1cf74129c`
-	Default Command: `["jshell"]`
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
# Thu, 12 Jan 2023 02:06:14 GMT
COPY dir:a12ba5a18c812bc88dc6c1e12f0d0bdbacab70db88697cd6bad273d4570ac4fb in C:\openjdk-17 
# Thu, 12 Jan 2023 02:06:38 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 12 Jan 2023 02:06:38 GMT
CMD ["jshell"]
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
	-	`sha256:ce60e56995d04ba51248d0f8ed787de22bb7119b405d03dea80bda23ae1b1a83`  
		Last Modified: Thu, 12 Jan 2023 02:46:33 GMT  
		Size: 185.4 MB (185432698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29bbc92bcbf6eb53793c115f39b5f5eaeac3590b9a46fb61ad2340541985ec8c`  
		Last Modified: Thu, 12 Jan 2023 02:46:13 GMT  
		Size: 3.7 MB (3664662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d136c3a17626fc94968ef75575e15ef47b95a09affad0e55a3a16cf5615eea`  
		Last Modified: Thu, 12 Jan 2023 02:46:11 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
