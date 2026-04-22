## `clojure:temurin-26-tools-deps`

```console
$ docker pull clojure@sha256:2c30708f082b19bc2411aa4eb0f4adb04bebbe0db09f3676e6c9187c55f81e60
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

### `clojure:temurin-26-tools-deps` - linux; amd64

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

### `clojure:temurin-26-tools-deps` - unknown; unknown

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

### `clojure:temurin-26-tools-deps` - linux; arm64 variant v8

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

### `clojure:temurin-26-tools-deps` - unknown; unknown

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

### `clojure:temurin-26-tools-deps` - linux; ppc64le

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

### `clojure:temurin-26-tools-deps` - unknown; unknown

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

### `clojure:temurin-26-tools-deps` - linux; s390x

```console
$ docker pull clojure@sha256:917368b14661fc6892f5e11c75a98f0a630f7b7293cec8e0c4aaa9321dbc05e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.7 MB (217676595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f81fdc9eb0e7bad50f4234c965d505125b9ef4a039c649a70b3f6c5f117734c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 04:06:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 04:06:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 04:06:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 04:06:50 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 04:06:51 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 04:08:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 04:08:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 04:08:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 04:08:01 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 04:08:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:65a8acd2327b0f3316fe8707ebd5c99b15e79306d4eca71f3e635588795ae2bb`  
		Last Modified: Wed, 22 Apr 2026 00:15:31 GMT  
		Size: 47.1 MB (47147970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76be733848ad2e2341b4747388067f625f269684e93fbce48b752d101175e95b`  
		Last Modified: Wed, 22 Apr 2026 04:07:30 GMT  
		Size: 90.5 MB (90547745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf34538ddfcdc0c25f47aebc4679fce2b6167bad922c819b1f3d8c9deae3ec85`  
		Last Modified: Wed, 22 Apr 2026 04:08:28 GMT  
		Size: 80.0 MB (79979839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c34034bf197f58969b39340c663e46443d4633fd0f61a9a2a27e02dc13d7de`  
		Last Modified: Wed, 22 Apr 2026 04:08:27 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7289db19a7c6e8013bb68e62088a10667f9d17100004b7059461414a8a0b6a3`  
		Last Modified: Wed, 22 Apr 2026 04:08:26 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:49272dd4b07cee06ad5fd6ac0220a35644b94ac06dd608cd8b384588a87caa2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7337450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d23f9dc5cf296a1514cacf85ee1cbbe281ced0b3ae659f62644fd686f2d63c3a`

```dockerfile
```

-	Layers:
	-	`sha256:328555adfa2bbe6d3fede2fb7771c180fbcd2a7d937924b8a1cd631757ec498f`  
		Last Modified: Wed, 22 Apr 2026 04:08:27 GMT  
		Size: 7.3 MB (7320995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba33cecaa307dc32245f3d28a9f040782703612cecaada63abd26e13e0bfbc77`  
		Last Modified: Wed, 22 Apr 2026 04:08:26 GMT  
		Size: 16.5 KB (16455 bytes)  
		MIME: application/vnd.in-toto+json
