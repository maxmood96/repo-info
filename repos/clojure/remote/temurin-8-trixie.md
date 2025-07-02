## `clojure:temurin-8-trixie`

```console
$ docker pull clojure@sha256:3d9570fd242963ef384d28313a835618e081e1e89ee6ba5e14891e370554d5df
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
$ docker pull clojure@sha256:947c2abb291ca9b2799c4551609373e0d30bf75ea4492075fde42b3eac589f03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.3 MB (189335823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d255c4aaa299785d48cc0f11cc164237ff409fc7362b22683a47ae16e2bd6fd`
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
	-	`sha256:b72fed6e2775feec9291a4bd4b416f996dfc503eda11eaa00def55711302b4ce`  
		Last Modified: Tue, 01 Jul 2025 01:15:00 GMT  
		Size: 49.3 MB (49263877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2121166af06e1412056dcacf68b2efdf4d55cc03422e495b470fab63edd53f5e`  
		Last Modified: Wed, 02 Jul 2025 04:16:12 GMT  
		Size: 54.7 MB (54716181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffeb5103650a881f19dec1a69133ffd3d73b8e94fd92700851bbc6ccfedc2966`  
		Last Modified: Wed, 02 Jul 2025 04:16:13 GMT  
		Size: 85.4 MB (85355120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251ccd57109451fe7e83952d84b86b2d2c8d7f7038b101b40efff84598d53efc`  
		Last Modified: Wed, 02 Jul 2025 04:16:11 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:0dcae7cef67c12eb3c66e5b60363d9a3e16c47993415db2fcf97bddb5fb75462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7594976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:855f8a922aa657165c4256c9ae57b0e1ce39e724d468efd2dbb2f63789fd0742`

```dockerfile
```

-	Layers:
	-	`sha256:3d3ddaaf24fe7c4d07a199d60e399fadcb29371c5e5c7c8ed878250a5af4fc3c`  
		Last Modified: Wed, 02 Jul 2025 06:44:12 GMT  
		Size: 7.6 MB (7580763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:481bf4e2692bb87c5217fe3aeb4f95426364d3ab4cddf715e45a314e96bbbf9a`  
		Last Modified: Wed, 02 Jul 2025 06:44:13 GMT  
		Size: 14.2 KB (14213 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5c5b7c71ef8d5f815da0b69b9af60174cbeb5ff5b66ad01c61daf381468e073f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.6 MB (188633737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd9ff39cca48ad1d6019e10ed855c379283032dc85db269807af55437580b9a`
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
	-	`sha256:2581a046e315a4b3013d50a17da46bcffbba144014a55d733fa55c3bafc6b7ab`  
		Last Modified: Tue, 01 Jul 2025 01:18:05 GMT  
		Size: 49.6 MB (49630154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cedf430bb4ee6a97bdfaf3b0fbd013b9d44aabf27f1bacae3767d1c0c0ed478`  
		Last Modified: Wed, 02 Jul 2025 12:09:34 GMT  
		Size: 53.8 MB (53830515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56796ce50b4d251cc8084ea14fb8235310bb80abe928eeec7a686088ff705a2`  
		Last Modified: Wed, 02 Jul 2025 12:15:20 GMT  
		Size: 85.2 MB (85172425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f808bf1eb2c7f68bd0fc3fccd63104d710a3aabc024fb0db17b850e5892e64fc`  
		Last Modified: Wed, 02 Jul 2025 12:15:12 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:33ab559f3934fec837993c51339a79eab3f686ecf6c19e6e4164a3a205ab4dc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7602822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c02d09115df94ce0e34b3388f68d22e233f0ce7964b714980e9d1def73d66b26`

```dockerfile
```

-	Layers:
	-	`sha256:924b0f7346273306894c0f39936202d4dfac09616610d697a672ff8b949cb998`  
		Last Modified: Wed, 02 Jul 2025 15:45:29 GMT  
		Size: 7.6 MB (7588491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0de12dfef5a0f83e0f78a6a5a47882980963a21feca28fbb431e35f7eb103df`  
		Last Modified: Wed, 02 Jul 2025 15:45:29 GMT  
		Size: 14.3 KB (14331 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:deb86cdf3c571c513fc87738f5ba9f935e13943560b6bf44ce53dfc995878f51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.0 MB (196035497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f070f217fa4e533d6ec43772efc0ff88aca90fce72d25fa6c8bd593e063f61d5`
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
	-	`sha256:5c6a246a80c20351fe842a314b6b3f8561a5ceaea736decf36fe380b29e53224`  
		Last Modified: Tue, 01 Jul 2025 01:18:57 GMT  
		Size: 53.1 MB (53097236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd98a2338e8bd817abecf8a68e60f9fd387ebb54aff3cada9115e6ed4a82ccee`  
		Last Modified: Wed, 02 Jul 2025 09:57:48 GMT  
		Size: 52.2 MB (52167965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2cb5895041deb942d26294d4c5ea1cdad22ac0a89c5beb740b4026b7e51fab`  
		Last Modified: Wed, 02 Jul 2025 10:06:10 GMT  
		Size: 90.8 MB (90769651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9558ff12a783e401b14035e08efef18d0efd407e239a1e97d899ab2ab4704eb`  
		Last Modified: Wed, 02 Jul 2025 10:06:45 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4e6c6a120182afce0c355d93feb19c53a225717e9bab3c07a4d43d0db6c1e9e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7600034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16d809268cdbfa4c23d3f7d2565d606d64bb001d6411cd110fb68596c24d8446`

```dockerfile
```

-	Layers:
	-	`sha256:eadeb8b4064e3496e9311205ea53b3f4a3c074b0563ec8535aadb1b07b4bd0ef`  
		Last Modified: Wed, 02 Jul 2025 12:42:53 GMT  
		Size: 7.6 MB (7585773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c75241023f4d675e8036ff1cf5d1fc950a1bac5f1873fc983034a707438dcbee`  
		Last Modified: Wed, 02 Jul 2025 12:42:54 GMT  
		Size: 14.3 KB (14261 bytes)  
		MIME: application/vnd.in-toto+json
