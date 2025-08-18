## `openjdk:26-jdk-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:8e9fbf01efe06255994e32318a9fb92cd0f143b13292ff772f3aebfe457b3bfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4946; amd64

### `openjdk:26-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.4946; amd64

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
