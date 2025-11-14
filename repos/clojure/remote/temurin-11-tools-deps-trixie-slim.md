## `clojure:temurin-11-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:4126adf34fe99eac28060c29bc110077107e5a1a0dd7b36fbd9fef79bc67d5a4
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

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ca29a3d355b2d726d0c395fa4d8506820f7ababb69c00b36541a3f52803a23ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.7 MB (246740503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e58e49a9998b3e18c9e89f1a3e30f358c6c59b885ab027b9e9f8b2fb2591de9b`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 00:51:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:51:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:51:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:51:48 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:51:48 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:52:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:52:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:52:06 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96328ff14225645ec90a19c4e83a3881e512470be4f0dff9097f6925fdfd32bd`  
		Last Modified: Fri, 14 Nov 2025 00:52:30 GMT  
		Size: 145.0 MB (144966606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0e212028156562f78b7bf587d634315af533838e96e7d584a1d985f29763e6`  
		Last Modified: Fri, 14 Nov 2025 00:52:43 GMT  
		Size: 72.0 MB (71995146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7830ad3f68dcc2c0092368b1756b1778654ea26b560b676052ae25c99128c57`  
		Last Modified: Fri, 14 Nov 2025 00:52:36 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:33be1739b005b8957226c9296040c20412db4659a6f05ca68fcfa359e0e79f8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5290551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec864bf52518bc9fd6381b0094b88823dd0d44472c170657ef117df8972c70cf`

```dockerfile
```

-	Layers:
	-	`sha256:8e8c2851b0753c0d78b61ddd776fe9ab7f4e3786406d48f312757e8c712bce6f`  
		Last Modified: Fri, 14 Nov 2025 01:38:07 GMT  
		Size: 5.3 MB (5276308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:931aa24b03594cf0bbc24d6d9f280359e96d5291499416f08e3aa20e5fe390f3`  
		Last Modified: Fri, 14 Nov 2025 01:38:08 GMT  
		Size: 14.2 KB (14243 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:03b6cf6ba7f91cfb940753c23aa6b0549bde4aa0ce7a7e9a512ba60ccca4cebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243683066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9250d9c7ab05f2c7431de4f1b04536388f57a27a4238d68e43acb56dbf8844ed`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 00:52:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:52:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:52:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:52:55 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:52:55 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:54:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:54:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:54:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129e1e2ce7c5b4f81f62b8d121a99a7b4768edf4a0dd2651421cdabf8e696bca`  
		Last Modified: Fri, 14 Nov 2025 00:53:32 GMT  
		Size: 141.7 MB (141731579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae678410f4dd99ad8357dd4adf0e51d5f1db7e327d5093d58c536774d52045aa`  
		Last Modified: Fri, 14 Nov 2025 00:54:42 GMT  
		Size: 71.8 MB (71808544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc1cf29a857f43fcdd8fb245722d4630e1d5f6fbeafcfb9349cff5c02df58464`  
		Last Modified: Fri, 14 Nov 2025 00:54:34 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7a1a6ac64e61c9522326ec278f0f9c6e53a17685ae169174e5dd0b18580aa0f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5297056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7f19442e1a22feae040db4a06f3eb927d6122c5d2cb39c57151738ffefb62c3`

```dockerfile
```

-	Layers:
	-	`sha256:2ddd977ba76f64d292c760f30a811470bd7385d4f3fd0a49d06e5fdb1ff3fdbb`  
		Last Modified: Fri, 14 Nov 2025 04:36:47 GMT  
		Size: 5.3 MB (5282695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f207dd6a1204c8564af7cb38cd6ce9e965727256e53d99b217cd5fdac1b3538`  
		Last Modified: Fri, 14 Nov 2025 04:36:48 GMT  
		Size: 14.4 KB (14361 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:2424787f49fb59086c359e29431c1a2c25b9328f75dc71039f97bd9bc55a59dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243078191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04fc70f63f84f05f87e2f7c63a52402839293a0eabf645e8d69e6f97e847fbd4`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 06:48:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 06:48:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 06:48:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 06:48:18 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 06:48:18 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 06:58:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 06:58:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 06:58:15 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba02b519b8b719ee4748bf543f937aad327f5a7c293b9d3f4889b5085d769344`  
		Last Modified: Fri, 14 Nov 2025 06:49:32 GMT  
		Size: 132.1 MB (132081963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516453827da09845a133922f9da30ea88e672bad8beaa815c7c2339ad57c28c3`  
		Last Modified: Fri, 14 Nov 2025 06:59:07 GMT  
		Size: 77.4 MB (77396936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2fa7a4f95da1b876dcdf5e63dff6928fa9bfa3939b64722c1aeb7fc4450b627`  
		Last Modified: Fri, 14 Nov 2025 06:59:00 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ae71c01767c9f60ebc4cb4583b8ca2d54efd24f8f033003e731d7146a38d5d64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5294355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf492a57d222ca3bf3de157f74678b9dbac0f7f93f1f80a07556fb28d4200c3`

```dockerfile
```

-	Layers:
	-	`sha256:d5f7b1025b32c00931aa979665f381571d10b96abff4e75d5f37a89c441b5a9f`  
		Last Modified: Fri, 14 Nov 2025 07:36:33 GMT  
		Size: 5.3 MB (5280064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:429f3e7e4dd76bca2f0ddb5844d3938231d48e703b384affd68d161130683a5f`  
		Last Modified: Fri, 14 Nov 2025 07:36:34 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:03fe89995a47abb6fe7bed3264c35e6ae4c7bf607084e81101d8da040c330d79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228486325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d81e14ae7baa601dcb1e1d0ce0e14e6aa111406b9c2bf9567ebe3f79db34d2de`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 00:52:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:52:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:52:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:52:50 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:52:50 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:54:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:54:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:54:57 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6345b0ba4ab712f7cc510aad027ef83b70aad351c8a0761add52239f87322f00`  
		Last Modified: Fri, 14 Nov 2025 00:53:44 GMT  
		Size: 125.7 MB (125694447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6501b1bb4e7077f613c58caf38f388261040fb408a4c3fb679223ccc98dbb3`  
		Last Modified: Fri, 14 Nov 2025 00:55:31 GMT  
		Size: 73.0 MB (72953840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d647a262a190a4c08e49ea7964d213ae83dee8d39d4706416a47ec947d380bd`  
		Last Modified: Fri, 14 Nov 2025 00:55:24 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:daa8580a92dc5030dc73c90018b4b28b4f0086c03c9bcfade9d71721797c3a61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5286479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87b9c7fe78a31e2812aa2278c2b2b82fe0e2722b778d732991dd11491f6f9203`

```dockerfile
```

-	Layers:
	-	`sha256:612588e0768d94acaa6ca722d5ed531779c12e5cdacc0957c5ef65153f1e5061`  
		Last Modified: Fri, 14 Nov 2025 01:38:22 GMT  
		Size: 5.3 MB (5272236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c308ac85c0a8b462fa5ac63925fe3c60d98a8ec38879953bfecaa57324ca834c`  
		Last Modified: Fri, 14 Nov 2025 01:38:23 GMT  
		Size: 14.2 KB (14243 bytes)  
		MIME: application/vnd.in-toto+json
