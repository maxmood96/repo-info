## `eclipse-temurin:11-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:b0313c7924a35e8505f5c941a3f5a7f8a13f6e256634e8d13184ad899fe315f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.469; amd64
	-	windows version 10.0.17763.2451; amd64

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.20348.469; amd64

```console
$ docker pull eclipse-temurin@sha256:892f5b3cb2590ca8ce675196a1403725b02ee70a4785d7930a30ff563ca5a86a
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.2 MB (160201150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb8a2a4f7648b45467f4aa0fe60ff8e898aec63eb47f8fe773816f352281f9d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 06 Jan 2022 03:34:42 GMT
RUN Apply image ltsc2022-amd64
# Tue, 11 Jan 2022 22:29:41 GMT
SHELL [cmd /s /c]
# Tue, 11 Jan 2022 22:31:07 GMT
ENV JAVA_VERSION=jdk-11.0.13+8
# Tue, 11 Jan 2022 22:31:08 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 11 Jan 2022 22:31:09 GMT
USER ContainerAdministrator
# Tue, 11 Jan 2022 22:31:36 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 11 Jan 2022 22:31:37 GMT
USER ContainerUser
# Tue, 11 Jan 2022 22:32:49 GMT
COPY dir:6031cfac1e4bd8de6c5533bea0aabc25715779d854db7f41b8aea3e1449ff0bf in C:\openjdk-11 
# Tue, 11 Jan 2022 22:33:01 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:b2bb136f79c12b0a42720d7bb83469bce3f7bf2ca5c8bc68a36228796311fc6b`  
		Size: 117.3 MB (117334348 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6d7943d6864d35f22a1b2c416194fc3658b93c41ce26a946ba9e15f3671a482a`  
		Last Modified: Tue, 11 Jan 2022 23:15:45 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e894c08eabdfc1e06e6987a9e2ddb2c09f7ed7ab3fff08e844ce2fd39cfeba`  
		Last Modified: Tue, 11 Jan 2022 23:18:04 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:354ba3364c0860caa2c825a1a26150294a09393dbc8d761f75ebf52a5134d4db`  
		Last Modified: Tue, 11 Jan 2022 23:18:04 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1813bcae056bc8bff01b9f696c4fb9ade29fa3650f47d71868655e7eb388b8`  
		Last Modified: Tue, 11 Jan 2022 23:18:03 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66b33f93e8e63d7b84b32fad660161e51dbf6f1a7e32e1a8468b8c71a18bf32`  
		Last Modified: Tue, 11 Jan 2022 23:18:01 GMT  
		Size: 87.5 KB (87527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3bd79bcea18d4373c3bc7435754f27f555f49ef5bb335ba1a9cffbd150ba497`  
		Last Modified: Tue, 11 Jan 2022 23:18:02 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc58a7a6910f2f85e4edc961715510dd69cda8f54571e6b0d875ded502701f3`  
		Last Modified: Tue, 11 Jan 2022 23:18:44 GMT  
		Size: 42.7 MB (42715516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5badd6c94af7656d02a6bedba9e74e958f4b516029892e9ef87ddf5e5a1e1cdc`  
		Last Modified: Tue, 11 Jan 2022 23:18:35 GMT  
		Size: 58.1 KB (58099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.17763.2451; amd64

```console
$ docker pull eclipse-temurin@sha256:492153042dc035e1d0cc594b231708b5e3b9fd509cb91c9c1ab928989cf3aafa
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.9 MB (145908031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f48b77f53515d987e2284605229da6ef705726ef8c672e0ff22c4918274fc29`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jan 2022 05:19:42 GMT
RUN Apply image 1809-amd64
# Tue, 11 Jan 2022 21:33:30 GMT
SHELL [cmd /s /c]
# Tue, 11 Jan 2022 21:49:57 GMT
ENV JAVA_VERSION=jdk-11.0.13+8
# Tue, 11 Jan 2022 21:49:58 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 11 Jan 2022 21:49:59 GMT
USER ContainerAdministrator
# Tue, 11 Jan 2022 21:50:10 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 11 Jan 2022 21:50:10 GMT
USER ContainerUser
# Tue, 11 Jan 2022 21:58:59 GMT
COPY dir:6031cfac1e4bd8de6c5533bea0aabc25715779d854db7f41b8aea3e1449ff0bf in C:\openjdk-11 
# Tue, 11 Jan 2022 21:59:11 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:f9d5f05eef69cdb907192f860ff14ce569d925f1f53ac5255a5b37631124fd4d`  
		Size: 103.0 MB (103014618 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6cc5785ab09c66739c3205c3a26410f1cf4bf85c377fa81b240e754cf0659c58`  
		Last Modified: Tue, 11 Jan 2022 22:44:40 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c631e6fd097cbb2c567e65314f289e8c6f25271d826134deb37e896949b681c8`  
		Last Modified: Tue, 11 Jan 2022 22:56:07 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4275da636a39fa6869cb200e28126b14ee6577828242ee62ad04e6a6a0902f5`  
		Last Modified: Tue, 11 Jan 2022 22:56:07 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76a14996a9d65b46149cf4b8f6e6cfd1f36eb911cf8f1d9d2e985f7d17166109`  
		Last Modified: Tue, 11 Jan 2022 22:56:07 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e5754f2462f2d79793337f2b5fd207a7ce771c1d722d9230e66385d0661723`  
		Last Modified: Tue, 11 Jan 2022 22:56:05 GMT  
		Size: 68.3 KB (68261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d44c79847d5679fac223a6e171d5dfecfd1fb065806fb8839e42cb3f90fa3d8`  
		Last Modified: Tue, 11 Jan 2022 22:56:05 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97dd1825eddd974c21b55190cc92f013a7fb993baefc79af88e8f5e3ed2f536d`  
		Last Modified: Tue, 11 Jan 2022 23:01:20 GMT  
		Size: 42.7 MB (42739104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892c076dac7e68f49ab102f5f46f73328ddcffdf59d96e93c097652cc55b38c2`  
		Last Modified: Tue, 11 Jan 2022 23:01:12 GMT  
		Size: 80.4 KB (80399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
