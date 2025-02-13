## `eclipse-temurin:23-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:b290d6ba52ceb8cacf91fe612c44bbca9d73344e5d825a9976c00e898dc33277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `eclipse-temurin:23-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull eclipse-temurin@sha256:0d80ee0dc25da09b4ff2a0ec7bb3c3b91213ac0419756c52fa2183b17bbcb8f6
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.9 MB (329865333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5327a0013a3f43c20306c61c002627e6e8645f0a8a364053b995df1c4158188`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 12 Jan 2025 09:54:50 GMT
RUN Apply image 10.0.20348.3091
# Fri, 31 Jan 2025 02:11:37 GMT
SHELL [cmd /s /c]
# Fri, 31 Jan 2025 02:11:38 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Fri, 31 Jan 2025 02:11:38 GMT
ENV JAVA_HOME=C:\openjdk-23
# Fri, 31 Jan 2025 02:11:39 GMT
USER ContainerAdministrator
# Fri, 31 Jan 2025 02:11:57 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 31 Jan 2025 02:11:58 GMT
USER ContainerUser
# Fri, 31 Jan 2025 02:12:06 GMT
COPY dir:0c46af2d3f44e3815e12a14e71a026bbbb77855831f9730ea0c94836a2ee7de2 in C:\openjdk-23 
# Fri, 31 Jan 2025 02:12:12 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 31 Jan 2025 02:12:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fd3058b29fbd287119a2fa4d2d36a46fdee3bbada5fd9ef6f02f2d7d4cc143ab`  
		Last Modified: Wed, 15 Jan 2025 01:24:28 GMT  
		Size: 120.7 MB (120661554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4aeecee15c4932f6ccf5fced631f60493956d32c7e0907e902d8d9311660577`  
		Last Modified: Tue, 11 Feb 2025 07:14:39 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a167c645929beda61db7270444d293efb00fac015429d142994ac5e8137d995`  
		Last Modified: Fri, 31 Jan 2025 02:12:17 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46f0877cd2b07d3e52828d7a412f8231d8bb4d38c2d62ddb395e6f40d783e0eb`  
		Last Modified: Tue, 11 Feb 2025 07:14:39 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db7f9fccfc2d0db0fbd06fe8a73b54437f82fcd014bd791e2ec3bb74a8626a2`  
		Last Modified: Fri, 31 Jan 2025 02:12:17 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7918a2b505fa6cbafbc0e1a5669c9d1b1961837915671f1daa522e677539edb4`  
		Last Modified: Tue, 11 Feb 2025 07:14:39 GMT  
		Size: 72.5 KB (72470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:249d5ec76522032760e1cd0c754f7b3a7e3b620b1dacaaa9e8ddbbec995ad16c`  
		Last Modified: Fri, 31 Jan 2025 02:12:16 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8373a216a1d0ffac427364495484fb500c92cff1b4fd28db41e3c97f3d695fe4`  
		Last Modified: Tue, 11 Feb 2025 07:14:49 GMT  
		Size: 209.0 MB (209027942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d87aa2796f810eb953e30cf116c3cfb42cdfddb4b207d2971a21175254337ee0`  
		Last Modified: Fri, 31 Jan 2025 02:12:16 GMT  
		Size: 97.2 KB (97171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9b49b87896fcbdc80a873c334e44af1b44acca390d65822f713e1c720883d5`  
		Last Modified: Fri, 31 Jan 2025 02:12:16 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
