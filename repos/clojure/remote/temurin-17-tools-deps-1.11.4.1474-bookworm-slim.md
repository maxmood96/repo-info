## `clojure:temurin-17-tools-deps-1.11.4.1474-bookworm-slim`

```console
$ docker pull clojure@sha256:5e2b11df0d3b3aeeeb6fd5d1d055a9ace4f1f1a7c3f639781abc9e7686d799fa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.11.4.1474-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:11220a3667c6cb9234db9e04d4afd9679dd50276d25a4ed88ee0138688f7b8d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.3 MB (243317560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ed2c9bad4b419b238315376a9e88d91abb379a5c8dcbb65de785f8a396b3573`
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
	-	`sha256:bada435c6abf18892682e64339c148566831f18dc40ad5858d2cbb6d34c540ec`  
		Last Modified: Fri, 23 Aug 2024 20:02:20 GMT  
		Size: 145.2 MB (145166507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4bbd0f97338b1fbf49c246643af89bc082db20e9ff02b6e26d1514daf1df00c`  
		Last Modified: Fri, 23 Aug 2024 20:02:18 GMT  
		Size: 69.0 MB (69023778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e276a7e8dbb20b8593fd9954eb897ed5b528fb19de04f28b71e7577815a2062`  
		Last Modified: Fri, 23 Aug 2024 20:02:17 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6fe3dd15f3fae6c4e876d65b6acaaeb1258aa9901e3a4ec3e54b06d61b7803`  
		Last Modified: Fri, 23 Aug 2024 20:02:17 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.11.4.1474-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ccdaf9d2e9632ba390fd63064899986ae2edec63cc3dfdda8d3f47cd634068c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4760677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a7f3f72e2002b93a27df40dcd1aabe4496486bc5ab8957856b18e4fcc7ba730`

```dockerfile
```

-	Layers:
	-	`sha256:22b6cefb730ac2f205925f974db1c3f67adac8c5eb43041d185fbdfd59b1ccc2`  
		Last Modified: Fri, 23 Aug 2024 20:02:17 GMT  
		Size: 4.7 MB (4745164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93489f2eece550dcca2350438f4b200204c057948ddbec16b19f504dbb4371f5`  
		Last Modified: Fri, 23 Aug 2024 20:02:17 GMT  
		Size: 15.5 KB (15513 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.11.4.1474-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:75e4b6e2fd4e4797c5059c4cecd4fe8980e7bfcc84e3ea9edb48a148243379c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.9 MB (241890359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd78fd3b904d21bf7ea6274f3ade1abb6825297cd8cfec2b7f5a80e2a765834`
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
	-	`sha256:e0215db3e3aa771746614fc4e3673f71f09461c4bbce29be5c787da057a5ee10`  
		Last Modified: Sat, 17 Aug 2024 06:12:19 GMT  
		Size: 144.0 MB (143959503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf15fdf76d024d73012191eb0b087fe0bbe07831d57413f83f74e1deee92c8ba`  
		Last Modified: Sat, 17 Aug 2024 06:17:28 GMT  
		Size: 68.8 MB (68773286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:983ea26cab84cc259cb3ac5e1385dbdd847ec510e80f2d91a96de556d6fb4c9c`  
		Last Modified: Sat, 17 Aug 2024 06:17:26 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c32176aa1210302b6cd2a442fdc4dc433e69e3f0874be8665edf687b8ff3f93`  
		Last Modified: Sat, 17 Aug 2024 06:17:26 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.11.4.1474-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c0c0f8442f3acc7fb7bfd07a892ef189a0c3a486181936e5dbc8e62aa69379c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4767602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a947192a13e837c94117476d3a53db477692ee180b09ac0b948d3c6cf4f262d2`

```dockerfile
```

-	Layers:
	-	`sha256:3a0c11fa92319f8c77eb4a1c244772e5bba655a4e3bf5544b94d70477f1f4069`  
		Last Modified: Sat, 17 Aug 2024 06:17:26 GMT  
		Size: 4.8 MB (4751549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f989797181b64d47055c51cc62a342798e99955dccf0e6f8d782e899f6ba591b`  
		Last Modified: Sat, 17 Aug 2024 06:17:26 GMT  
		Size: 16.1 KB (16053 bytes)  
		MIME: application/vnd.in-toto+json
