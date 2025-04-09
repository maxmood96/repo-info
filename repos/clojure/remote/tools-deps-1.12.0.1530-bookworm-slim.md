## `clojure:tools-deps-1.12.0.1530-bookworm-slim`

```console
$ docker pull clojure@sha256:2cc7ed73327c161d9ac1137f4e9ff24716bb8c3539c5c38830c75d3fd8d09c9e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-1.12.0.1530-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:dfacd769e2d515bfe2bb9d6c1f0d38a9073770a1d93e9022b5a7282af3d288f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.3 MB (255342627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dd0902382506570aed8212e0ee0754b19254b491685cc05b2fd61747db66015`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83b3694556202ee32f34d95f80c5a713c3b66c62f5b759aefddefa728204d92`  
		Last Modified: Wed, 09 Apr 2025 02:19:15 GMT  
		Size: 157.6 MB (157585841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc6a60e992ec505c82bfaeced0bb433dd20ec1d9e74c6383a4a8eea4f4caa161`  
		Last Modified: Wed, 09 Apr 2025 02:19:13 GMT  
		Size: 69.5 MB (69528484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5509f4b5d94324db1e5012859748426282d6bdbf3de01da83f734cc6aa92a15`  
		Last Modified: Wed, 09 Apr 2025 02:19:12 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5944ef9ede3ed86c32eb9b0023e7023acb6fc65f0c7cd3020168e0bce051552`  
		Last Modified: Wed, 09 Apr 2025 02:19:12 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1530-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:46707b683e98314fb878faee2d347e04f28cd51ae4b631574ca329de949d9e7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4934338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48880e45913e507dee02f538efbec5519dfaba3e974950643fe04d33bad8718a`

```dockerfile
```

-	Layers:
	-	`sha256:1a45735654f0c4fdafcbc53545585095a8a04b6b7f7ae9420a5b9b6f7a55977a`  
		Last Modified: Wed, 09 Apr 2025 02:19:12 GMT  
		Size: 4.9 MB (4917763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:060b8c2e4c7e520f0e948898540f583aa814b887bbeccde53a262e8047fe297f`  
		Last Modified: Wed, 09 Apr 2025 02:19:12 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.0.1530-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3e517b254afd8d3e5a3277897ea26a7c28fa3f8702d3c0e0d5a915b137c820a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.3 MB (253304857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfab67c2dff2b2fd3bb828076ef2161328e0eb2ce612f8fc7f6314e45880962e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3c058cd77d4a51f60ae9af79bb6ac59c8b48416474e3472848d56b12a8d512`  
		Last Modified: Tue, 08 Apr 2025 11:32:21 GMT  
		Size: 155.9 MB (155859256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8291a243525f0ae7f354ce5b905aae4fd4a830fd7413ea9ff49d84f8479f6995`  
		Last Modified: Tue, 08 Apr 2025 11:34:56 GMT  
		Size: 69.4 MB (69378238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b358ee862644876ec4285f629d72d1753bebcb2a075b6b070d16dcfaafe4dc6c`  
		Last Modified: Tue, 08 Apr 2025 11:34:53 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad25fd746b4fd0dadce58643b1ebfe6430e22d184737a84fe93319b388c7e19`  
		Last Modified: Tue, 08 Apr 2025 11:34:53 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1530-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:69dbc98f0c05cc934c9fccff3eb855b474a9f7be65092ec4dfdc707440c5fb84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4940265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da7cf3aa0a6605ce48bed267ef46d003be991025c00df00eec057196749fa487`

```dockerfile
```

-	Layers:
	-	`sha256:6cfb2fe1a75695e351e1a98e5ab74c663acd7e20cd3f5863b07a1d80db8c68c8`  
		Last Modified: Tue, 08 Apr 2025 11:34:54 GMT  
		Size: 4.9 MB (4923548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2fa69cf9dd17f0bc4cb347c8c4a6eb84ebcca6cb5ea9e0d0d9196c8708cffcc`  
		Last Modified: Tue, 08 Apr 2025 11:34:53 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json
