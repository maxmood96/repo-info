## `clojure:temurin-8-tools-deps-1.12.2.1571-bookworm-slim`

```console
$ docker pull clojure@sha256:04a6634bb52a9397abde1ca3ac4b0f59db19fe7cdbb8e4502e87a2396d59b537
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.2.1571-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:db7ecbe1b14f586e7658fd4203fc3c6600dc05567830124e647cbae9d3586469
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152635138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a21f1b48b346b7712603fbda4a91f6c05c9f5617224bd42ce7fc1e3bda31ee6`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2d2053102e207d6be73e44ae922482b252220dff830abcc5e8d31fd0300c91`  
		Last Modified: Mon, 22 Sep 2025 23:44:02 GMT  
		Size: 54.7 MB (54731284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d0be82823d3c4a71d210677fe528c7ffcf2d6e3bc68e364a51e4ff4318635a`  
		Last Modified: Mon, 22 Sep 2025 23:44:26 GMT  
		Size: 69.7 MB (69674861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf2c62eb48128103109fed29b80669a26621209699c17de269f78065f095710`  
		Last Modified: Mon, 22 Sep 2025 23:43:57 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.2.1571-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f58172b35c46c22ea375293785cfa08ed2487240a881eeab641c127c3a6fdfac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad94c720aeec5f643d4d5a174347335d77ead2fcf8028d83a8aa4a8fe795a764`

```dockerfile
```

-	Layers:
	-	`sha256:d4a88706e9929eeb03948add9955c0473da0a751cf7643ef29ba6b1745950c2d`  
		Last Modified: Tue, 23 Sep 2025 00:46:32 GMT  
		Size: 5.2 MB (5234998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a944620669983dfd3b585c0a0337fef4374607589ec6e2b44488c7b95c0c0cd4`  
		Last Modified: Tue, 23 Sep 2025 00:46:33 GMT  
		Size: 14.3 KB (14290 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.2.1571-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8294ac9a387a9b84963a62275bfaf25dae9c3c3205089f9dae641fba8314a0de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.5 MB (151501905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7fa819724f59bde8462e4b4a3e60d4b371503b1688c7f0a325f900150835c9e`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64177e1b15a9e1d556c03e2ddaf672633f0a541da04309ed67b60df66d7b3747`  
		Last Modified: Mon, 22 Sep 2025 22:16:00 GMT  
		Size: 53.8 MB (53835607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ec22f0b697c70d7765b534aa32f8b23595521195d9205134dc6c3d6c0376bb`  
		Last Modified: Mon, 22 Sep 2025 22:16:04 GMT  
		Size: 69.6 MB (69563553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed835d13c239f2e971ec1305f337d85e40a45c923a9eb99d101dc5f2c096a556`  
		Last Modified: Mon, 22 Sep 2025 22:15:53 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.2.1571-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4647ca13dfa6221b25ef06e985933c2dd292fb89b0641339ebccee95f9d5a88f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:069d75b2597b820163232d6c7812f5f4e0c3cb4957a7ebc58e7f5f1f4c312691`

```dockerfile
```

-	Layers:
	-	`sha256:a4eb6f6c18d28c1e0a23a760ddd125bc51eb78fc15ea4f4c6da4138128fd53fc`  
		Last Modified: Tue, 23 Sep 2025 00:46:37 GMT  
		Size: 5.2 MB (5241457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b14bb549db54eeeb69c01bad825894f5ff64a397d35900feae2d903f0ce07aed`  
		Last Modified: Tue, 23 Sep 2025 00:46:38 GMT  
		Size: 14.4 KB (14408 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.2.1571-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:49cbec3d0d84bb52dbd661b0184c399c7c8559ee57890e595d835b4861222076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159748101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae7fb9add06eeeeeb0863e90fda8625a78dbc4023c342e5e30a72e6227acc1a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:a438293490bbc2af66661166949a4d86358eeb39f9fadd5b0146666f05b9b9ac`  
		Last Modified: Mon, 08 Sep 2025 21:30:47 GMT  
		Size: 32.1 MB (32068762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed13d84bff762045539b913e52a0729034d3e873c719091b50c82ea6d8b6d03b`  
		Last Modified: Fri, 12 Sep 2025 23:44:39 GMT  
		Size: 52.2 MB (52165358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0196edaa68f9953979f84a694cd57b9f00613973de70c0028c71f32fc5875255`  
		Last Modified: Mon, 22 Sep 2025 22:37:07 GMT  
		Size: 75.5 MB (75513334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94907d42095ddfd46683f514b5d5a6db540702d5d884f0a24137157bcf1ca6f1`  
		Last Modified: Mon, 22 Sep 2025 22:36:54 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.2.1571-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:58a89acda374cf8726143721930b524a728ce459c338d6e17b69b952df948af1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:585152cf437d1cf2c636c54fe92e78146f2e5a93c878fd01f9f1b8eb91899250`

```dockerfile
```

-	Layers:
	-	`sha256:7bf1c3799e30f030559fae5775e2c2840000beba912d4bcec6babe70bf7f801f`  
		Last Modified: Tue, 23 Sep 2025 00:46:43 GMT  
		Size: 5.2 MB (5240749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2a63d5dc06f213480677b9bd4bcf06b9c0336966af354ed56b45b661a133a4c`  
		Last Modified: Tue, 23 Sep 2025 00:46:44 GMT  
		Size: 14.3 KB (14339 bytes)  
		MIME: application/vnd.in-toto+json
