## `clojure:temurin-17-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:a4ea34bfe2b96cb3be3a0e75e091ddad7f53e7cabe559c278dc78026e2ec7267
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:1345dd66b1bc2054c1d406c0a6f83da7ac641296c79cca98a42358094c18ddb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.2 MB (275175201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:313068e89e8397f88b3b4a80dbba88bd6e2f294348bbb1e8fb9daffcab58c298`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:0d5bdf84bbcdfa95d42190537e3cad2c0a5876f9127fae6a1d1c485d3539c77d in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:903681d87777d28dc56866a07a2774c3fd5bf65fd734b24c9d0ecd9a13c9f636`  
		Last Modified: Tue, 13 Aug 2024 00:23:26 GMT  
		Size: 49.6 MB (49554080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59502ede7907b20a2945ff72df066632d50b927a324555e2c9ab934f0aae8528`  
		Last Modified: Fri, 23 Aug 2024 20:02:22 GMT  
		Size: 145.2 MB (145166508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf526df8cdaecb65f65611e9dcde11d15ac27ca4121d3ea8597bf5711cecea79`  
		Last Modified: Fri, 23 Aug 2024 20:02:22 GMT  
		Size: 80.5 MB (80453570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c1194fa4a230a4b2c65496a4331e961cddea98123ca2ca13e547c09fff10df2`  
		Last Modified: Fri, 23 Aug 2024 20:02:19 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53dd6fc8e45d3938fe4dc6e46988d705b4c114eed8ac80ac074568a34e67b18`  
		Last Modified: Fri, 23 Aug 2024 20:02:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:fe7de90cb9f3982d6d0725350d871f5801a2976c388bad3989c8cfb25cbaa321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7015526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ef57893ac83166df8e5aec28ce10295271f9f5fdf796a237a2bc092fe70ab61`

```dockerfile
```

-	Layers:
	-	`sha256:ce299716c9b1e14c0f33681f98f05f980021a1843e507626c35d44fbf38d9be4`  
		Last Modified: Fri, 23 Aug 2024 20:02:20 GMT  
		Size: 7.0 MB (7000086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd323f18a8acc8240dc4cda93c93378df4fa2c21c3a00a09e3d6da5455e0f404`  
		Last Modified: Fri, 23 Aug 2024 20:02:20 GMT  
		Size: 15.4 KB (15440 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:91d47bfaa0f0a5fc919c976114e46e8a9a1948bd824f6befb6b78812aeaa687b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.7 MB (273747139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f018767933c2739b9f8b0b2cd151dfbbd0b191c1c46cec9265e72ef369b223ab`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:e81dd8b32e45ea6e761021a3e01b6efd339dd9248a2036dc4b51a2c1de560b4c in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7b24851aa36de07cd94173b8e2052846573dacc3b241620d713254e647352394`  
		Last Modified: Tue, 13 Aug 2024 00:42:24 GMT  
		Size: 49.6 MB (49588592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e30518595e909e33f4b333ed4f46e0a6bed2642d328f1ab72905e694f16d9876`  
		Last Modified: Sat, 17 Aug 2024 06:11:23 GMT  
		Size: 144.0 MB (143959503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:220261b1956251ae2442a71c098f9a023d967892e55772be7cfc1476d1e5646b`  
		Last Modified: Sat, 17 Aug 2024 06:16:42 GMT  
		Size: 80.2 MB (80198004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadff031a8540bcd4d6c7a22aab5e42379a2622977498a04f6200d6a95966593`  
		Last Modified: Sat, 17 Aug 2024 06:16:40 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5759d1c9ce50974aa4b67a54ee0ebf3395ab20d3505c0510d97ce28e2ab2aca`  
		Last Modified: Sat, 17 Aug 2024 06:16:40 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d1875279087438f024d0cfd5369c08b1e05792c096687958b721499dee689055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7022448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58656c24852a8b1508767033250b05c5e3896f2986a34f4e472d072011cb553f`

```dockerfile
```

-	Layers:
	-	`sha256:51db8ce3d6109667911421b1cc9bd98fba76b4bfa0eaef85a7c775c1b4fae26d`  
		Last Modified: Sat, 17 Aug 2024 06:16:40 GMT  
		Size: 7.0 MB (7006473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27a94ad94f20f0f7b8a1e03437d8c4e2fae40e12c87543998a00ecd1fd47be85`  
		Last Modified: Sat, 17 Aug 2024 06:16:40 GMT  
		Size: 16.0 KB (15975 bytes)  
		MIME: application/vnd.in-toto+json
