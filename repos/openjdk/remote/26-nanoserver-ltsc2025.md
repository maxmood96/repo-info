## `openjdk:26-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:c2bb0a544d3f80a44290d2046c2cfd7e117f35ef7458b00b09f88e6bb3358189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `openjdk:26-nanoserver-ltsc2025` - windows version 10.0.26100.6584; amd64

```console
$ docker pull openjdk@sha256:0cde35c79492abaf81baddc28916b2561f6eaf7b68d6426eb8d87819a2611403
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.9 MB (414931690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3894e86fb2a163de4220f27cc797ab05cba0f447d468a3689319521aabb1bf1`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Sep 2025 02:12:39 GMT
RUN Apply image 10.0.26100.6584
# Mon, 13 Oct 2025 19:12:15 GMT
SHELL [cmd /s /c]
# Mon, 13 Oct 2025 19:12:16 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 13 Oct 2025 19:12:16 GMT
USER ContainerAdministrator
# Mon, 13 Oct 2025 19:12:26 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 13 Oct 2025 19:12:27 GMT
USER ContainerUser
# Mon, 13 Oct 2025 19:12:27 GMT
ENV JAVA_VERSION=26-ea+19
# Mon, 13 Oct 2025 19:13:04 GMT
COPY dir:83313e74e1bdca6c4da8521f7958b3cb9f989c8b9d5087396f320ade6e966d10 in C:\openjdk-26 
# Mon, 13 Oct 2025 19:13:12 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 13 Oct 2025 19:13:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a75a4ab04983f989d9a1442633d6c3952b863719a00dd77cf160f7055beaded9`  
		Last Modified: Tue, 09 Sep 2025 22:28:08 GMT  
		Size: 193.6 MB (193550846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440ab8e560a8a0b2fbf0eee870d85cb038575979204780124b9b2add13964327`  
		Last Modified: Mon, 13 Oct 2025 19:14:09 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f207fe48eac331b93a8e20d0f3c904e94bbba525ff986a3b066a247641a287c3`  
		Last Modified: Mon, 13 Oct 2025 19:14:09 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a0286251f886eea2a48dcc0c9552bd0b1986b298a4fc913637fef3fffebc80`  
		Last Modified: Mon, 13 Oct 2025 19:14:10 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16815cceb162d698fd470cdef226c82f82fc349603c7518d7ff759f2396d29f9`  
		Last Modified: Mon, 13 Oct 2025 19:14:09 GMT  
		Size: 76.2 KB (76189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c163079d397c8d14d67ade2e1e1bbf8e26e18fb7b8d09cb6862c9b441f94fac`  
		Last Modified: Mon, 13 Oct 2025 19:14:09 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:265f98eb653b663d28047c56eb22b431e161a9f7c055d5ef06a30d384b05118e`  
		Last Modified: Mon, 13 Oct 2025 19:14:09 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd90db886916a2220901537ff8869b6127dc1f440960d1db931a48d6ab267978`  
		Last Modified: Mon, 13 Oct 2025 21:24:11 GMT  
		Size: 221.2 MB (221201313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4748fd41f46e4f5d73b6ae6e980df0a338c08774d4303e3731d04638caccc48`  
		Last Modified: Mon, 13 Oct 2025 19:14:09 GMT  
		Size: 96.9 KB (96924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:671b14d0b84bca3421a89cce7aec57e6b2424bdec5895875ed8fb3f4d7733a1e`  
		Last Modified: Mon, 13 Oct 2025 19:14:09 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
