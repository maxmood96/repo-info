## `eclipse-temurin:11-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:101c55036b00084d089ba77938f30a1c91133da3e200ed2d27bab6414121693e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2113; amd64

### `eclipse-temurin:11-nanoserver-ltsc2022` - windows version 10.0.20348.2113; amd64

```console
$ docker pull eclipse-temurin@sha256:543f3f18cb367a4977a6d882f6353c3361383e2a09729dd62d041abbabdd4713
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.9 MB (314868974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce109db4c357923aecaa9514c3d87f7059ca45bf6b0482dbb51b1251b6b0fd9c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Nov 2023 06:09:19 GMT
RUN Apply image 10.0.20348.2113
# Thu, 16 Nov 2023 02:17:18 GMT
SHELL [cmd /s /c]
# Thu, 16 Nov 2023 02:18:40 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Thu, 16 Nov 2023 02:18:40 GMT
ENV JAVA_HOME=C:\openjdk-11
# Thu, 16 Nov 2023 02:18:41 GMT
USER ContainerAdministrator
# Thu, 16 Nov 2023 02:18:51 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 16 Nov 2023 02:18:51 GMT
USER ContainerUser
# Thu, 16 Nov 2023 02:19:06 GMT
COPY dir:3378004dd1c559f9d7d6f4bacd149386aa6ab741f7dba391fbd8a10b1a80b205 in C:\openjdk-11 
# Thu, 16 Nov 2023 02:19:19 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 16 Nov 2023 02:19:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1ca4fbe907f22e883670decfa8d7f4490a79a995bb83a6c286248c21d61a62f5`  
		Last Modified: Tue, 14 Nov 2023 21:13:36 GMT  
		Size: 120.8 MB (120753560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a2f0edb58e1876347bbad88c907697db94e172aa6ff4a38560ccfb68d72aa86`  
		Last Modified: Thu, 16 Nov 2023 02:37:47 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b17da8727ce4c05eb0ac5d2556f4bae44bcfc7182f8b68aa18e0ce3f5d5f4c7a`  
		Last Modified: Thu, 16 Nov 2023 02:38:38 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619db30282dc4b71d71d51df46474e984e03c281012879e44b94c28db05a117f`  
		Last Modified: Thu, 16 Nov 2023 02:38:38 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d91d895e42f8926868d20203dd027e55b41e756b6f0e59c38f9707dc3eeb8d2a`  
		Last Modified: Thu, 16 Nov 2023 02:38:38 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e21aaa12f70b8a0296eec04bcf23166115d3ac45cd2966bb5ab2ed8b22b16e7`  
		Last Modified: Thu, 16 Nov 2023 02:38:37 GMT  
		Size: 78.1 KB (78051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b15e9cdc6258c0594edb12985429e990517aebff173af95a0a6d130c4cb4ab`  
		Last Modified: Thu, 16 Nov 2023 02:38:36 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5e8ee9d3f1994d9905eb83bb559b4e35c3a5c3e33fc693028deaec15d7bcd7`  
		Last Modified: Thu, 16 Nov 2023 02:38:55 GMT  
		Size: 194.0 MB (193969649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa898f4a0239d1366e889b05677eb481fafb17eebf3749a60ac0c02372453076`  
		Last Modified: Thu, 16 Nov 2023 02:38:36 GMT  
		Size: 61.0 KB (60971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86eecdd577dd0f9db25f4b45a85c66915637b3c05c70bcb9a2b56223765f389b`  
		Last Modified: Thu, 16 Nov 2023 02:38:36 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
