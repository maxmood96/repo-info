## `clojure:temurin-8-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:886faa2b2c69c0b12d5c6d7461bdef14b1e5f0b89a763ae4a4b006f6e2425f65
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:23b6c4f20f468236d0c8cf23f2fa126940aa430444dd900d4a6235bc5a7b8b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152639428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aee26f0ee02ca448665a4d2a3f0b8c090b73ba9a929157a265c328bef6f57ec`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 01:43:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:43:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:43:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:43:45 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 01:43:45 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:44:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 01:44:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 01:44:00 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abdc9643277e6ed13419a348061ce2996e8c94013db7aa705c046e9b1140285c`  
		Last Modified: Fri, 16 Jan 2026 01:44:32 GMT  
		Size: 54.7 MB (54733367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c570d2f9d7a2d6c755d909b908d4946b514703eeee9fdd39e7836e256ef179`  
		Last Modified: Fri, 16 Jan 2026 01:44:34 GMT  
		Size: 69.7 MB (69676845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b9708a51f894033255f10c00c227739d429d39ba07be8c52aa8ffacb057660`  
		Last Modified: Fri, 16 Jan 2026 01:44:26 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0edacba3d8318f6b9a6047366fe4a35faa370970951a3b4ace5d8f96dab8547c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f3f60330d1b0a7aa4386d41445514350ff4fa07198c6a89fbbb13ec98d5e664`

```dockerfile
```

-	Layers:
	-	`sha256:1c9c99efd866a66017bcf358a7834293c77ba5155892a1840ee8d1217aedd5c7`  
		Last Modified: Fri, 16 Jan 2026 04:52:14 GMT  
		Size: 5.2 MB (5235008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63846143833c839b3337067269fb182cff63cfb071e35e984a33bd7102a8b6d4`  
		Last Modified: Fri, 16 Jan 2026 01:44:15 GMT  
		Size: 14.2 KB (14248 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:167a7d2880629035ff5c6efb36bd380e3682978ec3d4b4b050169f5be3c4f3de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151595919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbfedd044d03ce0c9ad4de0bdde190200ce34b279e14e99994b04a0d9e723e50`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 01:47:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:47:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:47:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:47:36 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 01:47:36 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:47:51 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 01:47:51 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 01:47:51 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:09 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797a0b2a63a75a1edb649403975310947b3b436659b1300d566fe31e72b86b89`  
		Last Modified: Fri, 16 Jan 2026 01:48:22 GMT  
		Size: 53.8 MB (53815007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64438b4db26db76103d8cfe4953111d5a75caa897ddd97be56943d8a542b434`  
		Last Modified: Fri, 16 Jan 2026 01:48:21 GMT  
		Size: 69.7 MB (69672378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec19d40cbae45403aa419b7100640c2d405cd68f9c6e26ec8eb9d7035f5fc90`  
		Last Modified: Fri, 16 Jan 2026 01:48:15 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b4a5f39e3bd78f555addf9a6ff0e614211eff55fe68a65443633b11f55fa8c8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6ec7875cc8ad7819b09ed357891b76095706bc952c099dc7d46895e103091b7`

```dockerfile
```

-	Layers:
	-	`sha256:cedb0739c7e8bb9fe3d58815aeae25664f710cb8d22cc8bb1c7a062433fed230`  
		Last Modified: Fri, 16 Jan 2026 01:48:06 GMT  
		Size: 5.2 MB (5241467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e5ddbf7fec377b0ca60eac9285cfea0e3ee1dc0c05d7d0cdfdb9f6d5237bd97`  
		Last Modified: Fri, 16 Jan 2026 04:52:21 GMT  
		Size: 14.4 KB (14366 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:4c382033f830e769052e2d4b5c5dfafb564c29007306a90e2536a9e31d808b16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.8 MB (159756993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3008fe519d47cd9aaac436c836f054bce4c161439d3ac3673e123eb66721597c`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 02:46:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 02:46:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 02:46:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 02:46:30 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 02:46:31 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 02:52:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 02:52:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 02:52:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:cf92d3bf0add4f20720c3232cd336a7f7f50627989684b748675db0b2f2ce746`  
		Last Modified: Tue, 13 Jan 2026 23:17:24 GMT  
		Size: 32.1 MB (32068709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d225176ea3089fa66647c02eab51b7d4ae39e81703846fea6bddaaa39e73be6`  
		Last Modified: Fri, 16 Jan 2026 02:47:58 GMT  
		Size: 52.2 MB (52175159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13e913398727186f827afcf8895c4ac690180d5d5c7a3eda09d4c2bb3fd718d`  
		Last Modified: Fri, 16 Jan 2026 02:53:24 GMT  
		Size: 75.5 MB (75512478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea8d42fdc5a780f0ec35a24b6a647430475262dc5c7eff23f7cb7b89bfd9a76`  
		Last Modified: Fri, 16 Jan 2026 02:53:18 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c566af75a1ea1fc69794b61d93815821c6ceec2a24fe422ef4315586e0e4b9c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36afc25abfbf05f142b0f17855557e325b40ec085b15af5b89950908a5fb02e7`

```dockerfile
```

-	Layers:
	-	`sha256:f9b85dbc6aa393c33bc0c62710ea649303df0020746b4a639af34edc257d7104`  
		Last Modified: Fri, 16 Jan 2026 02:53:11 GMT  
		Size: 5.2 MB (5240759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a840daf6151ce4ed1461ce3b20f971d2fdc9bfb1872dc62f52192fe2cd411e4e`  
		Last Modified: Fri, 16 Jan 2026 04:52:27 GMT  
		Size: 14.3 KB (14296 bytes)  
		MIME: application/vnd.in-toto+json
