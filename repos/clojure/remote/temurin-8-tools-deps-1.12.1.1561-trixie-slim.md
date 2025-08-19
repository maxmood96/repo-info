## `clojure:temurin-8-tools-deps-1.12.1.1561-trixie-slim`

```console
$ docker pull clojure@sha256:dc95e6a8f8b791e7cccc713cc208f5f4715627efd58c03575a2edde4d59daed2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.1.1561-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e8ef6363af1475907acb3763126743e70eb0f204f29c23522231a5c1d3dc6070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156394543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a4f30d51ef4383b4a9e25be8f70f2c95d4e7cf4994219625233acc28b5be877`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a2310ddb3c240b2cc693b69cd20f833f5a698083d6b2721eb3ac0723c23407`  
		Last Modified: Mon, 18 Aug 2025 16:53:09 GMT  
		Size: 54.7 MB (54731354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e396ab6e759f283b8dfee9588cba73606f8a403cbce229576aae8bf67a786871`  
		Last Modified: Mon, 18 Aug 2025 16:53:18 GMT  
		Size: 71.9 MB (71889257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac90baf8809cd0f9c2a98839d1ea394de4dac560581635d45ce26097c3163f5`  
		Last Modified: Mon, 18 Aug 2025 16:52:56 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.1.1561-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b485657a991d29b66a1163602ded67554ef834ba7a6c2632a31b79b636f5e21c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5391118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcf95877ab44ff5730752c2ed602a17c2334451454037161d3a38034c98e76d9`

```dockerfile
```

-	Layers:
	-	`sha256:6bf7700be80b40a17a1f6ed0dd2520f3e9ba2d9dd4dbebcccc07c1609af309ad`  
		Last Modified: Mon, 18 Aug 2025 18:45:52 GMT  
		Size: 5.4 MB (5376847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16fb5f613178c3da51d5ab0a79cba472c7f41756eccb8284739e73b705e21b42`  
		Last Modified: Mon, 18 Aug 2025 18:45:53 GMT  
		Size: 14.3 KB (14271 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.1.1561-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:16545dad13ef2e8989b3dacf772b80368451bef81435540fd31348baa0aea4d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.7 MB (155679254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf6ab7d980a7e13506415021a50d4cc2fde2aab312537e76f84da293f5bfb8bf`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6e947fda8da40bbdedae94665dc12b0f76d05c15bdcfed7d7c7a25a08a34d4e`  
		Last Modified: Mon, 18 Aug 2025 16:59:02 GMT  
		Size: 53.8 MB (53835656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0710da9dae29c42ba36fa99db20f4fe5ac03dff23b31dc475e325440db11964f`  
		Last Modified: Mon, 18 Aug 2025 16:59:01 GMT  
		Size: 71.7 MB (71706908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8890b43ed117764b178165ebf57829e1ed3466d5e61e8e07cc63a4cad8b9e6a1`  
		Last Modified: Mon, 18 Aug 2025 16:58:49 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.1.1561-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4f6e268e9018d6f983fb1befb3e86170c9aab37e03596c9275abb86f4feff9de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8cd70e367781e652567e6369b41c7b62762a044eedcc19db5565e879a69644c`

```dockerfile
```

-	Layers:
	-	`sha256:a8b8cdeefea9131388962b58a3521bdb58200dd0188640d8347f300d230517ea`  
		Last Modified: Mon, 18 Aug 2025 18:45:59 GMT  
		Size: 5.4 MB (5383314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59d86f419fbaf36693d9ca9f1d485274305ae4141d71e23addfb7a3359e5b369`  
		Last Modified: Mon, 18 Aug 2025 18:46:00 GMT  
		Size: 14.4 KB (14388 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.1.1561-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:c269bf69f1f896695e48fa2cc6218072507d1b5f06a43231cf54aa1b1cb6648b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.0 MB (163049444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2627ad3f6f5289e8df16365c8cd9a8980674a6905bd57062941e309ff85e238`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800d9364a2f77d9c82408af7eefafc8a1f6c3cba74df0771e743034519bdd812`  
		Last Modified: Tue, 19 Aug 2025 18:05:57 GMT  
		Size: 52.2 MB (52165401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518965a1d86a1446aaf5c60c956f1c69aebb89c93a7e812e7d77f4ed3d413918`  
		Last Modified: Tue, 19 Aug 2025 18:06:06 GMT  
		Size: 77.3 MB (77289183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec1b1a7093f5f91a9aa745caf70e20c30668c1bd5f177f606bc9d4a74a4e00e`  
		Last Modified: Mon, 18 Aug 2025 17:13:31 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.1.1561-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e8ee479b0af5e486dff8f33cfd46524e1959bff84447f799e3ebcddad9f86adb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5396130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6cd39b4677d5360aa4f88d1ec5b49e22d96b232e3505e37e47747b672ccd382`

```dockerfile
```

-	Layers:
	-	`sha256:86e857d55149d2da0e72b8aec44dfd65b914942b19953ccdebb56aa3d9a2d2bf`  
		Last Modified: Mon, 18 Aug 2025 18:46:05 GMT  
		Size: 5.4 MB (5381811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5b181fb1c751d853e7ae4dbe3050ceb85a1f0813a666e4645d2676eb5e1a258`  
		Last Modified: Mon, 18 Aug 2025 18:46:05 GMT  
		Size: 14.3 KB (14319 bytes)  
		MIME: application/vnd.in-toto+json
