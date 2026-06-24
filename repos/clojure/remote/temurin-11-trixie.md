## `clojure:temurin-11-trixie`

```console
$ docker pull clojure@sha256:a6d149667cc3b71f493226c6290c0050189472a5e4a4c5b4458c2f5bfe51a513
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
$ docker pull clojure@sha256:e4f98f655620357dc33f20646dfdd298d43b1030890be15a94aec6d44ddcebcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.7 MB (277722032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e77872131e9302c04a2f0a65ae5ced2a6da9c35523d7582a4594fd64b919960`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:17:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:17:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:17:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:17:08 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:17:08 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:17:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:17:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:17:23 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:aa3e9ef32f73c30e8b065800ee66429992d3bfea6a1fb8224afdd878ab5b994f`  
		Last Modified: Wed, 24 Jun 2026 00:28:33 GMT  
		Size: 49.3 MB (49317255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01fa782e862ea408fcd07caf3c748c77bfdef043fffd5c1464a1c297280e8cb7`  
		Last Modified: Wed, 24 Jun 2026 02:17:47 GMT  
		Size: 145.9 MB (145886165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c20540051388ab892bceb84b8cb3065fbcfb9ca738071da665e038747c70b6`  
		Last Modified: Wed, 24 Jun 2026 02:17:46 GMT  
		Size: 82.5 MB (82517967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09d56dca245494cb3719589040ffebdea43594bf3d6f3c30aab5d66ab0a65ee`  
		Last Modified: Wed, 24 Jun 2026 02:17:42 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ac78ec27d7a49dc1f8a2b20abf6009fabf94f382299dcd15c9f20ddf1851751a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7502626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ed9065bd8e966867caf169a4d9ef129d66ba26073e2a1e788e41e412f5fc2fd`

```dockerfile
```

-	Layers:
	-	`sha256:92b6868e5145a50f05e1a3c3b3427ae8bb6279c3e82f7fcb8da5e8cb7c9f1789`  
		Last Modified: Wed, 24 Jun 2026 02:17:43 GMT  
		Size: 7.5 MB (7488287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f85b9238c52ba430a52bbef15a821446de82c3116257b804a56cebc093122d49`  
		Last Modified: Wed, 24 Jun 2026 02:17:42 GMT  
		Size: 14.3 KB (14339 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a11a222eadcdbfbd1e12d9e8f37d8bf3bdeed3541ca5549dcf0af0a6bbccd826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.6 MB (274599672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf425558acc9f4926e1d2aed6510fa7093da07d9c369d8f8b41d4eee22507f30`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:23:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:23:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:23:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:23:17 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:23:17 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:23:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:23:35 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:23:35 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c8a311258fd162f6aa0db134045a19154c81a2244ff9ed7620256c95ae5d6b69`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 49.7 MB (49678395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057a7e51871d1aaecc2d344b7742f8c7a03d65bf3009f96c6f687eedc96453f3`  
		Last Modified: Wed, 24 Jun 2026 02:24:02 GMT  
		Size: 142.6 MB (142582142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb9f468ab6bc679bb1f4fab6dc3fc5335e0c8e8576a5ebe9f94ea3a13b6b646`  
		Last Modified: Wed, 24 Jun 2026 02:24:00 GMT  
		Size: 82.3 MB (82338489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450cb7d507c1f34290036fc09da06d81bef74ec958e8de2159f627ed5fc44011`  
		Last Modified: Wed, 24 Jun 2026 02:23:55 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:04e4acaa5bb7669f61fcf574fbb9431b55d725bbef6318471804de527ef00f0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7509755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b1d4c26937a2c055fd05fabf16c29360c4a0134932838d79c71bf612edbf957`

```dockerfile
```

-	Layers:
	-	`sha256:76651b9ca84d045367aec4fdaa81fce397f3af28b3e58b9574f3b853e1216b00`  
		Last Modified: Wed, 24 Jun 2026 02:23:55 GMT  
		Size: 7.5 MB (7495298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:243ab3edb723f99caf0452c0bd365c24932fd54cd53a56a7de954742c672a709`  
		Last Modified: Wed, 24 Jun 2026 02:23:54 GMT  
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
