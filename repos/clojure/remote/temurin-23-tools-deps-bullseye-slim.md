## `clojure:temurin-23-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:824991a265247ca4b145c9438c240814c69e37e50a00eda7ad407f307c254b72
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:eb658b0a753574b6df65ca2186f6794661c8f51d18dd67d0c30b68fc59b8d7bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.3 MB (254336669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff972e2bfc6b876923ac7346da196a9132fd32eb0cd14c71692246a73641833c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa6d958247a265f84b47030af418a10cc5c263b0a448a008403cb7b60e237c2`  
		Last Modified: Wed, 29 Jan 2025 20:27:49 GMT  
		Size: 165.3 MB (165295113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217c1e11c52dfa8829ced08546c1d2ec3332492f00b7b691ab2fab0554e60d8c`  
		Last Modified: Wed, 29 Jan 2025 20:27:47 GMT  
		Size: 58.8 MB (58787850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31191dfd2a4a3547137ea94c402a1efded759980ab89205299aacfd583afd3c7`  
		Last Modified: Wed, 29 Jan 2025 20:27:46 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae381e16b31548be2e75de1ff51b4713e574c66a11e6c42453535695b3e48dc9`  
		Last Modified: Wed, 29 Jan 2025 20:27:46 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2c2e682e37e2b9ef4171e0850b76afe17270b247b43d4526d3e2ab1541232d80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e0fe80dd80fb724422f05135d9ab276aaa114541c987d10f53a54c30e253684`

```dockerfile
```

-	Layers:
	-	`sha256:d2c2c95b00e56a17a03bd779af46cbdf28f46d444fb87098357451716425de06`  
		Last Modified: Wed, 29 Jan 2025 20:27:47 GMT  
		Size: 5.1 MB (5122074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dacffeb96955a8bfa017c80cdfb2aabb7037c5d134691cc8b48bd6f76e5c663d`  
		Last Modified: Wed, 29 Jan 2025 20:27:46 GMT  
		Size: 15.9 KB (15878 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4c289fd2599d63d45998f29e96e00b4ec5a415b716f9502f6440a068281b1e1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.9 MB (250936809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a97c7e528d2db39b77aa8053e2ce3ae51973947b966a2fff7b97df3293bae73`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e71e71a7a2f1c4317d95aab1ef47ce698a25d97fba226c509a728d57301d5e`  
		Last Modified: Thu, 23 Jan 2025 03:56:48 GMT  
		Size: 163.3 MB (163281804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e669dad5ad51e0b132a8ce028623a05c535e2f6c69b3f6bb8fd659f35189cff5`  
		Last Modified: Wed, 29 Jan 2025 21:00:04 GMT  
		Size: 58.9 MB (58909050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a47df5a8608f1a317db79e62a295fb18dbc5cada2dccc4176f7de4d86013b9`  
		Last Modified: Wed, 29 Jan 2025 21:00:01 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0734d35249bac2aa03b82b78689c287bb73dcce17ab93c626f8af29cde4d51d7`  
		Last Modified: Wed, 29 Jan 2025 21:00:01 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:004fb5a0de6a13e92bf81b58481759a3b807c18094df60585bc26b2a6f712716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5143181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a4885888bf05278336c5e7f1af7e78f2ff79b8de692a436ee84aa8ef669224e`

```dockerfile
```

-	Layers:
	-	`sha256:c72aebea32c0c20d2a7b3874ca89bc6990e6604e676ef07be7505e1566e031b0`  
		Last Modified: Wed, 29 Jan 2025 21:00:01 GMT  
		Size: 5.1 MB (5127185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bdd9bc25d537067939d91917f3cab7f4322fae7a509fff64cab31938c43300c`  
		Last Modified: Wed, 29 Jan 2025 21:00:01 GMT  
		Size: 16.0 KB (15996 bytes)  
		MIME: application/vnd.in-toto+json
