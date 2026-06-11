## `clojure:temurin-25-tools-deps-1.12.5.1654-bookworm-slim`

```console
$ docker pull clojure@sha256:f2b24bec835ed7309e2dc68cfaa0bacb886ea3ae901661e1f2c48d30864b251c
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

### `clojure:temurin-25-tools-deps-1.12.5.1654-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d3a32046da7b1a70d04fd08d344367a9341fc90ab97fff4e24e5d86d9399f9ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.5 MB (187455813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa67943d03ab81a34dcada0f766853193d78cd1aa4438d827ac17cda2ddfbb93`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:20:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:20:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:20:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:20:59 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:20:59 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:21:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:21:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:21:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:21:13 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:21:13 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93307550f5e3c2ccda48767a423b465ebbd7176b8e832c68c4cbc20bdc9a578`  
		Last Modified: Thu, 11 Jun 2026 01:21:35 GMT  
		Size: 92.6 MB (92574574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f3f7f05ac4dc60e038da5f38cae82285800c16d49615585a00096186060a383`  
		Last Modified: Thu, 11 Jun 2026 01:21:34 GMT  
		Size: 66.6 MB (66642574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ddd1dc7938c513c2482d289827cc57b865572ca50b1b5b2d853ff10d73dec6`  
		Last Modified: Thu, 11 Jun 2026 01:21:32 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d257faec7b12c6c87d7de4cd1e9b03dfcec04bfaca14aecdec3c9c2fcdcdd15`  
		Last Modified: Thu, 11 Jun 2026 01:21:31 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.5.1654-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f3b254f7033540c73cb34d8ca3f1ae88e91f2db9f1c7ebe339ddcb9df11f374a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5098768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b3c1b4603b5c47c13d384eca13e324702b0551a586be4d51377a6610eb5711`

```dockerfile
```

-	Layers:
	-	`sha256:ffe148d65ab0ea80a539550782bf340bae5c148566ddd0c9d12cbc1fae9fd42c`  
		Last Modified: Thu, 11 Jun 2026 01:21:32 GMT  
		Size: 5.1 MB (5082089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86ce7a12b911643ec1a062ed9dc643e503db02fc19038d949fe50090dadcf40d`  
		Last Modified: Thu, 11 Jun 2026 01:21:32 GMT  
		Size: 16.7 KB (16679 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.5.1654-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:71bf0308a03e4d4a3433aad14d59d00a37a958196e3e29e6ca74c662fc31609f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.3 MB (186308872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efc5d1ead6496b64c5d98f5c82f45675fc17b193a464f19dc59c81aec8b0c39c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:25:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:25:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:25:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:25:05 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:25:05 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:25:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:25:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:25:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:25:19 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:25:19 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6eaf881cd87167af7048a480d7a8eb2893d7997a003316284b3a6e42a2cd1dd`  
		Last Modified: Thu, 11 Jun 2026 01:25:41 GMT  
		Size: 91.5 MB (91542295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:453c6e4abab1fe9c1e75ca9bde3f11fc02a6176551343963373d9dcdee441f98`  
		Last Modified: Thu, 11 Jun 2026 01:25:41 GMT  
		Size: 66.6 MB (66643233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2049733cfa22de99832f57d687474f2b7e476623dfeb55a40f37540c2ddef72`  
		Last Modified: Thu, 11 Jun 2026 01:25:37 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76e6815dca28c55fe3a239deb7ef6707057f97601a772e1b80825c528e846af`  
		Last Modified: Thu, 11 Jun 2026 01:25:36 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.5.1654-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:116caaa68a8531c793fcc8d3b8a5a1fd54539dd6b9079b3deede8198b5a6310a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5104692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b6db16c7c387fe231506b6fd424c9e8e5e4e0ed5132cd833d24ad0f25069814`

```dockerfile
```

-	Layers:
	-	`sha256:508aa6af9345343370af92d9fb74645a8aa7bb7c8968f38a6d57e0a2d872d9bd`  
		Last Modified: Thu, 11 Jun 2026 01:25:37 GMT  
		Size: 5.1 MB (5087871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7caa6e67a20e342f89ecdb438f5ca759519697abb0fca2778f6e9ba1c6553fe`  
		Last Modified: Thu, 11 Jun 2026 01:25:36 GMT  
		Size: 16.8 KB (16821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.5.1654-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:3aa592718e4516c74448df2b9113be1f46ef4e693d9913ea616461969b9484c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.5 MB (196473227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4fd68ee836406c5c02cd3b246c090a7297f15cb1475d9f770359a11a115afc0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 09:44:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 09:44:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 09:44:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 09:44:03 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 09:44:03 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 09:47:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 09:47:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 09:47:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 09:47:48 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 09:47:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:23f7cdee3ef2598b081c2b848fee95730a7ab2b1cc5b726c72dcb8c2fe3632f7`  
		Last Modified: Thu, 11 Jun 2026 00:21:33 GMT  
		Size: 32.1 MB (32081941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982932670843cfc9826334cdcfb7557104e8613cbf39950f8bd63bcb7d5d496f`  
		Last Modified: Thu, 11 Jun 2026 09:45:18 GMT  
		Size: 91.9 MB (91914010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b50c285dec66ce85e665f70ef7bea9f68cb8a4bba3541c8462ff92cdc63ff1`  
		Last Modified: Thu, 11 Jun 2026 09:48:20 GMT  
		Size: 72.5 MB (72476237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf710c46e47ae54296406acfb45eb4efcce917d383788a0c676e88e8b2d3bf2`  
		Last Modified: Thu, 11 Jun 2026 09:48:18 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c14b04b6444897eb6441b6f0d961cc1f5dcc6e7291dbcbd75f298357100a2bc9`  
		Last Modified: Thu, 11 Jun 2026 09:48:18 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.5.1654-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6a09805164b352090f777f0d45fce8a316463a433336e61d5d2624e606ca33b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5086355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec1ef3aee0c787fc1fd6ec04469f188ede8a8711efe93975937de3d4510f59c6`

```dockerfile
```

-	Layers:
	-	`sha256:a4a47040331145929fc441a911d8b725c6874476d930d6c2182f608ccc244fe8`  
		Last Modified: Thu, 11 Jun 2026 09:48:18 GMT  
		Size: 5.1 MB (5070571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43dd7ad8f6c5c0e16645e6e163885baaa2294d7270527af08807a364e7b83f66`  
		Last Modified: Thu, 11 Jun 2026 09:48:18 GMT  
		Size: 15.8 KB (15784 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.5.1654-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:15b4a42290b7e67cf7c76ea13f7893a2f24c532206cd28187f713627baac10ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.8 MB (180767034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1a5cd6eff88efc89032d5ca40551a571211d35939aa23464d885f2c4c4512e2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 03:13:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 03:13:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 03:13:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 03:13:15 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 03:13:15 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 03:14:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 03:14:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 03:14:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 03:14:32 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 03:14:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6483bebe0f30256cfdd9c6f96373508f6b33d18b4bc61668ee641c700aa3108a`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 26.9 MB (26893508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d5d28a9b892aa865b958e34a0eeffbccb54b6231b8f8f42d3512025b674cad`  
		Last Modified: Thu, 11 Jun 2026 03:13:56 GMT  
		Size: 88.4 MB (88420320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63640ea60cc6772cc5442e2c2bd963f4d2bd6b0bd84398aaa5138ad1e37b7433`  
		Last Modified: Thu, 11 Jun 2026 03:14:55 GMT  
		Size: 65.5 MB (65452167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3deaab0b5f498a9d1bffc7ecad2c27fdc21c980491a9a72bf51b9c9403adf92`  
		Last Modified: Thu, 11 Jun 2026 03:14:54 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbb728e5f40ba84571e7e8eabdeb7c00cb50f78229a816e28b5fc9917749fd0`  
		Last Modified: Thu, 11 Jun 2026 03:14:54 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.5.1654-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e4da892a976abf3943dc52ef3f8dba39a4bb5ea246e15a1e6f2ba3f01e6b9d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5074651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:709db59cb569acdc65cafb0fd668d94192c5f4d8e20160eece248a6cb9e76f31`

```dockerfile
```

-	Layers:
	-	`sha256:6106c08a4b114ab1767b62a250dc565f945a816f34611f65f7eb3eb14ebb03e7`  
		Last Modified: Thu, 11 Jun 2026 03:14:54 GMT  
		Size: 5.1 MB (5057972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e35964e4dffdde3bb6d48a94897275f8f271055b802adf025f214aa93c205a87`  
		Last Modified: Thu, 11 Jun 2026 03:14:53 GMT  
		Size: 16.7 KB (16679 bytes)  
		MIME: application/vnd.in-toto+json
