## `clojure:temurin-8-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:492fd72c99d5e8fafbf9ebf74295cf2ff5f65489bcd79ba21bb29620918314e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:dc21e1d36407c0bda0682f7b1918e29b9f74f5deac95bce5b53d36a439dd4aaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152468624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e56ce6f3bd8dde1f9fcf21cfd64613ec863048328fca7b4584497d1c2ab0198`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4aea381b6a80b00dae24146fb22f4d1e97a2ab19b7d7c2dabf9f95b3bc9e9e0`  
		Last Modified: Mon, 10 Mar 2025 17:39:47 GMT  
		Size: 54.7 MB (54721251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b5c437b7dc6ef22b07a54a015899c69e631a88973efec3a1cb47f3447fb308`  
		Last Modified: Mon, 10 Mar 2025 17:39:48 GMT  
		Size: 69.5 MB (69527424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65813e4001d474eca8e5ff12bd3ff9af0bd4a20d470daeb926f935d5a8b0d6e2`  
		Last Modified: Mon, 10 Mar 2025 17:39:46 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c8d307032100bf8f82801688281a516138909a67d24585537a8e6009c5fc4786
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5048486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15192de70cca250f3718eee12648580c25261a5b5da70aabcb391cce17fd46b5`

```dockerfile
```

-	Layers:
	-	`sha256:08ea2a7e6959920f0127d23acdde549c578307cc250bba3cc6e756a20977ae96`  
		Last Modified: Mon, 10 Mar 2025 17:39:46 GMT  
		Size: 5.0 MB (5034195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a3174537a0546ea813a28d3f1c70b0e10ed693fae986c46b50906b79ac8ed8d`  
		Last Modified: Mon, 10 Mar 2025 17:39:46 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3962cf203152ee05ce8a9393e96b994ff63afc4a65c87ed4b676701dcf0f41f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151250771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c59032885770b2d18a1c75c223fe10ec58e15e3236435792607e6b07b3a4f46a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff1299c0642985e2f942c61ce1745215a1f5b539a172f9619c706ea4a1c0f1b`  
		Last Modified: Mon, 10 Mar 2025 17:42:42 GMT  
		Size: 53.8 MB (53822752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d050ff19b575ed0ed36a31979db33e8cd5f5a94b7eda3cc986b4958a8c6bcde9`  
		Last Modified: Mon, 10 Mar 2025 17:42:43 GMT  
		Size: 69.4 MB (69378947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716fcf50f377e1f00de3373067330db8d84bfa51545f7f84e5cf56a83df1dda3`  
		Last Modified: Mon, 10 Mar 2025 17:42:41 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ac3d34e25fcb6dba32a3df99927a2bc939249fd6261c95f4241f9cb7d5c16a17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5055063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bc045e347008b5ceda16cd0845ea7fdaea81bfab52d04c7d9d6b4e569fed1c0`

```dockerfile
```

-	Layers:
	-	`sha256:9dd97905ce22a8353bd46acfb73c754fd0069b5caf4b4afcb88e34f045d68d1d`  
		Last Modified: Mon, 10 Mar 2025 17:42:41 GMT  
		Size: 5.0 MB (5040654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:987fa489382a8b83924ef9de962b08f5952c4a85c308484f2fa6da1f9c2dac78`  
		Last Modified: Mon, 10 Mar 2025 17:42:41 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json
