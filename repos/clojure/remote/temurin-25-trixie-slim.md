## `clojure:temurin-25-trixie-slim`

```console
$ docker pull clojure@sha256:04f577ac5952e64ae9030fa0c35f1dcd85e266975815dd74a6f35b999f92845d
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

### `clojure:temurin-25-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:eb4d2fe98fc688f3b067a1b0ae20692ff3398d4879c192415c5ef54ae9338557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193818808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcce5203de0e00f827c3b458c9c496b5e90084876e89e755c7c1e6636430186b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:57:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:57:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:57:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:57:24 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 23:57:24 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:57:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 08 Dec 2025 23:57:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 08 Dec 2025 23:57:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 08 Dec 2025 23:57:39 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 08 Dec 2025 23:57:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d8dd3b1dc7c187699b043db13acf83edae73d4b478d48fc28f957d63ab6a38`  
		Last Modified: Mon, 08 Dec 2025 23:58:19 GMT  
		Size: 92.0 MB (92045295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d830a6715d6042023a4f599c9a987f5593655d36e1d595d0a108ebeed29bae`  
		Last Modified: Mon, 08 Dec 2025 23:58:15 GMT  
		Size: 72.0 MB (71995977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a290f1ab1ffa51d239e33348459be77c1804b67e28aa8de44cf7f7cf275b3790`  
		Last Modified: Mon, 08 Dec 2025 23:58:06 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b291e1afc7d91706ea285a60ef20f5a127d0f37442dc2b2cc82b76f46db2b8fe`  
		Last Modified: Mon, 08 Dec 2025 23:58:06 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ef5224b0c409a51ab854087e33b003f74f97d7e7184742d3cf8e98e108abc760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5224042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6659536b7870b0db4d33652340781579f3fca0f34b637fe3b5e1814c1332190b`

```dockerfile
```

-	Layers:
	-	`sha256:5f2ca1ecf7b3eadaa54eb35a7a9dbd550891c1df5ef6566438fe4059aed0952c`  
		Last Modified: Tue, 09 Dec 2025 04:47:16 GMT  
		Size: 5.2 MB (5207549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee5f3b1a140cb8ed8a899714fc36df91b20a2e2ef7492940a92a2d931eecae64`  
		Last Modified: Tue, 09 Dec 2025 04:47:17 GMT  
		Size: 16.5 KB (16493 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:65f78ed64f23936383da791e94113e520ed86dca4fa388c44218d2ffebade3f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 MB (193000810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e79776ae6d849279cc9d8cf04e98a3c812d4b08fb09278072544396666c1d75f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:03:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 00:03:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 00:03:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 00:03:49 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 09 Dec 2025 00:03:49 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 00:04:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 09 Dec 2025 00:04:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 09 Dec 2025 00:04:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 00:04:06 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 00:04:06 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7113251430737f9cea145eaf063821f03713eba6dff0f4449a1829360eed78`  
		Last Modified: Tue, 09 Dec 2025 00:04:40 GMT  
		Size: 91.1 MB (91052502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03678b2787c87797f1606a68fdb86beb569821276ce58c3c66b491776a2e2f98`  
		Last Modified: Tue, 09 Dec 2025 00:04:37 GMT  
		Size: 71.8 MB (71808640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c780831bb5564a6412943b8712a667bfbd159eaf1ca136caf3761874400b84f`  
		Last Modified: Tue, 09 Dec 2025 00:04:32 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649faa195676c04dd04d880e39aadda1b6cd90ec4a048e481e033c3749d69e0d`  
		Last Modified: Tue, 09 Dec 2025 00:04:33 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a39d826af55d57cbbd1bc716f75c07caca031711ce3c213f9db95cdd84627395
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04d4b4b90a0a78015dcdcc674be39b3abc5b4aef9ed52a1f762d007bed6104d4`

```dockerfile
```

-	Layers:
	-	`sha256:a3d2a2b28a350562bfb6b345ac899948d111bd0aca9a5d67d1e18491a7c0e724`  
		Last Modified: Tue, 09 Dec 2025 04:47:23 GMT  
		Size: 5.2 MB (5213339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e21295d1dcf06139e857fa9c0a2ffd00f98f08d89efe8034a12cfdf7a6435a0`  
		Last Modified: Tue, 09 Dec 2025 04:47:24 GMT  
		Size: 16.6 KB (16635 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:d5e7e7fd678e395a1068d63dbf482808d7bfdc38e495b46d9d84238612608398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.6 MB (202600350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075d11c47dc980d17b8b9931e45b9707fee02baa9440d9fce8b8e5a8ed8da150`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 03:55:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 03:55:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 03:55:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 03:55:25 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 09 Dec 2025 03:55:26 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 03:56:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 09 Dec 2025 03:56:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 09 Dec 2025 03:56:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 03:56:16 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 03:56:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e90333d0ab795a7ae2c0a51c53552c38eb8f814a4df79b46ded26ce84b6fab`  
		Last Modified: Tue, 09 Dec 2025 03:57:08 GMT  
		Size: 91.6 MB (91610796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf8f28eed9826544b9b7aed8f3e6cc5cd3785e20f5457a85b6a75062c6d188c`  
		Last Modified: Tue, 09 Dec 2025 03:57:06 GMT  
		Size: 77.4 MB (77391626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822dab5493fcf8423f64455e758a850f5a7142704399cdc9e3857cceb9e79a8c`  
		Last Modified: Tue, 09 Dec 2025 03:57:00 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb54fe714c4b7fb5b37aaa0c7638fe0d1c85f1d159a1374eef44399f649ac8ff`  
		Last Modified: Tue, 09 Dec 2025 03:57:00 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6f09a730224a0b733f91b3a96fb749125e72eb946fe840afc9abb00d866f6d10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d61946073f77953fb08d4ffbc1d8146c05526e9b57d66194802b502c7244da2`

```dockerfile
```

-	Layers:
	-	`sha256:2ff2f30ca3828d51d94dafaeaf616c1b7c72fd65f0d621a2357f0f03f7103790`  
		Last Modified: Tue, 09 Dec 2025 04:47:30 GMT  
		Size: 5.2 MB (5213230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70e1e1aedac6d71eade6a746cc68882f44df1a6eb2be9f071b022f2b75bc688c`  
		Last Modified: Tue, 09 Dec 2025 04:47:31 GMT  
		Size: 16.6 KB (16551 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:4fca91f25949bbc97ae1bf8b3271c467b0696eeaf7cbb0e76f6d2cb84c187995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.9 MB (189907703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e973002afe9d56d7dd58e9d4dfb807f0abc998450a9430682a0eea0879debb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Thu, 20 Nov 2025 18:54:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 20 Nov 2025 18:54:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 20 Nov 2025 18:54:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 20 Nov 2025 18:54:05 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Thu, 20 Nov 2025 18:54:05 GMT
WORKDIR /tmp
# Thu, 20 Nov 2025 19:09:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 20 Nov 2025 19:09:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 20 Nov 2025 19:09:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 20 Nov 2025 19:09:49 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 20 Nov 2025 19:09:49 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e6d736f22fbd16f11de06f0cbb3ad19602da41d0ae18c2694b069ccfe7a409`  
		Last Modified: Thu, 20 Nov 2025 18:59:39 GMT  
		Size: 90.8 MB (90752878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c984831c7d0bb12b1a247ff56d2fd1a036e695717a635da3b6407225e1a2324`  
		Last Modified: Thu, 20 Nov 2025 19:13:40 GMT  
		Size: 70.9 MB (70880654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a968300f69805e85f31f6fd5b900d7c43dd72cf1b4d6138e897d7194b54c656`  
		Last Modified: Thu, 20 Nov 2025 19:13:30 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3dba38d726ae41f643a2801ae343077014ac3d89bbb1baf493886c26741de22`  
		Last Modified: Thu, 20 Nov 2025 19:13:30 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1d80d022b1bf8ce12df89ef99ffd0c1ce41419080a20d3f81abd96323816bfaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5213572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6b705302729a3ad056fbdef51b12d4b9f82a3a31ca6e5148076197788340449`

```dockerfile
```

-	Layers:
	-	`sha256:1d8d7fb5d1c5364ebb424b5dc3ec01f49701fc3f4e9056cd4243202d33b17424`  
		Last Modified: Thu, 20 Nov 2025 19:38:25 GMT  
		Size: 5.2 MB (5197022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:393b39d896d3afc39da6b1b79c0abef3aff51ceb128a4fd2d58e23e7d37833e1`  
		Last Modified: Thu, 20 Nov 2025 19:38:31 GMT  
		Size: 16.6 KB (16550 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:85fa28e5bd1e003ee285126c6329fb937f28ae00958da4f46a4afcb1fb53718f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.0 MB (190999505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:510872dc87c676f3c4fcc22df31892cca818e1794ab287753f41a4bf938b0273`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 01:33:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 01:33:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 01:33:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 01:33:39 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 09 Dec 2025 01:33:39 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 01:35:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 09 Dec 2025 01:35:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 09 Dec 2025 01:35:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 01:35:12 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 01:35:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:deacec5e6af82b258c59e95e3e86abeef36fad06b1d9ff2de33e88544ffb79ff`  
		Last Modified: Mon, 08 Dec 2025 22:20:52 GMT  
		Size: 29.8 MB (29834400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b901607e1053160f0c4a5999035c86877af07f0a5ab635c3250bef9051f1d4`  
		Last Modified: Tue, 09 Dec 2025 01:34:38 GMT  
		Size: 88.2 MB (88210741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f29d73214a6b4479e119138702ef79484fd7534f8ca9fab0c5643acab3f2e3f`  
		Last Modified: Tue, 09 Dec 2025 01:35:48 GMT  
		Size: 73.0 MB (72953323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee5eb2d580ef9bd2aa76562f1b43ca519b34ecf5646463ca5493ab7226174a1`  
		Last Modified: Tue, 09 Dec 2025 01:35:43 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d15685aec40194194d927cf14298106d39d873f83a07b74da8cb4507956d45`  
		Last Modified: Tue, 09 Dec 2025 01:35:43 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:04655a74c37d26b1f6540413dce33cbebc7670c56bd3a062b51757b22725a6a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5222514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cff36382867cd14028659b5fe118c173995529128fc29cac869692e083fa4725`

```dockerfile
```

-	Layers:
	-	`sha256:4b513d67551473d58bed7cc07c2cb0578dece2e2bc0a9dbf837830e978a0efa3`  
		Last Modified: Tue, 09 Dec 2025 04:47:41 GMT  
		Size: 5.2 MB (5206021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a30e40fef875f6d8da7a84c619fb926d8375954a2165b957477e1691396551cd`  
		Last Modified: Tue, 09 Dec 2025 04:47:44 GMT  
		Size: 16.5 KB (16493 bytes)  
		MIME: application/vnd.in-toto+json
