## `clojure:temurin-26-bullseye`

```console
$ docker pull clojure@sha256:f1d6664a3246685229d44976e7f2621309629e5ae011482a67eb71ce87c6dff7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-26-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:ae3303ff21194459fe1a19a8283b138d337309496390e89991175536f2d58d3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 MB (214811207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8ca4196954be7b5f37f3902092b3ae90e324b1243a257eb4a14fefde0c55df0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 02:23:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:23:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:23:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:23:15 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:23:15 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:23:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:23:27 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:23:27 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:23:27 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:23:27 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c67cddb4b9fcdeefaf829aa012f0ccaefcfa862a558064326104b95b8849cd81`  
		Last Modified: Wed, 24 Jun 2026 00:28:17 GMT  
		Size: 53.8 MB (53773009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b1a70201d2e5c1286af115c63cb26c95faa8fa5a7169b7e6d0dc6e73c7066d`  
		Last Modified: Wed, 24 Jun 2026 02:23:49 GMT  
		Size: 94.5 MB (94524344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad836a90830b682d43a1f53bef005abd2cb450ef036d6640f12a4d96dfa738ea`  
		Last Modified: Wed, 24 Jun 2026 02:23:48 GMT  
		Size: 66.5 MB (66512814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8afe828bae335037c3804ac2c931f91edeb0f138d63dec0d757d440b8056b8`  
		Last Modified: Wed, 24 Jun 2026 02:23:45 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9452fcff7b4cd8808a03a2b053069d727748369b4bd23087df81c9a0d7c38cb9`  
		Last Modified: Wed, 24 Jun 2026 02:23:45 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:65e5308f76f411a8c31dd0b8c8b72e6cd93c5240cfbc33260cbb4ebfcff53f43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7386265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e24d3b93b92b789f346097b04103891f5ed9e6e8df462a44edee4722fc2c963f`

```dockerfile
```

-	Layers:
	-	`sha256:e02e6c7585a29f789d92ea9cd763525da93a49a428ba4aac72dc666f9945e3ce`  
		Last Modified: Wed, 24 Jun 2026 02:23:45 GMT  
		Size: 7.4 MB (7370340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db0dc6b409cc7701fa56f62471a26b2f5d1f7c3bf2aa004a6bfc64a45db8edf7`  
		Last Modified: Wed, 24 Jun 2026 02:23:45 GMT  
		Size: 15.9 KB (15925 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ffa138795b09151ec19325b85e459e53ea6a4ddd3134f47f384bf6ffb0da02e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.4 MB (212440548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c791192f6f2158666820d1ede58e860aed3f60d1c0b85ca65cf62a1d92a2e4d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 02:29:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:29:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:29:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:29:44 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:29:44 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:29:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:29:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:29:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:29:58 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:29:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:35157acdff35db21da73141f382d0dca0f6bc6d183c3a816d283fe39f471e539`  
		Last Modified: Wed, 24 Jun 2026 00:27:56 GMT  
		Size: 52.3 MB (52257219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01cc7546e2980d85ecb306db82cb5139c4388dc5a642ab1a2f091ffe7f9065f`  
		Last Modified: Wed, 24 Jun 2026 02:30:22 GMT  
		Size: 93.5 MB (93504354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e336971e4ef1851a20472f0872b8812e6aab631bed0cd8a2136562ec992bb2`  
		Last Modified: Wed, 24 Jun 2026 02:30:21 GMT  
		Size: 66.7 MB (66677936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c3024f31ec00290d8129e0f2009b208d013317ef709b5378026d3216b8a8d64`  
		Last Modified: Wed, 24 Jun 2026 02:30:18 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d7ed8cd8def9fe2efc8f5af9a94229f54afdffa8a41402cdaf4058eee0acbc`  
		Last Modified: Wed, 24 Jun 2026 02:30:18 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:b3c5808881acabd36198528f7038b18baf0fa159d054bc37aca8d60ef6dbab7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7391479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ca2133e28a347dcef2604ca2c447d11f79f16a5b5ae2b5999690b16109f6e32`

```dockerfile
```

-	Layers:
	-	`sha256:d987df255b3583fcb308d149ee3a0dec73a76225135af859c976d97276e1f248`  
		Last Modified: Wed, 24 Jun 2026 02:30:18 GMT  
		Size: 7.4 MB (7375436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48daa8d97b5cc7e15fab548b592a9a4cfd4b10e5f25192b08aeba015f6046b32`  
		Last Modified: Wed, 24 Jun 2026 02:30:18 GMT  
		Size: 16.0 KB (16043 bytes)  
		MIME: application/vnd.in-toto+json
