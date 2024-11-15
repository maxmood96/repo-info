## `eclipse-temurin:11-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:9e5c13b5c74ce14c38a528cf14c08e96f1e99ee2762738992280711b28582f75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `eclipse-temurin:11-jre-nanoserver-1809` - windows version 10.0.17763.6532; amd64

```console
$ docker pull eclipse-temurin@sha256:4060abb3730d3165f17270a13b1bf6336aae2f1b4474d634ad423db2f5514ac6
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.7 MB (199725689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:625f09ea799aeb15fd82945a339ab1d3522a6d55bcab9483eb294c62da697c90`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 01 Nov 2024 11:18:21 GMT
RUN Apply image 10.0.17763.6532
# Thu, 14 Nov 2024 21:21:52 GMT
SHELL [cmd /s /c]
# Thu, 14 Nov 2024 21:21:54 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Thu, 14 Nov 2024 21:21:55 GMT
ENV JAVA_HOME=C:\openjdk-11
# Thu, 14 Nov 2024 21:21:56 GMT
USER ContainerAdministrator
# Thu, 14 Nov 2024 21:21:58 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 14 Nov 2024 21:21:59 GMT
USER ContainerUser
# Thu, 14 Nov 2024 21:22:02 GMT
COPY dir:a15dacd11bbcaacf83a6b6e1490d6483ae4af68a125407fd4cb6bb7a70e4639c in C:\openjdk-11 
# Thu, 14 Nov 2024 21:22:06 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:b79a100b554b1ee5bf83d129fe624c0ddd7754edeaf1a1364fefbbf2ba3095c1`  
		Last Modified: Tue, 12 Nov 2024 20:49:39 GMT  
		Size: 155.2 MB (155214227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc12755a8952a786ab6d3f329ea595e4351e8f6929367013dcb5f739a9a262f2`  
		Last Modified: Thu, 14 Nov 2024 21:22:09 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b0800a5a69ea8a757e6e1ccd075609850d2b2c97959207687678d9aeee8a90c`  
		Last Modified: Thu, 14 Nov 2024 21:22:09 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b3fd2cbfef4b2b2b5a80d88e125e0c490ba168f1ffa1972e01af9224ff8aaf`  
		Last Modified: Thu, 14 Nov 2024 21:22:09 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b5ea1734a6bc08dae602760af54a161cfa8beea566a23a65ec0a0ffb5685085`  
		Last Modified: Thu, 14 Nov 2024 21:22:08 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074548c34d146a6a3fe59b70d9f9fab40b404a294999d2c3d5226e9ec28a42e0`  
		Last Modified: Thu, 14 Nov 2024 21:22:08 GMT  
		Size: 87.9 KB (87858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:615be9ddbe173963eee5312cc1daee5d30f40a401b9220e0467365c5bcefbc16`  
		Last Modified: Thu, 14 Nov 2024 21:22:08 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a89e9c40ce3ea6d5cd9c7ba1655504f8d2acb1b9cb37722db1cf9dde6d2792`  
		Last Modified: Thu, 14 Nov 2024 21:22:13 GMT  
		Size: 44.3 MB (44309038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:722194b5b772ca4e8356c0c5631c7163e830757afe23e82abb1ff1211a00242d`  
		Last Modified: Thu, 14 Nov 2024 21:22:08 GMT  
		Size: 109.4 KB (109392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
