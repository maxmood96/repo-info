## `eclipse-temurin:24-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:c078e49711999a5061106513b4c47631d12ca04e5001d4954c4fe198f22e31f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `eclipse-temurin:24-nanoserver-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull eclipse-temurin@sha256:d03ec905c2af0c572ec248810352bf78b77184ca5f7582f1c1cef168ac95a0cf
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.6 MB (250601674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f466fd20884eb41ddc4ee6ee7251c5f5e1c49b1ec36d492fde9bb23558a0acf`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Fri, 18 Apr 2025 04:12:09 GMT
SHELL [cmd /s /c]
# Fri, 18 Apr 2025 04:12:10 GMT
ENV JAVA_VERSION=jdk-24+36
# Fri, 18 Apr 2025 04:12:11 GMT
ENV JAVA_HOME=C:\openjdk-24
# Fri, 18 Apr 2025 04:12:11 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:12:14 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 18 Apr 2025 04:12:14 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:12:20 GMT
COPY dir:82098476e422c0fd1b27846be91131b5a5073542830e51603132b80cd94d4318 in C:\openjdk-24 
# Fri, 18 Apr 2025 04:12:26 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 18 Apr 2025 04:12:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaaa7043bc969ffd10e73283f955d6a41ef6b4cc004dfaec79839e2c5e201890`  
		Last Modified: Fri, 18 Apr 2025 04:12:33 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c784adec165e2853397805404661a906451a492ceceed1b33c52e5825913412f`  
		Last Modified: Fri, 18 Apr 2025 04:12:32 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ec9b2136e68954d7a1c6c8e8b488b6450a5f02653a9eb63b17e3a03a8ccf50`  
		Last Modified: Fri, 18 Apr 2025 04:12:32 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3faa0ac4facd6bcbb529c6b71ef345a89551c460906353f8871618dabfe0ca`  
		Last Modified: Fri, 18 Apr 2025 04:12:32 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab36e2dd35a5a3a0ae469a69c596eeb82a7a63737bf475a21974ff16d029e9f9`  
		Last Modified: Fri, 18 Apr 2025 04:12:30 GMT  
		Size: 70.7 KB (70723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d04fc37255c2202e815e88873a4ed11f60974781e317e43719c45d908d11ecc`  
		Last Modified: Fri, 18 Apr 2025 04:12:30 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53c4947b164e13cddb0bd2293a11f7b7df70d8ddb4dc7a60adf62848b26440b`  
		Last Modified: Fri, 18 Apr 2025 04:12:40 GMT  
		Size: 137.4 MB (137355533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec0eaa25554856dd4582d7855999938d374d2e81dc7b686c6e710004e7aa923`  
		Last Modified: Fri, 18 Apr 2025 04:12:31 GMT  
		Size: 4.4 MB (4416931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:287a79f75770626b36b448b84bddb8844362830e5f5eeeac19a8ff463961f09a`  
		Last Modified: Fri, 18 Apr 2025 04:12:30 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
