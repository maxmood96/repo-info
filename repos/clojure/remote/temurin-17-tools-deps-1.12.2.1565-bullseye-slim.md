## `clojure:temurin-17-tools-deps-1.12.2.1565-bullseye-slim`

```console
$ docker pull clojure@sha256:a50f6fa6f3862ce62b9830d3c1e5a7c068093e2d3e22097d815b4670a2162390
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.2.1565-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1ab69025d4b5458806f9a15062318d0be710f405e2d85491ec9f7b86133d59de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.1 MB (234101269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82c38c8793f53a2586fe3745c260f68388144f37e91b6dda3da73d6f28a33cd4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3e41ca17193bcd7630e4dd210602930b1f94464bdd59680bbf6654206f7707b8`  
		Last Modified: Tue, 12 Aug 2025 20:44:40 GMT  
		Size: 30.3 MB (30256118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85cefdcaa156370e765cc2ac8b84c74c271903e9347b1991ca12d695181915ae`  
		Last Modified: Tue, 02 Sep 2025 00:17:42 GMT  
		Size: 144.7 MB (144693356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06623472503bd29bd30d9dac889090e211608a2a194a1b8f5f1601c2c01a0013`  
		Last Modified: Tue, 02 Sep 2025 01:56:16 GMT  
		Size: 59.2 MB (59150751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f4020a740a446293c1f6b5fedb3e161bd09916f3e02066dd1520d51cad30d9`  
		Last Modified: Tue, 02 Sep 2025 01:56:05 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea917dc95795e004d1234fd13585dbc71e143a6531abaa9b5fb86e5fac2660a`  
		Last Modified: Tue, 02 Sep 2025 01:56:05 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.2.1565-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ffe6699c304d49a57e1c31fa2fae800e0e10930f174d359e7e89cce8abef9fab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5323946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06d823e249d806f6b4f722b8506592a0328672fe0f5d3b6808cd1f66b4244e85`

```dockerfile
```

-	Layers:
	-	`sha256:c1429ccdd6090fe62700def3d4deaecde0daf3d1e27ec4239eae42417b912b54`  
		Last Modified: Tue, 02 Sep 2025 03:38:13 GMT  
		Size: 5.3 MB (5308067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3541c23120101972afce3175f8ed9b8ea7960672f33d913fd7d1d822fbdd72f0`  
		Last Modified: Tue, 02 Sep 2025 03:38:14 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.2.1565-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1e75512aa4a7c1ad16549750981d7d518aec5ee908115fa34014c2d76697d491
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231576302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a838fc5dfd80fec7ce66322179d42cd3c0fe42158e92da4becff009aa8bc2869`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b99ef417bc3eb3946e7b3162f6c19dbca1039f3b4124deb116c3a0ab763e65ad`  
		Last Modified: Tue, 12 Aug 2025 22:33:30 GMT  
		Size: 28.8 MB (28750491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3ae6e888f8d80755e7324ad970040abde4815c597db4a9f05cfdd6ecbe241c`  
		Last Modified: Tue, 19 Aug 2025 03:47:44 GMT  
		Size: 143.5 MB (143542102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d11688ab50ec6a4c8f7e7859401384cf8f08341cbe6226890ed0a95f7e68554`  
		Last Modified: Tue, 26 Aug 2025 17:43:32 GMT  
		Size: 59.3 MB (59282666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28554b69b6d35b83aa1dd1e970f62c8fdee64c013b4f92d0161f18ed35a87660`  
		Last Modified: Tue, 26 Aug 2025 17:43:27 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757c70190e01cdfac9abd943edd49696ffb18e09ae9cd29d5d139ad9afcdc1d8`  
		Last Modified: Tue, 26 Aug 2025 17:43:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.2.1565-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:393b932e14269933e87fb2e5f67a2b7fb45475b45f78dd04f34ea1041b9feb67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5329796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c372dc8acca9de95361efcb9735d65b5871784367115462cee7cbe27a40e134a`

```dockerfile
```

-	Layers:
	-	`sha256:0d981b8fd14ac3a8118d34d1342029c7eea78a50fc70f3a8cd319aabbd4d7760`  
		Last Modified: Tue, 26 Aug 2025 18:37:48 GMT  
		Size: 5.3 MB (5313799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e3def288ad498684055125d9a3b3df359b869467398ae2bb2036db6ad5269af`  
		Last Modified: Tue, 26 Aug 2025 18:37:49 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json
