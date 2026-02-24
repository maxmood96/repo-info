## `clojure:temurin-17-tools-deps-1.12.4.1602-trixie-slim`

```console
$ docker pull clojure@sha256:952b7b1dd619a3c98a45d627bf6a4cf780548919080cefd161137a928e3daf1a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3b604b59b0ff2d3599164c6b457290cfc8a6e0706996603ca45c519550b97df5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.4 MB (247402410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a186ec081408bf7c7e40ef585a36149d36550ec53881ae9e6037c805be44788a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:55:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:55:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:55:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:55:18 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 19:55:18 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:55:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 19:55:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 19:55:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 19:55:34 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 19:55:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e063e6e49615f7a5574c3eb139386789087166d9e1f60b2cf3cb655881f83e7`  
		Last Modified: Tue, 24 Feb 2026 19:55:55 GMT  
		Size: 145.6 MB (145628716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44086dab13d013e7222b245e8ea34f4547d51000c72425763551f7255ba8b3b2`  
		Last Modified: Tue, 24 Feb 2026 19:55:54 GMT  
		Size: 72.0 MB (71994021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df919d28368af3a30c17e7018b7dd2c0e9bd1b80ce772a81423c27bf1b88a344`  
		Last Modified: Tue, 24 Feb 2026 19:55:50 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb103d80d81e8cfdd901bef51d9dc09bff8a90c80a10c29dad9eb67845b41b4`  
		Last Modified: Tue, 24 Feb 2026 19:55:50 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4610bd79c4065d77eec1ba4979d0a3969cb7f8736c850b6613b4a369d2d40d8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01bd45e685f6a1816cea2cfd74e9b38dd2d737eff94f252e97eb76bc0cb29d31`

```dockerfile
```

-	Layers:
	-	`sha256:8a00fac21784ef906f222e6150a22e41c289c5a3c7dda56db5982fec9503f820`  
		Last Modified: Tue, 24 Feb 2026 19:55:51 GMT  
		Size: 5.3 MB (5257551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0735a14b7946c68415f55dee75b0c699f209b3708ddb4c796024d6b536c9201`  
		Last Modified: Tue, 24 Feb 2026 19:55:50 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b194b2e06eb9bb450119707b163e074dcae5d7f8bf4b108fe98f5a3214d4a940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246385470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b5cc523453d3d3b17c705360d627515b9c7df85ecd76a9e848eaee6cb9e4bc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:06:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:06:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:06:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:06:01 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 20:06:01 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:06:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 20:06:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 20:06:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 20:06:19 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 20:06:19 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be33b841005118b59a7e12d2bac78b2346ecd05133d16ed3b21f62309455ded`  
		Last Modified: Tue, 24 Feb 2026 20:06:41 GMT  
		Size: 144.4 MB (144436218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c595c67dfe9f81a6b1c2079ae9cf6d63f04a3a3983516e49c72c75d2f68cc4d`  
		Last Modified: Tue, 24 Feb 2026 20:06:40 GMT  
		Size: 71.8 MB (71808114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab006694edc12d601756e1e45e03e5c396979943fcdea6ff83a8ccee523c2d32`  
		Last Modified: Tue, 24 Feb 2026 20:06:37 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5049c33d948d5f25b28d3fde9c3cfd7da2be92b56a26046f3020b66444801c85`  
		Last Modified: Tue, 24 Feb 2026 20:06:37 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4d24f5f285b1e8e519fb7331b9be8265e2c82c033ada6c81ef9be90e202dbef8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bf3d40de7994a6c86bd509be18680212258f5150819cb7e7d2010c62ec29a5a`

```dockerfile
```

-	Layers:
	-	`sha256:69d9c7f03a32e8e5ea3e5f05037cab412d1ddb67dfeef2fe6127ff3de1d9af17`  
		Last Modified: Tue, 24 Feb 2026 20:06:37 GMT  
		Size: 5.3 MB (5263320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d962dd89f76e9b88de1c0b97542f7842f28ae04f90b9b6aeb008f86c0693ea35`  
		Last Modified: Tue, 24 Feb 2026 20:06:37 GMT  
		Size: 15.9 KB (15930 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:32fc99df7004793ccb50b07fdb9e541cf0554219ed0ff5ad0e05336113e7315b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.4 MB (256430064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:debba341be1cb7054aaa5833c40de715b7805ca69facba86dcb62e602ff91f82`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 23:48:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 23:48:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 23:48:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 23:48:37 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 23:48:38 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 23:55:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 23:55:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 23:55:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 23:55:50 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 23:55:50 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b4cabddd66d71e97ccb04d7861e4511a418edbd43a9f1a73ba473b7207138b`  
		Last Modified: Tue, 17 Feb 2026 23:50:19 GMT  
		Size: 145.4 MB (145438194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:479b8954710a381283bd468d798f5303d2096d2a39046377114ef33ec15c609b`  
		Last Modified: Tue, 17 Feb 2026 23:56:36 GMT  
		Size: 77.4 MB (77390640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60027f35b226184dc9ffa079a19a29ab0a18cd7c13c9e6e5d85519246f1a5f28`  
		Last Modified: Tue, 17 Feb 2026 23:56:33 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae140fcd67828b0c5d3cabd2abe5e0b320de4095266766959b5dae19a838e093`  
		Last Modified: Tue, 17 Feb 2026 23:56:33 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:52637576e5cd2f51009f2577e1fe63a3dea7447bbd080514e09a4612d0199e2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5277782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e958b28f705a19459ecab55ee4ddf550775db23505c62184fe2d401c5eca4c0`

```dockerfile
```

-	Layers:
	-	`sha256:01c28f61c7e6a2eab36c249cc4923ee994f778e8edd35ee0fbf836d10173e97c`  
		Last Modified: Tue, 17 Feb 2026 23:56:35 GMT  
		Size: 5.3 MB (5261922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47d384be72338e2e12d0d8cfde0f8633fd3b845d664ff6ae8a341c1b5aea85f0`  
		Last Modified: Tue, 17 Feb 2026 23:56:33 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:af348c4d6c0f65de46a77c14346dba72a3050ce1a8865a671c31318bf36dcff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.8 MB (241819580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5029c4736ff9d8744aa567dea4a5dc00df7d9a195992ea5f59651b2841c99df4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Wed, 18 Feb 2026 10:26:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Feb 2026 10:26:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 18 Feb 2026 10:26:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Feb 2026 10:26:35 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 18 Feb 2026 10:26:36 GMT
WORKDIR /tmp
# Wed, 18 Feb 2026 10:49:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 18 Feb 2026 10:49:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 18 Feb 2026 10:49:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 18 Feb 2026 10:49:29 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 18 Feb 2026 10:49:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4526db52defd9278f79daec64ebfa633041460dbe0cfad19564ae34d84b13b4c`  
		Last Modified: Tue, 03 Feb 2026 07:14:46 GMT  
		Size: 28.3 MB (28276389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:111103a58980758fcdb9577cdd1fcdb21280530f3d9c80e1e1c9faa138061546`  
		Last Modified: Wed, 18 Feb 2026 10:32:31 GMT  
		Size: 142.7 MB (142663128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf704af8904967b79a0ea75e952ff5340cc816742c921e18ef26305dfef02193`  
		Last Modified: Wed, 18 Feb 2026 10:53:09 GMT  
		Size: 70.9 MB (70879019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e45872d2dbd811c995a73ac5bb28e8e959f488af648d42761bd5522b62bc687`  
		Last Modified: Wed, 18 Feb 2026 10:52:58 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b16b08ff5514e031f4f82915e84fbe269c8ce5b718d849465c56454d50c4093`  
		Last Modified: Wed, 18 Feb 2026 10:52:58 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d96e35fd556385a58f585810d10cc7e8e46c434413f924945141c347b426e51b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5260956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ac39f68057fc0413aaa528066d1e2be032a6d9c23667fafdb828fa1f1bccbd5`

```dockerfile
```

-	Layers:
	-	`sha256:694e2203b6ad1ec646916351629ce5cf52fc1c3fd4cd5c57f2e4c03d6dcac85a`  
		Last Modified: Wed, 18 Feb 2026 10:52:59 GMT  
		Size: 5.2 MB (5245096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:544b32ca4f657aac7c2d561695b5ec21a9a09a8bc08fb7d1a8f9c11b587d5c9c`  
		Last Modified: Wed, 18 Feb 2026 10:52:58 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:218771d233622249352b7ccf26a556e690ce0847994162e4a9475cf666c32ad2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.4 MB (238419604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3794903947281247110400d363f7849e62aa04351f72a6d507b035ba87999862`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 22:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 22:09:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 22:09:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 22:09:56 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 22:09:57 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 22:10:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 22:10:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 22:10:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 22:10:49 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 22:10:49 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868d422d07fcb06624c9f60a8bf6f9f34a34f93817bcffd68a63a327f55e0e11`  
		Last Modified: Tue, 17 Feb 2026 22:11:27 GMT  
		Size: 135.6 MB (135627116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c17c1183193c041ec3764df19830c9587fc669cf2770effc4c4833c803cf66`  
		Last Modified: Tue, 17 Feb 2026 22:11:26 GMT  
		Size: 73.0 MB (72953294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b29b8554d465b41e1bcfe94293af85dc17dc2fe69019991c3383337baae8414`  
		Last Modified: Tue, 17 Feb 2026 22:11:24 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4601a146539f9e1c6f5c867c2069033727ba0ba1d8863fbbdfd9fcf0bf0c21e8`  
		Last Modified: Tue, 17 Feb 2026 22:11:24 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3266e5469e9a45972a492722a52add353955a2d4cd2611e0b6f0fe7b3daafcc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5269286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79bf58067d0a6459d528b8d197ba20ea35175334a851316d365374542fe1d32d`

```dockerfile
```

-	Layers:
	-	`sha256:c57b4361365acdec3c71adc6717c78f20fbcae89b89bed5cbda534a9cfa59bc0`  
		Last Modified: Tue, 17 Feb 2026 22:11:24 GMT  
		Size: 5.3 MB (5253475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fde5135312fdb61f0c63e52b75ef214d1df0f2550f4e5d48983d8ef67264b2f`  
		Last Modified: Tue, 17 Feb 2026 22:11:24 GMT  
		Size: 15.8 KB (15811 bytes)  
		MIME: application/vnd.in-toto+json
