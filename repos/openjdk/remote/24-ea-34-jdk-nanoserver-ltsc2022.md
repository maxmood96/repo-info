## `openjdk:24-ea-34-jdk-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:99490af6f8cb475d11d8552faa48d28064db57e44b9c0c5770a7d9da2777b525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `openjdk:24-ea-34-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull openjdk@sha256:e38191c526840e51e249d385f3cd6e2beece836fdf87fe8c341265c61d5e0615
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.4 MB (329392195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dccd4cec1e14f4715231ebbcbecbadbf416826445ce948cf360ad768c67fc295`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 12 Jan 2025 09:54:50 GMT
RUN Apply image 10.0.20348.3091
# Sat, 01 Feb 2025 00:27:51 GMT
SHELL [cmd /s /c]
# Sat, 01 Feb 2025 00:27:52 GMT
ENV JAVA_HOME=C:\openjdk-24
# Sat, 01 Feb 2025 00:27:53 GMT
USER ContainerAdministrator
# Sat, 01 Feb 2025 00:28:13 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Sat, 01 Feb 2025 00:28:14 GMT
USER ContainerUser
# Sat, 01 Feb 2025 00:28:14 GMT
ENV JAVA_VERSION=24-ea+34
# Sat, 01 Feb 2025 00:28:22 GMT
COPY dir:0417d4640b3e9898160c754927e6892a89119d4a6294484281d02c0d6a35e95f in C:\openjdk-24 
# Sat, 01 Feb 2025 00:28:28 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 01 Feb 2025 00:28:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fd3058b29fbd287119a2fa4d2d36a46fdee3bbada5fd9ef6f02f2d7d4cc143ab`  
		Last Modified: Tue, 14 Jan 2025 20:27:35 GMT  
		Size: 120.7 MB (120661554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b41f633378f84c0a110d07e814d103edc97b6bf6359ee159a25112ed1987bdc`  
		Last Modified: Sat, 01 Feb 2025 00:28:33 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60ad732a81c8bef07a550521e47b8b635c61cad15346324121926ed5d3488db0`  
		Last Modified: Sat, 01 Feb 2025 00:28:32 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314b7f5f102bb87c5f66ebddccb6dc6785d398a2e0545520145848fdfa81241d`  
		Last Modified: Sat, 01 Feb 2025 00:28:32 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:226aee3c470489db13b70f336ee2e0ca70d8ca7cbb6264e86f660ebc330063de`  
		Last Modified: Sat, 01 Feb 2025 00:28:32 GMT  
		Size: 93.1 KB (93087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb26cfa3c10ac3e598de4f9b084cddf3c63005ff3ab1a031891b0407355de40`  
		Last Modified: Sat, 01 Feb 2025 00:28:31 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac2eb2b30aeddfcd65b238057d0af67860e521b9099cdd56d6aadb81e480e11`  
		Last Modified: Sat, 01 Feb 2025 00:28:32 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5200bc29ba8ea7ef5b601b939f7be21649d1b5fce414eaa39d08632dd3273ea0`  
		Last Modified: Sat, 01 Feb 2025 00:28:42 GMT  
		Size: 208.5 MB (208532922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3277eebb2e2c73a6adf9975b37697c324db89d384cb53c74e732439ec1c9faed`  
		Last Modified: Sat, 01 Feb 2025 00:28:32 GMT  
		Size: 98.5 KB (98455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a194c3df9af8a1e0a0b0996e328ebc9d028e37d604943dd45fd43121f1577124`  
		Last Modified: Sat, 01 Feb 2025 00:28:31 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
