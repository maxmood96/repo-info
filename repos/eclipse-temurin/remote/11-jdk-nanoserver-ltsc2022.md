## `eclipse-temurin:11-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:50051a14ac2396944b97cbad3f04be4e1a1865ed1ef16cb11dd5dd36c17caf5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `eclipse-temurin:11-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull eclipse-temurin@sha256:85c0353dca607dac1321472e74475247ba1631d3eea65bd783148f033a6c09ed
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.8 MB (314833010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b8be6bac596b7af0b2c78566bd0ed814499ffb18b9822b212b1fdbe6024e33a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 05 Mar 2024 19:20:30 GMT
RUN Apply image 10.0.20348.2340
# Wed, 13 Mar 2024 01:20:55 GMT
SHELL [cmd /s /c]
# Wed, 13 Mar 2024 01:22:12 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 13 Mar 2024 01:22:13 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 13 Mar 2024 01:22:14 GMT
USER ContainerAdministrator
# Wed, 13 Mar 2024 01:22:24 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 Mar 2024 01:22:24 GMT
USER ContainerUser
# Wed, 13 Mar 2024 01:22:39 GMT
COPY dir:06bb700052ae5de12c7654c6d453b954bdaac52e59d87856592b85cdd3ce67e9 in C:\openjdk-11 
# Wed, 13 Mar 2024 01:22:53 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 13 Mar 2024 01:22:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:94ec3b200bababb5c0b6605ad82c23779d8f918fbfe1ef5d1cf51be6f12fa749`  
		Last Modified: Tue, 12 Mar 2024 19:42:37 GMT  
		Size: 120.7 MB (120702694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e98336f720b829e374bd1d59306210d3700861b11d3df51506afbc0b50d039`  
		Last Modified: Wed, 13 Mar 2024 01:40:26 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cec0ab7bdc84c7aa3b0c0c4c4b84e98cd17a44675e5aef0388443ae7923001a0`  
		Last Modified: Wed, 13 Mar 2024 01:41:15 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:420c774977f18e4352760dca44ff0e80f039f2013474a4bf99a392b06410d3e8`  
		Last Modified: Wed, 13 Mar 2024 01:41:15 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f6e016984917d152557b477731fbf584f47af9d73a8c2389b3c01b63261a5f`  
		Last Modified: Wed, 13 Mar 2024 01:41:15 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a89721e219774f09c4f2794c70440ea679f22d71091d8fc3c548b47f282f1a5`  
		Last Modified: Wed, 13 Mar 2024 01:41:13 GMT  
		Size: 80.5 KB (80461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:019ffc3eefab32a7474135d7ed570d6d7477e71b4296d5e6fa81b532db7dadc7`  
		Last Modified: Wed, 13 Mar 2024 01:41:13 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8be07e6ee882022a3aff83f4edb5b2a96d266e4c43e4a676230e08c5100aec6`  
		Last Modified: Wed, 13 Mar 2024 01:41:30 GMT  
		Size: 194.0 MB (193981801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb8c60fd8b5128bfc8c1e32db4434bb3864e3b4359581203fcda98fc1f393b75`  
		Last Modified: Wed, 13 Mar 2024 01:41:13 GMT  
		Size: 61.1 KB (61081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0ecc380fb67b0e1059f8e64630c6ee218bcc2f12d5d915cb3958557262ec2f`  
		Last Modified: Wed, 13 Mar 2024 01:41:13 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
