## `eclipse-temurin:11-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:2f7fccb56020ffbf233d51e83d80a5233975673d9041e02a1179fc4e99832610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4645; amd64

### `eclipse-temurin:11-jdk-nanoserver-1809` - windows version 10.0.17763.4645; amd64

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
