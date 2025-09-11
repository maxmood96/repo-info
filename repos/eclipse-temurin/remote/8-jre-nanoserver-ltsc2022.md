## `eclipse-temurin:8-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:8f1ae9bac4395ef4e595259b83f83f032862cccf6243319c09aa07812c0bc121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `eclipse-temurin:8-jre-nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull eclipse-temurin@sha256:e5efd07cca8ebc56f787a804e0e48963b79488c86028536c152cf34b927457a1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.4 MB (163448901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6631258942bcddeac26303547b0a9a67dc17a3016b72c693ddcc71ee8f9c39fc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Wed, 10 Sep 2025 22:18:12 GMT
SHELL [cmd /s /c]
# Wed, 10 Sep 2025 22:18:12 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Wed, 10 Sep 2025 22:18:13 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 10 Sep 2025 22:18:13 GMT
USER ContainerAdministrator
# Wed, 10 Sep 2025 22:18:18 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Sep 2025 22:18:18 GMT
USER ContainerUser
# Wed, 10 Sep 2025 22:18:25 GMT
COPY dir:dae5853f4b111011cf1e21d00736b413be35f27636dbbe76d1c13e33a12f455a in C:\openjdk-8 
# Wed, 10 Sep 2025 22:18:28 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bb56447072c84a7a61486562bdd4fd94d34eb682f5354768aeaaafe4b53fe1a`  
		Last Modified: Wed, 10 Sep 2025 22:19:31 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ed16b19d6f8a59bd25006a71b2ef16c9bb23e7a1350dbcca4ac1d6cb06d2bbf`  
		Last Modified: Wed, 10 Sep 2025 22:19:31 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1ab8f687fec68e6a2031bf262ddfaee44659ab5c8a0bc65cac7d80c78b7f5d0`  
		Last Modified: Wed, 10 Sep 2025 22:19:31 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73dfcf66d89656aded37c2c4b82f36b5760880bccb2f171b52014470ffbb39f8`  
		Last Modified: Wed, 10 Sep 2025 22:19:32 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e561d2f0364b4d164c945615f0928d960ad150d59f913bcf392a94b5190d6e`  
		Last Modified: Wed, 10 Sep 2025 22:19:31 GMT  
		Size: 87.4 KB (87423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51115d99044c7c543f94189f9adb915944320953e2d169b2d8953920ba88043`  
		Last Modified: Wed, 10 Sep 2025 22:19:31 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03d39061c9c6deba04dcfc47a8384aa5e6158e8c1dcf3e9424c7ba04c56d9ba`  
		Last Modified: Wed, 10 Sep 2025 22:19:39 GMT  
		Size: 40.5 MB (40547972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a994189caea4d186f0a78b7959cb916b2064802be0f5d31ad7317420fc591b95`  
		Last Modified: Wed, 10 Sep 2025 22:19:32 GMT  
		Size: 88.2 KB (88181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
