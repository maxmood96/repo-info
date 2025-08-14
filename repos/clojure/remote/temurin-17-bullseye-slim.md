## `clojure:temurin-17-bullseye-slim`

```console
$ docker pull clojure@sha256:bc869859d1118c2bb0a44631da46870141da1928880f33309ded77a7c1aa9838
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b1dd50bac50fbf01d49662b85d66ece8a01bc3bb4a65ed5a322112931c53f9b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.0 MB (233955943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:371a2b5afee4a46e8bdeaacc5c5547e1af89bab1e12cc496d7f4777f21049d0d`
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
	-	`sha256:5e7be5a063ce2fc05139349ab64a6429356efeb7760960d223ce4f65fef93c25`  
		Last Modified: Wed, 13 Aug 2025 00:21:41 GMT  
		Size: 144.7 MB (144693300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a8e1efef7f9929bea0107bc84c05987da948a940fda0c2aa3c16c58e5382c6`  
		Last Modified: Tue, 12 Aug 2025 21:36:53 GMT  
		Size: 59.0 MB (59005485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1817941453d8f2edf7103a16a806f357a902648490233812da016e6aa9555a3b`  
		Last Modified: Tue, 12 Aug 2025 21:36:51 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3255f38fb4493edc971e2bc40ffb13661aec32e1c9b8ed8cdb6fa7b05f38c25`  
		Last Modified: Tue, 12 Aug 2025 22:32:56 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2c9ab7e35fbd121c1762a683468b595cdf3e2c60c14261806b2e4005d7d929ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5323917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b8d4623e913d8e71e2f7ab4b59fbee3cbdbe4bdc8ff6e9592ef354ce3f17304`

```dockerfile
```

-	Layers:
	-	`sha256:7e75370522e1623c9464850a1903f43bc8a4af9bd7816ea931e90473cd555760`  
		Last Modified: Wed, 13 Aug 2025 00:36:55 GMT  
		Size: 5.3 MB (5308038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf7600f5276c48926f01cf5366c932ca9d3e66593514e823db614d6f81f54510`  
		Last Modified: Wed, 13 Aug 2025 00:36:56 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5bce6f622d0b8f4562abc6cd978ce905592754ff9c82e7513aa5a21b5b23cb35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.4 MB (231431354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:855d11c619a7e0abe7ec4dc5b81f073a7deb26b2e4e37ef6f8ac7d45755a8211`
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
	-	`sha256:554132d4fbb3932b7e2b1bcec38abd85ae0c20704c81e7370c80cad692f6108c`  
		Last Modified: Wed, 13 Aug 2025 08:47:16 GMT  
		Size: 143.5 MB (143542152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a253dad87938770b932375c674c20f1f34e8f4e9f9a5960413627ae175c2264`  
		Last Modified: Wed, 13 Aug 2025 14:29:04 GMT  
		Size: 59.1 MB (59137669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ec4b8c7ad27005fb0f5332e2ce5a1b86ce2aab220363e6433c3087dc6d47d5`  
		Last Modified: Wed, 13 Aug 2025 14:28:39 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d949dc424789a08a368b78c3bf003d201361a00e6c8030018f891c78e53fbb9`  
		Last Modified: Wed, 13 Aug 2025 14:28:39 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5874d38177eb6ef9176a3cf675bd04cb00a65fbf6a567110163d0003f0553fda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5329767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81dc2a052997c04d5cca8ab67d273d3707f9c02fe2bd2cc985800c89a4d210a0`

```dockerfile
```

-	Layers:
	-	`sha256:fc4316a7c3c019ca4c6a99aa9d21cb761284ac6b0e8abeadd2f5bbadcffa534e`  
		Last Modified: Wed, 13 Aug 2025 15:37:10 GMT  
		Size: 5.3 MB (5313770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdf4cb5a4a3de13baf1d82342e4622597203d2a926d80e37c5954600c4d48268`  
		Last Modified: Wed, 13 Aug 2025 15:37:11 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json
