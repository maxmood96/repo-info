## `openjdk:23-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:ec4b2c0f0a654970a614002b415b0f26eb12b2df10284f621e5b24520553b8f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `openjdk:23-jdk-nanoserver-1809` - windows version 10.0.17763.5936; amd64

```console
$ docker pull openjdk@sha256:57910f9b548096db368f5291184cb232f895e8c20c4256a2512f3424a1bc9404
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.4 MB (366382578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d87a2847c817c311cb494414811dea9d989428ec568e08d3575fd3500bff2c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Tue, 02 Jul 2024 03:14:27 GMT
SHELL [cmd /s /c]
# Tue, 02 Jul 2024 03:14:28 GMT
ENV JAVA_HOME=C:\openjdk-23
# Tue, 02 Jul 2024 03:14:28 GMT
USER ContainerAdministrator
# Tue, 02 Jul 2024 03:14:39 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 02 Jul 2024 03:14:40 GMT
USER ContainerUser
# Tue, 02 Jul 2024 03:14:40 GMT
ENV JAVA_VERSION=23-ea+29
# Tue, 02 Jul 2024 03:14:48 GMT
COPY dir:d500194483fdc1df3f4ca3e79e689897b4f762b7353730d4badae840cbb068ae in C:\openjdk-23 
# Tue, 02 Jul 2024 03:15:01 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 02 Jul 2024 03:15:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4f703ea968d7f7434cf61e5d835cb3c507a6364ff8c7b3b96b73391b22115615`  
		Last Modified: Tue, 11 Jun 2024 20:35:02 GMT  
		Size: 155.0 MB (155033193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b406fb127e8e425ec99baef6196f7a61d13cece87df2ac1849dd20e1ff9127b`  
		Last Modified: Tue, 02 Jul 2024 03:15:06 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7cd64563a324f4fc0328b28b05a6e8f8c60760672b7d28f371fc24aaa3b8b3`  
		Last Modified: Tue, 02 Jul 2024 03:15:05 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c805a7ac2d9409e07ad350a3c0b7a1188fea84ab3013a8e5c852563773740576`  
		Last Modified: Tue, 02 Jul 2024 03:15:05 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb77b3308666d79e7f774e2c88d8c8bc23adc7c323bc398fb0413de36370af4d`  
		Last Modified: Tue, 02 Jul 2024 03:15:05 GMT  
		Size: 67.8 KB (67782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d263a56f22e1f25ff6ab725e78269c0325d0544da3517e65cbe71b0b8057755f`  
		Last Modified: Tue, 02 Jul 2024 03:15:04 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:606130ba9d0baa488e1add40b5060c09ec1645883357af6e8b7e0e42ec3a6f81`  
		Last Modified: Tue, 02 Jul 2024 03:15:04 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f12e1de0378d22d0b055fe3e18648c9e7efa7bc2c0bbd96d9ce00abbeef460b`  
		Last Modified: Tue, 02 Jul 2024 03:15:15 GMT  
		Size: 206.1 MB (206057513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd99fa1540d891e5abdf151ecb94e6883131d2215956a650a314e0eb69638b17`  
		Last Modified: Tue, 02 Jul 2024 03:15:05 GMT  
		Size: 5.2 MB (5217820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f6f14aa569ec990419ebaade37e01716c499b27f424df2054ec0602b4a64fc`  
		Last Modified: Tue, 02 Jul 2024 03:15:04 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
