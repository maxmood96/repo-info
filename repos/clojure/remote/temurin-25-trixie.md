## `clojure:temurin-25-trixie`

```console
$ docker pull clojure@sha256:6cf93651ae25f42abb468ef072ad30081a90f984d3c1e8638ffaf8e60e05117b
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

### `clojure:temurin-25-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:9f0ea277aaf19c1c7ef4971b8ece70ea408434f5cf8092108de622b8203e9432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.9 MB (226877433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcc46edf70c83d0621351b7ea198a633fb7c612c6d21fb7e772a2b6964fb8c1e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:57:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:57:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:57:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:57:06 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 23:57:06 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:57:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 08 Dec 2025 23:57:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 08 Dec 2025 23:57:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 08 Dec 2025 23:57:24 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 08 Dec 2025 23:57:24 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2981f7e8980b9f4b6605026e1c5f99b4971ebba15f626e46904554de09f324f4`  
		Last Modified: Mon, 08 Dec 2025 22:17:46 GMT  
		Size: 49.3 MB (49289520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe126571d40ed322316926b03e8ad562cd1e2e29cd15b97222521f639ad2d29`  
		Last Modified: Mon, 08 Dec 2025 23:58:14 GMT  
		Size: 92.0 MB (92045322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7cb8f1931f2e4ca614ca1dddbbb4884e75a490fdd7ed42e4ebdb6ec639842e6`  
		Last Modified: Mon, 08 Dec 2025 23:57:58 GMT  
		Size: 85.5 MB (85541555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbbaa605905d056c8ae6774509576fd417bc0961bd9fde80e2ab1cc0141f5a5e`  
		Last Modified: Mon, 08 Dec 2025 23:57:53 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e570bb8cffe4722fe3b2941516f03e91fee1282a3d20087ed3c4a1f5ef61f1b1`  
		Last Modified: Mon, 08 Dec 2025 23:57:53 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:06c2037e1e3e7eae4df213b2c00457da5d909a67b5e6117da924d53a3c282b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7434676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a2ee0dcd887b1a5758328fae56bfba6a4dceaa7241fc339db1131cb4f585e3`

```dockerfile
```

-	Layers:
	-	`sha256:121fc37c4030d9dee0c3b2b4704aa3639b3d4e3124250bd9161efa24f202a4d9`  
		Last Modified: Tue, 09 Dec 2025 04:47:04 GMT  
		Size: 7.4 MB (7418261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cf035c658e9bd22dfb6094bbd6965bc16e4b758e3709fc3d5cab0057e101afa`  
		Last Modified: Tue, 09 Dec 2025 04:47:05 GMT  
		Size: 16.4 KB (16415 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e3fd1a2f54c0ae746712600ff2eff73d431743a55d40d47250c061e5dfdc1570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.1 MB (226067793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:557f4b502d4807132003d52b7d67add5b7b7a55e8289b874199c03890f5ea3ee`
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
# Tue, 09 Dec 2025 00:04:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 09 Dec 2025 00:04:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 09 Dec 2025 00:04:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 00:04:07 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 00:04:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a828f739420ec96bad6123094a07f3f234998f6cf772e34e0ba733aa8e2b347`  
		Last Modified: Mon, 08 Dec 2025 22:17:28 GMT  
		Size: 49.7 MB (49650226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0484d70ffed598abb52c462601340a8f43566d8f73587569a852c07032a8dd`  
		Last Modified: Tue, 09 Dec 2025 00:04:52 GMT  
		Size: 91.1 MB (91052515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c6bb5871719743393cfd7087896107c2404aa193421174f43028766f43fb71`  
		Last Modified: Tue, 09 Dec 2025 00:04:47 GMT  
		Size: 85.4 MB (85364016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c826fee79c2590d2bd87b51c1c152ca9f7a6ad956d88180831b8c8c0c36a6fe`  
		Last Modified: Tue, 09 Dec 2025 00:04:40 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed807c47fa49e2581039e787b232e3ca474d878267084b1233f3ed675e8953d`  
		Last Modified: Tue, 09 Dec 2025 00:04:40 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9c240fb69c755c9f1af7c312b201481fd563b038e65ac75a21b2395b19b1487c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7441869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08624e0ada1fdcef624c0305608666b62107a6195ebe92050b7e8aa8d3c07d80`

```dockerfile
```

-	Layers:
	-	`sha256:dc57c0396d8b87512655e8434860fe9ee98e543395b732216558f15aa63d39d5`  
		Last Modified: Tue, 09 Dec 2025 04:47:11 GMT  
		Size: 7.4 MB (7425312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:faa7979324b1c77839e75cfe94ced0d5374f45cd9a3a561c093cc25f99ee1afc`  
		Last Modified: Tue, 09 Dec 2025 04:47:12 GMT  
		Size: 16.6 KB (16557 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:1aaee8e644bdc625090169e54542fcc359690d83d9552b125dde169d6c374f9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.7 MB (235667560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb49c32e847ca01f77c92d32044239df167f78b5929cf258442ec81bc9f060b9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:32:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:32:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:32:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:32:22 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 23:32:23 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:33:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 08 Dec 2025 23:33:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 08 Dec 2025 23:33:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 08 Dec 2025 23:33:07 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 08 Dec 2025 23:33:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fb00391cdf4b5dc5fe2e67e0bee3770076e9af9efed48ba15cb306902e36c78c`  
		Last Modified: Mon, 08 Dec 2025 22:52:23 GMT  
		Size: 53.1 MB (53108478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe3513d576a2d4d2badd58f02126058233abf53aea816262c3b7f313a199d32`  
		Last Modified: Mon, 08 Dec 2025 23:34:05 GMT  
		Size: 91.6 MB (91610745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8f7f7014b8628d452646705dc66cfca5c27adfcba51d33a5802deb4504b06b`  
		Last Modified: Mon, 08 Dec 2025 23:34:08 GMT  
		Size: 90.9 MB (90947295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fff1a0df68dd43f2f4e9d139e9f0cc616c435787b0363769add18f9e1aa4e73`  
		Last Modified: Mon, 08 Dec 2025 23:33:56 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bd2b3fb620a878d7e397b491ec71f97d6cb947fde740b515767c79b056a96b`  
		Last Modified: Mon, 08 Dec 2025 23:33:56 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f5066b6ddb5f6898aad8e6597dd13acb82215319da9072d4e7807852ebab2d6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7440465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1df68aed388ccc77c094c4180135ebc8a4484c6b7f1058e6994f033f9c99b00f`

```dockerfile
```

-	Layers:
	-	`sha256:396d0b626bdf3f4c91cc3d94242d58cf37b9a10921d993a56dbaea8046696857`  
		Last Modified: Tue, 09 Dec 2025 01:39:34 GMT  
		Size: 7.4 MB (7423990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73c3b83a6bbecc6344f435207ae6010bdd397f33c7269ae809654faad35e2f83`  
		Last Modified: Tue, 09 Dec 2025 01:39:35 GMT  
		Size: 16.5 KB (16475 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:95373b1751fa6df9cc8c5c3d811d2340462011cff62d780ba74001f7104a2c58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (222951802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e28c36a8b3014591b5b2a5c1ef73d986034065812f09ba38b057b8126ebc3add`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Thu, 20 Nov 2025 18:48:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 20 Nov 2025 18:48:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 20 Nov 2025 18:48:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 20 Nov 2025 18:48:04 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Thu, 20 Nov 2025 18:48:04 GMT
WORKDIR /tmp
# Thu, 20 Nov 2025 19:02:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 20 Nov 2025 19:02:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 20 Nov 2025 19:02:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 20 Nov 2025 19:02:26 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 20 Nov 2025 19:02:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ed0507b92b5f6d1bbf086936336ca6e85b2d0afbbaab333064cc752190ce52b9`  
		Last Modified: Tue, 18 Nov 2025 01:45:17 GMT  
		Size: 47.8 MB (47771195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82da52be06de4ed4999d84e1a9d7d08b95b3d6f3efeae3a90908819ba167244`  
		Last Modified: Thu, 20 Nov 2025 18:54:07 GMT  
		Size: 90.8 MB (90752860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d96c70020c6aa81739134652887b2145444376e667c11fc82664345551ff81`  
		Last Modified: Thu, 20 Nov 2025 19:07:05 GMT  
		Size: 84.4 MB (84426704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aef4b5f7446ed29d2e9fda0674fc7bc52e1d0b3ff910603fcccf362ebce36d8`  
		Last Modified: Thu, 20 Nov 2025 19:06:51 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c31909422f581587106903a38bf443decdd9cebcc98f7f694eaffcbaa8316c6`  
		Last Modified: Thu, 20 Nov 2025 19:06:51 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:379c85f0a41d7336bd4e08e7807b5fe404a446e577ba2ed1f5955369370727bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7422658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d6992f64947961d74feb6d6c69372c2e4d1bb3db0e87d3002ff6a458c5f66cd`

```dockerfile
```

-	Layers:
	-	`sha256:460a0fe54f4bda90344f8f6324d13c9c979feb1274bce9cba722f21cfb291fdf`  
		Last Modified: Thu, 20 Nov 2025 19:38:24 GMT  
		Size: 7.4 MB (7406183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:160a0fe166c8a23ca505fce98860fdc430103e5113655e3eea9e5b463009b6e8`  
		Last Modified: Thu, 20 Nov 2025 19:38:26 GMT  
		Size: 16.5 KB (16475 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:cfccac2309bf7551fefe495ec0c6c51c0d329fc0ac031c7bd378452a22889425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224068972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd93841e355e9e3d29844560e2b287d9ab664e0e0471bf13539eb184e79ec012`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 01:33:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 01:33:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 01:33:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 01:33:33 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 09 Dec 2025 01:33:33 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 01:34:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 09 Dec 2025 01:34:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 09 Dec 2025 01:34:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 01:34:57 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 01:34:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3f8967bef2f6a8ec916f7d3a0d528a6724093176621c5758addeeece50e41dec`  
		Last Modified: Mon, 08 Dec 2025 22:16:15 GMT  
		Size: 49.3 MB (49345908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561af1fd1f572f4dbfb628c0a027acc23b1d8a0d6465efff545b43e36426f3e6`  
		Last Modified: Tue, 09 Dec 2025 01:34:33 GMT  
		Size: 88.2 MB (88210717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0952b4e881ec89fe6766b81a95921214473b7e0d31c1dd2d39a4b3084c179d4f`  
		Last Modified: Tue, 09 Dec 2025 01:35:46 GMT  
		Size: 86.5 MB (86511307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea4e31491f28bbf52d7d5a06bc0a75c32f60eb5d25429e7a4f9a288d6402a58`  
		Last Modified: Tue, 09 Dec 2025 01:35:31 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76888696a70eef1d0a2f2d0882caba2d93dd8993e02a7909c4a095b370147f7`  
		Last Modified: Tue, 09 Dec 2025 01:35:31 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:bfd93910b94f5b1ca5c66bd68952378ff77fa0991da8a928ca051515c8677e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7433146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13d20a9c4ac87c6d263c4805d4a4b19ecb3036fcf8ecd8b08b928ab976a9ae89`

```dockerfile
```

-	Layers:
	-	`sha256:a6416c4471f589797e6d31d3484ed2c3034a57d72268f710c33d45488655afff`  
		Last Modified: Tue, 09 Dec 2025 04:47:29 GMT  
		Size: 7.4 MB (7416731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:462920b516000ce4eef2f1b466825dc4948ca3639d03792ea88b3144aab3e6f0`  
		Last Modified: Tue, 09 Dec 2025 04:47:30 GMT  
		Size: 16.4 KB (16415 bytes)  
		MIME: application/vnd.in-toto+json
