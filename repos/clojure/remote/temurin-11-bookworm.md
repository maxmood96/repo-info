## `clojure:temurin-11-bookworm`

```console
$ docker pull clojure@sha256:50eafc9e0a1a2afcccad1e5e072465576756415e9092639ef1dbd98e9142d985
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
$ docker pull clojure@sha256:35412ab653de096c2dc5ff1fe9c59f8f533e5c4543950167de9f2f5ac8ecc579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.6 MB (275588687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:664058954f168106df643c8806091dd2aec6861beb3ea4418c109f952750fec4`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 23:34:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:34:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:34:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:34:16 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:34:17 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:34:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:34:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:34:30 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd57d488b84f7921a3b1685aeaee919f7f873beb65fcb022d20dc6ff06f86c1`  
		Last Modified: Thu, 14 May 2026 23:34:52 GMT  
		Size: 145.9 MB (145886202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9488a3ba78d3d9dffddd015cbde7b0a2d07cc0a3e5a0e3b2fc6e89c6b633da4e`  
		Last Modified: Thu, 14 May 2026 23:34:51 GMT  
		Size: 81.2 MB (81213161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf15eeb8fbebc736bc73fef2532689d4bfb7d896d887d14e57a2233b5be4bfa`  
		Last Modified: Thu, 14 May 2026 23:34:48 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d57519cd58feea309d1feb023a58bec2511a01b301bcb1535342bd4ae79b8a06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7412806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf6a170724f9f39f1a581466e15d4e7c4913ade69e11af8f3373ce850662e8c8`

```dockerfile
```

-	Layers:
	-	`sha256:adadacf64bd7244d0e2a815d013e477726dee6b99326dd99664f83a3ae192b8d`  
		Last Modified: Thu, 14 May 2026 23:34:48 GMT  
		Size: 7.4 MB (7398443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2516276d2f7b8120aa3b7fecd1d266581927cf14e77d90f4be73d94ca0176ef9`  
		Last Modified: Thu, 14 May 2026 23:34:47 GMT  
		Size: 14.4 KB (14363 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c3d1a3f99cf22697524a616a91a359fbb78c3639ca428be6d56dffda8dd9cf9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272152490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80de311141837e7cc24a3bae4fa46d58227adb1424e4a85dfb25e136fb88d816`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 23:34:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:34:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:34:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:34:50 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:34:50 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:35:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:35:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:35:06 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4ccdb18090db5931761bd3c6d6ec938c27b9378a759b6a3caa0a101c7e3fae`  
		Last Modified: Thu, 14 May 2026 23:35:30 GMT  
		Size: 142.6 MB (142582234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a804b904be1bacd8ab52844dc02c94bbcf74a29419dd2e39e73ba788964c40`  
		Last Modified: Thu, 14 May 2026 23:35:29 GMT  
		Size: 81.2 MB (81196459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94f0f3d8483e9e558ba815542b8b75f2eddc29c087fdedf81c2fd1804af26a7`  
		Last Modified: Thu, 14 May 2026 23:35:25 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:663754786c47962333f71bb4b6e6b153c443394fd65b6f59a1420d8b6d1dcdbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7419305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98dda69454635f3a865adbb43e63abdb49533ac18e1cfac54f5b5c779403d3c7`

```dockerfile
```

-	Layers:
	-	`sha256:55d6ce9654011251a8a6240097c1ae00c99549133da4f5782cc64c0ad12fe2cc`  
		Last Modified: Thu, 14 May 2026 23:35:25 GMT  
		Size: 7.4 MB (7404824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a95e9b042b822346fe5885918cae3c28827c1aa7e767710a70c47e3ad27f2611`  
		Last Modified: Thu, 14 May 2026 23:35:25 GMT  
		Size: 14.5 KB (14481 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:39c7343f06ccdbcafc5ad8d7bb7eec1baa11f242d198029bdbb5214a08a019b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.5 MB (272480601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc9cfa5ac1b956f7b18b92da3e1f133af3a8ed2e6b54399067b29588d6458d59`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Sat, 09 May 2026 02:25:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:25:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:25:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:25:03 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Sat, 09 May 2026 02:25:03 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:37:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:37:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:37:59 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:30ef9f53c997c6c1f1ab8f4cc559b32d9206d169c54ad5a0f0363076708fffef`  
		Last Modified: Fri, 08 May 2026 19:44:07 GMT  
		Size: 52.3 MB (52336787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07cbaabc187f4e33faa4937073e6b8d37c4b4ee8836b24edba986c27660880f2`  
		Last Modified: Sat, 09 May 2026 02:26:07 GMT  
		Size: 133.1 MB (133110168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5955f5b13b8bc7e2190efe9212d605f87246491bc33813556a89abbcab6a51b2`  
		Last Modified: Thu, 14 May 2026 23:38:39 GMT  
		Size: 87.0 MB (87032998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143ac12f0841777d6c66786ab9aaac09787e04b41dc38acca5fc0da81e0fd421`  
		Last Modified: Thu, 14 May 2026 23:38:36 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b673e3755e0adc3820133872014a9d442666e224f93cbd294f9842748bbefd52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7416499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7200e022037b3c772bdc7a1c37c67d62e91a686ff44983c0dbe0e70063cfecfc`

```dockerfile
```

-	Layers:
	-	`sha256:f7bbb2397a509be3ac057d3700fd76fde13f4446064b434fa1682ec3be5f0c74`  
		Last Modified: Thu, 14 May 2026 23:38:37 GMT  
		Size: 7.4 MB (7403044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ca1a8f8d9876390a8d3666d0c59ee0969066718864df0e61d62450e09b79af3`  
		Last Modified: Thu, 14 May 2026 23:38:36 GMT  
		Size: 13.5 KB (13455 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:83302ed956225ae8f982cb378ea369576df036c00a11e81b7ad2af1bb6edce42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.8 MB (253825373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1c410038d6ffe87ccba1ab2fe173337f0919585aa434317ffe8d63b4b7b415`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 23:32:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:32:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:32:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:32:15 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:32:15 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:32:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:32:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:32:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:124dbe049873037f973f01d877ec004bf4cd3ce5723d0b8f2067c58ad98137d6`  
		Last Modified: Fri, 08 May 2026 18:27:29 GMT  
		Size: 47.1 MB (47148023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e52372d5fb2e4448599149f5fdd18e1d6933ee7757f50701f6b69d3caa03696a`  
		Last Modified: Thu, 14 May 2026 23:33:05 GMT  
		Size: 126.7 MB (126651718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286b5c0821f4f10c8479f25ae4b102af7bd7b7d865a956de97de028133f2d548`  
		Last Modified: Thu, 14 May 2026 23:33:07 GMT  
		Size: 80.0 MB (80024984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eba98c74e76867f64c87f2005294f3e2f23116e675ad09c7037a4ed02eb9f08`  
		Last Modified: Thu, 14 May 2026 23:33:04 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:ac4b20c8e1c51efa213f2ca2dd56582b21f8223734614e4581cf3e5bd21dad5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7404129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69872b4679c79c4d8ba79ab8657bb0db50bf25815d9dd7d33f69e7f0a5fb0e3e`

```dockerfile
```

-	Layers:
	-	`sha256:207483745c98541ffcb44fb0979150148fca57bfb92f1e0916b0f981f59143ea`  
		Last Modified: Thu, 14 May 2026 23:33:05 GMT  
		Size: 7.4 MB (7389766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52437341d09bd8d73445a507f0c644558978afe7a8ca9c478bb169d2b026ec25`  
		Last Modified: Thu, 14 May 2026 23:33:05 GMT  
		Size: 14.4 KB (14363 bytes)  
		MIME: application/vnd.in-toto+json
