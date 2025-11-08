## `eclipse-temurin:8-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:e0ec74c6e1dce862eadb582309600729e810780d6e83ce4ca6885ba5036ad1b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6905; amd64
	-	windows version 10.0.20348.4297; amd64

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.26100.6905; amd64

```console
$ docker pull eclipse-temurin@sha256:0a2c91add668c6863f60aa2e5214d96bee09772412d1630529b1588fc7cee8dd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.8 MB (234763340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:379936b3bac5c796c7ebacfaebd2d2d89ac3c46905683f767f6ce4c0c32ae688`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 22 Oct 2025 07:22:01 GMT
RUN Apply image 10.0.26100.6905
# Sat, 08 Nov 2025 19:17:35 GMT
SHELL [cmd /s /c]
# Sat, 08 Nov 2025 19:17:36 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 19:17:37 GMT
ENV JAVA_HOME=C:\openjdk-8
# Sat, 08 Nov 2025 19:17:38 GMT
USER ContainerAdministrator
# Sat, 08 Nov 2025 19:17:47 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 08 Nov 2025 19:17:47 GMT
USER ContainerUser
# Sat, 08 Nov 2025 19:18:03 GMT
COPY dir:d46ae848a780de83988aca6679aeefb6cb592f306ae2eca344ddb66bc6559a89 in C:\openjdk-8 
# Sat, 08 Nov 2025 19:18:07 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:9188956580c47f583c927f17e42f8825823890544237141f21ca4ef10ea55e60`  
		Last Modified: Fri, 24 Oct 2025 11:13:56 GMT  
		Size: 194.0 MB (194029378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef09d293eebed8f2f1c597bfa2e946d24892ff5f7aaad5c1eafa9252b51e01a`  
		Last Modified: Sat, 08 Nov 2025 19:18:23 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f64d3febef62c6be987610f0fcd12d9354695dcb5f896bda904ef51102f4e0`  
		Last Modified: Sat, 08 Nov 2025 19:18:23 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e665da6c43752acbf7a3061a170a11060a9c40d88c93f5aa1dc19e167228f68`  
		Last Modified: Sat, 08 Nov 2025 19:18:23 GMT  
		Size: 1.1 KB (1084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ad8c40bccc27b2427724013e993a7f751ff13b6303a22dd9330ba3d3c9baa35`  
		Last Modified: Sat, 08 Nov 2025 19:18:25 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e39c4e2f445b666cc8547de33028be53bbef766ceec10ed5682fb18702cd527`  
		Last Modified: Sat, 08 Nov 2025 19:18:23 GMT  
		Size: 70.6 KB (70583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7097742967b6134833dc17f1dedd37ac3a3222f9c2bf6228a3f37ff26b5f43be`  
		Last Modified: Sat, 08 Nov 2025 19:18:23 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dbb3a2090927719b8c08608f554300c6840588465ceec79aaa1e1656cb0ecea`  
		Last Modified: Sat, 08 Nov 2025 19:18:29 GMT  
		Size: 40.6 MB (40555166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:056a1bb5ef5d2408623f0438bdfa8f720a5e4dec88ecce48a9716e1731677226`  
		Last Modified: Sat, 08 Nov 2025 19:18:23 GMT  
		Size: 102.9 KB (102855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.20348.4297; amd64

```console
$ docker pull eclipse-temurin@sha256:59589248fecd252ecab12b4c3228d9bc7f96f16522741dfc06595331b642fc6f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.4 MB (163431416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91e3d08677b8c8112736b79dc50d209b764a567ae37c0d3dbb3c8db0561fca9a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 22 Oct 2025 21:38:30 GMT
RUN Apply image 10.0.20348.4297
# Sat, 08 Nov 2025 18:23:50 GMT
SHELL [cmd /s /c]
# Sat, 08 Nov 2025 18:23:51 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 18:23:52 GMT
ENV JAVA_HOME=C:\openjdk-8
# Sat, 08 Nov 2025 18:23:53 GMT
USER ContainerAdministrator
# Sat, 08 Nov 2025 18:24:03 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 08 Nov 2025 18:24:04 GMT
USER ContainerUser
# Sat, 08 Nov 2025 18:24:21 GMT
COPY dir:d46ae848a780de83988aca6679aeefb6cb592f306ae2eca344ddb66bc6559a89 in C:\openjdk-8 
# Sat, 08 Nov 2025 18:24:25 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:2ac1abee018ad49a2f67a19d7f82901aac546affca76c86382db1a855dfcdaa1`  
		Last Modified: Fri, 24 Oct 2025 03:12:47 GMT  
		Size: 122.7 MB (122684063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f3d1b99aefd432856f0f4f98d27b5fc5c2951dd239b9d32746c7be474a64ff`  
		Last Modified: Sat, 08 Nov 2025 18:24:42 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a57bd6e68039542479b85990ec2d046fa3f5af7a9c508a3ae77a90be64b6b9`  
		Last Modified: Sat, 08 Nov 2025 18:24:42 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a78af6eddc59f287a7ecb9f93c47b7059fe67067aed8f656d29604ee8dfa209`  
		Last Modified: Sat, 08 Nov 2025 18:24:44 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0daa312075efaef75a9be3281324de5f81a0ce53d6e54f28fda2f92616f79eaa`  
		Last Modified: Sat, 08 Nov 2025 18:24:44 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8363dbe7195d3c9dca6936ca3938fc8994b81146c8b8d3ff00ea774af7feee`  
		Last Modified: Sat, 08 Nov 2025 18:24:44 GMT  
		Size: 81.2 KB (81223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02544e3c0cd892fadc13ac4e1ff560e2d5cc02099ed4f1490d4b338a36de9b61`  
		Last Modified: Sat, 08 Nov 2025 18:24:45 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63fb7bbde907e99c2946732038ad0a0de0406d0ed15971d753f7969d6e9fe972`  
		Last Modified: Sat, 08 Nov 2025 18:24:54 GMT  
		Size: 40.6 MB (40554912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff9d1baaf7151f2ea06920a0c6487b53ab0f7e9b86b40f3fb01fc498cfb6044`  
		Last Modified: Sat, 08 Nov 2025 18:24:45 GMT  
		Size: 105.9 KB (105918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
