## `openjdk:26-ea-nanoserver`

```console
$ docker pull openjdk@sha256:591cab6b93bc0a2deb39f5df7d1cd9f077859ebbebd4b21e5391546c99f1d7f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `openjdk:26-ea-nanoserver` - windows version 10.0.26100.32230; amd64

```console
$ docker pull openjdk@sha256:1dd78a4e768f2e739d4e5a95996c71f99ad4f09da860a67953d6b95ad39ca29a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.1 MB (423112370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7deafeca8be97a36ede7e3552eadee58d86e82fd3206c3b86ab9eafd5a0febba`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 11 Jan 2026 06:15:10 GMT
RUN Apply image 10.0.26100.32230
# Tue, 13 Jan 2026 23:39:23 GMT
SHELL [cmd /s /c]
# Tue, 13 Jan 2026 23:41:07 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 13 Jan 2026 23:41:07 GMT
USER ContainerAdministrator
# Tue, 13 Jan 2026 23:41:09 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 13 Jan 2026 23:41:09 GMT
USER ContainerUser
# Tue, 13 Jan 2026 23:41:10 GMT
ENV JAVA_VERSION=26-ea+30
# Tue, 13 Jan 2026 23:41:22 GMT
COPY dir:e07e90760755fda5775e159516136ae7ac9e724b6c3d3e98906408d196af4b98 in C:\openjdk-26 
# Tue, 13 Jan 2026 23:41:27 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 13 Jan 2026 23:41:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d441ba4c6d25e3ab6a1e3ce5360fd1d1214e97975f1e40b10c0ccb55dc46ad22`  
		Last Modified: Tue, 13 Jan 2026 22:42:56 GMT  
		Size: 199.1 MB (199076547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:449a8f38121ad9ab7bb32fd54119825e5f6c3a13152940fa400e7a44dd22a6bf`  
		Last Modified: Tue, 13 Jan 2026 23:39:55 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ced718e74d685b725f4052d135240c41b555fd8824695a48f9035a4858c1ed`  
		Last Modified: Tue, 13 Jan 2026 23:41:33 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff84be404aa57e42fe8a76f6706d4284542d81c9ed22b5b5dde873d94ccd6831`  
		Last Modified: Tue, 13 Jan 2026 23:41:55 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60edc2b0d87181243db16220d8d27184a5803d8b42b355e056e3e5eea50fad5`  
		Last Modified: Tue, 13 Jan 2026 23:41:33 GMT  
		Size: 72.0 KB (71951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:413694019043a62fc6686df5b55296fe526d233c162e29f99f909beb4ff1f4d4`  
		Last Modified: Tue, 13 Jan 2026 23:41:56 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda0ec99d44ba1cdb0ccd89ac69e1e0e1a0875135b298c08256625493382f40e`  
		Last Modified: Tue, 13 Jan 2026 23:41:55 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d19551296afbace182d99da87c8a5bce8885636e533418f8716a5c2f06d33bf`  
		Last Modified: Tue, 13 Jan 2026 23:42:45 GMT  
		Size: 223.8 MB (223833233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d75a536adf46f39f39e08b47022e7b5c548dc4540ae37fc2e91d7827bdcea2`  
		Last Modified: Tue, 13 Jan 2026 23:41:55 GMT  
		Size: 124.2 KB (124197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9280b49445ed1411162e1e4385040239f63ec475ca48fa2b6f449c2e1ad461fb`  
		Last Modified: Tue, 13 Jan 2026 23:41:31 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:26-ea-nanoserver` - windows version 10.0.20348.4648; amd64

```console
$ docker pull openjdk@sha256:dc0f1d317a5c460411fe7d12f9aaa570f73910442763fa517c5b746f46d5162b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.8 MB (350757171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0acea2c74cc1fe097dff7968d4bda178d7c0bea3b27ed3d2ef331f86517d3596`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Tue, 13 Jan 2026 23:37:24 GMT
SHELL [cmd /s /c]
# Tue, 13 Jan 2026 23:37:25 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 13 Jan 2026 23:37:25 GMT
USER ContainerAdministrator
# Tue, 13 Jan 2026 23:37:27 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 13 Jan 2026 23:37:27 GMT
USER ContainerUser
# Tue, 13 Jan 2026 23:37:28 GMT
ENV JAVA_VERSION=26-ea+30
# Tue, 13 Jan 2026 23:38:14 GMT
COPY dir:e07e90760755fda5775e159516136ae7ac9e724b6c3d3e98906408d196af4b98 in C:\openjdk-26 
# Tue, 13 Jan 2026 23:38:22 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 13 Jan 2026 23:38:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98454f6897609d2c5809bd23acc5ca6982642201b45e7e63d94baee989cf1f4d`  
		Last Modified: Tue, 13 Jan 2026 23:38:51 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dbc5145bfeeaef4b75d626dd071370cddfd0de53084147b7c478b7edaf81a64`  
		Last Modified: Tue, 13 Jan 2026 23:38:51 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25c38baea5a349f02799983d2d3c3a605358e950529c373bbf8ff1aae9a60f1f`  
		Last Modified: Tue, 13 Jan 2026 23:38:51 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8c739fc37583fcf99aa4fe8c71c059ed730e9bca70c5cad5193c485f019c59`  
		Last Modified: Tue, 13 Jan 2026 23:38:30 GMT  
		Size: 77.5 KB (77451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15b6e12d342b4b568d88d62b97b754f1d3d33b3e963c36ea5e84221a6d4a4b73`  
		Last Modified: Tue, 13 Jan 2026 23:38:51 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1874d44f528cc41c245df4baedcfeb20ef54303b483b4e5629a614b6843b5a`  
		Last Modified: Tue, 13 Jan 2026 23:38:28 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af1147ece7b75b221a2d0127342aeec49fb050d4b57dbf9053b821302b7f519d`  
		Last Modified: Tue, 13 Jan 2026 23:40:25 GMT  
		Size: 223.8 MB (223832917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6818e0838cdf47da76181d1e6b68572683eb132547bcee37b19301fea1a54fc5`  
		Last Modified: Tue, 13 Jan 2026 23:38:51 GMT  
		Size: 143.6 KB (143550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dceb016fbe8527a3268b30e87fe497fe6dd5de4967bd2d165e0d05d77313f698`  
		Last Modified: Tue, 13 Jan 2026 23:38:28 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
