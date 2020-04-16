## `openjdk:8-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:87d0207f71feb7feaff0dae7f13cf23822c36dbcfd1b84146cc635159a574951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1158; amd64

### `openjdk:8-jdk-nanoserver` - windows version 10.0.17763.1158; amd64

```console
$ docker pull openjdk@sha256:5cc39fcd71f102c0f8c6b7cb83961fad6a9d5f75b8ee43b6002d13c500aa0f12
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.0 MB (200989107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7ff414229af7669f70c70e686d3d4fe01656d91dbc072257a5f751abf1aa4b4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 12 Apr 2020 11:41:03 GMT
RUN Apply image 1809-amd64
# Tue, 14 Apr 2020 21:42:38 GMT
SHELL [cmd /s /c]
# Tue, 14 Apr 2020 22:09:12 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 14 Apr 2020 22:09:13 GMT
USER ContainerAdministrator
# Tue, 14 Apr 2020 22:09:25 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Tue, 14 Apr 2020 22:09:25 GMT
USER ContainerUser
# Thu, 16 Apr 2020 01:04:35 GMT
ENV JAVA_VERSION=8u252
# Thu, 16 Apr 2020 01:05:00 GMT
COPY dir:ab479e12b22d2d8e4d7a7f2a7c1ce2c9a985b2211941ab66c77b1be78e3ec440 in C:\openjdk-8 
# Thu, 16 Apr 2020 01:05:18 GMT
RUN echo Verifying install ... 	&& echo   javac -version && javac -version 	&& echo   java -version && java -version
```

-	Layers:
	-	`sha256:0fe89239909ba300aeb9b977458b61ae3fbbcd2d9591086ed05ca023209d3122`  
		Size: 101.1 MB (101118377 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:895ca47ba9cf1a5b61a0721217cfcc038bbe9a4987c7536321c3ac51ef8e5e0c`  
		Last Modified: Tue, 14 Apr 2020 22:17:22 GMT  
		Size: 836.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464df3018907c0527ae16790c7ef6af4d221c5a2c0a690ee308cfda190d2ae5e`  
		Last Modified: Tue, 14 Apr 2020 22:28:05 GMT  
		Size: 862.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:769a32652de01c0d6233289167835286ca3016229fee54adc998f71929b746bd`  
		Last Modified: Tue, 14 Apr 2020 22:28:05 GMT  
		Size: 866.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abf786c0bf7c6b12e21a30f380f2a5fdf5e9c65a9e257beaba2d4787140bc8f2`  
		Last Modified: Tue, 14 Apr 2020 22:28:03 GMT  
		Size: 66.0 KB (66008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3441b13590eaa83583b349361ff2920e835efdb191f68c066a858e5485ddbbf3`  
		Last Modified: Tue, 14 Apr 2020 22:28:02 GMT  
		Size: 890.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc28dcec7ca224286dd636d167f55d9f403261f13a05206be188af9727019cb`  
		Last Modified: Thu, 16 Apr 2020 01:15:26 GMT  
		Size: 831.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e5f0ec8fe5ad06639ce08a085d12690e8e54ddf7d74da09964dfc0d11286993`  
		Last Modified: Thu, 16 Apr 2020 01:15:38 GMT  
		Size: 99.7 MB (99746055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d2550de4cacabffb6ec8b1a2d03fe2fb9baf18dc08a83c36502374a9d884b84`  
		Last Modified: Thu, 16 Apr 2020 01:15:26 GMT  
		Size: 54.4 KB (54382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
