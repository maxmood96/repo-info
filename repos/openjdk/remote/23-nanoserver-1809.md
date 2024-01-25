## `openjdk:23-nanoserver-1809`

```console
$ docker pull openjdk@sha256:91cb02f1421d624590d2ac76f95ea392498ee48347f287825e1a79c92331d81f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `openjdk:23-nanoserver-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull openjdk@sha256:3ff0cc7775f350518a7c607c93f5326ee8385ecbc9c3fd8cd865664b4155a7b2
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.0 MB (305981322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6956dee284c1f6461c77f2ff2459047114f2ba6f3e84e31a9a71cb3480f2ba5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Wed, 24 Jan 2024 21:50:14 GMT
SHELL [cmd /s /c]
# Wed, 24 Jan 2024 21:50:17 GMT
ENV JAVA_HOME=C:\openjdk-23
# Wed, 24 Jan 2024 21:50:20 GMT
USER ContainerAdministrator
# Wed, 24 Jan 2024 21:50:36 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 24 Jan 2024 21:50:38 GMT
USER ContainerUser
# Wed, 24 Jan 2024 21:50:39 GMT
ENV JAVA_VERSION=23-ea+6
# Wed, 24 Jan 2024 21:50:49 GMT
COPY dir:176795690854a775a7e8cda29adda079cb7acc2307b29f50794edbf13b63f41c in C:\openjdk-23 
# Wed, 24 Jan 2024 21:50:55 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 24 Jan 2024 21:50:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2513b3b4415b3a913b65571629f442ad82eb82a1ebafb15b7e9a185d9e7aa9a9`  
		Last Modified: Wed, 24 Jan 2024 21:51:03 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b5103e1b67e3ccd5415d8e35a8f0ac7f293dcfbec282ccf9974543e118d56f0`  
		Last Modified: Wed, 24 Jan 2024 21:51:03 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e14e8c77910f817d4ff5acc868323d7fde5dc3e3415adbea182afb5784bc6b`  
		Last Modified: Wed, 24 Jan 2024 21:51:03 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27744dbb9788a37f56e43a1247e8c1c2d47a3e30eb4ceb87b0b5cc142e91cbe8`  
		Last Modified: Wed, 24 Jan 2024 21:51:03 GMT  
		Size: 68.3 KB (68286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:401008a0e2964156c1f8e91b2bb0c632c482bdee3d53805ed6e1cd55a5460883`  
		Last Modified: Wed, 24 Jan 2024 21:51:00 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4939ccd33635e2317cadfb8bd7d42201c2ba5448f23dffc62a611fe4a48d6f7e`  
		Last Modified: Wed, 24 Jan 2024 21:51:00 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f0dbd4882a797423fb0521b88b91ad2d1e20e8494438cbfa71e8a440321e452`  
		Last Modified: Wed, 24 Jan 2024 21:51:11 GMT  
		Size: 197.5 MB (197455477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc7d9bbf01191f6b6617e3fb2232d0c85313ec688852057e664c9c681cf9282a`  
		Last Modified: Wed, 24 Jan 2024 21:51:01 GMT  
		Size: 3.9 MB (3860083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbde1ee50caa3183cfc4c7fe812980ec8cecbaad16004c8c49dd3137a038dbc6`  
		Last Modified: Wed, 24 Jan 2024 21:51:00 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
