## `clojure:temurin-8-tools-deps-trixie`

```console
$ docker pull clojure@sha256:3f2d42806a3a3cb2790bd0689202262a4093c8dfcace20f39d0d80f7ec150584
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:72997d2826809d562ce81b833f8be07f8a5856b1def4ba7655d102ef83a5ac0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.0 MB (187027502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e30d15fe242ee8769c4fb35d3170e38a913ff89f70dc5daa20b889cd683da8b6`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 17:42:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:42:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:42:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:42:26 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:42:26 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:42:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:42:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:42:43 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f32f49ce655a9cf7c1fd4ca1417ddb39a54cedf4b7ff35de20f8009c18dd7a96`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 49.3 MB (49310623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc47d29bba037e4339b003a54ee5d7de82114830fa032a5e47a2284ffd9c282d`  
		Last Modified: Thu, 04 Jun 2026 17:43:03 GMT  
		Size: 55.2 MB (55198716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb7c97ccea2400a9167de4e4c9ed09a8e9424acdbed617b6e09925ba1bdaa827`  
		Last Modified: Thu, 04 Jun 2026 17:43:04 GMT  
		Size: 82.5 MB (82517517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15af6db42da9125728c93346522fd3b8b2efd1a8394c5b4eb16cf34a00e5271a`  
		Last Modified: Thu, 04 Jun 2026 17:43:01 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ddc070b2f643bc260f4f431eee9f375dc6703578cb0cde13628744c7de0ccfd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7603455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:706abaee40640792d1840df4cf52e845488cbc4fb9cda7dae1c6301426022ffe`

```dockerfile
```

-	Layers:
	-	`sha256:0cb35f69c49fe4f35e69580e74d97be0dcad394e71a429762099a2a40feb9e98`  
		Last Modified: Thu, 04 Jun 2026 17:43:01 GMT  
		Size: 7.6 MB (7589131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18623eb99dc064d16582a59632840dd6fb306e296af3a1b5b7afeb4a93d362c8`  
		Last Modified: Thu, 04 Jun 2026 17:43:01 GMT  
		Size: 14.3 KB (14324 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3809651644374210d1dc3d79a81737df089e37cc160dbf35c2107dd67c534401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.3 MB (186283953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8b4ee56db1257ec12bb440e628ca6028d6145fc96ebb81a727122f7471e46f4`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 17:42:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:42:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:42:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:42:20 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:42:20 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:42:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:42:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:42:38 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:635135721e54f918d2d81497bc66b71f98aee3b440dd6498218827c56d7d277f`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 49.7 MB (49672220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3128760ce8b3932b960240ec1e786c3160367861a0d555e41aaef2b6ef5d636d`  
		Last Modified: Thu, 04 Jun 2026 17:42:59 GMT  
		Size: 54.3 MB (54272927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0796e2fef79bfa22effd40622cf61a24a3f265b4ed8befb3ad5c6fdfc4b45c81`  
		Last Modified: Thu, 04 Jun 2026 17:42:59 GMT  
		Size: 82.3 MB (82338159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfc9a28dbfa61aff8b65a59435e42a16d574b03701d8c05b5a74d3dba1677f9`  
		Last Modified: Thu, 04 Jun 2026 17:42:57 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8aee9c63d0b5efd3ae134e215963f86a85bce8630aa0fff17146c5541568710e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7610666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdfdd2bbddba9e2df6ceab230d595c0d22ecafd07ab552dc69cdd8248d0bb2b6`

```dockerfile
```

-	Layers:
	-	`sha256:e5483acfe1575cffbf5d4d50b66060ccc089ba24b5971cc2d03d7aacf969a7d9`  
		Last Modified: Thu, 04 Jun 2026 17:42:57 GMT  
		Size: 7.6 MB (7596224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a8253e8e0d0762141b0865216c881512f38710cca33a31e8c74549502da3342`  
		Last Modified: Thu, 04 Jun 2026 17:42:57 GMT  
		Size: 14.4 KB (14442 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:6a3637f9aca337368c6f77f527ad7353b939c2cd953d70bc267463b1c4173ac8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.7 MB (193739797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95ae20dc1f57130a299d28544a4a0218154cc36f752d36e4f8f14ffe65a27dd8`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 17:44:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:44:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:44:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:44:47 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:44:47 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:45:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:45:48 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:55497c62a793e62a2e78a3fd85fcedf060da73e331ad107733199ea991106b96`  
		Last Modified: Tue, 19 May 2026 22:37:59 GMT  
		Size: 53.1 MB (53132182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1673d3cdac0410eed27d928b8c6fcc805e6b6c1f8bd6b2bc88a4e988ee9f13`  
		Last Modified: Thu, 04 Jun 2026 17:46:38 GMT  
		Size: 52.7 MB (52669153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1d144fbced401e62bf65cabda5a7cd707cd3466a674d3791eae34116732bee`  
		Last Modified: Thu, 04 Jun 2026 17:46:39 GMT  
		Size: 87.9 MB (87937816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5601cd42754cb27dedc597d90b69527e3305f38b1f9a9718e36a38c0e6f10153`  
		Last Modified: Thu, 04 Jun 2026 17:46:35 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:41b23b7c93b778e65bcb2fae5daeb580960792ed1309dc4f89bfe61d9d38002e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7608519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72971cf81c22486b812dfdebc22b39582c7d4ad0a177f0fa6818a3e15d5a68b3`

```dockerfile
```

-	Layers:
	-	`sha256:8fba01475d74f20e158c013ef9dae93db4318b295cb9e15b2188cf4318d7dc8e`  
		Last Modified: Thu, 04 Jun 2026 17:46:35 GMT  
		Size: 7.6 MB (7594147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c388573edbb7b55ce32a35b8d0fd57bdb78dd21919925d73a51621dfaed4dc36`  
		Last Modified: Thu, 04 Jun 2026 17:46:35 GMT  
		Size: 14.4 KB (14372 bytes)  
		MIME: application/vnd.in-toto+json
