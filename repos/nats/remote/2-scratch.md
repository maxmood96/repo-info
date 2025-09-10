## `nats:2-scratch`

```console
$ docker pull nats@sha256:5c7800cd46520feeef6ab80a168490cecfc86de38dd5be577cdcf311f36f3d91
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
$ docker pull nats@sha256:0366581599528ac497ee0495b85e912578564d47f4d00026c5bb46c155d3e9e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6361335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7a832dff1ddf9d7f164c5bcdfb99a174a196e2cc089cbd53cef0f6c506acdd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f1e5e99e9e8e314054239bd52d522a319466a9f7fcf972882b9818712e711c80`  
		Last Modified: Tue, 09 Sep 2025 15:32:16 GMT  
		Size: 6.4 MB (6360826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe0db0261279bad5dfe553062862dcf60b5e8df2ace4b10e4c593cfadf39869`  
		Last Modified: Tue, 09 Sep 2025 22:08:30 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:4497347445f7ccdefb45098959d69760b32679a1f2581284b3b9823e0785708a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007a27366aa1f5a38775ec5d381496143b4ca2fe9fd846ab69d84bdca5b13e0b`

```dockerfile
```

-	Layers:
	-	`sha256:02bc7ec45ccee88b20cb26fc0833f8670ce32e9f9c7a30dde2c7e535470c8ada`  
		Last Modified: Tue, 09 Sep 2025 23:56:23 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:df59895e6f317d92058c3f53b1a9544b96fd80579ec950b7e4d67f9c9b539690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6074491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f123bdee14496687de6ec3eee3447c6381fb3717dacaea05474bcadc2019fa48`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2b6f7cc8134ea0773d9caff5bf8e8875997f13c8890f8858a07fb618d4226024`  
		Last Modified: Wed, 10 Sep 2025 03:04:11 GMT  
		Size: 6.1 MB (6073981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb47342606c525913bb81290e7197a7595dc146afc44e19cada08858b97216a5`  
		Last Modified: Wed, 10 Sep 2025 03:04:04 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:54e77c5788599e7eca88e13e6508731e74173b3ad37aafd0a6d0de641b4406cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82e8cdfeea16ef858ef72dfa7ce6045c67bd558c9582f9f8ae22495bed5fe874`

```dockerfile
```

-	Layers:
	-	`sha256:1c69d82154a696989581e38dd2bdfeb417abc08245f0697898c4a790ef82be6b`  
		Last Modified: Wed, 10 Sep 2025 05:56:22 GMT  
		Size: 10.6 KB (10597 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:6a518a104ae2b1aad0647dd838be7967a9fe0a3009480644f3bdfc14b2e429e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6064454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:645f3612cba5f4aac9aedee3e8d59dec572a714a915d6c24960ff00c40cbeebd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8c5268ea0d0b83bfc9157796de81bd3fab9dce3a7b038b6beaf1911cc37a60cb`  
		Last Modified: Wed, 10 Sep 2025 03:04:41 GMT  
		Size: 6.1 MB (6063945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6433b4eb34ec7229032973eb2ef093451a00bc9227dee8d939c6a96a0f1b35`  
		Last Modified: Wed, 10 Sep 2025 03:04:33 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:f9bd1ebe6d8849975174dc9ce0c43e7c9297cc648ba8d41d21b859e5ae0afb56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:788549f1effaeaae27143b3960d07f2aeeeb70d82b5b1f59bdc61f31e4dee93f`

```dockerfile
```

-	Layers:
	-	`sha256:f6e74ad52574f198559a65cf1b2fbbacfc0d6f10bf2b72eee72aacecaa090175`  
		Last Modified: Wed, 10 Sep 2025 05:56:24 GMT  
		Size: 10.6 KB (10597 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:7781e7c23d25ee4d13bf87dbd07619596faa25f465b3d526237c4e683457e7b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5848847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6e69ca2ac8851f45d9ba52346473cfd8424ec21aef83f48d05be81f999a0b06`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cbde7a53b4e0a59cd5430565c0294229084bce14d9b5024c316fced138b10546`  
		Last Modified: Tue, 09 Sep 2025 16:18:18 GMT  
		Size: 5.8 MB (5848338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cedfa50f58252aeabd0f5034bd79cc5b82d9661cf625ebccb95f9f5e62c3fc33`  
		Last Modified: Tue, 09 Sep 2025 22:09:04 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:e1cb1d77737cabfc6940ec9b6736786f03b9512ba1ffd98625711f49feab89e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73246af39702079d557176a46db0601015f8a0969434d96c3d90f12cf81dfd1d`

```dockerfile
```

-	Layers:
	-	`sha256:f29e37449541a809b445fe1393a998d8b691e0288279c99ad212f42cd108d8de`  
		Last Modified: Tue, 09 Sep 2025 23:56:30 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:70ad109d17470e9dbefe10df2ea372ea487e5a28cf96934110c5f6e6b118c4ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5807845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dcf49d098aee252cf17a17945623b98c12312f01460230bd2494a20949c2703`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:221614c6b4427295323da315f973992219d61abd51aa73f549b80d617ceed783`  
		Last Modified: Thu, 14 Aug 2025 20:45:44 GMT  
		Size: 5.8 MB (5807337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea070ca5e9aa9e1edaa1764d931a0b0e385793e5b3124004b4ba91da5efc9e9`  
		Last Modified: Thu, 14 Aug 2025 20:45:40 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:bf4cec841a590e736bc48410cd41b4eb5176b07e39b161d5827a0dfe411fb72c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bd14ce8eff83929fceb915b93bd248d9837b402d7c289ab095bb35b5306608d`

```dockerfile
```

-	Layers:
	-	`sha256:f968b5bb7ad9cd95b31e5948c6d247e8ff2820fa830ca084746ac40f662b15d1`  
		Last Modified: Thu, 14 Aug 2025 23:56:26 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; s390x

```console
$ docker pull nats@sha256:98ab2d71a429177db97a9d5d21a237338d1db9dfe83790d4956d34ad1a270587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6196001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0cdf0e571cb9adb8c61493ab9f778b8ce9e9573709427e85a3dd7a2d988a972`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:33d4b78a45d256556f78665974744159b23f603ddfaa92c5cd874b4206ea9f67`  
		Last Modified: Wed, 10 Sep 2025 09:03:20 GMT  
		Size: 6.2 MB (6195492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6913cd8ec5da2c71d2db0113e3c442ec35ccc80764a3148e938087400c787e33`  
		Last Modified: Wed, 10 Sep 2025 09:27:52 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:2ddcee029df0dd3112a0d83e79de8f1ac9ded95665165b9c9d3c88aaf891b653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa10e2de6cc16fde4ddbb1022eb94a44c06f84c0d44042adbe03cd3fbdeda85`

```dockerfile
```

-	Layers:
	-	`sha256:14177593028ae4bbb71f1b5c45b4d2c8a21583a230c79d05c154714e458ec563`  
		Last Modified: Wed, 10 Sep 2025 11:56:27 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json
