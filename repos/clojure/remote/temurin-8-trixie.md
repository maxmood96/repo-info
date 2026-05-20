## `clojure:temurin-8-trixie`

```console
$ docker pull clojure@sha256:0d3186a5ddfa2b0ec04a6056df3ebb27cd3ea8370747029bbdce2d9e34945b2d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:2d83f56e24be75d58752d9cd4aefd38def5397a8b345bcb3042308637f5f9e4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.1 MB (190117479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44237e2cf283050a425c0f9efcb87aafe5c3a556ed968b87ada2877bff6268a5`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:56:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 May 2026 23:56:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 19 May 2026 23:56:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:56:53 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Tue, 19 May 2026 23:56:53 GMT
WORKDIR /tmp
# Tue, 19 May 2026 23:57:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 19 May 2026 23:57:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 19 May 2026 23:57:10 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f32f49ce655a9cf7c1fd4ca1417ddb39a54cedf4b7ff35de20f8009c18dd7a96`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 49.3 MB (49310623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbce9701f2bf39bdc30cd421cd94a2f138ecce3508230ae6c9cf2c1e75bda97c`  
		Last Modified: Tue, 19 May 2026 23:57:30 GMT  
		Size: 55.2 MB (55198723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1c998097dbeb1cd273863140e11bd65230cbb4a4824e25e4ac93376281f8fe`  
		Last Modified: Tue, 19 May 2026 23:57:31 GMT  
		Size: 85.6 MB (85607487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b6add56129b32e0a349fd1f56506bb234294a585632bbeccddacf5e99cca6e8`  
		Last Modified: Tue, 19 May 2026 23:57:28 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:18d4afb4ace5d53b8b27a15d81f7205735f5895da6ab9643974f334e8570d0a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7606180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d275046412ef39f04463e8a4e24a9d24b0da69e79309b8f53c75b90a1a7008d`

```dockerfile
```

-	Layers:
	-	`sha256:9cf08c352c869a2bd3e9631907c4229d8705bd7a594a5b2982bbf2ab8147d96f`  
		Last Modified: Tue, 19 May 2026 23:57:28 GMT  
		Size: 7.6 MB (7591856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:229091aff973d9c20cb7470610c73a050125c3eff407161c35aee7c2265275fd`  
		Last Modified: Tue, 19 May 2026 23:57:28 GMT  
		Size: 14.3 KB (14324 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:656fb2140d6084a50f2ffa2a844c5aa4bc5c06f2109895e86ab60a7a1ca551fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.4 MB (189377414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05569689333b9aac5f13d42237ccae2f95eddbf6e4f148e49ef3fdeaeb1e921e`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:03:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:03:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:03:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:03:09 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:03:09 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:04:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:04:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:04:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:635135721e54f918d2d81497bc66b71f98aee3b440dd6498218827c56d7d277f`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 49.7 MB (49672220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417494103773eca6dce729242fa226d69f1817b5ed6cde44b8e24b53db77313b`  
		Last Modified: Wed, 20 May 2026 00:03:42 GMT  
		Size: 54.3 MB (54272904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd1ed07e61fa6b46e946eb03a654226eccb5932f1a0a1340629c2dcf14c8263`  
		Last Modified: Wed, 20 May 2026 00:04:26 GMT  
		Size: 85.4 MB (85431646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502a420e51dc6f64111a4c8617ea23a90fa96677aeb09f5065c2c2b123c9993c`  
		Last Modified: Wed, 20 May 2026 00:04:24 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1d945a2e45be7e5d041c1a70125bbd3e8d8bdef1b517d5ebb97ae0713dcc3049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7613391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c939e7598e4e248048500a4597394b61c9beb7d4dc56274ce8e213cf780273c`

```dockerfile
```

-	Layers:
	-	`sha256:8c6a329e383c1e7c6e90cb24d3863ec191a3d3200c8107279224d891dd2c4f14`  
		Last Modified: Wed, 20 May 2026 00:04:24 GMT  
		Size: 7.6 MB (7598949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55e989b19fefa9ba677a8e2a5a8c7d384fc3c63e42bbb1d62ca894829ff7bd66`  
		Last Modified: Wed, 20 May 2026 00:04:23 GMT  
		Size: 14.4 KB (14442 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:f3865e36feaea26063b21c71d8ee683e95e2d49969bcb55f4d81ea0739d97180
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.8 MB (196829252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ddde30cbff8377357cb403e0c9ba6d4729c4bb9630b4ad38693199b42ff6939`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 05:43:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 05:43:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 05:43:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 05:43:58 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 05:43:58 GMT
WORKDIR /tmp
# Wed, 20 May 2026 05:47:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 05:47:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 05:47:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:55497c62a793e62a2e78a3fd85fcedf060da73e331ad107733199ea991106b96`  
		Last Modified: Tue, 19 May 2026 22:37:59 GMT  
		Size: 53.1 MB (53132182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb131e60882c6c99b34f1d0a5dae1d4e8aa1c48896f5ce690177030acaede9bb`  
		Last Modified: Wed, 20 May 2026 05:45:06 GMT  
		Size: 52.7 MB (52669123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0ccae12463b954d5c10e3820ca631c9a3aae8a01b4541ce6c12f86903e5646`  
		Last Modified: Wed, 20 May 2026 05:48:02 GMT  
		Size: 91.0 MB (91027303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7031bede0c294952eb49fca17a22024f132c8881b4616203c92f96d1df982ba`  
		Last Modified: Wed, 20 May 2026 05:47:59 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3a4547ea6c465ec04e8829cfb862093cdbb2c91dfc93dc63ab192e48c341298b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7611243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f76c7b7abeb3053f9871d17780b7c1e18e70ab0ae0b1bdaca1e7de6897732175`

```dockerfile
```

-	Layers:
	-	`sha256:b9b2298fd66760048ec32cdd7451e8a535b99d906346a9aa31bcd777f5a5e2ca`  
		Last Modified: Wed, 20 May 2026 05:48:00 GMT  
		Size: 7.6 MB (7596872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:519f366eb77dee293270230c670712eda03d5ecfc842cf9a39b012d35bc2342d`  
		Last Modified: Wed, 20 May 2026 05:47:59 GMT  
		Size: 14.4 KB (14371 bytes)  
		MIME: application/vnd.in-toto+json
