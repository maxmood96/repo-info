## `clojure:temurin-8-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:e57c4d26ab93b01fca637ad1c0c0545e9130e75f6c997bd73fa6d308d17d3811
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:9eb3f38e4dec904853423a723664b36d105fe0450444e684177a232041f451da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144140031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a877fc7381227353687ee6730a9b99a86bf8e7cfb6fbdbc4872467ad7299bb7f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:456a3213e1b1f193dc759cd05f6f8422428b8c4bd45ef40fbf41ba43bdce8570`  
		Last Modified: Mon, 08 Sep 2025 21:12:48 GMT  
		Size: 30.3 MB (30256068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e464b5bf635bd21f2d80857baf56eb692da3002549d90cb215a3598bb1451b4`  
		Last Modified: Fri, 26 Sep 2025 17:52:33 GMT  
		Size: 54.7 MB (54731292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07ae00d4f30c6ba4ed94c016993f986eb74a6c403911874c4d243b0eb9a54c1`  
		Last Modified: Fri, 26 Sep 2025 17:52:41 GMT  
		Size: 59.2 MB (59152026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eece436d3041a04cd4d94146a2880f432fa2d894cd53c778f40351c25c053cc8`  
		Last Modified: Fri, 26 Sep 2025 17:52:23 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e052815260e404f430f5ede2fed65a3b8080f5e8fa812417db741fc12dc85d5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5443968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51c4339f31f1aff1a64d580ca2ce05bf59cc392eb554855f5c9aaed4b8791743`

```dockerfile
```

-	Layers:
	-	`sha256:cef43deb6e33921ff5a77714ea56fcb2ae198bcedb2cb906c09204adab9eba7c`  
		Last Modified: Fri, 26 Sep 2025 18:46:50 GMT  
		Size: 5.4 MB (5429677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a79f2195b720214800e7542a544b4e86742d0e09fed145b6642b018bd7ecf3b`  
		Last Modified: Fri, 26 Sep 2025 18:46:51 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:859ac8eb7b999fcf8e6c02b5efd0676a031c361e06523bccc453c5823cbfc540
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141872972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22b793bdaf3ffece325fd2fbb419702fba9c78db465ccc665dbcb527f2d71df3`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8568e9af3ab25a29d98aac9a07896467a19253e72e5be0cf09cd3982ac4444d0`  
		Last Modified: Mon, 08 Sep 2025 21:15:52 GMT  
		Size: 28.8 MB (28750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa8c40c3c258217567f29e854d1a0423de678f485bae06e32c332ae1df7840d`  
		Last Modified: Fri, 26 Sep 2025 17:53:46 GMT  
		Size: 53.8 MB (53835609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb7f639e3fd6473c5e69dc0837c3f1ff2b2f3fc6df8ca99fdfbbb4f64ee26ca`  
		Last Modified: Fri, 26 Sep 2025 17:53:47 GMT  
		Size: 59.3 MB (59286260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737eaab86886e188d61f459bfbd915e80e5a4a3cd1d6d0d4dbd6dd9e6cd301be`  
		Last Modified: Fri, 26 Sep 2025 17:53:40 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:abeee52f048bd5e64b28c07cff5e731e2b9544fd88fec0fa7fcd2ea65a59617d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5450515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2a879122099d0fda5b1176c7b9cb97de56bb9a76d0ccf36073d68ba7c4f0bd1`

```dockerfile
```

-	Layers:
	-	`sha256:3ee546d98c59c1c71c6e927ddb9992f1eeb7b1e697b8907d4b0d2e06d05cb6e9`  
		Last Modified: Fri, 26 Sep 2025 18:46:56 GMT  
		Size: 5.4 MB (5436107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b05daadcf3fc93a1e119ff4d5427e04d03fc32e5ed5dcfab4f8899627e54aa36`  
		Last Modified: Fri, 26 Sep 2025 18:46:57 GMT  
		Size: 14.4 KB (14408 bytes)  
		MIME: application/vnd.in-toto+json
