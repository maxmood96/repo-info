## `clojure:temurin-23-bullseye-slim`

```console
$ docker pull clojure@sha256:280fe6cc9865aa48303a38c5b051570606195c682e974cd00916d481906620f2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5d9d2417f7e59be9cd02d7413189baa3d917934afa97c8d66dbb16c640b662e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.4 MB (254359424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e555b2cc9eb06ecf6e42411f1c69f71ed16aaca76df42cac854c007ef6e346e8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 19 Feb 2025 14:51:07 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c4ff3df84a0c586964c1da8f9b9ef42e07e8fa95825627b7d9b48b34ca9023a4`  
		Last Modified: Tue, 25 Feb 2025 01:29:38 GMT  
		Size: 30.3 MB (30253930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0209f077617b9bd0bd462327c9f994e3103cf0ecd47e835b26a40c13aff7167d`  
		Last Modified: Tue, 25 Feb 2025 02:35:52 GMT  
		Size: 165.3 MB (165316201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d067071394b33e854d63af2198a773f0d123b7f373be21487826db69f015eeb5`  
		Last Modified: Tue, 25 Feb 2025 02:35:51 GMT  
		Size: 58.8 MB (58788251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5444ae3c1a157bd5386cc8c958c165c25a1e9a9105ffec495fbf2ff17bb1375c`  
		Last Modified: Tue, 25 Feb 2025 02:35:50 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e16033dd6fd69c1a9b5b38d34e3f90948ec2bb34f9c7fc3de3d4aeb8dbb4333a`  
		Last Modified: Tue, 25 Feb 2025 02:35:50 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e61db80607ff308064c1020be4cdcd8bee2ce8bbb584942ccb889638b15b45d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5295d4b42a91b54aed7cbf0b836580c3ff99b95129f0a3f8d288258a7ac26520`

```dockerfile
```

-	Layers:
	-	`sha256:5ad772444d2a609fd355c8ba9177047de1800c51e3f9ce6664395dbcfb2a667d`  
		Last Modified: Tue, 25 Feb 2025 02:35:50 GMT  
		Size: 5.1 MB (5122072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b14ec91705066f81fc702c85305948a9724ff5c95d689c0a3cb91e2eb0ee6b72`  
		Last Modified: Tue, 25 Feb 2025 02:35:50 GMT  
		Size: 15.9 KB (15878 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ebd47cc17052cf078fcb8e8c6553f8a895ab1d5a9d7a8b5cae381c25a39c1714
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.0 MB (250998796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e3e529418c30fb9ae5606b4595494c643df6ec06687b60ed208519dee118870`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 19 Feb 2025 14:51:07 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c4c6d622e13259683de05019144b319d210aaf74faadf38f9ff2c9d56472ab51`  
		Last Modified: Tue, 25 Feb 2025 01:31:29 GMT  
		Size: 28.7 MB (28745987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:308f1b6351443eeb95b7663351c2cd91ab204f00518bea6af575eb787cf99623`  
		Last Modified: Tue, 25 Feb 2025 11:18:07 GMT  
		Size: 163.3 MB (163341440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8c8a92a310b1aa6a79b815ec526d234ea9fb453ea176f02aacaf12b78c0f2d`  
		Last Modified: Tue, 25 Feb 2025 11:21:03 GMT  
		Size: 58.9 MB (58910324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b26dae452022d03a1860d85dca50b479f5a6e22bfe5ee44ac86c28c2b203c3`  
		Last Modified: Tue, 25 Feb 2025 11:21:01 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9cf833d23d36c231c75513cf2a7da7c2ff78075290c5a6fc7d0c7b73ebdb2d`  
		Last Modified: Tue, 25 Feb 2025 11:21:01 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cd50079bd6ae31180ace998f13d4cbde7638d345669a19f7924f17f149efa1e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5143179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1db42e8f0bcadde878e7a59d84a0a33350d34ef644099d59c9976b771318085d`

```dockerfile
```

-	Layers:
	-	`sha256:e901fa57434878370f49fa3d9b93b93d436e7360af72f88fc3f9667a4890f13d`  
		Last Modified: Tue, 25 Feb 2025 11:21:01 GMT  
		Size: 5.1 MB (5127183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c36975375d364334d8d94d1f369f38d7976e4f00bf7b6a72ff2a86e6aa3440ad`  
		Last Modified: Tue, 25 Feb 2025 11:21:04 GMT  
		Size: 16.0 KB (15996 bytes)  
		MIME: application/vnd.in-toto+json
