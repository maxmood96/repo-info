<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rethinkdb`

-	[`rethinkdb:2`](#rethinkdb2)
-	[`rethinkdb:2-bookworm-slim`](#rethinkdb2-bookworm-slim)
-	[`rethinkdb:2.4`](#rethinkdb24)
-	[`rethinkdb:2.4-bookworm-slim`](#rethinkdb24-bookworm-slim)
-	[`rethinkdb:2.4.3`](#rethinkdb243)
-	[`rethinkdb:2.4.4-bookworm-slim`](#rethinkdb244-bookworm-slim)
-	[`rethinkdb:bookworm-slim`](#rethinkdbbookworm-slim)
-	[`rethinkdb:latest`](#rethinkdblatest)

## `rethinkdb:2`

```console
$ docker pull rethinkdb@sha256:bd052c2ca98d731e2b3e794f795ef1e24dec762108ce9734c5c19a56b73fa71a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rethinkdb:2` - linux; amd64

```console
$ docker pull rethinkdb@sha256:9a346c1b472d23752c3c75d25871b136052c84f5a0be54e11e555ac7d2662f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48031604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e19cb11eb2b02233f790d7cda93df1a6e95d1be1d5151ed397e7e887c9f583`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:35:56 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:35:57 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 16 Mar 2026 22:36:03 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 16 Mar 2026 22:36:03 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:36:03 GMT
VOLUME [/data]
# Mon, 16 Mar 2026 22:36:03 GMT
WORKDIR /data
# Mon, 16 Mar 2026 22:36:03 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 16 Mar 2026 22:36:03 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71704a3d3c7df105339617c2524cd0afb35d61ba643e31020adce407ac94d3de`  
		Last Modified: Mon, 16 Mar 2026 22:36:10 GMT  
		Size: 9.8 MB (9799396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2f94d16318afed5ecbb41d245aeaf836f2589faee765f3b6eea080831b8c1c`  
		Last Modified: Mon, 16 Mar 2026 22:36:10 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d9a0f54967e418507c12b24e9c37df0945177f9d80365f3c30b51dc8f6b6d6`  
		Last Modified: Mon, 16 Mar 2026 22:36:10 GMT  
		Size: 10.0 MB (9993221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2813767849ffed6060dbc015c616d93cf3dd9257b2dbca8535d52883e241cbf5`  
		Last Modified: Mon, 16 Mar 2026 22:36:10 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:fed881594fa2dc6a9c12da83a55e08779901151967d0acac544de78404407706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d9249e3d4f2a6023200ba79111a259b129a7d7881489a5f1919aa630c004bda`

```dockerfile
```

-	Layers:
	-	`sha256:1055d74f2a23f211107760f46673956a73f2806b372be64e267d1e69033f463d`  
		Last Modified: Mon, 16 Mar 2026 22:36:10 GMT  
		Size: 2.8 MB (2785046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a3b0dc6d885aa7907efd83e9d39e8aea97cbba5425ddebd8a7d0f8b208994e7`  
		Last Modified: Mon, 16 Mar 2026 22:36:10 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:eb5fa1f28212eb74ac40e4b41813690ddee9cb0631aeaf0dbaf112fe6d0e55fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47110147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc0dbf509a7be68a33e0fa5ac93b1604e87cfa0e1d5e97248fda3130f3cc14d`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:38:23 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:38:24 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 16 Mar 2026 22:38:29 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 16 Mar 2026 22:38:29 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:38:29 GMT
VOLUME [/data]
# Mon, 16 Mar 2026 22:38:29 GMT
WORKDIR /data
# Mon, 16 Mar 2026 22:38:29 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 16 Mar 2026 22:38:29 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:addc91a63479667884ce4f98cede66ac22fb9f4c00a54e6e037934325e1e6866`  
		Last Modified: Mon, 16 Mar 2026 22:38:36 GMT  
		Size: 9.6 MB (9628365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49afdf53e977087b916ed3869884b20c70ef5a0b0c740acc56b520525ceafdc9`  
		Last Modified: Mon, 16 Mar 2026 22:38:36 GMT  
		Size: 2.7 KB (2665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab2218262d3fce9640555b0728347b9b7b42e9058775fe8b237ca6f5851ab3a`  
		Last Modified: Mon, 16 Mar 2026 22:38:36 GMT  
		Size: 9.4 MB (9362959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d06ec3cd0cae998ad5994e2e6735bb051f5ca642c28bd1188f28a9902ed5ed20`  
		Last Modified: Mon, 16 Mar 2026 22:38:36 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:0294022552661a2bd8c3419bdfdf0e94c6c0af694168d7cdd12b52b3ce23a423
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e23178f8bea118419f36bf3579df653a032c7659f42766e141ad4e8d37fee76`

```dockerfile
```

-	Layers:
	-	`sha256:ffa03f3f0afd31eea7975eaacf743c3e0ab752b34d5e27854d0c2a3ca950b5d8`  
		Last Modified: Mon, 16 Mar 2026 22:38:36 GMT  
		Size: 2.8 MB (2785381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f87d57613fbff19f9f1b17891bd210539f6bdf95225bc85b68eca7761d7d92b6`  
		Last Modified: Mon, 16 Mar 2026 22:38:36 GMT  
		Size: 13.6 KB (13586 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2` - linux; s390x

```console
$ docker pull rethinkdb@sha256:5bdc081839b933b512e25d8c3acadfa2c20abfb1882ebd7d9a594350286aa7dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45495577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:353e6c471e19b5f3ccadb080b9aebb478b172302e956477e809d3cb8d303d1e0`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:42:55 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:42:57 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 16 Mar 2026 23:43:02 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 16 Mar 2026 23:43:02 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:43:02 GMT
VOLUME [/data]
# Mon, 16 Mar 2026 23:43:02 GMT
WORKDIR /data
# Mon, 16 Mar 2026 23:43:02 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 16 Mar 2026 23:43:02 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ae76cc96a4cba2739c8be0ce73e62f473c5a663eeb015b4cf60dda4895e88b`  
		Last Modified: Mon, 16 Mar 2026 23:43:19 GMT  
		Size: 9.3 MB (9297538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60e6fb7614b82d95c2c421fae589438a70eca69a9742211c7f70e8fa55d8bb5`  
		Last Modified: Mon, 16 Mar 2026 23:43:17 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3a1969febccd2d1846984311e6ac35eeaaeb64cdef9c24b8be97c093aaa4c8`  
		Last Modified: Mon, 16 Mar 2026 23:43:18 GMT  
		Size: 9.3 MB (9303762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730395b6605549628d7228a8fe89cd74d7fb18301b1ebad6d739425bde78aa86`  
		Last Modified: Mon, 16 Mar 2026 23:43:17 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:4d12fb1620d8ac8e82daca4df71ea2037f3e3fd8fd50efef793541311e85a319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2794652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78bc4d832486dc105b9b5e33841a8415a0bc562bb401a559e11e5cb2792bf568`

```dockerfile
```

-	Layers:
	-	`sha256:4ba1f101408adaa8602261d8d8f827abe5557ae92aaa639d8f4554ebda3c904b`  
		Last Modified: Mon, 16 Mar 2026 23:43:17 GMT  
		Size: 2.8 MB (2781248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7469dca3f1d192339e3e8d77677a7da5436b8a7ca780fd02b55c4f52d5ed9bea`  
		Last Modified: Mon, 16 Mar 2026 23:43:17 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:2-bookworm-slim`

```console
$ docker pull rethinkdb@sha256:bd052c2ca98d731e2b3e794f795ef1e24dec762108ce9734c5c19a56b73fa71a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rethinkdb:2-bookworm-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:9a346c1b472d23752c3c75d25871b136052c84f5a0be54e11e555ac7d2662f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48031604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e19cb11eb2b02233f790d7cda93df1a6e95d1be1d5151ed397e7e887c9f583`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:35:56 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:35:57 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 16 Mar 2026 22:36:03 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 16 Mar 2026 22:36:03 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:36:03 GMT
VOLUME [/data]
# Mon, 16 Mar 2026 22:36:03 GMT
WORKDIR /data
# Mon, 16 Mar 2026 22:36:03 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 16 Mar 2026 22:36:03 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71704a3d3c7df105339617c2524cd0afb35d61ba643e31020adce407ac94d3de`  
		Last Modified: Mon, 16 Mar 2026 22:36:10 GMT  
		Size: 9.8 MB (9799396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2f94d16318afed5ecbb41d245aeaf836f2589faee765f3b6eea080831b8c1c`  
		Last Modified: Mon, 16 Mar 2026 22:36:10 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d9a0f54967e418507c12b24e9c37df0945177f9d80365f3c30b51dc8f6b6d6`  
		Last Modified: Mon, 16 Mar 2026 22:36:10 GMT  
		Size: 10.0 MB (9993221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2813767849ffed6060dbc015c616d93cf3dd9257b2dbca8535d52883e241cbf5`  
		Last Modified: Mon, 16 Mar 2026 22:36:10 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:fed881594fa2dc6a9c12da83a55e08779901151967d0acac544de78404407706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d9249e3d4f2a6023200ba79111a259b129a7d7881489a5f1919aa630c004bda`

```dockerfile
```

-	Layers:
	-	`sha256:1055d74f2a23f211107760f46673956a73f2806b372be64e267d1e69033f463d`  
		Last Modified: Mon, 16 Mar 2026 22:36:10 GMT  
		Size: 2.8 MB (2785046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a3b0dc6d885aa7907efd83e9d39e8aea97cbba5425ddebd8a7d0f8b208994e7`  
		Last Modified: Mon, 16 Mar 2026 22:36:10 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:eb5fa1f28212eb74ac40e4b41813690ddee9cb0631aeaf0dbaf112fe6d0e55fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47110147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc0dbf509a7be68a33e0fa5ac93b1604e87cfa0e1d5e97248fda3130f3cc14d`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:38:23 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:38:24 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 16 Mar 2026 22:38:29 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 16 Mar 2026 22:38:29 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:38:29 GMT
VOLUME [/data]
# Mon, 16 Mar 2026 22:38:29 GMT
WORKDIR /data
# Mon, 16 Mar 2026 22:38:29 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 16 Mar 2026 22:38:29 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:addc91a63479667884ce4f98cede66ac22fb9f4c00a54e6e037934325e1e6866`  
		Last Modified: Mon, 16 Mar 2026 22:38:36 GMT  
		Size: 9.6 MB (9628365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49afdf53e977087b916ed3869884b20c70ef5a0b0c740acc56b520525ceafdc9`  
		Last Modified: Mon, 16 Mar 2026 22:38:36 GMT  
		Size: 2.7 KB (2665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab2218262d3fce9640555b0728347b9b7b42e9058775fe8b237ca6f5851ab3a`  
		Last Modified: Mon, 16 Mar 2026 22:38:36 GMT  
		Size: 9.4 MB (9362959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d06ec3cd0cae998ad5994e2e6735bb051f5ca642c28bd1188f28a9902ed5ed20`  
		Last Modified: Mon, 16 Mar 2026 22:38:36 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:0294022552661a2bd8c3419bdfdf0e94c6c0af694168d7cdd12b52b3ce23a423
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e23178f8bea118419f36bf3579df653a032c7659f42766e141ad4e8d37fee76`

```dockerfile
```

-	Layers:
	-	`sha256:ffa03f3f0afd31eea7975eaacf743c3e0ab752b34d5e27854d0c2a3ca950b5d8`  
		Last Modified: Mon, 16 Mar 2026 22:38:36 GMT  
		Size: 2.8 MB (2785381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f87d57613fbff19f9f1b17891bd210539f6bdf95225bc85b68eca7761d7d92b6`  
		Last Modified: Mon, 16 Mar 2026 22:38:36 GMT  
		Size: 13.6 KB (13586 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2-bookworm-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:5bdc081839b933b512e25d8c3acadfa2c20abfb1882ebd7d9a594350286aa7dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45495577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:353e6c471e19b5f3ccadb080b9aebb478b172302e956477e809d3cb8d303d1e0`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:42:55 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:42:57 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 16 Mar 2026 23:43:02 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 16 Mar 2026 23:43:02 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:43:02 GMT
VOLUME [/data]
# Mon, 16 Mar 2026 23:43:02 GMT
WORKDIR /data
# Mon, 16 Mar 2026 23:43:02 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 16 Mar 2026 23:43:02 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ae76cc96a4cba2739c8be0ce73e62f473c5a663eeb015b4cf60dda4895e88b`  
		Last Modified: Mon, 16 Mar 2026 23:43:19 GMT  
		Size: 9.3 MB (9297538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60e6fb7614b82d95c2c421fae589438a70eca69a9742211c7f70e8fa55d8bb5`  
		Last Modified: Mon, 16 Mar 2026 23:43:17 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3a1969febccd2d1846984311e6ac35eeaaeb64cdef9c24b8be97c093aaa4c8`  
		Last Modified: Mon, 16 Mar 2026 23:43:18 GMT  
		Size: 9.3 MB (9303762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730395b6605549628d7228a8fe89cd74d7fb18301b1ebad6d739425bde78aa86`  
		Last Modified: Mon, 16 Mar 2026 23:43:17 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:4d12fb1620d8ac8e82daca4df71ea2037f3e3fd8fd50efef793541311e85a319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2794652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78bc4d832486dc105b9b5e33841a8415a0bc562bb401a559e11e5cb2792bf568`

```dockerfile
```

-	Layers:
	-	`sha256:4ba1f101408adaa8602261d8d8f827abe5557ae92aaa639d8f4554ebda3c904b`  
		Last Modified: Mon, 16 Mar 2026 23:43:17 GMT  
		Size: 2.8 MB (2781248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7469dca3f1d192339e3e8d77677a7da5436b8a7ca780fd02b55c4f52d5ed9bea`  
		Last Modified: Mon, 16 Mar 2026 23:43:17 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:2.4`

```console
$ docker pull rethinkdb@sha256:bd052c2ca98d731e2b3e794f795ef1e24dec762108ce9734c5c19a56b73fa71a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rethinkdb:2.4` - linux; amd64

```console
$ docker pull rethinkdb@sha256:9a346c1b472d23752c3c75d25871b136052c84f5a0be54e11e555ac7d2662f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48031604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e19cb11eb2b02233f790d7cda93df1a6e95d1be1d5151ed397e7e887c9f583`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:35:56 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:35:57 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 16 Mar 2026 22:36:03 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 16 Mar 2026 22:36:03 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:36:03 GMT
VOLUME [/data]
# Mon, 16 Mar 2026 22:36:03 GMT
WORKDIR /data
# Mon, 16 Mar 2026 22:36:03 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 16 Mar 2026 22:36:03 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71704a3d3c7df105339617c2524cd0afb35d61ba643e31020adce407ac94d3de`  
		Last Modified: Mon, 16 Mar 2026 22:36:10 GMT  
		Size: 9.8 MB (9799396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2f94d16318afed5ecbb41d245aeaf836f2589faee765f3b6eea080831b8c1c`  
		Last Modified: Mon, 16 Mar 2026 22:36:10 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d9a0f54967e418507c12b24e9c37df0945177f9d80365f3c30b51dc8f6b6d6`  
		Last Modified: Mon, 16 Mar 2026 22:36:10 GMT  
		Size: 10.0 MB (9993221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2813767849ffed6060dbc015c616d93cf3dd9257b2dbca8535d52883e241cbf5`  
		Last Modified: Mon, 16 Mar 2026 22:36:10 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:fed881594fa2dc6a9c12da83a55e08779901151967d0acac544de78404407706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d9249e3d4f2a6023200ba79111a259b129a7d7881489a5f1919aa630c004bda`

```dockerfile
```

-	Layers:
	-	`sha256:1055d74f2a23f211107760f46673956a73f2806b372be64e267d1e69033f463d`  
		Last Modified: Mon, 16 Mar 2026 22:36:10 GMT  
		Size: 2.8 MB (2785046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a3b0dc6d885aa7907efd83e9d39e8aea97cbba5425ddebd8a7d0f8b208994e7`  
		Last Modified: Mon, 16 Mar 2026 22:36:10 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:eb5fa1f28212eb74ac40e4b41813690ddee9cb0631aeaf0dbaf112fe6d0e55fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47110147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc0dbf509a7be68a33e0fa5ac93b1604e87cfa0e1d5e97248fda3130f3cc14d`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:38:23 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:38:24 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 16 Mar 2026 22:38:29 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 16 Mar 2026 22:38:29 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:38:29 GMT
VOLUME [/data]
# Mon, 16 Mar 2026 22:38:29 GMT
WORKDIR /data
# Mon, 16 Mar 2026 22:38:29 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 16 Mar 2026 22:38:29 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:addc91a63479667884ce4f98cede66ac22fb9f4c00a54e6e037934325e1e6866`  
		Last Modified: Mon, 16 Mar 2026 22:38:36 GMT  
		Size: 9.6 MB (9628365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49afdf53e977087b916ed3869884b20c70ef5a0b0c740acc56b520525ceafdc9`  
		Last Modified: Mon, 16 Mar 2026 22:38:36 GMT  
		Size: 2.7 KB (2665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab2218262d3fce9640555b0728347b9b7b42e9058775fe8b237ca6f5851ab3a`  
		Last Modified: Mon, 16 Mar 2026 22:38:36 GMT  
		Size: 9.4 MB (9362959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d06ec3cd0cae998ad5994e2e6735bb051f5ca642c28bd1188f28a9902ed5ed20`  
		Last Modified: Mon, 16 Mar 2026 22:38:36 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:0294022552661a2bd8c3419bdfdf0e94c6c0af694168d7cdd12b52b3ce23a423
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e23178f8bea118419f36bf3579df653a032c7659f42766e141ad4e8d37fee76`

```dockerfile
```

-	Layers:
	-	`sha256:ffa03f3f0afd31eea7975eaacf743c3e0ab752b34d5e27854d0c2a3ca950b5d8`  
		Last Modified: Mon, 16 Mar 2026 22:38:36 GMT  
		Size: 2.8 MB (2785381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f87d57613fbff19f9f1b17891bd210539f6bdf95225bc85b68eca7761d7d92b6`  
		Last Modified: Mon, 16 Mar 2026 22:38:36 GMT  
		Size: 13.6 KB (13586 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4` - linux; s390x

```console
$ docker pull rethinkdb@sha256:5bdc081839b933b512e25d8c3acadfa2c20abfb1882ebd7d9a594350286aa7dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45495577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:353e6c471e19b5f3ccadb080b9aebb478b172302e956477e809d3cb8d303d1e0`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:42:55 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:42:57 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 16 Mar 2026 23:43:02 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 16 Mar 2026 23:43:02 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:43:02 GMT
VOLUME [/data]
# Mon, 16 Mar 2026 23:43:02 GMT
WORKDIR /data
# Mon, 16 Mar 2026 23:43:02 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 16 Mar 2026 23:43:02 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ae76cc96a4cba2739c8be0ce73e62f473c5a663eeb015b4cf60dda4895e88b`  
		Last Modified: Mon, 16 Mar 2026 23:43:19 GMT  
		Size: 9.3 MB (9297538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60e6fb7614b82d95c2c421fae589438a70eca69a9742211c7f70e8fa55d8bb5`  
		Last Modified: Mon, 16 Mar 2026 23:43:17 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3a1969febccd2d1846984311e6ac35eeaaeb64cdef9c24b8be97c093aaa4c8`  
		Last Modified: Mon, 16 Mar 2026 23:43:18 GMT  
		Size: 9.3 MB (9303762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730395b6605549628d7228a8fe89cd74d7fb18301b1ebad6d739425bde78aa86`  
		Last Modified: Mon, 16 Mar 2026 23:43:17 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:4d12fb1620d8ac8e82daca4df71ea2037f3e3fd8fd50efef793541311e85a319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2794652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78bc4d832486dc105b9b5e33841a8415a0bc562bb401a559e11e5cb2792bf568`

```dockerfile
```

-	Layers:
	-	`sha256:4ba1f101408adaa8602261d8d8f827abe5557ae92aaa639d8f4554ebda3c904b`  
		Last Modified: Mon, 16 Mar 2026 23:43:17 GMT  
		Size: 2.8 MB (2781248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7469dca3f1d192339e3e8d77677a7da5436b8a7ca780fd02b55c4f52d5ed9bea`  
		Last Modified: Mon, 16 Mar 2026 23:43:17 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:2.4-bookworm-slim`

```console
$ docker pull rethinkdb@sha256:bd052c2ca98d731e2b3e794f795ef1e24dec762108ce9734c5c19a56b73fa71a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rethinkdb:2.4-bookworm-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:9a346c1b472d23752c3c75d25871b136052c84f5a0be54e11e555ac7d2662f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48031604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e19cb11eb2b02233f790d7cda93df1a6e95d1be1d5151ed397e7e887c9f583`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:35:56 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:35:57 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 16 Mar 2026 22:36:03 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 16 Mar 2026 22:36:03 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:36:03 GMT
VOLUME [/data]
# Mon, 16 Mar 2026 22:36:03 GMT
WORKDIR /data
# Mon, 16 Mar 2026 22:36:03 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 16 Mar 2026 22:36:03 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71704a3d3c7df105339617c2524cd0afb35d61ba643e31020adce407ac94d3de`  
		Last Modified: Mon, 16 Mar 2026 22:36:10 GMT  
		Size: 9.8 MB (9799396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2f94d16318afed5ecbb41d245aeaf836f2589faee765f3b6eea080831b8c1c`  
		Last Modified: Mon, 16 Mar 2026 22:36:10 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d9a0f54967e418507c12b24e9c37df0945177f9d80365f3c30b51dc8f6b6d6`  
		Last Modified: Mon, 16 Mar 2026 22:36:10 GMT  
		Size: 10.0 MB (9993221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2813767849ffed6060dbc015c616d93cf3dd9257b2dbca8535d52883e241cbf5`  
		Last Modified: Mon, 16 Mar 2026 22:36:10 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:fed881594fa2dc6a9c12da83a55e08779901151967d0acac544de78404407706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d9249e3d4f2a6023200ba79111a259b129a7d7881489a5f1919aa630c004bda`

```dockerfile
```

-	Layers:
	-	`sha256:1055d74f2a23f211107760f46673956a73f2806b372be64e267d1e69033f463d`  
		Last Modified: Mon, 16 Mar 2026 22:36:10 GMT  
		Size: 2.8 MB (2785046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a3b0dc6d885aa7907efd83e9d39e8aea97cbba5425ddebd8a7d0f8b208994e7`  
		Last Modified: Mon, 16 Mar 2026 22:36:10 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:eb5fa1f28212eb74ac40e4b41813690ddee9cb0631aeaf0dbaf112fe6d0e55fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47110147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc0dbf509a7be68a33e0fa5ac93b1604e87cfa0e1d5e97248fda3130f3cc14d`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:38:23 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:38:24 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 16 Mar 2026 22:38:29 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 16 Mar 2026 22:38:29 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:38:29 GMT
VOLUME [/data]
# Mon, 16 Mar 2026 22:38:29 GMT
WORKDIR /data
# Mon, 16 Mar 2026 22:38:29 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 16 Mar 2026 22:38:29 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:addc91a63479667884ce4f98cede66ac22fb9f4c00a54e6e037934325e1e6866`  
		Last Modified: Mon, 16 Mar 2026 22:38:36 GMT  
		Size: 9.6 MB (9628365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49afdf53e977087b916ed3869884b20c70ef5a0b0c740acc56b520525ceafdc9`  
		Last Modified: Mon, 16 Mar 2026 22:38:36 GMT  
		Size: 2.7 KB (2665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab2218262d3fce9640555b0728347b9b7b42e9058775fe8b237ca6f5851ab3a`  
		Last Modified: Mon, 16 Mar 2026 22:38:36 GMT  
		Size: 9.4 MB (9362959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d06ec3cd0cae998ad5994e2e6735bb051f5ca642c28bd1188f28a9902ed5ed20`  
		Last Modified: Mon, 16 Mar 2026 22:38:36 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:0294022552661a2bd8c3419bdfdf0e94c6c0af694168d7cdd12b52b3ce23a423
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e23178f8bea118419f36bf3579df653a032c7659f42766e141ad4e8d37fee76`

```dockerfile
```

-	Layers:
	-	`sha256:ffa03f3f0afd31eea7975eaacf743c3e0ab752b34d5e27854d0c2a3ca950b5d8`  
		Last Modified: Mon, 16 Mar 2026 22:38:36 GMT  
		Size: 2.8 MB (2785381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f87d57613fbff19f9f1b17891bd210539f6bdf95225bc85b68eca7761d7d92b6`  
		Last Modified: Mon, 16 Mar 2026 22:38:36 GMT  
		Size: 13.6 KB (13586 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4-bookworm-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:5bdc081839b933b512e25d8c3acadfa2c20abfb1882ebd7d9a594350286aa7dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45495577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:353e6c471e19b5f3ccadb080b9aebb478b172302e956477e809d3cb8d303d1e0`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:42:55 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:42:57 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 16 Mar 2026 23:43:02 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 16 Mar 2026 23:43:02 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:43:02 GMT
VOLUME [/data]
# Mon, 16 Mar 2026 23:43:02 GMT
WORKDIR /data
# Mon, 16 Mar 2026 23:43:02 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 16 Mar 2026 23:43:02 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ae76cc96a4cba2739c8be0ce73e62f473c5a663eeb015b4cf60dda4895e88b`  
		Last Modified: Mon, 16 Mar 2026 23:43:19 GMT  
		Size: 9.3 MB (9297538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60e6fb7614b82d95c2c421fae589438a70eca69a9742211c7f70e8fa55d8bb5`  
		Last Modified: Mon, 16 Mar 2026 23:43:17 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3a1969febccd2d1846984311e6ac35eeaaeb64cdef9c24b8be97c093aaa4c8`  
		Last Modified: Mon, 16 Mar 2026 23:43:18 GMT  
		Size: 9.3 MB (9303762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730395b6605549628d7228a8fe89cd74d7fb18301b1ebad6d739425bde78aa86`  
		Last Modified: Mon, 16 Mar 2026 23:43:17 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:4d12fb1620d8ac8e82daca4df71ea2037f3e3fd8fd50efef793541311e85a319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2794652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78bc4d832486dc105b9b5e33841a8415a0bc562bb401a559e11e5cb2792bf568`

```dockerfile
```

-	Layers:
	-	`sha256:4ba1f101408adaa8602261d8d8f827abe5557ae92aaa639d8f4554ebda3c904b`  
		Last Modified: Mon, 16 Mar 2026 23:43:17 GMT  
		Size: 2.8 MB (2781248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7469dca3f1d192339e3e8d77677a7da5436b8a7ca780fd02b55c4f52d5ed9bea`  
		Last Modified: Mon, 16 Mar 2026 23:43:17 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:2.4.3`

```console
$ docker pull rethinkdb@sha256:bd052c2ca98d731e2b3e794f795ef1e24dec762108ce9734c5c19a56b73fa71a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rethinkdb:2.4.3` - linux; amd64

```console
$ docker pull rethinkdb@sha256:9a346c1b472d23752c3c75d25871b136052c84f5a0be54e11e555ac7d2662f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48031604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e19cb11eb2b02233f790d7cda93df1a6e95d1be1d5151ed397e7e887c9f583`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:35:56 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:35:57 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 16 Mar 2026 22:36:03 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 16 Mar 2026 22:36:03 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:36:03 GMT
VOLUME [/data]
# Mon, 16 Mar 2026 22:36:03 GMT
WORKDIR /data
# Mon, 16 Mar 2026 22:36:03 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 16 Mar 2026 22:36:03 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71704a3d3c7df105339617c2524cd0afb35d61ba643e31020adce407ac94d3de`  
		Last Modified: Mon, 16 Mar 2026 22:36:10 GMT  
		Size: 9.8 MB (9799396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2f94d16318afed5ecbb41d245aeaf836f2589faee765f3b6eea080831b8c1c`  
		Last Modified: Mon, 16 Mar 2026 22:36:10 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d9a0f54967e418507c12b24e9c37df0945177f9d80365f3c30b51dc8f6b6d6`  
		Last Modified: Mon, 16 Mar 2026 22:36:10 GMT  
		Size: 10.0 MB (9993221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2813767849ffed6060dbc015c616d93cf3dd9257b2dbca8535d52883e241cbf5`  
		Last Modified: Mon, 16 Mar 2026 22:36:10 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.3` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:fed881594fa2dc6a9c12da83a55e08779901151967d0acac544de78404407706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d9249e3d4f2a6023200ba79111a259b129a7d7881489a5f1919aa630c004bda`

```dockerfile
```

-	Layers:
	-	`sha256:1055d74f2a23f211107760f46673956a73f2806b372be64e267d1e69033f463d`  
		Last Modified: Mon, 16 Mar 2026 22:36:10 GMT  
		Size: 2.8 MB (2785046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a3b0dc6d885aa7907efd83e9d39e8aea97cbba5425ddebd8a7d0f8b208994e7`  
		Last Modified: Mon, 16 Mar 2026 22:36:10 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4.3` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:eb5fa1f28212eb74ac40e4b41813690ddee9cb0631aeaf0dbaf112fe6d0e55fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47110147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc0dbf509a7be68a33e0fa5ac93b1604e87cfa0e1d5e97248fda3130f3cc14d`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:38:23 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:38:24 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 16 Mar 2026 22:38:29 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 16 Mar 2026 22:38:29 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:38:29 GMT
VOLUME [/data]
# Mon, 16 Mar 2026 22:38:29 GMT
WORKDIR /data
# Mon, 16 Mar 2026 22:38:29 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 16 Mar 2026 22:38:29 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:addc91a63479667884ce4f98cede66ac22fb9f4c00a54e6e037934325e1e6866`  
		Last Modified: Mon, 16 Mar 2026 22:38:36 GMT  
		Size: 9.6 MB (9628365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49afdf53e977087b916ed3869884b20c70ef5a0b0c740acc56b520525ceafdc9`  
		Last Modified: Mon, 16 Mar 2026 22:38:36 GMT  
		Size: 2.7 KB (2665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab2218262d3fce9640555b0728347b9b7b42e9058775fe8b237ca6f5851ab3a`  
		Last Modified: Mon, 16 Mar 2026 22:38:36 GMT  
		Size: 9.4 MB (9362959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d06ec3cd0cae998ad5994e2e6735bb051f5ca642c28bd1188f28a9902ed5ed20`  
		Last Modified: Mon, 16 Mar 2026 22:38:36 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.3` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:0294022552661a2bd8c3419bdfdf0e94c6c0af694168d7cdd12b52b3ce23a423
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e23178f8bea118419f36bf3579df653a032c7659f42766e141ad4e8d37fee76`

```dockerfile
```

-	Layers:
	-	`sha256:ffa03f3f0afd31eea7975eaacf743c3e0ab752b34d5e27854d0c2a3ca950b5d8`  
		Last Modified: Mon, 16 Mar 2026 22:38:36 GMT  
		Size: 2.8 MB (2785381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f87d57613fbff19f9f1b17891bd210539f6bdf95225bc85b68eca7761d7d92b6`  
		Last Modified: Mon, 16 Mar 2026 22:38:36 GMT  
		Size: 13.6 KB (13586 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4.3` - linux; s390x

```console
$ docker pull rethinkdb@sha256:5bdc081839b933b512e25d8c3acadfa2c20abfb1882ebd7d9a594350286aa7dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45495577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:353e6c471e19b5f3ccadb080b9aebb478b172302e956477e809d3cb8d303d1e0`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:42:55 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:42:57 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 16 Mar 2026 23:43:02 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 16 Mar 2026 23:43:02 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:43:02 GMT
VOLUME [/data]
# Mon, 16 Mar 2026 23:43:02 GMT
WORKDIR /data
# Mon, 16 Mar 2026 23:43:02 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 16 Mar 2026 23:43:02 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ae76cc96a4cba2739c8be0ce73e62f473c5a663eeb015b4cf60dda4895e88b`  
		Last Modified: Mon, 16 Mar 2026 23:43:19 GMT  
		Size: 9.3 MB (9297538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60e6fb7614b82d95c2c421fae589438a70eca69a9742211c7f70e8fa55d8bb5`  
		Last Modified: Mon, 16 Mar 2026 23:43:17 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3a1969febccd2d1846984311e6ac35eeaaeb64cdef9c24b8be97c093aaa4c8`  
		Last Modified: Mon, 16 Mar 2026 23:43:18 GMT  
		Size: 9.3 MB (9303762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730395b6605549628d7228a8fe89cd74d7fb18301b1ebad6d739425bde78aa86`  
		Last Modified: Mon, 16 Mar 2026 23:43:17 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.3` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:4d12fb1620d8ac8e82daca4df71ea2037f3e3fd8fd50efef793541311e85a319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2794652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78bc4d832486dc105b9b5e33841a8415a0bc562bb401a559e11e5cb2792bf568`

```dockerfile
```

-	Layers:
	-	`sha256:4ba1f101408adaa8602261d8d8f827abe5557ae92aaa639d8f4554ebda3c904b`  
		Last Modified: Mon, 16 Mar 2026 23:43:17 GMT  
		Size: 2.8 MB (2781248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7469dca3f1d192339e3e8d77677a7da5436b8a7ca780fd02b55c4f52d5ed9bea`  
		Last Modified: Mon, 16 Mar 2026 23:43:17 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:2.4.4-bookworm-slim`

```console
$ docker pull rethinkdb@sha256:bd052c2ca98d731e2b3e794f795ef1e24dec762108ce9734c5c19a56b73fa71a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rethinkdb:2.4.4-bookworm-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:9a346c1b472d23752c3c75d25871b136052c84f5a0be54e11e555ac7d2662f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48031604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e19cb11eb2b02233f790d7cda93df1a6e95d1be1d5151ed397e7e887c9f583`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:35:56 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:35:57 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 16 Mar 2026 22:36:03 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 16 Mar 2026 22:36:03 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:36:03 GMT
VOLUME [/data]
# Mon, 16 Mar 2026 22:36:03 GMT
WORKDIR /data
# Mon, 16 Mar 2026 22:36:03 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 16 Mar 2026 22:36:03 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71704a3d3c7df105339617c2524cd0afb35d61ba643e31020adce407ac94d3de`  
		Last Modified: Mon, 16 Mar 2026 22:36:10 GMT  
		Size: 9.8 MB (9799396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2f94d16318afed5ecbb41d245aeaf836f2589faee765f3b6eea080831b8c1c`  
		Last Modified: Mon, 16 Mar 2026 22:36:10 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d9a0f54967e418507c12b24e9c37df0945177f9d80365f3c30b51dc8f6b6d6`  
		Last Modified: Mon, 16 Mar 2026 22:36:10 GMT  
		Size: 10.0 MB (9993221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2813767849ffed6060dbc015c616d93cf3dd9257b2dbca8535d52883e241cbf5`  
		Last Modified: Mon, 16 Mar 2026 22:36:10 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:fed881594fa2dc6a9c12da83a55e08779901151967d0acac544de78404407706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d9249e3d4f2a6023200ba79111a259b129a7d7881489a5f1919aa630c004bda`

```dockerfile
```

-	Layers:
	-	`sha256:1055d74f2a23f211107760f46673956a73f2806b372be64e267d1e69033f463d`  
		Last Modified: Mon, 16 Mar 2026 22:36:10 GMT  
		Size: 2.8 MB (2785046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a3b0dc6d885aa7907efd83e9d39e8aea97cbba5425ddebd8a7d0f8b208994e7`  
		Last Modified: Mon, 16 Mar 2026 22:36:10 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4.4-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:eb5fa1f28212eb74ac40e4b41813690ddee9cb0631aeaf0dbaf112fe6d0e55fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47110147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc0dbf509a7be68a33e0fa5ac93b1604e87cfa0e1d5e97248fda3130f3cc14d`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:38:23 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:38:24 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 16 Mar 2026 22:38:29 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 16 Mar 2026 22:38:29 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:38:29 GMT
VOLUME [/data]
# Mon, 16 Mar 2026 22:38:29 GMT
WORKDIR /data
# Mon, 16 Mar 2026 22:38:29 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 16 Mar 2026 22:38:29 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:addc91a63479667884ce4f98cede66ac22fb9f4c00a54e6e037934325e1e6866`  
		Last Modified: Mon, 16 Mar 2026 22:38:36 GMT  
		Size: 9.6 MB (9628365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49afdf53e977087b916ed3869884b20c70ef5a0b0c740acc56b520525ceafdc9`  
		Last Modified: Mon, 16 Mar 2026 22:38:36 GMT  
		Size: 2.7 KB (2665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab2218262d3fce9640555b0728347b9b7b42e9058775fe8b237ca6f5851ab3a`  
		Last Modified: Mon, 16 Mar 2026 22:38:36 GMT  
		Size: 9.4 MB (9362959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d06ec3cd0cae998ad5994e2e6735bb051f5ca642c28bd1188f28a9902ed5ed20`  
		Last Modified: Mon, 16 Mar 2026 22:38:36 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:0294022552661a2bd8c3419bdfdf0e94c6c0af694168d7cdd12b52b3ce23a423
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e23178f8bea118419f36bf3579df653a032c7659f42766e141ad4e8d37fee76`

```dockerfile
```

-	Layers:
	-	`sha256:ffa03f3f0afd31eea7975eaacf743c3e0ab752b34d5e27854d0c2a3ca950b5d8`  
		Last Modified: Mon, 16 Mar 2026 22:38:36 GMT  
		Size: 2.8 MB (2785381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f87d57613fbff19f9f1b17891bd210539f6bdf95225bc85b68eca7761d7d92b6`  
		Last Modified: Mon, 16 Mar 2026 22:38:36 GMT  
		Size: 13.6 KB (13586 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4.4-bookworm-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:5bdc081839b933b512e25d8c3acadfa2c20abfb1882ebd7d9a594350286aa7dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45495577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:353e6c471e19b5f3ccadb080b9aebb478b172302e956477e809d3cb8d303d1e0`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:42:55 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:42:57 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 16 Mar 2026 23:43:02 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 16 Mar 2026 23:43:02 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:43:02 GMT
VOLUME [/data]
# Mon, 16 Mar 2026 23:43:02 GMT
WORKDIR /data
# Mon, 16 Mar 2026 23:43:02 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 16 Mar 2026 23:43:02 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ae76cc96a4cba2739c8be0ce73e62f473c5a663eeb015b4cf60dda4895e88b`  
		Last Modified: Mon, 16 Mar 2026 23:43:19 GMT  
		Size: 9.3 MB (9297538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60e6fb7614b82d95c2c421fae589438a70eca69a9742211c7f70e8fa55d8bb5`  
		Last Modified: Mon, 16 Mar 2026 23:43:17 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3a1969febccd2d1846984311e6ac35eeaaeb64cdef9c24b8be97c093aaa4c8`  
		Last Modified: Mon, 16 Mar 2026 23:43:18 GMT  
		Size: 9.3 MB (9303762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730395b6605549628d7228a8fe89cd74d7fb18301b1ebad6d739425bde78aa86`  
		Last Modified: Mon, 16 Mar 2026 23:43:17 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:4d12fb1620d8ac8e82daca4df71ea2037f3e3fd8fd50efef793541311e85a319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2794652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78bc4d832486dc105b9b5e33841a8415a0bc562bb401a559e11e5cb2792bf568`

```dockerfile
```

-	Layers:
	-	`sha256:4ba1f101408adaa8602261d8d8f827abe5557ae92aaa639d8f4554ebda3c904b`  
		Last Modified: Mon, 16 Mar 2026 23:43:17 GMT  
		Size: 2.8 MB (2781248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7469dca3f1d192339e3e8d77677a7da5436b8a7ca780fd02b55c4f52d5ed9bea`  
		Last Modified: Mon, 16 Mar 2026 23:43:17 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:bookworm-slim`

```console
$ docker pull rethinkdb@sha256:bd052c2ca98d731e2b3e794f795ef1e24dec762108ce9734c5c19a56b73fa71a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rethinkdb:bookworm-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:9a346c1b472d23752c3c75d25871b136052c84f5a0be54e11e555ac7d2662f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48031604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e19cb11eb2b02233f790d7cda93df1a6e95d1be1d5151ed397e7e887c9f583`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:35:56 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:35:57 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 16 Mar 2026 22:36:03 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 16 Mar 2026 22:36:03 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:36:03 GMT
VOLUME [/data]
# Mon, 16 Mar 2026 22:36:03 GMT
WORKDIR /data
# Mon, 16 Mar 2026 22:36:03 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 16 Mar 2026 22:36:03 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71704a3d3c7df105339617c2524cd0afb35d61ba643e31020adce407ac94d3de`  
		Last Modified: Mon, 16 Mar 2026 22:36:10 GMT  
		Size: 9.8 MB (9799396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2f94d16318afed5ecbb41d245aeaf836f2589faee765f3b6eea080831b8c1c`  
		Last Modified: Mon, 16 Mar 2026 22:36:10 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d9a0f54967e418507c12b24e9c37df0945177f9d80365f3c30b51dc8f6b6d6`  
		Last Modified: Mon, 16 Mar 2026 22:36:10 GMT  
		Size: 10.0 MB (9993221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2813767849ffed6060dbc015c616d93cf3dd9257b2dbca8535d52883e241cbf5`  
		Last Modified: Mon, 16 Mar 2026 22:36:10 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:fed881594fa2dc6a9c12da83a55e08779901151967d0acac544de78404407706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d9249e3d4f2a6023200ba79111a259b129a7d7881489a5f1919aa630c004bda`

```dockerfile
```

-	Layers:
	-	`sha256:1055d74f2a23f211107760f46673956a73f2806b372be64e267d1e69033f463d`  
		Last Modified: Mon, 16 Mar 2026 22:36:10 GMT  
		Size: 2.8 MB (2785046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a3b0dc6d885aa7907efd83e9d39e8aea97cbba5425ddebd8a7d0f8b208994e7`  
		Last Modified: Mon, 16 Mar 2026 22:36:10 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:eb5fa1f28212eb74ac40e4b41813690ddee9cb0631aeaf0dbaf112fe6d0e55fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47110147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc0dbf509a7be68a33e0fa5ac93b1604e87cfa0e1d5e97248fda3130f3cc14d`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:38:23 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:38:24 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 16 Mar 2026 22:38:29 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 16 Mar 2026 22:38:29 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:38:29 GMT
VOLUME [/data]
# Mon, 16 Mar 2026 22:38:29 GMT
WORKDIR /data
# Mon, 16 Mar 2026 22:38:29 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 16 Mar 2026 22:38:29 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:addc91a63479667884ce4f98cede66ac22fb9f4c00a54e6e037934325e1e6866`  
		Last Modified: Mon, 16 Mar 2026 22:38:36 GMT  
		Size: 9.6 MB (9628365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49afdf53e977087b916ed3869884b20c70ef5a0b0c740acc56b520525ceafdc9`  
		Last Modified: Mon, 16 Mar 2026 22:38:36 GMT  
		Size: 2.7 KB (2665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab2218262d3fce9640555b0728347b9b7b42e9058775fe8b237ca6f5851ab3a`  
		Last Modified: Mon, 16 Mar 2026 22:38:36 GMT  
		Size: 9.4 MB (9362959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d06ec3cd0cae998ad5994e2e6735bb051f5ca642c28bd1188f28a9902ed5ed20`  
		Last Modified: Mon, 16 Mar 2026 22:38:36 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:0294022552661a2bd8c3419bdfdf0e94c6c0af694168d7cdd12b52b3ce23a423
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e23178f8bea118419f36bf3579df653a032c7659f42766e141ad4e8d37fee76`

```dockerfile
```

-	Layers:
	-	`sha256:ffa03f3f0afd31eea7975eaacf743c3e0ab752b34d5e27854d0c2a3ca950b5d8`  
		Last Modified: Mon, 16 Mar 2026 22:38:36 GMT  
		Size: 2.8 MB (2785381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f87d57613fbff19f9f1b17891bd210539f6bdf95225bc85b68eca7761d7d92b6`  
		Last Modified: Mon, 16 Mar 2026 22:38:36 GMT  
		Size: 13.6 KB (13586 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:bookworm-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:5bdc081839b933b512e25d8c3acadfa2c20abfb1882ebd7d9a594350286aa7dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45495577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:353e6c471e19b5f3ccadb080b9aebb478b172302e956477e809d3cb8d303d1e0`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:42:55 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:42:57 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 16 Mar 2026 23:43:02 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 16 Mar 2026 23:43:02 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:43:02 GMT
VOLUME [/data]
# Mon, 16 Mar 2026 23:43:02 GMT
WORKDIR /data
# Mon, 16 Mar 2026 23:43:02 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 16 Mar 2026 23:43:02 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ae76cc96a4cba2739c8be0ce73e62f473c5a663eeb015b4cf60dda4895e88b`  
		Last Modified: Mon, 16 Mar 2026 23:43:19 GMT  
		Size: 9.3 MB (9297538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60e6fb7614b82d95c2c421fae589438a70eca69a9742211c7f70e8fa55d8bb5`  
		Last Modified: Mon, 16 Mar 2026 23:43:17 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3a1969febccd2d1846984311e6ac35eeaaeb64cdef9c24b8be97c093aaa4c8`  
		Last Modified: Mon, 16 Mar 2026 23:43:18 GMT  
		Size: 9.3 MB (9303762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730395b6605549628d7228a8fe89cd74d7fb18301b1ebad6d739425bde78aa86`  
		Last Modified: Mon, 16 Mar 2026 23:43:17 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:4d12fb1620d8ac8e82daca4df71ea2037f3e3fd8fd50efef793541311e85a319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2794652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78bc4d832486dc105b9b5e33841a8415a0bc562bb401a559e11e5cb2792bf568`

```dockerfile
```

-	Layers:
	-	`sha256:4ba1f101408adaa8602261d8d8f827abe5557ae92aaa639d8f4554ebda3c904b`  
		Last Modified: Mon, 16 Mar 2026 23:43:17 GMT  
		Size: 2.8 MB (2781248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7469dca3f1d192339e3e8d77677a7da5436b8a7ca780fd02b55c4f52d5ed9bea`  
		Last Modified: Mon, 16 Mar 2026 23:43:17 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:latest`

```console
$ docker pull rethinkdb@sha256:bd052c2ca98d731e2b3e794f795ef1e24dec762108ce9734c5c19a56b73fa71a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rethinkdb:latest` - linux; amd64

```console
$ docker pull rethinkdb@sha256:9a346c1b472d23752c3c75d25871b136052c84f5a0be54e11e555ac7d2662f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48031604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e19cb11eb2b02233f790d7cda93df1a6e95d1be1d5151ed397e7e887c9f583`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:35:56 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:35:57 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 16 Mar 2026 22:36:03 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 16 Mar 2026 22:36:03 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:36:03 GMT
VOLUME [/data]
# Mon, 16 Mar 2026 22:36:03 GMT
WORKDIR /data
# Mon, 16 Mar 2026 22:36:03 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 16 Mar 2026 22:36:03 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71704a3d3c7df105339617c2524cd0afb35d61ba643e31020adce407ac94d3de`  
		Last Modified: Mon, 16 Mar 2026 22:36:10 GMT  
		Size: 9.8 MB (9799396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2f94d16318afed5ecbb41d245aeaf836f2589faee765f3b6eea080831b8c1c`  
		Last Modified: Mon, 16 Mar 2026 22:36:10 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d9a0f54967e418507c12b24e9c37df0945177f9d80365f3c30b51dc8f6b6d6`  
		Last Modified: Mon, 16 Mar 2026 22:36:10 GMT  
		Size: 10.0 MB (9993221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2813767849ffed6060dbc015c616d93cf3dd9257b2dbca8535d52883e241cbf5`  
		Last Modified: Mon, 16 Mar 2026 22:36:10 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:latest` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:fed881594fa2dc6a9c12da83a55e08779901151967d0acac544de78404407706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d9249e3d4f2a6023200ba79111a259b129a7d7881489a5f1919aa630c004bda`

```dockerfile
```

-	Layers:
	-	`sha256:1055d74f2a23f211107760f46673956a73f2806b372be64e267d1e69033f463d`  
		Last Modified: Mon, 16 Mar 2026 22:36:10 GMT  
		Size: 2.8 MB (2785046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a3b0dc6d885aa7907efd83e9d39e8aea97cbba5425ddebd8a7d0f8b208994e7`  
		Last Modified: Mon, 16 Mar 2026 22:36:10 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:latest` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:eb5fa1f28212eb74ac40e4b41813690ddee9cb0631aeaf0dbaf112fe6d0e55fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47110147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc0dbf509a7be68a33e0fa5ac93b1604e87cfa0e1d5e97248fda3130f3cc14d`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:38:23 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:38:24 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 16 Mar 2026 22:38:29 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 16 Mar 2026 22:38:29 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:38:29 GMT
VOLUME [/data]
# Mon, 16 Mar 2026 22:38:29 GMT
WORKDIR /data
# Mon, 16 Mar 2026 22:38:29 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 16 Mar 2026 22:38:29 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:addc91a63479667884ce4f98cede66ac22fb9f4c00a54e6e037934325e1e6866`  
		Last Modified: Mon, 16 Mar 2026 22:38:36 GMT  
		Size: 9.6 MB (9628365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49afdf53e977087b916ed3869884b20c70ef5a0b0c740acc56b520525ceafdc9`  
		Last Modified: Mon, 16 Mar 2026 22:38:36 GMT  
		Size: 2.7 KB (2665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab2218262d3fce9640555b0728347b9b7b42e9058775fe8b237ca6f5851ab3a`  
		Last Modified: Mon, 16 Mar 2026 22:38:36 GMT  
		Size: 9.4 MB (9362959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d06ec3cd0cae998ad5994e2e6735bb051f5ca642c28bd1188f28a9902ed5ed20`  
		Last Modified: Mon, 16 Mar 2026 22:38:36 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:latest` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:0294022552661a2bd8c3419bdfdf0e94c6c0af694168d7cdd12b52b3ce23a423
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e23178f8bea118419f36bf3579df653a032c7659f42766e141ad4e8d37fee76`

```dockerfile
```

-	Layers:
	-	`sha256:ffa03f3f0afd31eea7975eaacf743c3e0ab752b34d5e27854d0c2a3ca950b5d8`  
		Last Modified: Mon, 16 Mar 2026 22:38:36 GMT  
		Size: 2.8 MB (2785381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f87d57613fbff19f9f1b17891bd210539f6bdf95225bc85b68eca7761d7d92b6`  
		Last Modified: Mon, 16 Mar 2026 22:38:36 GMT  
		Size: 13.6 KB (13586 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:latest` - linux; s390x

```console
$ docker pull rethinkdb@sha256:5bdc081839b933b512e25d8c3acadfa2c20abfb1882ebd7d9a594350286aa7dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45495577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:353e6c471e19b5f3ccadb080b9aebb478b172302e956477e809d3cb8d303d1e0`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:42:55 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:42:57 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 16 Mar 2026 23:43:02 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 16 Mar 2026 23:43:02 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:43:02 GMT
VOLUME [/data]
# Mon, 16 Mar 2026 23:43:02 GMT
WORKDIR /data
# Mon, 16 Mar 2026 23:43:02 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 16 Mar 2026 23:43:02 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ae76cc96a4cba2739c8be0ce73e62f473c5a663eeb015b4cf60dda4895e88b`  
		Last Modified: Mon, 16 Mar 2026 23:43:19 GMT  
		Size: 9.3 MB (9297538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60e6fb7614b82d95c2c421fae589438a70eca69a9742211c7f70e8fa55d8bb5`  
		Last Modified: Mon, 16 Mar 2026 23:43:17 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3a1969febccd2d1846984311e6ac35eeaaeb64cdef9c24b8be97c093aaa4c8`  
		Last Modified: Mon, 16 Mar 2026 23:43:18 GMT  
		Size: 9.3 MB (9303762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730395b6605549628d7228a8fe89cd74d7fb18301b1ebad6d739425bde78aa86`  
		Last Modified: Mon, 16 Mar 2026 23:43:17 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:latest` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:4d12fb1620d8ac8e82daca4df71ea2037f3e3fd8fd50efef793541311e85a319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2794652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78bc4d832486dc105b9b5e33841a8415a0bc562bb401a559e11e5cb2792bf568`

```dockerfile
```

-	Layers:
	-	`sha256:4ba1f101408adaa8602261d8d8f827abe5557ae92aaa639d8f4554ebda3c904b`  
		Last Modified: Mon, 16 Mar 2026 23:43:17 GMT  
		Size: 2.8 MB (2781248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7469dca3f1d192339e3e8d77677a7da5436b8a7ca780fd02b55c4f52d5ed9bea`  
		Last Modified: Mon, 16 Mar 2026 23:43:17 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json
