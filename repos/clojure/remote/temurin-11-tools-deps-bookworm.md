## `clojure:temurin-11-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:b5d7031488d920bf1a6ebf3ec65f909b8e620c9f8c392b05cf7d4a2ea6977724
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:de039c0dd3a4842d2f5e0499c7562c9cdb988efe5c348b888157cd55f37f3a07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275291495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b5a76764ff237b16a1f1ed5a6cf3c63214322675c8f55eb3642f70b07e31db3`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9948923c6c177074ecf786ce1c9254647c8324cb424026e2d81786ee2c74b88`  
		Last Modified: Tue, 02 Sep 2025 00:17:19 GMT  
		Size: 145.7 MB (145658229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e145ba066b0a17c09c903bab1bb4f97bbcbffd6d08fdcaf024a0645f3b15b9`  
		Last Modified: Tue, 02 Sep 2025 00:18:03 GMT  
		Size: 81.1 MB (81138108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b74d8b047bbf24377f67fc3e8756c88c1d698e78407ec97d016c54b00bc8f1`  
		Last Modified: Tue, 02 Sep 2025 00:17:53 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:cf80a3f635be9466b950df0af6176503ceb34a1e2d1699ebdaa5f8b2345fefad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7402690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:722309a3c6331a1a2beba37646425019be0a9b810abb5ac4b8fc03325971459f`

```dockerfile
```

-	Layers:
	-	`sha256:16a49543f1c3c0a08a6bd03ce4802091e16f01e3f4091bd2e00a8dd5be3d6426`  
		Last Modified: Tue, 02 Sep 2025 03:35:23 GMT  
		Size: 7.4 MB (7388438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe7f78517de6b21a1fbe595148a9d3c1286a72ac50e1dbdcad6faafbc9e5df43`  
		Last Modified: Tue, 02 Sep 2025 03:35:24 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d26a6dc09f3b9432de2f4f4394f03e85393c8e5bda686f4d146d57976dbf11dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.8 MB (271811665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa9a19550dff829efda1fb7637a1c9c5aa7acf6f4cb17a815c1eb20446452bca`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7429580bc4909dc2b92c132128f2fd1ff99a197ea01179830079a2a9cb43dc74`  
		Last Modified: Tue, 02 Sep 2025 07:44:57 GMT  
		Size: 142.5 MB (142459134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aae6ef8e899339fa99841053ef455b4cfa40f2ca180222a51769a932fa964fb`  
		Last Modified: Tue, 02 Sep 2025 07:52:17 GMT  
		Size: 81.0 MB (81009434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa44bb96acbe876918f576bcb504af7641154c740a65590344e78896e286b312`  
		Last Modified: Tue, 02 Sep 2025 07:52:02 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:bae32f6238c232b656864434751a69daf457f31a5e6c34325ecb57306c7cee11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7409189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b833a353967b51ca4c09b0fe9ca21670c150b7467299cba7543230272dd0297d`

```dockerfile
```

-	Layers:
	-	`sha256:88765cba52e818136d531a318ff59036e8115414d2f43ea659fa481b172fcdc7`  
		Last Modified: Tue, 02 Sep 2025 09:35:22 GMT  
		Size: 7.4 MB (7394819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fe5382f3dbc5f99dfc8e25ff5ae43bccd736b8685f4d8a09e1b64a8d2b3b637`  
		Last Modified: Tue, 02 Sep 2025 09:35:23 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:937df28df701506477c817b755730cddc48431966ca3c329329fc3231435dae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272164334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:423c08c01da4ec3e205b9de9e93b870f64c256313f24074d98209ce92253cbd7`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:33bc01697f2fcceb00fe53fe1bf433b48dc127c82c1555f61eeddeda9d72ff40`  
		Last Modified: Tue, 12 Aug 2025 23:05:53 GMT  
		Size: 52.3 MB (52338077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14db4d6f7ef9094c5e71617a54cb12d0ac6f4763bb9d1c751909909533970b82`  
		Last Modified: Tue, 02 Sep 2025 08:10:17 GMT  
		Size: 132.9 MB (132853137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:465a1ba89664eab548d0a56aa8624b0d96651ac323559f3202ac0af0bf488639`  
		Last Modified: Tue, 02 Sep 2025 08:21:12 GMT  
		Size: 87.0 MB (86972473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8387d4a34ce8471442ced5ac7026a6ce67d2f0077531b58420dc97100a69edf8`  
		Last Modified: Tue, 02 Sep 2025 08:21:03 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f50681ba73ec16414897657a818befe755f9b2f60a4af1d5fdd54e95501abdf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7407327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffdf66525a3f6da6efc17309d4da1626071e0a33d4e843ecfc3ae5f840333656`

```dockerfile
```

-	Layers:
	-	`sha256:8922ec87eedbfb57cd8534a10fce6c0c3839f01a7b219e34f57d37f32652a924`  
		Last Modified: Tue, 02 Sep 2025 09:35:29 GMT  
		Size: 7.4 MB (7393027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cebabebee846cdb36f9af0174ea2104c6f1b6d80abcaa7c7469acb4abea36b51`  
		Last Modified: Tue, 02 Sep 2025 09:35:30 GMT  
		Size: 14.3 KB (14300 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:0d46837cd8cd60a4f06e73d3e04bab50d5ede0ed6b013fcfa91cd2415c760499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.7 MB (252726543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4eba8ca3b984597caf5efec1bff46fd4103ebf140a5e1188a5ed4764fda06d3`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:635b31fd21bf059b6af0abf57b343066d0218ebb3e0b679927cc1752427a72da`  
		Last Modified: Tue, 12 Aug 2025 20:53:37 GMT  
		Size: 47.1 MB (47149866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d47acbec51e8b49420ca54277b6b3c563cc58e460f494d612b9455da60c70c3`  
		Last Modified: Tue, 02 Sep 2025 01:44:23 GMT  
		Size: 125.6 MB (125622202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0591d9f09d1ef5cf907a1e9c396641d9771e33cc9b052362fd70bb45b8e4a80e`  
		Last Modified: Tue, 02 Sep 2025 01:51:03 GMT  
		Size: 80.0 MB (79953828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f538cdf57e5fb30be540352c6902e5711da3a248ef7ab548eb64cc352521f0d`  
		Last Modified: Tue, 02 Sep 2025 01:50:46 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:18a9306121f4b42e818ae6f9fde8921dcf19ac3780e5da34f76c283cecae3982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7394013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aee7a942e7d56c8c72aa3054ccdd4f34ceab367ffc8e7f85994bb839f8f23cf`

```dockerfile
```

-	Layers:
	-	`sha256:8259d20479a544d30be70276b8be0d199f6b7b526f0c81cdb029cca2cc04dcc7`  
		Last Modified: Tue, 02 Sep 2025 03:35:42 GMT  
		Size: 7.4 MB (7379761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6836bc2c33385de653f5fb6b186e7034a312c88d06450700e61d04234e39cf16`  
		Last Modified: Tue, 02 Sep 2025 03:35:43 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json
