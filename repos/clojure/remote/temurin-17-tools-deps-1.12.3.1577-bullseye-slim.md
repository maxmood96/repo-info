## `clojure:temurin-17-tools-deps-1.12.3.1577-bullseye-slim`

```console
$ docker pull clojure@sha256:54ef7b940dc859cfc3ff6ac627eb676f3c3f0f2fb859087ad51a1291a7232e73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.3.1577-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d0a4d662d02fee2cd5258b309193f14b156904f6c33e03530a7dca54cca7c9d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.1 MB (234104242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb68051d856281e3c8df886cff852e2ad7248419634ecba137b73d2d52defdd2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1759104000'
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
	-	`sha256:4eb1dd59a73886acc6a3cc9d4c8f8e66d1fd6ba6d6195b05ce21c22b0658aab8`  
		Last Modified: Mon, 29 Sep 2025 23:35:18 GMT  
		Size: 30.3 MB (30258363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1799611bbb511cdf63914ac5034962df40b7d12c02df4635d6eac27d11e827e8`  
		Last Modified: Thu, 09 Oct 2025 22:28:21 GMT  
		Size: 144.7 MB (144693293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4c1c15373a04e076a69748bdc30a984f7f9ff49f8cde82acc8af6b4a1cd91e`  
		Last Modified: Thu, 09 Oct 2025 22:28:31 GMT  
		Size: 59.2 MB (59151546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683ac72cc70ad7ecdaae69ecb7782d4d2f9cbe3ba43bccb79aaea169048c76eb`  
		Last Modified: Thu, 09 Oct 2025 22:28:27 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a78f3324febea30b27a0fbbc7561801de03f03b477f200c485b94565f9876c7`  
		Last Modified: Thu, 09 Oct 2025 22:28:26 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b9df1a006a7a7ae5ffb422c67ad35e4560d8a9581b567743379c7fca0336dc46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5325570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ffdf65cd8ab0ef0be13828c96aabee76d9ce079a1cf6e9b6448f4d9a7f9bac`

```dockerfile
```

-	Layers:
	-	`sha256:79d6c84eebd7fc8b1fd1601f4bf77000fae779bacebcb3135df786f69e657dc9`  
		Last Modified: Fri, 10 Oct 2025 06:40:07 GMT  
		Size: 5.3 MB (5309691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b638cbd86aa38e86172e2f32b42c87ea243468740a67f59f338b90391d5a5fcf`  
		Last Modified: Fri, 10 Oct 2025 06:40:08 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.3.1577-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:18bbe6ae5c404102a5b667f4753aa54a6ea1da57a7287bdff5739a385d013f2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231579301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a41abe32ece3e7b4d304f754947b0c345c3792c4c977a6a8385d83ddf9ab44d8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1759104000'
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
	-	`sha256:93b0b88e50eb7468103e583a7be2e8ee3fe5f86e6c74df4baca40a3685b5eee1`  
		Last Modified: Mon, 29 Sep 2025 23:34:34 GMT  
		Size: 28.7 MB (28748427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27694ea96739972ea9ff21bc4c8f69b73ed324803303ba44d597ddf956d23e3e`  
		Last Modified: Thu, 09 Oct 2025 22:28:39 GMT  
		Size: 143.5 MB (143542139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e7b84dcfcda24ba24896793a821cde40f6ec7a08f2e24ccd6cbdc1ba108e56`  
		Last Modified: Fri, 10 Oct 2025 03:52:06 GMT  
		Size: 59.3 MB (59287690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d072f47639f0c3322eaddbc17bcb29142ab29e89ce88e6c545e66e3c24cbde34`  
		Last Modified: Thu, 09 Oct 2025 23:11:50 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fec05b89b25e9c15286e76f05b177932259f62c7590802b11e46e4eea78081a`  
		Last Modified: Thu, 09 Oct 2025 23:11:51 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:32a622319bdf8bb3dbc94cea9d831f2fa8ccc65d89bd9885ef6506a19e9b70a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5331420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53f3eb14bbb6edc841e29b9497b25e83558c4353902b3012c3fb76d6877517a9`

```dockerfile
```

-	Layers:
	-	`sha256:befc015651bf52a036b7deac72908693c5c413a84fd769dba3ae066646030632`  
		Last Modified: Fri, 10 Oct 2025 06:40:13 GMT  
		Size: 5.3 MB (5315423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d661bd9ad43617e196591b0b21e2fc5374e137ea04eb595532b0ce583d51f4af`  
		Last Modified: Fri, 10 Oct 2025 06:40:13 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json
