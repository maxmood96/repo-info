## `eclipse-temurin:26-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:8f17ef5a329054a07b32746cb7af50c0eb73e6919c87f3455300623138c7c761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32522; amd64
	-	windows version 10.0.20348.4893; amd64

### `eclipse-temurin:26-nanoserver` - windows version 10.0.26100.32522; amd64

```console
$ docker pull eclipse-temurin@sha256:31b7eeaffccd9b5a3ce79f2e315c1b30113bf0f23594438abce74ea019bd5068
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.9 MB (340896452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2933b1a33b335d79b02babf3a094195c5fcd2ed2e20c346e9c3af5c41466166`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Mar 2026 01:45:55 GMT
RUN Apply image 10.0.26100.32522
# Wed, 08 Apr 2026 18:17:32 GMT
SHELL [cmd /s /c]
# Wed, 08 Apr 2026 18:17:35 GMT
ENV JAVA_VERSION=jdk-26+35
# Wed, 08 Apr 2026 18:17:36 GMT
ENV JAVA_HOME=C:\openjdk-26
# Wed, 08 Apr 2026 18:17:36 GMT
USER ContainerAdministrator
# Wed, 08 Apr 2026 18:17:52 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 08 Apr 2026 18:17:53 GMT
USER ContainerUser
# Wed, 08 Apr 2026 18:18:50 GMT
COPY dir:8f93d89558d485d03b81034182d43f2557754598b0731c760b32ca0af365b3c1 in C:\openjdk-26 
# Wed, 08 Apr 2026 18:19:01 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 08 Apr 2026 18:19:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:06fab7822816d5f43d6835d07ac8db280fdf81384187f36d8dc43bbb7064a76d`  
		Last Modified: Tue, 10 Mar 2026 20:41:46 GMT  
		Size: 199.4 MB (199409325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23e6be6267c9b5e89ad64f586098baf3618437e6b1dcda1bfb5cf8d6b28e957`  
		Last Modified: Wed, 08 Apr 2026 18:19:08 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:051372f4258c304b34a40048c842be5a324203427605a8145f550e1d6294183f`  
		Last Modified: Wed, 08 Apr 2026 18:19:08 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f77b1c40fbdeaeb43a7dda967b4ba2dd3233eb75dc7248a7f91e45a2a9691909`  
		Last Modified: Wed, 08 Apr 2026 18:19:08 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda6594e13640169ee0115a9ec2ae86d9a89e3bebce63ff1c27bf8b3bcb523d8`  
		Last Modified: Wed, 08 Apr 2026 18:19:08 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a494ef9b9fda1f1f2e1358310bdf3dd1c35cf40dec5f92fd05b41f89cd6069b`  
		Last Modified: Wed, 08 Apr 2026 18:19:06 GMT  
		Size: 70.8 KB (70804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d01633c8ce33baeea192b4a60cf3d82ece7ba3824d5043d2822fbbf850ce4b6`  
		Last Modified: Wed, 08 Apr 2026 18:19:06 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d551611456cd2b383b668cf446bb4882d64db0e0e2a06adf73739dbfc66f190`  
		Last Modified: Wed, 08 Apr 2026 18:19:18 GMT  
		Size: 141.3 MB (141307225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c8fc130d1613d1746b5df4d9156419bb8ea58b0016469e904d13430d5b7932e`  
		Last Modified: Wed, 08 Apr 2026 18:19:06 GMT  
		Size: 102.6 KB (102629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feedd27f9f2f78ae49c98ef0ab5c903b3cb68dd1769af54ca18d3f259ed2c925`  
		Last Modified: Wed, 08 Apr 2026 18:19:06 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:26-nanoserver` - windows version 10.0.20348.4893; amd64

```console
$ docker pull eclipse-temurin@sha256:6f7200e3b9a539f18df0e1cb5b32a37c5eee01e15f4b7f36bb7a85040a4f176b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.2 MB (268174439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fa9f6c983f786c40a98fe54799a3a510a2a01cadd8e58f1c475fa034ec10a0d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Wed, 08 Apr 2026 18:16:42 GMT
SHELL [cmd /s /c]
# Wed, 08 Apr 2026 18:16:45 GMT
ENV JAVA_VERSION=jdk-26+35
# Wed, 08 Apr 2026 18:16:46 GMT
ENV JAVA_HOME=C:\openjdk-26
# Wed, 08 Apr 2026 18:16:47 GMT
USER ContainerAdministrator
# Wed, 08 Apr 2026 18:17:06 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 08 Apr 2026 18:17:08 GMT
USER ContainerUser
# Wed, 08 Apr 2026 18:18:17 GMT
COPY dir:8f93d89558d485d03b81034182d43f2557754598b0731c760b32ca0af365b3c1 in C:\openjdk-26 
# Wed, 08 Apr 2026 18:18:29 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 08 Apr 2026 18:18:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c52e8dc7185acdf335f3e66a4717a90b37648943d2b2a62e58ac7fb994854cb`  
		Last Modified: Wed, 08 Apr 2026 18:18:36 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c981a6f75f9ed56a17b30f4ad0d927abacfb8b22b4f1afb6524e8ea30c026316`  
		Last Modified: Wed, 08 Apr 2026 18:18:36 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8619d6b7f5e7af3351c34b725959bf0183e9058375dea5a8142b3207ab8d4880`  
		Last Modified: Wed, 08 Apr 2026 18:18:36 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b17064cde33ad8eb5a19f7de5af5b266a60638019c915532c8865f9724a7a57`  
		Last Modified: Wed, 08 Apr 2026 18:18:35 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7b982e7e2760363f18c3dead1835ea7a7e60fd85e7256482c93a57c01b81f38`  
		Last Modified: Wed, 08 Apr 2026 18:18:34 GMT  
		Size: 84.9 KB (84946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d31be68e33cfbc0cdd9001fcd3a3b8bf53e62a516e7ab6e2f06cc929a078fa`  
		Last Modified: Wed, 08 Apr 2026 18:18:34 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd02bf72fcd7253c32cdb948b464dff67794a8edecc86f81e9f29724d0116e77`  
		Last Modified: Wed, 08 Apr 2026 18:18:46 GMT  
		Size: 141.3 MB (141306852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d438d906dabcabd27b8261eaddce408a3323e5fb441fa609509d669adc8c00ea`  
		Last Modified: Wed, 08 Apr 2026 18:18:34 GMT  
		Size: 125.8 KB (125753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b134feb2812a9cbcefb5a3f9e1048d60c96256ab6e978fea45a0fab7818269`  
		Last Modified: Wed, 08 Apr 2026 18:18:34 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
