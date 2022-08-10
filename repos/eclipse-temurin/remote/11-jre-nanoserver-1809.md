## `eclipse-temurin:11-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:8ebeb4c32130854e71ac1a8e1efc8ccd56a5929319705d87f7fdb0b45055640b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3287; amd64

### `eclipse-temurin:11-jre-nanoserver-1809` - windows version 10.0.17763.3287; amd64

```console
$ docker pull eclipse-temurin@sha256:d13add2035e71317443b160b1cb67716a9b2f2422245a0f7cec0ba47ff61f228
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.3 MB (146270332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2fd22a3ee826320a91ac6628933442007e79b1973fbf6af9c41454fc94a9e2c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Aug 2022 18:08:38 GMT
RUN Apply image 10.0.17763.3287
# Wed, 10 Aug 2022 15:57:07 GMT
SHELL [cmd /s /c]
# Wed, 10 Aug 2022 16:05:32 GMT
ENV JAVA_VERSION=jdk-11.0.16+8
# Wed, 10 Aug 2022 16:05:32 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 10 Aug 2022 16:05:33 GMT
USER ContainerAdministrator
# Wed, 10 Aug 2022 16:05:45 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Aug 2022 16:05:46 GMT
USER ContainerUser
# Wed, 10 Aug 2022 16:10:10 GMT
COPY dir:ed8aecf12b2f8b5c8236f0bd623d348ed23ce1dd32f70bd039c8f6b01f0feff1 in C:\openjdk-11 
# Wed, 10 Aug 2022 16:10:25 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:5c9d6483dab113d2d9b50fdf3156622aa2ec3d6faaed5664d15a5568032d1714`  
		Size: 103.2 MB (103204200 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0f4438539876006761cb687527bd8cb94cc7a273cf8bb47563981044f2e1771e`  
		Last Modified: Wed, 10 Aug 2022 16:38:40 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:657f852163df6cebfdf48240b33ab5eea4779e39e44141bc456671ce1aa1425e`  
		Last Modified: Wed, 10 Aug 2022 16:41:18 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:449b42af65b7afcbbbbe1c63accbdf920def5029a2e6b1ee4ff4d5abe46c69bd`  
		Last Modified: Wed, 10 Aug 2022 16:41:18 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b17c585212e74e450fb63d27950a921745936476bc2e8456acb6e15be08b194e`  
		Last Modified: Wed, 10 Aug 2022 16:41:18 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae2de8d8bba305ce1fc7a9be34d0e0dc042978d170c3111a862ad186d46f6b3`  
		Last Modified: Wed, 10 Aug 2022 16:41:16 GMT  
		Size: 70.1 KB (70072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f810f1b70fd32f557675c11c5d40ede431212f45cef74be03da1470c029346ce`  
		Last Modified: Wed, 10 Aug 2022 16:41:16 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6063119579ddaa4540c9bcc5cbdfb197401d49b0d33efcd39cc3acaad14e20c`  
		Last Modified: Wed, 10 Aug 2022 16:42:35 GMT  
		Size: 42.9 MB (42908613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16274d5ba1a9e252253a01733fc954383b39c9de036189f1ccf2a3631c1cb982`  
		Last Modified: Wed, 10 Aug 2022 16:42:26 GMT  
		Size: 81.7 KB (81714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
