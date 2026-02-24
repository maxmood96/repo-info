## `clojure:temurin-21-tools-deps-1.12.4.1602-trixie-slim`

```console
$ docker pull clojure@sha256:36e4498f855b48e21e56c931435867ee12534ff29a1976633bb0e2f886f14bf6
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

### `clojure:temurin-21-tools-deps-1.12.4.1602-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:426ff89f79183d284b7cb4ffa668fc58aaa85399bfa3ed4583d9615d6f48d11e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.6 MB (259631006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:003431eeb8bf972a135f6712eeabad6495270443acf53c38cda87c06200e2805`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:56:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:56:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:56:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:56:21 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 19:56:21 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:56:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 19:56:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 19:56:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 19:56:38 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 19:56:38 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9be13993c4dd5fa235899e23709c89c49fe153ffbac0a23ff289bb4d05004d`  
		Last Modified: Tue, 24 Feb 2026 19:57:00 GMT  
		Size: 157.9 MB (157857047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06a1ba811e7e1228d9659714e86e4f078579d2cd8636f1e64135266b0eb76c0`  
		Last Modified: Tue, 24 Feb 2026 19:56:59 GMT  
		Size: 72.0 MB (71994286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97319d9c5ba1888acf136685d69ddd754831c25d24e89d77dd253cd14327f67c`  
		Last Modified: Tue, 24 Feb 2026 19:56:56 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab126d2e834f00409900dad17f95f703bc0227ece4e41607f182fece35d9239c`  
		Last Modified: Tue, 24 Feb 2026 19:56:56 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:48f3a3cb9775dd95460adbfa97bdb3c625a66d987224bd0fba3d6ac49b5c1f0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:742703f1b4e7a1a9a8bd5268bb72f6200fc690c5943762d48c754ab4811abd87`

```dockerfile
```

-	Layers:
	-	`sha256:73f3578b0c99d8ca9befd72a7d557b97d04105d1e0e42ee9421e5f5d01e3ce2a`  
		Last Modified: Tue, 24 Feb 2026 19:56:56 GMT  
		Size: 5.3 MB (5259403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3309aa9e36f5e6bd78f5b79e0478333906473f480955f044de452ed55b12bd6d`  
		Last Modified: Tue, 24 Feb 2026 19:56:56 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1602-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5bdb95ed6b75f2898812f7292d8f7c7eab26620db76a5b19bd14607bb6f34164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258082296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92dab48780cd6de7e02df572204a139421531269557649ebc26852b08f98e9e2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:30:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:30:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:30:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:30:15 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 20:07:14 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:07:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 20:07:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 20:07:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 20:07:32 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 20:07:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c4b6e7fb0f050ef49246ff2a2a086263ae5b78d2cf5c3b335c840658feded2`  
		Last Modified: Tue, 24 Feb 2026 19:31:25 GMT  
		Size: 156.1 MB (156133092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252221282045fa312ab7c5a1dc8870ba73a600d00166b6b3c39a88e957543cdf`  
		Last Modified: Tue, 24 Feb 2026 20:07:49 GMT  
		Size: 71.8 MB (71808064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46313e1e31760a792b104884aab040f16cb3ff62f6d85130abe7de15aaee0e7`  
		Last Modified: Tue, 24 Feb 2026 20:07:47 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4fb55298524d995d5948ed951ef332414c97389f26119593560ef7859c9225`  
		Last Modified: Tue, 24 Feb 2026 20:07:47 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:812bf6547e7de7716ff61862f8fcdeba1d8875985276898afa1c09ad9510846e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cddfbb77e48b28131dab48022cc11050d4d7947b6c1a93c90aff7a790e3002e`

```dockerfile
```

-	Layers:
	-	`sha256:79df98e05dc6a43c0eba66de2d1d0a38ecdbca2a78a9993cd22b76e503833e09`  
		Last Modified: Tue, 24 Feb 2026 20:07:47 GMT  
		Size: 5.3 MB (5265172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b67902ee800229d193368cdff45556574fcbb9879dbb24825ea938c45f7158ae`  
		Last Modified: Tue, 24 Feb 2026 20:07:47 GMT  
		Size: 15.9 KB (15930 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1602-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:033dfa6372cdd855db6e30177994fe1e28d0b9045c477909527bb28809b88d32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268967314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9abd399ed2a7d964748dca3ee00a4709046ed60e7f4cb762248c2ca1d1348052`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Fri, 06 Feb 2026 00:37:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Feb 2026 00:37:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Feb 2026 00:37:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Feb 2026 00:37:54 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Fri, 06 Feb 2026 00:37:56 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:44:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Feb 2026 00:45:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Feb 2026 00:45:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Feb 2026 00:45:07 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Feb 2026 00:45:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d803d46010c6f6fae7ea82f881a836bc9d2bf4afad631cfb7ffd52616e4eec`  
		Last Modified: Fri, 06 Feb 2026 00:39:44 GMT  
		Size: 158.0 MB (157977492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d9d94dd49a553eb6136a41fad225a0afc6d956a42bdb9b005769df910a3a26`  
		Last Modified: Fri, 06 Feb 2026 00:45:51 GMT  
		Size: 77.4 MB (77388594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85d1e7fe6f35913773bdde43f9dbe517e6226e1edb2d2830777f8a208bd3990`  
		Last Modified: Fri, 06 Feb 2026 00:45:48 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d14c407954658464ba427b45e5d4df4f7bfb10593481a4ecd3e42d9773d07ca`  
		Last Modified: Fri, 06 Feb 2026 00:45:48 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0f742e2577630b53bad9d77e9e47adb5fe490e83f984b404f09e619e921d6c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a63995ab3c01cc59b0813203d3c4e1df73bfb158919c3fe14c1ae79f26263246`

```dockerfile
```

-	Layers:
	-	`sha256:454763be7f4f5315735eb8f9fa41ebe07eae742b923b8028107dac577ed038ae`  
		Last Modified: Wed, 18 Feb 2026 00:03:08 GMT  
		Size: 5.3 MB (5263774 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e4b791161483362a5d3909486970f0235cb2cdc62a89c28af2d1a4aa836073f`  
		Last Modified: Wed, 18 Feb 2026 00:03:07 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1602-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:90d84ff3534761311db737beb5490a81ae4883f412021e7f6f1dc092850d5b67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.4 MB (256373423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e701854161aa9713c6af912e21712ecc49e6e9ae6e1a6f489ebbc92daa595282`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Wed, 18 Feb 2026 11:04:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Feb 2026 11:04:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 18 Feb 2026 11:04:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Feb 2026 11:04:54 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 18 Feb 2026 11:04:54 GMT
WORKDIR /tmp
# Wed, 18 Feb 2026 11:28:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 18 Feb 2026 11:28:27 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 18 Feb 2026 11:28:27 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 18 Feb 2026 11:28:27 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 18 Feb 2026 11:28:27 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4526db52defd9278f79daec64ebfa633041460dbe0cfad19564ae34d84b13b4c`  
		Last Modified: Tue, 03 Feb 2026 07:14:46 GMT  
		Size: 28.3 MB (28276389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c1241f02353400467eda8df7776c998fe2e431d20bf997eeca9a8cae295c3e`  
		Last Modified: Wed, 18 Feb 2026 11:11:04 GMT  
		Size: 157.2 MB (157216934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8591c1784a97462458808eb239b0727249c978fc231694d52079cf8a1fb81979`  
		Last Modified: Wed, 18 Feb 2026 11:32:18 GMT  
		Size: 70.9 MB (70879056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e54d24d93e7ba0888c413c456377394e333cd6e2680c702663a85a6c2a77a24`  
		Last Modified: Wed, 18 Feb 2026 11:32:06 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5da49137056342e72134136adc0eb19638b32a027f3d7f81c13edc08290b75e`  
		Last Modified: Wed, 18 Feb 2026 11:32:06 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:aa1ba474f6ec5bce4a1d37b638f15c6338c43a4914fc144b88cf86ab353d0b85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5264726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:908f8593a87ab24b4602d083ebb0f9aae4d83f53fe9b9c798edd452dc5fe863c`

```dockerfile
```

-	Layers:
	-	`sha256:8075559ad73c4fea24ec0af6c7ec4647201668d32dd25562f341aa47f46528ea`  
		Last Modified: Wed, 18 Feb 2026 11:32:07 GMT  
		Size: 5.2 MB (5248867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:516ae1ca539ab4a17e32953159b4eb5656513d0835edc772ba2a10f9e75aad31`  
		Last Modified: Wed, 18 Feb 2026 11:32:06 GMT  
		Size: 15.9 KB (15859 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1602-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:d59fa6a94250a6a9803c4286064a6af29750db1fcdd734f1cee460ce286f2b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.9 MB (249897790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00c5f28c3032e9211b8dd6028c812cb751934c6492dc628f01aca27426030622`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 22:15:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 22:15:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 22:15:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 22:15:25 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 22:15:26 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 22:16:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 22:16:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 22:16:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 22:16:04 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 22:16:04 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d683fa0198e3614d660a404ef42dda95f985ff85d3392faaa770cc033bbf0045`  
		Last Modified: Tue, 17 Feb 2026 22:16:50 GMT  
		Size: 147.1 MB (147105294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27bff7004102cb26a7a1768d5bad16930950293a649967c589463bd224dcaec1`  
		Last Modified: Tue, 17 Feb 2026 22:16:48 GMT  
		Size: 73.0 MB (72953304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f714ecbc25d9067f25f2b9af540fbfcfcf4165a45de4b02b2dd1a6f8252a40`  
		Last Modified: Tue, 17 Feb 2026 22:16:46 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda5e77566bac658110e05ee2d297a5906163f2560344215d736ea67354a104e`  
		Last Modified: Tue, 17 Feb 2026 22:16:46 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:32b4b6e266ff8962c9aaabdb8735f5e198207c93781b285acad5c6fa7ebb7286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5271137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375eb8ce376aa41f04b3938203cd2d799dcb013ee2482097d46e168af50edd0b`

```dockerfile
```

-	Layers:
	-	`sha256:df765dab675f3df144b68e8027e17775642b4825a0fb533b88f0f1f1356c02eb`  
		Last Modified: Tue, 17 Feb 2026 22:16:45 GMT  
		Size: 5.3 MB (5255327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0be253629fe86031d388f3c5e91a4b9928910346a69dc56ccb61d736148ecaa5`  
		Last Modified: Tue, 17 Feb 2026 22:16:45 GMT  
		Size: 15.8 KB (15810 bytes)  
		MIME: application/vnd.in-toto+json
