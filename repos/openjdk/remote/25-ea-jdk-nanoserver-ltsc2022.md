## `openjdk:25-ea-jdk-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:af68b1f43cc39b88b5cb411212e321af177c9b785e1584bad54f66e67c0d4262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `openjdk:25-ea-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull openjdk@sha256:6e143f3e4f48e1e5dabb18972db3e6c8c3d4705822435552fc33ca54b821696d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.1 MB (332099856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a32c24c523b874fcf70bc6be4ebdb66d28b2f2c5e46fc1e24a3c5ce2d62bef7a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Fri, 23 May 2025 21:16:48 GMT
SHELL [cmd /s /c]
# Fri, 23 May 2025 21:16:49 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 23 May 2025 21:16:50 GMT
USER ContainerAdministrator
# Fri, 23 May 2025 21:16:52 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 23 May 2025 21:16:53 GMT
USER ContainerUser
# Fri, 23 May 2025 21:16:53 GMT
ENV JAVA_VERSION=25-ea+24
# Fri, 23 May 2025 21:17:00 GMT
COPY dir:d32a1e622c307f990d42f1dfe6052e231c098d4b948c30b3def65fbe5914b454 in C:\openjdk-25 
# Fri, 23 May 2025 21:17:05 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 23 May 2025 21:17:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Tue, 13 May 2025 19:42:18 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c895d1a2c31caf6ac01626454530bc419de36fa8b53993c1652ded6b3b39f4e8`  
		Last Modified: Fri, 23 May 2025 21:17:09 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:316474de4f07ac6982fc9f9b122dad30dc7f1a608da7e144937f68fa5df3b442`  
		Last Modified: Fri, 23 May 2025 21:17:09 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fd6c4c9996b340f8486e0bf88289c362fb1698055c6906ce619b52fc8607c47`  
		Last Modified: Fri, 23 May 2025 21:17:09 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a49e5498d5cb5c520c1e81a6a419fe27ce309b727ae29e894a2474d4080fd41`  
		Last Modified: Fri, 23 May 2025 21:17:09 GMT  
		Size: 75.8 KB (75811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:391b6d49dca611d0b90618255963e20315721948d6365322826aa4f71d5bc9d8`  
		Last Modified: Fri, 23 May 2025 21:17:08 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c054a3fbd3cd1cc9f601eb410f0c03cd802e129f71d85fb90b498af3c6f8642`  
		Last Modified: Fri, 23 May 2025 21:17:08 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce919243fd524241da6da77f0a9b30cdef06afad17ca05ec0e73f796cb1cb5d6`  
		Last Modified: Fri, 23 May 2025 21:17:19 GMT  
		Size: 209.3 MB (209334173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90228bc979e0d34e3a6272d70fb1565b68551b761a99b39c42afd7bb4603e26b`  
		Last Modified: Fri, 23 May 2025 21:17:08 GMT  
		Size: 107.1 KB (107061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b111bf0e7b902181429f16eb69c1ba0db58d78b1dbd4a211f07795a886d77a7`  
		Last Modified: Fri, 23 May 2025 21:17:08 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
