## `clojure:temurin-8-bookworm-slim`

```console
$ docker pull clojure@sha256:33f72501cb838f4ff73ed90747f2e99032e0d9e5cf9c2c6c683f992e36e03c25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a53050e6f343ec6416016b11c8841986819a0460e617527fd809dafc3eff739e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.2 MB (201159064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f20da3b59ba98413ba8c37985ecfc6eabd188a1ee9942403f706b51a3fbd92d`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585e257bd30f6accdd3f5fd8f11a6e160953c7568b1391bf6d7c3bee450f2473`  
		Last Modified: Tue, 24 Dec 2024 22:37:01 GMT  
		Size: 103.6 MB (103633884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198b0eabbe8b082f6498d1e4fbd7aaac7763a19604411da186b400cb6b2bf2c0`  
		Last Modified: Tue, 24 Dec 2024 22:37:01 GMT  
		Size: 69.3 MB (69292957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a18d5c5bf399716d796de485e940bc7d1b9165c70e24a4d5dda10e4059f1259`  
		Last Modified: Tue, 24 Dec 2024 22:37:00 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:85d1cc392e0d047604a4a15f27d833da0f7dae5d6bb1ea581487b83fc2408b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5049020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fed3b2f92e054231185dd06a729b830d890f43c3064aafeb721df229742ea803`

```dockerfile
```

-	Layers:
	-	`sha256:26e8f38ef0fd552d8ff464ccff1fb689405bdbf66dda372568823cea8207436c`  
		Last Modified: Tue, 24 Dec 2024 22:37:00 GMT  
		Size: 5.0 MB (5034725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fc0b994344efae27f0a7b26876848fb50c46d94bd30b60111796acb74e5d004`  
		Last Modified: Tue, 24 Dec 2024 22:37:00 GMT  
		Size: 14.3 KB (14295 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:da560122f746fafe01275344cf1e7b33ab08cfd4522c2f9d4ef7ef4cad8536b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.9 MB (199948249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0848ae82a8c6aa3452302aa7132c838ee7e84228ed9b3c43530ed714757b61a`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1cfe902e794cc801f92f679144f5d6a2eda6c1dabe35ae94bc730cf925e2044`  
		Size: 102.7 MB (102747754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8ff4d546d430e27c2d41d8e7f03f20ec420fefc32c5a86451ee0831952c51e`  
		Last Modified: Wed, 25 Dec 2024 07:15:34 GMT  
		Size: 69.1 MB (69141129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819f344ed1e0ae6483fa78f982519849e110447f9a75ae044c6bbef14dcfac49`  
		Last Modified: Wed, 25 Dec 2024 07:15:32 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5cc1260095cea2f5f4f8f2ac5a33edf98a06fb74af2cb33d0fd10cc5aaf76c0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5055597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9c828d280f8365d2d3e7352974bb246b069ff2089422a3f1864334189b05ff7`

```dockerfile
```

-	Layers:
	-	`sha256:a77724acb0195d56c90925c0200514d0348e8f5410db437e0c9f0e502f715de0`  
		Last Modified: Wed, 25 Dec 2024 07:15:32 GMT  
		Size: 5.0 MB (5041184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15be42e8fb5712f38acb3966622b3432f62e463d11908eec3825980ab0c93125`  
		Last Modified: Wed, 25 Dec 2024 07:15:31 GMT  
		Size: 14.4 KB (14413 bytes)  
		MIME: application/vnd.in-toto+json
