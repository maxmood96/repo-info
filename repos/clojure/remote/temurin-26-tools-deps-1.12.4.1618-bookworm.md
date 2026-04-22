## `clojure:temurin-26-tools-deps-1.12.4.1618-bookworm`

```console
$ docker pull clojure@sha256:05ae30bc3de57ec4534ff27c983faf772a5b715663b70210825f2ed52da4d385
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

### `clojure:temurin-26-tools-deps-1.12.4.1618-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:20e1d0b2e7497512edf636a9cdc3099382899646df9e63462795dd2a05d7f1ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224111688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77f2f03f56157d9ec04afa7ee83dc0f907089292857cd505d6c4792f4ecb9894`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:22:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:22:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:22:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:22:05 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:22:05 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:22:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:22:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:22:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:22:21 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:22:21 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da5d16c7a69753a8ccaa736be0dfa9e565c09ac5347ddfafd462699a4dcc4853`  
		Last Modified: Wed, 22 Apr 2026 02:22:44 GMT  
		Size: 94.5 MB (94455691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b962789dea89f71ab3e8926784c1246a0195c9715ed574acae8e883c1549b59f`  
		Last Modified: Wed, 22 Apr 2026 02:22:44 GMT  
		Size: 81.2 MB (81166328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b823733f03ca0daa89f8aee8221889493b2f360804bbef943d2f78a5411489`  
		Last Modified: Wed, 22 Apr 2026 02:22:40 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd71ee921cbcfeb2a8510fc4742ac9fc55c37ce1e7aa6bfca1bb647625359e74`  
		Last Modified: Wed, 22 Apr 2026 02:22:40 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:ea3d87c8acace8f588a0700cbc8d6048e20560ac50cdd981c43e362a67e827b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7360944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:978248873e91883ff0db321caa1924854413e941efdd1b363597185aa7ba06cf`

```dockerfile
```

-	Layers:
	-	`sha256:d96b1227b300243f794cdd02443ca7a86f39b6fcc5d94d8437899172278d762e`  
		Last Modified: Wed, 22 Apr 2026 02:22:41 GMT  
		Size: 7.3 MB (7344490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41a53e9b9a344e363dc737fe2ccc367da201d0ec4d46f5850924108043a4326e`  
		Last Modified: Wed, 22 Apr 2026 02:22:40 GMT  
		Size: 16.5 KB (16454 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.4.1618-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8bb94d50f040f5dcc6a0739593def00182b2e1b1d45830fb42b01b5821d662da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222943601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67df8467e6ab373eb1d4b9eff0ff33f5d08b473e66d6bcfc17eb03078d657bf3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:24:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:24:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:24:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:24:51 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:24:51 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:25:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:25:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:25:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:25:06 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:25:06 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578e0414abd78da67e86c1dbbbc95a93ca711cfb765d4ffcd00575ce258835a3`  
		Last Modified: Wed, 22 Apr 2026 02:25:29 GMT  
		Size: 93.4 MB (93395167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfe3d13d90569971655baaee8b9f436545a96ce37f8ad92768380204c7bf417`  
		Last Modified: Wed, 22 Apr 2026 02:25:28 GMT  
		Size: 81.2 MB (81174324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b40f281fdcbd456e5e149269b1412743a2786ca953a8b8b9e77c28da333d01`  
		Last Modified: Wed, 22 Apr 2026 02:25:25 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20e698d9a87411979deef426f312eb72513ed46289009cc201954aa10f57b6a`  
		Last Modified: Wed, 22 Apr 2026 02:25:25 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:9a13a10f89f78f9e2b7e403c1fdc6475e6030a24c6e3b89db3089a7698578edb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7366871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:180500580f02ca1fc9d23cd1f0da3ce51446568d9ccf2a4d6dcf458af77298ff`

```dockerfile
```

-	Layers:
	-	`sha256:5e5caf50a2aec9ba52206b9fbcc92b2c227821e3d4a62d73483db3ca526c3682`  
		Last Modified: Wed, 22 Apr 2026 02:25:25 GMT  
		Size: 7.4 MB (7350274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:153ddeb6425c2f1fafbe0604d148eeb3da93850657c0f95f398259b1cd19fdf2`  
		Last Modified: Wed, 22 Apr 2026 02:25:25 GMT  
		Size: 16.6 KB (16597 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.4.1618-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:4a9ce04e37617329c2b64dd562cc2f295687198d4f1172842f4b8fe726713c2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.1 MB (233123727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b904029ce4dfbba361ed22260def671de07f86ed7fdfe6353d47ddd74c9b2da`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Fri, 10 Apr 2026 00:49:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 10 Apr 2026 00:49:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 10 Apr 2026 00:49:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Apr 2026 00:49:05 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 10 Apr 2026 00:49:05 GMT
WORKDIR /tmp
# Fri, 10 Apr 2026 00:55:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 10 Apr 2026 00:55:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 10 Apr 2026 00:55:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 10 Apr 2026 00:55:25 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 10 Apr 2026 00:55:25 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6b775f7ad22043f8bb75d535d8a1279e43453a08a4a9e6a0b48c020c9b387079`  
		Last Modified: Tue, 07 Apr 2026 00:09:43 GMT  
		Size: 52.3 MB (52336938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5bb937b64e28b9440675ccbc228210a99b8d8484e299953df825953180b5f5`  
		Last Modified: Fri, 10 Apr 2026 00:50:20 GMT  
		Size: 93.8 MB (93781433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e06babe786768a3af7a08ac0e27c2469d113f91699dbc54d7741bebe5a79673`  
		Last Modified: Fri, 10 Apr 2026 00:56:00 GMT  
		Size: 87.0 MB (87004316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be5a1566efa6e60946982469ea2eb76c5b58c21a14f7e95b23a5616cfcc9b2c`  
		Last Modified: Fri, 10 Apr 2026 00:55:58 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c9fee73bbbbcb7161f58ca4ec903f171cba7e44036a6b3de4ef9215ce50c7a`  
		Last Modified: Fri, 10 Apr 2026 00:55:58 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:63f9512fcbc7162bad635b41bff289dd26ea602d7d179eab48a56595cecad686
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7350169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3cb9b848f1ebc4860cddce5f91ddec3a5e44790eaa94fe998d294185cef81e6`

```dockerfile
```

-	Layers:
	-	`sha256:028560077e9643b18032ee075f0512672020deb5ecf2c6bb90ca70ceb3b8de5f`  
		Last Modified: Thu, 16 Apr 2026 03:17:03 GMT  
		Size: 7.3 MB (7333654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb0eedcf349d2b3870b492fa8b7230f93da2a7099dc8eb83db9c4b774645c2ff`  
		Last Modified: Thu, 16 Apr 2026 03:17:02 GMT  
		Size: 16.5 KB (16515 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.4.1618-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:e4014008d168d526f699e2b4989bace929f789b2b4769acbabe5ced384417a50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.7 MB (217676677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2d9e9a04dee0f685a14ba9eedda33b6d566f03f144131c7abadd80f957c7e38`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Thu, 09 Apr 2026 23:43:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 09 Apr 2026 23:43:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 09 Apr 2026 23:43:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Apr 2026 23:43:20 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 09 Apr 2026 23:43:20 GMT
WORKDIR /tmp
# Thu, 09 Apr 2026 23:44:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 09 Apr 2026 23:44:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 09 Apr 2026 23:44:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 09 Apr 2026 23:44:44 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 09 Apr 2026 23:44:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:40ecbf1d4e17f6b072e6cef463823baec601d9f21c9dc33d98bd258448a986f6`  
		Last Modified: Tue, 07 Apr 2026 00:10:32 GMT  
		Size: 47.1 MB (47148084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4374cefdbacee456d8ed008c1f311f90f13f2b652def32ee01d354d19f349fd7`  
		Last Modified: Thu, 09 Apr 2026 23:44:03 GMT  
		Size: 90.5 MB (90547745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d981499af759fb6d244f56ea5e147e3b2e3e15371b11dee2bd300ce537ad52cb`  
		Last Modified: Thu, 09 Apr 2026 23:45:10 GMT  
		Size: 80.0 MB (79979806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9cfdff2b0b84521d4b4545bbe101ebe383c71f1c2c08c7e563de371fd995d7`  
		Last Modified: Thu, 09 Apr 2026 23:45:08 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dac0378a9a0ea19e94977f155843cb1157dbb1f887c6fd4332e0f9cce3687db`  
		Last Modified: Thu, 09 Apr 2026 23:45:08 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:99bc63e6209225314e075630ba3fd132071bb68847569552099e709f939182d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7337450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0c50a9fa44b724a9441b415f615fd041e72b9a5ed0c4568a4d18840b8ea9989`

```dockerfile
```

-	Layers:
	-	`sha256:4085187a567935d84142ee5107ebb6d1d34deeb47a826dd1696fa7f10b52b7ed`  
		Last Modified: Thu, 16 Apr 2026 00:47:05 GMT  
		Size: 7.3 MB (7320995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93cb105eb95d902c0f72e5da5f66fd3b00d61c2a37b35d22fdf1ed7712761d0e`  
		Last Modified: Thu, 16 Apr 2026 00:47:05 GMT  
		Size: 16.5 KB (16455 bytes)  
		MIME: application/vnd.in-toto+json
