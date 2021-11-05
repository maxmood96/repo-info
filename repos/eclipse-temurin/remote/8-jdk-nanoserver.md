## `eclipse-temurin:8-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:edd322a960265affe0e71bb49469a7923b1330437eb20e01ed75ee39c381cda9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.288; amd64
	-	windows version 10.0.17763.2237; amd64

### `eclipse-temurin:8-jdk-nanoserver` - windows version 10.0.20348.288; amd64

```console
$ docker pull eclipse-temurin@sha256:0254fb746d33d931e3df0dc282c3a5fa74dd4c4564fadbfc48fd261f68925e7f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 MB (217293441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13da8ffe4108cc75e2e998d3b3eb7fe9f6e4eeb37b8307bf7e3b925b43d0d061`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 07 Oct 2021 11:15:04 GMT
RUN Apply image ltsc2022-amd64
# Wed, 13 Oct 2021 19:02:30 GMT
SHELL [cmd /s /c]
# Fri, 05 Nov 2021 19:43:06 GMT
ENV JAVA_VERSION=jdk8u312-b07
# Fri, 05 Nov 2021 19:43:07 GMT
ENV JAVA_HOME=C:\openjdk-8
# Fri, 05 Nov 2021 19:43:07 GMT
USER ContainerAdministrator
# Fri, 05 Nov 2021 19:43:21 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 05 Nov 2021 19:43:22 GMT
USER ContainerUser
# Fri, 05 Nov 2021 19:43:32 GMT
COPY dir:7d20e7860b874019800a6393f3930849559cf997f64b86d2d0263d858293fa37 in C:\openjdk-8 
# Fri, 05 Nov 2021 19:43:46 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:91284e7e8fd4bd7ebcfa98544a3e4f59639f38281225c81c34b6fe22e0dba4e5`  
		Size: 116.9 MB (116939483 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1ba797e8f93823c3d71c52fcae413f3a33ca28ff2711c09ba5141432948f8298`  
		Last Modified: Wed, 13 Oct 2021 19:43:54 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9dec6b507607ca08e638c7d3ae3128972c49650144c514f4c38fc57ceb5c43`  
		Last Modified: Fri, 05 Nov 2021 20:39:18 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd9a6e263cf49da630f6760ba1b585fef5f0428dd256021064f116c34a3d2b98`  
		Last Modified: Fri, 05 Nov 2021 20:39:17 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee96e2b9d26ffc56e72b87fb9a7157aef8e02be14bc87c86f5eec89c492dc13`  
		Last Modified: Fri, 05 Nov 2021 20:39:15 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a309d0ae1eba4bee66a057c942a2f0bc3ecf5ce3637bb386e7302db6911bc8f3`  
		Last Modified: Fri, 05 Nov 2021 20:39:15 GMT  
		Size: 94.4 KB (94354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5beb7d50903a50966a72f48c7e65fa918cc57be153a73d494e86add07b2e55b9`  
		Last Modified: Fri, 05 Nov 2021 20:39:15 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7781661bd241457bca31a37c54819b089170552672f784676cccd3d49f1784`  
		Last Modified: Fri, 05 Nov 2021 20:39:27 GMT  
		Size: 100.2 MB (100187455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b984f6a8128dc7f416c473137ec4c4e859a43329261f55f319abdce761f637`  
		Last Modified: Fri, 05 Nov 2021 20:39:15 GMT  
		Size: 66.3 KB (66331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jdk-nanoserver` - windows version 10.0.17763.2237; amd64

```console
$ docker pull eclipse-temurin@sha256:31ea92962d6f6d2175f05d9726692cd192b24b5573dc26d404cc9dfaa0759edb
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.0 MB (202998082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5142854cd0cdf215e1ba2ab1fe97a728ceb7c0a89a6d4c1af6617a9c679344d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 07 Oct 2021 08:01:14 GMT
RUN Apply image 1809-amd64
# Wed, 13 Oct 2021 18:17:55 GMT
SHELL [cmd /s /c]
# Fri, 05 Nov 2021 19:18:23 GMT
ENV JAVA_VERSION=jdk8u312-b07
# Fri, 05 Nov 2021 19:18:24 GMT
ENV JAVA_HOME=C:\openjdk-8
# Fri, 05 Nov 2021 19:18:25 GMT
USER ContainerAdministrator
# Fri, 05 Nov 2021 19:18:49 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 05 Nov 2021 19:18:49 GMT
USER ContainerUser
# Fri, 05 Nov 2021 19:18:59 GMT
COPY dir:7d20e7860b874019800a6393f3930849559cf997f64b86d2d0263d858293fa37 in C:\openjdk-8 
# Fri, 05 Nov 2021 19:19:14 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:934e212983f208dc2bebc5de38259a6a62f1761868aacfee2cb3585a13b1e24b`  
		Size: 102.7 MB (102661372 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ceff24c3c0c2c360cd3788fcde5c41e1d6601339f4944623c732558a6030e631`  
		Last Modified: Wed, 13 Oct 2021 19:12:58 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177724a0db674e21ef5312fec420a4b52d5d2cc11f50b1618560b353b3d6b504`  
		Last Modified: Fri, 05 Nov 2021 20:22:24 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1511463fd5cb415be8764921c481a9f4720730625030680aef2b9733b3b9209b`  
		Last Modified: Fri, 05 Nov 2021 20:22:24 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb07f50c4396ee11e0efa3fb5bd2266c5659d6bcbaab9f40b250dc35be13699`  
		Last Modified: Fri, 05 Nov 2021 20:22:22 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb6006aacda1e222839c9f38b6f5c75362b53fbd85435ebbf419bb1993c309be`  
		Last Modified: Fri, 05 Nov 2021 20:22:22 GMT  
		Size: 69.0 KB (69001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a878a822d6235e0372f72239020c185d094c9e0141c1320b4f04b43614b1579`  
		Last Modified: Fri, 05 Nov 2021 20:22:22 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584ab9b080fd3f7e5216570d980f346631b3746e0eaaf84eb25f9a489ef6db1f`  
		Last Modified: Fri, 05 Nov 2021 20:24:12 GMT  
		Size: 100.2 MB (100179929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4d8dd4be8f14b929b59eee45b59465bb898bbad2b4e9b1cc456cf1d230b52b`  
		Last Modified: Fri, 05 Nov 2021 20:22:22 GMT  
		Size: 82.1 KB (82120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
