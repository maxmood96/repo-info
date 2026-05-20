## `clojure:temurin-26-tools-deps-1.12.5.1645-bookworm-slim`

```console
$ docker pull clojure@sha256:a86d88addaa3c1dc3a39b0e232b90c76a025f57ff280a3b1db12215364fa08bc
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

### `clojure:temurin-26-tools-deps-1.12.5.1645-bookworm-slim` - linux; amd64

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

### `clojure:temurin-26-tools-deps-1.12.5.1645-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-26-tools-deps-1.12.5.1645-bookworm-slim` - linux; arm64 variant v8

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

### `clojure:temurin-26-tools-deps-1.12.5.1645-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-26-tools-deps-1.12.5.1645-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:82c62d9bb1ae5ce31f0759df5265b612a0cae5bf2eb7084e159d1891a87efb2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.5 MB (201546924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173e22ace919ea3a64508aa39320793cf4f95236be800c172688677404be600a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Fri, 15 May 2026 21:45:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 21:45:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 21:45:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 21:45:51 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 21:45:51 GMT
WORKDIR /tmp
# Fri, 15 May 2026 21:51:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 21:51:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 21:51:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 21:51:14 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 21:51:14 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0e29ea7436ed4beb1c38bcfee44589407e49fc690669b42b35db33a9588e820a`  
		Last Modified: Fri, 08 May 2026 19:44:06 GMT  
		Size: 32.1 MB (32078453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80fd299d196bbbb90b619a2efbdb555a0daabbf409ed235c488e800b3c6f94e4`  
		Last Modified: Fri, 15 May 2026 21:47:13 GMT  
		Size: 93.9 MB (93902030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e86fc40d99416b143e0f820487aae6d191e93cea593e055b844ff9100b471fd`  
		Last Modified: Fri, 15 May 2026 21:51:53 GMT  
		Size: 75.6 MB (75565395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab80b0fbea2989f556279449278d94ec2120ff0844ac05abb31ecc11ed4ad39c`  
		Last Modified: Fri, 15 May 2026 21:51:51 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70b21f60ca1a6d4e5d40ee028567848d1b8b4de063e546cc26b2c2a8cd4b213`  
		Last Modified: Fri, 15 May 2026 21:51:51 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1645-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3e1bb191a37f021f3a9ac5e6c4bfee8e19484e6a6017faa07146dc1a42daf998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5086808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f90b99ea928f98676afd190adf37ce9ac1b46e3cfafb8bfc348f48a55037bbf7`

```dockerfile
```

-	Layers:
	-	`sha256:7f306c9a78278e1d1dbf4030d998009bc5b35dec1895844042bba8430355d229`  
		Last Modified: Fri, 15 May 2026 21:51:51 GMT  
		Size: 5.1 MB (5070777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5555096b28e8c85e0ad8a1498bd8b23d0880422592bfa4e36e460620150dbb77`  
		Last Modified: Fri, 15 May 2026 21:51:50 GMT  
		Size: 16.0 KB (16031 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.5.1645-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:eb8799ba630a9c5eafc921326b47e50b5c2aac6990fd5703bbb0a0bdb4d33253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.0 MB (185973130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d4b275e79f0da675e7f88c18db34af037a0f263d32b160c12d9cd454e281b9d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 15 May 2026 21:29:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 21:29:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 21:29:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 21:29:10 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 21:29:10 GMT
WORKDIR /tmp
# Fri, 15 May 2026 21:31:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 21:31:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 21:31:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 21:31:16 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 21:31:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfab53db9f0cc17ffff5864e26eda68d07663829af4b95b63bc4073b1f3451c`  
		Last Modified: Fri, 15 May 2026 21:30:23 GMT  
		Size: 90.5 MB (90536962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ad5f57b093dade96a849cf3eef69c7ca5dd3a90fc371859a89a976959a0cde`  
		Last Modified: Fri, 15 May 2026 21:31:46 GMT  
		Size: 68.5 MB (68543525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d6b59dcdb5021547125789e77e906129327fec9585f01cc888f3082c448ada1`  
		Last Modified: Fri, 15 May 2026 21:31:43 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a180476df48ce824de0d6929a29dce514879c04cf3e81793eed0e80c569df56a`  
		Last Modified: Fri, 15 May 2026 21:31:43 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1645-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:73fbff53d2f3483209f833e0ad9a0b560fad66c0bf88a7c3080d23edfac8d05e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5074173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c99533ecd427e83f7fc6da8b8f7131a9b90b27a595d46bda909d01be8ec52f`

```dockerfile
```

-	Layers:
	-	`sha256:538e49a9076c580cec636fe8e9995583f5c3fff6b7125323def3304efa0efd08`  
		Last Modified: Fri, 15 May 2026 21:31:43 GMT  
		Size: 5.1 MB (5058190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fee7c027743cb132b62acab567de93aa241b85f33981241ee93c4e6f2f04aa80`  
		Last Modified: Fri, 15 May 2026 21:31:43 GMT  
		Size: 16.0 KB (15983 bytes)  
		MIME: application/vnd.in-toto+json
