## `clojure:temurin-21-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:02bdc83a763e6eb2546947883da057a046edf4f52e21e4df5651e91e86f3bc5b
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

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:47d8cb942a199f15c019b891cee6872aa6f4ce6c68f39aad16106810fa3d6bf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.1 MB (262054764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3e354993699268469cd40ed1d208493bf5cfc693c49738028c011e36d04cc4c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ced038dea045df288fe9bdbe03117ca66fe2a071217e196ac86ed07f965fe688`  
		Last Modified: Tue, 03 Jun 2025 13:30:48 GMT  
		Size: 29.8 MB (29755384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a70a99e924b2fec02e6bfc5f50a3e99637c2e4b87a16e06ae4e3c9a3ac0e7e`  
		Last Modified: Mon, 09 Jun 2025 18:55:51 GMT  
		Size: 157.6 MB (157634498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3350620d10974556953ccf3c64843bd64d2e703b0078539ff8820d04abb6314c`  
		Last Modified: Mon, 09 Jun 2025 17:19:18 GMT  
		Size: 74.7 MB (74663841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7e38a876a1e7c83d72cbea27b41b0419fb9c1a77fc4ceefe2e470f97abac86`  
		Last Modified: Mon, 09 Jun 2025 17:19:08 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b4c10d01430c0552eebad3748c65331c3059921cab5de2c33c2f067bbd67a8`  
		Last Modified: Mon, 09 Jun 2025 17:19:07 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4288f512526a24e26c3fec99654ec8abab1ed545e6553775abaf59a05219a4d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e3d096ffa7412fc7b704245c3857379a1dfed7bd3c6631d35b6d610e74e0c4`

```dockerfile
```

-	Layers:
	-	`sha256:45e9e6ddefd0ddb9208d48c524da1b57074ac49125cc92db02fc7a16622824c9`  
		Last Modified: Mon, 09 Jun 2025 18:40:16 GMT  
		Size: 5.3 MB (5256074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aff097d1966f6fe61eb77cd86b934649d970426e4eeea57eed9d02296781c1d4`  
		Last Modified: Mon, 09 Jun 2025 18:40:17 GMT  
		Size: 16.5 KB (16543 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6952a271664ab8f1211290d023467c5850150bc90e427bec12c3cea2c0c98683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.0 MB (261016629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42561060a84ec991ca7b8aca70628f617ebc98f9162383783137db923b71c5ea`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1747699200'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6098c2c9fa277c00ab580ce12bf64a9e1edf9e9139ba18ad85f3cc3063834aa6`  
		Last Modified: Tue, 03 Jun 2025 13:33:56 GMT  
		Size: 30.1 MB (30119455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4a1faf17299c1f04638ddc5d736ac61ac6707116abce4ce0b018d30b88ee49`  
		Last Modified: Fri, 06 Jun 2025 11:55:14 GMT  
		Size: 155.9 MB (155928817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:146e6b6e5dbd4729806832b5086c3047d2d28c9f0dd88d4eae933846e9623243`  
		Last Modified: Mon, 09 Jun 2025 18:56:14 GMT  
		Size: 75.0 MB (74967318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3988f5ec252379bf8759ea2289d82107e481b6cc57b3e6dced1f0be41f3c7c`  
		Last Modified: Mon, 09 Jun 2025 17:57:17 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca32fa3546becf83f7e0d31f8a33ec53f0cd71097a801feb89cab25d6f83109`  
		Last Modified: Mon, 09 Jun 2025 17:57:17 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ba22ac0304e81904153d00e965b215bd3e3db87a3b8b3bfdf5b2f159c719a2d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5278552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b2d343523c01b008914ec368e9f4fc7482947a24aa4f2aad0ceac60ad16d22`

```dockerfile
```

-	Layers:
	-	`sha256:0d73dfb6103deaeba89e15ca51d7d77a14a5182fba2b847406ff7092b089b03c`  
		Last Modified: Mon, 09 Jun 2025 18:40:22 GMT  
		Size: 5.3 MB (5261867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29b7c04927f4f11d777dc56c8fa588362a1e95668d0a7e45287f88ef82842344`  
		Last Modified: Mon, 09 Jun 2025 18:40:23 GMT  
		Size: 16.7 KB (16685 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:2301d27bc15f7cdc62e3ee57f4fbc72b09e408e1f00c6834c97877ba288c9e17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.8 MB (271788815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:390dcdfd3103027fb5320307fc0952d65517730d8edfb14af0871824a1bdbb67`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1747699200'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:62eecea9deba6eaccef3e829ddec51f2c540dbbb668a68816c8ce3c4b8023d93`  
		Last Modified: Tue, 03 Jun 2025 14:07:09 GMT  
		Size: 33.6 MB (33580565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad2ab9d4ac6bb74fed4f1c45b064cd14cdabf6a0b701738b0c7f33fe7866ad1a`  
		Last Modified: Tue, 03 Jun 2025 09:13:13 GMT  
		Size: 157.8 MB (157804907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337c558e91ea01726fed754c4669aa4a0d957a69b4e73dd03c82e5230ea3b10b`  
		Last Modified: Mon, 09 Jun 2025 18:20:55 GMT  
		Size: 80.4 MB (80402300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15fec36fb026d59010bb4b065ceeac97f2ff91cd157ffbe983e40e508ba39a5`  
		Last Modified: Mon, 09 Jun 2025 18:20:26 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe633173d2590d7a293cec1744011929e650c30fd636bff9b501c1144786133`  
		Last Modified: Mon, 09 Jun 2025 18:20:27 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cc32f9d8042af2e6f552b8dc04373024f0e0eeb1b1104bf574ed79a24a3bf7ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5277060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cc4aec5dbc830e9b66a39019f3f847035b4f7ec85e00c2df09403ecf329901f`

```dockerfile
```

-	Layers:
	-	`sha256:d1dfb7bd1a4cb99991efb80e1395978a5861562d0dd7e60672b0bbec1f8b1dc6`  
		Last Modified: Mon, 09 Jun 2025 21:38:38 GMT  
		Size: 5.3 MB (5260457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d27404a1eec72874a0eea7deb7fd855e75fd147c85b98415e2306007b5821854`  
		Last Modified: Mon, 09 Jun 2025 21:38:38 GMT  
		Size: 16.6 KB (16603 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:fc4dec7f738d5d6fb35f9d8e7794264060fb378c8a60924d45433456fe10a845
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.0 MB (255004110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7764264b2c41088c00f92266b6229018347ef4cc1f6065c573892abd9d128232`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1747699200'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f092cb6a76bde9a7b3c337ea49e8a7adec71062dc5df097be99d3975e92bc53a`  
		Last Modified: Tue, 03 Jun 2025 14:07:17 GMT  
		Size: 28.2 MB (28245354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5009b64f50fb13ff55ef1af62e2fe1e6a6ee386115f6dc3a0f39a750f60310`  
		Last Modified: Tue, 03 Jun 2025 09:46:36 GMT  
		Size: 153.4 MB (153449629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0dcd9afd22b7b2c4cf20ef5223c82f166942ac89d394c10a82c993aedb5541`  
		Last Modified: Mon, 09 Jun 2025 19:22:41 GMT  
		Size: 73.3 MB (73308083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17656f37a10fc9f06c95a46645b2a34f60417263e5ced5abfc4c255f54736342`  
		Last Modified: Mon, 09 Jun 2025 19:22:29 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d9516dd716523b86d0c7b4fd805bd73931493c265abed1999fee15538e3c13f`  
		Last Modified: Mon, 09 Jun 2025 19:22:30 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ca594b72d7c3edcd87b97cee121bf12e0999e097b408a701e451ab3827cfcd7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5262153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8916d09de6f4e58be691a147af74d9d21e61c7e864364a309c53940e027f3df1`

```dockerfile
```

-	Layers:
	-	`sha256:7dd37e6ef2f1abc9b356e0bdfe2bfebb824363fa3673a1c10c86dcc25c035f74`  
		Last Modified: Mon, 09 Jun 2025 21:38:43 GMT  
		Size: 5.2 MB (5245550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3911c18802bb0ed9e3eec2abc776f03cc144e420ddbb48422474f663c23daca3`  
		Last Modified: Mon, 09 Jun 2025 21:38:44 GMT  
		Size: 16.6 KB (16603 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:baab09ce56443d08665e8b3f5e6081760b3cdd4e4ea614a128722fbbf0aa202f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.1 MB (252147478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50fdba9b19e0eb4ab1f7a7b747834a2473c4fe7d7e707cb1a10148651f6b48e9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1747699200'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7cbda353d6047374e3da60bdf79ae89f8047840010f0964c87a8f2714e146106`  
		Last Modified: Tue, 03 Jun 2025 13:43:57 GMT  
		Size: 29.8 MB (29829620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce31050e492004a774304e4a6a039f15374ef94ca4f31b4d1ea37f80078b58a`  
		Last Modified: Tue, 03 Jun 2025 06:29:06 GMT  
		Size: 146.9 MB (146910974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55836d8438c59d977721cc331792ae1ea635c14bbad8b506c2aa6a85762132e9`  
		Last Modified: Mon, 09 Jun 2025 18:57:15 GMT  
		Size: 75.4 MB (75405841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5882d16b37b984ba9ee1b508264f5bed45baa2bee45afd2081079b57194056`  
		Last Modified: Mon, 09 Jun 2025 18:56:59 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de24bfdfcbee4ea6d542bfec681a0b96b86e46330ca6da42f4f4219db0a4b88f`  
		Last Modified: Mon, 09 Jun 2025 18:56:59 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:97c72af7579106d3341aa8e4b8c45d99ba90e967186313ab7535f3c7d8875f01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5268541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8440b4bddaa0126312b06bf9df6a122f2706e06efebe3ccb77da7678c1d857e`

```dockerfile
```

-	Layers:
	-	`sha256:e0d7d1297656ce52eed08e24cad66d8d550f1c6966c5a688fa594d06b020fb9b`  
		Last Modified: Mon, 09 Jun 2025 21:38:49 GMT  
		Size: 5.3 MB (5251998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83105ce75e15a1bb43fd3be0d105ad6abb7532d656d27f71332cd9c2283e803c`  
		Last Modified: Mon, 09 Jun 2025 21:38:50 GMT  
		Size: 16.5 KB (16543 bytes)  
		MIME: application/vnd.in-toto+json
