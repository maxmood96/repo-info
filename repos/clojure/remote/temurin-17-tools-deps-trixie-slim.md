## `clojure:temurin-17-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:9f105343cf0c929eb25bc225466415129ce8c660c1fc1123facbdc0b94d8133e
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

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:fc4958a25d2283d8f137405d0ca2247fb4e611abc9cae79741733e823a0aac52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.4 MB (247417149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba702e2bc76e77d0a2b4af72659c299a8c7ac1b5ec2d99002673d2f3045d015b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 02:59:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:59:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:59:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:59:06 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 02:59:06 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 02:59:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 02:59:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 02:59:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 02:59:23 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 02:59:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c67ca49d06408f18b7610de7d98d21ca6ef194852db3ddaba232ea54cceb33`  
		Last Modified: Tue, 17 Mar 2026 02:59:44 GMT  
		Size: 145.6 MB (145628437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d1c646f32ba1fe2ab4b4253b680e541543c302f154bd9ca30dd51c047bf88ef`  
		Last Modified: Tue, 17 Mar 2026 02:59:43 GMT  
		Size: 72.0 MB (72012169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab7fa2211794e414afecbf15b3114101d6e8ddc187c27de688449acb6438977`  
		Last Modified: Tue, 17 Mar 2026 02:59:40 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e66d91b09d754004acfa318acbdbb5aef77b6707c9a50214441c6d1ca1c64a1`  
		Last Modified: Tue, 17 Mar 2026 02:59:40 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b3e1eeb9fcc0100d1ee0fe20caac87b95d1e15ea9d4e0afe84d772d52c955c29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5274950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec53f4ac8676265b6219a5bb19be8830cb3281e9bf86c37436028b5d8383f888`

```dockerfile
```

-	Layers:
	-	`sha256:1f2262e39531624bf65ee9f061f20f66208d22e09de4143bf633affa4bbd6c50`  
		Last Modified: Tue, 17 Mar 2026 02:59:41 GMT  
		Size: 5.3 MB (5259138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f45f7f8ffbd2d2a012042e30c0bcca9a4a4ff42b1d03a52cf4eb121cc4120d66`  
		Last Modified: Tue, 17 Mar 2026 02:59:40 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:349d0dc4de703f323ac7c9050e4e73f48916b5b398d90c1dc9286af1e9f87afd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246407136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66035f3b2069264e44ba772f3a1c31d178702782e07ee3c7b599e20dba9a138d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 03:03:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:03:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:03:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:03:31 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 03:03:31 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:03:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 03:03:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 03:03:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:03:50 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:03:50 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8f3a4c0c3f34019f959f46a63dc8a0a0b6ca3c47812fb4fa74c6b0a1ea69c0`  
		Last Modified: Tue, 17 Mar 2026 03:04:14 GMT  
		Size: 144.4 MB (144436242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac94772eac91fa5ec27ffd4edf90614974b9597db0594f1721ec6b45481ab93`  
		Last Modified: Tue, 17 Mar 2026 03:04:12 GMT  
		Size: 71.8 MB (71831436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff2454be88365e215cf461282a126956d96f142b95bfc2c824d410affc0bdc2`  
		Last Modified: Tue, 17 Mar 2026 03:04:09 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed28b0170b1c48b3746e03782906a5cc39b989e2fd783fc0258521a672f7352`  
		Last Modified: Tue, 17 Mar 2026 03:04:09 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a0f5d8d6f8f2df44fd07547b533d69a31a7a563d063f7f5130da849d8726d5bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5280837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8706c4ece8428b84af424146d26da35f41f31df2fdcd89f220514643708c72a6`

```dockerfile
```

-	Layers:
	-	`sha256:cbd90c4dc476fa9ba4d1ca3eaa2b2425a276e51a01839915a6c23fbdfe8e742a`  
		Last Modified: Tue, 17 Mar 2026 03:04:10 GMT  
		Size: 5.3 MB (5264907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78db06f9b2df47ea8ecaac5e9034fb5d81e398dff58f8c60b98c039e88bdaa84`  
		Last Modified: Tue, 17 Mar 2026 03:04:09 GMT  
		Size: 15.9 KB (15930 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:2e1a5798362b61b96206f5553a9f4b54d832841988acd7cf8300b80577164fb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.5 MB (256467908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4199b3d34bb37fbd91e5c34e5b384e0545abf877a2fe7d78a48cc7b92b05a3cb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 20:54:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:54:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:54:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:54:24 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:54:26 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:55:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:55:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:55:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:55:22 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:55:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa68eefccf52feae213c365bd35426d2716c52016a1ead8472aed0ffcacc64c0`  
		Last Modified: Mon, 09 Mar 2026 20:56:25 GMT  
		Size: 145.4 MB (145438177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587856f591158bc38270af110a8379d96cc7b3b21e614ebc330170c471900890`  
		Last Modified: Mon, 09 Mar 2026 20:56:23 GMT  
		Size: 77.4 MB (77428470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2624131e6edda69fdb1c0da34b4f76f44622538d4daf33a10b24eef293f5852`  
		Last Modified: Mon, 09 Mar 2026 20:56:20 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b3d6e3b13873ceac723c821fffd021fd2ab75c82f2ca779daf8d4b043c99a3`  
		Last Modified: Mon, 09 Mar 2026 20:56:20 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:eefda0cd7e7b88a6a05d407e888fbcca8d34b41768e3d146a5881ed5f126d17f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21f044cdebe604bb8dc19983fec5ae52356e2a965f4d84d0f8f4633be887fa41`

```dockerfile
```

-	Layers:
	-	`sha256:c6717c3a99ab55f148d36db08023826ac412a29cab8533afa41b5a936087a8ec`  
		Last Modified: Mon, 09 Mar 2026 20:56:20 GMT  
		Size: 5.3 MB (5263435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c3d11e84d1b77fed7f9df1b912635d73cc03ea8057b5d8007eade1f8c1cac76`  
		Last Modified: Mon, 09 Mar 2026 20:56:20 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:140ef8d1df99b4d67c4c12034d21850ab1d132ba328e33bfa329f4c74a3d908c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.8 MB (241839875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b172fef56a514e0e351720845bbc07548784edc000ac43abc152bfd3a80350ff`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 11:00:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 11:00:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 11:00:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 11:00:22 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 04 Mar 2026 11:00:22 GMT
WORKDIR /tmp
# Tue, 10 Mar 2026 01:22:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 10 Mar 2026 01:22:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 10 Mar 2026 01:22:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 10 Mar 2026 01:22:38 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 10 Mar 2026 01:22:38 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c563a7e83c0073076553db10b62cc19d4a3173b8d64e403513851f43436892cd`  
		Last Modified: Wed, 04 Mar 2026 11:07:48 GMT  
		Size: 142.7 MB (142662998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b58515c07c141fb6e96cd063edc195cc847d4c9f22f75c1365bab5a6522d5ec`  
		Last Modified: Tue, 10 Mar 2026 01:27:13 GMT  
		Size: 70.9 MB (70899418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e4bd5a2c572545210dcbd2e226cbdb798ec06b406fd4c7974c8fa19acd35f54`  
		Last Modified: Tue, 10 Mar 2026 01:27:01 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6780e0d7a7c26ca1f37b52e72001eda6b1a047dd6f257b5539bf58826237a7`  
		Last Modified: Tue, 10 Mar 2026 01:27:01 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:debfece0c168d0090ae686ce4d63c9eeaa5053a5241795c280880f44dc85c0ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5262469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d4e3040eb17fc7a8619d9f3775064f1d46e0829d958ff18f0a38d33c49b7aac`

```dockerfile
```

-	Layers:
	-	`sha256:a17bf42d0be9794ff5b55d49159d76c29f2a4d3a0c96b2fe4c082444d02720f4`  
		Last Modified: Tue, 10 Mar 2026 01:27:02 GMT  
		Size: 5.2 MB (5246609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa2eacbae838643061745a2a305316531bbf04e471b1f0057f5b262307d68981`  
		Last Modified: Tue, 10 Mar 2026 01:27:00 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:9bbdcf1bb44ddabe56be11256fd95b89c84fcb97f193de317261f59856a18579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.4 MB (238449983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71e6d8675deb961ba9f3dc10b8a246135afe5555f4badc014ac442752e7817db`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 11:38:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 11:38:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 11:38:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:38:14 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 11:38:14 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 11:38:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 11:38:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 11:38:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 11:38:50 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 11:38:50 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2c02a3d3f135c4bbe56488921bd86d969a76dcd5278abca1e81884d3bff0bd88`  
		Last Modified: Mon, 16 Mar 2026 21:52:55 GMT  
		Size: 29.8 MB (29835265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0e873883d06c3d66937d1b59b9c75c3451b6c0508819963b4679d67d56b74c`  
		Last Modified: Tue, 17 Mar 2026 11:39:29 GMT  
		Size: 135.6 MB (135626794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ac26bb03b22f8511a7da5076629048b6b228cc71ee703b02436d8bf8bf8aba`  
		Last Modified: Tue, 17 Mar 2026 11:39:27 GMT  
		Size: 73.0 MB (72986882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b2646cac42d8b0ad9227aed208fc5ed77776afa0a3430617e796742501036f`  
		Last Modified: Tue, 17 Mar 2026 11:39:25 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5e64ef8de8a710b31b8a902808498a52c8fdbc0f77b0cbdd260a5aeb78e40c`  
		Last Modified: Tue, 17 Mar 2026 11:39:25 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0e76ab769195d720a30a8fd0457f0d2cfb9accb4e750a14e0e94e4d93aba5333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5270873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1da1b1de18568674366a1a1ff16224602d5a746bb17f0f6774bc6b8c1b093768`

```dockerfile
```

-	Layers:
	-	`sha256:03b02d8070cfd8ed4b8829cc06e16825d1f20f8b83404d8620090fb62d9553d6`  
		Last Modified: Tue, 17 Mar 2026 11:39:25 GMT  
		Size: 5.3 MB (5255062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfd6a1da98f6aeb3ac88b5f6fcf3d3163a6b665e938faa4bf1a54c445bef605a`  
		Last Modified: Tue, 17 Mar 2026 11:39:25 GMT  
		Size: 15.8 KB (15811 bytes)  
		MIME: application/vnd.in-toto+json
