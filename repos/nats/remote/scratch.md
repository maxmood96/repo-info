## `nats:scratch`

```console
$ docker pull nats@sha256:1cc0d69cf362f2481381fed452ff0c7a664f8ca1fa99cd07fac30f8dc20586ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:scratch` - linux; amd64

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

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:da851c45cfe95a52ab3e6b013241c2e5271d28f7c0b136f1047c108fbabf859e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5347023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c2ed2be6ead45418e9fc8d5da88a292fcbb6879e7dcc4db9126a45c5176f6d7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 22:49:33 GMT
COPY file:0aba91b853d0eaf7d63d52b084d7546996e8db198a221ad2c77a29c916538108 in /nats-server 
# Tue, 21 May 2024 22:49:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 22:49:33 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 22:49:33 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 22:49:33 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e0e2aa814926dd6fcdc968764287dbba28f195a391d5ef6383057be5ff7f60d`  
		Last Modified: Tue, 21 May 2024 22:50:24 GMT  
		Size: 5.3 MB (5346515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772a5dc6e4bbb9f932bcf1232f3a7830303a955bbac3775e90153ce66ac9bd8d`  
		Last Modified: Tue, 21 May 2024 22:50:23 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:c655a24000047ea7fc1f1c8c4b1e9c282ac92e2d9706d5aaec92934ab55b72b6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5338015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb15c7fb2d9a1f5c89f39c7be34daef5e45d98f6454a74e07c7051a7e9223370`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:03:59 GMT
COPY file:ed3148eb9af051d444f42876fc76b54a26455984f4a53bbdf1058b0e11e8b336 in /nats-server 
# Tue, 21 May 2024 23:03:59 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:03:59 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:03:59 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:03:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9b7c9f79cc0b5fadd268a6afc358930f56c66b60358751ef77ef18f5e0e13a75`  
		Last Modified: Tue, 21 May 2024 23:04:53 GMT  
		Size: 5.3 MB (5337507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8193d445aa5ad5ea1f96740679c84ff3087a86b1d13258defc8bc3a21f395d18`  
		Last Modified: Tue, 21 May 2024 23:04:52 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:64d7152e25fd1648d59fe3fda7da9461723b0fa6905b144971bac30def679c99
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5233872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:850b1061eaa54e26469184edc02f606e471c4d9416a0a6bc6068251f90fc0c38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:21:31 GMT
COPY file:dc57eab26dd732b695752b0df8adf307bcbd19553cba75ac3ac2975e7d2cd86f in /nats-server 
# Tue, 21 May 2024 23:21:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:21:31 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:31 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:21:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:94ec6b53e66c8fcb745c43768f785b3b4877166276394c340184cf7174eb38e5`  
		Last Modified: Tue, 21 May 2024 23:22:24 GMT  
		Size: 5.2 MB (5233363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9af7d01d01fa2b520a97d19101ea36ea9b96e8124f2fdc1bb7076f976ab01ee`  
		Last Modified: Tue, 21 May 2024 23:22:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:d7f6dd76a8d365ac199d2e1767531fd74bf13cd2c78dba7ac042b8ed1937c4fc
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5215310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c128c5b164984dd4d70a48c9af0281112501c7ca458ff244d718d50a31dadb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 02:39:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:21:33 GMT
COPY file:e17294dc512d40e8e54498c73c890fd5204a41873c3567f7c18aa532ba727dc3 in /nats-server 
# Tue, 21 May 2024 23:21:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:21:34 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:34 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:21:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3554a35f86605472601753e787e946b0399c33611a4892aeed776bd0c951d04b`  
		Last Modified: Tue, 21 May 2024 23:22:15 GMT  
		Size: 5.2 MB (5214803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a45efcc2dc003ec8d53cb55ac8512bb7b4c35bcbd7a761991ef4c1b3147dfd3`  
		Last Modified: Tue, 21 May 2024 23:22:14 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; s390x

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
