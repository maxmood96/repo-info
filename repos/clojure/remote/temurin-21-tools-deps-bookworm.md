## `clojure:temurin-21-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:4d332a3761fe266ca45d9e4b3ab531f80df194fd969e6bd8bb8ee8cb6b9f3c94
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

### `clojure:temurin-21-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:a54de92604b73da4c9ea9268e1602a4ded71e6710d6fcea023d817e5118b469b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.5 MB (287454648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83c9209de503126ee63cd674e6b79bf11130625a61f06b942ab54a3309e45009`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:35:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:35:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:35:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:35:10 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:35:10 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:35:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:35:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:35:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:35:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:35:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:40 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d583676ee2894dad7a9afde419d6a4b09a062ae13ed46a3fc862bce43ae3f029`  
		Last Modified: Tue, 13 Jan 2026 08:29:02 GMT  
		Size: 157.8 MB (157825959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95cca145680f9ab5e3e0181929c2bcbb974ed7f996d0ba48306a0e920af0ed7b`  
		Last Modified: Tue, 13 Jan 2026 03:36:04 GMT  
		Size: 81.1 MB (81146030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a61d67df7f6a6cf956197c7bf7aef0d081e4e76185624d16ea5798d7206a53`  
		Last Modified: Tue, 13 Jan 2026 03:35:57 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d75bbdfc1beb15060165d94a85f6847801b8e0e420ab56d8eb7c2b34aaf044`  
		Last Modified: Tue, 13 Jan 2026 03:35:57 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:a397af2b5fbbfcb8ce3080164481cb1b360a2691b9c1a5334cbc2469f75a7e8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7395783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bcb505531120210f4a5454081471b466f2d24d1431ff893e18208a237966e77`

```dockerfile
```

-	Layers:
	-	`sha256:97efe6481dea24a8a0c24140b2b78362ea16fc4d39f75b6600dad36118f08d12`  
		Last Modified: Tue, 13 Jan 2026 07:42:16 GMT  
		Size: 7.4 MB (7379321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6af179faf421a620347e4230f3d54bd59c658a28f7557e63c15273ce950085c`  
		Last Modified: Tue, 13 Jan 2026 07:42:17 GMT  
		Size: 16.5 KB (16462 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d13e7e98201e597c7d14a71df3c76878058d8a95e603fa0110feb3681e127be2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.6 MB (285613753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49cacc7acb923a7fa7ef398bc76f70227327b4793e9d3aded64802e0a1a5721c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:39:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:39:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:39:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:39:13 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:39:13 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:39:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:39:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:39:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:39:29 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:39:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:34 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862051eefce9b32783eef63cb079e3d0350b5222c540c1086e857a3cf27ba87c`  
		Last Modified: Tue, 13 Jan 2026 08:11:56 GMT  
		Size: 156.1 MB (156107651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:069ac32e33c77f19bfcf9b96685251655ff1c1993b01018a3e6bb462e81c8083`  
		Last Modified: Tue, 13 Jan 2026 03:40:09 GMT  
		Size: 81.1 MB (81138993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121b4b116851a1567a3dda7fc78d31b934b1a6e2011ecdf4da29fda734086d23`  
		Last Modified: Tue, 13 Jan 2026 03:40:03 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd940fffb6bd94f4b1bd4b82e3062c8d51bc5edc967ef54750f694629a42e67`  
		Last Modified: Tue, 13 Jan 2026 03:40:05 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:ca35e8f1637750e0d9d2351c7aec72c0203f8815585d25b458213dfde1486e55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7401712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5d84517eaa59ec2ac644df8f37f67b379870a8644aace93a17af14fe1d58198`

```dockerfile
```

-	Layers:
	-	`sha256:a8768067ad7bbfb599e3bc9c608c66d96ea5cd9ed99920ba61b99e0b976808ff`  
		Last Modified: Tue, 13 Jan 2026 07:42:24 GMT  
		Size: 7.4 MB (7385108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bf3efbaa6ef70057fcfdc101ccf344deaeb951a6fd1a9e6543efee9e42ab4b8`  
		Last Modified: Tue, 13 Jan 2026 07:42:25 GMT  
		Size: 16.6 KB (16604 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:7ae8628de06492f4bf7a652a293f6583a34d5deb71d67b371c3c83f353ff610f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297257748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69ebbc168845e4b56dc82656fcd8c5ac4ece550f52b826edd65179aeaf9906f7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 05:45:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 05:45:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 05:45:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 05:45:24 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 05:45:25 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 05:48:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 05:48:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 05:48:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 05:48:39 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 05:48:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7fcf9f2b462d6af06c3ad2420b999e6b092984c4723ebac480c428a5d837d3b7`  
		Last Modified: Tue, 13 Jan 2026 00:40:39 GMT  
		Size: 52.3 MB (52327376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8804680ddf0e6491c95d8d7bb1e9bc4a8f40508c1c43881c7cf1ac223df9a2`  
		Last Modified: Tue, 13 Jan 2026 05:47:06 GMT  
		Size: 157.9 MB (157942951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3000e00234f26db15e59158d95782aa19c5c0f6bdf3221f1c844e5c6e4136b17`  
		Last Modified: Tue, 13 Jan 2026 05:49:34 GMT  
		Size: 87.0 MB (86986381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c9229a04ffdbb0f1824a86145713145c7b60d34c942701dc12a69ad8b1fb05`  
		Last Modified: Tue, 13 Jan 2026 05:49:28 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da7d9d85621b33fd16b9b618545c86e1df052ae39910dbb465d7d0c9e814e3d`  
		Last Modified: Tue, 13 Jan 2026 05:49:28 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:abc06ca4085ba590423431525fb6751eaf2835fb7b9825e1d240b5d9a041c765
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7401071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce2d8abdb4f29fc8548d693c890e82b9fa3863ee4b75c70ca28278ecef96b429`

```dockerfile
```

-	Layers:
	-	`sha256:dc9287865292ce3b6b7b8ccf65dc7d00a3aa6b11eaddbf73fd93f265e42e18c4`  
		Last Modified: Tue, 13 Jan 2026 07:42:31 GMT  
		Size: 7.4 MB (7384549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8080ab1f697d17e86cf4637f3944c841d3ac2912738ffe09f82c37881ad61fbe`  
		Last Modified: Tue, 13 Jan 2026 07:42:32 GMT  
		Size: 16.5 KB (16522 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:de0d814d78ec0bbe5c1e0b2ef3b679462bad84330c731ed09ca751b6a67d42e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274168401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574fb91f264c8c2cfa2677a7e03b7f29426531b5089893c581d9d2f71a127b09`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:06:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:06:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:06:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:06:51 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:06:51 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:07:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:07:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:07:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:07:05 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:07:05 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:533e1723f6efd3a2dac5ef2d710062f1e6292bf061b83d41b908fe862b8922dc`  
		Last Modified: Tue, 13 Jan 2026 00:40:26 GMT  
		Size: 47.1 MB (47138430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec63107eaeb3d1d2abca4ff87640859f745a8eee48006304ca542cd5d1de53d`  
		Last Modified: Tue, 13 Jan 2026 03:08:00 GMT  
		Size: 147.1 MB (147069812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5264c3f8ff0565816c136e01c00c38e3398fb67c60bb8a7505b6752ebd8f3f9a`  
		Last Modified: Tue, 13 Jan 2026 03:07:57 GMT  
		Size: 80.0 MB (79959124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23759d1167c12ba79669c316607cb751915f80a1b2b4e8fd84808b634b34f8a`  
		Last Modified: Tue, 13 Jan 2026 03:31:18 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ad1a0e68cb2ea1de581384cdf771b83f0a9a4b109a7a3f2854b21ebcd8b1b3`  
		Last Modified: Tue, 13 Jan 2026 03:07:42 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:dba4c14dc572964830c69d34c90f6eac52fd4a336cedf9ea60f05cd277bae7a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7387102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dbb9f3b0f71a881e9be29ea4d882b1f5f6e451465c20e094f4c0b80758860ca`

```dockerfile
```

-	Layers:
	-	`sha256:7b80d1b3d50d8b8c155c6d1971f15742d4a6c5d58df911334171bb5289a240fc`  
		Last Modified: Tue, 13 Jan 2026 04:38:43 GMT  
		Size: 7.4 MB (7370640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8339c2440d37702ea58604cca1bb155449f324ab31421e1cee1fba3a79ca2d0e`  
		Last Modified: Tue, 13 Jan 2026 04:38:44 GMT  
		Size: 16.5 KB (16462 bytes)  
		MIME: application/vnd.in-toto+json
