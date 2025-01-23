## `clojure:temurin-21-tools-deps-1.12.0.1495-bullseye-slim`

```console
$ docker pull clojure@sha256:2a718c69d54e360f65e6fe1019f7e225dd23ea5a11822cddc5e2e8e36495b565
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.0.1495-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b61324e9c9b2eab28ed795c07b2d56f7fd5538ee2235306c340e3c1570a36d3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.6 MB (246603439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c57948d6478f8b6745255ce111affe0bc1bd88f6b89eb99b7524e82ba9e2a39`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0e8f8ac2fb004af72dfa57d8787211dbb64167ef4cc1e7893c5adf27744c29`  
		Last Modified: Wed, 22 Jan 2025 19:37:12 GMT  
		Size: 157.6 MB (157568705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2923316c50c02c97374049af52f2b3329caf5adff600795764977274ca9b7622`  
		Last Modified: Wed, 22 Jan 2025 19:37:11 GMT  
		Size: 58.8 MB (58781025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50637358b75323f629f749adf5d89277a0fc8275ef66c682761f5f06d2969200`  
		Last Modified: Wed, 22 Jan 2025 19:37:10 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136db5629a6b4556fa4465832d5cb896ab34e1b293438333560cf911a147b916`  
		Last Modified: Wed, 22 Jan 2025 19:37:10 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1495-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fa420638f4db26ce82e60ee3266136163e496ffc2289221d99440b2223d52a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:124c6ac7cb56acdb969beae47a91e390136da796b9e3316d39c0263ed0507d55`

```dockerfile
```

-	Layers:
	-	`sha256:dc93d967a796b75396d7eec46ebfa092c9157ed171b0202c39ab5eef0ea2b839`  
		Last Modified: Wed, 22 Jan 2025 19:37:10 GMT  
		Size: 5.1 MB (5120867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f25106b95e2938a32ee86cf4ae88fc185d71e3b4878c9fd91cf5e7e9218a795`  
		Last Modified: Wed, 22 Jan 2025 19:37:10 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.0.1495-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:837cf1f562e7bb42a8cb4f8f57cb2559172ce5a521159cf0b0eba16602f2da6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.4 MB (243444151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9661f3ee49e6fb40ff738963017e94fad7f968c23ae096d08a03e9a102fc57ac`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55539c7f273509ebef282fa1d891a4509c722ccc8a21bfa5ea9e1bac67e688f`  
		Last Modified: Thu, 23 Jan 2025 02:56:29 GMT  
		Size: 155.8 MB (155793069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b80ebab2dd95fe6568604e8e8d4288498ff8ed0bada523ca40f47fad177546f4`  
		Last Modified: Thu, 23 Jan 2025 03:01:12 GMT  
		Size: 58.9 MB (58905126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:532b5eae892ce1cf7238ae7ca1fcf1da10ad343e9daba65fb60aae41414cef45`  
		Last Modified: Thu, 23 Jan 2025 03:01:10 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0041b58b638bcb7e725a02e8920c594185c4eee702c205e32e0eba2810ee34c0`  
		Last Modified: Thu, 23 Jan 2025 03:01:10 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1495-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b947f045919c5c3373421445e229df8c3cc6bdac74b98e76b16050eddc680201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5143340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc67573a6d7d1fbe11213bdadf0d69f9c76075430ca3d400060c8cefd7da68b`

```dockerfile
```

-	Layers:
	-	`sha256:e9a0c537e2c4c8c7552518368080d79f34f148f2fe49ec03133693eb06a1ca10`  
		Last Modified: Thu, 23 Jan 2025 03:01:11 GMT  
		Size: 5.1 MB (5126623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ec8425c602bd436f741b94b14e19021357a2cc33df154f245fd8527e892be2e`  
		Last Modified: Thu, 23 Jan 2025 03:01:10 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json
