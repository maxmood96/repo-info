## `clojure:temurin-11-bookworm-slim`

```console
$ docker pull clojure@sha256:821d1078537672d026785597bddd7dd4a602be6ae9cf5bd1e07c7b2898f81932
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

### `clojure:temurin-11-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2764bcd3c4573ac1332fbf7a8f57f7660494aa5fabf64afff990ab8c83633cdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.4 MB (243396657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6641c8a428763108245402071acaa35c0fe1c4d584199810f7c33f753556ca7e`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4950b3bea25c67612f9864df91ce6f88f44432f15792ee9890a4078a6bc97500`  
		Last Modified: Wed, 11 Jun 2025 04:25:57 GMT  
		Size: 145.6 MB (145635640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f9e6bbb6d9ee092cbdc86b2bf12737ad8cecadbce00e5742c25a5fa2def7961`  
		Last Modified: Tue, 10 Jun 2025 23:51:42 GMT  
		Size: 69.5 MB (69530245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b39b4e6587bc92e9af5993c52bbb6bfe692aff295edd171e7ea964feca76a07`  
		Last Modified: Tue, 10 Jun 2025 23:51:39 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:496b497cf912675588f19b12c7f6349d6c9b5619e105477859edc046bc115c24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5144338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08db5edeb616b0da6ea8f808ffe6aaeeae11e2594241a94d04bbc76356f6803a`

```dockerfile
```

-	Layers:
	-	`sha256:562064ea3b10f3fd99175bc4b1fe3901868e5a4a354f9aead6c8ecf320189394`  
		Last Modified: Wed, 11 Jun 2025 03:35:08 GMT  
		Size: 5.1 MB (5130029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc55c2d7bc2fa92ef678b14f56b1d590874ee9ce91032d29416e68d8b88aefb0`  
		Last Modified: Wed, 11 Jun 2025 03:35:09 GMT  
		Size: 14.3 KB (14309 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1be65b8f4eb8a84a089e98c4391388a4f277716fb8c696eb010f235dbd7c9be2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.9 MB (239877286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96b1a5451a9d9243f5afc3bf2a70978643b83ee87e631c18f036bd0bb42c62e5`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fefc44eaff424442f81822836abca91702f398096a9228568e0ead8c9faa1d`  
		Last Modified: Tue, 03 Jun 2025 13:57:49 GMT  
		Size: 142.4 MB (142420640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89bf551b01bbde908093d88703e0e3dd52ba8f1d78d5fd40c18c48b5b98d4f1a`  
		Last Modified: Mon, 09 Jun 2025 17:40:27 GMT  
		Size: 69.4 MB (69390721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c48e177ff6abb3f3ecf318d9564ad018331787b77134836f7263619de68284`  
		Last Modified: Mon, 09 Jun 2025 17:39:58 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5e87e2b2b0941a630d8d90c0b7ac11a3df9a7c55af11bbe42fab67e561b2c51c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5150836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3926e02db485db03b923da8be00cf58cd3205bba5823724fcbe96c42015364f8`

```dockerfile
```

-	Layers:
	-	`sha256:ab8cd8c7fd0dbc2203e83af6fad3719b9d0177f828fbdb50aa2c98145331f0f4`  
		Last Modified: Mon, 09 Jun 2025 18:35:07 GMT  
		Size: 5.1 MB (5136408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2aa3f8af0fab8300b09982b611b94154a47945aca760e67d26deca9971947648`  
		Last Modified: Mon, 09 Jun 2025 18:35:08 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:76ac6827658e18b18068a5d147e67edf37a9584049ca7bd88254f03c821c45ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.2 MB (240223816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1895873cf22c6e78943e425efe146ea53b0560bd4887c1bb1d9c7af2c7ca0ff`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:701606535a7233566815cc9ad5f3e5853b443be5476286f6799008053dc2b03b`  
		Last Modified: Tue, 03 Jun 2025 13:39:02 GMT  
		Size: 32.1 MB (32066912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb70de7f1ea6e9e8fa70cca464f19bf365abae7dceabc396212b1df21d889e84`  
		Last Modified: Mon, 09 Jun 2025 19:57:17 GMT  
		Size: 132.8 MB (132810522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b008591cc668816df7b9b1458366611f9333a294df6e078c359a9751b55d510`  
		Last Modified: Mon, 09 Jun 2025 17:52:51 GMT  
		Size: 75.3 MB (75345736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3edb69239a815a34f872689ec77182b81ec73bb48377e5e64c020b314df5e0`  
		Last Modified: Mon, 09 Jun 2025 17:52:34 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5d7a14a02fff5ada9a249008be160f67690f7ce9e5c5f5fcbdd75f432abf37a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5148930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9801cb451d24387728ba6deaf5bb4d95a642e03c3b8f564f213a775e7b73e6fb`

```dockerfile
```

-	Layers:
	-	`sha256:7ef347d42bef884146ce307be07817bd8ed860d2afb1102c6a09df32fb8531aa`  
		Last Modified: Mon, 09 Jun 2025 18:35:17 GMT  
		Size: 5.1 MB (5134572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d42d1347d9e8a32ee3d28321b01c91d18d7de494ca8027799dfeb66dc3c01ed1`  
		Last Modified: Mon, 09 Jun 2025 18:35:18 GMT  
		Size: 14.4 KB (14358 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:33b55a25b38e7027e70e12f40f192fd42c51a83c87e91c472aad8556658f1ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220807891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1fdec0d616df13a3a3a76be21c910cd64e88e1db1d0e1006bc9412028888c79`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4680dff1aa280799741b426efca04d2c5a30eb0a9af80fc9c58828b3c7fdb851`  
		Last Modified: Wed, 11 Jun 2025 05:34:43 GMT  
		Size: 125.6 MB (125585329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49b64ac029d09212f38989a255f8082f3de46723f3b4360e0e614a2bf1d1af5`  
		Last Modified: Wed, 11 Jun 2025 05:38:33 GMT  
		Size: 68.3 MB (68334064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00331d282ef90165d79a6741b85fa5b11934c8b906bc1c817d17e1dd9d715e99`  
		Last Modified: Wed, 11 Jun 2025 05:38:32 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:16debab2a2438399f7037e77a19fcaafb142af29ceb1282ba0863a3ea97afb57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5135664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e0a0f711ed9da3cfb3d6eeb35270a7a8d1369b6b8193ea8b50c701efde4d808`

```dockerfile
```

-	Layers:
	-	`sha256:18a19de8d8138236f8f0e965c638e351fcd6f43f82c7408f902d544c88830c26`  
		Last Modified: Wed, 11 Jun 2025 06:35:09 GMT  
		Size: 5.1 MB (5121354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08a9bb107d6392fa658bf147b8e6e2c40855ab6d0cad47f44aa5f5d00a33a8e6`  
		Last Modified: Wed, 11 Jun 2025 06:35:10 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json
