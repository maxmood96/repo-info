## `clojure:temurin-21-tools-deps-1.12.4.1618-trixie-slim`

```console
$ docker pull clojure@sha256:0d512c0a50c295acde7a9058f0c7fa1651da8705917d25361f0b4005f7b1a734
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

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:bf4ce3f7d73bffff2cdcab6f9c8cd44efccfd701f94a722b61c8e9128a12918a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.6 MB (259645817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2862cef418d126dfbe79e7bcc6c14d21494e7137cfba6db89d652788f3db8ae`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 02:40:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:40:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:40:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:40:58 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 03:17:19 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:17:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 03:17:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 03:17:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:17:37 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:17:37 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb505189910bc199c076ac3bb2347d9ecb604a5189192363af66d17a0db21ab1`  
		Last Modified: Tue, 17 Mar 2026 02:41:47 GMT  
		Size: 157.9 MB (157857118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0500ab27572549dfad063c046778e2299e2aae2cfebb4b00e97ce9c0aa77d182`  
		Last Modified: Tue, 17 Mar 2026 03:17:54 GMT  
		Size: 72.0 MB (72012157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d14913f7c3f24a92fde33795823f763e493b4b548b177736cbb0dcbd3521d7`  
		Last Modified: Tue, 17 Mar 2026 03:17:52 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b31b5786f7a2401a0b83946d37007bf7afd1894bc9f68d0ab2b5ffb2ed3525`  
		Last Modified: Tue, 17 Mar 2026 03:17:53 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:05ca0774cbc48f3e32321e8d7cb16167a7055c101b3ffe2908799699b19ef17b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5276801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a990a03e460449439fdeb7b5020ab3c34471cf353223178188516deea287e3d`

```dockerfile
```

-	Layers:
	-	`sha256:f9ce247febc10dc81a0b6f53d46904df8f048c3ed15d9a285bdc795b44c51e50`  
		Last Modified: Tue, 17 Mar 2026 03:17:53 GMT  
		Size: 5.3 MB (5260990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:202eab32c70f55eac8c029e6749ca22daaa2cfc1a483692f7f08a93eeb9146b5`  
		Last Modified: Tue, 17 Mar 2026 03:17:52 GMT  
		Size: 15.8 KB (15811 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8741b0e68718349b31957d5791bf07fbb3d02689ba9f53d030b0cf186e520862
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258102884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:941a8593966a9e787c80fa85b5d23b016be9bc25b6f9c2eba24d732a6255a36d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 02:45:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:45:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:45:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:45:34 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 03:05:08 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:05:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 03:05:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 03:05:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:05:28 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:05:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82cb513564ee1407eeee22eae7c45e107e887fee69943b91d27646fd7ddc81a8`  
		Last Modified: Tue, 17 Mar 2026 02:46:42 GMT  
		Size: 156.1 MB (156133025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f45b4e8a5321b86536aff62080ae2e9870e0c735a619af3dbbb99d7c89d2f29`  
		Last Modified: Tue, 17 Mar 2026 03:05:48 GMT  
		Size: 71.8 MB (71830403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fa7d42d2d664146d54388ab8c6396f19c4c66d3f106a150d0c58b4a25d0107`  
		Last Modified: Tue, 17 Mar 2026 03:05:46 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6ad53575c7203178b5224d9612b04475851ec05731ff30b51040c7e2e1d09e`  
		Last Modified: Tue, 17 Mar 2026 03:05:46 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d0b188648e85442047c78f989ae724ebf4f010ba53e1fce8442a0a5ac762f0a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8836f64b3d57c3a2e29b9fa0fdc9f03d490cc24780f9bf43506fa436fc7cec90`

```dockerfile
```

-	Layers:
	-	`sha256:effc1bf852227790cd779376e1e0854faf2f69220cffc42809e0b4ff0a967940`  
		Last Modified: Tue, 17 Mar 2026 03:05:46 GMT  
		Size: 5.3 MB (5266759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:183f445e0b91b6207acafd0146f8bd88cf0dfd121379451ef83f1b1c581159eb`  
		Last Modified: Tue, 17 Mar 2026 03:05:46 GMT  
		Size: 15.1 KB (15129 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:793e7368612b44f8db8dd42cd3fe6a1c120bab3259c86579f51be70fb18a5230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (269000902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d22ddd49ff8594ca04896a235bcac404d1ef6c0cfc19453f0079ceca2e37a668`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 18:37:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:37:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:37:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:37:33 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 18:37:33 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:43:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 18:43:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 18:43:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 18:43:28 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 18:43:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f078139432e0b368e27241df524f6ef0ed0148b217d7495670dc297af77699fb`  
		Last Modified: Mon, 16 Mar 2026 21:55:56 GMT  
		Size: 33.6 MB (33592834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a3ec6fdaa48a78814b25d06b8958fec2609466001981f561b8114f6360e796`  
		Last Modified: Tue, 17 Mar 2026 18:39:04 GMT  
		Size: 158.0 MB (157977471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d91eb187d8917ace2dc97d414b07a5d6c7202303e23958d567f71b2bbcbcee`  
		Last Modified: Tue, 17 Mar 2026 18:44:06 GMT  
		Size: 77.4 MB (77429555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53fb8b0246ac2030f984b095328c08da0c3407fc7789e5ed3e4e77884c282d87`  
		Last Modified: Tue, 17 Mar 2026 18:44:04 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3515028beaaafa57b08caab68e3222ab62f377d358557810c1a1d27b92f0b59`  
		Last Modified: Tue, 17 Mar 2026 18:44:04 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:890cdd56beb3f7bc2a1b8867a63cde085b909bc27f00c144bcc716e18d36e561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a91ee67588db7298d47cfba18ff5778a16329aab4ca383963e865b03ad857c66`

```dockerfile
```

-	Layers:
	-	`sha256:4f93896a4e3f5de116f867276756f9c4894db80c40ceb6f6a1895474890340af`  
		Last Modified: Tue, 17 Mar 2026 18:44:04 GMT  
		Size: 5.3 MB (5265361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc70129aaa174882bccc33a61ef0a5823b3ac1d8b6f69d070810dda346e684ae`  
		Last Modified: Tue, 17 Mar 2026 18:44:04 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:6fe2a4a9684742924a7540cffca96134e4e253f71b7158ebc1974668f06128fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.4 MB (256393854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09d2760dc01c7e4cecd6f9b4c5cf23580c3cd0c6136a382b2d50bbaf89717d99`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 11:23:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 11:23:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 11:23:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 11:23:46 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 04 Mar 2026 11:23:47 GMT
WORKDIR /tmp
# Tue, 10 Mar 2026 01:47:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 10 Mar 2026 01:47:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 10 Mar 2026 01:47:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 10 Mar 2026 01:47:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 10 Mar 2026 01:47:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6f2d4c20cb87ce38553ebd9ee153c1d2ba4124eefd89d1277f7fcbaccfbfa3`  
		Last Modified: Wed, 04 Mar 2026 11:31:31 GMT  
		Size: 157.2 MB (157216904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571881e3257cad982f734bbb80febd803b299e2063dff5c53c943ce6f6760413`  
		Last Modified: Tue, 10 Mar 2026 01:51:44 GMT  
		Size: 70.9 MB (70899486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c008bb54cab1c875fda1c06831458275ab51577dd26b9db4e55f5929bf1579d`  
		Last Modified: Tue, 10 Mar 2026 01:51:32 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c18e158bb1824ee66ddd858c648436d473964bf5f0a72fca6273d52487fbfb`  
		Last Modified: Tue, 10 Mar 2026 01:51:32 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:45e019bc4c3b97e1d2d5f0137da517e9f8565bc985e5b08e08f92fc1aa9a6d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5266240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fff93ce564c7bf3ef35950823e17da93a17616b6c90245c81d742b3a3c79eb81`

```dockerfile
```

-	Layers:
	-	`sha256:a89166c72a5fd45b5803572a49e76397c33e668ebf899cc1499d66ae65b0797f`  
		Last Modified: Tue, 10 Mar 2026 01:51:34 GMT  
		Size: 5.3 MB (5250380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04221e81007d18d6372b2d773659dc106204f8a778c3ff4233f71f794e40d1a4`  
		Last Modified: Tue, 10 Mar 2026 01:51:32 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:fa8e9bf380c46c43a3d05e242d7a1d6d9826f2e90f93cb2520dde9086c48b1c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.9 MB (249928971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9bd48ae3b3d3e01f8d22d2d6a442b63ccdf8f1b49769e39af13278c2f583272`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 11:42:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 11:42:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 11:42:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:42:33 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 11:42:33 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 11:43:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 11:43:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 11:43:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 11:43:21 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 11:43:21 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2c02a3d3f135c4bbe56488921bd86d969a76dcd5278abca1e81884d3bff0bd88`  
		Last Modified: Mon, 16 Mar 2026 21:52:55 GMT  
		Size: 29.8 MB (29835265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f17a655283acfd5026e7bf35bfd3c21747c0f9fb4e21fa04b1ee69e7f604fe`  
		Last Modified: Tue, 17 Mar 2026 11:44:04 GMT  
		Size: 147.1 MB (147105214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7444815c2a14f4d585144d21d82693a2b598e39bbb6ecb3ef8c3f02890bba8`  
		Last Modified: Tue, 17 Mar 2026 11:44:03 GMT  
		Size: 73.0 MB (72987450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c984c1d1eece5326e0371e32eb33ebc4c6f739c424999e5f540775044506e4`  
		Last Modified: Tue, 17 Mar 2026 11:44:00 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead5e5961509af62670002203fd8cc3ad050062a52bd16ea7921f2a92ca799f2`  
		Last Modified: Tue, 17 Mar 2026 11:44:00 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bb4e25079f7540cb9f0304b74d8a7e607a127544688fd56290ffa9ff02252863
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17e0dc11ea0fb4141e56b7af1c1d1c84e1f2a78b95d48d3c2edd4f29359ec720`

```dockerfile
```

-	Layers:
	-	`sha256:b4d7093e28556a53eb9ffd3a014907a105b722e29575c19f6ec6cb6a929a40f6`  
		Last Modified: Tue, 17 Mar 2026 11:44:00 GMT  
		Size: 5.3 MB (5256914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16b7304ecc357089eab89ab4015bd7ccce581e357ee24ba1edc19ff20c9d719c`  
		Last Modified: Tue, 17 Mar 2026 11:44:00 GMT  
		Size: 15.8 KB (15811 bytes)  
		MIME: application/vnd.in-toto+json
