## `clojure:temurin-24-tools-deps-1.12.2.1565-bullseye`

```console
$ docker pull clojure@sha256:2e86f97099625ec490e4aec1bda078a8f7b236f2aeea73afa3227c5a18371fcb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-1.12.2.1565-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:40a463f84ff903ac2046f95836e4c7ac7af1c771922d2d5580e7e3b8209d2ba0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.3 MB (213288001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eba8b9f8147ee0f713124d97645433669fe51579b9461852a3f5dfe69a10284`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:035115815e46101f9c9956e02e706f2f3ec8748e2b415f0d232b51eb76a6a779`  
		Last Modified: Mon, 08 Sep 2025 21:12:56 GMT  
		Size: 53.8 MB (53755396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd96df76e42b874fca038140b8011f1635c283dae9e97eaadfbf0662d10acb48`  
		Last Modified: Tue, 16 Sep 2025 00:22:57 GMT  
		Size: 90.0 MB (89975196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2454d65d48b0fbd9cf9581c778010b376a2e8ab405f639f1f4f831d292ccd877`  
		Last Modified: Tue, 16 Sep 2025 00:22:54 GMT  
		Size: 69.6 MB (69556366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a12efaa8480ff594744fd59e7b732e36723fbddc7ed1319c47c6c3e4b8159b`  
		Last Modified: Tue, 16 Sep 2025 00:17:27 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d654691df396469cefd3345f347d60b8c3d137035bea2de7bbb2d815d66e0a`  
		Last Modified: Tue, 16 Sep 2025 00:17:26 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.2.1565-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:ef363cf8cf5a32d81b7816ecd55cab72c2fe97b13a57598ff1d642e7d8a35996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7362129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dd13dd3603a08bfe0ef64bfb918546f514a59af5f70cfb6599e67d65e5f06c0`

```dockerfile
```

-	Layers:
	-	`sha256:ec13709a4921e5ebd84794fb8439b590708a1cdbbf1fe27fb84979d8c9b5851d`  
		Last Modified: Tue, 16 Sep 2025 00:44:41 GMT  
		Size: 7.3 MB (7346315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26ed7d649be828942df79db0b85ef3d09968553a9316803938ec5427c12da6e4`  
		Last Modified: Tue, 16 Sep 2025 00:44:42 GMT  
		Size: 15.8 KB (15814 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.2.1565-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:399dd33f8ca25a309d7dca82fac0cec91234d699a3ae2576b2bb046ae9b0eceb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.0 MB (211025885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fdff9aa322543122c2ac10b1651879cc407955dbc29f90b5ccdae38627c76a5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7df02cb4a974a4e8a9eb65ffcff7274f9dca341d29aaa763294c42e49805ca19`  
		Last Modified: Mon, 08 Sep 2025 21:15:41 GMT  
		Size: 52.2 MB (52248370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc9c9db46bbe7e9ce805463367a4a8cdb198f50ffe7377d5d7989164aee4edd`  
		Last Modified: Thu, 18 Sep 2025 15:29:51 GMT  
		Size: 89.1 MB (89092521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f85ea6d1bc18fe30b394a2c5bce87087f165bb38c738d52f70546b6b4e40c8`  
		Last Modified: Mon, 15 Sep 2025 23:29:07 GMT  
		Size: 69.7 MB (69683956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb5165d72f8efcc0cedc2779b32b2ba9827826a29d89cb77aa72150b756cfcd`  
		Last Modified: Mon, 15 Sep 2025 23:29:01 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362a6fb2ecf3e8e44981a10f2c76f020202e496bc2329bdc8b1441ebb77975e0`  
		Last Modified: Mon, 15 Sep 2025 23:29:01 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.2.1565-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:aa8d50758ce47d81584b650d923641d8d2c66e30b2da58a5acb5b5ea63575899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7367343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b53eb08570a2d0ee20713d95edc0d5408bcf8e8f1261ccfa9a77d3e6cabed25`

```dockerfile
```

-	Layers:
	-	`sha256:abd06ea0c6155216e6a54c8ef233091615d31c19883cc285d1c95e131a1c2214`  
		Last Modified: Tue, 16 Sep 2025 00:44:47 GMT  
		Size: 7.4 MB (7351411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad7091bb63b3fbb458e6cceed207ccd6a25f54f4ca8039461cf8406ce889650e`  
		Last Modified: Tue, 16 Sep 2025 00:44:48 GMT  
		Size: 15.9 KB (15932 bytes)  
		MIME: application/vnd.in-toto+json
