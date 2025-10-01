## `clojure:temurin-8-bullseye-slim`

```console
$ docker pull clojure@sha256:8eff3d6f93221ff0b1cdbc4ce72c5394b17bfc9dbf36452ade9f1f20d32e7bf9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:9949556cfa352b24819ef0f881d140f84c4d5d3608ce7b48cb70f8103ff90cf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144140883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f3f1113e21b5a90d0966375de28b48c0a4e26c4bb98af737003bc45928a0d9`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1759104000'
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
	-	`sha256:4eb1dd59a73886acc6a3cc9d4c8f8e66d1fd6ba6d6195b05ce21c22b0658aab8`  
		Last Modified: Mon, 29 Sep 2025 23:35:18 GMT  
		Size: 30.3 MB (30258363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24347d351394e95e8b219e55b3dbd91095c1a828ec89652c3f5c1a5cdf6334c2`  
		Last Modified: Tue, 30 Sep 2025 00:51:48 GMT  
		Size: 54.7 MB (54731286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383f68646dbea4e5b45ff2c1ccd00d29e9fc5a127cfea67f1661060c903d9f72`  
		Last Modified: Tue, 30 Sep 2025 00:51:37 GMT  
		Size: 59.2 MB (59150591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0341b47a7f00bb721f95bf81ffb14ba4e71e54c7b25a44b0c1bec592a8b7c42e`  
		Last Modified: Tue, 30 Sep 2025 00:51:33 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:41e1d931863ab37bb265eda6478d540ec7b17f060a702a1741421547b4f7ecbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5443968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9e45e1817099d021e091a3fb9e15640e8474aae22f7755d08589fc36e628efc`

```dockerfile
```

-	Layers:
	-	`sha256:db1586fd0b8c8950d5d15e45582e981323c721d73d01834d30556264fdb52900`  
		Last Modified: Tue, 30 Sep 2025 00:51:08 GMT  
		Size: 5.4 MB (5429677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:760a46405fd164a2aaee44f5427dca4026422c6846e5e4b531f2a26dc6c63667`  
		Last Modified: Tue, 30 Sep 2025 00:51:08 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye-slim` - linux; arm64 variant v8

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

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

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
