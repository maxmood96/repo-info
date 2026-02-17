## `openjdk:26-rc-jdk-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:a8c61df64b521cb5fb537eded3dae54e6c66ded2bf396524d0644eb76830aad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `openjdk:26-rc-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull openjdk@sha256:2cc308cbf67e80dea5a17180acbd82dd2c5b0a97a9bfef86018eabaa2505076c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.8 MB (350760684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8649cd444750a91ab6927a8761c6a75b986ed58bea461fc215499dcf397e2502`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Tue, 17 Feb 2026 20:11:58 GMT
SHELL [cmd /s /c]
# Tue, 17 Feb 2026 20:11:58 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 17 Feb 2026 20:11:59 GMT
USER ContainerAdministrator
# Tue, 17 Feb 2026 20:12:12 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 17 Feb 2026 20:12:13 GMT
USER ContainerUser
# Tue, 17 Feb 2026 20:12:13 GMT
ENV JAVA_VERSION=26
# Tue, 17 Feb 2026 20:13:10 GMT
COPY dir:48d9a1614aae77abafeeb59360dca42b580c313456033330908c8e794bbb7778 in C:\openjdk-26 
# Tue, 17 Feb 2026 20:13:14 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 17 Feb 2026 20:13:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b9133238e3559d47b254a3443555b690c1c826f76a8aa04c2132fa0a227e81e`  
		Last Modified: Tue, 17 Feb 2026 20:13:26 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da864b46468a299f67f85f1b601d513c620a895794ef044103ead49f10b9c733`  
		Last Modified: Tue, 17 Feb 2026 20:13:26 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5310926f9234562a49802e83d7c45ae8a73c6d294e79db9ff48164c968d549a4`  
		Last Modified: Tue, 17 Feb 2026 20:13:26 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2326daa8cfc5f787121139010a5927b1505265610c4ae165b7aa5c3ffa57418`  
		Last Modified: Tue, 17 Feb 2026 20:13:26 GMT  
		Size: 71.8 KB (71819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81f2ab1289f2b20cc8011d0c0840710127db6790d0b566844506d6b0de094e6`  
		Last Modified: Tue, 17 Feb 2026 20:13:24 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3a4ca9c4d13709a447b263a4e97ab37c202561b5e1d0867023516011c3a29b`  
		Last Modified: Tue, 17 Feb 2026 20:13:24 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8087557568f6641a805a799768c14e8568363dacf026690779c48c7d43ad8e`  
		Last Modified: Tue, 17 Feb 2026 20:13:41 GMT  
		Size: 223.9 MB (223948930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1df0f354fa6642971a818d7ef76ff8566587f06404d1f2118150f14383cdb0`  
		Last Modified: Tue, 17 Feb 2026 20:13:25 GMT  
		Size: 87.9 KB (87874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:753ccce01c4702fdef76acdc2617a8a29093968c30704271e54a366c5fb5d5bf`  
		Last Modified: Tue, 17 Feb 2026 20:13:25 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
