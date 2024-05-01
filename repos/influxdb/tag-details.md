<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `influxdb`

-	[`influxdb:1.10-data`](#influxdb110-data)
-	[`influxdb:1.10-data-alpine`](#influxdb110-data-alpine)
-	[`influxdb:1.10-meta`](#influxdb110-meta)
-	[`influxdb:1.10-meta-alpine`](#influxdb110-meta-alpine)
-	[`influxdb:1.10.6-data`](#influxdb1106-data)
-	[`influxdb:1.10.6-data-alpine`](#influxdb1106-data-alpine)
-	[`influxdb:1.10.6-meta`](#influxdb1106-meta)
-	[`influxdb:1.10.6-meta-alpine`](#influxdb1106-meta-alpine)
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
$ docker pull influxdb@sha256:ddd4d35422a53533366a12ec7749a0ccbf9ea5dac55a012be185badb02e37e72
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-data` - linux; amd64

```console
$ docker pull influxdb@sha256:1531266b6e0bdb803ab855447f66bc9c58463a3200723cda0ee98d8f10097d9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112248219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c4a80b600c750f610f067990692f95b286d6f620397cca3e392f443db984981`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:19 GMT
ADD file:d9efaba9e396cd5732f1689338ef5f1fbb66667806efe9c6938ca7169b305496 in / 
# Wed, 24 Apr 2024 03:28:19 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:12:09 GMT
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
	-	`sha256:646e886fa3cfd015533cf777eb62fc903426f0b57806d1cbaa843f8f07a9f66d`  
		Last Modified: Wed, 24 Apr 2024 03:33:00 GMT  
		Size: 55.1 MB (55098870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a360c5f105e29623d30cc42a1b871c17a19cbafe3ed994b3b64f2449cd1695`  
		Last Modified: Wed, 24 Apr 2024 04:21:57 GMT  
		Size: 15.8 MB (15765279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c6a947fe2b4a358e5206ab665d766ee8ce3e4eb5a8748b1c533ba733d3f5e7`  
		Last Modified: Wed, 01 May 2024 21:52:34 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ffcbaafc49af3e3ffb8358d27d56f3b8302b3a7384107b67c4ef9563a8537c`  
		Last Modified: Wed, 01 May 2024 21:52:36 GMT  
		Size: 41.4 MB (41380522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41553a7873925c7c1e2c021596617f2029425dee8c416584936455e881fc141e`  
		Last Modified: Wed, 01 May 2024 21:52:34 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a2882eb1ae9e24a6e4ff31710de6c257d716bc2202e20d4c75d1d29f2cb3eae`  
		Last Modified: Wed, 01 May 2024 21:52:35 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09888d5454928396ab82fa3ccd4f6acfe5853a7f21ef57cbb36fd2cf15fe4632`  
		Last Modified: Wed, 01 May 2024 21:52:32 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:be374164ec9c0494d1a5d134f2535eb8f1be9234e3af80b55c14c3980555e0f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4594155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa8f8db9eafbb9a40577ae828c09abcd25b33f3838709d0c69788dd8b2c30a5e`

```dockerfile
```

-	Layers:
	-	`sha256:fe72d888995f5b760f5565f24204a544a0806193b5a1b4e0729101aea891fa28`  
		Last Modified: Wed, 01 May 2024 21:52:35 GMT  
		Size: 4.6 MB (4579298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d108bff3b9d9a0ced686cc67e922acee4a34bc1e45afb3c3e75b11c26b4a5ffb`  
		Last Modified: Wed, 01 May 2024 21:52:34 GMT  
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
$ docker pull influxdb@sha256:bbd168ed806477aef340cc011205dc3915f1c6d1f82864afa2a0dd1e82980ffe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:0d830efa656879c035db808924a52ba9efa95c9d8fc2afe4196ba3f6f875a274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.0 MB (90961721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24d68b6c7724e78acbcd3257a5da30d7add47087f48568fe7c9ef85e592b8ab4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:19 GMT
ADD file:d9efaba9e396cd5732f1689338ef5f1fbb66667806efe9c6938ca7169b305496 in / 
# Wed, 24 Apr 2024 03:28:19 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:12:09 GMT
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
	-	`sha256:646e886fa3cfd015533cf777eb62fc903426f0b57806d1cbaa843f8f07a9f66d`  
		Last Modified: Wed, 24 Apr 2024 03:33:00 GMT  
		Size: 55.1 MB (55098870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a360c5f105e29623d30cc42a1b871c17a19cbafe3ed994b3b64f2449cd1695`  
		Last Modified: Wed, 24 Apr 2024 04:21:57 GMT  
		Size: 15.8 MB (15765279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2911b6cc0f1e670d091d47c3b3d94645c7ee9bbbcac4cd722a6975d1259f394`  
		Last Modified: Wed, 01 May 2024 21:52:30 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67a19b5d179e9e382589fa8874637b0400623133d17781ccf594701cf071375`  
		Last Modified: Wed, 01 May 2024 21:52:30 GMT  
		Size: 20.1 MB (20095234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f626703fcbf241a5c6ad0bd95edc43772b7a5670c85b6e7014ddf0afb49e0c`  
		Last Modified: Wed, 01 May 2024 21:52:30 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e710c4cb00bc1623a1a2adeb9bfe25ec99983af66469432ff0e6eb0c055c34b`  
		Last Modified: Wed, 01 May 2024 21:52:30 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:6d84247c1540f0afeffaa199972690cbc95d91a1c3f21fdfba506ed6c9b7036c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4529387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b70cf13e76882da37f4b9ff0335dca2166a63b1e7172cddb214a0a59674379a4`

```dockerfile
```

-	Layers:
	-	`sha256:baa8d8f574f120b640863d19fb7415747dfaed909b4dd2bd19b9ccaaaf93ed9d`  
		Last Modified: Wed, 01 May 2024 21:52:30 GMT  
		Size: 4.5 MB (4516183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aba922338572da99f541419fdfa1d7e4135c3db9331c597e2ce26d05ff09aa28`  
		Last Modified: Wed, 01 May 2024 21:52:29 GMT  
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

## `influxdb:1.10.6-data`

```console
$ docker pull influxdb@sha256:ddd4d35422a53533366a12ec7749a0ccbf9ea5dac55a012be185badb02e37e72
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.6-data` - linux; amd64

```console
$ docker pull influxdb@sha256:1531266b6e0bdb803ab855447f66bc9c58463a3200723cda0ee98d8f10097d9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112248219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c4a80b600c750f610f067990692f95b286d6f620397cca3e392f443db984981`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:19 GMT
ADD file:d9efaba9e396cd5732f1689338ef5f1fbb66667806efe9c6938ca7169b305496 in / 
# Wed, 24 Apr 2024 03:28:19 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:12:09 GMT
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
	-	`sha256:646e886fa3cfd015533cf777eb62fc903426f0b57806d1cbaa843f8f07a9f66d`  
		Last Modified: Wed, 24 Apr 2024 03:33:00 GMT  
		Size: 55.1 MB (55098870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a360c5f105e29623d30cc42a1b871c17a19cbafe3ed994b3b64f2449cd1695`  
		Last Modified: Wed, 24 Apr 2024 04:21:57 GMT  
		Size: 15.8 MB (15765279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c6a947fe2b4a358e5206ab665d766ee8ce3e4eb5a8748b1c533ba733d3f5e7`  
		Last Modified: Wed, 01 May 2024 21:52:34 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ffcbaafc49af3e3ffb8358d27d56f3b8302b3a7384107b67c4ef9563a8537c`  
		Last Modified: Wed, 01 May 2024 21:52:36 GMT  
		Size: 41.4 MB (41380522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41553a7873925c7c1e2c021596617f2029425dee8c416584936455e881fc141e`  
		Last Modified: Wed, 01 May 2024 21:52:34 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a2882eb1ae9e24a6e4ff31710de6c257d716bc2202e20d4c75d1d29f2cb3eae`  
		Last Modified: Wed, 01 May 2024 21:52:35 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09888d5454928396ab82fa3ccd4f6acfe5853a7f21ef57cbb36fd2cf15fe4632`  
		Last Modified: Wed, 01 May 2024 21:52:32 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.6-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:be374164ec9c0494d1a5d134f2535eb8f1be9234e3af80b55c14c3980555e0f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4594155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa8f8db9eafbb9a40577ae828c09abcd25b33f3838709d0c69788dd8b2c30a5e`

```dockerfile
```

-	Layers:
	-	`sha256:fe72d888995f5b760f5565f24204a544a0806193b5a1b4e0729101aea891fa28`  
		Last Modified: Wed, 01 May 2024 21:52:35 GMT  
		Size: 4.6 MB (4579298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d108bff3b9d9a0ced686cc67e922acee4a34bc1e45afb3c3e75b11c26b4a5ffb`  
		Last Modified: Wed, 01 May 2024 21:52:34 GMT  
		Size: 14.9 KB (14857 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10.6-data-alpine`

```console
$ docker pull influxdb@sha256:8a7499e1532155d81ee0b5517b09f2ed5589fbf819cec8c2709cc0121fe46076
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.6-data-alpine` - linux; amd64

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

### `influxdb:1.10.6-data-alpine` - unknown; unknown

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

## `influxdb:1.10.6-meta`

```console
$ docker pull influxdb@sha256:bbd168ed806477aef340cc011205dc3915f1c6d1f82864afa2a0dd1e82980ffe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.6-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:0d830efa656879c035db808924a52ba9efa95c9d8fc2afe4196ba3f6f875a274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.0 MB (90961721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24d68b6c7724e78acbcd3257a5da30d7add47087f48568fe7c9ef85e592b8ab4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:19 GMT
ADD file:d9efaba9e396cd5732f1689338ef5f1fbb66667806efe9c6938ca7169b305496 in / 
# Wed, 24 Apr 2024 03:28:19 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:12:09 GMT
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
	-	`sha256:646e886fa3cfd015533cf777eb62fc903426f0b57806d1cbaa843f8f07a9f66d`  
		Last Modified: Wed, 24 Apr 2024 03:33:00 GMT  
		Size: 55.1 MB (55098870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a360c5f105e29623d30cc42a1b871c17a19cbafe3ed994b3b64f2449cd1695`  
		Last Modified: Wed, 24 Apr 2024 04:21:57 GMT  
		Size: 15.8 MB (15765279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2911b6cc0f1e670d091d47c3b3d94645c7ee9bbbcac4cd722a6975d1259f394`  
		Last Modified: Wed, 01 May 2024 21:52:30 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67a19b5d179e9e382589fa8874637b0400623133d17781ccf594701cf071375`  
		Last Modified: Wed, 01 May 2024 21:52:30 GMT  
		Size: 20.1 MB (20095234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f626703fcbf241a5c6ad0bd95edc43772b7a5670c85b6e7014ddf0afb49e0c`  
		Last Modified: Wed, 01 May 2024 21:52:30 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e710c4cb00bc1623a1a2adeb9bfe25ec99983af66469432ff0e6eb0c055c34b`  
		Last Modified: Wed, 01 May 2024 21:52:30 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.6-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:6d84247c1540f0afeffaa199972690cbc95d91a1c3f21fdfba506ed6c9b7036c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4529387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b70cf13e76882da37f4b9ff0335dca2166a63b1e7172cddb214a0a59674379a4`

```dockerfile
```

-	Layers:
	-	`sha256:baa8d8f574f120b640863d19fb7415747dfaed909b4dd2bd19b9ccaaaf93ed9d`  
		Last Modified: Wed, 01 May 2024 21:52:30 GMT  
		Size: 4.5 MB (4516183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aba922338572da99f541419fdfa1d7e4135c3db9331c597e2ce26d05ff09aa28`  
		Last Modified: Wed, 01 May 2024 21:52:29 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10.6-meta-alpine`

```console
$ docker pull influxdb@sha256:bd35703ab4676ad52a6860655c6ec97c8ae28a9950e0aa862e4eed0b104a455b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.6-meta-alpine` - linux; amd64

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

### `influxdb:1.10.6-meta-alpine` - unknown; unknown

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

## `influxdb:1.11-data`

```console
$ docker pull influxdb@sha256:d51cf620df9554697b2deace96be5fd07f2593cf440bc3cdc459991166f528c2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data` - linux; amd64

```console
$ docker pull influxdb@sha256:2f8472606afea7cd69332f8d92cf1bbd902223fd5ed3199da9ed514badfc9a50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115452661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db48a5d7ebb5c9fba200c4bd35e05b8a607bf42a1a93308c16edee0313eba306`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 24 Apr 2024 03:27:57 GMT
ADD file:2cc4cba2834c189d0dc41b5d79e1236770862c38452517fcbbb28015b88ab5cf in / 
# Wed, 24 Apr 2024 03:27:57 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:10:26 GMT
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
	-	`sha256:1468e7ff95fcb865fbc4dee7094f8b99c4dcddd6eb2180cf044c7396baf6fc2f`  
		Last Modified: Wed, 24 Apr 2024 03:32:18 GMT  
		Size: 49.6 MB (49576283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf9c2b42f41b1845f3e4421b723d56146db82939dc884555e077768e18132f4`  
		Last Modified: Wed, 24 Apr 2024 04:20:50 GMT  
		Size: 24.1 MB (24050140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97437058c8227b6dd8acb330fe5694efae4788f866950b7a1315395964d34b0b`  
		Last Modified: Wed, 01 May 2024 21:52:36 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644fe3d9627e9b56cf9055cbc3b2302f606536120846becd669eca8a03f84e59`  
		Last Modified: Wed, 01 May 2024 21:52:37 GMT  
		Size: 41.8 MB (41822682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9ad2b5aebe2f742e70696b0a30e998d9f46cac9f711072d3f1ab260674a2e3`  
		Last Modified: Wed, 01 May 2024 21:52:36 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e33ba9a15c631cde01e3cb19888fe0bbb9801a6f981fad4b308de88a3695ff25`  
		Last Modified: Wed, 01 May 2024 21:52:36 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe36487da77941f93f9bad44794ec2fd104f841490df6c076550c4f52ee0adb`  
		Last Modified: Wed, 01 May 2024 21:52:37 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:a0e3d1ab07aa058e64081e1b84e139b494ac87ced81afc81498949f252e354b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4469401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0b7a90ab0b041e0229a55ccd5cfa2c6366e3329dbe1641c3e819a0b6ebd5562`

```dockerfile
```

-	Layers:
	-	`sha256:e0e4914348d3365d6a6583ec4db41bc6d34deb6e9a5a5bde69742970025cb2a9`  
		Last Modified: Wed, 01 May 2024 21:52:36 GMT  
		Size: 4.5 MB (4454545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d7459d86f84bc9eda5378cf3d7ff3e2d797834ca1bde632994a2eb181e2de22`  
		Last Modified: Wed, 01 May 2024 21:52:36 GMT  
		Size: 14.9 KB (14856 bytes)  
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
$ docker pull influxdb@sha256:294891167c5449c15d74df0d7f839616c15ef377eb11de42dea2072cad7be99a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:1f8316beda96099f5a916156d6e38d790f05adf4040abf532aff83d1805490b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (94021815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e767195c32b96043eae438169b929be4d7612ee8a62b2bd2a2d78b17c70f886`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 24 Apr 2024 03:27:57 GMT
ADD file:2cc4cba2834c189d0dc41b5d79e1236770862c38452517fcbbb28015b88ab5cf in / 
# Wed, 24 Apr 2024 03:27:57 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:10:26 GMT
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
	-	`sha256:1468e7ff95fcb865fbc4dee7094f8b99c4dcddd6eb2180cf044c7396baf6fc2f`  
		Last Modified: Wed, 24 Apr 2024 03:32:18 GMT  
		Size: 49.6 MB (49576283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf9c2b42f41b1845f3e4421b723d56146db82939dc884555e077768e18132f4`  
		Last Modified: Wed, 24 Apr 2024 04:20:50 GMT  
		Size: 24.1 MB (24050140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:268259fdcb9d445731fd282ecd104a5f114bdafcdbb92729884835ce0433264c`  
		Last Modified: Wed, 01 May 2024 21:52:36 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99c7657082a06d39acdb4c29fd2c5d839b7cb804ec66814322ea5de5715a07e`  
		Last Modified: Wed, 01 May 2024 21:52:37 GMT  
		Size: 20.4 MB (20393054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c3d1a3d72509a25efad22923829c0e380961d43738c5292fe87d2de0bf8248`  
		Last Modified: Wed, 01 May 2024 21:52:37 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d796cff2bfb3c9d044f4dd6feb15d1c6e3c07d18af87e846a5375b7d8e8f1a`  
		Last Modified: Wed, 01 May 2024 21:52:36 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:06324abb7e9980dabe827ec2e7df22daa4710199533768874a02db166361c984
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4405189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dc76e960e432b35f7586c6dd023d5a1273d5172221e95f204b7a90400e75594`

```dockerfile
```

-	Layers:
	-	`sha256:f810eb8f3f5650f45b93693ebeb1fb42555b47773eceef23e6b211cc33c10313`  
		Last Modified: Wed, 01 May 2024 21:52:37 GMT  
		Size: 4.4 MB (4391985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49724485577df718ae965ad9f3cb603ab20379d70106555c8f090db69d4d715f`  
		Last Modified: Wed, 01 May 2024 21:52:36 GMT  
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
$ docker pull influxdb@sha256:d51cf620df9554697b2deace96be5fd07f2593cf440bc3cdc459991166f528c2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.5-data` - linux; amd64

```console
$ docker pull influxdb@sha256:2f8472606afea7cd69332f8d92cf1bbd902223fd5ed3199da9ed514badfc9a50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115452661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db48a5d7ebb5c9fba200c4bd35e05b8a607bf42a1a93308c16edee0313eba306`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 24 Apr 2024 03:27:57 GMT
ADD file:2cc4cba2834c189d0dc41b5d79e1236770862c38452517fcbbb28015b88ab5cf in / 
# Wed, 24 Apr 2024 03:27:57 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:10:26 GMT
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
	-	`sha256:1468e7ff95fcb865fbc4dee7094f8b99c4dcddd6eb2180cf044c7396baf6fc2f`  
		Last Modified: Wed, 24 Apr 2024 03:32:18 GMT  
		Size: 49.6 MB (49576283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf9c2b42f41b1845f3e4421b723d56146db82939dc884555e077768e18132f4`  
		Last Modified: Wed, 24 Apr 2024 04:20:50 GMT  
		Size: 24.1 MB (24050140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97437058c8227b6dd8acb330fe5694efae4788f866950b7a1315395964d34b0b`  
		Last Modified: Wed, 01 May 2024 21:52:36 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644fe3d9627e9b56cf9055cbc3b2302f606536120846becd669eca8a03f84e59`  
		Last Modified: Wed, 01 May 2024 21:52:37 GMT  
		Size: 41.8 MB (41822682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9ad2b5aebe2f742e70696b0a30e998d9f46cac9f711072d3f1ab260674a2e3`  
		Last Modified: Wed, 01 May 2024 21:52:36 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e33ba9a15c631cde01e3cb19888fe0bbb9801a6f981fad4b308de88a3695ff25`  
		Last Modified: Wed, 01 May 2024 21:52:36 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe36487da77941f93f9bad44794ec2fd104f841490df6c076550c4f52ee0adb`  
		Last Modified: Wed, 01 May 2024 21:52:37 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.5-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:a0e3d1ab07aa058e64081e1b84e139b494ac87ced81afc81498949f252e354b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4469401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0b7a90ab0b041e0229a55ccd5cfa2c6366e3329dbe1641c3e819a0b6ebd5562`

```dockerfile
```

-	Layers:
	-	`sha256:e0e4914348d3365d6a6583ec4db41bc6d34deb6e9a5a5bde69742970025cb2a9`  
		Last Modified: Wed, 01 May 2024 21:52:36 GMT  
		Size: 4.5 MB (4454545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d7459d86f84bc9eda5378cf3d7ff3e2d797834ca1bde632994a2eb181e2de22`  
		Last Modified: Wed, 01 May 2024 21:52:36 GMT  
		Size: 14.9 KB (14856 bytes)  
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
$ docker pull influxdb@sha256:294891167c5449c15d74df0d7f839616c15ef377eb11de42dea2072cad7be99a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.5-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:1f8316beda96099f5a916156d6e38d790f05adf4040abf532aff83d1805490b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (94021815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e767195c32b96043eae438169b929be4d7612ee8a62b2bd2a2d78b17c70f886`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 24 Apr 2024 03:27:57 GMT
ADD file:2cc4cba2834c189d0dc41b5d79e1236770862c38452517fcbbb28015b88ab5cf in / 
# Wed, 24 Apr 2024 03:27:57 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:10:26 GMT
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
	-	`sha256:1468e7ff95fcb865fbc4dee7094f8b99c4dcddd6eb2180cf044c7396baf6fc2f`  
		Last Modified: Wed, 24 Apr 2024 03:32:18 GMT  
		Size: 49.6 MB (49576283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf9c2b42f41b1845f3e4421b723d56146db82939dc884555e077768e18132f4`  
		Last Modified: Wed, 24 Apr 2024 04:20:50 GMT  
		Size: 24.1 MB (24050140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:268259fdcb9d445731fd282ecd104a5f114bdafcdbb92729884835ce0433264c`  
		Last Modified: Wed, 01 May 2024 21:52:36 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99c7657082a06d39acdb4c29fd2c5d839b7cb804ec66814322ea5de5715a07e`  
		Last Modified: Wed, 01 May 2024 21:52:37 GMT  
		Size: 20.4 MB (20393054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c3d1a3d72509a25efad22923829c0e380961d43738c5292fe87d2de0bf8248`  
		Last Modified: Wed, 01 May 2024 21:52:37 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d796cff2bfb3c9d044f4dd6feb15d1c6e3c07d18af87e846a5375b7d8e8f1a`  
		Last Modified: Wed, 01 May 2024 21:52:36 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.5-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:06324abb7e9980dabe827ec2e7df22daa4710199533768874a02db166361c984
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4405189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dc76e960e432b35f7586c6dd023d5a1273d5172221e95f204b7a90400e75594`

```dockerfile
```

-	Layers:
	-	`sha256:f810eb8f3f5650f45b93693ebeb1fb42555b47773eceef23e6b211cc33c10313`  
		Last Modified: Wed, 01 May 2024 21:52:37 GMT  
		Size: 4.4 MB (4391985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49724485577df718ae965ad9f3cb603ab20379d70106555c8f090db69d4d715f`  
		Last Modified: Wed, 01 May 2024 21:52:36 GMT  
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
$ docker pull influxdb@sha256:675da300cf089bdc1f1c2e042b14454099c90a87fd58a42798b5fbfde8c529cb
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
$ docker pull influxdb@sha256:5ec6521a12e2f2eed8411df1d808962a2dbd137dfd7a29ce490da3958b88f939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125753021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a032878f5755b60ee55b1146e80908c54b905076a18c176057df75bc3ddb387`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:19 GMT
ADD file:d9efaba9e396cd5732f1689338ef5f1fbb66667806efe9c6938ca7169b305496 in / 
# Wed, 24 Apr 2024 03:28:19 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:12:09 GMT
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
	-	`sha256:646e886fa3cfd015533cf777eb62fc903426f0b57806d1cbaa843f8f07a9f66d`  
		Last Modified: Wed, 24 Apr 2024 03:33:00 GMT  
		Size: 55.1 MB (55098870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a360c5f105e29623d30cc42a1b871c17a19cbafe3ed994b3b64f2449cd1695`  
		Last Modified: Wed, 24 Apr 2024 04:21:57 GMT  
		Size: 15.8 MB (15765279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d474c7f1a4964353ab177e682105b1a6e0c2b51e2a21933c8c9cb46aad9b5b34`  
		Last Modified: Wed, 01 May 2024 21:52:27 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:598bb092688a83b44e56fa06e5f40fda7863419030eb4b6e6bfd7e5e70151fb1`  
		Last Modified: Wed, 01 May 2024 21:52:26 GMT  
		Size: 54.9 MB (54885370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357763ac263d00886db0eadf3380553a4a3d1c10f7e4b1933c1e4fe748389202`  
		Last Modified: Wed, 01 May 2024 21:52:25 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132a69027bec5b2470487aa2245ec6f4c93f9fed61b84b61def0c213d9b11b72`  
		Last Modified: Wed, 01 May 2024 21:52:25 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895c695cdc78d07c0252417f1b5767e5b48915e0a118b1504436cf3502994acc`  
		Last Modified: Wed, 01 May 2024 21:52:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:229010a23080ad063f2e6c244880747c970208ae4c98e6feae50872370c92b72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4478762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1d6a5ab1e9e8b4ac1c98b3deea35e888e20333bb213f4eb22cbb1aaca1ccb7d`

```dockerfile
```

-	Layers:
	-	`sha256:f6801b8b19d575a09c713053d45e9784f663f3fb6446c553a8055a9f0d056c13`  
		Last Modified: Wed, 01 May 2024 21:52:25 GMT  
		Size: 4.5 MB (4463018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6d7fb873e15af6759965e625861831474b34815b0133d9e4c4d2a9045bbc2d6`  
		Last Modified: Wed, 01 May 2024 21:52:25 GMT  
		Size: 15.7 KB (15744 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.8` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:864ae9fa94c6c78e0f5958d06eb86ef1f354b4588d14afaf4f6f310a18835455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116752369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb9577234ba4c6a2d7cfd077b391c43cb33ac61f623399a6c53e5498f58fda83`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:15 GMT
ADD file:59046a1e0987059e779fff5a0f35e03203c109d778a75058e9474705d3fcfdff in / 
# Wed, 24 Apr 2024 04:07:15 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:51:56 GMT
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
	-	`sha256:853e2341066ebc3a07d3c44ebac8c3ce40daf429fb9cc3f49f2d35115e9cc93f`  
		Last Modified: Wed, 24 Apr 2024 04:11:34 GMT  
		Size: 50.3 MB (50255574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5d5c1aa98981d0ab503d79e97e4eeed8435372346757065a98c291d66c74df`  
		Last Modified: Wed, 24 Apr 2024 05:03:57 GMT  
		Size: 14.9 MB (14880390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e50bff0ac925c8cd845ef2f7ccd280cb94adb215a6c0655472bfa1ab8116a18`  
		Last Modified: Wed, 01 May 2024 22:10:35 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518b5747df900233bd576532ccc0f4bf49fd6cd12dd5888904312342a46dbc65`  
		Last Modified: Wed, 01 May 2024 22:10:38 GMT  
		Size: 51.6 MB (51612898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa58f4a93d0c83bce78e6e48a5f11c34da55c23dee2d6b2163e69b1102fea30`  
		Last Modified: Wed, 01 May 2024 22:10:35 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea83fc4791895d49d887a2093a70db3cd2a66a5b5969d7a161a9528e17ae40a`  
		Last Modified: Wed, 01 May 2024 22:10:35 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69efd70d0dc3d9efd3b5676bb6d656a69717b70c179d59bb6c4f5cfd71099899`  
		Last Modified: Wed, 01 May 2024 22:10:37 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:71733c12ff7e0ce28be64b6b35917514b9f3c8e2a74db8e37983d34d69e7d7da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4480464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f44d7e0b517112b6c56849b987e27cbc41fd0b17f3ee4abf0ca25c9ab339429`

```dockerfile
```

-	Layers:
	-	`sha256:76b0bb386c02bef2854346b418e875cc5d8196cf0b0c648c2778f594ff95d14c`  
		Last Modified: Wed, 01 May 2024 22:10:36 GMT  
		Size: 4.5 MB (4464652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96507ea2960a4989ca67bff0bfed677fb3898e162aba0e9f4c373ce029866a27`  
		Last Modified: Wed, 01 May 2024 22:10:35 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:7a0c1286c2e4d3dd08897a4702df232c5c2c98bc072dee9ead1e0e0ebe7ccf07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120723938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c751f5c6b4f1c91c2642175abea699b95ec37a1f26f5a61c8372bd76efa347f9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:46 GMT
ADD file:3ebbb50438ec23ebe0c880a5421d505922771b7bd4202b5c8f839702dd726036 in / 
# Wed, 24 Apr 2024 04:10:46 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:33:39 GMT
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
	-	`sha256:64d502aff46d2ed56e6228994304818b354d02b13d6122492c5d3e0886c92897`  
		Last Modified: Wed, 24 Apr 2024 04:14:26 GMT  
		Size: 53.7 MB (53739959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33008ff0928e624ce22cedd5d004edd66b80372bfd1223e8900206330213ee34`  
		Last Modified: Wed, 24 Apr 2024 08:42:31 GMT  
		Size: 15.8 MB (15750623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b71cfaee0e75c41c3b90577f1ac53ef69b183a5c9796e111efe63906186c464`  
		Last Modified: Wed, 01 May 2024 22:29:03 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfb29ff3c405cda917f2d432a1dfee03e08c21a8dbc2e826a39399b43f8ec11`  
		Last Modified: Wed, 01 May 2024 22:29:04 GMT  
		Size: 51.2 MB (51229868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0296797cfe6ff6f85716512677044b23381da6941c49c60ad9f317bdc1e3b81`  
		Last Modified: Wed, 01 May 2024 22:29:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb70c490269d3aa859879cd50c080a7d61c58c06f64dba3275defda800d19c3`  
		Last Modified: Wed, 01 May 2024 22:29:03 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c8428f58c7344bd5a61aff44b9cffeede1107e477d6897cb1e03274bc04a51`  
		Last Modified: Wed, 01 May 2024 22:29:04 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:1a433bd35d328e7c5798f110c47059ace9a12ecb0330958935f5a2fd0a098f10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4478355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97b1fe0fe106688518c73792e79c4a631249a4f43b6f94d0df30b805cc551daf`

```dockerfile
```

-	Layers:
	-	`sha256:d4d8c7593da0a62c20376c1cc0160fe6c5ca18347ad86608eaec9a2d70b83f4b`  
		Last Modified: Wed, 01 May 2024 22:29:03 GMT  
		Size: 4.5 MB (4462605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec4c5562eaf0df7c8e849dfe69cd7d14d962aad4f7414c963a8b7905cf71eb4f`  
		Last Modified: Wed, 01 May 2024 22:29:03 GMT  
		Size: 15.8 KB (15750 bytes)  
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
$ docker pull influxdb@sha256:675da300cf089bdc1f1c2e042b14454099c90a87fd58a42798b5fbfde8c529cb
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
$ docker pull influxdb@sha256:5ec6521a12e2f2eed8411df1d808962a2dbd137dfd7a29ce490da3958b88f939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125753021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a032878f5755b60ee55b1146e80908c54b905076a18c176057df75bc3ddb387`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:19 GMT
ADD file:d9efaba9e396cd5732f1689338ef5f1fbb66667806efe9c6938ca7169b305496 in / 
# Wed, 24 Apr 2024 03:28:19 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:12:09 GMT
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
	-	`sha256:646e886fa3cfd015533cf777eb62fc903426f0b57806d1cbaa843f8f07a9f66d`  
		Last Modified: Wed, 24 Apr 2024 03:33:00 GMT  
		Size: 55.1 MB (55098870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a360c5f105e29623d30cc42a1b871c17a19cbafe3ed994b3b64f2449cd1695`  
		Last Modified: Wed, 24 Apr 2024 04:21:57 GMT  
		Size: 15.8 MB (15765279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d474c7f1a4964353ab177e682105b1a6e0c2b51e2a21933c8c9cb46aad9b5b34`  
		Last Modified: Wed, 01 May 2024 21:52:27 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:598bb092688a83b44e56fa06e5f40fda7863419030eb4b6e6bfd7e5e70151fb1`  
		Last Modified: Wed, 01 May 2024 21:52:26 GMT  
		Size: 54.9 MB (54885370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357763ac263d00886db0eadf3380553a4a3d1c10f7e4b1933c1e4fe748389202`  
		Last Modified: Wed, 01 May 2024 21:52:25 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132a69027bec5b2470487aa2245ec6f4c93f9fed61b84b61def0c213d9b11b72`  
		Last Modified: Wed, 01 May 2024 21:52:25 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895c695cdc78d07c0252417f1b5767e5b48915e0a118b1504436cf3502994acc`  
		Last Modified: Wed, 01 May 2024 21:52:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8.10` - unknown; unknown

```console
$ docker pull influxdb@sha256:229010a23080ad063f2e6c244880747c970208ae4c98e6feae50872370c92b72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4478762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1d6a5ab1e9e8b4ac1c98b3deea35e888e20333bb213f4eb22cbb1aaca1ccb7d`

```dockerfile
```

-	Layers:
	-	`sha256:f6801b8b19d575a09c713053d45e9784f663f3fb6446c553a8055a9f0d056c13`  
		Last Modified: Wed, 01 May 2024 21:52:25 GMT  
		Size: 4.5 MB (4463018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6d7fb873e15af6759965e625861831474b34815b0133d9e4c4d2a9045bbc2d6`  
		Last Modified: Wed, 01 May 2024 21:52:25 GMT  
		Size: 15.7 KB (15744 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.8.10` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:864ae9fa94c6c78e0f5958d06eb86ef1f354b4588d14afaf4f6f310a18835455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116752369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb9577234ba4c6a2d7cfd077b391c43cb33ac61f623399a6c53e5498f58fda83`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:15 GMT
ADD file:59046a1e0987059e779fff5a0f35e03203c109d778a75058e9474705d3fcfdff in / 
# Wed, 24 Apr 2024 04:07:15 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:51:56 GMT
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
	-	`sha256:853e2341066ebc3a07d3c44ebac8c3ce40daf429fb9cc3f49f2d35115e9cc93f`  
		Last Modified: Wed, 24 Apr 2024 04:11:34 GMT  
		Size: 50.3 MB (50255574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5d5c1aa98981d0ab503d79e97e4eeed8435372346757065a98c291d66c74df`  
		Last Modified: Wed, 24 Apr 2024 05:03:57 GMT  
		Size: 14.9 MB (14880390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e50bff0ac925c8cd845ef2f7ccd280cb94adb215a6c0655472bfa1ab8116a18`  
		Last Modified: Wed, 01 May 2024 22:10:35 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518b5747df900233bd576532ccc0f4bf49fd6cd12dd5888904312342a46dbc65`  
		Last Modified: Wed, 01 May 2024 22:10:38 GMT  
		Size: 51.6 MB (51612898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa58f4a93d0c83bce78e6e48a5f11c34da55c23dee2d6b2163e69b1102fea30`  
		Last Modified: Wed, 01 May 2024 22:10:35 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea83fc4791895d49d887a2093a70db3cd2a66a5b5969d7a161a9528e17ae40a`  
		Last Modified: Wed, 01 May 2024 22:10:35 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69efd70d0dc3d9efd3b5676bb6d656a69717b70c179d59bb6c4f5cfd71099899`  
		Last Modified: Wed, 01 May 2024 22:10:37 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8.10` - unknown; unknown

```console
$ docker pull influxdb@sha256:71733c12ff7e0ce28be64b6b35917514b9f3c8e2a74db8e37983d34d69e7d7da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4480464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f44d7e0b517112b6c56849b987e27cbc41fd0b17f3ee4abf0ca25c9ab339429`

```dockerfile
```

-	Layers:
	-	`sha256:76b0bb386c02bef2854346b418e875cc5d8196cf0b0c648c2778f594ff95d14c`  
		Last Modified: Wed, 01 May 2024 22:10:36 GMT  
		Size: 4.5 MB (4464652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96507ea2960a4989ca67bff0bfed677fb3898e162aba0e9f4c373ce029866a27`  
		Last Modified: Wed, 01 May 2024 22:10:35 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.8.10` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:7a0c1286c2e4d3dd08897a4702df232c5c2c98bc072dee9ead1e0e0ebe7ccf07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120723938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c751f5c6b4f1c91c2642175abea699b95ec37a1f26f5a61c8372bd76efa347f9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:46 GMT
ADD file:3ebbb50438ec23ebe0c880a5421d505922771b7bd4202b5c8f839702dd726036 in / 
# Wed, 24 Apr 2024 04:10:46 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:33:39 GMT
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
	-	`sha256:64d502aff46d2ed56e6228994304818b354d02b13d6122492c5d3e0886c92897`  
		Last Modified: Wed, 24 Apr 2024 04:14:26 GMT  
		Size: 53.7 MB (53739959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33008ff0928e624ce22cedd5d004edd66b80372bfd1223e8900206330213ee34`  
		Last Modified: Wed, 24 Apr 2024 08:42:31 GMT  
		Size: 15.8 MB (15750623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b71cfaee0e75c41c3b90577f1ac53ef69b183a5c9796e111efe63906186c464`  
		Last Modified: Wed, 01 May 2024 22:29:03 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfb29ff3c405cda917f2d432a1dfee03e08c21a8dbc2e826a39399b43f8ec11`  
		Last Modified: Wed, 01 May 2024 22:29:04 GMT  
		Size: 51.2 MB (51229868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0296797cfe6ff6f85716512677044b23381da6941c49c60ad9f317bdc1e3b81`  
		Last Modified: Wed, 01 May 2024 22:29:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb70c490269d3aa859879cd50c080a7d61c58c06f64dba3275defda800d19c3`  
		Last Modified: Wed, 01 May 2024 22:29:03 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c8428f58c7344bd5a61aff44b9cffeede1107e477d6897cb1e03274bc04a51`  
		Last Modified: Wed, 01 May 2024 22:29:04 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8.10` - unknown; unknown

```console
$ docker pull influxdb@sha256:1a433bd35d328e7c5798f110c47059ace9a12ecb0330958935f5a2fd0a098f10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4478355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97b1fe0fe106688518c73792e79c4a631249a4f43b6f94d0df30b805cc551daf`

```dockerfile
```

-	Layers:
	-	`sha256:d4d8c7593da0a62c20376c1cc0160fe6c5ca18347ad86608eaec9a2d70b83f4b`  
		Last Modified: Wed, 01 May 2024 22:29:03 GMT  
		Size: 4.5 MB (4462605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec4c5562eaf0df7c8e849dfe69cd7d14d962aad4f7414c963a8b7905cf71eb4f`  
		Last Modified: Wed, 01 May 2024 22:29:03 GMT  
		Size: 15.8 KB (15750 bytes)  
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
$ docker pull influxdb@sha256:0f9812b39cdf2ef0a728412eebac5b5bc4b84572ced60e0bf416626b2732896f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9-data` - linux; amd64

```console
$ docker pull influxdb@sha256:a521a8f110323a409a42bc155bebc387f633f73ba6e1892e2556d72b1f0f33c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 MB (104156686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6e109811053bfcae03d9104c9fe746641ca303f3620c55ae5ad257a1d885bbe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:19 GMT
ADD file:d9efaba9e396cd5732f1689338ef5f1fbb66667806efe9c6938ca7169b305496 in / 
# Wed, 24 Apr 2024 03:28:19 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:12:09 GMT
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
	-	`sha256:646e886fa3cfd015533cf777eb62fc903426f0b57806d1cbaa843f8f07a9f66d`  
		Last Modified: Wed, 24 Apr 2024 03:33:00 GMT  
		Size: 55.1 MB (55098870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a360c5f105e29623d30cc42a1b871c17a19cbafe3ed994b3b64f2449cd1695`  
		Last Modified: Wed, 24 Apr 2024 04:21:57 GMT  
		Size: 15.8 MB (15765279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6bd81781d6e2fbf347602c9736f83bf07680dd3494535e8d078709bbe7e1bc`  
		Last Modified: Wed, 01 May 2024 21:52:34 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5261984873c1de9727014a69c2d4ffaa2264733d0a855760f626f770c656be5`  
		Last Modified: Wed, 01 May 2024 21:52:35 GMT  
		Size: 33.3 MB (33288978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5f8c05135162f205a2b4cf04d2e6ee329c3d819e64a9aea4424fd2ad519e94`  
		Last Modified: Wed, 01 May 2024 21:52:34 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80694f3969856d54e56c118148109d9f508c74ea6e1cebe94335d87d0475b958`  
		Last Modified: Wed, 01 May 2024 21:52:27 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a25b9c74b63ac6b2c55d7d7fd1cd6eb18c2584dc0fcbbd811fcddeadbdac63`  
		Last Modified: Wed, 01 May 2024 21:52:27 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:600aae85c719f150203b2ab104d56eb0e3863758f4ca37426714cdb3c8bf5533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4584846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6b7faf3562288b5b2144a4a5c01f2794c87148b74b41cf67088872fadd573cb`

```dockerfile
```

-	Layers:
	-	`sha256:08b958270ce5b11a417c9277c3d48b459b2793a6ae33c78e348e012f7c96f388`  
		Last Modified: Wed, 01 May 2024 21:52:34 GMT  
		Size: 4.6 MB (4570022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13602e30bdcb8a244d3050b279c2dc57435bba9c0981b021e87d4cf8c26c82cb`  
		Last Modified: Wed, 01 May 2024 21:52:34 GMT  
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
$ docker pull influxdb@sha256:8fcecf5070ae71937ab1dde2ae0087e9b671c66a2d8facd89a702b6ee9c7509f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:98acae07c25ee31c0cdd1bcc2198c206165129359b449508eea5ac082acab48b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83635874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb19ee6bd260bf8367c7227060e6c355bd4f7702d7ec2bf37fd37ac02035c638`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:19 GMT
ADD file:d9efaba9e396cd5732f1689338ef5f1fbb66667806efe9c6938ca7169b305496 in / 
# Wed, 24 Apr 2024 03:28:19 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:12:09 GMT
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
	-	`sha256:646e886fa3cfd015533cf777eb62fc903426f0b57806d1cbaa843f8f07a9f66d`  
		Last Modified: Wed, 24 Apr 2024 03:33:00 GMT  
		Size: 55.1 MB (55098870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a360c5f105e29623d30cc42a1b871c17a19cbafe3ed994b3b64f2449cd1695`  
		Last Modified: Wed, 24 Apr 2024 04:21:57 GMT  
		Size: 15.8 MB (15765279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee1f33516642e2c3e81e301a5578193234ddc77a87ea6348a833d01089ec7f5`  
		Last Modified: Wed, 01 May 2024 21:52:30 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cfaf18eb35600238f81d1df33ab421083b9500262385bc020bfa685f5008a6`  
		Last Modified: Wed, 01 May 2024 21:52:31 GMT  
		Size: 12.8 MB (12769374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c52c892a2ff5ece0b9d8d001693d9f388ec6b36a21b3ecfb6c2e9505cde2ff`  
		Last Modified: Wed, 01 May 2024 21:52:30 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d3ae9c193af70597f2b5ba871aec0d5cc55200a69a43a2db7cf77b6add50f8`  
		Last Modified: Wed, 01 May 2024 21:52:23 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:4d9488cd70b6cc099e6ca64e1fc08035d79b2f12a47edaf1971daa30682b1e75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4529322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a0d72d28239fa8ed10ed03e5bdffdbbd9066bc42c437eea3fea7fd4224a4bf8`

```dockerfile
```

-	Layers:
	-	`sha256:63c4b1bc1f9358e5c408e4d828a522614f39c98508be9aa5916046fb86a94d14`  
		Last Modified: Wed, 01 May 2024 21:52:30 GMT  
		Size: 4.5 MB (4516151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a2fda5a4208bbac1a6b34c1acc711f1f87b438f8eb096d0ab04fdd5618b11f2`  
		Last Modified: Wed, 01 May 2024 21:52:30 GMT  
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
$ docker pull influxdb@sha256:0f9812b39cdf2ef0a728412eebac5b5bc4b84572ced60e0bf416626b2732896f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9.13-data` - linux; amd64

```console
$ docker pull influxdb@sha256:a521a8f110323a409a42bc155bebc387f633f73ba6e1892e2556d72b1f0f33c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 MB (104156686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6e109811053bfcae03d9104c9fe746641ca303f3620c55ae5ad257a1d885bbe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:19 GMT
ADD file:d9efaba9e396cd5732f1689338ef5f1fbb66667806efe9c6938ca7169b305496 in / 
# Wed, 24 Apr 2024 03:28:19 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:12:09 GMT
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
	-	`sha256:646e886fa3cfd015533cf777eb62fc903426f0b57806d1cbaa843f8f07a9f66d`  
		Last Modified: Wed, 24 Apr 2024 03:33:00 GMT  
		Size: 55.1 MB (55098870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a360c5f105e29623d30cc42a1b871c17a19cbafe3ed994b3b64f2449cd1695`  
		Last Modified: Wed, 24 Apr 2024 04:21:57 GMT  
		Size: 15.8 MB (15765279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6bd81781d6e2fbf347602c9736f83bf07680dd3494535e8d078709bbe7e1bc`  
		Last Modified: Wed, 01 May 2024 21:52:34 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5261984873c1de9727014a69c2d4ffaa2264733d0a855760f626f770c656be5`  
		Last Modified: Wed, 01 May 2024 21:52:35 GMT  
		Size: 33.3 MB (33288978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5f8c05135162f205a2b4cf04d2e6ee329c3d819e64a9aea4424fd2ad519e94`  
		Last Modified: Wed, 01 May 2024 21:52:34 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80694f3969856d54e56c118148109d9f508c74ea6e1cebe94335d87d0475b958`  
		Last Modified: Wed, 01 May 2024 21:52:27 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a25b9c74b63ac6b2c55d7d7fd1cd6eb18c2584dc0fcbbd811fcddeadbdac63`  
		Last Modified: Wed, 01 May 2024 21:52:27 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9.13-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:600aae85c719f150203b2ab104d56eb0e3863758f4ca37426714cdb3c8bf5533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4584846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6b7faf3562288b5b2144a4a5c01f2794c87148b74b41cf67088872fadd573cb`

```dockerfile
```

-	Layers:
	-	`sha256:08b958270ce5b11a417c9277c3d48b459b2793a6ae33c78e348e012f7c96f388`  
		Last Modified: Wed, 01 May 2024 21:52:34 GMT  
		Size: 4.6 MB (4570022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13602e30bdcb8a244d3050b279c2dc57435bba9c0981b021e87d4cf8c26c82cb`  
		Last Modified: Wed, 01 May 2024 21:52:34 GMT  
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
$ docker pull influxdb@sha256:8fcecf5070ae71937ab1dde2ae0087e9b671c66a2d8facd89a702b6ee9c7509f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9.13-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:98acae07c25ee31c0cdd1bcc2198c206165129359b449508eea5ac082acab48b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83635874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb19ee6bd260bf8367c7227060e6c355bd4f7702d7ec2bf37fd37ac02035c638`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:19 GMT
ADD file:d9efaba9e396cd5732f1689338ef5f1fbb66667806efe9c6938ca7169b305496 in / 
# Wed, 24 Apr 2024 03:28:19 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:12:09 GMT
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
	-	`sha256:646e886fa3cfd015533cf777eb62fc903426f0b57806d1cbaa843f8f07a9f66d`  
		Last Modified: Wed, 24 Apr 2024 03:33:00 GMT  
		Size: 55.1 MB (55098870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a360c5f105e29623d30cc42a1b871c17a19cbafe3ed994b3b64f2449cd1695`  
		Last Modified: Wed, 24 Apr 2024 04:21:57 GMT  
		Size: 15.8 MB (15765279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee1f33516642e2c3e81e301a5578193234ddc77a87ea6348a833d01089ec7f5`  
		Last Modified: Wed, 01 May 2024 21:52:30 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cfaf18eb35600238f81d1df33ab421083b9500262385bc020bfa685f5008a6`  
		Last Modified: Wed, 01 May 2024 21:52:31 GMT  
		Size: 12.8 MB (12769374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c52c892a2ff5ece0b9d8d001693d9f388ec6b36a21b3ecfb6c2e9505cde2ff`  
		Last Modified: Wed, 01 May 2024 21:52:30 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d3ae9c193af70597f2b5ba871aec0d5cc55200a69a43a2db7cf77b6add50f8`  
		Last Modified: Wed, 01 May 2024 21:52:23 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9.13-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:4d9488cd70b6cc099e6ca64e1fc08035d79b2f12a47edaf1971daa30682b1e75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4529322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a0d72d28239fa8ed10ed03e5bdffdbbd9066bc42c437eea3fea7fd4224a4bf8`

```dockerfile
```

-	Layers:
	-	`sha256:63c4b1bc1f9358e5c408e4d828a522614f39c98508be9aa5916046fb86a94d14`  
		Last Modified: Wed, 01 May 2024 21:52:30 GMT  
		Size: 4.5 MB (4516151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a2fda5a4208bbac1a6b34c1acc711f1f87b438f8eb096d0ab04fdd5618b11f2`  
		Last Modified: Wed, 01 May 2024 21:52:30 GMT  
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
$ docker pull influxdb@sha256:0b41fd998977efbe7df986e03c0932e64f74ed347ea68356289ee32ee31d4499
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2` - linux; amd64

```console
$ docker pull influxdb@sha256:b18296633f4c6368ed9ef0687defa1a414c94df613779d0444ee0d49b2ebcf90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (163963626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2347a667f34c96dd2bb711053800ded152012feae7a05a6fc33bad80aa435f21`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
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
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f73b2c3fb487d40499c1ddcbd6b518e4d8f9d17588acd9ad4c02cd58251477`  
		Last Modified: Wed, 01 May 2024 21:52:44 GMT  
		Size: 9.6 MB (9592087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b7ed840e23249ffb1cb2794c456e2b7a1d626900ae2f1e63aa23cd7b1907d0`  
		Last Modified: Wed, 01 May 2024 21:52:44 GMT  
		Size: 5.8 MB (5820924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e75552013d14f57e219b93a76ed4df639bb842330ae49e704cb554119cf4a6f`  
		Last Modified: Wed, 01 May 2024 21:52:44 GMT  
		Size: 3.2 KB (3232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b464a6ebd22a5d1c9f1e1c3a52c594b5863b462211628441a2ccc76626164e69`  
		Last Modified: Wed, 01 May 2024 21:52:44 GMT  
		Size: 1.0 MB (1006371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b71d89d0ea33d46a7a892759f2c23eeabe413caf3e84135af58c33c4757a50`  
		Last Modified: Wed, 01 May 2024 21:52:46 GMT  
		Size: 95.3 MB (95255493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f644c99e19f312326f23a72bd1aaafef67938bf354c711d5153dd6cbc461bd85`  
		Last Modified: Wed, 01 May 2024 21:52:45 GMT  
		Size: 23.1 MB (23128314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fedcea28a4aac63ae903531bd9797dbca1615a7c6b12a6c79fbf0a7306c0fb1`  
		Last Modified: Wed, 01 May 2024 21:52:45 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7ec675151b106c895ee0f29dd1d7438c4f86d0bfb8cf7940b571d0d4b60f1f`  
		Last Modified: Wed, 01 May 2024 21:52:45 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96bda8c59435efec7af66f8691bd57e40ea998e22466a425af541540373b5318`  
		Last Modified: Wed, 01 May 2024 21:52:46 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:e68563ef4e2a5f93a1630b6c22d74b79d3308904310a960fd05236b67ccb1f51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2788865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:230ae31659ae3ccfed8bcdff75e994a480170805d1fac7b67c827c46df8dd3db`

```dockerfile
```

-	Layers:
	-	`sha256:9dbcaacc5cb243d0ad977294d450f14bb16bebc8fbc839512dff8c0455a88110`  
		Last Modified: Wed, 01 May 2024 21:52:44 GMT  
		Size: 2.8 MB (2755207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0190dac23a81f514f5cc9f82d9e5a4c3e251ca54c6488d6d6772faaa158552fd`  
		Last Modified: Wed, 01 May 2024 21:52:44 GMT  
		Size: 33.7 KB (33658 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:699bc7cf026d3cccc062d6eca5bb3885afd049805c1404bd22a1d0b848e32de5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 MB (158094435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:376f599e99efeccbea38563b17aabf1e993c84f2d34dd48295677f9c96c1ed64`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
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
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40563ea69cbff5c1a45dc75899f1920a44d187519177c04caa3e0f5f138a8c8a`  
		Last Modified: Wed, 01 May 2024 22:29:50 GMT  
		Size: 9.4 MB (9388782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28c661e904ab15890c4a25b4217fab8234fc61bf4e1c058df70093905fbec24`  
		Last Modified: Wed, 01 May 2024 22:29:50 GMT  
		Size: 5.5 MB (5463797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe9a655a4caf7037c6216f987e7ea1c8fcbe01415474fce2e85ae098fcbafdf`  
		Last Modified: Wed, 01 May 2024 22:29:49 GMT  
		Size: 3.2 KB (3238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf7d30f7eda7ceb44953d13f39d62db35a2ca13a0ba19e88682ca879010fe27`  
		Last Modified: Wed, 01 May 2024 22:29:50 GMT  
		Size: 936.1 KB (936106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a6c1ba5bd8bdd375ee2ddc8bd62fa973e7ad9ed6e3449be80e7efa989f374e`  
		Last Modified: Wed, 01 May 2024 22:29:53 GMT  
		Size: 91.5 MB (91453330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fb235dfc2b03bcc24acbdc416c33dec3257d88ae34cc37dbd77d82339c6482`  
		Last Modified: Wed, 01 May 2024 22:29:52 GMT  
		Size: 21.7 MB (21662518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7b1954b4b11866cd6f33aac1578f4f63da2b9a87dbf7aa3a750444fa5fb191`  
		Last Modified: Wed, 01 May 2024 22:29:51 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80783551125bd030a5b4801fe8a543f9992dfd78cc8167287f8ae7f0bdace9ed`  
		Last Modified: Wed, 01 May 2024 22:29:51 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2745e5c37bcf74a3f4367693b5b8614ee22f8acdba508ac87dd077ee2f643b4e`  
		Last Modified: Wed, 01 May 2024 22:29:52 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:763bbeb6a5448752089fa864751e6a65218cfe71820b613c0ef24d493615248f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2788036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2d633e6c24b200747f5250a8fe360118217b18a2a11e2682f806b2eb3146afc`

```dockerfile
```

-	Layers:
	-	`sha256:ddce326635feac46d03bcc4edf86da3df7acd27e90b4d375d9a3d3b1381a1bb5`  
		Last Modified: Wed, 01 May 2024 22:29:50 GMT  
		Size: 2.8 MB (2754542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ee75260e7b456b1e3b48a502858dda3e0be6db7bb9bf26b87c6dff2b2e4bdb3`  
		Last Modified: Wed, 01 May 2024 22:29:49 GMT  
		Size: 33.5 KB (33494 bytes)  
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
$ docker pull influxdb@sha256:0b41fd998977efbe7df986e03c0932e64f74ed347ea68356289ee32ee31d4499
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7` - linux; amd64

```console
$ docker pull influxdb@sha256:b18296633f4c6368ed9ef0687defa1a414c94df613779d0444ee0d49b2ebcf90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (163963626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2347a667f34c96dd2bb711053800ded152012feae7a05a6fc33bad80aa435f21`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
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
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f73b2c3fb487d40499c1ddcbd6b518e4d8f9d17588acd9ad4c02cd58251477`  
		Last Modified: Wed, 01 May 2024 21:52:44 GMT  
		Size: 9.6 MB (9592087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b7ed840e23249ffb1cb2794c456e2b7a1d626900ae2f1e63aa23cd7b1907d0`  
		Last Modified: Wed, 01 May 2024 21:52:44 GMT  
		Size: 5.8 MB (5820924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e75552013d14f57e219b93a76ed4df639bb842330ae49e704cb554119cf4a6f`  
		Last Modified: Wed, 01 May 2024 21:52:44 GMT  
		Size: 3.2 KB (3232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b464a6ebd22a5d1c9f1e1c3a52c594b5863b462211628441a2ccc76626164e69`  
		Last Modified: Wed, 01 May 2024 21:52:44 GMT  
		Size: 1.0 MB (1006371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b71d89d0ea33d46a7a892759f2c23eeabe413caf3e84135af58c33c4757a50`  
		Last Modified: Wed, 01 May 2024 21:52:46 GMT  
		Size: 95.3 MB (95255493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f644c99e19f312326f23a72bd1aaafef67938bf354c711d5153dd6cbc461bd85`  
		Last Modified: Wed, 01 May 2024 21:52:45 GMT  
		Size: 23.1 MB (23128314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fedcea28a4aac63ae903531bd9797dbca1615a7c6b12a6c79fbf0a7306c0fb1`  
		Last Modified: Wed, 01 May 2024 21:52:45 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7ec675151b106c895ee0f29dd1d7438c4f86d0bfb8cf7940b571d0d4b60f1f`  
		Last Modified: Wed, 01 May 2024 21:52:45 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96bda8c59435efec7af66f8691bd57e40ea998e22466a425af541540373b5318`  
		Last Modified: Wed, 01 May 2024 21:52:46 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:e68563ef4e2a5f93a1630b6c22d74b79d3308904310a960fd05236b67ccb1f51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2788865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:230ae31659ae3ccfed8bcdff75e994a480170805d1fac7b67c827c46df8dd3db`

```dockerfile
```

-	Layers:
	-	`sha256:9dbcaacc5cb243d0ad977294d450f14bb16bebc8fbc839512dff8c0455a88110`  
		Last Modified: Wed, 01 May 2024 21:52:44 GMT  
		Size: 2.8 MB (2755207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0190dac23a81f514f5cc9f82d9e5a4c3e251ca54c6488d6d6772faaa158552fd`  
		Last Modified: Wed, 01 May 2024 21:52:44 GMT  
		Size: 33.7 KB (33658 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:699bc7cf026d3cccc062d6eca5bb3885afd049805c1404bd22a1d0b848e32de5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 MB (158094435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:376f599e99efeccbea38563b17aabf1e993c84f2d34dd48295677f9c96c1ed64`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
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
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40563ea69cbff5c1a45dc75899f1920a44d187519177c04caa3e0f5f138a8c8a`  
		Last Modified: Wed, 01 May 2024 22:29:50 GMT  
		Size: 9.4 MB (9388782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28c661e904ab15890c4a25b4217fab8234fc61bf4e1c058df70093905fbec24`  
		Last Modified: Wed, 01 May 2024 22:29:50 GMT  
		Size: 5.5 MB (5463797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe9a655a4caf7037c6216f987e7ea1c8fcbe01415474fce2e85ae098fcbafdf`  
		Last Modified: Wed, 01 May 2024 22:29:49 GMT  
		Size: 3.2 KB (3238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf7d30f7eda7ceb44953d13f39d62db35a2ca13a0ba19e88682ca879010fe27`  
		Last Modified: Wed, 01 May 2024 22:29:50 GMT  
		Size: 936.1 KB (936106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a6c1ba5bd8bdd375ee2ddc8bd62fa973e7ad9ed6e3449be80e7efa989f374e`  
		Last Modified: Wed, 01 May 2024 22:29:53 GMT  
		Size: 91.5 MB (91453330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fb235dfc2b03bcc24acbdc416c33dec3257d88ae34cc37dbd77d82339c6482`  
		Last Modified: Wed, 01 May 2024 22:29:52 GMT  
		Size: 21.7 MB (21662518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7b1954b4b11866cd6f33aac1578f4f63da2b9a87dbf7aa3a750444fa5fb191`  
		Last Modified: Wed, 01 May 2024 22:29:51 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80783551125bd030a5b4801fe8a543f9992dfd78cc8167287f8ae7f0bdace9ed`  
		Last Modified: Wed, 01 May 2024 22:29:51 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2745e5c37bcf74a3f4367693b5b8614ee22f8acdba508ac87dd077ee2f643b4e`  
		Last Modified: Wed, 01 May 2024 22:29:52 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:763bbeb6a5448752089fa864751e6a65218cfe71820b613c0ef24d493615248f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2788036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2d633e6c24b200747f5250a8fe360118217b18a2a11e2682f806b2eb3146afc`

```dockerfile
```

-	Layers:
	-	`sha256:ddce326635feac46d03bcc4edf86da3df7acd27e90b4d375d9a3d3b1381a1bb5`  
		Last Modified: Wed, 01 May 2024 22:29:50 GMT  
		Size: 2.8 MB (2754542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ee75260e7b456b1e3b48a502858dda3e0be6db7bb9bf26b87c6dff2b2e4bdb3`  
		Last Modified: Wed, 01 May 2024 22:29:49 GMT  
		Size: 33.5 KB (33494 bytes)  
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
$ docker pull influxdb@sha256:0b41fd998977efbe7df986e03c0932e64f74ed347ea68356289ee32ee31d4499
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7.6` - linux; amd64

```console
$ docker pull influxdb@sha256:b18296633f4c6368ed9ef0687defa1a414c94df613779d0444ee0d49b2ebcf90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (163963626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2347a667f34c96dd2bb711053800ded152012feae7a05a6fc33bad80aa435f21`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
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
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f73b2c3fb487d40499c1ddcbd6b518e4d8f9d17588acd9ad4c02cd58251477`  
		Last Modified: Wed, 01 May 2024 21:52:44 GMT  
		Size: 9.6 MB (9592087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b7ed840e23249ffb1cb2794c456e2b7a1d626900ae2f1e63aa23cd7b1907d0`  
		Last Modified: Wed, 01 May 2024 21:52:44 GMT  
		Size: 5.8 MB (5820924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e75552013d14f57e219b93a76ed4df639bb842330ae49e704cb554119cf4a6f`  
		Last Modified: Wed, 01 May 2024 21:52:44 GMT  
		Size: 3.2 KB (3232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b464a6ebd22a5d1c9f1e1c3a52c594b5863b462211628441a2ccc76626164e69`  
		Last Modified: Wed, 01 May 2024 21:52:44 GMT  
		Size: 1.0 MB (1006371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b71d89d0ea33d46a7a892759f2c23eeabe413caf3e84135af58c33c4757a50`  
		Last Modified: Wed, 01 May 2024 21:52:46 GMT  
		Size: 95.3 MB (95255493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f644c99e19f312326f23a72bd1aaafef67938bf354c711d5153dd6cbc461bd85`  
		Last Modified: Wed, 01 May 2024 21:52:45 GMT  
		Size: 23.1 MB (23128314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fedcea28a4aac63ae903531bd9797dbca1615a7c6b12a6c79fbf0a7306c0fb1`  
		Last Modified: Wed, 01 May 2024 21:52:45 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7ec675151b106c895ee0f29dd1d7438c4f86d0bfb8cf7940b571d0d4b60f1f`  
		Last Modified: Wed, 01 May 2024 21:52:45 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96bda8c59435efec7af66f8691bd57e40ea998e22466a425af541540373b5318`  
		Last Modified: Wed, 01 May 2024 21:52:46 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.6` - unknown; unknown

```console
$ docker pull influxdb@sha256:e68563ef4e2a5f93a1630b6c22d74b79d3308904310a960fd05236b67ccb1f51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2788865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:230ae31659ae3ccfed8bcdff75e994a480170805d1fac7b67c827c46df8dd3db`

```dockerfile
```

-	Layers:
	-	`sha256:9dbcaacc5cb243d0ad977294d450f14bb16bebc8fbc839512dff8c0455a88110`  
		Last Modified: Wed, 01 May 2024 21:52:44 GMT  
		Size: 2.8 MB (2755207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0190dac23a81f514f5cc9f82d9e5a4c3e251ca54c6488d6d6772faaa158552fd`  
		Last Modified: Wed, 01 May 2024 21:52:44 GMT  
		Size: 33.7 KB (33658 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7.6` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:699bc7cf026d3cccc062d6eca5bb3885afd049805c1404bd22a1d0b848e32de5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 MB (158094435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:376f599e99efeccbea38563b17aabf1e993c84f2d34dd48295677f9c96c1ed64`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
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
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40563ea69cbff5c1a45dc75899f1920a44d187519177c04caa3e0f5f138a8c8a`  
		Last Modified: Wed, 01 May 2024 22:29:50 GMT  
		Size: 9.4 MB (9388782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28c661e904ab15890c4a25b4217fab8234fc61bf4e1c058df70093905fbec24`  
		Last Modified: Wed, 01 May 2024 22:29:50 GMT  
		Size: 5.5 MB (5463797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe9a655a4caf7037c6216f987e7ea1c8fcbe01415474fce2e85ae098fcbafdf`  
		Last Modified: Wed, 01 May 2024 22:29:49 GMT  
		Size: 3.2 KB (3238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf7d30f7eda7ceb44953d13f39d62db35a2ca13a0ba19e88682ca879010fe27`  
		Last Modified: Wed, 01 May 2024 22:29:50 GMT  
		Size: 936.1 KB (936106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a6c1ba5bd8bdd375ee2ddc8bd62fa973e7ad9ed6e3449be80e7efa989f374e`  
		Last Modified: Wed, 01 May 2024 22:29:53 GMT  
		Size: 91.5 MB (91453330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fb235dfc2b03bcc24acbdc416c33dec3257d88ae34cc37dbd77d82339c6482`  
		Last Modified: Wed, 01 May 2024 22:29:52 GMT  
		Size: 21.7 MB (21662518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7b1954b4b11866cd6f33aac1578f4f63da2b9a87dbf7aa3a750444fa5fb191`  
		Last Modified: Wed, 01 May 2024 22:29:51 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80783551125bd030a5b4801fe8a543f9992dfd78cc8167287f8ae7f0bdace9ed`  
		Last Modified: Wed, 01 May 2024 22:29:51 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2745e5c37bcf74a3f4367693b5b8614ee22f8acdba508ac87dd077ee2f643b4e`  
		Last Modified: Wed, 01 May 2024 22:29:52 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.6` - unknown; unknown

```console
$ docker pull influxdb@sha256:763bbeb6a5448752089fa864751e6a65218cfe71820b613c0ef24d493615248f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2788036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2d633e6c24b200747f5250a8fe360118217b18a2a11e2682f806b2eb3146afc`

```dockerfile
```

-	Layers:
	-	`sha256:ddce326635feac46d03bcc4edf86da3df7acd27e90b4d375d9a3d3b1381a1bb5`  
		Last Modified: Wed, 01 May 2024 22:29:50 GMT  
		Size: 2.8 MB (2754542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ee75260e7b456b1e3b48a502858dda3e0be6db7bb9bf26b87c6dff2b2e4bdb3`  
		Last Modified: Wed, 01 May 2024 22:29:49 GMT  
		Size: 33.5 KB (33494 bytes)  
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
$ docker pull influxdb@sha256:0b41fd998977efbe7df986e03c0932e64f74ed347ea68356289ee32ee31d4499
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:b18296633f4c6368ed9ef0687defa1a414c94df613779d0444ee0d49b2ebcf90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (163963626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2347a667f34c96dd2bb711053800ded152012feae7a05a6fc33bad80aa435f21`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
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
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f73b2c3fb487d40499c1ddcbd6b518e4d8f9d17588acd9ad4c02cd58251477`  
		Last Modified: Wed, 01 May 2024 21:52:44 GMT  
		Size: 9.6 MB (9592087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b7ed840e23249ffb1cb2794c456e2b7a1d626900ae2f1e63aa23cd7b1907d0`  
		Last Modified: Wed, 01 May 2024 21:52:44 GMT  
		Size: 5.8 MB (5820924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e75552013d14f57e219b93a76ed4df639bb842330ae49e704cb554119cf4a6f`  
		Last Modified: Wed, 01 May 2024 21:52:44 GMT  
		Size: 3.2 KB (3232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b464a6ebd22a5d1c9f1e1c3a52c594b5863b462211628441a2ccc76626164e69`  
		Last Modified: Wed, 01 May 2024 21:52:44 GMT  
		Size: 1.0 MB (1006371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b71d89d0ea33d46a7a892759f2c23eeabe413caf3e84135af58c33c4757a50`  
		Last Modified: Wed, 01 May 2024 21:52:46 GMT  
		Size: 95.3 MB (95255493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f644c99e19f312326f23a72bd1aaafef67938bf354c711d5153dd6cbc461bd85`  
		Last Modified: Wed, 01 May 2024 21:52:45 GMT  
		Size: 23.1 MB (23128314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fedcea28a4aac63ae903531bd9797dbca1615a7c6b12a6c79fbf0a7306c0fb1`  
		Last Modified: Wed, 01 May 2024 21:52:45 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7ec675151b106c895ee0f29dd1d7438c4f86d0bfb8cf7940b571d0d4b60f1f`  
		Last Modified: Wed, 01 May 2024 21:52:45 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96bda8c59435efec7af66f8691bd57e40ea998e22466a425af541540373b5318`  
		Last Modified: Wed, 01 May 2024 21:52:46 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:e68563ef4e2a5f93a1630b6c22d74b79d3308904310a960fd05236b67ccb1f51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2788865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:230ae31659ae3ccfed8bcdff75e994a480170805d1fac7b67c827c46df8dd3db`

```dockerfile
```

-	Layers:
	-	`sha256:9dbcaacc5cb243d0ad977294d450f14bb16bebc8fbc839512dff8c0455a88110`  
		Last Modified: Wed, 01 May 2024 21:52:44 GMT  
		Size: 2.8 MB (2755207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0190dac23a81f514f5cc9f82d9e5a4c3e251ca54c6488d6d6772faaa158552fd`  
		Last Modified: Wed, 01 May 2024 21:52:44 GMT  
		Size: 33.7 KB (33658 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:699bc7cf026d3cccc062d6eca5bb3885afd049805c1404bd22a1d0b848e32de5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 MB (158094435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:376f599e99efeccbea38563b17aabf1e993c84f2d34dd48295677f9c96c1ed64`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
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
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40563ea69cbff5c1a45dc75899f1920a44d187519177c04caa3e0f5f138a8c8a`  
		Last Modified: Wed, 01 May 2024 22:29:50 GMT  
		Size: 9.4 MB (9388782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28c661e904ab15890c4a25b4217fab8234fc61bf4e1c058df70093905fbec24`  
		Last Modified: Wed, 01 May 2024 22:29:50 GMT  
		Size: 5.5 MB (5463797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe9a655a4caf7037c6216f987e7ea1c8fcbe01415474fce2e85ae098fcbafdf`  
		Last Modified: Wed, 01 May 2024 22:29:49 GMT  
		Size: 3.2 KB (3238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf7d30f7eda7ceb44953d13f39d62db35a2ca13a0ba19e88682ca879010fe27`  
		Last Modified: Wed, 01 May 2024 22:29:50 GMT  
		Size: 936.1 KB (936106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a6c1ba5bd8bdd375ee2ddc8bd62fa973e7ad9ed6e3449be80e7efa989f374e`  
		Last Modified: Wed, 01 May 2024 22:29:53 GMT  
		Size: 91.5 MB (91453330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fb235dfc2b03bcc24acbdc416c33dec3257d88ae34cc37dbd77d82339c6482`  
		Last Modified: Wed, 01 May 2024 22:29:52 GMT  
		Size: 21.7 MB (21662518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7b1954b4b11866cd6f33aac1578f4f63da2b9a87dbf7aa3a750444fa5fb191`  
		Last Modified: Wed, 01 May 2024 22:29:51 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80783551125bd030a5b4801fe8a543f9992dfd78cc8167287f8ae7f0bdace9ed`  
		Last Modified: Wed, 01 May 2024 22:29:51 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2745e5c37bcf74a3f4367693b5b8614ee22f8acdba508ac87dd077ee2f643b4e`  
		Last Modified: Wed, 01 May 2024 22:29:52 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:763bbeb6a5448752089fa864751e6a65218cfe71820b613c0ef24d493615248f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2788036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2d633e6c24b200747f5250a8fe360118217b18a2a11e2682f806b2eb3146afc`

```dockerfile
```

-	Layers:
	-	`sha256:ddce326635feac46d03bcc4edf86da3df7acd27e90b4d375d9a3d3b1381a1bb5`  
		Last Modified: Wed, 01 May 2024 22:29:50 GMT  
		Size: 2.8 MB (2754542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ee75260e7b456b1e3b48a502858dda3e0be6db7bb9bf26b87c6dff2b2e4bdb3`  
		Last Modified: Wed, 01 May 2024 22:29:49 GMT  
		Size: 33.5 KB (33494 bytes)  
		MIME: application/vnd.in-toto+json
