## `clojure:temurin-23-tools-deps-1.12.0.1495-bullseye-slim`

```console
$ docker pull clojure@sha256:aac60e60fcdebcc683b9188d4dce94c4b0e264fb93312b58cdcca06aa78706b3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-1.12.0.1495-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2dc6642348b64a27accec66d6fff41a41907237aea2e1e147cfdfa76da851544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.3 MB (254329596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60533e4bc6085e2178ab3961afc365ffc3d246c8137958050d06920457588f2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7740923aa31c7a87f3318b897684df83e03e82c6b0e153d68b98a1808330951`  
		Last Modified: Tue, 14 Jan 2025 02:45:33 GMT  
		Size: 165.3 MB (165295114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce9fd444573c89316950ac245110232334422402100559865f6f3872685d8aad`  
		Last Modified: Tue, 14 Jan 2025 02:45:32 GMT  
		Size: 58.8 MB (58780775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb567dc3ba4cc3a767935318ea446c62498fb9ad1d21adbb0effd58fda6d689f`  
		Last Modified: Tue, 14 Jan 2025 02:45:30 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64830349e211dde761879244558d2442aa829886e5e4ff43ba83438f4f002131`  
		Last Modified: Tue, 14 Jan 2025 02:45:30 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1495-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4b616b94d4ecc1fe1ca99ebdceda2c9c792007818a302864e831044070e38c3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00fd9ea415cb82e55a60d61f5dcc0e74e46002571374c5d4d07199e98b75ba4d`

```dockerfile
```

-	Layers:
	-	`sha256:7cdd0cc27536f83dd3ff25f7dd0fcb1879b77cd485b1c766d8a385589ae9a830`  
		Last Modified: Tue, 14 Jan 2025 02:45:30 GMT  
		Size: 5.1 MB (5122074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf9a39753c62d95b52e692b85225e4cc5293789f8f91dd6fdf8cf1846b058e08`  
		Last Modified: Tue, 14 Jan 2025 02:45:30 GMT  
		Size: 15.9 KB (15878 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-1.12.0.1495-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fdfd694d95329fbda2a328b82e0a33e392bb85499608bda68e0a780d19ace9d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.9 MB (250932894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:630891409a092f01300c1a67a36e4a917ee4d7aefe42ea218e96cc1ff44f611d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:879a6187682fc52c69294a2f450abdb54e257a50e8133ec6e89cb140345be6ce`  
		Last Modified: Tue, 24 Dec 2024 21:34:50 GMT  
		Size: 28.7 MB (28744853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5b4fb805b80b71c3e0694a62a0807be3fbcc30b4f67cf6fa8370c3421f0982`  
		Last Modified: Wed, 25 Dec 2024 07:39:53 GMT  
		Size: 163.3 MB (163281786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22bec54235a6d96df2358ef1c9a16d1f84c34c259f63f2936191fa95e34af72b`  
		Last Modified: Tue, 07 Jan 2025 03:38:33 GMT  
		Size: 58.9 MB (58905215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955b90af7a64212921f379114d683f1ad259102ca5b7713828b8ad8c729d50bb`  
		Last Modified: Tue, 07 Jan 2025 03:38:31 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27eeca1ffe02466f09c266336743183f5805b7f68d7bb4d4624e3a3686861aca`  
		Last Modified: Tue, 07 Jan 2025 03:38:31 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1495-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:130c70acec62d3c1e499f5fbc0c74f098ae4102aa6b18a4baa0a9b99580fd4b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5143181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65101f77953f205e27958b96a902abd2b8aa29080968addd73586fcf9ca2bbf3`

```dockerfile
```

-	Layers:
	-	`sha256:891b41d18847162d60fdaf17abf304265d16aa8c0a314db4b2620b26d2c2ad41`  
		Last Modified: Tue, 07 Jan 2025 03:38:32 GMT  
		Size: 5.1 MB (5127185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9445ef179c4453497e3cdf506592678db7852657b5bacce7c3c011dab3e73ed2`  
		Last Modified: Tue, 07 Jan 2025 03:38:31 GMT  
		Size: 16.0 KB (15996 bytes)  
		MIME: application/vnd.in-toto+json
