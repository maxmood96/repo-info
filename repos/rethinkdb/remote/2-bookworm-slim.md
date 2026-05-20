## `rethinkdb:2-bookworm-slim`

```console
$ docker pull rethinkdb@sha256:b49664e726021631386878c94052bd925a5afe5f84e03e91e36bbe964021ba43
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
$ docker pull rethinkdb@sha256:a4d3fe3c743474c7b9d63f51e296dbd532537a125c6ee5d76156c707fc75dc66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48031679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18fd74bf849199b35b7cecc44dfd78f1c462a865d14ada7b129d312f2884b5fc`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:17:40 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:17:41 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Tue, 19 May 2026 23:17:46 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Tue, 19 May 2026 23:17:46 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:17:46 GMT
VOLUME [/data]
# Tue, 19 May 2026 23:17:46 GMT
WORKDIR /data
# Tue, 19 May 2026 23:17:46 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 19 May 2026 23:17:46 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f35e2c931dcdc0a87410203196919245db68842bfa60de8b6405c720314b11`  
		Last Modified: Tue, 19 May 2026 23:17:53 GMT  
		Size: 9.8 MB (9802204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7213de8eecbe8577150188e0a33f9fae23f4360b22d2f87f66cf3409deb8adf`  
		Last Modified: Tue, 19 May 2026 23:17:53 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb0fbb4184efd641b9ef4fcc2510a88bd775bbdaa73606c7866a896188c456a`  
		Last Modified: Tue, 19 May 2026 23:17:54 GMT  
		Size: 10.0 MB (9993169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c260a3e376d69e7a3e79c3178b61a000e595c14148f0f943d9cddd1090396d`  
		Last Modified: Tue, 19 May 2026 23:17:53 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:45f086df9bf0dee5557b4aa6e66bc2efe3a49132d24d3a9cb160faa2e39e60b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:425c718c703d4c6a9359410fbbdb7aa52a72e85d71cb2b51c25774fe11ea369d`

```dockerfile
```

-	Layers:
	-	`sha256:5667db575cd64ded67351b0922f05d2026f2417b7fdb01182a8bad3bfb2e235f`  
		Last Modified: Tue, 19 May 2026 23:17:53 GMT  
		Size: 2.8 MB (2785064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbd6e03dd0b4667d8accdd00369afb225da200771190320e996003ac72ece093`  
		Last Modified: Tue, 19 May 2026 23:17:53 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:8ff7ccc889bb698b1d35e8048365d6ab6f56b23c912e142a0770f59672659cc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47111465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db64d53682fd336a0c8b8d9ab1a415a880807c5721f0b5de436009c8fe9ab6db`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:21:06 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:21:07 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Tue, 19 May 2026 23:21:13 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Tue, 19 May 2026 23:21:13 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:21:13 GMT
VOLUME [/data]
# Tue, 19 May 2026 23:21:13 GMT
WORKDIR /data
# Tue, 19 May 2026 23:21:13 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 19 May 2026 23:21:13 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a9c1a77aea29a4532909ff6050a4e82cb01ca98949723a4302b7aea4567b66`  
		Last Modified: Tue, 19 May 2026 23:21:21 GMT  
		Size: 9.6 MB (9630790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf32cefc21a9e873a6933a3eda46cdd63b59b9d0fc0a57a009ee4971ecaefee7`  
		Last Modified: Tue, 19 May 2026 23:21:21 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe4ac8114d144d8250f16a49f07efb1b4157904ee53d83a0a85e0e0b43f2c37`  
		Last Modified: Tue, 19 May 2026 23:21:21 GMT  
		Size: 9.4 MB (9362870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:761701a109a87b88bf991e77b8c3ac22db773b483c4070758361a1f30fa5d92e`  
		Last Modified: Tue, 19 May 2026 23:21:21 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:563dc9eee4c26176425d5509f79f07b3610598d679fbe018fa75f45db4de275d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c44d84b13f667182dbf4e36b11f07a055f17f051eda0e7b9788576f9d1716d7`

```dockerfile
```

-	Layers:
	-	`sha256:0cf7bb318664a0f80f1678d3f7c538b34da946d5001f644f6415a827e0c783b6`  
		Last Modified: Tue, 19 May 2026 23:21:21 GMT  
		Size: 2.8 MB (2785399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22c1bff2f030d64e5cd2b07f56064007cb6f15a76e6021b3c8a71628488f4bbb`  
		Last Modified: Tue, 19 May 2026 23:21:21 GMT  
		Size: 13.6 KB (13586 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2-bookworm-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:2461ac9365c6fb774b78f643d821f3ff2aedb16cc9b315e96343a916c5eb1624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45493621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b124ad6904159dffb01b4f04e29fad9168ca5c3ccacd39abfa1876e9cf70dcce`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:17:14 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:17:15 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Wed, 20 May 2026 00:17:20 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 20 May 2026 00:17:20 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:17:20 GMT
VOLUME [/data]
# Wed, 20 May 2026 00:17:20 GMT
WORKDIR /data
# Wed, 20 May 2026 00:17:20 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 20 May 2026 00:17:20 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:d5e0676594538bc23596fec84864fdfc1967950a13d798821e9073e432129029`  
		Last Modified: Tue, 19 May 2026 22:35:41 GMT  
		Size: 26.9 MB (26888597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b3169f84e6204e83cd3fdb622225d4c5389d65d65d5efff04605bfdbd6871a`  
		Last Modified: Wed, 20 May 2026 00:17:32 GMT  
		Size: 9.3 MB (9298402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85159b6f1ede355b6a5057345d44953e871e6a6940aed7a25d027e93bb5acb3e`  
		Last Modified: Wed, 20 May 2026 00:17:32 GMT  
		Size: 2.7 KB (2667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee7832967f22d386bf1e7283faae358436a83b0f24f9c0e27b59e331b7d802f`  
		Last Modified: Wed, 20 May 2026 00:17:32 GMT  
		Size: 9.3 MB (9303862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd6759a86e5090784a71eec42264275125363fda25ffad28c9085c0822134fb2`  
		Last Modified: Wed, 20 May 2026 00:17:32 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:78d2a077e142b03b1c24565eeaa923e0831edd3d9a8ff2564028feaddc2fbd15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2794665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:059f009e79f2b8d202f93cb5724c7185ed95652f013180bbe8a54792b2abcd77`

```dockerfile
```

-	Layers:
	-	`sha256:dadbcf3e2ffa551678467f3980ee57a3406380271f311b4e24116f6c310981e6`  
		Last Modified: Wed, 20 May 2026 00:17:32 GMT  
		Size: 2.8 MB (2781266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6654c2a5e60d1812cfcff85a4c3fda0b9025707d62699a0f64947fa11169eac4`  
		Last Modified: Wed, 20 May 2026 00:17:32 GMT  
		Size: 13.4 KB (13399 bytes)  
		MIME: application/vnd.in-toto+json
