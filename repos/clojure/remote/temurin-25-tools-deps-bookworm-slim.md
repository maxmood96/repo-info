## `clojure:temurin-25-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:6fd299aac083366704879583006d91def45a4aa0884a89d47f34f8fbb1ca83a3
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

### `clojure:temurin-25-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:9015a42151c30627fd302ca4667057eb50a3f89f72e6ee6b1aaa42cb4aedf505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (189951765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb21f93b3b94910a95f36ecc2ad8bcfc21b0f40789c045b90ccaf55d5641dc4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:39:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:39:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:39:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:39:42 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:39:43 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:39:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:39:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:39:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:39:56 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:39:56 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:50 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d59a1376786adbfb7c7e278819077b19620977118b7bfe6096d30b4ee46b13`  
		Last Modified: Tue, 13 Jan 2026 03:40:34 GMT  
		Size: 92.0 MB (92045300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2850b63a081a780dd26382a22457c2f6c0b4d2c73b16be6349199eee17eeeeb3`  
		Last Modified: Tue, 13 Jan 2026 03:40:32 GMT  
		Size: 69.7 MB (69676852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9de1ffe1f36c79ec2db4498b385f0eedc372a146c7fe162d0dcbf0f7eaed4a`  
		Last Modified: Tue, 13 Jan 2026 03:40:26 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2a4cf929a2e5e6bd229d498644f9f5ad12e131eeb370a338f791f3b1e5b580`  
		Last Modified: Tue, 13 Jan 2026 03:40:26 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e733498b4f7750df6c0185fe7a022ea977a4d830e3aaa548fe3d7c064d64ab8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5081283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c45a0c9dd156fb6fe4ea29556c634908b41f1c17369a98ddebc1911c1fed3da`

```dockerfile
```

-	Layers:
	-	`sha256:2c072b66bfd839b503e7bfab7b812394cbc124576a493da627cbe2bd002e8222`  
		Last Modified: Tue, 13 Jan 2026 07:45:30 GMT  
		Size: 5.1 MB (5064758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:810f5bb06d2070ec62eb7b86a2ddd789470fc3b7d15798346cbb658a90cc4841`  
		Last Modified: Tue, 13 Jan 2026 07:45:31 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3beb8695b410cc861858d1c631ce1065b499051c34a38170ba641bf518efd4c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.8 MB (188834363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d7c10b04b62ae9cae7a99ef943ac52f41d0fdb115ecc6f7650babc902a7aaf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:43:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:43:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:43:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:43:19 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:43:19 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:43:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:43:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:43:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:43:34 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:43:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:09 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b486d86dddacc8f700b18c4d5effbffcc0558c7b11527d14ec904fa08ab1e20f`  
		Last Modified: Tue, 13 Jan 2026 03:44:10 GMT  
		Size: 91.1 MB (91052515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1956a50e0b2cedb62d94ce727ca082023b73f5990962a6e25354b82c947226d5`  
		Last Modified: Tue, 13 Jan 2026 03:44:06 GMT  
		Size: 69.7 MB (69672919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908d18959876a3c7420fda5b7e98a63b108a9f998a34cdbc0f0ac0d7dac6762c`  
		Last Modified: Tue, 13 Jan 2026 03:44:01 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f8994d179bb6e3615f7c50b108d082999800976d9f4deb0d8d745cbaff0ab5`  
		Last Modified: Tue, 13 Jan 2026 03:44:01 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9883e158b25a13ef1e9545d1b17c8e4a999c0c5cf206aba58561c7c2cbf85be9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5087207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62c82f6e1721fefd26d3d50ed9be047543e14f40c60700ead056dcedf6de0d7b`

```dockerfile
```

-	Layers:
	-	`sha256:37200146e1dc99b1a16c804eacb8eb7826afa5bf9dc7dcee7d6e7a64ec0103dc`  
		Last Modified: Tue, 13 Jan 2026 07:45:36 GMT  
		Size: 5.1 MB (5070540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c179450693c787cff3d280c1e51ad3f301b4ee89a3b5f93f9499cc37133bb2ad`  
		Last Modified: Tue, 13 Jan 2026 07:45:36 GMT  
		Size: 16.7 KB (16667 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:4200a694c5f3713e7d0a59ecb6783c69f316bfa802fdfd1a669890ed6fd41faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.2 MB (199193086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76049dd071783080788e36252867aa2cf560f2d910ab928d24c01d5ba304ede8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Wed, 14 Jan 2026 03:04:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 14 Jan 2026 03:04:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 14 Jan 2026 03:04:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jan 2026 03:04:56 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Wed, 14 Jan 2026 03:04:57 GMT
WORKDIR /tmp
# Wed, 14 Jan 2026 03:07:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 14 Jan 2026 03:07:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 14 Jan 2026 03:07:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 14 Jan 2026 03:07:23 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 14 Jan 2026 03:07:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cf92d3bf0add4f20720c3232cd336a7f7f50627989684b748675db0b2f2ce746`  
		Last Modified: Tue, 13 Jan 2026 23:17:24 GMT  
		Size: 32.1 MB (32068709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba039fb3b2b15cba47b5660c224de13e9c3a8dc2e1d3bd3d3b3a8bd6852d6414`  
		Last Modified: Wed, 14 Jan 2026 03:06:52 GMT  
		Size: 91.6 MB (91610796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73e2dd88bb20b29f6d77d78f6dab8907266f53730577e67fdd83c171aaafda7`  
		Last Modified: Wed, 14 Jan 2026 03:08:16 GMT  
		Size: 75.5 MB (75512542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d39c05c01ec834a1e2d5bb99e7233e8cbb8a96c69ca75cea8126d1bdc79a0cb`  
		Last Modified: Wed, 14 Jan 2026 03:08:09 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d20219ad287af700e4c5ac3eddb71ccbd77930eb317d76787aab901f5acc34`  
		Last Modified: Wed, 14 Jan 2026 03:08:09 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:982af5bd7acefee022d8ef19af5daed8db43715c7c5831c70f22f82072cf1db3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5087811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ba35273da243e9caa88ac2b5654a02dd39434b93aa4bec767c0c6ed12de711`

```dockerfile
```

-	Layers:
	-	`sha256:0a43b25e8b4cb9c3bc88d3f045a49145b632a98b97e5b971ff3ad5b6e6d6dc54`  
		Last Modified: Wed, 14 Jan 2026 04:37:25 GMT  
		Size: 5.1 MB (5071226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af8c5d68a29e83d180f58d46670270194ee9d980fbb85d7b2bcf6c5a0f7f2848`  
		Last Modified: Wed, 14 Jan 2026 04:37:26 GMT  
		Size: 16.6 KB (16585 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bookworm-slim` - linux; s390x

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
		Last Modified: Tue, 13 Jan 2026 00:40:23 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2259f118386f883a2d8ab34e36f132523e1c60d0a403567de28c3c9dd6d1a5`  
		Last Modified: Thu, 15 Jan 2026 23:24:09 GMT  
		Size: 88.2 MB (88210675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c441dd29a7fd5744101d109ace8fa25faed3b5c0c28ffad3c43ea92b1b9122a2`  
		Last Modified: Thu, 15 Jan 2026 23:24:09 GMT  
		Size: 68.5 MB (68488781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc41702485bcf1ce6f918fcecf75a75b39860968f25f1f200e4e7af97a542743`  
		Last Modified: Thu, 15 Jan 2026 23:24:02 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535aff5b1a468f72be5b5825fdf6c06a2452b8984912f4b225e8b4fe7e6e2ceb`  
		Last Modified: Thu, 15 Jan 2026 23:24:02 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bookworm-slim` - unknown; unknown

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
		Last Modified: Fri, 16 Jan 2026 01:43:48 GMT  
		Size: 5.1 MB (5058627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e51fe2766a129fd174d4925e09cd5edca942b2c5997eb89bb7a43face416bb6`  
		Last Modified: Fri, 16 Jan 2026 01:43:49 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json
