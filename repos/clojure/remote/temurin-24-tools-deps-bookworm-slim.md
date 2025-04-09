## `clojure:temurin-24-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:9c6db5a372a7a192c01d681b70f2079f444d02e4b41fd6053ec05f80fda39b30
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c8df81dd4865831f8d7ea71203d6f54aad6666c734bf83e0a9014a4f86d51543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187705754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83a5fedb483a748ad400b6f143f0900a4538c9eb7cf0ee5852603d1554e892e3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fc9975e7fad3704a55fdf6228e858326023062a058bb7a21c728ea0a2963ce`  
		Last Modified: Wed, 09 Apr 2025 02:19:34 GMT  
		Size: 89.9 MB (89949048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59f9cfc8574e19c854e35cd4ed1dd5b251ffbad6403fb502c2a4a7c6f96d3cb`  
		Last Modified: Wed, 09 Apr 2025 02:19:34 GMT  
		Size: 69.5 MB (69528408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d275276ea4a71de1e63bd564ad6224bc3b8b66555fe6ed53cd95b46634ddbde`  
		Last Modified: Wed, 09 Apr 2025 02:19:31 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2c7dc6b18248ea62414881195358023ad48e6740d295a3441cdb33ef12c022`  
		Last Modified: Wed, 09 Apr 2025 02:19:31 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:78fc938b5eae3b26323c27e5ba73b32b5cc62e3d289770ffe513289f23d90272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4880469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a57c1aaa9a62faa0a89de749ef57cf86dc930aeeb3ec01056ce74452cc58b6e`

```dockerfile
```

-	Layers:
	-	`sha256:abcd8792187cae0796e9d148432b608b358f095866651b5b1e94e5a2775513df`  
		Last Modified: Wed, 09 Apr 2025 02:19:32 GMT  
		Size: 4.9 MB (4864597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf8bff64013ff04ed64c702d64aabb9c88ef1426638e9bc36031ad995c434d0e`  
		Last Modified: Wed, 09 Apr 2025 02:19:31 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1746579362301d6f9fd3a718ffed0fc2a1fc0e4c802fc6c9631e93ff7759ac6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.5 MB (186537680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c6058778af6f0709e18fc9d7782512dd49e35cf549f816f3f13840703a4a0dc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6e889996bf89b2f34eaa11526c26b2694b9cb20d1a4dfa0c7b5d26a120d225`  
		Last Modified: Wed, 09 Apr 2025 17:48:36 GMT  
		Size: 89.1 MB (89092721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a239a147fba202562e22ad1a5abafc30e90da19e162c1b19d573342d41f5886a`  
		Last Modified: Wed, 09 Apr 2025 17:52:43 GMT  
		Size: 69.4 MB (69377600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e069320e5d80a46977662985392ebc19b19e24325576c3cc81548a803caea86c`  
		Last Modified: Wed, 09 Apr 2025 17:52:40 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df981b6241b710b6afbbba99c92491440078827e021aaeaa18278571e3ee8468`  
		Last Modified: Wed, 09 Apr 2025 17:52:40 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c4dcb19aa9cdd1e796a0c6a807682c80754f314df84257a2b55d248c5ea7f3be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4886344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac61db8ecd0a8492245c9aecece365ad2505daf52ee8ff6b8f71c8eea3cc96b7`

```dockerfile
```

-	Layers:
	-	`sha256:b92535fc6f3995f253106923746bc59f5f83648a4c51e3e5a903a88598a3ba33`  
		Last Modified: Wed, 09 Apr 2025 17:52:41 GMT  
		Size: 4.9 MB (4870355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ef52464ebdefbb4736e1c2b71fc4e6d4bc1c8367cd549a4d9b864e075869a43`  
		Last Modified: Wed, 09 Apr 2025 17:52:40 GMT  
		Size: 16.0 KB (15989 bytes)  
		MIME: application/vnd.in-toto+json
