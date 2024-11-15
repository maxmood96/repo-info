## `eclipse-temurin:8u432-b06-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:ccd1ae8885d2e547b918c5c236d70a52384d1617b75b0fbe4a64b3ab0006a716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2849; amd64
	-	windows version 10.0.17763.6532; amd64

### `eclipse-temurin:8u432-b06-jdk-nanoserver` - windows version 10.0.20348.2849; amd64

```console
$ docker pull eclipse-temurin@sha256:69fca1f6a2068a6bfc198d1a725cddd26b9aff6dd17e481512377415cea5b8ae
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.2 MB (224235675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd6717275ca5a78c5d54b41728373772a85bbe9b160dbd17968ea7ef53c28b5e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 02 Nov 2024 23:34:35 GMT
RUN Apply image 10.0.20348.2849
# Thu, 14 Nov 2024 21:30:42 GMT
SHELL [cmd /s /c]
# Thu, 14 Nov 2024 21:30:43 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Thu, 14 Nov 2024 21:30:43 GMT
ENV JAVA_HOME=C:\openjdk-8
# Thu, 14 Nov 2024 21:30:44 GMT
USER ContainerAdministrator
# Thu, 14 Nov 2024 21:30:46 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 14 Nov 2024 21:30:47 GMT
USER ContainerUser
# Thu, 14 Nov 2024 21:30:53 GMT
COPY dir:20063c61efcf25f5137b7902f122f09a78eae5d617f3f56a66aed8780998122b in C:\openjdk-8 
# Thu, 14 Nov 2024 21:30:58 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:815d6b7f925aef8327c34c34073ae54cc1c82120f1058682eac4c8c14ca21c70`  
		Last Modified: Tue, 12 Nov 2024 22:44:32 GMT  
		Size: 120.6 MB (120604951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36980ff27c8e13b54f8df6f3ba3b550c8ac09a4c9036070b4ccef6dfdabbc35a`  
		Last Modified: Thu, 14 Nov 2024 21:31:02 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3400f7807b0ca6d54c6151778d9992a6c75e083eb1badd81e9fbc1515b17f626`  
		Last Modified: Thu, 14 Nov 2024 21:31:01 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c031a7128ce465c54625da1bc0f177aefdb2d5cf306bf9830b9f6789b8ae9044`  
		Last Modified: Thu, 14 Nov 2024 21:31:01 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a031715fa78d73a85c5e06e6b15c24254edf0976a2cc8682a9d0275bba7864`  
		Last Modified: Thu, 14 Nov 2024 21:31:00 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:898defcee03fe4aa7af403dca31cf19783e0d4aa92d63cc6101814156a5772ab`  
		Last Modified: Thu, 14 Nov 2024 21:31:01 GMT  
		Size: 77.4 KB (77443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df10e722d2848fcae6ffcdd65d25172b76ab3eab3f08fa1795bdebb1eefa4fe`  
		Last Modified: Thu, 14 Nov 2024 21:31:00 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e9b463122f21b30955e8fbb0c7d63a64aaeaf02fac62eece8c273b5e2ae276`  
		Last Modified: Thu, 14 Nov 2024 21:31:07 GMT  
		Size: 103.4 MB (103441336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3d5c65a4866f94937deb313647bc35278ee240aff58468b6a1e2cfcc4f6c9c`  
		Last Modified: Thu, 14 Nov 2024 21:31:00 GMT  
		Size: 106.8 KB (106787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u432-b06-jdk-nanoserver` - windows version 10.0.17763.6532; amd64

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
