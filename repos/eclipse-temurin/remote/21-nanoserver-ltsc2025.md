## `eclipse-temurin:21-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:1f95ad4772cc2fcce855807cb975fb1c403584bb65635a068e2ed5e2802cd636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3775; amd64

### `eclipse-temurin:21-nanoserver-ltsc2025` - windows version 10.0.26100.3775; amd64

```console
$ docker pull eclipse-temurin@sha256:bac63069e3306e31d47a1050d55c9245c36e0b3f3b742942466afbb4f5b85658
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.8 MB (391787460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:414762e44d12aa4097d36c0ad9d7e6a65896ef09283c9a7f064c8edb85307103`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 06 Apr 2025 07:26:08 GMT
RUN Apply image 10.0.26100.3775
# Wed, 09 Apr 2025 01:48:58 GMT
SHELL [cmd /s /c]
# Wed, 09 Apr 2025 01:48:59 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Wed, 09 Apr 2025 01:49:00 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 09 Apr 2025 01:49:01 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 01:49:04 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Apr 2025 01:49:05 GMT
USER ContainerUser
# Wed, 09 Apr 2025 01:49:14 GMT
COPY dir:87fb2a3fe15bf051f07e33b0f4d627a83582ff5ee0a30a4b75036496ad24f723 in C:\openjdk-21 
# Wed, 09 Apr 2025 01:49:22 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 09 Apr 2025 01:49:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:79b2ed45f890e91d23d7d22491a8fb6909c9268c668dc6a0e3b40131da02ed74`  
		Last Modified: Wed, 09 Apr 2025 00:36:30 GMT  
		Size: 190.1 MB (190113206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e549d6300b7c9dbe3837adb59ddcf6f523587df6ea304fe9fe2a97b101d53ef6`  
		Last Modified: Wed, 09 Apr 2025 01:49:30 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a8ec185fef8c2413b31b9b33de20e720d6a69c1fa3a4fa757294d7e3442d46`  
		Last Modified: Wed, 09 Apr 2025 01:49:29 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9e480055aae7693a113a33cce2e14d09850008160cf8b3b6e8d56214b3f9c6`  
		Last Modified: Wed, 09 Apr 2025 01:49:29 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37c1a18b756a8092d4f8234aa40de3406fcea65df07252652c953b0c7b296834`  
		Last Modified: Wed, 09 Apr 2025 01:49:29 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f2ad7918c8c1a90514782f4e83e817ef7caed717c271b410c0a72a6f4b1a789`  
		Last Modified: Wed, 09 Apr 2025 01:49:27 GMT  
		Size: 77.1 KB (77115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60ad3862c065dc84e2c88693cb8eeeed9969716787015d5246a1df11636b5c45`  
		Last Modified: Wed, 09 Apr 2025 01:49:27 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b1a9af3f70a3a2cc21eaa3a9abe8514053b3327dab802f9cc608a22762a481e`  
		Last Modified: Wed, 09 Apr 2025 01:49:40 GMT  
		Size: 201.5 MB (201476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b5954df206eb7e535d1d72655020b31c0c79e160694dbf02918cd876759dc31`  
		Last Modified: Wed, 09 Apr 2025 01:49:27 GMT  
		Size: 114.7 KB (114693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0072c03e3426aeef3c2f34b8b16063ab5fb81a7dec28e3b898db9077d895cb3`  
		Last Modified: Wed, 09 Apr 2025 01:49:27 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
