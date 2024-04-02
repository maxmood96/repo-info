## `openjdk:23-nanoserver-1809`

```console
$ docker pull openjdk@sha256:695895f41f65f350ba8a30192e4db0196dd86ac1c0c6cb641ffa93b2463ec7b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `openjdk:23-nanoserver-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull openjdk@sha256:980ef314d73fc9d4b4d0512852748b2724b2dac57aa011eac03da2aebdc404b5
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.4 MB (315444875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6889f531d45591b222ee5c6ec0f1eab19f9b4a0a6f32c50370ecd73a5b0df36f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 04 Mar 2024 00:43:57 GMT
RUN Apply image 10.0.17763.5576
# Tue, 02 Apr 2024 00:49:32 GMT
SHELL [cmd /s /c]
# Tue, 02 Apr 2024 00:49:33 GMT
ENV JAVA_HOME=C:\openjdk-23
# Tue, 02 Apr 2024 00:49:34 GMT
USER ContainerAdministrator
# Tue, 02 Apr 2024 00:49:40 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 02 Apr 2024 00:49:41 GMT
USER ContainerUser
# Tue, 02 Apr 2024 00:49:41 GMT
ENV JAVA_VERSION=23-ea+16
# Tue, 02 Apr 2024 00:49:49 GMT
COPY dir:f3d09cf69692f758db226c4f910955a08f8df4aaebb94168f321645efff83374 in C:\openjdk-23 
# Tue, 02 Apr 2024 00:49:59 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 02 Apr 2024 00:50:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7d1978583f4a1122c5128a802637410697b681e7aa97b596dcb589b088c0b85d`  
		Last Modified: Tue, 12 Mar 2024 19:41:51 GMT  
		Size: 104.6 MB (104620103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df7ce5e4e711f6348c9e9247aa4dafaed1c7298f89a410702eafc935d8bd2d4`  
		Last Modified: Tue, 02 Apr 2024 00:50:09 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1076d2ca9d032f349419125edf09fe4e45d754e33cf89d3fc0461c713b8009e9`  
		Last Modified: Tue, 02 Apr 2024 00:50:08 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01f5be77ecb1b2c2d3b4ad34b2046faa0f6f989265a5fc20cc52cd72b47e426b`  
		Last Modified: Tue, 02 Apr 2024 00:50:08 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf2e4b78253c2e172d4297a32b4f496316b3e8778b3afd09791a3f7ada4cf27`  
		Last Modified: Tue, 02 Apr 2024 00:50:08 GMT  
		Size: 67.0 KB (67050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bdd36c8c126c2d025eef2a884005288b404716d1cf6221e6edc5d520f7e7342`  
		Last Modified: Tue, 02 Apr 2024 00:50:06 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63c04e488ea34eb7a61bc9f8220f0dbb1b4cbda787e54b1a3b00d07ee8554c14`  
		Last Modified: Tue, 02 Apr 2024 00:50:06 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ea6a5651ff20ef1bfbbf5a954f9e82234a8265817d3f7aeced3b42700e9510c`  
		Last Modified: Tue, 02 Apr 2024 00:50:18 GMT  
		Size: 205.3 MB (205275956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db4f19c73f83ef0b6aa3199aa04d119b4314884566816e306e8404707835bb6`  
		Last Modified: Tue, 02 Apr 2024 00:50:07 GMT  
		Size: 5.5 MB (5475527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:864e267af1f0076762444564a3a76468f9f1ac2096a3569699104b648a565194`  
		Last Modified: Tue, 02 Apr 2024 00:50:06 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
