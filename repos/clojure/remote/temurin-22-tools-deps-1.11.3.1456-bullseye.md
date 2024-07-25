## `clojure:temurin-22-tools-deps-1.11.3.1456-bullseye`

```console
$ docker pull clojure@sha256:4b40585a69997cf36bd19d962825cf7fa1c45c4c4b514b9eadd3913a0feaeffb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-tools-deps-1.11.3.1456-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:88d607aacb1ecf02c250414e587a08251282a87da5e724466fd478f00fdac8c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.6 MB (280588283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8475de3b8410b525a2989ee9bede33657b30d9afd023747c7a374e927954aa0c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 20 Jul 2024 21:06:39 GMT
ADD file:61c91b2a02e0d3deb2364da03241d137acf78345623ae188082e574b043032a0 in / 
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["bash"]
# Sat, 20 Jul 2024 21:06:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 20 Jul 2024 21:06:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Jul 2024 21:06:39 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Sat, 20 Jul 2024 21:06:39 GMT
WORKDIR /tmp
# Sat, 20 Jul 2024 21:06:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:73226dab8db5240a2ddbdbe2fb1f0949a911563a62a3d5de3c8669ae708e88de`  
		Last Modified: Tue, 23 Jul 2024 05:28:11 GMT  
		Size: 55.1 MB (55084578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a5ba0901fdbddc420a57764dbabb8a07076ee216cb712c54cc3f00770a6391`  
		Last Modified: Thu, 25 Jul 2024 19:05:44 GMT  
		Size: 156.5 MB (156481615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b3c5d9125495ad21f85297db2dc2768b52671075fe6141f767dce7d290c9d4`  
		Last Modified: Thu, 25 Jul 2024 19:05:42 GMT  
		Size: 69.0 MB (69021050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f9d375e5fd3c04c0bb176190e9d1ab4bd7d2cbaf49cb2ee10c57a40327a674`  
		Last Modified: Thu, 25 Jul 2024 19:05:39 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da5ebe86fd83b346037e0df7bb31e2e9267bef9a2d8e55f25bdb0f4cd30808ad`  
		Last Modified: Thu, 25 Jul 2024 19:05:39 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-1.11.3.1456-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:6639c42c3c47ef9f8e26bd25cc1dded01fb3c50dd85b5620b4f0f98a4ab57d0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7055777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c0c8de4c9d5f9a0f5c0e2d63e15174e66318a9833c83fc0ce43aefdddcad047`

```dockerfile
```

-	Layers:
	-	`sha256:cf4b9fda2d03564154af6bdddd11b628550780972cee32653d0f437970325c2b`  
		Last Modified: Thu, 25 Jul 2024 19:05:40 GMT  
		Size: 7.0 MB (7040338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97de08addd5cbfce2fc8334c0bce2e9468f6198d082bf5a6c26989b6e32d3f31`  
		Last Modified: Thu, 25 Jul 2024 19:05:39 GMT  
		Size: 15.4 KB (15439 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-tools-deps-1.11.3.1456-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:018f731424238865ebe9d59a44f176e8cc5d972f3f20ad8c517cd9bfafb46490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.4 MB (277368806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a16721be274ef5de3832d8e22632b207b0c29025144122036719ab3ca9de4a1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 20 Jul 2024 21:06:39 GMT
ADD file:bbd5c67ed8e7916601bc20e4ce4973720e715d9dcd892ccbd64c1d5de711a38d in / 
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["bash"]
# Sat, 20 Jul 2024 21:06:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 20 Jul 2024 21:06:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Jul 2024 21:06:39 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Sat, 20 Jul 2024 21:06:39 GMT
WORKDIR /tmp
# Sat, 20 Jul 2024 21:06:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2c9750102c61ce3f4a11c8776dfc892d41a6d4a662d2882e471664dbad58487e`  
		Last Modified: Tue, 23 Jul 2024 04:20:44 GMT  
		Size: 53.7 MB (53729987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693f82ae39f775fa139a01037b01ebaa7596fecb3701f4ee212e1ee4aa7aaf1f`  
		Last Modified: Wed, 24 Jul 2024 11:38:10 GMT  
		Size: 154.5 MB (154503703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb7d8b5f91ab5c706c23d3c8f6ca9457f93617b087b20ca97c5558c823bb0228`  
		Last Modified: Wed, 24 Jul 2024 11:42:29 GMT  
		Size: 69.1 MB (69134074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eec1c79c3782a1660964bfbbe0a0ee9321c5e40b263fefe5aea9304e734946f`  
		Last Modified: Wed, 24 Jul 2024 11:42:27 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13359d2dfa5f8221283422f3c9dfab60383aaf4ad5509cd6c4a6635bf752e140`  
		Last Modified: Wed, 24 Jul 2024 11:42:26 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-1.11.3.1456-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:880d5280bb598ed42ae6c2797e3f4be713ad620f6f5248e4dd680e472a17c499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7061205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41de0d0f30db0d652452b21cf41d78dfc31c07cbe9f7b2d40b42bf59754a3b0b`

```dockerfile
```

-	Layers:
	-	`sha256:562519381f360b598088dda09789218572259ab163aac4d1c941bc44256554c4`  
		Last Modified: Wed, 24 Jul 2024 11:42:27 GMT  
		Size: 7.0 MB (7046060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:219ec39e8af8f5a852bc746737e152c81fa48c1dcb08eb850cfcda61c6dbb023`  
		Last Modified: Wed, 24 Jul 2024 11:42:27 GMT  
		Size: 15.1 KB (15145 bytes)  
		MIME: application/vnd.in-toto+json
