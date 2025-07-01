## `clojure:temurin-11-trixie-slim`

```console
$ docker pull clojure@sha256:ac0837b86db35f4dd5cb003dc4a9fdcc488d7287c237995bf8e9366162d4ab52
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

### `clojure:temurin-11-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:24b7a7f9cdbfea9503b190ed5723580f05c577e27593dc3a6f86ed40fe1cf362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 MB (247209283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eef2c95e29826ca693248474310f79c724ac0ca728607b7822176d0e815a9806`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1751241600'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:f7f88c6d7f710176d487a3ac59c7790f981832a06bfc197dbe4a74d73b1407b7`  
		Last Modified: Tue, 01 Jul 2025 01:14:56 GMT  
		Size: 29.8 MB (29761106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c007f3bcb7e5cdc56888ef71872415016cd5862f567475653636f3d34648965e`  
		Last Modified: Tue, 01 Jul 2025 17:43:22 GMT  
		Size: 145.6 MB (145635676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcb8c3470f62c0a66b8aa8c880c9942d04c35495fb5fac10693bb8bd2ff3a8b`  
		Last Modified: Tue, 01 Jul 2025 02:39:29 GMT  
		Size: 71.8 MB (71811856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afad3c8a09cf5f5a509ef21cde3a067f0fccc990dd446a1c719effe0833ae928`  
		Last Modified: Tue, 01 Jul 2025 02:39:24 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c016db049f5481e5a377af5d2e8af8c2b78780313941398912cc2cb984a60026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5287228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a5f8a0e837b5dea9a0b2abaed9d3067e3b7bc8167f8006a13d502393a97d57`

```dockerfile
```

-	Layers:
	-	`sha256:eb62b45e3d4081ccd3058bca41fbfdccb338c30af3ca5f77795315d14eb0a6fa`  
		Last Modified: Tue, 01 Jul 2025 06:36:35 GMT  
		Size: 5.3 MB (5272943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ee067d59c18b3354459adc7bd4c966289bd204884b32a0189bd8cbc18441e77`  
		Last Modified: Tue, 01 Jul 2025 06:36:36 GMT  
		Size: 14.3 KB (14285 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e95dada5c668633fc201ee85f1e47bffaddab56ca94c82955f75c64da1b00cae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244190952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e840df7e2b50431a9d875bb6b6139680f92859171309796078d2accc4407cbd`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1751241600'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:dfa10e860e0106510a14bae8331a4dd762d3d3737fdba0dbec102458f9853b71`  
		Last Modified: Tue, 01 Jul 2025 01:18:18 GMT  
		Size: 30.1 MB (30126864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9567d00eb14ef925231e5e45d487c4369b49a06892b393b014b6e576c603a7`  
		Last Modified: Tue, 01 Jul 2025 12:10:06 GMT  
		Size: 142.4 MB (142420681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f65eed9e19345e63acd67cac024021adcee259f1b5494f0fe9c96b77f2126e`  
		Last Modified: Tue, 01 Jul 2025 12:17:06 GMT  
		Size: 71.6 MB (71642763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6077d92a2af423c200b9f2cf06b1b402fb679cfc36424f82134738d3fdf6116`  
		Last Modified: Tue, 01 Jul 2025 12:17:00 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:364d673c2c21671df670de2cecd580a882fd5b4ff362ef3abcb64e3de3a4c67a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5293734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64900af51b568fe4ecb8bf04f01925295fae4f9c051e3d8e12d0191d49897bf6`

```dockerfile
```

-	Layers:
	-	`sha256:583f30049ba233e0ff0e815fedc0204e0a3d2738580fde21a6c0ba82a75ba744`  
		Last Modified: Tue, 01 Jul 2025 15:36:15 GMT  
		Size: 5.3 MB (5279330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ab26f6509cb6852891ead611c0c22d4031604133a5d1bfc3ab43d1f779bd853`  
		Last Modified: Tue, 01 Jul 2025 15:36:16 GMT  
		Size: 14.4 KB (14404 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:935da06452c5eba7265bd405322209ea7d9b0fede7be3f22b7cc4a013b2161d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243630092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b99959491e12d98d2920cc5e8c114c84cfb22d67a143169b1570efa6b99ffefc`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1751241600'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:2adebcab7d76ecb14ead3f70af8ca34e5abca513c2fcbd9f40e3af1e18442ccc`  
		Last Modified: Tue, 01 Jul 2025 01:19:23 GMT  
		Size: 33.6 MB (33586035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed42b7a45be9a319908284c305fbff7f8a11100527571431a46ab61609503d1`  
		Last Modified: Tue, 01 Jul 2025 08:34:13 GMT  
		Size: 132.8 MB (132810556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae36720d6e361aa78efc5846c47c84a0a41df2716bfbddf9ad18e2401764b62`  
		Last Modified: Tue, 01 Jul 2025 08:40:23 GMT  
		Size: 77.2 MB (77232856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b100f07698ef647ecb64cb32356513f9d27f5f5e80095d6828f344f6a3076496`  
		Last Modified: Tue, 01 Jul 2025 08:40:29 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:06242b7b8b10ec5c60f4224df27dc2dc655f05c4a9f1eb948a0d4abd41b2ff76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5291032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2bf4efca753514d3d7d6df6e1c8d87af79fce324b59bce988b9fc4ce04086dd`

```dockerfile
```

-	Layers:
	-	`sha256:fdd8e0389f8e8b331db5826fe41e4662feac558a2fa13207d75d2d1087c3f98d`  
		Last Modified: Tue, 01 Jul 2025 09:36:52 GMT  
		Size: 5.3 MB (5276699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37076908d53bb86eeb32e4750ab6ff1ace825c63286559e10e8cea4936fafe1c`  
		Last Modified: Tue, 01 Jul 2025 09:36:53 GMT  
		Size: 14.3 KB (14333 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:ff749b610d799573be20cd1b1c3acacebb100c624de8347456437d84926210de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228226706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:504d5ec15f9a13efe2522dbda75a99f1f3e0db4046a3dc4c4132678114c051e0`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1751241600'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:728fbd29b8599bd56dcb8703b5c428523bcf0f3d48c5e95804f60267a128a3bc`  
		Last Modified: Tue, 01 Jul 2025 01:19:25 GMT  
		Size: 29.8 MB (29838345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb755fd3e834f02efea83622543254c015a4203f3a730f75a90cbca87af499d8`  
		Last Modified: Tue, 01 Jul 2025 08:06:09 GMT  
		Size: 125.6 MB (125585329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f9e25d787b18b8c173e6d09734690ca89fc5382613edbf9097ec66f86e70c0`  
		Last Modified: Tue, 01 Jul 2025 08:08:42 GMT  
		Size: 72.8 MB (72802389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3900e013dbddf97e499b6862d4f7234f1a327aeb1d201a86ec37e1aeebd4e32b`  
		Last Modified: Tue, 01 Jul 2025 08:08:37 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:58e5fcc36be12bc6a887f73d0a37696abfd4e47f345d56b517049caaccf79ac6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5283157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98faac58e2292d5f7ebdfbec17d0be630064cdfea321a1fb300ed3b49343f794`

```dockerfile
```

-	Layers:
	-	`sha256:e5be886ed20a0ff9ba999c683456c2a65ce66541d22b4f162876ac42f10608f2`  
		Last Modified: Tue, 01 Jul 2025 09:36:59 GMT  
		Size: 5.3 MB (5268871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec76cef026b7cd02a973950a337899834aff248c4653728de3c2536b1edbdd3b`  
		Last Modified: Tue, 01 Jul 2025 09:36:59 GMT  
		Size: 14.3 KB (14286 bytes)  
		MIME: application/vnd.in-toto+json
