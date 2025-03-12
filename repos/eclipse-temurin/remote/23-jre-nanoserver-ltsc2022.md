## `eclipse-temurin:23-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:651cd5a3853d861572c893b7433cd34f8b3bec1b88d43529854aa9c31e5d79eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `eclipse-temurin:23-jre-nanoserver-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull eclipse-temurin@sha256:3f479effee035581cd32fe3a82a4ac24b39dbfacdd4af7a4650889d35e547ac2
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.9 MB (169856755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd03b4b3d47becbabaeccc5d4229dbd1fad141a11ea0b2659a8dd6bdd83b4f7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 06 Mar 2025 10:30:39 GMT
RUN Apply image 10.0.20348.3328
# Wed, 12 Mar 2025 19:15:52 GMT
SHELL [cmd /s /c]
# Wed, 12 Mar 2025 19:15:53 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Wed, 12 Mar 2025 19:15:54 GMT
ENV JAVA_HOME=C:\openjdk-23
# Wed, 12 Mar 2025 19:15:55 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 19:15:57 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Mar 2025 19:15:58 GMT
USER ContainerUser
# Wed, 12 Mar 2025 19:16:02 GMT
COPY dir:f0b8f3d1970d52810d59047a7e1dfff98787b37140cc4aafc37fc86b09fa8be8 in C:\openjdk-23 
# Wed, 12 Mar 2025 19:16:06 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:47ec0d45ee7716f773dfebb62d84eb3893d3af9baf9c799960566b016a17e330`  
		Last Modified: Wed, 12 Mar 2025 02:22:56 GMT  
		Size: 120.7 MB (120695547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed0085dc1f17830cd30ae840d6a5b382dfef7ab215e460654e580050fb1fda9`  
		Last Modified: Wed, 12 Mar 2025 19:16:12 GMT  
		Size: 1.1 KB (1092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720e98375b87ff708814765c95ed367b6ac0ffb17a99a94b7ba73d680421321e`  
		Last Modified: Wed, 12 Mar 2025 19:16:11 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32f6cfba4b7c429c8de7829e6278ab5cad25305ffeac32571caaf0fe92e606b7`  
		Last Modified: Wed, 12 Mar 2025 19:16:11 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac55dd69870dba411ad4e8757cb5de78447c5236d50935fbd56dca0a0fc77fe3`  
		Last Modified: Wed, 12 Mar 2025 19:16:10 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a77428959dee898a490d7b5f8ce6c77f4b1d308ff8870b89d7c9932e79b7aef`  
		Last Modified: Wed, 12 Mar 2025 19:16:10 GMT  
		Size: 77.9 KB (77942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c1949a6d9bc00e84e34af5b995f6c76dd00994b34998aad8ca186ab27e0d8c6`  
		Last Modified: Wed, 12 Mar 2025 19:16:10 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63826d11b8e363d2b582343751acbb43b1ca6dc205794375448351984bc0c939`  
		Last Modified: Wed, 12 Mar 2025 19:16:15 GMT  
		Size: 49.0 MB (48979935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b254f4fcc66fb74265693a92ebf655fd7790506ad6f97f4cb8e9565838bf62`  
		Last Modified: Wed, 12 Mar 2025 19:16:10 GMT  
		Size: 97.9 KB (97936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
