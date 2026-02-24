## `clojure:temurin-11-bullseye`

```console
$ docker pull clojure@sha256:e0a69ed850230cc3aeef77af394c31f9d357fdcdc4516f950a5110d45a732dfe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:f71889555c0dd9016686bd5c9e81bef7e0fdefb1f241792cc7dd35d989f2d0a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.1 MB (269131488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d5b89b135ae23d8b4365f7f9a0f414417d4e671ed52679b688ceba5ab56c992`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 19:54:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:54:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:54:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:54:09 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 19:54:09 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:54:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 19:54:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 19:54:23 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:fd834ead99fe4ea0884686321217c38494a7a0c7327e2a5ed98d978011de7ddb`  
		Last Modified: Tue, 24 Feb 2026 18:43:07 GMT  
		Size: 53.8 MB (53756434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead3fa85dce30c6fda47ac9e23b52188d5a7409318fbaf08f79e51031fd77299`  
		Last Modified: Tue, 24 Feb 2026 19:54:46 GMT  
		Size: 145.8 MB (145806748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ff32c048ad1cddffd499ee77941d2ee98b2cb556920730109813adaa43d3e8`  
		Last Modified: Tue, 24 Feb 2026 19:54:45 GMT  
		Size: 69.6 MB (69567663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b972fe49ab5609fffb4b2f6a1f5f554f3c1bcf5952818cc18172b4d4699f8d`  
		Last Modified: Tue, 24 Feb 2026 19:54:42 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c136329f2dfc4e38b57add61354b2564ef5db9214f595fe08c7c3ecbd3c1f2f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7442114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31e5d97086cbc281831fc48876d02b529335fb385a07402e4d56d28a7fcba9c5`

```dockerfile
```

-	Layers:
	-	`sha256:1a67d01390eddaf859d4adc1ea349f9968b2231aac052a9a06c2b3aa4059cfb4`  
		Last Modified: Tue, 24 Feb 2026 19:54:42 GMT  
		Size: 7.4 MB (7427905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:297f6c0b097b52e6be67d366d0f1f5c97b1970f2ce05c83903ea376f6af210a5`  
		Last Modified: Tue, 24 Feb 2026 19:54:42 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b5ced46193961c7c577620a4bbdc12a71b0afcf52e25f19c0d9055d3917c71fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.5 MB (264469120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b65bd8817e7af5b318d3e7bd16521278ef5d84e6afdd11c318820138dbd2e52e`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 20:04:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:04:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:04:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:04:51 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 20:04:51 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:05:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 20:05:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 20:05:05 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0509053f2cf8072309184287dd2fd397e589dc5db17a1ddc469001be80ea07a3`  
		Last Modified: Tue, 24 Feb 2026 18:42:38 GMT  
		Size: 52.3 MB (52258392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41eb63ce310e21c3ca4911221574e1ae41179bb2c655e95b2c72cf8d1760d8c5`  
		Last Modified: Tue, 24 Feb 2026 20:05:28 GMT  
		Size: 142.5 MB (142501443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5dccdbf69210b39e9392d16f90958bffaf005102eb5ec1272ababac5d9b5f6`  
		Last Modified: Tue, 24 Feb 2026 20:05:27 GMT  
		Size: 69.7 MB (69708641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ee010e0b079287b4ebfe8b4c592b9d8a656f5ecad8f9af181a9e0186c092aa`  
		Last Modified: Tue, 24 Feb 2026 20:05:24 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:1f714e60b9faf161c66e1150663beaef8cf797082bbc955394cb225669d8ad93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7447949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8068f51b281a4daa07ed57984f8b5a7ccc133089bcc12d1da6d4d98925338f69`

```dockerfile
```

-	Layers:
	-	`sha256:2c11110f5636208f5afe9a1d435cc4e274543a2812dc8a3065759c4eb3cef32d`  
		Last Modified: Tue, 24 Feb 2026 20:05:24 GMT  
		Size: 7.4 MB (7433622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:deba21d04cf0bdc2c3fde997602ce1a09d6df5d1d0fd19c81e7264e9498040cf`  
		Last Modified: Tue, 24 Feb 2026 20:05:24 GMT  
		Size: 14.3 KB (14327 bytes)  
		MIME: application/vnd.in-toto+json
