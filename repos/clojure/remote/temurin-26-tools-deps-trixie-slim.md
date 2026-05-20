## `clojure:temurin-26-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:1f289e834571415a6f82b10ccef73da62f59bce269a391279c4f8559d3f1f732
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

### `clojure:temurin-26-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:305dcec4dcff098939783dc791471d23098b6bd0ce55e1f7970b0bb6392f8290
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.4 MB (196353224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:770dec1e87e0818d42ed7449841d934f4449f7223174427d0828feb34cfe48b3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:02:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:02:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:02:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:02:51 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:02:51 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:03:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:03:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:03:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:03:06 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:03:06 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24a8e21c69b3af1d7a485eb2aec3bc805f3d247fde1173dc91f705055ab5f0e`  
		Last Modified: Wed, 20 May 2026 00:03:27 GMT  
		Size: 94.5 MB (94524344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b77aab4a3322a27c5d77944ef483d1242b684fa49ccb2cfb200c78c653bc4b1`  
		Last Modified: Wed, 20 May 2026 00:03:27 GMT  
		Size: 72.0 MB (72047913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5934524b8e1b4872d9dde8bceed59d451b2fa813486424454d87033ea95254e1`  
		Last Modified: Wed, 20 May 2026 00:03:24 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c96a0ea1cfe40289df0728ade302899e8d603718017235b8e39d2de6a5a05e`  
		Last Modified: Wed, 20 May 2026 00:03:24 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ee0424bc8b42a7095ab0b0ec886de7f7fc89fc6ad49aa83ed14c751695f57c61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5240816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8483e3206e26455ed5b25083894160fb6b5430829c516d23dfe7df903cadd4b1`

```dockerfile
```

-	Layers:
	-	`sha256:e5b63884c309575a4b97c1c67401d070435987004f5a0bca0519d3bd7101f4f5`  
		Last Modified: Wed, 20 May 2026 00:03:24 GMT  
		Size: 5.2 MB (5224858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9d55af2ea85d2583b864f40b1ecc5db2704e9a844251480eace69c95808d5ee`  
		Last Modified: Wed, 20 May 2026 00:03:24 GMT  
		Size: 16.0 KB (15958 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:12fea82b7e271f51802b2d32eabb043ee52f9c48456bb224dd9a20403b9bd0e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.5 MB (195519380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4528fdbb71674de4e0e081b3fc059d4cdc0e43cb3c9bc27cdea8d522d3a7138`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:09:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:09:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:09:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:09:39 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:09:39 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:09:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:09:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:09:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:09:57 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:09:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a80cbfdbf332678d68e9f50c7dc2913246ac2df517a03f27cfcdc053abb146bf`  
		Last Modified: Wed, 20 May 2026 00:10:19 GMT  
		Size: 93.5 MB (93504334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1911aad669681aabd7a50917008724b65828fc668c4c1585f2c06567e84d1119`  
		Last Modified: Wed, 20 May 2026 00:10:19 GMT  
		Size: 71.9 MB (71872083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03861512190f50c321c3e41e25bf180e6cbd96895857ba0c2c4cb7a954ceb76`  
		Last Modified: Wed, 20 May 2026 00:10:16 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8d7689f23072c4b79412b5b786a0f91dd01a453534773ad00c2ae7fade1e2a`  
		Last Modified: Wed, 20 May 2026 00:10:16 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a3faca0a24eadd70675958065237530fc16afe2dc16a5d082edf355a43225984
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5246693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a8b9181ffa38d3f1fc12da2ec3d1c14de661e44baddea32e7155b7bd29daed5`

```dockerfile
```

-	Layers:
	-	`sha256:d4f1801aed88075a64f12baa2f9b5ddcafffcd8f07964defbd333f946372aff2`  
		Last Modified: Wed, 20 May 2026 00:10:16 GMT  
		Size: 5.2 MB (5230616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:564a5d17a0b56617557768037d0d184d3ba7d0f25f1bca3f8b9c1513af7dff67`  
		Last Modified: Wed, 20 May 2026 00:10:16 GMT  
		Size: 16.1 KB (16077 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-trixie-slim` - linux; ppc64le

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

### `clojure:temurin-26-tools-deps-trixie-slim` - unknown; unknown

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

### `clojure:temurin-26-tools-deps-trixie-slim` - linux; s390x

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

### `clojure:temurin-26-tools-deps-trixie-slim` - unknown; unknown

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
