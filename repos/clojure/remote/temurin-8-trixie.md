## `clojure:temurin-8-trixie`

```console
$ docker pull clojure@sha256:b98968b7b880e3b3ac648e9abdc7af4a5a4a34215fcb87cbf0d4641cb9ba8084
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:2aeffea286f968b28b3a228b057718f192f42925743fe931369f86ffb74889a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.6 MB (189559068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb8465cffd0ca288fe8fca94f889cbc8b50e47a3e9419890848bd45ae0ef864`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
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
	-	`sha256:cae3b572364a7d48f8485d67baee38e4e44e299b8c8c4d020ff7fb5fdd97f88c`  
		Last Modified: Mon, 29 Sep 2025 23:35:29 GMT  
		Size: 49.3 MB (49284626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520a7728e088e0c88e7a4ea5d2535dda35faaa30206bb1ad08412141d005f253`  
		Last Modified: Tue, 30 Sep 2025 00:51:19 GMT  
		Size: 54.7 MB (54731283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d44c7f84316a60429ddf4081089a76a9be4d86e4aa02b5ca0ec755a3cb9225`  
		Last Modified: Tue, 30 Sep 2025 00:51:19 GMT  
		Size: 85.5 MB (85542515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d34c3c081a0f2a20ae1303aecf07b2f1b18803436dfd3d4b55042913f539d9f`  
		Last Modified: Tue, 30 Sep 2025 01:34:31 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c9a553992a88e7ba03792b77f0fdec5a7200857faf7c220d890ca44b95cce5c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7602668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07dcf70b3b08a3f5606d33bb8b409fa3f0ae717c2df569bbdf2c51f143d40a3`

```dockerfile
```

-	Layers:
	-	`sha256:00c0bd0dfe42e29c91e42c3defee793834babd0e0ab77ef2c578d075b873be7c`  
		Last Modified: Wed, 01 Oct 2025 15:44:53 GMT  
		Size: 7.6 MB (7588455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b04704927f8364a46492524bff28ddabf11f6129cd0f7c5e095371b2ffdbbb91`  
		Last Modified: Wed, 01 Oct 2025 15:44:55 GMT  
		Size: 14.2 KB (14213 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cddb269a80525b12a97a140a5a65a9d0668fea1116590cef13c6958b11bd4088
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.8 MB (188843454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a7669860162547c0acf0a01f30bad51484c908de3b569f5006c009d62873f25`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
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
	-	`sha256:37b49b813d9cadbc816aea22a15ef76898c66b4db015fea88b8f15bf213d5004`  
		Last Modified: Mon, 08 Sep 2025 21:13:28 GMT  
		Size: 49.6 MB (49643746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab8ae5703d0f794e6ee6047842a513c27486bc496feb3f085fd20606c0f2bb2`  
		Last Modified: Fri, 26 Sep 2025 20:03:54 GMT  
		Size: 53.8 MB (53835608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f1e48019453a195c6d08cd8a20f67914a5c704715e79be3d9a4463a648569c`  
		Last Modified: Fri, 26 Sep 2025 17:54:09 GMT  
		Size: 85.4 MB (85363453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad0c6f506fdf00aa9daf70666870ea5ba1d05eb1cee522a235a7c0970f88a78f`  
		Last Modified: Fri, 26 Sep 2025 17:53:59 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:5a1a4a5f21c2dead86db4ed661ba20b222562415d27893c1a409d5d180769163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7610513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d18407c36538e366f8de12917a574a6c35503c2af9f0737e8fec7a58b0cae0c4`

```dockerfile
```

-	Layers:
	-	`sha256:cec40d11941553363ea227ac79b21b5213f6eef7bed4dc6d0fbf1a133a1dc979`  
		Last Modified: Fri, 26 Sep 2025 18:48:04 GMT  
		Size: 7.6 MB (7596183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d61d55aba74c16a67f9a16c82143db556611bbd60a64256f7faed7851a956c2`  
		Last Modified: Fri, 26 Sep 2025 18:48:05 GMT  
		Size: 14.3 KB (14330 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:789b80a64a7b93853f1bda3e963a0d5790ce8b8f8dc46ce929fb1f9c8d3aff7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.2 MB (196219348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18674c4279e47a218b7088b63a8de365d2ba2540acc5bb3f78668c6058c62018`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
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
	-	`sha256:4cb8224e7ffc22512c71f1cfc1042cb22342df02312e61cb1ab0c492c3369711`  
		Last Modified: Mon, 08 Sep 2025 21:18:07 GMT  
		Size: 53.1 MB (53104433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556bc8b266ed0a6d0fe597ca3918c5ddbd8cbe311fc8eeb2f1938b6900c717e6`  
		Last Modified: Fri, 26 Sep 2025 18:01:07 GMT  
		Size: 52.2 MB (52165415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525db461bf11ed9dea04bf3e9b062afbf53b96bcdd069f2929c2f179646ce660`  
		Last Modified: Fri, 26 Sep 2025 18:01:11 GMT  
		Size: 90.9 MB (90948853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f5928e0acf988896145ca01eacf116d4ebcb5eab3e41434d6937077ff696a6e`  
		Last Modified: Fri, 26 Sep 2025 18:00:59 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a037bb2ab265abb3efdca17c38cb7bab2ee99bc5f687a68bfd5f5dd8e75e3c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7607728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69a4f7a54dfe32f00f9856e8682af5b2b13e91f26dd4d224d1f1b2934a282d87`

```dockerfile
```

-	Layers:
	-	`sha256:b8b374f2e6b2b6eddaacb1707522583a5a18ffaefa4c71886dd9f66cce34cf1e`  
		Last Modified: Fri, 26 Sep 2025 18:48:11 GMT  
		Size: 7.6 MB (7593467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f30cbd98a8e31cd5a3e64acb7a408a9f4194492ff1733c8beafb6e0f3be4802`  
		Last Modified: Fri, 26 Sep 2025 18:48:12 GMT  
		Size: 14.3 KB (14261 bytes)  
		MIME: application/vnd.in-toto+json
