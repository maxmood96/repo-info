## `eclipse-temurin:23-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:d652c989e545d3bdb283f02a3137b1075afd3181fb02b17c5ea69d4801ad5292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `eclipse-temurin:23-jre-nanoserver-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull eclipse-temurin@sha256:124da68bb365b233f248ff5403cedec7a63e0f86343745b771fac6c4416b1483
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.6 MB (159589292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74fca2080e5362f6abf8ed0db7aabbc9da27275e0524b03d4de6bf6218f8d68b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Thu, 13 Feb 2025 01:17:33 GMT
SHELL [cmd /s /c]
# Thu, 13 Feb 2025 01:17:34 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Thu, 13 Feb 2025 01:17:35 GMT
ENV JAVA_HOME=C:\openjdk-23
# Thu, 13 Feb 2025 01:17:36 GMT
USER ContainerAdministrator
# Thu, 13 Feb 2025 01:17:38 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 13 Feb 2025 01:17:39 GMT
USER ContainerUser
# Thu, 13 Feb 2025 01:17:43 GMT
COPY dir:f0b8f3d1970d52810d59047a7e1dfff98787b37140cc4aafc37fc86b09fa8be8 in C:\openjdk-23 
# Thu, 13 Feb 2025 01:17:46 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Wed, 12 Feb 2025 21:38:54 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9ae50f80add6e329a320188216ea095f83d125a3b6433ca4dd65d98af55251`  
		Last Modified: Thu, 13 Feb 2025 04:16:35 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0eadfeaa84a6f06352c7a13c6f24f96704a2c5a8d4b586c69524a340ef0bee2`  
		Last Modified: Thu, 13 Feb 2025 04:16:35 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:718fdd28f0ffb30987b97d0eb3e073b21663791fb98c92ae6ae8ee8d25d5c11f`  
		Last Modified: Thu, 13 Feb 2025 04:16:35 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e32810f8b3f5d0fb96ec8915e6142e5e289c71fe1360a5b5ae978bf13509792`  
		Last Modified: Thu, 13 Feb 2025 04:16:35 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d625b2d9e0720c3f33161389c8715c4f4cdd9f2fb579292a70f49be5189eeeb`  
		Last Modified: Thu, 13 Feb 2025 04:16:35 GMT  
		Size: 71.5 KB (71505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ad516ee215ba25c94ac787527a8bca1052bc875a4586525766bf1a418ed0f8`  
		Last Modified: Thu, 13 Feb 2025 04:16:35 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1f3ad896ab8dd43b22465760df65e40d23c180ae9646892600f849345dfe17`  
		Last Modified: Thu, 13 Feb 2025 04:16:40 GMT  
		Size: 49.0 MB (48980135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09bd81810b4a794ec09957a07fd3bc48419899ae96bccf4718addb97fad695d2`  
		Last Modified: Thu, 13 Feb 2025 04:16:36 GMT  
		Size: 3.6 MB (3616991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
