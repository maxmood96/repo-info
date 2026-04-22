## `clojure:temurin-21-trixie-slim`

```console
$ docker pull clojure@sha256:b4471e7b94185b07b140f657d5b62dad7abadc52b03a39f7bfb907cd0637a267
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

### `clojure:temurin-21-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e6befe1e911977b1637d0fb7ecff49534e5365484767c723a79fadf52cbcd6e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.6 MB (259649458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a50f57ac9fb0d3c9b182dab30f21cf96bd16630deba671b5dc9db1e11c59b9a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:20:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:20:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:20:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:20:13 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:20:13 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:20:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:20:31 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:20:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:20:31 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:20:31 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634d32ef46359a2820b42edb940524f5b6e3301f5ca4cc8814968d0c3ebf69c0`  
		Last Modified: Wed, 22 Apr 2026 02:20:56 GMT  
		Size: 157.9 MB (157857104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1239f370a763bb06e37331b4977eb923a16293523b926b4f07852968a76b5ee3`  
		Last Modified: Wed, 22 Apr 2026 02:20:54 GMT  
		Size: 72.0 MB (72011143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2cae559337016ef20c943eb5e79d24b7fa9b93b70051b4fd656de3071b0c8a5`  
		Last Modified: Wed, 22 Apr 2026 02:20:50 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c19bb7fbd5095a7a7f7e6ca78321feabb6f045b7c43a95eee26dfb0cca40d3`  
		Last Modified: Wed, 22 Apr 2026 02:20:50 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8b7b55b3becd2a92655813b3f6525ae93154e05899f62d38ca635cb1d392686b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5276856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f8413f6b685301bfab06533f5ead8ab30837a1f536d19537101f9e2404a5be4`

```dockerfile
```

-	Layers:
	-	`sha256:1cb9afdd0251fffa64e1d97fb01e44ced8e33390828f7c1a375f43469ca0c82d`  
		Last Modified: Wed, 22 Apr 2026 02:20:50 GMT  
		Size: 5.3 MB (5261044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3492b97d2ca00d2f3a4b4f36725ca85a76da92ceef859a75333e189b6ad6f691`  
		Last Modified: Wed, 22 Apr 2026 02:20:50 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4af2ff2e5de825350af921d06af09cb432a390fbeaaeae1e8bc68ae5e079c33a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258108300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16af40d6110125623018ae8f73f32be910230abe360f5d1b82a903708fff88d9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:46:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 01:46:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 01:46:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 01:46:21 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:23:14 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:23:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:23:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:23:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:23:32 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:23:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe9f0ef3f19e27b73c25387a916edb54921830265a7aad870e43390ffa99f76`  
		Last Modified: Wed, 22 Apr 2026 01:47:27 GMT  
		Size: 156.1 MB (156133067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56424479d36d58b87c8df709c51d19e8739a67381ef79cee6e81a8933d068ae0`  
		Last Modified: Wed, 22 Apr 2026 02:23:49 GMT  
		Size: 71.8 MB (71830589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7791b0427a2118e38fec49ec9bf602a40e5141eb188e4f18208d4705ebf311da`  
		Last Modified: Wed, 22 Apr 2026 02:23:47 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e36c55bea7103efc5d01f3684759147015761c79296e6ab5ae1bd8910e57f80`  
		Last Modified: Wed, 22 Apr 2026 02:23:47 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:75150e4eb79ac17c2907b3488a5cbe1b9aafc42e8e03c0aeb5e49ea91235f89d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5282743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec710d5e851fe4fa50d073178465af4a2384d419f32384f44127fac1be687a3b`

```dockerfile
```

-	Layers:
	-	`sha256:d885e8108db92156321f983b3ff5061654f4dd92a2da3fc4eda7578e6dc2bf30`  
		Last Modified: Wed, 22 Apr 2026 02:23:47 GMT  
		Size: 5.3 MB (5266813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:867c1150de788346c4bd25f602582a002a0f68d5865964f01e2ab1851bca9cad`  
		Last Modified: Wed, 22 Apr 2026 02:23:47 GMT  
		Size: 15.9 KB (15930 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:954b6c79db8971a394446f419274abbd0bd43a8ee2501537b505316e037e7a33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272181831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:648a5c19f6c3edb7ba28ffca9598335cb70523c8e35b52035ee1b7dc21700d05`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Thu, 16 Apr 2026 03:01:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 03:01:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 03:01:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 03:01:40 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 03:01:40 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 03:07:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 03:07:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 03:07:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 03:07:33 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 03:07:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6266996408f18fa5b8afefdb178402a7bc9517ccfdc1fdefe8e27ee9d954dade`  
		Last Modified: Thu, 16 Apr 2026 03:03:20 GMT  
		Size: 158.0 MB (157977492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0712d593bb6889f8e865a5a3a81735a6b0b3ec22fead7c52236f76cdadcc1af`  
		Last Modified: Thu, 16 Apr 2026 03:08:13 GMT  
		Size: 80.6 MB (80610282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef32de035f25055c3f14c2fb2855e55630004c7edbb443c1a8389e33260da5ab`  
		Last Modified: Thu, 16 Apr 2026 03:08:11 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34cc34b85539e026ded921876144b7c9d83917b58b4d56cb2c22accf915ad068`  
		Last Modified: Thu, 16 Apr 2026 03:08:11 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:83cb8a7cd1a34b463e7ff424082d8b3cd9fe19ec0f524eeda1a6e2c52c72b644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa49fed52e658207712d28330206baceace9e70f96b6c6ce59dcef044d2114e`

```dockerfile
```

-	Layers:
	-	`sha256:3736b4a7efdeba30b0eaa9b04c8493f0bdea5162d0666c47b4a2b62ca0d1085e`  
		Last Modified: Thu, 16 Apr 2026 03:08:12 GMT  
		Size: 5.3 MB (5265361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93c754517d3dc2d8e3b0e608dfb085d8a5f4b6b27e4f382727a5dde87356d98f`  
		Last Modified: Thu, 16 Apr 2026 03:08:11 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:9aaa235811d943460147dff0fddc9a3a60f4413851950d721debbf98740130b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.0 MB (259012426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c85c05788176c5b267ca86c4987f8fd4c7e679966091aabea86ea8ea61d919`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Sat, 11 Apr 2026 22:00:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 11 Apr 2026 22:00:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 11 Apr 2026 22:00:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Apr 2026 22:00:57 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Sat, 18 Apr 2026 04:49:20 GMT
WORKDIR /tmp
# Sat, 18 Apr 2026 05:11:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 18 Apr 2026 05:11:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 18 Apr 2026 05:11:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 18 Apr 2026 05:11:38 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 18 Apr 2026 05:11:38 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5427f8f7357cd1c2f90f35451416b331ea3c682f95a93bd8689b142ddc99805`  
		Last Modified: Sat, 11 Apr 2026 22:07:07 GMT  
		Size: 157.2 MB (157216895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcd9e65888bdd1763a340eae3ac6cae1421f830ecdd9a6291a969293a322dc1f`  
		Last Modified: Sat, 18 Apr 2026 05:15:29 GMT  
		Size: 73.5 MB (73518706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f097ec60300d12b67429b5cf2d0d9b3ab4c27f3c70b6d4905b444d708f82f9d`  
		Last Modified: Sat, 18 Apr 2026 05:15:16 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a77067a97433f03846e8e0196bddc16e5c6cdc6f86a336732438ca3ace731dc`  
		Last Modified: Sat, 18 Apr 2026 05:15:16 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fcedf84ffd77afb380968c9aa27b977b93e5b1a013dc1275bb55d428fc147036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5266314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83713c3c625ede87fd84c21ebd9bb6bc8af295a1337bc9a80e97aafeec7b4b73`

```dockerfile
```

-	Layers:
	-	`sha256:abdafee2cf231bbed3b9ef8bc59479903e8f8e5406cfb02e0f0e12e95e57f1c6`  
		Last Modified: Sat, 18 Apr 2026 05:15:17 GMT  
		Size: 5.3 MB (5250454 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:059614943fe787b967406e7b1c24bfd6f7df571922b7c29932a26b474d0dd622`  
		Last Modified: Sat, 18 Apr 2026 05:15:16 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:52ba36cc5236fcfbe8df82c2ae03d5d5fda78a802416f3957622ba9738608021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.5 MB (252540260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:723ddd7f0c592425a484cf00a1a608cef767ff723d8928cc4061274752cb3f9c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Thu, 16 Apr 2026 00:41:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 00:41:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 00:41:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 00:41:51 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 00:41:51 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 00:43:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 00:43:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 00:43:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 00:43:19 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 00:43:19 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dcda4ee8bd621aac2ef8027b80495558658cc850eca58d63e93743bca8b01b4`  
		Last Modified: Thu, 16 Apr 2026 00:42:33 GMT  
		Size: 147.1 MB (147105251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07e97b5ac60e80fa6914b0b0d53fa4d2e8eea4eebac818afe7e383010306e40`  
		Last Modified: Thu, 16 Apr 2026 00:43:43 GMT  
		Size: 75.6 MB (75598549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a928ecfbb6d351d813a5b226036f14229d0424ead99ebb83a83070aa404b55`  
		Last Modified: Thu, 16 Apr 2026 00:43:41 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57078e2cab2d2894567179d961edacc2fbdbaeb24095cb2b7cffaeb1d3094b83`  
		Last Modified: Thu, 16 Apr 2026 00:43:41 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:01cb671e4d7870de262c0cd35347cd0c8629c08dc927b50ddf922267d6899d6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c5f393c75511586cc925b84a3e1785a8d673fd6f3b33ea0041d8c2c8ebc77f`

```dockerfile
```

-	Layers:
	-	`sha256:122844a4fa6911d9e102a96e4216bc8b4fea900dab43859a2b660a836654ea13`  
		Last Modified: Thu, 16 Apr 2026 00:43:41 GMT  
		Size: 5.3 MB (5256914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cd3fec23fafb919d2372e0ecb10e9f2efeb1563d9f7c386742b46d7354bbca2`  
		Last Modified: Thu, 16 Apr 2026 00:43:41 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json
