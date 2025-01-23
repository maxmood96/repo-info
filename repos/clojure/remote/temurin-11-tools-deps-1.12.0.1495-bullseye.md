## `clojure:temurin-11-tools-deps-1.12.0.1495-bullseye`

```console
$ docker pull clojure@sha256:3ebdbae6d7aae4344b9fc6a136384d602b5b66cb8bf68c8c77314728bbd77e33
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.0.1495-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:1c55ff99f5245e8ec69de51b0773e4a5569ea61622676eeea684635b0a76eb89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.5 MB (268519773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fec52488109545dec1d4749dce2aec612f9afbed4219e19d5e5553ebe0496d82`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:de97e8062e06250e3c3cef0d40cfe62111bb4b74bcf6221e25a06452dacffcf6`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 53.7 MB (53739164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0246709c8f192e790538651c0d8790b5994317a9d4dac886ce655150b1bf6e2d`  
		Last Modified: Wed, 22 Jan 2025 19:42:18 GMT  
		Size: 145.6 MB (145601449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcfe4737349b804f9e1b039095b7501525ec05fcde2f406b7d2cb421ff891f61`  
		Last Modified: Wed, 22 Jan 2025 19:42:18 GMT  
		Size: 69.2 MB (69178515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5deeff609465a293a345ab6997bf647cc08e69d95ba75fc6331805c48265de63`  
		Last Modified: Wed, 22 Jan 2025 19:42:16 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1495-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:0cb3dc71d6ee0a76134469139eedaa36e3380a682d7b4549b65e443c55688e57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7238948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f3f66132fcc0b6274aa95847aaac78cd3dcfdc524333627f15fe5a148c2b26`

```dockerfile
```

-	Layers:
	-	`sha256:46e97e2e7467d526ed5ba73ffeee478a56c12c9cd7c847fb52aa58edcda9aead`  
		Last Modified: Wed, 22 Jan 2025 19:42:16 GMT  
		Size: 7.2 MB (7224696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a4a136ece464863ab0994594c6fd0ec1312fed3f6c2c108515b978fea9bf745`  
		Last Modified: Wed, 22 Jan 2025 19:42:16 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.0.1495-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cc652a0b941cec4f8bbf37ac82db5a3fb017ec8784e94245e4b74d65bc0c0935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.9 MB (263940189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d55e739b164a66cb1c4edc4c335bc172d61566d058e1321fd5544d3b9e4b8487`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1270858b2b9cb5d47abd119b946534b70ff7d09f29c425fc07b280e5c28971c6`  
		Last Modified: Tue, 14 Jan 2025 01:36:12 GMT  
		Size: 52.2 MB (52246060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e780c45b36bd873816073e4e93fe81cb349e604ae86992d9131497c0598ea2`  
		Last Modified: Tue, 14 Jan 2025 12:22:08 GMT  
		Size: 142.4 MB (142389012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f9cacd183bbc34e90d7097b8c512340445bdd25fd1b52deac89c1699631cad`  
		Last Modified: Tue, 14 Jan 2025 12:25:10 GMT  
		Size: 69.3 MB (69304473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ade6a8fa8c6013ebba84e690ed51255876197227b363d280da4921bac2ee3ed`  
		Last Modified: Tue, 14 Jan 2025 12:25:08 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1495-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:45f47b643fd591e9cb6d200e7ede24a3e40fcc9d92e3043856d2058646ec5a4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7244783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af8078d203cf2e7b5a738f74c3acd9d3c92b75dd8ee6d97aaf7ff980986a512c`

```dockerfile
```

-	Layers:
	-	`sha256:3c14551733057f7be424bd60d1576c5c326e919e5e5aa04020736eae4a50a444`  
		Last Modified: Tue, 14 Jan 2025 12:25:08 GMT  
		Size: 7.2 MB (7230413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7044074c38e0657f3bdff6c6b98796715308af6020dbb793741f798e747c442a`  
		Last Modified: Tue, 14 Jan 2025 12:25:08 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json
