## `openjdk:24-ea-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:f91fbba84a87a977536accbf8816ab05ba0fc0181eba7544e94a3237c1ef658d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `openjdk:24-ea-jdk-nanoserver` - windows version 10.0.26100.2894; amd64

```console
$ docker pull openjdk@sha256:7eefcb0a6d2b7ea1d1c6a6a0e800b034f67ac54d5f3367eb31803997bfe29e2b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.8 MB (407763395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df6e775fb32ff3effc10fecd0739bca1c99933ac5a232822531712194ad63a9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Jan 2025 02:49:59 GMT
RUN Apply image 10.0.26100.2894
# Fri, 31 Jan 2025 23:31:45 GMT
SHELL [cmd /s /c]
# Fri, 31 Jan 2025 23:31:45 GMT
ENV JAVA_HOME=C:\openjdk-24
# Fri, 31 Jan 2025 23:31:46 GMT
USER ContainerAdministrator
# Fri, 31 Jan 2025 23:31:48 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 31 Jan 2025 23:31:49 GMT
USER ContainerUser
# Fri, 31 Jan 2025 23:31:49 GMT
ENV JAVA_VERSION=24-ea+34
# Fri, 31 Jan 2025 23:31:56 GMT
COPY dir:0417d4640b3e9898160c754927e6892a89119d4a6294484281d02c0d6a35e95f in C:\openjdk-24 
# Fri, 31 Jan 2025 23:32:03 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 31 Jan 2025 23:32:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3c572c5b651b10d04181f97ce4c0938b69ad43912e8c0bf19f77a4ea9a8f72e8`  
		Last Modified: Sun, 19 Jan 2025 13:02:58 GMT  
		Size: 199.1 MB (199054258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1533284ea2cfb38d5f1a798e284206322419ca11840e8403b3bd020b477b889`  
		Last Modified: Fri, 31 Jan 2025 23:32:07 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e19f50bb503a8d32b57fc8982a846c29e7d9c3e0a32f5a4cbaaeb7523aa9494`  
		Last Modified: Fri, 31 Jan 2025 23:32:07 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8efef181910acf74810f2561b8e91db55f1ddce1d07306721e501f4b1851e7f9`  
		Last Modified: Fri, 31 Jan 2025 23:32:07 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b26247b8ed4e361a61489ed13b5857fcea91f87ddee53f5b0904a0c5d54bd7`  
		Last Modified: Fri, 31 Jan 2025 23:32:07 GMT  
		Size: 75.8 KB (75828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a56ba5193300ad96e37ec759681bf710597919f2fa7d8b155589b52b80c667c`  
		Last Modified: Fri, 31 Jan 2025 23:32:06 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5949c97eb7b095f3ef8c6519e2c86aff72060a053c2bb0f949fc6e1508df787d`  
		Last Modified: Fri, 31 Jan 2025 23:32:06 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d04dbc1086d65bd9a5986f45c05977482b603c1b64a3b4a8a1dfd3c8db83d4`  
		Last Modified: Fri, 31 Jan 2025 23:32:17 GMT  
		Size: 208.5 MB (208534184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7219f4f081190d565794a456555fa9277e77f4af8341bd5720567fdf7a151bdc`  
		Last Modified: Fri, 31 Jan 2025 23:32:06 GMT  
		Size: 92.7 KB (92738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1231ac63740ff9464af912aba0861c68827b7d04895aeb382a0af4eb3eb6407`  
		Last Modified: Fri, 31 Jan 2025 23:32:06 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:24-ea-jdk-nanoserver` - windows version 10.0.20348.3091; amd64

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

### `openjdk:24-ea-jdk-nanoserver` - windows version 10.0.17763.6775; amd64

```console
$ docker pull openjdk@sha256:6becba0ec6c2e3bec4143b45db006214baaea98466a967279bb02c1c5cb03581
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.3 MB (368290739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68335dabcbaea2173fbe949372931498e76233969e5f32cd6b43206621235b6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Fri, 31 Jan 2025 23:28:15 GMT
SHELL [cmd /s /c]
# Fri, 31 Jan 2025 23:28:18 GMT
ENV JAVA_HOME=C:\openjdk-24
# Fri, 31 Jan 2025 23:28:18 GMT
USER ContainerAdministrator
# Fri, 31 Jan 2025 23:28:39 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 31 Jan 2025 23:28:40 GMT
USER ContainerUser
# Fri, 31 Jan 2025 23:28:41 GMT
ENV JAVA_VERSION=24-ea+34
# Fri, 31 Jan 2025 23:28:54 GMT
COPY dir:0417d4640b3e9898160c754927e6892a89119d4a6294484281d02c0d6a35e95f in C:\openjdk-24 
# Fri, 31 Jan 2025 23:29:01 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 31 Jan 2025 23:29:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Tue, 14 Jan 2025 20:45:12 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71a99c5ebd4604be337c7fb6e6cb45247b83cba51bbdc92c8bc6e9b6f9b24810`  
		Last Modified: Fri, 31 Jan 2025 23:29:06 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c4d8208345e4826977d57e36bd7985f0fd36b36a45a45cfdc2ca9d56f85b39`  
		Last Modified: Fri, 31 Jan 2025 23:29:05 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:617939baf63e87a8bf207f917e213b24794a798fbc744c50240844c3db578356`  
		Last Modified: Fri, 31 Jan 2025 23:29:05 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def3112b3583e5a4bbf414f9947f51eb136e573de78e0a736289b3d8aaac9070`  
		Last Modified: Fri, 31 Jan 2025 23:29:05 GMT  
		Size: 81.7 KB (81734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa0e96e02182b98cab8c9e2d390f0b013d48b675db9fa45a84a3e3b0227f261`  
		Last Modified: Fri, 31 Jan 2025 23:29:04 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8553526d363f93c9a2acfa09e58bd9e87ce94ea7698283a46835f6a7c864433f`  
		Last Modified: Fri, 31 Jan 2025 23:29:04 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963fa4fe915f76e0f99cb0eaeb5451b858d9d028fbe98441a2a3dd9e4ef137be`  
		Last Modified: Fri, 31 Jan 2025 23:29:15 GMT  
		Size: 208.5 MB (208532469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8cb451df3f3c45f09858c5f9ec62f469c3feec176df32ccc63de2b93743b4b0`  
		Last Modified: Fri, 31 Jan 2025 23:29:05 GMT  
		Size: 4.4 MB (4402621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62cdc86c81aa56273b46de2d3d6ec74adcee38bee7bfe165b5efcdeb5975861c`  
		Last Modified: Fri, 31 Jan 2025 23:29:04 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
