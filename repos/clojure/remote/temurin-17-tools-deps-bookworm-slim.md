## `clojure:temurin-17-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:fbb4203d207c226b4832c10df54f8fe22599c8f275210914268014cff147e4f4
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

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:681ce7a9ad7332ec75c42cf21f11eef6e235954a2fae6fcd1aaa029472184a86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.9 MB (243872607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d153b56b3e0fa7ad47f7dca143d2dd7d877ca870bd4d2e0b5bf9df6aa17fb5e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 15 May 2026 20:14:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:14:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:14:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:14:36 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:14:36 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:14:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:14:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:14:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:14:50 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:14:50 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12e095ed4c7dedf80909f081234af07ac3b6ff416477400c355c32e7908d646`  
		Last Modified: Fri, 15 May 2026 20:15:12 GMT  
		Size: 145.9 MB (145905444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dce82d0c4d01ba2585b1a1d1dd7b15e469966b20586fcad476578e7a1ba5a30`  
		Last Modified: Fri, 15 May 2026 20:15:11 GMT  
		Size: 69.7 MB (69729836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ceaa85a24ccdb51b4eb5962da6c4221d5836687f0e4f7af7bc5658fb236a83`  
		Last Modified: Fri, 15 May 2026 20:15:08 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63713d86e0f9ab67e7327e7dfd46df0a3e71a612566c986885bb87398111c0ab`  
		Last Modified: Fri, 15 May 2026 20:15:08 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:42d8de63f4082deda333ed4f0a4fdbed481958f1351438484459ba526abd4477
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e797d634cd709cc30b3860e2a0553581ce9139bad1c2e019c899aa2757c33781`

```dockerfile
```

-	Layers:
	-	`sha256:ea9fa4f9fd2f07feb3642e9d85df0e76fd65229ba4ae3ea2310a93912b7fce56`  
		Last Modified: Fri, 15 May 2026 20:15:08 GMT  
		Size: 5.1 MB (5116792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82779412c06dfb7fbb7b667c8708a825ecedcc8e5d47b4f61e488a0f5e93961f`  
		Last Modified: Fri, 15 May 2026 20:15:07 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c5f52f2ed15fe37ee8efeb9605f42e36f46e1d7bc42d1497db983a2f6c70dd0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.6 MB (242564351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb40eeebdef50cbcaa3cc54de3a75a5c89cfc3141a09df7c04d9ed7f4b16fe7f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 15 May 2026 20:14:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:14:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:14:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:14:30 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:14:30 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:14:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:14:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:14:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:14:45 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:14:45 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f51aaae38d2d955693fe13c897d5feffe73b5639f8dd06157e1d10d0a9943fc6`  
		Last Modified: Fri, 15 May 2026 20:15:07 GMT  
		Size: 144.7 MB (144724358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aac3c7d9f238c1b50a80db936bf6a9fc5b185303fc9be5e5f94d948ed7def42`  
		Last Modified: Fri, 15 May 2026 20:15:06 GMT  
		Size: 69.7 MB (69722784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e4838c0641dd59e4dc3b62df6289938617c1b0b68e3093e2925e461371353c`  
		Last Modified: Fri, 15 May 2026 20:15:02 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b9bd6414f36b93f74cf19fb6bd20e386832c5e97b7314d9fc26556538a9abf`  
		Last Modified: Fri, 15 May 2026 20:15:03 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0c2edca796cdd1e6305704167ceb7cc36ccb8483fbdee58fa875296ac1b75805
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5138661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b60872851f9b34ad657f3ce4792ff5563ee3128380446010ff2b58e20e30fc0`

```dockerfile
```

-	Layers:
	-	`sha256:38b1add502b63de6172d1cd658196ba61b1979c0330fd4c33f55d69e93ac105c`  
		Last Modified: Fri, 15 May 2026 20:15:03 GMT  
		Size: 5.1 MB (5122553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d11a9dbf6906305329d3cded42308ed24167c7084fd3fbee3fc198c5af88c1f`  
		Last Modified: Fri, 15 May 2026 20:15:02 GMT  
		Size: 16.1 KB (16108 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:2f07383a73d7701371ae269257acfc675c125f5353a75ec34fac9c0421036e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253411484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13f4a35c669b41eb901cc987a16a164cb1d979ada7f5ecf85ad3cb786655a6be`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Sat, 09 May 2026 02:30:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:30:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:30:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:30:41 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Sat, 09 May 2026 02:30:42 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:23:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:23:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:23:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:23:38 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:23:38 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0e29ea7436ed4beb1c38bcfee44589407e49fc690669b42b35db33a9588e820a`  
		Last Modified: Fri, 08 May 2026 19:44:06 GMT  
		Size: 32.1 MB (32078453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ebb50b599e2de909acaf0c0d8a3d5a70b8d0e3b34206b32960ca5e3061a8a17`  
		Last Modified: Sat, 09 May 2026 02:31:50 GMT  
		Size: 145.8 MB (145766111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b2baab1e1ae3868d3dc4dfed46e618d295241812d44a810a34f837c5ca1d75`  
		Last Modified: Fri, 15 May 2026 20:24:14 GMT  
		Size: 75.6 MB (75565876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8c1a1ca0eac893e7133e15826ffbe93c8037318b0ea226646692b65f8a8bca`  
		Last Modified: Fri, 15 May 2026 20:24:11 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:194e750d7f055f1dce84dc59d0a566b87b4656cd644780bf6613cbbfe6d9c81e`  
		Last Modified: Fri, 15 May 2026 20:24:12 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f90bac21d11ccdbf2f81daf5d9d1959e828247bedcd2ec27aa246845d7b5f327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5daf4e38a4a5cc0a904f52de4c08287f41aee23c0c22336ee56d45c5468c622e`

```dockerfile
```

-	Layers:
	-	`sha256:76f5e6f304f87b309bfd3454f1544ffa8a79c020ec691d39df561bb766dcba8c`  
		Last Modified: Fri, 15 May 2026 20:24:12 GMT  
		Size: 5.1 MB (5121950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43459f150be5283f3aea2a4fab706e457165aa3fa055e918a1c9d87ab7471f30`  
		Last Modified: Fri, 15 May 2026 20:24:12 GMT  
		Size: 15.1 KB (15082 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:2cb070885da81cace54c564983caecdafaa56734606ccc914f9abe452a0b4eca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 MB (231347119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85140dc59c052b4bda8c9f69f5ad445e29febcff9c7d49cfaae6e792a1548d16`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 23:34:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:34:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:34:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:34:38 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Thu, 14 May 2026 23:34:38 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:20:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:20:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:20:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:20:19 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:20:19 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5694fd2fb22af8aa0f8c7978432e9a19d6412a485716d6faec12db03eb508801`  
		Last Modified: Thu, 14 May 2026 23:35:20 GMT  
		Size: 135.9 MB (135910447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f8f37b5fa4b940ea35c1d16c8705899c5144f6c02bfcc249686b8280ee5fa65`  
		Last Modified: Fri, 15 May 2026 20:21:39 GMT  
		Size: 68.5 MB (68544023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dc098ef18ac845e83f0616c29527b503d3656b30a73e07fc0f503babdddafb1`  
		Last Modified: Fri, 15 May 2026 20:21:34 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650447af1c9f2ad133ae920326fc3aabe12f222f7d65b4b8517a443399f828c8`  
		Last Modified: Fri, 15 May 2026 20:21:35 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7467cda93c8e5fa656f32e0154a3175d322fd01a3e4faa41e90924aad6eea7da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5123148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f78abe429b5cef416e7f0b35ab370c9d8c8bf22c02c3a66e9a3551683c8622a9`

```dockerfile
```

-	Layers:
	-	`sha256:7a9362f4a77de8c715b60b246148148ac8e7142610db0f583084732b27608318`  
		Last Modified: Fri, 15 May 2026 20:21:36 GMT  
		Size: 5.1 MB (5108113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:809487cbfcbf46227b43cf4f6ae8b09bbbc49bbd18e1f1c6a2f456a54ea10760`  
		Last Modified: Fri, 15 May 2026 20:21:34 GMT  
		Size: 15.0 KB (15035 bytes)  
		MIME: application/vnd.in-toto+json
