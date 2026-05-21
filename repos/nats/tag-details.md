<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats`

-	[`nats:2`](#nats2)
-	[`nats:2-alpine`](#nats2-alpine)
-	[`nats:2-alpine3.22`](#nats2-alpine322)
-	[`nats:2-linux`](#nats2-linux)
-	[`nats:2-nanoserver`](#nats2-nanoserver)
-	[`nats:2-nanoserver-ltsc2022`](#nats2-nanoserver-ltsc2022)
-	[`nats:2-scratch`](#nats2-scratch)
-	[`nats:2-windowsservercore`](#nats2-windowsservercore)
-	[`nats:2-windowsservercore-ltsc2022`](#nats2-windowsservercore-ltsc2022)
-	[`nats:2.12`](#nats212)
-	[`nats:2.12-alpine`](#nats212-alpine)
-	[`nats:2.12-alpine3.22`](#nats212-alpine322)
-	[`nats:2.12-linux`](#nats212-linux)
-	[`nats:2.12-nanoserver`](#nats212-nanoserver)
-	[`nats:2.12-nanoserver-ltsc2022`](#nats212-nanoserver-ltsc2022)
-	[`nats:2.12-scratch`](#nats212-scratch)
-	[`nats:2.12-windowsservercore`](#nats212-windowsservercore)
-	[`nats:2.12-windowsservercore-ltsc2022`](#nats212-windowsservercore-ltsc2022)
-	[`nats:2.12.9`](#nats2129)
-	[`nats:2.12.9-alpine`](#nats2129-alpine)
-	[`nats:2.12.9-alpine3.22`](#nats2129-alpine322)
-	[`nats:2.12.9-linux`](#nats2129-linux)
-	[`nats:2.12.9-nanoserver`](#nats2129-nanoserver)
-	[`nats:2.12.9-nanoserver-ltsc2022`](#nats2129-nanoserver-ltsc2022)
-	[`nats:2.12.9-scratch`](#nats2129-scratch)
-	[`nats:2.12.9-windowsservercore`](#nats2129-windowsservercore)
-	[`nats:2.12.9-windowsservercore-ltsc2022`](#nats2129-windowsservercore-ltsc2022)
-	[`nats:2.14`](#nats214)
-	[`nats:2.14-alpine`](#nats214-alpine)
-	[`nats:2.14-alpine3.22`](#nats214-alpine322)
-	[`nats:2.14-linux`](#nats214-linux)
-	[`nats:2.14-nanoserver`](#nats214-nanoserver)
-	[`nats:2.14-nanoserver-ltsc2022`](#nats214-nanoserver-ltsc2022)
-	[`nats:2.14-scratch`](#nats214-scratch)
-	[`nats:2.14-windowsservercore`](#nats214-windowsservercore)
-	[`nats:2.14-windowsservercore-ltsc2022`](#nats214-windowsservercore-ltsc2022)
-	[`nats:2.14.1`](#nats2141)
-	[`nats:2.14.1-alpine`](#nats2141-alpine)
-	[`nats:2.14.1-alpine3.22`](#nats2141-alpine322)
-	[`nats:2.14.1-linux`](#nats2141-linux)
-	[`nats:2.14.1-nanoserver`](#nats2141-nanoserver)
-	[`nats:2.14.1-nanoserver-ltsc2022`](#nats2141-nanoserver-ltsc2022)
-	[`nats:2.14.1-scratch`](#nats2141-scratch)
-	[`nats:2.14.1-windowsservercore`](#nats2141-windowsservercore)
-	[`nats:2.14.1-windowsservercore-ltsc2022`](#nats2141-windowsservercore-ltsc2022)
-	[`nats:alpine`](#natsalpine)
-	[`nats:alpine3.22`](#natsalpine322)
-	[`nats:latest`](#natslatest)
-	[`nats:linux`](#natslinux)
-	[`nats:nanoserver`](#natsnanoserver)
-	[`nats:nanoserver-ltsc2022`](#natsnanoserver-ltsc2022)
-	[`nats:scratch`](#natsscratch)
-	[`nats:windowsservercore`](#natswindowsservercore)
-	[`nats:windowsservercore-ltsc2022`](#natswindowsservercore-ltsc2022)

## `nats:2`

```console
$ docker pull nats@sha256:7f430e429d0a90444b38bd40ab7812fd3afcc49a51f6b03a931f9becd5aeb280
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
	-	windows version 10.0.20348.5139; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:aad7f400fa8a1cbcc2f818d5373638f91cfbfcac7cb9bd28fe6e8538c08b9c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6838210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39f65eeb0573eea876a604f186453a7a3cda0c8c511dd143432e1128e07a8734`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:10:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:10:38 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:10:38 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:10:38 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:10:38 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:10:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:05832d0be2949ff52eaf08a260411f3a4a020a066de4aa19dc62284052758304`  
		Last Modified: Wed, 20 May 2026 16:04:06 GMT  
		Size: 6.8 MB (6837703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a284b9b8e39214498d13f3dca35a9c9e81d34b69635ed74a3d47d26e45d5591`  
		Last Modified: Wed, 20 May 2026 19:10:42 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:6b2a0558891216e6e12622ac66d8766987858f507eee4cb4cfef25a0b1480e84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a061861dcdd34e8079637906d854df58e3e30fcfb0514aa93b4a1ada5b3936b9`

```dockerfile
```

-	Layers:
	-	`sha256:7fff463e51e2de542cc152e5196125c500561d37a866a78ab756f40188e25be6`  
		Last Modified: Wed, 20 May 2026 19:10:42 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:80f40fb067456022353b1754a4c58f49b1af454522a8af74e9c270e3a27668d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6573757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:039a8f82177ac58ba3952b7b25d8af7b14d0fbcf08e6e53efbab9e028b515cb5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:09:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:09:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:09:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:09:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:09:27 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:09:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3f675bd99a02bdb97f8ad1545908545b1e797e40d8038ce181205b0808044e20`  
		Last Modified: Wed, 20 May 2026 16:04:08 GMT  
		Size: 6.6 MB (6573248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715581626472620cc372593ae38a74d6c85239c0282bc3c5b7937fcd525bb308`  
		Last Modified: Wed, 20 May 2026 19:09:32 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:cd80c2a5593667a467031df5e49c9cab2cc1f5ae03e981c4789d7a262cbded23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac98f8edc0ec201da45e4d96bc1ea96d553e89648a61e35f8a195d38ce81d6b9`

```dockerfile
```

-	Layers:
	-	`sha256:d7cd588a4563631d4b86b381c7ee1c56114f94b80568f0e8defc278961b4c119`  
		Last Modified: Wed, 20 May 2026 19:09:31 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:ae43b4e3d705ed3a3386e6b303d8dfb011fec9e1cdf8523ff9c6387935d9652d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6565185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a493ff1dda3a5eb2f84019be4a31029f9463e5a91f142d91cbd96345245eadb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:09:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:09:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:09:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:09:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:09:01 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:09:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:07a4ad6a636748b056dca5d82613a936ff1872d9092911832cea1178d840cb7f`  
		Last Modified: Wed, 20 May 2026 16:04:08 GMT  
		Size: 6.6 MB (6564678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95ec1a5b2af5f3d81a39b2563595f7008790713449f52e148c254bc7d0be80e`  
		Last Modified: Wed, 20 May 2026 19:09:06 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:5b515d7d9aa87098056bad17534ca266bba383a9a52d362a1788c5ac7b596d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a1b7811acc104229e8cc148ff624e24efc4e31d06fce27cdd9091dd3237110`

```dockerfile
```

-	Layers:
	-	`sha256:e855458d7f5e87be1456ba294fc7386adaa0241520ff73ab4b95b94271f3d0a0`  
		Last Modified: Wed, 20 May 2026 19:09:05 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:89ea5f3d1a4e7db9650685b4b60d5f2340f6edd89f0d2a7a6f2a5cb9b6f144c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6189602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:080d11e023e3c9bc77bc5d6e137c30fcee2ca537fbda1d730ee0de9b5131cf97`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:10:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:10:02 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:10:02 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:10:02 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:10:02 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:10:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5f2fe2216ecafda68f73a81334875cb85722e57f12bc2af372cc03c4952017ff`  
		Last Modified: Wed, 20 May 2026 16:04:06 GMT  
		Size: 6.2 MB (6189094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f13aa02931bd62f5d9ce1935b8f163c6fcb3db670a4893037e6326c70ff971`  
		Last Modified: Wed, 20 May 2026 19:10:07 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:55f5544491f15bb813013ec1a1698f6e7e6f1ebbf96b4e49dba94dab9c27b313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30316b20c5d7aabdc5ded4b132f0725f10bdb7bd31bfbdb309184a8e58efe00c`

```dockerfile
```

-	Layers:
	-	`sha256:e06f44f5e5db93fe4fba02df22b44d37f71209d0cfbcbcec67b2ec6687bda27c`  
		Last Modified: Wed, 20 May 2026 19:10:07 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; ppc64le

```console
$ docker pull nats@sha256:9b9d19890e9399f86300407959de41b794ee8fd1b46720c7548163f7f94fd15e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6254150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dcae0dec9d781a4ed3bd8282b836bb0fc168482d57def8fec57c690ecdd111a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:09:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:09:00 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:09:00 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:09:00 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:09:00 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:09:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:eeebf06eacfa887b3524b3c76a2593bb68e43a09aa8ff01b5a09c0ce44ed2917`  
		Last Modified: Wed, 20 May 2026 16:04:05 GMT  
		Size: 6.3 MB (6253641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb234fae2f8c35c37c5a0a2b27b551816540b8c513f6b2c479728b77a462cc5`  
		Last Modified: Wed, 20 May 2026 19:09:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:44cc5336af1db8f2f590eca54680623452cbb2da64b65bb690521c087a9be389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2bccd9ad485d0016ce5f53e02daf116336befd19e206a354f9324e36b86c720`

```dockerfile
```

-	Layers:
	-	`sha256:33b891cec5ef0cfb52212abc7e2148afd94f43e4c045f9b8ee11b24532349469`  
		Last Modified: Wed, 20 May 2026 19:09:06 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; s390x

```console
$ docker pull nats@sha256:02ac81902397bc3ce3ae4f6bf57bb15925e02525fc49567e8db5747ae9e3cc7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6650240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f5f893e9ed2e5671b5afc696c46fd6aa4099811ef87a81fb46e2bf0c84ba84f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:10:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:10:22 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:10:24 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:10:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:10:24 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:10:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9e00525b36acc41f758b0363af2261253b6d35899fd8e6c7e6b4d30ff05eab43`  
		Last Modified: Wed, 20 May 2026 16:04:08 GMT  
		Size: 6.6 MB (6649731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61970d60cef7c5abc0f2985fb3486911eb5ae086553cd2bfb895dd97daa5dbe1`  
		Last Modified: Wed, 20 May 2026 19:10:43 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:91a6b246de893cdf55e56ebb0f717eb35cb29121fd44454bb5c2e66fe76ba11b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b822bf8bf39b54c102cf252c8b091bac1a2c642851dd34cc7445f10b19fbbe42`

```dockerfile
```

-	Layers:
	-	`sha256:a39452d35088530375cff827daeae3695859d1f87479bba2523d135b3256d905`  
		Last Modified: Wed, 20 May 2026 19:10:43 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:ad04df86864a0653927e5ff2293212d694588db88edc746ce8b917417317c0f3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134078105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc7e5bd03f66dabebd5917cf13f4067081477a5934e86d07357d04db10e33ec4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 20 May 2026 19:09:14 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 20 May 2026 19:09:15 GMT
RUN cmd /S /C #(nop) COPY file:5d608f6a5cbf80544d196a9ac38d66b2635084a5e0a392611785993205e5329d in C:\nats-server.exe 
# Wed, 20 May 2026 19:09:16 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 20 May 2026 19:09:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 20 May 2026 19:09:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 20 May 2026 19:09:18 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c815e3255991cc2df065c98a27664be46d8b5db04231449f637ecaf64c5c098f`  
		Last Modified: Wed, 20 May 2026 19:09:24 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68983020294e3083531b7192194e9d5172d2a1449eac04682b7544bb139048b5`  
		Last Modified: Wed, 20 May 2026 19:09:27 GMT  
		Size: 7.0 MB (7033380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730756958a80b0245caf373feb8024993ecef9e67a8ade759511f66d001f3f07`  
		Last Modified: Wed, 20 May 2026 19:09:22 GMT  
		Size: 1.7 KB (1672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ec9d4f153ff90a362ff5591192559ff2e3584441d0bee4e4fdd8b0a4845b833`  
		Last Modified: Wed, 20 May 2026 19:09:22 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb6e35267fc994af8eab6412783ba571dd4c1d14e5fa8771f50a386e61ef655`  
		Last Modified: Wed, 20 May 2026 19:09:22 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838e55b2d659c4cc5f4e0db1773fbe38aa8487984688f5a0f60b202907588e42`  
		Last Modified: Wed, 20 May 2026 19:09:22 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:ea17b9b7f74279b9239cf65e5786c0133e9a7c353bf218d29004abf2e7a33181
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
$ docker pull nats@sha256:4c516667ffae4977a0b4ee1d8caa5b663a0d147b66c6b2adc8ee8f3e23728bc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11103220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c133130b2f2f46568f11546ffef920fccb739e99fd733ef11ea43fc1737887c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:37:17 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:37:17 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:37:17 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:37:17 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:37:17 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:37:17 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:37:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:37:17 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6887181943c337b002058eb52d1b08afbc55add7c29a34ac80e3949090e15495`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 7.3 MB (7294060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a070bfd7422a373dc1b206300e1798aef404bf1bac5a04a3293b33f5468a167e`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4a08ddee9fc679f6a40d1ca0c325ec632bebcbb19437245764df5d7ccb6e0d`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:16deabb6f9a013834b95f04987ebab3d889f6704db15b71e13e10a4109b2e5b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d0fdb19df33d866a3c0b19c2d8aa933518ea4afc5b2f7562f2fd9364bb805ec`

```dockerfile
```

-	Layers:
	-	`sha256:650380b0910269f4395d628fbfafe98d4c910cc7a775ff48fa5093aaddc18b1f`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 15.4 KB (15403 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:32e7eb3bde61b1a81ba030cf21530f82b3713f20585f14da348ed9ff0099cd38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10540472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff1b400cc41fb9599883d47ee0cc98f26d14432cafaa79d7b00c36500c3be581`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:35:40 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:35:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:35:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:35:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac441e30d31da40cce92ca13be29a2ec33b8e530c12f39c4e6e6f821d36fa5f7`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 7.0 MB (7032117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588069c44453627769cbea386971dc510fa0a2a33fc33bc21795cbe4c6ceeb2e`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1efc9734efaa0feb255b7c30b046fb56094635c7d947db2f21f7a873a06b52a`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:e8fdb1f5ad9c517ef1795cc413d10f4304bac0bfacca20197b1324ceed658bd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67da2ba5e6d5168c0687521d71e8357c05504026864365687620573485a04e0`

```dockerfile
```

-	Layers:
	-	`sha256:63de3f19bc13cbd3dc2f28506681e74ef898d6cddd4ed65551521f9d641ff6b5`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:8805cf2aaa214d58393f7373011c4fe330f5225fb9bc4da6d715a6ab72ff8dc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10246493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32278cb7a1bf5e3ea24f7381d52c844e152750efbf7684af40245538a2fadaa4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:35:40 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:35:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:35:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:35:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3e43a7f3a2149acbd98329815e7e03d9dcf933d2131db6f8e1eecd1c01e173`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 7.0 MB (7019690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588069c44453627769cbea386971dc510fa0a2a33fc33bc21795cbe4c6ceeb2e`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9213cf8ea08c3ce1080672b9ea4c12034482854a1829a814ec22933ea91379a0`  
		Last Modified: Wed, 20 May 2026 18:35:44 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:83439ca6685120afbf799cb62bebb64b76d3419bd2523ae781dfad0b8bd8db9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f56fa87064674ea90080bd544ca88fd1b1f257088b93998a8cd46405b6249c`

```dockerfile
```

-	Layers:
	-	`sha256:22deddd2f98e84c9bc37c96058b3e88416465a5ea1004b4985cef2385de5a8be`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 15.5 KB (15515 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:abc668a25359714d7320be16684a7a6096d82a6d41aa9fbb4275c02f3fb1e716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10791094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c04c7a60cc127abb4b03f7f7593fb48cd0124f4f2cd959996fdcb5caba71e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:37:01 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:37:01 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:37:01 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:37:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:37:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:37:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:37:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:37:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b89c7be0c2d2557967711fd66cb73b3b64361381d066e02f0b52b2abeedd6b9`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 6.6 MB (6648233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b1bf5ee681da0d7929bf7d0e36bf5d24df48f214a25c32a7692f9fd0bc5eab`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2e67e1deca529e76612c525c5a8e12050d9ec84c3691673953e51573c1e653`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:5ae7b0317944de344d87247e9cb05a11dcd4f796e1800294193d7b60f43c9d9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9059f595926bbcc76e88f995c69a532e5bfdb37e53db7d9cbd26077b9a0f52d1`

```dockerfile
```

-	Layers:
	-	`sha256:a10a07e60572ceb3113b276c9a02c5aa46bf940b8f2a491e7064608fcac2409c`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:7c13d10c1f7169aaedc2ac8ecbc1f431dda7e906455b836d09a14b3b948f3036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10448793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa266dd5df001f7f566ffb0c8c8acff2de160efa06508788758a4e3022c8e98d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:39:54 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:39:54 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:39:54 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:39:55 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:39:55 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:39:55 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:39:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:39:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efe06b0c545d8e510a8131fe2984aa46a7c4d7502148ce8f2e94df5ffeed78f`  
		Last Modified: Wed, 20 May 2026 18:40:02 GMT  
		Size: 6.7 MB (6711165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3c6e5710602d0c65abfcc3a4aac8676e3cd1f849d5967bee0654b0ec045abe`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0fcc4ed5f0f4848feb91f0e5c409cb87bfd693a7056f2c0e574dbf0fc8ff4ab`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:7878f9d371c5d9227beef40f16b5dfd6d37465bab0104f835171af841d4c4a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47a1ee27b4ce5d60016cbff052995f2dbab1c7c6c61dcf79e2f75cbb1430fbad`

```dockerfile
```

-	Layers:
	-	`sha256:c27fc7351e2a880436edb13f3b1eaf0c5d83b4ec4a761386db3f8a0e0e8642a5`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; s390x

```console
$ docker pull nats@sha256:458d20eff2bdbc011304724399fc06b3db7dae7c95d0c806969fc503389a70c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10757148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0002a7df6776ecf8e0df1b73510a6014c1f519a3c9692cd787d8568dd8021d99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:48:37 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:48:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:48:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:48:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:48:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:48:43 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:48:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:48:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728aea4976117b7918cb9446c013c273cae16aa21337089d91cbd93761d10ae5`  
		Last Modified: Wed, 20 May 2026 18:49:10 GMT  
		Size: 7.1 MB (7102303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e102ba28952cc8bf83cffaefb3ec4b38d56cd736120ece8c71362ff603fd09b`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec22f8c91bd1e1b2e7f49773754ab16299137dd3226c8bb660a538d249364ae6`  
		Last Modified: Wed, 20 May 2026 18:49:08 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:38a69833b514d10d0b925fa5c4639cb5d17abe985f2b30699a0f305324397aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cffc57189208991582e7a0262e60b1415e19ac3919981144973c3d19428e23f6`

```dockerfile
```

-	Layers:
	-	`sha256:ccc40928ae38a1bd914e972d9acbe81dbc2e36b6132cee1761b8e20e7dda2db5`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-alpine3.22`

```console
$ docker pull nats@sha256:ea17b9b7f74279b9239cf65e5786c0133e9a7c353bf218d29004abf2e7a33181
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

### `nats:2-alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:4c516667ffae4977a0b4ee1d8caa5b663a0d147b66c6b2adc8ee8f3e23728bc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11103220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c133130b2f2f46568f11546ffef920fccb739e99fd733ef11ea43fc1737887c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:37:17 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:37:17 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:37:17 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:37:17 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:37:17 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:37:17 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:37:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:37:17 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6887181943c337b002058eb52d1b08afbc55add7c29a34ac80e3949090e15495`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 7.3 MB (7294060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a070bfd7422a373dc1b206300e1798aef404bf1bac5a04a3293b33f5468a167e`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4a08ddee9fc679f6a40d1ca0c325ec632bebcbb19437245764df5d7ccb6e0d`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:16deabb6f9a013834b95f04987ebab3d889f6704db15b71e13e10a4109b2e5b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d0fdb19df33d866a3c0b19c2d8aa933518ea4afc5b2f7562f2fd9364bb805ec`

```dockerfile
```

-	Layers:
	-	`sha256:650380b0910269f4395d628fbfafe98d4c910cc7a775ff48fa5093aaddc18b1f`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 15.4 KB (15403 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:32e7eb3bde61b1a81ba030cf21530f82b3713f20585f14da348ed9ff0099cd38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10540472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff1b400cc41fb9599883d47ee0cc98f26d14432cafaa79d7b00c36500c3be581`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:35:40 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:35:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:35:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:35:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac441e30d31da40cce92ca13be29a2ec33b8e530c12f39c4e6e6f821d36fa5f7`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 7.0 MB (7032117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588069c44453627769cbea386971dc510fa0a2a33fc33bc21795cbe4c6ceeb2e`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1efc9734efaa0feb255b7c30b046fb56094635c7d947db2f21f7a873a06b52a`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:e8fdb1f5ad9c517ef1795cc413d10f4304bac0bfacca20197b1324ceed658bd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67da2ba5e6d5168c0687521d71e8357c05504026864365687620573485a04e0`

```dockerfile
```

-	Layers:
	-	`sha256:63de3f19bc13cbd3dc2f28506681e74ef898d6cddd4ed65551521f9d641ff6b5`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:8805cf2aaa214d58393f7373011c4fe330f5225fb9bc4da6d715a6ab72ff8dc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10246493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32278cb7a1bf5e3ea24f7381d52c844e152750efbf7684af40245538a2fadaa4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:35:40 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:35:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:35:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:35:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3e43a7f3a2149acbd98329815e7e03d9dcf933d2131db6f8e1eecd1c01e173`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 7.0 MB (7019690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588069c44453627769cbea386971dc510fa0a2a33fc33bc21795cbe4c6ceeb2e`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9213cf8ea08c3ce1080672b9ea4c12034482854a1829a814ec22933ea91379a0`  
		Last Modified: Wed, 20 May 2026 18:35:44 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:83439ca6685120afbf799cb62bebb64b76d3419bd2523ae781dfad0b8bd8db9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f56fa87064674ea90080bd544ca88fd1b1f257088b93998a8cd46405b6249c`

```dockerfile
```

-	Layers:
	-	`sha256:22deddd2f98e84c9bc37c96058b3e88416465a5ea1004b4985cef2385de5a8be`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 15.5 KB (15515 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:abc668a25359714d7320be16684a7a6096d82a6d41aa9fbb4275c02f3fb1e716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10791094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c04c7a60cc127abb4b03f7f7593fb48cd0124f4f2cd959996fdcb5caba71e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:37:01 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:37:01 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:37:01 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:37:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:37:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:37:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:37:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:37:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b89c7be0c2d2557967711fd66cb73b3b64361381d066e02f0b52b2abeedd6b9`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 6.6 MB (6648233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b1bf5ee681da0d7929bf7d0e36bf5d24df48f214a25c32a7692f9fd0bc5eab`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2e67e1deca529e76612c525c5a8e12050d9ec84c3691673953e51573c1e653`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:5ae7b0317944de344d87247e9cb05a11dcd4f796e1800294193d7b60f43c9d9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9059f595926bbcc76e88f995c69a532e5bfdb37e53db7d9cbd26077b9a0f52d1`

```dockerfile
```

-	Layers:
	-	`sha256:a10a07e60572ceb3113b276c9a02c5aa46bf940b8f2a491e7064608fcac2409c`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:7c13d10c1f7169aaedc2ac8ecbc1f431dda7e906455b836d09a14b3b948f3036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10448793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa266dd5df001f7f566ffb0c8c8acff2de160efa06508788758a4e3022c8e98d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:39:54 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:39:54 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:39:54 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:39:55 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:39:55 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:39:55 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:39:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:39:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efe06b0c545d8e510a8131fe2984aa46a7c4d7502148ce8f2e94df5ffeed78f`  
		Last Modified: Wed, 20 May 2026 18:40:02 GMT  
		Size: 6.7 MB (6711165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3c6e5710602d0c65abfcc3a4aac8676e3cd1f849d5967bee0654b0ec045abe`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0fcc4ed5f0f4848feb91f0e5c409cb87bfd693a7056f2c0e574dbf0fc8ff4ab`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:7878f9d371c5d9227beef40f16b5dfd6d37465bab0104f835171af841d4c4a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47a1ee27b4ce5d60016cbff052995f2dbab1c7c6c61dcf79e2f75cbb1430fbad`

```dockerfile
```

-	Layers:
	-	`sha256:c27fc7351e2a880436edb13f3b1eaf0c5d83b4ec4a761386db3f8a0e0e8642a5`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:458d20eff2bdbc011304724399fc06b3db7dae7c95d0c806969fc503389a70c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10757148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0002a7df6776ecf8e0df1b73510a6014c1f519a3c9692cd787d8568dd8021d99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:48:37 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:48:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:48:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:48:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:48:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:48:43 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:48:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:48:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728aea4976117b7918cb9446c013c273cae16aa21337089d91cbd93761d10ae5`  
		Last Modified: Wed, 20 May 2026 18:49:10 GMT  
		Size: 7.1 MB (7102303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e102ba28952cc8bf83cffaefb3ec4b38d56cd736120ece8c71362ff603fd09b`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec22f8c91bd1e1b2e7f49773754ab16299137dd3226c8bb660a538d249364ae6`  
		Last Modified: Wed, 20 May 2026 18:49:08 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:38a69833b514d10d0b925fa5c4639cb5d17abe985f2b30699a0f305324397aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cffc57189208991582e7a0262e60b1415e19ac3919981144973c3d19428e23f6`

```dockerfile
```

-	Layers:
	-	`sha256:ccc40928ae38a1bd914e972d9acbe81dbc2e36b6132cee1761b8e20e7dda2db5`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-linux`

```console
$ docker pull nats@sha256:4223c8fa116891628611e154fb66570cad599d8f8b3b131b82caf10f378e9dcf
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
$ docker pull nats@sha256:aad7f400fa8a1cbcc2f818d5373638f91cfbfcac7cb9bd28fe6e8538c08b9c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6838210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39f65eeb0573eea876a604f186453a7a3cda0c8c511dd143432e1128e07a8734`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:10:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:10:38 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:10:38 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:10:38 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:10:38 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:10:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:05832d0be2949ff52eaf08a260411f3a4a020a066de4aa19dc62284052758304`  
		Last Modified: Wed, 20 May 2026 16:04:06 GMT  
		Size: 6.8 MB (6837703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a284b9b8e39214498d13f3dca35a9c9e81d34b69635ed74a3d47d26e45d5591`  
		Last Modified: Wed, 20 May 2026 19:10:42 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:6b2a0558891216e6e12622ac66d8766987858f507eee4cb4cfef25a0b1480e84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a061861dcdd34e8079637906d854df58e3e30fcfb0514aa93b4a1ada5b3936b9`

```dockerfile
```

-	Layers:
	-	`sha256:7fff463e51e2de542cc152e5196125c500561d37a866a78ab756f40188e25be6`  
		Last Modified: Wed, 20 May 2026 19:10:42 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:80f40fb067456022353b1754a4c58f49b1af454522a8af74e9c270e3a27668d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6573757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:039a8f82177ac58ba3952b7b25d8af7b14d0fbcf08e6e53efbab9e028b515cb5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:09:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:09:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:09:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:09:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:09:27 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:09:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3f675bd99a02bdb97f8ad1545908545b1e797e40d8038ce181205b0808044e20`  
		Last Modified: Wed, 20 May 2026 16:04:08 GMT  
		Size: 6.6 MB (6573248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715581626472620cc372593ae38a74d6c85239c0282bc3c5b7937fcd525bb308`  
		Last Modified: Wed, 20 May 2026 19:09:32 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:cd80c2a5593667a467031df5e49c9cab2cc1f5ae03e981c4789d7a262cbded23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac98f8edc0ec201da45e4d96bc1ea96d553e89648a61e35f8a195d38ce81d6b9`

```dockerfile
```

-	Layers:
	-	`sha256:d7cd588a4563631d4b86b381c7ee1c56114f94b80568f0e8defc278961b4c119`  
		Last Modified: Wed, 20 May 2026 19:09:31 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:ae43b4e3d705ed3a3386e6b303d8dfb011fec9e1cdf8523ff9c6387935d9652d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6565185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a493ff1dda3a5eb2f84019be4a31029f9463e5a91f142d91cbd96345245eadb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:09:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:09:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:09:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:09:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:09:01 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:09:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:07a4ad6a636748b056dca5d82613a936ff1872d9092911832cea1178d840cb7f`  
		Last Modified: Wed, 20 May 2026 16:04:08 GMT  
		Size: 6.6 MB (6564678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95ec1a5b2af5f3d81a39b2563595f7008790713449f52e148c254bc7d0be80e`  
		Last Modified: Wed, 20 May 2026 19:09:06 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:5b515d7d9aa87098056bad17534ca266bba383a9a52d362a1788c5ac7b596d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a1b7811acc104229e8cc148ff624e24efc4e31d06fce27cdd9091dd3237110`

```dockerfile
```

-	Layers:
	-	`sha256:e855458d7f5e87be1456ba294fc7386adaa0241520ff73ab4b95b94271f3d0a0`  
		Last Modified: Wed, 20 May 2026 19:09:05 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:89ea5f3d1a4e7db9650685b4b60d5f2340f6edd89f0d2a7a6f2a5cb9b6f144c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6189602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:080d11e023e3c9bc77bc5d6e137c30fcee2ca537fbda1d730ee0de9b5131cf97`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:10:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:10:02 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:10:02 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:10:02 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:10:02 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:10:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5f2fe2216ecafda68f73a81334875cb85722e57f12bc2af372cc03c4952017ff`  
		Last Modified: Wed, 20 May 2026 16:04:06 GMT  
		Size: 6.2 MB (6189094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f13aa02931bd62f5d9ce1935b8f163c6fcb3db670a4893037e6326c70ff971`  
		Last Modified: Wed, 20 May 2026 19:10:07 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:55f5544491f15bb813013ec1a1698f6e7e6f1ebbf96b4e49dba94dab9c27b313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30316b20c5d7aabdc5ded4b132f0725f10bdb7bd31bfbdb309184a8e58efe00c`

```dockerfile
```

-	Layers:
	-	`sha256:e06f44f5e5db93fe4fba02df22b44d37f71209d0cfbcbcec67b2ec6687bda27c`  
		Last Modified: Wed, 20 May 2026 19:10:07 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:9b9d19890e9399f86300407959de41b794ee8fd1b46720c7548163f7f94fd15e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6254150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dcae0dec9d781a4ed3bd8282b836bb0fc168482d57def8fec57c690ecdd111a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:09:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:09:00 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:09:00 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:09:00 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:09:00 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:09:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:eeebf06eacfa887b3524b3c76a2593bb68e43a09aa8ff01b5a09c0ce44ed2917`  
		Last Modified: Wed, 20 May 2026 16:04:05 GMT  
		Size: 6.3 MB (6253641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb234fae2f8c35c37c5a0a2b27b551816540b8c513f6b2c479728b77a462cc5`  
		Last Modified: Wed, 20 May 2026 19:09:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:44cc5336af1db8f2f590eca54680623452cbb2da64b65bb690521c087a9be389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2bccd9ad485d0016ce5f53e02daf116336befd19e206a354f9324e36b86c720`

```dockerfile
```

-	Layers:
	-	`sha256:33b891cec5ef0cfb52212abc7e2148afd94f43e4c045f9b8ee11b24532349469`  
		Last Modified: Wed, 20 May 2026 19:09:06 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; s390x

```console
$ docker pull nats@sha256:02ac81902397bc3ce3ae4f6bf57bb15925e02525fc49567e8db5747ae9e3cc7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6650240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f5f893e9ed2e5671b5afc696c46fd6aa4099811ef87a81fb46e2bf0c84ba84f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:10:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:10:22 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:10:24 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:10:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:10:24 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:10:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9e00525b36acc41f758b0363af2261253b6d35899fd8e6c7e6b4d30ff05eab43`  
		Last Modified: Wed, 20 May 2026 16:04:08 GMT  
		Size: 6.6 MB (6649731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61970d60cef7c5abc0f2985fb3486911eb5ae086553cd2bfb895dd97daa5dbe1`  
		Last Modified: Wed, 20 May 2026 19:10:43 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:91a6b246de893cdf55e56ebb0f717eb35cb29121fd44454bb5c2e66fe76ba11b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b822bf8bf39b54c102cf252c8b091bac1a2c642851dd34cc7445f10b19fbbe42`

```dockerfile
```

-	Layers:
	-	`sha256:a39452d35088530375cff827daeae3695859d1f87479bba2523d135b3256d905`  
		Last Modified: Wed, 20 May 2026 19:10:43 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:b8d325261e82cfa9b4561b3752e5791fc51c257bde48ca6e1ae65580749766a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2-nanoserver` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:ad04df86864a0653927e5ff2293212d694588db88edc746ce8b917417317c0f3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134078105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc7e5bd03f66dabebd5917cf13f4067081477a5934e86d07357d04db10e33ec4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 20 May 2026 19:09:14 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 20 May 2026 19:09:15 GMT
RUN cmd /S /C #(nop) COPY file:5d608f6a5cbf80544d196a9ac38d66b2635084a5e0a392611785993205e5329d in C:\nats-server.exe 
# Wed, 20 May 2026 19:09:16 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 20 May 2026 19:09:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 20 May 2026 19:09:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 20 May 2026 19:09:18 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c815e3255991cc2df065c98a27664be46d8b5db04231449f637ecaf64c5c098f`  
		Last Modified: Wed, 20 May 2026 19:09:24 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68983020294e3083531b7192194e9d5172d2a1449eac04682b7544bb139048b5`  
		Last Modified: Wed, 20 May 2026 19:09:27 GMT  
		Size: 7.0 MB (7033380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730756958a80b0245caf373feb8024993ecef9e67a8ade759511f66d001f3f07`  
		Last Modified: Wed, 20 May 2026 19:09:22 GMT  
		Size: 1.7 KB (1672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ec9d4f153ff90a362ff5591192559ff2e3584441d0bee4e4fdd8b0a4845b833`  
		Last Modified: Wed, 20 May 2026 19:09:22 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb6e35267fc994af8eab6412783ba571dd4c1d14e5fa8771f50a386e61ef655`  
		Last Modified: Wed, 20 May 2026 19:09:22 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838e55b2d659c4cc5f4e0db1773fbe38aa8487984688f5a0f60b202907588e42`  
		Last Modified: Wed, 20 May 2026 19:09:22 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:b8d325261e82cfa9b4561b3752e5791fc51c257bde48ca6e1ae65580749766a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2-nanoserver-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:ad04df86864a0653927e5ff2293212d694588db88edc746ce8b917417317c0f3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134078105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc7e5bd03f66dabebd5917cf13f4067081477a5934e86d07357d04db10e33ec4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 20 May 2026 19:09:14 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 20 May 2026 19:09:15 GMT
RUN cmd /S /C #(nop) COPY file:5d608f6a5cbf80544d196a9ac38d66b2635084a5e0a392611785993205e5329d in C:\nats-server.exe 
# Wed, 20 May 2026 19:09:16 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 20 May 2026 19:09:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 20 May 2026 19:09:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 20 May 2026 19:09:18 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c815e3255991cc2df065c98a27664be46d8b5db04231449f637ecaf64c5c098f`  
		Last Modified: Wed, 20 May 2026 19:09:24 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68983020294e3083531b7192194e9d5172d2a1449eac04682b7544bb139048b5`  
		Last Modified: Wed, 20 May 2026 19:09:27 GMT  
		Size: 7.0 MB (7033380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730756958a80b0245caf373feb8024993ecef9e67a8ade759511f66d001f3f07`  
		Last Modified: Wed, 20 May 2026 19:09:22 GMT  
		Size: 1.7 KB (1672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ec9d4f153ff90a362ff5591192559ff2e3584441d0bee4e4fdd8b0a4845b833`  
		Last Modified: Wed, 20 May 2026 19:09:22 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb6e35267fc994af8eab6412783ba571dd4c1d14e5fa8771f50a386e61ef655`  
		Last Modified: Wed, 20 May 2026 19:09:22 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838e55b2d659c4cc5f4e0db1773fbe38aa8487984688f5a0f60b202907588e42`  
		Last Modified: Wed, 20 May 2026 19:09:22 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:4223c8fa116891628611e154fb66570cad599d8f8b3b131b82caf10f378e9dcf
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
$ docker pull nats@sha256:aad7f400fa8a1cbcc2f818d5373638f91cfbfcac7cb9bd28fe6e8538c08b9c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6838210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39f65eeb0573eea876a604f186453a7a3cda0c8c511dd143432e1128e07a8734`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:10:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:10:38 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:10:38 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:10:38 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:10:38 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:10:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:05832d0be2949ff52eaf08a260411f3a4a020a066de4aa19dc62284052758304`  
		Last Modified: Wed, 20 May 2026 16:04:06 GMT  
		Size: 6.8 MB (6837703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a284b9b8e39214498d13f3dca35a9c9e81d34b69635ed74a3d47d26e45d5591`  
		Last Modified: Wed, 20 May 2026 19:10:42 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:6b2a0558891216e6e12622ac66d8766987858f507eee4cb4cfef25a0b1480e84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a061861dcdd34e8079637906d854df58e3e30fcfb0514aa93b4a1ada5b3936b9`

```dockerfile
```

-	Layers:
	-	`sha256:7fff463e51e2de542cc152e5196125c500561d37a866a78ab756f40188e25be6`  
		Last Modified: Wed, 20 May 2026 19:10:42 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:80f40fb067456022353b1754a4c58f49b1af454522a8af74e9c270e3a27668d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6573757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:039a8f82177ac58ba3952b7b25d8af7b14d0fbcf08e6e53efbab9e028b515cb5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:09:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:09:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:09:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:09:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:09:27 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:09:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3f675bd99a02bdb97f8ad1545908545b1e797e40d8038ce181205b0808044e20`  
		Last Modified: Wed, 20 May 2026 16:04:08 GMT  
		Size: 6.6 MB (6573248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715581626472620cc372593ae38a74d6c85239c0282bc3c5b7937fcd525bb308`  
		Last Modified: Wed, 20 May 2026 19:09:32 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:cd80c2a5593667a467031df5e49c9cab2cc1f5ae03e981c4789d7a262cbded23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac98f8edc0ec201da45e4d96bc1ea96d553e89648a61e35f8a195d38ce81d6b9`

```dockerfile
```

-	Layers:
	-	`sha256:d7cd588a4563631d4b86b381c7ee1c56114f94b80568f0e8defc278961b4c119`  
		Last Modified: Wed, 20 May 2026 19:09:31 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:ae43b4e3d705ed3a3386e6b303d8dfb011fec9e1cdf8523ff9c6387935d9652d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6565185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a493ff1dda3a5eb2f84019be4a31029f9463e5a91f142d91cbd96345245eadb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:09:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:09:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:09:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:09:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:09:01 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:09:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:07a4ad6a636748b056dca5d82613a936ff1872d9092911832cea1178d840cb7f`  
		Last Modified: Wed, 20 May 2026 16:04:08 GMT  
		Size: 6.6 MB (6564678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95ec1a5b2af5f3d81a39b2563595f7008790713449f52e148c254bc7d0be80e`  
		Last Modified: Wed, 20 May 2026 19:09:06 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:5b515d7d9aa87098056bad17534ca266bba383a9a52d362a1788c5ac7b596d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a1b7811acc104229e8cc148ff624e24efc4e31d06fce27cdd9091dd3237110`

```dockerfile
```

-	Layers:
	-	`sha256:e855458d7f5e87be1456ba294fc7386adaa0241520ff73ab4b95b94271f3d0a0`  
		Last Modified: Wed, 20 May 2026 19:09:05 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:89ea5f3d1a4e7db9650685b4b60d5f2340f6edd89f0d2a7a6f2a5cb9b6f144c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6189602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:080d11e023e3c9bc77bc5d6e137c30fcee2ca537fbda1d730ee0de9b5131cf97`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:10:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:10:02 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:10:02 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:10:02 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:10:02 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:10:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5f2fe2216ecafda68f73a81334875cb85722e57f12bc2af372cc03c4952017ff`  
		Last Modified: Wed, 20 May 2026 16:04:06 GMT  
		Size: 6.2 MB (6189094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f13aa02931bd62f5d9ce1935b8f163c6fcb3db670a4893037e6326c70ff971`  
		Last Modified: Wed, 20 May 2026 19:10:07 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:55f5544491f15bb813013ec1a1698f6e7e6f1ebbf96b4e49dba94dab9c27b313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30316b20c5d7aabdc5ded4b132f0725f10bdb7bd31bfbdb309184a8e58efe00c`

```dockerfile
```

-	Layers:
	-	`sha256:e06f44f5e5db93fe4fba02df22b44d37f71209d0cfbcbcec67b2ec6687bda27c`  
		Last Modified: Wed, 20 May 2026 19:10:07 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:9b9d19890e9399f86300407959de41b794ee8fd1b46720c7548163f7f94fd15e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6254150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dcae0dec9d781a4ed3bd8282b836bb0fc168482d57def8fec57c690ecdd111a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:09:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:09:00 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:09:00 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:09:00 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:09:00 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:09:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:eeebf06eacfa887b3524b3c76a2593bb68e43a09aa8ff01b5a09c0ce44ed2917`  
		Last Modified: Wed, 20 May 2026 16:04:05 GMT  
		Size: 6.3 MB (6253641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb234fae2f8c35c37c5a0a2b27b551816540b8c513f6b2c479728b77a462cc5`  
		Last Modified: Wed, 20 May 2026 19:09:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:44cc5336af1db8f2f590eca54680623452cbb2da64b65bb690521c087a9be389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2bccd9ad485d0016ce5f53e02daf116336befd19e206a354f9324e36b86c720`

```dockerfile
```

-	Layers:
	-	`sha256:33b891cec5ef0cfb52212abc7e2148afd94f43e4c045f9b8ee11b24532349469`  
		Last Modified: Wed, 20 May 2026 19:09:06 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; s390x

```console
$ docker pull nats@sha256:02ac81902397bc3ce3ae4f6bf57bb15925e02525fc49567e8db5747ae9e3cc7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6650240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f5f893e9ed2e5671b5afc696c46fd6aa4099811ef87a81fb46e2bf0c84ba84f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:10:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:10:22 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:10:24 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:10:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:10:24 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:10:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9e00525b36acc41f758b0363af2261253b6d35899fd8e6c7e6b4d30ff05eab43`  
		Last Modified: Wed, 20 May 2026 16:04:08 GMT  
		Size: 6.6 MB (6649731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61970d60cef7c5abc0f2985fb3486911eb5ae086553cd2bfb895dd97daa5dbe1`  
		Last Modified: Wed, 20 May 2026 19:10:43 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:91a6b246de893cdf55e56ebb0f717eb35cb29121fd44454bb5c2e66fe76ba11b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b822bf8bf39b54c102cf252c8b091bac1a2c642851dd34cc7445f10b19fbbe42`

```dockerfile
```

-	Layers:
	-	`sha256:a39452d35088530375cff827daeae3695859d1f87479bba2523d135b3256d905`  
		Last Modified: Wed, 20 May 2026 19:10:43 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:1ba584aa4a0b9afe4503a0bb74145174a5a8bd168c74991253e74a0f28cb7a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2-windowsservercore` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:7c0d2cfcb1ac8b9c5c8667631fe266d5058f54979c724dbc779cd1303cf56e41
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2130333726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2e9ee9e3b452a65f51ce4b7daa32d3b40f548b8548d8e18d6af0f98c1a6fd8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Wed, 20 May 2026 18:42:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 20 May 2026 18:42:48 GMT
ENV NATS_DOCKERIZED=1
# Wed, 20 May 2026 18:42:49 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:42:51 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:42:53 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.14.1/nats-server-v2.14.1-windows-amd64.zip
# Wed, 20 May 2026 18:42:55 GMT
ENV NATS_SERVER_SHASUM=fb7ddfdde7da0ce89a5174c00b0f7fa9d559ee88c6de638c681b464d35e7caca
# Wed, 20 May 2026 18:44:05 GMT
RUN Set-PSDebug -Trace 2
# Wed, 20 May 2026 18:44:38 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 20 May 2026 18:44:39 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 20 May 2026 18:44:40 GMT
EXPOSE 4222 6222 8222
# Wed, 20 May 2026 18:44:42 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 20 May 2026 18:44:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9541aea3e55bd746462fb4c6e57da81839bbdd92cde8c45bec531dc275c949`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acaeb80d5acbf745ec935e19b9c27aac2c1c36569184a441931640832febb401`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53700d3104e235624a186296ebdbc80307001a56022c9d7a56ca8e8441f1352e`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4698b50a4704844bff262f3486b8d21762a0b2216da94ee49cf3304647a202cf`  
		Last Modified: Wed, 20 May 2026 18:44:50 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39739d4a0333d45798f9c82521d794f7861019e48fcbfc35cec644df0ae2a4bf`  
		Last Modified: Wed, 20 May 2026 18:44:50 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4785912cbc50e52449bd79d36df3b0b1c35e93f26131aeb601005aa38d99d9f2`  
		Last Modified: Wed, 20 May 2026 18:44:50 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406ecfff99aabce085a608a58a3bc33d019a6c6a474f26cd2f037294ab00c29d`  
		Last Modified: Wed, 20 May 2026 18:44:51 GMT  
		Size: 501.6 KB (501598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653bb3e0442eb7d700abb5d1a972abb676d295a6e84793deb25232914a8e833e`  
		Last Modified: Wed, 20 May 2026 18:44:53 GMT  
		Size: 7.4 MB (7397859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662d62953cb63a3accb3782436a9739838d80e2f9610ceac2e47628cc18600fe`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7ba9d33ea88ed49cf0a5cf22fe293c829f1ad64c930e440993b2cb04a3e59a`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fd31c298d20b844c00bdce2ffe2a2370b1d271d45448caa64c2c4c9817afcf`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96cf0d23ad307ba86365cfda67df65a63a9b427078a3ba2715c22735719e8dd0`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:1ba584aa4a0b9afe4503a0bb74145174a5a8bd168c74991253e74a0f28cb7a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2-windowsservercore-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:7c0d2cfcb1ac8b9c5c8667631fe266d5058f54979c724dbc779cd1303cf56e41
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2130333726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2e9ee9e3b452a65f51ce4b7daa32d3b40f548b8548d8e18d6af0f98c1a6fd8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Wed, 20 May 2026 18:42:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 20 May 2026 18:42:48 GMT
ENV NATS_DOCKERIZED=1
# Wed, 20 May 2026 18:42:49 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:42:51 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:42:53 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.14.1/nats-server-v2.14.1-windows-amd64.zip
# Wed, 20 May 2026 18:42:55 GMT
ENV NATS_SERVER_SHASUM=fb7ddfdde7da0ce89a5174c00b0f7fa9d559ee88c6de638c681b464d35e7caca
# Wed, 20 May 2026 18:44:05 GMT
RUN Set-PSDebug -Trace 2
# Wed, 20 May 2026 18:44:38 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 20 May 2026 18:44:39 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 20 May 2026 18:44:40 GMT
EXPOSE 4222 6222 8222
# Wed, 20 May 2026 18:44:42 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 20 May 2026 18:44:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9541aea3e55bd746462fb4c6e57da81839bbdd92cde8c45bec531dc275c949`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acaeb80d5acbf745ec935e19b9c27aac2c1c36569184a441931640832febb401`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53700d3104e235624a186296ebdbc80307001a56022c9d7a56ca8e8441f1352e`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4698b50a4704844bff262f3486b8d21762a0b2216da94ee49cf3304647a202cf`  
		Last Modified: Wed, 20 May 2026 18:44:50 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39739d4a0333d45798f9c82521d794f7861019e48fcbfc35cec644df0ae2a4bf`  
		Last Modified: Wed, 20 May 2026 18:44:50 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4785912cbc50e52449bd79d36df3b0b1c35e93f26131aeb601005aa38d99d9f2`  
		Last Modified: Wed, 20 May 2026 18:44:50 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406ecfff99aabce085a608a58a3bc33d019a6c6a474f26cd2f037294ab00c29d`  
		Last Modified: Wed, 20 May 2026 18:44:51 GMT  
		Size: 501.6 KB (501598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653bb3e0442eb7d700abb5d1a972abb676d295a6e84793deb25232914a8e833e`  
		Last Modified: Wed, 20 May 2026 18:44:53 GMT  
		Size: 7.4 MB (7397859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662d62953cb63a3accb3782436a9739838d80e2f9610ceac2e47628cc18600fe`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7ba9d33ea88ed49cf0a5cf22fe293c829f1ad64c930e440993b2cb04a3e59a`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fd31c298d20b844c00bdce2ffe2a2370b1d271d45448caa64c2c4c9817afcf`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96cf0d23ad307ba86365cfda67df65a63a9b427078a3ba2715c22735719e8dd0`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12`

```console
$ docker pull nats@sha256:9dc953fcaefeec300a44f07cde52cc686823156c667bc27b2ee08adb7140f7a2
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
	-	windows version 10.0.20348.5139; amd64

### `nats:2.12` - linux; amd64

```console
$ docker pull nats@sha256:81dd79785518efd999b91f95c3704444c73865f457c195dbc2a7ca54f9e82b9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6643802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eee8ee507e1167111022248b38dc79952282435780aa5561a54272070231fba`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:10:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:10:49 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:10:49 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:10:49 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:10:49 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:10:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e5e76f67b303999883527fbb9d2827bb20bf4266bd14b30fe193b9c837d56b9`  
		Last Modified: Wed, 20 May 2026 16:04:23 GMT  
		Size: 6.6 MB (6643293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a25302c76354939bc63896b8a3c3e531819ed31d7c3fabed2c21912ed5a778a`  
		Last Modified: Wed, 20 May 2026 19:10:53 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:63bdef746f1bd984ed04788dbb4683d8899fde6b501588af9d034679f4d5c4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e9d8d10730cd5f5322c955e5243b4f410f4f61622f7e434b533f38cbfa8b9bd`

```dockerfile
```

-	Layers:
	-	`sha256:29922663c3486deec187939e4f05d87cecd02dbb505dadb59cab3b9b718aa068`  
		Last Modified: Wed, 20 May 2026 19:10:53 GMT  
		Size: 8.7 KB (8660 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; arm variant v6

```console
$ docker pull nats@sha256:697254950318448b92489577435eb73db46ad779dfa5bb8312950fcbcf774fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6383827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e55c4a455573962fac86f8a167ca43e89be66b7799b10d76e5465fdf00ffdf7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:09:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:09:39 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:09:39 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:09:39 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:09:39 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:09:39 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c10d60a8ee2ca1e386312db0a0b2473313d36b33da2c5a1eed45d3dbc145b255`  
		Last Modified: Wed, 20 May 2026 16:04:26 GMT  
		Size: 6.4 MB (6383319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1d283fe91c0f3527ed49fb1f312ae136b8fb1cab01bd902b22c0a912727bc7`  
		Last Modified: Wed, 20 May 2026 19:09:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:cc69b4de3ae7531530b6ae76912d528339157b572f0c822676897fac26e728d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08a5b8c8548b84e96f500c4ee6700a282c92ebc58d03b35f1d49ab5424ba360d`

```dockerfile
```

-	Layers:
	-	`sha256:bf6a20cdeb4777f1f89bf3b91149fbb9cd5193d460d2720e5856bc2a69d08a65`  
		Last Modified: Wed, 20 May 2026 19:09:43 GMT  
		Size: 8.7 KB (8744 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; arm variant v7

```console
$ docker pull nats@sha256:a2d058ffac3e0982c4263c4a98357898b61eca619d2c56a76aac7b9f2d18f171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6373077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:130977b1791d287860791cbc0f238f4bf8902acceeb859fc8663ca013fc90b15`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:09:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:09:50 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:09:50 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:09:50 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:09:50 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:09:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:efec7643648fe287ed0901613783bcd23bb5a8b7b2fb2aee2e9f58a8d0d8d7a8`  
		Last Modified: Wed, 20 May 2026 16:04:26 GMT  
		Size: 6.4 MB (6372568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af920700845e87c0ae0d0a2e002936cf3fe153e0d75cd8d28e1fdebe0951676c`  
		Last Modified: Wed, 20 May 2026 19:09:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:a96c4eefe96a686ef87c6963d464d87de0be9f9d27e2e065a01137de83f6f1ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f334115d58195d99db72b89b7cd06f5d63fbbfe2344d46642d5e03925960c426`

```dockerfile
```

-	Layers:
	-	`sha256:44bb6f0b5261e2b3668d54d1d0f788b8e18dd4e2ba44ef27c0949c43398854e9`  
		Last Modified: Wed, 20 May 2026 19:09:54 GMT  
		Size: 8.7 KB (8744 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:aa8f7e3d55a383e35f019c28b6c432ed2090b3dad56fead3e7a70ab1dba79ccc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6037707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1b69482ef45b939a2908e033d22c9582db2b53dac733301472ace541c756069`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:10:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:10:14 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:10:14 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:10:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:10:14 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:10:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:81af0467f4bfb473e50c712e06ca48adff2e7aab8456b45fcfbc3fefe8ef6df7`  
		Last Modified: Wed, 20 May 2026 16:04:24 GMT  
		Size: 6.0 MB (6037200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed22b68f9def9c87dfb1c5a9ec34a809caf385bcdfdd456fd3be55b553020ad`  
		Last Modified: Wed, 20 May 2026 19:10:19 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:534c5df88f202c2a015c845378127d701cc4faf3641326573fce6c0fd64dbd1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0a9c9217edbec11dd3120e94f789339bb631670a66be81de8e106830fef4b4`

```dockerfile
```

-	Layers:
	-	`sha256:743146aaf7c71f426d7abd3b4db2abcd72ecfd72aed9db12cb025a3148324d81`  
		Last Modified: Wed, 20 May 2026 19:10:19 GMT  
		Size: 8.8 KB (8774 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; ppc64le

```console
$ docker pull nats@sha256:3a024c2519d3e8d9afa913cc70dc8a08f42c27841b819c13ae7f4746791667f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6100417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a86f1bedebf55c136505a6a6115d4879fd94839c05722c2813b743b911513fc7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:09:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:09:00 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:09:00 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:09:00 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:09:00 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:09:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8d94981a1be7de02d7553ad09e31ec60ee268df51c2ef4762da5828b6b45674`  
		Last Modified: Wed, 20 May 2026 16:04:23 GMT  
		Size: 6.1 MB (6099908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb234fae2f8c35c37c5a0a2b27b551816540b8c513f6b2c479728b77a462cc5`  
		Last Modified: Wed, 20 May 2026 19:09:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:4bc8adf9c89eb891276d88ad9ef5302e83c23305ea4eee6318fdf94156bf00f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c21faa8dd4d3dbf3346283035cadd5da1c813c60749a515846c980e8940f08d8`

```dockerfile
```

-	Layers:
	-	`sha256:dd4e6d8e65f686896f2c04a5c31ca21c193b8ac222cbaa55fc6cf1e4ecbc68d7`  
		Last Modified: Wed, 20 May 2026 19:09:06 GMT  
		Size: 8.7 KB (8715 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; s390x

```console
$ docker pull nats@sha256:0ff65b369dcf8b26046db1efa962fef20887641c137fba88592e99ac6d946759
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6491050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1fbd0e893d6064d2ae64507740f42429bfd8b6626f01ff155f71d68cbac6dfe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:10:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:10:29 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:10:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:10:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:10:30 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:10:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d668ec0d13619d02b98ac6e2ab2bb7ca3974ad1ed964fbbfae78e23a777df473`  
		Last Modified: Wed, 20 May 2026 16:04:26 GMT  
		Size: 6.5 MB (6490542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5c187c9ced3347b391d712fe3353958272e09460e48ef72b492e55332f67a0`  
		Last Modified: Wed, 20 May 2026 19:10:48 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:6868356eb5df018325b032eca1a4d9471a915135b6ad01baf74cbed5245b7581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74a49ccc3dc2aca4a464c76934f3739fa2e4fdbc49a4fe3a93d58e620431eba9`

```dockerfile
```

-	Layers:
	-	`sha256:beed34e5caa7d0f8bb8e9624e6acbd693112ad713d81a6ebe9751d3d4a144a83`  
		Last Modified: Wed, 20 May 2026 19:10:48 GMT  
		Size: 8.7 KB (8661 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:b5f413bd3b0f768cdcfb88471ef7dd7e1e8979c00517fecb6fec681e1ff658dc
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133878103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14eeb0f5e1235887ceab95fb27b69b508faa0a9be7ec8654eb6483d61bd87539`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 20 May 2026 19:09:14 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 20 May 2026 19:09:43 GMT
RUN cmd /S /C #(nop) COPY file:dd9132ddd79eef4f3cbcb173e3b4c47616b6109b67b3da726ffcf5aa0546dfe6 in C:\nats-server.exe 
# Wed, 20 May 2026 19:09:44 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 20 May 2026 19:09:44 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 20 May 2026 19:09:44 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 20 May 2026 19:09:45 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c815e3255991cc2df065c98a27664be46d8b5db04231449f637ecaf64c5c098f`  
		Last Modified: Wed, 20 May 2026 19:09:24 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0584329bf51b06503599bd12d61e5b4b8022e17567c5a00bf044a36fec53f6ca`  
		Last Modified: Wed, 20 May 2026 19:09:54 GMT  
		Size: 6.8 MB (6833293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42502c403069fbf82a9dfaead168b2b5f649366919a105dc982b8388c2da2055`  
		Last Modified: Wed, 20 May 2026 19:09:49 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f632ce4ec8c46651a30b231de5b71039037abbc82f1bede845e302e0a576a256`  
		Last Modified: Wed, 20 May 2026 19:09:49 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceaf1e7278afa4664b03b5df7ba7fb9043b402be47232554b124a56a1c85927c`  
		Last Modified: Wed, 20 May 2026 19:09:49 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d4067da1a0ad2b0d46b1f5bbaebefcfeb420dbac588629c9d392f95f7723d4`  
		Last Modified: Wed, 20 May 2026 19:09:49 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12-alpine`

```console
$ docker pull nats@sha256:d152634b3db31218ca61c794827d04e8133e2538ef2f2cc3ab7be77b2ea8efd0
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

### `nats:2.12-alpine` - linux; amd64

```console
$ docker pull nats@sha256:9f005ca5efcae24ddd0413014c8ba5d3464d2a2560233b1bff108cc5563df009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10909206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c4eb9669610892376f2a3886a0c6e7b61fc0f2c5d3f740abe33e501f3f184c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:37:22 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:37:22 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:37:22 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='72b5841a019f6c5a0be78d3cf21cd293446317e6b4e769e3b9d72090f2d87afc' ;;     armhf) natsArch='arm6'; sha256='eb159297eb8539e47f615180b1de759e6a735cfe3274a31d405301e1c2ee2aec' ;;     armv7) natsArch='arm7'; sha256='2573d1cb723f55d81c58e854e63c771e1a2d954a91ed0a23042e7e38fa0d405c' ;;     x86_64) natsArch='amd64'; sha256='b126515225aa2265a0088e0170f2a9de4c7880b2388cc7584aa77859ce831e3f' ;;     x86) natsArch='386'; sha256='c29a867045b25e300e501101abc3714e4e56c89b35b90ddbfc55ec6e7928eb17' ;;     s390x) natsArch='s390x'; sha256='d508d9f40853828623b50e367a4dd0394361352195b3669d5da7966991e30c03' ;;     ppc64le) natsArch='ppc64le'; sha256='a2dcbabba4aede66b9939d59e829d61417fffa7c08c49635b9a550a23f733cdc' ;;     loong64) natsArch='loong64'; sha256='5a0347fa1400a569cc798da80001fca8c68dc7193daea334df9ea6ec5fe2649c' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:37:22 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:37:22 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:37:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:37:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:37:22 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785afd645f29603dfc502b5aed95092773a9d75614d744ab69f3c90a491db958`  
		Last Modified: Wed, 20 May 2026 18:37:27 GMT  
		Size: 7.1 MB (7100047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2f75731780f4bdd6e4465ff6aedcfb784f2e04de6f7f593183a54df15a238b`  
		Last Modified: Wed, 20 May 2026 18:37:26 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea647ca93a5f93dd0481e42085d112026c222e13018b23f940c1798f150ddfc1`  
		Last Modified: Wed, 20 May 2026 18:37:27 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:c8082807e13d0ed6d2ad0cebcad6ff56b3a50637c7121d851c85bc76d43e51db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d6c6f5b5e660ea789920f5dadbe9d69a4b9c17b3cb539f1ad32abfe974a8016`

```dockerfile
```

-	Layers:
	-	`sha256:d118d5c6f5a5b003d23105ccb683ce7cbca22c58923371c7a4cad24bb2a0fa7a`  
		Last Modified: Wed, 20 May 2026 18:37:27 GMT  
		Size: 14.2 KB (14204 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:6ca666c2519ce831880fc65291a7ba5e6bdde44f1fce5826695e03943924c735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10347662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae81b57a35e9f65ea23549d2183c2c2e7ca7d50ce3f5036fa062e1cafaf518d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:36:19 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:36:19 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:36:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='72b5841a019f6c5a0be78d3cf21cd293446317e6b4e769e3b9d72090f2d87afc' ;;     armhf) natsArch='arm6'; sha256='eb159297eb8539e47f615180b1de759e6a735cfe3274a31d405301e1c2ee2aec' ;;     armv7) natsArch='arm7'; sha256='2573d1cb723f55d81c58e854e63c771e1a2d954a91ed0a23042e7e38fa0d405c' ;;     x86_64) natsArch='amd64'; sha256='b126515225aa2265a0088e0170f2a9de4c7880b2388cc7584aa77859ce831e3f' ;;     x86) natsArch='386'; sha256='c29a867045b25e300e501101abc3714e4e56c89b35b90ddbfc55ec6e7928eb17' ;;     s390x) natsArch='s390x'; sha256='d508d9f40853828623b50e367a4dd0394361352195b3669d5da7966991e30c03' ;;     ppc64le) natsArch='ppc64le'; sha256='a2dcbabba4aede66b9939d59e829d61417fffa7c08c49635b9a550a23f733cdc' ;;     loong64) natsArch='loong64'; sha256='5a0347fa1400a569cc798da80001fca8c68dc7193daea334df9ea6ec5fe2649c' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:36:19 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:36:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:36:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:36:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:36:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2912b40ddee494992b06ce6cfb3fe8dcb65d8de1892afcc94917eca78b7d9a0e`  
		Last Modified: Wed, 20 May 2026 18:36:24 GMT  
		Size: 6.8 MB (6839309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c4d072278e3126931517cbe8b2c9ef7cb6deb74558f56fedca986a5290a04c`  
		Last Modified: Wed, 20 May 2026 18:36:24 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f197927573b1036dd0f62c1a4cc9744836b24dbc6a2f4de557bdc47a30ce8be`  
		Last Modified: Wed, 20 May 2026 18:36:23 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:c61ccd3efdac690b485d840b7dfeceda69959a897f80949d0526c35a457cf1f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eecbe0cf18d59940e35cb0d2a6250eef69ca91a9543eb363af073473e44f86c`

```dockerfile
```

-	Layers:
	-	`sha256:18009424a0cc1065f3e1eef0bf7339139ef37661b11ace35f1b5949d76f335d9`  
		Last Modified: Wed, 20 May 2026 18:36:23 GMT  
		Size: 14.3 KB (14284 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:bcaff37bbf2a1f726cb43e74fe7db6b6e753a949c6083b2822d18e14da85ca0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10055590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd657e711d296590c867eb7ef48b021588d25b86bfad505ec5ae8cde2ec1d1d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:36:15 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:36:15 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:36:15 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='72b5841a019f6c5a0be78d3cf21cd293446317e6b4e769e3b9d72090f2d87afc' ;;     armhf) natsArch='arm6'; sha256='eb159297eb8539e47f615180b1de759e6a735cfe3274a31d405301e1c2ee2aec' ;;     armv7) natsArch='arm7'; sha256='2573d1cb723f55d81c58e854e63c771e1a2d954a91ed0a23042e7e38fa0d405c' ;;     x86_64) natsArch='amd64'; sha256='b126515225aa2265a0088e0170f2a9de4c7880b2388cc7584aa77859ce831e3f' ;;     x86) natsArch='386'; sha256='c29a867045b25e300e501101abc3714e4e56c89b35b90ddbfc55ec6e7928eb17' ;;     s390x) natsArch='s390x'; sha256='d508d9f40853828623b50e367a4dd0394361352195b3669d5da7966991e30c03' ;;     ppc64le) natsArch='ppc64le'; sha256='a2dcbabba4aede66b9939d59e829d61417fffa7c08c49635b9a550a23f733cdc' ;;     loong64) natsArch='loong64'; sha256='5a0347fa1400a569cc798da80001fca8c68dc7193daea334df9ea6ec5fe2649c' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:36:15 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:36:15 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:36:15 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:36:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:36:15 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc50b4a871d38a0cadde4ed4e424bc2187dfef3cd7b5af2f61d284f5000115cd`  
		Last Modified: Wed, 20 May 2026 18:36:20 GMT  
		Size: 6.8 MB (6828786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9549ff00bf4e47e9e775e46e3309a6c2d758382c50d7296865843e1034afe6dc`  
		Last Modified: Wed, 20 May 2026 18:36:20 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519ec8720496ec12b71688a575e86930c39ad7b2f5f12bc6e1ea5efa4b6ed815`  
		Last Modified: Wed, 20 May 2026 18:36:20 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:c35fea02bd550591fb78b42bc3e5316a3ce215f434775a80bfb9160fbd852a30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64701b345d4b8c5c56c71be078a3da0398507cd26e5919d9645432b5788339d9`

```dockerfile
```

-	Layers:
	-	`sha256:98625cfe5efdb1372a3b79cc98481ba6088f0d689b3566d4b9137f4ae7c4e389`  
		Last Modified: Wed, 20 May 2026 18:36:20 GMT  
		Size: 14.3 KB (14284 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d5e2a634247e27b59ccf258b33f626c0f5949b96b737536496b562f06b7e094c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10642176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80fc2db9d5bb25035d90c05c366a4658fad874a40ee451f2a41188d4f6ead80b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:37:06 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:37:06 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:37:06 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='72b5841a019f6c5a0be78d3cf21cd293446317e6b4e769e3b9d72090f2d87afc' ;;     armhf) natsArch='arm6'; sha256='eb159297eb8539e47f615180b1de759e6a735cfe3274a31d405301e1c2ee2aec' ;;     armv7) natsArch='arm7'; sha256='2573d1cb723f55d81c58e854e63c771e1a2d954a91ed0a23042e7e38fa0d405c' ;;     x86_64) natsArch='amd64'; sha256='b126515225aa2265a0088e0170f2a9de4c7880b2388cc7584aa77859ce831e3f' ;;     x86) natsArch='386'; sha256='c29a867045b25e300e501101abc3714e4e56c89b35b90ddbfc55ec6e7928eb17' ;;     s390x) natsArch='s390x'; sha256='d508d9f40853828623b50e367a4dd0394361352195b3669d5da7966991e30c03' ;;     ppc64le) natsArch='ppc64le'; sha256='a2dcbabba4aede66b9939d59e829d61417fffa7c08c49635b9a550a23f733cdc' ;;     loong64) natsArch='loong64'; sha256='5a0347fa1400a569cc798da80001fca8c68dc7193daea334df9ea6ec5fe2649c' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:37:06 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:37:06 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:37:06 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:37:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:37:06 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ff339b51fb101889997a78aaa1897c82810b93750d3c1fad2c9939c172510d`  
		Last Modified: Wed, 20 May 2026 18:37:11 GMT  
		Size: 6.5 MB (6499312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01cdeeebd5372e1dc9a2c97c853e72b20a3622eed3457557f5913caa2b335da1`  
		Last Modified: Wed, 20 May 2026 18:37:11 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1624ccef5078119f6ce1d17ffcdd69ee710740b23ed841fbd209e80c8b6f3032`  
		Last Modified: Wed, 20 May 2026 18:37:11 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:d2b097ebfadc88817dcda244513c1536ee40a0fe3e24f28e6094d7eddf30a9ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:195c6c70cb97e0570c5672af8dc9c1b933cc356306a6daae576ac7e92b55ee69`

```dockerfile
```

-	Layers:
	-	`sha256:9145327976083751cab916e93d4003480e2bc0b428d04a554617da1720ba9788`  
		Last Modified: Wed, 20 May 2026 18:37:11 GMT  
		Size: 14.3 KB (14308 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:2e2a8c50a862185aabb439c2fe0736bf976ac4f14f840192f46ada06908ec62b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10295179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6684ad61a65a2f9bf995f867d9d9d9b78d57e72ecbac3ca56cb56b6e407e0ad6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:39:54 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:39:54 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:39:54 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='72b5841a019f6c5a0be78d3cf21cd293446317e6b4e769e3b9d72090f2d87afc' ;;     armhf) natsArch='arm6'; sha256='eb159297eb8539e47f615180b1de759e6a735cfe3274a31d405301e1c2ee2aec' ;;     armv7) natsArch='arm7'; sha256='2573d1cb723f55d81c58e854e63c771e1a2d954a91ed0a23042e7e38fa0d405c' ;;     x86_64) natsArch='amd64'; sha256='b126515225aa2265a0088e0170f2a9de4c7880b2388cc7584aa77859ce831e3f' ;;     x86) natsArch='386'; sha256='c29a867045b25e300e501101abc3714e4e56c89b35b90ddbfc55ec6e7928eb17' ;;     s390x) natsArch='s390x'; sha256='d508d9f40853828623b50e367a4dd0394361352195b3669d5da7966991e30c03' ;;     ppc64le) natsArch='ppc64le'; sha256='a2dcbabba4aede66b9939d59e829d61417fffa7c08c49635b9a550a23f733cdc' ;;     loong64) natsArch='loong64'; sha256='5a0347fa1400a569cc798da80001fca8c68dc7193daea334df9ea6ec5fe2649c' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:39:55 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:39:55 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:39:55 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:39:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:39:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe0b03709a632c9f299b1ef2c2691c1b292ae9f333a7b2083a9b51162a19669`  
		Last Modified: Wed, 20 May 2026 18:40:02 GMT  
		Size: 6.6 MB (6557551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3c6e5710602d0c65abfcc3a4aac8676e3cd1f849d5967bee0654b0ec045abe`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0fcc4ed5f0f4848feb91f0e5c409cb87bfd693a7056f2c0e574dbf0fc8ff4ab`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:5b7ba3b09bf23127b1a75c412fb6e5e3fa773abda140a3f0e45600422968bf88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b9cec962a037f640085142478803038714db7fa629a4b7e6cad1c2f41371943`

```dockerfile
```

-	Layers:
	-	`sha256:bc2e73ad0cbc0cad27f1667939617eb3a7d77a3ba7dd6d70917518d2ee4fed7f`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 14.2 KB (14248 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; s390x

```console
$ docker pull nats@sha256:ce14e245951893e72e72ac26599d178e07af3e24fd01a857cc00c484fee718cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10603715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0f596aa7cbe6e6e80f8063aae3852a811f7045c570a2bf4e89c6b1c0a0d596f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:48:37 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:48:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:48:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='72b5841a019f6c5a0be78d3cf21cd293446317e6b4e769e3b9d72090f2d87afc' ;;     armhf) natsArch='arm6'; sha256='eb159297eb8539e47f615180b1de759e6a735cfe3274a31d405301e1c2ee2aec' ;;     armv7) natsArch='arm7'; sha256='2573d1cb723f55d81c58e854e63c771e1a2d954a91ed0a23042e7e38fa0d405c' ;;     x86_64) natsArch='amd64'; sha256='b126515225aa2265a0088e0170f2a9de4c7880b2388cc7584aa77859ce831e3f' ;;     x86) natsArch='386'; sha256='c29a867045b25e300e501101abc3714e4e56c89b35b90ddbfc55ec6e7928eb17' ;;     s390x) natsArch='s390x'; sha256='d508d9f40853828623b50e367a4dd0394361352195b3669d5da7966991e30c03' ;;     ppc64le) natsArch='ppc64le'; sha256='a2dcbabba4aede66b9939d59e829d61417fffa7c08c49635b9a550a23f733cdc' ;;     loong64) natsArch='loong64'; sha256='5a0347fa1400a569cc798da80001fca8c68dc7193daea334df9ea6ec5fe2649c' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:48:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:48:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:48:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:48:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:48:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13002ceadd3c101c2cfaa462d93d68f1056f8fd0453fd99269b12c624bc6b38a`  
		Last Modified: Wed, 20 May 2026 18:49:13 GMT  
		Size: 6.9 MB (6948871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdaa4e64de2e200c41440e78516f3fbbcf03b5b5e18cb05b20a63bd1661ce87d`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d69a6bdd10e86979de515f61b8c590bea15507a88f17e4f5a7f57ddfac937e`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:92726e2db0802623d76696809568374f168d11a6eb505249100949eb89a74c6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a1345efb532a7d2fa604c74539fdd13035a959493b0f11f0e962227e91cfe8e`

```dockerfile
```

-	Layers:
	-	`sha256:afc92f71ec0a9bc07c23a3ff65bc6f32afe90cfc974b6e23b25a06cab13804fd`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 14.2 KB (14204 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12-alpine3.22`

```console
$ docker pull nats@sha256:d152634b3db31218ca61c794827d04e8133e2538ef2f2cc3ab7be77b2ea8efd0
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

### `nats:2.12-alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:9f005ca5efcae24ddd0413014c8ba5d3464d2a2560233b1bff108cc5563df009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10909206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c4eb9669610892376f2a3886a0c6e7b61fc0f2c5d3f740abe33e501f3f184c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:37:22 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:37:22 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:37:22 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='72b5841a019f6c5a0be78d3cf21cd293446317e6b4e769e3b9d72090f2d87afc' ;;     armhf) natsArch='arm6'; sha256='eb159297eb8539e47f615180b1de759e6a735cfe3274a31d405301e1c2ee2aec' ;;     armv7) natsArch='arm7'; sha256='2573d1cb723f55d81c58e854e63c771e1a2d954a91ed0a23042e7e38fa0d405c' ;;     x86_64) natsArch='amd64'; sha256='b126515225aa2265a0088e0170f2a9de4c7880b2388cc7584aa77859ce831e3f' ;;     x86) natsArch='386'; sha256='c29a867045b25e300e501101abc3714e4e56c89b35b90ddbfc55ec6e7928eb17' ;;     s390x) natsArch='s390x'; sha256='d508d9f40853828623b50e367a4dd0394361352195b3669d5da7966991e30c03' ;;     ppc64le) natsArch='ppc64le'; sha256='a2dcbabba4aede66b9939d59e829d61417fffa7c08c49635b9a550a23f733cdc' ;;     loong64) natsArch='loong64'; sha256='5a0347fa1400a569cc798da80001fca8c68dc7193daea334df9ea6ec5fe2649c' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:37:22 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:37:22 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:37:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:37:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:37:22 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785afd645f29603dfc502b5aed95092773a9d75614d744ab69f3c90a491db958`  
		Last Modified: Wed, 20 May 2026 18:37:27 GMT  
		Size: 7.1 MB (7100047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2f75731780f4bdd6e4465ff6aedcfb784f2e04de6f7f593183a54df15a238b`  
		Last Modified: Wed, 20 May 2026 18:37:26 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea647ca93a5f93dd0481e42085d112026c222e13018b23f940c1798f150ddfc1`  
		Last Modified: Wed, 20 May 2026 18:37:27 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:c8082807e13d0ed6d2ad0cebcad6ff56b3a50637c7121d851c85bc76d43e51db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d6c6f5b5e660ea789920f5dadbe9d69a4b9c17b3cb539f1ad32abfe974a8016`

```dockerfile
```

-	Layers:
	-	`sha256:d118d5c6f5a5b003d23105ccb683ce7cbca22c58923371c7a4cad24bb2a0fa7a`  
		Last Modified: Wed, 20 May 2026 18:37:27 GMT  
		Size: 14.2 KB (14204 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:6ca666c2519ce831880fc65291a7ba5e6bdde44f1fce5826695e03943924c735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10347662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae81b57a35e9f65ea23549d2183c2c2e7ca7d50ce3f5036fa062e1cafaf518d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:36:19 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:36:19 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:36:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='72b5841a019f6c5a0be78d3cf21cd293446317e6b4e769e3b9d72090f2d87afc' ;;     armhf) natsArch='arm6'; sha256='eb159297eb8539e47f615180b1de759e6a735cfe3274a31d405301e1c2ee2aec' ;;     armv7) natsArch='arm7'; sha256='2573d1cb723f55d81c58e854e63c771e1a2d954a91ed0a23042e7e38fa0d405c' ;;     x86_64) natsArch='amd64'; sha256='b126515225aa2265a0088e0170f2a9de4c7880b2388cc7584aa77859ce831e3f' ;;     x86) natsArch='386'; sha256='c29a867045b25e300e501101abc3714e4e56c89b35b90ddbfc55ec6e7928eb17' ;;     s390x) natsArch='s390x'; sha256='d508d9f40853828623b50e367a4dd0394361352195b3669d5da7966991e30c03' ;;     ppc64le) natsArch='ppc64le'; sha256='a2dcbabba4aede66b9939d59e829d61417fffa7c08c49635b9a550a23f733cdc' ;;     loong64) natsArch='loong64'; sha256='5a0347fa1400a569cc798da80001fca8c68dc7193daea334df9ea6ec5fe2649c' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:36:19 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:36:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:36:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:36:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:36:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2912b40ddee494992b06ce6cfb3fe8dcb65d8de1892afcc94917eca78b7d9a0e`  
		Last Modified: Wed, 20 May 2026 18:36:24 GMT  
		Size: 6.8 MB (6839309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c4d072278e3126931517cbe8b2c9ef7cb6deb74558f56fedca986a5290a04c`  
		Last Modified: Wed, 20 May 2026 18:36:24 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f197927573b1036dd0f62c1a4cc9744836b24dbc6a2f4de557bdc47a30ce8be`  
		Last Modified: Wed, 20 May 2026 18:36:23 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:c61ccd3efdac690b485d840b7dfeceda69959a897f80949d0526c35a457cf1f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eecbe0cf18d59940e35cb0d2a6250eef69ca91a9543eb363af073473e44f86c`

```dockerfile
```

-	Layers:
	-	`sha256:18009424a0cc1065f3e1eef0bf7339139ef37661b11ace35f1b5949d76f335d9`  
		Last Modified: Wed, 20 May 2026 18:36:23 GMT  
		Size: 14.3 KB (14284 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:bcaff37bbf2a1f726cb43e74fe7db6b6e753a949c6083b2822d18e14da85ca0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10055590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd657e711d296590c867eb7ef48b021588d25b86bfad505ec5ae8cde2ec1d1d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:36:15 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:36:15 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:36:15 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='72b5841a019f6c5a0be78d3cf21cd293446317e6b4e769e3b9d72090f2d87afc' ;;     armhf) natsArch='arm6'; sha256='eb159297eb8539e47f615180b1de759e6a735cfe3274a31d405301e1c2ee2aec' ;;     armv7) natsArch='arm7'; sha256='2573d1cb723f55d81c58e854e63c771e1a2d954a91ed0a23042e7e38fa0d405c' ;;     x86_64) natsArch='amd64'; sha256='b126515225aa2265a0088e0170f2a9de4c7880b2388cc7584aa77859ce831e3f' ;;     x86) natsArch='386'; sha256='c29a867045b25e300e501101abc3714e4e56c89b35b90ddbfc55ec6e7928eb17' ;;     s390x) natsArch='s390x'; sha256='d508d9f40853828623b50e367a4dd0394361352195b3669d5da7966991e30c03' ;;     ppc64le) natsArch='ppc64le'; sha256='a2dcbabba4aede66b9939d59e829d61417fffa7c08c49635b9a550a23f733cdc' ;;     loong64) natsArch='loong64'; sha256='5a0347fa1400a569cc798da80001fca8c68dc7193daea334df9ea6ec5fe2649c' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:36:15 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:36:15 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:36:15 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:36:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:36:15 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc50b4a871d38a0cadde4ed4e424bc2187dfef3cd7b5af2f61d284f5000115cd`  
		Last Modified: Wed, 20 May 2026 18:36:20 GMT  
		Size: 6.8 MB (6828786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9549ff00bf4e47e9e775e46e3309a6c2d758382c50d7296865843e1034afe6dc`  
		Last Modified: Wed, 20 May 2026 18:36:20 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519ec8720496ec12b71688a575e86930c39ad7b2f5f12bc6e1ea5efa4b6ed815`  
		Last Modified: Wed, 20 May 2026 18:36:20 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:c35fea02bd550591fb78b42bc3e5316a3ce215f434775a80bfb9160fbd852a30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64701b345d4b8c5c56c71be078a3da0398507cd26e5919d9645432b5788339d9`

```dockerfile
```

-	Layers:
	-	`sha256:98625cfe5efdb1372a3b79cc98481ba6088f0d689b3566d4b9137f4ae7c4e389`  
		Last Modified: Wed, 20 May 2026 18:36:20 GMT  
		Size: 14.3 KB (14284 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d5e2a634247e27b59ccf258b33f626c0f5949b96b737536496b562f06b7e094c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10642176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80fc2db9d5bb25035d90c05c366a4658fad874a40ee451f2a41188d4f6ead80b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:37:06 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:37:06 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:37:06 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='72b5841a019f6c5a0be78d3cf21cd293446317e6b4e769e3b9d72090f2d87afc' ;;     armhf) natsArch='arm6'; sha256='eb159297eb8539e47f615180b1de759e6a735cfe3274a31d405301e1c2ee2aec' ;;     armv7) natsArch='arm7'; sha256='2573d1cb723f55d81c58e854e63c771e1a2d954a91ed0a23042e7e38fa0d405c' ;;     x86_64) natsArch='amd64'; sha256='b126515225aa2265a0088e0170f2a9de4c7880b2388cc7584aa77859ce831e3f' ;;     x86) natsArch='386'; sha256='c29a867045b25e300e501101abc3714e4e56c89b35b90ddbfc55ec6e7928eb17' ;;     s390x) natsArch='s390x'; sha256='d508d9f40853828623b50e367a4dd0394361352195b3669d5da7966991e30c03' ;;     ppc64le) natsArch='ppc64le'; sha256='a2dcbabba4aede66b9939d59e829d61417fffa7c08c49635b9a550a23f733cdc' ;;     loong64) natsArch='loong64'; sha256='5a0347fa1400a569cc798da80001fca8c68dc7193daea334df9ea6ec5fe2649c' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:37:06 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:37:06 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:37:06 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:37:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:37:06 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ff339b51fb101889997a78aaa1897c82810b93750d3c1fad2c9939c172510d`  
		Last Modified: Wed, 20 May 2026 18:37:11 GMT  
		Size: 6.5 MB (6499312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01cdeeebd5372e1dc9a2c97c853e72b20a3622eed3457557f5913caa2b335da1`  
		Last Modified: Wed, 20 May 2026 18:37:11 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1624ccef5078119f6ce1d17ffcdd69ee710740b23ed841fbd209e80c8b6f3032`  
		Last Modified: Wed, 20 May 2026 18:37:11 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:d2b097ebfadc88817dcda244513c1536ee40a0fe3e24f28e6094d7eddf30a9ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:195c6c70cb97e0570c5672af8dc9c1b933cc356306a6daae576ac7e92b55ee69`

```dockerfile
```

-	Layers:
	-	`sha256:9145327976083751cab916e93d4003480e2bc0b428d04a554617da1720ba9788`  
		Last Modified: Wed, 20 May 2026 18:37:11 GMT  
		Size: 14.3 KB (14308 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:2e2a8c50a862185aabb439c2fe0736bf976ac4f14f840192f46ada06908ec62b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10295179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6684ad61a65a2f9bf995f867d9d9d9b78d57e72ecbac3ca56cb56b6e407e0ad6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:39:54 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:39:54 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:39:54 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='72b5841a019f6c5a0be78d3cf21cd293446317e6b4e769e3b9d72090f2d87afc' ;;     armhf) natsArch='arm6'; sha256='eb159297eb8539e47f615180b1de759e6a735cfe3274a31d405301e1c2ee2aec' ;;     armv7) natsArch='arm7'; sha256='2573d1cb723f55d81c58e854e63c771e1a2d954a91ed0a23042e7e38fa0d405c' ;;     x86_64) natsArch='amd64'; sha256='b126515225aa2265a0088e0170f2a9de4c7880b2388cc7584aa77859ce831e3f' ;;     x86) natsArch='386'; sha256='c29a867045b25e300e501101abc3714e4e56c89b35b90ddbfc55ec6e7928eb17' ;;     s390x) natsArch='s390x'; sha256='d508d9f40853828623b50e367a4dd0394361352195b3669d5da7966991e30c03' ;;     ppc64le) natsArch='ppc64le'; sha256='a2dcbabba4aede66b9939d59e829d61417fffa7c08c49635b9a550a23f733cdc' ;;     loong64) natsArch='loong64'; sha256='5a0347fa1400a569cc798da80001fca8c68dc7193daea334df9ea6ec5fe2649c' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:39:55 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:39:55 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:39:55 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:39:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:39:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe0b03709a632c9f299b1ef2c2691c1b292ae9f333a7b2083a9b51162a19669`  
		Last Modified: Wed, 20 May 2026 18:40:02 GMT  
		Size: 6.6 MB (6557551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3c6e5710602d0c65abfcc3a4aac8676e3cd1f849d5967bee0654b0ec045abe`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0fcc4ed5f0f4848feb91f0e5c409cb87bfd693a7056f2c0e574dbf0fc8ff4ab`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:5b7ba3b09bf23127b1a75c412fb6e5e3fa773abda140a3f0e45600422968bf88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b9cec962a037f640085142478803038714db7fa629a4b7e6cad1c2f41371943`

```dockerfile
```

-	Layers:
	-	`sha256:bc2e73ad0cbc0cad27f1667939617eb3a7d77a3ba7dd6d70917518d2ee4fed7f`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 14.2 KB (14248 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:ce14e245951893e72e72ac26599d178e07af3e24fd01a857cc00c484fee718cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10603715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0f596aa7cbe6e6e80f8063aae3852a811f7045c570a2bf4e89c6b1c0a0d596f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:48:37 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:48:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:48:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='72b5841a019f6c5a0be78d3cf21cd293446317e6b4e769e3b9d72090f2d87afc' ;;     armhf) natsArch='arm6'; sha256='eb159297eb8539e47f615180b1de759e6a735cfe3274a31d405301e1c2ee2aec' ;;     armv7) natsArch='arm7'; sha256='2573d1cb723f55d81c58e854e63c771e1a2d954a91ed0a23042e7e38fa0d405c' ;;     x86_64) natsArch='amd64'; sha256='b126515225aa2265a0088e0170f2a9de4c7880b2388cc7584aa77859ce831e3f' ;;     x86) natsArch='386'; sha256='c29a867045b25e300e501101abc3714e4e56c89b35b90ddbfc55ec6e7928eb17' ;;     s390x) natsArch='s390x'; sha256='d508d9f40853828623b50e367a4dd0394361352195b3669d5da7966991e30c03' ;;     ppc64le) natsArch='ppc64le'; sha256='a2dcbabba4aede66b9939d59e829d61417fffa7c08c49635b9a550a23f733cdc' ;;     loong64) natsArch='loong64'; sha256='5a0347fa1400a569cc798da80001fca8c68dc7193daea334df9ea6ec5fe2649c' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:48:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:48:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:48:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:48:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:48:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13002ceadd3c101c2cfaa462d93d68f1056f8fd0453fd99269b12c624bc6b38a`  
		Last Modified: Wed, 20 May 2026 18:49:13 GMT  
		Size: 6.9 MB (6948871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdaa4e64de2e200c41440e78516f3fbbcf03b5b5e18cb05b20a63bd1661ce87d`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d69a6bdd10e86979de515f61b8c590bea15507a88f17e4f5a7f57ddfac937e`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:92726e2db0802623d76696809568374f168d11a6eb505249100949eb89a74c6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a1345efb532a7d2fa604c74539fdd13035a959493b0f11f0e962227e91cfe8e`

```dockerfile
```

-	Layers:
	-	`sha256:afc92f71ec0a9bc07c23a3ff65bc6f32afe90cfc974b6e23b25a06cab13804fd`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 14.2 KB (14204 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12-linux`

```console
$ docker pull nats@sha256:ee9a8f12f3a0d9c2b26f6d16a5f1867f851d21f1acde6d5ae2b75570efe5cdb3
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

### `nats:2.12-linux` - linux; amd64

```console
$ docker pull nats@sha256:81dd79785518efd999b91f95c3704444c73865f457c195dbc2a7ca54f9e82b9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6643802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eee8ee507e1167111022248b38dc79952282435780aa5561a54272070231fba`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:10:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:10:49 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:10:49 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:10:49 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:10:49 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:10:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e5e76f67b303999883527fbb9d2827bb20bf4266bd14b30fe193b9c837d56b9`  
		Last Modified: Wed, 20 May 2026 16:04:23 GMT  
		Size: 6.6 MB (6643293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a25302c76354939bc63896b8a3c3e531819ed31d7c3fabed2c21912ed5a778a`  
		Last Modified: Wed, 20 May 2026 19:10:53 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:63bdef746f1bd984ed04788dbb4683d8899fde6b501588af9d034679f4d5c4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e9d8d10730cd5f5322c955e5243b4f410f4f61622f7e434b533f38cbfa8b9bd`

```dockerfile
```

-	Layers:
	-	`sha256:29922663c3486deec187939e4f05d87cecd02dbb505dadb59cab3b9b718aa068`  
		Last Modified: Wed, 20 May 2026 19:10:53 GMT  
		Size: 8.7 KB (8660 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:697254950318448b92489577435eb73db46ad779dfa5bb8312950fcbcf774fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6383827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e55c4a455573962fac86f8a167ca43e89be66b7799b10d76e5465fdf00ffdf7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:09:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:09:39 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:09:39 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:09:39 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:09:39 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:09:39 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c10d60a8ee2ca1e386312db0a0b2473313d36b33da2c5a1eed45d3dbc145b255`  
		Last Modified: Wed, 20 May 2026 16:04:26 GMT  
		Size: 6.4 MB (6383319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1d283fe91c0f3527ed49fb1f312ae136b8fb1cab01bd902b22c0a912727bc7`  
		Last Modified: Wed, 20 May 2026 19:09:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:cc69b4de3ae7531530b6ae76912d528339157b572f0c822676897fac26e728d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08a5b8c8548b84e96f500c4ee6700a282c92ebc58d03b35f1d49ab5424ba360d`

```dockerfile
```

-	Layers:
	-	`sha256:bf6a20cdeb4777f1f89bf3b91149fbb9cd5193d460d2720e5856bc2a69d08a65`  
		Last Modified: Wed, 20 May 2026 19:09:43 GMT  
		Size: 8.7 KB (8744 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:a2d058ffac3e0982c4263c4a98357898b61eca619d2c56a76aac7b9f2d18f171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6373077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:130977b1791d287860791cbc0f238f4bf8902acceeb859fc8663ca013fc90b15`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:09:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:09:50 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:09:50 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:09:50 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:09:50 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:09:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:efec7643648fe287ed0901613783bcd23bb5a8b7b2fb2aee2e9f58a8d0d8d7a8`  
		Last Modified: Wed, 20 May 2026 16:04:26 GMT  
		Size: 6.4 MB (6372568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af920700845e87c0ae0d0a2e002936cf3fe153e0d75cd8d28e1fdebe0951676c`  
		Last Modified: Wed, 20 May 2026 19:09:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:a96c4eefe96a686ef87c6963d464d87de0be9f9d27e2e065a01137de83f6f1ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f334115d58195d99db72b89b7cd06f5d63fbbfe2344d46642d5e03925960c426`

```dockerfile
```

-	Layers:
	-	`sha256:44bb6f0b5261e2b3668d54d1d0f788b8e18dd4e2ba44ef27c0949c43398854e9`  
		Last Modified: Wed, 20 May 2026 19:09:54 GMT  
		Size: 8.7 KB (8744 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:aa8f7e3d55a383e35f019c28b6c432ed2090b3dad56fead3e7a70ab1dba79ccc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6037707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1b69482ef45b939a2908e033d22c9582db2b53dac733301472ace541c756069`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:10:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:10:14 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:10:14 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:10:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:10:14 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:10:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:81af0467f4bfb473e50c712e06ca48adff2e7aab8456b45fcfbc3fefe8ef6df7`  
		Last Modified: Wed, 20 May 2026 16:04:24 GMT  
		Size: 6.0 MB (6037200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed22b68f9def9c87dfb1c5a9ec34a809caf385bcdfdd456fd3be55b553020ad`  
		Last Modified: Wed, 20 May 2026 19:10:19 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:534c5df88f202c2a015c845378127d701cc4faf3641326573fce6c0fd64dbd1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0a9c9217edbec11dd3120e94f789339bb631670a66be81de8e106830fef4b4`

```dockerfile
```

-	Layers:
	-	`sha256:743146aaf7c71f426d7abd3b4db2abcd72ecfd72aed9db12cb025a3148324d81`  
		Last Modified: Wed, 20 May 2026 19:10:19 GMT  
		Size: 8.8 KB (8774 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:3a024c2519d3e8d9afa913cc70dc8a08f42c27841b819c13ae7f4746791667f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6100417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a86f1bedebf55c136505a6a6115d4879fd94839c05722c2813b743b911513fc7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:09:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:09:00 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:09:00 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:09:00 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:09:00 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:09:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8d94981a1be7de02d7553ad09e31ec60ee268df51c2ef4762da5828b6b45674`  
		Last Modified: Wed, 20 May 2026 16:04:23 GMT  
		Size: 6.1 MB (6099908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb234fae2f8c35c37c5a0a2b27b551816540b8c513f6b2c479728b77a462cc5`  
		Last Modified: Wed, 20 May 2026 19:09:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:4bc8adf9c89eb891276d88ad9ef5302e83c23305ea4eee6318fdf94156bf00f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c21faa8dd4d3dbf3346283035cadd5da1c813c60749a515846c980e8940f08d8`

```dockerfile
```

-	Layers:
	-	`sha256:dd4e6d8e65f686896f2c04a5c31ca21c193b8ac222cbaa55fc6cf1e4ecbc68d7`  
		Last Modified: Wed, 20 May 2026 19:09:06 GMT  
		Size: 8.7 KB (8715 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; s390x

```console
$ docker pull nats@sha256:0ff65b369dcf8b26046db1efa962fef20887641c137fba88592e99ac6d946759
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6491050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1fbd0e893d6064d2ae64507740f42429bfd8b6626f01ff155f71d68cbac6dfe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:10:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:10:29 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:10:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:10:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:10:30 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:10:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d668ec0d13619d02b98ac6e2ab2bb7ca3974ad1ed964fbbfae78e23a777df473`  
		Last Modified: Wed, 20 May 2026 16:04:26 GMT  
		Size: 6.5 MB (6490542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5c187c9ced3347b391d712fe3353958272e09460e48ef72b492e55332f67a0`  
		Last Modified: Wed, 20 May 2026 19:10:48 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:6868356eb5df018325b032eca1a4d9471a915135b6ad01baf74cbed5245b7581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74a49ccc3dc2aca4a464c76934f3739fa2e4fdbc49a4fe3a93d58e620431eba9`

```dockerfile
```

-	Layers:
	-	`sha256:beed34e5caa7d0f8bb8e9624e6acbd693112ad713d81a6ebe9751d3d4a144a83`  
		Last Modified: Wed, 20 May 2026 19:10:48 GMT  
		Size: 8.7 KB (8661 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12-nanoserver`

```console
$ docker pull nats@sha256:6d72ba1561be987809ce565415cbaf51c83f70b06f4d54d31d8213416b2581e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2.12-nanoserver` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:b5f413bd3b0f768cdcfb88471ef7dd7e1e8979c00517fecb6fec681e1ff658dc
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133878103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14eeb0f5e1235887ceab95fb27b69b508faa0a9be7ec8654eb6483d61bd87539`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 20 May 2026 19:09:14 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 20 May 2026 19:09:43 GMT
RUN cmd /S /C #(nop) COPY file:dd9132ddd79eef4f3cbcb173e3b4c47616b6109b67b3da726ffcf5aa0546dfe6 in C:\nats-server.exe 
# Wed, 20 May 2026 19:09:44 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 20 May 2026 19:09:44 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 20 May 2026 19:09:44 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 20 May 2026 19:09:45 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c815e3255991cc2df065c98a27664be46d8b5db04231449f637ecaf64c5c098f`  
		Last Modified: Wed, 20 May 2026 19:09:24 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0584329bf51b06503599bd12d61e5b4b8022e17567c5a00bf044a36fec53f6ca`  
		Last Modified: Wed, 20 May 2026 19:09:54 GMT  
		Size: 6.8 MB (6833293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42502c403069fbf82a9dfaead168b2b5f649366919a105dc982b8388c2da2055`  
		Last Modified: Wed, 20 May 2026 19:09:49 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f632ce4ec8c46651a30b231de5b71039037abbc82f1bede845e302e0a576a256`  
		Last Modified: Wed, 20 May 2026 19:09:49 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceaf1e7278afa4664b03b5df7ba7fb9043b402be47232554b124a56a1c85927c`  
		Last Modified: Wed, 20 May 2026 19:09:49 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d4067da1a0ad2b0d46b1f5bbaebefcfeb420dbac588629c9d392f95f7723d4`  
		Last Modified: Wed, 20 May 2026 19:09:49 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:6d72ba1561be987809ce565415cbaf51c83f70b06f4d54d31d8213416b2581e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2.12-nanoserver-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:b5f413bd3b0f768cdcfb88471ef7dd7e1e8979c00517fecb6fec681e1ff658dc
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133878103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14eeb0f5e1235887ceab95fb27b69b508faa0a9be7ec8654eb6483d61bd87539`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 20 May 2026 19:09:14 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 20 May 2026 19:09:43 GMT
RUN cmd /S /C #(nop) COPY file:dd9132ddd79eef4f3cbcb173e3b4c47616b6109b67b3da726ffcf5aa0546dfe6 in C:\nats-server.exe 
# Wed, 20 May 2026 19:09:44 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 20 May 2026 19:09:44 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 20 May 2026 19:09:44 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 20 May 2026 19:09:45 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c815e3255991cc2df065c98a27664be46d8b5db04231449f637ecaf64c5c098f`  
		Last Modified: Wed, 20 May 2026 19:09:24 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0584329bf51b06503599bd12d61e5b4b8022e17567c5a00bf044a36fec53f6ca`  
		Last Modified: Wed, 20 May 2026 19:09:54 GMT  
		Size: 6.8 MB (6833293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42502c403069fbf82a9dfaead168b2b5f649366919a105dc982b8388c2da2055`  
		Last Modified: Wed, 20 May 2026 19:09:49 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f632ce4ec8c46651a30b231de5b71039037abbc82f1bede845e302e0a576a256`  
		Last Modified: Wed, 20 May 2026 19:09:49 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceaf1e7278afa4664b03b5df7ba7fb9043b402be47232554b124a56a1c85927c`  
		Last Modified: Wed, 20 May 2026 19:09:49 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d4067da1a0ad2b0d46b1f5bbaebefcfeb420dbac588629c9d392f95f7723d4`  
		Last Modified: Wed, 20 May 2026 19:09:49 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12-scratch`

```console
$ docker pull nats@sha256:ee9a8f12f3a0d9c2b26f6d16a5f1867f851d21f1acde6d5ae2b75570efe5cdb3
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

### `nats:2.12-scratch` - linux; amd64

```console
$ docker pull nats@sha256:81dd79785518efd999b91f95c3704444c73865f457c195dbc2a7ca54f9e82b9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6643802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eee8ee507e1167111022248b38dc79952282435780aa5561a54272070231fba`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:10:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:10:49 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:10:49 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:10:49 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:10:49 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:10:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e5e76f67b303999883527fbb9d2827bb20bf4266bd14b30fe193b9c837d56b9`  
		Last Modified: Wed, 20 May 2026 16:04:23 GMT  
		Size: 6.6 MB (6643293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a25302c76354939bc63896b8a3c3e531819ed31d7c3fabed2c21912ed5a778a`  
		Last Modified: Wed, 20 May 2026 19:10:53 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:63bdef746f1bd984ed04788dbb4683d8899fde6b501588af9d034679f4d5c4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e9d8d10730cd5f5322c955e5243b4f410f4f61622f7e434b533f38cbfa8b9bd`

```dockerfile
```

-	Layers:
	-	`sha256:29922663c3486deec187939e4f05d87cecd02dbb505dadb59cab3b9b718aa068`  
		Last Modified: Wed, 20 May 2026 19:10:53 GMT  
		Size: 8.7 KB (8660 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:697254950318448b92489577435eb73db46ad779dfa5bb8312950fcbcf774fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6383827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e55c4a455573962fac86f8a167ca43e89be66b7799b10d76e5465fdf00ffdf7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:09:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:09:39 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:09:39 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:09:39 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:09:39 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:09:39 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c10d60a8ee2ca1e386312db0a0b2473313d36b33da2c5a1eed45d3dbc145b255`  
		Last Modified: Wed, 20 May 2026 16:04:26 GMT  
		Size: 6.4 MB (6383319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1d283fe91c0f3527ed49fb1f312ae136b8fb1cab01bd902b22c0a912727bc7`  
		Last Modified: Wed, 20 May 2026 19:09:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:cc69b4de3ae7531530b6ae76912d528339157b572f0c822676897fac26e728d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08a5b8c8548b84e96f500c4ee6700a282c92ebc58d03b35f1d49ab5424ba360d`

```dockerfile
```

-	Layers:
	-	`sha256:bf6a20cdeb4777f1f89bf3b91149fbb9cd5193d460d2720e5856bc2a69d08a65`  
		Last Modified: Wed, 20 May 2026 19:09:43 GMT  
		Size: 8.7 KB (8744 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:a2d058ffac3e0982c4263c4a98357898b61eca619d2c56a76aac7b9f2d18f171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6373077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:130977b1791d287860791cbc0f238f4bf8902acceeb859fc8663ca013fc90b15`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:09:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:09:50 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:09:50 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:09:50 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:09:50 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:09:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:efec7643648fe287ed0901613783bcd23bb5a8b7b2fb2aee2e9f58a8d0d8d7a8`  
		Last Modified: Wed, 20 May 2026 16:04:26 GMT  
		Size: 6.4 MB (6372568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af920700845e87c0ae0d0a2e002936cf3fe153e0d75cd8d28e1fdebe0951676c`  
		Last Modified: Wed, 20 May 2026 19:09:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:a96c4eefe96a686ef87c6963d464d87de0be9f9d27e2e065a01137de83f6f1ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f334115d58195d99db72b89b7cd06f5d63fbbfe2344d46642d5e03925960c426`

```dockerfile
```

-	Layers:
	-	`sha256:44bb6f0b5261e2b3668d54d1d0f788b8e18dd4e2ba44ef27c0949c43398854e9`  
		Last Modified: Wed, 20 May 2026 19:09:54 GMT  
		Size: 8.7 KB (8744 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:aa8f7e3d55a383e35f019c28b6c432ed2090b3dad56fead3e7a70ab1dba79ccc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6037707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1b69482ef45b939a2908e033d22c9582db2b53dac733301472ace541c756069`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:10:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:10:14 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:10:14 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:10:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:10:14 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:10:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:81af0467f4bfb473e50c712e06ca48adff2e7aab8456b45fcfbc3fefe8ef6df7`  
		Last Modified: Wed, 20 May 2026 16:04:24 GMT  
		Size: 6.0 MB (6037200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed22b68f9def9c87dfb1c5a9ec34a809caf385bcdfdd456fd3be55b553020ad`  
		Last Modified: Wed, 20 May 2026 19:10:19 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:534c5df88f202c2a015c845378127d701cc4faf3641326573fce6c0fd64dbd1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0a9c9217edbec11dd3120e94f789339bb631670a66be81de8e106830fef4b4`

```dockerfile
```

-	Layers:
	-	`sha256:743146aaf7c71f426d7abd3b4db2abcd72ecfd72aed9db12cb025a3148324d81`  
		Last Modified: Wed, 20 May 2026 19:10:19 GMT  
		Size: 8.8 KB (8774 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:3a024c2519d3e8d9afa913cc70dc8a08f42c27841b819c13ae7f4746791667f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6100417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a86f1bedebf55c136505a6a6115d4879fd94839c05722c2813b743b911513fc7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:09:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:09:00 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:09:00 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:09:00 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:09:00 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:09:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8d94981a1be7de02d7553ad09e31ec60ee268df51c2ef4762da5828b6b45674`  
		Last Modified: Wed, 20 May 2026 16:04:23 GMT  
		Size: 6.1 MB (6099908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb234fae2f8c35c37c5a0a2b27b551816540b8c513f6b2c479728b77a462cc5`  
		Last Modified: Wed, 20 May 2026 19:09:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:4bc8adf9c89eb891276d88ad9ef5302e83c23305ea4eee6318fdf94156bf00f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c21faa8dd4d3dbf3346283035cadd5da1c813c60749a515846c980e8940f08d8`

```dockerfile
```

-	Layers:
	-	`sha256:dd4e6d8e65f686896f2c04a5c31ca21c193b8ac222cbaa55fc6cf1e4ecbc68d7`  
		Last Modified: Wed, 20 May 2026 19:09:06 GMT  
		Size: 8.7 KB (8715 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; s390x

```console
$ docker pull nats@sha256:0ff65b369dcf8b26046db1efa962fef20887641c137fba88592e99ac6d946759
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6491050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1fbd0e893d6064d2ae64507740f42429bfd8b6626f01ff155f71d68cbac6dfe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:10:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:10:29 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:10:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:10:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:10:30 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:10:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d668ec0d13619d02b98ac6e2ab2bb7ca3974ad1ed964fbbfae78e23a777df473`  
		Last Modified: Wed, 20 May 2026 16:04:26 GMT  
		Size: 6.5 MB (6490542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5c187c9ced3347b391d712fe3353958272e09460e48ef72b492e55332f67a0`  
		Last Modified: Wed, 20 May 2026 19:10:48 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:6868356eb5df018325b032eca1a4d9471a915135b6ad01baf74cbed5245b7581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74a49ccc3dc2aca4a464c76934f3739fa2e4fdbc49a4fe3a93d58e620431eba9`

```dockerfile
```

-	Layers:
	-	`sha256:beed34e5caa7d0f8bb8e9624e6acbd693112ad713d81a6ebe9751d3d4a144a83`  
		Last Modified: Wed, 20 May 2026 19:10:48 GMT  
		Size: 8.7 KB (8661 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12-windowsservercore`

```console
$ docker pull nats@sha256:93d7e77dc19ae1d7f04e86c2068da9a3b9e437892b266e13c64f28e1773223b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2.12-windowsservercore` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:e9d6a938ace06e341a366fc78d12f5aa1bd956dac71e4ff82158cb9eb81ac4c4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2130120651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1df05498b147c8f9c4865e19eb3f2266e06494384130ac34c45806311beb604`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Wed, 20 May 2026 18:42:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 20 May 2026 18:42:48 GMT
ENV NATS_DOCKERIZED=1
# Wed, 20 May 2026 18:59:48 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:59:48 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:59:50 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.9/nats-server-v2.12.9-windows-amd64.zip
# Wed, 20 May 2026 18:59:51 GMT
ENV NATS_SERVER_SHASUM=6d8d0b31ba2fbaca4613b9dbb1fd107c335ee26485f59fb9006e7ab34913117d
# Wed, 20 May 2026 18:59:59 GMT
RUN Set-PSDebug -Trace 2
# Wed, 20 May 2026 19:00:21 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 20 May 2026 19:00:22 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 20 May 2026 19:00:22 GMT
EXPOSE 4222 6222 8222
# Wed, 20 May 2026 19:00:23 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 20 May 2026 19:00:23 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9541aea3e55bd746462fb4c6e57da81839bbdd92cde8c45bec531dc275c949`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acaeb80d5acbf745ec935e19b9c27aac2c1c36569184a441931640832febb401`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f31a04aebe50db6f85e58a4df9a8d34f7df2bf36b2a1485ac21d1af7127d32c`  
		Last Modified: Wed, 20 May 2026 19:00:32 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c32221a695427881403603d85b9fbe9a208cafa19e27db15a2a87080b977aeb`  
		Last Modified: Wed, 20 May 2026 19:00:30 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fb78dc8e8b1e6679429c94711da7ef1a170469e7abd593d612090cbeabfc2ce`  
		Last Modified: Wed, 20 May 2026 19:00:30 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb3ca19f5131d5dac1c4bad13e5c900a1330ded4bc79991da462281aa3992a2a`  
		Last Modified: Wed, 20 May 2026 19:00:29 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67bc96c36328bd4cc9410563bf01b2c2ecae49584ea178bdb62d7b45109d586`  
		Last Modified: Wed, 20 May 2026 19:00:30 GMT  
		Size: 494.4 KB (494434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2a8ebf88f3c30a60da7b6608197c202a69ce7dd0ab6be014efbf6eadd2349f`  
		Last Modified: Wed, 20 May 2026 19:00:33 GMT  
		Size: 7.2 MB (7192011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e190bfa12df85ab9f289b0804e966103ffc0c26626f2c50e1a7409f5e5ed0855`  
		Last Modified: Wed, 20 May 2026 19:00:27 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7ce3c10c5a9944c33f1b695b2a9f04297226593bbaef9f132405493388c24c`  
		Last Modified: Wed, 20 May 2026 19:00:27 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6f580a22501d26e28952ee85653f70663980ab45953d0cfcbef50694db04d6`  
		Last Modified: Wed, 20 May 2026 19:00:28 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af4511ea5948cbca6aef9d7517e123f726b38c8a0eb9c947c2c4f6d7f54e0d88`  
		Last Modified: Wed, 20 May 2026 19:00:28 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:93d7e77dc19ae1d7f04e86c2068da9a3b9e437892b266e13c64f28e1773223b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2.12-windowsservercore-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:e9d6a938ace06e341a366fc78d12f5aa1bd956dac71e4ff82158cb9eb81ac4c4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2130120651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1df05498b147c8f9c4865e19eb3f2266e06494384130ac34c45806311beb604`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Wed, 20 May 2026 18:42:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 20 May 2026 18:42:48 GMT
ENV NATS_DOCKERIZED=1
# Wed, 20 May 2026 18:59:48 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:59:48 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:59:50 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.9/nats-server-v2.12.9-windows-amd64.zip
# Wed, 20 May 2026 18:59:51 GMT
ENV NATS_SERVER_SHASUM=6d8d0b31ba2fbaca4613b9dbb1fd107c335ee26485f59fb9006e7ab34913117d
# Wed, 20 May 2026 18:59:59 GMT
RUN Set-PSDebug -Trace 2
# Wed, 20 May 2026 19:00:21 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 20 May 2026 19:00:22 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 20 May 2026 19:00:22 GMT
EXPOSE 4222 6222 8222
# Wed, 20 May 2026 19:00:23 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 20 May 2026 19:00:23 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9541aea3e55bd746462fb4c6e57da81839bbdd92cde8c45bec531dc275c949`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acaeb80d5acbf745ec935e19b9c27aac2c1c36569184a441931640832febb401`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f31a04aebe50db6f85e58a4df9a8d34f7df2bf36b2a1485ac21d1af7127d32c`  
		Last Modified: Wed, 20 May 2026 19:00:32 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c32221a695427881403603d85b9fbe9a208cafa19e27db15a2a87080b977aeb`  
		Last Modified: Wed, 20 May 2026 19:00:30 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fb78dc8e8b1e6679429c94711da7ef1a170469e7abd593d612090cbeabfc2ce`  
		Last Modified: Wed, 20 May 2026 19:00:30 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb3ca19f5131d5dac1c4bad13e5c900a1330ded4bc79991da462281aa3992a2a`  
		Last Modified: Wed, 20 May 2026 19:00:29 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67bc96c36328bd4cc9410563bf01b2c2ecae49584ea178bdb62d7b45109d586`  
		Last Modified: Wed, 20 May 2026 19:00:30 GMT  
		Size: 494.4 KB (494434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2a8ebf88f3c30a60da7b6608197c202a69ce7dd0ab6be014efbf6eadd2349f`  
		Last Modified: Wed, 20 May 2026 19:00:33 GMT  
		Size: 7.2 MB (7192011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e190bfa12df85ab9f289b0804e966103ffc0c26626f2c50e1a7409f5e5ed0855`  
		Last Modified: Wed, 20 May 2026 19:00:27 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7ce3c10c5a9944c33f1b695b2a9f04297226593bbaef9f132405493388c24c`  
		Last Modified: Wed, 20 May 2026 19:00:27 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6f580a22501d26e28952ee85653f70663980ab45953d0cfcbef50694db04d6`  
		Last Modified: Wed, 20 May 2026 19:00:28 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af4511ea5948cbca6aef9d7517e123f726b38c8a0eb9c947c2c4f6d7f54e0d88`  
		Last Modified: Wed, 20 May 2026 19:00:28 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12.9`

```console
$ docker pull nats@sha256:9dc953fcaefeec300a44f07cde52cc686823156c667bc27b2ee08adb7140f7a2
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
	-	windows version 10.0.20348.5139; amd64

### `nats:2.12.9` - linux; amd64

```console
$ docker pull nats@sha256:81dd79785518efd999b91f95c3704444c73865f457c195dbc2a7ca54f9e82b9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6643802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eee8ee507e1167111022248b38dc79952282435780aa5561a54272070231fba`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:10:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:10:49 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:10:49 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:10:49 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:10:49 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:10:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e5e76f67b303999883527fbb9d2827bb20bf4266bd14b30fe193b9c837d56b9`  
		Last Modified: Wed, 20 May 2026 16:04:23 GMT  
		Size: 6.6 MB (6643293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a25302c76354939bc63896b8a3c3e531819ed31d7c3fabed2c21912ed5a778a`  
		Last Modified: Wed, 20 May 2026 19:10:53 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.9` - unknown; unknown

```console
$ docker pull nats@sha256:63bdef746f1bd984ed04788dbb4683d8899fde6b501588af9d034679f4d5c4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e9d8d10730cd5f5322c955e5243b4f410f4f61622f7e434b533f38cbfa8b9bd`

```dockerfile
```

-	Layers:
	-	`sha256:29922663c3486deec187939e4f05d87cecd02dbb505dadb59cab3b9b718aa068`  
		Last Modified: Wed, 20 May 2026 19:10:53 GMT  
		Size: 8.7 KB (8660 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.9` - linux; arm variant v6

```console
$ docker pull nats@sha256:697254950318448b92489577435eb73db46ad779dfa5bb8312950fcbcf774fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6383827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e55c4a455573962fac86f8a167ca43e89be66b7799b10d76e5465fdf00ffdf7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:09:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:09:39 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:09:39 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:09:39 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:09:39 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:09:39 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c10d60a8ee2ca1e386312db0a0b2473313d36b33da2c5a1eed45d3dbc145b255`  
		Last Modified: Wed, 20 May 2026 16:04:26 GMT  
		Size: 6.4 MB (6383319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1d283fe91c0f3527ed49fb1f312ae136b8fb1cab01bd902b22c0a912727bc7`  
		Last Modified: Wed, 20 May 2026 19:09:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.9` - unknown; unknown

```console
$ docker pull nats@sha256:cc69b4de3ae7531530b6ae76912d528339157b572f0c822676897fac26e728d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08a5b8c8548b84e96f500c4ee6700a282c92ebc58d03b35f1d49ab5424ba360d`

```dockerfile
```

-	Layers:
	-	`sha256:bf6a20cdeb4777f1f89bf3b91149fbb9cd5193d460d2720e5856bc2a69d08a65`  
		Last Modified: Wed, 20 May 2026 19:09:43 GMT  
		Size: 8.7 KB (8744 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.9` - linux; arm variant v7

```console
$ docker pull nats@sha256:a2d058ffac3e0982c4263c4a98357898b61eca619d2c56a76aac7b9f2d18f171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6373077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:130977b1791d287860791cbc0f238f4bf8902acceeb859fc8663ca013fc90b15`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:09:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:09:50 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:09:50 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:09:50 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:09:50 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:09:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:efec7643648fe287ed0901613783bcd23bb5a8b7b2fb2aee2e9f58a8d0d8d7a8`  
		Last Modified: Wed, 20 May 2026 16:04:26 GMT  
		Size: 6.4 MB (6372568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af920700845e87c0ae0d0a2e002936cf3fe153e0d75cd8d28e1fdebe0951676c`  
		Last Modified: Wed, 20 May 2026 19:09:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.9` - unknown; unknown

```console
$ docker pull nats@sha256:a96c4eefe96a686ef87c6963d464d87de0be9f9d27e2e065a01137de83f6f1ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f334115d58195d99db72b89b7cd06f5d63fbbfe2344d46642d5e03925960c426`

```dockerfile
```

-	Layers:
	-	`sha256:44bb6f0b5261e2b3668d54d1d0f788b8e18dd4e2ba44ef27c0949c43398854e9`  
		Last Modified: Wed, 20 May 2026 19:09:54 GMT  
		Size: 8.7 KB (8744 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.9` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:aa8f7e3d55a383e35f019c28b6c432ed2090b3dad56fead3e7a70ab1dba79ccc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6037707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1b69482ef45b939a2908e033d22c9582db2b53dac733301472ace541c756069`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:10:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:10:14 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:10:14 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:10:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:10:14 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:10:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:81af0467f4bfb473e50c712e06ca48adff2e7aab8456b45fcfbc3fefe8ef6df7`  
		Last Modified: Wed, 20 May 2026 16:04:24 GMT  
		Size: 6.0 MB (6037200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed22b68f9def9c87dfb1c5a9ec34a809caf385bcdfdd456fd3be55b553020ad`  
		Last Modified: Wed, 20 May 2026 19:10:19 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.9` - unknown; unknown

```console
$ docker pull nats@sha256:534c5df88f202c2a015c845378127d701cc4faf3641326573fce6c0fd64dbd1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0a9c9217edbec11dd3120e94f789339bb631670a66be81de8e106830fef4b4`

```dockerfile
```

-	Layers:
	-	`sha256:743146aaf7c71f426d7abd3b4db2abcd72ecfd72aed9db12cb025a3148324d81`  
		Last Modified: Wed, 20 May 2026 19:10:19 GMT  
		Size: 8.8 KB (8774 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.9` - linux; ppc64le

```console
$ docker pull nats@sha256:3a024c2519d3e8d9afa913cc70dc8a08f42c27841b819c13ae7f4746791667f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6100417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a86f1bedebf55c136505a6a6115d4879fd94839c05722c2813b743b911513fc7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:09:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:09:00 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:09:00 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:09:00 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:09:00 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:09:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8d94981a1be7de02d7553ad09e31ec60ee268df51c2ef4762da5828b6b45674`  
		Last Modified: Wed, 20 May 2026 16:04:23 GMT  
		Size: 6.1 MB (6099908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb234fae2f8c35c37c5a0a2b27b551816540b8c513f6b2c479728b77a462cc5`  
		Last Modified: Wed, 20 May 2026 19:09:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.9` - unknown; unknown

```console
$ docker pull nats@sha256:4bc8adf9c89eb891276d88ad9ef5302e83c23305ea4eee6318fdf94156bf00f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c21faa8dd4d3dbf3346283035cadd5da1c813c60749a515846c980e8940f08d8`

```dockerfile
```

-	Layers:
	-	`sha256:dd4e6d8e65f686896f2c04a5c31ca21c193b8ac222cbaa55fc6cf1e4ecbc68d7`  
		Last Modified: Wed, 20 May 2026 19:09:06 GMT  
		Size: 8.7 KB (8715 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.9` - linux; s390x

```console
$ docker pull nats@sha256:0ff65b369dcf8b26046db1efa962fef20887641c137fba88592e99ac6d946759
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6491050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1fbd0e893d6064d2ae64507740f42429bfd8b6626f01ff155f71d68cbac6dfe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:10:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:10:29 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:10:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:10:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:10:30 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:10:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d668ec0d13619d02b98ac6e2ab2bb7ca3974ad1ed964fbbfae78e23a777df473`  
		Last Modified: Wed, 20 May 2026 16:04:26 GMT  
		Size: 6.5 MB (6490542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5c187c9ced3347b391d712fe3353958272e09460e48ef72b492e55332f67a0`  
		Last Modified: Wed, 20 May 2026 19:10:48 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.9` - unknown; unknown

```console
$ docker pull nats@sha256:6868356eb5df018325b032eca1a4d9471a915135b6ad01baf74cbed5245b7581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74a49ccc3dc2aca4a464c76934f3739fa2e4fdbc49a4fe3a93d58e620431eba9`

```dockerfile
```

-	Layers:
	-	`sha256:beed34e5caa7d0f8bb8e9624e6acbd693112ad713d81a6ebe9751d3d4a144a83`  
		Last Modified: Wed, 20 May 2026 19:10:48 GMT  
		Size: 8.7 KB (8661 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.9` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:b5f413bd3b0f768cdcfb88471ef7dd7e1e8979c00517fecb6fec681e1ff658dc
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133878103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14eeb0f5e1235887ceab95fb27b69b508faa0a9be7ec8654eb6483d61bd87539`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 20 May 2026 19:09:14 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 20 May 2026 19:09:43 GMT
RUN cmd /S /C #(nop) COPY file:dd9132ddd79eef4f3cbcb173e3b4c47616b6109b67b3da726ffcf5aa0546dfe6 in C:\nats-server.exe 
# Wed, 20 May 2026 19:09:44 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 20 May 2026 19:09:44 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 20 May 2026 19:09:44 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 20 May 2026 19:09:45 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c815e3255991cc2df065c98a27664be46d8b5db04231449f637ecaf64c5c098f`  
		Last Modified: Wed, 20 May 2026 19:09:24 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0584329bf51b06503599bd12d61e5b4b8022e17567c5a00bf044a36fec53f6ca`  
		Last Modified: Wed, 20 May 2026 19:09:54 GMT  
		Size: 6.8 MB (6833293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42502c403069fbf82a9dfaead168b2b5f649366919a105dc982b8388c2da2055`  
		Last Modified: Wed, 20 May 2026 19:09:49 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f632ce4ec8c46651a30b231de5b71039037abbc82f1bede845e302e0a576a256`  
		Last Modified: Wed, 20 May 2026 19:09:49 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceaf1e7278afa4664b03b5df7ba7fb9043b402be47232554b124a56a1c85927c`  
		Last Modified: Wed, 20 May 2026 19:09:49 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d4067da1a0ad2b0d46b1f5bbaebefcfeb420dbac588629c9d392f95f7723d4`  
		Last Modified: Wed, 20 May 2026 19:09:49 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12.9-alpine`

```console
$ docker pull nats@sha256:d152634b3db31218ca61c794827d04e8133e2538ef2f2cc3ab7be77b2ea8efd0
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

### `nats:2.12.9-alpine` - linux; amd64

```console
$ docker pull nats@sha256:9f005ca5efcae24ddd0413014c8ba5d3464d2a2560233b1bff108cc5563df009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10909206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c4eb9669610892376f2a3886a0c6e7b61fc0f2c5d3f740abe33e501f3f184c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:37:22 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:37:22 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:37:22 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='72b5841a019f6c5a0be78d3cf21cd293446317e6b4e769e3b9d72090f2d87afc' ;;     armhf) natsArch='arm6'; sha256='eb159297eb8539e47f615180b1de759e6a735cfe3274a31d405301e1c2ee2aec' ;;     armv7) natsArch='arm7'; sha256='2573d1cb723f55d81c58e854e63c771e1a2d954a91ed0a23042e7e38fa0d405c' ;;     x86_64) natsArch='amd64'; sha256='b126515225aa2265a0088e0170f2a9de4c7880b2388cc7584aa77859ce831e3f' ;;     x86) natsArch='386'; sha256='c29a867045b25e300e501101abc3714e4e56c89b35b90ddbfc55ec6e7928eb17' ;;     s390x) natsArch='s390x'; sha256='d508d9f40853828623b50e367a4dd0394361352195b3669d5da7966991e30c03' ;;     ppc64le) natsArch='ppc64le'; sha256='a2dcbabba4aede66b9939d59e829d61417fffa7c08c49635b9a550a23f733cdc' ;;     loong64) natsArch='loong64'; sha256='5a0347fa1400a569cc798da80001fca8c68dc7193daea334df9ea6ec5fe2649c' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:37:22 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:37:22 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:37:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:37:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:37:22 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785afd645f29603dfc502b5aed95092773a9d75614d744ab69f3c90a491db958`  
		Last Modified: Wed, 20 May 2026 18:37:27 GMT  
		Size: 7.1 MB (7100047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2f75731780f4bdd6e4465ff6aedcfb784f2e04de6f7f593183a54df15a238b`  
		Last Modified: Wed, 20 May 2026 18:37:26 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea647ca93a5f93dd0481e42085d112026c222e13018b23f940c1798f150ddfc1`  
		Last Modified: Wed, 20 May 2026 18:37:27 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.9-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:c8082807e13d0ed6d2ad0cebcad6ff56b3a50637c7121d851c85bc76d43e51db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d6c6f5b5e660ea789920f5dadbe9d69a4b9c17b3cb539f1ad32abfe974a8016`

```dockerfile
```

-	Layers:
	-	`sha256:d118d5c6f5a5b003d23105ccb683ce7cbca22c58923371c7a4cad24bb2a0fa7a`  
		Last Modified: Wed, 20 May 2026 18:37:27 GMT  
		Size: 14.2 KB (14204 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.9-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:6ca666c2519ce831880fc65291a7ba5e6bdde44f1fce5826695e03943924c735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10347662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae81b57a35e9f65ea23549d2183c2c2e7ca7d50ce3f5036fa062e1cafaf518d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:36:19 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:36:19 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:36:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='72b5841a019f6c5a0be78d3cf21cd293446317e6b4e769e3b9d72090f2d87afc' ;;     armhf) natsArch='arm6'; sha256='eb159297eb8539e47f615180b1de759e6a735cfe3274a31d405301e1c2ee2aec' ;;     armv7) natsArch='arm7'; sha256='2573d1cb723f55d81c58e854e63c771e1a2d954a91ed0a23042e7e38fa0d405c' ;;     x86_64) natsArch='amd64'; sha256='b126515225aa2265a0088e0170f2a9de4c7880b2388cc7584aa77859ce831e3f' ;;     x86) natsArch='386'; sha256='c29a867045b25e300e501101abc3714e4e56c89b35b90ddbfc55ec6e7928eb17' ;;     s390x) natsArch='s390x'; sha256='d508d9f40853828623b50e367a4dd0394361352195b3669d5da7966991e30c03' ;;     ppc64le) natsArch='ppc64le'; sha256='a2dcbabba4aede66b9939d59e829d61417fffa7c08c49635b9a550a23f733cdc' ;;     loong64) natsArch='loong64'; sha256='5a0347fa1400a569cc798da80001fca8c68dc7193daea334df9ea6ec5fe2649c' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:36:19 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:36:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:36:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:36:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:36:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2912b40ddee494992b06ce6cfb3fe8dcb65d8de1892afcc94917eca78b7d9a0e`  
		Last Modified: Wed, 20 May 2026 18:36:24 GMT  
		Size: 6.8 MB (6839309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c4d072278e3126931517cbe8b2c9ef7cb6deb74558f56fedca986a5290a04c`  
		Last Modified: Wed, 20 May 2026 18:36:24 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f197927573b1036dd0f62c1a4cc9744836b24dbc6a2f4de557bdc47a30ce8be`  
		Last Modified: Wed, 20 May 2026 18:36:23 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.9-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:c61ccd3efdac690b485d840b7dfeceda69959a897f80949d0526c35a457cf1f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eecbe0cf18d59940e35cb0d2a6250eef69ca91a9543eb363af073473e44f86c`

```dockerfile
```

-	Layers:
	-	`sha256:18009424a0cc1065f3e1eef0bf7339139ef37661b11ace35f1b5949d76f335d9`  
		Last Modified: Wed, 20 May 2026 18:36:23 GMT  
		Size: 14.3 KB (14284 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.9-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:bcaff37bbf2a1f726cb43e74fe7db6b6e753a949c6083b2822d18e14da85ca0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10055590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd657e711d296590c867eb7ef48b021588d25b86bfad505ec5ae8cde2ec1d1d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:36:15 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:36:15 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:36:15 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='72b5841a019f6c5a0be78d3cf21cd293446317e6b4e769e3b9d72090f2d87afc' ;;     armhf) natsArch='arm6'; sha256='eb159297eb8539e47f615180b1de759e6a735cfe3274a31d405301e1c2ee2aec' ;;     armv7) natsArch='arm7'; sha256='2573d1cb723f55d81c58e854e63c771e1a2d954a91ed0a23042e7e38fa0d405c' ;;     x86_64) natsArch='amd64'; sha256='b126515225aa2265a0088e0170f2a9de4c7880b2388cc7584aa77859ce831e3f' ;;     x86) natsArch='386'; sha256='c29a867045b25e300e501101abc3714e4e56c89b35b90ddbfc55ec6e7928eb17' ;;     s390x) natsArch='s390x'; sha256='d508d9f40853828623b50e367a4dd0394361352195b3669d5da7966991e30c03' ;;     ppc64le) natsArch='ppc64le'; sha256='a2dcbabba4aede66b9939d59e829d61417fffa7c08c49635b9a550a23f733cdc' ;;     loong64) natsArch='loong64'; sha256='5a0347fa1400a569cc798da80001fca8c68dc7193daea334df9ea6ec5fe2649c' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:36:15 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:36:15 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:36:15 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:36:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:36:15 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc50b4a871d38a0cadde4ed4e424bc2187dfef3cd7b5af2f61d284f5000115cd`  
		Last Modified: Wed, 20 May 2026 18:36:20 GMT  
		Size: 6.8 MB (6828786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9549ff00bf4e47e9e775e46e3309a6c2d758382c50d7296865843e1034afe6dc`  
		Last Modified: Wed, 20 May 2026 18:36:20 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519ec8720496ec12b71688a575e86930c39ad7b2f5f12bc6e1ea5efa4b6ed815`  
		Last Modified: Wed, 20 May 2026 18:36:20 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.9-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:c35fea02bd550591fb78b42bc3e5316a3ce215f434775a80bfb9160fbd852a30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64701b345d4b8c5c56c71be078a3da0398507cd26e5919d9645432b5788339d9`

```dockerfile
```

-	Layers:
	-	`sha256:98625cfe5efdb1372a3b79cc98481ba6088f0d689b3566d4b9137f4ae7c4e389`  
		Last Modified: Wed, 20 May 2026 18:36:20 GMT  
		Size: 14.3 KB (14284 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.9-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d5e2a634247e27b59ccf258b33f626c0f5949b96b737536496b562f06b7e094c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10642176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80fc2db9d5bb25035d90c05c366a4658fad874a40ee451f2a41188d4f6ead80b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:37:06 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:37:06 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:37:06 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='72b5841a019f6c5a0be78d3cf21cd293446317e6b4e769e3b9d72090f2d87afc' ;;     armhf) natsArch='arm6'; sha256='eb159297eb8539e47f615180b1de759e6a735cfe3274a31d405301e1c2ee2aec' ;;     armv7) natsArch='arm7'; sha256='2573d1cb723f55d81c58e854e63c771e1a2d954a91ed0a23042e7e38fa0d405c' ;;     x86_64) natsArch='amd64'; sha256='b126515225aa2265a0088e0170f2a9de4c7880b2388cc7584aa77859ce831e3f' ;;     x86) natsArch='386'; sha256='c29a867045b25e300e501101abc3714e4e56c89b35b90ddbfc55ec6e7928eb17' ;;     s390x) natsArch='s390x'; sha256='d508d9f40853828623b50e367a4dd0394361352195b3669d5da7966991e30c03' ;;     ppc64le) natsArch='ppc64le'; sha256='a2dcbabba4aede66b9939d59e829d61417fffa7c08c49635b9a550a23f733cdc' ;;     loong64) natsArch='loong64'; sha256='5a0347fa1400a569cc798da80001fca8c68dc7193daea334df9ea6ec5fe2649c' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:37:06 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:37:06 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:37:06 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:37:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:37:06 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ff339b51fb101889997a78aaa1897c82810b93750d3c1fad2c9939c172510d`  
		Last Modified: Wed, 20 May 2026 18:37:11 GMT  
		Size: 6.5 MB (6499312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01cdeeebd5372e1dc9a2c97c853e72b20a3622eed3457557f5913caa2b335da1`  
		Last Modified: Wed, 20 May 2026 18:37:11 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1624ccef5078119f6ce1d17ffcdd69ee710740b23ed841fbd209e80c8b6f3032`  
		Last Modified: Wed, 20 May 2026 18:37:11 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.9-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:d2b097ebfadc88817dcda244513c1536ee40a0fe3e24f28e6094d7eddf30a9ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:195c6c70cb97e0570c5672af8dc9c1b933cc356306a6daae576ac7e92b55ee69`

```dockerfile
```

-	Layers:
	-	`sha256:9145327976083751cab916e93d4003480e2bc0b428d04a554617da1720ba9788`  
		Last Modified: Wed, 20 May 2026 18:37:11 GMT  
		Size: 14.3 KB (14308 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.9-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:2e2a8c50a862185aabb439c2fe0736bf976ac4f14f840192f46ada06908ec62b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10295179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6684ad61a65a2f9bf995f867d9d9d9b78d57e72ecbac3ca56cb56b6e407e0ad6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:39:54 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:39:54 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:39:54 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='72b5841a019f6c5a0be78d3cf21cd293446317e6b4e769e3b9d72090f2d87afc' ;;     armhf) natsArch='arm6'; sha256='eb159297eb8539e47f615180b1de759e6a735cfe3274a31d405301e1c2ee2aec' ;;     armv7) natsArch='arm7'; sha256='2573d1cb723f55d81c58e854e63c771e1a2d954a91ed0a23042e7e38fa0d405c' ;;     x86_64) natsArch='amd64'; sha256='b126515225aa2265a0088e0170f2a9de4c7880b2388cc7584aa77859ce831e3f' ;;     x86) natsArch='386'; sha256='c29a867045b25e300e501101abc3714e4e56c89b35b90ddbfc55ec6e7928eb17' ;;     s390x) natsArch='s390x'; sha256='d508d9f40853828623b50e367a4dd0394361352195b3669d5da7966991e30c03' ;;     ppc64le) natsArch='ppc64le'; sha256='a2dcbabba4aede66b9939d59e829d61417fffa7c08c49635b9a550a23f733cdc' ;;     loong64) natsArch='loong64'; sha256='5a0347fa1400a569cc798da80001fca8c68dc7193daea334df9ea6ec5fe2649c' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:39:55 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:39:55 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:39:55 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:39:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:39:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe0b03709a632c9f299b1ef2c2691c1b292ae9f333a7b2083a9b51162a19669`  
		Last Modified: Wed, 20 May 2026 18:40:02 GMT  
		Size: 6.6 MB (6557551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3c6e5710602d0c65abfcc3a4aac8676e3cd1f849d5967bee0654b0ec045abe`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0fcc4ed5f0f4848feb91f0e5c409cb87bfd693a7056f2c0e574dbf0fc8ff4ab`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.9-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:5b7ba3b09bf23127b1a75c412fb6e5e3fa773abda140a3f0e45600422968bf88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b9cec962a037f640085142478803038714db7fa629a4b7e6cad1c2f41371943`

```dockerfile
```

-	Layers:
	-	`sha256:bc2e73ad0cbc0cad27f1667939617eb3a7d77a3ba7dd6d70917518d2ee4fed7f`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 14.2 KB (14248 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.9-alpine` - linux; s390x

```console
$ docker pull nats@sha256:ce14e245951893e72e72ac26599d178e07af3e24fd01a857cc00c484fee718cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10603715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0f596aa7cbe6e6e80f8063aae3852a811f7045c570a2bf4e89c6b1c0a0d596f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:48:37 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:48:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:48:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='72b5841a019f6c5a0be78d3cf21cd293446317e6b4e769e3b9d72090f2d87afc' ;;     armhf) natsArch='arm6'; sha256='eb159297eb8539e47f615180b1de759e6a735cfe3274a31d405301e1c2ee2aec' ;;     armv7) natsArch='arm7'; sha256='2573d1cb723f55d81c58e854e63c771e1a2d954a91ed0a23042e7e38fa0d405c' ;;     x86_64) natsArch='amd64'; sha256='b126515225aa2265a0088e0170f2a9de4c7880b2388cc7584aa77859ce831e3f' ;;     x86) natsArch='386'; sha256='c29a867045b25e300e501101abc3714e4e56c89b35b90ddbfc55ec6e7928eb17' ;;     s390x) natsArch='s390x'; sha256='d508d9f40853828623b50e367a4dd0394361352195b3669d5da7966991e30c03' ;;     ppc64le) natsArch='ppc64le'; sha256='a2dcbabba4aede66b9939d59e829d61417fffa7c08c49635b9a550a23f733cdc' ;;     loong64) natsArch='loong64'; sha256='5a0347fa1400a569cc798da80001fca8c68dc7193daea334df9ea6ec5fe2649c' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:48:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:48:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:48:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:48:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:48:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13002ceadd3c101c2cfaa462d93d68f1056f8fd0453fd99269b12c624bc6b38a`  
		Last Modified: Wed, 20 May 2026 18:49:13 GMT  
		Size: 6.9 MB (6948871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdaa4e64de2e200c41440e78516f3fbbcf03b5b5e18cb05b20a63bd1661ce87d`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d69a6bdd10e86979de515f61b8c590bea15507a88f17e4f5a7f57ddfac937e`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.9-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:92726e2db0802623d76696809568374f168d11a6eb505249100949eb89a74c6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a1345efb532a7d2fa604c74539fdd13035a959493b0f11f0e962227e91cfe8e`

```dockerfile
```

-	Layers:
	-	`sha256:afc92f71ec0a9bc07c23a3ff65bc6f32afe90cfc974b6e23b25a06cab13804fd`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 14.2 KB (14204 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12.9-alpine3.22`

```console
$ docker pull nats@sha256:d152634b3db31218ca61c794827d04e8133e2538ef2f2cc3ab7be77b2ea8efd0
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

### `nats:2.12.9-alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:9f005ca5efcae24ddd0413014c8ba5d3464d2a2560233b1bff108cc5563df009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10909206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c4eb9669610892376f2a3886a0c6e7b61fc0f2c5d3f740abe33e501f3f184c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:37:22 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:37:22 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:37:22 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='72b5841a019f6c5a0be78d3cf21cd293446317e6b4e769e3b9d72090f2d87afc' ;;     armhf) natsArch='arm6'; sha256='eb159297eb8539e47f615180b1de759e6a735cfe3274a31d405301e1c2ee2aec' ;;     armv7) natsArch='arm7'; sha256='2573d1cb723f55d81c58e854e63c771e1a2d954a91ed0a23042e7e38fa0d405c' ;;     x86_64) natsArch='amd64'; sha256='b126515225aa2265a0088e0170f2a9de4c7880b2388cc7584aa77859ce831e3f' ;;     x86) natsArch='386'; sha256='c29a867045b25e300e501101abc3714e4e56c89b35b90ddbfc55ec6e7928eb17' ;;     s390x) natsArch='s390x'; sha256='d508d9f40853828623b50e367a4dd0394361352195b3669d5da7966991e30c03' ;;     ppc64le) natsArch='ppc64le'; sha256='a2dcbabba4aede66b9939d59e829d61417fffa7c08c49635b9a550a23f733cdc' ;;     loong64) natsArch='loong64'; sha256='5a0347fa1400a569cc798da80001fca8c68dc7193daea334df9ea6ec5fe2649c' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:37:22 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:37:22 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:37:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:37:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:37:22 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785afd645f29603dfc502b5aed95092773a9d75614d744ab69f3c90a491db958`  
		Last Modified: Wed, 20 May 2026 18:37:27 GMT  
		Size: 7.1 MB (7100047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2f75731780f4bdd6e4465ff6aedcfb784f2e04de6f7f593183a54df15a238b`  
		Last Modified: Wed, 20 May 2026 18:37:26 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea647ca93a5f93dd0481e42085d112026c222e13018b23f940c1798f150ddfc1`  
		Last Modified: Wed, 20 May 2026 18:37:27 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.9-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:c8082807e13d0ed6d2ad0cebcad6ff56b3a50637c7121d851c85bc76d43e51db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d6c6f5b5e660ea789920f5dadbe9d69a4b9c17b3cb539f1ad32abfe974a8016`

```dockerfile
```

-	Layers:
	-	`sha256:d118d5c6f5a5b003d23105ccb683ce7cbca22c58923371c7a4cad24bb2a0fa7a`  
		Last Modified: Wed, 20 May 2026 18:37:27 GMT  
		Size: 14.2 KB (14204 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.9-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:6ca666c2519ce831880fc65291a7ba5e6bdde44f1fce5826695e03943924c735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10347662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae81b57a35e9f65ea23549d2183c2c2e7ca7d50ce3f5036fa062e1cafaf518d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:36:19 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:36:19 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:36:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='72b5841a019f6c5a0be78d3cf21cd293446317e6b4e769e3b9d72090f2d87afc' ;;     armhf) natsArch='arm6'; sha256='eb159297eb8539e47f615180b1de759e6a735cfe3274a31d405301e1c2ee2aec' ;;     armv7) natsArch='arm7'; sha256='2573d1cb723f55d81c58e854e63c771e1a2d954a91ed0a23042e7e38fa0d405c' ;;     x86_64) natsArch='amd64'; sha256='b126515225aa2265a0088e0170f2a9de4c7880b2388cc7584aa77859ce831e3f' ;;     x86) natsArch='386'; sha256='c29a867045b25e300e501101abc3714e4e56c89b35b90ddbfc55ec6e7928eb17' ;;     s390x) natsArch='s390x'; sha256='d508d9f40853828623b50e367a4dd0394361352195b3669d5da7966991e30c03' ;;     ppc64le) natsArch='ppc64le'; sha256='a2dcbabba4aede66b9939d59e829d61417fffa7c08c49635b9a550a23f733cdc' ;;     loong64) natsArch='loong64'; sha256='5a0347fa1400a569cc798da80001fca8c68dc7193daea334df9ea6ec5fe2649c' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:36:19 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:36:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:36:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:36:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:36:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2912b40ddee494992b06ce6cfb3fe8dcb65d8de1892afcc94917eca78b7d9a0e`  
		Last Modified: Wed, 20 May 2026 18:36:24 GMT  
		Size: 6.8 MB (6839309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c4d072278e3126931517cbe8b2c9ef7cb6deb74558f56fedca986a5290a04c`  
		Last Modified: Wed, 20 May 2026 18:36:24 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f197927573b1036dd0f62c1a4cc9744836b24dbc6a2f4de557bdc47a30ce8be`  
		Last Modified: Wed, 20 May 2026 18:36:23 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.9-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:c61ccd3efdac690b485d840b7dfeceda69959a897f80949d0526c35a457cf1f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eecbe0cf18d59940e35cb0d2a6250eef69ca91a9543eb363af073473e44f86c`

```dockerfile
```

-	Layers:
	-	`sha256:18009424a0cc1065f3e1eef0bf7339139ef37661b11ace35f1b5949d76f335d9`  
		Last Modified: Wed, 20 May 2026 18:36:23 GMT  
		Size: 14.3 KB (14284 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.9-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:bcaff37bbf2a1f726cb43e74fe7db6b6e753a949c6083b2822d18e14da85ca0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10055590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd657e711d296590c867eb7ef48b021588d25b86bfad505ec5ae8cde2ec1d1d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:36:15 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:36:15 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:36:15 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='72b5841a019f6c5a0be78d3cf21cd293446317e6b4e769e3b9d72090f2d87afc' ;;     armhf) natsArch='arm6'; sha256='eb159297eb8539e47f615180b1de759e6a735cfe3274a31d405301e1c2ee2aec' ;;     armv7) natsArch='arm7'; sha256='2573d1cb723f55d81c58e854e63c771e1a2d954a91ed0a23042e7e38fa0d405c' ;;     x86_64) natsArch='amd64'; sha256='b126515225aa2265a0088e0170f2a9de4c7880b2388cc7584aa77859ce831e3f' ;;     x86) natsArch='386'; sha256='c29a867045b25e300e501101abc3714e4e56c89b35b90ddbfc55ec6e7928eb17' ;;     s390x) natsArch='s390x'; sha256='d508d9f40853828623b50e367a4dd0394361352195b3669d5da7966991e30c03' ;;     ppc64le) natsArch='ppc64le'; sha256='a2dcbabba4aede66b9939d59e829d61417fffa7c08c49635b9a550a23f733cdc' ;;     loong64) natsArch='loong64'; sha256='5a0347fa1400a569cc798da80001fca8c68dc7193daea334df9ea6ec5fe2649c' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:36:15 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:36:15 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:36:15 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:36:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:36:15 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc50b4a871d38a0cadde4ed4e424bc2187dfef3cd7b5af2f61d284f5000115cd`  
		Last Modified: Wed, 20 May 2026 18:36:20 GMT  
		Size: 6.8 MB (6828786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9549ff00bf4e47e9e775e46e3309a6c2d758382c50d7296865843e1034afe6dc`  
		Last Modified: Wed, 20 May 2026 18:36:20 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519ec8720496ec12b71688a575e86930c39ad7b2f5f12bc6e1ea5efa4b6ed815`  
		Last Modified: Wed, 20 May 2026 18:36:20 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.9-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:c35fea02bd550591fb78b42bc3e5316a3ce215f434775a80bfb9160fbd852a30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64701b345d4b8c5c56c71be078a3da0398507cd26e5919d9645432b5788339d9`

```dockerfile
```

-	Layers:
	-	`sha256:98625cfe5efdb1372a3b79cc98481ba6088f0d689b3566d4b9137f4ae7c4e389`  
		Last Modified: Wed, 20 May 2026 18:36:20 GMT  
		Size: 14.3 KB (14284 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.9-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d5e2a634247e27b59ccf258b33f626c0f5949b96b737536496b562f06b7e094c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10642176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80fc2db9d5bb25035d90c05c366a4658fad874a40ee451f2a41188d4f6ead80b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:37:06 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:37:06 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:37:06 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='72b5841a019f6c5a0be78d3cf21cd293446317e6b4e769e3b9d72090f2d87afc' ;;     armhf) natsArch='arm6'; sha256='eb159297eb8539e47f615180b1de759e6a735cfe3274a31d405301e1c2ee2aec' ;;     armv7) natsArch='arm7'; sha256='2573d1cb723f55d81c58e854e63c771e1a2d954a91ed0a23042e7e38fa0d405c' ;;     x86_64) natsArch='amd64'; sha256='b126515225aa2265a0088e0170f2a9de4c7880b2388cc7584aa77859ce831e3f' ;;     x86) natsArch='386'; sha256='c29a867045b25e300e501101abc3714e4e56c89b35b90ddbfc55ec6e7928eb17' ;;     s390x) natsArch='s390x'; sha256='d508d9f40853828623b50e367a4dd0394361352195b3669d5da7966991e30c03' ;;     ppc64le) natsArch='ppc64le'; sha256='a2dcbabba4aede66b9939d59e829d61417fffa7c08c49635b9a550a23f733cdc' ;;     loong64) natsArch='loong64'; sha256='5a0347fa1400a569cc798da80001fca8c68dc7193daea334df9ea6ec5fe2649c' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:37:06 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:37:06 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:37:06 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:37:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:37:06 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ff339b51fb101889997a78aaa1897c82810b93750d3c1fad2c9939c172510d`  
		Last Modified: Wed, 20 May 2026 18:37:11 GMT  
		Size: 6.5 MB (6499312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01cdeeebd5372e1dc9a2c97c853e72b20a3622eed3457557f5913caa2b335da1`  
		Last Modified: Wed, 20 May 2026 18:37:11 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1624ccef5078119f6ce1d17ffcdd69ee710740b23ed841fbd209e80c8b6f3032`  
		Last Modified: Wed, 20 May 2026 18:37:11 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.9-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:d2b097ebfadc88817dcda244513c1536ee40a0fe3e24f28e6094d7eddf30a9ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:195c6c70cb97e0570c5672af8dc9c1b933cc356306a6daae576ac7e92b55ee69`

```dockerfile
```

-	Layers:
	-	`sha256:9145327976083751cab916e93d4003480e2bc0b428d04a554617da1720ba9788`  
		Last Modified: Wed, 20 May 2026 18:37:11 GMT  
		Size: 14.3 KB (14308 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.9-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:2e2a8c50a862185aabb439c2fe0736bf976ac4f14f840192f46ada06908ec62b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10295179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6684ad61a65a2f9bf995f867d9d9d9b78d57e72ecbac3ca56cb56b6e407e0ad6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:39:54 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:39:54 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:39:54 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='72b5841a019f6c5a0be78d3cf21cd293446317e6b4e769e3b9d72090f2d87afc' ;;     armhf) natsArch='arm6'; sha256='eb159297eb8539e47f615180b1de759e6a735cfe3274a31d405301e1c2ee2aec' ;;     armv7) natsArch='arm7'; sha256='2573d1cb723f55d81c58e854e63c771e1a2d954a91ed0a23042e7e38fa0d405c' ;;     x86_64) natsArch='amd64'; sha256='b126515225aa2265a0088e0170f2a9de4c7880b2388cc7584aa77859ce831e3f' ;;     x86) natsArch='386'; sha256='c29a867045b25e300e501101abc3714e4e56c89b35b90ddbfc55ec6e7928eb17' ;;     s390x) natsArch='s390x'; sha256='d508d9f40853828623b50e367a4dd0394361352195b3669d5da7966991e30c03' ;;     ppc64le) natsArch='ppc64le'; sha256='a2dcbabba4aede66b9939d59e829d61417fffa7c08c49635b9a550a23f733cdc' ;;     loong64) natsArch='loong64'; sha256='5a0347fa1400a569cc798da80001fca8c68dc7193daea334df9ea6ec5fe2649c' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:39:55 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:39:55 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:39:55 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:39:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:39:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe0b03709a632c9f299b1ef2c2691c1b292ae9f333a7b2083a9b51162a19669`  
		Last Modified: Wed, 20 May 2026 18:40:02 GMT  
		Size: 6.6 MB (6557551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3c6e5710602d0c65abfcc3a4aac8676e3cd1f849d5967bee0654b0ec045abe`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0fcc4ed5f0f4848feb91f0e5c409cb87bfd693a7056f2c0e574dbf0fc8ff4ab`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.9-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:5b7ba3b09bf23127b1a75c412fb6e5e3fa773abda140a3f0e45600422968bf88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b9cec962a037f640085142478803038714db7fa629a4b7e6cad1c2f41371943`

```dockerfile
```

-	Layers:
	-	`sha256:bc2e73ad0cbc0cad27f1667939617eb3a7d77a3ba7dd6d70917518d2ee4fed7f`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 14.2 KB (14248 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.9-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:ce14e245951893e72e72ac26599d178e07af3e24fd01a857cc00c484fee718cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10603715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0f596aa7cbe6e6e80f8063aae3852a811f7045c570a2bf4e89c6b1c0a0d596f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:48:37 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:48:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:48:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='72b5841a019f6c5a0be78d3cf21cd293446317e6b4e769e3b9d72090f2d87afc' ;;     armhf) natsArch='arm6'; sha256='eb159297eb8539e47f615180b1de759e6a735cfe3274a31d405301e1c2ee2aec' ;;     armv7) natsArch='arm7'; sha256='2573d1cb723f55d81c58e854e63c771e1a2d954a91ed0a23042e7e38fa0d405c' ;;     x86_64) natsArch='amd64'; sha256='b126515225aa2265a0088e0170f2a9de4c7880b2388cc7584aa77859ce831e3f' ;;     x86) natsArch='386'; sha256='c29a867045b25e300e501101abc3714e4e56c89b35b90ddbfc55ec6e7928eb17' ;;     s390x) natsArch='s390x'; sha256='d508d9f40853828623b50e367a4dd0394361352195b3669d5da7966991e30c03' ;;     ppc64le) natsArch='ppc64le'; sha256='a2dcbabba4aede66b9939d59e829d61417fffa7c08c49635b9a550a23f733cdc' ;;     loong64) natsArch='loong64'; sha256='5a0347fa1400a569cc798da80001fca8c68dc7193daea334df9ea6ec5fe2649c' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:48:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:48:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:48:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:48:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:48:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13002ceadd3c101c2cfaa462d93d68f1056f8fd0453fd99269b12c624bc6b38a`  
		Last Modified: Wed, 20 May 2026 18:49:13 GMT  
		Size: 6.9 MB (6948871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdaa4e64de2e200c41440e78516f3fbbcf03b5b5e18cb05b20a63bd1661ce87d`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d69a6bdd10e86979de515f61b8c590bea15507a88f17e4f5a7f57ddfac937e`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.9-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:92726e2db0802623d76696809568374f168d11a6eb505249100949eb89a74c6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a1345efb532a7d2fa604c74539fdd13035a959493b0f11f0e962227e91cfe8e`

```dockerfile
```

-	Layers:
	-	`sha256:afc92f71ec0a9bc07c23a3ff65bc6f32afe90cfc974b6e23b25a06cab13804fd`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 14.2 KB (14204 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12.9-linux`

```console
$ docker pull nats@sha256:ee9a8f12f3a0d9c2b26f6d16a5f1867f851d21f1acde6d5ae2b75570efe5cdb3
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

### `nats:2.12.9-linux` - linux; amd64

```console
$ docker pull nats@sha256:81dd79785518efd999b91f95c3704444c73865f457c195dbc2a7ca54f9e82b9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6643802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eee8ee507e1167111022248b38dc79952282435780aa5561a54272070231fba`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:10:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:10:49 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:10:49 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:10:49 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:10:49 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:10:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e5e76f67b303999883527fbb9d2827bb20bf4266bd14b30fe193b9c837d56b9`  
		Last Modified: Wed, 20 May 2026 16:04:23 GMT  
		Size: 6.6 MB (6643293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a25302c76354939bc63896b8a3c3e531819ed31d7c3fabed2c21912ed5a778a`  
		Last Modified: Wed, 20 May 2026 19:10:53 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.9-linux` - unknown; unknown

```console
$ docker pull nats@sha256:63bdef746f1bd984ed04788dbb4683d8899fde6b501588af9d034679f4d5c4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e9d8d10730cd5f5322c955e5243b4f410f4f61622f7e434b533f38cbfa8b9bd`

```dockerfile
```

-	Layers:
	-	`sha256:29922663c3486deec187939e4f05d87cecd02dbb505dadb59cab3b9b718aa068`  
		Last Modified: Wed, 20 May 2026 19:10:53 GMT  
		Size: 8.7 KB (8660 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.9-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:697254950318448b92489577435eb73db46ad779dfa5bb8312950fcbcf774fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6383827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e55c4a455573962fac86f8a167ca43e89be66b7799b10d76e5465fdf00ffdf7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:09:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:09:39 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:09:39 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:09:39 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:09:39 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:09:39 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c10d60a8ee2ca1e386312db0a0b2473313d36b33da2c5a1eed45d3dbc145b255`  
		Last Modified: Wed, 20 May 2026 16:04:26 GMT  
		Size: 6.4 MB (6383319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1d283fe91c0f3527ed49fb1f312ae136b8fb1cab01bd902b22c0a912727bc7`  
		Last Modified: Wed, 20 May 2026 19:09:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.9-linux` - unknown; unknown

```console
$ docker pull nats@sha256:cc69b4de3ae7531530b6ae76912d528339157b572f0c822676897fac26e728d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08a5b8c8548b84e96f500c4ee6700a282c92ebc58d03b35f1d49ab5424ba360d`

```dockerfile
```

-	Layers:
	-	`sha256:bf6a20cdeb4777f1f89bf3b91149fbb9cd5193d460d2720e5856bc2a69d08a65`  
		Last Modified: Wed, 20 May 2026 19:09:43 GMT  
		Size: 8.7 KB (8744 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.9-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:a2d058ffac3e0982c4263c4a98357898b61eca619d2c56a76aac7b9f2d18f171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6373077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:130977b1791d287860791cbc0f238f4bf8902acceeb859fc8663ca013fc90b15`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:09:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:09:50 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:09:50 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:09:50 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:09:50 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:09:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:efec7643648fe287ed0901613783bcd23bb5a8b7b2fb2aee2e9f58a8d0d8d7a8`  
		Last Modified: Wed, 20 May 2026 16:04:26 GMT  
		Size: 6.4 MB (6372568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af920700845e87c0ae0d0a2e002936cf3fe153e0d75cd8d28e1fdebe0951676c`  
		Last Modified: Wed, 20 May 2026 19:09:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.9-linux` - unknown; unknown

```console
$ docker pull nats@sha256:a96c4eefe96a686ef87c6963d464d87de0be9f9d27e2e065a01137de83f6f1ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f334115d58195d99db72b89b7cd06f5d63fbbfe2344d46642d5e03925960c426`

```dockerfile
```

-	Layers:
	-	`sha256:44bb6f0b5261e2b3668d54d1d0f788b8e18dd4e2ba44ef27c0949c43398854e9`  
		Last Modified: Wed, 20 May 2026 19:09:54 GMT  
		Size: 8.7 KB (8744 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.9-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:aa8f7e3d55a383e35f019c28b6c432ed2090b3dad56fead3e7a70ab1dba79ccc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6037707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1b69482ef45b939a2908e033d22c9582db2b53dac733301472ace541c756069`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:10:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:10:14 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:10:14 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:10:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:10:14 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:10:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:81af0467f4bfb473e50c712e06ca48adff2e7aab8456b45fcfbc3fefe8ef6df7`  
		Last Modified: Wed, 20 May 2026 16:04:24 GMT  
		Size: 6.0 MB (6037200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed22b68f9def9c87dfb1c5a9ec34a809caf385bcdfdd456fd3be55b553020ad`  
		Last Modified: Wed, 20 May 2026 19:10:19 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.9-linux` - unknown; unknown

```console
$ docker pull nats@sha256:534c5df88f202c2a015c845378127d701cc4faf3641326573fce6c0fd64dbd1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0a9c9217edbec11dd3120e94f789339bb631670a66be81de8e106830fef4b4`

```dockerfile
```

-	Layers:
	-	`sha256:743146aaf7c71f426d7abd3b4db2abcd72ecfd72aed9db12cb025a3148324d81`  
		Last Modified: Wed, 20 May 2026 19:10:19 GMT  
		Size: 8.8 KB (8774 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.9-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:3a024c2519d3e8d9afa913cc70dc8a08f42c27841b819c13ae7f4746791667f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6100417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a86f1bedebf55c136505a6a6115d4879fd94839c05722c2813b743b911513fc7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:09:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:09:00 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:09:00 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:09:00 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:09:00 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:09:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8d94981a1be7de02d7553ad09e31ec60ee268df51c2ef4762da5828b6b45674`  
		Last Modified: Wed, 20 May 2026 16:04:23 GMT  
		Size: 6.1 MB (6099908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb234fae2f8c35c37c5a0a2b27b551816540b8c513f6b2c479728b77a462cc5`  
		Last Modified: Wed, 20 May 2026 19:09:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.9-linux` - unknown; unknown

```console
$ docker pull nats@sha256:4bc8adf9c89eb891276d88ad9ef5302e83c23305ea4eee6318fdf94156bf00f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c21faa8dd4d3dbf3346283035cadd5da1c813c60749a515846c980e8940f08d8`

```dockerfile
```

-	Layers:
	-	`sha256:dd4e6d8e65f686896f2c04a5c31ca21c193b8ac222cbaa55fc6cf1e4ecbc68d7`  
		Last Modified: Wed, 20 May 2026 19:09:06 GMT  
		Size: 8.7 KB (8715 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.9-linux` - linux; s390x

```console
$ docker pull nats@sha256:0ff65b369dcf8b26046db1efa962fef20887641c137fba88592e99ac6d946759
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6491050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1fbd0e893d6064d2ae64507740f42429bfd8b6626f01ff155f71d68cbac6dfe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:10:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:10:29 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:10:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:10:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:10:30 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:10:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d668ec0d13619d02b98ac6e2ab2bb7ca3974ad1ed964fbbfae78e23a777df473`  
		Last Modified: Wed, 20 May 2026 16:04:26 GMT  
		Size: 6.5 MB (6490542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5c187c9ced3347b391d712fe3353958272e09460e48ef72b492e55332f67a0`  
		Last Modified: Wed, 20 May 2026 19:10:48 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.9-linux` - unknown; unknown

```console
$ docker pull nats@sha256:6868356eb5df018325b032eca1a4d9471a915135b6ad01baf74cbed5245b7581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74a49ccc3dc2aca4a464c76934f3739fa2e4fdbc49a4fe3a93d58e620431eba9`

```dockerfile
```

-	Layers:
	-	`sha256:beed34e5caa7d0f8bb8e9624e6acbd693112ad713d81a6ebe9751d3d4a144a83`  
		Last Modified: Wed, 20 May 2026 19:10:48 GMT  
		Size: 8.7 KB (8661 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12.9-nanoserver`

```console
$ docker pull nats@sha256:6d72ba1561be987809ce565415cbaf51c83f70b06f4d54d31d8213416b2581e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2.12.9-nanoserver` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:b5f413bd3b0f768cdcfb88471ef7dd7e1e8979c00517fecb6fec681e1ff658dc
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133878103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14eeb0f5e1235887ceab95fb27b69b508faa0a9be7ec8654eb6483d61bd87539`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 20 May 2026 19:09:14 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 20 May 2026 19:09:43 GMT
RUN cmd /S /C #(nop) COPY file:dd9132ddd79eef4f3cbcb173e3b4c47616b6109b67b3da726ffcf5aa0546dfe6 in C:\nats-server.exe 
# Wed, 20 May 2026 19:09:44 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 20 May 2026 19:09:44 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 20 May 2026 19:09:44 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 20 May 2026 19:09:45 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c815e3255991cc2df065c98a27664be46d8b5db04231449f637ecaf64c5c098f`  
		Last Modified: Wed, 20 May 2026 19:09:24 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0584329bf51b06503599bd12d61e5b4b8022e17567c5a00bf044a36fec53f6ca`  
		Last Modified: Wed, 20 May 2026 19:09:54 GMT  
		Size: 6.8 MB (6833293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42502c403069fbf82a9dfaead168b2b5f649366919a105dc982b8388c2da2055`  
		Last Modified: Wed, 20 May 2026 19:09:49 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f632ce4ec8c46651a30b231de5b71039037abbc82f1bede845e302e0a576a256`  
		Last Modified: Wed, 20 May 2026 19:09:49 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceaf1e7278afa4664b03b5df7ba7fb9043b402be47232554b124a56a1c85927c`  
		Last Modified: Wed, 20 May 2026 19:09:49 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d4067da1a0ad2b0d46b1f5bbaebefcfeb420dbac588629c9d392f95f7723d4`  
		Last Modified: Wed, 20 May 2026 19:09:49 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12.9-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:6d72ba1561be987809ce565415cbaf51c83f70b06f4d54d31d8213416b2581e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2.12.9-nanoserver-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:b5f413bd3b0f768cdcfb88471ef7dd7e1e8979c00517fecb6fec681e1ff658dc
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133878103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14eeb0f5e1235887ceab95fb27b69b508faa0a9be7ec8654eb6483d61bd87539`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 20 May 2026 19:09:14 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 20 May 2026 19:09:43 GMT
RUN cmd /S /C #(nop) COPY file:dd9132ddd79eef4f3cbcb173e3b4c47616b6109b67b3da726ffcf5aa0546dfe6 in C:\nats-server.exe 
# Wed, 20 May 2026 19:09:44 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 20 May 2026 19:09:44 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 20 May 2026 19:09:44 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 20 May 2026 19:09:45 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c815e3255991cc2df065c98a27664be46d8b5db04231449f637ecaf64c5c098f`  
		Last Modified: Wed, 20 May 2026 19:09:24 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0584329bf51b06503599bd12d61e5b4b8022e17567c5a00bf044a36fec53f6ca`  
		Last Modified: Wed, 20 May 2026 19:09:54 GMT  
		Size: 6.8 MB (6833293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42502c403069fbf82a9dfaead168b2b5f649366919a105dc982b8388c2da2055`  
		Last Modified: Wed, 20 May 2026 19:09:49 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f632ce4ec8c46651a30b231de5b71039037abbc82f1bede845e302e0a576a256`  
		Last Modified: Wed, 20 May 2026 19:09:49 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceaf1e7278afa4664b03b5df7ba7fb9043b402be47232554b124a56a1c85927c`  
		Last Modified: Wed, 20 May 2026 19:09:49 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d4067da1a0ad2b0d46b1f5bbaebefcfeb420dbac588629c9d392f95f7723d4`  
		Last Modified: Wed, 20 May 2026 19:09:49 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12.9-scratch`

```console
$ docker pull nats@sha256:ee9a8f12f3a0d9c2b26f6d16a5f1867f851d21f1acde6d5ae2b75570efe5cdb3
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

### `nats:2.12.9-scratch` - linux; amd64

```console
$ docker pull nats@sha256:81dd79785518efd999b91f95c3704444c73865f457c195dbc2a7ca54f9e82b9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6643802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eee8ee507e1167111022248b38dc79952282435780aa5561a54272070231fba`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:10:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:10:49 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:10:49 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:10:49 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:10:49 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:10:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e5e76f67b303999883527fbb9d2827bb20bf4266bd14b30fe193b9c837d56b9`  
		Last Modified: Wed, 20 May 2026 16:04:23 GMT  
		Size: 6.6 MB (6643293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a25302c76354939bc63896b8a3c3e531819ed31d7c3fabed2c21912ed5a778a`  
		Last Modified: Wed, 20 May 2026 19:10:53 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.9-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:63bdef746f1bd984ed04788dbb4683d8899fde6b501588af9d034679f4d5c4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e9d8d10730cd5f5322c955e5243b4f410f4f61622f7e434b533f38cbfa8b9bd`

```dockerfile
```

-	Layers:
	-	`sha256:29922663c3486deec187939e4f05d87cecd02dbb505dadb59cab3b9b718aa068`  
		Last Modified: Wed, 20 May 2026 19:10:53 GMT  
		Size: 8.7 KB (8660 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.9-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:697254950318448b92489577435eb73db46ad779dfa5bb8312950fcbcf774fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6383827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e55c4a455573962fac86f8a167ca43e89be66b7799b10d76e5465fdf00ffdf7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:09:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:09:39 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:09:39 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:09:39 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:09:39 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:09:39 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c10d60a8ee2ca1e386312db0a0b2473313d36b33da2c5a1eed45d3dbc145b255`  
		Last Modified: Wed, 20 May 2026 16:04:26 GMT  
		Size: 6.4 MB (6383319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1d283fe91c0f3527ed49fb1f312ae136b8fb1cab01bd902b22c0a912727bc7`  
		Last Modified: Wed, 20 May 2026 19:09:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.9-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:cc69b4de3ae7531530b6ae76912d528339157b572f0c822676897fac26e728d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08a5b8c8548b84e96f500c4ee6700a282c92ebc58d03b35f1d49ab5424ba360d`

```dockerfile
```

-	Layers:
	-	`sha256:bf6a20cdeb4777f1f89bf3b91149fbb9cd5193d460d2720e5856bc2a69d08a65`  
		Last Modified: Wed, 20 May 2026 19:09:43 GMT  
		Size: 8.7 KB (8744 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.9-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:a2d058ffac3e0982c4263c4a98357898b61eca619d2c56a76aac7b9f2d18f171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6373077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:130977b1791d287860791cbc0f238f4bf8902acceeb859fc8663ca013fc90b15`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:09:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:09:50 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:09:50 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:09:50 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:09:50 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:09:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:efec7643648fe287ed0901613783bcd23bb5a8b7b2fb2aee2e9f58a8d0d8d7a8`  
		Last Modified: Wed, 20 May 2026 16:04:26 GMT  
		Size: 6.4 MB (6372568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af920700845e87c0ae0d0a2e002936cf3fe153e0d75cd8d28e1fdebe0951676c`  
		Last Modified: Wed, 20 May 2026 19:09:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.9-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:a96c4eefe96a686ef87c6963d464d87de0be9f9d27e2e065a01137de83f6f1ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f334115d58195d99db72b89b7cd06f5d63fbbfe2344d46642d5e03925960c426`

```dockerfile
```

-	Layers:
	-	`sha256:44bb6f0b5261e2b3668d54d1d0f788b8e18dd4e2ba44ef27c0949c43398854e9`  
		Last Modified: Wed, 20 May 2026 19:09:54 GMT  
		Size: 8.7 KB (8744 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.9-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:aa8f7e3d55a383e35f019c28b6c432ed2090b3dad56fead3e7a70ab1dba79ccc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6037707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1b69482ef45b939a2908e033d22c9582db2b53dac733301472ace541c756069`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:10:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:10:14 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:10:14 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:10:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:10:14 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:10:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:81af0467f4bfb473e50c712e06ca48adff2e7aab8456b45fcfbc3fefe8ef6df7`  
		Last Modified: Wed, 20 May 2026 16:04:24 GMT  
		Size: 6.0 MB (6037200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed22b68f9def9c87dfb1c5a9ec34a809caf385bcdfdd456fd3be55b553020ad`  
		Last Modified: Wed, 20 May 2026 19:10:19 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.9-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:534c5df88f202c2a015c845378127d701cc4faf3641326573fce6c0fd64dbd1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0a9c9217edbec11dd3120e94f789339bb631670a66be81de8e106830fef4b4`

```dockerfile
```

-	Layers:
	-	`sha256:743146aaf7c71f426d7abd3b4db2abcd72ecfd72aed9db12cb025a3148324d81`  
		Last Modified: Wed, 20 May 2026 19:10:19 GMT  
		Size: 8.8 KB (8774 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.9-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:3a024c2519d3e8d9afa913cc70dc8a08f42c27841b819c13ae7f4746791667f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6100417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a86f1bedebf55c136505a6a6115d4879fd94839c05722c2813b743b911513fc7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:09:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:09:00 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:09:00 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:09:00 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:09:00 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:09:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8d94981a1be7de02d7553ad09e31ec60ee268df51c2ef4762da5828b6b45674`  
		Last Modified: Wed, 20 May 2026 16:04:23 GMT  
		Size: 6.1 MB (6099908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb234fae2f8c35c37c5a0a2b27b551816540b8c513f6b2c479728b77a462cc5`  
		Last Modified: Wed, 20 May 2026 19:09:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.9-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:4bc8adf9c89eb891276d88ad9ef5302e83c23305ea4eee6318fdf94156bf00f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c21faa8dd4d3dbf3346283035cadd5da1c813c60749a515846c980e8940f08d8`

```dockerfile
```

-	Layers:
	-	`sha256:dd4e6d8e65f686896f2c04a5c31ca21c193b8ac222cbaa55fc6cf1e4ecbc68d7`  
		Last Modified: Wed, 20 May 2026 19:09:06 GMT  
		Size: 8.7 KB (8715 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.9-scratch` - linux; s390x

```console
$ docker pull nats@sha256:0ff65b369dcf8b26046db1efa962fef20887641c137fba88592e99ac6d946759
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6491050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1fbd0e893d6064d2ae64507740f42429bfd8b6626f01ff155f71d68cbac6dfe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:10:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:10:29 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:10:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:10:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:10:30 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:10:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d668ec0d13619d02b98ac6e2ab2bb7ca3974ad1ed964fbbfae78e23a777df473`  
		Last Modified: Wed, 20 May 2026 16:04:26 GMT  
		Size: 6.5 MB (6490542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5c187c9ced3347b391d712fe3353958272e09460e48ef72b492e55332f67a0`  
		Last Modified: Wed, 20 May 2026 19:10:48 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.9-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:6868356eb5df018325b032eca1a4d9471a915135b6ad01baf74cbed5245b7581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74a49ccc3dc2aca4a464c76934f3739fa2e4fdbc49a4fe3a93d58e620431eba9`

```dockerfile
```

-	Layers:
	-	`sha256:beed34e5caa7d0f8bb8e9624e6acbd693112ad713d81a6ebe9751d3d4a144a83`  
		Last Modified: Wed, 20 May 2026 19:10:48 GMT  
		Size: 8.7 KB (8661 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12.9-windowsservercore`

```console
$ docker pull nats@sha256:93d7e77dc19ae1d7f04e86c2068da9a3b9e437892b266e13c64f28e1773223b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2.12.9-windowsservercore` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:e9d6a938ace06e341a366fc78d12f5aa1bd956dac71e4ff82158cb9eb81ac4c4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2130120651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1df05498b147c8f9c4865e19eb3f2266e06494384130ac34c45806311beb604`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Wed, 20 May 2026 18:42:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 20 May 2026 18:42:48 GMT
ENV NATS_DOCKERIZED=1
# Wed, 20 May 2026 18:59:48 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:59:48 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:59:50 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.9/nats-server-v2.12.9-windows-amd64.zip
# Wed, 20 May 2026 18:59:51 GMT
ENV NATS_SERVER_SHASUM=6d8d0b31ba2fbaca4613b9dbb1fd107c335ee26485f59fb9006e7ab34913117d
# Wed, 20 May 2026 18:59:59 GMT
RUN Set-PSDebug -Trace 2
# Wed, 20 May 2026 19:00:21 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 20 May 2026 19:00:22 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 20 May 2026 19:00:22 GMT
EXPOSE 4222 6222 8222
# Wed, 20 May 2026 19:00:23 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 20 May 2026 19:00:23 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9541aea3e55bd746462fb4c6e57da81839bbdd92cde8c45bec531dc275c949`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acaeb80d5acbf745ec935e19b9c27aac2c1c36569184a441931640832febb401`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f31a04aebe50db6f85e58a4df9a8d34f7df2bf36b2a1485ac21d1af7127d32c`  
		Last Modified: Wed, 20 May 2026 19:00:32 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c32221a695427881403603d85b9fbe9a208cafa19e27db15a2a87080b977aeb`  
		Last Modified: Wed, 20 May 2026 19:00:30 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fb78dc8e8b1e6679429c94711da7ef1a170469e7abd593d612090cbeabfc2ce`  
		Last Modified: Wed, 20 May 2026 19:00:30 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb3ca19f5131d5dac1c4bad13e5c900a1330ded4bc79991da462281aa3992a2a`  
		Last Modified: Wed, 20 May 2026 19:00:29 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67bc96c36328bd4cc9410563bf01b2c2ecae49584ea178bdb62d7b45109d586`  
		Last Modified: Wed, 20 May 2026 19:00:30 GMT  
		Size: 494.4 KB (494434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2a8ebf88f3c30a60da7b6608197c202a69ce7dd0ab6be014efbf6eadd2349f`  
		Last Modified: Wed, 20 May 2026 19:00:33 GMT  
		Size: 7.2 MB (7192011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e190bfa12df85ab9f289b0804e966103ffc0c26626f2c50e1a7409f5e5ed0855`  
		Last Modified: Wed, 20 May 2026 19:00:27 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7ce3c10c5a9944c33f1b695b2a9f04297226593bbaef9f132405493388c24c`  
		Last Modified: Wed, 20 May 2026 19:00:27 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6f580a22501d26e28952ee85653f70663980ab45953d0cfcbef50694db04d6`  
		Last Modified: Wed, 20 May 2026 19:00:28 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af4511ea5948cbca6aef9d7517e123f726b38c8a0eb9c947c2c4f6d7f54e0d88`  
		Last Modified: Wed, 20 May 2026 19:00:28 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12.9-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:93d7e77dc19ae1d7f04e86c2068da9a3b9e437892b266e13c64f28e1773223b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2.12.9-windowsservercore-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:e9d6a938ace06e341a366fc78d12f5aa1bd956dac71e4ff82158cb9eb81ac4c4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2130120651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1df05498b147c8f9c4865e19eb3f2266e06494384130ac34c45806311beb604`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Wed, 20 May 2026 18:42:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 20 May 2026 18:42:48 GMT
ENV NATS_DOCKERIZED=1
# Wed, 20 May 2026 18:59:48 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:59:48 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:59:50 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.9/nats-server-v2.12.9-windows-amd64.zip
# Wed, 20 May 2026 18:59:51 GMT
ENV NATS_SERVER_SHASUM=6d8d0b31ba2fbaca4613b9dbb1fd107c335ee26485f59fb9006e7ab34913117d
# Wed, 20 May 2026 18:59:59 GMT
RUN Set-PSDebug -Trace 2
# Wed, 20 May 2026 19:00:21 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 20 May 2026 19:00:22 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 20 May 2026 19:00:22 GMT
EXPOSE 4222 6222 8222
# Wed, 20 May 2026 19:00:23 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 20 May 2026 19:00:23 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9541aea3e55bd746462fb4c6e57da81839bbdd92cde8c45bec531dc275c949`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acaeb80d5acbf745ec935e19b9c27aac2c1c36569184a441931640832febb401`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f31a04aebe50db6f85e58a4df9a8d34f7df2bf36b2a1485ac21d1af7127d32c`  
		Last Modified: Wed, 20 May 2026 19:00:32 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c32221a695427881403603d85b9fbe9a208cafa19e27db15a2a87080b977aeb`  
		Last Modified: Wed, 20 May 2026 19:00:30 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fb78dc8e8b1e6679429c94711da7ef1a170469e7abd593d612090cbeabfc2ce`  
		Last Modified: Wed, 20 May 2026 19:00:30 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb3ca19f5131d5dac1c4bad13e5c900a1330ded4bc79991da462281aa3992a2a`  
		Last Modified: Wed, 20 May 2026 19:00:29 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67bc96c36328bd4cc9410563bf01b2c2ecae49584ea178bdb62d7b45109d586`  
		Last Modified: Wed, 20 May 2026 19:00:30 GMT  
		Size: 494.4 KB (494434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2a8ebf88f3c30a60da7b6608197c202a69ce7dd0ab6be014efbf6eadd2349f`  
		Last Modified: Wed, 20 May 2026 19:00:33 GMT  
		Size: 7.2 MB (7192011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e190bfa12df85ab9f289b0804e966103ffc0c26626f2c50e1a7409f5e5ed0855`  
		Last Modified: Wed, 20 May 2026 19:00:27 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7ce3c10c5a9944c33f1b695b2a9f04297226593bbaef9f132405493388c24c`  
		Last Modified: Wed, 20 May 2026 19:00:27 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6f580a22501d26e28952ee85653f70663980ab45953d0cfcbef50694db04d6`  
		Last Modified: Wed, 20 May 2026 19:00:28 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af4511ea5948cbca6aef9d7517e123f726b38c8a0eb9c947c2c4f6d7f54e0d88`  
		Last Modified: Wed, 20 May 2026 19:00:28 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.14`

```console
$ docker pull nats@sha256:7f430e429d0a90444b38bd40ab7812fd3afcc49a51f6b03a931f9becd5aeb280
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
	-	windows version 10.0.20348.5139; amd64

### `nats:2.14` - linux; amd64

```console
$ docker pull nats@sha256:aad7f400fa8a1cbcc2f818d5373638f91cfbfcac7cb9bd28fe6e8538c08b9c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6838210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39f65eeb0573eea876a604f186453a7a3cda0c8c511dd143432e1128e07a8734`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:10:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:10:38 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:10:38 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:10:38 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:10:38 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:10:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:05832d0be2949ff52eaf08a260411f3a4a020a066de4aa19dc62284052758304`  
		Last Modified: Wed, 20 May 2026 16:04:06 GMT  
		Size: 6.8 MB (6837703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a284b9b8e39214498d13f3dca35a9c9e81d34b69635ed74a3d47d26e45d5591`  
		Last Modified: Wed, 20 May 2026 19:10:42 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14` - unknown; unknown

```console
$ docker pull nats@sha256:6b2a0558891216e6e12622ac66d8766987858f507eee4cb4cfef25a0b1480e84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a061861dcdd34e8079637906d854df58e3e30fcfb0514aa93b4a1ada5b3936b9`

```dockerfile
```

-	Layers:
	-	`sha256:7fff463e51e2de542cc152e5196125c500561d37a866a78ab756f40188e25be6`  
		Last Modified: Wed, 20 May 2026 19:10:42 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14` - linux; arm variant v6

```console
$ docker pull nats@sha256:80f40fb067456022353b1754a4c58f49b1af454522a8af74e9c270e3a27668d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6573757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:039a8f82177ac58ba3952b7b25d8af7b14d0fbcf08e6e53efbab9e028b515cb5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:09:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:09:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:09:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:09:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:09:27 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:09:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3f675bd99a02bdb97f8ad1545908545b1e797e40d8038ce181205b0808044e20`  
		Last Modified: Wed, 20 May 2026 16:04:08 GMT  
		Size: 6.6 MB (6573248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715581626472620cc372593ae38a74d6c85239c0282bc3c5b7937fcd525bb308`  
		Last Modified: Wed, 20 May 2026 19:09:32 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14` - unknown; unknown

```console
$ docker pull nats@sha256:cd80c2a5593667a467031df5e49c9cab2cc1f5ae03e981c4789d7a262cbded23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac98f8edc0ec201da45e4d96bc1ea96d553e89648a61e35f8a195d38ce81d6b9`

```dockerfile
```

-	Layers:
	-	`sha256:d7cd588a4563631d4b86b381c7ee1c56114f94b80568f0e8defc278961b4c119`  
		Last Modified: Wed, 20 May 2026 19:09:31 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14` - linux; arm variant v7

```console
$ docker pull nats@sha256:ae43b4e3d705ed3a3386e6b303d8dfb011fec9e1cdf8523ff9c6387935d9652d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6565185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a493ff1dda3a5eb2f84019be4a31029f9463e5a91f142d91cbd96345245eadb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:09:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:09:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:09:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:09:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:09:01 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:09:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:07a4ad6a636748b056dca5d82613a936ff1872d9092911832cea1178d840cb7f`  
		Last Modified: Wed, 20 May 2026 16:04:08 GMT  
		Size: 6.6 MB (6564678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95ec1a5b2af5f3d81a39b2563595f7008790713449f52e148c254bc7d0be80e`  
		Last Modified: Wed, 20 May 2026 19:09:06 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14` - unknown; unknown

```console
$ docker pull nats@sha256:5b515d7d9aa87098056bad17534ca266bba383a9a52d362a1788c5ac7b596d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a1b7811acc104229e8cc148ff624e24efc4e31d06fce27cdd9091dd3237110`

```dockerfile
```

-	Layers:
	-	`sha256:e855458d7f5e87be1456ba294fc7386adaa0241520ff73ab4b95b94271f3d0a0`  
		Last Modified: Wed, 20 May 2026 19:09:05 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:89ea5f3d1a4e7db9650685b4b60d5f2340f6edd89f0d2a7a6f2a5cb9b6f144c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6189602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:080d11e023e3c9bc77bc5d6e137c30fcee2ca537fbda1d730ee0de9b5131cf97`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:10:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:10:02 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:10:02 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:10:02 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:10:02 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:10:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5f2fe2216ecafda68f73a81334875cb85722e57f12bc2af372cc03c4952017ff`  
		Last Modified: Wed, 20 May 2026 16:04:06 GMT  
		Size: 6.2 MB (6189094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f13aa02931bd62f5d9ce1935b8f163c6fcb3db670a4893037e6326c70ff971`  
		Last Modified: Wed, 20 May 2026 19:10:07 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14` - unknown; unknown

```console
$ docker pull nats@sha256:55f5544491f15bb813013ec1a1698f6e7e6f1ebbf96b4e49dba94dab9c27b313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30316b20c5d7aabdc5ded4b132f0725f10bdb7bd31bfbdb309184a8e58efe00c`

```dockerfile
```

-	Layers:
	-	`sha256:e06f44f5e5db93fe4fba02df22b44d37f71209d0cfbcbcec67b2ec6687bda27c`  
		Last Modified: Wed, 20 May 2026 19:10:07 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14` - linux; ppc64le

```console
$ docker pull nats@sha256:9b9d19890e9399f86300407959de41b794ee8fd1b46720c7548163f7f94fd15e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6254150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dcae0dec9d781a4ed3bd8282b836bb0fc168482d57def8fec57c690ecdd111a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:09:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:09:00 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:09:00 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:09:00 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:09:00 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:09:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:eeebf06eacfa887b3524b3c76a2593bb68e43a09aa8ff01b5a09c0ce44ed2917`  
		Last Modified: Wed, 20 May 2026 16:04:05 GMT  
		Size: 6.3 MB (6253641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb234fae2f8c35c37c5a0a2b27b551816540b8c513f6b2c479728b77a462cc5`  
		Last Modified: Wed, 20 May 2026 19:09:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14` - unknown; unknown

```console
$ docker pull nats@sha256:44cc5336af1db8f2f590eca54680623452cbb2da64b65bb690521c087a9be389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2bccd9ad485d0016ce5f53e02daf116336befd19e206a354f9324e36b86c720`

```dockerfile
```

-	Layers:
	-	`sha256:33b891cec5ef0cfb52212abc7e2148afd94f43e4c045f9b8ee11b24532349469`  
		Last Modified: Wed, 20 May 2026 19:09:06 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14` - linux; s390x

```console
$ docker pull nats@sha256:02ac81902397bc3ce3ae4f6bf57bb15925e02525fc49567e8db5747ae9e3cc7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6650240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f5f893e9ed2e5671b5afc696c46fd6aa4099811ef87a81fb46e2bf0c84ba84f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:10:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:10:22 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:10:24 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:10:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:10:24 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:10:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9e00525b36acc41f758b0363af2261253b6d35899fd8e6c7e6b4d30ff05eab43`  
		Last Modified: Wed, 20 May 2026 16:04:08 GMT  
		Size: 6.6 MB (6649731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61970d60cef7c5abc0f2985fb3486911eb5ae086553cd2bfb895dd97daa5dbe1`  
		Last Modified: Wed, 20 May 2026 19:10:43 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14` - unknown; unknown

```console
$ docker pull nats@sha256:91a6b246de893cdf55e56ebb0f717eb35cb29121fd44454bb5c2e66fe76ba11b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b822bf8bf39b54c102cf252c8b091bac1a2c642851dd34cc7445f10b19fbbe42`

```dockerfile
```

-	Layers:
	-	`sha256:a39452d35088530375cff827daeae3695859d1f87479bba2523d135b3256d905`  
		Last Modified: Wed, 20 May 2026 19:10:43 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:ad04df86864a0653927e5ff2293212d694588db88edc746ce8b917417317c0f3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134078105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc7e5bd03f66dabebd5917cf13f4067081477a5934e86d07357d04db10e33ec4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 20 May 2026 19:09:14 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 20 May 2026 19:09:15 GMT
RUN cmd /S /C #(nop) COPY file:5d608f6a5cbf80544d196a9ac38d66b2635084a5e0a392611785993205e5329d in C:\nats-server.exe 
# Wed, 20 May 2026 19:09:16 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 20 May 2026 19:09:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 20 May 2026 19:09:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 20 May 2026 19:09:18 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c815e3255991cc2df065c98a27664be46d8b5db04231449f637ecaf64c5c098f`  
		Last Modified: Wed, 20 May 2026 19:09:24 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68983020294e3083531b7192194e9d5172d2a1449eac04682b7544bb139048b5`  
		Last Modified: Wed, 20 May 2026 19:09:27 GMT  
		Size: 7.0 MB (7033380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730756958a80b0245caf373feb8024993ecef9e67a8ade759511f66d001f3f07`  
		Last Modified: Wed, 20 May 2026 19:09:22 GMT  
		Size: 1.7 KB (1672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ec9d4f153ff90a362ff5591192559ff2e3584441d0bee4e4fdd8b0a4845b833`  
		Last Modified: Wed, 20 May 2026 19:09:22 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb6e35267fc994af8eab6412783ba571dd4c1d14e5fa8771f50a386e61ef655`  
		Last Modified: Wed, 20 May 2026 19:09:22 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838e55b2d659c4cc5f4e0db1773fbe38aa8487984688f5a0f60b202907588e42`  
		Last Modified: Wed, 20 May 2026 19:09:22 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.14-alpine`

```console
$ docker pull nats@sha256:ea17b9b7f74279b9239cf65e5786c0133e9a7c353bf218d29004abf2e7a33181
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

### `nats:2.14-alpine` - linux; amd64

```console
$ docker pull nats@sha256:4c516667ffae4977a0b4ee1d8caa5b663a0d147b66c6b2adc8ee8f3e23728bc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11103220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c133130b2f2f46568f11546ffef920fccb739e99fd733ef11ea43fc1737887c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:37:17 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:37:17 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:37:17 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:37:17 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:37:17 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:37:17 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:37:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:37:17 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6887181943c337b002058eb52d1b08afbc55add7c29a34ac80e3949090e15495`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 7.3 MB (7294060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a070bfd7422a373dc1b206300e1798aef404bf1bac5a04a3293b33f5468a167e`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4a08ddee9fc679f6a40d1ca0c325ec632bebcbb19437245764df5d7ccb6e0d`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:16deabb6f9a013834b95f04987ebab3d889f6704db15b71e13e10a4109b2e5b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d0fdb19df33d866a3c0b19c2d8aa933518ea4afc5b2f7562f2fd9364bb805ec`

```dockerfile
```

-	Layers:
	-	`sha256:650380b0910269f4395d628fbfafe98d4c910cc7a775ff48fa5093aaddc18b1f`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 15.4 KB (15403 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:32e7eb3bde61b1a81ba030cf21530f82b3713f20585f14da348ed9ff0099cd38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10540472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff1b400cc41fb9599883d47ee0cc98f26d14432cafaa79d7b00c36500c3be581`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:35:40 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:35:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:35:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:35:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac441e30d31da40cce92ca13be29a2ec33b8e530c12f39c4e6e6f821d36fa5f7`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 7.0 MB (7032117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588069c44453627769cbea386971dc510fa0a2a33fc33bc21795cbe4c6ceeb2e`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1efc9734efaa0feb255b7c30b046fb56094635c7d947db2f21f7a873a06b52a`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:e8fdb1f5ad9c517ef1795cc413d10f4304bac0bfacca20197b1324ceed658bd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67da2ba5e6d5168c0687521d71e8357c05504026864365687620573485a04e0`

```dockerfile
```

-	Layers:
	-	`sha256:63de3f19bc13cbd3dc2f28506681e74ef898d6cddd4ed65551521f9d641ff6b5`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:8805cf2aaa214d58393f7373011c4fe330f5225fb9bc4da6d715a6ab72ff8dc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10246493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32278cb7a1bf5e3ea24f7381d52c844e152750efbf7684af40245538a2fadaa4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:35:40 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:35:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:35:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:35:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3e43a7f3a2149acbd98329815e7e03d9dcf933d2131db6f8e1eecd1c01e173`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 7.0 MB (7019690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588069c44453627769cbea386971dc510fa0a2a33fc33bc21795cbe4c6ceeb2e`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9213cf8ea08c3ce1080672b9ea4c12034482854a1829a814ec22933ea91379a0`  
		Last Modified: Wed, 20 May 2026 18:35:44 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:83439ca6685120afbf799cb62bebb64b76d3419bd2523ae781dfad0b8bd8db9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f56fa87064674ea90080bd544ca88fd1b1f257088b93998a8cd46405b6249c`

```dockerfile
```

-	Layers:
	-	`sha256:22deddd2f98e84c9bc37c96058b3e88416465a5ea1004b4985cef2385de5a8be`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 15.5 KB (15515 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:abc668a25359714d7320be16684a7a6096d82a6d41aa9fbb4275c02f3fb1e716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10791094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c04c7a60cc127abb4b03f7f7593fb48cd0124f4f2cd959996fdcb5caba71e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:37:01 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:37:01 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:37:01 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:37:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:37:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:37:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:37:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:37:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b89c7be0c2d2557967711fd66cb73b3b64361381d066e02f0b52b2abeedd6b9`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 6.6 MB (6648233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b1bf5ee681da0d7929bf7d0e36bf5d24df48f214a25c32a7692f9fd0bc5eab`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2e67e1deca529e76612c525c5a8e12050d9ec84c3691673953e51573c1e653`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:5ae7b0317944de344d87247e9cb05a11dcd4f796e1800294193d7b60f43c9d9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9059f595926bbcc76e88f995c69a532e5bfdb37e53db7d9cbd26077b9a0f52d1`

```dockerfile
```

-	Layers:
	-	`sha256:a10a07e60572ceb3113b276c9a02c5aa46bf940b8f2a491e7064608fcac2409c`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:7c13d10c1f7169aaedc2ac8ecbc1f431dda7e906455b836d09a14b3b948f3036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10448793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa266dd5df001f7f566ffb0c8c8acff2de160efa06508788758a4e3022c8e98d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:39:54 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:39:54 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:39:54 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:39:55 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:39:55 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:39:55 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:39:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:39:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efe06b0c545d8e510a8131fe2984aa46a7c4d7502148ce8f2e94df5ffeed78f`  
		Last Modified: Wed, 20 May 2026 18:40:02 GMT  
		Size: 6.7 MB (6711165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3c6e5710602d0c65abfcc3a4aac8676e3cd1f849d5967bee0654b0ec045abe`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0fcc4ed5f0f4848feb91f0e5c409cb87bfd693a7056f2c0e574dbf0fc8ff4ab`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:7878f9d371c5d9227beef40f16b5dfd6d37465bab0104f835171af841d4c4a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47a1ee27b4ce5d60016cbff052995f2dbab1c7c6c61dcf79e2f75cbb1430fbad`

```dockerfile
```

-	Layers:
	-	`sha256:c27fc7351e2a880436edb13f3b1eaf0c5d83b4ec4a761386db3f8a0e0e8642a5`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine` - linux; s390x

```console
$ docker pull nats@sha256:458d20eff2bdbc011304724399fc06b3db7dae7c95d0c806969fc503389a70c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10757148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0002a7df6776ecf8e0df1b73510a6014c1f519a3c9692cd787d8568dd8021d99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:48:37 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:48:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:48:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:48:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:48:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:48:43 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:48:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:48:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728aea4976117b7918cb9446c013c273cae16aa21337089d91cbd93761d10ae5`  
		Last Modified: Wed, 20 May 2026 18:49:10 GMT  
		Size: 7.1 MB (7102303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e102ba28952cc8bf83cffaefb3ec4b38d56cd736120ece8c71362ff603fd09b`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec22f8c91bd1e1b2e7f49773754ab16299137dd3226c8bb660a538d249364ae6`  
		Last Modified: Wed, 20 May 2026 18:49:08 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:38a69833b514d10d0b925fa5c4639cb5d17abe985f2b30699a0f305324397aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cffc57189208991582e7a0262e60b1415e19ac3919981144973c3d19428e23f6`

```dockerfile
```

-	Layers:
	-	`sha256:ccc40928ae38a1bd914e972d9acbe81dbc2e36b6132cee1761b8e20e7dda2db5`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.14-alpine3.22`

```console
$ docker pull nats@sha256:ea17b9b7f74279b9239cf65e5786c0133e9a7c353bf218d29004abf2e7a33181
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

### `nats:2.14-alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:4c516667ffae4977a0b4ee1d8caa5b663a0d147b66c6b2adc8ee8f3e23728bc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11103220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c133130b2f2f46568f11546ffef920fccb739e99fd733ef11ea43fc1737887c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:37:17 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:37:17 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:37:17 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:37:17 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:37:17 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:37:17 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:37:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:37:17 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6887181943c337b002058eb52d1b08afbc55add7c29a34ac80e3949090e15495`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 7.3 MB (7294060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a070bfd7422a373dc1b206300e1798aef404bf1bac5a04a3293b33f5468a167e`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4a08ddee9fc679f6a40d1ca0c325ec632bebcbb19437245764df5d7ccb6e0d`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:16deabb6f9a013834b95f04987ebab3d889f6704db15b71e13e10a4109b2e5b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d0fdb19df33d866a3c0b19c2d8aa933518ea4afc5b2f7562f2fd9364bb805ec`

```dockerfile
```

-	Layers:
	-	`sha256:650380b0910269f4395d628fbfafe98d4c910cc7a775ff48fa5093aaddc18b1f`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 15.4 KB (15403 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:32e7eb3bde61b1a81ba030cf21530f82b3713f20585f14da348ed9ff0099cd38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10540472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff1b400cc41fb9599883d47ee0cc98f26d14432cafaa79d7b00c36500c3be581`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:35:40 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:35:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:35:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:35:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac441e30d31da40cce92ca13be29a2ec33b8e530c12f39c4e6e6f821d36fa5f7`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 7.0 MB (7032117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588069c44453627769cbea386971dc510fa0a2a33fc33bc21795cbe4c6ceeb2e`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1efc9734efaa0feb255b7c30b046fb56094635c7d947db2f21f7a873a06b52a`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:e8fdb1f5ad9c517ef1795cc413d10f4304bac0bfacca20197b1324ceed658bd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67da2ba5e6d5168c0687521d71e8357c05504026864365687620573485a04e0`

```dockerfile
```

-	Layers:
	-	`sha256:63de3f19bc13cbd3dc2f28506681e74ef898d6cddd4ed65551521f9d641ff6b5`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:8805cf2aaa214d58393f7373011c4fe330f5225fb9bc4da6d715a6ab72ff8dc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10246493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32278cb7a1bf5e3ea24f7381d52c844e152750efbf7684af40245538a2fadaa4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:35:40 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:35:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:35:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:35:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3e43a7f3a2149acbd98329815e7e03d9dcf933d2131db6f8e1eecd1c01e173`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 7.0 MB (7019690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588069c44453627769cbea386971dc510fa0a2a33fc33bc21795cbe4c6ceeb2e`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9213cf8ea08c3ce1080672b9ea4c12034482854a1829a814ec22933ea91379a0`  
		Last Modified: Wed, 20 May 2026 18:35:44 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:83439ca6685120afbf799cb62bebb64b76d3419bd2523ae781dfad0b8bd8db9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f56fa87064674ea90080bd544ca88fd1b1f257088b93998a8cd46405b6249c`

```dockerfile
```

-	Layers:
	-	`sha256:22deddd2f98e84c9bc37c96058b3e88416465a5ea1004b4985cef2385de5a8be`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 15.5 KB (15515 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:abc668a25359714d7320be16684a7a6096d82a6d41aa9fbb4275c02f3fb1e716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10791094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c04c7a60cc127abb4b03f7f7593fb48cd0124f4f2cd959996fdcb5caba71e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:37:01 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:37:01 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:37:01 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:37:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:37:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:37:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:37:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:37:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b89c7be0c2d2557967711fd66cb73b3b64361381d066e02f0b52b2abeedd6b9`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 6.6 MB (6648233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b1bf5ee681da0d7929bf7d0e36bf5d24df48f214a25c32a7692f9fd0bc5eab`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2e67e1deca529e76612c525c5a8e12050d9ec84c3691673953e51573c1e653`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:5ae7b0317944de344d87247e9cb05a11dcd4f796e1800294193d7b60f43c9d9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9059f595926bbcc76e88f995c69a532e5bfdb37e53db7d9cbd26077b9a0f52d1`

```dockerfile
```

-	Layers:
	-	`sha256:a10a07e60572ceb3113b276c9a02c5aa46bf940b8f2a491e7064608fcac2409c`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:7c13d10c1f7169aaedc2ac8ecbc1f431dda7e906455b836d09a14b3b948f3036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10448793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa266dd5df001f7f566ffb0c8c8acff2de160efa06508788758a4e3022c8e98d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:39:54 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:39:54 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:39:54 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:39:55 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:39:55 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:39:55 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:39:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:39:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efe06b0c545d8e510a8131fe2984aa46a7c4d7502148ce8f2e94df5ffeed78f`  
		Last Modified: Wed, 20 May 2026 18:40:02 GMT  
		Size: 6.7 MB (6711165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3c6e5710602d0c65abfcc3a4aac8676e3cd1f849d5967bee0654b0ec045abe`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0fcc4ed5f0f4848feb91f0e5c409cb87bfd693a7056f2c0e574dbf0fc8ff4ab`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:7878f9d371c5d9227beef40f16b5dfd6d37465bab0104f835171af841d4c4a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47a1ee27b4ce5d60016cbff052995f2dbab1c7c6c61dcf79e2f75cbb1430fbad`

```dockerfile
```

-	Layers:
	-	`sha256:c27fc7351e2a880436edb13f3b1eaf0c5d83b4ec4a761386db3f8a0e0e8642a5`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:458d20eff2bdbc011304724399fc06b3db7dae7c95d0c806969fc503389a70c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10757148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0002a7df6776ecf8e0df1b73510a6014c1f519a3c9692cd787d8568dd8021d99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:48:37 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:48:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:48:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:48:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:48:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:48:43 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:48:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:48:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728aea4976117b7918cb9446c013c273cae16aa21337089d91cbd93761d10ae5`  
		Last Modified: Wed, 20 May 2026 18:49:10 GMT  
		Size: 7.1 MB (7102303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e102ba28952cc8bf83cffaefb3ec4b38d56cd736120ece8c71362ff603fd09b`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec22f8c91bd1e1b2e7f49773754ab16299137dd3226c8bb660a538d249364ae6`  
		Last Modified: Wed, 20 May 2026 18:49:08 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:38a69833b514d10d0b925fa5c4639cb5d17abe985f2b30699a0f305324397aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cffc57189208991582e7a0262e60b1415e19ac3919981144973c3d19428e23f6`

```dockerfile
```

-	Layers:
	-	`sha256:ccc40928ae38a1bd914e972d9acbe81dbc2e36b6132cee1761b8e20e7dda2db5`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.14-linux`

```console
$ docker pull nats@sha256:4223c8fa116891628611e154fb66570cad599d8f8b3b131b82caf10f378e9dcf
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

### `nats:2.14-linux` - linux; amd64

```console
$ docker pull nats@sha256:aad7f400fa8a1cbcc2f818d5373638f91cfbfcac7cb9bd28fe6e8538c08b9c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6838210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39f65eeb0573eea876a604f186453a7a3cda0c8c511dd143432e1128e07a8734`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:10:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:10:38 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:10:38 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:10:38 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:10:38 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:10:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:05832d0be2949ff52eaf08a260411f3a4a020a066de4aa19dc62284052758304`  
		Last Modified: Wed, 20 May 2026 16:04:06 GMT  
		Size: 6.8 MB (6837703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a284b9b8e39214498d13f3dca35a9c9e81d34b69635ed74a3d47d26e45d5591`  
		Last Modified: Wed, 20 May 2026 19:10:42 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-linux` - unknown; unknown

```console
$ docker pull nats@sha256:6b2a0558891216e6e12622ac66d8766987858f507eee4cb4cfef25a0b1480e84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a061861dcdd34e8079637906d854df58e3e30fcfb0514aa93b4a1ada5b3936b9`

```dockerfile
```

-	Layers:
	-	`sha256:7fff463e51e2de542cc152e5196125c500561d37a866a78ab756f40188e25be6`  
		Last Modified: Wed, 20 May 2026 19:10:42 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:80f40fb067456022353b1754a4c58f49b1af454522a8af74e9c270e3a27668d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6573757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:039a8f82177ac58ba3952b7b25d8af7b14d0fbcf08e6e53efbab9e028b515cb5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:09:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:09:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:09:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:09:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:09:27 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:09:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3f675bd99a02bdb97f8ad1545908545b1e797e40d8038ce181205b0808044e20`  
		Last Modified: Wed, 20 May 2026 16:04:08 GMT  
		Size: 6.6 MB (6573248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715581626472620cc372593ae38a74d6c85239c0282bc3c5b7937fcd525bb308`  
		Last Modified: Wed, 20 May 2026 19:09:32 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-linux` - unknown; unknown

```console
$ docker pull nats@sha256:cd80c2a5593667a467031df5e49c9cab2cc1f5ae03e981c4789d7a262cbded23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac98f8edc0ec201da45e4d96bc1ea96d553e89648a61e35f8a195d38ce81d6b9`

```dockerfile
```

-	Layers:
	-	`sha256:d7cd588a4563631d4b86b381c7ee1c56114f94b80568f0e8defc278961b4c119`  
		Last Modified: Wed, 20 May 2026 19:09:31 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:ae43b4e3d705ed3a3386e6b303d8dfb011fec9e1cdf8523ff9c6387935d9652d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6565185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a493ff1dda3a5eb2f84019be4a31029f9463e5a91f142d91cbd96345245eadb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:09:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:09:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:09:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:09:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:09:01 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:09:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:07a4ad6a636748b056dca5d82613a936ff1872d9092911832cea1178d840cb7f`  
		Last Modified: Wed, 20 May 2026 16:04:08 GMT  
		Size: 6.6 MB (6564678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95ec1a5b2af5f3d81a39b2563595f7008790713449f52e148c254bc7d0be80e`  
		Last Modified: Wed, 20 May 2026 19:09:06 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-linux` - unknown; unknown

```console
$ docker pull nats@sha256:5b515d7d9aa87098056bad17534ca266bba383a9a52d362a1788c5ac7b596d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a1b7811acc104229e8cc148ff624e24efc4e31d06fce27cdd9091dd3237110`

```dockerfile
```

-	Layers:
	-	`sha256:e855458d7f5e87be1456ba294fc7386adaa0241520ff73ab4b95b94271f3d0a0`  
		Last Modified: Wed, 20 May 2026 19:09:05 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:89ea5f3d1a4e7db9650685b4b60d5f2340f6edd89f0d2a7a6f2a5cb9b6f144c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6189602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:080d11e023e3c9bc77bc5d6e137c30fcee2ca537fbda1d730ee0de9b5131cf97`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:10:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:10:02 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:10:02 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:10:02 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:10:02 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:10:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5f2fe2216ecafda68f73a81334875cb85722e57f12bc2af372cc03c4952017ff`  
		Last Modified: Wed, 20 May 2026 16:04:06 GMT  
		Size: 6.2 MB (6189094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f13aa02931bd62f5d9ce1935b8f163c6fcb3db670a4893037e6326c70ff971`  
		Last Modified: Wed, 20 May 2026 19:10:07 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-linux` - unknown; unknown

```console
$ docker pull nats@sha256:55f5544491f15bb813013ec1a1698f6e7e6f1ebbf96b4e49dba94dab9c27b313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30316b20c5d7aabdc5ded4b132f0725f10bdb7bd31bfbdb309184a8e58efe00c`

```dockerfile
```

-	Layers:
	-	`sha256:e06f44f5e5db93fe4fba02df22b44d37f71209d0cfbcbcec67b2ec6687bda27c`  
		Last Modified: Wed, 20 May 2026 19:10:07 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:9b9d19890e9399f86300407959de41b794ee8fd1b46720c7548163f7f94fd15e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6254150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dcae0dec9d781a4ed3bd8282b836bb0fc168482d57def8fec57c690ecdd111a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:09:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:09:00 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:09:00 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:09:00 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:09:00 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:09:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:eeebf06eacfa887b3524b3c76a2593bb68e43a09aa8ff01b5a09c0ce44ed2917`  
		Last Modified: Wed, 20 May 2026 16:04:05 GMT  
		Size: 6.3 MB (6253641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb234fae2f8c35c37c5a0a2b27b551816540b8c513f6b2c479728b77a462cc5`  
		Last Modified: Wed, 20 May 2026 19:09:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-linux` - unknown; unknown

```console
$ docker pull nats@sha256:44cc5336af1db8f2f590eca54680623452cbb2da64b65bb690521c087a9be389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2bccd9ad485d0016ce5f53e02daf116336befd19e206a354f9324e36b86c720`

```dockerfile
```

-	Layers:
	-	`sha256:33b891cec5ef0cfb52212abc7e2148afd94f43e4c045f9b8ee11b24532349469`  
		Last Modified: Wed, 20 May 2026 19:09:06 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-linux` - linux; s390x

```console
$ docker pull nats@sha256:02ac81902397bc3ce3ae4f6bf57bb15925e02525fc49567e8db5747ae9e3cc7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6650240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f5f893e9ed2e5671b5afc696c46fd6aa4099811ef87a81fb46e2bf0c84ba84f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:10:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:10:22 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:10:24 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:10:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:10:24 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:10:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9e00525b36acc41f758b0363af2261253b6d35899fd8e6c7e6b4d30ff05eab43`  
		Last Modified: Wed, 20 May 2026 16:04:08 GMT  
		Size: 6.6 MB (6649731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61970d60cef7c5abc0f2985fb3486911eb5ae086553cd2bfb895dd97daa5dbe1`  
		Last Modified: Wed, 20 May 2026 19:10:43 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-linux` - unknown; unknown

```console
$ docker pull nats@sha256:91a6b246de893cdf55e56ebb0f717eb35cb29121fd44454bb5c2e66fe76ba11b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b822bf8bf39b54c102cf252c8b091bac1a2c642851dd34cc7445f10b19fbbe42`

```dockerfile
```

-	Layers:
	-	`sha256:a39452d35088530375cff827daeae3695859d1f87479bba2523d135b3256d905`  
		Last Modified: Wed, 20 May 2026 19:10:43 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.14-nanoserver`

```console
$ docker pull nats@sha256:b8d325261e82cfa9b4561b3752e5791fc51c257bde48ca6e1ae65580749766a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2.14-nanoserver` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:ad04df86864a0653927e5ff2293212d694588db88edc746ce8b917417317c0f3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134078105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc7e5bd03f66dabebd5917cf13f4067081477a5934e86d07357d04db10e33ec4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 20 May 2026 19:09:14 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 20 May 2026 19:09:15 GMT
RUN cmd /S /C #(nop) COPY file:5d608f6a5cbf80544d196a9ac38d66b2635084a5e0a392611785993205e5329d in C:\nats-server.exe 
# Wed, 20 May 2026 19:09:16 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 20 May 2026 19:09:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 20 May 2026 19:09:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 20 May 2026 19:09:18 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c815e3255991cc2df065c98a27664be46d8b5db04231449f637ecaf64c5c098f`  
		Last Modified: Wed, 20 May 2026 19:09:24 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68983020294e3083531b7192194e9d5172d2a1449eac04682b7544bb139048b5`  
		Last Modified: Wed, 20 May 2026 19:09:27 GMT  
		Size: 7.0 MB (7033380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730756958a80b0245caf373feb8024993ecef9e67a8ade759511f66d001f3f07`  
		Last Modified: Wed, 20 May 2026 19:09:22 GMT  
		Size: 1.7 KB (1672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ec9d4f153ff90a362ff5591192559ff2e3584441d0bee4e4fdd8b0a4845b833`  
		Last Modified: Wed, 20 May 2026 19:09:22 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb6e35267fc994af8eab6412783ba571dd4c1d14e5fa8771f50a386e61ef655`  
		Last Modified: Wed, 20 May 2026 19:09:22 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838e55b2d659c4cc5f4e0db1773fbe38aa8487984688f5a0f60b202907588e42`  
		Last Modified: Wed, 20 May 2026 19:09:22 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.14-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:b8d325261e82cfa9b4561b3752e5791fc51c257bde48ca6e1ae65580749766a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2.14-nanoserver-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:ad04df86864a0653927e5ff2293212d694588db88edc746ce8b917417317c0f3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134078105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc7e5bd03f66dabebd5917cf13f4067081477a5934e86d07357d04db10e33ec4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 20 May 2026 19:09:14 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 20 May 2026 19:09:15 GMT
RUN cmd /S /C #(nop) COPY file:5d608f6a5cbf80544d196a9ac38d66b2635084a5e0a392611785993205e5329d in C:\nats-server.exe 
# Wed, 20 May 2026 19:09:16 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 20 May 2026 19:09:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 20 May 2026 19:09:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 20 May 2026 19:09:18 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c815e3255991cc2df065c98a27664be46d8b5db04231449f637ecaf64c5c098f`  
		Last Modified: Wed, 20 May 2026 19:09:24 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68983020294e3083531b7192194e9d5172d2a1449eac04682b7544bb139048b5`  
		Last Modified: Wed, 20 May 2026 19:09:27 GMT  
		Size: 7.0 MB (7033380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730756958a80b0245caf373feb8024993ecef9e67a8ade759511f66d001f3f07`  
		Last Modified: Wed, 20 May 2026 19:09:22 GMT  
		Size: 1.7 KB (1672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ec9d4f153ff90a362ff5591192559ff2e3584441d0bee4e4fdd8b0a4845b833`  
		Last Modified: Wed, 20 May 2026 19:09:22 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb6e35267fc994af8eab6412783ba571dd4c1d14e5fa8771f50a386e61ef655`  
		Last Modified: Wed, 20 May 2026 19:09:22 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838e55b2d659c4cc5f4e0db1773fbe38aa8487984688f5a0f60b202907588e42`  
		Last Modified: Wed, 20 May 2026 19:09:22 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.14-scratch`

```console
$ docker pull nats@sha256:4223c8fa116891628611e154fb66570cad599d8f8b3b131b82caf10f378e9dcf
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

### `nats:2.14-scratch` - linux; amd64

```console
$ docker pull nats@sha256:aad7f400fa8a1cbcc2f818d5373638f91cfbfcac7cb9bd28fe6e8538c08b9c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6838210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39f65eeb0573eea876a604f186453a7a3cda0c8c511dd143432e1128e07a8734`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:10:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:10:38 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:10:38 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:10:38 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:10:38 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:10:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:05832d0be2949ff52eaf08a260411f3a4a020a066de4aa19dc62284052758304`  
		Last Modified: Wed, 20 May 2026 16:04:06 GMT  
		Size: 6.8 MB (6837703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a284b9b8e39214498d13f3dca35a9c9e81d34b69635ed74a3d47d26e45d5591`  
		Last Modified: Wed, 20 May 2026 19:10:42 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:6b2a0558891216e6e12622ac66d8766987858f507eee4cb4cfef25a0b1480e84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a061861dcdd34e8079637906d854df58e3e30fcfb0514aa93b4a1ada5b3936b9`

```dockerfile
```

-	Layers:
	-	`sha256:7fff463e51e2de542cc152e5196125c500561d37a866a78ab756f40188e25be6`  
		Last Modified: Wed, 20 May 2026 19:10:42 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:80f40fb067456022353b1754a4c58f49b1af454522a8af74e9c270e3a27668d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6573757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:039a8f82177ac58ba3952b7b25d8af7b14d0fbcf08e6e53efbab9e028b515cb5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:09:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:09:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:09:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:09:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:09:27 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:09:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3f675bd99a02bdb97f8ad1545908545b1e797e40d8038ce181205b0808044e20`  
		Last Modified: Wed, 20 May 2026 16:04:08 GMT  
		Size: 6.6 MB (6573248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715581626472620cc372593ae38a74d6c85239c0282bc3c5b7937fcd525bb308`  
		Last Modified: Wed, 20 May 2026 19:09:32 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:cd80c2a5593667a467031df5e49c9cab2cc1f5ae03e981c4789d7a262cbded23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac98f8edc0ec201da45e4d96bc1ea96d553e89648a61e35f8a195d38ce81d6b9`

```dockerfile
```

-	Layers:
	-	`sha256:d7cd588a4563631d4b86b381c7ee1c56114f94b80568f0e8defc278961b4c119`  
		Last Modified: Wed, 20 May 2026 19:09:31 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:ae43b4e3d705ed3a3386e6b303d8dfb011fec9e1cdf8523ff9c6387935d9652d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6565185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a493ff1dda3a5eb2f84019be4a31029f9463e5a91f142d91cbd96345245eadb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:09:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:09:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:09:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:09:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:09:01 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:09:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:07a4ad6a636748b056dca5d82613a936ff1872d9092911832cea1178d840cb7f`  
		Last Modified: Wed, 20 May 2026 16:04:08 GMT  
		Size: 6.6 MB (6564678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95ec1a5b2af5f3d81a39b2563595f7008790713449f52e148c254bc7d0be80e`  
		Last Modified: Wed, 20 May 2026 19:09:06 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:5b515d7d9aa87098056bad17534ca266bba383a9a52d362a1788c5ac7b596d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a1b7811acc104229e8cc148ff624e24efc4e31d06fce27cdd9091dd3237110`

```dockerfile
```

-	Layers:
	-	`sha256:e855458d7f5e87be1456ba294fc7386adaa0241520ff73ab4b95b94271f3d0a0`  
		Last Modified: Wed, 20 May 2026 19:09:05 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:89ea5f3d1a4e7db9650685b4b60d5f2340f6edd89f0d2a7a6f2a5cb9b6f144c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6189602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:080d11e023e3c9bc77bc5d6e137c30fcee2ca537fbda1d730ee0de9b5131cf97`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:10:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:10:02 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:10:02 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:10:02 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:10:02 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:10:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5f2fe2216ecafda68f73a81334875cb85722e57f12bc2af372cc03c4952017ff`  
		Last Modified: Wed, 20 May 2026 16:04:06 GMT  
		Size: 6.2 MB (6189094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f13aa02931bd62f5d9ce1935b8f163c6fcb3db670a4893037e6326c70ff971`  
		Last Modified: Wed, 20 May 2026 19:10:07 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:55f5544491f15bb813013ec1a1698f6e7e6f1ebbf96b4e49dba94dab9c27b313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30316b20c5d7aabdc5ded4b132f0725f10bdb7bd31bfbdb309184a8e58efe00c`

```dockerfile
```

-	Layers:
	-	`sha256:e06f44f5e5db93fe4fba02df22b44d37f71209d0cfbcbcec67b2ec6687bda27c`  
		Last Modified: Wed, 20 May 2026 19:10:07 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:9b9d19890e9399f86300407959de41b794ee8fd1b46720c7548163f7f94fd15e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6254150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dcae0dec9d781a4ed3bd8282b836bb0fc168482d57def8fec57c690ecdd111a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:09:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:09:00 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:09:00 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:09:00 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:09:00 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:09:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:eeebf06eacfa887b3524b3c76a2593bb68e43a09aa8ff01b5a09c0ce44ed2917`  
		Last Modified: Wed, 20 May 2026 16:04:05 GMT  
		Size: 6.3 MB (6253641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb234fae2f8c35c37c5a0a2b27b551816540b8c513f6b2c479728b77a462cc5`  
		Last Modified: Wed, 20 May 2026 19:09:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:44cc5336af1db8f2f590eca54680623452cbb2da64b65bb690521c087a9be389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2bccd9ad485d0016ce5f53e02daf116336befd19e206a354f9324e36b86c720`

```dockerfile
```

-	Layers:
	-	`sha256:33b891cec5ef0cfb52212abc7e2148afd94f43e4c045f9b8ee11b24532349469`  
		Last Modified: Wed, 20 May 2026 19:09:06 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-scratch` - linux; s390x

```console
$ docker pull nats@sha256:02ac81902397bc3ce3ae4f6bf57bb15925e02525fc49567e8db5747ae9e3cc7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6650240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f5f893e9ed2e5671b5afc696c46fd6aa4099811ef87a81fb46e2bf0c84ba84f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:10:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:10:22 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:10:24 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:10:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:10:24 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:10:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9e00525b36acc41f758b0363af2261253b6d35899fd8e6c7e6b4d30ff05eab43`  
		Last Modified: Wed, 20 May 2026 16:04:08 GMT  
		Size: 6.6 MB (6649731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61970d60cef7c5abc0f2985fb3486911eb5ae086553cd2bfb895dd97daa5dbe1`  
		Last Modified: Wed, 20 May 2026 19:10:43 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:91a6b246de893cdf55e56ebb0f717eb35cb29121fd44454bb5c2e66fe76ba11b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b822bf8bf39b54c102cf252c8b091bac1a2c642851dd34cc7445f10b19fbbe42`

```dockerfile
```

-	Layers:
	-	`sha256:a39452d35088530375cff827daeae3695859d1f87479bba2523d135b3256d905`  
		Last Modified: Wed, 20 May 2026 19:10:43 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.14-windowsservercore`

```console
$ docker pull nats@sha256:1ba584aa4a0b9afe4503a0bb74145174a5a8bd168c74991253e74a0f28cb7a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2.14-windowsservercore` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:7c0d2cfcb1ac8b9c5c8667631fe266d5058f54979c724dbc779cd1303cf56e41
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2130333726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2e9ee9e3b452a65f51ce4b7daa32d3b40f548b8548d8e18d6af0f98c1a6fd8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Wed, 20 May 2026 18:42:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 20 May 2026 18:42:48 GMT
ENV NATS_DOCKERIZED=1
# Wed, 20 May 2026 18:42:49 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:42:51 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:42:53 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.14.1/nats-server-v2.14.1-windows-amd64.zip
# Wed, 20 May 2026 18:42:55 GMT
ENV NATS_SERVER_SHASUM=fb7ddfdde7da0ce89a5174c00b0f7fa9d559ee88c6de638c681b464d35e7caca
# Wed, 20 May 2026 18:44:05 GMT
RUN Set-PSDebug -Trace 2
# Wed, 20 May 2026 18:44:38 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 20 May 2026 18:44:39 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 20 May 2026 18:44:40 GMT
EXPOSE 4222 6222 8222
# Wed, 20 May 2026 18:44:42 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 20 May 2026 18:44:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9541aea3e55bd746462fb4c6e57da81839bbdd92cde8c45bec531dc275c949`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acaeb80d5acbf745ec935e19b9c27aac2c1c36569184a441931640832febb401`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53700d3104e235624a186296ebdbc80307001a56022c9d7a56ca8e8441f1352e`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4698b50a4704844bff262f3486b8d21762a0b2216da94ee49cf3304647a202cf`  
		Last Modified: Wed, 20 May 2026 18:44:50 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39739d4a0333d45798f9c82521d794f7861019e48fcbfc35cec644df0ae2a4bf`  
		Last Modified: Wed, 20 May 2026 18:44:50 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4785912cbc50e52449bd79d36df3b0b1c35e93f26131aeb601005aa38d99d9f2`  
		Last Modified: Wed, 20 May 2026 18:44:50 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406ecfff99aabce085a608a58a3bc33d019a6c6a474f26cd2f037294ab00c29d`  
		Last Modified: Wed, 20 May 2026 18:44:51 GMT  
		Size: 501.6 KB (501598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653bb3e0442eb7d700abb5d1a972abb676d295a6e84793deb25232914a8e833e`  
		Last Modified: Wed, 20 May 2026 18:44:53 GMT  
		Size: 7.4 MB (7397859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662d62953cb63a3accb3782436a9739838d80e2f9610ceac2e47628cc18600fe`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7ba9d33ea88ed49cf0a5cf22fe293c829f1ad64c930e440993b2cb04a3e59a`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fd31c298d20b844c00bdce2ffe2a2370b1d271d45448caa64c2c4c9817afcf`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96cf0d23ad307ba86365cfda67df65a63a9b427078a3ba2715c22735719e8dd0`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.14-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:1ba584aa4a0b9afe4503a0bb74145174a5a8bd168c74991253e74a0f28cb7a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2.14-windowsservercore-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:7c0d2cfcb1ac8b9c5c8667631fe266d5058f54979c724dbc779cd1303cf56e41
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2130333726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2e9ee9e3b452a65f51ce4b7daa32d3b40f548b8548d8e18d6af0f98c1a6fd8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Wed, 20 May 2026 18:42:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 20 May 2026 18:42:48 GMT
ENV NATS_DOCKERIZED=1
# Wed, 20 May 2026 18:42:49 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:42:51 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:42:53 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.14.1/nats-server-v2.14.1-windows-amd64.zip
# Wed, 20 May 2026 18:42:55 GMT
ENV NATS_SERVER_SHASUM=fb7ddfdde7da0ce89a5174c00b0f7fa9d559ee88c6de638c681b464d35e7caca
# Wed, 20 May 2026 18:44:05 GMT
RUN Set-PSDebug -Trace 2
# Wed, 20 May 2026 18:44:38 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 20 May 2026 18:44:39 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 20 May 2026 18:44:40 GMT
EXPOSE 4222 6222 8222
# Wed, 20 May 2026 18:44:42 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 20 May 2026 18:44:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9541aea3e55bd746462fb4c6e57da81839bbdd92cde8c45bec531dc275c949`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acaeb80d5acbf745ec935e19b9c27aac2c1c36569184a441931640832febb401`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53700d3104e235624a186296ebdbc80307001a56022c9d7a56ca8e8441f1352e`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4698b50a4704844bff262f3486b8d21762a0b2216da94ee49cf3304647a202cf`  
		Last Modified: Wed, 20 May 2026 18:44:50 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39739d4a0333d45798f9c82521d794f7861019e48fcbfc35cec644df0ae2a4bf`  
		Last Modified: Wed, 20 May 2026 18:44:50 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4785912cbc50e52449bd79d36df3b0b1c35e93f26131aeb601005aa38d99d9f2`  
		Last Modified: Wed, 20 May 2026 18:44:50 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406ecfff99aabce085a608a58a3bc33d019a6c6a474f26cd2f037294ab00c29d`  
		Last Modified: Wed, 20 May 2026 18:44:51 GMT  
		Size: 501.6 KB (501598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653bb3e0442eb7d700abb5d1a972abb676d295a6e84793deb25232914a8e833e`  
		Last Modified: Wed, 20 May 2026 18:44:53 GMT  
		Size: 7.4 MB (7397859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662d62953cb63a3accb3782436a9739838d80e2f9610ceac2e47628cc18600fe`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7ba9d33ea88ed49cf0a5cf22fe293c829f1ad64c930e440993b2cb04a3e59a`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fd31c298d20b844c00bdce2ffe2a2370b1d271d45448caa64c2c4c9817afcf`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96cf0d23ad307ba86365cfda67df65a63a9b427078a3ba2715c22735719e8dd0`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.14.1`

```console
$ docker pull nats@sha256:7f430e429d0a90444b38bd40ab7812fd3afcc49a51f6b03a931f9becd5aeb280
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
	-	windows version 10.0.20348.5139; amd64

### `nats:2.14.1` - linux; amd64

```console
$ docker pull nats@sha256:aad7f400fa8a1cbcc2f818d5373638f91cfbfcac7cb9bd28fe6e8538c08b9c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6838210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39f65eeb0573eea876a604f186453a7a3cda0c8c511dd143432e1128e07a8734`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:10:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:10:38 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:10:38 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:10:38 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:10:38 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:10:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:05832d0be2949ff52eaf08a260411f3a4a020a066de4aa19dc62284052758304`  
		Last Modified: Wed, 20 May 2026 16:04:06 GMT  
		Size: 6.8 MB (6837703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a284b9b8e39214498d13f3dca35a9c9e81d34b69635ed74a3d47d26e45d5591`  
		Last Modified: Wed, 20 May 2026 19:10:42 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.1` - unknown; unknown

```console
$ docker pull nats@sha256:6b2a0558891216e6e12622ac66d8766987858f507eee4cb4cfef25a0b1480e84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a061861dcdd34e8079637906d854df58e3e30fcfb0514aa93b4a1ada5b3936b9`

```dockerfile
```

-	Layers:
	-	`sha256:7fff463e51e2de542cc152e5196125c500561d37a866a78ab756f40188e25be6`  
		Last Modified: Wed, 20 May 2026 19:10:42 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.1` - linux; arm variant v6

```console
$ docker pull nats@sha256:80f40fb067456022353b1754a4c58f49b1af454522a8af74e9c270e3a27668d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6573757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:039a8f82177ac58ba3952b7b25d8af7b14d0fbcf08e6e53efbab9e028b515cb5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:09:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:09:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:09:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:09:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:09:27 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:09:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3f675bd99a02bdb97f8ad1545908545b1e797e40d8038ce181205b0808044e20`  
		Last Modified: Wed, 20 May 2026 16:04:08 GMT  
		Size: 6.6 MB (6573248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715581626472620cc372593ae38a74d6c85239c0282bc3c5b7937fcd525bb308`  
		Last Modified: Wed, 20 May 2026 19:09:32 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.1` - unknown; unknown

```console
$ docker pull nats@sha256:cd80c2a5593667a467031df5e49c9cab2cc1f5ae03e981c4789d7a262cbded23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac98f8edc0ec201da45e4d96bc1ea96d553e89648a61e35f8a195d38ce81d6b9`

```dockerfile
```

-	Layers:
	-	`sha256:d7cd588a4563631d4b86b381c7ee1c56114f94b80568f0e8defc278961b4c119`  
		Last Modified: Wed, 20 May 2026 19:09:31 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.1` - linux; arm variant v7

```console
$ docker pull nats@sha256:ae43b4e3d705ed3a3386e6b303d8dfb011fec9e1cdf8523ff9c6387935d9652d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6565185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a493ff1dda3a5eb2f84019be4a31029f9463e5a91f142d91cbd96345245eadb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:09:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:09:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:09:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:09:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:09:01 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:09:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:07a4ad6a636748b056dca5d82613a936ff1872d9092911832cea1178d840cb7f`  
		Last Modified: Wed, 20 May 2026 16:04:08 GMT  
		Size: 6.6 MB (6564678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95ec1a5b2af5f3d81a39b2563595f7008790713449f52e148c254bc7d0be80e`  
		Last Modified: Wed, 20 May 2026 19:09:06 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.1` - unknown; unknown

```console
$ docker pull nats@sha256:5b515d7d9aa87098056bad17534ca266bba383a9a52d362a1788c5ac7b596d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a1b7811acc104229e8cc148ff624e24efc4e31d06fce27cdd9091dd3237110`

```dockerfile
```

-	Layers:
	-	`sha256:e855458d7f5e87be1456ba294fc7386adaa0241520ff73ab4b95b94271f3d0a0`  
		Last Modified: Wed, 20 May 2026 19:09:05 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.1` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:89ea5f3d1a4e7db9650685b4b60d5f2340f6edd89f0d2a7a6f2a5cb9b6f144c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6189602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:080d11e023e3c9bc77bc5d6e137c30fcee2ca537fbda1d730ee0de9b5131cf97`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:10:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:10:02 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:10:02 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:10:02 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:10:02 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:10:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5f2fe2216ecafda68f73a81334875cb85722e57f12bc2af372cc03c4952017ff`  
		Last Modified: Wed, 20 May 2026 16:04:06 GMT  
		Size: 6.2 MB (6189094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f13aa02931bd62f5d9ce1935b8f163c6fcb3db670a4893037e6326c70ff971`  
		Last Modified: Wed, 20 May 2026 19:10:07 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.1` - unknown; unknown

```console
$ docker pull nats@sha256:55f5544491f15bb813013ec1a1698f6e7e6f1ebbf96b4e49dba94dab9c27b313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30316b20c5d7aabdc5ded4b132f0725f10bdb7bd31bfbdb309184a8e58efe00c`

```dockerfile
```

-	Layers:
	-	`sha256:e06f44f5e5db93fe4fba02df22b44d37f71209d0cfbcbcec67b2ec6687bda27c`  
		Last Modified: Wed, 20 May 2026 19:10:07 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.1` - linux; ppc64le

```console
$ docker pull nats@sha256:9b9d19890e9399f86300407959de41b794ee8fd1b46720c7548163f7f94fd15e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6254150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dcae0dec9d781a4ed3bd8282b836bb0fc168482d57def8fec57c690ecdd111a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:09:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:09:00 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:09:00 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:09:00 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:09:00 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:09:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:eeebf06eacfa887b3524b3c76a2593bb68e43a09aa8ff01b5a09c0ce44ed2917`  
		Last Modified: Wed, 20 May 2026 16:04:05 GMT  
		Size: 6.3 MB (6253641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb234fae2f8c35c37c5a0a2b27b551816540b8c513f6b2c479728b77a462cc5`  
		Last Modified: Wed, 20 May 2026 19:09:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.1` - unknown; unknown

```console
$ docker pull nats@sha256:44cc5336af1db8f2f590eca54680623452cbb2da64b65bb690521c087a9be389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2bccd9ad485d0016ce5f53e02daf116336befd19e206a354f9324e36b86c720`

```dockerfile
```

-	Layers:
	-	`sha256:33b891cec5ef0cfb52212abc7e2148afd94f43e4c045f9b8ee11b24532349469`  
		Last Modified: Wed, 20 May 2026 19:09:06 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.1` - linux; s390x

```console
$ docker pull nats@sha256:02ac81902397bc3ce3ae4f6bf57bb15925e02525fc49567e8db5747ae9e3cc7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6650240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f5f893e9ed2e5671b5afc696c46fd6aa4099811ef87a81fb46e2bf0c84ba84f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:10:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:10:22 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:10:24 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:10:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:10:24 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:10:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9e00525b36acc41f758b0363af2261253b6d35899fd8e6c7e6b4d30ff05eab43`  
		Last Modified: Wed, 20 May 2026 16:04:08 GMT  
		Size: 6.6 MB (6649731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61970d60cef7c5abc0f2985fb3486911eb5ae086553cd2bfb895dd97daa5dbe1`  
		Last Modified: Wed, 20 May 2026 19:10:43 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.1` - unknown; unknown

```console
$ docker pull nats@sha256:91a6b246de893cdf55e56ebb0f717eb35cb29121fd44454bb5c2e66fe76ba11b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b822bf8bf39b54c102cf252c8b091bac1a2c642851dd34cc7445f10b19fbbe42`

```dockerfile
```

-	Layers:
	-	`sha256:a39452d35088530375cff827daeae3695859d1f87479bba2523d135b3256d905`  
		Last Modified: Wed, 20 May 2026 19:10:43 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.1` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:ad04df86864a0653927e5ff2293212d694588db88edc746ce8b917417317c0f3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134078105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc7e5bd03f66dabebd5917cf13f4067081477a5934e86d07357d04db10e33ec4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 20 May 2026 19:09:14 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 20 May 2026 19:09:15 GMT
RUN cmd /S /C #(nop) COPY file:5d608f6a5cbf80544d196a9ac38d66b2635084a5e0a392611785993205e5329d in C:\nats-server.exe 
# Wed, 20 May 2026 19:09:16 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 20 May 2026 19:09:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 20 May 2026 19:09:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 20 May 2026 19:09:18 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c815e3255991cc2df065c98a27664be46d8b5db04231449f637ecaf64c5c098f`  
		Last Modified: Wed, 20 May 2026 19:09:24 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68983020294e3083531b7192194e9d5172d2a1449eac04682b7544bb139048b5`  
		Last Modified: Wed, 20 May 2026 19:09:27 GMT  
		Size: 7.0 MB (7033380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730756958a80b0245caf373feb8024993ecef9e67a8ade759511f66d001f3f07`  
		Last Modified: Wed, 20 May 2026 19:09:22 GMT  
		Size: 1.7 KB (1672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ec9d4f153ff90a362ff5591192559ff2e3584441d0bee4e4fdd8b0a4845b833`  
		Last Modified: Wed, 20 May 2026 19:09:22 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb6e35267fc994af8eab6412783ba571dd4c1d14e5fa8771f50a386e61ef655`  
		Last Modified: Wed, 20 May 2026 19:09:22 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838e55b2d659c4cc5f4e0db1773fbe38aa8487984688f5a0f60b202907588e42`  
		Last Modified: Wed, 20 May 2026 19:09:22 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.14.1-alpine`

```console
$ docker pull nats@sha256:ea17b9b7f74279b9239cf65e5786c0133e9a7c353bf218d29004abf2e7a33181
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

### `nats:2.14.1-alpine` - linux; amd64

```console
$ docker pull nats@sha256:4c516667ffae4977a0b4ee1d8caa5b663a0d147b66c6b2adc8ee8f3e23728bc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11103220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c133130b2f2f46568f11546ffef920fccb739e99fd733ef11ea43fc1737887c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:37:17 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:37:17 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:37:17 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:37:17 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:37:17 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:37:17 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:37:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:37:17 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6887181943c337b002058eb52d1b08afbc55add7c29a34ac80e3949090e15495`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 7.3 MB (7294060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a070bfd7422a373dc1b206300e1798aef404bf1bac5a04a3293b33f5468a167e`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4a08ddee9fc679f6a40d1ca0c325ec632bebcbb19437245764df5d7ccb6e0d`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.1-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:16deabb6f9a013834b95f04987ebab3d889f6704db15b71e13e10a4109b2e5b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d0fdb19df33d866a3c0b19c2d8aa933518ea4afc5b2f7562f2fd9364bb805ec`

```dockerfile
```

-	Layers:
	-	`sha256:650380b0910269f4395d628fbfafe98d4c910cc7a775ff48fa5093aaddc18b1f`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 15.4 KB (15403 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.1-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:32e7eb3bde61b1a81ba030cf21530f82b3713f20585f14da348ed9ff0099cd38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10540472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff1b400cc41fb9599883d47ee0cc98f26d14432cafaa79d7b00c36500c3be581`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:35:40 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:35:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:35:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:35:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac441e30d31da40cce92ca13be29a2ec33b8e530c12f39c4e6e6f821d36fa5f7`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 7.0 MB (7032117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588069c44453627769cbea386971dc510fa0a2a33fc33bc21795cbe4c6ceeb2e`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1efc9734efaa0feb255b7c30b046fb56094635c7d947db2f21f7a873a06b52a`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.1-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:e8fdb1f5ad9c517ef1795cc413d10f4304bac0bfacca20197b1324ceed658bd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67da2ba5e6d5168c0687521d71e8357c05504026864365687620573485a04e0`

```dockerfile
```

-	Layers:
	-	`sha256:63de3f19bc13cbd3dc2f28506681e74ef898d6cddd4ed65551521f9d641ff6b5`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.1-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:8805cf2aaa214d58393f7373011c4fe330f5225fb9bc4da6d715a6ab72ff8dc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10246493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32278cb7a1bf5e3ea24f7381d52c844e152750efbf7684af40245538a2fadaa4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:35:40 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:35:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:35:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:35:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3e43a7f3a2149acbd98329815e7e03d9dcf933d2131db6f8e1eecd1c01e173`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 7.0 MB (7019690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588069c44453627769cbea386971dc510fa0a2a33fc33bc21795cbe4c6ceeb2e`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9213cf8ea08c3ce1080672b9ea4c12034482854a1829a814ec22933ea91379a0`  
		Last Modified: Wed, 20 May 2026 18:35:44 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.1-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:83439ca6685120afbf799cb62bebb64b76d3419bd2523ae781dfad0b8bd8db9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f56fa87064674ea90080bd544ca88fd1b1f257088b93998a8cd46405b6249c`

```dockerfile
```

-	Layers:
	-	`sha256:22deddd2f98e84c9bc37c96058b3e88416465a5ea1004b4985cef2385de5a8be`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 15.5 KB (15515 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.1-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:abc668a25359714d7320be16684a7a6096d82a6d41aa9fbb4275c02f3fb1e716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10791094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c04c7a60cc127abb4b03f7f7593fb48cd0124f4f2cd959996fdcb5caba71e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:37:01 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:37:01 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:37:01 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:37:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:37:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:37:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:37:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:37:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b89c7be0c2d2557967711fd66cb73b3b64361381d066e02f0b52b2abeedd6b9`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 6.6 MB (6648233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b1bf5ee681da0d7929bf7d0e36bf5d24df48f214a25c32a7692f9fd0bc5eab`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2e67e1deca529e76612c525c5a8e12050d9ec84c3691673953e51573c1e653`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.1-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:5ae7b0317944de344d87247e9cb05a11dcd4f796e1800294193d7b60f43c9d9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9059f595926bbcc76e88f995c69a532e5bfdb37e53db7d9cbd26077b9a0f52d1`

```dockerfile
```

-	Layers:
	-	`sha256:a10a07e60572ceb3113b276c9a02c5aa46bf940b8f2a491e7064608fcac2409c`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.1-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:7c13d10c1f7169aaedc2ac8ecbc1f431dda7e906455b836d09a14b3b948f3036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10448793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa266dd5df001f7f566ffb0c8c8acff2de160efa06508788758a4e3022c8e98d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:39:54 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:39:54 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:39:54 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:39:55 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:39:55 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:39:55 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:39:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:39:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efe06b0c545d8e510a8131fe2984aa46a7c4d7502148ce8f2e94df5ffeed78f`  
		Last Modified: Wed, 20 May 2026 18:40:02 GMT  
		Size: 6.7 MB (6711165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3c6e5710602d0c65abfcc3a4aac8676e3cd1f849d5967bee0654b0ec045abe`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0fcc4ed5f0f4848feb91f0e5c409cb87bfd693a7056f2c0e574dbf0fc8ff4ab`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.1-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:7878f9d371c5d9227beef40f16b5dfd6d37465bab0104f835171af841d4c4a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47a1ee27b4ce5d60016cbff052995f2dbab1c7c6c61dcf79e2f75cbb1430fbad`

```dockerfile
```

-	Layers:
	-	`sha256:c27fc7351e2a880436edb13f3b1eaf0c5d83b4ec4a761386db3f8a0e0e8642a5`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.1-alpine` - linux; s390x

```console
$ docker pull nats@sha256:458d20eff2bdbc011304724399fc06b3db7dae7c95d0c806969fc503389a70c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10757148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0002a7df6776ecf8e0df1b73510a6014c1f519a3c9692cd787d8568dd8021d99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:48:37 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:48:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:48:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:48:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:48:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:48:43 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:48:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:48:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728aea4976117b7918cb9446c013c273cae16aa21337089d91cbd93761d10ae5`  
		Last Modified: Wed, 20 May 2026 18:49:10 GMT  
		Size: 7.1 MB (7102303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e102ba28952cc8bf83cffaefb3ec4b38d56cd736120ece8c71362ff603fd09b`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec22f8c91bd1e1b2e7f49773754ab16299137dd3226c8bb660a538d249364ae6`  
		Last Modified: Wed, 20 May 2026 18:49:08 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.1-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:38a69833b514d10d0b925fa5c4639cb5d17abe985f2b30699a0f305324397aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cffc57189208991582e7a0262e60b1415e19ac3919981144973c3d19428e23f6`

```dockerfile
```

-	Layers:
	-	`sha256:ccc40928ae38a1bd914e972d9acbe81dbc2e36b6132cee1761b8e20e7dda2db5`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.14.1-alpine3.22`

```console
$ docker pull nats@sha256:ea17b9b7f74279b9239cf65e5786c0133e9a7c353bf218d29004abf2e7a33181
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

### `nats:2.14.1-alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:4c516667ffae4977a0b4ee1d8caa5b663a0d147b66c6b2adc8ee8f3e23728bc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11103220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c133130b2f2f46568f11546ffef920fccb739e99fd733ef11ea43fc1737887c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:37:17 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:37:17 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:37:17 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:37:17 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:37:17 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:37:17 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:37:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:37:17 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6887181943c337b002058eb52d1b08afbc55add7c29a34ac80e3949090e15495`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 7.3 MB (7294060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a070bfd7422a373dc1b206300e1798aef404bf1bac5a04a3293b33f5468a167e`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4a08ddee9fc679f6a40d1ca0c325ec632bebcbb19437245764df5d7ccb6e0d`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.1-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:16deabb6f9a013834b95f04987ebab3d889f6704db15b71e13e10a4109b2e5b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d0fdb19df33d866a3c0b19c2d8aa933518ea4afc5b2f7562f2fd9364bb805ec`

```dockerfile
```

-	Layers:
	-	`sha256:650380b0910269f4395d628fbfafe98d4c910cc7a775ff48fa5093aaddc18b1f`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 15.4 KB (15403 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.1-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:32e7eb3bde61b1a81ba030cf21530f82b3713f20585f14da348ed9ff0099cd38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10540472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff1b400cc41fb9599883d47ee0cc98f26d14432cafaa79d7b00c36500c3be581`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:35:40 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:35:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:35:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:35:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac441e30d31da40cce92ca13be29a2ec33b8e530c12f39c4e6e6f821d36fa5f7`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 7.0 MB (7032117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588069c44453627769cbea386971dc510fa0a2a33fc33bc21795cbe4c6ceeb2e`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1efc9734efaa0feb255b7c30b046fb56094635c7d947db2f21f7a873a06b52a`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.1-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:e8fdb1f5ad9c517ef1795cc413d10f4304bac0bfacca20197b1324ceed658bd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67da2ba5e6d5168c0687521d71e8357c05504026864365687620573485a04e0`

```dockerfile
```

-	Layers:
	-	`sha256:63de3f19bc13cbd3dc2f28506681e74ef898d6cddd4ed65551521f9d641ff6b5`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.1-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:8805cf2aaa214d58393f7373011c4fe330f5225fb9bc4da6d715a6ab72ff8dc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10246493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32278cb7a1bf5e3ea24f7381d52c844e152750efbf7684af40245538a2fadaa4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:35:40 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:35:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:35:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:35:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3e43a7f3a2149acbd98329815e7e03d9dcf933d2131db6f8e1eecd1c01e173`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 7.0 MB (7019690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588069c44453627769cbea386971dc510fa0a2a33fc33bc21795cbe4c6ceeb2e`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9213cf8ea08c3ce1080672b9ea4c12034482854a1829a814ec22933ea91379a0`  
		Last Modified: Wed, 20 May 2026 18:35:44 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.1-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:83439ca6685120afbf799cb62bebb64b76d3419bd2523ae781dfad0b8bd8db9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f56fa87064674ea90080bd544ca88fd1b1f257088b93998a8cd46405b6249c`

```dockerfile
```

-	Layers:
	-	`sha256:22deddd2f98e84c9bc37c96058b3e88416465a5ea1004b4985cef2385de5a8be`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 15.5 KB (15515 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.1-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:abc668a25359714d7320be16684a7a6096d82a6d41aa9fbb4275c02f3fb1e716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10791094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c04c7a60cc127abb4b03f7f7593fb48cd0124f4f2cd959996fdcb5caba71e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:37:01 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:37:01 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:37:01 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:37:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:37:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:37:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:37:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:37:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b89c7be0c2d2557967711fd66cb73b3b64361381d066e02f0b52b2abeedd6b9`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 6.6 MB (6648233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b1bf5ee681da0d7929bf7d0e36bf5d24df48f214a25c32a7692f9fd0bc5eab`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2e67e1deca529e76612c525c5a8e12050d9ec84c3691673953e51573c1e653`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.1-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:5ae7b0317944de344d87247e9cb05a11dcd4f796e1800294193d7b60f43c9d9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9059f595926bbcc76e88f995c69a532e5bfdb37e53db7d9cbd26077b9a0f52d1`

```dockerfile
```

-	Layers:
	-	`sha256:a10a07e60572ceb3113b276c9a02c5aa46bf940b8f2a491e7064608fcac2409c`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.1-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:7c13d10c1f7169aaedc2ac8ecbc1f431dda7e906455b836d09a14b3b948f3036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10448793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa266dd5df001f7f566ffb0c8c8acff2de160efa06508788758a4e3022c8e98d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:39:54 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:39:54 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:39:54 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:39:55 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:39:55 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:39:55 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:39:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:39:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efe06b0c545d8e510a8131fe2984aa46a7c4d7502148ce8f2e94df5ffeed78f`  
		Last Modified: Wed, 20 May 2026 18:40:02 GMT  
		Size: 6.7 MB (6711165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3c6e5710602d0c65abfcc3a4aac8676e3cd1f849d5967bee0654b0ec045abe`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0fcc4ed5f0f4848feb91f0e5c409cb87bfd693a7056f2c0e574dbf0fc8ff4ab`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.1-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:7878f9d371c5d9227beef40f16b5dfd6d37465bab0104f835171af841d4c4a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47a1ee27b4ce5d60016cbff052995f2dbab1c7c6c61dcf79e2f75cbb1430fbad`

```dockerfile
```

-	Layers:
	-	`sha256:c27fc7351e2a880436edb13f3b1eaf0c5d83b4ec4a761386db3f8a0e0e8642a5`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.1-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:458d20eff2bdbc011304724399fc06b3db7dae7c95d0c806969fc503389a70c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10757148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0002a7df6776ecf8e0df1b73510a6014c1f519a3c9692cd787d8568dd8021d99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:48:37 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:48:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:48:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:48:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:48:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:48:43 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:48:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:48:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728aea4976117b7918cb9446c013c273cae16aa21337089d91cbd93761d10ae5`  
		Last Modified: Wed, 20 May 2026 18:49:10 GMT  
		Size: 7.1 MB (7102303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e102ba28952cc8bf83cffaefb3ec4b38d56cd736120ece8c71362ff603fd09b`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec22f8c91bd1e1b2e7f49773754ab16299137dd3226c8bb660a538d249364ae6`  
		Last Modified: Wed, 20 May 2026 18:49:08 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.1-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:38a69833b514d10d0b925fa5c4639cb5d17abe985f2b30699a0f305324397aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cffc57189208991582e7a0262e60b1415e19ac3919981144973c3d19428e23f6`

```dockerfile
```

-	Layers:
	-	`sha256:ccc40928ae38a1bd914e972d9acbe81dbc2e36b6132cee1761b8e20e7dda2db5`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.14.1-linux`

```console
$ docker pull nats@sha256:4223c8fa116891628611e154fb66570cad599d8f8b3b131b82caf10f378e9dcf
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

### `nats:2.14.1-linux` - linux; amd64

```console
$ docker pull nats@sha256:aad7f400fa8a1cbcc2f818d5373638f91cfbfcac7cb9bd28fe6e8538c08b9c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6838210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39f65eeb0573eea876a604f186453a7a3cda0c8c511dd143432e1128e07a8734`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:10:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:10:38 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:10:38 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:10:38 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:10:38 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:10:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:05832d0be2949ff52eaf08a260411f3a4a020a066de4aa19dc62284052758304`  
		Last Modified: Wed, 20 May 2026 16:04:06 GMT  
		Size: 6.8 MB (6837703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a284b9b8e39214498d13f3dca35a9c9e81d34b69635ed74a3d47d26e45d5591`  
		Last Modified: Wed, 20 May 2026 19:10:42 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.1-linux` - unknown; unknown

```console
$ docker pull nats@sha256:6b2a0558891216e6e12622ac66d8766987858f507eee4cb4cfef25a0b1480e84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a061861dcdd34e8079637906d854df58e3e30fcfb0514aa93b4a1ada5b3936b9`

```dockerfile
```

-	Layers:
	-	`sha256:7fff463e51e2de542cc152e5196125c500561d37a866a78ab756f40188e25be6`  
		Last Modified: Wed, 20 May 2026 19:10:42 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.1-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:80f40fb067456022353b1754a4c58f49b1af454522a8af74e9c270e3a27668d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6573757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:039a8f82177ac58ba3952b7b25d8af7b14d0fbcf08e6e53efbab9e028b515cb5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:09:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:09:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:09:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:09:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:09:27 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:09:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3f675bd99a02bdb97f8ad1545908545b1e797e40d8038ce181205b0808044e20`  
		Last Modified: Wed, 20 May 2026 16:04:08 GMT  
		Size: 6.6 MB (6573248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715581626472620cc372593ae38a74d6c85239c0282bc3c5b7937fcd525bb308`  
		Last Modified: Wed, 20 May 2026 19:09:32 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.1-linux` - unknown; unknown

```console
$ docker pull nats@sha256:cd80c2a5593667a467031df5e49c9cab2cc1f5ae03e981c4789d7a262cbded23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac98f8edc0ec201da45e4d96bc1ea96d553e89648a61e35f8a195d38ce81d6b9`

```dockerfile
```

-	Layers:
	-	`sha256:d7cd588a4563631d4b86b381c7ee1c56114f94b80568f0e8defc278961b4c119`  
		Last Modified: Wed, 20 May 2026 19:09:31 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.1-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:ae43b4e3d705ed3a3386e6b303d8dfb011fec9e1cdf8523ff9c6387935d9652d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6565185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a493ff1dda3a5eb2f84019be4a31029f9463e5a91f142d91cbd96345245eadb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:09:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:09:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:09:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:09:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:09:01 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:09:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:07a4ad6a636748b056dca5d82613a936ff1872d9092911832cea1178d840cb7f`  
		Last Modified: Wed, 20 May 2026 16:04:08 GMT  
		Size: 6.6 MB (6564678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95ec1a5b2af5f3d81a39b2563595f7008790713449f52e148c254bc7d0be80e`  
		Last Modified: Wed, 20 May 2026 19:09:06 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.1-linux` - unknown; unknown

```console
$ docker pull nats@sha256:5b515d7d9aa87098056bad17534ca266bba383a9a52d362a1788c5ac7b596d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a1b7811acc104229e8cc148ff624e24efc4e31d06fce27cdd9091dd3237110`

```dockerfile
```

-	Layers:
	-	`sha256:e855458d7f5e87be1456ba294fc7386adaa0241520ff73ab4b95b94271f3d0a0`  
		Last Modified: Wed, 20 May 2026 19:09:05 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.1-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:89ea5f3d1a4e7db9650685b4b60d5f2340f6edd89f0d2a7a6f2a5cb9b6f144c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6189602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:080d11e023e3c9bc77bc5d6e137c30fcee2ca537fbda1d730ee0de9b5131cf97`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:10:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:10:02 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:10:02 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:10:02 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:10:02 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:10:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5f2fe2216ecafda68f73a81334875cb85722e57f12bc2af372cc03c4952017ff`  
		Last Modified: Wed, 20 May 2026 16:04:06 GMT  
		Size: 6.2 MB (6189094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f13aa02931bd62f5d9ce1935b8f163c6fcb3db670a4893037e6326c70ff971`  
		Last Modified: Wed, 20 May 2026 19:10:07 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.1-linux` - unknown; unknown

```console
$ docker pull nats@sha256:55f5544491f15bb813013ec1a1698f6e7e6f1ebbf96b4e49dba94dab9c27b313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30316b20c5d7aabdc5ded4b132f0725f10bdb7bd31bfbdb309184a8e58efe00c`

```dockerfile
```

-	Layers:
	-	`sha256:e06f44f5e5db93fe4fba02df22b44d37f71209d0cfbcbcec67b2ec6687bda27c`  
		Last Modified: Wed, 20 May 2026 19:10:07 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.1-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:9b9d19890e9399f86300407959de41b794ee8fd1b46720c7548163f7f94fd15e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6254150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dcae0dec9d781a4ed3bd8282b836bb0fc168482d57def8fec57c690ecdd111a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:09:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:09:00 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:09:00 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:09:00 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:09:00 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:09:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:eeebf06eacfa887b3524b3c76a2593bb68e43a09aa8ff01b5a09c0ce44ed2917`  
		Last Modified: Wed, 20 May 2026 16:04:05 GMT  
		Size: 6.3 MB (6253641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb234fae2f8c35c37c5a0a2b27b551816540b8c513f6b2c479728b77a462cc5`  
		Last Modified: Wed, 20 May 2026 19:09:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.1-linux` - unknown; unknown

```console
$ docker pull nats@sha256:44cc5336af1db8f2f590eca54680623452cbb2da64b65bb690521c087a9be389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2bccd9ad485d0016ce5f53e02daf116336befd19e206a354f9324e36b86c720`

```dockerfile
```

-	Layers:
	-	`sha256:33b891cec5ef0cfb52212abc7e2148afd94f43e4c045f9b8ee11b24532349469`  
		Last Modified: Wed, 20 May 2026 19:09:06 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.1-linux` - linux; s390x

```console
$ docker pull nats@sha256:02ac81902397bc3ce3ae4f6bf57bb15925e02525fc49567e8db5747ae9e3cc7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6650240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f5f893e9ed2e5671b5afc696c46fd6aa4099811ef87a81fb46e2bf0c84ba84f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:10:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:10:22 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:10:24 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:10:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:10:24 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:10:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9e00525b36acc41f758b0363af2261253b6d35899fd8e6c7e6b4d30ff05eab43`  
		Last Modified: Wed, 20 May 2026 16:04:08 GMT  
		Size: 6.6 MB (6649731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61970d60cef7c5abc0f2985fb3486911eb5ae086553cd2bfb895dd97daa5dbe1`  
		Last Modified: Wed, 20 May 2026 19:10:43 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.1-linux` - unknown; unknown

```console
$ docker pull nats@sha256:91a6b246de893cdf55e56ebb0f717eb35cb29121fd44454bb5c2e66fe76ba11b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b822bf8bf39b54c102cf252c8b091bac1a2c642851dd34cc7445f10b19fbbe42`

```dockerfile
```

-	Layers:
	-	`sha256:a39452d35088530375cff827daeae3695859d1f87479bba2523d135b3256d905`  
		Last Modified: Wed, 20 May 2026 19:10:43 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.14.1-nanoserver`

```console
$ docker pull nats@sha256:b8d325261e82cfa9b4561b3752e5791fc51c257bde48ca6e1ae65580749766a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2.14.1-nanoserver` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:ad04df86864a0653927e5ff2293212d694588db88edc746ce8b917417317c0f3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134078105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc7e5bd03f66dabebd5917cf13f4067081477a5934e86d07357d04db10e33ec4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 20 May 2026 19:09:14 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 20 May 2026 19:09:15 GMT
RUN cmd /S /C #(nop) COPY file:5d608f6a5cbf80544d196a9ac38d66b2635084a5e0a392611785993205e5329d in C:\nats-server.exe 
# Wed, 20 May 2026 19:09:16 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 20 May 2026 19:09:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 20 May 2026 19:09:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 20 May 2026 19:09:18 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c815e3255991cc2df065c98a27664be46d8b5db04231449f637ecaf64c5c098f`  
		Last Modified: Wed, 20 May 2026 19:09:24 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68983020294e3083531b7192194e9d5172d2a1449eac04682b7544bb139048b5`  
		Last Modified: Wed, 20 May 2026 19:09:27 GMT  
		Size: 7.0 MB (7033380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730756958a80b0245caf373feb8024993ecef9e67a8ade759511f66d001f3f07`  
		Last Modified: Wed, 20 May 2026 19:09:22 GMT  
		Size: 1.7 KB (1672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ec9d4f153ff90a362ff5591192559ff2e3584441d0bee4e4fdd8b0a4845b833`  
		Last Modified: Wed, 20 May 2026 19:09:22 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb6e35267fc994af8eab6412783ba571dd4c1d14e5fa8771f50a386e61ef655`  
		Last Modified: Wed, 20 May 2026 19:09:22 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838e55b2d659c4cc5f4e0db1773fbe38aa8487984688f5a0f60b202907588e42`  
		Last Modified: Wed, 20 May 2026 19:09:22 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.14.1-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:b8d325261e82cfa9b4561b3752e5791fc51c257bde48ca6e1ae65580749766a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2.14.1-nanoserver-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:ad04df86864a0653927e5ff2293212d694588db88edc746ce8b917417317c0f3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134078105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc7e5bd03f66dabebd5917cf13f4067081477a5934e86d07357d04db10e33ec4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 20 May 2026 19:09:14 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 20 May 2026 19:09:15 GMT
RUN cmd /S /C #(nop) COPY file:5d608f6a5cbf80544d196a9ac38d66b2635084a5e0a392611785993205e5329d in C:\nats-server.exe 
# Wed, 20 May 2026 19:09:16 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 20 May 2026 19:09:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 20 May 2026 19:09:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 20 May 2026 19:09:18 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c815e3255991cc2df065c98a27664be46d8b5db04231449f637ecaf64c5c098f`  
		Last Modified: Wed, 20 May 2026 19:09:24 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68983020294e3083531b7192194e9d5172d2a1449eac04682b7544bb139048b5`  
		Last Modified: Wed, 20 May 2026 19:09:27 GMT  
		Size: 7.0 MB (7033380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730756958a80b0245caf373feb8024993ecef9e67a8ade759511f66d001f3f07`  
		Last Modified: Wed, 20 May 2026 19:09:22 GMT  
		Size: 1.7 KB (1672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ec9d4f153ff90a362ff5591192559ff2e3584441d0bee4e4fdd8b0a4845b833`  
		Last Modified: Wed, 20 May 2026 19:09:22 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb6e35267fc994af8eab6412783ba571dd4c1d14e5fa8771f50a386e61ef655`  
		Last Modified: Wed, 20 May 2026 19:09:22 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838e55b2d659c4cc5f4e0db1773fbe38aa8487984688f5a0f60b202907588e42`  
		Last Modified: Wed, 20 May 2026 19:09:22 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.14.1-scratch`

```console
$ docker pull nats@sha256:4223c8fa116891628611e154fb66570cad599d8f8b3b131b82caf10f378e9dcf
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

### `nats:2.14.1-scratch` - linux; amd64

```console
$ docker pull nats@sha256:aad7f400fa8a1cbcc2f818d5373638f91cfbfcac7cb9bd28fe6e8538c08b9c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6838210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39f65eeb0573eea876a604f186453a7a3cda0c8c511dd143432e1128e07a8734`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:10:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:10:38 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:10:38 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:10:38 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:10:38 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:10:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:05832d0be2949ff52eaf08a260411f3a4a020a066de4aa19dc62284052758304`  
		Last Modified: Wed, 20 May 2026 16:04:06 GMT  
		Size: 6.8 MB (6837703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a284b9b8e39214498d13f3dca35a9c9e81d34b69635ed74a3d47d26e45d5591`  
		Last Modified: Wed, 20 May 2026 19:10:42 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.1-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:6b2a0558891216e6e12622ac66d8766987858f507eee4cb4cfef25a0b1480e84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a061861dcdd34e8079637906d854df58e3e30fcfb0514aa93b4a1ada5b3936b9`

```dockerfile
```

-	Layers:
	-	`sha256:7fff463e51e2de542cc152e5196125c500561d37a866a78ab756f40188e25be6`  
		Last Modified: Wed, 20 May 2026 19:10:42 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.1-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:80f40fb067456022353b1754a4c58f49b1af454522a8af74e9c270e3a27668d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6573757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:039a8f82177ac58ba3952b7b25d8af7b14d0fbcf08e6e53efbab9e028b515cb5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:09:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:09:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:09:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:09:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:09:27 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:09:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3f675bd99a02bdb97f8ad1545908545b1e797e40d8038ce181205b0808044e20`  
		Last Modified: Wed, 20 May 2026 16:04:08 GMT  
		Size: 6.6 MB (6573248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715581626472620cc372593ae38a74d6c85239c0282bc3c5b7937fcd525bb308`  
		Last Modified: Wed, 20 May 2026 19:09:32 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.1-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:cd80c2a5593667a467031df5e49c9cab2cc1f5ae03e981c4789d7a262cbded23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac98f8edc0ec201da45e4d96bc1ea96d553e89648a61e35f8a195d38ce81d6b9`

```dockerfile
```

-	Layers:
	-	`sha256:d7cd588a4563631d4b86b381c7ee1c56114f94b80568f0e8defc278961b4c119`  
		Last Modified: Wed, 20 May 2026 19:09:31 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.1-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:ae43b4e3d705ed3a3386e6b303d8dfb011fec9e1cdf8523ff9c6387935d9652d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6565185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a493ff1dda3a5eb2f84019be4a31029f9463e5a91f142d91cbd96345245eadb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:09:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:09:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:09:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:09:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:09:01 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:09:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:07a4ad6a636748b056dca5d82613a936ff1872d9092911832cea1178d840cb7f`  
		Last Modified: Wed, 20 May 2026 16:04:08 GMT  
		Size: 6.6 MB (6564678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95ec1a5b2af5f3d81a39b2563595f7008790713449f52e148c254bc7d0be80e`  
		Last Modified: Wed, 20 May 2026 19:09:06 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.1-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:5b515d7d9aa87098056bad17534ca266bba383a9a52d362a1788c5ac7b596d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a1b7811acc104229e8cc148ff624e24efc4e31d06fce27cdd9091dd3237110`

```dockerfile
```

-	Layers:
	-	`sha256:e855458d7f5e87be1456ba294fc7386adaa0241520ff73ab4b95b94271f3d0a0`  
		Last Modified: Wed, 20 May 2026 19:09:05 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.1-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:89ea5f3d1a4e7db9650685b4b60d5f2340f6edd89f0d2a7a6f2a5cb9b6f144c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6189602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:080d11e023e3c9bc77bc5d6e137c30fcee2ca537fbda1d730ee0de9b5131cf97`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:10:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:10:02 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:10:02 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:10:02 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:10:02 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:10:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5f2fe2216ecafda68f73a81334875cb85722e57f12bc2af372cc03c4952017ff`  
		Last Modified: Wed, 20 May 2026 16:04:06 GMT  
		Size: 6.2 MB (6189094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f13aa02931bd62f5d9ce1935b8f163c6fcb3db670a4893037e6326c70ff971`  
		Last Modified: Wed, 20 May 2026 19:10:07 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.1-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:55f5544491f15bb813013ec1a1698f6e7e6f1ebbf96b4e49dba94dab9c27b313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30316b20c5d7aabdc5ded4b132f0725f10bdb7bd31bfbdb309184a8e58efe00c`

```dockerfile
```

-	Layers:
	-	`sha256:e06f44f5e5db93fe4fba02df22b44d37f71209d0cfbcbcec67b2ec6687bda27c`  
		Last Modified: Wed, 20 May 2026 19:10:07 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.1-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:9b9d19890e9399f86300407959de41b794ee8fd1b46720c7548163f7f94fd15e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6254150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dcae0dec9d781a4ed3bd8282b836bb0fc168482d57def8fec57c690ecdd111a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:09:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:09:00 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:09:00 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:09:00 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:09:00 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:09:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:eeebf06eacfa887b3524b3c76a2593bb68e43a09aa8ff01b5a09c0ce44ed2917`  
		Last Modified: Wed, 20 May 2026 16:04:05 GMT  
		Size: 6.3 MB (6253641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb234fae2f8c35c37c5a0a2b27b551816540b8c513f6b2c479728b77a462cc5`  
		Last Modified: Wed, 20 May 2026 19:09:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.1-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:44cc5336af1db8f2f590eca54680623452cbb2da64b65bb690521c087a9be389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2bccd9ad485d0016ce5f53e02daf116336befd19e206a354f9324e36b86c720`

```dockerfile
```

-	Layers:
	-	`sha256:33b891cec5ef0cfb52212abc7e2148afd94f43e4c045f9b8ee11b24532349469`  
		Last Modified: Wed, 20 May 2026 19:09:06 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.1-scratch` - linux; s390x

```console
$ docker pull nats@sha256:02ac81902397bc3ce3ae4f6bf57bb15925e02525fc49567e8db5747ae9e3cc7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6650240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f5f893e9ed2e5671b5afc696c46fd6aa4099811ef87a81fb46e2bf0c84ba84f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:10:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:10:22 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:10:24 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:10:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:10:24 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:10:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9e00525b36acc41f758b0363af2261253b6d35899fd8e6c7e6b4d30ff05eab43`  
		Last Modified: Wed, 20 May 2026 16:04:08 GMT  
		Size: 6.6 MB (6649731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61970d60cef7c5abc0f2985fb3486911eb5ae086553cd2bfb895dd97daa5dbe1`  
		Last Modified: Wed, 20 May 2026 19:10:43 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.1-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:91a6b246de893cdf55e56ebb0f717eb35cb29121fd44454bb5c2e66fe76ba11b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b822bf8bf39b54c102cf252c8b091bac1a2c642851dd34cc7445f10b19fbbe42`

```dockerfile
```

-	Layers:
	-	`sha256:a39452d35088530375cff827daeae3695859d1f87479bba2523d135b3256d905`  
		Last Modified: Wed, 20 May 2026 19:10:43 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.14.1-windowsservercore`

```console
$ docker pull nats@sha256:1ba584aa4a0b9afe4503a0bb74145174a5a8bd168c74991253e74a0f28cb7a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2.14.1-windowsservercore` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:7c0d2cfcb1ac8b9c5c8667631fe266d5058f54979c724dbc779cd1303cf56e41
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2130333726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2e9ee9e3b452a65f51ce4b7daa32d3b40f548b8548d8e18d6af0f98c1a6fd8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Wed, 20 May 2026 18:42:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 20 May 2026 18:42:48 GMT
ENV NATS_DOCKERIZED=1
# Wed, 20 May 2026 18:42:49 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:42:51 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:42:53 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.14.1/nats-server-v2.14.1-windows-amd64.zip
# Wed, 20 May 2026 18:42:55 GMT
ENV NATS_SERVER_SHASUM=fb7ddfdde7da0ce89a5174c00b0f7fa9d559ee88c6de638c681b464d35e7caca
# Wed, 20 May 2026 18:44:05 GMT
RUN Set-PSDebug -Trace 2
# Wed, 20 May 2026 18:44:38 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 20 May 2026 18:44:39 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 20 May 2026 18:44:40 GMT
EXPOSE 4222 6222 8222
# Wed, 20 May 2026 18:44:42 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 20 May 2026 18:44:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9541aea3e55bd746462fb4c6e57da81839bbdd92cde8c45bec531dc275c949`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acaeb80d5acbf745ec935e19b9c27aac2c1c36569184a441931640832febb401`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53700d3104e235624a186296ebdbc80307001a56022c9d7a56ca8e8441f1352e`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4698b50a4704844bff262f3486b8d21762a0b2216da94ee49cf3304647a202cf`  
		Last Modified: Wed, 20 May 2026 18:44:50 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39739d4a0333d45798f9c82521d794f7861019e48fcbfc35cec644df0ae2a4bf`  
		Last Modified: Wed, 20 May 2026 18:44:50 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4785912cbc50e52449bd79d36df3b0b1c35e93f26131aeb601005aa38d99d9f2`  
		Last Modified: Wed, 20 May 2026 18:44:50 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406ecfff99aabce085a608a58a3bc33d019a6c6a474f26cd2f037294ab00c29d`  
		Last Modified: Wed, 20 May 2026 18:44:51 GMT  
		Size: 501.6 KB (501598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653bb3e0442eb7d700abb5d1a972abb676d295a6e84793deb25232914a8e833e`  
		Last Modified: Wed, 20 May 2026 18:44:53 GMT  
		Size: 7.4 MB (7397859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662d62953cb63a3accb3782436a9739838d80e2f9610ceac2e47628cc18600fe`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7ba9d33ea88ed49cf0a5cf22fe293c829f1ad64c930e440993b2cb04a3e59a`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fd31c298d20b844c00bdce2ffe2a2370b1d271d45448caa64c2c4c9817afcf`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96cf0d23ad307ba86365cfda67df65a63a9b427078a3ba2715c22735719e8dd0`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.14.1-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:1ba584aa4a0b9afe4503a0bb74145174a5a8bd168c74991253e74a0f28cb7a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2.14.1-windowsservercore-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:7c0d2cfcb1ac8b9c5c8667631fe266d5058f54979c724dbc779cd1303cf56e41
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2130333726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2e9ee9e3b452a65f51ce4b7daa32d3b40f548b8548d8e18d6af0f98c1a6fd8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Wed, 20 May 2026 18:42:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 20 May 2026 18:42:48 GMT
ENV NATS_DOCKERIZED=1
# Wed, 20 May 2026 18:42:49 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:42:51 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:42:53 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.14.1/nats-server-v2.14.1-windows-amd64.zip
# Wed, 20 May 2026 18:42:55 GMT
ENV NATS_SERVER_SHASUM=fb7ddfdde7da0ce89a5174c00b0f7fa9d559ee88c6de638c681b464d35e7caca
# Wed, 20 May 2026 18:44:05 GMT
RUN Set-PSDebug -Trace 2
# Wed, 20 May 2026 18:44:38 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 20 May 2026 18:44:39 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 20 May 2026 18:44:40 GMT
EXPOSE 4222 6222 8222
# Wed, 20 May 2026 18:44:42 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 20 May 2026 18:44:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9541aea3e55bd746462fb4c6e57da81839bbdd92cde8c45bec531dc275c949`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acaeb80d5acbf745ec935e19b9c27aac2c1c36569184a441931640832febb401`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53700d3104e235624a186296ebdbc80307001a56022c9d7a56ca8e8441f1352e`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4698b50a4704844bff262f3486b8d21762a0b2216da94ee49cf3304647a202cf`  
		Last Modified: Wed, 20 May 2026 18:44:50 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39739d4a0333d45798f9c82521d794f7861019e48fcbfc35cec644df0ae2a4bf`  
		Last Modified: Wed, 20 May 2026 18:44:50 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4785912cbc50e52449bd79d36df3b0b1c35e93f26131aeb601005aa38d99d9f2`  
		Last Modified: Wed, 20 May 2026 18:44:50 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406ecfff99aabce085a608a58a3bc33d019a6c6a474f26cd2f037294ab00c29d`  
		Last Modified: Wed, 20 May 2026 18:44:51 GMT  
		Size: 501.6 KB (501598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653bb3e0442eb7d700abb5d1a972abb676d295a6e84793deb25232914a8e833e`  
		Last Modified: Wed, 20 May 2026 18:44:53 GMT  
		Size: 7.4 MB (7397859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662d62953cb63a3accb3782436a9739838d80e2f9610ceac2e47628cc18600fe`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7ba9d33ea88ed49cf0a5cf22fe293c829f1ad64c930e440993b2cb04a3e59a`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fd31c298d20b844c00bdce2ffe2a2370b1d271d45448caa64c2c4c9817afcf`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96cf0d23ad307ba86365cfda67df65a63a9b427078a3ba2715c22735719e8dd0`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:ea17b9b7f74279b9239cf65e5786c0133e9a7c353bf218d29004abf2e7a33181
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
$ docker pull nats@sha256:4c516667ffae4977a0b4ee1d8caa5b663a0d147b66c6b2adc8ee8f3e23728bc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11103220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c133130b2f2f46568f11546ffef920fccb739e99fd733ef11ea43fc1737887c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:37:17 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:37:17 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:37:17 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:37:17 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:37:17 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:37:17 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:37:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:37:17 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6887181943c337b002058eb52d1b08afbc55add7c29a34ac80e3949090e15495`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 7.3 MB (7294060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a070bfd7422a373dc1b206300e1798aef404bf1bac5a04a3293b33f5468a167e`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4a08ddee9fc679f6a40d1ca0c325ec632bebcbb19437245764df5d7ccb6e0d`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:16deabb6f9a013834b95f04987ebab3d889f6704db15b71e13e10a4109b2e5b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d0fdb19df33d866a3c0b19c2d8aa933518ea4afc5b2f7562f2fd9364bb805ec`

```dockerfile
```

-	Layers:
	-	`sha256:650380b0910269f4395d628fbfafe98d4c910cc7a775ff48fa5093aaddc18b1f`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 15.4 KB (15403 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:32e7eb3bde61b1a81ba030cf21530f82b3713f20585f14da348ed9ff0099cd38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10540472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff1b400cc41fb9599883d47ee0cc98f26d14432cafaa79d7b00c36500c3be581`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:35:40 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:35:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:35:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:35:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac441e30d31da40cce92ca13be29a2ec33b8e530c12f39c4e6e6f821d36fa5f7`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 7.0 MB (7032117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588069c44453627769cbea386971dc510fa0a2a33fc33bc21795cbe4c6ceeb2e`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1efc9734efaa0feb255b7c30b046fb56094635c7d947db2f21f7a873a06b52a`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:e8fdb1f5ad9c517ef1795cc413d10f4304bac0bfacca20197b1324ceed658bd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67da2ba5e6d5168c0687521d71e8357c05504026864365687620573485a04e0`

```dockerfile
```

-	Layers:
	-	`sha256:63de3f19bc13cbd3dc2f28506681e74ef898d6cddd4ed65551521f9d641ff6b5`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:8805cf2aaa214d58393f7373011c4fe330f5225fb9bc4da6d715a6ab72ff8dc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10246493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32278cb7a1bf5e3ea24f7381d52c844e152750efbf7684af40245538a2fadaa4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:35:40 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:35:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:35:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:35:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3e43a7f3a2149acbd98329815e7e03d9dcf933d2131db6f8e1eecd1c01e173`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 7.0 MB (7019690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588069c44453627769cbea386971dc510fa0a2a33fc33bc21795cbe4c6ceeb2e`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9213cf8ea08c3ce1080672b9ea4c12034482854a1829a814ec22933ea91379a0`  
		Last Modified: Wed, 20 May 2026 18:35:44 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:83439ca6685120afbf799cb62bebb64b76d3419bd2523ae781dfad0b8bd8db9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f56fa87064674ea90080bd544ca88fd1b1f257088b93998a8cd46405b6249c`

```dockerfile
```

-	Layers:
	-	`sha256:22deddd2f98e84c9bc37c96058b3e88416465a5ea1004b4985cef2385de5a8be`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 15.5 KB (15515 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:abc668a25359714d7320be16684a7a6096d82a6d41aa9fbb4275c02f3fb1e716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10791094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c04c7a60cc127abb4b03f7f7593fb48cd0124f4f2cd959996fdcb5caba71e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:37:01 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:37:01 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:37:01 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:37:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:37:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:37:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:37:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:37:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b89c7be0c2d2557967711fd66cb73b3b64361381d066e02f0b52b2abeedd6b9`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 6.6 MB (6648233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b1bf5ee681da0d7929bf7d0e36bf5d24df48f214a25c32a7692f9fd0bc5eab`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2e67e1deca529e76612c525c5a8e12050d9ec84c3691673953e51573c1e653`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:5ae7b0317944de344d87247e9cb05a11dcd4f796e1800294193d7b60f43c9d9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9059f595926bbcc76e88f995c69a532e5bfdb37e53db7d9cbd26077b9a0f52d1`

```dockerfile
```

-	Layers:
	-	`sha256:a10a07e60572ceb3113b276c9a02c5aa46bf940b8f2a491e7064608fcac2409c`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:7c13d10c1f7169aaedc2ac8ecbc1f431dda7e906455b836d09a14b3b948f3036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10448793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa266dd5df001f7f566ffb0c8c8acff2de160efa06508788758a4e3022c8e98d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:39:54 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:39:54 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:39:54 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:39:55 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:39:55 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:39:55 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:39:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:39:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efe06b0c545d8e510a8131fe2984aa46a7c4d7502148ce8f2e94df5ffeed78f`  
		Last Modified: Wed, 20 May 2026 18:40:02 GMT  
		Size: 6.7 MB (6711165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3c6e5710602d0c65abfcc3a4aac8676e3cd1f849d5967bee0654b0ec045abe`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0fcc4ed5f0f4848feb91f0e5c409cb87bfd693a7056f2c0e574dbf0fc8ff4ab`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:7878f9d371c5d9227beef40f16b5dfd6d37465bab0104f835171af841d4c4a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47a1ee27b4ce5d60016cbff052995f2dbab1c7c6c61dcf79e2f75cbb1430fbad`

```dockerfile
```

-	Layers:
	-	`sha256:c27fc7351e2a880436edb13f3b1eaf0c5d83b4ec4a761386db3f8a0e0e8642a5`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; s390x

```console
$ docker pull nats@sha256:458d20eff2bdbc011304724399fc06b3db7dae7c95d0c806969fc503389a70c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10757148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0002a7df6776ecf8e0df1b73510a6014c1f519a3c9692cd787d8568dd8021d99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:48:37 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:48:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:48:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:48:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:48:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:48:43 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:48:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:48:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728aea4976117b7918cb9446c013c273cae16aa21337089d91cbd93761d10ae5`  
		Last Modified: Wed, 20 May 2026 18:49:10 GMT  
		Size: 7.1 MB (7102303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e102ba28952cc8bf83cffaefb3ec4b38d56cd736120ece8c71362ff603fd09b`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec22f8c91bd1e1b2e7f49773754ab16299137dd3226c8bb660a538d249364ae6`  
		Last Modified: Wed, 20 May 2026 18:49:08 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:38a69833b514d10d0b925fa5c4639cb5d17abe985f2b30699a0f305324397aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cffc57189208991582e7a0262e60b1415e19ac3919981144973c3d19428e23f6`

```dockerfile
```

-	Layers:
	-	`sha256:ccc40928ae38a1bd914e972d9acbe81dbc2e36b6132cee1761b8e20e7dda2db5`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:alpine3.22`

```console
$ docker pull nats@sha256:ea17b9b7f74279b9239cf65e5786c0133e9a7c353bf218d29004abf2e7a33181
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

### `nats:alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:4c516667ffae4977a0b4ee1d8caa5b663a0d147b66c6b2adc8ee8f3e23728bc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11103220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c133130b2f2f46568f11546ffef920fccb739e99fd733ef11ea43fc1737887c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:37:17 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:37:17 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:37:17 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:37:17 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:37:17 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:37:17 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:37:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:37:17 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6887181943c337b002058eb52d1b08afbc55add7c29a34ac80e3949090e15495`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 7.3 MB (7294060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a070bfd7422a373dc1b206300e1798aef404bf1bac5a04a3293b33f5468a167e`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4a08ddee9fc679f6a40d1ca0c325ec632bebcbb19437245764df5d7ccb6e0d`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:16deabb6f9a013834b95f04987ebab3d889f6704db15b71e13e10a4109b2e5b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d0fdb19df33d866a3c0b19c2d8aa933518ea4afc5b2f7562f2fd9364bb805ec`

```dockerfile
```

-	Layers:
	-	`sha256:650380b0910269f4395d628fbfafe98d4c910cc7a775ff48fa5093aaddc18b1f`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 15.4 KB (15403 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:32e7eb3bde61b1a81ba030cf21530f82b3713f20585f14da348ed9ff0099cd38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10540472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff1b400cc41fb9599883d47ee0cc98f26d14432cafaa79d7b00c36500c3be581`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:35:40 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:35:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:35:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:35:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac441e30d31da40cce92ca13be29a2ec33b8e530c12f39c4e6e6f821d36fa5f7`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 7.0 MB (7032117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588069c44453627769cbea386971dc510fa0a2a33fc33bc21795cbe4c6ceeb2e`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1efc9734efaa0feb255b7c30b046fb56094635c7d947db2f21f7a873a06b52a`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:e8fdb1f5ad9c517ef1795cc413d10f4304bac0bfacca20197b1324ceed658bd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67da2ba5e6d5168c0687521d71e8357c05504026864365687620573485a04e0`

```dockerfile
```

-	Layers:
	-	`sha256:63de3f19bc13cbd3dc2f28506681e74ef898d6cddd4ed65551521f9d641ff6b5`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:8805cf2aaa214d58393f7373011c4fe330f5225fb9bc4da6d715a6ab72ff8dc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10246493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32278cb7a1bf5e3ea24f7381d52c844e152750efbf7684af40245538a2fadaa4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:35:40 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:35:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:35:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:35:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3e43a7f3a2149acbd98329815e7e03d9dcf933d2131db6f8e1eecd1c01e173`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 7.0 MB (7019690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588069c44453627769cbea386971dc510fa0a2a33fc33bc21795cbe4c6ceeb2e`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9213cf8ea08c3ce1080672b9ea4c12034482854a1829a814ec22933ea91379a0`  
		Last Modified: Wed, 20 May 2026 18:35:44 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:83439ca6685120afbf799cb62bebb64b76d3419bd2523ae781dfad0b8bd8db9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f56fa87064674ea90080bd544ca88fd1b1f257088b93998a8cd46405b6249c`

```dockerfile
```

-	Layers:
	-	`sha256:22deddd2f98e84c9bc37c96058b3e88416465a5ea1004b4985cef2385de5a8be`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 15.5 KB (15515 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:abc668a25359714d7320be16684a7a6096d82a6d41aa9fbb4275c02f3fb1e716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10791094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c04c7a60cc127abb4b03f7f7593fb48cd0124f4f2cd959996fdcb5caba71e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:37:01 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:37:01 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:37:01 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:37:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:37:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:37:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:37:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:37:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b89c7be0c2d2557967711fd66cb73b3b64361381d066e02f0b52b2abeedd6b9`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 6.6 MB (6648233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b1bf5ee681da0d7929bf7d0e36bf5d24df48f214a25c32a7692f9fd0bc5eab`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2e67e1deca529e76612c525c5a8e12050d9ec84c3691673953e51573c1e653`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:5ae7b0317944de344d87247e9cb05a11dcd4f796e1800294193d7b60f43c9d9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9059f595926bbcc76e88f995c69a532e5bfdb37e53db7d9cbd26077b9a0f52d1`

```dockerfile
```

-	Layers:
	-	`sha256:a10a07e60572ceb3113b276c9a02c5aa46bf940b8f2a491e7064608fcac2409c`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:7c13d10c1f7169aaedc2ac8ecbc1f431dda7e906455b836d09a14b3b948f3036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10448793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa266dd5df001f7f566ffb0c8c8acff2de160efa06508788758a4e3022c8e98d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:39:54 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:39:54 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:39:54 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:39:55 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:39:55 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:39:55 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:39:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:39:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efe06b0c545d8e510a8131fe2984aa46a7c4d7502148ce8f2e94df5ffeed78f`  
		Last Modified: Wed, 20 May 2026 18:40:02 GMT  
		Size: 6.7 MB (6711165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3c6e5710602d0c65abfcc3a4aac8676e3cd1f849d5967bee0654b0ec045abe`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0fcc4ed5f0f4848feb91f0e5c409cb87bfd693a7056f2c0e574dbf0fc8ff4ab`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:7878f9d371c5d9227beef40f16b5dfd6d37465bab0104f835171af841d4c4a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47a1ee27b4ce5d60016cbff052995f2dbab1c7c6c61dcf79e2f75cbb1430fbad`

```dockerfile
```

-	Layers:
	-	`sha256:c27fc7351e2a880436edb13f3b1eaf0c5d83b4ec4a761386db3f8a0e0e8642a5`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:458d20eff2bdbc011304724399fc06b3db7dae7c95d0c806969fc503389a70c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10757148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0002a7df6776ecf8e0df1b73510a6014c1f519a3c9692cd787d8568dd8021d99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:48:37 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:48:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:48:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:48:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:48:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:48:43 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:48:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:48:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728aea4976117b7918cb9446c013c273cae16aa21337089d91cbd93761d10ae5`  
		Last Modified: Wed, 20 May 2026 18:49:10 GMT  
		Size: 7.1 MB (7102303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e102ba28952cc8bf83cffaefb3ec4b38d56cd736120ece8c71362ff603fd09b`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec22f8c91bd1e1b2e7f49773754ab16299137dd3226c8bb660a538d249364ae6`  
		Last Modified: Wed, 20 May 2026 18:49:08 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:38a69833b514d10d0b925fa5c4639cb5d17abe985f2b30699a0f305324397aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cffc57189208991582e7a0262e60b1415e19ac3919981144973c3d19428e23f6`

```dockerfile
```

-	Layers:
	-	`sha256:ccc40928ae38a1bd914e972d9acbe81dbc2e36b6132cee1761b8e20e7dda2db5`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:latest`

```console
$ docker pull nats@sha256:7f430e429d0a90444b38bd40ab7812fd3afcc49a51f6b03a931f9becd5aeb280
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
	-	windows version 10.0.20348.5139; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:aad7f400fa8a1cbcc2f818d5373638f91cfbfcac7cb9bd28fe6e8538c08b9c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6838210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39f65eeb0573eea876a604f186453a7a3cda0c8c511dd143432e1128e07a8734`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:10:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:10:38 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:10:38 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:10:38 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:10:38 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:10:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:05832d0be2949ff52eaf08a260411f3a4a020a066de4aa19dc62284052758304`  
		Last Modified: Wed, 20 May 2026 16:04:06 GMT  
		Size: 6.8 MB (6837703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a284b9b8e39214498d13f3dca35a9c9e81d34b69635ed74a3d47d26e45d5591`  
		Last Modified: Wed, 20 May 2026 19:10:42 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:6b2a0558891216e6e12622ac66d8766987858f507eee4cb4cfef25a0b1480e84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a061861dcdd34e8079637906d854df58e3e30fcfb0514aa93b4a1ada5b3936b9`

```dockerfile
```

-	Layers:
	-	`sha256:7fff463e51e2de542cc152e5196125c500561d37a866a78ab756f40188e25be6`  
		Last Modified: Wed, 20 May 2026 19:10:42 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:80f40fb067456022353b1754a4c58f49b1af454522a8af74e9c270e3a27668d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6573757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:039a8f82177ac58ba3952b7b25d8af7b14d0fbcf08e6e53efbab9e028b515cb5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:09:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:09:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:09:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:09:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:09:27 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:09:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3f675bd99a02bdb97f8ad1545908545b1e797e40d8038ce181205b0808044e20`  
		Last Modified: Wed, 20 May 2026 16:04:08 GMT  
		Size: 6.6 MB (6573248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715581626472620cc372593ae38a74d6c85239c0282bc3c5b7937fcd525bb308`  
		Last Modified: Wed, 20 May 2026 19:09:32 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:cd80c2a5593667a467031df5e49c9cab2cc1f5ae03e981c4789d7a262cbded23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac98f8edc0ec201da45e4d96bc1ea96d553e89648a61e35f8a195d38ce81d6b9`

```dockerfile
```

-	Layers:
	-	`sha256:d7cd588a4563631d4b86b381c7ee1c56114f94b80568f0e8defc278961b4c119`  
		Last Modified: Wed, 20 May 2026 19:09:31 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:ae43b4e3d705ed3a3386e6b303d8dfb011fec9e1cdf8523ff9c6387935d9652d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6565185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a493ff1dda3a5eb2f84019be4a31029f9463e5a91f142d91cbd96345245eadb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:09:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:09:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:09:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:09:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:09:01 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:09:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:07a4ad6a636748b056dca5d82613a936ff1872d9092911832cea1178d840cb7f`  
		Last Modified: Wed, 20 May 2026 16:04:08 GMT  
		Size: 6.6 MB (6564678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95ec1a5b2af5f3d81a39b2563595f7008790713449f52e148c254bc7d0be80e`  
		Last Modified: Wed, 20 May 2026 19:09:06 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:5b515d7d9aa87098056bad17534ca266bba383a9a52d362a1788c5ac7b596d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a1b7811acc104229e8cc148ff624e24efc4e31d06fce27cdd9091dd3237110`

```dockerfile
```

-	Layers:
	-	`sha256:e855458d7f5e87be1456ba294fc7386adaa0241520ff73ab4b95b94271f3d0a0`  
		Last Modified: Wed, 20 May 2026 19:09:05 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:89ea5f3d1a4e7db9650685b4b60d5f2340f6edd89f0d2a7a6f2a5cb9b6f144c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6189602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:080d11e023e3c9bc77bc5d6e137c30fcee2ca537fbda1d730ee0de9b5131cf97`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:10:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:10:02 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:10:02 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:10:02 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:10:02 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:10:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5f2fe2216ecafda68f73a81334875cb85722e57f12bc2af372cc03c4952017ff`  
		Last Modified: Wed, 20 May 2026 16:04:06 GMT  
		Size: 6.2 MB (6189094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f13aa02931bd62f5d9ce1935b8f163c6fcb3db670a4893037e6326c70ff971`  
		Last Modified: Wed, 20 May 2026 19:10:07 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:55f5544491f15bb813013ec1a1698f6e7e6f1ebbf96b4e49dba94dab9c27b313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30316b20c5d7aabdc5ded4b132f0725f10bdb7bd31bfbdb309184a8e58efe00c`

```dockerfile
```

-	Layers:
	-	`sha256:e06f44f5e5db93fe4fba02df22b44d37f71209d0cfbcbcec67b2ec6687bda27c`  
		Last Modified: Wed, 20 May 2026 19:10:07 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; ppc64le

```console
$ docker pull nats@sha256:9b9d19890e9399f86300407959de41b794ee8fd1b46720c7548163f7f94fd15e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6254150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dcae0dec9d781a4ed3bd8282b836bb0fc168482d57def8fec57c690ecdd111a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:09:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:09:00 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:09:00 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:09:00 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:09:00 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:09:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:eeebf06eacfa887b3524b3c76a2593bb68e43a09aa8ff01b5a09c0ce44ed2917`  
		Last Modified: Wed, 20 May 2026 16:04:05 GMT  
		Size: 6.3 MB (6253641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb234fae2f8c35c37c5a0a2b27b551816540b8c513f6b2c479728b77a462cc5`  
		Last Modified: Wed, 20 May 2026 19:09:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:44cc5336af1db8f2f590eca54680623452cbb2da64b65bb690521c087a9be389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2bccd9ad485d0016ce5f53e02daf116336befd19e206a354f9324e36b86c720`

```dockerfile
```

-	Layers:
	-	`sha256:33b891cec5ef0cfb52212abc7e2148afd94f43e4c045f9b8ee11b24532349469`  
		Last Modified: Wed, 20 May 2026 19:09:06 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; s390x

```console
$ docker pull nats@sha256:02ac81902397bc3ce3ae4f6bf57bb15925e02525fc49567e8db5747ae9e3cc7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6650240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f5f893e9ed2e5671b5afc696c46fd6aa4099811ef87a81fb46e2bf0c84ba84f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:10:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:10:22 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:10:24 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:10:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:10:24 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:10:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9e00525b36acc41f758b0363af2261253b6d35899fd8e6c7e6b4d30ff05eab43`  
		Last Modified: Wed, 20 May 2026 16:04:08 GMT  
		Size: 6.6 MB (6649731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61970d60cef7c5abc0f2985fb3486911eb5ae086553cd2bfb895dd97daa5dbe1`  
		Last Modified: Wed, 20 May 2026 19:10:43 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:91a6b246de893cdf55e56ebb0f717eb35cb29121fd44454bb5c2e66fe76ba11b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b822bf8bf39b54c102cf252c8b091bac1a2c642851dd34cc7445f10b19fbbe42`

```dockerfile
```

-	Layers:
	-	`sha256:a39452d35088530375cff827daeae3695859d1f87479bba2523d135b3256d905`  
		Last Modified: Wed, 20 May 2026 19:10:43 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:ad04df86864a0653927e5ff2293212d694588db88edc746ce8b917417317c0f3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134078105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc7e5bd03f66dabebd5917cf13f4067081477a5934e86d07357d04db10e33ec4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 20 May 2026 19:09:14 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 20 May 2026 19:09:15 GMT
RUN cmd /S /C #(nop) COPY file:5d608f6a5cbf80544d196a9ac38d66b2635084a5e0a392611785993205e5329d in C:\nats-server.exe 
# Wed, 20 May 2026 19:09:16 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 20 May 2026 19:09:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 20 May 2026 19:09:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 20 May 2026 19:09:18 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c815e3255991cc2df065c98a27664be46d8b5db04231449f637ecaf64c5c098f`  
		Last Modified: Wed, 20 May 2026 19:09:24 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68983020294e3083531b7192194e9d5172d2a1449eac04682b7544bb139048b5`  
		Last Modified: Wed, 20 May 2026 19:09:27 GMT  
		Size: 7.0 MB (7033380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730756958a80b0245caf373feb8024993ecef9e67a8ade759511f66d001f3f07`  
		Last Modified: Wed, 20 May 2026 19:09:22 GMT  
		Size: 1.7 KB (1672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ec9d4f153ff90a362ff5591192559ff2e3584441d0bee4e4fdd8b0a4845b833`  
		Last Modified: Wed, 20 May 2026 19:09:22 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb6e35267fc994af8eab6412783ba571dd4c1d14e5fa8771f50a386e61ef655`  
		Last Modified: Wed, 20 May 2026 19:09:22 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838e55b2d659c4cc5f4e0db1773fbe38aa8487984688f5a0f60b202907588e42`  
		Last Modified: Wed, 20 May 2026 19:09:22 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:4223c8fa116891628611e154fb66570cad599d8f8b3b131b82caf10f378e9dcf
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
$ docker pull nats@sha256:aad7f400fa8a1cbcc2f818d5373638f91cfbfcac7cb9bd28fe6e8538c08b9c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6838210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39f65eeb0573eea876a604f186453a7a3cda0c8c511dd143432e1128e07a8734`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:10:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:10:38 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:10:38 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:10:38 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:10:38 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:10:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:05832d0be2949ff52eaf08a260411f3a4a020a066de4aa19dc62284052758304`  
		Last Modified: Wed, 20 May 2026 16:04:06 GMT  
		Size: 6.8 MB (6837703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a284b9b8e39214498d13f3dca35a9c9e81d34b69635ed74a3d47d26e45d5591`  
		Last Modified: Wed, 20 May 2026 19:10:42 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:6b2a0558891216e6e12622ac66d8766987858f507eee4cb4cfef25a0b1480e84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a061861dcdd34e8079637906d854df58e3e30fcfb0514aa93b4a1ada5b3936b9`

```dockerfile
```

-	Layers:
	-	`sha256:7fff463e51e2de542cc152e5196125c500561d37a866a78ab756f40188e25be6`  
		Last Modified: Wed, 20 May 2026 19:10:42 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:80f40fb067456022353b1754a4c58f49b1af454522a8af74e9c270e3a27668d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6573757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:039a8f82177ac58ba3952b7b25d8af7b14d0fbcf08e6e53efbab9e028b515cb5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:09:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:09:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:09:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:09:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:09:27 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:09:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3f675bd99a02bdb97f8ad1545908545b1e797e40d8038ce181205b0808044e20`  
		Last Modified: Wed, 20 May 2026 16:04:08 GMT  
		Size: 6.6 MB (6573248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715581626472620cc372593ae38a74d6c85239c0282bc3c5b7937fcd525bb308`  
		Last Modified: Wed, 20 May 2026 19:09:32 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:cd80c2a5593667a467031df5e49c9cab2cc1f5ae03e981c4789d7a262cbded23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac98f8edc0ec201da45e4d96bc1ea96d553e89648a61e35f8a195d38ce81d6b9`

```dockerfile
```

-	Layers:
	-	`sha256:d7cd588a4563631d4b86b381c7ee1c56114f94b80568f0e8defc278961b4c119`  
		Last Modified: Wed, 20 May 2026 19:09:31 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:ae43b4e3d705ed3a3386e6b303d8dfb011fec9e1cdf8523ff9c6387935d9652d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6565185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a493ff1dda3a5eb2f84019be4a31029f9463e5a91f142d91cbd96345245eadb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:09:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:09:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:09:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:09:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:09:01 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:09:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:07a4ad6a636748b056dca5d82613a936ff1872d9092911832cea1178d840cb7f`  
		Last Modified: Wed, 20 May 2026 16:04:08 GMT  
		Size: 6.6 MB (6564678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95ec1a5b2af5f3d81a39b2563595f7008790713449f52e148c254bc7d0be80e`  
		Last Modified: Wed, 20 May 2026 19:09:06 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:5b515d7d9aa87098056bad17534ca266bba383a9a52d362a1788c5ac7b596d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a1b7811acc104229e8cc148ff624e24efc4e31d06fce27cdd9091dd3237110`

```dockerfile
```

-	Layers:
	-	`sha256:e855458d7f5e87be1456ba294fc7386adaa0241520ff73ab4b95b94271f3d0a0`  
		Last Modified: Wed, 20 May 2026 19:09:05 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:89ea5f3d1a4e7db9650685b4b60d5f2340f6edd89f0d2a7a6f2a5cb9b6f144c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6189602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:080d11e023e3c9bc77bc5d6e137c30fcee2ca537fbda1d730ee0de9b5131cf97`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:10:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:10:02 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:10:02 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:10:02 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:10:02 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:10:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5f2fe2216ecafda68f73a81334875cb85722e57f12bc2af372cc03c4952017ff`  
		Last Modified: Wed, 20 May 2026 16:04:06 GMT  
		Size: 6.2 MB (6189094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f13aa02931bd62f5d9ce1935b8f163c6fcb3db670a4893037e6326c70ff971`  
		Last Modified: Wed, 20 May 2026 19:10:07 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:55f5544491f15bb813013ec1a1698f6e7e6f1ebbf96b4e49dba94dab9c27b313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30316b20c5d7aabdc5ded4b132f0725f10bdb7bd31bfbdb309184a8e58efe00c`

```dockerfile
```

-	Layers:
	-	`sha256:e06f44f5e5db93fe4fba02df22b44d37f71209d0cfbcbcec67b2ec6687bda27c`  
		Last Modified: Wed, 20 May 2026 19:10:07 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; ppc64le

```console
$ docker pull nats@sha256:9b9d19890e9399f86300407959de41b794ee8fd1b46720c7548163f7f94fd15e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6254150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dcae0dec9d781a4ed3bd8282b836bb0fc168482d57def8fec57c690ecdd111a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:09:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:09:00 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:09:00 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:09:00 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:09:00 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:09:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:eeebf06eacfa887b3524b3c76a2593bb68e43a09aa8ff01b5a09c0ce44ed2917`  
		Last Modified: Wed, 20 May 2026 16:04:05 GMT  
		Size: 6.3 MB (6253641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb234fae2f8c35c37c5a0a2b27b551816540b8c513f6b2c479728b77a462cc5`  
		Last Modified: Wed, 20 May 2026 19:09:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:44cc5336af1db8f2f590eca54680623452cbb2da64b65bb690521c087a9be389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2bccd9ad485d0016ce5f53e02daf116336befd19e206a354f9324e36b86c720`

```dockerfile
```

-	Layers:
	-	`sha256:33b891cec5ef0cfb52212abc7e2148afd94f43e4c045f9b8ee11b24532349469`  
		Last Modified: Wed, 20 May 2026 19:09:06 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; s390x

```console
$ docker pull nats@sha256:02ac81902397bc3ce3ae4f6bf57bb15925e02525fc49567e8db5747ae9e3cc7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6650240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f5f893e9ed2e5671b5afc696c46fd6aa4099811ef87a81fb46e2bf0c84ba84f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:10:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:10:22 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:10:24 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:10:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:10:24 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:10:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9e00525b36acc41f758b0363af2261253b6d35899fd8e6c7e6b4d30ff05eab43`  
		Last Modified: Wed, 20 May 2026 16:04:08 GMT  
		Size: 6.6 MB (6649731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61970d60cef7c5abc0f2985fb3486911eb5ae086553cd2bfb895dd97daa5dbe1`  
		Last Modified: Wed, 20 May 2026 19:10:43 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:91a6b246de893cdf55e56ebb0f717eb35cb29121fd44454bb5c2e66fe76ba11b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b822bf8bf39b54c102cf252c8b091bac1a2c642851dd34cc7445f10b19fbbe42`

```dockerfile
```

-	Layers:
	-	`sha256:a39452d35088530375cff827daeae3695859d1f87479bba2523d135b3256d905`  
		Last Modified: Wed, 20 May 2026 19:10:43 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:nanoserver`

```console
$ docker pull nats@sha256:b8d325261e82cfa9b4561b3752e5791fc51c257bde48ca6e1ae65580749766a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:nanoserver` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:ad04df86864a0653927e5ff2293212d694588db88edc746ce8b917417317c0f3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134078105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc7e5bd03f66dabebd5917cf13f4067081477a5934e86d07357d04db10e33ec4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 20 May 2026 19:09:14 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 20 May 2026 19:09:15 GMT
RUN cmd /S /C #(nop) COPY file:5d608f6a5cbf80544d196a9ac38d66b2635084a5e0a392611785993205e5329d in C:\nats-server.exe 
# Wed, 20 May 2026 19:09:16 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 20 May 2026 19:09:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 20 May 2026 19:09:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 20 May 2026 19:09:18 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c815e3255991cc2df065c98a27664be46d8b5db04231449f637ecaf64c5c098f`  
		Last Modified: Wed, 20 May 2026 19:09:24 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68983020294e3083531b7192194e9d5172d2a1449eac04682b7544bb139048b5`  
		Last Modified: Wed, 20 May 2026 19:09:27 GMT  
		Size: 7.0 MB (7033380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730756958a80b0245caf373feb8024993ecef9e67a8ade759511f66d001f3f07`  
		Last Modified: Wed, 20 May 2026 19:09:22 GMT  
		Size: 1.7 KB (1672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ec9d4f153ff90a362ff5591192559ff2e3584441d0bee4e4fdd8b0a4845b833`  
		Last Modified: Wed, 20 May 2026 19:09:22 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb6e35267fc994af8eab6412783ba571dd4c1d14e5fa8771f50a386e61ef655`  
		Last Modified: Wed, 20 May 2026 19:09:22 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838e55b2d659c4cc5f4e0db1773fbe38aa8487984688f5a0f60b202907588e42`  
		Last Modified: Wed, 20 May 2026 19:09:22 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:b8d325261e82cfa9b4561b3752e5791fc51c257bde48ca6e1ae65580749766a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:nanoserver-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:ad04df86864a0653927e5ff2293212d694588db88edc746ce8b917417317c0f3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134078105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc7e5bd03f66dabebd5917cf13f4067081477a5934e86d07357d04db10e33ec4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 20 May 2026 19:09:14 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 20 May 2026 19:09:15 GMT
RUN cmd /S /C #(nop) COPY file:5d608f6a5cbf80544d196a9ac38d66b2635084a5e0a392611785993205e5329d in C:\nats-server.exe 
# Wed, 20 May 2026 19:09:16 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 20 May 2026 19:09:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 20 May 2026 19:09:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 20 May 2026 19:09:18 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c815e3255991cc2df065c98a27664be46d8b5db04231449f637ecaf64c5c098f`  
		Last Modified: Wed, 20 May 2026 19:09:24 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68983020294e3083531b7192194e9d5172d2a1449eac04682b7544bb139048b5`  
		Last Modified: Wed, 20 May 2026 19:09:27 GMT  
		Size: 7.0 MB (7033380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730756958a80b0245caf373feb8024993ecef9e67a8ade759511f66d001f3f07`  
		Last Modified: Wed, 20 May 2026 19:09:22 GMT  
		Size: 1.7 KB (1672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ec9d4f153ff90a362ff5591192559ff2e3584441d0bee4e4fdd8b0a4845b833`  
		Last Modified: Wed, 20 May 2026 19:09:22 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb6e35267fc994af8eab6412783ba571dd4c1d14e5fa8771f50a386e61ef655`  
		Last Modified: Wed, 20 May 2026 19:09:22 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838e55b2d659c4cc5f4e0db1773fbe38aa8487984688f5a0f60b202907588e42`  
		Last Modified: Wed, 20 May 2026 19:09:22 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:4223c8fa116891628611e154fb66570cad599d8f8b3b131b82caf10f378e9dcf
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
$ docker pull nats@sha256:aad7f400fa8a1cbcc2f818d5373638f91cfbfcac7cb9bd28fe6e8538c08b9c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6838210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39f65eeb0573eea876a604f186453a7a3cda0c8c511dd143432e1128e07a8734`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:10:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:10:38 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:10:38 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:10:38 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:10:38 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:10:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:05832d0be2949ff52eaf08a260411f3a4a020a066de4aa19dc62284052758304`  
		Last Modified: Wed, 20 May 2026 16:04:06 GMT  
		Size: 6.8 MB (6837703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a284b9b8e39214498d13f3dca35a9c9e81d34b69635ed74a3d47d26e45d5591`  
		Last Modified: Wed, 20 May 2026 19:10:42 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:6b2a0558891216e6e12622ac66d8766987858f507eee4cb4cfef25a0b1480e84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a061861dcdd34e8079637906d854df58e3e30fcfb0514aa93b4a1ada5b3936b9`

```dockerfile
```

-	Layers:
	-	`sha256:7fff463e51e2de542cc152e5196125c500561d37a866a78ab756f40188e25be6`  
		Last Modified: Wed, 20 May 2026 19:10:42 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:80f40fb067456022353b1754a4c58f49b1af454522a8af74e9c270e3a27668d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6573757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:039a8f82177ac58ba3952b7b25d8af7b14d0fbcf08e6e53efbab9e028b515cb5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:09:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:09:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:09:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:09:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:09:27 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:09:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3f675bd99a02bdb97f8ad1545908545b1e797e40d8038ce181205b0808044e20`  
		Last Modified: Wed, 20 May 2026 16:04:08 GMT  
		Size: 6.6 MB (6573248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715581626472620cc372593ae38a74d6c85239c0282bc3c5b7937fcd525bb308`  
		Last Modified: Wed, 20 May 2026 19:09:32 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:cd80c2a5593667a467031df5e49c9cab2cc1f5ae03e981c4789d7a262cbded23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac98f8edc0ec201da45e4d96bc1ea96d553e89648a61e35f8a195d38ce81d6b9`

```dockerfile
```

-	Layers:
	-	`sha256:d7cd588a4563631d4b86b381c7ee1c56114f94b80568f0e8defc278961b4c119`  
		Last Modified: Wed, 20 May 2026 19:09:31 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:ae43b4e3d705ed3a3386e6b303d8dfb011fec9e1cdf8523ff9c6387935d9652d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6565185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a493ff1dda3a5eb2f84019be4a31029f9463e5a91f142d91cbd96345245eadb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:09:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:09:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:09:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:09:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:09:01 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:09:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:07a4ad6a636748b056dca5d82613a936ff1872d9092911832cea1178d840cb7f`  
		Last Modified: Wed, 20 May 2026 16:04:08 GMT  
		Size: 6.6 MB (6564678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95ec1a5b2af5f3d81a39b2563595f7008790713449f52e148c254bc7d0be80e`  
		Last Modified: Wed, 20 May 2026 19:09:06 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:5b515d7d9aa87098056bad17534ca266bba383a9a52d362a1788c5ac7b596d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a1b7811acc104229e8cc148ff624e24efc4e31d06fce27cdd9091dd3237110`

```dockerfile
```

-	Layers:
	-	`sha256:e855458d7f5e87be1456ba294fc7386adaa0241520ff73ab4b95b94271f3d0a0`  
		Last Modified: Wed, 20 May 2026 19:09:05 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:89ea5f3d1a4e7db9650685b4b60d5f2340f6edd89f0d2a7a6f2a5cb9b6f144c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6189602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:080d11e023e3c9bc77bc5d6e137c30fcee2ca537fbda1d730ee0de9b5131cf97`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:10:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:10:02 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:10:02 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:10:02 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:10:02 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:10:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5f2fe2216ecafda68f73a81334875cb85722e57f12bc2af372cc03c4952017ff`  
		Last Modified: Wed, 20 May 2026 16:04:06 GMT  
		Size: 6.2 MB (6189094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f13aa02931bd62f5d9ce1935b8f163c6fcb3db670a4893037e6326c70ff971`  
		Last Modified: Wed, 20 May 2026 19:10:07 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:55f5544491f15bb813013ec1a1698f6e7e6f1ebbf96b4e49dba94dab9c27b313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30316b20c5d7aabdc5ded4b132f0725f10bdb7bd31bfbdb309184a8e58efe00c`

```dockerfile
```

-	Layers:
	-	`sha256:e06f44f5e5db93fe4fba02df22b44d37f71209d0cfbcbcec67b2ec6687bda27c`  
		Last Modified: Wed, 20 May 2026 19:10:07 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:9b9d19890e9399f86300407959de41b794ee8fd1b46720c7548163f7f94fd15e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6254150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dcae0dec9d781a4ed3bd8282b836bb0fc168482d57def8fec57c690ecdd111a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:09:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:09:00 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:09:00 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:09:00 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:09:00 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:09:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:eeebf06eacfa887b3524b3c76a2593bb68e43a09aa8ff01b5a09c0ce44ed2917`  
		Last Modified: Wed, 20 May 2026 16:04:05 GMT  
		Size: 6.3 MB (6253641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb234fae2f8c35c37c5a0a2b27b551816540b8c513f6b2c479728b77a462cc5`  
		Last Modified: Wed, 20 May 2026 19:09:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:44cc5336af1db8f2f590eca54680623452cbb2da64b65bb690521c087a9be389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2bccd9ad485d0016ce5f53e02daf116336befd19e206a354f9324e36b86c720`

```dockerfile
```

-	Layers:
	-	`sha256:33b891cec5ef0cfb52212abc7e2148afd94f43e4c045f9b8ee11b24532349469`  
		Last Modified: Wed, 20 May 2026 19:09:06 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; s390x

```console
$ docker pull nats@sha256:02ac81902397bc3ce3ae4f6bf57bb15925e02525fc49567e8db5747ae9e3cc7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6650240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f5f893e9ed2e5671b5afc696c46fd6aa4099811ef87a81fb46e2bf0c84ba84f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 May 2026 19:10:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 May 2026 19:10:22 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 20 May 2026 19:10:24 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 20 May 2026 19:10:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 19:10:24 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 May 2026 19:10:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9e00525b36acc41f758b0363af2261253b6d35899fd8e6c7e6b4d30ff05eab43`  
		Last Modified: Wed, 20 May 2026 16:04:08 GMT  
		Size: 6.6 MB (6649731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61970d60cef7c5abc0f2985fb3486911eb5ae086553cd2bfb895dd97daa5dbe1`  
		Last Modified: Wed, 20 May 2026 19:10:43 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:91a6b246de893cdf55e56ebb0f717eb35cb29121fd44454bb5c2e66fe76ba11b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b822bf8bf39b54c102cf252c8b091bac1a2c642851dd34cc7445f10b19fbbe42`

```dockerfile
```

-	Layers:
	-	`sha256:a39452d35088530375cff827daeae3695859d1f87479bba2523d135b3256d905`  
		Last Modified: Wed, 20 May 2026 19:10:43 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:1ba584aa4a0b9afe4503a0bb74145174a5a8bd168c74991253e74a0f28cb7a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:windowsservercore` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:7c0d2cfcb1ac8b9c5c8667631fe266d5058f54979c724dbc779cd1303cf56e41
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2130333726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2e9ee9e3b452a65f51ce4b7daa32d3b40f548b8548d8e18d6af0f98c1a6fd8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Wed, 20 May 2026 18:42:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 20 May 2026 18:42:48 GMT
ENV NATS_DOCKERIZED=1
# Wed, 20 May 2026 18:42:49 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:42:51 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:42:53 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.14.1/nats-server-v2.14.1-windows-amd64.zip
# Wed, 20 May 2026 18:42:55 GMT
ENV NATS_SERVER_SHASUM=fb7ddfdde7da0ce89a5174c00b0f7fa9d559ee88c6de638c681b464d35e7caca
# Wed, 20 May 2026 18:44:05 GMT
RUN Set-PSDebug -Trace 2
# Wed, 20 May 2026 18:44:38 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 20 May 2026 18:44:39 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 20 May 2026 18:44:40 GMT
EXPOSE 4222 6222 8222
# Wed, 20 May 2026 18:44:42 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 20 May 2026 18:44:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9541aea3e55bd746462fb4c6e57da81839bbdd92cde8c45bec531dc275c949`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acaeb80d5acbf745ec935e19b9c27aac2c1c36569184a441931640832febb401`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53700d3104e235624a186296ebdbc80307001a56022c9d7a56ca8e8441f1352e`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4698b50a4704844bff262f3486b8d21762a0b2216da94ee49cf3304647a202cf`  
		Last Modified: Wed, 20 May 2026 18:44:50 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39739d4a0333d45798f9c82521d794f7861019e48fcbfc35cec644df0ae2a4bf`  
		Last Modified: Wed, 20 May 2026 18:44:50 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4785912cbc50e52449bd79d36df3b0b1c35e93f26131aeb601005aa38d99d9f2`  
		Last Modified: Wed, 20 May 2026 18:44:50 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406ecfff99aabce085a608a58a3bc33d019a6c6a474f26cd2f037294ab00c29d`  
		Last Modified: Wed, 20 May 2026 18:44:51 GMT  
		Size: 501.6 KB (501598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653bb3e0442eb7d700abb5d1a972abb676d295a6e84793deb25232914a8e833e`  
		Last Modified: Wed, 20 May 2026 18:44:53 GMT  
		Size: 7.4 MB (7397859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662d62953cb63a3accb3782436a9739838d80e2f9610ceac2e47628cc18600fe`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7ba9d33ea88ed49cf0a5cf22fe293c829f1ad64c930e440993b2cb04a3e59a`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fd31c298d20b844c00bdce2ffe2a2370b1d271d45448caa64c2c4c9817afcf`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96cf0d23ad307ba86365cfda67df65a63a9b427078a3ba2715c22735719e8dd0`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:1ba584aa4a0b9afe4503a0bb74145174a5a8bd168c74991253e74a0f28cb7a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:windowsservercore-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:7c0d2cfcb1ac8b9c5c8667631fe266d5058f54979c724dbc779cd1303cf56e41
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2130333726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2e9ee9e3b452a65f51ce4b7daa32d3b40f548b8548d8e18d6af0f98c1a6fd8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Wed, 20 May 2026 18:42:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 20 May 2026 18:42:48 GMT
ENV NATS_DOCKERIZED=1
# Wed, 20 May 2026 18:42:49 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:42:51 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:42:53 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.14.1/nats-server-v2.14.1-windows-amd64.zip
# Wed, 20 May 2026 18:42:55 GMT
ENV NATS_SERVER_SHASUM=fb7ddfdde7da0ce89a5174c00b0f7fa9d559ee88c6de638c681b464d35e7caca
# Wed, 20 May 2026 18:44:05 GMT
RUN Set-PSDebug -Trace 2
# Wed, 20 May 2026 18:44:38 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 20 May 2026 18:44:39 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 20 May 2026 18:44:40 GMT
EXPOSE 4222 6222 8222
# Wed, 20 May 2026 18:44:42 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 20 May 2026 18:44:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9541aea3e55bd746462fb4c6e57da81839bbdd92cde8c45bec531dc275c949`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acaeb80d5acbf745ec935e19b9c27aac2c1c36569184a441931640832febb401`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53700d3104e235624a186296ebdbc80307001a56022c9d7a56ca8e8441f1352e`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4698b50a4704844bff262f3486b8d21762a0b2216da94ee49cf3304647a202cf`  
		Last Modified: Wed, 20 May 2026 18:44:50 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39739d4a0333d45798f9c82521d794f7861019e48fcbfc35cec644df0ae2a4bf`  
		Last Modified: Wed, 20 May 2026 18:44:50 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4785912cbc50e52449bd79d36df3b0b1c35e93f26131aeb601005aa38d99d9f2`  
		Last Modified: Wed, 20 May 2026 18:44:50 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406ecfff99aabce085a608a58a3bc33d019a6c6a474f26cd2f037294ab00c29d`  
		Last Modified: Wed, 20 May 2026 18:44:51 GMT  
		Size: 501.6 KB (501598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653bb3e0442eb7d700abb5d1a972abb676d295a6e84793deb25232914a8e833e`  
		Last Modified: Wed, 20 May 2026 18:44:53 GMT  
		Size: 7.4 MB (7397859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662d62953cb63a3accb3782436a9739838d80e2f9610ceac2e47628cc18600fe`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7ba9d33ea88ed49cf0a5cf22fe293c829f1ad64c930e440993b2cb04a3e59a`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fd31c298d20b844c00bdce2ffe2a2370b1d271d45448caa64c2c4c9817afcf`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96cf0d23ad307ba86365cfda67df65a63a9b427078a3ba2715c22735719e8dd0`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
