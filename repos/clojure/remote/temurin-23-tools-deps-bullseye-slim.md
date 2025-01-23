## `clojure:temurin-23-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:cba21bbf966a024c4a0c3917859e6aceefd56f6a24ef6a3ed95c67b6e010bd60
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b306acaaaefbf5dca34d28cab901e2f0c8bfa06ebc0d8ab743ac4ac03f37e9fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.3 MB (254329942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84fba41d875d4777bfdf78d7341db8dbbf38d714d1fd9695bd6ee29af4e33280`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff21fa8ccfe6026e6aa108953a25786e7972c70f120ed7a9148d81e259dc42ed`  
		Last Modified: Wed, 22 Jan 2025 19:42:45 GMT  
		Size: 165.3 MB (165295122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3950b9641474e7d7cd58f3e96d618e5dfa29a8f4e42a6706352d0e4c1be3ec6f`  
		Last Modified: Wed, 22 Jan 2025 19:42:44 GMT  
		Size: 58.8 MB (58781118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57fa3b6cb88e57353e6e2f292ed90bc60ba5ac2340f7e165e0e432d8e9ddd445`  
		Last Modified: Wed, 22 Jan 2025 19:42:43 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750de468d4c76e59d0ea613c384639058af743b5922ffcb6f7d0e76fd9c343e3`  
		Last Modified: Wed, 22 Jan 2025 19:42:42 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cc68a19ec190b06002fe9e6364c703665e0ec27e7ee82b066da6d9bd3789f4db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2637116a9a9526c78c0b41355f0c28f9e9a573094387f835b7764bb1ce81841e`

```dockerfile
```

-	Layers:
	-	`sha256:b4d57f057726d0495dba528a00e8419f6d2b14bee2d18554dba1b7c493f0e239`  
		Last Modified: Wed, 22 Jan 2025 19:42:42 GMT  
		Size: 5.1 MB (5122074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de734eb5b19bd21fab699c1e9b06d5f17ae16019a21f0fb2303c957349f302b0`  
		Last Modified: Wed, 22 Jan 2025 19:42:42 GMT  
		Size: 15.9 KB (15878 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:05c534de3f3d82b687601e612641bced6a912e04676c57764725e4205a1536eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.9 MB (250932986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c76d48ef095e872640247a32f998c199cbb37aa4b69549b36fd19767537809b6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e71e71a7a2f1c4317d95aab1ef47ce698a25d97fba226c509a728d57301d5e`  
		Last Modified: Thu, 23 Jan 2025 03:56:48 GMT  
		Size: 163.3 MB (163281804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c08e31f89d500d47bb053cee8c6c2b2ab4b383b477ec143ba884ce7ebf7893`  
		Last Modified: Thu, 23 Jan 2025 04:01:10 GMT  
		Size: 58.9 MB (58905228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682e35be2ffefa04c43f53151c6c30d5025ed18c24425abd89a8d42fdb4a6603`  
		Last Modified: Thu, 23 Jan 2025 04:01:07 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade8232c0cc1bd2051573bea268048b37b694c5f019b796a5003317014c93c4e`  
		Last Modified: Thu, 23 Jan 2025 04:01:07 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f22830db6deabd7272966b370147a95704a120b0fb4d9e8d2cabf7d91fd7cdb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5143179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88adea27528e187065c705a5302519073c092dbd90f8d88b16cfa67f16e676d5`

```dockerfile
```

-	Layers:
	-	`sha256:561ea29bfb3324e9ab5b121e5970cc779db97a4caf2332a33f9066e4930874d3`  
		Last Modified: Thu, 23 Jan 2025 04:01:07 GMT  
		Size: 5.1 MB (5127185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eecfed546e0dcf31b9483854127e962b373e3deaafb8d50bab6adccc1b909042`  
		Last Modified: Thu, 23 Jan 2025 04:01:07 GMT  
		Size: 16.0 KB (15994 bytes)  
		MIME: application/vnd.in-toto+json
