## `clojure:temurin-25-bookworm`

```console
$ docker pull clojure@sha256:2ce399be45559b20f252c70779d365cf9e88780a9241b11d62d37d5717c0b083
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

### `clojure:temurin-25-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:9203cec60c817259e5d1580b83403d419857932bbdf129ccce98e297f713cc32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.2 MB (219202971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6b32aef96b922ad859b2ba2a59dba27b8c0cf096c347ea79424e821cc592f52`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:21:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:21:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:21:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:21:08 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:21:08 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:21:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:21:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:21:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:21:24 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:21:24 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:425befdf76e52426879d2abe42093a00dca59a893e7b4fa2a7679b0180b71d4b`  
		Last Modified: Wed, 24 Jun 2026 00:27:40 GMT  
		Size: 48.5 MB (48502210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699ed0bce7c27841391ce95eb8df65b61a551683603132573ed9c4a57ba194ca`  
		Last Modified: Wed, 24 Jun 2026 02:21:53 GMT  
		Size: 92.6 MB (92574587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c879889b90043f773cbb86dd48860d1a2576c144ae61259a9431030afdb19581`  
		Last Modified: Wed, 24 Jun 2026 02:21:52 GMT  
		Size: 78.1 MB (78125135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ff4c6544939c5e8dd08b572e2d1426f41bbc335ec1907aff6b6caff1103327`  
		Last Modified: Wed, 24 Jun 2026 02:21:49 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9340c03358ecbc78b571c50f87741abffeaec4ecec0cc560243e3dba18dc4b`  
		Last Modified: Wed, 24 Jun 2026 02:21:49 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:a2221ca9f7155d677f798464718552f33004de05d240ed24c941d127fdfffc74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7363451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6643c9f8a73e48b65be45767c1a9739cc237cae75aef0ff04fab5501cf069763`

```dockerfile
```

-	Layers:
	-	`sha256:81c106a8bc87c7d62bd90e6a6b5fa1ede025385730d0ea542c545066ebfb8606`  
		Last Modified: Wed, 24 Jun 2026 02:21:49 GMT  
		Size: 7.3 MB (7345528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70a38ea42c9cc3f590017cfcd5504ab1f426ddd2c6fd3abf3c28b6a721577e74`  
		Last Modified: Wed, 24 Jun 2026 02:21:49 GMT  
		Size: 17.9 KB (17923 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fe110c4e14b846ada75f752e2e834fa130844c40b8bdcf5b2cf6d3d8e2f77de5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.1 MB (218061644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d73e9b5d48bd57a3274680272959849ded8434d0c7a4dd61dab90cfa8677151`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:27:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:27:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:27:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:27:41 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:27:41 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:27:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:27:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:27:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:27:56 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:27:56 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0fb1189398e2e4b474d43aac6502510d0da0318e70137a377c21087f198814db`  
		Last Modified: Wed, 24 Jun 2026 00:27:19 GMT  
		Size: 48.4 MB (48389201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d595f75559d100229367e003c1aeb38e8555be0c963929714da599c740db5e4`  
		Last Modified: Wed, 24 Jun 2026 02:28:18 GMT  
		Size: 91.5 MB (91542269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed54856ef14532958af4bc51a2a52ee65be60bcc93af3f37065e6a5747c423d`  
		Last Modified: Wed, 24 Jun 2026 02:28:18 GMT  
		Size: 78.1 MB (78129135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89170a8aa46db221bcbe79c0d8f105b372f3786878dada145cb2ba8e08570ee`  
		Last Modified: Wed, 24 Jun 2026 02:28:15 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d3511d16e494dc1c045e13e7371136eabfad0dc8966df6fc87e814b26bb35d`  
		Last Modified: Wed, 24 Jun 2026 02:28:15 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:82fbf770d73d7926d5348c9d0311e19aa69173ecd2751e20bcb83a8e11eea425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7369475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cae3df5fab2305a8ddf7968f1d3b2c6f5e7c8c69189b2127619074e95e9d7584`

```dockerfile
```

-	Layers:
	-	`sha256:9d2617f95187ccc929c0e2477a917663e93a79fa419b09c1299e575dcf56a726`  
		Last Modified: Wed, 24 Jun 2026 02:28:15 GMT  
		Size: 7.4 MB (7351360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bde06cc545bac4e72b12249843d5ace61941ec43ce967234265619ef33461e2e`  
		Last Modified: Wed, 24 Jun 2026 02:28:14 GMT  
		Size: 18.1 KB (18115 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:445e9d668b668a5a044ad114c54e14c26f72714830ae309c4c233a98626e4a17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228220487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f84a45240f3e41cea6c7d5de862a6a0424575eff0aa1c1c5dafca0ebda12b2e0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:30:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:30:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:30:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:30:21 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Tue, 16 Jun 2026 23:30:22 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:55:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:55:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:55:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:55:39 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:55:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:88b94a58fac236a778527a3293ccd0ff4d309bff0bf314017ea5af603908fa2e`  
		Last Modified: Thu, 11 Jun 2026 00:21:34 GMT  
		Size: 52.3 MB (52346670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af2d7bc5e0f6f23b949f449ec38352dcc13ff43d0d262dab584e4f344eec386`  
		Last Modified: Tue, 16 Jun 2026 23:35:12 GMT  
		Size: 91.9 MB (91914009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb0b334fe03d11aca4fe609936d13f88ad2656643ddc16bfea81562bbe9eccd`  
		Last Modified: Fri, 19 Jun 2026 02:56:27 GMT  
		Size: 84.0 MB (83958767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b604c425d54a2507da522d802bb672a141b0243ba67844148088b1e88396ced4`  
		Last Modified: Fri, 19 Jun 2026 02:56:24 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2619c4cd68b73a15b57d109af67ebdd89c474f745aa9ad62370fa4acfdfa4c82`  
		Last Modified: Fri, 19 Jun 2026 02:56:24 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:4e3ed668f22264c9fe24f9444ba721caa62e0d6275d03e3b0ca330daa2627329
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7352101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f18cb2381e366b4a0c99f4b903a93a2c38e005ceece2ddbfef0d0079c34aa31`

```dockerfile
```

-	Layers:
	-	`sha256:befc66a59ef3c154fd7543e9fd95867509eff66ace09bbcc382f46dcb047d16d`  
		Last Modified: Fri, 19 Jun 2026 02:56:25 GMT  
		Size: 7.3 MB (7334092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:541b72f39ad956f8e4e5f09cda084d88956c4b1386c5e3ce1cc7fb219d6d008c`  
		Last Modified: Fri, 19 Jun 2026 02:56:24 GMT  
		Size: 18.0 KB (18009 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:ba10a7dd19be13f9a58850e94d92e3987684048ce22b16f295d92f6692211be2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212512123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:123a3fc6321a21f7a1c577d4633e5a19ca2cb7b26f931880b1f3afa771df6fb3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 04:07:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:07:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:07:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:07:44 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 04:07:44 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 04:17:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 04:17:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 04:17:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 04:17:56 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 04:17:56 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:bdd2e9d83d68023204331dd445067114dbd3500d2d496368624fa7ef81743d4a`  
		Last Modified: Wed, 24 Jun 2026 00:27:09 GMT  
		Size: 47.2 MB (47161675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42b02c985ff427f09da77745bd5599ec265500d0ffe9217e4629e6e410d74c2`  
		Last Modified: Wed, 24 Jun 2026 04:09:44 GMT  
		Size: 88.4 MB (88420330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77402aeba1546c1cd6df5cdc64fe3f24e4fce5df78d4e93ff9ebdae55d735d1a`  
		Last Modified: Wed, 24 Jun 2026 04:18:23 GMT  
		Size: 76.9 MB (76929076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422eff86697b90b4c82c1a780276ea606ef647cd3e0b427726cad8cb5e653028`  
		Last Modified: Wed, 24 Jun 2026 04:18:22 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058099d5bae1746b020ab5771cf8f891192e2ac8d02922fe3baa838dec407b83`  
		Last Modified: Wed, 24 Jun 2026 04:18:22 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:8dd5a9196a331123f4dfda419798caed64622ae5caaf706ec129adf8accecaa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7339334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4770ad73e1d5d332fc3c1edac02adf24ab9c4e8d5faa28f545a667259481ffd8`

```dockerfile
```

-	Layers:
	-	`sha256:75408284af7a4bc3c59555d829e8b94c0d29662349d8898a0b2737116f5a95e4`  
		Last Modified: Wed, 24 Jun 2026 04:18:22 GMT  
		Size: 7.3 MB (7321409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b60f7bc339ed7e1f413f8ffc948cbe809591f08df1427e49b88f26c14899db47`  
		Last Modified: Wed, 24 Jun 2026 04:18:22 GMT  
		Size: 17.9 KB (17925 bytes)  
		MIME: application/vnd.in-toto+json
