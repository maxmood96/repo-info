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
$ docker pull nats@sha256:d4c302ac4a0d84afff801c413f7f32e9e76505030d020b988605a3e839cbcd95
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
$ docker pull nats@sha256:67d3b85ece6c782cf7ead3ecb3a1ac84ea0f1a90692e49699e78cbded1b303f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5905656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30790e9a65a19f582b2ef7ef953584341edfe5d6fa4e0ca626c151bd29d42300`
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
		Size: 5.9 MB (5905148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8de2329765d2e9e6ad2eef24244fb693d2372ce8561eee2d04a4b15613d4957`  
		Last Modified: Tue, 17 Dec 2024 20:07:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:bf98881f063cf871ca1790de74f2e754f9d790b3db90451f6b5da630335ca9fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b933f94df98aa627cb8bf50b2acae5ed54c95244c49afe60cd9b9504d44c4dc8`

```dockerfile
```

-	Layers:
	-	`sha256:021e7dd96b286525c844698e284fea042a82a034acb1e22fe017dd14f20618a5`  
		Last Modified: Tue, 17 Dec 2024 20:07:46 GMT  
		Size: 10.5 KB (10473 bytes)  
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
$ docker pull nats@sha256:25129eb990a4dd587a984e2e2f97ef3492dc391a45119430a8a33cee51dfa7b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5418850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cf4789450fb70da1d11cc8480fe7fc5895888d5dec9b2f39fc4363a18f5e15e`
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
	-	`sha256:2154049e56fd256d2148c4e2e139e5269047c2bb399664b65fce45bbe9852ba6`  
		Last Modified: Tue, 17 Dec 2024 20:07:27 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:01db48579033a378b0e612214b5ca3906a4b332620348ae699697ca38929b3a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76ff46f64e472e71663b6e392cfa2b372b0a27346ae2de8ea608dd2f8e307c31`

```dockerfile
```

-	Layers:
	-	`sha256:74364e5c7720e83ad343b975d9a65bb9ca7f9689948c422c502889ae59651691`  
		Last Modified: Tue, 17 Dec 2024 20:07:27 GMT  
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
$ docker pull nats@sha256:ab1de7a4552e1aa8676fad12ef36415434dcb0f5e1a8f4bd98c1c0b0e23c3108
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
$ docker pull nats@sha256:29cae9fbb27a68c8d042585d900cfe6c6a0687be3fc48e3749907266646626f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10017369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:575ec7872076c7f2ef48a2565b99ac2557abe519a55646c520a6280dda578672`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ee010a6f8d65980fb2a10e8ed490ac5deeb2c57778398caaff2dd317814317`  
		Last Modified: Tue, 17 Dec 2024 19:28:31 GMT  
		Size: 6.4 MB (6371955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e4e90f8624a081c4f8b6390a205113fb3d4efb52df8b8c4c109f3cbb45e0d7`  
		Last Modified: Tue, 17 Dec 2024 19:28:31 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17488456929723e351ddeda9e989781d4d3524c497aac4a9f4986b0a3bab4945`  
		Last Modified: Tue, 17 Dec 2024 19:28:31 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:cfdf92514ba877de3aba717f98d14ddce733bbffb44c334f902dea9147d674fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1c24142e5eed2c70f10105cdb7898204d5e69436be032d28f67396ed116411e`

```dockerfile
```

-	Layers:
	-	`sha256:e27f4eb3a71bf3ac9a8a6b932556310d82674abcc3248ab6d039babb897b959a`  
		Last Modified: Tue, 17 Dec 2024 19:28:31 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:2d66dc5023cd20e375636ada663a151dc2cf1f1b81366b1be5734dfef827d758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9386302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff9ef91ef8059e02d14a92ff39f20c50ea1a73599f50d8896f1f6df2d1381e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af40215e42d92bd72970c881af08ff0be57978182c0ffc369a75fa63356a3ca8`  
		Last Modified: Tue, 17 Dec 2024 19:29:36 GMT  
		Size: 6.0 MB (6018149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a327f5c4e15af30fe773e5bccc7b9078fd582fa78f7b5fd0d7b2506ec3b4086`  
		Last Modified: Tue, 17 Dec 2024 19:29:35 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8cb23494fbc6a634aa201b70ba71a79f6de1cace9996ea9b672757cf7bca461`  
		Last Modified: Tue, 17 Dec 2024 19:29:35 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:8b64eedc6a198a946e7e91844bdd9f74180c28ccc096147695e88e4e6cf87ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ad27d08cd2faace9930eb98b50cc3e27beddd7c101b0d33c4e03535c60ad2a`

```dockerfile
```

