## `clojure:tools-deps-bullseye`

```console
$ docker pull clojure@sha256:a7bc643f1d4e78c920fee94bec1562ac2656b164f861173a87842ce6d9dd77df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:eb6eec035f6219fcfe8d5902a9b42d310977675908a56007fd23f36d374a136c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 MB (280800053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83b0005057b155b61f281896b8f57f9534cc39eab61c31cbe415c3df8dc4b5d9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2d765646d883a37610a09973a079fbba4c7596e54d18d0447bdfff142389d1f7`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 53.8 MB (53754822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e78cd354fe4b3fed7295da6ea1671d0fa79052733bf807863822f394cd598a`  
		Last Modified: Tue, 01 Jul 2025 06:52:48 GMT  
		Size: 157.6 MB (157634503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580e043f3ac248ec6bf5fe9968426dd40dc05fdb6164009bdc6a21efbd32c2aa`  
		Last Modified: Tue, 01 Jul 2025 11:23:56 GMT  
		Size: 69.4 MB (69409686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ac6f753e69744b02db56ef0cc7c47e101c008d928f368c601fc1eb58f1d493`  
		Last Modified: Tue, 01 Jul 2025 11:23:54 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fe0680938bbfb3cc73ca2a1ba85d53116b45f6117b8f20d03c4ab1718fb165`  
		Last Modified: Tue, 01 Jul 2025 11:23:54 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:a547c337c50a4bb4f4cfc678e0f4ea8ec203356165495fea60fefaf831da404d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7415913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83d15cd9301a4ce52d25cd820f0dbb939309a821b65f5097c55d7b3af7ddf44`

```dockerfile
```

-	Layers:
	-	`sha256:9044d0bfd3e31f0a021c0a5ecfd1cb278be073d4e8c7f6ade25a76a429107e4a`  
		Last Modified: Tue, 01 Jul 2025 06:38:55 GMT  
		Size: 7.4 MB (7399416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:513321b230aef04cc0c99fb9bdf75e8426d8ca53b5dd06554c8f977261dbe9d6`  
		Last Modified: Tue, 01 Jul 2025 06:38:56 GMT  
		Size: 16.5 KB (16497 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d761c93e87c785a7d73abe216da2e5c6aa064195e8aa054dbc42bc001df7906b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.7 MB (277719684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e04afeaf27b8c77c33a48115c76987a0697660cedadd1e12b1de9862cca23996`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:df45b4853b6fce6b81d1ac6218d861c6d7c8c14da4be409d42ee4bfdf0737e71`  
		Last Modified: Tue, 01 Jul 2025 01:15:18 GMT  
		Size: 52.3 MB (52252254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b42119ba0f8b050f01710505b7530a9471f982c77bab1989606c214f32fce0`  
		Last Modified: Tue, 01 Jul 2025 12:28:56 GMT  
		Size: 155.9 MB (155928817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0267fd0081135e7adf3f2d10ed7747b7cb0207baa73ada1b760da1f5bb859dd8`  
		Last Modified: Tue, 01 Jul 2025 12:33:39 GMT  
		Size: 69.5 MB (69537573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4df9ab5a71443a9c898f36d71f164b315072ea2e0925fab31948b372c67764`  
		Last Modified: Tue, 01 Jul 2025 12:33:35 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be0f542e92b227f845f54cb97e5c4fb1b8f2be304506c8b3585454762e379b2`  
		Last Modified: Tue, 01 Jul 2025 12:33:36 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3e6c04209e498ae9cb9bdbe26386d321890a3264aaf3d6a0e9d7a72e6d7dcd85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7421178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a65acf904027d297d1aa55a94b8f61249f5cc564eb723a9d82bbf06a1ee7818c`

```dockerfile
```

-	Layers:
	-	`sha256:4829ef8c0ce9f9f760fd7235ed7e8a92cee7926f824cdef26c682ba41b7a7a0f`  
		Last Modified: Tue, 01 Jul 2025 15:38:31 GMT  
		Size: 7.4 MB (7404539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93e86131875b86b26cbd323c4d8043b6a5ca7617f99cd9e5dfa499680455bed0`  
		Last Modified: Tue, 01 Jul 2025 15:38:32 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json
