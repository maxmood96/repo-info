## `clojure:temurin-21-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:10d5ca3afb8865a36a7df35e252b1cf09aa645064de9060b8890764e51d7fa7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e0f590b5de43d37dbd9641b7d4bade785ea530a4f7effbeb99c7ca5af4aa8f3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.3 MB (247299688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83e28fff01b223811e6aed13452c6ae1f883cb3fd1079ef5e7db5d6f7b960aa`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Wed, 04 Mar 2026 17:50:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:50:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:50:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:50:58 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:50:58 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:51:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:51:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:51:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 17:51:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 17:51:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:34f0642d22440b5813561cd4375937013bfb556bec8ff3b0e208699b786282a7`  
		Last Modified: Tue, 24 Feb 2026 18:43:06 GMT  
		Size: 30.3 MB (30258379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3e0fc3d24cb674b388995bfa55641eb48bcb1c3262a3c6ca232340fb8b7ac4`  
		Last Modified: Wed, 04 Mar 2026 17:51:33 GMT  
		Size: 157.9 MB (157857099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361730aea5a99fa093630b3e79b6ddfbdf8cfa1a327ff2add4f80527ea14290d`  
		Last Modified: Wed, 04 Mar 2026 17:51:32 GMT  
		Size: 59.2 MB (59183166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4345e906deaca787024626a2b4261ffb71931d136edf115379e252abd1e52d98`  
		Last Modified: Wed, 04 Mar 2026 17:51:29 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51074d4f086917cd5f894d51833cad081855dd3f980ca98f8abef3601564faad`  
		Last Modified: Wed, 04 Mar 2026 17:51:29 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0db9c4f27508e2da4966028c49ee3b0717ea3adc2506f20292434f7bddd77838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5339364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d9e8da632f4d7a5a5cb4d4c96807d9c17ccbcbba3a2cf0e1751b70c21bca9bb`

```dockerfile
```

-	Layers:
	-	`sha256:7149506cbae7dd8c80ac237b08324314ee12fcf5ef78f3f13f2b5f91c38f00d8`  
		Last Modified: Wed, 04 Mar 2026 17:51:29 GMT  
		Size: 5.3 MB (5323529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c75109f7fa3da3845e8c7b68a3cdc74450bf9c09ba666973a286a942931755d0`  
		Last Modified: Wed, 04 Mar 2026 17:51:29 GMT  
		Size: 15.8 KB (15835 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:20c07cbc757d908779877ba56852c0e4f4e086b25fdd213666767aa3cb5ce86c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244202061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898b2d8b2c3fdd1be54a00b4a6174078bdaebe23e73f2666a2124ed115f72a81`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Wed, 04 Mar 2026 17:50:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:50:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:50:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:50:33 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:50:33 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:50:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:50:47 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:50:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 17:50:47 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 17:50:47 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:018c0693c4a2532e5636d6115333db6d882da8f33f1f40cb3e88dbe62da21aac`  
		Last Modified: Tue, 24 Feb 2026 18:42:36 GMT  
		Size: 28.7 MB (28744470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8faf2cf0ad02dca936f72dd5b1362e41dbec1d1f5d17263df585f937c6fcae0`  
		Last Modified: Wed, 04 Mar 2026 17:51:14 GMT  
		Size: 156.1 MB (156133064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03311b55c280068b9167ef1d73a957adb863021b274a96ae294677b29aa475cf`  
		Last Modified: Wed, 04 Mar 2026 17:51:10 GMT  
		Size: 59.3 MB (59323485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f5eaac083c579cd9bceb51ac97971a80db62c559be508e91e74121f59a3ded`  
		Last Modified: Wed, 04 Mar 2026 17:51:05 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6f6fec9a5d6e523d3fcfc5f93717943563caa7b7967d0e1d547fa504db1d23`  
		Last Modified: Wed, 04 Mar 2026 17:51:05 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7b5c5772a3a6668439fa731180cb2f73450b7cdf171071d4aeec23716bba3c38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5345214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d3c42377230bebc818250f44f8c1e92101a5c9b2b80e0049c37f042274306d9`

```dockerfile
```

-	Layers:
	-	`sha256:1a10aa5f330b64e8f434c3d9de0f26e548195ac081a142e2a5109290f354a6ec`  
		Last Modified: Wed, 04 Mar 2026 17:51:06 GMT  
		Size: 5.3 MB (5329261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8513e892c9991778acbad9ae2ed564826efbc147a175d4bf82addfd85f1e404`  
		Last Modified: Wed, 04 Mar 2026 17:51:05 GMT  
		Size: 16.0 KB (15953 bytes)  
		MIME: application/vnd.in-toto+json
