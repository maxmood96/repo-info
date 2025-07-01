## `clojure:temurin-11-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:311220da352bb2650999e7dfcc42f004f02e6549149ac5ac5b3003b8be497d35
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:520581583c803a9fc161c918e51f18d17c746216ebf1bb4a3447013a560d35fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234897602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89d64b11acf26a4838b3a3af18eabdfa19b4f30a0214ddf721ec60cf9d609e99`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:cc41ef31545f10925901837c6dea7e184299788097caaa3fabb57ed109c52a98`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 30.3 MB (30256047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7547776343a3f86c5dd644cfa47d292c3f64406d4a7188b72c03ae511c828dfb`  
		Last Modified: Tue, 01 Jul 2025 14:25:15 GMT  
		Size: 145.6 MB (145635675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9591f6f703fe839483501887bc13179fb3685f4089ed3c05c67c7d7e5f9bd4`  
		Last Modified: Tue, 01 Jul 2025 02:39:12 GMT  
		Size: 59.0 MB (59005235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cbe64b1d0fd0dc05156d7bc631349227da82058ef0b29c459f43b0b560cf8a4`  
		Last Modified: Tue, 01 Jul 2025 02:39:01 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:610d7a38e797dd036a2dba641d54efc9d4cdebfe60d21b675cb5d9c0b9653697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5342489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b9f20df88d32773c63f0e2685547db31b44e691963b2a81029e11c0484e9fd7`

```dockerfile
```

-	Layers:
	-	`sha256:79638aabf2bbcbbaf7bbb1b94655c70ab95a6e464275c95335d9538ac47e598c`  
		Last Modified: Tue, 01 Jul 2025 06:35:29 GMT  
		Size: 5.3 MB (5328179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eec3bd7a1f847a02075846328e78eace9209bb22e0fdf161ecb895dfae112c0f`  
		Last Modified: Tue, 01 Jul 2025 06:35:30 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4b2e8c8e02ac448c7fa672fa9a9310321f9d0d859593926012ffe5b351304f50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.3 MB (230302955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41e821dd3ee5372f0f891944ec0198764a6aec7745d2e05c21aceb695af6fa2`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:1efb2a16e6255fa81193190b623ba0668ffa777ab1de41ac5c5d2d2060a47784`  
		Last Modified: Wed, 11 Jun 2025 00:07:31 GMT  
		Size: 28.7 MB (28744185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26518c10b68afa1c48a5e26202210cb45a06dfba3cb8c769d5dc88bad8be12cc`  
		Last Modified: Wed, 11 Jun 2025 06:07:18 GMT  
		Size: 142.4 MB (142420687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd0d905c0d2f11c80403a48802babe29a681fad0f913033cb01d5dc2b92e986`  
		Last Modified: Sat, 14 Jun 2025 09:13:56 GMT  
		Size: 59.1 MB (59137438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814280aa650819dd963639e7929c5a2f3cafaa3d0eeab1ade8fd8aed6a0d76a2`  
		Last Modified: Fri, 13 Jun 2025 00:48:49 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4637a7b6888001b0a894e805be6dcef350cba6bd5455d5c4f3a9b236e14bfd37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5348956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0c2433a945d4875672894f69f404aded878b585028ad4448fc3b8ecc6c79531`

```dockerfile
```

-	Layers:
	-	`sha256:bf67d8f20bf6bb9980de952d5f80409a92ee060edfe73855c38954892b1cb735`  
		Last Modified: Wed, 11 Jun 2025 09:35:39 GMT  
		Size: 5.3 MB (5334529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a52fcd2b042ffff2394211b277a86831b0f1b963f6fa1dfc5543328d60f34e7`  
		Last Modified: Wed, 11 Jun 2025 09:35:40 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json
