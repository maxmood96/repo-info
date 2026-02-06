## `clojure:temurin-11-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:cbb8f2e683270cc7a22d8fecb66399de6454f4b10cc63c45d1dfaed04cbcca8f
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

### `clojure:temurin-11-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:f782241b8650009d587bdebb90d34f02407976e985d4cf5a49ca87bd462562e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275439559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f898b650f78a78e600df9274c76477aff91c10cd3722a2372c28633109a62e6d`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Thu, 05 Feb 2026 23:02:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:02:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:02:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:02:39 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:02:40 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:02:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:02:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:02:55 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91681e5699bac06dd1a9f8909502fd18f6c9ec9afcdfe969b927d746ff06dfe9`  
		Last Modified: Thu, 05 Feb 2026 23:03:19 GMT  
		Size: 145.8 MB (145806944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37cc25482f50c40d24e6f80b62915fedfedad48ff44952aac63d43664d1f8afe`  
		Last Modified: Thu, 05 Feb 2026 23:03:17 GMT  
		Size: 81.2 MB (81150485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab88883dfbf3f54eba4d8ad46d9436b0c5eec75c5bfe5ac5b90e6e7e503675f1`  
		Last Modified: Thu, 05 Feb 2026 23:03:14 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:142eb4f86cee9722a9937caf005fe052b874176f915ff37e2ed439c996dc30bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7411139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5814864c8b887f42133816ce8fa66e91a5aa0f9e61de7e86bff2964d44cd787d`

```dockerfile
```

-	Layers:
	-	`sha256:d504b3f3e7ea885a304d26c8e96d7d6094f279953462b85b6808507bdde00396`  
		Last Modified: Thu, 05 Feb 2026 23:03:15 GMT  
		Size: 7.4 MB (7396930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd682a24901c275325d719b86cad490c761f96ce79aab26da1e04e9c6c85ca53`  
		Last Modified: Thu, 05 Feb 2026 23:03:14 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:143e22ab67435cde2931c3bb6198e4065dc621796c991f83e238b0339ed9356f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.0 MB (272006051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feeec0eb067bcfffcbbbd380b46b8cdf13a15d9bf2a6da932e2ac4118865a209`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Thu, 05 Feb 2026 23:03:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:03:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:03:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:03:50 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:03:50 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:04:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:04:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:04:05 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986a50998e27079a9d0d4d16696e49f26d56974e06d74ab594828790d580f9f1`  
		Last Modified: Thu, 05 Feb 2026 23:04:30 GMT  
		Size: 142.5 MB (142500849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c1c12416ecb6a74821827c0e74d4751159e00021c3fcf3e0bd4b38bf0fcf8e`  
		Last Modified: Thu, 05 Feb 2026 23:04:29 GMT  
		Size: 81.1 MB (81138601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06b037c1f929c2ca6ca6a338474caccbf4b31a659f9c0e4246ff75a00b939c0`  
		Last Modified: Thu, 05 Feb 2026 23:04:25 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:cd012d3e7919c6b4a1e4ad6e85ef842c16e2603f9662eaf12c09c7b1a05b4d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7417638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e452cb009e50a02c762da5b8a408427080573872c3b9192e8e9554fb636bda4`

```dockerfile
```

-	Layers:
	-	`sha256:13cf619b609cf50d22f6fa3d25b500ea1a1a679dd54bbaf7af14826f3cc4c5cd`  
		Last Modified: Thu, 05 Feb 2026 23:04:26 GMT  
		Size: 7.4 MB (7403311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7633e6166b711c8594c655a79880faa28c1914560e14cb4034d1c9d5283a7673`  
		Last Modified: Thu, 05 Feb 2026 23:04:25 GMT  
		Size: 14.3 KB (14327 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:09756de361311d99603542ac98f362fca7c4c1fbaba3bfe6d404d8d9972b0994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.3 MB (272311632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c0c522477d188297f8b84288d49488c7392326623e89ecdf747670cd99bfe2f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Fri, 06 Feb 2026 00:09:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Feb 2026 00:09:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Feb 2026 00:09:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Feb 2026 00:09:08 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Fri, 06 Feb 2026 00:09:08 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:16:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Feb 2026 00:16:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Feb 2026 00:16:21 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:5e189aacb842725e8d1d9877c9ab9af09e14901412b6665e179393112b5bca51`  
		Last Modified: Tue, 03 Feb 2026 01:12:57 GMT  
		Size: 52.3 MB (52327289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fca2015c73f0e5915a5a50bde838bd96f27a1612025ed2ce13be0761e803a5`  
		Last Modified: Fri, 06 Feb 2026 00:10:51 GMT  
		Size: 133.0 MB (132996872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c36c06e628592da7eb4af05a96eac490864d1f375f33dda1bfbdb165d724ccc4`  
		Last Modified: Fri, 06 Feb 2026 00:17:10 GMT  
		Size: 87.0 MB (86986825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8970ef07a31bbce8ba0d0ffab2195964a3415a2306b3bc59c7aade8a2868c5`  
		Last Modified: Fri, 06 Feb 2026 00:17:07 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:e39e92b191ab95319577c957073fe961469459da30d469394656379fef7ff22d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7415788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e236e940a46ea853fa0d099eeac4f147f1e540575121f2a07fb870282ba4fec`

```dockerfile
```

-	Layers:
	-	`sha256:4805db26f3e6171b35001fd1adf5b0b4105bcbe628b48e3f34d0f951b432f80a`  
		Last Modified: Fri, 06 Feb 2026 00:17:08 GMT  
		Size: 7.4 MB (7401531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22e6c6b42940d9fe33d4b08aab20762113f4debc5b069c1d8e2ea8ab34131aaf`  
		Last Modified: Fri, 06 Feb 2026 00:17:07 GMT  
		Size: 14.3 KB (14257 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:0fae2d89492fed5d699304c5218888d1c931fc027efdf0ee097ae47aa3622da2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.7 MB (253664241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9a691796a4a87d0a5cc47fdcf1ddbaebecf016126bbbdab22f05873c4441304`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Thu, 05 Feb 2026 22:58:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:58:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 22:58:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:58:30 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 22:58:30 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 22:59:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 22:59:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 22:59:58 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:4c4c4621da5085342b3b0d8d8ef57e5e44004eedf5818268af30c41a02cb6cf2`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 47.1 MB (47138343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8abc06cf4a82deb45e513d7f6178329e2b35b3d5a8bb810144ac55f73283f61`  
		Last Modified: Thu, 05 Feb 2026 22:59:08 GMT  
		Size: 126.6 MB (126562172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e791b55c7b2f552594da15ef0902adc534dd74752e530dac30a7311ab638c7`  
		Last Modified: Thu, 05 Feb 2026 23:00:25 GMT  
		Size: 80.0 MB (79963081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc6c6b1c10481d9a6deb6ce15500c6746d2eeca4dc135317392e1a5d932950b`  
		Last Modified: Thu, 05 Feb 2026 23:00:23 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:2e639c0cd0b6f57484b7a5b4d18196157721b27410234359ec15f6d62e9d2b4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7402462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b3a506c4f27cffd3da5b9bcb192d024d001804a80741e9d1d0877522b006ef1`

```dockerfile
```

-	Layers:
	-	`sha256:9ecc418b3f7a6708f4b8d4af263cd125108b15d82e61f3aed10d11c1de4b762e`  
		Last Modified: Thu, 05 Feb 2026 23:00:24 GMT  
		Size: 7.4 MB (7388253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b53a806fe688d17f182543e51b04c93acbdc20d6760ab0f027679907eb4903f`  
		Last Modified: Thu, 05 Feb 2026 23:00:25 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json
