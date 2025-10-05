## `clojure:temurin-11-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:19758944a788f158b044a5d0d1f811ad2b3ef18cdd088e7d6ef090cfa53594d5
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

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6a9bcbee39ee2acb192388e5f6d401dbb2f6840b5e206b4fd44a474ac7dd9b50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243566908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd0bfc1b5b3872571d825d7914044d6037a9199579868d281b13bfe9bea4aec0`
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
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24ae6560d61717f596685e0a0876ddeb0607a428595293c926b95830ab3d653`  
		Last Modified: Thu, 02 Oct 2025 12:45:28 GMT  
		Size: 145.7 MB (145658168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d137361de2c8ee970d910c469c5b7c0093cbf7d56e48bab27b9b35d0fa3ff8be`  
		Last Modified: Thu, 02 Oct 2025 12:45:24 GMT  
		Size: 69.7 MB (69679760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ab9859593f970151074f89c91d0445fbacf637cb33545898387cf80fd7d909`  
		Last Modified: Thu, 02 Oct 2025 12:45:18 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7ab2bc525149bab537b2478157bf7f9f168e39fbb3c29c33001fd57233498805
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5147839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c14333a5593204ab2832bac7c9a8d13237650259745642dea0c2b5cc6167cbea`

```dockerfile
```

-	Layers:
	-	`sha256:6b1958ec7e5a8beac8a6857322b05faec11836efca6f0ebeef2a18d3e44544fd`  
		Last Modified: Thu, 02 Oct 2025 12:35:38 GMT  
		Size: 5.1 MB (5133529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:761f0ddb67bf4eb1a0383e01eb1e0d05059b39afb299e846caff9394adff15ca`  
		Last Modified: Thu, 02 Oct 2025 12:35:39 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:93ac560ed0ac95fbe86b117db280828f658ed4e9b4d844bec03c99cc019b7f1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.1 MB (240121921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db07995fb1efbd51e10dfb43549d02c927d419dfb30e417e773552270bab09b8`
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
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da6e7cdf11293fee99646019d2b32994f71f7da8934e2a0426948c369095005`  
		Last Modified: Fri, 03 Oct 2025 09:08:28 GMT  
		Size: 142.5 MB (142458701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2263a7e181c559c5cdf6429f5b7826ad9cbe2b93f491a8fbb8c95e3482ecf76b`  
		Last Modified: Thu, 02 Oct 2025 02:42:00 GMT  
		Size: 69.6 MB (69560432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784b384130c00251044e4b2cc2f8936bbe11abe0c9ff012a0249e7ad381edeef`  
		Last Modified: Thu, 02 Oct 2025 02:41:56 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6001cecdc2525952a22faf2c840b2ec2583020d685e910e877ce7c2aacc8315a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5154336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b47ff3190e5f249ad5c831c162a825a657253403571e8cc51324bb4df033269`

```dockerfile
```

-	Layers:
	-	`sha256:776b251946815af508db23bc1770df2901625423a0535111a1d13c7f9bdd7e2c`  
		Last Modified: Thu, 02 Oct 2025 06:35:52 GMT  
		Size: 5.1 MB (5139908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40d3ccea332944c039bb7ee089b2bfedaa4964449bc368d6c47170c8d2498af4`  
		Last Modified: Thu, 02 Oct 2025 06:35:53 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:581d2e9d0d43c0b66c5f37089a71fb550bb6ed958977593ca7b9847157673860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.4 MB (240435927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76e6d7b922510f1fb86944348771a87ee84a8062736e02756a6b078f94a2af96`
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
	-	`sha256:2dae4fd387571f8090d4bc2fed08c7939fa2ac7aed0e2814aea4306333899e47`  
		Last Modified: Mon, 29 Sep 2025 23:34:09 GMT  
		Size: 32.1 MB (32068697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ddb2f7a53498fa8a4cc426cb43d224857888cf0ceb94fa48d644ae324348e0`  
		Last Modified: Sun, 05 Oct 2025 11:53:00 GMT  
		Size: 132.9 MB (132853347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73fe5c8f6d84883e11e1bbbb4e46d4401823fd9d9a59984e40126bb20070e319`  
		Last Modified: Thu, 02 Oct 2025 08:34:13 GMT  
		Size: 75.5 MB (75513238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24cd59090a44f0443ff65a3448887e4022fac19e4a0e72701e476847e551f6b`  
		Last Modified: Thu, 02 Oct 2025 08:34:08 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c5cbcb4f63f961954ce030288b1757978a4330818404d8809f78f59badf257ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5152430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b4aaf201a90ff3aee3e579056b867ae76b49af9a5baa589426aea5908b3c70`

```dockerfile
```

-	Layers:
	-	`sha256:ee889be18dfdf96a569f623715c6756599a1c39d916386665345cae19458bd48`  
		Last Modified: Thu, 02 Oct 2025 09:34:47 GMT  
		Size: 5.1 MB (5138072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66bfe54b3f72f0dfb4907d3b97443c2b68196e32a9d24b1c15c127ece2a53713`  
		Last Modified: Thu, 02 Oct 2025 09:34:48 GMT  
		Size: 14.4 KB (14358 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:310265e9766b8a6fe6d12526c7faaf2720b0fd83d983fd8cccee28ab21778ebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.0 MB (220997331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1adb4653c9e2ca0b249dffea01481274026c7a37cad208cd4df0c13461ce2d0`
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
	-	`sha256:ee23af7e2c95e7ad71a0f6edf7e138d45ffffb442811e2b9572806a68ee1338e`  
		Last Modified: Mon, 29 Sep 2025 23:34:05 GMT  
		Size: 26.9 MB (26884320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73cad13d67f0ce708a718e6fe181d120ddccd08391c3633576d8eeee39a4ef7e`  
		Last Modified: Thu, 02 Oct 2025 04:19:06 GMT  
		Size: 125.6 MB (125621580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc08a7ea13354790264bb2a30ffda26ed0bbc024a5744b54323bcf7de0d2950`  
		Last Modified: Thu, 02 Oct 2025 04:25:02 GMT  
		Size: 68.5 MB (68490787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2876caa99526bee744707e6568ce2cc9def725e00f30097a7b7aa646d8758a50`  
		Last Modified: Thu, 02 Oct 2025 04:24:55 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:316d705aca1264335e1bda166f6b638d91d745f23ec9e0ba017b333594052679
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5139164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c744e3cdfae8e1080cc3455812ac45f6c151d3f06216ec740d56abeff6f11fff`

```dockerfile
```

-	Layers:
	-	`sha256:bfcc3357fb51bcc95a7d053fc4c47a9232e56c811e3f13cdbaefd841bf668bde`  
		Last Modified: Thu, 02 Oct 2025 06:36:03 GMT  
		Size: 5.1 MB (5124854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a484faf1fda954a5d4580bd87a8c250601ed26d35b8c1d5cd23d0b5b5b614f3`  
		Last Modified: Thu, 02 Oct 2025 06:36:03 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json
