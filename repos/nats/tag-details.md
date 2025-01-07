<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats`

-	[`nats:2`](#nats2)
-	[`nats:2-alpine`](#nats2-alpine)
-	[`nats:2-alpine3.21`](#nats2-alpine321)
-	[`nats:2-linux`](#nats2-linux)
-	[`nats:2-nanoserver`](#nats2-nanoserver)
-	[`nats:2-nanoserver-1809`](#nats2-nanoserver-1809)
-	[`nats:2-scratch`](#nats2-scratch)
-	[`nats:2-windowsservercore`](#nats2-windowsservercore)
-	[`nats:2-windowsservercore-1809`](#nats2-windowsservercore-1809)
-	[`nats:2.10`](#nats210)
-	[`nats:2.10-alpine`](#nats210-alpine)
-	[`nats:2.10-alpine3.21`](#nats210-alpine321)
-	[`nats:2.10-linux`](#nats210-linux)
-	[`nats:2.10-nanoserver`](#nats210-nanoserver)
-	[`nats:2.10-nanoserver-1809`](#nats210-nanoserver-1809)
-	[`nats:2.10-scratch`](#nats210-scratch)
-	[`nats:2.10-windowsservercore`](#nats210-windowsservercore)
-	[`nats:2.10-windowsservercore-1809`](#nats210-windowsservercore-1809)
-	[`nats:2.10.24`](#nats21024)
-	[`nats:2.10.24-alpine`](#nats21024-alpine)
-	[`nats:2.10.24-alpine3.21`](#nats21024-alpine321)
-	[`nats:2.10.24-linux`](#nats21024-linux)
-	[`nats:2.10.24-nanoserver`](#nats21024-nanoserver)
-	[`nats:2.10.24-nanoserver-1809`](#nats21024-nanoserver-1809)
-	[`nats:2.10.24-scratch`](#nats21024-scratch)
-	[`nats:2.10.24-windowsservercore`](#nats21024-windowsservercore)
-	[`nats:2.10.24-windowsservercore-1809`](#nats21024-windowsservercore-1809)
-	[`nats:alpine`](#natsalpine)
-	[`nats:alpine3.21`](#natsalpine321)
-	[`nats:latest`](#natslatest)
-	[`nats:linux`](#natslinux)
-	[`nats:nanoserver`](#natsnanoserver)
-	[`nats:nanoserver-1809`](#natsnanoserver-1809)
-	[`nats:scratch`](#natsscratch)
-	[`nats:windowsservercore`](#natswindowsservercore)
-	[`nats:windowsservercore-1809`](#natswindowsservercore-1809)

## `nats:2`

```console
$ docker pull nats@sha256:bc2b3f3198786445a692d868397d7229502fc445f9966136d76c4d065e473c04
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.17763.6659; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:598ab684e8bafd4f4227ee552ce98bd196abf0cbf6afdc409f74f48886287bb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5905657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24ab2fdd6d375d97b62be28867989f387cc11050dcc31df27d4fa32b6b08e243`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2cb1f9bba9aff495d2f8a23661a6c1c7bc2c839cdc2be180b4b8d9bc9800c45e`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.9 MB (5905148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d543cdf7ef6e19ee24fcb0c663a82a570f5d76342cdbe1f16376e80658f531`  
		Last Modified: Tue, 07 Jan 2025 04:18:12 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:e7a69231651c265e8db70dc79d63ca27d50eff1c7d32be38202da1d315a624f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a5ad75f0ecaf5f3b903c67619e8421121692845fc51e699c386d8afbc9214d`

```dockerfile
```

-	Layers:
	-	`sha256:3b9fcbd5baa342487cc6ee0de074d83be1f60a7d04c5e296fd68ed85e1a4c76c`  
		Last Modified: Tue, 07 Jan 2025 04:18:12 GMT  
		Size: 10.5 KB (10472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:f801151009502a85c381ffc3e3d4da1b39a338bd804445dbab92e447a8d0742d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5dab6565a7ccd5e8b79dd46bc5519aff76b27bfd17665dd3ab08500446ae12c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:81fd6ecec75a6718f55afc7801f7191a8b41d70739a2651f877929f41efcd454`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.6 MB (5553927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4aef5e79acad5215cfeb435fcd7a420447cc550b3045715dcd97efb7cb374f`  
		Last Modified: Tue, 17 Dec 2024 20:07:21 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:aa392b8671143c697cdb326a2e6c742a067761c4db93860f234dc5b35ed0fb11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:976493cfd43ca3f9a8ad5279956a0080949b50282eecf7a444c4fda93c34322f`

```dockerfile
```

-	Layers:
	-	`sha256:8c2857f8ddfd44360797a8c21b94d211d9d2a7db67740cdb79c8c10aa235b398`  
		Last Modified: Tue, 17 Dec 2024 20:07:21 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:982d1d42158b250be7f9650713a8ce7f79bfcba19c04673b21aa2677f187e826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5541946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a6a2dc3f5ef13e36babac38a18c93a6285238679ddf644b3a3f7a5e9e2b29f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:85a1620c1bc6892b5d6c70da117024f4e8fd52994270c35fc7e84782f9682593`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.5 MB (5541438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cdb512b6ca4232a2dd947f49e124f42a6360977706249ce886b49eaba3d3658`  
		Last Modified: Tue, 17 Dec 2024 20:07:18 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:f9eaffb5a7d57be14405ae9a378201ab9a8b8f29afc536e0f8cc6212a74b1a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4afd2190878f0bf2aaadb3cf3fc2a325ccf406cb5223de0922fb20c9f55782d`

```dockerfile
```

-	Layers:
	-	`sha256:163a6014f277c730d1ebece60d800e1889e07231871cc75ab28b5544c87be3b1`  
		Last Modified: Tue, 17 Dec 2024 20:07:18 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:46cc8aa9b94b2de214209442d6cb1e771affdf42d871cfe81596929f23ab15a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5454197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a567c1ed7c844d528fb5acbc5c0388776a9735d231544b5281c56981009f7b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d0b7f1d89d35acbd261abd0ec2bcf54bcc65bb79ebf006850dc5cfae55765a62`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.5 MB (5453688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714d2581a122d6579083f834fb3cf2cea0ad605e1a1ea3cabc5e99db033a0de9`  
		Last Modified: Tue, 17 Dec 2024 23:47:32 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:f41b9f81c4ad1bf1332a199acd507a5e89a4a0d44aa0b141c1d31a41c940b3b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87666fbe34385bd1ec5ac0f209512cd54596dc5cae712d1600dbbb2ea2fcb91e`

```dockerfile
```

-	Layers:
	-	`sha256:c7ee9e2eebe3c624616f634e065612ab6d6e9395b5694f040d1fba9e93e18fec`  
		Last Modified: Tue, 17 Dec 2024 23:47:32 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; ppc64le

```console
$ docker pull nats@sha256:bf4bc17ce581fbc555448128b270a270364f08c1fa916496cdf12b90741ebcbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5418848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61ba372cd7f008492fffa212def1194d605e85849146fc8141f2f60a3935332d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:72b285162443e680327c1bf58de30e30459f3f8193b0769fd1fad6f4f115b124`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.4 MB (5418340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49171e380cf318294924933ba7552fde576651ba45f06690772f99bd0d09c62`  
		Last Modified: Tue, 07 Jan 2025 09:49:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:65d7ddac6a9451045689180537020395f325928967d57be7f680d41e62bfbc7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26558754194d57e26e105533c268c9dd4e5f229090f32bab381f786d5c1ab504`

```dockerfile
```

-	Layers:
	-	`sha256:5db6af784b78d60900035a04e99b70041ea3ee04c0eabcc41b60160cd2933452`  
		Last Modified: Tue, 07 Jan 2025 09:49:22 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; s390x

```console
$ docker pull nats@sha256:a82b5907b071519d7add42e0ff6632ee3ea5ad1152c0f3432ee682f4954e38f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5748559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:064b066d0f376d269a70742585b50ba3cd7c177611f92c629f158e2df7944418`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bd4119cb6f8c6b49f3ec55933200d2283d0f58b8b79bb753e5436770b7c2b320`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.7 MB (5748050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afd816dca497faa2937925ee17de8bdaa1530e524721a18bf0e7838bd7f6c2e`  
		Last Modified: Tue, 17 Dec 2024 20:07:57 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:c28225ad7ee2152f11088957130764b2ca530f01b73f693afc238a553b29d443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f772a80018515b59b3c7005be4f7c9bdc3a6a48167750b803269d3bf711e8f08`

```dockerfile
```

-	Layers:
	-	`sha256:9de3e5757b559fa1c5cba102c651c66e5db5e3b5889139d5508a670b2b9f07d5`  
		Last Modified: Tue, 17 Dec 2024 20:07:57 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - windows version 10.0.17763.6659; amd64

```console
$ docker pull nats@sha256:a3bf98913be025c2083ebd5687c133ab5b00f3a1894a3fe2231a87894b64bed0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161263273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50684e4ed1bf0d28623bfd52d2bfd9a7c4111c83ceaabd37a09cbf397e675281`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 04:54:21 GMT
RUN Apply image 10.0.17763.6659
# Tue, 17 Dec 2024 20:08:15 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 17 Dec 2024 20:08:18 GMT
RUN cmd /S /C #(nop) COPY file:32d2c78f0dd94e383b45881b640cf1b2c9c27decb4a66e09babbe6a0f796087f in C:\nats-server.exe 
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 17 Dec 2024 20:08:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fc1cdf36537340b1875b5d6573a58a268fc20b63dc54a780f9070e51cf9eb9ca`  
		Last Modified: Tue, 10 Dec 2024 21:03:34 GMT  
		Size: 155.2 MB (155231618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f2ef448a775bed9c6f05668d734eb51754170fdfc93c55c99bbaa763bf0d4e`  
		Last Modified: Tue, 17 Dec 2024 20:08:26 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe350f8421c39c736eb0f8180693ff45eedcd35a224bc510bd2626a0996409b`  
		Last Modified: Tue, 17 Dec 2024 20:08:25 GMT  
		Size: 6.0 MB (6025803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd8a7a90698ba96911ac6344eb5f5dd88c4dfebd29047be607133fadef68165`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.7 KB (1671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f84b1a718e07866b0c5d7f7666c682f746339824f50d2010237f8129d983c34`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be4b8e9d23c6bed197e181271e99e2a123100ad014b841f2409aaa51fe58303`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52cb4f7ea4c581f0a9e1eb6519dba6818337a039607974ce3fd7131a13ea51b0`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:1ae474d1c029d61d5ad7b170989ab048bc157b8d3ef173d9c8dda10431f4c66a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:e75e15a642407b176cda44b593952a650099bbffced18ac86e1da0adb45a815c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9984940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09fd7f582707a2da49e3e73d42a6397c85ea95b6e58a615a5f0bf1a3780834b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.1-x86_64.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:245043d9199c263f869fc0558f43f7cb98bbc92acdd5def1b4f690adc0ac7807`  
		Last Modified: Mon, 06 Jan 2025 21:44:42 GMT  
		Size: 3.6 MB (3636222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13a0d0824643f0161fd224aceb130343bf44e238a29f9f1cac440eb4b097701c`  
		Last Modified: Tue, 07 Jan 2025 03:20:06 GMT  
		Size: 6.3 MB (6347749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5413da9dd68b96d78c2f9a6ad90c83c10eba4927bfcf99f8812ea179a093c146`  
		Last Modified: Tue, 07 Jan 2025 03:20:06 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdba86b0d45f2bc8262ff57e28b3781caf6b47e078a80f3e89f03f05b9eac8a4`  
		Last Modified: Tue, 07 Jan 2025 03:20:06 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:74e3d1c872d5047663341b23e819482b2bf389190102cfdb5f2b5a10c87a0f08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb0055da207991572098ff5f84511e527c4057fa58cf40e1311b9013d4db18e6`

```dockerfile
```

-	Layers:
	-	`sha256:301c11a8c0e0cb7a10b31ed266709ff88d4cb1d04b4b773cda7d7a7af0a919ee`  
		Last Modified: Tue, 07 Jan 2025 03:20:07 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:56cbfc79edf7b2c7aa940cfd6f7383d3f0acd1d20aef967f001ded5079cb2b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9361190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a44eaada784dc01cb9c5f57575b9f22ece42b1f2885e166714a4ec2a677ee2bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.1-armhf.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:31d4a7f5d4e2c1fd6b13116c69b324d9255a249ba92b63cd7d98924ec5438675`  
		Last Modified: Tue, 07 Jan 2025 02:29:34 GMT  
		Size: 3.4 MB (3361034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3aeae20c738cb0545c05b726c587c76393b9a553968be75b99d583e66a7775b`  
		Last Modified: Tue, 07 Jan 2025 03:58:09 GMT  
		Size: 6.0 MB (5999180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ec491cee3b9736e33232b0eeecad77b992ef16de691db662b0b61774f8b73c`  
		Last Modified: Tue, 07 Jan 2025 03:58:08 GMT  
		Size: 564.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03aa8832feccfdad9eba1b2d0cfeabfbc22bd7ac1eb3047e9e71b63a38bb09c`  
		Last Modified: Tue, 07 Jan 2025 03:58:08 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:cb2eb11b7181517ab509ea8b21a459285feee2175862c053b04ac04c56ca29a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13da7c14ff3fa5a48c56b744564d8ee8a26501609ee8b4a5c1f30b63e89fcb91`

```dockerfile
```

-	Layers:
	-	`sha256:df8f81133a2bf850bec9c382e906dfc869f01f7c98b59587a49715e9aeb29498`  
		Last Modified: Tue, 07 Jan 2025 03:58:08 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:fdfe42e62e2b79b73f65039202fe3229e6cb71c69e82a64080c440b9707cedd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9080587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1588e3d1330f032c6efe96bdb72b0f9179e37f26f272bac3d8f53f11bef3cbff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.1-armv7.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fa398bd1707194d783a6221bb60ba630f074222cdc0f4b6a05d9167d6e9c4a9f`  
		Last Modified: Tue, 07 Jan 2025 02:55:27 GMT  
		Size: 3.1 MB (3093241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f00f9faabc3557dcc5a09506016607206ccc43235c52c7f039f0f569067899f`  
		Last Modified: Tue, 07 Jan 2025 03:43:07 GMT  
		Size: 6.0 MB (5986376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ec44d2ed6879601786756e72d73f99cde8e79fa55e16f1af107519e800da9e`  
		Last Modified: Tue, 07 Jan 2025 03:43:06 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e68cbd6292db04b815b0b4f504cc27d37888065829ba6187ed1b81146b0f8b`  
		Last Modified: Tue, 07 Jan 2025 03:43:06 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:42c8ebef1cfc8b8f2fb88adcab48268298580a6b1c7994bc90ecc0e85eaee6be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb1d3dff94118ce66c8f8e7273533a5489d0907af8d4d1c08d15b86a65ef9aa`

```dockerfile
```

-	Layers:
	-	`sha256:16ef13af5efe22a4816752712e3aa06f4d2e9e998d253a67358a93a82bf88c3b`  
		Last Modified: Tue, 07 Jan 2025 03:43:06 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a3bd4772713e383733977b42d0bdfde71d8bc73298b3043639c042161e7b3ce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9885113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80637e8b5cf4194cba52d82998bac00c029971bb34fc5be960598a7483cd5d67`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:707c94c90c597447ce10a36c9b56355c1cc67d0cf593a592daeb419d99a30d85`  
		Last Modified: Tue, 07 Jan 2025 03:02:50 GMT  
		Size: 4.0 MB (3983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81dca03c14249dbcca7f333b7af01e9e99db8e96d6c9d2f2bde6d66c7e329324`  
		Last Modified: Tue, 07 Jan 2025 04:20:26 GMT  
		Size: 5.9 MB (5901137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9545f2b071c52dcf93362ddf8c114680a82ab925c1a0404a1ced42ca02cf81c`  
		Last Modified: Tue, 07 Jan 2025 04:20:26 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22af105e2b54631c9d3d6f803af860c168d3e5cc35a5fa5be13328311c288cc8`  
		Last Modified: Tue, 07 Jan 2025 04:20:26 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:b33a75f3a131215546c5e5051f64d1da52efc1df0668a9807a8e69112eac7f54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d468c758973e805c31c177ab74b4029804f634f063c47cfb99ff25d3cf499b`

```dockerfile
```

-	Layers:
	-	`sha256:6179800d5433282d408054d0574571874af30c964b865ce8caa292b6df2ade56`  
		Last Modified: Tue, 07 Jan 2025 04:20:26 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:5d7ae4028ab12c2a74b8a7c331e4ccb0eae01a94d682cc65b60b8fd51c43d223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9432907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc3b47e1a998b06b497b8d3d4573199f0385b0f9bfe7543c284b47f05acebb66`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.1-ppc64le.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9207393f0daad55cddbc775f55edde5baecdca9e0441c9c1f627f2394d28b7c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:05 GMT  
		Size: 3.6 MB (3567745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acef6d00c5d9f955c0ada0042b4d702b198dc599a72773715bec6a5deab07ba2`  
		Last Modified: Tue, 07 Jan 2025 03:50:51 GMT  
		Size: 5.9 MB (5864192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce5db60d75e59b4b4f0e79bcd3c707843e4f174e155467ba9c768426b98a398`  
		Last Modified: Tue, 07 Jan 2025 03:50:51 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d120b1f8dd2ce33447645c1b4328c2d88cbb5d570c67bc161cc99b05f5c68e`  
		Last Modified: Tue, 07 Jan 2025 03:50:51 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:c9feafae7ef54aa6e4379a8e78a32c28c988b91724d91bb48524d6e2f396d67f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e39d2f23f56f144fffc66e26c856f03cde7d644a740c82397b8866f918db873d`

```dockerfile
```

-	Layers:
	-	`sha256:f681712c35cd291126837bbcdeb41fc7871fc45035d8dec9395bd27034b3d520`  
		Last Modified: Tue, 07 Jan 2025 03:50:51 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; s390x

```console
$ docker pull nats@sha256:4649a608cb9cdfc49ebb039d6ea36cd89a3ef0c6e2ce1402f3d2c24a9a221225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9653226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b55dcbb50fac7b108734557067c71c07e62274db299fe32ec263b9e11f2cb59`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.1-s390x.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:93a724ed1843277c272a09a7779ca31a802938fe3a88142df42e291e0dc759c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:17 GMT  
		Size: 3.5 MB (3459449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723f4bf7823ff55b05e1545bb39271fc9629e9d17ec83b14c487b1bc1feaf66e`  
		Last Modified: Tue, 07 Jan 2025 03:45:59 GMT  
		Size: 6.2 MB (6192808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8625174e21f292a47f2bb46a59b4d41f57a796cd52926234c718dd0556f08a54`  
		Last Modified: Tue, 07 Jan 2025 03:45:59 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b2c4e11055e3b9000f33288affd900fabde3b220edf8fbff0d50687fa637b06`  
		Last Modified: Tue, 07 Jan 2025 03:45:59 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:d952184708e04933d2b5631eb5fd04bdd74ca4e384122fa926fb8f74b34d0d93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e29dff1272c5b181c168004dd85e6068f54151252615c50a09ef6dff321104a9`

```dockerfile
```

-	Layers:
	-	`sha256:6ff141856e7b853dc1f812064b76dbb06f3dfb468f1dfa89312a9f106434e96f`  
		Last Modified: Tue, 07 Jan 2025 03:45:59 GMT  
		Size: 14.3 KB (14321 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-alpine3.21`

```console
$ docker pull nats@sha256:1ae474d1c029d61d5ad7b170989ab048bc157b8d3ef173d9c8dda10431f4c66a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2-alpine3.21` - linux; amd64

```console
$ docker pull nats@sha256:e75e15a642407b176cda44b593952a650099bbffced18ac86e1da0adb45a815c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9984940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09fd7f582707a2da49e3e73d42a6397c85ea95b6e58a615a5f0bf1a3780834b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.1-x86_64.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:245043d9199c263f869fc0558f43f7cb98bbc92acdd5def1b4f690adc0ac7807`  
		Last Modified: Mon, 06 Jan 2025 21:44:42 GMT  
		Size: 3.6 MB (3636222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13a0d0824643f0161fd224aceb130343bf44e238a29f9f1cac440eb4b097701c`  
		Last Modified: Tue, 07 Jan 2025 03:20:06 GMT  
		Size: 6.3 MB (6347749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5413da9dd68b96d78c2f9a6ad90c83c10eba4927bfcf99f8812ea179a093c146`  
		Last Modified: Tue, 07 Jan 2025 03:20:06 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdba86b0d45f2bc8262ff57e28b3781caf6b47e078a80f3e89f03f05b9eac8a4`  
		Last Modified: Tue, 07 Jan 2025 03:20:06 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:74e3d1c872d5047663341b23e819482b2bf389190102cfdb5f2b5a10c87a0f08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb0055da207991572098ff5f84511e527c4057fa58cf40e1311b9013d4db18e6`

```dockerfile
```

-	Layers:
	-	`sha256:301c11a8c0e0cb7a10b31ed266709ff88d4cb1d04b4b773cda7d7a7af0a919ee`  
		Last Modified: Tue, 07 Jan 2025 03:20:07 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:56cbfc79edf7b2c7aa940cfd6f7383d3f0acd1d20aef967f001ded5079cb2b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9361190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a44eaada784dc01cb9c5f57575b9f22ece42b1f2885e166714a4ec2a677ee2bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.1-armhf.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:31d4a7f5d4e2c1fd6b13116c69b324d9255a249ba92b63cd7d98924ec5438675`  
		Last Modified: Tue, 07 Jan 2025 02:29:34 GMT  
		Size: 3.4 MB (3361034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3aeae20c738cb0545c05b726c587c76393b9a553968be75b99d583e66a7775b`  
		Last Modified: Tue, 07 Jan 2025 03:58:09 GMT  
		Size: 6.0 MB (5999180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ec491cee3b9736e33232b0eeecad77b992ef16de691db662b0b61774f8b73c`  
		Last Modified: Tue, 07 Jan 2025 03:58:08 GMT  
		Size: 564.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03aa8832feccfdad9eba1b2d0cfeabfbc22bd7ac1eb3047e9e71b63a38bb09c`  
		Last Modified: Tue, 07 Jan 2025 03:58:08 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:cb2eb11b7181517ab509ea8b21a459285feee2175862c053b04ac04c56ca29a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13da7c14ff3fa5a48c56b744564d8ee8a26501609ee8b4a5c1f30b63e89fcb91`

```dockerfile
```

-	Layers:
	-	`sha256:df8f81133a2bf850bec9c382e906dfc869f01f7c98b59587a49715e9aeb29498`  
		Last Modified: Tue, 07 Jan 2025 03:58:08 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:fdfe42e62e2b79b73f65039202fe3229e6cb71c69e82a64080c440b9707cedd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9080587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1588e3d1330f032c6efe96bdb72b0f9179e37f26f272bac3d8f53f11bef3cbff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.1-armv7.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fa398bd1707194d783a6221bb60ba630f074222cdc0f4b6a05d9167d6e9c4a9f`  
		Last Modified: Tue, 07 Jan 2025 02:55:27 GMT  
		Size: 3.1 MB (3093241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f00f9faabc3557dcc5a09506016607206ccc43235c52c7f039f0f569067899f`  
		Last Modified: Tue, 07 Jan 2025 03:43:07 GMT  
		Size: 6.0 MB (5986376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ec44d2ed6879601786756e72d73f99cde8e79fa55e16f1af107519e800da9e`  
		Last Modified: Tue, 07 Jan 2025 03:43:06 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e68cbd6292db04b815b0b4f504cc27d37888065829ba6187ed1b81146b0f8b`  
		Last Modified: Tue, 07 Jan 2025 03:43:06 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:42c8ebef1cfc8b8f2fb88adcab48268298580a6b1c7994bc90ecc0e85eaee6be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb1d3dff94118ce66c8f8e7273533a5489d0907af8d4d1c08d15b86a65ef9aa`

```dockerfile
```

-	Layers:
	-	`sha256:16ef13af5efe22a4816752712e3aa06f4d2e9e998d253a67358a93a82bf88c3b`  
		Last Modified: Tue, 07 Jan 2025 03:43:06 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a3bd4772713e383733977b42d0bdfde71d8bc73298b3043639c042161e7b3ce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9885113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80637e8b5cf4194cba52d82998bac00c029971bb34fc5be960598a7483cd5d67`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:707c94c90c597447ce10a36c9b56355c1cc67d0cf593a592daeb419d99a30d85`  
		Last Modified: Tue, 07 Jan 2025 03:02:50 GMT  
		Size: 4.0 MB (3983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81dca03c14249dbcca7f333b7af01e9e99db8e96d6c9d2f2bde6d66c7e329324`  
		Last Modified: Tue, 07 Jan 2025 04:20:26 GMT  
		Size: 5.9 MB (5901137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9545f2b071c52dcf93362ddf8c114680a82ab925c1a0404a1ced42ca02cf81c`  
		Last Modified: Tue, 07 Jan 2025 04:20:26 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22af105e2b54631c9d3d6f803af860c168d3e5cc35a5fa5be13328311c288cc8`  
		Last Modified: Tue, 07 Jan 2025 04:20:26 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:b33a75f3a131215546c5e5051f64d1da52efc1df0668a9807a8e69112eac7f54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d468c758973e805c31c177ab74b4029804f634f063c47cfb99ff25d3cf499b`

```dockerfile
```

-	Layers:
	-	`sha256:6179800d5433282d408054d0574571874af30c964b865ce8caa292b6df2ade56`  
		Last Modified: Tue, 07 Jan 2025 04:20:26 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:5d7ae4028ab12c2a74b8a7c331e4ccb0eae01a94d682cc65b60b8fd51c43d223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9432907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc3b47e1a998b06b497b8d3d4573199f0385b0f9bfe7543c284b47f05acebb66`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.1-ppc64le.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9207393f0daad55cddbc775f55edde5baecdca9e0441c9c1f627f2394d28b7c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:05 GMT  
		Size: 3.6 MB (3567745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acef6d00c5d9f955c0ada0042b4d702b198dc599a72773715bec6a5deab07ba2`  
		Last Modified: Tue, 07 Jan 2025 03:50:51 GMT  
		Size: 5.9 MB (5864192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce5db60d75e59b4b4f0e79bcd3c707843e4f174e155467ba9c768426b98a398`  
		Last Modified: Tue, 07 Jan 2025 03:50:51 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d120b1f8dd2ce33447645c1b4328c2d88cbb5d570c67bc161cc99b05f5c68e`  
		Last Modified: Tue, 07 Jan 2025 03:50:51 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:c9feafae7ef54aa6e4379a8e78a32c28c988b91724d91bb48524d6e2f396d67f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e39d2f23f56f144fffc66e26c856f03cde7d644a740c82397b8866f918db873d`

```dockerfile
```

-	Layers:
	-	`sha256:f681712c35cd291126837bbcdeb41fc7871fc45035d8dec9395bd27034b3d520`  
		Last Modified: Tue, 07 Jan 2025 03:50:51 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:4649a608cb9cdfc49ebb039d6ea36cd89a3ef0c6e2ce1402f3d2c24a9a221225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9653226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b55dcbb50fac7b108734557067c71c07e62274db299fe32ec263b9e11f2cb59`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.1-s390x.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:93a724ed1843277c272a09a7779ca31a802938fe3a88142df42e291e0dc759c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:17 GMT  
		Size: 3.5 MB (3459449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723f4bf7823ff55b05e1545bb39271fc9629e9d17ec83b14c487b1bc1feaf66e`  
		Last Modified: Tue, 07 Jan 2025 03:45:59 GMT  
		Size: 6.2 MB (6192808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8625174e21f292a47f2bb46a59b4d41f57a796cd52926234c718dd0556f08a54`  
		Last Modified: Tue, 07 Jan 2025 03:45:59 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b2c4e11055e3b9000f33288affd900fabde3b220edf8fbff0d50687fa637b06`  
		Last Modified: Tue, 07 Jan 2025 03:45:59 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:d952184708e04933d2b5631eb5fd04bdd74ca4e384122fa926fb8f74b34d0d93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e29dff1272c5b181c168004dd85e6068f54151252615c50a09ef6dff321104a9`

```dockerfile
```

-	Layers:
	-	`sha256:6ff141856e7b853dc1f812064b76dbb06f3dfb468f1dfa89312a9f106434e96f`  
		Last Modified: Tue, 07 Jan 2025 03:45:59 GMT  
		Size: 14.3 KB (14321 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-linux`

```console
$ docker pull nats@sha256:c597fb1c0dbee32f6092767e6550bc6f458d011aa48f8467f483161208b853ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:598ab684e8bafd4f4227ee552ce98bd196abf0cbf6afdc409f74f48886287bb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5905657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24ab2fdd6d375d97b62be28867989f387cc11050dcc31df27d4fa32b6b08e243`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2cb1f9bba9aff495d2f8a23661a6c1c7bc2c839cdc2be180b4b8d9bc9800c45e`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.9 MB (5905148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d543cdf7ef6e19ee24fcb0c663a82a570f5d76342cdbe1f16376e80658f531`  
		Last Modified: Tue, 07 Jan 2025 04:18:12 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:e7a69231651c265e8db70dc79d63ca27d50eff1c7d32be38202da1d315a624f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a5ad75f0ecaf5f3b903c67619e8421121692845fc51e699c386d8afbc9214d`

```dockerfile
```

-	Layers:
	-	`sha256:3b9fcbd5baa342487cc6ee0de074d83be1f60a7d04c5e296fd68ed85e1a4c76c`  
		Last Modified: Tue, 07 Jan 2025 04:18:12 GMT  
		Size: 10.5 KB (10472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:f801151009502a85c381ffc3e3d4da1b39a338bd804445dbab92e447a8d0742d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5dab6565a7ccd5e8b79dd46bc5519aff76b27bfd17665dd3ab08500446ae12c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:81fd6ecec75a6718f55afc7801f7191a8b41d70739a2651f877929f41efcd454`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.6 MB (5553927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4aef5e79acad5215cfeb435fcd7a420447cc550b3045715dcd97efb7cb374f`  
		Last Modified: Tue, 17 Dec 2024 20:07:21 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:aa392b8671143c697cdb326a2e6c742a067761c4db93860f234dc5b35ed0fb11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:976493cfd43ca3f9a8ad5279956a0080949b50282eecf7a444c4fda93c34322f`

```dockerfile
```

-	Layers:
	-	`sha256:8c2857f8ddfd44360797a8c21b94d211d9d2a7db67740cdb79c8c10aa235b398`  
		Last Modified: Tue, 17 Dec 2024 20:07:21 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:982d1d42158b250be7f9650713a8ce7f79bfcba19c04673b21aa2677f187e826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5541946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a6a2dc3f5ef13e36babac38a18c93a6285238679ddf644b3a3f7a5e9e2b29f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:85a1620c1bc6892b5d6c70da117024f4e8fd52994270c35fc7e84782f9682593`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.5 MB (5541438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cdb512b6ca4232a2dd947f49e124f42a6360977706249ce886b49eaba3d3658`  
		Last Modified: Tue, 17 Dec 2024 20:07:18 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:f9eaffb5a7d57be14405ae9a378201ab9a8b8f29afc536e0f8cc6212a74b1a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4afd2190878f0bf2aaadb3cf3fc2a325ccf406cb5223de0922fb20c9f55782d`

```dockerfile
```

-	Layers:
	-	`sha256:163a6014f277c730d1ebece60d800e1889e07231871cc75ab28b5544c87be3b1`  
		Last Modified: Tue, 17 Dec 2024 20:07:18 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:46cc8aa9b94b2de214209442d6cb1e771affdf42d871cfe81596929f23ab15a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5454197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a567c1ed7c844d528fb5acbc5c0388776a9735d231544b5281c56981009f7b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d0b7f1d89d35acbd261abd0ec2bcf54bcc65bb79ebf006850dc5cfae55765a62`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.5 MB (5453688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714d2581a122d6579083f834fb3cf2cea0ad605e1a1ea3cabc5e99db033a0de9`  
		Last Modified: Tue, 17 Dec 2024 23:47:32 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:f41b9f81c4ad1bf1332a199acd507a5e89a4a0d44aa0b141c1d31a41c940b3b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87666fbe34385bd1ec5ac0f209512cd54596dc5cae712d1600dbbb2ea2fcb91e`

```dockerfile
```

-	Layers:
	-	`sha256:c7ee9e2eebe3c624616f634e065612ab6d6e9395b5694f040d1fba9e93e18fec`  
		Last Modified: Tue, 17 Dec 2024 23:47:32 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:bf4bc17ce581fbc555448128b270a270364f08c1fa916496cdf12b90741ebcbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5418848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61ba372cd7f008492fffa212def1194d605e85849146fc8141f2f60a3935332d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:72b285162443e680327c1bf58de30e30459f3f8193b0769fd1fad6f4f115b124`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.4 MB (5418340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49171e380cf318294924933ba7552fde576651ba45f06690772f99bd0d09c62`  
		Last Modified: Tue, 07 Jan 2025 09:49:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:65d7ddac6a9451045689180537020395f325928967d57be7f680d41e62bfbc7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26558754194d57e26e105533c268c9dd4e5f229090f32bab381f786d5c1ab504`

```dockerfile
```

-	Layers:
	-	`sha256:5db6af784b78d60900035a04e99b70041ea3ee04c0eabcc41b60160cd2933452`  
		Last Modified: Tue, 07 Jan 2025 09:49:22 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; s390x

```console
$ docker pull nats@sha256:a82b5907b071519d7add42e0ff6632ee3ea5ad1152c0f3432ee682f4954e38f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5748559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:064b066d0f376d269a70742585b50ba3cd7c177611f92c629f158e2df7944418`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bd4119cb6f8c6b49f3ec55933200d2283d0f58b8b79bb753e5436770b7c2b320`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.7 MB (5748050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afd816dca497faa2937925ee17de8bdaa1530e524721a18bf0e7838bd7f6c2e`  
		Last Modified: Tue, 17 Dec 2024 20:07:57 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:c28225ad7ee2152f11088957130764b2ca530f01b73f693afc238a553b29d443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f772a80018515b59b3c7005be4f7c9bdc3a6a48167750b803269d3bf711e8f08`

```dockerfile
```

-	Layers:
	-	`sha256:9de3e5757b559fa1c5cba102c651c66e5db5e3b5889139d5508a670b2b9f07d5`  
		Last Modified: Tue, 17 Dec 2024 20:07:57 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:37e1b8a8d0e258480f2b4e3e528c51625f7c66283ec06ca04228db3a08fa024e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.6659; amd64

```console
$ docker pull nats@sha256:a3bf98913be025c2083ebd5687c133ab5b00f3a1894a3fe2231a87894b64bed0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161263273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50684e4ed1bf0d28623bfd52d2bfd9a7c4111c83ceaabd37a09cbf397e675281`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 04:54:21 GMT
RUN Apply image 10.0.17763.6659
# Tue, 17 Dec 2024 20:08:15 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 17 Dec 2024 20:08:18 GMT
RUN cmd /S /C #(nop) COPY file:32d2c78f0dd94e383b45881b640cf1b2c9c27decb4a66e09babbe6a0f796087f in C:\nats-server.exe 
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 17 Dec 2024 20:08:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fc1cdf36537340b1875b5d6573a58a268fc20b63dc54a780f9070e51cf9eb9ca`  
		Last Modified: Tue, 10 Dec 2024 21:03:34 GMT  
		Size: 155.2 MB (155231618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f2ef448a775bed9c6f05668d734eb51754170fdfc93c55c99bbaa763bf0d4e`  
		Last Modified: Tue, 17 Dec 2024 20:08:26 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe350f8421c39c736eb0f8180693ff45eedcd35a224bc510bd2626a0996409b`  
		Last Modified: Tue, 17 Dec 2024 20:08:25 GMT  
		Size: 6.0 MB (6025803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd8a7a90698ba96911ac6344eb5f5dd88c4dfebd29047be607133fadef68165`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.7 KB (1671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f84b1a718e07866b0c5d7f7666c682f746339824f50d2010237f8129d983c34`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be4b8e9d23c6bed197e181271e99e2a123100ad014b841f2409aaa51fe58303`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52cb4f7ea4c581f0a9e1eb6519dba6818337a039607974ce3fd7131a13ea51b0`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:37e1b8a8d0e258480f2b4e3e528c51625f7c66283ec06ca04228db3a08fa024e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull nats@sha256:a3bf98913be025c2083ebd5687c133ab5b00f3a1894a3fe2231a87894b64bed0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161263273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50684e4ed1bf0d28623bfd52d2bfd9a7c4111c83ceaabd37a09cbf397e675281`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 04:54:21 GMT
RUN Apply image 10.0.17763.6659
# Tue, 17 Dec 2024 20:08:15 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 17 Dec 2024 20:08:18 GMT
RUN cmd /S /C #(nop) COPY file:32d2c78f0dd94e383b45881b640cf1b2c9c27decb4a66e09babbe6a0f796087f in C:\nats-server.exe 
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 17 Dec 2024 20:08:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fc1cdf36537340b1875b5d6573a58a268fc20b63dc54a780f9070e51cf9eb9ca`  
		Last Modified: Tue, 10 Dec 2024 21:03:34 GMT  
		Size: 155.2 MB (155231618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f2ef448a775bed9c6f05668d734eb51754170fdfc93c55c99bbaa763bf0d4e`  
		Last Modified: Tue, 17 Dec 2024 20:08:26 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe350f8421c39c736eb0f8180693ff45eedcd35a224bc510bd2626a0996409b`  
		Last Modified: Tue, 17 Dec 2024 20:08:25 GMT  
		Size: 6.0 MB (6025803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd8a7a90698ba96911ac6344eb5f5dd88c4dfebd29047be607133fadef68165`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.7 KB (1671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f84b1a718e07866b0c5d7f7666c682f746339824f50d2010237f8129d983c34`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be4b8e9d23c6bed197e181271e99e2a123100ad014b841f2409aaa51fe58303`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52cb4f7ea4c581f0a9e1eb6519dba6818337a039607974ce3fd7131a13ea51b0`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:c597fb1c0dbee32f6092767e6550bc6f458d011aa48f8467f483161208b853ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:598ab684e8bafd4f4227ee552ce98bd196abf0cbf6afdc409f74f48886287bb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5905657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24ab2fdd6d375d97b62be28867989f387cc11050dcc31df27d4fa32b6b08e243`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2cb1f9bba9aff495d2f8a23661a6c1c7bc2c839cdc2be180b4b8d9bc9800c45e`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.9 MB (5905148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d543cdf7ef6e19ee24fcb0c663a82a570f5d76342cdbe1f16376e80658f531`  
		Last Modified: Tue, 07 Jan 2025 04:18:12 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:e7a69231651c265e8db70dc79d63ca27d50eff1c7d32be38202da1d315a624f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a5ad75f0ecaf5f3b903c67619e8421121692845fc51e699c386d8afbc9214d`

```dockerfile
```

-	Layers:
	-	`sha256:3b9fcbd5baa342487cc6ee0de074d83be1f60a7d04c5e296fd68ed85e1a4c76c`  
		Last Modified: Tue, 07 Jan 2025 04:18:12 GMT  
		Size: 10.5 KB (10472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:f801151009502a85c381ffc3e3d4da1b39a338bd804445dbab92e447a8d0742d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5dab6565a7ccd5e8b79dd46bc5519aff76b27bfd17665dd3ab08500446ae12c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:81fd6ecec75a6718f55afc7801f7191a8b41d70739a2651f877929f41efcd454`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.6 MB (5553927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4aef5e79acad5215cfeb435fcd7a420447cc550b3045715dcd97efb7cb374f`  
		Last Modified: Tue, 17 Dec 2024 20:07:21 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:aa392b8671143c697cdb326a2e6c742a067761c4db93860f234dc5b35ed0fb11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:976493cfd43ca3f9a8ad5279956a0080949b50282eecf7a444c4fda93c34322f`

```dockerfile
```

-	Layers:
	-	`sha256:8c2857f8ddfd44360797a8c21b94d211d9d2a7db67740cdb79c8c10aa235b398`  
		Last Modified: Tue, 17 Dec 2024 20:07:21 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:982d1d42158b250be7f9650713a8ce7f79bfcba19c04673b21aa2677f187e826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5541946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a6a2dc3f5ef13e36babac38a18c93a6285238679ddf644b3a3f7a5e9e2b29f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:85a1620c1bc6892b5d6c70da117024f4e8fd52994270c35fc7e84782f9682593`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.5 MB (5541438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cdb512b6ca4232a2dd947f49e124f42a6360977706249ce886b49eaba3d3658`  
		Last Modified: Tue, 17 Dec 2024 20:07:18 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:f9eaffb5a7d57be14405ae9a378201ab9a8b8f29afc536e0f8cc6212a74b1a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4afd2190878f0bf2aaadb3cf3fc2a325ccf406cb5223de0922fb20c9f55782d`

```dockerfile
```

-	Layers:
	-	`sha256:163a6014f277c730d1ebece60d800e1889e07231871cc75ab28b5544c87be3b1`  
		Last Modified: Tue, 17 Dec 2024 20:07:18 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:46cc8aa9b94b2de214209442d6cb1e771affdf42d871cfe81596929f23ab15a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5454197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a567c1ed7c844d528fb5acbc5c0388776a9735d231544b5281c56981009f7b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d0b7f1d89d35acbd261abd0ec2bcf54bcc65bb79ebf006850dc5cfae55765a62`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.5 MB (5453688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714d2581a122d6579083f834fb3cf2cea0ad605e1a1ea3cabc5e99db033a0de9`  
		Last Modified: Tue, 17 Dec 2024 23:47:32 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:f41b9f81c4ad1bf1332a199acd507a5e89a4a0d44aa0b141c1d31a41c940b3b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87666fbe34385bd1ec5ac0f209512cd54596dc5cae712d1600dbbb2ea2fcb91e`

```dockerfile
```

-	Layers:
	-	`sha256:c7ee9e2eebe3c624616f634e065612ab6d6e9395b5694f040d1fba9e93e18fec`  
		Last Modified: Tue, 17 Dec 2024 23:47:32 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:bf4bc17ce581fbc555448128b270a270364f08c1fa916496cdf12b90741ebcbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5418848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61ba372cd7f008492fffa212def1194d605e85849146fc8141f2f60a3935332d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:72b285162443e680327c1bf58de30e30459f3f8193b0769fd1fad6f4f115b124`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.4 MB (5418340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49171e380cf318294924933ba7552fde576651ba45f06690772f99bd0d09c62`  
		Last Modified: Tue, 07 Jan 2025 09:49:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:65d7ddac6a9451045689180537020395f325928967d57be7f680d41e62bfbc7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26558754194d57e26e105533c268c9dd4e5f229090f32bab381f786d5c1ab504`

```dockerfile
```

-	Layers:
	-	`sha256:5db6af784b78d60900035a04e99b70041ea3ee04c0eabcc41b60160cd2933452`  
		Last Modified: Tue, 07 Jan 2025 09:49:22 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; s390x

```console
$ docker pull nats@sha256:a82b5907b071519d7add42e0ff6632ee3ea5ad1152c0f3432ee682f4954e38f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5748559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:064b066d0f376d269a70742585b50ba3cd7c177611f92c629f158e2df7944418`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bd4119cb6f8c6b49f3ec55933200d2283d0f58b8b79bb753e5436770b7c2b320`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.7 MB (5748050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afd816dca497faa2937925ee17de8bdaa1530e524721a18bf0e7838bd7f6c2e`  
		Last Modified: Tue, 17 Dec 2024 20:07:57 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:c28225ad7ee2152f11088957130764b2ca530f01b73f693afc238a553b29d443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f772a80018515b59b3c7005be4f7c9bdc3a6a48167750b803269d3bf711e8f08`

```dockerfile
```

-	Layers:
	-	`sha256:9de3e5757b559fa1c5cba102c651c66e5db5e3b5889139d5508a670b2b9f07d5`  
		Last Modified: Tue, 17 Dec 2024 20:07:57 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:358028020ee9c6b6ff8494f70ecbfddddf5b29d36bd20ec1b9b37eb351c46081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.6659; amd64

```console
$ docker pull nats@sha256:c6e3358af2d309d6c2ed2c4321b8d16f0c8c2b817d67b61e77790abeab192882
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2021024024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64938b4574dd9f4d28b0fdba70a6f3483c75359cd4de6fe307eaf6b4c9e6c5d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Tue, 17 Dec 2024 19:28:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 17 Dec 2024 19:28:54 GMT
ENV NATS_DOCKERIZED=1
# Tue, 17 Dec 2024 19:28:55 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 19:28:56 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.24/nats-server-v2.10.24-windows-amd64.zip
# Tue, 17 Dec 2024 19:28:57 GMT
ENV NATS_SERVER_SHASUM=bf94c9a9f1685147fd95f6c62f26d16fb72dc8c8c592e2d8c9115e2491c508c3
# Tue, 17 Dec 2024 19:30:38 GMT
RUN Set-PSDebug -Trace 2
# Tue, 17 Dec 2024 19:31:05 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 17 Dec 2024 19:31:06 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 17 Dec 2024 19:31:06 GMT
EXPOSE 4222 6222 8222
# Tue, 17 Dec 2024 19:31:07 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 17 Dec 2024 19:31:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995e898d38ff13b74b2bf42182403105bd564ca1c8cd3c2bccadac08c8172ca2`  
		Last Modified: Tue, 17 Dec 2024 19:31:15 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7f7d745fbcac3f49a978704fb067848ad5982ff0f7f116bfaceb8e9c68fbc7`  
		Last Modified: Tue, 17 Dec 2024 19:31:15 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0a5927c302d6e5e93a6570c06c06ce9862ef400bd5fea534fea403fd76e9b8`  
		Last Modified: Tue, 17 Dec 2024 19:31:13 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e7b1cd8a1d4aa5917755e9a51eb72256b93ddf6aa3825cbd84213d86f046d3`  
		Last Modified: Tue, 17 Dec 2024 19:31:13 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a76e8a87993daefe8a56da532e9ecac69a46fe935f34deac5f3e2ccff312c7`  
		Last Modified: Tue, 17 Dec 2024 19:31:13 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f37de67167c5db5acc1c6ba5c9f86ac4f699f4c646ecae8bccaaa2a6b86bb0`  
		Last Modified: Tue, 17 Dec 2024 19:31:14 GMT  
		Size: 465.9 KB (465852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d125faf71663c9c259588da9545dcfc1d961e59d92ce5a9486c7d389cb61bc2c`  
		Last Modified: Tue, 17 Dec 2024 19:31:13 GMT  
		Size: 6.4 MB (6375751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f9b5ddb5fe65a52ed1c161189ff40d0273af9d50a8a6777a98abffd5b4f7d0`  
		Last Modified: Tue, 17 Dec 2024 19:31:12 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f6b8c72206232edf4922cfb68939224b12d0d8eb8e2e4c88e5e66875586d0b`  
		Last Modified: Tue, 17 Dec 2024 19:31:12 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6ec3b766844bacc1ba6a7d126a373851ec2b899f045cddd539bc7f1f7ffbd6`  
		Last Modified: Tue, 17 Dec 2024 19:31:12 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d656e63d77c756e50abf1d5d895ac8c06814dd594cc1bf16ea92894907949e`  
		Last Modified: Tue, 17 Dec 2024 19:31:12 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:358028020ee9c6b6ff8494f70ecbfddddf5b29d36bd20ec1b9b37eb351c46081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull nats@sha256:c6e3358af2d309d6c2ed2c4321b8d16f0c8c2b817d67b61e77790abeab192882
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2021024024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64938b4574dd9f4d28b0fdba70a6f3483c75359cd4de6fe307eaf6b4c9e6c5d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Tue, 17 Dec 2024 19:28:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 17 Dec 2024 19:28:54 GMT
ENV NATS_DOCKERIZED=1
# Tue, 17 Dec 2024 19:28:55 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 19:28:56 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.24/nats-server-v2.10.24-windows-amd64.zip
# Tue, 17 Dec 2024 19:28:57 GMT
ENV NATS_SERVER_SHASUM=bf94c9a9f1685147fd95f6c62f26d16fb72dc8c8c592e2d8c9115e2491c508c3
# Tue, 17 Dec 2024 19:30:38 GMT
RUN Set-PSDebug -Trace 2
# Tue, 17 Dec 2024 19:31:05 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 17 Dec 2024 19:31:06 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 17 Dec 2024 19:31:06 GMT
EXPOSE 4222 6222 8222
# Tue, 17 Dec 2024 19:31:07 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 17 Dec 2024 19:31:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995e898d38ff13b74b2bf42182403105bd564ca1c8cd3c2bccadac08c8172ca2`  
		Last Modified: Tue, 17 Dec 2024 19:31:15 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7f7d745fbcac3f49a978704fb067848ad5982ff0f7f116bfaceb8e9c68fbc7`  
		Last Modified: Tue, 17 Dec 2024 19:31:15 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0a5927c302d6e5e93a6570c06c06ce9862ef400bd5fea534fea403fd76e9b8`  
		Last Modified: Tue, 17 Dec 2024 19:31:13 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e7b1cd8a1d4aa5917755e9a51eb72256b93ddf6aa3825cbd84213d86f046d3`  
		Last Modified: Tue, 17 Dec 2024 19:31:13 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a76e8a87993daefe8a56da532e9ecac69a46fe935f34deac5f3e2ccff312c7`  
		Last Modified: Tue, 17 Dec 2024 19:31:13 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f37de67167c5db5acc1c6ba5c9f86ac4f699f4c646ecae8bccaaa2a6b86bb0`  
		Last Modified: Tue, 17 Dec 2024 19:31:14 GMT  
		Size: 465.9 KB (465852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d125faf71663c9c259588da9545dcfc1d961e59d92ce5a9486c7d389cb61bc2c`  
		Last Modified: Tue, 17 Dec 2024 19:31:13 GMT  
		Size: 6.4 MB (6375751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f9b5ddb5fe65a52ed1c161189ff40d0273af9d50a8a6777a98abffd5b4f7d0`  
		Last Modified: Tue, 17 Dec 2024 19:31:12 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f6b8c72206232edf4922cfb68939224b12d0d8eb8e2e4c88e5e66875586d0b`  
		Last Modified: Tue, 17 Dec 2024 19:31:12 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6ec3b766844bacc1ba6a7d126a373851ec2b899f045cddd539bc7f1f7ffbd6`  
		Last Modified: Tue, 17 Dec 2024 19:31:12 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d656e63d77c756e50abf1d5d895ac8c06814dd594cc1bf16ea92894907949e`  
		Last Modified: Tue, 17 Dec 2024 19:31:12 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10`

```console
$ docker pull nats@sha256:bc2b3f3198786445a692d868397d7229502fc445f9966136d76c4d065e473c04
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.17763.6659; amd64

### `nats:2.10` - linux; amd64

```console
$ docker pull nats@sha256:598ab684e8bafd4f4227ee552ce98bd196abf0cbf6afdc409f74f48886287bb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5905657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24ab2fdd6d375d97b62be28867989f387cc11050dcc31df27d4fa32b6b08e243`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2cb1f9bba9aff495d2f8a23661a6c1c7bc2c839cdc2be180b4b8d9bc9800c45e`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.9 MB (5905148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d543cdf7ef6e19ee24fcb0c663a82a570f5d76342cdbe1f16376e80658f531`  
		Last Modified: Tue, 07 Jan 2025 04:18:12 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:e7a69231651c265e8db70dc79d63ca27d50eff1c7d32be38202da1d315a624f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a5ad75f0ecaf5f3b903c67619e8421121692845fc51e699c386d8afbc9214d`

```dockerfile
```

-	Layers:
	-	`sha256:3b9fcbd5baa342487cc6ee0de074d83be1f60a7d04c5e296fd68ed85e1a4c76c`  
		Last Modified: Tue, 07 Jan 2025 04:18:12 GMT  
		Size: 10.5 KB (10472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; arm variant v6

```console
$ docker pull nats@sha256:f801151009502a85c381ffc3e3d4da1b39a338bd804445dbab92e447a8d0742d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5dab6565a7ccd5e8b79dd46bc5519aff76b27bfd17665dd3ab08500446ae12c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:81fd6ecec75a6718f55afc7801f7191a8b41d70739a2651f877929f41efcd454`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.6 MB (5553927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4aef5e79acad5215cfeb435fcd7a420447cc550b3045715dcd97efb7cb374f`  
		Last Modified: Tue, 17 Dec 2024 20:07:21 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:aa392b8671143c697cdb326a2e6c742a067761c4db93860f234dc5b35ed0fb11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:976493cfd43ca3f9a8ad5279956a0080949b50282eecf7a444c4fda93c34322f`

```dockerfile
```

-	Layers:
	-	`sha256:8c2857f8ddfd44360797a8c21b94d211d9d2a7db67740cdb79c8c10aa235b398`  
		Last Modified: Tue, 17 Dec 2024 20:07:21 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; arm variant v7

```console
$ docker pull nats@sha256:982d1d42158b250be7f9650713a8ce7f79bfcba19c04673b21aa2677f187e826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5541946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a6a2dc3f5ef13e36babac38a18c93a6285238679ddf644b3a3f7a5e9e2b29f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:85a1620c1bc6892b5d6c70da117024f4e8fd52994270c35fc7e84782f9682593`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.5 MB (5541438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cdb512b6ca4232a2dd947f49e124f42a6360977706249ce886b49eaba3d3658`  
		Last Modified: Tue, 17 Dec 2024 20:07:18 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:f9eaffb5a7d57be14405ae9a378201ab9a8b8f29afc536e0f8cc6212a74b1a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4afd2190878f0bf2aaadb3cf3fc2a325ccf406cb5223de0922fb20c9f55782d`

```dockerfile
```

-	Layers:
	-	`sha256:163a6014f277c730d1ebece60d800e1889e07231871cc75ab28b5544c87be3b1`  
		Last Modified: Tue, 17 Dec 2024 20:07:18 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:46cc8aa9b94b2de214209442d6cb1e771affdf42d871cfe81596929f23ab15a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5454197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a567c1ed7c844d528fb5acbc5c0388776a9735d231544b5281c56981009f7b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d0b7f1d89d35acbd261abd0ec2bcf54bcc65bb79ebf006850dc5cfae55765a62`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.5 MB (5453688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714d2581a122d6579083f834fb3cf2cea0ad605e1a1ea3cabc5e99db033a0de9`  
		Last Modified: Tue, 17 Dec 2024 23:47:32 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:f41b9f81c4ad1bf1332a199acd507a5e89a4a0d44aa0b141c1d31a41c940b3b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87666fbe34385bd1ec5ac0f209512cd54596dc5cae712d1600dbbb2ea2fcb91e`

```dockerfile
```

-	Layers:
	-	`sha256:c7ee9e2eebe3c624616f634e065612ab6d6e9395b5694f040d1fba9e93e18fec`  
		Last Modified: Tue, 17 Dec 2024 23:47:32 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; ppc64le

```console
$ docker pull nats@sha256:bf4bc17ce581fbc555448128b270a270364f08c1fa916496cdf12b90741ebcbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5418848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61ba372cd7f008492fffa212def1194d605e85849146fc8141f2f60a3935332d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:72b285162443e680327c1bf58de30e30459f3f8193b0769fd1fad6f4f115b124`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.4 MB (5418340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49171e380cf318294924933ba7552fde576651ba45f06690772f99bd0d09c62`  
		Last Modified: Tue, 07 Jan 2025 09:49:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:65d7ddac6a9451045689180537020395f325928967d57be7f680d41e62bfbc7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26558754194d57e26e105533c268c9dd4e5f229090f32bab381f786d5c1ab504`

```dockerfile
```

-	Layers:
	-	`sha256:5db6af784b78d60900035a04e99b70041ea3ee04c0eabcc41b60160cd2933452`  
		Last Modified: Tue, 07 Jan 2025 09:49:22 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; s390x

```console
$ docker pull nats@sha256:a82b5907b071519d7add42e0ff6632ee3ea5ad1152c0f3432ee682f4954e38f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5748559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:064b066d0f376d269a70742585b50ba3cd7c177611f92c629f158e2df7944418`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bd4119cb6f8c6b49f3ec55933200d2283d0f58b8b79bb753e5436770b7c2b320`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.7 MB (5748050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afd816dca497faa2937925ee17de8bdaa1530e524721a18bf0e7838bd7f6c2e`  
		Last Modified: Tue, 17 Dec 2024 20:07:57 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:c28225ad7ee2152f11088957130764b2ca530f01b73f693afc238a553b29d443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f772a80018515b59b3c7005be4f7c9bdc3a6a48167750b803269d3bf711e8f08`

```dockerfile
```

-	Layers:
	-	`sha256:9de3e5757b559fa1c5cba102c651c66e5db5e3b5889139d5508a670b2b9f07d5`  
		Last Modified: Tue, 17 Dec 2024 20:07:57 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - windows version 10.0.17763.6659; amd64

```console
$ docker pull nats@sha256:a3bf98913be025c2083ebd5687c133ab5b00f3a1894a3fe2231a87894b64bed0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161263273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50684e4ed1bf0d28623bfd52d2bfd9a7c4111c83ceaabd37a09cbf397e675281`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 04:54:21 GMT
RUN Apply image 10.0.17763.6659
# Tue, 17 Dec 2024 20:08:15 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 17 Dec 2024 20:08:18 GMT
RUN cmd /S /C #(nop) COPY file:32d2c78f0dd94e383b45881b640cf1b2c9c27decb4a66e09babbe6a0f796087f in C:\nats-server.exe 
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 17 Dec 2024 20:08:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fc1cdf36537340b1875b5d6573a58a268fc20b63dc54a780f9070e51cf9eb9ca`  
		Last Modified: Tue, 10 Dec 2024 21:03:34 GMT  
		Size: 155.2 MB (155231618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f2ef448a775bed9c6f05668d734eb51754170fdfc93c55c99bbaa763bf0d4e`  
		Last Modified: Tue, 17 Dec 2024 20:08:26 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe350f8421c39c736eb0f8180693ff45eedcd35a224bc510bd2626a0996409b`  
		Last Modified: Tue, 17 Dec 2024 20:08:25 GMT  
		Size: 6.0 MB (6025803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd8a7a90698ba96911ac6344eb5f5dd88c4dfebd29047be607133fadef68165`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.7 KB (1671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f84b1a718e07866b0c5d7f7666c682f746339824f50d2010237f8129d983c34`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be4b8e9d23c6bed197e181271e99e2a123100ad014b841f2409aaa51fe58303`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52cb4f7ea4c581f0a9e1eb6519dba6818337a039607974ce3fd7131a13ea51b0`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine`

```console
$ docker pull nats@sha256:1ae474d1c029d61d5ad7b170989ab048bc157b8d3ef173d9c8dda10431f4c66a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.10-alpine` - linux; amd64

```console
$ docker pull nats@sha256:e75e15a642407b176cda44b593952a650099bbffced18ac86e1da0adb45a815c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9984940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09fd7f582707a2da49e3e73d42a6397c85ea95b6e58a615a5f0bf1a3780834b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.1-x86_64.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:245043d9199c263f869fc0558f43f7cb98bbc92acdd5def1b4f690adc0ac7807`  
		Last Modified: Mon, 06 Jan 2025 21:44:42 GMT  
		Size: 3.6 MB (3636222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13a0d0824643f0161fd224aceb130343bf44e238a29f9f1cac440eb4b097701c`  
		Last Modified: Tue, 07 Jan 2025 03:20:06 GMT  
		Size: 6.3 MB (6347749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5413da9dd68b96d78c2f9a6ad90c83c10eba4927bfcf99f8812ea179a093c146`  
		Last Modified: Tue, 07 Jan 2025 03:20:06 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdba86b0d45f2bc8262ff57e28b3781caf6b47e078a80f3e89f03f05b9eac8a4`  
		Last Modified: Tue, 07 Jan 2025 03:20:06 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:74e3d1c872d5047663341b23e819482b2bf389190102cfdb5f2b5a10c87a0f08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb0055da207991572098ff5f84511e527c4057fa58cf40e1311b9013d4db18e6`

```dockerfile
```

-	Layers:
	-	`sha256:301c11a8c0e0cb7a10b31ed266709ff88d4cb1d04b4b773cda7d7a7af0a919ee`  
		Last Modified: Tue, 07 Jan 2025 03:20:07 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:56cbfc79edf7b2c7aa940cfd6f7383d3f0acd1d20aef967f001ded5079cb2b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9361190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a44eaada784dc01cb9c5f57575b9f22ece42b1f2885e166714a4ec2a677ee2bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.1-armhf.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:31d4a7f5d4e2c1fd6b13116c69b324d9255a249ba92b63cd7d98924ec5438675`  
		Last Modified: Tue, 07 Jan 2025 02:29:34 GMT  
		Size: 3.4 MB (3361034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3aeae20c738cb0545c05b726c587c76393b9a553968be75b99d583e66a7775b`  
		Last Modified: Tue, 07 Jan 2025 03:58:09 GMT  
		Size: 6.0 MB (5999180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ec491cee3b9736e33232b0eeecad77b992ef16de691db662b0b61774f8b73c`  
		Last Modified: Tue, 07 Jan 2025 03:58:08 GMT  
		Size: 564.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03aa8832feccfdad9eba1b2d0cfeabfbc22bd7ac1eb3047e9e71b63a38bb09c`  
		Last Modified: Tue, 07 Jan 2025 03:58:08 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:cb2eb11b7181517ab509ea8b21a459285feee2175862c053b04ac04c56ca29a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13da7c14ff3fa5a48c56b744564d8ee8a26501609ee8b4a5c1f30b63e89fcb91`

```dockerfile
```

-	Layers:
	-	`sha256:df8f81133a2bf850bec9c382e906dfc869f01f7c98b59587a49715e9aeb29498`  
		Last Modified: Tue, 07 Jan 2025 03:58:08 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:fdfe42e62e2b79b73f65039202fe3229e6cb71c69e82a64080c440b9707cedd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9080587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1588e3d1330f032c6efe96bdb72b0f9179e37f26f272bac3d8f53f11bef3cbff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.1-armv7.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fa398bd1707194d783a6221bb60ba630f074222cdc0f4b6a05d9167d6e9c4a9f`  
		Last Modified: Tue, 07 Jan 2025 02:55:27 GMT  
		Size: 3.1 MB (3093241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f00f9faabc3557dcc5a09506016607206ccc43235c52c7f039f0f569067899f`  
		Last Modified: Tue, 07 Jan 2025 03:43:07 GMT  
		Size: 6.0 MB (5986376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ec44d2ed6879601786756e72d73f99cde8e79fa55e16f1af107519e800da9e`  
		Last Modified: Tue, 07 Jan 2025 03:43:06 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e68cbd6292db04b815b0b4f504cc27d37888065829ba6187ed1b81146b0f8b`  
		Last Modified: Tue, 07 Jan 2025 03:43:06 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:42c8ebef1cfc8b8f2fb88adcab48268298580a6b1c7994bc90ecc0e85eaee6be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb1d3dff94118ce66c8f8e7273533a5489d0907af8d4d1c08d15b86a65ef9aa`

```dockerfile
```

-	Layers:
	-	`sha256:16ef13af5efe22a4816752712e3aa06f4d2e9e998d253a67358a93a82bf88c3b`  
		Last Modified: Tue, 07 Jan 2025 03:43:06 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a3bd4772713e383733977b42d0bdfde71d8bc73298b3043639c042161e7b3ce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9885113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80637e8b5cf4194cba52d82998bac00c029971bb34fc5be960598a7483cd5d67`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:707c94c90c597447ce10a36c9b56355c1cc67d0cf593a592daeb419d99a30d85`  
		Last Modified: Tue, 07 Jan 2025 03:02:50 GMT  
		Size: 4.0 MB (3983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81dca03c14249dbcca7f333b7af01e9e99db8e96d6c9d2f2bde6d66c7e329324`  
		Last Modified: Tue, 07 Jan 2025 04:20:26 GMT  
		Size: 5.9 MB (5901137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9545f2b071c52dcf93362ddf8c114680a82ab925c1a0404a1ced42ca02cf81c`  
		Last Modified: Tue, 07 Jan 2025 04:20:26 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22af105e2b54631c9d3d6f803af860c168d3e5cc35a5fa5be13328311c288cc8`  
		Last Modified: Tue, 07 Jan 2025 04:20:26 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:b33a75f3a131215546c5e5051f64d1da52efc1df0668a9807a8e69112eac7f54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d468c758973e805c31c177ab74b4029804f634f063c47cfb99ff25d3cf499b`

```dockerfile
```

-	Layers:
	-	`sha256:6179800d5433282d408054d0574571874af30c964b865ce8caa292b6df2ade56`  
		Last Modified: Tue, 07 Jan 2025 04:20:26 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:5d7ae4028ab12c2a74b8a7c331e4ccb0eae01a94d682cc65b60b8fd51c43d223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9432907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc3b47e1a998b06b497b8d3d4573199f0385b0f9bfe7543c284b47f05acebb66`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.1-ppc64le.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9207393f0daad55cddbc775f55edde5baecdca9e0441c9c1f627f2394d28b7c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:05 GMT  
		Size: 3.6 MB (3567745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acef6d00c5d9f955c0ada0042b4d702b198dc599a72773715bec6a5deab07ba2`  
		Last Modified: Tue, 07 Jan 2025 03:50:51 GMT  
		Size: 5.9 MB (5864192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce5db60d75e59b4b4f0e79bcd3c707843e4f174e155467ba9c768426b98a398`  
		Last Modified: Tue, 07 Jan 2025 03:50:51 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d120b1f8dd2ce33447645c1b4328c2d88cbb5d570c67bc161cc99b05f5c68e`  
		Last Modified: Tue, 07 Jan 2025 03:50:51 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:c9feafae7ef54aa6e4379a8e78a32c28c988b91724d91bb48524d6e2f396d67f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e39d2f23f56f144fffc66e26c856f03cde7d644a740c82397b8866f918db873d`

```dockerfile
```

-	Layers:
	-	`sha256:f681712c35cd291126837bbcdeb41fc7871fc45035d8dec9395bd27034b3d520`  
		Last Modified: Tue, 07 Jan 2025 03:50:51 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; s390x

```console
$ docker pull nats@sha256:4649a608cb9cdfc49ebb039d6ea36cd89a3ef0c6e2ce1402f3d2c24a9a221225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9653226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b55dcbb50fac7b108734557067c71c07e62274db299fe32ec263b9e11f2cb59`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.1-s390x.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:93a724ed1843277c272a09a7779ca31a802938fe3a88142df42e291e0dc759c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:17 GMT  
		Size: 3.5 MB (3459449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723f4bf7823ff55b05e1545bb39271fc9629e9d17ec83b14c487b1bc1feaf66e`  
		Last Modified: Tue, 07 Jan 2025 03:45:59 GMT  
		Size: 6.2 MB (6192808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8625174e21f292a47f2bb46a59b4d41f57a796cd52926234c718dd0556f08a54`  
		Last Modified: Tue, 07 Jan 2025 03:45:59 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b2c4e11055e3b9000f33288affd900fabde3b220edf8fbff0d50687fa637b06`  
		Last Modified: Tue, 07 Jan 2025 03:45:59 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:d952184708e04933d2b5631eb5fd04bdd74ca4e384122fa926fb8f74b34d0d93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e29dff1272c5b181c168004dd85e6068f54151252615c50a09ef6dff321104a9`

```dockerfile
```

-	Layers:
	-	`sha256:6ff141856e7b853dc1f812064b76dbb06f3dfb468f1dfa89312a9f106434e96f`  
		Last Modified: Tue, 07 Jan 2025 03:45:59 GMT  
		Size: 14.3 KB (14321 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-alpine3.21`

```console
$ docker pull nats@sha256:1ae474d1c029d61d5ad7b170989ab048bc157b8d3ef173d9c8dda10431f4c66a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.10-alpine3.21` - linux; amd64

```console
$ docker pull nats@sha256:e75e15a642407b176cda44b593952a650099bbffced18ac86e1da0adb45a815c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9984940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09fd7f582707a2da49e3e73d42a6397c85ea95b6e58a615a5f0bf1a3780834b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.1-x86_64.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:245043d9199c263f869fc0558f43f7cb98bbc92acdd5def1b4f690adc0ac7807`  
		Last Modified: Mon, 06 Jan 2025 21:44:42 GMT  
		Size: 3.6 MB (3636222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13a0d0824643f0161fd224aceb130343bf44e238a29f9f1cac440eb4b097701c`  
		Last Modified: Tue, 07 Jan 2025 03:20:06 GMT  
		Size: 6.3 MB (6347749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5413da9dd68b96d78c2f9a6ad90c83c10eba4927bfcf99f8812ea179a093c146`  
		Last Modified: Tue, 07 Jan 2025 03:20:06 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdba86b0d45f2bc8262ff57e28b3781caf6b47e078a80f3e89f03f05b9eac8a4`  
		Last Modified: Tue, 07 Jan 2025 03:20:06 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:74e3d1c872d5047663341b23e819482b2bf389190102cfdb5f2b5a10c87a0f08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb0055da207991572098ff5f84511e527c4057fa58cf40e1311b9013d4db18e6`

```dockerfile
```

-	Layers:
	-	`sha256:301c11a8c0e0cb7a10b31ed266709ff88d4cb1d04b4b773cda7d7a7af0a919ee`  
		Last Modified: Tue, 07 Jan 2025 03:20:07 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:56cbfc79edf7b2c7aa940cfd6f7383d3f0acd1d20aef967f001ded5079cb2b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9361190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a44eaada784dc01cb9c5f57575b9f22ece42b1f2885e166714a4ec2a677ee2bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.1-armhf.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:31d4a7f5d4e2c1fd6b13116c69b324d9255a249ba92b63cd7d98924ec5438675`  
		Last Modified: Tue, 07 Jan 2025 02:29:34 GMT  
		Size: 3.4 MB (3361034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3aeae20c738cb0545c05b726c587c76393b9a553968be75b99d583e66a7775b`  
		Last Modified: Tue, 07 Jan 2025 03:58:09 GMT  
		Size: 6.0 MB (5999180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ec491cee3b9736e33232b0eeecad77b992ef16de691db662b0b61774f8b73c`  
		Last Modified: Tue, 07 Jan 2025 03:58:08 GMT  
		Size: 564.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03aa8832feccfdad9eba1b2d0cfeabfbc22bd7ac1eb3047e9e71b63a38bb09c`  
		Last Modified: Tue, 07 Jan 2025 03:58:08 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:cb2eb11b7181517ab509ea8b21a459285feee2175862c053b04ac04c56ca29a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13da7c14ff3fa5a48c56b744564d8ee8a26501609ee8b4a5c1f30b63e89fcb91`

```dockerfile
```

-	Layers:
	-	`sha256:df8f81133a2bf850bec9c382e906dfc869f01f7c98b59587a49715e9aeb29498`  
		Last Modified: Tue, 07 Jan 2025 03:58:08 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:fdfe42e62e2b79b73f65039202fe3229e6cb71c69e82a64080c440b9707cedd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9080587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1588e3d1330f032c6efe96bdb72b0f9179e37f26f272bac3d8f53f11bef3cbff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.1-armv7.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fa398bd1707194d783a6221bb60ba630f074222cdc0f4b6a05d9167d6e9c4a9f`  
		Last Modified: Tue, 07 Jan 2025 02:55:27 GMT  
		Size: 3.1 MB (3093241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f00f9faabc3557dcc5a09506016607206ccc43235c52c7f039f0f569067899f`  
		Last Modified: Tue, 07 Jan 2025 03:43:07 GMT  
		Size: 6.0 MB (5986376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ec44d2ed6879601786756e72d73f99cde8e79fa55e16f1af107519e800da9e`  
		Last Modified: Tue, 07 Jan 2025 03:43:06 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e68cbd6292db04b815b0b4f504cc27d37888065829ba6187ed1b81146b0f8b`  
		Last Modified: Tue, 07 Jan 2025 03:43:06 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:42c8ebef1cfc8b8f2fb88adcab48268298580a6b1c7994bc90ecc0e85eaee6be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb1d3dff94118ce66c8f8e7273533a5489d0907af8d4d1c08d15b86a65ef9aa`

```dockerfile
```

-	Layers:
	-	`sha256:16ef13af5efe22a4816752712e3aa06f4d2e9e998d253a67358a93a82bf88c3b`  
		Last Modified: Tue, 07 Jan 2025 03:43:06 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a3bd4772713e383733977b42d0bdfde71d8bc73298b3043639c042161e7b3ce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9885113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80637e8b5cf4194cba52d82998bac00c029971bb34fc5be960598a7483cd5d67`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:707c94c90c597447ce10a36c9b56355c1cc67d0cf593a592daeb419d99a30d85`  
		Last Modified: Tue, 07 Jan 2025 03:02:50 GMT  
		Size: 4.0 MB (3983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81dca03c14249dbcca7f333b7af01e9e99db8e96d6c9d2f2bde6d66c7e329324`  
		Last Modified: Tue, 07 Jan 2025 04:20:26 GMT  
		Size: 5.9 MB (5901137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9545f2b071c52dcf93362ddf8c114680a82ab925c1a0404a1ced42ca02cf81c`  
		Last Modified: Tue, 07 Jan 2025 04:20:26 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22af105e2b54631c9d3d6f803af860c168d3e5cc35a5fa5be13328311c288cc8`  
		Last Modified: Tue, 07 Jan 2025 04:20:26 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:b33a75f3a131215546c5e5051f64d1da52efc1df0668a9807a8e69112eac7f54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d468c758973e805c31c177ab74b4029804f634f063c47cfb99ff25d3cf499b`

```dockerfile
```

-	Layers:
	-	`sha256:6179800d5433282d408054d0574571874af30c964b865ce8caa292b6df2ade56`  
		Last Modified: Tue, 07 Jan 2025 04:20:26 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:5d7ae4028ab12c2a74b8a7c331e4ccb0eae01a94d682cc65b60b8fd51c43d223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9432907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc3b47e1a998b06b497b8d3d4573199f0385b0f9bfe7543c284b47f05acebb66`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.1-ppc64le.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9207393f0daad55cddbc775f55edde5baecdca9e0441c9c1f627f2394d28b7c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:05 GMT  
		Size: 3.6 MB (3567745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acef6d00c5d9f955c0ada0042b4d702b198dc599a72773715bec6a5deab07ba2`  
		Last Modified: Tue, 07 Jan 2025 03:50:51 GMT  
		Size: 5.9 MB (5864192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce5db60d75e59b4b4f0e79bcd3c707843e4f174e155467ba9c768426b98a398`  
		Last Modified: Tue, 07 Jan 2025 03:50:51 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d120b1f8dd2ce33447645c1b4328c2d88cbb5d570c67bc161cc99b05f5c68e`  
		Last Modified: Tue, 07 Jan 2025 03:50:51 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:c9feafae7ef54aa6e4379a8e78a32c28c988b91724d91bb48524d6e2f396d67f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e39d2f23f56f144fffc66e26c856f03cde7d644a740c82397b8866f918db873d`

```dockerfile
```

-	Layers:
	-	`sha256:f681712c35cd291126837bbcdeb41fc7871fc45035d8dec9395bd27034b3d520`  
		Last Modified: Tue, 07 Jan 2025 03:50:51 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:4649a608cb9cdfc49ebb039d6ea36cd89a3ef0c6e2ce1402f3d2c24a9a221225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9653226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b55dcbb50fac7b108734557067c71c07e62274db299fe32ec263b9e11f2cb59`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.1-s390x.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:93a724ed1843277c272a09a7779ca31a802938fe3a88142df42e291e0dc759c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:17 GMT  
		Size: 3.5 MB (3459449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723f4bf7823ff55b05e1545bb39271fc9629e9d17ec83b14c487b1bc1feaf66e`  
		Last Modified: Tue, 07 Jan 2025 03:45:59 GMT  
		Size: 6.2 MB (6192808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8625174e21f292a47f2bb46a59b4d41f57a796cd52926234c718dd0556f08a54`  
		Last Modified: Tue, 07 Jan 2025 03:45:59 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b2c4e11055e3b9000f33288affd900fabde3b220edf8fbff0d50687fa637b06`  
		Last Modified: Tue, 07 Jan 2025 03:45:59 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:d952184708e04933d2b5631eb5fd04bdd74ca4e384122fa926fb8f74b34d0d93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e29dff1272c5b181c168004dd85e6068f54151252615c50a09ef6dff321104a9`

```dockerfile
```

-	Layers:
	-	`sha256:6ff141856e7b853dc1f812064b76dbb06f3dfb468f1dfa89312a9f106434e96f`  
		Last Modified: Tue, 07 Jan 2025 03:45:59 GMT  
		Size: 14.3 KB (14321 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-linux`

```console
$ docker pull nats@sha256:c597fb1c0dbee32f6092767e6550bc6f458d011aa48f8467f483161208b853ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.10-linux` - linux; amd64

```console
$ docker pull nats@sha256:598ab684e8bafd4f4227ee552ce98bd196abf0cbf6afdc409f74f48886287bb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5905657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24ab2fdd6d375d97b62be28867989f387cc11050dcc31df27d4fa32b6b08e243`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2cb1f9bba9aff495d2f8a23661a6c1c7bc2c839cdc2be180b4b8d9bc9800c45e`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.9 MB (5905148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d543cdf7ef6e19ee24fcb0c663a82a570f5d76342cdbe1f16376e80658f531`  
		Last Modified: Tue, 07 Jan 2025 04:18:12 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:e7a69231651c265e8db70dc79d63ca27d50eff1c7d32be38202da1d315a624f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a5ad75f0ecaf5f3b903c67619e8421121692845fc51e699c386d8afbc9214d`

```dockerfile
```

-	Layers:
	-	`sha256:3b9fcbd5baa342487cc6ee0de074d83be1f60a7d04c5e296fd68ed85e1a4c76c`  
		Last Modified: Tue, 07 Jan 2025 04:18:12 GMT  
		Size: 10.5 KB (10472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:f801151009502a85c381ffc3e3d4da1b39a338bd804445dbab92e447a8d0742d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5dab6565a7ccd5e8b79dd46bc5519aff76b27bfd17665dd3ab08500446ae12c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:81fd6ecec75a6718f55afc7801f7191a8b41d70739a2651f877929f41efcd454`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.6 MB (5553927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4aef5e79acad5215cfeb435fcd7a420447cc550b3045715dcd97efb7cb374f`  
		Last Modified: Tue, 17 Dec 2024 20:07:21 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:aa392b8671143c697cdb326a2e6c742a067761c4db93860f234dc5b35ed0fb11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:976493cfd43ca3f9a8ad5279956a0080949b50282eecf7a444c4fda93c34322f`

```dockerfile
```

-	Layers:
	-	`sha256:8c2857f8ddfd44360797a8c21b94d211d9d2a7db67740cdb79c8c10aa235b398`  
		Last Modified: Tue, 17 Dec 2024 20:07:21 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:982d1d42158b250be7f9650713a8ce7f79bfcba19c04673b21aa2677f187e826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5541946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a6a2dc3f5ef13e36babac38a18c93a6285238679ddf644b3a3f7a5e9e2b29f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:85a1620c1bc6892b5d6c70da117024f4e8fd52994270c35fc7e84782f9682593`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.5 MB (5541438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cdb512b6ca4232a2dd947f49e124f42a6360977706249ce886b49eaba3d3658`  
		Last Modified: Tue, 17 Dec 2024 20:07:18 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:f9eaffb5a7d57be14405ae9a378201ab9a8b8f29afc536e0f8cc6212a74b1a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4afd2190878f0bf2aaadb3cf3fc2a325ccf406cb5223de0922fb20c9f55782d`

```dockerfile
```

-	Layers:
	-	`sha256:163a6014f277c730d1ebece60d800e1889e07231871cc75ab28b5544c87be3b1`  
		Last Modified: Tue, 17 Dec 2024 20:07:18 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:46cc8aa9b94b2de214209442d6cb1e771affdf42d871cfe81596929f23ab15a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5454197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a567c1ed7c844d528fb5acbc5c0388776a9735d231544b5281c56981009f7b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d0b7f1d89d35acbd261abd0ec2bcf54bcc65bb79ebf006850dc5cfae55765a62`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.5 MB (5453688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714d2581a122d6579083f834fb3cf2cea0ad605e1a1ea3cabc5e99db033a0de9`  
		Last Modified: Tue, 17 Dec 2024 23:47:32 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:f41b9f81c4ad1bf1332a199acd507a5e89a4a0d44aa0b141c1d31a41c940b3b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87666fbe34385bd1ec5ac0f209512cd54596dc5cae712d1600dbbb2ea2fcb91e`

```dockerfile
```

-	Layers:
	-	`sha256:c7ee9e2eebe3c624616f634e065612ab6d6e9395b5694f040d1fba9e93e18fec`  
		Last Modified: Tue, 17 Dec 2024 23:47:32 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:bf4bc17ce581fbc555448128b270a270364f08c1fa916496cdf12b90741ebcbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5418848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61ba372cd7f008492fffa212def1194d605e85849146fc8141f2f60a3935332d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:72b285162443e680327c1bf58de30e30459f3f8193b0769fd1fad6f4f115b124`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.4 MB (5418340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49171e380cf318294924933ba7552fde576651ba45f06690772f99bd0d09c62`  
		Last Modified: Tue, 07 Jan 2025 09:49:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:65d7ddac6a9451045689180537020395f325928967d57be7f680d41e62bfbc7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26558754194d57e26e105533c268c9dd4e5f229090f32bab381f786d5c1ab504`

```dockerfile
```

-	Layers:
	-	`sha256:5db6af784b78d60900035a04e99b70041ea3ee04c0eabcc41b60160cd2933452`  
		Last Modified: Tue, 07 Jan 2025 09:49:22 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; s390x

```console
$ docker pull nats@sha256:a82b5907b071519d7add42e0ff6632ee3ea5ad1152c0f3432ee682f4954e38f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5748559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:064b066d0f376d269a70742585b50ba3cd7c177611f92c629f158e2df7944418`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bd4119cb6f8c6b49f3ec55933200d2283d0f58b8b79bb753e5436770b7c2b320`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.7 MB (5748050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afd816dca497faa2937925ee17de8bdaa1530e524721a18bf0e7838bd7f6c2e`  
		Last Modified: Tue, 17 Dec 2024 20:07:57 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:c28225ad7ee2152f11088957130764b2ca530f01b73f693afc238a553b29d443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f772a80018515b59b3c7005be4f7c9bdc3a6a48167750b803269d3bf711e8f08`

```dockerfile
```

-	Layers:
	-	`sha256:9de3e5757b559fa1c5cba102c651c66e5db5e3b5889139d5508a670b2b9f07d5`  
		Last Modified: Tue, 17 Dec 2024 20:07:57 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-nanoserver`

```console
$ docker pull nats@sha256:37e1b8a8d0e258480f2b4e3e528c51625f7c66283ec06ca04228db3a08fa024e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `nats:2.10-nanoserver` - windows version 10.0.17763.6659; amd64

```console
$ docker pull nats@sha256:a3bf98913be025c2083ebd5687c133ab5b00f3a1894a3fe2231a87894b64bed0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161263273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50684e4ed1bf0d28623bfd52d2bfd9a7c4111c83ceaabd37a09cbf397e675281`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 04:54:21 GMT
RUN Apply image 10.0.17763.6659
# Tue, 17 Dec 2024 20:08:15 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 17 Dec 2024 20:08:18 GMT
RUN cmd /S /C #(nop) COPY file:32d2c78f0dd94e383b45881b640cf1b2c9c27decb4a66e09babbe6a0f796087f in C:\nats-server.exe 
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 17 Dec 2024 20:08:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fc1cdf36537340b1875b5d6573a58a268fc20b63dc54a780f9070e51cf9eb9ca`  
		Last Modified: Tue, 10 Dec 2024 21:03:34 GMT  
		Size: 155.2 MB (155231618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f2ef448a775bed9c6f05668d734eb51754170fdfc93c55c99bbaa763bf0d4e`  
		Last Modified: Tue, 17 Dec 2024 20:08:26 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe350f8421c39c736eb0f8180693ff45eedcd35a224bc510bd2626a0996409b`  
		Last Modified: Tue, 17 Dec 2024 20:08:25 GMT  
		Size: 6.0 MB (6025803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd8a7a90698ba96911ac6344eb5f5dd88c4dfebd29047be607133fadef68165`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.7 KB (1671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f84b1a718e07866b0c5d7f7666c682f746339824f50d2010237f8129d983c34`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be4b8e9d23c6bed197e181271e99e2a123100ad014b841f2409aaa51fe58303`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52cb4f7ea4c581f0a9e1eb6519dba6818337a039607974ce3fd7131a13ea51b0`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-nanoserver-1809`

```console
$ docker pull nats@sha256:37e1b8a8d0e258480f2b4e3e528c51625f7c66283ec06ca04228db3a08fa024e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `nats:2.10-nanoserver-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull nats@sha256:a3bf98913be025c2083ebd5687c133ab5b00f3a1894a3fe2231a87894b64bed0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161263273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50684e4ed1bf0d28623bfd52d2bfd9a7c4111c83ceaabd37a09cbf397e675281`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 04:54:21 GMT
RUN Apply image 10.0.17763.6659
# Tue, 17 Dec 2024 20:08:15 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 17 Dec 2024 20:08:18 GMT
RUN cmd /S /C #(nop) COPY file:32d2c78f0dd94e383b45881b640cf1b2c9c27decb4a66e09babbe6a0f796087f in C:\nats-server.exe 
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 17 Dec 2024 20:08:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fc1cdf36537340b1875b5d6573a58a268fc20b63dc54a780f9070e51cf9eb9ca`  
		Last Modified: Tue, 10 Dec 2024 21:03:34 GMT  
		Size: 155.2 MB (155231618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f2ef448a775bed9c6f05668d734eb51754170fdfc93c55c99bbaa763bf0d4e`  
		Last Modified: Tue, 17 Dec 2024 20:08:26 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe350f8421c39c736eb0f8180693ff45eedcd35a224bc510bd2626a0996409b`  
		Last Modified: Tue, 17 Dec 2024 20:08:25 GMT  
		Size: 6.0 MB (6025803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd8a7a90698ba96911ac6344eb5f5dd88c4dfebd29047be607133fadef68165`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.7 KB (1671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f84b1a718e07866b0c5d7f7666c682f746339824f50d2010237f8129d983c34`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be4b8e9d23c6bed197e181271e99e2a123100ad014b841f2409aaa51fe58303`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52cb4f7ea4c581f0a9e1eb6519dba6818337a039607974ce3fd7131a13ea51b0`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-scratch`

```console
$ docker pull nats@sha256:c597fb1c0dbee32f6092767e6550bc6f458d011aa48f8467f483161208b853ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.10-scratch` - linux; amd64

```console
$ docker pull nats@sha256:598ab684e8bafd4f4227ee552ce98bd196abf0cbf6afdc409f74f48886287bb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5905657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24ab2fdd6d375d97b62be28867989f387cc11050dcc31df27d4fa32b6b08e243`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2cb1f9bba9aff495d2f8a23661a6c1c7bc2c839cdc2be180b4b8d9bc9800c45e`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.9 MB (5905148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d543cdf7ef6e19ee24fcb0c663a82a570f5d76342cdbe1f16376e80658f531`  
		Last Modified: Tue, 07 Jan 2025 04:18:12 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:e7a69231651c265e8db70dc79d63ca27d50eff1c7d32be38202da1d315a624f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a5ad75f0ecaf5f3b903c67619e8421121692845fc51e699c386d8afbc9214d`

```dockerfile
```

-	Layers:
	-	`sha256:3b9fcbd5baa342487cc6ee0de074d83be1f60a7d04c5e296fd68ed85e1a4c76c`  
		Last Modified: Tue, 07 Jan 2025 04:18:12 GMT  
		Size: 10.5 KB (10472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:f801151009502a85c381ffc3e3d4da1b39a338bd804445dbab92e447a8d0742d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5dab6565a7ccd5e8b79dd46bc5519aff76b27bfd17665dd3ab08500446ae12c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:81fd6ecec75a6718f55afc7801f7191a8b41d70739a2651f877929f41efcd454`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.6 MB (5553927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4aef5e79acad5215cfeb435fcd7a420447cc550b3045715dcd97efb7cb374f`  
		Last Modified: Tue, 17 Dec 2024 20:07:21 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:aa392b8671143c697cdb326a2e6c742a067761c4db93860f234dc5b35ed0fb11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:976493cfd43ca3f9a8ad5279956a0080949b50282eecf7a444c4fda93c34322f`

```dockerfile
```

-	Layers:
	-	`sha256:8c2857f8ddfd44360797a8c21b94d211d9d2a7db67740cdb79c8c10aa235b398`  
		Last Modified: Tue, 17 Dec 2024 20:07:21 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:982d1d42158b250be7f9650713a8ce7f79bfcba19c04673b21aa2677f187e826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5541946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a6a2dc3f5ef13e36babac38a18c93a6285238679ddf644b3a3f7a5e9e2b29f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:85a1620c1bc6892b5d6c70da117024f4e8fd52994270c35fc7e84782f9682593`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.5 MB (5541438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cdb512b6ca4232a2dd947f49e124f42a6360977706249ce886b49eaba3d3658`  
		Last Modified: Tue, 17 Dec 2024 20:07:18 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:f9eaffb5a7d57be14405ae9a378201ab9a8b8f29afc536e0f8cc6212a74b1a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4afd2190878f0bf2aaadb3cf3fc2a325ccf406cb5223de0922fb20c9f55782d`

```dockerfile
```

-	Layers:
	-	`sha256:163a6014f277c730d1ebece60d800e1889e07231871cc75ab28b5544c87be3b1`  
		Last Modified: Tue, 17 Dec 2024 20:07:18 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:46cc8aa9b94b2de214209442d6cb1e771affdf42d871cfe81596929f23ab15a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5454197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a567c1ed7c844d528fb5acbc5c0388776a9735d231544b5281c56981009f7b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d0b7f1d89d35acbd261abd0ec2bcf54bcc65bb79ebf006850dc5cfae55765a62`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.5 MB (5453688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714d2581a122d6579083f834fb3cf2cea0ad605e1a1ea3cabc5e99db033a0de9`  
		Last Modified: Tue, 17 Dec 2024 23:47:32 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:f41b9f81c4ad1bf1332a199acd507a5e89a4a0d44aa0b141c1d31a41c940b3b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87666fbe34385bd1ec5ac0f209512cd54596dc5cae712d1600dbbb2ea2fcb91e`

```dockerfile
```

-	Layers:
	-	`sha256:c7ee9e2eebe3c624616f634e065612ab6d6e9395b5694f040d1fba9e93e18fec`  
		Last Modified: Tue, 17 Dec 2024 23:47:32 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:bf4bc17ce581fbc555448128b270a270364f08c1fa916496cdf12b90741ebcbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5418848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61ba372cd7f008492fffa212def1194d605e85849146fc8141f2f60a3935332d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:72b285162443e680327c1bf58de30e30459f3f8193b0769fd1fad6f4f115b124`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.4 MB (5418340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49171e380cf318294924933ba7552fde576651ba45f06690772f99bd0d09c62`  
		Last Modified: Tue, 07 Jan 2025 09:49:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:65d7ddac6a9451045689180537020395f325928967d57be7f680d41e62bfbc7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26558754194d57e26e105533c268c9dd4e5f229090f32bab381f786d5c1ab504`

```dockerfile
```

-	Layers:
	-	`sha256:5db6af784b78d60900035a04e99b70041ea3ee04c0eabcc41b60160cd2933452`  
		Last Modified: Tue, 07 Jan 2025 09:49:22 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; s390x

```console
$ docker pull nats@sha256:a82b5907b071519d7add42e0ff6632ee3ea5ad1152c0f3432ee682f4954e38f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5748559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:064b066d0f376d269a70742585b50ba3cd7c177611f92c629f158e2df7944418`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bd4119cb6f8c6b49f3ec55933200d2283d0f58b8b79bb753e5436770b7c2b320`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.7 MB (5748050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afd816dca497faa2937925ee17de8bdaa1530e524721a18bf0e7838bd7f6c2e`  
		Last Modified: Tue, 17 Dec 2024 20:07:57 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:c28225ad7ee2152f11088957130764b2ca530f01b73f693afc238a553b29d443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f772a80018515b59b3c7005be4f7c9bdc3a6a48167750b803269d3bf711e8f08`

```dockerfile
```

-	Layers:
	-	`sha256:9de3e5757b559fa1c5cba102c651c66e5db5e3b5889139d5508a670b2b9f07d5`  
		Last Modified: Tue, 17 Dec 2024 20:07:57 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-windowsservercore`

```console
$ docker pull nats@sha256:358028020ee9c6b6ff8494f70ecbfddddf5b29d36bd20ec1b9b37eb351c46081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `nats:2.10-windowsservercore` - windows version 10.0.17763.6659; amd64

```console
$ docker pull nats@sha256:c6e3358af2d309d6c2ed2c4321b8d16f0c8c2b817d67b61e77790abeab192882
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2021024024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64938b4574dd9f4d28b0fdba70a6f3483c75359cd4de6fe307eaf6b4c9e6c5d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Tue, 17 Dec 2024 19:28:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 17 Dec 2024 19:28:54 GMT
ENV NATS_DOCKERIZED=1
# Tue, 17 Dec 2024 19:28:55 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 19:28:56 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.24/nats-server-v2.10.24-windows-amd64.zip
# Tue, 17 Dec 2024 19:28:57 GMT
ENV NATS_SERVER_SHASUM=bf94c9a9f1685147fd95f6c62f26d16fb72dc8c8c592e2d8c9115e2491c508c3
# Tue, 17 Dec 2024 19:30:38 GMT
RUN Set-PSDebug -Trace 2
# Tue, 17 Dec 2024 19:31:05 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 17 Dec 2024 19:31:06 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 17 Dec 2024 19:31:06 GMT
EXPOSE 4222 6222 8222
# Tue, 17 Dec 2024 19:31:07 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 17 Dec 2024 19:31:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995e898d38ff13b74b2bf42182403105bd564ca1c8cd3c2bccadac08c8172ca2`  
		Last Modified: Tue, 17 Dec 2024 19:31:15 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7f7d745fbcac3f49a978704fb067848ad5982ff0f7f116bfaceb8e9c68fbc7`  
		Last Modified: Tue, 17 Dec 2024 19:31:15 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0a5927c302d6e5e93a6570c06c06ce9862ef400bd5fea534fea403fd76e9b8`  
		Last Modified: Tue, 17 Dec 2024 19:31:13 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e7b1cd8a1d4aa5917755e9a51eb72256b93ddf6aa3825cbd84213d86f046d3`  
		Last Modified: Tue, 17 Dec 2024 19:31:13 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a76e8a87993daefe8a56da532e9ecac69a46fe935f34deac5f3e2ccff312c7`  
		Last Modified: Tue, 17 Dec 2024 19:31:13 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f37de67167c5db5acc1c6ba5c9f86ac4f699f4c646ecae8bccaaa2a6b86bb0`  
		Last Modified: Tue, 17 Dec 2024 19:31:14 GMT  
		Size: 465.9 KB (465852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d125faf71663c9c259588da9545dcfc1d961e59d92ce5a9486c7d389cb61bc2c`  
		Last Modified: Tue, 17 Dec 2024 19:31:13 GMT  
		Size: 6.4 MB (6375751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f9b5ddb5fe65a52ed1c161189ff40d0273af9d50a8a6777a98abffd5b4f7d0`  
		Last Modified: Tue, 17 Dec 2024 19:31:12 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f6b8c72206232edf4922cfb68939224b12d0d8eb8e2e4c88e5e66875586d0b`  
		Last Modified: Tue, 17 Dec 2024 19:31:12 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6ec3b766844bacc1ba6a7d126a373851ec2b899f045cddd539bc7f1f7ffbd6`  
		Last Modified: Tue, 17 Dec 2024 19:31:12 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d656e63d77c756e50abf1d5d895ac8c06814dd594cc1bf16ea92894907949e`  
		Last Modified: Tue, 17 Dec 2024 19:31:12 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-windowsservercore-1809`

```console
$ docker pull nats@sha256:358028020ee9c6b6ff8494f70ecbfddddf5b29d36bd20ec1b9b37eb351c46081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `nats:2.10-windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull nats@sha256:c6e3358af2d309d6c2ed2c4321b8d16f0c8c2b817d67b61e77790abeab192882
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2021024024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64938b4574dd9f4d28b0fdba70a6f3483c75359cd4de6fe307eaf6b4c9e6c5d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Tue, 17 Dec 2024 19:28:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 17 Dec 2024 19:28:54 GMT
ENV NATS_DOCKERIZED=1
# Tue, 17 Dec 2024 19:28:55 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 19:28:56 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.24/nats-server-v2.10.24-windows-amd64.zip
# Tue, 17 Dec 2024 19:28:57 GMT
ENV NATS_SERVER_SHASUM=bf94c9a9f1685147fd95f6c62f26d16fb72dc8c8c592e2d8c9115e2491c508c3
# Tue, 17 Dec 2024 19:30:38 GMT
RUN Set-PSDebug -Trace 2
# Tue, 17 Dec 2024 19:31:05 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 17 Dec 2024 19:31:06 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 17 Dec 2024 19:31:06 GMT
EXPOSE 4222 6222 8222
# Tue, 17 Dec 2024 19:31:07 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 17 Dec 2024 19:31:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995e898d38ff13b74b2bf42182403105bd564ca1c8cd3c2bccadac08c8172ca2`  
		Last Modified: Tue, 17 Dec 2024 19:31:15 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7f7d745fbcac3f49a978704fb067848ad5982ff0f7f116bfaceb8e9c68fbc7`  
		Last Modified: Tue, 17 Dec 2024 19:31:15 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0a5927c302d6e5e93a6570c06c06ce9862ef400bd5fea534fea403fd76e9b8`  
		Last Modified: Tue, 17 Dec 2024 19:31:13 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e7b1cd8a1d4aa5917755e9a51eb72256b93ddf6aa3825cbd84213d86f046d3`  
		Last Modified: Tue, 17 Dec 2024 19:31:13 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a76e8a87993daefe8a56da532e9ecac69a46fe935f34deac5f3e2ccff312c7`  
		Last Modified: Tue, 17 Dec 2024 19:31:13 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f37de67167c5db5acc1c6ba5c9f86ac4f699f4c646ecae8bccaaa2a6b86bb0`  
		Last Modified: Tue, 17 Dec 2024 19:31:14 GMT  
		Size: 465.9 KB (465852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d125faf71663c9c259588da9545dcfc1d961e59d92ce5a9486c7d389cb61bc2c`  
		Last Modified: Tue, 17 Dec 2024 19:31:13 GMT  
		Size: 6.4 MB (6375751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f9b5ddb5fe65a52ed1c161189ff40d0273af9d50a8a6777a98abffd5b4f7d0`  
		Last Modified: Tue, 17 Dec 2024 19:31:12 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f6b8c72206232edf4922cfb68939224b12d0d8eb8e2e4c88e5e66875586d0b`  
		Last Modified: Tue, 17 Dec 2024 19:31:12 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6ec3b766844bacc1ba6a7d126a373851ec2b899f045cddd539bc7f1f7ffbd6`  
		Last Modified: Tue, 17 Dec 2024 19:31:12 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d656e63d77c756e50abf1d5d895ac8c06814dd594cc1bf16ea92894907949e`  
		Last Modified: Tue, 17 Dec 2024 19:31:12 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.24`

```console
$ docker pull nats@sha256:bc2b3f3198786445a692d868397d7229502fc445f9966136d76c4d065e473c04
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.17763.6659; amd64

### `nats:2.10.24` - linux; amd64

```console
$ docker pull nats@sha256:598ab684e8bafd4f4227ee552ce98bd196abf0cbf6afdc409f74f48886287bb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5905657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24ab2fdd6d375d97b62be28867989f387cc11050dcc31df27d4fa32b6b08e243`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2cb1f9bba9aff495d2f8a23661a6c1c7bc2c839cdc2be180b4b8d9bc9800c45e`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.9 MB (5905148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d543cdf7ef6e19ee24fcb0c663a82a570f5d76342cdbe1f16376e80658f531`  
		Last Modified: Tue, 07 Jan 2025 04:18:12 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24` - unknown; unknown

```console
$ docker pull nats@sha256:e7a69231651c265e8db70dc79d63ca27d50eff1c7d32be38202da1d315a624f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a5ad75f0ecaf5f3b903c67619e8421121692845fc51e699c386d8afbc9214d`

```dockerfile
```

-	Layers:
	-	`sha256:3b9fcbd5baa342487cc6ee0de074d83be1f60a7d04c5e296fd68ed85e1a4c76c`  
		Last Modified: Tue, 07 Jan 2025 04:18:12 GMT  
		Size: 10.5 KB (10472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.24` - linux; arm variant v6

```console
$ docker pull nats@sha256:f801151009502a85c381ffc3e3d4da1b39a338bd804445dbab92e447a8d0742d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5dab6565a7ccd5e8b79dd46bc5519aff76b27bfd17665dd3ab08500446ae12c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:81fd6ecec75a6718f55afc7801f7191a8b41d70739a2651f877929f41efcd454`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.6 MB (5553927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4aef5e79acad5215cfeb435fcd7a420447cc550b3045715dcd97efb7cb374f`  
		Last Modified: Tue, 17 Dec 2024 20:07:21 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24` - unknown; unknown

```console
$ docker pull nats@sha256:aa392b8671143c697cdb326a2e6c742a067761c4db93860f234dc5b35ed0fb11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:976493cfd43ca3f9a8ad5279956a0080949b50282eecf7a444c4fda93c34322f`

```dockerfile
```

-	Layers:
	-	`sha256:8c2857f8ddfd44360797a8c21b94d211d9d2a7db67740cdb79c8c10aa235b398`  
		Last Modified: Tue, 17 Dec 2024 20:07:21 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.24` - linux; arm variant v7

```console
$ docker pull nats@sha256:982d1d42158b250be7f9650713a8ce7f79bfcba19c04673b21aa2677f187e826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5541946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a6a2dc3f5ef13e36babac38a18c93a6285238679ddf644b3a3f7a5e9e2b29f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:85a1620c1bc6892b5d6c70da117024f4e8fd52994270c35fc7e84782f9682593`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.5 MB (5541438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cdb512b6ca4232a2dd947f49e124f42a6360977706249ce886b49eaba3d3658`  
		Last Modified: Tue, 17 Dec 2024 20:07:18 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24` - unknown; unknown

```console
$ docker pull nats@sha256:f9eaffb5a7d57be14405ae9a378201ab9a8b8f29afc536e0f8cc6212a74b1a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4afd2190878f0bf2aaadb3cf3fc2a325ccf406cb5223de0922fb20c9f55782d`

```dockerfile
```

-	Layers:
	-	`sha256:163a6014f277c730d1ebece60d800e1889e07231871cc75ab28b5544c87be3b1`  
		Last Modified: Tue, 17 Dec 2024 20:07:18 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.24` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:46cc8aa9b94b2de214209442d6cb1e771affdf42d871cfe81596929f23ab15a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5454197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a567c1ed7c844d528fb5acbc5c0388776a9735d231544b5281c56981009f7b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d0b7f1d89d35acbd261abd0ec2bcf54bcc65bb79ebf006850dc5cfae55765a62`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.5 MB (5453688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714d2581a122d6579083f834fb3cf2cea0ad605e1a1ea3cabc5e99db033a0de9`  
		Last Modified: Tue, 17 Dec 2024 23:47:32 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24` - unknown; unknown

```console
$ docker pull nats@sha256:f41b9f81c4ad1bf1332a199acd507a5e89a4a0d44aa0b141c1d31a41c940b3b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87666fbe34385bd1ec5ac0f209512cd54596dc5cae712d1600dbbb2ea2fcb91e`

```dockerfile
```

-	Layers:
	-	`sha256:c7ee9e2eebe3c624616f634e065612ab6d6e9395b5694f040d1fba9e93e18fec`  
		Last Modified: Tue, 17 Dec 2024 23:47:32 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.24` - linux; ppc64le

```console
$ docker pull nats@sha256:bf4bc17ce581fbc555448128b270a270364f08c1fa916496cdf12b90741ebcbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5418848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61ba372cd7f008492fffa212def1194d605e85849146fc8141f2f60a3935332d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:72b285162443e680327c1bf58de30e30459f3f8193b0769fd1fad6f4f115b124`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.4 MB (5418340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49171e380cf318294924933ba7552fde576651ba45f06690772f99bd0d09c62`  
		Last Modified: Tue, 07 Jan 2025 09:49:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24` - unknown; unknown

```console
$ docker pull nats@sha256:65d7ddac6a9451045689180537020395f325928967d57be7f680d41e62bfbc7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26558754194d57e26e105533c268c9dd4e5f229090f32bab381f786d5c1ab504`

```dockerfile
```

-	Layers:
	-	`sha256:5db6af784b78d60900035a04e99b70041ea3ee04c0eabcc41b60160cd2933452`  
		Last Modified: Tue, 07 Jan 2025 09:49:22 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.24` - linux; s390x

```console
$ docker pull nats@sha256:a82b5907b071519d7add42e0ff6632ee3ea5ad1152c0f3432ee682f4954e38f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5748559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:064b066d0f376d269a70742585b50ba3cd7c177611f92c629f158e2df7944418`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bd4119cb6f8c6b49f3ec55933200d2283d0f58b8b79bb753e5436770b7c2b320`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.7 MB (5748050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afd816dca497faa2937925ee17de8bdaa1530e524721a18bf0e7838bd7f6c2e`  
		Last Modified: Tue, 17 Dec 2024 20:07:57 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24` - unknown; unknown

```console
$ docker pull nats@sha256:c28225ad7ee2152f11088957130764b2ca530f01b73f693afc238a553b29d443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f772a80018515b59b3c7005be4f7c9bdc3a6a48167750b803269d3bf711e8f08`

```dockerfile
```

-	Layers:
	-	`sha256:9de3e5757b559fa1c5cba102c651c66e5db5e3b5889139d5508a670b2b9f07d5`  
		Last Modified: Tue, 17 Dec 2024 20:07:57 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.24` - windows version 10.0.17763.6659; amd64

```console
$ docker pull nats@sha256:a3bf98913be025c2083ebd5687c133ab5b00f3a1894a3fe2231a87894b64bed0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161263273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50684e4ed1bf0d28623bfd52d2bfd9a7c4111c83ceaabd37a09cbf397e675281`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 04:54:21 GMT
RUN Apply image 10.0.17763.6659
# Tue, 17 Dec 2024 20:08:15 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 17 Dec 2024 20:08:18 GMT
RUN cmd /S /C #(nop) COPY file:32d2c78f0dd94e383b45881b640cf1b2c9c27decb4a66e09babbe6a0f796087f in C:\nats-server.exe 
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 17 Dec 2024 20:08:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fc1cdf36537340b1875b5d6573a58a268fc20b63dc54a780f9070e51cf9eb9ca`  
		Last Modified: Tue, 10 Dec 2024 21:03:34 GMT  
		Size: 155.2 MB (155231618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f2ef448a775bed9c6f05668d734eb51754170fdfc93c55c99bbaa763bf0d4e`  
		Last Modified: Tue, 17 Dec 2024 20:08:26 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe350f8421c39c736eb0f8180693ff45eedcd35a224bc510bd2626a0996409b`  
		Last Modified: Tue, 17 Dec 2024 20:08:25 GMT  
		Size: 6.0 MB (6025803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd8a7a90698ba96911ac6344eb5f5dd88c4dfebd29047be607133fadef68165`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.7 KB (1671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f84b1a718e07866b0c5d7f7666c682f746339824f50d2010237f8129d983c34`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be4b8e9d23c6bed197e181271e99e2a123100ad014b841f2409aaa51fe58303`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52cb4f7ea4c581f0a9e1eb6519dba6818337a039607974ce3fd7131a13ea51b0`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.24-alpine`

```console
$ docker pull nats@sha256:1ae474d1c029d61d5ad7b170989ab048bc157b8d3ef173d9c8dda10431f4c66a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.10.24-alpine` - linux; amd64

```console
$ docker pull nats@sha256:e75e15a642407b176cda44b593952a650099bbffced18ac86e1da0adb45a815c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9984940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09fd7f582707a2da49e3e73d42a6397c85ea95b6e58a615a5f0bf1a3780834b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.1-x86_64.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:245043d9199c263f869fc0558f43f7cb98bbc92acdd5def1b4f690adc0ac7807`  
		Last Modified: Mon, 06 Jan 2025 21:44:42 GMT  
		Size: 3.6 MB (3636222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13a0d0824643f0161fd224aceb130343bf44e238a29f9f1cac440eb4b097701c`  
		Last Modified: Tue, 07 Jan 2025 03:20:06 GMT  
		Size: 6.3 MB (6347749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5413da9dd68b96d78c2f9a6ad90c83c10eba4927bfcf99f8812ea179a093c146`  
		Last Modified: Tue, 07 Jan 2025 03:20:06 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdba86b0d45f2bc8262ff57e28b3781caf6b47e078a80f3e89f03f05b9eac8a4`  
		Last Modified: Tue, 07 Jan 2025 03:20:06 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:74e3d1c872d5047663341b23e819482b2bf389190102cfdb5f2b5a10c87a0f08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb0055da207991572098ff5f84511e527c4057fa58cf40e1311b9013d4db18e6`

```dockerfile
```

-	Layers:
	-	`sha256:301c11a8c0e0cb7a10b31ed266709ff88d4cb1d04b4b773cda7d7a7af0a919ee`  
		Last Modified: Tue, 07 Jan 2025 03:20:07 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.24-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:56cbfc79edf7b2c7aa940cfd6f7383d3f0acd1d20aef967f001ded5079cb2b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9361190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a44eaada784dc01cb9c5f57575b9f22ece42b1f2885e166714a4ec2a677ee2bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.1-armhf.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:31d4a7f5d4e2c1fd6b13116c69b324d9255a249ba92b63cd7d98924ec5438675`  
		Last Modified: Tue, 07 Jan 2025 02:29:34 GMT  
		Size: 3.4 MB (3361034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3aeae20c738cb0545c05b726c587c76393b9a553968be75b99d583e66a7775b`  
		Last Modified: Tue, 07 Jan 2025 03:58:09 GMT  
		Size: 6.0 MB (5999180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ec491cee3b9736e33232b0eeecad77b992ef16de691db662b0b61774f8b73c`  
		Last Modified: Tue, 07 Jan 2025 03:58:08 GMT  
		Size: 564.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03aa8832feccfdad9eba1b2d0cfeabfbc22bd7ac1eb3047e9e71b63a38bb09c`  
		Last Modified: Tue, 07 Jan 2025 03:58:08 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:cb2eb11b7181517ab509ea8b21a459285feee2175862c053b04ac04c56ca29a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13da7c14ff3fa5a48c56b744564d8ee8a26501609ee8b4a5c1f30b63e89fcb91`

```dockerfile
```

-	Layers:
	-	`sha256:df8f81133a2bf850bec9c382e906dfc869f01f7c98b59587a49715e9aeb29498`  
		Last Modified: Tue, 07 Jan 2025 03:58:08 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.24-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:fdfe42e62e2b79b73f65039202fe3229e6cb71c69e82a64080c440b9707cedd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9080587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1588e3d1330f032c6efe96bdb72b0f9179e37f26f272bac3d8f53f11bef3cbff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.1-armv7.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fa398bd1707194d783a6221bb60ba630f074222cdc0f4b6a05d9167d6e9c4a9f`  
		Last Modified: Tue, 07 Jan 2025 02:55:27 GMT  
		Size: 3.1 MB (3093241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f00f9faabc3557dcc5a09506016607206ccc43235c52c7f039f0f569067899f`  
		Last Modified: Tue, 07 Jan 2025 03:43:07 GMT  
		Size: 6.0 MB (5986376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ec44d2ed6879601786756e72d73f99cde8e79fa55e16f1af107519e800da9e`  
		Last Modified: Tue, 07 Jan 2025 03:43:06 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e68cbd6292db04b815b0b4f504cc27d37888065829ba6187ed1b81146b0f8b`  
		Last Modified: Tue, 07 Jan 2025 03:43:06 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:42c8ebef1cfc8b8f2fb88adcab48268298580a6b1c7994bc90ecc0e85eaee6be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb1d3dff94118ce66c8f8e7273533a5489d0907af8d4d1c08d15b86a65ef9aa`

```dockerfile
```

-	Layers:
	-	`sha256:16ef13af5efe22a4816752712e3aa06f4d2e9e998d253a67358a93a82bf88c3b`  
		Last Modified: Tue, 07 Jan 2025 03:43:06 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.24-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a3bd4772713e383733977b42d0bdfde71d8bc73298b3043639c042161e7b3ce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9885113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80637e8b5cf4194cba52d82998bac00c029971bb34fc5be960598a7483cd5d67`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:707c94c90c597447ce10a36c9b56355c1cc67d0cf593a592daeb419d99a30d85`  
		Last Modified: Tue, 07 Jan 2025 03:02:50 GMT  
		Size: 4.0 MB (3983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81dca03c14249dbcca7f333b7af01e9e99db8e96d6c9d2f2bde6d66c7e329324`  
		Last Modified: Tue, 07 Jan 2025 04:20:26 GMT  
		Size: 5.9 MB (5901137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9545f2b071c52dcf93362ddf8c114680a82ab925c1a0404a1ced42ca02cf81c`  
		Last Modified: Tue, 07 Jan 2025 04:20:26 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22af105e2b54631c9d3d6f803af860c168d3e5cc35a5fa5be13328311c288cc8`  
		Last Modified: Tue, 07 Jan 2025 04:20:26 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:b33a75f3a131215546c5e5051f64d1da52efc1df0668a9807a8e69112eac7f54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d468c758973e805c31c177ab74b4029804f634f063c47cfb99ff25d3cf499b`

```dockerfile
```

-	Layers:
	-	`sha256:6179800d5433282d408054d0574571874af30c964b865ce8caa292b6df2ade56`  
		Last Modified: Tue, 07 Jan 2025 04:20:26 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.24-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:5d7ae4028ab12c2a74b8a7c331e4ccb0eae01a94d682cc65b60b8fd51c43d223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9432907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc3b47e1a998b06b497b8d3d4573199f0385b0f9bfe7543c284b47f05acebb66`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.1-ppc64le.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9207393f0daad55cddbc775f55edde5baecdca9e0441c9c1f627f2394d28b7c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:05 GMT  
		Size: 3.6 MB (3567745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acef6d00c5d9f955c0ada0042b4d702b198dc599a72773715bec6a5deab07ba2`  
		Last Modified: Tue, 07 Jan 2025 03:50:51 GMT  
		Size: 5.9 MB (5864192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce5db60d75e59b4b4f0e79bcd3c707843e4f174e155467ba9c768426b98a398`  
		Last Modified: Tue, 07 Jan 2025 03:50:51 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d120b1f8dd2ce33447645c1b4328c2d88cbb5d570c67bc161cc99b05f5c68e`  
		Last Modified: Tue, 07 Jan 2025 03:50:51 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:c9feafae7ef54aa6e4379a8e78a32c28c988b91724d91bb48524d6e2f396d67f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e39d2f23f56f144fffc66e26c856f03cde7d644a740c82397b8866f918db873d`

```dockerfile
```

-	Layers:
	-	`sha256:f681712c35cd291126837bbcdeb41fc7871fc45035d8dec9395bd27034b3d520`  
		Last Modified: Tue, 07 Jan 2025 03:50:51 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.24-alpine` - linux; s390x

```console
$ docker pull nats@sha256:4649a608cb9cdfc49ebb039d6ea36cd89a3ef0c6e2ce1402f3d2c24a9a221225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9653226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b55dcbb50fac7b108734557067c71c07e62274db299fe32ec263b9e11f2cb59`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.1-s390x.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:93a724ed1843277c272a09a7779ca31a802938fe3a88142df42e291e0dc759c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:17 GMT  
		Size: 3.5 MB (3459449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723f4bf7823ff55b05e1545bb39271fc9629e9d17ec83b14c487b1bc1feaf66e`  
		Last Modified: Tue, 07 Jan 2025 03:45:59 GMT  
		Size: 6.2 MB (6192808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8625174e21f292a47f2bb46a59b4d41f57a796cd52926234c718dd0556f08a54`  
		Last Modified: Tue, 07 Jan 2025 03:45:59 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b2c4e11055e3b9000f33288affd900fabde3b220edf8fbff0d50687fa637b06`  
		Last Modified: Tue, 07 Jan 2025 03:45:59 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:d952184708e04933d2b5631eb5fd04bdd74ca4e384122fa926fb8f74b34d0d93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e29dff1272c5b181c168004dd85e6068f54151252615c50a09ef6dff321104a9`

```dockerfile
```

-	Layers:
	-	`sha256:6ff141856e7b853dc1f812064b76dbb06f3dfb468f1dfa89312a9f106434e96f`  
		Last Modified: Tue, 07 Jan 2025 03:45:59 GMT  
		Size: 14.3 KB (14321 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.24-alpine3.21`

```console
$ docker pull nats@sha256:1ae474d1c029d61d5ad7b170989ab048bc157b8d3ef173d9c8dda10431f4c66a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.10.24-alpine3.21` - linux; amd64

```console
$ docker pull nats@sha256:e75e15a642407b176cda44b593952a650099bbffced18ac86e1da0adb45a815c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9984940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09fd7f582707a2da49e3e73d42a6397c85ea95b6e58a615a5f0bf1a3780834b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.1-x86_64.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:245043d9199c263f869fc0558f43f7cb98bbc92acdd5def1b4f690adc0ac7807`  
		Last Modified: Mon, 06 Jan 2025 21:44:42 GMT  
		Size: 3.6 MB (3636222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13a0d0824643f0161fd224aceb130343bf44e238a29f9f1cac440eb4b097701c`  
		Last Modified: Tue, 07 Jan 2025 03:20:06 GMT  
		Size: 6.3 MB (6347749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5413da9dd68b96d78c2f9a6ad90c83c10eba4927bfcf99f8812ea179a093c146`  
		Last Modified: Tue, 07 Jan 2025 03:20:06 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdba86b0d45f2bc8262ff57e28b3781caf6b47e078a80f3e89f03f05b9eac8a4`  
		Last Modified: Tue, 07 Jan 2025 03:20:06 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:74e3d1c872d5047663341b23e819482b2bf389190102cfdb5f2b5a10c87a0f08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb0055da207991572098ff5f84511e527c4057fa58cf40e1311b9013d4db18e6`

```dockerfile
```

-	Layers:
	-	`sha256:301c11a8c0e0cb7a10b31ed266709ff88d4cb1d04b4b773cda7d7a7af0a919ee`  
		Last Modified: Tue, 07 Jan 2025 03:20:07 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.24-alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:56cbfc79edf7b2c7aa940cfd6f7383d3f0acd1d20aef967f001ded5079cb2b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9361190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a44eaada784dc01cb9c5f57575b9f22ece42b1f2885e166714a4ec2a677ee2bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.1-armhf.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:31d4a7f5d4e2c1fd6b13116c69b324d9255a249ba92b63cd7d98924ec5438675`  
		Last Modified: Tue, 07 Jan 2025 02:29:34 GMT  
		Size: 3.4 MB (3361034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3aeae20c738cb0545c05b726c587c76393b9a553968be75b99d583e66a7775b`  
		Last Modified: Tue, 07 Jan 2025 03:58:09 GMT  
		Size: 6.0 MB (5999180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ec491cee3b9736e33232b0eeecad77b992ef16de691db662b0b61774f8b73c`  
		Last Modified: Tue, 07 Jan 2025 03:58:08 GMT  
		Size: 564.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03aa8832feccfdad9eba1b2d0cfeabfbc22bd7ac1eb3047e9e71b63a38bb09c`  
		Last Modified: Tue, 07 Jan 2025 03:58:08 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:cb2eb11b7181517ab509ea8b21a459285feee2175862c053b04ac04c56ca29a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13da7c14ff3fa5a48c56b744564d8ee8a26501609ee8b4a5c1f30b63e89fcb91`

```dockerfile
```

-	Layers:
	-	`sha256:df8f81133a2bf850bec9c382e906dfc869f01f7c98b59587a49715e9aeb29498`  
		Last Modified: Tue, 07 Jan 2025 03:58:08 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.24-alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:fdfe42e62e2b79b73f65039202fe3229e6cb71c69e82a64080c440b9707cedd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9080587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1588e3d1330f032c6efe96bdb72b0f9179e37f26f272bac3d8f53f11bef3cbff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.1-armv7.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fa398bd1707194d783a6221bb60ba630f074222cdc0f4b6a05d9167d6e9c4a9f`  
		Last Modified: Tue, 07 Jan 2025 02:55:27 GMT  
		Size: 3.1 MB (3093241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f00f9faabc3557dcc5a09506016607206ccc43235c52c7f039f0f569067899f`  
		Last Modified: Tue, 07 Jan 2025 03:43:07 GMT  
		Size: 6.0 MB (5986376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ec44d2ed6879601786756e72d73f99cde8e79fa55e16f1af107519e800da9e`  
		Last Modified: Tue, 07 Jan 2025 03:43:06 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e68cbd6292db04b815b0b4f504cc27d37888065829ba6187ed1b81146b0f8b`  
		Last Modified: Tue, 07 Jan 2025 03:43:06 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:42c8ebef1cfc8b8f2fb88adcab48268298580a6b1c7994bc90ecc0e85eaee6be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb1d3dff94118ce66c8f8e7273533a5489d0907af8d4d1c08d15b86a65ef9aa`

```dockerfile
```

-	Layers:
	-	`sha256:16ef13af5efe22a4816752712e3aa06f4d2e9e998d253a67358a93a82bf88c3b`  
		Last Modified: Tue, 07 Jan 2025 03:43:06 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.24-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a3bd4772713e383733977b42d0bdfde71d8bc73298b3043639c042161e7b3ce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9885113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80637e8b5cf4194cba52d82998bac00c029971bb34fc5be960598a7483cd5d67`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:707c94c90c597447ce10a36c9b56355c1cc67d0cf593a592daeb419d99a30d85`  
		Last Modified: Tue, 07 Jan 2025 03:02:50 GMT  
		Size: 4.0 MB (3983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81dca03c14249dbcca7f333b7af01e9e99db8e96d6c9d2f2bde6d66c7e329324`  
		Last Modified: Tue, 07 Jan 2025 04:20:26 GMT  
		Size: 5.9 MB (5901137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9545f2b071c52dcf93362ddf8c114680a82ab925c1a0404a1ced42ca02cf81c`  
		Last Modified: Tue, 07 Jan 2025 04:20:26 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22af105e2b54631c9d3d6f803af860c168d3e5cc35a5fa5be13328311c288cc8`  
		Last Modified: Tue, 07 Jan 2025 04:20:26 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:b33a75f3a131215546c5e5051f64d1da52efc1df0668a9807a8e69112eac7f54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d468c758973e805c31c177ab74b4029804f634f063c47cfb99ff25d3cf499b`

```dockerfile
```

-	Layers:
	-	`sha256:6179800d5433282d408054d0574571874af30c964b865ce8caa292b6df2ade56`  
		Last Modified: Tue, 07 Jan 2025 04:20:26 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.24-alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:5d7ae4028ab12c2a74b8a7c331e4ccb0eae01a94d682cc65b60b8fd51c43d223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9432907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc3b47e1a998b06b497b8d3d4573199f0385b0f9bfe7543c284b47f05acebb66`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.1-ppc64le.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9207393f0daad55cddbc775f55edde5baecdca9e0441c9c1f627f2394d28b7c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:05 GMT  
		Size: 3.6 MB (3567745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acef6d00c5d9f955c0ada0042b4d702b198dc599a72773715bec6a5deab07ba2`  
		Last Modified: Tue, 07 Jan 2025 03:50:51 GMT  
		Size: 5.9 MB (5864192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce5db60d75e59b4b4f0e79bcd3c707843e4f174e155467ba9c768426b98a398`  
		Last Modified: Tue, 07 Jan 2025 03:50:51 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d120b1f8dd2ce33447645c1b4328c2d88cbb5d570c67bc161cc99b05f5c68e`  
		Last Modified: Tue, 07 Jan 2025 03:50:51 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:c9feafae7ef54aa6e4379a8e78a32c28c988b91724d91bb48524d6e2f396d67f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e39d2f23f56f144fffc66e26c856f03cde7d644a740c82397b8866f918db873d`

```dockerfile
```

-	Layers:
	-	`sha256:f681712c35cd291126837bbcdeb41fc7871fc45035d8dec9395bd27034b3d520`  
		Last Modified: Tue, 07 Jan 2025 03:50:51 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.24-alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:4649a608cb9cdfc49ebb039d6ea36cd89a3ef0c6e2ce1402f3d2c24a9a221225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9653226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b55dcbb50fac7b108734557067c71c07e62274db299fe32ec263b9e11f2cb59`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.1-s390x.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:93a724ed1843277c272a09a7779ca31a802938fe3a88142df42e291e0dc759c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:17 GMT  
		Size: 3.5 MB (3459449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723f4bf7823ff55b05e1545bb39271fc9629e9d17ec83b14c487b1bc1feaf66e`  
		Last Modified: Tue, 07 Jan 2025 03:45:59 GMT  
		Size: 6.2 MB (6192808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8625174e21f292a47f2bb46a59b4d41f57a796cd52926234c718dd0556f08a54`  
		Last Modified: Tue, 07 Jan 2025 03:45:59 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b2c4e11055e3b9000f33288affd900fabde3b220edf8fbff0d50687fa637b06`  
		Last Modified: Tue, 07 Jan 2025 03:45:59 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:d952184708e04933d2b5631eb5fd04bdd74ca4e384122fa926fb8f74b34d0d93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e29dff1272c5b181c168004dd85e6068f54151252615c50a09ef6dff321104a9`

```dockerfile
```

-	Layers:
	-	`sha256:6ff141856e7b853dc1f812064b76dbb06f3dfb468f1dfa89312a9f106434e96f`  
		Last Modified: Tue, 07 Jan 2025 03:45:59 GMT  
		Size: 14.3 KB (14321 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.24-linux`

```console
$ docker pull nats@sha256:c597fb1c0dbee32f6092767e6550bc6f458d011aa48f8467f483161208b853ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.10.24-linux` - linux; amd64

```console
$ docker pull nats@sha256:598ab684e8bafd4f4227ee552ce98bd196abf0cbf6afdc409f74f48886287bb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5905657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24ab2fdd6d375d97b62be28867989f387cc11050dcc31df27d4fa32b6b08e243`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2cb1f9bba9aff495d2f8a23661a6c1c7bc2c839cdc2be180b4b8d9bc9800c45e`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.9 MB (5905148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d543cdf7ef6e19ee24fcb0c663a82a570f5d76342cdbe1f16376e80658f531`  
		Last Modified: Tue, 07 Jan 2025 04:18:12 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24-linux` - unknown; unknown

```console
$ docker pull nats@sha256:e7a69231651c265e8db70dc79d63ca27d50eff1c7d32be38202da1d315a624f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a5ad75f0ecaf5f3b903c67619e8421121692845fc51e699c386d8afbc9214d`

```dockerfile
```

-	Layers:
	-	`sha256:3b9fcbd5baa342487cc6ee0de074d83be1f60a7d04c5e296fd68ed85e1a4c76c`  
		Last Modified: Tue, 07 Jan 2025 04:18:12 GMT  
		Size: 10.5 KB (10472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.24-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:f801151009502a85c381ffc3e3d4da1b39a338bd804445dbab92e447a8d0742d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5dab6565a7ccd5e8b79dd46bc5519aff76b27bfd17665dd3ab08500446ae12c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:81fd6ecec75a6718f55afc7801f7191a8b41d70739a2651f877929f41efcd454`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.6 MB (5553927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4aef5e79acad5215cfeb435fcd7a420447cc550b3045715dcd97efb7cb374f`  
		Last Modified: Tue, 17 Dec 2024 20:07:21 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24-linux` - unknown; unknown

```console
$ docker pull nats@sha256:aa392b8671143c697cdb326a2e6c742a067761c4db93860f234dc5b35ed0fb11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:976493cfd43ca3f9a8ad5279956a0080949b50282eecf7a444c4fda93c34322f`

```dockerfile
```

-	Layers:
	-	`sha256:8c2857f8ddfd44360797a8c21b94d211d9d2a7db67740cdb79c8c10aa235b398`  
		Last Modified: Tue, 17 Dec 2024 20:07:21 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.24-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:982d1d42158b250be7f9650713a8ce7f79bfcba19c04673b21aa2677f187e826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5541946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a6a2dc3f5ef13e36babac38a18c93a6285238679ddf644b3a3f7a5e9e2b29f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:85a1620c1bc6892b5d6c70da117024f4e8fd52994270c35fc7e84782f9682593`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.5 MB (5541438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cdb512b6ca4232a2dd947f49e124f42a6360977706249ce886b49eaba3d3658`  
		Last Modified: Tue, 17 Dec 2024 20:07:18 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24-linux` - unknown; unknown

```console
$ docker pull nats@sha256:f9eaffb5a7d57be14405ae9a378201ab9a8b8f29afc536e0f8cc6212a74b1a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4afd2190878f0bf2aaadb3cf3fc2a325ccf406cb5223de0922fb20c9f55782d`

```dockerfile
```

-	Layers:
	-	`sha256:163a6014f277c730d1ebece60d800e1889e07231871cc75ab28b5544c87be3b1`  
		Last Modified: Tue, 17 Dec 2024 20:07:18 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.24-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:46cc8aa9b94b2de214209442d6cb1e771affdf42d871cfe81596929f23ab15a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5454197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a567c1ed7c844d528fb5acbc5c0388776a9735d231544b5281c56981009f7b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d0b7f1d89d35acbd261abd0ec2bcf54bcc65bb79ebf006850dc5cfae55765a62`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.5 MB (5453688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714d2581a122d6579083f834fb3cf2cea0ad605e1a1ea3cabc5e99db033a0de9`  
		Last Modified: Tue, 17 Dec 2024 23:47:32 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24-linux` - unknown; unknown

```console
$ docker pull nats@sha256:f41b9f81c4ad1bf1332a199acd507a5e89a4a0d44aa0b141c1d31a41c940b3b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87666fbe34385bd1ec5ac0f209512cd54596dc5cae712d1600dbbb2ea2fcb91e`

```dockerfile
```

-	Layers:
	-	`sha256:c7ee9e2eebe3c624616f634e065612ab6d6e9395b5694f040d1fba9e93e18fec`  
		Last Modified: Tue, 17 Dec 2024 23:47:32 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.24-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:bf4bc17ce581fbc555448128b270a270364f08c1fa916496cdf12b90741ebcbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5418848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61ba372cd7f008492fffa212def1194d605e85849146fc8141f2f60a3935332d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:72b285162443e680327c1bf58de30e30459f3f8193b0769fd1fad6f4f115b124`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.4 MB (5418340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49171e380cf318294924933ba7552fde576651ba45f06690772f99bd0d09c62`  
		Last Modified: Tue, 07 Jan 2025 09:49:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24-linux` - unknown; unknown

```console
$ docker pull nats@sha256:65d7ddac6a9451045689180537020395f325928967d57be7f680d41e62bfbc7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26558754194d57e26e105533c268c9dd4e5f229090f32bab381f786d5c1ab504`

```dockerfile
```

-	Layers:
	-	`sha256:5db6af784b78d60900035a04e99b70041ea3ee04c0eabcc41b60160cd2933452`  
		Last Modified: Tue, 07 Jan 2025 09:49:22 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.24-linux` - linux; s390x

```console
$ docker pull nats@sha256:a82b5907b071519d7add42e0ff6632ee3ea5ad1152c0f3432ee682f4954e38f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5748559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:064b066d0f376d269a70742585b50ba3cd7c177611f92c629f158e2df7944418`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bd4119cb6f8c6b49f3ec55933200d2283d0f58b8b79bb753e5436770b7c2b320`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.7 MB (5748050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afd816dca497faa2937925ee17de8bdaa1530e524721a18bf0e7838bd7f6c2e`  
		Last Modified: Tue, 17 Dec 2024 20:07:57 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24-linux` - unknown; unknown

```console
$ docker pull nats@sha256:c28225ad7ee2152f11088957130764b2ca530f01b73f693afc238a553b29d443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f772a80018515b59b3c7005be4f7c9bdc3a6a48167750b803269d3bf711e8f08`

```dockerfile
```

-	Layers:
	-	`sha256:9de3e5757b559fa1c5cba102c651c66e5db5e3b5889139d5508a670b2b9f07d5`  
		Last Modified: Tue, 17 Dec 2024 20:07:57 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.24-nanoserver`

```console
$ docker pull nats@sha256:37e1b8a8d0e258480f2b4e3e528c51625f7c66283ec06ca04228db3a08fa024e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `nats:2.10.24-nanoserver` - windows version 10.0.17763.6659; amd64

```console
$ docker pull nats@sha256:a3bf98913be025c2083ebd5687c133ab5b00f3a1894a3fe2231a87894b64bed0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161263273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50684e4ed1bf0d28623bfd52d2bfd9a7c4111c83ceaabd37a09cbf397e675281`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 04:54:21 GMT
RUN Apply image 10.0.17763.6659
# Tue, 17 Dec 2024 20:08:15 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 17 Dec 2024 20:08:18 GMT
RUN cmd /S /C #(nop) COPY file:32d2c78f0dd94e383b45881b640cf1b2c9c27decb4a66e09babbe6a0f796087f in C:\nats-server.exe 
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 17 Dec 2024 20:08:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fc1cdf36537340b1875b5d6573a58a268fc20b63dc54a780f9070e51cf9eb9ca`  
		Last Modified: Tue, 10 Dec 2024 21:03:34 GMT  
		Size: 155.2 MB (155231618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f2ef448a775bed9c6f05668d734eb51754170fdfc93c55c99bbaa763bf0d4e`  
		Last Modified: Tue, 17 Dec 2024 20:08:26 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe350f8421c39c736eb0f8180693ff45eedcd35a224bc510bd2626a0996409b`  
		Last Modified: Tue, 17 Dec 2024 20:08:25 GMT  
		Size: 6.0 MB (6025803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd8a7a90698ba96911ac6344eb5f5dd88c4dfebd29047be607133fadef68165`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.7 KB (1671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f84b1a718e07866b0c5d7f7666c682f746339824f50d2010237f8129d983c34`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be4b8e9d23c6bed197e181271e99e2a123100ad014b841f2409aaa51fe58303`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52cb4f7ea4c581f0a9e1eb6519dba6818337a039607974ce3fd7131a13ea51b0`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.24-nanoserver-1809`

```console
$ docker pull nats@sha256:37e1b8a8d0e258480f2b4e3e528c51625f7c66283ec06ca04228db3a08fa024e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `nats:2.10.24-nanoserver-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull nats@sha256:a3bf98913be025c2083ebd5687c133ab5b00f3a1894a3fe2231a87894b64bed0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161263273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50684e4ed1bf0d28623bfd52d2bfd9a7c4111c83ceaabd37a09cbf397e675281`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 04:54:21 GMT
RUN Apply image 10.0.17763.6659
# Tue, 17 Dec 2024 20:08:15 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 17 Dec 2024 20:08:18 GMT
RUN cmd /S /C #(nop) COPY file:32d2c78f0dd94e383b45881b640cf1b2c9c27decb4a66e09babbe6a0f796087f in C:\nats-server.exe 
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 17 Dec 2024 20:08:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fc1cdf36537340b1875b5d6573a58a268fc20b63dc54a780f9070e51cf9eb9ca`  
		Last Modified: Tue, 10 Dec 2024 21:03:34 GMT  
		Size: 155.2 MB (155231618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f2ef448a775bed9c6f05668d734eb51754170fdfc93c55c99bbaa763bf0d4e`  
		Last Modified: Tue, 17 Dec 2024 20:08:26 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe350f8421c39c736eb0f8180693ff45eedcd35a224bc510bd2626a0996409b`  
		Last Modified: Tue, 17 Dec 2024 20:08:25 GMT  
		Size: 6.0 MB (6025803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd8a7a90698ba96911ac6344eb5f5dd88c4dfebd29047be607133fadef68165`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.7 KB (1671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f84b1a718e07866b0c5d7f7666c682f746339824f50d2010237f8129d983c34`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be4b8e9d23c6bed197e181271e99e2a123100ad014b841f2409aaa51fe58303`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52cb4f7ea4c581f0a9e1eb6519dba6818337a039607974ce3fd7131a13ea51b0`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.24-scratch`

```console
$ docker pull nats@sha256:c597fb1c0dbee32f6092767e6550bc6f458d011aa48f8467f483161208b853ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.10.24-scratch` - linux; amd64

```console
$ docker pull nats@sha256:598ab684e8bafd4f4227ee552ce98bd196abf0cbf6afdc409f74f48886287bb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5905657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24ab2fdd6d375d97b62be28867989f387cc11050dcc31df27d4fa32b6b08e243`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2cb1f9bba9aff495d2f8a23661a6c1c7bc2c839cdc2be180b4b8d9bc9800c45e`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.9 MB (5905148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d543cdf7ef6e19ee24fcb0c663a82a570f5d76342cdbe1f16376e80658f531`  
		Last Modified: Tue, 07 Jan 2025 04:18:12 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:e7a69231651c265e8db70dc79d63ca27d50eff1c7d32be38202da1d315a624f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a5ad75f0ecaf5f3b903c67619e8421121692845fc51e699c386d8afbc9214d`

```dockerfile
```

-	Layers:
	-	`sha256:3b9fcbd5baa342487cc6ee0de074d83be1f60a7d04c5e296fd68ed85e1a4c76c`  
		Last Modified: Tue, 07 Jan 2025 04:18:12 GMT  
		Size: 10.5 KB (10472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.24-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:f801151009502a85c381ffc3e3d4da1b39a338bd804445dbab92e447a8d0742d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5dab6565a7ccd5e8b79dd46bc5519aff76b27bfd17665dd3ab08500446ae12c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:81fd6ecec75a6718f55afc7801f7191a8b41d70739a2651f877929f41efcd454`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.6 MB (5553927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4aef5e79acad5215cfeb435fcd7a420447cc550b3045715dcd97efb7cb374f`  
		Last Modified: Tue, 17 Dec 2024 20:07:21 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:aa392b8671143c697cdb326a2e6c742a067761c4db93860f234dc5b35ed0fb11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:976493cfd43ca3f9a8ad5279956a0080949b50282eecf7a444c4fda93c34322f`

```dockerfile
```

-	Layers:
	-	`sha256:8c2857f8ddfd44360797a8c21b94d211d9d2a7db67740cdb79c8c10aa235b398`  
		Last Modified: Tue, 17 Dec 2024 20:07:21 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.24-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:982d1d42158b250be7f9650713a8ce7f79bfcba19c04673b21aa2677f187e826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5541946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a6a2dc3f5ef13e36babac38a18c93a6285238679ddf644b3a3f7a5e9e2b29f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:85a1620c1bc6892b5d6c70da117024f4e8fd52994270c35fc7e84782f9682593`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.5 MB (5541438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cdb512b6ca4232a2dd947f49e124f42a6360977706249ce886b49eaba3d3658`  
		Last Modified: Tue, 17 Dec 2024 20:07:18 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:f9eaffb5a7d57be14405ae9a378201ab9a8b8f29afc536e0f8cc6212a74b1a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4afd2190878f0bf2aaadb3cf3fc2a325ccf406cb5223de0922fb20c9f55782d`

```dockerfile
```

-	Layers:
	-	`sha256:163a6014f277c730d1ebece60d800e1889e07231871cc75ab28b5544c87be3b1`  
		Last Modified: Tue, 17 Dec 2024 20:07:18 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.24-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:46cc8aa9b94b2de214209442d6cb1e771affdf42d871cfe81596929f23ab15a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5454197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a567c1ed7c844d528fb5acbc5c0388776a9735d231544b5281c56981009f7b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d0b7f1d89d35acbd261abd0ec2bcf54bcc65bb79ebf006850dc5cfae55765a62`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.5 MB (5453688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714d2581a122d6579083f834fb3cf2cea0ad605e1a1ea3cabc5e99db033a0de9`  
		Last Modified: Tue, 17 Dec 2024 23:47:32 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:f41b9f81c4ad1bf1332a199acd507a5e89a4a0d44aa0b141c1d31a41c940b3b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87666fbe34385bd1ec5ac0f209512cd54596dc5cae712d1600dbbb2ea2fcb91e`

```dockerfile
```

-	Layers:
	-	`sha256:c7ee9e2eebe3c624616f634e065612ab6d6e9395b5694f040d1fba9e93e18fec`  
		Last Modified: Tue, 17 Dec 2024 23:47:32 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.24-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:bf4bc17ce581fbc555448128b270a270364f08c1fa916496cdf12b90741ebcbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5418848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61ba372cd7f008492fffa212def1194d605e85849146fc8141f2f60a3935332d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:72b285162443e680327c1bf58de30e30459f3f8193b0769fd1fad6f4f115b124`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.4 MB (5418340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49171e380cf318294924933ba7552fde576651ba45f06690772f99bd0d09c62`  
		Last Modified: Tue, 07 Jan 2025 09:49:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:65d7ddac6a9451045689180537020395f325928967d57be7f680d41e62bfbc7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26558754194d57e26e105533c268c9dd4e5f229090f32bab381f786d5c1ab504`

```dockerfile
```

-	Layers:
	-	`sha256:5db6af784b78d60900035a04e99b70041ea3ee04c0eabcc41b60160cd2933452`  
		Last Modified: Tue, 07 Jan 2025 09:49:22 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.24-scratch` - linux; s390x

```console
$ docker pull nats@sha256:a82b5907b071519d7add42e0ff6632ee3ea5ad1152c0f3432ee682f4954e38f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5748559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:064b066d0f376d269a70742585b50ba3cd7c177611f92c629f158e2df7944418`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bd4119cb6f8c6b49f3ec55933200d2283d0f58b8b79bb753e5436770b7c2b320`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.7 MB (5748050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afd816dca497faa2937925ee17de8bdaa1530e524721a18bf0e7838bd7f6c2e`  
		Last Modified: Tue, 17 Dec 2024 20:07:57 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:c28225ad7ee2152f11088957130764b2ca530f01b73f693afc238a553b29d443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f772a80018515b59b3c7005be4f7c9bdc3a6a48167750b803269d3bf711e8f08`

```dockerfile
```

-	Layers:
	-	`sha256:9de3e5757b559fa1c5cba102c651c66e5db5e3b5889139d5508a670b2b9f07d5`  
		Last Modified: Tue, 17 Dec 2024 20:07:57 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.24-windowsservercore`

```console
$ docker pull nats@sha256:358028020ee9c6b6ff8494f70ecbfddddf5b29d36bd20ec1b9b37eb351c46081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `nats:2.10.24-windowsservercore` - windows version 10.0.17763.6659; amd64

```console
$ docker pull nats@sha256:c6e3358af2d309d6c2ed2c4321b8d16f0c8c2b817d67b61e77790abeab192882
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2021024024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64938b4574dd9f4d28b0fdba70a6f3483c75359cd4de6fe307eaf6b4c9e6c5d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Tue, 17 Dec 2024 19:28:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 17 Dec 2024 19:28:54 GMT
ENV NATS_DOCKERIZED=1
# Tue, 17 Dec 2024 19:28:55 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 19:28:56 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.24/nats-server-v2.10.24-windows-amd64.zip
# Tue, 17 Dec 2024 19:28:57 GMT
ENV NATS_SERVER_SHASUM=bf94c9a9f1685147fd95f6c62f26d16fb72dc8c8c592e2d8c9115e2491c508c3
# Tue, 17 Dec 2024 19:30:38 GMT
RUN Set-PSDebug -Trace 2
# Tue, 17 Dec 2024 19:31:05 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 17 Dec 2024 19:31:06 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 17 Dec 2024 19:31:06 GMT
EXPOSE 4222 6222 8222
# Tue, 17 Dec 2024 19:31:07 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 17 Dec 2024 19:31:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995e898d38ff13b74b2bf42182403105bd564ca1c8cd3c2bccadac08c8172ca2`  
		Last Modified: Tue, 17 Dec 2024 19:31:15 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7f7d745fbcac3f49a978704fb067848ad5982ff0f7f116bfaceb8e9c68fbc7`  
		Last Modified: Tue, 17 Dec 2024 19:31:15 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0a5927c302d6e5e93a6570c06c06ce9862ef400bd5fea534fea403fd76e9b8`  
		Last Modified: Tue, 17 Dec 2024 19:31:13 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e7b1cd8a1d4aa5917755e9a51eb72256b93ddf6aa3825cbd84213d86f046d3`  
		Last Modified: Tue, 17 Dec 2024 19:31:13 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a76e8a87993daefe8a56da532e9ecac69a46fe935f34deac5f3e2ccff312c7`  
		Last Modified: Tue, 17 Dec 2024 19:31:13 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f37de67167c5db5acc1c6ba5c9f86ac4f699f4c646ecae8bccaaa2a6b86bb0`  
		Last Modified: Tue, 17 Dec 2024 19:31:14 GMT  
		Size: 465.9 KB (465852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d125faf71663c9c259588da9545dcfc1d961e59d92ce5a9486c7d389cb61bc2c`  
		Last Modified: Tue, 17 Dec 2024 19:31:13 GMT  
		Size: 6.4 MB (6375751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f9b5ddb5fe65a52ed1c161189ff40d0273af9d50a8a6777a98abffd5b4f7d0`  
		Last Modified: Tue, 17 Dec 2024 19:31:12 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f6b8c72206232edf4922cfb68939224b12d0d8eb8e2e4c88e5e66875586d0b`  
		Last Modified: Tue, 17 Dec 2024 19:31:12 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6ec3b766844bacc1ba6a7d126a373851ec2b899f045cddd539bc7f1f7ffbd6`  
		Last Modified: Tue, 17 Dec 2024 19:31:12 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d656e63d77c756e50abf1d5d895ac8c06814dd594cc1bf16ea92894907949e`  
		Last Modified: Tue, 17 Dec 2024 19:31:12 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.24-windowsservercore-1809`

```console
$ docker pull nats@sha256:358028020ee9c6b6ff8494f70ecbfddddf5b29d36bd20ec1b9b37eb351c46081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `nats:2.10.24-windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull nats@sha256:c6e3358af2d309d6c2ed2c4321b8d16f0c8c2b817d67b61e77790abeab192882
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2021024024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64938b4574dd9f4d28b0fdba70a6f3483c75359cd4de6fe307eaf6b4c9e6c5d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Tue, 17 Dec 2024 19:28:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 17 Dec 2024 19:28:54 GMT
ENV NATS_DOCKERIZED=1
# Tue, 17 Dec 2024 19:28:55 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 19:28:56 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.24/nats-server-v2.10.24-windows-amd64.zip
# Tue, 17 Dec 2024 19:28:57 GMT
ENV NATS_SERVER_SHASUM=bf94c9a9f1685147fd95f6c62f26d16fb72dc8c8c592e2d8c9115e2491c508c3
# Tue, 17 Dec 2024 19:30:38 GMT
RUN Set-PSDebug -Trace 2
# Tue, 17 Dec 2024 19:31:05 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 17 Dec 2024 19:31:06 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 17 Dec 2024 19:31:06 GMT
EXPOSE 4222 6222 8222
# Tue, 17 Dec 2024 19:31:07 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 17 Dec 2024 19:31:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995e898d38ff13b74b2bf42182403105bd564ca1c8cd3c2bccadac08c8172ca2`  
		Last Modified: Tue, 17 Dec 2024 19:31:15 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7f7d745fbcac3f49a978704fb067848ad5982ff0f7f116bfaceb8e9c68fbc7`  
		Last Modified: Tue, 17 Dec 2024 19:31:15 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0a5927c302d6e5e93a6570c06c06ce9862ef400bd5fea534fea403fd76e9b8`  
		Last Modified: Tue, 17 Dec 2024 19:31:13 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e7b1cd8a1d4aa5917755e9a51eb72256b93ddf6aa3825cbd84213d86f046d3`  
		Last Modified: Tue, 17 Dec 2024 19:31:13 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a76e8a87993daefe8a56da532e9ecac69a46fe935f34deac5f3e2ccff312c7`  
		Last Modified: Tue, 17 Dec 2024 19:31:13 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f37de67167c5db5acc1c6ba5c9f86ac4f699f4c646ecae8bccaaa2a6b86bb0`  
		Last Modified: Tue, 17 Dec 2024 19:31:14 GMT  
		Size: 465.9 KB (465852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d125faf71663c9c259588da9545dcfc1d961e59d92ce5a9486c7d389cb61bc2c`  
		Last Modified: Tue, 17 Dec 2024 19:31:13 GMT  
		Size: 6.4 MB (6375751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f9b5ddb5fe65a52ed1c161189ff40d0273af9d50a8a6777a98abffd5b4f7d0`  
		Last Modified: Tue, 17 Dec 2024 19:31:12 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f6b8c72206232edf4922cfb68939224b12d0d8eb8e2e4c88e5e66875586d0b`  
		Last Modified: Tue, 17 Dec 2024 19:31:12 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6ec3b766844bacc1ba6a7d126a373851ec2b899f045cddd539bc7f1f7ffbd6`  
		Last Modified: Tue, 17 Dec 2024 19:31:12 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d656e63d77c756e50abf1d5d895ac8c06814dd594cc1bf16ea92894907949e`  
		Last Modified: Tue, 17 Dec 2024 19:31:12 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:1ae474d1c029d61d5ad7b170989ab048bc157b8d3ef173d9c8dda10431f4c66a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:e75e15a642407b176cda44b593952a650099bbffced18ac86e1da0adb45a815c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9984940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09fd7f582707a2da49e3e73d42a6397c85ea95b6e58a615a5f0bf1a3780834b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.1-x86_64.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:245043d9199c263f869fc0558f43f7cb98bbc92acdd5def1b4f690adc0ac7807`  
		Last Modified: Mon, 06 Jan 2025 21:44:42 GMT  
		Size: 3.6 MB (3636222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13a0d0824643f0161fd224aceb130343bf44e238a29f9f1cac440eb4b097701c`  
		Last Modified: Tue, 07 Jan 2025 03:20:06 GMT  
		Size: 6.3 MB (6347749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5413da9dd68b96d78c2f9a6ad90c83c10eba4927bfcf99f8812ea179a093c146`  
		Last Modified: Tue, 07 Jan 2025 03:20:06 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdba86b0d45f2bc8262ff57e28b3781caf6b47e078a80f3e89f03f05b9eac8a4`  
		Last Modified: Tue, 07 Jan 2025 03:20:06 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:74e3d1c872d5047663341b23e819482b2bf389190102cfdb5f2b5a10c87a0f08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb0055da207991572098ff5f84511e527c4057fa58cf40e1311b9013d4db18e6`

```dockerfile
```

-	Layers:
	-	`sha256:301c11a8c0e0cb7a10b31ed266709ff88d4cb1d04b4b773cda7d7a7af0a919ee`  
		Last Modified: Tue, 07 Jan 2025 03:20:07 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:56cbfc79edf7b2c7aa940cfd6f7383d3f0acd1d20aef967f001ded5079cb2b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9361190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a44eaada784dc01cb9c5f57575b9f22ece42b1f2885e166714a4ec2a677ee2bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.1-armhf.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:31d4a7f5d4e2c1fd6b13116c69b324d9255a249ba92b63cd7d98924ec5438675`  
		Last Modified: Tue, 07 Jan 2025 02:29:34 GMT  
		Size: 3.4 MB (3361034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3aeae20c738cb0545c05b726c587c76393b9a553968be75b99d583e66a7775b`  
		Last Modified: Tue, 07 Jan 2025 03:58:09 GMT  
		Size: 6.0 MB (5999180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ec491cee3b9736e33232b0eeecad77b992ef16de691db662b0b61774f8b73c`  
		Last Modified: Tue, 07 Jan 2025 03:58:08 GMT  
		Size: 564.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03aa8832feccfdad9eba1b2d0cfeabfbc22bd7ac1eb3047e9e71b63a38bb09c`  
		Last Modified: Tue, 07 Jan 2025 03:58:08 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:cb2eb11b7181517ab509ea8b21a459285feee2175862c053b04ac04c56ca29a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13da7c14ff3fa5a48c56b744564d8ee8a26501609ee8b4a5c1f30b63e89fcb91`

```dockerfile
```

-	Layers:
	-	`sha256:df8f81133a2bf850bec9c382e906dfc869f01f7c98b59587a49715e9aeb29498`  
		Last Modified: Tue, 07 Jan 2025 03:58:08 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:fdfe42e62e2b79b73f65039202fe3229e6cb71c69e82a64080c440b9707cedd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9080587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1588e3d1330f032c6efe96bdb72b0f9179e37f26f272bac3d8f53f11bef3cbff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.1-armv7.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fa398bd1707194d783a6221bb60ba630f074222cdc0f4b6a05d9167d6e9c4a9f`  
		Last Modified: Tue, 07 Jan 2025 02:55:27 GMT  
		Size: 3.1 MB (3093241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f00f9faabc3557dcc5a09506016607206ccc43235c52c7f039f0f569067899f`  
		Last Modified: Tue, 07 Jan 2025 03:43:07 GMT  
		Size: 6.0 MB (5986376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ec44d2ed6879601786756e72d73f99cde8e79fa55e16f1af107519e800da9e`  
		Last Modified: Tue, 07 Jan 2025 03:43:06 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e68cbd6292db04b815b0b4f504cc27d37888065829ba6187ed1b81146b0f8b`  
		Last Modified: Tue, 07 Jan 2025 03:43:06 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:42c8ebef1cfc8b8f2fb88adcab48268298580a6b1c7994bc90ecc0e85eaee6be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb1d3dff94118ce66c8f8e7273533a5489d0907af8d4d1c08d15b86a65ef9aa`

```dockerfile
```

-	Layers:
	-	`sha256:16ef13af5efe22a4816752712e3aa06f4d2e9e998d253a67358a93a82bf88c3b`  
		Last Modified: Tue, 07 Jan 2025 03:43:06 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a3bd4772713e383733977b42d0bdfde71d8bc73298b3043639c042161e7b3ce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9885113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80637e8b5cf4194cba52d82998bac00c029971bb34fc5be960598a7483cd5d67`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:707c94c90c597447ce10a36c9b56355c1cc67d0cf593a592daeb419d99a30d85`  
		Last Modified: Tue, 07 Jan 2025 03:02:50 GMT  
		Size: 4.0 MB (3983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81dca03c14249dbcca7f333b7af01e9e99db8e96d6c9d2f2bde6d66c7e329324`  
		Last Modified: Tue, 07 Jan 2025 04:20:26 GMT  
		Size: 5.9 MB (5901137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9545f2b071c52dcf93362ddf8c114680a82ab925c1a0404a1ced42ca02cf81c`  
		Last Modified: Tue, 07 Jan 2025 04:20:26 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22af105e2b54631c9d3d6f803af860c168d3e5cc35a5fa5be13328311c288cc8`  
		Last Modified: Tue, 07 Jan 2025 04:20:26 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:b33a75f3a131215546c5e5051f64d1da52efc1df0668a9807a8e69112eac7f54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d468c758973e805c31c177ab74b4029804f634f063c47cfb99ff25d3cf499b`

```dockerfile
```

-	Layers:
	-	`sha256:6179800d5433282d408054d0574571874af30c964b865ce8caa292b6df2ade56`  
		Last Modified: Tue, 07 Jan 2025 04:20:26 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:5d7ae4028ab12c2a74b8a7c331e4ccb0eae01a94d682cc65b60b8fd51c43d223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9432907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc3b47e1a998b06b497b8d3d4573199f0385b0f9bfe7543c284b47f05acebb66`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.1-ppc64le.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9207393f0daad55cddbc775f55edde5baecdca9e0441c9c1f627f2394d28b7c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:05 GMT  
		Size: 3.6 MB (3567745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acef6d00c5d9f955c0ada0042b4d702b198dc599a72773715bec6a5deab07ba2`  
		Last Modified: Tue, 07 Jan 2025 03:50:51 GMT  
		Size: 5.9 MB (5864192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce5db60d75e59b4b4f0e79bcd3c707843e4f174e155467ba9c768426b98a398`  
		Last Modified: Tue, 07 Jan 2025 03:50:51 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d120b1f8dd2ce33447645c1b4328c2d88cbb5d570c67bc161cc99b05f5c68e`  
		Last Modified: Tue, 07 Jan 2025 03:50:51 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:c9feafae7ef54aa6e4379a8e78a32c28c988b91724d91bb48524d6e2f396d67f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e39d2f23f56f144fffc66e26c856f03cde7d644a740c82397b8866f918db873d`

```dockerfile
```

-	Layers:
	-	`sha256:f681712c35cd291126837bbcdeb41fc7871fc45035d8dec9395bd27034b3d520`  
		Last Modified: Tue, 07 Jan 2025 03:50:51 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; s390x

```console
$ docker pull nats@sha256:4649a608cb9cdfc49ebb039d6ea36cd89a3ef0c6e2ce1402f3d2c24a9a221225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9653226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b55dcbb50fac7b108734557067c71c07e62274db299fe32ec263b9e11f2cb59`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.1-s390x.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:93a724ed1843277c272a09a7779ca31a802938fe3a88142df42e291e0dc759c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:17 GMT  
		Size: 3.5 MB (3459449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723f4bf7823ff55b05e1545bb39271fc9629e9d17ec83b14c487b1bc1feaf66e`  
		Last Modified: Tue, 07 Jan 2025 03:45:59 GMT  
		Size: 6.2 MB (6192808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8625174e21f292a47f2bb46a59b4d41f57a796cd52926234c718dd0556f08a54`  
		Last Modified: Tue, 07 Jan 2025 03:45:59 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b2c4e11055e3b9000f33288affd900fabde3b220edf8fbff0d50687fa637b06`  
		Last Modified: Tue, 07 Jan 2025 03:45:59 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:d952184708e04933d2b5631eb5fd04bdd74ca4e384122fa926fb8f74b34d0d93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e29dff1272c5b181c168004dd85e6068f54151252615c50a09ef6dff321104a9`

```dockerfile
```

-	Layers:
	-	`sha256:6ff141856e7b853dc1f812064b76dbb06f3dfb468f1dfa89312a9f106434e96f`  
		Last Modified: Tue, 07 Jan 2025 03:45:59 GMT  
		Size: 14.3 KB (14321 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:alpine3.21`

```console
$ docker pull nats@sha256:1ae474d1c029d61d5ad7b170989ab048bc157b8d3ef173d9c8dda10431f4c66a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:alpine3.21` - linux; amd64

```console
$ docker pull nats@sha256:e75e15a642407b176cda44b593952a650099bbffced18ac86e1da0adb45a815c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9984940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09fd7f582707a2da49e3e73d42a6397c85ea95b6e58a615a5f0bf1a3780834b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.1-x86_64.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:245043d9199c263f869fc0558f43f7cb98bbc92acdd5def1b4f690adc0ac7807`  
		Last Modified: Mon, 06 Jan 2025 21:44:42 GMT  
		Size: 3.6 MB (3636222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13a0d0824643f0161fd224aceb130343bf44e238a29f9f1cac440eb4b097701c`  
		Last Modified: Tue, 07 Jan 2025 03:20:06 GMT  
		Size: 6.3 MB (6347749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5413da9dd68b96d78c2f9a6ad90c83c10eba4927bfcf99f8812ea179a093c146`  
		Last Modified: Tue, 07 Jan 2025 03:20:06 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdba86b0d45f2bc8262ff57e28b3781caf6b47e078a80f3e89f03f05b9eac8a4`  
		Last Modified: Tue, 07 Jan 2025 03:20:06 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:74e3d1c872d5047663341b23e819482b2bf389190102cfdb5f2b5a10c87a0f08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb0055da207991572098ff5f84511e527c4057fa58cf40e1311b9013d4db18e6`

```dockerfile
```

-	Layers:
	-	`sha256:301c11a8c0e0cb7a10b31ed266709ff88d4cb1d04b4b773cda7d7a7af0a919ee`  
		Last Modified: Tue, 07 Jan 2025 03:20:07 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:56cbfc79edf7b2c7aa940cfd6f7383d3f0acd1d20aef967f001ded5079cb2b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9361190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a44eaada784dc01cb9c5f57575b9f22ece42b1f2885e166714a4ec2a677ee2bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.1-armhf.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:31d4a7f5d4e2c1fd6b13116c69b324d9255a249ba92b63cd7d98924ec5438675`  
		Last Modified: Tue, 07 Jan 2025 02:29:34 GMT  
		Size: 3.4 MB (3361034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3aeae20c738cb0545c05b726c587c76393b9a553968be75b99d583e66a7775b`  
		Last Modified: Tue, 07 Jan 2025 03:58:09 GMT  
		Size: 6.0 MB (5999180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ec491cee3b9736e33232b0eeecad77b992ef16de691db662b0b61774f8b73c`  
		Last Modified: Tue, 07 Jan 2025 03:58:08 GMT  
		Size: 564.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03aa8832feccfdad9eba1b2d0cfeabfbc22bd7ac1eb3047e9e71b63a38bb09c`  
		Last Modified: Tue, 07 Jan 2025 03:58:08 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:cb2eb11b7181517ab509ea8b21a459285feee2175862c053b04ac04c56ca29a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13da7c14ff3fa5a48c56b744564d8ee8a26501609ee8b4a5c1f30b63e89fcb91`

```dockerfile
```

-	Layers:
	-	`sha256:df8f81133a2bf850bec9c382e906dfc869f01f7c98b59587a49715e9aeb29498`  
		Last Modified: Tue, 07 Jan 2025 03:58:08 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:fdfe42e62e2b79b73f65039202fe3229e6cb71c69e82a64080c440b9707cedd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9080587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1588e3d1330f032c6efe96bdb72b0f9179e37f26f272bac3d8f53f11bef3cbff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.1-armv7.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fa398bd1707194d783a6221bb60ba630f074222cdc0f4b6a05d9167d6e9c4a9f`  
		Last Modified: Tue, 07 Jan 2025 02:55:27 GMT  
		Size: 3.1 MB (3093241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f00f9faabc3557dcc5a09506016607206ccc43235c52c7f039f0f569067899f`  
		Last Modified: Tue, 07 Jan 2025 03:43:07 GMT  
		Size: 6.0 MB (5986376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ec44d2ed6879601786756e72d73f99cde8e79fa55e16f1af107519e800da9e`  
		Last Modified: Tue, 07 Jan 2025 03:43:06 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e68cbd6292db04b815b0b4f504cc27d37888065829ba6187ed1b81146b0f8b`  
		Last Modified: Tue, 07 Jan 2025 03:43:06 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:42c8ebef1cfc8b8f2fb88adcab48268298580a6b1c7994bc90ecc0e85eaee6be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb1d3dff94118ce66c8f8e7273533a5489d0907af8d4d1c08d15b86a65ef9aa`

```dockerfile
```

-	Layers:
	-	`sha256:16ef13af5efe22a4816752712e3aa06f4d2e9e998d253a67358a93a82bf88c3b`  
		Last Modified: Tue, 07 Jan 2025 03:43:06 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a3bd4772713e383733977b42d0bdfde71d8bc73298b3043639c042161e7b3ce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9885113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80637e8b5cf4194cba52d82998bac00c029971bb34fc5be960598a7483cd5d67`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:707c94c90c597447ce10a36c9b56355c1cc67d0cf593a592daeb419d99a30d85`  
		Last Modified: Tue, 07 Jan 2025 03:02:50 GMT  
		Size: 4.0 MB (3983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81dca03c14249dbcca7f333b7af01e9e99db8e96d6c9d2f2bde6d66c7e329324`  
		Last Modified: Tue, 07 Jan 2025 04:20:26 GMT  
		Size: 5.9 MB (5901137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9545f2b071c52dcf93362ddf8c114680a82ab925c1a0404a1ced42ca02cf81c`  
		Last Modified: Tue, 07 Jan 2025 04:20:26 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22af105e2b54631c9d3d6f803af860c168d3e5cc35a5fa5be13328311c288cc8`  
		Last Modified: Tue, 07 Jan 2025 04:20:26 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:b33a75f3a131215546c5e5051f64d1da52efc1df0668a9807a8e69112eac7f54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d468c758973e805c31c177ab74b4029804f634f063c47cfb99ff25d3cf499b`

```dockerfile
```

-	Layers:
	-	`sha256:6179800d5433282d408054d0574571874af30c964b865ce8caa292b6df2ade56`  
		Last Modified: Tue, 07 Jan 2025 04:20:26 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:5d7ae4028ab12c2a74b8a7c331e4ccb0eae01a94d682cc65b60b8fd51c43d223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9432907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc3b47e1a998b06b497b8d3d4573199f0385b0f9bfe7543c284b47f05acebb66`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.1-ppc64le.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9207393f0daad55cddbc775f55edde5baecdca9e0441c9c1f627f2394d28b7c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:05 GMT  
		Size: 3.6 MB (3567745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acef6d00c5d9f955c0ada0042b4d702b198dc599a72773715bec6a5deab07ba2`  
		Last Modified: Tue, 07 Jan 2025 03:50:51 GMT  
		Size: 5.9 MB (5864192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce5db60d75e59b4b4f0e79bcd3c707843e4f174e155467ba9c768426b98a398`  
		Last Modified: Tue, 07 Jan 2025 03:50:51 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d120b1f8dd2ce33447645c1b4328c2d88cbb5d570c67bc161cc99b05f5c68e`  
		Last Modified: Tue, 07 Jan 2025 03:50:51 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:c9feafae7ef54aa6e4379a8e78a32c28c988b91724d91bb48524d6e2f396d67f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e39d2f23f56f144fffc66e26c856f03cde7d644a740c82397b8866f918db873d`

```dockerfile
```

-	Layers:
	-	`sha256:f681712c35cd291126837bbcdeb41fc7871fc45035d8dec9395bd27034b3d520`  
		Last Modified: Tue, 07 Jan 2025 03:50:51 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:4649a608cb9cdfc49ebb039d6ea36cd89a3ef0c6e2ce1402f3d2c24a9a221225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9653226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b55dcbb50fac7b108734557067c71c07e62274db299fe32ec263b9e11f2cb59`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.1-s390x.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:93a724ed1843277c272a09a7779ca31a802938fe3a88142df42e291e0dc759c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:17 GMT  
		Size: 3.5 MB (3459449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723f4bf7823ff55b05e1545bb39271fc9629e9d17ec83b14c487b1bc1feaf66e`  
		Last Modified: Tue, 07 Jan 2025 03:45:59 GMT  
		Size: 6.2 MB (6192808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8625174e21f292a47f2bb46a59b4d41f57a796cd52926234c718dd0556f08a54`  
		Last Modified: Tue, 07 Jan 2025 03:45:59 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b2c4e11055e3b9000f33288affd900fabde3b220edf8fbff0d50687fa637b06`  
		Last Modified: Tue, 07 Jan 2025 03:45:59 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:d952184708e04933d2b5631eb5fd04bdd74ca4e384122fa926fb8f74b34d0d93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e29dff1272c5b181c168004dd85e6068f54151252615c50a09ef6dff321104a9`

```dockerfile
```

-	Layers:
	-	`sha256:6ff141856e7b853dc1f812064b76dbb06f3dfb468f1dfa89312a9f106434e96f`  
		Last Modified: Tue, 07 Jan 2025 03:45:59 GMT  
		Size: 14.3 KB (14321 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:latest`

```console
$ docker pull nats@sha256:bc2b3f3198786445a692d868397d7229502fc445f9966136d76c4d065e473c04
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.17763.6659; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:598ab684e8bafd4f4227ee552ce98bd196abf0cbf6afdc409f74f48886287bb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5905657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24ab2fdd6d375d97b62be28867989f387cc11050dcc31df27d4fa32b6b08e243`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2cb1f9bba9aff495d2f8a23661a6c1c7bc2c839cdc2be180b4b8d9bc9800c45e`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.9 MB (5905148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d543cdf7ef6e19ee24fcb0c663a82a570f5d76342cdbe1f16376e80658f531`  
		Last Modified: Tue, 07 Jan 2025 04:18:12 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:e7a69231651c265e8db70dc79d63ca27d50eff1c7d32be38202da1d315a624f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a5ad75f0ecaf5f3b903c67619e8421121692845fc51e699c386d8afbc9214d`

```dockerfile
```

-	Layers:
	-	`sha256:3b9fcbd5baa342487cc6ee0de074d83be1f60a7d04c5e296fd68ed85e1a4c76c`  
		Last Modified: Tue, 07 Jan 2025 04:18:12 GMT  
		Size: 10.5 KB (10472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:f801151009502a85c381ffc3e3d4da1b39a338bd804445dbab92e447a8d0742d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5dab6565a7ccd5e8b79dd46bc5519aff76b27bfd17665dd3ab08500446ae12c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:81fd6ecec75a6718f55afc7801f7191a8b41d70739a2651f877929f41efcd454`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.6 MB (5553927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4aef5e79acad5215cfeb435fcd7a420447cc550b3045715dcd97efb7cb374f`  
		Last Modified: Tue, 17 Dec 2024 20:07:21 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:aa392b8671143c697cdb326a2e6c742a067761c4db93860f234dc5b35ed0fb11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:976493cfd43ca3f9a8ad5279956a0080949b50282eecf7a444c4fda93c34322f`

```dockerfile
```

-	Layers:
	-	`sha256:8c2857f8ddfd44360797a8c21b94d211d9d2a7db67740cdb79c8c10aa235b398`  
		Last Modified: Tue, 17 Dec 2024 20:07:21 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:982d1d42158b250be7f9650713a8ce7f79bfcba19c04673b21aa2677f187e826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5541946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a6a2dc3f5ef13e36babac38a18c93a6285238679ddf644b3a3f7a5e9e2b29f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:85a1620c1bc6892b5d6c70da117024f4e8fd52994270c35fc7e84782f9682593`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.5 MB (5541438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cdb512b6ca4232a2dd947f49e124f42a6360977706249ce886b49eaba3d3658`  
		Last Modified: Tue, 17 Dec 2024 20:07:18 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:f9eaffb5a7d57be14405ae9a378201ab9a8b8f29afc536e0f8cc6212a74b1a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4afd2190878f0bf2aaadb3cf3fc2a325ccf406cb5223de0922fb20c9f55782d`

```dockerfile
```

-	Layers:
	-	`sha256:163a6014f277c730d1ebece60d800e1889e07231871cc75ab28b5544c87be3b1`  
		Last Modified: Tue, 17 Dec 2024 20:07:18 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:46cc8aa9b94b2de214209442d6cb1e771affdf42d871cfe81596929f23ab15a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5454197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a567c1ed7c844d528fb5acbc5c0388776a9735d231544b5281c56981009f7b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d0b7f1d89d35acbd261abd0ec2bcf54bcc65bb79ebf006850dc5cfae55765a62`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.5 MB (5453688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714d2581a122d6579083f834fb3cf2cea0ad605e1a1ea3cabc5e99db033a0de9`  
		Last Modified: Tue, 17 Dec 2024 23:47:32 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:f41b9f81c4ad1bf1332a199acd507a5e89a4a0d44aa0b141c1d31a41c940b3b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87666fbe34385bd1ec5ac0f209512cd54596dc5cae712d1600dbbb2ea2fcb91e`

```dockerfile
```

-	Layers:
	-	`sha256:c7ee9e2eebe3c624616f634e065612ab6d6e9395b5694f040d1fba9e93e18fec`  
		Last Modified: Tue, 17 Dec 2024 23:47:32 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; ppc64le

```console
$ docker pull nats@sha256:bf4bc17ce581fbc555448128b270a270364f08c1fa916496cdf12b90741ebcbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5418848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61ba372cd7f008492fffa212def1194d605e85849146fc8141f2f60a3935332d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:72b285162443e680327c1bf58de30e30459f3f8193b0769fd1fad6f4f115b124`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.4 MB (5418340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49171e380cf318294924933ba7552fde576651ba45f06690772f99bd0d09c62`  
		Last Modified: Tue, 07 Jan 2025 09:49:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:65d7ddac6a9451045689180537020395f325928967d57be7f680d41e62bfbc7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26558754194d57e26e105533c268c9dd4e5f229090f32bab381f786d5c1ab504`

```dockerfile
```

-	Layers:
	-	`sha256:5db6af784b78d60900035a04e99b70041ea3ee04c0eabcc41b60160cd2933452`  
		Last Modified: Tue, 07 Jan 2025 09:49:22 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; s390x

```console
$ docker pull nats@sha256:a82b5907b071519d7add42e0ff6632ee3ea5ad1152c0f3432ee682f4954e38f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5748559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:064b066d0f376d269a70742585b50ba3cd7c177611f92c629f158e2df7944418`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bd4119cb6f8c6b49f3ec55933200d2283d0f58b8b79bb753e5436770b7c2b320`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.7 MB (5748050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afd816dca497faa2937925ee17de8bdaa1530e524721a18bf0e7838bd7f6c2e`  
		Last Modified: Tue, 17 Dec 2024 20:07:57 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:c28225ad7ee2152f11088957130764b2ca530f01b73f693afc238a553b29d443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f772a80018515b59b3c7005be4f7c9bdc3a6a48167750b803269d3bf711e8f08`

```dockerfile
```

-	Layers:
	-	`sha256:9de3e5757b559fa1c5cba102c651c66e5db5e3b5889139d5508a670b2b9f07d5`  
		Last Modified: Tue, 17 Dec 2024 20:07:57 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - windows version 10.0.17763.6659; amd64

```console
$ docker pull nats@sha256:a3bf98913be025c2083ebd5687c133ab5b00f3a1894a3fe2231a87894b64bed0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161263273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50684e4ed1bf0d28623bfd52d2bfd9a7c4111c83ceaabd37a09cbf397e675281`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 04:54:21 GMT
RUN Apply image 10.0.17763.6659
# Tue, 17 Dec 2024 20:08:15 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 17 Dec 2024 20:08:18 GMT
RUN cmd /S /C #(nop) COPY file:32d2c78f0dd94e383b45881b640cf1b2c9c27decb4a66e09babbe6a0f796087f in C:\nats-server.exe 
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 17 Dec 2024 20:08:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fc1cdf36537340b1875b5d6573a58a268fc20b63dc54a780f9070e51cf9eb9ca`  
		Last Modified: Tue, 10 Dec 2024 21:03:34 GMT  
		Size: 155.2 MB (155231618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f2ef448a775bed9c6f05668d734eb51754170fdfc93c55c99bbaa763bf0d4e`  
		Last Modified: Tue, 17 Dec 2024 20:08:26 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe350f8421c39c736eb0f8180693ff45eedcd35a224bc510bd2626a0996409b`  
		Last Modified: Tue, 17 Dec 2024 20:08:25 GMT  
		Size: 6.0 MB (6025803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd8a7a90698ba96911ac6344eb5f5dd88c4dfebd29047be607133fadef68165`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.7 KB (1671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f84b1a718e07866b0c5d7f7666c682f746339824f50d2010237f8129d983c34`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be4b8e9d23c6bed197e181271e99e2a123100ad014b841f2409aaa51fe58303`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52cb4f7ea4c581f0a9e1eb6519dba6818337a039607974ce3fd7131a13ea51b0`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:c597fb1c0dbee32f6092767e6550bc6f458d011aa48f8467f483161208b853ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:598ab684e8bafd4f4227ee552ce98bd196abf0cbf6afdc409f74f48886287bb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5905657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24ab2fdd6d375d97b62be28867989f387cc11050dcc31df27d4fa32b6b08e243`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2cb1f9bba9aff495d2f8a23661a6c1c7bc2c839cdc2be180b4b8d9bc9800c45e`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.9 MB (5905148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d543cdf7ef6e19ee24fcb0c663a82a570f5d76342cdbe1f16376e80658f531`  
		Last Modified: Tue, 07 Jan 2025 04:18:12 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:e7a69231651c265e8db70dc79d63ca27d50eff1c7d32be38202da1d315a624f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a5ad75f0ecaf5f3b903c67619e8421121692845fc51e699c386d8afbc9214d`

```dockerfile
```

-	Layers:
	-	`sha256:3b9fcbd5baa342487cc6ee0de074d83be1f60a7d04c5e296fd68ed85e1a4c76c`  
		Last Modified: Tue, 07 Jan 2025 04:18:12 GMT  
		Size: 10.5 KB (10472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:f801151009502a85c381ffc3e3d4da1b39a338bd804445dbab92e447a8d0742d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5dab6565a7ccd5e8b79dd46bc5519aff76b27bfd17665dd3ab08500446ae12c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:81fd6ecec75a6718f55afc7801f7191a8b41d70739a2651f877929f41efcd454`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.6 MB (5553927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4aef5e79acad5215cfeb435fcd7a420447cc550b3045715dcd97efb7cb374f`  
		Last Modified: Tue, 17 Dec 2024 20:07:21 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:aa392b8671143c697cdb326a2e6c742a067761c4db93860f234dc5b35ed0fb11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:976493cfd43ca3f9a8ad5279956a0080949b50282eecf7a444c4fda93c34322f`

```dockerfile
```

-	Layers:
	-	`sha256:8c2857f8ddfd44360797a8c21b94d211d9d2a7db67740cdb79c8c10aa235b398`  
		Last Modified: Tue, 17 Dec 2024 20:07:21 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:982d1d42158b250be7f9650713a8ce7f79bfcba19c04673b21aa2677f187e826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5541946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a6a2dc3f5ef13e36babac38a18c93a6285238679ddf644b3a3f7a5e9e2b29f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:85a1620c1bc6892b5d6c70da117024f4e8fd52994270c35fc7e84782f9682593`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.5 MB (5541438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cdb512b6ca4232a2dd947f49e124f42a6360977706249ce886b49eaba3d3658`  
		Last Modified: Tue, 17 Dec 2024 20:07:18 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:f9eaffb5a7d57be14405ae9a378201ab9a8b8f29afc536e0f8cc6212a74b1a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4afd2190878f0bf2aaadb3cf3fc2a325ccf406cb5223de0922fb20c9f55782d`

```dockerfile
```

-	Layers:
	-	`sha256:163a6014f277c730d1ebece60d800e1889e07231871cc75ab28b5544c87be3b1`  
		Last Modified: Tue, 17 Dec 2024 20:07:18 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:46cc8aa9b94b2de214209442d6cb1e771affdf42d871cfe81596929f23ab15a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5454197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a567c1ed7c844d528fb5acbc5c0388776a9735d231544b5281c56981009f7b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d0b7f1d89d35acbd261abd0ec2bcf54bcc65bb79ebf006850dc5cfae55765a62`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.5 MB (5453688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714d2581a122d6579083f834fb3cf2cea0ad605e1a1ea3cabc5e99db033a0de9`  
		Last Modified: Tue, 17 Dec 2024 23:47:32 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:f41b9f81c4ad1bf1332a199acd507a5e89a4a0d44aa0b141c1d31a41c940b3b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87666fbe34385bd1ec5ac0f209512cd54596dc5cae712d1600dbbb2ea2fcb91e`

```dockerfile
```

-	Layers:
	-	`sha256:c7ee9e2eebe3c624616f634e065612ab6d6e9395b5694f040d1fba9e93e18fec`  
		Last Modified: Tue, 17 Dec 2024 23:47:32 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; ppc64le

```console
$ docker pull nats@sha256:bf4bc17ce581fbc555448128b270a270364f08c1fa916496cdf12b90741ebcbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5418848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61ba372cd7f008492fffa212def1194d605e85849146fc8141f2f60a3935332d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:72b285162443e680327c1bf58de30e30459f3f8193b0769fd1fad6f4f115b124`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.4 MB (5418340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49171e380cf318294924933ba7552fde576651ba45f06690772f99bd0d09c62`  
		Last Modified: Tue, 07 Jan 2025 09:49:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:65d7ddac6a9451045689180537020395f325928967d57be7f680d41e62bfbc7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26558754194d57e26e105533c268c9dd4e5f229090f32bab381f786d5c1ab504`

```dockerfile
```

-	Layers:
	-	`sha256:5db6af784b78d60900035a04e99b70041ea3ee04c0eabcc41b60160cd2933452`  
		Last Modified: Tue, 07 Jan 2025 09:49:22 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; s390x

```console
$ docker pull nats@sha256:a82b5907b071519d7add42e0ff6632ee3ea5ad1152c0f3432ee682f4954e38f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5748559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:064b066d0f376d269a70742585b50ba3cd7c177611f92c629f158e2df7944418`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bd4119cb6f8c6b49f3ec55933200d2283d0f58b8b79bb753e5436770b7c2b320`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.7 MB (5748050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afd816dca497faa2937925ee17de8bdaa1530e524721a18bf0e7838bd7f6c2e`  
		Last Modified: Tue, 17 Dec 2024 20:07:57 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:c28225ad7ee2152f11088957130764b2ca530f01b73f693afc238a553b29d443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f772a80018515b59b3c7005be4f7c9bdc3a6a48167750b803269d3bf711e8f08`

```dockerfile
```

-	Layers:
	-	`sha256:9de3e5757b559fa1c5cba102c651c66e5db5e3b5889139d5508a670b2b9f07d5`  
		Last Modified: Tue, 17 Dec 2024 20:07:57 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:nanoserver`

```console
$ docker pull nats@sha256:37e1b8a8d0e258480f2b4e3e528c51625f7c66283ec06ca04228db3a08fa024e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `nats:nanoserver` - windows version 10.0.17763.6659; amd64

```console
$ docker pull nats@sha256:a3bf98913be025c2083ebd5687c133ab5b00f3a1894a3fe2231a87894b64bed0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161263273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50684e4ed1bf0d28623bfd52d2bfd9a7c4111c83ceaabd37a09cbf397e675281`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 04:54:21 GMT
RUN Apply image 10.0.17763.6659
# Tue, 17 Dec 2024 20:08:15 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 17 Dec 2024 20:08:18 GMT
RUN cmd /S /C #(nop) COPY file:32d2c78f0dd94e383b45881b640cf1b2c9c27decb4a66e09babbe6a0f796087f in C:\nats-server.exe 
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 17 Dec 2024 20:08:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fc1cdf36537340b1875b5d6573a58a268fc20b63dc54a780f9070e51cf9eb9ca`  
		Last Modified: Tue, 10 Dec 2024 21:03:34 GMT  
		Size: 155.2 MB (155231618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f2ef448a775bed9c6f05668d734eb51754170fdfc93c55c99bbaa763bf0d4e`  
		Last Modified: Tue, 17 Dec 2024 20:08:26 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe350f8421c39c736eb0f8180693ff45eedcd35a224bc510bd2626a0996409b`  
		Last Modified: Tue, 17 Dec 2024 20:08:25 GMT  
		Size: 6.0 MB (6025803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd8a7a90698ba96911ac6344eb5f5dd88c4dfebd29047be607133fadef68165`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.7 KB (1671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f84b1a718e07866b0c5d7f7666c682f746339824f50d2010237f8129d983c34`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be4b8e9d23c6bed197e181271e99e2a123100ad014b841f2409aaa51fe58303`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52cb4f7ea4c581f0a9e1eb6519dba6818337a039607974ce3fd7131a13ea51b0`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:37e1b8a8d0e258480f2b4e3e528c51625f7c66283ec06ca04228db3a08fa024e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull nats@sha256:a3bf98913be025c2083ebd5687c133ab5b00f3a1894a3fe2231a87894b64bed0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161263273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50684e4ed1bf0d28623bfd52d2bfd9a7c4111c83ceaabd37a09cbf397e675281`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 04:54:21 GMT
RUN Apply image 10.0.17763.6659
# Tue, 17 Dec 2024 20:08:15 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 17 Dec 2024 20:08:18 GMT
RUN cmd /S /C #(nop) COPY file:32d2c78f0dd94e383b45881b640cf1b2c9c27decb4a66e09babbe6a0f796087f in C:\nats-server.exe 
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 17 Dec 2024 20:08:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fc1cdf36537340b1875b5d6573a58a268fc20b63dc54a780f9070e51cf9eb9ca`  
		Last Modified: Tue, 10 Dec 2024 21:03:34 GMT  
		Size: 155.2 MB (155231618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f2ef448a775bed9c6f05668d734eb51754170fdfc93c55c99bbaa763bf0d4e`  
		Last Modified: Tue, 17 Dec 2024 20:08:26 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe350f8421c39c736eb0f8180693ff45eedcd35a224bc510bd2626a0996409b`  
		Last Modified: Tue, 17 Dec 2024 20:08:25 GMT  
		Size: 6.0 MB (6025803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd8a7a90698ba96911ac6344eb5f5dd88c4dfebd29047be607133fadef68165`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.7 KB (1671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f84b1a718e07866b0c5d7f7666c682f746339824f50d2010237f8129d983c34`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be4b8e9d23c6bed197e181271e99e2a123100ad014b841f2409aaa51fe58303`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52cb4f7ea4c581f0a9e1eb6519dba6818337a039607974ce3fd7131a13ea51b0`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:c597fb1c0dbee32f6092767e6550bc6f458d011aa48f8467f483161208b853ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:598ab684e8bafd4f4227ee552ce98bd196abf0cbf6afdc409f74f48886287bb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5905657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24ab2fdd6d375d97b62be28867989f387cc11050dcc31df27d4fa32b6b08e243`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2cb1f9bba9aff495d2f8a23661a6c1c7bc2c839cdc2be180b4b8d9bc9800c45e`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.9 MB (5905148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d543cdf7ef6e19ee24fcb0c663a82a570f5d76342cdbe1f16376e80658f531`  
		Last Modified: Tue, 07 Jan 2025 04:18:12 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:e7a69231651c265e8db70dc79d63ca27d50eff1c7d32be38202da1d315a624f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a5ad75f0ecaf5f3b903c67619e8421121692845fc51e699c386d8afbc9214d`

```dockerfile
```

-	Layers:
	-	`sha256:3b9fcbd5baa342487cc6ee0de074d83be1f60a7d04c5e296fd68ed85e1a4c76c`  
		Last Modified: Tue, 07 Jan 2025 04:18:12 GMT  
		Size: 10.5 KB (10472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:f801151009502a85c381ffc3e3d4da1b39a338bd804445dbab92e447a8d0742d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5dab6565a7ccd5e8b79dd46bc5519aff76b27bfd17665dd3ab08500446ae12c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:81fd6ecec75a6718f55afc7801f7191a8b41d70739a2651f877929f41efcd454`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.6 MB (5553927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4aef5e79acad5215cfeb435fcd7a420447cc550b3045715dcd97efb7cb374f`  
		Last Modified: Tue, 17 Dec 2024 20:07:21 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:aa392b8671143c697cdb326a2e6c742a067761c4db93860f234dc5b35ed0fb11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:976493cfd43ca3f9a8ad5279956a0080949b50282eecf7a444c4fda93c34322f`

```dockerfile
```

-	Layers:
	-	`sha256:8c2857f8ddfd44360797a8c21b94d211d9d2a7db67740cdb79c8c10aa235b398`  
		Last Modified: Tue, 17 Dec 2024 20:07:21 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:982d1d42158b250be7f9650713a8ce7f79bfcba19c04673b21aa2677f187e826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5541946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a6a2dc3f5ef13e36babac38a18c93a6285238679ddf644b3a3f7a5e9e2b29f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:85a1620c1bc6892b5d6c70da117024f4e8fd52994270c35fc7e84782f9682593`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.5 MB (5541438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cdb512b6ca4232a2dd947f49e124f42a6360977706249ce886b49eaba3d3658`  
		Last Modified: Tue, 17 Dec 2024 20:07:18 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:f9eaffb5a7d57be14405ae9a378201ab9a8b8f29afc536e0f8cc6212a74b1a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4afd2190878f0bf2aaadb3cf3fc2a325ccf406cb5223de0922fb20c9f55782d`

```dockerfile
```

-	Layers:
	-	`sha256:163a6014f277c730d1ebece60d800e1889e07231871cc75ab28b5544c87be3b1`  
		Last Modified: Tue, 17 Dec 2024 20:07:18 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:46cc8aa9b94b2de214209442d6cb1e771affdf42d871cfe81596929f23ab15a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5454197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a567c1ed7c844d528fb5acbc5c0388776a9735d231544b5281c56981009f7b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d0b7f1d89d35acbd261abd0ec2bcf54bcc65bb79ebf006850dc5cfae55765a62`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.5 MB (5453688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714d2581a122d6579083f834fb3cf2cea0ad605e1a1ea3cabc5e99db033a0de9`  
		Last Modified: Tue, 17 Dec 2024 23:47:32 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:f41b9f81c4ad1bf1332a199acd507a5e89a4a0d44aa0b141c1d31a41c940b3b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87666fbe34385bd1ec5ac0f209512cd54596dc5cae712d1600dbbb2ea2fcb91e`

```dockerfile
```

-	Layers:
	-	`sha256:c7ee9e2eebe3c624616f634e065612ab6d6e9395b5694f040d1fba9e93e18fec`  
		Last Modified: Tue, 17 Dec 2024 23:47:32 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:bf4bc17ce581fbc555448128b270a270364f08c1fa916496cdf12b90741ebcbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5418848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61ba372cd7f008492fffa212def1194d605e85849146fc8141f2f60a3935332d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:72b285162443e680327c1bf58de30e30459f3f8193b0769fd1fad6f4f115b124`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.4 MB (5418340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49171e380cf318294924933ba7552fde576651ba45f06690772f99bd0d09c62`  
		Last Modified: Tue, 07 Jan 2025 09:49:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:65d7ddac6a9451045689180537020395f325928967d57be7f680d41e62bfbc7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26558754194d57e26e105533c268c9dd4e5f229090f32bab381f786d5c1ab504`

```dockerfile
```

-	Layers:
	-	`sha256:5db6af784b78d60900035a04e99b70041ea3ee04c0eabcc41b60160cd2933452`  
		Last Modified: Tue, 07 Jan 2025 09:49:22 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; s390x

```console
$ docker pull nats@sha256:a82b5907b071519d7add42e0ff6632ee3ea5ad1152c0f3432ee682f4954e38f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5748559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:064b066d0f376d269a70742585b50ba3cd7c177611f92c629f158e2df7944418`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bd4119cb6f8c6b49f3ec55933200d2283d0f58b8b79bb753e5436770b7c2b320`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.7 MB (5748050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afd816dca497faa2937925ee17de8bdaa1530e524721a18bf0e7838bd7f6c2e`  
		Last Modified: Tue, 17 Dec 2024 20:07:57 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:c28225ad7ee2152f11088957130764b2ca530f01b73f693afc238a553b29d443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f772a80018515b59b3c7005be4f7c9bdc3a6a48167750b803269d3bf711e8f08`

```dockerfile
```

-	Layers:
	-	`sha256:9de3e5757b559fa1c5cba102c651c66e5db5e3b5889139d5508a670b2b9f07d5`  
		Last Modified: Tue, 17 Dec 2024 20:07:57 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:358028020ee9c6b6ff8494f70ecbfddddf5b29d36bd20ec1b9b37eb351c46081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `nats:windowsservercore` - windows version 10.0.17763.6659; amd64

```console
$ docker pull nats@sha256:c6e3358af2d309d6c2ed2c4321b8d16f0c8c2b817d67b61e77790abeab192882
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2021024024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64938b4574dd9f4d28b0fdba70a6f3483c75359cd4de6fe307eaf6b4c9e6c5d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Tue, 17 Dec 2024 19:28:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 17 Dec 2024 19:28:54 GMT
ENV NATS_DOCKERIZED=1
# Tue, 17 Dec 2024 19:28:55 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 19:28:56 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.24/nats-server-v2.10.24-windows-amd64.zip
# Tue, 17 Dec 2024 19:28:57 GMT
ENV NATS_SERVER_SHASUM=bf94c9a9f1685147fd95f6c62f26d16fb72dc8c8c592e2d8c9115e2491c508c3
# Tue, 17 Dec 2024 19:30:38 GMT
RUN Set-PSDebug -Trace 2
# Tue, 17 Dec 2024 19:31:05 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 17 Dec 2024 19:31:06 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 17 Dec 2024 19:31:06 GMT
EXPOSE 4222 6222 8222
# Tue, 17 Dec 2024 19:31:07 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 17 Dec 2024 19:31:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995e898d38ff13b74b2bf42182403105bd564ca1c8cd3c2bccadac08c8172ca2`  
		Last Modified: Tue, 17 Dec 2024 19:31:15 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7f7d745fbcac3f49a978704fb067848ad5982ff0f7f116bfaceb8e9c68fbc7`  
		Last Modified: Tue, 17 Dec 2024 19:31:15 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0a5927c302d6e5e93a6570c06c06ce9862ef400bd5fea534fea403fd76e9b8`  
		Last Modified: Tue, 17 Dec 2024 19:31:13 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e7b1cd8a1d4aa5917755e9a51eb72256b93ddf6aa3825cbd84213d86f046d3`  
		Last Modified: Tue, 17 Dec 2024 19:31:13 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a76e8a87993daefe8a56da532e9ecac69a46fe935f34deac5f3e2ccff312c7`  
		Last Modified: Tue, 17 Dec 2024 19:31:13 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f37de67167c5db5acc1c6ba5c9f86ac4f699f4c646ecae8bccaaa2a6b86bb0`  
		Last Modified: Tue, 17 Dec 2024 19:31:14 GMT  
		Size: 465.9 KB (465852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d125faf71663c9c259588da9545dcfc1d961e59d92ce5a9486c7d389cb61bc2c`  
		Last Modified: Tue, 17 Dec 2024 19:31:13 GMT  
		Size: 6.4 MB (6375751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f9b5ddb5fe65a52ed1c161189ff40d0273af9d50a8a6777a98abffd5b4f7d0`  
		Last Modified: Tue, 17 Dec 2024 19:31:12 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f6b8c72206232edf4922cfb68939224b12d0d8eb8e2e4c88e5e66875586d0b`  
		Last Modified: Tue, 17 Dec 2024 19:31:12 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6ec3b766844bacc1ba6a7d126a373851ec2b899f045cddd539bc7f1f7ffbd6`  
		Last Modified: Tue, 17 Dec 2024 19:31:12 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d656e63d77c756e50abf1d5d895ac8c06814dd594cc1bf16ea92894907949e`  
		Last Modified: Tue, 17 Dec 2024 19:31:12 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:358028020ee9c6b6ff8494f70ecbfddddf5b29d36bd20ec1b9b37eb351c46081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull nats@sha256:c6e3358af2d309d6c2ed2c4321b8d16f0c8c2b817d67b61e77790abeab192882
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2021024024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64938b4574dd9f4d28b0fdba70a6f3483c75359cd4de6fe307eaf6b4c9e6c5d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Tue, 17 Dec 2024 19:28:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 17 Dec 2024 19:28:54 GMT
ENV NATS_DOCKERIZED=1
# Tue, 17 Dec 2024 19:28:55 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 19:28:56 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.24/nats-server-v2.10.24-windows-amd64.zip
# Tue, 17 Dec 2024 19:28:57 GMT
ENV NATS_SERVER_SHASUM=bf94c9a9f1685147fd95f6c62f26d16fb72dc8c8c592e2d8c9115e2491c508c3
# Tue, 17 Dec 2024 19:30:38 GMT
RUN Set-PSDebug -Trace 2
# Tue, 17 Dec 2024 19:31:05 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 17 Dec 2024 19:31:06 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 17 Dec 2024 19:31:06 GMT
EXPOSE 4222 6222 8222
# Tue, 17 Dec 2024 19:31:07 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 17 Dec 2024 19:31:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995e898d38ff13b74b2bf42182403105bd564ca1c8cd3c2bccadac08c8172ca2`  
		Last Modified: Tue, 17 Dec 2024 19:31:15 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7f7d745fbcac3f49a978704fb067848ad5982ff0f7f116bfaceb8e9c68fbc7`  
		Last Modified: Tue, 17 Dec 2024 19:31:15 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0a5927c302d6e5e93a6570c06c06ce9862ef400bd5fea534fea403fd76e9b8`  
		Last Modified: Tue, 17 Dec 2024 19:31:13 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e7b1cd8a1d4aa5917755e9a51eb72256b93ddf6aa3825cbd84213d86f046d3`  
		Last Modified: Tue, 17 Dec 2024 19:31:13 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a76e8a87993daefe8a56da532e9ecac69a46fe935f34deac5f3e2ccff312c7`  
		Last Modified: Tue, 17 Dec 2024 19:31:13 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f37de67167c5db5acc1c6ba5c9f86ac4f699f4c646ecae8bccaaa2a6b86bb0`  
		Last Modified: Tue, 17 Dec 2024 19:31:14 GMT  
		Size: 465.9 KB (465852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d125faf71663c9c259588da9545dcfc1d961e59d92ce5a9486c7d389cb61bc2c`  
		Last Modified: Tue, 17 Dec 2024 19:31:13 GMT  
		Size: 6.4 MB (6375751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f9b5ddb5fe65a52ed1c161189ff40d0273af9d50a8a6777a98abffd5b4f7d0`  
		Last Modified: Tue, 17 Dec 2024 19:31:12 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f6b8c72206232edf4922cfb68939224b12d0d8eb8e2e4c88e5e66875586d0b`  
		Last Modified: Tue, 17 Dec 2024 19:31:12 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6ec3b766844bacc1ba6a7d126a373851ec2b899f045cddd539bc7f1f7ffbd6`  
		Last Modified: Tue, 17 Dec 2024 19:31:12 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d656e63d77c756e50abf1d5d895ac8c06814dd594cc1bf16ea92894907949e`  
		Last Modified: Tue, 17 Dec 2024 19:31:12 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
