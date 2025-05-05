## `clojure:temurin-17-bookworm`

```console
$ docker pull clojure@sha256:197e1936b55dea01b613c086ad8d078aefd10313a7e4670e5d3630757ceb6797
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:25f26f6235494593c940cc3e7695892681d27eb35d8f4c683a9d24a1ec51ad87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.1 MB (274118895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a007ceb562ef8a14c6bc5861cbf8c489cb839e123e134de6d5e7ee81c08d177`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811142764e4bd248dcb91193058d25b9278e8999f35cf511e3d3c2c20698faea`  
		Last Modified: Mon, 05 May 2025 17:07:32 GMT  
		Size: 144.6 MB (144635028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2c1defc4b0e23204341791be94a4b38a4dc8160e02b8444dd244d1ed7fb998`  
		Last Modified: Mon, 05 May 2025 17:07:31 GMT  
		Size: 81.0 MB (80991630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f981e63eadae807769b591d0fce420d8c1f5d5f21839a55544e89d74b754b769`  
		Last Modified: Mon, 05 May 2025 17:07:29 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a54d1c8d92f6f2129d25c5d43433496ef8506963be38c2aa49f76c2e066698`  
		Last Modified: Mon, 05 May 2025 17:07:29 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:7857262a36751343dc525c1eea7bfd267791c6eb79ab233a4ab378092bc4d5a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7188297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247785eeb212ae6a6cbe36e8cae45263676e7aabf59d9e30844dfc3fe6cffabb`

```dockerfile
```

-	Layers:
	-	`sha256:8f5ac1290cc1473579050be0ea47a5b321c4299c3307dfba12cf0607bdf9f38e`  
		Last Modified: Mon, 05 May 2025 17:07:29 GMT  
		Size: 7.2 MB (7172476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4e43d8c851ed532da4e3cf3314a4367c3bef167669a90f06c8f23d4343b3c02`  
		Last Modified: Mon, 05 May 2025 17:07:29 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b6be808140216d8235587db891f48a9804fe49ce112c27723d52c29df77e7ad7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.7 MB (272685334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49b148a573cb3d7caacdea998afa727fb667373f181017c1423d5cb3b0d6aad4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:de07ba6f486e0ce29760ab32d4381edabbc660a04c493e95eb9a8056925d8955`  
		Last Modified: Mon, 28 Apr 2025 21:20:23 GMT  
		Size: 48.3 MB (48327644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2cd361a781d708545f3868f3508f83147c1502bb5b628076be9993af2ddee0`  
		Last Modified: Wed, 30 Apr 2025 01:22:45 GMT  
		Size: 143.5 MB (143512607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3bc01aaa1de3d3ca363862cc23e91211be40e2c8b68251b4da6f34eb11e28f`  
		Last Modified: Wed, 30 Apr 2025 01:33:38 GMT  
		Size: 80.8 MB (80844042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b20c3ea7c531789b835ea992a91dfd51069418c4f4242249e30d2def7b82f3`  
		Last Modified: Wed, 30 Apr 2025 01:33:36 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47caaf807b8d52fe845bd400ffebfce77bfbc8839589499ff17586023ff9e3b0`  
		Last Modified: Wed, 30 Apr 2025 01:33:36 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:daf24a8c48122c44159e1a0d8962164dcd000f8cc54a0862b04c17f7521b6af6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7194178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9961447240bc9a0ee457c627621f42dbf0e0e032f52efed722023b23503d3312`

```dockerfile
```

-	Layers:
	-	`sha256:37226f35d88ddc69878a295644a30f72c99911d56e401d94b89c275ab6c4d64a`  
		Last Modified: Wed, 30 Apr 2025 01:33:36 GMT  
		Size: 7.2 MB (7178239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b132a48f19e8b53ce472507a7228e87aa76309f6d980fc124e1f6f627cc0d987`  
		Last Modified: Wed, 30 Apr 2025 01:33:36 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json
