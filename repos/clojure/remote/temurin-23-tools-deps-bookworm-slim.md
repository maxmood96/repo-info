## `clojure:temurin-23-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:db20e6219458fac045335e914ce544d7648bdb61fced029a4ea0c01f8e9ee58c
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
		Last Modified: Tue, 04 Feb 2025 04:27:59 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e69294228b93e1a28d8b9e46e0468f871e758c87675b15aae8daebfa5c7b838`  
		Last Modified: Wed, 05 Feb 2025 10:54:22 GMT  
		Size: 165.3 MB (165316181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d68133ed83c99896361b7cb59b1031ee08b8acf5da141b5e160fedea472b44d`  
		Last Modified: Wed, 05 Feb 2025 17:56:26 GMT  
		Size: 69.5 MB (69531308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ee25962b24fb7a8681ec39f8b9839fb7b4fb6d833f0a3e22d1051cd27cbde5b`  
		Last Modified: Wed, 05 Feb 2025 17:56:23 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2405761311f0c53e949c5ef363a9d9e7f7314cb5d2a03c64bfbb269a940021fc`  
		Last Modified: Wed, 05 Feb 2025 17:56:24 GMT  
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
$ docker pull clojure@sha256:ee10f41c15752c67f8e11841c2d3b6a331136c914a6e8e9c3eef701b97914f2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.8 MB (260765023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a3b98966e46010f24999bb3ac9dd24f19fa09c1454cc40144c52cdb3b66390`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 29 Jan 2025 19:11:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 04:29:51 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d3d2b1c1dfa2977b74e155013c02da80d2fb8bfea30462dc1a42ab04348739`  
		Last Modified: Fri, 07 Feb 2025 06:56:04 GMT  
		Size: 163.3 MB (163341435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a331eabbf7d57e6e8ba9410cd9838e5e0e48008b699bec745294aec254bb3ba`  
		Last Modified: Mon, 17 Feb 2025 12:36:11 GMT  
		Size: 69.4 MB (69381671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66bafa8da29f0da109ec3d5e09b1f34ac300ce4152f6f2ba8c708783ddf8ac0a`  
		Last Modified: Fri, 07 Feb 2025 06:55:56 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0691d54d707293b15f626f7b2560c38b57d7e49b37c1b6f65f3eca0c51258e9d`  
		Last Modified: Fri, 07 Feb 2025 06:55:58 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b487bf12606aaf8e536cffa24ee8ceabff71bba4c4f3542c842ddb86c97f5ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4938708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28c0ebdc54ab13cb051dac23990942cd05e45314690c023b74982bf88d690de`

```dockerfile
```

-	Layers:
	-	`sha256:6cd5ff6022c0e93b59587d0ca8bcae7c332bd5cfeb61e422d7bcd60a07b945eb`  
		Last Modified: Wed, 05 Feb 2025 00:05:17 GMT  
		Size: 4.9 MB (4922712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbf494a770bf1908336321b255d0c00f295bfa63f940d8d472f8d9f72b05386f`  
		Last Modified: Wed, 05 Feb 2025 00:05:16 GMT  
		Size: 16.0 KB (15996 bytes)  
		MIME: application/vnd.in-toto+json
