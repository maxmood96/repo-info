## `clojure:temurin-11-tools-deps-trixie`

```console
$ docker pull clojure@sha256:139909650e1b3e116cd7b051012d941aab923ae9a80e0c422665c7036013ba01
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

### `clojure:temurin-11-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:b91eab3c6b7dda1e9416a068153063c379c8de3b05485ef262f1c593be243e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.7 MB (277723072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2050b0a5f57db3bda1b82f75177f7ca9ca5139a65ec362e2085b82f074116d28`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:17:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:17:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:17:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:17:53 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:17:53 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:18:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:18:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:18:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ef1b08ddd59d42b444e8f9c68a6cebbed70636aed0c242fdccb0bd61b61ba26b`  
		Last Modified: Wed, 10 Jun 2026 23:40:27 GMT  
		Size: 49.3 MB (49317121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2939ac8ab476ff537b17050b25e2fafea7bf4f86046fa7193130889dac01e4`  
		Last Modified: Thu, 11 Jun 2026 01:18:30 GMT  
		Size: 145.9 MB (145886263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2346d73161f2805a59584a137a9ec7145da5121dc043f42497a3cea17324d114`  
		Last Modified: Thu, 11 Jun 2026 01:18:28 GMT  
		Size: 82.5 MB (82519042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6725723333c7c391ec450cf0872b2261589fe9041a20786daa4582d019a98819`  
		Last Modified: Thu, 11 Jun 2026 01:18:25 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e82c52637c8b988a6b7fce0dd34b27e4cb06e23c9298acd13b2aa9026cfcffe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7502626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bf7553614ea7a774f6f0bc30e3f638cda771bac3df026ab2759243a81739def`

```dockerfile
```

-	Layers:
	-	`sha256:97d52dbb9fff535342a19eb0f3fcfed1b0b7deeeb8e9dce97dbc2502914371eb`  
		Last Modified: Thu, 11 Jun 2026 01:18:26 GMT  
		Size: 7.5 MB (7488287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b95fd9001080c5f6687ef39896cf038c73c706347f36cd193c0b1c728f2b5c9`  
		Last Modified: Thu, 11 Jun 2026 01:18:25 GMT  
		Size: 14.3 KB (14339 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a41cc0740479e18c8a2b696d4041aad635124e96f415d00c48a2a45e8c023613
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.6 MB (274599395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb06fcad152718796c30f89a05ca6a5258262d71751be005beaf3974ed1fa38c`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:22:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:22:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:22:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:22:17 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:22:17 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:22:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:22:35 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:22:35 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ed660e1af0f5da9e93a4c43fb29e86cb46fe69c76bcf11a3de9c57c987acab82`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 49.7 MB (49678169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3700278b1c069c84ab7cc5b9cdcf17cb242741f705ea63d44a0559076cdbc987`  
		Last Modified: Thu, 11 Jun 2026 01:23:04 GMT  
		Size: 142.6 MB (142582236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322149d4515c998f6687a5d70dd2f5536be7c3c48a46124434963e12bfffcb81`  
		Last Modified: Thu, 11 Jun 2026 01:23:00 GMT  
		Size: 82.3 MB (82338344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec791ab7a893900194137caeb3f2ce2acd996dac4c449d02a1f4df9b5398c1e8`  
		Last Modified: Thu, 11 Jun 2026 01:22:55 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:dc63182f2e4a9e68fe9bcc6daf0f086fae96c848f0f5e4d85f552b79275f6781
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7509755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a895c4d4a1e9ad892c6e0a7f8e471ab6a095e715f82b12e7400b93b68b25b78f`

```dockerfile
```

-	Layers:
	-	`sha256:19d31c14c99e6b6a0664d3d1bfe2193c3cd862c27c5f853a1c2e6073ac0eeda3`  
		Last Modified: Thu, 11 Jun 2026 01:22:56 GMT  
		Size: 7.5 MB (7495298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c332917f5fb91d03306e64da2c0fb31c9b830484dd884ed6d223e9ff61902930`  
		Last Modified: Thu, 11 Jun 2026 01:22:54 GMT  
		Size: 14.5 KB (14457 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:d334ea2be82323f31e710376358f7e143560e3b06c730d7472ce4b128d1a980f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274187586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0c956bcd1d641492d0446cfed0a89b839a0aa1de50fa3dd4b50cd5023b12ce2`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 09:24:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 09:24:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 09:24:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 09:24:10 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 09:24:11 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 09:28:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 09:28:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 09:28:14 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:fc2380819f7227178ecd607b245c244d8811737f42c6112caf011a01a3889a8e`  
		Last Modified: Thu, 11 Jun 2026 00:24:43 GMT  
		Size: 53.1 MB (53137939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9054a5ac768834a10d14169acc177113311408987ed6c5625592f8ed37e45e6d`  
		Last Modified: Thu, 11 Jun 2026 09:25:29 GMT  
		Size: 133.1 MB (133110170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5310cbe489848e76efa60ac2a5640dccb93faf42265d4877bfe51542b819d4b`  
		Last Modified: Thu, 11 Jun 2026 09:28:52 GMT  
		Size: 87.9 MB (87938833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3110faa215a187e4aa6ebf806d1a98de8cee6aff2f6f1b0184dea8adf86e73e4`  
		Last Modified: Thu, 11 Jun 2026 09:28:50 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f7657b1550a8067411c30abdb5b7eb06c59af2dbd399e9d88b95eaaf0ba531df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7505525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a7093acd910f880d1a60f52417742b4e099add5209afd5457908ca6c5c4089a`

```dockerfile
```

-	Layers:
	-	`sha256:d054e76b0b83f569a4616d1feba934f4f4fb5691f3b23d23620d77133b3332e7`  
		Last Modified: Thu, 11 Jun 2026 09:28:50 GMT  
		Size: 7.5 MB (7492093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d7123c1feffac3454a6be5f75844b17b8a93ec1fd855947ee8e57b48ce038be`  
		Last Modified: Thu, 11 Jun 2026 09:28:50 GMT  
		Size: 13.4 KB (13432 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:f3173caa1347ffba0225ea658b251531cc60aaa21043a047a9b2420b7c5fce55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.5 MB (259540491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d2d5a9733374e8a34fcba970268d739517fde77c82129cde5a3f57b48ab07f4`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 03:06:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 03:06:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 03:06:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 03:06:55 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 03:06:55 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 03:08:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 03:08:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 03:08:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0ebf827318debac5b829e4cd5c36e0122490cf2392f532aa02b2b0999d5c1b37`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 49.4 MB (49385897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c97d8205f9a0577392faa69937ce07f45a0f333503df39ff6079a7df8f8d98`  
		Last Modified: Thu, 11 Jun 2026 03:07:40 GMT  
		Size: 126.7 MB (126651735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64d2329a8022ae64e0b1f10f20052f6cf57d67db2278def81f5d87d53bb6601`  
		Last Modified: Thu, 11 Jun 2026 03:08:50 GMT  
		Size: 83.5 MB (83502214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c9ff44cef803514a5c049e5a2c551b1b273cf948b2c5f76b12b152571d5ee4`  
		Last Modified: Thu, 11 Jun 2026 03:08:48 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:bd874024235dfda4a59283eeceaf86606af399d91587292adf2e17dc21d92198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7498551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9363d7bc5d3b4cf20f73de646624612d1f7867200f86bfa4e9427af9b739e04a`

```dockerfile
```

-	Layers:
	-	`sha256:4f165cb649c7d25504063ad5fd19f09913a64aabc55104302d77651aca496d89`  
		Last Modified: Thu, 11 Jun 2026 03:08:48 GMT  
		Size: 7.5 MB (7484213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1d873bd18fd0617b1cc1a51cfb20d4d2c1506d253e497ef26d0f3076a0e829e`  
		Last Modified: Thu, 11 Jun 2026 03:08:48 GMT  
		Size: 14.3 KB (14338 bytes)  
		MIME: application/vnd.in-toto+json
