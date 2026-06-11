## `clojure:temurin-8-tools-deps-1.12.5.1654-bookworm-slim`

```console
$ docker pull clojure@sha256:1ce14896d5ae9c3ce517d7fd70446fb15970f2b2804a69f38f1c00d1c864b05c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.5.1654-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4a2748beda28f81b9bb7b1a7f8941ff82de583e11660d54b8c187e09e3fd59e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150079516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bdd8e2997fd06ec6039e6c34881b4cb5fdfb81b3d10480be161ac4cb6c8a446`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:16:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:16:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:16:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:16:14 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:16:14 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:16:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:16:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:16:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab23b9cc7573c5b95e2593921c8d7e4a6b179906149c81aeaa20aedad83b758`  
		Last Modified: Thu, 11 Jun 2026 01:16:43 GMT  
		Size: 55.2 MB (55198723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b459e26bf61af160614ed28b96fd755f508d24e25ec2ba9492f859e96c9d0cd`  
		Last Modified: Thu, 11 Jun 2026 01:16:43 GMT  
		Size: 66.6 MB (66642525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d7ee6dd5305e656e14961beff2e6680c931419d85f4ea21d2274cb39962f0b`  
		Last Modified: Thu, 11 Jun 2026 01:16:40 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.5.1654-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4539c5c4e8dcfad730113db3547711e21ede92ad6d7de4f652313f09b33e3744
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5248761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5a17d5a65077f3e3558d86badc902357150160079ea0d79de9a3f976672bda2`

```dockerfile
```

-	Layers:
	-	`sha256:ec94eedaee8ccf06977170759682307486186264ae0ec9680cf015841d9ebafa`  
		Last Modified: Thu, 11 Jun 2026 01:16:39 GMT  
		Size: 5.2 MB (5234359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a32cf0c318227ae36adc4f20b736052bd461b708a5a1816c21a3afe73371c60`  
		Last Modified: Thu, 11 Jun 2026 01:16:39 GMT  
		Size: 14.4 KB (14402 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.5.1654-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0d7492459a531f49ee44fd636937e516be1328e8eed4e3fcd16a019edd46c1ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.0 MB (149039113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25ea5f8083eaa8886777b844678fbfcf1df7eeb7969fb534dbe9b47cf4ee96bd`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:20:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:20:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:20:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:20:27 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:20:27 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:20:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:20:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:20:42 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d33573b4bd7f65ddbe77f354f5becad0f890189a7e0268fda3edea1ec529ed0`  
		Last Modified: Thu, 11 Jun 2026 01:20:59 GMT  
		Size: 54.3 MB (54272927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62de3bab70308cba723b0946f7b6258e916a491f4f6e2882d390e0f819a22040`  
		Last Modified: Thu, 11 Jun 2026 01:20:59 GMT  
		Size: 66.6 MB (66643235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e18d213ffab8fd8f4a801388b1bdc11cb6e24aa3f7b0c09e47c5a5092259f70`  
		Last Modified: Thu, 11 Jun 2026 01:20:57 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.5.1654-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4255f6f5722437530b45a4f08aa8975b331bdaabd1c72f5381912c0014fcb1df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:242bf8b75f126ad225ca9c09394c7bf0872d338fc747e58926d4c0f7484e2fce`

```dockerfile
```

-	Layers:
	-	`sha256:6144cc37d268727b5ab933e7ecf0fecf11edd5c399b6f5f6c43fc6332e937345`  
		Last Modified: Thu, 11 Jun 2026 01:20:57 GMT  
		Size: 5.2 MB (5240820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a5a0bb72455e22d95a6d7d32ba960c2909f345923c6b5b7b3ae9df277631bf3`  
		Last Modified: Thu, 11 Jun 2026 01:20:57 GMT  
		Size: 14.5 KB (14519 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.5.1654-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:5cbdc3912f99b9782ebeb20e063dbd496596b20b25481043bbd7c39a94bb7b79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157227895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61b104fd030ac3f84a311409f5e2feb179a6223637a1690b021da7fb8a835d1c`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 09:16:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 09:16:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 09:16:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 09:16:30 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 09:16:32 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 09:19:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 09:19:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 09:19:38 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:23f7cdee3ef2598b081c2b848fee95730a7ab2b1cc5b726c72dcb8c2fe3632f7`  
		Last Modified: Thu, 11 Jun 2026 00:21:33 GMT  
		Size: 32.1 MB (32081941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39defc5bfb0ff6e9bb6148e9d9a77a4f16f9e97365a1c3b822d6654a2dbc185d`  
		Last Modified: Thu, 11 Jun 2026 09:17:33 GMT  
		Size: 52.7 MB (52669152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e16ef737627aa000aa77d315f6740194ef02be1c644a1066ec6202e67f1c2aa9`  
		Last Modified: Thu, 11 Jun 2026 09:20:11 GMT  
		Size: 72.5 MB (72476159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ebfce777623b9743add68d0cb257aa7fa746029ba4d719cffb4e5cabe55a47`  
		Last Modified: Thu, 11 Jun 2026 09:20:08 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.5.1654-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:01100fca28976728e33cee2b04355e51dc8393dc6b0f80e81fc95b713ff669d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5254562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ca81df67d2a526c2b79580df9ab4667bd5e087f86720e3af1f67e3cfc66f78d`

```dockerfile
```

-	Layers:
	-	`sha256:7eb27fa8e1e49532dba331f4e7521fd0bcf41ea3afbb741c60f2570b966db403`  
		Last Modified: Thu, 11 Jun 2026 09:20:08 GMT  
		Size: 5.2 MB (5240112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd9e1166414863b982ba217e0111001ae31f2bfae7f0d3a855bee105b01fac44`  
		Last Modified: Thu, 11 Jun 2026 09:20:07 GMT  
		Size: 14.4 KB (14450 bytes)  
		MIME: application/vnd.in-toto+json
