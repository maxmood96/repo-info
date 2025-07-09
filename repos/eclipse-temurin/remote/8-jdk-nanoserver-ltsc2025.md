## `eclipse-temurin:8-jdk-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:b5acacad5aaf91f774b0c487ab2b1a5bd7f4e40e6280cae1834ffaeb0b3dfc8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4652; amd64

### `eclipse-temurin:8-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.4652; amd64

```console
$ docker pull eclipse-temurin@sha256:e19d2ed804eca5738a54294b6cc6f75b3b52a90731a8462d7fe698239866469c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.8 MB (295799696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52bca6a3060f65fd317253d565b2ebd7e184d662ae40ee34947e6e37b24e3e18`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Jul 2025 18:13:07 GMT
RUN Apply image 10.0.26100.4652
# Wed, 09 Jul 2025 19:14:09 GMT
SHELL [cmd /s /c]
# Wed, 09 Jul 2025 19:14:10 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Wed, 09 Jul 2025 19:14:11 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 09 Jul 2025 19:14:12 GMT
USER ContainerAdministrator
# Wed, 09 Jul 2025 19:14:16 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Jul 2025 19:14:17 GMT
USER ContainerUser
# Wed, 09 Jul 2025 19:14:23 GMT
COPY dir:5c4bbf817a67c787f7f2d8809dee99be16882c3512e063f4e47205ca5ccbd190 in C:\openjdk-8 
# Wed, 09 Jul 2025 19:14:29 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:2fd4507679915420227c89c4f57165747b37deaa62748936e2af8c2f38de0b4e`  
		Last Modified: Wed, 09 Jul 2025 01:51:41 GMT  
		Size: 193.2 MB (193150329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09643ebb4dd55f3e28fc4b4413e19f95f379a7a57edfb8108b21af2865175b1b`  
		Last Modified: Wed, 09 Jul 2025 19:15:03 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f254a18a3175f7354fdf49f87ebfc1ae654c42ed0d1c6670c6cfc2f91ad48605`  
		Last Modified: Wed, 09 Jul 2025 19:15:03 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f79ff24ea6a875c2cad427f2b1006150219a4ed23f10c30e903df7665be767`  
		Last Modified: Wed, 09 Jul 2025 19:15:03 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b4fe5271655f1b9c547bb841a015e12b5f2e8622fc6eb0c11499e384037f79`  
		Last Modified: Wed, 09 Jul 2025 19:15:03 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7376aaea128d42599d66fdb79f6bcff9df67b297d0c651ba12a2ea18ca27b8f`  
		Last Modified: Wed, 09 Jul 2025 19:15:03 GMT  
		Size: 86.8 KB (86817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6da071c3328ee169aec12ebc07e6ce4b483c765f36d7fc1e954e0e1045ca46`  
		Last Modified: Wed, 09 Jul 2025 19:15:03 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33444a4e8f3bb404ed7ca9b40302d8956b55014e9a145fc8f01b1ea03b5a0622`  
		Last Modified: Wed, 09 Jul 2025 19:15:20 GMT  
		Size: 102.4 MB (102440465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ee1ec0eda175e5a77d7ef088e9d8e368ac511211fc8197e5a22b4a10e9d2a3`  
		Last Modified: Wed, 09 Jul 2025 19:15:02 GMT  
		Size: 116.8 KB (116850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
