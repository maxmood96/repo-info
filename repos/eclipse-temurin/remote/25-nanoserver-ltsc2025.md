## `eclipse-temurin:25-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:21ab7ba8b3978555b0bc3a064bb6bce7e10587c6043cc675136026a028fb242d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `eclipse-temurin:25-nanoserver-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull eclipse-temurin@sha256:410aa427bc8aeeabc23049e6cf704950e4d5a0d5fc443033d29e5a83979c75ef
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.1 MB (336079216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd54011dba478e2e91c43e16955fc0cbf4fc2130fd6a6f088323f403f0560c9f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 09 Nov 2025 10:04:50 GMT
RUN Apply image 10.0.26100.7171
# Tue, 11 Nov 2025 20:10:57 GMT
SHELL [cmd /s /c]
# Tue, 11 Nov 2025 20:13:09 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Tue, 11 Nov 2025 20:13:10 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 11 Nov 2025 20:13:10 GMT
USER ContainerAdministrator
# Tue, 11 Nov 2025 20:13:12 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 11 Nov 2025 20:13:13 GMT
USER ContainerUser
# Tue, 11 Nov 2025 20:13:24 GMT
COPY dir:889642903e29f32ff0f0b6da5f64cf6a40ecfa6d85d0926e4981ccbc885ac0c0 in C:\openjdk-25 
# Tue, 11 Nov 2025 20:13:29 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 11 Nov 2025 20:13:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:87c91227213eb6e7c8cfe33b6bd0429350e524756878f37f3860b013f804bf59`  
		Last Modified: Tue, 11 Nov 2025 20:41:49 GMT  
		Size: 197.9 MB (197936447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3719b064c723247381b30c79062f31cb652086c11ba8db976957ea55feb01df4`  
		Last Modified: Tue, 11 Nov 2025 20:12:16 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b0702a11bb87174c94228f2e8e8a5382be61bb8f84eb4b6224f0eaaba46d4f8`  
		Last Modified: Tue, 11 Nov 2025 20:13:54 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f3cb4abb53455ec9647a1ac3ed63cddec568ad2d013198df5b375b2d27841b`  
		Last Modified: Tue, 11 Nov 2025 20:13:54 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af0f9090038faf2c91a620b6d889ed8ddf2c0fde3faf0144d4fda450842d76b`  
		Last Modified: Tue, 11 Nov 2025 20:13:54 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b261326e27256d3079680eed76a252c579788d91dc2c2a50a1735b16bc8f3f`  
		Last Modified: Tue, 11 Nov 2025 20:13:54 GMT  
		Size: 72.8 KB (72848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2717c3a47bdcedf2a2ab7faa38db778a5be1dd0dd8f4fd605b937b7fb8b047c`  
		Last Modified: Tue, 11 Nov 2025 20:13:55 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5074c79aa222d100c388e300ad8bd5558b8ba1ee8916c8980bcde6a8b4b47e3b`  
		Last Modified: Tue, 11 Nov 2025 22:18:46 GMT  
		Size: 138.0 MB (137951559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6524ab40c11a27ccc38e662db5632035c46318cde546db7eefa3c4507f35f5`  
		Last Modified: Tue, 11 Nov 2025 20:13:54 GMT  
		Size: 112.0 KB (111975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3042ec8a7c2dac8b441a3d576847e934dc064bdcdb79667019cb56f11e91d3eb`  
		Last Modified: Tue, 11 Nov 2025 20:13:55 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
