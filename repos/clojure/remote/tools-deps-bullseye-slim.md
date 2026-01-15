## `clojure:tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:0d23f966044a95927877c2153bfa284517d15b84783844a3e0fc7a1106d7e6df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b96808a6e0379ab09182b5ffc1ed27d2363eaee29b68a142cba69c5e75301b38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.5 MB (181454692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1dbf5334cf1200ad9992e0680d9ff6a6daa083fc7b5b104e614f6682ff8c80d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 03:40:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:40:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:40:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:40:24 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:40:24 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:40:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:40:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:40:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:40:37 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:40:37 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:bd1b97a95a10ded4767bfcdbb3d042b961d107d141121fdbb255239f0ca115f4`  
		Last Modified: Tue, 13 Jan 2026 00:42:30 GMT  
		Size: 30.3 MB (30258497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ebd0333b31601b473effc5b772246f0b76d51a9caded026c90fbb52b54b82c`  
		Last Modified: Tue, 13 Jan 2026 03:41:10 GMT  
		Size: 92.0 MB (92045302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e708d1363a353f57f57ef5a70074db79d2d3604fd7c2843dbb9898432ed61099`  
		Last Modified: Tue, 13 Jan 2026 03:41:06 GMT  
		Size: 59.1 MB (59149854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd095bf0b1fd8473a0c9e325f56038f6391dded2f92c4264c9afa4324fc9e54`  
		Last Modified: Tue, 13 Jan 2026 03:41:02 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed3d396143c75ed9025b2cbd296d40d15a3550e8bd26e8e5b3475c04cb21741`  
		Last Modified: Tue, 13 Jan 2026 03:41:02 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:98b95a1e085e015c74654e32f31df937d1c9d5e2b1be451c6c8afc76a7ec2182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09cea4256389630a5d729b0d49452cb7351bc786c62f8578a882acbfe3adb16a`

```dockerfile
```

-	Layers:
	-	`sha256:ddbc73de2885edf45e66fe7e165025096cc40422d4a3d6071f3e01e29054c599`  
		Last Modified: Tue, 13 Jan 2026 07:45:45 GMT  
		Size: 5.3 MB (5259427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e75723d3c0c31b53ea877c77ac211e77757710526ee659ec2d0f7711e5e7dc8`  
		Last Modified: Tue, 13 Jan 2026 07:45:46 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d85f9b8e47f6953c28dcc78954f3379d4282e2f106709e10f8780daa79b6bc09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179085917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12e720264db40d9cda0776bd5e6b594d201ea56194ed91109ba890c6e2285dbb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 03:44:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:44:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:44:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:44:08 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:44:08 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:44:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:44:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:44:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:44:22 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:44:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7781088accb552d6473ed64f4649a64684d928b7cfad973d13e5c50942bf7a5b`  
		Last Modified: Tue, 13 Jan 2026 00:41:59 GMT  
		Size: 28.7 MB (28748518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b92bf485de9459761d3501b3a6e5213c3755c07748bce31cd08bb962f5070ce2`  
		Last Modified: Tue, 13 Jan 2026 03:45:21 GMT  
		Size: 91.1 MB (91052500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb04682417ece4a133c6a547bd2f624516b7549e6bd72d42d830c15975d8aa6`  
		Last Modified: Tue, 13 Jan 2026 03:45:01 GMT  
		Size: 59.3 MB (59283858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fce8ca91927af0f4b94d8f98e4d54634acc0f42db2a7d94f1df62c9d7a82ab1d`  
		Last Modified: Tue, 13 Jan 2026 03:44:52 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea254a0643dd9e0325dc01de6a14c6340bfa03bfb1608878a430601f3df54a0d`  
		Last Modified: Tue, 13 Jan 2026 03:44:52 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e0ec51393ea8125903922042bd966b3a0ab12152620abcea7649de06438172e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:335c919693b90f982c41e0500ddcb051127a215d369b0e0fd65e6911f493a70c`

```dockerfile
```

-	Layers:
	-	`sha256:af5f58bb8777a5618cae4cd4c41b981f2baaf3062837a7bfa97178917d4b2e62`  
		Last Modified: Tue, 13 Jan 2026 07:45:51 GMT  
		Size: 5.3 MB (5265180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9571b69840270a7fd824f8c840aca0f3d5cde2a684d2abd8c91b41984a96fdb`  
		Last Modified: Tue, 13 Jan 2026 07:45:52 GMT  
		Size: 16.7 KB (16667 bytes)  
		MIME: application/vnd.in-toto+json
