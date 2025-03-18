## `clojure:temurin-8-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:f71873343a36bcf3e30dda912e63e27ce0434b6e5191fda7850faecc706870c5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; amd64

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

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:146b10352e113708a126712421ddfec23956a79629610b439b938608e729e15c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151245077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5f9b20ede0bc9b8aa0dae59a252db0912b524120d425d13644a433d09774017`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 08 Mar 2025 19:45:48 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2428da9ac78ba6744298118e80258c610cbec1788af4ca9d2030790bb99e2bf6`  
		Last Modified: Tue, 18 Mar 2025 00:19:14 GMT  
		Size: 53.8 MB (53822778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5341f4c229ed19b47de7125a158f81cc8402adf15dda4a680cb6c98fe3ff9db`  
		Last Modified: Tue, 18 Mar 2025 00:20:07 GMT  
		Size: 69.4 MB (69377618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06067a9be6a756336d8c0f77fd18bb4ed0722e47c4fba98e8eb86ce86dae12ca`  
		Last Modified: Tue, 18 Mar 2025 00:20:04 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b67b7f2ae165e07bb7d8bdb1e3f78037f800a04ca17251b615568fe7b525dc89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5055075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecab39496655fcad8968e38a20e96388f450f4f85a064a78ef04e8cb503670cc`

```dockerfile
```

-	Layers:
	-	`sha256:066b22a3c846d8ab1c7b0a605afed6b21d3876ef8acc299b134b7b9a64d905c2`  
		Last Modified: Tue, 18 Mar 2025 00:20:04 GMT  
		Size: 5.0 MB (5040666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:436ea294462d99e97c3e0e7b4c8221c27ab5e93364e4570d42fe0ebcbfbfa643`  
		Last Modified: Tue, 18 Mar 2025 00:20:04 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json
