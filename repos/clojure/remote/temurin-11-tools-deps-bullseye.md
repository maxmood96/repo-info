## `clojure:temurin-11-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:0ee46f4d73ae62122520a7e74e437ecef0613036f18532ce5ca88d3b37b2e47f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:820376f17a1946007c5a90403607557693450bb257a11cc4b07cd44b01abc1d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268975349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb39193aff945d8b49e0f4823564b9ec92ef1fa82bc0ec475144154bad21f101`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:10ffc47270cd106d2d04bc7ef4749d579620e45a84804ba3b18f0898fe5ecc64`  
		Last Modified: Mon, 29 Sep 2025 23:35:07 GMT  
		Size: 53.8 MB (53756064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ec6a36b0732bbb8d366673ae6c7066eba243796b23c24a86bccbb39e8ea8bd`  
		Last Modified: Thu, 09 Oct 2025 22:27:10 GMT  
		Size: 145.7 MB (145658349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2922024399af6b825ae2bfe8f00f1785b4ad927193583a9c769c5e344231ef9`  
		Last Modified: Thu, 09 Oct 2025 22:27:22 GMT  
		Size: 69.6 MB (69560291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be6c9c0e74fa1b0179f627c0e9b1f20347a90d551b76888cd41b9d4fa9c206b`  
		Last Modified: Thu, 09 Oct 2025 22:27:17 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:338ac6375c91622e5bb4160ce2a2013ac139b2363ae201646188de2c94cac3cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7431683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9008e103a504fe407189c96cb9036c1083592f75b9973f5c4cd788cf7bdeb73`

```dockerfile
```

-	Layers:
	-	`sha256:ba10c17e81105a5a1a4c96ac72c23d3a95cd7070cdfa0885da06554d5b1b63f0`  
		Last Modified: Fri, 10 Oct 2025 06:36:24 GMT  
		Size: 7.4 MB (7417432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6957e29bbdc2a7f40623745ae85cc9494a576aa3c887449f10058b20671154db`  
		Last Modified: Fri, 10 Oct 2025 06:36:25 GMT  
		Size: 14.3 KB (14251 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:38d82b551f685d6163f414630a8b5ce3c046e7e0f3b5b9a08065f785e4d56f7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.4 MB (264406663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a78a958660ae7d2c0360e73927b86c3e3c44d4fe08010c805a2734a204b09b1`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9b16ae1bbd1ada84c12528379a10e280bd89e0d0332670c8487145eb77fe2fe1`  
		Last Modified: Mon, 29 Sep 2025 23:34:42 GMT  
		Size: 52.3 MB (52257414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4e2c12966d94303b35437487c13fdc98e736326b60c6d0d8359808a86234d6`  
		Last Modified: Thu, 09 Oct 2025 22:27:30 GMT  
		Size: 142.5 MB (142460610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02201df2103f1bce7dcb55b43e7c84c66e4c380824b155785d3b734bb7be3f8`  
		Last Modified: Thu, 09 Oct 2025 22:27:41 GMT  
		Size: 69.7 MB (69687994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934e7f803efa8e2d65c1696954d0372eee668dcc735144021851d39731762501`  
		Last Modified: Thu, 09 Oct 2025 22:27:37 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:70db67c7fa3892862a5b21e8a5118c6c49837e45e89ff5c46644065f942b20e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7437519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54f6565856ca49723e637777d229a1a6e29d4e2fda396cdadc3425e4c84718c5`

```dockerfile
```

-	Layers:
	-	`sha256:64d86c0adba355d9a0de078962df20141a05b0dbfd094591c5571321c85542b0`  
		Last Modified: Fri, 10 Oct 2025 06:36:31 GMT  
		Size: 7.4 MB (7423149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21a699b84dea29bff623d685d8b6649d5741b3ec44b11926304b00a35521b7a7`  
		Last Modified: Fri, 10 Oct 2025 06:36:31 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json
