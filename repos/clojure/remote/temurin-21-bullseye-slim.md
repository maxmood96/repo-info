## `clojure:temurin-21-bullseye-slim`

```console
$ docker pull clojure@sha256:13dd093ffb16b82e77bfa7eec6bf90baf47d7a101b02c5b53ce37ffd8651fcc6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1f23460fb3c8b8e122dec3c94c279ca870d53ad22f0a695ee9c7f9daafb10291
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 MB (247235544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16e55ea9605036bca4f40b812b89e6f91658dfe00d1e54833f622ad4c36e2cb2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1765152000'
# Thu, 11 Dec 2025 22:39:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:39:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:39:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:39:55 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:39:55 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:40:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:40:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:40:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:40:09 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:40:09 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a88499d92e58a9f7d74dc939bd949d9c2d87abbbaaec03b5f87553e69d901a53`  
		Last Modified: Mon, 08 Dec 2025 22:17:50 GMT  
		Size: 30.3 MB (30258465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a9534b09da01f0dc39405aa43d1e43f7e4920d97ad94ebab1b27c48d9cf5512`  
		Last Modified: Fri, 12 Dec 2025 08:04:16 GMT  
		Size: 157.8 MB (157826032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d219a8f3f98c039598072c8e225d74a4fa063b73d93b06bc337be9e4cb5371`  
		Last Modified: Thu, 11 Dec 2025 22:40:44 GMT  
		Size: 59.2 MB (59150006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef80455c4b43f29602a9370c5bf67b583eb8a5981fcaed3f7c394a16d3c1527e`  
		Last Modified: Thu, 11 Dec 2025 22:40:39 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5c3aca70074d1cddf2b50fb6f55a02ace4871fadbfb0542ddbdfd049cc6e44`  
		Last Modified: Thu, 11 Dec 2025 22:40:39 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b96f2d9464a76a0c5d8305acfc267ce049f51e433c2d39768cc734385b7c9b53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5327007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a5a6db81fa32b4c698a3f9857693726b782cb2853b1f9b761da6f26f143dda2`

```dockerfile
```

-	Layers:
	-	`sha256:995e5bb8101ac2e7947c78a1cf8ffef5d291a9ed72ea1bfb418280eb52550a5d`  
		Last Modified: Fri, 12 Dec 2025 01:41:19 GMT  
		Size: 5.3 MB (5311171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d2487afa699bd634430ea604575c60e34c4c1bfe222005bf878f467f9b325a7`  
		Last Modified: Fri, 12 Dec 2025 01:41:20 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f2d19a8c4aff386eda820ea0a217a4f013e62bb6c7988eca476cd186b3ff0952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.1 MB (244141791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ccbd92b8dd3cf9b9b6152a0b3fd3aaae7a56ed820cee8df4224a856c562c2ee`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1765152000'
# Thu, 11 Dec 2025 22:40:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:40:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:40:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:40:04 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:40:04 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:40:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:40:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:40:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:40:18 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:40:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7d43510e20279c4831f5ca1d424a1d56c6c24251d7c93288a50a066dc7e72bda`  
		Last Modified: Mon, 08 Dec 2025 22:16:06 GMT  
		Size: 28.7 MB (28748482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83750cb848feb5d0ae3f9954b5c0203231b4bf84d2a9cfd6bb0d49cd430123a0`  
		Last Modified: Thu, 11 Dec 2025 22:41:10 GMT  
		Size: 156.1 MB (156107638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6c5f245ec6f9f6db1fd423365fadc5a11816adc039e7384c3d29c39135dd04`  
		Last Modified: Thu, 11 Dec 2025 22:40:57 GMT  
		Size: 59.3 MB (59284632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784c59dffa0380a4a12e0383d67f41527266693a3c7fa44f0714d6e7cbdad2bd`  
		Last Modified: Thu, 11 Dec 2025 22:40:52 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309de2c7fb3bf3fb4d407cdf96de54434e91701c9b3a8cdfaa0917542f2481be`  
		Last Modified: Thu, 11 Dec 2025 22:40:52 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:baa5e43c892aace33460187244bfc3b14916c7e00cdf188d16d8e6021802434d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5332857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbda021df89611bc3acf047badd1c9bb63d5b697c71d0ff8294503c8be476c1c`

```dockerfile
```

-	Layers:
	-	`sha256:dfc09c59157d2283070347ef8f453db2c754167c896b89ef459a80167877fc5a`  
		Last Modified: Fri, 12 Dec 2025 01:41:26 GMT  
		Size: 5.3 MB (5316903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b1ab2c9f75c5b6bd99572f3659c52cd7144c57cc178a6fc1cfa6491abae8fb7`  
		Last Modified: Fri, 12 Dec 2025 01:41:27 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json
