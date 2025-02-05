## `clojure:temurin-21-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:ce54687ccb470bc9dad83890ba90ee9e8550b814cca9a5bf7633d9580fb6fdd9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bullseye` - linux; amd64

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

### `clojure:temurin-21-tools-deps-bullseye` - unknown; unknown

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

### `clojure:temurin-21-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ab118dc365dcb2dce86c9a6ecdc4e3287b62aa6b707317e94f96e0a152b60b13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.4 MB (277417546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63e3ac97a90ff07d9932028ed99e6fe66e71743238a813065cc6ffbfdfa1b00`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 29 Jan 2025 19:11:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
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
	-	`sha256:0038ef039a89ede34c57806e684dc9d9be7dcd22d3c08b90deb36bb22a2c7122`  
		Last Modified: Tue, 04 Feb 2025 01:38:11 GMT  
		Size: 52.2 MB (52245695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f54403f73300528ff748016d5f4c0d03ec3baaa58bb823c88b921db621de9ef`  
		Last Modified: Tue, 04 Feb 2025 23:53:08 GMT  
		Size: 155.9 MB (155859278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa506db1a1f773207a04bc7b864aeadff780f1d4fc9eb05cd12f8d0b30755d89`  
		Last Modified: Tue, 04 Feb 2025 23:57:41 GMT  
		Size: 69.3 MB (69311535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49589aa1b7eae6d64040375cf0c4d99bfdf47012d5434f35fe846021c70de3b5`  
		Last Modified: Tue, 04 Feb 2025 23:57:39 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a7aec58d21ea7ad2d1ed789a0e97e26af120048a0a818c9258b7756c9d8d2c7`  
		Last Modified: Tue, 04 Feb 2025 23:57:39 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:1a3ae47a8db51edd94e3207feed0928d9d45cdd2e1ac896cae7043623f6d3763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7230095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:349f4dea4d4542df65b318101b3d773ac25270295ad2b200bcb0928715a3a773`

```dockerfile
```

-	Layers:
	-	`sha256:f4eda3fdf64bcd51f6cb97f54b79533d2a77b2419b047033de4ff663ac8cb3fa`  
		Last Modified: Tue, 04 Feb 2025 23:57:39 GMT  
		Size: 7.2 MB (7213456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cc23f0d62da2036a255505f71ba1d3573795ead3a47489362e802c5ee566b2b`  
		Last Modified: Tue, 04 Feb 2025 23:57:39 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json
