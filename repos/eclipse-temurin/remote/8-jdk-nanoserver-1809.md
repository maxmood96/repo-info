## `eclipse-temurin:8-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:ce67984ed3f65405428f46e438b27d3d95355eb98a7b65de638b0d647f5d05bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `eclipse-temurin:8-jdk-nanoserver-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull eclipse-temurin@sha256:fd96cb94c9a1aa2427843f810cb1a25dbef49bc201e47b806ff7500b091f6363
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.8 MB (256812402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d740ace5caf108296987c47889d10b9eba4aa982dfe75e779fe379511f3e5c5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Wed, 09 Oct 2024 23:37:31 GMT
SHELL [cmd /s /c]
# Wed, 09 Oct 2024 23:37:32 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Wed, 09 Oct 2024 23:37:32 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 09 Oct 2024 23:37:33 GMT
USER ContainerAdministrator
# Wed, 09 Oct 2024 23:37:44 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Oct 2024 23:37:44 GMT
USER ContainerUser
# Wed, 09 Oct 2024 23:37:54 GMT
COPY dir:cf98fec7e439356342f3bf03fb67b0dac0e213296a20d5e427a9ebba9080193e in C:\openjdk-8 
# Wed, 09 Oct 2024 23:38:07 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6adfd98d9a05d48859cfa5f6e1dc162be56797c9e86e7647518192a16af3d27`  
		Last Modified: Thu, 10 Oct 2024 00:20:41 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28727a74df40b2463e1a5c1193cfe1cdb7fb960e48c494fa660b684f819aa7cb`  
		Last Modified: Thu, 10 Oct 2024 00:20:41 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27762712ab2901171f32f9f1dff0dda3fab334a6afe54dd0b39410e30b87be64`  
		Last Modified: Thu, 10 Oct 2024 00:20:40 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf55c537b39610846d2772cd1ad8a8a7a7330caaa2f96f10bdf95e4c0d61795`  
		Last Modified: Thu, 10 Oct 2024 00:20:38 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:818b97d2f0d5ad2b52d52882f709abfa91d0ee153d932d4c1464df9f5096ad85`  
		Last Modified: Thu, 10 Oct 2024 00:20:39 GMT  
		Size: 74.7 KB (74666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56b7c61cfcfe51d03564ff77bddcbd529b38927e2eae0d3b61951e505f209157`  
		Last Modified: Thu, 10 Oct 2024 00:20:38 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d74f2423e3fb75f8a49261a91ad6f2b4c0ceb37415f923e508d35440bb4d2e4`  
		Last Modified: Thu, 10 Oct 2024 00:20:51 GMT  
		Size: 101.5 MB (101544437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1dde14e5901028e7bb1c3dc064074202bc8aafd9017a7132e46f834b454896c`  
		Last Modified: Thu, 10 Oct 2024 00:20:39 GMT  
		Size: 93.9 KB (93890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
