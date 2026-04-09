## `eclipse-temurin:26_35-jdk-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:668167cd82d99860fc3e15f94689a17ede78c05a47ff02685cdbe74ed625db21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32522; amd64

### `eclipse-temurin:26_35-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.32522; amd64

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
