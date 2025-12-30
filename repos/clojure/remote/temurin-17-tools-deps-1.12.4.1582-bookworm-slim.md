## `clojure:temurin-17-tools-deps-1.12.4.1582-bookworm-slim`

```console
$ docker pull clojure@sha256:5fabcb085dce12355370146b2dd90e0e42b871356686cb77fe3590eac913d9d3
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

### `clojure:temurin-17-tools-deps-1.12.4.1582-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a8c7ea8b66fc21e3875cbc15d4affd7a8d2726a23503188a230139a8ecc6fc32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.8 MB (242754600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d86e3ab73c5b5a9a0fbf3fcf71ebc75684f64ffbeee16ec4420f5c263b441f59`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:59:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 00:59:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 00:59:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:59:50 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 00:59:50 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:00:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 01:00:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 01:00:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:00:05 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:00:05 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e2577b2f9d47c19dae5afae9c3905208bd6085fc36168d93e532fd512eb775`  
		Last Modified: Tue, 30 Dec 2025 01:14:18 GMT  
		Size: 144.8 MB (144847979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c04f5dd5159eb88e3998b07f36b2e6b8aac593de8accdc8f94c2ee1cedbd18`  
		Last Modified: Tue, 30 Dec 2025 01:00:41 GMT  
		Size: 69.7 MB (69677152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:472f893b32a541236e60ecc697091addacfdc4ddb7aef32ced800bc1494cadea`  
		Last Modified: Tue, 30 Dec 2025 01:00:35 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53c726db257073101665f85b6342f1ab3f0afbc8ddc4eb26f1b336123585f97`  
		Last Modified: Tue, 30 Dec 2025 01:00:35 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1582-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a873ec83f183e5c905e797c0018278fd6504510412e05f46b03ef886519f59e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5129226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c195e5e95986ebdfa172cc318fca438c43923b5cdc502fcee88ef3f1b53bbed`

```dockerfile
```

-	Layers:
	-	`sha256:8c80ca9b50d1d354c5ca56f8490e608eb52447c5369ff1ae6ad5ad27777d0d4f`  
		Last Modified: Tue, 30 Dec 2025 04:39:34 GMT  
		Size: 5.1 MB (5113390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a9aec53f9baf630573b3e23be199056d4ca732da4e47ee130c2e541d0368980`  
		Last Modified: Tue, 30 Dec 2025 04:39:35 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1582-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:762c18fd3dd4058d82ea46ee29c1ae60182f22745124c036f2bfcd0d40e95f3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.3 MB (241341667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0481f2c9c49f53639f04bf6c30af26181051751247275555c2c3a5314506b7cf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 01:00:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:00:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:00:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:00:29 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 01:00:29 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:00:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 01:00:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 01:00:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:00:43 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:00:43 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b41cc7c8926ee9fdfff83cc3ddc9854748e19b8de6bbc1270add8355094c371`  
		Last Modified: Tue, 30 Dec 2025 01:01:39 GMT  
		Size: 143.7 MB (143679909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3100e3bef010e7ad9613969cfb5f30f5ec37e83d326d8b295a8a94041197fb56`  
		Last Modified: Tue, 30 Dec 2025 01:01:16 GMT  
		Size: 69.6 MB (69558510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e11e893881d22ce3f75a24330d2ec85395906d92d47bb663f5b6d10e6a16965`  
		Last Modified: Tue, 30 Dec 2025 01:01:11 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da5ab2cb0148e5cf0047f16eb5d0f7d89739a5b4619f0026ac596c4b9f191e54`  
		Last Modified: Tue, 30 Dec 2025 01:01:11 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1582-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:58e47efb06623cfd83f5a0180b73c55430b39f8427f1bacb49cb3bb73a85fc8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5135105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fc368365cb9b835dcfcb00c15f0627220b55c4f573ecdd59c72458e945fe3b0`

```dockerfile
```

-	Layers:
	-	`sha256:0805665381ebe6329c8069f46fafc0b0b7b5bec9d098fb4ac5cd92fad631ab86`  
		Last Modified: Tue, 30 Dec 2025 04:39:39 GMT  
		Size: 5.1 MB (5119151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe4531cb08a73a740aa064c259074fec47c58a435871a9d9946d1feba7fbc25d`  
		Last Modified: Tue, 30 Dec 2025 04:39:40 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1582-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:c17cab168fce5408036c249a648c58e93c0c5e0a9048cd6d22a3fa570146e589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.1 MB (252105247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:194640bcbd04bc1e5fd26b7d1494684cef168385fcd6ba7ec126333f1f2dd7a1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 05:17:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 05:17:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 05:17:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 05:17:49 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 05:17:50 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 05:20:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 05:20:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 05:20:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 05:20:17 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 05:20:17 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b7648f01f6858fc79caf032b4b9ed2f7e43e57f4621dc8cb36e84eb86399065b`  
		Last Modified: Tue, 30 Dec 2025 01:48:36 GMT  
		Size: 32.1 MB (32068844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c662a1580b47c492cf3baff3cc57fac4e48d81084d9a9ed82cf007a60ca93b2`  
		Last Modified: Tue, 30 Dec 2025 05:19:12 GMT  
		Size: 144.5 MB (144525257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff4709ba829cd9c55a21fe3f91d66db8013aa45695d961458945599cf081333`  
		Last Modified: Tue, 30 Dec 2025 05:21:09 GMT  
		Size: 75.5 MB (75510105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ea468b25f0839bd9228f493169609a5a0ce91beb643748f72ad42c5375c8c5`  
		Last Modified: Tue, 30 Dec 2025 05:21:04 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658ee058d9ff05f302d8a06534f6465075e70696cf24a32268ee41e925f7adc3`  
		Last Modified: Tue, 30 Dec 2025 05:21:04 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1582-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1cc4b63652e80e7277813ba4a2beff1460aafe383108cec114370f3b0f06d05f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5134432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8014d5077e725ca061a647218a298f8c7f71590fb749c3f32145e42b56175e31`

```dockerfile
```

-	Layers:
	-	`sha256:cb72cb025f892153ea19523a08e045e039b589b9d7a4dacd747333f753f3c4a1`  
		Last Modified: Tue, 30 Dec 2025 07:36:14 GMT  
		Size: 5.1 MB (5118548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c03296bcf7a4581b9424a3fffa082e42277f42113784191b394c5a2bbbcf093`  
		Last Modified: Tue, 30 Dec 2025 07:36:15 GMT  
		Size: 15.9 KB (15884 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1582-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:d1cb7154be7afc1f754a70b3783dbbef1a9f5ddf4e5412a7b6baee65f6f115fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230232092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ae341767ed1f01a43abfed6fa1bdd491099aa5971c5ca6ec42b8fb9c394a78`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 02:02:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 02:02:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 02:02:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 02:02:26 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 02:02:26 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 02:03:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 02:03:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 02:03:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 02:03:57 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 02:03:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:908a8b9619550bcbaa302a1a1375bffd68fb4bab6330d7a965b0b9e3f3896a0a`  
		Last Modified: Mon, 29 Dec 2025 22:25:40 GMT  
		Size: 26.9 MB (26884397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c5ac6ff88101ab235cdce6d5bf5fbe508e81392d7c56a55438aa9880ee68ec`  
		Last Modified: Tue, 30 Dec 2025 02:03:25 GMT  
		Size: 134.9 MB (134859036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b65844c990eb3eb1105d87ea104815df84b9b32a6bce20870a0e05b393d4e7`  
		Last Modified: Tue, 30 Dec 2025 02:04:29 GMT  
		Size: 68.5 MB (68487617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7888ec9335d79ecd3854620dbffe645463892017479eae663b3695c8683413a`  
		Last Modified: Tue, 30 Dec 2025 02:04:24 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ac72798b55e605dc9d7877594601a87e4aba2d60e4e172fde5241fee0c2836`  
		Last Modified: Tue, 30 Dec 2025 02:04:25 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1582-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0f531fd3165393e802f68197586340d0098c9b8f652e678e7d6ab216e1f187e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5119746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a9ecee6bce9041b732559239b8239481d621933cbc98ad99b9e28932c07970`

```dockerfile
```

-	Layers:
	-	`sha256:8b7fe638a97efd19cddcdbbb6dac0256e80c3187e7138efb045d8e91a21da825`  
		Last Modified: Tue, 30 Dec 2025 04:39:49 GMT  
		Size: 5.1 MB (5104711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:636ed87deab80a802064d5c5905292738b43508756774d4ca538590522436ef6`  
		Last Modified: Tue, 30 Dec 2025 04:39:50 GMT  
		Size: 15.0 KB (15035 bytes)  
		MIME: application/vnd.in-toto+json
