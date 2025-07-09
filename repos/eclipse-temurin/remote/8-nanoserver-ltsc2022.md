## `eclipse-temurin:8-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:4b13a129ca3076bb8298e1efbeb2449a393d978275e4084eb02589a2f1746154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3932; amd64

### `eclipse-temurin:8-nanoserver-ltsc2022` - windows version 10.0.20348.3932; amd64

```console
$ docker pull eclipse-temurin@sha256:cae3cc6519dbecaaed9080ee09a821ad405262ae6bb09f73fc4e86d626d2b6ee
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.3 MB (225260432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a99d6d995fbd28b4a4385f46b51a5cfd6d1bbf5b94fb53f9840f921515a4781b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Jul 2025 05:15:23 GMT
RUN Apply image 10.0.20348.3932
# Wed, 09 Jul 2025 19:12:43 GMT
SHELL [cmd /s /c]
# Wed, 09 Jul 2025 19:12:45 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Wed, 09 Jul 2025 19:12:46 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 09 Jul 2025 19:12:47 GMT
USER ContainerAdministrator
# Wed, 09 Jul 2025 19:12:50 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Jul 2025 19:12:51 GMT
USER ContainerUser
# Wed, 09 Jul 2025 19:12:57 GMT
COPY dir:5c4bbf817a67c787f7f2d8809dee99be16882c3512e063f4e47205ca5ccbd190 in C:\openjdk-8 
# Wed, 09 Jul 2025 19:13:03 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:b1cf2c299ff70c52cb8ecf52e66d64d5068519867510919d8807ed2c58a54ba2`  
		Last Modified: Tue, 08 Jul 2025 21:55:51 GMT  
		Size: 122.6 MB (122630906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f638263b6397e28c2e8f70195f315ccc25e17441d4b981a38f8f8f320470d5c`  
		Last Modified: Wed, 09 Jul 2025 19:13:27 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8277e6ac0b0d37cce29f0cad1814648d4d3ceab06278317f28c6a97477bae67b`  
		Last Modified: Wed, 09 Jul 2025 19:13:27 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1bf9b2093366cb145d52985b8b3026452864afc86847dff1ae981fe0e78342f`  
		Last Modified: Wed, 09 Jul 2025 19:13:28 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccf814292c0ab0cbf77c4759ccba05244286829ab4c7f2d3ac8d8f47a8e7cda7`  
		Last Modified: Wed, 09 Jul 2025 19:13:28 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae71bcf1eb3c74baec30b64ce4bf82b0134323add9cb54a40bb4d5c12e107366`  
		Last Modified: Wed, 09 Jul 2025 19:13:28 GMT  
		Size: 77.7 KB (77696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444005d3e99ba94469fe1c61e22773f8932afbd3198454eab19424cd4cf77190`  
		Last Modified: Wed, 09 Jul 2025 19:13:28 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b401cbb2a2c1e57fb340ea79bfd37ed5612aab79955f4f8a1557ff36af11112d`  
		Last Modified: Wed, 09 Jul 2025 19:13:41 GMT  
		Size: 102.4 MB (102439185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a28f9d6fc9827743703ac0422691a8ede30365d2d2a3bd0f283a9c6a71f157`  
		Last Modified: Wed, 09 Jul 2025 19:13:28 GMT  
		Size: 107.5 KB (107489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
