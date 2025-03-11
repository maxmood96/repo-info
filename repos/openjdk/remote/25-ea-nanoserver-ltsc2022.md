## `openjdk:25-ea-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:ef315f8ac85a9718be29018ea339133e1448f7167d3437fe89ac597e3f4f466b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `openjdk:25-ea-nanoserver-ltsc2022` - windows version 10.0.20348.3207; amd64

```console
$ docker pull openjdk@sha256:17a5bd7b2bb73dfef1373d732100662c1eae33833fa87852ab9cee709ed9b7f2
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.3 MB (328261755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07792d9aabf4bd3dd9c4317f1a41236800a362a7b4be86f428ca143f8a71ce65`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Feb 2025 20:45:43 GMT
RUN Apply image 10.0.20348.3207
# Mon, 10 Mar 2025 22:11:34 GMT
SHELL [cmd /s /c]
# Mon, 10 Mar 2025 22:11:35 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 10 Mar 2025 22:11:36 GMT
USER ContainerAdministrator
# Mon, 10 Mar 2025 22:11:50 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 10 Mar 2025 22:11:51 GMT
USER ContainerUser
# Mon, 10 Mar 2025 22:11:51 GMT
ENV JAVA_VERSION=25-ea+13
# Mon, 10 Mar 2025 22:11:59 GMT
COPY dir:41adcea28f6e8239eac0b74c19049c5daef67ad138ba9db7bdf8df0acc8b0b9b in C:\openjdk-25 
# Mon, 10 Mar 2025 22:12:05 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 10 Mar 2025 22:12:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:938e4585b186fc3df3c1959d47ba7a634fea121cec7545db7923ceb191d99a33`  
		Last Modified: Tue, 11 Feb 2025 22:43:09 GMT  
		Size: 120.7 MB (120666610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9da150ea4148ad0207982ead62d436e56e22b37865514aecbdc4b994008e53`  
		Last Modified: Mon, 10 Mar 2025 22:12:11 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a608914bc4b0f024e9f44bf63980206c8c7537550ae1564f5621cd34470e5a`  
		Last Modified: Mon, 10 Mar 2025 22:12:10 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f96ae180f14b7a3e7cedd9f4f619315428605657860247afade0d649c8bbeeda`  
		Last Modified: Mon, 10 Mar 2025 22:12:10 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b4a178ad55a8bfd2faf5381391bbeb72f4915f2003e9229a3cc07c041d39ed`  
		Last Modified: Mon, 10 Mar 2025 22:12:10 GMT  
		Size: 83.6 KB (83565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c480dc0419ea8d8fd848b8ce031525d2bf4c2d7b72710ec28f61c86d100b799`  
		Last Modified: Mon, 10 Mar 2025 22:12:09 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87d72abacaf3bf5b966f062a6f3602c063175b55be91e3cea8c0082964f39f8`  
		Last Modified: Mon, 10 Mar 2025 22:12:09 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc5442221df34cb19c389bd2b5d77c78c1a746bb528221125c623879edbf8959`  
		Last Modified: Mon, 10 Mar 2025 22:12:20 GMT  
		Size: 207.4 MB (207399271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ebf2d14a6308825e46cb57407e39f4467eddc0db0017e31e4b4aeacabfa802d`  
		Last Modified: Mon, 10 Mar 2025 22:12:09 GMT  
		Size: 106.1 KB (106134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2cfdfff175f984e4f9b1dab9dc64910ae88d66a1d4be7813df72be8051c35c`  
		Last Modified: Mon, 10 Mar 2025 22:12:09 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
