## `clojure:temurin-17-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:bbfb7df1bd384621d85189cc65837dbfbb72c0b99a4cf7449a60dd60934eb7b5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:f21fec4f63d5373061f843e7277b377ac60491e96e76074717a957a2263ceee6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.2 MB (268162085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:318a0092c77e1148dd7775a9a2db8bd1b4382d3e7f13c1bcb79089151dad5028`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Tue, 30 Dec 2025 00:59:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 00:59:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 00:59:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:59:58 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 00:59:58 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:00:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 01:00:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 01:00:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:00:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:00:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:81c5fe73ee38995b42041f20ff8af640cf790ab264e1dc7316c4c1de7eceb4f1`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 53.8 MB (53756440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33170d7d04d6d814f95eaf98aa5216381422617edbae7df4fd7db0968fb04893`  
		Last Modified: Tue, 30 Dec 2025 01:00:53 GMT  
		Size: 144.8 MB (144847950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2803cc0d26a87f0a27caeac584acc63a4c06667529687b5c7370cacf6c849d`  
		Last Modified: Tue, 30 Dec 2025 01:00:47 GMT  
		Size: 69.6 MB (69556656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87dae6414c8152578ef9605700118a4ee2d12fb7fb591b75da9e9f01b9a48135`  
		Last Modified: Tue, 30 Dec 2025 01:00:39 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9b9ebae27d9d09e38ed6efd39e282baa8f4996630d1bb0e1982911a8dc4539`  
		Last Modified: Tue, 30 Dec 2025 01:00:39 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:b082f4324c80e79fa8b58ce7c4a6b2f8fdad10a8bb95041c01c606a13ce42feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7411447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ca0f8853029ae618f4bee2a7f5aa7ef3911362ac044fba5233a3adb29fa25db`

```dockerfile
```

-	Layers:
	-	`sha256:fcbe4bfc63b52e0bbbb6aebb2589c66437b6d55eb47083c656489f15af13c62a`  
		Last Modified: Tue, 30 Dec 2025 04:39:43 GMT  
		Size: 7.4 MB (7395669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dfeabd3e2586c6810b0ec4532c9c0b4d648d0252b0aa77eec42834b5abee4f2`  
		Last Modified: Tue, 30 Dec 2025 04:39:44 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a049b38872254afa42a1b85d76c16eadaac1f06571dcbe2c4177e0d9c669c8aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.6 MB (265625681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5877d1ef61c7318210c9d010baf56823fb0012daf36177eb3196d881b25f1107`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1766966400'
# Tue, 30 Dec 2025 01:01:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:01:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:01:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:01:07 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 01:01:07 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:01:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 01:01:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 01:01:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:01:20 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:01:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9cc7bc8e086c95eb3e992d2c623bd505740ab0a6afcbc89656d0bb477878489f`  
		Last Modified: Mon, 29 Dec 2025 22:27:00 GMT  
		Size: 52.3 MB (52257770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b116e4ad16c4b2998c1475dd51cfd0154440c8200e4868d03ce9abaf372e21a`  
		Last Modified: Tue, 30 Dec 2025 01:02:04 GMT  
		Size: 143.7 MB (143679894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb4a5b55e32ea3c10156bf4303761d4cfd142069fb6dec541e3626f80f17e9c`  
		Last Modified: Tue, 30 Dec 2025 01:01:57 GMT  
		Size: 69.7 MB (69686978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e94a04dba752b1dc79b05f04cd379980004987b0d85e681231dde3acd20b0f`  
		Last Modified: Tue, 30 Dec 2025 01:01:50 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b8baa6b25486e158c5bcdb8f950d453b616c771e66c837261ff97f6b8dbacf`  
		Last Modified: Tue, 30 Dec 2025 01:01:50 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:f514678f2400c961bd3035ca4b014b18154c76162adbb6ef0cc76d49d8190b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7416664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f284bf298ff0874e3573cb55b3b7db46c240db7a0855c7824afed74d471958e4`

```dockerfile
```

-	Layers:
	-	`sha256:dc8661c604ba0be0cce619a801e983887e8b72d2168110c16982ae8810126fa3`  
		Last Modified: Tue, 30 Dec 2025 04:39:50 GMT  
		Size: 7.4 MB (7400768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93a8040b11b1401c5f945e6d18c2ad305e0bf4a51a32424c9bd09712285b7aed`  
		Last Modified: Tue, 30 Dec 2025 04:39:51 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json
