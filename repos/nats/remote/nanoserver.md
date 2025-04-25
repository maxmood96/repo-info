## `nats:nanoserver`

```console
$ docker pull nats@sha256:8ad5e6770c1df7c06e37c1855692061a4dec81c3bc4d289d3873a4554aa94d14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `nats:nanoserver` - windows version 10.0.17763.7249; amd64

```console
$ docker pull nats@sha256:de296657002e12709da3c23acf58143be37a698131dc288d4cc2c0309d43f108
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.2 MB (115237047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb13670aa8a73fbb2b50a99b8f822097b91002c77c9e1a26d7b154316e88ca0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Fri, 25 Apr 2025 18:16:24 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 25 Apr 2025 18:16:26 GMT
RUN cmd /S /C #(nop) COPY file:5e3840af0e267b510d2e54914f636d4b01f954b096bf81d459cc821ca4b3b468 in C:\nats-server.exe 
# Fri, 25 Apr 2025 18:16:27 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Fri, 25 Apr 2025 18:16:27 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 25 Apr 2025 18:16:28 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 25 Apr 2025 18:16:28 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:971b95fc9f036b2ce06ef6f75c0142446cf388b3fba5797ae076811cae5833b6`  
		Last Modified: Fri, 25 Apr 2025 18:16:33 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be78d14ed5a916b3852e5c5b8f0c11c5ec282c35d533f16824dff33610aa794`  
		Last Modified: Fri, 25 Apr 2025 18:16:33 GMT  
		Size: 6.5 MB (6479002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4903b008a32f8cb1eec6d3c17a357bb5a5292b67abdefef767f778101422a266`  
		Last Modified: Fri, 25 Apr 2025 18:16:32 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48da8f54d5ccf3ef130af0a73b7b96919c2914ff036e75afef02bdbaa3434ad`  
		Last Modified: Fri, 25 Apr 2025 18:16:32 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae2a11075603c8b13618e5c581a166f4c1092208a1e0b6f6a1cd1cdd3e4d05d`  
		Last Modified: Fri, 25 Apr 2025 18:16:32 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9602c735353ba767b46b959a65eed16ad8ad55667c0a070c399b925fa4c2fea6`  
		Last Modified: Fri, 25 Apr 2025 18:16:32 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
