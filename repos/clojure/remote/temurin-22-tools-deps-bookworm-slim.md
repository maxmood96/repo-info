## `clojure:temurin-22-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:fdf437e460ebb28f6932aefa1ec7da0d8f8752341f7b178430028024da131e95
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0a6d2e7df1d0b51f9394279b5a65a8c77d8f78639d1567196e368d64d9cf4380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.6 MB (254633270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3a95c51c35f47464cfb6b465570dc3933f28e8d07713ba93c24791a6c5e177`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2f882b57155c1b63fa3afbc704c982868f22322db94bca4638bb3f43822271`  
		Last Modified: Tue, 13 Aug 2024 01:11:33 GMT  
		Size: 156.5 MB (156481579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6372d9aa56bb83ddd9cd3f8d12a2bbb014ff8d5066bea24454393cc083dc40dc`  
		Last Modified: Tue, 13 Aug 2024 01:11:31 GMT  
		Size: 69.0 MB (69024420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a00cf5db8d19d6086ae0d0c439541d12fe46d8edac2a873e9a36d742f68625d`  
		Last Modified: Tue, 13 Aug 2024 01:11:31 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3833e8c599f124d2c655cbfd1e330911188bc3e018b53e405ad09aaf48929d`  
		Last Modified: Tue, 13 Aug 2024 01:11:31 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:110c67308f8a0028e13a1f33a2e4eec5bf77923580f2b39533a1455e06dae5c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4760670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10d633218c8ae3139b6f9c19d1b9e7fa01ba6b687ca947fe408abe3e452fbfce`

```dockerfile
```

-	Layers:
	-	`sha256:15a9154896bbcaa82d6c56048e7230354ac25e39d1fbff877b59183b9a0e37c4`  
		Last Modified: Tue, 13 Aug 2024 01:11:31 GMT  
		Size: 4.7 MB (4745158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f85bd8c9d9a48cb7824a7f0e855a383b7304a0ef52918d2c041b54a6d02313c`  
		Last Modified: Tue, 13 Aug 2024 01:11:30 GMT  
		Size: 15.5 KB (15512 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:aebdbd81e0ebab18462895e8f05f64d7e2baba418d98d7673ff3598b775aed8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.4 MB (252434232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e87ea4022778ce8a6616bffd6f545af1083e488ef836f26007b5044e7e40c1a6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c142b38ffcbff18bde51f24b46783a56c2e920d03361ae340f0228c6870b66`  
		Last Modified: Tue, 13 Aug 2024 06:45:30 GMT  
		Size: 154.5 MB (154503733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99fe304648c3b55453bd96ac8c2417dd9c4a8c2be7abf0f8ffbf22fe540d44a7`  
		Last Modified: Tue, 13 Aug 2024 06:48:56 GMT  
		Size: 68.8 MB (68772933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2946c53673f0b1deb6fa7a18ce4dfd128a457f325b80b4a49235ef37284516aa`  
		Last Modified: Tue, 13 Aug 2024 06:48:54 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51f9ed17817513771682ce865c422be5520f5c3b69b23d1ca63012fd4b7db76`  
		Last Modified: Tue, 13 Aug 2024 06:48:53 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7e23975f9c68479fc10f5f416a3ed7c29627aaeee973f6b2e18420efdbcc80e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4767597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:922f7b6be4af23a91989a36f8765f7d3be22a476d2b8e23086ed40d76e4669cb`

```dockerfile
```

-	Layers:
	-	`sha256:ecfb9f248a8b9cf1e9688cb0b7a23e886b2cd0be6d7af331cfc7f0bb1c989ec1`  
		Last Modified: Tue, 13 Aug 2024 06:48:54 GMT  
		Size: 4.8 MB (4751543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dff254810768d3c9522b05d382cfad0858987329e0994863dbc8eb23eb472ebf`  
		Last Modified: Tue, 13 Aug 2024 06:48:53 GMT  
		Size: 16.1 KB (16054 bytes)  
		MIME: application/vnd.in-toto+json
