## `clojure:temurin-8-trixie-slim`

```console
$ docker pull clojure@sha256:12d0785d5ed005e5f79e735115a532a26e9af8b13bf734bfd6d56fc73f313a12
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:76843cd626dfc145499ce531b5d7396056c3edd77fa4d756512013d5c7cc9a90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (156990513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2926caa895c9985f80e7d6d3185069d262cbcca9c7fd47fb595a0a3108f58abb`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Tue, 12 May 2026 21:46:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:46:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 12 May 2026 21:46:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:46:09 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 12 May 2026 21:46:09 GMT
WORKDIR /tmp
# Tue, 12 May 2026 21:46:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 12 May 2026 21:46:27 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 12 May 2026 21:46:27 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9cdfacd0463362b9fc4a81d2d6be721b6c260d6f7a06f20db43d65987257ce`  
		Last Modified: Tue, 12 May 2026 21:46:45 GMT  
		Size: 55.2 MB (55198701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021e8ec00ee75e9a1727b493a8c53135a98e7fc4766a2ae2f923b11934afe2b4`  
		Last Modified: Tue, 12 May 2026 21:46:45 GMT  
		Size: 72.0 MB (72010941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7927879db59d13e5cc007fbc04d48c329d3289978d10506b60ffa9487c6e68e9`  
		Last Modified: Tue, 12 May 2026 21:46:42 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7fc261332bd8d39e84ef027a7c3b7e6cc2327ae8b35db81aa169827f03a8a92a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5394561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f3b424a0601bafe987b1b6efe54df0bc9dceb38ce70b3b76687b07782ec6cfb`

```dockerfile
```

-	Layers:
	-	`sha256:3cd53c37d0782fb05e48f6799a6c65b629a27f3ca309c72adeaa0190c35557e2`  
		Last Modified: Tue, 12 May 2026 21:46:43 GMT  
		Size: 5.4 MB (5380179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9e3cd555bed5fbc8fd4191a02773d11cc7eb712bd97273cfbf78f091cc624a4`  
		Last Modified: Tue, 12 May 2026 21:46:42 GMT  
		Size: 14.4 KB (14382 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:569dee4c50546d0774e543105cf74f08ff6cee55a3e9f01ca8cfcf9c9745b0b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156249138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2617ed58669e0b7e998e710d9e1521c756d033b34a4a7213450295e12adeb99a`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Tue, 12 May 2026 21:46:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:46:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 12 May 2026 21:46:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:46:01 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 12 May 2026 21:46:01 GMT
WORKDIR /tmp
# Tue, 12 May 2026 21:46:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 12 May 2026 21:46:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 12 May 2026 21:46:19 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa986c7e8159b86cf830f73b6a2f1830a4bcff1ebf741687f881a9f36306d094`  
		Last Modified: Tue, 12 May 2026 21:46:37 GMT  
		Size: 54.3 MB (54272928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe2d2d5ecf9504c694fd149aa276310550bbf5435e9876b2dcb175c2b8363a5`  
		Last Modified: Tue, 12 May 2026 21:46:37 GMT  
		Size: 71.8 MB (71831922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e386dda4896cf3e9a6319141db9c9b097a2a294724d4297efe2b7b40b98a19`  
		Last Modified: Tue, 12 May 2026 21:46:34 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e4e17301c9ecd0807ebfb42118160a67200fefb9f4b2199e52730742cb6408e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5401148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:241fecc0c8f17a55b400771253fcaddd5baed578c0a674dbf62cdbd5d4945128`

```dockerfile
```

-	Layers:
	-	`sha256:f8c0c8fc139973bd09c275781e4d8e9805d408baf7dd95d77245286dea7d6561`  
		Last Modified: Tue, 12 May 2026 21:46:35 GMT  
		Size: 5.4 MB (5386648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac7353cf012fcbf9720cdfe17252589f753cc46bb5b47b0750ad026675a4a180`  
		Last Modified: Tue, 12 May 2026 21:46:34 GMT  
		Size: 14.5 KB (14500 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:f8a10909c4c646194d639cd6bd89934c3a980e7181ce440fa05ff7c1655a5bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.7 MB (163696819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81b0c38ebcc1b983f6ff4c6bd85dbb2e9c8a1ef2b5db20c85a0d87308b1eeec2`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Tue, 12 May 2026 21:49:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:49:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 12 May 2026 21:49:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:49:10 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 12 May 2026 21:49:11 GMT
WORKDIR /tmp
# Tue, 12 May 2026 21:54:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 12 May 2026 21:54:47 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 12 May 2026 21:54:47 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6108e5c2a2245ec0c51d22b23687faec2598356811a7675057929aac5f8deda`  
		Last Modified: Tue, 12 May 2026 21:50:14 GMT  
		Size: 52.7 MB (52669152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd0e92fede26ce26a7bab590e014ca7d14208a6bec0617c670780780853ce1c`  
		Last Modified: Tue, 12 May 2026 21:55:32 GMT  
		Size: 77.4 MB (77428932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8615ba4c294e9154872606ef3d75cd82af68ff96945c76d0fa269fbba636a6c`  
		Last Modified: Tue, 12 May 2026 21:55:30 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a233485b145efce874fe8f5c3e7f4dd6fb9c11f1e630ea624ae5b2895d0d05a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5399575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af87b65fba615610900d67edfdebd78ed0085cbb9fbd7027d2a39a1ebbece06`

```dockerfile
```

-	Layers:
	-	`sha256:fffcbd1a5051b55494c85e6b3de0835fd77542277d2a1e1cb0942d3a42bf4c78`  
		Last Modified: Tue, 12 May 2026 21:55:30 GMT  
		Size: 5.4 MB (5385145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0103bc840f669227e1400c56bc6350b54de725b011216045705279e44fff3e99`  
		Last Modified: Tue, 12 May 2026 21:55:30 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json
