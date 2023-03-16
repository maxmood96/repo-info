## `eclipse-temurin:17-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:0877353881b09c0eec4dab49d9ffe23a26cb17d1452288993f1b026d90686acd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1607; amd64

### `eclipse-temurin:17-nanoserver-ltsc2022` - windows version 10.0.20348.1607; amd64

```console
$ docker pull eclipse-temurin@sha256:8b0c865b101e7d3d186e57661c242b506b775c612911d82110b76370c06c595a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.8 MB (307811017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f58a1f2ca42fff69f296b1be5faee029210e6d26f16c90a3e17adb2e25276c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 10 Mar 2023 06:31:34 GMT
RUN Apply image 10.0.20348.1607
# Thu, 16 Mar 2023 01:29:33 GMT
SHELL [cmd /s /c]
# Thu, 16 Mar 2023 01:33:25 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 16 Mar 2023 01:33:26 GMT
ENV JAVA_HOME=C:\openjdk-17
# Thu, 16 Mar 2023 01:33:27 GMT
USER ContainerAdministrator
# Thu, 16 Mar 2023 01:33:38 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 16 Mar 2023 01:33:39 GMT
USER ContainerUser
# Thu, 16 Mar 2023 01:33:55 GMT
COPY dir:b9d1887161cde3cc24ae2101d8a284bfc20814b15fed427bc1c905c1248fb0bf in C:\openjdk-17 
# Thu, 16 Mar 2023 01:34:36 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 16 Mar 2023 01:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7abf0a70d48bf65f3d985f5780d4bdaece36f1f4bb8be10d5a6aacce33dacc75`  
		Last Modified: Thu, 16 Mar 2023 01:54:24 GMT  
		Size: 122.2 MB (122171731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a611a20686e9374e3a55a49399506f83c041ae711ed47018c2267c341156dd97`  
		Last Modified: Thu, 16 Mar 2023 01:53:50 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9653c7841fe2911686bb05797100e5d3aac112a6c5a31fd109fdf273c3c7d81`  
		Last Modified: Thu, 16 Mar 2023 01:55:45 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d961af1d066326c8e1186fbc6876a3d4dbe91d3d6872218505bec61dd725a21f`  
		Last Modified: Thu, 16 Mar 2023 01:55:45 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b69ba0af288067e9cca1f23c1de2ead5658b53ed2546ea3de73c6f4e1b897504`  
		Last Modified: Thu, 16 Mar 2023 01:55:45 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1548f7ad98467d9f81b01049dc8293c2e89075b47855b6bbd4ec968122d401d`  
		Last Modified: Thu, 16 Mar 2023 01:55:43 GMT  
		Size: 80.0 KB (80016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24269970d76158337295eb022f62b2023eea8965be236222ea57b4f5ccbc6159`  
		Last Modified: Thu, 16 Mar 2023 01:55:43 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d466b70892a902e66a98a465c889f98691e262c776119b05363bd767add03f`  
		Last Modified: Thu, 16 Mar 2023 01:56:04 GMT  
		Size: 185.5 MB (185456425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf93481ed42c92b3232cb483e92ffb080186c7df5c9a5dd16e7be0f45048b5e8`  
		Last Modified: Thu, 16 Mar 2023 01:55:43 GMT  
		Size: 95.9 KB (95853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:386de6621e693368b294048039e6bb8935f07150c98cf844c4afb1f03a782af4`  
		Last Modified: Thu, 16 Mar 2023 01:55:43 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
