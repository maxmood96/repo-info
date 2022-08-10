## `eclipse-temurin:11-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:ed3da0420f16de64b7ceafb7d0e0c5350566409a7f735d6e1e68de79e0ac2f94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.887; amd64

### `eclipse-temurin:11-jre-nanoserver-ltsc2022` - windows version 10.0.20348.887; amd64

```console
$ docker pull eclipse-temurin@sha256:3ace50c3d2695bb6e3f2e925e4625d453b2fa8ce1727670933317a6525c8544e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.1 MB (161149599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44d24641fc82cdd1a8d282e5eec9d5e5d5aeb8b05bcf0401b0ae6bc25595ea25`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Aug 2022 18:05:23 GMT
RUN Apply image 10.0.20348.887
# Wed, 10 Aug 2022 16:28:17 GMT
SHELL [cmd /s /c]
# Wed, 10 Aug 2022 16:29:53 GMT
ENV JAVA_VERSION=jdk-11.0.16+8
# Wed, 10 Aug 2022 16:29:54 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 10 Aug 2022 16:29:55 GMT
USER ContainerAdministrator
# Wed, 10 Aug 2022 16:30:17 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Aug 2022 16:30:18 GMT
USER ContainerUser
# Wed, 10 Aug 2022 16:31:22 GMT
COPY dir:ed8aecf12b2f8b5c8236f0bd623d348ed23ce1dd32f70bd039c8f6b01f0feff1 in C:\openjdk-11 
# Wed, 10 Aug 2022 16:31:56 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:2ebf439f800cd4c1fccaf4a0545e6bff60caa5141295c8ab81f6c525073c423d`  
		Size: 118.1 MB (118088450 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5f1e06146ab0490d235fe89786637467a4b71853ee428e8740ea6efbc536c47c`  
		Last Modified: Wed, 10 Aug 2022 16:48:40 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4f00e89b19d1ce99daab79ba1bcca3e29ad052342fc52687679c6a9e6bdec0`  
		Last Modified: Wed, 10 Aug 2022 16:49:19 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2afc3c37badc7edc01952be676e9530d9ec3492ccf678d80c67b9548b96bee`  
		Last Modified: Wed, 10 Aug 2022 16:49:19 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef6a0937662bedc3cabcdb61a1381d73205583cc8305c01e7a454d9d497173d8`  
		Last Modified: Wed, 10 Aug 2022 16:49:19 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0950a807fee1581948edb4112ce7ac3456a011f5420c15f19c5a429ecac0ac3e`  
		Last Modified: Wed, 10 Aug 2022 16:49:17 GMT  
		Size: 87.6 KB (87631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5c928d9674ef57d0d85aa68dbff73f5992d86b39e5bc4f23d6db42329416c4`  
		Last Modified: Wed, 10 Aug 2022 16:49:17 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9dba244837b2ff14218bbfcc29ed0c4c455f118fae1c8811f7e943bda6dca83`  
		Last Modified: Wed, 10 Aug 2022 16:49:56 GMT  
		Size: 42.9 MB (42904061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e15d5e426234ceec9bc0918a502ab0da90087ca3b5b276d970a5367eafdc728`  
		Last Modified: Wed, 10 Aug 2022 16:49:48 GMT  
		Size: 63.7 KB (63723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
