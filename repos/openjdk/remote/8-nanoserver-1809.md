## `openjdk:8-nanoserver-1809`

```console
$ docker pull openjdk@sha256:412c240b37cda27948001bb5dd41b6c8a127eb482b465009da782b8de1f2f2a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1158; amd64

### `openjdk:8-nanoserver-1809` - windows version 10.0.17763.1158; amd64

```console
$ docker pull openjdk@sha256:aebcce49f86f83cc3d81f5f75812b11a96bb59714f07e8b7f27710aa5089c6f9
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.7 MB (200716572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43d3e253cb8cba96d1b268947086f05744032b6a3555e7275ec9cd5e962abebe`
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
# Tue, 14 Apr 2020 22:09:26 GMT
ENV JAVA_VERSION=8u242
# Tue, 14 Apr 2020 22:09:59 GMT
COPY dir:604850e4892a2e6375b4d95fb378e9776042497a20a33de1bbe6b0d17fade1d2 in C:\openjdk-8 
# Tue, 14 Apr 2020 22:10:17 GMT
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
	-	`sha256:84a7d2dd1a37d31c13991d6bb5ee42f738fa90168ea598efaeef6a5a87c012d5`  
		Last Modified: Tue, 14 Apr 2020 22:28:02 GMT  
		Size: 925.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015d707377387606ed4b0ae94557dbe08b4a01bece1d68864afe050f441b2c33`  
		Last Modified: Tue, 14 Apr 2020 22:28:14 GMT  
		Size: 99.5 MB (99473761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a24b6c203f894d105b6c0b45cd66906d3eb52d876104bdc7bd64b1a7c96a342`  
		Last Modified: Tue, 14 Apr 2020 22:28:03 GMT  
		Size: 54.0 KB (54047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
