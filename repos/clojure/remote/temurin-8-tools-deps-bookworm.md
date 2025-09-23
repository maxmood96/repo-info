## `clojure:temurin-8-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:6c94e32b1b3ceba7bf60f62fab6a85466cfb2871a7dccf0b3afa0e11eb77200e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:9834f298c4e68c93a499975fd8209e9afb4f7461c6b90316f67b9a171d952952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.4 MB (184353386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbf5b179016b9b848144fd622080bbb91b149d35448d5eb79ba2ec65e8f8df3c`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15502c0c6a5949eef1fc5fb7e3c26ce82a3a89a547a417ee1c43064bc6ed6d32`  
		Last Modified: Mon, 22 Sep 2025 23:44:27 GMT  
		Size: 54.7 MB (54731322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8087923b8d77b9f003fef24a027950d6fcf8a5c591b0aa8fab8e515c697054`  
		Last Modified: Mon, 22 Sep 2025 23:44:06 GMT  
		Size: 81.1 MB (81140807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e7d40a2bba2b3be88a46f5ef4d0ebb9e4d9bc634f91ce0c18775fd3e06b2f0`  
		Last Modified: Mon, 22 Sep 2025 23:43:57 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:5409124aaba39bde76014360a8effe3da8418fc6b02c44952b93b4ed004e0cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7510736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a722b6aa44f5f558acb598bc21c86211f1637dc10daafd597ebd6de8b7a8c0c`

```dockerfile
```

-	Layers:
	-	`sha256:a822790750aa8036992a753c1ce88d9e4a66bf0ccbcccd0d445d267ef09483f5`  
		Last Modified: Tue, 23 Sep 2025 00:46:25 GMT  
		Size: 7.5 MB (7496500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33fe9b8adcdcf870cef38215d871fc974bbabcc5bb6dcf9fe02e3fff597524a9`  
		Last Modified: Tue, 23 Sep 2025 00:46:26 GMT  
		Size: 14.2 KB (14236 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e2b0621dab755bafb7f290d99784ead84894503a8f7542696814389599d0a2eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.2 MB (183226490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0457a58f571ebc64d1e022e26f7fc5953b06b46d3df552c080a616013fe23c40`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de456fb2b813861039cc6da35bf3a9ede4a2375f3af038fd4526fa1edc591c6`  
		Last Modified: Mon, 22 Sep 2025 22:15:14 GMT  
		Size: 53.8 MB (53835655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6194596d5f393e8eace2d8c39bff76cb4afbd80438e32d51d09bcac4213fe21b`  
		Last Modified: Mon, 22 Sep 2025 22:15:16 GMT  
		Size: 81.0 MB (81031170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a5d77cad4a9c64ebd3eefd2c031ce1733e353c416e29d3898a269a4e67b4a4`  
		Last Modified: Mon, 22 Sep 2025 22:15:10 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:cd103834bddb3b2017157a5f6fbe845727532e3ca7d89488f159fcbc1132663d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7517316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbb2d08667eb2e3191c24993a5748f523d78be04c22e522e9c7d3b76023574b2`

```dockerfile
```

-	Layers:
	-	`sha256:b3dff1c1450d5ac050f971f8476026bc88e36728672dcd291845ee6ff747172f`  
		Last Modified: Tue, 23 Sep 2025 00:46:33 GMT  
		Size: 7.5 MB (7502961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:338e151c5de415f96598f7192cabf838473e1853cb4ca693777fe3f576ad0cfb`  
		Last Modified: Tue, 23 Sep 2025 00:46:34 GMT  
		Size: 14.4 KB (14355 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:c67202efeab0123ad504a2e10d83e95623c06cc3918b663ed93569d3fe1b81f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191476343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8eed573277d3923f0f13bf581f77cecd045252c06070f68b273e9c8f65f0f57`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:64b8116dd43c29a2a4aa3131cb4895af0a7267cc5883e3761556e54c369be9af`  
		Last Modified: Mon, 08 Sep 2025 21:22:08 GMT  
		Size: 52.3 MB (52326822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c92186a59edc4b8d6ddab20d89d6a51750d2caa0b76e9bfef225d72a96b0823`  
		Last Modified: Fri, 12 Sep 2025 23:42:43 GMT  
		Size: 52.2 MB (52165437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170e1dbf8b6453c533169c56c7f6c5c0c84fe56664581c3dc73eb99e3875879f`  
		Last Modified: Mon, 22 Sep 2025 22:35:11 GMT  
		Size: 87.0 MB (86983437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89dae51d3537419a80b6d0dda8abbb52a104f9da6dc5f187df59e352230062c4`  
		Last Modified: Mon, 22 Sep 2025 22:35:03 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:7326c115853b7f3ca621b483d3cef3898cf6c62ea54a4ac346ec81412aadedf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7516592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa4dd855263ac05a8f437417f06986c25f0cac0bb584f622a8ac17682e70e44`

```dockerfile
```

-	Layers:
	-	`sha256:b1f316d1876ec27bdd33e1d0a8f5d50588f8417d0b3ba632a227d7106e730a8b`  
		Last Modified: Tue, 23 Sep 2025 00:46:40 GMT  
		Size: 7.5 MB (7502307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:206297c907391fa176e1a5a1bc97a5f9c1a6d8c6c6a53ffe1a11e99b4efd7e06`  
		Last Modified: Tue, 23 Sep 2025 00:46:41 GMT  
		Size: 14.3 KB (14285 bytes)  
		MIME: application/vnd.in-toto+json
