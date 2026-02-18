## `clojure:temurin-21-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:3db8c91ae097a05597e27031cf585f5519ba8662efdd8548ed9497f3891795e1
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

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d7fddc0f74737c028a18d4477cbf4b20ad840d7f463ff85726967488c8509e91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.6 MB (259631584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe823608acb4215078a468537dee0e75e9bb8e32086ffe449ca1f34b34662d10`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 21:44:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:44:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:44:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:44:59 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:44:59 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:45:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:45:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:45:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:45:16 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:45:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:688a0c0ceb0c92d5bd0e66ebd330f7e64f02bbd903bea6c57c9a537e9f5c296a`  
		Last Modified: Tue, 17 Feb 2026 21:45:37 GMT  
		Size: 157.9 MB (157857045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f08fa2a006e85ee78559cb4343ddc7980b8415dbb0974de8069ab5b8fcbedaa`  
		Last Modified: Tue, 17 Feb 2026 21:45:36 GMT  
		Size: 72.0 MB (71994900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d1d429a18661d2ea449afb575e8f407897f970ad029377b6918fa6bd9a2e1f`  
		Last Modified: Tue, 17 Feb 2026 21:45:33 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4a3c7d8f80970a820066a9e1e6103c82f94d2d20a2feff2bdf924ac9578d24`  
		Last Modified: Tue, 17 Feb 2026 21:45:32 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5574f38b60143926028c4d89ee01416108da1a7b4e9587ce7be0a7e83fde3fed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8c7db6e8faf5df911c7cc19c01019b648bca34ea979304d6db513a59514348a`

```dockerfile
```

-	Layers:
	-	`sha256:55639675615694766ce82ff313d77b906f689d8dafcc1e37a8c3f68138b3fd7e`  
		Last Modified: Tue, 17 Feb 2026 21:45:33 GMT  
		Size: 5.3 MB (5259403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcba78104959eccee9a2b6a4445063b99731d2136d98696fe2ee0ce1a3598e9a`  
		Last Modified: Tue, 17 Feb 2026 21:45:32 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1618f8162bf099fd8df86519d20dd36c8b6f12b61dcdbc97f4132082531e1290
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258080577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e72f3024cd854e2a7dcb1c4b0c46cc09941f1bd029afaad0cf980127994ed06a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 21:44:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:44:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:44:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:44:39 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:44:39 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:44:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:44:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:44:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:44:57 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:44:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85852beac4880827c454c5360ab55b05e8b02f6dc8f1beb84080387f287764eb`  
		Last Modified: Tue, 17 Feb 2026 21:45:20 GMT  
		Size: 156.1 MB (156133070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d9529383bebb35780e5c2ef8e050fa2b1ddbcfa4548bb608db9691f65b5f4c`  
		Last Modified: Tue, 17 Feb 2026 21:45:18 GMT  
		Size: 71.8 MB (71806400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888d84ff003e1bf88a6f0bcad323b294e42913567fc66bcbdbceabf62f521c83`  
		Last Modified: Tue, 17 Feb 2026 21:45:15 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19811d4061238f9c1af48af619546986bf1d7f8d3b00500c2c82fd5b60a5829b`  
		Last Modified: Tue, 17 Feb 2026 21:45:15 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ebdb7d4d6b9b4747e88cd32c16313b82a78f4cf5f3bf45d3e0c3f0a51463ef5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1d11d67778bb756385a3cbb3f56468ec82f210bd2713a0ef3139235bc83d17b`

```dockerfile
```

-	Layers:
	-	`sha256:520324afa66e4e55aff5a6dc9184f98be2a7b4f3787ecbddc9096ad792e44fd9`  
		Last Modified: Tue, 17 Feb 2026 21:45:16 GMT  
		Size: 5.3 MB (5265172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba4d8eff944ae9eaa510fb760ab0fb338189828b6246c97983c730a93cc47594`  
		Last Modified: Tue, 17 Feb 2026 21:45:15 GMT  
		Size: 15.9 KB (15929 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; ppc64le

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

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

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

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; riscv64

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

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

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

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; s390x

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

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

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
