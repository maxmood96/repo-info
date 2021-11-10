## `openjdk:18-nanoserver`

```console
$ docker pull openjdk@sha256:2c698eed211dacdfcad8cfcf8bb65180e9feb2e4af011e0da302e5f09294fb74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `openjdk:18-nanoserver` - windows version 10.0.17763.2300; amd64

```console
$ docker pull openjdk@sha256:76e7ce8921200c2da74218723265e748efb5b538bbc805d96e5875c35e6c9685
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.7 MB (289705169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f605ec0f6d8620a8d7837798a5cb287e6f718b34f4aa184e494be9c400f5ee93`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 04 Nov 2021 00:06:50 GMT
RUN Apply image 1809-amd64
# Wed, 10 Nov 2021 17:13:20 GMT
SHELL [cmd /s /c]
# Wed, 10 Nov 2021 20:31:55 GMT
ENV JAVA_HOME=C:\openjdk-18
# Wed, 10 Nov 2021 20:31:55 GMT
USER ContainerAdministrator
# Wed, 10 Nov 2021 20:32:07 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 10 Nov 2021 20:32:07 GMT
USER ContainerUser
# Wed, 10 Nov 2021 20:32:08 GMT
ENV JAVA_VERSION=18-ea+21
# Wed, 10 Nov 2021 20:32:23 GMT
COPY dir:2484c24fc278a2a4f9b1faf3e56bed024398b36a40c94d33298963a00cd29cac in C:\openjdk-18 
# Wed, 10 Nov 2021 20:32:37 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 10 Nov 2021 20:32:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b9dc943b4e8df8f472d444248152fa0920172ec630a60ada316e1603600dd1c7`  
		Size: 102.8 MB (102782944 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e60ec86b90e1492e0e0ed2cbebcf624990a34862e24207343fd85b84b3544c8e`  
		Last Modified: Wed, 10 Nov 2021 18:01:59 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d97d878bac5dd9dcbe1bb5f45ade2111fc77e8d4a5a348163bd9c3ddddbaf0`  
		Last Modified: Wed, 10 Nov 2021 21:11:37 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5a46fd95d3a8e8b5949c49cc0d70b858bddbe38c8c33e0a6a3e0f157d7795a`  
		Last Modified: Wed, 10 Nov 2021 21:11:37 GMT  
		Size: 1.1 KB (1117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88539ad3f1fb0ea6957da9a7298c1f6546afbb52b2deb7199763195fca993d98`  
		Last Modified: Wed, 10 Nov 2021 21:11:37 GMT  
		Size: 74.2 KB (74205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d133fe2173015750539b2d0a8fb86dbdbe0c6b44c8d75ddeb714a82814f98e00`  
		Last Modified: Wed, 10 Nov 2021 21:11:33 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b032844458881830eff0be6c730b39b70a8e00d9d48b5614c499b10d0e55a131`  
		Last Modified: Wed, 10 Nov 2021 21:11:33 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03cfe5eb122e63822c38ded40d5cef742bc695b3c16c2c099cbfae63d43c6588`  
		Last Modified: Wed, 10 Nov 2021 21:11:54 GMT  
		Size: 183.3 MB (183299359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d4615c9ed406caf4fcd84446b3e0dd7e56d63892a56c81965b04d213d8a677`  
		Last Modified: Wed, 10 Nov 2021 21:11:35 GMT  
		Size: 3.5 MB (3541799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14712278de59cab664f0e49fa0f1871ec5ab10ba4e7b6dbe5945492d496c781e`  
		Last Modified: Wed, 10 Nov 2021 21:11:34 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
