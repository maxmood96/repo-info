## `clojure:temurin-26-bookworm`

```console
$ docker pull clojure@sha256:ad70375bd5c4dc9a8283beb98ca072ba8e1602da24d72e83faa234b7fe2ce66f
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

### `clojure:temurin-26-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:1bf6b12a2f0b7da6d5404cf830ae9d69cd4cb3defebcfdc5f262875551f14b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.2 MB (221152750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b04bca72daf8f0948e1859694ce762714d0763d1dd9e38e3e4da2c308a614fbd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:22:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:22:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:22:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:22:44 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:22:44 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:22:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:22:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:22:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:22:58 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:22:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:425befdf76e52426879d2abe42093a00dca59a893e7b4fa2a7679b0180b71d4b`  
		Last Modified: Wed, 24 Jun 2026 00:27:40 GMT  
		Size: 48.5 MB (48502210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beef06c0aa2f92c406529c97a3d6f77491765104401382ecd4c95b4f543902da`  
		Last Modified: Wed, 24 Jun 2026 02:23:20 GMT  
		Size: 94.5 MB (94524361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dcd2a69bc96eadb8950b5a1199522ec3c4d95c5ef0638d9c7fa9db509ba697f`  
		Last Modified: Wed, 24 Jun 2026 02:23:21 GMT  
		Size: 78.1 MB (78125135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a4c6a0a7d3765fb0ab1965346b63b38250b3743eddd1e83b65dd748a14d547`  
		Last Modified: Wed, 24 Jun 2026 02:23:17 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f45714faf26fa0db340700d014f5debf3c861318118048de6eb9999d5ec65eb5`  
		Last Modified: Wed, 24 Jun 2026 02:23:17 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f80d132d41e7c69bbb7a8849b4fb917024e1f21421998459b5ae4c82dfb82e94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7358318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95c9d8d89b642726d1f792ff7db7f22dbbc4977474445b336e0ec57c00ef0cce`

```dockerfile
```

-	Layers:
	-	`sha256:55146b73ff305655188c8c896b340891dacba198b4182aa2169e8d0cf1c26645`  
		Last Modified: Wed, 24 Jun 2026 02:23:17 GMT  
		Size: 7.3 MB (7341709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d0b5e61989e9436b1739f2865c61bed480d23e3f6920cd78db74db6d24b1074`  
		Last Modified: Wed, 24 Jun 2026 02:23:17 GMT  
		Size: 16.6 KB (16609 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cf367e5b27a7e02cc759371ac077f29157a1ba7bbe5404611a566c1d4968d50e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 MB (220023954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:248d1f01f16e09e7141b70da99ebf6c26bb10a79a0cfccec3ec2c778209f460b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:29:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:29:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:29:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:29:29 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:29:29 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:29:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:29:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:29:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:29:43 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:29:43 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0fb1189398e2e4b474d43aac6502510d0da0318e70137a377c21087f198814db`  
		Last Modified: Wed, 24 Jun 2026 00:27:19 GMT  
		Size: 48.4 MB (48389201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0734b3e19ec675ed9b31c44604136275a29c3275dac35289d9baa0e79f33b535`  
		Last Modified: Wed, 24 Jun 2026 02:30:06 GMT  
		Size: 93.5 MB (93504323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:317d9b9d5adb12b3ccb7d7d24fb621680ee73e03bce75bc9938e2e1a29a3dc00`  
		Last Modified: Wed, 24 Jun 2026 02:30:05 GMT  
		Size: 78.1 MB (78129391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cdfe61a32e54f9571b85299b4f56962dc88c6d948c87b2aca77924274c04c00`  
		Last Modified: Wed, 24 Jun 2026 02:30:02 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:761c628af8745ca215234a21198952cc36a1813ccf1ac989af2670e77594ecd6`  
		Last Modified: Wed, 24 Jun 2026 02:30:02 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f24ef162e63f9185e5c1ffa92ce0f4e615ba2ec909dd93b1d8da47fe4c468aaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7364244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ae9b8dbbdd1b6e2aa50847a1ba2911b98b2af58850cb014faecca5d524ba96`

```dockerfile
```

-	Layers:
	-	`sha256:2b59bbe270af663d65c1ea5836a3f8d56865e9a02e84553fa3df6da8a4fafd89`  
		Last Modified: Wed, 24 Jun 2026 02:30:03 GMT  
		Size: 7.3 MB (7347493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1a7374345cfe5bf6599f4f356dd9688720d9c4d97acbd3cb96ad1521c431c81`  
		Last Modified: Wed, 24 Jun 2026 02:30:02 GMT  
		Size: 16.8 KB (16751 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:0b866681b47af682b5e7de71262f2c385de87f8a1f45b9d35a149a09ad834415
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230208369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07c31aa61095852b93c5af374d88b668b81dffeb56e7e8b53ed243ce11dd4de5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Wed, 17 Jun 2026 00:07:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jun 2026 00:07:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 17 Jun 2026 00:07:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jun 2026 00:07:21 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 17 Jun 2026 00:07:21 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 03:00:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 03:00:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 03:00:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 03:00:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 03:00:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:88b94a58fac236a778527a3293ccd0ff4d309bff0bf314017ea5af603908fa2e`  
		Last Modified: Thu, 11 Jun 2026 00:21:34 GMT  
		Size: 52.3 MB (52346670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4759a87d2ab24b2fac4a2500d8d0888984823a78af74fea7debdc9f59a4aa41`  
		Last Modified: Wed, 17 Jun 2026 00:10:39 GMT  
		Size: 93.9 MB (93902050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940df2f34b1e0014aa6aa124f88b9936f280fddd171bdc3d254cb812f7f501f1`  
		Last Modified: Fri, 19 Jun 2026 03:01:02 GMT  
		Size: 84.0 MB (83958608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bcdbeac267d49bb6f5f446de16e6eafec8e50e80d29ea2e3c9a8e1c625ec5f9`  
		Last Modified: Fri, 19 Jun 2026 03:00:59 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37e871d9748d28fdf14174eed6ce36119943c7369b5208b7aa5073f1eaba6cd`  
		Last Modified: Fri, 19 Jun 2026 03:00:59 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c9810c5af5edbef65325c19a3e90c60724cb98424f680abe8ef91f04e04f9758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7347542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccb9171c1927bc8c0eb7bdf4aa95f51c9bc1e1e081cab23e206583b45bb9edb7`

```dockerfile
```

-	Layers:
	-	`sha256:5c1bb7f633d71bd16f70b13bcf10c8f9a0c97e3448f2bd9b70d7e26d8b6c18db`  
		Last Modified: Fri, 19 Jun 2026 03:01:00 GMT  
		Size: 7.3 MB (7330873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a639f8c41df30af64b2a7fa38e725192495e5dd21c9afe571593dcefd7da1e57`  
		Last Modified: Fri, 19 Jun 2026 03:00:59 GMT  
		Size: 16.7 KB (16669 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:74293377218599846d86b8a3ef976626cadabed31d17caa8cecda898963634c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.6 MB (214629002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8557536613feb92eb0267dddc29c0e674b77cdadcb4434607c4fc7fb64afd9ef`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:22:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:22:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:22:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:22:54 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:22:54 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:24:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:24:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:24:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:24:06 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:24:06 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b041a55a85cc0e47dd570746852cc1b0fee042f3a03eb250b9f896ac4aa74a3d`  
		Last Modified: Wed, 10 Jun 2026 23:41:01 GMT  
		Size: 47.2 MB (47161500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93dffac2f0aa26f15bbfc00b26f8e00f41d28e225af70af77c70295cf7b0a6c`  
		Last Modified: Fri, 19 Jun 2026 02:24:28 GMT  
		Size: 90.5 MB (90536936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e6022c19afbe49d4acdf5ac59cf718fdd24167b8c419a1d079bf4ac1789afac`  
		Last Modified: Fri, 19 Jun 2026 02:24:31 GMT  
		Size: 76.9 MB (76929525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e5d2985448e7f674132609f54a07c7d2d5de813f0b21aa481e0f4c9671bb3a`  
		Last Modified: Fri, 19 Jun 2026 02:24:30 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf8727fe20f04ed92e50130f7e94f80256f1b15874dc47fc9f563c1a5f5554d`  
		Last Modified: Fri, 19 Jun 2026 02:24:29 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f6ffac119ca7708b6e91d89bc57e74ccde0170635bf01f326f40517746b293c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7334823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c4d7e9900dff90d8777a44cd8067ba8aa9bf8b36eae65658205a8b0e2e93e5b`

```dockerfile
```

-	Layers:
	-	`sha256:f1cdf5caf3560bfd63257db39655fb95b92001484ebdf2341773cf6640225a4d`  
		Last Modified: Fri, 19 Jun 2026 02:24:29 GMT  
		Size: 7.3 MB (7318214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9d879f5035a5b3ad22c7a74c9458374e3a8827b5a43e7e86106ff301aa63c1e`  
		Last Modified: Fri, 19 Jun 2026 02:24:29 GMT  
		Size: 16.6 KB (16609 bytes)  
		MIME: application/vnd.in-toto+json
