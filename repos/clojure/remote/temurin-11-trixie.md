## `clojure:temurin-11-trixie`

```console
$ docker pull clojure@sha256:e19966ffb593906ed152f33f6096f763f4be06081914f5efbbf1de46e7499c55
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

### `clojure:temurin-11-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:3c53be9ea33456a3d4d16913d2bde33e890719efc9e4d92c10fa6c1b4f157194
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.7 MB (277714655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16fa041e2bff7f8d93d3c2822aa7e71857620c88914108f974983da5f1d7720b`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 17:45:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:45:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:45:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:45:39 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:45:39 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:45:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:45:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:45:55 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f32f49ce655a9cf7c1fd4ca1417ddb39a54cedf4b7ff35de20f8009c18dd7a96`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 49.3 MB (49310623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7961cbbb11abbe780bb282f281d95bbb014d4ea65aaf1d196c6ea86a7b88c23`  
		Last Modified: Thu, 04 Jun 2026 17:46:16 GMT  
		Size: 145.9 MB (145886263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ee601c774bbfce7bb0e243053e4fdf027b46590168e580587e390011d505ac`  
		Last Modified: Thu, 04 Jun 2026 17:46:15 GMT  
		Size: 82.5 MB (82517123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e41fa01755bfe180a1b89c07f5fdc23687f5b33e80e7380335cc346ebe2d64`  
		Last Modified: Thu, 04 Jun 2026 17:46:12 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:45234af02c19f9479c8bfab857d22e818f385804c9411d39bb70586e5699f5b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7502626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caca133bc2059149158971ebae9c7a38efd761e582134dcece44a42fe5e5b01b`

```dockerfile
```

-	Layers:
	-	`sha256:7f09e912bcb6c2718501dd85c96f54108d57316d28eedab8ac972f5e570ab175`  
		Last Modified: Thu, 04 Jun 2026 17:46:12 GMT  
		Size: 7.5 MB (7488287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff2bca59f1299cac9b89e1810a97d089220ff155c61fc518f731e52e128514d3`  
		Last Modified: Thu, 04 Jun 2026 17:46:11 GMT  
		Size: 14.3 KB (14339 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:915f499a0c37967c91c93e123b1cb7721fa2751132462bddd8c8d29008f7db73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.6 MB (274593299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66fbd844f8a71dfe56b227b5c01304284d78acb04c0768e292caeae4467be1d3`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 17:45:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:45:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:45:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:45:37 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:45:37 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:45:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:45:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:45:55 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:635135721e54f918d2d81497bc66b71f98aee3b440dd6498218827c56d7d277f`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 49.7 MB (49672220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5066f1a8babb6d627b5f78c798a23d8001819b3d197e598c73253edfc2e37ae1`  
		Last Modified: Thu, 04 Jun 2026 17:46:19 GMT  
		Size: 142.6 MB (142582235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0888bf007c985f1977f9aadff5be2bf4cd8fd8f120bb9efe0c94b5e1c40ab9`  
		Last Modified: Thu, 04 Jun 2026 17:46:18 GMT  
		Size: 82.3 MB (82338199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa2a9055fc961c8e24fbc888f535e4c8607a18b73eb1d5ce0b452ee384123b2`  
		Last Modified: Thu, 04 Jun 2026 17:46:15 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d84b144d450bb8971138ddd6a9aedd7682c22b61a427772843abb3892e56c3e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7509755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a8c510bc9ff8eb18f21207a07a600d2b003352f2374ba5881d9bee2f552b024`

```dockerfile
```

-	Layers:
	-	`sha256:19e32de3d916d038971432af526a9c3c13cb7e2ad9827e7720f5934cc4d9eb92`  
		Last Modified: Thu, 04 Jun 2026 17:46:15 GMT  
		Size: 7.5 MB (7495298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:628034fefe7260e661252f8412efdfeefe7bf652dc80205cffb2c4859ef7ddea`  
		Last Modified: Thu, 04 Jun 2026 17:46:14 GMT  
		Size: 14.5 KB (14457 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:29c48c099b92a43b552fed44e63ca3adb98969acd77e4e304fcd65c1d874dccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274180932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21b8d4fd2c4d794178cf1b905ee5e43219f8de89fb5e55d80686e4d1d0f53da7`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 17:50:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:50:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:50:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:50:24 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:50:24 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:51:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:51:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:51:10 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:55497c62a793e62a2e78a3fd85fcedf060da73e331ad107733199ea991106b96`  
		Last Modified: Tue, 19 May 2026 22:37:59 GMT  
		Size: 53.1 MB (53132182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91fa5e0dab8382a47cddbf98542ec1fd458e09183790d7d69c6930b01b1f581`  
		Last Modified: Thu, 04 Jun 2026 17:51:57 GMT  
		Size: 133.1 MB (133110217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23bc2298bfff1e502d14b5e090568de211dbfe783a2ba64394ba3a8fdef334c2`  
		Last Modified: Thu, 04 Jun 2026 17:51:56 GMT  
		Size: 87.9 MB (87937885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d616bc42e44ecdf53f4aa4fdf8368a27986344ecb1eaa62d14211b0545bfbeb5`  
		Last Modified: Thu, 04 Jun 2026 17:51:52 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6cfaf10c792a65e907d8523c9c51ad563b09960b6f08aa3ad2545d4a56fd19c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7506480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55d6a6050a9f2e6759c14168bef8bf73ac28dba59e5b72dc0008091083000740`

```dockerfile
```

-	Layers:
	-	`sha256:4cbe4b472ef45f212eec3bbae09eac6f4622e77f2007ee04f63d1a815948eaf2`  
		Last Modified: Thu, 04 Jun 2026 17:51:53 GMT  
		Size: 7.5 MB (7492093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdf421e0d1542590098bd3cfc92e7cb4b9cb740fcadccdf7c7abb68ce890fcbf`  
		Last Modified: Thu, 04 Jun 2026 17:51:52 GMT  
		Size: 14.4 KB (14387 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:7216aa5e24125ce87f088244f731fb760ce310896dbc330f0fa491d1fcecdadc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.5 MB (259533983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc834f15a17d9a9d8568e4749af33693b9019b5747b9c033b0e9197826fbca3e`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 17:41:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:41:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:41:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:41:28 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:41:28 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:41:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:41:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:41:50 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1540dbb0587ae9097c9d04c50809503aa74d42814940d640c6659645acc0bc6c`  
		Last Modified: Tue, 19 May 2026 22:37:00 GMT  
		Size: 49.4 MB (49379780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f38a9a10021642d38304ca2f4835906120ee9f5d7b6ae1fcbc21934d29f896`  
		Last Modified: Thu, 04 Jun 2026 17:42:21 GMT  
		Size: 126.7 MB (126651735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a638341d837531fa6a920057cd8b6bd3f54bbe02fa31836c4473108db6488920`  
		Last Modified: Thu, 04 Jun 2026 17:42:25 GMT  
		Size: 83.5 MB (83501823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97902c5b6619e71b6ba5e9b84c9cce519051feecf1fc9f20cb0fe14596d577df`  
		Last Modified: Thu, 04 Jun 2026 17:42:17 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6b118deb4fc5b0e424452c227202224c5b981d4120deb0bb0e3c216f376ed187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7498552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:858ba02009abf0bfa82902acf0027f167cdb736cd8c03c8e53b012ca1016c1a9`

```dockerfile
```

-	Layers:
	-	`sha256:0623aa18d7db7a7322167109b5df0d489a5c1a5cafb429c460e5f972c3398f20`  
		Last Modified: Thu, 04 Jun 2026 17:42:22 GMT  
		Size: 7.5 MB (7484213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c5c682c25eb5043152bb937315d631a94804d0de5a6a7a5f402047df18545fc`  
		Last Modified: Thu, 04 Jun 2026 17:42:21 GMT  
		Size: 14.3 KB (14339 bytes)  
		MIME: application/vnd.in-toto+json
