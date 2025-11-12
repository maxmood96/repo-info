## `eclipse-temurin:17-jdk-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:1455c86fd6290561dd1877e62b30a8d05ac5ca4309a712d9dafebeb6c22d10cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `eclipse-temurin:17-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull eclipse-temurin@sha256:68e3bd5a8bdadb384eed25479fd992aaa47b941fb79fdbe953c0d30fe11fc27e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.6 MB (385641487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d74f6527d6d341d0dade65e4e258e50a4d6edeeaba29998901e0ba78315a7fdf`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 09 Nov 2025 10:04:50 GMT
RUN Apply image 10.0.26100.7171
# Tue, 11 Nov 2025 20:11:08 GMT
SHELL [cmd /s /c]
# Tue, 11 Nov 2025 20:12:09 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Tue, 11 Nov 2025 20:12:09 GMT
ENV JAVA_HOME=C:\openjdk-17
# Tue, 11 Nov 2025 20:12:09 GMT
USER ContainerAdministrator
# Tue, 11 Nov 2025 20:12:11 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 11 Nov 2025 20:12:11 GMT
USER ContainerUser
# Tue, 11 Nov 2025 20:12:25 GMT
COPY dir:2018c1c9eb6dc671bed9b2018ab32e648d405ad10a017a184613d399d49818ed in C:\openjdk-17 
# Tue, 11 Nov 2025 20:12:30 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 11 Nov 2025 20:12:30 GMT
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
	-	`sha256:8386bf9ee217fcc51740a187f977f70e2fa30b37cd8a83d5f856c2faa24572c1`  
		Last Modified: Tue, 11 Nov 2025 20:12:55 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc83d16d84279b0c7acebcd504e8d67b2206ebec599b8bfcf1e32e3346029e7`  
		Last Modified: Tue, 11 Nov 2025 20:12:55 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b1b7dc58ece1342ee7577c2d85c39eaa6c1c88a6c66151c3aa602482384e66`  
		Last Modified: Tue, 11 Nov 2025 20:12:55 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0075601ebe65ebe627765e0c881faeaf4c3b5f9b7e4aea39bca0f5f87baf997f`  
		Last Modified: Tue, 11 Nov 2025 20:12:56 GMT  
		Size: 72.2 KB (72180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7b55980e738159c174d6cfe47bb75f090c1f32dbdd635e945d4b6d658251410`  
		Last Modified: Tue, 11 Nov 2025 20:13:01 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aaf27fcd08da4abea188a31fbd2191dd5ede51355b67d5eca1a1b7489f718ac`  
		Last Modified: Tue, 11 Nov 2025 22:14:57 GMT  
		Size: 187.5 MB (187511004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c71df17de93721249920ca62b244094d6074897917e7236e89e96564cf1780`  
		Last Modified: Tue, 11 Nov 2025 20:12:56 GMT  
		Size: 115.5 KB (115463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60a7850e87c662eae424c2353f62dda601c867bed55160d2ea507e311fdc234`  
		Last Modified: Tue, 11 Nov 2025 20:12:56 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
