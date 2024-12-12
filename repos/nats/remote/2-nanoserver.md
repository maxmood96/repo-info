## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:7d831354b8e7f9e4fed417e35c0e0b4a1aee3a79673791b6a16d533a4ae282f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.6659; amd64

```console
$ docker pull nats@sha256:a88b3f498a7f07122ffa03d32896f42f6ffb92c907afbb92beda0ee89a89eb04
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161264166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff0d464873e73abc47c3694c376e9a542426f6bcf3627932fbec103c39021be`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 04:54:21 GMT
RUN Apply image 10.0.17763.6659
# Wed, 11 Dec 2024 21:48:29 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2024 21:48:31 GMT
RUN cmd /S /C #(nop) COPY file:30d04105f2ee103eeaefb4dfeda74eb010a83b5e5fa9197d530ae8b0c97bf56f in C:\nats-server.exe 
# Wed, 11 Dec 2024 21:48:32 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 11 Dec 2024 21:48:33 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Dec 2024 21:48:33 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2024 21:48:34 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fc1cdf36537340b1875b5d6573a58a268fc20b63dc54a780f9070e51cf9eb9ca`  
		Last Modified: Tue, 10 Dec 2024 21:03:34 GMT  
		Size: 155.2 MB (155231618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:850c388750e1f4e2366ccb4c6665a6bd5e7bfa16c852e14b30c987846749ba89`  
		Last Modified: Wed, 11 Dec 2024 21:48:37 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43aa683f8715dbbad428641410ab7d3ca80b5d3eed2f40471f3d903c64b10d1`  
		Last Modified: Wed, 11 Dec 2024 21:48:37 GMT  
		Size: 6.0 MB (6026729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39f7f3bc05485b97240369056bba7e041384e47c57e3a11c29f02096f8ebfeb`  
		Last Modified: Wed, 11 Dec 2024 21:48:36 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccff8ae3529b8bd2b07d7ac97fa6046b6105e4b0bb0f0888a87e216274aff189`  
		Last Modified: Wed, 11 Dec 2024 21:48:36 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54f76e1dc1617c4a21f55ee55083fa4f52bb8b1e66d2162918413f5764b654c`  
		Last Modified: Wed, 11 Dec 2024 21:48:36 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e07b0e22e50619b175cebb49631701f59e6ce9a1a00f2bd4df055a9efae27026`  
		Last Modified: Wed, 11 Dec 2024 21:48:36 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
