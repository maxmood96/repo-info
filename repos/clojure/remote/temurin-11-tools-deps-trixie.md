## `clojure:temurin-11-tools-deps-trixie`

```console
$ docker pull clojure@sha256:8fd5031ef565d8004221dfd5d1c6e61178fbfa1deaf75c89c6ac0ea756ea32e5
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

### `clojure:temurin-11-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:7e5aacb470211b075c1ed26ca0dd88b5738154a4ad61f692ec8836f21a6cf6d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.8 MB (279796278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa000e6459ad1c911c588b034b535413702ee4a6be374886288782194b438a92`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 01:50:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:50:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:50:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:50:55 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 01:50:55 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:51:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 01:51:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 01:51:43 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:40 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a917e6b25a84a6551baa755c552a80909a4dd29f235cc2641e403c8c56694f9d`  
		Last Modified: Fri, 16 Jan 2026 01:52:06 GMT  
		Size: 145.0 MB (144966647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4872559af8df3810c5812b8abf865881077f6a9546b8e3970b6a1c527be9b97e`  
		Last Modified: Fri, 16 Jan 2026 01:52:04 GMT  
		Size: 85.5 MB (85543365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d85e27187463932a7a9810c990cae3c508f50115dca6735a8cf9604501ffaa`  
		Last Modified: Fri, 16 Jan 2026 01:52:01 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4770010254944b4e7c2e1c49175989465049cacf6865317fbcf9a1496975ec24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7502150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d253ca15bfdbb7115a2da3327b7abca70b0597d5e908dff7b3cf345960c326`

```dockerfile
```

-	Layers:
	-	`sha256:4fb26bff4a19cded796d7a6a2535cf6ba77fcc1ef612a9d2752061e172ccdcf2`  
		Last Modified: Fri, 16 Jan 2026 04:40:19 GMT  
		Size: 7.5 MB (7487965 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:760f0c6b8a612ef07d9f02dd3d1faaf845c0edb10ef43a551521c2b0c70d36f7`  
		Last Modified: Fri, 16 Jan 2026 04:40:20 GMT  
		Size: 14.2 KB (14185 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bc926a1d98e015be4c8376ca5aa08a33a3c652402d01de85b19e5158630ac13c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.7 MB (276739917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:145a9c59233721767f0861ed1e21964cca4638c64e288e80603717be66665b8e`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 01:54:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:54:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:54:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:54:52 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 01:54:52 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:55:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 01:55:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 01:55:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:51 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8b9f41a5185d4231dd2f748a14cbcb9392325c2f1d78a6a98697b57954016d`  
		Last Modified: Fri, 16 Jan 2026 01:55:35 GMT  
		Size: 141.7 MB (141729867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0eedec83f596627c9448ade184ac261961d41008dc41bde1f45637f8ee3253`  
		Last Modified: Fri, 16 Jan 2026 01:55:34 GMT  
		Size: 85.4 MB (85361321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb50397e3465efc4371f0486f23207a377bb2851fde872be201d7c04acbf9a5`  
		Last Modified: Fri, 16 Jan 2026 01:55:31 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f4e2e15438f0122a3293c49689b4f1c86166ecbdc84d8013dd64e15dd31051ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7509916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d3be19168c4965f98f722e54a0a0c1864ea648299cad3ded804a1c2fb5b9251`

```dockerfile
```

-	Layers:
	-	`sha256:b63fa0f44cc87fafdda4639125db023c0e8a78cfb36925ec2f5662aca2dbfb23`  
		Last Modified: Fri, 16 Jan 2026 04:40:27 GMT  
		Size: 7.5 MB (7495613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5817c32fa411b484edfb597014f250cb22e0605ffc35dd425b65c75de9bf76d9`  
		Last Modified: Fri, 16 Jan 2026 01:55:31 GMT  
		Size: 14.3 KB (14303 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:ce7a13b1682c3268be0a55eb60b8c084c51dacc92fc46e27d1e188226ef35ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.1 MB (276136867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce7ff6a40abe80bb101913faecc1c9ddcd7ff18655dd80fa0269ea9ed87063d`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 03:01:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 03:01:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 03:01:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 03:01:56 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 03:01:58 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 03:10:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 03:10:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 03:10:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6ff412c1efdf82a2030de7bb593b97f09e02e2b337f615eb1c3faedeef765d44`  
		Last Modified: Tue, 13 Jan 2026 08:45:48 GMT  
		Size: 53.1 MB (53106962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535e69c188d843a40931640c882aeab8cb565638d03ecacffc478c1a783da983`  
		Last Modified: Fri, 16 Jan 2026 03:03:52 GMT  
		Size: 132.1 MB (132079785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cf6113573d6e977a021b3f316871a109b45d115ed8e9d10099d07544c15dc07`  
		Last Modified: Fri, 16 Jan 2026 03:11:34 GMT  
		Size: 90.9 MB (90949475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a765f54699f6a311bca208c4d134eae94afdab6399d259c61b29896e71c296`  
		Last Modified: Fri, 16 Jan 2026 03:11:31 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6e597c04acbdc6c7213c30e4c56f47bc52419d8a339bd595a14cd31e2826dc02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7506004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc0352c533aff85af18875d55402fce758a6a957acc5ef4f76b1223794c25481`

```dockerfile
```

-	Layers:
	-	`sha256:c45455a6839c2140f95c7ecfbd2230abe4c5e22ad4208253b89939cbcd5e1f3b`  
		Last Modified: Fri, 16 Jan 2026 03:11:31 GMT  
		Size: 7.5 MB (7491771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf52180be1b3605015c1645bb32055ba3902443f159b9d1a5adc6762bcfcda28`  
		Last Modified: Fri, 16 Jan 2026 04:40:47 GMT  
		Size: 14.2 KB (14233 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:71f7bac9a2824b31a78287bf378ca57ec4c4133ca737f9f798d3398a7477526d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.6 MB (261553313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:681d2190e0b6c4b9353429a2c97287b2167cb9ccd719a87c0e06eeb8f75c5fe9`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Thu, 15 Jan 2026 23:10:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 23:10:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 15 Jan 2026 23:10:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:10:51 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 15 Jan 2026 23:10:51 GMT
WORKDIR /tmp
# Thu, 15 Jan 2026 23:13:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 15 Jan 2026 23:13:35 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 15 Jan 2026 23:13:35 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9de0288d81a9602539c9f3015fc521191e25eebfe6442c22cb974ea3a486f3a8`  
		Last Modified: Tue, 13 Jan 2026 00:41:55 GMT  
		Size: 49.3 MB (49348704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96aae73d6ca9c475bb213977dcd29121719a295968930d64b57e8491e3a1f0e1`  
		Last Modified: Thu, 15 Jan 2026 23:11:54 GMT  
		Size: 125.7 MB (125694843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf76a7c83996d80417decb31585a6bc4e3577b7808130186ba4d82caad8e7c6c`  
		Last Modified: Thu, 15 Jan 2026 23:14:03 GMT  
		Size: 86.5 MB (86509121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd858370a85287b81e2e98d546afb976f1498881791c9cfa9d90eff409f8296`  
		Last Modified: Thu, 15 Jan 2026 23:14:07 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:61c26fc8be42978f94d2dd550d276b49c75108a6bcd3aee9299331da253db424
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7498075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ceeb0c4ab482c7eb656e38dc3722d1c6941cdbfb00ed4c00e5c7be7e127132`

```dockerfile
```

-	Layers:
	-	`sha256:3cdae701c920f12a5f24033c04db14267e77c6b34b823a6926aa92199a88ec67`  
		Last Modified: Thu, 15 Jan 2026 23:14:01 GMT  
		Size: 7.5 MB (7483891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42c189ef0c4627aec4829db4567929ed49f208bb9d119806fb709a90441a8d6d`  
		Last Modified: Fri, 16 Jan 2026 01:38:31 GMT  
		Size: 14.2 KB (14184 bytes)  
		MIME: application/vnd.in-toto+json
