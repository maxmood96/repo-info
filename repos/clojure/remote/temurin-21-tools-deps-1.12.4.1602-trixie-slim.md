## `clojure:temurin-21-tools-deps-1.12.4.1602-trixie-slim`

```console
$ docker pull clojure@sha256:9cec671b8b807e3588c81a372853cf99e954d31e4eb01396f986538a10acf664
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
$ docker pull clojure@sha256:e49d56671e9b7c82798ce1525b95b6b37a0abf942ba989fd462056ed45f8cd59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268986134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad5c97f65e63bbaeba5e3c1b9fcab0b54407679f19c6a86e7fa5b44f04df4e2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Wed, 25 Feb 2026 02:08:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 25 Feb 2026 02:08:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 25 Feb 2026 02:08:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 02:08:05 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 25 Feb 2026 02:08:06 GMT
WORKDIR /tmp
# Wed, 25 Feb 2026 02:13:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 25 Feb 2026 02:13:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 25 Feb 2026 02:13:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 25 Feb 2026 02:13:17 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 25 Feb 2026 02:13:17 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e03e689c06567c80a28fd472748594e5fc56bc0f3f151ccb3aa20e431739eb37`  
		Last Modified: Wed, 25 Feb 2026 02:09:40 GMT  
		Size: 158.0 MB (157977516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6a7437d3f3931b4b98e583e1e94724b732b961101aa46ba3ce43ba5848e829`  
		Last Modified: Wed, 25 Feb 2026 02:13:59 GMT  
		Size: 77.4 MB (77407362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9b7599634518d2602edbd9f86f3fc9f347109df7902320f7c012ca2d0f388f`  
		Last Modified: Wed, 25 Feb 2026 02:13:57 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84a07798d7faeac34ae167b665b0e19e56e3e33e070284b5b2807228ed3a6a5`  
		Last Modified: Wed, 25 Feb 2026 02:13:57 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ae88d3156f5f3b91aa5b8a2d75dd1ac301e7676b47a2050650a6f5999844ce61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6835130dfe293f236bb90533f791bd5e33e97003adbb3487d2e85d61c1aa004`

```dockerfile
```

-	Layers:
	-	`sha256:04d24a73a2950aeae03325169709cf46efce5fdfae89eeafa32f384aeef126a3`  
		Last Modified: Wed, 25 Feb 2026 02:13:58 GMT  
		Size: 5.3 MB (5263774 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d286fba43bb5e3aab013f11e88e164c2947f7ee47bbe0f6c1b0b606f9f152202`  
		Last Modified: Wed, 25 Feb 2026 02:13:57 GMT  
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
$ docker pull clojure@sha256:bbfac04aba9ba83507f7059a130366dad3cc791c1fb5be7489d8cbf111ac95e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.9 MB (249904081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba4c91f541842d73085d2f035c7f9fc6f94f617bf8976dc6b18234ffd5bc94bf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 23:22:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 23:22:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 23:22:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 23:22:38 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 23:22:39 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 23:23:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 23:23:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 23:23:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 23:23:15 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 23:23:15 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13ddb44bc4e23c845d8416452a0b531a57cc933f0df6fb076c886b4d9472f68`  
		Last Modified: Tue, 24 Feb 2026 23:24:01 GMT  
		Size: 147.1 MB (147105302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c15885f0c79a200a3484510cf633e7ed32223931042796de4e2d1091612e5af`  
		Last Modified: Tue, 24 Feb 2026 23:23:59 GMT  
		Size: 73.0 MB (72959556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c1bd3d67c902817401440968b6e7e7e7df50c8d2ac8771e189825842aa6c7b`  
		Last Modified: Tue, 24 Feb 2026 23:23:57 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd03f63ca46647b70fb896dcafa13ab77cb5915fb6142de3f362d3dad74567a`  
		Last Modified: Tue, 24 Feb 2026 23:23:57 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c99efab78425c659d0876da7644a5ef0e6cafcab2eb1cd00802a1fe8ad9fe88a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5271135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab44128ebbffeeb2ad999871ffd034665fd2a18731d36e727ca80993797f070`

```dockerfile
```

-	Layers:
	-	`sha256:274b4447a7de15ca72a4c7f72eb2cd37ae44f5b54705508d5dc850ea63333517`  
		Last Modified: Tue, 24 Feb 2026 23:23:57 GMT  
		Size: 5.3 MB (5255327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2896fcf960e0e5074068a94d100ed1a58a6ec374ae8dea2074d795257233515a`  
		Last Modified: Tue, 24 Feb 2026 23:23:57 GMT  
		Size: 15.8 KB (15808 bytes)  
		MIME: application/vnd.in-toto+json
