## `openjdk:27-ea-20-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:1259bc3ace8ccd12b10e803e71cd33e10215bd80d59c388e5c1fa0eeba9a0505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32690; amd64
	-	windows version 10.0.20348.5020; amd64

### `openjdk:27-ea-20-jdk-nanoserver` - windows version 10.0.26100.32690; amd64

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

### `openjdk:27-ea-20-jdk-nanoserver` - windows version 10.0.20348.5020; amd64

```console
$ docker pull openjdk@sha256:66984483dea36639e75c6a18a85ae808e7ac8e90342baf344cedf608c1d1d630
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.7 MB (351730325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80a24b2e7c3f17313ab596a56b50594f4de7d6856799236e6ccc10531a65dd34`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Wed, 06 May 2026 00:17:06 GMT
SHELL [cmd /s /c]
# Wed, 06 May 2026 00:17:06 GMT
ENV JAVA_HOME=C:\openjdk-27
# Wed, 06 May 2026 00:17:07 GMT
USER ContainerAdministrator
# Wed, 06 May 2026 00:17:08 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 06 May 2026 00:17:09 GMT
USER ContainerUser
# Wed, 06 May 2026 00:17:09 GMT
ENV JAVA_VERSION=27-ea+20
# Wed, 06 May 2026 00:18:10 GMT
COPY dir:c3f224550ec8b6665cba07dbef908716e6de0966477f7a8dd0ae7dcb0ed38037 in C:\openjdk-27 
# Wed, 06 May 2026 00:18:15 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 06 May 2026 00:18:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2ad434b149465b0d86bd75fba84c0bbad6901ae4c912bcffc14cdf04e1a6d2`  
		Last Modified: Wed, 06 May 2026 00:18:22 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d09ae83f136fc48aa67fc113d1dc74cd00b32baa9fa0db1f3ba144e1a0e5650`  
		Last Modified: Wed, 06 May 2026 00:18:22 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db3a40bd243512f430ab5c45bc1b67847206631167378fe224716d42a961d08a`  
		Last Modified: Wed, 06 May 2026 00:18:22 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca405dd064bbda736decf75e21facc0396f4307244e4fb08ed54516e10da8cb5`  
		Last Modified: Wed, 06 May 2026 00:18:22 GMT  
		Size: 77.7 KB (77709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3a0e76eef28b41c235aeef38343bdd735f7b2e267c9b21f7b2d70ec9a389ac`  
		Last Modified: Wed, 06 May 2026 00:18:20 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d98e5bdf8c80a711acf4a3d38954e222e56b3a72cd36e4aba4b49e60afa08d`  
		Last Modified: Wed, 06 May 2026 00:18:20 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e40448f369c55e053fa80e021e5404c118bf8ec20beb3d5a9e58c9ff6990a57`  
		Last Modified: Wed, 06 May 2026 00:18:35 GMT  
		Size: 224.6 MB (224582605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19d250e690ea5dfbc3fe3849005db9e8d3fecfffe51bdc391ce921ebdc5a393`  
		Last Modified: Wed, 06 May 2026 00:18:21 GMT  
		Size: 107.7 KB (107716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b617df9b4ce45013a6ad0f8e424535edad757022fc1ba4ca17e19ac68f87f36f`  
		Last Modified: Wed, 06 May 2026 00:18:20 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
