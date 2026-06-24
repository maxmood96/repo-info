## `clojure:temurin-25-bookworm`

```console
$ docker pull clojure@sha256:a7c45dfa679f8433b19668e712901ceedb13942b4daad79ed6b9675c69421712
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
$ docker pull clojure@sha256:be62d7be813a67016802790eb47a5cf39a02a011071dcf7a0bc79af5105a17d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212511511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d325695b3d671521a1b949d92f0d5ed55efe795dd3b68654f8de64bd6b02ef5b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:30:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:30:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:30:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:30:16 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Tue, 16 Jun 2026 23:30:16 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:21:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:21:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:21:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:21:34 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:21:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b041a55a85cc0e47dd570746852cc1b0fee042f3a03eb250b9f896ac4aa74a3d`  
		Last Modified: Wed, 10 Jun 2026 23:41:01 GMT  
		Size: 47.2 MB (47161500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14907b0f682b8ecfba5edca7e3ae44505f908a9f5163eb33cb4b2d568ad948ea`  
		Last Modified: Tue, 16 Jun 2026 23:32:19 GMT  
		Size: 88.4 MB (88420320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01e583a20cd57b7b4cf4ea2074f0a86a9fc260f3b323ed6e9e9a5bfe895c5e2`  
		Last Modified: Fri, 19 Jun 2026 02:22:01 GMT  
		Size: 76.9 MB (76928649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9558baa62bf8e7e7657483a91ca54612f960011d65149679431f2a8f7a53422a`  
		Last Modified: Fri, 19 Jun 2026 02:22:00 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce12932e3926731c5e5c3f79950438a3d5b3d25c94d54c1a31ed1201d3106ac`  
		Last Modified: Fri, 19 Jun 2026 02:22:00 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:306c4f3ce0ecb90762cd85ad0fc44647feb6c11743a71f413e55f507c7aec4c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7339332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a044fce2d250ed73a46d44b18b7ee15cf76db0f6c34d3020c1669689bbc2032f`

```dockerfile
```

-	Layers:
	-	`sha256:63a7c760c0abbcab0cc76b95189b49157e7981457bdf0e11102f634bd125e845`  
		Last Modified: Fri, 19 Jun 2026 02:22:00 GMT  
		Size: 7.3 MB (7321409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33bf5388d03b1e473c6118806ec0acedbbdca3521c922b7e328ae1b3e36f9048`  
		Last Modified: Fri, 19 Jun 2026 02:22:00 GMT  
		Size: 17.9 KB (17923 bytes)  
		MIME: application/vnd.in-toto+json
