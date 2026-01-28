## `clojure:temurin-11-tools-deps-1.12.4.1602-bookworm-slim`

```console
$ docker pull clojure@sha256:4c1da30193bf7d3f30ea319f9dee30d1ee241a9f7338187d0bed714d4d2fcd33
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

### `clojure:temurin-11-tools-deps-1.12.4.1602-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2a3873b38412244ff3f10b587173d50db17fc7bcf4f8e6c9132b7c4e3d2f5543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.9 MB (242873394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6197c7613f6b62050a5f551605fb21611608d18872fa07789ffcbd2bf723724`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Wed, 28 Jan 2026 18:03:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:03:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:03:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:03:38 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:03:39 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:03:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:03:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:03:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13bced876324091c226aba805b77309f3a392babf4cebf699161f605fe29da1e`  
		Last Modified: Wed, 28 Jan 2026 18:04:13 GMT  
		Size: 145.0 MB (144966652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed9629d3e794a0833b3e740bf5eb406e05c81350578a1c09f8dec94cf74e870`  
		Last Modified: Wed, 28 Jan 2026 18:04:11 GMT  
		Size: 69.7 MB (69677525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef95790a014615768a09c8d4137f28fc51e8e67dceb6d5a805b594f1a6354b26`  
		Last Modified: Wed, 28 Jan 2026 18:04:08 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1602-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f34eba01387e0c1274460dda2c45699d564ebd43ae719ca15d47f0345dea36da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5147808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8196896eef82f0a89ea67c116a030dd02174b993e4d24764030963b15eea1985`

```dockerfile
```

-	Layers:
	-	`sha256:7a2a63148a165a01e4318b19f15fbaf45562fc0df02a47b9fae2ecc4ffe3402e`  
		Last Modified: Wed, 28 Jan 2026 18:04:08 GMT  
		Size: 5.1 MB (5133541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1be3bdbed54523cce976ec4b12adf0950ff271220a26cbfac4568cf6cb5698c3`  
		Last Modified: Wed, 28 Jan 2026 18:04:08 GMT  
		Size: 14.3 KB (14267 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1602-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:aa397c5f7b5641529f382c23e2b3982c99095d8aa95cf30acf2f2039c9506d41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.5 MB (239511155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c210ebfde76e31fe098045533392262e4db889b4dbaee9a3a3def8a0ac76f53`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Wed, 28 Jan 2026 18:01:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:01:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:01:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:01:57 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:01:57 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:02:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:02:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:02:12 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb77da95db9bb8db99ea5a7e5717352565756b8755349eb5f4660bdf3b08057`  
		Last Modified: Wed, 28 Jan 2026 18:02:34 GMT  
		Size: 141.7 MB (141729962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3a8482656e6c400ae7925fa3d4def9b1317e32fdb979acb2eafb5fee11a96c`  
		Last Modified: Wed, 28 Jan 2026 18:02:33 GMT  
		Size: 69.7 MB (69672659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2993d0f516b25bfdb9742a8cc52a7253359ce2eec9c0ce1193ac5b8fe648419f`  
		Last Modified: Wed, 28 Jan 2026 18:02:30 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1602-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:01abc953590e0440d95da8ded18bf9eb25c018bffe8e622dd640f240a88800dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5154304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0653a66f6634cf9c54be0a91b63ff4a46c0fd4b39be9f41ce02200d641dc64e4`

```dockerfile
```

-	Layers:
	-	`sha256:9b5e0ee211b235330bc9ccdd570ce17c5dcead4dfb0d0aec5470789902b541c2`  
		Last Modified: Wed, 28 Jan 2026 18:02:30 GMT  
		Size: 5.1 MB (5139920 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:835e80baa4123d28f75182c6dcc0c47ecfd59d77c37b8a72265775384baf8254`  
		Last Modified: Wed, 28 Jan 2026 18:02:30 GMT  
		Size: 14.4 KB (14384 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1602-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:c8f1b3f8e375ce81e3935c276c99540d609480b776665d80d9496ba2f9b5b6d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.7 MB (239663384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af8205504045ad1d6793745e4b8f08cab76bf735365473df4cecf2456b0fbde1`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Wed, 28 Jan 2026 18:17:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:17:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:17:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:17:58 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:17:59 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:18:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:18:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:18:41 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:cf92d3bf0add4f20720c3232cd336a7f7f50627989684b748675db0b2f2ce746`  
		Last Modified: Tue, 13 Jan 2026 23:17:03 GMT  
		Size: 32.1 MB (32068709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf0f93939fc5ea33261990501d3d19e6da19c743751c90599b5a9e199b778fa`  
		Last Modified: Wed, 28 Jan 2026 18:19:24 GMT  
		Size: 132.1 MB (132079782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a6fff195ba106420f78922136e8cde854c9a8dd7d0ea8b80ce02c330df638a`  
		Last Modified: Wed, 28 Jan 2026 18:19:22 GMT  
		Size: 75.5 MB (75514249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156a379674c6b4779511bfda3bbb947cd883ed0975fa55c83c8f439a29b42138`  
		Last Modified: Wed, 28 Jan 2026 18:19:19 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1602-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1842d30eb5a1bf76f762eb09da4767dbd7ddf0c38f12ef5648445c7b471b37d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5152399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bca5a41ec4170bb0c5d8eb3dc4b64c1fa4abbd7e2f3da3b00a1554a29e74ee38`

```dockerfile
```

-	Layers:
	-	`sha256:655fda968edd205fa0f05ed8113fe35dfc9d0ded5ec75b9335d01e91a836fed9`  
		Last Modified: Wed, 28 Jan 2026 18:19:20 GMT  
		Size: 5.1 MB (5138084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11c61c1a11f94258ac27e21391bdee527e5ba87a1e8fbd1943d7e5215daf359f`  
		Last Modified: Wed, 28 Jan 2026 18:19:19 GMT  
		Size: 14.3 KB (14315 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1602-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:abcd3f37c23d91d8c2fc74e268866999870801d576b4f22a2919ffec338a12f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 MB (221069857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6a619f7a6947dc05e0f408baf1d3536ca75ed93bafbe31edb00a453b1375226`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Wed, 28 Jan 2026 18:00:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:00:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:00:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:00:07 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:00:07 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:00:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:00:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:00:24 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:08 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e386b8a42bb47760140100fd558903946136489575aa98e3627dbdeabf78759e`  
		Last Modified: Wed, 28 Jan 2026 18:00:52 GMT  
		Size: 125.7 MB (125694849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ec96ba147c1111b84097c0aee4dc9e9ea8744f8089707a70ec32696e369478`  
		Last Modified: Wed, 28 Jan 2026 18:00:52 GMT  
		Size: 68.5 MB (68489950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ad9a63653636b848c87044050e6eb5d4de9cd4d1585dd8af9e07c2ea2b0f4c`  
		Last Modified: Wed, 28 Jan 2026 18:00:49 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1602-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9680280263d37b2da7b3fcad964157a8b747453e54355503db950398e2826489
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5139133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f4bc2e2b040bc9fafcc9e41de497b2475b1a7ce0732b9f1a2eae0145f95af3d`

```dockerfile
```

-	Layers:
	-	`sha256:d5091397b73b16102ca2fa984f881a7e375b9f740e23141b534b414c290b3058`  
		Last Modified: Wed, 28 Jan 2026 18:00:51 GMT  
		Size: 5.1 MB (5124866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b886d7241e93ff78888cd2d996eac6a15c99323c3c289b20a250f353c5fb2d2d`  
		Last Modified: Wed, 28 Jan 2026 18:00:51 GMT  
		Size: 14.3 KB (14267 bytes)  
		MIME: application/vnd.in-toto+json
