## `openjdk:22-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:6cc031947e5b060f656170b39c55c90ed32d94ab01b98293371ad9918dbbf8be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `openjdk:22-jdk-nanoserver` - windows version 10.0.17763.5329; amd64

```console
$ docker pull openjdk@sha256:dd2da2a6f834bee77b2dfee3e61a956432371bf02f030d5484ee9af093114227
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.9 MB (305862009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0ff50f643fab8e6f77f0f444b94a9be7ca29dca64727e9817456ec9e6e6295e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Wed, 24 Jan 2024 21:49:50 GMT
SHELL [cmd /s /c]
# Wed, 24 Jan 2024 21:49:52 GMT
ENV JAVA_HOME=C:\openjdk-22
# Wed, 24 Jan 2024 21:49:53 GMT
USER ContainerAdministrator
# Wed, 24 Jan 2024 21:50:04 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 24 Jan 2024 21:50:04 GMT
USER ContainerUser
# Wed, 24 Jan 2024 21:50:05 GMT
ENV JAVA_VERSION=22-ea+32
# Wed, 24 Jan 2024 21:50:13 GMT
COPY dir:2910aa6d48a65f6cb3b341e99f8037697e82cfa9d66306ea285460418ade2a15 in C:\openjdk-22 
# Wed, 24 Jan 2024 21:50:21 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 24 Jan 2024 21:50:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a7a1fde54c290957b88d84b1bc386d1cfbebd64c66a5f7d89dddbc0684f3b84`  
		Last Modified: Wed, 24 Jan 2024 21:50:29 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ff0717f84ce944ee71ea268b1f12385ce198caf6d4d9e191d4b2b98f134f342`  
		Last Modified: Wed, 24 Jan 2024 21:50:29 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf67ac6bb8ab30883ac7751f44b7bb0f4b5870867c1e6dfc6d8c81d6e4512bb5`  
		Last Modified: Wed, 24 Jan 2024 21:50:29 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d89e6f778ab14a8ea48b813f54139b00d5caa3d6a98a904fb857e5130079f105`  
		Last Modified: Wed, 24 Jan 2024 21:50:29 GMT  
		Size: 67.6 KB (67646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2761ce582c0cfbbd59ec63b4cab7fb90bdf757083d86bf41254fd5d46c4371f8`  
		Last Modified: Wed, 24 Jan 2024 21:50:26 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b2e2506948da141c186965cb4cd9e797714b1ddccd742af124398d14cd18a5`  
		Last Modified: Wed, 24 Jan 2024 21:50:26 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6a42ccd3b5a7c9402a464f8962d91c08b59c9a70ef6d9d24a0d30758a13672e`  
		Last Modified: Wed, 24 Jan 2024 21:50:37 GMT  
		Size: 197.4 MB (197371081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b32a36d2e9128bfc5c7e1410475d9643d12990861c7608b41d25b18f3cee5d`  
		Last Modified: Wed, 24 Jan 2024 21:50:26 GMT  
		Size: 3.8 MB (3825388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71e3d7e3f346bec6f3fb004b8bc76e57ba65910497fc6a54d9181647910fc723`  
		Last Modified: Wed, 24 Jan 2024 21:50:26 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
