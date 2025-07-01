## `clojure:temurin-11-tools-deps-1.12.1.1550-bookworm-slim`

```console
$ docker pull clojure@sha256:040bbac51ee34526673d402c498fefb6bf59225836ec51002cc53dd1a728c369
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

### `clojure:temurin-11-tools-deps-1.12.1.1550-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:077fbb5329413aeaa4116baff1949b88a5b1152fe05c7669791d3eaa5e47c794
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.4 MB (243399988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dabdd472e4dee085cb4d2ac0dc8eedc991ac1c68fc7b12ac2d5dc917916c04fb`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dccc21893abe08f2b082aef4f1427009dbcf1d2a61e7e3b2424f330b6a8ddf3d`  
		Last Modified: Tue, 01 Jul 2025 06:56:11 GMT  
		Size: 145.6 MB (145635595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a3ddb98f0d380293cac20552f9c3421ad039d343c3195fdf3c905b50294da29`  
		Last Modified: Tue, 01 Jul 2025 02:39:11 GMT  
		Size: 69.5 MB (69533607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4dd8137402ae1fb05d0128cdbc1cde1f0b5f07ef29c3e0c4f9b6e2fe94775c3`  
		Last Modified: Tue, 01 Jul 2025 02:39:00 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1550-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:465f4929a5ee87bccb8bab0f1ae3ae60240c5e79e63f7f6311db36a87bf3ae3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5145695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f7a4623d0ceb0af7accd1b587dbc754bc61a015f9d6b756971da1f5e64e7be6`

```dockerfile
```

-	Layers:
	-	`sha256:966dfa2b48722cb90235bc3e4346715932f9bbbe703a96899927682735f8e712`  
		Last Modified: Tue, 01 Jul 2025 06:35:19 GMT  
		Size: 5.1 MB (5131385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62cd970df194d4af471f4bcfd02eb24ca55524d546118435e835c087a7d7bd97`  
		Last Modified: Tue, 01 Jul 2025 06:35:20 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.1.1550-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:25dba85e019194d5b0269148b4fc7ceb66771453b8bd4604b0a7a742d59a663a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.9 MB (239887505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4996b51a004d5b5667ba35ce9b8a0b7cfbb0041e4d55adabd77e1c847347af37`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc1d02c448fe485425583bcbc9b5e3bd61a6bf61836f73f72aced0d452aa9c2`  
		Last Modified: Tue, 01 Jul 2025 13:33:05 GMT  
		Size: 142.4 MB (142420687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de979d126f806ab608fb5a5f629b6dd90444ee3eaeb0b71aaa679f8bdee1732b`  
		Last Modified: Tue, 01 Jul 2025 12:12:01 GMT  
		Size: 69.4 MB (69388498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb82171284c7267c5f62f326dec71db00d2cf87253ef7725c644204f709e32c`  
		Last Modified: Tue, 01 Jul 2025 12:11:55 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1550-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:406bf8ae29f112cdb4f7f4437c5b1b7f63deeefdb5cddd13f5cbee49e2436a6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5152192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed55727beb42a6e26d9050468b0e26c588ad7017f94eb13b0136df3c282c03ec`

```dockerfile
```

-	Layers:
	-	`sha256:ae0aa2fdca18e71e9d626aef1400ca7f6ef7ae9d09fe07870269fab3636ece95`  
		Last Modified: Tue, 01 Jul 2025 15:35:11 GMT  
		Size: 5.1 MB (5137764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3b1a7267b29363bbaea0cf9ccd54e14f416ff3e7a9c17d69899881b3fb5c5a7`  
		Last Modified: Tue, 01 Jul 2025 15:35:12 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.1.1550-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:3acffcd7c4570e16b593dc2093b465408b9add0b26c1e338b176eac082057f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.2 MB (240242016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:617bcdd4a196c55e52df56e5851af059cfaed65cd043cd1771cddc95a9284856`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
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
	-	`sha256:c5884d20b08634214a92bd5de559876bf30e6c5453807c3014f5480eeba20662`  
		Last Modified: Tue, 01 Jul 2025 01:15:20 GMT  
		Size: 32.1 MB (32072820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02a4696a1589b7f993ec4c3885ec710d9efc34062e9aa63943ba38857696a35`  
		Last Modified: Tue, 01 Jul 2025 13:32:41 GMT  
		Size: 132.8 MB (132810523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa598e273687829f5c652f9d14dbcb0f012201c3c0950d4b425550c18460e6a0`  
		Last Modified: Tue, 01 Jul 2025 08:37:16 GMT  
		Size: 75.4 MB (75358028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee11ffe1ceebf7241b4057af65c130f6cd176ec66ff2de5b7eb1f382b70fafa8`  
		Last Modified: Tue, 01 Jul 2025 08:37:09 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1550-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c8cbce389eb6beafd03eb6368b0eb2b23491ef5eeeb18715610565b155624aa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5150286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e39d9e23b6040a6eb1745cd5b49e136b515158dcd6ad019025238a81d8be3e3c`

```dockerfile
```

-	Layers:
	-	`sha256:eb71d5f1e00a96e39b5f258cbef3ef4a081bbb3c446c65978ff6d6ab88fc4a5a`  
		Last Modified: Tue, 01 Jul 2025 09:35:40 GMT  
		Size: 5.1 MB (5135928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b09548efa35e9b2021f4d5655b4df95c6ff3694677633e74cba209b413c0e7f`  
		Last Modified: Tue, 01 Jul 2025 09:35:41 GMT  
		Size: 14.4 KB (14358 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.1.1550-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:1346b0a30992f926f8585967968991103f7d715820a167312337c50eafecdd75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220812583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66c6cd62677c0d80275684d4891b506f3783730362695eba5b74f72e4ea135d5`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
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
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a6e69573d364f51e63b21b21091ef5b3b51cf18a353c8ef9a65a8a43966217`  
		Last Modified: Tue, 01 Jul 2025 08:03:06 GMT  
		Size: 125.6 MB (125585329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6fa3982ae3c16711894bb44c50447d5d4733afc13e7a28a77b1d104c109ba53`  
		Last Modified: Tue, 01 Jul 2025 08:06:42 GMT  
		Size: 68.3 MB (68338800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b31eab6cc89774117a31c28258c233f728aab7843bf814fa254c5b7dc14d2d`  
		Last Modified: Tue, 01 Jul 2025 08:06:37 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1550-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:47b375ea269c20a601a98b70746e45f3d11bc49bb324680020cafdc04f6ece7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d442616d86fa4d4956d28c2eb5df325310907bcc12ca15755038a8db7d2f9f1`

```dockerfile
```

-	Layers:
	-	`sha256:01d4eaad7cb40ef7f7b099102d43d7b1844cab56d991de2f59ffb64052f9fb28`  
		Last Modified: Tue, 01 Jul 2025 09:35:46 GMT  
		Size: 5.1 MB (5122710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bd5ae26510c5a85d335e573167fd1f8972e632723b9f031a49d7fa77477a8ef`  
		Last Modified: Tue, 01 Jul 2025 09:35:46 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json
