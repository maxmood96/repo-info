## `clojure:temurin-17-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:f27a0564cce6a104fa106cefad6623acc8a38205a0deb511898b6b6e81af0187
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:66af64766e7cc22a6792f52316c9832ba904e3f8bb123aa614e5939a917ed26c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234257369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:639682a76f2650d5cfe8b7a564186f9b48b0fce94b07aaa746f1a5e79f4bcefe`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Tue, 30 Dec 2025 01:00:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:00:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:00:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:00:26 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 01:00:26 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:00:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 01:00:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 01:00:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:00:40 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:00:40 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:37b52eae712b138ea3c9639c687f975153ccba96801de3dc69883975843edb35`  
		Last Modified: Mon, 29 Dec 2025 22:27:47 GMT  
		Size: 30.3 MB (30258441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf73e9da6b8b4321b6d5293c69535afcfc7e64e3e386926a12ca3161d37df87`  
		Last Modified: Tue, 30 Dec 2025 01:01:21 GMT  
		Size: 144.8 MB (144847979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083789e80846f3256d71512b96f0342ad9f0026c004330c93ce0fc7d741f4f94`  
		Last Modified: Tue, 30 Dec 2025 01:01:16 GMT  
		Size: 59.1 MB (59149911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1a1bed5af49e458e913141a67612d0518b9de6aea2057e1fed62145071602c`  
		Last Modified: Tue, 30 Dec 2025 01:01:10 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464179c3537a2e1e12fd3cf8f81b12ad73752940fde9d8c84fa99ec387d7ed1e`  
		Last Modified: Tue, 30 Dec 2025 01:01:10 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b34f52651bcf46de87abb73077d1bf380ef7eb91f9de09ff21ba3dc3be91b9dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5323905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a420b1246ced407c25cc6ce55e0b834bd9e38ede16026bb2095e58d60f0439c`

```dockerfile
```

-	Layers:
	-	`sha256:b034355492fd84348c5a256044838f03f819274c956e7c719b36f87a8614800a`  
		Last Modified: Tue, 30 Dec 2025 01:36:02 GMT  
		Size: 5.3 MB (5308069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56fdda78326e4c0428de84bdba31a894acbe334c533697e4b707d5a5c217d6ca`  
		Last Modified: Tue, 30 Dec 2025 01:36:03 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1a821945fd3d94d87e9d6bdd181def30b6c083ccc897ea1017f246a16a3e861d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.7 MB (231713693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d94eeb3cc4721fe66674ad03fe36955fead7bab242fba9acc3a11bf673ccecda`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1766966400'
# Tue, 30 Dec 2025 01:01:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:01:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:01:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:01:00 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 01:01:00 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:01:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 01:01:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 01:01:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:01:13 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:01:13 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2b952d66bc8c719b5ca92eacb4307075591731bdc405a12ebd6fa840a24375b7`  
		Last Modified: Mon, 29 Dec 2025 22:27:18 GMT  
		Size: 28.7 MB (28748462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26b8a63816566adbe3ed190c8fc6667296adf2d1b646e44221e67e3b80ab037`  
		Last Modified: Tue, 30 Dec 2025 01:03:23 GMT  
		Size: 143.7 MB (143679920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a200654fa494658eced5b9bb01b1b32ceabc6d5b60437b11c8080cb8efa77c`  
		Last Modified: Tue, 30 Dec 2025 01:01:49 GMT  
		Size: 59.3 MB (59284275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ebccc87e2bf718cac3101e256caad62ce416339980c0e1f9fc9ded1689436b`  
		Last Modified: Tue, 30 Dec 2025 01:01:42 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd2ae49a76379bfcc488eee3fa28b6d03f219d2e9599546d133cc639be7d12a`  
		Last Modified: Tue, 30 Dec 2025 01:01:42 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:24fc5c8572d33587d7ee70bf6e798d6768862d35cfae1106f04e5e86ea396f27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5329755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0edf06275c82c7b5d6de678dad370c894e108c1fba8bc2b53ae919b8a4898975`

```dockerfile
```

-	Layers:
	-	`sha256:d0b6ab505ad84d8e5a199f8d08199067ddbd5a7acfbdc74267958818c98a2b80`  
		Last Modified: Tue, 30 Dec 2025 04:39:53 GMT  
		Size: 5.3 MB (5313801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac26ebffed54935361525fa97fcfd483f576a13d0ec50ee3ec92121ad74486ad`  
		Last Modified: Tue, 30 Dec 2025 04:39:54 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json
