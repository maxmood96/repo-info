## `clojure:temurin-23-tools-deps-1.12.0.1479-bullseye`

```console
$ docker pull clojure@sha256:467d4397153d2f3686856e3ff18ed0c1c045d754f2d7b0ead6a5bb3f0c4fc915
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-1.12.0.1479-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:aeeab8d4e514a91ae4eda2de5f8ff5f3e39e41dedc79d9a6df18fe64b05cb1d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.7 MB (289683769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:253e2d94cc4aa399b279b2ca7024b8edfd251de2e15e7919229fbcb1404700f3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:42 GMT
ADD file:52a4b3d3a7281812594cb25cd6c6e83649d63a981e9f92f7c189ebe080249490 in / 
# Fri, 27 Sep 2024 04:29:43 GMT
CMD ["bash"]
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
	-	`sha256:014ac6453c34f79cc163f6567c184e5eb0b48cdc07ecbfb1388d90e95ac90b02`  
		Last Modified: Fri, 27 Sep 2024 04:33:28 GMT  
		Size: 55.1 MB (55081391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e1e36a3025c27a175d379fa6ff5bac5d82216f04655d74f83d6512808fadfdd`  
		Last Modified: Thu, 03 Oct 2024 19:00:55 GMT  
		Size: 165.3 MB (165267633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe84ba5e82f875c2500a489c9c6909792fd962ad89c1208887aba3d4337c5d0`  
		Last Modified: Thu, 03 Oct 2024 19:00:54 GMT  
		Size: 69.3 MB (69333704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc2ceecc6053a7decd8a554c0531199e80d7f5765fedd12aaf4dd2700d4a181b`  
		Last Modified: Thu, 03 Oct 2024 19:00:52 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a921ce06aa9a0b4fe982ed955f48e3915ce6571bfdae2e3ee32b50ec47ba402`  
		Last Modified: Thu, 03 Oct 2024 19:00:52 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1479-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:cf0517f1c6ffc4f9f7247737299ffa4f0cf60346ff4cf42f7a49c069e5357ca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7210441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ec4e50124000345974e7dd57a1b756b8e6f3cabb502a2a41c1fb797f252782b`

```dockerfile
```

-	Layers:
	-	`sha256:de01b403686aec2268d00cf917f3c3b98a27c34897fe590e50d90a2f8e6a25b9`  
		Last Modified: Thu, 03 Oct 2024 19:00:53 GMT  
		Size: 7.2 MB (7194996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c57ab8ec4917be4713fd739ece3a240b6cd92555b2c40b800a5066a65d02cfad`  
		Last Modified: Thu, 03 Oct 2024 19:00:52 GMT  
		Size: 15.4 KB (15445 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-1.12.0.1479-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2c233243f091822903e2b6b72d9418c9b6889137626674ff005b0bc8dcae7b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 MB (286454676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f131af915d98635b9c1ef0ee8e57c31e63a32b4f78acd9fdeeacbe1b377627`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:24 GMT
ADD file:20638e93d5a3e884b24b90ba3bef17ad5a4c795085c457bd5729f2f5caaf6a73 in / 
# Fri, 27 Sep 2024 04:38:25 GMT
CMD ["bash"]
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
	-	`sha256:374a548aba539daa8d37f8b0fe7326b582daa60fe22cc343a838af2e82a4ca1c`  
		Last Modified: Fri, 27 Sep 2024 04:41:08 GMT  
		Size: 53.7 MB (53733864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd21f2c0c517dbf21f8221774b130094c4842babef9809f4ca92c71e1a4db8e5`  
		Last Modified: Thu, 03 Oct 2024 19:03:12 GMT  
		Size: 163.3 MB (163252821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:826ee01166b70176ccbed5667f796ef6123cbcd5179c0e57739fd371a932bc8f`  
		Last Modified: Thu, 03 Oct 2024 19:08:41 GMT  
		Size: 69.5 MB (69466950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c4c3afc030c54157d42d4f052814123cf684de25502b4e85ee847d5c2057f6`  
		Last Modified: Thu, 03 Oct 2024 19:08:39 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404a40257d42ffe7beb4852aa03d0f7267db162376ba1d08f77fe130d468ff87`  
		Last Modified: Thu, 03 Oct 2024 19:08:39 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1479-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:7f7c8134643b5060d6879260db39753b661c9c8fb077fa8d589cfe255f454a5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7215028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:931827e32f982c010cf00a06130df97dd578d29a418ba18e486340638be22c0e`

```dockerfile
```

-	Layers:
	-	`sha256:84e8c30902231517492a1f27d5630d4d0b081be6ef5f7ab4e2f97fcd64856af4`  
		Last Modified: Thu, 03 Oct 2024 19:08:39 GMT  
		Size: 7.2 MB (7199477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2199b3fdb71a2965d89241c64285bbf2d12c5440ed25f3bd6234ed32ac78860b`  
		Last Modified: Thu, 03 Oct 2024 19:08:39 GMT  
		Size: 15.6 KB (15551 bytes)  
		MIME: application/vnd.in-toto+json
