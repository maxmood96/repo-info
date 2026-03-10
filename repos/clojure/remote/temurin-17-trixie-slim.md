## `clojure:temurin-17-trixie-slim`

```console
$ docker pull clojure@sha256:cb8f51aa4021b3416ed6d87bf55bdb3010846169143280ef20dfa73b9831a9c4
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

### `clojure:temurin-17-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:47d9a066c6666e6291c5080cc4039e2fad119aa804457b2da4a7df2cdf45dd7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.4 MB (247423277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:094d5d241047c6432039c6e557172adfd82fe87e5f10c0ff33e9a76514f2f4f7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 20:35:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:35:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:35:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:35:29 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:35:29 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:35:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:35:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:35:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:35:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:35:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f607399025d1f52f6029b73c00942e5162af60579b65bebb2e5d45ae710cf87d`  
		Last Modified: Mon, 09 Mar 2026 20:36:09 GMT  
		Size: 145.6 MB (145628711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50f32cdc47387a0fb39065ee15e1ee02f48138a88a83d5f329b78e01039c767`  
		Last Modified: Mon, 09 Mar 2026 20:36:07 GMT  
		Size: 72.0 MB (72014895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8487c4eed39644326453f8fbfd8bcb08a9665ae6c690728d1635ac1de8207c4d`  
		Last Modified: Mon, 09 Mar 2026 20:36:04 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c48ae58805ec03ac2c67233660901118584d49e0d743bbe79ec351c54c4054`  
		Last Modified: Mon, 09 Mar 2026 20:36:04 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d9ab3c8c25452fbdacc007b457c9a6a1a158eb7f53d8c62276a88f67942ad36f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5274876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb159958952080ec1f4092131399579c849d14aeb041ea12917b3cf823eab21`

```dockerfile
```

-	Layers:
	-	`sha256:d11b223df69e1494fa07fb4fd11f6b17b354cec5bc542f2abfb253726812749b`  
		Last Modified: Mon, 09 Mar 2026 20:36:04 GMT  
		Size: 5.3 MB (5259064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0be0670838a0a148f6cc8aea9862e91d7302962fd74f8b5dea88882e8980317d`  
		Last Modified: Mon, 09 Mar 2026 20:36:04 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:278ec2f7821b79127a4be67178ab920de9e6c18e9f82adce423fef58854059ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246409586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efc987f77d2fd16e9d58cc5368a2847752c31a1e7a23550471d8f47c2ddb1869`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 20:35:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:35:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:35:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:35:26 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:35:26 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:35:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:35:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:35:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:35:44 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:35:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559d20ee292f1585fe8c853eb84e11591b79b0074d54c1897f6b3ef9f00d9ed3`  
		Last Modified: Mon, 09 Mar 2026 20:36:05 GMT  
		Size: 144.4 MB (144436243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f446ef58f4833973de8ade83684baa910d5004e40787ebff75fd48397bee68b3`  
		Last Modified: Mon, 09 Mar 2026 20:36:04 GMT  
		Size: 71.8 MB (71832205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac32b80e97e4936d73df4c37597b2b5214523081c2b451f5a6b22df6a8dcdac`  
		Last Modified: Mon, 09 Mar 2026 20:36:01 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c132c7bba82582ea60187b0e0b7e19f95fdb3ccdf9d653c6de7798e07c7ccd7`  
		Last Modified: Mon, 09 Mar 2026 20:36:01 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0bd43637129a3d3c9c19dec0c725bc90263964a278bdee970f137bfc05c1ac31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5280763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d080d63b00a79b0dbb013362eccd76eb0c9dfd7cfbec77a40260cc0e63abb97`

```dockerfile
```

-	Layers:
	-	`sha256:50cb914b7b317924378271bf6ced83f1e2962bac92d9fc00886858b30735076b`  
		Last Modified: Mon, 09 Mar 2026 20:36:01 GMT  
		Size: 5.3 MB (5264833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d151df4a71fbb22dad2ccee73d6399f2cb21a54d62278a6244141a6a8616e75`  
		Last Modified: Mon, 09 Mar 2026 20:36:01 GMT  
		Size: 15.9 KB (15930 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; ppc64le

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

### `clojure:temurin-17-trixie-slim` - unknown; unknown

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

### `clojure:temurin-17-trixie-slim` - linux; riscv64

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

### `clojure:temurin-17-trixie-slim` - unknown; unknown

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

### `clojure:temurin-17-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:e954b1395dab0b50a0c0dfd6fd3740e118668809ddc248b698afa45326f174f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.5 MB (238450004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd3d3540ddb84eef7b4d8dfd545cc35395e5e92c1d4a1b844143b5f26ce27529`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 20:35:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:35:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:35:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:35:31 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:35:31 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:35:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:35:47 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:35:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:35:47 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:35:47 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8452513ca949f8424d5152c476196f53b10bd68f5bacd27ba8cb997eb0f4cd`  
		Last Modified: Mon, 09 Mar 2026 20:36:17 GMT  
		Size: 135.6 MB (135627117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a58f992b9ef7c10e5943efdb1e3938b023970a0c043772c42a064bd4ec59425`  
		Last Modified: Mon, 09 Mar 2026 20:36:15 GMT  
		Size: 73.0 MB (72983666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d1e2b902d10d7b1ad5ef5584611caea6eddf8ab2eef3e471239b34ff0b2851`  
		Last Modified: Mon, 09 Mar 2026 20:36:13 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0aa629bfd98f1f4e565fca4e54d9dd9c08195ff493cb7cfa5eabbbda07513e`  
		Last Modified: Mon, 09 Mar 2026 20:36:13 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d5648bb936e06e410bdef310e0290de5f8a4c6a74ac83f134b1dea72412847d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5270800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d3c8bf87bc32bcf7171cd4187d3780d148845beb74a375a13d769eb60cb1f77`

```dockerfile
```

-	Layers:
	-	`sha256:34d674b315ec3510b1ff4f96d7f8abd602cca1a38c8899600d5f98bbdc40e8b5`  
		Last Modified: Mon, 09 Mar 2026 20:36:13 GMT  
		Size: 5.3 MB (5254988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d65b3461e302bfd2c30bdee0ab66b8e1d7856deec8a7debbb4cdd7565e864038`  
		Last Modified: Mon, 09 Mar 2026 20:36:13 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json
