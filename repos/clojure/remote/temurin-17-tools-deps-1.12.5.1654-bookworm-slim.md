## `clojure:temurin-17-tools-deps-1.12.5.1654-bookworm-slim`

```console
$ docker pull clojure@sha256:2cb04ae73c274959b625aa96facdb73862e4a72226b3993857be8e8d92526bc6
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

### `clojure:temurin-17-tools-deps-1.12.5.1654-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:afb6ab5eebfe74c080ac5a6951f714e752e50172b784c5c739dfa8cafe2f10b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.8 MB (240786744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9242d7dd0e4432648f95144bc6e7b278a403beb7b929aecb56fe2de50f1244f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:18:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:18:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:18:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:18:45 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:18:45 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:18:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:18:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:18:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:18:59 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:18:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77433b5eacb5ce08560c487d4a447b53cebd08a9e690f8be5a0f73efc6b62aec`  
		Last Modified: Thu, 11 Jun 2026 01:19:21 GMT  
		Size: 145.9 MB (145905445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a0c5574d672cda800934fbc0dcda52f6ca92767f5ebc909b9dc5ea0ac33c91`  
		Last Modified: Thu, 11 Jun 2026 01:19:19 GMT  
		Size: 66.6 MB (66642635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cea7cce57747af781291c67f976d82681328cb40e3cc8ffd527752dc6175b4`  
		Last Modified: Thu, 11 Jun 2026 01:19:17 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5911808fcc91ffb83c3f80e6c5c1f5c231c6e107d518b381dc982b179811bdc1`  
		Last Modified: Thu, 11 Jun 2026 01:19:16 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1654-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:67b6911f1cb94fe036613ba8c7cc168e3977523bdb62a7879a73a7d026502a4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5129989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcbe9df46db2dc2108bfba724c622714bdafcf7659997721487b8e9093c9264f`

```dockerfile
```

-	Layers:
	-	`sha256:876490d2bc7f49c32c5111e92fcff9d017ee82fd22fd084c27628e1784435cc4`  
		Last Modified: Thu, 11 Jun 2026 01:19:17 GMT  
		Size: 5.1 MB (5113999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91dd2ccd52a995eb982c9fa7af977331bb99f82f0452034270fbed0d04f67392`  
		Last Modified: Thu, 11 Jun 2026 01:19:16 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.5.1654-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:65a3a68b9e1ad97edb399ced2c81a91d2b747450e0ccc80672621ec3f2b75ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.5 MB (239491051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c951424ba6f743626d862782381ad84527b292f75cf6facd58ce77bcd45bf0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:22:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:22:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:22:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:22:48 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:22:48 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:23:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:23:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:23:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:23:02 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:23:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8adb2116f24f3fb5f204ec34f9f8bbe6097fb12cab86a9f30b04b1617659a0b6`  
		Last Modified: Thu, 11 Jun 2026 01:23:25 GMT  
		Size: 144.7 MB (144724361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5a4f78e9da90dd685975bd473482a54ab242a1ff90e19bddc11081312b4b10`  
		Last Modified: Thu, 11 Jun 2026 01:23:23 GMT  
		Size: 66.6 MB (66643344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa00edde46dfcced1fe2a5e04d474ef19224f945e8328cfa228e2586088810d`  
		Last Modified: Thu, 11 Jun 2026 01:23:20 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0bd04d5ea972e094efd383653453614cd58f3af6b63dc49836c68f7d6d6b9d6`  
		Last Modified: Thu, 11 Jun 2026 01:23:20 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1654-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dca1d085fdfa0758cc009be2de63958a999043937d500889855eccd39ba63085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5135867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f19b8f5cef3c564c62f8937024a3b01caa6daa2db0fb3bab44cbfb1facaab1d`

```dockerfile
```

-	Layers:
	-	`sha256:59d8a9f8441707f685a43ebff231aa2f7311a64c3142ac5c8a2536209ddd214d`  
		Last Modified: Thu, 11 Jun 2026 01:23:20 GMT  
		Size: 5.1 MB (5119760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:229486a6d6164d4f857bb728c1429374ed2f953097684efa9ecbd5b97039a110`  
		Last Modified: Thu, 11 Jun 2026 01:23:20 GMT  
		Size: 16.1 KB (16107 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.5.1654-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:0a7aa2895584f21370e5578b4537c9ae870186bc3e2221d3dfc3ddf3a107e545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.3 MB (250325490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06c5ae2ff671eecbdb1e8f65845575c140bce0f669a494008f61e409f7f06424`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 09:29:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 09:29:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 09:29:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 09:29:22 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 09:29:27 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 09:34:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 09:34:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 09:34:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 09:34:08 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 09:34:08 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:23f7cdee3ef2598b081c2b848fee95730a7ab2b1cc5b726c72dcb8c2fe3632f7`  
		Last Modified: Thu, 11 Jun 2026 00:21:33 GMT  
		Size: 32.1 MB (32081941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bab2c1eb2f066d3ff6bab086dbc5fafbc50c746db8da2cc3d2b22fadc81c442`  
		Last Modified: Thu, 11 Jun 2026 09:30:52 GMT  
		Size: 145.8 MB (145766120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8318c007f29c2c3210f9171e96794e6add0b68b8850a86b31e48d22ed0edf1`  
		Last Modified: Thu, 11 Jun 2026 09:34:45 GMT  
		Size: 72.5 MB (72476390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12f7705926ae7f5485d76c44abae04e6460f5404b85cba86053bbac95633301`  
		Last Modified: Thu, 11 Jun 2026 09:34:43 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa913b4b701cdf0e57cfb16ff4bf784ff9b8fbee3c81a4092371efa61ceebe39`  
		Last Modified: Thu, 11 Jun 2026 09:34:43 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1654-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:84678a0ce75e56ffce26e59b4f69e760bfb85f6ac68d3326aee392c2fc99db9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5134240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3efaed900c8973f32d8489ac2874c76f24194936935d3e374f1e21ccf842dffa`

```dockerfile
```

-	Layers:
	-	`sha256:952333afd8298118cb327977d9d01462a5182eb58ad02da45806a8a1229f75ba`  
		Last Modified: Thu, 11 Jun 2026 09:34:43 GMT  
		Size: 5.1 MB (5119157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:744e1953181249e00b8d9a5c6f2ffb7e7c7592f4eabfb46ede8afc30c09e6b0f`  
		Last Modified: Thu, 11 Jun 2026 09:34:43 GMT  
		Size: 15.1 KB (15083 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.5.1654-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:8db73565cc91909c7ba9a69add896fbfe57bc4cab30bcb20185d4660d9ba0745
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228257059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf21a1e4a08836533a5ea4dfddd3f563a3aa57c8c9687541ad0a95466740f572`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 03:08:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 03:08:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 03:08:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 03:08:53 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 03:08:53 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 03:10:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 03:10:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 03:10:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 03:10:10 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 03:10:10 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6483bebe0f30256cfdd9c6f96373508f6b33d18b4bc61668ee641c700aa3108a`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 26.9 MB (26893508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0df9523820e83a5b63feeb7f96fdbb885f9dae313fed2f41bfabf8b2e65e98c`  
		Last Modified: Thu, 11 Jun 2026 03:09:36 GMT  
		Size: 135.9 MB (135910407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74b7dcf9bece11db2c58d9626cb842ae3a6fea766ba974a859d2bc80cc69599`  
		Last Modified: Thu, 11 Jun 2026 03:10:36 GMT  
		Size: 65.5 MB (65452106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce897ae1e9b5ff52426ebf596177fc738d883581c2b6b6ab9c47e6b59d7f3bbc`  
		Last Modified: Thu, 11 Jun 2026 03:10:33 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55412bd2f66712c737a10e35b6ab4b010e962e5e6ee8d4498788c9de4e563b34`  
		Last Modified: Thu, 11 Jun 2026 03:10:33 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1654-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bce7e21aca5fcf079b9e7a3638fcf74d7bddb5c880cfd14a1f4c04680ca519e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5120355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c47194f7a22a7fe3164dadefdd6031d54e1dfb2e12d689ec7156be275bbdd6`

```dockerfile
```

-	Layers:
	-	`sha256:b4803848a4869aa08c26f427df9e5b881442891b2a024550c351c5019cb51ac0`  
		Last Modified: Thu, 11 Jun 2026 03:10:34 GMT  
		Size: 5.1 MB (5105320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3283144ddd3bc609a35562147fdbf656906674aae0c50a946c4bb430dd83faa4`  
		Last Modified: Thu, 11 Jun 2026 03:10:33 GMT  
		Size: 15.0 KB (15035 bytes)  
		MIME: application/vnd.in-toto+json
