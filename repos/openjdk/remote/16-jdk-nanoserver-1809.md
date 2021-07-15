## `openjdk:16-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:c9977d04cdef3670c028ef7e24eb88733bd2e7faed0998d50a4dd8e5d140d1e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2061; amd64

### `openjdk:16-jdk-nanoserver-1809` - windows version 10.0.17763.2061; amd64

```console
$ docker pull openjdk@sha256:01f9098c3e8ee9c4a0186fffbdbb4ba672cff092d15f5f39611d47a0a1ef415c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 MB (286540663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b28b7afbdb41cbee562ba456a38eeb58748c683613e0f02be6e0c75e56d4533d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 06 Jul 2021 20:06:39 GMT
RUN Apply image 1809-amd64
# Wed, 14 Jul 2021 02:53:30 GMT
SHELL [cmd /s /c]
# Wed, 14 Jul 2021 03:10:50 GMT
ENV JAVA_HOME=C:\openjdk-16
# Wed, 14 Jul 2021 03:10:53 GMT
USER ContainerAdministrator
# Wed, 14 Jul 2021 03:11:07 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 14 Jul 2021 03:11:10 GMT
USER ContainerUser
# Wed, 14 Jul 2021 03:11:12 GMT
ENV JAVA_VERSION=16.0.1
# Wed, 14 Jul 2021 03:11:27 GMT
COPY dir:ec453f8f02d21eabd8383c9d68e7e854c44e602cce3510b820d8ac55a0745712 in C:\openjdk-16 
# Wed, 14 Jul 2021 03:11:48 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 14 Jul 2021 03:11:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:29d43e56445c5279a6386c4dfe4d1ada3c7124ade9cb7b0f2757e58ffc7cd10b`  
		Size: 102.7 MB (102725622 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:78d8754fb12dd351c91bed29d92c703cddb135a78d8f056b6a3bf13a251c1d2d`  
		Last Modified: Wed, 14 Jul 2021 03:42:27 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf9694a21ba555df087e8739998eca9a0b56540365a4cba596a87fa3e2c41ea`  
		Last Modified: Wed, 14 Jul 2021 03:53:04 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3911007b3fc33a0faac9b39ed10a6ae256b02f1e7c47048c129b6ad09d99ca2`  
		Last Modified: Wed, 14 Jul 2021 03:53:04 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce5e7db34dd013fa3d55087c8194334bd63cfd45e4466e0d55b55f63ce9398e`  
		Last Modified: Wed, 14 Jul 2021 03:53:04 GMT  
		Size: 65.0 KB (65038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89bbdb6526137bb3e66d6e831498bd6a0a30d786ebc3980ad9ded3e8b3eee0d5`  
		Last Modified: Wed, 14 Jul 2021 03:53:01 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25192095913bcad40e0db4b6d38600857c954f64fd610fcabba7e341ccfb80aa`  
		Last Modified: Wed, 14 Jul 2021 03:53:01 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fcba57b25603239aeaa57e127f99e99cfc3fce8f52ce392c6996412cb2c4aac`  
		Last Modified: Wed, 14 Jul 2021 03:53:21 GMT  
		Size: 180.1 MB (180079315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea35ebccb76a8554bdae50ea4b10ee8513d59cddd93bb5bba43762a012e4719`  
		Last Modified: Wed, 14 Jul 2021 03:53:02 GMT  
		Size: 3.7 MB (3663762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb60f040cb0b19d59b99047cab8b019ecfb0f0e04a3dafd43a95ab44c8691850`  
		Last Modified: Wed, 14 Jul 2021 03:53:01 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
