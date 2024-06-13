## `clojure:temurin-22-bookworm-slim`

```console
$ docker pull clojure@sha256:0c8fccf6af7dc077efb98f0bd108cc2a5d20b35fc35bd845ac26a3cf1d7bdc3a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c0a47121e0f6cc4677cd1b71af3295485ba6a4bb3a79c37255154c137886c99e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.7 MB (254735535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592e2d65694447e3a82f0f39bb3d713d168af601d12a9d53f83894cde1c31b93`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365b620ae50a84857718f14d6fea487eaf1f23ede2832ae70e4bc68b9e7d336b`  
		Last Modified: Wed, 05 Jun 2024 06:12:44 GMT  
		Size: 156.7 MB (156715499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1e757da22539075f20871dd1c5e367bb421441065cebf2fe3bd0029b30c45e9`  
		Last Modified: Wed, 05 Jun 2024 06:12:43 GMT  
		Size: 68.9 MB (68868578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91e845e3c5582ccff2aea7637ec3c50d0c1da51ab27760fe2d3e764d1ed165c`  
		Last Modified: Wed, 05 Jun 2024 06:12:42 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a33115e375c83578f338dc6b8ab8823341ea95464c5dd173107a513cfba790`  
		Last Modified: Wed, 05 Jun 2024 06:12:42 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5ee306b9065b18c13ad7fe3580e46208fb2c9529832a7be848530029f823b354
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4720395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10e6cc310027db4b4eb85cdf439b5b03b3ff01b0617bb95ba15395ed10cf60df`

```dockerfile
```

-	Layers:
	-	`sha256:c3c1eb2702062948f6208bee87c51ca13581aada87f8dc676e555f8ff19122db`  
		Last Modified: Wed, 05 Jun 2024 06:12:42 GMT  
		Size: 4.7 MB (4704932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:359a2d0919fa1be3fee7e3a940601da6fdb021b073a179dc97424498af641e6c`  
		Last Modified: Wed, 05 Jun 2024 06:12:42 GMT  
		Size: 15.5 KB (15463 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:53b4a9a8043ed99b91ae9d22b00b7ef548c4ea12ede3563a0188932580ab8dfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.5 MB (252539537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d0bbeab9827139a0d0ae61e5eadc41fbab9d043c9d2b0bdd7dccb559013647f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d556f73e4c9f57bac26b955ba103d774358439da4efb0b23e476a44efc2c3977`  
		Last Modified: Thu, 13 Jun 2024 12:00:35 GMT  
		Size: 154.7 MB (154738019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e529a5fc30ace21fcc5c078d0a06ab4e01735289c1ee6ed233e5504db10c737`  
		Last Modified: Thu, 13 Jun 2024 12:04:01 GMT  
		Size: 68.6 MB (68620806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777777e585912395d68d8e630605b625fccec4778a78ee1ee3eb0ac422494198`  
		Last Modified: Thu, 13 Jun 2024 12:03:58 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea98b54c7f6f645c334e1eaaa3dfbd0a826357c6519ee9cedcc0260e8ae6107`  
		Last Modified: Thu, 13 Jun 2024 12:03:59 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4fdb260cd33ead8f5e729ce62b04814083102a2c24b946330cd301262b56358c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4727370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b7fa45ea4666b6a43a5d06ae298fe02f6990ee112b5c46d43b68114bf8664b`

```dockerfile
```

-	Layers:
	-	`sha256:8e4af04f5f86794b7600ff726812b1adc8dd489c253213b87f24cbb6d20fc47d`  
		Last Modified: Thu, 13 Jun 2024 12:03:59 GMT  
		Size: 4.7 MB (4711317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:060b4e760b4d69996107aefa5f2c3763c72f125c44ceae2dcaa5c2839bc418ed`  
		Last Modified: Thu, 13 Jun 2024 12:03:58 GMT  
		Size: 16.1 KB (16053 bytes)  
		MIME: application/vnd.in-toto+json
