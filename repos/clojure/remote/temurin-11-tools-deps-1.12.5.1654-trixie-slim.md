## `clojure:temurin-11-tools-deps-1.12.5.1654-trixie-slim`

```console
$ docker pull clojure@sha256:ace7a3445c788c254efd985c942bfb7b107ac19fec0b3da07c8ee6de74298be4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.5.1654-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:501687974e00c447b7bdfaea1096b6c3f458ea138262dc0c864b5555806d2607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244623908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91198d7188390e90efad0d5c1075185978b714678099e2a18bfea5f26b9f3721`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:16:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:16:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:16:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:16:39 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:16:39 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:16:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:16:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:16:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd2500507b433d71b98033a2875fd2d63ecd32fa2913abc9a56a579f5016f2e`  
		Last Modified: Fri, 19 Jun 2026 02:17:15 GMT  
		Size: 145.9 MB (145886183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b2e5a161cd92b0facc178dc2c1fdf10410e8d628f75aa54fb637bc444811c90`  
		Last Modified: Fri, 19 Jun 2026 02:17:13 GMT  
		Size: 69.0 MB (68951665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86662867e3257e5b07b8d5378d8810237a0a6ce3d0ec7c34d58e0d05e6fde910`  
		Last Modified: Fri, 19 Jun 2026 02:17:10 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.5.1654-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:78660162ed7bc8b0168743b16961a2c6c52d4b06a8e5af27e339a1d885771268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5291155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05eeb59b9902d18eb8edd11feee9d1de96d580fc6d752c996f8c796d3bbf28c2`

```dockerfile
```

-	Layers:
	-	`sha256:3da8d145834cc375365d973545fb80df3ca3eee84cf1c1638c07ecfee63e226d`  
		Last Modified: Fri, 19 Jun 2026 02:17:10 GMT  
		Size: 5.3 MB (5276758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a5a41d1eb029a3a7690af18a2afafb3a6db1d18c869d1a0d846b9d756e77670`  
		Last Modified: Fri, 19 Jun 2026 02:17:10 GMT  
		Size: 14.4 KB (14397 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.5.1654-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4f3f6fa6c368731e72b5de66ca6e2acc10d6928ed236b46412d88e2dd37f2322
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.5 MB (241508820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2b6dd91c380262f1aa7b02ceabd4c1793f6caa0b4a767408e7a815c16d0454c`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:16:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:16:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:16:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:16:43 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:16:43 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:17:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:17:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:17:00 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe80cd134fc3a69f2b6f76e5bdc1620d4d40e4d2876804059ade3cc1535d565`  
		Last Modified: Fri, 19 Jun 2026 02:17:23 GMT  
		Size: 142.6 MB (142582166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af59df2367c377983ad5e616948027cb595eb453c97e234110ebd775a526235`  
		Last Modified: Fri, 19 Jun 2026 02:17:21 GMT  
		Size: 68.8 MB (68777480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d868c02cf121062e0942fe50eba159fde664ea1079b8ab6fe281f47fc62f087`  
		Last Modified: Fri, 19 Jun 2026 02:17:18 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.5.1654-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d7b340f2e3bdd1ce072040ef3ad3b78ea41b99aad707c7ed2678729336afaca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5297650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9874922c1a270a184adc76c0841baacba2bf58a42e1d762c321acbf949bdf60a`

```dockerfile
```

-	Layers:
	-	`sha256:9b56d1503367b8119eaa8a7aff1395942b1f005ba040c0b4377ed9f6fb49f9f7`  
		Last Modified: Fri, 19 Jun 2026 02:17:18 GMT  
		Size: 5.3 MB (5283137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de80eab62b048c6ee118e0555da066fc6792b751880a0652cb5f47136ccb1709`  
		Last Modified: Fri, 19 Jun 2026 02:17:18 GMT  
		Size: 14.5 KB (14513 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.5.1654-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:7600901e3ecb7a36a772944cdf749394a47588fdefe88d34b372a71259691e75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241086513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f701386d0d820bcae8aba9d828795377f195b7b9916f2d303e15b5939ef4b3bb`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:29:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:29:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:29:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:29:08 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:29:09 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:35:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:35:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:35:45 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9d6b2e320e2b74843186d830e8202c50ebfaeccf823d239e3e3e349a8a508d80`  
		Last Modified: Thu, 11 Jun 2026 00:24:42 GMT  
		Size: 33.6 MB (33606340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2428a8f97ac98f0d71ffd28681ba4ff4587bb2650c297ffc24f3785b183cee`  
		Last Modified: Fri, 19 Jun 2026 02:33:02 GMT  
		Size: 133.1 MB (133110616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b74a43550685af39bb3939051f30a5cbcf4f8448b56b9768c0dd03849cb1a5d`  
		Last Modified: Fri, 19 Jun 2026 02:36:25 GMT  
		Size: 74.4 MB (74368912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b3b07323441fde04a3beac8dc94e12c026088c9fc0429915baa51ae297e891`  
		Last Modified: Fri, 19 Jun 2026 02:36:23 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.5.1654-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5b5e1e2a21a907dafb10c746b4cde44a7e1acf9ca6269aa85453289f3d553639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5294959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:854a25cd104d627a1516b5ee82836d90892ef7677e7d284ec71e76a486beb39b`

```dockerfile
```

-	Layers:
	-	`sha256:2f11796d97b9baf550f06a8dac809b45066fac96c0d4941f65c8f9e579dc3fff`  
		Last Modified: Fri, 19 Jun 2026 02:36:23 GMT  
		Size: 5.3 MB (5280514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:336b923b5e4dd75ec1ec8682a1d6f0243f6e953acd324703b093ca2e11c7f1ea`  
		Last Modified: Fri, 19 Jun 2026 02:36:23 GMT  
		Size: 14.4 KB (14445 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.5.1654-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:79479da1e31caf32b096d3c4e9adf0af73b40a69acc9576eb44a4cca00a978fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.4 MB (226437026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:115fd2813e22e33d3ee977082ca0932973e17b178b98a4ddcb3c115b67e59522`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:16:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:16:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:16:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:16:13 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:16:13 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:16:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:16:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:16:30 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c53cde7c9a9ee847d52216cd6942384eb361f014d156cbf60aac7d77ee82ef`  
		Last Modified: Fri, 19 Jun 2026 02:16:59 GMT  
		Size: 126.7 MB (126652584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0fce09ec31c0eae95a59ab79af3fe0748aae86626ed7cababca44d5ec0785d`  
		Last Modified: Fri, 19 Jun 2026 02:16:58 GMT  
		Size: 69.9 MB (69932445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b0ff0d0fafb8a036728a7c8f1b143a169e0b54ee84cdd4b01bafd857750c19`  
		Last Modified: Fri, 19 Jun 2026 02:16:55 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.5.1654-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:71fff8ae99e95bb832dcb833fa4df767238926f2f2091770d55c8bd4118fd215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5287083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8f7cbe2995628908ca7498e64ef51dcf541b3dbf000fec211802a953fdd8bcf`

```dockerfile
```

-	Layers:
	-	`sha256:69c9d9da11506320eaeaa4a192e83ae7b061db393c51580314054bc621304925`  
		Last Modified: Fri, 19 Jun 2026 02:16:55 GMT  
		Size: 5.3 MB (5272686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af57751384921aea6ff231a5706e0ea7692437b7b98a2337302754ed480667cd`  
		Last Modified: Fri, 19 Jun 2026 02:16:55 GMT  
		Size: 14.4 KB (14397 bytes)  
		MIME: application/vnd.in-toto+json
