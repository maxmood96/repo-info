## `clojure:temurin-17-tools-deps-1.12.4.1607-trixie-slim`

```console
$ docker pull clojure@sha256:c0f841188ba7e20f6e81ec42bc74b85200c1e830a7bf0ee5552eb9cb34f17efe
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

### `clojure:temurin-17-tools-deps-1.12.4.1607-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e89c56ebdd9593e4c85151e78223c4e977e2e1041381d939bcc46b2a76765518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.4 MB (247416975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec762cae4c9a8db39be652d1cac845539e68c43838e3308451c8a79883b52a5c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Mon, 02 Mar 2026 19:47:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:47:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:47:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:47:01 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:47:01 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:47:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:47:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:47:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:47:18 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:47:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315db82081cc839294c38bb54c87fc9b749da10f2c613d67e043846fba2e3ba5`  
		Last Modified: Mon, 02 Mar 2026 19:47:41 GMT  
		Size: 145.6 MB (145628711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc1b12b92c08f2832cb46594e0f23bc5e3226c83c47a590cdf5965227fa6f49f`  
		Last Modified: Mon, 02 Mar 2026 19:47:39 GMT  
		Size: 72.0 MB (72008591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b90e344660562add7b58d2a398ee062379fad2f05b9131a71fdb26f91727585`  
		Last Modified: Mon, 02 Mar 2026 19:47:36 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35cb476b4433f0846ed595b678d9685b8a7f1f0a03ad57ff65631e100c00f539`  
		Last Modified: Mon, 02 Mar 2026 19:47:36 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1607-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:375b4e3edcab2d0adc4afcd6e99b7ce8e5338e506ebca36cd094116b5f0e6712
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5274875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299e0831ba149e8d3ea0ae66108cc60d1ab64346ec888d945084418aa7b62fd1`

```dockerfile
```

-	Layers:
	-	`sha256:30811c17e831cd9cc7565a28379acb575bdda9971afc5fe61cdf4e773d4e5e9f`  
		Last Modified: Mon, 02 Mar 2026 19:47:36 GMT  
		Size: 5.3 MB (5259064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09fb1f7276ea9d0eddbc2cb899c37b6652c709886354a7a499be9408063105f4`  
		Last Modified: Mon, 02 Mar 2026 19:47:36 GMT  
		Size: 15.8 KB (15811 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1607-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0810d1e7aa8cf8bb45af0998b80172f39e4ed2e82f72289105b003ffbe2b863c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246401417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f439e5a3ad29bbdaf41e7434ab54e3a82f2a9334189ece01c6df01f718c3dcf9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Mon, 02 Mar 2026 19:47:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:47:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:47:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:47:09 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:47:09 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:47:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:47:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:47:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:47:26 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:47:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119866638ed351da3266b57ca6835276ec9c3a923240e6dda6ab0ab93614319b`  
		Last Modified: Mon, 02 Mar 2026 19:47:49 GMT  
		Size: 144.4 MB (144436243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e840cd0e19ffdd9c02188fb6dfc9ad745c228ce9f97f2a89d0af1409696cd1c3`  
		Last Modified: Mon, 02 Mar 2026 19:47:47 GMT  
		Size: 71.8 MB (71824034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49c092f1a3748aa04e4d5cc8e7d42ea8fd14d770e0fc45aa8d2a4781868dc8f`  
		Last Modified: Mon, 02 Mar 2026 19:47:45 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413d875f9bfb3e87a6a5fe13ad634ecda6cfccaaab95fc0d12ef92dd8a746aa0`  
		Last Modified: Mon, 02 Mar 2026 19:47:45 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1607-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8898d675842509ab71479562f878f94e4187997ce8f389b947f3515d02211f80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5280762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8456fd03a7a9d84ee6d86ce6fc669e1ed80383e32324eb594e2bf9038afcb3c`

```dockerfile
```

-	Layers:
	-	`sha256:edab2e030ccfafc1ce21a24541902138b6fc2a6b769ca5b3e590446875c59364`  
		Last Modified: Mon, 02 Mar 2026 19:47:45 GMT  
		Size: 5.3 MB (5264833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3701cebc5b26ca239bddda2d84209b498384cfafd47d4fc2672ad77f68002599`  
		Last Modified: Mon, 02 Mar 2026 19:47:44 GMT  
		Size: 15.9 KB (15929 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1607-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:b7f0c8988a81da8820fe2ab603e32343bdf17227055ae2d97a4283e9bfe5bf5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.5 MB (256458872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ba8295bbd836538dc38508975e12d7ab549aa2406a3479548471a7df50a87d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Mon, 02 Mar 2026 19:59:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:59:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:59:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:59:39 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:59:41 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 20:00:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 20:00:31 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 20:00:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 20:00:32 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 20:00:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d62d6b5dc1b4454f99acd7d6194b49731da1884e444727edc9d0f444c53df525`  
		Last Modified: Mon, 02 Mar 2026 20:01:16 GMT  
		Size: 145.4 MB (145438252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc9488df46da259eed2d74e1ac155dc9254fb14df6ad57ef67e67e81757c31c3`  
		Last Modified: Mon, 02 Mar 2026 20:01:15 GMT  
		Size: 77.4 MB (77419361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931633a6ac3d00d9b65061fc7c122efe0dfa6bab9d5bf0b5c28201977985ed00`  
		Last Modified: Mon, 02 Mar 2026 20:01:15 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5683f4173c20cd4b4d8f13c086e56f2f6825f798f3ec644f1d2d5e2af2c202`  
		Last Modified: Mon, 02 Mar 2026 20:01:11 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1607-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dfadb11aed69c635584f00ac60160cdcdce417a95be8a301a8a44f9303f86d08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:272e1d16e50f2b209c30ae41894b9983e9781a2ec10c44163af7f7edab083ad8`

```dockerfile
```

-	Layers:
	-	`sha256:0ebf715fc56497124abee96daf5344d042eaca09d0a94d0d1c1a52f65757bd66`  
		Last Modified: Mon, 02 Mar 2026 20:01:14 GMT  
		Size: 5.3 MB (5263435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f26594486963e32eb2ff9bef41d3f5a274aa54e734932f57da6c07cea1c2f7f7`  
		Last Modified: Mon, 02 Mar 2026 20:01:11 GMT  
		Size: 15.9 KB (15859 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1607-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:347c6d9fb10bcdb64a15328ab047ad3e87e825f933b4b8f69f433dd5aba14a10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.8 MB (241834559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3d48b8142e9b6fb5981bbae91a03b4274affcd2e6ffc04bfcc7b98960d03da1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 11:00:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 11:00:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 11:00:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 11:00:22 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Wed, 04 Mar 2026 11:00:22 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 11:03:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 11:03:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 11:03:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 11:03:02 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 11:03:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c563a7e83c0073076553db10b62cc19d4a3173b8d64e403513851f43436892cd`  
		Last Modified: Wed, 04 Mar 2026 11:07:48 GMT  
		Size: 142.7 MB (142662998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd9c369b7e57674bd40399376a615a15d03cfaed8cc068629bfd9c57653991f`  
		Last Modified: Wed, 04 Mar 2026 11:07:38 GMT  
		Size: 70.9 MB (70894101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5830c8200d9eab04efc03461bc2884100aed7d5bbab9f8f6c8399757e7251c93`  
		Last Modified: Wed, 04 Mar 2026 11:07:17 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c21079c7b11953e9dcf97b5fb0bc4de4689c17f60bbd486b0be7566174cf7f2`  
		Last Modified: Wed, 04 Mar 2026 11:07:17 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1607-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d8af85e9216351db4f07375c5995c0be0ecccda675d07a7430bd79d6e0994253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5262469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f01b2ef10a748cdb06179386cebbb2360002b9de08d437c59ccfb734f688db5`

```dockerfile
```

-	Layers:
	-	`sha256:8da06f5b5b55c6baad96a473ed9e678e22cffa5d07393eaef4a07c065305da8f`  
		Last Modified: Wed, 04 Mar 2026 11:07:19 GMT  
		Size: 5.2 MB (5246609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d2884600df07bfe2d55ab7704088a156ab543f4df60729c3d9c16d947d53224`  
		Last Modified: Wed, 04 Mar 2026 11:07:17 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1607-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:09efd213e54eceffdcf93fe5282d8ceabbe6e5848d764d663aa7d032f5b064a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.4 MB (238438416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdf0deaa410dc0fdbba303ea9144ed1984880cd59f04040b3eb3633e3a566ad5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Mon, 02 Mar 2026 19:47:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:47:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:47:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:47:03 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:47:03 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:47:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:47:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:47:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:47:18 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:47:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745cc7983f05f95a0e68e8aec4faacd5e5c6f8c5b538a10fa3ef6b53c1688a0a`  
		Last Modified: Mon, 02 Mar 2026 19:47:46 GMT  
		Size: 135.6 MB (135627071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3042ff6dc2defb3da5f80c6eda1afb6ff68983f85e770ebfb6f3d04af2b88c6c`  
		Last Modified: Mon, 02 Mar 2026 19:47:45 GMT  
		Size: 73.0 MB (72972125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a0e280301380b4e81187efabb0ece324ac7ba799e1649fef98ff6714969ab6c`  
		Last Modified: Mon, 02 Mar 2026 19:47:43 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab03ce6d0aec614ccc991b85983f2a029bd2f43e0c90bb79f7972dd6ba374ec`  
		Last Modified: Mon, 02 Mar 2026 19:47:43 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1607-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fdec72d5adaaa596c18322af37052a4d36293282eb803ec252867c342098f842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5270800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62353db293507d8e5a0b1c103de9791cf054c63a9210b85508ce9869ca637473`

```dockerfile
```

-	Layers:
	-	`sha256:9eb3f39d69eb2a585e9fde842357dba5a01ce8499445f4b85a3212087741e012`  
		Last Modified: Mon, 02 Mar 2026 19:47:43 GMT  
		Size: 5.3 MB (5254988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ec7850f97422ed94babb17eb7a889667a044afa4081a1c382bc37be499d54c5`  
		Last Modified: Mon, 02 Mar 2026 19:47:43 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json
