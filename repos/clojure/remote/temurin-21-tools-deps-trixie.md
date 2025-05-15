## `clojure:temurin-21-tools-deps-trixie`

```console
$ docker pull clojure@sha256:8aaefd665b4bb018b62341b2091ed54403dd4506ae5eaf9b177d4f5971b4493e
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

### `clojure:temurin-21-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:4a1d307fdaf6ff387c2bec11c3cc83c55aeac519141a8daea9097ae4554975fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.1 MB (292143989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2bcb5e4c87f8b652d90e7a6299526c35b164e0ed6b0b75c14f4f12886323644`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f8c8542523ef5c08ca9bd5ab7d7265d12930a45ccc7c8364e909fde03c894479`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 49.2 MB (49248239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c29560bcb0a94f49db0b99cdf4839c10a64961f9b16f2d4da6cf47de1a3cc5`  
		Last Modified: Tue, 13 May 2025 17:54:05 GMT  
		Size: 157.6 MB (157634543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e987d0d7bfd2d027f00d685bd1f7b713bb3f46c000763dea9a3b6e61983552ed`  
		Last Modified: Tue, 13 May 2025 17:54:04 GMT  
		Size: 85.3 MB (85260165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57ecda5f595b7e4fea0f906d21b1074c9392989f9b3c9ca858c1991477d4b15`  
		Last Modified: Tue, 13 May 2025 17:54:02 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3d0270decc297afb1ae61c57ebe9bae094988a9caf65404e2bcaa0527a1561`  
		Last Modified: Tue, 13 May 2025 17:54:02 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:efaa00caaa71c0c34b3db6cf5ab2a84a53aa890910043b36ca939306c4ffb4d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7289404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0561011948e806b36f8ca7796e780b8fe0845a300cf574901ae48b2c3fb4725c`

```dockerfile
```

-	Layers:
	-	`sha256:73a73f2a989c254d55bf990e91768ef9295f7b8d646bcbce3ce8dfbc5b81d8f0`  
		Last Modified: Tue, 13 May 2025 17:54:02 GMT  
		Size: 7.3 MB (7272939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af540f704c3f86cfae28faf901a0ff5848c3a2576a4385b01c1710f18fc68a1e`  
		Last Modified: Tue, 13 May 2025 17:54:02 GMT  
		Size: 16.5 KB (16465 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:af12fbb841e51b97c5dbae42a999457484829eb5ade8fd3547c9693658bd8737
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.7 MB (290726422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b02d5e8bc5806c52d8cc468a7f05d82f93e64f750496e2c01c7e7eae3616bb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:288a1cecb0ea762427d39b072c1ca965d193e927e04da652f7b21eb12e9b2acd`  
		Last Modified: Thu, 08 May 2025 17:11:50 GMT  
		Size: 49.6 MB (49624118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676c3e417baafaf8b730adc6d0f78dc3fa5bdbb2f54632cf85169f85047e3825`  
		Last Modified: Tue, 13 May 2025 18:04:24 GMT  
		Size: 155.9 MB (155928808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d1a01c6ad14d6ff0ffa6af0dc5d67dddc139e939d67b6e2723672993ab8debe`  
		Last Modified: Tue, 13 May 2025 18:06:37 GMT  
		Size: 85.2 MB (85172457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f9716b24e7995becaf5b62afd017d09ac2c1ed1ce9599acab5cd405cdc6b88`  
		Last Modified: Tue, 13 May 2025 18:06:35 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8769dd8d09e972edacf7d5e6219f401b4ff4aa0ce935d1fbea7e00886cbfe7cc`  
		Last Modified: Tue, 13 May 2025 18:06:34 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:26fa8e7b45ace23d6e48b2e93fcdec2c550fefad929b6368a7165ba263dc053a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7296600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b311074def9ebbd6bd231d961cac5da839534ae84799fcffd75025f5d3667e16`

```dockerfile
```

-	Layers:
	-	`sha256:6552a24acd51053818384e1a34d1100ad89af33906624b6f068242659ec6b337`  
		Last Modified: Tue, 13 May 2025 18:06:35 GMT  
		Size: 7.3 MB (7279993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f0304755cf1ff133a54a6bea45ab41a2da880ac70dce8e8552e0167da932a67`  
		Last Modified: Tue, 13 May 2025 18:06:34 GMT  
		Size: 16.6 KB (16607 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:a34dd8bf13f7e9c772a35f54904c2886132fcc77db202081988bbe382c5ab431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.6 MB (301620828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46dbc7ddc5a3a931481b096b8d79dac8ab5b6f0cc76661787e0b2dfd53acc230`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:03ebb30bb37cd398ea8ab1a268c301664089cf5a54d23466e4338782afb5f9cf`  
		Last Modified: Fri, 09 May 2025 00:28:48 GMT  
		Size: 53.1 MB (53072552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2151ad68f58c4cb07dda1a2a4084ab06210fce8cc616b99b367a4f681d8b98`  
		Last Modified: Tue, 13 May 2025 19:16:46 GMT  
		Size: 157.8 MB (157804906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1244fd0b92cb79324efdaa7304cfcc972af6d966e2471b0e29408c459ac6b0e7`  
		Last Modified: Tue, 13 May 2025 19:26:57 GMT  
		Size: 90.7 MB (90742325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e4ac494317edb5eb108af357379841999f38c9bce66303830167250c0bdb4a5`  
		Last Modified: Tue, 13 May 2025 19:26:55 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e01e012d6bece5b94a3191bcc4fa5a311c766c4cd3ad0bac52e6267dae42ce5`  
		Last Modified: Tue, 13 May 2025 19:26:54 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:856067f5af8c5826624563b16256da23b91bb2ff48e1e739a00c0424ed54c39a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7293729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:912f8c37ed31e80bbb751e8861d74153a835879200a4e6b3097ab64eb167c85b`

```dockerfile
```

-	Layers:
	-	`sha256:76efd912286cb10604e3cbceee249017004455d08875c21bcc129c716fea52d8`  
		Last Modified: Tue, 13 May 2025 19:26:55 GMT  
		Size: 7.3 MB (7277204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e221162ac93f6c3654273781c4f11a473e74145cb6f0d9247aec188e642448e`  
		Last Modified: Tue, 13 May 2025 19:26:54 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:a26c81561e632539b77354ba08eb3b97b0967c641ade1fc8a63a3a259005e6ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.4 MB (285409056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d921cf2b7cac483e7e836d42ef7faf1452d60dc1571de692affb8c84baa7a8d3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3e87a3ef7201dacec1e06fe511cdfaa924c5bf89f4f022c082b59ff14eb11b6f`  
		Last Modified: Fri, 09 May 2025 00:14:52 GMT  
		Size: 47.7 MB (47740349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ccf62f3ad8d617e1ef5406ae0b0907516d6df50cbc3bf027f91f580469e46d4`  
		Last Modified: Tue, 13 May 2025 18:51:48 GMT  
		Size: 153.4 MB (153449675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91897a124008c6d572275cae259a3b2d90475852f9806347668336ad9a9a9a88`  
		Last Modified: Tue, 13 May 2025 19:14:57 GMT  
		Size: 84.2 MB (84217993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc5e8984a8a59da0a796dd11a0378e15d4c9914f7213301f977ac8b97a16185`  
		Last Modified: Tue, 13 May 2025 19:14:45 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77712c3eea697bd4decb19a8df9dc1e3db053e47f664766aaaca1976817b261a`  
		Last Modified: Tue, 13 May 2025 19:14:45 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:0bbf58a180b73d9dc262b691f915ecc9c0ad985a9f6052d19492ac12797b456f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7277503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:924521665b0561e51b48154444ab52140309b744062875e6c4e912f677168a76`

```dockerfile
```

-	Layers:
	-	`sha256:28cbacf64e3d88e3551befae4740467706556216d5532ab1eafd79f3dcdc75d7`  
		Last Modified: Tue, 13 May 2025 19:14:46 GMT  
		Size: 7.3 MB (7260978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22173ffa98944469862d3d94bc42e7464540f0bcc9925d2f260e256efe0278e1`  
		Last Modified: Tue, 13 May 2025 19:14:45 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:21a956d80d070e7876c38f3a8f728b99d06b4300ebe0ed5440e35b2e49be75d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.6 MB (282568440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907cea39b6054bb8c736a31016bfbe97d6eadd70f8193d9fe81edad1adaeef83`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e1ec3b1570f7d822c5a6aa013529484429ad99bde8495d827b56c3603992fd3c`  
		Last Modified: Mon, 28 Apr 2025 21:11:06 GMT  
		Size: 49.3 MB (49316646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf9b80551764e2fcd3aa753ecb8619efb583086386c68987930a0db6a5f7b77`  
		Last Modified: Tue, 13 May 2025 18:25:17 GMT  
		Size: 146.9 MB (146910900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e01ae968ed96f074f91cf0a6c3677340cf523f8357be2ee81d98d2a6e2a683f`  
		Last Modified: Tue, 13 May 2025 18:31:38 GMT  
		Size: 86.3 MB (86339856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de6869e14b509bac6f60992d4de2d92e7c774d308531791741d24c4cb07e4e80`  
		Last Modified: Tue, 13 May 2025 18:31:35 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf4ce5e0b8208cc5961a78d6b4476b0f254980b27fc8c67f725ce2584163780`  
		Last Modified: Tue, 13 May 2025 18:31:35 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:14ce74107e43750417748f8ac8d32bc1fcc4ead57bbb23b08463f39a36606f83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7285326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a97852eb826770ae13d91e26495e55781bbc0ebd17412eddd6467dcacd2094d`

```dockerfile
```

-	Layers:
	-	`sha256:d0c1b9b28ce9d75918ed0b8b02e98e174d19c427849fe5aa0d8edb83ca041eb6`  
		Last Modified: Tue, 13 May 2025 18:31:36 GMT  
		Size: 7.3 MB (7268861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ea6121962da0412f115c9783ee041659119ca20b7fef9b70d0d5f3afe88718c`  
		Last Modified: Tue, 13 May 2025 18:31:35 GMT  
		Size: 16.5 KB (16465 bytes)  
		MIME: application/vnd.in-toto+json
