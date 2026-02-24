## `clojure:temurin-21-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:53fa3877e66f7ecbfdabe47422b6dfd4b76bdcf436c0e5125913e00d71af8f59
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:bdba67e045f9363b363fd1b406630584d5d69ef8d1b4add3be0d16eae95c7641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.2 MB (281182459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2be3d721d41b7b5c25102341229fb4fbd8ef11f806bf3c1ceda035817109efd0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 19:56:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:56:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:56:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:56:26 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 19:56:26 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:56:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 19:56:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 19:56:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 19:56:39 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 19:56:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fd834ead99fe4ea0884686321217c38494a7a0c7327e2a5ed98d978011de7ddb`  
		Last Modified: Tue, 24 Feb 2026 18:43:07 GMT  
		Size: 53.8 MB (53756434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9be13993c4dd5fa235899e23709c89c49fe153ffbac0a23ff289bb4d05004d`  
		Last Modified: Tue, 24 Feb 2026 19:57:00 GMT  
		Size: 157.9 MB (157857047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecf17f8330cb8a9696537de7a9b591f1c23aaad79293c95ecf50bed08824ec80`  
		Last Modified: Tue, 24 Feb 2026 19:57:01 GMT  
		Size: 69.6 MB (69567939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2347fd19112eca64ff4df5d4daba81a630bd9d4fe733a5208c77310e72846ef`  
		Last Modified: Tue, 24 Feb 2026 19:56:57 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ff2c926597904135f41687f28375a01a75ccceef65a63e5958fe40c0c34a05`  
		Last Modified: Tue, 24 Feb 2026 19:56:57 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:7ab705feba5d06989fce374d28df31bd59c527e1d4e578ba9691d734c8715359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7425394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a17379c439feafcbe7d429110ba4b49c1701cb3b5d6badb80ef4ca52519367d7`

```dockerfile
```

-	Layers:
	-	`sha256:0216065c4c18c665231377b707991889f947cee046ddd384261fa70ddd596c35`  
		Last Modified: Tue, 24 Feb 2026 19:56:58 GMT  
		Size: 7.4 MB (7409616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06963159dd53fee10118120527fe578722c3bf0de0ed0277dd719187f741ab40`  
		Last Modified: Tue, 24 Feb 2026 19:56:57 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bb17c4338d06c894a10a8c1559e4ccf9bdce0a402706001c7133a2af7b3aff7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.1 MB (278100774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:351733896c706bfe0dd3ffbf783a0b99ddd52976ea45b60414e2ce70d80896ef`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 20:07:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:07:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:07:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:07:05 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 20:07:05 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:07:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 20:07:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 20:07:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 20:07:18 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 20:07:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0509053f2cf8072309184287dd2fd397e589dc5db17a1ddc469001be80ea07a3`  
		Last Modified: Tue, 24 Feb 2026 18:42:38 GMT  
		Size: 52.3 MB (52258392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27fc4b30486487defea7fe98cf82424566b692dc86819b69402bc699022c728b`  
		Last Modified: Tue, 24 Feb 2026 20:07:42 GMT  
		Size: 156.1 MB (156133056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601749dbd57dc4d9b67979fc954c77d9f17840bf13a86adcb6d2a8626d2d9c8f`  
		Last Modified: Tue, 24 Feb 2026 20:07:41 GMT  
		Size: 69.7 MB (69708287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9f747d1920f63e23df08a57168ce981b3d578a68a0c4bf528789016b2021a4`  
		Last Modified: Tue, 24 Feb 2026 20:07:38 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4852a2b2c24b75297644b2582bbd40a7339952bd5984f2aba9fd5af724be5da2`  
		Last Modified: Tue, 24 Feb 2026 20:07:38 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:37e61bfbd0f379bacd02aac722f9530a29019154860a76bdbeb72223a9336e04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7430611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771fdffc7578ae865c0e406aaafe32992c961ef0ed544f46223bcb24904db62c`

```dockerfile
```

-	Layers:
	-	`sha256:122247fbf926b7a720232a37a45ca79c8659264616fee6feb3c56edb7ace0e6f`  
		Last Modified: Tue, 24 Feb 2026 20:07:39 GMT  
		Size: 7.4 MB (7414715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb619e4f5e186f490dfb69d23a3373ba7f5cc698b6539849315ca2d32c94fb86`  
		Last Modified: Tue, 24 Feb 2026 20:07:38 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json
