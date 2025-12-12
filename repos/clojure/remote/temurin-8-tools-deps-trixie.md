## `clojure:temurin-8-tools-deps-trixie`

```console
$ docker pull clojure@sha256:207b24e5640b008fd47be1b36b057c0351b146ef24711b129443d97f00278a5a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:000b1013b50e316f8eefed4ec7f989bb097495c2fbe2e3cffc03c4dce763e2fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.6 MB (189566644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d967f2b5656b6c4193064a2a93873b9dae4f930c017f54828ef65569fe2ef3`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Thu, 11 Dec 2025 22:38:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:38:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:38:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:38:27 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:38:27 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:38:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:38:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:38:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2981f7e8980b9f4b6605026e1c5f99b4971ebba15f626e46904554de09f324f4`  
		Last Modified: Mon, 08 Dec 2025 22:17:46 GMT  
		Size: 49.3 MB (49289520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf03c19343dc5b1806715cc88d969dd89d062515c50207dd615690f9ea8b7d0`  
		Last Modified: Thu, 11 Dec 2025 22:39:21 GMT  
		Size: 54.7 MB (54733371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69b55f4d8c4e0006025670c0c3a0436a1135a4ab4530b1ca98136b22c483547`  
		Last Modified: Thu, 11 Dec 2025 22:39:24 GMT  
		Size: 85.5 MB (85543109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f21648b74d380ee43e3312da4db3dc108f133ba575a61cc5cc4ef8972a08d1`  
		Last Modified: Thu, 11 Dec 2025 22:39:12 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:fa7f531bcd2fa1d04f49d6146f2dacec22c8d0f966a2dd8c653815c6a8a764d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7602709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20e7a1e961b1c913bcb754589fdcb69056f58f0ad78a0a48632786d542bfa9f2`

```dockerfile
```

-	Layers:
	-	`sha256:831239e5e8e294caf1f125f9d4d68a5a3b9fe898852a983885ad50bfdfd2b012`  
		Last Modified: Fri, 12 Dec 2025 01:47:41 GMT  
		Size: 7.6 MB (7588539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55b6865e3008743578844998b852cc614208f77536601f1829aa580172d5546a`  
		Last Modified: Fri, 12 Dec 2025 01:47:42 GMT  
		Size: 14.2 KB (14170 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fc4f47e0278acf4a74b08a3bf8c083e915c716f54451db59288925c3362074d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.8 MB (188827044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8791c89a116515ead066afb6b61c034914ec5e2095f16c2435d823448da8821`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Thu, 11 Dec 2025 22:37:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:37:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:37:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:37:30 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:37:30 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:37:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:37:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:37:49 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6a828f739420ec96bad6123094a07f3f234998f6cf772e34e0ba733aa8e2b347`  
		Last Modified: Mon, 08 Dec 2025 22:17:28 GMT  
		Size: 49.7 MB (49650226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9f72568c59acde038d00c386810b2c1efe5dc3b41f1e5a705ded0098403ba6`  
		Last Modified: Thu, 11 Dec 2025 22:38:22 GMT  
		Size: 53.8 MB (53814993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed09c9dd0fe4082501db6fea1f8f20337aed821113ecc4506d15d9dc4113e5fe`  
		Last Modified: Thu, 11 Dec 2025 22:38:21 GMT  
		Size: 85.4 MB (85361179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1414966d4cd286938b839dec465eb9835d79db68d03fc67cef4d587188e073eb`  
		Last Modified: Thu, 11 Dec 2025 22:38:16 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9ac9dffb505e8513f493346056fd5fad2d4479ff1c6dbdbde53976ade49217ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7610555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:012a8a1d489777571e3492b3d79d356eccaee1cb4b75e3b41d7dfdd32cab4f42`

```dockerfile
```

-	Layers:
	-	`sha256:a20c9765a2d0ab78acb3032de65aa528908217f8a583f99efbe58c62b66a919d`  
		Last Modified: Fri, 12 Dec 2025 01:47:48 GMT  
		Size: 7.6 MB (7596267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:448cabbcbb0b6eda8098252726548d92eac0c9f0392be98d3a24c17d6308f26d`  
		Last Modified: Fri, 12 Dec 2025 01:47:49 GMT  
		Size: 14.3 KB (14288 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:e282e13ae26da6ad02a19326ad73085648971ef1f77d1a980dd7f189adb28f70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.2 MB (196229343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b745a00acf198dc997f3451b0df1b512d648a8e3d392f9bbe3f75885f51d5b`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:23:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:23:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:23:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:23:38 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Mon, 08 Dec 2025 23:23:39 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:46:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:46:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:46:13 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:fb00391cdf4b5dc5fe2e67e0bee3770076e9af9efed48ba15cb306902e36c78c`  
		Last Modified: Mon, 08 Dec 2025 22:52:23 GMT  
		Size: 53.1 MB (53108478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17fdcbbf285191165c95df89028a64259c84d1fd6873060f7cabecc5d7fc9547`  
		Last Modified: Mon, 08 Dec 2025 23:25:07 GMT  
		Size: 52.2 MB (52175122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1a6e6ad9be730d329519e6a9737ac0d25271d9c5027a217e1872745eb6e6ab`  
		Last Modified: Thu, 11 Dec 2025 22:47:07 GMT  
		Size: 90.9 MB (90945097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6c0d6fb699449f3316c0b54163b5bb830c03cd5518efd395bb15b005566f1a`  
		Last Modified: Thu, 11 Dec 2025 22:47:00 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d9e1771551cf3ec97a00f5f94c35b2161d5aaf48d2b9b776c06af94322e40feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7607769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d524e6f2d8ed02d63ffe7160e505cef6283f29a8a2311af5f06d6c832baea192`

```dockerfile
```

-	Layers:
	-	`sha256:51d471fe0776c8159e247ca16983eaab097e9a044b5718b3db3d3af2a1b2204c`  
		Last Modified: Fri, 12 Dec 2025 01:47:56 GMT  
		Size: 7.6 MB (7593551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:505d11ba902459cdf55ac8b2fc753878b608e3a7cb666718bba0d2ed74c54dc3`  
		Last Modified: Fri, 12 Dec 2025 01:47:57 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json
