## `clojure:temurin-25-tools-deps-1.12.4.1607-bullseye`

```console
$ docker pull clojure@sha256:141bfa9b97230c625e73718543b26a41ca280ddb1c529bec5827b0c58806fbea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-tools-deps-1.12.4.1607-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:e61ac08922f9a64c76d36b394091ceb7b9dac7b9bb871f9c15a06b2718dd48d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.6 MB (215598693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:624ad561ce563b324d3c0f3aa06acec42e3e43db6f35880c3e774824ea965252`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Mon, 02 Mar 2026 19:48:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:48:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:48:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:48:21 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:48:21 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:48:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:48:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:48:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:48:34 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:48:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fd834ead99fe4ea0884686321217c38494a7a0c7327e2a5ed98d978011de7ddb`  
		Last Modified: Tue, 24 Feb 2026 18:43:07 GMT  
		Size: 53.8 MB (53756434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142493ddd96838a09e822278b10ace55843045a0dbbc7a658acf38a56839b3a4`  
		Last Modified: Mon, 02 Mar 2026 19:48:56 GMT  
		Size: 92.3 MB (92256277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304ae14774ccd697585b1ffcc98c84aef887032fbb0f743c40cd16a8515b618e`  
		Last Modified: Mon, 02 Mar 2026 19:48:56 GMT  
		Size: 69.6 MB (69584936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b2c0546985d5f83200781928f57b3a8917d727d03d388e19851c0c429b651ea`  
		Last Modified: Mon, 02 Mar 2026 19:48:53 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:208f8f569979547d4756283e3ce907529c3f27a1bd191af92c8781c85a829e19`  
		Last Modified: Mon, 02 Mar 2026 19:48:53 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1607-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:402085377472d22e05821ae660a305dd93e691fc091689b63a18b477af4669b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7393798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9263c35ec632bf5e996bd8d8c8d2c1663b1f0aa13fb5fd5adbbd4f63e136bd93`

```dockerfile
```

-	Layers:
	-	`sha256:8384cc172c1192353b80b60eb7f8465ca450dab0f652a270c697222920cd226b`  
		Last Modified: Mon, 02 Mar 2026 19:48:53 GMT  
		Size: 7.4 MB (7377351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab36643936a116472d540b94f44b4639bdd2e89ad1ed2a008e4908929b923733`  
		Last Modified: Mon, 02 Mar 2026 19:48:53 GMT  
		Size: 16.4 KB (16447 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1607-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:88622ad74050adc7248be58caa89bcc120cb39697fad854d0c3aa09f64d2147b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.3 MB (213273180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3254c8c57f1247fe313a098846acbc580f091bc13ec9804771bd82c42a85b2b6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Mon, 02 Mar 2026 19:48:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:48:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:48:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:48:14 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:48:14 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:48:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:48:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:48:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:48:28 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:48:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0509053f2cf8072309184287dd2fd397e589dc5db17a1ddc469001be80ea07a3`  
		Last Modified: Tue, 24 Feb 2026 18:42:38 GMT  
		Size: 52.3 MB (52258392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed32f54341c5f6e91646992c4ed8171f1a2939a5fa039ead15e7bcd75455c0f`  
		Last Modified: Mon, 02 Mar 2026 19:48:50 GMT  
		Size: 91.3 MB (91288304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddcd37050a03be62f46fb89effa262f469eb357b85042ce4cdec232e6be510f1`  
		Last Modified: Mon, 02 Mar 2026 19:48:50 GMT  
		Size: 69.7 MB (69725442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f4f266b9b145420ffee8dead808c220eb0d4b4a5e2e35c195c74a8b9004520`  
		Last Modified: Mon, 02 Mar 2026 19:48:47 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a81251e973b1527a1c0665cefaa89a9f828c9bbdcf4bf704c2a1e04fa4ac13`  
		Last Modified: Mon, 02 Mar 2026 19:48:47 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1607-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:91734189cc7e09a43d98f60ae107b26a672818ee557e2e2ce4ad4831ac07174f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7399060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5757189895334abf8bb07cf849963ff3f3a9485e360618645a02a735006e1543`

```dockerfile
```

-	Layers:
	-	`sha256:1a5445f28abce9f047d4f91b63a002a66058fedbc1b23759aaf90e92a3dd5a93`  
		Last Modified: Mon, 02 Mar 2026 19:48:47 GMT  
		Size: 7.4 MB (7382471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ddd4ac37575c1c743035541bf6e94f5c0a12b414e40bfc02a49d07a5444ac19`  
		Last Modified: Mon, 02 Mar 2026 19:48:46 GMT  
		Size: 16.6 KB (16589 bytes)  
		MIME: application/vnd.in-toto+json
