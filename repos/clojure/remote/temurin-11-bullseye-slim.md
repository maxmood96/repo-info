## `clojure:temurin-11-bullseye-slim`

```console
$ docker pull clojure@sha256:83782d9358c632dd4b4e83ba7d75a60a9f320e4faaabe7f223d170fb928be32a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b31b1c4a9ddb0fe2564b0b018dadad41de90e2f0512af0e6dee23b1b7e6fdba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.3 MB (235257349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bdf88daa41e2ace1d6edab2ed872fb750df849a92cf5f5752e85c028338e13a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:02:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:02:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:02:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:02:53 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:02:53 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:03:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:03:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:03:06 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:60fb1d5aba60afdf7cbf00cf9bd0c125e0c9c2ef7f454a7a88b456dd51794fab`  
		Last Modified: Tue, 07 Apr 2026 00:11:21 GMT  
		Size: 30.3 MB (30258019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6cddbd6d75ee219005cd958811fbae0fbee07d9e8c95b70331a2d6d8d0c85ed`  
		Last Modified: Wed, 15 Apr 2026 22:03:28 GMT  
		Size: 145.8 MB (145806808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee90380fd03619f88887d53d319661aee78a0a90268421faa0705cbf65e134a`  
		Last Modified: Wed, 15 Apr 2026 22:03:26 GMT  
		Size: 59.2 MB (59191876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbe85eb5ae2ac858fff0f7d510827c1b968370012b7ecc4c28d768a4cfaa48d`  
		Last Modified: Wed, 15 Apr 2026 22:03:23 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f26b9bf671c0ad2141a8f9bce40c56b3a6c8d4799e76774ad2c3d56328b81504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5354461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92fa7839a2f12d6d6cbac5c77905b660bab4cdfe535580c35f879ad1d3e3e91c`

```dockerfile
```

-	Layers:
	-	`sha256:ef3c36c7aa8a84f18d90e5c57248ffe5c4471c32c381870001002001dc641abb`  
		Last Modified: Wed, 15 Apr 2026 22:03:24 GMT  
		Size: 5.3 MB (5340194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:957d67333e6664c54e9259d47abb97293ac0f8aa857c174e8db932f22a44fba5`  
		Last Modified: Wed, 15 Apr 2026 22:03:23 GMT  
		Size: 14.3 KB (14267 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:74fa2dde40a20a721f82b6a7642d3eeb80f564cb0b3af8ef0cfa07f4f43c7a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230575021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c59eb7c9288a7f901a1c60d9afd24b2e8bb6f30b557e34a84578172ed9154b3a`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:20:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:20:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:20:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:20:53 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:20:53 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:21:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:21:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:21:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ab304f220d8a8ccbd47569f385750aa3f87cafd221f915b82f8e566f1abe130b`  
		Last Modified: Wed, 22 Apr 2026 00:16:28 GMT  
		Size: 28.7 MB (28742512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26600aee22ead7827362fa31dfb6cfdc0a04d61583156e0182e6fde7635faceb`  
		Last Modified: Wed, 22 Apr 2026 02:21:29 GMT  
		Size: 142.5 MB (142500863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64e69e6509cf681989e9a843e1544ece5d465c6a7c65d3607ec011298c61cc7`  
		Last Modified: Wed, 22 Apr 2026 02:21:27 GMT  
		Size: 59.3 MB (59331002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7583b334aee3958b87fe8e99c289af2034200e561db81b88f0320c93ecb41af9`  
		Last Modified: Wed, 22 Apr 2026 02:21:25 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1274fd693a8aa2b585f8dbc63c741a2dd3dc14097f5bf8e76eb044da17034563
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5360928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aa0b2e6c8c41850196140fa392dddc8fe250a12c3f2f751cf8462daf84543b1`

```dockerfile
```

-	Layers:
	-	`sha256:badd8a9cb8f9d72ef853f3e5bd5749e8c035e79e8033dd27e4b6b750268f16c2`  
		Last Modified: Wed, 22 Apr 2026 02:21:25 GMT  
		Size: 5.3 MB (5346544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ad7cf56ff790e147a67d88a3ee5427656e12086bab0c395aaf1300cfe483211`  
		Last Modified: Wed, 22 Apr 2026 02:21:24 GMT  
		Size: 14.4 KB (14384 bytes)  
		MIME: application/vnd.in-toto+json
