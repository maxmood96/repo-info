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
$ docker pull influxdb@sha256:c349daa89b811dffc559dcf03dae01db3ee96e10ead706102b4d0659b01ba596
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:b0ef33bfeffe7bd25b14530f3fb43eba923286455902db131063b08b4f136855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46178996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efc5fe16a131289b6659656a59a99ada2ac6eea49937fd274aa2750eda0c32b0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["/bin/sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f32acfd72a12dc339f5b67752df209abba35968e2f6767bb155cc38c863e80`  
		Last Modified: Thu, 20 Jun 2024 20:54:49 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b228274f626977c1d9a5b608154d92bc99a72319e1e7bced77e9f8106cf21f`  
		Last Modified: Thu, 20 Jun 2024 20:54:54 GMT  
		Size: 1.2 MB (1231170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c62a54ac9a91295b1cad02674b4a5037d91e3338723777085f49781c6bca96`  
		Last Modified: Thu, 20 Jun 2024 20:54:55 GMT  
		Size: 41.3 MB (41321930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a65088a1a1584ff818855306ffc140af145d4226774769303c7fa450bec848c2`  
		Last Modified: Thu, 20 Jun 2024 20:54:54 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255e25fc8910552165291979205da40f523523a80cc80e91447e29532238d2de`  
		Last Modified: Thu, 20 Jun 2024 20:54:54 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fa56e70cc6a0b48539407ad1cf73af8ee634e66437dead6b43ed3b3d4bf635`  
		Last Modified: Thu, 20 Jun 2024 20:54:55 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:e3ac4b60dd768f4d5095453bca53efb241e85d4f0f1061bb89ee1a617f1bd78a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **744.4 KB (744414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f90f6d116cf2ccf70f278eb1b1ea8502a1bb5acb632249f1df2b299fbc972e69`

```dockerfile
```

-	Layers:
	-	`sha256:fe555655f1c7b21b8ffbeb9cd7f66241d556f13515902685b530e76ed8076fab`  
		Last Modified: Thu, 20 Jun 2024 20:54:54 GMT  
		Size: 728.0 KB (727990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9882a32dc718216742a187cb491702eafd42920f23ada85e76ceb7015002a1ef`  
		Last Modified: Thu, 20 Jun 2024 20:54:54 GMT  
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
$ docker pull influxdb@sha256:84c17a5ada52baa05a44dcd7aeb1208dc1cfc8edac473a7154304bf1071a8846
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:e16e08ef0fea1564fafd8a48d2c6bb95ce93b9fdec9ea99cf698df013b31cbeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.9 MB (24897952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0890cd820d3ef54e1bbd06789d7bcfb8800ca8e42799afc9f180b2c3d1fa98c8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["/bin/sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30bb9e747f3adcaa574cae4189503b723629f5b184f1ad36dab83bc0a450e045`  
		Last Modified: Thu, 20 Jun 2024 20:54:56 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5815ade88892654cf147c09d43ee92446f5da3fa6ccde9ce450d99308136cb9e`  
		Last Modified: Thu, 20 Jun 2024 20:54:56 GMT  
		Size: 1.2 MB (1231176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd46ec54c4f9112b8a38b6fa82bb15a50565531430506f45e965488619faf207`  
		Last Modified: Thu, 20 Jun 2024 20:54:56 GMT  
		Size: 20.0 MB (20042084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70e9912f5c46f4ae0a4a9ad46860de6c331300e9750f4a661498d18df89834b8`  
		Last Modified: Thu, 20 Jun 2024 20:54:56 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000f754597e54e2421d8d0a7e74baf037ef54afd5f5d6628b2816f9634b6b48b`  
		Last Modified: Thu, 20 Jun 2024 20:54:57 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:567d4123110d3ee8492e65154da7deefa3c8a86ed0a652d7c372b73fcc4f05c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **679.9 KB (679926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b6de906afcd7d4f5f498d6b5823f2aa0f082a318dab8ed03e62f05af71e972e`

```dockerfile
```

-	Layers:
	-	`sha256:746020856044996e197cac18318e36ff813650e6493e8ebd9ccb4de2c94a2e35`  
		Last Modified: Thu, 20 Jun 2024 20:54:56 GMT  
		Size: 665.1 KB (665137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d2480c95150b968c938b5ebdcccfda483d38539fafd894c924412ea1f1753c0`  
		Last Modified: Thu, 20 Jun 2024 20:54:56 GMT  
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
$ docker pull influxdb@sha256:c349daa89b811dffc559dcf03dae01db3ee96e10ead706102b4d0659b01ba596
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.7-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:b0ef33bfeffe7bd25b14530f3fb43eba923286455902db131063b08b4f136855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46178996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efc5fe16a131289b6659656a59a99ada2ac6eea49937fd274aa2750eda0c32b0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["/bin/sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f32acfd72a12dc339f5b67752df209abba35968e2f6767bb155cc38c863e80`  
		Last Modified: Thu, 20 Jun 2024 20:54:49 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b228274f626977c1d9a5b608154d92bc99a72319e1e7bced77e9f8106cf21f`  
		Last Modified: Thu, 20 Jun 2024 20:54:54 GMT  
		Size: 1.2 MB (1231170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c62a54ac9a91295b1cad02674b4a5037d91e3338723777085f49781c6bca96`  
		Last Modified: Thu, 20 Jun 2024 20:54:55 GMT  
		Size: 41.3 MB (41321930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a65088a1a1584ff818855306ffc140af145d4226774769303c7fa450bec848c2`  
		Last Modified: Thu, 20 Jun 2024 20:54:54 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255e25fc8910552165291979205da40f523523a80cc80e91447e29532238d2de`  
		Last Modified: Thu, 20 Jun 2024 20:54:54 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fa56e70cc6a0b48539407ad1cf73af8ee634e66437dead6b43ed3b3d4bf635`  
		Last Modified: Thu, 20 Jun 2024 20:54:55 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.7-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:e3ac4b60dd768f4d5095453bca53efb241e85d4f0f1061bb89ee1a617f1bd78a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **744.4 KB (744414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f90f6d116cf2ccf70f278eb1b1ea8502a1bb5acb632249f1df2b299fbc972e69`

```dockerfile
```

-	Layers:
	-	`sha256:fe555655f1c7b21b8ffbeb9cd7f66241d556f13515902685b530e76ed8076fab`  
		Last Modified: Thu, 20 Jun 2024 20:54:54 GMT  
		Size: 728.0 KB (727990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9882a32dc718216742a187cb491702eafd42920f23ada85e76ceb7015002a1ef`  
		Last Modified: Thu, 20 Jun 2024 20:54:54 GMT  
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
$ docker pull influxdb@sha256:84c17a5ada52baa05a44dcd7aeb1208dc1cfc8edac473a7154304bf1071a8846
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.7-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:e16e08ef0fea1564fafd8a48d2c6bb95ce93b9fdec9ea99cf698df013b31cbeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.9 MB (24897952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0890cd820d3ef54e1bbd06789d7bcfb8800ca8e42799afc9f180b2c3d1fa98c8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["/bin/sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30bb9e747f3adcaa574cae4189503b723629f5b184f1ad36dab83bc0a450e045`  
		Last Modified: Thu, 20 Jun 2024 20:54:56 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5815ade88892654cf147c09d43ee92446f5da3fa6ccde9ce450d99308136cb9e`  
		Last Modified: Thu, 20 Jun 2024 20:54:56 GMT  
		Size: 1.2 MB (1231176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd46ec54c4f9112b8a38b6fa82bb15a50565531430506f45e965488619faf207`  
		Last Modified: Thu, 20 Jun 2024 20:54:56 GMT  
		Size: 20.0 MB (20042084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70e9912f5c46f4ae0a4a9ad46860de6c331300e9750f4a661498d18df89834b8`  
		Last Modified: Thu, 20 Jun 2024 20:54:56 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000f754597e54e2421d8d0a7e74baf037ef54afd5f5d6628b2816f9634b6b48b`  
		Last Modified: Thu, 20 Jun 2024 20:54:57 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.7-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:567d4123110d3ee8492e65154da7deefa3c8a86ed0a652d7c372b73fcc4f05c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **679.9 KB (679926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b6de906afcd7d4f5f498d6b5823f2aa0f082a318dab8ed03e62f05af71e972e`

```dockerfile
```

-	Layers:
	-	`sha256:746020856044996e197cac18318e36ff813650e6493e8ebd9ccb4de2c94a2e35`  
		Last Modified: Thu, 20 Jun 2024 20:54:56 GMT  
		Size: 665.1 KB (665137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d2480c95150b968c938b5ebdcccfda483d38539fafd894c924412ea1f1753c0`  
		Last Modified: Thu, 20 Jun 2024 20:54:56 GMT  
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
$ docker pull influxdb@sha256:373550b72aee093db9a6e30dc11bcd997e57fb7789c3e61c8385aca3a47de7c0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:803e0324e65735c6a7f6484b16d7ede2bf96729d04600206fe58e8bf93beda9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46631579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35bbd4164f2923cca5470fd09f3108690a384ac8a2e63c6cb6db983f03a084c2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["/bin/sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.11.5-c1.11.5
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f32acfd72a12dc339f5b67752df209abba35968e2f6767bb155cc38c863e80`  
		Last Modified: Thu, 20 Jun 2024 20:54:49 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f5da72c838850065314b5d1079072f389c8dbac9505a2e45f438f67828d4e5a`  
		Last Modified: Thu, 20 Jun 2024 20:57:04 GMT  
		Size: 1.2 MB (1231181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:479aa498d667b108bd3bfed477e48fd76d87b633df7c78ad28c3f4eee31ac9b2`  
		Last Modified: Thu, 20 Jun 2024 20:57:05 GMT  
		Size: 41.8 MB (41774502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b587877f039ab1a27a83e9c8579633e9da594cade8e60af43b42da0a8aacca`  
		Last Modified: Thu, 20 Jun 2024 20:57:04 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53bb7ff347f154cc27dcc6a7a42f90dba616c5b482975304d1220c866e789278`  
		Last Modified: Thu, 20 Jun 2024 20:57:04 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bbf56f94a1d68aef84559d8ed703c36ed21abf775a7738af5f90b8c8d72f17c`  
		Last Modified: Thu, 20 Jun 2024 20:57:05 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:b56d56cfb4e826e2d596ee6bcfc4e58494bbfaef24f97ad183a7e0c744dffb7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **744.1 KB (744101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87c8f700b66131382ece67a1a62f0d1daac05e9c9653fc43092cb6fbcdf3d24a`

```dockerfile
```

-	Layers:
	-	`sha256:4e229025e8e57ed631582c171835de08ac4b06c6a335c31975ec52ee3d5d237a`  
		Last Modified: Thu, 20 Jun 2024 20:57:04 GMT  
		Size: 727.7 KB (727678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95af4137db0e119882af5b71b1b02849b15bc8e77854187704fe8d312faed310`  
		Last Modified: Thu, 20 Jun 2024 20:57:04 GMT  
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
$ docker pull influxdb@sha256:f6003b5d68a63b717d6ae4fde88b02feffac39a9bc8f6e5ef2cf5340192c9cbe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:4b863545313895041b9366263f45a2ce557d801733b06ca1a35282bb34ff307c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25201216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5a83176643e1e1b05a89faa7a74eace3b28e35da4d193d728115bd7346fcf0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["/bin/sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.11.5-c1.11.5
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb2c9ef3554ee7c21a51402d127e96f74733b80619acbd8786bcbeea50e07ad`  
		Last Modified: Thu, 20 Jun 2024 20:56:46 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0485b30f16104c439e8e63ce0896181dccbe7e4c38ff35c3c20f7f28f92669d0`  
		Last Modified: Thu, 20 Jun 2024 20:56:46 GMT  
		Size: 1.2 MB (1231170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46384ed337e6b715f2878c37c41ff7c6b838a69b02dab2ad52c011513b0ddb38`  
		Last Modified: Thu, 20 Jun 2024 20:56:46 GMT  
		Size: 20.3 MB (20345358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4847c7717b6d1278eb2bc03baf2c86ac7dde3dde66a7a34be092770b9ac03de`  
		Last Modified: Thu, 20 Jun 2024 20:56:46 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5d4827505b0c2930ad5d79567596d37e757ad466f44462258f3ee6c67587c5`  
		Last Modified: Thu, 20 Jun 2024 20:56:46 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:5e799fb1257a2582e333b7ecaf257d019dc2a4fca4bbf30ddb78edeff8a47095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **680.8 KB (680800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53bcf2cf3ce383536126dd16a19c474921408fa0160ea31a050f9bbfb190c4c8`

```dockerfile
```

-	Layers:
	-	`sha256:740011fd7d7243a5c04f6a499544dadcfc2b33d8e5cd8fbfd05d3cade2a18021`  
		Last Modified: Thu, 20 Jun 2024 20:56:46 GMT  
		Size: 666.0 KB (666011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:866c18570069c3695b8eadee3a09078bd09ad7e39d0646fab9c6ec86c280bae0`  
		Last Modified: Thu, 20 Jun 2024 20:56:46 GMT  
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
$ docker pull influxdb@sha256:373550b72aee093db9a6e30dc11bcd997e57fb7789c3e61c8385aca3a47de7c0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.5-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:803e0324e65735c6a7f6484b16d7ede2bf96729d04600206fe58e8bf93beda9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46631579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35bbd4164f2923cca5470fd09f3108690a384ac8a2e63c6cb6db983f03a084c2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["/bin/sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.11.5-c1.11.5
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f32acfd72a12dc339f5b67752df209abba35968e2f6767bb155cc38c863e80`  
		Last Modified: Thu, 20 Jun 2024 20:54:49 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f5da72c838850065314b5d1079072f389c8dbac9505a2e45f438f67828d4e5a`  
		Last Modified: Thu, 20 Jun 2024 20:57:04 GMT  
		Size: 1.2 MB (1231181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:479aa498d667b108bd3bfed477e48fd76d87b633df7c78ad28c3f4eee31ac9b2`  
		Last Modified: Thu, 20 Jun 2024 20:57:05 GMT  
		Size: 41.8 MB (41774502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b587877f039ab1a27a83e9c8579633e9da594cade8e60af43b42da0a8aacca`  
		Last Modified: Thu, 20 Jun 2024 20:57:04 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53bb7ff347f154cc27dcc6a7a42f90dba616c5b482975304d1220c866e789278`  
		Last Modified: Thu, 20 Jun 2024 20:57:04 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bbf56f94a1d68aef84559d8ed703c36ed21abf775a7738af5f90b8c8d72f17c`  
		Last Modified: Thu, 20 Jun 2024 20:57:05 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.5-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:b56d56cfb4e826e2d596ee6bcfc4e58494bbfaef24f97ad183a7e0c744dffb7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **744.1 KB (744101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87c8f700b66131382ece67a1a62f0d1daac05e9c9653fc43092cb6fbcdf3d24a`

```dockerfile
```

-	Layers:
	-	`sha256:4e229025e8e57ed631582c171835de08ac4b06c6a335c31975ec52ee3d5d237a`  
		Last Modified: Thu, 20 Jun 2024 20:57:04 GMT  
		Size: 727.7 KB (727678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95af4137db0e119882af5b71b1b02849b15bc8e77854187704fe8d312faed310`  
		Last Modified: Thu, 20 Jun 2024 20:57:04 GMT  
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
$ docker pull influxdb@sha256:f6003b5d68a63b717d6ae4fde88b02feffac39a9bc8f6e5ef2cf5340192c9cbe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.5-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:4b863545313895041b9366263f45a2ce557d801733b06ca1a35282bb34ff307c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25201216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5a83176643e1e1b05a89faa7a74eace3b28e35da4d193d728115bd7346fcf0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["/bin/sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.11.5-c1.11.5
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb2c9ef3554ee7c21a51402d127e96f74733b80619acbd8786bcbeea50e07ad`  
		Last Modified: Thu, 20 Jun 2024 20:56:46 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0485b30f16104c439e8e63ce0896181dccbe7e4c38ff35c3c20f7f28f92669d0`  
		Last Modified: Thu, 20 Jun 2024 20:56:46 GMT  
		Size: 1.2 MB (1231170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46384ed337e6b715f2878c37c41ff7c6b838a69b02dab2ad52c011513b0ddb38`  
		Last Modified: Thu, 20 Jun 2024 20:56:46 GMT  
		Size: 20.3 MB (20345358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4847c7717b6d1278eb2bc03baf2c86ac7dde3dde66a7a34be092770b9ac03de`  
		Last Modified: Thu, 20 Jun 2024 20:56:46 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5d4827505b0c2930ad5d79567596d37e757ad466f44462258f3ee6c67587c5`  
		Last Modified: Thu, 20 Jun 2024 20:56:46 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.5-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:5e799fb1257a2582e333b7ecaf257d019dc2a4fca4bbf30ddb78edeff8a47095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **680.8 KB (680800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53bcf2cf3ce383536126dd16a19c474921408fa0160ea31a050f9bbfb190c4c8`

```dockerfile
```

-	Layers:
	-	`sha256:740011fd7d7243a5c04f6a499544dadcfc2b33d8e5cd8fbfd05d3cade2a18021`  
		Last Modified: Thu, 20 Jun 2024 20:56:46 GMT  
		Size: 666.0 KB (666011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:866c18570069c3695b8eadee3a09078bd09ad7e39d0646fab9c6ec86c280bae0`  
		Last Modified: Thu, 20 Jun 2024 20:56:46 GMT  
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
$ docker pull influxdb@sha256:f47e2c0c19227b7edded2c599ae575fe8473ae18dcfb326719c7ef132592a711
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.8-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:e042e70d87b5e65af17668da397de33a84ae50eef2dce4b6547a936935a79a80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59518155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d091f5b0c8af87f05f242d96cd0bcbcc3d63701e2fd97e564d394e3928ecb117`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:cbcddefa487fb5085857fbba16854e06e53f93295bbf36ef1968a0b89835cad7 in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["/bin/sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.8.10
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     chmod +x /usr/src/influxdb-*/influx              /usr/src/influxdb-*/influx_inspect              /usr/src/influxdb-*/influx_stress              /usr/src/influxdb-*/influxd &&    mv /usr/src/influxdb-*/influx        /usr/src/influxdb-*/influx_inspect        /usr/src/influxdb-*/influx_stress         /usr/src/influxdb-*/influxd        /usr/bin/ &&    gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
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
	-	`sha256:f9202480295a4ef9cc62343dea568a5840b58bc68a1970045d30f3077a46a471`  
		Last Modified: Thu, 20 Jun 2024 20:18:01 GMT  
		Size: 3.4 MB (3389963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f090dc0a54bea08f163d45880d51f7788e0fbcb1ab7a7d8478580d334090d5ee`  
		Last Modified: Thu, 20 Jun 2024 20:54:52 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3476b3c19ca9862abb5959b005c2912320c53401c38d6fd9cbfd2e039940542e`  
		Last Modified: Thu, 20 Jun 2024 20:54:52 GMT  
		Size: 1.5 MB (1479503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e241256e83ddb646684dcb09be34251b7da60cdf088fe55c99027caa0fe8618`  
		Last Modified: Thu, 20 Jun 2024 20:54:53 GMT  
		Size: 54.6 MB (54646693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c46fbab942fcc512d8965cde5297adae0519cc5081658845e3493f76d5a90d63`  
		Last Modified: Thu, 20 Jun 2024 20:54:52 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528f2026877653ba9a39132db07cf9b8466f427965a4a734c6352765eb66dbaa`  
		Last Modified: Thu, 20 Jun 2024 20:54:53 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cbd4abecb8ff7e8ed50a6820ae6091c4cb9b860afa3fc5817d957e10e46711c`  
		Last Modified: Thu, 20 Jun 2024 20:54:53 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:a54c9a4778a0dfaf10edf26620065bb3ad335d967c4d1738895538de7e1f1503
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1000.3 KB (1000260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:873f0dfb8f9fb39a912ca56b93072a0f60f452c0a33d6d33127f72487f935b26`

```dockerfile
```

-	Layers:
	-	`sha256:39313ee392384622bbf078ebb0f3ad5d93d3db309778697dfccf2352b08f12d2`  
		Last Modified: Thu, 20 Jun 2024 20:54:52 GMT  
		Size: 982.9 KB (982898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f6822bbee646b2190637209708a566233d8528519bf029a24e959d7a07e9e6e`  
		Last Modified: Thu, 20 Jun 2024 20:54:52 GMT  
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
$ docker pull influxdb@sha256:f47e2c0c19227b7edded2c599ae575fe8473ae18dcfb326719c7ef132592a711
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.8.10-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:e042e70d87b5e65af17668da397de33a84ae50eef2dce4b6547a936935a79a80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59518155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d091f5b0c8af87f05f242d96cd0bcbcc3d63701e2fd97e564d394e3928ecb117`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:cbcddefa487fb5085857fbba16854e06e53f93295bbf36ef1968a0b89835cad7 in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["/bin/sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.8.10
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     chmod +x /usr/src/influxdb-*/influx              /usr/src/influxdb-*/influx_inspect              /usr/src/influxdb-*/influx_stress              /usr/src/influxdb-*/influxd &&    mv /usr/src/influxdb-*/influx        /usr/src/influxdb-*/influx_inspect        /usr/src/influxdb-*/influx_stress         /usr/src/influxdb-*/influxd        /usr/bin/ &&    gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
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
	-	`sha256:f9202480295a4ef9cc62343dea568a5840b58bc68a1970045d30f3077a46a471`  
		Last Modified: Thu, 20 Jun 2024 20:18:01 GMT  
		Size: 3.4 MB (3389963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f090dc0a54bea08f163d45880d51f7788e0fbcb1ab7a7d8478580d334090d5ee`  
		Last Modified: Thu, 20 Jun 2024 20:54:52 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3476b3c19ca9862abb5959b005c2912320c53401c38d6fd9cbfd2e039940542e`  
		Last Modified: Thu, 20 Jun 2024 20:54:52 GMT  
		Size: 1.5 MB (1479503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e241256e83ddb646684dcb09be34251b7da60cdf088fe55c99027caa0fe8618`  
		Last Modified: Thu, 20 Jun 2024 20:54:53 GMT  
		Size: 54.6 MB (54646693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c46fbab942fcc512d8965cde5297adae0519cc5081658845e3493f76d5a90d63`  
		Last Modified: Thu, 20 Jun 2024 20:54:52 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528f2026877653ba9a39132db07cf9b8466f427965a4a734c6352765eb66dbaa`  
		Last Modified: Thu, 20 Jun 2024 20:54:53 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cbd4abecb8ff7e8ed50a6820ae6091c4cb9b860afa3fc5817d957e10e46711c`  
		Last Modified: Thu, 20 Jun 2024 20:54:53 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8.10-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:a54c9a4778a0dfaf10edf26620065bb3ad335d967c4d1738895538de7e1f1503
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1000.3 KB (1000260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:873f0dfb8f9fb39a912ca56b93072a0f60f452c0a33d6d33127f72487f935b26`

```dockerfile
```

-	Layers:
	-	`sha256:39313ee392384622bbf078ebb0f3ad5d93d3db309778697dfccf2352b08f12d2`  
		Last Modified: Thu, 20 Jun 2024 20:54:52 GMT  
		Size: 982.9 KB (982898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f6822bbee646b2190637209708a566233d8528519bf029a24e959d7a07e9e6e`  
		Last Modified: Thu, 20 Jun 2024 20:54:52 GMT  
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
$ docker pull influxdb@sha256:9c575cc461b69c91518a6c2a16114740fdcbc3bd981c47500a3367b8b7be271a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:209ae4f4c147eedf4081201bf4fbe418ec9ee19a5afa66357d139471c7db7063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 MB (38120315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f6d06f6a725c76aadbdeb509b06dac36dddb4a9ea8c8ae1522428be512eac46`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:cbcddefa487fb5085857fbba16854e06e53f93295bbf36ef1968a0b89835cad7 in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["/bin/sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/etc/influxdb/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
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
	-	`sha256:f9202480295a4ef9cc62343dea568a5840b58bc68a1970045d30f3077a46a471`  
		Last Modified: Thu, 20 Jun 2024 20:18:01 GMT  
		Size: 3.4 MB (3389963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26458e6b14471f89c6d6e4957c039127c9681a9387898d6827c44e376b580f5`  
		Last Modified: Thu, 20 Jun 2024 20:55:00 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6017139ab47b9aa0a3a279bdcd5f084098b101a87bef62e91ba6ba9db7d2e47e`  
		Last Modified: Thu, 20 Jun 2024 20:55:00 GMT  
		Size: 1.5 MB (1479506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef37047fd369608a3b1690522b60a9703c169545f49d9ec7226f85aadba08695`  
		Last Modified: Thu, 20 Jun 2024 20:55:01 GMT  
		Size: 33.2 MB (33248792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1dd943f432de9dc8732bc4e8dfc0b8e3490c9ba9c2bcf379790f5c823d3e13`  
		Last Modified: Thu, 20 Jun 2024 20:55:00 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f522499af22ad04450f64af6a7b2a391c94c9783d8acadc612ae97f4335c19b6`  
		Last Modified: Thu, 20 Jun 2024 20:55:01 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab73fe86a4937474791a66485732a5f2fe1340eead6f8a55898e2c8e5e90a8b`  
		Last Modified: Thu, 20 Jun 2024 20:55:01 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:38395ca886b7a8088d1f10fc84e4cc0d0c33e72aa2cc8afb7ed335c9cdb3179b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1114153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df8e06d5667b686e50137ef262c1e385ee6d3277a0b9d683a7f932267edcc458`

```dockerfile
```

-	Layers:
	-	`sha256:767fe16230170b2f1da7f6516bb9cc035ede04f2f32ce5aaf902993afa3a2a10`  
		Last Modified: Thu, 20 Jun 2024 20:55:00 GMT  
		Size: 1.1 MB (1097705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4367fd67cfc8cc13aa2de79c86ec8a17ee63ff18f0a4ca54538a6b57796acfe9`  
		Last Modified: Thu, 20 Jun 2024 20:55:00 GMT  
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
$ docker pull influxdb@sha256:9e74ebc4c10822d4791ff4342e92f76d0b9b7d9cca78b0ec6a4a59a6e15c32e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:974b1d239a0188c298e98a59248fc8ae2ae49b7eac0cc19a549257296966c60e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17576909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68c2cd9f31dbc2d24eddfbf4a46d43d17dd5cff5884ff706efa26aad64eabb2d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["/bin/sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/etc/influxdb/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e4722b1542a3de0e2bd35092f5112ed1b72efad4a8f51b92d17566b1c1906f`  
		Last Modified: Thu, 20 Jun 2024 20:57:00 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fdd499727202e0d900bd7d5de5d9388fbc4a3a22605673d6700d16df59f5382`  
		Last Modified: Thu, 20 Jun 2024 20:57:00 GMT  
		Size: 1.2 MB (1231168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9283fc459df289d56e3eeaeac5fc6f34f7c0f5f22d5732460f46bbf9221c94ea`  
		Last Modified: Thu, 20 Jun 2024 20:57:00 GMT  
		Size: 12.7 MB (12721051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce45e6cbddc2c1f0cd8d574299788b96e999f8ef18e3072621f7492305757d0`  
		Last Modified: Thu, 20 Jun 2024 20:57:00 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c46ed6b3a9b3abbfc0b1c6991646a23aaa5e8acafb515693abbf4ec92a3fe6d`  
		Last Modified: Thu, 20 Jun 2024 20:57:00 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:6ae79d5dc183b93077011f1b4a5dcf34f1bc2eda2a250bdc8438d7ff4fda554e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **679.9 KB (679882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:243fa70b5a9753af6855d752a3db308ed6868a4b0eb9456f02b9048cb349b1e5`

```dockerfile
```

-	Layers:
	-	`sha256:d08d58024bd3107f36990545a8003ecb6b9799e3911b0ff97cd33cfacc9b6a9c`  
		Last Modified: Thu, 20 Jun 2024 20:57:00 GMT  
		Size: 665.1 KB (665069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07491a347b5fcda4b25a6b341fc328493ec6792736b5e40c5cd72a29cfe86c5a`  
		Last Modified: Thu, 20 Jun 2024 20:57:00 GMT  
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
$ docker pull influxdb@sha256:9c575cc461b69c91518a6c2a16114740fdcbc3bd981c47500a3367b8b7be271a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9.13-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:209ae4f4c147eedf4081201bf4fbe418ec9ee19a5afa66357d139471c7db7063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 MB (38120315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f6d06f6a725c76aadbdeb509b06dac36dddb4a9ea8c8ae1522428be512eac46`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:cbcddefa487fb5085857fbba16854e06e53f93295bbf36ef1968a0b89835cad7 in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["/bin/sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/etc/influxdb/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
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
	-	`sha256:f9202480295a4ef9cc62343dea568a5840b58bc68a1970045d30f3077a46a471`  
		Last Modified: Thu, 20 Jun 2024 20:18:01 GMT  
		Size: 3.4 MB (3389963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26458e6b14471f89c6d6e4957c039127c9681a9387898d6827c44e376b580f5`  
		Last Modified: Thu, 20 Jun 2024 20:55:00 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6017139ab47b9aa0a3a279bdcd5f084098b101a87bef62e91ba6ba9db7d2e47e`  
		Last Modified: Thu, 20 Jun 2024 20:55:00 GMT  
		Size: 1.5 MB (1479506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef37047fd369608a3b1690522b60a9703c169545f49d9ec7226f85aadba08695`  
		Last Modified: Thu, 20 Jun 2024 20:55:01 GMT  
		Size: 33.2 MB (33248792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1dd943f432de9dc8732bc4e8dfc0b8e3490c9ba9c2bcf379790f5c823d3e13`  
		Last Modified: Thu, 20 Jun 2024 20:55:00 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f522499af22ad04450f64af6a7b2a391c94c9783d8acadc612ae97f4335c19b6`  
		Last Modified: Thu, 20 Jun 2024 20:55:01 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab73fe86a4937474791a66485732a5f2fe1340eead6f8a55898e2c8e5e90a8b`  
		Last Modified: Thu, 20 Jun 2024 20:55:01 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9.13-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:38395ca886b7a8088d1f10fc84e4cc0d0c33e72aa2cc8afb7ed335c9cdb3179b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1114153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df8e06d5667b686e50137ef262c1e385ee6d3277a0b9d683a7f932267edcc458`

```dockerfile
```

-	Layers:
	-	`sha256:767fe16230170b2f1da7f6516bb9cc035ede04f2f32ce5aaf902993afa3a2a10`  
		Last Modified: Thu, 20 Jun 2024 20:55:00 GMT  
		Size: 1.1 MB (1097705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4367fd67cfc8cc13aa2de79c86ec8a17ee63ff18f0a4ca54538a6b57796acfe9`  
		Last Modified: Thu, 20 Jun 2024 20:55:00 GMT  
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
$ docker pull influxdb@sha256:9e74ebc4c10822d4791ff4342e92f76d0b9b7d9cca78b0ec6a4a59a6e15c32e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9.13-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:974b1d239a0188c298e98a59248fc8ae2ae49b7eac0cc19a549257296966c60e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17576909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68c2cd9f31dbc2d24eddfbf4a46d43d17dd5cff5884ff706efa26aad64eabb2d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["/bin/sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/etc/influxdb/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e4722b1542a3de0e2bd35092f5112ed1b72efad4a8f51b92d17566b1c1906f`  
		Last Modified: Thu, 20 Jun 2024 20:57:00 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fdd499727202e0d900bd7d5de5d9388fbc4a3a22605673d6700d16df59f5382`  
		Last Modified: Thu, 20 Jun 2024 20:57:00 GMT  
		Size: 1.2 MB (1231168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9283fc459df289d56e3eeaeac5fc6f34f7c0f5f22d5732460f46bbf9221c94ea`  
		Last Modified: Thu, 20 Jun 2024 20:57:00 GMT  
		Size: 12.7 MB (12721051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce45e6cbddc2c1f0cd8d574299788b96e999f8ef18e3072621f7492305757d0`  
		Last Modified: Thu, 20 Jun 2024 20:57:00 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c46ed6b3a9b3abbfc0b1c6991646a23aaa5e8acafb515693abbf4ec92a3fe6d`  
		Last Modified: Thu, 20 Jun 2024 20:57:00 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9.13-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:6ae79d5dc183b93077011f1b4a5dcf34f1bc2eda2a250bdc8438d7ff4fda554e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **679.9 KB (679882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:243fa70b5a9753af6855d752a3db308ed6868a4b0eb9456f02b9048cb349b1e5`

```dockerfile
```

-	Layers:
	-	`sha256:d08d58024bd3107f36990545a8003ecb6b9799e3911b0ff97cd33cfacc9b6a9c`  
		Last Modified: Thu, 20 Jun 2024 20:57:00 GMT  
		Size: 665.1 KB (665069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07491a347b5fcda4b25a6b341fc328493ec6792736b5e40c5cd72a29cfe86c5a`  
		Last Modified: Thu, 20 Jun 2024 20:57:00 GMT  
		Size: 14.8 KB (14813 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2`

```console
$ docker pull influxdb@sha256:57fbc491438c428a43168665cb9ca12709787a75e7b545cb593fe985aee843df
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
$ docker pull influxdb@sha256:29bf443e32d6ae32fa7155f3290fb9973c67eadc2256a3439d9e86dac6724fcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.3 MB (158267065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:565b979370ac25e8eaf3d51a30c63003090d3132030ef1b6de6803be7448589d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["bash"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV GOSU_VER=1.16
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=2.7.6
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd"]
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 06 Jun 2024 16:24:41 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244a66b2072ea3f07e91b5f8184b4b2752882498edfa7ba8fb76bb6824526c2b`  
		Last Modified: Tue, 02 Jul 2024 15:16:35 GMT  
		Size: 9.6 MB (9584780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909cdb72b23dce52c0f4bdc1dc18109aa9783ec88ff7de35937b9a10ea4f316c`  
		Last Modified: Tue, 02 Jul 2024 15:16:35 GMT  
		Size: 5.5 MB (5463796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff5f5ed1b375c5e0d895d30718c85a37e3c35d0a71cf7046c55aecb926622a2`  
		Last Modified: Tue, 02 Jul 2024 15:16:34 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282638484353524b10cab2a7692a18a864399334bcf1de03c904bbf2cc8d3576`  
		Last Modified: Tue, 02 Jul 2024 15:16:35 GMT  
		Size: 936.1 KB (936109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd75da185cd23e91ecd8ed745c0cca7c52ece635d99420e6b01dcf7a0a27e70`  
		Last Modified: Tue, 02 Jul 2024 15:16:37 GMT  
		Size: 91.5 MB (91453342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae4d7c532325604d920b375d5e1430758fb552ce5cc36c4ab9cb5a05b65c8fa`  
		Last Modified: Tue, 02 Jul 2024 15:16:37 GMT  
		Size: 21.7 MB (21662524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d400046518a6ade36b53c8b3ce4daf1f0e4baa3e00a01dd08fc3a7a27d5e239`  
		Last Modified: Tue, 02 Jul 2024 15:16:36 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dcdc4d64e1e66a79c69bd9677064c35c2b3b7b74da85491b2f60a80b7fdba19`  
		Last Modified: Tue, 02 Jul 2024 15:16:36 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539bf8697e8ab15fe15693bf1ffd910f0cdbd1c6a1aaa191e7da688576172903`  
		Last Modified: Tue, 02 Jul 2024 15:16:37 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:f2790ef100ade36090587201b37bad93c11fff2e8506ad5ca487a06076b7c383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2788414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:090324d138ff85b22d7d2f7b9493272543308d0bded8ef2c755dfe7c7f632335`

```dockerfile
```

-	Layers:
	-	`sha256:467e558654341de92d1993ece4018c64703a2e99b759db120854bd05ff17abfb`  
		Last Modified: Tue, 02 Jul 2024 15:16:35 GMT  
		Size: 2.8 MB (2754571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f79da47dbbf0f3b0da23c1f787782d41583205fab27216314003bc1694b9704f`  
		Last Modified: Tue, 02 Jul 2024 15:16:34 GMT  
		Size: 33.8 KB (33843 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2-alpine`

```console
$ docker pull influxdb@sha256:68a0ad0f478f4002bb56486d49fa3f53f61ef5a97d2de1a323308152e819745a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:053b555c82c43f155a480419bf4f6e025e6080f00d13455971c19381f1a9e898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (92012802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:008b14abfc6921435c404d82df72a3f9f8d974e5ec3d4ebc8f5b1c034ea5f66f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644653db676a15f1f50bac61ea74741812af17cf205867315c11d699f16fad2b`  
		Last Modified: Fri, 12 Jul 2024 00:55:53 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21bebbf70277f25932547a8637cd9367456a54d8ce8cb22fe4ebd0692bb0f4ac`  
		Last Modified: Fri, 12 Jul 2024 00:55:53 GMT  
		Size: 9.6 MB (9633408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a15a052dd483e14ed43222d004e26eeda1e18c8e7d84b6443f1a1b11d8b7b2`  
		Last Modified: Fri, 12 Jul 2024 00:55:53 GMT  
		Size: 5.8 MB (5820947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bbb02eef4582a56528c770a418f5f0bf7a6eb50223575a1ca849b51c18ab12`  
		Last Modified: Fri, 12 Jul 2024 00:55:53 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f09b3ac788a10f3050fa20e8b7e0ed1bb40e9fbb02549fbda4b4177a5c522f38`  
		Last Modified: Fri, 12 Jul 2024 00:55:54 GMT  
		Size: 49.8 MB (49798322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c93ff6cc6478170794864547261311a30a6d1e610e72c1817041ff43386f62`  
		Last Modified: Fri, 12 Jul 2024 00:55:54 GMT  
		Size: 23.1 MB (23128312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539fef72f2c64e74c561d0e68cd80db043dd5ad01bbe7347ca85e600f5fe1dbe`  
		Last Modified: Fri, 12 Jul 2024 00:55:54 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243fde49abb4336be77d98c80e1d241323bb1a87a161483b6f9bce1af7d24af2`  
		Last Modified: Fri, 12 Jul 2024 00:55:54 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3623a23ea66a849d5c0687161e04a53e38f2c462d4de045c2f7f5aa605bd10f8`  
		Last Modified: Fri, 12 Jul 2024 00:55:55 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:f91680e82dd21ac882b9d2ef1da99cafbc381bd18fc38b86cc006745810feea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **901.1 KB (901084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dffd21e309fd08499f77ff40fbc52ff9d0413102f9fb858eee09334c9332cad6`

```dockerfile
```

-	Layers:
	-	`sha256:9e73138dd0ccec6f51005bb78bc926eb129316edb63e8f44d963f31eef2b5047`  
		Last Modified: Fri, 12 Jul 2024 00:55:53 GMT  
		Size: 870.3 KB (870337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:108de35f41a7454b6dbf4918439c03260e68749a123c4caa772c86bd4ed34a2b`  
		Last Modified: Fri, 12 Jul 2024 00:55:53 GMT  
		Size: 30.7 KB (30747 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:8012710486cd42c92463f166da8f3cb85b6117bd1b4416f72d68da9b67253108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.7 MB (86695902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bffebd11d2bb8f925b4b3cd6896e225102f1181f44d14918d529fee04b36a479`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["/bin/sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=2.7.6
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd"]
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 06 Jun 2024 16:24:41 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4d02fd6d451824a88c3da056c35af5ef536e8a634a98239ab90c650e0518e3`  
		Last Modified: Fri, 21 Jun 2024 05:12:50 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2b01a32898b3b778615baf714c0f22bad40fe1d9dbddd0df741da93b96bf90`  
		Last Modified: Fri, 21 Jun 2024 05:12:51 GMT  
		Size: 9.8 MB (9750759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf24405751d72a203b1d9bebd0d05ff6dfef80c1932fb1494c98ba9278d9e588`  
		Last Modified: Fri, 21 Jun 2024 05:12:50 GMT  
		Size: 5.5 MB (5463802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12ebdf543d1e306cb0d041c1c843ba56ea37606cf20c4178fb8503420c5bd97`  
		Last Modified: Fri, 21 Jun 2024 05:12:50 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7f71798a2c4a5377d3c7cc1decb0d14434537b6266ab3a73a1a2000bc04d82`  
		Last Modified: Fri, 21 Jun 2024 05:12:53 GMT  
		Size: 45.7 MB (45722059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2f3dd6b1e82b054e5d7851d3d1180809055eed237a20961aad9352a720a1f8`  
		Last Modified: Fri, 21 Jun 2024 05:12:52 GMT  
		Size: 21.7 MB (21662516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2896f9dc4697a1df8ba98f785f4600faa604faf1d9fd61356428a8ae3224f633`  
		Last Modified: Fri, 21 Jun 2024 05:12:52 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dccba840458a1a7d517c9ac82f7a571e3946f75a62935610dfccaff09e4b2d2`  
		Last Modified: Fri, 21 Jun 2024 05:12:52 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea0d553a68019a537d89c04424ba1ec571aed2614c4973fb0ceb5af4af419a91`  
		Last Modified: Fri, 21 Jun 2024 05:12:53 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:c1b970eb2d343424b5d9f23632745417f45ba097b6a01ddb7bea505a7d3dd8ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **886.8 KB (886831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d814c5ee6f913730efa59405fc0deb9d4d1f5042aac36e4e798ffb4fe903d98`

```dockerfile
```

-	Layers:
	-	`sha256:43ab9a13bdfbf66d39011fa6361dbe012f8e5f72c6b42671ff9e70561b3e62b5`  
		Last Modified: Fri, 21 Jun 2024 05:12:50 GMT  
		Size: 855.8 KB (855784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f52cfecc2d36c66fba04e64b907e5b384907ca53f64768ef107bd1faf04ac22`  
		Last Modified: Fri, 21 Jun 2024 05:12:50 GMT  
		Size: 31.0 KB (31047 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7`

```console
$ docker pull influxdb@sha256:57fbc491438c428a43168665cb9ca12709787a75e7b545cb593fe985aee843df
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
$ docker pull influxdb@sha256:29bf443e32d6ae32fa7155f3290fb9973c67eadc2256a3439d9e86dac6724fcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.3 MB (158267065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:565b979370ac25e8eaf3d51a30c63003090d3132030ef1b6de6803be7448589d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["bash"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV GOSU_VER=1.16
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=2.7.6
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd"]
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 06 Jun 2024 16:24:41 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244a66b2072ea3f07e91b5f8184b4b2752882498edfa7ba8fb76bb6824526c2b`  
		Last Modified: Tue, 02 Jul 2024 15:16:35 GMT  
		Size: 9.6 MB (9584780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909cdb72b23dce52c0f4bdc1dc18109aa9783ec88ff7de35937b9a10ea4f316c`  
		Last Modified: Tue, 02 Jul 2024 15:16:35 GMT  
		Size: 5.5 MB (5463796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff5f5ed1b375c5e0d895d30718c85a37e3c35d0a71cf7046c55aecb926622a2`  
		Last Modified: Tue, 02 Jul 2024 15:16:34 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282638484353524b10cab2a7692a18a864399334bcf1de03c904bbf2cc8d3576`  
		Last Modified: Tue, 02 Jul 2024 15:16:35 GMT  
		Size: 936.1 KB (936109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd75da185cd23e91ecd8ed745c0cca7c52ece635d99420e6b01dcf7a0a27e70`  
		Last Modified: Tue, 02 Jul 2024 15:16:37 GMT  
		Size: 91.5 MB (91453342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae4d7c532325604d920b375d5e1430758fb552ce5cc36c4ab9cb5a05b65c8fa`  
		Last Modified: Tue, 02 Jul 2024 15:16:37 GMT  
		Size: 21.7 MB (21662524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d400046518a6ade36b53c8b3ce4daf1f0e4baa3e00a01dd08fc3a7a27d5e239`  
		Last Modified: Tue, 02 Jul 2024 15:16:36 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dcdc4d64e1e66a79c69bd9677064c35c2b3b7b74da85491b2f60a80b7fdba19`  
		Last Modified: Tue, 02 Jul 2024 15:16:36 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539bf8697e8ab15fe15693bf1ffd910f0cdbd1c6a1aaa191e7da688576172903`  
		Last Modified: Tue, 02 Jul 2024 15:16:37 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:f2790ef100ade36090587201b37bad93c11fff2e8506ad5ca487a06076b7c383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2788414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:090324d138ff85b22d7d2f7b9493272543308d0bded8ef2c755dfe7c7f632335`

```dockerfile
```

-	Layers:
	-	`sha256:467e558654341de92d1993ece4018c64703a2e99b759db120854bd05ff17abfb`  
		Last Modified: Tue, 02 Jul 2024 15:16:35 GMT  
		Size: 2.8 MB (2754571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f79da47dbbf0f3b0da23c1f787782d41583205fab27216314003bc1694b9704f`  
		Last Modified: Tue, 02 Jul 2024 15:16:34 GMT  
		Size: 33.8 KB (33843 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7-alpine`

```console
$ docker pull influxdb@sha256:68a0ad0f478f4002bb56486d49fa3f53f61ef5a97d2de1a323308152e819745a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:053b555c82c43f155a480419bf4f6e025e6080f00d13455971c19381f1a9e898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (92012802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:008b14abfc6921435c404d82df72a3f9f8d974e5ec3d4ebc8f5b1c034ea5f66f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644653db676a15f1f50bac61ea74741812af17cf205867315c11d699f16fad2b`  
		Last Modified: Fri, 12 Jul 2024 00:55:53 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21bebbf70277f25932547a8637cd9367456a54d8ce8cb22fe4ebd0692bb0f4ac`  
		Last Modified: Fri, 12 Jul 2024 00:55:53 GMT  
		Size: 9.6 MB (9633408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a15a052dd483e14ed43222d004e26eeda1e18c8e7d84b6443f1a1b11d8b7b2`  
		Last Modified: Fri, 12 Jul 2024 00:55:53 GMT  
		Size: 5.8 MB (5820947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bbb02eef4582a56528c770a418f5f0bf7a6eb50223575a1ca849b51c18ab12`  
		Last Modified: Fri, 12 Jul 2024 00:55:53 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f09b3ac788a10f3050fa20e8b7e0ed1bb40e9fbb02549fbda4b4177a5c522f38`  
		Last Modified: Fri, 12 Jul 2024 00:55:54 GMT  
		Size: 49.8 MB (49798322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c93ff6cc6478170794864547261311a30a6d1e610e72c1817041ff43386f62`  
		Last Modified: Fri, 12 Jul 2024 00:55:54 GMT  
		Size: 23.1 MB (23128312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539fef72f2c64e74c561d0e68cd80db043dd5ad01bbe7347ca85e600f5fe1dbe`  
		Last Modified: Fri, 12 Jul 2024 00:55:54 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243fde49abb4336be77d98c80e1d241323bb1a87a161483b6f9bce1af7d24af2`  
		Last Modified: Fri, 12 Jul 2024 00:55:54 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3623a23ea66a849d5c0687161e04a53e38f2c462d4de045c2f7f5aa605bd10f8`  
		Last Modified: Fri, 12 Jul 2024 00:55:55 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:f91680e82dd21ac882b9d2ef1da99cafbc381bd18fc38b86cc006745810feea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **901.1 KB (901084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dffd21e309fd08499f77ff40fbc52ff9d0413102f9fb858eee09334c9332cad6`

```dockerfile
```

-	Layers:
	-	`sha256:9e73138dd0ccec6f51005bb78bc926eb129316edb63e8f44d963f31eef2b5047`  
		Last Modified: Fri, 12 Jul 2024 00:55:53 GMT  
		Size: 870.3 KB (870337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:108de35f41a7454b6dbf4918439c03260e68749a123c4caa772c86bd4ed34a2b`  
		Last Modified: Fri, 12 Jul 2024 00:55:53 GMT  
		Size: 30.7 KB (30747 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:8012710486cd42c92463f166da8f3cb85b6117bd1b4416f72d68da9b67253108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.7 MB (86695902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bffebd11d2bb8f925b4b3cd6896e225102f1181f44d14918d529fee04b36a479`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["/bin/sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=2.7.6
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd"]
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 06 Jun 2024 16:24:41 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4d02fd6d451824a88c3da056c35af5ef536e8a634a98239ab90c650e0518e3`  
		Last Modified: Fri, 21 Jun 2024 05:12:50 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2b01a32898b3b778615baf714c0f22bad40fe1d9dbddd0df741da93b96bf90`  
		Last Modified: Fri, 21 Jun 2024 05:12:51 GMT  
		Size: 9.8 MB (9750759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf24405751d72a203b1d9bebd0d05ff6dfef80c1932fb1494c98ba9278d9e588`  
		Last Modified: Fri, 21 Jun 2024 05:12:50 GMT  
		Size: 5.5 MB (5463802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12ebdf543d1e306cb0d041c1c843ba56ea37606cf20c4178fb8503420c5bd97`  
		Last Modified: Fri, 21 Jun 2024 05:12:50 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7f71798a2c4a5377d3c7cc1decb0d14434537b6266ab3a73a1a2000bc04d82`  
		Last Modified: Fri, 21 Jun 2024 05:12:53 GMT  
		Size: 45.7 MB (45722059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2f3dd6b1e82b054e5d7851d3d1180809055eed237a20961aad9352a720a1f8`  
		Last Modified: Fri, 21 Jun 2024 05:12:52 GMT  
		Size: 21.7 MB (21662516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2896f9dc4697a1df8ba98f785f4600faa604faf1d9fd61356428a8ae3224f633`  
		Last Modified: Fri, 21 Jun 2024 05:12:52 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dccba840458a1a7d517c9ac82f7a571e3946f75a62935610dfccaff09e4b2d2`  
		Last Modified: Fri, 21 Jun 2024 05:12:52 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea0d553a68019a537d89c04424ba1ec571aed2614c4973fb0ceb5af4af419a91`  
		Last Modified: Fri, 21 Jun 2024 05:12:53 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:c1b970eb2d343424b5d9f23632745417f45ba097b6a01ddb7bea505a7d3dd8ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **886.8 KB (886831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d814c5ee6f913730efa59405fc0deb9d4d1f5042aac36e4e798ffb4fe903d98`

```dockerfile
```

-	Layers:
	-	`sha256:43ab9a13bdfbf66d39011fa6361dbe012f8e5f72c6b42671ff9e70561b3e62b5`  
		Last Modified: Fri, 21 Jun 2024 05:12:50 GMT  
		Size: 855.8 KB (855784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f52cfecc2d36c66fba04e64b907e5b384907ca53f64768ef107bd1faf04ac22`  
		Last Modified: Fri, 21 Jun 2024 05:12:50 GMT  
		Size: 31.0 KB (31047 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7.7`

```console
$ docker pull influxdb@sha256:eb28b4dd02a4bf472a53783e2e420775717dabcfb360835f666310c9fcb7a871
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
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

## `influxdb:2.7.7-alpine`

```console
$ docker pull influxdb@sha256:f5c97911e0ccab15c4c3f767de64efcc86212607d69d14216d80aec48fcb0058
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:2.7.7-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:053b555c82c43f155a480419bf4f6e025e6080f00d13455971c19381f1a9e898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (92012802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:008b14abfc6921435c404d82df72a3f9f8d974e5ec3d4ebc8f5b1c034ea5f66f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644653db676a15f1f50bac61ea74741812af17cf205867315c11d699f16fad2b`  
		Last Modified: Fri, 12 Jul 2024 00:55:53 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21bebbf70277f25932547a8637cd9367456a54d8ce8cb22fe4ebd0692bb0f4ac`  
		Last Modified: Fri, 12 Jul 2024 00:55:53 GMT  
		Size: 9.6 MB (9633408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a15a052dd483e14ed43222d004e26eeda1e18c8e7d84b6443f1a1b11d8b7b2`  
		Last Modified: Fri, 12 Jul 2024 00:55:53 GMT  
		Size: 5.8 MB (5820947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bbb02eef4582a56528c770a418f5f0bf7a6eb50223575a1ca849b51c18ab12`  
		Last Modified: Fri, 12 Jul 2024 00:55:53 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f09b3ac788a10f3050fa20e8b7e0ed1bb40e9fbb02549fbda4b4177a5c522f38`  
		Last Modified: Fri, 12 Jul 2024 00:55:54 GMT  
		Size: 49.8 MB (49798322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c93ff6cc6478170794864547261311a30a6d1e610e72c1817041ff43386f62`  
		Last Modified: Fri, 12 Jul 2024 00:55:54 GMT  
		Size: 23.1 MB (23128312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539fef72f2c64e74c561d0e68cd80db043dd5ad01bbe7347ca85e600f5fe1dbe`  
		Last Modified: Fri, 12 Jul 2024 00:55:54 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243fde49abb4336be77d98c80e1d241323bb1a87a161483b6f9bce1af7d24af2`  
		Last Modified: Fri, 12 Jul 2024 00:55:54 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3623a23ea66a849d5c0687161e04a53e38f2c462d4de045c2f7f5aa605bd10f8`  
		Last Modified: Fri, 12 Jul 2024 00:55:55 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.7-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:f91680e82dd21ac882b9d2ef1da99cafbc381bd18fc38b86cc006745810feea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **901.1 KB (901084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dffd21e309fd08499f77ff40fbc52ff9d0413102f9fb858eee09334c9332cad6`

```dockerfile
```

-	Layers:
	-	`sha256:9e73138dd0ccec6f51005bb78bc926eb129316edb63e8f44d963f31eef2b5047`  
		Last Modified: Fri, 12 Jul 2024 00:55:53 GMT  
		Size: 870.3 KB (870337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:108de35f41a7454b6dbf4918439c03260e68749a123c4caa772c86bd4ed34a2b`  
		Last Modified: Fri, 12 Jul 2024 00:55:53 GMT  
		Size: 30.7 KB (30747 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:68a0ad0f478f4002bb56486d49fa3f53f61ef5a97d2de1a323308152e819745a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:053b555c82c43f155a480419bf4f6e025e6080f00d13455971c19381f1a9e898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (92012802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:008b14abfc6921435c404d82df72a3f9f8d974e5ec3d4ebc8f5b1c034ea5f66f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644653db676a15f1f50bac61ea74741812af17cf205867315c11d699f16fad2b`  
		Last Modified: Fri, 12 Jul 2024 00:55:53 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21bebbf70277f25932547a8637cd9367456a54d8ce8cb22fe4ebd0692bb0f4ac`  
		Last Modified: Fri, 12 Jul 2024 00:55:53 GMT  
		Size: 9.6 MB (9633408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a15a052dd483e14ed43222d004e26eeda1e18c8e7d84b6443f1a1b11d8b7b2`  
		Last Modified: Fri, 12 Jul 2024 00:55:53 GMT  
		Size: 5.8 MB (5820947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bbb02eef4582a56528c770a418f5f0bf7a6eb50223575a1ca849b51c18ab12`  
		Last Modified: Fri, 12 Jul 2024 00:55:53 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f09b3ac788a10f3050fa20e8b7e0ed1bb40e9fbb02549fbda4b4177a5c522f38`  
		Last Modified: Fri, 12 Jul 2024 00:55:54 GMT  
		Size: 49.8 MB (49798322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c93ff6cc6478170794864547261311a30a6d1e610e72c1817041ff43386f62`  
		Last Modified: Fri, 12 Jul 2024 00:55:54 GMT  
		Size: 23.1 MB (23128312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539fef72f2c64e74c561d0e68cd80db043dd5ad01bbe7347ca85e600f5fe1dbe`  
		Last Modified: Fri, 12 Jul 2024 00:55:54 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243fde49abb4336be77d98c80e1d241323bb1a87a161483b6f9bce1af7d24af2`  
		Last Modified: Fri, 12 Jul 2024 00:55:54 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3623a23ea66a849d5c0687161e04a53e38f2c462d4de045c2f7f5aa605bd10f8`  
		Last Modified: Fri, 12 Jul 2024 00:55:55 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:f91680e82dd21ac882b9d2ef1da99cafbc381bd18fc38b86cc006745810feea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **901.1 KB (901084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dffd21e309fd08499f77ff40fbc52ff9d0413102f9fb858eee09334c9332cad6`

```dockerfile
```

-	Layers:
	-	`sha256:9e73138dd0ccec6f51005bb78bc926eb129316edb63e8f44d963f31eef2b5047`  
		Last Modified: Fri, 12 Jul 2024 00:55:53 GMT  
		Size: 870.3 KB (870337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:108de35f41a7454b6dbf4918439c03260e68749a123c4caa772c86bd4ed34a2b`  
		Last Modified: Fri, 12 Jul 2024 00:55:53 GMT  
		Size: 30.7 KB (30747 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:8012710486cd42c92463f166da8f3cb85b6117bd1b4416f72d68da9b67253108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.7 MB (86695902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bffebd11d2bb8f925b4b3cd6896e225102f1181f44d14918d529fee04b36a479`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["/bin/sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=2.7.6
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd"]
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 06 Jun 2024 16:24:41 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4d02fd6d451824a88c3da056c35af5ef536e8a634a98239ab90c650e0518e3`  
		Last Modified: Fri, 21 Jun 2024 05:12:50 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2b01a32898b3b778615baf714c0f22bad40fe1d9dbddd0df741da93b96bf90`  
		Last Modified: Fri, 21 Jun 2024 05:12:51 GMT  
		Size: 9.8 MB (9750759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf24405751d72a203b1d9bebd0d05ff6dfef80c1932fb1494c98ba9278d9e588`  
		Last Modified: Fri, 21 Jun 2024 05:12:50 GMT  
		Size: 5.5 MB (5463802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12ebdf543d1e306cb0d041c1c843ba56ea37606cf20c4178fb8503420c5bd97`  
		Last Modified: Fri, 21 Jun 2024 05:12:50 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7f71798a2c4a5377d3c7cc1decb0d14434537b6266ab3a73a1a2000bc04d82`  
		Last Modified: Fri, 21 Jun 2024 05:12:53 GMT  
		Size: 45.7 MB (45722059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2f3dd6b1e82b054e5d7851d3d1180809055eed237a20961aad9352a720a1f8`  
		Last Modified: Fri, 21 Jun 2024 05:12:52 GMT  
		Size: 21.7 MB (21662516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2896f9dc4697a1df8ba98f785f4600faa604faf1d9fd61356428a8ae3224f633`  
		Last Modified: Fri, 21 Jun 2024 05:12:52 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dccba840458a1a7d517c9ac82f7a571e3946f75a62935610dfccaff09e4b2d2`  
		Last Modified: Fri, 21 Jun 2024 05:12:52 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea0d553a68019a537d89c04424ba1ec571aed2614c4973fb0ceb5af4af419a91`  
		Last Modified: Fri, 21 Jun 2024 05:12:53 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:c1b970eb2d343424b5d9f23632745417f45ba097b6a01ddb7bea505a7d3dd8ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **886.8 KB (886831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d814c5ee6f913730efa59405fc0deb9d4d1f5042aac36e4e798ffb4fe903d98`

```dockerfile
```

-	Layers:
	-	`sha256:43ab9a13bdfbf66d39011fa6361dbe012f8e5f72c6b42671ff9e70561b3e62b5`  
		Last Modified: Fri, 21 Jun 2024 05:12:50 GMT  
		Size: 855.8 KB (855784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f52cfecc2d36c66fba04e64b907e5b384907ca53f64768ef107bd1faf04ac22`  
		Last Modified: Fri, 21 Jun 2024 05:12:50 GMT  
		Size: 31.0 KB (31047 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:latest`

```console
$ docker pull influxdb@sha256:57fbc491438c428a43168665cb9ca12709787a75e7b545cb593fe985aee843df
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
$ docker pull influxdb@sha256:29bf443e32d6ae32fa7155f3290fb9973c67eadc2256a3439d9e86dac6724fcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.3 MB (158267065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:565b979370ac25e8eaf3d51a30c63003090d3132030ef1b6de6803be7448589d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["bash"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV GOSU_VER=1.16
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=2.7.6
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd"]
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 06 Jun 2024 16:24:41 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244a66b2072ea3f07e91b5f8184b4b2752882498edfa7ba8fb76bb6824526c2b`  
		Last Modified: Tue, 02 Jul 2024 15:16:35 GMT  
		Size: 9.6 MB (9584780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909cdb72b23dce52c0f4bdc1dc18109aa9783ec88ff7de35937b9a10ea4f316c`  
		Last Modified: Tue, 02 Jul 2024 15:16:35 GMT  
		Size: 5.5 MB (5463796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff5f5ed1b375c5e0d895d30718c85a37e3c35d0a71cf7046c55aecb926622a2`  
		Last Modified: Tue, 02 Jul 2024 15:16:34 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282638484353524b10cab2a7692a18a864399334bcf1de03c904bbf2cc8d3576`  
		Last Modified: Tue, 02 Jul 2024 15:16:35 GMT  
		Size: 936.1 KB (936109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd75da185cd23e91ecd8ed745c0cca7c52ece635d99420e6b01dcf7a0a27e70`  
		Last Modified: Tue, 02 Jul 2024 15:16:37 GMT  
		Size: 91.5 MB (91453342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae4d7c532325604d920b375d5e1430758fb552ce5cc36c4ab9cb5a05b65c8fa`  
		Last Modified: Tue, 02 Jul 2024 15:16:37 GMT  
		Size: 21.7 MB (21662524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d400046518a6ade36b53c8b3ce4daf1f0e4baa3e00a01dd08fc3a7a27d5e239`  
		Last Modified: Tue, 02 Jul 2024 15:16:36 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dcdc4d64e1e66a79c69bd9677064c35c2b3b7b74da85491b2f60a80b7fdba19`  
		Last Modified: Tue, 02 Jul 2024 15:16:36 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539bf8697e8ab15fe15693bf1ffd910f0cdbd1c6a1aaa191e7da688576172903`  
		Last Modified: Tue, 02 Jul 2024 15:16:37 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:f2790ef100ade36090587201b37bad93c11fff2e8506ad5ca487a06076b7c383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2788414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:090324d138ff85b22d7d2f7b9493272543308d0bded8ef2c755dfe7c7f632335`

```dockerfile
```

-	Layers:
	-	`sha256:467e558654341de92d1993ece4018c64703a2e99b759db120854bd05ff17abfb`  
		Last Modified: Tue, 02 Jul 2024 15:16:35 GMT  
		Size: 2.8 MB (2754571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f79da47dbbf0f3b0da23c1f787782d41583205fab27216314003bc1694b9704f`  
		Last Modified: Tue, 02 Jul 2024 15:16:34 GMT  
		Size: 33.8 KB (33843 bytes)  
		MIME: application/vnd.in-toto+json
