## `eclipse-temurin:17-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:515b99a49fccf7827c3baa67909a0978fb28c4dc88812e3a4c3d27471713359e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3887; amd64

### `eclipse-temurin:17-jdk-nanoserver-1809` - windows version 10.0.17763.3887; amd64

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
