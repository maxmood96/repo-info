## `clojure:temurin-21-tools-deps-1.12.5.1654-trixie-slim`

```console
$ docker pull clojure@sha256:8d5058d73d6097e877f909ba0304dad30d42ce48fca6553c3ab375399aa24d2a
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

### `clojure:temurin-21-tools-deps-1.12.5.1654-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:274cff97296def06d1cbf3f79ed24d8a25ba57fc829cd36a8a1ae886640b0dfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.9 MB (256899845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:070d8810347f19560fa126ec9037c892be72656cf071076756f4740c7f0e4fcf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 17:46:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:46:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:46:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:46:45 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:46:45 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:47:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:47:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:47:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:47:02 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:47:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4bdc0441c04a489a83bcd641c3a352b08734b2c7e058a7da17b2897d4e9d72`  
		Last Modified: Thu, 04 Jun 2026 17:47:25 GMT  
		Size: 158.2 MB (158166958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac02a3efb8d2838e331dd496e22ff21b0b876fa7145dbab5ca45b5fdd0a2919`  
		Last Modified: Thu, 04 Jun 2026 17:47:23 GMT  
		Size: 69.0 MB (68951914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd9cef1d819f1a29fbcb31abff7f46b3553b3b37c9c22c94f5e77cb268195f5`  
		Last Modified: Thu, 04 Jun 2026 17:47:19 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e82926e4aa562510cb7984479c2ca3e1b9be0f231c398afa4c0d4fb99be02d82`  
		Last Modified: Thu, 04 Jun 2026 17:47:20 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.5.1654-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8854e6d6d788cf7fce152569c07edd00cefeec6b3df73891478947e6bd449ca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4acb934ebd7978700e630174eaf6ac298a32237e62aca75ba922d23afed750d`

```dockerfile
```

-	Layers:
	-	`sha256:8cbe4bebb5585e895608b7d7deb8fc1278fa18574031a83ae1e7cf1b2c0ccb20`  
		Last Modified: Thu, 04 Jun 2026 17:47:20 GMT  
		Size: 5.3 MB (5259094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:594de9fe32f9c32967100bac1d1826dbd42d3905a987cde448d37f66d78fc1a5`  
		Last Modified: Thu, 04 Jun 2026 17:47:20 GMT  
		Size: 16.0 KB (15966 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.5.1654-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:78641623cc5217c9467fc2a06244895a131f41368b6642020d43ada2980f6f4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255382079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:161b73cab9903b64272f0c04325248ef4cb3b2961a73262388b8d8b8a45848d8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 17:46:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:46:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:46:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:46:35 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:46:35 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:46:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:46:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:46:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:46:52 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:46:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a62a55de9f11a64e74db6cf492dd448c99dbd7cd12fc8887d862f1c261aac443`  
		Last Modified: Thu, 04 Jun 2026 17:47:16 GMT  
		Size: 156.5 MB (156461324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d49762cc0569ca66dd85896f59d37281d761d93255903a4594375f6a6f76282`  
		Last Modified: Thu, 04 Jun 2026 17:47:14 GMT  
		Size: 68.8 MB (68777792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34b7e9e19c806e06dd2481937bbb0ddda3fcd3480f1786ba984d4d7466bb2dc`  
		Last Modified: Thu, 04 Jun 2026 17:47:10 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b86bb859a6641d06153a9d4f20356117b36273f9950ae351468c5c30b474e5a`  
		Last Modified: Thu, 04 Jun 2026 17:47:11 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.5.1654-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2e3d15b57fa9a5a1cfd1dc36e0581e6b4b33c0e536350208681062f739e7eb97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5280939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63fd01044e88cc80514853127b0e33a1bec1bd77a2245fd9e729c4d4ecfe3151`

```dockerfile
```

-	Layers:
	-	`sha256:9c99a60ac49601f2dc813fc86d4d0a49c674de9b3159d1b78d955f6587ff56a0`  
		Last Modified: Thu, 04 Jun 2026 17:47:11 GMT  
		Size: 5.3 MB (5264855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b71677402e82d7826ffaf4461ef52d427f3eb386be94233e2598cdfbf9243be`  
		Last Modified: Thu, 04 Jun 2026 17:47:10 GMT  
		Size: 16.1 KB (16084 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.5.1654-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:a01bfd9d59b4cf0455193e6a1c3e5e9444479e6fe141f0f15e75f8201b144b4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266313644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:099180edd6edee4606412cbd538aaa940b0be286b618e1c1c41e0908294d4c0b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 18:02:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 18:02:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 18:02:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 18:02:28 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 18:02:29 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 18:03:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 18:03:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 18:03:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 18:03:18 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 18:03:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f96ab628163acfc4a897a60446de4136b4548cd3582a46ae52f4ea4f52f11fa`  
		Last Modified: Thu, 04 Jun 2026 18:04:09 GMT  
		Size: 158.3 MB (158343238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10ed3da1976ed5eebf23a34a41b2af1b8dc9f03b26e348f06b252890f603b77`  
		Last Modified: Thu, 04 Jun 2026 18:04:06 GMT  
		Size: 74.4 MB (74368907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499ddccba19f12b218f6fea3723687672453a34cf0eaa033a07520e5ed31ae1d`  
		Last Modified: Thu, 04 Jun 2026 18:04:03 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea57d62e98e2e672ad6a830b006e5a8298b3d5091337d29685a21f131a31a179`  
		Last Modified: Thu, 04 Jun 2026 18:04:03 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.5.1654-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8d52d7be53c3a377ce2a5bff3df0b11ee52254907e7dcc66da9a9c91096f639f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d7d72eb62d1b105d15472019ad618b7b5256246381be0d76afdf285781635a`

```dockerfile
```

-	Layers:
	-	`sha256:5b73106c4b619db73797c21cefaf18fb5f440728f395f0c358b229d1543567fe`  
		Last Modified: Thu, 04 Jun 2026 18:04:03 GMT  
		Size: 5.3 MB (5263465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:822b855110fc0e4307b0466ec23bebdc94d6bf9bbeac99b355a681ec66d449a3`  
		Last Modified: Thu, 04 Jun 2026 18:04:02 GMT  
		Size: 16.0 KB (16014 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.5.1654-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:b69f8a5cc9bc341a9a6f8f95552954b8f8e811387547ab462feb4f0e8f4fd049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 MB (247167931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1105cf7be50c81fa6a5e2cfb50226786b266efba1113878cbc77197b97eeb052`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 17:45:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:45:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:45:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:45:12 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:45:12 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:45:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:45:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:45:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:45:30 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:45:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3a7bf300ab749fc8aaa5ec872160f889b9f1fd11db31bb5e8fe4d9ec131347b0`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 29.8 MB (29845924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faff6f57917867a2aa876424deab51d8dc979a79045181c82b1e608268638232`  
		Last Modified: Thu, 04 Jun 2026 17:46:02 GMT  
		Size: 147.4 MB (147388349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc1dca23c0ab14344a0d0eafdaad2d145f8d737569c6a37102e7700a310c9ce`  
		Last Modified: Thu, 04 Jun 2026 17:46:00 GMT  
		Size: 69.9 MB (69932613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8832d668e8524baf6ee6690dcce0bdab58fd5f4950ac5de864771cda41eea871`  
		Last Modified: Thu, 04 Jun 2026 17:45:58 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7de4169569df0d3e58cce60d7e91e2e2c72d858c6dc533f8e91e25c2fe2efd9`  
		Last Modified: Thu, 04 Jun 2026 17:45:58 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.5.1654-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:87c30bb7d6b588f3e23eac8f1051d5bfb6f4c5ea01e2aaa969544bc867c158bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5270984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f51815d7fb012f462ef8b3f229338b649006834dc0c788fbcba8ce9af68c044`

```dockerfile
```

-	Layers:
	-	`sha256:9965b80b58acf6967039271619c98beb28baf317aa6c7fc0bc21cf85110c6cec`  
		Last Modified: Thu, 04 Jun 2026 17:45:58 GMT  
		Size: 5.3 MB (5255018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:967762c62bc4a91e886febfd8d05e6859560af15f9462b985c9bf0a1f0e8ce80`  
		Last Modified: Thu, 04 Jun 2026 17:45:58 GMT  
		Size: 16.0 KB (15966 bytes)  
		MIME: application/vnd.in-toto+json
