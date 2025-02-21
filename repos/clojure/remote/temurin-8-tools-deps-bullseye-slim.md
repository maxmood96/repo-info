## `clojure:temurin-8-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:9581d7421589a923cd622b266cf00597ec8710a637d540d8bd78f98d20782ed1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c445175639f38f33153e6a3182eae2653f4aa6898dd62c7f7c300da6310f4c53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143762837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dff255309312b9d4643deed79cd40597d1caacc12b08382117f289cbe7fe614`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
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
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac515e5352f245a7e3af614b365dc70c90aebdf977f0f1ea674d9162bb418351`  
		Last Modified: Thu, 20 Feb 2025 02:29:37 GMT  
		Size: 54.7 MB (54721245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec1aa7fcc39e5602c1c81aea2541b1269ae372dcb45906d624c2cebb06225754`  
		Last Modified: Thu, 20 Feb 2025 02:29:37 GMT  
		Size: 58.8 MB (58788358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a6391f6c499e8f975ad2453c1edb182edd9f385634f5a6e7c678f3c2610daa`  
		Last Modified: Thu, 20 Feb 2025 02:29:35 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ae0940094d362f04575d517a02980cd9747391ad6e7aa0c14e056af52ae76a87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5252966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f5f3ccb6dbaf54e90a76b991b494cb94903907ee12e5d22106e65fc0854106c`

```dockerfile
```

-	Layers:
	-	`sha256:04d6102fc07e2c8b90f583783cd3aefe8a62000a7e1d23772a63e887774a6657`  
		Last Modified: Thu, 20 Feb 2025 02:29:36 GMT  
		Size: 5.2 MB (5238677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bef72170709cb3348095634dd85046a64c0c11805ff808e12a727b8dc266fbbc`  
		Last Modified: Thu, 20 Feb 2025 02:29:35 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:960be0d94e7ba178551abad24c151423ff040fd01a0508ba080eb60a50a42fd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141478671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed35b08d7f327ec850d83861cf10a133139f6e2f13053516ae7429e6831694b6`
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
	-	`sha256:9225a2a808e874449ee822a282882a3c331aad2f5093c1062e16494d8bce3e9a`  
		Last Modified: Tue, 04 Feb 2025 01:38:25 GMT  
		Size: 28.7 MB (28744810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bbfecaf30e64df0a0ebb56cfcbcbb62350f903855a9adb4e256a20cd7116daa`  
		Last Modified: Tue, 04 Feb 2025 23:26:41 GMT  
		Size: 53.8 MB (53822776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78925c8aff1c8af06b8a528121eafdc47f5bb3a87ef86e9d7f13738b4ff6a448`  
		Last Modified: Thu, 20 Feb 2025 03:40:37 GMT  
		Size: 58.9 MB (58910441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdab8aa3123fa5d91686ed2289d10a889cbf5a9252ff0dad4b89e01def0e8724`  
		Last Modified: Thu, 20 Feb 2025 03:40:35 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fb72db6cea26a5566e7f0e845936bdbf7c40f20b7b0b3fbb16ffc6e724d6794b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5259516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb34fbd5446ff236cc01924fe7a6cb638d96ace52974685d44c448b83c6e6d5`

```dockerfile
```

-	Layers:
	-	`sha256:bdf66a0d134b8c4d27ecf3a40fe788d03697132af4988999d445662f8daa8d5b`  
		Last Modified: Thu, 20 Feb 2025 03:40:36 GMT  
		Size: 5.2 MB (5245107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78c1190093b9d722df8a228edbe31aa175058275b0b25b81e824685eaf3d1639`  
		Last Modified: Thu, 20 Feb 2025 03:40:35 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json
