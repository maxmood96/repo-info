## `clojure:temurin-17-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:0a565e254acabcf07e4042c857be0e8b069ab301b3b234e1abb0a6bbccc0d047
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

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2e5f5cc086ef92761e0fa4f3440667a780a5145b7b718c9f7910a554d7a7b754
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.5 MB (242458912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad4c7217b649119254aab5ffae753b3990bdba1c389301557d870fde781deb4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0a7fa069bcc662f87609ea6c3287f00b3050534b1ec9adc8def6f19dabb6f4`  
		Last Modified: Thu, 14 Aug 2025 03:02:04 GMT  
		Size: 144.7 MB (144693300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f916b5afc2258deefde1819160b7451beed189863187dc842356b651a6d3f1`  
		Last Modified: Tue, 12 Aug 2025 21:36:54 GMT  
		Size: 69.5 MB (69534318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca1bd83e822024a9d117da13a14b3a145c24ea9b840084531d0af00aae43a92`  
		Last Modified: Tue, 12 Aug 2025 21:36:43 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be8167ae18353149969ac640560f77f5060b79e3bd3f37e205a43effdd23725`  
		Last Modified: Tue, 12 Aug 2025 21:36:44 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c6f5b2993430147eddcae4ac543f30f2e469fc3a166c273fbb661f0f65e04710
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5127123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3a56b8edb52df51ca14776e5d4515343a72d7406b9e9da706ae28c86d2228fe`

```dockerfile
```

-	Layers:
	-	`sha256:c893cd2869a2d7ed251ec0dc2d884c59360027b675c1154ba16a22e905e7077f`  
		Last Modified: Wed, 13 Aug 2025 00:36:48 GMT  
		Size: 5.1 MB (5111244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8b9f4b85ad28eadea50bcb42389e1c15598fac1f40eb55319a8fefbbf84779d`  
		Last Modified: Wed, 13 Aug 2025 00:36:48 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d4fd59e6b261e8e79929ac031055b5761e8ce2a65d672db99c50fcbeee73ef72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (241030113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0883cad2bea1f4ca012d316bc024513532682262d83f7ceaaa7eab8f295a4c39`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e5db16cd1793d2e7d629b8fb75631916886e6ddb1093feb2a3d3d91cf057dfc`  
		Last Modified: Thu, 14 Aug 2025 17:05:23 GMT  
		Size: 143.5 MB (143542131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52cb144b733f24e572300001ca71f159856d560ab0d2a6282e6856d4baeb4d7`  
		Last Modified: Wed, 13 Aug 2025 14:27:36 GMT  
		Size: 69.4 MB (69404942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8d0ebd4811480d5463153653f6cd12fe17e48f4e5e2ea9982fcb95283d1eb9`  
		Last Modified: Wed, 13 Aug 2025 14:27:07 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9e64d632df3a29f403c3df6342b8614436d02c2e5a1abfdd27761923e8f7ce`  
		Last Modified: Wed, 13 Aug 2025 14:27:07 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3fc4146dc0faf9378eba3e26c0b08c5dee057f2fdbc66361f288b3b0f09d9bbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5133002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d6613f988e672a566da59d204651c25497fbefad87f49920834812394dc9828`

```dockerfile
```

-	Layers:
	-	`sha256:920b04498a6f7a75c2e32a6c77ff798c489446813b056b674159d6a3eeb73ba0`  
		Last Modified: Wed, 13 Aug 2025 15:37:02 GMT  
		Size: 5.1 MB (5117005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a62bec53db39dfde1ee56ef191ded5bd9c200c2b5242551883d2dc152c585a0`  
		Last Modified: Wed, 13 Aug 2025 15:37:02 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:37d38bf04bce31e83719d520aadd8a4fc90ca4f13c3ed49edd9e5310c07dea73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.8 MB (251808623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3f22ffc59c10684f3750ffdd0831e8a3b4fb710b943f65610c212132f391930`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71387f6064ed50c9f88693cf2daba57ea2b9dc027607d8ba070bfc970506f513`  
		Last Modified: Wed, 13 Aug 2025 19:48:43 GMT  
		Size: 144.4 MB (144372854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15c21121507ee8c6a7f156214ab796c940bbdadd5867ccca43bb00e06dad447`  
		Last Modified: Wed, 13 Aug 2025 19:57:48 GMT  
		Size: 75.4 MB (75361308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d1b3ab6850e9cd151d608b435bed7d754496e44744b98d98be5a8eed8d9ed7`  
		Last Modified: Wed, 13 Aug 2025 19:57:31 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc671ebca2cc93bf15a7d06319a12fca9baf390614683f037f8c409fcc459a1`  
		Last Modified: Wed, 13 Aug 2025 19:57:31 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e97bcccab7780160538b6cc8bea3ff410375c20880095619854c153f5cff5248
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d50f0d2bd9835dbe7e2c6dc88abaee311d7a952607114355905b111cc3311910`

```dockerfile
```

-	Layers:
	-	`sha256:12355be13103d41eb8845387527524a88ec7c03acda6f26e8e5406567ea25d5b`  
		Last Modified: Wed, 13 Aug 2025 21:36:31 GMT  
		Size: 5.1 MB (5116402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5deff074c63cfdd645f234f63b47802ce741d801d4684f4181a450b43a1c7863`  
		Last Modified: Wed, 13 Aug 2025 21:36:32 GMT  
		Size: 15.9 KB (15927 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:e8382f8e311efbbf50d619079dc2f215575d1da6fa7408c7360552e2c0729a14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.0 MB (229955500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdfa9bd87982a19f031290b1be204fc97a3b537c69e70035317b502f2c5aad06`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628d651b7d84571f6f8df5dc796f9d0438695cf77ad9e0cc56ddd940f61ddbcf`  
		Last Modified: Wed, 13 Aug 2025 18:08:24 GMT  
		Size: 134.7 MB (134724357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718471461e2f4074d0cc1575d41e478da2ffc9c2c5b42e6566f5e1d46e5b6971`  
		Last Modified: Wed, 13 Aug 2025 18:09:35 GMT  
		Size: 68.3 MB (68342262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d3fd9b6381bb773aeafe4ead0854155f2531a663c2f3c4cdce140a808d42d3`  
		Last Modified: Wed, 13 Aug 2025 18:52:29 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2244ac5dc97f1c79eb943819104affca79763e69c544b6abf160dc1a43e6ef4`  
		Last Modified: Wed, 13 Aug 2025 18:52:30 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ca4a92670caaf0f5aeecaa957bbf6ed80543566fe6d20bda4ee3ae7f792dc018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5118444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54b2b93914d5f07fe0e2e47c5552abeeae2d033b95385483d892a56c3b85f1b8`

```dockerfile
```

-	Layers:
	-	`sha256:918b9cee598ba829e517879d63b5138b66c4c9e332b07dd8835077452e62eefc`  
		Last Modified: Wed, 13 Aug 2025 18:35:37 GMT  
		Size: 5.1 MB (5102565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f23d6ea5eec98e7353e8df5dbbe745ea2f220c7243a48980de78fddf909f3ac8`  
		Last Modified: Wed, 13 Aug 2025 18:35:38 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json
