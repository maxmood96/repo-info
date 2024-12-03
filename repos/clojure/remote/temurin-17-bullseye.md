## `clojure:temurin-17-bullseye`

```console
$ docker pull clojure@sha256:2742624dddd8dc50bf82029d3388fb3ae6c2b2278c53ac46a43b67d420ded65a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:581eb5e90c3a0fa385ac989aedf87c2bb438848f3249c0ccc2ecb58f5ee89870
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.4 MB (267436546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:743ef814e76b560689842b4f299762962470e276d0a9fa5501258c2e758e2181`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cd606f6f489eb66f1307280aec321b3af3aa998dca447ae1cc91c6b884240064`  
		Last Modified: Tue, 03 Dec 2024 01:27:20 GMT  
		Size: 53.7 MB (53739147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35dd2ce389c2ba8241ab5a1413687a0b57613b16b38bac38a5c7ace5c96bf94`  
		Last Modified: Tue, 03 Dec 2024 03:20:10 GMT  
		Size: 144.5 MB (144536664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e535888fb75f9e22cec1310cd7ba03c139bf3f0f14f1b05264e61fccc15c29b`  
		Last Modified: Tue, 03 Dec 2024 03:20:09 GMT  
		Size: 69.2 MB (69159697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:598404607d023cd419afcbfe2a14d8d4710eb9919a0085c41738ed869e2968d4`  
		Last Modified: Tue, 03 Dec 2024 03:20:08 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537af8a2140187c10455b2bf6297678ed04153a5fd9fecfb3d57909ad09b50ca`  
		Last Modified: Tue, 03 Dec 2024 03:20:08 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:184c2f0019789827620dc4f5decf74524446cb68b116d6023ae7204f0968ba89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7229888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e2661e19fe75589c6b1b25570ca53a2a36cfa98ecaeec6a86c7aa524cbe260d`

```dockerfile
```

-	Layers:
	-	`sha256:55e4d2c6d14784f4bb8d29e5a425f83e599877b9a89a796526e665703546be79`  
		Last Modified: Tue, 03 Dec 2024 03:20:08 GMT  
		Size: 7.2 MB (7214067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c906b3c04a8be2bc5ccf9d9ea43a49a63815f94a0e8414a7ba02c3676232d10`  
		Last Modified: Tue, 03 Dec 2024 03:20:08 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c9e1c963453a3a50d940dddc6e5998eca7479dca97b9c8762486c4464629a8e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.9 MB (264893741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:543817e86f5f133cc9aca473e12dce6b44e03513e46d4938ec11e3570290714d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e357e1f94476a03fde298261e8c007d487d3cfade45a9eef064eba724a5c5e2e`  
		Last Modified: Tue, 03 Dec 2024 01:30:26 GMT  
		Size: 52.2 MB (52245994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912d1ea0cb763505ca8df8fc32c78297612e6917521b4419e34a15aea4a92e6b`  
		Last Modified: Tue, 03 Dec 2024 15:18:30 GMT  
		Size: 143.4 MB (143360959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3648a44f8907f695f2a7a55ccd78e78ee557ec55e8c4503ccd00e0e80d5572fc`  
		Last Modified: Tue, 03 Dec 2024 15:22:24 GMT  
		Size: 69.3 MB (69285751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d62eeca9d605a65cc8db007b2249917c7dd74a95cb782d2f3417bbbfedf905b`  
		Last Modified: Tue, 03 Dec 2024 15:22:21 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda6856938f2e8a29e8c0d4420b208eca4619da7d0d0e8abd35e1035e1fc7c8a`  
		Last Modified: Tue, 03 Dec 2024 15:22:21 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:f9b0e8296595fcd42dc0babe149dc87a3ecf08d576fe8cfb7f7dec3c7afb69b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7235108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51263b99ce99c9bbc28299511d54cccd36013e82afcd76403e5488a4b1ecdb76`

```dockerfile
```

-	Layers:
	-	`sha256:3a9d3593af45f02a13e63fdc0dab26abcb4df396c351af4c0308b4ed012d9dff`  
		Last Modified: Tue, 03 Dec 2024 15:22:22 GMT  
		Size: 7.2 MB (7219170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ecc8ed8c5b7456baa549f51f5da22a86677a2d86afa03f49f1374de2d45c2bd`  
		Last Modified: Tue, 03 Dec 2024 15:22:21 GMT  
		Size: 15.9 KB (15938 bytes)  
		MIME: application/vnd.in-toto+json
