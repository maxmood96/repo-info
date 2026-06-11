## `clojure:tools-deps-trixie`

```console
$ docker pull clojure@sha256:3eac932f623830f0269e324a80bcf5e593e047386b993c3804adb2e92f758efb
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

### `clojure:tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:3a7436e4c0372eee2492eb7ea0c2a87d06a31a315b81414aafba187c2bc6d0d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.4 MB (224411869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58fd4ed2344e76064fca2800c87fc360d09c7869d9ab35a3cc84f5c867576124`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:21:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:21:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:21:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:21:14 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:21:14 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:21:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:21:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:21:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:21:28 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:21:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ef1b08ddd59d42b444e8f9c68a6cebbed70636aed0c242fdccb0bd61b61ba26b`  
		Last Modified: Wed, 10 Jun 2026 23:40:27 GMT  
		Size: 49.3 MB (49317121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b557b81988f251324fda7cfcd051c2cebc136f52914112b95300d3fd027ae711`  
		Last Modified: Thu, 11 Jun 2026 01:21:49 GMT  
		Size: 92.6 MB (92574564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e22413026d47d3e7b9bbdc9c2c14316541504252101cf9265248e5c7f67f30e6`  
		Last Modified: Thu, 11 Jun 2026 01:21:49 GMT  
		Size: 82.5 MB (82519149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95bee5e5f191cb38af938e84525cc2c2ee180d726ced1abc2bc36b23e08addd`  
		Last Modified: Thu, 11 Jun 2026 01:21:45 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfb9e8599a11b87c88d888230912c2da320525696ec454ac5962b6c30fe353b`  
		Last Modified: Thu, 11 Jun 2026 01:21:46 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:21052f9319cde53a88b8eb3103e9a5317fcf0eef906d257317806767abf37172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7453401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af4b057cd525e6ce8b903bf8a8b40bf31cc9147952ce129ae44956916ea5c73a`

```dockerfile
```

-	Layers:
	-	`sha256:a95e4888cdbb4f91ac543ccaccd933b610cd753c658bcfac283f7c1d5ac8e2c1`  
		Last Modified: Thu, 11 Jun 2026 01:21:46 GMT  
		Size: 7.4 MB (7436833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df63a00403984d38be1280e57f3c2734aac99c3a0a3bf26076eb0aa5a33945da`  
		Last Modified: Thu, 11 Jun 2026 01:21:45 GMT  
		Size: 16.6 KB (16568 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3cb466a34fbe60332663cb493764bcd16359ca427117a2f3298b17742a3e0749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.6 MB (223559801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7943bf8177d50f86ad6d4cdd1ab8abf7fe63c6b4c6b148e430eaf05e18df874`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:25:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:25:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:25:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:25:18 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:25:18 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:25:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:25:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:25:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:25:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:25:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ed660e1af0f5da9e93a4c43fb29e86cb46fe69c76bcf11a3de9c57c987acab82`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 49.7 MB (49678169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c76ae67620895b39f9db6e82f5251e63328bde43a1aee8a6411d11fb19e7043`  
		Last Modified: Thu, 11 Jun 2026 01:25:57 GMT  
		Size: 91.5 MB (91542254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d9a86d179e4282afc956f2e363b9d3986f1cf4e50e9fececd2b68aaec5bfcf`  
		Last Modified: Thu, 11 Jun 2026 01:25:56 GMT  
		Size: 82.3 MB (82338338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2846610ff3c1889f4fb74dcd9e3bba9affd1d6c7df56f71fce1386f8f5196a41`  
		Last Modified: Thu, 11 Jun 2026 01:25:53 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fbbeddfe72711400db5a66b9b3e54f27206dfb228f1fa7a1e5e0431c8c75a6b`  
		Last Modified: Thu, 11 Jun 2026 01:25:53 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8d6bdbee7dd170b9a7f267b352aa8f0bdcbf4e781671536c9466b85543580de0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7459958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba7d07275f7fb350d294d78cc6a857970210b439d3724e73bb6cfa6b42e09e40`

```dockerfile
```

-	Layers:
	-	`sha256:a2ac309bd157425a4ed241743ba83053fe7ba093bd90956ef6a4bd8fd1e6bdb6`  
		Last Modified: Thu, 11 Jun 2026 01:25:53 GMT  
		Size: 7.4 MB (7443247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db05ab6aec3fd93467a94670871fed118a88123db291ef60d666985cba4acdac`  
		Last Modified: Thu, 11 Jun 2026 01:25:53 GMT  
		Size: 16.7 KB (16711 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:811188b5bf9dd4d98584237252ba1b31c64b84d0f1b58173bc8d21e456c82362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232991611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a9e939c2644c8c08d1de5fbd2049a55fa6d1e42745ef82c96847334eec00db3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 09:44:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 09:44:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 09:44:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 09:44:07 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 09:44:07 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 09:48:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 09:48:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 09:48:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 09:48:01 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 09:48:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fc2380819f7227178ecd607b245c244d8811737f42c6112caf011a01a3889a8e`  
		Last Modified: Thu, 11 Jun 2026 00:24:43 GMT  
		Size: 53.1 MB (53137939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7ecb1a90d8ff27a40d9e50d6613e7d3d7b6df7c9f63edc095609c25a1f30d7`  
		Last Modified: Thu, 11 Jun 2026 09:45:29 GMT  
		Size: 91.9 MB (91914038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714d4c7484ce9e9a8fbef59e8f84f5dba7f91262ed445568f616a47c81a6f539`  
		Last Modified: Thu, 11 Jun 2026 09:48:36 GMT  
		Size: 87.9 MB (87938600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88dccc810fe32e6aa975915c27a3c585147999791bb893e4c666832f2a13da7`  
		Last Modified: Thu, 11 Jun 2026 09:48:33 GMT  
		Size: 609.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a752b5007af00fa42f60927e9298a0d5329c3fbdc3c30e909e16b06c3031e2`  
		Last Modified: Thu, 11 Jun 2026 09:48:33 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:bd73a1d2aeb863be8bb822494b56c6bc843d779f209ffd321365891c86d6d58b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7440254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fe2e0461f2c76f49a2177ac5139a3f41473aab5de8e4b506f73c4cc2592815a`

```dockerfile
```

-	Layers:
	-	`sha256:1936953159bd247598f98e04dd98da4f045df073cbb35d7a91b9096d2772d960`  
		Last Modified: Thu, 11 Jun 2026 09:48:34 GMT  
		Size: 7.4 MB (7424578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad4afa843b3b804849e724ec895266aa017884b93a1ee1b9da55633ab604332a`  
		Last Modified: Thu, 11 Jun 2026 09:48:33 GMT  
		Size: 15.7 KB (15676 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:04b166160c881e470a1a5821fedc4936459b003650632829c5e8c367190f054d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.3 MB (221309409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86ad1b32690aa67cba885de4fcb4cdecb48585ac5cdd90ccc3f1ae3b6ca8fd8b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 03:13:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 03:13:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 03:13:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 03:13:33 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 03:13:33 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 03:14:49 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 03:14:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 03:14:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 03:14:49 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 03:14:49 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0ebf827318debac5b829e4cd5c36e0122490cf2392f532aa02b2b0999d5c1b37`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 49.4 MB (49385897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d7018c047dcfb3a1d71919456a69bf9d583fb6c58771bf17729ad5a401b79b`  
		Last Modified: Thu, 11 Jun 2026 03:14:13 GMT  
		Size: 88.4 MB (88420320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6380d357117cdc7dca94d2dfc77b5cb25c26385775ec4d168d0c1e721b3ec9be`  
		Last Modified: Thu, 11 Jun 2026 03:15:17 GMT  
		Size: 83.5 MB (83502154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea31c637de1452549731a230a2e58b2c4d23c5d044e1cb7c2c5e5187e4dcee3c`  
		Last Modified: Thu, 11 Jun 2026 03:15:15 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4252a69246fa28d42eeba435c9765b1c9c9e8f02d3f86e805906072e6eef0bb4`  
		Last Modified: Thu, 11 Jun 2026 03:15:15 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:80df66f45af98e0d60e3bca648c8daec14bdd9aaf8f34178645440dc9850b66a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7433886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6796fb9aa9185fc2684ff8acbe7f2502315ecb2016c23327279b88b386af7ff`

```dockerfile
```

-	Layers:
	-	`sha256:dcd9df65ace6d1cfd06f22be574c02870b4bf92ea4c8a25c88317f0e03cce420`  
		Last Modified: Thu, 11 Jun 2026 03:15:16 GMT  
		Size: 7.4 MB (7417317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80bbfefe2798670ed1cc2b043743bfe52bfa5a38bcf51b61092f34a5132effd8`  
		Last Modified: Thu, 11 Jun 2026 03:15:16 GMT  
		Size: 16.6 KB (16569 bytes)  
		MIME: application/vnd.in-toto+json
