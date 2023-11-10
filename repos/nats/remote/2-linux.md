## `nats:2-linux`

```console
$ docker pull nats@sha256:9b762a502b622e230c9f28209a99fa42c02b210c141db7d69371af3f314d2cfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:13c8d74fcc1a65baf6183ffd2fb0e6bf203c1733604bce5ed976f92899c4908a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5482912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c915a3a784500564d97666dfd079f51bd760ec9381c8e37672164ee5a8814dd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 09 Nov 2023 23:20:15 GMT
COPY file:eb240b5bffcc0f613e659042b381fda542cd7e880986c213f55614d8c9cd276c in /nats-server 
# Thu, 09 Nov 2023 23:20:15 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 09 Nov 2023 23:20:16 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:20:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 09 Nov 2023 23:20:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cba24f033da718f2444230f64e704439d7f2b84fabfc969c8d76bb9384846971`  
		Last Modified: Thu, 09 Nov 2023 23:21:11 GMT  
		Size: 5.5 MB (5482403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e73b7f3a0e802d16548b50a27050fdfbbeeceab3baa40b4d8edcd30ce2e9e4`  
		Last Modified: Thu, 09 Nov 2023 23:21:10 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:3824d5a2eaced6fc383dd112f9aa4419e7b695f3e28bfd82b777c51e0ed4f05b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5198038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:426c60b316ede95784f2e76d75502281fac3810627f124e56407076cc6b24413`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 09 Nov 2023 23:49:33 GMT
COPY file:9170d5b0d1641eee9b12dc349f23f35eda534f163f4e0774c2065bd1c6a6454a in /nats-server 
# Thu, 09 Nov 2023 23:49:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 09 Nov 2023 23:49:34 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:49:34 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 09 Nov 2023 23:49:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0b806f760797ca6495655d6ab966c0c7eb478e31a9e10edd05a11d19849361e0`  
		Last Modified: Thu, 09 Nov 2023 23:50:20 GMT  
		Size: 5.2 MB (5197530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa083376696ef3cfa57138bcef07c661395d393e21c97b5c292916c586b1113f`  
		Last Modified: Thu, 09 Nov 2023 23:50:19 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:076db1c8274b6d3365971b0789c7f8a8a0681edfbac5d8957fd61b0b451dec53
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5190584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba964d20fa3e0e7612e094883ddbdfa4a2da08e5991acf12078d98e6b0b40ecf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 09 Nov 2023 23:57:51 GMT
COPY file:c2ac13057067603fc11d31bf35f44ec61100129c7bd0159bca62c9ad70ec0446 in /nats-server 
# Thu, 09 Nov 2023 23:57:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 09 Nov 2023 23:57:51 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:57:51 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 09 Nov 2023 23:57:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b415d8adad5189ef844c42b0a3f47fd89e72a26541b97ea226549fa147225c05`  
		Last Modified: Thu, 09 Nov 2023 23:58:40 GMT  
		Size: 5.2 MB (5190076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc460654454d2ed863a7f07f1c65e9e81729b7021d1eaf8f4502ed7b74c4b4f`  
		Last Modified: Thu, 09 Nov 2023 23:58:40 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e02c3b198a6cf4ae395748b57c79c0306c6cab08d6b6f2df1541bd50858f6973
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5055703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b84170acbecc01b9d59102d83553de280f88645ad50d89c083db5ff92ed5de6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 09 Nov 2023 23:46:27 GMT
COPY file:2c77c6a1a9d77db3770061afda23f8d949858d1478cac389c677692fcbd14f75 in /nats-server 
# Thu, 09 Nov 2023 23:46:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 09 Nov 2023 23:46:27 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:46:27 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 09 Nov 2023 23:46:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:42f19c7824138f7306c0dc9c7f18acfbaf351d86f0631725acff764dec1557e9`  
		Last Modified: Thu, 09 Nov 2023 23:47:16 GMT  
		Size: 5.1 MB (5055195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f96f43f0639ac050e05813fdaa230e83b8066636d9c1be745853c81ece9ac89b`  
		Last Modified: Thu, 09 Nov 2023 23:47:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
