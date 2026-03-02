## `clojure:tools-deps-1.12.4.1607-bookworm-slim`

```console
$ docker pull clojure@sha256:de4bd89b886a4c91b6280617e0a818a7dcb78ba0abacb989b662d4682a317fab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:tools-deps-1.12.4.1607-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6b107ebe65d890e638881a288540fbf94b60668893a733afff98756b89bf8ae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.2 MB (190184688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0019b1cd2bcde933625b633216a1ba7976bb2707d6f6d89bb648d2f10c0b17f4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Mon, 02 Mar 2026 19:48:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:48:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:48:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:48:19 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:48:19 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:48:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:48:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:48:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:48:34 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:48:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24327a40272e6ab0f35a5447ec82c55d2e9a3076a1ada5dbb0ee9d3d02723950`  
		Last Modified: Mon, 02 Mar 2026 19:48:55 GMT  
		Size: 92.3 MB (92256315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e0f2337a536cf9824af4b3df7cb62ea58ca3b59dbfde16a8b45222d022b763`  
		Last Modified: Mon, 02 Mar 2026 19:48:54 GMT  
		Size: 69.7 MB (69691048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64a4139b2e4e378e21f972292868209c931fa283852a93a1439a701f165a39b`  
		Last Modified: Mon, 02 Mar 2026 19:48:51 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a17cf1466bf815d5d2f424b26419577f86aa89d32fd05532e3e8111d5832293`  
		Last Modified: Mon, 02 Mar 2026 19:48:51 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1607-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:849358e6cc9ebca9ed45063612cea5c24f959ace43cfc48c551fb3bfe0486c3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5100786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b76f0a8aedc85bee56ae32fa9769a66cf09c9b276da88c3c43303f1f25b7e55e`

```dockerfile
```

-	Layers:
	-	`sha256:17a4eecfed3196c599168a194f989bfe7428878e0eab5c82cbae8a67947f5c04`  
		Last Modified: Mon, 02 Mar 2026 19:48:52 GMT  
		Size: 5.1 MB (5084261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9367c70957ad28d2528321912eb7a28d21ce622c6265bd3474f98bcf7e00d683`  
		Last Modified: Mon, 02 Mar 2026 19:48:51 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1607-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0f179ff6301c03701c7a2c1c685de63bec56a8770a1871523beba232da73be16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.1 MB (189093347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5a64c162642aed4f4112adc09b1c4fd821b739981687561a12be18a67fa763b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Mon, 02 Mar 2026 19:48:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:48:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:48:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:48:17 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:48:17 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:48:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:48:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:48:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:48:32 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:48:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed32f54341c5f6e91646992c4ed8171f1a2939a5fa039ead15e7bcd75455c0f`  
		Last Modified: Mon, 02 Mar 2026 19:48:50 GMT  
		Size: 91.3 MB (91288304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7eab21083519e370838b20190b61b216cc950d44b9c4488726158195360b5c4`  
		Last Modified: Mon, 02 Mar 2026 19:48:52 GMT  
		Size: 69.7 MB (69687918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b898b2728f52227ee8f14658bb846d02a051b959bfc0beaa524ef3dbbdb973`  
		Last Modified: Mon, 02 Mar 2026 19:48:49 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c30b00a3e30718e1be5e159b3d70a61cc4338aeeea0d3982e3ce38818a180e0`  
		Last Modified: Mon, 02 Mar 2026 19:48:49 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1607-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:95f16d5b12bf677952e3c0a7dcbc0249b3e3ceb67eeb6fb8fb8b6a7985f9b30c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5106710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e13962e4033b2f80aa19dd335f0d81d4d6121be4d96e60923c547cc97b9a68`

```dockerfile
```

-	Layers:
	-	`sha256:acde4a556714a7291c4d9afed874d7da34180f8e54048d0cdf7b3bc827ffe7b4`  
		Last Modified: Mon, 02 Mar 2026 19:48:49 GMT  
		Size: 5.1 MB (5090043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27536d4bdcc1292ca8d4c7b205b307b0d880afd1229f136c1d16104e8b624258`  
		Last Modified: Mon, 02 Mar 2026 19:48:49 GMT  
		Size: 16.7 KB (16667 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1607-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:c4a91f62509fe525cdde0d86b1f860df235fde1c6671e5300bbdccf4b55c5caf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183630032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1f424996356fdc3490a281861108cb0289f59c953d62369ae48ee79509cf453`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Mon, 02 Mar 2026 19:51:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:51:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:51:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:51:34 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:51:34 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:51:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:51:47 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:51:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:51:47 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:51:47 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9bef76beebe598b8ff14a041376f35899cceaeb51a5810f860a721170c7db85e`  
		Last Modified: Tue, 24 Feb 2026 18:41:34 GMT  
		Size: 26.9 MB (26891524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a170f6d8ee797298bea616da8585392433435c386f042db18a4690f8f1fabf7f`  
		Last Modified: Mon, 02 Mar 2026 19:52:14 GMT  
		Size: 88.2 MB (88233869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b24793a190af85b8a34c3287d8071197c9b24c3cdae4cecdb094e6662417932`  
		Last Modified: Mon, 02 Mar 2026 19:52:14 GMT  
		Size: 68.5 MB (68503597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c2930c0f1d217f56988aeb4a04286286706fd4ac813c9068f0cd513a684f59`  
		Last Modified: Mon, 02 Mar 2026 19:52:12 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08a7efed4994036e7cd862a847eed30e1c15e13e5e7bfd6f5f3eaf619c7f2cc0`  
		Last Modified: Mon, 02 Mar 2026 19:52:11 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1607-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f5b830768b39e8dafaba3c1947bde98a8e1084531af18e3da7649fb6dd3211ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5076669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bfe8a6ffb8cde5aca410c9851edb11a2e7bd13685157633197cc8d80b4fe747`

```dockerfile
```

-	Layers:
	-	`sha256:c2ee2009c5e3d28def9b973efccd6f4aee84269176a10c2994a719257df0e47d`  
		Last Modified: Mon, 02 Mar 2026 19:52:12 GMT  
		Size: 5.1 MB (5060144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:896f006f2b4762c423e3d2d9e2bbfb2ec6749c388ce90e2199ee648cac2fe38b`  
		Last Modified: Mon, 02 Mar 2026 19:52:12 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json
