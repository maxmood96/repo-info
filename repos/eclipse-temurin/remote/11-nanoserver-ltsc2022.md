## `eclipse-temurin:11-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:744fe2ee0b92dfc3be055dcea1d86e29756d936e3b031873d157a6f5d72330e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `eclipse-temurin:11-nanoserver-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull eclipse-temurin@sha256:76cc32373fb0ebc0a3d4260386a286a73162a35a7c2bee4bd55f512aee55b585
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.3 MB (317310372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e1934b259c93599e3f33a791e74c66a6123b33f3e914083d88c0f1e1a98a87b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Jun 2025 00:43:46 GMT
RUN Apply image 10.0.20348.3807
# Tue, 10 Jun 2025 22:13:24 GMT
SHELL [cmd /s /c]
# Tue, 10 Jun 2025 22:13:24 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Tue, 10 Jun 2025 22:13:25 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 10 Jun 2025 22:13:26 GMT
USER ContainerAdministrator
# Tue, 10 Jun 2025 22:13:29 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Jun 2025 22:13:30 GMT
USER ContainerUser
# Tue, 10 Jun 2025 22:13:37 GMT
COPY dir:c61af6ceef573b3d63f31a61f55e07ef4d3bfab78d8c06e63a667655942ae5e8 in C:\openjdk-11 
# Tue, 10 Jun 2025 22:13:43 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 10 Jun 2025 22:13:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:96acbf1c6d5b6cc37517502ecbb6a1d2eb55b7615b696401ead868c97a971964`  
		Last Modified: Tue, 10 Jun 2025 20:17:56 GMT  
		Size: 122.5 MB (122540534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6e2da87273a18701b50679d0f33ab483e146c12d7b8b602deb54b9faec9205`  
		Last Modified: Tue, 10 Jun 2025 22:14:24 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9232c1390efc28b22b599aab39834419bd69d6448c4133e633692b92479f25f1`  
		Last Modified: Tue, 10 Jun 2025 22:14:24 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f757ffcb82a3e1886ca32a7db7fa5179a067d90a4cf291848d3cdd600f391a3`  
		Last Modified: Tue, 10 Jun 2025 22:14:24 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50b2c0d6685be3ac5acab8d3be827a08d4cf6dfba2a591cab3dd7cd09b5f47dd`  
		Last Modified: Tue, 10 Jun 2025 22:14:24 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8407366a950d9ccd0074db3db0e9a9fbbe82ac5f056a8025cf034711fdb3e5bc`  
		Last Modified: Tue, 10 Jun 2025 22:14:24 GMT  
		Size: 78.3 KB (78297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94ecfa4a3fe271e36115a1a56f3d94f910054e1281e5232e552cc300a6b31284`  
		Last Modified: Tue, 10 Jun 2025 22:14:25 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9487236b04ce9653240b580d03c89e61899ad3e3ad11cbbf32e032b7325e63`  
		Last Modified: Wed, 11 Jun 2025 00:12:59 GMT  
		Size: 194.6 MB (194577527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0ab9ff3108cdc10737bc3b3ed255985d29420f4101cd9123cc9f20fbef4e7be`  
		Last Modified: Tue, 10 Jun 2025 22:14:25 GMT  
		Size: 107.8 KB (107813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b538d90469ac9ff0e282bee3ba35d2317d15ee00706dd727cb7b69296a1e8118`  
		Last Modified: Tue, 10 Jun 2025 22:14:25 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
