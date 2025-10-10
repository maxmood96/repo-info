## `clojure:temurin-21-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:da36e735956d35f760871a1b3f7b6ea98ebe30c4901a954e173f33b149590b1f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; amd64

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
		Last Modified: Thu, 09 Oct 2025 22:29:38 GMT  
		Size: 157.8 MB (157804769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
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

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

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

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:307ac8cfb75d735db57c6df79972f4ed6dc942d804d5b2452dd7fc3925930613
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.1 MB (244115459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56c51b725d7a7eaf38fe21d97cb9477c8af3dc5d3edcb03686345323ed5027f4`
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
	-	`sha256:2f51c94d475d26f5f068b224e7f288b16ea055136de89cb9afd8e8f25a5c984a`  
		Last Modified: Thu, 02 Oct 2025 03:31:49 GMT  
		Size: 156.1 MB (156081188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74cc23cd4345035a0cf5e8a776f145f5c9945cbc29333ddfa13de4e97e244d4`  
		Last Modified: Thu, 02 Oct 2025 02:46:00 GMT  
		Size: 59.3 MB (59284802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4dfd08d6c1d5de03fed02607668821ea9339ff7b7ecb7243f06e4b1085842a6`  
		Last Modified: Thu, 02 Oct 2025 02:45:56 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5845025f884cc4d997c789b9256fce56e6cd135bc95186a3c7a063e2b6692f7e`  
		Last Modified: Thu, 02 Oct 2025 02:45:56 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ca81f05d114d4215e05689cb7176dfdad34406c43856a7d0a5fd37d8bba81bb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5332898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85871032d9049d9771d1b665d4e3d6a216135db4ac34e7d41558ad6f5922fd1e`

```dockerfile
```

-	Layers:
	-	`sha256:eb55226aaa002a17edf93edccab6cbcf0bb26fd297d2122377b669214e1d8ea6`  
		Last Modified: Thu, 02 Oct 2025 06:42:52 GMT  
		Size: 5.3 MB (5316901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e7fa545b26e998f1dc7fc94fc9856e9862a173b087fb09b7c0a9e87559fa0bb`  
		Last Modified: Thu, 02 Oct 2025 06:42:52 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json
