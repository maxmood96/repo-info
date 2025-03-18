## `clojure:temurin-17-bookworm`

```console
$ docker pull clojure@sha256:fd84ed8f93e2de01af90be8f3a89e9a10c224ffde4586d75623fac6b283efc94
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:0cfc14e5f734d4deae5a2d196bbfbd1707a058a3e97ec4f7e331602e8f90e5ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.0 MB (274037020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f193ef590b925515b55db0b33c916890aff9938d60ff038fba24b4ea45351cd3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a188d02295656d11eba221010636b3a2a18040f12e95838b26baaa70deb371b`  
		Last Modified: Mon, 10 Mar 2025 17:40:31 GMT  
		Size: 144.6 MB (144566594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd945ba5b0a3136862b31512965aae27348a216dd98a4de4cf2ec6177dcf2316`  
		Last Modified: Mon, 10 Mar 2025 17:40:30 GMT  
		Size: 81.0 MB (80993283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d5cc0f5d17d9780286fb5a937b6e6ea40269059856fb2014595901d94e0c11`  
		Last Modified: Mon, 10 Mar 2025 17:40:27 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37cd341e575f1d8a28d0881f38a337ec54a7d6db71ff5413b24fba9727c9b09f`  
		Last Modified: Mon, 10 Mar 2025 17:40:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:4d206d07643b030eba9f275b07c3ad81fa5ed1e8d48e7ddb15a34a372b7e2225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7186917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fddb6bff8137f44ad882d62fade5e03c95be9c55a7872b1149e3dcd30d6fce3`

```dockerfile
```

-	Layers:
	-	`sha256:2af50c215d1cac386c8fddd7a148b0893e41daeabb5691fed7325c400f5ed6e1`  
		Last Modified: Mon, 10 Mar 2025 17:40:28 GMT  
		Size: 7.2 MB (7171096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cb3f357e420d96b666fd4a950bdb164858a367e197ea917878eee1e08094a47`  
		Last Modified: Mon, 10 Mar 2025 17:40:27 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:80f7c0e4ca0914a04c2af75ab5637ced541d7b671175e2d70056e1533be205e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272603411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1cc12dbc15a02e135e3d43e197c213e07d3feaa01816ac8b8018232e42302f8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 08 Mar 2025 19:45:48 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:545aa82ec479fb0ff3a196141d43d14e5ab1bd1098048223bfd21e505b70581f`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.3 MB (48304855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998164cfae4d7f81bfc93eddab66e4a630e0ebbdc2a82ffda297a99017b6aa1e`  
		Last Modified: Mon, 17 Mar 2025 23:40:16 GMT  
		Size: 143.5 MB (143454716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:719ec5c6f685922819e6ad078067d97c7503551d877000bd6b826069be0543d3`  
		Last Modified: Tue, 18 Mar 2025 00:02:37 GMT  
		Size: 80.8 MB (80842796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3af4718ea050154c3a88839bb48844f7c8655f9cfecfcacef4d0029e0d680e`  
		Last Modified: Tue, 18 Mar 2025 00:02:35 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11bd44b4c7c94085fdfad20f7cd7391304a446f7035a2732d14443613fa61233`  
		Last Modified: Tue, 18 Mar 2025 00:02:35 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:ad45d5b0912c732c7648c36bf23a68d2c3224fc4d391c4a4da1f8f5172228208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7192810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdb84681039560de16f5c698947b6694556ca668250bf04062cfe3e0f781d171`

```dockerfile
```

-	Layers:
	-	`sha256:8859e5ff191047d1ed53892d7bddb0ff375555fff786d43f4ffe5cd03a685506`  
		Last Modified: Tue, 18 Mar 2025 00:02:35 GMT  
		Size: 7.2 MB (7176871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:150b8c1d4a8e21d6b42ac754a87e30b9cadb673679228472dcd7e3640bb95bc0`  
		Last Modified: Tue, 18 Mar 2025 00:02:34 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json
