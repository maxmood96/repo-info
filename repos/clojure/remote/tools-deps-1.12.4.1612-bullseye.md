## `clojure:tools-deps-1.12.4.1612-bullseye`

```console
$ docker pull clojure@sha256:b6137f50167c28ded2c19eab8b89893ddf4c9b3a96e3bcc781d27795428a9b4c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-1.12.4.1612-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:ba4de0bb0b1b62d00526be02326a2ce00d2cd91dae7e4ecb7133251a574054b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.6 MB (215601221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a6283933764bfa745dff023d07bb005add64a15abea46058974dfc87589af9e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Wed, 04 Mar 2026 17:51:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:51:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:51:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:51:33 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:51:33 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:51:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:51:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:51:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 17:51:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 17:51:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fd834ead99fe4ea0884686321217c38494a7a0c7327e2a5ed98d978011de7ddb`  
		Last Modified: Tue, 24 Feb 2026 18:43:07 GMT  
		Size: 53.8 MB (53756434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4b013b16a1cbf86e46b06c10aedf3accb9a4834e9fa03b1ce73687b6a5cf65`  
		Last Modified: Wed, 04 Mar 2026 17:52:05 GMT  
		Size: 92.3 MB (92256290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca14ad0b1961e2c870dd42e9faf49dba6915a246779c981dce588a70fea68672`  
		Last Modified: Wed, 04 Mar 2026 17:52:05 GMT  
		Size: 69.6 MB (69587453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e76b978bcd699211dbd202cb3b8dad96a3675927d62c4bd539b17c6344a1bed`  
		Last Modified: Wed, 04 Mar 2026 17:52:02 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:546b6c27f8c2618ca3ea4cdc3a68ec98e1bfb41ec260248162029f4ea70d2b7e`  
		Last Modified: Wed, 04 Mar 2026 17:52:02 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1612-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:bf3c9cfc3fa06c26a87db4b7a36963c23ac1b551c68bb7bb2ad986ceb97660f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7393798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:716a227d21bab308483810b55f287e4129aec1df9b219aaa5b4251da785d0954`

```dockerfile
```

-	Layers:
	-	`sha256:9b0358514806719d83685ac67224d9dce2fb80f471fc777263e94db07258ada9`  
		Last Modified: Wed, 04 Mar 2026 17:52:03 GMT  
		Size: 7.4 MB (7377351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:980741ef9fbe57b0c1613902ea568e287f69d2135d435d6170abc6e515797e6d`  
		Last Modified: Wed, 04 Mar 2026 17:52:02 GMT  
		Size: 16.4 KB (16447 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1612-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bbf8bf28e23042d16a1eb6f5f0e0c75b000e1932163050181d3a877c6ace7357
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.3 MB (213276197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7596bcc124320e8d72ba504c64b86b13c83591f0e9def93546d4a827c96d96d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Wed, 04 Mar 2026 17:51:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:51:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:51:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:51:13 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:51:13 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:51:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:51:27 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:51:27 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 17:51:27 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 17:51:27 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0509053f2cf8072309184287dd2fd397e589dc5db17a1ddc469001be80ea07a3`  
		Last Modified: Tue, 24 Feb 2026 18:42:38 GMT  
		Size: 52.3 MB (52258392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae5a044982d3cb04ca80bf57d3b4d638b8e33a85141c4a279e2df40caeeb777`  
		Last Modified: Wed, 04 Mar 2026 17:51:50 GMT  
		Size: 91.3 MB (91288274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88021c15b03091a55aaeb88f98d640989b8bb1002c5eed9ecb428553c3fb1fc`  
		Last Modified: Wed, 04 Mar 2026 17:51:49 GMT  
		Size: 69.7 MB (69728490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ca72cc56414f3c3f8f3a230ef90d7c15335d0e2ecdbe2cacdafdc9cd617fd5`  
		Last Modified: Wed, 04 Mar 2026 17:51:46 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32b33b6548c5cd8392f0f9bc94d6c6a9d4558b35f123558281c02a75b4177b4`  
		Last Modified: Wed, 04 Mar 2026 17:51:46 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1612-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:eb8264b54fcc3b1444b7845f19af3994d0fd12fc753f774a42e7dc6a7ef11199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7399060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90db2f5293c72d0e04a7e8093bd3a083559074550584077e8fad621ed2a011f`

```dockerfile
```

-	Layers:
	-	`sha256:7cd478a7c11181f80384efe5ce9d7835530b13a036a2ef232c207383430f65f6`  
		Last Modified: Wed, 04 Mar 2026 17:51:46 GMT  
		Size: 7.4 MB (7382471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4633c1b5f176ffc071482f6be4da16a0afc9705d0e98d0d7f1d209dfe5a0f88`  
		Last Modified: Wed, 04 Mar 2026 17:51:45 GMT  
		Size: 16.6 KB (16589 bytes)  
		MIME: application/vnd.in-toto+json
