## `eclipse-temurin:11-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:4d5638df990072005bfff50a2e066d0b2f7e7dd1ec92ce9d83cf1cece53cfecf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1850; amd64
	-	windows version 10.0.17763.4645; amd64

### `eclipse-temurin:11-nanoserver` - windows version 10.0.20348.1850; amd64

```console
$ docker pull eclipse-temurin@sha256:94b81aa67c4a1edea1d911bfeaf3d577fb0aeb19dd2ae1310c998080b36c686a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.3 MB (313311638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec359935d859ac9e0154e159115755c65f3836d74aeb99a41b770635f7a9373`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jul 2023 21:00:40 GMT
RUN Apply image 10.0.20348.1850
# Thu, 13 Jul 2023 22:10:51 GMT
SHELL [cmd /s /c]
# Wed, 26 Jul 2023 00:27:24 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Wed, 26 Jul 2023 00:27:25 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 26 Jul 2023 00:27:25 GMT
USER ContainerAdministrator
# Wed, 26 Jul 2023 00:27:35 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 26 Jul 2023 00:27:36 GMT
USER ContainerUser
# Wed, 26 Jul 2023 00:27:50 GMT
COPY dir:0494f0c3004dc0f4e40e3f6c0c6e0f2ac35120ffc9906421c49b5c62e99eee70 in C:\openjdk-11 
# Wed, 26 Jul 2023 00:28:04 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 26 Jul 2023 00:28:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cc0a26bd90fcc4d863317c36d7ffec77a0a82a905697204d4dcbc76ec13b3920`  
		Last Modified: Tue, 11 Jul 2023 20:10:45 GMT  
		Size: 120.1 MB (120056465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb11750b624a775aa3c21a13406dfc54458855b8684e21efba5bbb9b27ee0b12`  
		Last Modified: Thu, 13 Jul 2023 22:28:35 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f6fc7da52cd85c46d7cc9f4b0fe25d75d7e3cfcaa2dfc65ebac000529276d57`  
		Last Modified: Wed, 26 Jul 2023 00:34:25 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:835a4cdfb9b1958fb13255c78147171f9d8747a6fa5a2719e6bfc9da55fd9f88`  
		Last Modified: Wed, 26 Jul 2023 00:34:25 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46453ada3c9c1d0d1c66cf1fc4b47ec80b2e70a8efc7bc57d3032202abebf733`  
		Last Modified: Wed, 26 Jul 2023 00:34:25 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:075d5243707d8e6924ce011650fd2ae3e47c22405846bcbf95e4307ed0f9da5e`  
		Last Modified: Wed, 26 Jul 2023 00:34:24 GMT  
		Size: 80.2 KB (80184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b18907ca6b61aec2fab8b9c92eba73443a66ae1c03a167e26d6be34a7ba63020`  
		Last Modified: Wed, 26 Jul 2023 00:34:23 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baccff07c79e264703937b14194e48bab60b8cca253468921fd0d65aad34b1c2`  
		Last Modified: Wed, 26 Jul 2023 00:34:43 GMT  
		Size: 193.1 MB (193107061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbcd3d0b8d3f3c4914a5bee882ce0b2f241324d5d3ee4ca699fa3b79ec2e23c2`  
		Last Modified: Wed, 26 Jul 2023 00:34:23 GMT  
		Size: 61.0 KB (61009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3611dd2d2e0c0ec88f5265990bb2e6d608743e6a81ccf7635148f5a85397c748`  
		Last Modified: Wed, 26 Jul 2023 00:34:23 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-nanoserver` - windows version 10.0.17763.4645; amd64

```console
$ docker pull eclipse-temurin@sha256:0847d8dd2501ad041efde6697d278a24f29955adf9c50a37f7e275e8b4421394
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.6 MB (297643579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ddbb1e425417284b3b0c758706b3d9a1888ed1ddd0422f384306fab861318fa`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jul 2023 07:42:59 GMT
RUN Apply image 10.0.17763.4645
# Thu, 13 Jul 2023 21:36:32 GMT
SHELL [cmd /s /c]
# Wed, 26 Jul 2023 00:20:55 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Wed, 26 Jul 2023 00:20:55 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 26 Jul 2023 00:20:56 GMT
USER ContainerAdministrator
# Wed, 26 Jul 2023 00:21:05 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 26 Jul 2023 00:21:06 GMT
USER ContainerUser
# Wed, 26 Jul 2023 00:21:21 GMT
COPY dir:0494f0c3004dc0f4e40e3f6c0c6e0f2ac35120ffc9906421c49b5c62e99eee70 in C:\openjdk-11 
# Wed, 26 Jul 2023 00:21:33 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 26 Jul 2023 00:21:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5c5b06ba65934bcf850a1a54ecf4b3da34d3e6d6c8e90dbc897719c3ea377c8a`  
		Last Modified: Tue, 11 Jul 2023 17:31:37 GMT  
		Size: 104.4 MB (104408241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f13c473988daf5951866dd9b290bd6417227c1d7df6e811cfe11438d033a1eba`  
		Last Modified: Thu, 13 Jul 2023 22:19:06 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf417bf3467803e12fc9a31b5e6497d2433421e1fb614aac2984cf758f5b24b`  
		Last Modified: Wed, 26 Jul 2023 00:32:45 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8192126e41b0371c9ae3c94a72cf1c2d3e7d560a0c53ceaa0b4909e58ec91515`  
		Last Modified: Wed, 26 Jul 2023 00:32:45 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77854ff76c4d4dfbd3606d0a022401e89a7022cb27b1f8bfcc6d01883b30c37`  
		Last Modified: Wed, 26 Jul 2023 00:32:45 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd03a2c299188954a07fc8e131eafc52f6b71166fc234d29f4ee37a48e0c882b`  
		Last Modified: Wed, 26 Jul 2023 00:32:43 GMT  
		Size: 71.3 KB (71337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce4ec240d039cba153cd22b6d0835e907ed1b0f578b82283a6610e6a6144c91e`  
		Last Modified: Wed, 26 Jul 2023 00:32:43 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:521d435eeab1939fdd236fc1b27a12f85c7e7b877646e1dfacef858ab56827da`  
		Last Modified: Wed, 26 Jul 2023 00:33:02 GMT  
		Size: 193.1 MB (193106766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed558b2d70cc89efa6e102c62800140edcb9fb3b26d02b4688954ebac035696`  
		Last Modified: Wed, 26 Jul 2023 00:32:43 GMT  
		Size: 50.3 KB (50310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01f8e0fc38921aefe371ed8ac159125a81a84ef06530f11e4a83128460f7c19d`  
		Last Modified: Wed, 26 Jul 2023 00:32:43 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
