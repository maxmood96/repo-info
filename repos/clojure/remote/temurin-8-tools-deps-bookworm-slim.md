## `clojure:temurin-8-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:96849cdd9713696b0696521afb7cc6543f68029cb6ef67eb3183974ad6ac0f7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6723925ac391e2fed70a518269fd87b6dc7bf9e98cd690fddd3ead03eab1d2b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.2 MB (153166194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0cc35a3c862d2b1ae5f08769150b8129a2ac812ef6483c711b9e3d7eef32304`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 23:33:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:33:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:33:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:33:43 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:33:43 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:33:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:33:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:33:58 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87bed87ee33a3a7b6376f8b23437e35cbccd19aec2a8cf375664a0a0d0d2a685`  
		Last Modified: Thu, 14 May 2026 23:34:16 GMT  
		Size: 55.2 MB (55198723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:451dad6371dac5782112f4972b3f6ee33ebb0fe30016d18843b9dc326eb00a02`  
		Last Modified: Thu, 14 May 2026 23:34:17 GMT  
		Size: 69.7 MB (69730542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6088fb5773789e22a8a6859e9950562195fcb86a2d7316da740b23ae38ecd1`  
		Last Modified: Thu, 14 May 2026 23:34:14 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5bfd09f8de5d2c80beb5544fc72126bdd4b4b8d2abc23d8f7c0f4b1df2c07a23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5251552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0c5695d366e585e3ee422cf07d5191e952768fea6ee6ad0b5422d53e2054d0f`

```dockerfile
```

-	Layers:
	-	`sha256:d72996979bb5f5ed9e88bc95a21ffbf1b741ee8a551545bedf0d984b0ea41647`  
		Last Modified: Thu, 14 May 2026 23:34:14 GMT  
		Size: 5.2 MB (5237152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce4863df287fba27b6b26bb1b02f3fc898804f4b4aec005c5b578915bedb10fd`  
		Last Modified: Thu, 14 May 2026 23:34:14 GMT  
		Size: 14.4 KB (14400 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7f43b53f9d418d830a7c28e3ae28bbc67eaad41e26b78cda3538aaab53aaf3ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152111857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:537889d13eb098ed6a386fcbdd0b210dfad543eb30996875b109545781cfd26a`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 23:33:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:33:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:33:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:33:35 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:33:35 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:33:49 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:33:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:33:50 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df72c14f53dc2dd4592d4f850c41a419f398c87aa8a1a3044546d017444f5383`  
		Last Modified: Thu, 14 May 2026 23:34:07 GMT  
		Size: 54.3 MB (54272927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7977a0bdeef9c8098bb168b694eda841243695436316f640f0a071471af286`  
		Last Modified: Thu, 14 May 2026 23:34:08 GMT  
		Size: 69.7 MB (69722119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661c8be8eced217ac51b8502af876044ed1653f54aa36a42444e245b40822551`  
		Last Modified: Thu, 14 May 2026 23:34:05 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5245adaf2e3fdb9eb802b518e686af0d4580cdc6843449b136b360407a733ef8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5258133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b96f579891ac18c248aa88aca30114e6c748287733c36413c03a0fbb2d1c799`

```dockerfile
```

-	Layers:
	-	`sha256:4fcfaf1f96a54ecec9d161b513e13cb22a1258b9c97a4a5c3c8d750a689d14e3`  
		Last Modified: Thu, 14 May 2026 23:34:05 GMT  
		Size: 5.2 MB (5243613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:465254c94b002cc5071a86a1bfed373e1df260a3e3d21019508c4abfa0a6ecfe`  
		Last Modified: Thu, 14 May 2026 23:34:05 GMT  
		Size: 14.5 KB (14520 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:2b867efd61a61efac0d4599df5dd0e548d874aa2b24a0c06d3a32ecf1072c757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.3 MB (160314129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e0a2bd73da805c53c667b9e4b21926e5a328deb3dd01c2faa8e382bcdab6f84`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Tue, 12 May 2026 21:46:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:46:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 12 May 2026 21:46:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:46:26 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Tue, 12 May 2026 21:46:26 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:34:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:34:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:34:19 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0e29ea7436ed4beb1c38bcfee44589407e49fc690669b42b35db33a9588e820a`  
		Last Modified: Fri, 08 May 2026 19:44:06 GMT  
		Size: 32.1 MB (32078453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57a4137454cc0810d06042c272eb08276000e4b66a91f77145ef48d12c8463a`  
		Last Modified: Tue, 12 May 2026 21:47:32 GMT  
		Size: 52.7 MB (52669152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e1eb6848e73f237be44814acf27a85152440ca74d0f7fcc3aacadc7b846ff0`  
		Last Modified: Thu, 14 May 2026 23:34:53 GMT  
		Size: 75.6 MB (75565876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a079776975e53377f91f04061bb1ce3ff7d0e3c3d1c9dc4b00802f42de23db3`  
		Last Modified: Thu, 14 May 2026 23:34:51 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:136dc0bac8d736bf39c4f554da5d047ef1b29a8a8bedb1dd362741c930831cd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5257355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0224e6a45ef377a68ce7266e867513298ebd51c5d0cf4f4425c8b6db9a263d7`

```dockerfile
```

-	Layers:
	-	`sha256:972bec602fca8d23bb62cd88b8bc9df3141d6135b4f910471a6a8923dea91106`  
		Last Modified: Thu, 14 May 2026 23:34:51 GMT  
		Size: 5.2 MB (5242905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa4fb2763d4f274c6cade86f1ae3922bf8b8823683686cc05d9818c1f3b61106`  
		Last Modified: Thu, 14 May 2026 23:34:50 GMT  
		Size: 14.4 KB (14450 bytes)  
		MIME: application/vnd.in-toto+json
