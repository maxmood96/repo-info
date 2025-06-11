## `clojure:temurin-11-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:e8926e98338ecbd93c0687f1e6283a8a2ef33d45006c61e587d92719d25f36b7
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

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; amd64

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

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1b2785957075ccfc88128e5b75a221aaa0b3ad1c51d7b33bdeca769abd70aad2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.9 MB (239889963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c76178e723901ac5ce410b467c8183324af73649337e33f2f430ea2db3d1e258`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339f131b0c863dd40b5fd07ad70acb5f693f996675d13c5efd4b1e69e47b407a`  
		Last Modified: Wed, 11 Jun 2025 08:15:06 GMT  
		Size: 142.4 MB (142420687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6ffa2a190af615b036c414cceea8204d9c36047421adfcdd099d20d9dbff22`  
		Last Modified: Wed, 11 Jun 2025 08:21:16 GMT  
		Size: 69.4 MB (69390957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec274db6c2947fe49a5ee372190ab89ac550472234cc016076d3bb6c6888d3b`  
		Last Modified: Wed, 11 Jun 2025 08:21:11 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3e059fb634216e01720b9c26710ae54a7ac8b81d27284d4339e51b692eff44f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5150835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eefacc1a0a4d1bc516e7f2eb1230688be2ff01074ca0b98d91d7ceff25c6133`

```dockerfile
```

-	Layers:
	-	`sha256:882f95495311f3dfcc1114b531453f7325ce4b1f8e8aae59ebcb3fe402d44e8f`  
		Last Modified: Wed, 11 Jun 2025 09:35:32 GMT  
		Size: 5.1 MB (5136408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14534e4a800d368b835517433326c4c101550f3ae05f6f284dd88d6ca3825b74`  
		Last Modified: Wed, 11 Jun 2025 09:35:32 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:71cccfd164e26bee850a067d43ae268121446e688ef6d854da8574a17468f9bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.2 MB (240229748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:443f5212e44b8e85a0d832dd20f56d33f7b0af3009fc26d1205018df3331bf66`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
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
	-	`sha256:c9cd5d5c131a8141631d87d9507a82e0549a2144689442301c07d2da80f39d19`  
		Last Modified: Tue, 10 Jun 2025 23:58:45 GMT  
		Size: 32.1 MB (32072795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2fc8533a314cc3b060f159840519c245d5ae464e763a85f09d6182a04d7d37`  
		Last Modified: Wed, 11 Jun 2025 08:14:55 GMT  
		Size: 132.8 MB (132810557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534df4429f366c1266d7cdf3a01a927699aff730a1751a2d347150851d2fca92`  
		Last Modified: Wed, 11 Jun 2025 08:21:16 GMT  
		Size: 75.3 MB (75345751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b084298c99b017d6a465d430a1a787bfcac7ef4f8a371aa4f33021d3ab7db6c`  
		Last Modified: Wed, 11 Jun 2025 08:21:13 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:52e0fc1ff9f027f9ec26fb381502955bc35e639aad30b889c60f7c2648e10cec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5148930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:761682ec5b344939527d732f8cca1fbe0a04b99315df8312bffd41af5479afe0`

```dockerfile
```

-	Layers:
	-	`sha256:99021b95f14b875a8495b55989a12be673f7d2f1efb15f005013adfd01cfe115`  
		Last Modified: Wed, 11 Jun 2025 09:35:37 GMT  
		Size: 5.1 MB (5134572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ae282fd86745c766673acf08a2ebd361297fd02722aae8cd17ea350d72fe205`  
		Last Modified: Wed, 11 Jun 2025 09:35:38 GMT  
		Size: 14.4 KB (14358 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; s390x

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

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

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
