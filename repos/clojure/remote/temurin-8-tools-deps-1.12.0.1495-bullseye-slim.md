## `clojure:temurin-8-tools-deps-1.12.0.1495-bullseye-slim`

```console
$ docker pull clojure@sha256:faf9079753fa946d94feb4ae184a25a66ca6362cf889f9dfc994b097bb6df597
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.0.1495-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ad80554ddf7799df2515022debcf8a9b7248b0300952bc8c90a986e06e96b0fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.7 MB (192668161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bea3436c05bb0ad104e7d11fa64d9128f051b4daa05969fc4b6a5284d16317f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6c87eefc1f428634061bcdc9ec95ccceecd7c7475d35a777479af83f64ee6915`  
		Last Modified: Tue, 24 Dec 2024 21:32:32 GMT  
		Size: 30.3 MB (30252643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5e1045d804ecb81340e0c70aa89dbc3a49b4d3dd422cdd6792fdf620740a9c`  
		Last Modified: Tue, 07 Jan 2025 02:29:17 GMT  
		Size: 103.6 MB (103633892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a65902762c7081511e54c3da42dff87c6e60aea4305bfa601c7b53dc4160e25e`  
		Last Modified: Tue, 07 Jan 2025 02:29:16 GMT  
		Size: 58.8 MB (58780984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07425a451014bba872f2451aeb0083d96e5914d9ebda97a5c8736920de663b4`  
		Last Modified: Tue, 07 Jan 2025 02:29:15 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1495-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2200236a24c7d5f92632b03f8e95a471f56ff4134d495bb84d2a1e3106ac5100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5253583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f12b25582a4cc073d9088fdaf471eeb7b5c9b9a095a6c33838c4a7b5d5062ed`

```dockerfile
```

-	Layers:
	-	`sha256:022cde32f568ca1720bc7ab9e1aa14bd6b89b4af5cfc3874b1dc63cac0a67bc0`  
		Last Modified: Tue, 07 Jan 2025 02:29:15 GMT  
		Size: 5.2 MB (5239287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3480fc9097ced95a290882ad2bd147455b746c89435fcaadaf07c8922f5a985a`  
		Last Modified: Tue, 07 Jan 2025 02:29:15 GMT  
		Size: 14.3 KB (14296 bytes)  
		MIME: application/vnd.in-toto+json
