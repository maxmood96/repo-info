## `clojure:temurin-8-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:b826f81c9a6d7a8f299622ee7f46eacb082754a3b6c4a58b8242d6c91b26a739
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:183f2c8b7657c9600431e2e100fb0a9678e89088e0f427389956a1eaae0d9c0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (157026378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7fbb12367abf4b849319d7ac05beedeedde08a8bd2328e56d5e5fb657163960`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Thu, 14 May 2026 23:33:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:33:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:33:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:33:52 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:33:52 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:34:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:34:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:34:10 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:112f8a213bcf0ee1ed2f66c98439af43b35bbbe1510999514e0ff1925a401502`  
		Last Modified: Thu, 14 May 2026 23:34:29 GMT  
		Size: 55.2 MB (55198706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43a90d8b5c714255f4a82df5c2f0445115516fdf88ed478ce3fcc27056bf465`  
		Last Modified: Thu, 14 May 2026 23:34:29 GMT  
		Size: 72.0 MB (72046799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9c01f3b760c7fd1ab1c1d1ad669579c593f85bbc8501132fd12fbad9794d9c`  
		Last Modified: Thu, 14 May 2026 23:34:26 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2ec29fb8f95d715409c50e0fb1319649a2775c152bd41a732c11fe1a11190a91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5394595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99724b52407da44823abf564a2c3cad0a28a72967f0d97ffa3a7a98110b43047`

```dockerfile
```

-	Layers:
	-	`sha256:f4afa2bf85f2cb834615ae70ea41ccadbb22155a916dc02dedec13e08c84328e`  
		Last Modified: Thu, 14 May 2026 23:34:26 GMT  
		Size: 5.4 MB (5380213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d661c5f96131edc1eb4ca329c469ae8d46d6ed5f69878ea8534824870654b5a1`  
		Last Modified: Thu, 14 May 2026 23:34:26 GMT  
		Size: 14.4 KB (14382 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b5e2d4c77ae29344f3705e3772b9dc4cca417b8b6fbd3575a5ee8c2fa53c9129
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.3 MB (156271913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3897d29144bb7116e721f9df45a551c4ddde1d22d35eb5399c5d320ddec43592`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Thu, 14 May 2026 23:34:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:34:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:34:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:34:09 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:34:09 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:34:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:34:27 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:34:27 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6328ccac5de7f24555779ca4d239729fd1951e0b18f4b52b0bc9d5f8f92fdffe`  
		Last Modified: Thu, 14 May 2026 23:34:44 GMT  
		Size: 54.3 MB (54272927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8a91d76877c13cde4ba71e2c1d3ddd59afef2cc1fff4092e3e6de05761e24a`  
		Last Modified: Thu, 14 May 2026 23:34:45 GMT  
		Size: 71.9 MB (71854697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3faf379812bda853b76b640e7e558681a70d272a0de539ac9b54a6475a13dc5`  
		Last Modified: Thu, 14 May 2026 23:34:42 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ec87c65968a19cc91662274c6a10bc32eb35825109baa3053e894bdfd0f5f60c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5401182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19dfd5f08ac26b5b707822e972887be54f399bc69fec0be2cce6109b7b66c03b`

```dockerfile
```

-	Layers:
	-	`sha256:dfe60c25ef8f542d08eabb1eb85c488ba6537d795e70f4f1b43033f6b2c119ce`  
		Last Modified: Thu, 14 May 2026 23:34:42 GMT  
		Size: 5.4 MB (5386682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:185430c7287a81fad1a10eb5ae15a934b384e68e728b36904b6db9e38bdd405c`  
		Last Modified: Thu, 14 May 2026 23:34:42 GMT  
		Size: 14.5 KB (14500 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:1fb50e93ea293ffd1c2d681d1fb0b8ff6f90eef87b5140d0b0eff470272c7626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.7 MB (163725271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2032edc588d22e3ad40a10e5531f659fc6533d6a996e76a60aed756f3ec05e8`
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
ENV CLOJURE_VERSION=1.12.5.1638
# Tue, 12 May 2026 21:49:11 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:37:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:37:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:37:40 GMT
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
	-	`sha256:92c98320f3dec4984225c8ff7804e3da247a3d0918a3a2917ce2a7226db82068`  
		Last Modified: Thu, 14 May 2026 23:38:13 GMT  
		Size: 77.5 MB (77457386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb161a856a37e0385985aebe9490860046ac8ee37bf35652de00f0c19f48d400`  
		Last Modified: Thu, 14 May 2026 23:38:11 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:350b278cf9e18ae141fef6716efc6089d875ee18317798cffcbcd0e455bac375
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5399609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d203c430dd6594e3440f36791c619fcb74c8a849bbeada99c195aec8751c735`

```dockerfile
```

-	Layers:
	-	`sha256:1df819ee4f635967d162c6d1e5ff7046deb28d3eaac0c4c0df79c46e05fbed41`  
		Last Modified: Thu, 14 May 2026 23:38:11 GMT  
		Size: 5.4 MB (5385179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:701eda7963f4c583e6b55595ef24de30d506dd7179417a971c4e332ced5ea928`  
		Last Modified: Thu, 14 May 2026 23:38:10 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json
