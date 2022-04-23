## `nats:linux`

```console
$ docker pull nats@sha256:9addad33a841b1ca50669b2abe41b55d8d36358b26c33a9ab4d16277e0ac0d28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:e22bfb7fdf9006c8d295782e24a70c2197e340f216b649650ea67288ef841319
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4580124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:913890b0a2d48e5c381bcf8b123528904a57150fa69138277620e0ff995dff8b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 22 Apr 2022 16:22:23 GMT
COPY file:3454a426bcdf428c59f748013f6bd917cddf529f8a5032532fee8e7783f2d5e4 in /nats-server 
# Fri, 22 Apr 2022 16:22:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 22 Apr 2022 16:22:23 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:22:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 22 Apr 2022 16:22:23 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 22 Apr 2022 16:22:23 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:804b81b2249803c39d50d8d9262ec5bdb230411989987b9116527a02dbf021a8`  
		Last Modified: Fri, 22 Apr 2022 16:23:12 GMT  
		Size: 4.6 MB (4579616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ebd8666e9d6549b9ab43c6349958c6dbb767c779117f02d727d356e3daaf3d`  
		Last Modified: Fri, 22 Apr 2022 16:23:11 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:bb39905ea888630c30250ffee5dc2c940c3b95d2a2898b74a7aa139a7007f159
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4238093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ce28f90865945806936cfae5ee78d8f2f2598db1ac7086ad1929992f0b3c3a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 22 Apr 2022 16:50:00 GMT
COPY file:3de61978a9e8a2b166b752a33898d5f146479cdb1ce6ed9df10727fe98f55f51 in /nats-server 
# Fri, 22 Apr 2022 16:50:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 22 Apr 2022 16:50:01 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:50:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 22 Apr 2022 16:50:02 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 22 Apr 2022 16:50:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a90933979a2530bf92d8ed3112add5a8debe6da238f9becc07b90b414323e402`  
		Last Modified: Fri, 22 Apr 2022 16:52:22 GMT  
		Size: 4.2 MB (4237584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd95754400d2efb409a2eeed76406fade3b92c929c465f6a5c2189183a4e072`  
		Last Modified: Fri, 22 Apr 2022 16:52:19 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:c73d094a3eecc53745106d79abcf92f7f2c4959f2c7a607aa8a02aaecf2adc92
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4232128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d797593dddfb2960ff1bd893323d195aa2e61be166f83abcae8693f1f538cf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 23 Apr 2022 00:08:29 GMT
COPY file:91842064305817f2463830e9925a5bf281c10fa892125e096aa8c52cd100a677 in /nats-server 
# Sat, 23 Apr 2022 00:08:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 23 Apr 2022 00:08:30 GMT
EXPOSE 4222 6222 8222
# Sat, 23 Apr 2022 00:08:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 23 Apr 2022 00:08:31 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 23 Apr 2022 00:08:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4ca5997c585d7b90d306ca9e3facb866e5a008db5cfbecedf401e3de574c4445`  
		Last Modified: Sat, 23 Apr 2022 00:10:52 GMT  
		Size: 4.2 MB (4231620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a7a0c9aabdc2939a750f95344dfaf1abde695b5028a9ee42e0b11353fa7c91`  
		Last Modified: Sat, 23 Apr 2022 00:10:49 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cc2a7ab98b1adfcf8b16328efe3416e98bbed6146cffb9289d48b7f1d710f399
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4217735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd22baaa9b7fcf519609324f45785cad127c98aa25e6945ec3bd9144c6b100c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 22 Apr 2022 16:40:25 GMT
COPY file:a82c07c2e7d51d414d1e87aec6f9d2718447b772505fba86d5ea7617fc1992ac in /nats-server 
# Fri, 22 Apr 2022 16:40:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 22 Apr 2022 16:40:26 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:40:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 22 Apr 2022 16:40:28 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 22 Apr 2022 16:40:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:308394282a0e57ba139c96f20347213771c895947b7f9625212d7d91ac26cffd`  
		Last Modified: Fri, 22 Apr 2022 16:41:46 GMT  
		Size: 4.2 MB (4217229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a021323d331516d6b6519db1b4d42a2e922c74d6a39588a87e4859c26a9bd85`  
		Last Modified: Fri, 22 Apr 2022 16:41:45 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
