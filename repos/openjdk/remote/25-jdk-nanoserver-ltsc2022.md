## `openjdk:25-jdk-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:82ffa73e73eaf21a622974899b3d8bfe134cf44378e4cffab361fde64cbab336
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `openjdk:25-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull openjdk@sha256:45f58d1c84e26081cd4f71cf5cc441f5f400967ddfb0e569b03bae1db847e4a0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.2 MB (328222285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a740c8022ac4a2552fb3e44a37a29c739d75c973ba762be34c03eba08cb0491`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 12 Jan 2025 09:54:50 GMT
RUN Apply image 10.0.20348.3091
# Wed, 22 Jan 2025 20:42:20 GMT
SHELL [cmd /s /c]
# Wed, 22 Jan 2025 20:42:21 GMT
ENV JAVA_HOME=C:\openjdk-25
# Wed, 22 Jan 2025 20:42:22 GMT
USER ContainerAdministrator
# Wed, 22 Jan 2025 20:42:24 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 22 Jan 2025 20:42:24 GMT
USER ContainerUser
# Wed, 22 Jan 2025 20:42:25 GMT
ENV JAVA_VERSION=25-ea+6
# Wed, 22 Jan 2025 20:42:32 GMT
COPY dir:f68a0a203262648eaad23f672eb21e06d231a686a9fcf56b24be2d2d46cfaae7 in C:\openjdk-25 
# Wed, 22 Jan 2025 20:42:38 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 22 Jan 2025 20:42:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fd3058b29fbd287119a2fa4d2d36a46fdee3bbada5fd9ef6f02f2d7d4cc143ab`  
		Last Modified: Tue, 14 Jan 2025 20:27:35 GMT  
		Size: 120.7 MB (120661554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc5f876bd8a40865f3cc1f4967bceedd5e640dd7d99702609b05a1cc4edda97a`  
		Last Modified: Wed, 22 Jan 2025 20:42:45 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e789547d9f527fef787d89a7770370750451cd74f9345c9aed25b1d4b52f519`  
		Last Modified: Wed, 22 Jan 2025 20:42:44 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff384d45483ee1d9655631355b7797f8ad0c70895db634f92fdf5282506d2c0`  
		Last Modified: Wed, 22 Jan 2025 20:42:44 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e493838bd4e01c12dbe319512b8c770599084043513708f407c6f9bc736d47fd`  
		Last Modified: Wed, 22 Jan 2025 20:42:44 GMT  
		Size: 77.1 KB (77066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7f168ec1438cb46bb802ada4743bc90f0e2fb2fb320cc3d38d3d3413e96954`  
		Last Modified: Wed, 22 Jan 2025 20:42:42 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51aec607aa499d782433512a2a984b62832206059005054a819ffb27a948741e`  
		Last Modified: Wed, 22 Jan 2025 20:42:42 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a118e1e12c5298497693fe99d942d9d099df91c08499e50521c3224ae0eeed1`  
		Last Modified: Wed, 22 Jan 2025 20:42:55 GMT  
		Size: 207.4 MB (207370104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:355d9693b817a66f4fd56aa3e638bd03eb94308367d5339417811ad0fd5c220e`  
		Last Modified: Wed, 22 Jan 2025 20:42:42 GMT  
		Size: 107.3 KB (107276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9131c67d3e2e17d7c5e95a4fd0b86d860f320da9004bede83f94fd51e10f8ad`  
		Last Modified: Wed, 22 Jan 2025 20:42:42 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
