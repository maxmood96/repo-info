## `rethinkdb:latest`

```console
$ docker pull rethinkdb@sha256:5e42b327bb0f0f7827c990a3df0c33b3dc5582920ff0716e31e1d07d7c8a3c7f
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
$ docker pull rethinkdb@sha256:a88a58b04a3aed7aadf2bfe275d730c09de213850a2d14c1d001c6d4e55d1c9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48035564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0fb57c5faf5454bbccd6406d61f8a60ca95f17e98c2149078b92aa7ec431138`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:36:32 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:36:33 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Thu, 11 Jun 2026 00:36:40 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Thu, 11 Jun 2026 00:36:40 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:36:40 GMT
VOLUME [/data]
# Thu, 11 Jun 2026 00:36:40 GMT
WORKDIR /data
# Thu, 11 Jun 2026 00:36:40 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 11 Jun 2026 00:36:40 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29fe5f1a0775c69bf4b7a78edb3db503861eb5f6f48a0290903e070e2dee705e`  
		Last Modified: Thu, 11 Jun 2026 00:36:47 GMT  
		Size: 9.8 MB (9802036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114fa85e38b8a2dac38c71e4768cd29c4c377969a9e02387f8c8a194beed4511`  
		Last Modified: Thu, 11 Jun 2026 00:36:47 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e16ece7ef445b902f10f060ad26bfc93a4685d59c8fd99922eae247f14ce1e57`  
		Last Modified: Thu, 11 Jun 2026 00:36:47 GMT  
		Size: 10.0 MB (9993143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db75ecef04765040707d404c4c7307e5d75bd04db7e8dc069ad3cd4d0992c3f`  
		Last Modified: Thu, 11 Jun 2026 00:36:47 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:latest` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:282f4f2919afcfda7fd8cf6a66044be0792dcfd9ae0353e5ab6e41a117bc36cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e4288476aed7416456dc27341e8324d865998bec379207bc02b4052ff18e62`

```dockerfile
```

-	Layers:
	-	`sha256:ae43310c6584553967004381749ba70b240733169020f777d343b6d8abbd3f6b`  
		Last Modified: Thu, 11 Jun 2026 00:36:47 GMT  
		Size: 2.8 MB (2785082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:258c52baa0ff6c2863ca7702c47c1164d35ce8d2578637cdb95f9701dc61c3bf`  
		Last Modified: Thu, 11 Jun 2026 00:36:47 GMT  
		Size: 13.4 KB (13403 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:latest` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:05b86de505e07b30bff107c8c207772b7c47e6e1bfb523dc99c3f7e721b408e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47118599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:654fd053bc361071bc49fef96e901e347b60f09b28b202c80a1d6c39ed45cdfb`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:38:17 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:38:18 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Thu, 11 Jun 2026 00:38:24 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Thu, 11 Jun 2026 00:38:24 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:38:24 GMT
VOLUME [/data]
# Thu, 11 Jun 2026 00:38:24 GMT
WORKDIR /data
# Thu, 11 Jun 2026 00:38:24 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 11 Jun 2026 00:38:24 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55aaff645a11d5fa5fcfda1d98fb205a640b2cafab63cd2d087a383cc72c134b`  
		Last Modified: Thu, 11 Jun 2026 00:38:31 GMT  
		Size: 9.6 MB (9630556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc1ad4818806115db88f0b2f22ec53c5bb9bdb26d9358e660eb061b0cafacbf`  
		Last Modified: Thu, 11 Jun 2026 00:38:31 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bea7c837919308294d551b99df5079bf2e4d2f20563740da0c328669f9148b`  
		Last Modified: Thu, 11 Jun 2026 00:38:31 GMT  
		Size: 9.4 MB (9362975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5174e0439566488086f78ae14d5e29730647945a2abcf7894dd180db9eef8898`  
		Last Modified: Thu, 11 Jun 2026 00:38:31 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:latest` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:fe2b6321a97a5c786cf61c97af965bb3629d5e774481bccff4ae19306ac9b6d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2799003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07cfaf105d30d639a803ee063384601ba08ef3c41ca7c0d1150e683598885ad2`

```dockerfile
```

-	Layers:
	-	`sha256:c12b022626c0eb5fd8cc3e9ac4051ab3d6a46d874a0f7065c84fee2e2e64ad60`  
		Last Modified: Thu, 11 Jun 2026 00:38:31 GMT  
		Size: 2.8 MB (2785417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72e6fcd588058b14d0d0e09b67c3711e6fce1c00721e84275532587281e39535`  
		Last Modified: Thu, 11 Jun 2026 00:38:31 GMT  
		Size: 13.6 KB (13586 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:latest` - linux; s390x

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

### `rethinkdb:latest` - unknown; unknown

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
