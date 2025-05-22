## `clojure:temurin-24-trixie-slim`

```console
$ docker pull clojure@sha256:1bfa6cd1f2802c8abb425d8de27af74e04099998e461ce058c7b2f381ec92784
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

### `clojure:temurin-24-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4347cf6a956b05e2c1ce705c5209b2ff6b7dd8e52f918c82399eab9fd19de9d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191431403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a89f3c1975d1d4a69c72e559b79de5ce1e6254938e051e35d90db9c8147b2928`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ced038dea045df288fe9bdbe03117ca66fe2a071217e196ac86ed07f965fe688`  
		Last Modified: Wed, 21 May 2025 22:27:59 GMT  
		Size: 29.8 MB (29755384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c19fcc1640eebff50aa5903f43a258e337b8bfdfaf5e94fa811c522fe2af352`  
		Last Modified: Wed, 21 May 2025 23:34:02 GMT  
		Size: 90.0 MB (89952000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b28ca44287ab116d1d0bc154baa737ef8dbb1fe0514cbf95f143cd47ddb6ec`  
		Last Modified: Wed, 21 May 2025 23:34:02 GMT  
		Size: 71.7 MB (71722977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277f9320884a6cf54227d615b9d2d824425bb94451e4f10ea63eff828acd4441`  
		Last Modified: Wed, 21 May 2025 23:34:01 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5195bdb065bccea65a5853918af118f8ae85711bc4745a9bec06c90deac4f0f6`  
		Last Modified: Wed, 21 May 2025 23:34:01 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a6ae07803e5915326afe2af9959f3628cabfa43d6000addb16a09bf2f05c939a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5078559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633a24598f14d237788688ebcf0ea5a0242a6cce23c82dbac9cef5bb285388e5`

```dockerfile
```

-	Layers:
	-	`sha256:b4e9518f95c4c0bd906584d6e177955a37b91fec4fafff0e910ba5b2f771f8e9`  
		Last Modified: Wed, 21 May 2025 23:34:01 GMT  
		Size: 5.1 MB (5062711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80326ccaecbd629e9a4725e634cb3ccfe27b3a10c1b923c1121bc5ad916d0e76`  
		Last Modified: Wed, 21 May 2025 23:34:01 GMT  
		Size: 15.8 KB (15848 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:92afe7a6bdd9f837ff80b3212f484addb527d944137f67ec40b3a792d84ca06f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.9 MB (190858378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:332174daef054657c740586ac3bcd68070ff5928344eb0170881f7b99647a7d2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6098c2c9fa277c00ab580ce12bf64a9e1edf9e9139ba18ad85f3cc3063834aa6`  
		Last Modified: Wed, 21 May 2025 22:31:23 GMT  
		Size: 30.1 MB (30119455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:194de15ac003645cdf70d8dee3cb31319b90b7ad1a9df39b395a929d25343093`  
		Last Modified: Thu, 22 May 2025 08:43:09 GMT  
		Size: 89.1 MB (89091185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0abc6874f82cc1d70130c7a20667eca0a39bbecab32d8076da7d6b0f0d5c0d12`  
		Last Modified: Thu, 22 May 2025 08:47:33 GMT  
		Size: 71.6 MB (71646700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f606788707827c06831d8a3395b3821d1777de336662b1a3e8c4913893e12bd2`  
		Last Modified: Thu, 22 May 2025 08:47:31 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f4ebcf732d2e6547a5427e778a4e9589eecf0e6a3276029685049fe95ce506`  
		Last Modified: Thu, 22 May 2025 08:47:31 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1b9a88d464f1376624f21d30dfb6f16f2f1784cba0bcb0eaf7cc1f28142ce7eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5084443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e18af0cc252137ee388062744198354785eb06704cdddbe7909aab55390e12a2`

```dockerfile
```

-	Layers:
	-	`sha256:358e3f4c0e98fd6f5a2ee70007b3ae13527941bf97e8e2b62705a131b1096bf6`  
		Last Modified: Thu, 22 May 2025 08:47:32 GMT  
		Size: 5.1 MB (5068477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85df65c6d44b0786fa45f77c8e40001b7609828e11250f3717da53b9d9f12e6c`  
		Last Modified: Thu, 22 May 2025 08:47:31 GMT  
		Size: 16.0 KB (15966 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:aceae28d1603d12c8921d26488000f90876b08959fc0e89060eb2ab80a9a763b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.7 MB (200713883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edc7cf8b579390766f0fdf8267eda12c3078d2066e5ba866584c768103045d32`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a739447e8599431e1e4996b4b6d4022822d37eddea9a3737acbea74b8a860d49`  
		Last Modified: Mon, 28 Apr 2025 21:25:59 GMT  
		Size: 33.6 MB (33577694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8803762d089e91a891a211912215216c857d1bcb4d597780a3b0fa903fd22f`  
		Last Modified: Tue, 13 May 2025 19:37:16 GMT  
		Size: 89.9 MB (89920243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63235b607e1043b74347ac88b0f5477c1605cb3399008f758cc834da7660e04`  
		Last Modified: Tue, 13 May 2025 19:44:30 GMT  
		Size: 77.2 MB (77214905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3593b4b9cb9b0483c1c1b7f90fe2a9e0b8a28f30da5af364396dc4abd3772369`  
		Last Modified: Tue, 13 May 2025 19:44:27 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c58210d21e481a0649dfa5997f4576302d8513ff3a2deb618f94e63fc0ff196`  
		Last Modified: Tue, 13 May 2025 19:44:28 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b3b33cc89830032075f7614a74e5fbed453fec82dbfd76b53d8e4b0e1b3411a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5038736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec37d83c88c03f5c480961c867a878345bfca19540de9e2577d51c77e8a77dfb`

```dockerfile
```

-	Layers:
	-	`sha256:d03736efe85864671424e4034085fa38d957f0ed378390bc2a9af55269b2dc2f`  
		Last Modified: Tue, 13 May 2025 19:44:28 GMT  
		Size: 5.0 MB (5022840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5287ca572e65bdc081bd0e16cc451f1a5a426425a86a3a48c2e531d40d084cee`  
		Last Modified: Tue, 13 May 2025 19:44:27 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:856d3c74f69fe2ac1c1b9b437dfccd1f4252cca2d3d55d1f06732baf9ff3ed54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.6 MB (186560818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c47a327eb9fc9cf26bda348e161d3d1f6c6b88c87398a2e52a21d456b9eae7ef`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f092cb6a76bde9a7b3c337ea49e8a7adec71062dc5df097be99d3975e92bc53a`  
		Last Modified: Wed, 21 May 2025 22:38:21 GMT  
		Size: 28.2 MB (28245354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48520921fd3b539bfda2058ded0f2724c28bfb9b6163fa249dc8bc5476454af`  
		Last Modified: Thu, 22 May 2025 00:47:54 GMT  
		Size: 87.6 MB (87622251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb01f386008f25824d379d78916736e434ba7395ac497aff23c8c422a08acf8`  
		Last Modified: Thu, 22 May 2025 01:02:39 GMT  
		Size: 70.7 MB (70692171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91af2cf5dfbf7d20b4406f96906fbe00ea99b0c3e3fe4c131c07fa227758d4a2`  
		Last Modified: Thu, 22 May 2025 01:02:29 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3e8dc9ffb729fc15987aaf2c99be64eb45ec353cb34addaad8c206984f5b73`  
		Last Modified: Thu, 22 May 2025 01:02:29 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:930faa655d5ef047e6c0f5fc956aaea7a3639454a662d3f65e5889910c508220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5068068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ff05bbb56a959417bd7de312efe197c127c8a467db482af934c9700caa335b`

```dockerfile
```

-	Layers:
	-	`sha256:f559236862ab67b89a7ab3b307f3d1eba16e1b4f96f5300b352732978a57e4e6`  
		Last Modified: Thu, 22 May 2025 01:02:30 GMT  
		Size: 5.1 MB (5052172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f755089ede0ae4f97ef173264060d867f297c631f6b32e7b61f5014f5bc4e8e7`  
		Last Modified: Thu, 22 May 2025 01:02:29 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:5924cf5ca7a06b7e9945bf133e1e6b8dd4511e0732d5286f5a96c139662be5b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187859406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:946e0024640d13ac84206c78a17cfc18b25df3ce7138710b614da9ac729e9453`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7cbda353d6047374e3da60bdf79ae89f8047840010f0964c87a8f2714e146106`  
		Last Modified: Wed, 21 May 2025 22:32:10 GMT  
		Size: 29.8 MB (29829620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23819e9a6f660656140faefb0803a95a0ac0d02661346d1fc445aafdafc5e949`  
		Last Modified: Thu, 22 May 2025 04:08:52 GMT  
		Size: 85.2 MB (85216727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9518227ace0764dd58e73b4e297f411e3a1ba7a1ab485923b4b224f526bb33`  
		Last Modified: Thu, 22 May 2025 04:12:49 GMT  
		Size: 72.8 MB (72812023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3ce6a769a3ab0178514428da5aaf9c4948519fc3e2eb30381fec32a3c4e2d3`  
		Last Modified: Thu, 22 May 2025 04:12:48 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2b3c6ec91b0fcf8d3755e98b53f7ca1e916524109ee227035ccfd6424d31a2`  
		Last Modified: Thu, 22 May 2025 04:12:48 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:847c489c86bfd6a603e99c78ee409c3b515c43fa077b60f7681c4a5a97fb8207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5077031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a817166117f80421e921a5f7ac2212ce198c234201eff80eb39fe42d8161f0`

```dockerfile
```

-	Layers:
	-	`sha256:a81574ae514c102415a4347f30bec073e90e3823276a207ec50aabc62443f016`  
		Last Modified: Thu, 22 May 2025 04:12:49 GMT  
		Size: 5.1 MB (5061183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ed49d808369425f8c7dd97b6e46d4f35537917b277ebd5be915037ab270fc5c`  
		Last Modified: Thu, 22 May 2025 04:12:48 GMT  
		Size: 15.8 KB (15848 bytes)  
		MIME: application/vnd.in-toto+json
