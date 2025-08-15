## `clojure:temurin-24-tools-deps-trixie`

```console
$ docker pull clojure@sha256:c4911d23d4dbfadee5aa938d6a463f3d4ea38a4b2f5863cf7ca46c3615f656db
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

### `clojure:temurin-24-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:0b83d80e8cc2e2e5df9b2eaf8b26f94db2216f3a7a9ed0aaff89940f118e7b5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.6 MB (224640455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14ae6c28d979c1f2addd0315c83408c6fc5eb7aeb8cba7f271059bfe3ff46726`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
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
	-	`sha256:80b7316254b3093eb3c7ac44bb6c34bde013f27947c1ed8d8afe456b957ebfdb`  
		Last Modified: Tue, 12 Aug 2025 20:45:14 GMT  
		Size: 49.3 MB (49278280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d5892896b0faf04a035ac90254f1ef9e69385217d52e62e545c74b53d1c32d`  
		Last Modified: Tue, 12 Aug 2025 22:41:09 GMT  
		Size: 90.0 MB (89975189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f968ab78926d6e07e9bee94f99f8c517550fbbc3375a1e0627aacfd0202aae8b`  
		Last Modified: Tue, 12 Aug 2025 22:41:07 GMT  
		Size: 85.4 MB (85385942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1964297ce4a6114d766a4e7a01121d779a276f46259eacd277d25d2df36f7f5a`  
		Last Modified: Tue, 12 Aug 2025 22:40:54 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27bf79b67d5886b890c0f94159decd611157cefa979edab691f41845f643219`  
		Last Modified: Tue, 12 Aug 2025 22:40:56 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:7b8e4c7e6bd661e1297f7296be77a056d0d04c2196fad3a7ed522c06fdf2187b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7428630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d286a1effd6f0e2d8dd062a56cebddb7caa8157cdd856ccfe69fa2447612829`

```dockerfile
```

-	Layers:
	-	`sha256:e831ef5d139d7416c7f38133404c2dd00f57fda48285f8dfb6bbc99f3c0b8386`  
		Last Modified: Wed, 13 Aug 2025 00:41:10 GMT  
		Size: 7.4 MB (7412840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b47da409144e979c7807650c26ef5968578710191092fa18f0f3a5cfb3cf1578`  
		Last Modified: Wed, 13 Aug 2025 00:41:10 GMT  
		Size: 15.8 KB (15790 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:302b95cc9704fd23aa196308ceaf8d0beee433782e587f17393526f7d2df6295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.9 MB (223946395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce7a47c6976b4c382a6b859a1b7d55202dd5c48481e6572b01b901a6f10a54f5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
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
	-	`sha256:d1e40442030765a3ac5d135c39154d052eba20953ea0e5d35a066f7722cdd93d`  
		Last Modified: Tue, 12 Aug 2025 22:12:36 GMT  
		Size: 49.6 MB (49641603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51597c650a72609e7508681be1db5688d4c9188284533f2677b8f0f39c731b6b`  
		Last Modified: Fri, 15 Aug 2025 18:10:06 GMT  
		Size: 89.1 MB (89092517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61ba164f5c2d93dade7b171fe0f045daaf3db6bbcdc2b007036ba2641e5f35a`  
		Last Modified: Wed, 13 Aug 2025 14:49:09 GMT  
		Size: 85.2 MB (85211233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f3c7158168a6acd375629a29e904e72b6cf5ac8bdd1152b249086cc813885b8`  
		Last Modified: Wed, 13 Aug 2025 14:49:04 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5435cc15f8ad657ee491fe3fee87efeb38225dcb2c66d6af4ee5dbffdf7086c`  
		Last Modified: Wed, 13 Aug 2025 14:49:05 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9b261dfe9acea939f7f4aeb84ce2e8ad9a1effa00a82b117b7a8f2a6c270de63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7435775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63f38e1487e82c652955d8692396965c00e97335d77ed0315b9b3eeed121180`

```dockerfile
```

-	Layers:
	-	`sha256:51fb00be9fddee5485680a1867f46f9cbb35dc32e716a52ed80ec4e25b075ee0`  
		Last Modified: Wed, 13 Aug 2025 15:41:42 GMT  
		Size: 7.4 MB (7419867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f04c968c8e8bdf61954c487a42084ccfbd434f6dfd5ab71bffb4dc83bc8f29a`  
		Last Modified: Wed, 13 Aug 2025 15:41:43 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:bd9c7a749b8d2720744aa177337780de35db921d5d91f8f1264af1662a99257b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233817250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbc0c4abcefb1de2dd8f7a76f2a4ef0f55c56ae837ef39d21545d1febe91b8b4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
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
	-	`sha256:befe77620590f63939f5bcadadc9f45832981822c9c901f057eb4e86f733c29a`  
		Last Modified: Wed, 13 Aug 2025 00:32:04 GMT  
		Size: 53.1 MB (53103384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb08f4eb67a006175c2f5581fd1ddb8e0444fddabda29d05bb81b93b4156c3da`  
		Last Modified: Wed, 13 Aug 2025 20:21:50 GMT  
		Size: 89.9 MB (89918157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377d7a2bb5654197072508829f6a5cfc6738c32fd8dea110d964c67fed7c7bb5`  
		Last Modified: Wed, 13 Aug 2025 20:29:21 GMT  
		Size: 90.8 MB (90794669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:702dc0b6ad9a885c466d0545976d90fa8772fa4fd8a429050e2d0c3f105f3088`  
		Last Modified: Wed, 13 Aug 2025 21:09:13 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d16b10805d72c4c4844a8757abf416408ba053be7c4fd7c35829db47749e4d0`  
		Last Modified: Wed, 13 Aug 2025 21:09:13 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9d14fe786238b11530e58f6c81324eb3a8791aa93f8973eef3ddaed9a92d278b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7434395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1f6fec156637779e8ea991d457671ddd62ac310f5ab85139fcb2c600554f8bb`

```dockerfile
```

-	Layers:
	-	`sha256:178918fda425b5663fb90be10b16462532eadf3094877b5d73e0406107f5c2df`  
		Last Modified: Wed, 13 Aug 2025 21:40:01 GMT  
		Size: 7.4 MB (7418557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afd1bc74b3aa8ee7c0b8ee678a40c7755c9a30cefe8a2b598bb9276cb1aa6e13`  
		Last Modified: Wed, 13 Aug 2025 21:40:02 GMT  
		Size: 15.8 KB (15838 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:ebe7e55dd1373e7c9f9f67a09ec221e423d8dc67b9c083ebf259a27d4a593803
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.7 MB (219711921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3546197f39e196ac9f252d8f38419f611b3d54fe71e484caa22f28602fee5f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
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
	-	`sha256:59f3e0adb655cb03f7d489f3cc57e302e249916bbb076c78008f9329238bfb20`  
		Last Modified: Wed, 13 Aug 2025 01:13:55 GMT  
		Size: 47.8 MB (47764303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06baa43796aebc4f3d6bac79915da1ad2cd1c5a4dcb441027fb795d6aad4f6c3`  
		Last Modified: Fri, 15 Aug 2025 08:06:02 GMT  
		Size: 87.7 MB (87670417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ab036a4c236e98811e8120749fa68205b510179b6090392cec23461fdcb15a`  
		Last Modified: Fri, 15 Aug 2025 08:20:14 GMT  
		Size: 84.3 MB (84276159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616be74d3c4e76ed0125abffc43254eee294a5149794bc5543e2972834d1eede`  
		Last Modified: Fri, 15 Aug 2025 08:20:09 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aec1f4460f0d90805cd2af58f12b8ca0a6ab522a5206e8c48cf2d35c7efc3e6`  
		Last Modified: Fri, 15 Aug 2025 08:20:10 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:88256dacfad95fb3d03924f965f9fcf225e5bb1014e6e360803608d6ce7c54ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7416588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2834f700c77e41b0d4f7ed191ac67752d4dbf035b3ca4e31836a3a58d367f51b`

```dockerfile
```

-	Layers:
	-	`sha256:2714e2f8048ee9f7b621ad016095c9aa3c53d55e6009adb408b3430f4ac9fcaf`  
		Last Modified: Fri, 15 Aug 2025 09:37:46 GMT  
		Size: 7.4 MB (7400750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a9cc00dd8a59c8fd8a81f9422d0243063ccc42356d0f6239f61c88e0a93a37d`  
		Last Modified: Fri, 15 Aug 2025 09:37:47 GMT  
		Size: 15.8 KB (15838 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:f2f31f9251846bfae566afd5c687d9cecf517a37e2fe7e984579d1926dcd5624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 MB (220926393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9770408fe31351760e7432fcb8df1662e5b5c8ff3f100e6ab9fffdc2a5a8ad98`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
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
	-	`sha256:c3b791adea90b39bc59919a9959b7f44f65aa3364a03dd0271a5ff658488877f`  
		Last Modified: Tue, 12 Aug 2025 20:59:03 GMT  
		Size: 49.3 MB (49345161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d6b7e29e25673e60a91fd6fee9057a362045c8bda6e1e2f10253dc3291ad8b`  
		Last Modified: Wed, 13 Aug 2025 17:27:59 GMT  
		Size: 85.2 MB (85226407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb755ee4c758cbca883926945c5bbbd62162bd2e7aefc6aedac2f72e54dcba6`  
		Last Modified: Wed, 13 Aug 2025 07:30:28 GMT  
		Size: 86.4 MB (86353783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7617310a9691be9af82e6fc115d473364590b8a4d2bf228545ae3d2e717caa`  
		Last Modified: Wed, 13 Aug 2025 07:31:02 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217934142a07859f964d78eb08a6f8bd1490cd2651522ddcc40869fdea5eb918`  
		Last Modified: Wed, 13 Aug 2025 07:31:02 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:551458be23e7502913e66ee2037d11e0ed17d95093b11a7821984b280abf5b3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7427100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a6027eb5b0bca30ce864902e1045568dd060daf48b0332b1e4affbcb2dcae46`

```dockerfile
```

-	Layers:
	-	`sha256:ec578ee8d9dc8de246e80717e5735e03c700ab54ae5bb6cab3358399940f0732`  
		Last Modified: Wed, 13 Aug 2025 09:39:12 GMT  
		Size: 7.4 MB (7411310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fa65bd71eda2a7ca2986a2a6c6c86b49cadae08890aee539cc75addb62242be`  
		Last Modified: Wed, 13 Aug 2025 09:39:13 GMT  
		Size: 15.8 KB (15790 bytes)  
		MIME: application/vnd.in-toto+json
