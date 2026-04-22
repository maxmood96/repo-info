## `clojure:temurin-17-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:01abf675daff7601e470f304e65b23b50e6f3327e59421a7fc18ed820f4ba353
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:65358747e9342b34ea9caad1247eebea29905681ff99728bf3144ffb490470bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235079992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7651b8c288dbc7d8395e94f5ece01cb5837db0af7a58f8c72eca71fdb5ddd42a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:04:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:04:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:04:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:04:23 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:04:23 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:04:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:04:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:04:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:04:36 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:04:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:60fb1d5aba60afdf7cbf00cf9bd0c125e0c9c2ef7f454a7a88b456dd51794fab`  
		Last Modified: Tue, 07 Apr 2026 00:11:21 GMT  
		Size: 30.3 MB (30258019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6faf79026f6babd44b04dd5887986383cd0cbba011db172ef5114940c456ac0`  
		Last Modified: Wed, 15 Apr 2026 22:05:00 GMT  
		Size: 145.6 MB (145628776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf2fdd4538c728b87790a0b2d222c4a4b0d485cd24d11b1492ee1ba394644ab`  
		Last Modified: Wed, 15 Apr 2026 22:04:57 GMT  
		Size: 59.2 MB (59192155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e500d194476571f5ca11b99c8e4ca32aa808b3a6d25d420e764d7421974a2cd`  
		Last Modified: Wed, 15 Apr 2026 22:04:53 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5869097a110b105557117954fb21e821014e04be333db0c15c023ed4aa17908c`  
		Last Modified: Wed, 15 Apr 2026 22:04:53 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6caac81f94cef8deb4f78f807c27ea69bf556f70ac36932194ed4ea4aac601dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5335887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9932e5d5760c6277b0721b2e526f26331529b9f4e9b8e0bd30ffabc47a0482dd`

```dockerfile
```

-	Layers:
	-	`sha256:57e2c324713c12f161e89bc0bc2a8e6161293cc259b7725c2c264773cdf49c6d`  
		Last Modified: Wed, 15 Apr 2026 22:04:54 GMT  
		Size: 5.3 MB (5320053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3db656961f850861741682055e87940137f38efd4d866a75e9951aecc5b35dcc`  
		Last Modified: Wed, 15 Apr 2026 22:04:53 GMT  
		Size: 15.8 KB (15834 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8bed05e03e4778375052979f4676182d13377b4c04c84eae890a5672fafbcf7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232510871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c68965fcd5bd5250e449a100b038d9a0faf8b6fe96fa79c360f3a22c4eefa0b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:21:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:21:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:21:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:21:53 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:21:53 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:22:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:22:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:22:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:22:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:22:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ab304f220d8a8ccbd47569f385750aa3f87cafd221f915b82f8e566f1abe130b`  
		Last Modified: Wed, 22 Apr 2026 00:16:28 GMT  
		Size: 28.7 MB (28742512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca66113d91a0e3eab2f159e6e6509499f8ef1e9525180a9674951ab3698192b`  
		Last Modified: Wed, 22 Apr 2026 02:22:29 GMT  
		Size: 144.4 MB (144436243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5338c3ab91fa8e283db73fe0f9b9c154eb3f1374044be8b50b0cb8cfc7093f9f`  
		Last Modified: Wed, 22 Apr 2026 02:22:27 GMT  
		Size: 59.3 MB (59331078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a1e87cc3d612ab6be252e148ffbd5b855aec63bdc163ca303bf3add9a1e836`  
		Last Modified: Wed, 22 Apr 2026 02:22:24 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1717ec1025de7e37fe311b24fab0a79df4242cd460f878d67157dd03d2b15bfe`  
		Last Modified: Wed, 22 Apr 2026 02:22:24 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d14ef4ac2de990e11b27d91228eaa0409f882269e477c4b1c135009d6aed5ce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5341738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0d6fe5fd51d1400d962dce164c1418af33425be3bba71f97b9b28bead02fea8`

```dockerfile
```

-	Layers:
	-	`sha256:80f93f53d724eb852a1b5e9a9f11eadf42fda920ec9978d35dd2002a9b74e990`  
		Last Modified: Wed, 22 Apr 2026 02:22:25 GMT  
		Size: 5.3 MB (5325785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74944cba80a4075b4646fd390c18548f016c78a0c2d3b8e34d1475f5d98cfd04`  
		Last Modified: Wed, 22 Apr 2026 02:22:24 GMT  
		Size: 16.0 KB (15953 bytes)  
		MIME: application/vnd.in-toto+json
