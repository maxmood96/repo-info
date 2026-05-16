## `clojure:temurin-26-tools-deps-1.12.5.1645-bullseye`

```console
$ docker pull clojure@sha256:79c33364af6bb609f65145f3b3066724bd40ac91032c58bcaad075045e0a16b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-26-tools-deps-1.12.5.1645-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:4cafea76c63dab202d466faffdd836d322bf1f646dc92c1a6832fdf1d84da05b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.9 MB (217890873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52af6d0ea379c1d95cf02f23733c910c11770f4e4c9c06fc7cbc37b0c6de0607`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Fri, 15 May 2026 20:37:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:37:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:37:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:37:22 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:37:22 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:37:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:37:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:37:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:37:36 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:37:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1c662d8f6b122c4f09d6ae1b210df55a5ba6e7b529807c0757ccba0c1ac508e0`  
		Last Modified: Fri, 08 May 2026 18:23:06 GMT  
		Size: 53.8 MB (53763343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb4a71f078b9cdfa695e462869b254c13b3fea137800832e469224cf756a7ef`  
		Last Modified: Fri, 15 May 2026 20:38:10 GMT  
		Size: 94.5 MB (94524384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b77adcb5435e049d239ce45b4fddd34e83c7066a52639f72706f548cad7ef1c`  
		Last Modified: Fri, 15 May 2026 20:38:08 GMT  
		Size: 69.6 MB (69602103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa2738a5f0458dfb2af951fabd2aee8b7fd0d5d8db63dee381b8c6edd19a91d`  
		Last Modified: Fri, 15 May 2026 20:37:55 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f997f5d6c6f16b99554312b691bcdedc92f34ca9052d3f20e18ddb1dd97a1109`  
		Last Modified: Fri, 15 May 2026 20:37:55 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1645-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:0f0b29dea4a46d8559f45512a28ae3e5fef73e8a84d4a7392c4140fda80e5f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7389094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75bfc9983a49ea4bb429b5dfd57f3d9d3f3f2a1f988e7a2c82ed7c180a30c433`

```dockerfile
```

-	Layers:
	-	`sha256:1e88c721b226006e770add690f6eac6c63bfc2e6482b697201b542e25efb1237`  
		Last Modified: Fri, 15 May 2026 20:37:57 GMT  
		Size: 7.4 MB (7373169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29151afa469446699e027448c4f06d1a3b93664ed94c39839f662e4a32bcbd7e`  
		Last Modified: Fri, 15 May 2026 20:37:54 GMT  
		Size: 15.9 KB (15925 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.5.1645-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:19df0743081ed77d00983345896e74a94c4af5ba557ef2bccfa82b4cb9054412
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.5 MB (215529536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ce8ce08b9bcaef7c1c8f6b7bdf8aafaa6c6ef03724a40ed9828e546d8e50082`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 15 May 2026 20:35:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:35:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:35:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:35:58 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:35:58 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:37:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:37:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:37:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:37:09 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:37:09 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:965b6eb1fb4a74ed46e659c8fd725e1bec9bed6684b59cbca85e48b6c25a32c6`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 52.3 MB (52253210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0711e4c3ba63b66d51d59d6a3c1724c26d046a86e82e8bcfd8798d86c1c8e599`  
		Last Modified: Fri, 15 May 2026 20:36:32 GMT  
		Size: 93.5 MB (93504386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2e8568f836bf7111ede5032d39af5c8dc9330f52bee20be28431c9b6e33bb6`  
		Last Modified: Fri, 15 May 2026 20:37:25 GMT  
		Size: 69.8 MB (69770896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6863428d09688d6a4f42842a9d724998072f319295d6c70723798f81b70eb640`  
		Last Modified: Fri, 15 May 2026 20:37:23 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10673b47193afcfe119c5ec7902d2478d4105090159a1645f311de3844a9037f`  
		Last Modified: Fri, 15 May 2026 20:37:23 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1645-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:f51757f1f3f62a5d7afda964ef37dc64b09fea73f2d4aa7df0f4cfb3ad08c005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7394307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbfdd2c55df133f28e0feefbceda5482fa5bfbbb004fcb143e6cbbea5f03dad7`

```dockerfile
```

-	Layers:
	-	`sha256:9fe447cff514e9c9151af2c50f90aa11ad117858b542d940be48893aecaaa9b3`  
		Last Modified: Fri, 15 May 2026 20:37:24 GMT  
		Size: 7.4 MB (7378265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4091b7b386414367301d43537f7e6cff85dab661d7bc97873207a128c74cc7d`  
		Last Modified: Fri, 15 May 2026 20:37:23 GMT  
		Size: 16.0 KB (16042 bytes)  
		MIME: application/vnd.in-toto+json
