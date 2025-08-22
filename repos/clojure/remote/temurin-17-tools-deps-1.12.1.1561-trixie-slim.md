## `clojure:temurin-17-tools-deps-1.12.1.1561-trixie-slim`

```console
$ docker pull clojure@sha256:17160e1bae14050c8f50a6678a717318f1a5986b00a9ee18c37667e957e2eae3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.1.1561-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5c9f4e72204ed21b7c3a17d321a94af580a5e7b04721636fa714d173cf50319e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246356817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbf179690979938f440dff0a8d0e502b6ad00a51b5608b7b6745e42ef4555c51`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53752c9be324acf0f62da286f2b8a8b8e024a1696c3ce3ff44c0956be9e2a9d2`  
		Last Modified: Tue, 19 Aug 2025 03:39:47 GMT  
		Size: 144.7 MB (144693297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c58f4d289cd27fa3db8a138d16422be3581777f076b333a961ff348d059730b1`  
		Last Modified: Tue, 19 Aug 2025 03:39:48 GMT  
		Size: 71.9 MB (71889192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe7b8cff6d0482d1cd4a4cc25cf06f810144e4e1dcce89e2c79be634268d544`  
		Last Modified: Mon, 18 Aug 2025 16:54:05 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbbadab2dc72546716c51b9bc9ce7929412d2763f4ac287fe4df372ce3827d1`  
		Last Modified: Mon, 18 Aug 2025 16:54:05 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1561-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dba2599fbf060a6502e5cda3bf7fc2993c5297fe533e55e95a6dfba1f3f04378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5271092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e21949aeaf3259a791d022d213037a7f27bc945beb6a21ef8202bf2f2376048d`

```dockerfile
```

-	Layers:
	-	`sha256:1351d6a155d14c118a34d6cf1b716d7e43d164bc8b860ef5cbbb5723c8f0f29e`  
		Last Modified: Mon, 18 Aug 2025 18:39:09 GMT  
		Size: 5.3 MB (5255237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f37e0189e6436222c8fad5a084b88f40f9e4cf5a8586ac238ecfdd955cebce0`  
		Last Modified: Mon, 18 Aug 2025 18:39:10 GMT  
		Size: 15.9 KB (15855 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.1.1561-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:05ae1dfb7a172d40d34e547683ddc4054c45cf4476e03c9a9548e021df842ad0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.4 MB (245384912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15593f7fddfc12d98a133a52d6e58fecd954868953b3fdfac98e8c126d21f61c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640cf07419cf2a2f084e2df121a60b637ba9a6a3bb5fff3ddc4f930742d38659`  
		Last Modified: Tue, 19 Aug 2025 03:40:32 GMT  
		Size: 143.5 MB (143542104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099531cc389de4773a1640b613021d0ff1f977882fef39c5f979705ff4e3cfe2`  
		Last Modified: Mon, 18 Aug 2025 17:12:10 GMT  
		Size: 71.7 MB (71705721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe8913951078ffb3e5ac8b3bb8ad77c0562e010c59988121c6911fad8588a91`  
		Last Modified: Mon, 18 Aug 2025 17:11:55 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f5db556c6e41533a9cfb33a22f62ad18025052457227cd31b7a50a09ad67ea8`  
		Last Modified: Mon, 18 Aug 2025 17:11:55 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1561-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:18c6ce48f21f05eb0d9edcae38adb8be284896ea871a4454c2dd79020312b649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5276979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ce028eec90d75e0065b9e553f0cf0d8899fd02a915b917d8a891f313fdc46a`

```dockerfile
```

-	Layers:
	-	`sha256:c64c95f6dac21b842dc44b8e12fc637bfd4d22471251f632d007a59aa7bfe62b`  
		Last Modified: Mon, 18 Aug 2025 18:39:16 GMT  
		Size: 5.3 MB (5261006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ef7df9c45f2883b9eb4cc7d0e8511a3ec8cbfd8d0474baf8808aa3631ceaa14`  
		Last Modified: Mon, 18 Aug 2025 18:39:18 GMT  
		Size: 16.0 KB (15973 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.1.1561-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:3bb466900916691aa5d3c67b798f1635ed6bab53e635bda14f21fb26a108c87f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.3 MB (255258826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d01c4f5d7bae9fca22611972fd6a74481a395571159c425fcd9841c2aded5a9c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a139213f46a9b4f3351f5b4b2cdb1bc223768bb802b0d7ecc6c23c9602d56ac`  
		Last Modified: Mon, 18 Aug 2025 17:24:15 GMT  
		Size: 144.4 MB (144372823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58acf7ec1f9857504fe8783eec5165b9a3560af58d1e5d8bef741e482922d9b`  
		Last Modified: Mon, 18 Aug 2025 17:24:56 GMT  
		Size: 77.3 MB (77290747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211624adf8a43a87abb4b56cff0cbcdeaab4408b2aba55c74e18634a2bae610e`  
		Last Modified: Mon, 18 Aug 2025 17:24:45 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02679a863369266975cb3e612f10c6eb202117d3a6af6f0a5dbea8b7ee84dbd3`  
		Last Modified: Mon, 18 Aug 2025 17:24:45 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1561-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:deb7954df7189424f01c0a5fa438ca07fa137c53496e5cb47228587bf566732a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8be710fce1d2b06445873408588e8f69b7773587d650359f566a8f27db005a3f`

```dockerfile
```

-	Layers:
	-	`sha256:50bb99030048693f95fc1a874108097a24335d708344d36e05e21943c1adaff5`  
		Last Modified: Mon, 18 Aug 2025 18:39:23 GMT  
		Size: 5.3 MB (5259608 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c12a1f65d34b9b19f34ba33987b29f2d2cf5630f77efdbcf1ad85e31ad34a641`  
		Last Modified: Mon, 18 Aug 2025 18:39:24 GMT  
		Size: 15.9 KB (15902 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.1.1561-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:11e763ded4d615e56bceccd14aaa1dadb822ddf12c414fbd607928e7263d3d7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.6 MB (237628721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91af17712cc50b034716a4a892bbc7b00feba3f54c6a11f54ee3a92c779f0acb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4003c8df477a56c140d3903d6cff477740baf1dc3729dc456ec4837e6f283fe9`  
		Last Modified: Fri, 22 Aug 2025 00:35:07 GMT  
		Size: 138.6 MB (138575688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6b1ccaf434289e2c1046c29f89db9ea2a29b643b74851ab31bbcc636acbe4f`  
		Last Modified: Fri, 22 Aug 2025 00:35:20 GMT  
		Size: 70.8 MB (70780363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f4b068432103d6a323297e51a85ccda25114c02119f55c7a0ebb01a1e0a622`  
		Last Modified: Fri, 22 Aug 2025 00:35:14 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c97b4fda09ad7d223b2356260f7b5ea704d4007c6eb4c63299ffd282c3bb99`  
		Last Modified: Fri, 22 Aug 2025 00:35:14 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1561-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:135356bd71b1edca688df5e800c0dc1a5cfa84bb15c3bb60f153b434470520e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5258685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c739d8e4e75214971003e1f25793bc11bbb955531f0049bbcf721e72f51a5006`

```dockerfile
```

-	Layers:
	-	`sha256:d4bb4ac6536d89d9f7b8422330ffc8b7504386c4f02212c1b6f91ff7ea79d35a`  
		Last Modified: Fri, 22 Aug 2025 03:35:59 GMT  
		Size: 5.2 MB (5242782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab2464aa867a6f5eca8c1222ff388b8266e5fcb36362cd70e5401d41473d1c55`  
		Last Modified: Fri, 22 Aug 2025 03:36:00 GMT  
		Size: 15.9 KB (15903 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.1.1561-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:81b0dd4253d86589388e3b0fdbc5d49282889cf9da473e2c0a83f7f70d0461fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.4 MB (237409727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cf79e8b602a4c845ec05779a3a47db47501c858814e4233c333df196a60e3a5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3144a0cc045b5340a2720cef30a5ac35fe54584715375680594646fdb9f1dd5`  
		Last Modified: Mon, 18 Aug 2025 17:46:19 GMT  
		Size: 134.7 MB (134724368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423235b5ba4000f69748e3492affb75b96515d3bb82f42b73303d2b7a705d25a`  
		Last Modified: Mon, 18 Aug 2025 17:46:54 GMT  
		Size: 72.9 MB (72851256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65bd069fbcbee8e2769a031c1533e1a5f64bea8348c42378d7a710c0c31a8514`  
		Last Modified: Mon, 18 Aug 2025 17:46:46 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1b5c931f84a5fe07f41153f35253e46deb7d36c4b7585b1cd45b55b8ab2009`  
		Last Modified: Mon, 18 Aug 2025 17:46:46 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1561-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ddef1fb91556a7773d4a12a848a34b683e116b153e763267acc2f75f9aa4d6a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5267014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb54d5735dff777c6252f9e8f3c71f9fc035e4058ffde2b2d085ae14cda8624d`

```dockerfile
```

-	Layers:
	-	`sha256:4113e7ca76678ac1757a617c9a307310a555df4ee4fb2c9e6afc741bc507a562`  
		Last Modified: Mon, 18 Aug 2025 18:39:29 GMT  
		Size: 5.3 MB (5251161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca11bab8d2cbe2edc61f165b179edef779248dfe9d48e2a127f3e2e0bd919f48`  
		Last Modified: Mon, 18 Aug 2025 18:39:30 GMT  
		Size: 15.9 KB (15853 bytes)  
		MIME: application/vnd.in-toto+json
