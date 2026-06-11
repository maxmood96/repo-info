## `clojure:tools-deps-trixie`

```console
$ docker pull clojure@sha256:9deb077f6880d47ff53a6f0876323f05152adc5c309139e78a0a7619f427e5fa
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
$ docker pull clojure@sha256:fbb5cac016cdec65476eca9c40f910852aa31908a3950698e53a0d2f05ade93e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232985237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0be6e4943940871cd107a2569f78bf3bf674bcc31903c4521fb410478f101c52`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 18:06:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 18:06:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 18:06:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 18:06:36 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 18:06:36 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 18:07:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 18:07:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 18:07:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 18:07:26 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 18:07:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:55497c62a793e62a2e78a3fd85fcedf060da73e331ad107733199ea991106b96`  
		Last Modified: Tue, 19 May 2026 22:37:59 GMT  
		Size: 53.1 MB (53132182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1525d5045df9660d1c5f453aabf32cfbeb82239dce10b64e81ec9ff422c41e`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 91.9 MB (91914038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f380e52b3300e5add503f81d30cbd0d58c45f73c928f58499d6eb2e4ebc542d5`  
		Last Modified: Thu, 04 Jun 2026 18:08:13 GMT  
		Size: 87.9 MB (87937972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18dd49354089fd1918b589b3ef775e15da1a3f8799e8c3cfda5014ef8d1c83ac`  
		Last Modified: Thu, 04 Jun 2026 18:08:09 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f39ffa7600ddfef43326fd93c7aa6e9b3a9da170291b1a879dfd889fb6a971`  
		Last Modified: Thu, 04 Jun 2026 18:08:10 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1e90fac4d61957319bde84fb0b44c8de88df740310a1476f96b84ff20c4840f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7441207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:591051e6af2a42c1521e2eccd41da313d13bd2705ca7e8a507f64c158113d05b`

```dockerfile
```

-	Layers:
	-	`sha256:a2efd5386d91986778f7f533f54226aa1161d653d43702abc962367b4eff274c`  
		Last Modified: Thu, 04 Jun 2026 18:08:10 GMT  
		Size: 7.4 MB (7424578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1711428c4127436c0fc0d011f2abd4ba6dc6a08adc2181cba16d91e21fb29fa`  
		Last Modified: Thu, 04 Jun 2026 18:08:10 GMT  
		Size: 16.6 KB (16629 bytes)  
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
