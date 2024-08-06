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
-	[`influxdb:1.11.6-data`](#influxdb1116-data)
-	[`influxdb:1.11.6-data-alpine`](#influxdb1116-data-alpine)
-	[`influxdb:1.11.6-meta`](#influxdb1116-meta)
-	[`influxdb:1.11.6-meta-alpine`](#influxdb1116-meta-alpine)
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
$ docker pull influxdb@sha256:548dff40203b0904663cb4ca34c43f403e9d24dd87dbb97d63054c36be5bdb8a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data` - linux; amd64

```console
$ docker pull influxdb@sha256:301c16110fd22e567c81525b5e5286c93e17b5ccfe87129c418eac925803fbad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114732814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1459bbb952aad71719d436fe503b48290b11b5b38c604bc0a0e3288ce26e7be`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:03 GMT
ADD file:430cca9ad155514d8c818e860e66e2aeccfb6230874d4faf446a1d0c2fc1054f in / 
# Tue, 23 Jul 2024 05:24:03 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 06:06:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Aug 2024 15:57:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 06 Aug 2024 15:57:15 GMT
ENV INFLUXDB_VERSION=1.11.6-c1.11.6
# Tue, 06 Aug 2024 15:57:15 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Tue, 06 Aug 2024 15:57:15 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 06 Aug 2024 15:57:15 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 06 Aug 2024 15:57:15 GMT
VOLUME [/var/lib/influxdb]
# Tue, 06 Aug 2024 15:57:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 06 Aug 2024 15:57:15 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 06 Aug 2024 15:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Aug 2024 15:57:15 GMT
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
	-	`sha256:dbbadce9010a54cef87d16f217d36a4f82f107bca036ac130d4530aa11174bdc`  
		Last Modified: Tue, 06 Aug 2024 19:56:22 GMT  
		Size: 1.8 KB (1772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e976b793bb223917fe66e151c91a4b3b1b51cfcbbbdfd0860ae1897eae326de8`  
		Last Modified: Tue, 06 Aug 2024 19:56:23 GMT  
		Size: 41.1 MB (41124396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d445733563a597b446e6a7bcb67f1f826dff926c68443bdde2755b6c50fd5830`  
		Last Modified: Tue, 06 Aug 2024 19:56:22 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6677ea3b54e1a665cf5a9b58b211402e7391e8e81a9b6ea77ddb81388d727e43`  
		Last Modified: Tue, 06 Aug 2024 19:56:22 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153deee09bf5549a959defff37192e4c3bab1d317273ee46bad3d3493ac6fb30`  
		Last Modified: Tue, 06 Aug 2024 19:56:23 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:98d6271ba569a7ea020802deb4cafb47e849602a9035991655192a04796ee155
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4515829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02b41a40b9510efe2b0e90725ab6d7ccaa589a10677862df98b191cf7a3d0e95`

```dockerfile
```

-	Layers:
	-	`sha256:80d8e92561f450852eaadc0371606219e8412d7c864bdd94bcf9d54c3ab68837`  
		Last Modified: Tue, 06 Aug 2024 19:56:22 GMT  
		Size: 4.5 MB (4501255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83b01543d82e99c2fd977a3b26aa0aaddc871a186e7252888776b01f9099a7c0`  
		Last Modified: Tue, 06 Aug 2024 19:56:22 GMT  
		Size: 14.6 KB (14574 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-data-alpine`

```console
$ docker pull influxdb@sha256:bd5c6875b292348f2930d6943b29daac745b37136285c39e4529a8c338f24205
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:d6ee311dd86eedfb54844de21f7ea4b330f84d004530b2f371873da6ac3f4cb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45922020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48d3d5e06e6e2ca4a2c59f83368db402c260b83426a08a3357f23aeb3eecf802`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Tue, 06 Aug 2024 15:57:15 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 06 Aug 2024 15:57:15 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Tue, 06 Aug 2024 15:57:15 GMT
ENV INFLUXDB_VERSION=1.11.6-c1.11.6
# Tue, 06 Aug 2024 15:57:15 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Tue, 06 Aug 2024 15:57:15 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 06 Aug 2024 15:57:15 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 06 Aug 2024 15:57:15 GMT
VOLUME [/var/lib/influxdb]
# Tue, 06 Aug 2024 15:57:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 06 Aug 2024 15:57:15 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 06 Aug 2024 15:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Aug 2024 15:57:15 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beef28305f91f0b2d1f6d38895ae34a99a26d2dc5d6649f42ee743e3d96bef45`  
		Last Modified: Tue, 06 Aug 2024 19:56:26 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad377f34b9d71e2dfe77d43f336eb56fcaf45c934c2f0fa70103eb62a33b613`  
		Last Modified: Tue, 06 Aug 2024 19:56:27 GMT  
		Size: 1.2 MB (1229928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4dfa97192128724f265dc3381a270a194df468626660799eca2427be97aebf8`  
		Last Modified: Tue, 06 Aug 2024 19:56:28 GMT  
		Size: 41.1 MB (41067146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a77d6238d841848645ad266a2e8df60cfa079cf0ca8319d2862ca96e2a97a6a`  
		Last Modified: Tue, 06 Aug 2024 19:56:26 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e9f574fe92853117c47cd43166f17934ee9497a58f0c7a7d85192adda7c49d`  
		Last Modified: Tue, 06 Aug 2024 19:56:27 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c45228dcc96850b15bc7f65c9fead1286e1c138f33ede163e5c789a2095b9a1`  
		Last Modified: Tue, 06 Aug 2024 19:56:27 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:e9c715deba2e588cb0c6c68a9d169a75ddabf0e6eb3b39855423bf0f847151f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **769.0 KB (769008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75f869ba7771fe185d51a23de34ff32aa749ae86caf3e68ab8070b1a823d3048`

```dockerfile
```

-	Layers:
	-	`sha256:cfb7d3fdffa2197920ff1b07a1ab1dce73aa7f49900d6a7c90957884bcdc42f0`  
		Last Modified: Tue, 06 Aug 2024 19:56:26 GMT  
		Size: 752.6 KB (752584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:109fc02c424e0e8f848e52ac7eb43b51ce2c9e8dc6769d4563627157a34e54e8`  
		Last Modified: Tue, 06 Aug 2024 19:56:26 GMT  
		Size: 16.4 KB (16424 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-meta`

```console
$ docker pull influxdb@sha256:ead7c9e91ccf75b68ba739ce6d4df2ac289df348dbab7b5ce2a0af1af795fb3c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:f82985195e6cbc26516e8ae799b32eb5f4c85dbe2d5dc62668962d6a06068852
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93400182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:039e9294e9ecaedaedd198b7cf20c0b09302b8d18ba0187556bbb838ed2d6f32`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:03 GMT
ADD file:430cca9ad155514d8c818e860e66e2aeccfb6230874d4faf446a1d0c2fc1054f in / 
# Tue, 23 Jul 2024 05:24:03 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 06:06:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Aug 2024 15:57:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 06 Aug 2024 15:57:15 GMT
ENV INFLUXDB_VERSION=1.11.6-c1.11.6
# Tue, 06 Aug 2024 15:57:15 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Tue, 06 Aug 2024 15:57:15 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 06 Aug 2024 15:57:15 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 06 Aug 2024 15:57:15 GMT
VOLUME [/var/lib/influxdb]
# Tue, 06 Aug 2024 15:57:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 06 Aug 2024 15:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Aug 2024 15:57:15 GMT
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
	-	`sha256:9338eddceec6a41264a038496de5707c815c7f9af80148f655c6c880e2ca4312`  
		Last Modified: Tue, 06 Aug 2024 19:56:19 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e455dcb2dcf1dd47b134ecace6d695dc117b2c12845efd6a753d39e9edc69565`  
		Last Modified: Tue, 06 Aug 2024 19:56:20 GMT  
		Size: 19.8 MB (19792974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356ed78d4bf10e62795affd1302901c64f811f43822f61ea91cfb1311a2a1738`  
		Last Modified: Tue, 06 Aug 2024 19:56:20 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de9a886e2413207e7f41ded07d5e007c7f156ec2ac03f7c9f3be92e5f5f7197`  
		Last Modified: Tue, 06 Aug 2024 19:56:20 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:fe257b27e6867b87b39f5319c0e4673621faa3d502536f9670be36c34709d846
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4438928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef8329230f9db825cc1bba32a40172168b0e524060377bf576851a18a78937e`

```dockerfile
```

-	Layers:
	-	`sha256:2ef1093902f66706cd5486422fb731a9a590b8fa47e7884ab8647f50c44f6c07`  
		Last Modified: Tue, 06 Aug 2024 19:56:19 GMT  
		Size: 4.4 MB (4426007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15fc788160496891d0183089a680989e396a1a03a12a31c5c85e2906d80275a9`  
		Last Modified: Tue, 06 Aug 2024 19:56:19 GMT  
		Size: 12.9 KB (12921 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-meta-alpine`

```console
$ docker pull influxdb@sha256:d942988e95c48d8104b6beb4588cf23e1512d7e17eef37e08877d170e8ae9e0e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:b9f12d9d432e67cef6f5db79815c2ae1710ee417a3bf1f7b86864d060d55d187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24589293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:658e9c933488289bfbd28076d079eb1d4b8bff1b922128070045bcf95643a8a4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Tue, 06 Aug 2024 15:57:15 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 06 Aug 2024 15:57:15 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Tue, 06 Aug 2024 15:57:15 GMT
ENV INFLUXDB_VERSION=1.11.6-c1.11.6
# Tue, 06 Aug 2024 15:57:15 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Tue, 06 Aug 2024 15:57:15 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 06 Aug 2024 15:57:15 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 06 Aug 2024 15:57:15 GMT
VOLUME [/var/lib/influxdb]
# Tue, 06 Aug 2024 15:57:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 06 Aug 2024 15:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Aug 2024 15:57:15 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be56dad10b9cc3cc13e67a03ef0088c554ce99ba1b61cc7d69a854471d3380a4`  
		Last Modified: Tue, 06 Aug 2024 19:56:15 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e88ad6630520686a62ffa19b6fd12f9a4cea1e6cb02ca8bd4b0cb7a7511129`  
		Last Modified: Tue, 06 Aug 2024 19:56:15 GMT  
		Size: 1.2 MB (1229923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ce4d6e2c6e140485a8440bd065d46549261088b65a7c4857294426d80d4f00`  
		Last Modified: Tue, 06 Aug 2024 19:56:15 GMT  
		Size: 19.7 MB (19735630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b6e6bb0112ae34e939154f85db20041e69a790f20d6b2b9a3f101515720603`  
		Last Modified: Tue, 06 Aug 2024 19:56:15 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52e583db8f11924b02a4f79d41d725433b560281c3e81306dfd53c0f83116972`  
		Last Modified: Tue, 06 Aug 2024 19:56:16 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:732a8d91f74de14888f3a81c23a29c0bd523707f1704ea0213d9d3e55b0748a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **693.0 KB (693018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f4e9bf97aeb26a54a23049beed989f2c13580811953832198c49cecc924cb44`

```dockerfile
```

-	Layers:
	-	`sha256:159cad263f31660f2864d8b77a78cd92bf110f78fd9f62bb28a64f3143ecc3e8`  
		Last Modified: Tue, 06 Aug 2024 19:56:15 GMT  
		Size: 678.2 KB (678229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5de146fe4e5033fbc9ebe4d3c70880b0a2faa989808e4b0cbc39e71cce9c70c8`  
		Last Modified: Tue, 06 Aug 2024 19:56:15 GMT  
		Size: 14.8 KB (14789 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.6-data`

```console
$ docker pull influxdb@sha256:548dff40203b0904663cb4ca34c43f403e9d24dd87dbb97d63054c36be5bdb8a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.6-data` - linux; amd64

```console
$ docker pull influxdb@sha256:301c16110fd22e567c81525b5e5286c93e17b5ccfe87129c418eac925803fbad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114732814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1459bbb952aad71719d436fe503b48290b11b5b38c604bc0a0e3288ce26e7be`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:03 GMT
ADD file:430cca9ad155514d8c818e860e66e2aeccfb6230874d4faf446a1d0c2fc1054f in / 
# Tue, 23 Jul 2024 05:24:03 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 06:06:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Aug 2024 15:57:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 06 Aug 2024 15:57:15 GMT
ENV INFLUXDB_VERSION=1.11.6-c1.11.6
# Tue, 06 Aug 2024 15:57:15 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Tue, 06 Aug 2024 15:57:15 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 06 Aug 2024 15:57:15 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 06 Aug 2024 15:57:15 GMT
VOLUME [/var/lib/influxdb]
# Tue, 06 Aug 2024 15:57:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 06 Aug 2024 15:57:15 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 06 Aug 2024 15:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Aug 2024 15:57:15 GMT
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
	-	`sha256:dbbadce9010a54cef87d16f217d36a4f82f107bca036ac130d4530aa11174bdc`  
		Last Modified: Tue, 06 Aug 2024 19:56:22 GMT  
		Size: 1.8 KB (1772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e976b793bb223917fe66e151c91a4b3b1b51cfcbbbdfd0860ae1897eae326de8`  
		Last Modified: Tue, 06 Aug 2024 19:56:23 GMT  
		Size: 41.1 MB (41124396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d445733563a597b446e6a7bcb67f1f826dff926c68443bdde2755b6c50fd5830`  
		Last Modified: Tue, 06 Aug 2024 19:56:22 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6677ea3b54e1a665cf5a9b58b211402e7391e8e81a9b6ea77ddb81388d727e43`  
		Last Modified: Tue, 06 Aug 2024 19:56:22 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153deee09bf5549a959defff37192e4c3bab1d317273ee46bad3d3493ac6fb30`  
		Last Modified: Tue, 06 Aug 2024 19:56:23 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.6-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:98d6271ba569a7ea020802deb4cafb47e849602a9035991655192a04796ee155
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4515829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02b41a40b9510efe2b0e90725ab6d7ccaa589a10677862df98b191cf7a3d0e95`

```dockerfile
```

-	Layers:
	-	`sha256:80d8e92561f450852eaadc0371606219e8412d7c864bdd94bcf9d54c3ab68837`  
		Last Modified: Tue, 06 Aug 2024 19:56:22 GMT  
		Size: 4.5 MB (4501255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83b01543d82e99c2fd977a3b26aa0aaddc871a186e7252888776b01f9099a7c0`  
		Last Modified: Tue, 06 Aug 2024 19:56:22 GMT  
		Size: 14.6 KB (14574 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.6-data-alpine`

```console
$ docker pull influxdb@sha256:bd5c6875b292348f2930d6943b29daac745b37136285c39e4529a8c338f24205
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.6-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:d6ee311dd86eedfb54844de21f7ea4b330f84d004530b2f371873da6ac3f4cb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45922020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48d3d5e06e6e2ca4a2c59f83368db402c260b83426a08a3357f23aeb3eecf802`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Tue, 06 Aug 2024 15:57:15 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 06 Aug 2024 15:57:15 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Tue, 06 Aug 2024 15:57:15 GMT
ENV INFLUXDB_VERSION=1.11.6-c1.11.6
# Tue, 06 Aug 2024 15:57:15 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Tue, 06 Aug 2024 15:57:15 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 06 Aug 2024 15:57:15 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 06 Aug 2024 15:57:15 GMT
VOLUME [/var/lib/influxdb]
# Tue, 06 Aug 2024 15:57:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 06 Aug 2024 15:57:15 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 06 Aug 2024 15:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Aug 2024 15:57:15 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beef28305f91f0b2d1f6d38895ae34a99a26d2dc5d6649f42ee743e3d96bef45`  
		Last Modified: Tue, 06 Aug 2024 19:56:26 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad377f34b9d71e2dfe77d43f336eb56fcaf45c934c2f0fa70103eb62a33b613`  
		Last Modified: Tue, 06 Aug 2024 19:56:27 GMT  
		Size: 1.2 MB (1229928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4dfa97192128724f265dc3381a270a194df468626660799eca2427be97aebf8`  
		Last Modified: Tue, 06 Aug 2024 19:56:28 GMT  
		Size: 41.1 MB (41067146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a77d6238d841848645ad266a2e8df60cfa079cf0ca8319d2862ca96e2a97a6a`  
		Last Modified: Tue, 06 Aug 2024 19:56:26 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e9f574fe92853117c47cd43166f17934ee9497a58f0c7a7d85192adda7c49d`  
		Last Modified: Tue, 06 Aug 2024 19:56:27 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c45228dcc96850b15bc7f65c9fead1286e1c138f33ede163e5c789a2095b9a1`  
		Last Modified: Tue, 06 Aug 2024 19:56:27 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.6-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:e9c715deba2e588cb0c6c68a9d169a75ddabf0e6eb3b39855423bf0f847151f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **769.0 KB (769008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75f869ba7771fe185d51a23de34ff32aa749ae86caf3e68ab8070b1a823d3048`

```dockerfile
```

-	Layers:
	-	`sha256:cfb7d3fdffa2197920ff1b07a1ab1dce73aa7f49900d6a7c90957884bcdc42f0`  
		Last Modified: Tue, 06 Aug 2024 19:56:26 GMT  
		Size: 752.6 KB (752584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:109fc02c424e0e8f848e52ac7eb43b51ce2c9e8dc6769d4563627157a34e54e8`  
		Last Modified: Tue, 06 Aug 2024 19:56:26 GMT  
		Size: 16.4 KB (16424 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.6-meta`

```console
$ docker pull influxdb@sha256:ead7c9e91ccf75b68ba739ce6d4df2ac289df348dbab7b5ce2a0af1af795fb3c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.6-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:f82985195e6cbc26516e8ae799b32eb5f4c85dbe2d5dc62668962d6a06068852
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93400182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:039e9294e9ecaedaedd198b7cf20c0b09302b8d18ba0187556bbb838ed2d6f32`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:03 GMT
ADD file:430cca9ad155514d8c818e860e66e2aeccfb6230874d4faf446a1d0c2fc1054f in / 
# Tue, 23 Jul 2024 05:24:03 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 06:06:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Aug 2024 15:57:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 06 Aug 2024 15:57:15 GMT
ENV INFLUXDB_VERSION=1.11.6-c1.11.6
# Tue, 06 Aug 2024 15:57:15 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Tue, 06 Aug 2024 15:57:15 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 06 Aug 2024 15:57:15 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 06 Aug 2024 15:57:15 GMT
VOLUME [/var/lib/influxdb]
# Tue, 06 Aug 2024 15:57:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 06 Aug 2024 15:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Aug 2024 15:57:15 GMT
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
	-	`sha256:9338eddceec6a41264a038496de5707c815c7f9af80148f655c6c880e2ca4312`  
		Last Modified: Tue, 06 Aug 2024 19:56:19 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e455dcb2dcf1dd47b134ecace6d695dc117b2c12845efd6a753d39e9edc69565`  
		Last Modified: Tue, 06 Aug 2024 19:56:20 GMT  
		Size: 19.8 MB (19792974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356ed78d4bf10e62795affd1302901c64f811f43822f61ea91cfb1311a2a1738`  
		Last Modified: Tue, 06 Aug 2024 19:56:20 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de9a886e2413207e7f41ded07d5e007c7f156ec2ac03f7c9f3be92e5f5f7197`  
		Last Modified: Tue, 06 Aug 2024 19:56:20 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.6-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:fe257b27e6867b87b39f5319c0e4673621faa3d502536f9670be36c34709d846
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4438928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef8329230f9db825cc1bba32a40172168b0e524060377bf576851a18a78937e`

```dockerfile
```

-	Layers:
	-	`sha256:2ef1093902f66706cd5486422fb731a9a590b8fa47e7884ab8647f50c44f6c07`  
		Last Modified: Tue, 06 Aug 2024 19:56:19 GMT  
		Size: 4.4 MB (4426007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15fc788160496891d0183089a680989e396a1a03a12a31c5c85e2906d80275a9`  
		Last Modified: Tue, 06 Aug 2024 19:56:19 GMT  
		Size: 12.9 KB (12921 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.6-meta-alpine`

```console
$ docker pull influxdb@sha256:d942988e95c48d8104b6beb4588cf23e1512d7e17eef37e08877d170e8ae9e0e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.6-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:b9f12d9d432e67cef6f5db79815c2ae1710ee417a3bf1f7b86864d060d55d187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24589293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:658e9c933488289bfbd28076d079eb1d4b8bff1b922128070045bcf95643a8a4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Tue, 06 Aug 2024 15:57:15 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 06 Aug 2024 15:57:15 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Tue, 06 Aug 2024 15:57:15 GMT
ENV INFLUXDB_VERSION=1.11.6-c1.11.6
# Tue, 06 Aug 2024 15:57:15 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Tue, 06 Aug 2024 15:57:15 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 06 Aug 2024 15:57:15 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 06 Aug 2024 15:57:15 GMT
VOLUME [/var/lib/influxdb]
# Tue, 06 Aug 2024 15:57:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 06 Aug 2024 15:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Aug 2024 15:57:15 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be56dad10b9cc3cc13e67a03ef0088c554ce99ba1b61cc7d69a854471d3380a4`  
		Last Modified: Tue, 06 Aug 2024 19:56:15 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e88ad6630520686a62ffa19b6fd12f9a4cea1e6cb02ca8bd4b0cb7a7511129`  
		Last Modified: Tue, 06 Aug 2024 19:56:15 GMT  
		Size: 1.2 MB (1229923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ce4d6e2c6e140485a8440bd065d46549261088b65a7c4857294426d80d4f00`  
		Last Modified: Tue, 06 Aug 2024 19:56:15 GMT  
		Size: 19.7 MB (19735630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b6e6bb0112ae34e939154f85db20041e69a790f20d6b2b9a3f101515720603`  
		Last Modified: Tue, 06 Aug 2024 19:56:15 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52e583db8f11924b02a4f79d41d725433b560281c3e81306dfd53c0f83116972`  
		Last Modified: Tue, 06 Aug 2024 19:56:16 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.6-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:732a8d91f74de14888f3a81c23a29c0bd523707f1704ea0213d9d3e55b0748a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **693.0 KB (693018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f4e9bf97aeb26a54a23049beed989f2c13580811953832198c49cecc924cb44`

```dockerfile
```

-	Layers:
	-	`sha256:159cad263f31660f2864d8b77a78cd92bf110f78fd9f62bb28a64f3143ecc3e8`  
		Last Modified: Tue, 06 Aug 2024 19:56:15 GMT  
		Size: 678.2 KB (678229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5de146fe4e5033fbc9ebe4d3c70880b0a2faa989808e4b0cbc39e71cce9c70c8`  
		Last Modified: Tue, 06 Aug 2024 19:56:15 GMT  
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
$ docker pull influxdb@sha256:817a43e512687edbcfe0605df571d5e53b11f8b7ca7a6b317e69f763dc9be070
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2` - linux; amd64

```console
$ docker pull influxdb@sha256:cf8c92784dc721e6310ada35067f9d5893bbc9b99e8052237dcbe262b2f8f393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.1 MB (169052639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5b5658780163fd49de58a05c85391fd350be4292c3e9a7b90e6be6303fae0e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:15 GMT
ADD file:6c4730e7b12278bc7eb83b3b9d659437c92c42fc7ee70922ae8c4bebfb56a602 in / 
# Tue, 23 Jul 2024 05:24:16 GMT
CMD ["bash"]
# Thu, 25 Jul 2024 20:42:37 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENV GOSU_VER=1.16
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXDB_VERSION=2.7.8
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 25 Jul 2024 20:42:37 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Jul 2024 20:42:37 GMT
CMD ["influxd"]
# Thu, 25 Jul 2024 20:42:37 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 25 Jul 2024 20:42:37 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:efc2b5ad9eec05befa54239d53feeae3569ccbef689aa5e5dbfc25da6c4df559`  
		Last Modified: Tue, 23 Jul 2024 05:27:55 GMT  
		Size: 29.1 MB (29126287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aafe8e30583ab32a1e9ee7e2646e9683801bd17e63d70bb3bb3f4297db8baec`  
		Last Modified: Thu, 25 Jul 2024 22:00:46 GMT  
		Size: 9.8 MB (9786114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb3e64af86929ccda214e59bfcd54380f99fbd2cfbf05983e15896756066a27`  
		Last Modified: Thu, 25 Jul 2024 22:00:46 GMT  
		Size: 5.8 MB (5820922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b71a5ef49de7ee06787b83119ef3bcb1e81622e6be5f57a39b2c898690a0d2f`  
		Last Modified: Thu, 25 Jul 2024 22:00:46 GMT  
		Size: 3.2 KB (3229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0160b7176ca064e8395e1b99248ceed4ae5e3af57b7c152b522e9e64e53619`  
		Last Modified: Thu, 25 Jul 2024 22:00:46 GMT  
		Size: 1.0 MB (1006371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524d48b867737d10ef449f819f7fa36ea92a5ec7448b52063d4110e326cac34b`  
		Last Modified: Thu, 25 Jul 2024 22:00:48 GMT  
		Size: 100.2 MB (100174652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31cbe0a3f25d229f895dc1d474144dcc31c90a8e239848c874184752383e751`  
		Last Modified: Thu, 25 Jul 2024 22:00:47 GMT  
		Size: 23.1 MB (23128334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8597d281e9c9cb18a861eb227d9f3fa67b5cfa74b1bbbf16f951c694f37ae4b8`  
		Last Modified: Thu, 25 Jul 2024 22:00:47 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bcfb407f38709994863cbc982f8f47e428ed743239fa858736d02334bbd5a6f`  
		Last Modified: Thu, 25 Jul 2024 22:00:47 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634cb105b59a74b80dcdb92049a091cf008cb2fea675da232f5ac1f2d93d9df0`  
		Last Modified: Thu, 25 Jul 2024 22:00:48 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:9fb4a6136fa974e51994e3422345aaaef66b65ec3cb32779092981f6ecbcb32e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6139fd1cc0146a76decf6a803f95c12ac50149ef22d4c77500baba8b9f02c572`

```dockerfile
```

-	Layers:
	-	`sha256:c4fa52ea5261538daf2912b038fa96eadce9ce9198409ba8938af04c2b68cdcf`  
		Last Modified: Thu, 25 Jul 2024 22:00:46 GMT  
		Size: 2.8 MB (2833446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53b7394c3923f72225c4d186b8b3c829f52d3bc04899c3afa693b35d62339a6d`  
		Last Modified: Thu, 25 Jul 2024 22:00:46 GMT  
		Size: 33.5 KB (33544 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:ad1b67786fdafa8a6c928afde9514e9e61aa9196ba48ea0f85b02d46de88d4c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.8 MB (162819854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17b90fc212a2e15b03dfea6f55bba7e6841e9e68345b5de78ecae786f6715ee4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:51 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Tue, 23 Jul 2024 04:17:52 GMT
CMD ["bash"]
# Thu, 25 Jul 2024 20:42:37 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENV GOSU_VER=1.16
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXDB_VERSION=2.7.8
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 25 Jul 2024 20:42:37 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Jul 2024 20:42:37 GMT
CMD ["influxd"]
# Thu, 25 Jul 2024 20:42:37 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 25 Jul 2024 20:42:37 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570d86bee5eb6e09d1e4ecabe00877506dfef15eb8c1d0fb37fd03689650e726`  
		Last Modified: Fri, 26 Jul 2024 00:20:36 GMT  
		Size: 9.6 MB (9585146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8102b54b2061157b520e8d0c54ab9debfd7caeecf5b04ee4ff14f2a58c7ae5df`  
		Last Modified: Fri, 26 Jul 2024 00:20:36 GMT  
		Size: 5.5 MB (5463802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929f8e0bdc48c34a35a494a9768a1b505a86513c4cee278321f7df04a94698c2`  
		Last Modified: Fri, 26 Jul 2024 00:20:35 GMT  
		Size: 3.2 KB (3230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c078ee5f7362fbfa31e25a1b4c0fd0631479e57f820dfffe3d06fb939194699f`  
		Last Modified: Fri, 26 Jul 2024 00:20:36 GMT  
		Size: 936.1 KB (936109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0dd648633f64d4e39c97d3ef2a1d2784576fdbf65f90a11200b251c3b94c315`  
		Last Modified: Fri, 26 Jul 2024 00:20:39 GMT  
		Size: 96.0 MB (96005753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603c87bd567840dca04aa427260c8a8aef651d2c7dc55c70764e63200994ee71`  
		Last Modified: Fri, 26 Jul 2024 00:20:38 GMT  
		Size: 21.7 MB (21662517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7164f83c3085ab88b97f6aaecb51faaabcffcd70da9232e2a3982b9f6188905`  
		Last Modified: Fri, 26 Jul 2024 00:20:37 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132469a32a34a142198cc86019e6873278d6c8d25d43211ce10fff9327b6eb5c`  
		Last Modified: Fri, 26 Jul 2024 00:20:37 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8bee1e60c9fce079bf33dec8d4aa96459f86b491cb40d9a012fdf6c7eaf6663`  
		Last Modified: Fri, 26 Jul 2024 00:20:38 GMT  
		Size: 6.3 KB (6283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:e3c42143d1c2133c4178ab80b70d5a71beec793914426d9fba59eee164af843b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:894b26438d5a95eac85d03b568c647befed1805d6e9bf36fc3d6de8daecadb05`

```dockerfile
```

-	Layers:
	-	`sha256:83a2c2603d57f30d2d08d326b754c1e47956a0c97cf0f068b975475b846e4c5d`  
		Last Modified: Fri, 26 Jul 2024 00:20:36 GMT  
		Size: 2.8 MB (2832683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7db705f4da94aa74a70c426336d619b60b6abc61281b289133bd61d6273ce20d`  
		Last Modified: Fri, 26 Jul 2024 00:20:35 GMT  
		Size: 33.8 KB (33843 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2-alpine`

```console
$ docker pull influxdb@sha256:aa7c7967db6299829f225c931edbe2e53cb74bc32d8a8689eb10a71ec0cc4f9a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:9df149c10d324879963a5a690c3b3ba71bdea5208d5cb595d5aa083314438e92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92302723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:197b9f7cf87e0c89204d30b0327432a13a7d21e94eaaebad1208953a34be32b0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Thu, 25 Jul 2024 20:42:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXDB_VERSION=2.7.8
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 25 Jul 2024 20:42:37 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Jul 2024 20:42:37 GMT
CMD ["influxd"]
# Thu, 25 Jul 2024 20:42:37 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 25 Jul 2024 20:42:37 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d45a0a4871208edeaf34244b70f2d47191b76f2b4997648bacee65f0bb9b50f`  
		Last Modified: Thu, 25 Jul 2024 22:00:48 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee199347147ba36a9ac1c8db22d05c1c0b79ce7413994e38d8195544577dbca`  
		Last Modified: Thu, 25 Jul 2024 22:00:48 GMT  
		Size: 9.6 MB (9640728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa969dbbaaa21fef569a8823d550f3eb33e6b24d275e9c20b68b15cf0c605015`  
		Last Modified: Thu, 25 Jul 2024 22:00:48 GMT  
		Size: 5.8 MB (5820951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8142b4768fda9be2ced3e3eca82355fe675152715254e0baecfbbe1d80f5236`  
		Last Modified: Thu, 25 Jul 2024 22:00:48 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:380d583d17bced46b979236bdba753d5f94fa5a1fcadce3e45283a7d08918db2`  
		Last Modified: Thu, 25 Jul 2024 22:00:49 GMT  
		Size: 50.1 MB (50081865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff5e1ae40d1867d5fe7a6e65a7cc6488a475e6f73a97b2a4da6f8578ad3c21c`  
		Last Modified: Thu, 25 Jul 2024 22:00:49 GMT  
		Size: 23.1 MB (23128318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c693aab95480f71f592cc525cc940a6432037406963ee4ac5ad6035bd262167a`  
		Last Modified: Thu, 25 Jul 2024 22:00:49 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a68978ad7a69b0b85802e8367847c0ece31edd4e193283c0c40774fdbe43001`  
		Last Modified: Thu, 25 Jul 2024 22:00:49 GMT  
		Size: 235.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d385c3278fe6011ecc879151ad7f9bc7ba4a811b3c443d3b80afd979ee26eee`  
		Last Modified: Thu, 25 Jul 2024 22:00:49 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:097e3065499d4cc13248203886f2943f82a6e3a0ab2ab07cf9378e18831f7e5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.8 KB (944843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ab074677763b44aaf3b7d3bcacc8bd61e7fdb67dfab0e15c66f6ffa9c557a2e`

```dockerfile
```

-	Layers:
	-	`sha256:0a9cbd4c122519853b11796e1db3443af625b2b65b4199f595f63057b1cd5175`  
		Last Modified: Thu, 25 Jul 2024 22:00:48 GMT  
		Size: 914.1 KB (914097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49ecdfd8c6d37eac63328f874fbb9ad15ce00adce6366792a1af4c8fc13ade0a`  
		Last Modified: Thu, 25 Jul 2024 22:00:48 GMT  
		Size: 30.7 KB (30746 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:38069e07791802e3ae859b88d3ed24ae39bd47c0c262fadcaa5a19b6cc695307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.0 MB (88982239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:170537657cff123e5c869bab2bb7ea295cdc9d87b7ed152fa3a22dfc1fc381a0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Thu, 25 Jul 2024 20:42:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXDB_VERSION=2.7.8
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 25 Jul 2024 20:42:37 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Jul 2024 20:42:37 GMT
CMD ["influxd"]
# Thu, 25 Jul 2024 20:42:37 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 25 Jul 2024 20:42:37 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1de5eaf2a1972853375a025a0309628552446763159c73f9fb971eedad7e97c`  
		Last Modified: Fri, 26 Jul 2024 00:21:08 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b42d817c706fa63528ebb9df4f22670ee67a5c112ac51b215bd8678ac9d67ad`  
		Last Modified: Fri, 26 Jul 2024 00:21:09 GMT  
		Size: 9.8 MB (9763425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62906ecb281c2a5bc707f62ab2b4c4d4b2a03aa7f72fa2a50690041ee145d0a6`  
		Last Modified: Fri, 26 Jul 2024 00:21:09 GMT  
		Size: 5.5 MB (5463800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b061f6bfbb64e47b965b683ae90ab51edf297759c77aaed222b5fe725bcbf12c`  
		Last Modified: Fri, 26 Jul 2024 00:21:08 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ddf646868bea20fb9c33985e55a3399b91f7542506e04b9dbf75d1f577751c`  
		Last Modified: Fri, 26 Jul 2024 00:21:11 GMT  
		Size: 48.0 MB (47997597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c4e2b2b9f546f5ee7181d8d42ca929bc02f55aa86d66ceb9ad510107149aa0`  
		Last Modified: Fri, 26 Jul 2024 00:21:10 GMT  
		Size: 21.7 MB (21662516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cdf7866d6e2a92bb62169de5a27f2d1e5ff074c3fa58197a2a8b0c3f5e3795a`  
		Last Modified: Fri, 26 Jul 2024 00:21:10 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e860d28620195865eda75ca3b59e127cdfc148e6f2f569d8bed47d4f0d03d1`  
		Last Modified: Fri, 26 Jul 2024 00:21:10 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9275442b1367a934d6ac0672ae7677e98ccf3c367a779f1bc30d26421ee6bbfc`  
		Last Modified: Fri, 26 Jul 2024 00:21:11 GMT  
		Size: 6.3 KB (6283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:ef8e5056db345477948ce7481141622023935805a47ae0134cbf533b0e803dc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.4 KB (944404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2454014d973cf1c51ebd53b433151b51881c4affe5d5939ce894b2d0cd644705`

```dockerfile
```

-	Layers:
	-	`sha256:e3a5515ff59a3c4f7db137d7f91ed80d45620c9b4aca52f8dba2028f051a7610`  
		Last Modified: Fri, 26 Jul 2024 00:21:09 GMT  
		Size: 913.4 KB (913358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5480a638871ea5968968e63a134f3227aff5394e81061cfdad6ca533566a75aa`  
		Last Modified: Fri, 26 Jul 2024 00:21:08 GMT  
		Size: 31.0 KB (31046 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7`

```console
$ docker pull influxdb@sha256:817a43e512687edbcfe0605df571d5e53b11f8b7ca7a6b317e69f763dc9be070
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7` - linux; amd64

```console
$ docker pull influxdb@sha256:cf8c92784dc721e6310ada35067f9d5893bbc9b99e8052237dcbe262b2f8f393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.1 MB (169052639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5b5658780163fd49de58a05c85391fd350be4292c3e9a7b90e6be6303fae0e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:15 GMT
ADD file:6c4730e7b12278bc7eb83b3b9d659437c92c42fc7ee70922ae8c4bebfb56a602 in / 
# Tue, 23 Jul 2024 05:24:16 GMT
CMD ["bash"]
# Thu, 25 Jul 2024 20:42:37 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENV GOSU_VER=1.16
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXDB_VERSION=2.7.8
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 25 Jul 2024 20:42:37 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Jul 2024 20:42:37 GMT
CMD ["influxd"]
# Thu, 25 Jul 2024 20:42:37 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 25 Jul 2024 20:42:37 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:efc2b5ad9eec05befa54239d53feeae3569ccbef689aa5e5dbfc25da6c4df559`  
		Last Modified: Tue, 23 Jul 2024 05:27:55 GMT  
		Size: 29.1 MB (29126287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aafe8e30583ab32a1e9ee7e2646e9683801bd17e63d70bb3bb3f4297db8baec`  
		Last Modified: Thu, 25 Jul 2024 22:00:46 GMT  
		Size: 9.8 MB (9786114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb3e64af86929ccda214e59bfcd54380f99fbd2cfbf05983e15896756066a27`  
		Last Modified: Thu, 25 Jul 2024 22:00:46 GMT  
		Size: 5.8 MB (5820922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b71a5ef49de7ee06787b83119ef3bcb1e81622e6be5f57a39b2c898690a0d2f`  
		Last Modified: Thu, 25 Jul 2024 22:00:46 GMT  
		Size: 3.2 KB (3229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0160b7176ca064e8395e1b99248ceed4ae5e3af57b7c152b522e9e64e53619`  
		Last Modified: Thu, 25 Jul 2024 22:00:46 GMT  
		Size: 1.0 MB (1006371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524d48b867737d10ef449f819f7fa36ea92a5ec7448b52063d4110e326cac34b`  
		Last Modified: Thu, 25 Jul 2024 22:00:48 GMT  
		Size: 100.2 MB (100174652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31cbe0a3f25d229f895dc1d474144dcc31c90a8e239848c874184752383e751`  
		Last Modified: Thu, 25 Jul 2024 22:00:47 GMT  
		Size: 23.1 MB (23128334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8597d281e9c9cb18a861eb227d9f3fa67b5cfa74b1bbbf16f951c694f37ae4b8`  
		Last Modified: Thu, 25 Jul 2024 22:00:47 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bcfb407f38709994863cbc982f8f47e428ed743239fa858736d02334bbd5a6f`  
		Last Modified: Thu, 25 Jul 2024 22:00:47 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634cb105b59a74b80dcdb92049a091cf008cb2fea675da232f5ac1f2d93d9df0`  
		Last Modified: Thu, 25 Jul 2024 22:00:48 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:9fb4a6136fa974e51994e3422345aaaef66b65ec3cb32779092981f6ecbcb32e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6139fd1cc0146a76decf6a803f95c12ac50149ef22d4c77500baba8b9f02c572`

```dockerfile
```

-	Layers:
	-	`sha256:c4fa52ea5261538daf2912b038fa96eadce9ce9198409ba8938af04c2b68cdcf`  
		Last Modified: Thu, 25 Jul 2024 22:00:46 GMT  
		Size: 2.8 MB (2833446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53b7394c3923f72225c4d186b8b3c829f52d3bc04899c3afa693b35d62339a6d`  
		Last Modified: Thu, 25 Jul 2024 22:00:46 GMT  
		Size: 33.5 KB (33544 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:ad1b67786fdafa8a6c928afde9514e9e61aa9196ba48ea0f85b02d46de88d4c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.8 MB (162819854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17b90fc212a2e15b03dfea6f55bba7e6841e9e68345b5de78ecae786f6715ee4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:51 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Tue, 23 Jul 2024 04:17:52 GMT
CMD ["bash"]
# Thu, 25 Jul 2024 20:42:37 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENV GOSU_VER=1.16
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXDB_VERSION=2.7.8
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 25 Jul 2024 20:42:37 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Jul 2024 20:42:37 GMT
CMD ["influxd"]
# Thu, 25 Jul 2024 20:42:37 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 25 Jul 2024 20:42:37 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570d86bee5eb6e09d1e4ecabe00877506dfef15eb8c1d0fb37fd03689650e726`  
		Last Modified: Fri, 26 Jul 2024 00:20:36 GMT  
		Size: 9.6 MB (9585146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8102b54b2061157b520e8d0c54ab9debfd7caeecf5b04ee4ff14f2a58c7ae5df`  
		Last Modified: Fri, 26 Jul 2024 00:20:36 GMT  
		Size: 5.5 MB (5463802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929f8e0bdc48c34a35a494a9768a1b505a86513c4cee278321f7df04a94698c2`  
		Last Modified: Fri, 26 Jul 2024 00:20:35 GMT  
		Size: 3.2 KB (3230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c078ee5f7362fbfa31e25a1b4c0fd0631479e57f820dfffe3d06fb939194699f`  
		Last Modified: Fri, 26 Jul 2024 00:20:36 GMT  
		Size: 936.1 KB (936109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0dd648633f64d4e39c97d3ef2a1d2784576fdbf65f90a11200b251c3b94c315`  
		Last Modified: Fri, 26 Jul 2024 00:20:39 GMT  
		Size: 96.0 MB (96005753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603c87bd567840dca04aa427260c8a8aef651d2c7dc55c70764e63200994ee71`  
		Last Modified: Fri, 26 Jul 2024 00:20:38 GMT  
		Size: 21.7 MB (21662517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7164f83c3085ab88b97f6aaecb51faaabcffcd70da9232e2a3982b9f6188905`  
		Last Modified: Fri, 26 Jul 2024 00:20:37 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132469a32a34a142198cc86019e6873278d6c8d25d43211ce10fff9327b6eb5c`  
		Last Modified: Fri, 26 Jul 2024 00:20:37 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8bee1e60c9fce079bf33dec8d4aa96459f86b491cb40d9a012fdf6c7eaf6663`  
		Last Modified: Fri, 26 Jul 2024 00:20:38 GMT  
		Size: 6.3 KB (6283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:e3c42143d1c2133c4178ab80b70d5a71beec793914426d9fba59eee164af843b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:894b26438d5a95eac85d03b568c647befed1805d6e9bf36fc3d6de8daecadb05`

```dockerfile
```

-	Layers:
	-	`sha256:83a2c2603d57f30d2d08d326b754c1e47956a0c97cf0f068b975475b846e4c5d`  
		Last Modified: Fri, 26 Jul 2024 00:20:36 GMT  
		Size: 2.8 MB (2832683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7db705f4da94aa74a70c426336d619b60b6abc61281b289133bd61d6273ce20d`  
		Last Modified: Fri, 26 Jul 2024 00:20:35 GMT  
		Size: 33.8 KB (33843 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7-alpine`

```console
$ docker pull influxdb@sha256:aa7c7967db6299829f225c931edbe2e53cb74bc32d8a8689eb10a71ec0cc4f9a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:9df149c10d324879963a5a690c3b3ba71bdea5208d5cb595d5aa083314438e92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92302723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:197b9f7cf87e0c89204d30b0327432a13a7d21e94eaaebad1208953a34be32b0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Thu, 25 Jul 2024 20:42:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXDB_VERSION=2.7.8
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 25 Jul 2024 20:42:37 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Jul 2024 20:42:37 GMT
CMD ["influxd"]
# Thu, 25 Jul 2024 20:42:37 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 25 Jul 2024 20:42:37 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d45a0a4871208edeaf34244b70f2d47191b76f2b4997648bacee65f0bb9b50f`  
		Last Modified: Thu, 25 Jul 2024 22:00:48 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee199347147ba36a9ac1c8db22d05c1c0b79ce7413994e38d8195544577dbca`  
		Last Modified: Thu, 25 Jul 2024 22:00:48 GMT  
		Size: 9.6 MB (9640728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa969dbbaaa21fef569a8823d550f3eb33e6b24d275e9c20b68b15cf0c605015`  
		Last Modified: Thu, 25 Jul 2024 22:00:48 GMT  
		Size: 5.8 MB (5820951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8142b4768fda9be2ced3e3eca82355fe675152715254e0baecfbbe1d80f5236`  
		Last Modified: Thu, 25 Jul 2024 22:00:48 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:380d583d17bced46b979236bdba753d5f94fa5a1fcadce3e45283a7d08918db2`  
		Last Modified: Thu, 25 Jul 2024 22:00:49 GMT  
		Size: 50.1 MB (50081865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff5e1ae40d1867d5fe7a6e65a7cc6488a475e6f73a97b2a4da6f8578ad3c21c`  
		Last Modified: Thu, 25 Jul 2024 22:00:49 GMT  
		Size: 23.1 MB (23128318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c693aab95480f71f592cc525cc940a6432037406963ee4ac5ad6035bd262167a`  
		Last Modified: Thu, 25 Jul 2024 22:00:49 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a68978ad7a69b0b85802e8367847c0ece31edd4e193283c0c40774fdbe43001`  
		Last Modified: Thu, 25 Jul 2024 22:00:49 GMT  
		Size: 235.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d385c3278fe6011ecc879151ad7f9bc7ba4a811b3c443d3b80afd979ee26eee`  
		Last Modified: Thu, 25 Jul 2024 22:00:49 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:097e3065499d4cc13248203886f2943f82a6e3a0ab2ab07cf9378e18831f7e5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.8 KB (944843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ab074677763b44aaf3b7d3bcacc8bd61e7fdb67dfab0e15c66f6ffa9c557a2e`

```dockerfile
```

-	Layers:
	-	`sha256:0a9cbd4c122519853b11796e1db3443af625b2b65b4199f595f63057b1cd5175`  
		Last Modified: Thu, 25 Jul 2024 22:00:48 GMT  
		Size: 914.1 KB (914097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49ecdfd8c6d37eac63328f874fbb9ad15ce00adce6366792a1af4c8fc13ade0a`  
		Last Modified: Thu, 25 Jul 2024 22:00:48 GMT  
		Size: 30.7 KB (30746 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:38069e07791802e3ae859b88d3ed24ae39bd47c0c262fadcaa5a19b6cc695307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.0 MB (88982239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:170537657cff123e5c869bab2bb7ea295cdc9d87b7ed152fa3a22dfc1fc381a0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Thu, 25 Jul 2024 20:42:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXDB_VERSION=2.7.8
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 25 Jul 2024 20:42:37 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Jul 2024 20:42:37 GMT
CMD ["influxd"]
# Thu, 25 Jul 2024 20:42:37 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 25 Jul 2024 20:42:37 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1de5eaf2a1972853375a025a0309628552446763159c73f9fb971eedad7e97c`  
		Last Modified: Fri, 26 Jul 2024 00:21:08 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b42d817c706fa63528ebb9df4f22670ee67a5c112ac51b215bd8678ac9d67ad`  
		Last Modified: Fri, 26 Jul 2024 00:21:09 GMT  
		Size: 9.8 MB (9763425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62906ecb281c2a5bc707f62ab2b4c4d4b2a03aa7f72fa2a50690041ee145d0a6`  
		Last Modified: Fri, 26 Jul 2024 00:21:09 GMT  
		Size: 5.5 MB (5463800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b061f6bfbb64e47b965b683ae90ab51edf297759c77aaed222b5fe725bcbf12c`  
		Last Modified: Fri, 26 Jul 2024 00:21:08 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ddf646868bea20fb9c33985e55a3399b91f7542506e04b9dbf75d1f577751c`  
		Last Modified: Fri, 26 Jul 2024 00:21:11 GMT  
		Size: 48.0 MB (47997597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c4e2b2b9f546f5ee7181d8d42ca929bc02f55aa86d66ceb9ad510107149aa0`  
		Last Modified: Fri, 26 Jul 2024 00:21:10 GMT  
		Size: 21.7 MB (21662516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cdf7866d6e2a92bb62169de5a27f2d1e5ff074c3fa58197a2a8b0c3f5e3795a`  
		Last Modified: Fri, 26 Jul 2024 00:21:10 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e860d28620195865eda75ca3b59e127cdfc148e6f2f569d8bed47d4f0d03d1`  
		Last Modified: Fri, 26 Jul 2024 00:21:10 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9275442b1367a934d6ac0672ae7677e98ccf3c367a779f1bc30d26421ee6bbfc`  
		Last Modified: Fri, 26 Jul 2024 00:21:11 GMT  
		Size: 6.3 KB (6283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:ef8e5056db345477948ce7481141622023935805a47ae0134cbf533b0e803dc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.4 KB (944404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2454014d973cf1c51ebd53b433151b51881c4affe5d5939ce894b2d0cd644705`

```dockerfile
```

-	Layers:
	-	`sha256:e3a5515ff59a3c4f7db137d7f91ed80d45620c9b4aca52f8dba2028f051a7610`  
		Last Modified: Fri, 26 Jul 2024 00:21:09 GMT  
		Size: 913.4 KB (913358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5480a638871ea5968968e63a134f3227aff5394e81061cfdad6ca533566a75aa`  
		Last Modified: Fri, 26 Jul 2024 00:21:08 GMT  
		Size: 31.0 KB (31046 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7.8`

```console
$ docker pull influxdb@sha256:817a43e512687edbcfe0605df571d5e53b11f8b7ca7a6b317e69f763dc9be070
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7.8` - linux; amd64

```console
$ docker pull influxdb@sha256:cf8c92784dc721e6310ada35067f9d5893bbc9b99e8052237dcbe262b2f8f393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.1 MB (169052639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5b5658780163fd49de58a05c85391fd350be4292c3e9a7b90e6be6303fae0e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:15 GMT
ADD file:6c4730e7b12278bc7eb83b3b9d659437c92c42fc7ee70922ae8c4bebfb56a602 in / 
# Tue, 23 Jul 2024 05:24:16 GMT
CMD ["bash"]
# Thu, 25 Jul 2024 20:42:37 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENV GOSU_VER=1.16
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXDB_VERSION=2.7.8
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 25 Jul 2024 20:42:37 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Jul 2024 20:42:37 GMT
CMD ["influxd"]
# Thu, 25 Jul 2024 20:42:37 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 25 Jul 2024 20:42:37 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:efc2b5ad9eec05befa54239d53feeae3569ccbef689aa5e5dbfc25da6c4df559`  
		Last Modified: Tue, 23 Jul 2024 05:27:55 GMT  
		Size: 29.1 MB (29126287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aafe8e30583ab32a1e9ee7e2646e9683801bd17e63d70bb3bb3f4297db8baec`  
		Last Modified: Thu, 25 Jul 2024 22:00:46 GMT  
		Size: 9.8 MB (9786114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb3e64af86929ccda214e59bfcd54380f99fbd2cfbf05983e15896756066a27`  
		Last Modified: Thu, 25 Jul 2024 22:00:46 GMT  
		Size: 5.8 MB (5820922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b71a5ef49de7ee06787b83119ef3bcb1e81622e6be5f57a39b2c898690a0d2f`  
		Last Modified: Thu, 25 Jul 2024 22:00:46 GMT  
		Size: 3.2 KB (3229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0160b7176ca064e8395e1b99248ceed4ae5e3af57b7c152b522e9e64e53619`  
		Last Modified: Thu, 25 Jul 2024 22:00:46 GMT  
		Size: 1.0 MB (1006371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524d48b867737d10ef449f819f7fa36ea92a5ec7448b52063d4110e326cac34b`  
		Last Modified: Thu, 25 Jul 2024 22:00:48 GMT  
		Size: 100.2 MB (100174652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31cbe0a3f25d229f895dc1d474144dcc31c90a8e239848c874184752383e751`  
		Last Modified: Thu, 25 Jul 2024 22:00:47 GMT  
		Size: 23.1 MB (23128334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8597d281e9c9cb18a861eb227d9f3fa67b5cfa74b1bbbf16f951c694f37ae4b8`  
		Last Modified: Thu, 25 Jul 2024 22:00:47 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bcfb407f38709994863cbc982f8f47e428ed743239fa858736d02334bbd5a6f`  
		Last Modified: Thu, 25 Jul 2024 22:00:47 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634cb105b59a74b80dcdb92049a091cf008cb2fea675da232f5ac1f2d93d9df0`  
		Last Modified: Thu, 25 Jul 2024 22:00:48 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:9fb4a6136fa974e51994e3422345aaaef66b65ec3cb32779092981f6ecbcb32e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6139fd1cc0146a76decf6a803f95c12ac50149ef22d4c77500baba8b9f02c572`

```dockerfile
```

-	Layers:
	-	`sha256:c4fa52ea5261538daf2912b038fa96eadce9ce9198409ba8938af04c2b68cdcf`  
		Last Modified: Thu, 25 Jul 2024 22:00:46 GMT  
		Size: 2.8 MB (2833446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53b7394c3923f72225c4d186b8b3c829f52d3bc04899c3afa693b35d62339a6d`  
		Last Modified: Thu, 25 Jul 2024 22:00:46 GMT  
		Size: 33.5 KB (33544 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:ad1b67786fdafa8a6c928afde9514e9e61aa9196ba48ea0f85b02d46de88d4c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.8 MB (162819854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17b90fc212a2e15b03dfea6f55bba7e6841e9e68345b5de78ecae786f6715ee4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:51 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Tue, 23 Jul 2024 04:17:52 GMT
CMD ["bash"]
# Thu, 25 Jul 2024 20:42:37 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENV GOSU_VER=1.16
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXDB_VERSION=2.7.8
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 25 Jul 2024 20:42:37 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Jul 2024 20:42:37 GMT
CMD ["influxd"]
# Thu, 25 Jul 2024 20:42:37 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 25 Jul 2024 20:42:37 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570d86bee5eb6e09d1e4ecabe00877506dfef15eb8c1d0fb37fd03689650e726`  
		Last Modified: Fri, 26 Jul 2024 00:20:36 GMT  
		Size: 9.6 MB (9585146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8102b54b2061157b520e8d0c54ab9debfd7caeecf5b04ee4ff14f2a58c7ae5df`  
		Last Modified: Fri, 26 Jul 2024 00:20:36 GMT  
		Size: 5.5 MB (5463802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929f8e0bdc48c34a35a494a9768a1b505a86513c4cee278321f7df04a94698c2`  
		Last Modified: Fri, 26 Jul 2024 00:20:35 GMT  
		Size: 3.2 KB (3230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c078ee5f7362fbfa31e25a1b4c0fd0631479e57f820dfffe3d06fb939194699f`  
		Last Modified: Fri, 26 Jul 2024 00:20:36 GMT  
		Size: 936.1 KB (936109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0dd648633f64d4e39c97d3ef2a1d2784576fdbf65f90a11200b251c3b94c315`  
		Last Modified: Fri, 26 Jul 2024 00:20:39 GMT  
		Size: 96.0 MB (96005753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603c87bd567840dca04aa427260c8a8aef651d2c7dc55c70764e63200994ee71`  
		Last Modified: Fri, 26 Jul 2024 00:20:38 GMT  
		Size: 21.7 MB (21662517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7164f83c3085ab88b97f6aaecb51faaabcffcd70da9232e2a3982b9f6188905`  
		Last Modified: Fri, 26 Jul 2024 00:20:37 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132469a32a34a142198cc86019e6873278d6c8d25d43211ce10fff9327b6eb5c`  
		Last Modified: Fri, 26 Jul 2024 00:20:37 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8bee1e60c9fce079bf33dec8d4aa96459f86b491cb40d9a012fdf6c7eaf6663`  
		Last Modified: Fri, 26 Jul 2024 00:20:38 GMT  
		Size: 6.3 KB (6283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:e3c42143d1c2133c4178ab80b70d5a71beec793914426d9fba59eee164af843b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:894b26438d5a95eac85d03b568c647befed1805d6e9bf36fc3d6de8daecadb05`

```dockerfile
```

-	Layers:
	-	`sha256:83a2c2603d57f30d2d08d326b754c1e47956a0c97cf0f068b975475b846e4c5d`  
		Last Modified: Fri, 26 Jul 2024 00:20:36 GMT  
		Size: 2.8 MB (2832683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7db705f4da94aa74a70c426336d619b60b6abc61281b289133bd61d6273ce20d`  
		Last Modified: Fri, 26 Jul 2024 00:20:35 GMT  
		Size: 33.8 KB (33843 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7.8-alpine`

```console
$ docker pull influxdb@sha256:aa7c7967db6299829f225c931edbe2e53cb74bc32d8a8689eb10a71ec0cc4f9a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7.8-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:9df149c10d324879963a5a690c3b3ba71bdea5208d5cb595d5aa083314438e92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92302723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:197b9f7cf87e0c89204d30b0327432a13a7d21e94eaaebad1208953a34be32b0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Thu, 25 Jul 2024 20:42:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXDB_VERSION=2.7.8
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 25 Jul 2024 20:42:37 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Jul 2024 20:42:37 GMT
CMD ["influxd"]
# Thu, 25 Jul 2024 20:42:37 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 25 Jul 2024 20:42:37 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d45a0a4871208edeaf34244b70f2d47191b76f2b4997648bacee65f0bb9b50f`  
		Last Modified: Thu, 25 Jul 2024 22:00:48 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee199347147ba36a9ac1c8db22d05c1c0b79ce7413994e38d8195544577dbca`  
		Last Modified: Thu, 25 Jul 2024 22:00:48 GMT  
		Size: 9.6 MB (9640728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa969dbbaaa21fef569a8823d550f3eb33e6b24d275e9c20b68b15cf0c605015`  
		Last Modified: Thu, 25 Jul 2024 22:00:48 GMT  
		Size: 5.8 MB (5820951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8142b4768fda9be2ced3e3eca82355fe675152715254e0baecfbbe1d80f5236`  
		Last Modified: Thu, 25 Jul 2024 22:00:48 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:380d583d17bced46b979236bdba753d5f94fa5a1fcadce3e45283a7d08918db2`  
		Last Modified: Thu, 25 Jul 2024 22:00:49 GMT  
		Size: 50.1 MB (50081865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff5e1ae40d1867d5fe7a6e65a7cc6488a475e6f73a97b2a4da6f8578ad3c21c`  
		Last Modified: Thu, 25 Jul 2024 22:00:49 GMT  
		Size: 23.1 MB (23128318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c693aab95480f71f592cc525cc940a6432037406963ee4ac5ad6035bd262167a`  
		Last Modified: Thu, 25 Jul 2024 22:00:49 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a68978ad7a69b0b85802e8367847c0ece31edd4e193283c0c40774fdbe43001`  
		Last Modified: Thu, 25 Jul 2024 22:00:49 GMT  
		Size: 235.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d385c3278fe6011ecc879151ad7f9bc7ba4a811b3c443d3b80afd979ee26eee`  
		Last Modified: Thu, 25 Jul 2024 22:00:49 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.8-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:097e3065499d4cc13248203886f2943f82a6e3a0ab2ab07cf9378e18831f7e5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.8 KB (944843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ab074677763b44aaf3b7d3bcacc8bd61e7fdb67dfab0e15c66f6ffa9c557a2e`

```dockerfile
```

-	Layers:
	-	`sha256:0a9cbd4c122519853b11796e1db3443af625b2b65b4199f595f63057b1cd5175`  
		Last Modified: Thu, 25 Jul 2024 22:00:48 GMT  
		Size: 914.1 KB (914097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49ecdfd8c6d37eac63328f874fbb9ad15ce00adce6366792a1af4c8fc13ade0a`  
		Last Modified: Thu, 25 Jul 2024 22:00:48 GMT  
		Size: 30.7 KB (30746 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7.8-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:38069e07791802e3ae859b88d3ed24ae39bd47c0c262fadcaa5a19b6cc695307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.0 MB (88982239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:170537657cff123e5c869bab2bb7ea295cdc9d87b7ed152fa3a22dfc1fc381a0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Thu, 25 Jul 2024 20:42:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXDB_VERSION=2.7.8
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 25 Jul 2024 20:42:37 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Jul 2024 20:42:37 GMT
CMD ["influxd"]
# Thu, 25 Jul 2024 20:42:37 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 25 Jul 2024 20:42:37 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1de5eaf2a1972853375a025a0309628552446763159c73f9fb971eedad7e97c`  
		Last Modified: Fri, 26 Jul 2024 00:21:08 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b42d817c706fa63528ebb9df4f22670ee67a5c112ac51b215bd8678ac9d67ad`  
		Last Modified: Fri, 26 Jul 2024 00:21:09 GMT  
		Size: 9.8 MB (9763425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62906ecb281c2a5bc707f62ab2b4c4d4b2a03aa7f72fa2a50690041ee145d0a6`  
		Last Modified: Fri, 26 Jul 2024 00:21:09 GMT  
		Size: 5.5 MB (5463800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b061f6bfbb64e47b965b683ae90ab51edf297759c77aaed222b5fe725bcbf12c`  
		Last Modified: Fri, 26 Jul 2024 00:21:08 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ddf646868bea20fb9c33985e55a3399b91f7542506e04b9dbf75d1f577751c`  
		Last Modified: Fri, 26 Jul 2024 00:21:11 GMT  
		Size: 48.0 MB (47997597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c4e2b2b9f546f5ee7181d8d42ca929bc02f55aa86d66ceb9ad510107149aa0`  
		Last Modified: Fri, 26 Jul 2024 00:21:10 GMT  
		Size: 21.7 MB (21662516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cdf7866d6e2a92bb62169de5a27f2d1e5ff074c3fa58197a2a8b0c3f5e3795a`  
		Last Modified: Fri, 26 Jul 2024 00:21:10 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e860d28620195865eda75ca3b59e127cdfc148e6f2f569d8bed47d4f0d03d1`  
		Last Modified: Fri, 26 Jul 2024 00:21:10 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9275442b1367a934d6ac0672ae7677e98ccf3c367a779f1bc30d26421ee6bbfc`  
		Last Modified: Fri, 26 Jul 2024 00:21:11 GMT  
		Size: 6.3 KB (6283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.8-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:ef8e5056db345477948ce7481141622023935805a47ae0134cbf533b0e803dc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.4 KB (944404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2454014d973cf1c51ebd53b433151b51881c4affe5d5939ce894b2d0cd644705`

```dockerfile
```

-	Layers:
	-	`sha256:e3a5515ff59a3c4f7db137d7f91ed80d45620c9b4aca52f8dba2028f051a7610`  
		Last Modified: Fri, 26 Jul 2024 00:21:09 GMT  
		Size: 913.4 KB (913358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5480a638871ea5968968e63a134f3227aff5394e81061cfdad6ca533566a75aa`  
		Last Modified: Fri, 26 Jul 2024 00:21:08 GMT  
		Size: 31.0 KB (31046 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:aa7c7967db6299829f225c931edbe2e53cb74bc32d8a8689eb10a71ec0cc4f9a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:9df149c10d324879963a5a690c3b3ba71bdea5208d5cb595d5aa083314438e92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92302723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:197b9f7cf87e0c89204d30b0327432a13a7d21e94eaaebad1208953a34be32b0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Thu, 25 Jul 2024 20:42:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXDB_VERSION=2.7.8
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 25 Jul 2024 20:42:37 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Jul 2024 20:42:37 GMT
CMD ["influxd"]
# Thu, 25 Jul 2024 20:42:37 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 25 Jul 2024 20:42:37 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d45a0a4871208edeaf34244b70f2d47191b76f2b4997648bacee65f0bb9b50f`  
		Last Modified: Thu, 25 Jul 2024 22:00:48 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee199347147ba36a9ac1c8db22d05c1c0b79ce7413994e38d8195544577dbca`  
		Last Modified: Thu, 25 Jul 2024 22:00:48 GMT  
		Size: 9.6 MB (9640728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa969dbbaaa21fef569a8823d550f3eb33e6b24d275e9c20b68b15cf0c605015`  
		Last Modified: Thu, 25 Jul 2024 22:00:48 GMT  
		Size: 5.8 MB (5820951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8142b4768fda9be2ced3e3eca82355fe675152715254e0baecfbbe1d80f5236`  
		Last Modified: Thu, 25 Jul 2024 22:00:48 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:380d583d17bced46b979236bdba753d5f94fa5a1fcadce3e45283a7d08918db2`  
		Last Modified: Thu, 25 Jul 2024 22:00:49 GMT  
		Size: 50.1 MB (50081865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff5e1ae40d1867d5fe7a6e65a7cc6488a475e6f73a97b2a4da6f8578ad3c21c`  
		Last Modified: Thu, 25 Jul 2024 22:00:49 GMT  
		Size: 23.1 MB (23128318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c693aab95480f71f592cc525cc940a6432037406963ee4ac5ad6035bd262167a`  
		Last Modified: Thu, 25 Jul 2024 22:00:49 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a68978ad7a69b0b85802e8367847c0ece31edd4e193283c0c40774fdbe43001`  
		Last Modified: Thu, 25 Jul 2024 22:00:49 GMT  
		Size: 235.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d385c3278fe6011ecc879151ad7f9bc7ba4a811b3c443d3b80afd979ee26eee`  
		Last Modified: Thu, 25 Jul 2024 22:00:49 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:097e3065499d4cc13248203886f2943f82a6e3a0ab2ab07cf9378e18831f7e5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.8 KB (944843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ab074677763b44aaf3b7d3bcacc8bd61e7fdb67dfab0e15c66f6ffa9c557a2e`

```dockerfile
```

-	Layers:
	-	`sha256:0a9cbd4c122519853b11796e1db3443af625b2b65b4199f595f63057b1cd5175`  
		Last Modified: Thu, 25 Jul 2024 22:00:48 GMT  
		Size: 914.1 KB (914097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49ecdfd8c6d37eac63328f874fbb9ad15ce00adce6366792a1af4c8fc13ade0a`  
		Last Modified: Thu, 25 Jul 2024 22:00:48 GMT  
		Size: 30.7 KB (30746 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:38069e07791802e3ae859b88d3ed24ae39bd47c0c262fadcaa5a19b6cc695307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.0 MB (88982239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:170537657cff123e5c869bab2bb7ea295cdc9d87b7ed152fa3a22dfc1fc381a0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Thu, 25 Jul 2024 20:42:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXDB_VERSION=2.7.8
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 25 Jul 2024 20:42:37 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Jul 2024 20:42:37 GMT
CMD ["influxd"]
# Thu, 25 Jul 2024 20:42:37 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 25 Jul 2024 20:42:37 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1de5eaf2a1972853375a025a0309628552446763159c73f9fb971eedad7e97c`  
		Last Modified: Fri, 26 Jul 2024 00:21:08 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b42d817c706fa63528ebb9df4f22670ee67a5c112ac51b215bd8678ac9d67ad`  
		Last Modified: Fri, 26 Jul 2024 00:21:09 GMT  
		Size: 9.8 MB (9763425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62906ecb281c2a5bc707f62ab2b4c4d4b2a03aa7f72fa2a50690041ee145d0a6`  
		Last Modified: Fri, 26 Jul 2024 00:21:09 GMT  
		Size: 5.5 MB (5463800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b061f6bfbb64e47b965b683ae90ab51edf297759c77aaed222b5fe725bcbf12c`  
		Last Modified: Fri, 26 Jul 2024 00:21:08 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ddf646868bea20fb9c33985e55a3399b91f7542506e04b9dbf75d1f577751c`  
		Last Modified: Fri, 26 Jul 2024 00:21:11 GMT  
		Size: 48.0 MB (47997597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c4e2b2b9f546f5ee7181d8d42ca929bc02f55aa86d66ceb9ad510107149aa0`  
		Last Modified: Fri, 26 Jul 2024 00:21:10 GMT  
		Size: 21.7 MB (21662516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cdf7866d6e2a92bb62169de5a27f2d1e5ff074c3fa58197a2a8b0c3f5e3795a`  
		Last Modified: Fri, 26 Jul 2024 00:21:10 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e860d28620195865eda75ca3b59e127cdfc148e6f2f569d8bed47d4f0d03d1`  
		Last Modified: Fri, 26 Jul 2024 00:21:10 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9275442b1367a934d6ac0672ae7677e98ccf3c367a779f1bc30d26421ee6bbfc`  
		Last Modified: Fri, 26 Jul 2024 00:21:11 GMT  
		Size: 6.3 KB (6283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:ef8e5056db345477948ce7481141622023935805a47ae0134cbf533b0e803dc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.4 KB (944404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2454014d973cf1c51ebd53b433151b51881c4affe5d5939ce894b2d0cd644705`

```dockerfile
```

-	Layers:
	-	`sha256:e3a5515ff59a3c4f7db137d7f91ed80d45620c9b4aca52f8dba2028f051a7610`  
		Last Modified: Fri, 26 Jul 2024 00:21:09 GMT  
		Size: 913.4 KB (913358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5480a638871ea5968968e63a134f3227aff5394e81061cfdad6ca533566a75aa`  
		Last Modified: Fri, 26 Jul 2024 00:21:08 GMT  
		Size: 31.0 KB (31046 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:latest`

```console
$ docker pull influxdb@sha256:817a43e512687edbcfe0605df571d5e53b11f8b7ca7a6b317e69f763dc9be070
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:cf8c92784dc721e6310ada35067f9d5893bbc9b99e8052237dcbe262b2f8f393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.1 MB (169052639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5b5658780163fd49de58a05c85391fd350be4292c3e9a7b90e6be6303fae0e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:15 GMT
ADD file:6c4730e7b12278bc7eb83b3b9d659437c92c42fc7ee70922ae8c4bebfb56a602 in / 
# Tue, 23 Jul 2024 05:24:16 GMT
CMD ["bash"]
# Thu, 25 Jul 2024 20:42:37 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENV GOSU_VER=1.16
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXDB_VERSION=2.7.8
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 25 Jul 2024 20:42:37 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Jul 2024 20:42:37 GMT
CMD ["influxd"]
# Thu, 25 Jul 2024 20:42:37 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 25 Jul 2024 20:42:37 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:efc2b5ad9eec05befa54239d53feeae3569ccbef689aa5e5dbfc25da6c4df559`  
		Last Modified: Tue, 23 Jul 2024 05:27:55 GMT  
		Size: 29.1 MB (29126287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aafe8e30583ab32a1e9ee7e2646e9683801bd17e63d70bb3bb3f4297db8baec`  
		Last Modified: Thu, 25 Jul 2024 22:00:46 GMT  
		Size: 9.8 MB (9786114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb3e64af86929ccda214e59bfcd54380f99fbd2cfbf05983e15896756066a27`  
		Last Modified: Thu, 25 Jul 2024 22:00:46 GMT  
		Size: 5.8 MB (5820922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b71a5ef49de7ee06787b83119ef3bcb1e81622e6be5f57a39b2c898690a0d2f`  
		Last Modified: Thu, 25 Jul 2024 22:00:46 GMT  
		Size: 3.2 KB (3229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0160b7176ca064e8395e1b99248ceed4ae5e3af57b7c152b522e9e64e53619`  
		Last Modified: Thu, 25 Jul 2024 22:00:46 GMT  
		Size: 1.0 MB (1006371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524d48b867737d10ef449f819f7fa36ea92a5ec7448b52063d4110e326cac34b`  
		Last Modified: Thu, 25 Jul 2024 22:00:48 GMT  
		Size: 100.2 MB (100174652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31cbe0a3f25d229f895dc1d474144dcc31c90a8e239848c874184752383e751`  
		Last Modified: Thu, 25 Jul 2024 22:00:47 GMT  
		Size: 23.1 MB (23128334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8597d281e9c9cb18a861eb227d9f3fa67b5cfa74b1bbbf16f951c694f37ae4b8`  
		Last Modified: Thu, 25 Jul 2024 22:00:47 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bcfb407f38709994863cbc982f8f47e428ed743239fa858736d02334bbd5a6f`  
		Last Modified: Thu, 25 Jul 2024 22:00:47 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634cb105b59a74b80dcdb92049a091cf008cb2fea675da232f5ac1f2d93d9df0`  
		Last Modified: Thu, 25 Jul 2024 22:00:48 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:9fb4a6136fa974e51994e3422345aaaef66b65ec3cb32779092981f6ecbcb32e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6139fd1cc0146a76decf6a803f95c12ac50149ef22d4c77500baba8b9f02c572`

```dockerfile
```

-	Layers:
	-	`sha256:c4fa52ea5261538daf2912b038fa96eadce9ce9198409ba8938af04c2b68cdcf`  
		Last Modified: Thu, 25 Jul 2024 22:00:46 GMT  
		Size: 2.8 MB (2833446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53b7394c3923f72225c4d186b8b3c829f52d3bc04899c3afa693b35d62339a6d`  
		Last Modified: Thu, 25 Jul 2024 22:00:46 GMT  
		Size: 33.5 KB (33544 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:ad1b67786fdafa8a6c928afde9514e9e61aa9196ba48ea0f85b02d46de88d4c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.8 MB (162819854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17b90fc212a2e15b03dfea6f55bba7e6841e9e68345b5de78ecae786f6715ee4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:51 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Tue, 23 Jul 2024 04:17:52 GMT
CMD ["bash"]
# Thu, 25 Jul 2024 20:42:37 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENV GOSU_VER=1.16
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXDB_VERSION=2.7.8
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 25 Jul 2024 20:42:37 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Jul 2024 20:42:37 GMT
CMD ["influxd"]
# Thu, 25 Jul 2024 20:42:37 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 25 Jul 2024 20:42:37 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570d86bee5eb6e09d1e4ecabe00877506dfef15eb8c1d0fb37fd03689650e726`  
		Last Modified: Fri, 26 Jul 2024 00:20:36 GMT  
		Size: 9.6 MB (9585146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8102b54b2061157b520e8d0c54ab9debfd7caeecf5b04ee4ff14f2a58c7ae5df`  
		Last Modified: Fri, 26 Jul 2024 00:20:36 GMT  
		Size: 5.5 MB (5463802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929f8e0bdc48c34a35a494a9768a1b505a86513c4cee278321f7df04a94698c2`  
		Last Modified: Fri, 26 Jul 2024 00:20:35 GMT  
		Size: 3.2 KB (3230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c078ee5f7362fbfa31e25a1b4c0fd0631479e57f820dfffe3d06fb939194699f`  
		Last Modified: Fri, 26 Jul 2024 00:20:36 GMT  
		Size: 936.1 KB (936109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0dd648633f64d4e39c97d3ef2a1d2784576fdbf65f90a11200b251c3b94c315`  
		Last Modified: Fri, 26 Jul 2024 00:20:39 GMT  
		Size: 96.0 MB (96005753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603c87bd567840dca04aa427260c8a8aef651d2c7dc55c70764e63200994ee71`  
		Last Modified: Fri, 26 Jul 2024 00:20:38 GMT  
		Size: 21.7 MB (21662517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7164f83c3085ab88b97f6aaecb51faaabcffcd70da9232e2a3982b9f6188905`  
		Last Modified: Fri, 26 Jul 2024 00:20:37 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132469a32a34a142198cc86019e6873278d6c8d25d43211ce10fff9327b6eb5c`  
		Last Modified: Fri, 26 Jul 2024 00:20:37 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8bee1e60c9fce079bf33dec8d4aa96459f86b491cb40d9a012fdf6c7eaf6663`  
		Last Modified: Fri, 26 Jul 2024 00:20:38 GMT  
		Size: 6.3 KB (6283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:e3c42143d1c2133c4178ab80b70d5a71beec793914426d9fba59eee164af843b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:894b26438d5a95eac85d03b568c647befed1805d6e9bf36fc3d6de8daecadb05`

```dockerfile
```

-	Layers:
	-	`sha256:83a2c2603d57f30d2d08d326b754c1e47956a0c97cf0f068b975475b846e4c5d`  
		Last Modified: Fri, 26 Jul 2024 00:20:36 GMT  
		Size: 2.8 MB (2832683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7db705f4da94aa74a70c426336d619b60b6abc61281b289133bd61d6273ce20d`  
		Last Modified: Fri, 26 Jul 2024 00:20:35 GMT  
		Size: 33.8 KB (33843 bytes)  
		MIME: application/vnd.in-toto+json
