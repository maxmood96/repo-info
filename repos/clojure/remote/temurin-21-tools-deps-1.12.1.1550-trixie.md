## `clojure:temurin-21-tools-deps-1.12.1.1550-trixie`

```console
$ docker pull clojure@sha256:97b8ebc6991b31ba43f924c4194e35a097146838791b738af6d4076269ae31e4
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

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:bac7f12ea658a68c2f06538a2d9b332c5815a71cecaf378d1bd1bb67c2fcbed0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.2 MB (292154506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab516489c1df6146822d32e3cfc623d7070a0112ba796d461da87162753d9f77`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1749513600'
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
	-	`sha256:d8e51f6b7dcdaee60f07f9a13a971abe1be9dc977d52d0849087118f80a1c7d6`  
		Last Modified: Tue, 10 Jun 2025 23:25:45 GMT  
		Size: 49.3 MB (49253859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab634770862420b50ca7f736a011e30487ae5d3684e2f9c84ef2396dd089284`  
		Last Modified: Wed, 11 Jun 2025 03:45:08 GMT  
		Size: 157.6 MB (157634457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d460e5124d61c01257ccab7eba354b7c88cb12cde89c82e38ab5f532b8b5209`  
		Last Modified: Wed, 11 Jun 2025 03:45:03 GMT  
		Size: 85.3 MB (85265148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf66e45482c7de8977f4e7a73f4db294fb041925b8c759c80e0346279ddf2c91`  
		Last Modified: Wed, 11 Jun 2025 03:45:00 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e46817c16006cddf1cd81bcd76bab3d5c833590f1bded1997c148832cd6cd54`  
		Last Modified: Wed, 11 Jun 2025 03:45:03 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d3b50298699de2e58422ec8c6eba9d8c3b7bc4859cb96ef051f3b4d2a7d9e975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7479384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075885c88f363951ab96b7a72f953ae3793e4b267741c8a99f2c6da77ca7a422`

```dockerfile
```

-	Layers:
	-	`sha256:5b1193ec7827a90f2a8296c9c27fc27eda7b621b99c27528fda2b9b0da735b0f`  
		Last Modified: Wed, 11 Jun 2025 03:39:10 GMT  
		Size: 7.5 MB (7462919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcf8fa132b57dc15c80740acf01237dfe16808e2e33cd21298e516218723afb5`  
		Last Modified: Wed, 11 Jun 2025 03:39:11 GMT  
		Size: 16.5 KB (16465 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2bcc3bca708f6a45d319d0736dc9d1102d888a9d540a21a263b78249d6b7249a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.1 MB (294058913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f1567c4c5390636218ab5d10c23e05301c884a1c5d6bc97b7e1b2ea9e089a92`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1747699200'
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
	-	`sha256:397826b9fe635f12caff1a603eb12c37426a5b3dc563e0adff2debff0c68a6b0`  
		Last Modified: Tue, 03 Jun 2025 13:47:15 GMT  
		Size: 49.6 MB (49618294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669209475ccf588005064aec8b03f795116e849de02f62977a14a87f1ef3e90e`  
		Last Modified: Wed, 04 Jun 2025 11:30:41 GMT  
		Size: 155.9 MB (155928831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:874a8cbbc40e5a14834f27ff81176f9ac59f0a77cc90a8d86bfb898c8951daa8`  
		Last Modified: Mon, 09 Jun 2025 17:56:32 GMT  
		Size: 88.5 MB (88510747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8859b47abe90da8b5343cbed330755c3c8b247226f670b902299a33a631fee13`  
		Last Modified: Mon, 09 Jun 2025 17:56:26 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf3a597e9808f5cac0cd0b776fb75c88ae77c7f242334092cafcd08436776fe`  
		Last Modified: Mon, 09 Jun 2025 17:56:26 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b5d2d5a3b6af6fee9a32de57a4f215d74e19ab9c4ce6c6797b7727c9101dc01e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7486066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ef5a6c0a820252f1007281fde96249689e9d3314e70615367bd0a940b0b785`

```dockerfile
```

-	Layers:
	-	`sha256:43bc8aec5b2c489dbac7bb21bc4764ea920274a52028b5deaa461bf9be86353f`  
		Last Modified: Mon, 09 Jun 2025 18:40:17 GMT  
		Size: 7.5 MB (7469459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffb30620d89090349e8195ad99557bfd8e7e1c946df92f65d9df2d78e70ab91a`  
		Last Modified: Mon, 09 Jun 2025 18:40:18 GMT  
		Size: 16.6 KB (16607 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:e8c14fb75607faef04177ecd34ee4c79276ac3048742fdbb5d5c5f0d960eb950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.8 MB (304836803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27ae15a13c2b078849dd427238d3d1331bd9682116ad9e23170ddc91fd4435c5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1747699200'
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
	-	`sha256:25dfffa4126a91eb76c700c90bfdc9a9e15f34c7438a81f16c8a6999bbde6e45`  
		Last Modified: Tue, 03 Jun 2025 15:03:14 GMT  
		Size: 53.1 MB (53080544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f6bd552c8941351aec1fc10e7be3cba78443c32cad3ba1481c6ebefe465a52`  
		Last Modified: Tue, 10 Jun 2025 11:59:54 GMT  
		Size: 157.8 MB (157804856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067448693ed6e7019ab2b94a92bcc4addff5a988aaaadc28ace5af4aba2d6159`  
		Last Modified: Mon, 09 Jun 2025 18:18:15 GMT  
		Size: 94.0 MB (93950363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd5fecd647c0c15914b312b35b51f939d719c1ab1a725612c0d49edfaf41815`  
		Last Modified: Mon, 09 Jun 2025 18:17:55 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6edff878010af4646a9f4a5bf78971b850a5dfa5489559c7e20de03fec2dbd8e`  
		Last Modified: Mon, 09 Jun 2025 18:17:56 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:05cbba753fc1983a0f81be0aa65c663f8544162f60640c13aa9f397b409182e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7483359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:153ad46b013072c2811a7117308169bfafddfc881ca5c2bc944145279e8f88c9`

```dockerfile
```

-	Layers:
	-	`sha256:98fc5f2b2fa094e59d205f75e7b352041186659ed4cfeba1d37ab8eb08ed8dde`  
		Last Modified: Mon, 09 Jun 2025 21:38:32 GMT  
		Size: 7.5 MB (7466834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15ee820f4ec76b402ff5d03077277bf12e6a0fcf6fa15345089e1529445da003`  
		Last Modified: Mon, 09 Jun 2025 21:38:33 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:9256530cc60fb6e7220beb0ba030cbd04482c5dd4aa272dc64a8ef0a1bb210c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.4 MB (285437062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:382f5f513a9906cb8029f3d855ba66e8e5173af99e8cc1f1a891b518b314afb2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1749513600'
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
	-	`sha256:183a50217c4846c3775204631f79c9cba563face97fcc3de4421f000af401588`  
		Last Modified: Tue, 10 Jun 2025 22:56:31 GMT  
		Size: 47.7 MB (47743345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e321b849c3c9c5e86f1fdfbbd5dbabb64c6a9d3c0bbe94ab4b60806be3956b28`  
		Last Modified: Wed, 11 Jun 2025 00:14:28 GMT  
		Size: 153.4 MB (153449657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8dbec5c514290373fe63615684d8851086010f34798708d82970a0c86b3e1a`  
		Last Modified: Wed, 11 Jun 2025 03:39:33 GMT  
		Size: 84.2 MB (84243014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7ca718d7f1a60a11924c3666e3a3d0b030ca42f90cbbd9409c4186b49e415a`  
		Last Modified: Wed, 11 Jun 2025 00:38:55 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbe871cb70142ba550c552bca4ec786d5c4fa9318aa5f4ffe79ffe366f99b32`  
		Last Modified: Wed, 11 Jun 2025 00:38:57 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:0c633a65850b29aeff6975c27dd30d539fbdd433b511216b8125d6c30ad30424
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7467366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f99eb07bb6f9cd259fe97b432c4874e9ed0286f68c875dda6dc242a366d8833`

```dockerfile
```

-	Layers:
	-	`sha256:a04afa9b6c3b6e4edcd935a5f23fb91128cd829dd5ba8bc9a1a8cbb1b331e5de`  
		Last Modified: Wed, 11 Jun 2025 03:39:27 GMT  
		Size: 7.5 MB (7450842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:964a160e20a3118d5d1c0007fc34277667ed1f8f8daecc31aac62166cdc834a3`  
		Last Modified: Wed, 11 Jun 2025 03:39:28 GMT  
		Size: 16.5 KB (16524 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:c338d3eff60253783a111c6229b964616018ee1b089d88cb07d00a9ff838fa93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.6 MB (282589414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c03ac8e42b646d5d4a74e09e4e5030712ef2d277aefa93fec510947e837ff36`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1749513600'
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
	-	`sha256:1ffa7429d410cb8e2162450d6c2fc3a21121304db16d73a6b9feaa05000dde5c`  
		Last Modified: Tue, 10 Jun 2025 22:53:14 GMT  
		Size: 49.3 MB (49329768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb373063ac81b3f0833d1623165c6390ec100fb5eca64e5b76000fd12df8888c`  
		Last Modified: Wed, 11 Jun 2025 07:18:55 GMT  
		Size: 146.9 MB (146910994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7cd6ea104af06045737d7328b13bda97c010d8a2dcc7a9802e4d03b42e2df89`  
		Last Modified: Wed, 11 Jun 2025 05:55:12 GMT  
		Size: 86.3 MB (86347611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ebac0931bf7bd1ee2cab7370abe8287a286f2c86e6174f7c63df84d444ab85`  
		Last Modified: Wed, 11 Jun 2025 05:56:10 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13a66e0582d3b53a7958db98ce4eae9d0d2ab0082f2e65d4f26652835f075511`  
		Last Modified: Wed, 11 Jun 2025 05:56:14 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:086fc6731d350438d181cf3b7e8343feaafc18b6c75122a708a4a5dfec1e7cbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7475306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e379bed6e463ba4c6a1a8e632166357740c669001ad1af063bf3e1b504d8865d`

```dockerfile
```

-	Layers:
	-	`sha256:bfa6ad1fbf64000f45c300d78b501491be333eafe5bf228bcbb0e2921e8cdd3f`  
		Last Modified: Wed, 11 Jun 2025 06:38:27 GMT  
		Size: 7.5 MB (7458841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c00985599d28c0ff635f46e537a9a3704cca034403c6428d6eb7d1c1ea31174`  
		Last Modified: Wed, 11 Jun 2025 06:38:27 GMT  
		Size: 16.5 KB (16465 bytes)  
		MIME: application/vnd.in-toto+json
