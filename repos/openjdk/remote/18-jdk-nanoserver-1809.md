## `openjdk:18-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:9fe747e941ea704c141a034c0bb79b8d98cdd848fbe01ce1e034994e6d004ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2803; amd64

### `openjdk:18-jdk-nanoserver-1809` - windows version 10.0.17763.2803; amd64

```console
$ docker pull openjdk@sha256:a41584fdc596e98b5974f593b368d1bfe521b62141ee57ee4669a979cba17f10
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.7 MB (290712174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b87f9fbc54a58588fccd3092f4bbd3bfaa943f0a65aadf7d20a5b1cf974452e1`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 04 Apr 2022 10:52:49 GMT
RUN Apply image 1809-amd64
# Wed, 13 Apr 2022 15:16:11 GMT
SHELL [cmd /s /c]
# Wed, 13 Apr 2022 17:05:29 GMT
ENV JAVA_HOME=C:\openjdk-18
# Wed, 13 Apr 2022 17:05:30 GMT
USER ContainerAdministrator
# Wed, 13 Apr 2022 17:05:36 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 13 Apr 2022 17:05:36 GMT
USER ContainerUser
# Wed, 13 Apr 2022 17:05:37 GMT
ENV JAVA_VERSION=18
# Wed, 13 Apr 2022 17:05:51 GMT
COPY dir:9514de164eda2cdb5e3ddd51197372d790fb5291cfc39842e090e2c568516144 in C:\openjdk-18 
# Wed, 13 Apr 2022 17:06:03 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 13 Apr 2022 17:06:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6fc97003d8b7f593fe071cf3ea64f3ce760cc060f3402bb6b1b849c040e222d5`  
		Size: 103.1 MB (103096169 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ea4009814dceb50337c66614a6008cfc2fb73ce53e62162bce071ef6ea1adf2d`  
		Last Modified: Wed, 13 Apr 2022 15:58:06 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4468d9388e5559a4004079d5f1fd838e4035b4f7a779b9dcd519739bc5eb0c2`  
		Last Modified: Tue, 19 Apr 2022 00:58:37 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14553e0502d2ae5a3359bba1eddea3eb159cffd7f52d4feeb6ed6a0d4c8a2c1`  
		Last Modified: Tue, 19 Apr 2022 00:58:37 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7471a761068091f23d7258905991040011c191e07e8dc91f71fe3b1c4e88c29`  
		Last Modified: Tue, 19 Apr 2022 00:58:37 GMT  
		Size: 72.5 KB (72499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:975c3a13173078d8331455a5f4980e5df23fede4a4ecbaaf80352742f34fc590`  
		Last Modified: Tue, 19 Apr 2022 00:58:35 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d95e654dcc53c5b59b806f4c9ba2005b11295cecd74d0bb1913d6f084a181a5`  
		Last Modified: Tue, 19 Apr 2022 00:58:35 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f340b8def2c83209bf529bf39017931379f82a4b9fe893b473d1dee198d67b4c`  
		Last Modified: Tue, 19 Apr 2022 01:01:45 GMT  
		Size: 184.0 MB (183983717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246a58a80c5703049c8be7fef0a92ad9e387b330dbc8494dfa3f711f1951d0ee`  
		Last Modified: Tue, 19 Apr 2022 00:58:39 GMT  
		Size: 3.6 MB (3553071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fad66b245dbb89ea31823d1921cdaff02a0b120e0fc5448ce44a013613565920`  
		Last Modified: Tue, 19 Apr 2022 00:58:35 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
