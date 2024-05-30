## `clojure:temurin-21-tools-deps-1.11.3.1456-bookworm-slim`

```console
$ docker pull clojure@sha256:bed4869dfa9e17dcee169dcb9dff450dcc1a8d3c131fc642a3bf5f08fefb7756
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.11.3.1456-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:8d900ce818493af0c772064501c3c4e0e6c9ddb9c015394f92e36e6be0108fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.5 MB (256517162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144c64171a7f97acc9588aae9d07694c68594538c90e97adae6f996364918e86`
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
	-	`sha256:4f24651d987a2e75e63964720e07e73969c555c53a3bb0772657a5f25cd5e5a1`  
		Last Modified: Wed, 29 May 2024 19:58:24 GMT  
		Size: 158.5 MB (158497991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:007020339b8abfb0b0e98065e2f826a76b0dab5d4a30394350b9f49c210225c8`  
		Last Modified: Wed, 29 May 2024 19:58:23 GMT  
		Size: 68.9 MB (68867711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c1d057df6a16dfb669f06cf0f999722e9f0994a7e88ce1cacd3b30ef84f98d`  
		Last Modified: Wed, 29 May 2024 19:58:21 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8c31fcf1f917f434043fde20b7226ec36807e916fe68e92fc74437125e05f4`  
		Last Modified: Wed, 29 May 2024 19:58:21 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.11.3.1456-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6976a25054223a83a757fa577230136f8cad62c0314148e8c9a6e97412d9bf98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4721804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d03b1c22e0665a76b5f1125da270f3e86fdfa3697950f4624e61fc3361c77a1e`

```dockerfile
```

-	Layers:
	-	`sha256:8f4a12ace54260bff91859350e6cdc00fa8e52c47b1ed1cc0f932a14bdd5296e`  
		Last Modified: Wed, 29 May 2024 19:58:21 GMT  
		Size: 4.7 MB (4705645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:496d0215d46a7cb0b4c4a4d32c7d2a98c27e9e369e0d4c3d27617116b54922d2`  
		Last Modified: Wed, 29 May 2024 19:58:21 GMT  
		Size: 16.2 KB (16159 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.11.3.1456-bookworm-slim` - linux; arm64 variant v8

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

### `clojure:temurin-21-tools-deps-1.11.3.1456-bookworm-slim` - unknown; unknown

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
