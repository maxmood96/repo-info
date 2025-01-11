## `openjdk:24-nanoserver-1809`

```console
$ docker pull openjdk@sha256:4449c817a74006514cb815acfdad45304b7720e8810be25ca4526f9a568c35cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `openjdk:24-nanoserver-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull openjdk@sha256:2fd2360ea6008d2a20618cc932c5904be631c06b36b08c9cd4632b22c7acdc34
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.2 MB (368156500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d78a0ed3264b231cbd3f057e61eb9c71e58f1dc798f27a403e5e15ccff6ca80`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Dec 2024 04:54:21 GMT
RUN Apply image 10.0.17763.6659
# Sat, 11 Jan 2025 03:08:45 GMT
SHELL [cmd /s /c]
# Sat, 11 Jan 2025 03:08:47 GMT
ENV JAVA_HOME=C:\openjdk-24
# Sat, 11 Jan 2025 03:08:47 GMT
USER ContainerAdministrator
# Sat, 11 Jan 2025 03:09:04 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Sat, 11 Jan 2025 03:09:04 GMT
USER ContainerUser
# Sat, 11 Jan 2025 03:09:05 GMT
ENV JAVA_VERSION=24-ea+31
# Sat, 11 Jan 2025 03:09:13 GMT
COPY dir:ad771fa0c4659d73c3b630b6d3ca25a6a36b0b9af26b2bc144bd47e6e5f888f6 in C:\openjdk-24 
# Sat, 11 Jan 2025 03:09:19 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 11 Jan 2025 03:09:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fc1cdf36537340b1875b5d6573a58a268fc20b63dc54a780f9070e51cf9eb9ca`  
		Last Modified: Tue, 10 Dec 2024 21:03:34 GMT  
		Size: 155.2 MB (155231618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b49e6f9d6fb9e7e09f4c6d292a305e8342d172f4cecb7d99010a20bf73cba6f`  
		Last Modified: Sat, 11 Jan 2025 03:09:23 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a30c35af605473f276c4f7385fe06205e40d0c31fad5493fba8ce99b7f31c9be`  
		Last Modified: Sat, 11 Jan 2025 03:09:23 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f075cc1110f51ef0bdce02a2d20206cced78416def690c86c731fe8230bd2e2`  
		Last Modified: Sat, 11 Jan 2025 03:09:23 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c077bc7e26e0333c85cac61bfdb83c4c84d061e8171a1b6e65fe5f8fdd7f1b52`  
		Last Modified: Sat, 11 Jan 2025 03:09:23 GMT  
		Size: 68.2 KB (68150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fcc060dd7adc32da999b50a10d4738925dae5fbac544cd21a5514f684b0990b`  
		Last Modified: Sat, 11 Jan 2025 03:09:22 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321e73c4fd83db9fc715adefa1d3df57f02bd2b059cfc56be5ecc6d65da822e9`  
		Last Modified: Sat, 11 Jan 2025 03:09:22 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:644b405a38ce4fc1c47d753969d969dae67c8913ddce93a68c661b4e14e87dea`  
		Last Modified: Sat, 11 Jan 2025 03:09:33 GMT  
		Size: 208.5 MB (208468005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25013194177e39206afee11e79a83894fd458db4f0cffd7fbd6b5dfe91de0a87`  
		Last Modified: Sat, 11 Jan 2025 03:09:23 GMT  
		Size: 4.4 MB (4382319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57cb26ab9b9b41190d4e661974eed1446d358c72aa1f42a4be9cf8775e646ade`  
		Last Modified: Sat, 11 Jan 2025 03:09:22 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
