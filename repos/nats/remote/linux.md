## `nats:linux`

```console
$ docker pull nats@sha256:617b967545bf6e4f3b75cec41dfc37bd734544b4b4c33e3d9ee0da38dce161ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:92e7f9daede2d9f0bf0fb19ee9edbda0bb6f3d67d51fcaf7a0ea3a753f2a550c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4565653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7e4065a82a64422de8554705cef94cee44d57d142a8faeac26a705c22a167cb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 13 Oct 2021 16:13:46 GMT
COPY file:077f50be0de271ffda1008ecf0034a9197edf920d88c8b7acb4705e440055c58 in /nats-server 
# Wed, 13 Oct 2021 16:13:46 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 13 Oct 2021 16:13:46 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Oct 2021 16:13:47 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Oct 2021 16:13:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c78225a573bcf3c390263b8c87be5c2e84312bb59c28d935337b10784b2f26b6`  
		Last Modified: Wed, 13 Oct 2021 16:14:42 GMT  
		Size: 4.6 MB (4565176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb63e48ce7d1ea5803409d74f576817497e48d850a274d4aa8f8bf3abb8060e`  
		Last Modified: Wed, 13 Oct 2021 16:14:41 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:93693c23ea5644f401a72bf6929214e9dfd2720b1b4c373025e689c1495de5a4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4228700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a1d37c768b08a19ab2b56aff52bc2bd23a18c665a38568b80d03d43b91ebe1d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 12 Oct 2021 23:50:02 GMT
COPY file:87c492688776372ccf80f66cfc3e90fd8fab44035811506c7aaa232e547e000b in /nats-server 
# Tue, 12 Oct 2021 23:50:03 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 12 Oct 2021 23:50:03 GMT
EXPOSE 4222 6222 8222
# Tue, 12 Oct 2021 23:50:04 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 12 Oct 2021 23:50:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cd12bdf7a9a23f7457d02e8fc11f170382a386c0eeca79fe881fb322825f1a9`  
		Last Modified: Tue, 12 Oct 2021 23:52:26 GMT  
		Size: 4.2 MB (4228225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d6a7556bfb5d88c2ff5e698fcd012e06a282a35550cc4944de84fe772a4481`  
		Last Modified: Tue, 12 Oct 2021 23:52:23 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:d2e70b8a1a863ae0f789502434cef995627ed0f46f551f291f2f7a0ff7017642
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4213288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3787a15077edfb6d8fa1646ed439c24cc005849fcf8311a629d20c8679d8b139`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Sep 2021 19:47:57 GMT
COPY file:6d69eef0d821da908da152f3dfe853b07d173db35f1c40a85e545d8218aaeb7e in /nats-server 
# Thu, 30 Sep 2021 19:47:57 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Sep 2021 19:47:58 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Sep 2021 19:47:58 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Sep 2021 19:47:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c67bb3b32b6353245cbd27e1ee30c47b5cf8b7c76346ca37875fa7cc7086cf7e`  
		Last Modified: Thu, 30 Sep 2021 19:50:22 GMT  
		Size: 4.2 MB (4212814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065d109fdaff0adc51732a8f449fee6ffda396a8e2a53cda9273482aa1fb36f0`  
		Last Modified: Thu, 30 Sep 2021 19:50:19 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:2475df2d82899c998486ff164f63c549ab94f3ec9d6b6ced5f1a828feb097cbb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4170004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd70c0c61ec57441666601ccff002d189c00d3ecb3a1eb1ea97f052736bee1b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 24 Sep 2021 17:40:34 GMT
COPY file:9b757ffadeb4943a3ca6c78d9caf65891c08587f5bebf5be32974d1456afb89e in /nats-server 
# Fri, 24 Sep 2021 17:40:35 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 24 Sep 2021 17:40:35 GMT
EXPOSE 4222 6222 8222
# Fri, 24 Sep 2021 17:40:35 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 24 Sep 2021 17:40:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7d0e0caa3737fe1355285d221e0c8e078337a45e1506022ffc37197d044d1db3`  
		Last Modified: Fri, 24 Sep 2021 17:41:58 GMT  
		Size: 4.2 MB (4169531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f509df5c28970b2ba96c7084c68158896b7fcbf5faf2d170a8d8e61960294c8`  
		Last Modified: Fri, 24 Sep 2021 17:41:57 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
