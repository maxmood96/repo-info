## `clojure:temurin-11-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:f99eaaf41322c3c44754c2cc09a35a4a9aabb186ed04f6ed56c6c4518fd55e3b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7639f726f153af7d3eb243326044567c4d91293c87f64efb7fd87403bf428964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234883966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9797429d1b159ee5530d8aab305297cd8c2b3efcc0035e56fc769ec5ddb1f114`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c8e1eb8ab3b017bd9e33ddec83ebdd8292c542bbd14a8d5a6cfa2edc3ad3b8eb`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 30.3 MB (30254604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a333dbad3be2aeecd0c6a4a552c3e8d84fea1b4142a3ff171a6a8902ab425069`  
		Last Modified: Mon, 05 May 2025 17:08:14 GMT  
		Size: 145.6 MB (145635746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c197aeb92fb639b151e8eb45f60d10704d5669609d4cc34c46adda6b5559b1`  
		Last Modified: Mon, 05 May 2025 17:08:12 GMT  
		Size: 59.0 MB (58992971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4beba14f1694ddbdde32211f984649813342276e1012d0bc2234da1348e67f`  
		Last Modified: Mon, 05 May 2025 17:08:11 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:77c13bc997a3ee268efa9605d4080b95a17f3ffb41bcec38691f549892c7bc4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5153518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7298c7a64c8cb6675916f333b7799d1a5050ec7c8f3a81a7ecb6a7c5a2c6dfb3`

```dockerfile
```

-	Layers:
	-	`sha256:a0475a8eb311aed82c271163960c28d2f49ef9bc98a51c1ce17300937fcc5fd7`  
		Last Modified: Mon, 05 May 2025 17:08:11 GMT  
		Size: 5.1 MB (5139208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f79f56376212cabd7af8941d081f9419225f466fa5f7f9e3d617891c62b46ce3`  
		Last Modified: Mon, 05 May 2025 17:08:10 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f60bd2e2595fd3315d495231d947786e4afaaa2189c666f5cc5660a560fc6176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.3 MB (230294690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:122ac25f0568bfec16af5e62fd9e31c84ce21b2d825df82e389d897d8e0dc006`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:5d3a81360c5bb9281a4f735a1468429a1898f1a4fc24a2581dde4cf28ace4488`  
		Last Modified: Mon, 28 Apr 2025 21:21:09 GMT  
		Size: 28.7 MB (28744645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e78d2c29016836785703fd1a3b6a2c3ab908b7865aa01b553d5dbdeee44eea`  
		Last Modified: Tue, 29 Apr 2025 20:16:23 GMT  
		Size: 142.4 MB (142422045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c024bd4682e386307bac70d0cbaf908925038381daca6ee0ee73779361718c`  
		Last Modified: Wed, 30 Apr 2025 01:09:36 GMT  
		Size: 59.1 MB (59127355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18c645d702f0221fb90415aa2ceaa9c8715dbfba84df04060e2f942a3a0f1917`  
		Last Modified: Wed, 30 Apr 2025 01:09:34 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:15db83609d28f20974c55c4090cc6b9a93cde20073bb07f5243ba21f19683b90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5159986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39694411ed6af6826b4fd1f189740c7af66dbbc4cc39acf47f101fe7c44670f9`

```dockerfile
```

-	Layers:
	-	`sha256:07e4530b5e45a1d51225ee659c50ae6b2df87fcefbca73f4531bfe55c6479f4e`  
		Last Modified: Wed, 30 Apr 2025 01:09:35 GMT  
		Size: 5.1 MB (5145558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7adbab649b282b63bf2eb38ae5a12107b0687ae2d9315d6ee3de045aee48755c`  
		Last Modified: Wed, 30 Apr 2025 01:09:34 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json
