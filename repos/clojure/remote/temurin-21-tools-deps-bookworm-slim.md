## `clojure:temurin-21-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:5330cc6b43ad8a44a00262a18180b41c32674b9a4070da02a2d21a70b88c71af
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:8cf133625a56507b98b642366eb35333d356b86b8b4e5bd65704b9f5b7f42958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.5 MB (256517790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3710a434dccc7790f66f77be8db4cb44b08b64ceb588a3c5a59bec4ec162e27d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f813acd019188d826cfa0eb82e35b5e72840acd9944bdccf1102f36de2ce0a`  
		Last Modified: Wed, 05 Jun 2024 06:10:44 GMT  
		Size: 158.5 MB (158497970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f814f66f4c00fafe6f0508abec50956864fa519620718673a44eaf729f95b06`  
		Last Modified: Wed, 05 Jun 2024 06:10:42 GMT  
		Size: 68.9 MB (68868360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aca2f7e335e919e4dc94eec3f1fe1c701dedd8fdd88a6933c9c3f940184361b0`  
		Last Modified: Wed, 05 Jun 2024 06:10:40 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8773e62b1addb13326534627f715eadb46e6a49f2c8d43418c85131f47e155d9`  
		Last Modified: Wed, 05 Jun 2024 06:10:40 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b848b487ae2bd08cfaaa78045dcc86da4b90097b3b682c7cf8428fd3de877c19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4721802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b835e4061b7e6abd6369f3c36443576c5069023c0fb12e09bf499efd5ce6af0c`

```dockerfile
```

-	Layers:
	-	`sha256:6cbdc1a6245febebbcda480df2e8b3f9971e9cbb617c5b54a77d27f4edf28751`  
		Last Modified: Wed, 05 Jun 2024 06:10:40 GMT  
		Size: 4.7 MB (4705644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f16c356440a9299a02281824aa48dd1994610babb56cb9065f09686b0f23f43f`  
		Last Modified: Wed, 05 Jun 2024 06:10:39 GMT  
		Size: 16.2 KB (16158 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:053f1da3ad0fe96c96c7d5fba2752ecc016d92a70786cfbe750e27eb130fd344
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.5 MB (254466945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06bdaa7843de2975d131d20cc3e64981ccfd521acc9388fba28d6c59afcad4a0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53de0432743a37a66d2078f70aa933b19d00509431e369e4412519798eb46ba8`  
		Last Modified: Wed, 29 May 2024 21:48:52 GMT  
		Size: 156.7 MB (156665641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fbcf790e5dd5d5ee1895237918862206fa2b1788528471cf8f804061a519d00`  
		Last Modified: Wed, 29 May 2024 23:20:29 GMT  
		Size: 68.6 MB (68620756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fdfe101647fa3e6c96e5bd87720b168ab4d22f5b3838de908964d34514a7c59`  
		Last Modified: Wed, 29 May 2024 23:20:26 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ff512ae686110e0e361dfffadc61980e018ef65b61fb0c4d9d19854dc54957`  
		Last Modified: Wed, 29 May 2024 23:20:26 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:81a6147acd9aacf61dcf0fa9a610f3ba054e3d3909f9546686034a12fe75fb8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4728778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734a7a37f06376757d08773e8135d3d086f035b48599372242deda173d9abad8`

```dockerfile
```

-	Layers:
	-	`sha256:8bbdd70a077be67b974a23de236f97b162d724b25a98222b5c6199e63bd6e9e4`  
		Last Modified: Wed, 29 May 2024 23:20:27 GMT  
		Size: 4.7 MB (4712054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4502634e2693e061b90e9c65c63b958adae9fd2186b3ca7d13893c38ed506ae`  
		Last Modified: Wed, 29 May 2024 23:20:26 GMT  
		Size: 16.7 KB (16724 bytes)  
		MIME: application/vnd.in-toto+json
