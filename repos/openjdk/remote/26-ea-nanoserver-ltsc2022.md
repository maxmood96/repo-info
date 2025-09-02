## `openjdk:26-ea-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:9ace625a50061af571f18bcb135a6474f5568c24cd3c89546c6be0a0e206b4e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `openjdk:26-ea-nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull openjdk@sha256:74b0f911ce0e9142b31298ad446c90a0c46941e33e9dd5e56a65b2dc0ac3006b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.6 MB (341591860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9c79859b6bd859632ced704ddcc215e76a0e6d13443bc629b57ab881913975`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 02 Sep 2025 18:03:28 GMT
SHELL [cmd /s /c]
# Tue, 02 Sep 2025 18:03:29 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 02 Sep 2025 18:03:30 GMT
USER ContainerAdministrator
# Tue, 02 Sep 2025 18:03:36 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 02 Sep 2025 18:03:37 GMT
USER ContainerUser
# Tue, 02 Sep 2025 18:03:39 GMT
ENV JAVA_VERSION=26-ea+13
# Tue, 02 Sep 2025 18:03:47 GMT
COPY dir:08ed6392bbde5a6a9f4df62a4d13cd725bac341043a31a8c49758849f45c1fba in C:\openjdk-26 
# Tue, 02 Sep 2025 18:03:54 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 02 Sep 2025 18:03:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1608fb69ec834877c53973da3e2024776df5b6a35276cb5187bdae1f8ccd2f23`  
		Last Modified: Tue, 02 Sep 2025 18:04:43 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc9e6e68bebf5b722ffea5d06739f07488262f9ac09d1fa96005d261b1c4f1d`  
		Last Modified: Tue, 02 Sep 2025 18:04:43 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a0c669714f1065ddaa8312d31a0348a04209e8f7b1064be8e2d85100855b73`  
		Last Modified: Tue, 02 Sep 2025 18:04:43 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2631e3c1802a43155d88954fbbb67e149b3b3e89d7ffb922760da25bf02d5b`  
		Last Modified: Tue, 02 Sep 2025 18:04:43 GMT  
		Size: 73.8 KB (73833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbff9673a22f6eba653fe961b3fb3988b537c331775f79e2368900afb10fdfa6`  
		Last Modified: Tue, 02 Sep 2025 18:04:43 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b2515bdead523fd741e07e5063ea1d14176d0aa4f9c8def68a4f0b4cf90029a`  
		Last Modified: Tue, 02 Sep 2025 18:04:46 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29cbbfcf79c6332a62fe9c330311a9f52d8ffbebc18aedda596ca9e4bd83cbbb`  
		Last Modified: Tue, 02 Sep 2025 18:24:20 GMT  
		Size: 218.7 MB (218745061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba0abe3fa10b96429acdb1c29df730e2f3fa1f1d7a6de0a2d62719b483d23e3`  
		Last Modified: Tue, 02 Sep 2025 18:04:47 GMT  
		Size: 106.5 KB (106456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9e1daff97448c32a91e8067d8e1596db114d7a904ef34ae6133fff79d034c5`  
		Last Modified: Tue, 02 Sep 2025 18:04:46 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
