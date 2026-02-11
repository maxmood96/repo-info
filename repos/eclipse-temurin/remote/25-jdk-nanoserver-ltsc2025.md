## `eclipse-temurin:25-jdk-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:5ece911fe39c9140ce139a33491d7f258c1aaabf5f4f06f08393b72dbab04a60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32370; amd64

### `eclipse-temurin:25-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.32370; amd64

```console
$ docker pull eclipse-temurin@sha256:5d4ef4bb5917fca13bff1bec654c4c9fb0e9e4f533f4428b3518f5c028260d2a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.4 MB (337366977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:426bfd5a68fff05564a801a325e55157ddf329ea7a61ad82153f3286aee12a8c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Feb 2026 22:06:41 GMT
RUN Apply image 10.0.26100.32370
# Tue, 10 Feb 2026 23:37:42 GMT
SHELL [cmd /s /c]
# Tue, 10 Feb 2026 23:37:43 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Tue, 10 Feb 2026 23:37:43 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 10 Feb 2026 23:37:44 GMT
USER ContainerAdministrator
# Tue, 10 Feb 2026 23:37:50 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Feb 2026 23:37:50 GMT
USER ContainerUser
# Tue, 10 Feb 2026 23:38:00 GMT
COPY dir:ebca1fed269853ebca056470dac79e7ebf8f2b759d9752408e0c7f2313fb3842 in C:\openjdk-25 
# Tue, 10 Feb 2026 23:38:05 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 10 Feb 2026 23:38:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:77321bd03612cfa46920e790ae0c3b142758a5803ad759fdb406c98b6f2e4ed0`  
		Last Modified: Tue, 10 Feb 2026 22:50:26 GMT  
		Size: 199.3 MB (199251619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e531c529947e5012f634456b5c0dca050a4967e04d240ba9b77245c68246c195`  
		Last Modified: Tue, 10 Feb 2026 23:38:11 GMT  
		Size: 1.1 KB (1117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a691b36c2154a0ee02fb0b17ed9513d1944cf48f62fa1d3f229f475bd086b75`  
		Last Modified: Tue, 10 Feb 2026 23:38:11 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f93a275391cbcc5395573ae0861f42c5fddd92d73be99658923afb2301542e`  
		Last Modified: Tue, 10 Feb 2026 23:38:11 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e14beb39a8e0283d51dc0521c92ea67d4beedf6abde9decd11b19682aebf6c`  
		Last Modified: Tue, 10 Feb 2026 23:38:11 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c4f31a40df263657134136fcb2a614f7cce50fa7660f61e2893fc98ad398e6`  
		Last Modified: Tue, 10 Feb 2026 23:38:10 GMT  
		Size: 73.1 KB (73129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749e05b1df6c818aafb47d4abb3271cf8df3a8064e1489a55f99f445cb221bcd`  
		Last Modified: Tue, 10 Feb 2026 23:38:09 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9b5683170c07fb1cf2495be2c4d0631d2a94aa7b6bd2d231878304cb4ad0da`  
		Last Modified: Tue, 10 Feb 2026 23:38:22 GMT  
		Size: 137.9 MB (137932500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0becb4568846d3e4783e9d3ef54e34429e891415a65495af9ef7235b43b330f2`  
		Last Modified: Tue, 10 Feb 2026 23:38:10 GMT  
		Size: 103.3 KB (103252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee4d6844746b1881357fb3be49af030a9931acca4aa99f8d7d6b72548e552c1`  
		Last Modified: Tue, 10 Feb 2026 23:38:10 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
