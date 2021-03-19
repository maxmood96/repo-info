## `openjdk:jdk-nanoserver`

```console
$ docker pull openjdk@sha256:5d2914f18689f4531ee9b3a82548fdbbcb98dc0516c019ea5e730d4e2a92caff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1817; amd64

### `openjdk:jdk-nanoserver` - windows version 10.0.17763.1817; amd64

```console
$ docker pull openjdk@sha256:6eb9dbc49b9debd4372895f81b96268697e9aaaddb45a936df83d0b164042e77
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.2 MB (285162188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d889e838de5fbfc6bfb0caa818004cb927e2c75ee9f96e31b904843b328fa091`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 26 Feb 2021 16:47:31 GMT
RUN Apply image 1809-amd64
# Wed, 10 Mar 2021 17:50:47 GMT
SHELL [cmd /s /c]
# Wed, 10 Mar 2021 17:57:58 GMT
ENV JAVA_HOME=C:\openjdk-16
# Wed, 10 Mar 2021 17:57:59 GMT
USER ContainerAdministrator
# Wed, 10 Mar 2021 17:58:11 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 10 Mar 2021 17:58:12 GMT
USER ContainerUser
# Wed, 10 Mar 2021 17:58:13 GMT
ENV JAVA_VERSION=16
# Wed, 10 Mar 2021 17:58:30 GMT
COPY dir:03c380a356e8b0fa2d413bbd7f8427b40b2c6808fd016e7b77d87b6b5da6487b in C:\openjdk-16 
# Wed, 10 Mar 2021 17:58:50 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 10 Mar 2021 17:58:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a11c4ca8f1ba16b6e1395d4523be2215bd0871c2e3e4695b9f2b87bd7472be52`  
		Size: 101.4 MB (101389964 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b1146273d9b624ee892dfcbb3c753523f09f79536a16d63b711cb0027825374a`  
		Last Modified: Wed, 10 Mar 2021 18:33:51 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8ddb8991f773b01b6cd644e80eddc1e60d6e9b2ddec000d4f57728e0309e285`  
		Last Modified: Wed, 10 Mar 2021 18:36:34 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea50aaa0500230793665b7f9234cdc8bb7ac85d516e17417813293c454366fc`  
		Last Modified: Wed, 10 Mar 2021 18:36:34 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a131db452c0ac7657c39ee6d34cdd9901d71eb160682edca13d912db56d55c`  
		Last Modified: Wed, 10 Mar 2021 18:36:35 GMT  
		Size: 67.5 KB (67462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1184ed8e4354d579d8583fbd9cf778a49aca1d830af33c0372f57fdf23a3a1e1`  
		Last Modified: Wed, 10 Mar 2021 18:36:31 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d13ffae2cfb6bad786ff246dbde2ff50c00e75c22caa0f02dcefa763c47492`  
		Last Modified: Wed, 10 Mar 2021 18:36:32 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e23167269ef10c095d2249982da45930672919130340b53c75983fa0a28f5899`  
		Last Modified: Wed, 10 Mar 2021 18:36:52 GMT  
		Size: 180.0 MB (180032119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c31f7f608167a0c00011518a0b8b3d20ba940533184e54d841c2d03828b099`  
		Last Modified: Wed, 10 Mar 2021 18:36:33 GMT  
		Size: 3.7 MB (3665755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57cf9d05cd7e0405f7b7dd820f778c8e7a9dd7cbdd8bd796e626c5cb79543011`  
		Last Modified: Wed, 10 Mar 2021 18:36:31 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
