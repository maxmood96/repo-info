## `clojure:temurin-21-tools-deps-1.12.2.1565-bookworm`

```console
$ docker pull clojure@sha256:752b090bfc8d0171075ea9701b39e08b33f33beb7bc2b50afeeffdd5c107555f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.2.1565-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:8814d4583a174a6942a842cc36cb1a0dd802a34e6439d5d13fb73083c303176c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.4 MB (287424215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e87c7507e709e45b4507c7ccc6034fa07ea689feb76ef5541d8bbf327a0f590e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c9701605d9a3ad1faa4337faa315e0a434668779166df96b14eb60bc66c372`  
		Last Modified: Tue, 16 Sep 2025 01:07:45 GMT  
		Size: 157.8 MB (157804768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4deef49f82b45831984c5725b4bc3193352a437505ac8dcad2b02c07994431`  
		Last Modified: Tue, 16 Sep 2025 00:33:52 GMT  
		Size: 81.1 MB (81137792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5cc19ba01d651f3acaa170c56f3b1889ed875a9537f09e6b8908577b9ba515`  
		Last Modified: Tue, 16 Sep 2025 00:33:31 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4920b506be413e22fda36066d6cf66f88c1096f7019d9ee7c91782caf95e95a`  
		Last Modified: Tue, 16 Sep 2025 00:33:31 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.2.1565-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:71b31bd5300f2adfdea4c78a717d9f44746646d633ce30df11cb4aed6c408c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7397812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e279ca8567fc669d756c8ebe92f091349c81816b88b10bf3b92972257f4dbd1f`

```dockerfile
```

-	Layers:
	-	`sha256:d8cf41dee77df193e90f0a2521fb9bf2c9ffbc83f67743b1c54fa1f32bf953e4`  
		Last Modified: Tue, 16 Sep 2025 00:41:48 GMT  
		Size: 7.4 MB (7379992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:735fc5e6548f00aecf6b6f1f1a2809e7b1d1f6b294eb0d9f79e19ba1f545745c`  
		Last Modified: Tue, 16 Sep 2025 00:41:49 GMT  
		Size: 17.8 KB (17820 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.2.1565-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9aba700c18a720c2276e4472839393d40c3795420a62309e9b02d51f831acc04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.5 MB (285466911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ff49d35a21d7ccbb5648f7a9fa0f6934f2148fdbcfc6738062595b55dfe78ad`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c04143641a1317696daa1d0cfe8dd755f376701fbb2b0ba8a476d3943d8b725`  
		Last Modified: Tue, 16 Sep 2025 02:02:11 GMT  
		Size: 156.1 MB (156081177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8075dba3462502e2da4e490150b0eab04afb3616f9abea6b1d253337833b308e`  
		Last Modified: Tue, 16 Sep 2025 00:34:48 GMT  
		Size: 81.0 MB (81025673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce918f079fc22c51ae2a632a785592dd00fac4a2e0652de2a51edb9e04fa2ea8`  
		Last Modified: Tue, 16 Sep 2025 00:17:28 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03281699952b8b25078a6190ee1338d5e5d9298ed32f88e4b676029a0ae51342`  
		Last Modified: Tue, 16 Sep 2025 00:17:28 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.2.1565-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:cc20be01497612caa65c17b1c7300d7d5a6461e6fa05ed55641c42c0dfaf8c1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7403838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63f5ee29f3732e567abe3167882b90a3f6e1339048ee6ed1262d7e4ff3f119d5`

```dockerfile
```

-	Layers:
	-	`sha256:d33deb58fe980a28a0df50cba4ab39040973e4a23b266a2cace2df9bd42dcb95`  
		Last Modified: Tue, 16 Sep 2025 00:41:55 GMT  
		Size: 7.4 MB (7385827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86a34500aba0abaa4c83ff1e41f6a5bbc12f6de06ad703f3938b4fbbc30af68b`  
		Last Modified: Tue, 16 Sep 2025 00:41:56 GMT  
		Size: 18.0 KB (18011 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.2.1565-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:36349f20f6e317b3f39780275eef95ab91847faa5d60c408b862c9cc9088bfa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297269943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b20b49c9c7f6bd678957df3eaa01d675dc96dafc250d90cefc88772cc5b77ad`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:64b8116dd43c29a2a4aa3131cb4895af0a7267cc5883e3761556e54c369be9af`  
		Last Modified: Mon, 08 Sep 2025 21:22:08 GMT  
		Size: 52.3 MB (52326822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b2ca9ff1a3fccb012f6c51a9f097c6995575e5e55d69deb7d54ac91943ca62`  
		Last Modified: Tue, 09 Sep 2025 09:35:24 GMT  
		Size: 158.0 MB (157963479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ecc27473f629e5032921f972c70e466d5710100b8d9eec8dfea52f8199850f`  
		Last Modified: Tue, 16 Sep 2025 01:18:42 GMT  
		Size: 87.0 MB (86978601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374a78e022dd6b2303530ac34da9fb21e30596832e11a36edc336bbe1b0d2020`  
		Last Modified: Tue, 16 Sep 2025 01:18:38 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7c5a82e6107c12160f648a81d671c29603b437039397aa38b1990eb7ea84c5`  
		Last Modified: Tue, 16 Sep 2025 01:18:38 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.2.1565-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:1d4ab90d12877e828edcc0f158f006ee922b2090ce3fe5e1171418639930cad4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7403147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:477fe28f21c74b94545e53476048953a9fa87057b96187717274399d10d278bf`

```dockerfile
```

-	Layers:
	-	`sha256:14ddef5c66c289790bd14f8be08687f955d009766c8790eaae608fad468f6945`  
		Last Modified: Tue, 16 Sep 2025 03:40:21 GMT  
		Size: 7.4 MB (7385242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76901a2538f80aefce6a522d1efd3f7cec04b84a663238ba65370637399cccdd`  
		Last Modified: Tue, 16 Sep 2025 03:40:22 GMT  
		Size: 17.9 KB (17905 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.2.1565-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:e5f4337f18ad33481dfd6b656e1f35a03a850c9e156f393f935d750905e9afad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.1 MB (274115883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45625ca0110114a2a1a90b2ef6c128f80ee8458ccd61923381cc65e1bd85ed96`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:67e2d91fae4fd9af13e4e364bf8120dcca7856e8273995cc0651acae70b27e8e`  
		Last Modified: Mon, 08 Sep 2025 21:18:01 GMT  
		Size: 47.1 MB (47137539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84772536e34edd89b294c09dbe86293a053e24f7d3644f8bc0e4612df16f4795`  
		Last Modified: Tue, 09 Sep 2025 07:01:48 GMT  
		Size: 147.0 MB (147027040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d731d7168eb6874380022ba9abd9e616b1305328f80cdf80a8b6092dbe54e0`  
		Last Modified: Tue, 16 Sep 2025 00:53:54 GMT  
		Size: 80.0 MB (79950258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f970d4b29440b420e6f9f01fbe6d009d8e4987a2176ba25aaf129ada6251ed63`  
		Last Modified: Tue, 16 Sep 2025 00:53:32 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bc0b0b2a64faf08b475f2e9760293e4b6da02af1e892c64ce42c54d1ab2bd4e`  
		Last Modified: Tue, 16 Sep 2025 00:53:32 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.2.1565-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:33b611ff233a96197920e95b896572d8e46c39a67ea6c4374837e93c9d6e57b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7389132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a5640805782077e0051358745002c6eba9440f723be973f05a5d36e755a7ea6`

```dockerfile
```

-	Layers:
	-	`sha256:c56559ea17e709da534827418b13d38b2b8ca5547eb797b1bfdb66f8b16f1169`  
		Last Modified: Tue, 16 Sep 2025 03:40:27 GMT  
		Size: 7.4 MB (7371311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3d9e2bde53935b73b01a2743b5673e4d35302e7364f19b2bf724dadcf1c5e4b`  
		Last Modified: Tue, 16 Sep 2025 03:40:28 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json
