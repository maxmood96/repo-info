## `clojure:temurin-8-trixie`

```console
$ docker pull clojure@sha256:1d4caca0ceea328344e0a59dd4db9e5c297ea31e63c1489981b5219ef29b8ce1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:c5e8ddac1abb41e6a6642fbcc3c7d3d80afc17c1ae7cf72cbb0656c6aa03ed29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.0 MB (187035720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0256162df1c977f0a54354d7c7930cbd8a520c2f9ca37b2a5c4803acd674268d`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:15:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:15:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:15:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:15:47 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:15:47 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:16:51 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:16:51 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:16:51 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ef1b08ddd59d42b444e8f9c68a6cebbed70636aed0c242fdccb0bd61b61ba26b`  
		Last Modified: Wed, 10 Jun 2026 23:40:27 GMT  
		Size: 49.3 MB (49317121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f2a10c9e0919873abfc77c653c59aa5a1108b87f890949c154f54dd1d3c5ce`  
		Last Modified: Thu, 11 Jun 2026 01:16:19 GMT  
		Size: 55.2 MB (55198716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec6f97b3cfbbe4f5555f86d26c35a54d7e3cfd4a573de78e64b2e2748770a2ae`  
		Last Modified: Thu, 11 Jun 2026 01:17:09 GMT  
		Size: 82.5 MB (82519240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72350c0442b2fcb0662f8637083002581ca9399a4f4471cb4d472ad85b9eb74b`  
		Last Modified: Thu, 11 Jun 2026 01:17:07 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:47cd799bb1d98ba26b3072fbf59717618d9bf7016743d3d13db044bb438d68b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7602500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:012cfaa39596c8c5e15e5e606372a116e5e0da2ebfa7efea99bfc074e7b5e0cd`

```dockerfile
```

-	Layers:
	-	`sha256:ed32dbff1f2b73d400b9dadd25add720b33ab469fbf344b6f14ff0d335b2ea0a`  
		Last Modified: Thu, 11 Jun 2026 01:17:07 GMT  
		Size: 7.6 MB (7589131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce0d1b80fd799ea11aff277173708422258945b14ca4e99adcb4f59c7cfe25bb`  
		Last Modified: Thu, 11 Jun 2026 01:17:06 GMT  
		Size: 13.4 KB (13369 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8ff57574453f9430db060ddfe215020892cd75ce7a99bc768c1605d6ef8f47d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.3 MB (186290108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00e641685f621889f0f25c828d0d21f594d373114eaee0a2b51efb456170f4e0`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:19:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:19:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:19:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:19:53 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:19:53 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:20:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:20:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:20:50 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ed660e1af0f5da9e93a4c43fb29e86cb46fe69c76bcf11a3de9c57c987acab82`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 49.7 MB (49678169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63d7f1ce31d05a62238525ce8cf3ea30d1cbab129a966e41e305b63e1d63390`  
		Last Modified: Thu, 11 Jun 2026 01:20:24 GMT  
		Size: 54.3 MB (54272927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6181d47e9ee3f0fc304d8282fb8ce6f6bf7b7d8116a5fba1e7c7400847804c5`  
		Last Modified: Thu, 11 Jun 2026 01:21:09 GMT  
		Size: 82.3 MB (82338367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c88f6b29680457d8a77e2738f3fdaa112cedc08b73d637ec0bc0a1590a962e7`  
		Last Modified: Thu, 11 Jun 2026 01:21:07 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:17460367649c0ec0b607f6af6d4e0081e4945b5a621ea8ae187417e7d67a5d2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7609712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:989bf7075d7d910d938d351d7a75ad9b6dadbbea3a0371d86b5f5f4a92092beb`

```dockerfile
```

-	Layers:
	-	`sha256:145a1b29c0d838aba89e2b94c2c4ae6a243b4117e4184ae20a75eea1cd4c04ce`  
		Last Modified: Thu, 11 Jun 2026 01:21:07 GMT  
		Size: 7.6 MB (7596224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f735285322b1b595b81ca2384fbf3a245fa82eac9faa97ae31c7828731eb6072`  
		Last Modified: Thu, 11 Jun 2026 01:21:07 GMT  
		Size: 13.5 KB (13488 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:e6938be9a67b04f6b4112568e0f89e84decd70f67a6520c1cf4e288bdae658fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.7 MB (193746196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40e5c716fc34266d5c3c0dc9ce32e3a53d5c9ccda3f3ad54a79c4b4eda8ad430`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 09:17:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 09:17:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 09:17:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 09:17:18 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 09:17:18 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 09:21:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 09:21:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 09:21:01 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:fc2380819f7227178ecd607b245c244d8811737f42c6112caf011a01a3889a8e`  
		Last Modified: Thu, 11 Jun 2026 00:24:43 GMT  
		Size: 53.1 MB (53137939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bf754746c3f17631e9d8f036f4e175f1bd71812587b986fa8fc268bafa219a2`  
		Last Modified: Thu, 11 Jun 2026 09:18:32 GMT  
		Size: 52.7 MB (52669138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553b75ba8a2340a503b1f7993d4c50c9318d09702b337b2d4e948251c2a32d0c`  
		Last Modified: Thu, 11 Jun 2026 09:21:42 GMT  
		Size: 87.9 MB (87938476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab51b7406b1ed8281602ee25b86b099a1644833f9808af54a420a83908c74ae5`  
		Last Modified: Thu, 11 Jun 2026 09:21:39 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e2db4222e4981457c34d9573af42a39785fbf0dcc7eaaf5ee930ed62ddd0c0c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7607565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc054192e7bb4a93ad83f9bde27002d75e9cdbefecaa1f501e2682e24d5a488`

```dockerfile
```

-	Layers:
	-	`sha256:0b16ce67f066252bdff902b3d8f4b4d44e82eb0eff4f46479a8835794106fe46`  
		Last Modified: Thu, 11 Jun 2026 09:21:40 GMT  
		Size: 7.6 MB (7594147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6766c8d2d7847283beced73e60e35db2fefd43cb4177bc62093dde9d9b650cf8`  
		Last Modified: Thu, 11 Jun 2026 09:21:39 GMT  
		Size: 13.4 KB (13418 bytes)  
		MIME: application/vnd.in-toto+json
