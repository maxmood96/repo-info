## `nats:scratch`

```console
$ docker pull nats@sha256:0bec8cacca6439c410dc887f37401e3911bfcbb982f9012f33065d5ca3c86daa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; s390x

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:8e0d7c2f8e1a704b5a1510a9b792965e80df98c23266790f403c12a7e4b334a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5501340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce61e33cb4a8d130b0bb7871e706ccd2897ae03b3b77a43a733ff1364582c913`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 18:26:32 GMT
COPY file:a70beb4afc760b4eb620b77324ac11877e2d745bc4b21651e5f559167412340a in /nats-server 
# Thu, 11 Jan 2024 18:26:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 18:26:32 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 18:26:32 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 18:26:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:08d3ed80ce681bf0a8f2508582bd2ef4aa2dd9939984a992fd90ef1418b10450`  
		Last Modified: Thu, 11 Jan 2024 18:27:32 GMT  
		Size: 5.5 MB (5500831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64eee350ffa42c18b6c993b56ed7c2d44e1b73b9a6dc2ab17cd2babda5258ef4`  
		Last Modified: Thu, 11 Jan 2024 18:27:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:5d0d4af172e08fcb077acc722a291563bb4246cdc721f75e42741cbeadd9b01e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5219028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa461205d8d06abdf4b7afbc36edef28268cff127eca59c15781a21abdc05a44`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 17:54:58 GMT
COPY file:e0407774ec3be35d2e808ec5e153a35f02fee37376866bb6739551963e9d6d12 in /nats-server 
# Thu, 11 Jan 2024 17:54:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 17:54:58 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:58 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 17:54:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cac40ef0b21a2de49f6f818ce65744412272bb468bb3dca1cc5c716b2a6ee378`  
		Last Modified: Thu, 11 Jan 2024 17:55:42 GMT  
		Size: 5.2 MB (5218521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b62cc0a6c2abe679eec457a613170aa1795e9ce68d30456aa09b60970b00a0c8`  
		Last Modified: Thu, 11 Jan 2024 17:55:41 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:7b67d3baf5a1e10dbecb7b5514f42d73dce5d50450ceb708c3fa574b2893c430
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5210852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:609cc3c36f05c3ff3e3f4e1e67b5bb40e09138ef4e5f6abc6934e14cf521a2c3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 19:14:56 GMT
COPY file:d6340439c8d5766d4955e469bbaca54df62ba032566e17bab50e50e403cab1a0 in /nats-server 
# Thu, 11 Jan 2024 19:14:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 19:14:57 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 19:14:58 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 19:14:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c113f4984cb6e8b3483ce21ba872b78202b3b2eac11c724c47edad86810ce001`  
		Last Modified: Thu, 11 Jan 2024 19:16:02 GMT  
		Size: 5.2 MB (5210343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36ef6cc09b8153069eb28379b61acacd4a0f45729f233c8b9d4ecfbd48337810`  
		Last Modified: Thu, 11 Jan 2024 19:16:00 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

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

### `nats:scratch` - linux; s390x

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
