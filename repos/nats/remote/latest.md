## `nats:latest`

```console
$ docker pull nats@sha256:236498b19ca0ef368dae3931043e7ff3e16b27facae33f3723aca5b7d8c6f97a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.3287; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:1e1cc1b80a618a109970e841dfa2962318c7348441312b0b7e8f6e64b8eb812f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4905632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebe06e372ca40928fec9bf0cb9cf9751265f2ea179229b34abf54b42ec3612b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 19:32:21 GMT
COPY file:cd9de75b794fafb19e20bcd172a0323670b10f2af792997a2f16906c4bf3fcc3 in /nats-server 
# Mon, 12 Sep 2022 19:32:21 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 19:32:21 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:32:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 19:32:21 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 19:32:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ae176e6d0980e9d32d62aab8bce6ee604abd3d7934666cf81bffbdc646275ce1`  
		Last Modified: Mon, 12 Sep 2022 19:33:13 GMT  
		Size: 4.9 MB (4905124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d318ae137e300d4cdce8f1358c0992a66798618c91487a34d8cd6f2d49b220`  
		Last Modified: Mon, 12 Sep 2022 19:33:12 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:118585c5efc972b7af723b603811e3146ee914a26b54bcb892c506e8080d2fac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4665258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcd239e963a20ee15d599802357bd7485cbf652b2c7a5d9c77d6485c07168bce`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 18:49:48 GMT
COPY file:37e0cdc4ef3cae050b7a622e477f07fea2b89f2849c5c229803b12157182aa73 in /nats-server 
# Mon, 12 Sep 2022 18:49:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 18:49:48 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 18:49:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 18:49:49 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 18:49:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5a54d3866fde0d65a287b5e00b2251f84936c27eed638ecef0fa1e8f95134bd6`  
		Last Modified: Mon, 12 Sep 2022 18:51:17 GMT  
		Size: 4.7 MB (4664750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2846c8f5d71bd80327105a167594ce9f72272f7c6a141cf378e206141a075ab`  
		Last Modified: Mon, 12 Sep 2022 18:51:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:a48ca64c022b50e4612f11b7b0bdf380e886ad449c8eb5a48624b2df386ceab4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4658073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d43328d44a144020547148c52c8b0e257f2553339a66f15912b23f9b377d646d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 19:04:24 GMT
COPY file:88b07716d72d7b053cbf196c5562712b60f9d8875ee610f10839774e5aa8fd5e in /nats-server 
# Mon, 12 Sep 2022 19:04:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 19:04:24 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:04:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 19:04:24 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 19:04:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fdc81c83bc1df58c4e224556b8224d1e7425add4047736a641d435c2097b7c10`  
		Last Modified: Mon, 12 Sep 2022 19:05:53 GMT  
		Size: 4.7 MB (4657565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:012d019d0dd61d6f41306e0a2009771e9b75625f46458973bd5db00d964d0d28`  
		Last Modified: Mon, 12 Sep 2022 19:05:52 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:09ddfc36cc0a08d6c04828f085c33c72e9641c712d6a0f1a78126e3267a10699
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4492569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f28d3ca7b6670d9a7ef545dae9da4b8dfb8cb06b7f35b0a1fb9db72eb9327038`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 18:50:22 GMT
COPY file:2793f903eadf963d049d95e6645a7fc0e41632a84eff5d1055bd4de285218751 in /nats-server 
# Mon, 12 Sep 2022 18:50:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 18:50:23 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 18:50:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 18:50:25 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 18:50:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:29ad82f04593c429e1ee6bf6c0c2687549bee49e553052bf5b67eec17de00f9b`  
		Last Modified: Mon, 12 Sep 2022 18:51:40 GMT  
		Size: 4.5 MB (4492060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138da13517dd9cec8dbf0a87e0ce1dc5c15dbde69247362fc9895c07830e7f72`  
		Last Modified: Mon, 12 Sep 2022 18:51:39 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.3287; amd64

```console
$ docker pull nats@sha256:9f9679f278fbf584992e8d8fabe26ce93bc8d3c91d389ecf5de5b1bd619886dd
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.2 MB (108165102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:784cb4438a6fb065a40e7dba2da39341d32b88fa5218b2eb38f0c7ade22c2c78`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 06 Aug 2022 18:08:38 GMT
RUN Apply image 10.0.17763.3287
# Wed, 10 Aug 2022 15:30:21 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 12 Sep 2022 19:19:12 GMT
RUN cmd /S /C #(nop) COPY file:58259134bc4aec3b0bb4a01151c496cd2e557bf985d41d1838cb10c3492958d3 in C:\nats-server.exe 
# Mon, 12 Sep 2022 19:19:13 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Mon, 12 Sep 2022 19:19:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:19:14 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 12 Sep 2022 19:19:15 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5c9d6483dab113d2d9b50fdf3156622aa2ec3d6faaed5664d15a5568032d1714`  
		Size: 103.2 MB (103204200 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a5df16ce106b092b5399678da04735c18584e4f99ea301691eb433072953e9a`  
		Last Modified: Wed, 10 Aug 2022 15:31:14 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:661370d9d27020e3da7fd87855fd46c4b84dcad2a7734c033fd5d58f7cc10d99`  
		Last Modified: Mon, 12 Sep 2022 19:20:04 GMT  
		Size: 5.0 MB (4954584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebeb8f020417c79d7f9a4b96a5b4d8461fb8005ccf0f9d2a2ab15d23270852b`  
		Last Modified: Mon, 12 Sep 2022 19:20:03 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319410bd22fd8059a26939aab07894fa611ce65503ce2b50d40ac33ec1fe3591`  
		Last Modified: Mon, 12 Sep 2022 19:20:04 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca7e2f36b209328be490059b4a70b5f7451c842a2354410f2644a49676f4995`  
		Last Modified: Mon, 12 Sep 2022 19:20:03 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b020f5e205db60854c94a796e92914eb10c1fba1edea565697247d23c21321`  
		Last Modified: Mon, 12 Sep 2022 19:20:04 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
