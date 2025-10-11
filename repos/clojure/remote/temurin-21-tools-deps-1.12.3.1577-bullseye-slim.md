## `clojure:temurin-21-tools-deps-1.12.3.1577-bullseye-slim`

```console
$ docker pull clojure@sha256:fb4d6896b5a138429336ae2713d93ba19edf9a519705e76291763693e9659c42
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.3.1577-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5374f990594ab833c2514528b854efc7146a49ea81760ba3bae71214852a907b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 MB (247216144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c16f2398424f910a43fc341c16b421afd256aeaf0516b127021875ae9fc38e`
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
	-	`sha256:c1fb4d33ba11ed5a72bda3a51c78d99b9d54438514e5f5b210b664f865cd6303`  
		Last Modified: Fri, 10 Oct 2025 06:27:45 GMT  
		Size: 157.8 MB (157804769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe77b763f602afa586056564b784cff101a0bc478ddb46f3c4d58929f34715b`  
		Last Modified: Thu, 09 Oct 2025 22:30:10 GMT  
		Size: 59.2 MB (59151970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46353e26bffc5c79fcef4995619c2137d1b6f306e70091f08dfaaea358c758a5`  
		Last Modified: Thu, 09 Oct 2025 22:30:02 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2e2b435a38da9496678ee2aeaa548603940474c0004339de0bb55d509e4426`  
		Last Modified: Thu, 09 Oct 2025 22:30:02 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.3.1577-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6a21fa4e83b1e4a93c2b2aa850e0543851f6fbdf006ca5917e36d381e7880193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5328672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdf2fbd499765eee53c31f8d4615c81679b693b8a7c6898c3933417170b39284`

```dockerfile
```

-	Layers:
	-	`sha256:e7b3df4a81c2fefaceb8dd718761cc02d1b7eee8bd7f4fa86da73be445858bb5`  
		Last Modified: Fri, 10 Oct 2025 03:36:23 GMT  
		Size: 5.3 MB (5312793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:893ab6072b7508656c978dec88e61843a60fab1c54a339cc515acc3026354fa6`  
		Last Modified: Fri, 10 Oct 2025 03:36:24 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.3.1577-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e3d92de6c53bc12c3e6489c55f87cc9cceccfd1be06a60f53c86dd3850a503c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.1 MB (244118381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b06696f4f93686b30ddab74f2cff53395e1ea27be4edb51858545113065e434`
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
	-	`sha256:71d37cd390cfaa75311409d5fbc90594f2deb2286c0307821b993a6a5b5027fd`  
		Last Modified: Thu, 09 Oct 2025 22:29:47 GMT  
		Size: 156.1 MB (156081276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59522622483538362035034ce5f996f9428d0f6b824f9c351115a460fa4cbc22`  
		Last Modified: Thu, 09 Oct 2025 22:30:14 GMT  
		Size: 59.3 MB (59287635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5467be2533f417bb2e10d67abe363c9d8b2d598ae9d2e39f15cad3c49268e74`  
		Last Modified: Thu, 09 Oct 2025 22:30:04 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207ebc10bb04a63bedc9239f468706937e3617ed334b9eaa6ae2d75b1505f89a`  
		Last Modified: Thu, 09 Oct 2025 22:30:05 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.3.1577-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ba70ca8994a1bd8a0106d898dd8993c893384dea47214bd31123e16f7b6fa01e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5334522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd8b06e7e5de3851873e4253e352d7f3af10c690f40f2914962ace977badd6e`

```dockerfile
```

-	Layers:
	-	`sha256:7c318d755f7758507360178ab15ebd60f95b450dcd88cc7d2c692517499490f3`  
		Last Modified: Fri, 10 Oct 2025 06:43:51 GMT  
		Size: 5.3 MB (5318525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76b3b5a7dea7dda27f3f24ba35d5348b10958903ab1b1f4244fb65b3b339a667`  
		Last Modified: Fri, 10 Oct 2025 06:43:53 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json
