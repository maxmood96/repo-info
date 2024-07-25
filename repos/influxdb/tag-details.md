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
-	[`influxdb:2.7.8`](#influxdb278)
-	[`influxdb:2.7.8-alpine`](#influxdb278-alpine)
-	[`influxdb:alpine`](#influxdbalpine)
-	[`influxdb:latest`](#influxdblatest)

## `influxdb:1.10-data`

```console
$ docker pull influxdb@sha256:4df7180c4b2067a3868df9715e8357d688788c129cd5b0b3a6b8e26ed330e221
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-data` - linux; amd64

```console
$ docker pull influxdb@sha256:6cc78fc50a7c36fb09cff78269a2dfa89d255faeb62c337a5a973a88c4e09764
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112230142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caaba4ed3664b9b53db823e43c8d443dd0b6cc7ed8538aea97065eb441c845d9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 11 Jul 2024 20:47:57 GMT
ADD file:61c91b2a02e0d3deb2364da03241d137acf78345623ae188082e574b043032a0 in / 
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["bash"]
# Thu, 11 Jul 2024 20:47:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jul 2024 20:47:57 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Thu, 11 Jul 2024 20:47:57 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Jul 2024 20:47:57 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jul 2024 20:47:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:73226dab8db5240a2ddbdbe2fb1f0949a911563a62a3d5de3c8669ae708e88de`  
		Last Modified: Tue, 23 Jul 2024 05:28:11 GMT  
		Size: 55.1 MB (55084578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d53dfa00a586795de9dc9f5bc8ad4717b02a8c349b4bbc1f4600a926c5384f40`  
		Last Modified: Tue, 23 Jul 2024 06:14:18 GMT  
		Size: 15.8 MB (15764285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568d3cbe5c5d67e5ca6b7a58ddadc5dbe66624cb6ef432238913d77d9722267f`  
		Last Modified: Tue, 23 Jul 2024 07:14:29 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f8d9ef376bc5922df972822da6a8f58e85149ba3be302db810796d9820817d`  
		Last Modified: Tue, 23 Jul 2024 07:14:30 GMT  
		Size: 41.4 MB (41377731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b112ececdc29d493ec8ad2fc37b4343c093f441dec4cde9a26471efe62c81cd`  
		Last Modified: Tue, 23 Jul 2024 07:14:29 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3763838879248f0574219f90db4013a195073506ff2a01ceb8886953a5d5740`  
		Last Modified: Tue, 23 Jul 2024 07:14:30 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e5d898090ecd8c6861dd45fc583378257d6620a83c26ee8a7be745d2a2eb26`  
		Last Modified: Tue, 23 Jul 2024 07:14:28 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:5df66922e026484a98ce71444c5521f66e696e4097d6e1ced5f2f37ad3b637e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4642341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f443e9ebc6814520de45247abebc32f422138185afe0a3c03b2b845702c258b0`

```dockerfile
```

-	Layers:
	-	`sha256:224cd090304b1269d36632f9ef3140c6d9388be90f44e509893a5a934470272b`  
		Last Modified: Tue, 23 Jul 2024 07:14:30 GMT  
		Size: 4.6 MB (4627767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e7ea0ead5cbed08a3051383bbbc726542811b9e15f128be3dfabc913882458d`  
		Last Modified: Tue, 23 Jul 2024 07:14:29 GMT  
		Size: 14.6 KB (14574 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10-data-alpine`

```console
$ docker pull influxdb@sha256:cb91e2276f0a7467ba9849051d4783601d611e4fdf7858cc7a3e4c02bb2166b3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:fb446975bf2c90a566a5adda86334e13e637a26f5d54d7946eb95dce121a930d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46176803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1e941d43836dd1b85a7b0ac1de576fae7abf06d754280e302448ea867577a8c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 11 Jul 2024 20:47:57 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["/bin/sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Thu, 11 Jul 2024 20:47:57 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Jul 2024 20:47:57 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jul 2024 20:47:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0dc81762ab9cd4ef11ab0791cc1e4b892353c5ad16f3506e394ed6f4851e93`  
		Last Modified: Mon, 22 Jul 2024 23:05:36 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ee443a8375d9e90a3385f0333e994b58091f77ba5e52be7d06610b75219aab`  
		Last Modified: Mon, 22 Jul 2024 23:05:35 GMT  
		Size: 1.2 MB (1229932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c33d0acaa33885e986f7a509e6b296da210997e8e589b253b46eb4f4587ab78`  
		Last Modified: Mon, 22 Jul 2024 23:05:38 GMT  
		Size: 41.3 MB (41321925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4352fdc168f35acf4ecca2a01c1e45cf16752f5105b8e534f978967ddb9c022c`  
		Last Modified: Mon, 22 Jul 2024 23:05:37 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51126ebe33f23fd99fb08415f2a3e22a7c495a726b25262e4871e5a452e7b9a4`  
		Last Modified: Mon, 22 Jul 2024 23:05:37 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f966e9f0c105c5886529372b3bdb87900b7e00cb65fafeb7cb3b51a77af27c`  
		Last Modified: Mon, 22 Jul 2024 23:05:37 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:b28d31a5b38885c1966c8b8ada6c2d614ff9103f868f5669443668a0cb3be400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **769.8 KB (769824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee9f9ee2afa9eefe7f08bce14d2d5c4d5e3ea41c470f657d2f606cafb0e28042`

```dockerfile
```

-	Layers:
	-	`sha256:2a23df4497c12a904d0a3dc6701174ab198bf8b9ec08fc5f3f6249c6998d850c`  
		Last Modified: Mon, 22 Jul 2024 23:05:37 GMT  
		Size: 753.4 KB (753400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43473ac8a236cf49956f4cfa1968dec1d3264dc2b559aa337abde4359f18025a`  
		Last Modified: Mon, 22 Jul 2024 23:05:37 GMT  
		Size: 16.4 KB (16424 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10-meta`

```console
$ docker pull influxdb@sha256:5d0a56b8b0d356f843a9a2abfe9889e2de20f67b27b3aa60c01f0fb7f03ee4ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:3b8ff046f309b67d82707aaa772bb9bfe9eee1ec2e12b04c452562485042b685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.9 MB (90946774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea1c7822070a23d1e205b38d0c10882af153ce5b263f37116505a9e601793b89`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 11 Jul 2024 20:47:57 GMT
ADD file:61c91b2a02e0d3deb2364da03241d137acf78345623ae188082e574b043032a0 in / 
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["bash"]
# Thu, 11 Jul 2024 20:47:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jul 2024 20:47:57 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Thu, 11 Jul 2024 20:47:57 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
EXPOSE map[8091/tcp:{}]
# Thu, 11 Jul 2024 20:47:57 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jul 2024 20:47:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:73226dab8db5240a2ddbdbe2fb1f0949a911563a62a3d5de3c8669ae708e88de`  
		Last Modified: Tue, 23 Jul 2024 05:28:11 GMT  
		Size: 55.1 MB (55084578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d53dfa00a586795de9dc9f5bc8ad4717b02a8c349b4bbc1f4600a926c5384f40`  
		Last Modified: Tue, 23 Jul 2024 06:14:18 GMT  
		Size: 15.8 MB (15764285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0289b8309ae6eeca30b64f9c838d0a5efad8b33a88b141ad0f7aee4cde80258`  
		Last Modified: Tue, 23 Jul 2024 07:14:32 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037f701fd96b23c070574f407e3196af829c984ed68cbefee1aebc760e35ba6f`  
		Last Modified: Tue, 23 Jul 2024 07:14:32 GMT  
		Size: 20.1 MB (20095559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b3e3821c911476e04da1dad36357674847ca5c664f341f6d4e7efd9487b760`  
		Last Modified: Tue, 23 Jul 2024 07:14:32 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c9005ec9c308cd7e306cbf9df239ec0e03eaee7ef47cf48a0bf03202498e70`  
		Last Modified: Tue, 23 Jul 2024 07:14:32 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:1ac089e08891116aaaea037371849b954e27c7ffa4ff2ede96da7b89bbf5a0c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4565275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2f44fbe1b20667b7cf0258b319c4eb949a573ea501f3b2debd63b9b5d6ac54f`

```dockerfile
```

-	Layers:
	-	`sha256:b3c2f207cfa96276acc94bb7a4e356996d8f1848e19a22c43e03228a0a500b97`  
		Last Modified: Tue, 23 Jul 2024 07:14:32 GMT  
		Size: 4.6 MB (4552354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45d1896277eb5647c7d4119fa66b0618b8bc105eab7a7a0d2722a215b4320928`  
		Last Modified: Tue, 23 Jul 2024 07:14:32 GMT  
		Size: 12.9 KB (12921 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10-meta-alpine`

```console
$ docker pull influxdb@sha256:7099e3052f235d0a6dc91df58162516d0d4fb891bf2d4312660d6dc1d88696e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:e520a62776999a591feedbeea6afe0c025b5abf7830388bd2be456ff9963adf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.9 MB (24895714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2df11e6a8df056f02b940ca435f8c7ad2e4c2b0b953b4eb71924bd6fff48f7b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 11 Jul 2024 20:47:57 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["/bin/sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Thu, 11 Jul 2024 20:47:57 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
EXPOSE map[8091/tcp:{}]
# Thu, 11 Jul 2024 20:47:57 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jul 2024 20:47:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e46fef88be38a0a55b04198e631d7d77cb36f3716a89f6c53c04a47869d5ece`  
		Last Modified: Mon, 22 Jul 2024 23:05:40 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f52f5d29faa280b52577ca19302d591ce707d89f618bb212a2af88debfba52a9`  
		Last Modified: Mon, 22 Jul 2024 23:05:41 GMT  
		Size: 1.2 MB (1229919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cfc56a1746adf8954c3b3ced8afe1c25b8f033c12e92e641cc4ff009e0267d1`  
		Last Modified: Mon, 22 Jul 2024 23:05:41 GMT  
		Size: 20.0 MB (20042058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6b3903049ae7bbf7e6a6efe77ae26dbfe2a6dec0fe4292e51331522cf2d2a0`  
		Last Modified: Mon, 22 Jul 2024 23:05:40 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e2b1864fbf874b3dfdc254d796cd18aac337848fca46269989d30c32cc327e`  
		Last Modified: Mon, 22 Jul 2024 23:05:41 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:17f46b672cb02504849f8c0c3b1667cfaabb08e9a2601200876e0fc61182d6a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **693.0 KB (693038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:052b218a81655939e44802897e5872ef6a55c43a09ec4579a3ca7cebf6b5a318`

```dockerfile
```

-	Layers:
	-	`sha256:92260b24e1cf1a715755b7431f234f41fef9c080b7fe81c0f8bc84e8496ea37e`  
		Last Modified: Mon, 22 Jul 2024 23:05:41 GMT  
		Size: 678.2 KB (678249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e62e146b35e00a410bb7a7388531a0f27693cd2d3ec5c9c87ebd171e87914fff`  
		Last Modified: Mon, 22 Jul 2024 23:05:40 GMT  
		Size: 14.8 KB (14789 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10.7-data`

```console
$ docker pull influxdb@sha256:4df7180c4b2067a3868df9715e8357d688788c129cd5b0b3a6b8e26ed330e221
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.7-data` - linux; amd64

```console
$ docker pull influxdb@sha256:6cc78fc50a7c36fb09cff78269a2dfa89d255faeb62c337a5a973a88c4e09764
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112230142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caaba4ed3664b9b53db823e43c8d443dd0b6cc7ed8538aea97065eb441c845d9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 11 Jul 2024 20:47:57 GMT
ADD file:61c91b2a02e0d3deb2364da03241d137acf78345623ae188082e574b043032a0 in / 
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["bash"]
# Thu, 11 Jul 2024 20:47:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jul 2024 20:47:57 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Thu, 11 Jul 2024 20:47:57 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Jul 2024 20:47:57 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jul 2024 20:47:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:73226dab8db5240a2ddbdbe2fb1f0949a911563a62a3d5de3c8669ae708e88de`  
		Last Modified: Tue, 23 Jul 2024 05:28:11 GMT  
		Size: 55.1 MB (55084578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d53dfa00a586795de9dc9f5bc8ad4717b02a8c349b4bbc1f4600a926c5384f40`  
		Last Modified: Tue, 23 Jul 2024 06:14:18 GMT  
		Size: 15.8 MB (15764285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568d3cbe5c5d67e5ca6b7a58ddadc5dbe66624cb6ef432238913d77d9722267f`  
		Last Modified: Tue, 23 Jul 2024 07:14:29 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f8d9ef376bc5922df972822da6a8f58e85149ba3be302db810796d9820817d`  
		Last Modified: Tue, 23 Jul 2024 07:14:30 GMT  
		Size: 41.4 MB (41377731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b112ececdc29d493ec8ad2fc37b4343c093f441dec4cde9a26471efe62c81cd`  
		Last Modified: Tue, 23 Jul 2024 07:14:29 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3763838879248f0574219f90db4013a195073506ff2a01ceb8886953a5d5740`  
		Last Modified: Tue, 23 Jul 2024 07:14:30 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e5d898090ecd8c6861dd45fc583378257d6620a83c26ee8a7be745d2a2eb26`  
		Last Modified: Tue, 23 Jul 2024 07:14:28 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.7-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:5df66922e026484a98ce71444c5521f66e696e4097d6e1ced5f2f37ad3b637e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4642341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f443e9ebc6814520de45247abebc32f422138185afe0a3c03b2b845702c258b0`

```dockerfile
```

-	Layers:
	-	`sha256:224cd090304b1269d36632f9ef3140c6d9388be90f44e509893a5a934470272b`  
		Last Modified: Tue, 23 Jul 2024 07:14:30 GMT  
		Size: 4.6 MB (4627767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e7ea0ead5cbed08a3051383bbbc726542811b9e15f128be3dfabc913882458d`  
		Last Modified: Tue, 23 Jul 2024 07:14:29 GMT  
		Size: 14.6 KB (14574 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10.7-data-alpine`

```console
$ docker pull influxdb@sha256:cb91e2276f0a7467ba9849051d4783601d611e4fdf7858cc7a3e4c02bb2166b3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.7-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:fb446975bf2c90a566a5adda86334e13e637a26f5d54d7946eb95dce121a930d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46176803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1e941d43836dd1b85a7b0ac1de576fae7abf06d754280e302448ea867577a8c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 11 Jul 2024 20:47:57 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["/bin/sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Thu, 11 Jul 2024 20:47:57 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Jul 2024 20:47:57 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jul 2024 20:47:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0dc81762ab9cd4ef11ab0791cc1e4b892353c5ad16f3506e394ed6f4851e93`  
		Last Modified: Mon, 22 Jul 2024 23:05:36 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ee443a8375d9e90a3385f0333e994b58091f77ba5e52be7d06610b75219aab`  
		Last Modified: Mon, 22 Jul 2024 23:05:35 GMT  
		Size: 1.2 MB (1229932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c33d0acaa33885e986f7a509e6b296da210997e8e589b253b46eb4f4587ab78`  
		Last Modified: Mon, 22 Jul 2024 23:05:38 GMT  
		Size: 41.3 MB (41321925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4352fdc168f35acf4ecca2a01c1e45cf16752f5105b8e534f978967ddb9c022c`  
		Last Modified: Mon, 22 Jul 2024 23:05:37 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51126ebe33f23fd99fb08415f2a3e22a7c495a726b25262e4871e5a452e7b9a4`  
		Last Modified: Mon, 22 Jul 2024 23:05:37 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f966e9f0c105c5886529372b3bdb87900b7e00cb65fafeb7cb3b51a77af27c`  
		Last Modified: Mon, 22 Jul 2024 23:05:37 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.7-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:b28d31a5b38885c1966c8b8ada6c2d614ff9103f868f5669443668a0cb3be400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **769.8 KB (769824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee9f9ee2afa9eefe7f08bce14d2d5c4d5e3ea41c470f657d2f606cafb0e28042`

```dockerfile
```

-	Layers:
	-	`sha256:2a23df4497c12a904d0a3dc6701174ab198bf8b9ec08fc5f3f6249c6998d850c`  
		Last Modified: Mon, 22 Jul 2024 23:05:37 GMT  
		Size: 753.4 KB (753400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43473ac8a236cf49956f4cfa1968dec1d3264dc2b559aa337abde4359f18025a`  
		Last Modified: Mon, 22 Jul 2024 23:05:37 GMT  
		Size: 16.4 KB (16424 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10.7-meta`

```console
$ docker pull influxdb@sha256:5d0a56b8b0d356f843a9a2abfe9889e2de20f67b27b3aa60c01f0fb7f03ee4ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.7-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:3b8ff046f309b67d82707aaa772bb9bfe9eee1ec2e12b04c452562485042b685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.9 MB (90946774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea1c7822070a23d1e205b38d0c10882af153ce5b263f37116505a9e601793b89`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 11 Jul 2024 20:47:57 GMT
ADD file:61c91b2a02e0d3deb2364da03241d137acf78345623ae188082e574b043032a0 in / 
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["bash"]
# Thu, 11 Jul 2024 20:47:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jul 2024 20:47:57 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Thu, 11 Jul 2024 20:47:57 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
EXPOSE map[8091/tcp:{}]
# Thu, 11 Jul 2024 20:47:57 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jul 2024 20:47:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:73226dab8db5240a2ddbdbe2fb1f0949a911563a62a3d5de3c8669ae708e88de`  
		Last Modified: Tue, 23 Jul 2024 05:28:11 GMT  
		Size: 55.1 MB (55084578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d53dfa00a586795de9dc9f5bc8ad4717b02a8c349b4bbc1f4600a926c5384f40`  
		Last Modified: Tue, 23 Jul 2024 06:14:18 GMT  
		Size: 15.8 MB (15764285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0289b8309ae6eeca30b64f9c838d0a5efad8b33a88b141ad0f7aee4cde80258`  
		Last Modified: Tue, 23 Jul 2024 07:14:32 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037f701fd96b23c070574f407e3196af829c984ed68cbefee1aebc760e35ba6f`  
		Last Modified: Tue, 23 Jul 2024 07:14:32 GMT  
		Size: 20.1 MB (20095559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b3e3821c911476e04da1dad36357674847ca5c664f341f6d4e7efd9487b760`  
		Last Modified: Tue, 23 Jul 2024 07:14:32 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c9005ec9c308cd7e306cbf9df239ec0e03eaee7ef47cf48a0bf03202498e70`  
		Last Modified: Tue, 23 Jul 2024 07:14:32 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.7-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:1ac089e08891116aaaea037371849b954e27c7ffa4ff2ede96da7b89bbf5a0c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4565275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2f44fbe1b20667b7cf0258b319c4eb949a573ea501f3b2debd63b9b5d6ac54f`

```dockerfile
```

-	Layers:
	-	`sha256:b3c2f207cfa96276acc94bb7a4e356996d8f1848e19a22c43e03228a0a500b97`  
		Last Modified: Tue, 23 Jul 2024 07:14:32 GMT  
		Size: 4.6 MB (4552354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45d1896277eb5647c7d4119fa66b0618b8bc105eab7a7a0d2722a215b4320928`  
		Last Modified: Tue, 23 Jul 2024 07:14:32 GMT  
		Size: 12.9 KB (12921 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10.7-meta-alpine`

```console
$ docker pull influxdb@sha256:7099e3052f235d0a6dc91df58162516d0d4fb891bf2d4312660d6dc1d88696e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.7-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:e520a62776999a591feedbeea6afe0c025b5abf7830388bd2be456ff9963adf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.9 MB (24895714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2df11e6a8df056f02b940ca435f8c7ad2e4c2b0b953b4eb71924bd6fff48f7b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 11 Jul 2024 20:47:57 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["/bin/sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Thu, 11 Jul 2024 20:47:57 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
EXPOSE map[8091/tcp:{}]
# Thu, 11 Jul 2024 20:47:57 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jul 2024 20:47:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e46fef88be38a0a55b04198e631d7d77cb36f3716a89f6c53c04a47869d5ece`  
		Last Modified: Mon, 22 Jul 2024 23:05:40 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f52f5d29faa280b52577ca19302d591ce707d89f618bb212a2af88debfba52a9`  
		Last Modified: Mon, 22 Jul 2024 23:05:41 GMT  
		Size: 1.2 MB (1229919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cfc56a1746adf8954c3b3ced8afe1c25b8f033c12e92e641cc4ff009e0267d1`  
		Last Modified: Mon, 22 Jul 2024 23:05:41 GMT  
		Size: 20.0 MB (20042058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6b3903049ae7bbf7e6a6efe77ae26dbfe2a6dec0fe4292e51331522cf2d2a0`  
		Last Modified: Mon, 22 Jul 2024 23:05:40 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e2b1864fbf874b3dfdc254d796cd18aac337848fca46269989d30c32cc327e`  
		Last Modified: Mon, 22 Jul 2024 23:05:41 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.7-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:17f46b672cb02504849f8c0c3b1667cfaabb08e9a2601200876e0fc61182d6a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **693.0 KB (693038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:052b218a81655939e44802897e5872ef6a55c43a09ec4579a3ca7cebf6b5a318`

```dockerfile
```

-	Layers:
	-	`sha256:92260b24e1cf1a715755b7431f234f41fef9c080b7fe81c0f8bc84e8496ea37e`  
		Last Modified: Mon, 22 Jul 2024 23:05:41 GMT  
		Size: 678.2 KB (678249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e62e146b35e00a410bb7a7388531a0f27693cd2d3ec5c9c87ebd171e87914fff`  
		Last Modified: Mon, 22 Jul 2024 23:05:40 GMT  
		Size: 14.8 KB (14789 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-data`

```console
$ docker pull influxdb@sha256:b92ce2e3b6f15f7b29d66a240e698ffc3daacc799e68c5c912289dd1f81cdd5a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data` - linux; amd64

```console
$ docker pull influxdb@sha256:09a1647253e6b597e1f7eec484fb62fade3ccdd1440fb91911ce4e14ede4f95f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 MB (115431092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99f1f05a346546cb2752339c240b601c970957263aa5058ae816a441dface746`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 11 Jul 2024 20:47:57 GMT
ADD file:430cca9ad155514d8c818e860e66e2aeccfb6230874d4faf446a1d0c2fc1054f in / 
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["bash"]
# Thu, 11 Jul 2024 20:47:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jul 2024 20:47:57 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXDB_VERSION=1.11.5-c1.11.5
# Thu, 11 Jul 2024 20:47:57 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Jul 2024 20:47:57 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jul 2024 20:47:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:ca4e5d6727252f0dbc207fbf283cb95e278bf562bda42d35ce6c919583a110a0`  
		Last Modified: Tue, 23 Jul 2024 05:27:34 GMT  
		Size: 49.6 MB (49554075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b93c12a9c9326732b35d9e3ebe57148abe33f8fa6e25ab76867410b0ccf876`  
		Last Modified: Tue, 23 Jul 2024 06:13:16 GMT  
		Size: 24.1 MB (24050796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86fe0b623a550a38868e8eb3e8251e479ae5a2e9fcbb74db4d92db77c2eb0f18`  
		Last Modified: Tue, 23 Jul 2024 07:14:33 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:484d1de9e314c570f216e399ed207af552c89257b0845da422295f520a9be2df`  
		Last Modified: Tue, 23 Jul 2024 07:14:33 GMT  
		Size: 41.8 MB (41822676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b9dba2c5fa498bc1c157a00728e3fdc69d7b3c4fd3e94059bb2b509bf936d0`  
		Last Modified: Tue, 23 Jul 2024 07:14:33 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d191bbc3b09cfc6879b99a566beabad492daf2fd087964dfd9b0c36d0c70a5`  
		Last Modified: Tue, 23 Jul 2024 07:14:33 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc53c54120010d9d8c3d8e7a5856375904f24905d43cb4b67fa59d2039b95e0`  
		Last Modified: Tue, 23 Jul 2024 07:14:34 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:8518dab9eb8f24be54cb6c48a7d54a4e235b0544f4568ef5560848d1aee3abf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4516333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c91e78a1e6aa40792a4b796fa65404c681e538da4da9cd068d7150a6e7712dfe`

```dockerfile
```

-	Layers:
	-	`sha256:bb394aaeb26e7c8f8420a722e4a304c1d10367ddfa0bbac1f1a8096cef7d9d65`  
		Last Modified: Tue, 23 Jul 2024 07:14:33 GMT  
		Size: 4.5 MB (4501759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b4383aa92308fcf9b78f3c455e70280b35e5f7cd1f2f60710c3a00e9abc37df`  
		Last Modified: Tue, 23 Jul 2024 07:14:33 GMT  
		Size: 14.6 KB (14574 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-data-alpine`

```console
$ docker pull influxdb@sha256:91c1a923a9e4faadaecee55e8290f33d57d1dec39b1996fc348e90712ad5313d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:a3a9ee6443ef3a7f4ad2c6f7cd2b0a3696afc38df20c852bb02597a524f31e91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46629434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7875d7bb3aea16b08d347098332bdd0aec478658f10bb29566a372f9aaf6494`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 11 Jul 2024 20:47:57 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["/bin/sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXDB_VERSION=1.11.5-c1.11.5
# Thu, 11 Jul 2024 20:47:57 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Jul 2024 20:47:57 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jul 2024 20:47:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c19734685fd9086e9ad843f1b99a803203af9fdccff2c76de84208583c3c3d2`  
		Last Modified: Mon, 22 Jul 2024 23:05:39 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f14e2497a545d02fdaf49273f100d16d98f4c907fed55d91225317add7e764`  
		Last Modified: Mon, 22 Jul 2024 23:05:39 GMT  
		Size: 1.2 MB (1229926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d725c34f7f87aeb14d4fee68f16bab4af46fb516ebe408ecdc622b04b08de55d`  
		Last Modified: Mon, 22 Jul 2024 23:05:40 GMT  
		Size: 41.8 MB (41774561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2abb241390f62c4fc5afb047a941dccb49079d03d340ef1687d9c14e204dd4bd`  
		Last Modified: Mon, 22 Jul 2024 23:05:39 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47a7da7cef25f802a7c8815b60b103a6dffe11055f8ec3eecea16bbb430e5be`  
		Last Modified: Mon, 22 Jul 2024 23:05:40 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2680241baf83e1c07dee46cd3cc4c0455e72935e48e58fdb268965318701655`  
		Last Modified: Mon, 22 Jul 2024 23:05:40 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:726633ec96a5e5caf3cf182d9f69dce2b8db1ac23ff2927b7c6f08c57eb359ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **769.5 KB (769511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3351eb8d18b222d8e4bb39c70e027dca0e38f8cc6cf6b62f5b0f427b7b1d627`

```dockerfile
```

-	Layers:
	-	`sha256:65b27f4d62d4cae9f25335987cde220dd5cf9adb79b36095620684d82247374f`  
		Last Modified: Mon, 22 Jul 2024 23:05:39 GMT  
		Size: 753.1 KB (753088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c973a06beaa2ea2cc5297d155ac04dd7ceb24eeb6da47fec9465d015b8a86ed`  
		Last Modified: Mon, 22 Jul 2024 23:05:39 GMT  
		Size: 16.4 KB (16423 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-meta`

```console
$ docker pull influxdb@sha256:84c943c00c83d325e23e5ca11a500bf92df84a75483c2b1cfad40b627f7de4dc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:968037645600c8d3c5ed04c459b38993e0c87d17b979292fa1f93a19552b1547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (94000250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0348271af68c472e0d64954c58552351c4d07b37b8c84f2685313bc852d34889`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 11 Jul 2024 20:47:57 GMT
ADD file:430cca9ad155514d8c818e860e66e2aeccfb6230874d4faf446a1d0c2fc1054f in / 
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["bash"]
# Thu, 11 Jul 2024 20:47:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jul 2024 20:47:57 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXDB_VERSION=1.11.5-c1.11.5
# Thu, 11 Jul 2024 20:47:57 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
EXPOSE map[8091/tcp:{}]
# Thu, 11 Jul 2024 20:47:57 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jul 2024 20:47:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:ca4e5d6727252f0dbc207fbf283cb95e278bf562bda42d35ce6c919583a110a0`  
		Last Modified: Tue, 23 Jul 2024 05:27:34 GMT  
		Size: 49.6 MB (49554075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b93c12a9c9326732b35d9e3ebe57148abe33f8fa6e25ab76867410b0ccf876`  
		Last Modified: Tue, 23 Jul 2024 06:13:16 GMT  
		Size: 24.1 MB (24050796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7712e6683588807743ecac6c4908fe81225a4385e63e8adea125a0244ad0ce1`  
		Last Modified: Tue, 23 Jul 2024 07:14:46 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7d8d5b781df318a650a88be6dca42c32a81f15a4f1265ea735fb41e1bf9175`  
		Last Modified: Tue, 23 Jul 2024 07:14:46 GMT  
		Size: 20.4 MB (20393029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6299a2061f1cd6741125ca301d837cde56da42015e33184334bb7d76819dc55e`  
		Last Modified: Tue, 23 Jul 2024 07:14:46 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9fd27ba4cc5c2032f8b464efd3e1eb3114cdcfbfe48a7c41f2b3d04bf912d4`  
		Last Modified: Tue, 23 Jul 2024 07:14:46 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:2d211af75170e8b95638f5720ff26e5325dd95207c75b14c6d48ff48da6083f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4439965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ce5a69b1cd3ea0a0b1b403849f29c9d129ed24bbaf3450778ef76fefefe1e2f`

```dockerfile
```

-	Layers:
	-	`sha256:7c7ca81871c40422eb451898c142bef2bfb593625c65c584609d04265b59dd47`  
		Last Modified: Tue, 23 Jul 2024 07:14:46 GMT  
		Size: 4.4 MB (4427044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47d186f3a8ebfeb0d1d1e25d544b56cfd186d72a09f061fd9c2699812b59f906`  
		Last Modified: Tue, 23 Jul 2024 07:14:46 GMT  
		Size: 12.9 KB (12921 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-meta-alpine`

```console
$ docker pull influxdb@sha256:78fa5b2f40d4e36d43c5b8b457268c3f84630a7d6073ad417bc422280265171d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:dd1ec4e37011d3ca42de9ae3fe533abe443e2f93eb2d384e841a3f7deea678f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25198998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00ef7fcd3567c5f8e7c837ae578aee29c0f36185159415f695baca20bc22f3bd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 11 Jul 2024 20:47:57 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["/bin/sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXDB_VERSION=1.11.5-c1.11.5
# Thu, 11 Jul 2024 20:47:57 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
EXPOSE map[8091/tcp:{}]
# Thu, 11 Jul 2024 20:47:57 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jul 2024 20:47:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec0d47512f4629295aa8fd6f1d83552091d886f770afc4a5d00963edea45256`  
		Last Modified: Mon, 22 Jul 2024 23:05:35 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ee443a8375d9e90a3385f0333e994b58091f77ba5e52be7d06610b75219aab`  
		Last Modified: Mon, 22 Jul 2024 23:05:35 GMT  
		Size: 1.2 MB (1229932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9056ab6d3880e94254e3c0b56427d1f4a961bb71b2678ee47909e1539a81463d`  
		Last Modified: Mon, 22 Jul 2024 23:05:35 GMT  
		Size: 20.3 MB (20345329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009057299ceac908d66f67eeb9200d08532e9ceeb4cb98cca77e995964899c86`  
		Last Modified: Mon, 22 Jul 2024 23:05:35 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3213ab6698643b46e73196b529f80ca009d81c7e3eb6ee4f20cee2b3768a6dde`  
		Last Modified: Mon, 22 Jul 2024 23:05:36 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:94c064b8d0a7ac9bc5daf5bc5733ef2e78b8973201abd99f8bedfc649794e7ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **694.1 KB (694055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2bf04c610dd4936298c10fe74d82cdf75e1d95ec3f4e82f804d8228761eb63`

```dockerfile
```

-	Layers:
	-	`sha256:b41b47ac78e24a9424029d231ba40ca59c1466c58ec8f7c1fb9fa1be9175d6eb`  
		Last Modified: Mon, 22 Jul 2024 23:05:35 GMT  
		Size: 679.3 KB (679266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b79971aca68a9439d84b1eb3d5dd63c3422851a359196655b2a17ad32869830d`  
		Last Modified: Mon, 22 Jul 2024 23:05:35 GMT  
		Size: 14.8 KB (14789 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.5-data`

```console
$ docker pull influxdb@sha256:b92ce2e3b6f15f7b29d66a240e698ffc3daacc799e68c5c912289dd1f81cdd5a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.5-data` - linux; amd64

```console
$ docker pull influxdb@sha256:09a1647253e6b597e1f7eec484fb62fade3ccdd1440fb91911ce4e14ede4f95f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 MB (115431092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99f1f05a346546cb2752339c240b601c970957263aa5058ae816a441dface746`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 11 Jul 2024 20:47:57 GMT
ADD file:430cca9ad155514d8c818e860e66e2aeccfb6230874d4faf446a1d0c2fc1054f in / 
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["bash"]
# Thu, 11 Jul 2024 20:47:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jul 2024 20:47:57 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXDB_VERSION=1.11.5-c1.11.5
# Thu, 11 Jul 2024 20:47:57 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Jul 2024 20:47:57 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jul 2024 20:47:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:ca4e5d6727252f0dbc207fbf283cb95e278bf562bda42d35ce6c919583a110a0`  
		Last Modified: Tue, 23 Jul 2024 05:27:34 GMT  
		Size: 49.6 MB (49554075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b93c12a9c9326732b35d9e3ebe57148abe33f8fa6e25ab76867410b0ccf876`  
		Last Modified: Tue, 23 Jul 2024 06:13:16 GMT  
		Size: 24.1 MB (24050796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86fe0b623a550a38868e8eb3e8251e479ae5a2e9fcbb74db4d92db77c2eb0f18`  
		Last Modified: Tue, 23 Jul 2024 07:14:33 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:484d1de9e314c570f216e399ed207af552c89257b0845da422295f520a9be2df`  
		Last Modified: Tue, 23 Jul 2024 07:14:33 GMT  
		Size: 41.8 MB (41822676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b9dba2c5fa498bc1c157a00728e3fdc69d7b3c4fd3e94059bb2b509bf936d0`  
		Last Modified: Tue, 23 Jul 2024 07:14:33 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d191bbc3b09cfc6879b99a566beabad492daf2fd087964dfd9b0c36d0c70a5`  
		Last Modified: Tue, 23 Jul 2024 07:14:33 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc53c54120010d9d8c3d8e7a5856375904f24905d43cb4b67fa59d2039b95e0`  
		Last Modified: Tue, 23 Jul 2024 07:14:34 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.5-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:8518dab9eb8f24be54cb6c48a7d54a4e235b0544f4568ef5560848d1aee3abf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4516333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c91e78a1e6aa40792a4b796fa65404c681e538da4da9cd068d7150a6e7712dfe`

```dockerfile
```

-	Layers:
	-	`sha256:bb394aaeb26e7c8f8420a722e4a304c1d10367ddfa0bbac1f1a8096cef7d9d65`  
		Last Modified: Tue, 23 Jul 2024 07:14:33 GMT  
		Size: 4.5 MB (4501759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b4383aa92308fcf9b78f3c455e70280b35e5f7cd1f2f60710c3a00e9abc37df`  
		Last Modified: Tue, 23 Jul 2024 07:14:33 GMT  
		Size: 14.6 KB (14574 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.5-data-alpine`

```console
$ docker pull influxdb@sha256:91c1a923a9e4faadaecee55e8290f33d57d1dec39b1996fc348e90712ad5313d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.5-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:a3a9ee6443ef3a7f4ad2c6f7cd2b0a3696afc38df20c852bb02597a524f31e91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46629434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7875d7bb3aea16b08d347098332bdd0aec478658f10bb29566a372f9aaf6494`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 11 Jul 2024 20:47:57 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["/bin/sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXDB_VERSION=1.11.5-c1.11.5
# Thu, 11 Jul 2024 20:47:57 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Jul 2024 20:47:57 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jul 2024 20:47:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c19734685fd9086e9ad843f1b99a803203af9fdccff2c76de84208583c3c3d2`  
		Last Modified: Mon, 22 Jul 2024 23:05:39 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f14e2497a545d02fdaf49273f100d16d98f4c907fed55d91225317add7e764`  
		Last Modified: Mon, 22 Jul 2024 23:05:39 GMT  
		Size: 1.2 MB (1229926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d725c34f7f87aeb14d4fee68f16bab4af46fb516ebe408ecdc622b04b08de55d`  
		Last Modified: Mon, 22 Jul 2024 23:05:40 GMT  
		Size: 41.8 MB (41774561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2abb241390f62c4fc5afb047a941dccb49079d03d340ef1687d9c14e204dd4bd`  
		Last Modified: Mon, 22 Jul 2024 23:05:39 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47a7da7cef25f802a7c8815b60b103a6dffe11055f8ec3eecea16bbb430e5be`  
		Last Modified: Mon, 22 Jul 2024 23:05:40 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2680241baf83e1c07dee46cd3cc4c0455e72935e48e58fdb268965318701655`  
		Last Modified: Mon, 22 Jul 2024 23:05:40 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.5-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:726633ec96a5e5caf3cf182d9f69dce2b8db1ac23ff2927b7c6f08c57eb359ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **769.5 KB (769511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3351eb8d18b222d8e4bb39c70e027dca0e38f8cc6cf6b62f5b0f427b7b1d627`

```dockerfile
```

-	Layers:
	-	`sha256:65b27f4d62d4cae9f25335987cde220dd5cf9adb79b36095620684d82247374f`  
		Last Modified: Mon, 22 Jul 2024 23:05:39 GMT  
		Size: 753.1 KB (753088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c973a06beaa2ea2cc5297d155ac04dd7ceb24eeb6da47fec9465d015b8a86ed`  
		Last Modified: Mon, 22 Jul 2024 23:05:39 GMT  
		Size: 16.4 KB (16423 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.5-meta`

```console
$ docker pull influxdb@sha256:84c943c00c83d325e23e5ca11a500bf92df84a75483c2b1cfad40b627f7de4dc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.5-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:968037645600c8d3c5ed04c459b38993e0c87d17b979292fa1f93a19552b1547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (94000250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0348271af68c472e0d64954c58552351c4d07b37b8c84f2685313bc852d34889`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 11 Jul 2024 20:47:57 GMT
ADD file:430cca9ad155514d8c818e860e66e2aeccfb6230874d4faf446a1d0c2fc1054f in / 
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["bash"]
# Thu, 11 Jul 2024 20:47:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jul 2024 20:47:57 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXDB_VERSION=1.11.5-c1.11.5
# Thu, 11 Jul 2024 20:47:57 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
EXPOSE map[8091/tcp:{}]
# Thu, 11 Jul 2024 20:47:57 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jul 2024 20:47:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:ca4e5d6727252f0dbc207fbf283cb95e278bf562bda42d35ce6c919583a110a0`  
		Last Modified: Tue, 23 Jul 2024 05:27:34 GMT  
		Size: 49.6 MB (49554075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b93c12a9c9326732b35d9e3ebe57148abe33f8fa6e25ab76867410b0ccf876`  
		Last Modified: Tue, 23 Jul 2024 06:13:16 GMT  
		Size: 24.1 MB (24050796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7712e6683588807743ecac6c4908fe81225a4385e63e8adea125a0244ad0ce1`  
		Last Modified: Tue, 23 Jul 2024 07:14:46 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7d8d5b781df318a650a88be6dca42c32a81f15a4f1265ea735fb41e1bf9175`  
		Last Modified: Tue, 23 Jul 2024 07:14:46 GMT  
		Size: 20.4 MB (20393029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6299a2061f1cd6741125ca301d837cde56da42015e33184334bb7d76819dc55e`  
		Last Modified: Tue, 23 Jul 2024 07:14:46 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9fd27ba4cc5c2032f8b464efd3e1eb3114cdcfbfe48a7c41f2b3d04bf912d4`  
		Last Modified: Tue, 23 Jul 2024 07:14:46 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.5-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:2d211af75170e8b95638f5720ff26e5325dd95207c75b14c6d48ff48da6083f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4439965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ce5a69b1cd3ea0a0b1b403849f29c9d129ed24bbaf3450778ef76fefefe1e2f`

```dockerfile
```

-	Layers:
	-	`sha256:7c7ca81871c40422eb451898c142bef2bfb593625c65c584609d04265b59dd47`  
		Last Modified: Tue, 23 Jul 2024 07:14:46 GMT  
		Size: 4.4 MB (4427044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47d186f3a8ebfeb0d1d1e25d544b56cfd186d72a09f061fd9c2699812b59f906`  
		Last Modified: Tue, 23 Jul 2024 07:14:46 GMT  
		Size: 12.9 KB (12921 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.5-meta-alpine`

```console
$ docker pull influxdb@sha256:78fa5b2f40d4e36d43c5b8b457268c3f84630a7d6073ad417bc422280265171d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.5-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:dd1ec4e37011d3ca42de9ae3fe533abe443e2f93eb2d384e841a3f7deea678f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25198998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00ef7fcd3567c5f8e7c837ae578aee29c0f36185159415f695baca20bc22f3bd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 11 Jul 2024 20:47:57 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["/bin/sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXDB_VERSION=1.11.5-c1.11.5
# Thu, 11 Jul 2024 20:47:57 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
EXPOSE map[8091/tcp:{}]
# Thu, 11 Jul 2024 20:47:57 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jul 2024 20:47:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec0d47512f4629295aa8fd6f1d83552091d886f770afc4a5d00963edea45256`  
		Last Modified: Mon, 22 Jul 2024 23:05:35 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ee443a8375d9e90a3385f0333e994b58091f77ba5e52be7d06610b75219aab`  
		Last Modified: Mon, 22 Jul 2024 23:05:35 GMT  
		Size: 1.2 MB (1229932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9056ab6d3880e94254e3c0b56427d1f4a961bb71b2678ee47909e1539a81463d`  
		Last Modified: Mon, 22 Jul 2024 23:05:35 GMT  
		Size: 20.3 MB (20345329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009057299ceac908d66f67eeb9200d08532e9ceeb4cb98cca77e995964899c86`  
		Last Modified: Mon, 22 Jul 2024 23:05:35 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3213ab6698643b46e73196b529f80ca009d81c7e3eb6ee4f20cee2b3768a6dde`  
		Last Modified: Mon, 22 Jul 2024 23:05:36 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.5-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:94c064b8d0a7ac9bc5daf5bc5733ef2e78b8973201abd99f8bedfc649794e7ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **694.1 KB (694055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2bf04c610dd4936298c10fe74d82cdf75e1d95ec3f4e82f804d8228761eb63`

```dockerfile
```

-	Layers:
	-	`sha256:b41b47ac78e24a9424029d231ba40ca59c1466c58ec8f7c1fb9fa1be9175d6eb`  
		Last Modified: Mon, 22 Jul 2024 23:05:35 GMT  
		Size: 679.3 KB (679266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b79971aca68a9439d84b1eb3d5dd63c3422851a359196655b2a17ad32869830d`  
		Last Modified: Mon, 22 Jul 2024 23:05:35 GMT  
		Size: 14.8 KB (14789 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.8`

```console
$ docker pull influxdb@sha256:098f81c86aa2f8cd3dda5fbf80f0a1be36dd4627d8b6f4c69d2adcc4081bae57
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
$ docker pull influxdb@sha256:6ef1c358d207ceabd1a2ff761007933fe367a8d9be323d32cdcf656e8197e205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125737755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3048dd28fe878f446095d70108ff8aef122c6a3042d665236cf7acdbfb2ec18`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 11 Jul 2024 20:47:57 GMT
ADD file:61c91b2a02e0d3deb2364da03241d137acf78345623ae188082e574b043032a0 in / 
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["bash"]
# Thu, 11 Jul 2024 20:47:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jul 2024 20:47:57 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXDB_VERSION=1.8.10
# Thu, 11 Jul 2024 20:47:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb* # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Jul 2024 20:47:57 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jul 2024 20:47:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:73226dab8db5240a2ddbdbe2fb1f0949a911563a62a3d5de3c8669ae708e88de`  
		Last Modified: Tue, 23 Jul 2024 05:28:11 GMT  
		Size: 55.1 MB (55084578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d53dfa00a586795de9dc9f5bc8ad4717b02a8c349b4bbc1f4600a926c5384f40`  
		Last Modified: Tue, 23 Jul 2024 06:14:18 GMT  
		Size: 15.8 MB (15764285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a858ece523c9ef9ec3f519bc9bd26049333de293db155cb7c10620a99f6adf`  
		Last Modified: Tue, 23 Jul 2024 07:14:27 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1c503b7957c0e011afc6da3761979662f02c10758ed22889589f015a8405ba`  
		Last Modified: Tue, 23 Jul 2024 07:14:29 GMT  
		Size: 54.9 MB (54885390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d95e8819e3288cdd782bf26012ad6aaf309b1b01723a9c51b0d6ae4ed847d02`  
		Last Modified: Tue, 23 Jul 2024 07:14:27 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e66b627189791f82ef759024e43e7504ab0890fadfc17878642b92185766955`  
		Last Modified: Tue, 23 Jul 2024 07:14:27 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e5d898090ecd8c6861dd45fc583378257d6620a83c26ee8a7be745d2a2eb26`  
		Last Modified: Tue, 23 Jul 2024 07:14:28 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:da5bc9d40e501e8d0ae8a90fb2fe0173e4f5cc6127bf1365cf7bc1beb2e57d1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4505064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4395b09339655f796ac4d044fbd276fb8d3558e44432c074637196b698329064`

```dockerfile
```

-	Layers:
	-	`sha256:1700e0bf91b4585a215825c54f73dc55cef18048c180442eae7c9eab6241690b`  
		Last Modified: Tue, 23 Jul 2024 07:14:28 GMT  
		Size: 4.5 MB (4489602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c8988d7117b0beb273c12491422fde8552ebd56093fa1acc148f5d4002ead0c`  
		Last Modified: Tue, 23 Jul 2024 07:14:27 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.8` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:54567f26675b2bd14441805405e771fe9aec308326a876a190b870a0624f7866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.7 MB (116738442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ed08ea6e0a5e8078a191d4b05ac243ab77a699c607b8fcbeae78e9998b646c3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 11 Jul 2024 20:47:57 GMT
ADD file:45e512d8c89ef619a4db87ca11813c5b48e6332c4c281a9f0d4aaf7301e85990 in / 
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["bash"]
# Thu, 11 Jul 2024 20:47:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jul 2024 20:47:57 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXDB_VERSION=1.8.10
# Thu, 11 Jul 2024 20:47:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb* # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Jul 2024 20:47:57 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jul 2024 20:47:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:57c3fa3d04a48c55117bbc60f2775c978886b3bc89b70e48e85c0516ce060947`  
		Last Modified: Tue, 23 Jul 2024 03:07:14 GMT  
		Size: 50.2 MB (50242355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a61d577d5393ca0b5e52e6cbd75569b7d9e9b50cb27f783d5482f5f97240ba0`  
		Last Modified: Tue, 23 Jul 2024 03:48:23 GMT  
		Size: 14.9 MB (14879665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035572f49c487e188f94711360719c9046f1c53757defc29e652c9921ac2964f`  
		Last Modified: Tue, 23 Jul 2024 18:04:40 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831f75eb2f94da502decfc48ded607c4db4863b75bd3addb0de36ed5013f2e79`  
		Last Modified: Tue, 23 Jul 2024 18:04:41 GMT  
		Size: 51.6 MB (51612922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d17be05a90f85c9360b0700c706b493ca751e4f77f8c0f78971ae411fdb10bb`  
		Last Modified: Tue, 23 Jul 2024 18:04:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049fbb684456d735a169f30e4e884762fb76e495ec6721a44e76899e3d9804cd`  
		Last Modified: Tue, 23 Jul 2024 18:04:40 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77984ef4286708134411af5754e8d5ec314215a661155509b0fa3d13a6bdacd5`  
		Last Modified: Tue, 23 Jul 2024 18:04:41 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:bfe3b2b49f2447a140dc16d2237d98768008261c44c2e6ed40ecd7f6cbe133df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4506765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c13e418bc75ed8676252513aa2b45f086d3f18d6b0ea5041f6b2ffc133553de3`

```dockerfile
```

-	Layers:
	-	`sha256:3e66335bccc2e048fc689eb1ba4e03de628a659b9554aaecb1a75b6322563934`  
		Last Modified: Tue, 23 Jul 2024 18:04:40 GMT  
		Size: 4.5 MB (4491236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe4ce3a9b83e6eac07e5b584d0964c3bf831949a7e0a97147ffe95a2b21af51a`  
		Last Modified: Tue, 23 Jul 2024 18:04:40 GMT  
		Size: 15.5 KB (15529 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:8eb3af7b4fb89152b7e1dd270a833402e31b89a9e1f267fa2320df1b9da25b00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120712887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69b5eccc8dc2044b5cddba431307cb6b481d23dc501a6b481dc129de9f42cb09`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 11 Jul 2024 20:47:57 GMT
ADD file:bbd5c67ed8e7916601bc20e4ce4973720e715d9dcd892ccbd64c1d5de711a38d in / 
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["bash"]
# Thu, 11 Jul 2024 20:47:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jul 2024 20:47:57 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXDB_VERSION=1.8.10
# Thu, 11 Jul 2024 20:47:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb* # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Jul 2024 20:47:57 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jul 2024 20:47:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:2c9750102c61ce3f4a11c8776dfc892d41a6d4a662d2882e471664dbad58487e`  
		Last Modified: Tue, 23 Jul 2024 04:20:44 GMT  
		Size: 53.7 MB (53729987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c27a83c76abd51a72277b6a74eb7f88e560054e0d04383f64e2886877a20dd5`  
		Last Modified: Tue, 23 Jul 2024 08:11:04 GMT  
		Size: 15.7 MB (15749501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21df34121f07cde46d16a95cd811b085c30efb6036d87df1213f08e35d1cb79`  
		Last Modified: Tue, 23 Jul 2024 18:07:19 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e39d6080d9896adfb15b6593ba316a8bc0f148ef6db18dfaadfeb4988ade57`  
		Last Modified: Tue, 23 Jul 2024 18:07:21 GMT  
		Size: 51.2 MB (51229895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf17eec36ff49bd008bfa5e2c81693ec7233c1e7a66f3803d5819689b586e6d9`  
		Last Modified: Tue, 23 Jul 2024 18:07:19 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa8a6dc3a451c238d403bfe67962d1650bf3b3f2d0a542c5bcb49dd8d88012d`  
		Last Modified: Tue, 23 Jul 2024 18:07:19 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb71850f0370cdf385da02204f0c6e946c516249a71fdca53c874096ac0728a`  
		Last Modified: Tue, 23 Jul 2024 18:07:20 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:46ce5bdd97b5d6f1723e958875f40a7e7547b4721a91b8c7a5a8e2103a06a191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4504969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:950111314cc32ff119fe5320d6b4be32fd045412e2b0e5a93f270804f26ee458`

```dockerfile
```

-	Layers:
	-	`sha256:c212d6e191a5414cd74e41f439f1283e8b5642e6ac5b0462d8c668ba93e0fb83`  
		Last Modified: Tue, 23 Jul 2024 18:07:20 GMT  
		Size: 4.5 MB (4489214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1ac54423b665513d9fd05226d7e0a739158ad6cc100274966e8edfd39ee845b`  
		Last Modified: Tue, 23 Jul 2024 18:07:19 GMT  
		Size: 15.8 KB (15755 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.8-alpine`

```console
$ docker pull influxdb@sha256:f52cd1292b64127ab8678fcac6c4774afc52ca4da3f7d954b1e7be973655d588
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.8-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:1d18534cf6654e90cca79db370ee9f628b7040b059ed6ecef6e107c652765ddc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59520217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24f2eba593dbbf13eb38488802a41effd2a748061e1164c770daee63052225e4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 11 Jul 2024 20:47:57 GMT
ADD file:ec892b6986dac395477ae6947272ea0913b711cda60bbd7d575b374ecfc4cee2 in / 
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["/bin/sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXDB_VERSION=1.8.10
# Thu, 11 Jul 2024 20:47:57 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     chmod +x /usr/src/influxdb-*/influx              /usr/src/influxdb-*/influx_inspect              /usr/src/influxdb-*/influx_stress              /usr/src/influxdb-*/influxd &&    mv /usr/src/influxdb-*/influx        /usr/src/influxdb-*/influx_inspect        /usr/src/influxdb-*/influx_stress         /usr/src/influxdb-*/influxd        /usr/bin/ &&    gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Jul 2024 20:47:57 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jul 2024 20:47:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:b99da37831f37d3f77de0ac7a864f9b69f1dbb4461e5ddfe5a3c2b7e2a3586c5`  
		Last Modified: Mon, 22 Jul 2024 22:27:42 GMT  
		Size: 3.4 MB (3391983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac8005d8f32efbe91f954c7f94051605145a1537a13d6a8a40ea58a05cdd923`  
		Last Modified: Mon, 22 Jul 2024 23:05:32 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90be5351b15930dbb5259af38838fc6f6a39aab34dad44dd1a7ae91135a5030c`  
		Last Modified: Mon, 22 Jul 2024 23:05:32 GMT  
		Size: 1.5 MB (1479518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8bfcf12a3778310fe0b1ea0d28d9cc419712a985efebeafd583ae2a65059db`  
		Last Modified: Mon, 22 Jul 2024 23:05:33 GMT  
		Size: 54.6 MB (54646720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4844ed4fcf4c5b076014ae5536f16103f9fc202489779c33547142c6bfb2df`  
		Last Modified: Mon, 22 Jul 2024 23:05:32 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db830012c2cc0a6857e91d01066d3c71f55d3eb2fb36561d51972c87b5976ef`  
		Last Modified: Mon, 22 Jul 2024 23:05:33 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44cdf117f5104d6bbd0978338066b097f0d1e5e4069a4f7d22cce26aefac350`  
		Last Modified: Mon, 22 Jul 2024 23:05:33 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:7f1151daeb253ceef19200acd646a1e170aa59c08fe2ac4cfb15720d5ea315cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1004063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e004db706551b6381e195e1c846eaeb30e539bc169f73e274ad375fa3173498`

```dockerfile
```

-	Layers:
	-	`sha256:c157689659ad013dca63c0105f86f7d05985d3e53fcb7e4b359fe18fc0613c9e`  
		Last Modified: Mon, 22 Jul 2024 23:05:32 GMT  
		Size: 986.7 KB (986701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13e8616a09f8538bdb569465037d4624e83e8e5170719de9178e68973849b8cc`  
		Last Modified: Mon, 22 Jul 2024 23:05:32 GMT  
		Size: 17.4 KB (17362 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.8.10`

```console
$ docker pull influxdb@sha256:098f81c86aa2f8cd3dda5fbf80f0a1be36dd4627d8b6f4c69d2adcc4081bae57
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
$ docker pull influxdb@sha256:6ef1c358d207ceabd1a2ff761007933fe367a8d9be323d32cdcf656e8197e205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125737755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3048dd28fe878f446095d70108ff8aef122c6a3042d665236cf7acdbfb2ec18`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 11 Jul 2024 20:47:57 GMT
ADD file:61c91b2a02e0d3deb2364da03241d137acf78345623ae188082e574b043032a0 in / 
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["bash"]
# Thu, 11 Jul 2024 20:47:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jul 2024 20:47:57 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXDB_VERSION=1.8.10
# Thu, 11 Jul 2024 20:47:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb* # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Jul 2024 20:47:57 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jul 2024 20:47:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:73226dab8db5240a2ddbdbe2fb1f0949a911563a62a3d5de3c8669ae708e88de`  
		Last Modified: Tue, 23 Jul 2024 05:28:11 GMT  
		Size: 55.1 MB (55084578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d53dfa00a586795de9dc9f5bc8ad4717b02a8c349b4bbc1f4600a926c5384f40`  
		Last Modified: Tue, 23 Jul 2024 06:14:18 GMT  
		Size: 15.8 MB (15764285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a858ece523c9ef9ec3f519bc9bd26049333de293db155cb7c10620a99f6adf`  
		Last Modified: Tue, 23 Jul 2024 07:14:27 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1c503b7957c0e011afc6da3761979662f02c10758ed22889589f015a8405ba`  
		Last Modified: Tue, 23 Jul 2024 07:14:29 GMT  
		Size: 54.9 MB (54885390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d95e8819e3288cdd782bf26012ad6aaf309b1b01723a9c51b0d6ae4ed847d02`  
		Last Modified: Tue, 23 Jul 2024 07:14:27 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e66b627189791f82ef759024e43e7504ab0890fadfc17878642b92185766955`  
		Last Modified: Tue, 23 Jul 2024 07:14:27 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e5d898090ecd8c6861dd45fc583378257d6620a83c26ee8a7be745d2a2eb26`  
		Last Modified: Tue, 23 Jul 2024 07:14:28 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8.10` - unknown; unknown

```console
$ docker pull influxdb@sha256:da5bc9d40e501e8d0ae8a90fb2fe0173e4f5cc6127bf1365cf7bc1beb2e57d1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4505064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4395b09339655f796ac4d044fbd276fb8d3558e44432c074637196b698329064`

```dockerfile
```

-	Layers:
	-	`sha256:1700e0bf91b4585a215825c54f73dc55cef18048c180442eae7c9eab6241690b`  
		Last Modified: Tue, 23 Jul 2024 07:14:28 GMT  
		Size: 4.5 MB (4489602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c8988d7117b0beb273c12491422fde8552ebd56093fa1acc148f5d4002ead0c`  
		Last Modified: Tue, 23 Jul 2024 07:14:27 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.8.10` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:54567f26675b2bd14441805405e771fe9aec308326a876a190b870a0624f7866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.7 MB (116738442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ed08ea6e0a5e8078a191d4b05ac243ab77a699c607b8fcbeae78e9998b646c3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 11 Jul 2024 20:47:57 GMT
ADD file:45e512d8c89ef619a4db87ca11813c5b48e6332c4c281a9f0d4aaf7301e85990 in / 
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["bash"]
# Thu, 11 Jul 2024 20:47:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jul 2024 20:47:57 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXDB_VERSION=1.8.10
# Thu, 11 Jul 2024 20:47:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb* # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Jul 2024 20:47:57 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jul 2024 20:47:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:57c3fa3d04a48c55117bbc60f2775c978886b3bc89b70e48e85c0516ce060947`  
		Last Modified: Tue, 23 Jul 2024 03:07:14 GMT  
		Size: 50.2 MB (50242355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a61d577d5393ca0b5e52e6cbd75569b7d9e9b50cb27f783d5482f5f97240ba0`  
		Last Modified: Tue, 23 Jul 2024 03:48:23 GMT  
		Size: 14.9 MB (14879665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035572f49c487e188f94711360719c9046f1c53757defc29e652c9921ac2964f`  
		Last Modified: Tue, 23 Jul 2024 18:04:40 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831f75eb2f94da502decfc48ded607c4db4863b75bd3addb0de36ed5013f2e79`  
		Last Modified: Tue, 23 Jul 2024 18:04:41 GMT  
		Size: 51.6 MB (51612922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d17be05a90f85c9360b0700c706b493ca751e4f77f8c0f78971ae411fdb10bb`  
		Last Modified: Tue, 23 Jul 2024 18:04:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049fbb684456d735a169f30e4e884762fb76e495ec6721a44e76899e3d9804cd`  
		Last Modified: Tue, 23 Jul 2024 18:04:40 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77984ef4286708134411af5754e8d5ec314215a661155509b0fa3d13a6bdacd5`  
		Last Modified: Tue, 23 Jul 2024 18:04:41 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8.10` - unknown; unknown

```console
$ docker pull influxdb@sha256:bfe3b2b49f2447a140dc16d2237d98768008261c44c2e6ed40ecd7f6cbe133df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4506765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c13e418bc75ed8676252513aa2b45f086d3f18d6b0ea5041f6b2ffc133553de3`

```dockerfile
```

-	Layers:
	-	`sha256:3e66335bccc2e048fc689eb1ba4e03de628a659b9554aaecb1a75b6322563934`  
		Last Modified: Tue, 23 Jul 2024 18:04:40 GMT  
		Size: 4.5 MB (4491236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe4ce3a9b83e6eac07e5b584d0964c3bf831949a7e0a97147ffe95a2b21af51a`  
		Last Modified: Tue, 23 Jul 2024 18:04:40 GMT  
		Size: 15.5 KB (15529 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.8.10` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:8eb3af7b4fb89152b7e1dd270a833402e31b89a9e1f267fa2320df1b9da25b00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120712887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69b5eccc8dc2044b5cddba431307cb6b481d23dc501a6b481dc129de9f42cb09`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 11 Jul 2024 20:47:57 GMT
ADD file:bbd5c67ed8e7916601bc20e4ce4973720e715d9dcd892ccbd64c1d5de711a38d in / 
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["bash"]
# Thu, 11 Jul 2024 20:47:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jul 2024 20:47:57 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXDB_VERSION=1.8.10
# Thu, 11 Jul 2024 20:47:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb* # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Jul 2024 20:47:57 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jul 2024 20:47:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:2c9750102c61ce3f4a11c8776dfc892d41a6d4a662d2882e471664dbad58487e`  
		Last Modified: Tue, 23 Jul 2024 04:20:44 GMT  
		Size: 53.7 MB (53729987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c27a83c76abd51a72277b6a74eb7f88e560054e0d04383f64e2886877a20dd5`  
		Last Modified: Tue, 23 Jul 2024 08:11:04 GMT  
		Size: 15.7 MB (15749501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21df34121f07cde46d16a95cd811b085c30efb6036d87df1213f08e35d1cb79`  
		Last Modified: Tue, 23 Jul 2024 18:07:19 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e39d6080d9896adfb15b6593ba316a8bc0f148ef6db18dfaadfeb4988ade57`  
		Last Modified: Tue, 23 Jul 2024 18:07:21 GMT  
		Size: 51.2 MB (51229895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf17eec36ff49bd008bfa5e2c81693ec7233c1e7a66f3803d5819689b586e6d9`  
		Last Modified: Tue, 23 Jul 2024 18:07:19 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa8a6dc3a451c238d403bfe67962d1650bf3b3f2d0a542c5bcb49dd8d88012d`  
		Last Modified: Tue, 23 Jul 2024 18:07:19 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb71850f0370cdf385da02204f0c6e946c516249a71fdca53c874096ac0728a`  
		Last Modified: Tue, 23 Jul 2024 18:07:20 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8.10` - unknown; unknown

```console
$ docker pull influxdb@sha256:46ce5bdd97b5d6f1723e958875f40a7e7547b4721a91b8c7a5a8e2103a06a191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4504969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:950111314cc32ff119fe5320d6b4be32fd045412e2b0e5a93f270804f26ee458`

```dockerfile
```

-	Layers:
	-	`sha256:c212d6e191a5414cd74e41f439f1283e8b5642e6ac5b0462d8c668ba93e0fb83`  
		Last Modified: Tue, 23 Jul 2024 18:07:20 GMT  
		Size: 4.5 MB (4489214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1ac54423b665513d9fd05226d7e0a739158ad6cc100274966e8edfd39ee845b`  
		Last Modified: Tue, 23 Jul 2024 18:07:19 GMT  
		Size: 15.8 KB (15755 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.8.10-alpine`

```console
$ docker pull influxdb@sha256:f52cd1292b64127ab8678fcac6c4774afc52ca4da3f7d954b1e7be973655d588
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.8.10-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:1d18534cf6654e90cca79db370ee9f628b7040b059ed6ecef6e107c652765ddc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59520217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24f2eba593dbbf13eb38488802a41effd2a748061e1164c770daee63052225e4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 11 Jul 2024 20:47:57 GMT
ADD file:ec892b6986dac395477ae6947272ea0913b711cda60bbd7d575b374ecfc4cee2 in / 
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["/bin/sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXDB_VERSION=1.8.10
# Thu, 11 Jul 2024 20:47:57 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     chmod +x /usr/src/influxdb-*/influx              /usr/src/influxdb-*/influx_inspect              /usr/src/influxdb-*/influx_stress              /usr/src/influxdb-*/influxd &&    mv /usr/src/influxdb-*/influx        /usr/src/influxdb-*/influx_inspect        /usr/src/influxdb-*/influx_stress         /usr/src/influxdb-*/influxd        /usr/bin/ &&    gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Jul 2024 20:47:57 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jul 2024 20:47:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:b99da37831f37d3f77de0ac7a864f9b69f1dbb4461e5ddfe5a3c2b7e2a3586c5`  
		Last Modified: Mon, 22 Jul 2024 22:27:42 GMT  
		Size: 3.4 MB (3391983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac8005d8f32efbe91f954c7f94051605145a1537a13d6a8a40ea58a05cdd923`  
		Last Modified: Mon, 22 Jul 2024 23:05:32 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90be5351b15930dbb5259af38838fc6f6a39aab34dad44dd1a7ae91135a5030c`  
		Last Modified: Mon, 22 Jul 2024 23:05:32 GMT  
		Size: 1.5 MB (1479518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8bfcf12a3778310fe0b1ea0d28d9cc419712a985efebeafd583ae2a65059db`  
		Last Modified: Mon, 22 Jul 2024 23:05:33 GMT  
		Size: 54.6 MB (54646720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4844ed4fcf4c5b076014ae5536f16103f9fc202489779c33547142c6bfb2df`  
		Last Modified: Mon, 22 Jul 2024 23:05:32 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db830012c2cc0a6857e91d01066d3c71f55d3eb2fb36561d51972c87b5976ef`  
		Last Modified: Mon, 22 Jul 2024 23:05:33 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44cdf117f5104d6bbd0978338066b097f0d1e5e4069a4f7d22cce26aefac350`  
		Last Modified: Mon, 22 Jul 2024 23:05:33 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8.10-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:7f1151daeb253ceef19200acd646a1e170aa59c08fe2ac4cfb15720d5ea315cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1004063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e004db706551b6381e195e1c846eaeb30e539bc169f73e274ad375fa3173498`

```dockerfile
```

-	Layers:
	-	`sha256:c157689659ad013dca63c0105f86f7d05985d3e53fcb7e4b359fe18fc0613c9e`  
		Last Modified: Mon, 22 Jul 2024 23:05:32 GMT  
		Size: 986.7 KB (986701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13e8616a09f8538bdb569465037d4624e83e8e5170719de9178e68973849b8cc`  
		Last Modified: Mon, 22 Jul 2024 23:05:32 GMT  
		Size: 17.4 KB (17362 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.9-data`

```console
$ docker pull influxdb@sha256:5e3fa9a1e5aae995bcd168da87f0bdd7a7ae4d39ac8a2eaa8b01707554ab482d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9-data` - linux; amd64

```console
$ docker pull influxdb@sha256:355f77056f7f2e3f9c38e4b1937ad2da609c8e673ef1046671ecd7cac637fdd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104141371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d61136546d439fd0c5cd30fe2cb1f84b6776dae95d746026587d995b34895e7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 11 Jul 2024 20:47:57 GMT
ADD file:61c91b2a02e0d3deb2364da03241d137acf78345623ae188082e574b043032a0 in / 
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["bash"]
# Thu, 11 Jul 2024 20:47:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jul 2024 20:47:57 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Thu, 11 Jul 2024 20:47:57 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb* # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Jul 2024 20:47:57 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jul 2024 20:47:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:73226dab8db5240a2ddbdbe2fb1f0949a911563a62a3d5de3c8669ae708e88de`  
		Last Modified: Tue, 23 Jul 2024 05:28:11 GMT  
		Size: 55.1 MB (55084578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d53dfa00a586795de9dc9f5bc8ad4717b02a8c349b4bbc1f4600a926c5384f40`  
		Last Modified: Tue, 23 Jul 2024 06:14:18 GMT  
		Size: 15.8 MB (15764285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad210c6a8e753035ebd4ba4b31dfb9926982e786037a28b89f64134d63fc021`  
		Last Modified: Tue, 23 Jul 2024 07:14:32 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d687af40e84e34e860749942ebbd83afff7bde2d4a95e069492f22e7cabb2d`  
		Last Modified: Tue, 23 Jul 2024 07:14:33 GMT  
		Size: 33.3 MB (33288961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ee1f0ad724383666ffd4c4a179ce2326bbafade9f6872204de57150001e807`  
		Last Modified: Tue, 23 Jul 2024 07:14:33 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2bdbc5fdde58163e83183fd0cae92bc7210cdd7dcb0eeeae4de5d3d76d42ec0`  
		Last Modified: Tue, 23 Jul 2024 07:14:33 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9c0cb3d030372044c669589c6beab349c9e10f6a66acb3f84c256a52f60626`  
		Last Modified: Tue, 23 Jul 2024 07:14:33 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:db7820c56f95fd4f348d65fd9ba06c25c8790790b53b5ba061257b4d176fa07f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4631026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c980c27fce5b357880d850f553ab7209a0e54bb47f25b568eecdca4c1de3531`

```dockerfile
```

-	Layers:
	-	`sha256:8c79014c1da48b21ef32bc3cb315718eb037e8a46ef97ee3ace64dc63f93e4e0`  
		Last Modified: Tue, 23 Jul 2024 07:14:33 GMT  
		Size: 4.6 MB (4616485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b79dd5c11bbd489eb40008b6356554dcc7f30eaef637b810f904c5ce40488bd8`  
		Last Modified: Tue, 23 Jul 2024 07:14:32 GMT  
		Size: 14.5 KB (14541 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.9-data-alpine`

```console
$ docker pull influxdb@sha256:981099f2d73a30730757a3a2fac107989b1b11ce1a6a0aca0a3eb20aff1b5712
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:ccb4622d0b357f55225b536e9695b15a0c2811da4b855133c32bf78bbe146d75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 MB (38122366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d51b4bb84a1650953a6d5ad2b696d90a051be4a4ca6fa5698f0f79577bf482db`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 11 Jul 2024 20:47:57 GMT
ADD file:ec892b6986dac395477ae6947272ea0913b711cda60bbd7d575b374ecfc4cee2 in / 
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["/bin/sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Thu, 11 Jul 2024 20:47:57 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/etc/influxdb/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Jul 2024 20:47:57 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jul 2024 20:47:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:b99da37831f37d3f77de0ac7a864f9b69f1dbb4461e5ddfe5a3c2b7e2a3586c5`  
		Last Modified: Mon, 22 Jul 2024 22:27:42 GMT  
		Size: 3.4 MB (3391983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3748ccadccdc70cd557570f6bcbabcdfbfa095ac62846d20b0eefc3ba01770d`  
		Last Modified: Mon, 22 Jul 2024 23:05:33 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e07053d6c756ed8fbcec0d6eecd48eeef326b1f92aae3f57760e8701e51fa7e`  
		Last Modified: Mon, 22 Jul 2024 23:05:33 GMT  
		Size: 1.5 MB (1479499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87b93e6a04f81d2f23637f1a8c1f6d2f63b7b5be66652e8420de129cf529e2b`  
		Last Modified: Mon, 22 Jul 2024 23:05:33 GMT  
		Size: 33.2 MB (33248830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5457181f48f2d6046db3e5f84a3846de3b768282d25e54a1d49dd44a83e885f0`  
		Last Modified: Mon, 22 Jul 2024 23:05:33 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dbc4d5f43e57797d1eb5c621a6782209ab9b45747331ca73a001539ca5129ca`  
		Last Modified: Mon, 22 Jul 2024 23:05:34 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44cdf117f5104d6bbd0978338066b097f0d1e5e4069a4f7d22cce26aefac350`  
		Last Modified: Mon, 22 Jul 2024 23:05:33 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:15841646f5556b91743bdfe3027a18857dd9958b02291d9ef4c44a563fc68c1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1137833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fb9c8e7fefeeeb5790f14784ea76c7fa9dc05f72a07f9972f319552e488d3d1`

```dockerfile
```

-	Layers:
	-	`sha256:dbba8117c37d080c1eb223bd7cccfc0643acd0488789911a5253c5a04f29c7c3`  
		Last Modified: Mon, 22 Jul 2024 23:05:33 GMT  
		Size: 1.1 MB (1121385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8b49fbfdce611c1705e00c6df4936f8c89bfa452dc3815b7c5a1ac9c31f92c0`  
		Last Modified: Mon, 22 Jul 2024 23:05:33 GMT  
		Size: 16.4 KB (16448 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.9-meta`

```console
$ docker pull influxdb@sha256:f41faae5d4df0d355dbea876474687fd9797c456fb6355d053d5904314112fe0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:35110124cc571bdebeb9dcdd3bef885979c2c1a34dcfc3e3057b19bdaefcbee4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83620556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94d0d58b984651eb3aac3e3f997bf55acb4254ba4f06bb879644c626271f099a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 11 Jul 2024 20:47:57 GMT
ADD file:61c91b2a02e0d3deb2364da03241d137acf78345623ae188082e574b043032a0 in / 
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["bash"]
# Thu, 11 Jul 2024 20:47:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jul 2024 20:47:57 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Thu, 11 Jul 2024 20:47:57 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb* # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
EXPOSE map[8091/tcp:{}]
# Thu, 11 Jul 2024 20:47:57 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jul 2024 20:47:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:73226dab8db5240a2ddbdbe2fb1f0949a911563a62a3d5de3c8669ae708e88de`  
		Last Modified: Tue, 23 Jul 2024 05:28:11 GMT  
		Size: 55.1 MB (55084578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d53dfa00a586795de9dc9f5bc8ad4717b02a8c349b4bbc1f4600a926c5384f40`  
		Last Modified: Tue, 23 Jul 2024 06:14:18 GMT  
		Size: 15.8 MB (15764285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35bca3e71e909b9442abbb3ee2d1d8c57b72db81de9543dd21a2dafce67eef8`  
		Last Modified: Tue, 23 Jul 2024 07:14:25 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83fb0acbea8d98afab98de1cefb63307a1a93982fdba11a64adf6312bddb144d`  
		Last Modified: Tue, 23 Jul 2024 07:14:25 GMT  
		Size: 12.8 MB (12769354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17126c13bb401478d17468c2066853756ed365b6e9ff6064b8d88a4b9e030c37`  
		Last Modified: Tue, 23 Jul 2024 07:14:25 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f0ac58da24f1f914f7fb619daa7448fda3c2a3aab0a388d7a7a29ac33f1a5c`  
		Last Modified: Tue, 23 Jul 2024 07:14:25 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:35b7e4a062cd26a091c8789f42c8b23d626fb024e2b1f27e0f54237cb2b0120f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4565205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06610aa7b4ca3bfa82d06c274971d854cae382d555fa2118ecf3b1abc6a10b85`

```dockerfile
```

-	Layers:
	-	`sha256:eeb988250006b3d2e98c542c8440a34274a2a5595eb76d4b399d8673fb2e25cd`  
		Last Modified: Tue, 23 Jul 2024 07:14:25 GMT  
		Size: 4.6 MB (4552318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7538432a0de137bf9475febc30a0d0fe192b53dd5e0c2407534733bff5fead38`  
		Last Modified: Tue, 23 Jul 2024 07:14:25 GMT  
		Size: 12.9 KB (12887 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.9-meta-alpine`

```console
$ docker pull influxdb@sha256:7bdb23762424c5c9cb35bc2bea5204f3b8c5bf5141acc97c19d7e2d0b94cfc8f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:f4b74acd2c7db14b564847c48807c388d8206e6062632468f0d77f3433062886
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17574713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6524655e852c1b83406926edf23ff9f9c074789f0e2d9395bc414a05ebad6853`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 11 Jul 2024 20:47:57 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["/bin/sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Thu, 11 Jul 2024 20:47:57 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/etc/influxdb/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
EXPOSE map[8091/tcp:{}]
# Thu, 11 Jul 2024 20:47:57 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jul 2024 20:47:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77c0414ed6183ec37d6313fdd56563a59fe81dc7f317142b871c0aa55eb606c`  
		Last Modified: Mon, 22 Jul 2024 23:05:37 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb115a4a00f2a27ba60d888bafcd5968da6477f02abfd3787ff0a63856200e17`  
		Last Modified: Mon, 22 Jul 2024 23:05:38 GMT  
		Size: 1.2 MB (1229922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e554bccd3dc37ea9faae3dade6d87a70a156e58d42b0ad362442a2ea78efa5eb`  
		Last Modified: Mon, 22 Jul 2024 23:05:38 GMT  
		Size: 12.7 MB (12721055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67cfb0b39d17d59ae791833d34da9afa74d79704683fb65c2bb1a8cc26ffc0b6`  
		Last Modified: Mon, 22 Jul 2024 23:05:37 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5be18e3b49fc131aea50a410f1f2ff4d8ba797d7a15f047811c9ec06bd14275`  
		Last Modified: Mon, 22 Jul 2024 23:05:38 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:24e5e61e687fb237a832eecce75d5a141d8760546f459c9905f1f6176485d38c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **693.0 KB (692994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9253bb162952a664ee36e41e39bec18b26370719c1b00dfbf4316c37dc5a788a`

```dockerfile
```

-	Layers:
	-	`sha256:3ab1ce7dc5c647a2203a730e3b6cde5c12d20cc199e591f3e6d40025f8581432`  
		Last Modified: Mon, 22 Jul 2024 23:05:37 GMT  
		Size: 678.2 KB (678181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bce7575416a0c6a7dc4202b0cad48068d53174fb61755a117dea838eed059442`  
		Last Modified: Mon, 22 Jul 2024 23:05:37 GMT  
		Size: 14.8 KB (14813 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.9.13-data`

```console
$ docker pull influxdb@sha256:5e3fa9a1e5aae995bcd168da87f0bdd7a7ae4d39ac8a2eaa8b01707554ab482d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9.13-data` - linux; amd64

```console
$ docker pull influxdb@sha256:355f77056f7f2e3f9c38e4b1937ad2da609c8e673ef1046671ecd7cac637fdd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104141371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d61136546d439fd0c5cd30fe2cb1f84b6776dae95d746026587d995b34895e7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 11 Jul 2024 20:47:57 GMT
ADD file:61c91b2a02e0d3deb2364da03241d137acf78345623ae188082e574b043032a0 in / 
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["bash"]
# Thu, 11 Jul 2024 20:47:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jul 2024 20:47:57 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Thu, 11 Jul 2024 20:47:57 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb* # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Jul 2024 20:47:57 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jul 2024 20:47:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:73226dab8db5240a2ddbdbe2fb1f0949a911563a62a3d5de3c8669ae708e88de`  
		Last Modified: Tue, 23 Jul 2024 05:28:11 GMT  
		Size: 55.1 MB (55084578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d53dfa00a586795de9dc9f5bc8ad4717b02a8c349b4bbc1f4600a926c5384f40`  
		Last Modified: Tue, 23 Jul 2024 06:14:18 GMT  
		Size: 15.8 MB (15764285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad210c6a8e753035ebd4ba4b31dfb9926982e786037a28b89f64134d63fc021`  
		Last Modified: Tue, 23 Jul 2024 07:14:32 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d687af40e84e34e860749942ebbd83afff7bde2d4a95e069492f22e7cabb2d`  
		Last Modified: Tue, 23 Jul 2024 07:14:33 GMT  
		Size: 33.3 MB (33288961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ee1f0ad724383666ffd4c4a179ce2326bbafade9f6872204de57150001e807`  
		Last Modified: Tue, 23 Jul 2024 07:14:33 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2bdbc5fdde58163e83183fd0cae92bc7210cdd7dcb0eeeae4de5d3d76d42ec0`  
		Last Modified: Tue, 23 Jul 2024 07:14:33 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9c0cb3d030372044c669589c6beab349c9e10f6a66acb3f84c256a52f60626`  
		Last Modified: Tue, 23 Jul 2024 07:14:33 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9.13-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:db7820c56f95fd4f348d65fd9ba06c25c8790790b53b5ba061257b4d176fa07f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4631026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c980c27fce5b357880d850f553ab7209a0e54bb47f25b568eecdca4c1de3531`

```dockerfile
```

-	Layers:
	-	`sha256:8c79014c1da48b21ef32bc3cb315718eb037e8a46ef97ee3ace64dc63f93e4e0`  
		Last Modified: Tue, 23 Jul 2024 07:14:33 GMT  
		Size: 4.6 MB (4616485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b79dd5c11bbd489eb40008b6356554dcc7f30eaef637b810f904c5ce40488bd8`  
		Last Modified: Tue, 23 Jul 2024 07:14:32 GMT  
		Size: 14.5 KB (14541 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.9.13-data-alpine`

```console
$ docker pull influxdb@sha256:981099f2d73a30730757a3a2fac107989b1b11ce1a6a0aca0a3eb20aff1b5712
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9.13-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:ccb4622d0b357f55225b536e9695b15a0c2811da4b855133c32bf78bbe146d75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 MB (38122366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d51b4bb84a1650953a6d5ad2b696d90a051be4a4ca6fa5698f0f79577bf482db`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 11 Jul 2024 20:47:57 GMT
ADD file:ec892b6986dac395477ae6947272ea0913b711cda60bbd7d575b374ecfc4cee2 in / 
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["/bin/sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Thu, 11 Jul 2024 20:47:57 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/etc/influxdb/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Jul 2024 20:47:57 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jul 2024 20:47:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:b99da37831f37d3f77de0ac7a864f9b69f1dbb4461e5ddfe5a3c2b7e2a3586c5`  
		Last Modified: Mon, 22 Jul 2024 22:27:42 GMT  
		Size: 3.4 MB (3391983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3748ccadccdc70cd557570f6bcbabcdfbfa095ac62846d20b0eefc3ba01770d`  
		Last Modified: Mon, 22 Jul 2024 23:05:33 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e07053d6c756ed8fbcec0d6eecd48eeef326b1f92aae3f57760e8701e51fa7e`  
		Last Modified: Mon, 22 Jul 2024 23:05:33 GMT  
		Size: 1.5 MB (1479499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87b93e6a04f81d2f23637f1a8c1f6d2f63b7b5be66652e8420de129cf529e2b`  
		Last Modified: Mon, 22 Jul 2024 23:05:33 GMT  
		Size: 33.2 MB (33248830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5457181f48f2d6046db3e5f84a3846de3b768282d25e54a1d49dd44a83e885f0`  
		Last Modified: Mon, 22 Jul 2024 23:05:33 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dbc4d5f43e57797d1eb5c621a6782209ab9b45747331ca73a001539ca5129ca`  
		Last Modified: Mon, 22 Jul 2024 23:05:34 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44cdf117f5104d6bbd0978338066b097f0d1e5e4069a4f7d22cce26aefac350`  
		Last Modified: Mon, 22 Jul 2024 23:05:33 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9.13-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:15841646f5556b91743bdfe3027a18857dd9958b02291d9ef4c44a563fc68c1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1137833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fb9c8e7fefeeeb5790f14784ea76c7fa9dc05f72a07f9972f319552e488d3d1`

```dockerfile
```

-	Layers:
	-	`sha256:dbba8117c37d080c1eb223bd7cccfc0643acd0488789911a5253c5a04f29c7c3`  
		Last Modified: Mon, 22 Jul 2024 23:05:33 GMT  
		Size: 1.1 MB (1121385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8b49fbfdce611c1705e00c6df4936f8c89bfa452dc3815b7c5a1ac9c31f92c0`  
		Last Modified: Mon, 22 Jul 2024 23:05:33 GMT  
		Size: 16.4 KB (16448 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.9.13-meta`

```console
$ docker pull influxdb@sha256:f41faae5d4df0d355dbea876474687fd9797c456fb6355d053d5904314112fe0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9.13-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:35110124cc571bdebeb9dcdd3bef885979c2c1a34dcfc3e3057b19bdaefcbee4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83620556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94d0d58b984651eb3aac3e3f997bf55acb4254ba4f06bb879644c626271f099a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 11 Jul 2024 20:47:57 GMT
ADD file:61c91b2a02e0d3deb2364da03241d137acf78345623ae188082e574b043032a0 in / 
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["bash"]
# Thu, 11 Jul 2024 20:47:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jul 2024 20:47:57 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Thu, 11 Jul 2024 20:47:57 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb* # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
EXPOSE map[8091/tcp:{}]
# Thu, 11 Jul 2024 20:47:57 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jul 2024 20:47:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:73226dab8db5240a2ddbdbe2fb1f0949a911563a62a3d5de3c8669ae708e88de`  
		Last Modified: Tue, 23 Jul 2024 05:28:11 GMT  
		Size: 55.1 MB (55084578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d53dfa00a586795de9dc9f5bc8ad4717b02a8c349b4bbc1f4600a926c5384f40`  
		Last Modified: Tue, 23 Jul 2024 06:14:18 GMT  
		Size: 15.8 MB (15764285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35bca3e71e909b9442abbb3ee2d1d8c57b72db81de9543dd21a2dafce67eef8`  
		Last Modified: Tue, 23 Jul 2024 07:14:25 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83fb0acbea8d98afab98de1cefb63307a1a93982fdba11a64adf6312bddb144d`  
		Last Modified: Tue, 23 Jul 2024 07:14:25 GMT  
		Size: 12.8 MB (12769354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17126c13bb401478d17468c2066853756ed365b6e9ff6064b8d88a4b9e030c37`  
		Last Modified: Tue, 23 Jul 2024 07:14:25 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f0ac58da24f1f914f7fb619daa7448fda3c2a3aab0a388d7a7a29ac33f1a5c`  
		Last Modified: Tue, 23 Jul 2024 07:14:25 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9.13-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:35b7e4a062cd26a091c8789f42c8b23d626fb024e2b1f27e0f54237cb2b0120f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4565205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06610aa7b4ca3bfa82d06c274971d854cae382d555fa2118ecf3b1abc6a10b85`

```dockerfile
```

-	Layers:
	-	`sha256:eeb988250006b3d2e98c542c8440a34274a2a5595eb76d4b399d8673fb2e25cd`  
		Last Modified: Tue, 23 Jul 2024 07:14:25 GMT  
		Size: 4.6 MB (4552318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7538432a0de137bf9475febc30a0d0fe192b53dd5e0c2407534733bff5fead38`  
		Last Modified: Tue, 23 Jul 2024 07:14:25 GMT  
		Size: 12.9 KB (12887 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.9.13-meta-alpine`

```console
$ docker pull influxdb@sha256:7bdb23762424c5c9cb35bc2bea5204f3b8c5bf5141acc97c19d7e2d0b94cfc8f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9.13-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:f4b74acd2c7db14b564847c48807c388d8206e6062632468f0d77f3433062886
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17574713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6524655e852c1b83406926edf23ff9f9c074789f0e2d9395bc414a05ebad6853`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 11 Jul 2024 20:47:57 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["/bin/sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Thu, 11 Jul 2024 20:47:57 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/etc/influxdb/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
EXPOSE map[8091/tcp:{}]
# Thu, 11 Jul 2024 20:47:57 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jul 2024 20:47:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77c0414ed6183ec37d6313fdd56563a59fe81dc7f317142b871c0aa55eb606c`  
		Last Modified: Mon, 22 Jul 2024 23:05:37 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb115a4a00f2a27ba60d888bafcd5968da6477f02abfd3787ff0a63856200e17`  
		Last Modified: Mon, 22 Jul 2024 23:05:38 GMT  
		Size: 1.2 MB (1229922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e554bccd3dc37ea9faae3dade6d87a70a156e58d42b0ad362442a2ea78efa5eb`  
		Last Modified: Mon, 22 Jul 2024 23:05:38 GMT  
		Size: 12.7 MB (12721055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67cfb0b39d17d59ae791833d34da9afa74d79704683fb65c2bb1a8cc26ffc0b6`  
		Last Modified: Mon, 22 Jul 2024 23:05:37 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5be18e3b49fc131aea50a410f1f2ff4d8ba797d7a15f047811c9ec06bd14275`  
		Last Modified: Mon, 22 Jul 2024 23:05:38 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9.13-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:24e5e61e687fb237a832eecce75d5a141d8760546f459c9905f1f6176485d38c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **693.0 KB (692994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9253bb162952a664ee36e41e39bec18b26370719c1b00dfbf4316c37dc5a788a`

```dockerfile
```

-	Layers:
	-	`sha256:3ab1ce7dc5c647a2203a730e3b6cde5c12d20cc199e591f3e6d40025f8581432`  
		Last Modified: Mon, 22 Jul 2024 23:05:37 GMT  
		Size: 678.2 KB (678181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bce7575416a0c6a7dc4202b0cad48068d53174fb61755a117dea838eed059442`  
		Last Modified: Mon, 22 Jul 2024 23:05:37 GMT  
		Size: 14.8 KB (14813 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2`

```console
$ docker pull influxdb@sha256:3f52e727ad6f76202388d8461a4c92b883c169bd2409bcf2bcafd60ce448fc5c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2` - linux; amd64

```console
$ docker pull influxdb@sha256:e5caa85f18216d92d27adb02fb91cfc6c98aac9ecd7355a80efcb558c63f6b19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168482883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f26019eadb9acbba9378124cb10170b621c3d3aaad1af8b1a32061ca755df0a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 11 Jul 2024 20:47:57 GMT
ADD file:6c4730e7b12278bc7eb83b3b9d659437c92c42fc7ee70922ae8c4bebfb56a602 in / 
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["bash"]
# Thu, 11 Jul 2024 20:47:57 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV GOSU_VER=1.16
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXDB_VERSION=2.7.7
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 11 Jul 2024 20:47:57 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["influxd"]
# Thu, 11 Jul 2024 20:47:57 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 11 Jul 2024 20:47:57 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:efc2b5ad9eec05befa54239d53feeae3569ccbef689aa5e5dbfc25da6c4df559`  
		Last Modified: Tue, 23 Jul 2024 05:27:55 GMT  
		Size: 29.1 MB (29126287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22338516b2c3a384ef121fc1be4117457521cc28b7e49f84d3844566393dcbf4`  
		Last Modified: Tue, 23 Jul 2024 07:14:41 GMT  
		Size: 9.8 MB (9786187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac58becbac91dc22721c4bddf5b16a010cc0ac8b78fa9da9c77ea6cbee97e3bb`  
		Last Modified: Tue, 23 Jul 2024 07:14:41 GMT  
		Size: 5.8 MB (5820938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e42e673a8ae1ab1d8fc5db3121984aefb2a875239f966f93bac06ca732cc7f8`  
		Last Modified: Tue, 23 Jul 2024 07:14:41 GMT  
		Size: 3.2 KB (3226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ff614d7de17822649a373bf73d773320b1bdb865318678d0b4ef4977131282`  
		Last Modified: Tue, 23 Jul 2024 07:14:41 GMT  
		Size: 1.0 MB (1006375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8208204cff517a7b65a51a644ab584848a3370c7daa173aaa3481505bf12268`  
		Last Modified: Tue, 23 Jul 2024 07:14:43 GMT  
		Size: 99.6 MB (99604818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1929499f66d1a530f2797991e2886b1ca096fec9bbfd53f9adbdbd8624a114f1`  
		Last Modified: Tue, 23 Jul 2024 07:14:43 GMT  
		Size: 23.1 MB (23128322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f23b9837bf2e93895fedd50a59f58d21b04b2bb1903c3a4501eb8f6163d432c6`  
		Last Modified: Tue, 23 Jul 2024 07:14:42 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6466f3f77518b31b3654cea74b2328d01a9180754eb9e646bfc989fcd2ad47f0`  
		Last Modified: Tue, 23 Jul 2024 07:14:42 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aca036d4f9771de5ef76573cad0e3b0d7b85b1ac31b1aa42337d40de8b2e78f`  
		Last Modified: Tue, 23 Jul 2024 07:14:43 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:43fdd95cc12ecd9c5fbd0ceaf2fbeb17e58b2578eca1fe0b5939c1e1327bae1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:373e0fe134451558207814192070ce829957f2f6d71acc5313e26ca71afff868`

```dockerfile
```

-	Layers:
	-	`sha256:f6be574d8c745480b11a730d530d10b703c55a6d75425cec12b60ea60d5e0343`  
		Last Modified: Tue, 23 Jul 2024 07:14:41 GMT  
		Size: 2.8 MB (2833446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92aa852aed4af10be99849b53ebf64f9f53e41a1ea4c26751666c5f6a06eccb5`  
		Last Modified: Tue, 23 Jul 2024 07:14:41 GMT  
		Size: 33.5 KB (33540 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:6fc30098c206be774ed40d58f7ba5f57fd474cdd8e9401a9ba53a58758cd9dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162257327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18af809fb3588e1c6bab1a68368a4e6aa3bd9c5425ea77648a6b597a45da748f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 11 Jul 2024 20:47:57 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["bash"]
# Thu, 11 Jul 2024 20:47:57 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV GOSU_VER=1.16
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXDB_VERSION=2.7.7
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 11 Jul 2024 20:47:57 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["influxd"]
# Thu, 11 Jul 2024 20:47:57 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 11 Jul 2024 20:47:57 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67594e2e4aadf6baf66ac584c9fb6d83c809848e40f81bb739a001042589ccc2`  
		Last Modified: Tue, 23 Jul 2024 18:08:05 GMT  
		Size: 9.6 MB (9585121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029fa3409050b4d29ab49826756ef0ba10eea4bb6529ad8d696e69716515cf9a`  
		Last Modified: Tue, 23 Jul 2024 18:08:05 GMT  
		Size: 5.5 MB (5463796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e760cb86365539321da91ea2ecbd850cf9b4c00c74d22ee6aba4b1a5d31058d2`  
		Last Modified: Tue, 23 Jul 2024 18:08:04 GMT  
		Size: 3.2 KB (3224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9ddc905ddf37e776b4366405135b9ba49d670dae38dd71845af8f056c6b9b7`  
		Last Modified: Tue, 23 Jul 2024 18:08:05 GMT  
		Size: 936.1 KB (936106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ebd1e919c87ac45543c29b0b3a82a730ea7a7d28b0142d4cd83abcf63f92a9`  
		Last Modified: Tue, 23 Jul 2024 18:08:08 GMT  
		Size: 95.4 MB (95443280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed46f9349ddb8ffe48f56000fbf392c27f0a068fdd9e12c7fc7ebe49de719044`  
		Last Modified: Tue, 23 Jul 2024 18:08:07 GMT  
		Size: 21.7 MB (21662499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfa519bf3b45b0205f6abd623aa279262232dd3f3dd1f6a2d56f87acc0bc5db`  
		Last Modified: Tue, 23 Jul 2024 18:08:06 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d970d0ab9823c6f2cba6ee08efa804f42a149ab5801e9ba9b2bce0ed39197fe`  
		Last Modified: Tue, 23 Jul 2024 18:08:06 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b0745af95af38669f2e7868f4a109fcfc276707caa607972e06a18aeecbf40`  
		Last Modified: Tue, 23 Jul 2024 18:08:07 GMT  
		Size: 6.3 KB (6288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:c339ec1048e488d9e89cb3ce0374efbf00c4bc26d98f780301ee2fbb19123d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c18b2ca8457af116f9e445ed2e3054f0c55cb3f5b938ea40da06189b29bf25d0`

```dockerfile
```

-	Layers:
	-	`sha256:76db0783b7f4f0d0f478abe282c1e0ccac878c7d3e6c3e9fc186acd5c31959f2`  
		Last Modified: Tue, 23 Jul 2024 18:08:05 GMT  
		Size: 2.8 MB (2832683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3916f78c10e8d9745c67fe9f4b4017de13148117da95eedbee5e64ba423c7040`  
		Last Modified: Tue, 23 Jul 2024 18:08:04 GMT  
		Size: 33.8 KB (33843 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2-alpine`

```console
$ docker pull influxdb@sha256:c0eb6d9abd89dee9efc9f55e9ad81acb9db6db87e882667456a279ab7d61e25d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:980de6c467cf58935b54df248930259c47771cec6d3580e4c899fce364186f2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (92011663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c8369e23002583137c2fd7b5d9100ef3f597613b8d44a9652ad63b159df4309`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 11 Jul 2024 20:47:57 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["/bin/sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXDB_VERSION=2.7.7
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 11 Jul 2024 20:47:57 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["influxd"]
# Thu, 11 Jul 2024 20:47:57 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 11 Jul 2024 20:47:57 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0dc81762ab9cd4ef11ab0791cc1e4b892353c5ad16f3506e394ed6f4851e93`  
		Last Modified: Mon, 22 Jul 2024 23:05:36 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f18cef9a6cf8c8b1886e10d167cf6ab545b58cf2b96ccbfd151486bebdc7e6`  
		Last Modified: Mon, 22 Jul 2024 23:05:37 GMT  
		Size: 9.6 MB (9633256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c65a22e031fff63369e94994f8c1bf122ea9e4710a99745ba002d3668f2e53`  
		Last Modified: Mon, 22 Jul 2024 23:05:37 GMT  
		Size: 5.8 MB (5820927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0e14a2477df6c25c76b13f5009de5ceb13143a8cdae2647b3fda7d73cbe737`  
		Last Modified: Mon, 22 Jul 2024 23:05:36 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc70ac1afb69874bc1da494b05e87a8b12713f12f637f0e28838a57debc79be`  
		Last Modified: Mon, 22 Jul 2024 23:05:38 GMT  
		Size: 49.8 MB (49798314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff79ccb638859c2f93bc6b478d404485f0132770e580fd7c8d8a7fb8bfbe4b59`  
		Last Modified: Mon, 22 Jul 2024 23:05:38 GMT  
		Size: 23.1 MB (23128309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d98ec689fb5fab393c0e5c79138f617fa94d1c90e1ad0282abca6621c24675`  
		Last Modified: Mon, 22 Jul 2024 23:05:37 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1ea18c19e317393625c2c2939b3521fbc7ebba56bcb67cb68c068178955be7`  
		Last Modified: Mon, 22 Jul 2024 23:05:38 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7be8260682ef0a7adf8bd76b1950e012e93251862938923b508d7233a4dda1e`  
		Last Modified: Mon, 22 Jul 2024 23:05:38 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:b54de15363255b99d02d523b11514f1fe6f0e3a5f2bb67f22630ffa114929e5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.8 KB (944844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ac085702ffdda597a0b0cd8a1d8a890d7be317e1ae9d80df00320ec263ccda`

```dockerfile
```

-	Layers:
	-	`sha256:ab6f2b1e7c2aaa25faf3c871425e0419810e6a848cf15112dd95d05367dc0af7`  
		Last Modified: Mon, 22 Jul 2024 23:05:37 GMT  
		Size: 914.1 KB (914097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0db21d24731eed915a390cb46f22fcd094da7250ff07e8b773a1668085beebb1`  
		Last Modified: Mon, 22 Jul 2024 23:05:36 GMT  
		Size: 30.7 KB (30747 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:4c902582ab94505dd9e4c352ee0aff3048da9db7547e1012bdb79f3fa5daed13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88698755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68b49009cd3aca0446c38075b0ee0a77c2d775f54a99db28c921b59798884940`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 11 Jul 2024 20:47:57 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["/bin/sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXDB_VERSION=2.7.7
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 11 Jul 2024 20:47:57 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["influxd"]
# Thu, 11 Jul 2024 20:47:57 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 11 Jul 2024 20:47:57 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8919d5c79f658c9457d7a0f263bed9aff06bd63364af32b6bd6d948e2ffe5d`  
		Last Modified: Tue, 23 Jul 2024 18:08:40 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1fb104d942a3d0f0121732315db070fa51fd2e6cd64f9f4e7f8072cf5badb3`  
		Last Modified: Tue, 23 Jul 2024 18:08:40 GMT  
		Size: 9.8 MB (9760309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41f50520b6dfcfbe83d195a3a6b16b10b60e5c4058bd26a4f4a18f635134277`  
		Last Modified: Tue, 23 Jul 2024 18:08:40 GMT  
		Size: 5.5 MB (5463802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d079f2db321015236eff90f84c90e021d8133b242abbf9d6b170909f089827f`  
		Last Modified: Tue, 23 Jul 2024 18:08:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef02808a1dee2f5fa0729f991cb391f0880fa7cddf154f9acf77e0599fc8d84`  
		Last Modified: Tue, 23 Jul 2024 18:08:42 GMT  
		Size: 47.7 MB (47717248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03105aa47dfaad2780af3be9e10241551f9e93c90595f0ef7ea18ce01b4703e`  
		Last Modified: Tue, 23 Jul 2024 18:08:42 GMT  
		Size: 21.7 MB (21662496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be554794a10b5f70328f1a09f4b4c1934a1824c5d80e5b348524a2cee587020e`  
		Last Modified: Tue, 23 Jul 2024 18:08:41 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a615ab1c18038858040618fb58198c60b6d71f5d33af5852e992cbe54c469506`  
		Last Modified: Tue, 23 Jul 2024 18:08:42 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f7c06ca922ee2c0aef4c608c7df590708a18a18310e6679da55a762aeb607d`  
		Last Modified: Tue, 23 Jul 2024 18:08:42 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:434b30874520707afca8b4fd88bb5d56d18635494cac2ba9a5b81e69fab7ba9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.4 KB (944405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab93af0394b7cd8ab1b9bd687293c5802b03776e8a474526a958dcb1c7d447f`

```dockerfile
```

-	Layers:
	-	`sha256:0655772b893afadcce60bc0e6b913cf136c9892a51cddcd6b2a3a095b89599ba`  
		Last Modified: Tue, 23 Jul 2024 18:08:40 GMT  
		Size: 913.4 KB (913358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:556806b8d211baa4e0da276bae3645005542ab1065e7a6efdacd52d6d235df80`  
		Last Modified: Tue, 23 Jul 2024 18:08:40 GMT  
		Size: 31.0 KB (31047 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7`

```console
$ docker pull influxdb@sha256:3f52e727ad6f76202388d8461a4c92b883c169bd2409bcf2bcafd60ce448fc5c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7` - linux; amd64

```console
$ docker pull influxdb@sha256:e5caa85f18216d92d27adb02fb91cfc6c98aac9ecd7355a80efcb558c63f6b19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168482883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f26019eadb9acbba9378124cb10170b621c3d3aaad1af8b1a32061ca755df0a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 11 Jul 2024 20:47:57 GMT
ADD file:6c4730e7b12278bc7eb83b3b9d659437c92c42fc7ee70922ae8c4bebfb56a602 in / 
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["bash"]
# Thu, 11 Jul 2024 20:47:57 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV GOSU_VER=1.16
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXDB_VERSION=2.7.7
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 11 Jul 2024 20:47:57 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["influxd"]
# Thu, 11 Jul 2024 20:47:57 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 11 Jul 2024 20:47:57 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:efc2b5ad9eec05befa54239d53feeae3569ccbef689aa5e5dbfc25da6c4df559`  
		Last Modified: Tue, 23 Jul 2024 05:27:55 GMT  
		Size: 29.1 MB (29126287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22338516b2c3a384ef121fc1be4117457521cc28b7e49f84d3844566393dcbf4`  
		Last Modified: Tue, 23 Jul 2024 07:14:41 GMT  
		Size: 9.8 MB (9786187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac58becbac91dc22721c4bddf5b16a010cc0ac8b78fa9da9c77ea6cbee97e3bb`  
		Last Modified: Tue, 23 Jul 2024 07:14:41 GMT  
		Size: 5.8 MB (5820938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e42e673a8ae1ab1d8fc5db3121984aefb2a875239f966f93bac06ca732cc7f8`  
		Last Modified: Tue, 23 Jul 2024 07:14:41 GMT  
		Size: 3.2 KB (3226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ff614d7de17822649a373bf73d773320b1bdb865318678d0b4ef4977131282`  
		Last Modified: Tue, 23 Jul 2024 07:14:41 GMT  
		Size: 1.0 MB (1006375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8208204cff517a7b65a51a644ab584848a3370c7daa173aaa3481505bf12268`  
		Last Modified: Tue, 23 Jul 2024 07:14:43 GMT  
		Size: 99.6 MB (99604818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1929499f66d1a530f2797991e2886b1ca096fec9bbfd53f9adbdbd8624a114f1`  
		Last Modified: Tue, 23 Jul 2024 07:14:43 GMT  
		Size: 23.1 MB (23128322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f23b9837bf2e93895fedd50a59f58d21b04b2bb1903c3a4501eb8f6163d432c6`  
		Last Modified: Tue, 23 Jul 2024 07:14:42 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6466f3f77518b31b3654cea74b2328d01a9180754eb9e646bfc989fcd2ad47f0`  
		Last Modified: Tue, 23 Jul 2024 07:14:42 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aca036d4f9771de5ef76573cad0e3b0d7b85b1ac31b1aa42337d40de8b2e78f`  
		Last Modified: Tue, 23 Jul 2024 07:14:43 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:43fdd95cc12ecd9c5fbd0ceaf2fbeb17e58b2578eca1fe0b5939c1e1327bae1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:373e0fe134451558207814192070ce829957f2f6d71acc5313e26ca71afff868`

```dockerfile
```

-	Layers:
	-	`sha256:f6be574d8c745480b11a730d530d10b703c55a6d75425cec12b60ea60d5e0343`  
		Last Modified: Tue, 23 Jul 2024 07:14:41 GMT  
		Size: 2.8 MB (2833446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92aa852aed4af10be99849b53ebf64f9f53e41a1ea4c26751666c5f6a06eccb5`  
		Last Modified: Tue, 23 Jul 2024 07:14:41 GMT  
		Size: 33.5 KB (33540 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:6fc30098c206be774ed40d58f7ba5f57fd474cdd8e9401a9ba53a58758cd9dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162257327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18af809fb3588e1c6bab1a68368a4e6aa3bd9c5425ea77648a6b597a45da748f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 11 Jul 2024 20:47:57 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["bash"]
# Thu, 11 Jul 2024 20:47:57 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV GOSU_VER=1.16
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXDB_VERSION=2.7.7
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 11 Jul 2024 20:47:57 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["influxd"]
# Thu, 11 Jul 2024 20:47:57 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 11 Jul 2024 20:47:57 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67594e2e4aadf6baf66ac584c9fb6d83c809848e40f81bb739a001042589ccc2`  
		Last Modified: Tue, 23 Jul 2024 18:08:05 GMT  
		Size: 9.6 MB (9585121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029fa3409050b4d29ab49826756ef0ba10eea4bb6529ad8d696e69716515cf9a`  
		Last Modified: Tue, 23 Jul 2024 18:08:05 GMT  
		Size: 5.5 MB (5463796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e760cb86365539321da91ea2ecbd850cf9b4c00c74d22ee6aba4b1a5d31058d2`  
		Last Modified: Tue, 23 Jul 2024 18:08:04 GMT  
		Size: 3.2 KB (3224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9ddc905ddf37e776b4366405135b9ba49d670dae38dd71845af8f056c6b9b7`  
		Last Modified: Tue, 23 Jul 2024 18:08:05 GMT  
		Size: 936.1 KB (936106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ebd1e919c87ac45543c29b0b3a82a730ea7a7d28b0142d4cd83abcf63f92a9`  
		Last Modified: Tue, 23 Jul 2024 18:08:08 GMT  
		Size: 95.4 MB (95443280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed46f9349ddb8ffe48f56000fbf392c27f0a068fdd9e12c7fc7ebe49de719044`  
		Last Modified: Tue, 23 Jul 2024 18:08:07 GMT  
		Size: 21.7 MB (21662499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfa519bf3b45b0205f6abd623aa279262232dd3f3dd1f6a2d56f87acc0bc5db`  
		Last Modified: Tue, 23 Jul 2024 18:08:06 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d970d0ab9823c6f2cba6ee08efa804f42a149ab5801e9ba9b2bce0ed39197fe`  
		Last Modified: Tue, 23 Jul 2024 18:08:06 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b0745af95af38669f2e7868f4a109fcfc276707caa607972e06a18aeecbf40`  
		Last Modified: Tue, 23 Jul 2024 18:08:07 GMT  
		Size: 6.3 KB (6288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:c339ec1048e488d9e89cb3ce0374efbf00c4bc26d98f780301ee2fbb19123d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c18b2ca8457af116f9e445ed2e3054f0c55cb3f5b938ea40da06189b29bf25d0`

```dockerfile
```

-	Layers:
	-	`sha256:76db0783b7f4f0d0f478abe282c1e0ccac878c7d3e6c3e9fc186acd5c31959f2`  
		Last Modified: Tue, 23 Jul 2024 18:08:05 GMT  
		Size: 2.8 MB (2832683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3916f78c10e8d9745c67fe9f4b4017de13148117da95eedbee5e64ba423c7040`  
		Last Modified: Tue, 23 Jul 2024 18:08:04 GMT  
		Size: 33.8 KB (33843 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7-alpine`

```console
$ docker pull influxdb@sha256:c0eb6d9abd89dee9efc9f55e9ad81acb9db6db87e882667456a279ab7d61e25d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:980de6c467cf58935b54df248930259c47771cec6d3580e4c899fce364186f2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (92011663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c8369e23002583137c2fd7b5d9100ef3f597613b8d44a9652ad63b159df4309`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 11 Jul 2024 20:47:57 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["/bin/sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXDB_VERSION=2.7.7
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 11 Jul 2024 20:47:57 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["influxd"]
# Thu, 11 Jul 2024 20:47:57 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 11 Jul 2024 20:47:57 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0dc81762ab9cd4ef11ab0791cc1e4b892353c5ad16f3506e394ed6f4851e93`  
		Last Modified: Mon, 22 Jul 2024 23:05:36 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f18cef9a6cf8c8b1886e10d167cf6ab545b58cf2b96ccbfd151486bebdc7e6`  
		Last Modified: Mon, 22 Jul 2024 23:05:37 GMT  
		Size: 9.6 MB (9633256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c65a22e031fff63369e94994f8c1bf122ea9e4710a99745ba002d3668f2e53`  
		Last Modified: Mon, 22 Jul 2024 23:05:37 GMT  
		Size: 5.8 MB (5820927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0e14a2477df6c25c76b13f5009de5ceb13143a8cdae2647b3fda7d73cbe737`  
		Last Modified: Mon, 22 Jul 2024 23:05:36 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc70ac1afb69874bc1da494b05e87a8b12713f12f637f0e28838a57debc79be`  
		Last Modified: Mon, 22 Jul 2024 23:05:38 GMT  
		Size: 49.8 MB (49798314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff79ccb638859c2f93bc6b478d404485f0132770e580fd7c8d8a7fb8bfbe4b59`  
		Last Modified: Mon, 22 Jul 2024 23:05:38 GMT  
		Size: 23.1 MB (23128309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d98ec689fb5fab393c0e5c79138f617fa94d1c90e1ad0282abca6621c24675`  
		Last Modified: Mon, 22 Jul 2024 23:05:37 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1ea18c19e317393625c2c2939b3521fbc7ebba56bcb67cb68c068178955be7`  
		Last Modified: Mon, 22 Jul 2024 23:05:38 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7be8260682ef0a7adf8bd76b1950e012e93251862938923b508d7233a4dda1e`  
		Last Modified: Mon, 22 Jul 2024 23:05:38 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:b54de15363255b99d02d523b11514f1fe6f0e3a5f2bb67f22630ffa114929e5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.8 KB (944844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ac085702ffdda597a0b0cd8a1d8a890d7be317e1ae9d80df00320ec263ccda`

```dockerfile
```

-	Layers:
	-	`sha256:ab6f2b1e7c2aaa25faf3c871425e0419810e6a848cf15112dd95d05367dc0af7`  
		Last Modified: Mon, 22 Jul 2024 23:05:37 GMT  
		Size: 914.1 KB (914097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0db21d24731eed915a390cb46f22fcd094da7250ff07e8b773a1668085beebb1`  
		Last Modified: Mon, 22 Jul 2024 23:05:36 GMT  
		Size: 30.7 KB (30747 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:4c902582ab94505dd9e4c352ee0aff3048da9db7547e1012bdb79f3fa5daed13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88698755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68b49009cd3aca0446c38075b0ee0a77c2d775f54a99db28c921b59798884940`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 11 Jul 2024 20:47:57 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["/bin/sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXDB_VERSION=2.7.7
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 11 Jul 2024 20:47:57 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["influxd"]
# Thu, 11 Jul 2024 20:47:57 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 11 Jul 2024 20:47:57 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8919d5c79f658c9457d7a0f263bed9aff06bd63364af32b6bd6d948e2ffe5d`  
		Last Modified: Tue, 23 Jul 2024 18:08:40 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1fb104d942a3d0f0121732315db070fa51fd2e6cd64f9f4e7f8072cf5badb3`  
		Last Modified: Tue, 23 Jul 2024 18:08:40 GMT  
		Size: 9.8 MB (9760309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41f50520b6dfcfbe83d195a3a6b16b10b60e5c4058bd26a4f4a18f635134277`  
		Last Modified: Tue, 23 Jul 2024 18:08:40 GMT  
		Size: 5.5 MB (5463802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d079f2db321015236eff90f84c90e021d8133b242abbf9d6b170909f089827f`  
		Last Modified: Tue, 23 Jul 2024 18:08:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef02808a1dee2f5fa0729f991cb391f0880fa7cddf154f9acf77e0599fc8d84`  
		Last Modified: Tue, 23 Jul 2024 18:08:42 GMT  
		Size: 47.7 MB (47717248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03105aa47dfaad2780af3be9e10241551f9e93c90595f0ef7ea18ce01b4703e`  
		Last Modified: Tue, 23 Jul 2024 18:08:42 GMT  
		Size: 21.7 MB (21662496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be554794a10b5f70328f1a09f4b4c1934a1824c5d80e5b348524a2cee587020e`  
		Last Modified: Tue, 23 Jul 2024 18:08:41 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a615ab1c18038858040618fb58198c60b6d71f5d33af5852e992cbe54c469506`  
		Last Modified: Tue, 23 Jul 2024 18:08:42 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f7c06ca922ee2c0aef4c608c7df590708a18a18310e6679da55a762aeb607d`  
		Last Modified: Tue, 23 Jul 2024 18:08:42 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:434b30874520707afca8b4fd88bb5d56d18635494cac2ba9a5b81e69fab7ba9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.4 KB (944405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab93af0394b7cd8ab1b9bd687293c5802b03776e8a474526a958dcb1c7d447f`

```dockerfile
```

-	Layers:
	-	`sha256:0655772b893afadcce60bc0e6b913cf136c9892a51cddcd6b2a3a095b89599ba`  
		Last Modified: Tue, 23 Jul 2024 18:08:40 GMT  
		Size: 913.4 KB (913358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:556806b8d211baa4e0da276bae3645005542ab1065e7a6efdacd52d6d235df80`  
		Last Modified: Tue, 23 Jul 2024 18:08:40 GMT  
		Size: 31.0 KB (31047 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7.8`

**does not exist** (yet?)

## `influxdb:2.7.8-alpine`

**does not exist** (yet?)

## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:c0eb6d9abd89dee9efc9f55e9ad81acb9db6db87e882667456a279ab7d61e25d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:980de6c467cf58935b54df248930259c47771cec6d3580e4c899fce364186f2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (92011663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c8369e23002583137c2fd7b5d9100ef3f597613b8d44a9652ad63b159df4309`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 11 Jul 2024 20:47:57 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["/bin/sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXDB_VERSION=2.7.7
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 11 Jul 2024 20:47:57 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["influxd"]
# Thu, 11 Jul 2024 20:47:57 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 11 Jul 2024 20:47:57 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0dc81762ab9cd4ef11ab0791cc1e4b892353c5ad16f3506e394ed6f4851e93`  
		Last Modified: Mon, 22 Jul 2024 23:05:36 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f18cef9a6cf8c8b1886e10d167cf6ab545b58cf2b96ccbfd151486bebdc7e6`  
		Last Modified: Mon, 22 Jul 2024 23:05:37 GMT  
		Size: 9.6 MB (9633256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c65a22e031fff63369e94994f8c1bf122ea9e4710a99745ba002d3668f2e53`  
		Last Modified: Mon, 22 Jul 2024 23:05:37 GMT  
		Size: 5.8 MB (5820927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0e14a2477df6c25c76b13f5009de5ceb13143a8cdae2647b3fda7d73cbe737`  
		Last Modified: Mon, 22 Jul 2024 23:05:36 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc70ac1afb69874bc1da494b05e87a8b12713f12f637f0e28838a57debc79be`  
		Last Modified: Mon, 22 Jul 2024 23:05:38 GMT  
		Size: 49.8 MB (49798314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff79ccb638859c2f93bc6b478d404485f0132770e580fd7c8d8a7fb8bfbe4b59`  
		Last Modified: Mon, 22 Jul 2024 23:05:38 GMT  
		Size: 23.1 MB (23128309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d98ec689fb5fab393c0e5c79138f617fa94d1c90e1ad0282abca6621c24675`  
		Last Modified: Mon, 22 Jul 2024 23:05:37 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1ea18c19e317393625c2c2939b3521fbc7ebba56bcb67cb68c068178955be7`  
		Last Modified: Mon, 22 Jul 2024 23:05:38 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7be8260682ef0a7adf8bd76b1950e012e93251862938923b508d7233a4dda1e`  
		Last Modified: Mon, 22 Jul 2024 23:05:38 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:b54de15363255b99d02d523b11514f1fe6f0e3a5f2bb67f22630ffa114929e5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.8 KB (944844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ac085702ffdda597a0b0cd8a1d8a890d7be317e1ae9d80df00320ec263ccda`

```dockerfile
```

-	Layers:
	-	`sha256:ab6f2b1e7c2aaa25faf3c871425e0419810e6a848cf15112dd95d05367dc0af7`  
		Last Modified: Mon, 22 Jul 2024 23:05:37 GMT  
		Size: 914.1 KB (914097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0db21d24731eed915a390cb46f22fcd094da7250ff07e8b773a1668085beebb1`  
		Last Modified: Mon, 22 Jul 2024 23:05:36 GMT  
		Size: 30.7 KB (30747 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:4c902582ab94505dd9e4c352ee0aff3048da9db7547e1012bdb79f3fa5daed13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88698755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68b49009cd3aca0446c38075b0ee0a77c2d775f54a99db28c921b59798884940`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 11 Jul 2024 20:47:57 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["/bin/sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXDB_VERSION=2.7.7
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 11 Jul 2024 20:47:57 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["influxd"]
# Thu, 11 Jul 2024 20:47:57 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 11 Jul 2024 20:47:57 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8919d5c79f658c9457d7a0f263bed9aff06bd63364af32b6bd6d948e2ffe5d`  
		Last Modified: Tue, 23 Jul 2024 18:08:40 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1fb104d942a3d0f0121732315db070fa51fd2e6cd64f9f4e7f8072cf5badb3`  
		Last Modified: Tue, 23 Jul 2024 18:08:40 GMT  
		Size: 9.8 MB (9760309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41f50520b6dfcfbe83d195a3a6b16b10b60e5c4058bd26a4f4a18f635134277`  
		Last Modified: Tue, 23 Jul 2024 18:08:40 GMT  
		Size: 5.5 MB (5463802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d079f2db321015236eff90f84c90e021d8133b242abbf9d6b170909f089827f`  
		Last Modified: Tue, 23 Jul 2024 18:08:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef02808a1dee2f5fa0729f991cb391f0880fa7cddf154f9acf77e0599fc8d84`  
		Last Modified: Tue, 23 Jul 2024 18:08:42 GMT  
		Size: 47.7 MB (47717248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03105aa47dfaad2780af3be9e10241551f9e93c90595f0ef7ea18ce01b4703e`  
		Last Modified: Tue, 23 Jul 2024 18:08:42 GMT  
		Size: 21.7 MB (21662496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be554794a10b5f70328f1a09f4b4c1934a1824c5d80e5b348524a2cee587020e`  
		Last Modified: Tue, 23 Jul 2024 18:08:41 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a615ab1c18038858040618fb58198c60b6d71f5d33af5852e992cbe54c469506`  
		Last Modified: Tue, 23 Jul 2024 18:08:42 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f7c06ca922ee2c0aef4c608c7df590708a18a18310e6679da55a762aeb607d`  
		Last Modified: Tue, 23 Jul 2024 18:08:42 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:434b30874520707afca8b4fd88bb5d56d18635494cac2ba9a5b81e69fab7ba9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.4 KB (944405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab93af0394b7cd8ab1b9bd687293c5802b03776e8a474526a958dcb1c7d447f`

```dockerfile
```

-	Layers:
	-	`sha256:0655772b893afadcce60bc0e6b913cf136c9892a51cddcd6b2a3a095b89599ba`  
		Last Modified: Tue, 23 Jul 2024 18:08:40 GMT  
		Size: 913.4 KB (913358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:556806b8d211baa4e0da276bae3645005542ab1065e7a6efdacd52d6d235df80`  
		Last Modified: Tue, 23 Jul 2024 18:08:40 GMT  
		Size: 31.0 KB (31047 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:latest`

```console
$ docker pull influxdb@sha256:3f52e727ad6f76202388d8461a4c92b883c169bd2409bcf2bcafd60ce448fc5c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:e5caa85f18216d92d27adb02fb91cfc6c98aac9ecd7355a80efcb558c63f6b19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168482883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f26019eadb9acbba9378124cb10170b621c3d3aaad1af8b1a32061ca755df0a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 11 Jul 2024 20:47:57 GMT
ADD file:6c4730e7b12278bc7eb83b3b9d659437c92c42fc7ee70922ae8c4bebfb56a602 in / 
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["bash"]
# Thu, 11 Jul 2024 20:47:57 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV GOSU_VER=1.16
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXDB_VERSION=2.7.7
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 11 Jul 2024 20:47:57 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["influxd"]
# Thu, 11 Jul 2024 20:47:57 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 11 Jul 2024 20:47:57 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:efc2b5ad9eec05befa54239d53feeae3569ccbef689aa5e5dbfc25da6c4df559`  
		Last Modified: Tue, 23 Jul 2024 05:27:55 GMT  
		Size: 29.1 MB (29126287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22338516b2c3a384ef121fc1be4117457521cc28b7e49f84d3844566393dcbf4`  
		Last Modified: Tue, 23 Jul 2024 07:14:41 GMT  
		Size: 9.8 MB (9786187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac58becbac91dc22721c4bddf5b16a010cc0ac8b78fa9da9c77ea6cbee97e3bb`  
		Last Modified: Tue, 23 Jul 2024 07:14:41 GMT  
		Size: 5.8 MB (5820938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e42e673a8ae1ab1d8fc5db3121984aefb2a875239f966f93bac06ca732cc7f8`  
		Last Modified: Tue, 23 Jul 2024 07:14:41 GMT  
		Size: 3.2 KB (3226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ff614d7de17822649a373bf73d773320b1bdb865318678d0b4ef4977131282`  
		Last Modified: Tue, 23 Jul 2024 07:14:41 GMT  
		Size: 1.0 MB (1006375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8208204cff517a7b65a51a644ab584848a3370c7daa173aaa3481505bf12268`  
		Last Modified: Tue, 23 Jul 2024 07:14:43 GMT  
		Size: 99.6 MB (99604818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1929499f66d1a530f2797991e2886b1ca096fec9bbfd53f9adbdbd8624a114f1`  
		Last Modified: Tue, 23 Jul 2024 07:14:43 GMT  
		Size: 23.1 MB (23128322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f23b9837bf2e93895fedd50a59f58d21b04b2bb1903c3a4501eb8f6163d432c6`  
		Last Modified: Tue, 23 Jul 2024 07:14:42 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6466f3f77518b31b3654cea74b2328d01a9180754eb9e646bfc989fcd2ad47f0`  
		Last Modified: Tue, 23 Jul 2024 07:14:42 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aca036d4f9771de5ef76573cad0e3b0d7b85b1ac31b1aa42337d40de8b2e78f`  
		Last Modified: Tue, 23 Jul 2024 07:14:43 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:43fdd95cc12ecd9c5fbd0ceaf2fbeb17e58b2578eca1fe0b5939c1e1327bae1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:373e0fe134451558207814192070ce829957f2f6d71acc5313e26ca71afff868`

```dockerfile
```

-	Layers:
	-	`sha256:f6be574d8c745480b11a730d530d10b703c55a6d75425cec12b60ea60d5e0343`  
		Last Modified: Tue, 23 Jul 2024 07:14:41 GMT  
		Size: 2.8 MB (2833446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92aa852aed4af10be99849b53ebf64f9f53e41a1ea4c26751666c5f6a06eccb5`  
		Last Modified: Tue, 23 Jul 2024 07:14:41 GMT  
		Size: 33.5 KB (33540 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:6fc30098c206be774ed40d58f7ba5f57fd474cdd8e9401a9ba53a58758cd9dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162257327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18af809fb3588e1c6bab1a68368a4e6aa3bd9c5425ea77648a6b597a45da748f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 11 Jul 2024 20:47:57 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["bash"]
# Thu, 11 Jul 2024 20:47:57 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV GOSU_VER=1.16
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXDB_VERSION=2.7.7
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 11 Jul 2024 20:47:57 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["influxd"]
# Thu, 11 Jul 2024 20:47:57 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 11 Jul 2024 20:47:57 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67594e2e4aadf6baf66ac584c9fb6d83c809848e40f81bb739a001042589ccc2`  
		Last Modified: Tue, 23 Jul 2024 18:08:05 GMT  
		Size: 9.6 MB (9585121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029fa3409050b4d29ab49826756ef0ba10eea4bb6529ad8d696e69716515cf9a`  
		Last Modified: Tue, 23 Jul 2024 18:08:05 GMT  
		Size: 5.5 MB (5463796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e760cb86365539321da91ea2ecbd850cf9b4c00c74d22ee6aba4b1a5d31058d2`  
		Last Modified: Tue, 23 Jul 2024 18:08:04 GMT  
		Size: 3.2 KB (3224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9ddc905ddf37e776b4366405135b9ba49d670dae38dd71845af8f056c6b9b7`  
		Last Modified: Tue, 23 Jul 2024 18:08:05 GMT  
		Size: 936.1 KB (936106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ebd1e919c87ac45543c29b0b3a82a730ea7a7d28b0142d4cd83abcf63f92a9`  
		Last Modified: Tue, 23 Jul 2024 18:08:08 GMT  
		Size: 95.4 MB (95443280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed46f9349ddb8ffe48f56000fbf392c27f0a068fdd9e12c7fc7ebe49de719044`  
		Last Modified: Tue, 23 Jul 2024 18:08:07 GMT  
		Size: 21.7 MB (21662499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfa519bf3b45b0205f6abd623aa279262232dd3f3dd1f6a2d56f87acc0bc5db`  
		Last Modified: Tue, 23 Jul 2024 18:08:06 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d970d0ab9823c6f2cba6ee08efa804f42a149ab5801e9ba9b2bce0ed39197fe`  
		Last Modified: Tue, 23 Jul 2024 18:08:06 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b0745af95af38669f2e7868f4a109fcfc276707caa607972e06a18aeecbf40`  
		Last Modified: Tue, 23 Jul 2024 18:08:07 GMT  
		Size: 6.3 KB (6288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:c339ec1048e488d9e89cb3ce0374efbf00c4bc26d98f780301ee2fbb19123d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c18b2ca8457af116f9e445ed2e3054f0c55cb3f5b938ea40da06189b29bf25d0`

```dockerfile
```

-	Layers:
	-	`sha256:76db0783b7f4f0d0f478abe282c1e0ccac878c7d3e6c3e9fc186acd5c31959f2`  
		Last Modified: Tue, 23 Jul 2024 18:08:05 GMT  
		Size: 2.8 MB (2832683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3916f78c10e8d9745c67fe9f4b4017de13148117da95eedbee5e64ba423c7040`  
		Last Modified: Tue, 23 Jul 2024 18:08:04 GMT  
		Size: 33.8 KB (33843 bytes)  
		MIME: application/vnd.in-toto+json
