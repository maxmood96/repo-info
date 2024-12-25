## `clojure:temurin-21-tools-deps-1.12.0.1479-bookworm-slim`

```console
$ docker pull clojure@sha256:4489fbb258cbd52ed3b84815a9f9e5e93009a907d2d596254e947c11856cd1c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.0.1479-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:570cf91c920733028f3cf1a59b491f862d8b2343b4cd703476ee054218fa0b4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.1 MB (255094510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57e6a428a3791b3e70fa317e45f82ef3d99157ba47e0c610dc9e2f8357946e83`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
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
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:688fd16e9afddb6033aab9fa1a9a9052c33b294c202df5b2c80bcfd1abb85a7c`  
		Last Modified: Tue, 24 Dec 2024 22:38:31 GMT  
		Size: 157.6 MB (157568720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157593d36f039e662222aa39134ee088c1617ae2a65c0dc2247cf73ef6ee8912`  
		Last Modified: Tue, 24 Dec 2024 22:38:30 GMT  
		Size: 69.3 MB (69293171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fcc89434e8961e12026e467f0c2f0ca3a5e72f8080b1d8f03ad164adf563b59`  
		Last Modified: Tue, 24 Dec 2024 22:38:29 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44afbcc1a8d3147c25d0cd80b9022f4219ea6b3410fe79cd7ffbfa0068f7b6fe`  
		Last Modified: Tue, 24 Dec 2024 22:38:29 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fd347de41e5d06c293253c926be0d29391485afeb32da444173d5d9c57437003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4932880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1be64cdc9ed5e091e9bb322cca543d449a7aa446027b28f8c639581d96bb383b`

```dockerfile
```

-	Layers:
	-	`sha256:0b54d79517f30a7b6b260cde5704528126854286926f9808fe3756fa1d73d377`  
		Last Modified: Tue, 24 Dec 2024 22:38:29 GMT  
		Size: 4.9 MB (4916305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0749c3e7c1fea66ee2a624b456d35e3eb56df83cb1d36c73364bda4a08899ea`  
		Last Modified: Tue, 24 Dec 2024 22:38:29 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.0.1479-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:46dbfe38b01d8b4368a58aa947cc7e299c3eca9c90ff1df4750de34ec5d83f7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (252993730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3421c97b051f2797873dc31a4ac6b596beb7b3508f2548aa355f898177eec39d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
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
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11788338479823b777f7adacb2addcb65dc2a80dd644d7561877d39b5224b474`  
		Last Modified: Tue, 03 Dec 2024 15:25:04 GMT  
		Size: 155.8 MB (155793088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f414b3a529b9085d04ac429d6439e410acce19192fa235ade010718889018b05`  
		Last Modified: Tue, 03 Dec 2024 15:29:06 GMT  
		Size: 69.1 MB (69140792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d62f54cf2de67d5b750ca8d8b9eed267934bf05d6f5609ca566787a77564d3f`  
		Last Modified: Tue, 03 Dec 2024 15:29:04 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f3515e5344a3d0c414d1e0d93d8eb57f57e65f1f1bb7dc87a8e472a9bc8591d`  
		Last Modified: Tue, 03 Dec 2024 15:29:04 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:32cadbb516c528ab97c4de2c27a86dcc99a2233d0bde0ccbe4d72cc129a55632
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4945690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f5f73ef16e761a33ebe332c5fc9dc83a4ffedc8176215f2cfad5df92ddc57dc`

```dockerfile
```

-	Layers:
	-	`sha256:4825148d07285287b69ab0fc87d858c4b41df8250fe03fc249d6853cb412fcd7`  
		Last Modified: Tue, 03 Dec 2024 15:29:04 GMT  
		Size: 4.9 MB (4928973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bdb17d6af6b5e30b91068150a4705694351ad395f51b5553f08ca2fbb074640`  
		Last Modified: Tue, 03 Dec 2024 15:29:04 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json
