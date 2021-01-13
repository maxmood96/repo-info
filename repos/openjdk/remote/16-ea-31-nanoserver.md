## `openjdk:16-ea-31-nanoserver`

```console
$ docker pull openjdk@sha256:1b548345d0003eac196fc2456c421ce4610060f416c3b30f24c0c56f51ea1216
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `openjdk:16-ea-31-nanoserver` - windows version 10.0.17763.1697; amd64

```console
$ docker pull openjdk@sha256:2d4c09b415cc8c5660ff681e00e048409cc94b326f6fc574c54d9a688c8bdae1
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.2 MB (285174339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe6036ab642bf272cd0096022f748e9145e3156ed2e4e9db14745309a1d7b55e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 07 Jan 2021 16:14:35 GMT
RUN Apply image 1809-amd64
# Wed, 13 Jan 2021 19:56:48 GMT
SHELL [cmd /s /c]
# Wed, 13 Jan 2021 20:35:00 GMT
ENV JAVA_HOME=C:\openjdk-16
# Wed, 13 Jan 2021 20:35:01 GMT
USER ContainerAdministrator
# Wed, 13 Jan 2021 20:35:14 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 13 Jan 2021 20:35:14 GMT
USER ContainerUser
# Wed, 13 Jan 2021 20:35:15 GMT
ENV JAVA_VERSION=16-ea+31
# Wed, 13 Jan 2021 20:35:53 GMT
COPY dir:fe6fd9f7c603fa326749cdfccbcd31289565cc3ddebf09394bdb282528bbec2c in C:\openjdk-16 
# Wed, 13 Jan 2021 20:36:15 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Wed, 13 Jan 2021 20:36:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:62239e9aa1a352a20b0d4969c2b508b8a18d10e799d4db72e6f24ccbb2c724d9`  
		Size: 101.3 MB (101340070 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c2b6c001c337f812bceb3b03d15a70d1d9905540658e751e42f20f7cc0ddc819`  
		Last Modified: Wed, 13 Jan 2021 21:16:47 GMT  
		Size: 908.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22f53d1f631e14bb9677766dc089ce4caf4dae9627d1513773cfff289e94f42`  
		Last Modified: Wed, 13 Jan 2021 21:19:22 GMT  
		Size: 920.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43af010a68e2978961a3d63887efbc1230811009f66bd683e9fc4174f4185177`  
		Last Modified: Wed, 13 Jan 2021 21:19:20 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3132f9cb979d43ab9de9d926bc492cf9bd38763c7e557f278fe358ac557f14b6`  
		Last Modified: Wed, 13 Jan 2021 21:19:19 GMT  
		Size: 65.1 KB (65097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d6c42dd2fabc75c92d7f5ad83fa610805a5e5dea3aba8da7ef9c4271f5ec93`  
		Last Modified: Wed, 13 Jan 2021 21:19:16 GMT  
		Size: 937.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c305d39bd570a4cf26a62e0ba565b3ade4a6f94579e4f214edb131bc38eed2`  
		Last Modified: Wed, 13 Jan 2021 21:19:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41fbe3dedfaf1b65bcd1fa7a1fefd24bce7861d91926a0743359e87a127d55d3`  
		Last Modified: Wed, 13 Jan 2021 21:19:35 GMT  
		Size: 180.1 MB (180100041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1beb09f0fce8e993610f5fe07d43c5bc551dd96006fd45534831503966df1947`  
		Last Modified: Wed, 13 Jan 2021 21:19:17 GMT  
		Size: 3.7 MB (3663769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f65fc8c054e89c35c5ad5980292fbb7cc8e2ef4fdf38057fbec7a33db82348a`  
		Last Modified: Wed, 13 Jan 2021 21:19:17 GMT  
		Size: 825.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
