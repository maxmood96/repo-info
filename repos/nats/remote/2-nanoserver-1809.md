## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:836d18514ec5f462a05c29c37bb15d17bcc06d1f1ad3340f7fed8d036a6bb974
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:2f1adf696cb6bdf7754db60127cf2cd325ffbb2216b79a6a028437d2f2c8cd28
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110198122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:928a969a7ad85cd53ec4f5c8c726fbd460bd08b5bf95fe9922a4e6eb91e184aa`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 00:14:05 GMT
RUN cmd /S /C #(nop) COPY file:fc393f320d6ee1aed79e267d10a974b4a909e644d8da91a00b7860f174eacb86 in C:\nats-server.exe 
# Thu, 11 Jan 2024 00:14:06 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 00:14:07 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 00:14:08 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 00:14:08 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2709d5a04a12b60114def77faab6f397b3ae0ab2c8bfbadc074d319f1ad3bf`  
		Last Modified: Thu, 11 Jan 2024 00:18:05 GMT  
		Size: 5.6 MB (5600447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50aad73556f1a7888e6fb0027c710d0dfbced1a10b61024f9bd0e8b41797178c`  
		Last Modified: Thu, 11 Jan 2024 00:18:04 GMT  
		Size: 1.8 KB (1796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095bd67f48dc8b0b7c6ccb51b21043521a0cf4d3d9ce5802f897fafa30c0fcdb`  
		Last Modified: Thu, 11 Jan 2024 00:18:04 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5668632545ab35f5dc74883dc4df3d2d36d0a62e4a07f75c5c0b78ebf5f44d16`  
		Last Modified: Thu, 11 Jan 2024 00:18:04 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df2127036887316dce3332767b52cfeecbb23ffd90d457a8f1ea2103ad579e93`  
		Last Modified: Thu, 11 Jan 2024 00:18:04 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
