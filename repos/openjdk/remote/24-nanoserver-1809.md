## `openjdk:24-nanoserver-1809`

```console
$ docker pull openjdk@sha256:808de6296c599c4fc121f0c08ba89a10d3ab8ace3bc61f9761e94651ad88a6b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `openjdk:24-nanoserver-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull openjdk@sha256:334f80dc6c01c69695aaa832cad1ae8779d48741eec2a1f50bad5832268d9d45
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.7 MB (367676660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95b1c5764da5ea01e76b5f03e686a11603f024b7f49682eb4a5bbe17adce8b46`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Sep 2024 01:02:10 GMT
RUN Apply image 10.0.17763.6293
# Sat, 28 Sep 2024 01:53:45 GMT
SHELL [cmd /s /c]
# Sat, 28 Sep 2024 01:53:47 GMT
ENV JAVA_HOME=C:\openjdk-24
# Sat, 28 Sep 2024 01:53:48 GMT
USER ContainerAdministrator
# Sat, 28 Sep 2024 01:54:03 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Sat, 28 Sep 2024 01:54:04 GMT
USER ContainerUser
# Sat, 28 Sep 2024 01:54:05 GMT
ENV JAVA_VERSION=24-ea+17
# Sat, 28 Sep 2024 01:54:15 GMT
COPY dir:59fde22d333ab3856920abff671e860c3346f26584909cf660e6a76befb9ebb6 in C:\openjdk-24 
# Sat, 28 Sep 2024 01:54:23 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 28 Sep 2024 01:54:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a8b325bcb6d89afa770bc0d80d724a7529f3c8bdf940ab5418ad8d6b94fb07f0`  
		Last Modified: Tue, 10 Sep 2024 17:40:58 GMT  
		Size: 155.1 MB (155080848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18d21c9379a1977b98251ed10469ae8e713e070e3b67a7515fd35dc3ce1a2e3f`  
		Last Modified: Sat, 28 Sep 2024 01:54:28 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:633ea6e6f13065b85760c543d0ead8264cb04fc71ac9f96edaaeb18b07f978a4`  
		Last Modified: Sat, 28 Sep 2024 01:54:27 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2acc430a0e6d76f2dfd646e50e6a4711c12a807750f0383455354b5d4567ff76`  
		Last Modified: Sat, 28 Sep 2024 01:54:27 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4782d7e2daf128629952aa74c131e0e713e38d3319a4acbb3c7be9e348c92ad4`  
		Last Modified: Sat, 28 Sep 2024 01:54:28 GMT  
		Size: 68.2 KB (68156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48d5b41085b2ba44ea3ebb15252781344c7f4174333ea684a861e45cb4726f18`  
		Last Modified: Sat, 28 Sep 2024 01:54:26 GMT  
		Size: 1.1 KB (1117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df608ded0c6f5b8b7f0d5a531f7a4f3ef9d385bf4196a007bac4532395270a91`  
		Last Modified: Sat, 28 Sep 2024 01:54:26 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4380ad27d2d2daa9a02b437d64d3a0a78d66c538adee2e4b13a50e0c5269375a`  
		Last Modified: Sat, 28 Sep 2024 01:54:38 GMT  
		Size: 207.9 MB (207928961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc69db26a0a46f5fa1291bc603433a3286bf8a7cbff496b0ea564981d6638706`  
		Last Modified: Sat, 28 Sep 2024 01:54:27 GMT  
		Size: 4.6 MB (4592360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08bfb0d0f549b4e32aa7b8dcc45a61060d0bcde80beaf30085dce85c360167d8`  
		Last Modified: Sat, 28 Sep 2024 01:54:27 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
