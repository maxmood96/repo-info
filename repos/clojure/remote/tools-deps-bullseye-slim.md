## `clojure:tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:6ab9422ab6f35848c4243f2f571eb035e05e606e43a0f3d0ac6d2ae9a754e919
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:9298ab19d3b4ee99c68d4c709ff23b937087a8cec93a07706de95256809e7ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.7 MB (181699075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bdcbcc4eabae30109f5de3789513465bd346ab277fe4855d9a9b32d17b5f1cc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Mon, 09 Mar 2026 20:36:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:36:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:36:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:36:40 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:36:40 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:36:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:36:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:36:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:36:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:36:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:34f0642d22440b5813561cd4375937013bfb556bec8ff3b0e208699b786282a7`  
		Last Modified: Tue, 24 Feb 2026 18:43:06 GMT  
		Size: 30.3 MB (30258379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87afaaf46e7c705ea548c64ee97a063455e9ea256af7a2f044f458a6b5200647`  
		Last Modified: Mon, 09 Mar 2026 20:37:14 GMT  
		Size: 92.3 MB (92256329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0527cd471d0a15da5e73ac0ccfb51037e65a13e7fd3206126f2c726c0ca734`  
		Last Modified: Mon, 09 Mar 2026 20:37:13 GMT  
		Size: 59.2 MB (59183323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462fc85a4486403545010fe6d2739c532769411b91759db69710012fdf4f1eef`  
		Last Modified: Mon, 09 Mar 2026 20:37:11 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1609af50421e0e935302108ff9ea2b339670fa12301a1dc1a1d2a544189a9fa`  
		Last Modified: Mon, 09 Mar 2026 20:37:10 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:753b580e24a7dc4cc7944ca8ac8c40e7594a930cdcade454d0deea73c17a1d45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5306296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7db18d956b5feabb6b6027da10c105f1712a0c0d7576c4eb421d30228da0db2`

```dockerfile
```

-	Layers:
	-	`sha256:f63d940fe89d125c7b790e526098a96342f26973559ca3e3b1ad3554e6395c66`  
		Last Modified: Mon, 09 Mar 2026 20:37:11 GMT  
		Size: 5.3 MB (5289771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6442e471d3a9a62b3e86423c0d076e2840a03619636ce0e92e05cffbb11733b3`  
		Last Modified: Mon, 09 Mar 2026 20:37:10 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1ddf8bd7e195bf44d7f376c5907fd363039b9f8caf092002aeb19d1e7a335ca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.4 MB (179357399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49259938cc49af948082462ae117dc5cf8ed4da7c26bc4733f5d446d37602258`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Mon, 09 Mar 2026 20:36:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:36:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:36:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:36:36 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:36:36 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:36:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:36:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:36:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:36:50 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:36:50 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:018c0693c4a2532e5636d6115333db6d882da8f33f1f40cb3e88dbe62da21aac`  
		Last Modified: Tue, 24 Feb 2026 18:42:36 GMT  
		Size: 28.7 MB (28744470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7deb6ca27f42b2894a2c96f96205a7569b2be8c35c8f5a42e0f1d7166f9642`  
		Last Modified: Mon, 09 Mar 2026 20:37:11 GMT  
		Size: 91.3 MB (91288274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cea5b2646a4afbe599d9f7ba62d7790ee9c180f16561755902f9b5f2f3eab00`  
		Last Modified: Mon, 09 Mar 2026 20:37:10 GMT  
		Size: 59.3 MB (59323613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e994c541b59e2bdffcf8bd544803d749fbe666984eaaca4b598dd88c47b108a`  
		Last Modified: Mon, 09 Mar 2026 20:37:08 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d411cb6907c5b4fdb69393fcc3e41b50df6850e3eaff20e16713cc977698ab2`  
		Last Modified: Mon, 09 Mar 2026 20:37:08 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1f212b5d2bd076beb275aa29a3c3b1e5e010a927e13f08e00b7926539601f62c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5312190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65759fabc2884e35ad53c5222f04af71bc1811435760bdbb028b8f9bba6f52e7`

```dockerfile
```

-	Layers:
	-	`sha256:c01c51b93e7f2e6e0d88467fdfd0256b89b7d2ff79c69e6975b6294ffa56feba`  
		Last Modified: Mon, 09 Mar 2026 20:37:08 GMT  
		Size: 5.3 MB (5295524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b91f567b6318addc2a237750ed80facad56afc97e769f71113ff6675d4cb242`  
		Last Modified: Mon, 09 Mar 2026 20:37:07 GMT  
		Size: 16.7 KB (16666 bytes)  
		MIME: application/vnd.in-toto+json
