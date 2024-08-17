## `clojure:temurin-8-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:a7ddf92e841e9821dc7e80a202b9b21925bfd2bce19c0be30b5786d17add047e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ff590303e0f579074c3d76a4a3b733c73713b3a29191428d3814495ff46397fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.8 MB (201762686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c1c755d7b5f8d00b282cbafab5071ccb96ea5b1d498e8ed321acacec837f5f`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09becbbc3867dd12d232497598d9246fb4daadaf2ccc7f3f65ad6fc52615d5d`  
		Last Modified: Sat, 17 Aug 2024 01:59:20 GMT  
		Size: 103.6 MB (103611903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca748980600cf6074d3b106ff7fbbee26b08d9a11fafad75cd79135b52c6862`  
		Last Modified: Sat, 17 Aug 2024 01:59:20 GMT  
		Size: 69.0 MB (69023906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba3b409b7b06173f727eb324a7cea64c7c9dee7f7abfbf2a8dd6297e9ebe4ba`  
		Last Modified: Sat, 17 Aug 2024 01:59:19 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:de2f1c49f46c130ffa35da42cd2598cefc9840f20ecddb356e3c2b7e79ec680f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4784576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:962e9580ab70b43ceda899b2b90b5659745aa8da846d40be856fe928c6b1abb6`

```dockerfile
```

-	Layers:
	-	`sha256:da8d44e44903214a625ff813dc3765bcd7ce2a0349b20aad7ac1efec4fa86e56`  
		Last Modified: Sat, 17 Aug 2024 01:59:19 GMT  
		Size: 4.8 MB (4770655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:feb22b38841423b0753dd713ff5fa7f658479a306b5037aa53cfa255af59e772`  
		Last Modified: Sat, 17 Aug 2024 01:59:19 GMT  
		Size: 13.9 KB (13921 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ea697214feffadcafa9b21a3687d198729eee40740827f1f1e7fc4fd0a1a9657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.7 MB (200659249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6debbb9706e90788023e1afe2b4084ddc26e47b122b731a2790a62c00e34240`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5edcc7a7af68400eeaf570c17969676510119f264dd0e3c2e9727f01574ef515`  
		Last Modified: Sat, 17 Aug 2024 05:51:40 GMT  
		Size: 102.7 MB (102729220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3bead7a57dc0e19cb89ede2dd23bc3f99e00d3fdbc8029756ebeee42c77f26`  
		Last Modified: Sat, 17 Aug 2024 05:57:09 GMT  
		Size: 68.8 MB (68772855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac1d1084a3b9e944e3c1e469cf4fe436f24386887b751d633fc3514f45719e2`  
		Last Modified: Sat, 17 Aug 2024 05:57:05 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:72413b5970d07692c387b31c9538dce29d3178434a7e4ad1f7774570451e3f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4791501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdcb4111f705b049e43f20982b20d9b9d7f8905ce92d54a58f7bcfc3c15a0ead`

```dockerfile
```

-	Layers:
	-	`sha256:f2f105d58461c115639871d7e0c727bd3845e47879c9d9799d1f086dc0bde687`  
		Last Modified: Sat, 17 Aug 2024 05:57:05 GMT  
		Size: 4.8 MB (4777040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf8d9775cd6af56e737b41f664cec5b8fc52f1f359417487ec781f5da63363d5`  
		Last Modified: Sat, 17 Aug 2024 05:57:05 GMT  
		Size: 14.5 KB (14461 bytes)  
		MIME: application/vnd.in-toto+json
