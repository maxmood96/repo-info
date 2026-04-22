## `clojure:tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:0a2f74db4717d4970afd27f4c6c0624913d94dd4cf128458ed13045f99a6f3f6
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

### `clojure:tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:de92536d9664a0ad4d4584dac20a7cf2f4832c53d42bd49837b03c5e4d8f8273
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.0 MB (194048611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08d9f6803469df1e550b0a18747009b5190d7689f9baee78b8e817a782a48000`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:21:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:21:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:21:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:21:18 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:21:18 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:21:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:21:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:21:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:21:33 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:21:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff6df917239d3e913de76112b94d5b95a2e5a9cc4a7aafe4c6d35a814487738`  
		Last Modified: Wed, 22 Apr 2026 02:21:58 GMT  
		Size: 92.3 MB (92256281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cfd251b2924617442dbb50ae70486f8146958db6ac70b5cbe9feab3ccde2d88`  
		Last Modified: Wed, 22 Apr 2026 02:21:53 GMT  
		Size: 72.0 MB (72011119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7380de37f0c97fdcc32911bee0448b0cdc3a81b202b3253854a62a07963cb1f7`  
		Last Modified: Wed, 22 Apr 2026 02:21:50 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdfcd4f2dec9ffcdfce26d00bd7b1497dd89b073b7c5260b0f91a34380ceb3b3`  
		Last Modified: Wed, 22 Apr 2026 02:21:50 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c7669265bfb333d47bc0c8b4b5e0dc92428045ff6484e7e53647ea501d8a733f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5243771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c6205fd0989da962345b1c7faba01028977082e6249b27af7bd7d974dabe302`

```dockerfile
```

-	Layers:
	-	`sha256:dac73ba0d168699ad1c7bffd5916a055049b9808b24b7bec2de1b670b0df28bd`  
		Last Modified: Wed, 22 Apr 2026 02:21:50 GMT  
		Size: 5.2 MB (5227278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bc678704f4b0b12a449bccfad1a74e3f03314dde64ff135d0a3cbae76144e8c`  
		Last Modified: Wed, 22 Apr 2026 02:21:49 GMT  
		Size: 16.5 KB (16493 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3aec900e7ba2216d5a88dca01400b2fb524bd957bfac0a7639662540e278e248
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.3 MB (193264483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef4c7b5bcad86d4fb87a19043222361254c530a1ff227102e88d9e845ba9de2d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:45:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 01:45:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 01:45:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 01:45:06 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:24:21 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:24:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:24:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:24:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:24:39 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:24:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3214779e4c6a83f50c16481d42d1e2a6c2802bcae47f725dd458bbb3493a5ef5`  
		Last Modified: Wed, 22 Apr 2026 01:46:03 GMT  
		Size: 91.3 MB (91288309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1a31425f16cb592661b576e8de7c1419913c85bb0a018c8bf2e05b6f285178`  
		Last Modified: Wed, 22 Apr 2026 02:24:56 GMT  
		Size: 71.8 MB (71831527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb08efa56da6ae06c49e2c0659d914d369ab16cbcad74185d77eb026155ef4c2`  
		Last Modified: Wed, 22 Apr 2026 02:24:54 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd562fdc0d84039c80f85d6f2c25ad77cea348b4ae074182ef7131a2c4f56c4c`  
		Last Modified: Wed, 22 Apr 2026 02:24:54 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:164f45b9a9b2744b3e9ea4230c9a49e186c3e3080a5d0b88349b5202d79aa95a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5248903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:154f3aec3a712bcfbfd1048d935234cebc8b72a5435c9c8ccada7f1072fae48e`

```dockerfile
```

-	Layers:
	-	`sha256:9f7cf8c7a2cc2bcd4902edee10d3d3ab668d9d4fe652b3195412ba3603368756`  
		Last Modified: Wed, 22 Apr 2026 02:24:54 GMT  
		Size: 5.2 MB (5233068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d26b625029b240e3ea4fd3ffa79534778343ae8b678858586f0c7e8f656faeb`  
		Last Modified: Wed, 22 Apr 2026 02:24:54 GMT  
		Size: 15.8 KB (15835 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:f0fc798805eeed1ee2caf1a8790d15d9358ad9a491fd9f9ce7d8c1feb3fab55a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.8 MB (205837450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49b12ec0d06a3feffff1ead576cdbffcf3a2d414e69306bb7aebadffa1ef7851`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Thu, 16 Apr 2026 03:10:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 03:10:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 03:10:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 03:10:40 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 03:10:40 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 03:14:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 03:14:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 03:14:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 03:14:43 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 03:14:43 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba6211d0df66bd290a2d3cf64be5f95fba6a6de737b3a8c7f0f2b2200d8bc06f`  
		Last Modified: Thu, 16 Apr 2026 03:12:00 GMT  
		Size: 91.6 MB (91632998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aca4eca3b68cbf03a9b2bd758c7d854a2afec002c9a63934a7a97e54d1f25d8`  
		Last Modified: Thu, 16 Apr 2026 03:15:18 GMT  
		Size: 80.6 MB (80610389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f9eee3be22b464799db414a84fc9b82394e86da286105f7c8ca1e097eb3bd0`  
		Last Modified: Thu, 16 Apr 2026 03:15:15 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5ee8aa5f40842559634c1c8d9d2f9f3e72a255d2b46e68ddddcd1ef7892156c`  
		Last Modified: Thu, 16 Apr 2026 03:15:15 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3e632b8e6fd8783d24aab03d0c2703547fcdf437d688aba430e95a44fddcd763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5231472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:190d62871b7c305c6d2c04c60538c60ad31b4d82edd17596280cb88ce7167699`

```dockerfile
```

-	Layers:
	-	`sha256:4207a8c686ce4b33491ef1e3cde02000279b817f147b4c821120c53de980e600`  
		Last Modified: Thu, 16 Apr 2026 03:15:16 GMT  
		Size: 5.2 MB (5214919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b6009471ab40bfc7f626136c1c5f116230f489b83470ff42fc1fec3bdd4df84`  
		Last Modified: Thu, 16 Apr 2026 03:15:15 GMT  
		Size: 16.6 KB (16553 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:e5e0ee91cfa5e3ad4e7680742f4f581bce8c7558096d7449ee3dae4a5ff4065d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.6 MB (192569091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f691976ae08eed150d0d26ceedf3010ef3383cd31e31f60e1d2d186587a2434e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Sat, 11 Apr 2026 22:39:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 11 Apr 2026 22:39:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 11 Apr 2026 22:39:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Apr 2026 22:39:28 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Sat, 18 Apr 2026 05:24:42 GMT
WORKDIR /tmp
# Sat, 18 Apr 2026 05:45:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 18 Apr 2026 05:45:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 18 Apr 2026 05:45:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 18 Apr 2026 05:45:37 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 18 Apr 2026 05:45:37 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94187439743d0e4ea744bbf1c65c89e279a7b6b83ff5e8684b3251e143001c79`  
		Last Modified: Sat, 11 Apr 2026 22:44:45 GMT  
		Size: 90.8 MB (90773426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9936fd95725d24601fc401372cf26187ddd0ffe17d88af944ed5699adea3e4af`  
		Last Modified: Sat, 18 Apr 2026 05:49:16 GMT  
		Size: 73.5 MB (73518842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4fe0e011e2eacd8bd28f3c523ccea9bef77b1776eae578460581cdfb7e3e65`  
		Last Modified: Sat, 18 Apr 2026 05:49:05 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d12eba6178169a3c767b2ff096980b2cf211f96c19f930fe05ac76367ea951a`  
		Last Modified: Sat, 18 Apr 2026 05:49:05 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d591498fc04f7cf75d3208cb2b8e5f4acaa2de69ca72461077ebf354b1408137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5215264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:879143a48a3aa2b022d84a30e3f6a8350dc12e8af1ff5c469c2069d0cf91ebe1`

```dockerfile
```

-	Layers:
	-	`sha256:d0b75ad881724230be3ee5f26f571a09401c8df2dcd2a274046b1264c4c3e96a`  
		Last Modified: Sat, 18 Apr 2026 05:49:06 GMT  
		Size: 5.2 MB (5198711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7e6e524a02fcd3f958c6f5f1f761ccdd1150d3a36274c3e50844f38532889d1`  
		Last Modified: Sat, 18 Apr 2026 05:49:05 GMT  
		Size: 16.6 KB (16553 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:ca8088305435860f3a5c24015056dc6a0f2ed903f63744336e2cef039efc5ba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.7 MB (193669091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:859b14ab5e5025f953704af6439f99812b76dd5e677ad23fe5614974aa564b7b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Thu, 16 Apr 2026 00:45:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 00:45:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 00:45:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 00:45:44 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 00:45:44 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 00:46:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 00:46:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 00:46:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 00:46:01 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 00:46:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb362cb03216b959febd5e7567d524805fb46e649e271e2b623df3ab0d755a9f`  
		Last Modified: Thu, 16 Apr 2026 00:46:29 GMT  
		Size: 88.2 MB (88233835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1cf27d09061ed701b7e9d1b8c5c657101c7c030cac4a869c710ab8ddcd73a05`  
		Last Modified: Thu, 16 Apr 2026 00:46:28 GMT  
		Size: 75.6 MB (75598793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cde61be10525926e3904b60966569bf0dcc0c15b7df6a67bc313e4c20cc26b30`  
		Last Modified: Thu, 16 Apr 2026 00:46:26 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6efc458dbdabe87ccbeed957e531220612cbb443c20f097c75e0f481bff3bab9`  
		Last Modified: Thu, 16 Apr 2026 00:46:26 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0d05a4a7e82fb886ce5ed052ee414d9c5ace0b620dc7eb49a32d6f0cbffa94b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5224203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7844841470acbd952b1b529e7a8a3004291e2e81e5f4386854c47306e7909c30`

```dockerfile
```

-	Layers:
	-	`sha256:b86cd983c56ed4d2b1da325eff9995e0cfce19705d947c815b6a815d4f487835`  
		Last Modified: Thu, 16 Apr 2026 00:46:26 GMT  
		Size: 5.2 MB (5207710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fe3066c7efe9b0c74086d1e4289648841e431f5becdd385e59fc22ac387b3ba`  
		Last Modified: Thu, 16 Apr 2026 00:46:26 GMT  
		Size: 16.5 KB (16493 bytes)  
		MIME: application/vnd.in-toto+json
