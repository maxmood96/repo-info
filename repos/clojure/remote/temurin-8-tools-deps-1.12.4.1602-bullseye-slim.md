## `clojure:temurin-8-tools-deps-1.12.4.1602-bullseye-slim`

```console
$ docker pull clojure@sha256:fa4e9e2ad4e248ddf04130677f0359bff9915fcc4196fae4eb6b06303e000345
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.4.1602-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:907e5fc9ba2108964f10570246a2cb4f359095f400c7dce9f39b19b1f9f81686
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144129357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ca960ef54099a05414b074c1d71e7b0d4ae805f798c3ed8f7e07f1d793819d4`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Wed, 28 Jan 2026 18:03:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:03:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:03:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:03:07 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:03:07 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:03:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:03:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:03:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:bd1b97a95a10ded4767bfcdbb3d042b961d107d141121fdbb255239f0ca115f4`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 30.3 MB (30258497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f2dbacac8c4d29536cec97b0d5dadf994603d1d413082df7b31b9ee07f49ff`  
		Last Modified: Wed, 28 Jan 2026 18:03:37 GMT  
		Size: 54.7 MB (54733390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62029a24e17873ceb7d55b034dad5b0b93a4718bf8c02f1334298fa3ebf8c683`  
		Last Modified: Wed, 28 Jan 2026 18:03:36 GMT  
		Size: 59.1 MB (59136826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6b4d1dbe0fdfa78e66223a310d53f73d1147c8848ba818bc6c4de77cde59377`  
		Last Modified: Wed, 28 Jan 2026 18:03:34 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1602-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8519f0ec164c5ef420207ce04eab0b64d1884c8786af498e3868a31a67caa61b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840714a456ec7891e1aaa777db52e505d5aec131042f800bb97c9a7bd8aecf0d`

```dockerfile
```

-	Layers:
	-	`sha256:92b3f2171212836479c18c56a0d39c43ad86b8c9625bdd26c95b4db2e1d39b83`  
		Last Modified: Wed, 28 Jan 2026 18:03:34 GMT  
		Size: 5.4 MB (5430476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af7a8e9730d20574b3fd3579df8b1ee3d9be7c35b75ae0e13a43e2e855d091d5`  
		Last Modified: Wed, 28 Jan 2026 18:03:34 GMT  
		Size: 14.2 KB (14247 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1602-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:20d85cb537ccba404a8651a1284e0a7c49f4e10c67a317f91dd10b5dd1dde5c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141852134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19e5c537164a04c5a7fc39a876db579f5999e633b5a2531a069b0ab64a1c2398`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Wed, 28 Jan 2026 18:01:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:01:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:01:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:01:54 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:01:54 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:02:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:02:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:02:08 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7781088accb552d6473ed64f4649a64684d928b7cfad973d13e5c50942bf7a5b`  
		Last Modified: Tue, 13 Jan 2026 00:41:51 GMT  
		Size: 28.7 MB (28748518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec247465e3008126f52fdfac6083e17ba56b820e1d0f7e0c89c645f79531c94`  
		Last Modified: Wed, 28 Jan 2026 18:02:26 GMT  
		Size: 53.8 MB (53815008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64c2a8b30607c2928efadeae7a05e5e91b901a0bab24668cba35707080b2df7`  
		Last Modified: Wed, 28 Jan 2026 18:02:26 GMT  
		Size: 59.3 MB (59287963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b261ea8798eb8437a825f683a37aa0892dd76e42101442208856e997761ce2ab`  
		Last Modified: Wed, 28 Jan 2026 18:02:23 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1602-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0d238b173872ab7852f436c9a6d43cd8a2a1e064a30748d062240f32c2816e92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5451272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:955f5486072747daaf254e5cb5600f29a72f6ebea5d0111a7919360f34d77b47`

```dockerfile
```

-	Layers:
	-	`sha256:be3f4c502cc7e74ac184ec81712ec95ddf9765e05b441984fca1eba28a966b9a`  
		Last Modified: Wed, 28 Jan 2026 18:02:23 GMT  
		Size: 5.4 MB (5436906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bb093aa6e1ec44f9d5e8cd651c05af2c481131408dad9faa95dd9c0be52718d`  
		Last Modified: Wed, 28 Jan 2026 18:02:23 GMT  
		Size: 14.4 KB (14366 bytes)  
		MIME: application/vnd.in-toto+json
