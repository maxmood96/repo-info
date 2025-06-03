## `clojure:temurin-8-trixie-slim`

```console
$ docker pull clojure@sha256:a983718d0740c0db4d0c62d103101877327a6ce646694dad59c57fd451368c58
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:fc5d7f46281d1cbb3da58da808ac90bb77a8e1ad56befd643804aa1235cdfb8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.1 MB (159146804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633a3bfe4f0d34223d7203d90fec6c07d023a33758faf482eca62ebab69adde5`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ced038dea045df288fe9bdbe03117ca66fe2a071217e196ac86ed07f965fe688`  
		Last Modified: Tue, 03 Jun 2025 13:30:48 GMT  
		Size: 29.8 MB (29755384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991ba0099e31d5876895014c5273307078ddd690c1f52f2f98d8b9b4dec0e74e`  
		Last Modified: Tue, 03 Jun 2025 05:15:32 GMT  
		Size: 54.7 MB (54716190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e310ffd6bafb010f5814136676dd9347e1776e0a65857c501d155427cfb284b3`  
		Last Modified: Tue, 03 Jun 2025 05:15:33 GMT  
		Size: 74.7 MB (74674586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0200f6663565b580ac2a7f173d82323696aaed2c83153d11459d445122db63e`  
		Last Modified: Tue, 03 Jun 2025 05:15:31 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f3eafb555883e9e915a9b38e379d4f1fe45ded6195c88bd4efd66653a9c5289b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5247946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8383b647c56708e5ee25c07a9d2c2e9344cb0e915653cd227cf0a5bbed8b390e`

```dockerfile
```

-	Layers:
	-	`sha256:1f3ab794ab6256f1fd6f0595d91a8f2733cddeebe7a67a7e1a61f7286879a841`  
		Last Modified: Tue, 03 Jun 2025 05:15:31 GMT  
		Size: 5.2 MB (5233675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be5d58786adddafe94c29b42cb8d1149c7e2bd27fda8107937a2343b163b99eb`  
		Last Modified: Tue, 03 Jun 2025 05:15:31 GMT  
		Size: 14.3 KB (14271 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e06961cd30de0a541a760d7a9d84a4144cd6193667821ef41f74bee81e67e476
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.9 MB (158909488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09f33cad1dcd950e5ada03e96b4dee4fed45f2e2034dc595fc010b3ecc4492dc`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6098c2c9fa277c00ab580ce12bf64a9e1edf9e9139ba18ad85f3cc3063834aa6`  
		Last Modified: Tue, 03 Jun 2025 13:33:56 GMT  
		Size: 30.1 MB (30119455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3027bac347196f3028d06f80221ee420e9ad855e5c00339bbfa0557a9ae2305a`  
		Last Modified: Tue, 03 Jun 2025 10:33:22 GMT  
		Size: 53.8 MB (53830502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c76a72242be4a76c1789b77a1622cdbfedf7785f060c487cdf217cacd544bad`  
		Last Modified: Tue, 03 Jun 2025 10:39:19 GMT  
		Size: 75.0 MB (74958888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34b6bd585dee99ccfb701a2eba8e49fa20d644d0df2903e283f087b93c1d8b3`  
		Last Modified: Tue, 03 Jun 2025 10:39:17 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9484d718be70caba786de3a220756cfdbd81f21991b6c1098289c213488a5594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5254531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a27ad16a0478636b12b8420802e8b91d543e79f45ba7d88dde2240b36bc30303`

```dockerfile
```

-	Layers:
	-	`sha256:7583eb415c6e4ba2ff990053f1b01cdeaf627af9d801abf8df1dee5bf6a94f04`  
		Last Modified: Tue, 03 Jun 2025 10:39:17 GMT  
		Size: 5.2 MB (5240142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74308e6263171c4fba41de8c67b81eea8148bbaa06af3075c9e810941dafc787`  
		Last Modified: Tue, 03 Jun 2025 10:39:17 GMT  
		Size: 14.4 KB (14389 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:0f6e6589172dac386e24d197bf496fe8a6ab325f5aa0a5589b2fd65ddc9f6540
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.2 MB (166163156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ac854fa356aaa3ce98565b871a186bb6a8ead407ec2bb01d528e2a9d8622038`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:62eecea9deba6eaccef3e829ddec51f2c540dbbb668a68816c8ce3c4b8023d93`  
		Last Modified: Tue, 03 Jun 2025 14:07:09 GMT  
		Size: 33.6 MB (33580565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed347681401881a3761af3b137e387f41b112bad5ebb9315d39c8eed38c8394`  
		Last Modified: Tue, 03 Jun 2025 08:12:54 GMT  
		Size: 52.2 MB (52167965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af1ad1e28160224cf3b196b585a1021251ebdfd35b397dd361bffa2f6289522`  
		Last Modified: Tue, 03 Jun 2025 08:23:14 GMT  
		Size: 80.4 MB (80413983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86692ff2a74311ede0fc6b099b06f40ef1660c2cb75e7286e36d48c236f5382d`  
		Last Modified: Tue, 03 Jun 2025 08:23:11 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:856d0a17903cde4e7d087ede06a493ba10961e3e5a9f7d4a3038d53a2bf8f0ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5252958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc020e75be0bea1e33c0b627cb38673c11229340ba8a33681ae1ac3c732506a`

```dockerfile
```

-	Layers:
	-	`sha256:e5e19daa8989eecfb7b2db162675592cb1cf9ce2c9993a63d540a075ffd6b8c3`  
		Last Modified: Tue, 03 Jun 2025 08:23:11 GMT  
		Size: 5.2 MB (5238639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3c6f3a833d4365862e1d76c0a8f33ce42e53ecfb90de86eee812242d0a9421e`  
		Last Modified: Tue, 03 Jun 2025 08:23:11 GMT  
		Size: 14.3 KB (14319 bytes)  
		MIME: application/vnd.in-toto+json
