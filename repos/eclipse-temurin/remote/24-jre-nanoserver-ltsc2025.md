## `eclipse-temurin:24-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:b915807f6aa5a7b5534ae1ec4903320a296195f9d946539cffda735a327a38a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4946; amd64

### `eclipse-temurin:24-jre-nanoserver-ltsc2025` - windows version 10.0.26100.4946; amd64

```console
$ docker pull eclipse-temurin@sha256:12b672f23b06d44ca8908518f93dbce718d446420fe907627c216ccca28caf09
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.4 MB (251375815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00466621e19d517c07ed36344f0d9393dc6830f479bc83cbb3ef32f9359f3ae9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 10 Aug 2025 02:44:20 GMT
RUN Apply image 10.0.26100.4946
# Tue, 12 Aug 2025 20:50:13 GMT
SHELL [cmd /s /c]
# Tue, 12 Aug 2025 20:50:13 GMT
ENV JAVA_VERSION=jdk-24.0.2+12
# Tue, 12 Aug 2025 20:50:13 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 12 Aug 2025 20:50:14 GMT
USER ContainerAdministrator
# Tue, 12 Aug 2025 20:50:15 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 12 Aug 2025 20:50:16 GMT
USER ContainerUser
# Tue, 12 Aug 2025 20:50:19 GMT
COPY dir:68684ca63ce8d77d4faaa9841dd51e252c6afb57fd0de39359244aa7765e57f1 in C:\openjdk-24 
# Tue, 12 Aug 2025 20:50:21 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:6d63d98dae9e3419e8c965c24a11d30e40947cf35ee17c204c5d8b7bae7ff2ef`  
		Last Modified: Tue, 12 Aug 2025 21:13:38 GMT  
		Size: 193.5 MB (193469373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d33907d1de9a86fa9f6b64ebfe956e88a59995179f953ba71136dcc216c2a9`  
		Last Modified: Tue, 12 Aug 2025 20:51:36 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:392bdfdab461915a292ebabaf8ecb569d5fc66761448c759d52a06bc218727c4`  
		Last Modified: Tue, 12 Aug 2025 20:51:36 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c1b6a140b2dbd4e33e14751d514f5081fefde7ac2d78cef9373fdbf2a20001`  
		Last Modified: Tue, 12 Aug 2025 20:51:33 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:101e440a5e0e9c4e1b8a31532ed817fec0dd1131437598198de5255fe5f97491`  
		Last Modified: Tue, 12 Aug 2025 20:51:33 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b0f3a37e7cbfc8cc43dbd9b04650da34bbd5ffab64f33d542f937dff8799b1`  
		Last Modified: Tue, 12 Aug 2025 20:51:33 GMT  
		Size: 75.6 KB (75618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb1c7bb8394fbe4934bc35c2004d2b0a578a5abe8caf2b9ed75719335ac1461`  
		Last Modified: Tue, 12 Aug 2025 20:51:33 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6319135a14af87aaec61c58e719e82058f419bb3301e40eca3f866d87bc0e3e`  
		Last Modified: Tue, 12 Aug 2025 20:51:38 GMT  
		Size: 57.7 MB (57730083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4e398bb716b2c79b01542a859df481462c94b0f97553e60080fb1475a9c1ea`  
		Last Modified: Tue, 12 Aug 2025 20:51:35 GMT  
		Size: 95.5 KB (95477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
