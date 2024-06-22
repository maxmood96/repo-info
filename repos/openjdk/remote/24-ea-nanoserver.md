## `openjdk:24-ea-nanoserver`

```console
$ docker pull openjdk@sha256:289cfb631306213d8302803423302797a4502c349b4eddae59d5959652f3ba0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `openjdk:24-ea-nanoserver` - windows version 10.0.17763.5936; amd64

```console
$ docker pull openjdk@sha256:73544b4dfad423855fb4a65eae284023ba8cd5dfabe15d180477ee0c9804fdb2
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.4 MB (365361475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:435736eeac1066b4c6ac2ffee7b40d7d7caf98648d048b3a9109a213abd6c430`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Sat, 22 Jun 2024 01:55:50 GMT
SHELL [cmd /s /c]
# Sat, 22 Jun 2024 01:55:51 GMT
ENV JAVA_HOME=C:\openjdk-24
# Sat, 22 Jun 2024 01:55:51 GMT
USER ContainerAdministrator
# Sat, 22 Jun 2024 01:55:54 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Sat, 22 Jun 2024 01:55:54 GMT
USER ContainerUser
# Sat, 22 Jun 2024 01:55:55 GMT
ENV JAVA_VERSION=24-ea+3
# Sat, 22 Jun 2024 01:56:02 GMT
COPY dir:ac706fd7680243000916208fdac0fe012de984bd3d7c1a69a00cb1e912b945d5 in C:\openjdk-24 
# Sat, 22 Jun 2024 01:56:08 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 22 Jun 2024 01:56:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4f703ea968d7f7434cf61e5d835cb3c507a6364ff8c7b3b96b73391b22115615`  
		Last Modified: Tue, 11 Jun 2024 20:35:02 GMT  
		Size: 155.0 MB (155033193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81655ff74f289146f3e18d8e7c8ccb79401e616877c5d4682a328f27a026ccae`  
		Last Modified: Sat, 22 Jun 2024 01:56:15 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ef002b78ad7e29ada802ce6f70faf52eeb30739d36f0582d229fac256cd61f`  
		Last Modified: Sat, 22 Jun 2024 01:56:15 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38cb7fd26155dc728ba10c879a3e7fc6c24e7514e604cf028a3786a60a6ff43c`  
		Last Modified: Sat, 22 Jun 2024 01:56:14 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:797d06b71a375d8c6732efa869f0a77c1cd2b77757e92cf6db2f4b6b117ec7d7`  
		Last Modified: Sat, 22 Jun 2024 01:56:14 GMT  
		Size: 83.6 KB (83592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd3443c20a465844ce8061a4fdf4f045772839cf710f8afd2a4c946622ae1295`  
		Last Modified: Sat, 22 Jun 2024 01:56:13 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b7299ba25ba7296fc6a9f44b1f55b9af9dbfde2c0c66f0cb964ba0bef5b5a71`  
		Last Modified: Sat, 22 Jun 2024 01:56:13 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30dde71ed85e3d59d94d4812dd3f34690cd52805500c6fc50b799e55442af744`  
		Last Modified: Sat, 22 Jun 2024 01:56:24 GMT  
		Size: 206.2 MB (206164571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:031dc3928e6a990dba3f630e88cb0c4ba28f7425b70d9cb1b3696893de3924a6`  
		Last Modified: Sat, 22 Jun 2024 01:56:13 GMT  
		Size: 4.1 MB (4073646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ca41bb89179358ad2fd01b818437450d51afc2f0033a6b47ea02e5b53edb405`  
		Last Modified: Sat, 22 Jun 2024 01:56:13 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
