## `eclipse-temurin:8u432-b06-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:773de477f1ecde901af4e1683f5735e7af8297636536ab3e8c16310e73afb04b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `eclipse-temurin:8u432-b06-jdk-nanoserver-1809` - windows version 10.0.17763.6532; amd64

```console
$ docker pull eclipse-temurin@sha256:97bf59bbb9d210563efb1ecebdd82a0216a7bf8aa9dcc6cb7cd0db2ffc55e450
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.0 MB (258993264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbc36e238488d5a5ca4e16ec5e29c102d0fe4f1728400e7862e2c9714757f577`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 01 Nov 2024 11:18:21 GMT
RUN Apply image 10.0.17763.6532
# Thu, 14 Nov 2024 21:23:37 GMT
SHELL [cmd /s /c]
# Thu, 14 Nov 2024 21:23:40 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Thu, 14 Nov 2024 21:23:40 GMT
ENV JAVA_HOME=C:\openjdk-8
# Thu, 14 Nov 2024 21:23:41 GMT
USER ContainerAdministrator
# Thu, 14 Nov 2024 21:23:44 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 14 Nov 2024 21:23:45 GMT
USER ContainerUser
# Thu, 14 Nov 2024 21:23:51 GMT
COPY dir:20063c61efcf25f5137b7902f122f09a78eae5d617f3f56a66aed8780998122b in C:\openjdk-8 
# Thu, 14 Nov 2024 21:23:55 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:b79a100b554b1ee5bf83d129fe624c0ddd7754edeaf1a1364fefbbf2ba3095c1`  
		Last Modified: Tue, 12 Nov 2024 20:49:39 GMT  
		Size: 155.2 MB (155214227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd11ae50eebdd5f2699f06b79aba8d986cabd385b6ad8fe707e89102d3f45813`  
		Last Modified: Thu, 14 Nov 2024 21:23:59 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5863d2acfcd0cc6d05641f19f59ed98eeecc9a7e9cbba905028c42cfc3ff44`  
		Last Modified: Thu, 14 Nov 2024 21:23:59 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0149d086aff04732ebdb55f725813078c4e158c5408ea31b4c63383df0d15418`  
		Last Modified: Thu, 14 Nov 2024 21:23:59 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a3147b61d2e6e84c64c536cf1c5ca775c6f08fbfd671b02fedf62ca81979cce`  
		Last Modified: Thu, 14 Nov 2024 21:23:58 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3a74ba4afd402668564f8e623a5e87dc222eae1c344e44700e27ece3ba59be5`  
		Last Modified: Thu, 14 Nov 2024 21:23:58 GMT  
		Size: 94.2 KB (94247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6e04e97473386287ba5bd2745d218bd612bbd9018a3b1ced94cf466ef7b56b`  
		Last Modified: Thu, 14 Nov 2024 21:23:58 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad0efd2049f3221b1c62023144346961786f92df3bed020e2680449c614784d`  
		Last Modified: Thu, 14 Nov 2024 21:24:04 GMT  
		Size: 103.4 MB (103441164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b5c6b626d73bb1527f6ed67ee6737e461d63ba68d604068d3e662f0a7d821a`  
		Last Modified: Thu, 14 Nov 2024 21:23:58 GMT  
		Size: 238.3 KB (238328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
