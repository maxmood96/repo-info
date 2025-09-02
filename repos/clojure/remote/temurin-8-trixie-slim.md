## `clojure:temurin-8-trixie-slim`

```console
$ docker pull clojure@sha256:6ff1ebe840d534bfb72a6eac4c098d1b5ad3a2640fd11448ea63efc7c7bad588
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:be7dbafdc6a07447384158032b8cd2b4c4ba952da123ff9cfc1caaf7717b1473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156487985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76b67e96a4ce5326dcf29225591e8c3c8b0237bcba23771eeeba423149aca61c`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a4e0713c1c0b870472979bde305efa29d921decfab2c962b1c3f46d1562023`  
		Last Modified: Tue, 02 Sep 2025 00:16:57 GMT  
		Size: 54.7 MB (54731323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7869ab945edd40d0dcd3d3fbae535592077b5b9fe1879c317a2a5402f12a4ed`  
		Last Modified: Tue, 02 Sep 2025 00:16:59 GMT  
		Size: 72.0 MB (71982730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d66b4dcdd47fd024afddbab028db780116171c23e69bf24870e12f2976340e`  
		Last Modified: Tue, 02 Sep 2025 01:00:28 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d079af20fa629a79ba94d4346879529821b4c968ec33cecb5cc80e5b70307196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5391118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b97cea394aae6069311f046f11e5aa2d791e091c99c059c1dbb7fd2f7e51669e`

```dockerfile
```

-	Layers:
	-	`sha256:c6d82d7d4faf96e88f26bc362e19c3bc02b2dcf1edaa373a75a98c3701f2bd49`  
		Last Modified: Tue, 02 Sep 2025 03:46:47 GMT  
		Size: 5.4 MB (5376847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dbf5ca6b7933188285fc3aa47cbe57e75030f951534a8886e6afb4eae602649`  
		Last Modified: Tue, 02 Sep 2025 03:46:48 GMT  
		Size: 14.3 KB (14271 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cdb8f244b9c54c25260e52422b349b7980bfc19630d1906049e537dc2d74cecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.8 MB (155776190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28a4193a93e3758fd84432879588a6d6940191e1cfc40e4356b82315cb26184`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27cfc01299a2aefbcd2528420b2458f8e612ac351a67b5c408207eda11571f5c`  
		Last Modified: Tue, 02 Sep 2025 07:38:53 GMT  
		Size: 53.8 MB (53835608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975396f61c24e5ee1274056200b0f15893c0e6e0aaaecb6ae175983941b5f117`  
		Last Modified: Tue, 02 Sep 2025 07:44:25 GMT  
		Size: 71.8 MB (71803892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c05d2fc5f503ee466ad95b528a6c079321867f6838e6d1f6bb7a64d14f637a3`  
		Last Modified: Tue, 02 Sep 2025 07:44:18 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7c8b210ac48bfb5a63ae2e2faccadbac0f0d671bbdaa09a7bb794e44ee4df164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2246edccd9a33b1597f50d6a1f56eb0ba1fe28a6a44c1b60bc3a132781e12aa9`

```dockerfile
```

-	Layers:
	-	`sha256:e382b88ce54f331f6ec78851cd10750aae5c528582f355d2b51745bf01a710ca`  
		Last Modified: Tue, 02 Sep 2025 09:46:09 GMT  
		Size: 5.4 MB (5383314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:184f98d80c6cb1e122adcc2ee9ec92a6d1862e78861ddfa6d5328b95a4690ab8`  
		Last Modified: Tue, 02 Sep 2025 09:46:10 GMT  
		Size: 14.4 KB (14389 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:cf6d7d056f456daccb4279699e0a1504bb4d702367894192c1a84795f45e3534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.1 MB (163148985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c2c6a8e8012ecfb23e171665304a078e61cda426577c6d5ece568cb6b2cbf6`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b86b85d8e463227af39e173e64af903231b80321ea222465ddb24d5db1019a`  
		Last Modified: Tue, 02 Sep 2025 07:58:44 GMT  
		Size: 52.2 MB (52165455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f2490f5b0023a1fe4f541e09ce0ef61092086b8cb469e3f6009905babdd56c`  
		Last Modified: Tue, 02 Sep 2025 08:08:23 GMT  
		Size: 77.4 MB (77388670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c979b7b162b609a4fa6d1b97765189a44accb6b94113ff08179702a0d556d5`  
		Last Modified: Tue, 02 Sep 2025 08:55:05 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:931312eef923a5730b5a83a9a35620501768172dd5de274ab39730a7ecbde764
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5396130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f70aa4e3b870d09b120329af9670bbe47795f760cdba061188be932bb8a075f`

```dockerfile
```

-	Layers:
	-	`sha256:2c98164b781ff58d49d3c6d4bdea2b37c913cf89ba494388b38a6f85cfb2aa70`  
		Last Modified: Tue, 02 Sep 2025 09:46:15 GMT  
		Size: 5.4 MB (5381811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08da4cfcb53e12aa43d29f83d49c76b887ef60fa0cfc56e7fb434cb9fb1018c1`  
		Last Modified: Tue, 02 Sep 2025 09:46:16 GMT  
		Size: 14.3 KB (14319 bytes)  
		MIME: application/vnd.in-toto+json
