## `eclipse-temurin:11-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:0777e79ec4d47f0c610091e7747fe8d2751f0a2be3e7f244c69d4d2b6247ad5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.469; amd64
	-	windows version 10.0.17763.2452; amd64

### `eclipse-temurin:11-jdk-nanoserver` - windows version 10.0.20348.469; amd64

```console
$ docker pull eclipse-temurin@sha256:d7c683d03219ab30615d2ef2552b4f8c9d474a4457cf863d810d7b9eecd4f423
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.4 MB (309417346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4f86e22df87fcdf19770c455fd64c9133667d8a6229231653a5cf014592e7f3`
-	Default Command: `["jshell"]`
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
# Tue, 11 Jan 2022 22:32:10 GMT
COPY dir:7549fd743977f7762910679960e9adfeab116385590a40bc0f1570100fce1af1 in C:\openjdk-11 
# Tue, 11 Jan 2022 22:32:24 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 11 Jan 2022 22:32:25 GMT
CMD ["jshell"]
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
	-	`sha256:c69a190d0e6cdbc144ae2bcc5bf663103cae49ea54567e279550659ec9516f32`  
		Last Modified: Tue, 11 Jan 2022 23:18:21 GMT  
		Size: 191.9 MB (191930601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af330571e550839ef0544057dfbd24acae425f6cf87072fce67fb4fd117855c1`  
		Last Modified: Tue, 11 Jan 2022 23:18:01 GMT  
		Size: 58.0 KB (58044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c7c82d8c5e58b78214589ecb1441cad235d14631bb8780a2b068a42980656f6`  
		Last Modified: Tue, 11 Jan 2022 23:18:01 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-nanoserver` - windows version 10.0.17763.2452; amd64

```console
$ docker pull eclipse-temurin@sha256:8a95e000d12f0ac1f02b11f30f6922aca5c6406627ac33cc6cc698a7153ea036
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 MB (295111504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:732dd0be8e7f9d71d0e6457c4a01624b4536aaf482a94ec4e71b591032c2bcd9`
-	Default Command: `["jshell"]`
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
# Wed, 12 Jan 2022 15:42:26 GMT
COPY dir:7549fd743977f7762910679960e9adfeab116385590a40bc0f1570100fce1af1 in C:\openjdk-11 
# Wed, 12 Jan 2022 15:42:41 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 12 Jan 2022 15:42:42 GMT
CMD ["jshell"]
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
	-	`sha256:1b3d15b667502ab1849ea818f83f3178bd45d715cfbd787e79813079bedbf608`  
		Last Modified: Wed, 12 Jan 2022 16:13:31 GMT  
		Size: 191.9 MB (191943499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e610303cd010c1f3e52059bcbc86d016296a3b20bc7171572be04fc19c6bdd`  
		Last Modified: Wed, 12 Jan 2022 16:13:12 GMT  
		Size: 58.3 KB (58266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71fef56b14c7ab5275c55c77a2f5e77c54c95d9e47ed04e50f836573b0b42def`  
		Last Modified: Wed, 12 Jan 2022 16:13:12 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
