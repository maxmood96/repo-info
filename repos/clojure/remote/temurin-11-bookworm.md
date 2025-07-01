## `clojure:temurin-11-bookworm`

```console
$ docker pull clojure@sha256:1647467e94d2d783855d455a17a0680fa7c37dac388e00d8856a6505b69ce716
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

### `clojure:temurin-11-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:65e2df7a337baadaf0e5cbac26f240fdaefcd2b045880759053e421099384110
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.1 MB (275123470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a10e20240cefaa6e9ab064b1059aaa837ec8e199b3cab9b4c23b7bfe7b91045`
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
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd62fb65bf74c8cb6b31b8d5d992bc8902d6446d85752d5fd9fcecc824d1748`  
		Last Modified: Tue, 01 Jul 2025 17:46:41 GMT  
		Size: 145.6 MB (145635655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf0b0df025938fdcb52b1061034db6a2547833c851217f0c8e84e9c5d977344`  
		Last Modified: Tue, 01 Jul 2025 02:39:05 GMT  
		Size: 81.0 MB (80992887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0d28cd452f59660b78c85faf56766bf908c619ca2e3cf864f6cdff302f7250`  
		Last Modified: Tue, 01 Jul 2025 02:38:57 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f7afaefcffd789e903f66403cebf1d33f12f5ccd5660c02a659ee41b28ba406d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7402661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2cc9483cad8fe652fc0ff7f705cdc8d01aa9d9db4789f40af9b8fd63b4ff589`

```dockerfile
```

-	Layers:
	-	`sha256:23849d452ce806d107d8e4714c9bd2e29176c8e2ed1666b3a90871956690433b`  
		Last Modified: Tue, 01 Jul 2025 06:35:14 GMT  
		Size: 7.4 MB (7388409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd1daeca05d9ac8a62c341c7dabae913c8da1b7c66cfd8a6f238b0bf124e3b01`  
		Last Modified: Tue, 01 Jul 2025 06:35:14 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c516d8a2bd724752dee39fa9edf6dea360b95ee4be9ba656107e5ff42d39d629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.6 MB (271611556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4ff4c9fd142a979cb6fa84ed32d41ef9d1103a1adef0c4a6ab5ae9e62f965a2`
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
	-	`sha256:1f8ab7c4e8b4178f5f2504f6c4b199268151b1fc958cd53bb861d8dbd9faa8c3`  
		Last Modified: Tue, 01 Jul 2025 01:15:08 GMT  
		Size: 48.3 MB (48338785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641d690a167598ceb222525d3f12f2d1a9a8af6830dd7b301ad7edba141543ba`  
		Last Modified: Tue, 01 Jul 2025 12:05:31 GMT  
		Size: 142.4 MB (142420640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b091d3f116c7c13bb3b00fe704a1ee7aaaecf6d041869334053bacd5f7cc9b`  
		Last Modified: Tue, 01 Jul 2025 12:11:23 GMT  
		Size: 80.9 MB (80851488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0620857473b301af6c23749568538d87ac8ae4846cabcd731bf406de1e7d00b6`  
		Last Modified: Tue, 01 Jul 2025 12:11:08 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:6b59ab59ba0c6c37ab34c5dc48d78da18ca31f6d0c87538b662c66172018dba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7409160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dd5feae5fd6c7a6e202ade6c614acfa65c91fc1744c1f9c9553e69bdaa06e40`

```dockerfile
```

-	Layers:
	-	`sha256:eeff6693997c2f262501f960de2ec9ba39f04b2fbe60724372348048a55ba672`  
		Last Modified: Tue, 01 Jul 2025 15:35:10 GMT  
		Size: 7.4 MB (7394790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bd27637e6b357e0d6c3dc7de4441fd50ac2837d24c98c8bc01072ce159aa8c6`  
		Last Modified: Tue, 01 Jul 2025 15:35:10 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:ce6c5f1b612b9de24a65be55c2030a605d45c5c4acc1c12341a577bf0cbe6037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.0 MB (271967867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c7db6e5dc60b71ffc1918f69c2422d45dc349f15e6c41005ba17b046ff41d19`
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
	-	`sha256:2819217d87219cbf8b5ec7dfbc47c9a16195c7992a9fbe92da8723c42180b19b`  
		Last Modified: Tue, 01 Jul 2025 01:15:05 GMT  
		Size: 52.3 MB (52337243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63c633f9e5d44c1f765a009b05c519412a7c78d0bff2e37793b7681c50f85bb`  
		Last Modified: Tue, 01 Jul 2025 13:32:39 GMT  
		Size: 132.8 MB (132810531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48fd3329abbe2ec5dacab52a0cdaad3c9571ec5ca8dfce07e88a8f7548cd85e0`  
		Last Modified: Tue, 01 Jul 2025 08:36:14 GMT  
		Size: 86.8 MB (86819449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:279c9a3553b36bf7e1f8e001213d6381152651cf794fca89151627bb3e49e6f2`  
		Last Modified: Tue, 01 Jul 2025 08:36:01 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:33393f3574119bfaa4885a3a3373ec02cbe7dcaa884b0c7b9a7bc05ea63e60ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7407298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:085c95cf73d4eebe59d90cbce29e226bf5516d70ad2e52f56d096835809a2947`

```dockerfile
```

-	Layers:
	-	`sha256:95312b7911c5e8ab77e7af7e03c1857b899ce301effefeeacea18d26d2880e49`  
		Last Modified: Tue, 01 Jul 2025 09:35:31 GMT  
		Size: 7.4 MB (7392998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfdcf214f98498ff099a395c9b11c9ce2d1852d1635e85cd364ae29dadff0382`  
		Last Modified: Tue, 01 Jul 2025 09:35:32 GMT  
		Size: 14.3 KB (14300 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:53489afa97cb6476e3105c70a0b64d82fbf541f8fd943eb449b2a31df3dbfa7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.5 MB (252534793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18aedc3e43f3212ff8e28a1d1394ebe8d6edd3fed71160a08f26c60bbc2ff0d3`
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
	-	`sha256:f5e945529523ccd9610b7c0253cda59a29c297f0a697f3c402695e1c6ecf5e6c`  
		Last Modified: Tue, 01 Jul 2025 01:15:47 GMT  
		Size: 47.1 MB (47149287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36692572b1746a0d5517d83cbcbdccbb01a61f61c1ca871d6292e6483cd070c6`  
		Last Modified: Tue, 01 Jul 2025 08:02:07 GMT  
		Size: 125.6 MB (125585349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f197f41e70659b011dd80f9c8945732de4237934b2ae75d72c3fadb2e600a3c9`  
		Last Modified: Tue, 01 Jul 2025 08:06:04 GMT  
		Size: 79.8 MB (79799514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29837a426d12b4e3fa322c2412bfc551c8e77d086396b81a043d198c753701a4`  
		Last Modified: Tue, 01 Jul 2025 08:05:55 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:eb90d273179551dcb481836a2fdca5c1e63def4510c455ddd1350b28d27a26b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7393982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e1f6b67af1f7276a2bc1a6bf371309bad0300165f59bc33aa4ca9a5959841f3`

```dockerfile
```

-	Layers:
	-	`sha256:3ae2163340a5c69cc9f51a1b21f6ee22b9560cd4bc287782a6578545b9f460be`  
		Last Modified: Tue, 01 Jul 2025 09:35:38 GMT  
		Size: 7.4 MB (7379732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:604fbf5ff870c205005fdc2aa893e4a6b806f6b69365099660acc51e1b57acac`  
		Last Modified: Tue, 01 Jul 2025 09:35:39 GMT  
		Size: 14.2 KB (14250 bytes)  
		MIME: application/vnd.in-toto+json
