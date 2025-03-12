## `eclipse-temurin:21-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:24d8400633ad9e7487b778ebc01a2a752c91432f92000d87a67f51cb37dd8513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `eclipse-temurin:21-jdk-nanoserver-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull eclipse-temurin@sha256:d31df68726e3b9f2eceeb2c60653302185ae6e425438e2242cb9082750c6ae20
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.3 MB (312284750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f19af27b2d2e7be69a741890c921d087c5f4ebb0f2ac8d99a3190e248943e1`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Wed, 12 Mar 2025 19:20:15 GMT
SHELL [cmd /s /c]
# Wed, 12 Mar 2025 19:20:16 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Wed, 12 Mar 2025 19:20:16 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 12 Mar 2025 19:20:17 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 19:20:19 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Mar 2025 19:20:20 GMT
USER ContainerUser
# Wed, 12 Mar 2025 19:20:27 GMT
COPY dir:87fb2a3fe15bf051f07e33b0f4d627a83582ff5ee0a30a4b75036496ad24f723 in C:\openjdk-21 
# Wed, 12 Mar 2025 19:20:32 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 12 Mar 2025 19:20:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:633f59717174c850348fe3b434bc068593733d2346e5c6fbbe529aee63882d4d`  
		Last Modified: Wed, 12 Mar 2025 19:20:40 GMT  
		Size: 1.1 KB (1092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16104bba48dd3f262a1756ee0c39c520ec395044b6c17eec513018085d1a3a77`  
		Last Modified: Wed, 12 Mar 2025 19:20:40 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0482c5222d87fc37204d3c7ff8353d32d2e8295ef2d4c6841f228e54d033778`  
		Last Modified: Wed, 12 Mar 2025 19:20:40 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c03d2e2b3139f16c922e7661e82c9e2f8755efca961aa43df372a963a9ff885`  
		Last Modified: Wed, 12 Mar 2025 19:20:40 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97e8b1b7ee6a41bca3c51e594346839c0e5b2b0d820d6e236a634c24b970d106`  
		Last Modified: Wed, 12 Mar 2025 19:20:38 GMT  
		Size: 70.5 KB (70460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:533408626693c507c6339b2dee63b9025758cd2fca34256fa9535685385d257f`  
		Last Modified: Wed, 12 Mar 2025 19:20:38 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd289ee9eaf2cc98b0eea2f219c35ecc10acae4b99dc80831c609261348e213`  
		Last Modified: Wed, 12 Mar 2025 19:20:49 GMT  
		Size: 201.5 MB (201476126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ba3d812be4f32aad0f951e94e51a61bdf668d408b70f403bc5396c492e9593`  
		Last Modified: Wed, 12 Mar 2025 19:20:38 GMT  
		Size: 3.8 MB (3823839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c196135ca02bfcbd9d80724698d5bc2bfd0a48bd46a089118d2cf8564a4cdc`  
		Last Modified: Wed, 12 Mar 2025 19:20:38 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
