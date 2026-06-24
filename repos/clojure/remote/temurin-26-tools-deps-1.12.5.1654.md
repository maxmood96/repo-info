## `clojure:temurin-26-tools-deps-1.12.5.1654`

```console
$ docker pull clojure@sha256:f36e75ddbd4f56b80d2b702d890f1666c47689775f8d665d65fbea254fe4ad2d
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

### `clojure:temurin-26-tools-deps-1.12.5.1654` - linux; amd64

```console
$ docker pull clojure@sha256:1bf6b12a2f0b7da6d5404cf830ae9d69cd4cb3defebcfdc5f262875551f14b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.2 MB (221152750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b04bca72daf8f0948e1859694ce762714d0763d1dd9e38e3e4da2c308a614fbd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:22:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:22:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:22:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:22:44 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:22:44 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:22:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:22:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:22:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:22:58 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:22:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:425befdf76e52426879d2abe42093a00dca59a893e7b4fa2a7679b0180b71d4b`  
		Last Modified: Wed, 24 Jun 2026 00:27:40 GMT  
		Size: 48.5 MB (48502210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beef06c0aa2f92c406529c97a3d6f77491765104401382ecd4c95b4f543902da`  
		Last Modified: Wed, 24 Jun 2026 02:23:20 GMT  
		Size: 94.5 MB (94524361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dcd2a69bc96eadb8950b5a1199522ec3c4d95c5ef0638d9c7fa9db509ba697f`  
		Last Modified: Wed, 24 Jun 2026 02:23:21 GMT  
		Size: 78.1 MB (78125135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a4c6a0a7d3765fb0ab1965346b63b38250b3743eddd1e83b65dd748a14d547`  
		Last Modified: Wed, 24 Jun 2026 02:23:17 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f45714faf26fa0db340700d014f5debf3c861318118048de6eb9999d5ec65eb5`  
		Last Modified: Wed, 24 Jun 2026 02:23:17 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1654` - unknown; unknown

```console
$ docker pull clojure@sha256:f80d132d41e7c69bbb7a8849b4fb917024e1f21421998459b5ae4c82dfb82e94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7358318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95c9d8d89b642726d1f792ff7db7f22dbbc4977474445b336e0ec57c00ef0cce`

```dockerfile
```

-	Layers:
	-	`sha256:55146b73ff305655188c8c896b340891dacba198b4182aa2169e8d0cf1c26645`  
		Last Modified: Wed, 24 Jun 2026 02:23:17 GMT  
		Size: 7.3 MB (7341709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d0b5e61989e9436b1739f2865c61bed480d23e3f6920cd78db74db6d24b1074`  
		Last Modified: Wed, 24 Jun 2026 02:23:17 GMT  
		Size: 16.6 KB (16609 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.5.1654` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cf367e5b27a7e02cc759371ac077f29157a1ba7bbe5404611a566c1d4968d50e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 MB (220023954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:248d1f01f16e09e7141b70da99ebf6c26bb10a79a0cfccec3ec2c778209f460b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:29:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:29:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:29:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:29:29 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:29:29 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:29:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:29:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:29:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:29:43 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:29:43 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0fb1189398e2e4b474d43aac6502510d0da0318e70137a377c21087f198814db`  
		Last Modified: Wed, 24 Jun 2026 00:27:19 GMT  
		Size: 48.4 MB (48389201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0734b3e19ec675ed9b31c44604136275a29c3275dac35289d9baa0e79f33b535`  
		Last Modified: Wed, 24 Jun 2026 02:30:06 GMT  
		Size: 93.5 MB (93504323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:317d9b9d5adb12b3ccb7d7d24fb621680ee73e03bce75bc9938e2e1a29a3dc00`  
		Last Modified: Wed, 24 Jun 2026 02:30:05 GMT  
		Size: 78.1 MB (78129391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cdfe61a32e54f9571b85299b4f56962dc88c6d948c87b2aca77924274c04c00`  
		Last Modified: Wed, 24 Jun 2026 02:30:02 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:761c628af8745ca215234a21198952cc36a1813ccf1ac989af2670e77594ecd6`  
		Last Modified: Wed, 24 Jun 2026 02:30:02 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1654` - unknown; unknown

```console
$ docker pull clojure@sha256:f24ef162e63f9185e5c1ffa92ce0f4e615ba2ec909dd93b1d8da47fe4c468aaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7364244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ae9b8dbbdd1b6e2aa50847a1ba2911b98b2af58850cb014faecca5d524ba96`

```dockerfile
```

-	Layers:
	-	`sha256:2b59bbe270af663d65c1ea5836a3f8d56865e9a02e84553fa3df6da8a4fafd89`  
		Last Modified: Wed, 24 Jun 2026 02:30:03 GMT  
		Size: 7.3 MB (7347493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1a7374345cfe5bf6599f4f356dd9688720d9c4d97acbd3cb96ad1521c431c81`  
		Last Modified: Wed, 24 Jun 2026 02:30:02 GMT  
		Size: 16.8 KB (16751 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.5.1654` - linux; ppc64le

```console
$ docker pull clojure@sha256:43a332b216e157b2591046a77442dc9cf6e1134fc8ae620e3aa4546176920dcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230208611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44121cc40526473e59b690df3eed21e48484ba55de1ba43c53057c5f66c9bddc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 08:30:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 08:30:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 08:30:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 08:30:47 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 08:30:48 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 08:38:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 08:38:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 08:38:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 08:38:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 08:38:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:55b0e891f4e8dc14bf4bc7e853254fcf1f3ba5a8e8e3c07c21e7dd5bd6d87882`  
		Last Modified: Wed, 24 Jun 2026 00:27:34 GMT  
		Size: 52.3 MB (52346847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3911fb4790a8a823332a0489f588cce29b003efdc940702ba27434da3da607`  
		Last Modified: Wed, 24 Jun 2026 08:34:16 GMT  
		Size: 93.9 MB (93902051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbea5cdba79c2809647b316f0c9ed88db4163105d57c01b64ffbf2e1618e2f93`  
		Last Modified: Wed, 24 Jun 2026 08:39:22 GMT  
		Size: 84.0 MB (83958670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:762e4313fcbf0cc55d87269f82850c8e81dd7d4a75c2665ba9c2036f25512bc5`  
		Last Modified: Wed, 24 Jun 2026 08:39:19 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d37b83998c9e0f9ed8684be7a68cc71e35f41dcdcb83a51cd7bd6135d008dc36`  
		Last Modified: Wed, 24 Jun 2026 08:39:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1654` - unknown; unknown

```console
$ docker pull clojure@sha256:384c8ff705431aa169e08446a797ff5522f1d597cb54d0ea23ff47e44edbab6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7347542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4342d6862a31324ab7dca17211c16f4bc24fb995d39d4013bcf32096c781d09`

```dockerfile
```

-	Layers:
	-	`sha256:8c4b3e96e6467ef95c862f02bf786ee9a4d4a5cd9ba10ac1441ac543ff952b9a`  
		Last Modified: Wed, 24 Jun 2026 08:39:20 GMT  
		Size: 7.3 MB (7330873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97ecd1733833c3d15db6026c0442b3743fa80eee459ba19d54ac232c95cc1055`  
		Last Modified: Wed, 24 Jun 2026 08:39:19 GMT  
		Size: 16.7 KB (16669 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.5.1654` - linux; s390x

```console
$ docker pull clojure@sha256:40bc7091bb0bcf595239d6f5500286ccfd3618b11718dd7ce702d70f95af8c16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.6 MB (214628773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7773c295870fee069822cd1f78b2e622342612121f73948dc7cf204f9ea7d6d4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 04:19:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:19:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:19:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:19:34 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 04:19:34 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 04:21:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 04:21:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 04:21:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 04:21:34 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 04:21:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:bdd2e9d83d68023204331dd445067114dbd3500d2d496368624fa7ef81743d4a`  
		Last Modified: Wed, 24 Jun 2026 00:27:09 GMT  
		Size: 47.2 MB (47161675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec0a7bf706ef5f3dfc06370f280188b307fdbd1df1db2cee1e3b1703d342699`  
		Last Modified: Wed, 24 Jun 2026 04:21:03 GMT  
		Size: 90.5 MB (90536980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3807375218816bd01a2ab944e75ee176a0883119132ea5e31cef0abaa816ffad`  
		Last Modified: Wed, 24 Jun 2026 04:21:59 GMT  
		Size: 76.9 MB (76929079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d31894e8548b6f26b42a65df829bd12f0c800e26324abe9b79bc7923c46312d`  
		Last Modified: Wed, 24 Jun 2026 04:21:58 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b041c3300057c8b17817a436b574a1a77995210739db8e22997cb61ac1e8ba8f`  
		Last Modified: Wed, 24 Jun 2026 04:21:58 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1654` - unknown; unknown

```console
$ docker pull clojure@sha256:b2e2b3d460a05261a4546790153cb3c1a35d6a2fa399a74472a18ff5582d1233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7334823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66daaaa1358f4df62093b1baf15b3d5bf4657be921a3f552b43dbfeecf815dbe`

```dockerfile
```

-	Layers:
	-	`sha256:3ba6d362e42d5d7863fa7fb3ed6e659d46f5015b2242eb3c9eb6c7241b0aa450`  
		Last Modified: Wed, 24 Jun 2026 04:21:58 GMT  
		Size: 7.3 MB (7318214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:624c98cc458f0be587ecc8e85099727e662988ea910d3305a26c896636197ec3`  
		Last Modified: Wed, 24 Jun 2026 04:21:58 GMT  
		Size: 16.6 KB (16609 bytes)  
		MIME: application/vnd.in-toto+json
