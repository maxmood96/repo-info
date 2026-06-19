## `clojure:temurin-8-trixie-slim`

```console
$ docker pull clojure@sha256:68a3ffde14b5405486cb126021397e8ef6c69157530df20e20e446b1068e7b6d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:44cf74583ee942d5384b06e0725f0261124091c16b8a55432414ea858557a82c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.9 MB (153936953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb359bea4a3534c6f891aaad2cfa7252661c6fa655a460b2af94e97fb409a83`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:15:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:15:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:15:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:15:07 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:15:07 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:15:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:15:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:15:25 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0627c6e531690c63ce17a157d332b9ce71344aca52e5492bce92ec77f72892`  
		Last Modified: Fri, 19 Jun 2026 02:15:43 GMT  
		Size: 55.2 MB (55198724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a390fac072a4ff9b7f94f31cf01fe675531a1a1e7efaf698e1d6dae3e981043`  
		Last Modified: Fri, 19 Jun 2026 02:15:43 GMT  
		Size: 69.0 MB (68952169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e54176a0556caf60d357d906e1c8b11a9ea77a9adc1d974df6b6d8c2b8c3d18`  
		Last Modified: Fri, 19 Jun 2026 02:15:40 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d0bb116c4ee41d4cbcad91e569e50a1883cdb87ee5e68befc41cabadf962c6ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5391984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4dc62b144d7b52e4af24de56c7f52b5c53ae2442c1aa0f7cc4b9c0490ef0f8b`

```dockerfile
```

-	Layers:
	-	`sha256:d8970c997c5e1d40ec0b6eb5ea35ad91b268fea6bf81471554b467b1b5f779fd`  
		Last Modified: Fri, 19 Jun 2026 02:15:41 GMT  
		Size: 5.4 MB (5377602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:093c82df975394ca16a5c894c2022924d8ecf22d985572c718696fcb61a3b943`  
		Last Modified: Fri, 19 Jun 2026 02:15:40 GMT  
		Size: 14.4 KB (14382 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b851a8276c1afb18f6a73d0904fa3b713639f9e0c94c22391a5d094aa770d611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.2 MB (153199386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35fda24f55beaf39ab8f07dedb3da88f07cb274daf2044b417c408b6cca6e5ef`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:15:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:15:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:15:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:15:13 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:15:13 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:15:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:15:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:15:30 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e2b4976242a58b65a7551755c4f13b4c7f115f7e94dc7096b26bae543108e4`  
		Last Modified: Fri, 19 Jun 2026 02:15:48 GMT  
		Size: 54.3 MB (54272934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b779054a4f7390c114186fda36107bb74680a2eeabe731bd1495aa23311fa7a`  
		Last Modified: Fri, 19 Jun 2026 02:15:48 GMT  
		Size: 68.8 MB (68777278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e123ae5ca9297a25a46d185ee788cc912a8df9a4ef84775e232109e75030f7d`  
		Last Modified: Fri, 19 Jun 2026 02:15:46 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b183fdc6c7131de9f77d34e6d9761240db58240812417869c08edfd8d5375b6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40a0148c6021959c178062d2e4e0ec826ec481cef16ccc3fcf85778dd1f1193e`

```dockerfile
```

-	Layers:
	-	`sha256:42cbd2e89c5c95057025d636aa1b443906758c7a4777c1ae1dfa7b8c233a33d4`  
		Last Modified: Fri, 19 Jun 2026 02:15:46 GMT  
		Size: 5.4 MB (5384063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a491a075a08aa290ca7680c679859374a6567413b7026253a99ec79507d811c8`  
		Last Modified: Fri, 19 Jun 2026 02:15:46 GMT  
		Size: 14.5 KB (14498 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:2a0f18c908c575458cc1b54eae1da84a47a2a83a08c14deeb96ca2a46509e853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160645264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c70705eeeb6dac82d7ed50f94e7bae110e0aeb579772a5bb5a1ed3112d15cf33`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:23:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:23:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:23:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:23:01 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:23:01 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:23:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:23:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:23:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9d6b2e320e2b74843186d830e8202c50ebfaeccf823d239e3e3e349a8a508d80`  
		Last Modified: Thu, 11 Jun 2026 00:24:42 GMT  
		Size: 33.6 MB (33606340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd24a32632bdd61e7e0c9fbd36c723775eb7543e69a23326b4f3e78dcff0214a`  
		Last Modified: Fri, 19 Jun 2026 02:24:33 GMT  
		Size: 52.7 MB (52669121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ddc803aff3bcc374a0d91bf21c9046cd8c6f15424198353b16aeafa8baf94c4`  
		Last Modified: Fri, 19 Jun 2026 02:24:33 GMT  
		Size: 74.4 MB (74369160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f363ff095f04bc8d4214ecb37fe1ccd95f9b8d20e16214435c78e2bc63d41d1`  
		Last Modified: Fri, 19 Jun 2026 02:24:30 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4348cb2486a357800e9a51e7b0e390ae696381ca94e873b91b972bb9ca49132e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5396998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:661eb288f29c1efdbcfd63380fe3727bbdae68bdc6ec30ecd1102c1b0d2a90c1`

```dockerfile
```

-	Layers:
	-	`sha256:ce3aa151dcc22aa830f2c332d513b56933e879f193d843218415bc8760d2b964`  
		Last Modified: Fri, 19 Jun 2026 02:24:30 GMT  
		Size: 5.4 MB (5382568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83670121c668f4f62499750dea26a72094d4d1e02c25962f65bc13a75291d55d`  
		Last Modified: Fri, 19 Jun 2026 02:24:30 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json
