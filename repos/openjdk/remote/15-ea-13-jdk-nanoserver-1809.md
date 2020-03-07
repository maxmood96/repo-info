## `openjdk:15-ea-13-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:4214bd37d87d0e5af5d66c394412cd874261ccd85a4efd01d6517796375a6d02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1040; amd64

### `openjdk:15-ea-13-jdk-nanoserver-1809` - windows version 10.0.17763.1040; amd64

```console
$ docker pull openjdk@sha256:4d238414e093f6510b3b8f844afc72ea161080b417729dc849d9179d03349eef
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.0 MB (297966232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e58b6a4aaababfb387a1f891da732a1bd5869a004566eabe0304dbcd3cbfee7e`
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
# Fri, 06 Mar 2020 22:20:25 GMT
ENV JAVA_VERSION=15-ea+13
# Fri, 06 Mar 2020 22:21:23 GMT
COPY dir:381680c6d29a098adbd773948a72f80f540fcd0de924f6456602295be249872c in C:\openjdk-15 
# Fri, 06 Mar 2020 22:21:59 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Fri, 06 Mar 2020 22:22:00 GMT
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
	-	`sha256:e58cff8ce3982aa86df73701780ef80a0b366788f643a026a3fdc6b28c95d8ff`  
		Last Modified: Fri, 06 Mar 2020 22:31:36 GMT  
		Size: 931.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c4991c02c91a0cdabc60c457b88cb624c795caf9c4b6661a2f7f9e63c2cfdd`  
		Last Modified: Fri, 06 Mar 2020 22:32:22 GMT  
		Size: 193.3 MB (193314049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200766bd58e0f4304404de7693aa4327001ff44465f47b79e81093db9ae1e9c5`  
		Last Modified: Fri, 06 Mar 2020 22:31:36 GMT  
		Size: 3.4 MB (3427730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e62f1ed45d203a0e9cb4f78824e93da20266bf0e5a74f6538035a85a5d4fd53`  
		Last Modified: Fri, 06 Mar 2020 22:31:36 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
