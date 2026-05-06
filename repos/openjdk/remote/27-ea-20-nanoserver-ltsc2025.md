## `openjdk:27-ea-20-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:b7d5696db3cea15bbcdb2996bba38f93d33c6e32ebdee28b24cbc4ab5be6911b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32690; amd64

### `openjdk:27-ea-20-nanoserver-ltsc2025` - windows version 10.0.26100.32690; amd64

```console
$ docker pull openjdk@sha256:b432e625094554eab255ee54eaa16fb296a60803b6b341073ce52c1f45efae11
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.5 MB (424490506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b40f0a13df263e3ee050d1fbb6d9ea74dc20f2f39cbf1204a43701b003b16a11`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Apr 2026 06:39:57 GMT
RUN Apply image 10.0.26100.32690
# Wed, 06 May 2026 00:16:55 GMT
SHELL [cmd /s /c]
# Wed, 06 May 2026 00:16:56 GMT
ENV JAVA_HOME=C:\openjdk-27
# Wed, 06 May 2026 00:16:57 GMT
USER ContainerAdministrator
# Wed, 06 May 2026 00:17:16 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 06 May 2026 00:17:16 GMT
USER ContainerUser
# Wed, 06 May 2026 00:17:17 GMT
ENV JAVA_VERSION=27-ea+20
# Wed, 06 May 2026 00:18:00 GMT
COPY dir:c3f224550ec8b6665cba07dbef908716e6de0966477f7a8dd0ae7dcb0ed38037 in C:\openjdk-27 
# Wed, 06 May 2026 00:18:09 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 06 May 2026 00:18:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8af320c3b6d19296bcc7947e3beb8bc0c69cb12143db52efe988dc998ac088dc`  
		Last Modified: Tue, 14 Apr 2026 21:00:37 GMT  
		Size: 199.7 MB (199717094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c758385821b05d6a0be0ee41f01b399743123e2cd059bf23d15ce4c816a619`  
		Last Modified: Wed, 06 May 2026 00:18:16 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f6f016390cb18caa600bf52318f05bbc5cd8425cf95e0fa324d477496bdbba`  
		Last Modified: Wed, 06 May 2026 00:18:16 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:950248776fb50b8b33d55218a8e3b132be03c37aabdbf432a37601f5421339e6`  
		Last Modified: Wed, 06 May 2026 00:18:16 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6ac90b080437cc54c122ff26c86e744dfa110ab3fcf0896d9917900525101d0`  
		Last Modified: Wed, 06 May 2026 00:18:16 GMT  
		Size: 70.0 KB (69963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c39b6cac27488e5223b04958a9033e7c75c18c5836901713f893f0a8dadf162`  
		Last Modified: Wed, 06 May 2026 00:18:14 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4e66381fb18bceb980322e13ba0b62d58c7b555728b6d7b9c8ae1be057d852`  
		Last Modified: Wed, 06 May 2026 00:18:14 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beac1caa44be34ae72c5eea4f2ec2689144c62ba778bcf3ecd9ad714d0617030`  
		Last Modified: Wed, 06 May 2026 00:18:30 GMT  
		Size: 224.6 MB (224582676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b6822c961e1d86dcc7217a442e9770981d48c907a771ae780b72e6469d40641`  
		Last Modified: Wed, 06 May 2026 00:18:14 GMT  
		Size: 114.4 KB (114366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:050accbfc7b1aee58441521292e3f00b950b7e58fae1d96f7570a9b5000211c7`  
		Last Modified: Wed, 06 May 2026 00:18:14 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
