## `clojure:temurin-11-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:3a92c00648887781ae816e9b4ade6a91c0f39414f2e32f91101a96d57fe33a6b
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
$ docker pull clojure@sha256:4bd2b55073be40c92a86730a56bc2f98008b9e7c86dfff1ae84cea002c27ce70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243566702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4bfc738c6cc4a31191a4bd224d7e6537121ed062bfaa111c0279cc4829de54e`
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
	-	`sha256:abe1fea375429ba91b23776f15f53da4ed790fa2b779b40d20f21e69bd66de5a`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.2 MB (28228321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:466cc6eb31b01983068c13ba53a2aa463e5e8aff1b8c23634bda342930089d68`  
		Last Modified: Tue, 21 Oct 2025 13:02:34 GMT  
		Size: 145.7 MB (145658336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5bd1d244f29914d7abdb7b8ec1891c7ea3762eabd18dc85a79b1ae64efa241`  
		Last Modified: Tue, 21 Oct 2025 02:20:57 GMT  
		Size: 69.7 MB (69679400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009f3cc79f1b2798478976de1bda1764c1d6bed7b815e2f9f8643f95d116cb7c`  
		Last Modified: Tue, 21 Oct 2025 02:20:50 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e568137259532fa05bc78ef669ffb8a55b016034cd975f7c565ad3f54b38858a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5147839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:986b62fc63c92ffde07cc30a59ae6a056fe041bd007000fe125f3bd41094e35c`

```dockerfile
```

-	Layers:
	-	`sha256:37ce52edfe6e332bc08ec2aeff17216f51c54f74b03680737a4e93703fdb31a9`  
		Last Modified: Tue, 21 Oct 2025 09:35:51 GMT  
		Size: 5.1 MB (5133529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02df29d5e864fb4803c462a625f5a10ac95ff058743b7b7d90f4c884e30ccca5`  
		Last Modified: Tue, 21 Oct 2025 09:35:51 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c606729340b268e2ef6d61ecbfeece607d215ab47c367b2cfa8b236243f670fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.1 MB (240123917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ceedebfcd8a4c90be6383f4e991d0b3c5ee0947b4c1f06d0e9fc9c7e2ad3ae`
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
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44dfa17b7b9a6a46e97b622545899a48fa9bdf82cfe30f2802b1386cb347264`  
		Last Modified: Wed, 22 Oct 2025 09:15:11 GMT  
		Size: 142.5 MB (142460630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ea2d9d8746d0e7f639f5c4b4f9ac78f950621b7910eae5b370fff4a9b7917a`  
		Last Modified: Tue, 21 Oct 2025 02:26:38 GMT  
		Size: 69.6 MB (69560451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37165f91dc2679eabcd948f67b7b296a6a02e9c043f6c8e8c4a629f9f8b61d68`  
		Last Modified: Tue, 21 Oct 2025 02:26:31 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7c89fcb750fec2e33e9959c978e7994031c2a2f7741611b362a3fa77a94654ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5154335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53c117dae6677ba4eb09d80e24fb73fdf430a527dfd534ef801b32c1004de3de`

```dockerfile
```

-	Layers:
	-	`sha256:31a5f17f88cc7d6e462fb2e39862f961be7d0d80424d0d4b3f834bb7aaf88b51`  
		Last Modified: Tue, 21 Oct 2025 09:35:57 GMT  
		Size: 5.1 MB (5139908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e95f6e6674aeadd6a64eafc18870631a45e5ad85870f4c81ca1bd473bc6813b`  
		Last Modified: Tue, 21 Oct 2025 09:35:57 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:4d2a292b1b7b28aca24f99e5fbd7b3a70ac19005fefa7a47cbaf9bba57d18404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.4 MB (240435669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ed9331b335abf97a3ea512ca96216ca98a1ddd20682e54aec6ef32d1a6e0b0`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1760918400'
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
	-	`sha256:5a28d569c39dc949a4743122d7b5ec2d2e0664f1276c801bf984a711d80f2a1d`  
		Last Modified: Tue, 21 Oct 2025 03:26:43 GMT  
		Size: 32.1 MB (32068780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff2c1ebb85c9254a8c8215d014dbb150b8232a870379303a35902ddf787dcca`  
		Last Modified: Tue, 21 Oct 2025 15:34:29 GMT  
		Size: 132.9 MB (132853184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8353123ed4f283e716438da8629fcb7ac2e122540c7142d655242d3b5824f6a`  
		Last Modified: Tue, 21 Oct 2025 15:41:44 GMT  
		Size: 75.5 MB (75513062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ea8fc94f9b963583df1c38e8901135690adf705f784ee5232dbd395525d5ae`  
		Last Modified: Tue, 21 Oct 2025 15:41:38 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a6cf9d0405a0c1f02c38dd56b4885e92dadab9a8f36821e3bef3e055d17f324a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5152430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df4f0b1bd6cb0c3406c52938256418dc06ef7255979ca057c699e459dde0205`

```dockerfile
```

-	Layers:
	-	`sha256:3c0e4b6a39fa8f7558ad4fd752feea258e1edfc39764f52df6b8bae33af1a5d0`  
		Last Modified: Tue, 21 Oct 2025 18:35:21 GMT  
		Size: 5.1 MB (5138072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd47b5f3f02d44fe42550e10c1e55091506d1fd7159451da918421725975cb66`  
		Last Modified: Tue, 21 Oct 2025 18:35:22 GMT  
		Size: 14.4 KB (14358 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:4ca62d3ba003b167b6c3d107eb7ddca40b3474cf0340fecfbaeb2d3ff42bfd60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.0 MB (220997979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386ef8eda4bf91f4602ec8964147ee8741693ecc48066e46c93eca008e54970f`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1760918400'
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
	-	`sha256:43b0f588b497b17691a3547afa4ae41853829cffde6930e6425ddae4a3f89278`  
		Last Modified: Tue, 21 Oct 2025 00:21:28 GMT  
		Size: 26.9 MB (26884356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50113bb2be2d3e54d7b0c4bc781100dd4bc7275ca7ed4b6e4f3767eb2dd761e`  
		Last Modified: Tue, 21 Oct 2025 21:46:42 GMT  
		Size: 125.6 MB (125622140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab170f33b8f9b51acc1aa864f3d195c6c7b5c2f5e39d1546d5ca185dfbbfcd66`  
		Last Modified: Tue, 21 Oct 2025 21:55:37 GMT  
		Size: 68.5 MB (68490837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60eeba7352782c1eed26c3fc2a8671c401f3ec4e7c5c7e1e3cdbdc7c7af94c86`  
		Last Modified: Tue, 21 Oct 2025 21:55:28 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f717a5b6532d09078684d7ab937b35c20d2ab82cc90da0d78ff1c8a3eed67b7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5139164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:033ae5ed6c96387fc039f0dfda4526d029aac2dc0a4cf262ba395f50489186a1`

```dockerfile
```

-	Layers:
	-	`sha256:e52bbc0e2bf770cee613b6ee83d6e77a930e95ecd8f7cfe0124ffa5b27e53128`  
		Last Modified: Wed, 22 Oct 2025 00:35:22 GMT  
		Size: 5.1 MB (5124854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4c841c0945325ce5216364f1ccfa71fc5ed0877b8db9ee8c424741b1fa359bb`  
		Last Modified: Wed, 22 Oct 2025 00:35:23 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json
