## `openjdk:25-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:bec02eb4cfe2bb3f0c408352ad6ce8923b54faeaea6046241ba3e1d7bcec2ae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3775; amd64

### `openjdk:25-nanoserver-ltsc2025` - windows version 10.0.26100.3775; amd64

```console
$ docker pull openjdk@sha256:5c51639e2f3e5857a3397004e3166f666ae5c5e6164e028f1b2de2e5f7582036
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.3 MB (398267628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b0dcbdc3b77b86a167cffb9998a7b6d195727e4c082d8a42aad2ee580c98c3d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 06 Apr 2025 07:26:08 GMT
RUN Apply image 10.0.26100.3775
# Wed, 09 Apr 2025 01:18:18 GMT
SHELL [cmd /s /c]
# Wed, 09 Apr 2025 01:18:18 GMT
ENV JAVA_HOME=C:\openjdk-25
# Wed, 09 Apr 2025 01:18:19 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 01:18:21 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 09 Apr 2025 01:18:22 GMT
USER ContainerUser
# Wed, 09 Apr 2025 01:18:22 GMT
ENV JAVA_VERSION=25-ea+17
# Wed, 09 Apr 2025 01:18:29 GMT
COPY dir:31d4a08dd20e935927d81b33c56eb56ceaeead96529382a0c30c5f89fc836ee7 in C:\openjdk-25 
# Wed, 09 Apr 2025 01:18:36 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 09 Apr 2025 01:18:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:79b2ed45f890e91d23d7d22491a8fb6909c9268c668dc6a0e3b40131da02ed74`  
		Last Modified: Wed, 09 Apr 2025 00:36:30 GMT  
		Size: 190.1 MB (190113206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cdfe7b8f10b04296652ae9abbb37362fdd7e3adda4ace99bec5aa59d6c19769`  
		Last Modified: Wed, 09 Apr 2025 01:18:42 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a2a91e8784f4d940134c228c5facff9aa28b816c718df6aa20c2500d9bf1f2c`  
		Last Modified: Wed, 09 Apr 2025 01:18:42 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6e565ceb16763cf82294dbca944eaa9e87ad284f6c652c8f33d5f380c21450`  
		Last Modified: Wed, 09 Apr 2025 01:18:42 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f7c47343bc6d40619735349e13025407a28453f70334d136df0fd7c62eb2168`  
		Last Modified: Wed, 09 Apr 2025 01:18:42 GMT  
		Size: 76.2 KB (76170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feb1948d2ea41f6f9ac5c561fab41b76ef30dadb0522badb08c9a9c2a8f8c5c8`  
		Last Modified: Wed, 09 Apr 2025 01:18:40 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4414ae27a8a5f72ca8f740f0d9f7363c8b893191c777fa93cf343135bfa259a3`  
		Last Modified: Wed, 09 Apr 2025 01:18:40 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72e82fadf2ab1496c794d9e030acd85d6be33f4d586f05b47849128dcb23657e`  
		Last Modified: Wed, 09 Apr 2025 01:18:51 GMT  
		Size: 208.0 MB (207956634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:062cbd056959ea3cff5fcbce17c63b6307a44935e9e960bf2b3ab041d0dda243`  
		Last Modified: Wed, 09 Apr 2025 01:18:40 GMT  
		Size: 115.3 KB (115260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881ab8f2bd5f6520d8701a1b8952da4f440d612fe1701c149c0bab09ddcc977b`  
		Last Modified: Wed, 09 Apr 2025 01:18:40 GMT  
		Size: 1.1 KB (1088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
