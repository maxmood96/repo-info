## `eclipse-temurin:11-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:a0ecdb31073d07cf4622b089eae0340d0c8a91a280872d4edbd0a7c12096bec7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `eclipse-temurin:11-jdk-nanoserver` - windows version 10.0.26100.4946; amd64

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

### `eclipse-temurin:11-jdk-nanoserver` - windows version 10.0.20348.4052; amd64

```console
$ docker pull eclipse-temurin@sha256:373023e0c42e5b8099ca86ba07913c2f629ec10f34be818c94fe1f290e7bc5bc
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.5 MB (317482369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d5208c50df134a02028e1349678ebbf47e0d3c325373636db8274d1393bdb9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 12 Aug 2025 20:50:36 GMT
SHELL [cmd /s /c]
# Tue, 12 Aug 2025 20:50:37 GMT
ENV JAVA_VERSION=jdk-11.0.28+6
# Tue, 12 Aug 2025 20:50:38 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 12 Aug 2025 20:50:39 GMT
USER ContainerAdministrator
# Tue, 12 Aug 2025 20:50:43 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 12 Aug 2025 20:50:44 GMT
USER ContainerUser
# Tue, 12 Aug 2025 20:50:52 GMT
COPY dir:8b5aa3450b5ed8de1b2c81f4388b1a437f54688a5e8c6d990bf0f6727b917a6b in C:\openjdk-11 
# Tue, 12 Aug 2025 20:50:58 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 12 Aug 2025 20:50:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff74c81e4e9f8fb70d2c94bb1a2a222984c71b6444f1cceeffa739cb2f8fe7ea`  
		Last Modified: Tue, 12 Aug 2025 20:51:48 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952ecb4fbb04f8ebe06614ac6bbe684e122c5322a98e48b49cec394f67979c74`  
		Last Modified: Tue, 12 Aug 2025 20:51:49 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb5a3da1cdd83972318d32ab4c749dd519437c2125859e292aac2f987bee95e`  
		Last Modified: Tue, 12 Aug 2025 20:51:50 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f791afe4c7ff0892b329a82c7988c7fbf22a72c408610a6634b37340cfa55fe4`  
		Last Modified: Tue, 12 Aug 2025 20:51:50 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feed461223af0c64276e424c3cae76bb5ef12b6c06c86a19d22f7a5d54ff9327`  
		Last Modified: Tue, 12 Aug 2025 20:51:51 GMT  
		Size: 79.3 KB (79297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb84cc67daae841c6a563d21c6fda7cc64d1c4e6a2b22f40943c958c28656af`  
		Last Modified: Tue, 12 Aug 2025 20:51:51 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a371e0d0642100b256e461588bb5fe718df396320a7e5f119021a65d0460ed5`  
		Last Modified: Tue, 12 Aug 2025 21:14:04 GMT  
		Size: 194.6 MB (194618531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af600e9a17e6778b1cb30b6831fdb317abcb3f608726f5c8b25aa86b1599dc4e`  
		Last Modified: Tue, 12 Aug 2025 20:51:51 GMT  
		Size: 118.0 KB (118031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a78bc4979b646e175febf3586f29d6a37386a5c7dddcd71067965bf99cc1ef3`  
		Last Modified: Tue, 12 Aug 2025 20:51:57 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
