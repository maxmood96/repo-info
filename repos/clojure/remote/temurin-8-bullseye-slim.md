## `clojure:temurin-8-bullseye-slim`

```console
$ docker pull clojure@sha256:1d50ce7643c435731d2ec83554878d7254261904246b20774108a0c243de1f03
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye-slim` - linux; amd64

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

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

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

### `clojure:temurin-8-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fffc1cbe917c646986cbe5dbef20d5049e4f02c36d678502ebe21264c028a1bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.4 MB (190398603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f01bbb4b27a9fef26cc44f8daf55ca9d5918531dffd661d464bcbd774b26535`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
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
	-	`sha256:879a6187682fc52c69294a2f450abdb54e257a50e8133ec6e89cb140345be6ce`  
		Last Modified: Tue, 24 Dec 2024 21:34:50 GMT  
		Size: 28.7 MB (28744853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0955d514f6f2a289bad48cc1c4e8cae663c7421b08d1e1977c003b2d438c33b`  
		Last Modified: Wed, 25 Dec 2024 07:13:59 GMT  
		Size: 102.7 MB (102747715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3439ebf6aa9ce4e8d57b6b69ac389c7b53d199895d3c9de52cc4a3f4546700c4`  
		Last Modified: Tue, 07 Jan 2025 03:19:08 GMT  
		Size: 58.9 MB (58905393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ba74a6a3b92ed091e464479aaa25aa3ef88d8a48749e5a3e64159164aca61a`  
		Last Modified: Tue, 07 Jan 2025 03:19:06 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4ac5da24c86e429896df504126d41fd0296d56828ad07e752d3ddf9cfa7acbdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5260131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af057e1d07bec25cc206a21a239908d1d291f1e3af2e90dc9b4197cf7da383bb`

```dockerfile
```

-	Layers:
	-	`sha256:e92a5a1a18a70d81e7bcafb99df474134662e3a39012518de3ece35333777b76`  
		Size: 5.2 MB (5245717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a428b74057c96f0c0bc065ea057d068db2646982cfeb4294d9429780881fc2a0`  
		Last Modified: Tue, 07 Jan 2025 03:19:06 GMT  
		Size: 14.4 KB (14414 bytes)  
		MIME: application/vnd.in-toto+json
