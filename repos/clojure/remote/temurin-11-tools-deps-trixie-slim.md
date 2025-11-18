## `clojure:temurin-11-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:1fa3cbde6297c1ecda9b3588d7a61dd7d775ee103570ac4054bdeb96cc13008a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b21661fb322528242b0ef604e8892367ef675d856a8e665c670face7941ba571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.7 MB (246739861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:261b8034355557d71f800617f41ac23b9c17ed8b40a5cf93e4a80bbeacb0471b`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 06:08:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:08:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:08:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:08:08 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 06:08:08 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:08:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 06:08:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 06:08:25 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47c8f8aedeb9fb0243991d793c7b7bd07580191c1f416318ba425afa14d491e`  
		Last Modified: Tue, 18 Nov 2025 06:08:48 GMT  
		Size: 145.0 MB (144966634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f664538d77b3c8b3ef3fb3023433acefdc1ed528e936d0e6a9a430ac76ee15f9`  
		Last Modified: Tue, 18 Nov 2025 06:08:59 GMT  
		Size: 72.0 MB (71996101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af514030cae2ebc02617a9efecb1b6382b4d8ae0ed6ba561578eaf1dfd485721`  
		Last Modified: Tue, 18 Nov 2025 06:08:54 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2a26e946812e9ddb43d59d3987af0a6e82bcc9fdb4c4aebd6e52c90294327ca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5290581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbe9e75f0ccbb839dcabe88e3a4889647bca6fab5a9cd9453254129c78dacda0`

```dockerfile
```

-	Layers:
	-	`sha256:d1e43880b8c9984ccd0e4dafe99d50c0d8ed38ee4dc5c8c68b853d8f8eb27d83`  
		Last Modified: Tue, 18 Nov 2025 07:39:47 GMT  
		Size: 5.3 MB (5276338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f70aab51fcb86fa4f4686b6b4ad72af7166d3ed972c8d729ff3f1fa515bda6a4`  
		Last Modified: Tue, 18 Nov 2025 07:39:48 GMT  
		Size: 14.2 KB (14243 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:00723a7c1cd3e4ccf20e17c8b94e6c3edaaf130c53a4b259b2ee8a353ba65638
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243679476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c1251b5317735e8ec4bbf0259d0a8cb27dc48c1774be98e539b65a92b87f1b1`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:00:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:00:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:00:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:00:29 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 05:00:29 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:00:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 05:00:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 05:00:48 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:047fcb7a160079fa43b5a39c4c1a5a47acc6001852b7770a90c16cf22175924d`  
		Last Modified: Tue, 18 Nov 2025 05:01:11 GMT  
		Size: 141.7 MB (141731574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0799dae8e2ce27a2c36207067fc1acfe0cb54eab56cce1e181b45eaba542897`  
		Last Modified: Tue, 18 Nov 2025 05:01:24 GMT  
		Size: 71.8 MB (71808648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17aa21b0c69d76d9510954005b31e015aa1bdf30d9b0288b878b5e5c10ab1c7`  
		Last Modified: Tue, 18 Nov 2025 05:01:17 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7c4a931bccd3927e2b11573681627a7c39d72a11cab5ba00bef62235db77d949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5297086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380f032f88d7b0d76aee321773c5f0484b75ddf7899df0b15b76cfa70099f9f9`

```dockerfile
```

-	Layers:
	-	`sha256:d7ddb3ed55b18e4f12993432a74a511b7532b57b37e9bce7fa58e3156569699c`  
		Last Modified: Tue, 18 Nov 2025 07:39:53 GMT  
		Size: 5.3 MB (5282725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:773194a97ad2846e290d192072ebca1d3da8b2bb50a32919865256ec17da6f6c`  
		Last Modified: Tue, 18 Nov 2025 07:39:54 GMT  
		Size: 14.4 KB (14361 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:2424787f49fb59086c359e29431c1a2c25b9328f75dc71039f97bd9bc55a59dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243078191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04fc70f63f84f05f87e2f7c63a52402839293a0eabf645e8d69e6f97e847fbd4`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 06:48:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 06:48:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 06:48:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 06:48:18 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 06:48:18 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 06:58:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 06:58:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 06:58:15 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba02b519b8b719ee4748bf543f937aad327f5a7c293b9d3f4889b5085d769344`  
		Last Modified: Fri, 14 Nov 2025 06:49:32 GMT  
		Size: 132.1 MB (132081963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516453827da09845a133922f9da30ea88e672bad8beaa815c7c2339ad57c28c3`  
		Last Modified: Fri, 14 Nov 2025 06:59:07 GMT  
		Size: 77.4 MB (77396936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2fa7a4f95da1b876dcdf5e63dff6928fa9bfa3939b64722c1aeb7fc4450b627`  
		Last Modified: Fri, 14 Nov 2025 06:59:00 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ae71c01767c9f60ebc4cb4583b8ca2d54efd24f8f033003e731d7146a38d5d64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5294355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf492a57d222ca3bf3de157f74678b9dbac0f7f93f1f80a07556fb28d4200c3`

```dockerfile
```

-	Layers:
	-	`sha256:d5f7b1025b32c00931aa979665f381571d10b96abff4e75d5f37a89c441b5a9f`  
		Last Modified: Fri, 14 Nov 2025 07:36:33 GMT  
		Size: 5.3 MB (5280064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:429f3e7e4dd76bca2f0ddb5844d3938231d48e703b384affd68d161130683a5f`  
		Last Modified: Fri, 14 Nov 2025 07:36:34 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:e717c3b7cdf3528caf4afa59c51a4f28c039c9bcce77d38b449a086e9f70c1b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228482770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee98dc953fc5cc7d505ca8a452bb889fbef27e20e8f709b9c90ce76ed222247d`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:22:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:22:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:22:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:22:53 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 05:22:53 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:24:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 05:24:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 05:24:41 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1190da05ae19a10b46e3d831eebcdbad7fda228e722f28b4f162aae378b135`  
		Last Modified: Tue, 18 Nov 2025 05:23:45 GMT  
		Size: 125.7 MB (125694433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a333cb1c8f9f2eb0ed54690bc62cc5529478c4d3410ad2e863cb55a7ee0b2d`  
		Last Modified: Tue, 18 Nov 2025 05:25:19 GMT  
		Size: 73.0 MB (72953322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5499ed983b0de33cced99cbd5f83a91282fed5ed754b65bf70e158568171d6a8`  
		Last Modified: Tue, 18 Nov 2025 05:25:15 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0700124ebef9eb52bd52c76528984d7d012ff9ebd29ae72df6c2f70efb761c9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5286509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd6f92dfba52ae3f9238b509202e11edc9b0a5232b55cdab4de51a86e068c04`

```dockerfile
```

-	Layers:
	-	`sha256:f081923cbe15c83d6d8413d8624b769d64f3a5d157ddc30b6c096321a69935b7`  
		Last Modified: Tue, 18 Nov 2025 07:40:03 GMT  
		Size: 5.3 MB (5272266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef3cd6386f2cf6cbced9623e41171c74b259befc5bd3025aef4094b71b93a598`  
		Last Modified: Tue, 18 Nov 2025 07:40:04 GMT  
		Size: 14.2 KB (14243 bytes)  
		MIME: application/vnd.in-toto+json
