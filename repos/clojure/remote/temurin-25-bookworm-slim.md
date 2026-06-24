## `clojure:temurin-25-bookworm-slim`

```console
$ docker pull clojure@sha256:4849a252f1fad556d6b2f11ca05768eb246cfd272db6167de3b0ee64ff3da362
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

### `clojure:temurin-25-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1c87a49907be3bbbe31d3bc1c0ae67006fb43dcb0e59035d3292d7ae47a91a27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.5 MB (187455934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff00f65d35ba8ade0211c10848615986b1f4684c3a11f23d3e9c31f51b2fa276`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:21:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:21:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:21:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:21:20 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:21:20 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:21:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:21:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:21:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:21:34 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:21:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4adf0151446b3272a841b704509105684627af1d8938814f5deaac576f00e48b`  
		Last Modified: Wed, 24 Jun 2026 02:21:55 GMT  
		Size: 92.6 MB (92574585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2702606708b002b2e9247b34f8a35fc2f50eddf814155d4c683c3ae2527ede7d`  
		Last Modified: Wed, 24 Jun 2026 02:21:55 GMT  
		Size: 66.6 MB (66642670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc004c8757de8a18ddea8026264b3d4154508d8f821ae6b22bb0ab9f3b6e325c`  
		Last Modified: Wed, 24 Jun 2026 02:21:52 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:990d857770cad3acd32fe044598add4df155cfd6d0eab7d51a7cfcd07cd905d7`  
		Last Modified: Wed, 24 Jun 2026 02:21:51 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:92cfd848ea656f259bd69527b9a1f979e959c836c19aaf09485fcfaa1e69184d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5098768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdf48df83cf2e92f10cb35b4eca74cf2cd921efa416a45e973aedcd7208a6076`

```dockerfile
```

-	Layers:
	-	`sha256:2872de6660f982ee42dfb3b6d9f87543eb655f21986f7da76dcbf97246f7c23e`  
		Last Modified: Wed, 24 Jun 2026 02:21:52 GMT  
		Size: 5.1 MB (5082089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bb775850628c6469d98cd35fea22848a8a12acc2561ed405f88ebf25b495dd0`  
		Last Modified: Wed, 24 Jun 2026 02:21:51 GMT  
		Size: 16.7 KB (16679 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b39babbf22e83b19a35c540443176df9bd4dda2400ba9f2390c25f1a0c50ab83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.3 MB (186308950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d80b9672612d59f98a669059d738a5f6a3a7baff4794749fdc74d0d76f0b488b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:28:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:28:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:28:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:28:02 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:28:02 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:28:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:28:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:28:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:28:16 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:28:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:74f1dcfcc9c80045f6f6394ffcfc261cb19d0c71b97e964aec3d4abf4e0f7009`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 28.1 MB (28122418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0abd1129f0dcf442f4507efca1d18049de4c2107bd7cf8e67d8d73e8469d2af0`  
		Last Modified: Wed, 24 Jun 2026 02:28:38 GMT  
		Size: 91.5 MB (91542253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d00d59c0fd9766b0dd77dbfd900c61d291f6c91ba3307fe1965a4d11791299`  
		Last Modified: Wed, 24 Jun 2026 02:28:38 GMT  
		Size: 66.6 MB (66643240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2add8412ab1a32b14df62ff00bd9e3cb5aea48dad7b6915787353c07727a6b80`  
		Last Modified: Wed, 24 Jun 2026 02:28:34 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6867919a92b61d6e29b91820fffdd2fb2bcadf5a5a17d6a1db940587e0ddf051`  
		Last Modified: Wed, 24 Jun 2026 02:28:35 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5b792fa241858c3192b16d2c346511dab55089913d4f12b0564b37f3865e756c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5104692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7303c809dc327fa23dcf8922b17d940c24c96ce6831522c43f44e9c98c91bcc1`

```dockerfile
```

-	Layers:
	-	`sha256:4fe008c36708e5325c505016acd116e62d95854f60802d721bf3d8f0dd3b0860`  
		Last Modified: Wed, 24 Jun 2026 02:28:35 GMT  
		Size: 5.1 MB (5087871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:832b2370510ccd4cc573c11b677baf540a5b40086f63771cd3b75a688e14c8dd`  
		Last Modified: Wed, 24 Jun 2026 02:28:34 GMT  
		Size: 16.8 KB (16821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:1709f9d5d72cc626d6805abe5d12be49c1c63eec864ba805b3ef7b202bb270bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.5 MB (196473295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b3c052e6949024d9151a80d2420c41a9ced43d978561374e607808f46a989b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Wed, 17 Jun 2026 00:03:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jun 2026 00:03:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 17 Jun 2026 00:03:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jun 2026 00:03:19 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 17 Jun 2026 00:03:20 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:55:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:55:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:55:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:55:38 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:55:38 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:23f7cdee3ef2598b081c2b848fee95730a7ab2b1cc5b726c72dcb8c2fe3632f7`  
		Last Modified: Thu, 11 Jun 2026 00:21:33 GMT  
		Size: 32.1 MB (32081941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ceb0eb5280b5d711b09e7b6fc60f0539124c87d3b78261261a7696dc0d1b48`  
		Last Modified: Wed, 17 Jun 2026 00:06:20 GMT  
		Size: 91.9 MB (91914038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd04172e70ec74e8809fc5ad091eec63513d8ead413ff86ba78864470e1f68ac`  
		Last Modified: Fri, 19 Jun 2026 02:56:20 GMT  
		Size: 72.5 MB (72476275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd028238f62af350e76aaf9b47644b00ae8783cfd5d26dcbfd08d1c2a3863b2f`  
		Last Modified: Fri, 19 Jun 2026 02:56:18 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716a1fa406d268129021fd8d8011e986d3d7a9069101b9a350bee143c488b1ac`  
		Last Modified: Fri, 19 Jun 2026 02:56:18 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:825ea9cd0767caacdb6e6d6e7378c17250a23030800b43779ea3f87e8dd0e2ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5087309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9f4d133ca16053e0a621c5ba12bf28256a7e429ed47d461ad39f3b61bcc64ca`

```dockerfile
```

-	Layers:
	-	`sha256:41c22855a0c00d4475aeb905b7b3ad8f6dc5e3af5b8d72320f1286691735193f`  
		Last Modified: Fri, 19 Jun 2026 02:56:18 GMT  
		Size: 5.1 MB (5070571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:612bf34aa50d71c12a4ca15b95b751f38c7f90835fa91eff1cb71a05e688afdc`  
		Last Modified: Fri, 19 Jun 2026 02:56:18 GMT  
		Size: 16.7 KB (16738 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:e711ef57e5327022e8252150b71a46a9f27293167e96daee9b45134a8b0b0728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.8 MB (180767112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ae9880b150acf55cc83e8eff53a584a6d708c49702633c95662f3a06d8487b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 04:17:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:17:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:17:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:17:28 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 04:17:28 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 04:18:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 04:18:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 04:18:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 04:18:55 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 04:18:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e9aeeda7513dde59469463716e9e14f36210d6570c3cad5e5440b32d941733cd`  
		Last Modified: Wed, 24 Jun 2026 00:27:21 GMT  
		Size: 26.9 MB (26893585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64512e22f1cf746a8cfa05946899c57c3e320cd67aa253aab1b07c92bdf674a2`  
		Last Modified: Wed, 24 Jun 2026 04:19:00 GMT  
		Size: 88.4 MB (88420330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7150b001c2979b6a061f03f75f153c5cbc4bb108d727c92aab345e42b4070cea`  
		Last Modified: Wed, 24 Jun 2026 04:19:17 GMT  
		Size: 65.5 MB (65452157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df895b4bbc5b89d3c2bc72b4b9a49cdabceb2e02ae5e5587ec43f23488c6bc65`  
		Last Modified: Wed, 24 Jun 2026 04:19:16 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125c4af972b341f723ba78031d6a4ca312a3775c61589b7b96335c6e1e906a30`  
		Last Modified: Wed, 24 Jun 2026 04:19:16 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5bbf1651cd0075a4ca1fb247e55a81371abe17d0cbfe3e52c95079f1a8cd1d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5074651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:923bef3879a70195c57830df1e6dd4fd3cc0d02d51830c39eca0134ab95fc556`

```dockerfile
```

-	Layers:
	-	`sha256:1dab3c36c8e5d58aa6242e1406803d713cd744c3f6c30f8f257c0f5a31e5b118`  
		Last Modified: Wed, 24 Jun 2026 04:19:16 GMT  
		Size: 5.1 MB (5057972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bfbcaea2bb3a5eda7b0b58363e46a7a54cd0bb686e905c4e96ab3db319d6892`  
		Last Modified: Wed, 24 Jun 2026 04:19:16 GMT  
		Size: 16.7 KB (16679 bytes)  
		MIME: application/vnd.in-toto+json
