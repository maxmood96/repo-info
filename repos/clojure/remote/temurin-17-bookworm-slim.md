## `clojure:temurin-17-bookworm-slim`

```console
$ docker pull clojure@sha256:fb0f595c2565be4736475c103fa0be2f5c8e07ebacfa1e070224c3ab5e5525c0
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

### `clojure:temurin-17-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:21e8955fa5bc069205230802b6ec6601d5a875344e54e2d21bc151cb92146238
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.6 MB (242601959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99e31678db168b4f96d945d53544357beea4f61e14f800875ba4b2752eb7a056`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:55:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:55:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:55:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:55:10 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 00:55:10 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:55:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 00:55:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 00:55:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 00:55:25 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 00:55:25 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e7c2dfcabbd60f415566180582d4149abbfa5580d10a03e55ca5459561e286`  
		Last Modified: Tue, 04 Nov 2025 14:42:24 GMT  
		Size: 144.7 MB (144693306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0bb0c0cef8fe095702970310d94cc4004c2f0b4fdaaa16459745cfd5873b90e`  
		Last Modified: Tue, 04 Nov 2025 00:55:58 GMT  
		Size: 69.7 MB (69679046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf8c4e4ca2405d8e5303fcc42dc32eec0bd96d4e45c009750d86ad74e6cee47`  
		Last Modified: Tue, 04 Nov 2025 00:55:52 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d179c685d392c8a1657034755e8f506d1641efd42eaf63bd5942b30f9839d97`  
		Last Modified: Tue, 04 Nov 2025 00:55:52 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ed04a02c4796fe4e8d2f48af49f1ce992c5d33b9e63c167521ace4c0e59330c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5129223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c240b96448895b7ca67b9187ecac68b25b71a545c5326628bab67619a13f79f3`

```dockerfile
```

-	Layers:
	-	`sha256:b0e62a476c2af782097fa263b709ddac30a9bac037a06771df76e3cf5821b3ca`  
		Last Modified: Tue, 04 Nov 2025 10:41:05 GMT  
		Size: 5.1 MB (5113388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8995fae572f872f5939939333c23e78ea9e914e2bba0297bb02401d228b118c`  
		Last Modified: Tue, 04 Nov 2025 10:41:06 GMT  
		Size: 15.8 KB (15835 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6e605c0f7efcb07d3ec86e0195d4d58aa6694acac19951bbdaa7a7df81dca165
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.3 MB (241343850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2217f9bf6393436972dba8a9d03bcbd7f453f62bd04551bc4cc5dff3e64d46dc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 18:42:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:42:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:42:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:42:26 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:42:26 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:42:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:42:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:42:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:42:41 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:42:41 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b4a8cf669b443f60fea528c8903ef54f42cc746d80ce9f8604361f417c6429`  
		Last Modified: Sat, 08 Nov 2025 18:43:04 GMT  
		Size: 143.7 MB (143680023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e1846730ff64a1d9b83d4fe5f25d2fc9b6b8d61724b039fa6fabfda7870bda`  
		Last Modified: Sat, 08 Nov 2025 18:43:33 GMT  
		Size: 69.6 MB (69560410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5efd8d041f5e4a0d2e3da752a35034635bb577c2de84794b828ef342369a2219`  
		Last Modified: Sat, 08 Nov 2025 18:43:26 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92dfacf23e367ea092af39b2d81ebf7300ebb4672c87a3bda560704b629e6524`  
		Last Modified: Sat, 08 Nov 2025 18:43:26 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7f4d6b82704591a80c0afb56ef3cd36703711e1bc919e305c00dcf62d925e838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5135105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd9c930df978c968514023577106b01f04061a16ff12bdc2e1ca48ce6617cc1`

```dockerfile
```

-	Layers:
	-	`sha256:3ec30c76dae23a7e183c8b20fc6de070a8a44b6660072f7a880ef50ccbdc2920`  
		Last Modified: Sat, 08 Nov 2025 19:35:31 GMT  
		Size: 5.1 MB (5119151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ed2f2c7b1c7119a8f21fb24431253461860635b01e97c55e8b4622711e1e44f`  
		Last Modified: Sat, 08 Nov 2025 19:35:31 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:aa149f594e57011eb693b4df089d542f8ff3545c59709808ba84172a247d601d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.0 MB (251956051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c98f9b013a466559615f277c4613d1bce14e8047fb57b861765f6bd485353907`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 13:22:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 13:22:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 13:22:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 13:22:17 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 13:22:17 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 13:29:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 13:29:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 13:29:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 13:29:05 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 13:29:05 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2442ae4ed78d32124d4f8b92ec0b1caf0e12483bafbd1803659dc391d3600616`  
		Last Modified: Tue, 04 Nov 2025 00:13:59 GMT  
		Size: 32.1 MB (32068905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d248f9e6208a1a73ad5c5558888e9316001bfad40f2ca4ef555c2c9fe0555fda`  
		Last Modified: Tue, 04 Nov 2025 23:01:38 GMT  
		Size: 144.4 MB (144372909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c167f5c0f064f07312a49e651edc0817fabd7da0a71505f17784e809c3207c`  
		Last Modified: Tue, 04 Nov 2025 13:29:58 GMT  
		Size: 75.5 MB (75513196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595990a25cbfc7351dbefe58dc7403c7778d805117c79456dd1e626f4e8f1fdb`  
		Last Modified: Tue, 04 Nov 2025 13:29:52 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9056e887d527efde9f70d884a305ccaa28a652db7d9b7b2d5d834a09a7c96a87`  
		Last Modified: Tue, 04 Nov 2025 13:29:52 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fa61530bc0d89ad4632f9311f7487784924780c20888a742e52d0744a1030127
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5133629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1f30854ca0ff57a28113a1f06b8c22df27f46356aaaca7370cd86bb83c969da`

```dockerfile
```

-	Layers:
	-	`sha256:142478b3fc7353ed1596979aeac5673c07d4843008c99655546a1d65d36705f2`  
		Last Modified: Tue, 04 Nov 2025 16:36:32 GMT  
		Size: 5.1 MB (5118546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fab5e3be3805a814464ebb644c67342793692654e445f023b1f51004e41befdc`  
		Last Modified: Tue, 04 Nov 2025 16:36:33 GMT  
		Size: 15.1 KB (15083 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:b89571b1cfc7487e77ce8fb0d0836b00d18118a3e7e5ab4579d4ef827cdd1a62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.1 MB (230099972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fb65957893273cc0a98fc24717d7c084750dde28fb247547043c92ef3962c3c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 06:25:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 06:25:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 06:25:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 06:25:31 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 06:25:31 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 06:28:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 06:28:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 06:28:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 06:28:28 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 06:28:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68313fcc31f44a191d88f4190e266c8e4565e424c2b4ba1e5c7a0cd4cba3da3`  
		Last Modified: Tue, 04 Nov 2025 22:42:25 GMT  
		Size: 134.7 MB (134723626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f50024d7374b1414f4f0deb4dfa8a1029de2e524f9cd07966a8cb5b742ab95`  
		Last Modified: Tue, 04 Nov 2025 06:29:05 GMT  
		Size: 68.5 MB (68490750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dc1451267c4d3978dc596e46a94c2a30551cdd4da9ef908992ff160a28d4aff`  
		Last Modified: Tue, 04 Nov 2025 06:28:57 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4061067046328cc4e8d87c68241c8f290f60b76336a56ae233514474b4f2cb7`  
		Last Modified: Tue, 04 Nov 2025 06:28:57 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b3faa8c3f8daffd45f4deaaf368a4e827aaf3590c4c7b134fd4e237a12e4cb64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5119744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d44d7714f6d11de065718f9b5cee5ef139e80e5e7c0b9de9485572036a01e7`

```dockerfile
```

-	Layers:
	-	`sha256:a0985e06d945326bbbab16014ecf1ee6413c2703016685cd688f128bde9ac56d`  
		Last Modified: Tue, 04 Nov 2025 10:41:22 GMT  
		Size: 5.1 MB (5104709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02a1a3f22dd1c65e5b1cdb5071a52f81b8ca19095049a165434af32a0d8debd4`  
		Last Modified: Tue, 04 Nov 2025 10:41:23 GMT  
		Size: 15.0 KB (15035 bytes)  
		MIME: application/vnd.in-toto+json
