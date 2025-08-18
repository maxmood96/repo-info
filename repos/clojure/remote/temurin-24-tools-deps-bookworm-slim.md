## `clojure:temurin-24-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:c76dd743516e8b2e225822c1cd3dde88336ceb6631f27f47f1d8eddcf87068fd
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

### `clojure:temurin-24-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ae34fa02384aeef13d665708fd804ce0a20ffb75db908651e272790fdf9926c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.8 MB (187786333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acded7f76716409f0f0092f1ad57f9529d410ff3bd467ab1bbbb08f94147617a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96315b1b178f9c08e69bdeaec55f0824d724c4ae6c4591e9a80e87ee2f3b511`  
		Last Modified: Mon, 18 Aug 2025 20:13:09 GMT  
		Size: 90.0 MB (89975262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c57cf889f8f6c061ba937f135933ca4ae36c492926c793b7f578852368b0a7f`  
		Last Modified: Mon, 18 Aug 2025 20:13:06 GMT  
		Size: 69.6 MB (69579773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da354197d7609e2677895709dd7ad8c067c0ec10b91250ed6a7be470ed258645`  
		Last Modified: Mon, 18 Aug 2025 17:15:10 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ce618ddf258f3d861fabe13e50fa6c20b7d529a3e04270bf303442ee214e81`  
		Last Modified: Mon, 18 Aug 2025 17:15:08 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:da985a8a88a298717a634c0bb61f00a09941ed6487458a026d4a455e1c96002f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5077793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75f5fbd1e3b36ea19e87ec627b31c53234f8e0b76790d8ca4edee8b607c1baf3`

```dockerfile
```

-	Layers:
	-	`sha256:65386ed11c05a3252bd6bc5c27886aa7f1a19465894137ed61d7aa9dfa56916a`  
		Last Modified: Mon, 18 Aug 2025 18:42:40 GMT  
		Size: 5.1 MB (5061921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9d318622b09b7062e3a6f04e6f9898ce10f09f8406a7ce41050ac39341bf751`  
		Last Modified: Mon, 18 Aug 2025 18:42:41 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:933a526e254284f9eb897a072df642bdb7cda3f993fc5194149313301b966b20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.6 MB (186628245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e942fe1180f8c32b07ab7e7a78a3b428f9aca4bdb92ac8c4a0337b39687d0b05`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b87e6bfd40fe1f401c5b893a66ab4775a180924c4ca26ac82e4428bc83ebf62e`  
		Last Modified: Mon, 18 Aug 2025 17:21:15 GMT  
		Size: 89.1 MB (89092530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2446e1af31725ec00d217e4f9db9c177d21b0aa3ce02ce7ec577a55bfb8442`  
		Last Modified: Mon, 18 Aug 2025 17:21:07 GMT  
		Size: 69.5 MB (69452674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82ed488b67184bd1110c96f641b3ff3552084e859db8149a87ee29b7f609ba4`  
		Last Modified: Mon, 18 Aug 2025 17:21:00 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4add9ed650f2d913f4f7b126c21b1a11a18d7bba0fc202da0a5887cdf3d4fc8e`  
		Last Modified: Mon, 18 Aug 2025 17:21:00 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:846348b3d4328c316aaf5240624c52b899b9add31ba60b2cc768f2622b37ee52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5083669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1156931b079b64dfcbeef4eb00678742c2b7e564df23ed78f198e4d427bd1a83`

```dockerfile
```

-	Layers:
	-	`sha256:607d5bd450fe6856e3b64727d9d13d346b0563c6615dfc3a03aa1be78b4983a1`  
		Last Modified: Mon, 18 Aug 2025 18:42:47 GMT  
		Size: 5.1 MB (5067679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e92c471974f02bed8cb933ae04a24b069c52d99cf6c37a31529a60ee8314097b`  
		Last Modified: Mon, 18 Aug 2025 18:42:48 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:4197b0f6c794d50ff2802660d32af671edf459ad46b11f7dcb633489b7fe5b2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.4 MB (197398747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da1b585432eda17c7132a85fc841ed306befee996bed9b5e252d344722ce7fb0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72057f440526db0265c67512fdb1713f87ba9913daf842bcb2fc8b89526344fe`  
		Last Modified: Mon, 18 Aug 2025 17:37:14 GMT  
		Size: 89.9 MB (89918259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4c2e8461c75ac51d1d825211f75ebe3ab2f513d95668b4688a1940ce8cff09`  
		Last Modified: Mon, 18 Aug 2025 17:37:09 GMT  
		Size: 75.4 MB (75406025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31041622c97737a80baaf21c51b596581222c86e45773c7c4dd45da9f074ed32`  
		Last Modified: Mon, 18 Aug 2025 17:37:01 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a720218d11c06522549502cfbe525686771a3c3c619495c52474d4bfe598326e`  
		Last Modified: Mon, 18 Aug 2025 17:37:01 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dff426f1c778711a80c132bb22eda13058d3a2d1f2c72f4b1e1c42373ee122c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5084296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0380ec3edd65ea2bfd55daa6952e6e4f6eab39385c86f9f29a8c659e2b09536a`

```dockerfile
```

-	Layers:
	-	`sha256:7f2826ffa04552a5e959385d072bb6351180c99042fd2a14113bd90ee9c2e1da`  
		Last Modified: Mon, 18 Aug 2025 18:42:53 GMT  
		Size: 5.1 MB (5068377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:903afc9846dacd0e16db2c379c9151937249626d17d86b8b2570122e0c3b0df7`  
		Last Modified: Mon, 18 Aug 2025 18:42:54 GMT  
		Size: 15.9 KB (15919 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:b5404ccbf2ed51b3971193c41039676eced675412a28583b909dba6083d89feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.5 MB (180457287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0733f803c62452728014ed9e9b817142de565413f51272254ba55c6ac084dae1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
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
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c94aa6edd5ef2455ec9053295a37e8950ea22ff4805d862dd5baba16d5ff1451`  
		Last Modified: Wed, 13 Aug 2025 18:14:31 GMT  
		Size: 85.2 MB (85226400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ebf3bea4a633e9da9cd7ff40924334db3ec19dd44cec2501fbc23e22a97c872`  
		Last Modified: Wed, 13 Aug 2025 18:15:11 GMT  
		Size: 68.3 MB (68342007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613455bb695efae56cc7d67f05ca56b393cd68fd3f562056501050df54760c41`  
		Last Modified: Wed, 13 Aug 2025 18:15:07 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:268ee7895136e2e0686dd3303a17eaca0855061ddb66f2ed6d385f87ccd3f5ae`  
		Last Modified: Wed, 13 Aug 2025 18:15:07 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:eb0d7867adb3e04c8fe85913352ea51eab53b64f43558061d48ecfe6838a0b0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5071633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8761147c717ee4da16b2aad67f764518bf7bc80a528485b8c2c216d255edfcb4`

```dockerfile
```

-	Layers:
	-	`sha256:d5537234e9dfcf21c0987219f0492152ab6dde75b0992b7c17885e1da8221256`  
		Last Modified: Wed, 13 Aug 2025 18:37:17 GMT  
		Size: 5.1 MB (5055761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69f5fb5f49a38dc970fedce703402a634105143749c81f62ce208521975b12be`  
		Last Modified: Wed, 13 Aug 2025 18:37:18 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json
