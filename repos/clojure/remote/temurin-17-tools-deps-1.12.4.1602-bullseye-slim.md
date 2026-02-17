## `clojure:temurin-17-tools-deps-1.12.4.1602-bullseye-slim`

```console
$ docker pull clojure@sha256:a6dd05c3ca0b3ac5afb24cd0fc2d16749faea5532da29c0f0b93546b81646702
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.4.1602-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7aa3f78411702bbf546d5eecf31f82416b6b43643cb64ac74b88adc6d6e29ae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (235025112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f600f3a4769c70b4eed2d6ee93e8e34f8789b36666f7464ff08644a92d38c0f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 17 Feb 2026 21:43:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:43:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:43:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:43:25 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:43:25 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:43:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:43:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:43:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:43:38 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:43:38 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345789a0e24ae3b1939078960a48b280c3d2945860ea79dfb5d764ea3b307ba9`  
		Last Modified: Tue, 17 Feb 2026 21:44:01 GMT  
		Size: 145.6 MB (145628753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929b148585c367434b3646ae545c5e300b49cbde1a3d8b8eaaa352206642e696`  
		Last Modified: Tue, 17 Feb 2026 21:44:00 GMT  
		Size: 59.1 MB (59137034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8844fba78239812e3f44d6dd6cd7156c5887b1dd75f98f4fab43f7de1f9dd1d4`  
		Last Modified: Tue, 17 Feb 2026 21:43:57 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd17af02bc6c051a86263deef171c49c4ecc6b678113d329c4c8de0f524fc65`  
		Last Modified: Tue, 17 Feb 2026 21:43:57 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1602-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f619a146a0edc9da29b7488a1a9a038df5cdef8369dba0ac935691be37e64da0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5325956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0ff6384fc06a5e05631033d9adbd2b0d6d97385db97fe5f8ec88afacf69a8dd`

```dockerfile
```

-	Layers:
	-	`sha256:fa69552a900c924da299a5e371807d83e0fa4f878b237aa3c228cdca1212d767`  
		Last Modified: Tue, 17 Feb 2026 21:43:57 GMT  
		Size: 5.3 MB (5310120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3237ec23ccd916dd4357c605d7bfb43d965b909ec1455c728c95aae7fdd593b2`  
		Last Modified: Tue, 17 Feb 2026 21:43:57 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1602-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:061770cdb8a7ebc8b0cf70a18a04d35be6ffaaf0e72be3a5511eef07458fd682
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232469795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fecaf704a56562fa1df84730f629afe43add6b33bc16991ae626aa56fe4d684`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Tue, 17 Feb 2026 21:43:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:43:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:43:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:43:16 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:43:16 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:43:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:43:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:43:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:43:30 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:43:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0bab5b9a037a7924cbfa7e0cedabf52dc41fc1e49df102241165282dd277e254`  
		Last Modified: Tue, 03 Feb 2026 01:14:08 GMT  
		Size: 28.7 MB (28744439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff3336d47962acfa1c1c2a12ba7703a949f7f33bf1dc16a02bf9bc3d1d9c8fb`  
		Last Modified: Tue, 17 Feb 2026 21:43:53 GMT  
		Size: 144.4 MB (144436249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa69ca37778c022d869501a72aba09044b4f306d75a52b8b0409231849839491`  
		Last Modified: Tue, 17 Feb 2026 21:43:52 GMT  
		Size: 59.3 MB (59288066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5903abd6ab827f093fe42de57f835c56e9c9a95522a23f37556dd27982c11f7e`  
		Last Modified: Tue, 17 Feb 2026 21:43:49 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def79a2d54cbd9f6d12ec71b738e9f4a40a0af9a018956caa3885637fd81f9ab`  
		Last Modified: Tue, 17 Feb 2026 21:43:49 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1602-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9aaad02617ff90df743c10c2be114273ca58365f5b3eb36f00198051bd936003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5331806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb5a057be04048613806d9717adbce089ccfee7b7bf7c11eddf4460229270ff4`

```dockerfile
```

-	Layers:
	-	`sha256:72eee78ecb6d43efd0a95aae854db0964f15f54b6e7bf23c791272e1bfe811ed`  
		Last Modified: Tue, 17 Feb 2026 21:43:50 GMT  
		Size: 5.3 MB (5315852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05a22a3bc130568bcfebb96e3fb941789bf8c275316c8be396a19620442ccbac`  
		Last Modified: Tue, 17 Feb 2026 21:43:49 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json
