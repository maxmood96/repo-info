## `clojure:temurin-26-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:10747e60d34103c600926350eec74d3d391a1457a400e29474e90f9fefdd91ee
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

### `clojure:temurin-26-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3cb6a905ac3bdd1124c559aa785e1c493682fc241332faf24aed51aeac266cde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192496292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b84bd26e690944934573e8a6e80ae670b1fd328560f7758384aef8027f2539`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:02:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:02:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:02:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:02:24 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:02:24 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:02:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:02:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:02:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:02:37 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:02:37 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3286e2ef3f49c62f857382578ae0d11dae4d8aca85e55dbe9624d88d6b14d70`  
		Last Modified: Wed, 20 May 2026 00:02:57 GMT  
		Size: 94.5 MB (94524344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943e8297aa68485a97c22ab820b8d75a266603e8ee2c085fb7ff40b9781204ff`  
		Last Modified: Wed, 20 May 2026 00:02:56 GMT  
		Size: 69.7 MB (69737367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251f6ca2d8ed409bc30f47cae17c5f6fd99198281fc97e7046d915dc14823f81`  
		Last Modified: Wed, 20 May 2026 00:02:53 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a268e7e590ccfb329b65ff44a91ec11f79d91c4c1abe25b0ef0b4b5e1485703`  
		Last Modified: Wed, 20 May 2026 00:02:53 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8bb27300ef9891fab5576d3efb19b7b06723d1dc03cecbe3694f3b8c88b8fa98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5097687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fc9270aed1476579e66ab49c0080f695486fa7544a0233abb1bbe008c265327`

```dockerfile
```

-	Layers:
	-	`sha256:5e0a15dbff5176ee00b9d785d5137a89ccee48f46d4db17a08b8fafaed5f67ff`  
		Last Modified: Wed, 20 May 2026 00:02:53 GMT  
		Size: 5.1 MB (5081705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:850f3129179dd93c21aea4df9e9cf7a6d0fb51516449090198b4116a82be4c13`  
		Last Modified: Wed, 20 May 2026 00:02:53 GMT  
		Size: 16.0 KB (15982 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:519c04288cc8cdf7899f0b778314cd1cbcae3ad5648eb9a62677f3d9581059ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191351809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ca89bcc9efc37df78160afaaeac30add467642bd898276544f90bc0cac867f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:09:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:09:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:09:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:09:18 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:09:18 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:09:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:09:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:09:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:09:32 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:09:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5074b9c6b38380d1dc72e664a68501d3965c6ef85bd7530c46985298f52f290`  
		Last Modified: Wed, 20 May 2026 00:09:54 GMT  
		Size: 93.5 MB (93504348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12fa5bc2fbf2846118b51bdbcca36b83fd2a4de769ee609436f47c15076fb129`  
		Last Modified: Wed, 20 May 2026 00:09:54 GMT  
		Size: 69.7 MB (69731376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d46890db855ec9913daa6a7bc58361909ff27e37ee3b5030a93f7130cdad7f1`  
		Last Modified: Wed, 20 May 2026 00:09:51 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf44e75eaf03136a3fbdc23352832e1ad747bab4ea9ef404c0ce5ab58b0b847`  
		Last Modified: Wed, 20 May 2026 00:09:50 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:82e0ab882e8ab40693badb1c327a63580c1b4b0adf1ecc5ab84fa4dcf2719a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5103564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c38399b1f33314eaaac9c71730139fe80cdde0ca57cb82d7948a013c2fb4b5a`

```dockerfile
```

-	Layers:
	-	`sha256:01c838d15c3da59da562fe9b2f02aa4707fbbd6003b8963a996efddbf2ec01f4`  
		Last Modified: Wed, 20 May 2026 00:09:51 GMT  
		Size: 5.1 MB (5087463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:437a39133472b257b574c8ffac5add0568f60ae668aa1012de1c20af2578ca5b`  
		Last Modified: Wed, 20 May 2026 00:09:50 GMT  
		Size: 16.1 KB (16101 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:628bd6ff9c7880c9fc15da70ade45197101d977c3f56b4f0ff28ff454d97eb47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.6 MB (201550536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:433b6eb9773fee26475e50b26a440b740209e8d9582913ab1a17429b5b3fdb1b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 06:10:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 06:10:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 06:10:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 06:10:57 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 06:10:57 GMT
WORKDIR /tmp
# Wed, 20 May 2026 06:14:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 06:14:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 06:14:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 06:14:20 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 06:14:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:562cecbb5aa529d280e58ef1f95f14cdcd37a90c5ea9181798a78377e934e6e7`  
		Last Modified: Tue, 19 May 2026 22:35:14 GMT  
		Size: 32.1 MB (32075742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97e0d4e70f345e6ec3f734a63e6f3053a7af5fb9379e888c145034be666b5f4`  
		Last Modified: Wed, 20 May 2026 06:12:06 GMT  
		Size: 93.9 MB (93902017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a71916c18401781a3e3f2b9ca505636abb37a159a423e0017d147af5894db8a`  
		Last Modified: Wed, 20 May 2026 06:14:57 GMT  
		Size: 75.6 MB (75571736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57b249074a1ec6aa8cfe95afe82c5430be689b6c04ae4cb6931a323e0a3fbee`  
		Last Modified: Wed, 20 May 2026 06:14:54 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245c94d4c51954171c0eb16b62e1e9591a18770be56f63962a35ba9ba80f2932`  
		Last Modified: Wed, 20 May 2026 06:14:54 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1bb025dfa49e614081174727093140d3751f28dcae46c5828b7cf180be7e5575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5086830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:044553bde02aea7553f47aab8be2c0475752cf9a9f74253098f11083f4e25b0d`

```dockerfile
```

-	Layers:
	-	`sha256:8deede18d6993716d3dda8f79faf3d2b2b674c7fae937c53f71061791dd62a1a`  
		Last Modified: Wed, 20 May 2026 06:14:55 GMT  
		Size: 5.1 MB (5070799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d641e6a576604564bf1c4bba6883a0f7ffa50ed65ef22900769f4215c8d0b93`  
		Last Modified: Wed, 20 May 2026 06:14:54 GMT  
		Size: 16.0 KB (16031 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:95884d6ff577e496f56da132ae5cec0b00ef8d4ae3ce41949fb2c2d6f3884074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.0 MB (185965858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae2ac047b85523d9d2dc1b9fbc0574b29f0b870f324a91a686c4c9537ed546e8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 01:49:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 01:49:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 01:49:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:49:15 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 01:49:15 GMT
WORKDIR /tmp
# Wed, 20 May 2026 01:50:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 01:50:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 01:50:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 01:50:24 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 01:50:24 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d5e0676594538bc23596fec84864fdfc1967950a13d798821e9073e432129029`  
		Last Modified: Tue, 19 May 2026 22:35:41 GMT  
		Size: 26.9 MB (26888597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c29118544f59e703ad98367e9fb39137130383fc3cb03728d1b9b2d61a0ba20`  
		Last Modified: Wed, 20 May 2026 01:49:53 GMT  
		Size: 90.5 MB (90536968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ec61a410b02b0d9a63dc0d12499c7519c576d2721b9938b324f59cf95a593b`  
		Last Modified: Wed, 20 May 2026 01:50:48 GMT  
		Size: 68.5 MB (68539255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7a12c18a30e3521b0d013fd8920b6a8ff83d6aad66198736790ab8e168224c`  
		Last Modified: Wed, 20 May 2026 01:50:47 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5919c90cfdbe163f4aa71d7070926e974d65507c4d319d25cc3a6ba2f92635a8`  
		Last Modified: Wed, 20 May 2026 01:50:47 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6b7033c03067742033570032b74c82d9f6ac36f1267e9060c81f6631cd853964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5074195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12798a51d2fdd9be8aefb8336cb03cd47952843cc34c905b5c5caa2610bec15f`

```dockerfile
```

-	Layers:
	-	`sha256:3ef3312f5ae189f22ad9694aba12751637be83e89d70740baad815780a9f9553`  
		Last Modified: Wed, 20 May 2026 01:50:47 GMT  
		Size: 5.1 MB (5058212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17a7654815936bc2837334a5a863d9cad9ccc0d3fe71c536f461b4d453eaafbc`  
		Last Modified: Wed, 20 May 2026 01:50:47 GMT  
		Size: 16.0 KB (15983 bytes)  
		MIME: application/vnd.in-toto+json
