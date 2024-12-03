## `openjdk:24-ea-nanoserver`

```console
$ docker pull openjdk@sha256:f06fad750cc224e004928798a04bedd773c0f7848262051d13f709196db0121e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `openjdk:24-ea-nanoserver` - windows version 10.0.17763.6532; amd64

```console
$ docker pull openjdk@sha256:8b4ef91dbf05efa3436a938c721bb8862772dd7797d7592594fdadf29dd5211a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.0 MB (368003563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6d44ad9dfb4c2c8633ba0555c61b1e5976d8c08eae6981e8415c3adaf78c16c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 01 Nov 2024 11:18:21 GMT
RUN Apply image 10.0.17763.6532
# Tue, 03 Dec 2024 17:09:41 GMT
SHELL [cmd /s /c]
# Tue, 03 Dec 2024 17:09:43 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 03 Dec 2024 17:09:43 GMT
USER ContainerAdministrator
# Tue, 03 Dec 2024 17:09:55 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 03 Dec 2024 17:09:56 GMT
USER ContainerUser
# Tue, 03 Dec 2024 17:09:57 GMT
ENV JAVA_VERSION=24-ea+26
# Tue, 03 Dec 2024 17:10:05 GMT
COPY dir:5a65a74b2351a3e4a2b57ddaf0a289b4eb4ddfcff5f66e45048e5c25b479eaa5 in C:\openjdk-24 
# Tue, 03 Dec 2024 17:10:12 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 03 Dec 2024 17:10:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b79a100b554b1ee5bf83d129fe624c0ddd7754edeaf1a1364fefbbf2ba3095c1`  
		Last Modified: Tue, 12 Nov 2024 20:49:39 GMT  
		Size: 155.2 MB (155214227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cda329230529a64299cd884b0c74386cc1ff6ef537cfa7b6328202ea8b171bc`  
		Last Modified: Tue, 03 Dec 2024 17:10:17 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:266981be8e30270654b34105f5be7cdc9927aa6877c92dbb614431e04dfa331c`  
		Last Modified: Tue, 03 Dec 2024 17:10:17 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7291b42d7be7be4bc4b8d02de26aee1a9501ca89a14b6cf8515714feea7c35e0`  
		Last Modified: Tue, 03 Dec 2024 17:10:16 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14d55bf4d6fe5ab464436613d12ee481aea4e9df606a543e3c3a4bfc384ba33`  
		Last Modified: Tue, 03 Dec 2024 17:10:16 GMT  
		Size: 66.8 KB (66790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b751085d2b073949f4012a2c7999fc534862aad5dbbc68797178ee6e8e90df27`  
		Last Modified: Tue, 03 Dec 2024 17:10:15 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc848ace08f057bf78608d0b4de050c758d82ec5b246f12bcaad2285afd4512`  
		Last Modified: Tue, 03 Dec 2024 17:10:15 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7e256b8c873d19040be3007d7f5e67f1e6b042f9d85f22d67a360ea4af6ed5`  
		Last Modified: Tue, 03 Dec 2024 17:10:27 GMT  
		Size: 208.3 MB (208339538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0e51b6bdabe9325ae45f749c24803714a195ea6727e263007a52dd3fb497c65`  
		Last Modified: Tue, 03 Dec 2024 17:10:16 GMT  
		Size: 4.4 MB (4376530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cab06e660cfc642c86a5b78bd59506d97318b71db02cae10be10e0618506c507`  
		Last Modified: Tue, 03 Dec 2024 17:10:15 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
