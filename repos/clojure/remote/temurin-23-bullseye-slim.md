## `clojure:temurin-23-bullseye-slim`

```console
$ docker pull clojure@sha256:9f50c76eb79f1684a6e9c71083729e21db1d18a3962dd74ae021b428905f427f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0594e486b52a124e15814a840b79690f30ddda35d97d65697d39aefc70c182b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.3 MB (254305027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2c5b12fa750a5f36f57eba5b7985e9a8cdfb09ffaab8e298947efe3daa1cfad`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db7e8d16f520f65c2f8ad6c68b0f7969627407cc8dd2e5509d4900ac94f079a9`  
		Last Modified: Tue, 03 Dec 2024 04:32:59 GMT  
		Size: 165.3 MB (165295132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15f3ff54be14880560d53cebbfceb00ad9868cb7a83b27645412ecc1079301b`  
		Last Modified: Tue, 03 Dec 2024 04:32:58 GMT  
		Size: 58.8 MB (58756214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce05fc3655adf63404b81892c89740ad550f8f9339a640ee3590eb440bb5fd3`  
		Last Modified: Tue, 03 Dec 2024 04:32:57 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85875ede4a5d51079aa6a7e9846d36df8efbc9980ed2bb16835013116a78d99a`  
		Last Modified: Tue, 03 Dec 2024 04:32:57 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f7cdcfc975985b1b1de80d2bdc3c6195f144abf276b3f5161639e5830ff833b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5144440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1904090443f4301a580da7d5b94a267c15296d28b4c42edeeed6e4c507805db3`

```dockerfile
```

-	Layers:
	-	`sha256:53317252a55ebc38b091a6856f33e94ef0aacc41aef7c8d6a42fb763bfa4666e`  
		Last Modified: Tue, 03 Dec 2024 04:32:57 GMT  
		Size: 5.1 MB (5128562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff0a30fd8772f90dfe748a6c84036818c714db8c0ebac42cbdce6fc22bbdc22f`  
		Last Modified: Tue, 03 Dec 2024 04:32:57 GMT  
		Size: 15.9 KB (15878 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:758d1d5ee254e65d4d47bd4b17a69d242adcbd4b1515ff3b76d16061c1146413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.9 MB (250908022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:464fd2743cd44fa3d30310cdabe341281b6435acb82ed5aca681c0494cb645f4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c788e772ea911990d57e5f952f630757d6bd8d9e9c0bb82ec7e6021b67421c9b`  
		Last Modified: Tue, 03 Dec 2024 15:35:01 GMT  
		Size: 163.3 MB (163281795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986afaa046f7de85b2eaff4c728a7ffefc2ba4bdeb616c724c53577ab847d393`  
		Last Modified: Tue, 03 Dec 2024 15:38:53 GMT  
		Size: 58.9 MB (58880265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ec06574d02689990734633b76bcc27ca744884345eb171a2f739736d6d9f19`  
		Last Modified: Tue, 03 Dec 2024 15:38:51 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cbb2da8bac18c29144a886c23037351aaca98a3cb194b3f298cfa0e08285734`  
		Last Modified: Tue, 03 Dec 2024 15:38:51 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6a330d7fc915eb7a8602145beb344e0f4128dc079c48f53c6522ca49b6bc4c46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5149673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0238cb69037e22bfd3d1bedad5015cddf4792dcf8d5b4aeac670056c771ca0b1`

```dockerfile
```

-	Layers:
	-	`sha256:a783360852cf9fef3a8bed473545dd7bb7c0fb247e6c8aaaa31fa2d4ca9b056d`  
		Last Modified: Tue, 03 Dec 2024 15:38:51 GMT  
		Size: 5.1 MB (5133677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:289bf231e4e1de9ebe23bae37403ee3ef89db62a68d4e31bc2bca6aa54e0bb93`  
		Last Modified: Tue, 03 Dec 2024 15:38:50 GMT  
		Size: 16.0 KB (15996 bytes)  
		MIME: application/vnd.in-toto+json
