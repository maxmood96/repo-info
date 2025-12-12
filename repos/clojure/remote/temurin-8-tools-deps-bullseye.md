## `clojure:temurin-8-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:c61e590e8f8991e50543e97660dfd31bbb6238d33a06c399b7767ef88acaf0ea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:9b2a44002eb9f4928ecc1e3b315e0f398187038d95aad79d49ae4f8ec17b70e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.0 MB (178047299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956fea01235e7792dce0b24ba3dd4c7604f7851813bd9892265ab7e9c7e3a290`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1765152000'
# Thu, 11 Dec 2025 22:35:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:35:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:35:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:35:37 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:35:37 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:35:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:35:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:35:50 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:437b5b60e3a4b64e2c621589a67483eeef6d4b3fc4926655006ef41bd44f71dd`  
		Last Modified: Mon, 08 Dec 2025 22:16:49 GMT  
		Size: 53.8 MB (53756413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498de6c56e66cfde21117e0817a39a37e0ac46b1f3e7feaeef9b8f91038567fb`  
		Last Modified: Thu, 11 Dec 2025 22:36:20 GMT  
		Size: 54.7 MB (54733366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:702d8b53fcc2ff10d7e5fe37f8102cdc2f8d6d3f50f820e5af2e6ff51d3bfa9b`  
		Last Modified: Thu, 11 Dec 2025 22:36:20 GMT  
		Size: 69.6 MB (69556875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222cd5404ddae3fba0c7d676ff6ffc9492cbe075458c9595e089b47e7ee4ea61`  
		Last Modified: Thu, 11 Dec 2025 22:36:14 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:4614c04d3cf7356110238d08ac6f28a8bf54907cce1d1467abc75c39d49e45e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7531471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2589c1ed358fa4f91ad1509b81fae0fe36005e96ec5d7b62cb8daf4f67847e42`

```dockerfile
```

-	Layers:
	-	`sha256:88cd85251817303a2c71d07dafa7e3bc5d4ea02be0396bcfe3cb583cedbc2305`  
		Last Modified: Fri, 12 Dec 2025 01:46:32 GMT  
		Size: 7.5 MB (7517277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03e5b41024ad5dde23bc07b374b10ff85399e98d9c04126d212429eaec0d081a`  
		Last Modified: Fri, 12 Dec 2025 01:46:33 GMT  
		Size: 14.2 KB (14194 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bb7ddaffab3798f3841cb9f687229e868d256c456d11bc8a3b6da913593d62ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.8 MB (175760486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f1c9bc2d1313076dc3e2e4ae381cf1b2a6e708e8204a25521d4a6f542602b36`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1765152000'
# Thu, 11 Dec 2025 22:34:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:34:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:34:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:34:42 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:34:42 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:34:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:34:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:34:56 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:24bca79f74a34f86894c8fcdc6ce8d7dc3c11dd0c76b7e9fa80c7c64df65d166`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 52.3 MB (52257713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a74ac23dbd29991c532a2c7c30bf0d41bdd15d30e5278fc18f0f813cf349ae7`  
		Last Modified: Thu, 11 Dec 2025 22:35:27 GMT  
		Size: 53.8 MB (53814985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd50ec6cf493fd58a2139582f59aa189cf911747514cd69bf5ce8f6ada2f1aa3`  
		Last Modified: Thu, 11 Dec 2025 22:35:35 GMT  
		Size: 69.7 MB (69687142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be72bf77b750ce3dbdcda08801e84af5f23c674a86bc10f7b32623c6c2c2d8d1`  
		Last Modified: Thu, 11 Dec 2025 22:35:22 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:d27229a792a866f88eeb9946e361fd80b2137d80740db399b252671939e19ab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7537386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8b31bfc0bc85ee94fe22b065bec169c1cdc0a1fdf7c8d81bc0c2c019d861691`

```dockerfile
```

-	Layers:
	-	`sha256:6a32fc7b6cb7434592102dde8f2073b754eacd49c0608ad2031106f4cf61581a`  
		Last Modified: Fri, 12 Dec 2025 01:46:39 GMT  
		Size: 7.5 MB (7523074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:432f9198632020587e3ac8a546cd1112b5c166b092ceee5353e95ed6c8446443`  
		Last Modified: Fri, 12 Dec 2025 01:46:40 GMT  
		Size: 14.3 KB (14312 bytes)  
		MIME: application/vnd.in-toto+json
