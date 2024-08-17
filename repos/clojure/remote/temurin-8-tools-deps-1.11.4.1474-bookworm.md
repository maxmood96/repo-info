## `clojure:temurin-8-tools-deps-1.11.4.1474-bookworm`

```console
$ docker pull clojure@sha256:94aeef7a27deded31cd9ec3ac4ca8e52b7f498922e77bc959de75117a312b3ad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.11.4.1474-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:16f2bb9baebc3aa1e1020440c3db8b3e289fb7f9f5097520fcb9bb361b9e8d31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233620627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73c08cd7ebcce8021eaf4f7dee22fd78cf85bc49d391182a2e07be488f5ad863`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:0d5bdf84bbcdfa95d42190537e3cad2c0a5876f9127fae6a1d1c485d3539c77d in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:903681d87777d28dc56866a07a2774c3fd5bf65fd734b24c9d0ecd9a13c9f636`  
		Last Modified: Tue, 13 Aug 2024 00:23:26 GMT  
		Size: 49.6 MB (49554080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f988fcae5f7c2e5cd901cdd3f9f6818542a92e517485bbbb08de84d6a17a570`  
		Last Modified: Sat, 17 Aug 2024 01:59:27 GMT  
		Size: 103.6 MB (103611892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ee99793f3ad664ac032a480f8c5096ad3dbfefb2d7dbc92d12162a12552d0d`  
		Last Modified: Sat, 17 Aug 2024 01:59:26 GMT  
		Size: 80.5 MB (80454010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c6f1a6e98ba1c206fd49a3c88c620a2ffd6f8f399612e49666bc873e5c1d7c`  
		Last Modified: Sat, 17 Aug 2024 01:59:25 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.11.4.1474-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:2a6fe04c5c2b207c94b9af83df38d78fc65cd08b16db8cc65e902011a9a73481
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7039429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14a532a8a8ddbf7de4c0b5654048b4b91fb307f324a8b94d842a666574ab975`

```dockerfile
```

-	Layers:
	-	`sha256:474156e3799053d6319420e9e991caef2bb91cd2ce3a6e4e451ed9dd02e82707`  
		Last Modified: Sat, 17 Aug 2024 01:59:25 GMT  
		Size: 7.0 MB (7025577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5acad79f815ea518902ff35e0ef95f6e46fc7ef50114db8ccc20bbb7599c19e1`  
		Last Modified: Sat, 17 Aug 2024 01:59:25 GMT  
		Size: 13.9 KB (13852 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.11.4.1474-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6bb6fdcd30e17cedee2328eebf007f70f321fe0b6d648eb11ce128cb63441f1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232516379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f5f1d848929ff2e7021fc37fdae8ce754e9cb1e660c3ab1217c90a44743e4cc`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:e81dd8b32e45ea6e761021a3e01b6efd339dd9248a2036dc4b51a2c1de560b4c in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7b24851aa36de07cd94173b8e2052846573dacc3b241620d713254e647352394`  
		Last Modified: Tue, 13 Aug 2024 00:42:24 GMT  
		Size: 49.6 MB (49588592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7986c8e4558cd2e683983455be1de8eac003d3c4a12a96c3698cd852f4c1ee`  
		Last Modified: Tue, 13 Aug 2024 06:15:40 GMT  
		Size: 102.7 MB (102729218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab62ca20a4a172c83a543d25ad219a58dde31bc02b885401085d8308e7254ad`  
		Last Modified: Tue, 13 Aug 2024 06:19:24 GMT  
		Size: 80.2 MB (80197924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f329644b7bdcf494c35aac9a9426dcdf91ad930e806b142efe7dd4aacad9c8`  
		Last Modified: Tue, 13 Aug 2024 06:19:22 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.11.4.1474-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:42956bf6c5d78146a15d5a8fe9183903e71288da89b8ba7849ad67321d1cfd39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7046351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b987e113cfd4ba528a8d76f109fa7c37366d95826052dda8290d71bb08a6ed6`

```dockerfile
```

-	Layers:
	-	`sha256:56afdd653ed67a120ed5198ce6ac23260b3da472ef0040620cab365cb2504f17`  
		Last Modified: Tue, 13 Aug 2024 06:19:22 GMT  
		Size: 7.0 MB (7031964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d8dfe2e3d53669d13aa7a2dae22fa689a3ec33fe6a9e337d46ec5f6379dceb5`  
		Last Modified: Tue, 13 Aug 2024 06:19:22 GMT  
		Size: 14.4 KB (14387 bytes)  
		MIME: application/vnd.in-toto+json
