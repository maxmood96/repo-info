## `clojure:temurin-8-trixie-slim`

```console
$ docker pull clojure@sha256:b15fa20a749d7c9cc45fd2d63463a866d93442b34f3d9182e3e377949ae6f92b
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
		Last Modified: Wed, 21 May 2025 22:27:59 GMT  
		Size: 29.8 MB (29755384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991ba0099e31d5876895014c5273307078ddd690c1f52f2f98d8b9b4dec0e74e`  
		Last Modified: Tue, 03 Jun 2025 05:15:32 GMT  
		Size: 54.7 MB (54716190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
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
$ docker pull clojure@sha256:66537f8d28917f8697ff6922f700aa1147dd755bd4dfe37d59fbfa85dd755713
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.6 MB (155597474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:357aeef673958af23148ae69d576ab602653647a91c39f5f3821b51b93560b72`
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
		Last Modified: Wed, 21 May 2025 22:31:23 GMT  
		Size: 30.1 MB (30119455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1510a979eec55c1e74fba48e30c2b829ae1501a30aad31695a963a03b2325099`  
		Last Modified: Thu, 22 May 2025 08:04:19 GMT  
		Size: 53.8 MB (53830516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b108efd64759945348dde0a61d29aa58a8f285a75be707939c80cd30dc9cdb41`  
		Last Modified: Thu, 22 May 2025 08:08:39 GMT  
		Size: 71.6 MB (71646858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddd86793f441a5c77e3d6b64b28025c94c03e15f429622c856e8955a64a0137`  
		Last Modified: Thu, 22 May 2025 08:08:36 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9520a46cf63cbc80d5ca207dc477d619af7d103c9b7dd8c7d786c4f7820e1d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5254531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da5297617056bdb884a4510d0ae034a39b8d9e19b596d699243ea8aef5e7bc4`

```dockerfile
```

-	Layers:
	-	`sha256:731fbe8ec0ae5acb3fc9b4c30de28cc4103546d508acf02a66dd06b7145fde0b`  
		Last Modified: Thu, 22 May 2025 08:08:37 GMT  
		Size: 5.2 MB (5240142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59a585b5e769a46913197ae41591bb38da742fcf99cc4be28c931b78e3525271`  
		Last Modified: Thu, 22 May 2025 08:08:36 GMT  
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
		Last Modified: Wed, 21 May 2025 22:32:27 GMT  
		Size: 33.6 MB (33580565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed347681401881a3761af3b137e387f41b112bad5ebb9315d39c8eed38c8394`  
		Last Modified: Tue, 03 Jun 2025 08:12:54 GMT  
		Size: 52.2 MB (52167965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
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
