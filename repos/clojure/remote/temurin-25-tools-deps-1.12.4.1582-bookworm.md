## `clojure:temurin-25-tools-deps-1.12.4.1582-bookworm`

```console
$ docker pull clojure@sha256:d4a8076a7c567b79d4f4c9ad1c36c8c33f75dc5b1e3a3b8347c905ba573b2bf4
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

### `clojure:temurin-25-tools-deps-1.12.4.1582-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:9d085039fe63e40225b142a775ddb14ff079b69980acf22445569fc994735251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.7 MB (221673875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7605a2686f267fdefcea242921956cc9a13c70e8fabe3e4b412e8a83f5bf08e2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Thu, 11 Dec 2025 22:40:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:40:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:40:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:40:20 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:40:20 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:40:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:40:35 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:40:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:40:35 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:40:35 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dabf0df64a25fe54bb1b2c94946c7dbf3e4b008e80cddc7385549513426cdfc`  
		Last Modified: Thu, 11 Dec 2025 22:41:17 GMT  
		Size: 92.0 MB (92045295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb384f33f20be8d43e15f00b757112067839e24122646f6919f7e8a4ba0b4a7`  
		Last Modified: Thu, 11 Dec 2025 22:41:14 GMT  
		Size: 81.1 MB (81146804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32044688606fce5ee99fefc8d51616ca39b4b9fbc9ca6e1fe63b762eba43ac8`  
		Last Modified: Thu, 11 Dec 2025 22:41:04 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177a49adcd085c9a1f7ad69b4efeb4b34429606e89061d923663661968dc346c`  
		Last Modified: Thu, 11 Dec 2025 22:41:04 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1582-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:2c0bf77bc130757d7d12a6ae37e935b280315bac169fc884f8f103c4c10559fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7345325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e31897b75e961241c2cc94b3747280c68aac46a0a5f4f460d75e44b8171dfc2e`

```dockerfile
```

-	Layers:
	-	`sha256:065aff4a5aa9205edefa3e52a5721739490bcd2e112d6ac277fa58f337204ad9`  
		Last Modified: Fri, 12 Dec 2025 01:43:50 GMT  
		Size: 7.3 MB (7327554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dd50425dbc634611fe1bf4dc18daf781470604329fe948de710bf66f2921b7e`  
		Last Modified: Fri, 12 Dec 2025 01:43:51 GMT  
		Size: 17.8 KB (17771 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1582-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f7d6414626c6baefaddc7963a2e3c35ff87d94463037407f039da82261521e50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.4 MB (220438249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103d27b444b8812463113aa9aec2c2654f8e81d7f1343fd34c51941f48a8b94b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Thu, 11 Dec 2025 22:38:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:38:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:38:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:38:20 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:38:20 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:38:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:38:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:38:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:38:36 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:38:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7f2b9668af76f73927725e2d1fb5d7224604d8c4c42cb8cdecb502257d9101c4`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 48.4 MB (48359071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dfa49db300f867106f819bec2d41ceccf961e060a894816d56af2502a43b572`  
		Last Modified: Thu, 11 Dec 2025 22:39:12 GMT  
		Size: 91.1 MB (91052482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f642ab5b417a16009a4a15d66678a883b3ef8f40c06315a4ee365c61f61ecf`  
		Last Modified: Thu, 11 Dec 2025 22:39:10 GMT  
		Size: 81.0 MB (81025655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c9bd8e51006e208fc55a1715dc0df81657f25288f1116027042537b52fbe243`  
		Last Modified: Thu, 11 Dec 2025 22:39:04 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1edb165698fca5e2b9ec08b838186e0cd115204b93c4bcb3f0f8621a3bd04af4`  
		Last Modified: Thu, 11 Dec 2025 22:39:04 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1582-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:83e55886ff238803b8ea3e3ff6e3c412243de0800b9b20b0d4a7019d962fcb9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7351347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1fa3f8a27fbd61995b29d6525c2bdf19517469631e5ae4ce6acc57225ebc948`

```dockerfile
```

-	Layers:
	-	`sha256:d66ac0e3154257b0441d71386884f78a97ee5626e889ce365d33289f846c7ebd`  
		Last Modified: Fri, 12 Dec 2025 01:43:57 GMT  
		Size: 7.3 MB (7333386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30f5b4be220915eeb8486cf1c6bc7542fba3ae889d6eb538fbdd8ad641494c1c`  
		Last Modified: Fri, 12 Dec 2025 01:43:58 GMT  
		Size: 18.0 KB (17961 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1582-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:89cc2b1a963e8a9c18888b80ba889d4337a8a7cea86e3863e4f0cdd59f993659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230921282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8020422862e9778d6f4354f57b2647cb7cd68197976aae2619b8698e233e26c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:34:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 22:34:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 22:34:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 22:34:22 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Mon, 08 Dec 2025 22:34:23 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 23:04:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 23:04:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 23:04:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 23:04:48 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 23:04:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c088128ea77bb5c706bb00930020ea2fba147060275f49c5a7be6b54af5ca7c8`  
		Last Modified: Mon, 08 Dec 2025 22:17:06 GMT  
		Size: 52.3 MB (52326977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbeeb5c6058bd793bb98336cf15f96291626b642ff5b9461a0723bb0f77fc9eb`  
		Last Modified: Mon, 08 Dec 2025 22:36:56 GMT  
		Size: 91.6 MB (91610764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225ca04b74cb712afb6f4f60e93778953db0573176c3db19c16456f7b42dc1b2`  
		Last Modified: Thu, 11 Dec 2025 23:05:44 GMT  
		Size: 87.0 MB (86982498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee38049e318f7a1fa1ae107e735ae98a54f02c82af1d879db99dcdb888e603d9`  
		Last Modified: Thu, 11 Dec 2025 23:05:38 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5404283e3ec6819e6b7c34ec49d56328e7d05655d4a991d47fdabe5d3d979310`  
		Last Modified: Thu, 11 Dec 2025 23:05:38 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1582-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:5812962d35a3ebcbd3223bf324d5d68b6d0c6502a92308472725bc534e0de9c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7351955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba391f879d6c4563807481f5a3dab7ff9bee6399f6773d61204ecdc6ce94a433`

```dockerfile
```

-	Layers:
	-	`sha256:a9ef44b45d86011920a10c6597e9a84fe25348dd468ada618eadae4cab21dfd9`  
		Last Modified: Fri, 12 Dec 2025 01:44:05 GMT  
		Size: 7.3 MB (7334102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2c1a94470368ed6012fa436759f21adb2162747ac1f21ebe5267c6ad518cb02`  
		Last Modified: Fri, 12 Dec 2025 01:44:06 GMT  
		Size: 17.9 KB (17853 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1582-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:736c2fcf82d62523c2e901b866eab04cbde9e20af76b0503698db7ecb8636b63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.3 MB (215304531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3084074daed1c5bb42d9d58987fc2d0c41ba5e28c2ef365895efcb71ef39522`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 01:33:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 01:33:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 01:33:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 01:33:39 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 09 Dec 2025 01:33:39 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:36:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:36:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:36:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:36:40 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:36:40 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f1896ba83f603ad81e0d8cb48b496e763b4b781a68efe11f1b6de9da929514ea`  
		Last Modified: Mon, 08 Dec 2025 22:15:09 GMT  
		Size: 47.1 MB (47137665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b901607e1053160f0c4a5999035c86877af07f0a5ab635c3250bef9051f1d4`  
		Last Modified: Tue, 09 Dec 2025 01:34:38 GMT  
		Size: 88.2 MB (88210741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e30a1036d0ed030372da6f3eb7a7b018736a8ef65d9784d66e0fd3cde27ca482`  
		Last Modified: Thu, 11 Dec 2025 22:37:20 GMT  
		Size: 80.0 MB (79955084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03112d6a53158a150fd0dee6570487b4fccd47611f366d3ac07931d4db00c614`  
		Last Modified: Thu, 11 Dec 2025 22:37:11 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf99543c1daac29209a37f2e187e0cfcd0559de2b71baf57ee4d709cfe72ee19`  
		Last Modified: Thu, 11 Dec 2025 22:37:11 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1582-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:26cb57a83fd7cf72f5dea2b4163ecde56127cc2bb50752cfa02af17645a1dd5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7339192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3f406cd0765eb7210a884146158b700f6857745da9d62c725dc13f95c99a8f`

```dockerfile
```

-	Layers:
	-	`sha256:6409e31fe7006d22279f201185003731303b6e5a4056776ee522eac883ba2e56`  
		Last Modified: Fri, 12 Dec 2025 01:44:12 GMT  
		Size: 7.3 MB (7321421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8fca3bbff23c9596a69fa17246b338cbc8093997145b424d39d7b83268dfa44`  
		Last Modified: Fri, 12 Dec 2025 01:44:13 GMT  
		Size: 17.8 KB (17771 bytes)  
		MIME: application/vnd.in-toto+json
