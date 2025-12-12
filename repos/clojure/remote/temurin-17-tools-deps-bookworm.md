## `clojure:temurin-17-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:18c3cd351f451b5678e2a619139d73899b4db93b03747637a07c116e461c9de0
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

### `clojure:temurin-17-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:f8760edb63de6c81269b0fc4dcdd32d6ea8f425215f6f0185b2e1c0ad3ed2163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.5 MB (274476607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a9951e5998b8c2efbb587dc3cc61855c75449437abfd4f682679ca61d309c4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Thu, 11 Dec 2025 22:39:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:39:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:39:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:39:14 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:39:14 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:39:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:39:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:39:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:39:28 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:39:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf99dd5b49730220b0fb715ee5a6e6b5c85f10e6d95eb6d8d7443e5cc7d929e`  
		Last Modified: Thu, 11 Dec 2025 22:40:13 GMT  
		Size: 144.8 MB (144847922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fc610dbf51b23f994104582a3f1018cbe1ed6fbe8ab1ff27bb93c1424cc3cd`  
		Last Modified: Thu, 11 Dec 2025 22:40:04 GMT  
		Size: 81.1 MB (81146914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f6a7c5a07e42103ccb3fe573e0d46a628b371e1be42e86db9d2cdd24609bf8`  
		Last Modified: Thu, 11 Dec 2025 22:39:57 GMT  
		Size: 609.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4072055d799b564e32280527f5b6a29119bbfea916d3e106e7f1421fc07db4c`  
		Last Modified: Thu, 11 Dec 2025 22:39:57 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:6afabdf20b573d6bd5c918b49169e150191225d747cf8d5d9a70e0689c12b869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7390670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:243cfe8b9498c38ebd7f80daf2d1207663f1c9bbd7b9d10db80972a6fc7a44b8`

```dockerfile
```

-	Layers:
	-	`sha256:6500182e8c326c71cbac2d3100441d73aba89af6372eebb86dc246aaef1c036c`  
		Last Modified: Fri, 12 Dec 2025 01:37:43 GMT  
		Size: 7.4 MB (7374892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd9d3dfd09dd917c144d7b88e278e6053a827c9d3a2583f6969284ebe651b2c6`  
		Last Modified: Fri, 12 Dec 2025 01:37:43 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f0e44691ec24b9c7e2932922ded87679eaf669ff996f17e2cb2df7d9ee7bd743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.1 MB (273066015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dbca786ca0995716b287cafdb129f6ab5d5c01cc16dff3d25eb0f349703ce49`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Thu, 11 Dec 2025 22:39:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:39:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:39:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:39:13 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:39:13 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:39:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:39:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:39:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:39:28 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:39:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7f2b9668af76f73927725e2d1fb5d7224604d8c4c42cb8cdecb502257d9101c4`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 48.4 MB (48359071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795cd9a2a376fc17ed3ddaa808d00fd278ec23aeba11e5e79ad6f0c29d6b13bf`  
		Last Modified: Fri, 12 Dec 2025 05:48:07 GMT  
		Size: 143.7 MB (143679919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1cdddc0e8958029a90fe970327e0698cb8f2bf72c32ec137755c3be9c28e79`  
		Last Modified: Thu, 11 Dec 2025 22:40:08 GMT  
		Size: 81.0 MB (81025990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42572597e4ef20efec44dc6a2a0e408ea3b5b33cd7f16f5be51d7f22316d97f6`  
		Last Modified: Thu, 11 Dec 2025 22:40:01 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cfb99dd2d1c93436a26410981fc62c6793f16e7bc2df7493d58be990037a240`  
		Last Modified: Thu, 11 Dec 2025 22:40:01 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:1596cca9626d7952e30fc86442fccfe3e5bcff6e23489a4da5d1946a872ca8b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7396550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a37dec69ae0e522b130fae28d1a4387d40399cd1481c70ddcbae191d4b49e9a3`

```dockerfile
```

-	Layers:
	-	`sha256:da787e2b9dd675d1a29f2655a75c7aaecf82c5d6e904a17321da23fecfa054db`  
		Last Modified: Fri, 12 Dec 2025 01:37:50 GMT  
		Size: 7.4 MB (7380655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd173d172f87cadbd7f5458ac7216760b99f7e9452a04bc0ed59522d01b29d79`  
		Last Modified: Fri, 12 Dec 2025 01:37:50 GMT  
		Size: 15.9 KB (15895 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:d2a46982024849c08840a4c9956ccfb93263d69828286a4de1c4d0b99d6c6203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.8 MB (283835788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21494a563d0f767937fe2e851e1d021a450397ec6a9855283fe0e4d56d6efb5b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:42:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 22:42:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 22:42:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 22:42:09 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Mon, 08 Dec 2025 22:42:10 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:53:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:53:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:53:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:53:53 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:53:53 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c088128ea77bb5c706bb00930020ea2fba147060275f49c5a7be6b54af5ca7c8`  
		Last Modified: Mon, 08 Dec 2025 22:17:06 GMT  
		Size: 52.3 MB (52326977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35000cb1964cf20b1dfaf0b01681b83417814d0489bb0ac766df92e26616c6ab`  
		Last Modified: Mon, 08 Dec 2025 22:46:18 GMT  
		Size: 144.5 MB (144525257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b9316f861a4b9d0cff26d3f1b86ebc3e208e994c4c9a98c3daa5189393dc86`  
		Last Modified: Thu, 11 Dec 2025 22:54:58 GMT  
		Size: 87.0 MB (86982512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf8e9311c711f23b525d8c3b5eb2b36d79f0c15206de8d93eed3ead09da1a07`  
		Last Modified: Thu, 11 Dec 2025 22:54:48 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b4e0ebac6daae44e5af350d8b948e469c1205dd6b10231e801a7eb4491f7b95`  
		Last Modified: Thu, 11 Dec 2025 22:54:48 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:90f323a20b1fb32b3b20adefa9591a0700f529d9f126971e0dfe65d07d7195fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7395931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ca66a5974abf8ee1500a08845239cc4cf3061070e6160fcd77868b05b74549`

```dockerfile
```

-	Layers:
	-	`sha256:384ffaa00d27caa814c2b36507fb19ca4e4419fb8004407cd6bafbf28e9acd82`  
		Last Modified: Fri, 12 Dec 2025 01:37:56 GMT  
		Size: 7.4 MB (7380106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bb028cea6bc832731b2be6d40bdac6255162ef88795a93acce68ac5c9c58264`  
		Last Modified: Fri, 12 Dec 2025 01:37:57 GMT  
		Size: 15.8 KB (15825 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:23fe757ec253b586622af300f5ae10d1e9c81224704576f73fe6e321c4f5a5f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.0 MB (261952776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:759d7123ff62eb20b15419e2cae4a322a779dc1985ed37317a1e43e57ca7705f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Thu, 11 Dec 2025 22:33:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:33:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:33:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:33:12 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:33:12 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:33:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:33:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:33:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:33:25 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:33:25 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f1896ba83f603ad81e0d8cb48b496e763b4b781a68efe11f1b6de9da929514ea`  
		Last Modified: Mon, 08 Dec 2025 22:15:09 GMT  
		Size: 47.1 MB (47137665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a37b557cfc68bfb260f7a4c4d017a864b7f107aa9458fc0fbc5b61bba183532`  
		Last Modified: Thu, 11 Dec 2025 22:34:17 GMT  
		Size: 134.9 MB (134859049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f2e4a6bfdd31c620b398fdd3bb1384a1ccfea19c69ae1461fe2809cba6a0af`  
		Last Modified: Thu, 11 Dec 2025 22:34:08 GMT  
		Size: 80.0 MB (79955021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b02e733d9af57596be64325007b72066a8d5fa87a0bd06866368751e2168a10`  
		Last Modified: Thu, 11 Dec 2025 22:33:59 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6621e99c5d9de3fee08a7735dca870ecafa82572c3913170b2e2b72a0b34a71`  
		Last Modified: Thu, 11 Dec 2025 22:33:59 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:16cb53c19b0b25bffa0de58e42763e7056a459a4daf84a571512cb584313b4c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7381988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6c02c19ce488f2f52620f8ddf09e84d5198f35a4a94758998e0173a8cf7fdce`

```dockerfile
```

-	Layers:
	-	`sha256:068edebf66663041e770b316871cb4272005f4b9a6c3fe1cf3b680786fb518eb`  
		Last Modified: Fri, 12 Dec 2025 01:38:06 GMT  
		Size: 7.4 MB (7366211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daddb53c4b34f3a4c7bd11a6b7462e0ddba05b07a26dd3d8edc61501044a5f9b`  
		Last Modified: Fri, 12 Dec 2025 01:38:07 GMT  
		Size: 15.8 KB (15777 bytes)  
		MIME: application/vnd.in-toto+json
