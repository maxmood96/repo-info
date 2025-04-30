## `clojure:temurin-8-bullseye`

```console
$ docker pull clojure@sha256:62cca638f0e13d031b4a223b3b788c033a0750b615fa7ae52540a5191935f418
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:66960315c867caa63b30d7b8eeae5d3f3d8486c140487e44fed14dc8256f1df6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.9 MB (177860024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbbec13db5857bff1e1821a0da6cc04ffaa5632531afd27bc9321555970da1e6`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:19f1f54854d69811b3745bdd374e863f2fc2dc765fe37d1a30df3e590273322b`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 53.7 MB (53747740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ae857c483d9db15f355917316c91aceae5e787cac978212c74ba565a9dc1cc`  
		Last Modified: Mon, 28 Apr 2025 22:05:51 GMT  
		Size: 54.7 MB (54716178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17cb4befc0064a1c0f379061d3f9cca407f6a30ab999c63d7dbbbdddb3fd65b`  
		Last Modified: Mon, 28 Apr 2025 22:05:52 GMT  
		Size: 69.4 MB (69395462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290a85fcb4408343e9dcf0fc793035b7d4994ef55681fc97426c4b9445b39780`  
		Last Modified: Mon, 28 Apr 2025 22:05:51 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:02b4adcf0ff59e7a73d89b81dd16d4189a10af61f3135f4af7df860795b93b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7342402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e801c47565888529bcb76185126f76646bd08371c9257f8d45b196c42ce3f28`

```dockerfile
```

-	Layers:
	-	`sha256:39966fff111b6f2c003491a78b9ac11442b0b87fa8b92601d99c9f07127b04a0`  
		Last Modified: Mon, 28 Apr 2025 22:05:51 GMT  
		Size: 7.3 MB (7328165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1716e0add8cccb335cdc0bb545d6c3edcda20caba532a1e4a6d66c65a07cb951`  
		Last Modified: Mon, 28 Apr 2025 22:05:51 GMT  
		Size: 14.2 KB (14237 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:85edbd79b5576371b2f274375a948eeecb6164ba8ff04a8292dc474dcc27bc77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.6 MB (175606544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ccc1f83c101bcfa59dd1a7aceaec0246550b4ada3f66a3d7dc72d3bd02baf93`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9ce0153b823c3af508e9c8a003aa35daca140e8f4578ff2a451ac20469ea739a`  
		Last Modified: Mon, 28 Apr 2025 21:20:53 GMT  
		Size: 52.2 MB (52245979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb2f48618bca1674b7b6aa07975908acb6ec1fe86ee6887bac65ee97038b811`  
		Last Modified: Wed, 30 Apr 2025 01:00:11 GMT  
		Size: 53.8 MB (53830504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c26e7b04f99c52caadba553fcd81233a2492476f261a1074e6c733d82af737`  
		Last Modified: Wed, 30 Apr 2025 01:03:00 GMT  
		Size: 69.5 MB (69529418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858e98eeeaf032740cb7e020b8c57695762b31bdab37630402b65926c6c46aa3`  
		Last Modified: Wed, 30 Apr 2025 01:02:57 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:6a80cce08c4b5538ec00b5395a59709c0de666f016e65f4fc543c4fc67f47e7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7348317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:646f6dc3b3c859bf5afb1d2643ade255f50d8a704334d55f0c374dac19a3df5c`

```dockerfile
```

-	Layers:
	-	`sha256:94e49e58324a6cba30093a97778e357e9e2cfc5d9d434efc14b0a8faf7c55169`  
		Last Modified: Wed, 30 Apr 2025 01:02:58 GMT  
		Size: 7.3 MB (7333962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a311930fbc094aaa3be9585a02ca373124b8b757e256b3284208f52e75ca2a41`  
		Last Modified: Wed, 30 Apr 2025 01:02:57 GMT  
		Size: 14.4 KB (14355 bytes)  
		MIME: application/vnd.in-toto+json
