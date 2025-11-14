## `clojure:temurin-11-trixie-slim`

```console
$ docker pull clojure@sha256:3f4a24d9b1cd21c1644c7a19d8902b7fec97952e1d3ed3e787d47e7abccf54f0
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

### `clojure:temurin-11-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ca29a3d355b2d726d0c395fa4d8506820f7ababb69c00b36541a3f52803a23ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.7 MB (246740503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e58e49a9998b3e18c9e89f1a3e30f358c6c59b885ab027b9e9f8b2fb2591de9b`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 00:51:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:51:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:51:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:51:48 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:51:48 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:52:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:52:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:52:06 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96328ff14225645ec90a19c4e83a3881e512470be4f0dff9097f6925fdfd32bd`  
		Last Modified: Fri, 14 Nov 2025 00:52:30 GMT  
		Size: 145.0 MB (144966606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0e212028156562f78b7bf587d634315af533838e96e7d584a1d985f29763e6`  
		Last Modified: Fri, 14 Nov 2025 00:52:43 GMT  
		Size: 72.0 MB (71995146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7830ad3f68dcc2c0092368b1756b1778654ea26b560b676052ae25c99128c57`  
		Last Modified: Fri, 14 Nov 2025 00:52:36 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:33be1739b005b8957226c9296040c20412db4659a6f05ca68fcfa359e0e79f8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5290551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec864bf52518bc9fd6381b0094b88823dd0d44472c170657ef117df8972c70cf`

```dockerfile
```

-	Layers:
	-	`sha256:8e8c2851b0753c0d78b61ddd776fe9ab7f4e3786406d48f312757e8c712bce6f`  
		Last Modified: Fri, 14 Nov 2025 01:38:07 GMT  
		Size: 5.3 MB (5276308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:931aa24b03594cf0bbc24d6d9f280359e96d5291499416f08e3aa20e5fe390f3`  
		Last Modified: Fri, 14 Nov 2025 01:38:08 GMT  
		Size: 14.2 KB (14243 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:70674b44809a7b84ac68d1718b56903ce523d2a43571278e695011cc35436dc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243683087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67f8d0270d417012422626b3d0d575d52c04a8067899176a8e18a2eb736061ad`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 18:41:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:41:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:41:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:41:29 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:41:29 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:41:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:41:47 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:41:47 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d90057a63803b159ac670d744b0e7bed15a637d9adffc9b2bf8c39b05b378fc`  
		Last Modified: Mon, 10 Nov 2025 05:51:18 GMT  
		Size: 141.7 MB (141731668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948e71568c32748c1ce594e85593266d81dd8995558fdb976f9b2b1f0c8cc32a`  
		Last Modified: Sat, 08 Nov 2025 18:42:43 GMT  
		Size: 71.8 MB (71808477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc644dfd3224ce7b95ffcca76b63355c521e11d7702f4e61165fb1c6af6944ec`  
		Last Modified: Sat, 08 Nov 2025 18:42:38 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6d4576a06c8aa7bd97231f55daf8ebf845127feb7f5290f62359c66d8bd5268f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5297055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdcd9c39c4e6a3dc4da913fff7d4754a1c05b325fce6d644ee5b21ab1591c772`

```dockerfile
```

-	Layers:
	-	`sha256:c40d8e00d8a037670b9a7ebde470d00b8eca0da7c149fa6ca2f86301d81cd427`  
		Last Modified: Sat, 08 Nov 2025 22:40:16 GMT  
		Size: 5.3 MB (5282695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70580fc0f037421fdfdf285d28b4825ed8c976d1547522c8fc7c40adf2dd4d80`  
		Last Modified: Sat, 08 Nov 2025 22:40:16 GMT  
		Size: 14.4 KB (14360 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:d5dc58acaeba7a936e8dc3776b4ab0c88fafb37542b5099896ac38257f32ecd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243075956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:313f26a27d4c542e85c31e52a9c05ae37cc1aa7be4360264900328fb18299350`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 19:29:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 19:29:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 19:29:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 19:29:54 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 19:29:54 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 19:38:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 19:38:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 19:38:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e84755afedfc1f89c7dd573185b292e927a21b944ec113aeea516c2bc3165e1`  
		Last Modified: Sat, 08 Nov 2025 19:31:00 GMT  
		Size: 132.1 MB (132079869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a55ce9b574964f78dc82c5bec18de97818c78755b6e3062b34dc93ffce9571`  
		Last Modified: Sat, 08 Nov 2025 19:39:08 GMT  
		Size: 77.4 MB (77396793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620f9b2cfb231ec7f0e46b335b2a1de5344d1dd52c1f4b02b3b2f0e1f4ad777a`  
		Last Modified: Sat, 08 Nov 2025 19:38:47 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6d2bae97aac719f8fde5b0b8ad63f4f5458c9aa05915f93b6efc730ef69fc1f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5294355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b894c5530c8332a5bb02b9531cb4601568cd083f9928511dd1fb0ffe633d3aaf`

```dockerfile
```

-	Layers:
	-	`sha256:30087aed0beb75f1d62db0e71db4f888e2599b0d6719309e680e2e6cc23113ca`  
		Last Modified: Sat, 08 Nov 2025 22:40:21 GMT  
		Size: 5.3 MB (5280064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42e9932a99f9f945f6d0c545c50bc81bdc0eb8d7ce4655528d7dee08328b115f`  
		Last Modified: Sat, 08 Nov 2025 22:40:22 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:03fe89995a47abb6fe7bed3264c35e6ae4c7bf607084e81101d8da040c330d79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228486325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d81e14ae7baa601dcb1e1d0ce0e14e6aa111406b9c2bf9567ebe3f79db34d2de`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 00:52:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:52:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:52:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:52:50 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:52:50 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:54:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:54:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:54:57 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6345b0ba4ab712f7cc510aad027ef83b70aad351c8a0761add52239f87322f00`  
		Last Modified: Fri, 14 Nov 2025 00:53:44 GMT  
		Size: 125.7 MB (125694447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6501b1bb4e7077f613c58caf38f388261040fb408a4c3fb679223ccc98dbb3`  
		Last Modified: Fri, 14 Nov 2025 00:55:31 GMT  
		Size: 73.0 MB (72953840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d647a262a190a4c08e49ea7964d213ae83dee8d39d4706416a47ec947d380bd`  
		Last Modified: Fri, 14 Nov 2025 00:55:24 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:daa8580a92dc5030dc73c90018b4b28b4f0086c03c9bcfade9d71721797c3a61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5286479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87b9c7fe78a31e2812aa2278c2b2b82fe0e2722b778d732991dd11491f6f9203`

```dockerfile
```

-	Layers:
	-	`sha256:612588e0768d94acaa6ca722d5ed531779c12e5cdacc0957c5ef65153f1e5061`  
		Last Modified: Fri, 14 Nov 2025 01:38:22 GMT  
		Size: 5.3 MB (5272236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c308ac85c0a8b462fa5ac63925fe3c60d98a8ec38879953bfecaa57324ca834c`  
		Last Modified: Fri, 14 Nov 2025 01:38:23 GMT  
		Size: 14.2 KB (14243 bytes)  
		MIME: application/vnd.in-toto+json
