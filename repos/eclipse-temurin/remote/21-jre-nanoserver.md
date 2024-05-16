## `eclipse-temurin:21-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:e30532da3dbc9b668846d8a05a74b3f9928a8cb67af021deee7c333a27e9b56f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `eclipse-temurin:21-jre-nanoserver` - windows version 10.0.20348.2461; amd64

```console
$ docker pull eclipse-temurin@sha256:d6876eaab500b89a54a0192cb45e71d00aaab35bdf8535dbd85d2b30b26375fd
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.3 MB (169316895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbc8270ad9678d5a36af13d8b35a59f1ed8c38b32981aad4c6e820f337344e2b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 10 May 2024 20:16:48 GMT
RUN Apply image 10.0.20348.2461
# Wed, 15 May 2024 20:32:41 GMT
SHELL [cmd /s /c]
# Wed, 15 May 2024 20:36:55 GMT
ENV JAVA_VERSION=jdk-21.0.3+9
# Wed, 15 May 2024 20:36:55 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 15 May 2024 20:36:56 GMT
USER ContainerAdministrator
# Wed, 15 May 2024 20:37:05 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 May 2024 20:37:06 GMT
USER ContainerUser
# Wed, 15 May 2024 20:37:55 GMT
COPY dir:30866ffc44919960ba2d43fceab02c0cbcad12e73e3b28316799617dca9a13d0 in C:\openjdk-21 
# Wed, 15 May 2024 20:38:08 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:90b3a5622f8d62905d0a3029df4f91b934558ad375bef25c596214df31acac88`  
		Last Modified: Tue, 14 May 2024 17:22:15 GMT  
		Size: 120.4 MB (120425316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5560c76ac3d9aa2d8a6dbf79d443a7e1d170aae31c940cf791c9b532d5756a1`  
		Last Modified: Wed, 15 May 2024 20:58:04 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda6608870fce2c13c86ab91e9f607b9862d3c548045bee576d9baefd3d22f7c`  
		Last Modified: Wed, 15 May 2024 21:00:29 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0518617a8ea970e9e5195ac41a01ca64cf3a72c2e847651581d470838aeeb2e8`  
		Last Modified: Wed, 15 May 2024 21:00:28 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d665857a6bb1e36593f7c70701084ce53ef295002e87e14ff06eefa459da285`  
		Last Modified: Wed, 15 May 2024 21:00:28 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233c65ea3e60064f4860406b1ebdc9e6f0a9c673c0088e35e7a4976263dff606`  
		Last Modified: Wed, 15 May 2024 21:00:26 GMT  
		Size: 74.3 KB (74347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c280ad1b4f912c4574466274c8fad293d115b0e3abc25ca4e3e87d41a41918`  
		Last Modified: Wed, 15 May 2024 21:00:26 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444ec5383156dcf19a5b3ebf890aae9321399f3f4ee13bf96b8ca078b92f740d`  
		Last Modified: Wed, 15 May 2024 21:01:06 GMT  
		Size: 48.7 MB (48749847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:631bc5aec5c871655f0e1072fda677ae081a84f87aec6f04a2b233bc75cd7f91`  
		Last Modified: Wed, 15 May 2024 21:00:57 GMT  
		Size: 61.6 KB (61554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre-nanoserver` - windows version 10.0.17763.5820; amd64

```console
$ docker pull eclipse-temurin@sha256:b6ecc4a941ba48c9c67e252e300762d9a2cf26773d3b6c777e9f6044757c5e7c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.1 MB (207140667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c41aadaf2a1434062086207a23478d085155e4ff21111fa52c06bef80a03a534`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
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
# Wed, 15 May 2024 20:21:03 GMT
COPY dir:30866ffc44919960ba2d43fceab02c0cbcad12e73e3b28316799617dca9a13d0 in C:\openjdk-21 
# Wed, 15 May 2024 20:21:14 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
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
	-	`sha256:b19d88d104d426267c25fa419d8e14b759a519af11d256438debe36c93a93209`  
		Last Modified: Wed, 15 May 2024 20:55:07 GMT  
		Size: 48.8 MB (48758824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c816df84db4e89a349e5371b6034c0ee23d86f3464a2df6430397a76bca7845`  
		Last Modified: Wed, 15 May 2024 20:54:59 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
