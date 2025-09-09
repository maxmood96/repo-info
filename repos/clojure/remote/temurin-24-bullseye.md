## `clojure:temurin-24-bullseye`

```console
$ docker pull clojure@sha256:bbce56324dea5a66a9dbb06f5b1a0137640ba29cd3dd2d3e9e3139c591b86a21
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:3673b87d672acd9c2ca75d3bfa2d14830829a73946545144c9dae0a39aefc507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.3 MB (213288610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc8aa96b12d7c6a99a9eeb323a4e0e2a17b0c6e97fb168f78635f02dd1aacbe9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
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
	-	`sha256:035115815e46101f9c9956e02e706f2f3ec8748e2b415f0d232b51eb76a6a779`  
		Last Modified: Mon, 08 Sep 2025 21:12:56 GMT  
		Size: 53.8 MB (53755396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ddc3fce4317ae0ae2f3fa0aeb0c5a46ac5a267d694ffccdc1f0491557059cfc`  
		Last Modified: Mon, 08 Sep 2025 21:44:09 GMT  
		Size: 90.0 MB (89975251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11701e08c0b575826bbaa2fdd9c4c5a6aa8f3f111f2ffb8652910997f29eab2`  
		Last Modified: Mon, 08 Sep 2025 21:44:09 GMT  
		Size: 69.6 MB (69556920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4036646ea629c2b91c537aa51e931458ef633dcc33164c472fe0e2477d3b6a7b`  
		Last Modified: Mon, 08 Sep 2025 22:34:10 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2a5c9ad0a6762426375ea439231c82020cc053748ed0c16c57cfbdc267c91b`  
		Last Modified: Mon, 08 Sep 2025 22:34:09 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:b3dba2b5b733764ef7c19bc0dba72a3961a56994ab32cf13957bb404f576e5ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7362129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eb9bd897d09dd4ae8847359ef41583c9799f3a9cd4647fc196f7165a6d91c18`

```dockerfile
```

-	Layers:
	-	`sha256:6a0d6f5a71f7811ccee54e0bdb8ab789d345b64be6b1cb818de27c137ae47ee5`  
		Last Modified: Tue, 09 Sep 2025 00:43:26 GMT  
		Size: 7.3 MB (7346315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d403ca22f9c0e04f252954b7a8b69c7a1e8144c5e533b63dc2ea5a513ca9ce8`  
		Last Modified: Tue, 09 Sep 2025 00:43:27 GMT  
		Size: 15.8 KB (15814 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:83a08bcf1c5fd9564d2bac650fab6f0293ad7941ad7d30680a76926aad6ce6a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.0 MB (211025835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f8078474321a1a0a2e6ed0aba869dfab953cb79624f401837386f4f50e919fd`
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
	-	`sha256:7b68ea47bc3cd8615e51fdbe0976cb4999ba56ce8764e755543a4521d69a32f6`  
		Last Modified: Tue, 12 Aug 2025 22:08:57 GMT  
		Size: 52.2 MB (52248409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab60d85f112d5a9f600a471ed0d0ae6ac7f386dc0d9adace00ab46943420b1b4`  
		Last Modified: Tue, 02 Sep 2025 08:24:03 GMT  
		Size: 89.1 MB (89092502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec011300026fedf1060c1bcf7a65bf10f716f7ae2ab720ce8d9dfd1b9e5532fc`  
		Last Modified: Wed, 03 Sep 2025 07:08:03 GMT  
		Size: 69.7 MB (69683880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6a69adc3d02b9531ebe4ce06a80ebc78848e509fed55f7dc4dd8b79c77a59b`  
		Last Modified: Tue, 02 Sep 2025 09:19:04 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7021c510df81c0d38489576058118308fa015ce21e6f0acbd4be0c99bc4744`  
		Last Modified: Tue, 02 Sep 2025 09:19:05 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:39678b358d062f3139d17e934e2c7c15f3e0112c6cf265552e98b49556e1f814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7367341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de45e97f421535c467b960e29832d30e62ab0e61a25593ee1cbf3b8c7d3bb9d3`

```dockerfile
```

-	Layers:
	-	`sha256:4926eee80bf3b741d22a4ec098ea8f3831d8b8203981023f1819cc2539dac6fb`  
		Last Modified: Tue, 02 Sep 2025 09:42:37 GMT  
		Size: 7.4 MB (7351411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:911cc441995366bcb64e2246850c33680a0832d48033218e19c260d1c51b465c`  
		Last Modified: Tue, 02 Sep 2025 09:42:38 GMT  
		Size: 15.9 KB (15930 bytes)  
		MIME: application/vnd.in-toto+json
