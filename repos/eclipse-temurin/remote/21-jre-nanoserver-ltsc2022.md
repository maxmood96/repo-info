## `eclipse-temurin:21-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:d1e5155949ca93374c0a5595cbb5179f98dfbca5966b948518ec212cfb0136ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `eclipse-temurin:21-jre-nanoserver-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull eclipse-temurin@sha256:65c1205182decf0dfef2f27db8a7953d2c71fccb69cbed8eb573fa288ed7d5de
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.4 MB (170425335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:833ec730982102c7eea4049f617ef7524bd016e737b28aa26da5fad22272fe0c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 12 Jan 2025 09:54:50 GMT
RUN Apply image 10.0.20348.3091
# Wed, 15 Jan 2025 18:01:48 GMT
SHELL [cmd /s /c]
# Wed, 15 Jan 2025 18:01:48 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Wed, 15 Jan 2025 18:01:49 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 15 Jan 2025 18:01:50 GMT
USER ContainerAdministrator
# Wed, 15 Jan 2025 18:01:52 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 Jan 2025 18:01:52 GMT
USER ContainerUser
# Wed, 15 Jan 2025 18:01:56 GMT
COPY dir:d301f311784d572cc6cc0a5ee90712dcade9d3f8b4a48a0f2df4274582f5072e in C:\openjdk-21 
# Wed, 15 Jan 2025 18:02:00 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:fd3058b29fbd287119a2fa4d2d36a46fdee3bbada5fd9ef6f02f2d7d4cc143ab`  
		Last Modified: Tue, 14 Jan 2025 20:27:35 GMT  
		Size: 120.7 MB (120661554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05a01e615305dd2d16888a74c4ed26ec69cae6b71242786f21768b77969d2a36`  
		Last Modified: Wed, 15 Jan 2025 18:02:05 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed3a5175961301d6051424913862ddc65557d0d6266b81dded813e01473a95f4`  
		Last Modified: Wed, 15 Jan 2025 18:02:05 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:019fb5e9231428e85262335d8edf23b79fc066a47913a629ccee8fc13cfedf18`  
		Last Modified: Wed, 15 Jan 2025 18:02:05 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d5ad51951169cd60a0fa27fb8bedc2ab0bb1fd2279fa97e16a9946fc86c1f8e`  
		Last Modified: Wed, 15 Jan 2025 18:02:03 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cce615580c4e000b1500fa84ec3970da988e13c6d9e8a84a87f35ca9d74f7fc`  
		Last Modified: Wed, 15 Jan 2025 18:02:03 GMT  
		Size: 75.5 KB (75510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5499412ef408b4d9578999ccab9e545326194c2d5ab819619f721c2d07c4d5e5`  
		Last Modified: Wed, 15 Jan 2025 18:02:03 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88783bb9c41c68b14f89574168d7b159b2071f802b2140a3b67c317a46b5c9b3`  
		Last Modified: Wed, 15 Jan 2025 18:02:09 GMT  
		Size: 49.6 MB (49586266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6f435b804482f07e9557010ec96fe004ae65d4bf9060f1a30045a21dbbda69`  
		Last Modified: Wed, 15 Jan 2025 18:02:03 GMT  
		Size: 96.8 KB (96823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
