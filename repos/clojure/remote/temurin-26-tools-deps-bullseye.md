## `clojure:temurin-26-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:e992afc97e71e4fe6aa77dcd89015d6e0b6e1a038f4b637585bbcd12735b2bf9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-26-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:ec7350fa52b9c9eb9469d13b7852a6c434cb895a9d81434eb282ec09f3d4d85e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 MB (214809385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3e22f7a0d43c0125aaf5964b703f73bb081000ab9f40e49532d783f28b7d5a5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 01:22:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:22:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:22:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:22:11 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:22:11 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:22:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:22:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:22:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:22:23 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:22:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:af48a3e7696e07f88a02f9674e541901b65eadb5cf0f62e566b1d895099a1e9e`  
		Last Modified: Wed, 10 Jun 2026 23:40:09 GMT  
		Size: 53.8 MB (53771769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee71befeb627100f5379de2546e62a73a278ce486d7d50505879746dcd76b5c3`  
		Last Modified: Thu, 11 Jun 2026 01:22:44 GMT  
		Size: 94.5 MB (94524374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bf20b6ca233408b36acc9f04a8faf650b97abcf89017e4805b9cbdf5e97969e`  
		Last Modified: Thu, 11 Jun 2026 01:22:43 GMT  
		Size: 66.5 MB (66512202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbe34c58119aae1c3e7e4c8ee3e2c0ce91a96b69db9ac2ff9e472f98d4e9623`  
		Last Modified: Thu, 11 Jun 2026 01:22:40 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734e08158155608182509fbafca3e9d6903caf1e7132a1c4cf612d9ed2a1fb1b`  
		Last Modified: Thu, 11 Jun 2026 01:22:40 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:1a6273706095994eded05d10095ba7c8579a393c14cc3df52e93c89a1aad5a12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7386264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2131b8c67ee059af2284c65a8ad35a2192621d79a99185735eff028fbe798f4c`

```dockerfile
```

-	Layers:
	-	`sha256:189352bc43cdf6f996f7d10841454ce7f2cfc4a1983274e6934babe22659a870`  
		Last Modified: Thu, 11 Jun 2026 01:22:40 GMT  
		Size: 7.4 MB (7370340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48f061335622b089896639cd10851e404e660b0613f892556af9dff159c8b015`  
		Last Modified: Thu, 11 Jun 2026 01:22:40 GMT  
		Size: 15.9 KB (15924 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e3eeeedeaaa484e47b0abeccd0b571b2dfb339754baae65700b01f17abc6042f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.4 MB (212447356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdb82928a8d9563e89005a59fc8a82e1ce3324e6ce1aa069f5ec1440ed435473`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 01:26:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:26:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:26:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:26:14 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:26:15 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:26:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:26:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:26:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:26:29 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:26:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7c21e59e753cb91625909251110d6e4cc4a5411b4b7b37f74a62e56b927b7f1e`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 52.3 MB (52264114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ca91080a39e07e5e69ec02c5c44b270eab75aa807b3e1f0332680b6c48ceba`  
		Last Modified: Thu, 11 Jun 2026 01:26:52 GMT  
		Size: 93.5 MB (93504349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67117ab54966c7653ca75e657f7d1156dd76dff025b4565757d9c2aea69db41`  
		Last Modified: Thu, 11 Jun 2026 01:26:51 GMT  
		Size: 66.7 MB (66677855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c937a7f2b59388e5293c163106a08e90fed22113338c50354942378935a8c5d`  
		Last Modified: Thu, 11 Jun 2026 01:26:48 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48acb37415c10284155df90e1d508ec46b5d218eb3515a30aa27f45bfb3d077c`  
		Last Modified: Thu, 11 Jun 2026 01:26:48 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:faa1b056860e815aade127fdde7523a4da6578916bb245db95063529afb33978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7391479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e78094029c1e37758a60f9792046aaecfac4a6bffc6dae26fb7c68759c78f96`

```dockerfile
```

-	Layers:
	-	`sha256:a80d56862b4525b193b92cd09f6536c03a52ad564849edba6456918933fc45e1`  
		Last Modified: Thu, 11 Jun 2026 01:26:48 GMT  
		Size: 7.4 MB (7375436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be6c07ea32ca50581c3a691ef41b6abb6f04ca4346345fbff330846807e852fc`  
		Last Modified: Thu, 11 Jun 2026 01:26:48 GMT  
		Size: 16.0 KB (16043 bytes)  
		MIME: application/vnd.in-toto+json
