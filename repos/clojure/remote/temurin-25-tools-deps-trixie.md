## `clojure:temurin-25-tools-deps-trixie`

```console
$ docker pull clojure@sha256:5b71908adafb13e41cb1c9c4dfa72df48c8424f777b991d5f9996eb85e28aab9
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

### `clojure:temurin-25-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:12bedc8b5cac4f34dcb909c2d5132d709783cd2935ce966dc51add4bfeb68600
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.1 MB (227090073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b0ac0e54ab2cdc19fe78a8e33f1f847e109616abd526dac8023a2cb30d01fb1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:57:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:57:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:57:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:57:35 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 19:57:35 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:57:51 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 19:57:51 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 19:57:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 19:57:51 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 19:57:51 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:866771c43bf5eb77362eeeb163c0c825e194c2806d0b697028434e3b9c02f59d`  
		Last Modified: Tue, 24 Feb 2026 18:43:22 GMT  
		Size: 49.3 MB (49293124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183003a54bd0704ea3971054ada12f8eb7d539a0c269062a37f327fbf5e33997`  
		Last Modified: Tue, 24 Feb 2026 19:58:13 GMT  
		Size: 92.3 MB (92256297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4eb65c8cf822d78c0ade73a0b5f6d3708067c7ead944869ac3f79c6bd174dbf`  
		Last Modified: Tue, 24 Feb 2026 19:58:13 GMT  
		Size: 85.5 MB (85539617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d847eac25f740aec42a529de8ec33719274210b7b7856d33746c373accfb249`  
		Last Modified: Tue, 24 Feb 2026 19:58:09 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d74348cbba5343610d16a1fb2ff362440dde0c03508a00886288c2abb67def`  
		Last Modified: Tue, 24 Feb 2026 19:58:09 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:494e096395359bb38147b2550562866aac449a82fa3767da1786ac3b5ba67644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7453561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13c9721522438e196fb0f1c61a5ba7af54d22f064acfb55d12fab3abb189f98c`

```dockerfile
```

-	Layers:
	-	`sha256:c010f0b9cf5dc3463449be40de2a1d53fb1f4ad5952badee7acfceb9be558c69`  
		Last Modified: Tue, 24 Feb 2026 19:58:10 GMT  
		Size: 7.4 MB (7437146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f54184ef983d5759ffe5b5c0bb839f06d18e0cd7f4ab2eb142b5e998c6348b8`  
		Last Modified: Tue, 24 Feb 2026 19:58:09 GMT  
		Size: 16.4 KB (16415 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4c7d3649f44f21d93e1bf78c904923899ab74d9c3877385016813fd2f1de5017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226306740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f589c273b3f0c4fa87764d7efa92d215620879b15acf1a4bfaaaac522331544a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:08:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:08:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:08:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:08:11 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 20:08:11 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:08:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 20:08:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 20:08:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 20:08:29 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 20:08:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ac9148dc57ca750b09f3f3da6f16324e1a3b62432b2726734535ec610e1a9232`  
		Last Modified: Tue, 24 Feb 2026 18:42:56 GMT  
		Size: 49.7 MB (49652168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71f6343d802bbb11ecabfac7757348ac81fa7c44c7ef053b81d1159f2280c0a`  
		Last Modified: Tue, 24 Feb 2026 20:08:54 GMT  
		Size: 91.3 MB (91288274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925d6e9f957b451c20e4f1ae8d7118b87ab0149a4f15f4ed02deeaa059acb04e`  
		Last Modified: Tue, 24 Feb 2026 20:08:54 GMT  
		Size: 85.4 MB (85365258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc34b0a297203da4c53b43c828326f26ea8a276c29d36439182899b34f9b1117`  
		Last Modified: Tue, 24 Feb 2026 20:08:51 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9faa434027fdce9b3b444248d27d505d922665abdde01f69a2fbf2077578424f`  
		Last Modified: Tue, 24 Feb 2026 20:08:51 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:2515095560fdfe4d2270365833d7ec699bfb6ab87aaa48e43d60a80e9a1d8736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7460753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c114271bb4e97e233b99ed1cd0b03102c33a78fa42958e21f6eb8dfdecef0aa8`

```dockerfile
```

-	Layers:
	-	`sha256:60426bb0da078f8e400a86b23ae3ff7bc602f5231bb4b8c12b9048440ea7d89f`  
		Last Modified: Tue, 24 Feb 2026 20:08:51 GMT  
		Size: 7.4 MB (7444197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c2b03a1237d52f91239538626546ae15389a3ab51929cdceb5d54eeba50187e`  
		Last Modified: Tue, 24 Feb 2026 20:08:51 GMT  
		Size: 16.6 KB (16556 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:5643c402346eda3e9f962de5844b98d9edf67e4a6f3ed65a013ce9fac394d69a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.7 MB (235693564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b319f930a00829982ed3c066c41e674dd1aea7f19a1a5421f9771ed5da2318cf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Fri, 06 Feb 2026 00:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Feb 2026 00:48:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Feb 2026 00:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Feb 2026 00:48:05 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Fri, 06 Feb 2026 00:48:08 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:53:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Feb 2026 00:53:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Feb 2026 00:53:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Feb 2026 00:53:29 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Feb 2026 00:53:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6397fc946e64e7714633f42a4de42b00c617e66212cd1a0b61df76767b81f868`  
		Last Modified: Tue, 03 Feb 2026 01:16:36 GMT  
		Size: 53.1 MB (53112115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3230ebb877a1444adbcad5521afaffb1c41773004c4324fe65c2c551a9cc1544`  
		Last Modified: Fri, 06 Feb 2026 00:50:07 GMT  
		Size: 91.6 MB (91632873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ef605411196c730ec201e18c625f2cabfc5fb83efd9aa74fadd830038fa9a6`  
		Last Modified: Fri, 06 Feb 2026 00:54:13 GMT  
		Size: 90.9 MB (90947534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f44e46ba657109043e4bd78d3e9efe1f54b96ba06b92d73b3b462d3a1921ef8`  
		Last Modified: Fri, 06 Feb 2026 00:54:10 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655167cc00123f09c2a88756e426950971b5bfb6f02d958b0054e20f8bdf753f`  
		Last Modified: Fri, 06 Feb 2026 00:54:10 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:78d0f2d5872d09ddcade682857b713cace1babc67d5b4bfd6a2a171194ec139f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7441365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2642df4963aac19dbb1d0191df0c6d20de8fe59ba430e1c582f221fd05a9f255`

```dockerfile
```

-	Layers:
	-	`sha256:b651bcedae4c7cc363e070c930a7d225a0b867b1039a5df57fd310e3161dd6f4`  
		Last Modified: Wed, 18 Feb 2026 00:06:39 GMT  
		Size: 7.4 MB (7424891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c5b8fc6137227c3a49466d1615b2a4e1d017c3fe4da9a4b06f267345e97b19f`  
		Last Modified: Wed, 18 Feb 2026 00:06:39 GMT  
		Size: 16.5 KB (16474 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:75d42edf6a911f433be6ba1b3ffd292ef4fc55d41d1636eac8ca56c2c9ddfee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (222976456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0f534d2176a7d7ce3d3970157c24c7190fa2b9bb56d997fdfec8ddbee2d6b25`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Wed, 18 Feb 2026 11:49:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Feb 2026 11:49:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 18 Feb 2026 11:49:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Feb 2026 11:49:18 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 18 Feb 2026 11:49:18 GMT
WORKDIR /tmp
# Wed, 18 Feb 2026 11:52:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 18 Feb 2026 11:52:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 18 Feb 2026 11:52:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 18 Feb 2026 11:52:01 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 18 Feb 2026 11:52:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:618efd37f74728f7dcba60c231fad7f2d777dc65e4da32d0adae5e032e1fd125`  
		Last Modified: Tue, 03 Feb 2026 07:13:10 GMT  
		Size: 47.8 MB (47776763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0c08292c273f6fa94290477f212196176e148c5443e72d590aa78d4b504c5d`  
		Last Modified: Wed, 18 Feb 2026 11:56:49 GMT  
		Size: 90.8 MB (90773425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e5dea3ba31bbf37ebe3b3414bdf4258e0621b6aab164e9c2752fe0d6b1f786`  
		Last Modified: Wed, 18 Feb 2026 11:56:49 GMT  
		Size: 84.4 MB (84425223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7f7c826b217e95fd4d70b6791c43150f39357961456e4054c4782eb6bcd45e`  
		Last Modified: Wed, 18 Feb 2026 11:56:23 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e84ba204c8d259db90bace7fcc313ba1fea0b94a0dc26859f7206a9e9ceb66c`  
		Last Modified: Wed, 18 Feb 2026 11:56:23 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:587c106994e2521c67971419a361f0613cbc11e348e24e05ac0852586bee188a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7423559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b538e779102728ce651b789a1760578d4bcf9613d5d73da63a9e04d1c43ed279`

```dockerfile
```

-	Layers:
	-	`sha256:1f3210e0b07d1ea50cdd2a79dd4f3e4bcfebb64adf507e58cb64cfb04c0b917d`  
		Last Modified: Wed, 18 Feb 2026 11:56:26 GMT  
		Size: 7.4 MB (7407084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad1045cae8dc95a5e5d67d3d7d82b8194db34f4943cca8cd294e33026c772878`  
		Last Modified: Wed, 18 Feb 2026 11:56:23 GMT  
		Size: 16.5 KB (16475 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:e8341560379628ad7823aa48a6e0fc84d275837a2f84c4f8b529a6c80f7e4d41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224101332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32413711f764c5e98ee87701c1e73bca4bbd3e071b5766814fe3cca5ac1ba9f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 22:19:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 22:19:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 22:19:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 22:19:35 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 22:19:35 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 22:20:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 22:20:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 22:20:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 22:20:31 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 22:20:31 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5578086c4ad67b3331d31c74c0b8aa3d13821b75ffa03070b0c1c80fdba7ceaa`  
		Last Modified: Tue, 03 Feb 2026 01:14:13 GMT  
		Size: 49.4 MB (49354378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac064884eca297fda6b77725e0502ad7ae6b62db38d8cbd2ad4c4340d2bd416`  
		Last Modified: Tue, 17 Feb 2026 22:21:19 GMT  
		Size: 88.2 MB (88233833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78fe20b6831ce4ebc6b102c20849a866163dfbc9a171e78413c0afab26e1c57f`  
		Last Modified: Tue, 17 Feb 2026 22:21:19 GMT  
		Size: 86.5 MB (86512075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55eb9af37e3f6f33676169b03e4a2e528b57ada6c36ae198030489480480c413`  
		Last Modified: Tue, 17 Feb 2026 22:21:17 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8949eefb4c24ec43075a6a607f27114484aaac5a838cc776ff3d210abd986982`  
		Last Modified: Tue, 17 Feb 2026 22:21:17 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:30074d6b5a555b57589f45f950f9c5f671474b192845322887eef80b3a93e5bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7434044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb691ce07f297cbcda1d026cd394ed0e1d02205e6c429a3d4f4d4d7c33e1f507`

```dockerfile
```

-	Layers:
	-	`sha256:76828d15e1a8b0122213b2997d55425d5cce7adbfd35324b877337bdf41271c4`  
		Last Modified: Tue, 17 Feb 2026 22:21:17 GMT  
		Size: 7.4 MB (7417630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdbdbcaea02a2878157828d7ec5f74e454ecbbe0af022c46ee71cb0f8439e0ad`  
		Last Modified: Tue, 17 Feb 2026 22:21:17 GMT  
		Size: 16.4 KB (16414 bytes)  
		MIME: application/vnd.in-toto+json
