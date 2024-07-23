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
-	[`influxdb:2.7.7`](#influxdb277)
-	[`influxdb:2.7.7-alpine`](#influxdb277-alpine)
-	[`influxdb:alpine`](#influxdbalpine)
-	[`influxdb:latest`](#influxdblatest)

## `influxdb:1.10-data`

```console
$ docker pull influxdb@sha256:12fab1d0f130ffe380f2f5c4735f0e30233dad4c263f6f3b77c64a522a7117c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-data` - linux; amd64

```console
$ docker pull influxdb@sha256:b0880275c0583a517fe7f51e8716e26569b636502375d1b181dcc90d9895d273
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112226809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea729fa3809f54607a7ab7718af47998780d7e1e145958f9d3f9c932baad5545`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:b8d066bbda2d783c3ca81ab100fc5e45550234b68fde96332f303f669256842e in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["bash"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Thu, 06 Jun 2024 16:24:41 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c1c1a7d83fb1e16686c4e98df3d6f88b37beb4d65daae1ddd715f95d7ac4db5c`  
		Last Modified: Tue, 02 Jul 2024 01:29:07 GMT  
		Size: 55.1 MB (55081360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a305f523084f0a28b5daf532a5216d9be05d863c6bd3f5bd2969965eb7e9a27`  
		Last Modified: Tue, 02 Jul 2024 02:01:21 GMT  
		Size: 15.8 MB (15764174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a09ab90b1772c0fbe79457c1a0ce92fc161b421f6b2856765f9c80d81a544f`  
		Last Modified: Tue, 02 Jul 2024 03:03:30 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f31076d9552e4951b4d4b70e5f410c955e2773a887170a277a57c74285af903`  
		Last Modified: Tue, 02 Jul 2024 03:03:31 GMT  
		Size: 41.4 MB (41377718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f0bf4e4a337f42e9744a9818ab3c8d9e7d615f2d91eb5da67928993b42e86d`  
		Last Modified: Tue, 02 Jul 2024 03:03:30 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d12f1acb17338240e1aa1d1011cad635dd1fed038859b3dee7b19cab7069f3`  
		Last Modified: Tue, 02 Jul 2024 03:03:30 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7121dc90affd4971ed4020e7299242e1ca66ba9a802299817210c332eda4486`  
		Last Modified: Tue, 02 Jul 2024 03:03:31 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:7d27d7aed43196be2fa59657a8c5d483ad5f6929ada540a1e577a1862922131d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4593922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e620a40902fd705f79fc3cb08d5f6f077a078612fd5067f90adc0eb3b29400`

```dockerfile
```

-	Layers:
	-	`sha256:b30a9b6dec5981a5de0ad0486c6cbff48d24ca0ffcb4fa0170fa75acf6846750`  
		Last Modified: Tue, 02 Jul 2024 03:03:31 GMT  
		Size: 4.6 MB (4579348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3147ca73ca9cef831454435932cc4e30424267e06aa5bb1bd8414a5999ebdb3f`  
		Last Modified: Tue, 02 Jul 2024 03:03:31 GMT  
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
$ docker pull influxdb@sha256:dadadc47415cc2c035bd203d1d5e887385e9940207795f395eebcf284c180633
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:7d2342d7eef257a1084fb15044b034c0c383f4cc6e1b12c4f4ee947eb9f7b7f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.9 MB (90943465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7db0c854686f433740deaef4449d9b2a9bf1727cac575bebbedffb367393701`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:b8d066bbda2d783c3ca81ab100fc5e45550234b68fde96332f303f669256842e in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["bash"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Thu, 06 Jun 2024 16:24:41 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8091/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:c1c1a7d83fb1e16686c4e98df3d6f88b37beb4d65daae1ddd715f95d7ac4db5c`  
		Last Modified: Tue, 02 Jul 2024 01:29:07 GMT  
		Size: 55.1 MB (55081360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a305f523084f0a28b5daf532a5216d9be05d863c6bd3f5bd2969965eb7e9a27`  
		Last Modified: Tue, 02 Jul 2024 02:01:21 GMT  
		Size: 15.8 MB (15764174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b21dfc47cfa00632811197916a2e87cd12963db641190b378b26f914292e8ef`  
		Last Modified: Tue, 02 Jul 2024 03:03:30 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11019476cb1ba204cc59d9d6d20d4a80a1e7059dde0645c118f4ed9e2fd64f7`  
		Last Modified: Tue, 02 Jul 2024 03:03:31 GMT  
		Size: 20.1 MB (20095590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8c362cfed7532c2c9f7892eb363dff6d062ae758f58fae9647e96e52fc0f6e`  
		Last Modified: Tue, 02 Jul 2024 03:03:30 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203a0dd16f13afca2b6d71bfe203dcfaaf976dbce4d1a7387b160f1325d84df6`  
		Last Modified: Tue, 02 Jul 2024 03:03:30 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:a7e71c9421176666694445928b6ec9b536aa0d1f01fdfbabb5a203b3e3add1d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4529154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45bef63d312e8d70072a7f22c1964a94776f6668e88c600505a31c5e3678e07f`

```dockerfile
```

-	Layers:
	-	`sha256:9bda7a5ee66b27632e2e2006ae2f7601c48b33d691d8ed82991c05976d61d081`  
		Last Modified: Tue, 02 Jul 2024 03:03:30 GMT  
		Size: 4.5 MB (4516233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:588a040e34ea165f3ed3f48535d8b425e4267f8469c14967f9c714d27580220a`  
		Last Modified: Tue, 02 Jul 2024 03:03:30 GMT  
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
$ docker pull influxdb@sha256:12fab1d0f130ffe380f2f5c4735f0e30233dad4c263f6f3b77c64a522a7117c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.7-data` - linux; amd64

```console
$ docker pull influxdb@sha256:b0880275c0583a517fe7f51e8716e26569b636502375d1b181dcc90d9895d273
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112226809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea729fa3809f54607a7ab7718af47998780d7e1e145958f9d3f9c932baad5545`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:b8d066bbda2d783c3ca81ab100fc5e45550234b68fde96332f303f669256842e in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["bash"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Thu, 06 Jun 2024 16:24:41 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c1c1a7d83fb1e16686c4e98df3d6f88b37beb4d65daae1ddd715f95d7ac4db5c`  
		Last Modified: Tue, 02 Jul 2024 01:29:07 GMT  
		Size: 55.1 MB (55081360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a305f523084f0a28b5daf532a5216d9be05d863c6bd3f5bd2969965eb7e9a27`  
		Last Modified: Tue, 02 Jul 2024 02:01:21 GMT  
		Size: 15.8 MB (15764174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a09ab90b1772c0fbe79457c1a0ce92fc161b421f6b2856765f9c80d81a544f`  
		Last Modified: Tue, 02 Jul 2024 03:03:30 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f31076d9552e4951b4d4b70e5f410c955e2773a887170a277a57c74285af903`  
		Last Modified: Tue, 02 Jul 2024 03:03:31 GMT  
		Size: 41.4 MB (41377718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f0bf4e4a337f42e9744a9818ab3c8d9e7d615f2d91eb5da67928993b42e86d`  
		Last Modified: Tue, 02 Jul 2024 03:03:30 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d12f1acb17338240e1aa1d1011cad635dd1fed038859b3dee7b19cab7069f3`  
		Last Modified: Tue, 02 Jul 2024 03:03:30 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7121dc90affd4971ed4020e7299242e1ca66ba9a802299817210c332eda4486`  
		Last Modified: Tue, 02 Jul 2024 03:03:31 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.7-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:7d27d7aed43196be2fa59657a8c5d483ad5f6929ada540a1e577a1862922131d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4593922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e620a40902fd705f79fc3cb08d5f6f077a078612fd5067f90adc0eb3b29400`

```dockerfile
```

-	Layers:
	-	`sha256:b30a9b6dec5981a5de0ad0486c6cbff48d24ca0ffcb4fa0170fa75acf6846750`  
		Last Modified: Tue, 02 Jul 2024 03:03:31 GMT  
		Size: 4.6 MB (4579348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3147ca73ca9cef831454435932cc4e30424267e06aa5bb1bd8414a5999ebdb3f`  
		Last Modified: Tue, 02 Jul 2024 03:03:31 GMT  
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
$ docker pull influxdb@sha256:dadadc47415cc2c035bd203d1d5e887385e9940207795f395eebcf284c180633
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.7-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:7d2342d7eef257a1084fb15044b034c0c383f4cc6e1b12c4f4ee947eb9f7b7f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.9 MB (90943465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7db0c854686f433740deaef4449d9b2a9bf1727cac575bebbedffb367393701`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:b8d066bbda2d783c3ca81ab100fc5e45550234b68fde96332f303f669256842e in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["bash"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Thu, 06 Jun 2024 16:24:41 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8091/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:c1c1a7d83fb1e16686c4e98df3d6f88b37beb4d65daae1ddd715f95d7ac4db5c`  
		Last Modified: Tue, 02 Jul 2024 01:29:07 GMT  
		Size: 55.1 MB (55081360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a305f523084f0a28b5daf532a5216d9be05d863c6bd3f5bd2969965eb7e9a27`  
		Last Modified: Tue, 02 Jul 2024 02:01:21 GMT  
		Size: 15.8 MB (15764174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b21dfc47cfa00632811197916a2e87cd12963db641190b378b26f914292e8ef`  
		Last Modified: Tue, 02 Jul 2024 03:03:30 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11019476cb1ba204cc59d9d6d20d4a80a1e7059dde0645c118f4ed9e2fd64f7`  
		Last Modified: Tue, 02 Jul 2024 03:03:31 GMT  
		Size: 20.1 MB (20095590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8c362cfed7532c2c9f7892eb363dff6d062ae758f58fae9647e96e52fc0f6e`  
		Last Modified: Tue, 02 Jul 2024 03:03:30 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203a0dd16f13afca2b6d71bfe203dcfaaf976dbce4d1a7387b160f1325d84df6`  
		Last Modified: Tue, 02 Jul 2024 03:03:30 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.7-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:a7e71c9421176666694445928b6ec9b536aa0d1f01fdfbabb5a203b3e3add1d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4529154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45bef63d312e8d70072a7f22c1964a94776f6668e88c600505a31c5e3678e07f`

```dockerfile
```

-	Layers:
	-	`sha256:9bda7a5ee66b27632e2e2006ae2f7601c48b33d691d8ed82991c05976d61d081`  
		Last Modified: Tue, 02 Jul 2024 03:03:30 GMT  
		Size: 4.5 MB (4516233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:588a040e34ea165f3ed3f48535d8b425e4267f8469c14967f9c714d27580220a`  
		Last Modified: Tue, 02 Jul 2024 03:03:30 GMT  
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
$ docker pull influxdb@sha256:e55b98514d700229eb7fa728e706cc3192b81cbc54444a31362047906cf1424e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data` - linux; amd64

```console
$ docker pull influxdb@sha256:d88f1f641e427fba8b577613eef6d42b6e1e76248ab91740c4ab22d444303963
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 MB (115430078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f65689acada4b99e8e6c740ad691854ee28c4bcf20dbe1b0c83e4e0fc8ca29f2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:e8aac9b1598114ead96b4038c19d915b87f662ef342291d69c7e5255c5d731fc in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["bash"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.11.5-c1.11.5
# Thu, 06 Jun 2024 16:24:41 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:e9aef93137af6e967e7242f3b3c8ecd8e6f571d1e6fdd9e72db0befeeae3cf13`  
		Last Modified: Tue, 02 Jul 2024 01:28:26 GMT  
		Size: 49.6 MB (49554064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b365fa3e8dc16e70d89fab0e91f5242feb38ae3cfeb6655e654209ea109333`  
		Last Modified: Tue, 02 Jul 2024 02:00:17 GMT  
		Size: 24.0 MB (24049794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ce8052ded392581255102609c9e762cfe0138ac9f1f84f48273a2d0a75b1ed`  
		Last Modified: Tue, 02 Jul 2024 03:03:25 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cebc80bc73311fe34e10f3be81e11feba0bad1dc630ebee5faf81ddc9fc507e`  
		Last Modified: Tue, 02 Jul 2024 03:03:26 GMT  
		Size: 41.8 MB (41822661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa467c284d08679e8a978718a84df389de45b099bccbd66ec5dd2ff8d7b61a50`  
		Last Modified: Tue, 02 Jul 2024 03:03:25 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa7794091bcf053522fe9f291f59a810358245615301d2293ff4bcba2753864`  
		Last Modified: Tue, 02 Jul 2024 03:03:26 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4276be0cb3620b87a3008de157a4886c17b2ac808a7655b3cdf1e33c836fccfc`  
		Last Modified: Tue, 02 Jul 2024 03:03:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:62b1208f913bb025d4c2cbb8eba98ce92643a3f3f9c682ed04c97a1c02ccdfa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4468343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:524914c080c1e72a708f9116ed5d50f44637b94e1b4938cff057a94dbeea574c`

```dockerfile
```

-	Layers:
	-	`sha256:5bd9a289241c64d41979d05904e13936a86c7eb15a5287e71a682cb9bba78511`  
		Last Modified: Tue, 02 Jul 2024 03:03:26 GMT  
		Size: 4.5 MB (4453769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b079cae700e0ee816202f847150dd85b8d2589c94e4f5c6759d4dc45a0d6b682`  
		Last Modified: Tue, 02 Jul 2024 03:03:26 GMT  
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
$ docker pull influxdb@sha256:c0fc65a03709ff7b45ebf4b3f99024d7e0e6c6758944e544f447361107d3bc04
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:073fd87728df8c8e61a5c9c703a6a2d3e17636b526a643fcd5ee520126c1d68e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (93999240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c33eee34a4b90a63e416ae1d57aea7df041589a753fc59d4e7b456699e834a6d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:e8aac9b1598114ead96b4038c19d915b87f662ef342291d69c7e5255c5d731fc in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["bash"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.11.5-c1.11.5
# Thu, 06 Jun 2024 16:24:41 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8091/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:e9aef93137af6e967e7242f3b3c8ecd8e6f571d1e6fdd9e72db0befeeae3cf13`  
		Last Modified: Tue, 02 Jul 2024 01:28:26 GMT  
		Size: 49.6 MB (49554064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b365fa3e8dc16e70d89fab0e91f5242feb38ae3cfeb6655e654209ea109333`  
		Last Modified: Tue, 02 Jul 2024 02:00:17 GMT  
		Size: 24.0 MB (24049794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:367bb40e8733adeb557b66b98ab2bbc04ccdca889800efeb1d28751f10135948`  
		Last Modified: Tue, 02 Jul 2024 03:03:31 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0989e3d61ba8cbea6d809bcf02623e22c3b3cecd10e2757407ee22d82ecfdad1`  
		Last Modified: Tue, 02 Jul 2024 03:03:31 GMT  
		Size: 20.4 MB (20393033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19e131d1486106c7b990ac8ee3b3cc21746c7c7e25a5fac7e89a30c998f82b3`  
		Last Modified: Tue, 02 Jul 2024 03:03:31 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d99e7aadcf492fef1573519a7ebdb3f551d420520578804d3f14cc4967c5858`  
		Last Modified: Tue, 02 Jul 2024 03:03:31 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:7b8d6246377e0550106032397684ad7583ee6b57e1ec429c8aff2911e096b7ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4404129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e5e54a94b1102a92a848c785e35c2fb7586ccfbcdd7466291db8aa6c6eb3a20`

```dockerfile
```

-	Layers:
	-	`sha256:771c8398dfba0df96311d2ef8b7dcc58de599393e87c4a3d11c28def5d457c87`  
		Last Modified: Tue, 02 Jul 2024 03:03:31 GMT  
		Size: 4.4 MB (4391209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f31af46abae28ce1f848fba31742ac75895f469fbb5e28999e1ce08e564895d`  
		Last Modified: Tue, 02 Jul 2024 03:03:30 GMT  
		Size: 12.9 KB (12920 bytes)  
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
$ docker pull influxdb@sha256:e55b98514d700229eb7fa728e706cc3192b81cbc54444a31362047906cf1424e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.5-data` - linux; amd64

```console
$ docker pull influxdb@sha256:d88f1f641e427fba8b577613eef6d42b6e1e76248ab91740c4ab22d444303963
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 MB (115430078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f65689acada4b99e8e6c740ad691854ee28c4bcf20dbe1b0c83e4e0fc8ca29f2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:e8aac9b1598114ead96b4038c19d915b87f662ef342291d69c7e5255c5d731fc in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["bash"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.11.5-c1.11.5
# Thu, 06 Jun 2024 16:24:41 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:e9aef93137af6e967e7242f3b3c8ecd8e6f571d1e6fdd9e72db0befeeae3cf13`  
		Last Modified: Tue, 02 Jul 2024 01:28:26 GMT  
		Size: 49.6 MB (49554064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b365fa3e8dc16e70d89fab0e91f5242feb38ae3cfeb6655e654209ea109333`  
		Last Modified: Tue, 02 Jul 2024 02:00:17 GMT  
		Size: 24.0 MB (24049794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ce8052ded392581255102609c9e762cfe0138ac9f1f84f48273a2d0a75b1ed`  
		Last Modified: Tue, 02 Jul 2024 03:03:25 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cebc80bc73311fe34e10f3be81e11feba0bad1dc630ebee5faf81ddc9fc507e`  
		Last Modified: Tue, 02 Jul 2024 03:03:26 GMT  
		Size: 41.8 MB (41822661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa467c284d08679e8a978718a84df389de45b099bccbd66ec5dd2ff8d7b61a50`  
		Last Modified: Tue, 02 Jul 2024 03:03:25 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa7794091bcf053522fe9f291f59a810358245615301d2293ff4bcba2753864`  
		Last Modified: Tue, 02 Jul 2024 03:03:26 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4276be0cb3620b87a3008de157a4886c17b2ac808a7655b3cdf1e33c836fccfc`  
		Last Modified: Tue, 02 Jul 2024 03:03:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.5-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:62b1208f913bb025d4c2cbb8eba98ce92643a3f3f9c682ed04c97a1c02ccdfa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4468343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:524914c080c1e72a708f9116ed5d50f44637b94e1b4938cff057a94dbeea574c`

```dockerfile
```

-	Layers:
	-	`sha256:5bd9a289241c64d41979d05904e13936a86c7eb15a5287e71a682cb9bba78511`  
		Last Modified: Tue, 02 Jul 2024 03:03:26 GMT  
		Size: 4.5 MB (4453769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b079cae700e0ee816202f847150dd85b8d2589c94e4f5c6759d4dc45a0d6b682`  
		Last Modified: Tue, 02 Jul 2024 03:03:26 GMT  
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
$ docker pull influxdb@sha256:c0fc65a03709ff7b45ebf4b3f99024d7e0e6c6758944e544f447361107d3bc04
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.5-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:073fd87728df8c8e61a5c9c703a6a2d3e17636b526a643fcd5ee520126c1d68e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (93999240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c33eee34a4b90a63e416ae1d57aea7df041589a753fc59d4e7b456699e834a6d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:e8aac9b1598114ead96b4038c19d915b87f662ef342291d69c7e5255c5d731fc in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["bash"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.11.5-c1.11.5
# Thu, 06 Jun 2024 16:24:41 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8091/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:e9aef93137af6e967e7242f3b3c8ecd8e6f571d1e6fdd9e72db0befeeae3cf13`  
		Last Modified: Tue, 02 Jul 2024 01:28:26 GMT  
		Size: 49.6 MB (49554064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b365fa3e8dc16e70d89fab0e91f5242feb38ae3cfeb6655e654209ea109333`  
		Last Modified: Tue, 02 Jul 2024 02:00:17 GMT  
		Size: 24.0 MB (24049794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:367bb40e8733adeb557b66b98ab2bbc04ccdca889800efeb1d28751f10135948`  
		Last Modified: Tue, 02 Jul 2024 03:03:31 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0989e3d61ba8cbea6d809bcf02623e22c3b3cecd10e2757407ee22d82ecfdad1`  
		Last Modified: Tue, 02 Jul 2024 03:03:31 GMT  
		Size: 20.4 MB (20393033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19e131d1486106c7b990ac8ee3b3cc21746c7c7e25a5fac7e89a30c998f82b3`  
		Last Modified: Tue, 02 Jul 2024 03:03:31 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d99e7aadcf492fef1573519a7ebdb3f551d420520578804d3f14cc4967c5858`  
		Last Modified: Tue, 02 Jul 2024 03:03:31 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.5-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:7b8d6246377e0550106032397684ad7583ee6b57e1ec429c8aff2911e096b7ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4404129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e5e54a94b1102a92a848c785e35c2fb7586ccfbcdd7466291db8aa6c6eb3a20`

```dockerfile
```

-	Layers:
	-	`sha256:771c8398dfba0df96311d2ef8b7dcc58de599393e87c4a3d11c28def5d457c87`  
		Last Modified: Tue, 02 Jul 2024 03:03:31 GMT  
		Size: 4.4 MB (4391209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f31af46abae28ce1f848fba31742ac75895f469fbb5e28999e1ce08e564895d`  
		Last Modified: Tue, 02 Jul 2024 03:03:30 GMT  
		Size: 12.9 KB (12920 bytes)  
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
$ docker pull influxdb@sha256:8e068098a8fe81424458b6d0b2d21980723ff57cb0cec2008041733f37cb0994
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
$ docker pull influxdb@sha256:d7777388e9179a6a562c1251c349e0c3b716834ee9d5fcd5d55b317e2e7b7464
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125734423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e608808650dd4593af1168e55154edcccfad20f776758f8078229a2e60deebd9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:b8d066bbda2d783c3ca81ab100fc5e45550234b68fde96332f303f669256842e in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["bash"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.8.10
# Thu, 06 Jun 2024 16:24:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb* # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c1c1a7d83fb1e16686c4e98df3d6f88b37beb4d65daae1ddd715f95d7ac4db5c`  
		Last Modified: Tue, 02 Jul 2024 01:29:07 GMT  
		Size: 55.1 MB (55081360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a305f523084f0a28b5daf532a5216d9be05d863c6bd3f5bd2969965eb7e9a27`  
		Last Modified: Tue, 02 Jul 2024 02:01:21 GMT  
		Size: 15.8 MB (15764174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0a3c2ef21b8a19706215fef27807abe3cf56edad440a864cbb3bd9cee7b5cd`  
		Last Modified: Tue, 02 Jul 2024 03:03:31 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcfa799a51b4782ef38cecb8908061821aa3d3d21b18c946610ffb5e3745c1b2`  
		Last Modified: Tue, 02 Jul 2024 03:03:33 GMT  
		Size: 54.9 MB (54885392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171333e8962c652ce89d2063fe0f59bfb060276496a2426ab845ad0178209513`  
		Last Modified: Tue, 02 Jul 2024 03:03:31 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5c4bbf98d99c4316badaecaa3ccbf6938128d0bef06b49c7e57340ed86d25c`  
		Last Modified: Tue, 02 Jul 2024 03:03:31 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7121dc90affd4971ed4020e7299242e1ca66ba9a802299817210c332eda4486`  
		Last Modified: Tue, 02 Jul 2024 03:03:31 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:2c88d31d0c3637963e2089df8f68d2914fdde13f4f8ba46efb15e925550368ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4478524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63c2c1f1d8cb9d5f738a8f4ac6163411ce32c894f40068346243f588a262655c`

```dockerfile
```

-	Layers:
	-	`sha256:1f7bacbdb64b5165ad27fb0074d56d787495bf3c890988dccb0d2e29c07ae131`  
		Last Modified: Tue, 02 Jul 2024 03:03:31 GMT  
		Size: 4.5 MB (4463062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82068275cc749def54b6e3c9d757a84a8875b64f78665d6321e40440050122fc`  
		Last Modified: Tue, 02 Jul 2024 03:03:31 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.8` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:0d4072c569136a372d8d262fc355aec9ecacd6d94300507eaac3eee25aa645df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.7 MB (116734700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c211e92078bc1a1d11a2b3ebc5c5c6e83bb13e64b7b22e16a9172c7f403ca374`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:6e828fd5dbd54f949f96129ea922c27ff88709484119faef51401e338e900e6e in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["bash"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.8.10
# Thu, 06 Jun 2024 16:24:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb* # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:a0610bbe9cb80952dba5ef5efb55f03668fd4f8ab63ade3ba30e22a4c03c42da`  
		Last Modified: Tue, 02 Jul 2024 01:03:38 GMT  
		Size: 50.2 MB (50238998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c595e4d8c2d2c7ad66ab723b54c73c6a0aa876b01511358ec8af1aed8c8b94`  
		Last Modified: Tue, 02 Jul 2024 01:40:13 GMT  
		Size: 14.9 MB (14879331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6e2a4ec7528583f445ad9fb820ed6f276a627cbad1c5b24f73f06b07542168`  
		Last Modified: Tue, 02 Jul 2024 13:17:30 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9635550b558dbf4e2527f1780a084607b6002306026ac5696ff9e305ae09ac40`  
		Last Modified: Tue, 02 Jul 2024 13:17:33 GMT  
		Size: 51.6 MB (51612881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e352d824917a9d94e5992004f5bdc6aa4713c9198a0d4676b57092d0fde38a2`  
		Last Modified: Tue, 02 Jul 2024 13:17:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5166f2503dd2dadd25a263992ca2641f249d404cad3c4e43b45ba1a73767d40`  
		Last Modified: Tue, 02 Jul 2024 13:17:31 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46c41542a84b72f2becee93151e7b5d69c520b31572248889b932df4af5ef69`  
		Last Modified: Tue, 02 Jul 2024 13:17:32 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:3b6009ab98c3a9fbfdcd9fe927da45d1f06148badc118ab8c0fc76ceab606fab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4480225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7630451841936628fb051c3e730d9e014ec1ef56e71392e2f7220807782c76b`

```dockerfile
```

-	Layers:
	-	`sha256:b5b136d691475d7b306fd877c9493a7ea1f94d3846c37e5ad95a9f33390c9134`  
		Last Modified: Tue, 02 Jul 2024 13:17:31 GMT  
		Size: 4.5 MB (4464696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3ba2719b672f6fdd93fe4d463ccc4d5344fcd9d396a0ffba873147156c0c326`  
		Last Modified: Tue, 02 Jul 2024 13:17:30 GMT  
		Size: 15.5 KB (15529 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:62dc051897a095fc213f3f9d4c7049d73a616ddbc8de031f108094156888c585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120704586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d1994e001e0d14fd0d1db829adfd6f4116241806f4bc37b48d9eb1f2b242cb2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:4e98397394fc6db8fa55fb21c15dab09007b6ba883cb193f3a53f94480fee872 in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["bash"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.8.10
# Thu, 06 Jun 2024 16:24:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb* # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:a4cd3ad66f7873241881d2ddd4efa6521034245e95e2b0b4a059817345151048`  
		Last Modified: Tue, 02 Jul 2024 00:42:43 GMT  
		Size: 53.7 MB (53721653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699d9ac7785741df545f96a8744d3a9a5c29f75a171fb8de0a0bae196294ad50`  
		Last Modified: Tue, 02 Jul 2024 04:02:37 GMT  
		Size: 15.7 MB (15749565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19902d939cd2b6c4fe22bc11e43826e92a1c52dcab3fc724ef00a17345d086c1`  
		Last Modified: Tue, 02 Jul 2024 15:15:50 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c9e5841cd4acd888729691e700ae08dd48f200df8200861713e590ee4a5cde`  
		Last Modified: Tue, 02 Jul 2024 15:15:51 GMT  
		Size: 51.2 MB (51229868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaadb631a79a7ef5b88e36839bf44c66e81dd9d8a8b13d6231fd6bc3bac3c45a`  
		Last Modified: Tue, 02 Jul 2024 15:15:50 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2709c34647dbc08a82569f99a957086f4ebb820386f39bd66a68c220339e95af`  
		Last Modified: Tue, 02 Jul 2024 15:15:50 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175bded8cfa2d8421925b3dba844c279145c58f2cbb2eb2b5f89e0f820879bae`  
		Last Modified: Tue, 02 Jul 2024 15:15:51 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:b3c5b59c7d649a2bfa7731040bd25a3414233bd661593443c3c044336852f7e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4478428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e49e8507272b1fc362bea3924b98d0936db3092fe9b38fc5aa69a28a6dd2335d`

```dockerfile
```

-	Layers:
	-	`sha256:dec990b34d8e67ed72a966e00473277dd451ed451bee890c01a6e0d6c40a304d`  
		Last Modified: Tue, 02 Jul 2024 15:15:50 GMT  
		Size: 4.5 MB (4462674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:296b649b6cff9f13579b6d8b5b1fd072ec8e4533d0e935d55b92a6129ed6179e`  
		Last Modified: Tue, 02 Jul 2024 15:15:50 GMT  
		Size: 15.8 KB (15754 bytes)  
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
$ docker pull influxdb@sha256:8e068098a8fe81424458b6d0b2d21980723ff57cb0cec2008041733f37cb0994
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
$ docker pull influxdb@sha256:d7777388e9179a6a562c1251c349e0c3b716834ee9d5fcd5d55b317e2e7b7464
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125734423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e608808650dd4593af1168e55154edcccfad20f776758f8078229a2e60deebd9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:b8d066bbda2d783c3ca81ab100fc5e45550234b68fde96332f303f669256842e in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["bash"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.8.10
# Thu, 06 Jun 2024 16:24:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb* # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c1c1a7d83fb1e16686c4e98df3d6f88b37beb4d65daae1ddd715f95d7ac4db5c`  
		Last Modified: Tue, 02 Jul 2024 01:29:07 GMT  
		Size: 55.1 MB (55081360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a305f523084f0a28b5daf532a5216d9be05d863c6bd3f5bd2969965eb7e9a27`  
		Last Modified: Tue, 02 Jul 2024 02:01:21 GMT  
		Size: 15.8 MB (15764174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0a3c2ef21b8a19706215fef27807abe3cf56edad440a864cbb3bd9cee7b5cd`  
		Last Modified: Tue, 02 Jul 2024 03:03:31 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcfa799a51b4782ef38cecb8908061821aa3d3d21b18c946610ffb5e3745c1b2`  
		Last Modified: Tue, 02 Jul 2024 03:03:33 GMT  
		Size: 54.9 MB (54885392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171333e8962c652ce89d2063fe0f59bfb060276496a2426ab845ad0178209513`  
		Last Modified: Tue, 02 Jul 2024 03:03:31 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5c4bbf98d99c4316badaecaa3ccbf6938128d0bef06b49c7e57340ed86d25c`  
		Last Modified: Tue, 02 Jul 2024 03:03:31 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7121dc90affd4971ed4020e7299242e1ca66ba9a802299817210c332eda4486`  
		Last Modified: Tue, 02 Jul 2024 03:03:31 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8.10` - unknown; unknown

```console
$ docker pull influxdb@sha256:2c88d31d0c3637963e2089df8f68d2914fdde13f4f8ba46efb15e925550368ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4478524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63c2c1f1d8cb9d5f738a8f4ac6163411ce32c894f40068346243f588a262655c`

```dockerfile
```

-	Layers:
	-	`sha256:1f7bacbdb64b5165ad27fb0074d56d787495bf3c890988dccb0d2e29c07ae131`  
		Last Modified: Tue, 02 Jul 2024 03:03:31 GMT  
		Size: 4.5 MB (4463062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82068275cc749def54b6e3c9d757a84a8875b64f78665d6321e40440050122fc`  
		Last Modified: Tue, 02 Jul 2024 03:03:31 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.8.10` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:0d4072c569136a372d8d262fc355aec9ecacd6d94300507eaac3eee25aa645df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.7 MB (116734700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c211e92078bc1a1d11a2b3ebc5c5c6e83bb13e64b7b22e16a9172c7f403ca374`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:6e828fd5dbd54f949f96129ea922c27ff88709484119faef51401e338e900e6e in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["bash"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.8.10
# Thu, 06 Jun 2024 16:24:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb* # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:a0610bbe9cb80952dba5ef5efb55f03668fd4f8ab63ade3ba30e22a4c03c42da`  
		Last Modified: Tue, 02 Jul 2024 01:03:38 GMT  
		Size: 50.2 MB (50238998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c595e4d8c2d2c7ad66ab723b54c73c6a0aa876b01511358ec8af1aed8c8b94`  
		Last Modified: Tue, 02 Jul 2024 01:40:13 GMT  
		Size: 14.9 MB (14879331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6e2a4ec7528583f445ad9fb820ed6f276a627cbad1c5b24f73f06b07542168`  
		Last Modified: Tue, 02 Jul 2024 13:17:30 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9635550b558dbf4e2527f1780a084607b6002306026ac5696ff9e305ae09ac40`  
		Last Modified: Tue, 02 Jul 2024 13:17:33 GMT  
		Size: 51.6 MB (51612881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e352d824917a9d94e5992004f5bdc6aa4713c9198a0d4676b57092d0fde38a2`  
		Last Modified: Tue, 02 Jul 2024 13:17:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5166f2503dd2dadd25a263992ca2641f249d404cad3c4e43b45ba1a73767d40`  
		Last Modified: Tue, 02 Jul 2024 13:17:31 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46c41542a84b72f2becee93151e7b5d69c520b31572248889b932df4af5ef69`  
		Last Modified: Tue, 02 Jul 2024 13:17:32 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8.10` - unknown; unknown

```console
$ docker pull influxdb@sha256:3b6009ab98c3a9fbfdcd9fe927da45d1f06148badc118ab8c0fc76ceab606fab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4480225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7630451841936628fb051c3e730d9e014ec1ef56e71392e2f7220807782c76b`

```dockerfile
```

-	Layers:
	-	`sha256:b5b136d691475d7b306fd877c9493a7ea1f94d3846c37e5ad95a9f33390c9134`  
		Last Modified: Tue, 02 Jul 2024 13:17:31 GMT  
		Size: 4.5 MB (4464696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3ba2719b672f6fdd93fe4d463ccc4d5344fcd9d396a0ffba873147156c0c326`  
		Last Modified: Tue, 02 Jul 2024 13:17:30 GMT  
		Size: 15.5 KB (15529 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.8.10` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:62dc051897a095fc213f3f9d4c7049d73a616ddbc8de031f108094156888c585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120704586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d1994e001e0d14fd0d1db829adfd6f4116241806f4bc37b48d9eb1f2b242cb2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:4e98397394fc6db8fa55fb21c15dab09007b6ba883cb193f3a53f94480fee872 in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["bash"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.8.10
# Thu, 06 Jun 2024 16:24:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb* # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:a4cd3ad66f7873241881d2ddd4efa6521034245e95e2b0b4a059817345151048`  
		Last Modified: Tue, 02 Jul 2024 00:42:43 GMT  
		Size: 53.7 MB (53721653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699d9ac7785741df545f96a8744d3a9a5c29f75a171fb8de0a0bae196294ad50`  
		Last Modified: Tue, 02 Jul 2024 04:02:37 GMT  
		Size: 15.7 MB (15749565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19902d939cd2b6c4fe22bc11e43826e92a1c52dcab3fc724ef00a17345d086c1`  
		Last Modified: Tue, 02 Jul 2024 15:15:50 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c9e5841cd4acd888729691e700ae08dd48f200df8200861713e590ee4a5cde`  
		Last Modified: Tue, 02 Jul 2024 15:15:51 GMT  
		Size: 51.2 MB (51229868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaadb631a79a7ef5b88e36839bf44c66e81dd9d8a8b13d6231fd6bc3bac3c45a`  
		Last Modified: Tue, 02 Jul 2024 15:15:50 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2709c34647dbc08a82569f99a957086f4ebb820386f39bd66a68c220339e95af`  
		Last Modified: Tue, 02 Jul 2024 15:15:50 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175bded8cfa2d8421925b3dba844c279145c58f2cbb2eb2b5f89e0f820879bae`  
		Last Modified: Tue, 02 Jul 2024 15:15:51 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8.10` - unknown; unknown

```console
$ docker pull influxdb@sha256:b3c5b59c7d649a2bfa7731040bd25a3414233bd661593443c3c044336852f7e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4478428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e49e8507272b1fc362bea3924b98d0936db3092fe9b38fc5aa69a28a6dd2335d`

```dockerfile
```

-	Layers:
	-	`sha256:dec990b34d8e67ed72a966e00473277dd451ed451bee890c01a6e0d6c40a304d`  
		Last Modified: Tue, 02 Jul 2024 15:15:50 GMT  
		Size: 4.5 MB (4462674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:296b649b6cff9f13579b6d8b5b1fd072ec8e4533d0e935d55b92a6129ed6179e`  
		Last Modified: Tue, 02 Jul 2024 15:15:50 GMT  
		Size: 15.8 KB (15754 bytes)  
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
$ docker pull influxdb@sha256:b30f3bdc8a8771f6a3ec241536b046fda29b8b00cea90c50e6eacdfa86d5c05a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9-data` - linux; amd64

```console
$ docker pull influxdb@sha256:7a6b117fc5fd44e0044099a18de5875a4a4c636b865a6c263d94cbadac6bc0e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104138062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e662bbf6d1bbd0dec57f3d3a0c0f300d865ea1a48b5701ac5c72bc055a95d7c2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:b8d066bbda2d783c3ca81ab100fc5e45550234b68fde96332f303f669256842e in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["bash"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Thu, 06 Jun 2024 16:24:41 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb* # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c1c1a7d83fb1e16686c4e98df3d6f88b37beb4d65daae1ddd715f95d7ac4db5c`  
		Last Modified: Tue, 02 Jul 2024 01:29:07 GMT  
		Size: 55.1 MB (55081360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a305f523084f0a28b5daf532a5216d9be05d863c6bd3f5bd2969965eb7e9a27`  
		Last Modified: Tue, 02 Jul 2024 02:01:21 GMT  
		Size: 15.8 MB (15764174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2542c6de99d99e0094138b0d39caeb054355ba196ce9d5bb63b42f6838fc07`  
		Last Modified: Tue, 02 Jul 2024 03:03:30 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d217aa4e787a229be8441d74ad42d3ae3c109bf10ac98087b0b351564dbb796`  
		Last Modified: Tue, 02 Jul 2024 03:03:31 GMT  
		Size: 33.3 MB (33288974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f0bf4e4a337f42e9744a9818ab3c8d9e7d615f2d91eb5da67928993b42e86d`  
		Last Modified: Tue, 02 Jul 2024 03:03:30 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d12f1acb17338240e1aa1d1011cad635dd1fed038859b3dee7b19cab7069f3`  
		Last Modified: Tue, 02 Jul 2024 03:03:30 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7121dc90affd4971ed4020e7299242e1ca66ba9a802299817210c332eda4486`  
		Last Modified: Tue, 02 Jul 2024 03:03:31 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:61095cdc9c73fc1fe3cd311edf3f9f952b61ffe7290c7525a2722629d9f76226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4584609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b62ee20e7d336cc6316b32dd3df8db86aba2fe490c07e8fc5da0a81ea0f0fbae`

```dockerfile
```

-	Layers:
	-	`sha256:78f526dca57fadc382546f89b0a7925ea7f2001a9d2cb32a7fe3187efb0f905c`  
		Last Modified: Tue, 02 Jul 2024 03:03:30 GMT  
		Size: 4.6 MB (4570068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea23e077359c1cb544e1e306099966451afc8c4db9ef9fe03b678d235995efe9`  
		Last Modified: Tue, 02 Jul 2024 03:03:30 GMT  
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
$ docker pull influxdb@sha256:90df9217fcd4e98e423065845be9f11f56e56d75775fbdb33ea191a67533eb4f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:8b78e459a94d228c0a65de927f9b6a73ea1a9b664cc319e4478ffecb70d24535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83617254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c47443da747c514bbb1512c332a653f0882002ae2f6c9f75c223353c66e9d372`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:b8d066bbda2d783c3ca81ab100fc5e45550234b68fde96332f303f669256842e in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["bash"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Thu, 06 Jun 2024 16:24:41 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb* # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8091/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:c1c1a7d83fb1e16686c4e98df3d6f88b37beb4d65daae1ddd715f95d7ac4db5c`  
		Last Modified: Tue, 02 Jul 2024 01:29:07 GMT  
		Size: 55.1 MB (55081360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a305f523084f0a28b5daf532a5216d9be05d863c6bd3f5bd2969965eb7e9a27`  
		Last Modified: Tue, 02 Jul 2024 02:01:21 GMT  
		Size: 15.8 MB (15764174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a708b7fdf27ba4ea64096a2b7827c9f555fb4a5f0e3ce21bd0651b4c31cf1e34`  
		Last Modified: Tue, 02 Jul 2024 03:03:21 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce9e05833d3874ec714a8f8cc51d1b741c9a7ff46cf1800e9dc27816152c5de`  
		Last Modified: Tue, 02 Jul 2024 03:03:21 GMT  
		Size: 12.8 MB (12769369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae68e69940ea6a34912499096a51fb9f6b115f68206dc1886f623045dfec0c49`  
		Last Modified: Tue, 02 Jul 2024 03:03:21 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd196e99f6eb0a495263fbdcbf1f2898d8ee61b0e51af7a8b68273d9e18bab7`  
		Last Modified: Tue, 02 Jul 2024 03:03:22 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:8d045531fdb86a1553243e782a98c03321c142be0bbb450eb216cfd9b988bbe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4529085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f04905ae327d8d538fec190e0762d38f49de3adf7198e0c050742676a940289`

```dockerfile
```

-	Layers:
	-	`sha256:8d65bfb0fb32211c0d2fac08ac5d16259f4ce9fd67833e7555f503743d06c8a9`  
		Last Modified: Tue, 02 Jul 2024 03:03:21 GMT  
		Size: 4.5 MB (4516197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c1e9d5f0594e1c1ae7f7afdca1ec398d2e05b8d9c21f17687c69cea42f21a82`  
		Last Modified: Tue, 02 Jul 2024 03:03:21 GMT  
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
$ docker pull influxdb@sha256:b30f3bdc8a8771f6a3ec241536b046fda29b8b00cea90c50e6eacdfa86d5c05a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9.13-data` - linux; amd64

```console
$ docker pull influxdb@sha256:7a6b117fc5fd44e0044099a18de5875a4a4c636b865a6c263d94cbadac6bc0e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104138062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e662bbf6d1bbd0dec57f3d3a0c0f300d865ea1a48b5701ac5c72bc055a95d7c2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:b8d066bbda2d783c3ca81ab100fc5e45550234b68fde96332f303f669256842e in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["bash"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Thu, 06 Jun 2024 16:24:41 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb* # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c1c1a7d83fb1e16686c4e98df3d6f88b37beb4d65daae1ddd715f95d7ac4db5c`  
		Last Modified: Tue, 02 Jul 2024 01:29:07 GMT  
		Size: 55.1 MB (55081360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a305f523084f0a28b5daf532a5216d9be05d863c6bd3f5bd2969965eb7e9a27`  
		Last Modified: Tue, 02 Jul 2024 02:01:21 GMT  
		Size: 15.8 MB (15764174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2542c6de99d99e0094138b0d39caeb054355ba196ce9d5bb63b42f6838fc07`  
		Last Modified: Tue, 02 Jul 2024 03:03:30 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d217aa4e787a229be8441d74ad42d3ae3c109bf10ac98087b0b351564dbb796`  
		Last Modified: Tue, 02 Jul 2024 03:03:31 GMT  
		Size: 33.3 MB (33288974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f0bf4e4a337f42e9744a9818ab3c8d9e7d615f2d91eb5da67928993b42e86d`  
		Last Modified: Tue, 02 Jul 2024 03:03:30 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d12f1acb17338240e1aa1d1011cad635dd1fed038859b3dee7b19cab7069f3`  
		Last Modified: Tue, 02 Jul 2024 03:03:30 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7121dc90affd4971ed4020e7299242e1ca66ba9a802299817210c332eda4486`  
		Last Modified: Tue, 02 Jul 2024 03:03:31 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9.13-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:61095cdc9c73fc1fe3cd311edf3f9f952b61ffe7290c7525a2722629d9f76226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4584609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b62ee20e7d336cc6316b32dd3df8db86aba2fe490c07e8fc5da0a81ea0f0fbae`

```dockerfile
```

-	Layers:
	-	`sha256:78f526dca57fadc382546f89b0a7925ea7f2001a9d2cb32a7fe3187efb0f905c`  
		Last Modified: Tue, 02 Jul 2024 03:03:30 GMT  
		Size: 4.6 MB (4570068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea23e077359c1cb544e1e306099966451afc8c4db9ef9fe03b678d235995efe9`  
		Last Modified: Tue, 02 Jul 2024 03:03:30 GMT  
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
$ docker pull influxdb@sha256:90df9217fcd4e98e423065845be9f11f56e56d75775fbdb33ea191a67533eb4f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9.13-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:8b78e459a94d228c0a65de927f9b6a73ea1a9b664cc319e4478ffecb70d24535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83617254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c47443da747c514bbb1512c332a653f0882002ae2f6c9f75c223353c66e9d372`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:b8d066bbda2d783c3ca81ab100fc5e45550234b68fde96332f303f669256842e in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["bash"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Thu, 06 Jun 2024 16:24:41 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb* # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8091/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:c1c1a7d83fb1e16686c4e98df3d6f88b37beb4d65daae1ddd715f95d7ac4db5c`  
		Last Modified: Tue, 02 Jul 2024 01:29:07 GMT  
		Size: 55.1 MB (55081360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a305f523084f0a28b5daf532a5216d9be05d863c6bd3f5bd2969965eb7e9a27`  
		Last Modified: Tue, 02 Jul 2024 02:01:21 GMT  
		Size: 15.8 MB (15764174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a708b7fdf27ba4ea64096a2b7827c9f555fb4a5f0e3ce21bd0651b4c31cf1e34`  
		Last Modified: Tue, 02 Jul 2024 03:03:21 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce9e05833d3874ec714a8f8cc51d1b741c9a7ff46cf1800e9dc27816152c5de`  
		Last Modified: Tue, 02 Jul 2024 03:03:21 GMT  
		Size: 12.8 MB (12769369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae68e69940ea6a34912499096a51fb9f6b115f68206dc1886f623045dfec0c49`  
		Last Modified: Tue, 02 Jul 2024 03:03:21 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd196e99f6eb0a495263fbdcbf1f2898d8ee61b0e51af7a8b68273d9e18bab7`  
		Last Modified: Tue, 02 Jul 2024 03:03:22 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9.13-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:8d045531fdb86a1553243e782a98c03321c142be0bbb450eb216cfd9b988bbe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4529085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f04905ae327d8d538fec190e0762d38f49de3adf7198e0c050742676a940289`

```dockerfile
```

-	Layers:
	-	`sha256:8d65bfb0fb32211c0d2fac08ac5d16259f4ce9fd67833e7555f503743d06c8a9`  
		Last Modified: Tue, 02 Jul 2024 03:03:21 GMT  
		Size: 4.5 MB (4516197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c1e9d5f0594e1c1ae7f7afdca1ec398d2e05b8d9c21f17687c69cea42f21a82`  
		Last Modified: Tue, 02 Jul 2024 03:03:21 GMT  
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
$ docker pull influxdb@sha256:fd9b2692e0291b9f7731171de82a5943ea23356b0bee358cf9a7336b7260c65d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2` - linux; amd64

```console
$ docker pull influxdb@sha256:b2a9675c4500505de4f90163d512cf75f05c9d42cd7d5ec24db26e945443acfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168482795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a8b8cd9a7028b8b3433ab3f9df9fa37ad306501b79aad51b65c86abc28ab5af`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:02 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Tue, 02 Jul 2024 01:25:02 GMT
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
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245b750b3dbd4ecd8d4bf1dd2fa4152bed134157231886e67d9c6cd77d96d170`  
		Last Modified: Fri, 12 Jul 2024 00:56:00 GMT  
		Size: 9.8 MB (9786173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ffee79c9f66f54445f932a31f35d69c307f3248b7ad361641facd54fb68bb4`  
		Last Modified: Fri, 12 Jul 2024 00:56:00 GMT  
		Size: 5.8 MB (5820923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89624f628a1ab632599c90a54366782cf776104fd5d9fab77ef8447c34efbae4`  
		Last Modified: Fri, 12 Jul 2024 00:56:00 GMT  
		Size: 3.2 KB (3229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb932efdd4b8e8932418cbc3f4504137a54c3943d9b6e0df2c3d8ed2c52b7ce2`  
		Last Modified: Fri, 12 Jul 2024 00:56:00 GMT  
		Size: 1.0 MB (1006361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42295cbddaebd3646d97b87d9eb89d862354c98f4818dbd911b54b7d7ec7d7be`  
		Last Modified: Fri, 12 Jul 2024 00:56:02 GMT  
		Size: 99.6 MB (99604809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b0d26b4cd4afd57521f2a33f835e8f92df6640fcc78d06c946cbd0717db649`  
		Last Modified: Fri, 12 Jul 2024 00:56:01 GMT  
		Size: 23.1 MB (23128291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2823098ad982a9610360972234c674c4320736afd8156e8e737d25116be8aecd`  
		Last Modified: Fri, 12 Jul 2024 00:56:01 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe53c7a8bf1ec8290c6b080b4dcd2480131e925eb5fee92e56774d688084b39`  
		Last Modified: Fri, 12 Jul 2024 00:56:01 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a489731c1c780adbbcd02f9e9a78fdcc23b27849be6409f99addc2bed16984`  
		Last Modified: Fri, 12 Jul 2024 00:56:02 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:9352e0abfc848eb75b889e6cc5be4db50f96e3d0180644ddc2722c87b5ab6fcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2806269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c130c086dc63d64acd58bd3fd98d0ff6b0b16cc95c9f6184ab1fbe4aa22d8fa`

```dockerfile
```

-	Layers:
	-	`sha256:3c62ba2ed7795a5f89c1543a6ff2300402aaf5a324a4aa584866e50967a712fe`  
		Last Modified: Fri, 12 Jul 2024 00:56:00 GMT  
		Size: 2.8 MB (2772729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cca6c7303977c50501549610ff3950a75c65746f8ac5edf908dd3e898681ff8c`  
		Last Modified: Fri, 12 Jul 2024 00:56:00 GMT  
		Size: 33.5 KB (33540 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:ab4068e140d69eefb8f5134d8443402564857a760c4ac63c4a2640a59c5df8fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162257359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:babfb21c041ece360b0ebe226ced2dc006af72520146e2384978f3017d4e108a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:37 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Tue, 02 Jul 2024 00:39:37 GMT
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
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b786576aaeced8d0e3f4629cddc33ef3344b02b423e70f90628575293158876`  
		Last Modified: Fri, 12 Jul 2024 00:59:21 GMT  
		Size: 9.6 MB (9585141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e06d2219f0fc643d914caf4964dc79404236a9b66c8f5c5d4fddd70c27bbb5`  
		Last Modified: Fri, 12 Jul 2024 00:59:21 GMT  
		Size: 5.5 MB (5463798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af9beabe444dc89beef8e076bd658fb482b85f2548cb732dd5654f9d827158a`  
		Last Modified: Fri, 12 Jul 2024 00:59:20 GMT  
		Size: 3.2 KB (3227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582b012d6a97c3b5b46ae224b4773f900ce31fcefcd2445e201c57cedce4fa3c`  
		Last Modified: Fri, 12 Jul 2024 00:59:21 GMT  
		Size: 936.1 KB (936108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67162d043b41d2a09da357e28b87e5692bcf86fe1da5a9098aded9e4685376c4`  
		Last Modified: Fri, 12 Jul 2024 00:59:24 GMT  
		Size: 95.4 MB (95443266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b80ca3e3b97268665dc499c3639e9c915dabbaefe90225f33c4ee06ef6f6aa`  
		Last Modified: Fri, 12 Jul 2024 00:59:23 GMT  
		Size: 21.7 MB (21662524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef963534d0ea920ef82a986acec28d723c959c1c7ae7f4b3524b4accbc36cf9a`  
		Last Modified: Fri, 12 Jul 2024 00:59:22 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36930f0576c0362da87435f16eee2b6a17ff8d5f48f762f94b47ca4e1c41144`  
		Last Modified: Fri, 12 Jul 2024 00:59:22 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9bdede93fcba6ad11c582c806a9dcf9efe2095d22f4a21faf41d99fc87b37f`  
		Last Modified: Fri, 12 Jul 2024 00:59:23 GMT  
		Size: 6.3 KB (6288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:d342327984c78c72d419eeec2121a4e910e18cebca5403a4ea80cce8b476e5af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2805952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f65d349eee61c68c824c6b9dfae1c44b5dfb1c7d7a6b002a598038e4dac827f2`

```dockerfile
```

-	Layers:
	-	`sha256:22efa2d1de5ebc19032c4f173980ae813739f9b300f5c189076dfe023fae3d57`  
		Last Modified: Fri, 12 Jul 2024 00:59:21 GMT  
		Size: 2.8 MB (2772109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f7a2c5672308769994adaa03596da27088e67af9012114a696c3cc8d2aa64aa`  
		Last Modified: Fri, 12 Jul 2024 00:59:20 GMT  
		Size: 33.8 KB (33843 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2-alpine`

```console
$ docker pull influxdb@sha256:a210c27936248e77d1646bd9e2e14c3c05fbc9c7c1f70768f76f866e24fd6bdb
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
$ docker pull influxdb@sha256:450e152aa5087036710ff4f22f9e50f246f38e163260b218604f31ece446b625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88700622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60331e48743fd295013bcde9d8415219874150a88a3b2391288902e5525dccd7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
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
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7966ee58330d4838baa8b7f3790f1657e653c93e6af13f44a3a9e7ad5cab0aec`  
		Last Modified: Fri, 12 Jul 2024 00:59:50 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033c6a8887d050280cf2c7951a2c06d0a779601e7c24bbf367503decb0147188`  
		Last Modified: Fri, 12 Jul 2024 00:59:50 GMT  
		Size: 9.8 MB (9760271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8dc45b737a429d43d9159b709779ab55cb50ce09059ddce29740841968d08b`  
		Last Modified: Fri, 12 Jul 2024 00:59:50 GMT  
		Size: 5.5 MB (5463802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd3be33b2bcb4be0b1f745245347519b3af5ed664588610d6702a68467d4e6a`  
		Last Modified: Fri, 12 Jul 2024 00:59:50 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ecd7b8bdd121b8e849c8a91e540c1afa835c3e4337da8b50dc91ab94018984`  
		Last Modified: Fri, 12 Jul 2024 00:59:52 GMT  
		Size: 47.7 MB (47717265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:321e84a4ac3529aa6dd255e308ba9df3c09f4f0edb9a2e47b71eaaa8a5fd3549`  
		Last Modified: Fri, 12 Jul 2024 00:59:52 GMT  
		Size: 21.7 MB (21662512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd5d15bf6a575f4472da34ad84e79ef39f7f527772f85acd96f7f824fe1fb40`  
		Last Modified: Fri, 12 Jul 2024 00:59:52 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45250427d97aa0c820a41df90d98dc88c7f5becc7ca4c40da12ff26b9e6443df`  
		Last Modified: Fri, 12 Jul 2024 00:59:52 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8259f1217c391e86ec6f5ea2b73cd8e7ca976f7dc3dfc5eb34ab41035d26ae6a`  
		Last Modified: Fri, 12 Jul 2024 00:59:52 GMT  
		Size: 6.3 KB (6283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:e133ec2fa0631cf8507bff16aecbd91c2dd6a2228452dd3586be5b470560a691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **900.8 KB (900788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d65cd96be187154def8dbc5f6759e7ce1ede0e23b85a6c416eaa6dd87b61a6a`

```dockerfile
```

-	Layers:
	-	`sha256:5c350da9e39aa184aaf4fb6ca36e515a98e5431217bbe1833d6a1fcbac4cbdf3`  
		Last Modified: Fri, 12 Jul 2024 00:59:50 GMT  
		Size: 869.7 KB (869741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dc93909d32c197cd0366637e383af1f40f2a2e9ae0224531f36db1a289e4b7e`  
		Last Modified: Fri, 12 Jul 2024 00:59:50 GMT  
		Size: 31.0 KB (31047 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7`

```console
$ docker pull influxdb@sha256:fd9b2692e0291b9f7731171de82a5943ea23356b0bee358cf9a7336b7260c65d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7` - linux; amd64

```console
$ docker pull influxdb@sha256:b2a9675c4500505de4f90163d512cf75f05c9d42cd7d5ec24db26e945443acfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168482795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a8b8cd9a7028b8b3433ab3f9df9fa37ad306501b79aad51b65c86abc28ab5af`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:02 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Tue, 02 Jul 2024 01:25:02 GMT
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
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245b750b3dbd4ecd8d4bf1dd2fa4152bed134157231886e67d9c6cd77d96d170`  
		Last Modified: Fri, 12 Jul 2024 00:56:00 GMT  
		Size: 9.8 MB (9786173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ffee79c9f66f54445f932a31f35d69c307f3248b7ad361641facd54fb68bb4`  
		Last Modified: Fri, 12 Jul 2024 00:56:00 GMT  
		Size: 5.8 MB (5820923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89624f628a1ab632599c90a54366782cf776104fd5d9fab77ef8447c34efbae4`  
		Last Modified: Fri, 12 Jul 2024 00:56:00 GMT  
		Size: 3.2 KB (3229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb932efdd4b8e8932418cbc3f4504137a54c3943d9b6e0df2c3d8ed2c52b7ce2`  
		Last Modified: Fri, 12 Jul 2024 00:56:00 GMT  
		Size: 1.0 MB (1006361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42295cbddaebd3646d97b87d9eb89d862354c98f4818dbd911b54b7d7ec7d7be`  
		Last Modified: Fri, 12 Jul 2024 00:56:02 GMT  
		Size: 99.6 MB (99604809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b0d26b4cd4afd57521f2a33f835e8f92df6640fcc78d06c946cbd0717db649`  
		Last Modified: Fri, 12 Jul 2024 00:56:01 GMT  
		Size: 23.1 MB (23128291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2823098ad982a9610360972234c674c4320736afd8156e8e737d25116be8aecd`  
		Last Modified: Fri, 12 Jul 2024 00:56:01 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe53c7a8bf1ec8290c6b080b4dcd2480131e925eb5fee92e56774d688084b39`  
		Last Modified: Fri, 12 Jul 2024 00:56:01 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a489731c1c780adbbcd02f9e9a78fdcc23b27849be6409f99addc2bed16984`  
		Last Modified: Fri, 12 Jul 2024 00:56:02 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:9352e0abfc848eb75b889e6cc5be4db50f96e3d0180644ddc2722c87b5ab6fcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2806269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c130c086dc63d64acd58bd3fd98d0ff6b0b16cc95c9f6184ab1fbe4aa22d8fa`

```dockerfile
```

-	Layers:
	-	`sha256:3c62ba2ed7795a5f89c1543a6ff2300402aaf5a324a4aa584866e50967a712fe`  
		Last Modified: Fri, 12 Jul 2024 00:56:00 GMT  
		Size: 2.8 MB (2772729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cca6c7303977c50501549610ff3950a75c65746f8ac5edf908dd3e898681ff8c`  
		Last Modified: Fri, 12 Jul 2024 00:56:00 GMT  
		Size: 33.5 KB (33540 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:ab4068e140d69eefb8f5134d8443402564857a760c4ac63c4a2640a59c5df8fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162257359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:babfb21c041ece360b0ebe226ced2dc006af72520146e2384978f3017d4e108a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:37 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Tue, 02 Jul 2024 00:39:37 GMT
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
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b786576aaeced8d0e3f4629cddc33ef3344b02b423e70f90628575293158876`  
		Last Modified: Fri, 12 Jul 2024 00:59:21 GMT  
		Size: 9.6 MB (9585141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e06d2219f0fc643d914caf4964dc79404236a9b66c8f5c5d4fddd70c27bbb5`  
		Last Modified: Fri, 12 Jul 2024 00:59:21 GMT  
		Size: 5.5 MB (5463798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af9beabe444dc89beef8e076bd658fb482b85f2548cb732dd5654f9d827158a`  
		Last Modified: Fri, 12 Jul 2024 00:59:20 GMT  
		Size: 3.2 KB (3227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582b012d6a97c3b5b46ae224b4773f900ce31fcefcd2445e201c57cedce4fa3c`  
		Last Modified: Fri, 12 Jul 2024 00:59:21 GMT  
		Size: 936.1 KB (936108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67162d043b41d2a09da357e28b87e5692bcf86fe1da5a9098aded9e4685376c4`  
		Last Modified: Fri, 12 Jul 2024 00:59:24 GMT  
		Size: 95.4 MB (95443266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b80ca3e3b97268665dc499c3639e9c915dabbaefe90225f33c4ee06ef6f6aa`  
		Last Modified: Fri, 12 Jul 2024 00:59:23 GMT  
		Size: 21.7 MB (21662524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef963534d0ea920ef82a986acec28d723c959c1c7ae7f4b3524b4accbc36cf9a`  
		Last Modified: Fri, 12 Jul 2024 00:59:22 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36930f0576c0362da87435f16eee2b6a17ff8d5f48f762f94b47ca4e1c41144`  
		Last Modified: Fri, 12 Jul 2024 00:59:22 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9bdede93fcba6ad11c582c806a9dcf9efe2095d22f4a21faf41d99fc87b37f`  
		Last Modified: Fri, 12 Jul 2024 00:59:23 GMT  
		Size: 6.3 KB (6288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:d342327984c78c72d419eeec2121a4e910e18cebca5403a4ea80cce8b476e5af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2805952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f65d349eee61c68c824c6b9dfae1c44b5dfb1c7d7a6b002a598038e4dac827f2`

```dockerfile
```

-	Layers:
	-	`sha256:22efa2d1de5ebc19032c4f173980ae813739f9b300f5c189076dfe023fae3d57`  
		Last Modified: Fri, 12 Jul 2024 00:59:21 GMT  
		Size: 2.8 MB (2772109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f7a2c5672308769994adaa03596da27088e67af9012114a696c3cc8d2aa64aa`  
		Last Modified: Fri, 12 Jul 2024 00:59:20 GMT  
		Size: 33.8 KB (33843 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7-alpine`

```console
$ docker pull influxdb@sha256:a210c27936248e77d1646bd9e2e14c3c05fbc9c7c1f70768f76f866e24fd6bdb
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
$ docker pull influxdb@sha256:450e152aa5087036710ff4f22f9e50f246f38e163260b218604f31ece446b625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88700622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60331e48743fd295013bcde9d8415219874150a88a3b2391288902e5525dccd7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
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
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7966ee58330d4838baa8b7f3790f1657e653c93e6af13f44a3a9e7ad5cab0aec`  
		Last Modified: Fri, 12 Jul 2024 00:59:50 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033c6a8887d050280cf2c7951a2c06d0a779601e7c24bbf367503decb0147188`  
		Last Modified: Fri, 12 Jul 2024 00:59:50 GMT  
		Size: 9.8 MB (9760271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8dc45b737a429d43d9159b709779ab55cb50ce09059ddce29740841968d08b`  
		Last Modified: Fri, 12 Jul 2024 00:59:50 GMT  
		Size: 5.5 MB (5463802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd3be33b2bcb4be0b1f745245347519b3af5ed664588610d6702a68467d4e6a`  
		Last Modified: Fri, 12 Jul 2024 00:59:50 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ecd7b8bdd121b8e849c8a91e540c1afa835c3e4337da8b50dc91ab94018984`  
		Last Modified: Fri, 12 Jul 2024 00:59:52 GMT  
		Size: 47.7 MB (47717265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:321e84a4ac3529aa6dd255e308ba9df3c09f4f0edb9a2e47b71eaaa8a5fd3549`  
		Last Modified: Fri, 12 Jul 2024 00:59:52 GMT  
		Size: 21.7 MB (21662512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd5d15bf6a575f4472da34ad84e79ef39f7f527772f85acd96f7f824fe1fb40`  
		Last Modified: Fri, 12 Jul 2024 00:59:52 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45250427d97aa0c820a41df90d98dc88c7f5becc7ca4c40da12ff26b9e6443df`  
		Last Modified: Fri, 12 Jul 2024 00:59:52 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8259f1217c391e86ec6f5ea2b73cd8e7ca976f7dc3dfc5eb34ab41035d26ae6a`  
		Last Modified: Fri, 12 Jul 2024 00:59:52 GMT  
		Size: 6.3 KB (6283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:e133ec2fa0631cf8507bff16aecbd91c2dd6a2228452dd3586be5b470560a691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **900.8 KB (900788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d65cd96be187154def8dbc5f6759e7ce1ede0e23b85a6c416eaa6dd87b61a6a`

```dockerfile
```

-	Layers:
	-	`sha256:5c350da9e39aa184aaf4fb6ca36e515a98e5431217bbe1833d6a1fcbac4cbdf3`  
		Last Modified: Fri, 12 Jul 2024 00:59:50 GMT  
		Size: 869.7 KB (869741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dc93909d32c197cd0366637e383af1f40f2a2e9ae0224531f36db1a289e4b7e`  
		Last Modified: Fri, 12 Jul 2024 00:59:50 GMT  
		Size: 31.0 KB (31047 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7.7`

```console
$ docker pull influxdb@sha256:fd9b2692e0291b9f7731171de82a5943ea23356b0bee358cf9a7336b7260c65d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7.7` - linux; amd64

```console
$ docker pull influxdb@sha256:b2a9675c4500505de4f90163d512cf75f05c9d42cd7d5ec24db26e945443acfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168482795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a8b8cd9a7028b8b3433ab3f9df9fa37ad306501b79aad51b65c86abc28ab5af`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:02 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Tue, 02 Jul 2024 01:25:02 GMT
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
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245b750b3dbd4ecd8d4bf1dd2fa4152bed134157231886e67d9c6cd77d96d170`  
		Last Modified: Fri, 12 Jul 2024 00:56:00 GMT  
		Size: 9.8 MB (9786173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ffee79c9f66f54445f932a31f35d69c307f3248b7ad361641facd54fb68bb4`  
		Last Modified: Fri, 12 Jul 2024 00:56:00 GMT  
		Size: 5.8 MB (5820923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89624f628a1ab632599c90a54366782cf776104fd5d9fab77ef8447c34efbae4`  
		Last Modified: Fri, 12 Jul 2024 00:56:00 GMT  
		Size: 3.2 KB (3229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb932efdd4b8e8932418cbc3f4504137a54c3943d9b6e0df2c3d8ed2c52b7ce2`  
		Last Modified: Fri, 12 Jul 2024 00:56:00 GMT  
		Size: 1.0 MB (1006361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42295cbddaebd3646d97b87d9eb89d862354c98f4818dbd911b54b7d7ec7d7be`  
		Last Modified: Fri, 12 Jul 2024 00:56:02 GMT  
		Size: 99.6 MB (99604809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b0d26b4cd4afd57521f2a33f835e8f92df6640fcc78d06c946cbd0717db649`  
		Last Modified: Fri, 12 Jul 2024 00:56:01 GMT  
		Size: 23.1 MB (23128291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2823098ad982a9610360972234c674c4320736afd8156e8e737d25116be8aecd`  
		Last Modified: Fri, 12 Jul 2024 00:56:01 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe53c7a8bf1ec8290c6b080b4dcd2480131e925eb5fee92e56774d688084b39`  
		Last Modified: Fri, 12 Jul 2024 00:56:01 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a489731c1c780adbbcd02f9e9a78fdcc23b27849be6409f99addc2bed16984`  
		Last Modified: Fri, 12 Jul 2024 00:56:02 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:9352e0abfc848eb75b889e6cc5be4db50f96e3d0180644ddc2722c87b5ab6fcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2806269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c130c086dc63d64acd58bd3fd98d0ff6b0b16cc95c9f6184ab1fbe4aa22d8fa`

```dockerfile
```

-	Layers:
	-	`sha256:3c62ba2ed7795a5f89c1543a6ff2300402aaf5a324a4aa584866e50967a712fe`  
		Last Modified: Fri, 12 Jul 2024 00:56:00 GMT  
		Size: 2.8 MB (2772729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cca6c7303977c50501549610ff3950a75c65746f8ac5edf908dd3e898681ff8c`  
		Last Modified: Fri, 12 Jul 2024 00:56:00 GMT  
		Size: 33.5 KB (33540 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7.7` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:ab4068e140d69eefb8f5134d8443402564857a760c4ac63c4a2640a59c5df8fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162257359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:babfb21c041ece360b0ebe226ced2dc006af72520146e2384978f3017d4e108a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:37 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Tue, 02 Jul 2024 00:39:37 GMT
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
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b786576aaeced8d0e3f4629cddc33ef3344b02b423e70f90628575293158876`  
		Last Modified: Fri, 12 Jul 2024 00:59:21 GMT  
		Size: 9.6 MB (9585141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e06d2219f0fc643d914caf4964dc79404236a9b66c8f5c5d4fddd70c27bbb5`  
		Last Modified: Fri, 12 Jul 2024 00:59:21 GMT  
		Size: 5.5 MB (5463798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af9beabe444dc89beef8e076bd658fb482b85f2548cb732dd5654f9d827158a`  
		Last Modified: Fri, 12 Jul 2024 00:59:20 GMT  
		Size: 3.2 KB (3227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582b012d6a97c3b5b46ae224b4773f900ce31fcefcd2445e201c57cedce4fa3c`  
		Last Modified: Fri, 12 Jul 2024 00:59:21 GMT  
		Size: 936.1 KB (936108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67162d043b41d2a09da357e28b87e5692bcf86fe1da5a9098aded9e4685376c4`  
		Last Modified: Fri, 12 Jul 2024 00:59:24 GMT  
		Size: 95.4 MB (95443266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b80ca3e3b97268665dc499c3639e9c915dabbaefe90225f33c4ee06ef6f6aa`  
		Last Modified: Fri, 12 Jul 2024 00:59:23 GMT  
		Size: 21.7 MB (21662524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef963534d0ea920ef82a986acec28d723c959c1c7ae7f4b3524b4accbc36cf9a`  
		Last Modified: Fri, 12 Jul 2024 00:59:22 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36930f0576c0362da87435f16eee2b6a17ff8d5f48f762f94b47ca4e1c41144`  
		Last Modified: Fri, 12 Jul 2024 00:59:22 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9bdede93fcba6ad11c582c806a9dcf9efe2095d22f4a21faf41d99fc87b37f`  
		Last Modified: Fri, 12 Jul 2024 00:59:23 GMT  
		Size: 6.3 KB (6288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:d342327984c78c72d419eeec2121a4e910e18cebca5403a4ea80cce8b476e5af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2805952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f65d349eee61c68c824c6b9dfae1c44b5dfb1c7d7a6b002a598038e4dac827f2`

```dockerfile
```

-	Layers:
	-	`sha256:22efa2d1de5ebc19032c4f173980ae813739f9b300f5c189076dfe023fae3d57`  
		Last Modified: Fri, 12 Jul 2024 00:59:21 GMT  
		Size: 2.8 MB (2772109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f7a2c5672308769994adaa03596da27088e67af9012114a696c3cc8d2aa64aa`  
		Last Modified: Fri, 12 Jul 2024 00:59:20 GMT  
		Size: 33.8 KB (33843 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7.7-alpine`

```console
$ docker pull influxdb@sha256:a210c27936248e77d1646bd9e2e14c3c05fbc9c7c1f70768f76f866e24fd6bdb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7.7-alpine` - linux; amd64

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

### `influxdb:2.7.7-alpine` - unknown; unknown

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

### `influxdb:2.7.7-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:450e152aa5087036710ff4f22f9e50f246f38e163260b218604f31ece446b625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88700622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60331e48743fd295013bcde9d8415219874150a88a3b2391288902e5525dccd7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
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
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7966ee58330d4838baa8b7f3790f1657e653c93e6af13f44a3a9e7ad5cab0aec`  
		Last Modified: Fri, 12 Jul 2024 00:59:50 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033c6a8887d050280cf2c7951a2c06d0a779601e7c24bbf367503decb0147188`  
		Last Modified: Fri, 12 Jul 2024 00:59:50 GMT  
		Size: 9.8 MB (9760271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8dc45b737a429d43d9159b709779ab55cb50ce09059ddce29740841968d08b`  
		Last Modified: Fri, 12 Jul 2024 00:59:50 GMT  
		Size: 5.5 MB (5463802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd3be33b2bcb4be0b1f745245347519b3af5ed664588610d6702a68467d4e6a`  
		Last Modified: Fri, 12 Jul 2024 00:59:50 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ecd7b8bdd121b8e849c8a91e540c1afa835c3e4337da8b50dc91ab94018984`  
		Last Modified: Fri, 12 Jul 2024 00:59:52 GMT  
		Size: 47.7 MB (47717265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:321e84a4ac3529aa6dd255e308ba9df3c09f4f0edb9a2e47b71eaaa8a5fd3549`  
		Last Modified: Fri, 12 Jul 2024 00:59:52 GMT  
		Size: 21.7 MB (21662512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd5d15bf6a575f4472da34ad84e79ef39f7f527772f85acd96f7f824fe1fb40`  
		Last Modified: Fri, 12 Jul 2024 00:59:52 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45250427d97aa0c820a41df90d98dc88c7f5becc7ca4c40da12ff26b9e6443df`  
		Last Modified: Fri, 12 Jul 2024 00:59:52 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8259f1217c391e86ec6f5ea2b73cd8e7ca976f7dc3dfc5eb34ab41035d26ae6a`  
		Last Modified: Fri, 12 Jul 2024 00:59:52 GMT  
		Size: 6.3 KB (6283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.7-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:e133ec2fa0631cf8507bff16aecbd91c2dd6a2228452dd3586be5b470560a691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **900.8 KB (900788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d65cd96be187154def8dbc5f6759e7ce1ede0e23b85a6c416eaa6dd87b61a6a`

```dockerfile
```

-	Layers:
	-	`sha256:5c350da9e39aa184aaf4fb6ca36e515a98e5431217bbe1833d6a1fcbac4cbdf3`  
		Last Modified: Fri, 12 Jul 2024 00:59:50 GMT  
		Size: 869.7 KB (869741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dc93909d32c197cd0366637e383af1f40f2a2e9ae0224531f36db1a289e4b7e`  
		Last Modified: Fri, 12 Jul 2024 00:59:50 GMT  
		Size: 31.0 KB (31047 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:a210c27936248e77d1646bd9e2e14c3c05fbc9c7c1f70768f76f866e24fd6bdb
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
$ docker pull influxdb@sha256:450e152aa5087036710ff4f22f9e50f246f38e163260b218604f31ece446b625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88700622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60331e48743fd295013bcde9d8415219874150a88a3b2391288902e5525dccd7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
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
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7966ee58330d4838baa8b7f3790f1657e653c93e6af13f44a3a9e7ad5cab0aec`  
		Last Modified: Fri, 12 Jul 2024 00:59:50 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033c6a8887d050280cf2c7951a2c06d0a779601e7c24bbf367503decb0147188`  
		Last Modified: Fri, 12 Jul 2024 00:59:50 GMT  
		Size: 9.8 MB (9760271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8dc45b737a429d43d9159b709779ab55cb50ce09059ddce29740841968d08b`  
		Last Modified: Fri, 12 Jul 2024 00:59:50 GMT  
		Size: 5.5 MB (5463802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd3be33b2bcb4be0b1f745245347519b3af5ed664588610d6702a68467d4e6a`  
		Last Modified: Fri, 12 Jul 2024 00:59:50 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ecd7b8bdd121b8e849c8a91e540c1afa835c3e4337da8b50dc91ab94018984`  
		Last Modified: Fri, 12 Jul 2024 00:59:52 GMT  
		Size: 47.7 MB (47717265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:321e84a4ac3529aa6dd255e308ba9df3c09f4f0edb9a2e47b71eaaa8a5fd3549`  
		Last Modified: Fri, 12 Jul 2024 00:59:52 GMT  
		Size: 21.7 MB (21662512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd5d15bf6a575f4472da34ad84e79ef39f7f527772f85acd96f7f824fe1fb40`  
		Last Modified: Fri, 12 Jul 2024 00:59:52 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45250427d97aa0c820a41df90d98dc88c7f5becc7ca4c40da12ff26b9e6443df`  
		Last Modified: Fri, 12 Jul 2024 00:59:52 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8259f1217c391e86ec6f5ea2b73cd8e7ca976f7dc3dfc5eb34ab41035d26ae6a`  
		Last Modified: Fri, 12 Jul 2024 00:59:52 GMT  
		Size: 6.3 KB (6283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:e133ec2fa0631cf8507bff16aecbd91c2dd6a2228452dd3586be5b470560a691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **900.8 KB (900788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d65cd96be187154def8dbc5f6759e7ce1ede0e23b85a6c416eaa6dd87b61a6a`

```dockerfile
```

-	Layers:
	-	`sha256:5c350da9e39aa184aaf4fb6ca36e515a98e5431217bbe1833d6a1fcbac4cbdf3`  
		Last Modified: Fri, 12 Jul 2024 00:59:50 GMT  
		Size: 869.7 KB (869741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dc93909d32c197cd0366637e383af1f40f2a2e9ae0224531f36db1a289e4b7e`  
		Last Modified: Fri, 12 Jul 2024 00:59:50 GMT  
		Size: 31.0 KB (31047 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:latest`

```console
$ docker pull influxdb@sha256:fd9b2692e0291b9f7731171de82a5943ea23356b0bee358cf9a7336b7260c65d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:b2a9675c4500505de4f90163d512cf75f05c9d42cd7d5ec24db26e945443acfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168482795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a8b8cd9a7028b8b3433ab3f9df9fa37ad306501b79aad51b65c86abc28ab5af`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:02 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Tue, 02 Jul 2024 01:25:02 GMT
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
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245b750b3dbd4ecd8d4bf1dd2fa4152bed134157231886e67d9c6cd77d96d170`  
		Last Modified: Fri, 12 Jul 2024 00:56:00 GMT  
		Size: 9.8 MB (9786173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ffee79c9f66f54445f932a31f35d69c307f3248b7ad361641facd54fb68bb4`  
		Last Modified: Fri, 12 Jul 2024 00:56:00 GMT  
		Size: 5.8 MB (5820923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89624f628a1ab632599c90a54366782cf776104fd5d9fab77ef8447c34efbae4`  
		Last Modified: Fri, 12 Jul 2024 00:56:00 GMT  
		Size: 3.2 KB (3229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb932efdd4b8e8932418cbc3f4504137a54c3943d9b6e0df2c3d8ed2c52b7ce2`  
		Last Modified: Fri, 12 Jul 2024 00:56:00 GMT  
		Size: 1.0 MB (1006361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42295cbddaebd3646d97b87d9eb89d862354c98f4818dbd911b54b7d7ec7d7be`  
		Last Modified: Fri, 12 Jul 2024 00:56:02 GMT  
		Size: 99.6 MB (99604809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b0d26b4cd4afd57521f2a33f835e8f92df6640fcc78d06c946cbd0717db649`  
		Last Modified: Fri, 12 Jul 2024 00:56:01 GMT  
		Size: 23.1 MB (23128291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2823098ad982a9610360972234c674c4320736afd8156e8e737d25116be8aecd`  
		Last Modified: Fri, 12 Jul 2024 00:56:01 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe53c7a8bf1ec8290c6b080b4dcd2480131e925eb5fee92e56774d688084b39`  
		Last Modified: Fri, 12 Jul 2024 00:56:01 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a489731c1c780adbbcd02f9e9a78fdcc23b27849be6409f99addc2bed16984`  
		Last Modified: Fri, 12 Jul 2024 00:56:02 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:9352e0abfc848eb75b889e6cc5be4db50f96e3d0180644ddc2722c87b5ab6fcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2806269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c130c086dc63d64acd58bd3fd98d0ff6b0b16cc95c9f6184ab1fbe4aa22d8fa`

```dockerfile
```

-	Layers:
	-	`sha256:3c62ba2ed7795a5f89c1543a6ff2300402aaf5a324a4aa584866e50967a712fe`  
		Last Modified: Fri, 12 Jul 2024 00:56:00 GMT  
		Size: 2.8 MB (2772729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cca6c7303977c50501549610ff3950a75c65746f8ac5edf908dd3e898681ff8c`  
		Last Modified: Fri, 12 Jul 2024 00:56:00 GMT  
		Size: 33.5 KB (33540 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:ab4068e140d69eefb8f5134d8443402564857a760c4ac63c4a2640a59c5df8fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162257359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:babfb21c041ece360b0ebe226ced2dc006af72520146e2384978f3017d4e108a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:37 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Tue, 02 Jul 2024 00:39:37 GMT
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
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b786576aaeced8d0e3f4629cddc33ef3344b02b423e70f90628575293158876`  
		Last Modified: Fri, 12 Jul 2024 00:59:21 GMT  
		Size: 9.6 MB (9585141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e06d2219f0fc643d914caf4964dc79404236a9b66c8f5c5d4fddd70c27bbb5`  
		Last Modified: Fri, 12 Jul 2024 00:59:21 GMT  
		Size: 5.5 MB (5463798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af9beabe444dc89beef8e076bd658fb482b85f2548cb732dd5654f9d827158a`  
		Last Modified: Fri, 12 Jul 2024 00:59:20 GMT  
		Size: 3.2 KB (3227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582b012d6a97c3b5b46ae224b4773f900ce31fcefcd2445e201c57cedce4fa3c`  
		Last Modified: Fri, 12 Jul 2024 00:59:21 GMT  
		Size: 936.1 KB (936108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67162d043b41d2a09da357e28b87e5692bcf86fe1da5a9098aded9e4685376c4`  
		Last Modified: Fri, 12 Jul 2024 00:59:24 GMT  
		Size: 95.4 MB (95443266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b80ca3e3b97268665dc499c3639e9c915dabbaefe90225f33c4ee06ef6f6aa`  
		Last Modified: Fri, 12 Jul 2024 00:59:23 GMT  
		Size: 21.7 MB (21662524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef963534d0ea920ef82a986acec28d723c959c1c7ae7f4b3524b4accbc36cf9a`  
		Last Modified: Fri, 12 Jul 2024 00:59:22 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36930f0576c0362da87435f16eee2b6a17ff8d5f48f762f94b47ca4e1c41144`  
		Last Modified: Fri, 12 Jul 2024 00:59:22 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9bdede93fcba6ad11c582c806a9dcf9efe2095d22f4a21faf41d99fc87b37f`  
		Last Modified: Fri, 12 Jul 2024 00:59:23 GMT  
		Size: 6.3 KB (6288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:d342327984c78c72d419eeec2121a4e910e18cebca5403a4ea80cce8b476e5af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2805952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f65d349eee61c68c824c6b9dfae1c44b5dfb1c7d7a6b002a598038e4dac827f2`

```dockerfile
```

-	Layers:
	-	`sha256:22efa2d1de5ebc19032c4f173980ae813739f9b300f5c189076dfe023fae3d57`  
		Last Modified: Fri, 12 Jul 2024 00:59:21 GMT  
		Size: 2.8 MB (2772109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f7a2c5672308769994adaa03596da27088e67af9012114a696c3cc8d2aa64aa`  
		Last Modified: Fri, 12 Jul 2024 00:59:20 GMT  
		Size: 33.8 KB (33843 bytes)  
		MIME: application/vnd.in-toto+json
