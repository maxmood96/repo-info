## `clojure:tools-deps-1.12.1.1550-bullseye-slim`

```console
$ docker pull clojure@sha256:747ff337c740525e13dfe95f97619b1f1fcb2fac9e5d3bce2be87f6242fb48f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-1.12.1.1550-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:8abff0077980379b50495754fe6cf601ce01c236a339cffa29b71e7ba43ea7eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.1 MB (247067608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa2257f4b67b1176ed0a5e404591d55b22e583075ac4a5d8d06f897e8401cc8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3e41ca17193bcd7630e4dd210602930b1f94464bdd59680bbf6654206f7707b8`  
		Last Modified: Tue, 12 Aug 2025 20:44:40 GMT  
		Size: 30.3 MB (30256118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4692ac047552961c86bf9f174823b3265fcc13d180b502f151ef58c0017f8c`  
		Last Modified: Wed, 13 Aug 2025 02:30:24 GMT  
		Size: 157.8 MB (157804777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86cbefd477f7a9537f9ad9547dc8b0ccb0ebab596aa0fae8bbbfb91c447e8c84`  
		Last Modified: Tue, 12 Aug 2025 21:37:47 GMT  
		Size: 59.0 MB (59005672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b39075e4d4ae4808b799fa8d313e9923d5b3b935b30edb47e536c70ab38044`  
		Last Modified: Tue, 12 Aug 2025 21:37:40 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ad004990129408a77287534220332acca200347084658afaeccfc8aa313239`  
		Last Modified: Tue, 12 Aug 2025 21:37:42 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.1.1550-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1084ff8ea346e735ba9d2859d8e1594844a8cb9f65453ee130137995ce470d26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5328411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12d31352ad3c614c2aaf7ba2d1c2991198cb3af0f365d11fd668ae5ff5a6f2de`

```dockerfile
```

-	Layers:
	-	`sha256:0dd4f82db8366f678757358e6f83b68bba36ea61a594e902ac73e21f30291d3c`  
		Last Modified: Wed, 13 Aug 2025 00:38:36 GMT  
		Size: 5.3 MB (5311836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fb6c04daba2ad3fb5a9f652b0cc2e7af78e87685c0dff354d9d099ef02f9c7e`  
		Last Modified: Wed, 13 Aug 2025 00:38:37 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.1.1550-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4fbf3f61a8ddf01917b1213df187d2eee40cbe733543ca34fee645d5dcb538b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.0 MB (243970448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:582dba7ea222b6f7c36253ec4bbe4ae16638bc203d3bfbc49109a83bbff7ce12`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b99ef417bc3eb3946e7b3162f6c19dbca1039f3b4124deb116c3a0ab763e65ad`  
		Last Modified: Tue, 12 Aug 2025 22:33:30 GMT  
		Size: 28.8 MB (28750491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb248e0eb64501490978fbb8096bf909846446841c77a1b70d33bbc15b1005d`  
		Last Modified: Wed, 13 Aug 2025 08:45:09 GMT  
		Size: 156.1 MB (156081226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6855b24987fdc0412a70e4d828fb730d0e51e4d87b5fc4907f91fac614fcbdd5`  
		Last Modified: Sun, 17 Aug 2025 09:35:23 GMT  
		Size: 59.1 MB (59137689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7db6ec0207d632d47d09b0368c9ca38fd76189e66ec7bbf49e339783a4b1f7b`  
		Last Modified: Wed, 13 Aug 2025 15:11:12 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2417d05d6a3d68e3ed930f8718a986db7ac1d8ecbcb0579f2a0649ba5daeb47`  
		Last Modified: Wed, 13 Aug 2025 15:11:21 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.1.1550-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2ffd4b6e8e5b55787874cfeecc63e0b416880d2f0e17bde8054ac5f90824d700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5334309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5364d1d350236818e3dd4f5efcec164b4013eb22e55b5b0fb0208e3016079b06`

```dockerfile
```

-	Layers:
	-	`sha256:97a2c5392cf506c978478744223f3ca704eaedff1d3cbc4f389b0304cb5c2bf7`  
		Last Modified: Wed, 13 Aug 2025 15:38:57 GMT  
		Size: 5.3 MB (5317592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b5e2fcb0e4daa50869e3272cec42d165e4c45bf8bb305cec7648ed6ac565553`  
		Last Modified: Wed, 13 Aug 2025 15:38:58 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json
