## `clojure:temurin-21-bookworm-slim`

```console
$ docker pull clojure@sha256:218d2e72d39c4b91e02589abe211d997d90e1fcd773699c01a3a3bde85f7089a
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

### `clojure:temurin-21-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d0f0be2ab9f0f35fc8de54cbf5a9572525ce59fdde28e8d4f7ffa5ac56a1f276
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.8 MB (255764589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a8ff0880842eb751040a3dd25abd0ee0d4d8419ca9b4cef9a32dd4a9e9606f9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Thu, 05 Feb 2026 23:06:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:06:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:06:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:06:00 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:06:00 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:06:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:06:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:06:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:06:16 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:06:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:783c00640b8a1f21bd7ca81028997662f8f7e747f3d5a19861a1c5db7b33b183`  
		Last Modified: Thu, 05 Feb 2026 23:06:39 GMT  
		Size: 157.9 MB (157857047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d92e5bb11b3766d692c3d7f06bbdcdee3575948451a08ab79ad0bf80e99fe2`  
		Last Modified: Thu, 05 Feb 2026 23:06:38 GMT  
		Size: 69.7 MB (69678013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c61cd6e606a5a6bf67bbfb72b72835324170c65d6c25e036ea3e97fd78297a5e`  
		Last Modified: Thu, 05 Feb 2026 23:06:35 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0dcd935b329ca5f32604de92434e29a2ebef845b95ba45c268b9a6093c70b8f`  
		Last Modified: Thu, 05 Feb 2026 23:06:35 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:92f13788c83990c69bb82695f2355403cf90922a29fc6badce111824596ec087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7761a7dbe3270cac5d6a3dbb9e4165047c31724aeaafab49037fc66585fefd50`

```dockerfile
```

-	Layers:
	-	`sha256:56e095cdc605e9124d8742f5775f865d9fe40acdf2b8afd181e6db6461db0361`  
		Last Modified: Thu, 05 Feb 2026 23:06:35 GMT  
		Size: 5.1 MB (5116506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:432d955de012ad40808e64f945b8ef9f6eea3b60abe793abbf7194fd67c3c9f5`  
		Last Modified: Thu, 05 Feb 2026 23:06:35 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bfd8ece4ed5155dbf0e1ae596520dc92a12d262b50e5d19c7f28bc2a86666942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.9 MB (253914630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c63423de3df6021d86519d95b756f63f70ffb3e1bbc49874a200ec4f6840be3a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Thu, 05 Feb 2026 23:06:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:06:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:06:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:06:23 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:06:23 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:07:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:07:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:07:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:07:28 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:07:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d01e254986faf809242aaa62557b32c2bc14e99a0d6cd898f34f4b501316223f`  
		Last Modified: Thu, 05 Feb 2026 23:07:00 GMT  
		Size: 156.1 MB (156133048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9f252d5357e58ff2af0cb104af2d11d0f9a58746f49aabb88d9c9dc4770db3`  
		Last Modified: Thu, 05 Feb 2026 23:07:46 GMT  
		Size: 69.7 MB (69672717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4e96f9e0c8ca82fccbc403ba91e80b71a989be42cd625109349e7348d3a0ff`  
		Last Modified: Thu, 05 Feb 2026 23:07:44 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e218135821b68b26fcb39cef9745be969aaf7c08064c60cd246269c78bd844`  
		Last Modified: Thu, 05 Feb 2026 23:07:44 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:67e2f3b33c2ae82fc31a0d0791f6aabbc56fa53573b8664221542c954241fe32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5138221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9818791117aab2d16117e949629aaad789a015a8944bdd5e92f73a8a51f12f8f`

```dockerfile
```

-	Layers:
	-	`sha256:8704feefa7960ebb01454cec7a33cc77d4cf63004e096cbddccfa95553d24860`  
		Last Modified: Thu, 05 Feb 2026 23:07:44 GMT  
		Size: 5.1 MB (5122267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:314514f80c859670e79024d39cee9997599c5fc47262f429bbab7ad432cbe1dc`  
		Last Modified: Thu, 05 Feb 2026 23:07:44 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:32b10db04ee51b86bb595f4737cd2635c9ddf7b389e2bfc1bbe1ba5901e0a539
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.6 MB (265561408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e45247d9ae011d5bac4478a8006dc3020e2032a2c132a93257d8216e35b01ed`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Fri, 06 Feb 2026 00:34:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Feb 2026 00:34:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Feb 2026 00:34:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Feb 2026 00:34:00 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Fri, 06 Feb 2026 00:34:00 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:41:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Feb 2026 00:41:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Feb 2026 00:41:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Feb 2026 00:41:10 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Feb 2026 00:41:10 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7910825c7ec7b68916beacd9af906d34dec10e730af19f67c87aa4e2ee440381`  
		Last Modified: Tue, 03 Feb 2026 01:12:56 GMT  
		Size: 32.1 MB (32068712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f04686be48d2a894920edac0c0c6434c05a7128013df9522a975b048c103c93d`  
		Last Modified: Fri, 06 Feb 2026 00:36:06 GMT  
		Size: 158.0 MB (157977491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ff8ed03f353a0ece5f58bd3ce03806e34111b0130fe1fac2ba69c56d0e8e2f`  
		Last Modified: Fri, 06 Feb 2026 00:41:55 GMT  
		Size: 75.5 MB (75514159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7265c5180d70ca2c83535214d9fd18f098c2a50781f5aad0b7f5df89b09cee`  
		Last Modified: Fri, 06 Feb 2026 00:41:53 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c81e3bbf033fe93b7b083fd05fd6c7bf3ad2317b1c830b56e7b82f3b001ac9ff`  
		Last Modified: Fri, 06 Feb 2026 00:41:53 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7c5a1273be3ad2db6ce68f99aeeed9c6fa55fc981c2e2eecffea7065b659963e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3f6fdf15af8f7d1c96dea0edd31fc8e8663ec3a45bc950fc65b731e53cdd314`

```dockerfile
```

-	Layers:
	-	`sha256:b2bc6f8e55ee1cb6513cd8fdc905f573215483f40106eef0acf448c84abbd017`  
		Last Modified: Fri, 06 Feb 2026 00:41:53 GMT  
		Size: 5.1 MB (5121664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed9b82b833a6e16035e83dbc6f17aef322a511e7ea371eaf5207ab6ae71bbcdf`  
		Last Modified: Fri, 06 Feb 2026 00:41:53 GMT  
		Size: 15.9 KB (15884 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:ce9a8e2436fae3da9e9af9d2ed99e1938a34079a9bc10253b1fe16294710ee02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.5 MB (242480684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3725f6733a71c614246b62c09a3e0beb5f47cf5dbcd6e9ceeb41758fa97265d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Thu, 05 Feb 2026 23:06:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:06:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:06:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:06:44 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:06:44 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:06:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:06:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:06:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:06:58 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:06:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773403c4ac668294912a2f4bf051fccdb773b7f95b012f2359c393546e2ddef9`  
		Last Modified: Thu, 05 Feb 2026 23:07:29 GMT  
		Size: 147.1 MB (147105284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c378967ab4ba8289ea3b6f0834f056aa2928ffba607825b8e155f7a897ad2b5c`  
		Last Modified: Thu, 05 Feb 2026 23:07:27 GMT  
		Size: 68.5 MB (68489976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:690e0a039ed09ba1f7719fe86faba2b1576fbdf42003609d9307311e5a5284d4`  
		Last Modified: Thu, 05 Feb 2026 23:07:25 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67fef3b70f0946f8f228064f0b8526f80a5a4bde0150a76e5747952fe1f80d30`  
		Last Modified: Thu, 05 Feb 2026 23:07:25 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3f024b7e0b5bdc79e6dc269d2735deb44e6069a621913bb7b53dfdab9992c1b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5123662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1240576bc2eff6bd181ae867aef772fbc018ad60022dd38ea1bf16c89fc38f45`

```dockerfile
```

-	Layers:
	-	`sha256:bf49f8402469653d9e12a8fe13d495bba6c6602f2cf499c8c87493904a9c62c5`  
		Last Modified: Thu, 05 Feb 2026 23:07:25 GMT  
		Size: 5.1 MB (5107827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f65ce1ee2c3921150b49acb3cada5ed41ba0df08b611f6503c854c97f292c36d`  
		Last Modified: Thu, 05 Feb 2026 23:07:25 GMT  
		Size: 15.8 KB (15835 bytes)  
		MIME: application/vnd.in-toto+json
