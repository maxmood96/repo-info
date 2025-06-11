## `clojure:temurin-21-tools-deps-1.12.1.1550-trixie-slim`

```console
$ docker pull clojure@sha256:b2a789eae647d32f6a38144dd7f336e37244d04660f8c3d03e7387a58a8924f6
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

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3cc1b8afb3dc7af30bb3897037d615b6114f0eb95f76f44310b71d60e3384b04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.1 MB (259113966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a1e75ac76cf5c3ff81443153ee52593000b1bb40010a6b57607e63846564e41`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1749513600'
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
	-	`sha256:6f052c0ff895d860a8f6983dcf5207c5e8ff5949529101bf68c1e92e9c8baf36`  
		Last Modified: Tue, 10 Jun 2025 22:47:31 GMT  
		Size: 29.8 MB (29756816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027adf75a7eb9c545bb493793343135aacc2f94e096267d4299a0650262d7402`  
		Last Modified: Wed, 11 Jun 2025 03:43:51 GMT  
		Size: 157.6 MB (157634503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d787040c641380e8751a3817430105ac45636b9fcd804102bbde09d88eb23a72`  
		Last Modified: Tue, 10 Jun 2025 23:53:05 GMT  
		Size: 71.7 MB (71721606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1358338613bd9d2e202ecd4b0c6986cbb168ac89e05455b2ca14155755d7f55`  
		Last Modified: Tue, 10 Jun 2025 23:53:02 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:883f07dff9e947dbc706936243ce378948becc1c98247cbbf34de67a360e4ed2`  
		Last Modified: Tue, 10 Jun 2025 23:53:03 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5824ef76e18c6e41fb84c052b6e62148cedd37c17e0436d81bed4d2b916e9ddc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b163012400875c99973b1c583d32e9421f3233169e0990489bdfb4b851369d6`

```dockerfile
```

-	Layers:
	-	`sha256:01e10e9472ea9e201858cc84965deddaff37027be9de965a696395aeab318b56`  
		Last Modified: Wed, 11 Jun 2025 03:39:15 GMT  
		Size: 5.3 MB (5256588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0eef8c6d00fc3eaa434a6249450f63e3598ef007cbf4df5a3da7ad86450ce61e`  
		Last Modified: Wed, 11 Jun 2025 03:39:16 GMT  
		Size: 16.5 KB (16542 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie-slim` - linux; arm64 variant v8

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

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie-slim` - unknown; unknown

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

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie-slim` - linux; ppc64le

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
		Last Modified: Tue, 10 Jun 2025 12:00:12 GMT  
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

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie-slim` - unknown; unknown

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

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:5018be5a6d5622e0ba999fa2b6f462f6e438d0fb55ae4983734d8b8e622dcb42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.4 MB (252411866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7cbbcd83efc35518315457fc96954fc07829fc893aa71b4696f2b4803c3b286`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1749513600'
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
	-	`sha256:3a4ce3b49438d6e971d6a25501e5ee98899a309dea36cc03fae31602fe4551a7`  
		Last Modified: Tue, 10 Jun 2025 22:57:56 GMT  
		Size: 28.2 MB (28247070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc39fca1c5edc9e41789080ae4d2069c8256f0ff5e3b91de1cf94cee501e22b5`  
		Last Modified: Wed, 11 Jun 2025 00:21:47 GMT  
		Size: 153.4 MB (153449632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5603ca9ceed3abb1642c646698ba8a463f322eb509e5a8c30955449c8d2a6a2`  
		Last Modified: Wed, 11 Jun 2025 00:35:56 GMT  
		Size: 70.7 MB (70714121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4d18453928e09db4c0b7d6e6a47c07bb8140d4864b29fb85f352c713b16f90`  
		Last Modified: Wed, 11 Jun 2025 06:39:44 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687e012e7d7c40b687deead535fa288ca624bfbe984875f74b92af6835987018`  
		Last Modified: Wed, 11 Jun 2025 06:39:47 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0f26b1395fd6ff96c1b9f26496ae7e612a9dbac746903bf9bbb6f144e671f824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5262667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30b809f821ea66387d7bca587637d92e201841d8ed3192b7ebeb1b2bd331626b`

```dockerfile
```

-	Layers:
	-	`sha256:305533aee62a634ea7532d122ed06e3381a1bb90dee1f793bdd28da9fafe45ab`  
		Last Modified: Wed, 11 Jun 2025 03:39:28 GMT  
		Size: 5.2 MB (5246064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a9d3d764700b6f096ec3ceb6cc3da6c5e69bcbfa9f02be970e7162e1daafc55`  
		Last Modified: Wed, 11 Jun 2025 03:39:29 GMT  
		Size: 16.6 KB (16603 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:062d3e24fa161afdce9a69e225dab1dcf36dccc3e8599cccd3ba8e3777f9ac00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.6 MB (249564163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:099530955bcbd9c8c2d2f6da95cb6a2e9ff925672980e478d25605d642de954f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1749513600'
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
	-	`sha256:c274825e96bcfbbdcdc116bb72e2d5d06d51048380b2fb22f400e6f9627616b6`  
		Last Modified: Wed, 11 Jun 2025 00:37:39 GMT  
		Size: 29.8 MB (29831871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45021c7f7281fd7e0bd66ca1c56da1f0f7b0faeea6a81d9a5b224fc27237b729`  
		Last Modified: Wed, 11 Jun 2025 05:52:27 GMT  
		Size: 146.9 MB (146911003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f587826f4117b00ec24bb4eaf1e753fb7507b72f05f60f74a1aef73867399a95`  
		Last Modified: Wed, 11 Jun 2025 05:56:07 GMT  
		Size: 72.8 MB (72820253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30121fd0fe25fc369042764631849ef8f8a8ab9e3d008a79f2a41a2733eb400b`  
		Last Modified: Wed, 11 Jun 2025 05:56:52 GMT  
		Size: 609.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ad9be81ec992f210bf8f27483d1a6e8dd105a39f8b324baf945fc3885fef10`  
		Last Modified: Wed, 11 Jun 2025 05:56:55 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bbbd883f1a6688c92bad751458ffe0bf602f6d2212ebeb51efa8f1b474bd29d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5269055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3b4f82c094f5d2adf1aee9efd73aa66bf347d71c7ee27bed14017a223ec0957`

```dockerfile
```

-	Layers:
	-	`sha256:c49448d61ad5ced29bd56c68bb954065720d57e32e113f0662c25f7b531b2aca`  
		Last Modified: Wed, 11 Jun 2025 06:38:32 GMT  
		Size: 5.3 MB (5252512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d9283da2b6d1ad332bc0b20d88039d2574694be94b98b9ff7d54d8b0b8d185b`  
		Last Modified: Wed, 11 Jun 2025 06:38:33 GMT  
		Size: 16.5 KB (16543 bytes)  
		MIME: application/vnd.in-toto+json
