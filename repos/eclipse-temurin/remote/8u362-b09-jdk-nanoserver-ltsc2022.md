## `eclipse-temurin:8u362-b09-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:44c48a751d02aa3c13f28dc07f9d81fdd0de362ca96b822dc77c5b76e1941c05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1607; amd64

### `eclipse-temurin:8u362-b09-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.1607; amd64

```console
$ docker pull eclipse-temurin@sha256:25bb04d63cc19db57a79cfbb2b933dea54cdc29f86b4d7244c82eaedc9caf538
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.8 MB (223756393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fa0fac9054f8404def06ecf356384a15cd57eacb5265584187657378dd9a842`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 10 Mar 2023 06:31:34 GMT
RUN Apply image 10.0.20348.1607
# Thu, 16 Mar 2023 01:29:33 GMT
SHELL [cmd /s /c]
# Thu, 16 Mar 2023 01:29:34 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 16 Mar 2023 01:29:35 GMT
ENV JAVA_HOME=C:\openjdk-8
# Thu, 16 Mar 2023 01:29:36 GMT
USER ContainerAdministrator
# Thu, 16 Mar 2023 01:29:54 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 16 Mar 2023 01:29:55 GMT
USER ContainerUser
# Thu, 16 Mar 2023 01:30:07 GMT
COPY dir:8214f6b15a617bff549fa1e8e973ad9cf58dcd41804c9c4d00b4aebf5303ecc4 in C:\openjdk-8 
# Thu, 16 Mar 2023 01:30:43 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:7abf0a70d48bf65f3d985f5780d4bdaece36f1f4bb8be10d5a6aacce33dacc75`  
		Last Modified: Thu, 16 Mar 2023 01:54:24 GMT  
		Size: 122.2 MB (122171731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a611a20686e9374e3a55a49399506f83c041ae711ed47018c2267c341156dd97`  
		Last Modified: Thu, 16 Mar 2023 01:53:50 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b4d6464959d95eab200c9a49617a9855ec77e0de5a20563e87c1a56e8c25f4`  
		Last Modified: Thu, 16 Mar 2023 01:53:50 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29dfedf32262d5595636120ea0904b9230ad36710eb1b92ec3fc339f2f8f732`  
		Last Modified: Thu, 16 Mar 2023 01:53:50 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32c7189a4a615fd7df46d6561fae78a2d4fd0868a85a3d6ba60d2b9f9a5cc633`  
		Last Modified: Thu, 16 Mar 2023 01:53:48 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4bd03bc0018decd48fb94c93ab94e095a0a872bc5d358e40f4b3733d7bd517f`  
		Last Modified: Thu, 16 Mar 2023 01:53:48 GMT  
		Size: 90.1 KB (90142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a09b5f72b3f9a8e103254e56666bfefa259756235941f52d69d96d1ad2cc03`  
		Last Modified: Thu, 16 Mar 2023 01:53:48 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48becd23492920895a0c85c272aa32c1f2e1afe26141ff1de8cd195059487832`  
		Last Modified: Thu, 16 Mar 2023 01:54:05 GMT  
		Size: 101.4 MB (101401601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da603e997a1ee1e3473a9d2d5afc56879ea9cdd8ea4e1d1759f461b8760f7463`  
		Last Modified: Thu, 16 Mar 2023 01:53:48 GMT  
		Size: 87.1 KB (87121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
