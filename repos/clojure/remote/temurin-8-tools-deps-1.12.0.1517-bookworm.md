## `clojure:temurin-8-tools-deps-1.12.0.1517-bookworm`

```console
$ docker pull clojure@sha256:7f86d7329b851040675a54ed7afde397c6751fa003fa92610a33611c7741752f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.0.1517-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:0e763abca58dc7b82b959e9529ee495a22a172cc6fc028419cc25f544d9c16d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.2 MB (184195799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2117c259932878787343ab0d0aa8904efa4c7b6a71a5cc51f99b3d0c063a0d`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:a492eee5e55976c7d3feecce4c564aaf6f14fb07fdc5019d06f4154eddc93fde`  
		Last Modified: Tue, 04 Feb 2025 01:36:22 GMT  
		Size: 48.5 MB (48479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69585d6b47da15afe617a54a489eee3652680cd6a1da7d8d466302454ae7228`  
		Last Modified: Thu, 20 Feb 2025 02:29:32 GMT  
		Size: 54.7 MB (54721245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce843353d8f3ed42c2472c05a45561cf6c75df37e57741f83398115acd39753`  
		Last Modified: Thu, 20 Feb 2025 02:29:32 GMT  
		Size: 81.0 MB (80994222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d721f5903ff05bc70150fe5baf5cb8e1fb428accba232bcd7b9955e8d275b0e`  
		Last Modified: Thu, 20 Feb 2025 02:29:31 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1517-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:8f4f7c68948d79e61ee13a5809b87a6d4f84ea1d5bfeff03422d15f5dd06d987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7306925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a029e8cb8e14747bb16d9f8b38a20f706c48ce34e91e0743ae95e4194fdd9a51`

```dockerfile
```

-	Layers:
	-	`sha256:e975adbe12033d2ca0cf6cc3008ab8e34539cde3555333f883fd568319e7b47c`  
		Last Modified: Thu, 20 Feb 2025 02:29:31 GMT  
		Size: 7.3 MB (7292688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba92eb478c2be075c8fd19ee6f8150ebca1021af4f06be94cbe93e42250f46f7`  
		Last Modified: Thu, 20 Feb 2025 02:29:31 GMT  
		Size: 14.2 KB (14237 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.0.1517-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:24f5f48ba439511c00102504aa0edd312cb3521e507dc322d6a50bdb65932527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.0 MB (182973944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e24288190d93fa54dbf709a867d39266c3b3189bfdf8e60d7f1bab7ea2e45e16`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:106abeaee908db66722312b3379ae398e2bcc5b2fdad0cc248509efa14a819ff`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 48.3 MB (48306553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73158f818927f3d5d74c42ecfa65f28017e7d8107b6335006d95965106742209`  
		Last Modified: Tue, 04 Feb 2025 23:24:17 GMT  
		Size: 53.8 MB (53822777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd95378984ff69528a6e4cfbb8b3f4cdca757403a9afd7dffbd7b5f435e6c08e`  
		Last Modified: Thu, 20 Feb 2025 03:38:40 GMT  
		Size: 80.8 MB (80843969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b879f84f423546016ed12b8565657d26f72bbf4c69579a9a55d274d506b7a9`  
		Last Modified: Thu, 20 Feb 2025 03:38:38 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1517-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b3c7ad65e9f35bb3fa6eb7ec100727918281ca241e98fc89ffd527c8be1c8783
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7313504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d28cd2f17a9e399629b70bcb7f4d63a6f9bfdba0f54dcfc5ce25cfc26317c62d`

```dockerfile
```

-	Layers:
	-	`sha256:7a886df520cd185bc00b0e52533ae9f6dda8fe713da3416819cd0f0b1e08d7ce`  
		Last Modified: Thu, 20 Feb 2025 03:38:38 GMT  
		Size: 7.3 MB (7299149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5586d4893a3c98b230d700394d9ff7ea03f3fe244118173ecc23f449aeae11d1`  
		Last Modified: Thu, 20 Feb 2025 03:38:38 GMT  
		Size: 14.4 KB (14355 bytes)  
		MIME: application/vnd.in-toto+json
