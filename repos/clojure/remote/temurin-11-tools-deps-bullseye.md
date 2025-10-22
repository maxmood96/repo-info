## `clojure:temurin-11-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:fca8d978fd524550ccc65a393f19e6cf93cffae4b1f51b7b04b72a220b781fd5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:c6c1b59991c0a75212fb68d85c54bda4cf915c0ec5f21164346c4fb9c498957c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268974530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb1e74582888b8bed0313e24e0963acca3dca9c46513c19b95326070af9dfe7`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1760918400'
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
	-	`sha256:b6f830cd306f01980373f1e0120f2d00018fbe51a9506b7262f5d9e4bbda74f9`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 53.8 MB (53756115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fdfaf153f6b3c7d0ce83aeb79272151615e2cbf4f2c6698eb50eea1b99732e`  
		Last Modified: Tue, 21 Oct 2025 13:01:46 GMT  
		Size: 145.7 MB (145658349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cad78cb143e30c03ecdacfff65171765bfc05635aaec734ff1586cba2e2e363`  
		Last Modified: Tue, 21 Oct 2025 02:21:21 GMT  
		Size: 69.6 MB (69559422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eff52c24bfe653faf1444b72edf46328ab1c70b7d51fdc192dc5fb74d6c6199`  
		Last Modified: Tue, 21 Oct 2025 02:21:14 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:bf26c5749c31a6766394f15bf7293b9426dd3603e43af23c3f2fd02541d25911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7430059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb622f1f706568c7fba79e7e6e176b9d91aeba4912ec416c5279d1106e3cfea`

```dockerfile
```

-	Layers:
	-	`sha256:dbc9369de77ce11f22f4f64b94da040c0a29a9167c7a3ecd498777350ef6b73c`  
		Last Modified: Tue, 21 Oct 2025 09:35:59 GMT  
		Size: 7.4 MB (7415808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a2e3e2d01d8e8a563db4fa3759f885dba87d7a047b7a23dd86122b0c5d0ffef`  
		Last Modified: Tue, 21 Oct 2025 09:36:00 GMT  
		Size: 14.3 KB (14251 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:36c2d7b6c669e1ba1e599709ad030a6a04fdecd95b112c03e85e1e2f044b94dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.4 MB (264406773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0afc1a700902564fd7e6e3b2b8e0ea52db8bcb1b30380090237fd1ef7dfccf`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1760918400'
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
	-	`sha256:0a72c4e347b74aa6a0086cf3d1d928528ab02577a17bff4e22366a7df681f564`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 52.3 MB (52257444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2033b007fd41cea934872d63ad6c7f44e2c3ad08864553cec3aebe597bb38c65`  
		Last Modified: Wed, 22 Oct 2025 08:07:40 GMT  
		Size: 142.5 MB (142460560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd41e1310304d9fd67c18657ab987f6c9fee7e08a3373eb341fbb1ae260768fe`  
		Last Modified: Tue, 21 Oct 2025 02:26:58 GMT  
		Size: 69.7 MB (69688125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1678a2ed81656aefdd9fb45c5e97378f653ba4252a01c28c29bb18ac709fb3c5`  
		Last Modified: Tue, 21 Oct 2025 02:26:54 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:9fe029682129fe5ac3361253be902b2249a3d3894941f5b0fb33534a4469a6a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7435895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aaf6673d78fd434cf7d1d818ad74dc1558e29730297f0d0a501da54fbf870ff`

```dockerfile
```

-	Layers:
	-	`sha256:87352892fea345234bc390c63c7bcbf21a979234dc26d3f1cfb70db0ef20817c`  
		Last Modified: Tue, 21 Oct 2025 09:36:06 GMT  
		Size: 7.4 MB (7421525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7086d0d795e12e44128fc8cb39ee43fec4f0917cb1502b56bde4f30771a3bb1d`  
		Last Modified: Tue, 21 Oct 2025 09:36:07 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json
