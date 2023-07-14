## `openjdk:22-nanoserver`

```console
$ docker pull openjdk@sha256:5ac9d540ceeb9958ad9b8c5d917c1ba4f9b37480b7eb634fb37c7e3ca531f881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4645; amd64

### `openjdk:22-nanoserver` - windows version 10.0.17763.4645; amd64

```console
$ docker pull openjdk@sha256:ceb467dd31a8964d5faef87302201b4c0de25868c792d30661443bab5f20b29a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307060242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3afc015cefe7e9011f5718f6c3f3dd8820269267a1f170f6580e46d721014bd5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jul 2023 07:42:59 GMT
RUN Apply image 10.0.17763.4645
# Thu, 13 Jul 2023 21:36:32 GMT
SHELL [cmd /s /c]
# Fri, 14 Jul 2023 00:14:58 GMT
ENV JAVA_HOME=C:\openjdk-22
# Fri, 14 Jul 2023 00:14:58 GMT
USER ContainerAdministrator
# Fri, 14 Jul 2023 00:15:08 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 14 Jul 2023 00:15:09 GMT
USER ContainerUser
# Fri, 14 Jul 2023 00:15:09 GMT
ENV JAVA_VERSION=22-ea+6
# Fri, 14 Jul 2023 00:15:23 GMT
COPY dir:e0143c3e47465d9d68a55c00c13c05b43857da5554d7eaf78587a09b18822614 in C:\openjdk-22 
# Fri, 14 Jul 2023 00:15:35 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 14 Jul 2023 00:15:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5c5b06ba65934bcf850a1a54ecf4b3da34d3e6d6c8e90dbc897719c3ea377c8a`  
		Last Modified: Tue, 11 Jul 2023 17:31:37 GMT  
		Size: 104.4 MB (104408241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f13c473988daf5951866dd9b290bd6417227c1d7df6e811cfe11438d033a1eba`  
		Last Modified: Thu, 13 Jul 2023 22:19:06 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544d6fd540738704e91e0cdf5ce429fe06193ca6f57b912ecd37720a5398c73e`  
		Last Modified: Fri, 14 Jul 2023 00:23:01 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:184aebbaa7a5b561357f50ab1e278ddea12853b5513f6ccee076e8977ee17cb5`  
		Last Modified: Fri, 14 Jul 2023 00:23:00 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f517a720df0787d39ebc3c54f30149bad465e8af46947e6dd7c609c5c63d3ef3`  
		Last Modified: Fri, 14 Jul 2023 00:23:00 GMT  
		Size: 71.4 KB (71362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50ee6f2b90fa1d7c818530d35c4808f44d5fa2414919c02d26f5b7db881751ed`  
		Last Modified: Fri, 14 Jul 2023 00:22:58 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c93295755dd6ed9d31d9dbfbbc9e216b6eaeddf68fea0ec65dfa89c5024e012`  
		Last Modified: Fri, 14 Jul 2023 00:22:58 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7f0d7b60a0a847dcbaa79032c2e057b2cda037727d498320086d6934232622`  
		Last Modified: Fri, 14 Jul 2023 00:23:18 GMT  
		Size: 198.8 MB (198775205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a0efbf663caa39fde558f0df1c4c7c5bba8281c1b7816d24b2fbce3ece7ebf`  
		Last Modified: Fri, 14 Jul 2023 00:23:00 GMT  
		Size: 3.8 MB (3798616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0017153927a096d745790a911cc459b88d536a334be54112d5934ad95ba45539`  
		Last Modified: Fri, 14 Jul 2023 00:22:58 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
