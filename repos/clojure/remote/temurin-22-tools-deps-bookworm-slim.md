## `clojure:temurin-22-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:6eb9302842ec372044de1677499aa5e5bc2ff14024f3f3635a14b8ce1c8feeff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-tools-deps-bookworm-slim` - linux; amd64

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

### `clojure:temurin-22-tools-deps-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-22-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:26c242263b33a9c0f374cc6d0e5de1ad67659fb176f0b67af86c24a895617ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.5 MB (252539560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d70abc3b8d95dcb6834cf9d3e2e257ccfd113e58f728d2043bce82074d6c6700`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
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
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac1f9c76badfb6ef70e3ea9ab81d24da2bddd5fa36070c7576c724e965a77f0`  
		Last Modified: Thu, 30 May 2024 01:51:58 GMT  
		Size: 154.7 MB (154738000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9619bd124f81e18bddcbcf0e62dbe2b9428da597961613cc8f7b6db408d4db9`  
		Last Modified: Thu, 30 May 2024 02:07:14 GMT  
		Size: 68.6 MB (68621013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bd17ea751424d3adeebd70843095d67ee697222a7713958d91ffcafd5f2a17`  
		Last Modified: Thu, 30 May 2024 02:07:12 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e525761ffe65f4794fc252cd1f6f451557ebbf2d35b9de7f31b62138fed05b`  
		Last Modified: Thu, 30 May 2024 02:07:12 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0b43884f923ea712d5b01ff40c463f7522d7bfdbbf7c481f6a9eb278222ffc75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4727322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad7ec10bd287268a65a246363272b154660828517a24e7e5043f239aa754bf7d`

```dockerfile
```

-	Layers:
	-	`sha256:b574a1d14ec805545900e1f773d88133ec50eed07d7941820ea91b3c9dd6d46e`  
		Last Modified: Thu, 30 May 2024 02:07:12 GMT  
		Size: 4.7 MB (4711318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dc44fb4491714fe470adda6785926a28851c57cf8455dfc2baed0e6ada618c5`  
		Last Modified: Thu, 30 May 2024 02:07:12 GMT  
		Size: 16.0 KB (16004 bytes)  
		MIME: application/vnd.in-toto+json
