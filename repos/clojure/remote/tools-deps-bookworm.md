## `clojure:tools-deps-bookworm`

```console
$ docker pull clojure@sha256:9e54bc54365e5d97e62bc80c45b319df4c8065dc5a599f90625561e93492597b
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

### `clojure:tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:82b133bdea86dedc131e3709105ea22e98ca54e987cc43f301fced91c0b914ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 MB (287122732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b7bf3ec0f50b3457a0a96825f62a8a321aec05d895c28498ea091a3bb955de7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e78cd354fe4b3fed7295da6ea1671d0fa79052733bf807863822f394cd598a`  
		Last Modified: Tue, 01 Jul 2025 06:52:48 GMT  
		Size: 157.6 MB (157634503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bc2f0a825070aa7c8ab3971f59e2b4f100714ad969ee929b04a5f7f8f10ec4b`  
		Last Modified: Tue, 01 Jul 2025 06:52:44 GMT  
		Size: 81.0 MB (80992905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c2df9bde9d640dd6555eca2e8479831387c343ba17d115ed516840ff25b995`  
		Last Modified: Tue, 01 Jul 2025 03:45:16 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2631f633b64eed753b565bfc70f5aeebdd05d429a69e594e662131b13cda04b`  
		Last Modified: Tue, 01 Jul 2025 03:45:19 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:dedc6ed49f347c1a39ede5ea20ef4de8f8b93089c8ecefa9e0dbb8529ab98341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7391191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6556488f2e126052af04b78753bd90ea3d3e6c7f76e3963db7ac026c1729b4b`

```dockerfile
```

-	Layers:
	-	`sha256:762584053f7524b62cd92940590dd750293c57fce99ce1b750e1edbd480c72e1`  
		Last Modified: Tue, 01 Jul 2025 06:38:40 GMT  
		Size: 7.4 MB (7373370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6f006205f22851cd9bf62c88311b704e8bc861f57199a6ec3b2a23d3792b9a2`  
		Last Modified: Tue, 01 Jul 2025 06:38:41 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3949dc92c27d15ee0d29aecd0288cf46258ccbe1e52afd4ca4f3e41e1014a6a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.1 MB (285117012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9e9ddc430ee3abb832d0810ce6a748daa6e764da426a450fe822e3cd283faac`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:8fbf1dd6492cb885c9004e9e7ecb0880a823cd140e63f4b13dfc1bc4d0d3e37b`  
		Last Modified: Tue, 10 Jun 2025 23:26:40 GMT  
		Size: 48.3 MB (48338852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2c862dd63a0f06c6065a1f9eebb4c4c8659cf987595881d27397c18e9bfa45`  
		Last Modified: Wed, 11 Jun 2025 10:01:03 GMT  
		Size: 155.9 MB (155928834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf79607a6c72b41cd02f016b0072fbb43652314475655aaef94ab35feaf2ea7`  
		Last Modified: Wed, 11 Jun 2025 10:01:13 GMT  
		Size: 80.8 MB (80848286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f8affce2492591b9f679baf0040545186501ba1bf6d5553766c0fb22e10c3e`  
		Last Modified: Wed, 11 Jun 2025 08:38:06 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5e85bfbf785f086e58debb89435789db853baccc105dde551449fc19d5082d`  
		Last Modified: Wed, 11 Jun 2025 08:38:09 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:5e6f6a66b69d614e3de9b7a2ba7b820f774fdfebf57e93de6a72fb83d94c3471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7395860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8ff1d45df3e14fd18cca533935ef928cee510f18e9ca07d2749d78da46118b2`

```dockerfile
```

-	Layers:
	-	`sha256:8ade275353c4e98f242072cbbfb44e08232067dd8c84ace42f0c329e73ee34fc`  
		Last Modified: Wed, 11 Jun 2025 09:39:17 GMT  
		Size: 7.4 MB (7377849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f25c323af4f9d64bf5a3ea60d53489c533f9ecbbbc907eb70c582d42d8d7d203`  
		Last Modified: Wed, 11 Jun 2025 09:39:17 GMT  
		Size: 18.0 KB (18011 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:55b6680b512d3289c6ba218fe5682ae70590cb3efd7ffff7a37ec5287b8206a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.0 MB (296956738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c7ecd2e08be9f019f46b7be524477cfa69bb929eab7f7f7ef34711268598264`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
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
	-	`sha256:65d348c3abfb8493d4b77022d58f0afc8e2daa19b2af853f803aef5c836212f9`  
		Last Modified: Tue, 10 Jun 2025 23:28:11 GMT  
		Size: 52.3 MB (52337357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1fb7b706e33450e2c71d962a90e76d5c561e452adcf3efb6e0854003cbfea8`  
		Last Modified: Wed, 11 Jun 2025 10:01:43 GMT  
		Size: 157.8 MB (157804908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e1a871fad7c34a94ff89bd5b20650cd24812c7f1d9461f51523a89cf05c65a`  
		Last Modified: Wed, 11 Jun 2025 08:46:16 GMT  
		Size: 86.8 MB (86813428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c630c2a6c54cb01f7cc47a8a9a1a9f6c8605764299d5dc28ec1cbb0595dd7273`  
		Last Modified: Wed, 11 Jun 2025 08:45:58 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c359bac505d688c88f4beb4851ee89d2dfea25480f3ec96dba12337eaec9e486`  
		Last Modified: Wed, 11 Jun 2025 08:45:58 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:6202acd3b3ff090b60109fa4519ad074876d4719cbb5f7b4f986910cb8b4e7cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7395159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93afbcc7b77c11a1823f96d02dfc824318adf522c9cceaae439a8fe6ef78b506`

```dockerfile
```

-	Layers:
	-	`sha256:25f028f9a574219520e15e953056eb101a703fc225ae8503f8614db5450ebb82`  
		Last Modified: Wed, 11 Jun 2025 09:39:23 GMT  
		Size: 7.4 MB (7377254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f55919cf365e82462de6be18278cac384738f2449ba953ac8d820b6bc208156d`  
		Last Modified: Wed, 11 Jun 2025 09:39:24 GMT  
		Size: 17.9 KB (17905 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:e746db3e22716327864e65059deb60a1eb8a63fcbe94eabf449d0f7d08f59cc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.9 MB (273864088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a4ba8284bc4f69d55e63959acd1c91972b2909555aef52d9f70fafb7702d8f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
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
	-	`sha256:92d876c60c42d9677caf30587cba2266fe6860ddc50efdd0a6fcec154e589f76`  
		Last Modified: Tue, 10 Jun 2025 22:48:13 GMT  
		Size: 47.1 MB (47149408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda1d40bcba3d4c5b290c8a74ba0b4bfc95975ec2a23ad75658cd28e277e6baf`  
		Last Modified: Wed, 11 Jun 2025 07:02:00 GMT  
		Size: 146.9 MB (146911003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00daefb7d687a91e318b16b9c1b635a7bd53f6349d4a75495f9ef6c8a30fe7f6`  
		Last Modified: Wed, 11 Jun 2025 07:02:07 GMT  
		Size: 79.8 MB (79802636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54535089bc5a0ebd19412f776b37612e1336fbf15d98b201ced1736703e3d6e4`  
		Last Modified: Wed, 11 Jun 2025 05:53:58 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe0e2775354ef3c08ec3d2ee064a0cb638c1ab001835e39d2f7a6333ff2f5c5`  
		Last Modified: Wed, 11 Jun 2025 05:54:03 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:a1354e245c8517863555a852e32673fb76796cf554b6696f80f6bf9c3ef3db0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7381153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4cdaa4075dd3749f34df080f725d6278a930315a1b7a2586190963a629aa3e1`

```dockerfile
```

-	Layers:
	-	`sha256:264c52cddfdb2eb5e0cc6dfe35676f31cf5fe29e9bea5595966b60cf9e888c08`  
		Last Modified: Wed, 11 Jun 2025 06:37:41 GMT  
		Size: 7.4 MB (7363333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07a67f6c9f91024a09aa321cd16c1eb882ab93d3fd2c149954f9820c8bb8fcfb`  
		Last Modified: Wed, 11 Jun 2025 06:37:42 GMT  
		Size: 17.8 KB (17820 bytes)  
		MIME: application/vnd.in-toto+json
