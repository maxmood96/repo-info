## `clojure:temurin-17-bullseye`

```console
$ docker pull clojure@sha256:9210979faf902c192417ef5b47507ec4f5755d07c9715128dfbbf671bc35330b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:8dd6a413dc907537dbd068ec8a9db1e92a659c40513530ec0998824047c21df9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.8 MB (267800499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b4616417ebadfb074aef8ae47dcd1e9437e20becbd8f52a5ed0ec8cc5187db2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2d765646d883a37610a09973a079fbba4c7596e54d18d0447bdfff142389d1f7`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 53.8 MB (53754822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed96396b24255cadce6240e231e31609b7786c8502dcb580469b7f35d24c158f`  
		Last Modified: Wed, 02 Jul 2025 04:16:40 GMT  
		Size: 144.6 MB (144635025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ebc4c36018a8defbf8e5f2f52f5310e940828e4b0f52e94008856c6d52e75d`  
		Last Modified: Wed, 02 Jul 2025 04:16:39 GMT  
		Size: 69.4 MB (69409609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02e5a593723dcfdba0dfcb30ba03c104622162174856c375bd57a19286b63df`  
		Last Modified: Wed, 02 Jul 2025 11:52:04 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fca5d0b66bd0015dcad9f87ce1a4572a16c9849adbe9067789deabe0cad45f0`  
		Last Modified: Wed, 02 Jul 2025 11:52:06 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:72be7802b34cb9b8524e9e559e304cd455d9a003232444ab845eafdb0d3b34df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7411459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dae0b7b177e0752f41112825e9b0c07611c05f9deeb9d3f5fe4ee067cdadd686`

```dockerfile
```

-	Layers:
	-	`sha256:731ac9f478db0dcb8e502b30ffb28cb2ea97073de76156883a1cadad3a7532b8`  
		Last Modified: Wed, 02 Jul 2025 06:37:18 GMT  
		Size: 7.4 MB (7395638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:761e5579bb152e102e7e465bc06b52ce66e5f73dc2168c65ace9e842ac40fb81`  
		Last Modified: Wed, 02 Jul 2025 06:37:19 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a0aeb0ecfd25d407c78835fa3d572ef55b050ab98bf7a8be6daec36b308072a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.3 MB (265303831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19c314a12eb1458ef35b65f64f4f99dc8225c15b35a7d590b8037d4ae7e79e09`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:df45b4853b6fce6b81d1ac6218d861c6d7c8c14da4be409d42ee4bfdf0737e71`  
		Last Modified: Tue, 01 Jul 2025 01:15:18 GMT  
		Size: 52.3 MB (52252254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feec1691bd8435b5a7725d0efcfdcabe177c8705d157d2f53c026cbb74e59770`  
		Last Modified: Wed, 02 Jul 2025 09:22:41 GMT  
		Size: 143.5 MB (143512634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce1d596abe46bdf7808ab5fba6467595b5fe6fa20bca14c88e66e204232ac4e`  
		Last Modified: Tue, 01 Jul 2025 12:25:14 GMT  
		Size: 69.5 MB (69537902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52d4e7b8ddd5e536ac32f68cc9fbf0f1d98a609d71c8b86aaaa767cafebb7a1`  
		Last Modified: Tue, 01 Jul 2025 12:25:08 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31bbf5ff5dd77152de5823b8fa53463efdbb8b09ae5d84545b9791478c6a9822`  
		Last Modified: Tue, 01 Jul 2025 12:25:08 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:981992332c56a66b6bbf4c5a51ef068b22cf1e9aa36f8b38c54307c22b6d6f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7416676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5050a6b6ec287f68b3a78f88c14d7cf33349eea3ac694076a210cd4d3de775a`

```dockerfile
```

-	Layers:
	-	`sha256:7f668aa44f9ea58417b430916cb8521d579b9aee785982ece7c0a29559e334ab`  
		Last Modified: Tue, 01 Jul 2025 15:36:46 GMT  
		Size: 7.4 MB (7400737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58c853e63a6a2c49b130b4e007a8fcdfc469d4427eecee488dbf41948977d19a`  
		Last Modified: Tue, 01 Jul 2025 15:36:47 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json
