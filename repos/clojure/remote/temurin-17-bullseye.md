## `clojure:temurin-17-bullseye`

```console
$ docker pull clojure@sha256:8f6097d6ceef81638b44805ccd56d59a8ea22904532225e22591626c51574b75
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:b15c6de786beecf68947bf28581ccb8856081cb4f7bb46530b35c34a1881a324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.2 MB (268166374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ee7b3df913532be28f98f833fe69b5e42be8a0b2c20795956183891463ee28`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:53:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:53:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:53:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:53:29 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 23:53:29 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:53:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 08 Dec 2025 23:53:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 08 Dec 2025 23:53:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 08 Dec 2025 23:53:42 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 08 Dec 2025 23:53:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:437b5b60e3a4b64e2c621589a67483eeef6d4b3fc4926655006ef41bd44f71dd`  
		Last Modified: Mon, 08 Dec 2025 22:16:49 GMT  
		Size: 53.8 MB (53756413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28cd9914bc94999db70b3696473054ca5a0916eafe5b95f250635e4a6d66331d`  
		Last Modified: Mon, 08 Dec 2025 23:54:38 GMT  
		Size: 144.8 MB (144847948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8b076f19945efc96a2b13259c555c44cb459360bf2b7592db2c53ba91a2bcf`  
		Last Modified: Mon, 08 Dec 2025 23:54:16 GMT  
		Size: 69.6 MB (69560970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933e3448e0ba67d32a7c1b39515555ae1d220881563726f2930b9ec889d51377`  
		Last Modified: Mon, 08 Dec 2025 23:54:11 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945a9ff2be1c4309b5d0cf3d635e4e883982f780d63a583e7d72dc2c8f1002e3`  
		Last Modified: Mon, 08 Dec 2025 23:54:11 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:78e67e723e4ac40571699134f7bf388b3758887848cbd5127e7586b5dde64531
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7411446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7004757ffac698b50bf5f0c5adc954205a04d0b5ab0ef0a17f78aeae1e261673`

```dockerfile
```

-	Layers:
	-	`sha256:0e89566cf04bde91e02e80fe4626a14e2f3b3e85fa2d0a06bd4238b9288d7b06`  
		Last Modified: Tue, 09 Dec 2025 04:39:18 GMT  
		Size: 7.4 MB (7395669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9394de2070a2846aa69980fceaf936d54dd9c4c34c9d8c52df442bcd3d9f5db3`  
		Last Modified: Tue, 09 Dec 2025 04:39:19 GMT  
		Size: 15.8 KB (15777 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ed8e0a37d490b9048e628d254b989c8d12e72b20a1f8e1dcf08f0bc054d0ddf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.6 MB (265626844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57052f3ac43138063921907f8b4a1ac1729bbabbea38b3197ab82c2ab807d216`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1765152000'
# Tue, 09 Dec 2025 00:01:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 00:01:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 00:01:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 00:01:18 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 09 Dec 2025 00:01:18 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 00:01:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 09 Dec 2025 00:01:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 09 Dec 2025 00:01:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 00:01:32 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 00:01:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:24bca79f74a34f86894c8fcdc6ce8d7dc3c11dd0c76b7e9fa80c7c64df65d166`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 52.3 MB (52257713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02cae8fe60f4430c9d322abf44551ff661105f999531466c85ff4254c85a89e9`  
		Last Modified: Tue, 09 Dec 2025 02:47:22 GMT  
		Size: 143.7 MB (143679920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96f81e7eb11db4b63b56e7adc7b345941bad049bcc619bccbfdae8b6969442a`  
		Last Modified: Tue, 09 Dec 2025 00:02:15 GMT  
		Size: 69.7 MB (69688170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b20fca0f484874236228b2e35d2ef297eea0815ce971aa0ae341ac0a05bc0b5`  
		Last Modified: Tue, 09 Dec 2025 00:02:02 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b150a4ed23ecb5c288e068cbefb3bcb3fcbaa2c770498c70232673eb48f5e730`  
		Last Modified: Tue, 09 Dec 2025 00:02:02 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3dc4463740a7eea5940e0aff00c9e6a8c485d4a2325d8dcac42aae7b4bf80cab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7416664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca2cd00b3053952d6844397e17a36035a72d86bc81695c299075ad98b02ce66b`

```dockerfile
```

-	Layers:
	-	`sha256:943c0770efb94ae7a82b3e73559288b8c4cb076eae7c4238ed4148ba36924f49`  
		Last Modified: Tue, 09 Dec 2025 04:39:26 GMT  
		Size: 7.4 MB (7400768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6de7d825559124f2e97b0f4f174b0a8764d17d58b284cb6b7f91bd6524f40caa`  
		Last Modified: Tue, 09 Dec 2025 04:39:27 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json
