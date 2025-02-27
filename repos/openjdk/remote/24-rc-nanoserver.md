## `openjdk:24-rc-nanoserver`

```console
$ docker pull openjdk@sha256:cfec488515a6c6612967428527aa02bc3d10617749eb810a5b0b417d5b4799f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3194; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `openjdk:24-rc-nanoserver` - windows version 10.0.26100.3194; amd64

```console
$ docker pull openjdk@sha256:acd4cbbf0130e51eb7ffaa9688de0c96a574f625dfd18715e221de74d49c6ac8
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.6 MB (414592651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d6b4b543f3d3963688623b3c8fbff171d21695336b8b7bef19f42c4457253bb`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 08 Feb 2025 22:31:47 GMT
RUN Apply image 10.0.26100.3194
# Thu, 27 Feb 2025 19:13:47 GMT
SHELL [cmd /s /c]
# Thu, 27 Feb 2025 19:13:47 GMT
ENV JAVA_HOME=C:\openjdk-24
# Thu, 27 Feb 2025 19:13:48 GMT
USER ContainerAdministrator
# Thu, 27 Feb 2025 19:13:50 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 27 Feb 2025 19:13:51 GMT
USER ContainerUser
# Thu, 27 Feb 2025 19:13:51 GMT
ENV JAVA_VERSION=24
# Thu, 27 Feb 2025 19:13:58 GMT
COPY dir:cf5ecdf170ed29d5224593d2b3a510464d2e7297517065c397a2229de8b2a139 in C:\openjdk-24 
# Thu, 27 Feb 2025 19:14:04 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 27 Feb 2025 19:14:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e075dd07cbf907b7da8dbd8365b73a71ac92a834b78f520bd976cb97e0fcc0a1`  
		Last Modified: Wed, 12 Feb 2025 22:34:59 GMT  
		Size: 205.9 MB (205890263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9092cd1188531750c102da49846819f50a4ffa4e998cf04b2cc5359e0b46393c`  
		Last Modified: Thu, 27 Feb 2025 19:14:11 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da81558aa0912f78379267b1485bc45f924e197cf35b6ea36a968446472cbb59`  
		Last Modified: Thu, 27 Feb 2025 19:14:10 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50d83ccb227b31a610316b6fdf8d25ab2827cc3d84540493a360c3a145eebcb`  
		Last Modified: Thu, 27 Feb 2025 19:14:11 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7d57bc4c8fd68572fe5da998b7b145d42ccd121ea8ed57c2e7fc7f10f8e537`  
		Last Modified: Thu, 27 Feb 2025 19:14:11 GMT  
		Size: 76.1 KB (76089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3daf0b4cdc70b169e92cd8576865a124da6f2d49306ea9ccfb47d3ef73d167d8`  
		Last Modified: Thu, 27 Feb 2025 19:14:09 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b44ab63de4aa56f77509748fd3cbb2842e8f7eeeeaa933d53a63953d2a8d5a`  
		Last Modified: Thu, 27 Feb 2025 19:14:09 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ed45f9edf540adc8bdec2f8001d3b8ba42d92a4d0fa5af0339964502f367ed`  
		Last Modified: Thu, 27 Feb 2025 19:14:20 GMT  
		Size: 208.5 MB (208526176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1f903f313e3f2c20ed82a4b2d73bf3ed02033028ecc7e4e03f5dfd273f34403`  
		Last Modified: Thu, 27 Feb 2025 19:14:09 GMT  
		Size: 93.8 KB (93812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b321fe94742953cc5f0bebd3d721cf0072b2e61f8645876e2e2074d55c4bfff`  
		Last Modified: Thu, 27 Feb 2025 19:14:09 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:24-rc-nanoserver` - windows version 10.0.20348.3207; amd64

```console
$ docker pull openjdk@sha256:5d99fd40a56e2dc97df07817613073c7d8394315d89e14f725181c13eb7079ce
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.4 MB (329398030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffde4c639f0d9bddad0571c1d4c4e2e1eff1cf7ad7a7799db1fa685a799b503e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Feb 2025 20:45:43 GMT
RUN Apply image 10.0.20348.3207
# Thu, 13 Feb 2025 01:18:46 GMT
SHELL [cmd /s /c]
# Thu, 13 Feb 2025 01:18:47 GMT
ENV JAVA_HOME=C:\openjdk-24
# Thu, 13 Feb 2025 01:18:48 GMT
USER ContainerAdministrator
# Thu, 13 Feb 2025 01:18:51 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 13 Feb 2025 01:18:51 GMT
USER ContainerUser
# Thu, 13 Feb 2025 01:18:52 GMT
ENV JAVA_VERSION=24
# Thu, 13 Feb 2025 01:18:59 GMT
COPY dir:cf5ecdf170ed29d5224593d2b3a510464d2e7297517065c397a2229de8b2a139 in C:\openjdk-24 
# Thu, 13 Feb 2025 01:19:04 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 13 Feb 2025 01:19:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:938e4585b186fc3df3c1959d47ba7a634fea121cec7545db7923ceb191d99a33`  
		Last Modified: Tue, 11 Feb 2025 22:43:09 GMT  
		Size: 120.7 MB (120666610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca32c5ed90f22b0929449a457d80c4c4d488d229a00de61f4ad4c2ad992ab6e`  
		Last Modified: Thu, 13 Feb 2025 01:19:11 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7ec97e98e193c39e1ba87bf34b37ab27327cb58abd4c444ae089417a4d397e6`  
		Last Modified: Thu, 13 Feb 2025 01:19:11 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea151a55ec5a5402d2ed66d67168550cebb72bdae88962cdf056147110d30be9`  
		Last Modified: Thu, 13 Feb 2025 01:19:11 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e40df6a94263acbe1e3457fdc53e1d0c32c3475686f1ce81ac7813cf4416ae1`  
		Last Modified: Thu, 13 Feb 2025 01:19:11 GMT  
		Size: 79.3 KB (79336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26011d2ade6cdbbed31766f3d18cbb3a2f2320e8516c6857d724cfe3b4671366`  
		Last Modified: Thu, 13 Feb 2025 01:19:09 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bbb293beea64d907a749bea6cf0b9ba20cd3d8ed46e88b46ef3ae1ab16b8833`  
		Last Modified: Thu, 13 Feb 2025 01:19:09 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:046171047dce804264d3cea1587ddf75710e1a88d40de818a7185426f6dd27b3`  
		Last Modified: Thu, 13 Feb 2025 01:19:20 GMT  
		Size: 208.5 MB (208527578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39f03e65ece69044afe2727d8b07a82891ad8efedfc7596ff820e5f1bf387992`  
		Last Modified: Thu, 13 Feb 2025 01:19:09 GMT  
		Size: 118.3 KB (118277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75301350ffd85a4c54218762a009c59e3a7d0afd1ba168dc281b51f2361f394`  
		Last Modified: Thu, 13 Feb 2025 01:19:09 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:24-rc-nanoserver` - windows version 10.0.17763.6893; amd64

```console
$ docker pull openjdk@sha256:296396df4bb3a27df6f57305a46c036bc95239f9b067da25109484c9e141b9e1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.9 MB (319947495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe27c8d69bd53797c7cba7c49cee2885338a2b2f99ddfc43ef7123ce20e75d6b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Thu, 13 Feb 2025 01:15:32 GMT
SHELL [cmd /s /c]
# Thu, 13 Feb 2025 01:15:33 GMT
ENV JAVA_HOME=C:\openjdk-24
# Thu, 13 Feb 2025 01:15:34 GMT
USER ContainerAdministrator
# Thu, 13 Feb 2025 01:15:36 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 13 Feb 2025 01:15:36 GMT
USER ContainerUser
# Thu, 13 Feb 2025 01:15:37 GMT
ENV JAVA_VERSION=24
# Thu, 13 Feb 2025 01:15:44 GMT
COPY dir:cf5ecdf170ed29d5224593d2b3a510464d2e7297517065c397a2229de8b2a139 in C:\openjdk-24 
# Thu, 13 Feb 2025 01:15:49 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 13 Feb 2025 01:15:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Tue, 11 Feb 2025 20:25:23 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d693e20229b4584d695af0ea22ff9983a8de5c2580d824746662df0d098f502`  
		Last Modified: Thu, 13 Feb 2025 01:15:57 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048de90e4af2eabd8e88300d174a6eaf8d1affb9595bcb44a910aa550b022535`  
		Last Modified: Thu, 13 Feb 2025 01:15:56 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19bb4302440864df2605567730ccb6b95ebc4b08573d103a940c53acf995219`  
		Last Modified: Thu, 13 Feb 2025 01:15:56 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d6b5ce27eeb5fe93f3581fa080e78a5b7323e2324ad9d7d06be329180949cb`  
		Last Modified: Thu, 13 Feb 2025 01:15:56 GMT  
		Size: 71.8 KB (71844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f236e3498e94674c64603c786bf6df9aaf5094fb7432f19754a7f1bc615b010`  
		Last Modified: Thu, 13 Feb 2025 01:15:54 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555c2989c1b53c407da6d9802d5c6defa5d3e1792cafc3729a6ff5708bca5633`  
		Last Modified: Thu, 13 Feb 2025 01:15:54 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f41e9c89e8697db60ccd4b7fc32bf2e9f9dd03475e4dd99beddffd626920a5d`  
		Last Modified: Thu, 13 Feb 2025 01:16:05 GMT  
		Size: 208.5 MB (208527262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b42030d586c0ee7286f1ab46a1f0682b98fb2b2935a3e2769b0c20ba5b22d66b`  
		Last Modified: Thu, 13 Feb 2025 01:15:55 GMT  
		Size: 4.4 MB (4426662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bf7b48f254b4096babf9224902bad9fc075703ed90c1c0e1864722b25ee4867`  
		Last Modified: Thu, 13 Feb 2025 01:15:54 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
