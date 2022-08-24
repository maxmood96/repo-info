## `eclipse-temurin:17-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:e3ea7ae31afbe93d9a9629ca866f5f132b9b640acfb1c44c61666c1246baf22d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3287; amd64

### `eclipse-temurin:17-jre-nanoserver-1809` - windows version 10.0.17763.3287; amd64

```console
$ docker pull eclipse-temurin@sha256:9cfaad7a0ec81bcae5f23249e77f22d9ec35c30ef2059d0f39d3291a752b4a18
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.5 MB (149540547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6e9bd921659312b51877200ef0d49ad234603a66bb0dcd7faf2333f9881f1ea`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Aug 2022 18:08:38 GMT
RUN Apply image 10.0.17763.3287
# Wed, 10 Aug 2022 15:57:07 GMT
SHELL [cmd /s /c]
# Wed, 24 Aug 2022 19:32:32 GMT
ENV JAVA_VERSION=jdk-17.0.4.1+1
# Wed, 24 Aug 2022 19:32:34 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 24 Aug 2022 19:32:36 GMT
USER ContainerAdministrator
# Wed, 24 Aug 2022 19:32:47 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 24 Aug 2022 19:32:49 GMT
USER ContainerUser
# Wed, 24 Aug 2022 19:37:41 GMT
COPY dir:b68e969b54b81d301cc08056fc3e121f2bd91a79ba6f45c80e26c9a9bf23468d in C:\openjdk-17 
# Wed, 24 Aug 2022 19:37:57 GMT
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
	-	`sha256:87fa2b53daf0a009f5a5680ea21a6824afb9c997d21d4af46e7ecbd040aedb25`  
		Last Modified: Wed, 24 Aug 2022 19:49:56 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84c58823a6432e12c859def58c6ade94ad6f5e69a17f00a498addd51bb3e720e`  
		Last Modified: Wed, 24 Aug 2022 19:49:56 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63421ad3f49280b92c57458103894100ddd4da8e3ca2d79c12d8822a49b362f`  
		Last Modified: Wed, 24 Aug 2022 19:49:56 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af847c6b5654a4d258551cb35881903437f1fe149b67a38f3f2a3b39a392e451`  
		Last Modified: Wed, 24 Aug 2022 19:49:53 GMT  
		Size: 68.3 KB (68322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe245120e2dcfd02c932cd908b4499472c897b5f9aa5bb5f17ec726e9fe901d`  
		Last Modified: Wed, 24 Aug 2022 19:49:53 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec5f79bed20578e767e24406f16b98f6b3e034eb2c36ca6624a1c63b2eacd1b`  
		Last Modified: Wed, 24 Aug 2022 19:51:28 GMT  
		Size: 43.2 MB (43228599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77f0c3b4eb715d78e6a0f351714debb8236c9bcf0c3b507bab10e96c74d2de26`  
		Last Modified: Wed, 24 Aug 2022 19:51:19 GMT  
		Size: 3.0 MB (3033711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
