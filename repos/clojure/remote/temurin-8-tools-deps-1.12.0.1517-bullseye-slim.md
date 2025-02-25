## `clojure:temurin-8-tools-deps-1.12.0.1517-bullseye-slim`

```console
$ docker pull clojure@sha256:91c900bf81908b0c4b707b514a4b3218b0dcdb73a8533276ee5850faf387859d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.0.1517-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1de68ebf52c731c6106ed7d353f7fa301fbae2d7de4b7dcc22bda0538e02c28f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143764242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83139fbbba937cce9c6a1ad529a3bb64e5252384b5054dd45aaaac00cadbd59e`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 19 Feb 2025 14:51:07 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c4ff3df84a0c586964c1da8f9b9ef42e07e8fa95825627b7d9b48b34ca9023a4`  
		Last Modified: Tue, 25 Feb 2025 01:29:38 GMT  
		Size: 30.3 MB (30253930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ddf85ea66abdecb4d14570a54b010d5f450f6d5fdc21a257d657c63381f8a1`  
		Last Modified: Tue, 25 Feb 2025 02:15:27 GMT  
		Size: 54.7 MB (54721245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11cc6f8e7093b9779bf1ac0456b1d7f09c810cb7464780e83adb4c55bd25c517`  
		Last Modified: Tue, 25 Feb 2025 02:15:27 GMT  
		Size: 58.8 MB (58788422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac28fbdbebaa0cae9aa13723cb420df47e0dd81078fd1a04921d17958b00e32`  
		Last Modified: Tue, 25 Feb 2025 02:15:25 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1517-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f8a886d30fef965e9b31cf8a5d8b80f8c0c7e68c280fed556d4b7ea56fbb5b00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5252968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77ff5c3bcfdbe1b63a99509c826ebc556eb888785c2ee51fb576991014a89ce`

```dockerfile
```

-	Layers:
	-	`sha256:1ac01d29ffbbdcaef5f1b03a0d4f8c32c58559cfb11b783d5d1ae1044cdbb9e0`  
		Last Modified: Tue, 25 Feb 2025 02:15:25 GMT  
		Size: 5.2 MB (5238677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db1079252683f6cddac70ac98c52a9f1a73087ed68db466c7e474f09a7a8948f`  
		Last Modified: Tue, 25 Feb 2025 02:15:25 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.0.1517-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ee0d1772368a499942115eab722abed0ed1c550d2a01fc94a28f366f9ae86e94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141479846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad1e864826b3e468f7a1f49a976dba85850ba4e019be312bd0bfed1a0b19781b`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 19 Feb 2025 14:51:07 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c4c6d622e13259683de05019144b319d210aaf74faadf38f9ff2c9d56472ab51`  
		Last Modified: Tue, 25 Feb 2025 01:31:29 GMT  
		Size: 28.7 MB (28745987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9faa5996a9afb25a64d24de3d399638b37871d363eb2836265671e942ff7a1b6`  
		Last Modified: Tue, 25 Feb 2025 10:52:16 GMT  
		Size: 53.8 MB (53822757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d271dc4e53ddce537c69cbdc490856ff1ff22df64f58cc1bc7de31164b29c0ae`  
		Last Modified: Tue, 25 Feb 2025 10:55:10 GMT  
		Size: 58.9 MB (58910455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96014c87670aadcb0eb5560160291960dc6b79203388b86cdb321ee2b554187`  
		Last Modified: Tue, 25 Feb 2025 10:55:08 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1517-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c2feb0b763f500f4820f90ac2415332d17230bad4628561018fc4b4c48dc9f48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5259516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f3907557f7bd5581310bb3a080732535fe93127103ead74ef07fdfc108f02e4`

```dockerfile
```

-	Layers:
	-	`sha256:a45d4b5a2eacbe0d3a4ca40face33fffc13946c558a191132ce2c90bc65c7957`  
		Last Modified: Tue, 25 Feb 2025 10:55:08 GMT  
		Size: 5.2 MB (5245107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64df11d4f1bf6948c0a57a6e6e9a79b7d543391cff3a2da50a05188ea88be62c`  
		Last Modified: Tue, 25 Feb 2025 10:55:08 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json
