## `eclipse-temurin:25-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:9e225c06cade5ea8ff2ac2af9179110fcd4e489ecc2b8b4a435265a9087498c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6905; amd64

### `eclipse-temurin:25-nanoserver-ltsc2025` - windows version 10.0.26100.6905; amd64

```console
$ docker pull eclipse-temurin@sha256:8c56a064f7eef16f56b6aa94382c1ae0a529bcd5967e71b8fe1803624eaf8c1f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.1 MB (332145591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef3eb7a33ed41b5eef5793632797de4f4dc96759f006901cceb3ee2ce5f0d2fa`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 22 Oct 2025 07:22:01 GMT
RUN Apply image 10.0.26100.6905
# Fri, 24 Oct 2025 19:21:58 GMT
SHELL [cmd /s /c]
# Fri, 24 Oct 2025 19:21:59 GMT
ENV JAVA_VERSION=jdk-25+36
# Fri, 24 Oct 2025 19:21:59 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 24 Oct 2025 19:22:00 GMT
USER ContainerAdministrator
# Fri, 24 Oct 2025 19:22:05 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 24 Oct 2025 19:22:06 GMT
USER ContainerUser
# Fri, 24 Oct 2025 19:22:15 GMT
COPY dir:3b404a1cbcdf7278c6a85a2778d3f0c01bd0f1229e8c8ae0734ae7bd6fe589bb in C:\openjdk-25 
# Fri, 24 Oct 2025 19:22:20 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 24 Oct 2025 19:22:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9188956580c47f583c927f17e42f8825823890544237141f21ca4ef10ea55e60`  
		Last Modified: Fri, 24 Oct 2025 11:13:56 GMT  
		Size: 194.0 MB (194029378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c08b98af0a30a946339f7aeeeef8689a00af4aaae2ab0e1ef7795394ea48ef09`  
		Last Modified: Fri, 24 Oct 2025 19:23:21 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47080127c9d726738750eb4782d006310ac0283f48b118af6663ba3eb1cc5d03`  
		Last Modified: Fri, 24 Oct 2025 19:23:21 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c01db60328ff97c480a15156b4d4f0415f339887a455f796d13a966587d4a0e5`  
		Last Modified: Fri, 24 Oct 2025 19:23:21 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f13d1197ba75c12f2105e23bc7225bb2b71e0af70baf53c65874772c2daf09a0`  
		Last Modified: Fri, 24 Oct 2025 19:23:21 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89466dae87d415ce32a7c94507ebcac80a59a702c9a5f8e50e6cb060cabd4e7e`  
		Last Modified: Fri, 24 Oct 2025 19:23:21 GMT  
		Size: 70.6 KB (70589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1d898ed6e51f85339e1dfe74f727162ad96a6a8ed7a7f2199229d6ae71f5aa`  
		Last Modified: Fri, 24 Oct 2025 19:23:22 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf2a808ab1cc324248df807fd827e5526909419faa75a225b931065da0ac76c`  
		Last Modified: Fri, 24 Oct 2025 21:18:28 GMT  
		Size: 137.9 MB (137936322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:676be0d378d433132e60aa264b245daefbfb18d817b406cde3bc268b2d699c08`  
		Last Modified: Fri, 24 Oct 2025 19:23:22 GMT  
		Size: 102.9 KB (102908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6cb7ad93d084918c05f44358ea58afb60f232b1b39ce390ee6dbbce9a8bcf5`  
		Last Modified: Fri, 24 Oct 2025 19:23:22 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
