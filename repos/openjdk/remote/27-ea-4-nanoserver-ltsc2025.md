## `openjdk:27-ea-4-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:21abb98b3884fe44f3b9e3a0f87ad202838419a508f1ec98f81884e5a3d46c73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `openjdk:27-ea-4-nanoserver-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull openjdk@sha256:9310d667c82c5e908769f1a9c3a8e13f0829da6e3e6b881d968dcf2bdfd9b05a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.2 MB (423178025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7420c5b3487194b43fb3ced9bcd5d0a64c5c7efd9fcbb67b2a46e19e4296a5f4`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 11 Jan 2026 06:15:10 GMT
RUN Apply image 10.0.26100.32230
# Tue, 13 Jan 2026 23:38:54 GMT
SHELL [cmd /s /c]
# Tue, 13 Jan 2026 23:41:14 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 13 Jan 2026 23:41:15 GMT
USER ContainerAdministrator
# Tue, 13 Jan 2026 23:41:16 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 13 Jan 2026 23:41:17 GMT
USER ContainerUser
# Tue, 13 Jan 2026 23:41:17 GMT
ENV JAVA_VERSION=27-ea+4
# Tue, 13 Jan 2026 23:41:29 GMT
COPY dir:55417311536b64386669c9f543375752cfd39486cb0c7d8403a74e4cd382a3c4 in C:\openjdk-27 
# Tue, 13 Jan 2026 23:41:34 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 13 Jan 2026 23:41:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d441ba4c6d25e3ab6a1e3ce5360fd1d1214e97975f1e40b10c0ccb55dc46ad22`  
		Last Modified: Tue, 13 Jan 2026 22:42:10 GMT  
		Size: 199.1 MB (199076547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c3018f35c73af59a36350615c430cd199174009bb767471c37deb2372b9478`  
		Last Modified: Tue, 13 Jan 2026 23:40:03 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b920187cb8760844464774283ff95fcf01301f7e3cc842892daeb2624b47ca27`  
		Last Modified: Tue, 13 Jan 2026 23:42:01 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691147dfcbe8301285335d769a1c70061cceb5574c03d46c3ab767f5d498c941`  
		Last Modified: Tue, 13 Jan 2026 23:42:01 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958751a94a73dd3a4d8731f93cff6e654960d10ac00c51cacab3e4be530a81ca`  
		Last Modified: Tue, 13 Jan 2026 23:42:01 GMT  
		Size: 72.2 KB (72199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a88b91c95110895ef47b5b5357ba8138bb4ee2571fcefa1d0d038ce1823db0f`  
		Last Modified: Tue, 13 Jan 2026 23:41:39 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66729df7c3e3821bbc23c376a0cd578d423f364fbfd31b86e39c18a743fb3fb2`  
		Last Modified: Tue, 13 Jan 2026 23:42:01 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71385906499c269e4caa262136395ae2b9e4d9262aa199914f1c8d2ff4ae80ac`  
		Last Modified: Tue, 13 Jan 2026 23:41:53 GMT  
		Size: 223.9 MB (223909637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edb166faacfb089411f8bbd22ff901598b1763d3841af642a03c1b1865156344`  
		Last Modified: Tue, 13 Jan 2026 23:41:39 GMT  
		Size: 113.2 KB (113202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb46690aadd5cf416cde10a120b43794dd313c6f1206a1af27bd326a07537fa`  
		Last Modified: Tue, 13 Jan 2026 23:42:01 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