-	Layers:
	-	`sha256:1116a69deb5d903c668d4d739424c27736d4b250ac54f43eb4429c6a19165b7e`  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:9e84106ad88ced73c824cadca62f7e96f3015b20deba910b2e0b55189cc6f173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9107614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69dffc7badcd9eba6823886d65acbb0cfa112f8883783d134dc809e90b98f145`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc51158f73d5719731f6de6d6d24db0e1d4124a5ecd84bab5548388db0eded5a`  
		Last Modified: Tue, 17 Dec 2024 19:29:01 GMT  
		Size: 6.0 MB (6006607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c2203fb8a3575ff778e4d6965d233a19dd24a5bc90771ecca824833e155b06`  
		Last Modified: Tue, 17 Dec 2024 19:29:00 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacb2912b87b4350617243e5835a14b89a4006eb352e2e093b0b93284d61e070`  
		Last Modified: Tue, 17 Dec 2024 19:29:00 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:130347efdbef62b178c834dc5fda8f86a80bc17ee5ed4761825f0d10763932a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25422fc7bc14c1b14b45b22f895a7d64d49eb334e7564262dc1c10e8eca6abf9`

```dockerfile
```

-	Layers:
	-	`sha256:eb58607b3135d344e5e98c1c7130894a0412f1c8d219ba16ccfd1b8aaf8946cf`  
		Last Modified: Tue, 17 Dec 2024 19:29:00 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:91b0e0ed22e13b4b240286a274219ad0b7bef2ab2e5b9cfd4152e5c9c4ad246e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9912392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b9a70b84b2c7628f856d55590dc824bba274042faf6521e6dcecebf44b480f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d311607882428389c8bbb10058ff9f4a07c6714b605f6bd92afa58faf53ccf1`  
		Last Modified: Tue, 17 Dec 2024 19:29:19 GMT  
		Size: 5.9 MB (5918236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:120d4d49d4ce04dd2b71e71ea3c19191133df462671d15362ec224b0c7a6b329`  
		Last Modified: Tue, 17 Dec 2024 19:29:19 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2348ec882817d42d419fca6d6073f5980a4808bea9d36c67cc612d20f656a0c`  
		Last Modified: Tue, 17 Dec 2024 19:29:19 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:2bcdf7d278748efd5f3c41ad5a847840ecabae85a7f38d8bd2eab34f5d925562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51691faecee58ef8255c969e6e92d7f2119288caa70eb618072608de605727bf`

```dockerfile
```

-	Layers:
	-	`sha256:4ecc6db36ffe92c81d7ea0b122f98496f5b6cc7de311e1f92f29189a5e94477f`  
		Last Modified: Tue, 17 Dec 2024 19:29:19 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:3449804a92d7c624c6e5bbc48d29d3c785046de22627a6c4f25962e2f45affee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9464345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:526d9d5508e133079e9f97028d93c63cb13fd416f25a11fad5808f052ab50812`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-ppc64le.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:a12ff663c50b78339bd273940ba035e29d8220954846a4c35a5f79080b37a3d3`  
		Last Modified: Thu, 05 Dec 2024 22:18:21 GMT  
		Size: 3.6 MB (3577108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:672eaefb89f5c4c03dc1dfd0e81f2f3ad81e138d028b4087f87cd3ee9958423d`  
		Last Modified: Tue, 17 Dec 2024 19:28:25 GMT  
		Size: 5.9 MB (5886266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f573fb4c0caa43a456c5b6e69b41c587ceb460ed049cbbe6b7689f71878eb94b`  
		Last Modified: Tue, 17 Dec 2024 19:28:25 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6435cc906fd110b2082eb0900e048df12cb9ea784fd2c023d2802fb66bac5a46`  
		Last Modified: Tue, 17 Dec 2024 19:28:25 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:160f40bbb801fb82f584f14f06735d924e6e69fd6c2fc93acdeacf87846b7cfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159b7defb72e6a0f49e1e548aa2c7df4ee6b842169a267dd9652a7c0f0d338e0`

```dockerfile
```

-	Layers:
	-	`sha256:983eda21d01dd67d3a7bdb35b440c949942f2f1161e0e3a7ee0b98439732a7a6`  
		Last Modified: Tue, 17 Dec 2024 19:28:25 GMT  
		Size: 14.4 KB (14389 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; s390x

```console
$ docker pull nats@sha256:231606d59bf67bf0225b8ff9322391ff528761f9e0417de1607425d5afd4adae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9686596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ab6034672329d984598a6d355339e336c65909875e48379c20c3a8492d5243e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1426b7374b29c0dcb926cdf54914b6a90fcca6f795e94ecee6d05578db18dea`  
		Last Modified: Tue, 17 Dec 2024 19:29:54 GMT  
		Size: 6.2 MB (6216106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a8d5d73de329406149614539003981ece64c24f00a8063d0218ff3b79b4fdd`  
		Last Modified: Tue, 17 Dec 2024 19:29:54 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b700a203382b44c168db5158adc0136d31b657f61a768de50ce397725977f302`  
		Last Modified: Tue, 17 Dec 2024 19:29:54 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:9cb0f384d223b0fb893a8e6883d30cdc52d031457d2466c639299a197a71b02d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb032d67922303b6505eaeb4c3a2e1e93ce05ce4ac7358439ea0f5eda3f19cb6`

```dockerfile
```

-	Layers:
	-	`sha256:8dfd4b0613d89e1631f9a0b566c194348623859b7aab6010157dfa1a5ef47147`  
		Last Modified: Tue, 17 Dec 2024 19:29:54 GMT  
		Size: 14.3 KB (14321 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-alpine3.21`

```console
$ docker pull nats@sha256:ab1de7a4552e1aa8676fad12ef36415434dcb0f5e1a8f4bd98c1c0b0e23c3108
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
$ docker pull nats@sha256:29cae9fbb27a68c8d042585d900cfe6c6a0687be3fc48e3749907266646626f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10017369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:575ec7872076c7f2ef48a2565b99ac2557abe519a55646c520a6280dda578672`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ee010a6f8d65980fb2a10e8ed490ac5deeb2c57778398caaff2dd317814317`  
		Last Modified: Tue, 17 Dec 2024 19:28:31 GMT  
		Size: 6.4 MB (6371955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e4e90f8624a081c4f8b6390a205113fb3d4efb52df8b8c4c109f3cbb45e0d7`  
		Last Modified: Tue, 17 Dec 2024 19:28:31 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17488456929723e351ddeda9e989781d4d3524c497aac4a9f4986b0a3bab4945`  
		Last Modified: Tue, 17 Dec 2024 19:28:31 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:cfdf92514ba877de3aba717f98d14ddce733bbffb44c334f902dea9147d674fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1c24142e5eed2c70f10105cdb7898204d5e69436be032d28f67396ed116411e`

```dockerfile
```

-	Layers:
	-	`sha256:e27f4eb3a71bf3ac9a8a6b932556310d82674abcc3248ab6d039babb897b959a`  
		Last Modified: Tue, 17 Dec 2024 19:28:31 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:2d66dc5023cd20e375636ada663a151dc2cf1f1b81366b1be5734dfef827d758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9386302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff9ef91ef8059e02d14a92ff39f20c50ea1a73599f50d8896f1f6df2d1381e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af40215e42d92bd72970c881af08ff0be57978182c0ffc369a75fa63356a3ca8`  
		Last Modified: Tue, 17 Dec 2024 19:29:36 GMT  
		Size: 6.0 MB (6018149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a327f5c4e15af30fe773e5bccc7b9078fd582fa78f7b5fd0d7b2506ec3b4086`  
		Last Modified: Tue, 17 Dec 2024 19:29:35 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8cb23494fbc6a634aa201b70ba71a79f6de1cace9996ea9b672757cf7bca461`  
		Last Modified: Tue, 17 Dec 2024 19:29:35 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:8b64eedc6a198a946e7e91844bdd9f74180c28ccc096147695e88e4e6cf87ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ad27d08cd2faace9930eb98b50cc3e27beddd7c101b0d33c4e03535c60ad2a`

```dockerfile
```

-	Layers:
	-	`sha256:1116a69deb5d903c668d4d739424c27736d4b250ac54f43eb4429c6a19165b7e`  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:9e84106ad88ced73c824cadca62f7e96f3015b20deba910b2e0b55189cc6f173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9107614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69dffc7badcd9eba6823886d65acbb0cfa112f8883783d134dc809e90b98f145`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc51158f73d5719731f6de6d6d24db0e1d4124a5ecd84bab5548388db0eded5a`  
		Last Modified: Tue, 17 Dec 2024 19:29:01 GMT  
		Size: 6.0 MB (6006607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c2203fb8a3575ff778e4d6965d233a19dd24a5bc90771ecca824833e155b06`  
		Last Modified: Tue, 17 Dec 2024 19:29:00 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacb2912b87b4350617243e5835a14b89a4006eb352e2e093b0b93284d61e070`  
		Last Modified: Tue, 17 Dec 2024 19:29:00 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:130347efdbef62b178c834dc5fda8f86a80bc17ee5ed4761825f0d10763932a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25422fc7bc14c1b14b45b22f895a7d64d49eb334e7564262dc1c10e8eca6abf9`

```dockerfile
```

-	Layers:
	-	`sha256:eb58607b3135d344e5e98c1c7130894a0412f1c8d219ba16ccfd1b8aaf8946cf`  
		Last Modified: Tue, 17 Dec 2024 19:29:00 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:91b0e0ed22e13b4b240286a274219ad0b7bef2ab2e5b9cfd4152e5c9c4ad246e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9912392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b9a70b84b2c7628f856d55590dc824bba274042faf6521e6dcecebf44b480f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d311607882428389c8bbb10058ff9f4a07c6714b605f6bd92afa58faf53ccf1`  
		Last Modified: Tue, 17 Dec 2024 19:29:19 GMT  
		Size: 5.9 MB (5918236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:120d4d49d4ce04dd2b71e71ea3c19191133df462671d15362ec224b0c7a6b329`  
		Last Modified: Tue, 17 Dec 2024 19:29:19 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2348ec882817d42d419fca6d6073f5980a4808bea9d36c67cc612d20f656a0c`  
		Last Modified: Tue, 17 Dec 2024 19:29:19 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:2bcdf7d278748efd5f3c41ad5a847840ecabae85a7f38d8bd2eab34f5d925562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51691faecee58ef8255c969e6e92d7f2119288caa70eb618072608de605727bf`

```dockerfile
```

-	Layers:
	-	`sha256:4ecc6db36ffe92c81d7ea0b122f98496f5b6cc7de311e1f92f29189a5e94477f`  
		Last Modified: Tue, 17 Dec 2024 19:29:19 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:3449804a92d7c624c6e5bbc48d29d3c785046de22627a6c4f25962e2f45affee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9464345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:526d9d5508e133079e9f97028d93c63cb13fd416f25a11fad5808f052ab50812`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-ppc64le.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:a12ff663c50b78339bd273940ba035e29d8220954846a4c35a5f79080b37a3d3`  
		Last Modified: Thu, 05 Dec 2024 22:18:21 GMT  
		Size: 3.6 MB (3577108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:672eaefb89f5c4c03dc1dfd0e81f2f3ad81e138d028b4087f87cd3ee9958423d`  
		Last Modified: Tue, 17 Dec 2024 19:28:25 GMT  
		Size: 5.9 MB (5886266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f573fb4c0caa43a456c5b6e69b41c587ceb460ed049cbbe6b7689f71878eb94b`  
		Last Modified: Tue, 17 Dec 2024 19:28:25 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6435cc906fd110b2082eb0900e048df12cb9ea784fd2c023d2802fb66bac5a46`  
		Last Modified: Tue, 17 Dec 2024 19:28:25 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:160f40bbb801fb82f584f14f06735d924e6e69fd6c2fc93acdeacf87846b7cfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159b7defb72e6a0f49e1e548aa2c7df4ee6b842169a267dd9652a7c0f0d338e0`

```dockerfile
```

-	Layers:
	-	`sha256:983eda21d01dd67d3a7bdb35b440c949942f2f1161e0e3a7ee0b98439732a7a6`  
		Last Modified: Tue, 17 Dec 2024 19:28:25 GMT  
		Size: 14.4 KB (14389 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:231606d59bf67bf0225b8ff9322391ff528761f9e0417de1607425d5afd4adae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9686596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ab6034672329d984598a6d355339e336c65909875e48379c20c3a8492d5243e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1426b7374b29c0dcb926cdf54914b6a90fcca6f795e94ecee6d05578db18dea`  
		Last Modified: Tue, 17 Dec 2024 19:29:54 GMT  
		Size: 6.2 MB (6216106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a8d5d73de329406149614539003981ece64c24f00a8063d0218ff3b79b4fdd`  
		Last Modified: Tue, 17 Dec 2024 19:29:54 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b700a203382b44c168db5158adc0136d31b657f61a768de50ce397725977f302`  
		Last Modified: Tue, 17 Dec 2024 19:29:54 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:9cb0f384d223b0fb893a8e6883d30cdc52d031457d2466c639299a197a71b02d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb032d67922303b6505eaeb4c3a2e1e93ce05ce4ac7358439ea0f5eda3f19cb6`

```dockerfile
```

-	Layers:
	-	`sha256:8dfd4b0613d89e1631f9a0b566c194348623859b7aab6010157dfa1a5ef47147`  
		Last Modified: Tue, 17 Dec 2024 19:29:54 GMT  
		Size: 14.3 KB (14321 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-linux`

```console
$ docker pull nats@sha256:d5cf5fddd6246b37ee3acb3b67903298c21827c1862cd95d0d9f282794c82190
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
$ docker pull nats@sha256:67d3b85ece6c782cf7ead3ecb3a1ac84ea0f1a90692e49699e78cbded1b303f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5905656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30790e9a65a19f582b2ef7ef953584341edfe5d6fa4e0ca626c151bd29d42300`
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
		Size: 5.9 MB (5905148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8de2329765d2e9e6ad2eef24244fb693d2372ce8561eee2d04a4b15613d4957`  
		Last Modified: Tue, 17 Dec 2024 20:07:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:bf98881f063cf871ca1790de74f2e754f9d790b3db90451f6b5da630335ca9fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b933f94df98aa627cb8bf50b2acae5ed54c95244c49afe60cd9b9504d44c4dc8`

```dockerfile
```

-	Layers:
	-	`sha256:021e7dd96b286525c844698e284fea042a82a034acb1e22fe017dd14f20618a5`  
		Last Modified: Tue, 17 Dec 2024 20:07:46 GMT  
		Size: 10.5 KB (10473 bytes)  
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
$ docker pull nats@sha256:25129eb990a4dd587a984e2e2f97ef3492dc391a45119430a8a33cee51dfa7b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5418850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cf4789450fb70da1d11cc8480fe7fc5895888d5dec9b2f39fc4363a18f5e15e`
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
	-	`sha256:2154049e56fd256d2148c4e2e139e5269047c2bb399664b65fce45bbe9852ba6`  
		Last Modified: Tue, 17 Dec 2024 20:07:27 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:01db48579033a378b0e612214b5ca3906a4b332620348ae699697ca38929b3a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76ff46f64e472e71663b6e392cfa2b372b0a27346ae2de8ea608dd2f8e307c31`

```dockerfile
```

-	Layers:
	-	`sha256:74364e5c7720e83ad343b975d9a65bb9ca7f9689948c422c502889ae59651691`  
		Last Modified: Tue, 17 Dec 2024 20:07:27 GMT  
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
$ docker pull nats@sha256:d5cf5fddd6246b37ee3acb3b67903298c21827c1862cd95d0d9f282794c82190
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
$ docker pull nats@sha256:67d3b85ece6c782cf7ead3ecb3a1ac84ea0f1a90692e49699e78cbded1b303f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5905656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30790e9a65a19f582b2ef7ef953584341edfe5d6fa4e0ca626c151bd29d42300`
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
		Size: 5.9 MB (5905148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8de2329765d2e9e6ad2eef24244fb693d2372ce8561eee2d04a4b15613d4957`  
		Last Modified: Tue, 17 Dec 2024 20:07:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:bf98881f063cf871ca1790de74f2e754f9d790b3db90451f6b5da630335ca9fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b933f94df98aa627cb8bf50b2acae5ed54c95244c49afe60cd9b9504d44c4dc8`

```dockerfile
```

-	Layers:
	-	`sha256:021e7dd96b286525c844698e284fea042a82a034acb1e22fe017dd14f20618a5`  
		Last Modified: Tue, 17 Dec 2024 20:07:46 GMT  
		Size: 10.5 KB (10473 bytes)  
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
$ docker pull nats@sha256:25129eb990a4dd587a984e2e2f97ef3492dc391a45119430a8a33cee51dfa7b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5418850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cf4789450fb70da1d11cc8480fe7fc5895888d5dec9b2f39fc4363a18f5e15e`
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
	-	`sha256:2154049e56fd256d2148c4e2e139e5269047c2bb399664b65fce45bbe9852ba6`  
		Last Modified: Tue, 17 Dec 2024 20:07:27 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:01db48579033a378b0e612214b5ca3906a4b332620348ae699697ca38929b3a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76ff46f64e472e71663b6e392cfa2b372b0a27346ae2de8ea608dd2f8e307c31`

```dockerfile
```

-	Layers:
	-	`sha256:74364e5c7720e83ad343b975d9a65bb9ca7f9689948c422c502889ae59651691`  
		Last Modified: Tue, 17 Dec 2024 20:07:27 GMT  
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
$ docker pull nats@sha256:d4c302ac4a0d84afff801c413f7f32e9e76505030d020b988605a3e839cbcd95
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
$ docker pull nats@sha256:67d3b85ece6c782cf7ead3ecb3a1ac84ea0f1a90692e49699e78cbded1b303f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5905656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30790e9a65a19f582b2ef7ef953584341edfe5d6fa4e0ca626c151bd29d42300`
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
		Size: 5.9 MB (5905148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8de2329765d2e9e6ad2eef24244fb693d2372ce8561eee2d04a4b15613d4957`  
		Last Modified: Tue, 17 Dec 2024 20:07:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:bf98881f063cf871ca1790de74f2e754f9d790b3db90451f6b5da630335ca9fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b933f94df98aa627cb8bf50b2acae5ed54c95244c49afe60cd9b9504d44c4dc8`

```dockerfile
```

-	Layers:
	-	`sha256:021e7dd96b286525c844698e284fea042a82a034acb1e22fe017dd14f20618a5`  
		Last Modified: Tue, 17 Dec 2024 20:07:46 GMT  
		Size: 10.5 KB (10473 bytes)  
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
$ docker pull nats@sha256:25129eb990a4dd587a984e2e2f97ef3492dc391a45119430a8a33cee51dfa7b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5418850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cf4789450fb70da1d11cc8480fe7fc5895888d5dec9b2f39fc4363a18f5e15e`
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
	-	`sha256:2154049e56fd256d2148c4e2e139e5269047c2bb399664b65fce45bbe9852ba6`  
		Last Modified: Tue, 17 Dec 2024 20:07:27 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:01db48579033a378b0e612214b5ca3906a4b332620348ae699697ca38929b3a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76ff46f64e472e71663b6e392cfa2b372b0a27346ae2de8ea608dd2f8e307c31`

```dockerfile
```

-	Layers:
	-	`sha256:74364e5c7720e83ad343b975d9a65bb9ca7f9689948c422c502889ae59651691`  
		Last Modified: Tue, 17 Dec 2024 20:07:27 GMT  
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
$ docker pull nats@sha256:ab1de7a4552e1aa8676fad12ef36415434dcb0f5e1a8f4bd98c1c0b0e23c3108
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
$ docker pull nats@sha256:29cae9fbb27a68c8d042585d900cfe6c6a0687be3fc48e3749907266646626f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10017369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:575ec7872076c7f2ef48a2565b99ac2557abe519a55646c520a6280dda578672`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ee010a6f8d65980fb2a10e8ed490ac5deeb2c57778398caaff2dd317814317`  
		Last Modified: Tue, 17 Dec 2024 19:28:31 GMT  
		Size: 6.4 MB (6371955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e4e90f8624a081c4f8b6390a205113fb3d4efb52df8b8c4c109f3cbb45e0d7`  
		Last Modified: Tue, 17 Dec 2024 19:28:31 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17488456929723e351ddeda9e989781d4d3524c497aac4a9f4986b0a3bab4945`  
		Last Modified: Tue, 17 Dec 2024 19:28:31 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:cfdf92514ba877de3aba717f98d14ddce733bbffb44c334f902dea9147d674fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1c24142e5eed2c70f10105cdb7898204d5e69436be032d28f67396ed116411e`

```dockerfile
```

-	Layers:
	-	`sha256:e27f4eb3a71bf3ac9a8a6b932556310d82674abcc3248ab6d039babb897b959a`  
		Last Modified: Tue, 17 Dec 2024 19:28:31 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:2d66dc5023cd20e375636ada663a151dc2cf1f1b81366b1be5734dfef827d758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9386302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff9ef91ef8059e02d14a92ff39f20c50ea1a73599f50d8896f1f6df2d1381e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af40215e42d92bd72970c881af08ff0be57978182c0ffc369a75fa63356a3ca8`  
		Last Modified: Tue, 17 Dec 2024 19:29:36 GMT  
		Size: 6.0 MB (6018149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a327f5c4e15af30fe773e5bccc7b9078fd582fa78f7b5fd0d7b2506ec3b4086`  
		Last Modified: Tue, 17 Dec 2024 19:29:35 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8cb23494fbc6a634aa201b70ba71a79f6de1cace9996ea9b672757cf7bca461`  
		Last Modified: Tue, 17 Dec 2024 19:29:35 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:8b64eedc6a198a946e7e91844bdd9f74180c28ccc096147695e88e4e6cf87ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ad27d08cd2faace9930eb98b50cc3e27beddd7c101b0d33c4e03535c60ad2a`

```dockerfile
```

-	Layers:
	-	`sha256:1116a69deb5d903c668d4d739424c27736d4b250ac54f43eb4429c6a19165b7e`  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:9e84106ad88ced73c824cadca62f7e96f3015b20deba910b2e0b55189cc6f173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9107614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69dffc7badcd9eba6823886d65acbb0cfa112f8883783d134dc809e90b98f145`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc51158f73d5719731f6de6d6d24db0e1d4124a5ecd84bab5548388db0eded5a`  
		Last Modified: Tue, 17 Dec 2024 19:29:01 GMT  
		Size: 6.0 MB (6006607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c2203fb8a3575ff778e4d6965d233a19dd24a5bc90771ecca824833e155b06`  
		Last Modified: Tue, 17 Dec 2024 19:29:00 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacb2912b87b4350617243e5835a14b89a4006eb352e2e093b0b93284d61e070`  
		Last Modified: Tue, 17 Dec 2024 19:29:00 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:130347efdbef62b178c834dc5fda8f86a80bc17ee5ed4761825f0d10763932a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25422fc7bc14c1b14b45b22f895a7d64d49eb334e7564262dc1c10e8eca6abf9`

```dockerfile
```

-	Layers:
	-	`sha256:eb58607b3135d344e5e98c1c7130894a0412f1c8d219ba16ccfd1b8aaf8946cf`  
		Last Modified: Tue, 17 Dec 2024 19:29:00 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:91b0e0ed22e13b4b240286a274219ad0b7bef2ab2e5b9cfd4152e5c9c4ad246e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9912392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b9a70b84b2c7628f856d55590dc824bba274042faf6521e6dcecebf44b480f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d311607882428389c8bbb10058ff9f4a07c6714b605f6bd92afa58faf53ccf1`  
		Last Modified: Tue, 17 Dec 2024 19:29:19 GMT  
		Size: 5.9 MB (5918236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:120d4d49d4ce04dd2b71e71ea3c19191133df462671d15362ec224b0c7a6b329`  
		Last Modified: Tue, 17 Dec 2024 19:29:19 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2348ec882817d42d419fca6d6073f5980a4808bea9d36c67cc612d20f656a0c`  
		Last Modified: Tue, 17 Dec 2024 19:29:19 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:2bcdf7d278748efd5f3c41ad5a847840ecabae85a7f38d8bd2eab34f5d925562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51691faecee58ef8255c969e6e92d7f2119288caa70eb618072608de605727bf`

```dockerfile
```

-	Layers:
	-	`sha256:4ecc6db36ffe92c81d7ea0b122f98496f5b6cc7de311e1f92f29189a5e94477f`  
		Last Modified: Tue, 17 Dec 2024 19:29:19 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:3449804a92d7c624c6e5bbc48d29d3c785046de22627a6c4f25962e2f45affee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9464345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:526d9d5508e133079e9f97028d93c63cb13fd416f25a11fad5808f052ab50812`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-ppc64le.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:a12ff663c50b78339bd273940ba035e29d8220954846a4c35a5f79080b37a3d3`  
		Last Modified: Thu, 05 Dec 2024 22:18:21 GMT  
		Size: 3.6 MB (3577108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:672eaefb89f5c4c03dc1dfd0e81f2f3ad81e138d028b4087f87cd3ee9958423d`  
		Last Modified: Tue, 17 Dec 2024 19:28:25 GMT  
		Size: 5.9 MB (5886266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f573fb4c0caa43a456c5b6e69b41c587ceb460ed049cbbe6b7689f71878eb94b`  
		Last Modified: Tue, 17 Dec 2024 19:28:25 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6435cc906fd110b2082eb0900e048df12cb9ea784fd2c023d2802fb66bac5a46`  
		Last Modified: Tue, 17 Dec 2024 19:28:25 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:160f40bbb801fb82f584f14f06735d924e6e69fd6c2fc93acdeacf87846b7cfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159b7defb72e6a0f49e1e548aa2c7df4ee6b842169a267dd9652a7c0f0d338e0`

```dockerfile
```

-	Layers:
	-	`sha256:983eda21d01dd67d3a7bdb35b440c949942f2f1161e0e3a7ee0b98439732a7a6`  
		Last Modified: Tue, 17 Dec 2024 19:28:25 GMT  
		Size: 14.4 KB (14389 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; s390x

```console
$ docker pull nats@sha256:231606d59bf67bf0225b8ff9322391ff528761f9e0417de1607425d5afd4adae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9686596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ab6034672329d984598a6d355339e336c65909875e48379c20c3a8492d5243e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1426b7374b29c0dcb926cdf54914b6a90fcca6f795e94ecee6d05578db18dea`  
		Last Modified: Tue, 17 Dec 2024 19:29:54 GMT  
		Size: 6.2 MB (6216106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a8d5d73de329406149614539003981ece64c24f00a8063d0218ff3b79b4fdd`  
		Last Modified: Tue, 17 Dec 2024 19:29:54 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b700a203382b44c168db5158adc0136d31b657f61a768de50ce397725977f302`  
		Last Modified: Tue, 17 Dec 2024 19:29:54 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:9cb0f384d223b0fb893a8e6883d30cdc52d031457d2466c639299a197a71b02d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb032d67922303b6505eaeb4c3a2e1e93ce05ce4ac7358439ea0f5eda3f19cb6`

```dockerfile
```

-	Layers:
	-	`sha256:8dfd4b0613d89e1631f9a0b566c194348623859b7aab6010157dfa1a5ef47147`  
		Last Modified: Tue, 17 Dec 2024 19:29:54 GMT  
		Size: 14.3 KB (14321 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-alpine3.21`

```console
$ docker pull nats@sha256:ab1de7a4552e1aa8676fad12ef36415434dcb0f5e1a8f4bd98c1c0b0e23c3108
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
$ docker pull nats@sha256:29cae9fbb27a68c8d042585d900cfe6c6a0687be3fc48e3749907266646626f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10017369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:575ec7872076c7f2ef48a2565b99ac2557abe519a55646c520a6280dda578672`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ee010a6f8d65980fb2a10e8ed490ac5deeb2c57778398caaff2dd317814317`  
		Last Modified: Tue, 17 Dec 2024 19:28:31 GMT  
		Size: 6.4 MB (6371955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e4e90f8624a081c4f8b6390a205113fb3d4efb52df8b8c4c109f3cbb45e0d7`  
		Last Modified: Tue, 17 Dec 2024 19:28:31 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17488456929723e351ddeda9e989781d4d3524c497aac4a9f4986b0a3bab4945`  
		Last Modified: Tue, 17 Dec 2024 19:28:31 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:cfdf92514ba877de3aba717f98d14ddce733bbffb44c334f902dea9147d674fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1c24142e5eed2c70f10105cdb7898204d5e69436be032d28f67396ed116411e`

```dockerfile
```

-	Layers:
	-	`sha256:e27f4eb3a71bf3ac9a8a6b932556310d82674abcc3248ab6d039babb897b959a`  
		Last Modified: Tue, 17 Dec 2024 19:28:31 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:2d66dc5023cd20e375636ada663a151dc2cf1f1b81366b1be5734dfef827d758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9386302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff9ef91ef8059e02d14a92ff39f20c50ea1a73599f50d8896f1f6df2d1381e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af40215e42d92bd72970c881af08ff0be57978182c0ffc369a75fa63356a3ca8`  
		Last Modified: Tue, 17 Dec 2024 19:29:36 GMT  
		Size: 6.0 MB (6018149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a327f5c4e15af30fe773e5bccc7b9078fd582fa78f7b5fd0d7b2506ec3b4086`  
		Last Modified: Tue, 17 Dec 2024 19:29:35 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8cb23494fbc6a634aa201b70ba71a79f6de1cace9996ea9b672757cf7bca461`  
		Last Modified: Tue, 17 Dec 2024 19:29:35 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:8b64eedc6a198a946e7e91844bdd9f74180c28ccc096147695e88e4e6cf87ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ad27d08cd2faace9930eb98b50cc3e27beddd7c101b0d33c4e03535c60ad2a`

```dockerfile
```

-	Layers:
	-	`sha256:1116a69deb5d903c668d4d739424c27736d4b250ac54f43eb4429c6a19165b7e`  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:9e84106ad88ced73c824cadca62f7e96f3015b20deba910b2e0b55189cc6f173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9107614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69dffc7badcd9eba6823886d65acbb0cfa112f8883783d134dc809e90b98f145`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc51158f73d5719731f6de6d6d24db0e1d4124a5ecd84bab5548388db0eded5a`  
		Last Modified: Tue, 17 Dec 2024 19:29:01 GMT  
		Size: 6.0 MB (6006607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c2203fb8a3575ff778e4d6965d233a19dd24a5bc90771ecca824833e155b06`  
		Last Modified: Tue, 17 Dec 2024 19:29:00 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacb2912b87b4350617243e5835a14b89a4006eb352e2e093b0b93284d61e070`  
		Last Modified: Tue, 17 Dec 2024 19:29:00 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:130347efdbef62b178c834dc5fda8f86a80bc17ee5ed4761825f0d10763932a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25422fc7bc14c1b14b45b22f895a7d64d49eb334e7564262dc1c10e8eca6abf9`

```dockerfile
```

-	Layers:
	-	`sha256:eb58607b3135d344e5e98c1c7130894a0412f1c8d219ba16ccfd1b8aaf8946cf`  
		Last Modified: Tue, 17 Dec 2024 19:29:00 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:91b0e0ed22e13b4b240286a274219ad0b7bef2ab2e5b9cfd4152e5c9c4ad246e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9912392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b9a70b84b2c7628f856d55590dc824bba274042faf6521e6dcecebf44b480f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d311607882428389c8bbb10058ff9f4a07c6714b605f6bd92afa58faf53ccf1`  
		Last Modified: Tue, 17 Dec 2024 19:29:19 GMT  
		Size: 5.9 MB (5918236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:120d4d49d4ce04dd2b71e71ea3c19191133df462671d15362ec224b0c7a6b329`  
		Last Modified: Tue, 17 Dec 2024 19:29:19 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2348ec882817d42d419fca6d6073f5980a4808bea9d36c67cc612d20f656a0c`  
		Last Modified: Tue, 17 Dec 2024 19:29:19 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:2bcdf7d278748efd5f3c41ad5a847840ecabae85a7f38d8bd2eab34f5d925562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51691faecee58ef8255c969e6e92d7f2119288caa70eb618072608de605727bf`

```dockerfile
```

-	Layers:
	-	`sha256:4ecc6db36ffe92c81d7ea0b122f98496f5b6cc7de311e1f92f29189a5e94477f`  
		Last Modified: Tue, 17 Dec 2024 19:29:19 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:3449804a92d7c624c6e5bbc48d29d3c785046de22627a6c4f25962e2f45affee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9464345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:526d9d5508e133079e9f97028d93c63cb13fd416f25a11fad5808f052ab50812`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-ppc64le.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:a12ff663c50b78339bd273940ba035e29d8220954846a4c35a5f79080b37a3d3`  
		Last Modified: Thu, 05 Dec 2024 22:18:21 GMT  
		Size: 3.6 MB (3577108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:672eaefb89f5c4c03dc1dfd0e81f2f3ad81e138d028b4087f87cd3ee9958423d`  
		Last Modified: Tue, 17 Dec 2024 19:28:25 GMT  
		Size: 5.9 MB (5886266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f573fb4c0caa43a456c5b6e69b41c587ceb460ed049cbbe6b7689f71878eb94b`  
		Last Modified: Tue, 17 Dec 2024 19:28:25 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6435cc906fd110b2082eb0900e048df12cb9ea784fd2c023d2802fb66bac5a46`  
		Last Modified: Tue, 17 Dec 2024 19:28:25 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:160f40bbb801fb82f584f14f06735d924e6e69fd6c2fc93acdeacf87846b7cfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159b7defb72e6a0f49e1e548aa2c7df4ee6b842169a267dd9652a7c0f0d338e0`

```dockerfile
```

-	Layers:
	-	`sha256:983eda21d01dd67d3a7bdb35b440c949942f2f1161e0e3a7ee0b98439732a7a6`  
		Last Modified: Tue, 17 Dec 2024 19:28:25 GMT  
		Size: 14.4 KB (14389 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:231606d59bf67bf0225b8ff9322391ff528761f9e0417de1607425d5afd4adae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9686596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ab6034672329d984598a6d355339e336c65909875e48379c20c3a8492d5243e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1426b7374b29c0dcb926cdf54914b6a90fcca6f795e94ecee6d05578db18dea`  
		Last Modified: Tue, 17 Dec 2024 19:29:54 GMT  
		Size: 6.2 MB (6216106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a8d5d73de329406149614539003981ece64c24f00a8063d0218ff3b79b4fdd`  
		Last Modified: Tue, 17 Dec 2024 19:29:54 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b700a203382b44c168db5158adc0136d31b657f61a768de50ce397725977f302`  
		Last Modified: Tue, 17 Dec 2024 19:29:54 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:9cb0f384d223b0fb893a8e6883d30cdc52d031457d2466c639299a197a71b02d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb032d67922303b6505eaeb4c3a2e1e93ce05ce4ac7358439ea0f5eda3f19cb6`

```dockerfile
```

-	Layers:
	-	`sha256:8dfd4b0613d89e1631f9a0b566c194348623859b7aab6010157dfa1a5ef47147`  
		Last Modified: Tue, 17 Dec 2024 19:29:54 GMT  
		Size: 14.3 KB (14321 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-linux`

```console
$ docker pull nats@sha256:d5cf5fddd6246b37ee3acb3b67903298c21827c1862cd95d0d9f282794c82190
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
$ docker pull nats@sha256:67d3b85ece6c782cf7ead3ecb3a1ac84ea0f1a90692e49699e78cbded1b303f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5905656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30790e9a65a19f582b2ef7ef953584341edfe5d6fa4e0ca626c151bd29d42300`
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
		Size: 5.9 MB (5905148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8de2329765d2e9e6ad2eef24244fb693d2372ce8561eee2d04a4b15613d4957`  
		Last Modified: Tue, 17 Dec 2024 20:07:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:bf98881f063cf871ca1790de74f2e754f9d790b3db90451f6b5da630335ca9fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b933f94df98aa627cb8bf50b2acae5ed54c95244c49afe60cd9b9504d44c4dc8`

```dockerfile
```

-	Layers:
	-	`sha256:021e7dd96b286525c844698e284fea042a82a034acb1e22fe017dd14f20618a5`  
		Last Modified: Tue, 17 Dec 2024 20:07:46 GMT  
		Size: 10.5 KB (10473 bytes)  
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
$ docker pull nats@sha256:25129eb990a4dd587a984e2e2f97ef3492dc391a45119430a8a33cee51dfa7b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5418850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cf4789450fb70da1d11cc8480fe7fc5895888d5dec9b2f39fc4363a18f5e15e`
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
	-	`sha256:2154049e56fd256d2148c4e2e139e5269047c2bb399664b65fce45bbe9852ba6`  
		Last Modified: Tue, 17 Dec 2024 20:07:27 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:01db48579033a378b0e612214b5ca3906a4b332620348ae699697ca38929b3a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76ff46f64e472e71663b6e392cfa2b372b0a27346ae2de8ea608dd2f8e307c31`

```dockerfile
```

-	Layers:
	-	`sha256:74364e5c7720e83ad343b975d9a65bb9ca7f9689948c422c502889ae59651691`  
		Last Modified: Tue, 17 Dec 2024 20:07:27 GMT  
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
$ docker pull nats@sha256:d5cf5fddd6246b37ee3acb3b67903298c21827c1862cd95d0d9f282794c82190
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
$ docker pull nats@sha256:67d3b85ece6c782cf7ead3ecb3a1ac84ea0f1a90692e49699e78cbded1b303f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5905656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30790e9a65a19f582b2ef7ef953584341edfe5d6fa4e0ca626c151bd29d42300`
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
		Size: 5.9 MB (5905148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8de2329765d2e9e6ad2eef24244fb693d2372ce8561eee2d04a4b15613d4957`  
		Last Modified: Tue, 17 Dec 2024 20:07:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:bf98881f063cf871ca1790de74f2e754f9d790b3db90451f6b5da630335ca9fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b933f94df98aa627cb8bf50b2acae5ed54c95244c49afe60cd9b9504d44c4dc8`

```dockerfile
```

-	Layers:
	-	`sha256:021e7dd96b286525c844698e284fea042a82a034acb1e22fe017dd14f20618a5`  
		Last Modified: Tue, 17 Dec 2024 20:07:46 GMT  
		Size: 10.5 KB (10473 bytes)  
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
$ docker pull nats@sha256:25129eb990a4dd587a984e2e2f97ef3492dc391a45119430a8a33cee51dfa7b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5418850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cf4789450fb70da1d11cc8480fe7fc5895888d5dec9b2f39fc4363a18f5e15e`
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
	-	`sha256:2154049e56fd256d2148c4e2e139e5269047c2bb399664b65fce45bbe9852ba6`  
		Last Modified: Tue, 17 Dec 2024 20:07:27 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:01db48579033a378b0e612214b5ca3906a4b332620348ae699697ca38929b3a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76ff46f64e472e71663b6e392cfa2b372b0a27346ae2de8ea608dd2f8e307c31`

```dockerfile
```

-	Layers:
	-	`sha256:74364e5c7720e83ad343b975d9a65bb9ca7f9689948c422c502889ae59651691`  
		Last Modified: Tue, 17 Dec 2024 20:07:27 GMT  
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
$ docker pull nats@sha256:d4c302ac4a0d84afff801c413f7f32e9e76505030d020b988605a3e839cbcd95
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
$ docker pull nats@sha256:67d3b85ece6c782cf7ead3ecb3a1ac84ea0f1a90692e49699e78cbded1b303f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5905656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30790e9a65a19f582b2ef7ef953584341edfe5d6fa4e0ca626c151bd29d42300`
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
		Size: 5.9 MB (5905148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8de2329765d2e9e6ad2eef24244fb693d2372ce8561eee2d04a4b15613d4957`  
		Last Modified: Tue, 17 Dec 2024 20:07:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24` - unknown; unknown

```console
$ docker pull nats@sha256:bf98881f063cf871ca1790de74f2e754f9d790b3db90451f6b5da630335ca9fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b933f94df98aa627cb8bf50b2acae5ed54c95244c49afe60cd9b9504d44c4dc8`

```dockerfile
```

-	Layers:
	-	`sha256:021e7dd96b286525c844698e284fea042a82a034acb1e22fe017dd14f20618a5`  
		Last Modified: Tue, 17 Dec 2024 20:07:46 GMT  
		Size: 10.5 KB (10473 bytes)  
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
$ docker pull nats@sha256:25129eb990a4dd587a984e2e2f97ef3492dc391a45119430a8a33cee51dfa7b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5418850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cf4789450fb70da1d11cc8480fe7fc5895888d5dec9b2f39fc4363a18f5e15e`
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
	-	`sha256:2154049e56fd256d2148c4e2e139e5269047c2bb399664b65fce45bbe9852ba6`  
		Last Modified: Tue, 17 Dec 2024 20:07:27 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24` - unknown; unknown

```console
$ docker pull nats@sha256:01db48579033a378b0e612214b5ca3906a4b332620348ae699697ca38929b3a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76ff46f64e472e71663b6e392cfa2b372b0a27346ae2de8ea608dd2f8e307c31`

```dockerfile
```

-	Layers:
	-	`sha256:74364e5c7720e83ad343b975d9a65bb9ca7f9689948c422c502889ae59651691`  
		Last Modified: Tue, 17 Dec 2024 20:07:27 GMT  
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
$ docker pull nats@sha256:ab1de7a4552e1aa8676fad12ef36415434dcb0f5e1a8f4bd98c1c0b0e23c3108
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
$ docker pull nats@sha256:29cae9fbb27a68c8d042585d900cfe6c6a0687be3fc48e3749907266646626f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10017369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:575ec7872076c7f2ef48a2565b99ac2557abe519a55646c520a6280dda578672`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ee010a6f8d65980fb2a10e8ed490ac5deeb2c57778398caaff2dd317814317`  
		Last Modified: Tue, 17 Dec 2024 19:28:31 GMT  
		Size: 6.4 MB (6371955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e4e90f8624a081c4f8b6390a205113fb3d4efb52df8b8c4c109f3cbb45e0d7`  
		Last Modified: Tue, 17 Dec 2024 19:28:31 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17488456929723e351ddeda9e989781d4d3524c497aac4a9f4986b0a3bab4945`  
		Last Modified: Tue, 17 Dec 2024 19:28:31 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:cfdf92514ba877de3aba717f98d14ddce733bbffb44c334f902dea9147d674fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1c24142e5eed2c70f10105cdb7898204d5e69436be032d28f67396ed116411e`

```dockerfile
```

-	Layers:
	-	`sha256:e27f4eb3a71bf3ac9a8a6b932556310d82674abcc3248ab6d039babb897b959a`  
		Last Modified: Tue, 17 Dec 2024 19:28:31 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.24-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:2d66dc5023cd20e375636ada663a151dc2cf1f1b81366b1be5734dfef827d758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9386302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff9ef91ef8059e02d14a92ff39f20c50ea1a73599f50d8896f1f6df2d1381e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af40215e42d92bd72970c881af08ff0be57978182c0ffc369a75fa63356a3ca8`  
		Last Modified: Tue, 17 Dec 2024 19:29:36 GMT  
		Size: 6.0 MB (6018149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a327f5c4e15af30fe773e5bccc7b9078fd582fa78f7b5fd0d7b2506ec3b4086`  
		Last Modified: Tue, 17 Dec 2024 19:29:35 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8cb23494fbc6a634aa201b70ba71a79f6de1cace9996ea9b672757cf7bca461`  
		Last Modified: Tue, 17 Dec 2024 19:29:35 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:8b64eedc6a198a946e7e91844bdd9f74180c28ccc096147695e88e4e6cf87ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ad27d08cd2faace9930eb98b50cc3e27beddd7c101b0d33c4e03535c60ad2a`

```dockerfile
```

-	Layers:
	-	`sha256:1116a69deb5d903c668d4d739424c27736d4b250ac54f43eb4429c6a19165b7e`  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.24-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:9e84106ad88ced73c824cadca62f7e96f3015b20deba910b2e0b55189cc6f173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9107614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69dffc7badcd9eba6823886d65acbb0cfa112f8883783d134dc809e90b98f145`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc51158f73d5719731f6de6d6d24db0e1d4124a5ecd84bab5548388db0eded5a`  
		Last Modified: Tue, 17 Dec 2024 19:29:01 GMT  
		Size: 6.0 MB (6006607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c2203fb8a3575ff778e4d6965d233a19dd24a5bc90771ecca824833e155b06`  
		Last Modified: Tue, 17 Dec 2024 19:29:00 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacb2912b87b4350617243e5835a14b89a4006eb352e2e093b0b93284d61e070`  
		Last Modified: Tue, 17 Dec 2024 19:29:00 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:130347efdbef62b178c834dc5fda8f86a80bc17ee5ed4761825f0d10763932a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25422fc7bc14c1b14b45b22f895a7d64d49eb334e7564262dc1c10e8eca6abf9`

```dockerfile
```

-	Layers:
	-	`sha256:eb58607b3135d344e5e98c1c7130894a0412f1c8d219ba16ccfd1b8aaf8946cf`  
		Last Modified: Tue, 17 Dec 2024 19:29:00 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.24-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:91b0e0ed22e13b4b240286a274219ad0b7bef2ab2e5b9cfd4152e5c9c4ad246e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9912392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b9a70b84b2c7628f856d55590dc824bba274042faf6521e6dcecebf44b480f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d311607882428389c8bbb10058ff9f4a07c6714b605f6bd92afa58faf53ccf1`  
		Last Modified: Tue, 17 Dec 2024 19:29:19 GMT  
		Size: 5.9 MB (5918236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:120d4d49d4ce04dd2b71e71ea3c19191133df462671d15362ec224b0c7a6b329`  
		Last Modified: Tue, 17 Dec 2024 19:29:19 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2348ec882817d42d419fca6d6073f5980a4808bea9d36c67cc612d20f656a0c`  
		Last Modified: Tue, 17 Dec 2024 19:29:19 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:2bcdf7d278748efd5f3c41ad5a847840ecabae85a7f38d8bd2eab34f5d925562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51691faecee58ef8255c969e6e92d7f2119288caa70eb618072608de605727bf`

```dockerfile
```

-	Layers:
	-	`sha256:4ecc6db36ffe92c81d7ea0b122f98496f5b6cc7de311e1f92f29189a5e94477f`  
		Last Modified: Tue, 17 Dec 2024 19:29:19 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.24-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:3449804a92d7c624c6e5bbc48d29d3c785046de22627a6c4f25962e2f45affee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9464345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:526d9d5508e133079e9f97028d93c63cb13fd416f25a11fad5808f052ab50812`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-ppc64le.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:a12ff663c50b78339bd273940ba035e29d8220954846a4c35a5f79080b37a3d3`  
		Last Modified: Thu, 05 Dec 2024 22:18:21 GMT  
		Size: 3.6 MB (3577108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:672eaefb89f5c4c03dc1dfd0e81f2f3ad81e138d028b4087f87cd3ee9958423d`  
		Last Modified: Tue, 17 Dec 2024 19:28:25 GMT  
		Size: 5.9 MB (5886266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f573fb4c0caa43a456c5b6e69b41c587ceb460ed049cbbe6b7689f71878eb94b`  
		Last Modified: Tue, 17 Dec 2024 19:28:25 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6435cc906fd110b2082eb0900e048df12cb9ea784fd2c023d2802fb66bac5a46`  
		Last Modified: Tue, 17 Dec 2024 19:28:25 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:160f40bbb801fb82f584f14f06735d924e6e69fd6c2fc93acdeacf87846b7cfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159b7defb72e6a0f49e1e548aa2c7df4ee6b842169a267dd9652a7c0f0d338e0`

```dockerfile
```

-	Layers:
	-	`sha256:983eda21d01dd67d3a7bdb35b440c949942f2f1161e0e3a7ee0b98439732a7a6`  
		Last Modified: Tue, 17 Dec 2024 19:28:25 GMT  
		Size: 14.4 KB (14389 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.24-alpine` - linux; s390x

```console
$ docker pull nats@sha256:231606d59bf67bf0225b8ff9322391ff528761f9e0417de1607425d5afd4adae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9686596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ab6034672329d984598a6d355339e336c65909875e48379c20c3a8492d5243e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1426b7374b29c0dcb926cdf54914b6a90fcca6f795e94ecee6d05578db18dea`  
		Last Modified: Tue, 17 Dec 2024 19:29:54 GMT  
		Size: 6.2 MB (6216106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a8d5d73de329406149614539003981ece64c24f00a8063d0218ff3b79b4fdd`  
		Last Modified: Tue, 17 Dec 2024 19:29:54 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b700a203382b44c168db5158adc0136d31b657f61a768de50ce397725977f302`  
		Last Modified: Tue, 17 Dec 2024 19:29:54 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:9cb0f384d223b0fb893a8e6883d30cdc52d031457d2466c639299a197a71b02d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb032d67922303b6505eaeb4c3a2e1e93ce05ce4ac7358439ea0f5eda3f19cb6`

```dockerfile
```

-	Layers:
	-	`sha256:8dfd4b0613d89e1631f9a0b566c194348623859b7aab6010157dfa1a5ef47147`  
		Last Modified: Tue, 17 Dec 2024 19:29:54 GMT  
		Size: 14.3 KB (14321 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.24-alpine3.21`

```console
$ docker pull nats@sha256:ab1de7a4552e1aa8676fad12ef36415434dcb0f5e1a8f4bd98c1c0b0e23c3108
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
$ docker pull nats@sha256:29cae9fbb27a68c8d042585d900cfe6c6a0687be3fc48e3749907266646626f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10017369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:575ec7872076c7f2ef48a2565b99ac2557abe519a55646c520a6280dda578672`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ee010a6f8d65980fb2a10e8ed490ac5deeb2c57778398caaff2dd317814317`  
		Last Modified: Tue, 17 Dec 2024 19:28:31 GMT  
		Size: 6.4 MB (6371955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e4e90f8624a081c4f8b6390a205113fb3d4efb52df8b8c4c109f3cbb45e0d7`  
		Last Modified: Tue, 17 Dec 2024 19:28:31 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17488456929723e351ddeda9e989781d4d3524c497aac4a9f4986b0a3bab4945`  
		Last Modified: Tue, 17 Dec 2024 19:28:31 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:cfdf92514ba877de3aba717f98d14ddce733bbffb44c334f902dea9147d674fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1c24142e5eed2c70f10105cdb7898204d5e69436be032d28f67396ed116411e`

```dockerfile
```

-	Layers:
	-	`sha256:e27f4eb3a71bf3ac9a8a6b932556310d82674abcc3248ab6d039babb897b959a`  
		Last Modified: Tue, 17 Dec 2024 19:28:31 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.24-alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:2d66dc5023cd20e375636ada663a151dc2cf1f1b81366b1be5734dfef827d758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9386302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff9ef91ef8059e02d14a92ff39f20c50ea1a73599f50d8896f1f6df2d1381e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af40215e42d92bd72970c881af08ff0be57978182c0ffc369a75fa63356a3ca8`  
		Last Modified: Tue, 17 Dec 2024 19:29:36 GMT  
		Size: 6.0 MB (6018149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a327f5c4e15af30fe773e5bccc7b9078fd582fa78f7b5fd0d7b2506ec3b4086`  
		Last Modified: Tue, 17 Dec 2024 19:29:35 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8cb23494fbc6a634aa201b70ba71a79f6de1cace9996ea9b672757cf7bca461`  
		Last Modified: Tue, 17 Dec 2024 19:29:35 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:8b64eedc6a198a946e7e91844bdd9f74180c28ccc096147695e88e4e6cf87ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ad27d08cd2faace9930eb98b50cc3e27beddd7c101b0d33c4e03535c60ad2a`

```dockerfile
```

-	Layers:
	-	`sha256:1116a69deb5d903c668d4d739424c27736d4b250ac54f43eb4429c6a19165b7e`  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.24-alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:9e84106ad88ced73c824cadca62f7e96f3015b20deba910b2e0b55189cc6f173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9107614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69dffc7badcd9eba6823886d65acbb0cfa112f8883783d134dc809e90b98f145`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc51158f73d5719731f6de6d6d24db0e1d4124a5ecd84bab5548388db0eded5a`  
		Last Modified: Tue, 17 Dec 2024 19:29:01 GMT  
		Size: 6.0 MB (6006607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c2203fb8a3575ff778e4d6965d233a19dd24a5bc90771ecca824833e155b06`  
		Last Modified: Tue, 17 Dec 2024 19:29:00 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacb2912b87b4350617243e5835a14b89a4006eb352e2e093b0b93284d61e070`  
		Last Modified: Tue, 17 Dec 2024 19:29:00 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:130347efdbef62b178c834dc5fda8f86a80bc17ee5ed4761825f0d10763932a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25422fc7bc14c1b14b45b22f895a7d64d49eb334e7564262dc1c10e8eca6abf9`

```dockerfile
```

-	Layers:
	-	`sha256:eb58607b3135d344e5e98c1c7130894a0412f1c8d219ba16ccfd1b8aaf8946cf`  
		Last Modified: Tue, 17 Dec 2024 19:29:00 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.24-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:91b0e0ed22e13b4b240286a274219ad0b7bef2ab2e5b9cfd4152e5c9c4ad246e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9912392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b9a70b84b2c7628f856d55590dc824bba274042faf6521e6dcecebf44b480f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d311607882428389c8bbb10058ff9f4a07c6714b605f6bd92afa58faf53ccf1`  
		Last Modified: Tue, 17 Dec 2024 19:29:19 GMT  
		Size: 5.9 MB (5918236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:120d4d49d4ce04dd2b71e71ea3c19191133df462671d15362ec224b0c7a6b329`  
		Last Modified: Tue, 17 Dec 2024 19:29:19 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2348ec882817d42d419fca6d6073f5980a4808bea9d36c67cc612d20f656a0c`  
		Last Modified: Tue, 17 Dec 2024 19:29:19 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:2bcdf7d278748efd5f3c41ad5a847840ecabae85a7f38d8bd2eab34f5d925562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51691faecee58ef8255c969e6e92d7f2119288caa70eb618072608de605727bf`

```dockerfile
```

-	Layers:
	-	`sha256:4ecc6db36ffe92c81d7ea0b122f98496f5b6cc7de311e1f92f29189a5e94477f`  
		Last Modified: Tue, 17 Dec 2024 19:29:19 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.24-alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:3449804a92d7c624c6e5bbc48d29d3c785046de22627a6c4f25962e2f45affee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9464345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:526d9d5508e133079e9f97028d93c63cb13fd416f25a11fad5808f052ab50812`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-ppc64le.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:a12ff663c50b78339bd273940ba035e29d8220954846a4c35a5f79080b37a3d3`  
		Last Modified: Thu, 05 Dec 2024 22:18:21 GMT  
		Size: 3.6 MB (3577108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:672eaefb89f5c4c03dc1dfd0e81f2f3ad81e138d028b4087f87cd3ee9958423d`  
		Last Modified: Tue, 17 Dec 2024 19:28:25 GMT  
		Size: 5.9 MB (5886266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f573fb4c0caa43a456c5b6e69b41c587ceb460ed049cbbe6b7689f71878eb94b`  
		Last Modified: Tue, 17 Dec 2024 19:28:25 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6435cc906fd110b2082eb0900e048df12cb9ea784fd2c023d2802fb66bac5a46`  
		Last Modified: Tue, 17 Dec 2024 19:28:25 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:160f40bbb801fb82f584f14f06735d924e6e69fd6c2fc93acdeacf87846b7cfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159b7defb72e6a0f49e1e548aa2c7df4ee6b842169a267dd9652a7c0f0d338e0`

```dockerfile
```

-	Layers:
	-	`sha256:983eda21d01dd67d3a7bdb35b440c949942f2f1161e0e3a7ee0b98439732a7a6`  
		Last Modified: Tue, 17 Dec 2024 19:28:25 GMT  
		Size: 14.4 KB (14389 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.24-alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:231606d59bf67bf0225b8ff9322391ff528761f9e0417de1607425d5afd4adae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9686596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ab6034672329d984598a6d355339e336c65909875e48379c20c3a8492d5243e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1426b7374b29c0dcb926cdf54914b6a90fcca6f795e94ecee6d05578db18dea`  
		Last Modified: Tue, 17 Dec 2024 19:29:54 GMT  
		Size: 6.2 MB (6216106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a8d5d73de329406149614539003981ece64c24f00a8063d0218ff3b79b4fdd`  
		Last Modified: Tue, 17 Dec 2024 19:29:54 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b700a203382b44c168db5158adc0136d31b657f61a768de50ce397725977f302`  
		Last Modified: Tue, 17 Dec 2024 19:29:54 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:9cb0f384d223b0fb893a8e6883d30cdc52d031457d2466c639299a197a71b02d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb032d67922303b6505eaeb4c3a2e1e93ce05ce4ac7358439ea0f5eda3f19cb6`

```dockerfile
```

-	Layers:
	-	`sha256:8dfd4b0613d89e1631f9a0b566c194348623859b7aab6010157dfa1a5ef47147`  
		Last Modified: Tue, 17 Dec 2024 19:29:54 GMT  
		Size: 14.3 KB (14321 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.24-linux`

```console
$ docker pull nats@sha256:d5cf5fddd6246b37ee3acb3b67903298c21827c1862cd95d0d9f282794c82190
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
$ docker pull nats@sha256:67d3b85ece6c782cf7ead3ecb3a1ac84ea0f1a90692e49699e78cbded1b303f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5905656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30790e9a65a19f582b2ef7ef953584341edfe5d6fa4e0ca626c151bd29d42300`
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
		Size: 5.9 MB (5905148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8de2329765d2e9e6ad2eef24244fb693d2372ce8561eee2d04a4b15613d4957`  
		Last Modified: Tue, 17 Dec 2024 20:07:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24-linux` - unknown; unknown

```console
$ docker pull nats@sha256:bf98881f063cf871ca1790de74f2e754f9d790b3db90451f6b5da630335ca9fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b933f94df98aa627cb8bf50b2acae5ed54c95244c49afe60cd9b9504d44c4dc8`

```dockerfile
```

-	Layers:
	-	`sha256:021e7dd96b286525c844698e284fea042a82a034acb1e22fe017dd14f20618a5`  
		Last Modified: Tue, 17 Dec 2024 20:07:46 GMT  
		Size: 10.5 KB (10473 bytes)  
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
$ docker pull nats@sha256:25129eb990a4dd587a984e2e2f97ef3492dc391a45119430a8a33cee51dfa7b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5418850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cf4789450fb70da1d11cc8480fe7fc5895888d5dec9b2f39fc4363a18f5e15e`
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
	-	`sha256:2154049e56fd256d2148c4e2e139e5269047c2bb399664b65fce45bbe9852ba6`  
		Last Modified: Tue, 17 Dec 2024 20:07:27 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24-linux` - unknown; unknown

```console
$ docker pull nats@sha256:01db48579033a378b0e612214b5ca3906a4b332620348ae699697ca38929b3a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76ff46f64e472e71663b6e392cfa2b372b0a27346ae2de8ea608dd2f8e307c31`

```dockerfile
```

-	Layers:
	-	`sha256:74364e5c7720e83ad343b975d9a65bb9ca7f9689948c422c502889ae59651691`  
		Last Modified: Tue, 17 Dec 2024 20:07:27 GMT  
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
$ docker pull nats@sha256:d5cf5fddd6246b37ee3acb3b67903298c21827c1862cd95d0d9f282794c82190
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
$ docker pull nats@sha256:67d3b85ece6c782cf7ead3ecb3a1ac84ea0f1a90692e49699e78cbded1b303f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5905656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30790e9a65a19f582b2ef7ef953584341edfe5d6fa4e0ca626c151bd29d42300`
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
		Size: 5.9 MB (5905148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8de2329765d2e9e6ad2eef24244fb693d2372ce8561eee2d04a4b15613d4957`  
		Last Modified: Tue, 17 Dec 2024 20:07:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:bf98881f063cf871ca1790de74f2e754f9d790b3db90451f6b5da630335ca9fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b933f94df98aa627cb8bf50b2acae5ed54c95244c49afe60cd9b9504d44c4dc8`

```dockerfile
```

-	Layers:
	-	`sha256:021e7dd96b286525c844698e284fea042a82a034acb1e22fe017dd14f20618a5`  
		Last Modified: Tue, 17 Dec 2024 20:07:46 GMT  
		Size: 10.5 KB (10473 bytes)  
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
$ docker pull nats@sha256:25129eb990a4dd587a984e2e2f97ef3492dc391a45119430a8a33cee51dfa7b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5418850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cf4789450fb70da1d11cc8480fe7fc5895888d5dec9b2f39fc4363a18f5e15e`
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
	-	`sha256:2154049e56fd256d2148c4e2e139e5269047c2bb399664b65fce45bbe9852ba6`  
		Last Modified: Tue, 17 Dec 2024 20:07:27 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:01db48579033a378b0e612214b5ca3906a4b332620348ae699697ca38929b3a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76ff46f64e472e71663b6e392cfa2b372b0a27346ae2de8ea608dd2f8e307c31`

```dockerfile
```

-	Layers:
	-	`sha256:74364e5c7720e83ad343b975d9a65bb9ca7f9689948c422c502889ae59651691`  
		Last Modified: Tue, 17 Dec 2024 20:07:27 GMT  
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
$ docker pull nats@sha256:ab1de7a4552e1aa8676fad12ef36415434dcb0f5e1a8f4bd98c1c0b0e23c3108
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
$ docker pull nats@sha256:29cae9fbb27a68c8d042585d900cfe6c6a0687be3fc48e3749907266646626f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10017369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:575ec7872076c7f2ef48a2565b99ac2557abe519a55646c520a6280dda578672`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ee010a6f8d65980fb2a10e8ed490ac5deeb2c57778398caaff2dd317814317`  
		Last Modified: Tue, 17 Dec 2024 19:28:31 GMT  
		Size: 6.4 MB (6371955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e4e90f8624a081c4f8b6390a205113fb3d4efb52df8b8c4c109f3cbb45e0d7`  
		Last Modified: Tue, 17 Dec 2024 19:28:31 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17488456929723e351ddeda9e989781d4d3524c497aac4a9f4986b0a3bab4945`  
		Last Modified: Tue, 17 Dec 2024 19:28:31 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:cfdf92514ba877de3aba717f98d14ddce733bbffb44c334f902dea9147d674fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1c24142e5eed2c70f10105cdb7898204d5e69436be032d28f67396ed116411e`

```dockerfile
```

-	Layers:
	-	`sha256:e27f4eb3a71bf3ac9a8a6b932556310d82674abcc3248ab6d039babb897b959a`  
		Last Modified: Tue, 17 Dec 2024 19:28:31 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:2d66dc5023cd20e375636ada663a151dc2cf1f1b81366b1be5734dfef827d758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9386302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff9ef91ef8059e02d14a92ff39f20c50ea1a73599f50d8896f1f6df2d1381e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af40215e42d92bd72970c881af08ff0be57978182c0ffc369a75fa63356a3ca8`  
		Last Modified: Tue, 17 Dec 2024 19:29:36 GMT  
		Size: 6.0 MB (6018149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a327f5c4e15af30fe773e5bccc7b9078fd582fa78f7b5fd0d7b2506ec3b4086`  
		Last Modified: Tue, 17 Dec 2024 19:29:35 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8cb23494fbc6a634aa201b70ba71a79f6de1cace9996ea9b672757cf7bca461`  
		Last Modified: Tue, 17 Dec 2024 19:29:35 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:8b64eedc6a198a946e7e91844bdd9f74180c28ccc096147695e88e4e6cf87ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ad27d08cd2faace9930eb98b50cc3e27beddd7c101b0d33c4e03535c60ad2a`

```dockerfile
```

-	Layers:
	-	`sha256:1116a69deb5d903c668d4d739424c27736d4b250ac54f43eb4429c6a19165b7e`  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:9e84106ad88ced73c824cadca62f7e96f3015b20deba910b2e0b55189cc6f173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9107614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69dffc7badcd9eba6823886d65acbb0cfa112f8883783d134dc809e90b98f145`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc51158f73d5719731f6de6d6d24db0e1d4124a5ecd84bab5548388db0eded5a`  
		Last Modified: Tue, 17 Dec 2024 19:29:01 GMT  
		Size: 6.0 MB (6006607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c2203fb8a3575ff778e4d6965d233a19dd24a5bc90771ecca824833e155b06`  
		Last Modified: Tue, 17 Dec 2024 19:29:00 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacb2912b87b4350617243e5835a14b89a4006eb352e2e093b0b93284d61e070`  
		Last Modified: Tue, 17 Dec 2024 19:29:00 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:130347efdbef62b178c834dc5fda8f86a80bc17ee5ed4761825f0d10763932a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25422fc7bc14c1b14b45b22f895a7d64d49eb334e7564262dc1c10e8eca6abf9`

```dockerfile
```

-	Layers:
	-	`sha256:eb58607b3135d344e5e98c1c7130894a0412f1c8d219ba16ccfd1b8aaf8946cf`  
		Last Modified: Tue, 17 Dec 2024 19:29:00 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:91b0e0ed22e13b4b240286a274219ad0b7bef2ab2e5b9cfd4152e5c9c4ad246e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9912392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b9a70b84b2c7628f856d55590dc824bba274042faf6521e6dcecebf44b480f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d311607882428389c8bbb10058ff9f4a07c6714b605f6bd92afa58faf53ccf1`  
		Last Modified: Tue, 17 Dec 2024 19:29:19 GMT  
		Size: 5.9 MB (5918236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:120d4d49d4ce04dd2b71e71ea3c19191133df462671d15362ec224b0c7a6b329`  
		Last Modified: Tue, 17 Dec 2024 19:29:19 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2348ec882817d42d419fca6d6073f5980a4808bea9d36c67cc612d20f656a0c`  
		Last Modified: Tue, 17 Dec 2024 19:29:19 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:2bcdf7d278748efd5f3c41ad5a847840ecabae85a7f38d8bd2eab34f5d925562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51691faecee58ef8255c969e6e92d7f2119288caa70eb618072608de605727bf`

```dockerfile
```

-	Layers:
	-	`sha256:4ecc6db36ffe92c81d7ea0b122f98496f5b6cc7de311e1f92f29189a5e94477f`  
		Last Modified: Tue, 17 Dec 2024 19:29:19 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:3449804a92d7c624c6e5bbc48d29d3c785046de22627a6c4f25962e2f45affee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9464345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:526d9d5508e133079e9f97028d93c63cb13fd416f25a11fad5808f052ab50812`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-ppc64le.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:a12ff663c50b78339bd273940ba035e29d8220954846a4c35a5f79080b37a3d3`  
		Last Modified: Thu, 05 Dec 2024 22:18:21 GMT  
		Size: 3.6 MB (3577108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:672eaefb89f5c4c03dc1dfd0e81f2f3ad81e138d028b4087f87cd3ee9958423d`  
		Last Modified: Tue, 17 Dec 2024 19:28:25 GMT  
		Size: 5.9 MB (5886266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f573fb4c0caa43a456c5b6e69b41c587ceb460ed049cbbe6b7689f71878eb94b`  
		Last Modified: Tue, 17 Dec 2024 19:28:25 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6435cc906fd110b2082eb0900e048df12cb9ea784fd2c023d2802fb66bac5a46`  
		Last Modified: Tue, 17 Dec 2024 19:28:25 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:160f40bbb801fb82f584f14f06735d924e6e69fd6c2fc93acdeacf87846b7cfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159b7defb72e6a0f49e1e548aa2c7df4ee6b842169a267dd9652a7c0f0d338e0`

```dockerfile
```

-	Layers:
	-	`sha256:983eda21d01dd67d3a7bdb35b440c949942f2f1161e0e3a7ee0b98439732a7a6`  
		Last Modified: Tue, 17 Dec 2024 19:28:25 GMT  
		Size: 14.4 KB (14389 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; s390x

```console
$ docker pull nats@sha256:231606d59bf67bf0225b8ff9322391ff528761f9e0417de1607425d5afd4adae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9686596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ab6034672329d984598a6d355339e336c65909875e48379c20c3a8492d5243e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1426b7374b29c0dcb926cdf54914b6a90fcca6f795e94ecee6d05578db18dea`  
		Last Modified: Tue, 17 Dec 2024 19:29:54 GMT  
		Size: 6.2 MB (6216106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a8d5d73de329406149614539003981ece64c24f00a8063d0218ff3b79b4fdd`  
		Last Modified: Tue, 17 Dec 2024 19:29:54 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b700a203382b44c168db5158adc0136d31b657f61a768de50ce397725977f302`  
		Last Modified: Tue, 17 Dec 2024 19:29:54 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:9cb0f384d223b0fb893a8e6883d30cdc52d031457d2466c639299a197a71b02d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb032d67922303b6505eaeb4c3a2e1e93ce05ce4ac7358439ea0f5eda3f19cb6`

```dockerfile
```

-	Layers:
	-	`sha256:8dfd4b0613d89e1631f9a0b566c194348623859b7aab6010157dfa1a5ef47147`  
		Last Modified: Tue, 17 Dec 2024 19:29:54 GMT  
		Size: 14.3 KB (14321 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:alpine3.21`

```console
$ docker pull nats@sha256:ab1de7a4552e1aa8676fad12ef36415434dcb0f5e1a8f4bd98c1c0b0e23c3108
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
$ docker pull nats@sha256:29cae9fbb27a68c8d042585d900cfe6c6a0687be3fc48e3749907266646626f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10017369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:575ec7872076c7f2ef48a2565b99ac2557abe519a55646c520a6280dda578672`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ee010a6f8d65980fb2a10e8ed490ac5deeb2c57778398caaff2dd317814317`  
		Last Modified: Tue, 17 Dec 2024 19:28:31 GMT  
		Size: 6.4 MB (6371955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e4e90f8624a081c4f8b6390a205113fb3d4efb52df8b8c4c109f3cbb45e0d7`  
		Last Modified: Tue, 17 Dec 2024 19:28:31 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17488456929723e351ddeda9e989781d4d3524c497aac4a9f4986b0a3bab4945`  
		Last Modified: Tue, 17 Dec 2024 19:28:31 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:cfdf92514ba877de3aba717f98d14ddce733bbffb44c334f902dea9147d674fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1c24142e5eed2c70f10105cdb7898204d5e69436be032d28f67396ed116411e`

```dockerfile
```

-	Layers:
	-	`sha256:e27f4eb3a71bf3ac9a8a6b932556310d82674abcc3248ab6d039babb897b959a`  
		Last Modified: Tue, 17 Dec 2024 19:28:31 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:2d66dc5023cd20e375636ada663a151dc2cf1f1b81366b1be5734dfef827d758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9386302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff9ef91ef8059e02d14a92ff39f20c50ea1a73599f50d8896f1f6df2d1381e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af40215e42d92bd72970c881af08ff0be57978182c0ffc369a75fa63356a3ca8`  
		Last Modified: Tue, 17 Dec 2024 19:29:36 GMT  
		Size: 6.0 MB (6018149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a327f5c4e15af30fe773e5bccc7b9078fd582fa78f7b5fd0d7b2506ec3b4086`  
		Last Modified: Tue, 17 Dec 2024 19:29:35 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8cb23494fbc6a634aa201b70ba71a79f6de1cace9996ea9b672757cf7bca461`  
		Last Modified: Tue, 17 Dec 2024 19:29:35 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:8b64eedc6a198a946e7e91844bdd9f74180c28ccc096147695e88e4e6cf87ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ad27d08cd2faace9930eb98b50cc3e27beddd7c101b0d33c4e03535c60ad2a`

```dockerfile
```

-	Layers:
	-	`sha256:1116a69deb5d903c668d4d739424c27736d4b250ac54f43eb4429c6a19165b7e`  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:9e84106ad88ced73c824cadca62f7e96f3015b20deba910b2e0b55189cc6f173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9107614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69dffc7badcd9eba6823886d65acbb0cfa112f8883783d134dc809e90b98f145`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc51158f73d5719731f6de6d6d24db0e1d4124a5ecd84bab5548388db0eded5a`  
		Last Modified: Tue, 17 Dec 2024 19:29:01 GMT  
		Size: 6.0 MB (6006607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c2203fb8a3575ff778e4d6965d233a19dd24a5bc90771ecca824833e155b06`  
		Last Modified: Tue, 17 Dec 2024 19:29:00 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacb2912b87b4350617243e5835a14b89a4006eb352e2e093b0b93284d61e070`  
		Last Modified: Tue, 17 Dec 2024 19:29:00 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:130347efdbef62b178c834dc5fda8f86a80bc17ee5ed4761825f0d10763932a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25422fc7bc14c1b14b45b22f895a7d64d49eb334e7564262dc1c10e8eca6abf9`

```dockerfile
```

-	Layers:
	-	`sha256:eb58607b3135d344e5e98c1c7130894a0412f1c8d219ba16ccfd1b8aaf8946cf`  
		Last Modified: Tue, 17 Dec 2024 19:29:00 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:91b0e0ed22e13b4b240286a274219ad0b7bef2ab2e5b9cfd4152e5c9c4ad246e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9912392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b9a70b84b2c7628f856d55590dc824bba274042faf6521e6dcecebf44b480f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d311607882428389c8bbb10058ff9f4a07c6714b605f6bd92afa58faf53ccf1`  
		Last Modified: Tue, 17 Dec 2024 19:29:19 GMT  
		Size: 5.9 MB (5918236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:120d4d49d4ce04dd2b71e71ea3c19191133df462671d15362ec224b0c7a6b329`  
		Last Modified: Tue, 17 Dec 2024 19:29:19 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2348ec882817d42d419fca6d6073f5980a4808bea9d36c67cc612d20f656a0c`  
		Last Modified: Tue, 17 Dec 2024 19:29:19 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:2bcdf7d278748efd5f3c41ad5a847840ecabae85a7f38d8bd2eab34f5d925562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51691faecee58ef8255c969e6e92d7f2119288caa70eb618072608de605727bf`

```dockerfile
```

-	Layers:
	-	`sha256:4ecc6db36ffe92c81d7ea0b122f98496f5b6cc7de311e1f92f29189a5e94477f`  
		Last Modified: Tue, 17 Dec 2024 19:29:19 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:3449804a92d7c624c6e5bbc48d29d3c785046de22627a6c4f25962e2f45affee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9464345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:526d9d5508e133079e9f97028d93c63cb13fd416f25a11fad5808f052ab50812`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-ppc64le.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:a12ff663c50b78339bd273940ba035e29d8220954846a4c35a5f79080b37a3d3`  
		Last Modified: Thu, 05 Dec 2024 22:18:21 GMT  
		Size: 3.6 MB (3577108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:672eaefb89f5c4c03dc1dfd0e81f2f3ad81e138d028b4087f87cd3ee9958423d`  
		Last Modified: Tue, 17 Dec 2024 19:28:25 GMT  
		Size: 5.9 MB (5886266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f573fb4c0caa43a456c5b6e69b41c587ceb460ed049cbbe6b7689f71878eb94b`  
		Last Modified: Tue, 17 Dec 2024 19:28:25 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6435cc906fd110b2082eb0900e048df12cb9ea784fd2c023d2802fb66bac5a46`  
		Last Modified: Tue, 17 Dec 2024 19:28:25 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:160f40bbb801fb82f584f14f06735d924e6e69fd6c2fc93acdeacf87846b7cfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159b7defb72e6a0f49e1e548aa2c7df4ee6b842169a267dd9652a7c0f0d338e0`

```dockerfile
```

-	Layers:
	-	`sha256:983eda21d01dd67d3a7bdb35b440c949942f2f1161e0e3a7ee0b98439732a7a6`  
		Last Modified: Tue, 17 Dec 2024 19:28:25 GMT  
		Size: 14.4 KB (14389 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:231606d59bf67bf0225b8ff9322391ff528761f9e0417de1607425d5afd4adae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9686596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ab6034672329d984598a6d355339e336c65909875e48379c20c3a8492d5243e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1426b7374b29c0dcb926cdf54914b6a90fcca6f795e94ecee6d05578db18dea`  
		Last Modified: Tue, 17 Dec 2024 19:29:54 GMT  
		Size: 6.2 MB (6216106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a8d5d73de329406149614539003981ece64c24f00a8063d0218ff3b79b4fdd`  
		Last Modified: Tue, 17 Dec 2024 19:29:54 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b700a203382b44c168db5158adc0136d31b657f61a768de50ce397725977f302`  
		Last Modified: Tue, 17 Dec 2024 19:29:54 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:9cb0f384d223b0fb893a8e6883d30cdc52d031457d2466c639299a197a71b02d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb032d67922303b6505eaeb4c3a2e1e93ce05ce4ac7358439ea0f5eda3f19cb6`

```dockerfile
```

-	Layers:
	-	`sha256:8dfd4b0613d89e1631f9a0b566c194348623859b7aab6010157dfa1a5ef47147`  
		Last Modified: Tue, 17 Dec 2024 19:29:54 GMT  
		Size: 14.3 KB (14321 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:latest`

```console
$ docker pull nats@sha256:d4c302ac4a0d84afff801c413f7f32e9e76505030d020b988605a3e839cbcd95
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
$ docker pull nats@sha256:67d3b85ece6c782cf7ead3ecb3a1ac84ea0f1a90692e49699e78cbded1b303f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5905656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30790e9a65a19f582b2ef7ef953584341edfe5d6fa4e0ca626c151bd29d42300`
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
		Size: 5.9 MB (5905148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8de2329765d2e9e6ad2eef24244fb693d2372ce8561eee2d04a4b15613d4957`  
		Last Modified: Tue, 17 Dec 2024 20:07:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:bf98881f063cf871ca1790de74f2e754f9d790b3db90451f6b5da630335ca9fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b933f94df98aa627cb8bf50b2acae5ed54c95244c49afe60cd9b9504d44c4dc8`

```dockerfile
```

-	Layers:
	-	`sha256:021e7dd96b286525c844698e284fea042a82a034acb1e22fe017dd14f20618a5`  
		Last Modified: Tue, 17 Dec 2024 20:07:46 GMT  
		Size: 10.5 KB (10473 bytes)  
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
$ docker pull nats@sha256:25129eb990a4dd587a984e2e2f97ef3492dc391a45119430a8a33cee51dfa7b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5418850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cf4789450fb70da1d11cc8480fe7fc5895888d5dec9b2f39fc4363a18f5e15e`
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
	-	`sha256:2154049e56fd256d2148c4e2e139e5269047c2bb399664b65fce45bbe9852ba6`  
		Last Modified: Tue, 17 Dec 2024 20:07:27 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:01db48579033a378b0e612214b5ca3906a4b332620348ae699697ca38929b3a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76ff46f64e472e71663b6e392cfa2b372b0a27346ae2de8ea608dd2f8e307c31`

```dockerfile
```

-	Layers:
	-	`sha256:74364e5c7720e83ad343b975d9a65bb9ca7f9689948c422c502889ae59651691`  
		Last Modified: Tue, 17 Dec 2024 20:07:27 GMT  
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
$ docker pull nats@sha256:d5cf5fddd6246b37ee3acb3b67903298c21827c1862cd95d0d9f282794c82190
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
$ docker pull nats@sha256:67d3b85ece6c782cf7ead3ecb3a1ac84ea0f1a90692e49699e78cbded1b303f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5905656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30790e9a65a19f582b2ef7ef953584341edfe5d6fa4e0ca626c151bd29d42300`
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
		Size: 5.9 MB (5905148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8de2329765d2e9e6ad2eef24244fb693d2372ce8561eee2d04a4b15613d4957`  
		Last Modified: Tue, 17 Dec 2024 20:07:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:bf98881f063cf871ca1790de74f2e754f9d790b3db90451f6b5da630335ca9fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b933f94df98aa627cb8bf50b2acae5ed54c95244c49afe60cd9b9504d44c4dc8`

```dockerfile
```

-	Layers:
	-	`sha256:021e7dd96b286525c844698e284fea042a82a034acb1e22fe017dd14f20618a5`  
		Last Modified: Tue, 17 Dec 2024 20:07:46 GMT  
		Size: 10.5 KB (10473 bytes)  
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
$ docker pull nats@sha256:25129eb990a4dd587a984e2e2f97ef3492dc391a45119430a8a33cee51dfa7b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5418850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cf4789450fb70da1d11cc8480fe7fc5895888d5dec9b2f39fc4363a18f5e15e`
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
	-	`sha256:2154049e56fd256d2148c4e2e139e5269047c2bb399664b65fce45bbe9852ba6`  
		Last Modified: Tue, 17 Dec 2024 20:07:27 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:01db48579033a378b0e612214b5ca3906a4b332620348ae699697ca38929b3a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76ff46f64e472e71663b6e392cfa2b372b0a27346ae2de8ea608dd2f8e307c31`

```dockerfile
```

-	Layers:
	-	`sha256:74364e5c7720e83ad343b975d9a65bb9ca7f9689948c422c502889ae59651691`  
		Last Modified: Tue, 17 Dec 2024 20:07:27 GMT  
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
$ docker pull nats@sha256:d5cf5fddd6246b37ee3acb3b67903298c21827c1862cd95d0d9f282794c82190
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
$ docker pull nats@sha256:67d3b85ece6c782cf7ead3ecb3a1ac84ea0f1a90692e49699e78cbded1b303f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5905656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30790e9a65a19f582b2ef7ef953584341edfe5d6fa4e0ca626c151bd29d42300`
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
		Size: 5.9 MB (5905148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8de2329765d2e9e6ad2eef24244fb693d2372ce8561eee2d04a4b15613d4957`  
		Last Modified: Tue, 17 Dec 2024 20:07:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:bf98881f063cf871ca1790de74f2e754f9d790b3db90451f6b5da630335ca9fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b933f94df98aa627cb8bf50b2acae5ed54c95244c49afe60cd9b9504d44c4dc8`

```dockerfile
```

-	Layers:
	-	`sha256:021e7dd96b286525c844698e284fea042a82a034acb1e22fe017dd14f20618a5`  
		Last Modified: Tue, 17 Dec 2024 20:07:46 GMT  
		Size: 10.5 KB (10473 bytes)  
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
$ docker pull nats@sha256:25129eb990a4dd587a984e2e2f97ef3492dc391a45119430a8a33cee51dfa7b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5418850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cf4789450fb70da1d11cc8480fe7fc5895888d5dec9b2f39fc4363a18f5e15e`
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
	-	`sha256:2154049e56fd256d2148c4e2e139e5269047c2bb399664b65fce45bbe9852ba6`  
		Last Modified: Tue, 17 Dec 2024 20:07:27 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:01db48579033a378b0e612214b5ca3906a4b332620348ae699697ca38929b3a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76ff46f64e472e71663b6e392cfa2b372b0a27346ae2de8ea608dd2f8e307c31`

```dockerfile
```

-	Layers:
	-	`sha256:74364e5c7720e83ad343b975d9a65bb9ca7f9689948c422c502889ae59651691`  
		Last Modified: Tue, 17 Dec 2024 20:07:27 GMT  
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
