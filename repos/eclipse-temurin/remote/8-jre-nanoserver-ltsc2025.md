## `eclipse-temurin:8-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:17a03f8ca0bd8c9c6532bbdf8e43800c32d27ae6f0ecdbb1e9ed8ddf3af0339e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32522; amd64

### `eclipse-temurin:8-jre-nanoserver-ltsc2025` - windows version 10.0.26100.32522; amd64

```console
$ docker pull eclipse-temurin@sha256:526dbfe3aad112801d474a01cc0a179637163bcf31e7541ed4cef21ca142d092
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.5 MB (239541783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c30b8c7d9e78fce4a4ff89aa5bd0b59a1ad223922669c1d4dd3a31ed94292a0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Mar 2026 01:45:55 GMT
RUN Apply image 10.0.26100.32522
# Tue, 10 Mar 2026 22:42:57 GMT
SHELL [cmd /s /c]
# Tue, 10 Mar 2026 22:42:58 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 10 Mar 2026 22:42:59 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 10 Mar 2026 22:42:59 GMT
USER ContainerAdministrator
# Tue, 10 Mar 2026 22:43:04 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Mar 2026 22:43:04 GMT
USER ContainerUser
# Tue, 10 Mar 2026 22:43:10 GMT
COPY dir:e192ec1627bb02acae941746a6647cea6857b84f7daa4f746913822a0bac9dcc in C:\openjdk-8 
# Tue, 10 Mar 2026 22:43:13 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:06fab7822816d5f43d6835d07ac8db280fdf81384187f36d8dc43bbb7064a76d`  
		Last Modified: Tue, 10 Mar 2026 20:41:46 GMT  
		Size: 199.4 MB (199409325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982f6bcd510ac3d867816ccc93a3285f373275b9c91df694985b091ce189a66b`  
		Last Modified: Tue, 10 Mar 2026 22:43:18 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c51e5c79ba90603b1e4ac729bf2671990420bb737fa00a23f57052d2ae6760c`  
		Last Modified: Tue, 10 Mar 2026 22:43:18 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03ba2bcc6a24e51b7a322d198dea744e3287ae16fb825b5750733f8cff71da2`  
		Last Modified: Tue, 10 Mar 2026 22:43:18 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dead7438daf7ba3d9aa881827833db71731d1ac4ac15a1b6294bc703f7ff49b2`  
		Last Modified: Tue, 10 Mar 2026 22:43:16 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e384b79d32873328a227206543c4298bf9103ce8e7cf17405b284d8e753438`  
		Last Modified: Tue, 10 Mar 2026 22:43:16 GMT  
		Size: 77.6 KB (77567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34871689e9a61b776e28e85a52426fe72779df3b6206f9ca3163b8ab9a05e44e`  
		Last Modified: Tue, 10 Mar 2026 22:43:16 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0045ee81f835dd6b86f094c7e7afd6bb1961f6e425827933ffe6e288e01dd75`  
		Last Modified: Tue, 10 Mar 2026 22:43:20 GMT  
		Size: 40.0 MB (39969860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f87aa06f05f77f514de81001d709035999fab1286f33b21f4c6a70ea673ea8a`  
		Last Modified: Tue, 10 Mar 2026 22:43:16 GMT  
		Size: 79.7 KB (79683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
