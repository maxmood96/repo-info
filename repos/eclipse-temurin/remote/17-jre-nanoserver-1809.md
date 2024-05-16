## `eclipse-temurin:17-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:aedb883ba738a19f7cedc112d3f16f0dd1e995800f4865fff690fbc5012ccb7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `eclipse-temurin:17-jre-nanoserver-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull eclipse-temurin@sha256:b777706c9b00447a374fcfd09edcfa8c356a778b46914ad0162101ce8c17def8
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.5 MB (201450273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dcf55600b6071db43a0f34a344d671053eacb76cd2977b2511ddbb795bb33ec`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Wed, 15 May 2024 19:42:01 GMT
SHELL [cmd /s /c]
# Wed, 15 May 2024 20:04:34 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Wed, 15 May 2024 20:04:35 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 15 May 2024 20:04:35 GMT
USER ContainerAdministrator
# Wed, 15 May 2024 20:04:45 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 May 2024 20:04:45 GMT
USER ContainerUser
# Wed, 15 May 2024 20:10:14 GMT
COPY dir:a78f43753c24e3e0717a998b116850ca8c6149210b4cd2529d3fd312f361a7bd in C:\openjdk-17 
# Wed, 15 May 2024 20:10:26 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6a511fea8e874efc08e5058ac5b12b6433c36ba6570862a619dd80cfb0e190`  
		Last Modified: Wed, 15 May 2024 20:45:52 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4da49c4b8012eb26cf69c376d99dd8f1cb1e3ca715beb7254db10e9807c4fc9f`  
		Last Modified: Wed, 15 May 2024 20:51:10 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80045ad85cfa6eab06f555a848b724489fc2aafccc21d8dc6ac3b9201980ff7c`  
		Last Modified: Wed, 15 May 2024 20:51:09 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d438955ec9000bd485218afe17f2d42614a0ce5ef330651ce4c2940273c187`  
		Last Modified: Wed, 15 May 2024 20:51:09 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c63495db38074e2cb31d8afcccbf3f3588fd25c298c3f82cfce36b2deaf2b39`  
		Last Modified: Wed, 15 May 2024 20:51:07 GMT  
		Size: 68.9 KB (68939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49bc8a43e83602c3561ce59837b5348440e9d183f9f759da75dcee6267db095`  
		Last Modified: Wed, 15 May 2024 20:51:07 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89e67ef9789fd22c907f9df2724fffd60e76a09953d28e6c070d03b43ba4e7c`  
		Last Modified: Wed, 15 May 2024 20:52:22 GMT  
		Size: 43.5 MB (43453678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00ec2f1cdc870b6a175a509c474c9c8c69abf2a1b1c9737c8bcc8d8ae4966b05`  
		Last Modified: Wed, 15 May 2024 20:52:15 GMT  
		Size: 3.0 MB (2980469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
