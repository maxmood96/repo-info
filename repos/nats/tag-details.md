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
-	[`nats:2.10.27`](#nats21027)
-	[`nats:2.10.27-alpine`](#nats21027-alpine)
-	[`nats:2.10.27-alpine3.21`](#nats21027-alpine321)
-	[`nats:2.10.27-linux`](#nats21027-linux)
-	[`nats:2.10.27-nanoserver`](#nats21027-nanoserver)
-	[`nats:2.10.27-nanoserver-1809`](#nats21027-nanoserver-1809)
-	[`nats:2.10.27-scratch`](#nats21027-scratch)
-	[`nats:2.10.27-windowsservercore`](#nats21027-windowsservercore)
-	[`nats:2.10.27-windowsservercore-1809`](#nats21027-windowsservercore-1809)
-	[`nats:2.11`](#nats211)
-	[`nats:2.11-alpine`](#nats211-alpine)
-	[`nats:2.11-alpine3.21`](#nats211-alpine321)
-	[`nats:2.11-linux`](#nats211-linux)
-	[`nats:2.11-nanoserver`](#nats211-nanoserver)
-	[`nats:2.11-nanoserver-1809`](#nats211-nanoserver-1809)
-	[`nats:2.11-scratch`](#nats211-scratch)
-	[`nats:2.11-windowsservercore`](#nats211-windowsservercore)
-	[`nats:2.11-windowsservercore-1809`](#nats211-windowsservercore-1809)
-	[`nats:2.11.1`](#nats2111)
-	[`nats:2.11.1-alpine`](#nats2111-alpine)
-	[`nats:2.11.1-alpine3.21`](#nats2111-alpine321)
-	[`nats:2.11.1-linux`](#nats2111-linux)
-	[`nats:2.11.1-nanoserver`](#nats2111-nanoserver)
-	[`nats:2.11.1-nanoserver-1809`](#nats2111-nanoserver-1809)
-	[`nats:2.11.1-scratch`](#nats2111-scratch)
-	[`nats:2.11.1-windowsservercore`](#nats2111-windowsservercore)
-	[`nats:2.11.1-windowsservercore-1809`](#nats2111-windowsservercore-1809)
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
$ docker pull nats@sha256:d80d5773c4e558914e79e2886f54a64963d1f07d8638b0c49217cf6fb8e95049
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
	-	windows version 10.0.17763.7009; amd64

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

### `nats:2` - windows version 10.0.17763.7009; amd64

```console
$ docker pull nats@sha256:715ccd4de0bcee69815ad68778b62f6b9373b757afb53337ede87f360c5a010e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113369449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3d563f68baff6d95b9b2b72e3ae34a23681a1a3f2185a8990940cd3a979268a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Tue, 08 Apr 2025 22:13:52 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 08 Apr 2025 22:13:55 GMT
RUN cmd /S /C #(nop) COPY file:eee3870bfbcd9bfddd3622d20a6c2075b583b61ab0944602ceefed02dee11aa2 in C:\nats-server.exe 
# Tue, 08 Apr 2025 22:13:56 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 08 Apr 2025 22:13:57 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 08 Apr 2025 22:13:57 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 08 Apr 2025 22:13:58 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cfa145690c6aebcb679b25530d2fe0c89c7895d522bc2a51865f9318b005b5f`  
		Last Modified: Tue, 08 Apr 2025 22:14:02 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935788f0279b4a2c1b70d0513fd91be7c0c51126d6ea20137c285b06b5bb1f72`  
		Last Modified: Tue, 08 Apr 2025 22:14:02 GMT  
		Size: 6.5 MB (6455907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f144255a54963a1049be6601f86720694f66bb79a738c6f8bd9f1e50cf078872`  
		Last Modified: Tue, 08 Apr 2025 22:14:01 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55833ccd9e0a66322e50524b64d784272932816426d2b868274b94d5eda2b9cb`  
		Last Modified: Tue, 08 Apr 2025 22:14:01 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba94d6c3b308280e6cb389c9f65d5fca970fe7338eb34c025df4d83870244a4`  
		Last Modified: Tue, 08 Apr 2025 22:14:01 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07636e21dc67f902c5b4325c6a45d77f4c0717a519e17f32f1079e8988eb7bbb`  
		Last Modified: Tue, 08 Apr 2025 22:14:01 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:f3d9be9e3809381297c6fc2e1d071bbab2ff25df5fa89e89edbd00fce34f1ca0
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
$ docker pull nats@sha256:33bedd609f7f7f31c7a609239dff642b098d339b2ae5c72f358aca3b0bdfcd99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9830618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f144ccbbca357bd10e864ad6a9469caf63d49af1182de50d7da5e3d4641bcf0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
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
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9048a08e892a91b40d37a992fb9228a855e04b86a0193658785404d407502c36`  
		Last Modified: Tue, 08 Apr 2025 20:28:28 GMT  
		Size: 6.5 MB (6464916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b28e407313ff54262ed40c18741ab1d8d650c46875eb53e1f4dae7a19d64f0`  
		Last Modified: Tue, 08 Apr 2025 20:28:28 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1037b517e6fb05b376c0f845c2de48f91d85acef85548878752fff9e0e5fcb4e`  
		Last Modified: Tue, 08 Apr 2025 20:28:28 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:f99dfd48fc9fbd2ad2bda5e2128399c2608b793c2df1677489b75ed55c958c80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76d73ac2a38ee74207ea6780edbe4013fa25eafa0ecf5318e88d09592d7da396`

```dockerfile
```

-	Layers:
	-	`sha256:a5c19b7d31f9642dc7ccbb0d73e2008fec7c606c270d5f41a4a1d534c57eb386`  
		Last Modified: Tue, 08 Apr 2025 20:28:27 GMT  
		Size: 14.4 KB (14425 bytes)  
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
$ docker pull nats@sha256:bc972962a3f6fd357ba4b57dcf878b3c6958fa2fbf75b65bf909c33b47f740e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10234750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:413538651b4a89933595bd87d769140c04c8eae8fac10ef3ff3a2d91bc53712f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
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
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b621e6959e97eb3ca377c901a7c1245231edc4c09198cb628915b5d3e10736c`  
		Last Modified: Tue, 08 Apr 2025 21:41:26 GMT  
		Size: 6.2 MB (6240748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1118a4f264db0d527eda19b814faffbbb61a8097f95ef2157fab3c21c0da752e`  
		Last Modified: Tue, 08 Apr 2025 21:41:25 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd107cb6fb6fc67b6484a7213268c505f995d9ec489e02602183d895d2cf6142`  
		Last Modified: Tue, 08 Apr 2025 21:41:25 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:dbcfea7b097433117d3ae7e09f5c5824d45dd3d22107d68ef1a2d3080a3742ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43ca0929e9d902e26a1809f5bc3001f3f41b0dc140fd461409cd02b47a6b7219`

```dockerfile
```

-	Layers:
	-	`sha256:6477b5d99ee19ec70115adc1465de3de4a5c61690c1f3f6c597057a749b64c3a`  
		Last Modified: Tue, 08 Apr 2025 21:41:25 GMT  
		Size: 14.5 KB (14468 bytes)  
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
$ docker pull nats@sha256:f3d9be9e3809381297c6fc2e1d071bbab2ff25df5fa89e89edbd00fce34f1ca0
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
$ docker pull nats@sha256:33bedd609f7f7f31c7a609239dff642b098d339b2ae5c72f358aca3b0bdfcd99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9830618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f144ccbbca357bd10e864ad6a9469caf63d49af1182de50d7da5e3d4641bcf0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
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
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9048a08e892a91b40d37a992fb9228a855e04b86a0193658785404d407502c36`  
		Last Modified: Tue, 08 Apr 2025 20:28:28 GMT  
		Size: 6.5 MB (6464916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b28e407313ff54262ed40c18741ab1d8d650c46875eb53e1f4dae7a19d64f0`  
		Last Modified: Tue, 08 Apr 2025 20:28:28 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1037b517e6fb05b376c0f845c2de48f91d85acef85548878752fff9e0e5fcb4e`  
		Last Modified: Tue, 08 Apr 2025 20:28:28 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:f99dfd48fc9fbd2ad2bda5e2128399c2608b793c2df1677489b75ed55c958c80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76d73ac2a38ee74207ea6780edbe4013fa25eafa0ecf5318e88d09592d7da396`

```dockerfile
```

-	Layers:
	-	`sha256:a5c19b7d31f9642dc7ccbb0d73e2008fec7c606c270d5f41a4a1d534c57eb386`  
		Last Modified: Tue, 08 Apr 2025 20:28:27 GMT  
		Size: 14.4 KB (14425 bytes)  
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
$ docker pull nats@sha256:bc972962a3f6fd357ba4b57dcf878b3c6958fa2fbf75b65bf909c33b47f740e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10234750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:413538651b4a89933595bd87d769140c04c8eae8fac10ef3ff3a2d91bc53712f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
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
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b621e6959e97eb3ca377c901a7c1245231edc4c09198cb628915b5d3e10736c`  
		Last Modified: Tue, 08 Apr 2025 21:41:26 GMT  
		Size: 6.2 MB (6240748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1118a4f264db0d527eda19b814faffbbb61a8097f95ef2157fab3c21c0da752e`  
		Last Modified: Tue, 08 Apr 2025 21:41:25 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd107cb6fb6fc67b6484a7213268c505f995d9ec489e02602183d895d2cf6142`  
		Last Modified: Tue, 08 Apr 2025 21:41:25 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:dbcfea7b097433117d3ae7e09f5c5824d45dd3d22107d68ef1a2d3080a3742ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43ca0929e9d902e26a1809f5bc3001f3f41b0dc140fd461409cd02b47a6b7219`

```dockerfile
```

-	Layers:
	-	`sha256:6477b5d99ee19ec70115adc1465de3de4a5c61690c1f3f6c597057a749b64c3a`  
		Last Modified: Tue, 08 Apr 2025 21:41:25 GMT  
		Size: 14.5 KB (14468 bytes)  
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
$ docker pull nats@sha256:abf7e27366b68d9cd2043a5da962739151157116459ae937f689ebaaff08b11a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.7009; amd64

```console
$ docker pull nats@sha256:715ccd4de0bcee69815ad68778b62f6b9373b757afb53337ede87f360c5a010e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113369449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3d563f68baff6d95b9b2b72e3ae34a23681a1a3f2185a8990940cd3a979268a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Tue, 08 Apr 2025 22:13:52 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 08 Apr 2025 22:13:55 GMT
RUN cmd /S /C #(nop) COPY file:eee3870bfbcd9bfddd3622d20a6c2075b583b61ab0944602ceefed02dee11aa2 in C:\nats-server.exe 
# Tue, 08 Apr 2025 22:13:56 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 08 Apr 2025 22:13:57 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 08 Apr 2025 22:13:57 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 08 Apr 2025 22:13:58 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cfa145690c6aebcb679b25530d2fe0c89c7895d522bc2a51865f9318b005b5f`  
		Last Modified: Tue, 08 Apr 2025 22:14:02 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935788f0279b4a2c1b70d0513fd91be7c0c51126d6ea20137c285b06b5bb1f72`  
		Last Modified: Tue, 08 Apr 2025 22:14:02 GMT  
		Size: 6.5 MB (6455907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f144255a54963a1049be6601f86720694f66bb79a738c6f8bd9f1e50cf078872`  
		Last Modified: Tue, 08 Apr 2025 22:14:01 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55833ccd9e0a66322e50524b64d784272932816426d2b868274b94d5eda2b9cb`  
		Last Modified: Tue, 08 Apr 2025 22:14:01 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba94d6c3b308280e6cb389c9f65d5fca970fe7338eb34c025df4d83870244a4`  
		Last Modified: Tue, 08 Apr 2025 22:14:01 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07636e21dc67f902c5b4325c6a45d77f4c0717a519e17f32f1079e8988eb7bbb`  
		Last Modified: Tue, 08 Apr 2025 22:14:01 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:abf7e27366b68d9cd2043a5da962739151157116459ae937f689ebaaff08b11a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull nats@sha256:715ccd4de0bcee69815ad68778b62f6b9373b757afb53337ede87f360c5a010e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113369449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3d563f68baff6d95b9b2b72e3ae34a23681a1a3f2185a8990940cd3a979268a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Tue, 08 Apr 2025 22:13:52 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 08 Apr 2025 22:13:55 GMT
RUN cmd /S /C #(nop) COPY file:eee3870bfbcd9bfddd3622d20a6c2075b583b61ab0944602ceefed02dee11aa2 in C:\nats-server.exe 
# Tue, 08 Apr 2025 22:13:56 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 08 Apr 2025 22:13:57 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 08 Apr 2025 22:13:57 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 08 Apr 2025 22:13:58 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cfa145690c6aebcb679b25530d2fe0c89c7895d522bc2a51865f9318b005b5f`  
		Last Modified: Tue, 08 Apr 2025 22:14:02 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935788f0279b4a2c1b70d0513fd91be7c0c51126d6ea20137c285b06b5bb1f72`  
		Last Modified: Tue, 08 Apr 2025 22:14:02 GMT  
		Size: 6.5 MB (6455907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f144255a54963a1049be6601f86720694f66bb79a738c6f8bd9f1e50cf078872`  
		Last Modified: Tue, 08 Apr 2025 22:14:01 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55833ccd9e0a66322e50524b64d784272932816426d2b868274b94d5eda2b9cb`  
		Last Modified: Tue, 08 Apr 2025 22:14:01 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba94d6c3b308280e6cb389c9f65d5fca970fe7338eb34c025df4d83870244a4`  
		Last Modified: Tue, 08 Apr 2025 22:14:01 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07636e21dc67f902c5b4325c6a45d77f4c0717a519e17f32f1079e8988eb7bbb`  
		Last Modified: Tue, 08 Apr 2025 22:14:01 GMT  
		Size: 1.0 KB (1044 bytes)  
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
$ docker pull nats@sha256:d5a5a3214c03e4383b75d3a553d43f1e6966f5e1e2f2fb1f81587381822f7b76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7136; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.7136; amd64

```console
$ docker pull nats@sha256:607f6e73ed9007241ff50a84dba439ab79d98a3f3fb47ea3a930f688f67f3088
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2169857611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:597119b40ab372d074effb9f06eec9a9d1a3e9637ac4696ce5f338e8ff4106b3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Sat, 05 Apr 2025 01:48:05 GMT
RUN Install update 10.0.17763.7136
# Wed, 09 Apr 2025 00:59:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Apr 2025 00:59:01 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Apr 2025 00:59:02 GMT
ENV NATS_SERVER=2.11.1
# Wed, 09 Apr 2025 00:59:03 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.1/nats-server-v2.11.1-windows-amd64.zip
# Wed, 09 Apr 2025 00:59:03 GMT
ENV NATS_SERVER_SHASUM=f5594798e1b77013b674c0049070d2502c20ee6f03a04d854cac333e2a21ca20
# Wed, 09 Apr 2025 00:59:40 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Apr 2025 00:59:59 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Apr 2025 00:59:59 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 09 Apr 2025 01:00:00 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Apr 2025 01:00:00 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Apr 2025 01:00:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d949f82a48e7c53af792160596b10005419fbc7ecfed6bc45bbeee3a5a2f07`  
		Last Modified: Tue, 08 Apr 2025 19:58:26 GMT  
		Size: 442.5 MB (442457492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a09300fffebaa4864cab22c763b15a10f2bbf057547b6ff255863442e152d0`  
		Last Modified: Wed, 09 Apr 2025 01:00:09 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21038a6eaee5de691c53f4cf4d271a784a445d934945099069a55d2b2b1a69e9`  
		Last Modified: Wed, 09 Apr 2025 01:00:09 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24942860fb41d5b161011df2cd69c16f7d6847ed7b6db02a33bb64054a72788`  
		Last Modified: Wed, 09 Apr 2025 01:00:07 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e46de18cf6f2c6f8ab7a838c3809a4539af5c48187286fa9e2bba100aed7f0de`  
		Last Modified: Wed, 09 Apr 2025 01:00:07 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d3f59562780344fd3c1ba4f023d776c21499331a904bfcbd4368f20d9da6dab`  
		Last Modified: Wed, 09 Apr 2025 01:00:07 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:795d0c7a551fbfc87a25f38f1a5fa59e2655ca81e62da54e276767f53017edd0`  
		Last Modified: Wed, 09 Apr 2025 01:00:07 GMT  
		Size: 327.2 KB (327167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6cb9f352ed0567a90df0ec2d622906e5d9afe98f400ca192be89a3e899f7d9`  
		Last Modified: Wed, 09 Apr 2025 01:00:07 GMT  
		Size: 6.8 MB (6791732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0f251d7ebfa8a3ecc74f04cf48dbdfb0bbdff942b30e6e4f0d0cbf0f620229`  
		Last Modified: Wed, 09 Apr 2025 01:00:05 GMT  
		Size: 1.9 KB (1934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1994ceebe61f490ae0929761fd777cec24a750b119093e271c15448e6069772e`  
		Last Modified: Wed, 09 Apr 2025 01:00:05 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe64f8769bc81f46b33af77ab80603037a4c694a21ef49ed7c458b22bb1b3e6`  
		Last Modified: Wed, 09 Apr 2025 01:00:05 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca16d5f700915418444888d8391f2ddbdc7a15396a440fbbef200bb6a460b19a`  
		Last Modified: Wed, 09 Apr 2025 01:00:06 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:d5a5a3214c03e4383b75d3a553d43f1e6966f5e1e2f2fb1f81587381822f7b76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7136; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.7136; amd64

```console
$ docker pull nats@sha256:607f6e73ed9007241ff50a84dba439ab79d98a3f3fb47ea3a930f688f67f3088
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2169857611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:597119b40ab372d074effb9f06eec9a9d1a3e9637ac4696ce5f338e8ff4106b3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Sat, 05 Apr 2025 01:48:05 GMT
RUN Install update 10.0.17763.7136
# Wed, 09 Apr 2025 00:59:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Apr 2025 00:59:01 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Apr 2025 00:59:02 GMT
ENV NATS_SERVER=2.11.1
# Wed, 09 Apr 2025 00:59:03 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.1/nats-server-v2.11.1-windows-amd64.zip
# Wed, 09 Apr 2025 00:59:03 GMT
ENV NATS_SERVER_SHASUM=f5594798e1b77013b674c0049070d2502c20ee6f03a04d854cac333e2a21ca20
# Wed, 09 Apr 2025 00:59:40 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Apr 2025 00:59:59 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Apr 2025 00:59:59 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 09 Apr 2025 01:00:00 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Apr 2025 01:00:00 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Apr 2025 01:00:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d949f82a48e7c53af792160596b10005419fbc7ecfed6bc45bbeee3a5a2f07`  
		Last Modified: Tue, 08 Apr 2025 19:58:26 GMT  
		Size: 442.5 MB (442457492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a09300fffebaa4864cab22c763b15a10f2bbf057547b6ff255863442e152d0`  
		Last Modified: Wed, 09 Apr 2025 01:00:09 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21038a6eaee5de691c53f4cf4d271a784a445d934945099069a55d2b2b1a69e9`  
		Last Modified: Wed, 09 Apr 2025 01:00:09 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24942860fb41d5b161011df2cd69c16f7d6847ed7b6db02a33bb64054a72788`  
		Last Modified: Wed, 09 Apr 2025 01:00:07 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e46de18cf6f2c6f8ab7a838c3809a4539af5c48187286fa9e2bba100aed7f0de`  
		Last Modified: Wed, 09 Apr 2025 01:00:07 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d3f59562780344fd3c1ba4f023d776c21499331a904bfcbd4368f20d9da6dab`  
		Last Modified: Wed, 09 Apr 2025 01:00:07 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:795d0c7a551fbfc87a25f38f1a5fa59e2655ca81e62da54e276767f53017edd0`  
		Last Modified: Wed, 09 Apr 2025 01:00:07 GMT  
		Size: 327.2 KB (327167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6cb9f352ed0567a90df0ec2d622906e5d9afe98f400ca192be89a3e899f7d9`  
		Last Modified: Wed, 09 Apr 2025 01:00:07 GMT  
		Size: 6.8 MB (6791732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0f251d7ebfa8a3ecc74f04cf48dbdfb0bbdff942b30e6e4f0d0cbf0f620229`  
		Last Modified: Wed, 09 Apr 2025 01:00:05 GMT  
		Size: 1.9 KB (1934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1994ceebe61f490ae0929761fd777cec24a750b119093e271c15448e6069772e`  
		Last Modified: Wed, 09 Apr 2025 01:00:05 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe64f8769bc81f46b33af77ab80603037a4c694a21ef49ed7c458b22bb1b3e6`  
		Last Modified: Wed, 09 Apr 2025 01:00:05 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca16d5f700915418444888d8391f2ddbdc7a15396a440fbbef200bb6a460b19a`  
		Last Modified: Wed, 09 Apr 2025 01:00:06 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10`

```console
$ docker pull nats@sha256:8a808485b1a116d6908fa81e328be83b01bf0da6cf8bb95f34681dedf3d8d84c
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
	-	windows version 10.0.17763.7009; amd64

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

### `nats:2.10` - windows version 10.0.17763.7009; amd64

```console
$ docker pull nats@sha256:3d7e34f37e5d3a52d700c1e79f59f13da605f176056911c06c6018aff824a881
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 MB (113200253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c130a8066e6988bb80322a1463575126ad49dcc4eac9bde949d5f8f8700245d2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Tue, 08 Apr 2025 22:14:05 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 08 Apr 2025 22:14:07 GMT
RUN cmd /S /C #(nop) COPY file:911e7fad0174090a7de06fb3b7fca63c95843409a6ad46e295d2fe4da8d99d2a in C:\nats-server.exe 
# Tue, 08 Apr 2025 22:14:08 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 08 Apr 2025 22:14:08 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 08 Apr 2025 22:14:09 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 08 Apr 2025 22:14:10 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f6acdbafb61d829b0f8ca95b32b0ccf5c447f898e355108570cd0259ebc5a57`  
		Last Modified: Tue, 08 Apr 2025 22:14:13 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1676b0df597845c0dedf663901c220c1f121d58fdb561a439eab94cc89768819`  
		Last Modified: Tue, 08 Apr 2025 22:14:13 GMT  
		Size: 6.3 MB (6286693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0255179dc6894853ae0159b887a38b465dc585c5e4bd328251f9ae51f8cdcb`  
		Last Modified: Tue, 08 Apr 2025 22:14:12 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200a3150dce3b9d8ce51c430fd9c9e14d344ef75ba9e466d85bfb7b3f7a91f45`  
		Last Modified: Tue, 08 Apr 2025 22:14:12 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b404aa582bdecfbf7bdbc91ee90de91d6d15d6d6202b2d6727682002378e67`  
		Last Modified: Tue, 08 Apr 2025 22:14:12 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e127e6a4caa3eab8729eae82aa5d747dc650fe981906ec050f43cdeb2c89e337`  
		Last Modified: Tue, 08 Apr 2025 22:14:12 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine`

```console
$ docker pull nats@sha256:e243c53e5b2ebf24f5d8f05d7555462003c050a51ee0a2643d2dc89aea6d06a5
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
$ docker pull nats@sha256:4632ca3d999fe68493ea2ed5d84dd51b01007f17a9541cb4e1699f69b14e567d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9721153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f606fc733c44eafa7b41bec8d259da9c5fd26276df8894ccf42d3f6373e7e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
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
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c4d4ac036d3e9ea1b0876b5fb0a2495ed304d6b156011acfe4edd6015f06bf`  
		Last Modified: Tue, 08 Apr 2025 20:28:41 GMT  
		Size: 6.4 MB (6355452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33387efebc89387e808c896b85201ab384cad0eb689aeb33150ee974d9bc86c6`  
		Last Modified: Tue, 08 Apr 2025 20:28:40 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a506ef078ce7ef90659eb2c5c6cdd9e168db5c649df636b995d7850d6ba123`  
		Last Modified: Tue, 08 Apr 2025 20:28:40 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:853dad0f33fa0d69187c3cb1a45872db5706b82f34ef463c8600574cc8665d5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eead0a360dfced7c60114991f1f7efc861cab15f454c29ca5dea2c21a9b2270`

```dockerfile
```

-	Layers:
	-	`sha256:beb17eeae7561e658284ca176f32ee1ff0b554e3baf90d450e8b7a768121a83e`  
		Last Modified: Tue, 08 Apr 2025 20:28:40 GMT  
		Size: 13.2 KB (13197 bytes)  
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
$ docker pull nats@sha256:799daf4b6cf85a36125e0d6bec2533a0c8b5ec84e59b841506a6809cb9a7d3e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10129977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5493be1b5d060e3664e0ed0105b9a117646a6c5431bf40575ce8067dfb6e624f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
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
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2242ea11d02d4b76585c5bd3c1a8d48abc89637565f98c10bc95093e2ac85fd9`  
		Last Modified: Tue, 08 Apr 2025 21:41:38 GMT  
		Size: 6.1 MB (6135979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71dc7021098449aef008fd78a2bf07e2c2cf8c6a9983fbd93e3a7d8fb02b4b44`  
		Last Modified: Tue, 08 Apr 2025 21:41:37 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ffaf0a4fe2676b683b4266bfa9f63838485fd955714979fe322e23a8ad52f6`  
		Last Modified: Tue, 08 Apr 2025 21:41:37 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:a2c32b998e310db81899db4a7ea0bf211f8177355e498a163b5ee12dce6fb8c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa451c798f073309ad1606f97a9e84b9789dc257fd3aca978f4dc90b95cd3d54`

```dockerfile
```

-	Layers:
	-	`sha256:e4657c77e9aadc2989733b284b18c737a42c14d4619111b6ee1b55d1cf4af7bc`  
		Last Modified: Tue, 08 Apr 2025 21:41:37 GMT  
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
$ docker pull nats@sha256:e243c53e5b2ebf24f5d8f05d7555462003c050a51ee0a2643d2dc89aea6d06a5
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
$ docker pull nats@sha256:4632ca3d999fe68493ea2ed5d84dd51b01007f17a9541cb4e1699f69b14e567d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9721153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f606fc733c44eafa7b41bec8d259da9c5fd26276df8894ccf42d3f6373e7e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
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
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c4d4ac036d3e9ea1b0876b5fb0a2495ed304d6b156011acfe4edd6015f06bf`  
		Last Modified: Tue, 08 Apr 2025 20:28:41 GMT  
		Size: 6.4 MB (6355452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33387efebc89387e808c896b85201ab384cad0eb689aeb33150ee974d9bc86c6`  
		Last Modified: Tue, 08 Apr 2025 20:28:40 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a506ef078ce7ef90659eb2c5c6cdd9e168db5c649df636b995d7850d6ba123`  
		Last Modified: Tue, 08 Apr 2025 20:28:40 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:853dad0f33fa0d69187c3cb1a45872db5706b82f34ef463c8600574cc8665d5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eead0a360dfced7c60114991f1f7efc861cab15f454c29ca5dea2c21a9b2270`

```dockerfile
```

-	Layers:
	-	`sha256:beb17eeae7561e658284ca176f32ee1ff0b554e3baf90d450e8b7a768121a83e`  
		Last Modified: Tue, 08 Apr 2025 20:28:40 GMT  
		Size: 13.2 KB (13197 bytes)  
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
$ docker pull nats@sha256:799daf4b6cf85a36125e0d6bec2533a0c8b5ec84e59b841506a6809cb9a7d3e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10129977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5493be1b5d060e3664e0ed0105b9a117646a6c5431bf40575ce8067dfb6e624f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
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
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2242ea11d02d4b76585c5bd3c1a8d48abc89637565f98c10bc95093e2ac85fd9`  
		Last Modified: Tue, 08 Apr 2025 21:41:38 GMT  
		Size: 6.1 MB (6135979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71dc7021098449aef008fd78a2bf07e2c2cf8c6a9983fbd93e3a7d8fb02b4b44`  
		Last Modified: Tue, 08 Apr 2025 21:41:37 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ffaf0a4fe2676b683b4266bfa9f63838485fd955714979fe322e23a8ad52f6`  
		Last Modified: Tue, 08 Apr 2025 21:41:37 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:a2c32b998e310db81899db4a7ea0bf211f8177355e498a163b5ee12dce6fb8c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa451c798f073309ad1606f97a9e84b9789dc257fd3aca978f4dc90b95cd3d54`

```dockerfile
```

-	Layers:
	-	`sha256:e4657c77e9aadc2989733b284b18c737a42c14d4619111b6ee1b55d1cf4af7bc`  
		Last Modified: Tue, 08 Apr 2025 21:41:37 GMT  
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
$ docker pull nats@sha256:7a09b6190c3e41cb21a077399d30e0d7df137cf0ec3fbf442b934ccc11e3cb56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `nats:2.10-nanoserver` - windows version 10.0.17763.7009; amd64

```console
$ docker pull nats@sha256:3d7e34f37e5d3a52d700c1e79f59f13da605f176056911c06c6018aff824a881
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 MB (113200253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c130a8066e6988bb80322a1463575126ad49dcc4eac9bde949d5f8f8700245d2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Tue, 08 Apr 2025 22:14:05 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 08 Apr 2025 22:14:07 GMT
RUN cmd /S /C #(nop) COPY file:911e7fad0174090a7de06fb3b7fca63c95843409a6ad46e295d2fe4da8d99d2a in C:\nats-server.exe 
# Tue, 08 Apr 2025 22:14:08 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 08 Apr 2025 22:14:08 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 08 Apr 2025 22:14:09 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 08 Apr 2025 22:14:10 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f6acdbafb61d829b0f8ca95b32b0ccf5c447f898e355108570cd0259ebc5a57`  
		Last Modified: Tue, 08 Apr 2025 22:14:13 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1676b0df597845c0dedf663901c220c1f121d58fdb561a439eab94cc89768819`  
		Last Modified: Tue, 08 Apr 2025 22:14:13 GMT  
		Size: 6.3 MB (6286693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0255179dc6894853ae0159b887a38b465dc585c5e4bd328251f9ae51f8cdcb`  
		Last Modified: Tue, 08 Apr 2025 22:14:12 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200a3150dce3b9d8ce51c430fd9c9e14d344ef75ba9e466d85bfb7b3f7a91f45`  
		Last Modified: Tue, 08 Apr 2025 22:14:12 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b404aa582bdecfbf7bdbc91ee90de91d6d15d6d6202b2d6727682002378e67`  
		Last Modified: Tue, 08 Apr 2025 22:14:12 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e127e6a4caa3eab8729eae82aa5d747dc650fe981906ec050f43cdeb2c89e337`  
		Last Modified: Tue, 08 Apr 2025 22:14:12 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-nanoserver-1809`

```console
$ docker pull nats@sha256:7a09b6190c3e41cb21a077399d30e0d7df137cf0ec3fbf442b934ccc11e3cb56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `nats:2.10-nanoserver-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull nats@sha256:3d7e34f37e5d3a52d700c1e79f59f13da605f176056911c06c6018aff824a881
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 MB (113200253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c130a8066e6988bb80322a1463575126ad49dcc4eac9bde949d5f8f8700245d2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Tue, 08 Apr 2025 22:14:05 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 08 Apr 2025 22:14:07 GMT
RUN cmd /S /C #(nop) COPY file:911e7fad0174090a7de06fb3b7fca63c95843409a6ad46e295d2fe4da8d99d2a in C:\nats-server.exe 
# Tue, 08 Apr 2025 22:14:08 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 08 Apr 2025 22:14:08 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 08 Apr 2025 22:14:09 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 08 Apr 2025 22:14:10 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f6acdbafb61d829b0f8ca95b32b0ccf5c447f898e355108570cd0259ebc5a57`  
		Last Modified: Tue, 08 Apr 2025 22:14:13 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1676b0df597845c0dedf663901c220c1f121d58fdb561a439eab94cc89768819`  
		Last Modified: Tue, 08 Apr 2025 22:14:13 GMT  
		Size: 6.3 MB (6286693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0255179dc6894853ae0159b887a38b465dc585c5e4bd328251f9ae51f8cdcb`  
		Last Modified: Tue, 08 Apr 2025 22:14:12 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200a3150dce3b9d8ce51c430fd9c9e14d344ef75ba9e466d85bfb7b3f7a91f45`  
		Last Modified: Tue, 08 Apr 2025 22:14:12 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b404aa582bdecfbf7bdbc91ee90de91d6d15d6d6202b2d6727682002378e67`  
		Last Modified: Tue, 08 Apr 2025 22:14:12 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e127e6a4caa3eab8729eae82aa5d747dc650fe981906ec050f43cdeb2c89e337`  
		Last Modified: Tue, 08 Apr 2025 22:14:12 GMT  
		Size: 1.1 KB (1066 bytes)  
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
$ docker pull nats@sha256:1891d93647864dd6c6318d048b949015c6216d8ec11bf9e37b3891576a17178c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7136; amd64

### `nats:2.10-windowsservercore` - windows version 10.0.17763.7136; amd64

```console
$ docker pull nats@sha256:0c65c0a3388c8af8374786ff39e40da34f73388c9e7c2ac9f5d68a8fc316acca
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2169683478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2fad4e7d9b5aa00f12f1db4af938391b8585f97908aa5a3ad2c5f8bc525d0c6`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Sat, 05 Apr 2025 01:48:05 GMT
RUN Install update 10.0.17763.7136
# Wed, 09 Apr 2025 00:43:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Apr 2025 00:43:38 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Apr 2025 00:43:39 GMT
ENV NATS_SERVER=2.10.27
# Wed, 09 Apr 2025 00:43:39 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.27/nats-server-v2.10.27-windows-amd64.zip
# Wed, 09 Apr 2025 00:43:40 GMT
ENV NATS_SERVER_SHASUM=f7033b98f4e063cc4790e3a1ec4853f2f5f6a474fea6090de8a04f851d46e277
# Wed, 09 Apr 2025 00:44:17 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Apr 2025 00:44:36 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Apr 2025 00:44:36 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 09 Apr 2025 00:44:37 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Apr 2025 00:44:37 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Apr 2025 00:44:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d949f82a48e7c53af792160596b10005419fbc7ecfed6bc45bbeee3a5a2f07`  
		Last Modified: Tue, 08 Apr 2025 19:58:26 GMT  
		Size: 442.5 MB (442457492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540e7bd3125ffb496f680b3d3952bbd22366a9e752d5e6dec96247e803bccb1c`  
		Last Modified: Wed, 09 Apr 2025 00:44:45 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4303d2939dc9258d4246ccf0b03d1b918228e2943a9afd52231d4dd8c154d963`  
		Last Modified: Wed, 09 Apr 2025 00:44:44 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7220d22cc412fb6cd92dec83b8529607fd3947ca9278fe98676540912765b9bc`  
		Last Modified: Wed, 09 Apr 2025 00:44:43 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e4fac0229d5f697947bc4e94df7e69ad0bfe018e14f6b53b9cecc2f8c91e2ef`  
		Last Modified: Wed, 09 Apr 2025 00:44:43 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18acb882f8d1bb26c7653c14ef093477843f41e93816ce568f1115924d969ba9`  
		Last Modified: Wed, 09 Apr 2025 00:44:43 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ecbb058dda4e8fe8642c51a93cc392d939ccd5916a2621444beefb16500e56`  
		Last Modified: Wed, 09 Apr 2025 00:44:43 GMT  
		Size: 325.0 KB (324974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e8bdd7909f61900c12df66f2df4ca7b73b05f52880bee030fffd9deafc19f4`  
		Last Modified: Wed, 09 Apr 2025 00:44:42 GMT  
		Size: 6.6 MB (6620330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ec9ac762bf362919d19a102678196cbfd27ef99b482ce5c3066ab9c430b653`  
		Last Modified: Wed, 09 Apr 2025 00:44:41 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36eeb493e51587becf998fe959c2e9ce9a7c774276e3e4226e929a48aee96486`  
		Last Modified: Wed, 09 Apr 2025 00:44:41 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7555d365971bb67d94c5fd08e40eee4148342a147ff03a8ebf04c4f26aefc478`  
		Last Modified: Wed, 09 Apr 2025 00:44:41 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e0e5f7029d615dba38afe0c91afe73cbeb5a1f9be9ef939b1afa3c5ed79bd2`  
		Last Modified: Wed, 09 Apr 2025 00:44:41 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-windowsservercore-1809`

```console
$ docker pull nats@sha256:1891d93647864dd6c6318d048b949015c6216d8ec11bf9e37b3891576a17178c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7136; amd64

### `nats:2.10-windowsservercore-1809` - windows version 10.0.17763.7136; amd64

```console
$ docker pull nats@sha256:0c65c0a3388c8af8374786ff39e40da34f73388c9e7c2ac9f5d68a8fc316acca
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2169683478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2fad4e7d9b5aa00f12f1db4af938391b8585f97908aa5a3ad2c5f8bc525d0c6`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Sat, 05 Apr 2025 01:48:05 GMT
RUN Install update 10.0.17763.7136
# Wed, 09 Apr 2025 00:43:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Apr 2025 00:43:38 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Apr 2025 00:43:39 GMT
ENV NATS_SERVER=2.10.27
# Wed, 09 Apr 2025 00:43:39 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.27/nats-server-v2.10.27-windows-amd64.zip
# Wed, 09 Apr 2025 00:43:40 GMT
ENV NATS_SERVER_SHASUM=f7033b98f4e063cc4790e3a1ec4853f2f5f6a474fea6090de8a04f851d46e277
# Wed, 09 Apr 2025 00:44:17 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Apr 2025 00:44:36 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Apr 2025 00:44:36 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 09 Apr 2025 00:44:37 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Apr 2025 00:44:37 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Apr 2025 00:44:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d949f82a48e7c53af792160596b10005419fbc7ecfed6bc45bbeee3a5a2f07`  
		Last Modified: Tue, 08 Apr 2025 19:58:26 GMT  
		Size: 442.5 MB (442457492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540e7bd3125ffb496f680b3d3952bbd22366a9e752d5e6dec96247e803bccb1c`  
		Last Modified: Wed, 09 Apr 2025 00:44:45 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4303d2939dc9258d4246ccf0b03d1b918228e2943a9afd52231d4dd8c154d963`  
		Last Modified: Wed, 09 Apr 2025 00:44:44 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7220d22cc412fb6cd92dec83b8529607fd3947ca9278fe98676540912765b9bc`  
		Last Modified: Wed, 09 Apr 2025 00:44:43 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e4fac0229d5f697947bc4e94df7e69ad0bfe018e14f6b53b9cecc2f8c91e2ef`  
		Last Modified: Wed, 09 Apr 2025 00:44:43 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18acb882f8d1bb26c7653c14ef093477843f41e93816ce568f1115924d969ba9`  
		Last Modified: Wed, 09 Apr 2025 00:44:43 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ecbb058dda4e8fe8642c51a93cc392d939ccd5916a2621444beefb16500e56`  
		Last Modified: Wed, 09 Apr 2025 00:44:43 GMT  
		Size: 325.0 KB (324974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e8bdd7909f61900c12df66f2df4ca7b73b05f52880bee030fffd9deafc19f4`  
		Last Modified: Wed, 09 Apr 2025 00:44:42 GMT  
		Size: 6.6 MB (6620330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ec9ac762bf362919d19a102678196cbfd27ef99b482ce5c3066ab9c430b653`  
		Last Modified: Wed, 09 Apr 2025 00:44:41 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36eeb493e51587becf998fe959c2e9ce9a7c774276e3e4226e929a48aee96486`  
		Last Modified: Wed, 09 Apr 2025 00:44:41 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7555d365971bb67d94c5fd08e40eee4148342a147ff03a8ebf04c4f26aefc478`  
		Last Modified: Wed, 09 Apr 2025 00:44:41 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e0e5f7029d615dba38afe0c91afe73cbeb5a1f9be9ef939b1afa3c5ed79bd2`  
		Last Modified: Wed, 09 Apr 2025 00:44:41 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.27`

```console
$ docker pull nats@sha256:8a808485b1a116d6908fa81e328be83b01bf0da6cf8bb95f34681dedf3d8d84c
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
	-	windows version 10.0.17763.7009; amd64

### `nats:2.10.27` - linux; amd64

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

### `nats:2.10.27` - unknown; unknown

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

### `nats:2.10.27` - linux; arm variant v6

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

### `nats:2.10.27` - unknown; unknown

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

### `nats:2.10.27` - linux; arm variant v7

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

### `nats:2.10.27` - unknown; unknown

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

### `nats:2.10.27` - linux; arm64 variant v8

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

### `nats:2.10.27` - unknown; unknown

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

### `nats:2.10.27` - linux; ppc64le

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

### `nats:2.10.27` - unknown; unknown

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

### `nats:2.10.27` - linux; s390x

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

### `nats:2.10.27` - unknown; unknown

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

### `nats:2.10.27` - windows version 10.0.17763.7009; amd64

```console
$ docker pull nats@sha256:3d7e34f37e5d3a52d700c1e79f59f13da605f176056911c06c6018aff824a881
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 MB (113200253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c130a8066e6988bb80322a1463575126ad49dcc4eac9bde949d5f8f8700245d2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Tue, 08 Apr 2025 22:14:05 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 08 Apr 2025 22:14:07 GMT
RUN cmd /S /C #(nop) COPY file:911e7fad0174090a7de06fb3b7fca63c95843409a6ad46e295d2fe4da8d99d2a in C:\nats-server.exe 
# Tue, 08 Apr 2025 22:14:08 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 08 Apr 2025 22:14:08 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 08 Apr 2025 22:14:09 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 08 Apr 2025 22:14:10 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f6acdbafb61d829b0f8ca95b32b0ccf5c447f898e355108570cd0259ebc5a57`  
		Last Modified: Tue, 08 Apr 2025 22:14:13 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1676b0df597845c0dedf663901c220c1f121d58fdb561a439eab94cc89768819`  
		Last Modified: Tue, 08 Apr 2025 22:14:13 GMT  
		Size: 6.3 MB (6286693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0255179dc6894853ae0159b887a38b465dc585c5e4bd328251f9ae51f8cdcb`  
		Last Modified: Tue, 08 Apr 2025 22:14:12 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200a3150dce3b9d8ce51c430fd9c9e14d344ef75ba9e466d85bfb7b3f7a91f45`  
		Last Modified: Tue, 08 Apr 2025 22:14:12 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b404aa582bdecfbf7bdbc91ee90de91d6d15d6d6202b2d6727682002378e67`  
		Last Modified: Tue, 08 Apr 2025 22:14:12 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e127e6a4caa3eab8729eae82aa5d747dc650fe981906ec050f43cdeb2c89e337`  
		Last Modified: Tue, 08 Apr 2025 22:14:12 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.27-alpine`

```console
$ docker pull nats@sha256:e243c53e5b2ebf24f5d8f05d7555462003c050a51ee0a2643d2dc89aea6d06a5
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

### `nats:2.10.27-alpine` - linux; amd64

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

### `nats:2.10.27-alpine` - unknown; unknown

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

### `nats:2.10.27-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:4632ca3d999fe68493ea2ed5d84dd51b01007f17a9541cb4e1699f69b14e567d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9721153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f606fc733c44eafa7b41bec8d259da9c5fd26276df8894ccf42d3f6373e7e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
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
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c4d4ac036d3e9ea1b0876b5fb0a2495ed304d6b156011acfe4edd6015f06bf`  
		Last Modified: Tue, 08 Apr 2025 20:28:41 GMT  
		Size: 6.4 MB (6355452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33387efebc89387e808c896b85201ab384cad0eb689aeb33150ee974d9bc86c6`  
		Last Modified: Tue, 08 Apr 2025 20:28:40 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a506ef078ce7ef90659eb2c5c6cdd9e168db5c649df636b995d7850d6ba123`  
		Last Modified: Tue, 08 Apr 2025 20:28:40 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.27-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:853dad0f33fa0d69187c3cb1a45872db5706b82f34ef463c8600574cc8665d5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eead0a360dfced7c60114991f1f7efc861cab15f454c29ca5dea2c21a9b2270`

```dockerfile
```

-	Layers:
	-	`sha256:beb17eeae7561e658284ca176f32ee1ff0b554e3baf90d450e8b7a768121a83e`  
		Last Modified: Tue, 08 Apr 2025 20:28:40 GMT  
		Size: 13.2 KB (13197 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.27-alpine` - linux; arm variant v7

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

### `nats:2.10.27-alpine` - unknown; unknown

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

### `nats:2.10.27-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:799daf4b6cf85a36125e0d6bec2533a0c8b5ec84e59b841506a6809cb9a7d3e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10129977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5493be1b5d060e3664e0ed0105b9a117646a6c5431bf40575ce8067dfb6e624f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
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
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2242ea11d02d4b76585c5bd3c1a8d48abc89637565f98c10bc95093e2ac85fd9`  
		Last Modified: Tue, 08 Apr 2025 21:41:38 GMT  
		Size: 6.1 MB (6135979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71dc7021098449aef008fd78a2bf07e2c2cf8c6a9983fbd93e3a7d8fb02b4b44`  
		Last Modified: Tue, 08 Apr 2025 21:41:37 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ffaf0a4fe2676b683b4266bfa9f63838485fd955714979fe322e23a8ad52f6`  
		Last Modified: Tue, 08 Apr 2025 21:41:37 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.27-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:a2c32b998e310db81899db4a7ea0bf211f8177355e498a163b5ee12dce6fb8c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa451c798f073309ad1606f97a9e84b9789dc257fd3aca978f4dc90b95cd3d54`

```dockerfile
```

-	Layers:
	-	`sha256:e4657c77e9aadc2989733b284b18c737a42c14d4619111b6ee1b55d1cf4af7bc`  
		Last Modified: Tue, 08 Apr 2025 21:41:37 GMT  
		Size: 13.2 KB (13226 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.27-alpine` - linux; ppc64le

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

### `nats:2.10.27-alpine` - unknown; unknown

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

### `nats:2.10.27-alpine` - linux; s390x

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

### `nats:2.10.27-alpine` - unknown; unknown

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

## `nats:2.10.27-alpine3.21`

```console
$ docker pull nats@sha256:e243c53e5b2ebf24f5d8f05d7555462003c050a51ee0a2643d2dc89aea6d06a5
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

### `nats:2.10.27-alpine3.21` - linux; amd64

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

### `nats:2.10.27-alpine3.21` - unknown; unknown

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

### `nats:2.10.27-alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:4632ca3d999fe68493ea2ed5d84dd51b01007f17a9541cb4e1699f69b14e567d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9721153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f606fc733c44eafa7b41bec8d259da9c5fd26276df8894ccf42d3f6373e7e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
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
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c4d4ac036d3e9ea1b0876b5fb0a2495ed304d6b156011acfe4edd6015f06bf`  
		Last Modified: Tue, 08 Apr 2025 20:28:41 GMT  
		Size: 6.4 MB (6355452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33387efebc89387e808c896b85201ab384cad0eb689aeb33150ee974d9bc86c6`  
		Last Modified: Tue, 08 Apr 2025 20:28:40 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a506ef078ce7ef90659eb2c5c6cdd9e168db5c649df636b995d7850d6ba123`  
		Last Modified: Tue, 08 Apr 2025 20:28:40 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.27-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:853dad0f33fa0d69187c3cb1a45872db5706b82f34ef463c8600574cc8665d5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eead0a360dfced7c60114991f1f7efc861cab15f454c29ca5dea2c21a9b2270`

```dockerfile
```

-	Layers:
	-	`sha256:beb17eeae7561e658284ca176f32ee1ff0b554e3baf90d450e8b7a768121a83e`  
		Last Modified: Tue, 08 Apr 2025 20:28:40 GMT  
		Size: 13.2 KB (13197 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.27-alpine3.21` - linux; arm variant v7

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

### `nats:2.10.27-alpine3.21` - unknown; unknown

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

### `nats:2.10.27-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:799daf4b6cf85a36125e0d6bec2533a0c8b5ec84e59b841506a6809cb9a7d3e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10129977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5493be1b5d060e3664e0ed0105b9a117646a6c5431bf40575ce8067dfb6e624f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
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
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2242ea11d02d4b76585c5bd3c1a8d48abc89637565f98c10bc95093e2ac85fd9`  
		Last Modified: Tue, 08 Apr 2025 21:41:38 GMT  
		Size: 6.1 MB (6135979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71dc7021098449aef008fd78a2bf07e2c2cf8c6a9983fbd93e3a7d8fb02b4b44`  
		Last Modified: Tue, 08 Apr 2025 21:41:37 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ffaf0a4fe2676b683b4266bfa9f63838485fd955714979fe322e23a8ad52f6`  
		Last Modified: Tue, 08 Apr 2025 21:41:37 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.27-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:a2c32b998e310db81899db4a7ea0bf211f8177355e498a163b5ee12dce6fb8c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa451c798f073309ad1606f97a9e84b9789dc257fd3aca978f4dc90b95cd3d54`

```dockerfile
```

-	Layers:
	-	`sha256:e4657c77e9aadc2989733b284b18c737a42c14d4619111b6ee1b55d1cf4af7bc`  
		Last Modified: Tue, 08 Apr 2025 21:41:37 GMT  
		Size: 13.2 KB (13226 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.27-alpine3.21` - linux; ppc64le

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

### `nats:2.10.27-alpine3.21` - unknown; unknown

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

### `nats:2.10.27-alpine3.21` - linux; s390x

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

### `nats:2.10.27-alpine3.21` - unknown; unknown

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

## `nats:2.10.27-linux`

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

### `nats:2.10.27-linux` - linux; amd64

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

### `nats:2.10.27-linux` - unknown; unknown

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

### `nats:2.10.27-linux` - linux; arm variant v6

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

### `nats:2.10.27-linux` - unknown; unknown

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

### `nats:2.10.27-linux` - linux; arm variant v7

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

### `nats:2.10.27-linux` - unknown; unknown

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

### `nats:2.10.27-linux` - linux; arm64 variant v8

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

### `nats:2.10.27-linux` - unknown; unknown

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

### `nats:2.10.27-linux` - linux; ppc64le

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

### `nats:2.10.27-linux` - unknown; unknown

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

### `nats:2.10.27-linux` - linux; s390x

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

### `nats:2.10.27-linux` - unknown; unknown

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

## `nats:2.10.27-nanoserver`

```console
$ docker pull nats@sha256:7a09b6190c3e41cb21a077399d30e0d7df137cf0ec3fbf442b934ccc11e3cb56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `nats:2.10.27-nanoserver` - windows version 10.0.17763.7009; amd64

```console
$ docker pull nats@sha256:3d7e34f37e5d3a52d700c1e79f59f13da605f176056911c06c6018aff824a881
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 MB (113200253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c130a8066e6988bb80322a1463575126ad49dcc4eac9bde949d5f8f8700245d2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Tue, 08 Apr 2025 22:14:05 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 08 Apr 2025 22:14:07 GMT
RUN cmd /S /C #(nop) COPY file:911e7fad0174090a7de06fb3b7fca63c95843409a6ad46e295d2fe4da8d99d2a in C:\nats-server.exe 
# Tue, 08 Apr 2025 22:14:08 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 08 Apr 2025 22:14:08 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 08 Apr 2025 22:14:09 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 08 Apr 2025 22:14:10 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f6acdbafb61d829b0f8ca95b32b0ccf5c447f898e355108570cd0259ebc5a57`  
		Last Modified: Tue, 08 Apr 2025 22:14:13 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1676b0df597845c0dedf663901c220c1f121d58fdb561a439eab94cc89768819`  
		Last Modified: Tue, 08 Apr 2025 22:14:13 GMT  
		Size: 6.3 MB (6286693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0255179dc6894853ae0159b887a38b465dc585c5e4bd328251f9ae51f8cdcb`  
		Last Modified: Tue, 08 Apr 2025 22:14:12 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200a3150dce3b9d8ce51c430fd9c9e14d344ef75ba9e466d85bfb7b3f7a91f45`  
		Last Modified: Tue, 08 Apr 2025 22:14:12 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b404aa582bdecfbf7bdbc91ee90de91d6d15d6d6202b2d6727682002378e67`  
		Last Modified: Tue, 08 Apr 2025 22:14:12 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e127e6a4caa3eab8729eae82aa5d747dc650fe981906ec050f43cdeb2c89e337`  
		Last Modified: Tue, 08 Apr 2025 22:14:12 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.27-nanoserver-1809`

```console
$ docker pull nats@sha256:7a09b6190c3e41cb21a077399d30e0d7df137cf0ec3fbf442b934ccc11e3cb56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `nats:2.10.27-nanoserver-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull nats@sha256:3d7e34f37e5d3a52d700c1e79f59f13da605f176056911c06c6018aff824a881
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 MB (113200253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c130a8066e6988bb80322a1463575126ad49dcc4eac9bde949d5f8f8700245d2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Tue, 08 Apr 2025 22:14:05 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 08 Apr 2025 22:14:07 GMT
RUN cmd /S /C #(nop) COPY file:911e7fad0174090a7de06fb3b7fca63c95843409a6ad46e295d2fe4da8d99d2a in C:\nats-server.exe 
# Tue, 08 Apr 2025 22:14:08 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 08 Apr 2025 22:14:08 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 08 Apr 2025 22:14:09 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 08 Apr 2025 22:14:10 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f6acdbafb61d829b0f8ca95b32b0ccf5c447f898e355108570cd0259ebc5a57`  
		Last Modified: Tue, 08 Apr 2025 22:14:13 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1676b0df597845c0dedf663901c220c1f121d58fdb561a439eab94cc89768819`  
		Last Modified: Tue, 08 Apr 2025 22:14:13 GMT  
		Size: 6.3 MB (6286693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0255179dc6894853ae0159b887a38b465dc585c5e4bd328251f9ae51f8cdcb`  
		Last Modified: Tue, 08 Apr 2025 22:14:12 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200a3150dce3b9d8ce51c430fd9c9e14d344ef75ba9e466d85bfb7b3f7a91f45`  
		Last Modified: Tue, 08 Apr 2025 22:14:12 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b404aa582bdecfbf7bdbc91ee90de91d6d15d6d6202b2d6727682002378e67`  
		Last Modified: Tue, 08 Apr 2025 22:14:12 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e127e6a4caa3eab8729eae82aa5d747dc650fe981906ec050f43cdeb2c89e337`  
		Last Modified: Tue, 08 Apr 2025 22:14:12 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.27-scratch`

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

### `nats:2.10.27-scratch` - linux; amd64

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

### `nats:2.10.27-scratch` - unknown; unknown

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

### `nats:2.10.27-scratch` - linux; arm variant v6

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

### `nats:2.10.27-scratch` - unknown; unknown

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

### `nats:2.10.27-scratch` - linux; arm variant v7

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

### `nats:2.10.27-scratch` - unknown; unknown

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

### `nats:2.10.27-scratch` - linux; arm64 variant v8

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

### `nats:2.10.27-scratch` - unknown; unknown

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

### `nats:2.10.27-scratch` - linux; ppc64le

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

### `nats:2.10.27-scratch` - unknown; unknown

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

### `nats:2.10.27-scratch` - linux; s390x

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

### `nats:2.10.27-scratch` - unknown; unknown

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

## `nats:2.10.27-windowsservercore`

```console
$ docker pull nats@sha256:1891d93647864dd6c6318d048b949015c6216d8ec11bf9e37b3891576a17178c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7136; amd64

### `nats:2.10.27-windowsservercore` - windows version 10.0.17763.7136; amd64

```console
$ docker pull nats@sha256:0c65c0a3388c8af8374786ff39e40da34f73388c9e7c2ac9f5d68a8fc316acca
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2169683478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2fad4e7d9b5aa00f12f1db4af938391b8585f97908aa5a3ad2c5f8bc525d0c6`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Sat, 05 Apr 2025 01:48:05 GMT
RUN Install update 10.0.17763.7136
# Wed, 09 Apr 2025 00:43:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Apr 2025 00:43:38 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Apr 2025 00:43:39 GMT
ENV NATS_SERVER=2.10.27
# Wed, 09 Apr 2025 00:43:39 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.27/nats-server-v2.10.27-windows-amd64.zip
# Wed, 09 Apr 2025 00:43:40 GMT
ENV NATS_SERVER_SHASUM=f7033b98f4e063cc4790e3a1ec4853f2f5f6a474fea6090de8a04f851d46e277
# Wed, 09 Apr 2025 00:44:17 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Apr 2025 00:44:36 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Apr 2025 00:44:36 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 09 Apr 2025 00:44:37 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Apr 2025 00:44:37 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Apr 2025 00:44:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d949f82a48e7c53af792160596b10005419fbc7ecfed6bc45bbeee3a5a2f07`  
		Last Modified: Tue, 08 Apr 2025 19:58:26 GMT  
		Size: 442.5 MB (442457492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540e7bd3125ffb496f680b3d3952bbd22366a9e752d5e6dec96247e803bccb1c`  
		Last Modified: Wed, 09 Apr 2025 00:44:45 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4303d2939dc9258d4246ccf0b03d1b918228e2943a9afd52231d4dd8c154d963`  
		Last Modified: Wed, 09 Apr 2025 00:44:44 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7220d22cc412fb6cd92dec83b8529607fd3947ca9278fe98676540912765b9bc`  
		Last Modified: Wed, 09 Apr 2025 00:44:43 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e4fac0229d5f697947bc4e94df7e69ad0bfe018e14f6b53b9cecc2f8c91e2ef`  
		Last Modified: Wed, 09 Apr 2025 00:44:43 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18acb882f8d1bb26c7653c14ef093477843f41e93816ce568f1115924d969ba9`  
		Last Modified: Wed, 09 Apr 2025 00:44:43 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ecbb058dda4e8fe8642c51a93cc392d939ccd5916a2621444beefb16500e56`  
		Last Modified: Wed, 09 Apr 2025 00:44:43 GMT  
		Size: 325.0 KB (324974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e8bdd7909f61900c12df66f2df4ca7b73b05f52880bee030fffd9deafc19f4`  
		Last Modified: Wed, 09 Apr 2025 00:44:42 GMT  
		Size: 6.6 MB (6620330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ec9ac762bf362919d19a102678196cbfd27ef99b482ce5c3066ab9c430b653`  
		Last Modified: Wed, 09 Apr 2025 00:44:41 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36eeb493e51587becf998fe959c2e9ce9a7c774276e3e4226e929a48aee96486`  
		Last Modified: Wed, 09 Apr 2025 00:44:41 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7555d365971bb67d94c5fd08e40eee4148342a147ff03a8ebf04c4f26aefc478`  
		Last Modified: Wed, 09 Apr 2025 00:44:41 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e0e5f7029d615dba38afe0c91afe73cbeb5a1f9be9ef939b1afa3c5ed79bd2`  
		Last Modified: Wed, 09 Apr 2025 00:44:41 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.27-windowsservercore-1809`

```console
$ docker pull nats@sha256:1891d93647864dd6c6318d048b949015c6216d8ec11bf9e37b3891576a17178c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7136; amd64

### `nats:2.10.27-windowsservercore-1809` - windows version 10.0.17763.7136; amd64

```console
$ docker pull nats@sha256:0c65c0a3388c8af8374786ff39e40da34f73388c9e7c2ac9f5d68a8fc316acca
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2169683478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2fad4e7d9b5aa00f12f1db4af938391b8585f97908aa5a3ad2c5f8bc525d0c6`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Sat, 05 Apr 2025 01:48:05 GMT
RUN Install update 10.0.17763.7136
# Wed, 09 Apr 2025 00:43:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Apr 2025 00:43:38 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Apr 2025 00:43:39 GMT
ENV NATS_SERVER=2.10.27
# Wed, 09 Apr 2025 00:43:39 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.27/nats-server-v2.10.27-windows-amd64.zip
# Wed, 09 Apr 2025 00:43:40 GMT
ENV NATS_SERVER_SHASUM=f7033b98f4e063cc4790e3a1ec4853f2f5f6a474fea6090de8a04f851d46e277
# Wed, 09 Apr 2025 00:44:17 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Apr 2025 00:44:36 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Apr 2025 00:44:36 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 09 Apr 2025 00:44:37 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Apr 2025 00:44:37 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Apr 2025 00:44:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d949f82a48e7c53af792160596b10005419fbc7ecfed6bc45bbeee3a5a2f07`  
		Last Modified: Tue, 08 Apr 2025 19:58:26 GMT  
		Size: 442.5 MB (442457492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540e7bd3125ffb496f680b3d3952bbd22366a9e752d5e6dec96247e803bccb1c`  
		Last Modified: Wed, 09 Apr 2025 00:44:45 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4303d2939dc9258d4246ccf0b03d1b918228e2943a9afd52231d4dd8c154d963`  
		Last Modified: Wed, 09 Apr 2025 00:44:44 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7220d22cc412fb6cd92dec83b8529607fd3947ca9278fe98676540912765b9bc`  
		Last Modified: Wed, 09 Apr 2025 00:44:43 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e4fac0229d5f697947bc4e94df7e69ad0bfe018e14f6b53b9cecc2f8c91e2ef`  
		Last Modified: Wed, 09 Apr 2025 00:44:43 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18acb882f8d1bb26c7653c14ef093477843f41e93816ce568f1115924d969ba9`  
		Last Modified: Wed, 09 Apr 2025 00:44:43 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ecbb058dda4e8fe8642c51a93cc392d939ccd5916a2621444beefb16500e56`  
		Last Modified: Wed, 09 Apr 2025 00:44:43 GMT  
		Size: 325.0 KB (324974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e8bdd7909f61900c12df66f2df4ca7b73b05f52880bee030fffd9deafc19f4`  
		Last Modified: Wed, 09 Apr 2025 00:44:42 GMT  
		Size: 6.6 MB (6620330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ec9ac762bf362919d19a102678196cbfd27ef99b482ce5c3066ab9c430b653`  
		Last Modified: Wed, 09 Apr 2025 00:44:41 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36eeb493e51587becf998fe959c2e9ce9a7c774276e3e4226e929a48aee96486`  
		Last Modified: Wed, 09 Apr 2025 00:44:41 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7555d365971bb67d94c5fd08e40eee4148342a147ff03a8ebf04c4f26aefc478`  
		Last Modified: Wed, 09 Apr 2025 00:44:41 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e0e5f7029d615dba38afe0c91afe73cbeb5a1f9be9ef939b1afa3c5ed79bd2`  
		Last Modified: Wed, 09 Apr 2025 00:44:41 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11`

```console
$ docker pull nats@sha256:d80d5773c4e558914e79e2886f54a64963d1f07d8638b0c49217cf6fb8e95049
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
	-	windows version 10.0.17763.7009; amd64

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

### `nats:2.11` - windows version 10.0.17763.7009; amd64

```console
$ docker pull nats@sha256:715ccd4de0bcee69815ad68778b62f6b9373b757afb53337ede87f360c5a010e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113369449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3d563f68baff6d95b9b2b72e3ae34a23681a1a3f2185a8990940cd3a979268a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Tue, 08 Apr 2025 22:13:52 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 08 Apr 2025 22:13:55 GMT
RUN cmd /S /C #(nop) COPY file:eee3870bfbcd9bfddd3622d20a6c2075b583b61ab0944602ceefed02dee11aa2 in C:\nats-server.exe 
# Tue, 08 Apr 2025 22:13:56 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 08 Apr 2025 22:13:57 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 08 Apr 2025 22:13:57 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 08 Apr 2025 22:13:58 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cfa145690c6aebcb679b25530d2fe0c89c7895d522bc2a51865f9318b005b5f`  
		Last Modified: Tue, 08 Apr 2025 22:14:02 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935788f0279b4a2c1b70d0513fd91be7c0c51126d6ea20137c285b06b5bb1f72`  
		Last Modified: Tue, 08 Apr 2025 22:14:02 GMT  
		Size: 6.5 MB (6455907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f144255a54963a1049be6601f86720694f66bb79a738c6f8bd9f1e50cf078872`  
		Last Modified: Tue, 08 Apr 2025 22:14:01 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55833ccd9e0a66322e50524b64d784272932816426d2b868274b94d5eda2b9cb`  
		Last Modified: Tue, 08 Apr 2025 22:14:01 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba94d6c3b308280e6cb389c9f65d5fca970fe7338eb34c025df4d83870244a4`  
		Last Modified: Tue, 08 Apr 2025 22:14:01 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07636e21dc67f902c5b4325c6a45d77f4c0717a519e17f32f1079e8988eb7bbb`  
		Last Modified: Tue, 08 Apr 2025 22:14:01 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-alpine`

```console
$ docker pull nats@sha256:f3d9be9e3809381297c6fc2e1d071bbab2ff25df5fa89e89edbd00fce34f1ca0
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
$ docker pull nats@sha256:33bedd609f7f7f31c7a609239dff642b098d339b2ae5c72f358aca3b0bdfcd99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9830618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f144ccbbca357bd10e864ad6a9469caf63d49af1182de50d7da5e3d4641bcf0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
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
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9048a08e892a91b40d37a992fb9228a855e04b86a0193658785404d407502c36`  
		Last Modified: Tue, 08 Apr 2025 20:28:28 GMT  
		Size: 6.5 MB (6464916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b28e407313ff54262ed40c18741ab1d8d650c46875eb53e1f4dae7a19d64f0`  
		Last Modified: Tue, 08 Apr 2025 20:28:28 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1037b517e6fb05b376c0f845c2de48f91d85acef85548878752fff9e0e5fcb4e`  
		Last Modified: Tue, 08 Apr 2025 20:28:28 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:f99dfd48fc9fbd2ad2bda5e2128399c2608b793c2df1677489b75ed55c958c80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76d73ac2a38ee74207ea6780edbe4013fa25eafa0ecf5318e88d09592d7da396`

```dockerfile
```

-	Layers:
	-	`sha256:a5c19b7d31f9642dc7ccbb0d73e2008fec7c606c270d5f41a4a1d534c57eb386`  
		Last Modified: Tue, 08 Apr 2025 20:28:27 GMT  
		Size: 14.4 KB (14425 bytes)  
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
$ docker pull nats@sha256:bc972962a3f6fd357ba4b57dcf878b3c6958fa2fbf75b65bf909c33b47f740e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10234750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:413538651b4a89933595bd87d769140c04c8eae8fac10ef3ff3a2d91bc53712f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
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
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b621e6959e97eb3ca377c901a7c1245231edc4c09198cb628915b5d3e10736c`  
		Last Modified: Tue, 08 Apr 2025 21:41:26 GMT  
		Size: 6.2 MB (6240748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1118a4f264db0d527eda19b814faffbbb61a8097f95ef2157fab3c21c0da752e`  
		Last Modified: Tue, 08 Apr 2025 21:41:25 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd107cb6fb6fc67b6484a7213268c505f995d9ec489e02602183d895d2cf6142`  
		Last Modified: Tue, 08 Apr 2025 21:41:25 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:dbcfea7b097433117d3ae7e09f5c5824d45dd3d22107d68ef1a2d3080a3742ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43ca0929e9d902e26a1809f5bc3001f3f41b0dc140fd461409cd02b47a6b7219`

```dockerfile
```

-	Layers:
	-	`sha256:6477b5d99ee19ec70115adc1465de3de4a5c61690c1f3f6c597057a749b64c3a`  
		Last Modified: Tue, 08 Apr 2025 21:41:25 GMT  
		Size: 14.5 KB (14468 bytes)  
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
$ docker pull nats@sha256:f3d9be9e3809381297c6fc2e1d071bbab2ff25df5fa89e89edbd00fce34f1ca0
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
$ docker pull nats@sha256:33bedd609f7f7f31c7a609239dff642b098d339b2ae5c72f358aca3b0bdfcd99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9830618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f144ccbbca357bd10e864ad6a9469caf63d49af1182de50d7da5e3d4641bcf0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
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
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9048a08e892a91b40d37a992fb9228a855e04b86a0193658785404d407502c36`  
		Last Modified: Tue, 08 Apr 2025 20:28:28 GMT  
		Size: 6.5 MB (6464916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b28e407313ff54262ed40c18741ab1d8d650c46875eb53e1f4dae7a19d64f0`  
		Last Modified: Tue, 08 Apr 2025 20:28:28 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1037b517e6fb05b376c0f845c2de48f91d85acef85548878752fff9e0e5fcb4e`  
		Last Modified: Tue, 08 Apr 2025 20:28:28 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:f99dfd48fc9fbd2ad2bda5e2128399c2608b793c2df1677489b75ed55c958c80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76d73ac2a38ee74207ea6780edbe4013fa25eafa0ecf5318e88d09592d7da396`

```dockerfile
```

-	Layers:
	-	`sha256:a5c19b7d31f9642dc7ccbb0d73e2008fec7c606c270d5f41a4a1d534c57eb386`  
		Last Modified: Tue, 08 Apr 2025 20:28:27 GMT  
		Size: 14.4 KB (14425 bytes)  
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
$ docker pull nats@sha256:bc972962a3f6fd357ba4b57dcf878b3c6958fa2fbf75b65bf909c33b47f740e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10234750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:413538651b4a89933595bd87d769140c04c8eae8fac10ef3ff3a2d91bc53712f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
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
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b621e6959e97eb3ca377c901a7c1245231edc4c09198cb628915b5d3e10736c`  
		Last Modified: Tue, 08 Apr 2025 21:41:26 GMT  
		Size: 6.2 MB (6240748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1118a4f264db0d527eda19b814faffbbb61a8097f95ef2157fab3c21c0da752e`  
		Last Modified: Tue, 08 Apr 2025 21:41:25 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd107cb6fb6fc67b6484a7213268c505f995d9ec489e02602183d895d2cf6142`  
		Last Modified: Tue, 08 Apr 2025 21:41:25 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:dbcfea7b097433117d3ae7e09f5c5824d45dd3d22107d68ef1a2d3080a3742ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43ca0929e9d902e26a1809f5bc3001f3f41b0dc140fd461409cd02b47a6b7219`

```dockerfile
```

-	Layers:
	-	`sha256:6477b5d99ee19ec70115adc1465de3de4a5c61690c1f3f6c597057a749b64c3a`  
		Last Modified: Tue, 08 Apr 2025 21:41:25 GMT  
		Size: 14.5 KB (14468 bytes)  
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
$ docker pull nats@sha256:abf7e27366b68d9cd2043a5da962739151157116459ae937f689ebaaff08b11a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `nats:2.11-nanoserver` - windows version 10.0.17763.7009; amd64

```console
$ docker pull nats@sha256:715ccd4de0bcee69815ad68778b62f6b9373b757afb53337ede87f360c5a010e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113369449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3d563f68baff6d95b9b2b72e3ae34a23681a1a3f2185a8990940cd3a979268a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Tue, 08 Apr 2025 22:13:52 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 08 Apr 2025 22:13:55 GMT
RUN cmd /S /C #(nop) COPY file:eee3870bfbcd9bfddd3622d20a6c2075b583b61ab0944602ceefed02dee11aa2 in C:\nats-server.exe 
# Tue, 08 Apr 2025 22:13:56 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 08 Apr 2025 22:13:57 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 08 Apr 2025 22:13:57 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 08 Apr 2025 22:13:58 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cfa145690c6aebcb679b25530d2fe0c89c7895d522bc2a51865f9318b005b5f`  
		Last Modified: Tue, 08 Apr 2025 22:14:02 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935788f0279b4a2c1b70d0513fd91be7c0c51126d6ea20137c285b06b5bb1f72`  
		Last Modified: Tue, 08 Apr 2025 22:14:02 GMT  
		Size: 6.5 MB (6455907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f144255a54963a1049be6601f86720694f66bb79a738c6f8bd9f1e50cf078872`  
		Last Modified: Tue, 08 Apr 2025 22:14:01 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55833ccd9e0a66322e50524b64d784272932816426d2b868274b94d5eda2b9cb`  
		Last Modified: Tue, 08 Apr 2025 22:14:01 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba94d6c3b308280e6cb389c9f65d5fca970fe7338eb34c025df4d83870244a4`  
		Last Modified: Tue, 08 Apr 2025 22:14:01 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07636e21dc67f902c5b4325c6a45d77f4c0717a519e17f32f1079e8988eb7bbb`  
		Last Modified: Tue, 08 Apr 2025 22:14:01 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-nanoserver-1809`

```console
$ docker pull nats@sha256:abf7e27366b68d9cd2043a5da962739151157116459ae937f689ebaaff08b11a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `nats:2.11-nanoserver-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull nats@sha256:715ccd4de0bcee69815ad68778b62f6b9373b757afb53337ede87f360c5a010e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113369449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3d563f68baff6d95b9b2b72e3ae34a23681a1a3f2185a8990940cd3a979268a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Tue, 08 Apr 2025 22:13:52 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 08 Apr 2025 22:13:55 GMT
RUN cmd /S /C #(nop) COPY file:eee3870bfbcd9bfddd3622d20a6c2075b583b61ab0944602ceefed02dee11aa2 in C:\nats-server.exe 
# Tue, 08 Apr 2025 22:13:56 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 08 Apr 2025 22:13:57 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 08 Apr 2025 22:13:57 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 08 Apr 2025 22:13:58 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cfa145690c6aebcb679b25530d2fe0c89c7895d522bc2a51865f9318b005b5f`  
		Last Modified: Tue, 08 Apr 2025 22:14:02 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935788f0279b4a2c1b70d0513fd91be7c0c51126d6ea20137c285b06b5bb1f72`  
		Last Modified: Tue, 08 Apr 2025 22:14:02 GMT  
		Size: 6.5 MB (6455907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f144255a54963a1049be6601f86720694f66bb79a738c6f8bd9f1e50cf078872`  
		Last Modified: Tue, 08 Apr 2025 22:14:01 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55833ccd9e0a66322e50524b64d784272932816426d2b868274b94d5eda2b9cb`  
		Last Modified: Tue, 08 Apr 2025 22:14:01 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba94d6c3b308280e6cb389c9f65d5fca970fe7338eb34c025df4d83870244a4`  
		Last Modified: Tue, 08 Apr 2025 22:14:01 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07636e21dc67f902c5b4325c6a45d77f4c0717a519e17f32f1079e8988eb7bbb`  
		Last Modified: Tue, 08 Apr 2025 22:14:01 GMT  
		Size: 1.0 KB (1044 bytes)  
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
$ docker pull nats@sha256:d5a5a3214c03e4383b75d3a553d43f1e6966f5e1e2f2fb1f81587381822f7b76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7136; amd64

### `nats:2.11-windowsservercore` - windows version 10.0.17763.7136; amd64

```console
$ docker pull nats@sha256:607f6e73ed9007241ff50a84dba439ab79d98a3f3fb47ea3a930f688f67f3088
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2169857611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:597119b40ab372d074effb9f06eec9a9d1a3e9637ac4696ce5f338e8ff4106b3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Sat, 05 Apr 2025 01:48:05 GMT
RUN Install update 10.0.17763.7136
# Wed, 09 Apr 2025 00:59:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Apr 2025 00:59:01 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Apr 2025 00:59:02 GMT
ENV NATS_SERVER=2.11.1
# Wed, 09 Apr 2025 00:59:03 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.1/nats-server-v2.11.1-windows-amd64.zip
# Wed, 09 Apr 2025 00:59:03 GMT
ENV NATS_SERVER_SHASUM=f5594798e1b77013b674c0049070d2502c20ee6f03a04d854cac333e2a21ca20
# Wed, 09 Apr 2025 00:59:40 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Apr 2025 00:59:59 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Apr 2025 00:59:59 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 09 Apr 2025 01:00:00 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Apr 2025 01:00:00 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Apr 2025 01:00:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d949f82a48e7c53af792160596b10005419fbc7ecfed6bc45bbeee3a5a2f07`  
		Last Modified: Tue, 08 Apr 2025 19:58:26 GMT  
		Size: 442.5 MB (442457492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a09300fffebaa4864cab22c763b15a10f2bbf057547b6ff255863442e152d0`  
		Last Modified: Wed, 09 Apr 2025 01:00:09 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21038a6eaee5de691c53f4cf4d271a784a445d934945099069a55d2b2b1a69e9`  
		Last Modified: Wed, 09 Apr 2025 01:00:09 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24942860fb41d5b161011df2cd69c16f7d6847ed7b6db02a33bb64054a72788`  
		Last Modified: Wed, 09 Apr 2025 01:00:07 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e46de18cf6f2c6f8ab7a838c3809a4539af5c48187286fa9e2bba100aed7f0de`  
		Last Modified: Wed, 09 Apr 2025 01:00:07 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d3f59562780344fd3c1ba4f023d776c21499331a904bfcbd4368f20d9da6dab`  
		Last Modified: Wed, 09 Apr 2025 01:00:07 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:795d0c7a551fbfc87a25f38f1a5fa59e2655ca81e62da54e276767f53017edd0`  
		Last Modified: Wed, 09 Apr 2025 01:00:07 GMT  
		Size: 327.2 KB (327167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6cb9f352ed0567a90df0ec2d622906e5d9afe98f400ca192be89a3e899f7d9`  
		Last Modified: Wed, 09 Apr 2025 01:00:07 GMT  
		Size: 6.8 MB (6791732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0f251d7ebfa8a3ecc74f04cf48dbdfb0bbdff942b30e6e4f0d0cbf0f620229`  
		Last Modified: Wed, 09 Apr 2025 01:00:05 GMT  
		Size: 1.9 KB (1934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1994ceebe61f490ae0929761fd777cec24a750b119093e271c15448e6069772e`  
		Last Modified: Wed, 09 Apr 2025 01:00:05 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe64f8769bc81f46b33af77ab80603037a4c694a21ef49ed7c458b22bb1b3e6`  
		Last Modified: Wed, 09 Apr 2025 01:00:05 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca16d5f700915418444888d8391f2ddbdc7a15396a440fbbef200bb6a460b19a`  
		Last Modified: Wed, 09 Apr 2025 01:00:06 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-windowsservercore-1809`

```console
$ docker pull nats@sha256:d5a5a3214c03e4383b75d3a553d43f1e6966f5e1e2f2fb1f81587381822f7b76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7136; amd64

### `nats:2.11-windowsservercore-1809` - windows version 10.0.17763.7136; amd64

```console
$ docker pull nats@sha256:607f6e73ed9007241ff50a84dba439ab79d98a3f3fb47ea3a930f688f67f3088
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2169857611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:597119b40ab372d074effb9f06eec9a9d1a3e9637ac4696ce5f338e8ff4106b3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Sat, 05 Apr 2025 01:48:05 GMT
RUN Install update 10.0.17763.7136
# Wed, 09 Apr 2025 00:59:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Apr 2025 00:59:01 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Apr 2025 00:59:02 GMT
ENV NATS_SERVER=2.11.1
# Wed, 09 Apr 2025 00:59:03 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.1/nats-server-v2.11.1-windows-amd64.zip
# Wed, 09 Apr 2025 00:59:03 GMT
ENV NATS_SERVER_SHASUM=f5594798e1b77013b674c0049070d2502c20ee6f03a04d854cac333e2a21ca20
# Wed, 09 Apr 2025 00:59:40 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Apr 2025 00:59:59 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Apr 2025 00:59:59 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 09 Apr 2025 01:00:00 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Apr 2025 01:00:00 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Apr 2025 01:00:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d949f82a48e7c53af792160596b10005419fbc7ecfed6bc45bbeee3a5a2f07`  
		Last Modified: Tue, 08 Apr 2025 19:58:26 GMT  
		Size: 442.5 MB (442457492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a09300fffebaa4864cab22c763b15a10f2bbf057547b6ff255863442e152d0`  
		Last Modified: Wed, 09 Apr 2025 01:00:09 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21038a6eaee5de691c53f4cf4d271a784a445d934945099069a55d2b2b1a69e9`  
		Last Modified: Wed, 09 Apr 2025 01:00:09 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24942860fb41d5b161011df2cd69c16f7d6847ed7b6db02a33bb64054a72788`  
		Last Modified: Wed, 09 Apr 2025 01:00:07 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e46de18cf6f2c6f8ab7a838c3809a4539af5c48187286fa9e2bba100aed7f0de`  
		Last Modified: Wed, 09 Apr 2025 01:00:07 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d3f59562780344fd3c1ba4f023d776c21499331a904bfcbd4368f20d9da6dab`  
		Last Modified: Wed, 09 Apr 2025 01:00:07 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:795d0c7a551fbfc87a25f38f1a5fa59e2655ca81e62da54e276767f53017edd0`  
		Last Modified: Wed, 09 Apr 2025 01:00:07 GMT  
		Size: 327.2 KB (327167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6cb9f352ed0567a90df0ec2d622906e5d9afe98f400ca192be89a3e899f7d9`  
		Last Modified: Wed, 09 Apr 2025 01:00:07 GMT  
		Size: 6.8 MB (6791732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0f251d7ebfa8a3ecc74f04cf48dbdfb0bbdff942b30e6e4f0d0cbf0f620229`  
		Last Modified: Wed, 09 Apr 2025 01:00:05 GMT  
		Size: 1.9 KB (1934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1994ceebe61f490ae0929761fd777cec24a750b119093e271c15448e6069772e`  
		Last Modified: Wed, 09 Apr 2025 01:00:05 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe64f8769bc81f46b33af77ab80603037a4c694a21ef49ed7c458b22bb1b3e6`  
		Last Modified: Wed, 09 Apr 2025 01:00:05 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca16d5f700915418444888d8391f2ddbdc7a15396a440fbbef200bb6a460b19a`  
		Last Modified: Wed, 09 Apr 2025 01:00:06 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11.1`

```console
$ docker pull nats@sha256:d80d5773c4e558914e79e2886f54a64963d1f07d8638b0c49217cf6fb8e95049
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
	-	windows version 10.0.17763.7009; amd64

### `nats:2.11.1` - linux; amd64

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

### `nats:2.11.1` - unknown; unknown

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

### `nats:2.11.1` - linux; arm variant v6

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

### `nats:2.11.1` - unknown; unknown

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

### `nats:2.11.1` - linux; arm variant v7

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

### `nats:2.11.1` - unknown; unknown

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

### `nats:2.11.1` - linux; arm64 variant v8

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

### `nats:2.11.1` - unknown; unknown

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

### `nats:2.11.1` - linux; ppc64le

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

### `nats:2.11.1` - unknown; unknown

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

### `nats:2.11.1` - linux; s390x

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

### `nats:2.11.1` - unknown; unknown

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

### `nats:2.11.1` - windows version 10.0.17763.7009; amd64

```console
$ docker pull nats@sha256:715ccd4de0bcee69815ad68778b62f6b9373b757afb53337ede87f360c5a010e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113369449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3d563f68baff6d95b9b2b72e3ae34a23681a1a3f2185a8990940cd3a979268a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Tue, 08 Apr 2025 22:13:52 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 08 Apr 2025 22:13:55 GMT
RUN cmd /S /C #(nop) COPY file:eee3870bfbcd9bfddd3622d20a6c2075b583b61ab0944602ceefed02dee11aa2 in C:\nats-server.exe 
# Tue, 08 Apr 2025 22:13:56 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 08 Apr 2025 22:13:57 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 08 Apr 2025 22:13:57 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 08 Apr 2025 22:13:58 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cfa145690c6aebcb679b25530d2fe0c89c7895d522bc2a51865f9318b005b5f`  
		Last Modified: Tue, 08 Apr 2025 22:14:02 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935788f0279b4a2c1b70d0513fd91be7c0c51126d6ea20137c285b06b5bb1f72`  
		Last Modified: Tue, 08 Apr 2025 22:14:02 GMT  
		Size: 6.5 MB (6455907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f144255a54963a1049be6601f86720694f66bb79a738c6f8bd9f1e50cf078872`  
		Last Modified: Tue, 08 Apr 2025 22:14:01 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55833ccd9e0a66322e50524b64d784272932816426d2b868274b94d5eda2b9cb`  
		Last Modified: Tue, 08 Apr 2025 22:14:01 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba94d6c3b308280e6cb389c9f65d5fca970fe7338eb34c025df4d83870244a4`  
		Last Modified: Tue, 08 Apr 2025 22:14:01 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07636e21dc67f902c5b4325c6a45d77f4c0717a519e17f32f1079e8988eb7bbb`  
		Last Modified: Tue, 08 Apr 2025 22:14:01 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11.1-alpine`

```console
$ docker pull nats@sha256:f3d9be9e3809381297c6fc2e1d071bbab2ff25df5fa89e89edbd00fce34f1ca0
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

### `nats:2.11.1-alpine` - linux; amd64

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

### `nats:2.11.1-alpine` - unknown; unknown

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

### `nats:2.11.1-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:33bedd609f7f7f31c7a609239dff642b098d339b2ae5c72f358aca3b0bdfcd99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9830618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f144ccbbca357bd10e864ad6a9469caf63d49af1182de50d7da5e3d4641bcf0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
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
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9048a08e892a91b40d37a992fb9228a855e04b86a0193658785404d407502c36`  
		Last Modified: Tue, 08 Apr 2025 20:28:28 GMT  
		Size: 6.5 MB (6464916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b28e407313ff54262ed40c18741ab1d8d650c46875eb53e1f4dae7a19d64f0`  
		Last Modified: Tue, 08 Apr 2025 20:28:28 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1037b517e6fb05b376c0f845c2de48f91d85acef85548878752fff9e0e5fcb4e`  
		Last Modified: Tue, 08 Apr 2025 20:28:28 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.1-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:f99dfd48fc9fbd2ad2bda5e2128399c2608b793c2df1677489b75ed55c958c80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76d73ac2a38ee74207ea6780edbe4013fa25eafa0ecf5318e88d09592d7da396`

```dockerfile
```

-	Layers:
	-	`sha256:a5c19b7d31f9642dc7ccbb0d73e2008fec7c606c270d5f41a4a1d534c57eb386`  
		Last Modified: Tue, 08 Apr 2025 20:28:27 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.1-alpine` - linux; arm variant v7

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

### `nats:2.11.1-alpine` - unknown; unknown

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

### `nats:2.11.1-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:bc972962a3f6fd357ba4b57dcf878b3c6958fa2fbf75b65bf909c33b47f740e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10234750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:413538651b4a89933595bd87d769140c04c8eae8fac10ef3ff3a2d91bc53712f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
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
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b621e6959e97eb3ca377c901a7c1245231edc4c09198cb628915b5d3e10736c`  
		Last Modified: Tue, 08 Apr 2025 21:41:26 GMT  
		Size: 6.2 MB (6240748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1118a4f264db0d527eda19b814faffbbb61a8097f95ef2157fab3c21c0da752e`  
		Last Modified: Tue, 08 Apr 2025 21:41:25 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd107cb6fb6fc67b6484a7213268c505f995d9ec489e02602183d895d2cf6142`  
		Last Modified: Tue, 08 Apr 2025 21:41:25 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.1-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:dbcfea7b097433117d3ae7e09f5c5824d45dd3d22107d68ef1a2d3080a3742ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43ca0929e9d902e26a1809f5bc3001f3f41b0dc140fd461409cd02b47a6b7219`

```dockerfile
```

-	Layers:
	-	`sha256:6477b5d99ee19ec70115adc1465de3de4a5c61690c1f3f6c597057a749b64c3a`  
		Last Modified: Tue, 08 Apr 2025 21:41:25 GMT  
		Size: 14.5 KB (14468 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.1-alpine` - linux; ppc64le

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

### `nats:2.11.1-alpine` - unknown; unknown

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

### `nats:2.11.1-alpine` - linux; s390x

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

### `nats:2.11.1-alpine` - unknown; unknown

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

## `nats:2.11.1-alpine3.21`

```console
$ docker pull nats@sha256:f3d9be9e3809381297c6fc2e1d071bbab2ff25df5fa89e89edbd00fce34f1ca0
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

### `nats:2.11.1-alpine3.21` - linux; amd64

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

### `nats:2.11.1-alpine3.21` - unknown; unknown

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

### `nats:2.11.1-alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:33bedd609f7f7f31c7a609239dff642b098d339b2ae5c72f358aca3b0bdfcd99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9830618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f144ccbbca357bd10e864ad6a9469caf63d49af1182de50d7da5e3d4641bcf0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
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
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9048a08e892a91b40d37a992fb9228a855e04b86a0193658785404d407502c36`  
		Last Modified: Tue, 08 Apr 2025 20:28:28 GMT  
		Size: 6.5 MB (6464916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b28e407313ff54262ed40c18741ab1d8d650c46875eb53e1f4dae7a19d64f0`  
		Last Modified: Tue, 08 Apr 2025 20:28:28 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1037b517e6fb05b376c0f845c2de48f91d85acef85548878752fff9e0e5fcb4e`  
		Last Modified: Tue, 08 Apr 2025 20:28:28 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.1-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:f99dfd48fc9fbd2ad2bda5e2128399c2608b793c2df1677489b75ed55c958c80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76d73ac2a38ee74207ea6780edbe4013fa25eafa0ecf5318e88d09592d7da396`

```dockerfile
```

-	Layers:
	-	`sha256:a5c19b7d31f9642dc7ccbb0d73e2008fec7c606c270d5f41a4a1d534c57eb386`  
		Last Modified: Tue, 08 Apr 2025 20:28:27 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.1-alpine3.21` - linux; arm variant v7

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

### `nats:2.11.1-alpine3.21` - unknown; unknown

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

### `nats:2.11.1-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:bc972962a3f6fd357ba4b57dcf878b3c6958fa2fbf75b65bf909c33b47f740e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10234750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:413538651b4a89933595bd87d769140c04c8eae8fac10ef3ff3a2d91bc53712f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
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
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b621e6959e97eb3ca377c901a7c1245231edc4c09198cb628915b5d3e10736c`  
		Last Modified: Tue, 08 Apr 2025 21:41:26 GMT  
		Size: 6.2 MB (6240748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1118a4f264db0d527eda19b814faffbbb61a8097f95ef2157fab3c21c0da752e`  
		Last Modified: Tue, 08 Apr 2025 21:41:25 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd107cb6fb6fc67b6484a7213268c505f995d9ec489e02602183d895d2cf6142`  
		Last Modified: Tue, 08 Apr 2025 21:41:25 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.1-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:dbcfea7b097433117d3ae7e09f5c5824d45dd3d22107d68ef1a2d3080a3742ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43ca0929e9d902e26a1809f5bc3001f3f41b0dc140fd461409cd02b47a6b7219`

```dockerfile
```

-	Layers:
	-	`sha256:6477b5d99ee19ec70115adc1465de3de4a5c61690c1f3f6c597057a749b64c3a`  
		Last Modified: Tue, 08 Apr 2025 21:41:25 GMT  
		Size: 14.5 KB (14468 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.1-alpine3.21` - linux; ppc64le

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

### `nats:2.11.1-alpine3.21` - unknown; unknown

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

### `nats:2.11.1-alpine3.21` - linux; s390x

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

### `nats:2.11.1-alpine3.21` - unknown; unknown

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

## `nats:2.11.1-linux`

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

### `nats:2.11.1-linux` - linux; amd64

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

### `nats:2.11.1-linux` - unknown; unknown

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

### `nats:2.11.1-linux` - linux; arm variant v6

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

### `nats:2.11.1-linux` - unknown; unknown

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

### `nats:2.11.1-linux` - linux; arm variant v7

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

### `nats:2.11.1-linux` - unknown; unknown

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

### `nats:2.11.1-linux` - linux; arm64 variant v8

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

### `nats:2.11.1-linux` - unknown; unknown

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

### `nats:2.11.1-linux` - linux; ppc64le

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

### `nats:2.11.1-linux` - unknown; unknown

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

### `nats:2.11.1-linux` - linux; s390x

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

### `nats:2.11.1-linux` - unknown; unknown

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

## `nats:2.11.1-nanoserver`

```console
$ docker pull nats@sha256:abf7e27366b68d9cd2043a5da962739151157116459ae937f689ebaaff08b11a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `nats:2.11.1-nanoserver` - windows version 10.0.17763.7009; amd64

```console
$ docker pull nats@sha256:715ccd4de0bcee69815ad68778b62f6b9373b757afb53337ede87f360c5a010e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113369449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3d563f68baff6d95b9b2b72e3ae34a23681a1a3f2185a8990940cd3a979268a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Tue, 08 Apr 2025 22:13:52 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 08 Apr 2025 22:13:55 GMT
RUN cmd /S /C #(nop) COPY file:eee3870bfbcd9bfddd3622d20a6c2075b583b61ab0944602ceefed02dee11aa2 in C:\nats-server.exe 
# Tue, 08 Apr 2025 22:13:56 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 08 Apr 2025 22:13:57 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 08 Apr 2025 22:13:57 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 08 Apr 2025 22:13:58 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cfa145690c6aebcb679b25530d2fe0c89c7895d522bc2a51865f9318b005b5f`  
		Last Modified: Tue, 08 Apr 2025 22:14:02 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935788f0279b4a2c1b70d0513fd91be7c0c51126d6ea20137c285b06b5bb1f72`  
		Last Modified: Tue, 08 Apr 2025 22:14:02 GMT  
		Size: 6.5 MB (6455907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f144255a54963a1049be6601f86720694f66bb79a738c6f8bd9f1e50cf078872`  
		Last Modified: Tue, 08 Apr 2025 22:14:01 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55833ccd9e0a66322e50524b64d784272932816426d2b868274b94d5eda2b9cb`  
		Last Modified: Tue, 08 Apr 2025 22:14:01 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba94d6c3b308280e6cb389c9f65d5fca970fe7338eb34c025df4d83870244a4`  
		Last Modified: Tue, 08 Apr 2025 22:14:01 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07636e21dc67f902c5b4325c6a45d77f4c0717a519e17f32f1079e8988eb7bbb`  
		Last Modified: Tue, 08 Apr 2025 22:14:01 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11.1-nanoserver-1809`

```console
$ docker pull nats@sha256:abf7e27366b68d9cd2043a5da962739151157116459ae937f689ebaaff08b11a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `nats:2.11.1-nanoserver-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull nats@sha256:715ccd4de0bcee69815ad68778b62f6b9373b757afb53337ede87f360c5a010e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113369449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3d563f68baff6d95b9b2b72e3ae34a23681a1a3f2185a8990940cd3a979268a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Tue, 08 Apr 2025 22:13:52 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 08 Apr 2025 22:13:55 GMT
RUN cmd /S /C #(nop) COPY file:eee3870bfbcd9bfddd3622d20a6c2075b583b61ab0944602ceefed02dee11aa2 in C:\nats-server.exe 
# Tue, 08 Apr 2025 22:13:56 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 08 Apr 2025 22:13:57 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 08 Apr 2025 22:13:57 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 08 Apr 2025 22:13:58 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cfa145690c6aebcb679b25530d2fe0c89c7895d522bc2a51865f9318b005b5f`  
		Last Modified: Tue, 08 Apr 2025 22:14:02 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935788f0279b4a2c1b70d0513fd91be7c0c51126d6ea20137c285b06b5bb1f72`  
		Last Modified: Tue, 08 Apr 2025 22:14:02 GMT  
		Size: 6.5 MB (6455907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f144255a54963a1049be6601f86720694f66bb79a738c6f8bd9f1e50cf078872`  
		Last Modified: Tue, 08 Apr 2025 22:14:01 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55833ccd9e0a66322e50524b64d784272932816426d2b868274b94d5eda2b9cb`  
		Last Modified: Tue, 08 Apr 2025 22:14:01 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba94d6c3b308280e6cb389c9f65d5fca970fe7338eb34c025df4d83870244a4`  
		Last Modified: Tue, 08 Apr 2025 22:14:01 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07636e21dc67f902c5b4325c6a45d77f4c0717a519e17f32f1079e8988eb7bbb`  
		Last Modified: Tue, 08 Apr 2025 22:14:01 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11.1-scratch`

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

### `nats:2.11.1-scratch` - linux; amd64

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

### `nats:2.11.1-scratch` - unknown; unknown

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

### `nats:2.11.1-scratch` - linux; arm variant v6

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

### `nats:2.11.1-scratch` - unknown; unknown

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

### `nats:2.11.1-scratch` - linux; arm variant v7

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

### `nats:2.11.1-scratch` - unknown; unknown

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

### `nats:2.11.1-scratch` - linux; arm64 variant v8

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

### `nats:2.11.1-scratch` - unknown; unknown

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

### `nats:2.11.1-scratch` - linux; ppc64le

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

### `nats:2.11.1-scratch` - unknown; unknown

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

### `nats:2.11.1-scratch` - linux; s390x

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

### `nats:2.11.1-scratch` - unknown; unknown

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

## `nats:2.11.1-windowsservercore`

```console
$ docker pull nats@sha256:d5a5a3214c03e4383b75d3a553d43f1e6966f5e1e2f2fb1f81587381822f7b76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7136; amd64

### `nats:2.11.1-windowsservercore` - windows version 10.0.17763.7136; amd64

```console
$ docker pull nats@sha256:607f6e73ed9007241ff50a84dba439ab79d98a3f3fb47ea3a930f688f67f3088
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2169857611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:597119b40ab372d074effb9f06eec9a9d1a3e9637ac4696ce5f338e8ff4106b3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Sat, 05 Apr 2025 01:48:05 GMT
RUN Install update 10.0.17763.7136
# Wed, 09 Apr 2025 00:59:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Apr 2025 00:59:01 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Apr 2025 00:59:02 GMT
ENV NATS_SERVER=2.11.1
# Wed, 09 Apr 2025 00:59:03 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.1/nats-server-v2.11.1-windows-amd64.zip
# Wed, 09 Apr 2025 00:59:03 GMT
ENV NATS_SERVER_SHASUM=f5594798e1b77013b674c0049070d2502c20ee6f03a04d854cac333e2a21ca20
# Wed, 09 Apr 2025 00:59:40 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Apr 2025 00:59:59 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Apr 2025 00:59:59 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 09 Apr 2025 01:00:00 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Apr 2025 01:00:00 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Apr 2025 01:00:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d949f82a48e7c53af792160596b10005419fbc7ecfed6bc45bbeee3a5a2f07`  
		Last Modified: Tue, 08 Apr 2025 19:58:26 GMT  
		Size: 442.5 MB (442457492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a09300fffebaa4864cab22c763b15a10f2bbf057547b6ff255863442e152d0`  
		Last Modified: Wed, 09 Apr 2025 01:00:09 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21038a6eaee5de691c53f4cf4d271a784a445d934945099069a55d2b2b1a69e9`  
		Last Modified: Wed, 09 Apr 2025 01:00:09 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24942860fb41d5b161011df2cd69c16f7d6847ed7b6db02a33bb64054a72788`  
		Last Modified: Wed, 09 Apr 2025 01:00:07 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e46de18cf6f2c6f8ab7a838c3809a4539af5c48187286fa9e2bba100aed7f0de`  
		Last Modified: Wed, 09 Apr 2025 01:00:07 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d3f59562780344fd3c1ba4f023d776c21499331a904bfcbd4368f20d9da6dab`  
		Last Modified: Wed, 09 Apr 2025 01:00:07 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:795d0c7a551fbfc87a25f38f1a5fa59e2655ca81e62da54e276767f53017edd0`  
		Last Modified: Wed, 09 Apr 2025 01:00:07 GMT  
		Size: 327.2 KB (327167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6cb9f352ed0567a90df0ec2d622906e5d9afe98f400ca192be89a3e899f7d9`  
		Last Modified: Wed, 09 Apr 2025 01:00:07 GMT  
		Size: 6.8 MB (6791732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0f251d7ebfa8a3ecc74f04cf48dbdfb0bbdff942b30e6e4f0d0cbf0f620229`  
		Last Modified: Wed, 09 Apr 2025 01:00:05 GMT  
		Size: 1.9 KB (1934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1994ceebe61f490ae0929761fd777cec24a750b119093e271c15448e6069772e`  
		Last Modified: Wed, 09 Apr 2025 01:00:05 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe64f8769bc81f46b33af77ab80603037a4c694a21ef49ed7c458b22bb1b3e6`  
		Last Modified: Wed, 09 Apr 2025 01:00:05 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca16d5f700915418444888d8391f2ddbdc7a15396a440fbbef200bb6a460b19a`  
		Last Modified: Wed, 09 Apr 2025 01:00:06 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11.1-windowsservercore-1809`

```console
$ docker pull nats@sha256:d5a5a3214c03e4383b75d3a553d43f1e6966f5e1e2f2fb1f81587381822f7b76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7136; amd64

### `nats:2.11.1-windowsservercore-1809` - windows version 10.0.17763.7136; amd64

```console
$ docker pull nats@sha256:607f6e73ed9007241ff50a84dba439ab79d98a3f3fb47ea3a930f688f67f3088
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2169857611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:597119b40ab372d074effb9f06eec9a9d1a3e9637ac4696ce5f338e8ff4106b3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Sat, 05 Apr 2025 01:48:05 GMT
RUN Install update 10.0.17763.7136
# Wed, 09 Apr 2025 00:59:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Apr 2025 00:59:01 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Apr 2025 00:59:02 GMT
ENV NATS_SERVER=2.11.1
# Wed, 09 Apr 2025 00:59:03 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.1/nats-server-v2.11.1-windows-amd64.zip
# Wed, 09 Apr 2025 00:59:03 GMT
ENV NATS_SERVER_SHASUM=f5594798e1b77013b674c0049070d2502c20ee6f03a04d854cac333e2a21ca20
# Wed, 09 Apr 2025 00:59:40 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Apr 2025 00:59:59 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Apr 2025 00:59:59 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 09 Apr 2025 01:00:00 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Apr 2025 01:00:00 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Apr 2025 01:00:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d949f82a48e7c53af792160596b10005419fbc7ecfed6bc45bbeee3a5a2f07`  
		Last Modified: Tue, 08 Apr 2025 19:58:26 GMT  
		Size: 442.5 MB (442457492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a09300fffebaa4864cab22c763b15a10f2bbf057547b6ff255863442e152d0`  
		Last Modified: Wed, 09 Apr 2025 01:00:09 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21038a6eaee5de691c53f4cf4d271a784a445d934945099069a55d2b2b1a69e9`  
		Last Modified: Wed, 09 Apr 2025 01:00:09 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24942860fb41d5b161011df2cd69c16f7d6847ed7b6db02a33bb64054a72788`  
		Last Modified: Wed, 09 Apr 2025 01:00:07 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e46de18cf6f2c6f8ab7a838c3809a4539af5c48187286fa9e2bba100aed7f0de`  
		Last Modified: Wed, 09 Apr 2025 01:00:07 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d3f59562780344fd3c1ba4f023d776c21499331a904bfcbd4368f20d9da6dab`  
		Last Modified: Wed, 09 Apr 2025 01:00:07 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:795d0c7a551fbfc87a25f38f1a5fa59e2655ca81e62da54e276767f53017edd0`  
		Last Modified: Wed, 09 Apr 2025 01:00:07 GMT  
		Size: 327.2 KB (327167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6cb9f352ed0567a90df0ec2d622906e5d9afe98f400ca192be89a3e899f7d9`  
		Last Modified: Wed, 09 Apr 2025 01:00:07 GMT  
		Size: 6.8 MB (6791732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0f251d7ebfa8a3ecc74f04cf48dbdfb0bbdff942b30e6e4f0d0cbf0f620229`  
		Last Modified: Wed, 09 Apr 2025 01:00:05 GMT  
		Size: 1.9 KB (1934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1994ceebe61f490ae0929761fd777cec24a750b119093e271c15448e6069772e`  
		Last Modified: Wed, 09 Apr 2025 01:00:05 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe64f8769bc81f46b33af77ab80603037a4c694a21ef49ed7c458b22bb1b3e6`  
		Last Modified: Wed, 09 Apr 2025 01:00:05 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca16d5f700915418444888d8391f2ddbdc7a15396a440fbbef200bb6a460b19a`  
		Last Modified: Wed, 09 Apr 2025 01:00:06 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:f3d9be9e3809381297c6fc2e1d071bbab2ff25df5fa89e89edbd00fce34f1ca0
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
$ docker pull nats@sha256:33bedd609f7f7f31c7a609239dff642b098d339b2ae5c72f358aca3b0bdfcd99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9830618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f144ccbbca357bd10e864ad6a9469caf63d49af1182de50d7da5e3d4641bcf0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
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
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9048a08e892a91b40d37a992fb9228a855e04b86a0193658785404d407502c36`  
		Last Modified: Tue, 08 Apr 2025 20:28:28 GMT  
		Size: 6.5 MB (6464916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b28e407313ff54262ed40c18741ab1d8d650c46875eb53e1f4dae7a19d64f0`  
		Last Modified: Tue, 08 Apr 2025 20:28:28 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1037b517e6fb05b376c0f845c2de48f91d85acef85548878752fff9e0e5fcb4e`  
		Last Modified: Tue, 08 Apr 2025 20:28:28 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:f99dfd48fc9fbd2ad2bda5e2128399c2608b793c2df1677489b75ed55c958c80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76d73ac2a38ee74207ea6780edbe4013fa25eafa0ecf5318e88d09592d7da396`

```dockerfile
```

-	Layers:
	-	`sha256:a5c19b7d31f9642dc7ccbb0d73e2008fec7c606c270d5f41a4a1d534c57eb386`  
		Last Modified: Tue, 08 Apr 2025 20:28:27 GMT  
		Size: 14.4 KB (14425 bytes)  
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
$ docker pull nats@sha256:bc972962a3f6fd357ba4b57dcf878b3c6958fa2fbf75b65bf909c33b47f740e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10234750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:413538651b4a89933595bd87d769140c04c8eae8fac10ef3ff3a2d91bc53712f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
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
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b621e6959e97eb3ca377c901a7c1245231edc4c09198cb628915b5d3e10736c`  
		Last Modified: Tue, 08 Apr 2025 21:41:26 GMT  
		Size: 6.2 MB (6240748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1118a4f264db0d527eda19b814faffbbb61a8097f95ef2157fab3c21c0da752e`  
		Last Modified: Tue, 08 Apr 2025 21:41:25 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd107cb6fb6fc67b6484a7213268c505f995d9ec489e02602183d895d2cf6142`  
		Last Modified: Tue, 08 Apr 2025 21:41:25 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:dbcfea7b097433117d3ae7e09f5c5824d45dd3d22107d68ef1a2d3080a3742ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43ca0929e9d902e26a1809f5bc3001f3f41b0dc140fd461409cd02b47a6b7219`

```dockerfile
```

-	Layers:
	-	`sha256:6477b5d99ee19ec70115adc1465de3de4a5c61690c1f3f6c597057a749b64c3a`  
		Last Modified: Tue, 08 Apr 2025 21:41:25 GMT  
		Size: 14.5 KB (14468 bytes)  
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
$ docker pull nats@sha256:f3d9be9e3809381297c6fc2e1d071bbab2ff25df5fa89e89edbd00fce34f1ca0
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
$ docker pull nats@sha256:33bedd609f7f7f31c7a609239dff642b098d339b2ae5c72f358aca3b0bdfcd99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9830618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f144ccbbca357bd10e864ad6a9469caf63d49af1182de50d7da5e3d4641bcf0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
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
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9048a08e892a91b40d37a992fb9228a855e04b86a0193658785404d407502c36`  
		Last Modified: Tue, 08 Apr 2025 20:28:28 GMT  
		Size: 6.5 MB (6464916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b28e407313ff54262ed40c18741ab1d8d650c46875eb53e1f4dae7a19d64f0`  
		Last Modified: Tue, 08 Apr 2025 20:28:28 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1037b517e6fb05b376c0f845c2de48f91d85acef85548878752fff9e0e5fcb4e`  
		Last Modified: Tue, 08 Apr 2025 20:28:28 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:f99dfd48fc9fbd2ad2bda5e2128399c2608b793c2df1677489b75ed55c958c80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76d73ac2a38ee74207ea6780edbe4013fa25eafa0ecf5318e88d09592d7da396`

```dockerfile
```

-	Layers:
	-	`sha256:a5c19b7d31f9642dc7ccbb0d73e2008fec7c606c270d5f41a4a1d534c57eb386`  
		Last Modified: Tue, 08 Apr 2025 20:28:27 GMT  
		Size: 14.4 KB (14425 bytes)  
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
$ docker pull nats@sha256:bc972962a3f6fd357ba4b57dcf878b3c6958fa2fbf75b65bf909c33b47f740e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10234750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:413538651b4a89933595bd87d769140c04c8eae8fac10ef3ff3a2d91bc53712f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
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
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b621e6959e97eb3ca377c901a7c1245231edc4c09198cb628915b5d3e10736c`  
		Last Modified: Tue, 08 Apr 2025 21:41:26 GMT  
		Size: 6.2 MB (6240748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1118a4f264db0d527eda19b814faffbbb61a8097f95ef2157fab3c21c0da752e`  
		Last Modified: Tue, 08 Apr 2025 21:41:25 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd107cb6fb6fc67b6484a7213268c505f995d9ec489e02602183d895d2cf6142`  
		Last Modified: Tue, 08 Apr 2025 21:41:25 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:dbcfea7b097433117d3ae7e09f5c5824d45dd3d22107d68ef1a2d3080a3742ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43ca0929e9d902e26a1809f5bc3001f3f41b0dc140fd461409cd02b47a6b7219`

```dockerfile
```

-	Layers:
	-	`sha256:6477b5d99ee19ec70115adc1465de3de4a5c61690c1f3f6c597057a749b64c3a`  
		Last Modified: Tue, 08 Apr 2025 21:41:25 GMT  
		Size: 14.5 KB (14468 bytes)  
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
$ docker pull nats@sha256:d80d5773c4e558914e79e2886f54a64963d1f07d8638b0c49217cf6fb8e95049
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
	-	windows version 10.0.17763.7009; amd64

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

### `nats:latest` - windows version 10.0.17763.7009; amd64

```console
$ docker pull nats@sha256:715ccd4de0bcee69815ad68778b62f6b9373b757afb53337ede87f360c5a010e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113369449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3d563f68baff6d95b9b2b72e3ae34a23681a1a3f2185a8990940cd3a979268a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Tue, 08 Apr 2025 22:13:52 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 08 Apr 2025 22:13:55 GMT
RUN cmd /S /C #(nop) COPY file:eee3870bfbcd9bfddd3622d20a6c2075b583b61ab0944602ceefed02dee11aa2 in C:\nats-server.exe 
# Tue, 08 Apr 2025 22:13:56 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 08 Apr 2025 22:13:57 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 08 Apr 2025 22:13:57 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 08 Apr 2025 22:13:58 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cfa145690c6aebcb679b25530d2fe0c89c7895d522bc2a51865f9318b005b5f`  
		Last Modified: Tue, 08 Apr 2025 22:14:02 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935788f0279b4a2c1b70d0513fd91be7c0c51126d6ea20137c285b06b5bb1f72`  
		Last Modified: Tue, 08 Apr 2025 22:14:02 GMT  
		Size: 6.5 MB (6455907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f144255a54963a1049be6601f86720694f66bb79a738c6f8bd9f1e50cf078872`  
		Last Modified: Tue, 08 Apr 2025 22:14:01 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55833ccd9e0a66322e50524b64d784272932816426d2b868274b94d5eda2b9cb`  
		Last Modified: Tue, 08 Apr 2025 22:14:01 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba94d6c3b308280e6cb389c9f65d5fca970fe7338eb34c025df4d83870244a4`  
		Last Modified: Tue, 08 Apr 2025 22:14:01 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07636e21dc67f902c5b4325c6a45d77f4c0717a519e17f32f1079e8988eb7bbb`  
		Last Modified: Tue, 08 Apr 2025 22:14:01 GMT  
		Size: 1.0 KB (1044 bytes)  
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
$ docker pull nats@sha256:abf7e27366b68d9cd2043a5da962739151157116459ae937f689ebaaff08b11a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `nats:nanoserver` - windows version 10.0.17763.7009; amd64

```console
$ docker pull nats@sha256:715ccd4de0bcee69815ad68778b62f6b9373b757afb53337ede87f360c5a010e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113369449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3d563f68baff6d95b9b2b72e3ae34a23681a1a3f2185a8990940cd3a979268a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Tue, 08 Apr 2025 22:13:52 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 08 Apr 2025 22:13:55 GMT
RUN cmd /S /C #(nop) COPY file:eee3870bfbcd9bfddd3622d20a6c2075b583b61ab0944602ceefed02dee11aa2 in C:\nats-server.exe 
# Tue, 08 Apr 2025 22:13:56 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 08 Apr 2025 22:13:57 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 08 Apr 2025 22:13:57 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 08 Apr 2025 22:13:58 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cfa145690c6aebcb679b25530d2fe0c89c7895d522bc2a51865f9318b005b5f`  
		Last Modified: Tue, 08 Apr 2025 22:14:02 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935788f0279b4a2c1b70d0513fd91be7c0c51126d6ea20137c285b06b5bb1f72`  
		Last Modified: Tue, 08 Apr 2025 22:14:02 GMT  
		Size: 6.5 MB (6455907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f144255a54963a1049be6601f86720694f66bb79a738c6f8bd9f1e50cf078872`  
		Last Modified: Tue, 08 Apr 2025 22:14:01 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55833ccd9e0a66322e50524b64d784272932816426d2b868274b94d5eda2b9cb`  
		Last Modified: Tue, 08 Apr 2025 22:14:01 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba94d6c3b308280e6cb389c9f65d5fca970fe7338eb34c025df4d83870244a4`  
		Last Modified: Tue, 08 Apr 2025 22:14:01 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07636e21dc67f902c5b4325c6a45d77f4c0717a519e17f32f1079e8988eb7bbb`  
		Last Modified: Tue, 08 Apr 2025 22:14:01 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:abf7e27366b68d9cd2043a5da962739151157116459ae937f689ebaaff08b11a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull nats@sha256:715ccd4de0bcee69815ad68778b62f6b9373b757afb53337ede87f360c5a010e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113369449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3d563f68baff6d95b9b2b72e3ae34a23681a1a3f2185a8990940cd3a979268a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Tue, 08 Apr 2025 22:13:52 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 08 Apr 2025 22:13:55 GMT
RUN cmd /S /C #(nop) COPY file:eee3870bfbcd9bfddd3622d20a6c2075b583b61ab0944602ceefed02dee11aa2 in C:\nats-server.exe 
# Tue, 08 Apr 2025 22:13:56 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 08 Apr 2025 22:13:57 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 08 Apr 2025 22:13:57 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 08 Apr 2025 22:13:58 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cfa145690c6aebcb679b25530d2fe0c89c7895d522bc2a51865f9318b005b5f`  
		Last Modified: Tue, 08 Apr 2025 22:14:02 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935788f0279b4a2c1b70d0513fd91be7c0c51126d6ea20137c285b06b5bb1f72`  
		Last Modified: Tue, 08 Apr 2025 22:14:02 GMT  
		Size: 6.5 MB (6455907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f144255a54963a1049be6601f86720694f66bb79a738c6f8bd9f1e50cf078872`  
		Last Modified: Tue, 08 Apr 2025 22:14:01 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55833ccd9e0a66322e50524b64d784272932816426d2b868274b94d5eda2b9cb`  
		Last Modified: Tue, 08 Apr 2025 22:14:01 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba94d6c3b308280e6cb389c9f65d5fca970fe7338eb34c025df4d83870244a4`  
		Last Modified: Tue, 08 Apr 2025 22:14:01 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07636e21dc67f902c5b4325c6a45d77f4c0717a519e17f32f1079e8988eb7bbb`  
		Last Modified: Tue, 08 Apr 2025 22:14:01 GMT  
		Size: 1.0 KB (1044 bytes)  
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
$ docker pull nats@sha256:d5a5a3214c03e4383b75d3a553d43f1e6966f5e1e2f2fb1f81587381822f7b76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7136; amd64

### `nats:windowsservercore` - windows version 10.0.17763.7136; amd64

```console
$ docker pull nats@sha256:607f6e73ed9007241ff50a84dba439ab79d98a3f3fb47ea3a930f688f67f3088
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2169857611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:597119b40ab372d074effb9f06eec9a9d1a3e9637ac4696ce5f338e8ff4106b3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Sat, 05 Apr 2025 01:48:05 GMT
RUN Install update 10.0.17763.7136
# Wed, 09 Apr 2025 00:59:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Apr 2025 00:59:01 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Apr 2025 00:59:02 GMT
ENV NATS_SERVER=2.11.1
# Wed, 09 Apr 2025 00:59:03 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.1/nats-server-v2.11.1-windows-amd64.zip
# Wed, 09 Apr 2025 00:59:03 GMT
ENV NATS_SERVER_SHASUM=f5594798e1b77013b674c0049070d2502c20ee6f03a04d854cac333e2a21ca20
# Wed, 09 Apr 2025 00:59:40 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Apr 2025 00:59:59 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Apr 2025 00:59:59 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 09 Apr 2025 01:00:00 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Apr 2025 01:00:00 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Apr 2025 01:00:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d949f82a48e7c53af792160596b10005419fbc7ecfed6bc45bbeee3a5a2f07`  
		Last Modified: Tue, 08 Apr 2025 19:58:26 GMT  
		Size: 442.5 MB (442457492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a09300fffebaa4864cab22c763b15a10f2bbf057547b6ff255863442e152d0`  
		Last Modified: Wed, 09 Apr 2025 01:00:09 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21038a6eaee5de691c53f4cf4d271a784a445d934945099069a55d2b2b1a69e9`  
		Last Modified: Wed, 09 Apr 2025 01:00:09 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24942860fb41d5b161011df2cd69c16f7d6847ed7b6db02a33bb64054a72788`  
		Last Modified: Wed, 09 Apr 2025 01:00:07 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e46de18cf6f2c6f8ab7a838c3809a4539af5c48187286fa9e2bba100aed7f0de`  
		Last Modified: Wed, 09 Apr 2025 01:00:07 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d3f59562780344fd3c1ba4f023d776c21499331a904bfcbd4368f20d9da6dab`  
		Last Modified: Wed, 09 Apr 2025 01:00:07 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:795d0c7a551fbfc87a25f38f1a5fa59e2655ca81e62da54e276767f53017edd0`  
		Last Modified: Wed, 09 Apr 2025 01:00:07 GMT  
		Size: 327.2 KB (327167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6cb9f352ed0567a90df0ec2d622906e5d9afe98f400ca192be89a3e899f7d9`  
		Last Modified: Wed, 09 Apr 2025 01:00:07 GMT  
		Size: 6.8 MB (6791732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0f251d7ebfa8a3ecc74f04cf48dbdfb0bbdff942b30e6e4f0d0cbf0f620229`  
		Last Modified: Wed, 09 Apr 2025 01:00:05 GMT  
		Size: 1.9 KB (1934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1994ceebe61f490ae0929761fd777cec24a750b119093e271c15448e6069772e`  
		Last Modified: Wed, 09 Apr 2025 01:00:05 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe64f8769bc81f46b33af77ab80603037a4c694a21ef49ed7c458b22bb1b3e6`  
		Last Modified: Wed, 09 Apr 2025 01:00:05 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca16d5f700915418444888d8391f2ddbdc7a15396a440fbbef200bb6a460b19a`  
		Last Modified: Wed, 09 Apr 2025 01:00:06 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:d5a5a3214c03e4383b75d3a553d43f1e6966f5e1e2f2fb1f81587381822f7b76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7136; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.7136; amd64

```console
$ docker pull nats@sha256:607f6e73ed9007241ff50a84dba439ab79d98a3f3fb47ea3a930f688f67f3088
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2169857611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:597119b40ab372d074effb9f06eec9a9d1a3e9637ac4696ce5f338e8ff4106b3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Sat, 05 Apr 2025 01:48:05 GMT
RUN Install update 10.0.17763.7136
# Wed, 09 Apr 2025 00:59:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Apr 2025 00:59:01 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Apr 2025 00:59:02 GMT
ENV NATS_SERVER=2.11.1
# Wed, 09 Apr 2025 00:59:03 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.1/nats-server-v2.11.1-windows-amd64.zip
# Wed, 09 Apr 2025 00:59:03 GMT
ENV NATS_SERVER_SHASUM=f5594798e1b77013b674c0049070d2502c20ee6f03a04d854cac333e2a21ca20
# Wed, 09 Apr 2025 00:59:40 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Apr 2025 00:59:59 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Apr 2025 00:59:59 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 09 Apr 2025 01:00:00 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Apr 2025 01:00:00 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Apr 2025 01:00:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d949f82a48e7c53af792160596b10005419fbc7ecfed6bc45bbeee3a5a2f07`  
		Last Modified: Tue, 08 Apr 2025 19:58:26 GMT  
		Size: 442.5 MB (442457492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a09300fffebaa4864cab22c763b15a10f2bbf057547b6ff255863442e152d0`  
		Last Modified: Wed, 09 Apr 2025 01:00:09 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21038a6eaee5de691c53f4cf4d271a784a445d934945099069a55d2b2b1a69e9`  
		Last Modified: Wed, 09 Apr 2025 01:00:09 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24942860fb41d5b161011df2cd69c16f7d6847ed7b6db02a33bb64054a72788`  
		Last Modified: Wed, 09 Apr 2025 01:00:07 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e46de18cf6f2c6f8ab7a838c3809a4539af5c48187286fa9e2bba100aed7f0de`  
		Last Modified: Wed, 09 Apr 2025 01:00:07 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d3f59562780344fd3c1ba4f023d776c21499331a904bfcbd4368f20d9da6dab`  
		Last Modified: Wed, 09 Apr 2025 01:00:07 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:795d0c7a551fbfc87a25f38f1a5fa59e2655ca81e62da54e276767f53017edd0`  
		Last Modified: Wed, 09 Apr 2025 01:00:07 GMT  
		Size: 327.2 KB (327167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6cb9f352ed0567a90df0ec2d622906e5d9afe98f400ca192be89a3e899f7d9`  
		Last Modified: Wed, 09 Apr 2025 01:00:07 GMT  
		Size: 6.8 MB (6791732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0f251d7ebfa8a3ecc74f04cf48dbdfb0bbdff942b30e6e4f0d0cbf0f620229`  
		Last Modified: Wed, 09 Apr 2025 01:00:05 GMT  
		Size: 1.9 KB (1934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1994ceebe61f490ae0929761fd777cec24a750b119093e271c15448e6069772e`  
		Last Modified: Wed, 09 Apr 2025 01:00:05 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe64f8769bc81f46b33af77ab80603037a4c694a21ef49ed7c458b22bb1b3e6`  
		Last Modified: Wed, 09 Apr 2025 01:00:05 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca16d5f700915418444888d8391f2ddbdc7a15396a440fbbef200bb6a460b19a`  
		Last Modified: Wed, 09 Apr 2025 01:00:06 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
