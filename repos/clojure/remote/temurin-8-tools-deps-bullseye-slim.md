## `clojure:temurin-8-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:73b67c55df15339dabc37fa69c147ce02fa63e9d6a95a7c792e9d6c5cbcd4a3f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; amd64

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

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

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

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:826ac6831048189f71e5331c47fee421ace29e1480acbe30f4b7e1cd6f3c190b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.4 MB (190373526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73cac49c14dab361cfb3ddbbc13e2dbeaf1a4501270020152463fb1c069b37ae`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
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
	-	`sha256:b2d6270f53f11e6d7750ff80f77a95d094cb16d3dd2a56adb644e4eb0d7bf8f8`  
		Last Modified: Wed, 25 Dec 2024 07:16:56 GMT  
		Size: 58.9 MB (58880315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6334c5446f1936cf57f2c3d08eed50d116efd4186c0f54ee4be1ceeb2cd3f5bb`  
		Last Modified: Wed, 25 Dec 2024 07:16:54 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:20d0de9f082f8aed8867d29118985f2df13c7c85e8500ec2409e059645d91efe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5260069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22312e1d573ec4d3f7756d1959e2753b332ab3d47d81345584c76272b569e086`

```dockerfile
```

-	Layers:
	-	`sha256:dd6bff0975532e7cd636f6e2646bbedb095d0cb8823b459eacf47d1e1fe1c738`  
		Size: 5.2 MB (5245655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1e316d0d26388a33276e1bb00f576ca99a9f255db4927b084627ac648084346`  
		Last Modified: Wed, 25 Dec 2024 07:16:54 GMT  
		Size: 14.4 KB (14414 bytes)  
		MIME: application/vnd.in-toto+json
