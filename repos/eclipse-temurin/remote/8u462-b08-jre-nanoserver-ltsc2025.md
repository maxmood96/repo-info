## `eclipse-temurin:8u462-b08-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:697b6724a18fc22074b2fb796e0276780e1f3215fbac72a994cbd7f889d6378f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6905; amd64

### `eclipse-temurin:8u462-b08-jre-nanoserver-ltsc2025` - windows version 10.0.26100.6905; amd64

```console
$ docker pull eclipse-temurin@sha256:2fd79343ca4d17763f8f8356f8624fe52bb10c44ff8648f9f207fdd8b2579f33
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.8 MB (234767082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7c37d75ef5e91dedcfd606f2910f985bbb2183e919bd9f23dac24a7fa19c7a9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 22 Oct 2025 07:22:01 GMT
RUN Apply image 10.0.26100.6905
# Fri, 24 Oct 2025 19:20:51 GMT
SHELL [cmd /s /c]
# Fri, 24 Oct 2025 19:20:52 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 24 Oct 2025 19:20:53 GMT
ENV JAVA_HOME=C:\openjdk-8
# Fri, 24 Oct 2025 19:20:53 GMT
USER ContainerAdministrator
# Fri, 24 Oct 2025 19:20:58 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 24 Oct 2025 19:20:58 GMT
USER ContainerUser
# Fri, 24 Oct 2025 19:21:03 GMT
COPY dir:dae5853f4b111011cf1e21d00736b413be35f27636dbbe76d1c13e33a12f455a in C:\openjdk-8 
# Fri, 24 Oct 2025 19:21:07 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:9188956580c47f583c927f17e42f8825823890544237141f21ca4ef10ea55e60`  
		Last Modified: Fri, 24 Oct 2025 11:13:56 GMT  
		Size: 194.0 MB (194029378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8407703267a708f1e861d96ba7297b491ec4181f89a12fcf487a7b283523fd8a`  
		Last Modified: Fri, 24 Oct 2025 19:21:56 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54292356ef002a246ae14ad8d9bacc4ae5219c9db3f5bf270d39276a10979e5c`  
		Last Modified: Fri, 24 Oct 2025 19:21:56 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67509d601dcc388f095a258a6c0a25058beba808819da3e8e5ff663049fe51c9`  
		Last Modified: Fri, 24 Oct 2025 19:21:56 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:823f68e46c596940b7564b86fb15f86994fb43136d277f1f7fc043fdf3abf0e9`  
		Last Modified: Fri, 24 Oct 2025 19:21:56 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d79d4086ef409528d92a6868c108c26288c0d3d022f74e175072df0360f51a8`  
		Last Modified: Fri, 24 Oct 2025 19:21:56 GMT  
		Size: 72.0 KB (71960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc5284c3bd386bc6b4a13d0b74d3368f052e0f0538fd72fa314b4237640ce0da`  
		Last Modified: Fri, 24 Oct 2025 19:21:56 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81812a76a42ea5d9f73af608faa8d06e539fd5e76677efa46e06a4a5234a5f63`  
		Last Modified: Fri, 24 Oct 2025 19:22:00 GMT  
		Size: 40.5 MB (40548135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd1c13c223db4bb6cd997e28d88b7ce0a5103e0aa12130c851911c037f309dff`  
		Last Modified: Fri, 24 Oct 2025 19:21:56 GMT  
		Size: 112.3 KB (112336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
