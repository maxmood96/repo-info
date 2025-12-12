## `clojure:temurin-11-bookworm`

```console
$ docker pull clojure@sha256:20d10996febde4a159ac213a8c716f450884c1086840cd8631e2524018117a27
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-11-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:d3b03df681a0b217b05f19b56fede20e2eeb26f062cc3bb7742cd5e461b870b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.6 MB (274595353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eec3c93e3c43afaa14d3d95cf37761fdbe233b8151647bdcd2a5850daa6e22e`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Thu, 11 Dec 2025 22:38:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:38:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:38:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:38:33 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:38:33 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:38:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:38:47 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:38:47 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44944d0a6995b4c476f951265630c6b82232884258fb9c289a99666c8d612276`  
		Last Modified: Thu, 11 Dec 2025 22:39:33 GMT  
		Size: 145.0 MB (144966645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14359ac47fb88016dfd3f28271531ac49ed19aa133821083294966b8c01c1c84`  
		Last Modified: Thu, 11 Dec 2025 22:39:27 GMT  
		Size: 81.1 MB (81147325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6426b66a5722972ded1a54e5a601063d3aaf473633fd78e761cb327a1e12ff92`  
		Last Modified: Thu, 11 Dec 2025 22:39:16 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:4ed02c6b2515970de11a0b7ebd0727eb2d9e8390de4d31f1d1c89b686d7b2f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7409239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9af7ad7dbc210aa33267a2dcade7c3d4f59c7e9a198afcc11356f31b67b7e4fb`

```dockerfile
```

-	Layers:
	-	`sha256:6b79f8272447a50c9fae60c4a18373ac24f26be18dac7ff94a61c04186848a85`  
		Last Modified: Fri, 12 Dec 2025 01:34:58 GMT  
		Size: 7.4 MB (7395031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e789b1434cc2c6ddc1a8deac49129d94d179613a99622f88590a59746f3a3f9`  
		Last Modified: Fri, 12 Dec 2025 01:34:59 GMT  
		Size: 14.2 KB (14208 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bc5f25a76ad540f8df9f184302fcf7c5382fe8c096ef09d3fd170820cf7a42ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.1 MB (271116620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76d0082e5562055e38dedcc383e7ead6fb958f5df5f2475c25a41016b0156a0a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Thu, 11 Dec 2025 22:38:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:38:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:38:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:38:29 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:38:29 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:38:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:38:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:38:44 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7f2b9668af76f73927725e2d1fb5d7224604d8c4c42cb8cdecb502257d9101c4`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 48.4 MB (48359071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562b1c8ec36a43688a72ac3d4c1c9a56447acd0bf0017122d6109131a3ef621b`  
		Last Modified: Thu, 11 Dec 2025 22:39:08 GMT  
		Size: 141.7 MB (141731581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfad36701dbc2b23e1d26df21da281641d2bc069c31a68cc2c73200a51b2adc5`  
		Last Modified: Thu, 11 Dec 2025 22:39:24 GMT  
		Size: 81.0 MB (81025324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481e77bc1f47194eac06990dcad6d8c2eede682a4916af58946fdf201b87c924`  
		Last Modified: Thu, 11 Dec 2025 22:39:14 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:17b30ec24ae7fd6fc5ab96d11e53ca7cbd927ec8fd4fe7124ec3239a4e049355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7415739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bac4eb3e053e9c071636268e922e18e0b0a593d748ad03c996c32bb1f2dcef1`

```dockerfile
```

-	Layers:
	-	`sha256:079046c4cad81f5f72ad6999cc0c55bd98d16c633702457b5458ae614ee5edd1`  
		Last Modified: Fri, 12 Dec 2025 01:35:06 GMT  
		Size: 7.4 MB (7401412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf735c83865d5ac442e49f97a261fc2198c1f0cb84207a599a80879df83059d9`  
		Last Modified: Fri, 12 Dec 2025 01:35:07 GMT  
		Size: 14.3 KB (14327 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:77f51d30954e40caf6fd600872895471bd61c243e8e6ba093a4bddf8aadad829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.4 MB (271392236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e1daa0b7196597bfac71e1f36baf0b4b96727841bb09c91b0138487dd0fa5f5`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:40:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 22:40:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 22:40:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 22:40:17 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Mon, 08 Dec 2025 22:40:17 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:48:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:48:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:48:19 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c088128ea77bb5c706bb00930020ea2fba147060275f49c5a7be6b54af5ca7c8`  
		Last Modified: Mon, 08 Dec 2025 22:17:06 GMT  
		Size: 52.3 MB (52326977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea2fdeb54b2cee4553e719a73e258ac39eb559f4d51f9bcd020d029ca3c9cb5`  
		Last Modified: Mon, 08 Dec 2025 22:41:54 GMT  
		Size: 132.1 MB (132081948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40942d15826f8c7185eef886ce2fef3a88f6e2fe40e356e4d9d48bfb30ee014a`  
		Last Modified: Thu, 11 Dec 2025 22:49:37 GMT  
		Size: 87.0 MB (86982664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71569a5b5ff641a66890fa464ba3a2d48a6cc29bf871f036ab68a8647f0d5018`  
		Last Modified: Thu, 11 Dec 2025 22:49:20 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:7c086f8b4191043e458aba9fbfdd1474cd143b333da65c0074224b8995b1ab9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7413887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b38d5c68aca6f3c8609a6766476bf37063d372a1d5228fbe44b377f37c7729e2`

```dockerfile
```

-	Layers:
	-	`sha256:b33307ba5e0e47a1fe54069f4d9ba2d44469ac2993190873a2c81c6a8fac9b3a`  
		Last Modified: Fri, 12 Dec 2025 01:35:13 GMT  
		Size: 7.4 MB (7399630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b86e206c38d9dbde4d80337a2454ce638b81c99e80f5a9a0199bb7d67676e129`  
		Last Modified: Fri, 12 Dec 2025 01:35:14 GMT  
		Size: 14.3 KB (14257 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:e9e3b07b6ec6882dbd0fc92a0d84f5e5cf41c826c0231b64b449017e5f0528fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.8 MB (252788073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4afedb4d0387a6c43550ebc82bb952d10221f757a91580e112e42dfd27d30c42`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 01:26:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 01:26:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 01:26:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 01:26:04 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 09 Dec 2025 01:26:04 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:32:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:32:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:32:14 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f1896ba83f603ad81e0d8cb48b496e763b4b781a68efe11f1b6de9da929514ea`  
		Last Modified: Mon, 08 Dec 2025 22:15:09 GMT  
		Size: 47.1 MB (47137665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0da402ac0335fa8c106407457a6e9dff3b61dd890c09a3107b689a3f9fc23b`  
		Last Modified: Tue, 09 Dec 2025 01:26:58 GMT  
		Size: 125.7 MB (125694469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3d6680726353b716b7ad6728a4f58db4a9e1135b241ce77d884ac33988f634`  
		Last Modified: Thu, 11 Dec 2025 22:32:54 GMT  
		Size: 80.0 MB (79955293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f4203cd40305e1efa94475fc0de9081d44fc4a300b62d405760f243378ddc69`  
		Last Modified: Thu, 11 Dec 2025 22:32:46 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:93e391877e0058104ef636b51de48467279104f5d1603744dac8da3a27646b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7400562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3591b14ec7def9fbcd402e7c45bdc4e6998d82df912ac1df99b7cde53f51923b`

```dockerfile
```

-	Layers:
	-	`sha256:b9c989828c15612244b4459259716d60a9bcbcc0d84ba5defa779f1ae5317941`  
		Last Modified: Fri, 12 Dec 2025 01:35:21 GMT  
		Size: 7.4 MB (7386354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9aa72b710c24648b22921e7de0efcbac4f146dace6907c3abe4265cefa5f3e8b`  
		Last Modified: Fri, 12 Dec 2025 01:35:22 GMT  
		Size: 14.2 KB (14208 bytes)  
		MIME: application/vnd.in-toto+json
