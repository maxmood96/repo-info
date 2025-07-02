## `clojure:temurin-8-tools-deps-1.12.1.1550-trixie-slim`

```console
$ docker pull clojure@sha256:9758a0722114e761552dc45b9e096dea872bf6b5511c8c01dff29cf2bd4718ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.1.1550-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:71c0b9ada4ff81cf9e37dedc93b8457090cdaf1c407d2d0465eff6726a138e6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.3 MB (156289741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c040a7c344cbf7ce90145b033cb19be7c364b87a323777a13de19c48ce302c0a`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f7f88c6d7f710176d487a3ac59c7790f981832a06bfc197dbe4a74d73b1407b7`  
		Last Modified: Tue, 01 Jul 2025 01:14:56 GMT  
		Size: 29.8 MB (29761106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71039e295ac88fbe92857fb224fefe5e8b660818f787f7fdf3814a053c6f8d5c`  
		Last Modified: Wed, 02 Jul 2025 04:16:01 GMT  
		Size: 54.7 MB (54716182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdff7602460d7fe35c25b10eb23e6b2a81fdbf780eeadbf53805f3d89422e319`  
		Last Modified: Wed, 02 Jul 2025 04:16:02 GMT  
		Size: 71.8 MB (71811811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33a5e25e4d8e06f06137a8fe789db4278a9ee637824926908f7edfd7c3d6e1e`  
		Last Modified: Wed, 02 Jul 2025 04:16:00 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.1.1550-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a6b9d95c6e21d981c15d22fa94bfadb5b37c37f4e630c4cc3252f4a4f7886e43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5388683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dbb63703e21e8d62a3056f1e1cbc47969565db3f01d599234bc2364cea16911`

```dockerfile
```

-	Layers:
	-	`sha256:37dbe7c76926c98b6c57566df8b50a33ab994e42eb82fd730c7a64139a22dc15`  
		Last Modified: Wed, 02 Jul 2025 06:44:16 GMT  
		Size: 5.4 MB (5374412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8f719d3443b6398ebd93ca9071e1f0f74b81b79fa671d98bbede6a7da17879d`  
		Last Modified: Wed, 02 Jul 2025 06:44:17 GMT  
		Size: 14.3 KB (14271 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.1.1550-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8d50d015a8db95157b121e157015c8b8747c09e71e9f43101b01e430f2d1dcd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.6 MB (155600653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78ea84d7859987b1250fec86a9646ff0e945e6295c85644b265d71ed4f3a5977`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:dfa10e860e0106510a14bae8331a4dd762d3d3737fdba0dbec102458f9853b71`  
		Last Modified: Tue, 01 Jul 2025 01:18:18 GMT  
		Size: 30.1 MB (30126864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fab7ab71429fe9fd6f8605a909c7fc7ff78f2050e83de6cc053213bd3632461`  
		Last Modified: Tue, 01 Jul 2025 12:00:15 GMT  
		Size: 53.8 MB (53830498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3671ffe27d19436c18421ea18714ace27fcf63565baeba83e6c13c5451d5ce`  
		Last Modified: Tue, 01 Jul 2025 12:04:47 GMT  
		Size: 71.6 MB (71642646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c0d599ea72c6618ffe27672a05c9978a9ab07c9766040a8836db30eac6cb62`  
		Last Modified: Tue, 01 Jul 2025 12:04:41 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.1.1550-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f0f3f2409e1d6be048da11cffb927bb7e7a8bd7853fcffeb7a7b454e4426f0fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5395268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b7e9b95f3482d64edde21a3c3e29a9925921678b4795a2f5a85099905cda04c`

```dockerfile
```

-	Layers:
	-	`sha256:bd1e78d8db40c33e22d7f1bc3e6417d66c0157b35c4ab3807bdd8f6739c64c3b`  
		Last Modified: Tue, 01 Jul 2025 12:40:00 GMT  
		Size: 5.4 MB (5380879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c45e39510c80f7ce6128821c37cf1734d1875eb008845618daa6aebcd95a70b0`  
		Last Modified: Tue, 01 Jul 2025 12:40:00 GMT  
		Size: 14.4 KB (14389 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.1.1550-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:73f31381ed3e8557df0002e27fbe6341ab8627c48c864fb0795b4fac67b07489
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.0 MB (162987574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c4d3c8503853bff3316e05ef7643f63cbc05e591ee876b2c33e674b52f1284`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2adebcab7d76ecb14ead3f70af8ca34e5abca513c2fcbd9f40e3af1e18442ccc`  
		Last Modified: Tue, 01 Jul 2025 01:19:23 GMT  
		Size: 33.6 MB (33586035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940d4577e90e91e93bc0661f944376a04970f346bbafa049e4ea9ab1b2d336b0`  
		Last Modified: Tue, 01 Jul 2025 08:20:20 GMT  
		Size: 52.2 MB (52167970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2d129d56368d7cce3c5d6aaf0d8555ff4ff166f2f473282cd258741f8a103f`  
		Last Modified: Tue, 01 Jul 2025 08:27:35 GMT  
		Size: 77.2 MB (77232924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac791e0dd313ea3093afb67f3159b6f668e4131b17b58a36b02ff4241a73dfa`  
		Last Modified: Tue, 01 Jul 2025 08:27:24 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.1.1550-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:feb22127af37032c6f03ea2056195ea4fd0c7714dcdba6cce115d83fe4905fe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5393694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:065492ff7b66dde697a0acabd70b7a48ce2bf453900ce48ab718cddce820d86a`

```dockerfile
```

-	Layers:
	-	`sha256:e03aaabaa83a6ff7cf4aedf9d7cbfb8dbea21f3b7bcbb841277d222e7610f147`  
		Last Modified: Tue, 01 Jul 2025 09:42:52 GMT  
		Size: 5.4 MB (5379376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b5855826156df15723fd6030e525ecebbed3103c6c9b58b7488afa7d220ea0a`  
		Last Modified: Tue, 01 Jul 2025 09:42:53 GMT  
		Size: 14.3 KB (14318 bytes)  
		MIME: application/vnd.in-toto+json
