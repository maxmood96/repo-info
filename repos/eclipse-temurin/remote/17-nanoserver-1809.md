## `eclipse-temurin:17-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:dd168312d8225c13d0aef6ed1bfe9ac427f53ce86f1d41842d581549649511d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `eclipse-temurin:17-nanoserver-1809` - windows version 10.0.17763.3532; amd64

```console
$ docker pull eclipse-temurin@sha256:efb6b671e98da23ab14fb41432c9a2d5735df2c6ea68e415d707b05f8232f723
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.4 MB (292440577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14c1eabbd40374020506f9a55eac3ec74f718925323d8caeaf48e98caf41ff63`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 08 Oct 2022 01:37:47 GMT
RUN Apply image 10.0.17763.3532
# Wed, 12 Oct 2022 15:20:49 GMT
SHELL [cmd /s /c]
# Wed, 12 Oct 2022 15:40:45 GMT
ENV JAVA_VERSION=jdk-17.0.4.1+1
# Wed, 12 Oct 2022 15:40:46 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 12 Oct 2022 15:40:46 GMT
USER ContainerAdministrator
# Wed, 12 Oct 2022 15:40:56 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Oct 2022 15:40:56 GMT
USER ContainerUser
# Wed, 12 Oct 2022 15:41:11 GMT
COPY dir:de893fa6f4d02b385cd95015ab74e60b0c0c67a3785d10d2649390aedc7b2648 in C:\openjdk-17 
# Wed, 12 Oct 2022 15:41:24 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 12 Oct 2022 15:41:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5ead999142ecce15e02523c49706a633fa708374d94bb65a254e3a3c117d609b`  
		Size: 103.4 MB (103377244 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4a6a667d76c19fca171390d60fb90c40e16c777050e943a7fe17ad7686841f0f`  
		Last Modified: Wed, 12 Oct 2022 16:02:59 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a93b28de80dea4b31537a30529c041fb9ceba4183aca57155184c6d05b0136bb`  
		Last Modified: Wed, 12 Oct 2022 16:08:24 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8e5beb2714bccb035d187dfdd22fb39e4b5f128eb0af4ea1c5f32e56088bff`  
		Last Modified: Wed, 12 Oct 2022 16:08:24 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6223d43a575f8a5c5ebd4c40a04b96e68adf31120367abeb5d5e69fd3a7cd06b`  
		Last Modified: Wed, 12 Oct 2022 16:08:24 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06d0068cfd061307ed374fce36327e5cbfbf0f8f02eab6418115556ceed7a9e5`  
		Last Modified: Wed, 12 Oct 2022 16:08:22 GMT  
		Size: 73.1 KB (73061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa18be91d790ceae1d739ec811f5ac76faf2ee82c5882a508aec601dd4fba967`  
		Last Modified: Wed, 12 Oct 2022 16:08:22 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d05af531dae728250f23f1f671d422129e1e0d1c33a0a6de15e07e1b5946213d`  
		Last Modified: Wed, 12 Oct 2022 16:08:41 GMT  
		Size: 185.3 MB (185339980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b625e090be19b93bc3d2847d517970c95c3b48e9c6fb79ae78c2f23c0ebb99c`  
		Last Modified: Wed, 12 Oct 2022 16:08:23 GMT  
		Size: 3.6 MB (3643463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68051f51ea6f4c7fdb4e7090bd2d7199f8fa95e8aaa7382c05bef84852208171`  
		Last Modified: Wed, 12 Oct 2022 16:08:22 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
