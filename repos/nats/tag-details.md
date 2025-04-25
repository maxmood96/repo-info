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
-	[`nats:2.10.28`](#nats21028)
-	[`nats:2.10.28-alpine`](#nats21028-alpine)
-	[`nats:2.10.28-alpine3.21`](#nats21028-alpine321)
-	[`nats:2.10.28-linux`](#nats21028-linux)
-	[`nats:2.10.28-nanoserver`](#nats21028-nanoserver)
-	[`nats:2.10.28-nanoserver-1809`](#nats21028-nanoserver-1809)
-	[`nats:2.10.28-scratch`](#nats21028-scratch)
-	[`nats:2.10.28-windowsservercore`](#nats21028-windowsservercore)
-	[`nats:2.10.28-windowsservercore-1809`](#nats21028-windowsservercore-1809)
-	[`nats:2.11`](#nats211)
-	[`nats:2.11-alpine`](#nats211-alpine)
-	[`nats:2.11-alpine3.21`](#nats211-alpine321)
-	[`nats:2.11-linux`](#nats211-linux)
-	[`nats:2.11-nanoserver`](#nats211-nanoserver)
-	[`nats:2.11-nanoserver-1809`](#nats211-nanoserver-1809)
-	[`nats:2.11-scratch`](#nats211-scratch)
-	[`nats:2.11-windowsservercore`](#nats211-windowsservercore)
-	[`nats:2.11-windowsservercore-1809`](#nats211-windowsservercore-1809)
-	[`nats:2.11.2`](#nats2112)
-	[`nats:2.11.2-alpine`](#nats2112-alpine)
-	[`nats:2.11.2-alpine3.21`](#nats2112-alpine321)
-	[`nats:2.11.2-linux`](#nats2112-linux)
-	[`nats:2.11.2-nanoserver`](#nats2112-nanoserver)
-	[`nats:2.11.2-nanoserver-1809`](#nats2112-nanoserver-1809)
-	[`nats:2.11.2-scratch`](#nats2112-scratch)
-	[`nats:2.11.2-windowsservercore`](#nats2112-windowsservercore)
-	[`nats:2.11.2-windowsservercore-1809`](#nats2112-windowsservercore-1809)
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
$ docker pull nats@sha256:29ae7f55fbaa9d23949237c58593a3451ef74493e5b3644d6a837219d1d4028c
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
	-	windows version 10.0.17763.7249; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:41dddbc7a9265892086db802a374dbf910b5d0db786c8ba12e27a81f2ede8f05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6282680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ddda49ccc5be8fc53872fcb74f0f168368af1d3e5fc27fd096bb4ab9fac9e5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7a31ab99389a11bb36db183df5a6bc8d784c1e96fb10c1973e04b98e17e58f51`  
		Last Modified: Tue, 08 Apr 2025 17:26:21 GMT  
		Size: 6.3 MB (6282171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bcd18a1de501f0dcf00113b8c1effd2b7f198a1383c537490e8dce3a826adce`  
		Last Modified: Tue, 08 Apr 2025 21:07:44 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:16692b029d2fd73a6c9833d59190a10a052903fbc5b68228ca0ce31e25895ee4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a60659f991d784a3586e62308c55e27054bad66d740cbde49980328b682cb858`

```dockerfile
```

-	Layers:
	-	`sha256:d0fd9d7883ec1e99c1a17109b0a6fd39dec7b9ec8f40f0ace2f2c15f9d8846a3`  
		Last Modified: Tue, 08 Apr 2025 21:07:45 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:f53994879dbfd2fc8177b383905d33db1095d8b42bb4bec64088771cecdb2bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6002072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01de3b3fb48e4b75539a9af5640e6f77115cdbe9419f3da2891472ec6e806148`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bc9bfb085b797367e9407dbdf5a3928ee0d69859fb96188165856b5e8e1b6e88`  
		Last Modified: Tue, 08 Apr 2025 17:26:22 GMT  
		Size: 6.0 MB (6001563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef30b0264d904d40fbf4763922653522d80a800c24f6bcbb52a1a66fd1accaf8`  
		Last Modified: Tue, 08 Apr 2025 21:07:08 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:f9537be10194b98f78298fad26add4a04948857f650479e674587da738dcf69c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7014bcdaac4c9653a29f6fc739854477633a62a69bd0cba053bbeecbfc57e101`

```dockerfile
```

-	Layers:
	-	`sha256:e337d587115a4b810f5a9fa3deb1db109744f3828488f355e6bfa4c965ea5501`  
		Last Modified: Tue, 08 Apr 2025 21:07:08 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:859b07690a2059b52277aceb9feed7e81269aed09859f1c3b0f3162d751ddb29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5992346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e38aded7ecfd1e1b61cc0452d01e01718e0a4be4ee666ac1980ddacb6f7defbc`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8f114aa547686a4604d8f5fbabd3d89b59a801cc55b68aa653d813c66ca32a65`  
		Last Modified: Tue, 08 Apr 2025 17:26:18 GMT  
		Size: 6.0 MB (5991835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844018e59249593be5d829b3a4bba323e96c26297db204b3a8a8a52e847f8041`  
		Last Modified: Tue, 08 Apr 2025 21:25:07 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:1e53207f824b4b97a2158a01c60662ef62ff32a777e55e615077563d48bcc314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a229febf9f435367bc3df4661afe24971b0581fa0b4b375a92d4ac38c3ce791`

```dockerfile
```

-	Layers:
	-	`sha256:36f6e0df21021319068725c9d7c2325e4fad06927e5ff9fe7fe11ec830f17f1c`  
		Last Modified: Tue, 08 Apr 2025 21:25:06 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:9142b78e748793c9e3b2fda3ac3800e66e866bf0147d634a7aea592f973a023a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5776867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee76a21b5d66ec40c0c8c53a6af4ed91124f7a2820ab80bf20279efdc3e689c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6b90b986da10be1b936fe6989055b49edb315427df0ceb03d1dd2f9dd98fb88`  
		Last Modified: Tue, 08 Apr 2025 17:26:18 GMT  
		Size: 5.8 MB (5776357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5e46c8b1d8619650c3d1afbfcf70b02949ce40d6fd6eb7d769bdc98a1def25`  
		Last Modified: Wed, 09 Apr 2025 00:53:02 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:9f289daca75844d624973e2b4e4a78db9e2026bfd59d743648f68e3c13d32a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53971055b1ebeea168a941b88f41f089dd9886aa55cbebe6b4f12f98ddb49666`

```dockerfile
```

-	Layers:
	-	`sha256:a65f769c9cecfc76c232cf377b8548ffd7fc82eae67b781487e0924b3319a183`  
		Last Modified: Wed, 09 Apr 2025 00:53:02 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; ppc64le

```console
$ docker pull nats@sha256:8cbd8caa2bdb9c64319ae113af4cf4170b92f3795148cb20401f2f1f16aa1d11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5757631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ba2ae7e87afe027065399c01f1230c431bed76a811a5cc5c83e971b6e70a26`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2c03c8b47070105a3781cfd93e5a048f0fcf1895182b8500a1875b914beccc2b`  
		Last Modified: Tue, 08 Apr 2025 17:26:19 GMT  
		Size: 5.8 MB (5757122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425937f6cd03177f214b970352644a3316a1a6ac085099e96875d62e6eb6b95d`  
		Last Modified: Tue, 08 Apr 2025 22:18:51 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:5aa97ff134b80e48aaa63c71d9c8343062cb648de6445e6d078b62dab5b08a3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8af43893a1163e246e9f97ae6b6ca899d5147c74db410070388f3dc6b1bb9a`

```dockerfile
```

-	Layers:
	-	`sha256:b2dde84b1c72b35f921945f0d6bec4b01ff2c811e34deff66dc5a99577731ade`  
		Last Modified: Tue, 08 Apr 2025 22:18:51 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; s390x

```console
$ docker pull nats@sha256:24602554caa826a00e26b3dae9c589026eaab3e0ad8e59cb573cac3996e62f8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6122577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7976c47bfec0473931b30ef2753bdc1cefde06b7a03f869cabb36b78aee6fd30`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:096b0701966ee2a29da8fc2c3f8ad25d2a0bb1211425d296e92558196ebe09c9`  
		Last Modified: Tue, 08 Apr 2025 17:26:22 GMT  
		Size: 6.1 MB (6122069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50402e49c7c832b57fb874a3e012194a27d09597f2d39ddc97db3701ae5bfb7`  
		Last Modified: Tue, 08 Apr 2025 22:07:44 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:6f2d2b491eee799540891efc47f6f00293192e82097e7b80bb5fd571bbf312c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8736b1c1aaa3dce6b14a6b7b5cad1d5cc142fae7d7d9fd17b8a6d72e67a82268`

```dockerfile
```

-	Layers:
	-	`sha256:1ab1e3d26d57dec0dbbe6b34b8c0c23c6308ed6e3e58b9267695ff2247985c40`  
		Last Modified: Tue, 08 Apr 2025 22:07:44 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - windows version 10.0.17763.7249; amd64

```console
$ docker pull nats@sha256:70dfa0a823409d278307a2f602a989bb5088fc2ed408add1628e7026065e4f7f
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.2 MB (115214035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c10544dab15e09a82ee58dfe65c5cebe6e37634a0fc0e40720019d69e49ec056`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Fri, 18 Apr 2025 04:11:39 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 18 Apr 2025 04:11:40 GMT
RUN cmd /S /C #(nop) COPY file:eee3870bfbcd9bfddd3622d20a6c2075b583b61ab0944602ceefed02dee11aa2 in C:\nats-server.exe 
# Fri, 18 Apr 2025 04:11:41 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Fri, 18 Apr 2025 04:11:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 18 Apr 2025 04:11:42 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 18 Apr 2025 04:11:42 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5dab9cfa2f7ef2b19e95e68d27e3d0b208d9016da1b04298c500e78281a15e7`  
		Last Modified: Fri, 18 Apr 2025 04:11:48 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d0b032347a8dcb65e359d04c00733934bf6cfe61db4b1142a1df5f3de23a9cc`  
		Last Modified: Fri, 18 Apr 2025 04:11:47 GMT  
		Size: 6.5 MB (6455931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497b3350d5c31834bcca73478d5fc7c0d3c546c1676c042e1e9d1ec9afc85bdd`  
		Last Modified: Fri, 18 Apr 2025 04:11:46 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658de08330e9b739dfbff680b38b2bb55dc4b4aec6d4064b19ecc24c7ba9a8aa`  
		Last Modified: Fri, 18 Apr 2025 04:11:46 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0312f657691b722f56e7ed6bc33b2119988f7f21d9853fe0a8dcc79a3b5aec`  
		Last Modified: Fri, 18 Apr 2025 04:11:46 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fc9ae19d64bc742bb97a1eec58e04de0d2eab1eb71186876fed513a4b21a3d`  
		Last Modified: Fri, 18 Apr 2025 04:11:46 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:a6e0002b6027b9f64619750d8d2d535c54fe247b54050959be29bb69e6b0d1f1
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
$ docker pull nats@sha256:7cbd5f7f5326233bf97e186073144217f7b98b8cf904d0d83ba9ff08caf6f0d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10386082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a900eac76440acf8f75c33c7a37e9103f53d792b082074036e8ee5a2df6903ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
ENV NATS_SERVER=2.11.1
# Tue, 08 Apr 2025 17:23:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='27c90d8bc0ad10bfb38ef92bdea8528b4bfc5aa56afba91c790fb3921ea205a2' ;; 		armhf) natsArch='arm6'; sha256='8f9f2f4aa85c242f254a175c9455e9d00c6a0e7fc96b87a14ef3bd6d8762e900' ;; 		armv7) natsArch='arm7'; sha256='06dee81c2fd32639ae646112daaf9b84b71023bee88b16fd3324fd922095dda1' ;; 		x86_64) natsArch='amd64'; sha256='f1d9754bf34316d1f7d349b176ff0414c9cce742846bf2eec0b402eee35a638c' ;; 		x86) natsArch='386'; sha256='b746e832f96f07ee5958c99201b7a96695a3e1339f416342b9fd3c083a68dba7' ;; 		s390x) natsArch='s390x'; sha256='018ec95e10758c3e6ea14f034d3fe099234957dec8290bc5aa3480a8d77e3e29' ;; 		ppc64le) natsArch='ppc64le'; sha256='be0f9308ffcdfa36189afdf7e8116235995d7d20406c0fc7b8aa5b5f724aa3d6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bffd47baa898ba4523ccc09b26058ea27891e234ee7563e763b8f9bd29bde2e`  
		Last Modified: Tue, 08 Apr 2025 20:28:15 GMT  
		Size: 6.7 MB (6742867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63af34edcf916551729eef83c51841b9403e9bedf717838e0dedfe7e5bfa977b`  
		Last Modified: Tue, 08 Apr 2025 20:28:15 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9081de8dcbbc97f988fe2e6b0695f7eaea0f8774966c467ed29bd8602391ff9`  
		Last Modified: Tue, 08 Apr 2025 20:28:14 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:062f6b7155ed98648412670dffe43c7be1f4768f50bfa3fa63ba59b794ec300c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b2af7e3b213deee44fd319c5441ec699c53280a665cf650e9eec87b50af831`

```dockerfile
```

-	Layers:
	-	`sha256:df59247835527b1024e29a039c6dd53ac255e4500ded522b5e05635e9495a453`  
		Last Modified: Tue, 08 Apr 2025 20:28:15 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:b25ce7d7cfb629d1a132ae08b8fd84da4ab34c224fc57a9366f4f7e8284a89b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9849553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5bc00749e465a4c423af0395ea8a620f5184198a26aa70c550afb018dcd620d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da0a4b9d57d2a4c2439f0c8731b7e1ef8f0a7f2a1edf643d5f50a73ffc0c31f9' ;; 		armhf) natsArch='arm6'; sha256='2370e8d794acb0f176be0f0885f9930fa9d8d1276f15162eb8db336467279bc1' ;; 		armv7) natsArch='arm7'; sha256='46b038e57ad586f05342dcd3b29a2c2597217c19172a916eef9187170f024ad8' ;; 		x86_64) natsArch='amd64'; sha256='a123c8e43abe5ca8f0bff9393547f20f4bbac6fc0fb3c586ec031855911c414a' ;; 		x86) natsArch='386'; sha256='03bf7db9323c453b1257c3a43a21fcd5a975a2cc136c4bbeab7c0e815939e37e' ;; 		s390x) natsArch='s390x'; sha256='eb40e4a843124198b7e8625b7cccbd52810d63db17e1557d59681f5f29be5a98' ;; 		ppc64le) natsArch='ppc64le'; sha256='28e2afbca41dffe453507a993291560bfc57c6f43fe435604f894c3d91426dd0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53314fd665bd0c97ace20b7fb2ca1b46ecfdd7426150f8745639bb7704613d5a`  
		Last Modified: Fri, 25 Apr 2025 17:47:34 GMT  
		Size: 6.5 MB (6483851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cefa71e52d2f6e7b13aac0c8fe523facca0507ac8e8b180b168eeadfd046b89`  
		Last Modified: Fri, 25 Apr 2025 17:47:33 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c198696667425fcef5f606fda093ce31277d14ed9b5dc1592fb47511143d5052`  
		Last Modified: Fri, 25 Apr 2025 17:47:33 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:20a327f5442b5e1a069fb161658d8b9436e0f0ce2df3802ad9d74362036c2210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b2f873973386278768ee962ed71409b2376682ae823894072e19be8cde68680`

```dockerfile
```

-	Layers:
	-	`sha256:9122357572edf020a23a1bbf0fbe37650762d41d728dfaccb594f7e5890cbd2d`  
		Last Modified: Fri, 25 Apr 2025 17:47:33 GMT  
		Size: 14.4 KB (14424 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:2f0c0883a1c8a7dd3a93730ce2ca646928c272aba42b05b5d163f5e779696f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9552050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28191bc799228c242ab1ebf65c8eaa89c320b25a78ee799103e544b8250226d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
ENV NATS_SERVER=2.11.1
# Tue, 08 Apr 2025 17:23:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='27c90d8bc0ad10bfb38ef92bdea8528b4bfc5aa56afba91c790fb3921ea205a2' ;; 		armhf) natsArch='arm6'; sha256='8f9f2f4aa85c242f254a175c9455e9d00c6a0e7fc96b87a14ef3bd6d8762e900' ;; 		armv7) natsArch='arm7'; sha256='06dee81c2fd32639ae646112daaf9b84b71023bee88b16fd3324fd922095dda1' ;; 		x86_64) natsArch='amd64'; sha256='f1d9754bf34316d1f7d349b176ff0414c9cce742846bf2eec0b402eee35a638c' ;; 		x86) natsArch='386'; sha256='b746e832f96f07ee5958c99201b7a96695a3e1339f416342b9fd3c083a68dba7' ;; 		s390x) natsArch='s390x'; sha256='018ec95e10758c3e6ea14f034d3fe099234957dec8290bc5aa3480a8d77e3e29' ;; 		ppc64le) natsArch='ppc64le'; sha256='be0f9308ffcdfa36189afdf7e8116235995d7d20406c0fc7b8aa5b5f724aa3d6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b82717f71af9d7a4242a00c3efbdf445cc5b3122fb74530e7d5e2971036151`  
		Last Modified: Tue, 08 Apr 2025 20:32:08 GMT  
		Size: 6.5 MB (6452958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49791283070c29e615bbe60ca9b43f0b5c63e67560f09700c02a4920fc31499`  
		Last Modified: Tue, 08 Apr 2025 20:32:07 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ade19b2805065881eeef7b4e282331a2f7fbd91f70c6349b33b2d448e8dc64`  
		Last Modified: Tue, 08 Apr 2025 20:32:07 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:f66e974c49c5b42df6f26cfe23be843bed87adb4df5efde68922bcd9bcdb0654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45fd3c0542a49a774cbfafb32d74dcb38bb7230e53a346c90ea2dc92652e671d`

```dockerfile
```

-	Layers:
	-	`sha256:dafec31d0d294d05c575a7f27247bd7720e66c489584ce418ed700595bb00c9f`  
		Last Modified: Tue, 08 Apr 2025 20:32:07 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:4fe60f222966727f3e81dbb3bf2aaec58c7c8b573afbe318f6cb2c70c19f37c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10254225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5d5d918ca9a0f7dd7c056851f2898f207c48f854da7954fc8fafc8fd1aa3021`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da0a4b9d57d2a4c2439f0c8731b7e1ef8f0a7f2a1edf643d5f50a73ffc0c31f9' ;; 		armhf) natsArch='arm6'; sha256='2370e8d794acb0f176be0f0885f9930fa9d8d1276f15162eb8db336467279bc1' ;; 		armv7) natsArch='arm7'; sha256='46b038e57ad586f05342dcd3b29a2c2597217c19172a916eef9187170f024ad8' ;; 		x86_64) natsArch='amd64'; sha256='a123c8e43abe5ca8f0bff9393547f20f4bbac6fc0fb3c586ec031855911c414a' ;; 		x86) natsArch='386'; sha256='03bf7db9323c453b1257c3a43a21fcd5a975a2cc136c4bbeab7c0e815939e37e' ;; 		s390x) natsArch='s390x'; sha256='eb40e4a843124198b7e8625b7cccbd52810d63db17e1557d59681f5f29be5a98' ;; 		ppc64le) natsArch='ppc64le'; sha256='28e2afbca41dffe453507a993291560bfc57c6f43fe435604f894c3d91426dd0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3febb0921652e8042f634bdcb7812f9a2ed40e073970e14a940960350b775dbf`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 6.3 MB (6260226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc226874bc3060e6e916fa3ef948812c54a012b6081a27eaab55addfec8b7473`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e367a33259d9c5e7a6a6b42c8482e8bc6930e1a713671c0cf2fd1b5c879eef01`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:fda84d5581ce64cec49def3b469b26e717bf64d28a817656b19e16da89e9ea25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a714d7bd3b6fd55a075f56b50fa0da44cf6616089161edf7a648ba47af3256`

```dockerfile
```

-	Layers:
	-	`sha256:5f55a5edc5478bd7d7c9bc7e0763ad4dee93ecffafd3ed2f7702e7ee06ae75b0`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 14.5 KB (14469 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:6b6b1109a98eafc180bae27e0e27a1110433dfd3577e78cac2d8eb793969fc43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9797332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52bb4f9d9231f9b6c625e4a3a3f2874bd83248ad61158f697eb327444118f598`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
ENV NATS_SERVER=2.11.1
# Tue, 08 Apr 2025 17:23:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='27c90d8bc0ad10bfb38ef92bdea8528b4bfc5aa56afba91c790fb3921ea205a2' ;; 		armhf) natsArch='arm6'; sha256='8f9f2f4aa85c242f254a175c9455e9d00c6a0e7fc96b87a14ef3bd6d8762e900' ;; 		armv7) natsArch='arm7'; sha256='06dee81c2fd32639ae646112daaf9b84b71023bee88b16fd3324fd922095dda1' ;; 		x86_64) natsArch='amd64'; sha256='f1d9754bf34316d1f7d349b176ff0414c9cce742846bf2eec0b402eee35a638c' ;; 		x86) natsArch='386'; sha256='b746e832f96f07ee5958c99201b7a96695a3e1339f416342b9fd3c083a68dba7' ;; 		s390x) natsArch='s390x'; sha256='018ec95e10758c3e6ea14f034d3fe099234957dec8290bc5aa3480a8d77e3e29' ;; 		ppc64le) natsArch='ppc64le'; sha256='be0f9308ffcdfa36189afdf7e8116235995d7d20406c0fc7b8aa5b5f724aa3d6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8be7344e3eed187cfb792f8b098e4b9639bd0e5318ceffb68a33a3bad2164c`  
		Last Modified: Tue, 08 Apr 2025 20:42:59 GMT  
		Size: 6.2 MB (6222020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd19bdb0c54b34703a3579dcae0cd27d09d0ed9ac711591a13fba04c9a89aacf`  
		Last Modified: Tue, 08 Apr 2025 20:42:58 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2608514a04b63ea4ad3654f5acd693a1bc97dc1d1c8b8a1495df0e53dda6ff0`  
		Last Modified: Tue, 08 Apr 2025 20:42:58 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:28f492787cca2adfb7bcfcb21be59f4685caad51e81ff81fac96d5d46445c776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ada670995406f8a9d5e52233a0003738fc8c1933710c4de448e87af34e5a3863`

```dockerfile
```

-	Layers:
	-	`sha256:e269226b323faa520a451de66e148284583959e77af2bf7d56a4d350cc37623a`  
		Last Modified: Tue, 08 Apr 2025 20:42:58 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; s390x

```console
$ docker pull nats@sha256:cf54ecfbde97d03a9d1a1bfdbcf069c2683ef48f34d72013b9064f5ed0ab9183
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10053959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f94c74252361e5594561679a5358b7e135dd9c7c2f3c51be0138903f04c6aa8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
ENV NATS_SERVER=2.11.1
# Tue, 08 Apr 2025 17:23:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='27c90d8bc0ad10bfb38ef92bdea8528b4bfc5aa56afba91c790fb3921ea205a2' ;; 		armhf) natsArch='arm6'; sha256='8f9f2f4aa85c242f254a175c9455e9d00c6a0e7fc96b87a14ef3bd6d8762e900' ;; 		armv7) natsArch='arm7'; sha256='06dee81c2fd32639ae646112daaf9b84b71023bee88b16fd3324fd922095dda1' ;; 		x86_64) natsArch='amd64'; sha256='f1d9754bf34316d1f7d349b176ff0414c9cce742846bf2eec0b402eee35a638c' ;; 		x86) natsArch='386'; sha256='b746e832f96f07ee5958c99201b7a96695a3e1339f416342b9fd3c083a68dba7' ;; 		s390x) natsArch='s390x'; sha256='018ec95e10758c3e6ea14f034d3fe099234957dec8290bc5aa3480a8d77e3e29' ;; 		ppc64le) natsArch='ppc64le'; sha256='be0f9308ffcdfa36189afdf7e8116235995d7d20406c0fc7b8aa5b5f724aa3d6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a92fbe14b2cdd6c1a85f89f171cfbad87c0f00fc6205b2d6c5cfa29cf51cf30`  
		Last Modified: Tue, 08 Apr 2025 22:04:28 GMT  
		Size: 6.6 MB (6585420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc913d6647309b3286a51c5f87c54edfb961dd53b9ca8a4496335154e303ab2e`  
		Last Modified: Tue, 08 Apr 2025 22:04:28 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22b8967d9a9d213c271cc67dcbe1d89b5b0870a2d2a399344c51f7cdc25b2c7`  
		Last Modified: Tue, 08 Apr 2025 22:04:28 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:b55039b07dc68ae69425511e99ab099b60f707e9a565a17a0d28e21a33c1f346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4570b0028f776dbca1deaabac6952192f625b95ec93d8098c7058262a3ca4b9`

```dockerfile
```

-	Layers:
	-	`sha256:5b1859f0680f19779c89b10a96fe392f905b04060b6ca55b19696d4fc51ece7c`  
		Last Modified: Tue, 08 Apr 2025 22:04:28 GMT  
		Size: 14.3 KB (14316 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-alpine3.21`

```console
$ docker pull nats@sha256:a6e0002b6027b9f64619750d8d2d535c54fe247b54050959be29bb69e6b0d1f1
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
$ docker pull nats@sha256:7cbd5f7f5326233bf97e186073144217f7b98b8cf904d0d83ba9ff08caf6f0d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10386082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a900eac76440acf8f75c33c7a37e9103f53d792b082074036e8ee5a2df6903ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
ENV NATS_SERVER=2.11.1
# Tue, 08 Apr 2025 17:23:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='27c90d8bc0ad10bfb38ef92bdea8528b4bfc5aa56afba91c790fb3921ea205a2' ;; 		armhf) natsArch='arm6'; sha256='8f9f2f4aa85c242f254a175c9455e9d00c6a0e7fc96b87a14ef3bd6d8762e900' ;; 		armv7) natsArch='arm7'; sha256='06dee81c2fd32639ae646112daaf9b84b71023bee88b16fd3324fd922095dda1' ;; 		x86_64) natsArch='amd64'; sha256='f1d9754bf34316d1f7d349b176ff0414c9cce742846bf2eec0b402eee35a638c' ;; 		x86) natsArch='386'; sha256='b746e832f96f07ee5958c99201b7a96695a3e1339f416342b9fd3c083a68dba7' ;; 		s390x) natsArch='s390x'; sha256='018ec95e10758c3e6ea14f034d3fe099234957dec8290bc5aa3480a8d77e3e29' ;; 		ppc64le) natsArch='ppc64le'; sha256='be0f9308ffcdfa36189afdf7e8116235995d7d20406c0fc7b8aa5b5f724aa3d6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bffd47baa898ba4523ccc09b26058ea27891e234ee7563e763b8f9bd29bde2e`  
		Last Modified: Tue, 08 Apr 2025 20:28:15 GMT  
		Size: 6.7 MB (6742867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63af34edcf916551729eef83c51841b9403e9bedf717838e0dedfe7e5bfa977b`  
		Last Modified: Tue, 08 Apr 2025 20:28:15 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9081de8dcbbc97f988fe2e6b0695f7eaea0f8774966c467ed29bd8602391ff9`  
		Last Modified: Tue, 08 Apr 2025 20:28:14 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:062f6b7155ed98648412670dffe43c7be1f4768f50bfa3fa63ba59b794ec300c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b2af7e3b213deee44fd319c5441ec699c53280a665cf650e9eec87b50af831`

```dockerfile
```

-	Layers:
	-	`sha256:df59247835527b1024e29a039c6dd53ac255e4500ded522b5e05635e9495a453`  
		Last Modified: Tue, 08 Apr 2025 20:28:15 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:b25ce7d7cfb629d1a132ae08b8fd84da4ab34c224fc57a9366f4f7e8284a89b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9849553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5bc00749e465a4c423af0395ea8a620f5184198a26aa70c550afb018dcd620d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da0a4b9d57d2a4c2439f0c8731b7e1ef8f0a7f2a1edf643d5f50a73ffc0c31f9' ;; 		armhf) natsArch='arm6'; sha256='2370e8d794acb0f176be0f0885f9930fa9d8d1276f15162eb8db336467279bc1' ;; 		armv7) natsArch='arm7'; sha256='46b038e57ad586f05342dcd3b29a2c2597217c19172a916eef9187170f024ad8' ;; 		x86_64) natsArch='amd64'; sha256='a123c8e43abe5ca8f0bff9393547f20f4bbac6fc0fb3c586ec031855911c414a' ;; 		x86) natsArch='386'; sha256='03bf7db9323c453b1257c3a43a21fcd5a975a2cc136c4bbeab7c0e815939e37e' ;; 		s390x) natsArch='s390x'; sha256='eb40e4a843124198b7e8625b7cccbd52810d63db17e1557d59681f5f29be5a98' ;; 		ppc64le) natsArch='ppc64le'; sha256='28e2afbca41dffe453507a993291560bfc57c6f43fe435604f894c3d91426dd0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53314fd665bd0c97ace20b7fb2ca1b46ecfdd7426150f8745639bb7704613d5a`  
		Last Modified: Fri, 25 Apr 2025 17:47:34 GMT  
		Size: 6.5 MB (6483851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cefa71e52d2f6e7b13aac0c8fe523facca0507ac8e8b180b168eeadfd046b89`  
		Last Modified: Fri, 25 Apr 2025 17:47:33 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c198696667425fcef5f606fda093ce31277d14ed9b5dc1592fb47511143d5052`  
		Last Modified: Fri, 25 Apr 2025 17:47:33 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:20a327f5442b5e1a069fb161658d8b9436e0f0ce2df3802ad9d74362036c2210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b2f873973386278768ee962ed71409b2376682ae823894072e19be8cde68680`

```dockerfile
```

-	Layers:
	-	`sha256:9122357572edf020a23a1bbf0fbe37650762d41d728dfaccb594f7e5890cbd2d`  
		Last Modified: Fri, 25 Apr 2025 17:47:33 GMT  
		Size: 14.4 KB (14424 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:2f0c0883a1c8a7dd3a93730ce2ca646928c272aba42b05b5d163f5e779696f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9552050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28191bc799228c242ab1ebf65c8eaa89c320b25a78ee799103e544b8250226d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
ENV NATS_SERVER=2.11.1
# Tue, 08 Apr 2025 17:23:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='27c90d8bc0ad10bfb38ef92bdea8528b4bfc5aa56afba91c790fb3921ea205a2' ;; 		armhf) natsArch='arm6'; sha256='8f9f2f4aa85c242f254a175c9455e9d00c6a0e7fc96b87a14ef3bd6d8762e900' ;; 		armv7) natsArch='arm7'; sha256='06dee81c2fd32639ae646112daaf9b84b71023bee88b16fd3324fd922095dda1' ;; 		x86_64) natsArch='amd64'; sha256='f1d9754bf34316d1f7d349b176ff0414c9cce742846bf2eec0b402eee35a638c' ;; 		x86) natsArch='386'; sha256='b746e832f96f07ee5958c99201b7a96695a3e1339f416342b9fd3c083a68dba7' ;; 		s390x) natsArch='s390x'; sha256='018ec95e10758c3e6ea14f034d3fe099234957dec8290bc5aa3480a8d77e3e29' ;; 		ppc64le) natsArch='ppc64le'; sha256='be0f9308ffcdfa36189afdf7e8116235995d7d20406c0fc7b8aa5b5f724aa3d6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b82717f71af9d7a4242a00c3efbdf445cc5b3122fb74530e7d5e2971036151`  
		Last Modified: Tue, 08 Apr 2025 20:32:08 GMT  
		Size: 6.5 MB (6452958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49791283070c29e615bbe60ca9b43f0b5c63e67560f09700c02a4920fc31499`  
		Last Modified: Tue, 08 Apr 2025 20:32:07 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ade19b2805065881eeef7b4e282331a2f7fbd91f70c6349b33b2d448e8dc64`  
		Last Modified: Tue, 08 Apr 2025 20:32:07 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:f66e974c49c5b42df6f26cfe23be843bed87adb4df5efde68922bcd9bcdb0654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45fd3c0542a49a774cbfafb32d74dcb38bb7230e53a346c90ea2dc92652e671d`

```dockerfile
```

-	Layers:
	-	`sha256:dafec31d0d294d05c575a7f27247bd7720e66c489584ce418ed700595bb00c9f`  
		Last Modified: Tue, 08 Apr 2025 20:32:07 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:4fe60f222966727f3e81dbb3bf2aaec58c7c8b573afbe318f6cb2c70c19f37c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10254225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5d5d918ca9a0f7dd7c056851f2898f207c48f854da7954fc8fafc8fd1aa3021`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da0a4b9d57d2a4c2439f0c8731b7e1ef8f0a7f2a1edf643d5f50a73ffc0c31f9' ;; 		armhf) natsArch='arm6'; sha256='2370e8d794acb0f176be0f0885f9930fa9d8d1276f15162eb8db336467279bc1' ;; 		armv7) natsArch='arm7'; sha256='46b038e57ad586f05342dcd3b29a2c2597217c19172a916eef9187170f024ad8' ;; 		x86_64) natsArch='amd64'; sha256='a123c8e43abe5ca8f0bff9393547f20f4bbac6fc0fb3c586ec031855911c414a' ;; 		x86) natsArch='386'; sha256='03bf7db9323c453b1257c3a43a21fcd5a975a2cc136c4bbeab7c0e815939e37e' ;; 		s390x) natsArch='s390x'; sha256='eb40e4a843124198b7e8625b7cccbd52810d63db17e1557d59681f5f29be5a98' ;; 		ppc64le) natsArch='ppc64le'; sha256='28e2afbca41dffe453507a993291560bfc57c6f43fe435604f894c3d91426dd0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3febb0921652e8042f634bdcb7812f9a2ed40e073970e14a940960350b775dbf`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 6.3 MB (6260226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc226874bc3060e6e916fa3ef948812c54a012b6081a27eaab55addfec8b7473`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e367a33259d9c5e7a6a6b42c8482e8bc6930e1a713671c0cf2fd1b5c879eef01`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:fda84d5581ce64cec49def3b469b26e717bf64d28a817656b19e16da89e9ea25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a714d7bd3b6fd55a075f56b50fa0da44cf6616089161edf7a648ba47af3256`

```dockerfile
```

-	Layers:
	-	`sha256:5f55a5edc5478bd7d7c9bc7e0763ad4dee93ecffafd3ed2f7702e7ee06ae75b0`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 14.5 KB (14469 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:6b6b1109a98eafc180bae27e0e27a1110433dfd3577e78cac2d8eb793969fc43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9797332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52bb4f9d9231f9b6c625e4a3a3f2874bd83248ad61158f697eb327444118f598`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
ENV NATS_SERVER=2.11.1
# Tue, 08 Apr 2025 17:23:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='27c90d8bc0ad10bfb38ef92bdea8528b4bfc5aa56afba91c790fb3921ea205a2' ;; 		armhf) natsArch='arm6'; sha256='8f9f2f4aa85c242f254a175c9455e9d00c6a0e7fc96b87a14ef3bd6d8762e900' ;; 		armv7) natsArch='arm7'; sha256='06dee81c2fd32639ae646112daaf9b84b71023bee88b16fd3324fd922095dda1' ;; 		x86_64) natsArch='amd64'; sha256='f1d9754bf34316d1f7d349b176ff0414c9cce742846bf2eec0b402eee35a638c' ;; 		x86) natsArch='386'; sha256='b746e832f96f07ee5958c99201b7a96695a3e1339f416342b9fd3c083a68dba7' ;; 		s390x) natsArch='s390x'; sha256='018ec95e10758c3e6ea14f034d3fe099234957dec8290bc5aa3480a8d77e3e29' ;; 		ppc64le) natsArch='ppc64le'; sha256='be0f9308ffcdfa36189afdf7e8116235995d7d20406c0fc7b8aa5b5f724aa3d6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8be7344e3eed187cfb792f8b098e4b9639bd0e5318ceffb68a33a3bad2164c`  
		Last Modified: Tue, 08 Apr 2025 20:42:59 GMT  
		Size: 6.2 MB (6222020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd19bdb0c54b34703a3579dcae0cd27d09d0ed9ac711591a13fba04c9a89aacf`  
		Last Modified: Tue, 08 Apr 2025 20:42:58 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2608514a04b63ea4ad3654f5acd693a1bc97dc1d1c8b8a1495df0e53dda6ff0`  
		Last Modified: Tue, 08 Apr 2025 20:42:58 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:28f492787cca2adfb7bcfcb21be59f4685caad51e81ff81fac96d5d46445c776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ada670995406f8a9d5e52233a0003738fc8c1933710c4de448e87af34e5a3863`

```dockerfile
```

-	Layers:
	-	`sha256:e269226b323faa520a451de66e148284583959e77af2bf7d56a4d350cc37623a`  
		Last Modified: Tue, 08 Apr 2025 20:42:58 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:cf54ecfbde97d03a9d1a1bfdbcf069c2683ef48f34d72013b9064f5ed0ab9183
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10053959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f94c74252361e5594561679a5358b7e135dd9c7c2f3c51be0138903f04c6aa8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
ENV NATS_SERVER=2.11.1
# Tue, 08 Apr 2025 17:23:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='27c90d8bc0ad10bfb38ef92bdea8528b4bfc5aa56afba91c790fb3921ea205a2' ;; 		armhf) natsArch='arm6'; sha256='8f9f2f4aa85c242f254a175c9455e9d00c6a0e7fc96b87a14ef3bd6d8762e900' ;; 		armv7) natsArch='arm7'; sha256='06dee81c2fd32639ae646112daaf9b84b71023bee88b16fd3324fd922095dda1' ;; 		x86_64) natsArch='amd64'; sha256='f1d9754bf34316d1f7d349b176ff0414c9cce742846bf2eec0b402eee35a638c' ;; 		x86) natsArch='386'; sha256='b746e832f96f07ee5958c99201b7a96695a3e1339f416342b9fd3c083a68dba7' ;; 		s390x) natsArch='s390x'; sha256='018ec95e10758c3e6ea14f034d3fe099234957dec8290bc5aa3480a8d77e3e29' ;; 		ppc64le) natsArch='ppc64le'; sha256='be0f9308ffcdfa36189afdf7e8116235995d7d20406c0fc7b8aa5b5f724aa3d6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a92fbe14b2cdd6c1a85f89f171cfbad87c0f00fc6205b2d6c5cfa29cf51cf30`  
		Last Modified: Tue, 08 Apr 2025 22:04:28 GMT  
		Size: 6.6 MB (6585420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc913d6647309b3286a51c5f87c54edfb961dd53b9ca8a4496335154e303ab2e`  
		Last Modified: Tue, 08 Apr 2025 22:04:28 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22b8967d9a9d213c271cc67dcbe1d89b5b0870a2d2a399344c51f7cdc25b2c7`  
		Last Modified: Tue, 08 Apr 2025 22:04:28 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:b55039b07dc68ae69425511e99ab099b60f707e9a565a17a0d28e21a33c1f346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4570b0028f776dbca1deaabac6952192f625b95ec93d8098c7058262a3ca4b9`

```dockerfile
```

-	Layers:
	-	`sha256:5b1859f0680f19779c89b10a96fe392f905b04060b6ca55b19696d4fc51ece7c`  
		Last Modified: Tue, 08 Apr 2025 22:04:28 GMT  
		Size: 14.3 KB (14316 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-linux`

```console
$ docker pull nats@sha256:4bb7463f82c83da51fd098d9ddbc0dccfdc7415e110b02de375f60066b392878
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
$ docker pull nats@sha256:41dddbc7a9265892086db802a374dbf910b5d0db786c8ba12e27a81f2ede8f05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6282680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ddda49ccc5be8fc53872fcb74f0f168368af1d3e5fc27fd096bb4ab9fac9e5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7a31ab99389a11bb36db183df5a6bc8d784c1e96fb10c1973e04b98e17e58f51`  
		Last Modified: Tue, 08 Apr 2025 17:26:21 GMT  
		Size: 6.3 MB (6282171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bcd18a1de501f0dcf00113b8c1effd2b7f198a1383c537490e8dce3a826adce`  
		Last Modified: Tue, 08 Apr 2025 21:07:44 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:16692b029d2fd73a6c9833d59190a10a052903fbc5b68228ca0ce31e25895ee4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a60659f991d784a3586e62308c55e27054bad66d740cbde49980328b682cb858`

```dockerfile
```

-	Layers:
	-	`sha256:d0fd9d7883ec1e99c1a17109b0a6fd39dec7b9ec8f40f0ace2f2c15f9d8846a3`  
		Last Modified: Tue, 08 Apr 2025 21:07:45 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:f53994879dbfd2fc8177b383905d33db1095d8b42bb4bec64088771cecdb2bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6002072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01de3b3fb48e4b75539a9af5640e6f77115cdbe9419f3da2891472ec6e806148`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bc9bfb085b797367e9407dbdf5a3928ee0d69859fb96188165856b5e8e1b6e88`  
		Last Modified: Tue, 08 Apr 2025 17:26:22 GMT  
		Size: 6.0 MB (6001563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef30b0264d904d40fbf4763922653522d80a800c24f6bcbb52a1a66fd1accaf8`  
		Last Modified: Tue, 08 Apr 2025 21:07:08 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:f9537be10194b98f78298fad26add4a04948857f650479e674587da738dcf69c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7014bcdaac4c9653a29f6fc739854477633a62a69bd0cba053bbeecbfc57e101`

```dockerfile
```

-	Layers:
	-	`sha256:e337d587115a4b810f5a9fa3deb1db109744f3828488f355e6bfa4c965ea5501`  
		Last Modified: Tue, 08 Apr 2025 21:07:08 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:859b07690a2059b52277aceb9feed7e81269aed09859f1c3b0f3162d751ddb29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5992346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e38aded7ecfd1e1b61cc0452d01e01718e0a4be4ee666ac1980ddacb6f7defbc`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8f114aa547686a4604d8f5fbabd3d89b59a801cc55b68aa653d813c66ca32a65`  
		Last Modified: Tue, 08 Apr 2025 17:26:18 GMT  
		Size: 6.0 MB (5991835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844018e59249593be5d829b3a4bba323e96c26297db204b3a8a8a52e847f8041`  
		Last Modified: Tue, 08 Apr 2025 21:25:07 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:1e53207f824b4b97a2158a01c60662ef62ff32a777e55e615077563d48bcc314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a229febf9f435367bc3df4661afe24971b0581fa0b4b375a92d4ac38c3ce791`

```dockerfile
```

-	Layers:
	-	`sha256:36f6e0df21021319068725c9d7c2325e4fad06927e5ff9fe7fe11ec830f17f1c`  
		Last Modified: Tue, 08 Apr 2025 21:25:06 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:9142b78e748793c9e3b2fda3ac3800e66e866bf0147d634a7aea592f973a023a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5776867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee76a21b5d66ec40c0c8c53a6af4ed91124f7a2820ab80bf20279efdc3e689c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6b90b986da10be1b936fe6989055b49edb315427df0ceb03d1dd2f9dd98fb88`  
		Last Modified: Tue, 08 Apr 2025 17:26:18 GMT  
		Size: 5.8 MB (5776357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5e46c8b1d8619650c3d1afbfcf70b02949ce40d6fd6eb7d769bdc98a1def25`  
		Last Modified: Wed, 09 Apr 2025 00:53:02 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:9f289daca75844d624973e2b4e4a78db9e2026bfd59d743648f68e3c13d32a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53971055b1ebeea168a941b88f41f089dd9886aa55cbebe6b4f12f98ddb49666`

```dockerfile
```

-	Layers:
	-	`sha256:a65f769c9cecfc76c232cf377b8548ffd7fc82eae67b781487e0924b3319a183`  
		Last Modified: Wed, 09 Apr 2025 00:53:02 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:8cbd8caa2bdb9c64319ae113af4cf4170b92f3795148cb20401f2f1f16aa1d11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5757631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ba2ae7e87afe027065399c01f1230c431bed76a811a5cc5c83e971b6e70a26`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2c03c8b47070105a3781cfd93e5a048f0fcf1895182b8500a1875b914beccc2b`  
		Last Modified: Tue, 08 Apr 2025 17:26:19 GMT  
		Size: 5.8 MB (5757122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425937f6cd03177f214b970352644a3316a1a6ac085099e96875d62e6eb6b95d`  
		Last Modified: Tue, 08 Apr 2025 22:18:51 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:5aa97ff134b80e48aaa63c71d9c8343062cb648de6445e6d078b62dab5b08a3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8af43893a1163e246e9f97ae6b6ca899d5147c74db410070388f3dc6b1bb9a`

```dockerfile
```

-	Layers:
	-	`sha256:b2dde84b1c72b35f921945f0d6bec4b01ff2c811e34deff66dc5a99577731ade`  
		Last Modified: Tue, 08 Apr 2025 22:18:51 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; s390x

```console
$ docker pull nats@sha256:24602554caa826a00e26b3dae9c589026eaab3e0ad8e59cb573cac3996e62f8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6122577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7976c47bfec0473931b30ef2753bdc1cefde06b7a03f869cabb36b78aee6fd30`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:096b0701966ee2a29da8fc2c3f8ad25d2a0bb1211425d296e92558196ebe09c9`  
		Last Modified: Tue, 08 Apr 2025 17:26:22 GMT  
		Size: 6.1 MB (6122069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50402e49c7c832b57fb874a3e012194a27d09597f2d39ddc97db3701ae5bfb7`  
		Last Modified: Tue, 08 Apr 2025 22:07:44 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:6f2d2b491eee799540891efc47f6f00293192e82097e7b80bb5fd571bbf312c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8736b1c1aaa3dce6b14a6b7b5cad1d5cc142fae7d7d9fd17b8a6d72e67a82268`

```dockerfile
```

-	Layers:
	-	`sha256:1ab1e3d26d57dec0dbbe6b34b8c0c23c6308ed6e3e58b9267695ff2247985c40`  
		Last Modified: Tue, 08 Apr 2025 22:07:44 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:714b0b324ae5c514cc8066861c1ea58b8e852b21686bd57938b4cad501106b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.7249; amd64

```console
$ docker pull nats@sha256:70dfa0a823409d278307a2f602a989bb5088fc2ed408add1628e7026065e4f7f
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.2 MB (115214035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c10544dab15e09a82ee58dfe65c5cebe6e37634a0fc0e40720019d69e49ec056`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Fri, 18 Apr 2025 04:11:39 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 18 Apr 2025 04:11:40 GMT
RUN cmd /S /C #(nop) COPY file:eee3870bfbcd9bfddd3622d20a6c2075b583b61ab0944602ceefed02dee11aa2 in C:\nats-server.exe 
# Fri, 18 Apr 2025 04:11:41 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Fri, 18 Apr 2025 04:11:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 18 Apr 2025 04:11:42 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 18 Apr 2025 04:11:42 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5dab9cfa2f7ef2b19e95e68d27e3d0b208d9016da1b04298c500e78281a15e7`  
		Last Modified: Fri, 18 Apr 2025 04:11:48 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d0b032347a8dcb65e359d04c00733934bf6cfe61db4b1142a1df5f3de23a9cc`  
		Last Modified: Fri, 18 Apr 2025 04:11:47 GMT  
		Size: 6.5 MB (6455931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497b3350d5c31834bcca73478d5fc7c0d3c546c1676c042e1e9d1ec9afc85bdd`  
		Last Modified: Fri, 18 Apr 2025 04:11:46 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658de08330e9b739dfbff680b38b2bb55dc4b4aec6d4064b19ecc24c7ba9a8aa`  
		Last Modified: Fri, 18 Apr 2025 04:11:46 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0312f657691b722f56e7ed6bc33b2119988f7f21d9853fe0a8dcc79a3b5aec`  
		Last Modified: Fri, 18 Apr 2025 04:11:46 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fc9ae19d64bc742bb97a1eec58e04de0d2eab1eb71186876fed513a4b21a3d`  
		Last Modified: Fri, 18 Apr 2025 04:11:46 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:714b0b324ae5c514cc8066861c1ea58b8e852b21686bd57938b4cad501106b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull nats@sha256:70dfa0a823409d278307a2f602a989bb5088fc2ed408add1628e7026065e4f7f
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.2 MB (115214035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c10544dab15e09a82ee58dfe65c5cebe6e37634a0fc0e40720019d69e49ec056`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Fri, 18 Apr 2025 04:11:39 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 18 Apr 2025 04:11:40 GMT
RUN cmd /S /C #(nop) COPY file:eee3870bfbcd9bfddd3622d20a6c2075b583b61ab0944602ceefed02dee11aa2 in C:\nats-server.exe 
# Fri, 18 Apr 2025 04:11:41 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Fri, 18 Apr 2025 04:11:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 18 Apr 2025 04:11:42 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 18 Apr 2025 04:11:42 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5dab9cfa2f7ef2b19e95e68d27e3d0b208d9016da1b04298c500e78281a15e7`  
		Last Modified: Fri, 18 Apr 2025 04:11:48 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d0b032347a8dcb65e359d04c00733934bf6cfe61db4b1142a1df5f3de23a9cc`  
		Last Modified: Fri, 18 Apr 2025 04:11:47 GMT  
		Size: 6.5 MB (6455931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497b3350d5c31834bcca73478d5fc7c0d3c546c1676c042e1e9d1ec9afc85bdd`  
		Last Modified: Fri, 18 Apr 2025 04:11:46 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658de08330e9b739dfbff680b38b2bb55dc4b4aec6d4064b19ecc24c7ba9a8aa`  
		Last Modified: Fri, 18 Apr 2025 04:11:46 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0312f657691b722f56e7ed6bc33b2119988f7f21d9853fe0a8dcc79a3b5aec`  
		Last Modified: Fri, 18 Apr 2025 04:11:46 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fc9ae19d64bc742bb97a1eec58e04de0d2eab1eb71186876fed513a4b21a3d`  
		Last Modified: Fri, 18 Apr 2025 04:11:46 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:4bb7463f82c83da51fd098d9ddbc0dccfdc7415e110b02de375f60066b392878
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
$ docker pull nats@sha256:41dddbc7a9265892086db802a374dbf910b5d0db786c8ba12e27a81f2ede8f05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6282680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ddda49ccc5be8fc53872fcb74f0f168368af1d3e5fc27fd096bb4ab9fac9e5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7a31ab99389a11bb36db183df5a6bc8d784c1e96fb10c1973e04b98e17e58f51`  
		Last Modified: Tue, 08 Apr 2025 17:26:21 GMT  
		Size: 6.3 MB (6282171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bcd18a1de501f0dcf00113b8c1effd2b7f198a1383c537490e8dce3a826adce`  
		Last Modified: Tue, 08 Apr 2025 21:07:44 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:16692b029d2fd73a6c9833d59190a10a052903fbc5b68228ca0ce31e25895ee4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a60659f991d784a3586e62308c55e27054bad66d740cbde49980328b682cb858`

```dockerfile
```

-	Layers:
	-	`sha256:d0fd9d7883ec1e99c1a17109b0a6fd39dec7b9ec8f40f0ace2f2c15f9d8846a3`  
		Last Modified: Tue, 08 Apr 2025 21:07:45 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:f53994879dbfd2fc8177b383905d33db1095d8b42bb4bec64088771cecdb2bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6002072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01de3b3fb48e4b75539a9af5640e6f77115cdbe9419f3da2891472ec6e806148`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bc9bfb085b797367e9407dbdf5a3928ee0d69859fb96188165856b5e8e1b6e88`  
		Last Modified: Tue, 08 Apr 2025 17:26:22 GMT  
		Size: 6.0 MB (6001563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef30b0264d904d40fbf4763922653522d80a800c24f6bcbb52a1a66fd1accaf8`  
		Last Modified: Tue, 08 Apr 2025 21:07:08 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:f9537be10194b98f78298fad26add4a04948857f650479e674587da738dcf69c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7014bcdaac4c9653a29f6fc739854477633a62a69bd0cba053bbeecbfc57e101`

```dockerfile
```

-	Layers:
	-	`sha256:e337d587115a4b810f5a9fa3deb1db109744f3828488f355e6bfa4c965ea5501`  
		Last Modified: Tue, 08 Apr 2025 21:07:08 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:859b07690a2059b52277aceb9feed7e81269aed09859f1c3b0f3162d751ddb29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5992346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e38aded7ecfd1e1b61cc0452d01e01718e0a4be4ee666ac1980ddacb6f7defbc`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8f114aa547686a4604d8f5fbabd3d89b59a801cc55b68aa653d813c66ca32a65`  
		Last Modified: Tue, 08 Apr 2025 17:26:18 GMT  
		Size: 6.0 MB (5991835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844018e59249593be5d829b3a4bba323e96c26297db204b3a8a8a52e847f8041`  
		Last Modified: Tue, 08 Apr 2025 21:25:07 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:1e53207f824b4b97a2158a01c60662ef62ff32a777e55e615077563d48bcc314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a229febf9f435367bc3df4661afe24971b0581fa0b4b375a92d4ac38c3ce791`

```dockerfile
```

-	Layers:
	-	`sha256:36f6e0df21021319068725c9d7c2325e4fad06927e5ff9fe7fe11ec830f17f1c`  
		Last Modified: Tue, 08 Apr 2025 21:25:06 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:9142b78e748793c9e3b2fda3ac3800e66e866bf0147d634a7aea592f973a023a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5776867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee76a21b5d66ec40c0c8c53a6af4ed91124f7a2820ab80bf20279efdc3e689c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6b90b986da10be1b936fe6989055b49edb315427df0ceb03d1dd2f9dd98fb88`  
		Last Modified: Tue, 08 Apr 2025 17:26:18 GMT  
		Size: 5.8 MB (5776357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5e46c8b1d8619650c3d1afbfcf70b02949ce40d6fd6eb7d769bdc98a1def25`  
		Last Modified: Wed, 09 Apr 2025 00:53:02 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:9f289daca75844d624973e2b4e4a78db9e2026bfd59d743648f68e3c13d32a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53971055b1ebeea168a941b88f41f089dd9886aa55cbebe6b4f12f98ddb49666`

```dockerfile
```

-	Layers:
	-	`sha256:a65f769c9cecfc76c232cf377b8548ffd7fc82eae67b781487e0924b3319a183`  
		Last Modified: Wed, 09 Apr 2025 00:53:02 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:8cbd8caa2bdb9c64319ae113af4cf4170b92f3795148cb20401f2f1f16aa1d11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5757631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ba2ae7e87afe027065399c01f1230c431bed76a811a5cc5c83e971b6e70a26`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2c03c8b47070105a3781cfd93e5a048f0fcf1895182b8500a1875b914beccc2b`  
		Last Modified: Tue, 08 Apr 2025 17:26:19 GMT  
		Size: 5.8 MB (5757122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425937f6cd03177f214b970352644a3316a1a6ac085099e96875d62e6eb6b95d`  
		Last Modified: Tue, 08 Apr 2025 22:18:51 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:5aa97ff134b80e48aaa63c71d9c8343062cb648de6445e6d078b62dab5b08a3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8af43893a1163e246e9f97ae6b6ca899d5147c74db410070388f3dc6b1bb9a`

```dockerfile
```

-	Layers:
	-	`sha256:b2dde84b1c72b35f921945f0d6bec4b01ff2c811e34deff66dc5a99577731ade`  
		Last Modified: Tue, 08 Apr 2025 22:18:51 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; s390x

```console
$ docker pull nats@sha256:24602554caa826a00e26b3dae9c589026eaab3e0ad8e59cb573cac3996e62f8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6122577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7976c47bfec0473931b30ef2753bdc1cefde06b7a03f869cabb36b78aee6fd30`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:096b0701966ee2a29da8fc2c3f8ad25d2a0bb1211425d296e92558196ebe09c9`  
		Last Modified: Tue, 08 Apr 2025 17:26:22 GMT  
		Size: 6.1 MB (6122069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50402e49c7c832b57fb874a3e012194a27d09597f2d39ddc97db3701ae5bfb7`  
		Last Modified: Tue, 08 Apr 2025 22:07:44 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:6f2d2b491eee799540891efc47f6f00293192e82097e7b80bb5fd571bbf312c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8736b1c1aaa3dce6b14a6b7b5cad1d5cc142fae7d7d9fd17b8a6d72e67a82268`

```dockerfile
```

-	Layers:
	-	`sha256:1ab1e3d26d57dec0dbbe6b34b8c0c23c6308ed6e3e58b9267695ff2247985c40`  
		Last Modified: Tue, 08 Apr 2025 22:07:44 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:d50be1cda62b37ce5581671dafc900fc728a2c95a2497d7a1a3f76578329fa81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.7249; amd64

```console
$ docker pull nats@sha256:de12da09e1602e2f93ed8b9b9897000258cf9608c390bc2620472c61a146810b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2172650201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f8e26de837c3eb00f55fdb3ea32e3a8eca48f3f6f7163fe633b78ed5241d985`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Fri, 18 Apr 2025 03:15:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 18 Apr 2025 03:15:31 GMT
ENV NATS_DOCKERIZED=1
# Fri, 18 Apr 2025 03:15:32 GMT
ENV NATS_SERVER=2.11.1
# Fri, 18 Apr 2025 03:15:33 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.1/nats-server-v2.11.1-windows-amd64.zip
# Fri, 18 Apr 2025 03:15:34 GMT
ENV NATS_SERVER_SHASUM=f5594798e1b77013b674c0049070d2502c20ee6f03a04d854cac333e2a21ca20
# Fri, 18 Apr 2025 03:16:07 GMT
RUN Set-PSDebug -Trace 2
# Fri, 18 Apr 2025 03:16:25 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 18 Apr 2025 03:16:26 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Fri, 18 Apr 2025 03:16:27 GMT
EXPOSE 4222 6222 8222
# Fri, 18 Apr 2025 03:16:27 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 18 Apr 2025 03:16:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Fri, 18 Apr 2025 03:13:03 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7822538d66aa517be43d1d696a9cc338fba7d6950e51918ac111ff32439b76d`  
		Last Modified: Fri, 18 Apr 2025 03:16:32 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:352f9e3e8b1aeaa1335f9d9417867a41164c3927fc6b5260d2f8c727d7ce3537`  
		Last Modified: Fri, 18 Apr 2025 03:16:32 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1f23260e2b6c00f1d9e28c5e37d7bdd45320561ed314845ff8d9ad8815ba79`  
		Last Modified: Fri, 18 Apr 2025 03:16:32 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66dc359cc850871940050c1e2fa57ba9ee16d9b033fba1532255cc0ea7a487da`  
		Last Modified: Fri, 18 Apr 2025 03:16:31 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd3feaf085072d792e35ade328ab0c2c1ecf53fd61f3c21f296549840710430`  
		Last Modified: Fri, 18 Apr 2025 03:16:31 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dae23d135bd9c3a0f11a7fb76e406cf4f5492a7988bdc3d9611f746ebb6945c`  
		Last Modified: Fri, 18 Apr 2025 03:16:31 GMT  
		Size: 322.6 KB (322628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bcdffa91604493a08769e767b51db8f8bc176116e8019a081a432923b5cb8d2`  
		Last Modified: Fri, 18 Apr 2025 03:16:31 GMT  
		Size: 6.8 MB (6789581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270410cf637c0ea7c99ed52451d17b6129481750e0caf3e12ad1cab37a0cb3ce`  
		Last Modified: Fri, 18 Apr 2025 03:16:30 GMT  
		Size: 1.8 KB (1849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2ad53fbd757d0e60898d5ee40e6355c43e9a4862e5b82429752248dbd9a85b6`  
		Last Modified: Fri, 18 Apr 2025 03:16:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c32fbcc93f5bdc7d627e5633180fff8d0b1759564412e5571800b97b912e371e`  
		Last Modified: Fri, 18 Apr 2025 03:16:30 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7c6da8a76e3b31cfa4ea2184896009c2dc8b62dd7f14fb45739484b9d6189f9`  
		Last Modified: Fri, 18 Apr 2025 03:16:31 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:d50be1cda62b37ce5581671dafc900fc728a2c95a2497d7a1a3f76578329fa81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull nats@sha256:de12da09e1602e2f93ed8b9b9897000258cf9608c390bc2620472c61a146810b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2172650201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f8e26de837c3eb00f55fdb3ea32e3a8eca48f3f6f7163fe633b78ed5241d985`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Fri, 18 Apr 2025 03:15:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 18 Apr 2025 03:15:31 GMT
ENV NATS_DOCKERIZED=1
# Fri, 18 Apr 2025 03:15:32 GMT
ENV NATS_SERVER=2.11.1
# Fri, 18 Apr 2025 03:15:33 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.1/nats-server-v2.11.1-windows-amd64.zip
# Fri, 18 Apr 2025 03:15:34 GMT
ENV NATS_SERVER_SHASUM=f5594798e1b77013b674c0049070d2502c20ee6f03a04d854cac333e2a21ca20
# Fri, 18 Apr 2025 03:16:07 GMT
RUN Set-PSDebug -Trace 2
# Fri, 18 Apr 2025 03:16:25 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 18 Apr 2025 03:16:26 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Fri, 18 Apr 2025 03:16:27 GMT
EXPOSE 4222 6222 8222
# Fri, 18 Apr 2025 03:16:27 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 18 Apr 2025 03:16:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Fri, 18 Apr 2025 03:13:03 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7822538d66aa517be43d1d696a9cc338fba7d6950e51918ac111ff32439b76d`  
		Last Modified: Fri, 18 Apr 2025 03:16:32 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:352f9e3e8b1aeaa1335f9d9417867a41164c3927fc6b5260d2f8c727d7ce3537`  
		Last Modified: Fri, 18 Apr 2025 03:16:32 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1f23260e2b6c00f1d9e28c5e37d7bdd45320561ed314845ff8d9ad8815ba79`  
		Last Modified: Fri, 18 Apr 2025 03:16:32 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66dc359cc850871940050c1e2fa57ba9ee16d9b033fba1532255cc0ea7a487da`  
		Last Modified: Fri, 18 Apr 2025 03:16:31 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd3feaf085072d792e35ade328ab0c2c1ecf53fd61f3c21f296549840710430`  
		Last Modified: Fri, 18 Apr 2025 03:16:31 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dae23d135bd9c3a0f11a7fb76e406cf4f5492a7988bdc3d9611f746ebb6945c`  
		Last Modified: Fri, 18 Apr 2025 03:16:31 GMT  
		Size: 322.6 KB (322628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bcdffa91604493a08769e767b51db8f8bc176116e8019a081a432923b5cb8d2`  
		Last Modified: Fri, 18 Apr 2025 03:16:31 GMT  
		Size: 6.8 MB (6789581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270410cf637c0ea7c99ed52451d17b6129481750e0caf3e12ad1cab37a0cb3ce`  
		Last Modified: Fri, 18 Apr 2025 03:16:30 GMT  
		Size: 1.8 KB (1849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2ad53fbd757d0e60898d5ee40e6355c43e9a4862e5b82429752248dbd9a85b6`  
		Last Modified: Fri, 18 Apr 2025 03:16:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c32fbcc93f5bdc7d627e5633180fff8d0b1759564412e5571800b97b912e371e`  
		Last Modified: Fri, 18 Apr 2025 03:16:30 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7c6da8a76e3b31cfa4ea2184896009c2dc8b62dd7f14fb45739484b9d6189f9`  
		Last Modified: Fri, 18 Apr 2025 03:16:31 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10`

```console
$ docker pull nats@sha256:ef569ceb79faf65ff225371b1ab410fe2fab0561c2b32b54fb04fa53a3d1856e
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
	-	windows version 10.0.17763.7249; amd64

### `nats:2.10` - linux; amd64

```console
$ docker pull nats@sha256:eb025eeb0d8833044a3586a8f877482c5cae975cf0db03161d852efc1246a6af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6168774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d1f7c9f744161aacb847006fe289263073f3b614d1c3b26d77eb78c8cf81bc1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fa699494b4e64a703db8ad4671c9c07acbcebf379361896152b27f3c751db5ea`  
		Last Modified: Tue, 08 Apr 2025 17:26:15 GMT  
		Size: 6.2 MB (6168265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bcd18a1de501f0dcf00113b8c1effd2b7f198a1383c537490e8dce3a826adce`  
		Last Modified: Tue, 08 Apr 2025 21:07:44 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:c517a451e9619031d8c7624144f9ad61c5ce8fc44a6b98384b1be37db42a13aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a30f6e0f6a9c75dc1e119cc79f082306fbd1135b4623bcac32b4e69c5477c79`

```dockerfile
```

-	Layers:
	-	`sha256:c1f4c5ceb5f8a657b2f58404551421559687776ee014f879d1de5ebfcfc8dece`  
		Last Modified: Tue, 08 Apr 2025 21:07:44 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; arm variant v6

```console
$ docker pull nats@sha256:7db0743b57a4c00470536801c63dab555cde243256324e65f52fa56f95e8d05c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5892863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:156b95545afd9f61a732db04e0e269ad8096a44d11fcba171f46f5fc09f10be8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f15bb1b47edf48e706d17c3e23b17de9fd17df8625ebe30db7b257f38601880b`  
		Last Modified: Tue, 08 Apr 2025 17:26:16 GMT  
		Size: 5.9 MB (5892353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c04ce8d443571bb4036f99c3781518adcf9060a99a5ea6831ea8f84166009fa`  
		Last Modified: Tue, 08 Apr 2025 21:07:19 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:15d9432cd998d8b87f997b05c593e27930683fdbc66928719c62ae4d0ec12dcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:720e7875f18f4349eb3b0fdfdbfd7286ff0c08f0429432b15bafee93e932bf74`

```dockerfile
```

-	Layers:
	-	`sha256:88029e21b6c24e65c3027c232c1081a99596ee9a2a06d32df17b3302efd1b906`  
		Last Modified: Tue, 08 Apr 2025 21:07:20 GMT  
		Size: 8.8 KB (8788 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; arm variant v7

```console
$ docker pull nats@sha256:ee4e0314a0e7aea512e4a409b764dad958b834efa343dc2c9f43af51cd9f93f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5881346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a4be349c6c0f0343730c248084c65d1d6f47c18e3f8e0b451b2a081c18d2a59`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:dd82440cc0596353342b1677ea71d5175ec429a9b36ac37432305afd5db00b0c`  
		Last Modified: Tue, 08 Apr 2025 17:26:14 GMT  
		Size: 5.9 MB (5880837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53370f7d0e620e0c268408ebb6d4eb116cc5d1cb1116c38c4cfc478a97770c97`  
		Last Modified: Tue, 08 Apr 2025 21:25:18 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:b1befa3c23bdad19d294b5d73df0215bbf522fb002ba9e3910b085ed6010a672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2488e8a26c16d254d9b2c73a8f05bc4633e461cafb394be336c89b3d8e25385b`

```dockerfile
```

-	Layers:
	-	`sha256:22c87716fccba9922e3ab54d04c96d96849a07f9008c769d2e3c0c70d8aa5c4f`  
		Last Modified: Tue, 08 Apr 2025 21:25:18 GMT  
		Size: 8.8 KB (8789 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cbddc5491ac98646fe41ec6d0ddb64a8eeb7dfc7e39a7943ad6726cb34b7e53a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5671791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:695af0b5b248614722193c65c6610f25cb624e737ad6cada12d6e37ebce83468`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3e90cc5bec7d316417a1d1f6be7467d1ffc087233ec78f52ac78ab8830e3acea`  
		Last Modified: Tue, 08 Apr 2025 17:26:16 GMT  
		Size: 5.7 MB (5671283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7220a61a8a41868b70e67bdb239c254b16b0205ec13df5e994651ae989244cc8`  
		Last Modified: Wed, 09 Apr 2025 00:53:12 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:fe978136fb3f048731eae4c0049b4a6c7e1666d28e67cc5230db8ea3ff1330f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a4a78a719e6a4228f405f630420a6708c2fae6cca4dae826bfcfb5b7d105b46`

```dockerfile
```

-	Layers:
	-	`sha256:4e5927ac7d992740c9f913dcbd55ca3e49730c8e36ff5582baa08390ba8f6124`  
		Last Modified: Wed, 09 Apr 2025 00:53:12 GMT  
		Size: 8.8 KB (8824 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; ppc64le

```console
$ docker pull nats@sha256:4a615aba087255752db7335a6bc4249a0647cb418f579c74482db9abb86fae25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5649622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f2ce6cc279148f1f5bd10181203af2ebbd5ab6a72adb1cd14182022df01e79a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:34e405e5099052276a00bc13663d16e3de17abc6fc928997b78eab3bc6ba70c3`  
		Last Modified: Tue, 08 Apr 2025 17:26:11 GMT  
		Size: 5.6 MB (5649113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df44b2e202d4a27f74e605facd189d353c5221f85ec1ec8921e000d806f8aba2`  
		Last Modified: Tue, 08 Apr 2025 22:19:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:7b0abcba33ed78e06ef8539efa7d2f8e497f1a1e073dabe92eeb6b7921e05eaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1aa5a17256650818135e1acc93b601b5f73efdda407af6915ac035b2278439b`

```dockerfile
```

-	Layers:
	-	`sha256:1fdc46b1ea6a973250b0cb5fc1081608ff47e0ef6968275a7dbe62f66e9a1b80`  
		Last Modified: Tue, 08 Apr 2025 22:19:06 GMT  
		Size: 8.8 KB (8765 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; s390x

```console
$ docker pull nats@sha256:908f46d6f7d985bd1f0886839f21899dff78cbc2532bf80bb0af3885f5939698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6011225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02bf6f293b378ae455ac72206cbc16982912a66a96a1889f9ab0bb1e61652d68`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4df3046fee85d5087ea08a6ef49df55c38ddd7977f89e5073f536b8f0736b450`  
		Last Modified: Tue, 08 Apr 2025 17:26:14 GMT  
		Size: 6.0 MB (6010715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56724fa9fe9d3923fb6f5b9b821dbabbcce3213f51cac5dd418711765c5b1dc9`  
		Last Modified: Tue, 08 Apr 2025 22:08:16 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:09b3b37c386e69802fb1aab1352764f3bb00d31c4640fc88d2985d8fb0d6a98f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:427ab84d44e26941a1638adaca454bcd6c70232bf10994ece31a10d955adf2c5`

```dockerfile
```

-	Layers:
	-	`sha256:450d43c8eb4ce30507123a312630f9694cda7bbff21b8a86a48e4ba09049b69c`  
		Last Modified: Tue, 08 Apr 2025 22:08:16 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - windows version 10.0.17763.7249; amd64

```console
$ docker pull nats@sha256:87b23809aa621f181b677e1c5a17da29d313a6a77b1d5d75f3b5a05f34ebce40
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 MB (115044774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce961ec5557c6d1b57877c9594add188039f9cd34dd7a53cede119a9c2a48f0d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Fri, 18 Apr 2025 04:13:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 18 Apr 2025 04:13:42 GMT
RUN cmd /S /C #(nop) COPY file:911e7fad0174090a7de06fb3b7fca63c95843409a6ad46e295d2fe4da8d99d2a in C:\nats-server.exe 
# Fri, 18 Apr 2025 04:13:42 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Fri, 18 Apr 2025 04:13:43 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 18 Apr 2025 04:13:43 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 18 Apr 2025 04:13:44 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:581d68c582ecb4e34ebbf95721dde6c0dad76f87dffcf1b2a281a068e7c997b2`  
		Last Modified: Fri, 18 Apr 2025 04:13:47 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dacc779fecd4cecc205cc8b50de0a3f71c9251adb342ad22bedefcb3b971d889`  
		Last Modified: Fri, 18 Apr 2025 04:13:47 GMT  
		Size: 6.3 MB (6286707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec94aed503ca0a62740a2ad52a1f3572585c0afd9d51f366dee00e232097ce1`  
		Last Modified: Fri, 18 Apr 2025 04:13:46 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60d81dd7de5c54597a8c47ee90f1f2d2743a987da2e7b0859f2889658673db7a`  
		Last Modified: Fri, 18 Apr 2025 04:13:46 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d93759a1c81017eaad5721c68a97202528074ab706a10309bc3a564a87d630c`  
		Last Modified: Fri, 18 Apr 2025 04:13:46 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7115d3cfeddee720c6c7f4d7c65d6bd8676389e9e44d59afacd0a722a3da6c`  
		Last Modified: Fri, 18 Apr 2025 04:13:46 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine`

```console
$ docker pull nats@sha256:a369873a0c06bd111535b2a9f17fdff08372032d82d4cbf39e2e92ae8c4d158b
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
$ docker pull nats@sha256:7c595082cf89feecb72266d508dbee805293d22ef11c33feef2c36d53bf8129b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10275635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40dfcebf44e537b17b99074bbbae39852a43835cac98fb5db055c9957ec8bea8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
ENV NATS_SERVER=2.10.27
# Tue, 08 Apr 2025 17:23:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='47067e41dc27890d9665ddf429ce24f9ed50bddd035dee63b915fcfcb1f8043b' ;; 		armhf) natsArch='arm6'; sha256='4e4268d1bb83568217f8dbce77d5e0ca93cea8282d6fef796b505cdd2b16cb64' ;; 		armv7) natsArch='arm7'; sha256='a1dc4d8ff0a1e61aa80c9b50f5aa45dac3a3126e70d0c2ae5f53119dcf697503' ;; 		x86_64) natsArch='amd64'; sha256='0c3f53edaf1acccc41866d49d9c3626c9de8c9138b2fc11bbadfd3a4eb544ef1' ;; 		x86) natsArch='386'; sha256='f6b515da90da16bf09570d9dc67ef1488aaa75334c559c4c71371527242c5511' ;; 		s390x) natsArch='s390x'; sha256='f6864ce2b8fe25359ff9a307fabc88201e113b8c57634be2893d7bfafe425525' ;; 		ppc64le) natsArch='ppc64le'; sha256='29c22b82c139baca9231c30f9a4a61f0f6df9407d67971c035a5ad45eb4296cf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b418e663727e5b843db36fa727e22d92fb31bb99f1235e26dccfeb39750e0fa1`  
		Last Modified: Tue, 08 Apr 2025 20:28:15 GMT  
		Size: 6.6 MB (6632418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076c16eaada3cf6044d2362098bd6dedbdeb8506a826aeb10418ba41b6c55649`  
		Last Modified: Tue, 08 Apr 2025 20:28:15 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182cda9eb87b0b6df53ff5440502e2b7c3abdc0af53ef762bf3bda16a3c652e0`  
		Last Modified: Tue, 08 Apr 2025 20:28:15 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:bae31228d4a07f797e747d5d364ac169bd32a5b4f304f82cded49785b87c3865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3098b404f7af3eb2639f27bc50e6ee18a546586df54e768d10ec3e8649d19c1`

```dockerfile
```

-	Layers:
	-	`sha256:810b82eda42e704bfe9a436a96b272f32b793c1afc9cbcad6685ebd5f9d2e64a`  
		Last Modified: Tue, 08 Apr 2025 20:28:15 GMT  
		Size: 13.1 KB (13122 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:f4af69c51467ad969030a6285656c53a491fc03b8e442c30b897b1691439c471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9729296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db7b314b737c1720f822adbbefbcae87909929bf35a02b8d28a76fa7aeb01bc0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.10.28
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='78f9b382d468f7b683bf8bdda2c6276de1fd230d9d19724485f48b327d7ed4c2' ;; 		armhf) natsArch='arm6'; sha256='2a29a87abdec21bff9fb19a30aa06af12a6db31ec32d0b3de1a7c8bdeeb74b19' ;; 		armv7) natsArch='arm7'; sha256='837db6e72894993bde7f0e402f6f9dc151d8452b0441cea630260764bafd4c84' ;; 		x86_64) natsArch='amd64'; sha256='52e3baee2bf9cb4f3d362e293538e9f11ccfdb22ac9fbbd2bcad790e3ba41e3e' ;; 		x86) natsArch='386'; sha256='ffabdd7c124951b68ed4501223d5a877c3e90c5da68c27c884a58806eaa1c369' ;; 		s390x) natsArch='s390x'; sha256='f5627e4db5746200f62e6d5d9212dcfc59a4d4dc9cee30abf8eafdafac5445a1' ;; 		ppc64le) natsArch='ppc64le'; sha256='096424d6958c7b2798027208d0cc0c2ea5632e5530fd94d66712d586ca6d6d27' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e97974a6f36486b798da64002fc218b2233d353058852cffd0220594b01e269`  
		Last Modified: Fri, 25 Apr 2025 17:47:47 GMT  
		Size: 6.4 MB (6363595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb6a73b6e361505406303a8c7b3f3cfeba51010bf739aef7889bf7f0317a3b8`  
		Last Modified: Fri, 25 Apr 2025 17:47:46 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e222efd7d05fe8bcbda2e28970d7b05f8bb17ea70e7b7facf4701541d05df8`  
		Last Modified: Fri, 25 Apr 2025 17:47:46 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:5d34c1d5bed5a36593535f90aa950998957ae6a3d449899399f891679fa4ccb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05763aa76d78f8542ea1a12d8d75d8fe560b0dc4580158377ec49947c2b6d9cb`

```dockerfile
```

-	Layers:
	-	`sha256:27aef148734276a47a22fea3a763eeb98084a6604242d969b88cfa2ebba41576`  
		Last Modified: Fri, 25 Apr 2025 17:47:46 GMT  
		Size: 13.2 KB (13198 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:621f3f44322f8b79f9c90854c7a90a771165c16aa6d0e7974c79c101dbf23277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9443111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d811fdd54801fa7bfb080198ad7ef6ad0f572b8116d167e7fcafdc8fa3bd416`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
ENV NATS_SERVER=2.10.27
# Tue, 08 Apr 2025 17:23:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='47067e41dc27890d9665ddf429ce24f9ed50bddd035dee63b915fcfcb1f8043b' ;; 		armhf) natsArch='arm6'; sha256='4e4268d1bb83568217f8dbce77d5e0ca93cea8282d6fef796b505cdd2b16cb64' ;; 		armv7) natsArch='arm7'; sha256='a1dc4d8ff0a1e61aa80c9b50f5aa45dac3a3126e70d0c2ae5f53119dcf697503' ;; 		x86_64) natsArch='amd64'; sha256='0c3f53edaf1acccc41866d49d9c3626c9de8c9138b2fc11bbadfd3a4eb544ef1' ;; 		x86) natsArch='386'; sha256='f6b515da90da16bf09570d9dc67ef1488aaa75334c559c4c71371527242c5511' ;; 		s390x) natsArch='s390x'; sha256='f6864ce2b8fe25359ff9a307fabc88201e113b8c57634be2893d7bfafe425525' ;; 		ppc64le) natsArch='ppc64le'; sha256='29c22b82c139baca9231c30f9a4a61f0f6df9407d67971c035a5ad45eb4296cf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ecbba4e95d185ac65d0c976ec7b556783ec7a2c472f76f120b280418cb0086c`  
		Last Modified: Tue, 08 Apr 2025 20:32:21 GMT  
		Size: 6.3 MB (6344018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc57271692fbc3c72f3c7a7a018a4559f99357a43f63f6310b4933863caf445`  
		Last Modified: Tue, 08 Apr 2025 20:32:20 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28439e554ffc1776ef89b1a3cce85713e57c4f52c1839c9200c5122d14a69b72`  
		Last Modified: Tue, 08 Apr 2025 20:32:20 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:47c2e0842bde6cf10f7522a782753461a508494a2c2d0c7705de463304cfbfb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28a6b164add8300b5c9ca2618136d48ac0701896918b8215a43b18cfc8276aec`

```dockerfile
```

-	Layers:
	-	`sha256:5f67ac49cf858b21532ebd7b3ab2c3f96b8e6618096700d163b9c3aa1d7cff3c`  
		Last Modified: Tue, 08 Apr 2025 20:32:20 GMT  
		Size: 13.2 KB (13198 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:fb56b601a01e41e3fa3e1ec6882a5c7080064af2cbf8eebbe0aa8789057d7d65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10139926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c20275401ac1b6354f9bceea70fdbc9ea6b248f61de5860e8a48f4b9fa13449`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.10.28
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='78f9b382d468f7b683bf8bdda2c6276de1fd230d9d19724485f48b327d7ed4c2' ;; 		armhf) natsArch='arm6'; sha256='2a29a87abdec21bff9fb19a30aa06af12a6db31ec32d0b3de1a7c8bdeeb74b19' ;; 		armv7) natsArch='arm7'; sha256='837db6e72894993bde7f0e402f6f9dc151d8452b0441cea630260764bafd4c84' ;; 		x86_64) natsArch='amd64'; sha256='52e3baee2bf9cb4f3d362e293538e9f11ccfdb22ac9fbbd2bcad790e3ba41e3e' ;; 		x86) natsArch='386'; sha256='ffabdd7c124951b68ed4501223d5a877c3e90c5da68c27c884a58806eaa1c369' ;; 		s390x) natsArch='s390x'; sha256='f5627e4db5746200f62e6d5d9212dcfc59a4d4dc9cee30abf8eafdafac5445a1' ;; 		ppc64le) natsArch='ppc64le'; sha256='096424d6958c7b2798027208d0cc0c2ea5632e5530fd94d66712d586ca6d6d27' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d88dec44185a51ca27621bbb65e75ccd454b3c28c91009b2dde51a8ff3b55e`  
		Last Modified: Fri, 25 Apr 2025 17:47:42 GMT  
		Size: 6.1 MB (6145926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf91e9429cda3e96e24922bd3640282bad3965a0d6209055ac549cc49b5e0f8a`  
		Last Modified: Fri, 25 Apr 2025 17:47:41 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c6034f34091ef89d05c32fed01a7493f7c83cbbf10547c8aefac36a59fe368`  
		Last Modified: Fri, 25 Apr 2025 17:47:41 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:770428e58483a9652ac1bc757a92b38fb475e7802a1661bd0ee9bdbcc99a1a7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9fafe954b8c08a5febfa3873a84d9f621009fd0e4dc99eecd3c7d0e8a2ee129`

```dockerfile
```

-	Layers:
	-	`sha256:3d1465d1edfad8a9d270db627b7ae6ba90ac0fe85ef2e09550f0bd2a9ff67820`  
		Last Modified: Fri, 25 Apr 2025 17:47:41 GMT  
		Size: 13.2 KB (13226 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:4ccdae65f4f4d5a390b65d808cf366bf3356dc9570d9ed1dbe567de6f7aced46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9687965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae24adf477a3928acf9bb4015ae7dfd6e3ebb7bc64b5112a7748aaf8de2e6b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
ENV NATS_SERVER=2.10.27
# Tue, 08 Apr 2025 17:23:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='47067e41dc27890d9665ddf429ce24f9ed50bddd035dee63b915fcfcb1f8043b' ;; 		armhf) natsArch='arm6'; sha256='4e4268d1bb83568217f8dbce77d5e0ca93cea8282d6fef796b505cdd2b16cb64' ;; 		armv7) natsArch='arm7'; sha256='a1dc4d8ff0a1e61aa80c9b50f5aa45dac3a3126e70d0c2ae5f53119dcf697503' ;; 		x86_64) natsArch='amd64'; sha256='0c3f53edaf1acccc41866d49d9c3626c9de8c9138b2fc11bbadfd3a4eb544ef1' ;; 		x86) natsArch='386'; sha256='f6b515da90da16bf09570d9dc67ef1488aaa75334c559c4c71371527242c5511' ;; 		s390x) natsArch='s390x'; sha256='f6864ce2b8fe25359ff9a307fabc88201e113b8c57634be2893d7bfafe425525' ;; 		ppc64le) natsArch='ppc64le'; sha256='29c22b82c139baca9231c30f9a4a61f0f6df9407d67971c035a5ad45eb4296cf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0eb548ac9ea6536b78e8f022f0d54ddffc8ea698158ef2dd5c90e238cac65e`  
		Last Modified: Tue, 08 Apr 2025 20:43:16 GMT  
		Size: 6.1 MB (6112651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070f6b3e1d4c7ee5c34fe90575222c16cb533a5013090a2d96cf2fe15441e7fe`  
		Last Modified: Tue, 08 Apr 2025 20:43:16 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4bff1be241b9035bfdb6d41902299798fd8b8811fad836335944dc49920a79`  
		Last Modified: Tue, 08 Apr 2025 20:43:16 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:8e4df5e79b39eaed88cb71036fb80f61702f2601cc57b0e7fdab1f889bd113c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce86b2dc9ab5ee3ddbf5ef34cca1565cb9e233f1e4dad0dba95e8e2751f2fb2c`

```dockerfile
```

-	Layers:
	-	`sha256:2ae687dfeb6d4cccd84c06c540f9544bc669b3c193f9b98e10776a0dfb588e17`  
		Last Modified: Tue, 08 Apr 2025 20:43:16 GMT  
		Size: 13.2 KB (13166 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; s390x

```console
$ docker pull nats@sha256:80d526ba0a022ac0ecfbbdca744389216ff7c8399fc04ef39bd6e396687de0d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9941268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70204f740518f4ef8a7dd69d3c31dd799668f8e7e8d5d52e1f5256d137038688`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
ENV NATS_SERVER=2.10.27
# Tue, 08 Apr 2025 17:23:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='47067e41dc27890d9665ddf429ce24f9ed50bddd035dee63b915fcfcb1f8043b' ;; 		armhf) natsArch='arm6'; sha256='4e4268d1bb83568217f8dbce77d5e0ca93cea8282d6fef796b505cdd2b16cb64' ;; 		armv7) natsArch='arm7'; sha256='a1dc4d8ff0a1e61aa80c9b50f5aa45dac3a3126e70d0c2ae5f53119dcf697503' ;; 		x86_64) natsArch='amd64'; sha256='0c3f53edaf1acccc41866d49d9c3626c9de8c9138b2fc11bbadfd3a4eb544ef1' ;; 		x86) natsArch='386'; sha256='f6b515da90da16bf09570d9dc67ef1488aaa75334c559c4c71371527242c5511' ;; 		s390x) natsArch='s390x'; sha256='f6864ce2b8fe25359ff9a307fabc88201e113b8c57634be2893d7bfafe425525' ;; 		ppc64le) natsArch='ppc64le'; sha256='29c22b82c139baca9231c30f9a4a61f0f6df9407d67971c035a5ad45eb4296cf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c041fe5b245699ea36fdb48b91a9d8ebf8dc87e35168700ac1c6e8948e6af313`  
		Last Modified: Tue, 08 Apr 2025 22:05:03 GMT  
		Size: 6.5 MB (6472729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b5afb5bf0ac45f46d5b31544b015ea414b7d7448db9edcd0dec1f9eebeb2562`  
		Last Modified: Tue, 08 Apr 2025 22:05:02 GMT  
		Size: 563.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb6a7384e45593ad76154cb90a12af434edf7778649891b70375376eee4e9c9`  
		Last Modified: Tue, 08 Apr 2025 22:05:02 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:eed6bfa39f5936905bfc2f98abed09ae4372ed48ebf7a4c9786297f5ab631d69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:735f8f8452a47df4ff10c63c24dcedfa4647a11a7a26d2a5855451a9c35058cd`

```dockerfile
```

-	Layers:
	-	`sha256:10db7a231528e13d3ae0c5ebede33bc4beeb45f89d6e2cccfa6ce4eed84c27bd`  
		Last Modified: Tue, 08 Apr 2025 22:05:02 GMT  
		Size: 13.1 KB (13122 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-alpine3.21`

```console
$ docker pull nats@sha256:a369873a0c06bd111535b2a9f17fdff08372032d82d4cbf39e2e92ae8c4d158b
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
$ docker pull nats@sha256:7c595082cf89feecb72266d508dbee805293d22ef11c33feef2c36d53bf8129b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10275635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40dfcebf44e537b17b99074bbbae39852a43835cac98fb5db055c9957ec8bea8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
ENV NATS_SERVER=2.10.27
# Tue, 08 Apr 2025 17:23:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='47067e41dc27890d9665ddf429ce24f9ed50bddd035dee63b915fcfcb1f8043b' ;; 		armhf) natsArch='arm6'; sha256='4e4268d1bb83568217f8dbce77d5e0ca93cea8282d6fef796b505cdd2b16cb64' ;; 		armv7) natsArch='arm7'; sha256='a1dc4d8ff0a1e61aa80c9b50f5aa45dac3a3126e70d0c2ae5f53119dcf697503' ;; 		x86_64) natsArch='amd64'; sha256='0c3f53edaf1acccc41866d49d9c3626c9de8c9138b2fc11bbadfd3a4eb544ef1' ;; 		x86) natsArch='386'; sha256='f6b515da90da16bf09570d9dc67ef1488aaa75334c559c4c71371527242c5511' ;; 		s390x) natsArch='s390x'; sha256='f6864ce2b8fe25359ff9a307fabc88201e113b8c57634be2893d7bfafe425525' ;; 		ppc64le) natsArch='ppc64le'; sha256='29c22b82c139baca9231c30f9a4a61f0f6df9407d67971c035a5ad45eb4296cf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b418e663727e5b843db36fa727e22d92fb31bb99f1235e26dccfeb39750e0fa1`  
		Last Modified: Tue, 08 Apr 2025 20:28:15 GMT  
		Size: 6.6 MB (6632418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076c16eaada3cf6044d2362098bd6dedbdeb8506a826aeb10418ba41b6c55649`  
		Last Modified: Tue, 08 Apr 2025 20:28:15 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182cda9eb87b0b6df53ff5440502e2b7c3abdc0af53ef762bf3bda16a3c652e0`  
		Last Modified: Tue, 08 Apr 2025 20:28:15 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:bae31228d4a07f797e747d5d364ac169bd32a5b4f304f82cded49785b87c3865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3098b404f7af3eb2639f27bc50e6ee18a546586df54e768d10ec3e8649d19c1`

```dockerfile
```

-	Layers:
	-	`sha256:810b82eda42e704bfe9a436a96b272f32b793c1afc9cbcad6685ebd5f9d2e64a`  
		Last Modified: Tue, 08 Apr 2025 20:28:15 GMT  
		Size: 13.1 KB (13122 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:f4af69c51467ad969030a6285656c53a491fc03b8e442c30b897b1691439c471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9729296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db7b314b737c1720f822adbbefbcae87909929bf35a02b8d28a76fa7aeb01bc0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.10.28
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='78f9b382d468f7b683bf8bdda2c6276de1fd230d9d19724485f48b327d7ed4c2' ;; 		armhf) natsArch='arm6'; sha256='2a29a87abdec21bff9fb19a30aa06af12a6db31ec32d0b3de1a7c8bdeeb74b19' ;; 		armv7) natsArch='arm7'; sha256='837db6e72894993bde7f0e402f6f9dc151d8452b0441cea630260764bafd4c84' ;; 		x86_64) natsArch='amd64'; sha256='52e3baee2bf9cb4f3d362e293538e9f11ccfdb22ac9fbbd2bcad790e3ba41e3e' ;; 		x86) natsArch='386'; sha256='ffabdd7c124951b68ed4501223d5a877c3e90c5da68c27c884a58806eaa1c369' ;; 		s390x) natsArch='s390x'; sha256='f5627e4db5746200f62e6d5d9212dcfc59a4d4dc9cee30abf8eafdafac5445a1' ;; 		ppc64le) natsArch='ppc64le'; sha256='096424d6958c7b2798027208d0cc0c2ea5632e5530fd94d66712d586ca6d6d27' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e97974a6f36486b798da64002fc218b2233d353058852cffd0220594b01e269`  
		Last Modified: Fri, 25 Apr 2025 17:47:47 GMT  
		Size: 6.4 MB (6363595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb6a73b6e361505406303a8c7b3f3cfeba51010bf739aef7889bf7f0317a3b8`  
		Last Modified: Fri, 25 Apr 2025 17:47:46 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e222efd7d05fe8bcbda2e28970d7b05f8bb17ea70e7b7facf4701541d05df8`  
		Last Modified: Fri, 25 Apr 2025 17:47:46 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:5d34c1d5bed5a36593535f90aa950998957ae6a3d449899399f891679fa4ccb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05763aa76d78f8542ea1a12d8d75d8fe560b0dc4580158377ec49947c2b6d9cb`

```dockerfile
```

-	Layers:
	-	`sha256:27aef148734276a47a22fea3a763eeb98084a6604242d969b88cfa2ebba41576`  
		Last Modified: Fri, 25 Apr 2025 17:47:46 GMT  
		Size: 13.2 KB (13198 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:621f3f44322f8b79f9c90854c7a90a771165c16aa6d0e7974c79c101dbf23277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9443111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d811fdd54801fa7bfb080198ad7ef6ad0f572b8116d167e7fcafdc8fa3bd416`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
ENV NATS_SERVER=2.10.27
# Tue, 08 Apr 2025 17:23:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='47067e41dc27890d9665ddf429ce24f9ed50bddd035dee63b915fcfcb1f8043b' ;; 		armhf) natsArch='arm6'; sha256='4e4268d1bb83568217f8dbce77d5e0ca93cea8282d6fef796b505cdd2b16cb64' ;; 		armv7) natsArch='arm7'; sha256='a1dc4d8ff0a1e61aa80c9b50f5aa45dac3a3126e70d0c2ae5f53119dcf697503' ;; 		x86_64) natsArch='amd64'; sha256='0c3f53edaf1acccc41866d49d9c3626c9de8c9138b2fc11bbadfd3a4eb544ef1' ;; 		x86) natsArch='386'; sha256='f6b515da90da16bf09570d9dc67ef1488aaa75334c559c4c71371527242c5511' ;; 		s390x) natsArch='s390x'; sha256='f6864ce2b8fe25359ff9a307fabc88201e113b8c57634be2893d7bfafe425525' ;; 		ppc64le) natsArch='ppc64le'; sha256='29c22b82c139baca9231c30f9a4a61f0f6df9407d67971c035a5ad45eb4296cf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ecbba4e95d185ac65d0c976ec7b556783ec7a2c472f76f120b280418cb0086c`  
		Last Modified: Tue, 08 Apr 2025 20:32:21 GMT  
		Size: 6.3 MB (6344018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc57271692fbc3c72f3c7a7a018a4559f99357a43f63f6310b4933863caf445`  
		Last Modified: Tue, 08 Apr 2025 20:32:20 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28439e554ffc1776ef89b1a3cce85713e57c4f52c1839c9200c5122d14a69b72`  
		Last Modified: Tue, 08 Apr 2025 20:32:20 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:47c2e0842bde6cf10f7522a782753461a508494a2c2d0c7705de463304cfbfb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28a6b164add8300b5c9ca2618136d48ac0701896918b8215a43b18cfc8276aec`

```dockerfile
```

-	Layers:
	-	`sha256:5f67ac49cf858b21532ebd7b3ab2c3f96b8e6618096700d163b9c3aa1d7cff3c`  
		Last Modified: Tue, 08 Apr 2025 20:32:20 GMT  
		Size: 13.2 KB (13198 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:fb56b601a01e41e3fa3e1ec6882a5c7080064af2cbf8eebbe0aa8789057d7d65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10139926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c20275401ac1b6354f9bceea70fdbc9ea6b248f61de5860e8a48f4b9fa13449`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.10.28
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='78f9b382d468f7b683bf8bdda2c6276de1fd230d9d19724485f48b327d7ed4c2' ;; 		armhf) natsArch='arm6'; sha256='2a29a87abdec21bff9fb19a30aa06af12a6db31ec32d0b3de1a7c8bdeeb74b19' ;; 		armv7) natsArch='arm7'; sha256='837db6e72894993bde7f0e402f6f9dc151d8452b0441cea630260764bafd4c84' ;; 		x86_64) natsArch='amd64'; sha256='52e3baee2bf9cb4f3d362e293538e9f11ccfdb22ac9fbbd2bcad790e3ba41e3e' ;; 		x86) natsArch='386'; sha256='ffabdd7c124951b68ed4501223d5a877c3e90c5da68c27c884a58806eaa1c369' ;; 		s390x) natsArch='s390x'; sha256='f5627e4db5746200f62e6d5d9212dcfc59a4d4dc9cee30abf8eafdafac5445a1' ;; 		ppc64le) natsArch='ppc64le'; sha256='096424d6958c7b2798027208d0cc0c2ea5632e5530fd94d66712d586ca6d6d27' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d88dec44185a51ca27621bbb65e75ccd454b3c28c91009b2dde51a8ff3b55e`  
		Last Modified: Fri, 25 Apr 2025 17:47:42 GMT  
		Size: 6.1 MB (6145926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf91e9429cda3e96e24922bd3640282bad3965a0d6209055ac549cc49b5e0f8a`  
		Last Modified: Fri, 25 Apr 2025 17:47:41 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c6034f34091ef89d05c32fed01a7493f7c83cbbf10547c8aefac36a59fe368`  
		Last Modified: Fri, 25 Apr 2025 17:47:41 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:770428e58483a9652ac1bc757a92b38fb475e7802a1661bd0ee9bdbcc99a1a7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9fafe954b8c08a5febfa3873a84d9f621009fd0e4dc99eecd3c7d0e8a2ee129`

```dockerfile
```

-	Layers:
	-	`sha256:3d1465d1edfad8a9d270db627b7ae6ba90ac0fe85ef2e09550f0bd2a9ff67820`  
		Last Modified: Fri, 25 Apr 2025 17:47:41 GMT  
		Size: 13.2 KB (13226 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:4ccdae65f4f4d5a390b65d808cf366bf3356dc9570d9ed1dbe567de6f7aced46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9687965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae24adf477a3928acf9bb4015ae7dfd6e3ebb7bc64b5112a7748aaf8de2e6b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
ENV NATS_SERVER=2.10.27
# Tue, 08 Apr 2025 17:23:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='47067e41dc27890d9665ddf429ce24f9ed50bddd035dee63b915fcfcb1f8043b' ;; 		armhf) natsArch='arm6'; sha256='4e4268d1bb83568217f8dbce77d5e0ca93cea8282d6fef796b505cdd2b16cb64' ;; 		armv7) natsArch='arm7'; sha256='a1dc4d8ff0a1e61aa80c9b50f5aa45dac3a3126e70d0c2ae5f53119dcf697503' ;; 		x86_64) natsArch='amd64'; sha256='0c3f53edaf1acccc41866d49d9c3626c9de8c9138b2fc11bbadfd3a4eb544ef1' ;; 		x86) natsArch='386'; sha256='f6b515da90da16bf09570d9dc67ef1488aaa75334c559c4c71371527242c5511' ;; 		s390x) natsArch='s390x'; sha256='f6864ce2b8fe25359ff9a307fabc88201e113b8c57634be2893d7bfafe425525' ;; 		ppc64le) natsArch='ppc64le'; sha256='29c22b82c139baca9231c30f9a4a61f0f6df9407d67971c035a5ad45eb4296cf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0eb548ac9ea6536b78e8f022f0d54ddffc8ea698158ef2dd5c90e238cac65e`  
		Last Modified: Tue, 08 Apr 2025 20:43:16 GMT  
		Size: 6.1 MB (6112651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070f6b3e1d4c7ee5c34fe90575222c16cb533a5013090a2d96cf2fe15441e7fe`  
		Last Modified: Tue, 08 Apr 2025 20:43:16 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4bff1be241b9035bfdb6d41902299798fd8b8811fad836335944dc49920a79`  
		Last Modified: Tue, 08 Apr 2025 20:43:16 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:8e4df5e79b39eaed88cb71036fb80f61702f2601cc57b0e7fdab1f889bd113c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce86b2dc9ab5ee3ddbf5ef34cca1565cb9e233f1e4dad0dba95e8e2751f2fb2c`

```dockerfile
```

-	Layers:
	-	`sha256:2ae687dfeb6d4cccd84c06c540f9544bc669b3c193f9b98e10776a0dfb588e17`  
		Last Modified: Tue, 08 Apr 2025 20:43:16 GMT  
		Size: 13.2 KB (13166 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:80d526ba0a022ac0ecfbbdca744389216ff7c8399fc04ef39bd6e396687de0d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9941268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70204f740518f4ef8a7dd69d3c31dd799668f8e7e8d5d52e1f5256d137038688`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
ENV NATS_SERVER=2.10.27
# Tue, 08 Apr 2025 17:23:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='47067e41dc27890d9665ddf429ce24f9ed50bddd035dee63b915fcfcb1f8043b' ;; 		armhf) natsArch='arm6'; sha256='4e4268d1bb83568217f8dbce77d5e0ca93cea8282d6fef796b505cdd2b16cb64' ;; 		armv7) natsArch='arm7'; sha256='a1dc4d8ff0a1e61aa80c9b50f5aa45dac3a3126e70d0c2ae5f53119dcf697503' ;; 		x86_64) natsArch='amd64'; sha256='0c3f53edaf1acccc41866d49d9c3626c9de8c9138b2fc11bbadfd3a4eb544ef1' ;; 		x86) natsArch='386'; sha256='f6b515da90da16bf09570d9dc67ef1488aaa75334c559c4c71371527242c5511' ;; 		s390x) natsArch='s390x'; sha256='f6864ce2b8fe25359ff9a307fabc88201e113b8c57634be2893d7bfafe425525' ;; 		ppc64le) natsArch='ppc64le'; sha256='29c22b82c139baca9231c30f9a4a61f0f6df9407d67971c035a5ad45eb4296cf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c041fe5b245699ea36fdb48b91a9d8ebf8dc87e35168700ac1c6e8948e6af313`  
		Last Modified: Tue, 08 Apr 2025 22:05:03 GMT  
		Size: 6.5 MB (6472729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b5afb5bf0ac45f46d5b31544b015ea414b7d7448db9edcd0dec1f9eebeb2562`  
		Last Modified: Tue, 08 Apr 2025 22:05:02 GMT  
		Size: 563.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb6a7384e45593ad76154cb90a12af434edf7778649891b70375376eee4e9c9`  
		Last Modified: Tue, 08 Apr 2025 22:05:02 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:eed6bfa39f5936905bfc2f98abed09ae4372ed48ebf7a4c9786297f5ab631d69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:735f8f8452a47df4ff10c63c24dcedfa4647a11a7a26d2a5855451a9c35058cd`

```dockerfile
```

-	Layers:
	-	`sha256:10db7a231528e13d3ae0c5ebede33bc4beeb45f89d6e2cccfa6ce4eed84c27bd`  
		Last Modified: Tue, 08 Apr 2025 22:05:02 GMT  
		Size: 13.1 KB (13122 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-linux`

```console
$ docker pull nats@sha256:aa9edd55232bed7d9a8c0a20688499e331d9fb63eeb946b192d119e46c6fdc92
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
$ docker pull nats@sha256:eb025eeb0d8833044a3586a8f877482c5cae975cf0db03161d852efc1246a6af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6168774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d1f7c9f744161aacb847006fe289263073f3b614d1c3b26d77eb78c8cf81bc1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fa699494b4e64a703db8ad4671c9c07acbcebf379361896152b27f3c751db5ea`  
		Last Modified: Tue, 08 Apr 2025 17:26:15 GMT  
		Size: 6.2 MB (6168265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bcd18a1de501f0dcf00113b8c1effd2b7f198a1383c537490e8dce3a826adce`  
		Last Modified: Tue, 08 Apr 2025 21:07:44 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:c517a451e9619031d8c7624144f9ad61c5ce8fc44a6b98384b1be37db42a13aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a30f6e0f6a9c75dc1e119cc79f082306fbd1135b4623bcac32b4e69c5477c79`

```dockerfile
```

-	Layers:
	-	`sha256:c1f4c5ceb5f8a657b2f58404551421559687776ee014f879d1de5ebfcfc8dece`  
		Last Modified: Tue, 08 Apr 2025 21:07:44 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:7db0743b57a4c00470536801c63dab555cde243256324e65f52fa56f95e8d05c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5892863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:156b95545afd9f61a732db04e0e269ad8096a44d11fcba171f46f5fc09f10be8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f15bb1b47edf48e706d17c3e23b17de9fd17df8625ebe30db7b257f38601880b`  
		Last Modified: Tue, 08 Apr 2025 17:26:16 GMT  
		Size: 5.9 MB (5892353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c04ce8d443571bb4036f99c3781518adcf9060a99a5ea6831ea8f84166009fa`  
		Last Modified: Tue, 08 Apr 2025 21:07:19 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:15d9432cd998d8b87f997b05c593e27930683fdbc66928719c62ae4d0ec12dcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:720e7875f18f4349eb3b0fdfdbfd7286ff0c08f0429432b15bafee93e932bf74`

```dockerfile
```

-	Layers:
	-	`sha256:88029e21b6c24e65c3027c232c1081a99596ee9a2a06d32df17b3302efd1b906`  
		Last Modified: Tue, 08 Apr 2025 21:07:20 GMT  
		Size: 8.8 KB (8788 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:ee4e0314a0e7aea512e4a409b764dad958b834efa343dc2c9f43af51cd9f93f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5881346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a4be349c6c0f0343730c248084c65d1d6f47c18e3f8e0b451b2a081c18d2a59`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:dd82440cc0596353342b1677ea71d5175ec429a9b36ac37432305afd5db00b0c`  
		Last Modified: Tue, 08 Apr 2025 17:26:14 GMT  
		Size: 5.9 MB (5880837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53370f7d0e620e0c268408ebb6d4eb116cc5d1cb1116c38c4cfc478a97770c97`  
		Last Modified: Tue, 08 Apr 2025 21:25:18 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:b1befa3c23bdad19d294b5d73df0215bbf522fb002ba9e3910b085ed6010a672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2488e8a26c16d254d9b2c73a8f05bc4633e461cafb394be336c89b3d8e25385b`

```dockerfile
```

-	Layers:
	-	`sha256:22c87716fccba9922e3ab54d04c96d96849a07f9008c769d2e3c0c70d8aa5c4f`  
		Last Modified: Tue, 08 Apr 2025 21:25:18 GMT  
		Size: 8.8 KB (8789 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cbddc5491ac98646fe41ec6d0ddb64a8eeb7dfc7e39a7943ad6726cb34b7e53a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5671791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:695af0b5b248614722193c65c6610f25cb624e737ad6cada12d6e37ebce83468`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3e90cc5bec7d316417a1d1f6be7467d1ffc087233ec78f52ac78ab8830e3acea`  
		Last Modified: Tue, 08 Apr 2025 17:26:16 GMT  
		Size: 5.7 MB (5671283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7220a61a8a41868b70e67bdb239c254b16b0205ec13df5e994651ae989244cc8`  
		Last Modified: Wed, 09 Apr 2025 00:53:12 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:fe978136fb3f048731eae4c0049b4a6c7e1666d28e67cc5230db8ea3ff1330f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a4a78a719e6a4228f405f630420a6708c2fae6cca4dae826bfcfb5b7d105b46`

```dockerfile
```

-	Layers:
	-	`sha256:4e5927ac7d992740c9f913dcbd55ca3e49730c8e36ff5582baa08390ba8f6124`  
		Last Modified: Wed, 09 Apr 2025 00:53:12 GMT  
		Size: 8.8 KB (8824 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:4a615aba087255752db7335a6bc4249a0647cb418f579c74482db9abb86fae25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5649622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f2ce6cc279148f1f5bd10181203af2ebbd5ab6a72adb1cd14182022df01e79a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:34e405e5099052276a00bc13663d16e3de17abc6fc928997b78eab3bc6ba70c3`  
		Last Modified: Tue, 08 Apr 2025 17:26:11 GMT  
		Size: 5.6 MB (5649113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df44b2e202d4a27f74e605facd189d353c5221f85ec1ec8921e000d806f8aba2`  
		Last Modified: Tue, 08 Apr 2025 22:19:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:7b0abcba33ed78e06ef8539efa7d2f8e497f1a1e073dabe92eeb6b7921e05eaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1aa5a17256650818135e1acc93b601b5f73efdda407af6915ac035b2278439b`

```dockerfile
```

-	Layers:
	-	`sha256:1fdc46b1ea6a973250b0cb5fc1081608ff47e0ef6968275a7dbe62f66e9a1b80`  
		Last Modified: Tue, 08 Apr 2025 22:19:06 GMT  
		Size: 8.8 KB (8765 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; s390x

```console
$ docker pull nats@sha256:908f46d6f7d985bd1f0886839f21899dff78cbc2532bf80bb0af3885f5939698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6011225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02bf6f293b378ae455ac72206cbc16982912a66a96a1889f9ab0bb1e61652d68`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4df3046fee85d5087ea08a6ef49df55c38ddd7977f89e5073f536b8f0736b450`  
		Last Modified: Tue, 08 Apr 2025 17:26:14 GMT  
		Size: 6.0 MB (6010715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56724fa9fe9d3923fb6f5b9b821dbabbcce3213f51cac5dd418711765c5b1dc9`  
		Last Modified: Tue, 08 Apr 2025 22:08:16 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:09b3b37c386e69802fb1aab1352764f3bb00d31c4640fc88d2985d8fb0d6a98f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:427ab84d44e26941a1638adaca454bcd6c70232bf10994ece31a10d955adf2c5`

```dockerfile
```

-	Layers:
	-	`sha256:450d43c8eb4ce30507123a312630f9694cda7bbff21b8a86a48e4ba09049b69c`  
		Last Modified: Tue, 08 Apr 2025 22:08:16 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-nanoserver`

```console
$ docker pull nats@sha256:172b32815e8a701c212591a844c8de5b8ab5cb717b39b75b56094a131a0e5b4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `nats:2.10-nanoserver` - windows version 10.0.17763.7249; amd64

```console
$ docker pull nats@sha256:87b23809aa621f181b677e1c5a17da29d313a6a77b1d5d75f3b5a05f34ebce40
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 MB (115044774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce961ec5557c6d1b57877c9594add188039f9cd34dd7a53cede119a9c2a48f0d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Fri, 18 Apr 2025 04:13:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 18 Apr 2025 04:13:42 GMT
RUN cmd /S /C #(nop) COPY file:911e7fad0174090a7de06fb3b7fca63c95843409a6ad46e295d2fe4da8d99d2a in C:\nats-server.exe 
# Fri, 18 Apr 2025 04:13:42 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Fri, 18 Apr 2025 04:13:43 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 18 Apr 2025 04:13:43 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 18 Apr 2025 04:13:44 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:581d68c582ecb4e34ebbf95721dde6c0dad76f87dffcf1b2a281a068e7c997b2`  
		Last Modified: Fri, 18 Apr 2025 04:13:47 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dacc779fecd4cecc205cc8b50de0a3f71c9251adb342ad22bedefcb3b971d889`  
		Last Modified: Fri, 18 Apr 2025 04:13:47 GMT  
		Size: 6.3 MB (6286707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec94aed503ca0a62740a2ad52a1f3572585c0afd9d51f366dee00e232097ce1`  
		Last Modified: Fri, 18 Apr 2025 04:13:46 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60d81dd7de5c54597a8c47ee90f1f2d2743a987da2e7b0859f2889658673db7a`  
		Last Modified: Fri, 18 Apr 2025 04:13:46 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d93759a1c81017eaad5721c68a97202528074ab706a10309bc3a564a87d630c`  
		Last Modified: Fri, 18 Apr 2025 04:13:46 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7115d3cfeddee720c6c7f4d7c65d6bd8676389e9e44d59afacd0a722a3da6c`  
		Last Modified: Fri, 18 Apr 2025 04:13:46 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-nanoserver-1809`

```console
$ docker pull nats@sha256:172b32815e8a701c212591a844c8de5b8ab5cb717b39b75b56094a131a0e5b4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `nats:2.10-nanoserver-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull nats@sha256:87b23809aa621f181b677e1c5a17da29d313a6a77b1d5d75f3b5a05f34ebce40
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 MB (115044774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce961ec5557c6d1b57877c9594add188039f9cd34dd7a53cede119a9c2a48f0d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Fri, 18 Apr 2025 04:13:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 18 Apr 2025 04:13:42 GMT
RUN cmd /S /C #(nop) COPY file:911e7fad0174090a7de06fb3b7fca63c95843409a6ad46e295d2fe4da8d99d2a in C:\nats-server.exe 
# Fri, 18 Apr 2025 04:13:42 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Fri, 18 Apr 2025 04:13:43 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 18 Apr 2025 04:13:43 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 18 Apr 2025 04:13:44 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:581d68c582ecb4e34ebbf95721dde6c0dad76f87dffcf1b2a281a068e7c997b2`  
		Last Modified: Fri, 18 Apr 2025 04:13:47 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dacc779fecd4cecc205cc8b50de0a3f71c9251adb342ad22bedefcb3b971d889`  
		Last Modified: Fri, 18 Apr 2025 04:13:47 GMT  
		Size: 6.3 MB (6286707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec94aed503ca0a62740a2ad52a1f3572585c0afd9d51f366dee00e232097ce1`  
		Last Modified: Fri, 18 Apr 2025 04:13:46 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60d81dd7de5c54597a8c47ee90f1f2d2743a987da2e7b0859f2889658673db7a`  
		Last Modified: Fri, 18 Apr 2025 04:13:46 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d93759a1c81017eaad5721c68a97202528074ab706a10309bc3a564a87d630c`  
		Last Modified: Fri, 18 Apr 2025 04:13:46 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7115d3cfeddee720c6c7f4d7c65d6bd8676389e9e44d59afacd0a722a3da6c`  
		Last Modified: Fri, 18 Apr 2025 04:13:46 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-scratch`

```console
$ docker pull nats@sha256:aa9edd55232bed7d9a8c0a20688499e331d9fb63eeb946b192d119e46c6fdc92
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
$ docker pull nats@sha256:eb025eeb0d8833044a3586a8f877482c5cae975cf0db03161d852efc1246a6af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6168774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d1f7c9f744161aacb847006fe289263073f3b614d1c3b26d77eb78c8cf81bc1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fa699494b4e64a703db8ad4671c9c07acbcebf379361896152b27f3c751db5ea`  
		Last Modified: Tue, 08 Apr 2025 17:26:15 GMT  
		Size: 6.2 MB (6168265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bcd18a1de501f0dcf00113b8c1effd2b7f198a1383c537490e8dce3a826adce`  
		Last Modified: Tue, 08 Apr 2025 21:07:44 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:c517a451e9619031d8c7624144f9ad61c5ce8fc44a6b98384b1be37db42a13aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a30f6e0f6a9c75dc1e119cc79f082306fbd1135b4623bcac32b4e69c5477c79`

```dockerfile
```

-	Layers:
	-	`sha256:c1f4c5ceb5f8a657b2f58404551421559687776ee014f879d1de5ebfcfc8dece`  
		Last Modified: Tue, 08 Apr 2025 21:07:44 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:7db0743b57a4c00470536801c63dab555cde243256324e65f52fa56f95e8d05c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5892863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:156b95545afd9f61a732db04e0e269ad8096a44d11fcba171f46f5fc09f10be8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f15bb1b47edf48e706d17c3e23b17de9fd17df8625ebe30db7b257f38601880b`  
		Last Modified: Tue, 08 Apr 2025 17:26:16 GMT  
		Size: 5.9 MB (5892353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c04ce8d443571bb4036f99c3781518adcf9060a99a5ea6831ea8f84166009fa`  
		Last Modified: Tue, 08 Apr 2025 21:07:19 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:15d9432cd998d8b87f997b05c593e27930683fdbc66928719c62ae4d0ec12dcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:720e7875f18f4349eb3b0fdfdbfd7286ff0c08f0429432b15bafee93e932bf74`

```dockerfile
```

-	Layers:
	-	`sha256:88029e21b6c24e65c3027c232c1081a99596ee9a2a06d32df17b3302efd1b906`  
		Last Modified: Tue, 08 Apr 2025 21:07:20 GMT  
		Size: 8.8 KB (8788 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:ee4e0314a0e7aea512e4a409b764dad958b834efa343dc2c9f43af51cd9f93f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5881346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a4be349c6c0f0343730c248084c65d1d6f47c18e3f8e0b451b2a081c18d2a59`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:dd82440cc0596353342b1677ea71d5175ec429a9b36ac37432305afd5db00b0c`  
		Last Modified: Tue, 08 Apr 2025 17:26:14 GMT  
		Size: 5.9 MB (5880837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53370f7d0e620e0c268408ebb6d4eb116cc5d1cb1116c38c4cfc478a97770c97`  
		Last Modified: Tue, 08 Apr 2025 21:25:18 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:b1befa3c23bdad19d294b5d73df0215bbf522fb002ba9e3910b085ed6010a672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2488e8a26c16d254d9b2c73a8f05bc4633e461cafb394be336c89b3d8e25385b`

```dockerfile
```

-	Layers:
	-	`sha256:22c87716fccba9922e3ab54d04c96d96849a07f9008c769d2e3c0c70d8aa5c4f`  
		Last Modified: Tue, 08 Apr 2025 21:25:18 GMT  
		Size: 8.8 KB (8789 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cbddc5491ac98646fe41ec6d0ddb64a8eeb7dfc7e39a7943ad6726cb34b7e53a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5671791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:695af0b5b248614722193c65c6610f25cb624e737ad6cada12d6e37ebce83468`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3e90cc5bec7d316417a1d1f6be7467d1ffc087233ec78f52ac78ab8830e3acea`  
		Last Modified: Tue, 08 Apr 2025 17:26:16 GMT  
		Size: 5.7 MB (5671283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7220a61a8a41868b70e67bdb239c254b16b0205ec13df5e994651ae989244cc8`  
		Last Modified: Wed, 09 Apr 2025 00:53:12 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:fe978136fb3f048731eae4c0049b4a6c7e1666d28e67cc5230db8ea3ff1330f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a4a78a719e6a4228f405f630420a6708c2fae6cca4dae826bfcfb5b7d105b46`

```dockerfile
```

-	Layers:
	-	`sha256:4e5927ac7d992740c9f913dcbd55ca3e49730c8e36ff5582baa08390ba8f6124`  
		Last Modified: Wed, 09 Apr 2025 00:53:12 GMT  
		Size: 8.8 KB (8824 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:4a615aba087255752db7335a6bc4249a0647cb418f579c74482db9abb86fae25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5649622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f2ce6cc279148f1f5bd10181203af2ebbd5ab6a72adb1cd14182022df01e79a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:34e405e5099052276a00bc13663d16e3de17abc6fc928997b78eab3bc6ba70c3`  
		Last Modified: Tue, 08 Apr 2025 17:26:11 GMT  
		Size: 5.6 MB (5649113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df44b2e202d4a27f74e605facd189d353c5221f85ec1ec8921e000d806f8aba2`  
		Last Modified: Tue, 08 Apr 2025 22:19:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:7b0abcba33ed78e06ef8539efa7d2f8e497f1a1e073dabe92eeb6b7921e05eaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1aa5a17256650818135e1acc93b601b5f73efdda407af6915ac035b2278439b`

```dockerfile
```

-	Layers:
	-	`sha256:1fdc46b1ea6a973250b0cb5fc1081608ff47e0ef6968275a7dbe62f66e9a1b80`  
		Last Modified: Tue, 08 Apr 2025 22:19:06 GMT  
		Size: 8.8 KB (8765 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; s390x

```console
$ docker pull nats@sha256:908f46d6f7d985bd1f0886839f21899dff78cbc2532bf80bb0af3885f5939698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6011225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02bf6f293b378ae455ac72206cbc16982912a66a96a1889f9ab0bb1e61652d68`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4df3046fee85d5087ea08a6ef49df55c38ddd7977f89e5073f536b8f0736b450`  
		Last Modified: Tue, 08 Apr 2025 17:26:14 GMT  
		Size: 6.0 MB (6010715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56724fa9fe9d3923fb6f5b9b821dbabbcce3213f51cac5dd418711765c5b1dc9`  
		Last Modified: Tue, 08 Apr 2025 22:08:16 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:09b3b37c386e69802fb1aab1352764f3bb00d31c4640fc88d2985d8fb0d6a98f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:427ab84d44e26941a1638adaca454bcd6c70232bf10994ece31a10d955adf2c5`

```dockerfile
```

-	Layers:
	-	`sha256:450d43c8eb4ce30507123a312630f9694cda7bbff21b8a86a48e4ba09049b69c`  
		Last Modified: Tue, 08 Apr 2025 22:08:16 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-windowsservercore`

```console
$ docker pull nats@sha256:5ff21d5b5603d3c2c8e9200060c8a7a5c892fa3ce940cf9d804a065fe9f22ef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `nats:2.10-windowsservercore` - windows version 10.0.17763.7249; amd64

```console
$ docker pull nats@sha256:d691a0780c6f46990a34034bca3075fcdd1677f0257104abcb1758aafc3d73ff
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2172486422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6131715dc519f9f506b2d1a1a79e6aa1acb8a57047c5614ee47d0bf1ec43a3b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Fri, 18 Apr 2025 03:11:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 18 Apr 2025 03:11:22 GMT
ENV NATS_DOCKERIZED=1
# Fri, 18 Apr 2025 03:11:23 GMT
ENV NATS_SERVER=2.10.27
# Fri, 18 Apr 2025 03:11:24 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.27/nats-server-v2.10.27-windows-amd64.zip
# Fri, 18 Apr 2025 03:11:24 GMT
ENV NATS_SERVER_SHASUM=f7033b98f4e063cc4790e3a1ec4853f2f5f6a474fea6090de8a04f851d46e277
# Fri, 18 Apr 2025 03:11:41 GMT
RUN Set-PSDebug -Trace 2
# Fri, 18 Apr 2025 03:11:57 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 18 Apr 2025 03:11:58 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Fri, 18 Apr 2025 03:11:58 GMT
EXPOSE 4222 6222 8222
# Fri, 18 Apr 2025 03:11:59 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 18 Apr 2025 03:12:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Fri, 18 Apr 2025 03:13:03 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6791c0db10f65d44afb15ac7abbe3073370c618ef3a888ec1815caeb3f561f2`  
		Last Modified: Fri, 18 Apr 2025 03:12:08 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea2f486fafa94abdf3bfcb27678b258d267463a636c1a341aad3396611bfbfa`  
		Last Modified: Fri, 18 Apr 2025 03:12:08 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d80b28ee9129daa260f6f0d99d363e153afd03fed931ac4ef92c525ec269e05a`  
		Last Modified: Fri, 18 Apr 2025 03:12:06 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dcf7d681671994fa79b504e890e7b5e6e876357cf1380f6c618997066644e38`  
		Last Modified: Fri, 18 Apr 2025 03:12:06 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d64c456212bb2cb69bfaa3321d71ae910e48ae9c92a3bfcae50b39e909d593e9`  
		Last Modified: Fri, 18 Apr 2025 03:12:06 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0965c8b55d50fe15d854c99481dc0034169f8c05c49a15fb61b432027d0b9bdd`  
		Last Modified: Fri, 18 Apr 2025 03:12:06 GMT  
		Size: 325.8 KB (325773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e80856eb636d5211c9d6af7e055a42a18ea656e9c523825636832322a90e9a`  
		Last Modified: Fri, 18 Apr 2025 03:12:05 GMT  
		Size: 6.6 MB (6622626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3efeef9de85538a2e71962c7f60e8e42413c83bc13fed0ed50db0563b83b026f`  
		Last Modified: Fri, 18 Apr 2025 03:12:04 GMT  
		Size: 1.9 KB (1868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:535de5f2e65cc08817faba0408b6b28d88839948f69fdb0ef9573a9603590d7b`  
		Last Modified: Fri, 18 Apr 2025 03:12:04 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea6c18c17908edbbade5b74ab604b6bad59f6fd85ebaf98dc12a907412ae13a`  
		Last Modified: Fri, 18 Apr 2025 03:12:04 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67c00a61488349c3fd978c59419416d65706ee0687ce152ebe3fd8f36bbd0797`  
		Last Modified: Fri, 18 Apr 2025 03:12:04 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-windowsservercore-1809`

```console
$ docker pull nats@sha256:5ff21d5b5603d3c2c8e9200060c8a7a5c892fa3ce940cf9d804a065fe9f22ef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `nats:2.10-windowsservercore-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull nats@sha256:d691a0780c6f46990a34034bca3075fcdd1677f0257104abcb1758aafc3d73ff
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2172486422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6131715dc519f9f506b2d1a1a79e6aa1acb8a57047c5614ee47d0bf1ec43a3b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Fri, 18 Apr 2025 03:11:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 18 Apr 2025 03:11:22 GMT
ENV NATS_DOCKERIZED=1
# Fri, 18 Apr 2025 03:11:23 GMT
ENV NATS_SERVER=2.10.27
# Fri, 18 Apr 2025 03:11:24 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.27/nats-server-v2.10.27-windows-amd64.zip
# Fri, 18 Apr 2025 03:11:24 GMT
ENV NATS_SERVER_SHASUM=f7033b98f4e063cc4790e3a1ec4853f2f5f6a474fea6090de8a04f851d46e277
# Fri, 18 Apr 2025 03:11:41 GMT
RUN Set-PSDebug -Trace 2
# Fri, 18 Apr 2025 03:11:57 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 18 Apr 2025 03:11:58 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Fri, 18 Apr 2025 03:11:58 GMT
EXPOSE 4222 6222 8222
# Fri, 18 Apr 2025 03:11:59 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 18 Apr 2025 03:12:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Fri, 18 Apr 2025 03:13:03 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6791c0db10f65d44afb15ac7abbe3073370c618ef3a888ec1815caeb3f561f2`  
		Last Modified: Fri, 18 Apr 2025 03:12:08 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea2f486fafa94abdf3bfcb27678b258d267463a636c1a341aad3396611bfbfa`  
		Last Modified: Fri, 18 Apr 2025 03:12:08 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d80b28ee9129daa260f6f0d99d363e153afd03fed931ac4ef92c525ec269e05a`  
		Last Modified: Fri, 18 Apr 2025 03:12:06 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dcf7d681671994fa79b504e890e7b5e6e876357cf1380f6c618997066644e38`  
		Last Modified: Fri, 18 Apr 2025 03:12:06 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d64c456212bb2cb69bfaa3321d71ae910e48ae9c92a3bfcae50b39e909d593e9`  
		Last Modified: Fri, 18 Apr 2025 03:12:06 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0965c8b55d50fe15d854c99481dc0034169f8c05c49a15fb61b432027d0b9bdd`  
		Last Modified: Fri, 18 Apr 2025 03:12:06 GMT  
		Size: 325.8 KB (325773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e80856eb636d5211c9d6af7e055a42a18ea656e9c523825636832322a90e9a`  
		Last Modified: Fri, 18 Apr 2025 03:12:05 GMT  
		Size: 6.6 MB (6622626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3efeef9de85538a2e71962c7f60e8e42413c83bc13fed0ed50db0563b83b026f`  
		Last Modified: Fri, 18 Apr 2025 03:12:04 GMT  
		Size: 1.9 KB (1868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:535de5f2e65cc08817faba0408b6b28d88839948f69fdb0ef9573a9603590d7b`  
		Last Modified: Fri, 18 Apr 2025 03:12:04 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea6c18c17908edbbade5b74ab604b6bad59f6fd85ebaf98dc12a907412ae13a`  
		Last Modified: Fri, 18 Apr 2025 03:12:04 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67c00a61488349c3fd978c59419416d65706ee0687ce152ebe3fd8f36bbd0797`  
		Last Modified: Fri, 18 Apr 2025 03:12:04 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.28`

```console
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `nats:2.10.28-alpine`

```console
$ docker pull nats@sha256:c775829f858308be0fe9020fd3ac94ce16bcf7ee4cd511505fedd4829a375eb8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `nats:2.10.28-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:f4af69c51467ad969030a6285656c53a491fc03b8e442c30b897b1691439c471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9729296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db7b314b737c1720f822adbbefbcae87909929bf35a02b8d28a76fa7aeb01bc0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.10.28
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='78f9b382d468f7b683bf8bdda2c6276de1fd230d9d19724485f48b327d7ed4c2' ;; 		armhf) natsArch='arm6'; sha256='2a29a87abdec21bff9fb19a30aa06af12a6db31ec32d0b3de1a7c8bdeeb74b19' ;; 		armv7) natsArch='arm7'; sha256='837db6e72894993bde7f0e402f6f9dc151d8452b0441cea630260764bafd4c84' ;; 		x86_64) natsArch='amd64'; sha256='52e3baee2bf9cb4f3d362e293538e9f11ccfdb22ac9fbbd2bcad790e3ba41e3e' ;; 		x86) natsArch='386'; sha256='ffabdd7c124951b68ed4501223d5a877c3e90c5da68c27c884a58806eaa1c369' ;; 		s390x) natsArch='s390x'; sha256='f5627e4db5746200f62e6d5d9212dcfc59a4d4dc9cee30abf8eafdafac5445a1' ;; 		ppc64le) natsArch='ppc64le'; sha256='096424d6958c7b2798027208d0cc0c2ea5632e5530fd94d66712d586ca6d6d27' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e97974a6f36486b798da64002fc218b2233d353058852cffd0220594b01e269`  
		Last Modified: Fri, 25 Apr 2025 17:47:47 GMT  
		Size: 6.4 MB (6363595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb6a73b6e361505406303a8c7b3f3cfeba51010bf739aef7889bf7f0317a3b8`  
		Last Modified: Fri, 25 Apr 2025 17:47:46 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e222efd7d05fe8bcbda2e28970d7b05f8bb17ea70e7b7facf4701541d05df8`  
		Last Modified: Fri, 25 Apr 2025 17:47:46 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.28-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:5d34c1d5bed5a36593535f90aa950998957ae6a3d449899399f891679fa4ccb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05763aa76d78f8542ea1a12d8d75d8fe560b0dc4580158377ec49947c2b6d9cb`

```dockerfile
```

-	Layers:
	-	`sha256:27aef148734276a47a22fea3a763eeb98084a6604242d969b88cfa2ebba41576`  
		Last Modified: Fri, 25 Apr 2025 17:47:46 GMT  
		Size: 13.2 KB (13198 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.28-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:fb56b601a01e41e3fa3e1ec6882a5c7080064af2cbf8eebbe0aa8789057d7d65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10139926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c20275401ac1b6354f9bceea70fdbc9ea6b248f61de5860e8a48f4b9fa13449`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.10.28
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='78f9b382d468f7b683bf8bdda2c6276de1fd230d9d19724485f48b327d7ed4c2' ;; 		armhf) natsArch='arm6'; sha256='2a29a87abdec21bff9fb19a30aa06af12a6db31ec32d0b3de1a7c8bdeeb74b19' ;; 		armv7) natsArch='arm7'; sha256='837db6e72894993bde7f0e402f6f9dc151d8452b0441cea630260764bafd4c84' ;; 		x86_64) natsArch='amd64'; sha256='52e3baee2bf9cb4f3d362e293538e9f11ccfdb22ac9fbbd2bcad790e3ba41e3e' ;; 		x86) natsArch='386'; sha256='ffabdd7c124951b68ed4501223d5a877c3e90c5da68c27c884a58806eaa1c369' ;; 		s390x) natsArch='s390x'; sha256='f5627e4db5746200f62e6d5d9212dcfc59a4d4dc9cee30abf8eafdafac5445a1' ;; 		ppc64le) natsArch='ppc64le'; sha256='096424d6958c7b2798027208d0cc0c2ea5632e5530fd94d66712d586ca6d6d27' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d88dec44185a51ca27621bbb65e75ccd454b3c28c91009b2dde51a8ff3b55e`  
		Last Modified: Fri, 25 Apr 2025 17:47:42 GMT  
		Size: 6.1 MB (6145926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf91e9429cda3e96e24922bd3640282bad3965a0d6209055ac549cc49b5e0f8a`  
		Last Modified: Fri, 25 Apr 2025 17:47:41 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c6034f34091ef89d05c32fed01a7493f7c83cbbf10547c8aefac36a59fe368`  
		Last Modified: Fri, 25 Apr 2025 17:47:41 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.28-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:770428e58483a9652ac1bc757a92b38fb475e7802a1661bd0ee9bdbcc99a1a7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9fafe954b8c08a5febfa3873a84d9f621009fd0e4dc99eecd3c7d0e8a2ee129`

```dockerfile
```

-	Layers:
	-	`sha256:3d1465d1edfad8a9d270db627b7ae6ba90ac0fe85ef2e09550f0bd2a9ff67820`  
		Last Modified: Fri, 25 Apr 2025 17:47:41 GMT  
		Size: 13.2 KB (13226 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.28-alpine3.21`

```console
$ docker pull nats@sha256:c775829f858308be0fe9020fd3ac94ce16bcf7ee4cd511505fedd4829a375eb8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `nats:2.10.28-alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:f4af69c51467ad969030a6285656c53a491fc03b8e442c30b897b1691439c471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9729296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db7b314b737c1720f822adbbefbcae87909929bf35a02b8d28a76fa7aeb01bc0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.10.28
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='78f9b382d468f7b683bf8bdda2c6276de1fd230d9d19724485f48b327d7ed4c2' ;; 		armhf) natsArch='arm6'; sha256='2a29a87abdec21bff9fb19a30aa06af12a6db31ec32d0b3de1a7c8bdeeb74b19' ;; 		armv7) natsArch='arm7'; sha256='837db6e72894993bde7f0e402f6f9dc151d8452b0441cea630260764bafd4c84' ;; 		x86_64) natsArch='amd64'; sha256='52e3baee2bf9cb4f3d362e293538e9f11ccfdb22ac9fbbd2bcad790e3ba41e3e' ;; 		x86) natsArch='386'; sha256='ffabdd7c124951b68ed4501223d5a877c3e90c5da68c27c884a58806eaa1c369' ;; 		s390x) natsArch='s390x'; sha256='f5627e4db5746200f62e6d5d9212dcfc59a4d4dc9cee30abf8eafdafac5445a1' ;; 		ppc64le) natsArch='ppc64le'; sha256='096424d6958c7b2798027208d0cc0c2ea5632e5530fd94d66712d586ca6d6d27' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e97974a6f36486b798da64002fc218b2233d353058852cffd0220594b01e269`  
		Last Modified: Fri, 25 Apr 2025 17:47:47 GMT  
		Size: 6.4 MB (6363595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb6a73b6e361505406303a8c7b3f3cfeba51010bf739aef7889bf7f0317a3b8`  
		Last Modified: Fri, 25 Apr 2025 17:47:46 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e222efd7d05fe8bcbda2e28970d7b05f8bb17ea70e7b7facf4701541d05df8`  
		Last Modified: Fri, 25 Apr 2025 17:47:46 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.28-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:5d34c1d5bed5a36593535f90aa950998957ae6a3d449899399f891679fa4ccb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05763aa76d78f8542ea1a12d8d75d8fe560b0dc4580158377ec49947c2b6d9cb`

```dockerfile
```

-	Layers:
	-	`sha256:27aef148734276a47a22fea3a763eeb98084a6604242d969b88cfa2ebba41576`  
		Last Modified: Fri, 25 Apr 2025 17:47:46 GMT  
		Size: 13.2 KB (13198 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.28-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:fb56b601a01e41e3fa3e1ec6882a5c7080064af2cbf8eebbe0aa8789057d7d65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10139926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c20275401ac1b6354f9bceea70fdbc9ea6b248f61de5860e8a48f4b9fa13449`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.10.28
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='78f9b382d468f7b683bf8bdda2c6276de1fd230d9d19724485f48b327d7ed4c2' ;; 		armhf) natsArch='arm6'; sha256='2a29a87abdec21bff9fb19a30aa06af12a6db31ec32d0b3de1a7c8bdeeb74b19' ;; 		armv7) natsArch='arm7'; sha256='837db6e72894993bde7f0e402f6f9dc151d8452b0441cea630260764bafd4c84' ;; 		x86_64) natsArch='amd64'; sha256='52e3baee2bf9cb4f3d362e293538e9f11ccfdb22ac9fbbd2bcad790e3ba41e3e' ;; 		x86) natsArch='386'; sha256='ffabdd7c124951b68ed4501223d5a877c3e90c5da68c27c884a58806eaa1c369' ;; 		s390x) natsArch='s390x'; sha256='f5627e4db5746200f62e6d5d9212dcfc59a4d4dc9cee30abf8eafdafac5445a1' ;; 		ppc64le) natsArch='ppc64le'; sha256='096424d6958c7b2798027208d0cc0c2ea5632e5530fd94d66712d586ca6d6d27' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d88dec44185a51ca27621bbb65e75ccd454b3c28c91009b2dde51a8ff3b55e`  
		Last Modified: Fri, 25 Apr 2025 17:47:42 GMT  
		Size: 6.1 MB (6145926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf91e9429cda3e96e24922bd3640282bad3965a0d6209055ac549cc49b5e0f8a`  
		Last Modified: Fri, 25 Apr 2025 17:47:41 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c6034f34091ef89d05c32fed01a7493f7c83cbbf10547c8aefac36a59fe368`  
		Last Modified: Fri, 25 Apr 2025 17:47:41 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.28-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:770428e58483a9652ac1bc757a92b38fb475e7802a1661bd0ee9bdbcc99a1a7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9fafe954b8c08a5febfa3873a84d9f621009fd0e4dc99eecd3c7d0e8a2ee129`

```dockerfile
```

-	Layers:
	-	`sha256:3d1465d1edfad8a9d270db627b7ae6ba90ac0fe85ef2e09550f0bd2a9ff67820`  
		Last Modified: Fri, 25 Apr 2025 17:47:41 GMT  
		Size: 13.2 KB (13226 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.28-linux`

```console
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `nats:2.10.28-nanoserver`

```console
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `nats:2.10.28-nanoserver-1809`

```console
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `nats:2.10.28-scratch`

```console
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `nats:2.10.28-windowsservercore`

```console
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `nats:2.10.28-windowsservercore-1809`

```console
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `nats:2.11`

```console
$ docker pull nats@sha256:29ae7f55fbaa9d23949237c58593a3451ef74493e5b3644d6a837219d1d4028c
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
	-	windows version 10.0.17763.7249; amd64

### `nats:2.11` - linux; amd64

```console
$ docker pull nats@sha256:41dddbc7a9265892086db802a374dbf910b5d0db786c8ba12e27a81f2ede8f05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6282680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ddda49ccc5be8fc53872fcb74f0f168368af1d3e5fc27fd096bb4ab9fac9e5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7a31ab99389a11bb36db183df5a6bc8d784c1e96fb10c1973e04b98e17e58f51`  
		Last Modified: Tue, 08 Apr 2025 17:26:21 GMT  
		Size: 6.3 MB (6282171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bcd18a1de501f0dcf00113b8c1effd2b7f198a1383c537490e8dce3a826adce`  
		Last Modified: Tue, 08 Apr 2025 21:07:44 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:16692b029d2fd73a6c9833d59190a10a052903fbc5b68228ca0ce31e25895ee4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a60659f991d784a3586e62308c55e27054bad66d740cbde49980328b682cb858`

```dockerfile
```

-	Layers:
	-	`sha256:d0fd9d7883ec1e99c1a17109b0a6fd39dec7b9ec8f40f0ace2f2c15f9d8846a3`  
		Last Modified: Tue, 08 Apr 2025 21:07:45 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; arm variant v6

```console
$ docker pull nats@sha256:f53994879dbfd2fc8177b383905d33db1095d8b42bb4bec64088771cecdb2bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6002072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01de3b3fb48e4b75539a9af5640e6f77115cdbe9419f3da2891472ec6e806148`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bc9bfb085b797367e9407dbdf5a3928ee0d69859fb96188165856b5e8e1b6e88`  
		Last Modified: Tue, 08 Apr 2025 17:26:22 GMT  
		Size: 6.0 MB (6001563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef30b0264d904d40fbf4763922653522d80a800c24f6bcbb52a1a66fd1accaf8`  
		Last Modified: Tue, 08 Apr 2025 21:07:08 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:f9537be10194b98f78298fad26add4a04948857f650479e674587da738dcf69c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7014bcdaac4c9653a29f6fc739854477633a62a69bd0cba053bbeecbfc57e101`

```dockerfile
```

-	Layers:
	-	`sha256:e337d587115a4b810f5a9fa3deb1db109744f3828488f355e6bfa4c965ea5501`  
		Last Modified: Tue, 08 Apr 2025 21:07:08 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; arm variant v7

```console
$ docker pull nats@sha256:859b07690a2059b52277aceb9feed7e81269aed09859f1c3b0f3162d751ddb29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5992346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e38aded7ecfd1e1b61cc0452d01e01718e0a4be4ee666ac1980ddacb6f7defbc`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8f114aa547686a4604d8f5fbabd3d89b59a801cc55b68aa653d813c66ca32a65`  
		Last Modified: Tue, 08 Apr 2025 17:26:18 GMT  
		Size: 6.0 MB (5991835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844018e59249593be5d829b3a4bba323e96c26297db204b3a8a8a52e847f8041`  
		Last Modified: Tue, 08 Apr 2025 21:25:07 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:1e53207f824b4b97a2158a01c60662ef62ff32a777e55e615077563d48bcc314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a229febf9f435367bc3df4661afe24971b0581fa0b4b375a92d4ac38c3ce791`

```dockerfile
```

-	Layers:
	-	`sha256:36f6e0df21021319068725c9d7c2325e4fad06927e5ff9fe7fe11ec830f17f1c`  
		Last Modified: Tue, 08 Apr 2025 21:25:06 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:9142b78e748793c9e3b2fda3ac3800e66e866bf0147d634a7aea592f973a023a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5776867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee76a21b5d66ec40c0c8c53a6af4ed91124f7a2820ab80bf20279efdc3e689c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6b90b986da10be1b936fe6989055b49edb315427df0ceb03d1dd2f9dd98fb88`  
		Last Modified: Tue, 08 Apr 2025 17:26:18 GMT  
		Size: 5.8 MB (5776357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5e46c8b1d8619650c3d1afbfcf70b02949ce40d6fd6eb7d769bdc98a1def25`  
		Last Modified: Wed, 09 Apr 2025 00:53:02 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:9f289daca75844d624973e2b4e4a78db9e2026bfd59d743648f68e3c13d32a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53971055b1ebeea168a941b88f41f089dd9886aa55cbebe6b4f12f98ddb49666`

```dockerfile
```

-	Layers:
	-	`sha256:a65f769c9cecfc76c232cf377b8548ffd7fc82eae67b781487e0924b3319a183`  
		Last Modified: Wed, 09 Apr 2025 00:53:02 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; ppc64le

```console
$ docker pull nats@sha256:8cbd8caa2bdb9c64319ae113af4cf4170b92f3795148cb20401f2f1f16aa1d11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5757631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ba2ae7e87afe027065399c01f1230c431bed76a811a5cc5c83e971b6e70a26`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2c03c8b47070105a3781cfd93e5a048f0fcf1895182b8500a1875b914beccc2b`  
		Last Modified: Tue, 08 Apr 2025 17:26:19 GMT  
		Size: 5.8 MB (5757122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425937f6cd03177f214b970352644a3316a1a6ac085099e96875d62e6eb6b95d`  
		Last Modified: Tue, 08 Apr 2025 22:18:51 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:5aa97ff134b80e48aaa63c71d9c8343062cb648de6445e6d078b62dab5b08a3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8af43893a1163e246e9f97ae6b6ca899d5147c74db410070388f3dc6b1bb9a`

```dockerfile
```

-	Layers:
	-	`sha256:b2dde84b1c72b35f921945f0d6bec4b01ff2c811e34deff66dc5a99577731ade`  
		Last Modified: Tue, 08 Apr 2025 22:18:51 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; s390x

```console
$ docker pull nats@sha256:24602554caa826a00e26b3dae9c589026eaab3e0ad8e59cb573cac3996e62f8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6122577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7976c47bfec0473931b30ef2753bdc1cefde06b7a03f869cabb36b78aee6fd30`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:096b0701966ee2a29da8fc2c3f8ad25d2a0bb1211425d296e92558196ebe09c9`  
		Last Modified: Tue, 08 Apr 2025 17:26:22 GMT  
		Size: 6.1 MB (6122069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50402e49c7c832b57fb874a3e012194a27d09597f2d39ddc97db3701ae5bfb7`  
		Last Modified: Tue, 08 Apr 2025 22:07:44 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:6f2d2b491eee799540891efc47f6f00293192e82097e7b80bb5fd571bbf312c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8736b1c1aaa3dce6b14a6b7b5cad1d5cc142fae7d7d9fd17b8a6d72e67a82268`

```dockerfile
```

-	Layers:
	-	`sha256:1ab1e3d26d57dec0dbbe6b34b8c0c23c6308ed6e3e58b9267695ff2247985c40`  
		Last Modified: Tue, 08 Apr 2025 22:07:44 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - windows version 10.0.17763.7249; amd64

```console
$ docker pull nats@sha256:70dfa0a823409d278307a2f602a989bb5088fc2ed408add1628e7026065e4f7f
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.2 MB (115214035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c10544dab15e09a82ee58dfe65c5cebe6e37634a0fc0e40720019d69e49ec056`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Fri, 18 Apr 2025 04:11:39 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 18 Apr 2025 04:11:40 GMT
RUN cmd /S /C #(nop) COPY file:eee3870bfbcd9bfddd3622d20a6c2075b583b61ab0944602ceefed02dee11aa2 in C:\nats-server.exe 
# Fri, 18 Apr 2025 04:11:41 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Fri, 18 Apr 2025 04:11:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 18 Apr 2025 04:11:42 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 18 Apr 2025 04:11:42 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5dab9cfa2f7ef2b19e95e68d27e3d0b208d9016da1b04298c500e78281a15e7`  
		Last Modified: Fri, 18 Apr 2025 04:11:48 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d0b032347a8dcb65e359d04c00733934bf6cfe61db4b1142a1df5f3de23a9cc`  
		Last Modified: Fri, 18 Apr 2025 04:11:47 GMT  
		Size: 6.5 MB (6455931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497b3350d5c31834bcca73478d5fc7c0d3c546c1676c042e1e9d1ec9afc85bdd`  
		Last Modified: Fri, 18 Apr 2025 04:11:46 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658de08330e9b739dfbff680b38b2bb55dc4b4aec6d4064b19ecc24c7ba9a8aa`  
		Last Modified: Fri, 18 Apr 2025 04:11:46 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0312f657691b722f56e7ed6bc33b2119988f7f21d9853fe0a8dcc79a3b5aec`  
		Last Modified: Fri, 18 Apr 2025 04:11:46 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fc9ae19d64bc742bb97a1eec58e04de0d2eab1eb71186876fed513a4b21a3d`  
		Last Modified: Fri, 18 Apr 2025 04:11:46 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-alpine`

```console
$ docker pull nats@sha256:a6e0002b6027b9f64619750d8d2d535c54fe247b54050959be29bb69e6b0d1f1
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

### `nats:2.11-alpine` - linux; amd64

```console
$ docker pull nats@sha256:7cbd5f7f5326233bf97e186073144217f7b98b8cf904d0d83ba9ff08caf6f0d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10386082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a900eac76440acf8f75c33c7a37e9103f53d792b082074036e8ee5a2df6903ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
ENV NATS_SERVER=2.11.1
# Tue, 08 Apr 2025 17:23:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='27c90d8bc0ad10bfb38ef92bdea8528b4bfc5aa56afba91c790fb3921ea205a2' ;; 		armhf) natsArch='arm6'; sha256='8f9f2f4aa85c242f254a175c9455e9d00c6a0e7fc96b87a14ef3bd6d8762e900' ;; 		armv7) natsArch='arm7'; sha256='06dee81c2fd32639ae646112daaf9b84b71023bee88b16fd3324fd922095dda1' ;; 		x86_64) natsArch='amd64'; sha256='f1d9754bf34316d1f7d349b176ff0414c9cce742846bf2eec0b402eee35a638c' ;; 		x86) natsArch='386'; sha256='b746e832f96f07ee5958c99201b7a96695a3e1339f416342b9fd3c083a68dba7' ;; 		s390x) natsArch='s390x'; sha256='018ec95e10758c3e6ea14f034d3fe099234957dec8290bc5aa3480a8d77e3e29' ;; 		ppc64le) natsArch='ppc64le'; sha256='be0f9308ffcdfa36189afdf7e8116235995d7d20406c0fc7b8aa5b5f724aa3d6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bffd47baa898ba4523ccc09b26058ea27891e234ee7563e763b8f9bd29bde2e`  
		Last Modified: Tue, 08 Apr 2025 20:28:15 GMT  
		Size: 6.7 MB (6742867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63af34edcf916551729eef83c51841b9403e9bedf717838e0dedfe7e5bfa977b`  
		Last Modified: Tue, 08 Apr 2025 20:28:15 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9081de8dcbbc97f988fe2e6b0695f7eaea0f8774966c467ed29bd8602391ff9`  
		Last Modified: Tue, 08 Apr 2025 20:28:14 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:062f6b7155ed98648412670dffe43c7be1f4768f50bfa3fa63ba59b794ec300c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b2af7e3b213deee44fd319c5441ec699c53280a665cf650e9eec87b50af831`

```dockerfile
```

-	Layers:
	-	`sha256:df59247835527b1024e29a039c6dd53ac255e4500ded522b5e05635e9495a453`  
		Last Modified: Tue, 08 Apr 2025 20:28:15 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:b25ce7d7cfb629d1a132ae08b8fd84da4ab34c224fc57a9366f4f7e8284a89b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9849553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5bc00749e465a4c423af0395ea8a620f5184198a26aa70c550afb018dcd620d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da0a4b9d57d2a4c2439f0c8731b7e1ef8f0a7f2a1edf643d5f50a73ffc0c31f9' ;; 		armhf) natsArch='arm6'; sha256='2370e8d794acb0f176be0f0885f9930fa9d8d1276f15162eb8db336467279bc1' ;; 		armv7) natsArch='arm7'; sha256='46b038e57ad586f05342dcd3b29a2c2597217c19172a916eef9187170f024ad8' ;; 		x86_64) natsArch='amd64'; sha256='a123c8e43abe5ca8f0bff9393547f20f4bbac6fc0fb3c586ec031855911c414a' ;; 		x86) natsArch='386'; sha256='03bf7db9323c453b1257c3a43a21fcd5a975a2cc136c4bbeab7c0e815939e37e' ;; 		s390x) natsArch='s390x'; sha256='eb40e4a843124198b7e8625b7cccbd52810d63db17e1557d59681f5f29be5a98' ;; 		ppc64le) natsArch='ppc64le'; sha256='28e2afbca41dffe453507a993291560bfc57c6f43fe435604f894c3d91426dd0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53314fd665bd0c97ace20b7fb2ca1b46ecfdd7426150f8745639bb7704613d5a`  
		Last Modified: Fri, 25 Apr 2025 17:47:34 GMT  
		Size: 6.5 MB (6483851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cefa71e52d2f6e7b13aac0c8fe523facca0507ac8e8b180b168eeadfd046b89`  
		Last Modified: Fri, 25 Apr 2025 17:47:33 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c198696667425fcef5f606fda093ce31277d14ed9b5dc1592fb47511143d5052`  
		Last Modified: Fri, 25 Apr 2025 17:47:33 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:20a327f5442b5e1a069fb161658d8b9436e0f0ce2df3802ad9d74362036c2210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b2f873973386278768ee962ed71409b2376682ae823894072e19be8cde68680`

```dockerfile
```

-	Layers:
	-	`sha256:9122357572edf020a23a1bbf0fbe37650762d41d728dfaccb594f7e5890cbd2d`  
		Last Modified: Fri, 25 Apr 2025 17:47:33 GMT  
		Size: 14.4 KB (14424 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:2f0c0883a1c8a7dd3a93730ce2ca646928c272aba42b05b5d163f5e779696f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9552050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28191bc799228c242ab1ebf65c8eaa89c320b25a78ee799103e544b8250226d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
ENV NATS_SERVER=2.11.1
# Tue, 08 Apr 2025 17:23:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='27c90d8bc0ad10bfb38ef92bdea8528b4bfc5aa56afba91c790fb3921ea205a2' ;; 		armhf) natsArch='arm6'; sha256='8f9f2f4aa85c242f254a175c9455e9d00c6a0e7fc96b87a14ef3bd6d8762e900' ;; 		armv7) natsArch='arm7'; sha256='06dee81c2fd32639ae646112daaf9b84b71023bee88b16fd3324fd922095dda1' ;; 		x86_64) natsArch='amd64'; sha256='f1d9754bf34316d1f7d349b176ff0414c9cce742846bf2eec0b402eee35a638c' ;; 		x86) natsArch='386'; sha256='b746e832f96f07ee5958c99201b7a96695a3e1339f416342b9fd3c083a68dba7' ;; 		s390x) natsArch='s390x'; sha256='018ec95e10758c3e6ea14f034d3fe099234957dec8290bc5aa3480a8d77e3e29' ;; 		ppc64le) natsArch='ppc64le'; sha256='be0f9308ffcdfa36189afdf7e8116235995d7d20406c0fc7b8aa5b5f724aa3d6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b82717f71af9d7a4242a00c3efbdf445cc5b3122fb74530e7d5e2971036151`  
		Last Modified: Tue, 08 Apr 2025 20:32:08 GMT  
		Size: 6.5 MB (6452958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49791283070c29e615bbe60ca9b43f0b5c63e67560f09700c02a4920fc31499`  
		Last Modified: Tue, 08 Apr 2025 20:32:07 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ade19b2805065881eeef7b4e282331a2f7fbd91f70c6349b33b2d448e8dc64`  
		Last Modified: Tue, 08 Apr 2025 20:32:07 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:f66e974c49c5b42df6f26cfe23be843bed87adb4df5efde68922bcd9bcdb0654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45fd3c0542a49a774cbfafb32d74dcb38bb7230e53a346c90ea2dc92652e671d`

```dockerfile
```

-	Layers:
	-	`sha256:dafec31d0d294d05c575a7f27247bd7720e66c489584ce418ed700595bb00c9f`  
		Last Modified: Tue, 08 Apr 2025 20:32:07 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:4fe60f222966727f3e81dbb3bf2aaec58c7c8b573afbe318f6cb2c70c19f37c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10254225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5d5d918ca9a0f7dd7c056851f2898f207c48f854da7954fc8fafc8fd1aa3021`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da0a4b9d57d2a4c2439f0c8731b7e1ef8f0a7f2a1edf643d5f50a73ffc0c31f9' ;; 		armhf) natsArch='arm6'; sha256='2370e8d794acb0f176be0f0885f9930fa9d8d1276f15162eb8db336467279bc1' ;; 		armv7) natsArch='arm7'; sha256='46b038e57ad586f05342dcd3b29a2c2597217c19172a916eef9187170f024ad8' ;; 		x86_64) natsArch='amd64'; sha256='a123c8e43abe5ca8f0bff9393547f20f4bbac6fc0fb3c586ec031855911c414a' ;; 		x86) natsArch='386'; sha256='03bf7db9323c453b1257c3a43a21fcd5a975a2cc136c4bbeab7c0e815939e37e' ;; 		s390x) natsArch='s390x'; sha256='eb40e4a843124198b7e8625b7cccbd52810d63db17e1557d59681f5f29be5a98' ;; 		ppc64le) natsArch='ppc64le'; sha256='28e2afbca41dffe453507a993291560bfc57c6f43fe435604f894c3d91426dd0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3febb0921652e8042f634bdcb7812f9a2ed40e073970e14a940960350b775dbf`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 6.3 MB (6260226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc226874bc3060e6e916fa3ef948812c54a012b6081a27eaab55addfec8b7473`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e367a33259d9c5e7a6a6b42c8482e8bc6930e1a713671c0cf2fd1b5c879eef01`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:fda84d5581ce64cec49def3b469b26e717bf64d28a817656b19e16da89e9ea25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a714d7bd3b6fd55a075f56b50fa0da44cf6616089161edf7a648ba47af3256`

```dockerfile
```

-	Layers:
	-	`sha256:5f55a5edc5478bd7d7c9bc7e0763ad4dee93ecffafd3ed2f7702e7ee06ae75b0`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 14.5 KB (14469 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:6b6b1109a98eafc180bae27e0e27a1110433dfd3577e78cac2d8eb793969fc43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9797332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52bb4f9d9231f9b6c625e4a3a3f2874bd83248ad61158f697eb327444118f598`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
ENV NATS_SERVER=2.11.1
# Tue, 08 Apr 2025 17:23:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='27c90d8bc0ad10bfb38ef92bdea8528b4bfc5aa56afba91c790fb3921ea205a2' ;; 		armhf) natsArch='arm6'; sha256='8f9f2f4aa85c242f254a175c9455e9d00c6a0e7fc96b87a14ef3bd6d8762e900' ;; 		armv7) natsArch='arm7'; sha256='06dee81c2fd32639ae646112daaf9b84b71023bee88b16fd3324fd922095dda1' ;; 		x86_64) natsArch='amd64'; sha256='f1d9754bf34316d1f7d349b176ff0414c9cce742846bf2eec0b402eee35a638c' ;; 		x86) natsArch='386'; sha256='b746e832f96f07ee5958c99201b7a96695a3e1339f416342b9fd3c083a68dba7' ;; 		s390x) natsArch='s390x'; sha256='018ec95e10758c3e6ea14f034d3fe099234957dec8290bc5aa3480a8d77e3e29' ;; 		ppc64le) natsArch='ppc64le'; sha256='be0f9308ffcdfa36189afdf7e8116235995d7d20406c0fc7b8aa5b5f724aa3d6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8be7344e3eed187cfb792f8b098e4b9639bd0e5318ceffb68a33a3bad2164c`  
		Last Modified: Tue, 08 Apr 2025 20:42:59 GMT  
		Size: 6.2 MB (6222020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd19bdb0c54b34703a3579dcae0cd27d09d0ed9ac711591a13fba04c9a89aacf`  
		Last Modified: Tue, 08 Apr 2025 20:42:58 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2608514a04b63ea4ad3654f5acd693a1bc97dc1d1c8b8a1495df0e53dda6ff0`  
		Last Modified: Tue, 08 Apr 2025 20:42:58 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:28f492787cca2adfb7bcfcb21be59f4685caad51e81ff81fac96d5d46445c776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ada670995406f8a9d5e52233a0003738fc8c1933710c4de448e87af34e5a3863`

```dockerfile
```

-	Layers:
	-	`sha256:e269226b323faa520a451de66e148284583959e77af2bf7d56a4d350cc37623a`  
		Last Modified: Tue, 08 Apr 2025 20:42:58 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; s390x

```console
$ docker pull nats@sha256:cf54ecfbde97d03a9d1a1bfdbcf069c2683ef48f34d72013b9064f5ed0ab9183
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10053959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f94c74252361e5594561679a5358b7e135dd9c7c2f3c51be0138903f04c6aa8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
ENV NATS_SERVER=2.11.1
# Tue, 08 Apr 2025 17:23:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='27c90d8bc0ad10bfb38ef92bdea8528b4bfc5aa56afba91c790fb3921ea205a2' ;; 		armhf) natsArch='arm6'; sha256='8f9f2f4aa85c242f254a175c9455e9d00c6a0e7fc96b87a14ef3bd6d8762e900' ;; 		armv7) natsArch='arm7'; sha256='06dee81c2fd32639ae646112daaf9b84b71023bee88b16fd3324fd922095dda1' ;; 		x86_64) natsArch='amd64'; sha256='f1d9754bf34316d1f7d349b176ff0414c9cce742846bf2eec0b402eee35a638c' ;; 		x86) natsArch='386'; sha256='b746e832f96f07ee5958c99201b7a96695a3e1339f416342b9fd3c083a68dba7' ;; 		s390x) natsArch='s390x'; sha256='018ec95e10758c3e6ea14f034d3fe099234957dec8290bc5aa3480a8d77e3e29' ;; 		ppc64le) natsArch='ppc64le'; sha256='be0f9308ffcdfa36189afdf7e8116235995d7d20406c0fc7b8aa5b5f724aa3d6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a92fbe14b2cdd6c1a85f89f171cfbad87c0f00fc6205b2d6c5cfa29cf51cf30`  
		Last Modified: Tue, 08 Apr 2025 22:04:28 GMT  
		Size: 6.6 MB (6585420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc913d6647309b3286a51c5f87c54edfb961dd53b9ca8a4496335154e303ab2e`  
		Last Modified: Tue, 08 Apr 2025 22:04:28 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22b8967d9a9d213c271cc67dcbe1d89b5b0870a2d2a399344c51f7cdc25b2c7`  
		Last Modified: Tue, 08 Apr 2025 22:04:28 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:b55039b07dc68ae69425511e99ab099b60f707e9a565a17a0d28e21a33c1f346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4570b0028f776dbca1deaabac6952192f625b95ec93d8098c7058262a3ca4b9`

```dockerfile
```

-	Layers:
	-	`sha256:5b1859f0680f19779c89b10a96fe392f905b04060b6ca55b19696d4fc51ece7c`  
		Last Modified: Tue, 08 Apr 2025 22:04:28 GMT  
		Size: 14.3 KB (14316 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11-alpine3.21`

```console
$ docker pull nats@sha256:a6e0002b6027b9f64619750d8d2d535c54fe247b54050959be29bb69e6b0d1f1
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

### `nats:2.11-alpine3.21` - linux; amd64

```console
$ docker pull nats@sha256:7cbd5f7f5326233bf97e186073144217f7b98b8cf904d0d83ba9ff08caf6f0d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10386082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a900eac76440acf8f75c33c7a37e9103f53d792b082074036e8ee5a2df6903ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
ENV NATS_SERVER=2.11.1
# Tue, 08 Apr 2025 17:23:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='27c90d8bc0ad10bfb38ef92bdea8528b4bfc5aa56afba91c790fb3921ea205a2' ;; 		armhf) natsArch='arm6'; sha256='8f9f2f4aa85c242f254a175c9455e9d00c6a0e7fc96b87a14ef3bd6d8762e900' ;; 		armv7) natsArch='arm7'; sha256='06dee81c2fd32639ae646112daaf9b84b71023bee88b16fd3324fd922095dda1' ;; 		x86_64) natsArch='amd64'; sha256='f1d9754bf34316d1f7d349b176ff0414c9cce742846bf2eec0b402eee35a638c' ;; 		x86) natsArch='386'; sha256='b746e832f96f07ee5958c99201b7a96695a3e1339f416342b9fd3c083a68dba7' ;; 		s390x) natsArch='s390x'; sha256='018ec95e10758c3e6ea14f034d3fe099234957dec8290bc5aa3480a8d77e3e29' ;; 		ppc64le) natsArch='ppc64le'; sha256='be0f9308ffcdfa36189afdf7e8116235995d7d20406c0fc7b8aa5b5f724aa3d6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bffd47baa898ba4523ccc09b26058ea27891e234ee7563e763b8f9bd29bde2e`  
		Last Modified: Tue, 08 Apr 2025 20:28:15 GMT  
		Size: 6.7 MB (6742867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63af34edcf916551729eef83c51841b9403e9bedf717838e0dedfe7e5bfa977b`  
		Last Modified: Tue, 08 Apr 2025 20:28:15 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9081de8dcbbc97f988fe2e6b0695f7eaea0f8774966c467ed29bd8602391ff9`  
		Last Modified: Tue, 08 Apr 2025 20:28:14 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:062f6b7155ed98648412670dffe43c7be1f4768f50bfa3fa63ba59b794ec300c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b2af7e3b213deee44fd319c5441ec699c53280a665cf650e9eec87b50af831`

```dockerfile
```

-	Layers:
	-	`sha256:df59247835527b1024e29a039c6dd53ac255e4500ded522b5e05635e9495a453`  
		Last Modified: Tue, 08 Apr 2025 20:28:15 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:b25ce7d7cfb629d1a132ae08b8fd84da4ab34c224fc57a9366f4f7e8284a89b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9849553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5bc00749e465a4c423af0395ea8a620f5184198a26aa70c550afb018dcd620d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da0a4b9d57d2a4c2439f0c8731b7e1ef8f0a7f2a1edf643d5f50a73ffc0c31f9' ;; 		armhf) natsArch='arm6'; sha256='2370e8d794acb0f176be0f0885f9930fa9d8d1276f15162eb8db336467279bc1' ;; 		armv7) natsArch='arm7'; sha256='46b038e57ad586f05342dcd3b29a2c2597217c19172a916eef9187170f024ad8' ;; 		x86_64) natsArch='amd64'; sha256='a123c8e43abe5ca8f0bff9393547f20f4bbac6fc0fb3c586ec031855911c414a' ;; 		x86) natsArch='386'; sha256='03bf7db9323c453b1257c3a43a21fcd5a975a2cc136c4bbeab7c0e815939e37e' ;; 		s390x) natsArch='s390x'; sha256='eb40e4a843124198b7e8625b7cccbd52810d63db17e1557d59681f5f29be5a98' ;; 		ppc64le) natsArch='ppc64le'; sha256='28e2afbca41dffe453507a993291560bfc57c6f43fe435604f894c3d91426dd0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53314fd665bd0c97ace20b7fb2ca1b46ecfdd7426150f8745639bb7704613d5a`  
		Last Modified: Fri, 25 Apr 2025 17:47:34 GMT  
		Size: 6.5 MB (6483851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cefa71e52d2f6e7b13aac0c8fe523facca0507ac8e8b180b168eeadfd046b89`  
		Last Modified: Fri, 25 Apr 2025 17:47:33 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c198696667425fcef5f606fda093ce31277d14ed9b5dc1592fb47511143d5052`  
		Last Modified: Fri, 25 Apr 2025 17:47:33 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:20a327f5442b5e1a069fb161658d8b9436e0f0ce2df3802ad9d74362036c2210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b2f873973386278768ee962ed71409b2376682ae823894072e19be8cde68680`

```dockerfile
```

-	Layers:
	-	`sha256:9122357572edf020a23a1bbf0fbe37650762d41d728dfaccb594f7e5890cbd2d`  
		Last Modified: Fri, 25 Apr 2025 17:47:33 GMT  
		Size: 14.4 KB (14424 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:2f0c0883a1c8a7dd3a93730ce2ca646928c272aba42b05b5d163f5e779696f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9552050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28191bc799228c242ab1ebf65c8eaa89c320b25a78ee799103e544b8250226d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
ENV NATS_SERVER=2.11.1
# Tue, 08 Apr 2025 17:23:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='27c90d8bc0ad10bfb38ef92bdea8528b4bfc5aa56afba91c790fb3921ea205a2' ;; 		armhf) natsArch='arm6'; sha256='8f9f2f4aa85c242f254a175c9455e9d00c6a0e7fc96b87a14ef3bd6d8762e900' ;; 		armv7) natsArch='arm7'; sha256='06dee81c2fd32639ae646112daaf9b84b71023bee88b16fd3324fd922095dda1' ;; 		x86_64) natsArch='amd64'; sha256='f1d9754bf34316d1f7d349b176ff0414c9cce742846bf2eec0b402eee35a638c' ;; 		x86) natsArch='386'; sha256='b746e832f96f07ee5958c99201b7a96695a3e1339f416342b9fd3c083a68dba7' ;; 		s390x) natsArch='s390x'; sha256='018ec95e10758c3e6ea14f034d3fe099234957dec8290bc5aa3480a8d77e3e29' ;; 		ppc64le) natsArch='ppc64le'; sha256='be0f9308ffcdfa36189afdf7e8116235995d7d20406c0fc7b8aa5b5f724aa3d6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b82717f71af9d7a4242a00c3efbdf445cc5b3122fb74530e7d5e2971036151`  
		Last Modified: Tue, 08 Apr 2025 20:32:08 GMT  
		Size: 6.5 MB (6452958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49791283070c29e615bbe60ca9b43f0b5c63e67560f09700c02a4920fc31499`  
		Last Modified: Tue, 08 Apr 2025 20:32:07 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ade19b2805065881eeef7b4e282331a2f7fbd91f70c6349b33b2d448e8dc64`  
		Last Modified: Tue, 08 Apr 2025 20:32:07 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:f66e974c49c5b42df6f26cfe23be843bed87adb4df5efde68922bcd9bcdb0654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45fd3c0542a49a774cbfafb32d74dcb38bb7230e53a346c90ea2dc92652e671d`

```dockerfile
```

-	Layers:
	-	`sha256:dafec31d0d294d05c575a7f27247bd7720e66c489584ce418ed700595bb00c9f`  
		Last Modified: Tue, 08 Apr 2025 20:32:07 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:4fe60f222966727f3e81dbb3bf2aaec58c7c8b573afbe318f6cb2c70c19f37c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10254225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5d5d918ca9a0f7dd7c056851f2898f207c48f854da7954fc8fafc8fd1aa3021`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da0a4b9d57d2a4c2439f0c8731b7e1ef8f0a7f2a1edf643d5f50a73ffc0c31f9' ;; 		armhf) natsArch='arm6'; sha256='2370e8d794acb0f176be0f0885f9930fa9d8d1276f15162eb8db336467279bc1' ;; 		armv7) natsArch='arm7'; sha256='46b038e57ad586f05342dcd3b29a2c2597217c19172a916eef9187170f024ad8' ;; 		x86_64) natsArch='amd64'; sha256='a123c8e43abe5ca8f0bff9393547f20f4bbac6fc0fb3c586ec031855911c414a' ;; 		x86) natsArch='386'; sha256='03bf7db9323c453b1257c3a43a21fcd5a975a2cc136c4bbeab7c0e815939e37e' ;; 		s390x) natsArch='s390x'; sha256='eb40e4a843124198b7e8625b7cccbd52810d63db17e1557d59681f5f29be5a98' ;; 		ppc64le) natsArch='ppc64le'; sha256='28e2afbca41dffe453507a993291560bfc57c6f43fe435604f894c3d91426dd0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3febb0921652e8042f634bdcb7812f9a2ed40e073970e14a940960350b775dbf`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 6.3 MB (6260226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc226874bc3060e6e916fa3ef948812c54a012b6081a27eaab55addfec8b7473`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e367a33259d9c5e7a6a6b42c8482e8bc6930e1a713671c0cf2fd1b5c879eef01`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:fda84d5581ce64cec49def3b469b26e717bf64d28a817656b19e16da89e9ea25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a714d7bd3b6fd55a075f56b50fa0da44cf6616089161edf7a648ba47af3256`

```dockerfile
```

-	Layers:
	-	`sha256:5f55a5edc5478bd7d7c9bc7e0763ad4dee93ecffafd3ed2f7702e7ee06ae75b0`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 14.5 KB (14469 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:6b6b1109a98eafc180bae27e0e27a1110433dfd3577e78cac2d8eb793969fc43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9797332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52bb4f9d9231f9b6c625e4a3a3f2874bd83248ad61158f697eb327444118f598`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
ENV NATS_SERVER=2.11.1
# Tue, 08 Apr 2025 17:23:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='27c90d8bc0ad10bfb38ef92bdea8528b4bfc5aa56afba91c790fb3921ea205a2' ;; 		armhf) natsArch='arm6'; sha256='8f9f2f4aa85c242f254a175c9455e9d00c6a0e7fc96b87a14ef3bd6d8762e900' ;; 		armv7) natsArch='arm7'; sha256='06dee81c2fd32639ae646112daaf9b84b71023bee88b16fd3324fd922095dda1' ;; 		x86_64) natsArch='amd64'; sha256='f1d9754bf34316d1f7d349b176ff0414c9cce742846bf2eec0b402eee35a638c' ;; 		x86) natsArch='386'; sha256='b746e832f96f07ee5958c99201b7a96695a3e1339f416342b9fd3c083a68dba7' ;; 		s390x) natsArch='s390x'; sha256='018ec95e10758c3e6ea14f034d3fe099234957dec8290bc5aa3480a8d77e3e29' ;; 		ppc64le) natsArch='ppc64le'; sha256='be0f9308ffcdfa36189afdf7e8116235995d7d20406c0fc7b8aa5b5f724aa3d6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8be7344e3eed187cfb792f8b098e4b9639bd0e5318ceffb68a33a3bad2164c`  
		Last Modified: Tue, 08 Apr 2025 20:42:59 GMT  
		Size: 6.2 MB (6222020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd19bdb0c54b34703a3579dcae0cd27d09d0ed9ac711591a13fba04c9a89aacf`  
		Last Modified: Tue, 08 Apr 2025 20:42:58 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2608514a04b63ea4ad3654f5acd693a1bc97dc1d1c8b8a1495df0e53dda6ff0`  
		Last Modified: Tue, 08 Apr 2025 20:42:58 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:28f492787cca2adfb7bcfcb21be59f4685caad51e81ff81fac96d5d46445c776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ada670995406f8a9d5e52233a0003738fc8c1933710c4de448e87af34e5a3863`

```dockerfile
```

-	Layers:
	-	`sha256:e269226b323faa520a451de66e148284583959e77af2bf7d56a4d350cc37623a`  
		Last Modified: Tue, 08 Apr 2025 20:42:58 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:cf54ecfbde97d03a9d1a1bfdbcf069c2683ef48f34d72013b9064f5ed0ab9183
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10053959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f94c74252361e5594561679a5358b7e135dd9c7c2f3c51be0138903f04c6aa8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
ENV NATS_SERVER=2.11.1
# Tue, 08 Apr 2025 17:23:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='27c90d8bc0ad10bfb38ef92bdea8528b4bfc5aa56afba91c790fb3921ea205a2' ;; 		armhf) natsArch='arm6'; sha256='8f9f2f4aa85c242f254a175c9455e9d00c6a0e7fc96b87a14ef3bd6d8762e900' ;; 		armv7) natsArch='arm7'; sha256='06dee81c2fd32639ae646112daaf9b84b71023bee88b16fd3324fd922095dda1' ;; 		x86_64) natsArch='amd64'; sha256='f1d9754bf34316d1f7d349b176ff0414c9cce742846bf2eec0b402eee35a638c' ;; 		x86) natsArch='386'; sha256='b746e832f96f07ee5958c99201b7a96695a3e1339f416342b9fd3c083a68dba7' ;; 		s390x) natsArch='s390x'; sha256='018ec95e10758c3e6ea14f034d3fe099234957dec8290bc5aa3480a8d77e3e29' ;; 		ppc64le) natsArch='ppc64le'; sha256='be0f9308ffcdfa36189afdf7e8116235995d7d20406c0fc7b8aa5b5f724aa3d6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a92fbe14b2cdd6c1a85f89f171cfbad87c0f00fc6205b2d6c5cfa29cf51cf30`  
		Last Modified: Tue, 08 Apr 2025 22:04:28 GMT  
		Size: 6.6 MB (6585420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc913d6647309b3286a51c5f87c54edfb961dd53b9ca8a4496335154e303ab2e`  
		Last Modified: Tue, 08 Apr 2025 22:04:28 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22b8967d9a9d213c271cc67dcbe1d89b5b0870a2d2a399344c51f7cdc25b2c7`  
		Last Modified: Tue, 08 Apr 2025 22:04:28 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:b55039b07dc68ae69425511e99ab099b60f707e9a565a17a0d28e21a33c1f346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4570b0028f776dbca1deaabac6952192f625b95ec93d8098c7058262a3ca4b9`

```dockerfile
```

-	Layers:
	-	`sha256:5b1859f0680f19779c89b10a96fe392f905b04060b6ca55b19696d4fc51ece7c`  
		Last Modified: Tue, 08 Apr 2025 22:04:28 GMT  
		Size: 14.3 KB (14316 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11-linux`

```console
$ docker pull nats@sha256:4bb7463f82c83da51fd098d9ddbc0dccfdc7415e110b02de375f60066b392878
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

### `nats:2.11-linux` - linux; amd64

```console
$ docker pull nats@sha256:41dddbc7a9265892086db802a374dbf910b5d0db786c8ba12e27a81f2ede8f05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6282680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ddda49ccc5be8fc53872fcb74f0f168368af1d3e5fc27fd096bb4ab9fac9e5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7a31ab99389a11bb36db183df5a6bc8d784c1e96fb10c1973e04b98e17e58f51`  
		Last Modified: Tue, 08 Apr 2025 17:26:21 GMT  
		Size: 6.3 MB (6282171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bcd18a1de501f0dcf00113b8c1effd2b7f198a1383c537490e8dce3a826adce`  
		Last Modified: Tue, 08 Apr 2025 21:07:44 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:16692b029d2fd73a6c9833d59190a10a052903fbc5b68228ca0ce31e25895ee4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a60659f991d784a3586e62308c55e27054bad66d740cbde49980328b682cb858`

```dockerfile
```

-	Layers:
	-	`sha256:d0fd9d7883ec1e99c1a17109b0a6fd39dec7b9ec8f40f0ace2f2c15f9d8846a3`  
		Last Modified: Tue, 08 Apr 2025 21:07:45 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:f53994879dbfd2fc8177b383905d33db1095d8b42bb4bec64088771cecdb2bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6002072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01de3b3fb48e4b75539a9af5640e6f77115cdbe9419f3da2891472ec6e806148`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bc9bfb085b797367e9407dbdf5a3928ee0d69859fb96188165856b5e8e1b6e88`  
		Last Modified: Tue, 08 Apr 2025 17:26:22 GMT  
		Size: 6.0 MB (6001563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef30b0264d904d40fbf4763922653522d80a800c24f6bcbb52a1a66fd1accaf8`  
		Last Modified: Tue, 08 Apr 2025 21:07:08 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:f9537be10194b98f78298fad26add4a04948857f650479e674587da738dcf69c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7014bcdaac4c9653a29f6fc739854477633a62a69bd0cba053bbeecbfc57e101`

```dockerfile
```

-	Layers:
	-	`sha256:e337d587115a4b810f5a9fa3deb1db109744f3828488f355e6bfa4c965ea5501`  
		Last Modified: Tue, 08 Apr 2025 21:07:08 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:859b07690a2059b52277aceb9feed7e81269aed09859f1c3b0f3162d751ddb29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5992346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e38aded7ecfd1e1b61cc0452d01e01718e0a4be4ee666ac1980ddacb6f7defbc`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8f114aa547686a4604d8f5fbabd3d89b59a801cc55b68aa653d813c66ca32a65`  
		Last Modified: Tue, 08 Apr 2025 17:26:18 GMT  
		Size: 6.0 MB (5991835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844018e59249593be5d829b3a4bba323e96c26297db204b3a8a8a52e847f8041`  
		Last Modified: Tue, 08 Apr 2025 21:25:07 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:1e53207f824b4b97a2158a01c60662ef62ff32a777e55e615077563d48bcc314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a229febf9f435367bc3df4661afe24971b0581fa0b4b375a92d4ac38c3ce791`

```dockerfile
```

-	Layers:
	-	`sha256:36f6e0df21021319068725c9d7c2325e4fad06927e5ff9fe7fe11ec830f17f1c`  
		Last Modified: Tue, 08 Apr 2025 21:25:06 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:9142b78e748793c9e3b2fda3ac3800e66e866bf0147d634a7aea592f973a023a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5776867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee76a21b5d66ec40c0c8c53a6af4ed91124f7a2820ab80bf20279efdc3e689c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6b90b986da10be1b936fe6989055b49edb315427df0ceb03d1dd2f9dd98fb88`  
		Last Modified: Tue, 08 Apr 2025 17:26:18 GMT  
		Size: 5.8 MB (5776357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5e46c8b1d8619650c3d1afbfcf70b02949ce40d6fd6eb7d769bdc98a1def25`  
		Last Modified: Wed, 09 Apr 2025 00:53:02 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:9f289daca75844d624973e2b4e4a78db9e2026bfd59d743648f68e3c13d32a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53971055b1ebeea168a941b88f41f089dd9886aa55cbebe6b4f12f98ddb49666`

```dockerfile
```

-	Layers:
	-	`sha256:a65f769c9cecfc76c232cf377b8548ffd7fc82eae67b781487e0924b3319a183`  
		Last Modified: Wed, 09 Apr 2025 00:53:02 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:8cbd8caa2bdb9c64319ae113af4cf4170b92f3795148cb20401f2f1f16aa1d11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5757631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ba2ae7e87afe027065399c01f1230c431bed76a811a5cc5c83e971b6e70a26`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2c03c8b47070105a3781cfd93e5a048f0fcf1895182b8500a1875b914beccc2b`  
		Last Modified: Tue, 08 Apr 2025 17:26:19 GMT  
		Size: 5.8 MB (5757122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425937f6cd03177f214b970352644a3316a1a6ac085099e96875d62e6eb6b95d`  
		Last Modified: Tue, 08 Apr 2025 22:18:51 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:5aa97ff134b80e48aaa63c71d9c8343062cb648de6445e6d078b62dab5b08a3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8af43893a1163e246e9f97ae6b6ca899d5147c74db410070388f3dc6b1bb9a`

```dockerfile
```

-	Layers:
	-	`sha256:b2dde84b1c72b35f921945f0d6bec4b01ff2c811e34deff66dc5a99577731ade`  
		Last Modified: Tue, 08 Apr 2025 22:18:51 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; s390x

```console
$ docker pull nats@sha256:24602554caa826a00e26b3dae9c589026eaab3e0ad8e59cb573cac3996e62f8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6122577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7976c47bfec0473931b30ef2753bdc1cefde06b7a03f869cabb36b78aee6fd30`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:096b0701966ee2a29da8fc2c3f8ad25d2a0bb1211425d296e92558196ebe09c9`  
		Last Modified: Tue, 08 Apr 2025 17:26:22 GMT  
		Size: 6.1 MB (6122069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50402e49c7c832b57fb874a3e012194a27d09597f2d39ddc97db3701ae5bfb7`  
		Last Modified: Tue, 08 Apr 2025 22:07:44 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:6f2d2b491eee799540891efc47f6f00293192e82097e7b80bb5fd571bbf312c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8736b1c1aaa3dce6b14a6b7b5cad1d5cc142fae7d7d9fd17b8a6d72e67a82268`

```dockerfile
```

-	Layers:
	-	`sha256:1ab1e3d26d57dec0dbbe6b34b8c0c23c6308ed6e3e58b9267695ff2247985c40`  
		Last Modified: Tue, 08 Apr 2025 22:07:44 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11-nanoserver`

```console
$ docker pull nats@sha256:714b0b324ae5c514cc8066861c1ea58b8e852b21686bd57938b4cad501106b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `nats:2.11-nanoserver` - windows version 10.0.17763.7249; amd64

```console
$ docker pull nats@sha256:70dfa0a823409d278307a2f602a989bb5088fc2ed408add1628e7026065e4f7f
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.2 MB (115214035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c10544dab15e09a82ee58dfe65c5cebe6e37634a0fc0e40720019d69e49ec056`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Fri, 18 Apr 2025 04:11:39 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 18 Apr 2025 04:11:40 GMT
RUN cmd /S /C #(nop) COPY file:eee3870bfbcd9bfddd3622d20a6c2075b583b61ab0944602ceefed02dee11aa2 in C:\nats-server.exe 
# Fri, 18 Apr 2025 04:11:41 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Fri, 18 Apr 2025 04:11:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 18 Apr 2025 04:11:42 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 18 Apr 2025 04:11:42 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5dab9cfa2f7ef2b19e95e68d27e3d0b208d9016da1b04298c500e78281a15e7`  
		Last Modified: Fri, 18 Apr 2025 04:11:48 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d0b032347a8dcb65e359d04c00733934bf6cfe61db4b1142a1df5f3de23a9cc`  
		Last Modified: Fri, 18 Apr 2025 04:11:47 GMT  
		Size: 6.5 MB (6455931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497b3350d5c31834bcca73478d5fc7c0d3c546c1676c042e1e9d1ec9afc85bdd`  
		Last Modified: Fri, 18 Apr 2025 04:11:46 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658de08330e9b739dfbff680b38b2bb55dc4b4aec6d4064b19ecc24c7ba9a8aa`  
		Last Modified: Fri, 18 Apr 2025 04:11:46 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0312f657691b722f56e7ed6bc33b2119988f7f21d9853fe0a8dcc79a3b5aec`  
		Last Modified: Fri, 18 Apr 2025 04:11:46 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fc9ae19d64bc742bb97a1eec58e04de0d2eab1eb71186876fed513a4b21a3d`  
		Last Modified: Fri, 18 Apr 2025 04:11:46 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-nanoserver-1809`

```console
$ docker pull nats@sha256:714b0b324ae5c514cc8066861c1ea58b8e852b21686bd57938b4cad501106b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `nats:2.11-nanoserver-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull nats@sha256:70dfa0a823409d278307a2f602a989bb5088fc2ed408add1628e7026065e4f7f
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.2 MB (115214035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c10544dab15e09a82ee58dfe65c5cebe6e37634a0fc0e40720019d69e49ec056`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Fri, 18 Apr 2025 04:11:39 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 18 Apr 2025 04:11:40 GMT
RUN cmd /S /C #(nop) COPY file:eee3870bfbcd9bfddd3622d20a6c2075b583b61ab0944602ceefed02dee11aa2 in C:\nats-server.exe 
# Fri, 18 Apr 2025 04:11:41 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Fri, 18 Apr 2025 04:11:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 18 Apr 2025 04:11:42 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 18 Apr 2025 04:11:42 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5dab9cfa2f7ef2b19e95e68d27e3d0b208d9016da1b04298c500e78281a15e7`  
		Last Modified: Fri, 18 Apr 2025 04:11:48 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d0b032347a8dcb65e359d04c00733934bf6cfe61db4b1142a1df5f3de23a9cc`  
		Last Modified: Fri, 18 Apr 2025 04:11:47 GMT  
		Size: 6.5 MB (6455931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497b3350d5c31834bcca73478d5fc7c0d3c546c1676c042e1e9d1ec9afc85bdd`  
		Last Modified: Fri, 18 Apr 2025 04:11:46 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658de08330e9b739dfbff680b38b2bb55dc4b4aec6d4064b19ecc24c7ba9a8aa`  
		Last Modified: Fri, 18 Apr 2025 04:11:46 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0312f657691b722f56e7ed6bc33b2119988f7f21d9853fe0a8dcc79a3b5aec`  
		Last Modified: Fri, 18 Apr 2025 04:11:46 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fc9ae19d64bc742bb97a1eec58e04de0d2eab1eb71186876fed513a4b21a3d`  
		Last Modified: Fri, 18 Apr 2025 04:11:46 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-scratch`

```console
$ docker pull nats@sha256:4bb7463f82c83da51fd098d9ddbc0dccfdc7415e110b02de375f60066b392878
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

### `nats:2.11-scratch` - linux; amd64

```console
$ docker pull nats@sha256:41dddbc7a9265892086db802a374dbf910b5d0db786c8ba12e27a81f2ede8f05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6282680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ddda49ccc5be8fc53872fcb74f0f168368af1d3e5fc27fd096bb4ab9fac9e5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7a31ab99389a11bb36db183df5a6bc8d784c1e96fb10c1973e04b98e17e58f51`  
		Last Modified: Tue, 08 Apr 2025 17:26:21 GMT  
		Size: 6.3 MB (6282171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bcd18a1de501f0dcf00113b8c1effd2b7f198a1383c537490e8dce3a826adce`  
		Last Modified: Tue, 08 Apr 2025 21:07:44 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:16692b029d2fd73a6c9833d59190a10a052903fbc5b68228ca0ce31e25895ee4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a60659f991d784a3586e62308c55e27054bad66d740cbde49980328b682cb858`

```dockerfile
```

-	Layers:
	-	`sha256:d0fd9d7883ec1e99c1a17109b0a6fd39dec7b9ec8f40f0ace2f2c15f9d8846a3`  
		Last Modified: Tue, 08 Apr 2025 21:07:45 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:f53994879dbfd2fc8177b383905d33db1095d8b42bb4bec64088771cecdb2bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6002072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01de3b3fb48e4b75539a9af5640e6f77115cdbe9419f3da2891472ec6e806148`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bc9bfb085b797367e9407dbdf5a3928ee0d69859fb96188165856b5e8e1b6e88`  
		Last Modified: Tue, 08 Apr 2025 17:26:22 GMT  
		Size: 6.0 MB (6001563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef30b0264d904d40fbf4763922653522d80a800c24f6bcbb52a1a66fd1accaf8`  
		Last Modified: Tue, 08 Apr 2025 21:07:08 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:f9537be10194b98f78298fad26add4a04948857f650479e674587da738dcf69c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7014bcdaac4c9653a29f6fc739854477633a62a69bd0cba053bbeecbfc57e101`

```dockerfile
```

-	Layers:
	-	`sha256:e337d587115a4b810f5a9fa3deb1db109744f3828488f355e6bfa4c965ea5501`  
		Last Modified: Tue, 08 Apr 2025 21:07:08 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:859b07690a2059b52277aceb9feed7e81269aed09859f1c3b0f3162d751ddb29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5992346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e38aded7ecfd1e1b61cc0452d01e01718e0a4be4ee666ac1980ddacb6f7defbc`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8f114aa547686a4604d8f5fbabd3d89b59a801cc55b68aa653d813c66ca32a65`  
		Last Modified: Tue, 08 Apr 2025 17:26:18 GMT  
		Size: 6.0 MB (5991835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844018e59249593be5d829b3a4bba323e96c26297db204b3a8a8a52e847f8041`  
		Last Modified: Tue, 08 Apr 2025 21:25:07 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:1e53207f824b4b97a2158a01c60662ef62ff32a777e55e615077563d48bcc314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a229febf9f435367bc3df4661afe24971b0581fa0b4b375a92d4ac38c3ce791`

```dockerfile
```

-	Layers:
	-	`sha256:36f6e0df21021319068725c9d7c2325e4fad06927e5ff9fe7fe11ec830f17f1c`  
		Last Modified: Tue, 08 Apr 2025 21:25:06 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:9142b78e748793c9e3b2fda3ac3800e66e866bf0147d634a7aea592f973a023a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5776867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee76a21b5d66ec40c0c8c53a6af4ed91124f7a2820ab80bf20279efdc3e689c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6b90b986da10be1b936fe6989055b49edb315427df0ceb03d1dd2f9dd98fb88`  
		Last Modified: Tue, 08 Apr 2025 17:26:18 GMT  
		Size: 5.8 MB (5776357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5e46c8b1d8619650c3d1afbfcf70b02949ce40d6fd6eb7d769bdc98a1def25`  
		Last Modified: Wed, 09 Apr 2025 00:53:02 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:9f289daca75844d624973e2b4e4a78db9e2026bfd59d743648f68e3c13d32a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53971055b1ebeea168a941b88f41f089dd9886aa55cbebe6b4f12f98ddb49666`

```dockerfile
```

-	Layers:
	-	`sha256:a65f769c9cecfc76c232cf377b8548ffd7fc82eae67b781487e0924b3319a183`  
		Last Modified: Wed, 09 Apr 2025 00:53:02 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:8cbd8caa2bdb9c64319ae113af4cf4170b92f3795148cb20401f2f1f16aa1d11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5757631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ba2ae7e87afe027065399c01f1230c431bed76a811a5cc5c83e971b6e70a26`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2c03c8b47070105a3781cfd93e5a048f0fcf1895182b8500a1875b914beccc2b`  
		Last Modified: Tue, 08 Apr 2025 17:26:19 GMT  
		Size: 5.8 MB (5757122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425937f6cd03177f214b970352644a3316a1a6ac085099e96875d62e6eb6b95d`  
		Last Modified: Tue, 08 Apr 2025 22:18:51 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:5aa97ff134b80e48aaa63c71d9c8343062cb648de6445e6d078b62dab5b08a3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8af43893a1163e246e9f97ae6b6ca899d5147c74db410070388f3dc6b1bb9a`

```dockerfile
```

-	Layers:
	-	`sha256:b2dde84b1c72b35f921945f0d6bec4b01ff2c811e34deff66dc5a99577731ade`  
		Last Modified: Tue, 08 Apr 2025 22:18:51 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; s390x

```console
$ docker pull nats@sha256:24602554caa826a00e26b3dae9c589026eaab3e0ad8e59cb573cac3996e62f8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6122577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7976c47bfec0473931b30ef2753bdc1cefde06b7a03f869cabb36b78aee6fd30`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:096b0701966ee2a29da8fc2c3f8ad25d2a0bb1211425d296e92558196ebe09c9`  
		Last Modified: Tue, 08 Apr 2025 17:26:22 GMT  
		Size: 6.1 MB (6122069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50402e49c7c832b57fb874a3e012194a27d09597f2d39ddc97db3701ae5bfb7`  
		Last Modified: Tue, 08 Apr 2025 22:07:44 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:6f2d2b491eee799540891efc47f6f00293192e82097e7b80bb5fd571bbf312c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8736b1c1aaa3dce6b14a6b7b5cad1d5cc142fae7d7d9fd17b8a6d72e67a82268`

```dockerfile
```

-	Layers:
	-	`sha256:1ab1e3d26d57dec0dbbe6b34b8c0c23c6308ed6e3e58b9267695ff2247985c40`  
		Last Modified: Tue, 08 Apr 2025 22:07:44 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11-windowsservercore`

```console
$ docker pull nats@sha256:d50be1cda62b37ce5581671dafc900fc728a2c95a2497d7a1a3f76578329fa81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `nats:2.11-windowsservercore` - windows version 10.0.17763.7249; amd64

```console
$ docker pull nats@sha256:de12da09e1602e2f93ed8b9b9897000258cf9608c390bc2620472c61a146810b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2172650201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f8e26de837c3eb00f55fdb3ea32e3a8eca48f3f6f7163fe633b78ed5241d985`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Fri, 18 Apr 2025 03:15:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 18 Apr 2025 03:15:31 GMT
ENV NATS_DOCKERIZED=1
# Fri, 18 Apr 2025 03:15:32 GMT
ENV NATS_SERVER=2.11.1
# Fri, 18 Apr 2025 03:15:33 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.1/nats-server-v2.11.1-windows-amd64.zip
# Fri, 18 Apr 2025 03:15:34 GMT
ENV NATS_SERVER_SHASUM=f5594798e1b77013b674c0049070d2502c20ee6f03a04d854cac333e2a21ca20
# Fri, 18 Apr 2025 03:16:07 GMT
RUN Set-PSDebug -Trace 2
# Fri, 18 Apr 2025 03:16:25 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 18 Apr 2025 03:16:26 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Fri, 18 Apr 2025 03:16:27 GMT
EXPOSE 4222 6222 8222
# Fri, 18 Apr 2025 03:16:27 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 18 Apr 2025 03:16:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Fri, 18 Apr 2025 03:13:03 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7822538d66aa517be43d1d696a9cc338fba7d6950e51918ac111ff32439b76d`  
		Last Modified: Fri, 18 Apr 2025 03:16:32 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:352f9e3e8b1aeaa1335f9d9417867a41164c3927fc6b5260d2f8c727d7ce3537`  
		Last Modified: Fri, 18 Apr 2025 03:16:32 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1f23260e2b6c00f1d9e28c5e37d7bdd45320561ed314845ff8d9ad8815ba79`  
		Last Modified: Fri, 18 Apr 2025 03:16:32 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66dc359cc850871940050c1e2fa57ba9ee16d9b033fba1532255cc0ea7a487da`  
		Last Modified: Fri, 18 Apr 2025 03:16:31 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd3feaf085072d792e35ade328ab0c2c1ecf53fd61f3c21f296549840710430`  
		Last Modified: Fri, 18 Apr 2025 03:16:31 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dae23d135bd9c3a0f11a7fb76e406cf4f5492a7988bdc3d9611f746ebb6945c`  
		Last Modified: Fri, 18 Apr 2025 03:16:31 GMT  
		Size: 322.6 KB (322628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bcdffa91604493a08769e767b51db8f8bc176116e8019a081a432923b5cb8d2`  
		Last Modified: Fri, 18 Apr 2025 03:16:31 GMT  
		Size: 6.8 MB (6789581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270410cf637c0ea7c99ed52451d17b6129481750e0caf3e12ad1cab37a0cb3ce`  
		Last Modified: Fri, 18 Apr 2025 03:16:30 GMT  
		Size: 1.8 KB (1849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2ad53fbd757d0e60898d5ee40e6355c43e9a4862e5b82429752248dbd9a85b6`  
		Last Modified: Fri, 18 Apr 2025 03:16:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c32fbcc93f5bdc7d627e5633180fff8d0b1759564412e5571800b97b912e371e`  
		Last Modified: Fri, 18 Apr 2025 03:16:30 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7c6da8a76e3b31cfa4ea2184896009c2dc8b62dd7f14fb45739484b9d6189f9`  
		Last Modified: Fri, 18 Apr 2025 03:16:31 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-windowsservercore-1809`

```console
$ docker pull nats@sha256:d50be1cda62b37ce5581671dafc900fc728a2c95a2497d7a1a3f76578329fa81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `nats:2.11-windowsservercore-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull nats@sha256:de12da09e1602e2f93ed8b9b9897000258cf9608c390bc2620472c61a146810b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2172650201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f8e26de837c3eb00f55fdb3ea32e3a8eca48f3f6f7163fe633b78ed5241d985`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Fri, 18 Apr 2025 03:15:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 18 Apr 2025 03:15:31 GMT
ENV NATS_DOCKERIZED=1
# Fri, 18 Apr 2025 03:15:32 GMT
ENV NATS_SERVER=2.11.1
# Fri, 18 Apr 2025 03:15:33 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.1/nats-server-v2.11.1-windows-amd64.zip
# Fri, 18 Apr 2025 03:15:34 GMT
ENV NATS_SERVER_SHASUM=f5594798e1b77013b674c0049070d2502c20ee6f03a04d854cac333e2a21ca20
# Fri, 18 Apr 2025 03:16:07 GMT
RUN Set-PSDebug -Trace 2
# Fri, 18 Apr 2025 03:16:25 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 18 Apr 2025 03:16:26 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Fri, 18 Apr 2025 03:16:27 GMT
EXPOSE 4222 6222 8222
# Fri, 18 Apr 2025 03:16:27 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 18 Apr 2025 03:16:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Fri, 18 Apr 2025 03:13:03 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7822538d66aa517be43d1d696a9cc338fba7d6950e51918ac111ff32439b76d`  
		Last Modified: Fri, 18 Apr 2025 03:16:32 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:352f9e3e8b1aeaa1335f9d9417867a41164c3927fc6b5260d2f8c727d7ce3537`  
		Last Modified: Fri, 18 Apr 2025 03:16:32 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1f23260e2b6c00f1d9e28c5e37d7bdd45320561ed314845ff8d9ad8815ba79`  
		Last Modified: Fri, 18 Apr 2025 03:16:32 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66dc359cc850871940050c1e2fa57ba9ee16d9b033fba1532255cc0ea7a487da`  
		Last Modified: Fri, 18 Apr 2025 03:16:31 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd3feaf085072d792e35ade328ab0c2c1ecf53fd61f3c21f296549840710430`  
		Last Modified: Fri, 18 Apr 2025 03:16:31 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dae23d135bd9c3a0f11a7fb76e406cf4f5492a7988bdc3d9611f746ebb6945c`  
		Last Modified: Fri, 18 Apr 2025 03:16:31 GMT  
		Size: 322.6 KB (322628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bcdffa91604493a08769e767b51db8f8bc176116e8019a081a432923b5cb8d2`  
		Last Modified: Fri, 18 Apr 2025 03:16:31 GMT  
		Size: 6.8 MB (6789581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270410cf637c0ea7c99ed52451d17b6129481750e0caf3e12ad1cab37a0cb3ce`  
		Last Modified: Fri, 18 Apr 2025 03:16:30 GMT  
		Size: 1.8 KB (1849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2ad53fbd757d0e60898d5ee40e6355c43e9a4862e5b82429752248dbd9a85b6`  
		Last Modified: Fri, 18 Apr 2025 03:16:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c32fbcc93f5bdc7d627e5633180fff8d0b1759564412e5571800b97b912e371e`  
		Last Modified: Fri, 18 Apr 2025 03:16:30 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7c6da8a76e3b31cfa4ea2184896009c2dc8b62dd7f14fb45739484b9d6189f9`  
		Last Modified: Fri, 18 Apr 2025 03:16:31 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11.2`

```console
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `nats:2.11.2-alpine`

```console
$ docker pull nats@sha256:3a0146ad423a4ab99a4ca6df797401fa60e96289fa21c1370909a73d6122134b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `nats:2.11.2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:b25ce7d7cfb629d1a132ae08b8fd84da4ab34c224fc57a9366f4f7e8284a89b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9849553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5bc00749e465a4c423af0395ea8a620f5184198a26aa70c550afb018dcd620d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da0a4b9d57d2a4c2439f0c8731b7e1ef8f0a7f2a1edf643d5f50a73ffc0c31f9' ;; 		armhf) natsArch='arm6'; sha256='2370e8d794acb0f176be0f0885f9930fa9d8d1276f15162eb8db336467279bc1' ;; 		armv7) natsArch='arm7'; sha256='46b038e57ad586f05342dcd3b29a2c2597217c19172a916eef9187170f024ad8' ;; 		x86_64) natsArch='amd64'; sha256='a123c8e43abe5ca8f0bff9393547f20f4bbac6fc0fb3c586ec031855911c414a' ;; 		x86) natsArch='386'; sha256='03bf7db9323c453b1257c3a43a21fcd5a975a2cc136c4bbeab7c0e815939e37e' ;; 		s390x) natsArch='s390x'; sha256='eb40e4a843124198b7e8625b7cccbd52810d63db17e1557d59681f5f29be5a98' ;; 		ppc64le) natsArch='ppc64le'; sha256='28e2afbca41dffe453507a993291560bfc57c6f43fe435604f894c3d91426dd0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53314fd665bd0c97ace20b7fb2ca1b46ecfdd7426150f8745639bb7704613d5a`  
		Last Modified: Fri, 25 Apr 2025 17:47:34 GMT  
		Size: 6.5 MB (6483851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cefa71e52d2f6e7b13aac0c8fe523facca0507ac8e8b180b168eeadfd046b89`  
		Last Modified: Fri, 25 Apr 2025 17:47:33 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c198696667425fcef5f606fda093ce31277d14ed9b5dc1592fb47511143d5052`  
		Last Modified: Fri, 25 Apr 2025 17:47:33 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:20a327f5442b5e1a069fb161658d8b9436e0f0ce2df3802ad9d74362036c2210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b2f873973386278768ee962ed71409b2376682ae823894072e19be8cde68680`

```dockerfile
```

-	Layers:
	-	`sha256:9122357572edf020a23a1bbf0fbe37650762d41d728dfaccb594f7e5890cbd2d`  
		Last Modified: Fri, 25 Apr 2025 17:47:33 GMT  
		Size: 14.4 KB (14424 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:4fe60f222966727f3e81dbb3bf2aaec58c7c8b573afbe318f6cb2c70c19f37c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10254225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5d5d918ca9a0f7dd7c056851f2898f207c48f854da7954fc8fafc8fd1aa3021`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da0a4b9d57d2a4c2439f0c8731b7e1ef8f0a7f2a1edf643d5f50a73ffc0c31f9' ;; 		armhf) natsArch='arm6'; sha256='2370e8d794acb0f176be0f0885f9930fa9d8d1276f15162eb8db336467279bc1' ;; 		armv7) natsArch='arm7'; sha256='46b038e57ad586f05342dcd3b29a2c2597217c19172a916eef9187170f024ad8' ;; 		x86_64) natsArch='amd64'; sha256='a123c8e43abe5ca8f0bff9393547f20f4bbac6fc0fb3c586ec031855911c414a' ;; 		x86) natsArch='386'; sha256='03bf7db9323c453b1257c3a43a21fcd5a975a2cc136c4bbeab7c0e815939e37e' ;; 		s390x) natsArch='s390x'; sha256='eb40e4a843124198b7e8625b7cccbd52810d63db17e1557d59681f5f29be5a98' ;; 		ppc64le) natsArch='ppc64le'; sha256='28e2afbca41dffe453507a993291560bfc57c6f43fe435604f894c3d91426dd0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3febb0921652e8042f634bdcb7812f9a2ed40e073970e14a940960350b775dbf`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 6.3 MB (6260226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc226874bc3060e6e916fa3ef948812c54a012b6081a27eaab55addfec8b7473`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e367a33259d9c5e7a6a6b42c8482e8bc6930e1a713671c0cf2fd1b5c879eef01`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:fda84d5581ce64cec49def3b469b26e717bf64d28a817656b19e16da89e9ea25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a714d7bd3b6fd55a075f56b50fa0da44cf6616089161edf7a648ba47af3256`

```dockerfile
```

-	Layers:
	-	`sha256:5f55a5edc5478bd7d7c9bc7e0763ad4dee93ecffafd3ed2f7702e7ee06ae75b0`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 14.5 KB (14469 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11.2-alpine3.21`

```console
$ docker pull nats@sha256:3a0146ad423a4ab99a4ca6df797401fa60e96289fa21c1370909a73d6122134b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `nats:2.11.2-alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:b25ce7d7cfb629d1a132ae08b8fd84da4ab34c224fc57a9366f4f7e8284a89b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9849553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5bc00749e465a4c423af0395ea8a620f5184198a26aa70c550afb018dcd620d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da0a4b9d57d2a4c2439f0c8731b7e1ef8f0a7f2a1edf643d5f50a73ffc0c31f9' ;; 		armhf) natsArch='arm6'; sha256='2370e8d794acb0f176be0f0885f9930fa9d8d1276f15162eb8db336467279bc1' ;; 		armv7) natsArch='arm7'; sha256='46b038e57ad586f05342dcd3b29a2c2597217c19172a916eef9187170f024ad8' ;; 		x86_64) natsArch='amd64'; sha256='a123c8e43abe5ca8f0bff9393547f20f4bbac6fc0fb3c586ec031855911c414a' ;; 		x86) natsArch='386'; sha256='03bf7db9323c453b1257c3a43a21fcd5a975a2cc136c4bbeab7c0e815939e37e' ;; 		s390x) natsArch='s390x'; sha256='eb40e4a843124198b7e8625b7cccbd52810d63db17e1557d59681f5f29be5a98' ;; 		ppc64le) natsArch='ppc64le'; sha256='28e2afbca41dffe453507a993291560bfc57c6f43fe435604f894c3d91426dd0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53314fd665bd0c97ace20b7fb2ca1b46ecfdd7426150f8745639bb7704613d5a`  
		Last Modified: Fri, 25 Apr 2025 17:47:34 GMT  
		Size: 6.5 MB (6483851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cefa71e52d2f6e7b13aac0c8fe523facca0507ac8e8b180b168eeadfd046b89`  
		Last Modified: Fri, 25 Apr 2025 17:47:33 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c198696667425fcef5f606fda093ce31277d14ed9b5dc1592fb47511143d5052`  
		Last Modified: Fri, 25 Apr 2025 17:47:33 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:20a327f5442b5e1a069fb161658d8b9436e0f0ce2df3802ad9d74362036c2210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b2f873973386278768ee962ed71409b2376682ae823894072e19be8cde68680`

```dockerfile
```

-	Layers:
	-	`sha256:9122357572edf020a23a1bbf0fbe37650762d41d728dfaccb594f7e5890cbd2d`  
		Last Modified: Fri, 25 Apr 2025 17:47:33 GMT  
		Size: 14.4 KB (14424 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.2-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:4fe60f222966727f3e81dbb3bf2aaec58c7c8b573afbe318f6cb2c70c19f37c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10254225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5d5d918ca9a0f7dd7c056851f2898f207c48f854da7954fc8fafc8fd1aa3021`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da0a4b9d57d2a4c2439f0c8731b7e1ef8f0a7f2a1edf643d5f50a73ffc0c31f9' ;; 		armhf) natsArch='arm6'; sha256='2370e8d794acb0f176be0f0885f9930fa9d8d1276f15162eb8db336467279bc1' ;; 		armv7) natsArch='arm7'; sha256='46b038e57ad586f05342dcd3b29a2c2597217c19172a916eef9187170f024ad8' ;; 		x86_64) natsArch='amd64'; sha256='a123c8e43abe5ca8f0bff9393547f20f4bbac6fc0fb3c586ec031855911c414a' ;; 		x86) natsArch='386'; sha256='03bf7db9323c453b1257c3a43a21fcd5a975a2cc136c4bbeab7c0e815939e37e' ;; 		s390x) natsArch='s390x'; sha256='eb40e4a843124198b7e8625b7cccbd52810d63db17e1557d59681f5f29be5a98' ;; 		ppc64le) natsArch='ppc64le'; sha256='28e2afbca41dffe453507a993291560bfc57c6f43fe435604f894c3d91426dd0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3febb0921652e8042f634bdcb7812f9a2ed40e073970e14a940960350b775dbf`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 6.3 MB (6260226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc226874bc3060e6e916fa3ef948812c54a012b6081a27eaab55addfec8b7473`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e367a33259d9c5e7a6a6b42c8482e8bc6930e1a713671c0cf2fd1b5c879eef01`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:fda84d5581ce64cec49def3b469b26e717bf64d28a817656b19e16da89e9ea25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a714d7bd3b6fd55a075f56b50fa0da44cf6616089161edf7a648ba47af3256`

```dockerfile
```

-	Layers:
	-	`sha256:5f55a5edc5478bd7d7c9bc7e0763ad4dee93ecffafd3ed2f7702e7ee06ae75b0`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 14.5 KB (14469 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11.2-linux`

```console
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `nats:2.11.2-nanoserver`

```console
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `nats:2.11.2-nanoserver-1809`

```console
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `nats:2.11.2-scratch`

```console
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `nats:2.11.2-windowsservercore`

```console
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `nats:2.11.2-windowsservercore-1809`

```console
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `nats:alpine`

```console
$ docker pull nats@sha256:a6e0002b6027b9f64619750d8d2d535c54fe247b54050959be29bb69e6b0d1f1
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
$ docker pull nats@sha256:7cbd5f7f5326233bf97e186073144217f7b98b8cf904d0d83ba9ff08caf6f0d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10386082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a900eac76440acf8f75c33c7a37e9103f53d792b082074036e8ee5a2df6903ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
ENV NATS_SERVER=2.11.1
# Tue, 08 Apr 2025 17:23:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='27c90d8bc0ad10bfb38ef92bdea8528b4bfc5aa56afba91c790fb3921ea205a2' ;; 		armhf) natsArch='arm6'; sha256='8f9f2f4aa85c242f254a175c9455e9d00c6a0e7fc96b87a14ef3bd6d8762e900' ;; 		armv7) natsArch='arm7'; sha256='06dee81c2fd32639ae646112daaf9b84b71023bee88b16fd3324fd922095dda1' ;; 		x86_64) natsArch='amd64'; sha256='f1d9754bf34316d1f7d349b176ff0414c9cce742846bf2eec0b402eee35a638c' ;; 		x86) natsArch='386'; sha256='b746e832f96f07ee5958c99201b7a96695a3e1339f416342b9fd3c083a68dba7' ;; 		s390x) natsArch='s390x'; sha256='018ec95e10758c3e6ea14f034d3fe099234957dec8290bc5aa3480a8d77e3e29' ;; 		ppc64le) natsArch='ppc64le'; sha256='be0f9308ffcdfa36189afdf7e8116235995d7d20406c0fc7b8aa5b5f724aa3d6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bffd47baa898ba4523ccc09b26058ea27891e234ee7563e763b8f9bd29bde2e`  
		Last Modified: Tue, 08 Apr 2025 20:28:15 GMT  
		Size: 6.7 MB (6742867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63af34edcf916551729eef83c51841b9403e9bedf717838e0dedfe7e5bfa977b`  
		Last Modified: Tue, 08 Apr 2025 20:28:15 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9081de8dcbbc97f988fe2e6b0695f7eaea0f8774966c467ed29bd8602391ff9`  
		Last Modified: Tue, 08 Apr 2025 20:28:14 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:062f6b7155ed98648412670dffe43c7be1f4768f50bfa3fa63ba59b794ec300c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b2af7e3b213deee44fd319c5441ec699c53280a665cf650e9eec87b50af831`

```dockerfile
```

-	Layers:
	-	`sha256:df59247835527b1024e29a039c6dd53ac255e4500ded522b5e05635e9495a453`  
		Last Modified: Tue, 08 Apr 2025 20:28:15 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:b25ce7d7cfb629d1a132ae08b8fd84da4ab34c224fc57a9366f4f7e8284a89b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9849553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5bc00749e465a4c423af0395ea8a620f5184198a26aa70c550afb018dcd620d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da0a4b9d57d2a4c2439f0c8731b7e1ef8f0a7f2a1edf643d5f50a73ffc0c31f9' ;; 		armhf) natsArch='arm6'; sha256='2370e8d794acb0f176be0f0885f9930fa9d8d1276f15162eb8db336467279bc1' ;; 		armv7) natsArch='arm7'; sha256='46b038e57ad586f05342dcd3b29a2c2597217c19172a916eef9187170f024ad8' ;; 		x86_64) natsArch='amd64'; sha256='a123c8e43abe5ca8f0bff9393547f20f4bbac6fc0fb3c586ec031855911c414a' ;; 		x86) natsArch='386'; sha256='03bf7db9323c453b1257c3a43a21fcd5a975a2cc136c4bbeab7c0e815939e37e' ;; 		s390x) natsArch='s390x'; sha256='eb40e4a843124198b7e8625b7cccbd52810d63db17e1557d59681f5f29be5a98' ;; 		ppc64le) natsArch='ppc64le'; sha256='28e2afbca41dffe453507a993291560bfc57c6f43fe435604f894c3d91426dd0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53314fd665bd0c97ace20b7fb2ca1b46ecfdd7426150f8745639bb7704613d5a`  
		Last Modified: Fri, 25 Apr 2025 17:47:34 GMT  
		Size: 6.5 MB (6483851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cefa71e52d2f6e7b13aac0c8fe523facca0507ac8e8b180b168eeadfd046b89`  
		Last Modified: Fri, 25 Apr 2025 17:47:33 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c198696667425fcef5f606fda093ce31277d14ed9b5dc1592fb47511143d5052`  
		Last Modified: Fri, 25 Apr 2025 17:47:33 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:20a327f5442b5e1a069fb161658d8b9436e0f0ce2df3802ad9d74362036c2210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b2f873973386278768ee962ed71409b2376682ae823894072e19be8cde68680`

```dockerfile
```

-	Layers:
	-	`sha256:9122357572edf020a23a1bbf0fbe37650762d41d728dfaccb594f7e5890cbd2d`  
		Last Modified: Fri, 25 Apr 2025 17:47:33 GMT  
		Size: 14.4 KB (14424 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:2f0c0883a1c8a7dd3a93730ce2ca646928c272aba42b05b5d163f5e779696f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9552050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28191bc799228c242ab1ebf65c8eaa89c320b25a78ee799103e544b8250226d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
ENV NATS_SERVER=2.11.1
# Tue, 08 Apr 2025 17:23:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='27c90d8bc0ad10bfb38ef92bdea8528b4bfc5aa56afba91c790fb3921ea205a2' ;; 		armhf) natsArch='arm6'; sha256='8f9f2f4aa85c242f254a175c9455e9d00c6a0e7fc96b87a14ef3bd6d8762e900' ;; 		armv7) natsArch='arm7'; sha256='06dee81c2fd32639ae646112daaf9b84b71023bee88b16fd3324fd922095dda1' ;; 		x86_64) natsArch='amd64'; sha256='f1d9754bf34316d1f7d349b176ff0414c9cce742846bf2eec0b402eee35a638c' ;; 		x86) natsArch='386'; sha256='b746e832f96f07ee5958c99201b7a96695a3e1339f416342b9fd3c083a68dba7' ;; 		s390x) natsArch='s390x'; sha256='018ec95e10758c3e6ea14f034d3fe099234957dec8290bc5aa3480a8d77e3e29' ;; 		ppc64le) natsArch='ppc64le'; sha256='be0f9308ffcdfa36189afdf7e8116235995d7d20406c0fc7b8aa5b5f724aa3d6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b82717f71af9d7a4242a00c3efbdf445cc5b3122fb74530e7d5e2971036151`  
		Last Modified: Tue, 08 Apr 2025 20:32:08 GMT  
		Size: 6.5 MB (6452958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49791283070c29e615bbe60ca9b43f0b5c63e67560f09700c02a4920fc31499`  
		Last Modified: Tue, 08 Apr 2025 20:32:07 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ade19b2805065881eeef7b4e282331a2f7fbd91f70c6349b33b2d448e8dc64`  
		Last Modified: Tue, 08 Apr 2025 20:32:07 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:f66e974c49c5b42df6f26cfe23be843bed87adb4df5efde68922bcd9bcdb0654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45fd3c0542a49a774cbfafb32d74dcb38bb7230e53a346c90ea2dc92652e671d`

```dockerfile
```

-	Layers:
	-	`sha256:dafec31d0d294d05c575a7f27247bd7720e66c489584ce418ed700595bb00c9f`  
		Last Modified: Tue, 08 Apr 2025 20:32:07 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:4fe60f222966727f3e81dbb3bf2aaec58c7c8b573afbe318f6cb2c70c19f37c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10254225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5d5d918ca9a0f7dd7c056851f2898f207c48f854da7954fc8fafc8fd1aa3021`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da0a4b9d57d2a4c2439f0c8731b7e1ef8f0a7f2a1edf643d5f50a73ffc0c31f9' ;; 		armhf) natsArch='arm6'; sha256='2370e8d794acb0f176be0f0885f9930fa9d8d1276f15162eb8db336467279bc1' ;; 		armv7) natsArch='arm7'; sha256='46b038e57ad586f05342dcd3b29a2c2597217c19172a916eef9187170f024ad8' ;; 		x86_64) natsArch='amd64'; sha256='a123c8e43abe5ca8f0bff9393547f20f4bbac6fc0fb3c586ec031855911c414a' ;; 		x86) natsArch='386'; sha256='03bf7db9323c453b1257c3a43a21fcd5a975a2cc136c4bbeab7c0e815939e37e' ;; 		s390x) natsArch='s390x'; sha256='eb40e4a843124198b7e8625b7cccbd52810d63db17e1557d59681f5f29be5a98' ;; 		ppc64le) natsArch='ppc64le'; sha256='28e2afbca41dffe453507a993291560bfc57c6f43fe435604f894c3d91426dd0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3febb0921652e8042f634bdcb7812f9a2ed40e073970e14a940960350b775dbf`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 6.3 MB (6260226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc226874bc3060e6e916fa3ef948812c54a012b6081a27eaab55addfec8b7473`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e367a33259d9c5e7a6a6b42c8482e8bc6930e1a713671c0cf2fd1b5c879eef01`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:fda84d5581ce64cec49def3b469b26e717bf64d28a817656b19e16da89e9ea25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a714d7bd3b6fd55a075f56b50fa0da44cf6616089161edf7a648ba47af3256`

```dockerfile
```

-	Layers:
	-	`sha256:5f55a5edc5478bd7d7c9bc7e0763ad4dee93ecffafd3ed2f7702e7ee06ae75b0`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 14.5 KB (14469 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:6b6b1109a98eafc180bae27e0e27a1110433dfd3577e78cac2d8eb793969fc43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9797332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52bb4f9d9231f9b6c625e4a3a3f2874bd83248ad61158f697eb327444118f598`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
ENV NATS_SERVER=2.11.1
# Tue, 08 Apr 2025 17:23:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='27c90d8bc0ad10bfb38ef92bdea8528b4bfc5aa56afba91c790fb3921ea205a2' ;; 		armhf) natsArch='arm6'; sha256='8f9f2f4aa85c242f254a175c9455e9d00c6a0e7fc96b87a14ef3bd6d8762e900' ;; 		armv7) natsArch='arm7'; sha256='06dee81c2fd32639ae646112daaf9b84b71023bee88b16fd3324fd922095dda1' ;; 		x86_64) natsArch='amd64'; sha256='f1d9754bf34316d1f7d349b176ff0414c9cce742846bf2eec0b402eee35a638c' ;; 		x86) natsArch='386'; sha256='b746e832f96f07ee5958c99201b7a96695a3e1339f416342b9fd3c083a68dba7' ;; 		s390x) natsArch='s390x'; sha256='018ec95e10758c3e6ea14f034d3fe099234957dec8290bc5aa3480a8d77e3e29' ;; 		ppc64le) natsArch='ppc64le'; sha256='be0f9308ffcdfa36189afdf7e8116235995d7d20406c0fc7b8aa5b5f724aa3d6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8be7344e3eed187cfb792f8b098e4b9639bd0e5318ceffb68a33a3bad2164c`  
		Last Modified: Tue, 08 Apr 2025 20:42:59 GMT  
		Size: 6.2 MB (6222020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd19bdb0c54b34703a3579dcae0cd27d09d0ed9ac711591a13fba04c9a89aacf`  
		Last Modified: Tue, 08 Apr 2025 20:42:58 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2608514a04b63ea4ad3654f5acd693a1bc97dc1d1c8b8a1495df0e53dda6ff0`  
		Last Modified: Tue, 08 Apr 2025 20:42:58 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:28f492787cca2adfb7bcfcb21be59f4685caad51e81ff81fac96d5d46445c776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ada670995406f8a9d5e52233a0003738fc8c1933710c4de448e87af34e5a3863`

```dockerfile
```

-	Layers:
	-	`sha256:e269226b323faa520a451de66e148284583959e77af2bf7d56a4d350cc37623a`  
		Last Modified: Tue, 08 Apr 2025 20:42:58 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; s390x

```console
$ docker pull nats@sha256:cf54ecfbde97d03a9d1a1bfdbcf069c2683ef48f34d72013b9064f5ed0ab9183
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10053959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f94c74252361e5594561679a5358b7e135dd9c7c2f3c51be0138903f04c6aa8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
ENV NATS_SERVER=2.11.1
# Tue, 08 Apr 2025 17:23:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='27c90d8bc0ad10bfb38ef92bdea8528b4bfc5aa56afba91c790fb3921ea205a2' ;; 		armhf) natsArch='arm6'; sha256='8f9f2f4aa85c242f254a175c9455e9d00c6a0e7fc96b87a14ef3bd6d8762e900' ;; 		armv7) natsArch='arm7'; sha256='06dee81c2fd32639ae646112daaf9b84b71023bee88b16fd3324fd922095dda1' ;; 		x86_64) natsArch='amd64'; sha256='f1d9754bf34316d1f7d349b176ff0414c9cce742846bf2eec0b402eee35a638c' ;; 		x86) natsArch='386'; sha256='b746e832f96f07ee5958c99201b7a96695a3e1339f416342b9fd3c083a68dba7' ;; 		s390x) natsArch='s390x'; sha256='018ec95e10758c3e6ea14f034d3fe099234957dec8290bc5aa3480a8d77e3e29' ;; 		ppc64le) natsArch='ppc64le'; sha256='be0f9308ffcdfa36189afdf7e8116235995d7d20406c0fc7b8aa5b5f724aa3d6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a92fbe14b2cdd6c1a85f89f171cfbad87c0f00fc6205b2d6c5cfa29cf51cf30`  
		Last Modified: Tue, 08 Apr 2025 22:04:28 GMT  
		Size: 6.6 MB (6585420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc913d6647309b3286a51c5f87c54edfb961dd53b9ca8a4496335154e303ab2e`  
		Last Modified: Tue, 08 Apr 2025 22:04:28 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22b8967d9a9d213c271cc67dcbe1d89b5b0870a2d2a399344c51f7cdc25b2c7`  
		Last Modified: Tue, 08 Apr 2025 22:04:28 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:b55039b07dc68ae69425511e99ab099b60f707e9a565a17a0d28e21a33c1f346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4570b0028f776dbca1deaabac6952192f625b95ec93d8098c7058262a3ca4b9`

```dockerfile
```

-	Layers:
	-	`sha256:5b1859f0680f19779c89b10a96fe392f905b04060b6ca55b19696d4fc51ece7c`  
		Last Modified: Tue, 08 Apr 2025 22:04:28 GMT  
		Size: 14.3 KB (14316 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:alpine3.21`

```console
$ docker pull nats@sha256:a6e0002b6027b9f64619750d8d2d535c54fe247b54050959be29bb69e6b0d1f1
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
$ docker pull nats@sha256:7cbd5f7f5326233bf97e186073144217f7b98b8cf904d0d83ba9ff08caf6f0d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10386082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a900eac76440acf8f75c33c7a37e9103f53d792b082074036e8ee5a2df6903ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
ENV NATS_SERVER=2.11.1
# Tue, 08 Apr 2025 17:23:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='27c90d8bc0ad10bfb38ef92bdea8528b4bfc5aa56afba91c790fb3921ea205a2' ;; 		armhf) natsArch='arm6'; sha256='8f9f2f4aa85c242f254a175c9455e9d00c6a0e7fc96b87a14ef3bd6d8762e900' ;; 		armv7) natsArch='arm7'; sha256='06dee81c2fd32639ae646112daaf9b84b71023bee88b16fd3324fd922095dda1' ;; 		x86_64) natsArch='amd64'; sha256='f1d9754bf34316d1f7d349b176ff0414c9cce742846bf2eec0b402eee35a638c' ;; 		x86) natsArch='386'; sha256='b746e832f96f07ee5958c99201b7a96695a3e1339f416342b9fd3c083a68dba7' ;; 		s390x) natsArch='s390x'; sha256='018ec95e10758c3e6ea14f034d3fe099234957dec8290bc5aa3480a8d77e3e29' ;; 		ppc64le) natsArch='ppc64le'; sha256='be0f9308ffcdfa36189afdf7e8116235995d7d20406c0fc7b8aa5b5f724aa3d6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bffd47baa898ba4523ccc09b26058ea27891e234ee7563e763b8f9bd29bde2e`  
		Last Modified: Tue, 08 Apr 2025 20:28:15 GMT  
		Size: 6.7 MB (6742867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63af34edcf916551729eef83c51841b9403e9bedf717838e0dedfe7e5bfa977b`  
		Last Modified: Tue, 08 Apr 2025 20:28:15 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9081de8dcbbc97f988fe2e6b0695f7eaea0f8774966c467ed29bd8602391ff9`  
		Last Modified: Tue, 08 Apr 2025 20:28:14 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:062f6b7155ed98648412670dffe43c7be1f4768f50bfa3fa63ba59b794ec300c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b2af7e3b213deee44fd319c5441ec699c53280a665cf650e9eec87b50af831`

```dockerfile
```

-	Layers:
	-	`sha256:df59247835527b1024e29a039c6dd53ac255e4500ded522b5e05635e9495a453`  
		Last Modified: Tue, 08 Apr 2025 20:28:15 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:b25ce7d7cfb629d1a132ae08b8fd84da4ab34c224fc57a9366f4f7e8284a89b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9849553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5bc00749e465a4c423af0395ea8a620f5184198a26aa70c550afb018dcd620d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da0a4b9d57d2a4c2439f0c8731b7e1ef8f0a7f2a1edf643d5f50a73ffc0c31f9' ;; 		armhf) natsArch='arm6'; sha256='2370e8d794acb0f176be0f0885f9930fa9d8d1276f15162eb8db336467279bc1' ;; 		armv7) natsArch='arm7'; sha256='46b038e57ad586f05342dcd3b29a2c2597217c19172a916eef9187170f024ad8' ;; 		x86_64) natsArch='amd64'; sha256='a123c8e43abe5ca8f0bff9393547f20f4bbac6fc0fb3c586ec031855911c414a' ;; 		x86) natsArch='386'; sha256='03bf7db9323c453b1257c3a43a21fcd5a975a2cc136c4bbeab7c0e815939e37e' ;; 		s390x) natsArch='s390x'; sha256='eb40e4a843124198b7e8625b7cccbd52810d63db17e1557d59681f5f29be5a98' ;; 		ppc64le) natsArch='ppc64le'; sha256='28e2afbca41dffe453507a993291560bfc57c6f43fe435604f894c3d91426dd0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53314fd665bd0c97ace20b7fb2ca1b46ecfdd7426150f8745639bb7704613d5a`  
		Last Modified: Fri, 25 Apr 2025 17:47:34 GMT  
		Size: 6.5 MB (6483851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cefa71e52d2f6e7b13aac0c8fe523facca0507ac8e8b180b168eeadfd046b89`  
		Last Modified: Fri, 25 Apr 2025 17:47:33 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c198696667425fcef5f606fda093ce31277d14ed9b5dc1592fb47511143d5052`  
		Last Modified: Fri, 25 Apr 2025 17:47:33 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:20a327f5442b5e1a069fb161658d8b9436e0f0ce2df3802ad9d74362036c2210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b2f873973386278768ee962ed71409b2376682ae823894072e19be8cde68680`

```dockerfile
```

-	Layers:
	-	`sha256:9122357572edf020a23a1bbf0fbe37650762d41d728dfaccb594f7e5890cbd2d`  
		Last Modified: Fri, 25 Apr 2025 17:47:33 GMT  
		Size: 14.4 KB (14424 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:2f0c0883a1c8a7dd3a93730ce2ca646928c272aba42b05b5d163f5e779696f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9552050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28191bc799228c242ab1ebf65c8eaa89c320b25a78ee799103e544b8250226d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
ENV NATS_SERVER=2.11.1
# Tue, 08 Apr 2025 17:23:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='27c90d8bc0ad10bfb38ef92bdea8528b4bfc5aa56afba91c790fb3921ea205a2' ;; 		armhf) natsArch='arm6'; sha256='8f9f2f4aa85c242f254a175c9455e9d00c6a0e7fc96b87a14ef3bd6d8762e900' ;; 		armv7) natsArch='arm7'; sha256='06dee81c2fd32639ae646112daaf9b84b71023bee88b16fd3324fd922095dda1' ;; 		x86_64) natsArch='amd64'; sha256='f1d9754bf34316d1f7d349b176ff0414c9cce742846bf2eec0b402eee35a638c' ;; 		x86) natsArch='386'; sha256='b746e832f96f07ee5958c99201b7a96695a3e1339f416342b9fd3c083a68dba7' ;; 		s390x) natsArch='s390x'; sha256='018ec95e10758c3e6ea14f034d3fe099234957dec8290bc5aa3480a8d77e3e29' ;; 		ppc64le) natsArch='ppc64le'; sha256='be0f9308ffcdfa36189afdf7e8116235995d7d20406c0fc7b8aa5b5f724aa3d6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b82717f71af9d7a4242a00c3efbdf445cc5b3122fb74530e7d5e2971036151`  
		Last Modified: Tue, 08 Apr 2025 20:32:08 GMT  
		Size: 6.5 MB (6452958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49791283070c29e615bbe60ca9b43f0b5c63e67560f09700c02a4920fc31499`  
		Last Modified: Tue, 08 Apr 2025 20:32:07 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ade19b2805065881eeef7b4e282331a2f7fbd91f70c6349b33b2d448e8dc64`  
		Last Modified: Tue, 08 Apr 2025 20:32:07 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:f66e974c49c5b42df6f26cfe23be843bed87adb4df5efde68922bcd9bcdb0654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45fd3c0542a49a774cbfafb32d74dcb38bb7230e53a346c90ea2dc92652e671d`

```dockerfile
```

-	Layers:
	-	`sha256:dafec31d0d294d05c575a7f27247bd7720e66c489584ce418ed700595bb00c9f`  
		Last Modified: Tue, 08 Apr 2025 20:32:07 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:4fe60f222966727f3e81dbb3bf2aaec58c7c8b573afbe318f6cb2c70c19f37c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10254225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5d5d918ca9a0f7dd7c056851f2898f207c48f854da7954fc8fafc8fd1aa3021`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da0a4b9d57d2a4c2439f0c8731b7e1ef8f0a7f2a1edf643d5f50a73ffc0c31f9' ;; 		armhf) natsArch='arm6'; sha256='2370e8d794acb0f176be0f0885f9930fa9d8d1276f15162eb8db336467279bc1' ;; 		armv7) natsArch='arm7'; sha256='46b038e57ad586f05342dcd3b29a2c2597217c19172a916eef9187170f024ad8' ;; 		x86_64) natsArch='amd64'; sha256='a123c8e43abe5ca8f0bff9393547f20f4bbac6fc0fb3c586ec031855911c414a' ;; 		x86) natsArch='386'; sha256='03bf7db9323c453b1257c3a43a21fcd5a975a2cc136c4bbeab7c0e815939e37e' ;; 		s390x) natsArch='s390x'; sha256='eb40e4a843124198b7e8625b7cccbd52810d63db17e1557d59681f5f29be5a98' ;; 		ppc64le) natsArch='ppc64le'; sha256='28e2afbca41dffe453507a993291560bfc57c6f43fe435604f894c3d91426dd0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3febb0921652e8042f634bdcb7812f9a2ed40e073970e14a940960350b775dbf`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 6.3 MB (6260226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc226874bc3060e6e916fa3ef948812c54a012b6081a27eaab55addfec8b7473`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e367a33259d9c5e7a6a6b42c8482e8bc6930e1a713671c0cf2fd1b5c879eef01`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:fda84d5581ce64cec49def3b469b26e717bf64d28a817656b19e16da89e9ea25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a714d7bd3b6fd55a075f56b50fa0da44cf6616089161edf7a648ba47af3256`

```dockerfile
```

-	Layers:
	-	`sha256:5f55a5edc5478bd7d7c9bc7e0763ad4dee93ecffafd3ed2f7702e7ee06ae75b0`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 14.5 KB (14469 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:6b6b1109a98eafc180bae27e0e27a1110433dfd3577e78cac2d8eb793969fc43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9797332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52bb4f9d9231f9b6c625e4a3a3f2874bd83248ad61158f697eb327444118f598`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
ENV NATS_SERVER=2.11.1
# Tue, 08 Apr 2025 17:23:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='27c90d8bc0ad10bfb38ef92bdea8528b4bfc5aa56afba91c790fb3921ea205a2' ;; 		armhf) natsArch='arm6'; sha256='8f9f2f4aa85c242f254a175c9455e9d00c6a0e7fc96b87a14ef3bd6d8762e900' ;; 		armv7) natsArch='arm7'; sha256='06dee81c2fd32639ae646112daaf9b84b71023bee88b16fd3324fd922095dda1' ;; 		x86_64) natsArch='amd64'; sha256='f1d9754bf34316d1f7d349b176ff0414c9cce742846bf2eec0b402eee35a638c' ;; 		x86) natsArch='386'; sha256='b746e832f96f07ee5958c99201b7a96695a3e1339f416342b9fd3c083a68dba7' ;; 		s390x) natsArch='s390x'; sha256='018ec95e10758c3e6ea14f034d3fe099234957dec8290bc5aa3480a8d77e3e29' ;; 		ppc64le) natsArch='ppc64le'; sha256='be0f9308ffcdfa36189afdf7e8116235995d7d20406c0fc7b8aa5b5f724aa3d6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8be7344e3eed187cfb792f8b098e4b9639bd0e5318ceffb68a33a3bad2164c`  
		Last Modified: Tue, 08 Apr 2025 20:42:59 GMT  
		Size: 6.2 MB (6222020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd19bdb0c54b34703a3579dcae0cd27d09d0ed9ac711591a13fba04c9a89aacf`  
		Last Modified: Tue, 08 Apr 2025 20:42:58 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2608514a04b63ea4ad3654f5acd693a1bc97dc1d1c8b8a1495df0e53dda6ff0`  
		Last Modified: Tue, 08 Apr 2025 20:42:58 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:28f492787cca2adfb7bcfcb21be59f4685caad51e81ff81fac96d5d46445c776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ada670995406f8a9d5e52233a0003738fc8c1933710c4de448e87af34e5a3863`

```dockerfile
```

-	Layers:
	-	`sha256:e269226b323faa520a451de66e148284583959e77af2bf7d56a4d350cc37623a`  
		Last Modified: Tue, 08 Apr 2025 20:42:58 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:cf54ecfbde97d03a9d1a1bfdbcf069c2683ef48f34d72013b9064f5ed0ab9183
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10053959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f94c74252361e5594561679a5358b7e135dd9c7c2f3c51be0138903f04c6aa8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
ENV NATS_SERVER=2.11.1
# Tue, 08 Apr 2025 17:23:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='27c90d8bc0ad10bfb38ef92bdea8528b4bfc5aa56afba91c790fb3921ea205a2' ;; 		armhf) natsArch='arm6'; sha256='8f9f2f4aa85c242f254a175c9455e9d00c6a0e7fc96b87a14ef3bd6d8762e900' ;; 		armv7) natsArch='arm7'; sha256='06dee81c2fd32639ae646112daaf9b84b71023bee88b16fd3324fd922095dda1' ;; 		x86_64) natsArch='amd64'; sha256='f1d9754bf34316d1f7d349b176ff0414c9cce742846bf2eec0b402eee35a638c' ;; 		x86) natsArch='386'; sha256='b746e832f96f07ee5958c99201b7a96695a3e1339f416342b9fd3c083a68dba7' ;; 		s390x) natsArch='s390x'; sha256='018ec95e10758c3e6ea14f034d3fe099234957dec8290bc5aa3480a8d77e3e29' ;; 		ppc64le) natsArch='ppc64le'; sha256='be0f9308ffcdfa36189afdf7e8116235995d7d20406c0fc7b8aa5b5f724aa3d6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a92fbe14b2cdd6c1a85f89f171cfbad87c0f00fc6205b2d6c5cfa29cf51cf30`  
		Last Modified: Tue, 08 Apr 2025 22:04:28 GMT  
		Size: 6.6 MB (6585420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc913d6647309b3286a51c5f87c54edfb961dd53b9ca8a4496335154e303ab2e`  
		Last Modified: Tue, 08 Apr 2025 22:04:28 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22b8967d9a9d213c271cc67dcbe1d89b5b0870a2d2a399344c51f7cdc25b2c7`  
		Last Modified: Tue, 08 Apr 2025 22:04:28 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:b55039b07dc68ae69425511e99ab099b60f707e9a565a17a0d28e21a33c1f346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4570b0028f776dbca1deaabac6952192f625b95ec93d8098c7058262a3ca4b9`

```dockerfile
```

-	Layers:
	-	`sha256:5b1859f0680f19779c89b10a96fe392f905b04060b6ca55b19696d4fc51ece7c`  
		Last Modified: Tue, 08 Apr 2025 22:04:28 GMT  
		Size: 14.3 KB (14316 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:latest`

```console
$ docker pull nats@sha256:29ae7f55fbaa9d23949237c58593a3451ef74493e5b3644d6a837219d1d4028c
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
	-	windows version 10.0.17763.7249; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:41dddbc7a9265892086db802a374dbf910b5d0db786c8ba12e27a81f2ede8f05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6282680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ddda49ccc5be8fc53872fcb74f0f168368af1d3e5fc27fd096bb4ab9fac9e5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7a31ab99389a11bb36db183df5a6bc8d784c1e96fb10c1973e04b98e17e58f51`  
		Last Modified: Tue, 08 Apr 2025 17:26:21 GMT  
		Size: 6.3 MB (6282171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bcd18a1de501f0dcf00113b8c1effd2b7f198a1383c537490e8dce3a826adce`  
		Last Modified: Tue, 08 Apr 2025 21:07:44 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:16692b029d2fd73a6c9833d59190a10a052903fbc5b68228ca0ce31e25895ee4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a60659f991d784a3586e62308c55e27054bad66d740cbde49980328b682cb858`

```dockerfile
```

-	Layers:
	-	`sha256:d0fd9d7883ec1e99c1a17109b0a6fd39dec7b9ec8f40f0ace2f2c15f9d8846a3`  
		Last Modified: Tue, 08 Apr 2025 21:07:45 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:f53994879dbfd2fc8177b383905d33db1095d8b42bb4bec64088771cecdb2bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6002072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01de3b3fb48e4b75539a9af5640e6f77115cdbe9419f3da2891472ec6e806148`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bc9bfb085b797367e9407dbdf5a3928ee0d69859fb96188165856b5e8e1b6e88`  
		Last Modified: Tue, 08 Apr 2025 17:26:22 GMT  
		Size: 6.0 MB (6001563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef30b0264d904d40fbf4763922653522d80a800c24f6bcbb52a1a66fd1accaf8`  
		Last Modified: Tue, 08 Apr 2025 21:07:08 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:f9537be10194b98f78298fad26add4a04948857f650479e674587da738dcf69c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7014bcdaac4c9653a29f6fc739854477633a62a69bd0cba053bbeecbfc57e101`

```dockerfile
```

-	Layers:
	-	`sha256:e337d587115a4b810f5a9fa3deb1db109744f3828488f355e6bfa4c965ea5501`  
		Last Modified: Tue, 08 Apr 2025 21:07:08 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:859b07690a2059b52277aceb9feed7e81269aed09859f1c3b0f3162d751ddb29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5992346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e38aded7ecfd1e1b61cc0452d01e01718e0a4be4ee666ac1980ddacb6f7defbc`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8f114aa547686a4604d8f5fbabd3d89b59a801cc55b68aa653d813c66ca32a65`  
		Last Modified: Tue, 08 Apr 2025 17:26:18 GMT  
		Size: 6.0 MB (5991835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844018e59249593be5d829b3a4bba323e96c26297db204b3a8a8a52e847f8041`  
		Last Modified: Tue, 08 Apr 2025 21:25:07 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:1e53207f824b4b97a2158a01c60662ef62ff32a777e55e615077563d48bcc314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a229febf9f435367bc3df4661afe24971b0581fa0b4b375a92d4ac38c3ce791`

```dockerfile
```

-	Layers:
	-	`sha256:36f6e0df21021319068725c9d7c2325e4fad06927e5ff9fe7fe11ec830f17f1c`  
		Last Modified: Tue, 08 Apr 2025 21:25:06 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:9142b78e748793c9e3b2fda3ac3800e66e866bf0147d634a7aea592f973a023a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5776867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee76a21b5d66ec40c0c8c53a6af4ed91124f7a2820ab80bf20279efdc3e689c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6b90b986da10be1b936fe6989055b49edb315427df0ceb03d1dd2f9dd98fb88`  
		Last Modified: Tue, 08 Apr 2025 17:26:18 GMT  
		Size: 5.8 MB (5776357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5e46c8b1d8619650c3d1afbfcf70b02949ce40d6fd6eb7d769bdc98a1def25`  
		Last Modified: Wed, 09 Apr 2025 00:53:02 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:9f289daca75844d624973e2b4e4a78db9e2026bfd59d743648f68e3c13d32a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53971055b1ebeea168a941b88f41f089dd9886aa55cbebe6b4f12f98ddb49666`

```dockerfile
```

-	Layers:
	-	`sha256:a65f769c9cecfc76c232cf377b8548ffd7fc82eae67b781487e0924b3319a183`  
		Last Modified: Wed, 09 Apr 2025 00:53:02 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; ppc64le

```console
$ docker pull nats@sha256:8cbd8caa2bdb9c64319ae113af4cf4170b92f3795148cb20401f2f1f16aa1d11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5757631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ba2ae7e87afe027065399c01f1230c431bed76a811a5cc5c83e971b6e70a26`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2c03c8b47070105a3781cfd93e5a048f0fcf1895182b8500a1875b914beccc2b`  
		Last Modified: Tue, 08 Apr 2025 17:26:19 GMT  
		Size: 5.8 MB (5757122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425937f6cd03177f214b970352644a3316a1a6ac085099e96875d62e6eb6b95d`  
		Last Modified: Tue, 08 Apr 2025 22:18:51 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:5aa97ff134b80e48aaa63c71d9c8343062cb648de6445e6d078b62dab5b08a3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8af43893a1163e246e9f97ae6b6ca899d5147c74db410070388f3dc6b1bb9a`

```dockerfile
```

-	Layers:
	-	`sha256:b2dde84b1c72b35f921945f0d6bec4b01ff2c811e34deff66dc5a99577731ade`  
		Last Modified: Tue, 08 Apr 2025 22:18:51 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; s390x

```console
$ docker pull nats@sha256:24602554caa826a00e26b3dae9c589026eaab3e0ad8e59cb573cac3996e62f8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6122577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7976c47bfec0473931b30ef2753bdc1cefde06b7a03f869cabb36b78aee6fd30`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:096b0701966ee2a29da8fc2c3f8ad25d2a0bb1211425d296e92558196ebe09c9`  
		Last Modified: Tue, 08 Apr 2025 17:26:22 GMT  
		Size: 6.1 MB (6122069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50402e49c7c832b57fb874a3e012194a27d09597f2d39ddc97db3701ae5bfb7`  
		Last Modified: Tue, 08 Apr 2025 22:07:44 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:6f2d2b491eee799540891efc47f6f00293192e82097e7b80bb5fd571bbf312c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8736b1c1aaa3dce6b14a6b7b5cad1d5cc142fae7d7d9fd17b8a6d72e67a82268`

```dockerfile
```

-	Layers:
	-	`sha256:1ab1e3d26d57dec0dbbe6b34b8c0c23c6308ed6e3e58b9267695ff2247985c40`  
		Last Modified: Tue, 08 Apr 2025 22:07:44 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - windows version 10.0.17763.7249; amd64

```console
$ docker pull nats@sha256:70dfa0a823409d278307a2f602a989bb5088fc2ed408add1628e7026065e4f7f
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.2 MB (115214035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c10544dab15e09a82ee58dfe65c5cebe6e37634a0fc0e40720019d69e49ec056`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Fri, 18 Apr 2025 04:11:39 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 18 Apr 2025 04:11:40 GMT
RUN cmd /S /C #(nop) COPY file:eee3870bfbcd9bfddd3622d20a6c2075b583b61ab0944602ceefed02dee11aa2 in C:\nats-server.exe 
# Fri, 18 Apr 2025 04:11:41 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Fri, 18 Apr 2025 04:11:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 18 Apr 2025 04:11:42 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 18 Apr 2025 04:11:42 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5dab9cfa2f7ef2b19e95e68d27e3d0b208d9016da1b04298c500e78281a15e7`  
		Last Modified: Fri, 18 Apr 2025 04:11:48 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d0b032347a8dcb65e359d04c00733934bf6cfe61db4b1142a1df5f3de23a9cc`  
		Last Modified: Fri, 18 Apr 2025 04:11:47 GMT  
		Size: 6.5 MB (6455931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497b3350d5c31834bcca73478d5fc7c0d3c546c1676c042e1e9d1ec9afc85bdd`  
		Last Modified: Fri, 18 Apr 2025 04:11:46 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658de08330e9b739dfbff680b38b2bb55dc4b4aec6d4064b19ecc24c7ba9a8aa`  
		Last Modified: Fri, 18 Apr 2025 04:11:46 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0312f657691b722f56e7ed6bc33b2119988f7f21d9853fe0a8dcc79a3b5aec`  
		Last Modified: Fri, 18 Apr 2025 04:11:46 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fc9ae19d64bc742bb97a1eec58e04de0d2eab1eb71186876fed513a4b21a3d`  
		Last Modified: Fri, 18 Apr 2025 04:11:46 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:4bb7463f82c83da51fd098d9ddbc0dccfdc7415e110b02de375f60066b392878
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
$ docker pull nats@sha256:41dddbc7a9265892086db802a374dbf910b5d0db786c8ba12e27a81f2ede8f05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6282680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ddda49ccc5be8fc53872fcb74f0f168368af1d3e5fc27fd096bb4ab9fac9e5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7a31ab99389a11bb36db183df5a6bc8d784c1e96fb10c1973e04b98e17e58f51`  
		Last Modified: Tue, 08 Apr 2025 17:26:21 GMT  
		Size: 6.3 MB (6282171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bcd18a1de501f0dcf00113b8c1effd2b7f198a1383c537490e8dce3a826adce`  
		Last Modified: Tue, 08 Apr 2025 21:07:44 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:16692b029d2fd73a6c9833d59190a10a052903fbc5b68228ca0ce31e25895ee4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a60659f991d784a3586e62308c55e27054bad66d740cbde49980328b682cb858`

```dockerfile
```

-	Layers:
	-	`sha256:d0fd9d7883ec1e99c1a17109b0a6fd39dec7b9ec8f40f0ace2f2c15f9d8846a3`  
		Last Modified: Tue, 08 Apr 2025 21:07:45 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:f53994879dbfd2fc8177b383905d33db1095d8b42bb4bec64088771cecdb2bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6002072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01de3b3fb48e4b75539a9af5640e6f77115cdbe9419f3da2891472ec6e806148`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bc9bfb085b797367e9407dbdf5a3928ee0d69859fb96188165856b5e8e1b6e88`  
		Last Modified: Tue, 08 Apr 2025 17:26:22 GMT  
		Size: 6.0 MB (6001563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef30b0264d904d40fbf4763922653522d80a800c24f6bcbb52a1a66fd1accaf8`  
		Last Modified: Tue, 08 Apr 2025 21:07:08 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:f9537be10194b98f78298fad26add4a04948857f650479e674587da738dcf69c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7014bcdaac4c9653a29f6fc739854477633a62a69bd0cba053bbeecbfc57e101`

```dockerfile
```

-	Layers:
	-	`sha256:e337d587115a4b810f5a9fa3deb1db109744f3828488f355e6bfa4c965ea5501`  
		Last Modified: Tue, 08 Apr 2025 21:07:08 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:859b07690a2059b52277aceb9feed7e81269aed09859f1c3b0f3162d751ddb29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5992346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e38aded7ecfd1e1b61cc0452d01e01718e0a4be4ee666ac1980ddacb6f7defbc`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8f114aa547686a4604d8f5fbabd3d89b59a801cc55b68aa653d813c66ca32a65`  
		Last Modified: Tue, 08 Apr 2025 17:26:18 GMT  
		Size: 6.0 MB (5991835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844018e59249593be5d829b3a4bba323e96c26297db204b3a8a8a52e847f8041`  
		Last Modified: Tue, 08 Apr 2025 21:25:07 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:1e53207f824b4b97a2158a01c60662ef62ff32a777e55e615077563d48bcc314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a229febf9f435367bc3df4661afe24971b0581fa0b4b375a92d4ac38c3ce791`

```dockerfile
```

-	Layers:
	-	`sha256:36f6e0df21021319068725c9d7c2325e4fad06927e5ff9fe7fe11ec830f17f1c`  
		Last Modified: Tue, 08 Apr 2025 21:25:06 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:9142b78e748793c9e3b2fda3ac3800e66e866bf0147d634a7aea592f973a023a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5776867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee76a21b5d66ec40c0c8c53a6af4ed91124f7a2820ab80bf20279efdc3e689c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6b90b986da10be1b936fe6989055b49edb315427df0ceb03d1dd2f9dd98fb88`  
		Last Modified: Tue, 08 Apr 2025 17:26:18 GMT  
		Size: 5.8 MB (5776357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5e46c8b1d8619650c3d1afbfcf70b02949ce40d6fd6eb7d769bdc98a1def25`  
		Last Modified: Wed, 09 Apr 2025 00:53:02 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:9f289daca75844d624973e2b4e4a78db9e2026bfd59d743648f68e3c13d32a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53971055b1ebeea168a941b88f41f089dd9886aa55cbebe6b4f12f98ddb49666`

```dockerfile
```

-	Layers:
	-	`sha256:a65f769c9cecfc76c232cf377b8548ffd7fc82eae67b781487e0924b3319a183`  
		Last Modified: Wed, 09 Apr 2025 00:53:02 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; ppc64le

```console
$ docker pull nats@sha256:8cbd8caa2bdb9c64319ae113af4cf4170b92f3795148cb20401f2f1f16aa1d11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5757631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ba2ae7e87afe027065399c01f1230c431bed76a811a5cc5c83e971b6e70a26`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2c03c8b47070105a3781cfd93e5a048f0fcf1895182b8500a1875b914beccc2b`  
		Last Modified: Tue, 08 Apr 2025 17:26:19 GMT  
		Size: 5.8 MB (5757122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425937f6cd03177f214b970352644a3316a1a6ac085099e96875d62e6eb6b95d`  
		Last Modified: Tue, 08 Apr 2025 22:18:51 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:5aa97ff134b80e48aaa63c71d9c8343062cb648de6445e6d078b62dab5b08a3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8af43893a1163e246e9f97ae6b6ca899d5147c74db410070388f3dc6b1bb9a`

```dockerfile
```

-	Layers:
	-	`sha256:b2dde84b1c72b35f921945f0d6bec4b01ff2c811e34deff66dc5a99577731ade`  
		Last Modified: Tue, 08 Apr 2025 22:18:51 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; s390x

```console
$ docker pull nats@sha256:24602554caa826a00e26b3dae9c589026eaab3e0ad8e59cb573cac3996e62f8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6122577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7976c47bfec0473931b30ef2753bdc1cefde06b7a03f869cabb36b78aee6fd30`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:096b0701966ee2a29da8fc2c3f8ad25d2a0bb1211425d296e92558196ebe09c9`  
		Last Modified: Tue, 08 Apr 2025 17:26:22 GMT  
		Size: 6.1 MB (6122069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50402e49c7c832b57fb874a3e012194a27d09597f2d39ddc97db3701ae5bfb7`  
		Last Modified: Tue, 08 Apr 2025 22:07:44 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:6f2d2b491eee799540891efc47f6f00293192e82097e7b80bb5fd571bbf312c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8736b1c1aaa3dce6b14a6b7b5cad1d5cc142fae7d7d9fd17b8a6d72e67a82268`

```dockerfile
```

-	Layers:
	-	`sha256:1ab1e3d26d57dec0dbbe6b34b8c0c23c6308ed6e3e58b9267695ff2247985c40`  
		Last Modified: Tue, 08 Apr 2025 22:07:44 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:nanoserver`

```console
$ docker pull nats@sha256:714b0b324ae5c514cc8066861c1ea58b8e852b21686bd57938b4cad501106b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `nats:nanoserver` - windows version 10.0.17763.7249; amd64

```console
$ docker pull nats@sha256:70dfa0a823409d278307a2f602a989bb5088fc2ed408add1628e7026065e4f7f
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.2 MB (115214035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c10544dab15e09a82ee58dfe65c5cebe6e37634a0fc0e40720019d69e49ec056`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Fri, 18 Apr 2025 04:11:39 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 18 Apr 2025 04:11:40 GMT
RUN cmd /S /C #(nop) COPY file:eee3870bfbcd9bfddd3622d20a6c2075b583b61ab0944602ceefed02dee11aa2 in C:\nats-server.exe 
# Fri, 18 Apr 2025 04:11:41 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Fri, 18 Apr 2025 04:11:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 18 Apr 2025 04:11:42 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 18 Apr 2025 04:11:42 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5dab9cfa2f7ef2b19e95e68d27e3d0b208d9016da1b04298c500e78281a15e7`  
		Last Modified: Fri, 18 Apr 2025 04:11:48 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d0b032347a8dcb65e359d04c00733934bf6cfe61db4b1142a1df5f3de23a9cc`  
		Last Modified: Fri, 18 Apr 2025 04:11:47 GMT  
		Size: 6.5 MB (6455931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497b3350d5c31834bcca73478d5fc7c0d3c546c1676c042e1e9d1ec9afc85bdd`  
		Last Modified: Fri, 18 Apr 2025 04:11:46 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658de08330e9b739dfbff680b38b2bb55dc4b4aec6d4064b19ecc24c7ba9a8aa`  
		Last Modified: Fri, 18 Apr 2025 04:11:46 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0312f657691b722f56e7ed6bc33b2119988f7f21d9853fe0a8dcc79a3b5aec`  
		Last Modified: Fri, 18 Apr 2025 04:11:46 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fc9ae19d64bc742bb97a1eec58e04de0d2eab1eb71186876fed513a4b21a3d`  
		Last Modified: Fri, 18 Apr 2025 04:11:46 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:714b0b324ae5c514cc8066861c1ea58b8e852b21686bd57938b4cad501106b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull nats@sha256:70dfa0a823409d278307a2f602a989bb5088fc2ed408add1628e7026065e4f7f
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.2 MB (115214035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c10544dab15e09a82ee58dfe65c5cebe6e37634a0fc0e40720019d69e49ec056`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Fri, 18 Apr 2025 04:11:39 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 18 Apr 2025 04:11:40 GMT
RUN cmd /S /C #(nop) COPY file:eee3870bfbcd9bfddd3622d20a6c2075b583b61ab0944602ceefed02dee11aa2 in C:\nats-server.exe 
# Fri, 18 Apr 2025 04:11:41 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Fri, 18 Apr 2025 04:11:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 18 Apr 2025 04:11:42 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 18 Apr 2025 04:11:42 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5dab9cfa2f7ef2b19e95e68d27e3d0b208d9016da1b04298c500e78281a15e7`  
		Last Modified: Fri, 18 Apr 2025 04:11:48 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d0b032347a8dcb65e359d04c00733934bf6cfe61db4b1142a1df5f3de23a9cc`  
		Last Modified: Fri, 18 Apr 2025 04:11:47 GMT  
		Size: 6.5 MB (6455931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497b3350d5c31834bcca73478d5fc7c0d3c546c1676c042e1e9d1ec9afc85bdd`  
		Last Modified: Fri, 18 Apr 2025 04:11:46 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658de08330e9b739dfbff680b38b2bb55dc4b4aec6d4064b19ecc24c7ba9a8aa`  
		Last Modified: Fri, 18 Apr 2025 04:11:46 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0312f657691b722f56e7ed6bc33b2119988f7f21d9853fe0a8dcc79a3b5aec`  
		Last Modified: Fri, 18 Apr 2025 04:11:46 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fc9ae19d64bc742bb97a1eec58e04de0d2eab1eb71186876fed513a4b21a3d`  
		Last Modified: Fri, 18 Apr 2025 04:11:46 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:4bb7463f82c83da51fd098d9ddbc0dccfdc7415e110b02de375f60066b392878
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
$ docker pull nats@sha256:41dddbc7a9265892086db802a374dbf910b5d0db786c8ba12e27a81f2ede8f05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6282680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ddda49ccc5be8fc53872fcb74f0f168368af1d3e5fc27fd096bb4ab9fac9e5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7a31ab99389a11bb36db183df5a6bc8d784c1e96fb10c1973e04b98e17e58f51`  
		Last Modified: Tue, 08 Apr 2025 17:26:21 GMT  
		Size: 6.3 MB (6282171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bcd18a1de501f0dcf00113b8c1effd2b7f198a1383c537490e8dce3a826adce`  
		Last Modified: Tue, 08 Apr 2025 21:07:44 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:16692b029d2fd73a6c9833d59190a10a052903fbc5b68228ca0ce31e25895ee4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a60659f991d784a3586e62308c55e27054bad66d740cbde49980328b682cb858`

```dockerfile
```

-	Layers:
	-	`sha256:d0fd9d7883ec1e99c1a17109b0a6fd39dec7b9ec8f40f0ace2f2c15f9d8846a3`  
		Last Modified: Tue, 08 Apr 2025 21:07:45 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:f53994879dbfd2fc8177b383905d33db1095d8b42bb4bec64088771cecdb2bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6002072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01de3b3fb48e4b75539a9af5640e6f77115cdbe9419f3da2891472ec6e806148`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bc9bfb085b797367e9407dbdf5a3928ee0d69859fb96188165856b5e8e1b6e88`  
		Last Modified: Tue, 08 Apr 2025 17:26:22 GMT  
		Size: 6.0 MB (6001563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef30b0264d904d40fbf4763922653522d80a800c24f6bcbb52a1a66fd1accaf8`  
		Last Modified: Tue, 08 Apr 2025 21:07:08 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:f9537be10194b98f78298fad26add4a04948857f650479e674587da738dcf69c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7014bcdaac4c9653a29f6fc739854477633a62a69bd0cba053bbeecbfc57e101`

```dockerfile
```

-	Layers:
	-	`sha256:e337d587115a4b810f5a9fa3deb1db109744f3828488f355e6bfa4c965ea5501`  
		Last Modified: Tue, 08 Apr 2025 21:07:08 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:859b07690a2059b52277aceb9feed7e81269aed09859f1c3b0f3162d751ddb29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5992346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e38aded7ecfd1e1b61cc0452d01e01718e0a4be4ee666ac1980ddacb6f7defbc`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8f114aa547686a4604d8f5fbabd3d89b59a801cc55b68aa653d813c66ca32a65`  
		Last Modified: Tue, 08 Apr 2025 17:26:18 GMT  
		Size: 6.0 MB (5991835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844018e59249593be5d829b3a4bba323e96c26297db204b3a8a8a52e847f8041`  
		Last Modified: Tue, 08 Apr 2025 21:25:07 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:1e53207f824b4b97a2158a01c60662ef62ff32a777e55e615077563d48bcc314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a229febf9f435367bc3df4661afe24971b0581fa0b4b375a92d4ac38c3ce791`

```dockerfile
```

-	Layers:
	-	`sha256:36f6e0df21021319068725c9d7c2325e4fad06927e5ff9fe7fe11ec830f17f1c`  
		Last Modified: Tue, 08 Apr 2025 21:25:06 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:9142b78e748793c9e3b2fda3ac3800e66e866bf0147d634a7aea592f973a023a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5776867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee76a21b5d66ec40c0c8c53a6af4ed91124f7a2820ab80bf20279efdc3e689c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6b90b986da10be1b936fe6989055b49edb315427df0ceb03d1dd2f9dd98fb88`  
		Last Modified: Tue, 08 Apr 2025 17:26:18 GMT  
		Size: 5.8 MB (5776357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5e46c8b1d8619650c3d1afbfcf70b02949ce40d6fd6eb7d769bdc98a1def25`  
		Last Modified: Wed, 09 Apr 2025 00:53:02 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:9f289daca75844d624973e2b4e4a78db9e2026bfd59d743648f68e3c13d32a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53971055b1ebeea168a941b88f41f089dd9886aa55cbebe6b4f12f98ddb49666`

```dockerfile
```

-	Layers:
	-	`sha256:a65f769c9cecfc76c232cf377b8548ffd7fc82eae67b781487e0924b3319a183`  
		Last Modified: Wed, 09 Apr 2025 00:53:02 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:8cbd8caa2bdb9c64319ae113af4cf4170b92f3795148cb20401f2f1f16aa1d11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5757631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ba2ae7e87afe027065399c01f1230c431bed76a811a5cc5c83e971b6e70a26`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2c03c8b47070105a3781cfd93e5a048f0fcf1895182b8500a1875b914beccc2b`  
		Last Modified: Tue, 08 Apr 2025 17:26:19 GMT  
		Size: 5.8 MB (5757122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425937f6cd03177f214b970352644a3316a1a6ac085099e96875d62e6eb6b95d`  
		Last Modified: Tue, 08 Apr 2025 22:18:51 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:5aa97ff134b80e48aaa63c71d9c8343062cb648de6445e6d078b62dab5b08a3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8af43893a1163e246e9f97ae6b6ca899d5147c74db410070388f3dc6b1bb9a`

```dockerfile
```

-	Layers:
	-	`sha256:b2dde84b1c72b35f921945f0d6bec4b01ff2c811e34deff66dc5a99577731ade`  
		Last Modified: Tue, 08 Apr 2025 22:18:51 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; s390x

```console
$ docker pull nats@sha256:24602554caa826a00e26b3dae9c589026eaab3e0ad8e59cb573cac3996e62f8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6122577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7976c47bfec0473931b30ef2753bdc1cefde06b7a03f869cabb36b78aee6fd30`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 08 Apr 2025 17:23:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 08 Apr 2025 17:23:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 08 Apr 2025 17:23:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 08 Apr 2025 17:23:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 08 Apr 2025 17:23:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:096b0701966ee2a29da8fc2c3f8ad25d2a0bb1211425d296e92558196ebe09c9`  
		Last Modified: Tue, 08 Apr 2025 17:26:22 GMT  
		Size: 6.1 MB (6122069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50402e49c7c832b57fb874a3e012194a27d09597f2d39ddc97db3701ae5bfb7`  
		Last Modified: Tue, 08 Apr 2025 22:07:44 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:6f2d2b491eee799540891efc47f6f00293192e82097e7b80bb5fd571bbf312c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8736b1c1aaa3dce6b14a6b7b5cad1d5cc142fae7d7d9fd17b8a6d72e67a82268`

```dockerfile
```

-	Layers:
	-	`sha256:1ab1e3d26d57dec0dbbe6b34b8c0c23c6308ed6e3e58b9267695ff2247985c40`  
		Last Modified: Tue, 08 Apr 2025 22:07:44 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:d50be1cda62b37ce5581671dafc900fc728a2c95a2497d7a1a3f76578329fa81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `nats:windowsservercore` - windows version 10.0.17763.7249; amd64

```console
$ docker pull nats@sha256:de12da09e1602e2f93ed8b9b9897000258cf9608c390bc2620472c61a146810b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2172650201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f8e26de837c3eb00f55fdb3ea32e3a8eca48f3f6f7163fe633b78ed5241d985`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Fri, 18 Apr 2025 03:15:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 18 Apr 2025 03:15:31 GMT
ENV NATS_DOCKERIZED=1
# Fri, 18 Apr 2025 03:15:32 GMT
ENV NATS_SERVER=2.11.1
# Fri, 18 Apr 2025 03:15:33 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.1/nats-server-v2.11.1-windows-amd64.zip
# Fri, 18 Apr 2025 03:15:34 GMT
ENV NATS_SERVER_SHASUM=f5594798e1b77013b674c0049070d2502c20ee6f03a04d854cac333e2a21ca20
# Fri, 18 Apr 2025 03:16:07 GMT
RUN Set-PSDebug -Trace 2
# Fri, 18 Apr 2025 03:16:25 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 18 Apr 2025 03:16:26 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Fri, 18 Apr 2025 03:16:27 GMT
EXPOSE 4222 6222 8222
# Fri, 18 Apr 2025 03:16:27 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 18 Apr 2025 03:16:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Fri, 18 Apr 2025 03:13:03 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7822538d66aa517be43d1d696a9cc338fba7d6950e51918ac111ff32439b76d`  
		Last Modified: Fri, 18 Apr 2025 03:16:32 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:352f9e3e8b1aeaa1335f9d9417867a41164c3927fc6b5260d2f8c727d7ce3537`  
		Last Modified: Fri, 18 Apr 2025 03:16:32 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1f23260e2b6c00f1d9e28c5e37d7bdd45320561ed314845ff8d9ad8815ba79`  
		Last Modified: Fri, 18 Apr 2025 03:16:32 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66dc359cc850871940050c1e2fa57ba9ee16d9b033fba1532255cc0ea7a487da`  
		Last Modified: Fri, 18 Apr 2025 03:16:31 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd3feaf085072d792e35ade328ab0c2c1ecf53fd61f3c21f296549840710430`  
		Last Modified: Fri, 18 Apr 2025 03:16:31 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dae23d135bd9c3a0f11a7fb76e406cf4f5492a7988bdc3d9611f746ebb6945c`  
		Last Modified: Fri, 18 Apr 2025 03:16:31 GMT  
		Size: 322.6 KB (322628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bcdffa91604493a08769e767b51db8f8bc176116e8019a081a432923b5cb8d2`  
		Last Modified: Fri, 18 Apr 2025 03:16:31 GMT  
		Size: 6.8 MB (6789581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270410cf637c0ea7c99ed52451d17b6129481750e0caf3e12ad1cab37a0cb3ce`  
		Last Modified: Fri, 18 Apr 2025 03:16:30 GMT  
		Size: 1.8 KB (1849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2ad53fbd757d0e60898d5ee40e6355c43e9a4862e5b82429752248dbd9a85b6`  
		Last Modified: Fri, 18 Apr 2025 03:16:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c32fbcc93f5bdc7d627e5633180fff8d0b1759564412e5571800b97b912e371e`  
		Last Modified: Fri, 18 Apr 2025 03:16:30 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7c6da8a76e3b31cfa4ea2184896009c2dc8b62dd7f14fb45739484b9d6189f9`  
		Last Modified: Fri, 18 Apr 2025 03:16:31 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:d50be1cda62b37ce5581671dafc900fc728a2c95a2497d7a1a3f76578329fa81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull nats@sha256:de12da09e1602e2f93ed8b9b9897000258cf9608c390bc2620472c61a146810b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2172650201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f8e26de837c3eb00f55fdb3ea32e3a8eca48f3f6f7163fe633b78ed5241d985`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Fri, 18 Apr 2025 03:15:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 18 Apr 2025 03:15:31 GMT
ENV NATS_DOCKERIZED=1
# Fri, 18 Apr 2025 03:15:32 GMT
ENV NATS_SERVER=2.11.1
# Fri, 18 Apr 2025 03:15:33 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.1/nats-server-v2.11.1-windows-amd64.zip
# Fri, 18 Apr 2025 03:15:34 GMT
ENV NATS_SERVER_SHASUM=f5594798e1b77013b674c0049070d2502c20ee6f03a04d854cac333e2a21ca20
# Fri, 18 Apr 2025 03:16:07 GMT
RUN Set-PSDebug -Trace 2
# Fri, 18 Apr 2025 03:16:25 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 18 Apr 2025 03:16:26 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Fri, 18 Apr 2025 03:16:27 GMT
EXPOSE 4222 6222 8222
# Fri, 18 Apr 2025 03:16:27 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 18 Apr 2025 03:16:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Fri, 18 Apr 2025 03:13:03 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7822538d66aa517be43d1d696a9cc338fba7d6950e51918ac111ff32439b76d`  
		Last Modified: Fri, 18 Apr 2025 03:16:32 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:352f9e3e8b1aeaa1335f9d9417867a41164c3927fc6b5260d2f8c727d7ce3537`  
		Last Modified: Fri, 18 Apr 2025 03:16:32 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1f23260e2b6c00f1d9e28c5e37d7bdd45320561ed314845ff8d9ad8815ba79`  
		Last Modified: Fri, 18 Apr 2025 03:16:32 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66dc359cc850871940050c1e2fa57ba9ee16d9b033fba1532255cc0ea7a487da`  
		Last Modified: Fri, 18 Apr 2025 03:16:31 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd3feaf085072d792e35ade328ab0c2c1ecf53fd61f3c21f296549840710430`  
		Last Modified: Fri, 18 Apr 2025 03:16:31 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dae23d135bd9c3a0f11a7fb76e406cf4f5492a7988bdc3d9611f746ebb6945c`  
		Last Modified: Fri, 18 Apr 2025 03:16:31 GMT  
		Size: 322.6 KB (322628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bcdffa91604493a08769e767b51db8f8bc176116e8019a081a432923b5cb8d2`  
		Last Modified: Fri, 18 Apr 2025 03:16:31 GMT  
		Size: 6.8 MB (6789581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270410cf637c0ea7c99ed52451d17b6129481750e0caf3e12ad1cab37a0cb3ce`  
		Last Modified: Fri, 18 Apr 2025 03:16:30 GMT  
		Size: 1.8 KB (1849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2ad53fbd757d0e60898d5ee40e6355c43e9a4862e5b82429752248dbd9a85b6`  
		Last Modified: Fri, 18 Apr 2025 03:16:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c32fbcc93f5bdc7d627e5633180fff8d0b1759564412e5571800b97b912e371e`  
		Last Modified: Fri, 18 Apr 2025 03:16:30 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7c6da8a76e3b31cfa4ea2184896009c2dc8b62dd7f14fb45739484b9d6189f9`  
		Last Modified: Fri, 18 Apr 2025 03:16:31 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
