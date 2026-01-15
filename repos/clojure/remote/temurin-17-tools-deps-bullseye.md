## `clojure:temurin-17-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:1297db80694b106318c418adac0ad6a879ea7506809441da8f30b753be0b0dbc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:09a6d0b3384189321c1482b4daaffa4a8d11effe106a49ba4dd930d7bd0b10db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.2 MB (268162178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e8d145526b2621b5ea91a07fbfb29737a8072314f1afb7570abc38e37297f7f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 03:32:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:32:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:32:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:32:19 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:32:19 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:32:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:32:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:32:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:32:34 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:32:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fccfc62cb15165379a658b98df1680b95e3908f69adc8e7176a095a7b4cf2106`  
		Last Modified: Tue, 13 Jan 2026 00:41:36 GMT  
		Size: 53.8 MB (53756446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cf20f82676b882d3aba3771042795c802fefb9bc8c0af7c6b7d2904dbab669`  
		Last Modified: Thu, 15 Jan 2026 03:57:03 GMT  
		Size: 144.8 MB (144847921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34133309cc278bd2914e98408dfd3d4eed2202ba420da8b757f551c4a3980a4`  
		Last Modified: Tue, 13 Jan 2026 03:33:10 GMT  
		Size: 69.6 MB (69556773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d9f1f3b0c06fc6b20e4ea36366193b7c86e3a867ec58f6d6ba7831393ddd74`  
		Last Modified: Tue, 13 Jan 2026 03:33:04 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c580cafc22050e4fb3875b86000964ae955ef2f68172224ec4e42eb94ef6b280`  
		Last Modified: Tue, 13 Jan 2026 03:33:05 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c5fc96be5de8896f31d848b6db55bbe5bb8ce292a699ee710ced1b95ac9c0719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7411447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf3f1898b4d8b8467ce8cc6b003fde1b3ad354a01059b934b486707df0f65165`

```dockerfile
```

-	Layers:
	-	`sha256:b37b7a28fed83216e62134f925f810ba3f103bc63d36a50d1a7a5e17d6427087`  
		Last Modified: Tue, 13 Jan 2026 07:39:35 GMT  
		Size: 7.4 MB (7395669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c85303e6fefb23c3d547140b7b29a381039d4a655613fe7582d8e15ddcfd58ad`  
		Last Modified: Tue, 13 Jan 2026 07:39:36 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a778ce4389d63250ef957784a414286bc083c4bc65268e2d0b830e06abc95ab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.6 MB (265625684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef646db908cf669849167c6d962f5b744871fd6ef4772fd74cc1e8517ee5c353`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 03:35:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:35:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:35:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:35:43 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:35:43 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:35:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:35:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:35:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:35:57 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:35:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0c9029c19a9aa67ff2b1313f591bcb473f0522775cc5a54491b5f7754253c547`  
		Last Modified: Tue, 13 Jan 2026 00:41:52 GMT  
		Size: 52.3 MB (52257769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819411190735cfeb7bb7fdde3fd70691a4ed8c2f75ae0fcc6663ca3bd26e6fd0`  
		Last Modified: Tue, 13 Jan 2026 03:36:21 GMT  
		Size: 143.7 MB (143679886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b18a4aceadd6cfce8ad98f770f59876978c6596ba689a51892bd5f1cb05f1f1`  
		Last Modified: Tue, 13 Jan 2026 03:36:37 GMT  
		Size: 69.7 MB (69686986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45e2a74038dcbcfe7c414417b354332d706f55d7d3f35db99db0018ff1c20103`  
		Last Modified: Tue, 13 Jan 2026 03:36:28 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9efcb5b07ef131023440919b77c7fbdf4d682403d3fc451fb201ac98a967e660`  
		Last Modified: Tue, 13 Jan 2026 03:36:28 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:8c8669df7e588fd267c1f335675b8b7c0b2db035665d458b76799964c0ec3cad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7416664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d05d05eba41e7fe87545c9089c8360851775344251e59c8118c1988d46d0686`

```dockerfile
```

-	Layers:
	-	`sha256:1577410b07b5c9c7421c6a136002db22917a34c54fc4840e0ac25af8d7f73f14`  
		Last Modified: Tue, 13 Jan 2026 07:39:42 GMT  
		Size: 7.4 MB (7400768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a57234469690f1bab0c990dd1fb077f2f8a206a688d5354a11c30cfa1dac7ba2`  
		Last Modified: Tue, 13 Jan 2026 07:39:43 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json
