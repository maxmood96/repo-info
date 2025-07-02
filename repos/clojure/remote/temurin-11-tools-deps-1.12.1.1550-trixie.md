## `clojure:temurin-11-tools-deps-1.12.1.1550-trixie`

```console
$ docker pull clojure@sha256:3073e801c77dedf44904e4bad5286252c9156444b069d1de49fb4e3e382850f4
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

### `clojure:temurin-11-tools-deps-1.12.1.1550-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:dbc5cb432c07188d1cf361f55c5ab9f90bef48611ac85bf73b7f715f98591f29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.3 MB (280255231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdb7a76f246280877256b27eceea622c1f9e6ffa64fde38da691b3c4475c97a0`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1751241600'
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
	-	`sha256:b72fed6e2775feec9291a4bd4b416f996dfc503eda11eaa00def55711302b4ce`  
		Last Modified: Tue, 01 Jul 2025 01:15:00 GMT  
		Size: 49.3 MB (49263877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f93f1923d9c255a441deddf37751562c619383c2b3016138c88ee4cb061d4b0`  
		Last Modified: Wed, 02 Jul 2025 04:17:03 GMT  
		Size: 145.6 MB (145635777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1587fa3ab85a22dab2cd5f12731cbf6e8e6eff8317e92225a152bf51b2faa251`  
		Last Modified: Wed, 02 Jul 2025 04:17:25 GMT  
		Size: 85.4 MB (85354932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64482e3813f2a1a16fb38ecddf7babbd0f01c97cd479458fdf2538a22e49977b`  
		Last Modified: Wed, 02 Jul 2025 04:17:10 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c8d09d24a74d6c114db4b3ce68836eb62977a87728a803ab7e73676c1fb4f657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7493521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0ab672325f89b5313f109936b60593407d26c4943127bca6e1a7b1e1275f1d1`

```dockerfile
```

-	Layers:
	-	`sha256:4fd5911bd0ee9847debba246eb0d134f0956167e5c21c69aeabdaa43694167e9`  
		Last Modified: Wed, 02 Jul 2025 06:36:41 GMT  
		Size: 7.5 MB (7479294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4928c8cdb5d2dfce72eadb966173fa6fe46ddab4dd32e5a6f3ddcadbf06cf403`  
		Last Modified: Wed, 02 Jul 2025 06:36:41 GMT  
		Size: 14.2 KB (14227 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.1.1550-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b102f9e976709c65280527ef2c430e6e61991b7203a2789a59ca8f935d6ba62c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.2 MB (277223149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cba7a48ee0a55589ad52a49304776b3df40ee063d0f5df92124e2e7921c0d88`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1751241600'
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
	-	`sha256:2581a046e315a4b3013d50a17da46bcffbba144014a55d733fa55c3bafc6b7ab`  
		Last Modified: Tue, 01 Jul 2025 01:18:05 GMT  
		Size: 49.6 MB (49630154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e6339d5adb3a9918bbc55cf5d0e99be79d094dbf68f1fc790ad1fc33ef9444`  
		Last Modified: Tue, 01 Jul 2025 12:09:02 GMT  
		Size: 142.4 MB (142420639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32abd5e5ca1164ff2fe7757b1ebf1ba4bbb0f46d7b874514bf6164fc37e14f20`  
		Last Modified: Tue, 01 Jul 2025 12:16:23 GMT  
		Size: 85.2 MB (85171711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12b8babb3ca6cae8eb772696ceffa07538b9bb88ca5ad0bbdd1e649d08685d2`  
		Last Modified: Tue, 01 Jul 2025 12:16:15 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8d5aa02f5389a75eca3ed5512e19433086c419016dc024910f44f299f8d10639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7501288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99c3bdd3d35c1f5ab49c7a0ee256de8144822a3bf2fb236933ab01d8c02a6d6a`

```dockerfile
```

-	Layers:
	-	`sha256:3f16673609b13c484a0926c3cc1c85adb1b4470ec03e1c4cf6e50d55dd6341a5`  
		Last Modified: Tue, 01 Jul 2025 15:36:14 GMT  
		Size: 7.5 MB (7486942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d4d2894867a682a3a2ac6a540ee33ee3e70bdef261f53f93c59610dc9d64f67`  
		Last Modified: Tue, 01 Jul 2025 15:36:15 GMT  
		Size: 14.3 KB (14346 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.1.1550-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:232f7dd77618ac5c732f188419caa731c3d296be07f80ba88a6c32baf0752b8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.7 MB (276677689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c7e947e242fe54dc4ebc6ff7fad06abda417e9f64b070374f64da89812a0db`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1751241600'
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
	-	`sha256:5c6a246a80c20351fe842a314b6b3f8561a5ceaea736decf36fe380b29e53224`  
		Last Modified: Tue, 01 Jul 2025 01:18:57 GMT  
		Size: 53.1 MB (53097236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85a969def2863a9e85601ef2d4f2e86efa8ff38674c223fec6a8890f4ca131a`  
		Last Modified: Tue, 01 Jul 2025 08:32:36 GMT  
		Size: 132.8 MB (132810557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:845abc443984b91ec28ba019dd19c9f8abec41b136ce13c23464c3a610aed834`  
		Last Modified: Tue, 01 Jul 2025 08:39:01 GMT  
		Size: 90.8 MB (90769251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e606c630e86e2c648c6171c1d9054ecb63b619e3c167d1ce8dedd2123fd4f3`  
		Last Modified: Tue, 01 Jul 2025 08:38:54 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f7e0b2cba4b2239f5de93649d8f912214a807f8561fcd6a348bd5e6ec019974f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7497372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac794b57eeb18fb861ca8862fdb0edc348dcaf6af777546dcea1972c539f847`

```dockerfile
```

-	Layers:
	-	`sha256:69ba6164b99717a2992bcb82af4afda8fdb945904e1c206c9a260bb490e46f94`  
		Last Modified: Tue, 01 Jul 2025 09:36:45 GMT  
		Size: 7.5 MB (7483096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2988fbe22981cf6d006827246d039f4146ffe6d58658fc549947a75a498c5623`  
		Last Modified: Tue, 01 Jul 2025 09:36:46 GMT  
		Size: 14.3 KB (14276 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.1.1550-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:9ce53491b96951ce598600e638bb64616e79bdf6f8edf66144a10cc2e2540103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.3 MB (261264946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac9d67d61e68e2ba685088b7f52ab5f64d6fa68158502634362348cb9b94539`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1751241600'
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
	-	`sha256:48de1d8f52c0a2a00375babc11bf69628b8225862d3b6ebbb2205e4ae2f3e96a`  
		Last Modified: Tue, 01 Jul 2025 01:19:00 GMT  
		Size: 49.3 MB (49343660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e886a3da26b6eec580831e6bb7710600a3bb78747e0fa988359be96e14f44218`  
		Last Modified: Wed, 02 Jul 2025 06:27:55 GMT  
		Size: 125.6 MB (125586092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6f5e1ee29099374a93e24862df81b2c1d2de4180d9b942dcbceaaaeec083083`  
		Last Modified: Wed, 02 Jul 2025 06:32:49 GMT  
		Size: 86.3 MB (86334549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0bfbda4a95b3fbd5d67b08cc8d08a61ac0f3446d8a65651b7dd87661024934`  
		Last Modified: Wed, 02 Jul 2025 06:33:04 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b90cbd8b42d4073fb9a9cc159e58a59a2ba110313549f9c7b48d9cd8a3e206fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7489448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c9fa660f4ab305bfc3dca3b174dbe5755801db10c3def05098bfac12bc7af4c`

```dockerfile
```

-	Layers:
	-	`sha256:61231cc4002ade5a614036315e453262427ce02480d57bdd6d61947960ca5408`  
		Last Modified: Wed, 02 Jul 2025 09:36:30 GMT  
		Size: 7.5 MB (7475220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a7c2fd806fa353644803b8b524eebdfc94d2f4c72053f0eddd64468f48e2770`  
		Last Modified: Wed, 02 Jul 2025 09:36:30 GMT  
		Size: 14.2 KB (14228 bytes)  
		MIME: application/vnd.in-toto+json
