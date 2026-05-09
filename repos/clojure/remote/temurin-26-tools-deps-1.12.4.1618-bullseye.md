## `clojure:temurin-26-tools-deps-1.12.4.1618-bullseye`

```console
$ docker pull clojure@sha256:bd45f475279fa9969d392afc982e70aae1852797b7732cdecd652338ada7831b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-26-tools-deps-1.12.4.1618-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:e46a46fed361eb82dd949a2a1319455343a4eb5565b67dec031bb57faac24e03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.8 MB (217817483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0901b551126501cfe621614807de6b1ccfeb0da7d8df946a3578254d129424bb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 20:20:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:20:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:20:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:20:28 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:20:28 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:20:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:20:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:20:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:20:41 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:20:41 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1c662d8f6b122c4f09d6ae1b210df55a5ba6e7b529807c0757ccba0c1ac508e0`  
		Last Modified: Fri, 08 May 2026 18:23:06 GMT  
		Size: 53.8 MB (53763343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b1b79b6096db868e091f2cef6b32678f5d5da02026226c73d65a607a2312b0`  
		Last Modified: Fri, 08 May 2026 20:21:04 GMT  
		Size: 94.5 MB (94455691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88937aae730ae9c3b9c43f95bbdd7e157f2736cf1603dbcaff3ae9f174b326cb`  
		Last Modified: Fri, 08 May 2026 20:21:03 GMT  
		Size: 69.6 MB (69597409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1308ce9e1b3f6f9225fbd4b22ca8a3cade0d6d22cbae7bbc5823cb4ad9a460a2`  
		Last Modified: Fri, 08 May 2026 20:21:01 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7810385136c394315606e49aa6fbaf2e9a0e5fbdaf74fbfd847eb755e242f1`  
		Last Modified: Fri, 08 May 2026 20:21:00 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.4.1618-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:35b6665af95e09d451518dde9bd10292e648940f69e6801ea1c93d0a69aeeda9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7388928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ce1f65337313a03bfa9b8fc531e58254110437251077f34105b92a4d809df92`

```dockerfile
```

-	Layers:
	-	`sha256:2c6854f95375cb39e1b64a0c417258df811e0661327a9c6f0140ff843d921cae`  
		Last Modified: Fri, 08 May 2026 20:21:01 GMT  
		Size: 7.4 MB (7373157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1747b7f9865cce2f7f6709cd3ec21c8d15cd4fc705f7bd61dd27fb1efe82dcb3`  
		Last Modified: Fri, 08 May 2026 20:21:00 GMT  
		Size: 15.8 KB (15771 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.4.1618-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:120df579c3ab74cb04a4692368674d5a7df86e8b583d3761673c6f3726bdc1f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215387978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de62b0feb1c9b649c8d1d116effb3891c1b5184877bcdafd45068ee64d15f251`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 20:25:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:25:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:25:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:25:04 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:25:04 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:25:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:25:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:25:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:25:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:25:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:965b6eb1fb4a74ed46e659c8fd725e1bec9bed6684b59cbca85e48b6c25a32c6`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 52.3 MB (52253210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473758cbdf98afa88d74c12a68f684bbd2148020927b778c8c5664550cd54d83`  
		Last Modified: Fri, 08 May 2026 20:25:40 GMT  
		Size: 93.4 MB (93395167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8825c7564dc399d545f06f4c35441cdc99eacad5fefb80e7874620f73edf6c99`  
		Last Modified: Fri, 08 May 2026 20:25:40 GMT  
		Size: 69.7 MB (69738560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dcd321e973e6b52abe4e73b4b73346c081f0dae35feb1b68062516f896d6193`  
		Last Modified: Fri, 08 May 2026 20:25:37 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:459619cc85ed58dba8a6f263cb9394ecb3fd64c6c71d5f70a7ba16e302d85517`  
		Last Modified: Fri, 08 May 2026 20:25:37 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.4.1618-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:b56b198b992c1c3995830706e38e7dc671e481f63a74f78ffe62a6ad84bf4006
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7394142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a93089a4c1a30e281eb5576823fcf8cb26badcd02689914ff3c30f349ec4c025`

```dockerfile
```

-	Layers:
	-	`sha256:d18e8fda5cb539e34450489225e871a449ed3ddccdcda8ea22fb95205b849649`  
		Last Modified: Fri, 08 May 2026 20:25:37 GMT  
		Size: 7.4 MB (7378253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e99b6947780c6dbfef82c78f5dcd5ea4f1c21355afc0ee68db6d8b9f732821c`  
		Last Modified: Fri, 08 May 2026 20:25:37 GMT  
		Size: 15.9 KB (15889 bytes)  
		MIME: application/vnd.in-toto+json
