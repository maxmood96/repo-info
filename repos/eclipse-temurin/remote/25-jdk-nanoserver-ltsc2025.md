## `eclipse-temurin:25-jdk-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:0541b24ccca0220031c0e1ef6a46c94ac18d2f285aee6be06b7ba94eae1fa43f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32690; amd64

### `eclipse-temurin:25-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.32690; amd64

```console
$ docker pull eclipse-temurin@sha256:ae10c8f9c7ea9a8d3a2657fae6b67f008b4f9decd906890b5d38383718285b02
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.9 MB (337914928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:687fbbc66a6edd0d93ccfd71beb6cd259743e6a3f086482e83876585e847d09e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Apr 2026 06:39:57 GMT
RUN Apply image 10.0.26100.32690
# Fri, 01 May 2026 00:08:17 GMT
SHELL [cmd /s /c]
# Fri, 01 May 2026 00:08:17 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Fri, 01 May 2026 00:08:18 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 01 May 2026 00:08:20 GMT
USER ContainerAdministrator
# Fri, 01 May 2026 00:08:30 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 01 May 2026 00:08:30 GMT
USER ContainerUser
# Fri, 01 May 2026 00:09:01 GMT
COPY dir:93c9a33f6e3b7bf9a4cc6584352427179a8f4d1e9396155b43179dd1c4270396 in C:\openjdk-25 
# Fri, 01 May 2026 00:09:09 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 May 2026 00:09:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8af320c3b6d19296bcc7947e3beb8bc0c69cb12143db52efe988dc998ac088dc`  
		Last Modified: Tue, 14 Apr 2026 21:00:37 GMT  
		Size: 199.7 MB (199717094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f2eaa2e471458f8dbdb4928684021c4d03924c87d1f171b3719d4b554fb875`  
		Last Modified: Fri, 01 May 2026 00:09:15 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745abc4dcc729c2f164471bbce39eaf74e3ba19485554a271af34b321c233d51`  
		Last Modified: Fri, 01 May 2026 00:09:15 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4c4a06995ebd75ee21ed5f5b46c7452d0d428e6caa795f7145b474fbcfb26d`  
		Last Modified: Fri, 01 May 2026 00:09:15 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e3a7369ab79e37e13dc458824b5d8a5d33963a484472e8fe8f24bd34e4575a6`  
		Last Modified: Fri, 01 May 2026 00:09:15 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1a733bf9c13f86bcd3aa846f6ce8c9ff5106b5f65a30f79c9a2cee688df8b4`  
		Last Modified: Fri, 01 May 2026 00:09:13 GMT  
		Size: 69.6 KB (69633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccf188222791c8c1664f5f36e4456ae7295050af45049d36b7f7775b0a31d47`  
		Last Modified: Fri, 01 May 2026 00:09:13 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:830ff6f4681e7bcda62dc10982148361a3c6c858de2f2fb6fd9af956acaa1ab6`  
		Last Modified: Fri, 01 May 2026 00:09:25 GMT  
		Size: 138.0 MB (138009570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a089c54d186d7c0ba0857aac0d1deab2caeb02576abc02797412b70607b370f9`  
		Last Modified: Fri, 01 May 2026 00:09:13 GMT  
		Size: 112.2 KB (112244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deda98798c505f7a3300c338fab3bb83c07404307db498f29b37cdfa468bdd8d`  
		Last Modified: Fri, 01 May 2026 00:09:13 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
