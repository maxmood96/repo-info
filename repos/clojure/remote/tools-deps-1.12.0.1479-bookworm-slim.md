## `clojure:tools-deps-1.12.0.1479-bookworm-slim`

```console
$ docker pull clojure@sha256:5b66f384f04f6f71f2b782fb0f12488b8221133df7086351d3fc441455b43ec8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-1.12.0.1479-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6b217981a3952f747cf12cadd0e573f89189108ca131e94d4c7481442e69c5ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.2 MB (256184609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46243c8757d776163e2c789dff47b2354ef951e8ca31e2e30e70f244e5c11903`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a508a80b47ab791a3c316a7995bf7dc31f191f6f299c11ce462146ce03030dde`  
		Last Modified: Tue, 12 Nov 2024 02:24:38 GMT  
		Size: 157.6 MB (157568686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be46ba7ac074ddf6808f22eafd620d9f3c32612eb3923634949bcf6be960e929`  
		Last Modified: Tue, 12 Nov 2024 02:24:37 GMT  
		Size: 69.5 MB (69486886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2289eef2e49388214da6548b776c3f7f89e942338c5e8a30c6c67a20cf2c5f`  
		Last Modified: Tue, 12 Nov 2024 02:24:36 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5cc06e8400971402d57e6d455c2adfcd4c66a3b31f19fb0d2a2c9f4250bdcc`  
		Last Modified: Tue, 12 Nov 2024 02:24:36 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6d6235ea9701f5fe0244ee28cf6a7b9d93574e6f50d40dc1691da2765af7d9d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4941005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2425ed98d92d634f396068b4bd58d99077ec5722c16ee27254d5c9e985965de5`

```dockerfile
```

-	Layers:
	-	`sha256:41fa074b5a93529697fbb30ad3bc2f3ac202f68dfdcdb06831fc1e986fa62f52`  
		Last Modified: Tue, 12 Nov 2024 02:24:36 GMT  
		Size: 4.9 MB (4924431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf3044ef91298b5ed25685b3fbdee496524870237d2d8252043c487b188e398d`  
		Last Modified: Tue, 12 Nov 2024 02:24:36 GMT  
		Size: 16.6 KB (16574 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.0.1479-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:59ec4d30db6b47867f0aef649c06479549b9018f6aa08dfa49dc8234fe424a79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.3 MB (254286267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d147f92ba528fad11f4b19d948dec0727a99a6b59a9cb06756777d35ef6141`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3054732fa24dd2c498471a73cee8487d5121eff8cdbd9d249dd36d57b9a224cd`  
		Last Modified: Wed, 13 Nov 2024 01:26:18 GMT  
		Size: 155.8 MB (155793092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eebd5d00a5444bc06777a293377efe3c46ec11e319c8385da350d8a1d30566e`  
		Last Modified: Wed, 13 Nov 2024 01:30:29 GMT  
		Size: 69.3 MB (69334779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b27b4486c3b9eb4ec3d102874520712a39970212c703f8b775e5b6190b8888`  
		Last Modified: Wed, 13 Nov 2024 01:30:27 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33008fb8688cccf5f8b2edb6118a11b98891a5ca0208068bdedb004805bcbf4d`  
		Last Modified: Wed, 13 Nov 2024 01:30:27 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4b1162c20517797c654d126630cc2cc84a615716354c62fff38f94c5f691bf7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4946937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d431d49a305d19be0e4a95795733633ef36cce3f2c1045979518dc88f9e81a30`

```dockerfile
```

-	Layers:
	-	`sha256:8dc38579420c1956eb131a6309694ff9966dabf5e177f7f2dc7b63614265f214`  
		Last Modified: Wed, 13 Nov 2024 01:30:28 GMT  
		Size: 4.9 MB (4930221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:888958cc1c67a301fcc990f484138857fa243f2907766962891b4c286310f90b`  
		Last Modified: Wed, 13 Nov 2024 01:30:27 GMT  
		Size: 16.7 KB (16716 bytes)  
		MIME: application/vnd.in-toto+json
