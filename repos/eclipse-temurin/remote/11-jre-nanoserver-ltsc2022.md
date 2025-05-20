## `eclipse-temurin:11-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:f059498ae7cc2bb1b94cf8c8426548092c461b7fafe87c3d213419abba302456
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `eclipse-temurin:11-jre-nanoserver-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull eclipse-temurin@sha256:e9d53e4c4c6bd0b84bd5bbdf76a984d905268d067f9e63f7641ff059b116c706
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.4 MB (166421517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ccfcb0d5883875f009d4080d4a61839d1e4d5e623439abc767c19aa26159db`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Wed, 14 May 2025 21:12:38 GMT
SHELL [cmd /s /c]
# Wed, 14 May 2025 21:12:38 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 14 May 2025 21:12:39 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 14 May 2025 21:12:40 GMT
USER ContainerAdministrator
# Wed, 14 May 2025 21:12:43 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 14 May 2025 21:12:44 GMT
USER ContainerUser
# Wed, 14 May 2025 21:12:48 GMT
COPY dir:d6f4a8ae4843d3009794ef7988392b65ed4dd8f1da131593f0c13b36f9fcbd8a in C:\openjdk-11 
# Wed, 14 May 2025 21:12:52 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Tue, 13 May 2025 19:42:18 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f938df684a7c14cb4f344109b3713ce9bd9f9c9dfb793f73abfc809a7145bb`  
		Last Modified: Wed, 14 May 2025 21:12:58 GMT  
		Size: 1.1 KB (1092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bba672c21645500d8786ee442481ca1b2b4daf44b763c82aa4e45e6de73e5b9`  
		Last Modified: Wed, 14 May 2025 21:13:02 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f028fb9c4ca7b78ae451336d91230b49211793210991f6c30839da295299f03d`  
		Last Modified: Wed, 14 May 2025 21:12:58 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c6cb09a5847b4b91ecc782e79245e0be555b4a1daad88399476d450922faa54`  
		Last Modified: Wed, 14 May 2025 21:12:56 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66d05cd0c8c6f40d85ccdcb0b09896a6a03b1cd21ee7c4b7ebecf46e50b0ddfe`  
		Last Modified: Wed, 14 May 2025 21:12:56 GMT  
		Size: 77.6 KB (77579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:719bb59e970f4366a571b4ce0934c5b274ef22c2488c1796c7a5f66ed10865d3`  
		Last Modified: Wed, 14 May 2025 21:12:56 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d96d8695b3845f4ab5886676f009ed8a43453316d7d9a31ded34161c1088d9db`  
		Last Modified: Wed, 14 May 2025 21:13:00 GMT  
		Size: 43.7 MB (43664042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2019e97d5d75058359e7873bd1d6fcf93a4f58024767669b5ddddfdb0a328a9`  
		Last Modified: Wed, 14 May 2025 21:12:56 GMT  
		Size: 97.9 KB (97940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
