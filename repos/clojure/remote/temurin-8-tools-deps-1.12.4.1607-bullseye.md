## `clojure:temurin-8-tools-deps-1.12.4.1607-bullseye`

```console
$ docker pull clojure@sha256:dc8912df9e3c20074b41a20435b8c3c0c0d9efb66c4b767a16e5b69a4da52891
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.4.1607-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:e3c28a9b84b3677c6bb745ae7b3714818608aeac81b4af47b97144c6348ab360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178512119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d499463fc705010572d96dc1f6eebf72b265c2145fc93fb9002c7abb1e45302`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Mon, 02 Mar 2026 19:45:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:45:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:45:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:45:19 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:45:19 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:45:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:45:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:45:32 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:fd834ead99fe4ea0884686321217c38494a7a0c7327e2a5ed98d978011de7ddb`  
		Last Modified: Tue, 24 Feb 2026 18:43:07 GMT  
		Size: 53.8 MB (53756434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3e223611d42c6c518074069186d83c8b12bab7a1ab35f28080cc97f46b3ad4`  
		Last Modified: Mon, 02 Mar 2026 19:45:48 GMT  
		Size: 55.2 MB (55170068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ebcba15e3dff27e7f06413d485ac678274aa23f7a6b9f64862b3899c38ecf0`  
		Last Modified: Mon, 02 Mar 2026 19:45:49 GMT  
		Size: 69.6 MB (69584969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab9bad4869233cf5772132402e6bd2c04206e2a95b75ad1dd9c1aa9351420ba`  
		Last Modified: Mon, 02 Mar 2026 19:45:46 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1607-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:2f3f7ff0dd52745ca3fc37427c701c0fcc8ba9f47a64f76163601b7fa9e38f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7544458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ae86bbe6497f09e3b566b52026acce642b02b594c23112ffc630e104266594e`

```dockerfile
```

-	Layers:
	-	`sha256:1af5d0ade995410f95aa37da6335f04bbed1522a256b6eb45b1caf9464b1308c`  
		Last Modified: Mon, 02 Mar 2026 19:45:47 GMT  
		Size: 7.5 MB (7530264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86e48f500b322443eabe1c84cba8724604b2f7f40b72aa649912efba00bf3458`  
		Last Modified: Mon, 02 Mar 2026 19:45:46 GMT  
		Size: 14.2 KB (14194 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1607-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2f4f50cf500fbb3b78f5ba8523581dfb0ed885562e540c809f1ad5527c8ceee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.2 MB (176236282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a59fcbc0723cd014e63a79a0e5e9233900a2cbd66063a82ac6ecfabcbe74cab`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Mon, 02 Mar 2026 19:45:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:45:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:45:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:45:10 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:45:10 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:45:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:45:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:45:24 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0509053f2cf8072309184287dd2fd397e589dc5db17a1ddc469001be80ea07a3`  
		Last Modified: Tue, 24 Feb 2026 18:42:38 GMT  
		Size: 52.3 MB (52258392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1a8984de4108197ecc995b132f7ba7282586e3c00f14fcb950ccf80f31152c`  
		Last Modified: Mon, 02 Mar 2026 19:45:42 GMT  
		Size: 54.3 MB (54251614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed4146f52d1f1e2db0fdf36b798288b80ba1a74831acd2cc1c1df19a38f8fec`  
		Last Modified: Mon, 02 Mar 2026 19:45:43 GMT  
		Size: 69.7 MB (69725628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2253f2b1cc074f16dd8c08eccee44f979d1f529fd51a69ddbb38de8fb48f58`  
		Last Modified: Mon, 02 Mar 2026 19:45:40 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1607-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c240398d52fa7bd9262b05763e3a2df69ea3dfd69b789851b6fd5270fdd81cd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7550374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b150019e0a8b1f3b0cc841e7f46e2b459bc2db8717a66006c33934fbb574592`

```dockerfile
```

-	Layers:
	-	`sha256:bb93574c14ce2b28592b02c2020065a692f33445f18addb511482891a7b7e984`  
		Last Modified: Mon, 02 Mar 2026 19:45:40 GMT  
		Size: 7.5 MB (7536063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10cb1f3418bc74f31317a6ebd92c6c2dc0bc40fa6cea647791338b37505b8b25`  
		Last Modified: Mon, 02 Mar 2026 19:45:39 GMT  
		Size: 14.3 KB (14311 bytes)  
		MIME: application/vnd.in-toto+json
