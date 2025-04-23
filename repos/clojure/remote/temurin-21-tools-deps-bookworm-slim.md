## `clojure:temurin-21-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:b1c285dd9a880fc31795f7a0ca607da0fb781c5c56eda11ba5704e4dd10cf54c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:64b59aaa0b0c1e3c20690bb251e663cae8fe8cf6e30d145086cbf6f338e4d58e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.7 MB (257692710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3d802c45da07e5dc449dd5bb0b01746809ae3a523f3ab8d13bc42167a7a498`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d37952808e934ebc2faf946963dfa9c04b37eb5359a12198ad520cf34dfec659`  
		Last Modified: Wed, 23 Apr 2025 17:16:29 GMT  
		Size: 157.6 MB (157634501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132c02f0a4f56efbc5ac9d4b6cee769f47e211a9bcd0d6b2a9143c7874104532`  
		Last Modified: Wed, 23 Apr 2025 17:16:28 GMT  
		Size: 71.8 MB (71829909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b094d7a180397d3091a7d2ecf41a83a45861b6d3f37b02b0fe4eb374626145ef`  
		Last Modified: Wed, 23 Apr 2025 17:16:27 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c61300fcc618985cf5121efaa2c3343f3d0769339ddfb755117ac545111390`  
		Last Modified: Wed, 23 Apr 2025 17:16:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:81305c68ea8946010c7f201edb7ab12cd60119d518e0d863a280b64d526a4afa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4934338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d112cd7615e2b4c9fa8950985e0c9d37e28d18474acbcfd286ac8319ceb0ed35`

```dockerfile
```

-	Layers:
	-	`sha256:d8ea3e10d631f41fb6dc8670037c2501f380daf0a6f15c5d83a9a6cc04e4a60d`  
		Last Modified: Wed, 23 Apr 2025 17:16:27 GMT  
		Size: 4.9 MB (4917763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43d29839a98187c596c357e5c4dbaed228ff385f8bab7aa91c8e315a8d08fee7`  
		Last Modified: Wed, 23 Apr 2025 17:16:27 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:afb368dbdf59cd8971344086b315e1a1cacce69d439363181ec125648f1fafc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.6 MB (255645530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76926d6de9fc88250427958b863b92a143660edd1b85cb056657ead95d06ddee`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311c425f48e589712e3ad2dbaa278b82b3c5c4429d8aa40b3e63fa33305956a5`  
		Last Modified: Wed, 23 Apr 2025 19:54:47 GMT  
		Size: 155.9 MB (155928754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b80cf01bb610692d3e9d36753a3eef4a32de90dec8129562c03f7523872172`  
		Last Modified: Wed, 23 Apr 2025 19:59:19 GMT  
		Size: 71.6 MB (71649409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f424a345dfa97182f1940e269135d4592a297c96a70e5440710b2ae21196e4e`  
		Last Modified: Wed, 23 Apr 2025 19:59:17 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6755e48231704cc8f6a37fb1218aa61eff332da9c30e54595acfe61d5554bf0f`  
		Last Modified: Wed, 23 Apr 2025 19:59:17 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:69950b07afc948e0856bffe19ba14c1fa9443e5b3021a62b377cccf7fadf5721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4940265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b514e301f942644600d38d43447e611fe1f3b537c6465e95c1b6ea1c95f28971`

```dockerfile
```

-	Layers:
	-	`sha256:c74efdc114821bc0990b16a68f958b69e3fe72733f2c964117818a9fa2cd51a7`  
		Last Modified: Wed, 23 Apr 2025 19:59:17 GMT  
		Size: 4.9 MB (4923548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62c4bc656bbcf8060c544f6c74d4eab7af364df811bd87cf8a461c9e73a34798`  
		Last Modified: Wed, 23 Apr 2025 19:59:17 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json
