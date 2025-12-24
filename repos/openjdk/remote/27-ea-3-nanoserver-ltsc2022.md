## `openjdk:27-ea-3-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:7b66315babfca35df843e64d2b8e077b7d4cd88fe5290fd606fc742028149d9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `openjdk:27-ea-3-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull openjdk@sha256:48a7e871906374cce263a6a109583e2c555d518aedbbaf205d6b815e1faa3d77
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.5 MB (350512682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6adad0a10708ce31921d43fc98d8e459f90e4171d72f47c04c425b27912b365`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Wed, 24 Dec 2025 06:14:45 GMT
SHELL [cmd /s /c]
# Wed, 24 Dec 2025 06:14:47 GMT
ENV JAVA_HOME=C:\openjdk-27
# Wed, 24 Dec 2025 06:14:48 GMT
USER ContainerAdministrator
# Wed, 24 Dec 2025 06:14:57 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 24 Dec 2025 06:14:58 GMT
USER ContainerUser
# Wed, 24 Dec 2025 06:14:58 GMT
ENV JAVA_VERSION=27-ea+3
# Wed, 24 Dec 2025 06:15:53 GMT
COPY dir:fd5bab190d0e23cab6ba3a5710a034aa8e7b3d18ea9d8ef51c8a34f9322814a7 in C:\openjdk-27 
# Wed, 24 Dec 2025 06:16:02 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 24 Dec 2025 06:16:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c9ca070baab1bf4c5eb21b86c4c67fb5a0d7bb1936e4ad37200cd8e6b7ab67`  
		Last Modified: Wed, 24 Dec 2025 06:16:30 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1028a1d301ec80077d341d4fb7dcfc450815b3dd5a44eb8805d7ffd5f770429`  
		Last Modified: Wed, 24 Dec 2025 06:16:29 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcfc23f3ebe9db058e457b405e51bc6aced29e708a958a4b60d59b8d03256d4`  
		Last Modified: Wed, 24 Dec 2025 06:16:30 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:618658c740c0a72b6283c57b04d6e0659e05504488aa64e844204fd0e5253c38`  
		Last Modified: Wed, 24 Dec 2025 06:16:29 GMT  
		Size: 70.5 KB (70513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f09e2aa9c7c633b01473b7cbb4e04841606e9a41cfa58163df04e5a32359a2`  
		Last Modified: Wed, 24 Dec 2025 06:16:29 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ffae1032297eb3afb5a1adca116590e19aea266bb68735e15910deacae73d86`  
		Last Modified: Wed, 24 Dec 2025 06:16:29 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c323f8eb1b674794dd84fb427e87b23ae505ceabff42ea59e3560801673a0beb`  
		Last Modified: Wed, 24 Dec 2025 06:16:35 GMT  
		Size: 223.9 MB (223925401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91d034c8efac37b7c8f6a7fe4648fec8c1ef10f7cad2ec25e5b94eebfa189b69`  
		Last Modified: Wed, 24 Dec 2025 06:16:29 GMT  
		Size: 152.1 KB (152062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0f3b09dd1821f8514c6d1226e7150d1a17d5c5c37215384c9ea4fea9cd26d3f`  
		Last Modified: Wed, 24 Dec 2025 06:16:29 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
