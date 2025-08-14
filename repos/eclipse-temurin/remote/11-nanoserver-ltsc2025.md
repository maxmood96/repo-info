## `eclipse-temurin:11-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:7ab60d5bd21758e44ddc8ae586995ac9cd4c564b1b61a9525645d4cbfaba07f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4946; amd64

### `eclipse-temurin:11-nanoserver-ltsc2025` - windows version 10.0.26100.4946; amd64

```console
$ docker pull eclipse-temurin@sha256:4ab75f115a094b94cf956e9d56f8a7019bcfccf263590fa6fcd2cffe9866dd1b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.3 MB (388288700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beeac63d57c90e570db1479d9a255f6676a4f8425135dd8e88316ae456deafae`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 10 Aug 2025 02:44:20 GMT
RUN Apply image 10.0.26100.4946
# Tue, 12 Aug 2025 20:50:57 GMT
SHELL [cmd /s /c]
# Tue, 12 Aug 2025 20:50:58 GMT
ENV JAVA_VERSION=jdk-11.0.28+6
# Tue, 12 Aug 2025 20:50:58 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 12 Aug 2025 20:50:58 GMT
USER ContainerAdministrator
# Tue, 12 Aug 2025 20:51:00 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 12 Aug 2025 20:51:01 GMT
USER ContainerUser
# Tue, 12 Aug 2025 20:51:07 GMT
COPY dir:8b5aa3450b5ed8de1b2c81f4388b1a437f54688a5e8c6d990bf0f6727b917a6b in C:\openjdk-11 
# Tue, 12 Aug 2025 20:51:11 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 12 Aug 2025 20:51:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6d63d98dae9e3419e8c965c24a11d30e40947cf35ee17c204c5d8b7bae7ff2ef`  
		Last Modified: Tue, 12 Aug 2025 21:13:38 GMT  
		Size: 193.5 MB (193469373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ddc5fe89889faf8792219338f143992a064504fa4e9287d60bfba6284611dfe`  
		Last Modified: Tue, 12 Aug 2025 20:52:08 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bdf4831d265e0337450c3410fb3ac82e1eaf470d3f8d6aa82dc5f6427bd8d79`  
		Last Modified: Tue, 12 Aug 2025 20:52:09 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebdcb5da6292a80f3a0ced88565f83d2eb31738f21589b1e8cdcd445bd2bcd12`  
		Last Modified: Tue, 12 Aug 2025 20:52:09 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e82b85aab26eacf47532dedb4bd461c8999ed25caab3288a6c3956a45113965`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6721e5e149131c3a235a8cb0a8d3313e0611c3069cadef3e419628e9f2449a1b`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 75.7 KB (75720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548a95e89edd6964bbc00bd6908f21875fc2f852dd62c6dd1163e1d264b8ef12`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:651a12c77ccd08b96f709eee8d7c7b201d64c905a9355b599a83fa855d3c01f7`  
		Last Modified: Tue, 12 Aug 2025 21:13:41 GMT  
		Size: 194.6 MB (194622790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b546b54d414b19d0d715c1b99f8d158b4c75bb5829e9a136953c4fd4e4f16722`  
		Last Modified: Tue, 12 Aug 2025 21:13:24 GMT  
		Size: 114.4 KB (114411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5da2f39379c5164f14c83dfd98a476a9e63670e9b0c7518e3d1863149a90a51`  
		Last Modified: Tue, 12 Aug 2025 21:13:24 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
