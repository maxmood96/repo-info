## `clojure:temurin-11-tools-deps-1.12.2.1565-bookworm-slim`

```console
$ docker pull clojure@sha256:321f8f1f0ce236de0e0099ff4697c26ca19ac5ce5f48723b0e6fc437c5eeb55d
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

### `clojure:temurin-11-tools-deps-1.12.2.1565-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d32172117ae167e1b5a62ad3e522358499388190edbb12db37a3de6178a2fa58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243565572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:019944bee8d53ae2e0cab003c68931a5884906e5c14fe086b4145f08f6de1a40`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5d36682b30815fc000c5ea237982d9d183bf00f269124d65aeeaca8af92c36`  
		Last Modified: Tue, 02 Sep 2025 00:16:41 GMT  
		Size: 145.7 MB (145658229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac72c768941aac287571f11f16045abc8d886134f07e4fb44bea826e524576a`  
		Last Modified: Tue, 02 Sep 2025 00:17:25 GMT  
		Size: 69.7 MB (69676440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8296a6328b2c275b60600515318c445129557472d84a4b65d9e2a8e5538d76b7`  
		Last Modified: Tue, 02 Sep 2025 02:35:06 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.2.1565-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:811cb18c4bc7428011ee6e1ba793ee1be8db0722adeac529fae9294ef362078d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5145724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b404afe0ce97163c9c6dc8f45a4194b4c8daf495753b55de0628cd0b3884ce1`

```dockerfile
```

-	Layers:
	-	`sha256:0273b89ca7649d0abdaf95495ea333da3e0d4743e7296c48761a846d98f4ed6e`  
		Last Modified: Tue, 02 Sep 2025 03:35:29 GMT  
		Size: 5.1 MB (5131414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aca02d57887a051e54046be5291d08f1299715578d9d04d8197fade581f7b789`  
		Last Modified: Tue, 02 Sep 2025 03:35:30 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.2.1565-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:aeb3abb899ce6f22fc2b813d5081b90729ef9472f10404181d2492d96566f332
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.1 MB (240091317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb4c2a7cd94956ff1e38fa13672d7a0101047127cb462c4a761247f51f4e5264`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:835edc7f3c4540a8fd6aa34189a38ee0a43a8857a67e5ce020d4fa39c6954844`  
		Last Modified: Tue, 02 Sep 2025 07:45:46 GMT  
		Size: 142.5 MB (142459133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31dc0043987dfb1da785ed5b405f54c74f8c60c79264f0a4f982195c1dad6c5`  
		Last Modified: Tue, 02 Sep 2025 07:52:48 GMT  
		Size: 69.5 MB (69549537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4e8caf161d7cb43155ecd80c384d6fd8d93b26e06d4f5edd66a4ab26666b68`  
		Last Modified: Tue, 02 Sep 2025 07:52:42 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.2.1565-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a92e4d6556dace5b1d2cd508a18f9e59847c0cc67e49f58749b120e10806ac39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5152221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc035c0a101ced917a9db8bcf0658f08eafca5f16dceb5e14d8d621f9fa3b6a`

```dockerfile
```

-	Layers:
	-	`sha256:31c8146ba0708769e5ecbae2bc4f8a71dc48d9300355e6ae1ff95fec1dddad03`  
		Last Modified: Tue, 02 Sep 2025 09:35:30 GMT  
		Size: 5.1 MB (5137793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccef5e954f09ca2e57654fb27b42e45af51bfaf6c2c57350aeafb0346f63cdd8`  
		Last Modified: Tue, 02 Sep 2025 09:35:31 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.2.1565-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:9d78d18fea9553f50e101cad207f524a8f60643bbcc494c1ec5a6f3d81b68e8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.4 MB (240431219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a91cfc154903ac565be43faef46b5b367a18463834d634bf923251b6238747c`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f342ff8ad80874f0a163e9e352e9ed6ad7192942a6ae1eca40b87d872162f0c`  
		Last Modified: Tue, 02 Sep 2025 08:12:24 GMT  
		Size: 132.9 MB (132853147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a21faecb8f4ef03e26152ee8f09f5dde0c856b02f07af935fe3c966b1bccd1`  
		Last Modified: Tue, 02 Sep 2025 08:23:11 GMT  
		Size: 75.5 MB (75504004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe877fbb3e696f943fbcb1f95612a478e842b3da1f58dffeb2b14e409f12833`  
		Last Modified: Tue, 02 Sep 2025 08:22:55 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.2.1565-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:eaad73b975b99f86f2a5dfa2110c3cacc7bf2cedc3090c50a01674c569ead2dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5150314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e3415b84fb3b0572c0d3a73806e469336f8cc7b705f0ad35294f80f732925b7`

```dockerfile
```

-	Layers:
	-	`sha256:377e95ff2e222f286cb381a5f62708ed09afdcff6bd428bfacc9f193789c7027`  
		Last Modified: Tue, 02 Sep 2025 09:35:35 GMT  
		Size: 5.1 MB (5135957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ecc0d417e92adebd8d8c06952f55ace3c6c1d9d83aa7ade2ba46f45b2cb3be6`  
		Last Modified: Tue, 02 Sep 2025 09:35:36 GMT  
		Size: 14.4 KB (14357 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.2.1565-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:dbc152e72c7aa191b25ef5b197c108a9b843db7351ae1a81be9028105074f7bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.0 MB (220995151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbeb3625eaeee4e8b8a80a5812db78d41f18ef8da6e885344bf3a063853fc025`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632e8bc83e880acb510052f87a9ce5503ba3f0b0be39945274f7d49fd731441d`  
		Last Modified: Tue, 02 Sep 2025 01:45:26 GMT  
		Size: 125.6 MB (125622191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b81ef5218dbd4487b23f0feed9ed2cf1772e97133253f8c060a71adbbb90f99`  
		Last Modified: Tue, 02 Sep 2025 01:52:03 GMT  
		Size: 68.5 MB (68484479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361cf46fc47ad4fb5098812667341ca4f26b85bd1955d312baca71dfd7e15688`  
		Last Modified: Tue, 02 Sep 2025 01:51:51 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.2.1565-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:202ba8500628c0b6fa685c43c8398eb15aeac674328e3057fe0a7f732cb157be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de129dbb82dbdacc4d3b87f6f22e36e6c9cc54f5e58142e4bd61962eb5fbdf95`

```dockerfile
```

-	Layers:
	-	`sha256:60e6edddf10a9a00dacf8a40b8579230b6fd6fb2e4d582b8690c8cfe0a7ef244`  
		Last Modified: Tue, 02 Sep 2025 03:35:43 GMT  
		Size: 5.1 MB (5122739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7f0dd2bea3216097aff3f021ddfffb7c7293254f038519930d23940f1bed751`  
		Last Modified: Tue, 02 Sep 2025 03:35:44 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json
