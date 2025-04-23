## `clojure:tools-deps-1.12.0.1530`

```console
$ docker pull clojure@sha256:d07d9f8cc7f29c658d7f0516495009b7b29089f5913c840e7f4db6e697e32a74
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-1.12.0.1530` - linux; amd64

```console
$ docker pull clojure@sha256:9b3a1def5b4db60d9a099a8f7fb5aef89b408f3d65cd4418d498fe5635fab31e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.4 MB (289426641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72dc1bbd614cdaef34b9652dbaf11dd1a03c42a5bba84b2255cf34196bf0980e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:23b7d26ef1d294256da0d70ce374277b9aab5ca683015073316005cb63d33849`  
		Last Modified: Tue, 08 Apr 2025 00:22:55 GMT  
		Size: 48.5 MB (48490541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f034b0308d1e2fe51ace71e3e8ca8c3405b6eec9b23977b3d1d67c7262803a`  
		Last Modified: Wed, 23 Apr 2025 17:16:31 GMT  
		Size: 157.6 MB (157634413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b6781ff396fa0bcaab8713a7f7f6521eaa7c23a9879bdea0875b61b80b93186`  
		Last Modified: Wed, 23 Apr 2025 17:16:29 GMT  
		Size: 83.3 MB (83300644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bdff747b602360819cd96f854a0b62a7739ba1509e8a42d705f37dd3a9a8cbe`  
		Last Modified: Wed, 23 Apr 2025 17:16:28 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc9ae7e5acfcabed101ca3424d89eb767b43e1eedccb521ec7f726e9bddbb2d`  
		Last Modified: Wed, 23 Apr 2025 17:16:28 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1530` - unknown; unknown

```console
$ docker pull clojure@sha256:35ee3b357fec6cc1b03b4f41926396e5f5a802b021fbbd879d90a8b2b344bd2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7195399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecf406e8ba845d79d6e2eacb92f29f3546b2ee62727955aec5810c97ed14cd6c`

```dockerfile
```

-	Layers:
	-	`sha256:c430d6aa10d2eb2c8783822c256c5cf1e963856fccc895820950b8cbaef2929d`  
		Last Modified: Wed, 23 Apr 2025 17:16:28 GMT  
		Size: 7.2 MB (7177578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:031f87c190ce92756a05f7c7f883c55f96fab927b32c31ec1b89ca6e2c6c2ff3`  
		Last Modified: Wed, 23 Apr 2025 17:16:28 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.0.1530` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:082d20bdf23f65d06b762dd0e63aaafecd809747509cab6ac6f83795b6ce2dfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.4 MB (287375957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c27ccd960ddb9fd3c4d2daf7e4b447a3383a432b6ecb9203e42c9636cb06bb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:71daa2c787b0984bbf3b93b60686fc9fe305d28e833914019b2745ab9f36730e`  
		Last Modified: Tue, 08 Apr 2025 00:22:46 GMT  
		Size: 48.3 MB (48327469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771e0574ee8af76655a2c97a3503c5fdf5d9484db1a222049918a5010c5d4b75`  
		Last Modified: Wed, 23 Apr 2025 19:35:02 GMT  
		Size: 155.9 MB (155928754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:490e1adc34cfa6ecd2cf4c1a585a3014a00acedcaf6372b13b19ed309f5cc4fd`  
		Last Modified: Wed, 23 Apr 2025 19:58:35 GMT  
		Size: 83.1 MB (83118688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e554a4ff48f61f2e4d83f9892b8d3230fe025dfb6a606092b584c1ffde8ec6`  
		Last Modified: Wed, 23 Apr 2025 19:58:33 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b74e8e57b6f8eabd6f15d9137d421a48ee6c2aafb12990b17ba84b0d46db45e`  
		Last Modified: Wed, 23 Apr 2025 19:58:33 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1530` - unknown; unknown

```console
$ docker pull clojure@sha256:acac36cc51d4cbac62f7c659917280a1c334a64783e5eea749920eaf95c574de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7201424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89bb442a97b0bbeef69b00696403656db55499f759e32a73bf18a69d7688ed73`

```dockerfile
```

-	Layers:
	-	`sha256:13b606ad7e58e2bfae5e30b9e5d43cba4552bb44c77707a9cf3021cb4faf4045`  
		Last Modified: Wed, 23 Apr 2025 19:58:36 GMT  
		Size: 7.2 MB (7183413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bec7aaec409a47b7c48ac1ad46f114ab49c3c1cef1d4f53335b94d79daacb66`  
		Last Modified: Wed, 23 Apr 2025 19:58:33 GMT  
		Size: 18.0 KB (18011 bytes)  
		MIME: application/vnd.in-toto+json
