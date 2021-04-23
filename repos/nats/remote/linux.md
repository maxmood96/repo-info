## `nats:linux`

```console
$ docker pull nats@sha256:efb7005aa69eae8c01d32f56cf0a229b54aaf15f486b3f0c39ce1de41f19ab95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:28d9b42f5045e931f540022b50d140778296614cc46fea7fedef50e26b1584e2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4225945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1080c373df8961fed31f1a39e28cc6c25d6795e0d7c3d561f2d379cf92def32`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Apr 2021 23:02:29 GMT
COPY file:9bb0ab90c22cd1ed787dfe4292c36984fd21bc48b2174ddad3b1e218161e3cf2 in /nats-server 
# Thu, 22 Apr 2021 23:02:29 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 22 Apr 2021 23:02:30 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:02:30 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Apr 2021 23:02:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:10c4c9fb12b776e55b0ea8d3264f808ccc5caffaf56114cb844d5cb09786a6f1`  
		Last Modified: Thu, 22 Apr 2021 23:03:33 GMT  
		Size: 4.2 MB (4225473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473fec5c1cde7c5433c3e027919086bdd598e029899936541b2ec21ddb7847b0`  
		Last Modified: Thu, 22 Apr 2021 23:03:32 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:a7a2c8f7194409c4dd75c93a6f9de11db1fc17bf1737db1c06240524e0b1858e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3895594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db1fb4c72cd0448a5ba37409b399e5f04057f31f629ec5be8445008c54972c7f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Apr 2021 22:19:49 GMT
COPY file:64e71cd1d2e9467abd40785edd59f9612f1881becc619f3bedb155000a247b80 in /nats-server 
# Thu, 22 Apr 2021 22:19:51 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 22 Apr 2021 22:19:51 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 22:19:52 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Apr 2021 22:19:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:238304e519d8648cca435478a5cebd819ed4063a311feaa2db6ec68565dde2d9`  
		Last Modified: Thu, 22 Apr 2021 22:20:38 GMT  
		Size: 3.9 MB (3895118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc7507e43fa5a0838f598dd2a7130b2a5a79aa79cd6a06a73a1836fc2e6d6b5`  
		Last Modified: Thu, 22 Apr 2021 22:20:35 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:7a8f74c069f07b3f0b1351bc3aa1e2894ecc216e60c645973dcc81d261801b1f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3891970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:369c32ee391f07aae82ebd5e96f68ab9f24da31ffc8c257980974aaae2c38302`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Apr 2021 23:02:41 GMT
COPY file:4b22e9e541a652ab24ae042aa5e507153db95686a925c860d8e1d0d6abad10a3 in /nats-server 
# Thu, 22 Apr 2021 23:02:42 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 22 Apr 2021 23:02:43 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:02:44 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Apr 2021 23:02:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:65dc194b502e4ec7533d01c0251af4373a42f1054f5dc600b8d4aa96c6697a99`  
		Last Modified: Thu, 22 Apr 2021 23:03:32 GMT  
		Size: 3.9 MB (3891497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12bcc4ebf70a26891fd7de222893f55bb8968e80212d8fdba06e24381f864e08`  
		Last Modified: Thu, 22 Apr 2021 23:03:31 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a8b6b6b66c99dbfca177d9c18db7748068af5b7b397ff6444bef7d8c5df1ba19
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3865538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd2844c33ced18f889b04345db4c42c57c97e38a0c8a922035c8e9833f3c3062`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Apr 2021 23:34:22 GMT
COPY file:7c26ed7ed2d57f80534f12bf79cbe9c116a73d781f8e5d610a54d82baca800a3 in /nats-server 
# Thu, 22 Apr 2021 23:34:23 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 22 Apr 2021 23:34:24 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:34:26 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Apr 2021 23:34:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3946fb3fc24631b9897efde5d957a63512d59c5745a8d0b8a4dca3171d07f77b`  
		Last Modified: Thu, 22 Apr 2021 23:35:18 GMT  
		Size: 3.9 MB (3865066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9203e1c4fb17a9b11e7579ecba8ba11004c1f5565dd8a2cd3d2fc45182152a6`  
		Last Modified: Thu, 22 Apr 2021 23:35:17 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
