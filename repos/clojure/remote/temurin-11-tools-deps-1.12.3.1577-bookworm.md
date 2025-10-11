## `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm`

```console
$ docker pull clojure@sha256:1422a63600fad0a8db08d5dc788cc222462743796cbf6ada4e4994c3cefad08f
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
$ docker pull clojure@sha256:33a88c138ec41cb097401e5744f71235e21ac723cac41df9032ebde6a0e416d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275286602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2f94702eb0a120bc933493de8e099495c3870778d1c2ce6bd20df83a4b4118`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
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
	-	`sha256:c6b11972fd12973831818babf60f1ffc1c4047507943d132dffc612884022858`  
		Last Modified: Mon, 29 Sep 2025 23:34:14 GMT  
		Size: 48.5 MB (48480557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd346097a1d46e82ad870b6227b1b0ba6b5e994aae4c80b68f5bfd2a8f865fc`  
		Last Modified: Sat, 11 Oct 2025 04:32:59 GMT  
		Size: 145.7 MB (145658311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502f5e9037d98129936e5d25421604a268851d3ef7e38e6e5535b151a1d61aee`  
		Last Modified: Thu, 09 Oct 2025 22:27:36 GMT  
		Size: 81.1 MB (81147090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb68d34a395d6a2ea0969ea2616836099d68efa52f1e1656eba32bf667ade5d`  
		Last Modified: Thu, 09 Oct 2025 22:27:30 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f997c6fba2df409effe731195db12d7bde1df2bfc760400616b480dbf668cf28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7409283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d5989e51a9ca872aa562668456e7f41d94762e464cc67bb3d6e1ba2bbb4ed87`

```dockerfile
```

-	Layers:
	-	`sha256:f01adae2c8e0885315007a5e01412c7bb4150ea7565913e34892660fd112d3a1`  
		Last Modified: Fri, 10 Oct 2025 06:36:04 GMT  
		Size: 7.4 MB (7395031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fec71909697c2e51075073019affd681d362cf4057052347bef112385afda41`  
		Last Modified: Fri, 10 Oct 2025 06:36:06 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d6b3a17ab3dbc02f5ef7ed3c487895c27b2b1065bb18b90565fd8576978927d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.8 MB (271849611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592a442f7d686634b26321849fe1131a3684a12a30f6cba11f35f6deb683827a`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
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
	-	`sha256:f7b43f0d0a8b99591b27457b368e70a582002600d32503fd07798c1bee7cd134`  
		Last Modified: Mon, 29 Sep 2025 23:34:16 GMT  
		Size: 48.4 MB (48358915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e025e1df0671783a5decfe1ed63c0f2f2b7137d0eddfa4c07cbb06bcf1117c`  
		Last Modified: Sat, 11 Oct 2025 04:33:50 GMT  
		Size: 142.5 MB (142460578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b18e2a4df821d2e2ca106e5f4c72d1035ae08003a9ebab59e3c6dd066b89b1`  
		Last Modified: Thu, 09 Oct 2025 22:27:34 GMT  
		Size: 81.0 MB (81029473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f83aea7e9375fae587c8da4abafe7a3d980ea9186ac161466654c144af8b411`  
		Last Modified: Thu, 09 Oct 2025 22:27:29 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b86097d2889fc397d0edd08dba975920663d657a61e8a90e90b69b20dc3db062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7415782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66db3fc6d567bdea6656633cc3495aeb05b67cfb7ff1bd6d556762f0e68b9026`

```dockerfile
```

-	Layers:
	-	`sha256:25869b3e7e031f275bae081fdc727a979568550a19cfaf216aa06e53ac9edb7e`  
		Last Modified: Fri, 10 Oct 2025 06:36:12 GMT  
		Size: 7.4 MB (7401412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e63da4eaa486e045d462a30b3670b8a619f98190bd979972faf24dced1678b60`  
		Last Modified: Fri, 10 Oct 2025 06:36:13 GMT  
		Size: 14.4 KB (14370 bytes)  
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
		Last Modified: Fri, 10 Oct 2025 04:57:26 GMT  
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
