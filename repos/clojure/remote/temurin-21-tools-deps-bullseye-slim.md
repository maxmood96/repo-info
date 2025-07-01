## `clojure:temurin-21-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:6ce0a319d4ba0be6e92b695e1b68013154f010b065addda84fea65a00cf2add6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ac92dd8fa79e13cf10b5864e43f552ba22ee6f96ba987314b29903ea8124612f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.9 MB (246897297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3249a11770e262eb66affe9a892b3187b0c88ebba77facdc1d0724c87d3bf2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cc41ef31545f10925901837c6dea7e184299788097caaa3fabb57ed109c52a98`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 30.3 MB (30256047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c31cd5c526834225ac1d69b43027ec668b7d99742f42f1b857f06f0ae6b53b7`  
		Last Modified: Tue, 01 Jul 2025 07:08:44 GMT  
		Size: 157.6 MB (157634498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab25fe7e0a9ce031433bb201f75666154389e2fc098dfc1c709ce7543a1ecc4d`  
		Last Modified: Tue, 01 Jul 2025 07:08:41 GMT  
		Size: 59.0 MB (59005712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b62e680f7b69132c1b86fe39d3f7f590ad4e3dc2e2360d8a1f9185f6f0bed5`  
		Last Modified: Tue, 01 Jul 2025 07:08:38 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c0f487c4187416e7f3003fc9c847fec686ec530b153635f62188ab80ad98c4`  
		Last Modified: Tue, 01 Jul 2025 07:08:38 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8a6fb11d3fb188d7b841b85116233ce4de9e0f1a9f14fe02d55592ff889864a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5328410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6485cdfdcae9b46e483e3f12fbbe27797953276b7a02f708a49f62d222500181`

```dockerfile
```

-	Layers:
	-	`sha256:208728994c4a4f8e4394d0a9d67167a1f9fde8510e37b0828bf70aca8829e959`  
		Last Modified: Tue, 01 Jul 2025 06:38:52 GMT  
		Size: 5.3 MB (5311836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0608f408a5a2bccf48634f97669d4bf88925673ff86f1777bbce3d3bb28ceaa0`  
		Last Modified: Tue, 01 Jul 2025 06:38:53 GMT  
		Size: 16.6 KB (16574 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:591b72d49c73844d78121f1e1ed12831cef88b5fe63b9e40cf989ae846ebc0ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243811576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0b588aa9abafec88d8dea753309756047d9269bdd32720c291bafd86b5775a2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1749513600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1efb2a16e6255fa81193190b623ba0668ffa777ab1de41ac5c5d2d2060a47784`  
		Last Modified: Wed, 11 Jun 2025 00:07:31 GMT  
		Size: 28.7 MB (28744185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6234ac02f2dcc239c9056925c661110c694e5f2e647658c2af946ab8e8e50b`  
		Last Modified: Wed, 11 Jun 2025 05:48:57 GMT  
		Size: 155.9 MB (155928823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56046c428cb652ccec24b676ebd7ceadd951ae89707838aed0f95d1082eb7156`  
		Last Modified: Wed, 11 Jun 2025 15:02:37 GMT  
		Size: 59.1 MB (59137532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2d6f801ac205ba10d76d3f9d1b7dfee7711e22a5586831f770158c6c20a7e9`  
		Last Modified: Wed, 11 Jun 2025 08:40:24 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f476b5d38bf73ed6dd72339c866f61a35c9c494de6344bec3e61b8750598354`  
		Last Modified: Wed, 11 Jun 2025 08:40:27 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:969733f35333ac4ba3c54e9e93b118b936a930780f606012926367b37415ba09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5334309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1068edcc9d332bfd5438d684e778a23043ec1409a6612162b90d4231f87b3ad9`

```dockerfile
```

-	Layers:
	-	`sha256:e0c4b60c7e3d5a5e332527dff538959c6b2fb9fb00dd3d29511211076c8f09fe`  
		Last Modified: Wed, 11 Jun 2025 09:39:33 GMT  
		Size: 5.3 MB (5317592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48873dfc43d272c14f4a81cb4f53e544d87fb81148ba01fd0d6f72fed786b44c`  
		Last Modified: Wed, 11 Jun 2025 09:39:34 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json
