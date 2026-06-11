## `clojure:temurin-25-tools-deps-1.12.5.1654-bullseye-slim`

```console
$ docker pull clojure@sha256:ad8f227c5410fc89e8d620c1a102af9cbf760201db83a13e44c623aade529930
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-tools-deps-1.12.5.1654-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d6d946d9953e42325aa63127caef02d2dbb9f7372ce2d195a5703ab5cac7f1dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.9 MB (178936217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ca0d08cf1e67c325c0b411cf60da8e5d9dc05eb9098a5df987ff48eee2ead29`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 01:21:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:21:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:21:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:21:09 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:21:09 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:21:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:21:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:21:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:21:22 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:21:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:55534d9909ecd18467599b415fa2553c3106849154ae8a361a75f1a24f2a4364`  
		Last Modified: Wed, 10 Jun 2026 23:40:12 GMT  
		Size: 30.3 MB (30260255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08e70a297c43d1da0761ce3e19ee85b385d7377c9d5839861437a0c5686e552`  
		Last Modified: Thu, 11 Jun 2026 01:21:43 GMT  
		Size: 92.6 MB (92574588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5638ff197a3cbd1211fb1f240767e1f9a000d91cf64d43f3c7f370bb16bd1f82`  
		Last Modified: Thu, 11 Jun 2026 01:21:42 GMT  
		Size: 56.1 MB (56100333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3a56dd1dbf78486185a5660d9016c9a8724585e6408776f4eef22b0364bee5`  
		Last Modified: Thu, 11 Jun 2026 01:21:39 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e223c65d267061f7b9c2a46b9ed3978cc035cf4a45ace3d7d4b9d4a452397a`  
		Last Modified: Thu, 11 Jun 2026 01:21:39 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.5.1654-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0f2da76e75042162262d9e41f02c57d6938a6244240820cc97f8bb45892fbc13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5302618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:776c87e8cbc190931df1958bad12e3e07d96943106737d0c2c38a3d9ffc1bc7b`

```dockerfile
```

-	Layers:
	-	`sha256:4c593265149b822e80a2dce0d3372ec03592b6d3641dec8116bdabe632e1efed`  
		Last Modified: Thu, 11 Jun 2026 01:21:40 GMT  
		Size: 5.3 MB (5285939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eac38505562409778b975836b2a6300146eba7980d58aad2882736719e5bb317`  
		Last Modified: Thu, 11 Jun 2026 01:21:39 GMT  
		Size: 16.7 KB (16679 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.5.1654-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c80a2350f43c64e7521ec28e9e9064ff7b5a60b53f79ba566835ecc21387b864
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.6 MB (176556697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4805c8cb8815e6465d0834d589d8c9d3b9d9dd8deed3e32f601fdd4ea743037`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 01:25:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:25:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:25:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:25:23 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:25:23 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:25:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:25:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:25:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:25:36 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:25:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ca483a18241c226a06a4a4afd22dc5496062254c671fa595136458fb8fcd0107`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 28.7 MB (28746154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d36cccb6274139a4fa539db7ec46ec7e715f0d7d993f8676ec16f52a6dfb542`  
		Last Modified: Thu, 11 Jun 2026 01:25:57 GMT  
		Size: 91.5 MB (91542254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe56aca85302378e5e3715f0fcc70cefa6cf383e0e7e0d3736eaae78665cee42`  
		Last Modified: Thu, 11 Jun 2026 01:25:56 GMT  
		Size: 56.3 MB (56267250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b053eb92e4a0ba77764bb01d204af8d6919154818adf41f4269dbb8d3a2ef5fa`  
		Last Modified: Thu, 11 Jun 2026 01:25:54 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0645ac8f5feade78c2371bf1ce69007b7c77d07bdfd81860fa02977ab69bfb4`  
		Last Modified: Thu, 11 Jun 2026 01:25:54 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.5.1654-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c4411509c7e7c771781bf2c4e212fd3c0980b1fb6437d6a74f39e2675d3a8202
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5308513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:917bd4c7bd68eff1b29cc6e05aa10abbb828afe039dcad6847956e0642216ec6`

```dockerfile
```

-	Layers:
	-	`sha256:d5f2c1dc492a5d9d7148ae571daca2b025a44fab2595ae9f5f4bdb791510fa61`  
		Last Modified: Thu, 11 Jun 2026 01:25:54 GMT  
		Size: 5.3 MB (5291692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d3914a113cf2df1dbd460bb957265c44baa3fb22c0d92d28a7da9457180975b`  
		Last Modified: Thu, 11 Jun 2026 01:25:53 GMT  
		Size: 16.8 KB (16821 bytes)  
		MIME: application/vnd.in-toto+json
