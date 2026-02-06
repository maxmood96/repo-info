## `eclipse-temurin:8u482-b08-jdk-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:adacc9215b133c54ec958419516b79aca68c4ac374a5f61d429ba266e97454e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `eclipse-temurin:8u482-b08-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull eclipse-temurin@sha256:915ccc7e66c596ef1713cce163419fd1ba86ca37b7df029ea6029bcf860bfc56
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.2 MB (301164570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:376743a6a0c0ac3a52d5bc24b3236457050f8a4bac36b8358516e024bb65964a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 11 Jan 2026 06:15:10 GMT
RUN Apply image 10.0.26100.32230
# Thu, 05 Feb 2026 22:39:23 GMT
SHELL [cmd /s /c]
# Thu, 05 Feb 2026 22:39:24 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Thu, 05 Feb 2026 22:39:25 GMT
ENV JAVA_HOME=C:\openjdk-8
# Thu, 05 Feb 2026 22:39:25 GMT
USER ContainerAdministrator
# Thu, 05 Feb 2026 22:39:33 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 05 Feb 2026 22:39:34 GMT
USER ContainerUser
# Thu, 05 Feb 2026 22:39:51 GMT
COPY dir:076949d8a0679d24528f11c4150b1ea7a552717f0bf1fb11a9fa610f7e5e2ea0 in C:\openjdk-8 
# Thu, 05 Feb 2026 22:39:56 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:d441ba4c6d25e3ab6a1e3ce5360fd1d1214e97975f1e40b10c0ccb55dc46ad22`  
		Last Modified: Tue, 13 Jan 2026 22:42:10 GMT  
		Size: 199.1 MB (199076547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f040bc3ccdaf5303b7ec7db8b9c37f0cd0fd43191b6b4b9689c2fb66cc3f91c`  
		Last Modified: Thu, 05 Feb 2026 22:40:01 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:397ed63aa48ab347bcfe2685cdccac40bf4c38b6965ffcae3a6e8de950ccb999`  
		Last Modified: Thu, 05 Feb 2026 22:40:01 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3750e33776daccbf84999efe63724cd78441c81cda03f98f6bdd9806e2fffa9f`  
		Last Modified: Thu, 05 Feb 2026 22:40:01 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7c5ead3b8d3d031f01fe7d40ebb1adc88e414f93968e0af4542b62eb216d07c`  
		Last Modified: Thu, 05 Feb 2026 22:40:00 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:312037b2a22363c82c1b42ad952787bbba4ade825f0c3e704290bdcb16f15af7`  
		Last Modified: Thu, 05 Feb 2026 22:40:00 GMT  
		Size: 71.0 KB (71018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bd1dadb458313195f8b1855e6069245a862a6ee4c5812ec06d1a5acbef11ac3`  
		Last Modified: Thu, 05 Feb 2026 22:40:00 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5a8cc05bf4d2fb3420ca757105eb84a2f744bf86f515a162cbf2e062b5fe3b`  
		Last Modified: Thu, 05 Feb 2026 22:40:07 GMT  
		Size: 101.9 MB (101908756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed46a300eb9da4bc9e0fd0faa4e98f4f20f4f9079d9e9c4ec516b48a8ca68755`  
		Last Modified: Thu, 05 Feb 2026 22:40:00 GMT  
		Size: 102.9 KB (102887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
