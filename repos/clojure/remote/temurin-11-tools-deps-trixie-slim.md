## `clojure:temurin-11-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:aa33b0b947c0187b84bcd2e45f2e41e8abd4f6079e0b3819435bbc8151cd4ed1
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

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:61dc6198592a2d2e8f635ee6d6aa9fa957c22becab6bca441ded97182b0ad459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244624093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37e139acf35ee6c8690005f46a42cf2b218dedd90d7b081e79c415ad902ca3d4`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:16:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:16:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:16:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:16:54 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:16:54 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:17:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29ed2b38d0eceb355c225a1ea29df7c7c356e723d29293cec122e302bf99aae`  
		Last Modified: Wed, 24 Jun 2026 02:17:34 GMT  
		Size: 145.9 MB (145886167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e210dbfe613a1692995655800937e476b18cbd8ec1b2d9b75272f77ad0293ee4`  
		Last Modified: Wed, 24 Jun 2026 02:17:33 GMT  
		Size: 69.0 MB (68951862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666d0dede8687b8673589f56dd8167682fed8aae32b9c5e519e375aa41c1f104`  
		Last Modified: Wed, 24 Jun 2026 02:17:29 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6ebbfd9f9dc1dc6913912c1ccc453b4b3a3093c8a0677defe5849b6f747f2cb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5291155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:607a1ea7ff363e7d1f78501615af71826b876bd72c7361c86f1009d689e7e2c2`

```dockerfile
```

-	Layers:
	-	`sha256:7aff31c0eed741545f6daf8e179095675cd98785476ce25607e9a618fce1bbe1`  
		Last Modified: Wed, 24 Jun 2026 02:17:30 GMT  
		Size: 5.3 MB (5276758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b00ba2dbf93720764c93818e703b58537b0e67807b560f77bad85285c0dd780`  
		Last Modified: Wed, 24 Jun 2026 02:17:29 GMT  
		Size: 14.4 KB (14397 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7f453c1e5667f394632301429484f6baf1652b0971c326ddc7cfce1291a76c4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.5 MB (241508885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a940f0eac9ac29baf5287bd0a62e2bf39ceab1713ea4d06ce9fbf75ff3f0b3c5`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:23:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:23:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:23:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:23:29 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:23:29 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:23:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:23:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:23:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b481e690ed9259247e406fb8c177ad527db3ad6ee3ae560a7bbfa2215d954e3a`  
		Last Modified: Wed, 24 Jun 2026 02:24:08 GMT  
		Size: 142.6 MB (142582130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6185b7b0175ef7ae7b7f0cd02a96421fa0b1404986a9ebee57989ce4b736363d`  
		Last Modified: Wed, 24 Jun 2026 02:24:07 GMT  
		Size: 68.8 MB (68777559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736b03594c8c12fc909c3f390af0f494c040948c44174745b10f7b6ef7a00946`  
		Last Modified: Wed, 24 Jun 2026 02:24:04 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:04cbe2941abf658f0d93ecb200e75d6745b84a92f9298e2d5f8cf89d7f2f77b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5297652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483132dbe01fe6162e9000e9de0ddd834d0993b52492aedd8b98d1dfea683327`

```dockerfile
```

-	Layers:
	-	`sha256:66033af8e4dc43430e7fe945d882418e6943150ba6a2e283cee24efad42fc848`  
		Last Modified: Wed, 24 Jun 2026 02:24:04 GMT  
		Size: 5.3 MB (5283137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a84ac1912c3864d42d2eb5fa6dc9a68899790fa4bb1cde94109d760f01a96006`  
		Last Modified: Wed, 24 Jun 2026 02:24:04 GMT  
		Size: 14.5 KB (14515 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; ppc64le

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

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

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

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; s390x

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

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

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
