## `clojure:temurin-21-bullseye-slim`

```console
$ docker pull clojure@sha256:9cbacb24295da3afc5f882facc02deaf3fe9bf4a6fefe14299ac0f2ac50882fc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:714d840a1449023f58263847852af94f7f27f1fbf43b181139fff9c8dfec2d7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.4 MB (248352308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dc3f10dc10175ecfcee46a6e0633b2b58a24d002e6b83f6fc526fd0f3241c74`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7080db256fffd5c8d1202dac128df392b0494c474ac393236cdc1e6595da464`  
		Last Modified: Wed, 05 Jun 2024 06:12:30 GMT  
		Size: 158.5 MB (158497956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae729e2fd3d134d8c8f96e4578a3aee654eba4bb97d0d7ee8dd9838786ade610`  
		Last Modified: Wed, 05 Jun 2024 06:12:28 GMT  
		Size: 58.4 MB (58419377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ad38075136b5030c03e50c39558a6a4d87587dcf34f8846e8783758740965c`  
		Last Modified: Wed, 05 Jun 2024 06:12:27 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae955c8c4e15230535624fafed0937198a3d9c653f5e7f2f2c59fc0c84da8e9`  
		Last Modified: Wed, 05 Jun 2024 06:12:27 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:49744985092ec2acb952fe0fb8b36be1cd727a540c6bd517f16d4dea6f007fcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4926098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55236ef1937ba432b84025ccc8fd0be97f4a470f63254ba8c75b21e84299d77a`

```dockerfile
```

-	Layers:
	-	`sha256:9f4bfa93ae59696a82f9330f2c9cc7f982ebd335c6758de76b561b73ffb36039`  
		Last Modified: Wed, 05 Jun 2024 06:12:28 GMT  
		Size: 4.9 MB (4909939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42ffdb852a1ae65e8efc8efeac64070ec1bc84ad6d49371c057affd841c90027`  
		Last Modified: Wed, 05 Jun 2024 06:12:27 GMT  
		Size: 16.2 KB (16159 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:95fc889bdff271e25c322158556de6fe70c1ed10ca95d3e6eec3d2da756fa763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.3 MB (245293724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47ec96e1fd4c742a00ffeec11d3f1306870d23d69d559ccbe6ed096f0a00442b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dd15b1be93169016c018f76840cf32e20d66f24cc8d06216f46a26bc8bfaf06`  
		Last Modified: Wed, 05 Jun 2024 14:14:17 GMT  
		Size: 156.7 MB (156665602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2123dd024b5c5aff995e25b6edbaf98221ab56035b6a051bf6214cf4468ffa82`  
		Last Modified: Wed, 05 Jun 2024 14:17:58 GMT  
		Size: 58.5 MB (58540165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e3cbb2a8f28e15721df6ce83671438e27960412cfee8dfcd3437db7ed10455`  
		Last Modified: Wed, 05 Jun 2024 14:17:56 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f255df6d339d3ebb095fef7e94853fac44dd3ff3a99e50a32a75ca5ac503eb`  
		Last Modified: Wed, 05 Jun 2024 14:17:56 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f36ed9ba92abf81c64defd678b9330f9bf6fecb59491dc024fbbe6d90a1c645f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4933043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baf28197d26e1c29a31a524427b186297e9cdd486b69977c39c70974026e99b4`

```dockerfile
```

-	Layers:
	-	`sha256:8c3d93d80ef5179e561b24cb6907fc91f0217f89b4819c631c9ee7fd000aeae5`  
		Last Modified: Wed, 05 Jun 2024 14:17:57 GMT  
		Size: 4.9 MB (4916319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:968ce510ccd9e0d5f82961972d46947d4b22502e09e869f1475c2f17b202203f`  
		Last Modified: Wed, 05 Jun 2024 14:17:57 GMT  
		Size: 16.7 KB (16724 bytes)  
		MIME: application/vnd.in-toto+json
