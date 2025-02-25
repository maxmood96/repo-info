## `rethinkdb:bookworm-slim`

```console
$ docker pull rethinkdb@sha256:2bd058a87d458ac6b6dfcd8a390ad6eff37acce04d25271ff16ccb0cfaa6a66b
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
$ docker pull rethinkdb@sha256:1ffadc99b30953738347e15c9feaaf0d3ba434749a0ca7956d97bf0ca63761e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48005908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfee24e58c9b24c20146c9b3414a0554783a417ad3f68bafc3642a8884246de9`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
VOLUME [/data]
# Wed, 13 Dec 2023 22:17:20 GMT
WORKDIR /data
# Wed, 13 Dec 2023 22:17:20 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 13 Dec 2023 22:17:20 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595c7f2c683ab14deac0c267673a11013e4ffe81cf4afc22e5e22466d4b602cc`  
		Last Modified: Tue, 25 Feb 2025 02:12:32 GMT  
		Size: 9.8 MB (9791146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ec15c2966fb9478d83ca8223d737a15cce4dcafd6941855d5dbfba9499abda`  
		Last Modified: Tue, 25 Feb 2025 02:12:31 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17caa49083c23bf1b6258b5f521bcdef30dea63ef626ca68f8a6c8a9c8ffa6c`  
		Last Modified: Tue, 25 Feb 2025 02:12:32 GMT  
		Size: 10.0 MB (9992698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea3d66599ca732e1e8d24f1dee941ec8551d2e424986272c734de315744eb78`  
		Last Modified: Tue, 25 Feb 2025 02:12:31 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:06cb32b1bdca5f7733f19e3e147760769515e82d665f87e4126242e55c8bf379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2639590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebfea0e525999c864052603cebdc3ec85d148e873125542dad54a547bdf6575c`

```dockerfile
```

-	Layers:
	-	`sha256:69fc3a6518db6ca0c7c0cfdb01be3ea9616be48bcfa2bde77ea5b96ddc1658e2`  
		Last Modified: Tue, 25 Feb 2025 02:12:31 GMT  
		Size: 2.6 MB (2626143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df02e15a0109c63008f9b27a45dab2b3e39cf7e1bd186bae505a381038c5179e`  
		Last Modified: Tue, 25 Feb 2025 02:12:31 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:f78aa071f0d1986784d0734e4f6aca187b01f9bdddc529f7663effb475a87bec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (47002363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bddd5094e9eefbf9cefa6d94224b923858c5684c9f905a91f27de1904510c3ed`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
VOLUME [/data]
# Wed, 13 Dec 2023 22:17:20 GMT
WORKDIR /data
# Wed, 13 Dec 2023 22:17:20 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 13 Dec 2023 22:17:20 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5d165c25d7451c9dcf07a9ed0aebab022a0d75f8f8f81e94343e5dd79478c7`  
		Last Modified: Tue, 25 Feb 2025 05:20:07 GMT  
		Size: 9.6 MB (9588703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418aafa3fab2f0e02e2cf945212d3c04e3117174e2da17f27ef726e4bb06a449`  
		Last Modified: Tue, 25 Feb 2025 05:20:06 GMT  
		Size: 2.7 KB (2670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42eaaf95cee9126f51ab7f648ebb1f79df3efed41b9b1ec2ac66ca18ec9f7d17`  
		Last Modified: Tue, 25 Feb 2025 05:20:07 GMT  
		Size: 9.4 MB (9362472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7fd8d22a6e8a3606b1c185d1ea70744561f9009f9c1ff6700ec423979ef43b`  
		Last Modified: Tue, 25 Feb 2025 05:20:07 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:c8df483d3a69359595d9724c103c51c63fc9c658d6cdbf942f8c4218bab60b3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2640107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65163324ed50f22237a0c96005e6674d10004925bf5bffe9383ceea27d15868f`

```dockerfile
```

-	Layers:
	-	`sha256:a0a8cb0c84f1577669c5e4900ce368763752d40ac3247c268156920c4ce1a8fe`  
		Last Modified: Tue, 25 Feb 2025 05:20:07 GMT  
		Size: 2.6 MB (2626478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:127c182f093bcfa82d3a87faac1dcf614dc94fe9704ddb6a5c555ea1f66cfd06`  
		Last Modified: Tue, 25 Feb 2025 05:20:07 GMT  
		Size: 13.6 KB (13629 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:bookworm-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:c1f872f56e3430406ca144243774fa1ee65a921145d910893bb749a466bf794c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45460642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bee1e624859e0551dce079fdd377bcf580e425b1fc408c9005a41568eca43f28`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
VOLUME [/data]
# Wed, 13 Dec 2023 22:17:20 GMT
WORKDIR /data
# Wed, 13 Dec 2023 22:17:20 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 13 Dec 2023 22:17:20 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:6d4d169c55c2ee02478b6705c4ba9e6795bffbbb872a22adfd95fb2484f2e85c`  
		Last Modified: Tue, 25 Feb 2025 01:30:03 GMT  
		Size: 26.9 MB (26864838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c193b0b8173d098c5c2a8113e171e598fbb3313cd9de9835e280f9f5a78913a1`  
		Last Modified: Tue, 25 Feb 2025 03:54:17 GMT  
		Size: 9.3 MB (9289551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545654c9eaef2891057b4f30c67b6e107947fe014eed087c867a6e4e5e436399`  
		Last Modified: Tue, 25 Feb 2025 03:54:16 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30e055d4d969e6f02ec3556f25ea99f7b0cc711b11bc90a5fe3ccfd384ee23e`  
		Last Modified: Tue, 25 Feb 2025 03:54:16 GMT  
		Size: 9.3 MB (9303490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066fd5a1996c8a5ed90b83ecb54f1bcb81755c27d2ea351df05c05fd6a18b7df`  
		Last Modified: Tue, 25 Feb 2025 03:54:16 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:0007be8ff799b36de841ca32eb1da3d4ad64ba16901f7e6e300a72c77388b320
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2638684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf58c70ca29cfc2a1902f953c2b6493f3000b4c024f835cf281b7e91b01ed23a`

```dockerfile
```

-	Layers:
	-	`sha256:ccdd32c35657b65dcc8a7aacc2c8c90eb69524c27c0a2bc98b0c8392fc16adf6`  
		Last Modified: Tue, 25 Feb 2025 03:54:16 GMT  
		Size: 2.6 MB (2625237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0eed72a0ef024482db4e00572b4130012855b6516fbf87f52711832baa158191`  
		Last Modified: Tue, 25 Feb 2025 03:54:16 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json
