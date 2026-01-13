## `clojure:temurin-21-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:93efef1fa391b2aad43ba9a73725273df29d19ebea1b9a955ef273e85458b18a
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
$ docker pull clojure@sha256:a6ed58d4b344d0a081e926ac88fa56439759c603e89ecd35dabe4ba80213d504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.5 MB (287454928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3bb845045ef78cebd2ec9a97db73e6b901e507536f517594933624e196f9c78`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 01:03:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:03:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:03:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:03:23 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 01:03:23 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:03:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 01:03:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 01:03:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:03:38 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:03:38 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea3563cdad36c1222a88e24ee316bcf4d48bc679cd6d8c26e60255c52e25dce`  
		Last Modified: Tue, 30 Dec 2025 01:04:18 GMT  
		Size: 157.8 MB (157826042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b26c8ecf7a818bd76d02f725d0f63114624fbd0491ef34de25ad4054d93e54d`  
		Last Modified: Tue, 30 Dec 2025 01:04:12 GMT  
		Size: 81.1 MB (81147051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d945381b088df8c893f508d37a27bd706bdc14ccc0ba0f77f0e37364771e2909`  
		Last Modified: Tue, 30 Dec 2025 01:04:06 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5b27ff29d7089792c81c771a7befcfd3dcd53dc3f966fe1f121cc33c419715`  
		Last Modified: Tue, 30 Dec 2025 01:04:06 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:597acafe6b487925d1d45881d4777ce3c80d8fad80bf194f0769ef4826d576a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7395140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:022404e8b0e03c08b262eb684224bcc4013b45fbf005c2e8b8f943597ddb0217`

```dockerfile
```

-	Layers:
	-	`sha256:a701a750ad30ed1f9816259129d7bc1deee0dc9f0b35ec555821412beaba8b28`  
		Last Modified: Tue, 30 Dec 2025 04:42:44 GMT  
		Size: 7.4 MB (7378678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9f9f3c194bca9d8fae684ae4bfeb53544c2d8cc22f61e5442cb25c81b10e912`  
		Last Modified: Tue, 30 Dec 2025 04:42:45 GMT  
		Size: 16.5 KB (16462 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1cc5773f2dfa7053df1f5617eba92266ac7287241b261dcb2411af12147b5b79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.5 MB (285493794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:621c32535098007cb0e1f59ca9bcf9359bf645831563a1ed1d5afc8c272bc3df`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 01:02:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:02:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:02:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:02:19 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 01:02:19 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:05:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 01:05:03 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 01:05:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:05:04 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:05:04 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:bc82f51ad2e6d256131f87c3aebb045333f03c39e64a6b4985cc9e6ea5602d4d`  
		Last Modified: Mon, 29 Dec 2025 22:26:42 GMT  
		Size: 48.4 MB (48359147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744000bf154ed9411b9b928e26e7796f03848939d9160ed9b1b49c76651c3b7f`  
		Last Modified: Tue, 30 Dec 2025 01:03:14 GMT  
		Size: 156.1 MB (156107673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1cde0a5347c0fd62a376ed61357763f1458f951982c4175167076d64e40327b`  
		Last Modified: Tue, 30 Dec 2025 01:05:39 GMT  
		Size: 81.0 MB (81025935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:740a39497ecd1156a4ec5debf5ca50e204b85e035db279f205097640d4f06aa6`  
		Last Modified: Tue, 30 Dec 2025 01:05:28 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e5f5313e964d0b2cb0f02655eb214a85c563a192702a186082b987dd2ff394`  
		Last Modified: Tue, 30 Dec 2025 01:05:28 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:9f367008034a8b8bccad536ac7880562de221c1ab8f948457018d21cbe727808
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7400267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fd2c056c331e17fc13fd8bf54232b42bd0d252219bd285180cd8eab8cfb6cd2`

```dockerfile
```

-	Layers:
	-	`sha256:24598a881e1c69283e18cf0c79b904076e1c99ec3c0ebf5655eb33a68d216102`  
		Last Modified: Tue, 30 Dec 2025 04:42:51 GMT  
		Size: 7.4 MB (7384465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0250aff6ffcc6066cbfe8dc2d2138ae8d74729088dad383f0adec8b3273f8d21`  
		Last Modified: Tue, 30 Dec 2025 04:42:52 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:c6db6ae025927573d26c4704c0f0f98739e751be704355a151edb74b4cf47f68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297253333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86d90b05e9d8b7ab39f9270ab4e78c9ad3ac91fedb75a79a816ce680e479f921`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 01:43:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:43:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:43:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:43:53 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 01:43:54 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:46:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 01:46:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 01:46:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:46:45 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:46:45 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:48e256c4119c0ad256492d6a930e99d2b2d7f8d7920d619aa2de4f616c37076e`  
		Last Modified: Mon, 29 Dec 2025 22:25:39 GMT  
		Size: 52.3 MB (52326998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9d97546303efd08b59676c0ae34293278a22e0472a5e5aed8160ac03056604`  
		Last Modified: Tue, 30 Dec 2025 01:45:40 GMT  
		Size: 157.9 MB (157942939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64a6a42d6b53e935a248ab194a27b68938c36d24c82e5c8d98cf38d1b531fec`  
		Last Modified: Tue, 30 Dec 2025 01:47:40 GMT  
		Size: 87.0 MB (86982355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c4494e4b09777554e1d41982d2bd4ff021f9efa0a1d6c9d6de2bf0e6de368c`  
		Last Modified: Tue, 30 Dec 2025 01:47:35 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e45d08a39e9efbc4df054481b6680614faf68ebe78859670557acb677e6abd5a`  
		Last Modified: Tue, 30 Dec 2025 01:47:35 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:db7e4e96a1dd28b952d3543814d33c157a249550ca8c3e08d3fa9c47d9ee6bf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7400426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:830a7063f6158fd823bfa479d01c60fd0275261fde9c175111c4af806b6050f9`

```dockerfile
```

-	Layers:
	-	`sha256:fe88d8591b03198a36d1ad06a9e9eaefe290f683357b3676b25c6b14a1b21c1e`  
		Last Modified: Tue, 30 Dec 2025 04:42:58 GMT  
		Size: 7.4 MB (7383904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd813ba52eb3fca27e946a808e8cc13634d95d040899d58add49a6fa7c391360`  
		Last Modified: Tue, 30 Dec 2025 04:42:59 GMT  
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
