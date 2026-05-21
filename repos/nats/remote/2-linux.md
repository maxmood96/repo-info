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
