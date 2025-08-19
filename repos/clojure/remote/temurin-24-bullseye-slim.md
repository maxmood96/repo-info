## `clojure:temurin-24-bullseye-slim`

```console
$ docker pull clojure@sha256:ed09b340bdc5a4d07429d9476c82a88a813f69faae41772a8bd51bdb072c8191
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d667d9e20777ce2799d41993c14fccf69a8d8f971fdf58a80c144d80704d341b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.3 MB (179284870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:106ed96e4f7a628bcb550b34cbd551b8d9cd6dcf231fc4b7480241c7c170bfc2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3e41ca17193bcd7630e4dd210602930b1f94464bdd59680bbf6654206f7707b8`  
		Last Modified: Tue, 12 Aug 2025 20:44:40 GMT  
		Size: 30.3 MB (30256118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44f5a94a21e4adc15b35d9fd9e93abefe973ffe7299210fb9185b861532894b`  
		Last Modified: Mon, 18 Aug 2025 16:53:28 GMT  
		Size: 90.0 MB (89975262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad6dd43586a2c41a16179185a1ac708149e88b303977b5aa1f7425cb93ff2c7c`  
		Last Modified: Tue, 19 Aug 2025 03:09:44 GMT  
		Size: 59.1 MB (59052445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10413cb4844a216a8755a533408fac940d909fd12429968b4a89ee08d9397f06`  
		Last Modified: Mon, 18 Aug 2025 16:57:25 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da412dc595361ef84b12aa7d8a422a069037488b2bf3ea56211f65f8cf6e956`  
		Last Modified: Mon, 18 Aug 2025 16:57:24 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:259fdb9146f993a236d9623f9b1d9862da2940df6308ff31fcb679eb11674da8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5274587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:016e09b204c6a73630b24777b824efc34d81cb731b5502f94d3b0285b1ef11b5`

```dockerfile
```

-	Layers:
	-	`sha256:780a68ed545ffc725cc890ef4b3e13990640c83985f62557b6d25beceedab486`  
		Last Modified: Mon, 18 Aug 2025 18:42:54 GMT  
		Size: 5.3 MB (5258715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f495b282fa780bfb905f5972c1e4cb15e97cd5bfa7e6f58cdc12c8bdc75f86af`  
		Last Modified: Mon, 18 Aug 2025 18:42:55 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5f8fc6e16ead59bd3a6a7a2493292e32b55b86eb54d8a4f217a9b8594f2266dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.0 MB (177030842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0156e5cbd2494bd35d027055d0802b9fe0029236d0509015d17b3f8b820afdc1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b99ef417bc3eb3946e7b3162f6c19dbca1039f3b4124deb116c3a0ab763e65ad`  
		Last Modified: Tue, 12 Aug 2025 22:33:30 GMT  
		Size: 28.8 MB (28750491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba3d12b45d8e4d10ca991b219a355a4f41aa2138be3962b8523e2c567bbad12`  
		Last Modified: Mon, 18 Aug 2025 17:22:57 GMT  
		Size: 89.1 MB (89092530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7cee2dc6d36d3af4b73c231af9dffa3fd3ce1aea4280d4014232385c1ce599e`  
		Last Modified: Mon, 18 Aug 2025 17:22:43 GMT  
		Size: 59.2 MB (59186782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d94e726f7c3d51b47420ac7b59d1b4bed6bf5f520f5d0835b9e5d8e697ca78`  
		Last Modified: Mon, 18 Aug 2025 17:22:37 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1a0d4cf121c4e93618beb627182801af4e6e84e612b29286179dc7cb4cdc54`  
		Last Modified: Mon, 18 Aug 2025 17:22:38 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:87c9d8e23a995a0b999f94c84e47e54b22a23437997fa9077cb3fee649544340
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5280434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0097b9b5822fa908fce9ffd0117d07bbee463040279e769c654657d72663e57`

```dockerfile
```

-	Layers:
	-	`sha256:b5968f0bfe88c8e2447b3ba53efeff1c404c70fd3f95cfd1188b5ac7374156e9`  
		Last Modified: Mon, 18 Aug 2025 18:43:00 GMT  
		Size: 5.3 MB (5264444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abced31cf9c18f80a797ea5f38a73c55dc6c38334c73e39f5bc11b8f64d281a6`  
		Last Modified: Mon, 18 Aug 2025 18:43:01 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json
