## `clojure:tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:e4a736c633e70aecdd44a75ee381dbfbc8eba0383feb387098fbef5d768d9246
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

### `clojure:tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3b38923374c717cf56b0e6d857b7a6eb0424ce13590a6d2203be535e40788214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.6 MB (255616179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65a96a72aaee630881a85fad35f0bac3d3f243df2cf66b1d787d3a1756b887c5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d54afe5fc7c56f3d5c8ac3d6d255e131506d26a56377393d6c3fc215f714c8`  
		Last Modified: Mon, 18 Aug 2025 19:44:15 GMT  
		Size: 157.8 MB (157804778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35aced6e37a3cfc0e6537465fda769417599fd9a145805e6295483e33275a42`  
		Last Modified: Mon, 18 Aug 2025 19:44:13 GMT  
		Size: 69.6 MB (69580103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d399e3dc1e8c510d0a21c9c5b84740132f22f845454d02a1bf8710d019188bc`  
		Last Modified: Mon, 18 Aug 2025 19:44:10 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f15c9c99ecaf74851d8253146524cdf432ddac37bee2589361a91ea12e1e08`  
		Last Modified: Mon, 18 Aug 2025 19:44:10 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e4e59cfd00043478db2f46d8acdad32cb9ecb1f996df9de3a86fbca5139da77a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5131644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0348f495e1b96628d0256a2cf1665984fa39d4ac1e0c1af72069dc296a2dbb45`

```dockerfile
```

-	Layers:
	-	`sha256:01e693a3948c7f7fea908b00cc5d7f74fb63ae242453b35a8ecfd812046926b0`  
		Last Modified: Mon, 18 Aug 2025 18:40:04 GMT  
		Size: 5.1 MB (5115071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16ea7bd3e0f6b6440f6bd16ab8a6d8947f7bc09911ccf1cc4d876478b26029ef`  
		Last Modified: Mon, 18 Aug 2025 18:40:05 GMT  
		Size: 16.6 KB (16573 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ee60ec8a62f085863930cb6b84821aefb42540c30a5174b8fdcc972f472f1859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.6 MB (253617019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6125de88dad35864254aad433866b76f94763d99a1e2a10e00eca35cbdcbee2a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf7991a92c7ee87da171852566b076064998d9091210c9e1f68f8874a4a0f1ef`  
		Last Modified: Mon, 18 Aug 2025 20:51:19 GMT  
		Size: 156.1 MB (156081253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b11ec4d6865b8bd742403117e52fa4b4568049956ee7b46cc984f0e4aadc88e`  
		Last Modified: Mon, 18 Aug 2025 20:51:16 GMT  
		Size: 69.5 MB (69452722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8aa29b11153b5c6fa67d4c9246c54cbd47f28145cbea4624f221c101d5042a9`  
		Last Modified: Mon, 18 Aug 2025 17:16:48 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0abd77a707c6a4797c6b59a06a9b6044a528686eb78ae7f76dfd63e1f050f8ba`  
		Last Modified: Mon, 18 Aug 2025 17:16:48 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dd86cc1bd122fa7111867d1cfa49afa92949c22049791940eab9256b1dbd05fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:418f8603e80bcba5068a92d305ba510a8ee451201df60ffe6a1309a1c9942387`

```dockerfile
```

-	Layers:
	-	`sha256:4536e2dd97cf18e20dd0402dab60bd3046306d4dd9045ea51687dfe6b7d5a792`  
		Last Modified: Mon, 18 Aug 2025 18:40:11 GMT  
		Size: 5.1 MB (5120856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:144f3f5ce5f5b3f246ba9508da8d8dc2d745ca3a425b20fe6be51a7d66e8ba9e`  
		Last Modified: Mon, 18 Aug 2025 18:40:12 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:c9c9aef3fb59ca549448101067f4a3ff3da53794bfb5de1a04a0043a2af4b842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.4 MB (265444668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfaa9c39a56fcb853845d29a09b5bf038912e917acd896843661ad2db733e16f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f159f526f8a9c3649fee57d0df8248d04aeb1f957c2fcd7d35d584b2f74bdf`  
		Last Modified: Tue, 19 Aug 2025 18:06:25 GMT  
		Size: 158.0 MB (157963439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e8a316ff386438bea7db2703240e600588816fc10e30591d522bf8ab520aa2`  
		Last Modified: Mon, 18 Aug 2025 17:27:58 GMT  
		Size: 75.4 MB (75406766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e2d3c02bcc1f65699ce97030616bc4a16bb2a2ca9baee40c9ecec1a54576b7`  
		Last Modified: Mon, 18 Aug 2025 17:27:49 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca79fe52215be3d2995e531dc6b9c148d335ee94b1260f650ada4253cc129a5`  
		Last Modified: Mon, 18 Aug 2025 17:27:49 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:40a5e970b0efd3cd852200c8c4e02f95e6d6eb2372b45c2717467a0db94a74c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5136876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:936dfc8728e055203414e23be8f09a42bd5f4b2c3887a8e835823a92fbac8dcc`

```dockerfile
```

-	Layers:
	-	`sha256:f5024f52b78db729e1b36ddb54524415ab0c173099825067b5f586ce8274d1cf`  
		Last Modified: Mon, 18 Aug 2025 18:40:17 GMT  
		Size: 5.1 MB (5120241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10e501bd5c3ca25dd9bfb6501e68210822c532fd8715b045ba66dcd9cc290a8e`  
		Last Modified: Mon, 18 Aug 2025 18:40:18 GMT  
		Size: 16.6 KB (16635 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:125f3f26c216ad19f8bc0f45ba030ab1f6f28c57d042208ac66c1a37e67ea5c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.3 MB (242303959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93673982fa6d52bc9aa17a16e8a606d7b148f0fdc1a3627476c26dd82138ffbc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f1cd2e643b85f38b855ab774d4606497ec4c96716612b07695839e1f191597`  
		Last Modified: Tue, 19 Aug 2025 18:06:08 GMT  
		Size: 147.0 MB (147026954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b68b6c5d3ca276eb037bf2837b8aadc76425b02d267f15248a559a539bd5dd`  
		Last Modified: Mon, 18 Aug 2025 17:51:59 GMT  
		Size: 68.4 MB (68388126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff56a384e39296cd36ec6e33a5b063320366d7b98be8abeba2407d6af881765`  
		Last Modified: Mon, 18 Aug 2025 17:51:42 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35607ae545ba54cba461c96dd15383b7a5d95703528bd296ac551f17edb34f72`  
		Last Modified: Mon, 18 Aug 2025 17:51:42 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:539d4276a1cdcf2cc5b7679513959b77b32277418b2880ff673bad8fa72e2acb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5122966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10b881abdc03b18131243b7b5173f008b386a55e13967b836988e966f4c2cc5d`

```dockerfile
```

-	Layers:
	-	`sha256:f5f9323ac6ef19939d7d818ee94b520373802ba1dbb2f74229c9a751a9ce0a5b`  
		Last Modified: Mon, 18 Aug 2025 18:40:23 GMT  
		Size: 5.1 MB (5106392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c57f51533344c26f4d4505ca5eb5aaa979ed26df268b990f595e9ef6ee9d6d22`  
		Last Modified: Mon, 18 Aug 2025 18:40:24 GMT  
		Size: 16.6 KB (16574 bytes)  
		MIME: application/vnd.in-toto+json
