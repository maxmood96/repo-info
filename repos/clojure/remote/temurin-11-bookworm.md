## `clojure:temurin-11-bookworm`

```console
$ docker pull clojure@sha256:3eb610723a59054932d91b15b6f9bcdb2c01e4ba54bcc012d30bf8391ff86a38
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

### `clojure:temurin-11-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:1c9f386ec411df72ee08b965b659a72763c96718484f6a1e005ffe56e7a9381b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.1 MB (275118741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aa7a477f7a568e64c8e8534cf886f7dd051aa2b7d03c922d7faf86cdeef24e1`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Tue, 03 Jun 2025 13:30:19 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f226527949e63264ec1bfdae881cba35688c8d844f827037a042f1db72f870b7`  
		Last Modified: Thu, 05 Jun 2025 02:26:17 GMT  
		Size: 145.6 MB (145635594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e03f591928971ef43e66259e4e4782ac70ac4dbd7173e49d18d0183089c4442d`  
		Last Modified: Thu, 05 Jun 2025 02:26:16 GMT  
		Size: 81.0 MB (80994259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7f8acd740587c6fe4187ff839db9ed5e8a003e8664db226bc1f2351cda8b42c`  
		Last Modified: Wed, 04 Jun 2025 09:18:16 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:3bbe9f59718fc50418eb16b6133592f1776d31899e1a9f220e41b70369e7f203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7252915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d40f1edb871cd02bbafb66becce437e2d6514d00c7371b3537f39a1da55726f`

```dockerfile
```

-	Layers:
	-	`sha256:95182399f4d4c3535e648d35a8cac416909fd65ba61bae721928a474011935db`  
		Last Modified: Tue, 03 Jun 2025 21:34:55 GMT  
		Size: 7.2 MB (7238663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e15faee5d96c37322406cd2e35a1a5dd498edf4b97e69a0eececcbedc364eeb9`  
		Last Modified: Tue, 03 Jun 2025 21:34:55 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0a5aed652b489d5194120109f35b605433df90a663d05f8ce1cc54f6b33a7893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.6 MB (271597602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b024457fe69dc72b7b4b0096a2fb9bc31dded8c0cd3ff0c38ca12c98184855e7`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07fd337589b0c96f06ac5d8a22e233b7ae5c98928b27c342b7ea0174f5098e96`  
		Last Modified: Tue, 03 Jun 2025 10:40:13 GMT  
		Size: 142.4 MB (142420644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9040f16649c3559ebf9a1194d79f022dead4a4de44c1719ccb1438aea81fbfe`  
		Last Modified: Tue, 03 Jun 2025 18:32:30 GMT  
		Size: 80.8 MB (80849132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d7c333797456d49b451ad448dbc60d7d576bb7027a6e356bd0932539ce7075`  
		Last Modified: Tue, 03 Jun 2025 18:32:25 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:ed034e95e516b06a0330c969e0e36e6ba4971e1867f62bc90939c382cb6e0c49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7259414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d160404830b26794ce75e23453d8dbded7739ae4ea967d380e5d107e92080a2`

```dockerfile
```

-	Layers:
	-	`sha256:e48224acb71ffe6019014ca2658c8f0481371947043e288d25c7efd5fb3e8f9f`  
		Last Modified: Tue, 03 Jun 2025 21:35:02 GMT  
		Size: 7.2 MB (7245044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9bbd13f3566b7667446df7bf3c85e0b1953143234194612f7e929fa99e09c15`  
		Last Modified: Tue, 03 Jun 2025 21:35:03 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:26036707bf86cd3bb727fe2f4cec44a27473940403fc587dc54fd4b5e1619e3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.0 MB (271955940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba3cc2839f1dd7c49537596ed3a96d0879419f3582691dba0f17e35c67d00362`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:996840ee350796081b3c80118ca1a58ce8212c6fdf88c454706a16457903a0c9`  
		Last Modified: Tue, 03 Jun 2025 13:33:40 GMT  
		Size: 52.3 MB (52331619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc84d937b9f9c6a8fdf10268fbf36f3f3530d2d16cd85cb8e98d71c60b41b51`  
		Last Modified: Tue, 03 Jun 2025 08:25:04 GMT  
		Size: 132.8 MB (132810522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742f95dd5fe27fa2c97158942f543a715599be6ac43f778d694092484582811f`  
		Last Modified: Tue, 03 Jun 2025 18:39:27 GMT  
		Size: 86.8 MB (86813154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4c7f3e2a3b15f8bbfa14e8fbee51322ee3c912bc3df5a79bf3643776c52e69`  
		Last Modified: Tue, 03 Jun 2025 18:39:23 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:3770f0d6fe4b891beb3c43e3d2cd3ae0db24da11d631e75e6645783a69b95a19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7257552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f35e618a056d4593ffc1c04f84f372d9e5e16846b82a44012f0ee40091a4d749`

```dockerfile
```

-	Layers:
	-	`sha256:2237860d376768260aa67a9afd80149c3d2adc93eda8486f544d03db10409114`  
		Last Modified: Tue, 03 Jun 2025 21:35:09 GMT  
		Size: 7.2 MB (7243252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a566a0c33b54879a1306fbebd64458f046891ea59cc4f16c64c70928f384fe0`  
		Last Modified: Tue, 03 Jun 2025 21:35:10 GMT  
		Size: 14.3 KB (14300 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:aaa81ae5fe492c920780c1d8402e390c3c355f840843d5ec5d494151d3222e3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.5 MB (252532561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:406c1bf6de138a1d7c32f53e4eed5232a02039382f5c885331efe1194a3dc57f`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:47f9a2c2279c9df9e222a4c8af501e43b0b5e2552eda9597a97162080b8f106b`  
		Last Modified: Tue, 03 Jun 2025 13:33:39 GMT  
		Size: 47.1 MB (47143842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86c88c5d926257cdcfb8a6708039fa40a0a893499f3bc0262b7011bfd58b087`  
		Last Modified: Tue, 03 Jun 2025 06:00:21 GMT  
		Size: 125.6 MB (125585354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de86c7fe3621ccec24386aa20fc5caa0d0a94b54aee7ef5a38893c42f6a07800`  
		Last Modified: Tue, 03 Jun 2025 18:25:29 GMT  
		Size: 79.8 MB (79802721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8140168962e63da3397310eadc0a25ceb2d1f80e22a482febcb5d19d256e652d`  
		Last Modified: Tue, 03 Jun 2025 18:25:30 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:cdfbadf03ea132f0e89221fb00299bd4f1b0bc1fb1f75b3e66b23602f840d36b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7247130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f596cd477d6bb18dbb960e10349ec3bc4bed50afae8cefa18c3e2fcd8fe89da9`

```dockerfile
```

-	Layers:
	-	`sha256:efe162aa79701937c7b36cecf24d0e58435cb3efa1e57ab0b4e52d3ee16af57c`  
		Last Modified: Tue, 03 Jun 2025 21:35:16 GMT  
		Size: 7.2 MB (7232878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24550b7ad61bcb00e6f50e731b0f5f958929702025d7062608dfcc63ef6fc9f2`  
		Last Modified: Tue, 03 Jun 2025 21:35:17 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json
