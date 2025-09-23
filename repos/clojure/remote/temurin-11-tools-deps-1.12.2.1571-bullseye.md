## `clojure:temurin-11-tools-deps-1.12.2.1571-bullseye`

```console
$ docker pull clojure@sha256:2d78bc47c620325f9ba61db2c33339f4363b4f1b0db8c5a49baa10e9caefc6c7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.2.1571-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:1b4d7ffa9d461603d54cdcaa82cfb8008ef32314e4cf2efaa0184c9567c023bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268974516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fed4204c95626c46de2040370b421650f61180b35a66d059f3bc6825de1d77b2`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:035115815e46101f9c9956e02e706f2f3ec8748e2b415f0d232b51eb76a6a779`  
		Last Modified: Mon, 08 Sep 2025 21:12:56 GMT  
		Size: 53.8 MB (53755396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49c53625567c5726fa7dda71704c3d667437612f033777f2455210a28ab74284`  
		Last Modified: Tue, 23 Sep 2025 01:40:49 GMT  
		Size: 145.7 MB (145658218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad794bb6490e398918b4f603a5d5ee086c89af07e91e2eb3bcf24604a98663a7`  
		Last Modified: Mon, 22 Sep 2025 23:45:02 GMT  
		Size: 69.6 MB (69560257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca2b0ed8b7145387de62835cb1223aa55737b0dea997bcad74bd6a3a7d564e7`  
		Last Modified: Mon, 22 Sep 2025 23:44:56 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.2.1571-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:30a87f4bef1d301ab42e2e83572e9c0e20494ac199ecdd37333b88affefab097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7430060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14f67c79b3960d02905c221748fc6e9fccd6aa6052391b65868d5f1124c67204`

```dockerfile
```

-	Layers:
	-	`sha256:90da66d8b6d3e4196a30e0e096d6c81758b89a67d8c0f85166f0a7c91ddd8948`  
		Last Modified: Tue, 23 Sep 2025 00:35:19 GMT  
		Size: 7.4 MB (7415808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d73a2dfccacf2d7dfd50ac8024439a059c5ac1728f219c41e73cc223a835070`  
		Last Modified: Tue, 23 Sep 2025 00:35:21 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.2.1571-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a0df6591528440f19d1b8ef65544b39fb612240577c3ac5f8c84c64b9dadfe90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.4 MB (264395608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:319b5ac47d069205a1ce05380cd1d691f10518d5549a12280bf5d4b572c5119b`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7df02cb4a974a4e8a9eb65ffcff7274f9dca341d29aaa763294c42e49805ca19`  
		Last Modified: Mon, 08 Sep 2025 21:15:41 GMT  
		Size: 52.2 MB (52248370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b1b1ae2f19e71fb2ff0de09e977a6f869441d775c8e4727e7f5789b071348f`  
		Last Modified: Mon, 22 Sep 2025 22:17:15 GMT  
		Size: 142.5 MB (142458749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50bad8849e24803ff411b6313e9ef697ad0ab8b1ee2c7764c13cc17deef14436`  
		Last Modified: Mon, 22 Sep 2025 22:17:14 GMT  
		Size: 69.7 MB (69687841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b28ec5ea555cc2c10bfd86fd9abf14c8cc538537dace7304d4db109b87b21a7`  
		Last Modified: Tue, 23 Sep 2025 01:07:19 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.2.1571-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:2ef1fc43dface287bf4584ad8f09d7bc754c079ff99ce31c79c45a5fb02b02ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7435895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcc63330e2bf52e38146b7f89f892fd78ca1b2a0cbd939e1b2133abc8e0c01e3`

```dockerfile
```

-	Layers:
	-	`sha256:26bff001029acb92fcd5a1a9632d33251c7978b04533e93261a4c4787fb9dab2`  
		Last Modified: Tue, 23 Sep 2025 00:35:27 GMT  
		Size: 7.4 MB (7421525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa2503d8d77e273d836fc01fc87d148a64770f2c3111418dc7b5452fdc9f10cf`  
		Last Modified: Tue, 23 Sep 2025 00:35:28 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json
