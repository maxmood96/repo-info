## `clojure:temurin-22-bookworm-slim`

```console
$ docker pull clojure@sha256:21f7ae6558223828dc3fa29422106a0d5f0189ea8b189e33ca4ee9e506a2a898
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2b732b69f4dbc085cba587730aa77bce39fb707dd67f4079d557a45ec3a86f74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.7 MB (254676353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0ef2c5061e4501f64ba5f48c434394e77b5d2b8e6d37960aaced41ff7c8bbba`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 20 Jul 2024 21:06:39 GMT
ADD file:6c4730e7b12278bc7eb83b3b9d659437c92c42fc7ee70922ae8c4bebfb56a602 in / 
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["bash"]
# Sat, 20 Jul 2024 21:06:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 20 Jul 2024 21:06:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Jul 2024 21:06:39 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Sat, 20 Jul 2024 21:06:39 GMT
WORKDIR /tmp
# Sat, 20 Jul 2024 21:06:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:efc2b5ad9eec05befa54239d53feeae3569ccbef689aa5e5dbfc25da6c4df559`  
		Last Modified: Tue, 23 Jul 2024 05:27:55 GMT  
		Size: 29.1 MB (29126287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fd20a38cd0f8643a9006db93a1d58f6aa3f9804f3faaa305160c02ecb8a7da`  
		Last Modified: Thu, 25 Jul 2024 19:05:27 GMT  
		Size: 156.5 MB (156481615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6edfe65999fb902c63b2784c0b21eeab71fbbc9904e6a9a59cd99bba805daeaa`  
		Last Modified: Thu, 25 Jul 2024 19:05:26 GMT  
		Size: 69.1 MB (69067408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23b56d8d21399e42ab7f99d116ccd05d3d0b9bf0b22d6dd6d4ebe7d1bf8da9e`  
		Last Modified: Thu, 25 Jul 2024 19:05:25 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88613fec4ef2d0cffe1cbc5549e876645b0244f7e9c6107f67dbbe92bdae4eb`  
		Last Modified: Thu, 25 Jul 2024 19:05:25 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:000cfa62c8e0451bd408e0233590dda3d8bc6e92a6d75a619ebccbb56ee43e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4760671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ec3f2c4ab373e49139f50a748db3cf2268038e9f37505c3883fced4e140673f`

```dockerfile
```

-	Layers:
	-	`sha256:9655dcf6a0d9596cdb76bd3e2cee46aaba8ea381632796dbb54bd20aceb0065a`  
		Last Modified: Thu, 25 Jul 2024 19:05:25 GMT  
		Size: 4.7 MB (4745158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f665633e6381c07b6afe4c14c210af717c2356c6f10d878b2fe9488ffd6ad188`  
		Last Modified: Thu, 25 Jul 2024 19:05:25 GMT  
		Size: 15.5 KB (15513 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8e10b9008594bebc85c651471a3ad0002bbeede98c6658deef4ca74d2330080c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.5 MB (252479400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aa4ec792159520ce2a89d9e5b4baba690b2e8ba9469ef5ccd8cec3c3947772b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 20 Jul 2024 21:06:39 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["bash"]
# Sat, 20 Jul 2024 21:06:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 20 Jul 2024 21:06:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Jul 2024 21:06:39 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Sat, 20 Jul 2024 21:06:39 GMT
WORKDIR /tmp
# Sat, 20 Jul 2024 21:06:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44131b313aa4d7bad1771ecbd24677b9132ac2fed12d8437cc1fc2bcb0c40e98`  
		Last Modified: Wed, 24 Jul 2024 11:37:09 GMT  
		Size: 154.5 MB (154503755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6add89073d9278825dd37db7a85e294d32222b523df4ca95518c69ce8bd5f7`  
		Last Modified: Wed, 24 Jul 2024 11:41:40 GMT  
		Size: 68.8 MB (68818032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97deb0917c97aa41047741bd9e5cf44bc60772683f48d21bfb55a8a03a45ffb`  
		Last Modified: Wed, 24 Jul 2024 11:41:37 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1927f0bf3e5de3d538e47c8d48ff2ca01cda4a519777c3c88c15badb0f40f36b`  
		Last Modified: Wed, 24 Jul 2024 11:41:37 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ee91a86370e849c2c09875184b26f4a656ba57fa60b2d51ee0c3ecb30e07dcbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4766766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a15ba1282f4941efb386851eaec4c5d31a0c9faee666e96fb6e243da215306ea`

```dockerfile
```

-	Layers:
	-	`sha256:109ff53bd16f75303e3bf9c0d58e97a4c209b0b4ef3efef281119b762a0d0271`  
		Last Modified: Wed, 24 Jul 2024 11:41:37 GMT  
		Size: 4.8 MB (4751543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c74a7c75f20fc67e70b8a4d832d147ffcdbae97a63cf994e0a787f5d89ab107`  
		Last Modified: Wed, 24 Jul 2024 11:41:37 GMT  
		Size: 15.2 KB (15223 bytes)  
		MIME: application/vnd.in-toto+json
