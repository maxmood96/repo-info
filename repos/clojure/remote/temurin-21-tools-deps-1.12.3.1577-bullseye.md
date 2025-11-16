## `clojure:temurin-21-tools-deps-1.12.3.1577-bullseye`

```console
$ docker pull clojure@sha256:0f146e07e8a4e21a4300bc0399b1d6240e7703bc345619499b82a811d3ca9be8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.3.1577-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:cce8ba158054024d4aa001da46d5655a21abb6c85c8eb978f53397267641ab09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.1 MB (281144763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fb38bc5d28f3b52f0b5ec680bc5e64fb3066eb883d196bc6596f7353608b236`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Fri, 14 Nov 2025 00:54:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:54:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:54:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:54:50 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:54:51 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:55:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:55:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:55:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:55:05 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:55:05 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1e2d66c9d9f8efe285cc550f7cf8cb1194222debc79cfaec92fe8f171356abec`  
		Last Modified: Tue, 04 Nov 2025 00:13:02 GMT  
		Size: 53.8 MB (53756694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aba529ddea5cb85c4de127dffefbb48f54200185871e77994fd1cfb0749f1ee`  
		Last Modified: Sun, 16 Nov 2025 01:28:41 GMT  
		Size: 157.8 MB (157825981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1a4ce0aa9822e83903d57e1c8c0a70961058fa715a8a4ed0aebadeb4b71772`  
		Last Modified: Fri, 14 Nov 2025 00:55:41 GMT  
		Size: 69.6 MB (69561044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6024fe585151865abd8e9820e179356bb2c2894bce3d2df33941352abe48e6a`  
		Last Modified: Fri, 14 Nov 2025 00:55:36 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9a352a303f14a3c1c2fed35e208a88d560cb908a1650d87ef19a05cff41164`  
		Last Modified: Fri, 14 Nov 2025 00:55:36 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.3.1577-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:79eb22a7e59ba80e46a1714042378e3c23e0c26f3955654567e95d3a8410b5ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7414548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:657d3e46754a3d9f1d3a79f7dff4f7c8d0e41ff29f4d119d0c8a2ddb81ab5653`

```dockerfile
```

-	Layers:
	-	`sha256:2d693ec13e47223a58c1c16b841ac8599346bd00018fb27656464c9784a6b075`  
		Last Modified: Fri, 14 Nov 2025 01:45:51 GMT  
		Size: 7.4 MB (7398771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21901c06dccdcc0c210b0841736a7a7cec2a1dc118cdc906b6d5196b07c944b9`  
		Last Modified: Fri, 14 Nov 2025 01:45:52 GMT  
		Size: 15.8 KB (15777 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.3.1577-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ca7fb4006c6210c7fcba0089653204a6fa6e0d4afa44d657db39cc0f44177caf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.1 MB (278055067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4037e5edb538bfc3e03b4c5beb35388ae437252255e80c334b257834b48c7922`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Fri, 14 Nov 2025 00:56:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:56:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:56:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:56:52 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:56:52 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:57:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:57:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:57:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:57:06 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:57:06 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fd1e161a67e40ef9e2635aad60e4206efb76978ad46d67a3d4e7430236c982bf`  
		Last Modified: Tue, 04 Nov 2025 00:13:13 GMT  
		Size: 52.3 MB (52257969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2132c24fc654a76482968a9bbce35b966b96c04a2070dbd22cb879e232dcec82`  
		Last Modified: Fri, 14 Nov 2025 05:05:07 GMT  
		Size: 156.1 MB (156107671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978a674f17eebb3531f7d4b5f7b627ad11af08bc2ee430d18c5d627f9db52c41`  
		Last Modified: Fri, 14 Nov 2025 00:57:50 GMT  
		Size: 69.7 MB (69688386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:756aff4558242666cee227fa9394748fc6be233c93af9a7291600ef0c28a8d1a`  
		Last Modified: Fri, 14 Nov 2025 00:57:36 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8061def0d2fe93e43f8088c3605f824527b03bd06a44f08b70d51a887af7e0`  
		Last Modified: Fri, 14 Nov 2025 00:57:36 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.3.1577-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:a118818b46e6ab1feecf9f7367a19dcb67fb79aa2a6ef340e98d606a1dab902d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7419766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6284f63c2fcb109eb4d9fe53c626e5551b9413664d8b56a85f17217907abe5c`

```dockerfile
```

-	Layers:
	-	`sha256:18b01f58fe0774a89341fb6cbbd7ed8c4a8413a6342e09d62c7f45792b426bf9`  
		Last Modified: Fri, 14 Nov 2025 04:38:56 GMT  
		Size: 7.4 MB (7403870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abf1b5f05546dcb037e224a6b9eeca0499b401f2742e074c639e75d896825291`  
		Last Modified: Fri, 14 Nov 2025 04:38:57 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json
