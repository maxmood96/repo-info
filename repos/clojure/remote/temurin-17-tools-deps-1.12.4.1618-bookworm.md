## `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm`

```console
$ docker pull clojure@sha256:36bccef488ce3f324b2f9daab5148e173c096a0a4e12e7805bb68cd14f9ca4f8
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

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:16e9b58f8db9563520b765e4030036c051abf084c6af3d905898566e5f990be5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.6 MB (275561666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db461adaacfee16750eac1ae0cd69f9a45091e52f35e6532b15ea68fe6983988`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:17:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:17:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:17:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:17:12 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:17:12 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:17:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:17:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:17:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:17:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:17:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5778c2dc7e37d458048d8dec91f7a444e6199011c8cddce74d8538d4647503d2`  
		Last Modified: Fri, 08 May 2026 20:17:51 GMT  
		Size: 145.9 MB (145905478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cdc88e54924ced955e8fc1f9703447ad030b495543179a57d87446263994e95`  
		Last Modified: Fri, 08 May 2026 20:17:50 GMT  
		Size: 81.2 MB (81166468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529a8e081f82048fb5bf0d8aeaf78a790d11b8d41d524be8060df1702a4e3a3a`  
		Last Modified: Fri, 08 May 2026 20:17:46 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba4b580a0fc9e1af231b708c540a99970d1ac43d707b0d6e11f06c679b84f19f`  
		Last Modified: Fri, 08 May 2026 20:17:46 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:078277f8f24ce70cab408a0d014b20799c9744fc7710ec6cca24accb0990a543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7394861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9b60d356e63b18018ecd5b9ae4c1c06c36f40dfaaf25609ecf1182ca3f4920f`

```dockerfile
```

-	Layers:
	-	`sha256:d36705ffc668aef3da62b387f4360de84d118db2fc102d95a450a77a7b3e939d`  
		Last Modified: Fri, 08 May 2026 20:17:46 GMT  
		Size: 7.4 MB (7378929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fe95f4e35ee1ae812d0a9c85efc3b90900e678d75faa81ebb1e8b49f1db715b`  
		Last Modified: Fri, 08 May 2026 20:17:46 GMT  
		Size: 15.9 KB (15932 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a7a7e85fb2f7519c2aac2a696261403c2e4aceb5204a56b2d21c761366059249
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.3 MB (274271711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed056a956724d3287bca6bb020fb196e1361cc1c96a52ba6e8ee139c371eb64e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:21:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:21:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:21:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:21:16 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:21:16 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:21:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:21:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:21:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:21:30 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:21:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304d7d18bca0b80fac43cafc6f88c8951c109808d6ab2c71d9e40627996f3e79`  
		Last Modified: Fri, 08 May 2026 20:21:54 GMT  
		Size: 144.7 MB (144724307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d611d208ef7421ba018a7c3957d72e1c8ca668ec100ca6a04d95c827a5010ed`  
		Last Modified: Fri, 08 May 2026 20:21:52 GMT  
		Size: 81.2 MB (81173211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d24616f28f5c5b23c205fc843ab600c847416efb9e44b3e24d16ae20a8e3e1b`  
		Last Modified: Fri, 08 May 2026 20:21:49 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06364b81f4361e1aec112b18176205ab2ddebbb77f532b572124d9fe707f81d9`  
		Last Modified: Fri, 08 May 2026 20:21:49 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:af657c55b6d39d1655bfd4b564693bf98b7a96d1ec21530345c57bbc8d48aa93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7400742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6699f92c0c0dfcea78e225fd01c0558127c3485ce5557b3ab8ef51a8753d344`

```dockerfile
```

-	Layers:
	-	`sha256:099ee5cc624cad83aceb45b51c394b7dac14299cd434a50840f078247c180359`  
		Last Modified: Fri, 08 May 2026 20:21:50 GMT  
		Size: 7.4 MB (7384692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65fa090d42b2f3cdd46aab0c348fecaf64f284011c26af3840cd17d5bebaca63`  
		Last Modified: Fri, 08 May 2026 20:21:49 GMT  
		Size: 16.1 KB (16050 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:2a074e76ea7dd7ac2f598b120a5a697b683323c88586b2b843ce8011d9834fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.1 MB (285107930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6cbcd34ec923f423294e2a6b5dfabaf9eaa183077b8e2956390cc99211e8f93`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 00:43:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:43:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:43:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:43:06 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:43:06 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:50:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:50:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:50:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:50:10 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:50:10 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0b84f035435acf0ec33df4748d96fad1243fd6b0ea9917f29eaa507d4c458365`  
		Last Modified: Wed, 22 Apr 2026 00:15:04 GMT  
		Size: 52.3 MB (52336735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1a630844f3ca330b4aeb3cf62ea83634554dfbe591d28cdf3d1bbe7c2c4aa2`  
		Last Modified: Fri, 08 May 2026 00:44:30 GMT  
		Size: 145.8 MB (145766245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0272ba3b63e5a8f5e8bc52fe20cea12d57aa685e78e0ed0e8af00c60cf28a963`  
		Last Modified: Fri, 08 May 2026 00:50:55 GMT  
		Size: 87.0 MB (87003907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8215814d5f034ca2952a3e5c8298434992e841ee59976199e6e4ac860f01ebb0`  
		Last Modified: Fri, 08 May 2026 00:50:48 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849cb1872f7a7b6040e25b46cafa38b3836f868c0bd8fe727e87e93b4a6b9bdc`  
		Last Modified: Fri, 08 May 2026 00:50:46 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:96204f32aa781fc50bfa1dcdc2fd0dc7486a4c99fe31a15bc2258d171ae2da44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7400125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0927093711b6dbf7ab5453ee99118f302728b18945324ab988c78d5e37ffba2`

```dockerfile
```

-	Layers:
	-	`sha256:395e89d7e8bf9a56feb11fea8e110fa5c94e92e19dece86398df4ce1372629e6`  
		Last Modified: Fri, 08 May 2026 00:50:48 GMT  
		Size: 7.4 MB (7384145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:273914722ce0d7618af61988c0d9814377953869148993433dfd00161d80bfe2`  
		Last Modified: Fri, 08 May 2026 00:50:48 GMT  
		Size: 16.0 KB (15980 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:b646082b1b2aa1086974d7bde1542abf4c6a99a225fde0deec7c868cc9b894ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.0 MB (263039422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de5422407ab87f9ae19fe32e6ec3673f823d1da7a5e972d11e4bb009be5d7bc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 22:14:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 22:14:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 22:14:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:14:57 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 22:14:57 GMT
WORKDIR /tmp
# Fri, 08 May 2026 22:16:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 22:16:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 22:16:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 22:16:10 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 22:16:10 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:124dbe049873037f973f01d877ec004bf4cd3ce5723d0b8f2067c58ad98137d6`  
		Last Modified: Fri, 08 May 2026 18:27:29 GMT  
		Size: 47.1 MB (47148023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c10a6897782f771d3606e3e80b8e1017d240690fd955802892aea8e434131f`  
		Last Modified: Fri, 08 May 2026 22:15:37 GMT  
		Size: 135.9 MB (135910446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a05c13535b222831e0447a40c6b1e3d0cad1e508e989d60fbafebf0fac87c0`  
		Last Modified: Fri, 08 May 2026 22:16:37 GMT  
		Size: 80.0 MB (79979911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c905fc8c40592c5d4cc6e2e6cab0668dc5fbdd99d3ab681ffd846533fd1f0644`  
		Last Modified: Fri, 08 May 2026 22:16:33 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19fb636bf4bfee053031c578c0ddeb23c58a2e043d82a1b54c333cfee417c1d1`  
		Last Modified: Fri, 08 May 2026 22:16:33 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:beea69a47065bda98e37a7f86d133bd36c41e73a20fbab732e80831c6f1bdd6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7386180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ae68d0da6dfee4de8a9bf72db21f8dc816d4040c6d0ca9299a4b15974a1de8`

```dockerfile
```

-	Layers:
	-	`sha256:4de682aa13cef293da4604149ac3a044c8a33f2e0ec30635a19030b08527aaed`  
		Last Modified: Fri, 08 May 2026 22:16:35 GMT  
		Size: 7.4 MB (7370248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52437ae0cbf42cceaef17e2d5d105ae8c53eccae04d04fd8e47fa2248b45bd49`  
		Last Modified: Fri, 08 May 2026 22:16:35 GMT  
		Size: 15.9 KB (15932 bytes)  
		MIME: application/vnd.in-toto+json
