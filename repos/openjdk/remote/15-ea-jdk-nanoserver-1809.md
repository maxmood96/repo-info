## `openjdk:15-ea-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:bac559b2495a33ad169c01ebc82ad5429a232305572dbcbf3d33558b58428e07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1040; amd64

### `openjdk:15-ea-jdk-nanoserver-1809` - windows version 10.0.17763.1040; amd64

```console
$ docker pull openjdk@sha256:6759f77290c707cbf46631cbede287e6fe5116972b5b09c3aa1d9ce94a8f6d23
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297787428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dc880f9610fbe9eadec878e91b81e204c75a210dd81c529016a5ab2e7415878`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 16 Feb 2020 01:25:57 GMT
RUN Apply image 1809-amd64
# Thu, 20 Feb 2020 02:05:49 GMT
SHELL [cmd /s /c]
# Thu, 20 Feb 2020 02:05:51 GMT
ENV JAVA_HOME=C:\openjdk-15
# Thu, 20 Feb 2020 02:05:53 GMT
USER ContainerAdministrator
# Thu, 20 Feb 2020 02:06:20 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Thu, 20 Feb 2020 02:06:21 GMT
USER ContainerUser
# Fri, 21 Feb 2020 00:29:14 GMT
ENV JAVA_VERSION=15-ea+11
# Fri, 21 Feb 2020 00:30:10 GMT
COPY dir:a5b0f2f60c1f21129144eeca247140764e8957c1c61c3413dbb5958e01f276ce in C:\openjdk-15 
# Fri, 21 Feb 2020 00:30:33 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Fri, 21 Feb 2020 00:30:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a35da61c356213336e646756218539950461ff2bf096badf307a23add6e70053`  
		Size: 101.1 MB (101145811 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:141e7d00d8743fe3d0c951c1f46529a11bff09056f891a37a603bbde2491228e`  
		Last Modified: Thu, 20 Feb 2020 03:06:23 GMT  
		Size: 923.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02e7d5fabfd691f6f12b0f526dd517b21dba9a0d86160f5a031a9915b3cebbe`  
		Last Modified: Thu, 20 Feb 2020 03:06:22 GMT  
		Size: 915.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:797ce79628a34cd492d0a7deb2d4a028a4732ed656ba28675127d0d8ee1c7976`  
		Last Modified: Thu, 20 Feb 2020 03:06:22 GMT  
		Size: 935.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83840f341da670f768c8e90bfab9ea570671d70d0aedcf3fc430325628c790b7`  
		Last Modified: Thu, 20 Feb 2020 03:06:22 GMT  
		Size: 73.1 KB (73055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60136e35e1da9de137c41ef1a897b216fce1e005981f3ad3191275b74f94de9c`  
		Last Modified: Thu, 20 Feb 2020 03:06:19 GMT  
		Size: 928.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2333435bcd8618643538eeff3ac197e9db77e521620bc2d6f8ee51da573373c`  
		Last Modified: Fri, 21 Feb 2020 00:37:50 GMT  
		Size: 921.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab8e0e27aeb92ab69d939adacba9746577e98413298cfb5fbc0acc469f87b50e`  
		Last Modified: Fri, 21 Feb 2020 00:38:18 GMT  
		Size: 193.1 MB (193110089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64dc3c8911c406f66bda6c1c4a5a435fd71f02bc56a769eb1ef86cde84f643a0`  
		Last Modified: Fri, 21 Feb 2020 00:37:51 GMT  
		Size: 3.5 MB (3452925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b774c5c4d60a8d89150f87727a8543817eaa8bada35130a6e250caad6a49ee66`  
		Last Modified: Fri, 21 Feb 2020 00:37:50 GMT  
		Size: 926.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
