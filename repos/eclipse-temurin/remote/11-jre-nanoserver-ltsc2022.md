## `eclipse-temurin:11-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:d2c754a3649d808e808c705117ff282d9b9858effbc304c0b08893ff6294f595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `eclipse-temurin:11-jre-nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull eclipse-temurin@sha256:607e1394d029b19b12fba1fab6c0db8dc17206561db335bb29a12bd459767e8b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.6 MB (166569040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c094784007da44794d1f2aa311cb01a69186f3f475dbf38c06ba8e4fc52521e0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Wed, 10 Sep 2025 22:18:34 GMT
SHELL [cmd /s /c]
# Wed, 10 Sep 2025 22:18:34 GMT
ENV JAVA_VERSION=jdk-11.0.28+6
# Wed, 10 Sep 2025 22:18:34 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 10 Sep 2025 22:18:35 GMT
USER ContainerAdministrator
# Wed, 10 Sep 2025 22:18:40 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Sep 2025 22:18:40 GMT
USER ContainerUser
# Wed, 10 Sep 2025 22:18:48 GMT
COPY dir:58dfc6149e1020fd4be2dce5848817d79ad79993fb8b5211b36f6f0e332ab65c in C:\openjdk-11 
# Wed, 10 Sep 2025 22:18:50 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f33532287b0006fe87acc27b3bf5bcdae6f0948804665cf7a9e3814536742d9`  
		Last Modified: Wed, 10 Sep 2025 22:19:37 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:354ba5f2a7059ef0a057357e6897c5bd218fca27ba2a7fde09059806795bb2db`  
		Last Modified: Wed, 10 Sep 2025 22:19:37 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d31b30d0eb29f08d160e387dc0e24796f00e3c84d671c735f3bcc732ee6ff1c`  
		Last Modified: Wed, 10 Sep 2025 22:19:37 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6175ebf55c12a511f00bedd528be9b74bfd70eafe324edc5e280aa3d6dd08e`  
		Last Modified: Wed, 10 Sep 2025 22:19:38 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cad91a483a38fd8f05a7d12298e549cc4906c71c01f66519b7dd66b32d41c0ed`  
		Last Modified: Wed, 10 Sep 2025 22:19:37 GMT  
		Size: 85.4 KB (85401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ecd9b0dbac2cb214ee88ddbbcef5879e66ba923d40f33d5c4f7a90e2f66f541`  
		Last Modified: Wed, 10 Sep 2025 22:19:38 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134181f1480ba5e856f118c3cb386aa84ac305797f265f87af1045e036707453`  
		Last Modified: Wed, 10 Sep 2025 22:19:44 GMT  
		Size: 43.7 MB (43666233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5278e0cf3ebfac5a0acb5dac1479d466af2fc7d121320c4852651d91d9879eb8`  
		Last Modified: Wed, 10 Sep 2025 22:19:38 GMT  
		Size: 92.2 KB (92164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
