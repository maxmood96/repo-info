## `clojure:temurin-11-bullseye`

```console
$ docker pull clojure@sha256:c7cbafa8a063b7addb465d1181dd0733e4ed00686b3acf0faeb06e445f40712d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:14d84e4d984148e6e41c782ea3d90800cd6819e951263a777f3952d9f2ff72a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.8 MB (268778153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c9ab4bba702a5209b0f1301c5da8c02543e964dd90361853819cf7f5981e85`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
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
	-	`sha256:19f1f54854d69811b3745bdd374e863f2fc2dc765fe37d1a30df3e590273322b`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 53.7 MB (53747740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1129f5a88aab2573b6f924e429ed0a9d975e6438ddf3ff9813952b0b450d4b63`  
		Last Modified: Mon, 28 Apr 2025 22:06:57 GMT  
		Size: 145.6 MB (145635848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05add4e5f3735b4b95fbdad491d83abb30c0080b5a6e398c906b1af4df0386e8`  
		Last Modified: Mon, 28 Apr 2025 22:06:56 GMT  
		Size: 69.4 MB (69393922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5ab1427222dfb58935ff50bf704e8765a3aff7dc65d536157283e67a8e72ee9`  
		Last Modified: Mon, 28 Apr 2025 22:06:55 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3467c62fa939fce2d78b3238534592efb3a1e6d0918a7df8c9ba460e6b8646b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7240948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d82a15cd5d60a11b3c256d73935f803246f943decd99dc2fd5a2d00d13e014f8`

```dockerfile
```

-	Layers:
	-	`sha256:1b648c77bc6c3a947a188ddf834cfe61a2d1272fe07456c0b81bbba6148ea1b1`  
		Last Modified: Mon, 28 Apr 2025 22:06:55 GMT  
		Size: 7.2 MB (7226696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc76e6ebe59184abc22dbb3865e4bca4cd426f8a6e8268b8e2d2d41bfa830aff`  
		Last Modified: Mon, 28 Apr 2025 22:06:55 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f90bf53dc71b8e037e9303709ef9ca011c0658bf344da63db50cffcac4c72c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.2 MB (264197970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ba834a4b322b42b7604fc6e081cf3821fdf87bc49a9162831ddd51d1fca7f7e`
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
	-	`sha256:759e4ad874f5777fbce652a7c935712ffe5414d948698ae7d54c4a184278b915`  
		Last Modified: Wed, 30 Apr 2025 01:06:10 GMT  
		Size: 142.4 MB (142422081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b94033bc39922dcd0b56f56688ab012059f5b9b3f9fe81545120b1cb7949673`  
		Last Modified: Wed, 30 Apr 2025 01:08:59 GMT  
		Size: 69.5 MB (69529268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e48ab5a03e933f87f10ab58a66dcc1d6d9e03fb1c24bb147e0951aa4dacb0fb2`  
		Last Modified: Wed, 30 Apr 2025 01:08:56 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:08e160f4c422ac2d33c5e294d34150b8c619a44c993338c48d7881cceaaea333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7246782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f28fc362862f035d1fb6d391077e94379d492789e925d25f365ddc10c5e1447`

```dockerfile
```

-	Layers:
	-	`sha256:17631fdec6c59f9b3a5ab5e2eacefb2b572f4b0cb46d285056794d09a6aa6121`  
		Last Modified: Wed, 30 Apr 2025 01:08:57 GMT  
		Size: 7.2 MB (7232413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80a18b475f85300c9407a542847dc84880c615933d42285c51a183960f7d715f`  
		Last Modified: Wed, 30 Apr 2025 01:08:56 GMT  
		Size: 14.4 KB (14369 bytes)  
		MIME: application/vnd.in-toto+json
