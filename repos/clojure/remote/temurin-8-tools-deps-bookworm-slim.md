## `clojure:temurin-8-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:67661211571857e28bd20d438415168b362bcf52f56959a7aeac1416716427b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ece9522e23826a6da71393ab57daed82408c14003f13493a9120f43f4bc07343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152477763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:679ea9e89f88cf420b4201605ed79b377da61ef4e418f835b528894cf0209381`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef0548d224b83376a60f405481ba646f0d97ea531021f41cb2801a144591656`  
		Last Modified: Tue, 08 Apr 2025 01:35:19 GMT  
		Size: 54.7 MB (54721226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b93f688568f66be102ac95d403c7e4bd30813a0b10cf0a278011afaa586930d`  
		Last Modified: Tue, 08 Apr 2025 01:35:20 GMT  
		Size: 69.5 MB (69528632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a45523932f3b859a9ea33b7db570767df49fcf793e636f3c803103f4fd3f07d`  
		Last Modified: Tue, 08 Apr 2025 01:35:18 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0458d5e243350b0694f3fb9b0e2280274ab0fe00d1696d7338ecda8e56473140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5049866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a7b3ba2d6503e606b9df35ee5af17ed5b5a5859fff235a483d345ae284fdfce`

```dockerfile
```

-	Layers:
	-	`sha256:f399df84941e7a397a7a9ca73c5acd319cda0e023e2b24043f9fe536c7d9d3bc`  
		Last Modified: Tue, 08 Apr 2025 01:35:18 GMT  
		Size: 5.0 MB (5035575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a990bd125d6452b4101384d1cdf4053800c4dca1bfcec20e89a76155b80a303f`  
		Last Modified: Tue, 08 Apr 2025 01:35:18 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:146b10352e113708a126712421ddfec23956a79629610b439b938608e729e15c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151245077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5f9b20ede0bc9b8aa0dae59a252db0912b524120d425d13644a433d09774017`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 08 Mar 2025 19:45:48 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2428da9ac78ba6744298118e80258c610cbec1788af4ca9d2030790bb99e2bf6`  
		Last Modified: Tue, 18 Mar 2025 00:19:14 GMT  
		Size: 53.8 MB (53822778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5341f4c229ed19b47de7125a158f81cc8402adf15dda4a680cb6c98fe3ff9db`  
		Last Modified: Tue, 18 Mar 2025 00:20:07 GMT  
		Size: 69.4 MB (69377618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06067a9be6a756336d8c0f77fd18bb4ed0722e47c4fba98e8eb86ce86dae12ca`  
		Last Modified: Tue, 18 Mar 2025 00:20:04 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b67b7f2ae165e07bb7d8bdb1e3f78037f800a04ca17251b615568fe7b525dc89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5055075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecab39496655fcad8968e38a20e96388f450f4f85a064a78ef04e8cb503670cc`

```dockerfile
```

-	Layers:
	-	`sha256:066b22a3c846d8ab1c7b0a605afed6b21d3876ef8acc299b134b7b9a64d905c2`  
		Last Modified: Tue, 18 Mar 2025 00:20:04 GMT  
		Size: 5.0 MB (5040666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:436ea294462d99e97c3e0e7b4c8221c27ab5e93364e4570d42fe0ebcbfbfa643`  
		Last Modified: Tue, 18 Mar 2025 00:20:04 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json
