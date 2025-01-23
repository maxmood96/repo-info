## `clojure:temurin-21-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:c9558a0ee51f30bdbcec1e0cc51a7dc0c96b5928e7255c2723b56d928e85d713
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:37370126e75367c837a696bff6184159900cf0df907dbdb7a3abea0e0627a57f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.5 MB (280487403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26dbeb9bcd86f400c53849e3f5d0dbd22476a2e8fc4a8865d46518492204e1fc`
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
	-	`sha256:de97e8062e06250e3c3cef0d40cfe62111bb4b74bcf6221e25a06452dacffcf6`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 53.7 MB (53739164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2176b2d01f419bbd22117d470d594e2ac21fe2d96f731aa22f80eb1458e63fbe`  
		Last Modified: Wed, 22 Jan 2025 19:37:11 GMT  
		Size: 157.6 MB (157568693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f3930511481c748162a9bd997e99c7410b975c15444f2b389e470239700297f`  
		Last Modified: Wed, 22 Jan 2025 19:37:10 GMT  
		Size: 69.2 MB (69178504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebfdb279bf521f3cb316624a1ca4d4d02dbd9c9053a10f9e6610cc7a4ab0e892`  
		Last Modified: Wed, 22 Jan 2025 19:37:09 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8444d161b084fcddb66da6a009c074a4c54f4e142bc0cb93a727ba76ebcac1c9`  
		Last Modified: Wed, 22 Jan 2025 19:37:09 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:b6597bea6e715dba1c487de74381486ee5949acac258dab3a4a0f6fd08ba63cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7224832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad642d153e42b3f2137dba487b6f38ae6e87e6b2bd6048d9c6c26f44c0d5d056`

```dockerfile
```

-	Layers:
	-	`sha256:a80fddfd6f92f6ae8a36e0f9a706c89d46fa1f67cdb59e9b21b4f2da9838d3cb`  
		Last Modified: Wed, 22 Jan 2025 19:37:09 GMT  
		Size: 7.2 MB (7208335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:277378e5d5c4b5da4079c01ca4a47b8a31076ce94dee78acb12e0f0df6cf6b29`  
		Last Modified: Wed, 22 Jan 2025 19:37:09 GMT  
		Size: 16.5 KB (16497 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b25f48ac4606f667cb351174d18a7ce91bfa81d7d609d198c5e792ecd4b565f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.3 MB (277344924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daab9e6fa2fcecb964a2b231e0749f22b866d3607eeb810237748cca0c02321c`
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
	-	`sha256:1270858b2b9cb5d47abd119b946534b70ff7d09f29c425fc07b280e5c28971c6`  
		Last Modified: Tue, 14 Jan 2025 01:36:12 GMT  
		Size: 52.2 MB (52246060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbaed61333d448587c75d37b7e4bbd48824a358426cc2231c04825daf1e805c`  
		Last Modified: Tue, 14 Jan 2025 12:34:46 GMT  
		Size: 155.8 MB (155793168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25093e468939f2f4ae56587f51d23f632dcba4e17b738fde5b0c90681b66bf58`  
		Last Modified: Tue, 14 Jan 2025 12:37:09 GMT  
		Size: 69.3 MB (69304659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd6260537e9d38fce5bc52866633755b45a316c9e50b9893ec79386b1102e39`  
		Last Modified: Tue, 14 Jan 2025 12:37:07 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd740b62c98fcf12c71ea090c70b60600dd8435c6dcc962dd34b90523f32b92`  
		Last Modified: Tue, 14 Jan 2025 12:37:07 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:30868e467b0d89507fd3e62afaaf3f689b4fc06a7cc76f7214a17d661ed8cd78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7230097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b5c70aa71160967d4fb3a739c2abafdb485cbf3044000e236583632ad8ae6a`

```dockerfile
```

-	Layers:
	-	`sha256:a2675d8d894a88d108d1d59cb6636e810aed74a0bc466b8a6e85971d84701cb3`  
		Last Modified: Tue, 14 Jan 2025 12:37:08 GMT  
		Size: 7.2 MB (7213458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:949295a56189a3cf4f36dc1ddc10b3df33a753d02eb16823cb0902ab4be535f3`  
		Last Modified: Tue, 14 Jan 2025 12:37:07 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json
