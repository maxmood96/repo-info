## `clojure:temurin-24-tools-deps-1.12.1.1543-trixie-slim`

```console
$ docker pull clojure@sha256:0f6e84048a34849af3085ad196dc6d943e41efb4aae7030a316b1ae21f41cd62
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-1.12.1.1543-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f173fac9321491bef63242610332c9bcb1f4644abfe93a7f5abe3ef5b31bcc1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.4 MB (194373283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4506da81717de4dbf37cb237e15d2cd3f299da028ba69e13775a3eb639d84bca`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ced038dea045df288fe9bdbe03117ca66fe2a071217e196ac86ed07f965fe688`  
		Last Modified: Tue, 03 Jun 2025 13:30:48 GMT  
		Size: 29.8 MB (29755384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476d54fe308c7e34a289d06169ac662ae27267f2391ce5a5f0251f140b35e9f8`  
		Last Modified: Tue, 03 Jun 2025 18:24:52 GMT  
		Size: 90.0 MB (89952003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5916c2cf94661d2173dad64ac1bcf5d27851dd5553d56770db160b0e15ff3e2f`  
		Last Modified: Tue, 03 Jun 2025 18:25:06 GMT  
		Size: 74.7 MB (74664855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397b5e561d94f0cb61c50d73c0e1b342490ad172a3e61a4b40e57596a0a0df5f`  
		Last Modified: Tue, 03 Jun 2025 18:24:49 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7023ab0472d7d3b7aa9098ab18dde36da2ccdad24467d23d608906651d1eb590`  
		Last Modified: Tue, 03 Jun 2025 18:24:50 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1543-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:740bd5b26f196a957d9acdaa5472e0c086c28f29b4e0026c8ca87ed6fb8d78db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5078559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a936f038f49981835f3a51a7746caf4b8e0bed9e5446d3804b916179d41d3d9d`

```dockerfile
```

-	Layers:
	-	`sha256:0e9de21643db86620bd968e8520a65d91ff6ed45a05e5495252feaa591c163ea`  
		Last Modified: Tue, 03 Jun 2025 21:43:54 GMT  
		Size: 5.1 MB (5062711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ed9c562d08a5d016d470d85a79212a826055d1d77f2c1c8e708a51b56c9748a`  
		Last Modified: Tue, 03 Jun 2025 21:43:55 GMT  
		Size: 15.8 KB (15848 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.1.1543-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8a3b865f62bceace01316e49fad08ab3de2d3675c7e83735fa624ad12817b5c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.2 MB (194179186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef4dc2fd1ff4228ee0c81c4d58e7b18cfbd11dd2f9563c2cfe34cfea5ff999da`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6098c2c9fa277c00ab580ce12bf64a9e1edf9e9139ba18ad85f3cc3063834aa6`  
		Last Modified: Tue, 03 Jun 2025 13:33:56 GMT  
		Size: 30.1 MB (30119455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9eae18b910302d512424dc442cd7d56bf789911ad2568ced024da733788c71`  
		Last Modified: Tue, 03 Jun 2025 11:10:25 GMT  
		Size: 89.1 MB (89091283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0f4e0de1c74d82e790ee36319079a32440fd6c9b942d3dbebe3d8b8e22a2ed`  
		Last Modified: Tue, 03 Jun 2025 18:57:08 GMT  
		Size: 75.0 MB (74967413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948fa9b50d31e3644154c49ab8703d998ad33fc59f9ba1a7f0390ca88b5f2b62`  
		Last Modified: Tue, 03 Jun 2025 18:57:00 GMT  
		Size: 609.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85006b6d762c39b55b67fa2f980f22cdc73b00b06cc8e4a60d5849d9181dba2`  
		Last Modified: Tue, 03 Jun 2025 18:57:01 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1543-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1287d1634052abd5265130a1f2ec7d3dc98d1a5c1767b67b6d8a118d90f6c2a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5084443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1258e5b09e1a7b4f297ef6677c55945955979504f1d23b505719ff0f3209dd37`

```dockerfile
```

-	Layers:
	-	`sha256:eda0a0ab3e1350e7c3f8a73eada2016007358b5f0f315da2da378e279f899ab6`  
		Last Modified: Tue, 03 Jun 2025 21:44:02 GMT  
		Size: 5.1 MB (5068477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:590cfac4f7741bc35043eedf20a00b9a41396ff7f805a204c165145213f303d8`  
		Last Modified: Tue, 03 Jun 2025 21:44:03 GMT  
		Size: 16.0 KB (15966 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.1.1543-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:35c491338477f43f53638e8f18e333e4209ea5052a181ebf638b86d1b5c8fcbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.9 MB (203903928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c1507ab7c51bb98f88848d340f587f2ddb95cee42b05d75e1f791bfbb62fb8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:62eecea9deba6eaccef3e829ddec51f2c540dbbb668a68816c8ce3c4b8023d93`  
		Last Modified: Tue, 03 Jun 2025 14:07:09 GMT  
		Size: 33.6 MB (33580565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9425324caed17cbe9579689cf7955835ba7b30d6602498824e5018dfaa80960`  
		Last Modified: Tue, 03 Jun 2025 09:32:38 GMT  
		Size: 89.9 MB (89920262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66a0f0a08378bb7d1452298ce5da9c1af012861849b18d29d183d3f217b02c5`  
		Last Modified: Tue, 03 Jun 2025 19:19:14 GMT  
		Size: 80.4 MB (80402060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372fa95e1805a17dea59e84e26292b8b71f91ec3285df1b9e542505cd2294c72`  
		Last Modified: Tue, 03 Jun 2025 19:19:03 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5250105ecd80f10956f4b3aa9ac92cf6653769d17c8e39df2a4ea0f963a8d191`  
		Last Modified: Tue, 03 Jun 2025 19:19:03 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1543-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3e2464934b19cf868cb93323ed536e03f465703b3240eb2f23c7b67d99049cbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5084276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28b63344da5c42b045a7cd87752938d5f86cf2f7f45088b9316ba83aff7ca70e`

```dockerfile
```

-	Layers:
	-	`sha256:bf897c11d603e3781682dc656720865de13a91cf3214a0a052ec9b63f7c5df6a`  
		Last Modified: Tue, 03 Jun 2025 21:44:08 GMT  
		Size: 5.1 MB (5068380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:923fcdcfa73daabec53e5faba81e66cc97a0ecbbe580821a9a4b9c8217c6b4d8`  
		Last Modified: Tue, 03 Jun 2025 21:44:09 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.1.1543-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:37065a8fa2639b9d7727bc012c4e8c617bba89d98784ca96d3f6c63ca3a14a32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.2 MB (189176937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a4900881ed2b2549bdd43ceb5d348377b305dcba885d3d915353dc2cf665087`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f092cb6a76bde9a7b3c337ea49e8a7adec71062dc5df097be99d3975e92bc53a`  
		Last Modified: Tue, 03 Jun 2025 14:07:17 GMT  
		Size: 28.2 MB (28245354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4940ebfc6f1c13fcbe1aced0ae631c0e454ff970d870d449e8b90708e20cd8c`  
		Last Modified: Tue, 03 Jun 2025 10:29:53 GMT  
		Size: 87.6 MB (87622163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c97e6283851aa9649922038603f23b6ce9dea2aa4318809812025ea78a3f51f`  
		Last Modified: Tue, 03 Jun 2025 19:30:36 GMT  
		Size: 73.3 MB (73308377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d11755d73a05b370ea3cedc7be564c1258b44fd3ad0ac7eebd86da2b20b29ea`  
		Last Modified: Tue, 03 Jun 2025 19:30:24 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca1644f6d3ab96d24ef3fb97ac16b02dda00054a1920da8e2e3f8bce4c8c309`  
		Last Modified: Tue, 03 Jun 2025 19:30:24 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1543-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:788d5a8aa6b253b8a7441f76ca6fd14bd3b57d2ec8008985a6079ce6a536cce4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5068068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8f7e7477e7538773076a7d82438965ceb410fb127754cc30bab57b0c2b73d9d`

```dockerfile
```

-	Layers:
	-	`sha256:3148d35b003e6104d0cf56bc5b4ff738d4f659b5d909d8c95b3a3f3114ff9f7f`  
		Last Modified: Tue, 03 Jun 2025 21:44:15 GMT  
		Size: 5.1 MB (5052172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:835a4307afa29a2e5f50c8cac2d623e2ea08bf9a2c3e1f5d96df2ad97d666f66`  
		Last Modified: Tue, 03 Jun 2025 21:44:15 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.1.1543-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:263936c1036faed7668f6bd0062070357f9550c85e19332c65a9f8a9bab881c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.5 MB (190453472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:059efaeabaeae8aae8b9c7996a7ab868827520db514dd4c06036c0d0f91e6505`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7cbda353d6047374e3da60bdf79ae89f8047840010f0964c87a8f2714e146106`  
		Last Modified: Tue, 03 Jun 2025 13:43:57 GMT  
		Size: 29.8 MB (29829620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e16c52945849bd7ff81f8fad1acf7f6b275ebd424116d7c5e5b466881d6e648`  
		Last Modified: Tue, 03 Jun 2025 06:39:48 GMT  
		Size: 85.2 MB (85216842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a1b695547b8924aeea480a370d7b8d64f46ba18a05b95e4b144df61e684b20`  
		Last Modified: Tue, 03 Jun 2025 18:47:46 GMT  
		Size: 75.4 MB (75405971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4aa46a8bc88767ced75e2d5f1476044991bf38dacb68fa2b398f9a077491379`  
		Last Modified: Tue, 03 Jun 2025 18:47:42 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1e4cde7eb632fc3e27e931f340c5f8a87a374ff173b3224cf212c65c1f4717`  
		Last Modified: Tue, 03 Jun 2025 18:47:42 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1543-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6bc7bc4d545b9cbf1aadfe80bb5d5fb8f1b896783ea6b38db6852e9c62a32ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5077030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dbee37f049630467f3078f0c9b058016a7b2c54d6f22919ef40f6f3c6276099`

```dockerfile
```

-	Layers:
	-	`sha256:e361b78c571b364925dc8fc538bfd162c77cbe18d995946b5e2202d7fd8aa4be`  
		Last Modified: Tue, 03 Jun 2025 21:44:20 GMT  
		Size: 5.1 MB (5061183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bd7c4763022c5d4b7437c3bc6a5054716c44508d3f5575188f227b48746d2fd`  
		Last Modified: Tue, 03 Jun 2025 21:44:21 GMT  
		Size: 15.8 KB (15847 bytes)  
		MIME: application/vnd.in-toto+json
