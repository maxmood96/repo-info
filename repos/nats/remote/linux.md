## `nats:linux`

```console
$ docker pull nats@sha256:4da96b2fa5da16b6660f43092d49bd57ffff27e46e1a761eb1522709e0f7bd6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:linux` - linux; amd64

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

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:f9c6f9abbead4a684c7b883f4a7452710aa092d1ed595ba0dbd6179372d0be63
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4668800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b361f078e342fdb327cb4f5b2914d500fb5670e8424ba7dc9f20ffb4fff3c68`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Sep 2022 23:49:35 GMT
COPY file:945dfac8719ced982d1230b42c4e21c20cfe1792458759d37bd8f34702b97d49 in /nats-server 
# Thu, 22 Sep 2022 23:49:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 22 Sep 2022 23:49:35 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Sep 2022 23:49:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 Sep 2022 23:49:36 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Sep 2022 23:49:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:de6a34af6a596d1c7b7537e42748d9178faf87b637f714573303791154838994`  
		Last Modified: Thu, 22 Sep 2022 23:51:04 GMT  
		Size: 4.7 MB (4668293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4d5a0f70821a3f8fc7b8b1111c2166c03c48d05ebc9ce0473931d1ca74a09b`  
		Last Modified: Thu, 22 Sep 2022 23:51:03 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:03a39590b94ba73f75c39970947a3ff276c7f37d7e6e8009ccf780251f6cbc81
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4660097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f35ae12fca7c133fb2e99616ac3d87777680804b3654472e9c4d78d28db4e965`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Sep 2022 23:58:10 GMT
COPY file:8333f5a10c97b92118357725370604074ebcfef54b0d6e7d818b8a5280ac8fee in /nats-server 
# Thu, 22 Sep 2022 23:58:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 22 Sep 2022 23:58:10 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Sep 2022 23:58:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 Sep 2022 23:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Sep 2022 23:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:131d7d99719c2d3afa300226a95a811f986eb26f05d0aa3bd08fda92824f90a7`  
		Last Modified: Thu, 22 Sep 2022 23:59:35 GMT  
		Size: 4.7 MB (4659588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40b4198acf76381af038bfd14e9332c1ccd3a7235889f327c2d387fbd44b1b3`  
		Last Modified: Thu, 22 Sep 2022 23:59:34 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:080acc4ece31f7fc871e35471f286e4991b8febfe1379f1fb6b1e0d6eac551ff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4494416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d3fd2d5a277619c0411f028a92dd0e001aaf241be51e3bfc66db595c651f32`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Sep 2022 23:40:22 GMT
COPY file:78383a44c18e587e522cc9799431581c891b0ef3afdf06dee4c7f7267ca8bde9 in /nats-server 
# Thu, 22 Sep 2022 23:40:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 22 Sep 2022 23:40:23 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Sep 2022 23:40:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 Sep 2022 23:40:25 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Sep 2022 23:40:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3708e85fb8eb51ba8efd3211608a7049a9714a9f0f6282c1d78fb3efc99abed8`  
		Last Modified: Thu, 22 Sep 2022 23:41:42 GMT  
		Size: 4.5 MB (4493908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee57fd3c887f07b3980dd16bfc149abfd66ce3cba86f7e877dfa055492cba071`  
		Last Modified: Thu, 22 Sep 2022 23:41:42 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
