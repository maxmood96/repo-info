## `eclipse-temurin:17-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:bac3929c38b7e611687a6f4e10f7529c7b15bb349cc86bdf2e582e4df4e05cf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `eclipse-temurin:17-nanoserver` - windows version 10.0.26100.7171; amd64

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

### `eclipse-temurin:17-nanoserver` - windows version 10.0.20348.4405; amd64

```console
$ docker pull eclipse-temurin@sha256:ff264c05b0d1b7404889ea68d29562dd0eafab0bb194debbcae1ff23965532d2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (314049884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93454f24060fd40db0bbc8b19ff79c97a4a7de61635759d02c7f49addc447886`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Tue, 11 Nov 2025 20:11:36 GMT
SHELL [cmd /s /c]
# Tue, 11 Nov 2025 20:11:37 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Tue, 11 Nov 2025 20:11:37 GMT
ENV JAVA_HOME=C:\openjdk-17
# Tue, 11 Nov 2025 20:11:38 GMT
USER ContainerAdministrator
# Tue, 11 Nov 2025 20:11:39 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 11 Nov 2025 20:11:40 GMT
USER ContainerUser
# Tue, 11 Nov 2025 20:11:48 GMT
COPY dir:2018c1c9eb6dc671bed9b2018ab32e648d405ad10a017a184613d399d49818ed in C:\openjdk-17 
# Tue, 11 Nov 2025 20:11:52 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 11 Nov 2025 20:11:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c422c24444f92cd38b400c7780d321b06063f75701e2f199142de5f34b71c7e2`  
		Last Modified: Tue, 11 Nov 2025 20:12:16 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c75275d9bb3bf74ab87cd6d507572917b208964b8b3a8c9c245e09fffd38f6b`  
		Last Modified: Tue, 11 Nov 2025 20:12:16 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83026828a287fa708216a4fe5abe74faf8bd6638f65409cc41a9cfc6f75ce3b`  
		Last Modified: Tue, 11 Nov 2025 20:12:16 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a2f795c7b8d433167f63997ab5d32fbdf5872ab5fadf145d7d0c3754a677b6`  
		Last Modified: Tue, 11 Nov 2025 20:12:16 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9571d163f92785bbff4e752854827be7fbc2fc31afaa644a4da57cc8d03c6ad1`  
		Last Modified: Tue, 11 Nov 2025 20:12:16 GMT  
		Size: 76.7 KB (76737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21cb3b0959275c2a67b4412c85e30b3d69e2334893e9b278d1eb99471afd7335`  
		Last Modified: Tue, 11 Nov 2025 20:12:16 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c444970e3d9a94a3464dd1ed1bd3af4d472a5641f8585ccf303f75af891edcf7`  
		Last Modified: Tue, 11 Nov 2025 22:14:52 GMT  
		Size: 187.5 MB (187510968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21948e3fc81d70a7f2edf297fde963af7bfdac3062d3c6f332c5e69901f0b2dc`  
		Last Modified: Tue, 11 Nov 2025 20:12:16 GMT  
		Size: 106.7 KB (106741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805778b224ac292e75624afde33b0c18d1bdf8bc3fe8e2d247b0f08bda648ed5`  
		Last Modified: Tue, 11 Nov 2025 20:12:16 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
