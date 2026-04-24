## `clojure:temurin-21-tools-deps-trixie`

```console
$ docker pull clojure@sha256:6810818e9e9838689309f05a80feeea7de1b987ee994cbd204ce2aecaa59f38c
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
$ docker pull clojure@sha256:09a21d8d19a403177c735c4050a32cdf86f26b675139da0590b73fa4bb05c9a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292730924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4dcf609af8a923fc3a1f78d68fa78bd932bc2760d2f9d82f0422bbb939e38e2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:19:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:19:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:19:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:19:50 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:19:50 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:20:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:20:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:20:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:20:06 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:20:06 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3b32e3bb7338c216b077e95920ae53332d81bd57f4a7393bc324432d5a3f88a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:56 GMT  
		Size: 49.3 MB (49302102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749ac892fcd735f7c2e252e553e8148e3b4a4b6b2c2bf149b8d33e8fe92efaee`  
		Last Modified: Wed, 22 Apr 2026 02:20:31 GMT  
		Size: 157.9 MB (157857054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa1edbc2b925b6566eb08ed75e546d8bfcf8d02bf12c16561e6680a01c39c3f`  
		Last Modified: Wed, 22 Apr 2026 02:20:29 GMT  
		Size: 85.6 MB (85570731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52d25635c3ccc35947ea7d0a4f0b030271a82fc514b163d7e1c8d53d7dcce42`  
		Last Modified: Wed, 22 Apr 2026 02:20:25 GMT  
		Size: 609.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb9a5e1f7e11b30a6685f7072acd72d01ffcfcc6b61197cab256ed77b6cb442`  
		Last Modified: Wed, 22 Apr 2026 02:20:25 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e930d1d5f94c489fd3ff36b2e95748555fb105a8e4742a860bd23235f42214e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7488327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:212a82e9e11bd6294cec0f36afef985f3cfa6adeea2221e4ca09c801eb06d4db`

```dockerfile
```

-	Layers:
	-	`sha256:fa514e99b7a0c6e51d0fa5141870ab083d3b40a30a2d7deb0aaa56165b23d349`  
		Last Modified: Wed, 22 Apr 2026 02:20:26 GMT  
		Size: 7.5 MB (7472573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20ffe026e4604e4dbb010618dda297a10fd0b10615fb32dd0a51b9ff4daa6f14`  
		Last Modified: Wed, 22 Apr 2026 02:20:25 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9966d01ad3055d4a48078e008af36fe4d2964e3fd0b90feca1869b5a73be9178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.2 MB (291186745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a71e455d4ecb594cfed9027437a6a94bf95af1afe4234571ccd475d7bfbb3f8a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:23:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:23:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:23:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:23:31 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:23:31 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:23:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:23:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:23:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:23:50 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:23:50 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6e7932d5cb5573d1bff4fb8801baad19fc72d2ae741bb046333573653944f5a5`  
		Last Modified: Wed, 22 Apr 2026 00:16:45 GMT  
		Size: 49.7 MB (49669245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b2594b313d306b3ad2ef11e5b022a8281a79dadd45b5e4d2bb93c14d42c24a`  
		Last Modified: Wed, 22 Apr 2026 02:24:15 GMT  
		Size: 156.1 MB (156133076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7470172a3521add5555a7f2e19b0911f4e6e652c9aad7e478a408f54cd24b869`  
		Last Modified: Wed, 22 Apr 2026 02:24:14 GMT  
		Size: 85.4 MB (85383383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54a9aa328396d8df45e63e74b7f7469cb78e208b3c4803c96b817afc77fbef3`  
		Last Modified: Wed, 22 Apr 2026 02:24:11 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ca8c6da05d56adaf709e409a722a32fd6d45aab32caf316a11fff9deb8d206`  
		Last Modified: Wed, 22 Apr 2026 02:24:11 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a41c04b32c01566deca905cb8f449a59eafab3a639e700a40565b85b9e163117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7495475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48b9ac2530bb83a3728ffc6b8e0445342e7e272bb01e53cf8e60cf2051ccc54b`

```dockerfile
```

-	Layers:
	-	`sha256:c763fcd5114f16fa06b1659fbbe5c1c421e73adcec09267f2ce71042587129af`  
		Last Modified: Wed, 22 Apr 2026 02:24:11 GMT  
		Size: 7.5 MB (7479603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1e25cfe7811ca762a7d3a63f75b84f1a0c03142eb68ea974b0f284d4ac95aea`  
		Last Modified: Wed, 22 Apr 2026 02:24:11 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:8a076f27b06ebc7c1546919c41e2de066336658c48dd85ba3c1a75b7b65a787b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.1 MB (302087854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3aea2113b7e73f6057b80022a946a20e86eb03fec511430d3fcc425b99c822`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 08:39:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 08:39:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 08:39:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 08:39:30 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 08:39:30 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 08:43:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 08:43:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 08:43:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 08:43:55 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 08:43:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0fab4f6170940889900b2327e1b3c62dace993eab8074ca7d33d1ffeef137c08`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 53.1 MB (53122984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dfd4a596860411869ba1b27f063b5f93a5f8477634fb7f87b5eea1fe9858af2`  
		Last Modified: Wed, 22 Apr 2026 08:41:02 GMT  
		Size: 158.0 MB (157977486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475e9f3be26e1181e8a4583bd1bcca4efd24f2f84fc3fe1d5145183333f56dba`  
		Last Modified: Wed, 22 Apr 2026 08:44:38 GMT  
		Size: 91.0 MB (90986344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a160a8a5fcf2e9c148d82f3d8c1a0164cda0aab0b4760712ca8b886781495f7`  
		Last Modified: Wed, 22 Apr 2026 08:44:35 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c33d320fbc9e5ba8cc07bdd9c88f38b62d6fe20d4b49b120cfe04453a0675c`  
		Last Modified: Wed, 22 Apr 2026 08:44:35 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9e1cbc104615e30da1638557f2a840a880ae09abd7663e64ad484c9e31236e8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7492796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:600a7103fec5579e8224acea5d808949809a4032252aae074fb086cc719963e3`

```dockerfile
```

-	Layers:
	-	`sha256:0d34353b6f483a21512984472633e8bf17f85f72a13946674ccad016c4f60ab0`  
		Last Modified: Wed, 22 Apr 2026 08:44:36 GMT  
		Size: 7.5 MB (7476994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1f0a98b1e399b59a5fa9e193c38c2a89e365f46385770ac8d374e49123ad480`  
		Last Modified: Wed, 22 Apr 2026 08:44:35 GMT  
		Size: 15.8 KB (15802 bytes)  
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
$ docker pull clojure@sha256:af763a523e13486c9f1622989f05dc6b884a6aa22c4e1ec4818d0eb5320209c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.0 MB (283023392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d2ff871b78f1a5c677d5847996380e43aff685dfbef5548a42cb79fe76db80e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 04:03:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 04:03:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 04:03:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 04:03:12 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 04:03:12 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 04:04:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 04:04:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 04:04:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 04:04:30 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 04:04:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:943402c24d6e7299016c00f751297dfb5fc1821547fdd1d9c56a206079784185`  
		Last Modified: Wed, 22 Apr 2026 00:17:09 GMT  
		Size: 49.4 MB (49372106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60cdd84aff24f59863daaed198419b0074a2a76183e68980d9cedc370030291a`  
		Last Modified: Wed, 22 Apr 2026 04:03:54 GMT  
		Size: 147.1 MB (147105212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe6b92bd2e9abef5d9e28ab9dcf1821d33eca057cee3ea6cdea475fec82bb3b`  
		Last Modified: Wed, 22 Apr 2026 04:05:02 GMT  
		Size: 86.5 MB (86545033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ad677bae19aa35b2c03531d0e7781838e0fe0a52a68ef8e55a241adedb20e9`  
		Last Modified: Wed, 22 Apr 2026 04:04:56 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56171ac7de425ce14089e3f3da0c83a3b7bcfe1919ceeb2fd81074543d86d907`  
		Last Modified: Wed, 22 Apr 2026 04:04:56 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:fe6ed8757d8c334e827eb9c39c5d6e7f7e5ce3f17423793b786898ed4c1a1a8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7484248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1bdd5ca69b83be9d7e56b65dcb27314445072c5415fb519075372b3f4ee72b7`

```dockerfile
```

-	Layers:
	-	`sha256:c3c5616689fb48df60651d5230294fe485665fc6afd025870b0b93b5a4f01d69`  
		Last Modified: Wed, 22 Apr 2026 04:04:56 GMT  
		Size: 7.5 MB (7468495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7da53ddeeac82044b8acd19d32c59da38e64013b132638481b120f866a769ceb`  
		Last Modified: Wed, 22 Apr 2026 04:04:56 GMT  
		Size: 15.8 KB (15753 bytes)  
		MIME: application/vnd.in-toto+json
