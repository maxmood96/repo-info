## `eclipse-temurin:21-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:e2023c9df0ca19f21c4c63a97ea9e1ecd1668cfec5219132e4977475fbea1a66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `eclipse-temurin:21-jdk-nanoserver-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull eclipse-temurin@sha256:03aeae94a22b6e0b27e6b6f42f84d6b5094d1169698def0d76568fd1879e04c4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.0 MB (359980691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7e651e026ad4453b6a9b411cbbbd5ab7f64b344ee3e15838f17c29568e4cbaf`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Wed, 15 May 2024 19:42:01 GMT
SHELL [cmd /s /c]
# Wed, 15 May 2024 20:15:47 GMT
ENV JAVA_VERSION=jdk-21.0.3+9
# Wed, 15 May 2024 20:15:47 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 15 May 2024 20:15:48 GMT
USER ContainerAdministrator
# Wed, 15 May 2024 20:15:59 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 May 2024 20:15:59 GMT
USER ContainerUser
# Wed, 15 May 2024 20:16:17 GMT
COPY dir:23b4ead9c2036754f644b00182bded9da6af0a8e5b9adaf18f46a103fb435a07 in C:\openjdk-21 
# Wed, 15 May 2024 20:16:30 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 15 May 2024 20:16:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6a511fea8e874efc08e5058ac5b12b6433c36ba6570862a619dd80cfb0e190`  
		Last Modified: Wed, 15 May 2024 20:45:52 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4841491247350a2cba22e1d7deecfc13e43a405a6bf7b96689d0b169bf4a4fe0`  
		Last Modified: Wed, 15 May 2024 20:53:51 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a6273893979eaf90f1cf0ba4b42c4c9369bf97d556f2e62ba9fa4eff08f910`  
		Last Modified: Wed, 15 May 2024 20:53:51 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c33ee8b266be6936b2f35575cf3a5a5383bee76bbe81975578e99f6651514d`  
		Last Modified: Wed, 15 May 2024 20:53:50 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d775a9c260301bb3c11962dba072c4a531ef28a1f85dc32dd705e3e05daad8e`  
		Last Modified: Wed, 15 May 2024 20:53:49 GMT  
		Size: 68.4 KB (68439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18782632469d51a768f172daa64d27fc8cca50a0276127a4c4f5ef26e28973fb`  
		Last Modified: Wed, 15 May 2024 20:53:49 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597db69c94367a5058f268265337e52e14d52dbe49f6444eb6310f9b062de27f`  
		Last Modified: Wed, 15 May 2024 20:54:08 GMT  
		Size: 201.1 MB (201147743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96666d60f4890b69fe1cbda68f88ca4aa5ee89d90505905ab1274f34700c1fc6`  
		Last Modified: Wed, 15 May 2024 20:53:50 GMT  
		Size: 3.8 MB (3816668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c6d6e7546e5d13be27a18c32509f449b54d1dca8692ef0cf01e95d7faafa2b`  
		Last Modified: Wed, 15 May 2024 20:53:49 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
