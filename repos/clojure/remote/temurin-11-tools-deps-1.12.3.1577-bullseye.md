## `clojure:temurin-11-tools-deps-1.12.3.1577-bullseye`

```console
$ docker pull clojure@sha256:be8eca31a94ae5dd6c00cb225a39ccba5a705d1e5df2db3d8440a48d1aaf55e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.3.1577-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:850f2634ffb5e25d4b221d025a0c7979c7720c0d0a262242d5809a3f86d80ee9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.3 MB (268284708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e5524f91838c2063f0ab806aea2393af5c7a6832a5cd6102b6ca8ba1d7fc34`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:51:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:51:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:51:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:51:27 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 23:51:27 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:51:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 08 Dec 2025 23:51:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 08 Dec 2025 23:51:40 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:437b5b60e3a4b64e2c621589a67483eeef6d4b3fc4926655006ef41bd44f71dd`  
		Last Modified: Mon, 08 Dec 2025 22:16:49 GMT  
		Size: 53.8 MB (53756413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43be188993ef55ba8cd37ebf7bb2b446eaf1f4cede07c43f37c1795a6434b3c1`  
		Last Modified: Mon, 08 Dec 2025 23:52:15 GMT  
		Size: 145.0 MB (144966652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c23de58a4149d0b1a5a700aca75a91f2ebade45baf225ef407a38cc8439f6bd`  
		Last Modified: Thu, 11 Dec 2025 03:17:54 GMT  
		Size: 69.6 MB (69560999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f77a69304d6a200a69d5589ed07fe80a3bb301ff951e4a0fe753d9f4b3ca25`  
		Last Modified: Mon, 08 Dec 2025 23:52:06 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:80c79e368a71026ce92fb2a6276cf81de6c2087121edbf91b564394085880ed3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7430017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ddbe708bdc63e4a3dc29e49b39e2dac6f04f0811157baf1298b1318793c3559`

```dockerfile
```

-	Layers:
	-	`sha256:9c1c7a478ff3efde943632f2a2fe36c67dfd221784c9470b2daacf4aa1a40072`  
		Last Modified: Tue, 09 Dec 2025 04:36:25 GMT  
		Size: 7.4 MB (7415808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aada9335f0fefd6435494f499ae209b698d3bbe4642f5edd4a8ad63dce686293`  
		Last Modified: Tue, 09 Dec 2025 04:36:26 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.3.1577-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a0e26e4fef8945808928efe134434a7342b127fb05d965203ae537d80d568e9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.7 MB (263678287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:783004083f7c5b48ddb9258aadfa4b1376721c37a7aa4f63a1459b72184b5789`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:59:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:59:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:59:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:59:57 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 23:59:57 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 00:00:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 09 Dec 2025 00:00:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 09 Dec 2025 00:00:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:24bca79f74a34f86894c8fcdc6ce8d7dc3c11dd0c76b7e9fa80c7c64df65d166`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 52.3 MB (52257713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b23d4b74e6507914f1d8469ad88019660743a15306c0655deb3c191b1b384c`  
		Last Modified: Tue, 09 Dec 2025 00:00:58 GMT  
		Size: 141.7 MB (141731575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5700fb7806be2803b604740fbffb65789148d57b7eb0daf80eea352856fd57`  
		Last Modified: Tue, 09 Dec 2025 00:00:51 GMT  
		Size: 69.7 MB (69688353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36670886e9ab7f12ac86795b4e7b89451d94cc876df02416914e71f432840724`  
		Last Modified: Tue, 09 Dec 2025 00:00:46 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:e3c0414c15aff4c319be6085d0b11497ef790bed05319ceb19cb91f3f1bd92bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7435852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d700aa21464d7b0841905d8271f10e255aa98644a1912a8e1ac56c97b40135ee`

```dockerfile
```

-	Layers:
	-	`sha256:13f2d10343bab99c627fd1074dc54358ec40d6357b00e868104ed5d51a1bdef2`  
		Last Modified: Tue, 09 Dec 2025 04:36:32 GMT  
		Size: 7.4 MB (7421525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5bae43449f75f4829811f236e65966c0004c502f8b5caccdbedfe596b7bd935`  
		Last Modified: Tue, 09 Dec 2025 04:36:32 GMT  
		Size: 14.3 KB (14327 bytes)  
		MIME: application/vnd.in-toto+json
