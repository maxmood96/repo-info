## `eclipse-temurin:11-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:c489645e710c7cb4957cd72e9037665f806d6d564296ca5ad1bf70c35aa39041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.469; amd64
	-	windows version 10.0.17763.2452; amd64

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

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.17763.2452; amd64

```console
$ docker pull eclipse-temurin@sha256:e3268dc2ac51cf26be947edb54d22ba100408e1d9fa91109d8e3215d8688d0ca
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.9 MB (145886351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a2bf700f210b2a123c3e27b34e230ce9ab4848410b9aadc1bf5217f0262afed`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jan 2022 22:25:06 GMT
RUN Apply image 1809-amd64
# Wed, 12 Jan 2022 05:19:56 GMT
SHELL [cmd /s /c]
# Wed, 12 Jan 2022 15:41:41 GMT
ENV JAVA_VERSION=jdk-11.0.13+8
# Wed, 12 Jan 2022 15:41:42 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 12 Jan 2022 15:41:43 GMT
USER ContainerAdministrator
# Wed, 12 Jan 2022 15:41:55 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Jan 2022 15:41:56 GMT
USER ContainerUser
# Wed, 12 Jan 2022 15:45:58 GMT
COPY dir:6031cfac1e4bd8de6c5533bea0aabc25715779d854db7f41b8aea3e1449ff0bf in C:\openjdk-11 
# Wed, 12 Jan 2022 15:46:08 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:3a78847ea829208edc2d7b320b7e602b9d12e47689499d5180a9cc7790dec4d7`  
		Size: 103.0 MB (103031066 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:71dcb756adb8534a87210067788d6aa4a5a366b72d022b7af035e5263a3e54a0`  
		Last Modified: Wed, 12 Jan 2022 16:05:17 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4ea70b005e41ddc4a95fc7fb15951e348a19152d6b73a3b12bfb999fc6a257`  
		Last Modified: Wed, 12 Jan 2022 16:13:15 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dca5a57808ce387df1ce94bb982a29da2a12df8e756f6c08841cd2c50514a5a`  
		Last Modified: Wed, 12 Jan 2022 16:13:15 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae7a5ceb0434da477def40e4519d41218e841f10f8fd2590d8c3a67c9eb34e5a`  
		Last Modified: Wed, 12 Jan 2022 16:13:14 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8739b602e8fca551fcf4512abe5c66b4fe03a2086bf109b24193c8cd919169ff`  
		Last Modified: Wed, 12 Jan 2022 16:13:12 GMT  
		Size: 71.7 KB (71701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc86a69fcf0830120bf56c69b5a19bb167b7193783c3d071858b50aef785aec5`  
		Last Modified: Wed, 12 Jan 2022 16:13:12 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed9c850d0df5b835f82a653188a80bf74427a8e5a29bfaebbdb2776780c2a434`  
		Last Modified: Wed, 12 Jan 2022 16:14:14 GMT  
		Size: 42.7 MB (42728393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:676987ef5191f314774b94c0b618bfcad3866e0889d0b85d9c2f2c9065a77834`  
		Last Modified: Wed, 12 Jan 2022 16:14:06 GMT  
		Size: 49.4 KB (49397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
