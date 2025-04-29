## `clojure:temurin-8-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:4df5c3df8950e45eb36aa9c415ec1652ac91b8c0df4e12b0c7052dd70281651e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2354ba72e82eeda3fff6982b43a637915c88efda13fe1a69514ed2c92aaa9145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152470179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34b75f3a588990094c3a06f314cfd7e3eadcb97a3684d981d5c0711e33e9203d`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c4033ce196a6f714c7b18dbaf36bd59d4dd12621abad09b9905ae0ed919ab5`  
		Last Modified: Mon, 28 Apr 2025 22:05:48 GMT  
		Size: 54.7 MB (54716178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70ed9bcef3fe06befc5dd9c22e4b2bd40dbfa5f28e2d796dd4dbf662b4e8fdf`  
		Last Modified: Mon, 28 Apr 2025 22:05:48 GMT  
		Size: 69.5 MB (69525713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01bb68122cdd0ce5d0376f7117933fac27effc168255792e40cf02c76c04aaad`  
		Last Modified: Mon, 28 Apr 2025 22:05:47 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ca4c245d8221dfc89c8976aac3f41c907ed291d33618cc7a1545e66789f91fe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5049866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ba3a8ae395edc4b8ae870f44b64a668d4721e193468bf038600bc2d946c147`

```dockerfile
```

-	Layers:
	-	`sha256:79d098d2fbe0e7836acab78cfe864e40ac0c793b8cda4a4f95bdadcb475671f0`  
		Last Modified: Mon, 28 Apr 2025 22:05:47 GMT  
		Size: 5.0 MB (5035575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6166410ef4fc1ec9b1fc842cfe10ba22144bbd6acd0666717ff21d2c36380e07`  
		Last Modified: Mon, 28 Apr 2025 22:05:47 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:08ceb21650cb3010609f60fdea87da623466149997f746394912e23d5eab42ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151267739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7034c92ac52f706ef6887b27b6dc49e61aa2011afdfe7ae046bf5e9f27352a`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e816d872a5165a56e55df8bea6933fd7114deda268519e3d3e5ba5725dbdc956`  
		Last Modified: Wed, 09 Apr 2025 17:12:23 GMT  
		Size: 53.8 MB (53822736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a960f6b11cb1ad17bf3c05af39a91e9f4f127376ffe0c5ed9890af0d53d7cd0`  
		Last Modified: Wed, 09 Apr 2025 17:17:04 GMT  
		Size: 69.4 MB (69378039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959de21762964d4ba64c11c4cb89baae63ff52fc2a633cc6a7be254991deada3`  
		Last Modified: Wed, 09 Apr 2025 17:17:02 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6d0b8a2eeb32899af355f157eb8244e6298fcdfad1b6c3007bca849e9c522fd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5056443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade8666d8e5cfd02edaf09c1a8acb0dbac3afe03c3539f0be2db55a9a8a994b8`

```dockerfile
```

-	Layers:
	-	`sha256:321819a00e00fbfc8fcd1032dde90bc7d6f92d40870983c31616b7fed4d6949c`  
		Last Modified: Wed, 09 Apr 2025 17:17:02 GMT  
		Size: 5.0 MB (5042034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fad4df2a983f68716a9de155731587eead9bab354c3b7ed07677caed0430658`  
		Last Modified: Wed, 09 Apr 2025 17:17:02 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json
