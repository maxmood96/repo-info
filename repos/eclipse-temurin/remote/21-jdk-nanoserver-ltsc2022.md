## `eclipse-temurin:21-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:1c05ddd2fb95ebedf3c9646e1b08bcb7475d2f16749fef2e0635bb18fa8a68bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `eclipse-temurin:21-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull eclipse-temurin@sha256:a3c059c2b8cb6bc759389dac75bd0c7a2ee4c1ca48bbf832c8bb44fee359ee7d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.6 MB (328630325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785715e1a79dbc75bec34e427af004830d85a58de337c7772852dc1f5eac1a9a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Tue, 10 Feb 2026 23:31:16 GMT
SHELL [cmd /s /c]
# Tue, 10 Feb 2026 23:31:16 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Tue, 10 Feb 2026 23:31:17 GMT
ENV JAVA_HOME=C:\openjdk-21
# Tue, 10 Feb 2026 23:31:17 GMT
USER ContainerAdministrator
# Tue, 10 Feb 2026 23:31:20 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Feb 2026 23:31:20 GMT
USER ContainerUser
# Tue, 10 Feb 2026 23:31:47 GMT
COPY dir:a00a0ee8f4ae82aa8e2b5d2b9cb5c2941887de3e7b021ae64d7924c257e6915c in C:\openjdk-21 
# Tue, 10 Feb 2026 23:31:52 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 10 Feb 2026 23:31:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb00098d2863860ba1b3327ab48272351942fb5b8e4cec5a5a6e7eef49ce21be`  
		Last Modified: Tue, 10 Feb 2026 23:31:58 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee315d96e4a530af8f144d88610281d7834c69af5acae4df815441e6247d0cf`  
		Last Modified: Tue, 10 Feb 2026 23:31:58 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d312517244ea350388d9f89af8d4a6961681de5459dff31f14eb315f25e83b`  
		Last Modified: Tue, 10 Feb 2026 23:31:58 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66e355aa295c76e31c4f83760be4eb0677db88d4d2429f78f530fb12d360e328`  
		Last Modified: Tue, 10 Feb 2026 23:31:58 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb00e01f5006ce61e18a06b058baa3f743541d949b05445f387f2c5cf1e0c1f4`  
		Last Modified: Tue, 10 Feb 2026 23:31:57 GMT  
		Size: 88.7 KB (88723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd75179eb5565f87b1f2e0edf04fa47e84ee4fc108f3e7846ad59f6fef60d18`  
		Last Modified: Tue, 10 Feb 2026 23:31:57 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:694d824be8e5a403d37e5681340c3b622c6af29e4cbe0aff5381548fa28bae23`  
		Last Modified: Tue, 10 Feb 2026 23:32:10 GMT  
		Size: 201.8 MB (201752557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55515c7a0619321237df2b0e796ae1b45ae3580b73775f2bb3108b8fa50bef29`  
		Last Modified: Tue, 10 Feb 2026 23:31:57 GMT  
		Size: 136.9 KB (136854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:011ac1664a41955956c0e0b7b56ec9d70dd8ee4898f2182a1fd48d518169f7a8`  
		Last Modified: Tue, 10 Feb 2026 23:31:56 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
