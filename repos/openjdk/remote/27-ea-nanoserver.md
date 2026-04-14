## `openjdk:27-ea-nanoserver`

```console
$ docker pull openjdk@sha256:59ae7b5e0e4b7d7c348a228fdc11c77a4250560ef0b1d4d1ba3aac29de3ae411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32522; amd64
	-	windows version 10.0.20348.4893; amd64

### `openjdk:27-ea-nanoserver` - windows version 10.0.26100.32522; amd64

```console
$ docker pull openjdk@sha256:7b7f4768fe38503bfcebbc32595197496d8bc545504119090a0a4872e3f870a9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.4 MB (424402210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a268790e18a74e85cf34da17e8f18ebdeb3c52c1b3b5b8c99323aa7c9d2a244c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Mar 2026 01:45:55 GMT
RUN Apply image 10.0.26100.32522
# Tue, 14 Apr 2026 01:49:59 GMT
SHELL [cmd /s /c]
# Tue, 14 Apr 2026 01:50:01 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 14 Apr 2026 01:50:03 GMT
USER ContainerAdministrator
# Tue, 14 Apr 2026 01:50:21 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 14 Apr 2026 01:50:21 GMT
USER ContainerUser
# Tue, 14 Apr 2026 01:50:22 GMT
ENV JAVA_VERSION=27-ea+17
# Tue, 14 Apr 2026 01:51:34 GMT
COPY dir:0691f65abcad9aa5e8b70bfb251a5fc900e0d4cf82de17dca757301a739d34d1 in C:\openjdk-27 
# Tue, 14 Apr 2026 01:51:44 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 14 Apr 2026 01:51:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:06fab7822816d5f43d6835d07ac8db280fdf81384187f36d8dc43bbb7064a76d`  
		Last Modified: Tue, 10 Mar 2026 20:41:46 GMT  
		Size: 199.4 MB (199409325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91da1d89d7b84e207bc76ccd6265075c393fdd33fa2042b7897589954a7f8fb8`  
		Last Modified: Tue, 14 Apr 2026 01:51:51 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cd0d830657bf28567229111aab08bb039012ca2d87dc3457601a3f589c100aa`  
		Last Modified: Tue, 14 Apr 2026 01:51:51 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a00f6f26fa3782083d24decc9799751f5b757f98701131781abe576b9323a295`  
		Last Modified: Tue, 14 Apr 2026 01:51:51 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b5416ea89c24d9ffcd369bdc3c2637d22a99597800ba6e32041aead7e5352e`  
		Last Modified: Tue, 14 Apr 2026 01:51:51 GMT  
		Size: 70.6 KB (70597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:338778a3ca711138a21148b61d4e98691119f9c4c074b6b3c95a659a72848614`  
		Last Modified: Tue, 14 Apr 2026 01:51:49 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f299641552201f88c0d230353fc890c283b1a3aebb31d297c911b3470db2e7ea`  
		Last Modified: Tue, 14 Apr 2026 01:51:49 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea10634e93c23a7adf15fdd55735300424e06e1c20bd1666a35064788aaacfb2`  
		Last Modified: Tue, 14 Apr 2026 01:52:04 GMT  
		Size: 224.8 MB (224811669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d39e094fbe3051da7bf59e8a5915b1e6b623bf7214481c02bf23495d388d088`  
		Last Modified: Tue, 14 Apr 2026 01:51:49 GMT  
		Size: 104.3 KB (104269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef9cd8ee3d254ba37a982360f1c2859142ae26776d244d5748d0ff93b923d66`  
		Last Modified: Tue, 14 Apr 2026 01:51:49 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:27-ea-nanoserver` - windows version 10.0.20348.4893; amd64

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
