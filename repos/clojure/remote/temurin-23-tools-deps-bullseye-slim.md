## `clojure:temurin-23-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:eb1c5262bd9df6c1e490a32db72ace8fe2807103a178777997e1d689cdaf51e6
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
$ docker pull clojure@sha256:731759b5b30bd45315f58170318a97a086f23186b5d3125ec72f13212720c008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.9 MB (250932982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12b0beb1ce3a398b5efd469032694282ac7db4537d6920d40408fec499726fc2`
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
	-	`sha256:e206b6fd86d16b339586be06a284d97aa652cd2602791ae8ae2346212f045696`  
		Last Modified: Tue, 14 Jan 2025 12:41:46 GMT  
		Size: 163.3 MB (163281785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6dd3db52a5eb193e40d2804bf5efd0f0f5917dbfdf358ad43fb05f226948137`  
		Last Modified: Tue, 14 Jan 2025 12:44:46 GMT  
		Size: 58.9 MB (58905242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd095e36253f4200eae061e4bf02168d7f3d145bc5f0b92a63271103a938770e`  
		Last Modified: Tue, 14 Jan 2025 12:44:44 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca357b42c840cafc1cff963374c6ea2e8745a8eec8abb735d0a24761973e3c29`  
		Last Modified: Tue, 14 Jan 2025 12:44:45 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:02fd003945ec473877e1a3ef8f5e17aae8e115193e83b650cbaebc509b7fc18e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5142381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea9236aaafc5ffe79e98ffa5aed5f9f821477d8e53053936b560afa7e3ec3130`

```dockerfile
```

-	Layers:
	-	`sha256:097dc8d212c6796264cda1a08a22c6f94bd72feed2def0972d97a1e6326663d9`  
		Last Modified: Tue, 14 Jan 2025 12:44:45 GMT  
		Size: 5.1 MB (5127185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d410d0c61190ef4e0f203ad4baa6b4d025cb7b4dd904d256ba10014b9d0f6698`  
		Last Modified: Tue, 14 Jan 2025 12:44:45 GMT  
		Size: 15.2 KB (15196 bytes)  
		MIME: application/vnd.in-toto+json
