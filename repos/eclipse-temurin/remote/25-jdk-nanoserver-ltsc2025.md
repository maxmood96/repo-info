## `eclipse-temurin:25-jdk-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:fe056447464f8e5c229fecdd02ba2bdd869c4d0192da93011d3e4e4fd2958a8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32860; amd64

### `eclipse-temurin:25-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.32860; amd64

```console
$ docker pull eclipse-temurin@sha256:00185c664f24a51df9428311637521d8ad062e7860edd57272b21cdd19cb3cdd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.9 MB (337948244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04a5624a1a1cd88a9c213aa6e5352967fdbd5b94f5904d019585c52c72698a10`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 10 May 2026 09:46:02 GMT
RUN Apply image 10.0.26100.32860
# Wed, 13 May 2026 00:29:14 GMT
SHELL [cmd /s /c]
# Wed, 13 May 2026 00:29:14 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Wed, 13 May 2026 00:29:14 GMT
ENV JAVA_HOME=C:\openjdk-25
# Wed, 13 May 2026 00:29:14 GMT
USER ContainerAdministrator
# Wed, 13 May 2026 00:29:16 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 May 2026 00:29:16 GMT
USER ContainerUser
# Wed, 13 May 2026 00:29:24 GMT
COPY dir:93c9a33f6e3b7bf9a4cc6584352427179a8f4d1e9396155b43179dd1c4270396 in C:\openjdk-25 
# Wed, 13 May 2026 00:29:28 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 13 May 2026 00:29:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:34ab6476d71f2d23d05a00ac439000ba4c19d17e5c66f15efbe329ed79bba2bf`  
		Last Modified: Tue, 12 May 2026 22:29:47 GMT  
		Size: 199.7 MB (199739001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353f839ae1b6bca354af0c348feb64f0df227628c75588ea69316206842af558`  
		Last Modified: Wed, 13 May 2026 00:29:35 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89c098f7b89a27e6df27130a9bd72c22fd633e96ad9169f5f7d4531d9625a30`  
		Last Modified: Wed, 13 May 2026 00:29:34 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9486b6fb6a0bde0513253100276abdb342050dc3501172170b4f7549b45e5c3d`  
		Last Modified: Wed, 13 May 2026 00:29:34 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1810ab78031910f468ee9575439f6f1dfb694b3de5589e99e5af655c1f3155`  
		Last Modified: Wed, 13 May 2026 00:29:34 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7ff9e638730eb45cf6d695efc76054e52d7f5c940f22337202d58efbc28e544`  
		Last Modified: Wed, 13 May 2026 00:29:32 GMT  
		Size: 72.1 KB (72102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87032a46c77f631dddd9398fac92c0d0da6f40a26cf55dc72f9b5fe22b194330`  
		Last Modified: Wed, 13 May 2026 00:29:32 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44ff2cd8e023557cb502f13137a79918288206369a3a94054913dfc19ec33bad`  
		Last Modified: Wed, 13 May 2026 00:29:44 GMT  
		Size: 138.0 MB (138009432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955225bdce2a4febc995fc58c73abc3e346c9f1eb53f309a6916d13c10d067a6`  
		Last Modified: Wed, 13 May 2026 00:29:32 GMT  
		Size: 121.3 KB (121269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:378612450f50ae2abc777cadd7a01019c23a0830023b034fdc5024224c59dbee`  
		Last Modified: Wed, 13 May 2026 00:29:32 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
