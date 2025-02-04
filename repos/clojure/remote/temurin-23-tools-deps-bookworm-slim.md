## `clojure:temurin-23-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:642e8fb5c68fa14102fdd46bda2b801cde42b2225310c7483ad0ebc90cc7fe89
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:596ac137ae9e4a3ca7883b63ec2ac51da978079ad6ed05fad81a26b31793ea92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263060834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b360c23806622752d3ca81b914c8f7d754dff39a07c85db2144eb09315bd4576`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 29 Jan 2025 19:11:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e69294228b93e1a28d8b9e46e0468f871e758c87675b15aae8daebfa5c7b838`  
		Last Modified: Tue, 04 Feb 2025 05:21:41 GMT  
		Size: 165.3 MB (165316181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d68133ed83c99896361b7cb59b1031ee08b8acf5da141b5e160fedea472b44d`  
		Last Modified: Tue, 04 Feb 2025 05:21:40 GMT  
		Size: 69.5 MB (69531308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ee25962b24fb7a8681ec39f8b9839fb7b4fb6d833f0a3e22d1051cd27cbde5b`  
		Last Modified: Tue, 04 Feb 2025 05:21:38 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2405761311f0c53e949c5ef363a9d9e7f7314cb5d2a03c64bfbb269a940021fc`  
		Last Modified: Tue, 04 Feb 2025 05:21:38 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3d5f1a3b18d1a8954cec8e074d22927bfc093d71498dd523ca6d2d0498b126be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4933450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0b91870824a0af7a5ea9842541a68b172bc230315441c44ce350f83c2da922e`

```dockerfile
```

-	Layers:
	-	`sha256:68f4509162732b2376cc559101105fca1772e358f95820535a65a732f39c8ae8`  
		Last Modified: Tue, 04 Feb 2025 05:21:38 GMT  
		Size: 4.9 MB (4917572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13894b25704d99947e3fa48ddff4b2a45c1df2f621ee3acd1b0daa557f44404f`  
		Last Modified: Tue, 04 Feb 2025 05:21:38 GMT  
		Size: 15.9 KB (15878 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:80fb0c12f4834673368510bff2db70813e4eee0ed51cc7945b083fddd1595512
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.8 MB (260765509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c39fb0365c90b21decf64c4675b591daf63fc143464631f9c3d679ed10159290`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a656661714c1ebb064b5d1dcba3954ce2bcf4775c081e8d50a223977425e56`  
		Last Modified: Fri, 31 Jan 2025 05:29:49 GMT  
		Size: 163.3 MB (163341470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24959d09b0da41261d137216a6dc247275608da01bbd24034b5bffe048931b5b`  
		Last Modified: Fri, 31 Jan 2025 05:34:23 GMT  
		Size: 69.4 MB (69381966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596a18157b9604bed71e753098daf17089207b8d958e6de35115736c41698cc9`  
		Last Modified: Fri, 31 Jan 2025 05:34:21 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9101b803bcb24fccf448ca4872b1a16d04f7bd12da3d46babff416285417895`  
		Last Modified: Fri, 31 Jan 2025 05:34:21 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a4d18707cec3f980018c65ba3e09c09a90053b7f986acf64d2128639cd41fadc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4938708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7010b4ffeaa176c190d144fb64d743bf379d6c6cb103c3bde01dbfb4a862c58d`

```dockerfile
```

-	Layers:
	-	`sha256:ffd54e4381985e29e384f2e52f144a292f2776de3f0e7791ee396584b9118c9b`  
		Last Modified: Fri, 31 Jan 2025 05:34:21 GMT  
		Size: 4.9 MB (4922712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbe8091ae24e4a87ae4553c290199b989588150af7f45f471fe267e33f353d16`  
		Last Modified: Fri, 31 Jan 2025 05:34:21 GMT  
		Size: 16.0 KB (15996 bytes)  
		MIME: application/vnd.in-toto+json
