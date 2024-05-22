## `nats:latest`

```console
$ docker pull nats@sha256:baa58b815d814480ac53730f5130d418d729255b4d777e061c193599f4221b0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.5820; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:e07193ea8fcf8ae410f97d311f779f92149f970fcbb0b0e7ac8b2b4305a8e88e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5672972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:905978e0f86ce03a472031f938dbb5d82824228186a364ea9ca06e47d8d262e5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:34:54 GMT
COPY file:66fcac5cf0cfd76e1fc66b9f3b1086ada024b4366b874c394c710514342ad3b2 in /nats-server 
# Tue, 21 May 2024 23:34:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:34:55 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:34:55 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:34:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d79939f5589ddcdfe25deacd46470779a671bda9460d28dcc354413093601b95`  
		Last Modified: Tue, 21 May 2024 23:35:47 GMT  
		Size: 5.7 MB (5672465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8fe5c09e28b96796ebda8cc2a2436676df103b032bb2ce0213de8f77784486a`  
		Last Modified: Tue, 21 May 2024 23:35:46 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:9dc19c23861e3ce6e8e88ee73e3958da0bcd18a87555db4483de98488233fd3b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5347023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39acc1f24db69b12c0c78b69d765755b8dd525179e9b5f7c46c41912d05cfe72`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 22 May 2024 18:13:36 GMT
COPY file:008e1f8859dbe07df9a3518ca5a4221602d13a6b648ffe9a29b2d00b629f16e0 in /nats-server 
# Wed, 22 May 2024 18:13:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 22 May 2024 18:13:36 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 18:13:36 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 May 2024 18:13:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e0e2aa814926dd6fcdc968764287dbba28f195a391d5ef6383057be5ff7f60d`  
		Last Modified: Tue, 21 May 2024 22:50:24 GMT  
		Size: 5.3 MB (5346515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59834a85fd030a0e2de5b0256062a145d86ba2cc27ea20e7dd6ad115fe5ae292`  
		Last Modified: Wed, 22 May 2024 18:14:20 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:e3aa3be2c67194016b3f11276b1ba5d7099d61e00cd83b8cf6a2447367de0704
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5338015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee458741b6b2f61474f34a27770215e71e07d677698d2df0e74f83b168a9f61`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 22 May 2024 18:33:26 GMT
COPY file:9bd22b280d9474da700b413662ba97d86693461a656554c7d65e50aa664d72d2 in /nats-server 
# Wed, 22 May 2024 18:33:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 22 May 2024 18:33:26 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 18:33:27 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 May 2024 18:33:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9b7c9f79cc0b5fadd268a6afc358930f56c66b60358751ef77ef18f5e0e13a75`  
		Last Modified: Tue, 21 May 2024 23:04:53 GMT  
		Size: 5.3 MB (5337507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36381f89dbcb69410eaee4d31b42055ec46d797db481affddcb39bc62a9534d`  
		Last Modified: Wed, 22 May 2024 18:34:17 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:4f6fc8f497424d89e607cfb165023bd35408d3fbec8304ad5c2ee6f679beb22d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5233872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df8eb36225fb1a16cc99aed36b19b20e28df34370c0503e1059eb95ec21f6513`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 22 May 2024 18:57:04 GMT
COPY file:f564da141e6306628e75d438342668cf55fdafa63094782cbe4449f5d6c98215 in /nats-server 
# Wed, 22 May 2024 18:57:04 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 22 May 2024 18:57:04 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 18:57:04 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 May 2024 18:57:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:94ec6b53e66c8fcb745c43768f785b3b4877166276394c340184cf7174eb38e5`  
		Last Modified: Tue, 21 May 2024 23:22:24 GMT  
		Size: 5.2 MB (5233363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4d070e4c1e34577f1901cb71a0e8e00121235e70dd20dac6edaf0314dda1a4`  
		Last Modified: Wed, 22 May 2024 18:57:45 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; ppc64le

```console
$ docker pull nats@sha256:5b8d1fba767738da069b15e8a8994079a8fe04d05ba4eeb984789d5122754664
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5215311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6ae8b9b6416926cf64c00ed55999a9c01b1aebc605f17ad48a742b23fd741e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 02:39:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 22 May 2024 18:49:00 GMT
COPY file:aeec7db8c859fc6772a1e71152ae0edf2fbb33888beee45ff6f537021682c368 in /nats-server 
# Wed, 22 May 2024 18:49:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 22 May 2024 18:49:01 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 18:49:01 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 May 2024 18:49:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3554a35f86605472601753e787e946b0399c33611a4892aeed776bd0c951d04b`  
		Last Modified: Tue, 21 May 2024 23:22:15 GMT  
		Size: 5.2 MB (5214803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991491415cd5d43a93764a75256a8d811ae5149ffc154b27fe3d2f4f38f38805`  
		Last Modified: Wed, 22 May 2024 18:49:34 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; s390x

```console
$ docker pull nats@sha256:a9a0d93cb6a669f0fc2d842220f3a517c5c4ac5b345f0e2dc6aa8267c6fc76a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5536745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56c6e37910e564eec4963a6cbe0df805262ea12e504977a860f55fc52a39d05`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 16:58:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:21:30 GMT
COPY file:359d868ca3e4f687575abd568ad941a9d2682ed2ca604af3309b28b73679d2b7 in /nats-server 
# Tue, 21 May 2024 23:21:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:21:30 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:21:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1bc7712db04e70325970d818ce3314c72e3e1a2e148f5c5a7d2378504e1a05f7`  
		Last Modified: Tue, 21 May 2024 23:22:11 GMT  
		Size: 5.5 MB (5536237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0c0c15d382278c746e463dce4639563f785a5f07f552c8f5caceb88a87d424`  
		Last Modified: Tue, 21 May 2024 23:22:11 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:958a15d708d62f00bc9918e2283ecab5d12a85d54187bb5301593f33c452a6dc
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160734385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bceedc7adb4c9ed6737507c649ee6ff628321a49b2274fbed9b74f50ca19557`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Wed, 15 May 2024 21:08:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 21 May 2024 23:17:18 GMT
RUN cmd /S /C #(nop) COPY file:e634b8d8431824b53f95f04a1a787a66fac400f6b27037e57e00122926afdb6c in C:\nats-server.exe 
# Tue, 21 May 2024 23:17:19 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 21 May 2024 23:17:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:17:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 21 May 2024 23:17:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e15682c89e7337c581629534d634fb5bc56c6cea86ed0785b8309b2876701a`  
		Last Modified: Wed, 15 May 2024 21:13:34 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be448c0648b4e415641d5d7504a60f23cb03b4b00b0211021d9fbf697157d4ff`  
		Last Modified: Tue, 21 May 2024 23:18:13 GMT  
		Size: 5.8 MB (5786623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17add0d9ad6ce3c2580f4f65cc11d1d7c6eb572e2df535e9b7d1538394ef668e`  
		Last Modified: Tue, 21 May 2024 23:18:12 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c916da7655fd8a5653ae241bc5e9e7657b62c26bce65ae68453896906234d11e`  
		Last Modified: Tue, 21 May 2024 23:18:12 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696dcba679ec709b4b8fa95dcd27de7889439d88a304ac3770ac1e6f32f8010c`  
		Last Modified: Tue, 21 May 2024 23:18:12 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4a7a4b5fb58cd41e8b7478c971ce9a63da9d056aed725662939f3f108cc898`  
		Last Modified: Tue, 21 May 2024 23:18:12 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
