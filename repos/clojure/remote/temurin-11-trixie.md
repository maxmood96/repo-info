## `clojure:temurin-11-trixie`

```console
$ docker pull clojure@sha256:5955d0390a4a93c4c193851d8ad7b90eb9cd55b34250bdbb9f9bdd4ab769180e
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

### `clojure:temurin-11-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:422b03b6917d9d367f1d106cda2648e42ec94eed614ffb358c1783f890f67817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.7 MB (277723037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23923553c33d1a61ed288798d780098019952e92a97f67c4ded68878e3255fe6`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:16:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:16:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:16:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:16:41 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:16:41 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:16:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:16:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:16:56 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ef1b08ddd59d42b444e8f9c68a6cebbed70636aed0c242fdccb0bd61b61ba26b`  
		Last Modified: Wed, 10 Jun 2026 23:40:27 GMT  
		Size: 49.3 MB (49317121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd2500507b433d71b98033a2875fd2d63ecd32fa2913abc9a56a579f5016f2e`  
		Last Modified: Fri, 19 Jun 2026 02:17:15 GMT  
		Size: 145.9 MB (145886183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841098351530bdf7424f2ddcf84ecc0166f1b1f60e7ee2bd255cd939e1644462`  
		Last Modified: Fri, 19 Jun 2026 02:17:18 GMT  
		Size: 82.5 MB (82519091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba2322b6d33e7fd8674b566e609f4fcc1abfbb9a4479252e6c3cb2e2ea13f14`  
		Last Modified: Fri, 19 Jun 2026 02:17:15 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:94e649d22e69d0598e3b07acf56c97cacbf1045c5ba5b0368a32d6d1c14afa98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7502626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dbbaa7973413094c843b5576eb1bcbf03c53f4c81231afed0670a5399325a84`

```dockerfile
```

-	Layers:
	-	`sha256:533c43f4102c0c6e2157ff26bcbfbeca2415bec5a42f971752b025ab41d4f0db`  
		Last Modified: Fri, 19 Jun 2026 02:17:15 GMT  
		Size: 7.5 MB (7488287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ed62a28399c976fa65a16ed9f7ead0fd7227fbf4438041b3bdc34b4d51f8658`  
		Last Modified: Fri, 19 Jun 2026 02:17:15 GMT  
		Size: 14.3 KB (14339 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:21d260fbabb1ae54bad20d5a00e40540b66088026243a87c288b07bf29103a08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.6 MB (274599439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73094227ec54a1ef53b23d33e3fea0d6ff17458180b3fcd3eb9c78d09c2ec61c`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:16:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:16:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:16:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:16:41 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:16:41 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:16:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:16:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:16:59 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ed660e1af0f5da9e93a4c43fb29e86cb46fe69c76bcf11a3de9c57c987acab82`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 49.7 MB (49678169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8c39feca3865a2fa9dc46620f3b22967e70c420d2eb174c18866d9a097d214`  
		Last Modified: Fri, 19 Jun 2026 02:17:22 GMT  
		Size: 142.6 MB (142582166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51911220a249f93e0c1b5526ed2cfaf4dbed2e6fd421529ed233f3c1806c8409`  
		Last Modified: Fri, 19 Jun 2026 02:17:21 GMT  
		Size: 82.3 MB (82338462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d092e8807c1c20ab70c965843fa5ec43003d36ce80d55279dfd318f0a1a991f8`  
		Last Modified: Fri, 19 Jun 2026 02:17:17 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8edaf9eac036da26a2471fab4a07bc3fffa7f24ae894bb7131bdea7fffe12b50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7509755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4014808a74cecd736b121d3e7c6e836790bce5ea098f57d0dfad557e2be765b`

```dockerfile
```

-	Layers:
	-	`sha256:0dbc1cb175301e1911ede1c7f47d9d877b49c8a352298c8e2b5f42e024f58230`  
		Last Modified: Fri, 19 Jun 2026 02:17:18 GMT  
		Size: 7.5 MB (7495298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13b558bf9b697ba1fae51058aa108bd3389330cd95bfac844a783c18d47e0e40`  
		Last Modified: Fri, 19 Jun 2026 02:17:17 GMT  
		Size: 14.5 KB (14457 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:191233cd5a20ba27365d28c1e7104bbef2f28f882ee12022625d540f40d5cc34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274187728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d6f34f9ef3c3182920162e777867b27f61acb36ab5d54f15fb81ca5399cf3b`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:28:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:28:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:28:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:28:46 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:28:47 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:35:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:35:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:35:45 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:fc2380819f7227178ecd607b245c244d8811737f42c6112caf011a01a3889a8e`  
		Last Modified: Thu, 11 Jun 2026 00:24:43 GMT  
		Size: 53.1 MB (53137939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c757e25eae7c582cfef76c30181fc527b42e7b29239bda1a4edb72b6b1ee22ff`  
		Last Modified: Fri, 19 Jun 2026 02:32:44 GMT  
		Size: 133.1 MB (133110616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ef027edd064d4e75767ecb50cd79a0089d4b502b3f51ec96fb0b8706397dc3`  
		Last Modified: Fri, 19 Jun 2026 02:36:28 GMT  
		Size: 87.9 MB (87938528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94deb0d8c9ec363d7825f9c1fb5a13631de11b955d4102761806738ed6c61b50`  
		Last Modified: Fri, 19 Jun 2026 02:36:25 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:dffbe259d008336daea20c3edecafd851e6cbaca6258d54ddd4630ce351f6633
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7506480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8447d8b0f32562c8bdb24f12d2297f6596568a99e55bdfa7bc22d40a86b469bc`

```dockerfile
```

-	Layers:
	-	`sha256:11b58258a156d5dee5c70081430e9e18d67a8e1053f2cbdc45792bdeb07824a4`  
		Last Modified: Fri, 19 Jun 2026 02:36:26 GMT  
		Size: 7.5 MB (7492093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:866bd33f2385d466b9c5734bfe722aad9d6e8bb36678954d176b3107d17891e6`  
		Last Modified: Fri, 19 Jun 2026 02:36:25 GMT  
		Size: 14.4 KB (14387 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:c317e280fc5fa34514804f596767603eedcd3cb257553e888c9c28aa8eaa6d0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.5 MB (259541027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb8752ac99ef60cfb2b5e51cad7c8e3c1bb0439840058cc8b2c044068c293e7`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:16:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:16:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:16:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:16:04 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:16:04 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:16:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:16:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:16:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0ebf827318debac5b829e4cd5c36e0122490cf2392f532aa02b2b0999d5c1b37`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 49.4 MB (49385897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57712a77edb5fb5870f6e2c7189783614a7b3cfcfcb661fb1ad32c31ebd81312`  
		Last Modified: Fri, 19 Jun 2026 02:16:50 GMT  
		Size: 126.7 MB (126652563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e76166bc5448a39404249c609bd7a2fb42a61f8c8a5aa6ee13269d31a332b9b`  
		Last Modified: Fri, 19 Jun 2026 02:16:50 GMT  
		Size: 83.5 MB (83501923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0effd922391b940d76c0f6977a31bec02d51e1bf0855db1dfc1a4a7b853773`  
		Last Modified: Fri, 19 Jun 2026 02:16:47 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e0afc3af7f2d44b1e644b6cb7a6391f8acd9647e621cc6de346ca71789844ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7498552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3ce39aa2617e2cc09a4bb3d0a315cc7e6fa0bec60eb2bb61e57f82c5202dd58`

```dockerfile
```

-	Layers:
	-	`sha256:3f3adea1861dd50cafd315a160fc8ebf18553843a9522d1d26bcbdf935ad86a5`  
		Last Modified: Fri, 19 Jun 2026 02:16:48 GMT  
		Size: 7.5 MB (7484213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68ec063767fa7e38f06e1fe3096d4023958a6cf3a14a27653b071e8618b061c0`  
		Last Modified: Fri, 19 Jun 2026 02:16:47 GMT  
		Size: 14.3 KB (14339 bytes)  
		MIME: application/vnd.in-toto+json
