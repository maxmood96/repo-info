## `clojure:temurin-17-tools-deps-1.12.3.1577-bookworm`

```console
$ docker pull clojure@sha256:af220b441235ba780e85a1f7466874473d2555b4300a941068a4c0b406753af7
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

### `clojure:temurin-17-tools-deps-1.12.3.1577-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:6177ad48566e534f97cb34cd5205b0f797500b86ba84f40f3fd39579c527c79f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.5 MB (274475754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84a0c26ae756662a1a54245a1b5f6b8fdb062499042d4d696f24864dcd25b4f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:53:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:53:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:53:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:53:18 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 23:53:18 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:53:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 08 Dec 2025 23:53:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 08 Dec 2025 23:53:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 08 Dec 2025 23:53:34 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 08 Dec 2025 23:53:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bf45e9c56c31c00b25ec0ded6c31a5c14de6ffdf972c0b4635e19122614ddb`  
		Last Modified: Mon, 08 Dec 2025 23:54:14 GMT  
		Size: 144.8 MB (144847946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55cd80f30655287eabad2140635ff92e5c092d249e7937f6d5e6c646df9b758`  
		Last Modified: Tue, 09 Dec 2025 06:49:32 GMT  
		Size: 81.1 MB (81146032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a67fee7627f120fa1f0a790ebd429228630faa331d47c8ad0fd54ba136068e`  
		Last Modified: Mon, 08 Dec 2025 23:54:07 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03766e7bd55e255c845560d576036a99427611f1df980365cc3cf464d41922f3`  
		Last Modified: Mon, 08 Dec 2025 23:54:07 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d859e084dda9fc0265aadd40a079f9c3b50c455e30dc5cef81bf37404ff74ff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7390670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f088d4bf3728d9199bd080de0c22798af481b697f0a38b3d3130ebef69f7563d`

```dockerfile
```

-	Layers:
	-	`sha256:6de7498c42a5726338ea92a7a5370db7fb7d2f6eccb6df8e735b637adea3ca05`  
		Last Modified: Tue, 09 Dec 2025 04:39:01 GMT  
		Size: 7.4 MB (7374892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbc999e57cc986c2e1564dfacb2a8717d74a3c1ea85c86c29b0f68f3b0c4ce71`  
		Last Modified: Tue, 09 Dec 2025 04:39:02 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.3.1577-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4d20803d855c27a48678be9f093a499a5841c31058261aaffccf315c4eddc8dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.1 MB (273070754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:963551b95c1b3ac21334894defc236a6e020feb0392e7dd44fe331cf94e0fe92`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:00:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 00:00:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 00:00:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 00:00:59 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 09 Dec 2025 00:00:59 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 00:01:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 09 Dec 2025 00:01:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 09 Dec 2025 00:01:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 00:01:13 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 00:01:13 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7f2b9668af76f73927725e2d1fb5d7224604d8c4c42cb8cdecb502257d9101c4`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 48.4 MB (48359071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f1c1de6f000339346820df8180799beda05986da7e242490c4245da149ce361`  
		Last Modified: Tue, 09 Dec 2025 00:03:21 GMT  
		Size: 143.7 MB (143679912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd164481af0a7195d400c4ce88e0deb01414028e94df76642c378d969a7ac47`  
		Last Modified: Tue, 09 Dec 2025 00:01:50 GMT  
		Size: 81.0 MB (81030731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb736354fce9c7a60e4885f4011d29e055c2d2b5ee9e9c4b76ec5bd0720f091c`  
		Last Modified: Tue, 09 Dec 2025 00:01:42 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9280740b72b50b262da0007d447e79fc3f0ca8fb05463db2545d8bf105871361`  
		Last Modified: Tue, 09 Dec 2025 00:01:43 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b42a49925cc8dbd38575e471bb16fb496affeb92749047fb67c429b46d2fde91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7396551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb8b883474285008ce9d5542f970f11d65e083c1c40cb80bcc168cb422a9a5b2`

```dockerfile
```

-	Layers:
	-	`sha256:a771cf6d3cdc835a897f5e60835a26e081371104d391699c6c9b59f8d555b06d`  
		Last Modified: Tue, 09 Dec 2025 04:39:07 GMT  
		Size: 7.4 MB (7380655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47a4dc102174df40bf32695efe9d4f9d6833065a7a90cc5971b0f91fe61cb4ef`  
		Last Modified: Tue, 09 Dec 2025 04:39:08 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.3.1577-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:a218e5a3b52922b09e8c7727e42a3179dbb35b122844d84a5b0b982aee8777e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.8 MB (283839646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007a9d80ca699097ab419b1ee3f6637e1ff10fe15cdb68224568224325bb9170`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:42:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 22:42:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 22:42:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 22:42:09 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 22:42:10 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 22:44:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 08 Dec 2025 22:44:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 08 Dec 2025 22:44:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 08 Dec 2025 22:44:34 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 08 Dec 2025 22:44:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c088128ea77bb5c706bb00930020ea2fba147060275f49c5a7be6b54af5ca7c8`  
		Last Modified: Mon, 08 Dec 2025 22:17:06 GMT  
		Size: 52.3 MB (52326977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35000cb1964cf20b1dfaf0b01681b83417814d0489bb0ac766df92e26616c6ab`  
		Last Modified: Mon, 08 Dec 2025 22:46:18 GMT  
		Size: 144.5 MB (144525257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84b57f2ce02b1e20d233278c4f341e752e08e68082577e98f1781e21eadd489`  
		Last Modified: Mon, 08 Dec 2025 22:45:34 GMT  
		Size: 87.0 MB (86986374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8027a5152a1cdfe264320bd5706b08d635c926ff2093bd2af75530a346895ef`  
		Last Modified: Mon, 08 Dec 2025 22:45:26 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a49b74421e63fc08c24987f3a30dd979ccd3250c6f0caaa584aa66debc4f9d`  
		Last Modified: Mon, 08 Dec 2025 22:45:26 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:88f3fc604d2b18a885b51765a9379277abcf1c2e648158385d4bdd20c707f974
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7395932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f0d4f1aaf404dbc806b0f56f2e2eb63c0676379038e0c18207707d044f3f7a8`

```dockerfile
```

-	Layers:
	-	`sha256:396c1707b6f487aeb37d5ece8405b33dee17b7c3d95c5eaddf8954475745c130`  
		Last Modified: Tue, 09 Dec 2025 01:37:04 GMT  
		Size: 7.4 MB (7380106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1835daff53806c55f187d9c3e8d7a132e3c8e5e83aa160c655b535f3c59fb5f8`  
		Last Modified: Tue, 09 Dec 2025 01:37:05 GMT  
		Size: 15.8 KB (15826 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.3.1577-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:2786a76da30256a28d613afa0bd4e7399ba3b9acfaa7ef55d255da967ae3dfc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.0 MB (261954424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:027dc02c98bbba9f1a7280f62134adf1ad22d84201ae3a3f0fc24a96904a960a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 01:28:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 01:28:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 01:28:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 01:28:22 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 09 Dec 2025 01:28:22 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 01:29:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 09 Dec 2025 01:29:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 09 Dec 2025 01:29:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 01:29:39 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 01:29:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f1896ba83f603ad81e0d8cb48b496e763b4b781a68efe11f1b6de9da929514ea`  
		Last Modified: Mon, 08 Dec 2025 22:15:09 GMT  
		Size: 47.1 MB (47137665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068f08d66ab2276a2c9ca78524faf8035ccd0094d15e25fe24702ef0fe52c031`  
		Last Modified: Tue, 09 Dec 2025 01:29:16 GMT  
		Size: 134.9 MB (134859062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d64c1bd2ce000969f02ae6f86fa9edb23840d7b4e1346b49dff036248918ba`  
		Last Modified: Tue, 09 Dec 2025 01:30:26 GMT  
		Size: 80.0 MB (79956659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a4bf26692474f6456a09d88aa24a69bb95d682b910a201a8c64da08d30e8f1`  
		Last Modified: Tue, 09 Dec 2025 01:30:14 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:321dfb05be398d479ffe339fc3cc37599543aa45f783fed2763cec8e9e31da6b`  
		Last Modified: Tue, 09 Dec 2025 01:30:14 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:e199dc68a4c31a36cd845746e3a399888731e2c046b31ad7ada9162aba70d3ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7381988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b885c9321cfd95508cd88ded286c7802860e629b3ba440d54bf24d488242daac`

```dockerfile
```

-	Layers:
	-	`sha256:54d0acf0edde98a063083c5eb253430b3ce7f511879d7451025fcd7724f901d1`  
		Last Modified: Tue, 09 Dec 2025 04:39:18 GMT  
		Size: 7.4 MB (7366211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a07b4a3fca9905ad4c8124194ef25a44471ec8a0290ee975798cea1f8bc1ba82`  
		Last Modified: Tue, 09 Dec 2025 04:39:19 GMT  
		Size: 15.8 KB (15777 bytes)  
		MIME: application/vnd.in-toto+json
