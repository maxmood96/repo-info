## `clojure:temurin-17-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:f88fe1be52a4f3e15e94f61a0b970c9063e6a7bd41895cdb5d634c685da7e99d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:5bb38d74235a5caa45b389dec7fd03bec07bc8e69bafcefdd9c8013a6954df13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.9 MB (267910482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:616e4f00701781bbeb199684e0e1ab2a394d619e3ac4a5326ae36a95e370ca04`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:078965fc7cf303b72cc4eef5479dc2dbf5bc84fb8e6052a89b9b5362e14b3651`  
		Last Modified: Tue, 12 Aug 2025 20:44:43 GMT  
		Size: 53.8 MB (53755344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9b1953779a7967ef001f7145905e0bf1e35672708bf1a82fcbbe0fdd4013b0`  
		Last Modified: Tue, 19 Aug 2025 03:47:04 GMT  
		Size: 144.7 MB (144693284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdfc6a050e32784be47b52f4c7280a15f7ada6a5acc50e749bfeca36812e0f5c`  
		Last Modified: Mon, 18 Aug 2025 16:53:21 GMT  
		Size: 69.5 MB (69460811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f5a0d6413d509ab281a68593c01374baa65563dbb92cbed46f5d6712c04c66b`  
		Last Modified: Mon, 18 Aug 2025 16:53:12 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ab509dac36d7a575f13ea8d497fb0fcae56ade0559a41e47e9f9f902b243f2`  
		Last Modified: Mon, 18 Aug 2025 16:53:13 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:e0487c0bc4a51c0feacdbcfe5dcdf1a32767b874a156e3e1065fdf381420172e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7411487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81d05135993b94f85063bcfef8bdace6ed962416d9a62d85f97dadeaab88e815`

```dockerfile
```

-	Layers:
	-	`sha256:cf425d666103984a8750467b2ae9c079ae6ef116399c6001e1ccbbaf9d1f942f`  
		Last Modified: Mon, 18 Aug 2025 18:37:36 GMT  
		Size: 7.4 MB (7395667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c2b091dbaa8a856bd1853e52b3db8942d320165b8d11ae8486310e52cb69625`  
		Last Modified: Mon, 18 Aug 2025 18:37:37 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:42dd2ef3437565f96e4e13bace34337ad0f71c3c7e76261bdd52cf78292016c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.4 MB (265380071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:925ee631eb5b73063d0e087908999cbde9739683878e170b414808e35636b526`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7b68ea47bc3cd8615e51fdbe0976cb4999ba56ce8764e755543a4521d69a32f6`  
		Last Modified: Tue, 12 Aug 2025 22:08:57 GMT  
		Size: 52.2 MB (52248409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df15f2eff937c38546ced8d4865e045d0e5e6d5f3bc0f26200a5c72c013ca2e4`  
		Last Modified: Tue, 19 Aug 2025 03:49:08 GMT  
		Size: 143.5 MB (143542129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1d3abbd8dbafafa13c60a8d170392cd3cbd33e150ca2ef26e9d418cd0392cc`  
		Last Modified: Tue, 19 Aug 2025 03:49:04 GMT  
		Size: 69.6 MB (69588491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe12644c826e532c222f16d970d74fc292c105b746b689f9e3c385d7698a6940`  
		Last Modified: Mon, 18 Aug 2025 17:10:55 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aecb4fa7ee72a577037d645e1c6bb7c758f5e10a2a7e844656f1d97b0da7644`  
		Last Modified: Mon, 18 Aug 2025 17:11:00 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:1ece241f410e88a0e1c085d2e09a76ba718b00d76f6c7b206fcaf6fc9d3bae5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7416705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:067698b3c7c5d9db6ef6f75fa1493b6fd236c6a4afdefff605ce29a5c9cc2e4b`

```dockerfile
```

-	Layers:
	-	`sha256:70c7877f0a4644719313c2011d4b536c94e4aba828fcd03af81909018102e27c`  
		Last Modified: Mon, 18 Aug 2025 18:37:47 GMT  
		Size: 7.4 MB (7400766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b33fa58060671001f22abe9ef8c6a357f7ae9155f0dd28eecfe4eb516d7ae40f`  
		Last Modified: Mon, 18 Aug 2025 18:37:48 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json
