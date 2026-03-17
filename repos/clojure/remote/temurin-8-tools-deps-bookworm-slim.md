## `clojure:temurin-8-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:5aa029959f60d389f53e1e61f7ad7d3d782ff345f2ed471b2a2df7fa6e316167
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7aea941b03833e38f895ccca79539e15446be81e02504d0f3db0fdfe7a21332d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153108438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b8a85861f532c2bc6de464b8759230cc8627c4872ad7657a5fb2e073c01a829`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:56:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:56:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:56:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:56:09 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 02:56:10 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 02:56:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 02:56:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 02:56:25 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4277b26dedec6a4e710fb747cc087946362a748ee944533d09b45b5ef60cd35`  
		Last Modified: Tue, 17 Mar 2026 02:56:42 GMT  
		Size: 55.2 MB (55170146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2060fd3b7e00f35bbdfe6a4cb6b9b6c4953d9beb774770f3e83482d71b270f5`  
		Last Modified: Tue, 17 Mar 2026 02:56:42 GMT  
		Size: 69.7 MB (69701425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba58034cb475ce00e103a84c103e18a1942436479a7b9fc3fab566d57d2e821`  
		Last Modified: Tue, 17 Mar 2026 02:56:39 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d65e43cccb072ca2c26e15a169e9d37c2f722b45a02256b12d23c94ff58fbb28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5251402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:595d7b3c3a3c69a9b9d98f6c3a0eea62953dae46b952ad1eefb89bf5d8f09136`

```dockerfile
```

-	Layers:
	-	`sha256:3cc560d504dcd0fcef3441e826595bfd36f7201e21fb9e7f6b64e74cb0f64285`  
		Last Modified: Tue, 17 Mar 2026 02:56:39 GMT  
		Size: 5.2 MB (5237154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab60fa63e3d5aba3cb005efe87cb2dca61dd6cdd0ba568792ede54b5af908f75`  
		Last Modified: Tue, 17 Mar 2026 02:56:39 GMT  
		Size: 14.2 KB (14248 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ad901387d7ed50c8fe988929d93e5477d9dc3e488e8ee0766f5548bb9d7c6c90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152057177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b057972752df89a7648e94a81c1d9ea946f2503468b06783050bee2a86f1817c`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 03:00:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:00:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:00:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:00:38 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 03:00:38 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:00:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 03:00:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 03:00:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a3e6b072dc22aa4facd9121d8539874cd773fa8479c466607b0e913381c86dc`  
		Last Modified: Tue, 17 Mar 2026 03:01:13 GMT  
		Size: 54.3 MB (54251604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be058cf3bf87a44d6050e47aae610623a7aea8ed83633580b0b474e8a7ae2bd`  
		Last Modified: Tue, 17 Mar 2026 03:01:14 GMT  
		Size: 69.7 MB (69688863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a692ed3c68f58d28e31346ff867c041045195db1788846f1d9a929369b45e876`  
		Last Modified: Tue, 17 Mar 2026 03:01:13 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:926e99c9d1ee586d8ea105f2396e1d3ff3407ecc5c65eafb91e0a26c7bf1c623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5257981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f23e8c4c61181adefdd0b41ccffdc81e3b56c4ca0a89dd521d08450b217ab02d`

```dockerfile
```

-	Layers:
	-	`sha256:acd36bbdc4ee876c89b932b36719c2d9ba69b463e2ddd1feb14c89adda36912c`  
		Last Modified: Tue, 17 Mar 2026 03:01:14 GMT  
		Size: 5.2 MB (5243615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b05992d60747b97537614860a227e788bf05e237c1382b9dbf455e14b696c6d3`  
		Last Modified: Tue, 17 Mar 2026 03:01:10 GMT  
		Size: 14.4 KB (14366 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:339ba3bfd8fc60b812efbc5875bbc0d43412cbb14231c82d4157390584c63cad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.3 MB (160262856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af5b327ed690f8dfae4d1ef41ce463a7f5715e2b15969665b2ac7d4c2ab3a98`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Mon, 09 Mar 2026 20:41:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:41:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:41:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:41:37 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:41:38 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:42:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:42:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:42:14 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3def25e912c223ee8b3899e5ca048b2439f856f438ac690293817fbc0291fb36`  
		Last Modified: Tue, 24 Feb 2026 18:41:49 GMT  
		Size: 32.1 MB (32078334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd057b79f3d60ba47d0a93ff8e0542dbf45f859c8097f8afbf582b24f76e4b70`  
		Last Modified: Mon, 09 Mar 2026 20:42:45 GMT  
		Size: 52.7 MB (52650417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09063cc9838a8f760480bc034318b193aca1c37440905c5ccb3cfe17be7d37ba`  
		Last Modified: Mon, 09 Mar 2026 20:42:46 GMT  
		Size: 75.5 MB (75533459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:285e66c6c8b517ce531d0ce0ab6cdd44ae7764b544ec6303e8d6cd78cdd62a42`  
		Last Modified: Mon, 09 Mar 2026 20:42:43 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d53b109ce4c88acef14af0a68adf2e5271cf2e965f0277a02760a6a8ecd5b4a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5257203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55cc388db12db215e46c2479c544d30c49af4255ce6be2a68dbc37c82628f2d7`

```dockerfile
```

-	Layers:
	-	`sha256:ba173103fafa4153bb491274376bedbf039898853b7909a6c6212ab45d7832ea`  
		Last Modified: Mon, 09 Mar 2026 20:42:43 GMT  
		Size: 5.2 MB (5242907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5cd4b8b3fddbd0f696ec5c30a382db88f56e8550d08e1cf33220110ef83de6c`  
		Last Modified: Mon, 09 Mar 2026 20:42:42 GMT  
		Size: 14.3 KB (14296 bytes)  
		MIME: application/vnd.in-toto+json
