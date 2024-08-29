## `nats:scratch`

```console
$ docker pull nats@sha256:94e1eaf45c054dbc930035e76b89e85eab6c266c17534b0d063ed8e3c032bc60
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
$ docker pull nats@sha256:26f9940ea550f1d389e8d5260fe185353829e6814d8805ee2541fb2b53d634e0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5739793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22356c9f54ceb0ddd41c5cfea9fb5c89b48993e9accd9781985a9a4418fb50f5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 22:17:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:20:17 GMT
COPY file:4d4c6bbcd202b388b8eff8cce9964b31d0997fc62cdae2adadfaa86026571621 in /nats-server 
# Thu, 29 Aug 2024 22:20:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:20:18 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:20:18 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:20:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:083c87973157a09ec07f0dd6dd5110ba9e1a57c6d647dc61514fb59cbb42da4a`  
		Last Modified: Thu, 29 Aug 2024 22:21:04 GMT  
		Size: 5.7 MB (5739284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f59b5522908b0b9758561c85eefef18f863ae2dd35ca41414aca4f16707c3b`  
		Last Modified: Thu, 29 Aug 2024 22:21:03 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:176b95c4062fd85702f49bbc78dff4b57edd5790245aa0e1c699cbbc49a35aa5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5404567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce9b022c686673449d9d2205da1b289ea73535dd7a7b89f741d7c074d73c5dee`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 27 Aug 2024 23:49:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 27 Aug 2024 23:49:30 GMT
COPY file:0f3043e78404aeee0c1926e22dfa81bcfe207f7abb098a6fdd2d33dcc6b4a1d9 in /nats-server 
# Tue, 27 Aug 2024 23:49:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 27 Aug 2024 23:49:31 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Aug 2024 23:49:31 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 27 Aug 2024 23:49:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:686fb205a38e15909f87592b273ac6008601d1223818c700942acbc8e4f54529`  
		Last Modified: Tue, 27 Aug 2024 23:50:13 GMT  
		Size: 5.4 MB (5404058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97e337c2b8e2c2d07a6e385a3e6583a3cc101056c653fb45ba772eb41e7c9b8`  
		Last Modified: Tue, 27 Aug 2024 23:50:12 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:61ba665ac13ca66df96588019703687bffc077d701860712a3aa0a93f9f4facd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5b7956b2f0b8e4fb51c8ee977b7ce4873427d0c5b884e9ebe8bbd50b43c9c0e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 28 Aug 2024 00:04:53 GMT
COPY file:c8ee0b15c325c5088e57b5e5492ee2c01695495a2b757a951121446d1ffd90b7 in /nats-server 
# Wed, 28 Aug 2024 00:04:53 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 28 Aug 2024 00:04:53 GMT
EXPOSE 4222 6222 8222
# Wed, 28 Aug 2024 00:04:53 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 28 Aug 2024 00:04:53 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1d6b0c5ddf29ba3a84a0793d5bfaeb7f563047168e1c12443dcdd930e32bd872`  
		Last Modified: Wed, 28 Aug 2024 00:05:39 GMT  
		Size: 5.4 MB (5397911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5683077b4071b5151ded7b9fcd9d271a5fc856551c6b94cc46b82d947dbb63fb`  
		Last Modified: Wed, 28 Aug 2024 00:05:38 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:61322136f4d8a9232e2cdb8ae5b736415bc201b07500855ee8aa49afeaaf326d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5303762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7f0dff002fd8334800d3cfbe204ba000d8b699d15c4c0989c77789199386b67`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 27 Aug 2024 23:39:53 GMT
COPY file:277590be7861f3cf15baf11372aae16f964b193d0d3a607e7ecc03b1cca74b9a in /nats-server 
# Tue, 27 Aug 2024 23:39:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 27 Aug 2024 23:39:54 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Aug 2024 23:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 27 Aug 2024 23:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1536caa8c610091658759b64913e3c0effbcb91887a17183434a4d54e3b5d937`  
		Last Modified: Tue, 27 Aug 2024 23:40:37 GMT  
		Size: 5.3 MB (5303255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446a6360be093c9b01286accbc4d319e4251d1b7d9c88aae3733850c2b87219e`  
		Last Modified: Tue, 27 Aug 2024 23:40:36 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:ea88a24f5ac53d55afe5c5c38d743675b1d3fa668aa486c7e84697d66f759bc2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e301c2dbf05db489d319a3743b1dc16d5d29a4b24c2b2bd5aff4a371d084304`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:18:10 GMT
COPY file:718222216801d1c2996467e7100b9f56c3c29518d4a649f841aec107d9d59201 in /nats-server 
# Thu, 29 Aug 2024 22:18:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:18:10 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:18:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:18:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d1d29609fe0a3017982bc88b4bba8c874dd1ed1dfd9129ad75b7379f1deb7a9b`  
		Last Modified: Thu, 29 Aug 2024 22:18:50 GMT  
		Size: 5.3 MB (5275207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c04e39e857f0741e987fd5be70bc340f797420da1de1fb5495945dd3ca174a`  
		Last Modified: Thu, 29 Aug 2024 22:18:49 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; s390x

```console
$ docker pull nats@sha256:c87088ebf4e79060a373a6c1f1fc60e7fecb9a41eb49637589e8e5a5c266b5f9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5599361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:661336d758f38c24ccb698eeade837b3d86090ebf7a7b1e1ad8c73ab4f52ffc2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 27 Aug 2024 23:43:10 GMT
COPY file:52551ec29ba6335f03c9bd2a9a5d4864865380a166065e08075334bcdfee5e35 in /nats-server 
# Tue, 27 Aug 2024 23:43:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 27 Aug 2024 23:43:11 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Aug 2024 23:43:11 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 27 Aug 2024 23:43:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7ddb84faf584ab5adad5c027a3864bb7818cff4333a74f7aa7192b3338f0cf6c`  
		Last Modified: Tue, 27 Aug 2024 23:43:49 GMT  
		Size: 5.6 MB (5598854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4bd06b12ff8a1a8df4ed6516a6a634fc3428de1ca1bd509a23e845b3b67004`  
		Last Modified: Tue, 27 Aug 2024 23:43:48 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
