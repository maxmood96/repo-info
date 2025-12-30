## `clojure:temurin-25-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:c040714ecf21d1e9102d957696d1851c6f20d1ecf862d7379aba179c6353a9ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:48bbad727be7257fed346c26d1cf83709e7c78cdb02ad990d6b5bcccefb08eba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.5 MB (181454694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb495459e6ac3012c6c22d59dbd95d1d48ca27a68e13b9cc395dc01a3cfa71b8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Tue, 30 Dec 2025 01:08:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:08:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:08:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:08:59 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 01:08:59 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:09:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 01:09:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 01:09:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:09:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:09:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:37b52eae712b138ea3c9639c687f975153ccba96801de3dc69883975843edb35`  
		Last Modified: Mon, 29 Dec 2025 22:27:47 GMT  
		Size: 30.3 MB (30258441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77950409bfab1b2f2dd49bc0bfd4f5185c4b4ae11825c0a7508c6b09fa4f9acd`  
		Last Modified: Tue, 30 Dec 2025 01:09:50 GMT  
		Size: 92.0 MB (92045301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93af42872d4b0e2ec1ad9c6b3b8e9c4a3666efd31a4ffaab31a3e223d7024d0`  
		Last Modified: Tue, 30 Dec 2025 01:09:43 GMT  
		Size: 59.1 MB (59149910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca53f0a1d468536539d132e7a03d60d895b04cd37a6ba1858cde7f42130c388c`  
		Last Modified: Tue, 30 Dec 2025 01:09:38 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15aa855a89b3d89413278b937fa526d089e5e090b093a6f9ab490a82fcb25e6`  
		Last Modified: Tue, 30 Dec 2025 01:09:38 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:31e7f762f3dd1035a4acd08ca52def39bea1eb708bf89a607815944b988efd98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:331c3e2fc91a9a80ffda183a833d0192d59c38565eed7bf87036ee0d2d8e679d`

```dockerfile
```

-	Layers:
	-	`sha256:6ea4554ecbabc187d6323c2530edf87687b889a71073fc7f03f95539d7cdf441`  
		Last Modified: Tue, 30 Dec 2025 04:46:23 GMT  
		Size: 5.3 MB (5259427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34bacc4ff6ee5d2a004ce6fc8467ec66132d059489462d93bdad926eef4f2895`  
		Last Modified: Tue, 30 Dec 2025 04:46:24 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:57304d30bbaa2c9985a388f2c98410af2a2ff715640abbf077c4252ec940b39c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179086281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb33bc8ea847b3ec525d537f004215c591d9c2a4bcaa1583f878d707ba65046`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1766966400'
# Tue, 30 Dec 2025 01:10:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:10:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:10:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:10:12 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 01:10:12 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:10:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 01:10:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 01:10:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:10:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:10:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2b952d66bc8c719b5ca92eacb4307075591731bdc405a12ebd6fa840a24375b7`  
		Last Modified: Mon, 29 Dec 2025 22:27:18 GMT  
		Size: 28.7 MB (28748462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172774dff4dae7b0fd5632387df01e61cdaaae809bad16dfebc6e3a57d0372f7`  
		Last Modified: Tue, 30 Dec 2025 01:10:59 GMT  
		Size: 91.1 MB (91052481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47b3f2fc6aba57dba50b8cb38b08d07f23fee7577bd4803e3efd5aea4f4e19f`  
		Last Modified: Tue, 30 Dec 2025 01:11:00 GMT  
		Size: 59.3 MB (59284296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7852b3e6c219d3775e2b2354a6c3303beff772f8cf09c399c43149f6288b9b`  
		Last Modified: Tue, 30 Dec 2025 01:10:52 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8dc3736e5b86acb524c9fe4e31430ff3459af0d9725c8f80a1a950e3c72112c`  
		Last Modified: Tue, 30 Dec 2025 01:10:52 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f9c7038dc03445e4e0bd8077e58b4ce03e3e1576e1496544ae3a703848d90d3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a8fc5df8d563511675316f0407874f19a2bdbac25e7460fd635b431ed7b5b60`

```dockerfile
```

-	Layers:
	-	`sha256:9cf638a3825dc1f776614fcf6dfed9208bc1958aecd75930fd9e2be262ed2458`  
		Last Modified: Tue, 30 Dec 2025 04:46:30 GMT  
		Size: 5.3 MB (5265180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:655eca5781280a7c86a1d9ea17a2403e499e635148aba57929bfa2da4430edb0`  
		Last Modified: Tue, 30 Dec 2025 04:46:30 GMT  
		Size: 16.7 KB (16667 bytes)  
		MIME: application/vnd.in-toto+json
