## `clojure:temurin-26-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:c30dbbc9638e6c9148602d61a159eb8300fe437ec91a3dc35937246f1a86801e
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

### `clojure:temurin-26-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e7123387e0586ce3e8ebfaa45d10cd0a0099ef9e0c8e409f79ad524b07474b3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.2 MB (196248082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebe3cd5d5e66a0a0ae80a610dc86b960547b3eb76e60685a259bd355f70718c1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:22:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:22:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:22:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:22:17 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:22:17 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:22:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:22:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:22:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:22:32 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:22:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fcda5d39d379c60b31dd9ddd9104c436e9b0e529d066197aacfb6182efd9972`  
		Last Modified: Wed, 22 Apr 2026 02:22:53 GMT  
		Size: 94.5 MB (94455690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970e2b3ab58dc4684e8eafc047f72aaeb68fc9d15d63ee503ea62cd279b34986`  
		Last Modified: Wed, 22 Apr 2026 02:22:53 GMT  
		Size: 72.0 MB (72011179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f97a70a90d67277bd6c669b51ad6fb6735c851b263d6db94dbe478fe0d86f5`  
		Last Modified: Wed, 22 Apr 2026 02:22:49 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b78217a14862f298d4f25d013aff03506b4ddeebdee6772f72f6920527df334`  
		Last Modified: Wed, 22 Apr 2026 02:22:49 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0b1eaadedde9c6ad1680f823e02edd32cdcd3dd9733fcea834d5b1d7e34751c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5240501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7941eaf7509d9077a0979a61f534e684d4b656c8d5638d347901a55840af36e2`

```dockerfile
```

-	Layers:
	-	`sha256:8a830e529271a2c24ed45f7955a9916f828def2492e0e24ae198163425a9df5c`  
		Last Modified: Wed, 22 Apr 2026 02:22:50 GMT  
		Size: 5.2 MB (5224696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecbe0e26f7be4f57f0212e69bc7b39a8c7b76daffa15365a71a9d537e2d7d38d`  
		Last Modified: Wed, 22 Apr 2026 02:22:49 GMT  
		Size: 15.8 KB (15805 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:617549a89e1b811d565fb81cb8d637238ffb591f617eaaa14419b7240497f407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.4 MB (195370837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e306ec4da0a2101ead5947392c5333077a7497a2741b97b416a1fcd12bdd676e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:25:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:25:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:25:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:25:24 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:25:24 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:25:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:25:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:25:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:25:42 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:25:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847e1a865f0f2effb7dc3de47305db674e73c067232661263821c44c73e54b9c`  
		Last Modified: Wed, 22 Apr 2026 02:26:04 GMT  
		Size: 93.4 MB (93395200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d1b50a69f6ea18afffcc7f43dc7f8f5d22567ffd95fa8dc005ba7e1842a432d`  
		Last Modified: Wed, 22 Apr 2026 02:26:03 GMT  
		Size: 71.8 MB (71830992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e22e1713129c8df714251933fd984eb968f6b893e265f9e721fff383b74dd3`  
		Last Modified: Wed, 22 Apr 2026 02:26:01 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf84fd1b579a6128ad0988d5d5a4a029969385702fa44d34e0cf66caf2b0185`  
		Last Modified: Wed, 22 Apr 2026 02:26:01 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f279bfe4a01b88247416304c3c1a79f6814a83f2b1649b6a017dd618a9fdb9fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5246384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574ba58dce384433bd2f43db9760c7134a52bc690955529ac92909591385a4c9`

```dockerfile
```

-	Layers:
	-	`sha256:e3f478a3f8903d5587fa2cda5e1fea348de22121fc2c7a83cab576ddcad6fe62`  
		Last Modified: Wed, 22 Apr 2026 02:26:01 GMT  
		Size: 5.2 MB (5230462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef395c138dadf614270c1c0ce8195e6f3a31cf8ed218480e2c03047351841e27`  
		Last Modified: Wed, 22 Apr 2026 02:26:00 GMT  
		Size: 15.9 KB (15922 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:885e9fad9902b27b753ec2579b6f3b7aefee87b093e1aebbbb346c10da9a5f03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.0 MB (207985989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b869cae6c8fbc7787bf00ffe434fb64c444572a3821b515826541cb5c8642251`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Fri, 10 Apr 2026 00:53:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 10 Apr 2026 00:53:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 10 Apr 2026 00:53:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Apr 2026 00:53:44 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 10 Apr 2026 00:53:45 GMT
WORKDIR /tmp
# Fri, 10 Apr 2026 00:58:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 10 Apr 2026 00:58:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 10 Apr 2026 00:58:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 10 Apr 2026 00:58:42 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 10 Apr 2026 00:58:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ad9d78de109af0508c6cea77373f8cb08369c373cf24c72f7da9935301139a`  
		Last Modified: Fri, 10 Apr 2026 00:55:00 GMT  
		Size: 93.8 MB (93781481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac72e545ef7eefd4903d47a4d9541b09a6a095df7fdd043f838ec6ab97bea3c`  
		Last Modified: Fri, 10 Apr 2026 00:59:18 GMT  
		Size: 80.6 MB (80610448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5770d7433e19a249b7ef4a5e0d8e1e91476ea5cc03899e54182e4fd200998295`  
		Last Modified: Fri, 10 Apr 2026 00:59:16 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af421ae655820796b85429674b1042a4fbc995ca03e4412b7cc1690a2ce97157`  
		Last Modified: Fri, 10 Apr 2026 00:59:16 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7fb3abb958dfcd8a9cc718c35d6efa459a9534434d13a98e55a257248fd6decb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5228802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef1886867b07d17a91ad194af5b409b850b325f4df8ed4f7ea5537553d32cf12`

```dockerfile
```

-	Layers:
	-	`sha256:9ac52f6a9af55208ef981b4006459f47596280aae5bfa0d8c807fcfa25073a60`  
		Last Modified: Thu, 16 Apr 2026 03:18:34 GMT  
		Size: 5.2 MB (5212949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e510e9704a8cc8ad66b9d7473efa5cc247f6c0a47a9dc9a8e5e901bd1ccee15`  
		Last Modified: Thu, 16 Apr 2026 03:18:34 GMT  
		Size: 15.9 KB (15853 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:8289c431dd701e310b022923183b0a9513e44adb40a3d6a07d0174c3856d5bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.8 MB (194804089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:961192848b537541886385f037ac2315de7ad53b86a73595907673ee13db98df`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Sun, 12 Apr 2026 18:55:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 12 Apr 2026 18:55:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sun, 12 Apr 2026 18:55:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 12 Apr 2026 18:55:33 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Sat, 18 Apr 2026 05:58:19 GMT
WORKDIR /tmp
# Sat, 18 Apr 2026 06:19:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 18 Apr 2026 06:19:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 18 Apr 2026 06:19:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 18 Apr 2026 06:19:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 18 Apr 2026 06:19:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7fc246f5e32984af9b4236c90104244f3679fa7192854d7e61221c59edbfc2c`  
		Last Modified: Sun, 12 Apr 2026 19:01:08 GMT  
		Size: 93.0 MB (93008131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a8e63f51a11c3d3c0573ef3c09f3ffb158a873fc1efa913495fdb80a05529a9`  
		Last Modified: Sat, 18 Apr 2026 06:23:09 GMT  
		Size: 73.5 MB (73519133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709db08c6a081196e38ae4b5b2db2ceec86c0a8c6e36fb55e33e909074e211a1`  
		Last Modified: Sat, 18 Apr 2026 06:22:57 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fa14834f228bf7327f3f241f4df700e799ce1612422421d1c85c1defacc499`  
		Last Modified: Sat, 18 Apr 2026 06:22:57 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1e8c096417f6e77ee427e0285f10562bbf3903ffd0fd83c86577d7d69970812f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5212594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30d49fda5af6e92d1a6897b56b0edbecd62d050f5ac12e308ff12ca759edecd0`

```dockerfile
```

-	Layers:
	-	`sha256:12c687006908b6d7cac59681e544eb5d05e141b8a127c73e0e3c6f1be73469bd`  
		Last Modified: Sat, 18 Apr 2026 06:22:58 GMT  
		Size: 5.2 MB (5196741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:695b08ddc99ca42beb7d8de69927c3f5fda49250dc5634fd496e21db0fff82ef`  
		Last Modified: Sat, 18 Apr 2026 06:22:57 GMT  
		Size: 15.9 KB (15853 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:3c1f39dec1d6d5b1b7a0b3b59633da3dfda8254cd17bf28b29332839e61b1d02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.0 MB (195982824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84edd2105d0e009c384a1d9245ca64fd8d6cf339f4c6440a65652170e114ab9d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Thu, 16 Apr 2026 00:46:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 00:46:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 00:46:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 00:46:45 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 00:46:46 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 00:47:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 00:47:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 00:47:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 00:47:57 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 00:47:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d73a2a76ddf7460ab2878123e70b72f683be95027429b7589ec35877df13dc`  
		Last Modified: Thu, 16 Apr 2026 00:47:24 GMT  
		Size: 90.5 MB (90547699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ad69d85d809c5dc4fdfa3ad7a95bef300ed6ae0e069fcf59199845beb449da`  
		Last Modified: Thu, 16 Apr 2026 00:48:22 GMT  
		Size: 75.6 MB (75598667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bcd544d6f72148576e8737de30d8b7f67f96cd2d1e72e451a76c262ef2781b4`  
		Last Modified: Thu, 16 Apr 2026 00:48:20 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004348d1b6eb58c750640697f74d1e77e555516da0e835a048b4e6312f98daa0`  
		Last Modified: Thu, 16 Apr 2026 00:48:20 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:780df2a843451a21175e19abbcd3e61859f56fb4d04827140ea907df2207c0e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5221556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc82f280e98e2dcfcfda36656c38aef384f8a75afcb292305295c8ad840da0b5`

```dockerfile
```

-	Layers:
	-	`sha256:56431f1ad1354824ed76873607154118314d40aff6e5fe189652b2c88b7554bf`  
		Last Modified: Thu, 16 Apr 2026 00:48:20 GMT  
		Size: 5.2 MB (5205752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b6f5a0ca8a549a288d7933280b667f10a4eea1d3349e77fdc1bad5a9f386fa7`  
		Last Modified: Thu, 16 Apr 2026 00:48:20 GMT  
		Size: 15.8 KB (15804 bytes)  
		MIME: application/vnd.in-toto+json
