## `clojure:temurin-26-tools-deps-1.12.5.1654-bookworm`

```console
$ docker pull clojure@sha256:e979552dd12ffec4ad140b6e586ef978ffb821d35c671b4c235b9815920dc428
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

### `clojure:temurin-26-tools-deps-1.12.5.1654-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:c41ca23e50a83fadf23f85492874ab88b753514849028d997f051b46b760fdf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.2 MB (221152919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:864d02e0cdea5932b5ca91dc803936d5a3ff66d312c655fea3e16229bff47de2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:21:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:21:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:21:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:21:45 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:21:45 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:22:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:22:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:22:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:22:00 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:22:00 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0356f91f3c0f6cf51a06bef168076305bb38854ffba8a3c69027d32c29326e69`  
		Last Modified: Fri, 19 Jun 2026 02:22:23 GMT  
		Size: 94.5 MB (94524351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7c645e2ae65020c93b471b0869496179f16b80adde317355f9137a42a11a4c`  
		Last Modified: Fri, 19 Jun 2026 02:22:23 GMT  
		Size: 78.1 MB (78125484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b390a26472e593ff6f2506b6677c7f89bc6a1446d7ca85f73012e8f10fe786`  
		Last Modified: Fri, 19 Jun 2026 02:22:19 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113104c41ddf2a52dd69ea25d2b0da27218f77d07858bbf118eb668a5cd00867`  
		Last Modified: Fri, 19 Jun 2026 02:22:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1654-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:3eeca58711f31890216574447b7d74bc0d2d4abbd1bc6a5bdb9d9b5ba8591b77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7358318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d676f6146f0f4a307b83cec2a6c4ae08f22b558a8c07cfb7dfc92f7727c54300`

```dockerfile
```

-	Layers:
	-	`sha256:284bc35af8dfc8a4b40efe30d8770cde1800b8802c6e8c29cb97904ea191c592`  
		Last Modified: Fri, 19 Jun 2026 02:22:19 GMT  
		Size: 7.3 MB (7341709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:253013a57f89ecd95d98a663c8ef8c69c26e4fb7fc08a9426f5210666fbbfb6b`  
		Last Modified: Fri, 19 Jun 2026 02:22:19 GMT  
		Size: 16.6 KB (16609 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.5.1654-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:86abf96921470fd9eef0ce6ff59879696e2e230b4b2d8491c34bbb7b7db3851e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 MB (220023903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67f3fa20599807fc64c8bc9406c6595e0f27c66dd5a9e8bdc99bfb06c5858c69`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:21:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:21:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:21:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:21:54 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:21:54 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:22:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:22:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:22:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:22:08 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:22:08 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a67f775c910af1e7030eda26520240eb5b262217312b4df0b96c7f976b43da`  
		Last Modified: Fri, 19 Jun 2026 02:22:30 GMT  
		Size: 93.5 MB (93504354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b56706a093985f547d7ab4f27c1343051a47b247dead2ec9e89c79887e8f638`  
		Last Modified: Fri, 19 Jun 2026 02:22:30 GMT  
		Size: 78.1 MB (78129491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a01435535851137b0bef0742c32c1d83bdf4a1e1ea931f31be333273f77318e`  
		Last Modified: Fri, 19 Jun 2026 02:22:26 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae2a8498ddac5e031764ce208b67484ff0af5195a0497520fd516d87aee61df`  
		Last Modified: Fri, 19 Jun 2026 02:22:26 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1654-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:a7fef1f2da5bfa3d4045bb58f588f6e53015f0873cb20297b0453a6555ce39b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7364244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b517947b015347bd6ca20df4a7b5452689bf24bbc581e5a6f29fc628cb15694e`

```dockerfile
```

-	Layers:
	-	`sha256:e0518d4def86a87251b7741b05301a3f995d54bd49bea337069b444f624fc719`  
		Last Modified: Fri, 19 Jun 2026 02:22:27 GMT  
		Size: 7.3 MB (7347493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92f201561e13f0ce723a300597dcec662079528557fd47f2e688fe3bc8ce1b1f`  
		Last Modified: Fri, 19 Jun 2026 02:22:26 GMT  
		Size: 16.8 KB (16751 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.5.1654-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:0b866681b47af682b5e7de71262f2c385de87f8a1f45b9d35a149a09ad834415
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230208369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07c31aa61095852b93c5af374d88b668b81dffeb56e7e8b53ed243ce11dd4de5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Wed, 17 Jun 2026 00:07:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jun 2026 00:07:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 17 Jun 2026 00:07:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jun 2026 00:07:21 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 17 Jun 2026 00:07:21 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 03:00:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 03:00:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 03:00:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 03:00:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 03:00:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:88b94a58fac236a778527a3293ccd0ff4d309bff0bf314017ea5af603908fa2e`  
		Last Modified: Thu, 11 Jun 2026 00:21:34 GMT  
		Size: 52.3 MB (52346670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4759a87d2ab24b2fac4a2500d8d0888984823a78af74fea7debdc9f59a4aa41`  
		Last Modified: Wed, 17 Jun 2026 00:10:39 GMT  
		Size: 93.9 MB (93902050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940df2f34b1e0014aa6aa124f88b9936f280fddd171bdc3d254cb812f7f501f1`  
		Last Modified: Fri, 19 Jun 2026 03:01:02 GMT  
		Size: 84.0 MB (83958608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bcdbeac267d49bb6f5f446de16e6eafec8e50e80d29ea2e3c9a8e1c625ec5f9`  
		Last Modified: Fri, 19 Jun 2026 03:00:59 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37e871d9748d28fdf14174eed6ce36119943c7369b5208b7aa5073f1eaba6cd`  
		Last Modified: Fri, 19 Jun 2026 03:00:59 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1654-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c9810c5af5edbef65325c19a3e90c60724cb98424f680abe8ef91f04e04f9758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7347542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccb9171c1927bc8c0eb7bdf4aa95f51c9bc1e1e081cab23e206583b45bb9edb7`

```dockerfile
```

-	Layers:
	-	`sha256:5c1bb7f633d71bd16f70b13bcf10c8f9a0c97e3448f2bd9b70d7e26d8b6c18db`  
		Last Modified: Fri, 19 Jun 2026 03:01:00 GMT  
		Size: 7.3 MB (7330873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a639f8c41df30af64b2a7fa38e725192495e5dd21c9afe571593dcefd7da1e57`  
		Last Modified: Fri, 19 Jun 2026 03:00:59 GMT  
		Size: 16.7 KB (16669 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.5.1654-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:74293377218599846d86b8a3ef976626cadabed31d17caa8cecda898963634c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.6 MB (214629002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8557536613feb92eb0267dddc29c0e674b77cdadcb4434607c4fc7fb64afd9ef`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:22:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:22:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:22:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:22:54 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:22:54 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:24:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:24:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:24:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:24:06 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:24:06 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b041a55a85cc0e47dd570746852cc1b0fee042f3a03eb250b9f896ac4aa74a3d`  
		Last Modified: Wed, 10 Jun 2026 23:41:01 GMT  
		Size: 47.2 MB (47161500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93dffac2f0aa26f15bbfc00b26f8e00f41d28e225af70af77c70295cf7b0a6c`  
		Last Modified: Fri, 19 Jun 2026 02:24:28 GMT  
		Size: 90.5 MB (90536936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e6022c19afbe49d4acdf5ac59cf718fdd24167b8c419a1d079bf4ac1789afac`  
		Last Modified: Fri, 19 Jun 2026 02:24:31 GMT  
		Size: 76.9 MB (76929525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e5d2985448e7f674132609f54a07c7d2d5de813f0b21aa481e0f4c9671bb3a`  
		Last Modified: Fri, 19 Jun 2026 02:24:30 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf8727fe20f04ed92e50130f7e94f80256f1b15874dc47fc9f563c1a5f5554d`  
		Last Modified: Fri, 19 Jun 2026 02:24:29 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1654-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f6ffac119ca7708b6e91d89bc57e74ccde0170635bf01f326f40517746b293c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7334823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c4d7e9900dff90d8777a44cd8067ba8aa9bf8b36eae65658205a8b0e2e93e5b`

```dockerfile
```

-	Layers:
	-	`sha256:f1cdf5caf3560bfd63257db39655fb95b92001484ebdf2341773cf6640225a4d`  
		Last Modified: Fri, 19 Jun 2026 02:24:29 GMT  
		Size: 7.3 MB (7318214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9d879f5035a5b3ad22c7a74c9458374e3a8827b5a43e7e86106ff301aa63c1e`  
		Last Modified: Fri, 19 Jun 2026 02:24:29 GMT  
		Size: 16.6 KB (16609 bytes)  
		MIME: application/vnd.in-toto+json
