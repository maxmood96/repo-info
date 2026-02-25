## `clojure:temurin-25-tools-deps-1.12.4.1602-trixie-slim`

```console
$ docker pull clojure@sha256:c1cd95bfffec62adaad9d229896cd982ee034d83ac4742592e198338115327a5
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

### `clojure:temurin-25-tools-deps-1.12.4.1602-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:52d6cc0ece6c90ba6416cf1f7a44ec6803035138d06fcc1660712d6e376a0b72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.0 MB (194030482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:403e7e604f3f83233556842d0d1c93029c8c10e51699998bd7d4aee91cfa8d02`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:57:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:57:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:57:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:57:33 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 19:57:33 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:57:51 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 19:57:51 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 19:57:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 19:57:51 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 19:57:51 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe564199e0775db75226ddb6bcc99b54345340bead994374bf87eee58d5e071`  
		Last Modified: Tue, 24 Feb 2026 19:58:12 GMT  
		Size: 92.3 MB (92256297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba607e54bb7185a35c17f77423b9daf278b11c51bf2faab0d11c331d00d6c556`  
		Last Modified: Tue, 24 Feb 2026 19:58:12 GMT  
		Size: 72.0 MB (71994517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b183ac7c74fb8023fb2e95e2639eda79a8b26d94ddb2277bbbb76a90ab9ec92d`  
		Last Modified: Tue, 24 Feb 2026 19:58:09 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6acf8f6580f0719766e2beeb3ec1e5c5427eb590412ce749de31c2c8bda70a7`  
		Last Modified: Tue, 24 Feb 2026 19:58:09 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b80589e2d3b8276a8a8a7618f613a9aa22c0310fca108c5f709cd777f4aa283e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5242130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a58d8f07567af7d84d807ea64d176341571a64bdc4a6a8aad5ed8f3d185e2dd`

```dockerfile
```

-	Layers:
	-	`sha256:5849221f36e0b3e3054247d8a1aa81b4062679a1a28a74a42336822329952729`  
		Last Modified: Tue, 24 Feb 2026 19:58:09 GMT  
		Size: 5.2 MB (5225637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca6a22d1b6e1bea890974544a589484a505e2cb52cc9fde47bb49fe8295798a7`  
		Last Modified: Tue, 24 Feb 2026 19:58:09 GMT  
		Size: 16.5 KB (16493 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1602-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:44f9e04b3ed16db0bfa699a61fbcf575ec5db843557c73dea3c490403a444737
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.2 MB (193237355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4078ece82fee778f19032db30ef9978361836ad8cfa352264183c1248f295b27`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:29:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:29:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:29:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:29:44 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 20:08:11 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:08:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 20:08:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 20:08:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 20:08:28 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 20:08:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087ec517868ed803a063545471c1a9157e24188ebaf82c221efe60f61d6ba345`  
		Last Modified: Tue, 24 Feb 2026 19:30:40 GMT  
		Size: 91.3 MB (91288274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e8f58bb425dcf8a27eccd2d577e73517623297381c4a17d4e14115cb173af2`  
		Last Modified: Tue, 24 Feb 2026 20:08:44 GMT  
		Size: 71.8 MB (71807946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6c359650e4db4570eefeee2f5a4d738dd432ba718bb3b80f079ac07afc6f50`  
		Last Modified: Tue, 24 Feb 2026 20:08:42 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a8949d00d3dd5b132f7cec917b4c73248634c62c215d307b39a7576e346098`  
		Last Modified: Tue, 24 Feb 2026 20:08:42 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1b666be3d0892c76c1c45318fa5ff091c5f352c12df2df240afe8f6830f5d70f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5247263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1229d2369efefc4f248a1ecea4164944a7ce73464579c1d2f662d390bde031cb`

```dockerfile
```

-	Layers:
	-	`sha256:05e26fe2dea06cf74db836fbf425ce844ecc12ca069e52cea3e4b6cad54bbb61`  
		Last Modified: Tue, 24 Feb 2026 20:08:42 GMT  
		Size: 5.2 MB (5231427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a980dff3634b212c7c6648aa6a0be62b64e0da0e2bebb75dc6f64f87b34a9bd7`  
		Last Modified: Tue, 24 Feb 2026 20:08:42 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1602-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:85fdb6d392d49c2525bb349839bb162c7092fd0ab39cd81836c6c89e7fbf7517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.6 MB (202641603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b8ddf5f0214c512d0de573856743b65ff7bf88347982c27054704b6233116b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Wed, 25 Feb 2026 02:16:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 25 Feb 2026 02:16:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 25 Feb 2026 02:16:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 02:16:00 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 25 Feb 2026 02:16:00 GMT
WORKDIR /tmp
# Wed, 25 Feb 2026 02:20:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 25 Feb 2026 02:20:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 25 Feb 2026 02:20:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 25 Feb 2026 02:20:19 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 25 Feb 2026 02:20:19 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298dcaf9753f81c5e53558fa373fd37f301367b171dcf2c711fb1baa27c30921`  
		Last Modified: Wed, 25 Feb 2026 02:17:31 GMT  
		Size: 91.6 MB (91633002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13cb4dfabbbb4ce76272f3fb414346a37145c1e64f4ca34454ccbb3ff613270`  
		Last Modified: Wed, 25 Feb 2026 02:20:57 GMT  
		Size: 77.4 MB (77407343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9399c028ed4996a107a23a19d0e7f6c89037b65f28d71b3a3d287b1700cfe591`  
		Last Modified: Wed, 25 Feb 2026 02:20:55 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251ce48a39d869383bb2b8ca57a0da7feed2e54795596617fdddb4e0093d09a2`  
		Last Modified: Wed, 25 Feb 2026 02:20:55 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4e24bcc8c0cfb51b743dd120b7e1a031f6625f2a7c9c8e870a23eb68c3e764f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88932224941842157191a85dc88dc123f1dba54c4fda777db36fc3f0aa6a95a1`

```dockerfile
```

-	Layers:
	-	`sha256:40c85ed7b047d922ac3449caea21d102058b1f36dc343fe96188480d0974441b`  
		Last Modified: Wed, 25 Feb 2026 02:20:55 GMT  
		Size: 5.2 MB (5213332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:485d56091cb16cdb248596671a90c3cbe2a995d8b381b267212977fd7547496a`  
		Last Modified: Wed, 25 Feb 2026 02:20:55 GMT  
		Size: 16.6 KB (16553 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1602-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:5b05611e670e1d87990755833873f0060254ec52b7dbb0e109e2e88a798b9dcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.9 MB (189930378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90207267d35650deba8a8551715bf28efb326cd923122a938fc9d5900964e0a9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Wed, 18 Feb 2026 11:37:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Feb 2026 11:37:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 18 Feb 2026 11:37:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Feb 2026 11:37:05 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 18 Feb 2026 11:37:05 GMT
WORKDIR /tmp
# Wed, 18 Feb 2026 11:59:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 18 Feb 2026 11:59:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 18 Feb 2026 11:59:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 18 Feb 2026 11:59:56 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 18 Feb 2026 11:59:56 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4526db52defd9278f79daec64ebfa633041460dbe0cfad19564ae34d84b13b4c`  
		Last Modified: Tue, 03 Feb 2026 07:14:46 GMT  
		Size: 28.3 MB (28276389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a69466dfc7b8b2fe8edf62758177fe993cfe6f66d072d0ca0803ea54b9a979e`  
		Last Modified: Wed, 18 Feb 2026 11:42:30 GMT  
		Size: 90.8 MB (90773436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ff929ff5739745503e2d7d5596eb11ddb0d8da5adf230f0c1f735de258c3fd`  
		Last Modified: Wed, 18 Feb 2026 12:03:31 GMT  
		Size: 70.9 MB (70879507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a676881e66fb8eb63327059b58532d17512eeb506614239d3c9bb3eeeaf7291b`  
		Last Modified: Wed, 18 Feb 2026 12:03:20 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4ad4ec4d3de79a3ea3cb8625c80fb68fba94cc21a77839da48542d56137725`  
		Last Modified: Wed, 18 Feb 2026 12:03:20 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:046d7d14cdb03cd1d4f9c263d4cdc4d3b71692c90c3b506818b5874a6a76a8eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5213677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0646c15cd27c424899d5a154d101925c288b3d9ab38f722414a60ec7699701c4`

```dockerfile
```

-	Layers:
	-	`sha256:e277f6295ea63e9817b1f3fb15f8164290fa349f3a91282c9c8890ae90cc6c20`  
		Last Modified: Wed, 18 Feb 2026 12:03:21 GMT  
		Size: 5.2 MB (5197124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96e3c5d35b8340acbf472c1845e99f0d86189737381f5344aeb14e830055c8c0`  
		Last Modified: Wed, 18 Feb 2026 12:03:20 GMT  
		Size: 16.6 KB (16553 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1602-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:3c3e42624cd60a6ac8746a32eb0db37bec3b737f1d8aa9d00d382254944e6eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.0 MB (191032957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a42e0dc54bdbe9c5bee1185c811c160a971bb882a5b1e87153bc4cc85e043544`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 23:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 23:26:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 23:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 23:26:20 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 23:26:22 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 23:27:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 23:27:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 23:27:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 23:27:14 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 23:27:14 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31bdb7559bfa77d5702f5ace7dad2898ba4ee8cd813b72d03811b472c6ea57c8`  
		Last Modified: Tue, 24 Feb 2026 23:28:00 GMT  
		Size: 88.2 MB (88233846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21eb38b86930e11f8cc2e5315efbbd5f70a5c839c567cfd11f08e3782b061037`  
		Last Modified: Tue, 24 Feb 2026 23:28:00 GMT  
		Size: 73.0 MB (72959889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8336c043595d7510ecc1d2e276674980a3d9ca75688d0d6922cb5e0d411307`  
		Last Modified: Tue, 24 Feb 2026 23:27:57 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5fc61d42f39b3180d50dabb10b0a1394a20c337cdd7a0e83a3aa5e35ed39d91`  
		Last Modified: Tue, 24 Feb 2026 23:27:57 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:46ab6c1acd1e509f01daf5d68b905a59e957b551207470da865ee5da55312506
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5222616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc92d203b0c9531c262291f3205d2498376d4ce859dfad37e6ce15f0288fb210`

```dockerfile
```

-	Layers:
	-	`sha256:10ba592f93cf121e4bccc03544f925f5a877f3022b4aa922fdd4963138baa66a`  
		Last Modified: Tue, 24 Feb 2026 23:27:57 GMT  
		Size: 5.2 MB (5206123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17ce9570a03bd4c1aaee6b79f5c68abb7aa026bc109fb275a3d7e018146ea6bc`  
		Last Modified: Tue, 24 Feb 2026 23:27:57 GMT  
		Size: 16.5 KB (16493 bytes)  
		MIME: application/vnd.in-toto+json
