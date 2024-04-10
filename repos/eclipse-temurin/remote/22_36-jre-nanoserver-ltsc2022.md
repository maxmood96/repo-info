## `eclipse-temurin:22_36-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:d63c54bc33b010f156090452ce45ed3e8914797b8b7c6afecf22c0175fa275ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `eclipse-temurin:22_36-jre-nanoserver-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull eclipse-temurin@sha256:8771f8198353599c3bf8b72bf7e73f1c4c0f1277a023c1eed0f6b077bfeefbda
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.6 MB (169613674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:369562ee4c3e9a2c690d9c39f309a0de9348ededa2d89a272e77ae5926bf01cd`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Apr 2024 08:53:11 GMT
RUN Apply image 10.0.20348.2402
# Wed, 10 Apr 2024 00:34:53 GMT
SHELL [cmd /s /c]
# Wed, 10 Apr 2024 00:40:19 GMT
ENV JAVA_VERSION=jdk-22+36
# Wed, 10 Apr 2024 00:40:20 GMT
ENV JAVA_HOME=C:\openjdk-22
# Wed, 10 Apr 2024 00:40:21 GMT
USER ContainerAdministrator
# Wed, 10 Apr 2024 00:40:30 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Apr 2024 00:40:31 GMT
USER ContainerUser
# Wed, 10 Apr 2024 00:41:21 GMT
COPY dir:205bc28a2cfde808c3c902b087992a6d179f1f6b12b6c0fffa64f09e3dab56d1 in C:\openjdk-22 
# Wed, 10 Apr 2024 00:41:32 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:755fc767289b8847bd0d0d8d75efc308c040140acf2a3426973ba9fbf022c4c0`  
		Last Modified: Tue, 09 Apr 2024 23:50:18 GMT  
		Size: 121.0 MB (120993754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e70887eeae6a5d6d5fd81661024afc84fee637f674dee5e7127112cbfce90750`  
		Last Modified: Wed, 10 Apr 2024 01:00:01 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2fb0d9a77a72d9bcd9e2571d43678ec7cdbd36fa04817c766e3629434c90ace`  
		Last Modified: Wed, 10 Apr 2024 01:03:20 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7584ce14c659083fbc4898e8fc6dd6813e919285f680b44a48916c549504fb`  
		Last Modified: Wed, 10 Apr 2024 01:03:20 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:113fffa2e102ada8b3611a56f23c0b15a5118850881d7c58ce938c8190d3e4f8`  
		Last Modified: Wed, 10 Apr 2024 01:03:20 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf022c1012c448e2444fd3ac66c18203719fe5307e49ac8c8823db4428296274`  
		Last Modified: Wed, 10 Apr 2024 01:03:18 GMT  
		Size: 76.9 KB (76881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe3d2f58650e4ea177e80de5227843bec54db0abfad8bcf0a22549cb7fa9d5ff`  
		Last Modified: Wed, 10 Apr 2024 01:03:18 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7148e0b7781746b4fcd09c30ba9106aa0515e7e535800a1db7ae0de6c1f459e`  
		Last Modified: Wed, 10 Apr 2024 01:03:58 GMT  
		Size: 48.5 MB (48477962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210ab2d260fc6520971c354fd04951930ceb52e024c6d04dd60c3379d6abf48e`  
		Last Modified: Wed, 10 Apr 2024 01:03:49 GMT  
		Size: 59.7 KB (59719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
