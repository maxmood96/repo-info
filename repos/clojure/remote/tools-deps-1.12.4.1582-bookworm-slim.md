## `clojure:tools-deps-1.12.4.1582-bookworm-slim`

```console
$ docker pull clojure@sha256:c6c17434f934c39abd1381c138ab653f534abca18965e545ee5146c83c8a2772
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

### `clojure:tools-deps-1.12.4.1582-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:31973b7b00fb522f5bfd2b1d1b590a62491a9c4fe781a59bd56fc77e06e41821
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (189951596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdb01ed790f0296af1ceb030bb1c43a3a5b6f6b7c334b40c4c262b3b247ebea8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 02:05:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 02:05:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 02:05:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 02:05:46 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 02:05:46 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 02:06:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 02:06:03 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 02:06:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 02:06:03 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 02:06:03 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d7693197338d8cdd091dbf24ca08ab59e0e02c226ccb707e34ba4283112aae`  
		Last Modified: Fri, 16 Jan 2026 02:06:26 GMT  
		Size: 92.0 MB (92045317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79eeab38cbdef088f902d975e31c51266208511a53c7e756ecfa19ea2d83bdc7`  
		Last Modified: Fri, 16 Jan 2026 02:06:26 GMT  
		Size: 69.7 MB (69676664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc478ea7e0bc03f504120853b7dbd4f9ae9c74e5bde1dd4a835e2c466406c31`  
		Last Modified: Fri, 16 Jan 2026 02:06:33 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75f50af465d33cb9d5cad5b544915f37a46d7b95c8c4c5696c397faad4e0e9d`  
		Last Modified: Fri, 16 Jan 2026 02:06:23 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1582-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:36095bf7a6445ae513cf59579ac5d579914c160217a7f4eb15fc225bc57358bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5081283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de5b2d4629dd2ff9cdc7d74a9a0d1ef67403e45c83204e465b110df23746155`

```dockerfile
```

-	Layers:
	-	`sha256:0d6cbc413b2b0d6a80a7e2ae10cb94a0436981ab472df7fea599ba3404f47d3d`  
		Last Modified: Fri, 16 Jan 2026 04:51:01 GMT  
		Size: 5.1 MB (5064758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20f30f335058577a3570d901c06dfa6d8839f258d8582eec3fa842cc204183e2`  
		Last Modified: Fri, 16 Jan 2026 04:51:02 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1582-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:58885339039c150c0193277477952b6f63c18ce0010640f50ac4a0cbb665ebd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.8 MB (188834191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5063e732db119e67bc875f7820cd5f07dc80af4b221bc26c4b3137ac6a3d4b6e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 02:11:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 02:11:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 02:11:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 02:11:06 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 02:11:06 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 02:11:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 02:11:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 02:11:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 02:11:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 02:11:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04792101ec738816608625db57309e1ce1f05e1e74515d45eec8a870e1df36b`  
		Last Modified: Fri, 16 Jan 2026 02:11:57 GMT  
		Size: 91.1 MB (91052480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031b2020c33edae07d8fae0604ee3c9dfd99ccbd066c71c697693a4d444d9efe`  
		Last Modified: Fri, 16 Jan 2026 02:11:55 GMT  
		Size: 69.7 MB (69672783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e0407c3f1475e27060a623fa00320b0a596f73107d0e440297138770b365be`  
		Last Modified: Fri, 16 Jan 2026 02:11:47 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80eacb1b5b91c1da2dfaad1a1d3548ffbccf3ef75c868cd5d934640468381dd`  
		Last Modified: Fri, 16 Jan 2026 02:11:47 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1582-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:21838a28705e3e3883afef6835f0ad979e56df183ffc6137c40756814e948394
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5087207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5707ef17c14dd29d16db9506ecaac04ec97c1f3ac44383b7566931c54ca10792`

```dockerfile
```

-	Layers:
	-	`sha256:05c6f97b5b57aed1e4bf767d28a991a6e73abc8fb9432f7217b5101823930aca`  
		Last Modified: Fri, 16 Jan 2026 02:11:38 GMT  
		Size: 5.1 MB (5070540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab8030375d440581291745f811315741f37d120adcacb5c0cbc469a5f390f1ff`  
		Last Modified: Fri, 16 Jan 2026 04:51:09 GMT  
		Size: 16.7 KB (16667 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1582-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:b01246c37d2f4309d707a9615ae8aef545ed03c82e1fc1074798cf91a5300875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.2 MB (199193139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dbd72ebed3cd4de943ac4cb170e2eb5f9f7949e55f84fc98b5840f659fe5b6d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 03:42:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 03:42:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 03:42:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 03:42:30 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 03:42:31 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 03:48:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 03:48:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 03:48:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 03:48:10 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 03:48:10 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cf92d3bf0add4f20720c3232cd336a7f7f50627989684b748675db0b2f2ce746`  
		Last Modified: Tue, 13 Jan 2026 23:17:03 GMT  
		Size: 32.1 MB (32068709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3b35e93b96e6ec97e655f2b0ad366e3b2cfef00f6563db06ed66b91aa30cf4`  
		Last Modified: Sat, 17 Jan 2026 13:41:21 GMT  
		Size: 91.6 MB (91610755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb62495a417705c84861612a20eec7439e88804110457fb141eabfdda0a8923`  
		Last Modified: Fri, 16 Jan 2026 03:48:51 GMT  
		Size: 75.5 MB (75512632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2f3132696a401a89e847e8a845bb600de34f72378823cd266e4e2963f7527c`  
		Last Modified: Fri, 16 Jan 2026 03:48:48 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c61a0e4bd6ebc14c1e26924a33ec3b8fce7997ddae436bb235c2bde2a297debf`  
		Last Modified: Fri, 16 Jan 2026 03:48:48 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1582-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:52ec273b0ad73a8fa8d95386bd2c3a41e5c4d24e6074b5715f0502683e13780b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5087811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a3eacdc974e7eb9d82c3cc629d1c088e2a12bc7a5f7199e1caa49fa544b698`

```dockerfile
```

-	Layers:
	-	`sha256:dcec97976dc31501c1528f8cbb1fda786099c4e2f264ef5c3b7b08e019d55456`  
		Last Modified: Fri, 16 Jan 2026 04:51:14 GMT  
		Size: 5.1 MB (5071226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d075797b4544aefa6ce374d6e7db0f80f80ab831b340ac7460ef47833119c113`  
		Last Modified: Fri, 16 Jan 2026 03:48:48 GMT  
		Size: 16.6 KB (16585 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1582-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:c374b74475aafafe3a65b44b189b60b83fdcda2459240c50b6b2c9a0a4bb58ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183584914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e73b3965675adf26ed29ac03b0feeffcc0edab37101b0243047dc5e887a8b8b4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Thu, 15 Jan 2026 23:23:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 23:23:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 15 Jan 2026 23:23:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:23:13 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 15 Jan 2026 23:23:13 GMT
WORKDIR /tmp
# Thu, 15 Jan 2026 23:23:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 15 Jan 2026 23:23:27 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 15 Jan 2026 23:23:27 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 15 Jan 2026 23:23:27 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 15 Jan 2026 23:23:27 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:08 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2259f118386f883a2d8ab34e36f132523e1c60d0a403567de28c3c9dd6d1a5`  
		Last Modified: Thu, 15 Jan 2026 23:23:56 GMT  
		Size: 88.2 MB (88210675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c441dd29a7fd5744101d109ace8fa25faed3b5c0c28ffad3c43ea92b1b9122a2`  
		Last Modified: Thu, 15 Jan 2026 23:23:55 GMT  
		Size: 68.5 MB (68488781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc41702485bcf1ce6f918fcecf75a75b39860968f25f1f200e4e7af97a542743`  
		Last Modified: Thu, 15 Jan 2026 23:23:54 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535aff5b1a468f72be5b5825fdf6c06a2452b8984912f4b225e8b4fe7e6e2ceb`  
		Last Modified: Thu, 15 Jan 2026 23:24:02 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1582-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:64819898249d67571762f5d6d28b5a081c10c466161615f666f9d711efdae69b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5075152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c419ba6524af9fbec4914215ef82a031400dcc0d28a7b9d81a5d75a32706e5e0`

```dockerfile
```

-	Layers:
	-	`sha256:358bfbc1afe1e6154147ac5a8a62ef73e139aa2be9eed603103c21b69105633f`  
		Last Modified: Thu, 15 Jan 2026 23:23:54 GMT  
		Size: 5.1 MB (5058627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e51fe2766a129fd174d4925e09cd5edca942b2c5997eb89bb7a43face416bb6`  
		Last Modified: Thu, 15 Jan 2026 23:23:53 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json
