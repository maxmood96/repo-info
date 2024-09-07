## `nats:scratch`

```console
$ docker pull nats@sha256:2f17324034f4e30c0c9cd64cc6201b75b6cb157bc93497a65802d2e3de065d3f
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
$ docker pull nats@sha256:d1176625176b038634a1d26c3318402d1e90e8182b84c0a15066f9976df4d3cd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5404593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef470af6831eaea797989f8792a895712972098273c0f919072cbadc562ca603`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 23:28:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 06 Sep 2024 23:28:39 GMT
COPY file:ac658fb12bcdb7cd40b3d3097ffcfa78f50d46d96774dc02c9d195773d7e52ba in /nats-server 
# Fri, 06 Sep 2024 23:28:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 06 Sep 2024 23:28:39 GMT
EXPOSE 4222 6222 8222
# Fri, 06 Sep 2024 23:28:39 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 06 Sep 2024 23:28:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c41b4b2468a159241e30133cd5adbf7c2191d7b5b854b67bfa47620944ceccd9`  
		Last Modified: Thu, 29 Aug 2024 22:50:10 GMT  
		Size: 5.4 MB (5404086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b88ff4b780b6c5dc8199c2fbc771ac2544acbaf40432a1f2cd77d707db0ceb4`  
		Last Modified: Fri, 06 Sep 2024 23:29:23 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:19c0572ce33bf9f915b08f320469e20af05afa2381ad84ed62fccce39e19a58f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70c53db195a414d8b4da69a9a9a79b66e2b22f6e1228978376218ce3853c088`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:58:38 GMT
COPY file:74a10207a3902ee396bbb792050b9696deba77249109c95ab9371918b138a9ff in /nats-server 
# Thu, 29 Aug 2024 22:58:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:58:38 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:58:38 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:58:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6531d64beb656b90d0588ca1e9ee5baa9b31c60c43b92a162e8650afc24e7066`  
		Last Modified: Thu, 29 Aug 2024 22:59:21 GMT  
		Size: 5.4 MB (5397937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18a539f2c989b9dd07de8fc0804fdc3e205851c58cca1876c944bb5ecd5e92b`  
		Last Modified: Thu, 29 Aug 2024 22:59:19 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:ba7822e542a94faf6af1dcec9a916b16e1b1263a9a2ba6402c48501bd416e119
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5303788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a4baeefffc6b16fee272be8679dcdb682415879b6e683a8bbf5a6f53d0ee676`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:40:03 GMT
COPY file:c5d4b3d47c26488975afc541176b56cf7c6ccd7f3e5d0200f303d12268a852eb in /nats-server 
# Thu, 29 Aug 2024 22:40:03 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:40:03 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:40:03 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:40:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:09bddb13d9e64aaa6ab3394fe0d1b088ecfd0b7270b519276a9ecf02865cdadf`  
		Last Modified: Thu, 29 Aug 2024 22:40:43 GMT  
		Size: 5.3 MB (5303280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f745d4d198c9120853c8182bbccae4912dd657b26c7d5d1c25a1ae37ca143f6`  
		Last Modified: Thu, 29 Aug 2024 22:40:42 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:66094b9e4c2415278e45d8310a46d4173bc4e7464e57ed9b4e0e2c84032ca0d9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5599459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb71815fbcdc0c9c8a6fa7b5a343c44b57ba690102e20f670496d00c280ba6d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:43:08 GMT
COPY file:03c3fc08b74c712c3e71bd1c81d9242c4307ba294e3b35b6e2299d163dcbe7dc in /nats-server 
# Thu, 29 Aug 2024 22:43:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:43:09 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:43:09 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:43:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2e62649b495d16f1d94e1bf73a6fe201307f62a2f5a8d5d462108462cbe0ad05`  
		Last Modified: Thu, 29 Aug 2024 22:43:47 GMT  
		Size: 5.6 MB (5598951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bdc7b959a53c76211ac1612f90cf81dd154ce2e9d544d0d214d5310e6da40a`  
		Last Modified: Thu, 29 Aug 2024 22:43:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
