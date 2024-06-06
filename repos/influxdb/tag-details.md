<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `influxdb`

-	[`influxdb:1.10-data`](#influxdb110-data)
-	[`influxdb:1.10-data-alpine`](#influxdb110-data-alpine)
-	[`influxdb:1.10-meta`](#influxdb110-meta)
-	[`influxdb:1.10-meta-alpine`](#influxdb110-meta-alpine)
-	[`influxdb:1.10.7-data`](#influxdb1107-data)
-	[`influxdb:1.10.7-data-alpine`](#influxdb1107-data-alpine)
-	[`influxdb:1.10.7-meta`](#influxdb1107-meta)
-	[`influxdb:1.10.7-meta-alpine`](#influxdb1107-meta-alpine)
-	[`influxdb:1.11-data`](#influxdb111-data)
-	[`influxdb:1.11-data-alpine`](#influxdb111-data-alpine)
-	[`influxdb:1.11-meta`](#influxdb111-meta)
-	[`influxdb:1.11-meta-alpine`](#influxdb111-meta-alpine)
-	[`influxdb:1.11.5-data`](#influxdb1115-data)
-	[`influxdb:1.11.5-data-alpine`](#influxdb1115-data-alpine)
-	[`influxdb:1.11.5-meta`](#influxdb1115-meta)
-	[`influxdb:1.11.5-meta-alpine`](#influxdb1115-meta-alpine)
-	[`influxdb:1.8`](#influxdb18)
-	[`influxdb:1.8-alpine`](#influxdb18-alpine)
-	[`influxdb:1.8.10`](#influxdb1810)
-	[`influxdb:1.8.10-alpine`](#influxdb1810-alpine)
-	[`influxdb:1.9-data`](#influxdb19-data)
-	[`influxdb:1.9-data-alpine`](#influxdb19-data-alpine)
-	[`influxdb:1.9-meta`](#influxdb19-meta)
-	[`influxdb:1.9-meta-alpine`](#influxdb19-meta-alpine)
-	[`influxdb:1.9.13-data`](#influxdb1913-data)
-	[`influxdb:1.9.13-data-alpine`](#influxdb1913-data-alpine)
-	[`influxdb:1.9.13-meta`](#influxdb1913-meta)
-	[`influxdb:1.9.13-meta-alpine`](#influxdb1913-meta-alpine)
-	[`influxdb:2`](#influxdb2)
-	[`influxdb:2-alpine`](#influxdb2-alpine)
-	[`influxdb:2.7`](#influxdb27)
-	[`influxdb:2.7-alpine`](#influxdb27-alpine)
-	[`influxdb:2.7.6`](#influxdb276)
-	[`influxdb:2.7.6-alpine`](#influxdb276-alpine)
-	[`influxdb:alpine`](#influxdbalpine)
-	[`influxdb:latest`](#influxdblatest)

## `influxdb:1.10-data`

```console
$ docker pull influxdb@sha256:0ad0fe64637b6c2d4f2738bb8737af5f0da2482cead814d95ffea5a252eb7ff4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-data` - linux; amd64

```console
$ docker pull influxdb@sha256:81cc12ae235997253f05f7882f3d4dce442e86dfa25a7ff9c1959724617cd7be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112248371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33437447a3648ff7d8b0957ae8ba1f0c9f80eacf43a131525ca2962464a3c409`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Apr 2024 14:27:41 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=1.10.6-c1.10.6
# Tue, 30 Apr 2024 14:27:41 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f0bf643eb6745d5c7e9bada33de1786ab2350240206a1956fa506a1b47b129`  
		Last Modified: Tue, 14 May 2024 03:05:14 GMT  
		Size: 15.8 MB (15764867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eadca51f67d5ce7300aad704278ea61f7465fcf956c5304414d1c9bce14b2d8`  
		Last Modified: Tue, 14 May 2024 03:56:39 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63eb9fe06230278c66b1415cc26c412196a9a61380c02e3d97e8cfc66f8c175`  
		Last Modified: Tue, 14 May 2024 03:56:43 GMT  
		Size: 41.4 MB (41380557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af1d44333ea57b5ee6158f37fbdd4d2c42b64b8ac452403e575be0ec125c590`  
		Last Modified: Tue, 14 May 2024 03:56:42 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412cbf3548432b9f5fa8550ba9ea3f00035aa7ad855b4e748a432a5e5aa2ec92`  
		Last Modified: Tue, 14 May 2024 03:56:42 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6047a88c3dec65eb4ed97e46fc852e7d0abfa6a89751787e1619c282f8320ee`  
		Last Modified: Tue, 14 May 2024 03:56:42 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:0bcc39564e392b37f81528c82c661b7b11a2afad0e39dfac8fc50dcecffba69a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4594161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc143bff30b5262265b139a405c580691becd60333f353593b405a22648209b1`

```dockerfile
```

-	Layers:
	-	`sha256:4baeef9ebcc7410fc83be9cb439b080eb9ae609156843df2ddd8edcc46085af1`  
		Last Modified: Tue, 14 May 2024 03:56:42 GMT  
		Size: 4.6 MB (4579304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9caef871458ad755709447e9cb8dc78922d696a2b9413b11c2f54c4ae2cb1108`  
		Last Modified: Tue, 14 May 2024 03:56:42 GMT  
		Size: 14.9 KB (14857 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10-data-alpine`

```console
$ docker pull influxdb@sha256:8a7499e1532155d81ee0b5517b09f2ed5589fbf819cec8c2709cc0121fe46076
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:10b5ab29704a87488ecf6f03706076790d377b35b8787644bc114ad2138b7060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46200279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53a1fda40fcaeddddde539ad785cc9d68a87f1dfbd87892961d41135cfa7ded0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=1.10.6-c1.10.6
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd4bd2a4f26e2d834e8b8a307630862ab941dc0f22b55171d8ab6ab882174e9`  
		Last Modified: Wed, 01 May 2024 21:52:22 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0722703d5ed6c1a996bfa3511e9246cbfeeb3a55e29f8eb55e7060d929760958`  
		Last Modified: Wed, 01 May 2024 21:52:28 GMT  
		Size: 1.5 MB (1479556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d88aab8a5f52c39080d55b3a7f07d4f5aa5dfa6df5ecaedea59741d0309aed`  
		Last Modified: Wed, 01 May 2024 21:52:29 GMT  
		Size: 41.3 MB (41339265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f05010bf897ca5d4a251f4de7daa75f4c5fc7f1881ec93b8662e25ebb8b44d`  
		Last Modified: Wed, 01 May 2024 21:52:28 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80694f3969856d54e56c118148109d9f508c74ea6e1cebe94335d87d0475b958`  
		Last Modified: Wed, 01 May 2024 21:52:27 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a25b9c74b63ac6b2c55d7d7fd1cd6eb18c2584dc0fcbbd811fcddeadbdac63`  
		Last Modified: Wed, 01 May 2024 21:52:27 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:0ce2a1be9b5681545d847a22e81db16b5498957a8a7bc4a209639e98cf502c80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1124467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fc02df61bbfcb7e672af904a82452a933ce3b4741d79b940905e8388079f110`

```dockerfile
```

-	Layers:
	-	`sha256:7586086123d2969e880d5f4901021caa2b68be38f485e059d2860099f047f774`  
		Last Modified: Wed, 01 May 2024 21:52:28 GMT  
		Size: 1.1 MB (1107926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a14d7b024c600bae0f3dc1c03269a97c51ad8ec80a6a2962c89a8681f3a6e1cc`  
		Last Modified: Wed, 01 May 2024 21:52:28 GMT  
		Size: 16.5 KB (16541 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10-meta`

```console
$ docker pull influxdb@sha256:f1ba8d9027363efe3e7041ac872ecdeb23690c9c7872bb432e52dba3044d07b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:fa79793df228d84fc37a2c2899f5a540296e8e3f5e5b48e4b34be4cddb6f51a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.0 MB (90961782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cf2a74448a93d35d45e0282accdb6989b47b794758e3d5185fcd64647cdb7a5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 30 Apr 2024 14:27:41 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=1.10.6-c1.10.6
# Tue, 30 Apr 2024 14:27:41 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f0bf643eb6745d5c7e9bada33de1786ab2350240206a1956fa506a1b47b129`  
		Last Modified: Tue, 14 May 2024 03:05:14 GMT  
		Size: 15.8 MB (15764867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eadca51f67d5ce7300aad704278ea61f7465fcf956c5304414d1c9bce14b2d8`  
		Last Modified: Tue, 14 May 2024 03:56:39 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc9a2d73a8319bb972cd7882a9bc9e867b296b2355a7d7c85a9abf58decf70be`  
		Last Modified: Tue, 14 May 2024 03:56:38 GMT  
		Size: 20.1 MB (20095179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f67884c52fc4796d9915dc22b112cd6e30fe454db3e8b179cb21a0beb7cda30`  
		Last Modified: Tue, 14 May 2024 03:56:39 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80e27f78bddd3c6596fa12264e47149f9f645fe1e81d83e20b0cd78513941f6`  
		Last Modified: Tue, 14 May 2024 03:56:39 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:e7aa2cf6ec2c8d5fea6743f691df634d38c992fc206a3445cfd6a0366db97ca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4529393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:116f975fca59975e1be0102b7e730efc4bfc7944cdffe43628812b1a153894bd`

```dockerfile
```

-	Layers:
	-	`sha256:b3a04600972b5a78417875fe6dfd7e4974e48670b9bb15710e50f276ac6f2319`  
		Last Modified: Tue, 14 May 2024 03:56:38 GMT  
		Size: 4.5 MB (4516189 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a66624493d4394bd80e53d6fbd6496263cc9beb8c52b7702cc44dd3bc19f699`  
		Last Modified: Tue, 14 May 2024 03:56:38 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10-meta-alpine`

```console
$ docker pull influxdb@sha256:bd35703ab4676ad52a6860655c6ec97c8ae28a9950e0aa862e4eed0b104a455b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:334be1fea3426b1d8912b4b5207a24bce0669ba955300270b3effed0e42c5436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.9 MB (24916142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c2ae1ddf0b98fc1e9a34156b4c89b0dbf0b4fcc8f1c5e3dedc2b77aba3382f2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=1.10.6-c1.10.6
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aaf2c11393eef91a9b3651ad8396e0fe21609dc1fef68042a447e517a01c538`  
		Last Modified: Wed, 01 May 2024 21:52:25 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:affc145b25b016d97ae8324ed15d2b8027bceabced280ecbaaebbcbcb40c5ff2`  
		Last Modified: Wed, 01 May 2024 21:52:25 GMT  
		Size: 1.5 MB (1479561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70b3c9d35df3c9c446ca5c427d5eef9255bf2b01b2c1a7f003ee8ed04a9304c`  
		Last Modified: Wed, 01 May 2024 21:52:25 GMT  
		Size: 20.1 MB (20056335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a60f7861c794d7d1717011196ed0efe5c8240942b1c67a4c39fbe7ee4594762`  
		Last Modified: Wed, 01 May 2024 21:52:25 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e666991d2cc7bd4930756e2e2c08e65e88a3ebf76588d7e0009bb18d26a59e17`  
		Last Modified: Wed, 01 May 2024 21:52:26 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:b4e833fcd42b510fa6275df999980bb2a597051081a0246248f3a66bba8d8b8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1059979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd3869f575f402e412b4faa7995544a2e02d701f52a56daa596d50013afa2218`

```dockerfile
```

-	Layers:
	-	`sha256:029e8db012b08cbf9f75831e2f9460ba8d49646a625a7db4fb000f0b8842e1d6`  
		Last Modified: Wed, 01 May 2024 21:52:26 GMT  
		Size: 1.0 MB (1045073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:110215d8c6789e188c7ea81909e3a390bf53e8432dec0af04e362d47a4f58175`  
		Last Modified: Wed, 01 May 2024 21:52:25 GMT  
		Size: 14.9 KB (14906 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10.7-data`

**does not exist** (yet?)

## `influxdb:1.10.7-data-alpine`

**does not exist** (yet?)

## `influxdb:1.10.7-meta`

**does not exist** (yet?)

## `influxdb:1.10.7-meta-alpine`

**does not exist** (yet?)

## `influxdb:1.11-data`

```console
$ docker pull influxdb@sha256:e4738bae7e07731d8021aa1e3d9b67ebe1604032320c182afe1797ffae4d9bf6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data` - linux; amd64

```console
$ docker pull influxdb@sha256:396b122bc57838082f0c9c50caa455cdf4a3ab71205fb150f665c8391c3816a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115452727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c578a1439ccf19ef636bfe2506310f17f0c990f79f6a72fc4bc289215c73e04b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Apr 2024 14:27:41 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=1.11.5-c1.11.5
# Tue, 30 Apr 2024 14:27:41 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891494355808bdd3db5552f0d3723fd0fa826675f774853796fafa221d850d42`  
		Last Modified: Tue, 14 May 2024 03:04:06 GMT  
		Size: 24.1 MB (24050100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ab3e63aeb098cb04df62d1a671ef91577347b141c0afed6029c646d1ee17cd`  
		Last Modified: Tue, 14 May 2024 03:56:41 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4422712ed2e38978ccbbad0e732492b03763e1461ff3e1dd0efc24e7ed6adc`  
		Last Modified: Tue, 14 May 2024 03:56:42 GMT  
		Size: 41.8 MB (41822691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d34cae322d6039b1c8d60e1109a50ae47870846f6c178c6bb0dcbf90952c97c`  
		Last Modified: Tue, 14 May 2024 03:56:42 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b649fbdcc873553c85e08173b0fc28fd19b703061f172fbb873ac574e1188ba8`  
		Last Modified: Tue, 14 May 2024 03:56:42 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4992b44a9f8f9afa0d20ab67c8257c3f7ec014c6a96b2660a967dedc14cee06b`  
		Last Modified: Tue, 14 May 2024 03:56:43 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:4a662e21865900636fceff8228e3fe0878c17f75f25fd3599ed939484d7ba08c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4469402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ca4b5d995f781c366d487dbfa4d2e404d0a97d5be7ceb446c1e1a30d4d8b8e4`

```dockerfile
```

-	Layers:
	-	`sha256:0ebb41e17b2d1d7a0b88ae90d59f6b3fe845df951fa5bd2c35fb9073c570f0c1`  
		Last Modified: Tue, 14 May 2024 03:56:41 GMT  
		Size: 4.5 MB (4454545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3f6f52a9a4fafb7eb9f58a96837ed7a6e2e2e17405b4d0469c76155b1dfa287`  
		Last Modified: Tue, 14 May 2024 03:56:41 GMT  
		Size: 14.9 KB (14857 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-data-alpine`

```console
$ docker pull influxdb@sha256:6ad1cc471a2f039931f45d081768f1e852f2955aa59611ce16c42d642166c8ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:992d5e235b6ea4b16b92304938c69fb98c6ee823d8c9ab4feac33917e8a78dd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46598732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd1650fba374636f75f71052c2ca5e3d9524c42565b3e403ee0d93f43ec16dd6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=1.11.5-c1.11.5
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd4bd2a4f26e2d834e8b8a307630862ab941dc0f22b55171d8ab6ab882174e9`  
		Last Modified: Wed, 01 May 2024 21:52:22 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9367615c38660b609e090e894fdbc58854450aac2cc6058faab56823451266ff`  
		Last Modified: Wed, 01 May 2024 21:52:23 GMT  
		Size: 1.4 MB (1415699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf4ca7bcdf6aa1ea25ba6a9cbb1b93655b4ad6ee2dbb66c4a701c82ac131936`  
		Last Modified: Wed, 01 May 2024 21:52:27 GMT  
		Size: 41.8 MB (41778438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61584e90a9d0576f1e517993cc51948ea56096d337cdccc4c69fa71d10ae0a4e`  
		Last Modified: Wed, 01 May 2024 21:52:27 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80694f3969856d54e56c118148109d9f508c74ea6e1cebe94335d87d0475b958`  
		Last Modified: Wed, 01 May 2024 21:52:27 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a25b9c74b63ac6b2c55d7d7fd1cd6eb18c2584dc0fcbbd811fcddeadbdac63`  
		Last Modified: Wed, 01 May 2024 21:52:27 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:d4deb61d969c308281bccd69715892d206996241124e0af8623293c60fb4661c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1122464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea24aeff94aa23b8e5d62208e0897a74635c73ba278919dcded6e9a188275d88`

```dockerfile
```

-	Layers:
	-	`sha256:a7e90665d75611b426555b34cd7dd824b49e7619fa5221a5e3677c52dcb55419`  
		Last Modified: Wed, 01 May 2024 21:52:27 GMT  
		Size: 1.1 MB (1105923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0be69bdac5f38efb7d8b1216b82f200bbc7610c5b00a22983ebc0ffb8be6b907`  
		Last Modified: Wed, 01 May 2024 21:52:27 GMT  
		Size: 16.5 KB (16541 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-meta`

```console
$ docker pull influxdb@sha256:5adbcc41297a4f6274d6781d7edefaac60cca1c22c69a24532089e0421e01676
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:6ef52fcff737385be7bb91817b19e5fe8b4261fa96f2258fbc1207246364ab08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (94021903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20845487a4499950a137b8cdbe79e1a857867e8210d99fde3a6a4d6d69f0d09c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 30 Apr 2024 14:27:41 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=1.11.5-c1.11.5
# Tue, 30 Apr 2024 14:27:41 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891494355808bdd3db5552f0d3723fd0fa826675f774853796fafa221d850d42`  
		Last Modified: Tue, 14 May 2024 03:04:06 GMT  
		Size: 24.1 MB (24050100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70aa78fdc4ae88fa00f467b0649984f31203883a4ff67fca21758bfc02f74fec`  
		Last Modified: Tue, 14 May 2024 03:56:49 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247b9ef9f9974cba69a4250e68259f5461b8e657c365ee1fa4877120c38da105`  
		Last Modified: Tue, 14 May 2024 03:56:49 GMT  
		Size: 20.4 MB (20393062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91a4abc8ca4d47b49a0c48584e35bead63fa598533165b0456292d53cff79dc`  
		Last Modified: Tue, 14 May 2024 03:56:49 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4ba0f55440b96a76fd95b27125075874d80fcb3eaa7e3681f8eb010c5b2da5`  
		Last Modified: Tue, 14 May 2024 03:56:49 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:88c3c2f779042cd06a95341960ba9d278544efb4333846c7b8d03621d5a2b83d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4405189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5edb24620a80995be284169bcc39a7ae22a76c7a594c97fde4ae24e01f29962`

```dockerfile
```

-	Layers:
	-	`sha256:29a34f8477ed7b99e665a0118e5556d360f3f6e536184f7ed02bf47c7de0ce65`  
		Last Modified: Tue, 14 May 2024 03:56:49 GMT  
		Size: 4.4 MB (4391985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25d5e0872d5a6d42188d0089772983e97bab5ab0e8055f6ab5386e84ffe0df30`  
		Last Modified: Tue, 14 May 2024 03:56:49 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-meta-alpine`

```console
$ docker pull influxdb@sha256:8cf982543a730086a70714eb28e793001db23a1647062a4d0cccfca516d2acca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:dacd2110143b311a4c61cd5a048696cd3b0327f75701ad5433d88dc0c2151b31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25179753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d67e26bf34765d493cbbb64c9c1f7b9e1ee63cc30d1f7edc2774b7cc71320e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=1.11.5-c1.11.5
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd4bd2a4f26e2d834e8b8a307630862ab941dc0f22b55171d8ab6ab882174e9`  
		Last Modified: Wed, 01 May 2024 21:52:22 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9367615c38660b609e090e894fdbc58854450aac2cc6058faab56823451266ff`  
		Last Modified: Wed, 01 May 2024 21:52:23 GMT  
		Size: 1.4 MB (1415699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce91759131a1d95cbfb140d61d4547bb23752535f92cf15f07ca9ef6f61cb5d3`  
		Last Modified: Wed, 01 May 2024 21:52:23 GMT  
		Size: 20.4 MB (20360666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c65bcfeb136f5b80fe865367f52e7d6d57d1ac0311e456ed72309f31cc66521`  
		Last Modified: Wed, 01 May 2024 21:52:23 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d3ae9c193af70597f2b5ba871aec0d5cc55200a69a43a2db7cf77b6add50f8`  
		Last Modified: Wed, 01 May 2024 21:52:23 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:167c3c6814f96fd138615a5a220168024ce838f4c5d1e7ebdd33503c1bd5a690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1059162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ed478bc3e928e8b5e1dfcaae2982fa02bccf15a563cc518039dc60ca0c67df`

```dockerfile
```

-	Layers:
	-	`sha256:dbc034e317d0e9ee1d98a393c373b7fc601450bcd7ead190777fe7d66aa057b8`  
		Last Modified: Wed, 01 May 2024 21:52:23 GMT  
		Size: 1.0 MB (1044256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:797a630895c564d2b761a18880549f066ec59db4e9e46d436536cdeba619d9a7`  
		Last Modified: Wed, 01 May 2024 21:52:23 GMT  
		Size: 14.9 KB (14906 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.5-data`

```console
$ docker pull influxdb@sha256:e4738bae7e07731d8021aa1e3d9b67ebe1604032320c182afe1797ffae4d9bf6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.5-data` - linux; amd64

```console
$ docker pull influxdb@sha256:396b122bc57838082f0c9c50caa455cdf4a3ab71205fb150f665c8391c3816a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115452727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c578a1439ccf19ef636bfe2506310f17f0c990f79f6a72fc4bc289215c73e04b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Apr 2024 14:27:41 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=1.11.5-c1.11.5
# Tue, 30 Apr 2024 14:27:41 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891494355808bdd3db5552f0d3723fd0fa826675f774853796fafa221d850d42`  
		Last Modified: Tue, 14 May 2024 03:04:06 GMT  
		Size: 24.1 MB (24050100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ab3e63aeb098cb04df62d1a671ef91577347b141c0afed6029c646d1ee17cd`  
		Last Modified: Tue, 14 May 2024 03:56:41 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4422712ed2e38978ccbbad0e732492b03763e1461ff3e1dd0efc24e7ed6adc`  
		Last Modified: Tue, 14 May 2024 03:56:42 GMT  
		Size: 41.8 MB (41822691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d34cae322d6039b1c8d60e1109a50ae47870846f6c178c6bb0dcbf90952c97c`  
		Last Modified: Tue, 14 May 2024 03:56:42 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b649fbdcc873553c85e08173b0fc28fd19b703061f172fbb873ac574e1188ba8`  
		Last Modified: Tue, 14 May 2024 03:56:42 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4992b44a9f8f9afa0d20ab67c8257c3f7ec014c6a96b2660a967dedc14cee06b`  
		Last Modified: Tue, 14 May 2024 03:56:43 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.5-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:4a662e21865900636fceff8228e3fe0878c17f75f25fd3599ed939484d7ba08c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4469402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ca4b5d995f781c366d487dbfa4d2e404d0a97d5be7ceb446c1e1a30d4d8b8e4`

```dockerfile
```

-	Layers:
	-	`sha256:0ebb41e17b2d1d7a0b88ae90d59f6b3fe845df951fa5bd2c35fb9073c570f0c1`  
		Last Modified: Tue, 14 May 2024 03:56:41 GMT  
		Size: 4.5 MB (4454545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3f6f52a9a4fafb7eb9f58a96837ed7a6e2e2e17405b4d0469c76155b1dfa287`  
		Last Modified: Tue, 14 May 2024 03:56:41 GMT  
		Size: 14.9 KB (14857 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.5-data-alpine`

```console
$ docker pull influxdb@sha256:6ad1cc471a2f039931f45d081768f1e852f2955aa59611ce16c42d642166c8ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.5-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:992d5e235b6ea4b16b92304938c69fb98c6ee823d8c9ab4feac33917e8a78dd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46598732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd1650fba374636f75f71052c2ca5e3d9524c42565b3e403ee0d93f43ec16dd6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=1.11.5-c1.11.5
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd4bd2a4f26e2d834e8b8a307630862ab941dc0f22b55171d8ab6ab882174e9`  
		Last Modified: Wed, 01 May 2024 21:52:22 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9367615c38660b609e090e894fdbc58854450aac2cc6058faab56823451266ff`  
		Last Modified: Wed, 01 May 2024 21:52:23 GMT  
		Size: 1.4 MB (1415699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf4ca7bcdf6aa1ea25ba6a9cbb1b93655b4ad6ee2dbb66c4a701c82ac131936`  
		Last Modified: Wed, 01 May 2024 21:52:27 GMT  
		Size: 41.8 MB (41778438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61584e90a9d0576f1e517993cc51948ea56096d337cdccc4c69fa71d10ae0a4e`  
		Last Modified: Wed, 01 May 2024 21:52:27 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80694f3969856d54e56c118148109d9f508c74ea6e1cebe94335d87d0475b958`  
		Last Modified: Wed, 01 May 2024 21:52:27 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a25b9c74b63ac6b2c55d7d7fd1cd6eb18c2584dc0fcbbd811fcddeadbdac63`  
		Last Modified: Wed, 01 May 2024 21:52:27 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.5-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:d4deb61d969c308281bccd69715892d206996241124e0af8623293c60fb4661c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1122464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea24aeff94aa23b8e5d62208e0897a74635c73ba278919dcded6e9a188275d88`

```dockerfile
```

-	Layers:
	-	`sha256:a7e90665d75611b426555b34cd7dd824b49e7619fa5221a5e3677c52dcb55419`  
		Last Modified: Wed, 01 May 2024 21:52:27 GMT  
		Size: 1.1 MB (1105923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0be69bdac5f38efb7d8b1216b82f200bbc7610c5b00a22983ebc0ffb8be6b907`  
		Last Modified: Wed, 01 May 2024 21:52:27 GMT  
		Size: 16.5 KB (16541 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.5-meta`

```console
$ docker pull influxdb@sha256:5adbcc41297a4f6274d6781d7edefaac60cca1c22c69a24532089e0421e01676
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.5-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:6ef52fcff737385be7bb91817b19e5fe8b4261fa96f2258fbc1207246364ab08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (94021903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20845487a4499950a137b8cdbe79e1a857867e8210d99fde3a6a4d6d69f0d09c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 30 Apr 2024 14:27:41 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=1.11.5-c1.11.5
# Tue, 30 Apr 2024 14:27:41 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891494355808bdd3db5552f0d3723fd0fa826675f774853796fafa221d850d42`  
		Last Modified: Tue, 14 May 2024 03:04:06 GMT  
		Size: 24.1 MB (24050100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70aa78fdc4ae88fa00f467b0649984f31203883a4ff67fca21758bfc02f74fec`  
		Last Modified: Tue, 14 May 2024 03:56:49 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247b9ef9f9974cba69a4250e68259f5461b8e657c365ee1fa4877120c38da105`  
		Last Modified: Tue, 14 May 2024 03:56:49 GMT  
		Size: 20.4 MB (20393062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91a4abc8ca4d47b49a0c48584e35bead63fa598533165b0456292d53cff79dc`  
		Last Modified: Tue, 14 May 2024 03:56:49 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4ba0f55440b96a76fd95b27125075874d80fcb3eaa7e3681f8eb010c5b2da5`  
		Last Modified: Tue, 14 May 2024 03:56:49 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.5-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:88c3c2f779042cd06a95341960ba9d278544efb4333846c7b8d03621d5a2b83d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4405189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5edb24620a80995be284169bcc39a7ae22a76c7a594c97fde4ae24e01f29962`

```dockerfile
```

-	Layers:
	-	`sha256:29a34f8477ed7b99e665a0118e5556d360f3f6e536184f7ed02bf47c7de0ce65`  
		Last Modified: Tue, 14 May 2024 03:56:49 GMT  
		Size: 4.4 MB (4391985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25d5e0872d5a6d42188d0089772983e97bab5ab0e8055f6ab5386e84ffe0df30`  
		Last Modified: Tue, 14 May 2024 03:56:49 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.5-meta-alpine`

```console
$ docker pull influxdb@sha256:8cf982543a730086a70714eb28e793001db23a1647062a4d0cccfca516d2acca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.5-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:dacd2110143b311a4c61cd5a048696cd3b0327f75701ad5433d88dc0c2151b31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25179753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d67e26bf34765d493cbbb64c9c1f7b9e1ee63cc30d1f7edc2774b7cc71320e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=1.11.5-c1.11.5
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd4bd2a4f26e2d834e8b8a307630862ab941dc0f22b55171d8ab6ab882174e9`  
		Last Modified: Wed, 01 May 2024 21:52:22 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9367615c38660b609e090e894fdbc58854450aac2cc6058faab56823451266ff`  
		Last Modified: Wed, 01 May 2024 21:52:23 GMT  
		Size: 1.4 MB (1415699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce91759131a1d95cbfb140d61d4547bb23752535f92cf15f07ca9ef6f61cb5d3`  
		Last Modified: Wed, 01 May 2024 21:52:23 GMT  
		Size: 20.4 MB (20360666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c65bcfeb136f5b80fe865367f52e7d6d57d1ac0311e456ed72309f31cc66521`  
		Last Modified: Wed, 01 May 2024 21:52:23 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d3ae9c193af70597f2b5ba871aec0d5cc55200a69a43a2db7cf77b6add50f8`  
		Last Modified: Wed, 01 May 2024 21:52:23 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.5-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:167c3c6814f96fd138615a5a220168024ce838f4c5d1e7ebdd33503c1bd5a690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1059162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ed478bc3e928e8b5e1dfcaae2982fa02bccf15a563cc518039dc60ca0c67df`

```dockerfile
```

-	Layers:
	-	`sha256:dbc034e317d0e9ee1d98a393c373b7fc601450bcd7ead190777fe7d66aa057b8`  
		Last Modified: Wed, 01 May 2024 21:52:23 GMT  
		Size: 1.0 MB (1044256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:797a630895c564d2b761a18880549f066ec59db4e9e46d436536cdeba619d9a7`  
		Last Modified: Wed, 01 May 2024 21:52:23 GMT  
		Size: 14.9 KB (14906 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.8`

```console
$ docker pull influxdb@sha256:69e2de7972e79a58cd0d59c4342a97dcf8272fca7f043e74b06b5a4e9aacffd6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.8` - linux; amd64

```console
$ docker pull influxdb@sha256:3c2eda6f43015553442085945f92786c865c48e392bbf71996e7c340ac7c235a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125753099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:537feebce5de940bd0a65da5ae1a1aeedbcb8d17a74105e856d8b17309bfd348`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Apr 2024 14:27:41 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=1.8.10
# Tue, 30 Apr 2024 14:27:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb* # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f0bf643eb6745d5c7e9bada33de1786ab2350240206a1956fa506a1b47b129`  
		Last Modified: Tue, 14 May 2024 03:05:14 GMT  
		Size: 15.8 MB (15764867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c32c4d98fbd052f0f4a536efb88d9b2e144b4bf79cd4cd33df103e28f050341`  
		Last Modified: Tue, 14 May 2024 03:56:37 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98fd68546b20bcc44d227d891eed45a36fee3af68741f4e358df294472c56ca`  
		Last Modified: Tue, 14 May 2024 03:56:42 GMT  
		Size: 54.9 MB (54885342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb879554bc7565992b281513b1874d77404fee9cfd1f23e0a253ccfde4c829a`  
		Last Modified: Tue, 14 May 2024 03:56:41 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acea3ef2a6803c4c4c3dd03fad3c513b2a6715a6dfcf2725176e07d138cfc524`  
		Last Modified: Tue, 14 May 2024 03:56:41 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66dad3b6cf1fa9fce1e05e97e5ea30ce4c2ffabf7a5285a5f0d94d4e9a146299`  
		Last Modified: Tue, 14 May 2024 03:56:39 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:d2e4e27551f0dcc3f836861d4456444dda5e99dbec9247381a079211f4bb8373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4478769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41bda3e539751432f041b8a059c7ceb064e0b9acdebe33ad54060de59cf5fb86`

```dockerfile
```

-	Layers:
	-	`sha256:94852a45c0c70580f23297007e49b58e5c16f341b7407a7decf4abded16e1a0d`  
		Last Modified: Tue, 14 May 2024 03:56:41 GMT  
		Size: 4.5 MB (4463024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0319393364625e84382318325bf9b7431b34a7ad6026bbc00fe660794a97d8d`  
		Last Modified: Tue, 14 May 2024 03:56:41 GMT  
		Size: 15.7 KB (15745 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.8` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:1fc46b054f8c81da888270fba0697693d16a2cd30a77479b8f5d08aaa9cabe01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116753126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4669c4d757d9401f0fd074b47e6d64fa1e028fc65c56d7e2dd444d34414e028d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Apr 2024 14:27:41 GMT
ADD file:e0e66bc918a84b9ec6caaae1380270276be179a5864b6234a18c001b3e94f855 in / 
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=1.8.10
# Tue, 30 Apr 2024 14:27:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb* # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:ebc97a184476667a6a83dfc0759e34e05bc66d258ece39a010b6273982b4dc57`  
		Last Modified: Tue, 14 May 2024 01:13:05 GMT  
		Size: 50.3 MB (50256445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f46483bc34de5be97fb9e8af88e9cf41c36db4eecccc529cc7904ee92a32f72`  
		Last Modified: Tue, 14 May 2024 01:48:02 GMT  
		Size: 14.9 MB (14880295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd066b093a7746e74d25ea627a2111dd19654237a7257fcb7804c1c55759f18`  
		Last Modified: Wed, 15 May 2024 04:05:05 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240ac8c2f35d67a24105c27c457b8ccad3936782e3978c2fb8a41d451e41f971`  
		Last Modified: Wed, 15 May 2024 04:05:07 GMT  
		Size: 51.6 MB (51612889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b00daf20f0db2bc366545df978793f25f63b5f720a0766f1cb04d338c6567ea`  
		Last Modified: Wed, 15 May 2024 04:05:05 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a04ed8ed48519de3d21dd8d67f2119e44f4ee7c5a6333b9c7e05cf03226c3b0`  
		Last Modified: Wed, 15 May 2024 04:05:05 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1329fef7c177a249087af4e46f7868776731241795bb952ebc25ed76ffd0e13b`  
		Last Modified: Wed, 15 May 2024 04:05:06 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:7225b5dae545603b29e46fe36b369b54323d46aa7ede7f4ad7ca8a68afbd9ee9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4480470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba00583a69ab709e178f4aad21f42002659f078a8e37fd54e6594a21587b0734`

```dockerfile
```

-	Layers:
	-	`sha256:953e35f6df00210ebda97328ffed55daa4c94fcd75a64f6b9e09826c916d1a3b`  
		Last Modified: Wed, 15 May 2024 04:05:05 GMT  
		Size: 4.5 MB (4464658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b01ab423ffbd1a00409daa024818a6f6f13f05406c7ccce5856d3fe481234d06`  
		Last Modified: Wed, 15 May 2024 04:05:05 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:ed7da84d66ed893d1f4d9820705a34d0a97bff63951ad987fb7326503e862b19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120722918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c93cf83723c98b3e2dfe274145852bf0832a6cc49d31071abe2c84fbadbc1ef9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Apr 2024 14:27:41 GMT
ADD file:43721c605da3f74f0c3f71384780fc0e57e2478b88197672caaf4baa3eddab23 in / 
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=1.8.10
# Tue, 30 Apr 2024 14:27:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb* # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:078d9526cc72763b2db16388f6b511c18a73e3e7f9d229364b3b85a6b5277bc8`  
		Last Modified: Tue, 14 May 2024 00:43:13 GMT  
		Size: 53.7 MB (53738990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691cb555e773cb93573d3bc043d7cf17af1d4819163089dfddab3f4cc971718e`  
		Last Modified: Tue, 14 May 2024 01:53:53 GMT  
		Size: 15.8 MB (15750525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2262e06ef8042a165821b6784ae33c5d70f476d554cf389c6abc35d3570e1faf`  
		Last Modified: Wed, 15 May 2024 10:30:27 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a603a55186a716d56071f71438f076793c5d8aefe1b881a11bdad83d419208`  
		Last Modified: Wed, 15 May 2024 10:30:28 GMT  
		Size: 51.2 MB (51229901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa05cf835851cef9136db0277a84cfddcc6acc72210c7a9884fcea3917cfe8f`  
		Last Modified: Wed, 15 May 2024 10:30:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb02d2aa86c305a962f70559440d76b924eddd7d128782d05c05e021aa7badc0`  
		Last Modified: Wed, 15 May 2024 10:30:27 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d28f6f0235c6a370b10ff479d90afdd26203b3226a701751ba8d51c92a36c4`  
		Last Modified: Wed, 15 May 2024 10:30:28 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:b4e8bc875fcd8451323f2de3328b85365b042a482064d3ecd8ded999e7e62105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4478362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512c0d9b7fb0d29f2a3ae8b900791181ec77f15ef9a3616bcb22ee46ac337d61`

```dockerfile
```

-	Layers:
	-	`sha256:1f78ed01a2f50b1b70184c27144ec58fef1019247b5741b9be13eeb4227d6887`  
		Last Modified: Wed, 15 May 2024 10:30:27 GMT  
		Size: 4.5 MB (4462611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4def6cfd8269618f707e147179c0e05a5c749d69d6eb72f8391c05968378ab3`  
		Last Modified: Wed, 15 May 2024 10:30:27 GMT  
		Size: 15.8 KB (15751 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.8-alpine`

```console
$ docker pull influxdb@sha256:ff68a78c2613757cc137ec48f7a862c6edb0f5a6a1e3fc52d604cb3e036ddd0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.8-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:8da7b4c9ea4e1290de176a2bc593b08de1c53e678db9858a49c3d8754e4fdfc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59507670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65603081c7d10c6afa775ed78364a34f726d21ef37ef8c6c58e28410b3886a4a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=1.8.10
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     chmod +x /usr/src/influxdb-*/influx              /usr/src/influxdb-*/influx_inspect              /usr/src/influxdb-*/influx_stress              /usr/src/influxdb-*/influxd &&    mv /usr/src/influxdb-*/influx        /usr/src/influxdb-*/influx_inspect        /usr/src/influxdb-*/influx_stress         /usr/src/influxdb-*/influxd        /usr/bin/ &&    gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d66e26ed51acf4d96c08bb777b841268e106a7712b3862519b5d7507d4f189`  
		Last Modified: Wed, 01 May 2024 21:52:30 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f1f494dad6160af22c1dc31566a1be8f66250e86a9a9ffcdfbf66c4721973d`  
		Last Modified: Wed, 01 May 2024 21:52:31 GMT  
		Size: 1.5 MB (1479571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead4cfe8a0866f27bab617e5f96f856f1e54bc3c33772f0166fd144e546954d4`  
		Last Modified: Wed, 01 May 2024 21:52:32 GMT  
		Size: 54.6 MB (54646698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba6dd6e0aa4ab870a6f13c45453e45ed0884669946fea824deba36caf1f1f81`  
		Last Modified: Wed, 01 May 2024 21:52:31 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50167d227c71947421041efc1934d2c71aa0be90637fabd044b4649e9b57e25f`  
		Last Modified: Wed, 01 May 2024 21:52:32 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09888d5454928396ab82fa3ccd4f6acfe5853a7f21ef57cbb36fd2cf15fe4632`  
		Last Modified: Wed, 01 May 2024 21:52:32 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:004a0352a5399a0749e2871e2f4a07d65d4623992bf220a1734b7bc140c399dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1001318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dfc61e7b8b3073e626ae1040b147a7bf23356fb904652d854e8d2db80126c42`

```dockerfile
```

-	Layers:
	-	`sha256:a34439932d7458286af23f31a01a9f738f9b8afd789a17d697f9eec6f18e02ff`  
		Last Modified: Wed, 01 May 2024 21:52:31 GMT  
		Size: 983.8 KB (983839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96000468ba486d74f19b0155419e78110d366cf9dba2ea7bf86c977c1475c321`  
		Last Modified: Wed, 01 May 2024 21:52:31 GMT  
		Size: 17.5 KB (17479 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.8.10`

```console
$ docker pull influxdb@sha256:69e2de7972e79a58cd0d59c4342a97dcf8272fca7f043e74b06b5a4e9aacffd6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.8.10` - linux; amd64

```console
$ docker pull influxdb@sha256:3c2eda6f43015553442085945f92786c865c48e392bbf71996e7c340ac7c235a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125753099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:537feebce5de940bd0a65da5ae1a1aeedbcb8d17a74105e856d8b17309bfd348`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Apr 2024 14:27:41 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=1.8.10
# Tue, 30 Apr 2024 14:27:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb* # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f0bf643eb6745d5c7e9bada33de1786ab2350240206a1956fa506a1b47b129`  
		Last Modified: Tue, 14 May 2024 03:05:14 GMT  
		Size: 15.8 MB (15764867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c32c4d98fbd052f0f4a536efb88d9b2e144b4bf79cd4cd33df103e28f050341`  
		Last Modified: Tue, 14 May 2024 03:56:37 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98fd68546b20bcc44d227d891eed45a36fee3af68741f4e358df294472c56ca`  
		Last Modified: Tue, 14 May 2024 03:56:42 GMT  
		Size: 54.9 MB (54885342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb879554bc7565992b281513b1874d77404fee9cfd1f23e0a253ccfde4c829a`  
		Last Modified: Tue, 14 May 2024 03:56:41 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acea3ef2a6803c4c4c3dd03fad3c513b2a6715a6dfcf2725176e07d138cfc524`  
		Last Modified: Tue, 14 May 2024 03:56:41 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66dad3b6cf1fa9fce1e05e97e5ea30ce4c2ffabf7a5285a5f0d94d4e9a146299`  
		Last Modified: Tue, 14 May 2024 03:56:39 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8.10` - unknown; unknown

```console
$ docker pull influxdb@sha256:d2e4e27551f0dcc3f836861d4456444dda5e99dbec9247381a079211f4bb8373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4478769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41bda3e539751432f041b8a059c7ceb064e0b9acdebe33ad54060de59cf5fb86`

```dockerfile
```

-	Layers:
	-	`sha256:94852a45c0c70580f23297007e49b58e5c16f341b7407a7decf4abded16e1a0d`  
		Last Modified: Tue, 14 May 2024 03:56:41 GMT  
		Size: 4.5 MB (4463024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0319393364625e84382318325bf9b7431b34a7ad6026bbc00fe660794a97d8d`  
		Last Modified: Tue, 14 May 2024 03:56:41 GMT  
		Size: 15.7 KB (15745 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.8.10` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:1fc46b054f8c81da888270fba0697693d16a2cd30a77479b8f5d08aaa9cabe01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116753126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4669c4d757d9401f0fd074b47e6d64fa1e028fc65c56d7e2dd444d34414e028d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Apr 2024 14:27:41 GMT
ADD file:e0e66bc918a84b9ec6caaae1380270276be179a5864b6234a18c001b3e94f855 in / 
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=1.8.10
# Tue, 30 Apr 2024 14:27:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb* # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:ebc97a184476667a6a83dfc0759e34e05bc66d258ece39a010b6273982b4dc57`  
		Last Modified: Tue, 14 May 2024 01:13:05 GMT  
		Size: 50.3 MB (50256445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f46483bc34de5be97fb9e8af88e9cf41c36db4eecccc529cc7904ee92a32f72`  
		Last Modified: Tue, 14 May 2024 01:48:02 GMT  
		Size: 14.9 MB (14880295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd066b093a7746e74d25ea627a2111dd19654237a7257fcb7804c1c55759f18`  
		Last Modified: Wed, 15 May 2024 04:05:05 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240ac8c2f35d67a24105c27c457b8ccad3936782e3978c2fb8a41d451e41f971`  
		Last Modified: Wed, 15 May 2024 04:05:07 GMT  
		Size: 51.6 MB (51612889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b00daf20f0db2bc366545df978793f25f63b5f720a0766f1cb04d338c6567ea`  
		Last Modified: Wed, 15 May 2024 04:05:05 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a04ed8ed48519de3d21dd8d67f2119e44f4ee7c5a6333b9c7e05cf03226c3b0`  
		Last Modified: Wed, 15 May 2024 04:05:05 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1329fef7c177a249087af4e46f7868776731241795bb952ebc25ed76ffd0e13b`  
		Last Modified: Wed, 15 May 2024 04:05:06 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8.10` - unknown; unknown

```console
$ docker pull influxdb@sha256:7225b5dae545603b29e46fe36b369b54323d46aa7ede7f4ad7ca8a68afbd9ee9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4480470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba00583a69ab709e178f4aad21f42002659f078a8e37fd54e6594a21587b0734`

```dockerfile
```

-	Layers:
	-	`sha256:953e35f6df00210ebda97328ffed55daa4c94fcd75a64f6b9e09826c916d1a3b`  
		Last Modified: Wed, 15 May 2024 04:05:05 GMT  
		Size: 4.5 MB (4464658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b01ab423ffbd1a00409daa024818a6f6f13f05406c7ccce5856d3fe481234d06`  
		Last Modified: Wed, 15 May 2024 04:05:05 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.8.10` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:ed7da84d66ed893d1f4d9820705a34d0a97bff63951ad987fb7326503e862b19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120722918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c93cf83723c98b3e2dfe274145852bf0832a6cc49d31071abe2c84fbadbc1ef9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Apr 2024 14:27:41 GMT
ADD file:43721c605da3f74f0c3f71384780fc0e57e2478b88197672caaf4baa3eddab23 in / 
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=1.8.10
# Tue, 30 Apr 2024 14:27:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb* # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:078d9526cc72763b2db16388f6b511c18a73e3e7f9d229364b3b85a6b5277bc8`  
		Last Modified: Tue, 14 May 2024 00:43:13 GMT  
		Size: 53.7 MB (53738990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691cb555e773cb93573d3bc043d7cf17af1d4819163089dfddab3f4cc971718e`  
		Last Modified: Tue, 14 May 2024 01:53:53 GMT  
		Size: 15.8 MB (15750525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2262e06ef8042a165821b6784ae33c5d70f476d554cf389c6abc35d3570e1faf`  
		Last Modified: Wed, 15 May 2024 10:30:27 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a603a55186a716d56071f71438f076793c5d8aefe1b881a11bdad83d419208`  
		Last Modified: Wed, 15 May 2024 10:30:28 GMT  
		Size: 51.2 MB (51229901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa05cf835851cef9136db0277a84cfddcc6acc72210c7a9884fcea3917cfe8f`  
		Last Modified: Wed, 15 May 2024 10:30:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb02d2aa86c305a962f70559440d76b924eddd7d128782d05c05e021aa7badc0`  
		Last Modified: Wed, 15 May 2024 10:30:27 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d28f6f0235c6a370b10ff479d90afdd26203b3226a701751ba8d51c92a36c4`  
		Last Modified: Wed, 15 May 2024 10:30:28 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8.10` - unknown; unknown

```console
$ docker pull influxdb@sha256:b4e8bc875fcd8451323f2de3328b85365b042a482064d3ecd8ded999e7e62105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4478362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512c0d9b7fb0d29f2a3ae8b900791181ec77f15ef9a3616bcb22ee46ac337d61`

```dockerfile
```

-	Layers:
	-	`sha256:1f78ed01a2f50b1b70184c27144ec58fef1019247b5741b9be13eeb4227d6887`  
		Last Modified: Wed, 15 May 2024 10:30:27 GMT  
		Size: 4.5 MB (4462611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4def6cfd8269618f707e147179c0e05a5c749d69d6eb72f8391c05968378ab3`  
		Last Modified: Wed, 15 May 2024 10:30:27 GMT  
		Size: 15.8 KB (15751 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.8.10-alpine`

```console
$ docker pull influxdb@sha256:ff68a78c2613757cc137ec48f7a862c6edb0f5a6a1e3fc52d604cb3e036ddd0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.8.10-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:8da7b4c9ea4e1290de176a2bc593b08de1c53e678db9858a49c3d8754e4fdfc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59507670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65603081c7d10c6afa775ed78364a34f726d21ef37ef8c6c58e28410b3886a4a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=1.8.10
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     chmod +x /usr/src/influxdb-*/influx              /usr/src/influxdb-*/influx_inspect              /usr/src/influxdb-*/influx_stress              /usr/src/influxdb-*/influxd &&    mv /usr/src/influxdb-*/influx        /usr/src/influxdb-*/influx_inspect        /usr/src/influxdb-*/influx_stress         /usr/src/influxdb-*/influxd        /usr/bin/ &&    gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d66e26ed51acf4d96c08bb777b841268e106a7712b3862519b5d7507d4f189`  
		Last Modified: Wed, 01 May 2024 21:52:30 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f1f494dad6160af22c1dc31566a1be8f66250e86a9a9ffcdfbf66c4721973d`  
		Last Modified: Wed, 01 May 2024 21:52:31 GMT  
		Size: 1.5 MB (1479571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead4cfe8a0866f27bab617e5f96f856f1e54bc3c33772f0166fd144e546954d4`  
		Last Modified: Wed, 01 May 2024 21:52:32 GMT  
		Size: 54.6 MB (54646698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba6dd6e0aa4ab870a6f13c45453e45ed0884669946fea824deba36caf1f1f81`  
		Last Modified: Wed, 01 May 2024 21:52:31 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50167d227c71947421041efc1934d2c71aa0be90637fabd044b4649e9b57e25f`  
		Last Modified: Wed, 01 May 2024 21:52:32 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09888d5454928396ab82fa3ccd4f6acfe5853a7f21ef57cbb36fd2cf15fe4632`  
		Last Modified: Wed, 01 May 2024 21:52:32 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8.10-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:004a0352a5399a0749e2871e2f4a07d65d4623992bf220a1734b7bc140c399dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1001318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dfc61e7b8b3073e626ae1040b147a7bf23356fb904652d854e8d2db80126c42`

```dockerfile
```

-	Layers:
	-	`sha256:a34439932d7458286af23f31a01a9f738f9b8afd789a17d697f9eec6f18e02ff`  
		Last Modified: Wed, 01 May 2024 21:52:31 GMT  
		Size: 983.8 KB (983839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96000468ba486d74f19b0155419e78110d366cf9dba2ea7bf86c977c1475c321`  
		Last Modified: Wed, 01 May 2024 21:52:31 GMT  
		Size: 17.5 KB (17479 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.9-data`

```console
$ docker pull influxdb@sha256:7e10ad79a8651d64f63f54fe9f88f9493ca08a32751af6ce226a062d8435d9da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9-data` - linux; amd64

```console
$ docker pull influxdb@sha256:97f42220f0690f2794acffd5969809695c6e382d0d6dcec5856ef1c4384d949e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 MB (104156782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6611bfa4aa15c73bda80038fac5370eafd763bdbbfecd83c677c9a795e010d5a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Apr 2024 14:27:41 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Tue, 30 Apr 2024 14:27:41 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb* # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f0bf643eb6745d5c7e9bada33de1786ab2350240206a1956fa506a1b47b129`  
		Last Modified: Tue, 14 May 2024 03:05:14 GMT  
		Size: 15.8 MB (15764867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c32c4d98fbd052f0f4a536efb88d9b2e144b4bf79cd4cd33df103e28f050341`  
		Last Modified: Tue, 14 May 2024 03:56:37 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a111da990975546bc1bc10a4f3a2f3fc9aed6e72b04c956f60022f23c57c0e4d`  
		Last Modified: Tue, 14 May 2024 03:56:38 GMT  
		Size: 33.3 MB (33288968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c576a03d546526c7fa9ddbd91a423bb7fa7ae9e9d2efd283b823f879cfcd03`  
		Last Modified: Tue, 14 May 2024 03:56:38 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a95386436e7bc24e7c1bc7a1ea073da71f18baace1f0d3ad15b7146d5b8280`  
		Last Modified: Tue, 14 May 2024 03:56:38 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66dad3b6cf1fa9fce1e05e97e5ea30ce4c2ffabf7a5285a5f0d94d4e9a146299`  
		Last Modified: Tue, 14 May 2024 03:56:39 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:dd381bfd53f5fe143e8f84744ff5b8d59cc52efdb5200baac1cf914311ae7321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4584852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4563fe0dd49891093819431100b74d9f46668fb32ab02c6e2420be699231b1d`

```dockerfile
```

-	Layers:
	-	`sha256:7f7d78ef7b467d8de8dc1259a340005af876ee8a55c109b013d499a6374bf522`  
		Last Modified: Tue, 14 May 2024 03:56:38 GMT  
		Size: 4.6 MB (4570028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e6f79ae8daae8946fb6f7554932337202306ff4b540224418a6ad96b3eb94a3`  
		Last Modified: Tue, 14 May 2024 03:56:37 GMT  
		Size: 14.8 KB (14824 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.9-data-alpine`

```console
$ docker pull influxdb@sha256:15d7365e6227e9431db5579e8f141482364c3046af6a1d6be52af335fcbafc07
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:9a0c681e6b278f2e194fbe5452b3459f922d3cb3f2a6d31bfbb90a714ade5e23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 MB (38109822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffbab36ed44522c8d2dec80d16a7ed5a4ffd9e6a44a84054eef7fe7e9637b391`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/etc/influxdb/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a317c2aa42265d50e848acb3635467a3773abf72ae2c7c2b504afe418a10834`  
		Last Modified: Wed, 01 May 2024 21:52:18 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e369ee0d89881d654f2528406cf92ff7a8d541ba7266124369ec2bd44d4c0634`  
		Last Modified: Wed, 01 May 2024 21:52:19 GMT  
		Size: 1.5 MB (1479528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db38a39344c06c8e1a02dbbf4a37994d0eee0ed0b6f584d8b60956915632f20`  
		Last Modified: Wed, 01 May 2024 21:52:19 GMT  
		Size: 33.2 MB (33248839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ae21f968fc95d3825832158c8041d2855e592424710eaf8b5c0b885652f9bc`  
		Last Modified: Wed, 01 May 2024 21:52:18 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483336b199da361cc41931239143ff402ef984b7f73c096c0477f984749bd073`  
		Last Modified: Wed, 01 May 2024 21:52:19 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7b27961f871f2793f18147681fef6f317a0770678efdbb10fb5bea9520dddf`  
		Last Modified: Wed, 01 May 2024 21:52:19 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:cb120e160467668a6e67f9f7b4c95a286948b5ed2166e8aab1294f5bc0c4b26d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1115209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47692d0f47733e5825af244b172ca4816fb810d11cb8b4db2cbefaf8fd3e3a94`

```dockerfile
```

-	Layers:
	-	`sha256:e67d6e6010f71f6a83aa9d1ce76511d4d3203364f25080bd6d2f637a58678ce0`  
		Last Modified: Wed, 01 May 2024 21:52:18 GMT  
		Size: 1.1 MB (1098644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c01e8a120720019fadacc05b56d4022f3247730ee5b0c399b93e61f30bf2151`  
		Last Modified: Wed, 01 May 2024 21:52:18 GMT  
		Size: 16.6 KB (16565 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.9-meta`

```console
$ docker pull influxdb@sha256:c3607c2f3d1b6099f581a0dde16ac6f2669758c9be06650518ad6b951d9a4793
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:1c6db348aa5e0a6e8c96f62637cf064d18658305b78fc6d2091985603677c9ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83635954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a42077e4565d830f6f6b1565dea4dd8768bffd2688e1c4afbc11eeaffeafc46`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 30 Apr 2024 14:27:41 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Tue, 30 Apr 2024 14:27:41 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb* # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f0bf643eb6745d5c7e9bada33de1786ab2350240206a1956fa506a1b47b129`  
		Last Modified: Tue, 14 May 2024 03:05:14 GMT  
		Size: 15.8 MB (15764867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d12b6386edc3e1f7267ca5eb78e3e41301565e13961ae3f097f2966aea7b9c`  
		Last Modified: Tue, 14 May 2024 03:56:39 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5d290cbc8de21b69b5060ba892a6a3893120cea672eb5fc88f33b3ffe83ba7`  
		Last Modified: Tue, 14 May 2024 03:56:39 GMT  
		Size: 12.8 MB (12769341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8b6c9160b18e279509b69a2da837b4e09a0c750a52d323ec895e85cf4946f9`  
		Last Modified: Tue, 14 May 2024 03:56:39 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150129c5d1c54477fe7e3d295afa7b641550cca2a85309a43e0ad15be212a3ca`  
		Last Modified: Tue, 14 May 2024 03:56:39 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:cd1b913219b59b453fee4ac14a3603bd0da40d3f2176e116751e0306c8439298
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4529328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a622b0300987377f3f54d5fdc7fa8c38a9ab16e8c371ecd077b642766931991a`

```dockerfile
```

-	Layers:
	-	`sha256:0fbecbae89f9acdce5047e8ad154544466b19a39115aa400959523fa352cc9d9`  
		Last Modified: Tue, 14 May 2024 03:56:39 GMT  
		Size: 4.5 MB (4516157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0d64448b12a4ede0b3a702a74aaf5c9e40c52b2753d0a8f11c975818d8eac54`  
		Last Modified: Tue, 14 May 2024 03:56:39 GMT  
		Size: 13.2 KB (13171 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.9-meta-alpine`

```console
$ docker pull influxdb@sha256:66ab261719e1c0f01be6b23d4ca528e818496d523e9af571697aa1c5e041c4ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:ccc210b1156d33adb71f2555b6401a8a874308fe4317ab4f3afa532bfd695490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17594177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:521c8e538680a350a503444fd7a8cca096c7c546e65cde39b3a2a66f58ea2fb5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/etc/influxdb/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b28eadf388e599b4a13053167aacec5d9b8f04bd20e51802d5c5b0cc30017b`  
		Last Modified: Wed, 01 May 2024 21:52:19 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1cb261ee6b33db5c86f4f909edf59330c7b0f42f3b655b661b1b44b56a87617`  
		Last Modified: Wed, 01 May 2024 21:52:20 GMT  
		Size: 1.5 MB (1479564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8c2464ec800e8abaaacf6c7dfb9535113e1db1c9be7aed5dac73111de19a0e`  
		Last Modified: Wed, 01 May 2024 21:52:20 GMT  
		Size: 12.7 MB (12734364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc30d67c3f256925019c3b7ca48a85f7c43473542efd57a6193cc4e839d6ae60`  
		Last Modified: Wed, 01 May 2024 21:52:20 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f59dc2b609146f1f6ea066534b0f0b6d73bffdbf440a5fafa9d3a0806a98552`  
		Last Modified: Wed, 01 May 2024 21:52:20 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:051fd69588801e89446bbdc9a116814b5bab9fac69cf3867c763df3f5c2b3809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1059939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d43a3e82c6fc2f141e49c1301ca99d11805eb01b166816a2c7800be951496027`

```dockerfile
```

-	Layers:
	-	`sha256:5e1b23b87a9a4da70821a1a29956402e72b414f37f5aa6798340755f5cb43870`  
		Last Modified: Wed, 01 May 2024 21:52:19 GMT  
		Size: 1.0 MB (1045009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a07320f6996a26b1b970f5db94262aff1faaf31a056a74d47cc443c21622428`  
		Last Modified: Wed, 01 May 2024 21:52:20 GMT  
		Size: 14.9 KB (14930 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.9.13-data`

```console
$ docker pull influxdb@sha256:7e10ad79a8651d64f63f54fe9f88f9493ca08a32751af6ce226a062d8435d9da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9.13-data` - linux; amd64

```console
$ docker pull influxdb@sha256:97f42220f0690f2794acffd5969809695c6e382d0d6dcec5856ef1c4384d949e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 MB (104156782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6611bfa4aa15c73bda80038fac5370eafd763bdbbfecd83c677c9a795e010d5a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Apr 2024 14:27:41 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Tue, 30 Apr 2024 14:27:41 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb* # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f0bf643eb6745d5c7e9bada33de1786ab2350240206a1956fa506a1b47b129`  
		Last Modified: Tue, 14 May 2024 03:05:14 GMT  
		Size: 15.8 MB (15764867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c32c4d98fbd052f0f4a536efb88d9b2e144b4bf79cd4cd33df103e28f050341`  
		Last Modified: Tue, 14 May 2024 03:56:37 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a111da990975546bc1bc10a4f3a2f3fc9aed6e72b04c956f60022f23c57c0e4d`  
		Last Modified: Tue, 14 May 2024 03:56:38 GMT  
		Size: 33.3 MB (33288968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c576a03d546526c7fa9ddbd91a423bb7fa7ae9e9d2efd283b823f879cfcd03`  
		Last Modified: Tue, 14 May 2024 03:56:38 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a95386436e7bc24e7c1bc7a1ea073da71f18baace1f0d3ad15b7146d5b8280`  
		Last Modified: Tue, 14 May 2024 03:56:38 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66dad3b6cf1fa9fce1e05e97e5ea30ce4c2ffabf7a5285a5f0d94d4e9a146299`  
		Last Modified: Tue, 14 May 2024 03:56:39 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9.13-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:dd381bfd53f5fe143e8f84744ff5b8d59cc52efdb5200baac1cf914311ae7321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4584852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4563fe0dd49891093819431100b74d9f46668fb32ab02c6e2420be699231b1d`

```dockerfile
```

-	Layers:
	-	`sha256:7f7d78ef7b467d8de8dc1259a340005af876ee8a55c109b013d499a6374bf522`  
		Last Modified: Tue, 14 May 2024 03:56:38 GMT  
		Size: 4.6 MB (4570028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e6f79ae8daae8946fb6f7554932337202306ff4b540224418a6ad96b3eb94a3`  
		Last Modified: Tue, 14 May 2024 03:56:37 GMT  
		Size: 14.8 KB (14824 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.9.13-data-alpine`

```console
$ docker pull influxdb@sha256:15d7365e6227e9431db5579e8f141482364c3046af6a1d6be52af335fcbafc07
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9.13-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:9a0c681e6b278f2e194fbe5452b3459f922d3cb3f2a6d31bfbb90a714ade5e23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 MB (38109822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffbab36ed44522c8d2dec80d16a7ed5a4ffd9e6a44a84054eef7fe7e9637b391`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/etc/influxdb/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a317c2aa42265d50e848acb3635467a3773abf72ae2c7c2b504afe418a10834`  
		Last Modified: Wed, 01 May 2024 21:52:18 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e369ee0d89881d654f2528406cf92ff7a8d541ba7266124369ec2bd44d4c0634`  
		Last Modified: Wed, 01 May 2024 21:52:19 GMT  
		Size: 1.5 MB (1479528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db38a39344c06c8e1a02dbbf4a37994d0eee0ed0b6f584d8b60956915632f20`  
		Last Modified: Wed, 01 May 2024 21:52:19 GMT  
		Size: 33.2 MB (33248839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ae21f968fc95d3825832158c8041d2855e592424710eaf8b5c0b885652f9bc`  
		Last Modified: Wed, 01 May 2024 21:52:18 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483336b199da361cc41931239143ff402ef984b7f73c096c0477f984749bd073`  
		Last Modified: Wed, 01 May 2024 21:52:19 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7b27961f871f2793f18147681fef6f317a0770678efdbb10fb5bea9520dddf`  
		Last Modified: Wed, 01 May 2024 21:52:19 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9.13-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:cb120e160467668a6e67f9f7b4c95a286948b5ed2166e8aab1294f5bc0c4b26d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1115209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47692d0f47733e5825af244b172ca4816fb810d11cb8b4db2cbefaf8fd3e3a94`

```dockerfile
```

-	Layers:
	-	`sha256:e67d6e6010f71f6a83aa9d1ce76511d4d3203364f25080bd6d2f637a58678ce0`  
		Last Modified: Wed, 01 May 2024 21:52:18 GMT  
		Size: 1.1 MB (1098644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c01e8a120720019fadacc05b56d4022f3247730ee5b0c399b93e61f30bf2151`  
		Last Modified: Wed, 01 May 2024 21:52:18 GMT  
		Size: 16.6 KB (16565 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.9.13-meta`

```console
$ docker pull influxdb@sha256:c3607c2f3d1b6099f581a0dde16ac6f2669758c9be06650518ad6b951d9a4793
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9.13-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:1c6db348aa5e0a6e8c96f62637cf064d18658305b78fc6d2091985603677c9ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83635954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a42077e4565d830f6f6b1565dea4dd8768bffd2688e1c4afbc11eeaffeafc46`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 30 Apr 2024 14:27:41 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Tue, 30 Apr 2024 14:27:41 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb* # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f0bf643eb6745d5c7e9bada33de1786ab2350240206a1956fa506a1b47b129`  
		Last Modified: Tue, 14 May 2024 03:05:14 GMT  
		Size: 15.8 MB (15764867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d12b6386edc3e1f7267ca5eb78e3e41301565e13961ae3f097f2966aea7b9c`  
		Last Modified: Tue, 14 May 2024 03:56:39 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5d290cbc8de21b69b5060ba892a6a3893120cea672eb5fc88f33b3ffe83ba7`  
		Last Modified: Tue, 14 May 2024 03:56:39 GMT  
		Size: 12.8 MB (12769341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8b6c9160b18e279509b69a2da837b4e09a0c750a52d323ec895e85cf4946f9`  
		Last Modified: Tue, 14 May 2024 03:56:39 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150129c5d1c54477fe7e3d295afa7b641550cca2a85309a43e0ad15be212a3ca`  
		Last Modified: Tue, 14 May 2024 03:56:39 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9.13-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:cd1b913219b59b453fee4ac14a3603bd0da40d3f2176e116751e0306c8439298
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4529328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a622b0300987377f3f54d5fdc7fa8c38a9ab16e8c371ecd077b642766931991a`

```dockerfile
```

-	Layers:
	-	`sha256:0fbecbae89f9acdce5047e8ad154544466b19a39115aa400959523fa352cc9d9`  
		Last Modified: Tue, 14 May 2024 03:56:39 GMT  
		Size: 4.5 MB (4516157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0d64448b12a4ede0b3a702a74aaf5c9e40c52b2753d0a8f11c975818d8eac54`  
		Last Modified: Tue, 14 May 2024 03:56:39 GMT  
		Size: 13.2 KB (13171 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.9.13-meta-alpine`

```console
$ docker pull influxdb@sha256:66ab261719e1c0f01be6b23d4ca528e818496d523e9af571697aa1c5e041c4ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9.13-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:ccc210b1156d33adb71f2555b6401a8a874308fe4317ab4f3afa532bfd695490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17594177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:521c8e538680a350a503444fd7a8cca096c7c546e65cde39b3a2a66f58ea2fb5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/etc/influxdb/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b28eadf388e599b4a13053167aacec5d9b8f04bd20e51802d5c5b0cc30017b`  
		Last Modified: Wed, 01 May 2024 21:52:19 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1cb261ee6b33db5c86f4f909edf59330c7b0f42f3b655b661b1b44b56a87617`  
		Last Modified: Wed, 01 May 2024 21:52:20 GMT  
		Size: 1.5 MB (1479564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8c2464ec800e8abaaacf6c7dfb9535113e1db1c9be7aed5dac73111de19a0e`  
		Last Modified: Wed, 01 May 2024 21:52:20 GMT  
		Size: 12.7 MB (12734364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc30d67c3f256925019c3b7ca48a85f7c43473542efd57a6193cc4e839d6ae60`  
		Last Modified: Wed, 01 May 2024 21:52:20 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f59dc2b609146f1f6ea066534b0f0b6d73bffdbf440a5fafa9d3a0806a98552`  
		Last Modified: Wed, 01 May 2024 21:52:20 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9.13-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:051fd69588801e89446bbdc9a116814b5bab9fac69cf3867c763df3f5c2b3809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1059939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d43a3e82c6fc2f141e49c1301ca99d11805eb01b166816a2c7800be951496027`

```dockerfile
```

-	Layers:
	-	`sha256:5e1b23b87a9a4da70821a1a29956402e72b414f37f5aa6798340755f5cb43870`  
		Last Modified: Wed, 01 May 2024 21:52:19 GMT  
		Size: 1.0 MB (1045009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a07320f6996a26b1b970f5db94262aff1faaf31a056a74d47cc443c21622428`  
		Last Modified: Wed, 01 May 2024 21:52:20 GMT  
		Size: 14.9 KB (14930 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2`

```console
$ docker pull influxdb@sha256:166d2c5d89dd4a726709a9cf661236ab5d3efb6f9b6aa7765ae405e1d5b5c0e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2` - linux; amd64

```console
$ docker pull influxdb@sha256:d99286d6d608ab56c099a34cf89b06081855e4e74b7f19cbc77f0767bc481960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (163963521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e8e0548f67de407e9e1e4c3dd2ec1624e6580e697fdc0eeb8d297bfa6054924`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Apr 2024 14:27:41 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV GOSU_VER=1.16
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=2.7.6
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 30 Apr 2024 14:27:41 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3281a4f6315699b26a503c6566f103759a828f12f553d92c9b8568fc7c1559d9`  
		Last Modified: Tue, 14 May 2024 02:56:14 GMT  
		Size: 9.6 MB (9592066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771d8fabb6d8d6168dff52e46c2de8bd63cbd254aa1daaae0de29c4a8a9c60ca`  
		Last Modified: Tue, 14 May 2024 02:56:13 GMT  
		Size: 5.8 MB (5820930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd80e673f4ae3a675aac60f5fe134631bf83ca02d261dbb6e0b2c5ac459fdb5d`  
		Last Modified: Tue, 14 May 2024 02:56:13 GMT  
		Size: 3.2 KB (3228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbc0440f3fc95e1ee5718c116e488c2ef54dd855e8a785fe0df1b38d3772ace`  
		Last Modified: Tue, 14 May 2024 02:56:14 GMT  
		Size: 1.0 MB (1006369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5287862d976b0fb6bb758104e481b6ad632695afc1b02be6b63e62a7c08d181`  
		Last Modified: Tue, 14 May 2024 02:56:17 GMT  
		Size: 95.3 MB (95255495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:600d43bc88368488e797321a2e61f29d6693c25109fbe3e90f0ace24ed64e94e`  
		Last Modified: Tue, 14 May 2024 02:56:15 GMT  
		Size: 23.1 MB (23128297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08c5b27d92fd53db8497e383fd147eac93f0e9855db3d6ea795a2b94db66a8f`  
		Last Modified: Tue, 14 May 2024 02:56:15 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68e3f9b103c4ff3003adecfabc60a61919e76d6e3ee51bef7922da4fd4288a9`  
		Last Modified: Tue, 14 May 2024 02:56:15 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ccdb2a969faa0715ed4dd94da0470c3f7c197963087f7583b9acdeefca42bbe`  
		Last Modified: Tue, 14 May 2024 02:56:16 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:f4b8b5685fa1e5e9b907546f08c5ad89a95a70e489fdd70d6c8162492791d1dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2788865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7011ea586dd090e9eb31c3ad42fe4ecdf4dc7b525db11c74583f1d317c3c4ec8`

```dockerfile
```

-	Layers:
	-	`sha256:18a0d6b5136dce2ea4c5894cd551c68208911928081cfee3ec4909776478332f`  
		Last Modified: Tue, 14 May 2024 02:56:13 GMT  
		Size: 2.8 MB (2755207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a13cf10a8af436c29a25887e528c27a9c80df9830f83d34a67a68dd42f52706d`  
		Last Modified: Tue, 14 May 2024 02:56:13 GMT  
		Size: 33.7 KB (33658 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:3b699dc75f2a75f81e057a047085b6c016dc575e1acf48a3320af878d5589a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 MB (158094032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8acfacfc83128f2e92d41bea9c1bb8e15e8ff7027b39dcef185e22ab6fbe197`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Apr 2024 14:27:41 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV GOSU_VER=1.16
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=2.7.6
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 30 Apr 2024 14:27:41 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98167288b15823502ff3c008c1bebe0312b59afc732eaf2dec0e61340c46635`  
		Last Modified: Tue, 14 May 2024 17:29:50 GMT  
		Size: 9.4 MB (9388812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91a101ca6ad0fddf0d58a75e2aa3bb06ec6478360acf2382b7e6541b8acce87`  
		Last Modified: Tue, 14 May 2024 17:29:50 GMT  
		Size: 5.5 MB (5463799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85934a06a541a67e972990b0c86ca48db4f2193900c938ac37ff7781246b491`  
		Last Modified: Tue, 14 May 2024 17:29:49 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76eac9bf03788d128473d4585c76d733f0fa758a7a6c6030be6e41d679f4a109`  
		Last Modified: Tue, 14 May 2024 17:29:50 GMT  
		Size: 936.1 KB (936105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2bd9f7fe580a2e35e6ea5dc4651d37e5a7efca901a7771bc3dcc3fcaaa8f03b`  
		Last Modified: Tue, 14 May 2024 17:29:53 GMT  
		Size: 91.5 MB (91453341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1724f8117c2e536d58a8b35800242451c4200dc0e76515c3d8004f5749ea454f`  
		Last Modified: Tue, 14 May 2024 17:29:52 GMT  
		Size: 21.7 MB (21662520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87030b6e2eb8ed62a2f9eec98a69f009a24ca821fa253e7d294609a815139927`  
		Last Modified: Tue, 14 May 2024 17:29:51 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6692a03c0e61ca71e99d6d173185294196b720fcc30dd72bcd1a4b54527bdf9b`  
		Last Modified: Tue, 14 May 2024 17:29:51 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95596ef02d9b608a1e30a9fe24fa90955cc15b2d96d3e8393f0297ae95c173e3`  
		Last Modified: Tue, 14 May 2024 17:29:52 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:86f1191ef06a948e5bacffa42e23b84ebf6cf9e1c0a8258ff8d4b2d7d7a0d7ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2788037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed888077f2bca79d4b912479ff9f356e6f2430ff82f6ed778039f16f8c47918`

```dockerfile
```

-	Layers:
	-	`sha256:19d119d867f247c4f3d37761b112c7335a36f67ce31a2f99fba848e75cce5a13`  
		Last Modified: Tue, 14 May 2024 17:29:50 GMT  
		Size: 2.8 MB (2754542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63537c3dbb581b34d88d4a7c800055a2d489f9d10f6b1adbad109b606ae59a22`  
		Last Modified: Tue, 14 May 2024 17:29:49 GMT  
		Size: 33.5 KB (33495 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2-alpine`

```console
$ docker pull influxdb@sha256:e8227ea5a0d439fbadfdc4313127de265db828aeb98a5010192f4ad6ddb0f153
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:3a1c312451e324385faa9b9057769a14bc238db40d8997b63c2b8b76266740a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.9 MB (88914195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2913aad91f13be6e0dc94098f3a8f1a08f493ada7fb2ba78a41b39d57d5b607`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=2.7.6
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 30 Apr 2024 14:27:41 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9c75e715b41546198c3da36896fa3210984b20f84ce352fcce24a85f11fecf`  
		Last Modified: Wed, 01 May 2024 21:52:46 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86a684a638a803548c01347581fa410ef7c523c0ff0def4ab203579530d9199`  
		Last Modified: Wed, 01 May 2024 21:52:46 GMT  
		Size: 8.9 MB (8932328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2160075fafe03b859c8e27c2d4dcaa8bff187f92106fe0e924f2333fd62366e`  
		Last Modified: Wed, 01 May 2024 21:52:47 GMT  
		Size: 5.8 MB (5820950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1603bd3d6bab54257e1b2a23182aa4b4239ecbf3cb80d920999c475203231d4`  
		Last Modified: Wed, 01 May 2024 21:52:46 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9f491f6e21ace7509bfde52f5d098369f6626f8842dbb06d48b1636c70ced1`  
		Last Modified: Wed, 01 May 2024 21:52:49 GMT  
		Size: 47.6 MB (47621806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b53c87e5b526d236c41673b3bfde57ca79ae235453cab950c1ba124336208e2`  
		Last Modified: Wed, 01 May 2024 21:52:49 GMT  
		Size: 23.1 MB (23128321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440ad3b60c84a145c02f692d5cabc649daedd0a9f8f04ca26b8530a623743713`  
		Last Modified: Wed, 01 May 2024 21:52:48 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31eb252bb9c09aef315832bf92b3316658989516a2e3c2887d3fa9ce560b458`  
		Last Modified: Wed, 01 May 2024 21:52:48 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d44f3cbb340a85e386bd993b25d34012ea7f4c79e860539d09dec23202d30f5`  
		Last Modified: Wed, 01 May 2024 21:52:49 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:45fdefdcf4c1ee32fabfad3f379b0f841946b89d9a7c5397b88bd46536db7786
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1260016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4ed59c7b50554b948c0a1ec9c46e5dfa3d6407e3991d4dcc9f5a19d528386d2`

```dockerfile
```

-	Layers:
	-	`sha256:e9388f451e266a044806099e30a6b720473a00d7643cd0a6d13d39628d4d317a`  
		Last Modified: Wed, 01 May 2024 21:52:46 GMT  
		Size: 1.2 MB (1229146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cd26525de9a20fba6ba3120f4c20f7b7e87d1776a369ccf8b2d5bde71fe660a`  
		Last Modified: Wed, 01 May 2024 21:52:46 GMT  
		Size: 30.9 KB (30870 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:a447c7691118e4b944fc4253646a85bdc4dd5d85bc67053aa00407799be5eb98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.2 MB (85195071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88b59f2ea0e777f58a286b6868c8b9c651068837f807657799f230a35d803fec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=2.7.6
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 30 Apr 2024 14:27:41 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e74179715305742e7954518090dcbbc3c0add9c427eeb0a7ae2a70233db410`  
		Last Modified: Wed, 01 May 2024 22:30:24 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c2caa740ce1bd53f19359065530c9b61190044a34f9b68851fb0b76883eeec`  
		Last Modified: Wed, 01 May 2024 22:30:24 GMT  
		Size: 9.0 MB (9005097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc8e03f34f4b44aaeef0577844e031669b08a49e4ad60844581665284bd27b5`  
		Last Modified: Wed, 01 May 2024 22:30:24 GMT  
		Size: 5.5 MB (5463799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f301d47f64728dbf02749d5a89a4276afd3091dfcf5025175626d0549e9966`  
		Last Modified: Wed, 01 May 2024 22:30:24 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e707164649a9968ab55dbd0a9c6b9a40236fc07af816ab780a67c95b06a24dc2`  
		Last Modified: Wed, 01 May 2024 22:30:27 GMT  
		Size: 45.7 MB (45722044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a75ebcf248502332725da8073f88cd2962b663a00d89c4cb4ff08474819278`  
		Last Modified: Wed, 01 May 2024 22:30:26 GMT  
		Size: 21.7 MB (21662519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b005b15de8f90ca32745124d3daacfe3d25494e5c0d920cb284a941018b8c4`  
		Last Modified: Wed, 01 May 2024 22:30:25 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd62367cd346c2f5a62be762cba4e2766a0c0c4b47e90ccf503f3ebcc490e63`  
		Last Modified: Wed, 01 May 2024 22:30:25 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a931c6d2672f2b420e8716757f669bf6c04d82edff90c6c3d2143c3f2b1aee`  
		Last Modified: Wed, 01 May 2024 22:30:26 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:55b507eedf67d40c2aa038c77fb348a7ffa09e8a49a1e5182d434aa2619fec0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1259219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55488d110c8e420ffb50282e47c31d05394a3c5a4810555a149197f4308115e1`

```dockerfile
```

-	Layers:
	-	`sha256:a251dff465e4fd6d762a0530cc733e8edb351699632df99091cc1a1abdc80e8e`  
		Last Modified: Wed, 01 May 2024 22:30:24 GMT  
		Size: 1.2 MB (1228505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dfc68710136fe415ffc99b514fc089af11e92a2f8b5bcef9c5f4309c11ca24d`  
		Last Modified: Wed, 01 May 2024 22:30:24 GMT  
		Size: 30.7 KB (30714 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7`

```console
$ docker pull influxdb@sha256:166d2c5d89dd4a726709a9cf661236ab5d3efb6f9b6aa7765ae405e1d5b5c0e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7` - linux; amd64

```console
$ docker pull influxdb@sha256:d99286d6d608ab56c099a34cf89b06081855e4e74b7f19cbc77f0767bc481960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (163963521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e8e0548f67de407e9e1e4c3dd2ec1624e6580e697fdc0eeb8d297bfa6054924`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Apr 2024 14:27:41 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV GOSU_VER=1.16
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=2.7.6
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 30 Apr 2024 14:27:41 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3281a4f6315699b26a503c6566f103759a828f12f553d92c9b8568fc7c1559d9`  
		Last Modified: Tue, 14 May 2024 02:56:14 GMT  
		Size: 9.6 MB (9592066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771d8fabb6d8d6168dff52e46c2de8bd63cbd254aa1daaae0de29c4a8a9c60ca`  
		Last Modified: Tue, 14 May 2024 02:56:13 GMT  
		Size: 5.8 MB (5820930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd80e673f4ae3a675aac60f5fe134631bf83ca02d261dbb6e0b2c5ac459fdb5d`  
		Last Modified: Tue, 14 May 2024 02:56:13 GMT  
		Size: 3.2 KB (3228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbc0440f3fc95e1ee5718c116e488c2ef54dd855e8a785fe0df1b38d3772ace`  
		Last Modified: Tue, 14 May 2024 02:56:14 GMT  
		Size: 1.0 MB (1006369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5287862d976b0fb6bb758104e481b6ad632695afc1b02be6b63e62a7c08d181`  
		Last Modified: Tue, 14 May 2024 02:56:17 GMT  
		Size: 95.3 MB (95255495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:600d43bc88368488e797321a2e61f29d6693c25109fbe3e90f0ace24ed64e94e`  
		Last Modified: Tue, 14 May 2024 02:56:15 GMT  
		Size: 23.1 MB (23128297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08c5b27d92fd53db8497e383fd147eac93f0e9855db3d6ea795a2b94db66a8f`  
		Last Modified: Tue, 14 May 2024 02:56:15 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68e3f9b103c4ff3003adecfabc60a61919e76d6e3ee51bef7922da4fd4288a9`  
		Last Modified: Tue, 14 May 2024 02:56:15 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ccdb2a969faa0715ed4dd94da0470c3f7c197963087f7583b9acdeefca42bbe`  
		Last Modified: Tue, 14 May 2024 02:56:16 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:f4b8b5685fa1e5e9b907546f08c5ad89a95a70e489fdd70d6c8162492791d1dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2788865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7011ea586dd090e9eb31c3ad42fe4ecdf4dc7b525db11c74583f1d317c3c4ec8`

```dockerfile
```

-	Layers:
	-	`sha256:18a0d6b5136dce2ea4c5894cd551c68208911928081cfee3ec4909776478332f`  
		Last Modified: Tue, 14 May 2024 02:56:13 GMT  
		Size: 2.8 MB (2755207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a13cf10a8af436c29a25887e528c27a9c80df9830f83d34a67a68dd42f52706d`  
		Last Modified: Tue, 14 May 2024 02:56:13 GMT  
		Size: 33.7 KB (33658 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:3b699dc75f2a75f81e057a047085b6c016dc575e1acf48a3320af878d5589a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 MB (158094032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8acfacfc83128f2e92d41bea9c1bb8e15e8ff7027b39dcef185e22ab6fbe197`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Apr 2024 14:27:41 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV GOSU_VER=1.16
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=2.7.6
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 30 Apr 2024 14:27:41 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98167288b15823502ff3c008c1bebe0312b59afc732eaf2dec0e61340c46635`  
		Last Modified: Tue, 14 May 2024 17:29:50 GMT  
		Size: 9.4 MB (9388812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91a101ca6ad0fddf0d58a75e2aa3bb06ec6478360acf2382b7e6541b8acce87`  
		Last Modified: Tue, 14 May 2024 17:29:50 GMT  
		Size: 5.5 MB (5463799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85934a06a541a67e972990b0c86ca48db4f2193900c938ac37ff7781246b491`  
		Last Modified: Tue, 14 May 2024 17:29:49 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76eac9bf03788d128473d4585c76d733f0fa758a7a6c6030be6e41d679f4a109`  
		Last Modified: Tue, 14 May 2024 17:29:50 GMT  
		Size: 936.1 KB (936105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2bd9f7fe580a2e35e6ea5dc4651d37e5a7efca901a7771bc3dcc3fcaaa8f03b`  
		Last Modified: Tue, 14 May 2024 17:29:53 GMT  
		Size: 91.5 MB (91453341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1724f8117c2e536d58a8b35800242451c4200dc0e76515c3d8004f5749ea454f`  
		Last Modified: Tue, 14 May 2024 17:29:52 GMT  
		Size: 21.7 MB (21662520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87030b6e2eb8ed62a2f9eec98a69f009a24ca821fa253e7d294609a815139927`  
		Last Modified: Tue, 14 May 2024 17:29:51 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6692a03c0e61ca71e99d6d173185294196b720fcc30dd72bcd1a4b54527bdf9b`  
		Last Modified: Tue, 14 May 2024 17:29:51 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95596ef02d9b608a1e30a9fe24fa90955cc15b2d96d3e8393f0297ae95c173e3`  
		Last Modified: Tue, 14 May 2024 17:29:52 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:86f1191ef06a948e5bacffa42e23b84ebf6cf9e1c0a8258ff8d4b2d7d7a0d7ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2788037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed888077f2bca79d4b912479ff9f356e6f2430ff82f6ed778039f16f8c47918`

```dockerfile
```

-	Layers:
	-	`sha256:19d119d867f247c4f3d37761b112c7335a36f67ce31a2f99fba848e75cce5a13`  
		Last Modified: Tue, 14 May 2024 17:29:50 GMT  
		Size: 2.8 MB (2754542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63537c3dbb581b34d88d4a7c800055a2d489f9d10f6b1adbad109b606ae59a22`  
		Last Modified: Tue, 14 May 2024 17:29:49 GMT  
		Size: 33.5 KB (33495 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7-alpine`

```console
$ docker pull influxdb@sha256:e8227ea5a0d439fbadfdc4313127de265db828aeb98a5010192f4ad6ddb0f153
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:3a1c312451e324385faa9b9057769a14bc238db40d8997b63c2b8b76266740a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.9 MB (88914195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2913aad91f13be6e0dc94098f3a8f1a08f493ada7fb2ba78a41b39d57d5b607`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=2.7.6
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 30 Apr 2024 14:27:41 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9c75e715b41546198c3da36896fa3210984b20f84ce352fcce24a85f11fecf`  
		Last Modified: Wed, 01 May 2024 21:52:46 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86a684a638a803548c01347581fa410ef7c523c0ff0def4ab203579530d9199`  
		Last Modified: Wed, 01 May 2024 21:52:46 GMT  
		Size: 8.9 MB (8932328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2160075fafe03b859c8e27c2d4dcaa8bff187f92106fe0e924f2333fd62366e`  
		Last Modified: Wed, 01 May 2024 21:52:47 GMT  
		Size: 5.8 MB (5820950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1603bd3d6bab54257e1b2a23182aa4b4239ecbf3cb80d920999c475203231d4`  
		Last Modified: Wed, 01 May 2024 21:52:46 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9f491f6e21ace7509bfde52f5d098369f6626f8842dbb06d48b1636c70ced1`  
		Last Modified: Wed, 01 May 2024 21:52:49 GMT  
		Size: 47.6 MB (47621806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b53c87e5b526d236c41673b3bfde57ca79ae235453cab950c1ba124336208e2`  
		Last Modified: Wed, 01 May 2024 21:52:49 GMT  
		Size: 23.1 MB (23128321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440ad3b60c84a145c02f692d5cabc649daedd0a9f8f04ca26b8530a623743713`  
		Last Modified: Wed, 01 May 2024 21:52:48 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31eb252bb9c09aef315832bf92b3316658989516a2e3c2887d3fa9ce560b458`  
		Last Modified: Wed, 01 May 2024 21:52:48 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d44f3cbb340a85e386bd993b25d34012ea7f4c79e860539d09dec23202d30f5`  
		Last Modified: Wed, 01 May 2024 21:52:49 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:45fdefdcf4c1ee32fabfad3f379b0f841946b89d9a7c5397b88bd46536db7786
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1260016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4ed59c7b50554b948c0a1ec9c46e5dfa3d6407e3991d4dcc9f5a19d528386d2`

```dockerfile
```

-	Layers:
	-	`sha256:e9388f451e266a044806099e30a6b720473a00d7643cd0a6d13d39628d4d317a`  
		Last Modified: Wed, 01 May 2024 21:52:46 GMT  
		Size: 1.2 MB (1229146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cd26525de9a20fba6ba3120f4c20f7b7e87d1776a369ccf8b2d5bde71fe660a`  
		Last Modified: Wed, 01 May 2024 21:52:46 GMT  
		Size: 30.9 KB (30870 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:a447c7691118e4b944fc4253646a85bdc4dd5d85bc67053aa00407799be5eb98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.2 MB (85195071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88b59f2ea0e777f58a286b6868c8b9c651068837f807657799f230a35d803fec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=2.7.6
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 30 Apr 2024 14:27:41 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e74179715305742e7954518090dcbbc3c0add9c427eeb0a7ae2a70233db410`  
		Last Modified: Wed, 01 May 2024 22:30:24 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c2caa740ce1bd53f19359065530c9b61190044a34f9b68851fb0b76883eeec`  
		Last Modified: Wed, 01 May 2024 22:30:24 GMT  
		Size: 9.0 MB (9005097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc8e03f34f4b44aaeef0577844e031669b08a49e4ad60844581665284bd27b5`  
		Last Modified: Wed, 01 May 2024 22:30:24 GMT  
		Size: 5.5 MB (5463799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f301d47f64728dbf02749d5a89a4276afd3091dfcf5025175626d0549e9966`  
		Last Modified: Wed, 01 May 2024 22:30:24 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e707164649a9968ab55dbd0a9c6b9a40236fc07af816ab780a67c95b06a24dc2`  
		Last Modified: Wed, 01 May 2024 22:30:27 GMT  
		Size: 45.7 MB (45722044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a75ebcf248502332725da8073f88cd2962b663a00d89c4cb4ff08474819278`  
		Last Modified: Wed, 01 May 2024 22:30:26 GMT  
		Size: 21.7 MB (21662519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b005b15de8f90ca32745124d3daacfe3d25494e5c0d920cb284a941018b8c4`  
		Last Modified: Wed, 01 May 2024 22:30:25 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd62367cd346c2f5a62be762cba4e2766a0c0c4b47e90ccf503f3ebcc490e63`  
		Last Modified: Wed, 01 May 2024 22:30:25 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a931c6d2672f2b420e8716757f669bf6c04d82edff90c6c3d2143c3f2b1aee`  
		Last Modified: Wed, 01 May 2024 22:30:26 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:55b507eedf67d40c2aa038c77fb348a7ffa09e8a49a1e5182d434aa2619fec0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1259219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55488d110c8e420ffb50282e47c31d05394a3c5a4810555a149197f4308115e1`

```dockerfile
```

-	Layers:
	-	`sha256:a251dff465e4fd6d762a0530cc733e8edb351699632df99091cc1a1abdc80e8e`  
		Last Modified: Wed, 01 May 2024 22:30:24 GMT  
		Size: 1.2 MB (1228505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dfc68710136fe415ffc99b514fc089af11e92a2f8b5bcef9c5f4309c11ca24d`  
		Last Modified: Wed, 01 May 2024 22:30:24 GMT  
		Size: 30.7 KB (30714 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7.6`

```console
$ docker pull influxdb@sha256:166d2c5d89dd4a726709a9cf661236ab5d3efb6f9b6aa7765ae405e1d5b5c0e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7.6` - linux; amd64

```console
$ docker pull influxdb@sha256:d99286d6d608ab56c099a34cf89b06081855e4e74b7f19cbc77f0767bc481960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (163963521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e8e0548f67de407e9e1e4c3dd2ec1624e6580e697fdc0eeb8d297bfa6054924`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Apr 2024 14:27:41 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV GOSU_VER=1.16
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=2.7.6
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 30 Apr 2024 14:27:41 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3281a4f6315699b26a503c6566f103759a828f12f553d92c9b8568fc7c1559d9`  
		Last Modified: Tue, 14 May 2024 02:56:14 GMT  
		Size: 9.6 MB (9592066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771d8fabb6d8d6168dff52e46c2de8bd63cbd254aa1daaae0de29c4a8a9c60ca`  
		Last Modified: Tue, 14 May 2024 02:56:13 GMT  
		Size: 5.8 MB (5820930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd80e673f4ae3a675aac60f5fe134631bf83ca02d261dbb6e0b2c5ac459fdb5d`  
		Last Modified: Tue, 14 May 2024 02:56:13 GMT  
		Size: 3.2 KB (3228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbc0440f3fc95e1ee5718c116e488c2ef54dd855e8a785fe0df1b38d3772ace`  
		Last Modified: Tue, 14 May 2024 02:56:14 GMT  
		Size: 1.0 MB (1006369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5287862d976b0fb6bb758104e481b6ad632695afc1b02be6b63e62a7c08d181`  
		Last Modified: Tue, 14 May 2024 02:56:17 GMT  
		Size: 95.3 MB (95255495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:600d43bc88368488e797321a2e61f29d6693c25109fbe3e90f0ace24ed64e94e`  
		Last Modified: Tue, 14 May 2024 02:56:15 GMT  
		Size: 23.1 MB (23128297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08c5b27d92fd53db8497e383fd147eac93f0e9855db3d6ea795a2b94db66a8f`  
		Last Modified: Tue, 14 May 2024 02:56:15 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68e3f9b103c4ff3003adecfabc60a61919e76d6e3ee51bef7922da4fd4288a9`  
		Last Modified: Tue, 14 May 2024 02:56:15 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ccdb2a969faa0715ed4dd94da0470c3f7c197963087f7583b9acdeefca42bbe`  
		Last Modified: Tue, 14 May 2024 02:56:16 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.6` - unknown; unknown

```console
$ docker pull influxdb@sha256:f4b8b5685fa1e5e9b907546f08c5ad89a95a70e489fdd70d6c8162492791d1dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2788865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7011ea586dd090e9eb31c3ad42fe4ecdf4dc7b525db11c74583f1d317c3c4ec8`

```dockerfile
```

-	Layers:
	-	`sha256:18a0d6b5136dce2ea4c5894cd551c68208911928081cfee3ec4909776478332f`  
		Last Modified: Tue, 14 May 2024 02:56:13 GMT  
		Size: 2.8 MB (2755207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a13cf10a8af436c29a25887e528c27a9c80df9830f83d34a67a68dd42f52706d`  
		Last Modified: Tue, 14 May 2024 02:56:13 GMT  
		Size: 33.7 KB (33658 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7.6` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:3b699dc75f2a75f81e057a047085b6c016dc575e1acf48a3320af878d5589a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 MB (158094032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8acfacfc83128f2e92d41bea9c1bb8e15e8ff7027b39dcef185e22ab6fbe197`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Apr 2024 14:27:41 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV GOSU_VER=1.16
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=2.7.6
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 30 Apr 2024 14:27:41 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98167288b15823502ff3c008c1bebe0312b59afc732eaf2dec0e61340c46635`  
		Last Modified: Tue, 14 May 2024 17:29:50 GMT  
		Size: 9.4 MB (9388812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91a101ca6ad0fddf0d58a75e2aa3bb06ec6478360acf2382b7e6541b8acce87`  
		Last Modified: Tue, 14 May 2024 17:29:50 GMT  
		Size: 5.5 MB (5463799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85934a06a541a67e972990b0c86ca48db4f2193900c938ac37ff7781246b491`  
		Last Modified: Tue, 14 May 2024 17:29:49 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76eac9bf03788d128473d4585c76d733f0fa758a7a6c6030be6e41d679f4a109`  
		Last Modified: Tue, 14 May 2024 17:29:50 GMT  
		Size: 936.1 KB (936105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2bd9f7fe580a2e35e6ea5dc4651d37e5a7efca901a7771bc3dcc3fcaaa8f03b`  
		Last Modified: Tue, 14 May 2024 17:29:53 GMT  
		Size: 91.5 MB (91453341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1724f8117c2e536d58a8b35800242451c4200dc0e76515c3d8004f5749ea454f`  
		Last Modified: Tue, 14 May 2024 17:29:52 GMT  
		Size: 21.7 MB (21662520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87030b6e2eb8ed62a2f9eec98a69f009a24ca821fa253e7d294609a815139927`  
		Last Modified: Tue, 14 May 2024 17:29:51 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6692a03c0e61ca71e99d6d173185294196b720fcc30dd72bcd1a4b54527bdf9b`  
		Last Modified: Tue, 14 May 2024 17:29:51 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95596ef02d9b608a1e30a9fe24fa90955cc15b2d96d3e8393f0297ae95c173e3`  
		Last Modified: Tue, 14 May 2024 17:29:52 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.6` - unknown; unknown

```console
$ docker pull influxdb@sha256:86f1191ef06a948e5bacffa42e23b84ebf6cf9e1c0a8258ff8d4b2d7d7a0d7ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2788037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed888077f2bca79d4b912479ff9f356e6f2430ff82f6ed778039f16f8c47918`

```dockerfile
```

-	Layers:
	-	`sha256:19d119d867f247c4f3d37761b112c7335a36f67ce31a2f99fba848e75cce5a13`  
		Last Modified: Tue, 14 May 2024 17:29:50 GMT  
		Size: 2.8 MB (2754542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63537c3dbb581b34d88d4a7c800055a2d489f9d10f6b1adbad109b606ae59a22`  
		Last Modified: Tue, 14 May 2024 17:29:49 GMT  
		Size: 33.5 KB (33495 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7.6-alpine`

```console
$ docker pull influxdb@sha256:e8227ea5a0d439fbadfdc4313127de265db828aeb98a5010192f4ad6ddb0f153
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7.6-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:3a1c312451e324385faa9b9057769a14bc238db40d8997b63c2b8b76266740a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.9 MB (88914195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2913aad91f13be6e0dc94098f3a8f1a08f493ada7fb2ba78a41b39d57d5b607`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=2.7.6
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 30 Apr 2024 14:27:41 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9c75e715b41546198c3da36896fa3210984b20f84ce352fcce24a85f11fecf`  
		Last Modified: Wed, 01 May 2024 21:52:46 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86a684a638a803548c01347581fa410ef7c523c0ff0def4ab203579530d9199`  
		Last Modified: Wed, 01 May 2024 21:52:46 GMT  
		Size: 8.9 MB (8932328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2160075fafe03b859c8e27c2d4dcaa8bff187f92106fe0e924f2333fd62366e`  
		Last Modified: Wed, 01 May 2024 21:52:47 GMT  
		Size: 5.8 MB (5820950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1603bd3d6bab54257e1b2a23182aa4b4239ecbf3cb80d920999c475203231d4`  
		Last Modified: Wed, 01 May 2024 21:52:46 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9f491f6e21ace7509bfde52f5d098369f6626f8842dbb06d48b1636c70ced1`  
		Last Modified: Wed, 01 May 2024 21:52:49 GMT  
		Size: 47.6 MB (47621806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b53c87e5b526d236c41673b3bfde57ca79ae235453cab950c1ba124336208e2`  
		Last Modified: Wed, 01 May 2024 21:52:49 GMT  
		Size: 23.1 MB (23128321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440ad3b60c84a145c02f692d5cabc649daedd0a9f8f04ca26b8530a623743713`  
		Last Modified: Wed, 01 May 2024 21:52:48 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31eb252bb9c09aef315832bf92b3316658989516a2e3c2887d3fa9ce560b458`  
		Last Modified: Wed, 01 May 2024 21:52:48 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d44f3cbb340a85e386bd993b25d34012ea7f4c79e860539d09dec23202d30f5`  
		Last Modified: Wed, 01 May 2024 21:52:49 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.6-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:45fdefdcf4c1ee32fabfad3f379b0f841946b89d9a7c5397b88bd46536db7786
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1260016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4ed59c7b50554b948c0a1ec9c46e5dfa3d6407e3991d4dcc9f5a19d528386d2`

```dockerfile
```

-	Layers:
	-	`sha256:e9388f451e266a044806099e30a6b720473a00d7643cd0a6d13d39628d4d317a`  
		Last Modified: Wed, 01 May 2024 21:52:46 GMT  
		Size: 1.2 MB (1229146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cd26525de9a20fba6ba3120f4c20f7b7e87d1776a369ccf8b2d5bde71fe660a`  
		Last Modified: Wed, 01 May 2024 21:52:46 GMT  
		Size: 30.9 KB (30870 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7.6-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:a447c7691118e4b944fc4253646a85bdc4dd5d85bc67053aa00407799be5eb98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.2 MB (85195071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88b59f2ea0e777f58a286b6868c8b9c651068837f807657799f230a35d803fec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=2.7.6
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 30 Apr 2024 14:27:41 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e74179715305742e7954518090dcbbc3c0add9c427eeb0a7ae2a70233db410`  
		Last Modified: Wed, 01 May 2024 22:30:24 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c2caa740ce1bd53f19359065530c9b61190044a34f9b68851fb0b76883eeec`  
		Last Modified: Wed, 01 May 2024 22:30:24 GMT  
		Size: 9.0 MB (9005097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc8e03f34f4b44aaeef0577844e031669b08a49e4ad60844581665284bd27b5`  
		Last Modified: Wed, 01 May 2024 22:30:24 GMT  
		Size: 5.5 MB (5463799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f301d47f64728dbf02749d5a89a4276afd3091dfcf5025175626d0549e9966`  
		Last Modified: Wed, 01 May 2024 22:30:24 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e707164649a9968ab55dbd0a9c6b9a40236fc07af816ab780a67c95b06a24dc2`  
		Last Modified: Wed, 01 May 2024 22:30:27 GMT  
		Size: 45.7 MB (45722044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a75ebcf248502332725da8073f88cd2962b663a00d89c4cb4ff08474819278`  
		Last Modified: Wed, 01 May 2024 22:30:26 GMT  
		Size: 21.7 MB (21662519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b005b15de8f90ca32745124d3daacfe3d25494e5c0d920cb284a941018b8c4`  
		Last Modified: Wed, 01 May 2024 22:30:25 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd62367cd346c2f5a62be762cba4e2766a0c0c4b47e90ccf503f3ebcc490e63`  
		Last Modified: Wed, 01 May 2024 22:30:25 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a931c6d2672f2b420e8716757f669bf6c04d82edff90c6c3d2143c3f2b1aee`  
		Last Modified: Wed, 01 May 2024 22:30:26 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.6-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:55b507eedf67d40c2aa038c77fb348a7ffa09e8a49a1e5182d434aa2619fec0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1259219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55488d110c8e420ffb50282e47c31d05394a3c5a4810555a149197f4308115e1`

```dockerfile
```

-	Layers:
	-	`sha256:a251dff465e4fd6d762a0530cc733e8edb351699632df99091cc1a1abdc80e8e`  
		Last Modified: Wed, 01 May 2024 22:30:24 GMT  
		Size: 1.2 MB (1228505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dfc68710136fe415ffc99b514fc089af11e92a2f8b5bcef9c5f4309c11ca24d`  
		Last Modified: Wed, 01 May 2024 22:30:24 GMT  
		Size: 30.7 KB (30714 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:e8227ea5a0d439fbadfdc4313127de265db828aeb98a5010192f4ad6ddb0f153
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:3a1c312451e324385faa9b9057769a14bc238db40d8997b63c2b8b76266740a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.9 MB (88914195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2913aad91f13be6e0dc94098f3a8f1a08f493ada7fb2ba78a41b39d57d5b607`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=2.7.6
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 30 Apr 2024 14:27:41 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9c75e715b41546198c3da36896fa3210984b20f84ce352fcce24a85f11fecf`  
		Last Modified: Wed, 01 May 2024 21:52:46 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86a684a638a803548c01347581fa410ef7c523c0ff0def4ab203579530d9199`  
		Last Modified: Wed, 01 May 2024 21:52:46 GMT  
		Size: 8.9 MB (8932328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2160075fafe03b859c8e27c2d4dcaa8bff187f92106fe0e924f2333fd62366e`  
		Last Modified: Wed, 01 May 2024 21:52:47 GMT  
		Size: 5.8 MB (5820950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1603bd3d6bab54257e1b2a23182aa4b4239ecbf3cb80d920999c475203231d4`  
		Last Modified: Wed, 01 May 2024 21:52:46 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9f491f6e21ace7509bfde52f5d098369f6626f8842dbb06d48b1636c70ced1`  
		Last Modified: Wed, 01 May 2024 21:52:49 GMT  
		Size: 47.6 MB (47621806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b53c87e5b526d236c41673b3bfde57ca79ae235453cab950c1ba124336208e2`  
		Last Modified: Wed, 01 May 2024 21:52:49 GMT  
		Size: 23.1 MB (23128321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440ad3b60c84a145c02f692d5cabc649daedd0a9f8f04ca26b8530a623743713`  
		Last Modified: Wed, 01 May 2024 21:52:48 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31eb252bb9c09aef315832bf92b3316658989516a2e3c2887d3fa9ce560b458`  
		Last Modified: Wed, 01 May 2024 21:52:48 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d44f3cbb340a85e386bd993b25d34012ea7f4c79e860539d09dec23202d30f5`  
		Last Modified: Wed, 01 May 2024 21:52:49 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:45fdefdcf4c1ee32fabfad3f379b0f841946b89d9a7c5397b88bd46536db7786
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1260016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4ed59c7b50554b948c0a1ec9c46e5dfa3d6407e3991d4dcc9f5a19d528386d2`

```dockerfile
```

-	Layers:
	-	`sha256:e9388f451e266a044806099e30a6b720473a00d7643cd0a6d13d39628d4d317a`  
		Last Modified: Wed, 01 May 2024 21:52:46 GMT  
		Size: 1.2 MB (1229146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cd26525de9a20fba6ba3120f4c20f7b7e87d1776a369ccf8b2d5bde71fe660a`  
		Last Modified: Wed, 01 May 2024 21:52:46 GMT  
		Size: 30.9 KB (30870 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:a447c7691118e4b944fc4253646a85bdc4dd5d85bc67053aa00407799be5eb98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.2 MB (85195071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88b59f2ea0e777f58a286b6868c8b9c651068837f807657799f230a35d803fec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=2.7.6
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 30 Apr 2024 14:27:41 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e74179715305742e7954518090dcbbc3c0add9c427eeb0a7ae2a70233db410`  
		Last Modified: Wed, 01 May 2024 22:30:24 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c2caa740ce1bd53f19359065530c9b61190044a34f9b68851fb0b76883eeec`  
		Last Modified: Wed, 01 May 2024 22:30:24 GMT  
		Size: 9.0 MB (9005097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc8e03f34f4b44aaeef0577844e031669b08a49e4ad60844581665284bd27b5`  
		Last Modified: Wed, 01 May 2024 22:30:24 GMT  
		Size: 5.5 MB (5463799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f301d47f64728dbf02749d5a89a4276afd3091dfcf5025175626d0549e9966`  
		Last Modified: Wed, 01 May 2024 22:30:24 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e707164649a9968ab55dbd0a9c6b9a40236fc07af816ab780a67c95b06a24dc2`  
		Last Modified: Wed, 01 May 2024 22:30:27 GMT  
		Size: 45.7 MB (45722044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a75ebcf248502332725da8073f88cd2962b663a00d89c4cb4ff08474819278`  
		Last Modified: Wed, 01 May 2024 22:30:26 GMT  
		Size: 21.7 MB (21662519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b005b15de8f90ca32745124d3daacfe3d25494e5c0d920cb284a941018b8c4`  
		Last Modified: Wed, 01 May 2024 22:30:25 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd62367cd346c2f5a62be762cba4e2766a0c0c4b47e90ccf503f3ebcc490e63`  
		Last Modified: Wed, 01 May 2024 22:30:25 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a931c6d2672f2b420e8716757f669bf6c04d82edff90c6c3d2143c3f2b1aee`  
		Last Modified: Wed, 01 May 2024 22:30:26 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:55b507eedf67d40c2aa038c77fb348a7ffa09e8a49a1e5182d434aa2619fec0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1259219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55488d110c8e420ffb50282e47c31d05394a3c5a4810555a149197f4308115e1`

```dockerfile
```

-	Layers:
	-	`sha256:a251dff465e4fd6d762a0530cc733e8edb351699632df99091cc1a1abdc80e8e`  
		Last Modified: Wed, 01 May 2024 22:30:24 GMT  
		Size: 1.2 MB (1228505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dfc68710136fe415ffc99b514fc089af11e92a2f8b5bcef9c5f4309c11ca24d`  
		Last Modified: Wed, 01 May 2024 22:30:24 GMT  
		Size: 30.7 KB (30714 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:latest`

```console
$ docker pull influxdb@sha256:166d2c5d89dd4a726709a9cf661236ab5d3efb6f9b6aa7765ae405e1d5b5c0e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:d99286d6d608ab56c099a34cf89b06081855e4e74b7f19cbc77f0767bc481960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (163963521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e8e0548f67de407e9e1e4c3dd2ec1624e6580e697fdc0eeb8d297bfa6054924`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Apr 2024 14:27:41 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV GOSU_VER=1.16
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=2.7.6
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 30 Apr 2024 14:27:41 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3281a4f6315699b26a503c6566f103759a828f12f553d92c9b8568fc7c1559d9`  
		Last Modified: Tue, 14 May 2024 02:56:14 GMT  
		Size: 9.6 MB (9592066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771d8fabb6d8d6168dff52e46c2de8bd63cbd254aa1daaae0de29c4a8a9c60ca`  
		Last Modified: Tue, 14 May 2024 02:56:13 GMT  
		Size: 5.8 MB (5820930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd80e673f4ae3a675aac60f5fe134631bf83ca02d261dbb6e0b2c5ac459fdb5d`  
		Last Modified: Tue, 14 May 2024 02:56:13 GMT  
		Size: 3.2 KB (3228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbc0440f3fc95e1ee5718c116e488c2ef54dd855e8a785fe0df1b38d3772ace`  
		Last Modified: Tue, 14 May 2024 02:56:14 GMT  
		Size: 1.0 MB (1006369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5287862d976b0fb6bb758104e481b6ad632695afc1b02be6b63e62a7c08d181`  
		Last Modified: Tue, 14 May 2024 02:56:17 GMT  
		Size: 95.3 MB (95255495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:600d43bc88368488e797321a2e61f29d6693c25109fbe3e90f0ace24ed64e94e`  
		Last Modified: Tue, 14 May 2024 02:56:15 GMT  
		Size: 23.1 MB (23128297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08c5b27d92fd53db8497e383fd147eac93f0e9855db3d6ea795a2b94db66a8f`  
		Last Modified: Tue, 14 May 2024 02:56:15 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68e3f9b103c4ff3003adecfabc60a61919e76d6e3ee51bef7922da4fd4288a9`  
		Last Modified: Tue, 14 May 2024 02:56:15 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ccdb2a969faa0715ed4dd94da0470c3f7c197963087f7583b9acdeefca42bbe`  
		Last Modified: Tue, 14 May 2024 02:56:16 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:f4b8b5685fa1e5e9b907546f08c5ad89a95a70e489fdd70d6c8162492791d1dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2788865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7011ea586dd090e9eb31c3ad42fe4ecdf4dc7b525db11c74583f1d317c3c4ec8`

```dockerfile
```

-	Layers:
	-	`sha256:18a0d6b5136dce2ea4c5894cd551c68208911928081cfee3ec4909776478332f`  
		Last Modified: Tue, 14 May 2024 02:56:13 GMT  
		Size: 2.8 MB (2755207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a13cf10a8af436c29a25887e528c27a9c80df9830f83d34a67a68dd42f52706d`  
		Last Modified: Tue, 14 May 2024 02:56:13 GMT  
		Size: 33.7 KB (33658 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:3b699dc75f2a75f81e057a047085b6c016dc575e1acf48a3320af878d5589a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 MB (158094032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8acfacfc83128f2e92d41bea9c1bb8e15e8ff7027b39dcef185e22ab6fbe197`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Apr 2024 14:27:41 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV GOSU_VER=1.16
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=2.7.6
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 30 Apr 2024 14:27:41 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98167288b15823502ff3c008c1bebe0312b59afc732eaf2dec0e61340c46635`  
		Last Modified: Tue, 14 May 2024 17:29:50 GMT  
		Size: 9.4 MB (9388812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91a101ca6ad0fddf0d58a75e2aa3bb06ec6478360acf2382b7e6541b8acce87`  
		Last Modified: Tue, 14 May 2024 17:29:50 GMT  
		Size: 5.5 MB (5463799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85934a06a541a67e972990b0c86ca48db4f2193900c938ac37ff7781246b491`  
		Last Modified: Tue, 14 May 2024 17:29:49 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76eac9bf03788d128473d4585c76d733f0fa758a7a6c6030be6e41d679f4a109`  
		Last Modified: Tue, 14 May 2024 17:29:50 GMT  
		Size: 936.1 KB (936105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2bd9f7fe580a2e35e6ea5dc4651d37e5a7efca901a7771bc3dcc3fcaaa8f03b`  
		Last Modified: Tue, 14 May 2024 17:29:53 GMT  
		Size: 91.5 MB (91453341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1724f8117c2e536d58a8b35800242451c4200dc0e76515c3d8004f5749ea454f`  
		Last Modified: Tue, 14 May 2024 17:29:52 GMT  
		Size: 21.7 MB (21662520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87030b6e2eb8ed62a2f9eec98a69f009a24ca821fa253e7d294609a815139927`  
		Last Modified: Tue, 14 May 2024 17:29:51 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6692a03c0e61ca71e99d6d173185294196b720fcc30dd72bcd1a4b54527bdf9b`  
		Last Modified: Tue, 14 May 2024 17:29:51 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95596ef02d9b608a1e30a9fe24fa90955cc15b2d96d3e8393f0297ae95c173e3`  
		Last Modified: Tue, 14 May 2024 17:29:52 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:86f1191ef06a948e5bacffa42e23b84ebf6cf9e1c0a8258ff8d4b2d7d7a0d7ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2788037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed888077f2bca79d4b912479ff9f356e6f2430ff82f6ed778039f16f8c47918`

```dockerfile
```

-	Layers:
	-	`sha256:19d119d867f247c4f3d37761b112c7335a36f67ce31a2f99fba848e75cce5a13`  
		Last Modified: Tue, 14 May 2024 17:29:50 GMT  
		Size: 2.8 MB (2754542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63537c3dbb581b34d88d4a7c800055a2d489f9d10f6b1adbad109b606ae59a22`  
		Last Modified: Tue, 14 May 2024 17:29:49 GMT  
		Size: 33.5 KB (33495 bytes)  
		MIME: application/vnd.in-toto+json
