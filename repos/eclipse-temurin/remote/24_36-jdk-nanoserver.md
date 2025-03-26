## `eclipse-temurin:24_36-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:b5989070238d68a5490141ad39b3826fa82b65fe523f29cc3aed3b84a7543ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `eclipse-temurin:24_36-jdk-nanoserver` - windows version 10.0.26100.3476; amd64

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

### `eclipse-temurin:24_36-jdk-nanoserver` - windows version 10.0.20348.3328; amd64

```console
$ docker pull eclipse-temurin@sha256:2cbe404936e80155ecaf3135b01939efc696094863fb080be573a51e6a275d4b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.2 MB (258240422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0239db6d1a7f0faf196fa548bbe5ed346063dadc6fa1bc463c22a7e640d19ac2`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 06 Mar 2025 10:30:39 GMT
RUN Apply image 10.0.20348.3328
# Tue, 25 Mar 2025 23:26:04 GMT
SHELL [cmd /s /c]
# Tue, 25 Mar 2025 23:26:05 GMT
ENV JAVA_VERSION=jdk-24+36
# Tue, 25 Mar 2025 23:26:06 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 25 Mar 2025 23:26:06 GMT
USER ContainerAdministrator
# Tue, 25 Mar 2025 23:26:08 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 25 Mar 2025 23:26:09 GMT
USER ContainerUser
# Tue, 25 Mar 2025 23:26:17 GMT
COPY dir:82098476e422c0fd1b27846be91131b5a5073542830e51603132b80cd94d4318 in C:\openjdk-24 
# Tue, 25 Mar 2025 23:26:22 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 25 Mar 2025 23:26:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:47ec0d45ee7716f773dfebb62d84eb3893d3af9baf9c799960566b016a17e330`  
		Last Modified: Wed, 12 Mar 2025 02:22:56 GMT  
		Size: 120.7 MB (120695547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e6ffb79d9315b5241076ade3856244a705c31f5a7c9c10b6149df1a4900dc8`  
		Last Modified: Tue, 25 Mar 2025 23:26:27 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbfa1056b3ee7b5cd69c2fd29bd1dccefdec46ed40b06dfbbfc7b68674db4f5d`  
		Last Modified: Tue, 25 Mar 2025 23:26:26 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50cc68a6758888000a724dc3285d7b8608e683e1c8851881246e3ab0840ab094`  
		Last Modified: Tue, 25 Mar 2025 23:26:26 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d7f122edb834b8b41030c868a6b1141cd281d07713b99c03c152da51b256c82`  
		Last Modified: Tue, 25 Mar 2025 23:26:26 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9ca459ed970ac5a9099526af76c8dded05e1c73288d3d6bb9becfb42870c91`  
		Last Modified: Tue, 25 Mar 2025 23:26:25 GMT  
		Size: 76.2 KB (76216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38faf301c0b506ab9d65210d6ccd31b711383a07f30f4350e6066ed2c3711b35`  
		Last Modified: Tue, 25 Mar 2025 23:26:25 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f33d8c8e01c272b34b89f56a48461754b6f24604457fb0c37fcf3f6e0c49f9`  
		Last Modified: Tue, 25 Mar 2025 23:26:37 GMT  
		Size: 137.4 MB (137355283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30debebfd983b79e2baddc283eaa90bf33a4eda5ae3e3ca28223045a2d4d7d1e`  
		Last Modified: Tue, 25 Mar 2025 23:26:25 GMT  
		Size: 107.2 KB (107174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d1ef7b604437a77cabba7e9d072260146eba0b4a4acb4ecb3533cd7c5d1903`  
		Last Modified: Tue, 25 Mar 2025 23:26:25 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:24_36-jdk-nanoserver` - windows version 10.0.17763.7009; amd64

```console
$ docker pull eclipse-temurin@sha256:a0553dbe1c4406e7c4b677c1f915fddee600fbf45d9992129a0b4ccb73f62fda
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.7 MB (248740091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c2c8d17ce2a1307d0c67396ed39a2426b2290146e8afad638e402877e0b623`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Tue, 25 Mar 2025 23:14:57 GMT
SHELL [cmd /s /c]
# Tue, 25 Mar 2025 23:15:00 GMT
ENV JAVA_VERSION=jdk-24+36
# Tue, 25 Mar 2025 23:15:00 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 25 Mar 2025 23:15:01 GMT
USER ContainerAdministrator
# Tue, 25 Mar 2025 23:15:03 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 25 Mar 2025 23:15:04 GMT
USER ContainerUser
# Tue, 25 Mar 2025 23:15:11 GMT
COPY dir:82098476e422c0fd1b27846be91131b5a5073542830e51603132b80cd94d4318 in C:\openjdk-24 
# Tue, 25 Mar 2025 23:15:17 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 25 Mar 2025 23:15:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d870e42e7f6c7d99a4db68ec41feb180a4f0eb340ba043353d93752fc4aa5f3`  
		Last Modified: Tue, 25 Mar 2025 23:15:23 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1863918c094b9495e054f76ec871fb75161dedaae8fc03ffed0f6e414952833a`  
		Last Modified: Tue, 25 Mar 2025 23:15:22 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e89ee47c80546632a1b01a7ad5a332f48d1645836837b9200fea8e4e9fb944`  
		Last Modified: Tue, 25 Mar 2025 23:15:22 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc4a27e48af860be19436024decfab0152b011ef1ebc390e11d8d11ced061a3`  
		Last Modified: Tue, 25 Mar 2025 23:15:22 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb6875e454342557657bbb77921bb05e0af7d038946343eb435260340035648`  
		Last Modified: Tue, 25 Mar 2025 23:15:21 GMT  
		Size: 69.8 KB (69753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e3a49255455a5ebeafcdf8db812a0e1e71f834773641c89c0f2c41ccd47c46f`  
		Last Modified: Tue, 25 Mar 2025 23:15:21 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb71b271686991f336591f6e191f7665b6ced81a998f829cce05005940af9ca`  
		Last Modified: Tue, 25 Mar 2025 23:15:32 GMT  
		Size: 137.4 MB (137354928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13a0676d6fdbef7bdedf6cd62b48d6b84a9bbc20d1caa2aa864740e5fcacebf`  
		Last Modified: Tue, 25 Mar 2025 23:15:21 GMT  
		Size: 4.4 MB (4401317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4865b5f4e44b21eaebd875f1faeeeb14ca7dfbee5d9687c5c86064e98844d597`  
		Last Modified: Tue, 25 Mar 2025 23:15:21 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
