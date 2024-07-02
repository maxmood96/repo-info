## `clojure:temurin-22-tools-deps`

```console
$ docker pull clojure@sha256:166865a447a968f7a8cdc14d5e0eef3db0c4757eae555c840ec618ec5082cc87
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-tools-deps` - linux; amd64

```console
$ docker pull clojure@sha256:a5dc363e90d0ddfe63f465c5e5da33fd1055348232bc6d08b76b4d78cc7cf7a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.8 MB (286782752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07de85c1dd18187befe74d484190e61fc07cd7b4691b51b3b27bd73acac0f5b5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:e8aac9b1598114ead96b4038c19d915b87f662ef342291d69c7e5255c5d731fc in / 
# Tue, 28 May 2024 15:17:11 GMT
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
	-	`sha256:e9aef93137af6e967e7242f3b3c8ecd8e6f571d1e6fdd9e72db0befeeae3cf13`  
		Last Modified: Tue, 02 Jul 2024 01:28:26 GMT  
		Size: 49.6 MB (49554064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18c7af59b2691506eaa321edf8b9d275b9a02b7c618750f2179fd675fed0f40c`  
		Last Modified: Tue, 02 Jul 2024 03:03:12 GMT  
		Size: 156.7 MB (156715520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f829ddf2d900269079cd8fd06a67c4a0b368945a3c3ed4c6b90c77c986e7e25`  
		Last Modified: Tue, 02 Jul 2024 03:03:11 GMT  
		Size: 80.5 MB (80512130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76541f235fabc872e9039fac0f00ff91bc1fddc19f61b16a9124745d34566d76`  
		Last Modified: Tue, 02 Jul 2024 03:03:09 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a58029ec7a60f54975a9f20ab8b387cafd560cf04bd6c9d0eed18bb3c83b083`  
		Last Modified: Tue, 02 Jul 2024 03:03:09 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:90ea2a91204560b59a72f0f7c7d4f78f05663160f52f0c2468c2cc006226c90c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6976761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b34d76b80233c0bf98c51829a078444b26b783973b74b6cc4bc062c24b81c7bc`

```dockerfile
```

-	Layers:
	-	`sha256:49e6ef130609910eeb39ed1cf566cbf3e6ca16188b0ee579738aa16331631a4b`  
		Last Modified: Tue, 02 Jul 2024 03:03:09 GMT  
		Size: 7.0 MB (6960639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c19b12a21e8a59ddd85bfeb49c9def409dd49bcf326d6ce0b970540d97dbe36c`  
		Last Modified: Tue, 02 Jul 2024 03:03:09 GMT  
		Size: 16.1 KB (16122 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-tools-deps` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7d09b526f2dad0be20a27aff976816da1c4ba077ca4490f2d31ada3e52161907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.4 MB (284397055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72fdd5bd88f49b42e67a6461e88d565c28ac4a056116826c285276a3691f508e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:cfc8f76c8181d3ae6dda16ae894b184c69dbba114d446426e466126fe0ae62e5 in / 
# Tue, 28 May 2024 15:17:11 GMT
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
	-	`sha256:1e60a453843e00d6f3d4242dbd696365f0894e3ca2f02f4ce1ab098d7ff7907f`  
		Last Modified: Thu, 13 Jun 2024 00:42:50 GMT  
		Size: 49.6 MB (49613402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a7de9ee68abedc6c5a307899774444d3faa4324c90df9c8bb81d7c84f33414`  
		Last Modified: Thu, 13 Jun 2024 11:59:37 GMT  
		Size: 154.7 MB (154738035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:700d1b3ef1da44e6e96f3ba993d36f968ea1a8ce71de573c05b2b4ba87f4b030`  
		Last Modified: Thu, 13 Jun 2024 12:03:16 GMT  
		Size: 80.0 MB (80044571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f2425113bbd696cb4e059bc20b86840300e4fa5503e4fc2b84e6b75e1734cd`  
		Last Modified: Thu, 13 Jun 2024 12:03:13 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f1e3a0b8f135dca52f9913b27d27f3f813b7e29e421eb606e1ef99cdb8c451`  
		Last Modified: Thu, 13 Jun 2024 12:03:13 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:6bbea5642e92098ca260374db7b2529d3f18f093007d3bb65839d9448449cfbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6984437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb57a8a5db454a905eeba35f507abbf68b33d2ee898012aa25327fae98237d9f`

```dockerfile
```

-	Layers:
	-	`sha256:fb2a0720afc0f2141a75d2273474d53178626e2351bb34d1e17a70f06c3bb4e5`  
		Last Modified: Thu, 13 Jun 2024 12:03:14 GMT  
		Size: 7.0 MB (6967755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c836e2dc742b683315db1fc9b5442de6d214487bbfc00c5e4587deebf997400f`  
		Last Modified: Thu, 13 Jun 2024 12:03:13 GMT  
		Size: 16.7 KB (16682 bytes)  
		MIME: application/vnd.in-toto+json
