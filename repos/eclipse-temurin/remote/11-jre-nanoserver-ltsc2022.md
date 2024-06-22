## `eclipse-temurin:11-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:19019141ea564b8b5bf76e003053f43737de5b13f11ed68b8312314b8c242dfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2529; amd64

### `eclipse-temurin:11-jre-nanoserver-ltsc2022` - windows version 10.0.20348.2529; amd64

```console
$ docker pull eclipse-temurin@sha256:0a764b3d9b1d15822562ea618a522af0a9cee412bad5db5bcf99d0d0fac6a990
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (164030421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05c0ddb9c3ff6aafbba74481bd713163ffedb7fdb594b7e50d30a4892e1bc549`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 19 Jun 2024 19:27:30 GMT
RUN Apply image 10.0.20348.2529
# Sat, 22 Jun 2024 00:50:29 GMT
SHELL [cmd /s /c]
# Sat, 22 Jun 2024 00:51:43 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Sat, 22 Jun 2024 00:51:43 GMT
ENV JAVA_HOME=C:\openjdk-11
# Sat, 22 Jun 2024 00:51:44 GMT
USER ContainerAdministrator
# Sat, 22 Jun 2024 00:51:55 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 22 Jun 2024 00:51:56 GMT
USER ContainerUser
# Sat, 22 Jun 2024 00:52:44 GMT
COPY dir:b092036da9619d86aad01e40fe92454a038bf12563d3a63208d5f3f51004688a in C:\openjdk-11 
# Sat, 22 Jun 2024 00:52:56 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:a8c295c425a912de308ded279124ae45fec44d55a451843fe5877155417f453c`  
		Last Modified: Fri, 21 Jun 2024 02:24:34 GMT  
		Size: 120.5 MB (120499549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8c04e6fe7f33e5ed7b73641c362d031eb0404b55967c9af2b8fa6f2269d9f92`  
		Last Modified: Sat, 22 Jun 2024 01:06:26 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d16af20197b9d8bbced9115bf2165d4f33b21fbc4db6e804091898a1257f50d`  
		Last Modified: Sat, 22 Jun 2024 01:07:14 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e5bb2acc79bb7db5b22838eac7b0413ae9f7fe202c8eccb3dba05471674514`  
		Last Modified: Sat, 22 Jun 2024 01:07:15 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb5b0777099d49667c4f974ec034d24c9b979e42a53262b448331a7aa82dadc`  
		Last Modified: Sat, 22 Jun 2024 01:07:14 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d2d9660d3ac4c0459737d76c86cc346bcf0cbade5fc466f694f4e5371d070b1`  
		Last Modified: Sat, 22 Jun 2024 01:07:12 GMT  
		Size: 79.4 KB (79441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d4dc52f85c49b3b28579e356773af9aa0f201792792d5c30c22f0c1236fb1d9`  
		Last Modified: Sat, 22 Jun 2024 01:07:12 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d405756aa24c0d0aa96836671c8a50dfdda97cc84b9cc1ce0dd182baccf632bf`  
		Last Modified: Sat, 22 Jun 2024 01:07:48 GMT  
		Size: 43.4 MB (43384458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ad724ea76acf719ee9b0d658cab888c133f66ef523729a73b02d1cb06869d3f`  
		Last Modified: Sat, 22 Jun 2024 01:07:40 GMT  
		Size: 61.2 KB (61191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
