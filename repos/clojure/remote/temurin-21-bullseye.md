## `clojure:temurin-21-bullseye`

```console
$ docker pull clojure@sha256:52a4c7f21411e27744ce2cec5aa1b1641798e49a6cf6787ba9f75a046719f973
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye` - linux; amd64

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

### `clojure:temurin-21-bullseye` - unknown; unknown

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

### `clojure:temurin-21-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:99a8773516960cd33012b668ccd5586b95677190a9cc944e04629bae3cea0430
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.3 MB (277344617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb4cf9fc102c89e44a22e69c50ebe489756f55cf2872bdee6a0b219b36c949cf`
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
	-	`sha256:17eda5fd7e4740de452e0eb0971c85821bbb430f489028d0235cb971ae002be3`  
		Last Modified: Thu, 23 Jan 2025 02:55:26 GMT  
		Size: 155.8 MB (155793069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32dd37a33bbe3ec16ca52a0a53591784d52111bfbdf718c34b499eb3b8f5359`  
		Last Modified: Thu, 23 Jan 2025 03:00:22 GMT  
		Size: 69.3 MB (69304446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd00473e99a47c4ae8d3b324baa8b2821c947c1e69dfb209d0f494d92e8082ef`  
		Last Modified: Thu, 23 Jan 2025 03:00:18 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc1fb7c27365a9a2cbab1d992b8503147c518662ec8cd60290be0f20a5505e7`  
		Last Modified: Thu, 23 Jan 2025 03:00:19 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c3fde82999bb7a647095b965cef004988fae362c35f61e161385f83bcfea36ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7230097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc84e1008f97b36a3160995bb814beaa75d64735ee6aca5aec1d1c09476cf498`

```dockerfile
```

-	Layers:
	-	`sha256:20d072f0e814f55ede05e6dcef82f8a17eb931ab11d810ec236edde0d4a57ab7`  
		Last Modified: Thu, 23 Jan 2025 03:00:18 GMT  
		Size: 7.2 MB (7213458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78940565b3e9291a0acebaa139aa2aaa537b061f06710235f4730f5c6daa77ac`  
		Last Modified: Thu, 23 Jan 2025 03:00:18 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json
