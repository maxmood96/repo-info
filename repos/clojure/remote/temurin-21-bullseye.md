## `clojure:temurin-21-bullseye`

```console
$ docker pull clojure@sha256:7f5cc364d7fffbdb07c697e965a4d207eaa97491319deed94d219d989dfb06dc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:9fc33831c27afff62e8a9dc3aa8d741f9ae1032af5b2fa37493b832e11ebf850
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.5 MB (280516926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54d4778742873444159c1265335fa2066bb0cad380b5143e9ad7644d53e40cf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 29 Jan 2025 19:11:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:478cb73646107d7b3f891aa53abaed926667463844c07b1d924bd760ae03f38a`  
		Last Modified: Tue, 04 Feb 2025 01:36:37 GMT  
		Size: 53.7 MB (53738873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6abc1c181c1449af26b030b9b0f8b1bc07de21603f9bfc4163b7b2364f6e9fd5`  
		Last Modified: Tue, 04 Feb 2025 05:21:24 GMT  
		Size: 157.6 MB (157585860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3903c505ae230c49e7f1d6d7c12b07b0f54e3ea22765addf61604bbf1315554`  
		Last Modified: Tue, 04 Feb 2025 05:21:24 GMT  
		Size: 69.2 MB (69191155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a693193a0fbb85e0226e632da5f7f5f41f15f70f00433157e68357824e926024`  
		Last Modified: Tue, 04 Feb 2025 05:21:23 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3fe756e897c671fc6fe2c9bf51f8c3858f18de383c5b836ea326ab3e13943e9`  
		Last Modified: Tue, 04 Feb 2025 05:21:23 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:288eb4d7a16cd7c479082dff0e9e49aec2fccf4c9e4f274c21111bde3217bde9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7224829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f7032451979a63362daefaf151aa634b6768b7919588251517e0d617e1eeb29`

```dockerfile
```

-	Layers:
	-	`sha256:aa9d72f44fb44b57269c3bce5bc1b708cccee192a108f01c09ed6170d4004e4d`  
		Last Modified: Tue, 04 Feb 2025 05:21:23 GMT  
		Size: 7.2 MB (7208333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da79b8adff63498e4e225033216a9f8e673d9a0a356c1f91c71cf889c93db3eb`  
		Last Modified: Tue, 04 Feb 2025 05:21:23 GMT  
		Size: 16.5 KB (16496 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d3548e9f04c96716c659fd064e631d3f9e7c51e04d97f1a7ef5cd99dd1bf1c7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.4 MB (277417949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:082d5f1ee1380c46b137240b782b550d8c18a907ef72be6dad45f49de9d28b42`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1270858b2b9cb5d47abd119b946534b70ff7d09f29c425fc07b280e5c28971c6`  
		Last Modified: Tue, 14 Jan 2025 01:36:12 GMT  
		Size: 52.2 MB (52246060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b9222735831f6fd3481eee72a48b5b08e308836b70040ea266b1e403cbd850`  
		Last Modified: Fri, 31 Jan 2025 05:20:59 GMT  
		Size: 155.9 MB (155859332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555409a38646bf01dfbe0ca368bdb229544c07810ad8271d48157b2305d941fd`  
		Last Modified: Fri, 31 Jan 2025 05:25:41 GMT  
		Size: 69.3 MB (69311514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03148d0ee9271bbdcaa536f5ebb788acd6211bcfccf57ac03bc12e0f0b3397f`  
		Last Modified: Fri, 31 Jan 2025 05:25:38 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8264ef43930e45e47d9bfda11c05df68c1579456ba76403578f5acd0bf0158e8`  
		Last Modified: Fri, 31 Jan 2025 05:25:38 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:e78ae47d7198403eae19e4c185c18be7f877a5af3fe57df174ef439816b2212e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7230095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0be9af588697a614db490c57fb9198fe1d629b536b426b715330258640101675`

```dockerfile
```

-	Layers:
	-	`sha256:4a85b9816bdc9ea2c0c5de18d3a82a6cadaf453a0363c5025e17d22c834f9296`  
		Last Modified: Fri, 31 Jan 2025 05:25:39 GMT  
		Size: 7.2 MB (7213456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e244d3233796e31dde470ea91a745f8672369add98d9538a0c5ce714cdbd658a`  
		Last Modified: Fri, 31 Jan 2025 05:25:38 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json
