## `openjdk:27-ea-17-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:eca567b9f073d201ccda253f0965fbeb9c6126e46f43dd83af996951d580b308
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `openjdk:27-ea-17-nanoserver-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull openjdk@sha256:2441173eaa4ebe86051004f844ccb1982f03239d488c5d2707cdad894bcd89c0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.6 MB (351634755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac14330d25af25f5a0acb01df48999018f322a28618e771fa8c614dc7c7c6724`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Tue, 14 Apr 2026 02:08:52 GMT
SHELL [cmd /s /c]
# Tue, 14 Apr 2026 02:08:55 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 14 Apr 2026 02:08:55 GMT
USER ContainerAdministrator
# Tue, 14 Apr 2026 02:09:08 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 14 Apr 2026 02:09:09 GMT
USER ContainerUser
# Tue, 14 Apr 2026 02:09:10 GMT
ENV JAVA_VERSION=27-ea+17
# Tue, 14 Apr 2026 02:10:54 GMT
COPY dir:0691f65abcad9aa5e8b70bfb251a5fc900e0d4cf82de17dca757301a739d34d1 in C:\openjdk-27 
# Tue, 14 Apr 2026 02:11:03 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 14 Apr 2026 02:11:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4791039a28038e31988b509d67caf387f82be83001f1422e84d1563e4b0007be`  
		Last Modified: Tue, 14 Apr 2026 02:11:10 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d783c6e0785183bd59e686005bca5a796c63d0bc2baaa4f079028376fffc471`  
		Last Modified: Tue, 14 Apr 2026 02:11:10 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b2a2079a615a0ade82edafcb0bf13f0332fe470c612faebe85aeadef22b96c`  
		Last Modified: Tue, 14 Apr 2026 02:11:10 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a705e2d8e8ee143e5e2937ba0a1fdcef21d95f24f719fc620dc07d0423b145`  
		Last Modified: Tue, 14 Apr 2026 02:11:10 GMT  
		Size: 70.3 KB (70343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9786a7b6c6dc26f212eb94bd404aef3f0bef93d20686557b414b3852d75db66`  
		Last Modified: Tue, 14 Apr 2026 02:11:09 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d18d5bb82719ecd64a18caf016c010ef19c7e15c99e9f0d18a9421a159b479b`  
		Last Modified: Tue, 14 Apr 2026 02:11:08 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7040f20f64cc83ae59381d34e7464e468f26c2b6246a4888a7b19c30c2a6ae13`  
		Last Modified: Tue, 14 Apr 2026 02:11:24 GMT  
		Size: 224.8 MB (224811387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:490fea1d20db26d88d2c14b31ce5b7ee1ffbbef5c0d8b68ed9676e3afd43d131`  
		Last Modified: Tue, 14 Apr 2026 02:11:09 GMT  
		Size: 96.1 KB (96135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c12205a4c6c62deea7b7363f4b2d4e450dad290e3cc6dd1d698437fb90a0f2a`  
		Last Modified: Tue, 14 Apr 2026 02:11:09 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
