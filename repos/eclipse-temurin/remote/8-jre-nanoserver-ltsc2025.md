## `eclipse-temurin:8-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:7d18c380b3e962c8000ba90f85bf96bb43dd7722552ff4a4ff7a1f1736fd43e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6905; amd64

### `eclipse-temurin:8-jre-nanoserver-ltsc2025` - windows version 10.0.26100.6905; amd64

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
