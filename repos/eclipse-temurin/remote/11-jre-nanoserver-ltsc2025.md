## `eclipse-temurin:11-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:62b1424bfeae0964312a063db4e0ddad288e9008e65f55b3fb9e7cf2c2218451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4349; amd64

### `eclipse-temurin:11-jre-nanoserver-ltsc2025` - windows version 10.0.26100.4349; amd64

```console
$ docker pull eclipse-temurin@sha256:3e2898ab54a556d5c42a843c06a54dcee360cc6d6f75da968239babfc3745863
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235919349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:584f58c8eaaacc05b677206b26889e89b112542d8d3e4b19ea2831a1172c1890`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 07 Jun 2025 15:19:59 GMT
RUN Apply image 10.0.26100.4349
# Tue, 10 Jun 2025 22:15:07 GMT
SHELL [cmd /s /c]
# Tue, 10 Jun 2025 22:15:08 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Tue, 10 Jun 2025 22:15:10 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 10 Jun 2025 22:15:11 GMT
USER ContainerAdministrator
# Tue, 10 Jun 2025 22:15:15 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Jun 2025 22:15:16 GMT
USER ContainerUser
# Tue, 10 Jun 2025 22:15:21 GMT
COPY dir:d6f4a8ae4843d3009794ef7988392b65ed4dd8f1da131593f0c13b36f9fcbd8a in C:\openjdk-11 
# Tue, 10 Jun 2025 22:15:27 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:709fa8bff22087ae5c45c65a3b0777eb6ee12afd1b773aece2a322e84b66b1d1`  
		Last Modified: Tue, 10 Jun 2025 22:41:49 GMT  
		Size: 192.1 MB (192082516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29a73d776eb14b1f89363be06031d02cbba3e25d23fae01547150f4598c67fc`  
		Last Modified: Tue, 10 Jun 2025 22:16:05 GMT  
		Size: 1.1 KB (1090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc422772ffa7f1c2edf38b0b51c5bce1eace918e322998a9ba9697405108b2a`  
		Last Modified: Tue, 10 Jun 2025 22:16:05 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ade207c4bd8603cc683c4e96c45d2282f18bd8b39746e35c6a9034991e1595`  
		Last Modified: Tue, 10 Jun 2025 22:16:05 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3426ee194964cf761b4f4c7eb557a4ee88403619d927d8e68282f924fba07df0`  
		Last Modified: Tue, 10 Jun 2025 22:16:05 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa117fbb014ae0d2c3c2e1c41e8df2b5f7dc7f876410f19ab7b5051c67f62a9`  
		Last Modified: Tue, 10 Jun 2025 22:16:06 GMT  
		Size: 75.7 KB (75704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56944523db82eec3c28a7c3e290796151c76694d3155a9210869e5defd361ef3`  
		Last Modified: Tue, 10 Jun 2025 22:16:06 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dbd467dc1de45f8789b4cc255075dcdb91bbceabcdbfd4fa1d22429b1ab888a`  
		Last Modified: Tue, 10 Jun 2025 22:16:09 GMT  
		Size: 43.7 MB (43664061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae6e7f89aadcf5a9255a920c85866c93ead4361f91259918f9db8d9fa88dfcfb`  
		Last Modified: Tue, 10 Jun 2025 22:16:06 GMT  
		Size: 91.8 KB (91793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
