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
$ docker pull influxdb@sha256:444ac10d971d0f1970669b7b0be35763bdb9cf2c545d6782194e026081aff592
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-data` - linux; amd64

```console
$ docker pull influxdb@sha256:a510f3dda221d42b1cfee921ee2b7870a823f93967e08cfd94020bb3cdecc9c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112245319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c7b89693707242c1725d79dd63ded1d04e353cbd43f2fe946b2cf898fabcfbc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:d2a2ac890c4f902560feaadaac9f36a9b844131c97453ecb90241cf525185196 in / 
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
	-	`sha256:29f873e2e3f8f1b35ae4bee023807e71b6e16e714dbd1cbd19b3124c62e7634c`  
		Last Modified: Thu, 13 Jun 2024 01:25:49 GMT  
		Size: 55.1 MB (55099190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e1ed81430e2556f97ec363517655fd54e04e4f6b0eaa55faa9aa88490e96d9`  
		Last Modified: Thu, 13 Jun 2024 03:50:28 GMT  
		Size: 15.8 MB (15764834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006a70ad0c3fa769de0312c86d1532eecebd99e18de8748f37f5f33a4e496588`  
		Last Modified: Thu, 13 Jun 2024 18:28:40 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7af11a09cd38a1bb3193cf005130739729b872e9371b111728e14d28245705a`  
		Last Modified: Thu, 13 Jun 2024 18:28:42 GMT  
		Size: 41.4 MB (41377751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e960f8f51a21473b22bd32c2601047f9e68b7bf8e14e36a034510a72932d719`  
		Last Modified: Thu, 13 Jun 2024 18:28:40 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a419980cca3d72ba3679c38400ba2c86c700de0494acff47df58de42017b9d21`  
		Last Modified: Thu, 13 Jun 2024 18:28:41 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36ff6e3fdb3bf5612ed3dbee1f682a7ef0452ef26184183a6e1967dadb15b14`  
		Last Modified: Thu, 13 Jun 2024 18:28:41 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:c9430221938ee756fdbbd050baf6402881edae0504923e069b306bfeedabe069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4593883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bee4490c9a7f01b305f49087644b6b3008198091b92f55b5ee95332b19b9a39f`

```dockerfile
```

-	Layers:
	-	`sha256:19f939e26d52a40100e19584933a7ea0a2cb12754e9d6392b11266cb71ab7426`  
		Last Modified: Thu, 13 Jun 2024 18:28:41 GMT  
		Size: 4.6 MB (4579309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b2fc2cb802caecbe7105b6f62ac794b55fb5669b6f373c6aa135e4965c0d1d3`  
		Last Modified: Thu, 13 Jun 2024 18:28:40 GMT  
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
$ docker pull influxdb@sha256:c2689cd574fcb06ac2ed20c4a08826bcb121847df21771db056973e886a4bdc8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:bcedf12bdccaec1b53010b19490d0472b607525c711773a0d6237ded731dd6b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.0 MB (90961944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b4f0d377cf9409c9ba1fe8ed1520e03be799f29b1287610f6ee4941db32739`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:d2a2ac890c4f902560feaadaac9f36a9b844131c97453ecb90241cf525185196 in / 
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
	-	`sha256:29f873e2e3f8f1b35ae4bee023807e71b6e16e714dbd1cbd19b3124c62e7634c`  
		Last Modified: Thu, 13 Jun 2024 01:25:49 GMT  
		Size: 55.1 MB (55099190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e1ed81430e2556f97ec363517655fd54e04e4f6b0eaa55faa9aa88490e96d9`  
		Last Modified: Thu, 13 Jun 2024 03:50:28 GMT  
		Size: 15.8 MB (15764834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe325bea5fa295da512eefcd28e2c9cd4735c198213bc5d3af11391e7255efcd`  
		Last Modified: Thu, 13 Jun 2024 18:28:32 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:538bc5f5918327e11b766749581572bfeb5c907f5f92dc7b68f90d9979c983b8`  
		Last Modified: Thu, 13 Jun 2024 18:28:32 GMT  
		Size: 20.1 MB (20095568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b6187743f48aede39fcd31cc3fd10ad2252a657cc1df32cf99770bb07da3462`  
		Last Modified: Thu, 13 Jun 2024 18:28:32 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e221ae9cb90080504a204fee036be9206886567254032197212c240b50eb14`  
		Last Modified: Thu, 13 Jun 2024 18:28:32 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:41b8f653b32b0effe2f18c599dc82b23280b2524ab528ce442b402fb498fba8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4529114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12a20909246843a6051ac311b5a0c5307fcbb07819a615d11b92966d14ae5574`

```dockerfile
```

-	Layers:
	-	`sha256:fa0812bd9ad86da041248a37a207cd084bc31f3eefc0e5dc105c95defc669cf2`  
		Last Modified: Thu, 13 Jun 2024 18:28:32 GMT  
		Size: 4.5 MB (4516194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bbb188a42ebd5df73a5d9c23c68e6d01bd789a3e2b648132fbd83d9ee72d9d7`  
		Last Modified: Thu, 13 Jun 2024 18:28:32 GMT  
		Size: 12.9 KB (12920 bytes)  
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
$ docker pull influxdb@sha256:444ac10d971d0f1970669b7b0be35763bdb9cf2c545d6782194e026081aff592
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.7-data` - linux; amd64

```console
$ docker pull influxdb@sha256:a510f3dda221d42b1cfee921ee2b7870a823f93967e08cfd94020bb3cdecc9c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112245319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c7b89693707242c1725d79dd63ded1d04e353cbd43f2fe946b2cf898fabcfbc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:d2a2ac890c4f902560feaadaac9f36a9b844131c97453ecb90241cf525185196 in / 
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
	-	`sha256:29f873e2e3f8f1b35ae4bee023807e71b6e16e714dbd1cbd19b3124c62e7634c`  
		Last Modified: Thu, 13 Jun 2024 01:25:49 GMT  
		Size: 55.1 MB (55099190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e1ed81430e2556f97ec363517655fd54e04e4f6b0eaa55faa9aa88490e96d9`  
		Last Modified: Thu, 13 Jun 2024 03:50:28 GMT  
		Size: 15.8 MB (15764834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006a70ad0c3fa769de0312c86d1532eecebd99e18de8748f37f5f33a4e496588`  
		Last Modified: Thu, 13 Jun 2024 18:28:40 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7af11a09cd38a1bb3193cf005130739729b872e9371b111728e14d28245705a`  
		Last Modified: Thu, 13 Jun 2024 18:28:42 GMT  
		Size: 41.4 MB (41377751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e960f8f51a21473b22bd32c2601047f9e68b7bf8e14e36a034510a72932d719`  
		Last Modified: Thu, 13 Jun 2024 18:28:40 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a419980cca3d72ba3679c38400ba2c86c700de0494acff47df58de42017b9d21`  
		Last Modified: Thu, 13 Jun 2024 18:28:41 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36ff6e3fdb3bf5612ed3dbee1f682a7ef0452ef26184183a6e1967dadb15b14`  
		Last Modified: Thu, 13 Jun 2024 18:28:41 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.7-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:c9430221938ee756fdbbd050baf6402881edae0504923e069b306bfeedabe069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4593883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bee4490c9a7f01b305f49087644b6b3008198091b92f55b5ee95332b19b9a39f`

```dockerfile
```

-	Layers:
	-	`sha256:19f939e26d52a40100e19584933a7ea0a2cb12754e9d6392b11266cb71ab7426`  
		Last Modified: Thu, 13 Jun 2024 18:28:41 GMT  
		Size: 4.6 MB (4579309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b2fc2cb802caecbe7105b6f62ac794b55fb5669b6f373c6aa135e4965c0d1d3`  
		Last Modified: Thu, 13 Jun 2024 18:28:40 GMT  
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
$ docker pull influxdb@sha256:c2689cd574fcb06ac2ed20c4a08826bcb121847df21771db056973e886a4bdc8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.7-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:bcedf12bdccaec1b53010b19490d0472b607525c711773a0d6237ded731dd6b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.0 MB (90961944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b4f0d377cf9409c9ba1fe8ed1520e03be799f29b1287610f6ee4941db32739`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:d2a2ac890c4f902560feaadaac9f36a9b844131c97453ecb90241cf525185196 in / 
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
	-	`sha256:29f873e2e3f8f1b35ae4bee023807e71b6e16e714dbd1cbd19b3124c62e7634c`  
		Last Modified: Thu, 13 Jun 2024 01:25:49 GMT  
		Size: 55.1 MB (55099190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e1ed81430e2556f97ec363517655fd54e04e4f6b0eaa55faa9aa88490e96d9`  
		Last Modified: Thu, 13 Jun 2024 03:50:28 GMT  
		Size: 15.8 MB (15764834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe325bea5fa295da512eefcd28e2c9cd4735c198213bc5d3af11391e7255efcd`  
		Last Modified: Thu, 13 Jun 2024 18:28:32 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:538bc5f5918327e11b766749581572bfeb5c907f5f92dc7b68f90d9979c983b8`  
		Last Modified: Thu, 13 Jun 2024 18:28:32 GMT  
		Size: 20.1 MB (20095568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b6187743f48aede39fcd31cc3fd10ad2252a657cc1df32cf99770bb07da3462`  
		Last Modified: Thu, 13 Jun 2024 18:28:32 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e221ae9cb90080504a204fee036be9206886567254032197212c240b50eb14`  
		Last Modified: Thu, 13 Jun 2024 18:28:32 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.7-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:41b8f653b32b0effe2f18c599dc82b23280b2524ab528ce442b402fb498fba8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4529114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12a20909246843a6051ac311b5a0c5307fcbb07819a615d11b92966d14ae5574`

```dockerfile
```

-	Layers:
	-	`sha256:fa0812bd9ad86da041248a37a207cd084bc31f3eefc0e5dc105c95defc669cf2`  
		Last Modified: Thu, 13 Jun 2024 18:28:32 GMT  
		Size: 4.5 MB (4516194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bbb188a42ebd5df73a5d9c23c68e6d01bd789a3e2b648132fbd83d9ee72d9d7`  
		Last Modified: Thu, 13 Jun 2024 18:28:32 GMT  
		Size: 12.9 KB (12920 bytes)  
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
$ docker pull influxdb@sha256:81b5ad6321a313fe7f82a7c34276cd6fe72ffa18223a5367f9f03c521d165e0a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data` - linux; amd64

```console
$ docker pull influxdb@sha256:f057f85707e88d4526ed6a1d5fa0c06c8292063847ddd73636f31630af3bb907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115452899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21912531e87eaa668568594fdfe9ed9974a267b80b7e7dc6084df2dba3e13f65`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:b532f8e401e9a1fcc2ea1fc034adf820a5269c6ace45769f60a81fcb673f01b8 in / 
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
	-	`sha256:fea1432adf0957427b45b0ef8e37cbfe045b7cf8c15e3f43e48f2f613e214d16`  
		Last Modified: Thu, 13 Jun 2024 01:25:07 GMT  
		Size: 49.6 MB (49576643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5651b5803b186603909f6c77cdff7bdd4ba7ab8ca4ebccb5a6b0be9037b4e5b6`  
		Last Modified: Thu, 13 Jun 2024 03:49:21 GMT  
		Size: 24.1 MB (24050013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70a86055641dc24259b5c02d9931a17cf67483bcb3ca83e648c6394116a7fc2`  
		Last Modified: Thu, 13 Jun 2024 18:28:44 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a925d31b68388a415295462ccc507bc225784e8c72c6948d746b1dc7034e3162`  
		Last Modified: Thu, 13 Jun 2024 18:28:45 GMT  
		Size: 41.8 MB (41822688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774d1b873d3cdefbcf10f7079ac83024b97f7ba67599ee47bad9accb57188878`  
		Last Modified: Thu, 13 Jun 2024 18:28:44 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f6f6cf8334a813f05b6d7b51a4a588d9d664a707ee6c61002a224c72b8e3e7`  
		Last Modified: Thu, 13 Jun 2024 18:28:44 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2eb468c01062e48661761acf6b87176853cac5b90a1f3214d88f57e12bb081`  
		Last Modified: Thu, 13 Jun 2024 18:28:45 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:c28e5f0926c58e9af2de1e30a15540dec5c25b5166a067603d584902e5d3af10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4469120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a74de3c17d68b0fcdde108e9fd466a909fccea7e81e5bd1638544ef52d9aa7f`

```dockerfile
```

-	Layers:
	-	`sha256:3d93801a7b08e3015eefc8dc425b8d94e2ffc8c2767860383f86d28321b9d310`  
		Last Modified: Thu, 13 Jun 2024 18:28:44 GMT  
		Size: 4.5 MB (4454546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d6780ac418457fdf075d25b6d65b7c3c621f12288a6eb596f21fb087062522c`  
		Last Modified: Thu, 13 Jun 2024 18:28:44 GMT  
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
$ docker pull influxdb@sha256:52c8a1612bfb1817fd0af25701f576bc220c87dcc8ad1ef76e8f9652cb4be0c8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:837cdb359ac6b90948414fa056bb2786e423feec0d12c4a47225d51da23114b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (94022063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f4e2a99085a5f46a1b1d668425daacf77d2d5c66b48934fae5e1ac104a675f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:b532f8e401e9a1fcc2ea1fc034adf820a5269c6ace45769f60a81fcb673f01b8 in / 
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
	-	`sha256:fea1432adf0957427b45b0ef8e37cbfe045b7cf8c15e3f43e48f2f613e214d16`  
		Last Modified: Thu, 13 Jun 2024 01:25:07 GMT  
		Size: 49.6 MB (49576643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5651b5803b186603909f6c77cdff7bdd4ba7ab8ca4ebccb5a6b0be9037b4e5b6`  
		Last Modified: Thu, 13 Jun 2024 03:49:21 GMT  
		Size: 24.1 MB (24050013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f04efdc0ddd8684eb7ca3ecf605fab0c132264cb9e83f7a8b366ce8e1e3eea96`  
		Last Modified: Thu, 13 Jun 2024 18:28:44 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c193c84c0c0801833f3284bb7d7cf2c44cd820d96935ed3b66985dede0a74f5`  
		Last Modified: Thu, 13 Jun 2024 18:28:45 GMT  
		Size: 20.4 MB (20393059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624ba9dd5223c9f0c7bab069f2dbcee955b3f40d5da32d4dbcb1223a849cd8db`  
		Last Modified: Thu, 13 Jun 2024 18:28:44 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4402042ce8b0d8a1efeaeb68a2993e262b3492c0187d812b6e3124b462970153`  
		Last Modified: Thu, 13 Jun 2024 18:28:44 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:489e37b6936c75d54526311839f5d51a99f3ff6ad07d00e6fda8f238b8bf61e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4404907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2218c9cf76f2ecd0bd6f7ee333e1ddf900133a659e22c754e40d39a1721b1b4c`

```dockerfile
```

-	Layers:
	-	`sha256:677087dd3bd16f310a285d49e02b7494b001828c8aa35ab5f53d991fe67bbd45`  
		Last Modified: Thu, 13 Jun 2024 18:28:45 GMT  
		Size: 4.4 MB (4391986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51d6e771742b70b4f9e26c492e0e4955514046357577f252759ce2700770c00c`  
		Last Modified: Thu, 13 Jun 2024 18:28:44 GMT  
		Size: 12.9 KB (12921 bytes)  
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
$ docker pull influxdb@sha256:81b5ad6321a313fe7f82a7c34276cd6fe72ffa18223a5367f9f03c521d165e0a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.5-data` - linux; amd64

```console
$ docker pull influxdb@sha256:f057f85707e88d4526ed6a1d5fa0c06c8292063847ddd73636f31630af3bb907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115452899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21912531e87eaa668568594fdfe9ed9974a267b80b7e7dc6084df2dba3e13f65`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:b532f8e401e9a1fcc2ea1fc034adf820a5269c6ace45769f60a81fcb673f01b8 in / 
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
	-	`sha256:fea1432adf0957427b45b0ef8e37cbfe045b7cf8c15e3f43e48f2f613e214d16`  
		Last Modified: Thu, 13 Jun 2024 01:25:07 GMT  
		Size: 49.6 MB (49576643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5651b5803b186603909f6c77cdff7bdd4ba7ab8ca4ebccb5a6b0be9037b4e5b6`  
		Last Modified: Thu, 13 Jun 2024 03:49:21 GMT  
		Size: 24.1 MB (24050013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70a86055641dc24259b5c02d9931a17cf67483bcb3ca83e648c6394116a7fc2`  
		Last Modified: Thu, 13 Jun 2024 18:28:44 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a925d31b68388a415295462ccc507bc225784e8c72c6948d746b1dc7034e3162`  
		Last Modified: Thu, 13 Jun 2024 18:28:45 GMT  
		Size: 41.8 MB (41822688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774d1b873d3cdefbcf10f7079ac83024b97f7ba67599ee47bad9accb57188878`  
		Last Modified: Thu, 13 Jun 2024 18:28:44 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f6f6cf8334a813f05b6d7b51a4a588d9d664a707ee6c61002a224c72b8e3e7`  
		Last Modified: Thu, 13 Jun 2024 18:28:44 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2eb468c01062e48661761acf6b87176853cac5b90a1f3214d88f57e12bb081`  
		Last Modified: Thu, 13 Jun 2024 18:28:45 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.5-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:c28e5f0926c58e9af2de1e30a15540dec5c25b5166a067603d584902e5d3af10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4469120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a74de3c17d68b0fcdde108e9fd466a909fccea7e81e5bd1638544ef52d9aa7f`

```dockerfile
```

-	Layers:
	-	`sha256:3d93801a7b08e3015eefc8dc425b8d94e2ffc8c2767860383f86d28321b9d310`  
		Last Modified: Thu, 13 Jun 2024 18:28:44 GMT  
		Size: 4.5 MB (4454546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d6780ac418457fdf075d25b6d65b7c3c621f12288a6eb596f21fb087062522c`  
		Last Modified: Thu, 13 Jun 2024 18:28:44 GMT  
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
$ docker pull influxdb@sha256:52c8a1612bfb1817fd0af25701f576bc220c87dcc8ad1ef76e8f9652cb4be0c8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.5-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:837cdb359ac6b90948414fa056bb2786e423feec0d12c4a47225d51da23114b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (94022063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f4e2a99085a5f46a1b1d668425daacf77d2d5c66b48934fae5e1ac104a675f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:b532f8e401e9a1fcc2ea1fc034adf820a5269c6ace45769f60a81fcb673f01b8 in / 
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
	-	`sha256:fea1432adf0957427b45b0ef8e37cbfe045b7cf8c15e3f43e48f2f613e214d16`  
		Last Modified: Thu, 13 Jun 2024 01:25:07 GMT  
		Size: 49.6 MB (49576643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5651b5803b186603909f6c77cdff7bdd4ba7ab8ca4ebccb5a6b0be9037b4e5b6`  
		Last Modified: Thu, 13 Jun 2024 03:49:21 GMT  
		Size: 24.1 MB (24050013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f04efdc0ddd8684eb7ca3ecf605fab0c132264cb9e83f7a8b366ce8e1e3eea96`  
		Last Modified: Thu, 13 Jun 2024 18:28:44 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c193c84c0c0801833f3284bb7d7cf2c44cd820d96935ed3b66985dede0a74f5`  
		Last Modified: Thu, 13 Jun 2024 18:28:45 GMT  
		Size: 20.4 MB (20393059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624ba9dd5223c9f0c7bab069f2dbcee955b3f40d5da32d4dbcb1223a849cd8db`  
		Last Modified: Thu, 13 Jun 2024 18:28:44 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4402042ce8b0d8a1efeaeb68a2993e262b3492c0187d812b6e3124b462970153`  
		Last Modified: Thu, 13 Jun 2024 18:28:44 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.5-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:489e37b6936c75d54526311839f5d51a99f3ff6ad07d00e6fda8f238b8bf61e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4404907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2218c9cf76f2ecd0bd6f7ee333e1ddf900133a659e22c754e40d39a1721b1b4c`

```dockerfile
```

-	Layers:
	-	`sha256:677087dd3bd16f310a285d49e02b7494b001828c8aa35ab5f53d991fe67bbd45`  
		Last Modified: Thu, 13 Jun 2024 18:28:45 GMT  
		Size: 4.4 MB (4391986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51d6e771742b70b4f9e26c492e0e4955514046357577f252759ce2700770c00c`  
		Last Modified: Thu, 13 Jun 2024 18:28:44 GMT  
		Size: 12.9 KB (12921 bytes)  
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
$ docker pull influxdb@sha256:344806154e3f76736c5d5880838276758bc9c6455ee9952815b51e3c0c8595f0
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
$ docker pull influxdb@sha256:ce2dfa3b03c14ea8a917cebed2457493f1e586bff15162ebf3de5bc4463430d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125752851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0067f69032c84af27d9fe1f4e917f626da1ff2c9d98cab7ebc688dc16f9e88a5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:d2a2ac890c4f902560feaadaac9f36a9b844131c97453ecb90241cf525185196 in / 
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
	-	`sha256:29f873e2e3f8f1b35ae4bee023807e71b6e16e714dbd1cbd19b3124c62e7634c`  
		Last Modified: Thu, 13 Jun 2024 01:25:49 GMT  
		Size: 55.1 MB (55099190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e1ed81430e2556f97ec363517655fd54e04e4f6b0eaa55faa9aa88490e96d9`  
		Last Modified: Thu, 13 Jun 2024 03:50:28 GMT  
		Size: 15.8 MB (15764834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d220f7af07d471eec68cd698fe1363ee69a2f7a926bfd50f1eb96ba1bf4dce`  
		Last Modified: Thu, 13 Jun 2024 18:28:27 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9705621dee45f1f9e5647a7d6ca47e541d2afa241e303d2058bf8b30283192`  
		Last Modified: Thu, 13 Jun 2024 18:28:28 GMT  
		Size: 54.9 MB (54885339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b28c35e15bf441fc6995e5c298361ff2c8410779bd74f912d257b8b7809a78`  
		Last Modified: Thu, 13 Jun 2024 18:28:27 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd6a1c1ce75b899a8c47b6fe54f2156c7634d79ce7b5bdf55dd107f4401a2f4`  
		Last Modified: Thu, 13 Jun 2024 18:28:27 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22644748f9bcbf70be4a399e048e8bcbaa7c30a44d30a80c4082e4966042ff8f`  
		Last Modified: Thu, 13 Jun 2024 18:28:28 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:c0ea11133afa3fdf341c29556b5bfb1f3135fb6e93466b467878c2e8f90ee008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4478485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc06c4941c99fbbb48a4d94ad9f18f1dc5eea9f9850689a98ea5c8a1ca93b90`

```dockerfile
```

-	Layers:
	-	`sha256:5be49328e38c50cb64b1303f45e70e83c9d75e46b949144ddbe47feded49b688`  
		Last Modified: Thu, 13 Jun 2024 18:28:27 GMT  
		Size: 4.5 MB (4463023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:666d0f50bfc45d5e5ccaded91de9a2e3cd2fc2500bad83bbac48b4452fbb604b`  
		Last Modified: Thu, 13 Jun 2024 18:28:27 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.8` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:73ed0545d0d7b4750b82348b80637a6ee5b43fa6b5dc1f7119e9385a35b4a5a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116752976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b6467f69d4c0618ed63f2839f6e74733f26b8485c01aeb6076bd414c30e270`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:4993add96e8cc180b89e1b978fddc0b0876a303bce87dc08120edbe9513432bd in / 
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
	-	`sha256:45c5e98886f73bd45565e271bba1de66ffee1cfe17345d38a8e7179841133d4f`  
		Last Modified: Thu, 13 Jun 2024 01:01:59 GMT  
		Size: 50.3 MB (50256430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d823c90ec6db52ee3c5a3a116b21e47442be8c0e35cc53f6f7f4db398ba08fe`  
		Last Modified: Thu, 13 Jun 2024 01:34:16 GMT  
		Size: 14.9 MB (14880170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4a19f7612bbb72940cdb51cd2101cb18ebfaf1a8626e2a3439a67deaee2a45`  
		Last Modified: Thu, 13 Jun 2024 19:47:50 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc91d1881f12116fa9079825376d00db58c069f271f70480296f9d73e5f9214`  
		Last Modified: Thu, 13 Jun 2024 19:47:52 GMT  
		Size: 51.6 MB (51612887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee905aa2a8918b373df9724acef14e55cc2f2fe140a30fe2d73af3d023d320aa`  
		Last Modified: Thu, 13 Jun 2024 19:47:50 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251896ff9028ac4ce43839a2ade13e6d35d725129ceebf2a9e7afa48bd0cefdb`  
		Last Modified: Thu, 13 Jun 2024 19:47:50 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7d8d8854d045b9b1ac6560c4e7d2d326e6745403a6d8559103669152f47856`  
		Last Modified: Thu, 13 Jun 2024 19:47:51 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:fabf9d73f8a655423f971923ff727ec760097cdfbd3b02e5d5add121cbce8c90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4480186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5004d84faed8b4e29d7a335a9b3cb755e56f075c1b049065db004cefeeb9d822`

```dockerfile
```

-	Layers:
	-	`sha256:a4abcc921434578a4c84c315ac2aa09c27a014254ab11e90e1205c5685eb30fb`  
		Last Modified: Thu, 13 Jun 2024 19:47:51 GMT  
		Size: 4.5 MB (4464657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa91e7e749ecac64d2a06978219e9f3620094238c6a58b8f6d4e40ba487ff67e`  
		Last Modified: Thu, 13 Jun 2024 19:47:50 GMT  
		Size: 15.5 KB (15529 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:1caf2085dba3d9a8bbfa1ec8bea174a870ba8b909153181d5a414b0473410398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120723436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62a3066ce71bd8b347cafa915f8e86245399256baeb3fe2b3dfb70f1926ec3fe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:cd3edc79f93d09aa5daffba99cc698c3fe0e02348e8dc284ef466b7e6596e68c in / 
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
	-	`sha256:f975e52008de385eb513258b4912477b214cddf1c8e87877f85028d940bfcdae`  
		Last Modified: Thu, 13 Jun 2024 00:43:32 GMT  
		Size: 53.7 MB (53739581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859b5bb8f5d471015f3add7e778bc507fc4a6f1fce8561c2b0a336734a55a365`  
		Last Modified: Thu, 13 Jun 2024 01:31:15 GMT  
		Size: 15.8 MB (15750467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b2fb20f9f51757e797e545393f33b973f5dc2a7c1dd712ecf0e5991d5918e8`  
		Last Modified: Thu, 13 Jun 2024 19:05:43 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da5ae0423c2e85505018c5b499f925f04388c20431940db3692ae98fb231f2d`  
		Last Modified: Thu, 13 Jun 2024 19:05:45 GMT  
		Size: 51.2 MB (51229889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62508be208408a3c8a880e27494c6b9fee7aef78ebc5a9750a056c26db72a2a`  
		Last Modified: Thu, 13 Jun 2024 19:05:44 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94feea3223345147a3e497a14d9aa4e9a05d2f6910c91fff8ec3b156cc683294`  
		Last Modified: Thu, 13 Jun 2024 19:05:44 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e36e4aebd642d8c367809784144ecdb816bdd8e7725cf71f749711929cecbc`  
		Last Modified: Thu, 13 Jun 2024 19:05:45 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:646a94f8a3f0346228055dac352d07982eaa0f17455f40c6c135d3455c418cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4478390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:073640e935c37c6c6b6022684081580d3578edee045177e0e9c2794c4cd1fa80`

```dockerfile
```

-	Layers:
	-	`sha256:61b783c8655800c4db918c6eda2b014773c25666a071a3a83c5aee46a86df699`  
		Last Modified: Thu, 13 Jun 2024 19:05:44 GMT  
		Size: 4.5 MB (4462635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b112ed998e8d9a8938adfff07e3e86921b17771130d2468075188c4ad0e01a4b`  
		Last Modified: Thu, 13 Jun 2024 19:05:44 GMT  
		Size: 15.8 KB (15755 bytes)  
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
$ docker pull influxdb@sha256:344806154e3f76736c5d5880838276758bc9c6455ee9952815b51e3c0c8595f0
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
$ docker pull influxdb@sha256:ce2dfa3b03c14ea8a917cebed2457493f1e586bff15162ebf3de5bc4463430d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125752851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0067f69032c84af27d9fe1f4e917f626da1ff2c9d98cab7ebc688dc16f9e88a5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:d2a2ac890c4f902560feaadaac9f36a9b844131c97453ecb90241cf525185196 in / 
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
	-	`sha256:29f873e2e3f8f1b35ae4bee023807e71b6e16e714dbd1cbd19b3124c62e7634c`  
		Last Modified: Thu, 13 Jun 2024 01:25:49 GMT  
		Size: 55.1 MB (55099190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e1ed81430e2556f97ec363517655fd54e04e4f6b0eaa55faa9aa88490e96d9`  
		Last Modified: Thu, 13 Jun 2024 03:50:28 GMT  
		Size: 15.8 MB (15764834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d220f7af07d471eec68cd698fe1363ee69a2f7a926bfd50f1eb96ba1bf4dce`  
		Last Modified: Thu, 13 Jun 2024 18:28:27 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9705621dee45f1f9e5647a7d6ca47e541d2afa241e303d2058bf8b30283192`  
		Last Modified: Thu, 13 Jun 2024 18:28:28 GMT  
		Size: 54.9 MB (54885339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b28c35e15bf441fc6995e5c298361ff2c8410779bd74f912d257b8b7809a78`  
		Last Modified: Thu, 13 Jun 2024 18:28:27 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd6a1c1ce75b899a8c47b6fe54f2156c7634d79ce7b5bdf55dd107f4401a2f4`  
		Last Modified: Thu, 13 Jun 2024 18:28:27 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22644748f9bcbf70be4a399e048e8bcbaa7c30a44d30a80c4082e4966042ff8f`  
		Last Modified: Thu, 13 Jun 2024 18:28:28 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8.10` - unknown; unknown

```console
$ docker pull influxdb@sha256:c0ea11133afa3fdf341c29556b5bfb1f3135fb6e93466b467878c2e8f90ee008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4478485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc06c4941c99fbbb48a4d94ad9f18f1dc5eea9f9850689a98ea5c8a1ca93b90`

```dockerfile
```

-	Layers:
	-	`sha256:5be49328e38c50cb64b1303f45e70e83c9d75e46b949144ddbe47feded49b688`  
		Last Modified: Thu, 13 Jun 2024 18:28:27 GMT  
		Size: 4.5 MB (4463023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:666d0f50bfc45d5e5ccaded91de9a2e3cd2fc2500bad83bbac48b4452fbb604b`  
		Last Modified: Thu, 13 Jun 2024 18:28:27 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.8.10` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:73ed0545d0d7b4750b82348b80637a6ee5b43fa6b5dc1f7119e9385a35b4a5a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116752976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b6467f69d4c0618ed63f2839f6e74733f26b8485c01aeb6076bd414c30e270`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:4993add96e8cc180b89e1b978fddc0b0876a303bce87dc08120edbe9513432bd in / 
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
	-	`sha256:45c5e98886f73bd45565e271bba1de66ffee1cfe17345d38a8e7179841133d4f`  
		Last Modified: Thu, 13 Jun 2024 01:01:59 GMT  
		Size: 50.3 MB (50256430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d823c90ec6db52ee3c5a3a116b21e47442be8c0e35cc53f6f7f4db398ba08fe`  
		Last Modified: Thu, 13 Jun 2024 01:34:16 GMT  
		Size: 14.9 MB (14880170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4a19f7612bbb72940cdb51cd2101cb18ebfaf1a8626e2a3439a67deaee2a45`  
		Last Modified: Thu, 13 Jun 2024 19:47:50 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc91d1881f12116fa9079825376d00db58c069f271f70480296f9d73e5f9214`  
		Last Modified: Thu, 13 Jun 2024 19:47:52 GMT  
		Size: 51.6 MB (51612887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee905aa2a8918b373df9724acef14e55cc2f2fe140a30fe2d73af3d023d320aa`  
		Last Modified: Thu, 13 Jun 2024 19:47:50 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251896ff9028ac4ce43839a2ade13e6d35d725129ceebf2a9e7afa48bd0cefdb`  
		Last Modified: Thu, 13 Jun 2024 19:47:50 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7d8d8854d045b9b1ac6560c4e7d2d326e6745403a6d8559103669152f47856`  
		Last Modified: Thu, 13 Jun 2024 19:47:51 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8.10` - unknown; unknown

```console
$ docker pull influxdb@sha256:fabf9d73f8a655423f971923ff727ec760097cdfbd3b02e5d5add121cbce8c90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4480186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5004d84faed8b4e29d7a335a9b3cb755e56f075c1b049065db004cefeeb9d822`

```dockerfile
```

-	Layers:
	-	`sha256:a4abcc921434578a4c84c315ac2aa09c27a014254ab11e90e1205c5685eb30fb`  
		Last Modified: Thu, 13 Jun 2024 19:47:51 GMT  
		Size: 4.5 MB (4464657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa91e7e749ecac64d2a06978219e9f3620094238c6a58b8f6d4e40ba487ff67e`  
		Last Modified: Thu, 13 Jun 2024 19:47:50 GMT  
		Size: 15.5 KB (15529 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.8.10` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:1caf2085dba3d9a8bbfa1ec8bea174a870ba8b909153181d5a414b0473410398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120723436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62a3066ce71bd8b347cafa915f8e86245399256baeb3fe2b3dfb70f1926ec3fe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:cd3edc79f93d09aa5daffba99cc698c3fe0e02348e8dc284ef466b7e6596e68c in / 
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
	-	`sha256:f975e52008de385eb513258b4912477b214cddf1c8e87877f85028d940bfcdae`  
		Last Modified: Thu, 13 Jun 2024 00:43:32 GMT  
		Size: 53.7 MB (53739581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859b5bb8f5d471015f3add7e778bc507fc4a6f1fce8561c2b0a336734a55a365`  
		Last Modified: Thu, 13 Jun 2024 01:31:15 GMT  
		Size: 15.8 MB (15750467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b2fb20f9f51757e797e545393f33b973f5dc2a7c1dd712ecf0e5991d5918e8`  
		Last Modified: Thu, 13 Jun 2024 19:05:43 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da5ae0423c2e85505018c5b499f925f04388c20431940db3692ae98fb231f2d`  
		Last Modified: Thu, 13 Jun 2024 19:05:45 GMT  
		Size: 51.2 MB (51229889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62508be208408a3c8a880e27494c6b9fee7aef78ebc5a9750a056c26db72a2a`  
		Last Modified: Thu, 13 Jun 2024 19:05:44 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94feea3223345147a3e497a14d9aa4e9a05d2f6910c91fff8ec3b156cc683294`  
		Last Modified: Thu, 13 Jun 2024 19:05:44 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e36e4aebd642d8c367809784144ecdb816bdd8e7725cf71f749711929cecbc`  
		Last Modified: Thu, 13 Jun 2024 19:05:45 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8.10` - unknown; unknown

```console
$ docker pull influxdb@sha256:646a94f8a3f0346228055dac352d07982eaa0f17455f40c6c135d3455c418cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4478390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:073640e935c37c6c6b6022684081580d3578edee045177e0e9c2794c4cd1fa80`

```dockerfile
```

-	Layers:
	-	`sha256:61b783c8655800c4db918c6eda2b014773c25666a071a3a83c5aee46a86df699`  
		Last Modified: Thu, 13 Jun 2024 19:05:44 GMT  
		Size: 4.5 MB (4462635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b112ed998e8d9a8938adfff07e3e86921b17771130d2468075188c4ad0e01a4b`  
		Last Modified: Thu, 13 Jun 2024 19:05:44 GMT  
		Size: 15.8 KB (15755 bytes)  
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
$ docker pull influxdb@sha256:86ab0b6fb1399dba796baae8053bb25d6d25a05abe290e9653c0db9c7c78b005
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9-data` - linux; amd64

```console
$ docker pull influxdb@sha256:700982e519ea56c8e1939a5165762a25ccff1ae1eeb8ffcd7a6e3279235cd2ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 MB (104156541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e60bc6b4ddab6bc9a44ff13c4be3c4b36ac9c9ff88b207d4becede1010bfb7f9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:d2a2ac890c4f902560feaadaac9f36a9b844131c97453ecb90241cf525185196 in / 
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
	-	`sha256:29f873e2e3f8f1b35ae4bee023807e71b6e16e714dbd1cbd19b3124c62e7634c`  
		Last Modified: Thu, 13 Jun 2024 01:25:49 GMT  
		Size: 55.1 MB (55099190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e1ed81430e2556f97ec363517655fd54e04e4f6b0eaa55faa9aa88490e96d9`  
		Last Modified: Thu, 13 Jun 2024 03:50:28 GMT  
		Size: 15.8 MB (15764834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4dcc94a6f1fa678d46b0ab818eb0d724838181ccdcd4dcefc6913f747fc905b`  
		Last Modified: Thu, 13 Jun 2024 18:28:30 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957594b16e0b0064114b23dc1892010a4dc90c0baa98a705648fd577048b7ff9`  
		Last Modified: Thu, 13 Jun 2024 18:28:31 GMT  
		Size: 33.3 MB (33288959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef58e8a1f016a39de2d8492b12dad5a839739ebd4cb0848658937b8c74c256b4`  
		Last Modified: Thu, 13 Jun 2024 18:28:30 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6564b87df9d45ec2f4296c078d8ef71d21b0b481ae66bc5a19783f5adeb3ff`  
		Last Modified: Thu, 13 Jun 2024 18:28:30 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacf028904564dbe0b651cd88b8b37e130c26de6c11d4fdba9ecb9bf29fcef7c`  
		Last Modified: Thu, 13 Jun 2024 18:28:31 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:74c0ca665848d5667a5c68800b848cbf6d9d4cfdbc510f3954a7a1883555d930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4584570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc0f1357d42478766f9631ff434bae81f20feebf611c7c38d2b2781fa2c2d4a`

```dockerfile
```

-	Layers:
	-	`sha256:2cdf29fa10b8b767dd265a5a21f06a7f0e6889e34d17781ba392b5c5f65ded9c`  
		Last Modified: Thu, 13 Jun 2024 18:28:30 GMT  
		Size: 4.6 MB (4570029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fedddbe8895a149fd54e0a9c9cf1263426f76bdd6f5e05f8dea68b2f58ce79fb`  
		Last Modified: Thu, 13 Jun 2024 18:28:30 GMT  
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
$ docker pull influxdb@sha256:db6468154a5c2fbbe34ffb0d38efd7c9a870a56003588cf12dc1fbc58b90a481
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:4f37acb24d052ce198eb7ce1083813abb22f01f8202f5bf081faee440c166dea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83635750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af0fda022b38aaa46a320dfa0af6faee7bd9ac263a9a5fc7907da77713ae8be6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:d2a2ac890c4f902560feaadaac9f36a9b844131c97453ecb90241cf525185196 in / 
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
	-	`sha256:29f873e2e3f8f1b35ae4bee023807e71b6e16e714dbd1cbd19b3124c62e7634c`  
		Last Modified: Thu, 13 Jun 2024 01:25:49 GMT  
		Size: 55.1 MB (55099190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e1ed81430e2556f97ec363517655fd54e04e4f6b0eaa55faa9aa88490e96d9`  
		Last Modified: Thu, 13 Jun 2024 03:50:28 GMT  
		Size: 15.8 MB (15764834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf12e4de679c91ac55b036333ae3df3c7b12b4f8ea0e201a196ca9e54cb76960`  
		Last Modified: Thu, 13 Jun 2024 18:28:28 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05220e020dc05e32599ac940029afb2a536d1a29bc762235ed55e7d974815233`  
		Last Modified: Thu, 13 Jun 2024 18:28:28 GMT  
		Size: 12.8 MB (12769376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7f6c7c8ff780009697525b169a7e4c675c5eb2cc162aeee8a908c38612871a`  
		Last Modified: Thu, 13 Jun 2024 18:28:28 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a750c2dafce9732d56e9a48237d3d4617e45cba04f79038a6160d5e4091f6d66`  
		Last Modified: Thu, 13 Jun 2024 18:28:28 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:ae3fba0e0e6878bcb4371cbfa38d73b9d1ac3647f8487ae54144c9c96e4ab662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4529045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e8adfb69fa1f01e89c76919176b0e1fe11f6f33d09b23f0dcfc17f7bffe67a`

```dockerfile
```

-	Layers:
	-	`sha256:c6c3c908bd9f48dd21ccec96bb5e6f68bd23332a49302c0aa74f59d5752293c4`  
		Last Modified: Thu, 13 Jun 2024 18:28:28 GMT  
		Size: 4.5 MB (4516158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94daa159ccd76def86bce20750751f925b5eb1d7cf745fde1a6b22ff21f51384`  
		Last Modified: Thu, 13 Jun 2024 18:28:28 GMT  
		Size: 12.9 KB (12887 bytes)  
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
$ docker pull influxdb@sha256:86ab0b6fb1399dba796baae8053bb25d6d25a05abe290e9653c0db9c7c78b005
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9.13-data` - linux; amd64

```console
$ docker pull influxdb@sha256:700982e519ea56c8e1939a5165762a25ccff1ae1eeb8ffcd7a6e3279235cd2ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 MB (104156541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e60bc6b4ddab6bc9a44ff13c4be3c4b36ac9c9ff88b207d4becede1010bfb7f9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:d2a2ac890c4f902560feaadaac9f36a9b844131c97453ecb90241cf525185196 in / 
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
	-	`sha256:29f873e2e3f8f1b35ae4bee023807e71b6e16e714dbd1cbd19b3124c62e7634c`  
		Last Modified: Thu, 13 Jun 2024 01:25:49 GMT  
		Size: 55.1 MB (55099190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e1ed81430e2556f97ec363517655fd54e04e4f6b0eaa55faa9aa88490e96d9`  
		Last Modified: Thu, 13 Jun 2024 03:50:28 GMT  
		Size: 15.8 MB (15764834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4dcc94a6f1fa678d46b0ab818eb0d724838181ccdcd4dcefc6913f747fc905b`  
		Last Modified: Thu, 13 Jun 2024 18:28:30 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957594b16e0b0064114b23dc1892010a4dc90c0baa98a705648fd577048b7ff9`  
		Last Modified: Thu, 13 Jun 2024 18:28:31 GMT  
		Size: 33.3 MB (33288959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef58e8a1f016a39de2d8492b12dad5a839739ebd4cb0848658937b8c74c256b4`  
		Last Modified: Thu, 13 Jun 2024 18:28:30 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6564b87df9d45ec2f4296c078d8ef71d21b0b481ae66bc5a19783f5adeb3ff`  
		Last Modified: Thu, 13 Jun 2024 18:28:30 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacf028904564dbe0b651cd88b8b37e130c26de6c11d4fdba9ecb9bf29fcef7c`  
		Last Modified: Thu, 13 Jun 2024 18:28:31 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9.13-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:74c0ca665848d5667a5c68800b848cbf6d9d4cfdbc510f3954a7a1883555d930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4584570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc0f1357d42478766f9631ff434bae81f20feebf611c7c38d2b2781fa2c2d4a`

```dockerfile
```

-	Layers:
	-	`sha256:2cdf29fa10b8b767dd265a5a21f06a7f0e6889e34d17781ba392b5c5f65ded9c`  
		Last Modified: Thu, 13 Jun 2024 18:28:30 GMT  
		Size: 4.6 MB (4570029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fedddbe8895a149fd54e0a9c9cf1263426f76bdd6f5e05f8dea68b2f58ce79fb`  
		Last Modified: Thu, 13 Jun 2024 18:28:30 GMT  
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
$ docker pull influxdb@sha256:db6468154a5c2fbbe34ffb0d38efd7c9a870a56003588cf12dc1fbc58b90a481
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9.13-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:4f37acb24d052ce198eb7ce1083813abb22f01f8202f5bf081faee440c166dea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83635750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af0fda022b38aaa46a320dfa0af6faee7bd9ac263a9a5fc7907da77713ae8be6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:d2a2ac890c4f902560feaadaac9f36a9b844131c97453ecb90241cf525185196 in / 
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
	-	`sha256:29f873e2e3f8f1b35ae4bee023807e71b6e16e714dbd1cbd19b3124c62e7634c`  
		Last Modified: Thu, 13 Jun 2024 01:25:49 GMT  
		Size: 55.1 MB (55099190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e1ed81430e2556f97ec363517655fd54e04e4f6b0eaa55faa9aa88490e96d9`  
		Last Modified: Thu, 13 Jun 2024 03:50:28 GMT  
		Size: 15.8 MB (15764834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf12e4de679c91ac55b036333ae3df3c7b12b4f8ea0e201a196ca9e54cb76960`  
		Last Modified: Thu, 13 Jun 2024 18:28:28 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05220e020dc05e32599ac940029afb2a536d1a29bc762235ed55e7d974815233`  
		Last Modified: Thu, 13 Jun 2024 18:28:28 GMT  
		Size: 12.8 MB (12769376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7f6c7c8ff780009697525b169a7e4c675c5eb2cc162aeee8a908c38612871a`  
		Last Modified: Thu, 13 Jun 2024 18:28:28 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a750c2dafce9732d56e9a48237d3d4617e45cba04f79038a6160d5e4091f6d66`  
		Last Modified: Thu, 13 Jun 2024 18:28:28 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9.13-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:ae3fba0e0e6878bcb4371cbfa38d73b9d1ac3647f8487ae54144c9c96e4ab662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4529045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e8adfb69fa1f01e89c76919176b0e1fe11f6f33d09b23f0dcfc17f7bffe67a`

```dockerfile
```

-	Layers:
	-	`sha256:c6c3c908bd9f48dd21ccec96bb5e6f68bd23332a49302c0aa74f59d5752293c4`  
		Last Modified: Thu, 13 Jun 2024 18:28:28 GMT  
		Size: 4.5 MB (4516158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94daa159ccd76def86bce20750751f925b5eb1d7cf745fde1a6b22ff21f51384`  
		Last Modified: Thu, 13 Jun 2024 18:28:28 GMT  
		Size: 12.9 KB (12887 bytes)  
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
$ docker pull influxdb@sha256:13579a335363aa9721985087af25afcaf71fbb566dd0d758078f27e0ad9057a0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2` - linux; amd64

```console
$ docker pull influxdb@sha256:320b09dd9fdf88d3e5e279b1117f854c7680d62489a442ff6a19ce56f6555972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (163963594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a087752ab8a7ad3b11ce82767c68fe6ce8046ff3d5e3cf276889384715aed8e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
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
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de8170e6c8b5b3ea069bc5fc36a8cd2a73786660643fd6f6d86dd017355cffc`  
		Last Modified: Thu, 13 Jun 2024 18:28:52 GMT  
		Size: 9.6 MB (9592091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7975cebe753fece4b01d83191733754cc672e30a5ab432e947ed06be8d34bc5`  
		Last Modified: Thu, 13 Jun 2024 18:28:52 GMT  
		Size: 5.8 MB (5820923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44a7d512a02b1ad2aeaf4f331f37237a0c688ce3bf238ed32626a3385c8a659`  
		Last Modified: Thu, 13 Jun 2024 18:28:52 GMT  
		Size: 3.2 KB (3230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323fd3a42118e489eb04f0cb4e66140e9b77738c5d09169009e2e37ca63ff5f8`  
		Last Modified: Thu, 13 Jun 2024 18:28:52 GMT  
		Size: 1.0 MB (1006371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8258065e79d1ce73e35fd7b1e72ae73037cb757ed6be1e69847e3bc5745de2df`  
		Last Modified: Thu, 13 Jun 2024 18:28:54 GMT  
		Size: 95.3 MB (95255503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a65d57478ce8fc72fc34a67910e1e50c64693e72c564b31e7a821c9d18acd6`  
		Last Modified: Thu, 13 Jun 2024 18:28:53 GMT  
		Size: 23.1 MB (23128319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b394fbb7bd6706dc09b4b01478313c007b0d5e05fc639d1badb052f5b0183194`  
		Last Modified: Thu, 13 Jun 2024 18:28:53 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc27e810bf29cf774ea3693f137c338f48a55fcd9b0b4fea5e1d2caf58e236bf`  
		Last Modified: Thu, 13 Jun 2024 18:28:53 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d5888dc1284a2aa4bce210dbf8af2e970f75ccd7c973e418acbb28515c1b98`  
		Last Modified: Thu, 13 Jun 2024 18:28:54 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:20424bf712d71c63b9f7544a480fdd2a517e38857ea60b4a6670e57df14df869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2788702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f234781a8ff2d1edf9144f0b45a9c506f5b1673984c7a04c61eaddf56677ba`

```dockerfile
```

-	Layers:
	-	`sha256:d12f468f75c562ece4a7df52ba540696d1bdb860670d38bb74613e32d0cd12d5`  
		Last Modified: Thu, 13 Jun 2024 18:28:52 GMT  
		Size: 2.8 MB (2755162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:081106b445bdecce52ce39df7f878ccbec04062065d2a592f85046859107c9a8`  
		Last Modified: Thu, 13 Jun 2024 18:28:52 GMT  
		Size: 33.5 KB (33540 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:d9ccf4d36f36102c1a38d7f385c4b33a14cc69ba4f3c64af0d3f542289e98dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 MB (158094169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f54ea7920d13b97b3ecf7f351e9cc4361e0147736f2ffb8b2e5a00420355e4ac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
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
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce1ea3b6373448936e739ee0f0ebf73ae303d4231eb55cae9758d1a3cf05951`  
		Last Modified: Thu, 13 Jun 2024 19:06:31 GMT  
		Size: 9.4 MB (9388817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645a0c4887383b15b407aefefafee7aa3f7d365458d3b6a596f2b61bd6da0db4`  
		Last Modified: Thu, 13 Jun 2024 19:06:31 GMT  
		Size: 5.5 MB (5463787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94cf59e453e7b5c98871fbf3cd2d0223f337134760424ba431e324474daff757`  
		Last Modified: Thu, 13 Jun 2024 19:06:30 GMT  
		Size: 3.2 KB (3228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05aa93a5d874d074948e80d205b4e508c417624943bb88e2e35fb65f92fd90b4`  
		Last Modified: Thu, 13 Jun 2024 19:06:31 GMT  
		Size: 936.1 KB (936106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9bec4fc4e59e2023689d18549ae2ef013ff5dab335528a5f48b698684b96bd`  
		Last Modified: Thu, 13 Jun 2024 19:06:35 GMT  
		Size: 91.5 MB (91453318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef1efac592486882b6e74f4f28ce817ef11ec79b5f5b77adbb8fbfad52489e7`  
		Last Modified: Thu, 13 Jun 2024 19:06:33 GMT  
		Size: 21.7 MB (21662521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b72ce02738a13a6b5efb59a8a98b3755bf73f55c2147fa3f43edfdcfd6c5b3`  
		Last Modified: Thu, 13 Jun 2024 19:06:32 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9cc8a55c0ea84af9576af5a680bc47bae003061c547f72548f711d1a1426471`  
		Last Modified: Thu, 13 Jun 2024 19:06:32 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4e70be6e23adc337e9ce6111f51ec49d07c0b7014c49918e347457e998cd6c`  
		Last Modified: Thu, 13 Jun 2024 19:06:33 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:1cad6a2c3e6e18cf7dede6ddfa98559a36133aab9a40a04084d2ca6d2c182f78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2788385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e6c7da3f669d816be0bb1c6c8ae4c83b0d9d32b619216330fbb1b1f4c38af5`

```dockerfile
```

-	Layers:
	-	`sha256:3ffff0605b518572f1ad5dd2a1b9da5eb66d86cbeaf8b8bd19f7fff86c74f02f`  
		Last Modified: Thu, 13 Jun 2024 19:06:31 GMT  
		Size: 2.8 MB (2754542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5414cc3be457867e9ab93f1555fce2d2a1971d42bb48c5846e7cdf1e1149907`  
		Last Modified: Thu, 13 Jun 2024 19:06:30 GMT  
		Size: 33.8 KB (33843 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2-alpine`

```console
$ docker pull influxdb@sha256:8190c63f7892b7377e8f9ecf6057a766f242614ef8603d4b6a84ba2844f4b35e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:8fb72e9b1dd5df2d2ecb8201c3dac3d85fb4c0d217187b72ba5c290b4f941279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89833441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d489cf7c69589a3bedfde0adf613af40abc5c50bd65b85ede0de8a3b1ee53580`
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78233a51c37b63a5d0dfb3f19da2586c9fa861b54e0bbf1b70a80875cadced1f`  
		Last Modified: Thu, 20 Jun 2024 20:56:06 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28110b5bbbeab324abf5501db842f1dd0df6a19d379e92e2c42129c9c5e33a62`  
		Last Modified: Thu, 20 Jun 2024 20:56:06 GMT  
		Size: 9.6 MB (9630577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2c38391b43cf30fc9494bfd7310fe25d02e2e2aad0e6bbd3a6a31a7c5732eb`  
		Last Modified: Thu, 20 Jun 2024 20:56:06 GMT  
		Size: 5.8 MB (5820949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ed1d717a25ee5fa59dd9e2b100b9c78b33de4bf8ca7d7d39093ce59626db21`  
		Last Modified: Thu, 20 Jun 2024 20:56:06 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55011f35b7dce11140b1343d9973f66e6cec2cac89f82766dc8f715eaceba84`  
		Last Modified: Thu, 20 Jun 2024 20:56:07 GMT  
		Size: 47.6 MB (47621802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c907588fe177b5f2b5b48a0bddae0407e281ccd24ba410096a8230ad70e19cb4`  
		Last Modified: Thu, 20 Jun 2024 20:56:07 GMT  
		Size: 23.1 MB (23128304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d9303dc18ddb862d68ecfcf31b63e0fe84a004741980c5f40b2fdf8f4be39e`  
		Last Modified: Thu, 20 Jun 2024 20:56:07 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3aad3cb080baac2e2da3a4257353e8b81e841f4b6bf7ac26523da6c53bcec1`  
		Last Modified: Thu, 20 Jun 2024 20:56:07 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19689c0021345c8f777d5d28db1668d598acbd646cc6e8c3ad36b4e027bd1ad`  
		Last Modified: Thu, 20 Jun 2024 20:56:08 GMT  
		Size: 6.3 KB (6281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:eada47181c572dd69f1ff41ec2fcd0244a5d591d999967c523496979ca7f1c80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **887.1 KB (887126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e908161ef6f1ea7600cbab8224d15602ea617dec76211ced2613c8f3c1b71644`

```dockerfile
```

-	Layers:
	-	`sha256:e00f50a1837979e2f81dee93e8b402b0041824e1772e44d526a1d6097fe2518f`  
		Last Modified: Thu, 20 Jun 2024 20:56:06 GMT  
		Size: 856.4 KB (856380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb977e34a5a17908ac79ef59d798fd7cc4639a728471e38b928fb3d49cd45694`  
		Last Modified: Thu, 20 Jun 2024 20:56:06 GMT  
		Size: 30.7 KB (30746 bytes)  
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
$ docker pull influxdb@sha256:13579a335363aa9721985087af25afcaf71fbb566dd0d758078f27e0ad9057a0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7` - linux; amd64

```console
$ docker pull influxdb@sha256:320b09dd9fdf88d3e5e279b1117f854c7680d62489a442ff6a19ce56f6555972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (163963594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a087752ab8a7ad3b11ce82767c68fe6ce8046ff3d5e3cf276889384715aed8e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
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
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de8170e6c8b5b3ea069bc5fc36a8cd2a73786660643fd6f6d86dd017355cffc`  
		Last Modified: Thu, 13 Jun 2024 18:28:52 GMT  
		Size: 9.6 MB (9592091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7975cebe753fece4b01d83191733754cc672e30a5ab432e947ed06be8d34bc5`  
		Last Modified: Thu, 13 Jun 2024 18:28:52 GMT  
		Size: 5.8 MB (5820923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44a7d512a02b1ad2aeaf4f331f37237a0c688ce3bf238ed32626a3385c8a659`  
		Last Modified: Thu, 13 Jun 2024 18:28:52 GMT  
		Size: 3.2 KB (3230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323fd3a42118e489eb04f0cb4e66140e9b77738c5d09169009e2e37ca63ff5f8`  
		Last Modified: Thu, 13 Jun 2024 18:28:52 GMT  
		Size: 1.0 MB (1006371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8258065e79d1ce73e35fd7b1e72ae73037cb757ed6be1e69847e3bc5745de2df`  
		Last Modified: Thu, 13 Jun 2024 18:28:54 GMT  
		Size: 95.3 MB (95255503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a65d57478ce8fc72fc34a67910e1e50c64693e72c564b31e7a821c9d18acd6`  
		Last Modified: Thu, 13 Jun 2024 18:28:53 GMT  
		Size: 23.1 MB (23128319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b394fbb7bd6706dc09b4b01478313c007b0d5e05fc639d1badb052f5b0183194`  
		Last Modified: Thu, 13 Jun 2024 18:28:53 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc27e810bf29cf774ea3693f137c338f48a55fcd9b0b4fea5e1d2caf58e236bf`  
		Last Modified: Thu, 13 Jun 2024 18:28:53 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d5888dc1284a2aa4bce210dbf8af2e970f75ccd7c973e418acbb28515c1b98`  
		Last Modified: Thu, 13 Jun 2024 18:28:54 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:20424bf712d71c63b9f7544a480fdd2a517e38857ea60b4a6670e57df14df869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2788702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f234781a8ff2d1edf9144f0b45a9c506f5b1673984c7a04c61eaddf56677ba`

```dockerfile
```

-	Layers:
	-	`sha256:d12f468f75c562ece4a7df52ba540696d1bdb860670d38bb74613e32d0cd12d5`  
		Last Modified: Thu, 13 Jun 2024 18:28:52 GMT  
		Size: 2.8 MB (2755162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:081106b445bdecce52ce39df7f878ccbec04062065d2a592f85046859107c9a8`  
		Last Modified: Thu, 13 Jun 2024 18:28:52 GMT  
		Size: 33.5 KB (33540 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:d9ccf4d36f36102c1a38d7f385c4b33a14cc69ba4f3c64af0d3f542289e98dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 MB (158094169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f54ea7920d13b97b3ecf7f351e9cc4361e0147736f2ffb8b2e5a00420355e4ac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
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
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce1ea3b6373448936e739ee0f0ebf73ae303d4231eb55cae9758d1a3cf05951`  
		Last Modified: Thu, 13 Jun 2024 19:06:31 GMT  
		Size: 9.4 MB (9388817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645a0c4887383b15b407aefefafee7aa3f7d365458d3b6a596f2b61bd6da0db4`  
		Last Modified: Thu, 13 Jun 2024 19:06:31 GMT  
		Size: 5.5 MB (5463787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94cf59e453e7b5c98871fbf3cd2d0223f337134760424ba431e324474daff757`  
		Last Modified: Thu, 13 Jun 2024 19:06:30 GMT  
		Size: 3.2 KB (3228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05aa93a5d874d074948e80d205b4e508c417624943bb88e2e35fb65f92fd90b4`  
		Last Modified: Thu, 13 Jun 2024 19:06:31 GMT  
		Size: 936.1 KB (936106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9bec4fc4e59e2023689d18549ae2ef013ff5dab335528a5f48b698684b96bd`  
		Last Modified: Thu, 13 Jun 2024 19:06:35 GMT  
		Size: 91.5 MB (91453318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef1efac592486882b6e74f4f28ce817ef11ec79b5f5b77adbb8fbfad52489e7`  
		Last Modified: Thu, 13 Jun 2024 19:06:33 GMT  
		Size: 21.7 MB (21662521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b72ce02738a13a6b5efb59a8a98b3755bf73f55c2147fa3f43edfdcfd6c5b3`  
		Last Modified: Thu, 13 Jun 2024 19:06:32 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9cc8a55c0ea84af9576af5a680bc47bae003061c547f72548f711d1a1426471`  
		Last Modified: Thu, 13 Jun 2024 19:06:32 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4e70be6e23adc337e9ce6111f51ec49d07c0b7014c49918e347457e998cd6c`  
		Last Modified: Thu, 13 Jun 2024 19:06:33 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:1cad6a2c3e6e18cf7dede6ddfa98559a36133aab9a40a04084d2ca6d2c182f78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2788385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e6c7da3f669d816be0bb1c6c8ae4c83b0d9d32b619216330fbb1b1f4c38af5`

```dockerfile
```

-	Layers:
	-	`sha256:3ffff0605b518572f1ad5dd2a1b9da5eb66d86cbeaf8b8bd19f7fff86c74f02f`  
		Last Modified: Thu, 13 Jun 2024 19:06:31 GMT  
		Size: 2.8 MB (2754542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5414cc3be457867e9ab93f1555fce2d2a1971d42bb48c5846e7cdf1e1149907`  
		Last Modified: Thu, 13 Jun 2024 19:06:30 GMT  
		Size: 33.8 KB (33843 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7-alpine`

```console
$ docker pull influxdb@sha256:8190c63f7892b7377e8f9ecf6057a766f242614ef8603d4b6a84ba2844f4b35e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:8fb72e9b1dd5df2d2ecb8201c3dac3d85fb4c0d217187b72ba5c290b4f941279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89833441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d489cf7c69589a3bedfde0adf613af40abc5c50bd65b85ede0de8a3b1ee53580`
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78233a51c37b63a5d0dfb3f19da2586c9fa861b54e0bbf1b70a80875cadced1f`  
		Last Modified: Thu, 20 Jun 2024 20:56:06 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28110b5bbbeab324abf5501db842f1dd0df6a19d379e92e2c42129c9c5e33a62`  
		Last Modified: Thu, 20 Jun 2024 20:56:06 GMT  
		Size: 9.6 MB (9630577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2c38391b43cf30fc9494bfd7310fe25d02e2e2aad0e6bbd3a6a31a7c5732eb`  
		Last Modified: Thu, 20 Jun 2024 20:56:06 GMT  
		Size: 5.8 MB (5820949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ed1d717a25ee5fa59dd9e2b100b9c78b33de4bf8ca7d7d39093ce59626db21`  
		Last Modified: Thu, 20 Jun 2024 20:56:06 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55011f35b7dce11140b1343d9973f66e6cec2cac89f82766dc8f715eaceba84`  
		Last Modified: Thu, 20 Jun 2024 20:56:07 GMT  
		Size: 47.6 MB (47621802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c907588fe177b5f2b5b48a0bddae0407e281ccd24ba410096a8230ad70e19cb4`  
		Last Modified: Thu, 20 Jun 2024 20:56:07 GMT  
		Size: 23.1 MB (23128304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d9303dc18ddb862d68ecfcf31b63e0fe84a004741980c5f40b2fdf8f4be39e`  
		Last Modified: Thu, 20 Jun 2024 20:56:07 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3aad3cb080baac2e2da3a4257353e8b81e841f4b6bf7ac26523da6c53bcec1`  
		Last Modified: Thu, 20 Jun 2024 20:56:07 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19689c0021345c8f777d5d28db1668d598acbd646cc6e8c3ad36b4e027bd1ad`  
		Last Modified: Thu, 20 Jun 2024 20:56:08 GMT  
		Size: 6.3 KB (6281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:eada47181c572dd69f1ff41ec2fcd0244a5d591d999967c523496979ca7f1c80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **887.1 KB (887126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e908161ef6f1ea7600cbab8224d15602ea617dec76211ced2613c8f3c1b71644`

```dockerfile
```

-	Layers:
	-	`sha256:e00f50a1837979e2f81dee93e8b402b0041824e1772e44d526a1d6097fe2518f`  
		Last Modified: Thu, 20 Jun 2024 20:56:06 GMT  
		Size: 856.4 KB (856380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb977e34a5a17908ac79ef59d798fd7cc4639a728471e38b928fb3d49cd45694`  
		Last Modified: Thu, 20 Jun 2024 20:56:06 GMT  
		Size: 30.7 KB (30746 bytes)  
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

## `influxdb:2.7.6`

```console
$ docker pull influxdb@sha256:13579a335363aa9721985087af25afcaf71fbb566dd0d758078f27e0ad9057a0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7.6` - linux; amd64

```console
$ docker pull influxdb@sha256:320b09dd9fdf88d3e5e279b1117f854c7680d62489a442ff6a19ce56f6555972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (163963594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a087752ab8a7ad3b11ce82767c68fe6ce8046ff3d5e3cf276889384715aed8e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
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
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de8170e6c8b5b3ea069bc5fc36a8cd2a73786660643fd6f6d86dd017355cffc`  
		Last Modified: Thu, 13 Jun 2024 18:28:52 GMT  
		Size: 9.6 MB (9592091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7975cebe753fece4b01d83191733754cc672e30a5ab432e947ed06be8d34bc5`  
		Last Modified: Thu, 13 Jun 2024 18:28:52 GMT  
		Size: 5.8 MB (5820923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44a7d512a02b1ad2aeaf4f331f37237a0c688ce3bf238ed32626a3385c8a659`  
		Last Modified: Thu, 13 Jun 2024 18:28:52 GMT  
		Size: 3.2 KB (3230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323fd3a42118e489eb04f0cb4e66140e9b77738c5d09169009e2e37ca63ff5f8`  
		Last Modified: Thu, 13 Jun 2024 18:28:52 GMT  
		Size: 1.0 MB (1006371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8258065e79d1ce73e35fd7b1e72ae73037cb757ed6be1e69847e3bc5745de2df`  
		Last Modified: Thu, 13 Jun 2024 18:28:54 GMT  
		Size: 95.3 MB (95255503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a65d57478ce8fc72fc34a67910e1e50c64693e72c564b31e7a821c9d18acd6`  
		Last Modified: Thu, 13 Jun 2024 18:28:53 GMT  
		Size: 23.1 MB (23128319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b394fbb7bd6706dc09b4b01478313c007b0d5e05fc639d1badb052f5b0183194`  
		Last Modified: Thu, 13 Jun 2024 18:28:53 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc27e810bf29cf774ea3693f137c338f48a55fcd9b0b4fea5e1d2caf58e236bf`  
		Last Modified: Thu, 13 Jun 2024 18:28:53 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d5888dc1284a2aa4bce210dbf8af2e970f75ccd7c973e418acbb28515c1b98`  
		Last Modified: Thu, 13 Jun 2024 18:28:54 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.6` - unknown; unknown

```console
$ docker pull influxdb@sha256:20424bf712d71c63b9f7544a480fdd2a517e38857ea60b4a6670e57df14df869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2788702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f234781a8ff2d1edf9144f0b45a9c506f5b1673984c7a04c61eaddf56677ba`

```dockerfile
```

-	Layers:
	-	`sha256:d12f468f75c562ece4a7df52ba540696d1bdb860670d38bb74613e32d0cd12d5`  
		Last Modified: Thu, 13 Jun 2024 18:28:52 GMT  
		Size: 2.8 MB (2755162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:081106b445bdecce52ce39df7f878ccbec04062065d2a592f85046859107c9a8`  
		Last Modified: Thu, 13 Jun 2024 18:28:52 GMT  
		Size: 33.5 KB (33540 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7.6` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:d9ccf4d36f36102c1a38d7f385c4b33a14cc69ba4f3c64af0d3f542289e98dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 MB (158094169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f54ea7920d13b97b3ecf7f351e9cc4361e0147736f2ffb8b2e5a00420355e4ac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
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
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce1ea3b6373448936e739ee0f0ebf73ae303d4231eb55cae9758d1a3cf05951`  
		Last Modified: Thu, 13 Jun 2024 19:06:31 GMT  
		Size: 9.4 MB (9388817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645a0c4887383b15b407aefefafee7aa3f7d365458d3b6a596f2b61bd6da0db4`  
		Last Modified: Thu, 13 Jun 2024 19:06:31 GMT  
		Size: 5.5 MB (5463787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94cf59e453e7b5c98871fbf3cd2d0223f337134760424ba431e324474daff757`  
		Last Modified: Thu, 13 Jun 2024 19:06:30 GMT  
		Size: 3.2 KB (3228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05aa93a5d874d074948e80d205b4e508c417624943bb88e2e35fb65f92fd90b4`  
		Last Modified: Thu, 13 Jun 2024 19:06:31 GMT  
		Size: 936.1 KB (936106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9bec4fc4e59e2023689d18549ae2ef013ff5dab335528a5f48b698684b96bd`  
		Last Modified: Thu, 13 Jun 2024 19:06:35 GMT  
		Size: 91.5 MB (91453318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef1efac592486882b6e74f4f28ce817ef11ec79b5f5b77adbb8fbfad52489e7`  
		Last Modified: Thu, 13 Jun 2024 19:06:33 GMT  
		Size: 21.7 MB (21662521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b72ce02738a13a6b5efb59a8a98b3755bf73f55c2147fa3f43edfdcfd6c5b3`  
		Last Modified: Thu, 13 Jun 2024 19:06:32 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9cc8a55c0ea84af9576af5a680bc47bae003061c547f72548f711d1a1426471`  
		Last Modified: Thu, 13 Jun 2024 19:06:32 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4e70be6e23adc337e9ce6111f51ec49d07c0b7014c49918e347457e998cd6c`  
		Last Modified: Thu, 13 Jun 2024 19:06:33 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.6` - unknown; unknown

```console
$ docker pull influxdb@sha256:1cad6a2c3e6e18cf7dede6ddfa98559a36133aab9a40a04084d2ca6d2c182f78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2788385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e6c7da3f669d816be0bb1c6c8ae4c83b0d9d32b619216330fbb1b1f4c38af5`

```dockerfile
```

-	Layers:
	-	`sha256:3ffff0605b518572f1ad5dd2a1b9da5eb66d86cbeaf8b8bd19f7fff86c74f02f`  
		Last Modified: Thu, 13 Jun 2024 19:06:31 GMT  
		Size: 2.8 MB (2754542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5414cc3be457867e9ab93f1555fce2d2a1971d42bb48c5846e7cdf1e1149907`  
		Last Modified: Thu, 13 Jun 2024 19:06:30 GMT  
		Size: 33.8 KB (33843 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7.6-alpine`

```console
$ docker pull influxdb@sha256:8190c63f7892b7377e8f9ecf6057a766f242614ef8603d4b6a84ba2844f4b35e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7.6-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:8fb72e9b1dd5df2d2ecb8201c3dac3d85fb4c0d217187b72ba5c290b4f941279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89833441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d489cf7c69589a3bedfde0adf613af40abc5c50bd65b85ede0de8a3b1ee53580`
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78233a51c37b63a5d0dfb3f19da2586c9fa861b54e0bbf1b70a80875cadced1f`  
		Last Modified: Thu, 20 Jun 2024 20:56:06 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28110b5bbbeab324abf5501db842f1dd0df6a19d379e92e2c42129c9c5e33a62`  
		Last Modified: Thu, 20 Jun 2024 20:56:06 GMT  
		Size: 9.6 MB (9630577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2c38391b43cf30fc9494bfd7310fe25d02e2e2aad0e6bbd3a6a31a7c5732eb`  
		Last Modified: Thu, 20 Jun 2024 20:56:06 GMT  
		Size: 5.8 MB (5820949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ed1d717a25ee5fa59dd9e2b100b9c78b33de4bf8ca7d7d39093ce59626db21`  
		Last Modified: Thu, 20 Jun 2024 20:56:06 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55011f35b7dce11140b1343d9973f66e6cec2cac89f82766dc8f715eaceba84`  
		Last Modified: Thu, 20 Jun 2024 20:56:07 GMT  
		Size: 47.6 MB (47621802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c907588fe177b5f2b5b48a0bddae0407e281ccd24ba410096a8230ad70e19cb4`  
		Last Modified: Thu, 20 Jun 2024 20:56:07 GMT  
		Size: 23.1 MB (23128304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d9303dc18ddb862d68ecfcf31b63e0fe84a004741980c5f40b2fdf8f4be39e`  
		Last Modified: Thu, 20 Jun 2024 20:56:07 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3aad3cb080baac2e2da3a4257353e8b81e841f4b6bf7ac26523da6c53bcec1`  
		Last Modified: Thu, 20 Jun 2024 20:56:07 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19689c0021345c8f777d5d28db1668d598acbd646cc6e8c3ad36b4e027bd1ad`  
		Last Modified: Thu, 20 Jun 2024 20:56:08 GMT  
		Size: 6.3 KB (6281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.6-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:eada47181c572dd69f1ff41ec2fcd0244a5d591d999967c523496979ca7f1c80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **887.1 KB (887126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e908161ef6f1ea7600cbab8224d15602ea617dec76211ced2613c8f3c1b71644`

```dockerfile
```

-	Layers:
	-	`sha256:e00f50a1837979e2f81dee93e8b402b0041824e1772e44d526a1d6097fe2518f`  
		Last Modified: Thu, 20 Jun 2024 20:56:06 GMT  
		Size: 856.4 KB (856380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb977e34a5a17908ac79ef59d798fd7cc4639a728471e38b928fb3d49cd45694`  
		Last Modified: Thu, 20 Jun 2024 20:56:06 GMT  
		Size: 30.7 KB (30746 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7.6-alpine` - linux; arm64 variant v8

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

### `influxdb:2.7.6-alpine` - unknown; unknown

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

## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:8190c63f7892b7377e8f9ecf6057a766f242614ef8603d4b6a84ba2844f4b35e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:8fb72e9b1dd5df2d2ecb8201c3dac3d85fb4c0d217187b72ba5c290b4f941279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89833441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d489cf7c69589a3bedfde0adf613af40abc5c50bd65b85ede0de8a3b1ee53580`
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78233a51c37b63a5d0dfb3f19da2586c9fa861b54e0bbf1b70a80875cadced1f`  
		Last Modified: Thu, 20 Jun 2024 20:56:06 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28110b5bbbeab324abf5501db842f1dd0df6a19d379e92e2c42129c9c5e33a62`  
		Last Modified: Thu, 20 Jun 2024 20:56:06 GMT  
		Size: 9.6 MB (9630577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2c38391b43cf30fc9494bfd7310fe25d02e2e2aad0e6bbd3a6a31a7c5732eb`  
		Last Modified: Thu, 20 Jun 2024 20:56:06 GMT  
		Size: 5.8 MB (5820949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ed1d717a25ee5fa59dd9e2b100b9c78b33de4bf8ca7d7d39093ce59626db21`  
		Last Modified: Thu, 20 Jun 2024 20:56:06 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55011f35b7dce11140b1343d9973f66e6cec2cac89f82766dc8f715eaceba84`  
		Last Modified: Thu, 20 Jun 2024 20:56:07 GMT  
		Size: 47.6 MB (47621802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c907588fe177b5f2b5b48a0bddae0407e281ccd24ba410096a8230ad70e19cb4`  
		Last Modified: Thu, 20 Jun 2024 20:56:07 GMT  
		Size: 23.1 MB (23128304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d9303dc18ddb862d68ecfcf31b63e0fe84a004741980c5f40b2fdf8f4be39e`  
		Last Modified: Thu, 20 Jun 2024 20:56:07 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3aad3cb080baac2e2da3a4257353e8b81e841f4b6bf7ac26523da6c53bcec1`  
		Last Modified: Thu, 20 Jun 2024 20:56:07 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19689c0021345c8f777d5d28db1668d598acbd646cc6e8c3ad36b4e027bd1ad`  
		Last Modified: Thu, 20 Jun 2024 20:56:08 GMT  
		Size: 6.3 KB (6281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:eada47181c572dd69f1ff41ec2fcd0244a5d591d999967c523496979ca7f1c80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **887.1 KB (887126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e908161ef6f1ea7600cbab8224d15602ea617dec76211ced2613c8f3c1b71644`

```dockerfile
```

-	Layers:
	-	`sha256:e00f50a1837979e2f81dee93e8b402b0041824e1772e44d526a1d6097fe2518f`  
		Last Modified: Thu, 20 Jun 2024 20:56:06 GMT  
		Size: 856.4 KB (856380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb977e34a5a17908ac79ef59d798fd7cc4639a728471e38b928fb3d49cd45694`  
		Last Modified: Thu, 20 Jun 2024 20:56:06 GMT  
		Size: 30.7 KB (30746 bytes)  
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
$ docker pull influxdb@sha256:13579a335363aa9721985087af25afcaf71fbb566dd0d758078f27e0ad9057a0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:320b09dd9fdf88d3e5e279b1117f854c7680d62489a442ff6a19ce56f6555972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (163963594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a087752ab8a7ad3b11ce82767c68fe6ce8046ff3d5e3cf276889384715aed8e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
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
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de8170e6c8b5b3ea069bc5fc36a8cd2a73786660643fd6f6d86dd017355cffc`  
		Last Modified: Thu, 13 Jun 2024 18:28:52 GMT  
		Size: 9.6 MB (9592091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7975cebe753fece4b01d83191733754cc672e30a5ab432e947ed06be8d34bc5`  
		Last Modified: Thu, 13 Jun 2024 18:28:52 GMT  
		Size: 5.8 MB (5820923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44a7d512a02b1ad2aeaf4f331f37237a0c688ce3bf238ed32626a3385c8a659`  
		Last Modified: Thu, 13 Jun 2024 18:28:52 GMT  
		Size: 3.2 KB (3230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323fd3a42118e489eb04f0cb4e66140e9b77738c5d09169009e2e37ca63ff5f8`  
		Last Modified: Thu, 13 Jun 2024 18:28:52 GMT  
		Size: 1.0 MB (1006371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8258065e79d1ce73e35fd7b1e72ae73037cb757ed6be1e69847e3bc5745de2df`  
		Last Modified: Thu, 13 Jun 2024 18:28:54 GMT  
		Size: 95.3 MB (95255503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a65d57478ce8fc72fc34a67910e1e50c64693e72c564b31e7a821c9d18acd6`  
		Last Modified: Thu, 13 Jun 2024 18:28:53 GMT  
		Size: 23.1 MB (23128319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b394fbb7bd6706dc09b4b01478313c007b0d5e05fc639d1badb052f5b0183194`  
		Last Modified: Thu, 13 Jun 2024 18:28:53 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc27e810bf29cf774ea3693f137c338f48a55fcd9b0b4fea5e1d2caf58e236bf`  
		Last Modified: Thu, 13 Jun 2024 18:28:53 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d5888dc1284a2aa4bce210dbf8af2e970f75ccd7c973e418acbb28515c1b98`  
		Last Modified: Thu, 13 Jun 2024 18:28:54 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:20424bf712d71c63b9f7544a480fdd2a517e38857ea60b4a6670e57df14df869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2788702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f234781a8ff2d1edf9144f0b45a9c506f5b1673984c7a04c61eaddf56677ba`

```dockerfile
```

-	Layers:
	-	`sha256:d12f468f75c562ece4a7df52ba540696d1bdb860670d38bb74613e32d0cd12d5`  
		Last Modified: Thu, 13 Jun 2024 18:28:52 GMT  
		Size: 2.8 MB (2755162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:081106b445bdecce52ce39df7f878ccbec04062065d2a592f85046859107c9a8`  
		Last Modified: Thu, 13 Jun 2024 18:28:52 GMT  
		Size: 33.5 KB (33540 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:d9ccf4d36f36102c1a38d7f385c4b33a14cc69ba4f3c64af0d3f542289e98dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 MB (158094169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f54ea7920d13b97b3ecf7f351e9cc4361e0147736f2ffb8b2e5a00420355e4ac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
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
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce1ea3b6373448936e739ee0f0ebf73ae303d4231eb55cae9758d1a3cf05951`  
		Last Modified: Thu, 13 Jun 2024 19:06:31 GMT  
		Size: 9.4 MB (9388817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645a0c4887383b15b407aefefafee7aa3f7d365458d3b6a596f2b61bd6da0db4`  
		Last Modified: Thu, 13 Jun 2024 19:06:31 GMT  
		Size: 5.5 MB (5463787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94cf59e453e7b5c98871fbf3cd2d0223f337134760424ba431e324474daff757`  
		Last Modified: Thu, 13 Jun 2024 19:06:30 GMT  
		Size: 3.2 KB (3228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05aa93a5d874d074948e80d205b4e508c417624943bb88e2e35fb65f92fd90b4`  
		Last Modified: Thu, 13 Jun 2024 19:06:31 GMT  
		Size: 936.1 KB (936106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9bec4fc4e59e2023689d18549ae2ef013ff5dab335528a5f48b698684b96bd`  
		Last Modified: Thu, 13 Jun 2024 19:06:35 GMT  
		Size: 91.5 MB (91453318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef1efac592486882b6e74f4f28ce817ef11ec79b5f5b77adbb8fbfad52489e7`  
		Last Modified: Thu, 13 Jun 2024 19:06:33 GMT  
		Size: 21.7 MB (21662521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b72ce02738a13a6b5efb59a8a98b3755bf73f55c2147fa3f43edfdcfd6c5b3`  
		Last Modified: Thu, 13 Jun 2024 19:06:32 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9cc8a55c0ea84af9576af5a680bc47bae003061c547f72548f711d1a1426471`  
		Last Modified: Thu, 13 Jun 2024 19:06:32 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4e70be6e23adc337e9ce6111f51ec49d07c0b7014c49918e347457e998cd6c`  
		Last Modified: Thu, 13 Jun 2024 19:06:33 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:1cad6a2c3e6e18cf7dede6ddfa98559a36133aab9a40a04084d2ca6d2c182f78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2788385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e6c7da3f669d816be0bb1c6c8ae4c83b0d9d32b619216330fbb1b1f4c38af5`

```dockerfile
```

-	Layers:
	-	`sha256:3ffff0605b518572f1ad5dd2a1b9da5eb66d86cbeaf8b8bd19f7fff86c74f02f`  
		Last Modified: Thu, 13 Jun 2024 19:06:31 GMT  
		Size: 2.8 MB (2754542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5414cc3be457867e9ab93f1555fce2d2a1971d42bb48c5846e7cdf1e1149907`  
		Last Modified: Thu, 13 Jun 2024 19:06:30 GMT  
		Size: 33.8 KB (33843 bytes)  
		MIME: application/vnd.in-toto+json
