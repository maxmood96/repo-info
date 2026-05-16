## `clojure:temurin-26-tools-deps-1.12.5.1645-bookworm-slim`

```console
$ docker pull clojure@sha256:b799e92a3619d1bb17fcba92c4c9e81e461646e888f34108c7a8e300fe52a0d8
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
$ docker pull clojure@sha256:68e114eea1b3ee67c31521de01c53ebae55caf5ab2c2dd7959992e27d51a2012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192491900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:399d6cb4f2101e5ee385087421ce7bfff28d6315950bf40f0150478f1d9eae67`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 15 May 2026 20:37:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:37:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:37:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:37:11 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:37:11 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:37:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:37:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:37:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:37:24 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:37:24 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adee6f9e7889d559f0ef77fd7f1f1bae21a8ea812ecd7fd59c7d5765496d7b9c`  
		Last Modified: Fri, 15 May 2026 20:37:45 GMT  
		Size: 94.5 MB (94524384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebab800db5d567b4ce60299f79190567e06ab58cc88a08126452c91e5408a827`  
		Last Modified: Fri, 15 May 2026 20:37:45 GMT  
		Size: 69.7 MB (69730190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e150d432afb56410231462d4f7dd5efa14c67e8e9c5431ce90c5592b1db8729`  
		Last Modified: Fri, 15 May 2026 20:37:41 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e20aa12d6b865a3b6eade540abf26bdb771d0ecca5d95941c89d9d0093bca30b`  
		Last Modified: Fri, 15 May 2026 20:37:46 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1645-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f1675f18127f0e55492fc2c2dd1d4c06cb98c9d810e03eaa8603e3e67d3f88a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5097666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6db7b67eb74bf02f2cdb54f6ce3408aad6e1a2a105266fe8efbdafd1518aa5c`

```dockerfile
```

-	Layers:
	-	`sha256:6353d68128252709abf824b4cba332625bada5b4f5851336cc9ae580a8d02f91`  
		Last Modified: Fri, 15 May 2026 20:37:42 GMT  
		Size: 5.1 MB (5081683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb63913f42dccb01bae809cea0827d7c683850afcdc52ede7243ce1e2d0e4b18`  
		Last Modified: Fri, 15 May 2026 20:37:42 GMT  
		Size: 16.0 KB (15983 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.5.1645-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e670ecd46d473e7b3a9a71d1e3fd4c45ec5e02a9187a780447c98c0fc6187e1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191344218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:686a116ef3be40d1799abda1d840564940f90112b76d3beabb9cc6776f04efa4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 15 May 2026 20:37:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:37:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:37:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:37:01 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:37:01 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:37:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:37:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:37:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:37:16 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:37:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0ae4bb921bc833cfdbbeb5bff85abdcc8cd85849955dbcc006daa6ba238c09`  
		Last Modified: Fri, 15 May 2026 20:37:38 GMT  
		Size: 93.5 MB (93504390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c54c64139710ae76f5a13986b6829e08e30128604a7d6c91ddcad79c3f7c6cf`  
		Last Modified: Fri, 15 May 2026 20:37:38 GMT  
		Size: 69.7 MB (69722622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc616e436cd399a41cf36f4771c5d56341972cb08eb147291b34f5a8d3c83320`  
		Last Modified: Fri, 15 May 2026 20:37:34 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f86e07fbcbc1c591144bcd542a56c3ba5582cce8cd9dbd15c2f853f3147ee719`  
		Last Modified: Fri, 15 May 2026 20:37:34 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1645-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:eadb969f237ab7aa141eeea22caa4acebf64171ef170d3e8dfcefbf79524a845
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5103542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c765c773b73d9f95e949e6a9d35761fa48848e12d9dfaca90e0cce93b090a70`

```dockerfile
```

-	Layers:
	-	`sha256:1ca698a70f2ad7acbe86ff42f9d90ebd7c7899f3055081b3aa25e9e9be27f424`  
		Last Modified: Fri, 15 May 2026 20:37:34 GMT  
		Size: 5.1 MB (5087441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a8acbf81b0bc06301ab408c9645d32161ccbe8c298571a81fcdd105f9d0d72f`  
		Last Modified: Fri, 15 May 2026 20:37:34 GMT  
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
