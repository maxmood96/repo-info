## `clojure:temurin-8-bullseye`

```console
$ docker pull clojure@sha256:fd28cfc43e84edead8f927dc704bce1b88c476ca96d72d19fe63ac73c0762a11
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:9b0b0e2ff089fe60b581e517f779fabdf578e1d123e0e6f95cc39bed2d153b42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178521085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eec9498ef2227bc023b75c4766aa5c5a7391e0e57149b687f1c6f1ec9268684`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 03:13:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:13:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:13:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:13:01 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:13:01 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:13:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:13:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:13:16 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ced3088fc7691915325d6187786ba346149f7c9dcdbfb3772ca71be74bf87622`  
		Last Modified: Tue, 07 Apr 2026 00:10:43 GMT  
		Size: 53.8 MB (53762793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18eb531585f80630785cdb6193cfb62a9eb228fe297de6c6fd484e4823f50f46`  
		Last Modified: Tue, 07 Apr 2026 03:13:35 GMT  
		Size: 55.2 MB (55170118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042417a8c2356f9651b8f71507ca9943585d04f06338e0af9f886dc199421bf1`  
		Last Modified: Tue, 07 Apr 2026 03:13:40 GMT  
		Size: 69.6 MB (69587528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ad6dfa8bd83cbc79621a33034947e834aedfbd97def75983bf77452a389c3f`  
		Last Modified: Tue, 07 Apr 2026 03:13:36 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:a87b88e3201f9d2a8261ccc4c99998b77c19d780a025de87ded80aaec1bcaf4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7542833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f3f9555bfb52a16a2740f3db221bf02701b444ef68275c29254f0e83d0abaec`

```dockerfile
```

-	Layers:
	-	`sha256:af1a52b29a5ae210d93ca89b1f8a99f86537aa01ba47c255b4dbf4aeab9baa79`  
		Last Modified: Tue, 07 Apr 2026 03:13:37 GMT  
		Size: 7.5 MB (7528640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0151026caf346c2d92b3d1c3da8a29bf5f84ecfbceb3f50cc8f1b18b4d59cdf`  
		Last Modified: Tue, 07 Apr 2026 03:13:37 GMT  
		Size: 14.2 KB (14193 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a48c172662fef7790abe18c66fbea1b20bc4e5eb0fc2bdda72b2706553adf228
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.2 MB (176228279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:242ded80efcce5c7f43fc658ba5f29479e5273a98794bc610f0fc6f6dfea7b01`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 03:23:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:23:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:23:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:23:31 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:23:31 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:23:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:23:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:23:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:910d955c4ed64a8ee0854ded27fe508086448dca2dcf21a0af023b8bc9d2020f`  
		Last Modified: Tue, 07 Apr 2026 00:10:48 GMT  
		Size: 52.2 MB (52247615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d6e595111a1b4e74740bc6a5a1d2cc6adbf096152fe0b40a97c5dbe2ac6e441`  
		Last Modified: Tue, 07 Apr 2026 03:24:03 GMT  
		Size: 54.3 MB (54251612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2971709514eb72d1716a266458393d9e842588822e92a1b5aef222d187e18e`  
		Last Modified: Tue, 07 Apr 2026 03:24:04 GMT  
		Size: 69.7 MB (69728406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee628e83ae2c471dd3f9184d7682fe2b0cf333584907bd4aef4e7f0e78243a82`  
		Last Modified: Tue, 07 Apr 2026 03:24:01 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:ced4c53fdafe71d36413bbc54fc6eb5c79a4125cc9f94741086bf654bff30577
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7548750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907ca78c40a969319d426a409148000a63498177fa12b6659f379b308d64363a`

```dockerfile
```

-	Layers:
	-	`sha256:06202130ec1da6fb97660df0f9c0ba49c9b6b4e80c792821a7509b884e7e7c1a`  
		Last Modified: Tue, 07 Apr 2026 03:24:02 GMT  
		Size: 7.5 MB (7534439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c9edd74dab8cf982b1ea8605de207911d92381a2889dd81f92b83d72b8cc504`  
		Last Modified: Tue, 07 Apr 2026 03:24:02 GMT  
		Size: 14.3 KB (14311 bytes)  
		MIME: application/vnd.in-toto+json
