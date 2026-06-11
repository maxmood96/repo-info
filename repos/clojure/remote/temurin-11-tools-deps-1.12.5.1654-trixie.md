## `clojure:temurin-11-tools-deps-1.12.5.1654-trixie`

```console
$ docker pull clojure@sha256:9e65a977b703de0c11078377e078372dcd7045b32b7f151fbb628b4a9fa5a8c8
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

### `clojure:temurin-11-tools-deps-1.12.5.1654-trixie` - linux; amd64

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

### `clojure:temurin-11-tools-deps-1.12.5.1654-trixie` - unknown; unknown

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

### `clojure:temurin-11-tools-deps-1.12.5.1654-trixie` - linux; arm64 variant v8

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

### `clojure:temurin-11-tools-deps-1.12.5.1654-trixie` - unknown; unknown

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

### `clojure:temurin-11-tools-deps-1.12.5.1654-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:29c48c099b92a43b552fed44e63ca3adb98969acd77e4e304fcd65c1d874dccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274180932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21b8d4fd2c4d794178cf1b905ee5e43219f8de89fb5e55d80686e4d1d0f53da7`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 17:50:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:50:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:50:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:50:24 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:50:24 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:51:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:51:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:51:10 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:55497c62a793e62a2e78a3fd85fcedf060da73e331ad107733199ea991106b96`  
		Last Modified: Tue, 19 May 2026 22:37:59 GMT  
		Size: 53.1 MB (53132182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91fa5e0dab8382a47cddbf98542ec1fd458e09183790d7d69c6930b01b1f581`  
		Last Modified: Thu, 04 Jun 2026 17:51:57 GMT  
		Size: 133.1 MB (133110217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23bc2298bfff1e502d14b5e090568de211dbfe783a2ba64394ba3a8fdef334c2`  
		Last Modified: Thu, 04 Jun 2026 17:51:56 GMT  
		Size: 87.9 MB (87937885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d616bc42e44ecdf53f4aa4fdf8368a27986344ecb1eaa62d14211b0545bfbeb5`  
		Last Modified: Thu, 04 Jun 2026 17:51:52 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.5.1654-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6cfaf10c792a65e907d8523c9c51ad563b09960b6f08aa3ad2545d4a56fd19c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7506480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55d6a6050a9f2e6759c14168bef8bf73ac28dba59e5b72dc0008091083000740`

```dockerfile
```

-	Layers:
	-	`sha256:4cbe4b472ef45f212eec3bbae09eac6f4622e77f2007ee04f63d1a815948eaf2`  
		Last Modified: Thu, 04 Jun 2026 17:51:53 GMT  
		Size: 7.5 MB (7492093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdf421e0d1542590098bd3cfc92e7cb4b9cb740fcadccdf7c7abb68ce890fcbf`  
		Last Modified: Thu, 04 Jun 2026 17:51:52 GMT  
		Size: 14.4 KB (14387 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.5.1654-trixie` - linux; s390x

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

### `clojure:temurin-11-tools-deps-1.12.5.1654-trixie` - unknown; unknown

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
