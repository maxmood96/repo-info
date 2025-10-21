## `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm`

```console
$ docker pull clojure@sha256:46d1c843f62c2d616c2a5b55931dff02ee81fa591214916e237c512b4976323d
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

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:984d126f7dbe28ad4627d53957ad7c1172ea4ac57bf6cacaf869850df1abe968
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275287134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:033d9dbb830aeac6526530391c38dee06bda2160a2401f4a13890ccb74628111`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:cd01849e3cbdfc6993640303768edbb56372cf9f1ae101d516334c8d462341af`  
		Last Modified: Tue, 21 Oct 2025 00:19:25 GMT  
		Size: 48.5 MB (48480563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801881f575f94423d8282dd87e841cfc39eb090eef6ee3a96f5695a20bbe01db`  
		Last Modified: Tue, 21 Oct 2025 13:03:29 GMT  
		Size: 145.7 MB (145658335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f1c46995d5cc84969ed8736112c3a9f557ba513b33989d5144e3e8dabb9d5b`  
		Last Modified: Tue, 21 Oct 2025 13:03:13 GMT  
		Size: 81.1 MB (81147591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8e11db79818bbb5c9d15cb9dbf4f9ca659dda799fd16bbd8c3ce9ab96017ff`  
		Last Modified: Tue, 21 Oct 2025 13:03:05 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:5448865b49aeccb7bd60e340676d73812ccac839cbbce84feb133cc0f6c91bf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7409283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01770ff6d9f64241d6c4accb38143c4788e7817a3cfe8b9a47a8f910fbf3acc9`

```dockerfile
```

-	Layers:
	-	`sha256:711b060d14d537ee46a69780ca76137231b1350bcd115b5f9f65dd27f242344f`  
		Last Modified: Tue, 21 Oct 2025 09:35:44 GMT  
		Size: 7.4 MB (7395031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c8cf31b284eace9b90f4cf1b6e13d0ee9b9a070626089827c0fbd08353129ef`  
		Last Modified: Tue, 21 Oct 2025 09:35:45 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f397bdf8234e5b816adc8ba7d564fd4ce220e5cd77cab4dd3d0e3b9c6c3c02af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.8 MB (271848749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:443c3742fb77283cec312e8046c34df57712481ecd04d9a6306f894797637f25`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:394d8e61f78f890cc5a49345ac4d4eb6176cdcf6b4b6af62502ae74b1662e421`  
		Last Modified: Tue, 21 Oct 2025 00:18:41 GMT  
		Size: 48.4 MB (48358996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf4ff441e1e139d3d55c506bbfe01297495240642a95ec9334409a63cdf6be0`  
		Last Modified: Tue, 21 Oct 2025 02:25:45 GMT  
		Size: 142.5 MB (142460648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5523df84bacc24e11eadb6076c7de2b41fc03fa51e3dabf2e6b725150605e30a`  
		Last Modified: Tue, 21 Oct 2025 02:26:37 GMT  
		Size: 81.0 MB (81028461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05f47e30cf9ffffb9d9591c4083cc30db044d41af0b74c76bbf7dc15dffb614`  
		Last Modified: Tue, 21 Oct 2025 02:26:31 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:50f418d95a675316e6ee5dff3931d8bb3bf240e952bfec610b674d861f19fcf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7415781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc46f261535a08b0481129fefde378151586afcf455074702e6e9b9ea9346f5a`

```dockerfile
```

-	Layers:
	-	`sha256:e8b555a2b20c57241a2446595a55c0bca73f67bdc1fda72f397f27bb63d14b49`  
		Last Modified: Tue, 21 Oct 2025 09:35:51 GMT  
		Size: 7.4 MB (7401412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:532b5c91072dcd77affcfee3119ca47f0f7f63611f972417c6db5ed60b587559`  
		Last Modified: Tue, 21 Oct 2025 09:35:52 GMT  
		Size: 14.4 KB (14369 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:8be7ca7322d5950decec901f5ad1d1cf1cc5351de8861d8dc774759e911baf0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272166445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69abf0173728ffb25251049ec7123f8d9fb86a5bd6463c843583747ccee5e15c`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:812b25f785969d275d8c3962568c03f83ccc4df31b95f01c0646d79d6d5069f3`  
		Last Modified: Mon, 29 Sep 2025 23:33:30 GMT  
		Size: 52.3 MB (52326764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9775786e5c038055f9d7cc602cd56de1156477d7f85bdc656ed523ac899b868`  
		Last Modified: Mon, 20 Oct 2025 15:04:43 GMT  
		Size: 132.9 MB (132853219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c05fc04e08c8ee438f729e27479a91332e16ec8a996fa5f431557ee825ea9e5`  
		Last Modified: Fri, 10 Oct 2025 05:06:51 GMT  
		Size: 87.0 MB (86985817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9d31ec937561d28ddd15a3057db26ca0db3c5aa7c1a2d28b47c598fffcc5b6`  
		Last Modified: Fri, 10 Oct 2025 05:06:41 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:4e5ea0cda19dbb3955b382ba36402ed2bcda8bdf203701a224e5cfa6fb45afbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7413930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b594eec0451ed954f5e1376661504c011ac08930c9f8cb7a8106f7f8b9accc05`

```dockerfile
```

-	Layers:
	-	`sha256:09d677d873f665a27357004483791b9e65baed927b390cc2f6dd9ae49fa53eb8`  
		Last Modified: Fri, 10 Oct 2025 06:36:20 GMT  
		Size: 7.4 MB (7399630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:842634ce71b32c1b02f71170be5c112a77adb86728ac7fb4f5de2931742e7bc1`  
		Last Modified: Fri, 10 Oct 2025 06:36:21 GMT  
		Size: 14.3 KB (14300 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:b9dd2ba73cd893dbc6a14a7e0a717a4d11f097111099e4124d63ab5bbe639d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.7 MB (252717118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d0114fc77516c9ba6ef70efb99fc6e81e1a5f829eb056e01cafdf756a322fc5`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:87d1bec83b35277b636c6e05b9418301b2f025752d7539cecae442f0b94d8fbe`  
		Last Modified: Mon, 29 Sep 2025 23:33:26 GMT  
		Size: 47.1 MB (47137446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ec68282f946501e8651907346ed42431fdda18b82c1c7e69c431aeba35370d`  
		Last Modified: Thu, 09 Oct 2025 22:51:30 GMT  
		Size: 125.6 MB (125622159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34bdfe8467dd2698ecc2ffa419932836648f79704247866140a0dc4a2c1f2cf`  
		Last Modified: Thu, 09 Oct 2025 23:03:11 GMT  
		Size: 80.0 MB (79956868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e03453b517d71ca21d3882d1f9d7fd3049f8ff016eaec5302f636b9766e981ef`  
		Last Modified: Thu, 09 Oct 2025 23:03:02 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:7b532bc8f30cad5e0e58ae2647acd39f5d338d6a25ebe1d53efd694d1ceb185c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7400606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75e08589dc938fa4d195254aa3f92b030e5133ca6edea700cc13d5a92d624e95`

```dockerfile
```

-	Layers:
	-	`sha256:d77ef8841754db1f026b9c757f84fb5c64e58b39e4d89412d2377706145c7171`  
		Last Modified: Fri, 10 Oct 2025 00:35:15 GMT  
		Size: 7.4 MB (7386354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed2a9941730e0eb89c52e42126483de80c9b2dae249baa9bbf0b631f1d40f71c`  
		Last Modified: Fri, 10 Oct 2025 00:35:16 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json
