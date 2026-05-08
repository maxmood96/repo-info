## `clojure:temurin-21-tools-deps-trixie`

```console
$ docker pull clojure@sha256:94999bd48c65eab1fef5c8ce625c35a8d347af18f322066a79b001b00302869a
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

### `clojure:temurin-21-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:09afb597fc492e7759851ffdecb6e126901ae7edb2f428651b700f6dae17d17c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.0 MB (293040441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:675d62733cb33d3011aeb9195bd97e7953613553121807e49797002deccabe9e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 00:27:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:27:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:27:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:27:32 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:27:32 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:27:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:27:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:27:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:27:50 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:27:50 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3b32e3bb7338c216b077e95920ae53332d81bd57f4a7393bc324432d5a3f88a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:56 GMT  
		Size: 49.3 MB (49302102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab00ef5327f96f780fe870bbf0dbe0878b26307c9df76b8a9ecefaf00478d562`  
		Last Modified: Fri, 08 May 2026 00:28:14 GMT  
		Size: 158.2 MB (158166935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6a33108cb4189ad7961b01efbb9ad56ce4b2768c0b7264bdc7c9e815dc6451`  
		Last Modified: Fri, 08 May 2026 00:28:19 GMT  
		Size: 85.6 MB (85570362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6886d5b74fd8366bd273566df965a0b7cefd69f23390fd72362b883c5221fc76`  
		Last Modified: Fri, 08 May 2026 00:28:11 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c8c7ebc28cd72eef115e9662afd07a5e0ddea85053be5f90fd695a3b747f5a`  
		Last Modified: Fri, 08 May 2026 00:28:11 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:112398867d4bb43d9f1aebb4b091f03c888168f1e9594312bd273c71767bdff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7489107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb8a81d9c18bf19144dce9696173e5f71ae8cf0ea453f8d07869d0fc5c0af556`

```dockerfile
```

-	Layers:
	-	`sha256:d9832cf467d1ccb5d82480b162c4bb19d43d0a4deed88410abda7690edc4844c`  
		Last Modified: Fri, 08 May 2026 00:28:11 GMT  
		Size: 7.5 MB (7473200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a3a0375d1723578007b99b6742a32dc9e0cfc565a9f3c3d4c33c08f5bbf8445`  
		Last Modified: Fri, 08 May 2026 00:28:11 GMT  
		Size: 15.9 KB (15907 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0e169d2ffc2d1dee4cc0cc56b1f550544abfaa8a97051cb88b63c8b3ed1a9e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.5 MB (291514999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0b01dd816d36a3a370f8af5a26cfc240cf7a64b5814c34ae6dbaffe55eefa45`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 00:26:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:26:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:26:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:26:44 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:26:44 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:27:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:27:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:27:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:27:02 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:27:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6e7932d5cb5573d1bff4fb8801baad19fc72d2ae741bb046333573653944f5a5`  
		Last Modified: Wed, 22 Apr 2026 00:16:45 GMT  
		Size: 49.7 MB (49669245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1897eacd9df5ce28cf79fdecd8ec6f06eba17dbcd736e9a00a995fe4dc2b35ac`  
		Last Modified: Fri, 08 May 2026 00:27:31 GMT  
		Size: 156.5 MB (156461191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae17a65c26a5fc99eae793334ad694f7f20f5249fcca6f375fc3343c7e8a4c10`  
		Last Modified: Fri, 08 May 2026 00:27:27 GMT  
		Size: 85.4 MB (85383525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22fe0d1692b5e17865c2f3a98cba8156aa24550d81feff8e0bd05fed8941f425`  
		Last Modified: Fri, 08 May 2026 00:27:23 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08642dfd1e0b4e35362a7d1557a0ccb019280cd6b673a3503f6dc626cd52826c`  
		Last Modified: Fri, 08 May 2026 00:27:23 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:53384a612a2b514ca6af906f474f060ba9b5d51c6787c174d74836f1ef4b4511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7496256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ace8903f61abf2f8f94196b0b3f315a1af02dbe246feb8609285d0be7f5e658`

```dockerfile
```

-	Layers:
	-	`sha256:633bd7318dedb5ab486928f1cb609149a3cce262e9023fa46a4d8ed98310658f`  
		Last Modified: Fri, 08 May 2026 00:27:24 GMT  
		Size: 7.5 MB (7480230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7586f55ab872c050cad05fdbee08ae73cd58bf411f96d8034fa1077c199b061`  
		Last Modified: Fri, 08 May 2026 00:27:23 GMT  
		Size: 16.0 KB (16026 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:70c2630dbeb41741ce7984f340a44cacf79a6132a864e046a932ef29575b6aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.5 MB (302453615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3896e832e1b6bbba19218e0905a6d94f089d61701c8c9894ca2e94596b5d751`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 01:38:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 01:38:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 01:38:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 01:38:05 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 01:38:06 GMT
WORKDIR /tmp
# Fri, 08 May 2026 01:42:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 01:42:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 01:42:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 01:42:41 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 01:42:41 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0fab4f6170940889900b2327e1b3c62dace993eab8074ca7d33d1ffeef137c08`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 53.1 MB (53122984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef2aeb89dd432248a27be9658c9ad2fe8736e1bb0a40602c7b1b444a977ed1e`  
		Last Modified: Fri, 08 May 2026 01:39:21 GMT  
		Size: 158.3 MB (158343239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a7e4ef72133a6c9dd402973c479574b5d7cf184082f20abb89c47f9a3ec02ff`  
		Last Modified: Fri, 08 May 2026 01:43:17 GMT  
		Size: 91.0 MB (90986352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed836d8ee30823a14faf982ad9467edd66a04ed488d3121e9b24d73ea60d48e0`  
		Last Modified: Fri, 08 May 2026 01:43:15 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc1cb60dd07f4ea1625f8741262d4afc2ba4c39b0eecdda0d27788d1371d801`  
		Last Modified: Fri, 08 May 2026 01:43:15 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f8823656ea24b2ea26ce6a2a44a31cfe2ea33f5f117ebb705f860008d0df5c7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7493576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27dcd2d252a19ff68de95344d1b7135d367f2cc91163c3cf81379ebb06580ad9`

```dockerfile
```

-	Layers:
	-	`sha256:4a1a2c87f3a9dde89d13096b0b50d7e5155756dbfee0b0fec59221c15d70a013`  
		Last Modified: Fri, 08 May 2026 01:43:15 GMT  
		Size: 7.5 MB (7477621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ca05686a224b995e61f30bf079969214b2cddda8b9769635a6441acf3b708c4`  
		Last Modified: Fri, 08 May 2026 01:43:14 GMT  
		Size: 16.0 KB (15955 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:f00c43878ea30a2ef5ac0f5a9325c68bdf2a0705dfc1ee83bbd2c8435f614601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.5 MB (289476031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d1d7e7d50dd759bf6afa5677cd47dd8668dbbf479bfe8f3bff312daa7c902a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Fri, 24 Apr 2026 18:09:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 24 Apr 2026 18:09:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 24 Apr 2026 18:09:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Apr 2026 18:09:44 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 24 Apr 2026 18:09:44 GMT
WORKDIR /tmp
# Fri, 24 Apr 2026 18:26:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 24 Apr 2026 18:26:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 24 Apr 2026 18:26:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 24 Apr 2026 18:26:08 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 24 Apr 2026 18:26:08 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6e518626ae0de2d990c7c66185d308a25cb3affebb6204543438f56fd9f94992`  
		Last Modified: Wed, 22 Apr 2026 02:29:17 GMT  
		Size: 47.8 MB (47798217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d4384d0aaf4c67d90bf2e07cb4852bca10fcf970d4b6c61ba3f1acafc7915a`  
		Last Modified: Fri, 24 Apr 2026 18:16:13 GMT  
		Size: 157.2 MB (157216912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0585ff758ed9b6f7c69ee80876dc8ccfa843986d0b4810fb359694b00051290e`  
		Last Modified: Fri, 24 Apr 2026 18:30:35 GMT  
		Size: 84.5 MB (84459862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aafee907925dbbe870efbd4c95cee231f6e6c351b8c93c053bda55a6578b402`  
		Last Modified: Fri, 24 Apr 2026 18:30:22 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd7bf6aeb2e5730a778806e4ef412b7438012d7d98b8edade956df1f21a2354`  
		Last Modified: Fri, 24 Apr 2026 18:30:22 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:79da2da682da246290a5d26abbbaa3cd34dea6e39ee17d77912655573f406ab9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7476290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f340a044f0cacc14425b1c5a610c0acf85d788ea8a0cff08cd112436ae7b1fb`

```dockerfile
```

-	Layers:
	-	`sha256:7c4014697035fbbd5ec26a2f1f701fd4bda684eb6607252f20ae3e30c63bbe3e`  
		Last Modified: Fri, 24 Apr 2026 18:30:24 GMT  
		Size: 7.5 MB (7460488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb95f6f40cf9fe59c017b42383d2cda3dcc179824bb14363db66e2451eedc6d6`  
		Last Modified: Fri, 24 Apr 2026 18:30:22 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:b9431eae760cd21e445ad838c9860cc49472178669a57e1b03d01611defd46d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.3 MB (283306870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc86ba3c65b343cb9de4ce259fcf583090c2a5cd111928e90e724fc1b416482b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 00:38:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:38:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:38:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:38:17 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:38:17 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:39:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:39:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:39:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:39:44 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:39:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:943402c24d6e7299016c00f751297dfb5fc1821547fdd1d9c56a206079784185`  
		Last Modified: Wed, 22 Apr 2026 00:17:09 GMT  
		Size: 49.4 MB (49372106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d702ada2d7e9d00abe722366b56fc0be0dcfc2ec7236668048bc2c5e0273e1d3`  
		Last Modified: Fri, 08 May 2026 00:39:07 GMT  
		Size: 147.4 MB (147388367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a6c79643ec7d88305eaf54d6f6e403e1561cadc728be09dbc1f9da850939ff`  
		Last Modified: Fri, 08 May 2026 00:40:12 GMT  
		Size: 86.5 MB (86545355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3a0b1be087b6a2998fa738b7ef97e34b5e69c52271a2518aebd801704cce28`  
		Last Modified: Fri, 08 May 2026 00:40:10 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1784cd02e52dfc45332fc3fbb28582261e5b19c4719d0c94337711d24646f1a7`  
		Last Modified: Fri, 08 May 2026 00:40:10 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:34dc4b534b84a18100f04f3d6462d1e272abe8f2aa2940a58fc42aca7e8c29c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7485030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8486c55829ffe2088b26f6c04dba14e58893346df4e134360cac6eee221a3e73`

```dockerfile
```

-	Layers:
	-	`sha256:7f2bbe11998a59afe2ab6e1aa97984c18e9477c0200bbef95d08ff8ef78cc5eb`  
		Last Modified: Fri, 08 May 2026 00:40:10 GMT  
		Size: 7.5 MB (7469122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7422b727af93599a7b78d19f692067aafbc84620a339bb541681d3abbf22568a`  
		Last Modified: Fri, 08 May 2026 00:40:10 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json
