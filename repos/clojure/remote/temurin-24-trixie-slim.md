## `clojure:temurin-24-trixie-slim`

```console
$ docker pull clojure@sha256:d7df49e49d19807a4fe72f3fbf6b3d0ffe18c417f4bb68048d5ef937a97c8854
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-24-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:719ba2cbf09d78485564c18ba210162dee6ad7b6e1f765a40860964d80e7f4f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.4 MB (194382809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63c1dca7b2eb45f536f862dbfc889974637160e893d1e8b8a1ead3167f99eaee`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ced038dea045df288fe9bdbe03117ca66fe2a071217e196ac86ed07f965fe688`  
		Last Modified: Wed, 21 May 2025 22:27:59 GMT  
		Size: 29.8 MB (29755384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc86bd58cd0afaa65d917ef01e60beaa668dd73a51c501ee92ab52aae941769`  
		Last Modified: Tue, 03 Jun 2025 05:17:13 GMT  
		Size: 90.0 MB (89952019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4e614a08bce0ccf209f6b802d316829a68ef1c115de0f7e5d4068f03af2f55`  
		Last Modified: Tue, 03 Jun 2025 05:17:13 GMT  
		Size: 74.7 MB (74674366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a213fb040817b464b4810351f43205792bf486549d65f792c3aa7fd67bfcfd0e`  
		Last Modified: Tue, 03 Jun 2025 05:17:10 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7822c26f1852b6a41fe6e00141cfe5bfc897dadf0fe1beb0ea33c93a27028d8e`  
		Last Modified: Tue, 03 Jun 2025 05:17:10 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b775dfd45db603b1447af67085f062256ce3b94cb22f94bd8dc9e655000def16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5078559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:729edae7edc5d4106c312a789dc0efe0cd5ed253b81bc888f75885fb7298dfc7`

```dockerfile
```

-	Layers:
	-	`sha256:7b5df4fadc2b67810b8adc2dd8882eec4c1fc35ebd2837283467131a357cf3dc`  
		Last Modified: Tue, 03 Jun 2025 05:17:11 GMT  
		Size: 5.1 MB (5062711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bb0361fd519cb55397c98133151f3bdedf06d8422bd9a4f0e499599790315e4`  
		Last Modified: Tue, 03 Jun 2025 05:17:10 GMT  
		Size: 15.8 KB (15848 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:92afe7a6bdd9f837ff80b3212f484addb527d944137f67ec40b3a792d84ca06f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.9 MB (190858378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:332174daef054657c740586ac3bcd68070ff5928344eb0170881f7b99647a7d2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6098c2c9fa277c00ab580ce12bf64a9e1edf9e9139ba18ad85f3cc3063834aa6`  
		Last Modified: Wed, 21 May 2025 22:31:23 GMT  
		Size: 30.1 MB (30119455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:194de15ac003645cdf70d8dee3cb31319b90b7ad1a9df39b395a929d25343093`  
		Last Modified: Thu, 22 May 2025 08:43:09 GMT  
		Size: 89.1 MB (89091185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0abc6874f82cc1d70130c7a20667eca0a39bbecab32d8076da7d6b0f0d5c0d12`  
		Last Modified: Thu, 22 May 2025 08:47:33 GMT  
		Size: 71.6 MB (71646700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f606788707827c06831d8a3395b3821d1777de336662b1a3e8c4913893e12bd2`  
		Last Modified: Thu, 22 May 2025 08:47:31 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f4ebcf732d2e6547a5427e778a4e9589eecf0e6a3276029685049fe95ce506`  
		Last Modified: Thu, 22 May 2025 08:47:31 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1b9a88d464f1376624f21d30dfb6f16f2f1784cba0bcb0eaf7cc1f28142ce7eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5084443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e18af0cc252137ee388062744198354785eb06704cdddbe7909aab55390e12a2`

```dockerfile
```

-	Layers:
	-	`sha256:358e3f4c0e98fd6f5a2ee70007b3ae13527941bf97e8e2b62705a131b1096bf6`  
		Last Modified: Thu, 22 May 2025 08:47:32 GMT  
		Size: 5.1 MB (5068477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85df65c6d44b0786fa45f77c8e40001b7609828e11250f3717da53b9d9f12e6c`  
		Last Modified: Thu, 22 May 2025 08:47:31 GMT  
		Size: 16.0 KB (15966 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:6fc9b5ef984b9b062ee2cd5ab2c44554c9402c5a2575bee696021eb2f64d95fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.7 MB (200717950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf6f2d870195c8ee45b7a30a5154f4e3053f001146051c6458716a4ee542bd5a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:62eecea9deba6eaccef3e829ddec51f2c540dbbb668a68816c8ce3c4b8023d93`  
		Last Modified: Wed, 21 May 2025 22:32:27 GMT  
		Size: 33.6 MB (33580565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9fc8c5f0af333e2a3da968e470f55e3fcb8a33acef1d4ab1817407fa890745`  
		Last Modified: Thu, 22 May 2025 11:47:16 GMT  
		Size: 89.9 MB (89920247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5a1c07d8c0ac7f6b7ef8290605bdf80a4910f7a0bd5f9f05068bf175364a5f`  
		Last Modified: Thu, 22 May 2025 11:53:35 GMT  
		Size: 77.2 MB (77216095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328144d01b3f2b9f83a6b9985a425f5d17ce0d787493c2a04588fc0c024f1674`  
		Last Modified: Thu, 22 May 2025 11:53:32 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ac42d786bf18c3c12d968ace242125dc221c5948c5d3b51cf3e30abd1eb264`  
		Last Modified: Thu, 22 May 2025 11:53:32 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c8ce67fd6e3d6822ea142662029fc29a1caade7c523d7dd316a43a39333635a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5084276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:254712198e9276d4e93b1a0b6c19e7275602ff779dfa8f33110d34b910f4b232`

```dockerfile
```

-	Layers:
	-	`sha256:94aa89dee26955951eceeb61dd3ca22c8dc168bb55f98442ccfd84d1651b9b4e`  
		Last Modified: Thu, 22 May 2025 11:53:33 GMT  
		Size: 5.1 MB (5068380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cedbc8558a483ad4220c2d6ed8ee33fcec7d9e96634d34a8e6627ba9ec43b81a`  
		Last Modified: Thu, 22 May 2025 11:53:32 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:856d3c74f69fe2ac1c1b9b437dfccd1f4252cca2d3d55d1f06732baf9ff3ed54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.6 MB (186560818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c47a327eb9fc9cf26bda348e161d3d1f6c6b88c87398a2e52a21d456b9eae7ef`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f092cb6a76bde9a7b3c337ea49e8a7adec71062dc5df097be99d3975e92bc53a`  
		Last Modified: Wed, 21 May 2025 22:38:21 GMT  
		Size: 28.2 MB (28245354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48520921fd3b539bfda2058ded0f2724c28bfb9b6163fa249dc8bc5476454af`  
		Last Modified: Thu, 22 May 2025 00:47:54 GMT  
		Size: 87.6 MB (87622251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb01f386008f25824d379d78916736e434ba7395ac497aff23c8c422a08acf8`  
		Last Modified: Thu, 22 May 2025 01:02:39 GMT  
		Size: 70.7 MB (70692171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91af2cf5dfbf7d20b4406f96906fbe00ea99b0c3e3fe4c131c07fa227758d4a2`  
		Last Modified: Thu, 22 May 2025 01:02:29 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3e8dc9ffb729fc15987aaf2c99be64eb45ec353cb34addaad8c206984f5b73`  
		Last Modified: Thu, 22 May 2025 01:02:29 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:930faa655d5ef047e6c0f5fc956aaea7a3639454a662d3f65e5889910c508220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5068068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ff05bbb56a959417bd7de312efe197c127c8a467db482af934c9700caa335b`

```dockerfile
```

-	Layers:
	-	`sha256:f559236862ab67b89a7ab3b307f3d1eba16e1b4f96f5300b352732978a57e4e6`  
		Last Modified: Thu, 22 May 2025 01:02:30 GMT  
		Size: 5.1 MB (5052172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f755089ede0ae4f97ef173264060d867f297c631f6b32e7b61f5014f5bc4e8e7`  
		Last Modified: Thu, 22 May 2025 01:02:29 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:5924cf5ca7a06b7e9945bf133e1e6b8dd4511e0732d5286f5a96c139662be5b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187859406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:946e0024640d13ac84206c78a17cfc18b25df3ce7138710b614da9ac729e9453`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7cbda353d6047374e3da60bdf79ae89f8047840010f0964c87a8f2714e146106`  
		Last Modified: Wed, 21 May 2025 22:32:10 GMT  
		Size: 29.8 MB (29829620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23819e9a6f660656140faefb0803a95a0ac0d02661346d1fc445aafdafc5e949`  
		Last Modified: Thu, 22 May 2025 04:08:52 GMT  
		Size: 85.2 MB (85216727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9518227ace0764dd58e73b4e297f411e3a1ba7a1ab485923b4b224f526bb33`  
		Last Modified: Thu, 22 May 2025 04:12:49 GMT  
		Size: 72.8 MB (72812023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3ce6a769a3ab0178514428da5aaf9c4948519fc3e2eb30381fec32a3c4e2d3`  
		Last Modified: Thu, 22 May 2025 04:12:48 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2b3c6ec91b0fcf8d3755e98b53f7ca1e916524109ee227035ccfd6424d31a2`  
		Last Modified: Thu, 22 May 2025 04:12:48 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:847c489c86bfd6a603e99c78ee409c3b515c43fa077b60f7681c4a5a97fb8207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5077031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a817166117f80421e921a5f7ac2212ce198c234201eff80eb39fe42d8161f0`

```dockerfile
```

-	Layers:
	-	`sha256:a81574ae514c102415a4347f30bec073e90e3823276a207ec50aabc62443f016`  
		Last Modified: Thu, 22 May 2025 04:12:49 GMT  
		Size: 5.1 MB (5061183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ed49d808369425f8c7dd97b6e46d4f35537917b277ebd5be915037ab270fc5c`  
		Last Modified: Thu, 22 May 2025 04:12:48 GMT  
		Size: 15.8 KB (15848 bytes)  
		MIME: application/vnd.in-toto+json
