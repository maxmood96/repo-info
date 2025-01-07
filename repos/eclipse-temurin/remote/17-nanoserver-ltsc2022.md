## `eclipse-temurin:17-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:44efc77b85d76394abc0827f484dc99620cdb3f4144c4fea0a1b38440e19ac6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `eclipse-temurin:17-nanoserver-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull eclipse-temurin@sha256:dec074c0e29550eb0411663d984fd01e9bc2d5343329507f06d7c5a685b37757
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.1 MB (309095044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c23129738b37106932087c392b14bd58aaca6e6651449b23ba546ab4253c0af9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Dec 2024 01:18:54 GMT
RUN Apply image 10.0.20348.2966
# Wed, 11 Dec 2024 21:43:11 GMT
SHELL [cmd /s /c]
# Wed, 11 Dec 2024 21:43:12 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Wed, 11 Dec 2024 21:43:13 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 11 Dec 2024 21:43:13 GMT
USER ContainerAdministrator
# Wed, 11 Dec 2024 21:43:16 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 11 Dec 2024 21:43:16 GMT
USER ContainerUser
# Wed, 11 Dec 2024 21:43:23 GMT
COPY dir:52d780064906626480ed3e0e10c20681fda9fbf2926de2858bcee46524c2c3aa in C:\openjdk-17 
# Wed, 11 Dec 2024 21:43:29 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 11 Dec 2024 21:43:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f9d5d5ca3244fc2c429a892cbe6066394790f649f32d59acfdf012e490896378`  
		Last Modified: Tue, 10 Dec 2024 18:34:17 GMT  
		Size: 120.6 MB (120601318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf4f6d103501611228fce046c7f2fc8ff0697e6cb4d8fcafb923bc590654530`  
		Last Modified: Wed, 11 Dec 2024 21:43:35 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3ac4e76bb28855a0b60f319890fdf9db413b078ea1d9db61cffefc3aebe386`  
		Last Modified: Wed, 11 Dec 2024 21:43:35 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0563045832f8b0231e81c97c2efcab4509d0203389f06126a536ab8f7d069e6c`  
		Last Modified: Wed, 11 Dec 2024 21:43:35 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ea0c642c73972d1f9df79860b7cf415b44f7636cd99106e35eeab007150c61`  
		Last Modified: Wed, 11 Dec 2024 21:43:35 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b656844444f6c32820c4e2fd6eb0697e478ec00ed001ac6d0d1c9f4c943263`  
		Last Modified: Wed, 11 Dec 2024 21:43:33 GMT  
		Size: 76.7 KB (76721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ed8736eb6ab963790dbc8e06f936e102edff7002147928fe885024768390ecf`  
		Last Modified: Wed, 11 Dec 2024 21:43:33 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4683b1892730c95e038501963723951952d824ffd938613407c88b30e8b9bf`  
		Last Modified: Wed, 11 Dec 2024 21:43:43 GMT  
		Size: 188.3 MB (188303761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:399c4c8558cffabc37c64e8178d457868bf30b539402acad75f1b0b7404e0552`  
		Size: 107.1 KB (107068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1119839ade91827ad8d810abf2c1f0b901858f530462702dd808d2aacaf84a`  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
