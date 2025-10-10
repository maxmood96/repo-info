## `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm-slim`

```console
$ docker pull clojure@sha256:106bc866948a634b8fc50b65ca11a42be21f8ffd7c351386e9b84e1de88c0301
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

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm-slim` - linux; amd64

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

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm-slim` - linux; arm64 variant v8

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

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm-slim` - linux; ppc64le

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

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:067a88c77b617181d7dea65c2c5fb6f72e868fe6a285fbd075088aae84758030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.0 MB (220997765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64682a7db19a3dd9927d264834ed48f4c52d4291ecfa01488588ba3c7e508724`
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
	-	`sha256:aa291952ad59c6ea9569bb51a04baaf55248795f16158a7bc208077b119a10d7`  
		Last Modified: Thu, 09 Oct 2025 22:52:28 GMT  
		Size: 125.6 MB (125622160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752ecb05f21b9b6eb4e76d3383ca53fe4c3c747636799cb3e6e966f689257fb1`  
		Last Modified: Thu, 09 Oct 2025 23:04:09 GMT  
		Size: 68.5 MB (68490640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2dbf058ddc20d1fea82b18a49257e33b317274049287f1cad042d7eba179874`  
		Last Modified: Thu, 09 Oct 2025 23:04:00 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:58c8d5c2583be9e01077886c5ad0028dd50bc5049cc67ce4913e02ee8ca094f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5139164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be7089e2a5b206ecaecf0125e6fc36f86c254f196c25bc2a105bccf533cf1475`

```dockerfile
```

-	Layers:
	-	`sha256:5262eb7f19ff76a97f278e0341806364dc0368c9509508b62e276c0020d51daa`  
		Last Modified: Fri, 10 Oct 2025 00:35:37 GMT  
		Size: 5.1 MB (5124854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c594fd65f7dbdb4606ebe7b41865c785fa4795784157c6ab71bb855833c787e`  
		Last Modified: Fri, 10 Oct 2025 00:35:44 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json
