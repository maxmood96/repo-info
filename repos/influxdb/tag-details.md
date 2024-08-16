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
-	[`influxdb:2.7.10`](#influxdb2710)
-	[`influxdb:2.7.10-alpine`](#influxdb2710-alpine)
-	[`influxdb:alpine`](#influxdbalpine)
-	[`influxdb:latest`](#influxdblatest)

## `influxdb:1.10-data`

```console
$ docker pull influxdb@sha256:a2a1fa5a3ee9019dda6acd6b80f8af673951d70526abce517b89186965a65594
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-data` - linux; amd64

```console
$ docker pull influxdb@sha256:398ef1970753f6a490a6965d94cff64d2ea1cf572358b5e251f1f44e76dbc1fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112230208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8615678857816d90234092d60bb45ad92bfc891bb8e4eaf7239aaede82181982`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 09 Aug 2024 17:32:24 GMT
ADD file:6648a8158bbf4a36244eb9e936fbed4ea29f2f090fb0a97a6a737be2d85a5333 in / 
# Fri, 09 Aug 2024 17:32:24 GMT
CMD ["bash"]
# Fri, 09 Aug 2024 17:32:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 09 Aug 2024 17:32:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Fri, 09 Aug 2024 17:32:24 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 09 Aug 2024 17:32:24 GMT
VOLUME [/var/lib/influxdb]
# Fri, 09 Aug 2024 17:32:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 09 Aug 2024 17:32:24 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:203e9cf21bd27322e5baf32653bf3314ccf688be497585240d18b9f0ca24f2ee`  
		Last Modified: Tue, 13 Aug 2024 00:24:05 GMT  
		Size: 55.1 MB (55084675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3438c04e457d7cf49dfbfe92aa9c64df2c0d9dc8ac53a7dbda0c620c405d9f`  
		Last Modified: Tue, 13 Aug 2024 00:50:52 GMT  
		Size: 15.8 MB (15764253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbd27048e1302b743b3cdd1d2cf403df1fe028b664c0fde226ccb39ef7f56ec`  
		Last Modified: Tue, 13 Aug 2024 02:05:13 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d345ea0aba110ae587db3f39beb70a1809ea873785b298a52293863de43ef9ff`  
		Last Modified: Tue, 13 Aug 2024 02:05:14 GMT  
		Size: 41.4 MB (41377725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be26ebfa45b9171ac3a9f5521ecdb2046ed098563a3a659744b9a618b08ee162`  
		Last Modified: Tue, 13 Aug 2024 02:05:13 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01af6894a5dea53e335765557ce0c12c1bdbb904cbace4b09c2020d7788715b5`  
		Last Modified: Tue, 13 Aug 2024 02:05:13 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4706c4c52818abab48f3604dba30f5076cbaabc7956d2cca10e3ba433f95f6a4`  
		Last Modified: Tue, 13 Aug 2024 02:05:14 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:3585fccfa5b3b3b239036f087760429df9e43616b1bad6d6f53214beb18cf904
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4642339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:645ff29f6723bb6e1b7028db37286ad642e6a3a6f7b6c76ad1b023970f0f4166`

```dockerfile
```

-	Layers:
	-	`sha256:63fbdb7b26a9e1389cee1e1150aee6fb1b7ef9af5ebc54caf34af95c4944bbd7`  
		Last Modified: Tue, 13 Aug 2024 02:05:14 GMT  
		Size: 4.6 MB (4627765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eec7d255b2be8a900783b4e0566cc1d648cc80560fca0926d58c0abca47407b4`  
		Last Modified: Tue, 13 Aug 2024 02:05:13 GMT  
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
$ docker pull influxdb@sha256:e15e10788f4341283bbec0acef7c4dd53e331da04284318674ee7d51c41a73af
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:136743b0ae896a2d00680f3b54ae0f80297d0ef206ebc6c72e4d0c4e450e93a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.9 MB (90946836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e142dabf758fdb0ccd2bab51f16e6dbab3e133feee4c9be36b1d0c123789942c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 09 Aug 2024 17:32:24 GMT
ADD file:6648a8158bbf4a36244eb9e936fbed4ea29f2f090fb0a97a6a737be2d85a5333 in / 
# Fri, 09 Aug 2024 17:32:24 GMT
CMD ["bash"]
# Fri, 09 Aug 2024 17:32:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 09 Aug 2024 17:32:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Fri, 09 Aug 2024 17:32:24 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
EXPOSE map[8091/tcp:{}]
# Fri, 09 Aug 2024 17:32:24 GMT
VOLUME [/var/lib/influxdb]
# Fri, 09 Aug 2024 17:32:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 09 Aug 2024 17:32:24 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:203e9cf21bd27322e5baf32653bf3314ccf688be497585240d18b9f0ca24f2ee`  
		Last Modified: Tue, 13 Aug 2024 00:24:05 GMT  
		Size: 55.1 MB (55084675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3438c04e457d7cf49dfbfe92aa9c64df2c0d9dc8ac53a7dbda0c620c405d9f`  
		Last Modified: Tue, 13 Aug 2024 00:50:52 GMT  
		Size: 15.8 MB (15764253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15acb6e8ba6f585da38f92c7895727059f503db9e280524390613a46aa89b7f6`  
		Last Modified: Tue, 13 Aug 2024 02:05:07 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64084cab3be860a75e3036cae85d429cd7a55d852b180604482a7e49d34d913`  
		Last Modified: Tue, 13 Aug 2024 02:05:07 GMT  
		Size: 20.1 MB (20095560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4502ab9716dc0acb1426b0da9d360c8e547737889f95966d0ab3f87da26f36f8`  
		Last Modified: Tue, 13 Aug 2024 02:05:07 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff8d064ba730aa5122c27fe7d5f8d87777104d7ab5fbada6f9a5dcfbcfdd461e`  
		Last Modified: Tue, 13 Aug 2024 02:05:08 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:394606bc38295d944d3cdfee09fd114d98f910ee2692c60bb941fa253fcb714d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4565272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff64edbaabd5e714b08dd62fd5be77deff95ed43b2beedd01497c594caf90740`

```dockerfile
```

-	Layers:
	-	`sha256:c5f0975bf8e6fd5478caa84e3b603649f43471bdb90e1275b82a12c3816544f9`  
		Last Modified: Tue, 13 Aug 2024 02:05:07 GMT  
		Size: 4.6 MB (4552352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:683df59afad61a38452cca605f5acd411e756999ec6f09c1553e8b8599213fcb`  
		Last Modified: Tue, 13 Aug 2024 02:05:07 GMT  
		Size: 12.9 KB (12920 bytes)  
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
$ docker pull influxdb@sha256:a2a1fa5a3ee9019dda6acd6b80f8af673951d70526abce517b89186965a65594
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.7-data` - linux; amd64

```console
$ docker pull influxdb@sha256:398ef1970753f6a490a6965d94cff64d2ea1cf572358b5e251f1f44e76dbc1fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112230208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8615678857816d90234092d60bb45ad92bfc891bb8e4eaf7239aaede82181982`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 09 Aug 2024 17:32:24 GMT
ADD file:6648a8158bbf4a36244eb9e936fbed4ea29f2f090fb0a97a6a737be2d85a5333 in / 
# Fri, 09 Aug 2024 17:32:24 GMT
CMD ["bash"]
# Fri, 09 Aug 2024 17:32:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 09 Aug 2024 17:32:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Fri, 09 Aug 2024 17:32:24 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 09 Aug 2024 17:32:24 GMT
VOLUME [/var/lib/influxdb]
# Fri, 09 Aug 2024 17:32:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 09 Aug 2024 17:32:24 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:203e9cf21bd27322e5baf32653bf3314ccf688be497585240d18b9f0ca24f2ee`  
		Last Modified: Tue, 13 Aug 2024 00:24:05 GMT  
		Size: 55.1 MB (55084675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3438c04e457d7cf49dfbfe92aa9c64df2c0d9dc8ac53a7dbda0c620c405d9f`  
		Last Modified: Tue, 13 Aug 2024 00:50:52 GMT  
		Size: 15.8 MB (15764253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbd27048e1302b743b3cdd1d2cf403df1fe028b664c0fde226ccb39ef7f56ec`  
		Last Modified: Tue, 13 Aug 2024 02:05:13 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d345ea0aba110ae587db3f39beb70a1809ea873785b298a52293863de43ef9ff`  
		Last Modified: Tue, 13 Aug 2024 02:05:14 GMT  
		Size: 41.4 MB (41377725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be26ebfa45b9171ac3a9f5521ecdb2046ed098563a3a659744b9a618b08ee162`  
		Last Modified: Tue, 13 Aug 2024 02:05:13 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01af6894a5dea53e335765557ce0c12c1bdbb904cbace4b09c2020d7788715b5`  
		Last Modified: Tue, 13 Aug 2024 02:05:13 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4706c4c52818abab48f3604dba30f5076cbaabc7956d2cca10e3ba433f95f6a4`  
		Last Modified: Tue, 13 Aug 2024 02:05:14 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.7-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:3585fccfa5b3b3b239036f087760429df9e43616b1bad6d6f53214beb18cf904
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4642339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:645ff29f6723bb6e1b7028db37286ad642e6a3a6f7b6c76ad1b023970f0f4166`

```dockerfile
```

-	Layers:
	-	`sha256:63fbdb7b26a9e1389cee1e1150aee6fb1b7ef9af5ebc54caf34af95c4944bbd7`  
		Last Modified: Tue, 13 Aug 2024 02:05:14 GMT  
		Size: 4.6 MB (4627765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eec7d255b2be8a900783b4e0566cc1d648cc80560fca0926d58c0abca47407b4`  
		Last Modified: Tue, 13 Aug 2024 02:05:13 GMT  
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
$ docker pull influxdb@sha256:e15e10788f4341283bbec0acef7c4dd53e331da04284318674ee7d51c41a73af
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.7-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:136743b0ae896a2d00680f3b54ae0f80297d0ef206ebc6c72e4d0c4e450e93a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.9 MB (90946836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e142dabf758fdb0ccd2bab51f16e6dbab3e133feee4c9be36b1d0c123789942c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 09 Aug 2024 17:32:24 GMT
ADD file:6648a8158bbf4a36244eb9e936fbed4ea29f2f090fb0a97a6a737be2d85a5333 in / 
# Fri, 09 Aug 2024 17:32:24 GMT
CMD ["bash"]
# Fri, 09 Aug 2024 17:32:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 09 Aug 2024 17:32:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Fri, 09 Aug 2024 17:32:24 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
EXPOSE map[8091/tcp:{}]
# Fri, 09 Aug 2024 17:32:24 GMT
VOLUME [/var/lib/influxdb]
# Fri, 09 Aug 2024 17:32:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 09 Aug 2024 17:32:24 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:203e9cf21bd27322e5baf32653bf3314ccf688be497585240d18b9f0ca24f2ee`  
		Last Modified: Tue, 13 Aug 2024 00:24:05 GMT  
		Size: 55.1 MB (55084675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3438c04e457d7cf49dfbfe92aa9c64df2c0d9dc8ac53a7dbda0c620c405d9f`  
		Last Modified: Tue, 13 Aug 2024 00:50:52 GMT  
		Size: 15.8 MB (15764253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15acb6e8ba6f585da38f92c7895727059f503db9e280524390613a46aa89b7f6`  
		Last Modified: Tue, 13 Aug 2024 02:05:07 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64084cab3be860a75e3036cae85d429cd7a55d852b180604482a7e49d34d913`  
		Last Modified: Tue, 13 Aug 2024 02:05:07 GMT  
		Size: 20.1 MB (20095560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4502ab9716dc0acb1426b0da9d360c8e547737889f95966d0ab3f87da26f36f8`  
		Last Modified: Tue, 13 Aug 2024 02:05:07 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff8d064ba730aa5122c27fe7d5f8d87777104d7ab5fbada6f9a5dcfbcfdd461e`  
		Last Modified: Tue, 13 Aug 2024 02:05:08 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.7-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:394606bc38295d944d3cdfee09fd114d98f910ee2692c60bb941fa253fcb714d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4565272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff64edbaabd5e714b08dd62fd5be77deff95ed43b2beedd01497c594caf90740`

```dockerfile
```

-	Layers:
	-	`sha256:c5f0975bf8e6fd5478caa84e3b603649f43471bdb90e1275b82a12c3816544f9`  
		Last Modified: Tue, 13 Aug 2024 02:05:07 GMT  
		Size: 4.6 MB (4552352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:683df59afad61a38452cca605f5acd411e756999ec6f09c1553e8b8599213fcb`  
		Last Modified: Tue, 13 Aug 2024 02:05:07 GMT  
		Size: 12.9 KB (12920 bytes)  
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
$ docker pull influxdb@sha256:d15f83bfdb8f9b22a40c86442e5ceb0ec63f19d061600dc5a430c639e50f4de3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data` - linux; amd64

```console
$ docker pull influxdb@sha256:e659b59ba45125804b636cbb9182681fcc1b4923e271b28f85c68f2bb5b0a59d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114732704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1046c78ec3a11ff6d8896ac109b2d33e0533516f700974894661db24d19f0b6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 09 Aug 2024 17:32:24 GMT
ADD file:0d5bdf84bbcdfa95d42190537e3cad2c0a5876f9127fae6a1d1c485d3539c77d in / 
# Fri, 09 Aug 2024 17:32:24 GMT
CMD ["bash"]
# Fri, 09 Aug 2024 17:32:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 09 Aug 2024 17:32:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUXDB_VERSION=1.11.6-c1.11.6
# Fri, 09 Aug 2024 17:32:24 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 09 Aug 2024 17:32:24 GMT
VOLUME [/var/lib/influxdb]
# Fri, 09 Aug 2024 17:32:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 09 Aug 2024 17:32:24 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:903681d87777d28dc56866a07a2774c3fd5bf65fd734b24c9d0ecd9a13c9f636`  
		Last Modified: Tue, 13 Aug 2024 00:23:26 GMT  
		Size: 49.6 MB (49554080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cbbe86a28c2f6b3c3e0e8c6dcfba369e1ea656cf8daf69be789e0fe2105982b`  
		Last Modified: Tue, 13 Aug 2024 00:49:47 GMT  
		Size: 24.1 MB (24050697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb214b8f5f5e8956ad5ea8f980c9e6f56c5a9098d7e50d00a34c7792df23a79`  
		Last Modified: Tue, 13 Aug 2024 02:05:19 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6573d4aeb8df47ac73414c1a747d6e6e07756469db238cb0485eaac08ff4660b`  
		Last Modified: Tue, 13 Aug 2024 02:05:19 GMT  
		Size: 41.1 MB (41124377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5490dc6a9835356f1937e41e7e239a5fd5a76cc08362c0ae4de6c9dfd071b07`  
		Last Modified: Tue, 13 Aug 2024 02:05:19 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51790e06b4ef2b1bae56652a38c2cd0ddf9242cee2d24f74e926e3eacaa79173`  
		Last Modified: Tue, 13 Aug 2024 02:05:19 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e783ee95bfb4cfed880f3dc934887c227a5f1f6d6c6cb69a90fc833cd8ecf02`  
		Last Modified: Tue, 13 Aug 2024 02:05:20 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:02ddfbb6bcbee1d7c85555d822a389e9cfb946f576139a8a7169d121ad79aa6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4515827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce32357c2f36b19362969bd979d3665104a9bf874f63568c2e83ddb08ce4116b`

```dockerfile
```

-	Layers:
	-	`sha256:8d4d502355fc2e5791b885a6085b1be30d92253ff54f3dcbe16443d754ca2728`  
		Last Modified: Tue, 13 Aug 2024 02:05:19 GMT  
		Size: 4.5 MB (4501253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:244183a49fc7df8d1eba76cd76f6b8ae48f8b8b9f0e9e516d759d604d423417c`  
		Last Modified: Tue, 13 Aug 2024 02:05:19 GMT  
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
$ docker pull influxdb@sha256:9f5e6e61b7cb7d193d04eca6e739533bd37cc5b7e6a894fe644090acfadd1577
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:6c036945aa4dec1f7d5964bf89bc6bd59f04341aaea7a110a66a84063e5481da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93400080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c36bc489f6155ce0e0b71b0dbe8eeccb90a3fe7f26021055ccdcddf002556c84`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 09 Aug 2024 17:32:24 GMT
ADD file:0d5bdf84bbcdfa95d42190537e3cad2c0a5876f9127fae6a1d1c485d3539c77d in / 
# Fri, 09 Aug 2024 17:32:24 GMT
CMD ["bash"]
# Fri, 09 Aug 2024 17:32:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 09 Aug 2024 17:32:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUXDB_VERSION=1.11.6-c1.11.6
# Fri, 09 Aug 2024 17:32:24 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
EXPOSE map[8091/tcp:{}]
# Fri, 09 Aug 2024 17:32:24 GMT
VOLUME [/var/lib/influxdb]
# Fri, 09 Aug 2024 17:32:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 09 Aug 2024 17:32:24 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:903681d87777d28dc56866a07a2774c3fd5bf65fd734b24c9d0ecd9a13c9f636`  
		Last Modified: Tue, 13 Aug 2024 00:23:26 GMT  
		Size: 49.6 MB (49554080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cbbe86a28c2f6b3c3e0e8c6dcfba369e1ea656cf8daf69be789e0fe2105982b`  
		Last Modified: Tue, 13 Aug 2024 00:49:47 GMT  
		Size: 24.1 MB (24050697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113d358eb6edd71a2e53cf41f22a348d9c3499c8601ec3fea72a36087c402563`  
		Last Modified: Tue, 13 Aug 2024 02:05:09 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa96fa3a890c6826aeecd42a0be37e9aee3ea27df5d24bf9add8c0400002168`  
		Last Modified: Tue, 13 Aug 2024 02:05:09 GMT  
		Size: 19.8 MB (19792961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846ee7855c17bb9b947c017faa117f9f785f4d36304742388a668090e898ffe5`  
		Last Modified: Tue, 13 Aug 2024 02:05:09 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa9919dc2aa123f3af79dc82e71d22fa4a82560fb750ff91dcca9f0863672ab`  
		Last Modified: Tue, 13 Aug 2024 02:05:09 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:499faf0d917497bcccc9a2728c8701dee572a39d5b22b198c39e019fb73a48c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4438926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be49d971a831188e7533ffdc4153c7ae0549cac00c46afb3699c8c333d536c48`

```dockerfile
```

-	Layers:
	-	`sha256:48a4c28032cd0cb2ab455843fdd0be672cf5d5b1388527bcc1a26132761c1f44`  
		Last Modified: Tue, 13 Aug 2024 02:05:09 GMT  
		Size: 4.4 MB (4426005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a771792ae944e75552f3d88c98a38c4157e9cb52e95ecc4447172eb0b27c027a`  
		Last Modified: Tue, 13 Aug 2024 02:05:09 GMT  
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
$ docker pull influxdb@sha256:d15f83bfdb8f9b22a40c86442e5ceb0ec63f19d061600dc5a430c639e50f4de3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.6-data` - linux; amd64

```console
$ docker pull influxdb@sha256:e659b59ba45125804b636cbb9182681fcc1b4923e271b28f85c68f2bb5b0a59d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114732704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1046c78ec3a11ff6d8896ac109b2d33e0533516f700974894661db24d19f0b6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 09 Aug 2024 17:32:24 GMT
ADD file:0d5bdf84bbcdfa95d42190537e3cad2c0a5876f9127fae6a1d1c485d3539c77d in / 
# Fri, 09 Aug 2024 17:32:24 GMT
CMD ["bash"]
# Fri, 09 Aug 2024 17:32:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 09 Aug 2024 17:32:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUXDB_VERSION=1.11.6-c1.11.6
# Fri, 09 Aug 2024 17:32:24 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 09 Aug 2024 17:32:24 GMT
VOLUME [/var/lib/influxdb]
# Fri, 09 Aug 2024 17:32:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 09 Aug 2024 17:32:24 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:903681d87777d28dc56866a07a2774c3fd5bf65fd734b24c9d0ecd9a13c9f636`  
		Last Modified: Tue, 13 Aug 2024 00:23:26 GMT  
		Size: 49.6 MB (49554080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cbbe86a28c2f6b3c3e0e8c6dcfba369e1ea656cf8daf69be789e0fe2105982b`  
		Last Modified: Tue, 13 Aug 2024 00:49:47 GMT  
		Size: 24.1 MB (24050697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb214b8f5f5e8956ad5ea8f980c9e6f56c5a9098d7e50d00a34c7792df23a79`  
		Last Modified: Tue, 13 Aug 2024 02:05:19 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6573d4aeb8df47ac73414c1a747d6e6e07756469db238cb0485eaac08ff4660b`  
		Last Modified: Tue, 13 Aug 2024 02:05:19 GMT  
		Size: 41.1 MB (41124377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5490dc6a9835356f1937e41e7e239a5fd5a76cc08362c0ae4de6c9dfd071b07`  
		Last Modified: Tue, 13 Aug 2024 02:05:19 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51790e06b4ef2b1bae56652a38c2cd0ddf9242cee2d24f74e926e3eacaa79173`  
		Last Modified: Tue, 13 Aug 2024 02:05:19 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e783ee95bfb4cfed880f3dc934887c227a5f1f6d6c6cb69a90fc833cd8ecf02`  
		Last Modified: Tue, 13 Aug 2024 02:05:20 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.6-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:02ddfbb6bcbee1d7c85555d822a389e9cfb946f576139a8a7169d121ad79aa6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4515827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce32357c2f36b19362969bd979d3665104a9bf874f63568c2e83ddb08ce4116b`

```dockerfile
```

-	Layers:
	-	`sha256:8d4d502355fc2e5791b885a6085b1be30d92253ff54f3dcbe16443d754ca2728`  
		Last Modified: Tue, 13 Aug 2024 02:05:19 GMT  
		Size: 4.5 MB (4501253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:244183a49fc7df8d1eba76cd76f6b8ae48f8b8b9f0e9e516d759d604d423417c`  
		Last Modified: Tue, 13 Aug 2024 02:05:19 GMT  
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
$ docker pull influxdb@sha256:9f5e6e61b7cb7d193d04eca6e739533bd37cc5b7e6a894fe644090acfadd1577
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.6-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:6c036945aa4dec1f7d5964bf89bc6bd59f04341aaea7a110a66a84063e5481da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93400080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c36bc489f6155ce0e0b71b0dbe8eeccb90a3fe7f26021055ccdcddf002556c84`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 09 Aug 2024 17:32:24 GMT
ADD file:0d5bdf84bbcdfa95d42190537e3cad2c0a5876f9127fae6a1d1c485d3539c77d in / 
# Fri, 09 Aug 2024 17:32:24 GMT
CMD ["bash"]
# Fri, 09 Aug 2024 17:32:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 09 Aug 2024 17:32:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUXDB_VERSION=1.11.6-c1.11.6
# Fri, 09 Aug 2024 17:32:24 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
EXPOSE map[8091/tcp:{}]
# Fri, 09 Aug 2024 17:32:24 GMT
VOLUME [/var/lib/influxdb]
# Fri, 09 Aug 2024 17:32:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 09 Aug 2024 17:32:24 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:903681d87777d28dc56866a07a2774c3fd5bf65fd734b24c9d0ecd9a13c9f636`  
		Last Modified: Tue, 13 Aug 2024 00:23:26 GMT  
		Size: 49.6 MB (49554080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cbbe86a28c2f6b3c3e0e8c6dcfba369e1ea656cf8daf69be789e0fe2105982b`  
		Last Modified: Tue, 13 Aug 2024 00:49:47 GMT  
		Size: 24.1 MB (24050697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113d358eb6edd71a2e53cf41f22a348d9c3499c8601ec3fea72a36087c402563`  
		Last Modified: Tue, 13 Aug 2024 02:05:09 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa96fa3a890c6826aeecd42a0be37e9aee3ea27df5d24bf9add8c0400002168`  
		Last Modified: Tue, 13 Aug 2024 02:05:09 GMT  
		Size: 19.8 MB (19792961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846ee7855c17bb9b947c017faa117f9f785f4d36304742388a668090e898ffe5`  
		Last Modified: Tue, 13 Aug 2024 02:05:09 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa9919dc2aa123f3af79dc82e71d22fa4a82560fb750ff91dcca9f0863672ab`  
		Last Modified: Tue, 13 Aug 2024 02:05:09 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.6-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:499faf0d917497bcccc9a2728c8701dee572a39d5b22b198c39e019fb73a48c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4438926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be49d971a831188e7533ffdc4153c7ae0549cac00c46afb3699c8c333d536c48`

```dockerfile
```

-	Layers:
	-	`sha256:48a4c28032cd0cb2ab455843fdd0be672cf5d5b1388527bcc1a26132761c1f44`  
		Last Modified: Tue, 13 Aug 2024 02:05:09 GMT  
		Size: 4.4 MB (4426005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a771792ae944e75552f3d88c98a38c4157e9cb52e95ecc4447172eb0b27c027a`  
		Last Modified: Tue, 13 Aug 2024 02:05:09 GMT  
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
$ docker pull influxdb@sha256:63ac4c2fc4a32935e64005cad337b2179c5088a14e63ca2a39df32ca2896f035
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
$ docker pull influxdb@sha256:a1cff51e969116db95524c76492de787f478df0c0b18e71377aa4907b7f671e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125737758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1a05be76ff56d25c6ec29b865f821487574de7ce0d341437520d58df809343`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 09 Aug 2024 17:32:24 GMT
ADD file:6648a8158bbf4a36244eb9e936fbed4ea29f2f090fb0a97a6a737be2d85a5333 in / 
# Fri, 09 Aug 2024 17:32:24 GMT
CMD ["bash"]
# Fri, 09 Aug 2024 17:32:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 09 Aug 2024 17:32:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUXDB_VERSION=1.8.10
# Fri, 09 Aug 2024 17:32:24 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb* # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 09 Aug 2024 17:32:24 GMT
VOLUME [/var/lib/influxdb]
# Fri, 09 Aug 2024 17:32:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 09 Aug 2024 17:32:24 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:203e9cf21bd27322e5baf32653bf3314ccf688be497585240d18b9f0ca24f2ee`  
		Last Modified: Tue, 13 Aug 2024 00:24:05 GMT  
		Size: 55.1 MB (55084675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3438c04e457d7cf49dfbfe92aa9c64df2c0d9dc8ac53a7dbda0c620c405d9f`  
		Last Modified: Tue, 13 Aug 2024 00:50:52 GMT  
		Size: 15.8 MB (15764253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fae74047f53df5d19dc67e64abdc40dc350d03d4f623ad3ec325f220bc3021d`  
		Last Modified: Tue, 13 Aug 2024 02:05:09 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd282ef883380123d5ca12fe4d2e74a153c98c7206c8497a83586adf44e54f4`  
		Last Modified: Tue, 13 Aug 2024 02:05:10 GMT  
		Size: 54.9 MB (54885341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f33e3f1fd11e4759ac2a66019a524d7d823a7f22292f50b8947a0a8e3f5436d`  
		Last Modified: Tue, 13 Aug 2024 02:05:09 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581165bc35a7c883119e28149510eec63d64c21127e5925ce9ce4a3abc47e048`  
		Last Modified: Tue, 13 Aug 2024 02:05:09 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8e1898a057428b1c3b985d25177d994576aeea179d9e5cfd8d77ea8950729f`  
		Last Modified: Tue, 13 Aug 2024 02:05:08 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:441aa239ca2b0966c30d39a39e81f10320fa508f57792efb11bde669e47e0c10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4505064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c566beb429a5f29db96b1e530e9f3b889136ff147401b8985bef1c99d041825d`

```dockerfile
```

-	Layers:
	-	`sha256:09227b8d9743c512ed6a993f7fd56d33903a1ad5ba7f99de6c6b6d33565565b9`  
		Last Modified: Tue, 13 Aug 2024 02:05:09 GMT  
		Size: 4.5 MB (4489602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72b6ffd30ea57a587062c110ef88c411ef6bbce2093916fc81be8dc99287c5db`  
		Last Modified: Tue, 13 Aug 2024 02:05:09 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.8` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:0ecba43dd90df9068cb2cff3a87013e000fd11bf72333b89f752ed14ff60e68f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.7 MB (116738225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78f94e9c4d07808f88c500aaa483bbfa199642b9aef14e74df8aabbf96fa1d03`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 09 Aug 2024 17:32:24 GMT
ADD file:7674761630f1c6dfdf95da576bd19dbfe7bc4d942d11d31eff2012ec8b2c7ff1 in / 
# Fri, 09 Aug 2024 17:32:24 GMT
CMD ["bash"]
# Fri, 09 Aug 2024 17:32:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 09 Aug 2024 17:32:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUXDB_VERSION=1.8.10
# Fri, 09 Aug 2024 17:32:24 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb* # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 09 Aug 2024 17:32:24 GMT
VOLUME [/var/lib/influxdb]
# Fri, 09 Aug 2024 17:32:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 09 Aug 2024 17:32:24 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:a986643b6b9d356e3c44ee35fdd352a1064e1fb2a1524c0627e84ba34207b8e2`  
		Last Modified: Tue, 13 Aug 2024 01:01:15 GMT  
		Size: 50.2 MB (50242333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8868560f8e978ee832f67027b7330376be350ffacd30a199b730c72d9550757`  
		Last Modified: Tue, 13 Aug 2024 01:33:28 GMT  
		Size: 14.9 MB (14879497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f31635f0fcf4e0331f67eeeba7e57aa6cf7366ffefcf61ba16ef7bc06cc1faba`  
		Last Modified: Tue, 13 Aug 2024 11:50:08 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06cf2b45553f3c8081d5912ff91000d9975ff6023c73fdc2c7426a1bd5258f54`  
		Last Modified: Tue, 13 Aug 2024 11:50:10 GMT  
		Size: 51.6 MB (51612894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377e7763146cdf6e1224a17b276412c4a0b32a877ecd22a2634f96759d85ceb4`  
		Last Modified: Tue, 13 Aug 2024 11:50:08 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb8bf6f763c5f27da3393789a1e7bd8d56504694546bed3e13cf64efb017341`  
		Last Modified: Tue, 13 Aug 2024 11:50:08 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2106b6c748e77694c282a77ad7f8b1288ce7570d178056e3df0903f5ba151ad9`  
		Last Modified: Tue, 13 Aug 2024 11:50:09 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:c6e179c7659f699f4c7d86997821c2aec8c529b2bc6485425db50f189765c665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4506765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6366688d1dcc1e9160737661e9342e974ef9cdf7aed0a7d5585b691287e02cb0`

```dockerfile
```

-	Layers:
	-	`sha256:c32cffb3b45a0815cf6045f75b647a8208ddadea3382d410628ff00dcf4bf29c`  
		Last Modified: Tue, 13 Aug 2024 11:50:09 GMT  
		Size: 4.5 MB (4491236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba52ad2a12aa381560bdce33abb7a38fb9882f50bca5415ea25801da3a256b3d`  
		Last Modified: Tue, 13 Aug 2024 11:50:08 GMT  
		Size: 15.5 KB (15529 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:e05fded0caceaa58d466474301af730a4b47af9507685e9ad5989b3133384554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120712808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:622da13a9d35e0bc9564d071923ed9237e595a17b524d08aaf9376e7f25d83bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 09 Aug 2024 17:32:24 GMT
ADD file:4a2aa1b23402547c558d14f98384342f2e98460b659cd211609373f5408e83bc in / 
# Fri, 09 Aug 2024 17:32:24 GMT
CMD ["bash"]
# Fri, 09 Aug 2024 17:32:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 09 Aug 2024 17:32:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUXDB_VERSION=1.8.10
# Fri, 09 Aug 2024 17:32:24 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb* # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 09 Aug 2024 17:32:24 GMT
VOLUME [/var/lib/influxdb]
# Fri, 09 Aug 2024 17:32:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 09 Aug 2024 17:32:24 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:5d8903d6126c38fefcb1196b9998da0798f56cbdf18a91c00d822144c232af6b`  
		Last Modified: Tue, 13 Aug 2024 00:43:03 GMT  
		Size: 53.7 MB (53729921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3db3ee6245513b1422983db21d89f4f743f300e726af9eff6c9f7e2dddcb67`  
		Last Modified: Tue, 13 Aug 2024 01:10:18 GMT  
		Size: 15.7 MB (15749505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e759fbe1698327dfd0561ff1d9145828a5d611511b46dd571379350f1f060d2`  
		Last Modified: Tue, 13 Aug 2024 16:06:54 GMT  
		Size: 1.8 KB (1780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77df2e180567e6ced3ca591a1e71cbc114eddb9d9aa29f222a7ac5d4e577dfc9`  
		Last Modified: Tue, 13 Aug 2024 16:06:56 GMT  
		Size: 51.2 MB (51229882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13037daa21218c05d94c7ca2201c8347f1c393bcebce32d178d4b4f89ccb3b54`  
		Last Modified: Tue, 13 Aug 2024 16:06:54 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fbe410f7a47050b7bc53eac06111f0c35f7eff75c6ebf020510d4a78134ce1`  
		Last Modified: Tue, 13 Aug 2024 16:06:54 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c3b0e4c58bb7f5765e1b58730f6e2f51d9b83c38432f4bc9adaf271bba8921`  
		Last Modified: Tue, 13 Aug 2024 16:06:55 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:0d9fda79bc8b3ee6b05c4640309d357f504aebf98912f73a997655238e55a883
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4504969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8618b442caf22c279af0391cd9fd239f40abdb60371a9ba4682ec8ff2ad22c00`

```dockerfile
```

-	Layers:
	-	`sha256:ee7d9137457a563d80b4a703fd0fd381ac91b65a7ce7bcdc5095e853095ce077`  
		Last Modified: Tue, 13 Aug 2024 16:06:55 GMT  
		Size: 4.5 MB (4489214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f40dc13d31f013a8dbefe252a59155fceaf13a14125ce652686150439615ec0`  
		Last Modified: Tue, 13 Aug 2024 16:06:54 GMT  
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
$ docker pull influxdb@sha256:63ac4c2fc4a32935e64005cad337b2179c5088a14e63ca2a39df32ca2896f035
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
$ docker pull influxdb@sha256:a1cff51e969116db95524c76492de787f478df0c0b18e71377aa4907b7f671e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125737758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1a05be76ff56d25c6ec29b865f821487574de7ce0d341437520d58df809343`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 09 Aug 2024 17:32:24 GMT
ADD file:6648a8158bbf4a36244eb9e936fbed4ea29f2f090fb0a97a6a737be2d85a5333 in / 
# Fri, 09 Aug 2024 17:32:24 GMT
CMD ["bash"]
# Fri, 09 Aug 2024 17:32:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 09 Aug 2024 17:32:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUXDB_VERSION=1.8.10
# Fri, 09 Aug 2024 17:32:24 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb* # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 09 Aug 2024 17:32:24 GMT
VOLUME [/var/lib/influxdb]
# Fri, 09 Aug 2024 17:32:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 09 Aug 2024 17:32:24 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:203e9cf21bd27322e5baf32653bf3314ccf688be497585240d18b9f0ca24f2ee`  
		Last Modified: Tue, 13 Aug 2024 00:24:05 GMT  
		Size: 55.1 MB (55084675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3438c04e457d7cf49dfbfe92aa9c64df2c0d9dc8ac53a7dbda0c620c405d9f`  
		Last Modified: Tue, 13 Aug 2024 00:50:52 GMT  
		Size: 15.8 MB (15764253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fae74047f53df5d19dc67e64abdc40dc350d03d4f623ad3ec325f220bc3021d`  
		Last Modified: Tue, 13 Aug 2024 02:05:09 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd282ef883380123d5ca12fe4d2e74a153c98c7206c8497a83586adf44e54f4`  
		Last Modified: Tue, 13 Aug 2024 02:05:10 GMT  
		Size: 54.9 MB (54885341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f33e3f1fd11e4759ac2a66019a524d7d823a7f22292f50b8947a0a8e3f5436d`  
		Last Modified: Tue, 13 Aug 2024 02:05:09 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581165bc35a7c883119e28149510eec63d64c21127e5925ce9ce4a3abc47e048`  
		Last Modified: Tue, 13 Aug 2024 02:05:09 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8e1898a057428b1c3b985d25177d994576aeea179d9e5cfd8d77ea8950729f`  
		Last Modified: Tue, 13 Aug 2024 02:05:08 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8.10` - unknown; unknown

```console
$ docker pull influxdb@sha256:441aa239ca2b0966c30d39a39e81f10320fa508f57792efb11bde669e47e0c10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4505064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c566beb429a5f29db96b1e530e9f3b889136ff147401b8985bef1c99d041825d`

```dockerfile
```

-	Layers:
	-	`sha256:09227b8d9743c512ed6a993f7fd56d33903a1ad5ba7f99de6c6b6d33565565b9`  
		Last Modified: Tue, 13 Aug 2024 02:05:09 GMT  
		Size: 4.5 MB (4489602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72b6ffd30ea57a587062c110ef88c411ef6bbce2093916fc81be8dc99287c5db`  
		Last Modified: Tue, 13 Aug 2024 02:05:09 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.8.10` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:0ecba43dd90df9068cb2cff3a87013e000fd11bf72333b89f752ed14ff60e68f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.7 MB (116738225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78f94e9c4d07808f88c500aaa483bbfa199642b9aef14e74df8aabbf96fa1d03`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 09 Aug 2024 17:32:24 GMT
ADD file:7674761630f1c6dfdf95da576bd19dbfe7bc4d942d11d31eff2012ec8b2c7ff1 in / 
# Fri, 09 Aug 2024 17:32:24 GMT
CMD ["bash"]
# Fri, 09 Aug 2024 17:32:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 09 Aug 2024 17:32:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUXDB_VERSION=1.8.10
# Fri, 09 Aug 2024 17:32:24 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb* # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 09 Aug 2024 17:32:24 GMT
VOLUME [/var/lib/influxdb]
# Fri, 09 Aug 2024 17:32:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 09 Aug 2024 17:32:24 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:a986643b6b9d356e3c44ee35fdd352a1064e1fb2a1524c0627e84ba34207b8e2`  
		Last Modified: Tue, 13 Aug 2024 01:01:15 GMT  
		Size: 50.2 MB (50242333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8868560f8e978ee832f67027b7330376be350ffacd30a199b730c72d9550757`  
		Last Modified: Tue, 13 Aug 2024 01:33:28 GMT  
		Size: 14.9 MB (14879497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f31635f0fcf4e0331f67eeeba7e57aa6cf7366ffefcf61ba16ef7bc06cc1faba`  
		Last Modified: Tue, 13 Aug 2024 11:50:08 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06cf2b45553f3c8081d5912ff91000d9975ff6023c73fdc2c7426a1bd5258f54`  
		Last Modified: Tue, 13 Aug 2024 11:50:10 GMT  
		Size: 51.6 MB (51612894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377e7763146cdf6e1224a17b276412c4a0b32a877ecd22a2634f96759d85ceb4`  
		Last Modified: Tue, 13 Aug 2024 11:50:08 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb8bf6f763c5f27da3393789a1e7bd8d56504694546bed3e13cf64efb017341`  
		Last Modified: Tue, 13 Aug 2024 11:50:08 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2106b6c748e77694c282a77ad7f8b1288ce7570d178056e3df0903f5ba151ad9`  
		Last Modified: Tue, 13 Aug 2024 11:50:09 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8.10` - unknown; unknown

```console
$ docker pull influxdb@sha256:c6e179c7659f699f4c7d86997821c2aec8c529b2bc6485425db50f189765c665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4506765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6366688d1dcc1e9160737661e9342e974ef9cdf7aed0a7d5585b691287e02cb0`

```dockerfile
```

-	Layers:
	-	`sha256:c32cffb3b45a0815cf6045f75b647a8208ddadea3382d410628ff00dcf4bf29c`  
		Last Modified: Tue, 13 Aug 2024 11:50:09 GMT  
		Size: 4.5 MB (4491236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba52ad2a12aa381560bdce33abb7a38fb9882f50bca5415ea25801da3a256b3d`  
		Last Modified: Tue, 13 Aug 2024 11:50:08 GMT  
		Size: 15.5 KB (15529 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.8.10` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:e05fded0caceaa58d466474301af730a4b47af9507685e9ad5989b3133384554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120712808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:622da13a9d35e0bc9564d071923ed9237e595a17b524d08aaf9376e7f25d83bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 09 Aug 2024 17:32:24 GMT
ADD file:4a2aa1b23402547c558d14f98384342f2e98460b659cd211609373f5408e83bc in / 
# Fri, 09 Aug 2024 17:32:24 GMT
CMD ["bash"]
# Fri, 09 Aug 2024 17:32:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 09 Aug 2024 17:32:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUXDB_VERSION=1.8.10
# Fri, 09 Aug 2024 17:32:24 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb* # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 09 Aug 2024 17:32:24 GMT
VOLUME [/var/lib/influxdb]
# Fri, 09 Aug 2024 17:32:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 09 Aug 2024 17:32:24 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:5d8903d6126c38fefcb1196b9998da0798f56cbdf18a91c00d822144c232af6b`  
		Last Modified: Tue, 13 Aug 2024 00:43:03 GMT  
		Size: 53.7 MB (53729921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3db3ee6245513b1422983db21d89f4f743f300e726af9eff6c9f7e2dddcb67`  
		Last Modified: Tue, 13 Aug 2024 01:10:18 GMT  
		Size: 15.7 MB (15749505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e759fbe1698327dfd0561ff1d9145828a5d611511b46dd571379350f1f060d2`  
		Last Modified: Tue, 13 Aug 2024 16:06:54 GMT  
		Size: 1.8 KB (1780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77df2e180567e6ced3ca591a1e71cbc114eddb9d9aa29f222a7ac5d4e577dfc9`  
		Last Modified: Tue, 13 Aug 2024 16:06:56 GMT  
		Size: 51.2 MB (51229882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13037daa21218c05d94c7ca2201c8347f1c393bcebce32d178d4b4f89ccb3b54`  
		Last Modified: Tue, 13 Aug 2024 16:06:54 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fbe410f7a47050b7bc53eac06111f0c35f7eff75c6ebf020510d4a78134ce1`  
		Last Modified: Tue, 13 Aug 2024 16:06:54 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c3b0e4c58bb7f5765e1b58730f6e2f51d9b83c38432f4bc9adaf271bba8921`  
		Last Modified: Tue, 13 Aug 2024 16:06:55 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8.10` - unknown; unknown

```console
$ docker pull influxdb@sha256:0d9fda79bc8b3ee6b05c4640309d357f504aebf98912f73a997655238e55a883
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4504969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8618b442caf22c279af0391cd9fd239f40abdb60371a9ba4682ec8ff2ad22c00`

```dockerfile
```

-	Layers:
	-	`sha256:ee7d9137457a563d80b4a703fd0fd381ac91b65a7ce7bcdc5095e853095ce077`  
		Last Modified: Tue, 13 Aug 2024 16:06:55 GMT  
		Size: 4.5 MB (4489214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f40dc13d31f013a8dbefe252a59155fceaf13a14125ce652686150439615ec0`  
		Last Modified: Tue, 13 Aug 2024 16:06:54 GMT  
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
$ docker pull influxdb@sha256:b45c47ad6f423e9446601c571f42926f19d4985e6fa02e28ccc5d2b6a83932ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9-data` - linux; amd64

```console
$ docker pull influxdb@sha256:d3171bcfdb939328bb7392aaec90ae16143b9db97c24eba3c2e5088b6f3e10a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104141447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e094eba8aca79cd14f81d29f488d2602591ba1a3093ab7911b43cddb6d023a51`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 09 Aug 2024 17:32:24 GMT
ADD file:6648a8158bbf4a36244eb9e936fbed4ea29f2f090fb0a97a6a737be2d85a5333 in / 
# Fri, 09 Aug 2024 17:32:24 GMT
CMD ["bash"]
# Fri, 09 Aug 2024 17:32:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 09 Aug 2024 17:32:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Fri, 09 Aug 2024 17:32:24 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb* # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 09 Aug 2024 17:32:24 GMT
VOLUME [/var/lib/influxdb]
# Fri, 09 Aug 2024 17:32:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 09 Aug 2024 17:32:24 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:203e9cf21bd27322e5baf32653bf3314ccf688be497585240d18b9f0ca24f2ee`  
		Last Modified: Tue, 13 Aug 2024 00:24:05 GMT  
		Size: 55.1 MB (55084675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3438c04e457d7cf49dfbfe92aa9c64df2c0d9dc8ac53a7dbda0c620c405d9f`  
		Last Modified: Tue, 13 Aug 2024 00:50:52 GMT  
		Size: 15.8 MB (15764253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868fe916c54f53a9edd43413823d53065adef7185714a0bf94182c2592d243f9`  
		Last Modified: Tue, 13 Aug 2024 02:05:07 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee1083a4dffcc4671a92e74326e24ffa7f61925d23de8f929be1f259f95d681`  
		Last Modified: Tue, 13 Aug 2024 02:05:08 GMT  
		Size: 33.3 MB (33288971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15d69d1edfa5b052f8a31e9f8b95c111af89aae830ede54d3aa6f1469910de8`  
		Last Modified: Tue, 13 Aug 2024 02:05:07 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42fcc6f3c6c29a8712d06b198c31960dbdc118e7cdd90c5d4601740c0cd1e92`  
		Last Modified: Tue, 13 Aug 2024 02:05:08 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8e1898a057428b1c3b985d25177d994576aeea179d9e5cfd8d77ea8950729f`  
		Last Modified: Tue, 13 Aug 2024 02:05:08 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:90c5d30d3c85347ada43928bb60e3a238827bb0b734454baa1aa3c38a30b9fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4631024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1baa985d1ef2ffc707309dc793a22b6fd2be4dfee5edfb55b888540ebe5b6f7`

```dockerfile
```

-	Layers:
	-	`sha256:2153e1bfe3a362fa8cd17378cb8633d0797dc193e49cd028b74acdb8e35fb1c2`  
		Last Modified: Tue, 13 Aug 2024 02:05:07 GMT  
		Size: 4.6 MB (4616483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:811dbd389dd450e434304a62bc71d2136cf8e9e61fbe344f3c0287f75bc31476`  
		Last Modified: Tue, 13 Aug 2024 02:05:07 GMT  
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
$ docker pull influxdb@sha256:6ff6582942b9d2195886b782cb0fbc7f646cc5af77a0efb627bf76060a251d41
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:457b022c7a4c38974f512ebd3e1069497f35610f85a9fff02f8c049f98b94888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83620650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbeda1e35fb1b0ea34841d0d925a515677fa659d6dea7c09fde191b7028a2c11`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 09 Aug 2024 17:32:24 GMT
ADD file:6648a8158bbf4a36244eb9e936fbed4ea29f2f090fb0a97a6a737be2d85a5333 in / 
# Fri, 09 Aug 2024 17:32:24 GMT
CMD ["bash"]
# Fri, 09 Aug 2024 17:32:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 09 Aug 2024 17:32:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Fri, 09 Aug 2024 17:32:24 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb* # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
EXPOSE map[8091/tcp:{}]
# Fri, 09 Aug 2024 17:32:24 GMT
VOLUME [/var/lib/influxdb]
# Fri, 09 Aug 2024 17:32:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 09 Aug 2024 17:32:24 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:203e9cf21bd27322e5baf32653bf3314ccf688be497585240d18b9f0ca24f2ee`  
		Last Modified: Tue, 13 Aug 2024 00:24:05 GMT  
		Size: 55.1 MB (55084675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3438c04e457d7cf49dfbfe92aa9c64df2c0d9dc8ac53a7dbda0c620c405d9f`  
		Last Modified: Tue, 13 Aug 2024 00:50:52 GMT  
		Size: 15.8 MB (15764253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605423f9bda2c4757dbbe8e60c8bdf268a1e4d84225a8ba216c598e2a1876d2c`  
		Last Modified: Tue, 13 Aug 2024 02:05:15 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3441f95c94df76544bf146be67682eb1e008ede365f64807ca921238665324a2`  
		Last Modified: Tue, 13 Aug 2024 02:05:16 GMT  
		Size: 12.8 MB (12769371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024c3dcfa5f4547f794183b81f5b751ee61d58bb217f96f7a6e57e72cea054de`  
		Last Modified: Tue, 13 Aug 2024 02:05:16 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf67fab00a409b9160b1f78ab3ed9cfad0c64834a185e2d1e72e67e1f0503848`  
		Last Modified: Tue, 13 Aug 2024 02:05:16 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:1c3df78615aa949f99fb3828ea5bc0f9f7f37f987ca6acbf6ec9d6ccab62522d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4565204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bfd9c389135a3efb2b5ee4cc0393ecc2ba541c489b14f6c9d9c9ab23513c9ee`

```dockerfile
```

-	Layers:
	-	`sha256:3861ebfb16cf5ef0dcbc002368d1aa0c76c621980cffd3f143f372eae466183f`  
		Last Modified: Tue, 13 Aug 2024 02:05:16 GMT  
		Size: 4.6 MB (4552316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e37bee4a611775cef6b0d75aaf11b5d330b1e8be08a8811ea1fde7e0a7647d3`  
		Last Modified: Tue, 13 Aug 2024 02:05:15 GMT  
		Size: 12.9 KB (12888 bytes)  
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
$ docker pull influxdb@sha256:b45c47ad6f423e9446601c571f42926f19d4985e6fa02e28ccc5d2b6a83932ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9.13-data` - linux; amd64

```console
$ docker pull influxdb@sha256:d3171bcfdb939328bb7392aaec90ae16143b9db97c24eba3c2e5088b6f3e10a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104141447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e094eba8aca79cd14f81d29f488d2602591ba1a3093ab7911b43cddb6d023a51`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 09 Aug 2024 17:32:24 GMT
ADD file:6648a8158bbf4a36244eb9e936fbed4ea29f2f090fb0a97a6a737be2d85a5333 in / 
# Fri, 09 Aug 2024 17:32:24 GMT
CMD ["bash"]
# Fri, 09 Aug 2024 17:32:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 09 Aug 2024 17:32:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Fri, 09 Aug 2024 17:32:24 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb* # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 09 Aug 2024 17:32:24 GMT
VOLUME [/var/lib/influxdb]
# Fri, 09 Aug 2024 17:32:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 09 Aug 2024 17:32:24 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:203e9cf21bd27322e5baf32653bf3314ccf688be497585240d18b9f0ca24f2ee`  
		Last Modified: Tue, 13 Aug 2024 00:24:05 GMT  
		Size: 55.1 MB (55084675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3438c04e457d7cf49dfbfe92aa9c64df2c0d9dc8ac53a7dbda0c620c405d9f`  
		Last Modified: Tue, 13 Aug 2024 00:50:52 GMT  
		Size: 15.8 MB (15764253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868fe916c54f53a9edd43413823d53065adef7185714a0bf94182c2592d243f9`  
		Last Modified: Tue, 13 Aug 2024 02:05:07 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee1083a4dffcc4671a92e74326e24ffa7f61925d23de8f929be1f259f95d681`  
		Last Modified: Tue, 13 Aug 2024 02:05:08 GMT  
		Size: 33.3 MB (33288971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15d69d1edfa5b052f8a31e9f8b95c111af89aae830ede54d3aa6f1469910de8`  
		Last Modified: Tue, 13 Aug 2024 02:05:07 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42fcc6f3c6c29a8712d06b198c31960dbdc118e7cdd90c5d4601740c0cd1e92`  
		Last Modified: Tue, 13 Aug 2024 02:05:08 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8e1898a057428b1c3b985d25177d994576aeea179d9e5cfd8d77ea8950729f`  
		Last Modified: Tue, 13 Aug 2024 02:05:08 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9.13-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:90c5d30d3c85347ada43928bb60e3a238827bb0b734454baa1aa3c38a30b9fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4631024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1baa985d1ef2ffc707309dc793a22b6fd2be4dfee5edfb55b888540ebe5b6f7`

```dockerfile
```

-	Layers:
	-	`sha256:2153e1bfe3a362fa8cd17378cb8633d0797dc193e49cd028b74acdb8e35fb1c2`  
		Last Modified: Tue, 13 Aug 2024 02:05:07 GMT  
		Size: 4.6 MB (4616483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:811dbd389dd450e434304a62bc71d2136cf8e9e61fbe344f3c0287f75bc31476`  
		Last Modified: Tue, 13 Aug 2024 02:05:07 GMT  
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
$ docker pull influxdb@sha256:6ff6582942b9d2195886b782cb0fbc7f646cc5af77a0efb627bf76060a251d41
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9.13-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:457b022c7a4c38974f512ebd3e1069497f35610f85a9fff02f8c049f98b94888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83620650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbeda1e35fb1b0ea34841d0d925a515677fa659d6dea7c09fde191b7028a2c11`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 09 Aug 2024 17:32:24 GMT
ADD file:6648a8158bbf4a36244eb9e936fbed4ea29f2f090fb0a97a6a737be2d85a5333 in / 
# Fri, 09 Aug 2024 17:32:24 GMT
CMD ["bash"]
# Fri, 09 Aug 2024 17:32:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 09 Aug 2024 17:32:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Fri, 09 Aug 2024 17:32:24 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb* # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
EXPOSE map[8091/tcp:{}]
# Fri, 09 Aug 2024 17:32:24 GMT
VOLUME [/var/lib/influxdb]
# Fri, 09 Aug 2024 17:32:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 09 Aug 2024 17:32:24 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:203e9cf21bd27322e5baf32653bf3314ccf688be497585240d18b9f0ca24f2ee`  
		Last Modified: Tue, 13 Aug 2024 00:24:05 GMT  
		Size: 55.1 MB (55084675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3438c04e457d7cf49dfbfe92aa9c64df2c0d9dc8ac53a7dbda0c620c405d9f`  
		Last Modified: Tue, 13 Aug 2024 00:50:52 GMT  
		Size: 15.8 MB (15764253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605423f9bda2c4757dbbe8e60c8bdf268a1e4d84225a8ba216c598e2a1876d2c`  
		Last Modified: Tue, 13 Aug 2024 02:05:15 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3441f95c94df76544bf146be67682eb1e008ede365f64807ca921238665324a2`  
		Last Modified: Tue, 13 Aug 2024 02:05:16 GMT  
		Size: 12.8 MB (12769371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024c3dcfa5f4547f794183b81f5b751ee61d58bb217f96f7a6e57e72cea054de`  
		Last Modified: Tue, 13 Aug 2024 02:05:16 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf67fab00a409b9160b1f78ab3ed9cfad0c64834a185e2d1e72e67e1f0503848`  
		Last Modified: Tue, 13 Aug 2024 02:05:16 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9.13-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:1c3df78615aa949f99fb3828ea5bc0f9f7f37f987ca6acbf6ec9d6ccab62522d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4565204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bfd9c389135a3efb2b5ee4cc0393ecc2ba541c489b14f6c9d9c9ab23513c9ee`

```dockerfile
```

-	Layers:
	-	`sha256:3861ebfb16cf5ef0dcbc002368d1aa0c76c621980cffd3f143f372eae466183f`  
		Last Modified: Tue, 13 Aug 2024 02:05:16 GMT  
		Size: 4.6 MB (4552316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e37bee4a611775cef6b0d75aaf11b5d330b1e8be08a8811ea1fde7e0a7647d3`  
		Last Modified: Tue, 13 Aug 2024 02:05:15 GMT  
		Size: 12.9 KB (12888 bytes)  
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
$ docker pull influxdb@sha256:52b002a758ccc33d0ddb8ac006823fe8b5a9a1277338046a9976fabe98d4d13b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2` - linux; amd64

```console
$ docker pull influxdb@sha256:067bd997ad1dbc62a77b5076fd5779d9f50d9bcc7eb32ec6ae28d93f9e1ed752
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168476549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58bdeea2b858ea26080e1377571c587f2d790fb09e598747d7d99a4efaf65322`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 09 Aug 2024 17:32:24 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Fri, 09 Aug 2024 17:32:24 GMT
CMD ["bash"]
# Fri, 09 Aug 2024 17:32:24 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENV GOSU_VER=1.16
# Fri, 09 Aug 2024 17:32:24 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUXDB_VERSION=2.7.9
# Fri, 09 Aug 2024 17:32:24 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Fri, 09 Aug 2024 17:32:24 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 09 Aug 2024 17:32:24 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 09 Aug 2024 17:32:24 GMT
CMD ["influxd"]
# Fri, 09 Aug 2024 17:32:24 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 09 Aug 2024 17:32:24 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb66f32b72131e4dbe8a37fa0fdcae3f2403ced6d15fd68128cfdb31df9d105d`  
		Last Modified: Tue, 13 Aug 2024 01:18:22 GMT  
		Size: 9.8 MB (9786136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffffb3badc7145e237597d807220c68b3b99d8f8f7b0f8698cfa16e59a6832c0`  
		Last Modified: Tue, 13 Aug 2024 01:18:22 GMT  
		Size: 5.8 MB (5820938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e805ddd5f740b452df1f5aa8709acf7c8cfe05e1bbecbdb66ca23dfee6f1b6c7`  
		Last Modified: Tue, 13 Aug 2024 01:18:22 GMT  
		Size: 3.2 KB (3224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5182142bbb3d4cd9f0842ce4a47558bf5a347ccde155b639b4900f57b005db7d`  
		Last Modified: Tue, 13 Aug 2024 01:18:22 GMT  
		Size: 1.0 MB (1006370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae5bdb75813050ac227d3c05e8c221bb60c3c320e4e7999666c7a9409812055`  
		Last Modified: Tue, 13 Aug 2024 01:18:24 GMT  
		Size: 99.6 MB (99598615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92d2f549099f782f689c6dc40d89515db96f2f046bb3b68faa974ebf2df63c4`  
		Last Modified: Tue, 13 Aug 2024 01:18:23 GMT  
		Size: 23.1 MB (23128307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3259b34ea6a5547bae58cfcdd7b22477f94e69861eb0b81d95358344d2b4146`  
		Last Modified: Tue, 13 Aug 2024 01:18:23 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da3072f071ac90de49cd981e143bd59b095e6aa59d05f79f59bf8b4143814f0`  
		Last Modified: Tue, 13 Aug 2024 01:18:23 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49fc83331c9f60f2976426e18c83e370022992ac27c682223d6872c1813dcc52`  
		Last Modified: Tue, 13 Aug 2024 01:18:23 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:e12889f12dde15ed974d64f6d2a55d8f5dfa884b16c67e39e4e6951921468fa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:947bc2abfa72fb85868df0f0899a1cf183797a5aa22d917e513dcee701dd0ff9`

```dockerfile
```

-	Layers:
	-	`sha256:9d3c0316d99ae11edb762b105c2bba8a91bd8d84000bd36999781fa422d23971`  
		Last Modified: Tue, 13 Aug 2024 01:18:22 GMT  
		Size: 2.8 MB (2833438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee48b73455f9d44f3bdd1f1cec8cd2ca4567dfefec7105826dc35e1dd5db1a21`  
		Last Modified: Tue, 13 Aug 2024 01:18:22 GMT  
		Size: 33.5 KB (33540 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:38c90c641a28bed8d1c06cf9e73e8ebc7bb759bcbebf24c9787dd8d2fd977826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162251582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e98a9ac2dfe717bd84cd9069d0e67aebfbd61b0842c7293fd1f3cb949ea133`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 09 Aug 2024 17:32:24 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Fri, 09 Aug 2024 17:32:24 GMT
CMD ["bash"]
# Fri, 09 Aug 2024 17:32:24 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENV GOSU_VER=1.16
# Fri, 09 Aug 2024 17:32:24 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUXDB_VERSION=2.7.9
# Fri, 09 Aug 2024 17:32:24 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Fri, 09 Aug 2024 17:32:24 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 09 Aug 2024 17:32:24 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 09 Aug 2024 17:32:24 GMT
CMD ["influxd"]
# Fri, 09 Aug 2024 17:32:24 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 09 Aug 2024 17:32:24 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af8cd4147de7f78511d80ebd168ada550c516bc7b7ed15865aa5a32fbd733089`  
		Last Modified: Tue, 13 Aug 2024 07:21:58 GMT  
		Size: 9.6 MB (9585117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53bc08419b6bfeb1324aa33ae3db2694f2fc8584e5ca8cb0ce38b69722e84d7`  
		Last Modified: Tue, 13 Aug 2024 07:21:58 GMT  
		Size: 5.5 MB (5463786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb2629f78b117ded6b2a6c524416ae254383a1d7873b717c9117221549b859e`  
		Last Modified: Tue, 13 Aug 2024 07:21:58 GMT  
		Size: 3.2 KB (3226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8380d9c1dfee9401788143d4b533d97220b95afb5290f5fc52e1a0392b86c8`  
		Last Modified: Tue, 13 Aug 2024 07:21:58 GMT  
		Size: 936.1 KB (936111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887263e189946abfbbdd9aeba3f901d1ab04fae88c5b0cfbd8362b526fc493d8`  
		Last Modified: Tue, 13 Aug 2024 07:22:01 GMT  
		Size: 95.4 MB (95437568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa25a5c69d1ffd85fa21abcf0d7b738136c9ef9dac31bece7b089542663593f`  
		Last Modified: Tue, 13 Aug 2024 07:22:00 GMT  
		Size: 21.7 MB (21662519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddce16abef94acc9b3beb7ba2d70c053d3fe91393f3122eedb9de5c90b41821d`  
		Last Modified: Tue, 13 Aug 2024 07:21:59 GMT  
		Size: 207.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3db895c0f8393c87eac4a7e6f76a587ca7c07b4d021038189266130c2a23e32`  
		Last Modified: Tue, 13 Aug 2024 07:22:00 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f26c0696526948b6a0e0d4c5b94469566baae900b49922fbe2d11b0b282c031`  
		Last Modified: Tue, 13 Aug 2024 07:22:00 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:1591961c61dbf849630bc9fb76c0a36602a1aaf45ce41cd9de67d7f11a99cd81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a907c57d223f8c2b09edfbb904aa6edbbc5ce8f56133affaaf98540a4f3edf7b`

```dockerfile
```

-	Layers:
	-	`sha256:aa94f2b9189325067e7127dc36b448a6a1a91b14535cc733af2f59f4c961dd1e`  
		Last Modified: Tue, 13 Aug 2024 07:21:58 GMT  
		Size: 2.8 MB (2832675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b639136a991ad8af0a7d68223a4669ff95935dfab68f7399973cd728b4e40ec3`  
		Last Modified: Tue, 13 Aug 2024 07:21:58 GMT  
		Size: 33.8 KB (33843 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2-alpine`

```console
$ docker pull influxdb@sha256:82ad20cfcb42ef800a31977d2e38debe6cdbf97160a6ea2155f7b56e0e3a431b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:98372aea3611142e87695dfd7e9d2b3cc3ff2e578f20af3de6c12c9320e50de3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (92015067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a2d2ab55637eae1e066c53cd40aaeea2e3c654020ee4a95c6e7ea96057add57`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Fri, 09 Aug 2024 17:32:24 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUXDB_VERSION=2.7.9
# Fri, 09 Aug 2024 17:32:24 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Fri, 09 Aug 2024 17:32:24 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 09 Aug 2024 17:32:24 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 09 Aug 2024 17:32:24 GMT
CMD ["influxd"]
# Fri, 09 Aug 2024 17:32:24 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 09 Aug 2024 17:32:24 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1528dee854fc1f40b7c54907a20de439ff29be27ccee84ee7adceeb64d36c84`  
		Last Modified: Fri, 09 Aug 2024 19:55:20 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d0a0d1b2cfdf9f90e47e9bff0a9f08f4ac7216d01f3884095e632c3128e5b4`  
		Last Modified: Fri, 09 Aug 2024 19:55:20 GMT  
		Size: 9.6 MB (9640813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c2c66982b49b5b513e77b7b03fda2b29aec87cbf33c9f980359981fb0eb3cc`  
		Last Modified: Fri, 09 Aug 2024 19:55:20 GMT  
		Size: 5.8 MB (5820950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095db1998ffcf2b245ed0f7ac3a0185f67989ed98e961aff1d28371f000ede19`  
		Last Modified: Fri, 09 Aug 2024 19:55:20 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6001d4fdb935199cba7e53ed000343b3eecc5a5926ebafb05dd979de058a332`  
		Last Modified: Fri, 09 Aug 2024 19:55:21 GMT  
		Size: 49.8 MB (49794132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02594e3b15af8542f06b4d84da4fa9383963777e6bea11309fb6cf8a8175d0a4`  
		Last Modified: Fri, 09 Aug 2024 19:55:21 GMT  
		Size: 23.1 MB (23128306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab0c893a2b25f512b7ff6a2d27365c16af02446bf1680e7a5c3b6f7344fa3cf`  
		Last Modified: Fri, 09 Aug 2024 19:55:21 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a90a7c6ae18eb2a780591b70c66c21213226de3512def65007b96606341afa8`  
		Last Modified: Fri, 09 Aug 2024 19:55:22 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea284cd99da2c6ee20d61b3673c0466c0db028d4297e6cddbd6fec4ef99eee4`  
		Last Modified: Fri, 09 Aug 2024 19:55:22 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:3bfc5594ee42d5cfdb962e3fbf7a6181464c6520c8a5367795551dd737cf5a91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.8 KB (944836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa98eb786937e1d80b19e243a3ea098430db34e39d6d3728ed0c70e5f6467d20`

```dockerfile
```

-	Layers:
	-	`sha256:37d7671128e10a26561e278c2e50a483be6c45b6f40d168b74f8dbba78557d7c`  
		Last Modified: Fri, 09 Aug 2024 19:55:20 GMT  
		Size: 914.1 KB (914089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f88bd506db6060b89b3cb5c421a13f6edcb689ce2f2c376ae2255970a3426fe`  
		Last Modified: Fri, 09 Aug 2024 19:55:20 GMT  
		Size: 30.7 KB (30747 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:6f8b89248297236e1222038ca90649c4d87998a38d5318438d9964473d2bef74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88699480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2387b4f2c78beb65b235419ba705cc0631de21818a9837a4bc7d1fcbbe379f32`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Fri, 09 Aug 2024 17:32:24 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUXDB_VERSION=2.7.9
# Fri, 09 Aug 2024 17:32:24 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Fri, 09 Aug 2024 17:32:24 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 09 Aug 2024 17:32:24 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 09 Aug 2024 17:32:24 GMT
CMD ["influxd"]
# Fri, 09 Aug 2024 17:32:24 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 09 Aug 2024 17:32:24 GMT
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
	-	`sha256:25c2b45ae44eeb9120a8f9ef5aadd1b0b10a69c7d4a6f95538cf39dc03005836`  
		Last Modified: Fri, 09 Aug 2024 19:56:26 GMT  
		Size: 47.7 MB (47714838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277072d078732ce10258c55416ee7f6d276011662e975bb58416bf452d637604`  
		Last Modified: Fri, 09 Aug 2024 19:56:26 GMT  
		Size: 21.7 MB (21662514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68364aae7ae05636c832d6ba637df69884f019412253d9bd75de6de337f5be39`  
		Last Modified: Fri, 09 Aug 2024 19:56:25 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3346d563b96b5ad0b207db43d9d45393b0906f15e37522f5f45ec675740f512`  
		Last Modified: Fri, 09 Aug 2024 19:56:25 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f677757efa8f8ba6ac9200eee890b02300277cbcfeb0148ce8edca9090b865`  
		Last Modified: Fri, 09 Aug 2024 19:56:26 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:97582757bd74853ee0ef89750ad55be13c4f0a4c32d891bc4b1423f0c3d32c33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.4 KB (944397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:151d694d9bf12cfe6d6de7fba37b50e5f5c7aba79ff8ca36dd8d11243f4c9741`

```dockerfile
```

-	Layers:
	-	`sha256:95c403dd8b4f74de03fbb631461bab69012e12ef201fec9b8fd781c4fc9128ff`  
		Last Modified: Fri, 09 Aug 2024 19:56:25 GMT  
		Size: 913.4 KB (913350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d45ef7eaaa1e18e534b8bb7140d96ff580257058b2c2a805dd2131d5f6f1bc9`  
		Last Modified: Fri, 09 Aug 2024 19:56:25 GMT  
		Size: 31.0 KB (31047 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7`

```console
$ docker pull influxdb@sha256:52b002a758ccc33d0ddb8ac006823fe8b5a9a1277338046a9976fabe98d4d13b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7` - linux; amd64

```console
$ docker pull influxdb@sha256:067bd997ad1dbc62a77b5076fd5779d9f50d9bcc7eb32ec6ae28d93f9e1ed752
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168476549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58bdeea2b858ea26080e1377571c587f2d790fb09e598747d7d99a4efaf65322`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 09 Aug 2024 17:32:24 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Fri, 09 Aug 2024 17:32:24 GMT
CMD ["bash"]
# Fri, 09 Aug 2024 17:32:24 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENV GOSU_VER=1.16
# Fri, 09 Aug 2024 17:32:24 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUXDB_VERSION=2.7.9
# Fri, 09 Aug 2024 17:32:24 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Fri, 09 Aug 2024 17:32:24 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 09 Aug 2024 17:32:24 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 09 Aug 2024 17:32:24 GMT
CMD ["influxd"]
# Fri, 09 Aug 2024 17:32:24 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 09 Aug 2024 17:32:24 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb66f32b72131e4dbe8a37fa0fdcae3f2403ced6d15fd68128cfdb31df9d105d`  
		Last Modified: Tue, 13 Aug 2024 01:18:22 GMT  
		Size: 9.8 MB (9786136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffffb3badc7145e237597d807220c68b3b99d8f8f7b0f8698cfa16e59a6832c0`  
		Last Modified: Tue, 13 Aug 2024 01:18:22 GMT  
		Size: 5.8 MB (5820938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e805ddd5f740b452df1f5aa8709acf7c8cfe05e1bbecbdb66ca23dfee6f1b6c7`  
		Last Modified: Tue, 13 Aug 2024 01:18:22 GMT  
		Size: 3.2 KB (3224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5182142bbb3d4cd9f0842ce4a47558bf5a347ccde155b639b4900f57b005db7d`  
		Last Modified: Tue, 13 Aug 2024 01:18:22 GMT  
		Size: 1.0 MB (1006370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae5bdb75813050ac227d3c05e8c221bb60c3c320e4e7999666c7a9409812055`  
		Last Modified: Tue, 13 Aug 2024 01:18:24 GMT  
		Size: 99.6 MB (99598615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92d2f549099f782f689c6dc40d89515db96f2f046bb3b68faa974ebf2df63c4`  
		Last Modified: Tue, 13 Aug 2024 01:18:23 GMT  
		Size: 23.1 MB (23128307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3259b34ea6a5547bae58cfcdd7b22477f94e69861eb0b81d95358344d2b4146`  
		Last Modified: Tue, 13 Aug 2024 01:18:23 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da3072f071ac90de49cd981e143bd59b095e6aa59d05f79f59bf8b4143814f0`  
		Last Modified: Tue, 13 Aug 2024 01:18:23 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49fc83331c9f60f2976426e18c83e370022992ac27c682223d6872c1813dcc52`  
		Last Modified: Tue, 13 Aug 2024 01:18:23 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:e12889f12dde15ed974d64f6d2a55d8f5dfa884b16c67e39e4e6951921468fa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:947bc2abfa72fb85868df0f0899a1cf183797a5aa22d917e513dcee701dd0ff9`

```dockerfile
```

-	Layers:
	-	`sha256:9d3c0316d99ae11edb762b105c2bba8a91bd8d84000bd36999781fa422d23971`  
		Last Modified: Tue, 13 Aug 2024 01:18:22 GMT  
		Size: 2.8 MB (2833438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee48b73455f9d44f3bdd1f1cec8cd2ca4567dfefec7105826dc35e1dd5db1a21`  
		Last Modified: Tue, 13 Aug 2024 01:18:22 GMT  
		Size: 33.5 KB (33540 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:38c90c641a28bed8d1c06cf9e73e8ebc7bb759bcbebf24c9787dd8d2fd977826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162251582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e98a9ac2dfe717bd84cd9069d0e67aebfbd61b0842c7293fd1f3cb949ea133`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 09 Aug 2024 17:32:24 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Fri, 09 Aug 2024 17:32:24 GMT
CMD ["bash"]
# Fri, 09 Aug 2024 17:32:24 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENV GOSU_VER=1.16
# Fri, 09 Aug 2024 17:32:24 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUXDB_VERSION=2.7.9
# Fri, 09 Aug 2024 17:32:24 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Fri, 09 Aug 2024 17:32:24 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 09 Aug 2024 17:32:24 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 09 Aug 2024 17:32:24 GMT
CMD ["influxd"]
# Fri, 09 Aug 2024 17:32:24 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 09 Aug 2024 17:32:24 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af8cd4147de7f78511d80ebd168ada550c516bc7b7ed15865aa5a32fbd733089`  
		Last Modified: Tue, 13 Aug 2024 07:21:58 GMT  
		Size: 9.6 MB (9585117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53bc08419b6bfeb1324aa33ae3db2694f2fc8584e5ca8cb0ce38b69722e84d7`  
		Last Modified: Tue, 13 Aug 2024 07:21:58 GMT  
		Size: 5.5 MB (5463786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb2629f78b117ded6b2a6c524416ae254383a1d7873b717c9117221549b859e`  
		Last Modified: Tue, 13 Aug 2024 07:21:58 GMT  
		Size: 3.2 KB (3226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8380d9c1dfee9401788143d4b533d97220b95afb5290f5fc52e1a0392b86c8`  
		Last Modified: Tue, 13 Aug 2024 07:21:58 GMT  
		Size: 936.1 KB (936111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887263e189946abfbbdd9aeba3f901d1ab04fae88c5b0cfbd8362b526fc493d8`  
		Last Modified: Tue, 13 Aug 2024 07:22:01 GMT  
		Size: 95.4 MB (95437568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa25a5c69d1ffd85fa21abcf0d7b738136c9ef9dac31bece7b089542663593f`  
		Last Modified: Tue, 13 Aug 2024 07:22:00 GMT  
		Size: 21.7 MB (21662519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddce16abef94acc9b3beb7ba2d70c053d3fe91393f3122eedb9de5c90b41821d`  
		Last Modified: Tue, 13 Aug 2024 07:21:59 GMT  
		Size: 207.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3db895c0f8393c87eac4a7e6f76a587ca7c07b4d021038189266130c2a23e32`  
		Last Modified: Tue, 13 Aug 2024 07:22:00 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f26c0696526948b6a0e0d4c5b94469566baae900b49922fbe2d11b0b282c031`  
		Last Modified: Tue, 13 Aug 2024 07:22:00 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:1591961c61dbf849630bc9fb76c0a36602a1aaf45ce41cd9de67d7f11a99cd81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a907c57d223f8c2b09edfbb904aa6edbbc5ce8f56133affaaf98540a4f3edf7b`

```dockerfile
```

-	Layers:
	-	`sha256:aa94f2b9189325067e7127dc36b448a6a1a91b14535cc733af2f59f4c961dd1e`  
		Last Modified: Tue, 13 Aug 2024 07:21:58 GMT  
		Size: 2.8 MB (2832675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b639136a991ad8af0a7d68223a4669ff95935dfab68f7399973cd728b4e40ec3`  
		Last Modified: Tue, 13 Aug 2024 07:21:58 GMT  
		Size: 33.8 KB (33843 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7-alpine`

```console
$ docker pull influxdb@sha256:82ad20cfcb42ef800a31977d2e38debe6cdbf97160a6ea2155f7b56e0e3a431b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:98372aea3611142e87695dfd7e9d2b3cc3ff2e578f20af3de6c12c9320e50de3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (92015067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a2d2ab55637eae1e066c53cd40aaeea2e3c654020ee4a95c6e7ea96057add57`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Fri, 09 Aug 2024 17:32:24 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUXDB_VERSION=2.7.9
# Fri, 09 Aug 2024 17:32:24 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Fri, 09 Aug 2024 17:32:24 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 09 Aug 2024 17:32:24 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 09 Aug 2024 17:32:24 GMT
CMD ["influxd"]
# Fri, 09 Aug 2024 17:32:24 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 09 Aug 2024 17:32:24 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1528dee854fc1f40b7c54907a20de439ff29be27ccee84ee7adceeb64d36c84`  
		Last Modified: Fri, 09 Aug 2024 19:55:20 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d0a0d1b2cfdf9f90e47e9bff0a9f08f4ac7216d01f3884095e632c3128e5b4`  
		Last Modified: Fri, 09 Aug 2024 19:55:20 GMT  
		Size: 9.6 MB (9640813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c2c66982b49b5b513e77b7b03fda2b29aec87cbf33c9f980359981fb0eb3cc`  
		Last Modified: Fri, 09 Aug 2024 19:55:20 GMT  
		Size: 5.8 MB (5820950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095db1998ffcf2b245ed0f7ac3a0185f67989ed98e961aff1d28371f000ede19`  
		Last Modified: Fri, 09 Aug 2024 19:55:20 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6001d4fdb935199cba7e53ed000343b3eecc5a5926ebafb05dd979de058a332`  
		Last Modified: Fri, 09 Aug 2024 19:55:21 GMT  
		Size: 49.8 MB (49794132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02594e3b15af8542f06b4d84da4fa9383963777e6bea11309fb6cf8a8175d0a4`  
		Last Modified: Fri, 09 Aug 2024 19:55:21 GMT  
		Size: 23.1 MB (23128306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab0c893a2b25f512b7ff6a2d27365c16af02446bf1680e7a5c3b6f7344fa3cf`  
		Last Modified: Fri, 09 Aug 2024 19:55:21 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a90a7c6ae18eb2a780591b70c66c21213226de3512def65007b96606341afa8`  
		Last Modified: Fri, 09 Aug 2024 19:55:22 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea284cd99da2c6ee20d61b3673c0466c0db028d4297e6cddbd6fec4ef99eee4`  
		Last Modified: Fri, 09 Aug 2024 19:55:22 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:3bfc5594ee42d5cfdb962e3fbf7a6181464c6520c8a5367795551dd737cf5a91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.8 KB (944836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa98eb786937e1d80b19e243a3ea098430db34e39d6d3728ed0c70e5f6467d20`

```dockerfile
```

-	Layers:
	-	`sha256:37d7671128e10a26561e278c2e50a483be6c45b6f40d168b74f8dbba78557d7c`  
		Last Modified: Fri, 09 Aug 2024 19:55:20 GMT  
		Size: 914.1 KB (914089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f88bd506db6060b89b3cb5c421a13f6edcb689ce2f2c376ae2255970a3426fe`  
		Last Modified: Fri, 09 Aug 2024 19:55:20 GMT  
		Size: 30.7 KB (30747 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:6f8b89248297236e1222038ca90649c4d87998a38d5318438d9964473d2bef74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88699480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2387b4f2c78beb65b235419ba705cc0631de21818a9837a4bc7d1fcbbe379f32`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Fri, 09 Aug 2024 17:32:24 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUXDB_VERSION=2.7.9
# Fri, 09 Aug 2024 17:32:24 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Fri, 09 Aug 2024 17:32:24 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 09 Aug 2024 17:32:24 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 09 Aug 2024 17:32:24 GMT
CMD ["influxd"]
# Fri, 09 Aug 2024 17:32:24 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 09 Aug 2024 17:32:24 GMT
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
	-	`sha256:25c2b45ae44eeb9120a8f9ef5aadd1b0b10a69c7d4a6f95538cf39dc03005836`  
		Last Modified: Fri, 09 Aug 2024 19:56:26 GMT  
		Size: 47.7 MB (47714838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277072d078732ce10258c55416ee7f6d276011662e975bb58416bf452d637604`  
		Last Modified: Fri, 09 Aug 2024 19:56:26 GMT  
		Size: 21.7 MB (21662514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68364aae7ae05636c832d6ba637df69884f019412253d9bd75de6de337f5be39`  
		Last Modified: Fri, 09 Aug 2024 19:56:25 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3346d563b96b5ad0b207db43d9d45393b0906f15e37522f5f45ec675740f512`  
		Last Modified: Fri, 09 Aug 2024 19:56:25 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f677757efa8f8ba6ac9200eee890b02300277cbcfeb0148ce8edca9090b865`  
		Last Modified: Fri, 09 Aug 2024 19:56:26 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:97582757bd74853ee0ef89750ad55be13c4f0a4c32d891bc4b1423f0c3d32c33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.4 KB (944397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:151d694d9bf12cfe6d6de7fba37b50e5f5c7aba79ff8ca36dd8d11243f4c9741`

```dockerfile
```

-	Layers:
	-	`sha256:95c403dd8b4f74de03fbb631461bab69012e12ef201fec9b8fd781c4fc9128ff`  
		Last Modified: Fri, 09 Aug 2024 19:56:25 GMT  
		Size: 913.4 KB (913350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d45ef7eaaa1e18e534b8bb7140d96ff580257058b2c2a805dd2131d5f6f1bc9`  
		Last Modified: Fri, 09 Aug 2024 19:56:25 GMT  
		Size: 31.0 KB (31047 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7.10`

**does not exist** (yet?)

## `influxdb:2.7.10-alpine`

**does not exist** (yet?)

## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:82ad20cfcb42ef800a31977d2e38debe6cdbf97160a6ea2155f7b56e0e3a431b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:98372aea3611142e87695dfd7e9d2b3cc3ff2e578f20af3de6c12c9320e50de3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (92015067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a2d2ab55637eae1e066c53cd40aaeea2e3c654020ee4a95c6e7ea96057add57`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Fri, 09 Aug 2024 17:32:24 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUXDB_VERSION=2.7.9
# Fri, 09 Aug 2024 17:32:24 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Fri, 09 Aug 2024 17:32:24 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 09 Aug 2024 17:32:24 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 09 Aug 2024 17:32:24 GMT
CMD ["influxd"]
# Fri, 09 Aug 2024 17:32:24 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 09 Aug 2024 17:32:24 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1528dee854fc1f40b7c54907a20de439ff29be27ccee84ee7adceeb64d36c84`  
		Last Modified: Fri, 09 Aug 2024 19:55:20 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d0a0d1b2cfdf9f90e47e9bff0a9f08f4ac7216d01f3884095e632c3128e5b4`  
		Last Modified: Fri, 09 Aug 2024 19:55:20 GMT  
		Size: 9.6 MB (9640813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c2c66982b49b5b513e77b7b03fda2b29aec87cbf33c9f980359981fb0eb3cc`  
		Last Modified: Fri, 09 Aug 2024 19:55:20 GMT  
		Size: 5.8 MB (5820950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095db1998ffcf2b245ed0f7ac3a0185f67989ed98e961aff1d28371f000ede19`  
		Last Modified: Fri, 09 Aug 2024 19:55:20 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6001d4fdb935199cba7e53ed000343b3eecc5a5926ebafb05dd979de058a332`  
		Last Modified: Fri, 09 Aug 2024 19:55:21 GMT  
		Size: 49.8 MB (49794132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02594e3b15af8542f06b4d84da4fa9383963777e6bea11309fb6cf8a8175d0a4`  
		Last Modified: Fri, 09 Aug 2024 19:55:21 GMT  
		Size: 23.1 MB (23128306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab0c893a2b25f512b7ff6a2d27365c16af02446bf1680e7a5c3b6f7344fa3cf`  
		Last Modified: Fri, 09 Aug 2024 19:55:21 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a90a7c6ae18eb2a780591b70c66c21213226de3512def65007b96606341afa8`  
		Last Modified: Fri, 09 Aug 2024 19:55:22 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea284cd99da2c6ee20d61b3673c0466c0db028d4297e6cddbd6fec4ef99eee4`  
		Last Modified: Fri, 09 Aug 2024 19:55:22 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:3bfc5594ee42d5cfdb962e3fbf7a6181464c6520c8a5367795551dd737cf5a91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.8 KB (944836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa98eb786937e1d80b19e243a3ea098430db34e39d6d3728ed0c70e5f6467d20`

```dockerfile
```

-	Layers:
	-	`sha256:37d7671128e10a26561e278c2e50a483be6c45b6f40d168b74f8dbba78557d7c`  
		Last Modified: Fri, 09 Aug 2024 19:55:20 GMT  
		Size: 914.1 KB (914089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f88bd506db6060b89b3cb5c421a13f6edcb689ce2f2c376ae2255970a3426fe`  
		Last Modified: Fri, 09 Aug 2024 19:55:20 GMT  
		Size: 30.7 KB (30747 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:6f8b89248297236e1222038ca90649c4d87998a38d5318438d9964473d2bef74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88699480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2387b4f2c78beb65b235419ba705cc0631de21818a9837a4bc7d1fcbbe379f32`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Fri, 09 Aug 2024 17:32:24 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUXDB_VERSION=2.7.9
# Fri, 09 Aug 2024 17:32:24 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Fri, 09 Aug 2024 17:32:24 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 09 Aug 2024 17:32:24 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 09 Aug 2024 17:32:24 GMT
CMD ["influxd"]
# Fri, 09 Aug 2024 17:32:24 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 09 Aug 2024 17:32:24 GMT
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
	-	`sha256:25c2b45ae44eeb9120a8f9ef5aadd1b0b10a69c7d4a6f95538cf39dc03005836`  
		Last Modified: Fri, 09 Aug 2024 19:56:26 GMT  
		Size: 47.7 MB (47714838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277072d078732ce10258c55416ee7f6d276011662e975bb58416bf452d637604`  
		Last Modified: Fri, 09 Aug 2024 19:56:26 GMT  
		Size: 21.7 MB (21662514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68364aae7ae05636c832d6ba637df69884f019412253d9bd75de6de337f5be39`  
		Last Modified: Fri, 09 Aug 2024 19:56:25 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3346d563b96b5ad0b207db43d9d45393b0906f15e37522f5f45ec675740f512`  
		Last Modified: Fri, 09 Aug 2024 19:56:25 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f677757efa8f8ba6ac9200eee890b02300277cbcfeb0148ce8edca9090b865`  
		Last Modified: Fri, 09 Aug 2024 19:56:26 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:97582757bd74853ee0ef89750ad55be13c4f0a4c32d891bc4b1423f0c3d32c33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.4 KB (944397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:151d694d9bf12cfe6d6de7fba37b50e5f5c7aba79ff8ca36dd8d11243f4c9741`

```dockerfile
```

-	Layers:
	-	`sha256:95c403dd8b4f74de03fbb631461bab69012e12ef201fec9b8fd781c4fc9128ff`  
		Last Modified: Fri, 09 Aug 2024 19:56:25 GMT  
		Size: 913.4 KB (913350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d45ef7eaaa1e18e534b8bb7140d96ff580257058b2c2a805dd2131d5f6f1bc9`  
		Last Modified: Fri, 09 Aug 2024 19:56:25 GMT  
		Size: 31.0 KB (31047 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:latest`

```console
$ docker pull influxdb@sha256:52b002a758ccc33d0ddb8ac006823fe8b5a9a1277338046a9976fabe98d4d13b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:067bd997ad1dbc62a77b5076fd5779d9f50d9bcc7eb32ec6ae28d93f9e1ed752
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168476549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58bdeea2b858ea26080e1377571c587f2d790fb09e598747d7d99a4efaf65322`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 09 Aug 2024 17:32:24 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Fri, 09 Aug 2024 17:32:24 GMT
CMD ["bash"]
# Fri, 09 Aug 2024 17:32:24 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENV GOSU_VER=1.16
# Fri, 09 Aug 2024 17:32:24 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUXDB_VERSION=2.7.9
# Fri, 09 Aug 2024 17:32:24 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Fri, 09 Aug 2024 17:32:24 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 09 Aug 2024 17:32:24 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 09 Aug 2024 17:32:24 GMT
CMD ["influxd"]
# Fri, 09 Aug 2024 17:32:24 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 09 Aug 2024 17:32:24 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb66f32b72131e4dbe8a37fa0fdcae3f2403ced6d15fd68128cfdb31df9d105d`  
		Last Modified: Tue, 13 Aug 2024 01:18:22 GMT  
		Size: 9.8 MB (9786136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffffb3badc7145e237597d807220c68b3b99d8f8f7b0f8698cfa16e59a6832c0`  
		Last Modified: Tue, 13 Aug 2024 01:18:22 GMT  
		Size: 5.8 MB (5820938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e805ddd5f740b452df1f5aa8709acf7c8cfe05e1bbecbdb66ca23dfee6f1b6c7`  
		Last Modified: Tue, 13 Aug 2024 01:18:22 GMT  
		Size: 3.2 KB (3224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5182142bbb3d4cd9f0842ce4a47558bf5a347ccde155b639b4900f57b005db7d`  
		Last Modified: Tue, 13 Aug 2024 01:18:22 GMT  
		Size: 1.0 MB (1006370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae5bdb75813050ac227d3c05e8c221bb60c3c320e4e7999666c7a9409812055`  
		Last Modified: Tue, 13 Aug 2024 01:18:24 GMT  
		Size: 99.6 MB (99598615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92d2f549099f782f689c6dc40d89515db96f2f046bb3b68faa974ebf2df63c4`  
		Last Modified: Tue, 13 Aug 2024 01:18:23 GMT  
		Size: 23.1 MB (23128307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3259b34ea6a5547bae58cfcdd7b22477f94e69861eb0b81d95358344d2b4146`  
		Last Modified: Tue, 13 Aug 2024 01:18:23 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da3072f071ac90de49cd981e143bd59b095e6aa59d05f79f59bf8b4143814f0`  
		Last Modified: Tue, 13 Aug 2024 01:18:23 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49fc83331c9f60f2976426e18c83e370022992ac27c682223d6872c1813dcc52`  
		Last Modified: Tue, 13 Aug 2024 01:18:23 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:e12889f12dde15ed974d64f6d2a55d8f5dfa884b16c67e39e4e6951921468fa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:947bc2abfa72fb85868df0f0899a1cf183797a5aa22d917e513dcee701dd0ff9`

```dockerfile
```

-	Layers:
	-	`sha256:9d3c0316d99ae11edb762b105c2bba8a91bd8d84000bd36999781fa422d23971`  
		Last Modified: Tue, 13 Aug 2024 01:18:22 GMT  
		Size: 2.8 MB (2833438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee48b73455f9d44f3bdd1f1cec8cd2ca4567dfefec7105826dc35e1dd5db1a21`  
		Last Modified: Tue, 13 Aug 2024 01:18:22 GMT  
		Size: 33.5 KB (33540 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:38c90c641a28bed8d1c06cf9e73e8ebc7bb759bcbebf24c9787dd8d2fd977826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162251582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e98a9ac2dfe717bd84cd9069d0e67aebfbd61b0842c7293fd1f3cb949ea133`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 09 Aug 2024 17:32:24 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Fri, 09 Aug 2024 17:32:24 GMT
CMD ["bash"]
# Fri, 09 Aug 2024 17:32:24 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENV GOSU_VER=1.16
# Fri, 09 Aug 2024 17:32:24 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUXDB_VERSION=2.7.9
# Fri, 09 Aug 2024 17:32:24 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Fri, 09 Aug 2024 17:32:24 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 09 Aug 2024 17:32:24 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 09 Aug 2024 17:32:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 09 Aug 2024 17:32:24 GMT
CMD ["influxd"]
# Fri, 09 Aug 2024 17:32:24 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 09 Aug 2024 17:32:24 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 09 Aug 2024 17:32:24 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af8cd4147de7f78511d80ebd168ada550c516bc7b7ed15865aa5a32fbd733089`  
		Last Modified: Tue, 13 Aug 2024 07:21:58 GMT  
		Size: 9.6 MB (9585117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53bc08419b6bfeb1324aa33ae3db2694f2fc8584e5ca8cb0ce38b69722e84d7`  
		Last Modified: Tue, 13 Aug 2024 07:21:58 GMT  
		Size: 5.5 MB (5463786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb2629f78b117ded6b2a6c524416ae254383a1d7873b717c9117221549b859e`  
		Last Modified: Tue, 13 Aug 2024 07:21:58 GMT  
		Size: 3.2 KB (3226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8380d9c1dfee9401788143d4b533d97220b95afb5290f5fc52e1a0392b86c8`  
		Last Modified: Tue, 13 Aug 2024 07:21:58 GMT  
		Size: 936.1 KB (936111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887263e189946abfbbdd9aeba3f901d1ab04fae88c5b0cfbd8362b526fc493d8`  
		Last Modified: Tue, 13 Aug 2024 07:22:01 GMT  
		Size: 95.4 MB (95437568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa25a5c69d1ffd85fa21abcf0d7b738136c9ef9dac31bece7b089542663593f`  
		Last Modified: Tue, 13 Aug 2024 07:22:00 GMT  
		Size: 21.7 MB (21662519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddce16abef94acc9b3beb7ba2d70c053d3fe91393f3122eedb9de5c90b41821d`  
		Last Modified: Tue, 13 Aug 2024 07:21:59 GMT  
		Size: 207.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3db895c0f8393c87eac4a7e6f76a587ca7c07b4d021038189266130c2a23e32`  
		Last Modified: Tue, 13 Aug 2024 07:22:00 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f26c0696526948b6a0e0d4c5b94469566baae900b49922fbe2d11b0b282c031`  
		Last Modified: Tue, 13 Aug 2024 07:22:00 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:1591961c61dbf849630bc9fb76c0a36602a1aaf45ce41cd9de67d7f11a99cd81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a907c57d223f8c2b09edfbb904aa6edbbc5ce8f56133affaaf98540a4f3edf7b`

```dockerfile
```

-	Layers:
	-	`sha256:aa94f2b9189325067e7127dc36b448a6a1a91b14535cc733af2f59f4c961dd1e`  
		Last Modified: Tue, 13 Aug 2024 07:21:58 GMT  
		Size: 2.8 MB (2832675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b639136a991ad8af0a7d68223a4669ff95935dfab68f7399973cd728b4e40ec3`  
		Last Modified: Tue, 13 Aug 2024 07:21:58 GMT  
		Size: 33.8 KB (33843 bytes)  
		MIME: application/vnd.in-toto+json
