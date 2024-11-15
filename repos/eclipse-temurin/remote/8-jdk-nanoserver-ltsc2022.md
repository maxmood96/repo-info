## `eclipse-temurin:8-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:dd0cf9dc04d532e202717d25a6dae95bfcf6fd1dbb278a24dd2dd5c472e48bfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2849; amd64

### `eclipse-temurin:8-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.2849; amd64

```console
$ docker pull eclipse-temurin@sha256:69fca1f6a2068a6bfc198d1a725cddd26b9aff6dd17e481512377415cea5b8ae
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.2 MB (224235675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd6717275ca5a78c5d54b41728373772a85bbe9b160dbd17968ea7ef53c28b5e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 02 Nov 2024 23:34:35 GMT
RUN Apply image 10.0.20348.2849
# Thu, 14 Nov 2024 21:30:42 GMT
SHELL [cmd /s /c]
# Thu, 14 Nov 2024 21:30:43 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Thu, 14 Nov 2024 21:30:43 GMT
ENV JAVA_HOME=C:\openjdk-8
# Thu, 14 Nov 2024 21:30:44 GMT
USER ContainerAdministrator
# Thu, 14 Nov 2024 21:30:46 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 14 Nov 2024 21:30:47 GMT
USER ContainerUser
# Thu, 14 Nov 2024 21:30:53 GMT
COPY dir:20063c61efcf25f5137b7902f122f09a78eae5d617f3f56a66aed8780998122b in C:\openjdk-8 
# Thu, 14 Nov 2024 21:30:58 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:815d6b7f925aef8327c34c34073ae54cc1c82120f1058682eac4c8c14ca21c70`  
		Last Modified: Tue, 12 Nov 2024 22:44:32 GMT  
		Size: 120.6 MB (120604951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36980ff27c8e13b54f8df6f3ba3b550c8ac09a4c9036070b4ccef6dfdabbc35a`  
		Last Modified: Thu, 14 Nov 2024 21:31:02 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3400f7807b0ca6d54c6151778d9992a6c75e083eb1badd81e9fbc1515b17f626`  
		Last Modified: Thu, 14 Nov 2024 21:31:01 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c031a7128ce465c54625da1bc0f177aefdb2d5cf306bf9830b9f6789b8ae9044`  
		Last Modified: Thu, 14 Nov 2024 21:31:01 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a031715fa78d73a85c5e06e6b15c24254edf0976a2cc8682a9d0275bba7864`  
		Last Modified: Thu, 14 Nov 2024 21:31:00 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:898defcee03fe4aa7af403dca31cf19783e0d4aa92d63cc6101814156a5772ab`  
		Last Modified: Thu, 14 Nov 2024 21:31:01 GMT  
		Size: 77.4 KB (77443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df10e722d2848fcae6ffcdd65d25172b76ab3eab3f08fa1795bdebb1eefa4fe`  
		Last Modified: Thu, 14 Nov 2024 21:31:00 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e9b463122f21b30955e8fbb0c7d63a64aaeaf02fac62eece8c273b5e2ae276`  
		Last Modified: Thu, 14 Nov 2024 21:31:07 GMT  
		Size: 103.4 MB (103441336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3d5c65a4866f94937deb313647bc35278ee240aff58468b6a1e2cfcc4f6c9c`  
		Last Modified: Thu, 14 Nov 2024 21:31:00 GMT  
		Size: 106.8 KB (106787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
