## `openjdk:26-ea-17-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:2fa42d731f526965289a55b4a68383689b456118f45d57b1ba096994677feb97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `openjdk:26-ea-17-nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull openjdk@sha256:eb9da50056a5c0f2f2faf3a62ac52b3aeb6a23977946420b7d63ccdecbc83dfc
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.1 MB (344058230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:993fcbccbd5b8a3b474214b7bbaf91ac08fe645f3365d7c7c3e3bcdcfce08bcb`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Fri, 26 Sep 2025 22:47:03 GMT
SHELL [cmd /s /c]
# Fri, 26 Sep 2025 22:47:04 GMT
ENV JAVA_HOME=C:\openjdk-26
# Fri, 26 Sep 2025 22:47:05 GMT
USER ContainerAdministrator
# Fri, 26 Sep 2025 22:47:16 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 26 Sep 2025 22:47:17 GMT
USER ContainerUser
# Fri, 26 Sep 2025 22:47:18 GMT
ENV JAVA_VERSION=26-ea+17
# Fri, 26 Sep 2025 22:48:14 GMT
COPY dir:00243416b2d1eb1675fd4c082ccd61e2c80377000367c1dfb1f71202ed6aabd5 in C:\openjdk-26 
# Fri, 26 Sep 2025 22:48:23 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 26 Sep 2025 22:48:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46340b8979f289bcaf285ece02bed3ec2854bfa7c2ed4832db6c4aa2305f9ed0`  
		Last Modified: Fri, 26 Sep 2025 22:48:55 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c129981d58881324998b0e4847cee578c3bd437b03960324b76ff46f24e7f3`  
		Last Modified: Fri, 26 Sep 2025 22:48:55 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0cab07eed729b42d1000ca66b8393917c8a57182dda802c628ed7423f191d21`  
		Last Modified: Fri, 26 Sep 2025 22:48:55 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c935ed3274972357166c602592471dd8551c916e641baa7b95d17fdaa17bd6e7`  
		Last Modified: Fri, 26 Sep 2025 22:48:55 GMT  
		Size: 82.9 KB (82875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aafb8cf92d35cfd6d65a646ab0c3bdbc458e2a5fd0b7b2ddc395ca04cd5911fe`  
		Last Modified: Fri, 26 Sep 2025 22:48:55 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e23edf0f483301e5359c2758a43a7900f5d075941f50eae4678814bdd3b905a`  
		Last Modified: Fri, 26 Sep 2025 22:48:55 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:019399d7d29937e73b72c0dee877fbac772669d5b10ec4b79af9ab8415ac822b`  
		Last Modified: Sat, 27 Sep 2025 00:24:12 GMT  
		Size: 221.1 MB (221123424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d90b2b14d405a3fdb5c9b33abb8b82326fec747a4196d0bcad23bc705f60740`  
		Last Modified: Fri, 26 Sep 2025 22:48:55 GMT  
		Size: 125.7 KB (125705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103ea98e12ff56769b07c025fbaac2ce83e072bf845c23c9290db67c0eb14e27`  
		Last Modified: Fri, 26 Sep 2025 22:48:55 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
