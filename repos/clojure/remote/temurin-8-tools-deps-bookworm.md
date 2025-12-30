## `clojure:temurin-8-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:18f9f9e2c6acda0f66594ec5bd519d3b61526a6b04fc569e7b3645b24665221c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:97eb6b5ec28a47751c49ee261f8f87286d6aae1941f2bd0db76f9dcf5fa49493
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.4 MB (184363039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ff8b687d492e55c04c2311d180cd61b6d52aa0a593a0efa072390b7e717f5d`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:51:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 00:51:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 00:51:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:51:08 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 00:51:08 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 00:51:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 00:51:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 00:51:23 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c849172ea6a19bd4c8c93920c4a8bc7300ba8a00c06dabd33724b8b93621a22a`  
		Last Modified: Tue, 30 Dec 2025 00:51:59 GMT  
		Size: 54.7 MB (54733390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f301586b61883744529bbf367af1411c746fcfd3d29a287ba8a268a21b3c4a20`  
		Last Modified: Tue, 30 Dec 2025 00:51:58 GMT  
		Size: 81.1 MB (81148208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b413d9196be5837e66314a34b25a1da8a0955392c10120399df03bbcfab3034`  
		Last Modified: Tue, 30 Dec 2025 00:51:50 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:659df4c08ea730af06f4b5c44f401adac0a262b3ded9a82b754ee6bf52b79ea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7510694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6eb157a1a2a933631fb2bac1a3fa17ba0a49879636b1b8c1e0db9c30370a18`

```dockerfile
```

-	Layers:
	-	`sha256:19cb7b28e8d3507a4857cc315b5ecda2927539ab255808bf9d9333f63fc7abc4`  
		Last Modified: Tue, 30 Dec 2025 04:48:14 GMT  
		Size: 7.5 MB (7496500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:deddfcc6dbe2a8497654852d5cc0a9edbeb103e41c12a878f217b4f5a54f924e`  
		Last Modified: Tue, 30 Dec 2025 04:48:15 GMT  
		Size: 14.2 KB (14194 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3faded6c90451e9688de7b24a326c84a5fe1195f345d18f2703da320da40d06c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.2 MB (183200501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a9611c93dfea662a14ac9cce412d1e195c7ab5da8c9727641436e8a48e4589e`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:54:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 00:54:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 00:54:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:54:39 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 00:54:39 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 00:54:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 00:54:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 00:54:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:bc82f51ad2e6d256131f87c3aebb045333f03c39e64a6b4985cc9e6ea5602d4d`  
		Last Modified: Mon, 29 Dec 2025 22:26:42 GMT  
		Size: 48.4 MB (48359147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30214f1492318f4a2362ac906f8fa13aa70826716091930a643fa5f3a1629d1f`  
		Last Modified: Tue, 30 Dec 2025 00:55:23 GMT  
		Size: 53.8 MB (53814985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c556aebf5362d4728048edaa867242e8c66348867596a57eba811c4c1373c7`  
		Last Modified: Tue, 30 Dec 2025 00:55:31 GMT  
		Size: 81.0 MB (81025724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6f71534aaf7d18680b81f0093fcea853fa66ba1e201410a9e1077ee9cd0c09`  
		Last Modified: Tue, 30 Dec 2025 00:55:20 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:978175d13ce0792ae5ce3305b6a3d52d874b4aa4b409cba19085ad63cb634f3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7517273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c884c51653b273e7a64f0374106535455221da8f54eed6f31d780886705ec2b7`

```dockerfile
```

-	Layers:
	-	`sha256:2d8ecdecc6502feccc851b874074148b6a7668a32024b8f76eeaf2b832c6fe20`  
		Last Modified: Tue, 30 Dec 2025 04:48:24 GMT  
		Size: 7.5 MB (7502961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40088210d32c229f5aa0332d1105cf8a3b02cb2c08914f84adabbb118f273383`  
		Last Modified: Tue, 30 Dec 2025 04:48:24 GMT  
		Size: 14.3 KB (14312 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:01b7ede035b936ba552bd646812d23cce0f7f862442099fc5b76116d3c093d39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191485004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79a4148d2565bca5797df61cf56b8c58c2e6f0d72c913b2fe5c8e672e5c0d11a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 01:37:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:37:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:37:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:37:42 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 01:37:42 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:40:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 01:40:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 01:40:10 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:48e256c4119c0ad256492d6a930e99d2b2d7f8d7920d619aa2de4f616c37076e`  
		Last Modified: Mon, 29 Dec 2025 22:25:39 GMT  
		Size: 52.3 MB (52326998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47946acdfe0b67a6e1db4a2b3b2f698f4c262ec2a112bff084a70f8d9d3aeb9`  
		Last Modified: Tue, 30 Dec 2025 01:39:03 GMT  
		Size: 52.2 MB (52175138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a2dbaf7ef1570c8f823cd4d5de7e9070e758c09d590fd77e093f3754c66b39`  
		Last Modified: Tue, 30 Dec 2025 01:41:09 GMT  
		Size: 87.0 MB (86982224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cbb0371475a11b49230e88242066369ed61569c3586eca14036324031c89ecf`  
		Last Modified: Tue, 30 Dec 2025 01:40:57 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:3eb52524f4fbfcc092d8a5fb6bcffbafcc5b1e15a6f6743571d77a204f378d0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7516548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5067300440ae5535a2497ee19dd4600c3a6d7b2f8dd407a6967fad36f164ec7b`

```dockerfile
```

-	Layers:
	-	`sha256:751c60de14d3e96ce14622faae9ec57726dbff8cea5b577bfd1366bb0d51af14`  
		Last Modified: Tue, 30 Dec 2025 04:48:31 GMT  
		Size: 7.5 MB (7502307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d2ceea1717b2e30158f512f296da488f66504faa68efba6f869be361a309c54`  
		Last Modified: Tue, 30 Dec 2025 04:48:31 GMT  
		Size: 14.2 KB (14241 bytes)  
		MIME: application/vnd.in-toto+json
