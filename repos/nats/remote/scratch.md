## `nats:scratch`

```console
$ docker pull nats@sha256:2be97fe6d850acdbf489f22d1a91206b09fb14e959e0c47a41aa84df8dc6617a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:35ff92bfc7e822eab96fe3d712164f6b547c3acffc8691b80528d334283849ab
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4535346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:165538b9f99adf71764e6e01627236bc7de03587ef8c39b621c159491466465e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 27 Aug 2021 03:35:09 GMT
COPY file:c88c76fcaa944eb4751e2b3c987b59dd654a42db7426be2223f22a0698cd6e5c in /nats-server 
# Fri, 27 Aug 2021 03:35:09 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 27 Aug 2021 03:35:09 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Aug 2021 03:35:10 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Aug 2021 03:35:10 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d96e79a5881296813985815a1fa73e2441e72769541b1fb32a0e14f2acf4d659`  
		Last Modified: Fri, 27 Aug 2021 03:36:00 GMT  
		Size: 4.5 MB (4534870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04479ea8ab2597ba1679773da48df06a9e646e3e7b67b0eb2c8c0bc6c51eb598`  
		Last Modified: Fri, 27 Aug 2021 03:35:59 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:b21057f1f945b501d03cf3c5c2d530f7961e1a3198e00bb297b7f69a849cc0e9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4210290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:865dcd8a77138e8339293c7089adeee440305e68331df5533186ea36b8132f84`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 09 Sep 2021 23:50:15 GMT
COPY file:a60049eef2da0cbda1255e229e5e5c6377e3c3445b0cd16ce13a272139c7ce85 in /nats-server 
# Thu, 09 Sep 2021 23:50:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 09 Sep 2021 23:50:17 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Sep 2021 23:50:17 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 09 Sep 2021 23:50:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b95232e9c9c31dfba5a6124fb74b4abc750a3fd6d5f89a13438a0b051430299e`  
		Last Modified: Thu, 09 Sep 2021 23:52:42 GMT  
		Size: 4.2 MB (4209813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2c01128246ad2a36efed9386a5ed63a01f73f3f56e54d059834ac17a2f64a48`  
		Last Modified: Thu, 09 Sep 2021 23:52:38 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:f2057644b631cd588b9ef8800c17a98848297ef9e8b14e896c6637c419716372
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4196286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4e34b9a7771c2092b58b5d6f99401eee0374e56201d34a1c7f84d6f53c05428`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 27 Aug 2021 04:12:30 GMT
COPY file:6576d0950936fbd8cd0ba8e9a7c8094950f25bd1a90d55b60e3e65ea2042854c in /nats-server 
# Fri, 27 Aug 2021 04:12:31 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 27 Aug 2021 04:12:31 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Aug 2021 04:12:32 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Aug 2021 04:12:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d135e76e7d6d665dbc290a175c8ae8ecfb2ca0aa9f3a2ba24b7dccf731e64cde`  
		Last Modified: Fri, 27 Aug 2021 04:14:54 GMT  
		Size: 4.2 MB (4195812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc14281759482e956b9f087159fb1610c9a80c3fe13daec5850693cafea3d3d`  
		Last Modified: Fri, 27 Aug 2021 04:14:51 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:24f192937e7bc371f7c2631055e49a51d489659d28f55b4fdf2eb5a19843a5ae
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4158958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd8bb7e96599c9badd4424f86ef2d5f8561cfa0c4a4322057847c002da643a9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 09 Sep 2021 23:40:25 GMT
COPY file:eda8ae8779fbfb7d34c95bc93fc8ce409cbd298cb302284f61ee4ebf6ac10b0e in /nats-server 
# Thu, 09 Sep 2021 23:40:26 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 09 Sep 2021 23:40:26 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Sep 2021 23:40:26 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 09 Sep 2021 23:40:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0c0083faeb4bd1e89eefb7cbc2a5556eb056acaba6107a833c271a1ca7cd8633`  
		Last Modified: Thu, 09 Sep 2021 23:41:48 GMT  
		Size: 4.2 MB (4158481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4227e148c1053ae9735f2dcc2ab35b83566aab7b85aa3d50395ec15be4630e26`  
		Last Modified: Thu, 09 Sep 2021 23:41:47 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
