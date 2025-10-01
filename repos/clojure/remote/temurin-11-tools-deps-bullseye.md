## `clojure:temurin-11-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:f75ba0e2cd01026db52c526608abd18b9562c3f9ebeecedf01a1752061577f2d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:467b21062e1e495c6f58c961b68250e90147e87b5f14b2424b7c2cc426f69b6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268974690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7f915e5761d0e97c365bdfdc3120c438745ede6b7f35ac5b703b616827421fd`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:10ffc47270cd106d2d04bc7ef4749d579620e45a84804ba3b18f0898fe5ecc64`  
		Last Modified: Mon, 29 Sep 2025 23:35:07 GMT  
		Size: 53.8 MB (53756064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c95dccd09a097f11bc9c7cd183a6e0f3e04340d2c9132646610471084e2a1b7`  
		Last Modified: Tue, 30 Sep 2025 00:51:51 GMT  
		Size: 145.7 MB (145658240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ea1c3e827e88c65f798b9ebdcf53571382ecb2f62455d4bce858ac017f80b6`  
		Last Modified: Tue, 30 Sep 2025 00:53:14 GMT  
		Size: 69.6 MB (69559742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552f7c20a6af0c84570a402f1448e7ab0b5db24d02ead480281a4a835686a23a`  
		Last Modified: Tue, 30 Sep 2025 00:53:05 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:851d49d021c3e244d2703d972bb325e3d2cb19ed4167559df9c37fda48eed3be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7429259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:517ea4df42111331d39ce6f67b089f0e52f3e8da9cccca7a301d96e09e54e22f`

```dockerfile
```

-	Layers:
	-	`sha256:10607c3cad232527f8ad4d322a507bd10e7d63a7375afb5899663a7322509975`  
		Last Modified: Wed, 01 Oct 2025 15:35:26 GMT  
		Size: 7.4 MB (7415808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fc099a8a17135d1abb47e19a831eecfa3dc1192365cb4fc20c80fb1d0693d1f`  
		Last Modified: Wed, 01 Oct 2025 15:35:27 GMT  
		Size: 13.5 KB (13451 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4b40f81c3504c28aacf7dc4038dbc5a01a6623e244e2b312fa7078f30cc7bbcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.4 MB (264404441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a5901ac60affbba768762abf50650fc859ac5913a732715476af4bd35a50d2d`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9b16ae1bbd1ada84c12528379a10e280bd89e0d0332670c8487145eb77fe2fe1`  
		Last Modified: Mon, 29 Sep 2025 23:34:42 GMT  
		Size: 52.3 MB (52257414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c2cd9bb833d98006aa080ec0506032b4bb9387a695f1fbcd510217495668e9`  
		Last Modified: Tue, 30 Sep 2025 00:51:36 GMT  
		Size: 142.5 MB (142458731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1d578b9a3f2991f468ac1a2c96b4a975e66d07d01529d7eff1d57aee483995`  
		Last Modified: Tue, 30 Sep 2025 00:52:19 GMT  
		Size: 69.7 MB (69687653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f798fc2af011f4b286fdd149d3ca7956c52376000bfd7bf39f511c4b73b123`  
		Last Modified: Tue, 30 Sep 2025 00:52:14 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:aa2931cdb6a158eb1eb43033ce11e27be2a1a557116d3fba682102e12a56cebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7435895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b88d265ed716a50111e3662ceb631d143c4fd41dee586f10000f78c4f1cad69`

```dockerfile
```

-	Layers:
	-	`sha256:6435ae2d0d7681d25e1785d22f3a8fd42bc9bac4a340d3e1665651439c4744e8`  
		Last Modified: Wed, 01 Oct 2025 21:36:15 GMT  
		Size: 7.4 MB (7421525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71f21a267cf414ea20732b5ee399d05268b5d0c701367f697365e223ae3e11e5`  
		Last Modified: Wed, 01 Oct 2025 21:36:17 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json
