## `clojure:temurin-8-tools-deps-trixie`

```console
$ docker pull clojure@sha256:5b683e04bc712b4d220e74c4de09d3af87383a4fead4d6c07342f03cf96213d5
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
$ docker pull clojure@sha256:05562844f00b2829169955e32a278f7c2474f50e4029b276987c517ac6f79a52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.6 MB (189562510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b280efb0a76d51e754c24fbf3f3a0821510fce1db18f7f9f28245a8097f9f7e9`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 01:44:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:44:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:44:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:44:55 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 01:44:55 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:45:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 01:45:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 01:45:12 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975d188193c45c6c238c8aec640615a2f4c921f694f96b07ea5f3d7be468791e`  
		Last Modified: Fri, 16 Jan 2026 01:45:31 GMT  
		Size: 54.7 MB (54733361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886894cc528500a0949253879f1ec15d79cbb2a8e2f7e1b1314df6603ffbed67`  
		Last Modified: Fri, 16 Jan 2026 01:45:52 GMT  
		Size: 85.5 MB (85542885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6e54bb763b038cfdcdad352e9b3ca962a46e899dcd84c254a00cab06558c68`  
		Last Modified: Fri, 16 Jan 2026 01:45:40 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4fc346600e4853adadbd3822fafeff5b4f1dc428d19a7ab57d983946fdd411c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7603604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d85ce1eaea2430027ac42f2d346409a966b8610de76fe109f92b1fb5c3332b63`

```dockerfile
```

-	Layers:
	-	`sha256:5a3ec59ebc1785914d538ead32893045f96f760da3be6ded54ff1171624b8c1d`  
		Last Modified: Fri, 16 Jan 2026 04:55:09 GMT  
		Size: 7.6 MB (7589434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e57068ce314bc0edbde8adc3d7d1829578b383479b8ace0ffc3eeeb2a1ba9532`  
		Last Modified: Fri, 16 Jan 2026 04:55:10 GMT  
		Size: 14.2 KB (14170 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:070f6a02bcda1676c4cdc2ebc5b614dc0f130b133e0b4628932c9be30b4acf5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.8 MB (188824905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e05082ee34251c75a316cf803fc31f7b7bbaec8c01cfe07b348f249c3c73c6f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 01:48:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:48:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:48:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:48:30 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 01:48:30 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:48:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 01:48:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 01:48:48 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:42 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaec506dc63d309c98dc43468719c5f80bd1c4343751d53224d2ddf85ceb1b49`  
		Last Modified: Fri, 16 Jan 2026 01:49:18 GMT  
		Size: 53.8 MB (53815007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5397cdf36a67130f18df095764b1ac9509ab1c38db8703e9ae4f32d72dec14d6`  
		Last Modified: Fri, 16 Jan 2026 01:49:26 GMT  
		Size: 85.4 MB (85361171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f57661a75336a32ad6d406f4bc8d9c1e1e5367b08c84a7d69b0e556dd66e69c`  
		Last Modified: Fri, 16 Jan 2026 01:49:14 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1e93f25e6d9b1ed067354b5150dcbd0d58daee9db04fe7823525466166431a18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7611450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e88f5744948406a041b9d587a78c4ed199c68448bcdf138d26e1a76c928ad31`

```dockerfile
```

-	Layers:
	-	`sha256:edae2736b1722d8f4677ca82a61874e59608283b86784a97262af8b1fd5d2ddb`  
		Last Modified: Fri, 16 Jan 2026 01:49:06 GMT  
		Size: 7.6 MB (7597162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64c1334bd0b663c891367185f3cb8a538610469e5efd2d7de8c1c19ce6a09945`  
		Last Modified: Fri, 16 Jan 2026 01:49:05 GMT  
		Size: 14.3 KB (14288 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:0291ae7e3be9e9bd86d12bb8ce32ec13a44fab98a86ffe13ce862135eef48d05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.2 MB (196231263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a30137770a3f78d69ab3a22340197ffa836e8d7d6afe34d4b69e1896d9e1534`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 02:48:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 02:48:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 02:48:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 02:48:36 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 02:48:37 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 02:55:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 02:55:47 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 02:55:47 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6ff412c1efdf82a2030de7bb593b97f09e02e2b337f615eb1c3faedeef765d44`  
		Last Modified: Tue, 13 Jan 2026 08:45:48 GMT  
		Size: 53.1 MB (53106962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b450c5f7d58a9a7ac9c8651b6b73ac9e1c6307f2834881a528832693d6211e`  
		Last Modified: Fri, 16 Jan 2026 02:50:15 GMT  
		Size: 52.2 MB (52175110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c920ca82b964ee4b38e2ea68ef7f959ae0fd65e2e69b37269215731655c5ab`  
		Last Modified: Fri, 16 Jan 2026 02:56:50 GMT  
		Size: 90.9 MB (90948546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b38d5cbcd9384f17200229304c4cce6d1cfcaed90ab13c618546eb9f59ee5a03`  
		Last Modified: Fri, 16 Jan 2026 02:56:39 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d2075ea48b25904af77d6a8b093741c5c25825ae4cbe97a50febf0d8f42469bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7608666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ee30abf203d3e63f85c7d50e506d94dd917dc86128b9febee0500a67c1641ae`

```dockerfile
```

-	Layers:
	-	`sha256:bbf66358b18c885b8313be69ed0020fca16d9e4bc094640d6e21db11b79ea2ef`  
		Last Modified: Fri, 16 Jan 2026 04:55:23 GMT  
		Size: 7.6 MB (7594448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40287e1678e3024a79cdbb432b628ea33733188d76a2209209df01bfb5b385f5`  
		Last Modified: Fri, 16 Jan 2026 04:55:24 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json
