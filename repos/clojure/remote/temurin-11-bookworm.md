## `clojure:temurin-11-bookworm`

```console
$ docker pull clojure@sha256:f028b072e507b450080c835996b1e2b342e5750570004f5a3c9a6637876df1b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:b2c0a5be7060ff481c86b8c096af88271306b90cd2b7361f8f7d01fad6c1037d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.1 MB (275061335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c9b96b0c8b40a39ac1f082e7d0271bae5d60ae80fe2c490e444a9150e1a97bc`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 08 Mar 2025 19:45:48 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7cd785773db44407e20a679ce5439222e505475eed5b99f1910eb2cda51729ab`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.5 MB (48467838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbc22fc60a208c544c8c2050fdc98b14e3cb5767cbf3de9424efb8edc85d3ea`  
		Last Modified: Mon, 17 Mar 2025 23:17:06 GMT  
		Size: 145.6 MB (145598936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7fba707de595d2d9befd793cf10902a54f4b4b7324064a2d61e016027133f55`  
		Last Modified: Mon, 17 Mar 2025 23:17:06 GMT  
		Size: 81.0 MB (80993918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c652aed92b7c28097c547a2654d5fabb82a4909c2ba655b6442ef4dcdcbe1a`  
		Last Modified: Mon, 17 Mar 2025 23:17:04 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c5af60fcd0807497610b82bd46c27cb9aa412d9ca27a6fdf598df48270d243b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7205501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d80df42538ecf2900b77fd6841ad407c1c6c72847b6f9edce6e045ac124c4c17`

```dockerfile
```

-	Layers:
	-	`sha256:314f7652d9b638c7455876624db188b4bb0ac3c12e20985c21fb6c9b0272d6e6`  
		Last Modified: Mon, 17 Mar 2025 23:17:04 GMT  
		Size: 7.2 MB (7191249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddafb2de3044f534d23d96b86001584d3d0421b5eb169953e58ad75f385be1c6`  
		Last Modified: Mon, 17 Mar 2025 23:17:04 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b38f46d242ed1d14cd96ccc51f35d2aa0bb76f88f57e8b00690836674ce93125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.5 MB (271533420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f7d153fa23f8e3c11eb32af13ed53fb672d614ae1080624b98e7d06edb953c6`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 08 Mar 2025 19:45:48 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:545aa82ec479fb0ff3a196141d43d14e5ab1bd1098048223bfd21e505b70581f`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.3 MB (48304855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80416af1d3bf4ace7aa0e10ee519635ec3d15c0d12597a41d027eae7da592c3`  
		Last Modified: Tue, 18 Mar 2025 00:12:41 GMT  
		Size: 142.4 MB (142385459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d190f20538667c16df22cf1a15e2a15ca0f4edb204f331a726c276e6f8079e`  
		Last Modified: Tue, 18 Mar 2025 00:12:40 GMT  
		Size: 80.8 MB (80842460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f220c0a8b144efba18e222c53a5bbffdfde27fe53802600d4d6b6bf6abe57e3`  
		Last Modified: Tue, 18 Mar 2025 00:12:37 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:fb60ccd51a3a99552a59a94d4f4144ba6f65514032d7cf4389c325133f7a5f77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7211998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccfb03beb11cfbd7331a0a2bbbc5b1386d6e5ff386668f68c9ce84f804c05684`

```dockerfile
```

-	Layers:
	-	`sha256:1686dc0da175281623b6eddd0a7b4f46ad64270931984006ff284e2c1e6c4f18`  
		Last Modified: Tue, 18 Mar 2025 00:12:38 GMT  
		Size: 7.2 MB (7197630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55f69461567512742dae394fbdc0b31456795094f9a5bb81212b3e2c6901ec4e`  
		Last Modified: Tue, 18 Mar 2025 00:12:37 GMT  
		Size: 14.4 KB (14368 bytes)  
		MIME: application/vnd.in-toto+json
