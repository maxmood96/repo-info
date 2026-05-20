## `clojure:temurin-11-tools-deps-1.12.5.1645-trixie`

```console
$ docker pull clojure@sha256:11d786edd2b457ef24469b48defb0159c68db817ec671994cb9966416e5889c2
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

### `clojure:temurin-11-tools-deps-1.12.5.1645-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:a1be2e6d7c4b599685807f9dfa5abed58ec52f190a0b4f8d96b4fe42e593e9be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 MB (280804920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f907bca55c58dff0906dcb2d8adf1f2426de8bd1f7dbfdcd2f37503c513d7b`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:58:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 May 2026 23:58:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 19 May 2026 23:58:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:58:13 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Tue, 19 May 2026 23:58:13 GMT
WORKDIR /tmp
# Tue, 19 May 2026 23:58:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 19 May 2026 23:58:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 19 May 2026 23:58:29 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f32f49ce655a9cf7c1fd4ca1417ddb39a54cedf4b7ff35de20f8009c18dd7a96`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 49.3 MB (49310623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da4efafb668a2750e069f47336bd6671b79f6e1cf314ab29af76a0f2e60f2d9`  
		Last Modified: Tue, 19 May 2026 23:58:56 GMT  
		Size: 145.9 MB (145886262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b796c6c2bfd6a375c2eadf9c90fc096f7d88109a7f139cac7d973e406f40a2`  
		Last Modified: Tue, 19 May 2026 23:58:55 GMT  
		Size: 85.6 MB (85607390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2567a44c370b28676d41e647224f98d87837f1cb8853240fa72b3bd7c5fba9a0`  
		Last Modified: Tue, 19 May 2026 23:58:52 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.5.1645-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6d7ae174c291bde21a620f5fdbac27b111608c9f9252252efbf2ea6da1043a96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7505351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56f16e0a9b50351f63695168f6a37e48b0beb99588158a7be08f8ce3bbea8af2`

```dockerfile
```

-	Layers:
	-	`sha256:ead58a1ce17333b43c5c004877af6edd60dc6da49080a75484ebdd2fce43035b`  
		Last Modified: Tue, 19 May 2026 23:58:52 GMT  
		Size: 7.5 MB (7491012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca9a081f71db06e8cc316d6cc1398681cbce78b674b794b3cd4b7848788f76bb`  
		Last Modified: Tue, 19 May 2026 23:58:52 GMT  
		Size: 14.3 KB (14339 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.5.1645-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dce17c95a5336e8dc289115ad9a9fa1ae106590c3718ed6ca62e68638f6ccfca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.7 MB (277686593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d79476d7c38d76dedd8f1115baf68ff5a791841873f475f5c8699f94f6be8ba`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:05:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:05:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:05:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:05:12 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:05:12 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:05:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:05:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:05:29 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:635135721e54f918d2d81497bc66b71f98aee3b440dd6498218827c56d7d277f`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 49.7 MB (49672220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:219861c11c57f50fe8e376337efed53a48b754c9df99db788c9a4f77c3791de7`  
		Last Modified: Wed, 20 May 2026 00:05:57 GMT  
		Size: 142.6 MB (142582230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8993921d0cddb622bcba966a78fab57f5a0eeb1348e4ca6c695ed42e458b5bb`  
		Last Modified: Wed, 20 May 2026 00:05:55 GMT  
		Size: 85.4 MB (85431498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e700f1ae052b27a1f39cd745030ec9f5ecb2991dba5c231977b5c5d7adf410`  
		Last Modified: Wed, 20 May 2026 00:05:52 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.5.1645-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9afe79619dc7eb1a1a2bb0defd9af4c71b55c3cd13843f9a9425e47a5a44aa11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7512480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba8be95ee52c1546b5c6642494f528495dd3f25b9c6ff58395e9f96e4d45a567`

```dockerfile
```

-	Layers:
	-	`sha256:cc257c2f2672469403b264e6a75af5e2c66d99945b2bd075318612ed14b50394`  
		Last Modified: Wed, 20 May 2026 00:05:52 GMT  
		Size: 7.5 MB (7498023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b4770603daea335d76535163286eef2bafa7a7b9e548e92f002e086c4b62d61`  
		Last Modified: Wed, 20 May 2026 00:05:52 GMT  
		Size: 14.5 KB (14457 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.5.1645-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:85a2b423dca5b256c1d089d7ccf893667c220b2d88eecf455043ad7ab7b2156f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.3 MB (277270290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da5b3862de0afa475b4b174491ef01f90e5978ed0b760731621dc5ab843f2763`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 05:49:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 05:49:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 05:49:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 05:49:47 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 05:49:47 GMT
WORKDIR /tmp
# Wed, 20 May 2026 05:53:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 05:53:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 05:53:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:55497c62a793e62a2e78a3fd85fcedf060da73e331ad107733199ea991106b96`  
		Last Modified: Tue, 19 May 2026 22:37:59 GMT  
		Size: 53.1 MB (53132182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a9fef26d6c90c0453bfba8b1ff5cca1a32387bdf0466d3503a6eea28f899b8`  
		Last Modified: Wed, 20 May 2026 05:51:10 GMT  
		Size: 133.1 MB (133110168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1f3716c159d4449234c2aa156bfc8706881b4057d81be9555d605a361703ce`  
		Last Modified: Wed, 20 May 2026 05:54:12 GMT  
		Size: 91.0 MB (91027294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36cdd82eeb9022f479e7468a352b3c1da452a19d7fd742adae0d31ee418122d0`  
		Last Modified: Wed, 20 May 2026 05:54:09 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.5.1645-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b7f2b098acd3e85803d37a4da528518bd4cad41dc3361c349a45201633e28b19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7508250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdc165ca9c803a885dffc44883beca4b30afaeea2e99485e93d62a4bc71a2205`

```dockerfile
```

-	Layers:
	-	`sha256:8af08360e070f7eddc9f22f000d897e435f652a2ee63e246b3fabb37f4b79802`  
		Last Modified: Wed, 20 May 2026 05:54:10 GMT  
		Size: 7.5 MB (7494818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6eb3900b78a807e6652e6b84857af47e87420b5c55ee1237b5e4fe020e31ece2`  
		Last Modified: Wed, 20 May 2026 05:54:09 GMT  
		Size: 13.4 KB (13432 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.5.1645-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:e50d4915ea690709c64c5edb0288c6cceb31fb2fefe0e9b73ef2cbacf891635a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.6 MB (262622804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:984481ab2ac3bc54a6199c6b1a3481326bd48145ea32a36b0bafbdd23fa6589b`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 01:41:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 01:41:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 01:41:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:41:36 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 01:41:36 GMT
WORKDIR /tmp
# Wed, 20 May 2026 01:42:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 01:42:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 01:42:58 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1540dbb0587ae9097c9d04c50809503aa74d42814940d640c6659645acc0bc6c`  
		Last Modified: Tue, 19 May 2026 22:37:00 GMT  
		Size: 49.4 MB (49379780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e6016d4ebf4c94d6542085c791df63dbd93201c2c8fc6d05dc6abacf51ce4a`  
		Last Modified: Wed, 20 May 2026 01:42:15 GMT  
		Size: 126.7 MB (126651716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e35875dc4550ca73a1d8990aecd8c7339e6a3a625336fb4c44655f2415d7d1`  
		Last Modified: Wed, 20 May 2026 01:43:26 GMT  
		Size: 86.6 MB (86590664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed5fdf83d377ee4870e771dbc46fd2be487ec01cd722b9312274ee88a4fa4d8`  
		Last Modified: Wed, 20 May 2026 01:43:24 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.5.1645-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9dedb6f5715cfa50c7aed1ad80872ff1cb74f6c14eb304814a60deb68f62ab90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7500322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45e7cf37452ad6b4a0ee7cab2e981592a8b9468bdd5d910f56abe44e80e53d33`

```dockerfile
```

-	Layers:
	-	`sha256:8b43b96e17435e82fd203244c36b4ef14a5564bb6e18b45405af78f222febf49`  
		Last Modified: Wed, 20 May 2026 01:43:24 GMT  
		Size: 7.5 MB (7486938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b683684bad784306cf4dff8dc8efd2ee0029fc4b653bcd6c9b8a4deb1354a82`  
		Last Modified: Wed, 20 May 2026 01:43:24 GMT  
		Size: 13.4 KB (13384 bytes)  
		MIME: application/vnd.in-toto+json
