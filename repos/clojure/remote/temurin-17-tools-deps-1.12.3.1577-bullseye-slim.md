## `clojure:temurin-17-tools-deps-1.12.3.1577-bullseye-slim`

```console
$ docker pull clojure@sha256:811bfbd70a0a2e26aab496044a2bde95e2ae53cb50eccffb230f2752a4fba794
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.3.1577-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5aaeb7bbff73369fc1444082a75336ab4a6739e285dfa1eb6d4b6961beb02785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234259817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b915a22e4825f8665cf466f6beff329a229b2e0995461f969f0c46593b5680b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Fri, 14 Nov 2025 00:53:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:53:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:53:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:53:14 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:53:14 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:53:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:53:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:53:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:53:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:53:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cf5f39ef3fca9730ed04aee5f10040ea152a9793dec0d626f4205eeac5ec3fc0`  
		Last Modified: Tue, 04 Nov 2025 00:13:10 GMT  
		Size: 30.3 MB (30258596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b22d4e48c3dc9e273c1e582fa2f5bad5c0d9ed873b938074d2ac0e7caa482d8`  
		Last Modified: Fri, 14 Nov 2025 00:53:48 GMT  
		Size: 144.8 MB (144847948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02651c46be36352c33d88e655ea2b67a92c2c2f83b982c1dc94142f80635e691`  
		Last Modified: Fri, 14 Nov 2025 01:29:48 GMT  
		Size: 59.2 MB (59152229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0243e7c58b9adccaa366fb7026eec509e234a6b24e316bb10c76950d6ef07b08`  
		Last Modified: Fri, 14 Nov 2025 01:29:42 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63288063e70f2dfce34bfa699e3411c5ae533a425e2af89f4400c088b1ef1777`  
		Last Modified: Fri, 14 Nov 2025 01:29:42 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cf770e428798bb7a1905834eeb6d046879e7450c36eecc4a0037f8f141b16994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5323905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c679840e62a5acd71ab72e5e5f4099ee11991585d25e8fa3cd623266a9f2b27`

```dockerfile
```

-	Layers:
	-	`sha256:26420c272fd5c6f4e99c44a0c2e86bf8952943927481245c9b4c8b718980ff23`  
		Last Modified: Fri, 14 Nov 2025 01:39:06 GMT  
		Size: 5.3 MB (5308069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bfe470aefcd1f95d25a066091131b456d6cab9b5bdf9068b89500e2f05e0593`  
		Last Modified: Fri, 14 Nov 2025 01:39:07 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.3.1577-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2f2b790fbcbcff4f6edaf740406eb8eb01d6ca4a7fb991744513affdaaf34278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.7 MB (231717147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24399ec5c256b41283c24bdf034ee42890e5df2feb99a910c26594539d22fc54`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Fri, 14 Nov 2025 00:54:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:54:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:54:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:54:53 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:54:53 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:55:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:55:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:55:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:55:07 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:55:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:241077dc995c26590e89ca59e622bf97509f2613a9e84e3e745225e4259eb511`  
		Last Modified: Tue, 04 Nov 2025 00:13:03 GMT  
		Size: 28.7 MB (28748552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce749164759a8a2a8e21aca9c14b71b669f5305cf09e2953e8600034e5c170a`  
		Last Modified: Fri, 14 Nov 2025 00:55:30 GMT  
		Size: 143.7 MB (143679910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264e47aba9978545667eb51e40478997e02ebf3fa55e51689b191384a150c7e4`  
		Last Modified: Fri, 14 Nov 2025 00:55:40 GMT  
		Size: 59.3 MB (59287642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f15895e5bd6fcd6d65a336eb9f344362f9f060449273ede115b29916bc4ab3`  
		Last Modified: Fri, 14 Nov 2025 00:55:34 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:371f1b3a8b46b126786ecf9b23755f92a21879fbf58329f1e820ef774f9f26f9`  
		Last Modified: Fri, 14 Nov 2025 00:55:34 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5d4319786e6eb6940cf30133205811b1e2f6facfde1f25376ba3ec67fb664e20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5329755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:092a63860ee736680ae8d78d2d7519e75a80b623003e6cff98b3fd4dc2cd9648`

```dockerfile
```

-	Layers:
	-	`sha256:5cd88170a72474c8b5f4919d39f2288177bf807fbc73e386a22271bbd97aa52d`  
		Last Modified: Fri, 14 Nov 2025 01:39:12 GMT  
		Size: 5.3 MB (5313801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b57b54910cd998ba8c4872b1be5fa3a4760bf33babb7d734f30b779717c6f5b`  
		Last Modified: Fri, 14 Nov 2025 01:39:13 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json
