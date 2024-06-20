## `nats:2-linux`

```console
$ docker pull nats@sha256:0c16d0ae4810124d679d4d5b90428c647a9271aea6c2cca7e41875a2b27ad70b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:32e1e8abb5a8cfdf609faa5a42f8ac7a7c197bb505481a0f2ca8dec96c92fcef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5672973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4fed1eae653c9e468d6aab8948dfeed03248e5f67d2f2da27c630d7a1bd668e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 22 May 2024 19:46:57 GMT
COPY file:bde3b96323851506bdb8dee1a5c849f57fed0675a388571c8ae8bdb78fbb308f in /nats-server 
# Wed, 22 May 2024 19:46:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 22 May 2024 19:46:57 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 19:46:57 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 May 2024 19:46:57 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d79939f5589ddcdfe25deacd46470779a671bda9460d28dcc354413093601b95`  
		Last Modified: Tue, 21 May 2024 23:35:47 GMT  
		Size: 5.7 MB (5672465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:facc84a4e89ca7d5be0bf5171bf5436fd0b90af5d9e581180824a8e11137f006`  
		Last Modified: Wed, 22 May 2024 19:47:42 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:cdaef1917e97728209e2d31ad322ab062dd242d703a1107afb87a14f69c42224
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5347024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09a002d72561346cd80f81415b378fdb474d607e7890ee7c3842e80a6dc76d7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:05:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 18:05:28 GMT
COPY file:008e1f8859dbe07df9a3518ca5a4221602d13a6b648ffe9a29b2d00b629f16e0 in /nats-server 
# Thu, 20 Jun 2024 18:05:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 18:05:28 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:05:28 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 18:05:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e0e2aa814926dd6fcdc968764287dbba28f195a391d5ef6383057be5ff7f60d`  
		Last Modified: Tue, 21 May 2024 22:50:24 GMT  
		Size: 5.3 MB (5346515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a335ca1d1d74fac94ca3f1e18cacc14e4988b48dcc0bf71a6ad6b331a124dea`  
		Last Modified: Thu, 20 Jun 2024 18:06:16 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v7

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

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e5f9f78a2c4c5f0a7d38232239f5d2afaa03cf3a506155e952fc1b020ba4531b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5233871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bef3ac3fddade2f62d6dcf1dc867c7dfe53c9a930e48efd12c3a431bbbddd414`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 19:07:40 GMT
COPY file:f564da141e6306628e75d438342668cf55fdafa63094782cbe4449f5d6c98215 in /nats-server 
# Thu, 20 Jun 2024 19:07:40 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 19:07:41 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 19:07:41 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 19:07:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:94ec6b53e66c8fcb745c43768f785b3b4877166276394c340184cf7174eb38e5`  
		Last Modified: Tue, 21 May 2024 23:22:24 GMT  
		Size: 5.2 MB (5233363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ab7e76b355afe745179986de5020717321b38dae61b2b1bcaa587c3a1d6044`  
		Last Modified: Thu, 20 Jun 2024 19:08:31 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:a651b2d76541fa428ed0ca09c3bdd8c959684fa1f0e62a6c8c8771e963476c57
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5215312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdcdece433818613588c4b3b9dfb3c7a80da774a7e13ff9071787a657805b3c3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 19:53:02 GMT
COPY file:aeec7db8c859fc6772a1e71152ae0edf2fbb33888beee45ff6f537021682c368 in /nats-server 
# Thu, 20 Jun 2024 19:53:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 19:53:02 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 19:53:03 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 19:53:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3554a35f86605472601753e787e946b0399c33611a4892aeed776bd0c951d04b`  
		Last Modified: Tue, 21 May 2024 23:22:15 GMT  
		Size: 5.2 MB (5214803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7e6c0a75b1efcc5091e3d2e007c13249f5f153818300c138840287e6a6d29f`  
		Last Modified: Thu, 20 Jun 2024 19:53:37 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; s390x

```console
$ docker pull nats@sha256:1c85d5dd96f8e24bb928941e213d64cb7f634841e04009ab1224f0efbe26b65b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5536746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe4c51fa5803cfee1eaaafc771c418b91caeab0549fb33309918a892cbe39864`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 18:02:16 GMT
COPY file:0d0169a9305ddffbf54ee7393cdb2ab8fe694a4c7952574ebaeccc212cbf834b in /nats-server 
# Thu, 20 Jun 2024 18:02:16 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 18:02:16 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:02:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 18:02:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1bc7712db04e70325970d818ce3314c72e3e1a2e148f5c5a7d2378504e1a05f7`  
		Last Modified: Tue, 21 May 2024 23:22:11 GMT  
		Size: 5.5 MB (5536237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b37e5601e62dd96baed2c90e93a74897cf17cd435704ed61f758023d765100`  
		Last Modified: Thu, 20 Jun 2024 18:02:58 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
