## `clojure:temurin-8-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:726bb62e9cde3e043a8fa173a459ce142c8b4b96de7abb0aa008e90ebbda5d09
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:0bc71a21d0e5306655880efac127a4568638e15e5295eda7db9da47506068e6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.9 MB (177865320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f30c2f903abcf09652f9589f318a30f5201ee2ccce57a151ac8c1e4a94bbf039`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:54107f2de180b7b6e9f909d2f1c6c18e10c700a6bd80a035d931768b06bb2905`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac6767fa03bce181cd3d1f18316eac49fed96a79803a1e857b523a4846a99a91`  
		Last Modified: Wed, 21 May 2025 23:32:05 GMT  
		Size: 54.7 MB (54716179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55d90466c06702ae2f5bf261551beb70d2008069edab08d3380e2f02cc310a1`  
		Last Modified: Wed, 21 May 2025 23:32:05 GMT  
		Size: 69.4 MB (69398302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f87f195df8e2bbc25b55ef99780b2b589160e098b832ab0117d781226d4a51`  
		Last Modified: Wed, 21 May 2025 23:32:03 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:658b862f508d74958fa80ddbcfe9360d48256445341c06cdb1c21e4dc0c4ee4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7390437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8274a3e27588212faed155c0d2d68318765b8c8f9b484d8486eddfad14bd7b6c`

```dockerfile
```

-	Layers:
	-	`sha256:80c391ac80df48f931f9675f01b4be3383662fcd39683402291abb0baba3e93e`  
		Last Modified: Wed, 21 May 2025 23:32:03 GMT  
		Size: 7.4 MB (7376200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b901fccf73d0222508cf2b2b366d2a99eceff5365542fe4a681bbc596c02997c`  
		Last Modified: Wed, 21 May 2025 23:32:03 GMT  
		Size: 14.2 KB (14237 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:85edbd79b5576371b2f274375a948eeecb6164ba8ff04a8292dc474dcc27bc77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.6 MB (175606544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ccc1f83c101bcfa59dd1a7aceaec0246550b4ada3f66a3d7dc72d3bd02baf93`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9ce0153b823c3af508e9c8a003aa35daca140e8f4578ff2a451ac20469ea739a`  
		Last Modified: Mon, 28 Apr 2025 21:20:53 GMT  
		Size: 52.2 MB (52245979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb2f48618bca1674b7b6aa07975908acb6ec1fe86ee6887bac65ee97038b811`  
		Last Modified: Wed, 30 Apr 2025 01:00:11 GMT  
		Size: 53.8 MB (53830504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c26e7b04f99c52caadba553fcd81233a2492476f261a1074e6c733d82af737`  
		Last Modified: Wed, 30 Apr 2025 01:03:00 GMT  
		Size: 69.5 MB (69529418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858e98eeeaf032740cb7e020b8c57695762b31bdab37630402b65926c6c46aa3`  
		Last Modified: Wed, 30 Apr 2025 01:02:57 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:a40e7753436a449003c0c3012dd4bd25d433ffe4892ba7d39f67d12c0d8203c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7348317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af411b455dd5e06c89c3ba876a68ef365c32c24cc6b1780f43d2a355ca69e746`

```dockerfile
```

-	Layers:
	-	`sha256:069b334ff466e54f494eaf23e35ab2f4c53a44f2632696ef45d35ff74ce2e879`  
		Last Modified: Tue, 06 May 2025 00:20:27 GMT  
		Size: 7.3 MB (7333962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58d0ebc41b7f6720e0331888f132aaff0ef4f45fbe7d3e1d373afa09376d6be6`  
		Last Modified: Tue, 06 May 2025 00:20:26 GMT  
		Size: 14.4 KB (14355 bytes)  
		MIME: application/vnd.in-toto+json
