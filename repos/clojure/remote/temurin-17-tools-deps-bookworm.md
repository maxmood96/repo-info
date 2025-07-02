## `clojure:temurin-17-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:c50ad5688a4715205b6dfde67b51a3ef4c781c712a55bc4bf415771f30b17447
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

### `clojure:temurin-17-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:cc4dc857334e8eda110c3ccb16266f2259d784ed8e295dcdb5ee74fd231221e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.1 MB (274123397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95578848b936fb42325d6b18d1375f2c5c4a5caf3898f857b1484c4f68cd4fe2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed96396b24255cadce6240e231e31609b7786c8502dcb580469b7f35d24c158f`  
		Last Modified: Wed, 02 Jul 2025 04:16:40 GMT  
		Size: 144.6 MB (144635025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e78d23a46ad5bb920dcb7c1a0b5b4a8cc9e45e0c93e9a1ae595658fcb2974ad`  
		Last Modified: Wed, 02 Jul 2025 04:17:10 GMT  
		Size: 81.0 MB (80993045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02e5a593723dcfdba0dfcb30ba03c104622162174856c375bd57a19286b63df`  
		Last Modified: Wed, 02 Jul 2025 04:16:38 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fca5d0b66bd0015dcad9f87ce1a4572a16c9849adbe9067789deabe0cad45f0`  
		Last Modified: Wed, 02 Jul 2025 04:16:38 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f53afc3be49edd7876eaff0c601edcd24405a94053427dbd2066f4023f4866c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7384089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87de1b8a9839eb609ecb4fc39464e123c7c0ccfdaa63e857122b146fd4822ce3`

```dockerfile
```

-	Layers:
	-	`sha256:ac14263d97e629de7fdcb1c2cda39467eab781fce7357e3f3153ed00f51bd88a`  
		Last Modified: Wed, 02 Jul 2025 06:37:10 GMT  
		Size: 7.4 MB (7368268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:baff5dc9c93a40a5396fdce4ed0d68918fc1a4e4d216df9cba28866b4dc5ab73`  
		Last Modified: Wed, 02 Jul 2025 06:37:11 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:937947a78b23154ea11f5c400299fc568262b36b95fd971e979aedf364803d14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.7 MB (272704456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2af7b6cd54a6c4f68a6a9bac6e63a313d0a036a44d6ce934a1a9199424612637`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1f8ab7c4e8b4178f5f2504f6c4b199268151b1fc958cd53bb861d8dbd9faa8c3`  
		Last Modified: Tue, 01 Jul 2025 01:15:08 GMT  
		Size: 48.3 MB (48338785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a58b74b351f1a626d14153bd13df5f52eaca6b7b23f4ae06890adf7033c6d9e`  
		Last Modified: Wed, 02 Jul 2025 03:41:09 GMT  
		Size: 143.5 MB (143512615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a47dc690943a83e4c82a580c146337b8441885f04ee359fd3e8e9faaf517819`  
		Last Modified: Tue, 01 Jul 2025 12:23:50 GMT  
		Size: 80.9 MB (80852017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae67ec25e37513aa62d45307d0fb2a3fe7028003d11be90d1b1a930fae411c9a`  
		Last Modified: Tue, 01 Jul 2025 12:23:42 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d9998eab460a02c1bf679734c52586daa1acd0088461dc13d7e4982053186d`  
		Last Modified: Tue, 01 Jul 2025 12:23:43 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:0822c5aa64238a84858b79b1ab152d9435e79bfd99951ddf2790af2971818805
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7389970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e5216b88773140bb410e5e811413918a80cdae49e26f79323eca809db16f71f`

```dockerfile
```

-	Layers:
	-	`sha256:5f602ed8d74a67dfbc2e9a7ac859099a47190dd98bd5b0aa7e03f5287bbcd6aa`  
		Last Modified: Tue, 01 Jul 2025 15:36:36 GMT  
		Size: 7.4 MB (7374031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac8cd7c1684a2bc28e97686bceae2af4f7791bf5dcff8cd5fb53016d8b8b73f0`  
		Last Modified: Tue, 01 Jul 2025 15:36:37 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:ca6edd601338825e625e5d3e77532e74d126dec616f05c359dc3082b73f0744e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.4 MB (283438548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c39df04465132a0dc3776c1fa77fafb00c926d27bc8ea25f8f1834b3f54850f7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2819217d87219cbf8b5ec7dfbc47c9a16195c7992a9fbe92da8723c42180b19b`  
		Last Modified: Tue, 01 Jul 2025 01:15:05 GMT  
		Size: 52.3 MB (52337243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a0ea4b882af434d42baa78fc13182c3a0199b5d594cadfa32f9327ef20526df`  
		Last Modified: Tue, 01 Jul 2025 13:31:29 GMT  
		Size: 144.3 MB (144280581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284618a6436e8bbd703c261050d98b9e81d1665747803d3262165edb7351f522`  
		Last Modified: Tue, 01 Jul 2025 13:31:50 GMT  
		Size: 86.8 MB (86819683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0843a9d902868ec208cd0c2603362a1806b220f0ee743aaf3400c88053e5f114`  
		Last Modified: Tue, 01 Jul 2025 08:49:27 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b120ad3fea26833ba30438c445d6b0e56f7602392103b3a6bc4f330c5ae44d0`  
		Last Modified: Tue, 01 Jul 2025 08:49:28 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c4c8d71523a81e4ef12c61eb898398dae91dac1281d87b6d0317a6222227132f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7389341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16f32871ca1efb0f89117bd44701d9fd1ee46b78b212ab9a5a3c74abf58eb133`

```dockerfile
```

-	Layers:
	-	`sha256:cb6b6a8277642841167c138da5697ff8312f93c0c540aa2ff246aecd7f328f71`  
		Last Modified: Tue, 01 Jul 2025 09:37:16 GMT  
		Size: 7.4 MB (7373472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:146e6e696da319399471d66238f4b0b1251b03944bd176d349f6678c5f0464a0`  
		Last Modified: Tue, 01 Jul 2025 09:37:17 GMT  
		Size: 15.9 KB (15869 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:a7cad4215f7529fb2ec4084ce355a40c8cd87db43d9653b75e3e0a6f53d469fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.6 MB (261623444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fab161b2d2c63896fc4a58fc06c83d3cd827ddb68c0bfc1b3ac66c51af5c05c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f5e945529523ccd9610b7c0253cda59a29c297f0a697f3c402695e1c6ecf5e6c`  
		Last Modified: Tue, 01 Jul 2025 01:15:47 GMT  
		Size: 47.1 MB (47149287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109b6103eea7647ec4468d79df7063299de38b8cf13abe06fcd434a70d2ee5c8`  
		Last Modified: Tue, 01 Jul 2025 13:31:28 GMT  
		Size: 134.7 MB (134673550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ecb9c88a9641c14bae8e408c1c21b95307e8375db46debc454cb3b71902fae2`  
		Last Modified: Tue, 01 Jul 2025 08:14:32 GMT  
		Size: 79.8 MB (79799569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a482345e587111875f0bcaa071e3445e4b0696a039ce983a71560f642e7c8e0d`  
		Last Modified: Tue, 01 Jul 2025 08:14:32 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfda24dbb65667b42d5c4cf2f74b4c4b8e9f5e5f41223f5c116fcb3ac1c49be2`  
		Last Modified: Tue, 01 Jul 2025 08:14:20 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:e072fbab492e11325014d324d8916895f0c2e899da2b636dfb29097296545e12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7375408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e72ec1f963de6af2bf0fb3145a1a58ae9e6c6387afd0748ac0e748f574eeeac3`

```dockerfile
```

-	Layers:
	-	`sha256:21b78f0c8d83c1edde5ab32749c8e74444a649b24415c2dc268a4b5e2173028a`  
		Last Modified: Tue, 01 Jul 2025 09:37:23 GMT  
		Size: 7.4 MB (7359587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:849440634fcf0b105288f74fd17d78603a97d03e9ab923ec21cb2a65a3735838`  
		Last Modified: Tue, 01 Jul 2025 09:37:24 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json
