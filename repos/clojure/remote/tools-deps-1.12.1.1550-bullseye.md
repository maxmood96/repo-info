## `clojure:tools-deps-1.12.1.1550-bullseye`

```console
$ docker pull clojure@sha256:f57ed84cb39b9742d0e6fc8fff6cd28827fcbc2cb8dce1f95852cdc010f6414b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-1.12.1.1550-bullseye` - linux; amd64

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
		Last Modified: Tue, 01 Jul 2025 02:40:23 GMT  
		Size: 69.4 MB (69409686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ac6f753e69744b02db56ef0cc7c47e101c008d928f368c601fc1eb58f1d493`  
		Last Modified: Tue, 01 Jul 2025 02:40:21 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fe0680938bbfb3cc73ca2a1ba85d53116b45f6117b8f20d03c4ab1718fb165`  
		Last Modified: Tue, 01 Jul 2025 02:40:21 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.1.1550-bullseye` - unknown; unknown

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

### `clojure:tools-deps-1.12.1.1550-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e75b1ec1425f0ecb40f7382d6e4fa75e1bf06a78c079f59e94d34ea6cb9433d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.7 MB (277719595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43943bf4863f3dcab83f655bb5ff86de154ea63dab78efa29a13d224bfda1db5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1749513600'
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
	-	`sha256:01b9f05048bbb73f25cf8fdb677f6390611ed20f4945645387ddce6122b5075e`  
		Last Modified: Tue, 10 Jun 2025 22:49:07 GMT  
		Size: 52.3 MB (52252301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc0dcb5ec9d5e14ecff4311df1937f52c510ad6d465139196e19d8c6d8e9f1ea`  
		Last Modified: Fri, 13 Jun 2025 17:31:38 GMT  
		Size: 155.9 MB (155928844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d78257653896b859f0dff555d488fa932e68828bc3174e9d098faef075d2499`  
		Last Modified: Fri, 13 Jun 2025 17:31:36 GMT  
		Size: 69.5 MB (69537415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb1be1cc68135c7836ee785af2f6e0ec25b35a63e31e6462221397dc2b39ce1`  
		Last Modified: Wed, 11 Jun 2025 08:43:53 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a20adb6342263aed8212dce7741768e2753c072fe4fd8b7efac3f25f9cdb12`  
		Last Modified: Wed, 11 Jun 2025 08:43:55 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.1.1550-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:4c0877675ea29eef79d48014c110e0073fc5f6d6798cefa40412030dbf0314d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7421175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b00177c6232ea0cc4cb21693e5a3eeabd2e6da2555d7069d0077be27b4a6f174`

```dockerfile
```

-	Layers:
	-	`sha256:0896e9bbbdc6a563e0121ca30b59a4a74b560b2da459bbad8522256ecad1adaf`  
		Last Modified: Wed, 11 Jun 2025 09:39:30 GMT  
		Size: 7.4 MB (7404539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf5118b2910e3614baafb3703a9c944220d6d4e12507214c159f5fd0aa62cc43`  
		Last Modified: Wed, 11 Jun 2025 09:39:30 GMT  
		Size: 16.6 KB (16636 bytes)  
		MIME: application/vnd.in-toto+json
