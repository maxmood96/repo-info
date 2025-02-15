## `nats:2-scratch`

```console
$ docker pull nats@sha256:8c07c320366d9ab1531607e96faa531fc0daf94dcdf7e92e80fab5d5d0dd217b
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
$ docker pull nats@sha256:a3cce34063e2171e52961998710abcb68c0af5ce582b4bd261a0e73d991b05ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5908740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0adf374ee8949cadaebd08ad86e992523bcb3b988aaeabd23a0f982b42962ad`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b0ab7b6cbd4f04e3ccfc7e43007f7265c99112ffd21d84d3216eb8066171328c`  
		Last Modified: Fri, 24 Jan 2025 01:11:44 GMT  
		Size: 5.9 MB (5908232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809716529f1b9d64de6f836666c6a4c543cf6e9c48fc283a26ee651aecdb4999`  
		Last Modified: Sat, 15 Feb 2025 00:56:28 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:0633f77705ca0fb4f0c1f0a9365c42b39cd14dc9cbdfce33ffc4c73770652dd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55dbb8da0c17d4a24f1468741734648fa7e4b817d6f57c94c74a950e25f80f1c`

```dockerfile
```

-	Layers:
	-	`sha256:983b8962d9613c7d12384470fec9ffc9324734f010ef39b6edb64a855226f206`  
		Last Modified: Sat, 15 Feb 2025 00:56:17 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:907407420d3e9ba94671a7c000937b1a0dcdf18331a8b99a7d7e19e88895b546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5558542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab1619fc65e8146b5b114ff9d595ae238d0721250f1f51ddc72f514786a5bff`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c739286a1eb26d88eea2bfa99a29b1319b70d05868d157fe40c186fb43158e5`  
		Last Modified: Fri, 24 Jan 2025 01:11:44 GMT  
		Size: 5.6 MB (5558034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97295afa42b2558422039cb042bc418cfdc6df8afc9b6e8e7a9d9cc0f96169b`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:0bb608d112d13f92d2126b84d0251ea63930d03a10fb27c45d05d31c57f780c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89066d5d3d9e338d818e7c2aa03b09333e6e431746e67d73ef1b2c746b6ae358`

```dockerfile
```

-	Layers:
	-	`sha256:f4bb13e94c06463c9a1e7db8944b4ef2f51270e9a9f9ef3aa05684d9445c562a`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:488b90f04339fca9728f4951e9ad8ba55f8f900cb8c4751756637e7d8bd2d995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc0b2fa9c3ab6ac63944db04254bd5e5d17ad1ebe0638fc63fad21e9865853fa`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1399c48aa9c68af4b7de581a13cf0ec1bfbe3133690d03f24371574694d40756`  
		Last Modified: Fri, 24 Jan 2025 01:11:46 GMT  
		Size: 5.5 MB (5545979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481dcd244ab71a71ee9b9fe26c2964654abe92238c9f0d884ee0c699ccf59640`  
		Last Modified: Fri, 24 Jan 2025 01:11:45 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:e7c9614a8f08c2147e7188ea2ff5b0c52f28ffd502158643855b52f42223a6ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ce5f946a7951df51bf1a314c263faf9026b15a2082e73c4def270135f6bf2e`

```dockerfile
```

-	Layers:
	-	`sha256:07711e5ebb4f91ff8c9c5ed71d8487590a3c5789740123f154f8cb6617e4df17`  
		Last Modified: Fri, 24 Jan 2025 01:11:45 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:63bdc87cb63f584a3a60786100ae1195bcd67c9c6e8c9a8aa10de82ae5ab7e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5458697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e445c826e9720a9666773ed4e3ac2406f8b4d0eeaa0af2d7059b8e37597ee1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e0a114dd0250b8bf3ba799553b9c1ed6689c907a86d69dc80c2b7c19554f649b`  
		Last Modified: Fri, 24 Jan 2025 01:11:47 GMT  
		Size: 5.5 MB (5458189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97295afa42b2558422039cb042bc418cfdc6df8afc9b6e8e7a9d9cc0f96169b`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:a98ab643def392a3228cb986f42774fd3fd387751bfd7ebda9bcae8ea5a2112f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:185708e96c1654a4c771e548cc6b45da84ddbb18969a03f169da285cbffeafb8`

```dockerfile
```

-	Layers:
	-	`sha256:812b02d5eb49e9f6787679987eda5039cc446dec7b062f61ab99b11cef1b70d9`  
		Last Modified: Fri, 24 Jan 2025 01:11:47 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:434c658bc44b8b9dcab77f74cfad202c200736a8461f5d265dae43c873adc9e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5423162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a74f3ad6ea74c5856e162d25336c70f7a796ec1c80f6eac76353e29aedd0a276`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37f24eed68b496d8539fa581425e2e13b88b0c51d26fd4d01b05df701440639f`  
		Last Modified: Fri, 24 Jan 2025 01:11:47 GMT  
		Size: 5.4 MB (5422654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1570ebf2846c1ac3745f0511a216eace0026742ba8ec4daecfc127a0f9662cfc`  
		Last Modified: Sat, 15 Feb 2025 02:30:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:da5b993e04aafc807cd0165c760b94933d34353a2feb454220ac1ca4a44037d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7834ebdcd9c91d3d31870e814669c44adce88e5d6204859c0816a6577673b3ec`

```dockerfile
```

-	Layers:
	-	`sha256:224a4e70cf72f1667da6acadc14554fbf2d958040a351cf7ca1ece7ef8a414d8`  
		Last Modified: Sat, 15 Feb 2025 03:56:22 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; s390x

```console
$ docker pull nats@sha256:120f05f21700741861065232b957d34875b121529dcfebd4e4e2ed1b65243aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5752043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78f9a6d423e17760a1c0596eab9d1b2d58f619748bd5738cb3643ab9d565d4a7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:89e691e76569a64cd402c4b21acd57d1e4a79c42c6a04faaa925902a0c35cf6b`  
		Last Modified: Fri, 24 Jan 2025 01:11:49 GMT  
		Size: 5.8 MB (5751534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78bb58bc5c01f048f85b7106af4b332f3b0b3ebdb2c8686f83ea2a3cb5085fec`  
		Last Modified: Fri, 24 Jan 2025 01:11:49 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:f2680e2ebdb2231cf9f2c1a7caed0ead5654c7067080669530accc8dbc402fec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f808ecf65a3b9a11f96880bd8e99059848afcd1c374040a6bb9349203aff4162`

```dockerfile
```

-	Layers:
	-	`sha256:4b106a1a302d1726161028aba125a47ba72b3899e91ce153422cdb67b669748d`  
		Last Modified: Fri, 24 Jan 2025 01:11:50 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json
