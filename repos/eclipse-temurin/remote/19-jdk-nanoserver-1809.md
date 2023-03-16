## `eclipse-temurin:19-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:653c26019eca15b4b171e894a0123892fea5e927a2a98e19556831db8bcf8905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4131; amd64

### `eclipse-temurin:19-jdk-nanoserver-1809` - windows version 10.0.17763.4131; amd64

```console
$ docker pull eclipse-temurin@sha256:6a02398702faf6af5cd722b5095fc8cf3aad600be766694979646b296bce299f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.7 MB (303742684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:744a1d086ca19f0d1baad4001a498304074c5ab98923e84af92229084e8ebbb2`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 11 Mar 2023 10:09:02 GMT
RUN Apply image 10.0.17763.4131
# Thu, 16 Mar 2023 00:45:50 GMT
SHELL [cmd /s /c]
# Thu, 16 Mar 2023 01:23:09 GMT
ENV JAVA_VERSION=jdk-19.0.2+7
# Thu, 16 Mar 2023 01:23:10 GMT
ENV JAVA_HOME=C:\openjdk-19
# Thu, 16 Mar 2023 01:23:11 GMT
USER ContainerAdministrator
# Thu, 16 Mar 2023 01:23:22 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 16 Mar 2023 01:23:23 GMT
USER ContainerUser
# Thu, 16 Mar 2023 01:23:39 GMT
COPY dir:09b3ada3bc8ac44822b97a9a56d697461744d2194cdcb6ab15233b0b9b376e38 in C:\openjdk-19 
# Thu, 16 Mar 2023 01:24:03 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 16 Mar 2023 01:24:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:95eb2f0f3287f5ec687287cc244924aafc74c7ada3121d43f54223487f3f2d8d`  
		Last Modified: Thu, 16 Mar 2023 01:43:14 GMT  
		Size: 106.7 MB (106684240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b5837fe68a36caddf38b0aaa99f4ef20ca36d8dfe2825fa6ffbcf0d38b9d59a`  
		Last Modified: Thu, 16 Mar 2023 01:42:43 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff0203cee4455804fb9efd8e5ab10476e33070a8381b133321b6040a7165dc13`  
		Last Modified: Thu, 16 Mar 2023 01:52:14 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b597da8738d9af3f7b678cb69221dd791517cffd43be0c5b8827d58396fc8f`  
		Last Modified: Thu, 16 Mar 2023 01:52:14 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b13b51bc5f7e086a7933dc25e93e541c6c5567835954dccda0b9acfa548c93`  
		Last Modified: Thu, 16 Mar 2023 01:52:14 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f93025d0762ff8183a41d12c546f8e1e228d843cd806b8517d9cb7a69d6416`  
		Last Modified: Thu, 16 Mar 2023 01:52:12 GMT  
		Size: 69.0 KB (69016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e445ed55caa35f1d5ff0e86202f3d3e09a051af742b5da6b3fefcd35016367`  
		Last Modified: Thu, 16 Mar 2023 01:52:12 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a6ff9c8dc682113b7153df0453a70bc5630bf741e13159ae12656cf1b777bc`  
		Last Modified: Thu, 16 Mar 2023 01:52:35 GMT  
		Size: 193.3 MB (193263057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a97ae539f1eb1900c5037b4de4dec702fae38e598cec5d621f08efc0634e23d`  
		Last Modified: Thu, 16 Mar 2023 01:52:13 GMT  
		Size: 3.7 MB (3719393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:904469d8a93946c4060bc6eedc746ec185223a9d9c44392c1c7b0d1ca8483cb4`  
		Last Modified: Thu, 16 Mar 2023 01:52:12 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
