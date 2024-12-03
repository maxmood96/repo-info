## `clojure:temurin-8-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:6297d56f0569b2d4aaed86a238c43107e2c3b8ef3561f4dbf38373211cbc992d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:5352587daacc53ebe7ec440dfc6cde430af3af75f4646d5fdc5c850e94244a84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232876097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6964db4bd9eda58c443c14d4741338e7d68cf2a37037ea56087326a5e0bab18`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:fdf894e782a221820acf469d425b802be26aedb5e5d26ea80a650ff6a974d488`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 48.5 MB (48497210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46afd374d1f5883e7fac7dbc3c08e8ad4ed34400bf285a382735561528bb976`  
		Last Modified: Tue, 03 Dec 2024 03:19:25 GMT  
		Size: 103.6 MB (103633923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd60a82602ac3561a02627c6ba3d5b3355a177e4c6d63b8e5564c8502bd2b93`  
		Last Modified: Tue, 03 Dec 2024 03:19:25 GMT  
		Size: 80.7 MB (80744320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2986535e01aa9cd9bbea9af281829f44f7f15fe85ae096106420e20137c2e8`  
		Last Modified: Tue, 03 Dec 2024 03:19:23 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:18406002dc24d6511fb729a6dba60ac215e9d4314772f7d38af1426e00c1c631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7317586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a10f5faf034b73b12e9bdc149431898ebea7ca2ba5ceabebd4b76e45c1eaa6eb`

```dockerfile
```

-	Layers:
	-	`sha256:69e12e72f35e850b2a8dec3c11bb21efe8dd149f9bcf04df8531198b68b687b7`  
		Last Modified: Tue, 03 Dec 2024 03:19:24 GMT  
		Size: 7.3 MB (7303345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b44ec66afbf5fbf1d30838e21dae1baa71363279787642b9b15d1a098eff496`  
		Last Modified: Tue, 03 Dec 2024 03:19:23 GMT  
		Size: 14.2 KB (14241 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:75fb6ccbfe3a065eda7137da6650e5adce5153be3940aaa486515896c87539b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.1 MB (233133641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e013a5279b65a78fab0c7002adf32e84a0a3f8ae1bff4aab93dbe90ab45a4c`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1a3f1864ec54b1398987bbe673e93d8b09842ecd51e86ab87d64857b70d188b1`  
		Last Modified: Tue, 12 Nov 2024 00:56:20 GMT  
		Size: 49.6 MB (49587201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27189750e14ce1c29681e47d9469dd8c2a66d939a975563f578cda090c27b4bd`  
		Last Modified: Sat, 16 Nov 2024 05:11:00 GMT  
		Size: 102.7 MB (102747706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a58e9f441e15a322b18f947ad179525da3c4709a5c6acca42801977e9f41c9`  
		Last Modified: Sat, 16 Nov 2024 05:15:45 GMT  
		Size: 80.8 MB (80798090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13cff59b386112042106e9d1ea9130509e182aef89906338cdb316e56964cefa`  
		Last Modified: Sat, 16 Nov 2024 05:15:43 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:8600c8be048a99c1e2cc1e28209045213296580e5e8750aca8f567fd635558d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7325420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1c891c3482e42785a4b8e6bd340d8a1a8a74ff7073fdb69a3f4357e3839ce41`

```dockerfile
```

-	Layers:
	-	`sha256:4c939eb1e74268750c2b350fb9aaa252b4aec956f196bed4e153a7af9eadf118`  
		Last Modified: Sat, 16 Nov 2024 05:15:43 GMT  
		Size: 7.3 MB (7311060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b57ca8355bf780ae01ceb1050c77a9efdd746b41bfb49408bff61a4152b1a40`  
		Last Modified: Sat, 16 Nov 2024 05:15:43 GMT  
		Size: 14.4 KB (14360 bytes)  
		MIME: application/vnd.in-toto+json
