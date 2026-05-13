## `nats:2-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:2b6839a0f95f211d134087d05f1c2b6985ffe28ad04ab158bedd18b7430ac79b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2-nanoserver-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:10447eaa252bcfb6c3c80118cac7a3b7d51c9a6498cc26d41dea1f72a29a718a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134088579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa19bee47e781cb629295ccf987910ba8172d206a2c5b755715734337341c77`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 13 May 2026 00:22:19 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 May 2026 00:22:20 GMT
RUN cmd /S /C #(nop) COPY file:04a1144166eb5b33184d353a4d7fcf95d121b39915427dc4374067d235aa4fae in C:\nats-server.exe 
# Wed, 13 May 2026 00:22:20 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 13 May 2026 00:22:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 13 May 2026 00:22:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 May 2026 00:22:21 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba58bc2ff4cb3ed55b80304b80b9c63f18f2df3aa65906a51c4228a916de113b`  
		Last Modified: Wed, 13 May 2026 00:22:27 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08ee7a8195af77f60f35ff2d6b86f9b83c3ea7a0787b41513b6d512a38cfbeb1`  
		Last Modified: Wed, 13 May 2026 00:22:27 GMT  
		Size: 7.0 MB (7043891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee6a61086d35b626fb6f16c1e6be5566b2c6cafc605ea3ffd8bb0131f0aa62cd`  
		Last Modified: Wed, 13 May 2026 00:22:26 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09595785c206d9c7108fdd885443f316708faa65baaa5229d4727c90dfeb7890`  
		Last Modified: Wed, 13 May 2026 00:22:26 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa49d51a826ee74af6afa6df4d7672be2e6d939ce87c78cc52903605ff9aa79c`  
		Last Modified: Wed, 13 May 2026 00:22:25 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd25503378a2c0fd04f5a847805ea1d9dca5b4ab6baef186823953f0b0b69d8a`  
		Last Modified: Wed, 13 May 2026 00:22:25 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
