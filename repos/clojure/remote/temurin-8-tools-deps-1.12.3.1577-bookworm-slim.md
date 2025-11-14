## `clojure:temurin-8-tools-deps-1.12.3.1577-bookworm-slim`

```console
$ docker pull clojure@sha256:a1d64de1546695363248aabf42cafe7c71cf99038326c6e926840fd802af854c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.3.1577-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a2b2945ab15ad036b826c1c72560e5048afe5c39484404c9a2f2ea0653b23233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152642076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ae4c8204b16ca944f5939352fe4277165fc2f299639b212671cbf563296686`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 00:49:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:49:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:49:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:49:44 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:49:44 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:49:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:49:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:49:59 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a707864e336507ee79b36761c01dd08c9e7025b8199b239cbfe746680d4230`  
		Last Modified: Fri, 14 Nov 2025 00:50:27 GMT  
		Size: 54.7 MB (54733370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457ae0aeca7e8d160c48bf56597aa34f9afba7cdf45aa2a3a24d6df2bdf59dc5`  
		Last Modified: Fri, 14 Nov 2025 00:50:27 GMT  
		Size: 69.7 MB (69679493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90081438bb6fcf8ec8ae43e82fd399acc66cacd6730050df9d5f0eb16ce4ba39`  
		Last Modified: Fri, 14 Nov 2025 00:50:22 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3db1d2302c82062877a3568b304b38a49ab6ec80d100bd7c2c420dae0fbb0bcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f147c54ce67eee3834c102fb5c8ffb743f37d41549e4a8dbd2d1c8e366a41d05`

```dockerfile
```

-	Layers:
	-	`sha256:aa96d2b8345fde31af2d0deffdd4db90e5e03ff3b5892286101f3784552eb16c`  
		Last Modified: Fri, 14 Nov 2025 01:49:15 GMT  
		Size: 5.2 MB (5234998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e544a457a62430b97aaf07e9e7c0460e7210c628b05e122a55c6e3a2abcffe7`  
		Last Modified: Fri, 14 Nov 2025 01:49:16 GMT  
		Size: 14.2 KB (14248 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.3.1577-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7c96910ae058fc33ffec251ab133892cb2b5120f45b838bf0033cee5e3d57fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.5 MB (151478617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5b7e0db1b474c66d59af0227c040bd761d62b656bbbef059ffbb4ebacb88300`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 00:51:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:51:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:51:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:51:37 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:51:37 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:51:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:51:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:51:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ed64950460bc94ecd9ebd9018221ea2315cc17d94930e57125afc0b0a811c1`  
		Last Modified: Fri, 14 Nov 2025 00:52:24 GMT  
		Size: 53.8 MB (53815011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23817b75628694df389dd32da47ee68a290fd43a0f83392353c4f9ec6c3d2253`  
		Last Modified: Fri, 14 Nov 2025 00:52:27 GMT  
		Size: 69.6 MB (69560582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d296da018bb579eac53cdbc0bdb5d046e4ba1501c86b885d85cc110696db750`  
		Last Modified: Fri, 14 Nov 2025 00:52:17 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:099446125973bcb3dc4b655e6574dd513b635df4e951a5e9b61331a2976ce592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f73469ec693c803c58e7d8b77c160aec7db38071fbb82e0099de10da494a3dd`

```dockerfile
```

-	Layers:
	-	`sha256:3206544b30017f9a5eeec5a35568a154841ffa52530be494f1b1cc1d48f2d0d6`  
		Last Modified: Fri, 14 Nov 2025 01:49:21 GMT  
		Size: 5.2 MB (5241457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4caf2bbf71aae531991d83ef591954be3614935a6af0cd56537fd948de57a5a`  
		Last Modified: Fri, 14 Nov 2025 01:49:22 GMT  
		Size: 14.4 KB (14366 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.3.1577-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:4c0d1b28187fff393af3256cc77e874a5961c9378e923d6189ebd67b1cccd8dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.8 MB (159758257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01511e022f407d78e5ee8a067fce28fed0a8f57a22142daa4f8794c40cecac46`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 06:25:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 06:25:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 06:25:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 06:25:13 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 06:25:14 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 06:34:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 06:34:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 06:34:28 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2442ae4ed78d32124d4f8b92ec0b1caf0e12483bafbd1803659dc391d3600616`  
		Last Modified: Tue, 04 Nov 2025 00:13:59 GMT  
		Size: 32.1 MB (32068905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06690e9a4868c5149e430d9b77d8b8edde0f36a52f628919ee8e22174312b710`  
		Last Modified: Fri, 14 Nov 2025 06:26:25 GMT  
		Size: 52.2 MB (52175091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac54881e6b08117e10520915ff7d3bcb8e6ba9a24a4cb393526970695fd25ef`  
		Last Modified: Fri, 14 Nov 2025 06:35:16 GMT  
		Size: 75.5 MB (75513614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa26227b3174c55fadf8d97f997ef86c111014c67ba96a5afc191ccc8dc179b9`  
		Last Modified: Fri, 14 Nov 2025 06:35:10 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:05525757ab2bb4ac361339ca9f616070ebe057bb99760b01d44331f4f488548c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b1693f663502c718bfde25d14b4ac77dd9c5719ed7a73cf72730a919697cc86`

```dockerfile
```

-	Layers:
	-	`sha256:024da9626ca77b7ece5e33ee7c32c8dbf766c609b01de15d6180a8305520874c`  
		Last Modified: Fri, 14 Nov 2025 07:39:36 GMT  
		Size: 5.2 MB (5240749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d18e43a77a188dea2dc9106585a95542d79d9d6217e0dbfe46b81b08ea4b0b34`  
		Last Modified: Fri, 14 Nov 2025 07:39:36 GMT  
		Size: 14.3 KB (14296 bytes)  
		MIME: application/vnd.in-toto+json
