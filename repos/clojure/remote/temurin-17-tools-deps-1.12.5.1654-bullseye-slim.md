## `clojure:temurin-17-tools-deps-1.12.5.1654-bullseye-slim`

```console
$ docker pull clojure@sha256:2439b8a10c3a74e32bee6d231de600ee387d01afef8a19122ad3929d3ca0f9c4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.5.1654-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2b009101a3743bf3a0e7c26f1c80190c5e8da99a1c7fd26be2fa377cadfc1408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232264602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2b05df4d93699cc603d25865900fb1d1d1faff6aa94c65d2b5a69776c102ebf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1779062400'
# Thu, 04 Jun 2026 17:45:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:45:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:45:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:45:21 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:45:21 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:45:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:45:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:45:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:45:36 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:45:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8419f4a27c97b0c111ab0dc77e0159bd3abfadcb948d4a49cf6dd6670703b84e`  
		Last Modified: Tue, 19 May 2026 22:36:35 GMT  
		Size: 30.3 MB (30257598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7234bdc48fc734724702c75874b3caf163e1026a5feccc1a71a30fdea102aa87`  
		Last Modified: Thu, 04 Jun 2026 17:45:57 GMT  
		Size: 145.9 MB (145905490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df90b72f60636778dae52b72c91fac2126d20b5444a24708bca458901859ab1`  
		Last Modified: Thu, 04 Jun 2026 17:45:57 GMT  
		Size: 56.1 MB (56100471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91c6877ea4a5e0538052dbc0fe1e10016c735a386c901eb11d1e0ea7ed35ef6`  
		Last Modified: Thu, 04 Jun 2026 17:45:53 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5e14eae37762c070cc43e2ef6a03eee1ce42a535ca8bd7f3a8bd9b98e1b3fe`  
		Last Modified: Thu, 04 Jun 2026 17:45:53 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1654-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:77db0161b85dbfe99ca93e6cc20b7476af4e7c29b713cde99b41d3c65255e8a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5333835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b34fbdb0b4d6fdef59fcdd44bff0d00f08249f840e3f2448426c117750e3a72`

```dockerfile
```

-	Layers:
	-	`sha256:ebd803e366e2cc0f43c46d3be9d4fa52b7940d161e785d2d5c5f259efc5464d5`  
		Last Modified: Thu, 04 Jun 2026 17:45:53 GMT  
		Size: 5.3 MB (5317845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7466b2a6e06036f9863fdd160a8e4b605443b18bdd5ac4f3045770c3ccc217c`  
		Last Modified: Thu, 04 Jun 2026 17:45:53 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.5.1654-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8b7f1bbf3ed5001e271ba55a038f5dd774f39f31cff958bd19d6e835389da02e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.7 MB (229736097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46a69c3daa80eb5449d8eac4a2759f677d6a9e96c2f7081ae95b31e991af68ef`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1779062400'
# Thu, 04 Jun 2026 17:45:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:45:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:45:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:45:37 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:45:37 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:45:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:45:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:45:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:45:50 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:45:50 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2b99ba6638377be8e7e1e9a328ebb001513ab9f700c8168d404eed03437c7ce5`  
		Last Modified: Tue, 19 May 2026 22:36:47 GMT  
		Size: 28.7 MB (28742972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65687cf30483e04ca99b5c7ad827a0b1aa6ff74e50647599f2e7b8e5a70fcd53`  
		Last Modified: Thu, 04 Jun 2026 17:46:15 GMT  
		Size: 144.7 MB (144724335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19c1c24501af68035fdbc7481b94300307f561dd3814db6ebfca71292e03ddd`  
		Last Modified: Thu, 04 Jun 2026 17:46:13 GMT  
		Size: 56.3 MB (56267748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cca5284aa4942e2bee9e97e17a2dc579a62263bdb52ceea2d8b552c22ffcdc7`  
		Last Modified: Thu, 04 Jun 2026 17:46:11 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadd518e057e17d68eb8dae361e278ddcaf031d475d65ca906f51e6da1805337`  
		Last Modified: Thu, 04 Jun 2026 17:46:11 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1654-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0a662874eafa2337233b366fd38a055d3a20d2199d393f04ad43fe838c4a9bbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5339685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ee128659b282a7ecd26727d5b635aea2b2675e3aea6156220064b882cb0162`

```dockerfile
```

-	Layers:
	-	`sha256:e75e123361a3e62401ab435a02b063ced82cb6d63e9aa4f3fbadefd2abe25ea1`  
		Last Modified: Thu, 04 Jun 2026 17:46:11 GMT  
		Size: 5.3 MB (5323577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:300dd78cca04c5a7c82e1cd975761c1cb8fc1e394874ed376709339ba55cf7dc`  
		Last Modified: Thu, 04 Jun 2026 17:46:11 GMT  
		Size: 16.1 KB (16108 bytes)  
		MIME: application/vnd.in-toto+json
