## `clojure:temurin-21-trixie`

```console
$ docker pull clojure@sha256:e177d8a50a07e0b525ce1a1e5b2bcab257b6e3de4cb5c8e88a7fcced15b1d8d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-21-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:e7a285de8487edded331e00e6a80b9a7b3d02ee730c9e4edc40b96478a513e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292632070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35ed6afe3d122c9e0d8e1e98e7dffea8774ebd225ed977ec125afef34ba5a87e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cae3b572364a7d48f8485d67baee38e4e44e299b8c8c4d020ff7fb5fdd97f88c`  
		Last Modified: Mon, 29 Sep 2025 23:35:29 GMT  
		Size: 49.3 MB (49284626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eedb24155b59746dbef955d021cd73e15072b61920233c77afac5fe4bc699c7`  
		Last Modified: Wed, 01 Oct 2025 15:56:12 GMT  
		Size: 157.8 MB (157804739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30331201a8e7c755dd4f733ee6c703d54b7ef05e00415c5cfca3794df5b5ea42`  
		Last Modified: Wed, 01 Oct 2025 01:00:15 GMT  
		Size: 85.5 MB (85541665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71409e600d3d36f7f53a763ee6751bfe692fa990f96f9d6ac2251c073e2dafd`  
		Last Modified: Tue, 30 Sep 2025 01:39:26 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1b818e494a6b767127f1e475ee1b950453ba4e24e9b6b60c6154426940e63d`  
		Last Modified: Tue, 30 Sep 2025 01:39:26 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:dac8cb90df274598bc5f5de86a6074b87a4ddfe9175a8294f16b83a58f44d5cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7485744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f516a539756ddce2372145f243ea4e41fe9569334e3758824410f718ecc2579c`

```dockerfile
```

-	Layers:
	-	`sha256:967fb3c497329e1e8e9307969422858d12b2ee76971b011dbe155c70c0e7e26f`  
		Last Modified: Tue, 30 Sep 2025 21:36:19 GMT  
		Size: 7.5 MB (7469947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64d9a702de9b744cbf35ecab862d357d84cd353b85eb78b21d7ff601cf9f1726`  
		Last Modified: Tue, 30 Sep 2025 21:36:19 GMT  
		Size: 15.8 KB (15797 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:29724daddfe5718791f9a8cb5804bf5656ee95ad463e0d3d773390e9775d28d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.1 MB (291094306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f432896ff8d4a89070e93758ec5b6ac116f4a73f01751783c9f348c0e15cab67`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:28aec8b14b3eeacbf47ef38af72fab694b109fdcdf31581722750599baf1a932`  
		Last Modified: Mon, 29 Sep 2025 23:35:17 GMT  
		Size: 49.6 MB (49648695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549e0483b8900c07a9193cbe38334223d448cb1d42f5956e0a19caa625fa6922`  
		Last Modified: Wed, 01 Oct 2025 13:54:19 GMT  
		Size: 156.1 MB (156081234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3fe48789055eddbedd7261253bbfd2ce6e1659f33fd373a4550f62f98da7207`  
		Last Modified: Tue, 30 Sep 2025 00:54:40 GMT  
		Size: 85.4 MB (85363339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e26d6b58330c6130a13454c375dad067478ab0af4f70bc6460fc7e9879e5b0`  
		Last Modified: Tue, 30 Sep 2025 00:54:34 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5149eecdd3727f5db7afeeb4c7c669f86cab26a6e313c5bf0991b8bbbe34db`  
		Last Modified: Tue, 30 Sep 2025 00:54:33 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9bce93df52a59b1cb57dc0d3b38cc92d924411ef17a81e8e126484c596a2cdf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7492892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94d819c725cd1b643d193df7eb80f4a44460b3dee5999490575fd20f8467d851`

```dockerfile
```

-	Layers:
	-	`sha256:6bb458030a13695d39980bebe1fb6fa808ad09cc5085635d3e965b42d82003ca`  
		Last Modified: Wed, 01 Oct 2025 12:36:23 GMT  
		Size: 7.5 MB (7476977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba575ac4957bc90e5c5aab00aad72389cacc7fdd83a77583d5edb0d56d2393cb`  
		Last Modified: Wed, 01 Oct 2025 12:36:24 GMT  
		Size: 15.9 KB (15915 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:1728766f6a9c8f39b0d4ea84887dea49a97753faaaed053965e3d713f0c5c58f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.0 MB (302017158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c19f74d09ffe8d51f84220300de188a70ca1f3f22744c963f0cbc950da1c0c15`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4cb8224e7ffc22512c71f1cfc1042cb22342df02312e61cb1ab0c492c3369711`  
		Last Modified: Mon, 08 Sep 2025 21:18:07 GMT  
		Size: 53.1 MB (53104433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330554e28470024f1db371837c89576dd6d42feba85f739f013830e8d15b7103`  
		Last Modified: Sat, 27 Sep 2025 20:14:27 GMT  
		Size: 158.0 MB (157963450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a1cb3469fd517ed4355e94b00751e21e9370954a75627abcc35dfc564486eb`  
		Last Modified: Fri, 26 Sep 2025 18:29:08 GMT  
		Size: 90.9 MB (90948232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8bfa4d10eb5df9bec83fc70598e1717099ee8eb82db07945b90b811451e363d`  
		Last Modified: Fri, 26 Sep 2025 18:29:03 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89efb1597c315cf783bc6ddd4b07088ec01dc47b7aaca8a926f7c00a2ccf4637`  
		Last Modified: Fri, 26 Sep 2025 18:29:03 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:40486cc4f0c652db446f3853d99900eb082ecfa038630d743cbdc515fec55180
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7490210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6afbf95a84734074fa5475896c51126e1074484b910b957c5c6578220185fc9`

```dockerfile
```

-	Layers:
	-	`sha256:aaa3fb48826b1adb2f744dc0bc1a4ec45db497eebc4ff634c13027b3cc42a6d4`  
		Last Modified: Fri, 26 Sep 2025 21:40:09 GMT  
		Size: 7.5 MB (7474366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01fe9f5aa0f373bd83c4fcd310dc97e524bb1c7f72e8490ed77586885b6a48cb`  
		Last Modified: Fri, 26 Sep 2025 21:40:11 GMT  
		Size: 15.8 KB (15844 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:d433310ce58a7e56387428d9d5db03bb334df5eba6b724059b9ec78aee055b8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285786807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f695ff7d572cf2e0b13904cd07430eb9651229c970e92c8b8ef13b8b82b8aa63`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8f913be5ecadf79e3ee9792194aaab366421c7e066487d572f285b293ff78a7a`  
		Last Modified: Tue, 09 Sep 2025 00:25:27 GMT  
		Size: 47.8 MB (47765447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d16d1a64bf63ce2a46fd192fcc03ef4725134c5c609d93baa2aa37b68e7d97`  
		Last Modified: Sun, 14 Sep 2025 03:36:09 GMT  
		Size: 153.6 MB (153593506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74bc4e9a15c6f8f2f3b4771e517985742ac52aac3e8576f7702ac9d8a78d5c4d`  
		Last Modified: Sat, 27 Sep 2025 00:38:22 GMT  
		Size: 84.4 MB (84426806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39dcf1b4e0374fb2ef86629b0a97ca67db2818628f73d6b22b5a62180085ab1`  
		Last Modified: Sat, 27 Sep 2025 00:38:18 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82cd56b0d22c1fa21a8630b224fd7fddd8bfbe566aad548f12f6e1f145f9fd03`  
		Last Modified: Sat, 27 Sep 2025 00:38:18 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1d60822a67fda07ec3637f272beff4e2624ce0a00eb122a29eda821615327081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7473705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88b407f73610100ad9bc020844bc359e1ef719a99282536789e1b658a324c514`

```dockerfile
```

-	Layers:
	-	`sha256:28b96cf378e189903075d65dc51af665d4b03a551ccd32dacae4462014e4e5bc`  
		Last Modified: Sat, 27 Sep 2025 03:36:49 GMT  
		Size: 7.5 MB (7457860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1638d92575162b5c1b41ddf1ecb9cc68365e30a951a6786f30d69bcb38e48e01`  
		Last Modified: Sat, 27 Sep 2025 03:36:49 GMT  
		Size: 15.8 KB (15845 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:83967a783f30f2b65f03bf1c7be12913d28892dd68de9f5c3ad7fd225eb8e631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.9 MB (282880542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4342c67eed5c72502872597c60556d9b55753583727bc93cd092360435e6e93`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:28eee642962fd09c10ecf87da2d4b65d208f3d5c1bf3fcca21c105c0213f558a`  
		Last Modified: Mon, 08 Sep 2025 21:32:18 GMT  
		Size: 49.3 MB (49346327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca6732308093ffadca9f5979257a664a89575a7116c201847cfc81c8d14134ab`  
		Last Modified: Fri, 26 Sep 2025 19:29:41 GMT  
		Size: 147.0 MB (147026955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:465f982f215ec0de40a5796df8e4f71adbd38e25c6722a51445e6817f5e0bdb2`  
		Last Modified: Fri, 26 Sep 2025 19:29:36 GMT  
		Size: 86.5 MB (86506217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb8bf7dd15a7f4d9d3e69a34416bef54887efc94c6ad05d2ee75297596a836c`  
		Last Modified: Fri, 26 Sep 2025 19:29:24 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a321db04a5e8d4c5263f03bac72a64bf5a40415eb2eac66c7e2169b6714d5d96`  
		Last Modified: Fri, 26 Sep 2025 19:29:25 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a624263b819ed359f7f866062c8840042cfa27cfd49d934e954f7bd62c22bccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7481666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ce8a82b584e30f8512389857081630aabd2dec743dcc2af31c48c1553f2ec18`

```dockerfile
```

-	Layers:
	-	`sha256:472ab2957a011dbc575b0b03a8aa188f90aa7ffade1a123b92d263fc0c8293a9`  
		Last Modified: Fri, 26 Sep 2025 21:40:16 GMT  
		Size: 7.5 MB (7465869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c4a000037d0cda8ba9654b11a6d4752b8766c0abacbf475be66c64eb088abdf`  
		Last Modified: Fri, 26 Sep 2025 21:40:17 GMT  
		Size: 15.8 KB (15797 bytes)  
		MIME: application/vnd.in-toto+json
