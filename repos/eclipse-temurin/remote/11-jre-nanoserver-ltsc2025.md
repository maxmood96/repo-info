## `eclipse-temurin:11-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:c08f57331f59b10d71c549e4a360c72508c14011f1bfa8ffd76d6efef179549d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3775; amd64

### `eclipse-temurin:11-jre-nanoserver-ltsc2025` - windows version 10.0.26100.3775; amd64

```console
$ docker pull eclipse-temurin@sha256:a9226ae5afea9c54c36aee62bf7d5b74b59cccb49142f4446b74639f08ea2af5
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.0 MB (233955519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d6845a0156d1bc3a4ed59ffa14e85c757f033f8a84e1c7e67edefed608e9d91`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 06 Apr 2025 07:26:08 GMT
RUN Apply image 10.0.26100.3775
# Wed, 09 Apr 2025 01:17:33 GMT
SHELL [cmd /s /c]
# Wed, 09 Apr 2025 01:17:34 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Wed, 09 Apr 2025 01:17:35 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 09 Apr 2025 01:17:36 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 01:17:39 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Apr 2025 01:17:40 GMT
USER ContainerUser
# Wed, 09 Apr 2025 01:17:44 GMT
COPY dir:e7319a06d2b9171c954fc18de0614fa7d0eb408950b795be61492806db04a6ea in C:\openjdk-11 
# Wed, 09 Apr 2025 01:17:48 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:79b2ed45f890e91d23d7d22491a8fb6909c9268c668dc6a0e3b40131da02ed74`  
		Last Modified: Wed, 09 Apr 2025 00:36:30 GMT  
		Size: 190.1 MB (190113206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f35326682400ca198f0714baa663029235da99784314e6e39e2cb0187f6b7a`  
		Last Modified: Wed, 09 Apr 2025 01:17:52 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b794edcdd112bad11544e07c17753e1a2e927537de6b9ee25138ea7956f016de`  
		Last Modified: Wed, 09 Apr 2025 01:17:53 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f627ddab4df96ed184a919cb7fbb7c0076e62edc7ba8bf6a5a88e98131ab63f`  
		Last Modified: Wed, 09 Apr 2025 01:17:52 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06a2f156ad6a1de9dd571d77b7e1e192d53d1dd579a986d49b177d006e8054e5`  
		Last Modified: Wed, 09 Apr 2025 01:17:51 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39252553e0b52f574874ec549e7a030986c937e6b97ce8b5de6e1d40f2d64ec8`  
		Last Modified: Wed, 09 Apr 2025 01:17:51 GMT  
		Size: 75.9 KB (75915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48dd237c00d3cffe9072fca48094853c6793f6c75775a652409b8a19a46cc1c9`  
		Last Modified: Wed, 09 Apr 2025 01:17:51 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9427bac43e96a132321d5d56a3452f168fef8d450b6f56f4269415cfc6d733f7`  
		Last Modified: Wed, 09 Apr 2025 01:17:56 GMT  
		Size: 43.7 MB (43656841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5896538a01bb278000d7a5af1517b2a77df24a3534f9d7d398bab64242dc9c17`  
		Last Modified: Wed, 09 Apr 2025 01:17:51 GMT  
		Size: 104.3 KB (104305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
