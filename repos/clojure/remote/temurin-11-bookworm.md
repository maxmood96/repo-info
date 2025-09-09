## `clojure:temurin-11-bookworm`

```console
$ docker pull clojure@sha256:12c7186dd717d506143a340809190ddecc91491c833e211c93eb3470bf38640a
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
$ docker pull clojure@sha256:9f0f19dd6dc204e476867560581f65443e17c8a6f29bfe46b02c9fb8764da61f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275277077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d594d1e1da9fc030a9c830458762dedbbc5c86edf3e543d141654a40fa9608`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aecae31e39d77991deeebd01ed059b924b89ee6ca7f5021ba338f331eebb433`  
		Last Modified: Tue, 09 Sep 2025 12:43:24 GMT  
		Size: 145.7 MB (145658228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33f7071b988566b50ece6feb09611f42408c28e6caad9044d2579dcd8ba76cb`  
		Last Modified: Tue, 09 Sep 2025 09:34:55 GMT  
		Size: 81.1 MB (81137595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efc74353257457e106cefd5750b54d0b757d2517083929e0c41ef8c7ac4395e`  
		Last Modified: Mon, 08 Sep 2025 22:30:28 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:5735717e3cdf741718a0a89752673f367905a2c26f57ca04932e01d61043f34e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7409283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:514a9e30bbe9ed25d8741c2bdaf3ba7c4db3f38a35f03303a5b1c087edc4a4ce`

```dockerfile
```

-	Layers:
	-	`sha256:b9f68df81df292310718ec9e0b3005536a5b44066c84c9e41c9b5c8e332bb4c6`  
		Last Modified: Tue, 09 Sep 2025 00:35:25 GMT  
		Size: 7.4 MB (7395031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23a30998456248f75ac11f9a825f567836446004bfe5386889c3ad70b9051077`  
		Last Modified: Tue, 09 Sep 2025 00:35:26 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ce388b3cde69b09e49caad3265dd9087f02a423f157eb60af3ceda1b1f0fde5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.8 MB (271844284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d1ede3e3a9a46fe3b83a0c0ea0a7ef82f84c44b7c7a845dd7f74afd627a040a`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d3ca051d0881543b12e94feab3be036876e99e80f6d2e45e969a88570cdc99`  
		Last Modified: Tue, 09 Sep 2025 00:37:24 GMT  
		Size: 142.5 MB (142459120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b25c1d3c5ba287e864287d8669402fdd19a6a468cd8422de6435647c70607e`  
		Last Modified: Tue, 09 Sep 2025 09:34:56 GMT  
		Size: 81.0 MB (81025499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf7a6098373450798a9863e706916c1a9b5b7ac80613f60e493430a2650d52b`  
		Last Modified: Tue, 09 Sep 2025 01:19:50 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c0c40e7937eec44dbc76e1816bca1d023b887c223733d36e269c4274d00e6ab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7415782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7dc0a2eb0c8eab9349f547906fe503dc8adc2bd8baf393ee91381cfe6543503`

```dockerfile
```

-	Layers:
	-	`sha256:75191146c40ecb12bfd8c41cd49cbb5ae6889446a9df29225ca94f06b8b75691`  
		Last Modified: Tue, 09 Sep 2025 03:35:24 GMT  
		Size: 7.4 MB (7401412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edd8e883bc6eb35c57c8200e32398bbeb3ef44c898c8875302119459528ddbac`  
		Last Modified: Tue, 09 Sep 2025 03:35:25 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:937df28df701506477c817b755730cddc48431966ca3c329329fc3231435dae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272164334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:423c08c01da4ec3e205b9de9e93b870f64c256313f24074d98209ce92253cbd7`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:33bc01697f2fcceb00fe53fe1bf433b48dc127c82c1555f61eeddeda9d72ff40`  
		Last Modified: Tue, 12 Aug 2025 23:05:53 GMT  
		Size: 52.3 MB (52338077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14db4d6f7ef9094c5e71617a54cb12d0ac6f4763bb9d1c751909909533970b82`  
		Last Modified: Tue, 02 Sep 2025 08:10:17 GMT  
		Size: 132.9 MB (132853137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:465a1ba89664eab548d0a56aa8624b0d96651ac323559f3202ac0af0bf488639`  
		Last Modified: Tue, 02 Sep 2025 08:21:12 GMT  
		Size: 87.0 MB (86972473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8387d4a34ce8471442ced5ac7026a6ce67d2f0077531b58420dc97100a69edf8`  
		Last Modified: Tue, 02 Sep 2025 08:21:03 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f50681ba73ec16414897657a818befe755f9b2f60a4af1d5fdd54e95501abdf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7407327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffdf66525a3f6da6efc17309d4da1626071e0a33d4e843ecfc3ae5f840333656`

```dockerfile
```

-	Layers:
	-	`sha256:8922ec87eedbfb57cd8534a10fce6c0c3839f01a7b219e34f57d37f32652a924`  
		Last Modified: Tue, 02 Sep 2025 09:35:29 GMT  
		Size: 7.4 MB (7393027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cebabebee846cdb36f9af0174ea2104c6f1b6d80abcaa7c7469acb4abea36b51`  
		Last Modified: Tue, 02 Sep 2025 09:35:30 GMT  
		Size: 14.3 KB (14300 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:e4cf2a123e01db97fb02d9e826c44c95c86e80c200604b30faef98707e08e10e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.7 MB (252711314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:586cfd48d54f7c91de53e2a552a69338de95c2c155c4e494c60a7df0ac132f76`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:67e2d91fae4fd9af13e4e364bf8120dcca7856e8273995cc0651acae70b27e8e`  
		Last Modified: Mon, 08 Sep 2025 21:18:01 GMT  
		Size: 47.1 MB (47137539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb4c4145d4aab829fc7e44e87d4d021835ef4b819489da06e2a7bc73faecf79`  
		Last Modified: Tue, 09 Sep 2025 05:26:58 GMT  
		Size: 125.6 MB (125622189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c89b65b53ed29f2a3102dcfa72bf810dad405521976e1403b4610d90343ed4`  
		Last Modified: Tue, 09 Sep 2025 06:13:10 GMT  
		Size: 80.0 MB (79950942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e94e0e1e487f3ee8e843eaf99acbe5581e532179be905df70f02357656ac487`  
		Last Modified: Tue, 09 Sep 2025 06:57:16 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:a2f91b512bc303aef4dde3dc4885fa42b85cea59b364c2defb0881f7cccf7a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7400606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abc57d84ccc1b1188623896fbcd3d7386f8fb5a59115e8adc2625e488b7c892f`

```dockerfile
```

-	Layers:
	-	`sha256:14f481cbe35e0fea30593a76364082cbcf149a5c736fab419fa18f10e7f8e868`  
		Last Modified: Tue, 09 Sep 2025 09:34:49 GMT  
		Size: 7.4 MB (7386354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c94934969586b5d5c9abca1d6d673db48b244410e1da5eb38a80cc54a656aac7`  
		Last Modified: Tue, 09 Sep 2025 09:34:50 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json
