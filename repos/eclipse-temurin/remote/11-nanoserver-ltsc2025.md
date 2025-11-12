## `eclipse-temurin:11-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:c6f8adb1c3c932b616d8f83ddf54603456515fdf3185d5acd2309a6250406971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `eclipse-temurin:11-nanoserver-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull eclipse-temurin@sha256:1c2ace8b698310c5ce2930148e6da477dfc3307b6ed2177ca7f0a300ddbd0ce5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.8 MB (392794983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dde68496688b2663294f269704e8b983f35686cd20d3c43035d1f52fbc1e03b0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 09 Nov 2025 10:04:50 GMT
RUN Apply image 10.0.26100.7171
# Tue, 11 Nov 2025 20:11:08 GMT
SHELL [cmd /s /c]
# Tue, 11 Nov 2025 20:11:09 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Tue, 11 Nov 2025 20:11:09 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 11 Nov 2025 20:11:09 GMT
USER ContainerAdministrator
# Tue, 11 Nov 2025 20:11:13 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 11 Nov 2025 20:11:13 GMT
USER ContainerUser
# Tue, 11 Nov 2025 20:11:30 GMT
COPY dir:207a50c3961430a3231a748eb9ce354eec00313f0753b2d5e8f279d3afd46cd8 in C:\openjdk-11 
# Tue, 11 Nov 2025 20:11:35 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 11 Nov 2025 20:11:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:87c91227213eb6e7c8cfe33b6bd0429350e524756878f37f3860b013f804bf59`  
		Last Modified: Tue, 11 Nov 2025 20:41:49 GMT  
		Size: 197.9 MB (197936447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6194cd77702c569004d9457e0c06be0662b8256bcd8f00c1d770f01827ff09e`  
		Last Modified: Tue, 11 Nov 2025 20:12:01 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67871f81b5ec40ac602e45a83ebe454e076338464f766992203bc1f53f4e1a35`  
		Last Modified: Tue, 11 Nov 2025 20:12:01 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c35afdfbbc4c4b0757cc4c62c9ebc693d58f784680717e31026a5c9067ae2db`  
		Last Modified: Tue, 11 Nov 2025 20:12:02 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e791920643a287ad1c39321fa982e9dec7b3587424d99d26b6554d861f686d`  
		Last Modified: Tue, 11 Nov 2025 20:12:02 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef790762d90ad66ecef8715e67bffff3b1d67033204833d8cf9b46d4f986fdf`  
		Last Modified: Tue, 11 Nov 2025 20:12:02 GMT  
		Size: 69.4 KB (69449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c973c6572d8c7d29ac1d3f9489cd0cf6a0d741c2e1f87cd84dba78f5666b318`  
		Last Modified: Tue, 11 Nov 2025 20:12:02 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16b0aa9daeedbef78d5ef96ba6d82ea4924d3dd24903e783786de787748ca5a`  
		Last Modified: Tue, 11 Nov 2025 22:13:01 GMT  
		Size: 194.7 MB (194670594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c90c2e6e877d122887029383a02ef8cdce9a5a92aec6c67aa97060be1007e1`  
		Last Modified: Tue, 11 Nov 2025 20:12:02 GMT  
		Size: 112.1 KB (112140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd1d483696e0605e62da83b7ce480d25f9ce7a73f43a76b6450d22eaeedd0061`  
		Last Modified: Tue, 11 Nov 2025 20:12:02 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
