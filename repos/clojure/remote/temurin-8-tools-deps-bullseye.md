## `clojure:temurin-8-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:2855bcd2831af5ba0483ac87d669622347fc1c2165c2c15d85ce5eedb8ddf9dc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:e4fd1566e0728117ed2e862d693f41578e447675337089a98b2668c6c9701d16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.7 MB (177650798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68759ec3ec48908e51dacb35524e8330588851b49f12a4a1d1372b0adc8f061f`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 19 Feb 2025 14:51:07 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:4ff5a3a54264ee833e4a09583363bbe779e881f15449fe4f4a6a662885dd37fb`  
		Last Modified: Tue, 25 Feb 2025 01:29:47 GMT  
		Size: 53.7 MB (53741401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6442588b0a71939b2f330c324569a215c5c58a1421aeaa1aa06132ce3f5710f9`  
		Last Modified: Tue, 25 Feb 2025 02:15:11 GMT  
		Size: 54.7 MB (54721234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968441723d588c6285f75117aeb0d665bd95dde45f0f232ed04229c177ec9818`  
		Last Modified: Tue, 25 Feb 2025 02:15:11 GMT  
		Size: 69.2 MB (69187518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80191ddab46fbed061a61de8dfa9b665ba4ee29b1b14cf1f04bd2a45c222c118`  
		Last Modified: Tue, 25 Feb 2025 02:15:10 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:e66b70561497548a673091d4f3afe53070985568e22582824d23b4d53751927b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7340402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:394df6665dc5202e90266175539ce064df8b7fad512cb109f8c4159e62837c61`

```dockerfile
```

-	Layers:
	-	`sha256:61c27094e1f572d657f943b5c15cedf7b0f6468ad31e0c244f1eaeac44253c1b`  
		Last Modified: Tue, 25 Feb 2025 02:15:10 GMT  
		Size: 7.3 MB (7326165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00e799e8aaf171c9b12dfa1e242783208e590973d7ba8714b2565ef4e3999459`  
		Last Modified: Tue, 25 Feb 2025 02:15:10 GMT  
		Size: 14.2 KB (14237 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:12c76e35254f21ca73d039ed29afaf148a28a69f8ac4f1f3e7c2ef02d1527c2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.4 MB (175378438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72972b16588cc9f7a3b212550641dbe2340bbcdcf03dfbd0df76d8ec79515006`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0038ef039a89ede34c57806e684dc9d9be7dcd22d3c08b90deb36bb22a2c7122`  
		Last Modified: Tue, 04 Feb 2025 01:38:11 GMT  
		Size: 52.2 MB (52245695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7e26da71c068cb6c68e55199cec0b81f2ef30055e49e4a653cd41241402103`  
		Last Modified: Tue, 04 Feb 2025 23:25:54 GMT  
		Size: 53.8 MB (53822761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2870157ad64dc96fcfd49b9ff7f7f36bb3866d2f185f25dc37fa06d4a0cb1365`  
		Last Modified: Thu, 20 Feb 2025 04:06:10 GMT  
		Size: 69.3 MB (69309337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ff6a7b89f695b5b65c786c6fd0c7c0daa7e1ae82ff42d1e8a9390369e8c30c`  
		Last Modified: Thu, 20 Feb 2025 04:06:08 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:f3dc3a0f532ca2bd16cba20a521810041640116d43ffc27f6c7c33778f6bcc2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7346315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c910c0ada1fc9ef0739cace436d32e40eb2724c945c2a1d8d4868908ca6ad2`

```dockerfile
```

-	Layers:
	-	`sha256:84c507c76e0c7574ab2b89df98a56578e571cc546089a6f9a04c3ccb05c6f5ce`  
		Last Modified: Thu, 20 Feb 2025 04:06:08 GMT  
		Size: 7.3 MB (7331962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b41472c366e1a168237299772dd33dcc236f38ab934af4d56dbd16513fde1cb`  
		Last Modified: Thu, 20 Feb 2025 04:06:07 GMT  
		Size: 14.4 KB (14353 bytes)  
		MIME: application/vnd.in-toto+json
