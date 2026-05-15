## `clojure:tools-deps-1.12.5.1645-trixie-slim`

```console
$ docker pull clojure@sha256:67a6e2a3ac87b5b1685a6a92b4e94c9a6b5c830b29ed49d56922c0224b2ebc09
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-1.12.5.1645-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:87ae54aebe6cff1025a045bf4ae3b05c2034769e37dcbdd01d158e5ec4187723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.4 MB (194401879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad737ca56c73f6bab87816780e3b01c6e210e049818107279b1a0715689421ef`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 20:16:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:16:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:16:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:16:13 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:16:13 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:16:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:16:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:16:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:16:29 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:16:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1a535892c33d429684443c5469ea54f368e23ab3f1f61eddab17d076af600a`  
		Last Modified: Fri, 15 May 2026 20:16:51 GMT  
		Size: 92.6 MB (92574564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305254915beb812e48f81550728b63de7cd2b89e4b1830d06ea35212d3662f9b`  
		Last Modified: Fri, 15 May 2026 20:16:51 GMT  
		Size: 72.0 MB (72046045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669624fb8a3612e826cd8b3c31568f89ef09b2dac24f1b32c4d67d7e85cb02af`  
		Last Modified: Fri, 15 May 2026 20:16:48 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ecddf1dcaceb5954de6b1a6ab0baec69ff6ce4f85031275f34a6d4040a5c63a`  
		Last Modified: Fri, 15 May 2026 20:16:48 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.5.1645-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:72c64a834ba00cf07edbff972155897bd05cc4d9250378a9525f45322c6fbcc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5244581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02b5f2b64dce6f9d167481dc0c8cd491f7bb52d3e9aefff4bda92fab93272568`

```dockerfile
```

-	Layers:
	-	`sha256:d4d74ad40d7d0869c4df61fe10c1ffa050f861276dd2a4f7ca7aa888dc6b34e4`  
		Last Modified: Fri, 15 May 2026 20:16:48 GMT  
		Size: 5.2 MB (5227935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b0e6cdf86d260f326dd4e125e60f843bc56db74ca3e33b508e98d587908d5df`  
		Last Modified: Fri, 15 May 2026 20:16:47 GMT  
		Size: 16.6 KB (16646 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.5.1645-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:169767b29d6d74260caf5a45cd9538af4c507f519efad91377a8c143b32c80ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.5 MB (193541781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:421b25cac3ef65e5498af61a55e6dfc3586eabfb588d1a1b048c4f83161f845b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 20:16:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:16:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:16:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:16:14 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:16:14 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:16:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:16:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:16:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:16:32 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:16:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417c808e65004d4b52c30b70f88571a5c92a3ad98317169d501055711b70baab`  
		Last Modified: Fri, 15 May 2026 20:16:53 GMT  
		Size: 91.5 MB (91542254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb04b242533c7bfe87d4a43e9460d14df0c68f85455eef8939ce08fde8c059c`  
		Last Modified: Fri, 15 May 2026 20:16:53 GMT  
		Size: 71.9 MB (71854844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbdb1a6dbc5d6de119d951a823905898434c9977e14625f6bab48d7e5bbf4098`  
		Last Modified: Fri, 15 May 2026 20:16:49 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:843fa8f64f67cd16ab077dce56e58e6ee84955287e46d4b853822ab9d9fd2704`  
		Last Modified: Fri, 15 May 2026 20:16:49 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.5.1645-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b1b263baf93740a65690947bb306f8d48020bf442654f1bbfbbefa2ad14d0a5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5250514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:712bac4297995cfdab081ab1f2d88b922c977874ffa76e990b3686e7f486914e`

```dockerfile
```

-	Layers:
	-	`sha256:1676c419ef493a1ebb7bdeb66d20e881d65f2b28a49665878ff1c2d3b3ba2b80`  
		Last Modified: Fri, 15 May 2026 20:16:50 GMT  
		Size: 5.2 MB (5233725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48e5d2a5b5c0218c6b6a4d0bf484e0a3ceae096dc73262b5a55d623cd1aea070`  
		Last Modified: Fri, 15 May 2026 20:16:49 GMT  
		Size: 16.8 KB (16789 bytes)  
		MIME: application/vnd.in-toto+json
