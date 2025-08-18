## `openjdk:26-nanoserver`

```console
$ docker pull openjdk@sha256:bacfbf8ea1421df0d7ac5c053c80b2e183434b60ae99c57dd9f18a6a8702d172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `openjdk:26-nanoserver` - windows version 10.0.26100.4946; amd64

```console
$ docker pull openjdk@sha256:61b8390c71c4773122f6546b2cffee10bc782ba189c674d6fc027cbdf4e6fd62
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.3 MB (412291263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:743d7020377516b85c2a5fbdbea53adeab8d50a2abdd77fbf90c6a5361464911`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 10 Aug 2025 02:44:20 GMT
RUN Apply image 10.0.26100.4946
# Mon, 18 Aug 2025 19:13:26 GMT
SHELL [cmd /s /c]
# Mon, 18 Aug 2025 19:13:27 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 18 Aug 2025 19:13:27 GMT
USER ContainerAdministrator
# Mon, 18 Aug 2025 19:13:29 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 18 Aug 2025 19:13:30 GMT
USER ContainerUser
# Mon, 18 Aug 2025 19:13:30 GMT
ENV JAVA_VERSION=26-ea+11
# Mon, 18 Aug 2025 19:13:38 GMT
COPY dir:09f4868e1f7c5ae8d19f1d7cad1a0f2936cafbde6923e47f6983d12823f358c0 in C:\openjdk-26 
# Mon, 18 Aug 2025 19:13:42 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 18 Aug 2025 19:13:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6d63d98dae9e3419e8c965c24a11d30e40947cf35ee17c204c5d8b7bae7ff2ef`  
		Last Modified: Tue, 12 Aug 2025 21:13:38 GMT  
		Size: 193.5 MB (193469373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c86cc14d0611f51585d6ce9f75b1136bb40e272e5b9c94265c6587578519ec8`  
		Last Modified: Mon, 18 Aug 2025 19:14:36 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94d80d3b3ce5761644109734f42cbbf88f6d39b25e268d32bfac87d77ff81784`  
		Last Modified: Mon, 18 Aug 2025 19:14:36 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b2cc500d1abfabd86f17dcbfa66d6130f9f9ce475b558ef49e567a5574c224`  
		Last Modified: Mon, 18 Aug 2025 19:14:36 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a351a0c391ac472ae020e4d8ba8f90472cf9cfba74e97195e452504bfda7b9`  
		Last Modified: Mon, 18 Aug 2025 19:14:36 GMT  
		Size: 76.2 KB (76182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff532839d2158aabae3813f290f595344e33d22b2bd19b4d2a65ed100a894574`  
		Last Modified: Mon, 18 Aug 2025 19:14:36 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:054650a6f1bd17815e2e7e8205511b7098345c24e4db772d1326085cfe7039cd`  
		Last Modified: Mon, 18 Aug 2025 19:14:37 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d43b5d4805920206386ea84297b13bacd6aea94465c9c2aced78daeeb018c9c9`  
		Last Modified: Mon, 18 Aug 2025 21:25:35 GMT  
		Size: 218.6 MB (218614952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d967611be5cfc3cf93290798488761f1de301d69a24286381ff0f1575266c83`  
		Last Modified: Mon, 18 Aug 2025 19:14:38 GMT  
		Size: 124.3 KB (124301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0689fe2b2aab6bd0316e728aa601a6934f5dd5f108f8061e7a2852b21e8587f1`  
		Last Modified: Mon, 18 Aug 2025 19:14:36 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:26-nanoserver` - windows version 10.0.20348.4052; amd64

```console
$ docker pull openjdk@sha256:def7cbc41cfa7fe5f58a9cc4bfbd40366c141448114893f369ffb4f62b07ade2
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.5 MB (341466897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b4066f83a070dd745df1d45d64638acf23710dd5e320d2e7dce250f29111fc1`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Mon, 18 Aug 2025 19:13:27 GMT
SHELL [cmd /s /c]
# Mon, 18 Aug 2025 19:13:28 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 18 Aug 2025 19:13:29 GMT
USER ContainerAdministrator
# Mon, 18 Aug 2025 19:13:32 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 18 Aug 2025 19:13:33 GMT
USER ContainerUser
# Mon, 18 Aug 2025 19:13:34 GMT
ENV JAVA_VERSION=26-ea+11
# Mon, 18 Aug 2025 19:13:42 GMT
COPY dir:09f4868e1f7c5ae8d19f1d7cad1a0f2936cafbde6923e47f6983d12823f358c0 in C:\openjdk-26 
# Mon, 18 Aug 2025 19:13:48 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 18 Aug 2025 19:13:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc5571bb3a397f57645df901022d541eb0d1cd81c154d3bff5c17ad51ee1bf0d`  
		Last Modified: Mon, 18 Aug 2025 19:31:53 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48cae7011f04bb6efab39a696e5ddc5db8ff8f93c5c2da77f27cea8a9882c6d6`  
		Last Modified: Mon, 18 Aug 2025 19:31:54 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26cc1fa446c208f1719c95a744ebf9f8f1a8d85c3d2deaf765c8b9475a5506d5`  
		Last Modified: Mon, 18 Aug 2025 19:31:54 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c90a26a5be78ee1b1fbb18f25a40a42b01e7d36edd6dd6f5b210d454f0d6385`  
		Last Modified: Mon, 18 Aug 2025 19:31:54 GMT  
		Size: 79.2 KB (79232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab82c88123b8792618b41fd1ddea96e3b1d22a1b955ab0f1d820ca10572c81f7`  
		Last Modified: Mon, 18 Aug 2025 19:31:54 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3997feadd5abdc972ffbaa2b4ec8cb069af526b3388eadce66ab55e4e017c67`  
		Last Modified: Mon, 18 Aug 2025 19:31:55 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8c966bb5968cf8af73ff45d7dae3abdb039f8359b0ac8f67a704a3c5da7398a`  
		Last Modified: Mon, 18 Aug 2025 21:25:38 GMT  
		Size: 218.6 MB (218613646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc0281e8299ff5ac0e7381d787d647fe489c89e74be1d61401098e2a3226053`  
		Last Modified: Mon, 18 Aug 2025 19:32:07 GMT  
		Size: 107.4 KB (107421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:735f28b3ba16245fc46d473b2d8196d7378c1f71667220be36655766397ac9fd`  
		Last Modified: Mon, 18 Aug 2025 19:31:54 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
