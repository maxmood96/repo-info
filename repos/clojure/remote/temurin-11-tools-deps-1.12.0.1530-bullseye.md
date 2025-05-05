## `clojure:temurin-11-tools-deps-1.12.0.1530-bullseye`

```console
$ docker pull clojure@sha256:51df521b3989cb435e78fe8e71de18f2b9a267a70ebf1a18fd4c1a5df034fcbb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.0.1530-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:fcbabf0c20f5b0d238e80798c90dae10194b57e408d674fb92f2340832eb5653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.8 MB (268780534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a0d7d8f9f5ed0649d0340f28af2d85d473ddf64152f2d1ebd1df2b81f7f46fa`
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
	-	`sha256:a1fd8ae85a2e253a4d448bf266b233c771a948c073c1b06e49cc201326e16286`  
		Last Modified: Mon, 05 May 2025 17:07:18 GMT  
		Size: 145.6 MB (145635734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22bfa5f1c8554371a2728f42f8ea6b0a781e158f21a2d68e6c1ff548134fae50`  
		Last Modified: Mon, 05 May 2025 17:07:18 GMT  
		Size: 69.4 MB (69396417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9923c8ee0bc818424da8897429c7de814ec00303a8649c4b88b3996908c4250c`  
		Last Modified: Mon, 05 May 2025 17:07:16 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1530-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:450cf9d4fc902ec1e3e7424babcd8d411841b82c47656f8c7be66fc34f278162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7240948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:807e4b176fafa16dec6413bdf54e519ea3cde147822a94673bbec0c5e6581c5d`

```dockerfile
```

-	Layers:
	-	`sha256:41dd9c0c29b25acdd4417b1f1b97de944cdc5ce28844dd61d57cade0f2419af7`  
		Last Modified: Mon, 05 May 2025 17:07:17 GMT  
		Size: 7.2 MB (7226696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4c3bcc7f2d1f4bd342dd963bc319377ecac9e07d57123acaf5e3e1baf75b2d9`  
		Last Modified: Mon, 05 May 2025 17:07:16 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.0.1530-bullseye` - linux; arm64 variant v8

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

### `clojure:temurin-11-tools-deps-1.12.0.1530-bullseye` - unknown; unknown

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
