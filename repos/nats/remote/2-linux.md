## `nats:2-linux`

```console
$ docker pull nats@sha256:fbaad6757f783e35e2e1c17dbfaa01698a745a0b9da612b5ceb03b1125598a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; s390x

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:fa26beda8a3187ccefa47afcfe9ea6d0e2f40a57c8f64d70bd63c792d7973938
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5534991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aa17fbc9745c6d9a8844e1ab4bb411caac4d947976e573ea86772f7aa77fc94`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 03 Feb 2024 09:22:51 GMT
COPY file:c08da355ccf630687140908574051bdb27ddac7abffc43539f1c353a915995cb in /nats-server 
# Sat, 03 Feb 2024 09:22:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 03 Feb 2024 09:22:51 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Feb 2024 09:22:51 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Feb 2024 09:22:52 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:047025d894a82d5535fd2b9375a9afb4ee6cc12a2b1e4867be9190608b7d0e10`  
		Last Modified: Sat, 03 Feb 2024 09:23:46 GMT  
		Size: 5.5 MB (5534482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12bb1b76b38e15129b4ab3f2c13a8104a99b4fcef2c0a3e660b6aaae01fa1458`  
		Last Modified: Sat, 03 Feb 2024 09:23:45 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:bf131e69ab071b6f35b570adbc6e1cecd2bfe84b3266f6f90f65a608a4b93a43
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5251767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd385de8b290b9955080cae793cf6cc6035d37a033c7372f51b0f14ef3fd00d4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 02 Feb 2024 22:53:47 GMT
COPY file:4258d78e61f143bf9ab22c31b60d52274c67232f99da900403fa34fb76729fb5 in /nats-server 
# Fri, 02 Feb 2024 22:53:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 02 Feb 2024 22:53:48 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 22:53:48 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 02 Feb 2024 22:53:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6ca579f793deefb3bceddd7cc6434a1adce9d85d8fc09de9f54d543ea96b97f`  
		Last Modified: Fri, 02 Feb 2024 22:54:39 GMT  
		Size: 5.3 MB (5251258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a09cf38736260e7d6e66ea6a9f76ecfbce658e9595b92187e7a5c609e775e4df`  
		Last Modified: Fri, 02 Feb 2024 22:54:38 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:4d1b9adf07bca0383a20f3a21531b8d21b8b969c16b1f0598ecfba3348507df4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5243763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf13f9de87831135f176796dd8eabff25a62f3e951e6e65e4522dd6217976a1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 02 Feb 2024 23:26:54 GMT
COPY file:a5369e97852f33a5b160df764848008d4e49500d87a2e74a481b8edb12653e8e in /nats-server 
# Fri, 02 Feb 2024 23:26:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 02 Feb 2024 23:26:54 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 23:26:54 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 02 Feb 2024 23:26:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2f6811f2c3b47fd4f9bfbc306106cab5eaa4a76efcbfb405c5444c3cfca0dcbf`  
		Last Modified: Fri, 02 Feb 2024 23:27:48 GMT  
		Size: 5.2 MB (5243254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b28d09f0aa31c4843e0b7e128993c19c836b0ff361c9187632539ff1eb416a`  
		Last Modified: Fri, 02 Feb 2024 23:27:47 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:72b3850d5a9af2035c35513106c9f06bf73cca3681e78abd1cc95635edcbfa6f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5106107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb64a905fbeb688b0d47c8c50cb919729a44ec3bc9e3a6d4181968b0652e2fa7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 02 Feb 2024 21:54:18 GMT
COPY file:8296ec99f2edacbd26a36bcbea24c2220019685c80d72189ab30a4ead40b0a0d in /nats-server 
# Fri, 02 Feb 2024 21:54:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 02 Feb 2024 21:54:18 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 21:54:18 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 02 Feb 2024 21:54:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5b73c63f9aa24e1c550000ee6aab1b78e9bc25b97748ad58194fbfb6c6cf673c`  
		Last Modified: Fri, 02 Feb 2024 21:55:14 GMT  
		Size: 5.1 MB (5105599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9835428a911094e35ecc76ef5e5906af872d4c0923381656ac1d2e760789e181`  
		Last Modified: Fri, 02 Feb 2024 21:55:13 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; s390x

```console
$ docker pull nats@sha256:d0b84ed068b7f0fe00d5ab02f7a8bbb8ebaf90bf657c36463c76b41ac0d50ed8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5385103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69542e675992da4639da6f2c125c0d51560fd34f85b4de29815593a7136e3c38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 11 Jan 2024 17:54:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 17:54:04 GMT
COPY file:62b4ff865435762036d97cf7296ae4eb04b8fffbc5feee5da88fd1a6eca3e5c6 in /nats-server 
# Thu, 11 Jan 2024 17:54:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 17:54:05 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:05 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 17:54:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7224d41d2ed8555b103fcef1a66d70913eb475babd8b1dfea87c7fdfe6620f86`  
		Last Modified: Thu, 11 Jan 2024 17:54:45 GMT  
		Size: 5.4 MB (5384594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1588d0af47d5bdf74a41af3929e6ec39ddfeabb9aa5a13ffe9debfad15e51626`  
		Last Modified: Thu, 11 Jan 2024 17:54:44 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
