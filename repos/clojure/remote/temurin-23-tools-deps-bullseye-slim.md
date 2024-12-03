## `clojure:temurin-23-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:2686f54a4d39680abd915c7ed0cd8738972e63f9aaa4470a96539fc5e5d7688f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-bullseye-slim` - linux; amd64

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

### `clojure:temurin-23-tools-deps-bullseye-slim` - unknown; unknown

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

### `clojure:temurin-23-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9414d22b921e2d699ffc38fbc4929648f56ed227189a402a6cc4aee2195ac855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.2 MB (252249874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f7eb40482381a4b3bfe7b34acd0c3120d11b0c298463186b804bd3d20b41ce4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
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
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28ca6f73ecea9eadb356f63023098f39244b4749ad15cf045cbfe2b62999eaa`  
		Last Modified: Sat, 16 Nov 2024 05:49:47 GMT  
		Size: 163.3 MB (163281799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1debda06ee56a62d2f6683f9df7e4e52014f7c25bf4edd62d7d93dd83ce3fd9c`  
		Last Modified: Sat, 16 Nov 2024 05:54:10 GMT  
		Size: 58.9 MB (58875436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ccad201912530f864ac805a0816a397f8402394cea25e3d4c1d31ff2cc6b08`  
		Last Modified: Sat, 16 Nov 2024 05:54:07 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2818993103b1dfe6d1bac7a56dc614db614f05d21f6219958c5463030adef5`  
		Last Modified: Sat, 16 Nov 2024 05:54:07 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6ace5eae4a9be1572179cccf0ea83dcf6d3db8591962275e66ff5dc2caed913a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5151474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf563d003db3015a1db32716c344b78e35ca83e1ce13ff413e0d6061b6baac66`

```dockerfile
```

-	Layers:
	-	`sha256:16185335a4a2562232c77f9715ad24affc636cc7be415b7e8a0f6395823d6ce5`  
		Last Modified: Sat, 16 Nov 2024 05:54:07 GMT  
		Size: 5.1 MB (5135480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92a5939ae76bcdfa3810779697e1f9b43df97bdd7e871d7664ef5bc2c2fdfde5`  
		Last Modified: Sat, 16 Nov 2024 05:54:07 GMT  
		Size: 16.0 KB (15994 bytes)  
		MIME: application/vnd.in-toto+json
