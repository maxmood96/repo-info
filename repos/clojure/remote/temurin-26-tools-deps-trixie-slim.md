## `clojure:temurin-26-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:8735f5d4ab6c731b934b8e38ba8fd3880464e65b1fc1df56a1c219da3c9fe8f2
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
$ docker pull clojure@sha256:0f7a9ac083fd432984122ff61848aaf5bde2040b9be1ac096195348485306896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.8 MB (204809251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efb6cd2f29d90860cb531cdbe2161270baecb8d14312fcefdd460616a6d83803`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 08:52:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 08:52:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 08:52:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 08:52:30 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 08:52:31 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 08:56:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 08:56:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 08:56:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 08:56:17 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 08:56:17 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e771730505306c65b920a33ea03d87b316b140e1fe4d13ec6a98c1278d920c3a`  
		Last Modified: Wed, 22 Apr 2026 08:53:41 GMT  
		Size: 93.8 MB (93781494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8373c0f62241966237311cf27655f2ffa5199dbd7f2b2d461d2324a1dbcbea6`  
		Last Modified: Wed, 22 Apr 2026 08:56:53 GMT  
		Size: 77.4 MB (77428690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7706d05826018f9c78aefbc6befd5bb6ac4d821243baa99f5ea4ef66605c6b59`  
		Last Modified: Wed, 22 Apr 2026 08:56:51 GMT  
		Size: 609.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4315b1e98556f8f666fc098c3224bfd8fbeae9d8859288ac55906013515b2369`  
		Last Modified: Wed, 22 Apr 2026 08:56:51 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fff36e7e596901befd404c1dea8964fc323bb5a29cf8385369fb5a0b6764814e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5228856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e8643e214e7550c608e0751ecc19b3555084b15bd2f44a5928b873427ba9ba0`

```dockerfile
```

-	Layers:
	-	`sha256:9d397371c2603a53e7f38d9820954f168f15328a325dd777e14d8671ef869ef3`  
		Last Modified: Wed, 22 Apr 2026 08:56:51 GMT  
		Size: 5.2 MB (5213003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b35ff088a8d0af786a096f98e41a4f7dd36ac6b5ef5e5efcdd06e6bd932364d`  
		Last Modified: Wed, 22 Apr 2026 08:56:50 GMT  
		Size: 15.9 KB (15853 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:7af8afea9d39b5764273c0a4b76ea23b57d4d1bd3477538633fae698be0da22d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 MB (192190233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e469c060b1f789c59c59ed6c42326aec9dfef498f24940ef3ff2afe4132686d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Fri, 24 Apr 2026 19:10:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 24 Apr 2026 19:10:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 24 Apr 2026 19:10:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Apr 2026 19:10:34 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 24 Apr 2026 19:10:34 GMT
WORKDIR /tmp
# Fri, 24 Apr 2026 19:26:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 24 Apr 2026 19:26:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 24 Apr 2026 19:26:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 24 Apr 2026 19:26:38 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 24 Apr 2026 19:26:38 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4570a2040f6cfb5fdde4314c204e28e913195fc06cfb70d3ed0994fb7a93519a`  
		Last Modified: Fri, 24 Apr 2026 19:15:57 GMT  
		Size: 93.0 MB (93008135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d7aafa3a88c354e3b14e67e21485b3b14ecf5b7b6794eadadd0c183d4fa060`  
		Last Modified: Fri, 24 Apr 2026 19:30:09 GMT  
		Size: 70.9 MB (70900863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4175bf8f566a106c56f244fda6edcf5b86f897f2b9bd6f1b5afa415b11a1958`  
		Last Modified: Fri, 24 Apr 2026 19:29:58 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77da22c728253cf1215f5d727d3734f7d8f4809521153d3ce10060548cd8fb19`  
		Last Modified: Fri, 24 Apr 2026 19:29:58 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1b9010f629abd5995ca1e95f3c950de339928c02086ca37543f5294cad3ff064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5212648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f230dec7ad72de068275f499e022759b2f4cfe53c1d627fbd4a4b8bf1be026d`

```dockerfile
```

-	Layers:
	-	`sha256:d265cf604a10fa167a3c0bafea61c3bab16da1dddb245ebddb744e9f3d457b69`  
		Last Modified: Fri, 24 Apr 2026 19:29:59 GMT  
		Size: 5.2 MB (5196795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6e4b428660b4bf2a272b43f115f991a0407321b4d98d7f4c1b9189d831f0a43`  
		Last Modified: Fri, 24 Apr 2026 19:29:58 GMT  
		Size: 15.9 KB (15853 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:e20440ab958ce121e5d5155bcd109e63ba06071f329022391f9a7cc83a084c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.4 MB (193375890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dfd1acbc79f9b163fa9e7f3d0f2e9f1d4d0dc237916f8767685be105537fa19`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 04:07:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 04:07:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 04:07:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 04:07:17 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 04:07:17 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 04:08:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 04:08:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 04:08:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 04:08:34 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 04:08:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6552167c3fb921ccc494ee3bece04b6397bc0c70a2295fcbb0589332416e0edd`  
		Last Modified: Wed, 22 Apr 2026 04:07:58 GMT  
		Size: 90.5 MB (90547693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c17b0f285d4bfcede4330b8475135aa775b18d5e554ebfaf0ef28da710606e3`  
		Last Modified: Wed, 22 Apr 2026 04:08:58 GMT  
		Size: 73.0 MB (72986856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012f3b27ee5b25aeac2ec9716690662258544ff5b131aee292f264b1921c02a9`  
		Last Modified: Wed, 22 Apr 2026 04:08:56 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa00bf070dc8fd386c7d5eff62c8f1a8ac36c72cec81117667b719e2e741a2a`  
		Last Modified: Wed, 22 Apr 2026 04:08:56 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:de34cd98206793c1635b956e78f1b8bd95f75ef7328ed30a232197d66421d073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5221611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f9dd35446b024d54430a119d5a0fb7ba35d8a84ef94872687682801ec70889`

```dockerfile
```

-	Layers:
	-	`sha256:ce522e10084cf4dc9069ae06576924647866add90964073ffa71582a8edb2603`  
		Last Modified: Wed, 22 Apr 2026 04:08:56 GMT  
		Size: 5.2 MB (5205806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb8b6f079b27fd368aaa8230d451087aa58c20a6456d791304578163e861f51c`  
		Last Modified: Wed, 22 Apr 2026 04:08:56 GMT  
		Size: 15.8 KB (15805 bytes)  
		MIME: application/vnd.in-toto+json
