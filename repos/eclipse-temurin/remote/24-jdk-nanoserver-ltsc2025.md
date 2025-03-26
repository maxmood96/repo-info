## `eclipse-temurin:24-jdk-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:6a82c0aca3400385a3d4f19b27ae735d6d493ec9f3ccf9018c6ec308bebfac78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3476; amd64

### `eclipse-temurin:24-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.3476; amd64

```console
$ docker pull eclipse-temurin@sha256:2cc546a01568634258865472c3093211543e5984b8f8de389e95f2083651a600
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.9 MB (343854958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee8516850041c7cf18d83e256e8dd40fd16281e7f0f7aea5d8626922141f921`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Mar 2025 05:48:38 GMT
RUN Apply image 10.0.26100.3476
# Tue, 25 Mar 2025 23:13:59 GMT
SHELL [cmd /s /c]
# Tue, 25 Mar 2025 23:14:00 GMT
ENV JAVA_VERSION=jdk-24+36
# Tue, 25 Mar 2025 23:14:01 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 25 Mar 2025 23:14:02 GMT
USER ContainerAdministrator
# Tue, 25 Mar 2025 23:14:06 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 25 Mar 2025 23:14:06 GMT
USER ContainerUser
# Tue, 25 Mar 2025 23:14:12 GMT
COPY dir:82098476e422c0fd1b27846be91131b5a5073542830e51603132b80cd94d4318 in C:\openjdk-24 
# Tue, 25 Mar 2025 23:14:19 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 25 Mar 2025 23:14:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6008a43ec9274f69b461027b7f4e2fe6a71387d40072c0b5b4f0dbbfa688d8a5`  
		Last Modified: Wed, 12 Mar 2025 18:43:31 GMT  
		Size: 206.3 MB (206302205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7b1fedd6698f1f20a6608acb47dc182f711cb913f4fa97718460c2c46738d8`  
		Last Modified: Tue, 25 Mar 2025 23:14:24 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce0489ccbe558c5f3a0cb17b2e47a02a71dd86b1372ab2fbb5ea6af0b27b7c1`  
		Last Modified: Tue, 25 Mar 2025 23:14:23 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07511559a9995e3d89cf8715e5a0d10eb18fc35e833168972f8d3c424328b0d7`  
		Last Modified: Tue, 25 Mar 2025 23:14:23 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3667b2a53ebab2ec31332adb36ebb115e98e90375574913f80e3f590371b6b45`  
		Last Modified: Tue, 25 Mar 2025 23:14:23 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d3ecc9f9760d47fd777494c378400310c97e8f02f2443fddbd7a270d24d3d8`  
		Last Modified: Tue, 25 Mar 2025 23:14:22 GMT  
		Size: 76.2 KB (76232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7872219819c5e7476c6abeaef594ab9d85e173c9da3529ac3c60cf562835a0e0`  
		Last Modified: Tue, 25 Mar 2025 23:14:22 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258af92ef0e237696730e12e45fdbc5e25a5351ac43c19200700d1db20606f05`  
		Last Modified: Tue, 25 Mar 2025 23:14:33 GMT  
		Size: 137.4 MB (137356006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c5cc79157ebac48ed3647f6513fce4587c9300d79b652c759e8d5e2a02d8b3`  
		Last Modified: Tue, 25 Mar 2025 23:14:22 GMT  
		Size: 114.3 KB (114267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:003e2bb26cbfe39024337cff9710ca2ec186595b8e76b51c0f089dc367d98a8f`  
		Last Modified: Tue, 25 Mar 2025 23:14:22 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
