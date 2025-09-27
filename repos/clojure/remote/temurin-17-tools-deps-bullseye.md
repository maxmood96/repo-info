## `clojure:temurin-17-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:536e37622e6b8b2de4c2858a2ad330c2afa5c04f425f01d9a465244e34b00d9e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:d9de26b121b23dbacfff5e2d3327f3345ade899e207062edbb5f76f53017af07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.0 MB (268011153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73fd03870995d838176a9cd7a67a5cdd6fc861b897de94894d93f62ee9417fc5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:035115815e46101f9c9956e02e706f2f3ec8748e2b415f0d232b51eb76a6a779`  
		Last Modified: Mon, 08 Sep 2025 21:12:56 GMT  
		Size: 53.8 MB (53755396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b553c1643aeb5da02a3dca521305c384e7db2e09e50b4fe663cd0721fa4b225`  
		Last Modified: Sat, 27 Sep 2025 01:19:56 GMT  
		Size: 144.7 MB (144693605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640e529b09029e42ff5dd826aa2f5f7de49bd0b26a554d73c1eb9e5b19f9eab8`  
		Last Modified: Sat, 27 Sep 2025 01:19:53 GMT  
		Size: 69.6 MB (69561110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87a011a432a86916ca891a84e6fd5737709e1b02c3c7e4f8c53fa8afaa6e610`  
		Last Modified: Fri, 26 Sep 2025 18:45:46 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd5bc77d83bd573f3db657c4718fca790b068f909992cf9b2e9bb8809cb8aec`  
		Last Modified: Fri, 26 Sep 2025 18:45:48 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:b69ff256b09aa6a6b49f1699289225b64dda1953556dcc9e9d2e2dedfdb2efa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7411488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd2e22d61d6b159799327ae9382ae6d88de2dd9c17709a49d3a96d745f1c1f5b`

```dockerfile
```

-	Layers:
	-	`sha256:25a7dd0f3ca5962ef73e6c4333b9306a151ed8f26a8b8282ed3526c4b16bcff4`  
		Last Modified: Fri, 26 Sep 2025 18:38:48 GMT  
		Size: 7.4 MB (7395667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d60f9fee8e88e97f65f21341e8ed8a685c3fa29d55af049f3dfcf023fe9614dd`  
		Last Modified: Fri, 26 Sep 2025 18:38:49 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dedebb8ec3e08b5cc67b24d448be7092184c0a217cd42c370a0321a8474696f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.5 MB (265479910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad08126c175c919ddc0b9a9e5c1acff015054856a84c1ef231bdfcbd9157ab65`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7df02cb4a974a4e8a9eb65ffcff7274f9dca341d29aaa763294c42e49805ca19`  
		Last Modified: Mon, 08 Sep 2025 21:15:41 GMT  
		Size: 52.2 MB (52248370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11020012e5e5e092b18b0bf0b1d607e0c297d75a6a4578c94c6362e72e42a6a5`  
		Last Modified: Fri, 26 Sep 2025 17:54:44 GMT  
		Size: 143.5 MB (143542108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c91ed4ecaa0ee9d521a532c97eb40d0231ff270b7436d62f01428233d87993`  
		Last Modified: Fri, 26 Sep 2025 17:55:06 GMT  
		Size: 69.7 MB (69688391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:989d099b5b2eb5a0a329b50f7d64f527133f816a881d84e2cfb79e10292519e2`  
		Last Modified: Fri, 26 Sep 2025 17:55:00 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5a191ab10d08c11a1cfd4b87fff712fb9608f0eddac238127ae04f7aa473ab`  
		Last Modified: Fri, 26 Sep 2025 17:55:00 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3328098da12156c4631c69e1a2211d8a0dbb9a981d9038af259c8d677362f365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7416705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ced900446868ba4525543f78d969c3aa85c316d886889d80d562a7dec4c197b4`

```dockerfile
```

-	Layers:
	-	`sha256:e4f0ebe3d5c372f8dd96afe2cc623313be5c391b874f1c686841bdcbce84b6c8`  
		Last Modified: Fri, 26 Sep 2025 18:38:56 GMT  
		Size: 7.4 MB (7400766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7066a5d91eea244132722f94d8e1be76aecd939c98a157134b0ee90151acb2b4`  
		Last Modified: Fri, 26 Sep 2025 18:38:57 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json
