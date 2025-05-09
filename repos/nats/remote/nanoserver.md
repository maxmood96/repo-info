## `nats:nanoserver`

```console
$ docker pull nats@sha256:2ae730ef67555c3028bddfce6bca43830d80040ab573d611e5cda2e6dabfa6e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `nats:nanoserver` - windows version 10.0.17763.7249; amd64

```console
$ docker pull nats@sha256:8417f8bbf0ce1644b9edf44c65ecfced6ac24408b7eff7c390cebcd1d387c992
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.2 MB (115237192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cf35061184d45bbf893c8b149eef5983bba0785a1c10e8a45976bdbae0ca6f6`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Thu, 01 May 2025 16:47:54 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 01 May 2025 16:47:58 GMT
RUN cmd /S /C #(nop) COPY file:597800b942878c0dcccccdeec13566a54f5747a8b41cbc437b6c383be7c26c87 in C:\nats-server.exe 
# Thu, 01 May 2025 16:47:59 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 01 May 2025 16:48:00 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 01 May 2025 16:48:01 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 01 May 2025 16:48:01 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65886e4bc86839428ebb3594aa57119afe4f6e2b0b2c4893307d4c34fdb386d2`  
		Last Modified: Thu, 01 May 2025 16:48:05 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ca77e35d8dbb1edb4f4de2b6a4f0480bcc7295778c9b1c61e772a921d47de15`  
		Last Modified: Thu, 01 May 2025 16:48:05 GMT  
		Size: 6.5 MB (6478821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deb2786d37a62d2495660d9a38f9bdbb36c84856895bf5ba0adae35dd44e5e21`  
		Last Modified: Thu, 01 May 2025 16:48:04 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2654cee3140e59825c237b4d656aa7ca726756428feda8cbf56491a79a62ad39`  
		Last Modified: Thu, 01 May 2025 16:48:04 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc2c0d17001c7a0a4c5f6d89bedd97f81d9944bad261987178826573d37549ea`  
		Last Modified: Thu, 01 May 2025 16:48:04 GMT  
		Size: 1.1 KB (1088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8e6963ed08110da1a824e61ca4f5bbe320457796a1b0bc6e4c4c7324cfb7ea`  
		Last Modified: Thu, 01 May 2025 16:48:04 GMT  
		Size: 1.1 KB (1090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
