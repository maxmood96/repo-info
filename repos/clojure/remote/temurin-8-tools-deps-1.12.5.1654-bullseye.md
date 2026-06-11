## `clojure:temurin-8-tools-deps-1.12.5.1654-bullseye`

```console
$ docker pull clojure@sha256:4c13b202a33b7ac69bf8b83342e52f5d7bca5036c61fc784daa82bedb933e41a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.5.1654-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:3bf2da45cde48e4b903e3bbe179e19c60813b46b7b0594878725497f61c9b37c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.5 MB (175483562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cf85f618bd76b7b5560f65a00fcfa1403489dcbadb321462c55386475e7e839`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 01:15:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:15:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:15:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:15:38 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:15:38 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:16:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:16:27 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:16:27 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:af48a3e7696e07f88a02f9674e541901b65eadb5cf0f62e566b1d895099a1e9e`  
		Last Modified: Wed, 10 Jun 2026 23:40:09 GMT  
		Size: 53.8 MB (53771769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad41bbbd8855cd51d869142e12ac8fb77cfd5b1a58c5a21b30ee9f4da8b244fe`  
		Last Modified: Thu, 11 Jun 2026 01:16:07 GMT  
		Size: 55.2 MB (55198726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58aaf0d1a1edc1ed43b35ae1452615f917b3b19cb5f68b5f46fed006ed4df142`  
		Last Modified: Thu, 11 Jun 2026 01:16:45 GMT  
		Size: 66.5 MB (66512424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0362f7135b5cd3448b65b50621c33f19ad5441f1151146b13b9a96bb4ba18370`  
		Last Modified: Thu, 11 Jun 2026 01:16:43 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.5.1654-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:01fc65c1753be866aaaecc9ee175771e88dbea094ac256d243a30c4edec1aa2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7539202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c246ff8c0748f37cf300432a6183d185fcdebf90135fc13ca69798b6558a0cfe`

```dockerfile
```

-	Layers:
	-	`sha256:9a9b083f2ee604aea08eefd4e7960a28b89dfa5118c1b850f6009a1d79c151a6`  
		Last Modified: Thu, 11 Jun 2026 01:16:43 GMT  
		Size: 7.5 MB (7525809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58a2a52e12b8f5085492d5df9a35d1e2458cecac968496123480c72ec7c9aea3`  
		Last Modified: Thu, 11 Jun 2026 01:16:42 GMT  
		Size: 13.4 KB (13393 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.5.1654-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cd2ec29de9d1fd47851c1479be4f3752a36c341209c1da500fb108389ee3830a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.2 MB (173215386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81947715933a72eb1c80ea6c16f52226c19d9fa84c03a1a3685a7b58dee3815c`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 01:20:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:20:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:20:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:20:33 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:20:33 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:20:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:20:47 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:20:47 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7c21e59e753cb91625909251110d6e4cc4a5411b4b7b37f74a62e56b927b7f1e`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 52.3 MB (52264114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143d75d71e52fe6dab00c488c06cdf95e30cc7557181a478162a40147886df6f`  
		Last Modified: Thu, 11 Jun 2026 01:21:05 GMT  
		Size: 54.3 MB (54272936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea51e99d94ff12d402ce442ecf981628e60eb7d62974797aadf673718fa0f518`  
		Last Modified: Thu, 11 Jun 2026 01:21:05 GMT  
		Size: 66.7 MB (66677693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e264d852708d0bb2750fd432d7942f0c1a45afc1fe8346538bfaea61502c44`  
		Last Modified: Thu, 11 Jun 2026 01:21:02 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.5.1654-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:f7b15d5b15bb14676b235921dc2ef4f20114f4c38a3b65616ddcc9855189e908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7546074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2a1778a0eef7b22bcd598f4c7bb0d36d02dc619a255b7390c0493dbc2e8ed9e`

```dockerfile
```

-	Layers:
	-	`sha256:b18668ac203fbfb3a06b55c348bd0e216a4bc08c2e0c23408e033c1b8e36299a`  
		Last Modified: Thu, 11 Jun 2026 01:21:03 GMT  
		Size: 7.5 MB (7531608 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d131155fe89c2f03435e4fbb85704ee59eeb2c7e6fdc349f84a1d53c4de728a`  
		Last Modified: Thu, 11 Jun 2026 01:21:02 GMT  
		Size: 14.5 KB (14466 bytes)  
		MIME: application/vnd.in-toto+json
