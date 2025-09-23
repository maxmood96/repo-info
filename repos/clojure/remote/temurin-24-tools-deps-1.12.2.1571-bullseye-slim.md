## `clojure:temurin-24-tools-deps-1.12.2.1571-bullseye-slim`

```console
$ docker pull clojure@sha256:33749e3d85a108ecd33cfc3a1f123ee2674944a03d558dfd7efd40b090167708
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-1.12.2.1571-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6f8fc60ee30b72abb259c93e95ba8447f4aef7afbb52845821e764fa09b5d56e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.4 MB (179386038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5204b738b196fe35456ba2f9b9eccb9d4d2d336ae832ea415a3498328630cebb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:456a3213e1b1f193dc759cd05f6f8422428b8c4bd45ef40fbf41ba43bdce8570`  
		Last Modified: Mon, 08 Sep 2025 21:12:48 GMT  
		Size: 30.3 MB (30256068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378e8261df17c7ab30e393de2091f489a94269cd59bd39468c1cd0e599721e3a`  
		Last Modified: Mon, 22 Sep 2025 23:47:19 GMT  
		Size: 90.0 MB (89975264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb80668b730a43bf116bb29011d4842c20cf8d1fe08ed98fca417487ec9be1a`  
		Last Modified: Mon, 22 Sep 2025 23:47:12 GMT  
		Size: 59.2 MB (59153661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c317a2c74c8e9760df48ae6fc905e6efe830d2de55b5e13f8af046d4672374`  
		Last Modified: Mon, 22 Sep 2025 23:47:07 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad531d879857367380428e481a4d86f363006a9de860257297b7d57d18afe96`  
		Last Modified: Mon, 22 Sep 2025 23:47:07 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.2.1571-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9c1d19653ea3c1ae6612e8a13d89efdec0f990f37085c3de57b9166aa7320a21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5274587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3553e73c3b8afe2e65d5a1689cfb2a8289dfde1c2a7d80a958379161c96080a8`

```dockerfile
```

-	Layers:
	-	`sha256:8e7dd51827faa29528c6505a4a5f0d5678eb140864e2d8462fbb98345ab95d47`  
		Last Modified: Tue, 23 Sep 2025 00:44:21 GMT  
		Size: 5.3 MB (5258715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ed1d490b14d2d787f6e77ea862edfe87b35a1a04adda99557e247ee585b9d52`  
		Last Modified: Tue, 23 Sep 2025 00:44:22 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.2.1571-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:22ca65ab76dd0f28ccbda17f974b0e31d677836fcbbeab4cfd9209f8d0fca005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.1 MB (177131212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a47e84cb04f3a5d85d79bf933824be04430cf6475c2fc92f1f195a66d0809e96`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8568e9af3ab25a29d98aac9a07896467a19253e72e5be0cf09cd3982ac4444d0`  
		Last Modified: Mon, 08 Sep 2025 21:15:52 GMT  
		Size: 28.8 MB (28750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d314bc0db3064aa8aa33a19e4f74bc7e81fb27a9ed86ecc4f2c851e8d492dc8`  
		Last Modified: Mon, 22 Sep 2025 22:21:10 GMT  
		Size: 89.1 MB (89092490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86470be59a53876a8e0e76966cc2c03c6e4872c40fabc0f24cfa36881a5dc63b`  
		Last Modified: Mon, 22 Sep 2025 22:21:05 GMT  
		Size: 59.3 MB (59287221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e22d70e1f867b4d209db3ffefe0f96650bcc8dbc22c24fe557ebe57f9777f0`  
		Last Modified: Mon, 22 Sep 2025 22:21:01 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fffbbcce946ffd4fc47da772113da6a41c0ecc048bbf9c2d20ca9c6508f4cef8`  
		Last Modified: Mon, 22 Sep 2025 22:21:01 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.2.1571-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0e715c26fa3a342e960beeee8917fb05e4fabadb2473672845ce0713e6892912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5280434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e9fff484d56e248c2c6087a38267a511de09cbf4e3dc5902ddeea8f9d58d4e9`

```dockerfile
```

-	Layers:
	-	`sha256:ccecf5555a8d4bafeb4e16e97dbd5d41e713d0bfd2a2d947e6eb63587b9ad6cf`  
		Last Modified: Tue, 23 Sep 2025 00:44:27 GMT  
		Size: 5.3 MB (5264444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64ebf267b10bf8c23afe50c47ec71d5a9c70631a653896104e9864290be957c5`  
		Last Modified: Tue, 23 Sep 2025 00:44:28 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json
