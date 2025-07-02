## `clojure:temurin-11-tools-deps-trixie`

```console
$ docker pull clojure@sha256:253b94a3638f521dcd1e6a1e5f7e71785c11bb354f1c79c9de5f4d6fb0cdd752
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

### `clojure:temurin-11-tools-deps-trixie` - linux; amd64

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
		Last Modified: Wed, 02 Jul 2025 17:06:14 GMT  
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

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

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

### `clojure:temurin-11-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:308fdec00aa04fb08c3df616881b9c75212dcd91c5b2d4462e6b45c3c95307e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.2 MB (277223510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68f9418c5a932ec01a1e33c4d4cfa1c3c0c71beeb93df41dd81ddb9064b809fe`
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
	-	`sha256:30491e5de4a2268042f6637f9070c07b6990d0f97b46c74091707707a15cc7d9`  
		Last Modified: Wed, 02 Jul 2025 17:07:12 GMT  
		Size: 142.4 MB (142420717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d903c9ec56a0cb74d33f3580c3aca26ff4d3e14c33cd6b8a18f244af273c5c32`  
		Last Modified: Wed, 02 Jul 2025 17:07:09 GMT  
		Size: 85.2 MB (85171995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2134be75468d9d246a42d6712e6d9e11503fef3ad799041e3d8d1536415fac78`  
		Last Modified: Wed, 02 Jul 2025 12:28:06 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:66a012f6230855f0a7c6475d6eaa1db95b78dfde5c987be9e580203793c33920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7501287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691da85ce121cd77856f098e4173a2daa8050ef4daabdd166764c7f678d80f77`

```dockerfile
```

-	Layers:
	-	`sha256:87f4999993376271fdd721542ffc42df7a3e7b5dc6c3fa6f5ed898aebae910e9`  
		Last Modified: Wed, 02 Jul 2025 15:36:49 GMT  
		Size: 7.5 MB (7486942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c7f9564bed926bde6f09341750904082f32bae1395a8788c079dab86c93f2c4`  
		Last Modified: Wed, 02 Jul 2025 15:36:49 GMT  
		Size: 14.3 KB (14345 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:da440f4c6d0f224e6c71640ce633bc3716c541fd7cfc99e46ac5c3a7e8279959
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.7 MB (276677605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b03d2c89ac66f9cd45137b9d6d12d8dd50600d1e59c99f6e5a280540c748268c`
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
	-	`sha256:0d444579278889dce299d8c5d962674bdc7d1eccc25e9124de2a757e8fbe5000`  
		Last Modified: Wed, 02 Jul 2025 10:14:42 GMT  
		Size: 132.8 MB (132810379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f6222c1cdcb5bdf26f45937aea88aca44a430de4705f3cac072bfe0cdc0123`  
		Last Modified: Wed, 02 Jul 2025 10:23:35 GMT  
		Size: 90.8 MB (90769347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8943a0dad40dd91d0b9733147944603f0222c7c780eea4b93fb1c4540b6693ee`  
		Last Modified: Wed, 02 Jul 2025 10:23:18 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:22f5ff7e4bf7761dbeb6d73f8f46e88feac7966d775fff85b70e1e0be8ea195c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7497372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de7aa62ee7f1b77789e5e2c47a4e926a0c4efbe5c4190021d0cdf70556a65110`

```dockerfile
```

-	Layers:
	-	`sha256:2a2fc7155b4069ae7105b8d4f5f08ec06f2d63dd8085322f5f3e0dcef47afc0f`  
		Last Modified: Wed, 02 Jul 2025 12:36:30 GMT  
		Size: 7.5 MB (7483096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2f3994ad17bf68c7ad7bd7bc3eda1e8b585bd73d65423d8ca78859510169b39`  
		Last Modified: Wed, 02 Jul 2025 12:36:30 GMT  
		Size: 14.3 KB (14276 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; s390x

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

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

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
