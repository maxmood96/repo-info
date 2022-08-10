## `eclipse-temurin:11-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:135abdbe186976d53907e89ffbaa36b22a968c5d4077ccab0ef585c214e785ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.887; amd64
	-	windows version 10.0.17763.3287; amd64

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.20348.887; amd64

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

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.17763.3287; amd64

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
