## `clojure:temurin-8-tools-deps-1.12.4.1582-bullseye-slim`

```console
$ docker pull clojure@sha256:ce5f2dd7d31556aa963cb9d6c30adbaee42c8fce82f55051f4529e714998977b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.4.1582-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2d0f240eb6a43dd324bfcdb9bc49637c8cce47667f6eb17a1348508c98990241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144142425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7910bd519ba864164c42a8fc4e9bce62889cb45defce4ac5d3246fda0e3dae9e`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Tue, 30 Dec 2025 00:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 00:51:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 00:51:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:51:59 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 00:51:59 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 00:52:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 00:52:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 00:52:12 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:37b52eae712b138ea3c9639c687f975153ccba96801de3dc69883975843edb35`  
		Last Modified: Mon, 29 Dec 2025 22:27:47 GMT  
		Size: 30.3 MB (30258441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1748b24126873d66b8c0e615bfbf80ae8e1fd3d1ea6a0b297dfa8206e75168ae`  
		Last Modified: Tue, 30 Dec 2025 00:52:38 GMT  
		Size: 54.7 MB (54733365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba91d3d6524a7984b654330fab0dd52dc50ee0d7b46e2265aef0fe30cfe6665`  
		Last Modified: Tue, 30 Dec 2025 00:52:37 GMT  
		Size: 59.1 MB (59149975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da4923c221f8bc37c054cc9364c9a751440d5ff638010182900b591bc58ffbd`  
		Last Modified: Tue, 30 Dec 2025 00:52:33 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1582-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:da30c6f0ff88ca067070ef891bd1416ed9ae9a0c916cc17f0e4bbaf4cfbd4655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5443925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa5b2956b35afba893c8e43b4c709134f08829912bd7e003d4a28887fdc116a`

```dockerfile
```

-	Layers:
	-	`sha256:98be737d6b0e406fabf2cf52b7d32632d6bad87329cb6de896394c3787446835`  
		Last Modified: Tue, 30 Dec 2025 04:48:39 GMT  
		Size: 5.4 MB (5429677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fc522e27712503b49085a4927cd3fceea9ad2d07d70b0a3a2608efc1b908efb`  
		Last Modified: Tue, 30 Dec 2025 04:48:40 GMT  
		Size: 14.2 KB (14248 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1582-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4ed3d324568bd831dc140e23eed03394c4a4c1b994dc3d2075ba88cb729b9fe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141847918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27318f2df510a13df39cecbb90226ea4de3297cb46204bedccec0d86458fd755`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1766966400'
# Tue, 30 Dec 2025 00:55:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 00:55:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 00:55:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:55:06 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 00:55:06 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 00:55:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 00:55:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 00:55:19 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2b952d66bc8c719b5ca92eacb4307075591731bdc405a12ebd6fa840a24375b7`  
		Last Modified: Mon, 29 Dec 2025 22:27:18 GMT  
		Size: 28.7 MB (28748462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7358c636897e9612499e63bad23009ce45100404eead82f8d150dde0ef0e9109`  
		Last Modified: Tue, 30 Dec 2025 00:55:48 GMT  
		Size: 53.8 MB (53814993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eaa408de3a492624f74f3c915c5ed838081a19711a1c97a660e0a0b8b20652f`  
		Last Modified: Tue, 30 Dec 2025 00:55:45 GMT  
		Size: 59.3 MB (59283818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fd8ec5cb6874330d6f404cd091d94f0a005da632c5390541adb31cad506316`  
		Last Modified: Tue, 30 Dec 2025 00:55:42 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1582-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7667a5ce2d18f72d1eb92eeb3a0c170b7a7bed2042a80d8bfb8a16554a97bd37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5450473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f4fa07430c5353cb30640985b30e35373cba825420c9b6603ab7243a8c2e7d`

```dockerfile
```

-	Layers:
	-	`sha256:ae9f4cb6ccec8d2f162425c67f989836a002bd505b98f3c3980f5897656835c9`  
		Last Modified: Tue, 30 Dec 2025 04:48:45 GMT  
		Size: 5.4 MB (5436107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5d1039858d152fba5536dfa0ea4ed6a023a231a32af8211a9e10fcf10c6f9ec`  
		Last Modified: Tue, 30 Dec 2025 04:48:45 GMT  
		Size: 14.4 KB (14366 bytes)  
		MIME: application/vnd.in-toto+json
