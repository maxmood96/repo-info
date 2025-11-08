## `eclipse-temurin:21-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:7ee3defb8dccf0a3045f7a438f42a34b218878549ff3e2e6e82e9ca170117e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6905; amd64
	-	windows version 10.0.20348.4297; amd64

### `eclipse-temurin:21-jre-nanoserver` - windows version 10.0.26100.6905; amd64

```console
$ docker pull eclipse-temurin@sha256:f5b0027165958fcd10134668b3f354f144771587fd5f5c5cf0f3a0434276260d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.3 MB (243272875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48066092b0bb647748261ace78a98a11b881462c63fe998502a2f1e361653df8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 22 Oct 2025 07:22:01 GMT
RUN Apply image 10.0.26100.6905
# Sat, 08 Nov 2025 19:16:45 GMT
SHELL [cmd /s /c]
# Sat, 08 Nov 2025 19:16:46 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Sat, 08 Nov 2025 19:16:46 GMT
ENV JAVA_HOME=C:\openjdk-21
# Sat, 08 Nov 2025 19:16:47 GMT
USER ContainerAdministrator
# Sat, 08 Nov 2025 19:16:53 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 08 Nov 2025 19:16:54 GMT
USER ContainerUser
# Sat, 08 Nov 2025 19:17:04 GMT
COPY dir:1612d20d6d454244847586ca6f13699611833617704a1c55730e9c479e5d220d in C:\openjdk-21 
# Sat, 08 Nov 2025 19:17:08 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:9188956580c47f583c927f17e42f8825823890544237141f21ca4ef10ea55e60`  
		Last Modified: Fri, 24 Oct 2025 11:13:56 GMT  
		Size: 194.0 MB (194029378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5a4112a31b422a7f7b32c75013023f8fce10f4ce3b96e83d0a9ee625daaf23c`  
		Last Modified: Sat, 08 Nov 2025 19:17:36 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66e58835a20cb2f50ff84bfe661987120abb6977556b864ba046c7e1464ea198`  
		Last Modified: Sat, 08 Nov 2025 19:17:35 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ff989dc22b13c09cc867d8a99e8d70a190ae2858aea489655865f4a1d1e05f`  
		Last Modified: Sat, 08 Nov 2025 19:17:35 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3e89d3f5d397b198eb0d8101d0e1cb8ec4a4fa2cfd435c3e95f2c4a398e1ebb`  
		Last Modified: Sat, 08 Nov 2025 19:17:36 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e96b05ad760ff96e75239d671da64713798740b76bef1aef4b300464719bc916`  
		Last Modified: Sat, 08 Nov 2025 19:17:36 GMT  
		Size: 87.2 KB (87247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5374a185d5d585bda5e313228e004d41500a096a83c093f35a9fe5244cd3036c`  
		Last Modified: Sat, 08 Nov 2025 19:17:36 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129b332f988c6142e1504eb24e1ce2d0a2bd561e7e844bf991c59c8998454af6`  
		Last Modified: Sat, 08 Nov 2025 19:17:39 GMT  
		Size: 49.0 MB (49034863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56373b38d23f4988ec914e32d406c524277781ab0e84ff38c2f16857999bb6bf`  
		Last Modified: Sat, 08 Nov 2025 19:17:37 GMT  
		Size: 116.1 KB (116085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre-nanoserver` - windows version 10.0.20348.4297; amd64

```console
$ docker pull eclipse-temurin@sha256:34b8a2e6be66f2250efa233335b10a0bb44cdfec7bfdf778865e3f0f60e85241
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171903935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7c2cbbac48db6ceaa2757466b549c376cd99fb66194d12775a15b247bbb29a4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 22 Oct 2025 21:38:30 GMT
RUN Apply image 10.0.20348.4297
# Sat, 08 Nov 2025 19:16:37 GMT
SHELL [cmd /s /c]
# Sat, 08 Nov 2025 19:18:12 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Sat, 08 Nov 2025 19:18:13 GMT
ENV JAVA_HOME=C:\openjdk-21
# Sat, 08 Nov 2025 19:18:14 GMT
USER ContainerAdministrator
# Sat, 08 Nov 2025 19:18:16 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 08 Nov 2025 19:18:17 GMT
USER ContainerUser
# Sat, 08 Nov 2025 19:18:26 GMT
COPY dir:1612d20d6d454244847586ca6f13699611833617704a1c55730e9c479e5d220d in C:\openjdk-21 
# Sat, 08 Nov 2025 19:18:30 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:2ac1abee018ad49a2f67a19d7f82901aac546affca76c86382db1a855dfcdaa1`  
		Last Modified: Fri, 24 Oct 2025 03:12:47 GMT  
		Size: 122.7 MB (122684063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f067baf40f21395bac37e4c7af8a0458f0bdce5214d71325155d2888213178`  
		Last Modified: Sat, 08 Nov 2025 19:18:48 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a810299cb83686d0513360e51578e262a52bab2a5217d72412a2d5432de9aa7`  
		Last Modified: Sat, 08 Nov 2025 19:18:48 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1c8bfbedeb0fab73b37122828e82484b96c4e5938113856fb7ce91aaf70c99`  
		Last Modified: Sat, 08 Nov 2025 19:18:48 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4096c90385b48b5054a753e4af8e929107fc22175c6d57021f36a9b4317bb967`  
		Last Modified: Sat, 08 Nov 2025 19:18:49 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b52250c48e653404400b1604e7f960daa8e6ca56c14c41d690c9c40c158a61a`  
		Last Modified: Sat, 08 Nov 2025 19:18:48 GMT  
		Size: 87.7 KB (87700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faecefbc564704de9ff3535a3ee50bac20c7c05478980eed6125b951a6cd2f49`  
		Last Modified: Sat, 08 Nov 2025 19:18:49 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0322edb6fb7910a40ac8197400c9813af94837e3eec5ff044edbbd8ba3eeabb1`  
		Last Modified: Sat, 08 Nov 2025 19:19:13 GMT  
		Size: 49.0 MB (49035145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a923d38de25be8494180012885a7bb7c335bf81123874efa8bb22ba1d78210a0`  
		Last Modified: Sat, 08 Nov 2025 19:18:50 GMT  
		Size: 91.8 KB (91786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
