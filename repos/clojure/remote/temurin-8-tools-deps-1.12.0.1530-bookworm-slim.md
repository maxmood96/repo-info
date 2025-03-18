## `clojure:temurin-8-tools-deps-1.12.0.1530-bookworm-slim`

```console
$ docker pull clojure@sha256:0a9c13126725d6b33db5907a827210767f26a6e026899a2b8a48103648d5c624
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.0.1530-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:21ceccfc1c9c8ecfadc6fa65b956f65baa1be1172430d2f756175e9904d7f1cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152455118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e20fff408a23a4726f2a75d4fe1c0725cb27949820c048a9e9606a9d342da796`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 08 Mar 2025 19:45:48 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6984ef393f85d40a757baa477f3538147b541f23ca5d9b60e750c44030260d96`  
		Last Modified: Mon, 17 Mar 2025 23:16:49 GMT  
		Size: 54.7 MB (54721226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89986b5d1e722bc5266cafd407207dacd5befa87441431b8fa3d72426d075746`  
		Last Modified: Mon, 17 Mar 2025 23:16:50 GMT  
		Size: 69.5 MB (69528381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ba6e3d1717b17b516548df61925bd38c5e4ecb9b18c3de9b0446a9ef9d11d6`  
		Last Modified: Mon, 17 Mar 2025 23:16:47 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1530-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:221e46694f592f3c105aeaceb4e06427aedd4f0838ab7549083256a6be45e172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5048498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e8c613941faec39416c3c8b88073855aeced001902bc3ae85686794bd2c81c2`

```dockerfile
```

-	Layers:
	-	`sha256:eb1793e97b491e5a05ee5c8b1423ca784f31b00d4d3e8383be2888e078323a17`  
		Last Modified: Mon, 17 Mar 2025 23:16:48 GMT  
		Size: 5.0 MB (5034207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2d4f78589eb3a3ad9072e5aee5cd20919a82fa93f87a49830d72351bb906f37`  
		Last Modified: Mon, 17 Mar 2025 23:16:47 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.0.1530-bookworm-slim` - linux; arm64 variant v8

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

### `clojure:temurin-8-tools-deps-1.12.0.1530-bookworm-slim` - unknown; unknown

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
