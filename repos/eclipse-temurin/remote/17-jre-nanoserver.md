## `eclipse-temurin:17-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:adf2be78afa47d7f5c859cff9456939582261611d8f1c64f6bf9a9318a9afcc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `eclipse-temurin:17-jre-nanoserver` - windows version 10.0.20348.2966; amd64

```console
$ docker pull eclipse-temurin@sha256:2a3683ee6535f15bb28e8ecad5fe37a235332fb4a46f267a87c952346594cc6e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.1 MB (165142368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b161c5ed02e296459650bd4d2920299e56689ac382121dc6d56776149c78c1d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Dec 2024 01:18:54 GMT
RUN Apply image 10.0.20348.2966
# Wed, 11 Dec 2024 21:50:25 GMT
SHELL [cmd /s /c]
# Wed, 11 Dec 2024 21:50:26 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Wed, 11 Dec 2024 21:50:26 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 11 Dec 2024 21:50:27 GMT
USER ContainerAdministrator
# Wed, 11 Dec 2024 21:50:29 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 11 Dec 2024 21:50:29 GMT
USER ContainerUser
# Wed, 11 Dec 2024 21:50:33 GMT
COPY dir:4c6d77ca6f58a330005c5f34389fe1882335ea3db28c021259e868cb18ddb756 in C:\openjdk-17 
# Wed, 11 Dec 2024 21:50:37 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:f9d5d5ca3244fc2c429a892cbe6066394790f649f32d59acfdf012e490896378`  
		Last Modified: Tue, 10 Dec 2024 18:34:17 GMT  
		Size: 120.6 MB (120601318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae6c6bdc6426b545bbcc2f77097322383ebd65c7206acc0b4b4861d3beeb325`  
		Last Modified: Wed, 11 Dec 2024 21:50:41 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9990302f2983d2237ad28822328fec5d81e96f228b2615627ed0a32fd0f93612`  
		Last Modified: Wed, 11 Dec 2024 21:50:41 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b792c02401e9e31fe79813eb563c5abd0d154f63a709af13763cc40c71cfe05`  
		Last Modified: Wed, 11 Dec 2024 21:50:41 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e8c3fa67dc975b777e71c2d9cae125c9347a34a4978c83ba323bc889629b947`  
		Last Modified: Wed, 11 Dec 2024 21:50:40 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4fd67ab762d0374e8ea7a32cf688f71d860fdf0b030e5e46de28ae113de4776`  
		Size: 77.7 KB (77685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67690accfabae65f804ce841bc14ecf97a05a0999e2773ab2f1ebde1bc6d9714`  
		Last Modified: Wed, 11 Dec 2024 21:50:40 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8a48e323b13e88de5d4ff5b91a7fd616081cf4798832fffae0fba4e720d89f7`  
		Size: 44.4 MB (44360064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa26d3f009ae9d461b155656f983999243c2ac10a7b550faedd1c8e9b06506f`  
		Last Modified: Wed, 11 Dec 2024 21:50:40 GMT  
		Size: 98.0 KB (97970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jre-nanoserver` - windows version 10.0.17763.6659; amd64

```console
$ docker pull eclipse-temurin@sha256:ff03263473930091fb4ce59750ae284c66349566fd8a52d20312b0179d891726
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202670937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdb85a58dc6b04706526f42c5ac64e6e7b4d05f630033381ebb82f8f167e1654`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Dec 2024 04:54:21 GMT
RUN Apply image 10.0.17763.6659
# Wed, 11 Dec 2024 21:42:18 GMT
SHELL [cmd /s /c]
# Wed, 11 Dec 2024 21:42:19 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Wed, 11 Dec 2024 21:42:19 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 11 Dec 2024 21:42:20 GMT
USER ContainerAdministrator
# Wed, 11 Dec 2024 21:42:22 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 11 Dec 2024 21:42:22 GMT
USER ContainerUser
# Wed, 11 Dec 2024 21:42:26 GMT
COPY dir:4c6d77ca6f58a330005c5f34389fe1882335ea3db28c021259e868cb18ddb756 in C:\openjdk-17 
# Wed, 11 Dec 2024 21:42:30 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:fc1cdf36537340b1875b5d6573a58a268fc20b63dc54a780f9070e51cf9eb9ca`  
		Last Modified: Tue, 10 Dec 2024 21:03:34 GMT  
		Size: 155.2 MB (155231618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4041cdc3de0123f009fdb45c35448c5da71423bc08af4d6d231c67d516dc7af`  
		Last Modified: Wed, 11 Dec 2024 21:42:36 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f59aad8e34cb07df8a271ba05d1ccad181b0e3deb1c5313744442cbcc64b2364`  
		Last Modified: Wed, 11 Dec 2024 21:42:35 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2055d5286ad0862072fff3192865c2ebef87e5d0cf8de8ef6cdcc277b12d8d8d`  
		Last Modified: Wed, 11 Dec 2024 21:42:35 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4cd071c45c436e57ed59bc69747d37f2b1b2871bbb972cd8f2c83a9211897b`  
		Last Modified: Wed, 11 Dec 2024 21:42:33 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c4016a1d09d22e56037429de83f6ab70cbcced60a4111857acebd3706847d1`  
		Last Modified: Wed, 11 Dec 2024 21:42:33 GMT  
		Size: 71.7 KB (71713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7000229b8d18b427862fcca32835c91499f474bf0d2b4ac43abc40032267c0d`  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d6582f386c9c0a6888f79dead48ec7e6956d308c15902f9ed5a3d5c7a48662`  
		Last Modified: Wed, 11 Dec 2024 21:42:39 GMT  
		Size: 44.4 MB (44359385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c716a027743a8888117b2c10e6f05ff0e866dd4c4fd114506b1268ea6011cd6e`  
		Last Modified: Wed, 11 Dec 2024 21:42:34 GMT  
		Size: 3.0 MB (3003006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
