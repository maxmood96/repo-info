## `clojure:temurin-26-tools-deps-1.12.5.1645-trixie-slim`

```console
$ docker pull clojure@sha256:33372d62dfb5656da4e0728f5fe695371cf7a9fe8b93e818af62eef89abffa44
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

### `clojure:temurin-26-tools-deps-1.12.5.1645-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:fb3ea806cc07d3150615dc6ba250faf0daf90e78cf31dcaaf2e69e3b472b623f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.4 MB (196351679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac5675a1e8310759e311cd9a7a4cbbca81e5e28be9ed310b27dbf2e2d9895eb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 20:36:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:36:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:36:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:36:57 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:36:57 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:37:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:37:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:37:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:37:58 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:37:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5f40d497db616e9e8bab62f0d3c53265bfddc76ce642df21622b30556e2a40`  
		Last Modified: Fri, 15 May 2026 20:37:34 GMT  
		Size: 94.5 MB (94524372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1402cf2891d1edf8aa8d9d9ec9e25b3c7ddfd8e3f79773484835e7ea2b005294`  
		Last Modified: Fri, 15 May 2026 20:38:15 GMT  
		Size: 72.0 MB (72046038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f550ba937a5d828a2305f61fef4bd891f9bbd8fdc41796d1f9ee9dcbce5c45f`  
		Last Modified: Fri, 15 May 2026 20:38:13 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745ebf34c678247bdbd0132d331e176aee556028de0c4b834bd27e7240287588`  
		Last Modified: Fri, 15 May 2026 20:38:13 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1645-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a3bdd4782a12925f5a64ea8e053a2248568872885b228f2dd4e2eb116da89df3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5240703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bbbb2ab5264807882c84c2fa42c3dde02564ecb2d9e09e6507806288b052acf`

```dockerfile
```

-	Layers:
	-	`sha256:0a371b7f4af67c1bbf5b505545761992e56ff6c87cb43bc5e277832a9aa3ef34`  
		Last Modified: Fri, 15 May 2026 20:38:13 GMT  
		Size: 5.2 MB (5224744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39f126241b7e6506a03ea11d696c57cc0797a16f01c20679a870330fe98b8edc`  
		Last Modified: Fri, 15 May 2026 20:38:13 GMT  
		Size: 16.0 KB (15959 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.5.1645-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:db982e89ef89219494f07d4eb63957d25de9ab0fd3c101bf246fd9052bee13b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.5 MB (195503676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51773a6210fb8a0fe92ab4280c4a635cf796570c317a8dbf66fef108c0b68c0e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 20:36:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:36:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:36:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:36:40 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:36:40 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:37:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:37:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:37:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:37:40 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:37:40 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0d6f29a06c87d2da8b37558e582208fee2d182d8c68e104eb4edaab6d58eba`  
		Last Modified: Fri, 15 May 2026 20:37:17 GMT  
		Size: 93.5 MB (93504423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:962c21fb6c20ed83c6945d986cc04f490eccd50d375a67707fbb3466801ab5ef`  
		Last Modified: Fri, 15 May 2026 20:37:57 GMT  
		Size: 71.9 MB (71854570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86537225f2d70e56ce4562fa782a9c03580e78ea57c2cf747d15653b8b65b6e`  
		Last Modified: Fri, 15 May 2026 20:37:55 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2911a90207f19e7583ea62103d06409756583363f7f64fde51c750f69cfb0cb7`  
		Last Modified: Fri, 15 May 2026 20:37:55 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1645-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ca71ec7ccd2e881962548adbdeaf7ede4268a78f3dfb4746bb5709459fe0c73c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5246587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b17e17118005eacd9e8cb5692a84979ec5c346d71c676f757d2580aeea1e3af7`

```dockerfile
```

-	Layers:
	-	`sha256:5867d842fea613b4284fdad4703224dbfdbfe7bb8e0255147693874c0793d476`  
		Last Modified: Fri, 15 May 2026 20:37:55 GMT  
		Size: 5.2 MB (5230510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55326f772e8ae607c4a37c25df5f44c9f5d702da7eea7825e6647343f0419ee8`  
		Last Modified: Fri, 15 May 2026 20:37:55 GMT  
		Size: 16.1 KB (16077 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.5.1645-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:d64f32f91859d0d377983d1037e7b59cb67394085012c8e7dd42d03b5ce9a05b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.0 MB (204956993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0bc12773f93fc3cc102697810a2a6a6aa4567560b234031c2f7be2271c8b1a3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 21:48:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 21:48:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 21:48:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 21:48:47 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 21:48:47 GMT
WORKDIR /tmp
# Fri, 15 May 2026 21:53:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 21:53:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 21:53:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 21:53:12 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 21:53:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f8ab13e6d21adc6f6b5e2937ae339405e46ec097e90a97ff0de0b57189e749`  
		Last Modified: Fri, 15 May 2026 21:50:11 GMT  
		Size: 93.9 MB (93902067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:146822f3bba22a6b92bbe9138494649ab9e6bed58b76fd2c3b7fecad9b09cc12`  
		Last Modified: Fri, 15 May 2026 21:53:45 GMT  
		Size: 77.5 MB (77455794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a536e44fd5c626b6e78ce7b069a77b1a57aaa4009d279bf198beba92d740f8`  
		Last Modified: Fri, 15 May 2026 21:53:43 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74680a1c909086cd168f267f751f2d55f3b249b159994a6267413ed3e7287d1f`  
		Last Modified: Fri, 15 May 2026 21:53:43 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1645-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:25603b649bf326e075bf947b7e132844640855ca49ddc8007eabb30af05e6347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3e4efc5c4d477e8c066c668247ca8a0a437df004cc2e73ffef81b9f1009b960`

```dockerfile
```

-	Layers:
	-	`sha256:777bbf8f60b687cdaa35509b17705dcb13136362d9b6a45ef4ac65edbf02add1`  
		Last Modified: Fri, 15 May 2026 21:53:43 GMT  
		Size: 5.2 MB (5213051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1222c4338dbfe6fcc8c37affa737f4212636bb6738aec0d0a7a4ad4bb58f3f33`  
		Last Modified: Fri, 15 May 2026 21:53:43 GMT  
		Size: 16.0 KB (16007 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.5.1645-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:3b3579a65a18e2df95f9072806cc61087de0fbe445d80bf30430addc48dbb730
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.4 MB (193391314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5964ad3352cdfdd77e5a358dca0dce84ab47631be7c1a38a58e4ff49e51a13f3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 21:32:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 21:32:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 21:32:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 21:32:07 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 21:32:07 GMT
WORKDIR /tmp
# Fri, 15 May 2026 21:32:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 21:32:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 21:32:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 21:32:43 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 21:32:43 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2fbbc68c452b3ba3a496488f38159dac53afe693311bee1c04f555d854ff4a2e`  
		Last Modified: Fri, 08 May 2026 18:29:20 GMT  
		Size: 29.8 MB (29840347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f8d192a477fc92bbf7684aff2d4971ef4a77f646678c728d5f898070821435`  
		Last Modified: Fri, 15 May 2026 21:33:19 GMT  
		Size: 90.5 MB (90536989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a4b7a17a07f22ffcadb6a452b4f4d71128d6ef5306c6811014fb3f46e9e05e`  
		Last Modified: Fri, 15 May 2026 21:33:18 GMT  
		Size: 73.0 MB (73012935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ded76b2f04b105b79bbfbb71fd93a45f84ed18959981bdb99a48c12cf89ce6`  
		Last Modified: Fri, 15 May 2026 21:33:15 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a44544780cd5cbd6c93ee1661ab7a8e1ed22a2a120200532814305a9abf0dc`  
		Last Modified: Fri, 15 May 2026 21:33:16 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1645-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:53071dc3650bedd1268bf9b68ec1caab6f180f4ec1d8e77486c16f1dc74ff481
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5221813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1526eb643e93bea6aaa0e9b39433e637a492bf18b0a6636591be27eee415c775`

```dockerfile
```

-	Layers:
	-	`sha256:29f0106215dfb30fbe6daa01a916cf5f873967d0d4cd78a327d409e257d02507`  
		Last Modified: Fri, 15 May 2026 21:33:16 GMT  
		Size: 5.2 MB (5205854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23f272aa57c9c4b6107d561cfccdfdda6316ff4324a9c698d19faa998d6ae7e8`  
		Last Modified: Fri, 15 May 2026 21:33:16 GMT  
		Size: 16.0 KB (15959 bytes)  
		MIME: application/vnd.in-toto+json
