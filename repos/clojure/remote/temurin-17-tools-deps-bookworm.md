## `clojure:temurin-17-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:1c35b8d5ec028d5b1f239a7c5e9ae48c39904c37adaecf58e34f85a0b503d4b5
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

### `clojure:temurin-17-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:376de66385b5991d10f4fee847b6fa2be2a6cad633b4167b8f033e7b63bb0f01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.5 MB (274476135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c52a7201392102be2934fc4faba5c35d2c3c3e4db1397e95bfa062a0fd2f1ff2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 06:09:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:09:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:09:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:09:42 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 06:09:42 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:09:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 06:09:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 06:09:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:09:58 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:09:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724d11414d0d30c99b8dc319686d437de16c1afe28eb16f6624c4b313f9ab728`  
		Last Modified: Tue, 18 Nov 2025 09:32:28 GMT  
		Size: 144.8 MB (144847946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1cdfa4e235cf961f4c9c1c619a228dd21bdddcbd84678daaf3537e8aa69d1f0`  
		Last Modified: Tue, 18 Nov 2025 06:10:37 GMT  
		Size: 81.1 MB (81146387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66231224dc2d3d6a1eafa2691eb893b463af3d4be93f77c4f04121261489882`  
		Last Modified: Tue, 18 Nov 2025 06:10:29 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e519cea073d6baa75584b9e1b9b33fd63534c93ece03f403f56edfd339e79351`  
		Last Modified: Tue, 18 Nov 2025 06:10:29 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f978a3dd8fbebe591463e4409b198f550c20e6b4fc305282c8bce0569fef57ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7390670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b120bfe263e1c60751d016a2191253f456f3213e7f192a1377322239d11808df`

```dockerfile
```

-	Layers:
	-	`sha256:122a91ba8d555808ec32cae6c76571cafbee87834b4755d984b2375bdca0add2`  
		Last Modified: Tue, 18 Nov 2025 07:40:28 GMT  
		Size: 7.4 MB (7374892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f421fb504b4b97ba54764ed86c0492e99d7351f59a5c8b3eef6b5e6e935c21db`  
		Last Modified: Tue, 18 Nov 2025 07:40:28 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:de7b38a1ac969b564a223cfebce1f6c709433fc953ebaee66181a09b346d3686
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.1 MB (273070417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ac2baf6ea0993fe2fea61352e0cb77755f1ffb28abb8eff2dcfcec3f4821e4f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:00:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:00:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:00:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:00:50 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 05:00:50 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:03:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 05:03:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 05:03:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:03:40 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:03:40 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d3668e2db51bce474c7b67ef499fc8f66561e8fe5a79c3084c8814e154e54f`  
		Last Modified: Tue, 18 Nov 2025 08:25:25 GMT  
		Size: 143.7 MB (143679921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d10512412261d23026315684af899269d51ecd5217bef7b5c8f41faf0b8c16`  
		Last Modified: Tue, 18 Nov 2025 05:04:12 GMT  
		Size: 81.0 MB (81030319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82edf88603b99f4f934350cf78d8d6e3edabce8a3a14b3592ac7b8aad1bc876`  
		Last Modified: Tue, 18 Nov 2025 05:04:05 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e8025434aa0e5aa173eeaaad34a4c61c4376633364ba3386072721b214534b`  
		Last Modified: Tue, 18 Nov 2025 05:04:06 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c556fa0e8d21d3252bc7529388b8dda1550a1afae2a171ee193df09d7683493a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7395749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ab5dd47019fbff199193ae88f3de629a36ac087fdc86a15e75e90d09348e9a`

```dockerfile
```

-	Layers:
	-	`sha256:9974dcbe657605a6b4d378ca780cab36909c7e123a4b6cac6873f10c85b2a72b`  
		Last Modified: Tue, 18 Nov 2025 07:40:34 GMT  
		Size: 7.4 MB (7380655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37fa42663259cc4a328904971089ff559460177c59a3c11d10c09bc8085e9e77`  
		Last Modified: Tue, 18 Nov 2025 07:40:35 GMT  
		Size: 15.1 KB (15094 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; ppc64le

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

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

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

### `clojure:temurin-17-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:b22d19f11006451226491bf5cec3cf1a80a587d202abb5805ea06f0726d0efa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.0 MB (261954316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b6a0b7971dd12661a64a304c9f3541281ceff7047b69591fcb2952101975e6d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:25:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:25:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:25:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:25:48 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 05:25:48 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:26:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 05:26:03 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 05:26:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:26:03 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:26:03 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:784b9caf46c66ff55a92c27127d39febf2385f329efae62bb4e65b91f3751223`  
		Last Modified: Tue, 18 Nov 2025 01:11:06 GMT  
		Size: 47.1 MB (47137641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cffae098e23cf109be27a5b5ecccbc864970c575f510e26bf08231e0395f8de`  
		Last Modified: Tue, 18 Nov 2025 05:26:40 GMT  
		Size: 134.9 MB (134859044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:983edd389dc2994d20dc490a2fd3a32fffec2ff629c23afb368d1d5620a68cc9`  
		Last Modified: Tue, 18 Nov 2025 05:26:54 GMT  
		Size: 80.0 MB (79956593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ee42b3a201caa4f1ea44bafb75a9624498572786dca9ab47f76b907d3dc9bf`  
		Last Modified: Tue, 18 Nov 2025 05:26:45 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44143f0432cf4e1caf01ab36587ef04149c25843c8adb8f356814594ef50b99`  
		Last Modified: Tue, 18 Nov 2025 05:26:45 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f3339e7bbaa21e84b02871530e33192c5dd02870a1c4db6f5f42ee850999c20a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7381989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d7478a194777415d489a9841ffa58b57c568b59b4248540befd026fb44097de`

```dockerfile
```

-	Layers:
	-	`sha256:f4bf4f235592478e8b7ef80ad0c5789f6f069aca7f3befc7c5c294b6e93eb796`  
		Last Modified: Tue, 18 Nov 2025 07:40:48 GMT  
		Size: 7.4 MB (7366211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a161e82079b5d5b867308090b4ed17bb086590c42b10fd914686411d598ed33`  
		Last Modified: Tue, 18 Nov 2025 07:40:49 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json
