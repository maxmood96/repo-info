## `clojure:temurin-25-trixie-slim`

```console
$ docker pull clojure@sha256:3d3f18d5dc95f7578ce1fe039d4f7baa8e5b9cc3e851cd46c088ee9b95411860
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-25-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:288b46d0d66793fa229c867a7031c1db17e9793fdff7f8a15e56e00c8f22a0f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193815687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b10014a2e021c749ffbbfe74f16797d5d526aa5543893ed3b765b274a2fc06`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Thu, 11 Dec 2025 22:40:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:40:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:40:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:40:47 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:40:47 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:41:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:41:03 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:41:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:41:03 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:41:03 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:decb9f3c4199e8c762e83c5a54169c237a83cd0f316f9f599ba3e8664f18177f`  
		Last Modified: Thu, 11 Dec 2025 22:41:39 GMT  
		Size: 92.0 MB (92045295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52683997dd4cf878992397d4c9463b979c1167a043ecfce595f3c26fc542e348`  
		Last Modified: Thu, 11 Dec 2025 22:41:34 GMT  
		Size: 72.0 MB (71992855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7251699b64d6093f79e84ad8438ca7c6088dd23b3bce626c2ca40ed5eb8f6db7`  
		Last Modified: Thu, 11 Dec 2025 22:41:29 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e65c43766be6bf9cb23d00914dd1354483515b1287cca6e60caa668baf1ac9`  
		Last Modified: Thu, 11 Dec 2025 22:41:29 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1c329b9d7f858e8ebd234921e1b256f235093e9eaff58f170718cc60e9c60616
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5224042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fcb21bb71b9ced6be18c1f4f771852eaeae58f63dd38ef1bf64fb63448c968f`

```dockerfile
```

-	Layers:
	-	`sha256:b8fb40a775a92cbca7ac847e4535278e307390dfbd340505ef1b31949c4c1bf0`  
		Last Modified: Fri, 12 Dec 2025 01:45:36 GMT  
		Size: 5.2 MB (5207549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:728ce063bfb4b52453b9dc4fd4d69bfddcfbee77d16e3080a6724e558dc0336a`  
		Last Modified: Fri, 12 Dec 2025 01:45:37 GMT  
		Size: 16.5 KB (16493 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6d90730d50feceb1e5aaba423d79465f53f4fc8e8ba098361c1b84ca750e490e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 MB (192998720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29659bbfc42d2d7d2354fffffd7b367b44ed5535f89565b46a004c06fe3d62dc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Thu, 11 Dec 2025 22:40:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:40:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:40:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:40:58 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:40:58 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:41:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:41:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:41:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:41:17 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:41:17 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d869e92beb17b5cc5e3a81f75741c5d86b1ce3d3883c8caec60656a1e80f21`  
		Last Modified: Thu, 11 Dec 2025 22:41:54 GMT  
		Size: 91.1 MB (91052481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc4e99ae85c30280b74b179cd2e4be330c55086b29529ff1b2ae8bd8a9de740`  
		Last Modified: Thu, 11 Dec 2025 22:41:51 GMT  
		Size: 71.8 MB (71806569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb7f579f9903be87f5ae7bc1c5f72888a1bb056ac592e74621981ddcb3fc01b`  
		Last Modified: Thu, 11 Dec 2025 22:41:44 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043f1f33fcc29f1aa5a90ea5c8fbbee9dfdcb566eec6d40633a0d1506b6aeaf2`  
		Last Modified: Thu, 11 Dec 2025 22:41:44 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:25b1037b868ef7a9b44f7c4d054026768ec8796befea6b2fd73d8f7db17a832d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bfddf98d15b60ebaba9f95fe465ab7317c6e01b56152f8143a0757b373dcc91`

```dockerfile
```

-	Layers:
	-	`sha256:aba2c483b3a5c49e854ffd2be1170f83b5d15ac656a538e7c5d18a557fdfb454`  
		Last Modified: Fri, 12 Dec 2025 01:45:42 GMT  
		Size: 5.2 MB (5213339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28581eea07fdf38c524784f49f238f03fdd28259f6200db1ed768b509dca6f24`  
		Last Modified: Fri, 12 Dec 2025 01:45:43 GMT  
		Size: 16.6 KB (16635 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:8404514db412848148a7ba6ff2843ef094b4b292a30f6d4c1a297cf72e91d17e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.6 MB (202595845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca64d0e1ba70e6efdfaeb51efab95498ef481cebebdc5f23432ab8a18a595f54`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 03:55:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 03:55:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 03:55:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 03:55:25 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 09 Dec 2025 03:55:26 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 23:08:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 23:08:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 23:08:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 23:08:42 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 23:08:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e90333d0ab795a7ae2c0a51c53552c38eb8f814a4df79b46ded26ce84b6fab`  
		Last Modified: Tue, 09 Dec 2025 03:57:08 GMT  
		Size: 91.6 MB (91610796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:962464b0042161866f876d09cd1bf7b4d14ff97da4702d53fce3eb520707808e`  
		Last Modified: Thu, 11 Dec 2025 23:09:33 GMT  
		Size: 77.4 MB (77387116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e221b65d9ee8c69e66ed0c75bd970c99d356a4337878c7fcc787e748a01f6bbd`  
		Last Modified: Thu, 11 Dec 2025 23:09:26 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55174c52f0e33924e323c7611c75fdd631ef39c551f73785929fc69a2ce0c0d9`  
		Last Modified: Thu, 11 Dec 2025 23:09:26 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:06a1c9e259cdfe775e78b11e4c78b8410495a3ac5dbdfd63e3a88f81f86d7223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75cda811628c9fe2af6a1898cb161a9d8d648601610be8933ffd2ffe46c20508`

```dockerfile
```

-	Layers:
	-	`sha256:26e8ae34516f43188bb115570c6e07dcbf887346fac331bb1537e70cb3daeec5`  
		Last Modified: Fri, 12 Dec 2025 01:45:49 GMT  
		Size: 5.2 MB (5213230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c82ee5f6924693f4699adc5b5c36e5e6d2ef573dc74f52c9c7bf0ca17ef25c06`  
		Last Modified: Fri, 12 Dec 2025 01:45:50 GMT  
		Size: 16.6 KB (16553 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:4fca91f25949bbc97ae1bf8b3271c467b0696eeaf7cbb0e76f6d2cb84c187995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.9 MB (189907703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e973002afe9d56d7dd58e9d4dfb807f0abc998450a9430682a0eea0879debb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Thu, 20 Nov 2025 18:54:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 20 Nov 2025 18:54:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 20 Nov 2025 18:54:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 20 Nov 2025 18:54:05 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Thu, 20 Nov 2025 18:54:05 GMT
WORKDIR /tmp
# Thu, 20 Nov 2025 19:09:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 20 Nov 2025 19:09:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 20 Nov 2025 19:09:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 20 Nov 2025 19:09:49 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 20 Nov 2025 19:09:49 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e6d736f22fbd16f11de06f0cbb3ad19602da41d0ae18c2694b069ccfe7a409`  
		Last Modified: Thu, 20 Nov 2025 18:59:39 GMT  
		Size: 90.8 MB (90752878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c984831c7d0bb12b1a247ff56d2fd1a036e695717a635da3b6407225e1a2324`  
		Last Modified: Thu, 20 Nov 2025 19:13:40 GMT  
		Size: 70.9 MB (70880654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a968300f69805e85f31f6fd5b900d7c43dd72cf1b4d6138e897d7194b54c656`  
		Last Modified: Thu, 20 Nov 2025 19:13:30 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3dba38d726ae41f643a2801ae343077014ac3d89bbb1baf493886c26741de22`  
		Last Modified: Thu, 20 Nov 2025 19:13:30 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1d80d022b1bf8ce12df89ef99ffd0c1ce41419080a20d3f81abd96323816bfaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5213572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6b705302729a3ad056fbdef51b12d4b9f82a3a31ca6e5148076197788340449`

```dockerfile
```

-	Layers:
	-	`sha256:1d8d7fb5d1c5364ebb424b5dc3ec01f49701fc3f4e9056cd4243202d33b17424`  
		Last Modified: Thu, 20 Nov 2025 19:38:25 GMT  
		Size: 5.2 MB (5197022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:393b39d896d3afc39da6b1b79c0abef3aff51ceb128a4fd2d58e23e7d37833e1`  
		Last Modified: Thu, 20 Nov 2025 19:38:31 GMT  
		Size: 16.6 KB (16550 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:9ff0246b052929b90f6557078c3696e01466f7291e55a19b3481155992a7ec19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.0 MB (190999917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1872bd44cb2a951a642b7055e70fce5911acf1b9ca0888a49aa48be8787d7866`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 01:33:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 01:33:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 01:33:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 01:33:39 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 09 Dec 2025 01:33:39 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:37:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:37:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:37:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:37:42 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:37:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:deacec5e6af82b258c59e95e3e86abeef36fad06b1d9ff2de33e88544ffb79ff`  
		Last Modified: Mon, 08 Dec 2025 22:20:52 GMT  
		Size: 29.8 MB (29834400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b901607e1053160f0c4a5999035c86877af07f0a5ab635c3250bef9051f1d4`  
		Last Modified: Tue, 09 Dec 2025 01:34:38 GMT  
		Size: 88.2 MB (88210741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6f832d3fabf90bf71b24a16d2383da36cc57d808c533fc8b68eebd99ffc9d48`  
		Last Modified: Thu, 11 Dec 2025 22:38:16 GMT  
		Size: 73.0 MB (72953739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f7c05ca7f55ddeeca6efe5c608c75ca07be1134a05fa1e16b3978dc78448f3f`  
		Last Modified: Thu, 11 Dec 2025 22:38:10 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b705231fc56f826b0ebd31eb2c58301012edb211ff98bcefb3105dc2e49881`  
		Last Modified: Thu, 11 Dec 2025 22:38:10 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:844851f75bfdf92d91bce39b1a02452f99db1221234d0b0807f09b6a59d193d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5222514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39990c668173f830144a15cd9332fcb9a16293ce6905f314bbb682aafe3e32bb`

```dockerfile
```

-	Layers:
	-	`sha256:779a18348274b82303db2f3cfd934af96cf30632615c097c6840a8ff70626ca5`  
		Last Modified: Fri, 12 Dec 2025 01:45:55 GMT  
		Size: 5.2 MB (5206021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5b333786d283a49ff605f17ec955c0f830be8f9547259151973e16287265802`  
		Last Modified: Fri, 12 Dec 2025 01:45:56 GMT  
		Size: 16.5 KB (16493 bytes)  
		MIME: application/vnd.in-toto+json
