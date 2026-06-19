## `clojure:temurin-26-bullseye`

```console
$ docker pull clojure@sha256:29822ebe4ee7884615403b077780da87f6465604b433a39605c3ab26a59fa119
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-26-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:3a2a6778b543525850555734f36f7eca4ae157864e08e34ed94ed2bf1d3b7357
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 MB (214809876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c3415bf5ba693d22d57b0d69cecdb8b6e53682209955f70425be88b37766b2b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Fri, 19 Jun 2026 02:21:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:21:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:21:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:21:50 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:21:50 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:22:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:22:03 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:22:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:22:03 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:22:03 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:af48a3e7696e07f88a02f9674e541901b65eadb5cf0f62e566b1d895099a1e9e`  
		Last Modified: Wed, 10 Jun 2026 23:40:09 GMT  
		Size: 53.8 MB (53771769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41b242d7b3a1f205f106b588d82c399f56d0a35ecef25aa9a611ec67917c66b`  
		Last Modified: Fri, 19 Jun 2026 02:22:24 GMT  
		Size: 94.5 MB (94524377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed846ae4ccd34e2875a2becf9421a95c35540cbeff85ac510b2e9a7f92f942f`  
		Last Modified: Fri, 19 Jun 2026 02:22:23 GMT  
		Size: 66.5 MB (66512688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddbef80682190c5f7e97a16ae3cf04c96117b8512024914cfbde73c07c8887bf`  
		Last Modified: Fri, 19 Jun 2026 02:22:20 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1c49213cd9b0a9f6904146b0552735278fc99cde9e344bd545531fbb450de8`  
		Last Modified: Fri, 19 Jun 2026 02:22:20 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:bdd2876a53b9ca02210ba2de97168638d289d708d1a45093d8b180b97a00db14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7387889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e03121754e57561429dea519ad4db654f884004efba63ff8900fc2d01c099cff`

```dockerfile
```

-	Layers:
	-	`sha256:80d809dae0fe7955f3ba14007e1abf0ea968c887561ae75eebe8fefdb656fd33`  
		Last Modified: Fri, 19 Jun 2026 02:22:20 GMT  
		Size: 7.4 MB (7371964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3f1154eb9f923ffea9e27954d6a75fe6a9806da826137d854652b27337957bd`  
		Last Modified: Fri, 19 Jun 2026 02:22:20 GMT  
		Size: 15.9 KB (15925 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:57f56cf65a637ff3e077533cb3b45ceab284105e3214ee2cdad4b7f6c000d64e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.4 MB (212447599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37467f7cf59738ed3a7a0d09dabcc9250ece45494e1a86f57db6b1f66ec9490b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Fri, 19 Jun 2026 02:22:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:22:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:22:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:22:06 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:22:06 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:22:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:22:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:22:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:22:19 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:22:19 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7c21e59e753cb91625909251110d6e4cc4a5411b4b7b37f74a62e56b927b7f1e`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 52.3 MB (52264114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68108532c38bbf8dfb1a7ebbe2607285c03441483c6773be65a940ad1ffb1ee`  
		Last Modified: Fri, 19 Jun 2026 02:22:41 GMT  
		Size: 93.5 MB (93504354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8919ab3dcf5cf51530158d71ff007a9b4491da1bf0ad3d061bf45e13999a80`  
		Last Modified: Fri, 19 Jun 2026 02:22:40 GMT  
		Size: 66.7 MB (66678090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae737661367a4a2cc8a2691b709b4e32e92e614a31aa5e9a89886861320f50a8`  
		Last Modified: Fri, 19 Jun 2026 02:22:37 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96f564a03146d7629c3877e7a894f8e18bf8ce4ede1746f4a872a0b800da076`  
		Last Modified: Fri, 19 Jun 2026 02:22:38 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:6d9fa01b10006e5a9961de6ef5faa9c9311cb91be9fb69c70f86060caf1e5657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7393102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1c6faa0a3cac9b4d32d6ebb14afdc30cab59deaf937e5ac1167a3458e892b38`

```dockerfile
```

-	Layers:
	-	`sha256:7e6b97bf7cefe46e4f599ba82ca42797b76d408c4f943666ea21598473b0aa9f`  
		Last Modified: Fri, 19 Jun 2026 02:22:38 GMT  
		Size: 7.4 MB (7377060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e8b0c74af3d18a47a75e8553413ea3eae5e2d16f953a4a19ef716ebb6d42f29`  
		Last Modified: Fri, 19 Jun 2026 02:22:38 GMT  
		Size: 16.0 KB (16042 bytes)  
		MIME: application/vnd.in-toto+json
