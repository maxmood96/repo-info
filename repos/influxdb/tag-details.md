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
$ docker pull influxdb@sha256:8061d9385485b0b605ba652b84ad0fa907902ee1c4591942150e1d471abc039b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-data` - linux; amd64

```console
$ docker pull influxdb@sha256:23fbc12873b2e91d5f17a71b7c92b10a9ca19e13e86a8d74c4f6aab4ccf43273
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112227026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f363bdf74a675c97b988e3397588f276c4d049c17701fdd14e3e91a2ac59bf26`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:e1bdcceaa316a43ad58ce8cf054a8e89ecf5a0dbae8125eb85e9b26fdb2fca2b in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["bash"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Fri, 16 Aug 2024 20:18:45 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:ba83bbfca9443648a883d1404b33faa0f5e096a99a2b683e3bbaee8912bca845`  
		Last Modified: Wed, 04 Sep 2024 22:34:34 GMT  
		Size: 55.1 MB (55081329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e779000ed269823143d5ce9acd3ef6f6ff7465222482f7b02c10ba21f448cc`  
		Last Modified: Wed, 04 Sep 2024 23:02:18 GMT  
		Size: 15.8 MB (15764398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48d628ef1376e9f7ebbcd7c0b7a0eb79e9e76c1bf2157fd12144cca307e5006`  
		Last Modified: Thu, 05 Sep 2024 00:07:24 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7ab6690662448ecaef92b8e30a871c40478a031b192428c6ddd9b2cbf1e432`  
		Last Modified: Thu, 05 Sep 2024 00:07:25 GMT  
		Size: 41.4 MB (41377750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318cbe37c677500ffb4db37b3cdde0f53c9efde562d8ae875b49d76ab3d8b007`  
		Last Modified: Thu, 05 Sep 2024 00:07:24 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f160122f95417a46503340b7b2abfd7f5a3ffc520020927e3d83d81170165455`  
		Last Modified: Thu, 05 Sep 2024 00:07:25 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39150552d86495d3032315c32e916031fd63785fd2570da35793a58a024bdd0`  
		Last Modified: Thu, 05 Sep 2024 00:07:25 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:263647b758acb884ac94521856807f1e12b5b33a271315889b25c4575d2215de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4642339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6185ac407276221e3e70689d924f10a15a4fc264a3168df8fefaca2749683584`

```dockerfile
```

-	Layers:
	-	`sha256:114714e24e99b7198426bfbbaa46bcd3fa6381413831d54b36a9ba6e51b28c69`  
		Last Modified: Thu, 05 Sep 2024 00:07:25 GMT  
		Size: 4.6 MB (4627765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1df7d00973fa65befd15b6be7bc54dc4640ceacaa4613992dcb82df00200d7d4`  
		Last Modified: Thu, 05 Sep 2024 00:07:24 GMT  
		Size: 14.6 KB (14574 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10-data-alpine`

```console
$ docker pull influxdb@sha256:370d944030462279c3189799e5c3a9d15220d6e487ca03af94a1f8788a4da9f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:653874d25b1383462b359d675210b3cd438173fb871ed520b1cdc0dbdb517b89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46172232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c04e5c493c1f404d57e8d8bcd8afe95a301d364b74a83e9177e62b4bedcd1b3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18613db354a55d6bb85cd76fb0f3e831e6591ad95c34b88f90658be65f7116d`  
		Last Modified: Fri, 06 Sep 2024 23:21:24 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e59caec40e984bfa16a5e7147968ab7a9269dd4b26c967e537a1f2501ed3ad`  
		Last Modified: Fri, 06 Sep 2024 23:21:24 GMT  
		Size: 1.2 MB (1223703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0757cceaa7ec332ca815a4d90b3f46ded79411250ca9f1889fb270327c0173`  
		Last Modified: Fri, 06 Sep 2024 23:21:25 GMT  
		Size: 41.3 MB (41322669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c14ee22e9d502bd5298b3848671c5557c53049eb7f60df36ec4f2f758a67b3c9`  
		Last Modified: Fri, 06 Sep 2024 23:21:24 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4be3d77ac7975178bcbbc3155b75b76f8923053f65fa7663f3a5af12c53ec52`  
		Last Modified: Fri, 06 Sep 2024 23:21:24 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83fdf656cf90fdf1b8f8f48b71a53775179b0b60ae49f34b8acc0b7153d19a41`  
		Last Modified: Fri, 06 Sep 2024 23:21:24 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:6d05144fbccc788aaccf6d1dc2007869d0da21c50e5f9e736bea204ad9359559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **769.8 KB (769822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f819c61fc69d757bc44998f0fdba45add017b7d4237cb95072f25a6cd43e6fb3`

```dockerfile
```

-	Layers:
	-	`sha256:c4a3a4d77fa125bb5220f97544befc1b5519f459c8192d57f7c18b73abb78f26`  
		Last Modified: Fri, 06 Sep 2024 23:21:24 GMT  
		Size: 753.4 KB (753398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:830ea66b76032518b0106771dfbc761eb4d76f6dd29fe1f3fe5182d0ca1bd055`  
		Last Modified: Fri, 06 Sep 2024 23:21:24 GMT  
		Size: 16.4 KB (16424 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10-meta`

```console
$ docker pull influxdb@sha256:d7ca856e34063572dc07910edd06fdb8264b69977e0e5545774e64b1d3d82719
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:d65a5d60fbaac17a598a396209a2c2a2c2a55800254db9f2199f4492dac2f4c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.9 MB (90943663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14fd92e369a60d25ff5fda2bebf43c9a2328b0da7365775654d38337972cd971`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:e1bdcceaa316a43ad58ce8cf054a8e89ecf5a0dbae8125eb85e9b26fdb2fca2b in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["bash"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Fri, 16 Aug 2024 20:18:45 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8091/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:ba83bbfca9443648a883d1404b33faa0f5e096a99a2b683e3bbaee8912bca845`  
		Last Modified: Wed, 04 Sep 2024 22:34:34 GMT  
		Size: 55.1 MB (55081329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e779000ed269823143d5ce9acd3ef6f6ff7465222482f7b02c10ba21f448cc`  
		Last Modified: Wed, 04 Sep 2024 23:02:18 GMT  
		Size: 15.8 MB (15764398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:618f3e3cc3f4ef1ef0ccd7eba04c7b686d6de894f95602f8d6458d56adcf937e`  
		Last Modified: Thu, 05 Sep 2024 00:07:17 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af97bef47211e3071ca26c9182f34cbf7c6378b9fcd3e3dac029eec655649705`  
		Last Modified: Thu, 05 Sep 2024 00:07:17 GMT  
		Size: 20.1 MB (20095584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:513e20d7ebaff33273d1464555197222e2229e39bcc4b98a412d07f7453fb647`  
		Last Modified: Thu, 05 Sep 2024 00:07:17 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0561d1a1824ba018c3a295a4f44c085e85764673c9117518b5f5f453e432a3`  
		Last Modified: Thu, 05 Sep 2024 00:07:17 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:151add571eccb9a24da9c22f928356141c73361d2ddeb70d652dacfa74b00080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4565273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d151fd1def2e7d52e45c6ffde321303d13cda079638582a962565721932c475`

```dockerfile
```

-	Layers:
	-	`sha256:2826e7cae244ba800ef6395911030b400d630c0890f5233d1137165662081f30`  
		Last Modified: Thu, 05 Sep 2024 00:07:17 GMT  
		Size: 4.6 MB (4552352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b17f4941fa183207a5801c1c310045f4ee6baca3ec2f0c0a8c56a80ee709b84f`  
		Last Modified: Thu, 05 Sep 2024 00:07:17 GMT  
		Size: 12.9 KB (12921 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10-meta-alpine`

```console
$ docker pull influxdb@sha256:67adfea4d46a3f7184cb062485f23b1a8e47fd5784741dd2a33d267f376e86af
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:bf763c0bcb054bc0918be70c7d67966b574dab590dfd3d3d8272aa5819112dff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.9 MB (24890434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:049d73c8ab49415eb2b21665604553ab378cd72545e8f274d895c11927af5730`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8091/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03dd48d2c5535d4eea4020d819b1c2b0614d8341047cf5641226da18956a050`  
		Last Modified: Fri, 06 Sep 2024 23:21:29 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38aa5ba473028136559f78cd4be4fbc2d308adc5e1a5b8ca6025a8bbd55bc14f`  
		Last Modified: Fri, 06 Sep 2024 23:21:29 GMT  
		Size: 1.2 MB (1223696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d6ebc99cde426570222ae63c2e8e75b500db24c701aba4ddc9229103f38f73`  
		Last Modified: Fri, 06 Sep 2024 23:21:29 GMT  
		Size: 20.0 MB (20042088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c061eb560cf799acbda3a5059aeb5c12617459ebc4e38b3f7d08b3c260f27940`  
		Last Modified: Fri, 06 Sep 2024 23:21:29 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1615cdb4622a98fc159240966cfd0a445043128fbdc8809aba87498e565b2363`  
		Last Modified: Fri, 06 Sep 2024 23:21:29 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:895aac1fbc74f937fcc6a6cdd1af858062f0e38a93dca57ba46a81ba91d834c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **693.0 KB (693036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ff6674d0a004b9c79820b00b6131411dfea7b092bec38adb7e659755c18100`

```dockerfile
```

-	Layers:
	-	`sha256:55fdeb6f675534ee479e135766703a171beb48fe4353e726089a3ccd9a9a1551`  
		Last Modified: Fri, 06 Sep 2024 23:21:29 GMT  
		Size: 678.2 KB (678247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ed4aae58d0b14a616bd7f18d98c46612d64c769948b0b9230b62aa54a91074c`  
		Last Modified: Fri, 06 Sep 2024 23:21:29 GMT  
		Size: 14.8 KB (14789 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10.7-data`

```console
$ docker pull influxdb@sha256:8061d9385485b0b605ba652b84ad0fa907902ee1c4591942150e1d471abc039b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.7-data` - linux; amd64

```console
$ docker pull influxdb@sha256:23fbc12873b2e91d5f17a71b7c92b10a9ca19e13e86a8d74c4f6aab4ccf43273
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112227026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f363bdf74a675c97b988e3397588f276c4d049c17701fdd14e3e91a2ac59bf26`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:e1bdcceaa316a43ad58ce8cf054a8e89ecf5a0dbae8125eb85e9b26fdb2fca2b in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["bash"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Fri, 16 Aug 2024 20:18:45 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:ba83bbfca9443648a883d1404b33faa0f5e096a99a2b683e3bbaee8912bca845`  
		Last Modified: Wed, 04 Sep 2024 22:34:34 GMT  
		Size: 55.1 MB (55081329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e779000ed269823143d5ce9acd3ef6f6ff7465222482f7b02c10ba21f448cc`  
		Last Modified: Wed, 04 Sep 2024 23:02:18 GMT  
		Size: 15.8 MB (15764398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48d628ef1376e9f7ebbcd7c0b7a0eb79e9e76c1bf2157fd12144cca307e5006`  
		Last Modified: Thu, 05 Sep 2024 00:07:24 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7ab6690662448ecaef92b8e30a871c40478a031b192428c6ddd9b2cbf1e432`  
		Last Modified: Thu, 05 Sep 2024 00:07:25 GMT  
		Size: 41.4 MB (41377750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318cbe37c677500ffb4db37b3cdde0f53c9efde562d8ae875b49d76ab3d8b007`  
		Last Modified: Thu, 05 Sep 2024 00:07:24 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f160122f95417a46503340b7b2abfd7f5a3ffc520020927e3d83d81170165455`  
		Last Modified: Thu, 05 Sep 2024 00:07:25 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39150552d86495d3032315c32e916031fd63785fd2570da35793a58a024bdd0`  
		Last Modified: Thu, 05 Sep 2024 00:07:25 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.7-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:263647b758acb884ac94521856807f1e12b5b33a271315889b25c4575d2215de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4642339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6185ac407276221e3e70689d924f10a15a4fc264a3168df8fefaca2749683584`

```dockerfile
```

-	Layers:
	-	`sha256:114714e24e99b7198426bfbbaa46bcd3fa6381413831d54b36a9ba6e51b28c69`  
		Last Modified: Thu, 05 Sep 2024 00:07:25 GMT  
		Size: 4.6 MB (4627765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1df7d00973fa65befd15b6be7bc54dc4640ceacaa4613992dcb82df00200d7d4`  
		Last Modified: Thu, 05 Sep 2024 00:07:24 GMT  
		Size: 14.6 KB (14574 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10.7-data-alpine`

```console
$ docker pull influxdb@sha256:370d944030462279c3189799e5c3a9d15220d6e487ca03af94a1f8788a4da9f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.7-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:653874d25b1383462b359d675210b3cd438173fb871ed520b1cdc0dbdb517b89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46172232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c04e5c493c1f404d57e8d8bcd8afe95a301d364b74a83e9177e62b4bedcd1b3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18613db354a55d6bb85cd76fb0f3e831e6591ad95c34b88f90658be65f7116d`  
		Last Modified: Fri, 06 Sep 2024 23:21:24 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e59caec40e984bfa16a5e7147968ab7a9269dd4b26c967e537a1f2501ed3ad`  
		Last Modified: Fri, 06 Sep 2024 23:21:24 GMT  
		Size: 1.2 MB (1223703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0757cceaa7ec332ca815a4d90b3f46ded79411250ca9f1889fb270327c0173`  
		Last Modified: Fri, 06 Sep 2024 23:21:25 GMT  
		Size: 41.3 MB (41322669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c14ee22e9d502bd5298b3848671c5557c53049eb7f60df36ec4f2f758a67b3c9`  
		Last Modified: Fri, 06 Sep 2024 23:21:24 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4be3d77ac7975178bcbbc3155b75b76f8923053f65fa7663f3a5af12c53ec52`  
		Last Modified: Fri, 06 Sep 2024 23:21:24 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83fdf656cf90fdf1b8f8f48b71a53775179b0b60ae49f34b8acc0b7153d19a41`  
		Last Modified: Fri, 06 Sep 2024 23:21:24 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.7-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:6d05144fbccc788aaccf6d1dc2007869d0da21c50e5f9e736bea204ad9359559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **769.8 KB (769822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f819c61fc69d757bc44998f0fdba45add017b7d4237cb95072f25a6cd43e6fb3`

```dockerfile
```

-	Layers:
	-	`sha256:c4a3a4d77fa125bb5220f97544befc1b5519f459c8192d57f7c18b73abb78f26`  
		Last Modified: Fri, 06 Sep 2024 23:21:24 GMT  
		Size: 753.4 KB (753398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:830ea66b76032518b0106771dfbc761eb4d76f6dd29fe1f3fe5182d0ca1bd055`  
		Last Modified: Fri, 06 Sep 2024 23:21:24 GMT  
		Size: 16.4 KB (16424 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10.7-meta`

```console
$ docker pull influxdb@sha256:d7ca856e34063572dc07910edd06fdb8264b69977e0e5545774e64b1d3d82719
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.7-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:d65a5d60fbaac17a598a396209a2c2a2c2a55800254db9f2199f4492dac2f4c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.9 MB (90943663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14fd92e369a60d25ff5fda2bebf43c9a2328b0da7365775654d38337972cd971`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:e1bdcceaa316a43ad58ce8cf054a8e89ecf5a0dbae8125eb85e9b26fdb2fca2b in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["bash"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Fri, 16 Aug 2024 20:18:45 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8091/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:ba83bbfca9443648a883d1404b33faa0f5e096a99a2b683e3bbaee8912bca845`  
		Last Modified: Wed, 04 Sep 2024 22:34:34 GMT  
		Size: 55.1 MB (55081329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e779000ed269823143d5ce9acd3ef6f6ff7465222482f7b02c10ba21f448cc`  
		Last Modified: Wed, 04 Sep 2024 23:02:18 GMT  
		Size: 15.8 MB (15764398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:618f3e3cc3f4ef1ef0ccd7eba04c7b686d6de894f95602f8d6458d56adcf937e`  
		Last Modified: Thu, 05 Sep 2024 00:07:17 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af97bef47211e3071ca26c9182f34cbf7c6378b9fcd3e3dac029eec655649705`  
		Last Modified: Thu, 05 Sep 2024 00:07:17 GMT  
		Size: 20.1 MB (20095584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:513e20d7ebaff33273d1464555197222e2229e39bcc4b98a412d07f7453fb647`  
		Last Modified: Thu, 05 Sep 2024 00:07:17 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0561d1a1824ba018c3a295a4f44c085e85764673c9117518b5f5f453e432a3`  
		Last Modified: Thu, 05 Sep 2024 00:07:17 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.7-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:151add571eccb9a24da9c22f928356141c73361d2ddeb70d652dacfa74b00080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4565273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d151fd1def2e7d52e45c6ffde321303d13cda079638582a962565721932c475`

```dockerfile
```

-	Layers:
	-	`sha256:2826e7cae244ba800ef6395911030b400d630c0890f5233d1137165662081f30`  
		Last Modified: Thu, 05 Sep 2024 00:07:17 GMT  
		Size: 4.6 MB (4552352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b17f4941fa183207a5801c1c310045f4ee6baca3ec2f0c0a8c56a80ee709b84f`  
		Last Modified: Thu, 05 Sep 2024 00:07:17 GMT  
		Size: 12.9 KB (12921 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10.7-meta-alpine`

```console
$ docker pull influxdb@sha256:67adfea4d46a3f7184cb062485f23b1a8e47fd5784741dd2a33d267f376e86af
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.7-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:bf763c0bcb054bc0918be70c7d67966b574dab590dfd3d3d8272aa5819112dff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.9 MB (24890434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:049d73c8ab49415eb2b21665604553ab378cd72545e8f274d895c11927af5730`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8091/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03dd48d2c5535d4eea4020d819b1c2b0614d8341047cf5641226da18956a050`  
		Last Modified: Fri, 06 Sep 2024 23:21:29 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38aa5ba473028136559f78cd4be4fbc2d308adc5e1a5b8ca6025a8bbd55bc14f`  
		Last Modified: Fri, 06 Sep 2024 23:21:29 GMT  
		Size: 1.2 MB (1223696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d6ebc99cde426570222ae63c2e8e75b500db24c701aba4ddc9229103f38f73`  
		Last Modified: Fri, 06 Sep 2024 23:21:29 GMT  
		Size: 20.0 MB (20042088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c061eb560cf799acbda3a5059aeb5c12617459ebc4e38b3f7d08b3c260f27940`  
		Last Modified: Fri, 06 Sep 2024 23:21:29 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1615cdb4622a98fc159240966cfd0a445043128fbdc8809aba87498e565b2363`  
		Last Modified: Fri, 06 Sep 2024 23:21:29 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.7-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:895aac1fbc74f937fcc6a6cdd1af858062f0e38a93dca57ba46a81ba91d834c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **693.0 KB (693036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ff6674d0a004b9c79820b00b6131411dfea7b092bec38adb7e659755c18100`

```dockerfile
```

-	Layers:
	-	`sha256:55fdeb6f675534ee479e135766703a171beb48fe4353e726089a3ccd9a9a1551`  
		Last Modified: Fri, 06 Sep 2024 23:21:29 GMT  
		Size: 678.2 KB (678247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ed4aae58d0b14a616bd7f18d98c46612d64c769948b0b9230b62aa54a91074c`  
		Last Modified: Fri, 06 Sep 2024 23:21:29 GMT  
		Size: 14.8 KB (14789 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-data`

```console
$ docker pull influxdb@sha256:fc5429b63bdaf6f07092d7a04a8b1ad6b3d52f5b1e4c8a4d4784f3d64ea98cec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data` - linux; amd64

```console
$ docker pull influxdb@sha256:e1ce84c069cda2d14bd92d36d1a795adc3e5a0eaf533fba6fe964b02a0f63230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114737850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c117267f1be297d592181aeb332b7471234ef4802d74181c57716bf2ad5e074e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["bash"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=1.11.6-c1.11.6
# Fri, 16 Aug 2024 20:18:45 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6afa3f266c11e8960349e7866203a9df478a50362bb5488c45fe39d99b2707`  
		Last Modified: Wed, 04 Sep 2024 23:01:16 GMT  
		Size: 24.1 MB (24053153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cbdef24485959f16fe63a7989babef84af3ab193d82f3471faa4f4114837f94`  
		Last Modified: Thu, 05 Sep 2024 00:07:24 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923689fdab5fa7293367f0c671ef7c222e0b1f3a207267bd0a1fb5f66a612a81`  
		Last Modified: Thu, 05 Sep 2024 00:07:25 GMT  
		Size: 41.1 MB (41124436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9272bf7ac2eeeb5a91ed7f370a62528e79c0cf9438b25184650205efcf9511f8`  
		Last Modified: Thu, 05 Sep 2024 00:07:24 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36fbef62a9c69f5ebcf0143caa0574ae7ab4448ecd46b8f92d028eb5ad23001`  
		Last Modified: Thu, 05 Sep 2024 00:07:24 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:817767cb2d0e0dd298a6144dd0bd21cf6e7c8f2dcec4b2b52ec150b322a4cea6`  
		Last Modified: Thu, 05 Sep 2024 00:07:25 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:ab8dbcf7a825ed03f2db1263c9031b6bfeff0fd4a125ea1c3f43ccf030800f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4515212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d175d677ea0227269900df4eabb1225e622bd93ceb6669f6e8dd26d71388be4`

```dockerfile
```

-	Layers:
	-	`sha256:11d607603ac694676cda749a049ffb4bcd4834da0b5de423d1c6a7c3dc137b45`  
		Last Modified: Thu, 05 Sep 2024 00:07:24 GMT  
		Size: 4.5 MB (4500638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2833f79afb90fc7db8042cfbf57a867dcfec0b47f16c12b4ae37d813fb52304`  
		Last Modified: Thu, 05 Sep 2024 00:07:24 GMT  
		Size: 14.6 KB (14574 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-data-alpine`

```console
$ docker pull influxdb@sha256:793f886a0f196db5905fe5c032ad3ef68d70ad98c34c6637ea21bce6229a8ddf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:573fd78175f9c2b67d5134f99e038cb635825904582cebeb099e80587bc00159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45917646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ed4bbecfe834f3c3e8b5c61751972611866f1e7ae3deafc324207bd89a86f6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=1.11.6-c1.11.6
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:857ecb64e1c45d46a8c34612f7a82dff76a2e2dc69ad314d38fb25ecbefb8935`  
		Last Modified: Fri, 06 Sep 2024 23:21:30 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d259500ab08714fd23f323e03db9b6667d134caa6125bc719b389b715b0d72`  
		Last Modified: Fri, 06 Sep 2024 23:21:30 GMT  
		Size: 1.2 MB (1223697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5ed4398154e144152fceb43093803a978b1642da200499812971bf123cdcfe`  
		Last Modified: Fri, 06 Sep 2024 23:21:31 GMT  
		Size: 41.1 MB (41068088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a6154e867ed06e7522e5f54847c2eae97d713e8902c5d37b425c92b5e3c45b`  
		Last Modified: Fri, 06 Sep 2024 23:21:30 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d38d399e914c79804eebd54b4a7d99674b1e1d40f47a7bc9152a6ed3b0bdbf`  
		Last Modified: Fri, 06 Sep 2024 23:21:31 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464862829bd851eba89202a10fbcf1648268f3bc281488f81516fd88e9ec75b4`  
		Last Modified: Fri, 06 Sep 2024 23:21:31 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:131870e981caa20de1edd37280d24b40a7fe3b95cee55d955fa15b1af30a3e50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **769.0 KB (769006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6649dc24824db616e8fc760ca5599e1218515de43eb8a6568dbdc6ad8cdd652c`

```dockerfile
```

-	Layers:
	-	`sha256:d1e882cf6a38dfc88429d43a01e90cd5f85aa265dc0f421c764a7267f6d54e42`  
		Last Modified: Fri, 06 Sep 2024 23:21:30 GMT  
		Size: 752.6 KB (752582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80efadee668de3a90c9d62413a69233f4a279b4f423beb1d10924af871ad913b`  
		Last Modified: Fri, 06 Sep 2024 23:21:30 GMT  
		Size: 16.4 KB (16424 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-meta`

```console
$ docker pull influxdb@sha256:fba180529c4956404f095216dd07e5113901a2408e18195c34e5d35189ee8d26
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:6f2ecd106b00cc0200625b38207af91e78faa26bdd198adc18167b88addb12e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93405144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6067f66c866248a8310b79d5a0e895aeda3a03029de7beda46201f25eb13b37b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["bash"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=1.11.6-c1.11.6
# Fri, 16 Aug 2024 20:18:45 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8091/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6afa3f266c11e8960349e7866203a9df478a50362bb5488c45fe39d99b2707`  
		Last Modified: Wed, 04 Sep 2024 23:01:16 GMT  
		Size: 24.1 MB (24053153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ab7d46ec983fb778815f9093777fc0c9e2fc21b85a3fd214210b14d11712c8`  
		Last Modified: Thu, 05 Sep 2024 00:07:18 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d01453461eddf0df37b9d68affbca83a7ec243d34615a24d1977f302d6925b41`  
		Last Modified: Thu, 05 Sep 2024 00:07:18 GMT  
		Size: 19.8 MB (19792951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a34da6abdb53ed675a0ed2b62e6b6145f111ad0cd00f92c9f0fc4e1cfeb1731`  
		Last Modified: Thu, 05 Sep 2024 00:07:18 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0561d1a1824ba018c3a295a4f44c085e85764673c9117518b5f5f453e432a3`  
		Last Modified: Thu, 05 Sep 2024 00:07:17 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:e8842e27fb455505f481c3952ff3796d3180bd946d024043523872319823de8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4438311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39265cdab7165ca7852b3badb04ebe005433de8cae0c577428c9a922975690f2`

```dockerfile
```

-	Layers:
	-	`sha256:280c7104a41b00e83ff6ce1675c0581c8523d0f05f5726b7369e7d82d91c4502`  
		Last Modified: Thu, 05 Sep 2024 00:07:18 GMT  
		Size: 4.4 MB (4425390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55127cdf07a184a8acbbaeab23d32e7ed157932e5c47c1baea6e195a5071fa7e`  
		Last Modified: Thu, 05 Sep 2024 00:07:18 GMT  
		Size: 12.9 KB (12921 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-meta-alpine`

```console
$ docker pull influxdb@sha256:96bd9ec295c6c0ab62749a038cdc13ad5082792a73d41ded0f2d21e35fe9f21f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:a56a53388024c062e4f3ee08114cf6986b61f6201e5d8373384ec217117e903b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24584604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:500aabb8f592d298e1e576c5317e23c7059936093841aea87577a95931515648`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=1.11.6-c1.11.6
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8091/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078166243ebe0c2b9c91a2f7e164076218c7716b68301080fac2f19f177dd096`  
		Last Modified: Fri, 06 Sep 2024 23:21:35 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1798891eeacb4169638b5166c9e8cac1a921167b71619feef52252cbc89c4dda`  
		Last Modified: Fri, 06 Sep 2024 23:21:35 GMT  
		Size: 1.2 MB (1223696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef37378c1a1c94f9d7791528dd34dc79702e4799fd548e2bfe6b9ca7b343955`  
		Last Modified: Fri, 06 Sep 2024 23:21:36 GMT  
		Size: 19.7 MB (19736254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8e176e0b983dd08fc989b466f8cbf8fb62e7e9c6c212c76ea7bd08b5118414`  
		Last Modified: Fri, 06 Sep 2024 23:21:35 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227ebad2c15b696728c9d1fa05d604f31709b9ddfecaa3e9cf9a0b6aedce32e3`  
		Last Modified: Fri, 06 Sep 2024 23:21:36 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:3cb8c03d383d8b03f6bda40519a6a1d6d8fce3d357ca1193992ccbca30832abe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **693.0 KB (693016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5562508b37e0ac45d12bf7f861aee0c9b278146b238c0c07af053d8dc44277de`

```dockerfile
```

-	Layers:
	-	`sha256:8733ae4a661f1f95273f1984aa60368d9b1a0c7d2e9affdbce5ab38fb7aa9192`  
		Last Modified: Fri, 06 Sep 2024 23:21:35 GMT  
		Size: 678.2 KB (678227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42d685a470a69c05014558d05c4b43b664c5d30866a83c2a64b167a2204ff9bf`  
		Last Modified: Fri, 06 Sep 2024 23:21:35 GMT  
		Size: 14.8 KB (14789 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.6-data`

```console
$ docker pull influxdb@sha256:fc5429b63bdaf6f07092d7a04a8b1ad6b3d52f5b1e4c8a4d4784f3d64ea98cec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.6-data` - linux; amd64

```console
$ docker pull influxdb@sha256:e1ce84c069cda2d14bd92d36d1a795adc3e5a0eaf533fba6fe964b02a0f63230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114737850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c117267f1be297d592181aeb332b7471234ef4802d74181c57716bf2ad5e074e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["bash"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=1.11.6-c1.11.6
# Fri, 16 Aug 2024 20:18:45 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6afa3f266c11e8960349e7866203a9df478a50362bb5488c45fe39d99b2707`  
		Last Modified: Wed, 04 Sep 2024 23:01:16 GMT  
		Size: 24.1 MB (24053153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cbdef24485959f16fe63a7989babef84af3ab193d82f3471faa4f4114837f94`  
		Last Modified: Thu, 05 Sep 2024 00:07:24 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923689fdab5fa7293367f0c671ef7c222e0b1f3a207267bd0a1fb5f66a612a81`  
		Last Modified: Thu, 05 Sep 2024 00:07:25 GMT  
		Size: 41.1 MB (41124436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9272bf7ac2eeeb5a91ed7f370a62528e79c0cf9438b25184650205efcf9511f8`  
		Last Modified: Thu, 05 Sep 2024 00:07:24 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36fbef62a9c69f5ebcf0143caa0574ae7ab4448ecd46b8f92d028eb5ad23001`  
		Last Modified: Thu, 05 Sep 2024 00:07:24 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:817767cb2d0e0dd298a6144dd0bd21cf6e7c8f2dcec4b2b52ec150b322a4cea6`  
		Last Modified: Thu, 05 Sep 2024 00:07:25 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.6-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:ab8dbcf7a825ed03f2db1263c9031b6bfeff0fd4a125ea1c3f43ccf030800f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4515212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d175d677ea0227269900df4eabb1225e622bd93ceb6669f6e8dd26d71388be4`

```dockerfile
```

-	Layers:
	-	`sha256:11d607603ac694676cda749a049ffb4bcd4834da0b5de423d1c6a7c3dc137b45`  
		Last Modified: Thu, 05 Sep 2024 00:07:24 GMT  
		Size: 4.5 MB (4500638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2833f79afb90fc7db8042cfbf57a867dcfec0b47f16c12b4ae37d813fb52304`  
		Last Modified: Thu, 05 Sep 2024 00:07:24 GMT  
		Size: 14.6 KB (14574 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.6-data-alpine`

```console
$ docker pull influxdb@sha256:793f886a0f196db5905fe5c032ad3ef68d70ad98c34c6637ea21bce6229a8ddf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.6-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:573fd78175f9c2b67d5134f99e038cb635825904582cebeb099e80587bc00159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45917646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ed4bbecfe834f3c3e8b5c61751972611866f1e7ae3deafc324207bd89a86f6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=1.11.6-c1.11.6
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:857ecb64e1c45d46a8c34612f7a82dff76a2e2dc69ad314d38fb25ecbefb8935`  
		Last Modified: Fri, 06 Sep 2024 23:21:30 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d259500ab08714fd23f323e03db9b6667d134caa6125bc719b389b715b0d72`  
		Last Modified: Fri, 06 Sep 2024 23:21:30 GMT  
		Size: 1.2 MB (1223697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5ed4398154e144152fceb43093803a978b1642da200499812971bf123cdcfe`  
		Last Modified: Fri, 06 Sep 2024 23:21:31 GMT  
		Size: 41.1 MB (41068088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a6154e867ed06e7522e5f54847c2eae97d713e8902c5d37b425c92b5e3c45b`  
		Last Modified: Fri, 06 Sep 2024 23:21:30 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d38d399e914c79804eebd54b4a7d99674b1e1d40f47a7bc9152a6ed3b0bdbf`  
		Last Modified: Fri, 06 Sep 2024 23:21:31 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464862829bd851eba89202a10fbcf1648268f3bc281488f81516fd88e9ec75b4`  
		Last Modified: Fri, 06 Sep 2024 23:21:31 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.6-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:131870e981caa20de1edd37280d24b40a7fe3b95cee55d955fa15b1af30a3e50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **769.0 KB (769006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6649dc24824db616e8fc760ca5599e1218515de43eb8a6568dbdc6ad8cdd652c`

```dockerfile
```

-	Layers:
	-	`sha256:d1e882cf6a38dfc88429d43a01e90cd5f85aa265dc0f421c764a7267f6d54e42`  
		Last Modified: Fri, 06 Sep 2024 23:21:30 GMT  
		Size: 752.6 KB (752582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80efadee668de3a90c9d62413a69233f4a279b4f423beb1d10924af871ad913b`  
		Last Modified: Fri, 06 Sep 2024 23:21:30 GMT  
		Size: 16.4 KB (16424 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.6-meta`

```console
$ docker pull influxdb@sha256:fba180529c4956404f095216dd07e5113901a2408e18195c34e5d35189ee8d26
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.6-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:6f2ecd106b00cc0200625b38207af91e78faa26bdd198adc18167b88addb12e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93405144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6067f66c866248a8310b79d5a0e895aeda3a03029de7beda46201f25eb13b37b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["bash"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=1.11.6-c1.11.6
# Fri, 16 Aug 2024 20:18:45 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8091/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6afa3f266c11e8960349e7866203a9df478a50362bb5488c45fe39d99b2707`  
		Last Modified: Wed, 04 Sep 2024 23:01:16 GMT  
		Size: 24.1 MB (24053153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ab7d46ec983fb778815f9093777fc0c9e2fc21b85a3fd214210b14d11712c8`  
		Last Modified: Thu, 05 Sep 2024 00:07:18 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d01453461eddf0df37b9d68affbca83a7ec243d34615a24d1977f302d6925b41`  
		Last Modified: Thu, 05 Sep 2024 00:07:18 GMT  
		Size: 19.8 MB (19792951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a34da6abdb53ed675a0ed2b62e6b6145f111ad0cd00f92c9f0fc4e1cfeb1731`  
		Last Modified: Thu, 05 Sep 2024 00:07:18 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0561d1a1824ba018c3a295a4f44c085e85764673c9117518b5f5f453e432a3`  
		Last Modified: Thu, 05 Sep 2024 00:07:17 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.6-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:e8842e27fb455505f481c3952ff3796d3180bd946d024043523872319823de8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4438311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39265cdab7165ca7852b3badb04ebe005433de8cae0c577428c9a922975690f2`

```dockerfile
```

-	Layers:
	-	`sha256:280c7104a41b00e83ff6ce1675c0581c8523d0f05f5726b7369e7d82d91c4502`  
		Last Modified: Thu, 05 Sep 2024 00:07:18 GMT  
		Size: 4.4 MB (4425390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55127cdf07a184a8acbbaeab23d32e7ed157932e5c47c1baea6e195a5071fa7e`  
		Last Modified: Thu, 05 Sep 2024 00:07:18 GMT  
		Size: 12.9 KB (12921 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.6-meta-alpine`

```console
$ docker pull influxdb@sha256:96bd9ec295c6c0ab62749a038cdc13ad5082792a73d41ded0f2d21e35fe9f21f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.6-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:a56a53388024c062e4f3ee08114cf6986b61f6201e5d8373384ec217117e903b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24584604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:500aabb8f592d298e1e576c5317e23c7059936093841aea87577a95931515648`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=1.11.6-c1.11.6
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8091/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078166243ebe0c2b9c91a2f7e164076218c7716b68301080fac2f19f177dd096`  
		Last Modified: Fri, 06 Sep 2024 23:21:35 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1798891eeacb4169638b5166c9e8cac1a921167b71619feef52252cbc89c4dda`  
		Last Modified: Fri, 06 Sep 2024 23:21:35 GMT  
		Size: 1.2 MB (1223696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef37378c1a1c94f9d7791528dd34dc79702e4799fd548e2bfe6b9ca7b343955`  
		Last Modified: Fri, 06 Sep 2024 23:21:36 GMT  
		Size: 19.7 MB (19736254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8e176e0b983dd08fc989b466f8cbf8fb62e7e9c6c212c76ea7bd08b5118414`  
		Last Modified: Fri, 06 Sep 2024 23:21:35 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227ebad2c15b696728c9d1fa05d604f31709b9ddfecaa3e9cf9a0b6aedce32e3`  
		Last Modified: Fri, 06 Sep 2024 23:21:36 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.6-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:3cb8c03d383d8b03f6bda40519a6a1d6d8fce3d357ca1193992ccbca30832abe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **693.0 KB (693016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5562508b37e0ac45d12bf7f861aee0c9b278146b238c0c07af053d8dc44277de`

```dockerfile
```

-	Layers:
	-	`sha256:8733ae4a661f1f95273f1984aa60368d9b1a0c7d2e9affdbce5ab38fb7aa9192`  
		Last Modified: Fri, 06 Sep 2024 23:21:35 GMT  
		Size: 678.2 KB (678227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42d685a470a69c05014558d05c4b43b664c5d30866a83c2a64b167a2204ff9bf`  
		Last Modified: Fri, 06 Sep 2024 23:21:35 GMT  
		Size: 14.8 KB (14789 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.8`

```console
$ docker pull influxdb@sha256:2d4846756ff07787af6cbb62c60d2b130734ed1ffaeab878daeea7fd8dc362d2
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
$ docker pull influxdb@sha256:0b80e8e602be61636bfc50520369fa171979bb9f50e4a7f587089b1710aa1860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125734632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99bbc70e243d1afada9eddb6274e9bac9376a3f8ce0451b04947f392f6e1db7a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:e1bdcceaa316a43ad58ce8cf054a8e89ecf5a0dbae8125eb85e9b26fdb2fca2b in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["bash"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=1.8.10
# Fri, 16 Aug 2024 20:18:45 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb* # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:ba83bbfca9443648a883d1404b33faa0f5e096a99a2b683e3bbaee8912bca845`  
		Last Modified: Wed, 04 Sep 2024 22:34:34 GMT  
		Size: 55.1 MB (55081329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e779000ed269823143d5ce9acd3ef6f6ff7465222482f7b02c10ba21f448cc`  
		Last Modified: Wed, 04 Sep 2024 23:02:18 GMT  
		Size: 15.8 MB (15764398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32c4e3b42ad04f94e9f7efdd685e1303aef713ead689e322ba447781d6222e6`  
		Last Modified: Thu, 05 Sep 2024 00:07:21 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f51177c502b7e2a53113ba4f3b1324158452bcdb35ce7e581e19a73189f57e85`  
		Last Modified: Thu, 05 Sep 2024 00:07:22 GMT  
		Size: 54.9 MB (54885402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0cc17e692b22c835f49853419dc6e1a27ac3202f067878259addac0678e858`  
		Last Modified: Thu, 05 Sep 2024 00:07:21 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1ac99f35a4b1aabe14b7ac292039696f2f6ca808c639b439e6b270fc552200`  
		Last Modified: Thu, 05 Sep 2024 00:07:21 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:048078e3cfbf5890e03b21e5c1b361837b6c7abba724caf8fa39c93975e77190`  
		Last Modified: Thu, 05 Sep 2024 00:07:21 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:db36e0abd08321225f9240c5fd3bb891cccf7ca54b9962421b951e71ab21085c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4505064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf637e86f7baa8aa2f8d9ece2439b90cea7010d12b6b78e88510054fb6366ae5`

```dockerfile
```

-	Layers:
	-	`sha256:535c35954befbb527026ffa5ff5512dba8ae05d1db7c0aeb3719c8b37b83aca5`  
		Last Modified: Thu, 05 Sep 2024 00:07:21 GMT  
		Size: 4.5 MB (4489602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bd1470a6bfe94a904f057830c544eaefe76028cd5fa983d11b60f5dcebf2989`  
		Last Modified: Thu, 05 Sep 2024 00:07:21 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.8` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:778b94492a48ba32b3cb31337715bda9fe3db77845d4f2aa7acac21364ca0548
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.7 MB (116736612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:686c7d46f35080ab1f7f0e99e08745b0c3f9d180b7d8f0436fb117006dba4aba`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:e3043c245364d9fe593e24bbcac51334dca659e8ec7cd42b6368ba7ea83ea087 in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["bash"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=1.8.10
# Fri, 16 Aug 2024 20:18:45 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb* # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:3e424c6173543918aac0bf0552ca8359d23f7b7baa2d77fc8e2c9deb6756f39d`  
		Last Modified: Wed, 04 Sep 2024 22:02:04 GMT  
		Size: 50.2 MB (50240273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0451e8e66d2aa4834e6580560eb32abf8bbac64409d70c85811226b651f2aba`  
		Last Modified: Wed, 04 Sep 2024 22:37:06 GMT  
		Size: 14.9 MB (14879935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc25e14cad7979203f8f57b6993097c9c6b25dd52fc629b1e066cb819311de28`  
		Last Modified: Thu, 05 Sep 2024 23:29:44 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7bf69b4bc799ce78303838f59d1c3b596955cfbe9a02ac68d920b066053929`  
		Last Modified: Thu, 05 Sep 2024 23:29:46 GMT  
		Size: 51.6 MB (51612902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0c4093a2efe78d3079743abd5057e48336317b93070db32f68870d754d24af`  
		Last Modified: Thu, 05 Sep 2024 23:29:44 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4025bbd1fc834d20e1ef60b3e88eaae077878c0a617e0107089e2f615361fa13`  
		Last Modified: Thu, 05 Sep 2024 23:29:44 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e254dd0828d7d9d8315d047574b1a5dc04d181411d09b8cc1d2fe0b6de20ad93`  
		Last Modified: Thu, 05 Sep 2024 23:29:45 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:333fa05346f69a7a4ca67af997f40a58e4d3ef8693d2359b9780d292e2625931
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4506765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:508d5a8108831e0c96b131e3bd67459036def67b8b43cb1ec60f4d390172e132`

```dockerfile
```

-	Layers:
	-	`sha256:8f920905034fc18f7ad82be5667ec4c5bc6676d676ac454b75deb81d7b02e209`  
		Last Modified: Thu, 05 Sep 2024 23:29:45 GMT  
		Size: 4.5 MB (4491236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab1388228bd77b7925a42ab6a3aae4ce18c31b05e0d4a668a734d8c80cd5c214`  
		Last Modified: Thu, 05 Sep 2024 23:29:44 GMT  
		Size: 15.5 KB (15529 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:e76311afc20d32c6ef6297086418956100ea398e1f96f787f375eb1cf461bb68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120714731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f46829530ad94dea5ccf9be815bff9c3b29f9e78cd5ee49a02f8a5cf690aef7c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:aad8b86b3a958bc07504985acedcc819faa4f1ed12ca8b46d8d94c4d564cbdfa in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["bash"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=1.8.10
# Fri, 16 Aug 2024 20:18:45 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb* # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:d82c4492ee91810a42e0c53e955a661e9a092364bc474c9db559ea5b24b7047f`  
		Last Modified: Wed, 04 Sep 2024 21:42:52 GMT  
		Size: 53.7 MB (53731619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf248fd698830ce7c74f07fb7ca6adac7bea55a16521e9e1f2afe06219e00f6`  
		Last Modified: Wed, 04 Sep 2024 22:08:56 GMT  
		Size: 15.7 MB (15749712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5139f22d8f65526bce73fabdb47a0cf930d4f9440f9bd83cf2aaa2c069d3c54`  
		Last Modified: Thu, 05 Sep 2024 12:17:52 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:625920f7e298fab2d79cf80d0c012b3bf5b07f0a48a45604b8e52568c5e04bda`  
		Last Modified: Thu, 05 Sep 2024 12:17:54 GMT  
		Size: 51.2 MB (51229894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e534a8c3450ec9794a8865e2ec1b27afa297d1fda6a96c2c54a642c11a6b6d4`  
		Last Modified: Thu, 05 Sep 2024 12:17:52 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8cad6ae7011b47b6b7f0451e661abb3920aa13ac6bdc6d711bd15381ef8a91`  
		Last Modified: Thu, 05 Sep 2024 12:17:52 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2c4b345db382001b449eda23efecb6a7bf18857b16fc649bc1ab44075024c0`  
		Last Modified: Thu, 05 Sep 2024 12:17:53 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:fbc84754f3650746b1687403f93dceb7610992f2a34687a8b0105b3085b11e0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4504969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0425648e1bbdf9b04fe71deff6b27568357acaa2ea37c55044cb87befbd0572c`

```dockerfile
```

-	Layers:
	-	`sha256:87a8bc3465e29c8e4e5440dbb0081fa81573865781c02b8cf91a0be19ab140a0`  
		Last Modified: Thu, 05 Sep 2024 12:17:53 GMT  
		Size: 4.5 MB (4489214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad833097f6da63d42b7bf37a73d710803f225f29e3d1bd166e24237c925a7d55`  
		Last Modified: Thu, 05 Sep 2024 12:17:52 GMT  
		Size: 15.8 KB (15755 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.8-alpine`

```console
$ docker pull influxdb@sha256:2601e27d6b7eac276017d7ea48d2685d52639cea974744b5877924376283a4cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.8-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:323bec748932cf3049bcd0ad3df03da7a85743014f37c5c06390d3dd090d5027
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59520385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c14632645a8e98cabcfa629d7f97d199afdc7b0435d24fe7c0bffcbd0925fe6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:8bf458f5fbed9f27c897506538c02fb5810b70aba850bb883d2120985fa15bac in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=1.8.10
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     chmod +x /usr/src/influxdb-*/influx              /usr/src/influxdb-*/influx_inspect              /usr/src/influxdb-*/influx_stress              /usr/src/influxdb-*/influxd &&    mv /usr/src/influxdb-*/influx        /usr/src/influxdb-*/influx_inspect        /usr/src/influxdb-*/influx_stress         /usr/src/influxdb-*/influxd        /usr/bin/ &&    gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:a0f4cbe03b6df9e61ce02b3c41bbc05481842858bd48d9687614abe719303b47`  
		Last Modified: Fri, 06 Sep 2024 22:21:07 GMT  
		Size: 3.4 MB (3392194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a63e70873dd8d18fc4e609edbcd780bf91673580b44f6778efc5cd01e91416`  
		Last Modified: Fri, 06 Sep 2024 23:21:20 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3019afc3f13df4911e2077ec99e0d88ca3cea7acca75646748dc4448363fdc6`  
		Last Modified: Fri, 06 Sep 2024 23:21:20 GMT  
		Size: 1.5 MB (1479482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40cfe8e6bcbeae6388a3e7d07db6cd1394e73cdf54ce683edbb1b7c3671a17c`  
		Last Modified: Fri, 06 Sep 2024 23:21:20 GMT  
		Size: 54.6 MB (54646714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784f4de03565d8b1d250901b03046846f5c1d470c593bd5c3659ace47f783ede`  
		Last Modified: Fri, 06 Sep 2024 23:21:20 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736622afe4eb3db6ea76fd89d7ac1d5e77d5880030d85231d501cfcbbf109518`  
		Last Modified: Fri, 06 Sep 2024 23:21:20 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85d23128f7bc1806470e05b177060a051b55e1f209ee6fbdc04ff31e2077651`  
		Last Modified: Fri, 06 Sep 2024 23:21:21 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:bb8c66f3e48bbdf4bf837fcc1ee9679803fbe889db56efdf5357a718e9e0949c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1004063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67740208b251a99deebeae23d6c8d13b17326e8cca04cbb249627ac8460a4277`

```dockerfile
```

-	Layers:
	-	`sha256:a9272376189bcad2f11697903cbc6eccc780943ecc0445d25c1c98feb509eaf7`  
		Last Modified: Fri, 06 Sep 2024 23:21:20 GMT  
		Size: 986.7 KB (986701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58257e0baabc8dbe52d193e3864f126406b8a8ef94fcc42024004fe91365e44f`  
		Last Modified: Fri, 06 Sep 2024 23:21:20 GMT  
		Size: 17.4 KB (17362 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.8.10`

```console
$ docker pull influxdb@sha256:2d4846756ff07787af6cbb62c60d2b130734ed1ffaeab878daeea7fd8dc362d2
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
$ docker pull influxdb@sha256:0b80e8e602be61636bfc50520369fa171979bb9f50e4a7f587089b1710aa1860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125734632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99bbc70e243d1afada9eddb6274e9bac9376a3f8ce0451b04947f392f6e1db7a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:e1bdcceaa316a43ad58ce8cf054a8e89ecf5a0dbae8125eb85e9b26fdb2fca2b in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["bash"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=1.8.10
# Fri, 16 Aug 2024 20:18:45 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb* # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:ba83bbfca9443648a883d1404b33faa0f5e096a99a2b683e3bbaee8912bca845`  
		Last Modified: Wed, 04 Sep 2024 22:34:34 GMT  
		Size: 55.1 MB (55081329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e779000ed269823143d5ce9acd3ef6f6ff7465222482f7b02c10ba21f448cc`  
		Last Modified: Wed, 04 Sep 2024 23:02:18 GMT  
		Size: 15.8 MB (15764398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32c4e3b42ad04f94e9f7efdd685e1303aef713ead689e322ba447781d6222e6`  
		Last Modified: Thu, 05 Sep 2024 00:07:21 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f51177c502b7e2a53113ba4f3b1324158452bcdb35ce7e581e19a73189f57e85`  
		Last Modified: Thu, 05 Sep 2024 00:07:22 GMT  
		Size: 54.9 MB (54885402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0cc17e692b22c835f49853419dc6e1a27ac3202f067878259addac0678e858`  
		Last Modified: Thu, 05 Sep 2024 00:07:21 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1ac99f35a4b1aabe14b7ac292039696f2f6ca808c639b439e6b270fc552200`  
		Last Modified: Thu, 05 Sep 2024 00:07:21 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:048078e3cfbf5890e03b21e5c1b361837b6c7abba724caf8fa39c93975e77190`  
		Last Modified: Thu, 05 Sep 2024 00:07:21 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8.10` - unknown; unknown

```console
$ docker pull influxdb@sha256:db36e0abd08321225f9240c5fd3bb891cccf7ca54b9962421b951e71ab21085c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4505064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf637e86f7baa8aa2f8d9ece2439b90cea7010d12b6b78e88510054fb6366ae5`

```dockerfile
```

-	Layers:
	-	`sha256:535c35954befbb527026ffa5ff5512dba8ae05d1db7c0aeb3719c8b37b83aca5`  
		Last Modified: Thu, 05 Sep 2024 00:07:21 GMT  
		Size: 4.5 MB (4489602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bd1470a6bfe94a904f057830c544eaefe76028cd5fa983d11b60f5dcebf2989`  
		Last Modified: Thu, 05 Sep 2024 00:07:21 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.8.10` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:778b94492a48ba32b3cb31337715bda9fe3db77845d4f2aa7acac21364ca0548
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.7 MB (116736612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:686c7d46f35080ab1f7f0e99e08745b0c3f9d180b7d8f0436fb117006dba4aba`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:e3043c245364d9fe593e24bbcac51334dca659e8ec7cd42b6368ba7ea83ea087 in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["bash"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=1.8.10
# Fri, 16 Aug 2024 20:18:45 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb* # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:3e424c6173543918aac0bf0552ca8359d23f7b7baa2d77fc8e2c9deb6756f39d`  
		Last Modified: Wed, 04 Sep 2024 22:02:04 GMT  
		Size: 50.2 MB (50240273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0451e8e66d2aa4834e6580560eb32abf8bbac64409d70c85811226b651f2aba`  
		Last Modified: Wed, 04 Sep 2024 22:37:06 GMT  
		Size: 14.9 MB (14879935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc25e14cad7979203f8f57b6993097c9c6b25dd52fc629b1e066cb819311de28`  
		Last Modified: Thu, 05 Sep 2024 23:29:44 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7bf69b4bc799ce78303838f59d1c3b596955cfbe9a02ac68d920b066053929`  
		Last Modified: Thu, 05 Sep 2024 23:29:46 GMT  
		Size: 51.6 MB (51612902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0c4093a2efe78d3079743abd5057e48336317b93070db32f68870d754d24af`  
		Last Modified: Thu, 05 Sep 2024 23:29:44 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4025bbd1fc834d20e1ef60b3e88eaae077878c0a617e0107089e2f615361fa13`  
		Last Modified: Thu, 05 Sep 2024 23:29:44 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e254dd0828d7d9d8315d047574b1a5dc04d181411d09b8cc1d2fe0b6de20ad93`  
		Last Modified: Thu, 05 Sep 2024 23:29:45 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8.10` - unknown; unknown

```console
$ docker pull influxdb@sha256:333fa05346f69a7a4ca67af997f40a58e4d3ef8693d2359b9780d292e2625931
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4506765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:508d5a8108831e0c96b131e3bd67459036def67b8b43cb1ec60f4d390172e132`

```dockerfile
```

-	Layers:
	-	`sha256:8f920905034fc18f7ad82be5667ec4c5bc6676d676ac454b75deb81d7b02e209`  
		Last Modified: Thu, 05 Sep 2024 23:29:45 GMT  
		Size: 4.5 MB (4491236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab1388228bd77b7925a42ab6a3aae4ce18c31b05e0d4a668a734d8c80cd5c214`  
		Last Modified: Thu, 05 Sep 2024 23:29:44 GMT  
		Size: 15.5 KB (15529 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.8.10` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:e76311afc20d32c6ef6297086418956100ea398e1f96f787f375eb1cf461bb68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120714731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f46829530ad94dea5ccf9be815bff9c3b29f9e78cd5ee49a02f8a5cf690aef7c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:aad8b86b3a958bc07504985acedcc819faa4f1ed12ca8b46d8d94c4d564cbdfa in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["bash"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=1.8.10
# Fri, 16 Aug 2024 20:18:45 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb* # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:d82c4492ee91810a42e0c53e955a661e9a092364bc474c9db559ea5b24b7047f`  
		Last Modified: Wed, 04 Sep 2024 21:42:52 GMT  
		Size: 53.7 MB (53731619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf248fd698830ce7c74f07fb7ca6adac7bea55a16521e9e1f2afe06219e00f6`  
		Last Modified: Wed, 04 Sep 2024 22:08:56 GMT  
		Size: 15.7 MB (15749712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5139f22d8f65526bce73fabdb47a0cf930d4f9440f9bd83cf2aaa2c069d3c54`  
		Last Modified: Thu, 05 Sep 2024 12:17:52 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:625920f7e298fab2d79cf80d0c012b3bf5b07f0a48a45604b8e52568c5e04bda`  
		Last Modified: Thu, 05 Sep 2024 12:17:54 GMT  
		Size: 51.2 MB (51229894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e534a8c3450ec9794a8865e2ec1b27afa297d1fda6a96c2c54a642c11a6b6d4`  
		Last Modified: Thu, 05 Sep 2024 12:17:52 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8cad6ae7011b47b6b7f0451e661abb3920aa13ac6bdc6d711bd15381ef8a91`  
		Last Modified: Thu, 05 Sep 2024 12:17:52 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2c4b345db382001b449eda23efecb6a7bf18857b16fc649bc1ab44075024c0`  
		Last Modified: Thu, 05 Sep 2024 12:17:53 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8.10` - unknown; unknown

```console
$ docker pull influxdb@sha256:fbc84754f3650746b1687403f93dceb7610992f2a34687a8b0105b3085b11e0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4504969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0425648e1bbdf9b04fe71deff6b27568357acaa2ea37c55044cb87befbd0572c`

```dockerfile
```

-	Layers:
	-	`sha256:87a8bc3465e29c8e4e5440dbb0081fa81573865781c02b8cf91a0be19ab140a0`  
		Last Modified: Thu, 05 Sep 2024 12:17:53 GMT  
		Size: 4.5 MB (4489214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad833097f6da63d42b7bf37a73d710803f225f29e3d1bd166e24237c925a7d55`  
		Last Modified: Thu, 05 Sep 2024 12:17:52 GMT  
		Size: 15.8 KB (15755 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.8.10-alpine`

```console
$ docker pull influxdb@sha256:2601e27d6b7eac276017d7ea48d2685d52639cea974744b5877924376283a4cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.8.10-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:323bec748932cf3049bcd0ad3df03da7a85743014f37c5c06390d3dd090d5027
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59520385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c14632645a8e98cabcfa629d7f97d199afdc7b0435d24fe7c0bffcbd0925fe6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:8bf458f5fbed9f27c897506538c02fb5810b70aba850bb883d2120985fa15bac in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=1.8.10
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     chmod +x /usr/src/influxdb-*/influx              /usr/src/influxdb-*/influx_inspect              /usr/src/influxdb-*/influx_stress              /usr/src/influxdb-*/influxd &&    mv /usr/src/influxdb-*/influx        /usr/src/influxdb-*/influx_inspect        /usr/src/influxdb-*/influx_stress         /usr/src/influxdb-*/influxd        /usr/bin/ &&    gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:a0f4cbe03b6df9e61ce02b3c41bbc05481842858bd48d9687614abe719303b47`  
		Last Modified: Fri, 06 Sep 2024 22:21:07 GMT  
		Size: 3.4 MB (3392194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a63e70873dd8d18fc4e609edbcd780bf91673580b44f6778efc5cd01e91416`  
		Last Modified: Fri, 06 Sep 2024 23:21:20 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3019afc3f13df4911e2077ec99e0d88ca3cea7acca75646748dc4448363fdc6`  
		Last Modified: Fri, 06 Sep 2024 23:21:20 GMT  
		Size: 1.5 MB (1479482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40cfe8e6bcbeae6388a3e7d07db6cd1394e73cdf54ce683edbb1b7c3671a17c`  
		Last Modified: Fri, 06 Sep 2024 23:21:20 GMT  
		Size: 54.6 MB (54646714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784f4de03565d8b1d250901b03046846f5c1d470c593bd5c3659ace47f783ede`  
		Last Modified: Fri, 06 Sep 2024 23:21:20 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736622afe4eb3db6ea76fd89d7ac1d5e77d5880030d85231d501cfcbbf109518`  
		Last Modified: Fri, 06 Sep 2024 23:21:20 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85d23128f7bc1806470e05b177060a051b55e1f209ee6fbdc04ff31e2077651`  
		Last Modified: Fri, 06 Sep 2024 23:21:21 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8.10-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:bb8c66f3e48bbdf4bf837fcc1ee9679803fbe889db56efdf5357a718e9e0949c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1004063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67740208b251a99deebeae23d6c8d13b17326e8cca04cbb249627ac8460a4277`

```dockerfile
```

-	Layers:
	-	`sha256:a9272376189bcad2f11697903cbc6eccc780943ecc0445d25c1c98feb509eaf7`  
		Last Modified: Fri, 06 Sep 2024 23:21:20 GMT  
		Size: 986.7 KB (986701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58257e0baabc8dbe52d193e3864f126406b8a8ef94fcc42024004fe91365e44f`  
		Last Modified: Fri, 06 Sep 2024 23:21:20 GMT  
		Size: 17.4 KB (17362 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.9-data`

```console
$ docker pull influxdb@sha256:8af40b412b800830bd0ac3a1d3dece1b1bd94fadbfcd8a02cf4766873276fb0d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9-data` - linux; amd64

```console
$ docker pull influxdb@sha256:5bcc5cfa768f7494477c32b3e8ce6537ed497a1e0f2f9e288ff3d334c1c77abf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104138268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fc52d127e13510be5227875f12fdf0a50f996318b98903e95a5a8f56f79b7bd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:e1bdcceaa316a43ad58ce8cf054a8e89ecf5a0dbae8125eb85e9b26fdb2fca2b in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["bash"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Fri, 16 Aug 2024 20:18:45 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb* # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:ba83bbfca9443648a883d1404b33faa0f5e096a99a2b683e3bbaee8912bca845`  
		Last Modified: Wed, 04 Sep 2024 22:34:34 GMT  
		Size: 55.1 MB (55081329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e779000ed269823143d5ce9acd3ef6f6ff7465222482f7b02c10ba21f448cc`  
		Last Modified: Wed, 04 Sep 2024 23:02:18 GMT  
		Size: 15.8 MB (15764398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c57f3ebf6ba1222605ded6f31b09730aefa5a64791de44ac1a8f1919af8b3b`  
		Last Modified: Thu, 05 Sep 2024 00:07:26 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69cef328a32344daf1ce6a4c3ff73055e34985292f417495a0be34e1e141c4d7`  
		Last Modified: Thu, 05 Sep 2024 00:07:27 GMT  
		Size: 33.3 MB (33288981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b55e3689e292003f69a7094fcd35d06080fb274e02a426ff164386f1e8fd61`  
		Last Modified: Thu, 05 Sep 2024 00:07:26 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f160122f95417a46503340b7b2abfd7f5a3ffc520020927e3d83d81170165455`  
		Last Modified: Thu, 05 Sep 2024 00:07:25 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39150552d86495d3032315c32e916031fd63785fd2570da35793a58a024bdd0`  
		Last Modified: Thu, 05 Sep 2024 00:07:25 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:1613ad6a1236ef52a4a641e41e61825dca893dd55f906a6a9016f8bc9f406d24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4631024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:449b1dfda018e5c9f8920a063549c17d67aef194381b954ea14dd6a2f6fada5c`

```dockerfile
```

-	Layers:
	-	`sha256:1b880a197e5aa4f37dbc25240a7bfdf2b2d402719004575c40a2681d5d018ab6`  
		Last Modified: Thu, 05 Sep 2024 00:07:26 GMT  
		Size: 4.6 MB (4616483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3014ad4a6c1b33169ae5a1bcaad68310d2bf3ded0cea7406230740ed6d047aaa`  
		Last Modified: Thu, 05 Sep 2024 00:07:26 GMT  
		Size: 14.5 KB (14541 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.9-data-alpine`

```console
$ docker pull influxdb@sha256:8e4766170552f7235b1c95b807219c581220679cfff432ac822c633df62bc67d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:2be9c69c4dcd5b5ae85762696e710b68b9274a3ffece838c55f1c4dfd476720e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 MB (38122546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d021f63e78c0dcaf4f0c4843c08277496a2f3fa39a22064e24859434ce7570a1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:8bf458f5fbed9f27c897506538c02fb5810b70aba850bb883d2120985fa15bac in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/etc/influxdb/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:a0f4cbe03b6df9e61ce02b3c41bbc05481842858bd48d9687614abe719303b47`  
		Last Modified: Fri, 06 Sep 2024 22:21:07 GMT  
		Size: 3.4 MB (3392194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc88cdf71faaf02dcebd3cdcc8ce57a3b308c18e1848992c3aa12889d68a7301`  
		Last Modified: Fri, 06 Sep 2024 23:21:25 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f1954a31a733b8d976bc7f913379f93944a904187dada2925e7b3cdbabc0f5`  
		Last Modified: Fri, 06 Sep 2024 23:21:25 GMT  
		Size: 1.5 MB (1479490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea04e3b2c5bbeec39091ab366a332265cf6a1fcd0a00a3d955795bfbdefdf86b`  
		Last Modified: Fri, 06 Sep 2024 23:21:25 GMT  
		Size: 33.2 MB (33248810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31752a5b6441ca3f6fbf58a13a9df69554b08cd5a0a98b42b9af86bd91bae722`  
		Last Modified: Fri, 06 Sep 2024 23:21:25 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e28722e5f3c56298697a4b05f52f60035c8581bfc3598ce2fcf490278b3e4fa`  
		Last Modified: Fri, 06 Sep 2024 23:21:26 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a27e41d4bb82b0a46cee7d7b7054ea092e52fb02cf0c3620e2cdf32e0038ca`  
		Last Modified: Fri, 06 Sep 2024 23:21:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:52997d7d8ef387e2e2bf5593c589b466eae768552b84efa1547cdb8ce44616e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1137829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baab96e09494545e50ecde071d196cb1a9b8250cb52b0d169702e169b2c85bb1`

```dockerfile
```

-	Layers:
	-	`sha256:1781d7e34c0831e0d91185e04c6d0e841144d3fdfcfe61991f8e8c86ba334130`  
		Last Modified: Fri, 06 Sep 2024 23:21:25 GMT  
		Size: 1.1 MB (1121383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1d27a2c65fe763ea61971a95d715655cd32f3bcf319da8dabb4f1900c2e7056`  
		Last Modified: Fri, 06 Sep 2024 23:21:25 GMT  
		Size: 16.4 KB (16446 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.9-meta`

```console
$ docker pull influxdb@sha256:6da2f7485452466d64f8c1416afa97f61854918093d228e374648daa1bce9316
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:75c38bfc4c80b4037aef703085265fb9b8bafc695606ec594b05ad674f5e96da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83617428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86131929d77352207b5468b18b585feec41be6348039b53c2de2b8305f1eab8f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:e1bdcceaa316a43ad58ce8cf054a8e89ecf5a0dbae8125eb85e9b26fdb2fca2b in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["bash"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Fri, 16 Aug 2024 20:18:45 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb* # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8091/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:ba83bbfca9443648a883d1404b33faa0f5e096a99a2b683e3bbaee8912bca845`  
		Last Modified: Wed, 04 Sep 2024 22:34:34 GMT  
		Size: 55.1 MB (55081329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e779000ed269823143d5ce9acd3ef6f6ff7465222482f7b02c10ba21f448cc`  
		Last Modified: Wed, 04 Sep 2024 23:02:18 GMT  
		Size: 15.8 MB (15764398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d113da3afe194834e8e9c0f598bd48d1bea5e6e99f3b775b928be7b49f3b920`  
		Last Modified: Thu, 05 Sep 2024 00:07:15 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:456317fca70518e1239de9cc655f5cb8908b9a5b0aafa9524201108a3d24054d`  
		Last Modified: Thu, 05 Sep 2024 00:07:15 GMT  
		Size: 12.8 MB (12769364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be781808d513db32bb1996165399b7b847f9d9e726e43eebf1aa231b6347246`  
		Last Modified: Thu, 05 Sep 2024 00:07:15 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3bc9d07a61c8bacf82c41e1af5473bf189d057e7af34038aa286d6f1dfd397`  
		Last Modified: Thu, 05 Sep 2024 00:07:16 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:a8dfb0f1b65372f671f6eeb4415896aa643c6aa784cdb93c7887a52ccbd35dbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4565204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8073f4b937990dc70bf227487dff0a5538e99674974fd3d066cc42747ec06e73`

```dockerfile
```

-	Layers:
	-	`sha256:aef63a94272522c380ec0a71a7645b7829d2e989c0f62ec5344dc3679cf2fa0d`  
		Last Modified: Thu, 05 Sep 2024 00:07:15 GMT  
		Size: 4.6 MB (4552316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0c54073bdeff22ff9ae968cdb1a5f41c19458dc0ea0898e10167080bac25931`  
		Last Modified: Thu, 05 Sep 2024 00:07:15 GMT  
		Size: 12.9 KB (12888 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.9-meta-alpine`

```console
$ docker pull influxdb@sha256:4d3a9c68cfc5211e9079595580408c93af827777d33bf0f66a34a87c0966a03f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:e4d7f35c0a96a009bc919f98118cf471c253e54c5dd47ff14ab4fd80b86e4c81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17569067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e77bc62f618fb464838b1d92de778a70e3072262f06ecd84f96c4073d5898eb3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/etc/influxdb/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8091/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:020562199c64aad524deae5d3ab9ce90e8b6cd8a2f2efa68dc89be44c4bbbcb0`  
		Last Modified: Fri, 06 Sep 2024 23:21:34 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164109d9ed866529603429a063011bb370e035ba2582d27646c7d720dc703e70`  
		Last Modified: Fri, 06 Sep 2024 23:21:34 GMT  
		Size: 1.2 MB (1223701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2001df372492d0f10ab280222c05f3d766032e54ebdbb87c17e1c55489fbcf8`  
		Last Modified: Fri, 06 Sep 2024 23:21:34 GMT  
		Size: 12.7 MB (12720713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0680dcab1180b67227ca80095a9b3b636c0182c7d8df7c911b8b8f2a097e3456`  
		Last Modified: Fri, 06 Sep 2024 23:21:34 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8044a8f410b1af2cb55de0e9463e0da9482b826ed89980872400a29373ad7145`  
		Last Modified: Fri, 06 Sep 2024 23:21:35 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:e4ec93149fe8e573bc5b6cdfbd1476c21c497f6b34a54badf6e7addaf3b882ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **693.0 KB (692992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a56585d872141e680b91773c695f6dc007ef5b4ade58ae79965a0d351dcd95`

```dockerfile
```

-	Layers:
	-	`sha256:b6d1ec9d01fb7b59c9c9d2c5998b0930a3b42d3648164bb5573ae0fc0cf64fa8`  
		Last Modified: Fri, 06 Sep 2024 23:21:34 GMT  
		Size: 678.2 KB (678179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03a4e5534447245d871a73fce3f69e717a88c925647a19d9bfabd1b57d1b5e69`  
		Last Modified: Fri, 06 Sep 2024 23:21:34 GMT  
		Size: 14.8 KB (14813 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.9.13-data`

```console
$ docker pull influxdb@sha256:8af40b412b800830bd0ac3a1d3dece1b1bd94fadbfcd8a02cf4766873276fb0d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9.13-data` - linux; amd64

```console
$ docker pull influxdb@sha256:5bcc5cfa768f7494477c32b3e8ce6537ed497a1e0f2f9e288ff3d334c1c77abf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104138268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fc52d127e13510be5227875f12fdf0a50f996318b98903e95a5a8f56f79b7bd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:e1bdcceaa316a43ad58ce8cf054a8e89ecf5a0dbae8125eb85e9b26fdb2fca2b in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["bash"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Fri, 16 Aug 2024 20:18:45 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb* # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:ba83bbfca9443648a883d1404b33faa0f5e096a99a2b683e3bbaee8912bca845`  
		Last Modified: Wed, 04 Sep 2024 22:34:34 GMT  
		Size: 55.1 MB (55081329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e779000ed269823143d5ce9acd3ef6f6ff7465222482f7b02c10ba21f448cc`  
		Last Modified: Wed, 04 Sep 2024 23:02:18 GMT  
		Size: 15.8 MB (15764398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c57f3ebf6ba1222605ded6f31b09730aefa5a64791de44ac1a8f1919af8b3b`  
		Last Modified: Thu, 05 Sep 2024 00:07:26 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69cef328a32344daf1ce6a4c3ff73055e34985292f417495a0be34e1e141c4d7`  
		Last Modified: Thu, 05 Sep 2024 00:07:27 GMT  
		Size: 33.3 MB (33288981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b55e3689e292003f69a7094fcd35d06080fb274e02a426ff164386f1e8fd61`  
		Last Modified: Thu, 05 Sep 2024 00:07:26 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f160122f95417a46503340b7b2abfd7f5a3ffc520020927e3d83d81170165455`  
		Last Modified: Thu, 05 Sep 2024 00:07:25 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39150552d86495d3032315c32e916031fd63785fd2570da35793a58a024bdd0`  
		Last Modified: Thu, 05 Sep 2024 00:07:25 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9.13-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:1613ad6a1236ef52a4a641e41e61825dca893dd55f906a6a9016f8bc9f406d24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4631024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:449b1dfda018e5c9f8920a063549c17d67aef194381b954ea14dd6a2f6fada5c`

```dockerfile
```

-	Layers:
	-	`sha256:1b880a197e5aa4f37dbc25240a7bfdf2b2d402719004575c40a2681d5d018ab6`  
		Last Modified: Thu, 05 Sep 2024 00:07:26 GMT  
		Size: 4.6 MB (4616483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3014ad4a6c1b33169ae5a1bcaad68310d2bf3ded0cea7406230740ed6d047aaa`  
		Last Modified: Thu, 05 Sep 2024 00:07:26 GMT  
		Size: 14.5 KB (14541 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.9.13-data-alpine`

```console
$ docker pull influxdb@sha256:8e4766170552f7235b1c95b807219c581220679cfff432ac822c633df62bc67d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9.13-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:2be9c69c4dcd5b5ae85762696e710b68b9274a3ffece838c55f1c4dfd476720e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 MB (38122546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d021f63e78c0dcaf4f0c4843c08277496a2f3fa39a22064e24859434ce7570a1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:8bf458f5fbed9f27c897506538c02fb5810b70aba850bb883d2120985fa15bac in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/etc/influxdb/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:a0f4cbe03b6df9e61ce02b3c41bbc05481842858bd48d9687614abe719303b47`  
		Last Modified: Fri, 06 Sep 2024 22:21:07 GMT  
		Size: 3.4 MB (3392194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc88cdf71faaf02dcebd3cdcc8ce57a3b308c18e1848992c3aa12889d68a7301`  
		Last Modified: Fri, 06 Sep 2024 23:21:25 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f1954a31a733b8d976bc7f913379f93944a904187dada2925e7b3cdbabc0f5`  
		Last Modified: Fri, 06 Sep 2024 23:21:25 GMT  
		Size: 1.5 MB (1479490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea04e3b2c5bbeec39091ab366a332265cf6a1fcd0a00a3d955795bfbdefdf86b`  
		Last Modified: Fri, 06 Sep 2024 23:21:25 GMT  
		Size: 33.2 MB (33248810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31752a5b6441ca3f6fbf58a13a9df69554b08cd5a0a98b42b9af86bd91bae722`  
		Last Modified: Fri, 06 Sep 2024 23:21:25 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e28722e5f3c56298697a4b05f52f60035c8581bfc3598ce2fcf490278b3e4fa`  
		Last Modified: Fri, 06 Sep 2024 23:21:26 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a27e41d4bb82b0a46cee7d7b7054ea092e52fb02cf0c3620e2cdf32e0038ca`  
		Last Modified: Fri, 06 Sep 2024 23:21:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9.13-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:52997d7d8ef387e2e2bf5593c589b466eae768552b84efa1547cdb8ce44616e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1137829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baab96e09494545e50ecde071d196cb1a9b8250cb52b0d169702e169b2c85bb1`

```dockerfile
```

-	Layers:
	-	`sha256:1781d7e34c0831e0d91185e04c6d0e841144d3fdfcfe61991f8e8c86ba334130`  
		Last Modified: Fri, 06 Sep 2024 23:21:25 GMT  
		Size: 1.1 MB (1121383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1d27a2c65fe763ea61971a95d715655cd32f3bcf319da8dabb4f1900c2e7056`  
		Last Modified: Fri, 06 Sep 2024 23:21:25 GMT  
		Size: 16.4 KB (16446 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.9.13-meta`

```console
$ docker pull influxdb@sha256:6da2f7485452466d64f8c1416afa97f61854918093d228e374648daa1bce9316
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9.13-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:75c38bfc4c80b4037aef703085265fb9b8bafc695606ec594b05ad674f5e96da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83617428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86131929d77352207b5468b18b585feec41be6348039b53c2de2b8305f1eab8f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:e1bdcceaa316a43ad58ce8cf054a8e89ecf5a0dbae8125eb85e9b26fdb2fca2b in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["bash"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Fri, 16 Aug 2024 20:18:45 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb* # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8091/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:ba83bbfca9443648a883d1404b33faa0f5e096a99a2b683e3bbaee8912bca845`  
		Last Modified: Wed, 04 Sep 2024 22:34:34 GMT  
		Size: 55.1 MB (55081329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e779000ed269823143d5ce9acd3ef6f6ff7465222482f7b02c10ba21f448cc`  
		Last Modified: Wed, 04 Sep 2024 23:02:18 GMT  
		Size: 15.8 MB (15764398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d113da3afe194834e8e9c0f598bd48d1bea5e6e99f3b775b928be7b49f3b920`  
		Last Modified: Thu, 05 Sep 2024 00:07:15 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:456317fca70518e1239de9cc655f5cb8908b9a5b0aafa9524201108a3d24054d`  
		Last Modified: Thu, 05 Sep 2024 00:07:15 GMT  
		Size: 12.8 MB (12769364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be781808d513db32bb1996165399b7b847f9d9e726e43eebf1aa231b6347246`  
		Last Modified: Thu, 05 Sep 2024 00:07:15 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3bc9d07a61c8bacf82c41e1af5473bf189d057e7af34038aa286d6f1dfd397`  
		Last Modified: Thu, 05 Sep 2024 00:07:16 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9.13-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:a8dfb0f1b65372f671f6eeb4415896aa643c6aa784cdb93c7887a52ccbd35dbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4565204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8073f4b937990dc70bf227487dff0a5538e99674974fd3d066cc42747ec06e73`

```dockerfile
```

-	Layers:
	-	`sha256:aef63a94272522c380ec0a71a7645b7829d2e989c0f62ec5344dc3679cf2fa0d`  
		Last Modified: Thu, 05 Sep 2024 00:07:15 GMT  
		Size: 4.6 MB (4552316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0c54073bdeff22ff9ae968cdb1a5f41c19458dc0ea0898e10167080bac25931`  
		Last Modified: Thu, 05 Sep 2024 00:07:15 GMT  
		Size: 12.9 KB (12888 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.9.13-meta-alpine`

```console
$ docker pull influxdb@sha256:4d3a9c68cfc5211e9079595580408c93af827777d33bf0f66a34a87c0966a03f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9.13-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:e4d7f35c0a96a009bc919f98118cf471c253e54c5dd47ff14ab4fd80b86e4c81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17569067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e77bc62f618fb464838b1d92de778a70e3072262f06ecd84f96c4073d5898eb3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/etc/influxdb/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8091/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:020562199c64aad524deae5d3ab9ce90e8b6cd8a2f2efa68dc89be44c4bbbcb0`  
		Last Modified: Fri, 06 Sep 2024 23:21:34 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164109d9ed866529603429a063011bb370e035ba2582d27646c7d720dc703e70`  
		Last Modified: Fri, 06 Sep 2024 23:21:34 GMT  
		Size: 1.2 MB (1223701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2001df372492d0f10ab280222c05f3d766032e54ebdbb87c17e1c55489fbcf8`  
		Last Modified: Fri, 06 Sep 2024 23:21:34 GMT  
		Size: 12.7 MB (12720713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0680dcab1180b67227ca80095a9b3b636c0182c7d8df7c911b8b8f2a097e3456`  
		Last Modified: Fri, 06 Sep 2024 23:21:34 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8044a8f410b1af2cb55de0e9463e0da9482b826ed89980872400a29373ad7145`  
		Last Modified: Fri, 06 Sep 2024 23:21:35 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9.13-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:e4ec93149fe8e573bc5b6cdfbd1476c21c497f6b34a54badf6e7addaf3b882ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **693.0 KB (692992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a56585d872141e680b91773c695f6dc007ef5b4ade58ae79965a0d351dcd95`

```dockerfile
```

-	Layers:
	-	`sha256:b6d1ec9d01fb7b59c9c9d2c5998b0930a3b42d3648164bb5573ae0fc0cf64fa8`  
		Last Modified: Fri, 06 Sep 2024 23:21:34 GMT  
		Size: 678.2 KB (678179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03a4e5534447245d871a73fce3f69e717a88c925647a19d9bfabd1b57d1b5e69`  
		Last Modified: Fri, 06 Sep 2024 23:21:34 GMT  
		Size: 14.8 KB (14813 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2`

```console
$ docker pull influxdb@sha256:b59864431e6f10a40aeb1040d4e11114c86ec8ec900926ee4d88cee8b89d20e7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2` - linux; amd64

```console
$ docker pull influxdb@sha256:565fd3432b668a2fea119e9d2d7e857c49688af708aafb30cb5c6476b8d73e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168475058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82765bab090017edb2e03a187c5668f5f9048b52efb857d458521dd5774160b2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["bash"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV GOSU_VER=1.16
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=2.7.10
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 16 Aug 2024 20:18:45 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477705850a3a7f5f03e5d6a1a59a0dcfa91b94206e39a56cc6948133bfeee20c`  
		Last Modified: Wed, 04 Sep 2024 23:10:04 GMT  
		Size: 9.8 MB (9788950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb97151d37e4aa70aa077f6162a9890304784966c35ba5d3af11f1def2b263fd`  
		Last Modified: Wed, 04 Sep 2024 23:10:04 GMT  
		Size: 5.8 MB (5820938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f3fc2b91f4c45426d08bb4e1a3cbf12c856cfed711e1d43c65f2cc105cc256`  
		Last Modified: Wed, 04 Sep 2024 23:10:04 GMT  
		Size: 3.2 KB (3226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389c37eac14d118b3cb70b72e1f477a24c4986b26ade1960b57d552bbcd57f19`  
		Last Modified: Wed, 04 Sep 2024 23:10:04 GMT  
		Size: 1.0 MB (1006368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd854556873c80b5145bf59213db12c5417313e31ecb8190690ce1899737ad10`  
		Last Modified: Wed, 04 Sep 2024 23:10:07 GMT  
		Size: 99.6 MB (99594066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ae1439b7721fdeded51a74c06d4911e5aa66f9c6de27df9df050d64d194d56`  
		Last Modified: Wed, 04 Sep 2024 23:10:05 GMT  
		Size: 23.1 MB (23128301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81be0a7f65a5159ce17c6a5c844f578c79cdc48d004173b15b6fe6ed6b225dd1`  
		Last Modified: Wed, 04 Sep 2024 23:10:06 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af8f8db7d47ab30ae652279949643449f0f4722ac4e8f0a6bfcbeccf6a54b12`  
		Last Modified: Wed, 04 Sep 2024 23:10:05 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65fc8982233fe665574473fa1c2f285de2428e3ce74a9d595f6ae0744bbcbdb0`  
		Last Modified: Wed, 04 Sep 2024 23:10:06 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:67c55d73c97a06ccd1f33b9623748a63f4bcd3bf5b9a466699b240eaa03a716f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de69f4b4f8604f2c94d486d1b0a00fa53c547ab5de99010a8578be79610d1673`

```dockerfile
```

-	Layers:
	-	`sha256:af7960aa38e90d8826134f7591e3b020c58f42468d23e5ab3ff2a5edca9bea22`  
		Last Modified: Wed, 04 Sep 2024 23:10:04 GMT  
		Size: 2.8 MB (2833443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35599651b4f0cdc382b9c7d513b3fd5e35824e7a6c12b885cbf120268e730a08`  
		Last Modified: Wed, 04 Sep 2024 23:10:04 GMT  
		Size: 33.5 KB (33545 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:0dee8c333792bdf4ae8bb45f90c537f93c93ead6c0746c991dbfbcbbcc9291f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.2 MB (162243946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3397d79b74503e0df0a037eb63b3d6eaca40d36a99d570483cafe6d5552cbfc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["bash"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV GOSU_VER=1.16
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=2.7.10
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 16 Aug 2024 20:18:45 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3788f6761354a8e34c9dee5aa1c5e266c9f7fb192ee67465d0b3381a6675dadd`  
		Last Modified: Thu, 05 Sep 2024 12:18:43 GMT  
		Size: 9.6 MB (9587108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607ee39df12476d4788e3aa8305639d96df0197a9826a2088f03b89ba769e349`  
		Last Modified: Thu, 05 Sep 2024 12:18:43 GMT  
		Size: 5.5 MB (5463801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d90eb06433b93420b11b1d6a090d6866dd1a61d72d8742b786199b56c20a09d`  
		Last Modified: Thu, 05 Sep 2024 12:18:42 GMT  
		Size: 3.2 KB (3226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bb7b9bd024f3c163fc1ec8c85baa5a0ecaaa6bf6e4fcc1705854b855a5bd73`  
		Last Modified: Thu, 05 Sep 2024 12:18:43 GMT  
		Size: 936.1 KB (936105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26df1b491b2829e3c2a79bf79ef065f479659639c8c6bcef909c5a0521a16963`  
		Last Modified: Thu, 05 Sep 2024 12:18:46 GMT  
		Size: 95.4 MB (95427914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67aef66159039be0863ad28aa66d7317c2af5505d5c9e89b4f5b799bb764cd04`  
		Last Modified: Thu, 05 Sep 2024 12:18:45 GMT  
		Size: 21.7 MB (21662519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2e701aaea336fdc9d97cb2ead500046df05e86c131199ad1ca8e67350a44c2`  
		Last Modified: Thu, 05 Sep 2024 12:18:44 GMT  
		Size: 207.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38bb9310aa18b0e075b702b3ef35d26ab7e0a2e66d526b5a1708577f6ffcc987`  
		Last Modified: Thu, 05 Sep 2024 12:18:44 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf751defaf44888faf018dfcc83f5490a231ce314117a56b7e25e985656cd86`  
		Last Modified: Thu, 05 Sep 2024 12:18:45 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:8bfe01d8dca857195cc81d6e1e452a5c8270cd1146a53cd47a948ed3c5a20c74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9488a1be5ce1441c26e77352b52a7ea839cabba20629d4560c4308f1ffe16c4`

```dockerfile
```

-	Layers:
	-	`sha256:a7b7f386f124d2d793ad5f4c9b797a20074563fdfb8b7b393b7dbf6a9f96c640`  
		Last Modified: Thu, 05 Sep 2024 12:18:43 GMT  
		Size: 2.8 MB (2832680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa9da7ba1e0fb5f1af48ead53d074eb281f5a557cfccb02b51cd097d034edcee`  
		Last Modified: Thu, 05 Sep 2024 12:18:42 GMT  
		Size: 33.8 KB (33848 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2-alpine`

```console
$ docker pull influxdb@sha256:327be0243a329b1da350a37c1468d756f4258330d50d10a2a993e5bb9a6e3d2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:cac47619d57d832e6a0f787362eba5b3e1f36629afd0e2e843e066b35151e380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (92006098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6a7f3befda36a7f068f8339e56f8f59f6e527333e161482eae1d0df560e75c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=2.7.10
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 16 Aug 2024 20:18:45 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078166243ebe0c2b9c91a2f7e164076218c7716b68301080fac2f19f177dd096`  
		Last Modified: Fri, 06 Sep 2024 23:21:35 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1587bf1467bd7fa0cc2b3706d4443a35b49f61bd49b1290f081643d747c38c`  
		Last Modified: Fri, 06 Sep 2024 23:21:40 GMT  
		Size: 9.6 MB (9634631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed395597bc0621a59fd604631b8c292c382b858b04d465c184da49759e54a5f2`  
		Last Modified: Fri, 06 Sep 2024 23:21:40 GMT  
		Size: 5.8 MB (5820945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d0f5c43f5e203308ab55d4d25d6adedc07ff5e1ae398853254c3b438bbf159`  
		Last Modified: Fri, 06 Sep 2024 23:21:39 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050deb0e5ac12402242203b9a1622d17bb64075b547efbbd845bec1f2a228b3f`  
		Last Modified: Fri, 06 Sep 2024 23:21:41 GMT  
		Size: 49.8 MB (49790466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84be9b15369ef3c36eb630297dc094d0685e0b0b896139448712012f1770e988`  
		Last Modified: Fri, 06 Sep 2024 23:21:41 GMT  
		Size: 23.1 MB (23128284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64fac09c6feb55954579c03c8eb95a176fa4466a843ffd0bff0f34285b16fff`  
		Last Modified: Fri, 06 Sep 2024 23:21:40 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc407c5347f2647cdac2b45ee7c93f275e3b7b3ae212b1ef9aa98d85bcde01a2`  
		Last Modified: Fri, 06 Sep 2024 23:21:41 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd950ffb540d8825efa00e5972a9aa81a31adcd1b9c6350cac0788e1a18392f2`  
		Last Modified: Fri, 06 Sep 2024 23:21:41 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:acbb7b79cd5c3b0c183013df9776032eb14bb163e9eb2b3becd90c70b47a0c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.8 KB (944845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b3b3774810f57f3371aa23eaffa51ffbdc41e5b074a7c7e3ab902304cffe58`

```dockerfile
```

-	Layers:
	-	`sha256:5c072ab20e36c5f3b5b02ca06364a72e79aad9b7562f55eacf3460ebc071a8ed`  
		Last Modified: Fri, 06 Sep 2024 23:21:39 GMT  
		Size: 914.1 KB (914093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b689f3cda8aaa0b6667d6a4d53280e261fa5922f2272a2269832f1b17f8711f`  
		Last Modified: Fri, 06 Sep 2024 23:21:39 GMT  
		Size: 30.8 KB (30752 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:1000811b02d8b6fdb75ea723c4e9c33746c27e6d0be65a84b9152ecc28fb0f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88688483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feba5f301346b7e3cba9218b3a9b5ae318b06386a0b000e04c7dab92f1576f5a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=2.7.10
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 16 Aug 2024 20:18:45 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e4b70a44519145916f8803166c99c3ba52ea4bf109ad21b6d3e97aaa6f17a6`  
		Last Modified: Sat, 07 Sep 2024 05:27:19 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9713c4c4a81b87a3373d8e7be5320c3cc5cc86ad74b6c2a3b331c3be04d8cac`  
		Last Modified: Sat, 07 Sep 2024 05:27:20 GMT  
		Size: 9.8 MB (9757048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbef7f92137af9c8d8b2ceb13c99138a68cd759251cc1d5e407ff11e6bd9db8`  
		Last Modified: Sat, 07 Sep 2024 05:27:19 GMT  
		Size: 5.5 MB (5463803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7a1f6a4d13197b794b1cec6c7f7160c8d5a86013ec29ba75ac7fb7cd7dda19`  
		Last Modified: Sat, 07 Sep 2024 05:27:19 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a928a7eba1ff5a21c666fa39ef8dade819caf6ce52010688b7d5b2d950456277`  
		Last Modified: Sat, 07 Sep 2024 05:27:22 GMT  
		Size: 47.7 MB (47709505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2432c5f0597753c705d3724184b3356815256a64a8c93aa3781d2e785593ce7`  
		Last Modified: Sat, 07 Sep 2024 05:27:21 GMT  
		Size: 21.7 MB (21662516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5933260cd0024e114bab17baef98e72aa06083573baa234ae705402c874b1a6e`  
		Last Modified: Sat, 07 Sep 2024 05:27:21 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343fdf5a00e872d5be68ab0f1f4c181170fb92a665999710b3589a2f80b8354b`  
		Last Modified: Sat, 07 Sep 2024 05:27:21 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c614e03155dfd058b554c17f6b42e3fa4eddd5938d80ec113ef5ea4e07bc045a`  
		Last Modified: Sat, 07 Sep 2024 05:27:21 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:fd0b50cc9671d0a3aded8e829d944212c24854b17ce177492fdd78e3c85adbca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.4 KB (944406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c436daff587bcef14431aa15b0a39ef47994bc66d9a0353450d30a519c01ad27`

```dockerfile
```

-	Layers:
	-	`sha256:ca5611f32d0ac5d978cefb8dc3b90ae6bfae5a67b19d2f2bdc02d6c9000569a7`  
		Last Modified: Sat, 07 Sep 2024 05:27:19 GMT  
		Size: 913.4 KB (913354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e00d02321e4e44e7c735484a05227ce7d6b07e76a212b03bf5b22f30d7ee3d3`  
		Last Modified: Sat, 07 Sep 2024 05:27:19 GMT  
		Size: 31.1 KB (31052 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7`

```console
$ docker pull influxdb@sha256:b59864431e6f10a40aeb1040d4e11114c86ec8ec900926ee4d88cee8b89d20e7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7` - linux; amd64

```console
$ docker pull influxdb@sha256:565fd3432b668a2fea119e9d2d7e857c49688af708aafb30cb5c6476b8d73e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168475058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82765bab090017edb2e03a187c5668f5f9048b52efb857d458521dd5774160b2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["bash"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV GOSU_VER=1.16
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=2.7.10
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 16 Aug 2024 20:18:45 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477705850a3a7f5f03e5d6a1a59a0dcfa91b94206e39a56cc6948133bfeee20c`  
		Last Modified: Wed, 04 Sep 2024 23:10:04 GMT  
		Size: 9.8 MB (9788950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb97151d37e4aa70aa077f6162a9890304784966c35ba5d3af11f1def2b263fd`  
		Last Modified: Wed, 04 Sep 2024 23:10:04 GMT  
		Size: 5.8 MB (5820938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f3fc2b91f4c45426d08bb4e1a3cbf12c856cfed711e1d43c65f2cc105cc256`  
		Last Modified: Wed, 04 Sep 2024 23:10:04 GMT  
		Size: 3.2 KB (3226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389c37eac14d118b3cb70b72e1f477a24c4986b26ade1960b57d552bbcd57f19`  
		Last Modified: Wed, 04 Sep 2024 23:10:04 GMT  
		Size: 1.0 MB (1006368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd854556873c80b5145bf59213db12c5417313e31ecb8190690ce1899737ad10`  
		Last Modified: Wed, 04 Sep 2024 23:10:07 GMT  
		Size: 99.6 MB (99594066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ae1439b7721fdeded51a74c06d4911e5aa66f9c6de27df9df050d64d194d56`  
		Last Modified: Wed, 04 Sep 2024 23:10:05 GMT  
		Size: 23.1 MB (23128301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81be0a7f65a5159ce17c6a5c844f578c79cdc48d004173b15b6fe6ed6b225dd1`  
		Last Modified: Wed, 04 Sep 2024 23:10:06 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af8f8db7d47ab30ae652279949643449f0f4722ac4e8f0a6bfcbeccf6a54b12`  
		Last Modified: Wed, 04 Sep 2024 23:10:05 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65fc8982233fe665574473fa1c2f285de2428e3ce74a9d595f6ae0744bbcbdb0`  
		Last Modified: Wed, 04 Sep 2024 23:10:06 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:67c55d73c97a06ccd1f33b9623748a63f4bcd3bf5b9a466699b240eaa03a716f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de69f4b4f8604f2c94d486d1b0a00fa53c547ab5de99010a8578be79610d1673`

```dockerfile
```

-	Layers:
	-	`sha256:af7960aa38e90d8826134f7591e3b020c58f42468d23e5ab3ff2a5edca9bea22`  
		Last Modified: Wed, 04 Sep 2024 23:10:04 GMT  
		Size: 2.8 MB (2833443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35599651b4f0cdc382b9c7d513b3fd5e35824e7a6c12b885cbf120268e730a08`  
		Last Modified: Wed, 04 Sep 2024 23:10:04 GMT  
		Size: 33.5 KB (33545 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:0dee8c333792bdf4ae8bb45f90c537f93c93ead6c0746c991dbfbcbbcc9291f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.2 MB (162243946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3397d79b74503e0df0a037eb63b3d6eaca40d36a99d570483cafe6d5552cbfc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["bash"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV GOSU_VER=1.16
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=2.7.10
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 16 Aug 2024 20:18:45 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3788f6761354a8e34c9dee5aa1c5e266c9f7fb192ee67465d0b3381a6675dadd`  
		Last Modified: Thu, 05 Sep 2024 12:18:43 GMT  
		Size: 9.6 MB (9587108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607ee39df12476d4788e3aa8305639d96df0197a9826a2088f03b89ba769e349`  
		Last Modified: Thu, 05 Sep 2024 12:18:43 GMT  
		Size: 5.5 MB (5463801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d90eb06433b93420b11b1d6a090d6866dd1a61d72d8742b786199b56c20a09d`  
		Last Modified: Thu, 05 Sep 2024 12:18:42 GMT  
		Size: 3.2 KB (3226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bb7b9bd024f3c163fc1ec8c85baa5a0ecaaa6bf6e4fcc1705854b855a5bd73`  
		Last Modified: Thu, 05 Sep 2024 12:18:43 GMT  
		Size: 936.1 KB (936105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26df1b491b2829e3c2a79bf79ef065f479659639c8c6bcef909c5a0521a16963`  
		Last Modified: Thu, 05 Sep 2024 12:18:46 GMT  
		Size: 95.4 MB (95427914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67aef66159039be0863ad28aa66d7317c2af5505d5c9e89b4f5b799bb764cd04`  
		Last Modified: Thu, 05 Sep 2024 12:18:45 GMT  
		Size: 21.7 MB (21662519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2e701aaea336fdc9d97cb2ead500046df05e86c131199ad1ca8e67350a44c2`  
		Last Modified: Thu, 05 Sep 2024 12:18:44 GMT  
		Size: 207.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38bb9310aa18b0e075b702b3ef35d26ab7e0a2e66d526b5a1708577f6ffcc987`  
		Last Modified: Thu, 05 Sep 2024 12:18:44 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf751defaf44888faf018dfcc83f5490a231ce314117a56b7e25e985656cd86`  
		Last Modified: Thu, 05 Sep 2024 12:18:45 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:8bfe01d8dca857195cc81d6e1e452a5c8270cd1146a53cd47a948ed3c5a20c74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9488a1be5ce1441c26e77352b52a7ea839cabba20629d4560c4308f1ffe16c4`

```dockerfile
```

-	Layers:
	-	`sha256:a7b7f386f124d2d793ad5f4c9b797a20074563fdfb8b7b393b7dbf6a9f96c640`  
		Last Modified: Thu, 05 Sep 2024 12:18:43 GMT  
		Size: 2.8 MB (2832680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa9da7ba1e0fb5f1af48ead53d074eb281f5a557cfccb02b51cd097d034edcee`  
		Last Modified: Thu, 05 Sep 2024 12:18:42 GMT  
		Size: 33.8 KB (33848 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7-alpine`

```console
$ docker pull influxdb@sha256:327be0243a329b1da350a37c1468d756f4258330d50d10a2a993e5bb9a6e3d2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:cac47619d57d832e6a0f787362eba5b3e1f36629afd0e2e843e066b35151e380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (92006098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6a7f3befda36a7f068f8339e56f8f59f6e527333e161482eae1d0df560e75c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=2.7.10
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 16 Aug 2024 20:18:45 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078166243ebe0c2b9c91a2f7e164076218c7716b68301080fac2f19f177dd096`  
		Last Modified: Fri, 06 Sep 2024 23:21:35 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1587bf1467bd7fa0cc2b3706d4443a35b49f61bd49b1290f081643d747c38c`  
		Last Modified: Fri, 06 Sep 2024 23:21:40 GMT  
		Size: 9.6 MB (9634631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed395597bc0621a59fd604631b8c292c382b858b04d465c184da49759e54a5f2`  
		Last Modified: Fri, 06 Sep 2024 23:21:40 GMT  
		Size: 5.8 MB (5820945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d0f5c43f5e203308ab55d4d25d6adedc07ff5e1ae398853254c3b438bbf159`  
		Last Modified: Fri, 06 Sep 2024 23:21:39 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050deb0e5ac12402242203b9a1622d17bb64075b547efbbd845bec1f2a228b3f`  
		Last Modified: Fri, 06 Sep 2024 23:21:41 GMT  
		Size: 49.8 MB (49790466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84be9b15369ef3c36eb630297dc094d0685e0b0b896139448712012f1770e988`  
		Last Modified: Fri, 06 Sep 2024 23:21:41 GMT  
		Size: 23.1 MB (23128284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64fac09c6feb55954579c03c8eb95a176fa4466a843ffd0bff0f34285b16fff`  
		Last Modified: Fri, 06 Sep 2024 23:21:40 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc407c5347f2647cdac2b45ee7c93f275e3b7b3ae212b1ef9aa98d85bcde01a2`  
		Last Modified: Fri, 06 Sep 2024 23:21:41 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd950ffb540d8825efa00e5972a9aa81a31adcd1b9c6350cac0788e1a18392f2`  
		Last Modified: Fri, 06 Sep 2024 23:21:41 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:acbb7b79cd5c3b0c183013df9776032eb14bb163e9eb2b3becd90c70b47a0c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.8 KB (944845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b3b3774810f57f3371aa23eaffa51ffbdc41e5b074a7c7e3ab902304cffe58`

```dockerfile
```

-	Layers:
	-	`sha256:5c072ab20e36c5f3b5b02ca06364a72e79aad9b7562f55eacf3460ebc071a8ed`  
		Last Modified: Fri, 06 Sep 2024 23:21:39 GMT  
		Size: 914.1 KB (914093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b689f3cda8aaa0b6667d6a4d53280e261fa5922f2272a2269832f1b17f8711f`  
		Last Modified: Fri, 06 Sep 2024 23:21:39 GMT  
		Size: 30.8 KB (30752 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:1000811b02d8b6fdb75ea723c4e9c33746c27e6d0be65a84b9152ecc28fb0f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88688483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feba5f301346b7e3cba9218b3a9b5ae318b06386a0b000e04c7dab92f1576f5a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=2.7.10
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 16 Aug 2024 20:18:45 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e4b70a44519145916f8803166c99c3ba52ea4bf109ad21b6d3e97aaa6f17a6`  
		Last Modified: Sat, 07 Sep 2024 05:27:19 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9713c4c4a81b87a3373d8e7be5320c3cc5cc86ad74b6c2a3b331c3be04d8cac`  
		Last Modified: Sat, 07 Sep 2024 05:27:20 GMT  
		Size: 9.8 MB (9757048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbef7f92137af9c8d8b2ceb13c99138a68cd759251cc1d5e407ff11e6bd9db8`  
		Last Modified: Sat, 07 Sep 2024 05:27:19 GMT  
		Size: 5.5 MB (5463803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7a1f6a4d13197b794b1cec6c7f7160c8d5a86013ec29ba75ac7fb7cd7dda19`  
		Last Modified: Sat, 07 Sep 2024 05:27:19 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a928a7eba1ff5a21c666fa39ef8dade819caf6ce52010688b7d5b2d950456277`  
		Last Modified: Sat, 07 Sep 2024 05:27:22 GMT  
		Size: 47.7 MB (47709505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2432c5f0597753c705d3724184b3356815256a64a8c93aa3781d2e785593ce7`  
		Last Modified: Sat, 07 Sep 2024 05:27:21 GMT  
		Size: 21.7 MB (21662516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5933260cd0024e114bab17baef98e72aa06083573baa234ae705402c874b1a6e`  
		Last Modified: Sat, 07 Sep 2024 05:27:21 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343fdf5a00e872d5be68ab0f1f4c181170fb92a665999710b3589a2f80b8354b`  
		Last Modified: Sat, 07 Sep 2024 05:27:21 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c614e03155dfd058b554c17f6b42e3fa4eddd5938d80ec113ef5ea4e07bc045a`  
		Last Modified: Sat, 07 Sep 2024 05:27:21 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:fd0b50cc9671d0a3aded8e829d944212c24854b17ce177492fdd78e3c85adbca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.4 KB (944406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c436daff587bcef14431aa15b0a39ef47994bc66d9a0353450d30a519c01ad27`

```dockerfile
```

-	Layers:
	-	`sha256:ca5611f32d0ac5d978cefb8dc3b90ae6bfae5a67b19d2f2bdc02d6c9000569a7`  
		Last Modified: Sat, 07 Sep 2024 05:27:19 GMT  
		Size: 913.4 KB (913354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e00d02321e4e44e7c735484a05227ce7d6b07e76a212b03bf5b22f30d7ee3d3`  
		Last Modified: Sat, 07 Sep 2024 05:27:19 GMT  
		Size: 31.1 KB (31052 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7.10`

```console
$ docker pull influxdb@sha256:b59864431e6f10a40aeb1040d4e11114c86ec8ec900926ee4d88cee8b89d20e7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7.10` - linux; amd64

```console
$ docker pull influxdb@sha256:565fd3432b668a2fea119e9d2d7e857c49688af708aafb30cb5c6476b8d73e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168475058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82765bab090017edb2e03a187c5668f5f9048b52efb857d458521dd5774160b2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["bash"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV GOSU_VER=1.16
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=2.7.10
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 16 Aug 2024 20:18:45 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477705850a3a7f5f03e5d6a1a59a0dcfa91b94206e39a56cc6948133bfeee20c`  
		Last Modified: Wed, 04 Sep 2024 23:10:04 GMT  
		Size: 9.8 MB (9788950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb97151d37e4aa70aa077f6162a9890304784966c35ba5d3af11f1def2b263fd`  
		Last Modified: Wed, 04 Sep 2024 23:10:04 GMT  
		Size: 5.8 MB (5820938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f3fc2b91f4c45426d08bb4e1a3cbf12c856cfed711e1d43c65f2cc105cc256`  
		Last Modified: Wed, 04 Sep 2024 23:10:04 GMT  
		Size: 3.2 KB (3226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389c37eac14d118b3cb70b72e1f477a24c4986b26ade1960b57d552bbcd57f19`  
		Last Modified: Wed, 04 Sep 2024 23:10:04 GMT  
		Size: 1.0 MB (1006368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd854556873c80b5145bf59213db12c5417313e31ecb8190690ce1899737ad10`  
		Last Modified: Wed, 04 Sep 2024 23:10:07 GMT  
		Size: 99.6 MB (99594066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ae1439b7721fdeded51a74c06d4911e5aa66f9c6de27df9df050d64d194d56`  
		Last Modified: Wed, 04 Sep 2024 23:10:05 GMT  
		Size: 23.1 MB (23128301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81be0a7f65a5159ce17c6a5c844f578c79cdc48d004173b15b6fe6ed6b225dd1`  
		Last Modified: Wed, 04 Sep 2024 23:10:06 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af8f8db7d47ab30ae652279949643449f0f4722ac4e8f0a6bfcbeccf6a54b12`  
		Last Modified: Wed, 04 Sep 2024 23:10:05 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65fc8982233fe665574473fa1c2f285de2428e3ce74a9d595f6ae0744bbcbdb0`  
		Last Modified: Wed, 04 Sep 2024 23:10:06 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.10` - unknown; unknown

```console
$ docker pull influxdb@sha256:67c55d73c97a06ccd1f33b9623748a63f4bcd3bf5b9a466699b240eaa03a716f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de69f4b4f8604f2c94d486d1b0a00fa53c547ab5de99010a8578be79610d1673`

```dockerfile
```

-	Layers:
	-	`sha256:af7960aa38e90d8826134f7591e3b020c58f42468d23e5ab3ff2a5edca9bea22`  
		Last Modified: Wed, 04 Sep 2024 23:10:04 GMT  
		Size: 2.8 MB (2833443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35599651b4f0cdc382b9c7d513b3fd5e35824e7a6c12b885cbf120268e730a08`  
		Last Modified: Wed, 04 Sep 2024 23:10:04 GMT  
		Size: 33.5 KB (33545 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7.10` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:0dee8c333792bdf4ae8bb45f90c537f93c93ead6c0746c991dbfbcbbcc9291f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.2 MB (162243946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3397d79b74503e0df0a037eb63b3d6eaca40d36a99d570483cafe6d5552cbfc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["bash"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV GOSU_VER=1.16
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=2.7.10
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 16 Aug 2024 20:18:45 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3788f6761354a8e34c9dee5aa1c5e266c9f7fb192ee67465d0b3381a6675dadd`  
		Last Modified: Thu, 05 Sep 2024 12:18:43 GMT  
		Size: 9.6 MB (9587108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607ee39df12476d4788e3aa8305639d96df0197a9826a2088f03b89ba769e349`  
		Last Modified: Thu, 05 Sep 2024 12:18:43 GMT  
		Size: 5.5 MB (5463801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d90eb06433b93420b11b1d6a090d6866dd1a61d72d8742b786199b56c20a09d`  
		Last Modified: Thu, 05 Sep 2024 12:18:42 GMT  
		Size: 3.2 KB (3226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bb7b9bd024f3c163fc1ec8c85baa5a0ecaaa6bf6e4fcc1705854b855a5bd73`  
		Last Modified: Thu, 05 Sep 2024 12:18:43 GMT  
		Size: 936.1 KB (936105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26df1b491b2829e3c2a79bf79ef065f479659639c8c6bcef909c5a0521a16963`  
		Last Modified: Thu, 05 Sep 2024 12:18:46 GMT  
		Size: 95.4 MB (95427914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67aef66159039be0863ad28aa66d7317c2af5505d5c9e89b4f5b799bb764cd04`  
		Last Modified: Thu, 05 Sep 2024 12:18:45 GMT  
		Size: 21.7 MB (21662519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2e701aaea336fdc9d97cb2ead500046df05e86c131199ad1ca8e67350a44c2`  
		Last Modified: Thu, 05 Sep 2024 12:18:44 GMT  
		Size: 207.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38bb9310aa18b0e075b702b3ef35d26ab7e0a2e66d526b5a1708577f6ffcc987`  
		Last Modified: Thu, 05 Sep 2024 12:18:44 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf751defaf44888faf018dfcc83f5490a231ce314117a56b7e25e985656cd86`  
		Last Modified: Thu, 05 Sep 2024 12:18:45 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.10` - unknown; unknown

```console
$ docker pull influxdb@sha256:8bfe01d8dca857195cc81d6e1e452a5c8270cd1146a53cd47a948ed3c5a20c74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9488a1be5ce1441c26e77352b52a7ea839cabba20629d4560c4308f1ffe16c4`

```dockerfile
```

-	Layers:
	-	`sha256:a7b7f386f124d2d793ad5f4c9b797a20074563fdfb8b7b393b7dbf6a9f96c640`  
		Last Modified: Thu, 05 Sep 2024 12:18:43 GMT  
		Size: 2.8 MB (2832680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa9da7ba1e0fb5f1af48ead53d074eb281f5a557cfccb02b51cd097d034edcee`  
		Last Modified: Thu, 05 Sep 2024 12:18:42 GMT  
		Size: 33.8 KB (33848 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7.10-alpine`

```console
$ docker pull influxdb@sha256:327be0243a329b1da350a37c1468d756f4258330d50d10a2a993e5bb9a6e3d2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7.10-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:cac47619d57d832e6a0f787362eba5b3e1f36629afd0e2e843e066b35151e380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (92006098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6a7f3befda36a7f068f8339e56f8f59f6e527333e161482eae1d0df560e75c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=2.7.10
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 16 Aug 2024 20:18:45 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078166243ebe0c2b9c91a2f7e164076218c7716b68301080fac2f19f177dd096`  
		Last Modified: Fri, 06 Sep 2024 23:21:35 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1587bf1467bd7fa0cc2b3706d4443a35b49f61bd49b1290f081643d747c38c`  
		Last Modified: Fri, 06 Sep 2024 23:21:40 GMT  
		Size: 9.6 MB (9634631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed395597bc0621a59fd604631b8c292c382b858b04d465c184da49759e54a5f2`  
		Last Modified: Fri, 06 Sep 2024 23:21:40 GMT  
		Size: 5.8 MB (5820945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d0f5c43f5e203308ab55d4d25d6adedc07ff5e1ae398853254c3b438bbf159`  
		Last Modified: Fri, 06 Sep 2024 23:21:39 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050deb0e5ac12402242203b9a1622d17bb64075b547efbbd845bec1f2a228b3f`  
		Last Modified: Fri, 06 Sep 2024 23:21:41 GMT  
		Size: 49.8 MB (49790466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84be9b15369ef3c36eb630297dc094d0685e0b0b896139448712012f1770e988`  
		Last Modified: Fri, 06 Sep 2024 23:21:41 GMT  
		Size: 23.1 MB (23128284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64fac09c6feb55954579c03c8eb95a176fa4466a843ffd0bff0f34285b16fff`  
		Last Modified: Fri, 06 Sep 2024 23:21:40 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc407c5347f2647cdac2b45ee7c93f275e3b7b3ae212b1ef9aa98d85bcde01a2`  
		Last Modified: Fri, 06 Sep 2024 23:21:41 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd950ffb540d8825efa00e5972a9aa81a31adcd1b9c6350cac0788e1a18392f2`  
		Last Modified: Fri, 06 Sep 2024 23:21:41 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.10-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:acbb7b79cd5c3b0c183013df9776032eb14bb163e9eb2b3becd90c70b47a0c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.8 KB (944845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b3b3774810f57f3371aa23eaffa51ffbdc41e5b074a7c7e3ab902304cffe58`

```dockerfile
```

-	Layers:
	-	`sha256:5c072ab20e36c5f3b5b02ca06364a72e79aad9b7562f55eacf3460ebc071a8ed`  
		Last Modified: Fri, 06 Sep 2024 23:21:39 GMT  
		Size: 914.1 KB (914093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b689f3cda8aaa0b6667d6a4d53280e261fa5922f2272a2269832f1b17f8711f`  
		Last Modified: Fri, 06 Sep 2024 23:21:39 GMT  
		Size: 30.8 KB (30752 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7.10-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:1000811b02d8b6fdb75ea723c4e9c33746c27e6d0be65a84b9152ecc28fb0f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88688483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feba5f301346b7e3cba9218b3a9b5ae318b06386a0b000e04c7dab92f1576f5a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=2.7.10
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 16 Aug 2024 20:18:45 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e4b70a44519145916f8803166c99c3ba52ea4bf109ad21b6d3e97aaa6f17a6`  
		Last Modified: Sat, 07 Sep 2024 05:27:19 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9713c4c4a81b87a3373d8e7be5320c3cc5cc86ad74b6c2a3b331c3be04d8cac`  
		Last Modified: Sat, 07 Sep 2024 05:27:20 GMT  
		Size: 9.8 MB (9757048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbef7f92137af9c8d8b2ceb13c99138a68cd759251cc1d5e407ff11e6bd9db8`  
		Last Modified: Sat, 07 Sep 2024 05:27:19 GMT  
		Size: 5.5 MB (5463803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7a1f6a4d13197b794b1cec6c7f7160c8d5a86013ec29ba75ac7fb7cd7dda19`  
		Last Modified: Sat, 07 Sep 2024 05:27:19 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a928a7eba1ff5a21c666fa39ef8dade819caf6ce52010688b7d5b2d950456277`  
		Last Modified: Sat, 07 Sep 2024 05:27:22 GMT  
		Size: 47.7 MB (47709505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2432c5f0597753c705d3724184b3356815256a64a8c93aa3781d2e785593ce7`  
		Last Modified: Sat, 07 Sep 2024 05:27:21 GMT  
		Size: 21.7 MB (21662516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5933260cd0024e114bab17baef98e72aa06083573baa234ae705402c874b1a6e`  
		Last Modified: Sat, 07 Sep 2024 05:27:21 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343fdf5a00e872d5be68ab0f1f4c181170fb92a665999710b3589a2f80b8354b`  
		Last Modified: Sat, 07 Sep 2024 05:27:21 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c614e03155dfd058b554c17f6b42e3fa4eddd5938d80ec113ef5ea4e07bc045a`  
		Last Modified: Sat, 07 Sep 2024 05:27:21 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.10-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:fd0b50cc9671d0a3aded8e829d944212c24854b17ce177492fdd78e3c85adbca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.4 KB (944406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c436daff587bcef14431aa15b0a39ef47994bc66d9a0353450d30a519c01ad27`

```dockerfile
```

-	Layers:
	-	`sha256:ca5611f32d0ac5d978cefb8dc3b90ae6bfae5a67b19d2f2bdc02d6c9000569a7`  
		Last Modified: Sat, 07 Sep 2024 05:27:19 GMT  
		Size: 913.4 KB (913354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e00d02321e4e44e7c735484a05227ce7d6b07e76a212b03bf5b22f30d7ee3d3`  
		Last Modified: Sat, 07 Sep 2024 05:27:19 GMT  
		Size: 31.1 KB (31052 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:327be0243a329b1da350a37c1468d756f4258330d50d10a2a993e5bb9a6e3d2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:cac47619d57d832e6a0f787362eba5b3e1f36629afd0e2e843e066b35151e380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (92006098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6a7f3befda36a7f068f8339e56f8f59f6e527333e161482eae1d0df560e75c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=2.7.10
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 16 Aug 2024 20:18:45 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078166243ebe0c2b9c91a2f7e164076218c7716b68301080fac2f19f177dd096`  
		Last Modified: Fri, 06 Sep 2024 23:21:35 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1587bf1467bd7fa0cc2b3706d4443a35b49f61bd49b1290f081643d747c38c`  
		Last Modified: Fri, 06 Sep 2024 23:21:40 GMT  
		Size: 9.6 MB (9634631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed395597bc0621a59fd604631b8c292c382b858b04d465c184da49759e54a5f2`  
		Last Modified: Fri, 06 Sep 2024 23:21:40 GMT  
		Size: 5.8 MB (5820945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d0f5c43f5e203308ab55d4d25d6adedc07ff5e1ae398853254c3b438bbf159`  
		Last Modified: Fri, 06 Sep 2024 23:21:39 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050deb0e5ac12402242203b9a1622d17bb64075b547efbbd845bec1f2a228b3f`  
		Last Modified: Fri, 06 Sep 2024 23:21:41 GMT  
		Size: 49.8 MB (49790466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84be9b15369ef3c36eb630297dc094d0685e0b0b896139448712012f1770e988`  
		Last Modified: Fri, 06 Sep 2024 23:21:41 GMT  
		Size: 23.1 MB (23128284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64fac09c6feb55954579c03c8eb95a176fa4466a843ffd0bff0f34285b16fff`  
		Last Modified: Fri, 06 Sep 2024 23:21:40 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc407c5347f2647cdac2b45ee7c93f275e3b7b3ae212b1ef9aa98d85bcde01a2`  
		Last Modified: Fri, 06 Sep 2024 23:21:41 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd950ffb540d8825efa00e5972a9aa81a31adcd1b9c6350cac0788e1a18392f2`  
		Last Modified: Fri, 06 Sep 2024 23:21:41 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:acbb7b79cd5c3b0c183013df9776032eb14bb163e9eb2b3becd90c70b47a0c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.8 KB (944845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b3b3774810f57f3371aa23eaffa51ffbdc41e5b074a7c7e3ab902304cffe58`

```dockerfile
```

-	Layers:
	-	`sha256:5c072ab20e36c5f3b5b02ca06364a72e79aad9b7562f55eacf3460ebc071a8ed`  
		Last Modified: Fri, 06 Sep 2024 23:21:39 GMT  
		Size: 914.1 KB (914093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b689f3cda8aaa0b6667d6a4d53280e261fa5922f2272a2269832f1b17f8711f`  
		Last Modified: Fri, 06 Sep 2024 23:21:39 GMT  
		Size: 30.8 KB (30752 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:1000811b02d8b6fdb75ea723c4e9c33746c27e6d0be65a84b9152ecc28fb0f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88688483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feba5f301346b7e3cba9218b3a9b5ae318b06386a0b000e04c7dab92f1576f5a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=2.7.10
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 16 Aug 2024 20:18:45 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e4b70a44519145916f8803166c99c3ba52ea4bf109ad21b6d3e97aaa6f17a6`  
		Last Modified: Sat, 07 Sep 2024 05:27:19 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9713c4c4a81b87a3373d8e7be5320c3cc5cc86ad74b6c2a3b331c3be04d8cac`  
		Last Modified: Sat, 07 Sep 2024 05:27:20 GMT  
		Size: 9.8 MB (9757048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbef7f92137af9c8d8b2ceb13c99138a68cd759251cc1d5e407ff11e6bd9db8`  
		Last Modified: Sat, 07 Sep 2024 05:27:19 GMT  
		Size: 5.5 MB (5463803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7a1f6a4d13197b794b1cec6c7f7160c8d5a86013ec29ba75ac7fb7cd7dda19`  
		Last Modified: Sat, 07 Sep 2024 05:27:19 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a928a7eba1ff5a21c666fa39ef8dade819caf6ce52010688b7d5b2d950456277`  
		Last Modified: Sat, 07 Sep 2024 05:27:22 GMT  
		Size: 47.7 MB (47709505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2432c5f0597753c705d3724184b3356815256a64a8c93aa3781d2e785593ce7`  
		Last Modified: Sat, 07 Sep 2024 05:27:21 GMT  
		Size: 21.7 MB (21662516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5933260cd0024e114bab17baef98e72aa06083573baa234ae705402c874b1a6e`  
		Last Modified: Sat, 07 Sep 2024 05:27:21 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343fdf5a00e872d5be68ab0f1f4c181170fb92a665999710b3589a2f80b8354b`  
		Last Modified: Sat, 07 Sep 2024 05:27:21 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c614e03155dfd058b554c17f6b42e3fa4eddd5938d80ec113ef5ea4e07bc045a`  
		Last Modified: Sat, 07 Sep 2024 05:27:21 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:fd0b50cc9671d0a3aded8e829d944212c24854b17ce177492fdd78e3c85adbca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.4 KB (944406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c436daff587bcef14431aa15b0a39ef47994bc66d9a0353450d30a519c01ad27`

```dockerfile
```

-	Layers:
	-	`sha256:ca5611f32d0ac5d978cefb8dc3b90ae6bfae5a67b19d2f2bdc02d6c9000569a7`  
		Last Modified: Sat, 07 Sep 2024 05:27:19 GMT  
		Size: 913.4 KB (913354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e00d02321e4e44e7c735484a05227ce7d6b07e76a212b03bf5b22f30d7ee3d3`  
		Last Modified: Sat, 07 Sep 2024 05:27:19 GMT  
		Size: 31.1 KB (31052 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:latest`

```console
$ docker pull influxdb@sha256:b59864431e6f10a40aeb1040d4e11114c86ec8ec900926ee4d88cee8b89d20e7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:565fd3432b668a2fea119e9d2d7e857c49688af708aafb30cb5c6476b8d73e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168475058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82765bab090017edb2e03a187c5668f5f9048b52efb857d458521dd5774160b2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["bash"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV GOSU_VER=1.16
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=2.7.10
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 16 Aug 2024 20:18:45 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477705850a3a7f5f03e5d6a1a59a0dcfa91b94206e39a56cc6948133bfeee20c`  
		Last Modified: Wed, 04 Sep 2024 23:10:04 GMT  
		Size: 9.8 MB (9788950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb97151d37e4aa70aa077f6162a9890304784966c35ba5d3af11f1def2b263fd`  
		Last Modified: Wed, 04 Sep 2024 23:10:04 GMT  
		Size: 5.8 MB (5820938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f3fc2b91f4c45426d08bb4e1a3cbf12c856cfed711e1d43c65f2cc105cc256`  
		Last Modified: Wed, 04 Sep 2024 23:10:04 GMT  
		Size: 3.2 KB (3226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389c37eac14d118b3cb70b72e1f477a24c4986b26ade1960b57d552bbcd57f19`  
		Last Modified: Wed, 04 Sep 2024 23:10:04 GMT  
		Size: 1.0 MB (1006368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd854556873c80b5145bf59213db12c5417313e31ecb8190690ce1899737ad10`  
		Last Modified: Wed, 04 Sep 2024 23:10:07 GMT  
		Size: 99.6 MB (99594066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ae1439b7721fdeded51a74c06d4911e5aa66f9c6de27df9df050d64d194d56`  
		Last Modified: Wed, 04 Sep 2024 23:10:05 GMT  
		Size: 23.1 MB (23128301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81be0a7f65a5159ce17c6a5c844f578c79cdc48d004173b15b6fe6ed6b225dd1`  
		Last Modified: Wed, 04 Sep 2024 23:10:06 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af8f8db7d47ab30ae652279949643449f0f4722ac4e8f0a6bfcbeccf6a54b12`  
		Last Modified: Wed, 04 Sep 2024 23:10:05 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65fc8982233fe665574473fa1c2f285de2428e3ce74a9d595f6ae0744bbcbdb0`  
		Last Modified: Wed, 04 Sep 2024 23:10:06 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:67c55d73c97a06ccd1f33b9623748a63f4bcd3bf5b9a466699b240eaa03a716f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de69f4b4f8604f2c94d486d1b0a00fa53c547ab5de99010a8578be79610d1673`

```dockerfile
```

-	Layers:
	-	`sha256:af7960aa38e90d8826134f7591e3b020c58f42468d23e5ab3ff2a5edca9bea22`  
		Last Modified: Wed, 04 Sep 2024 23:10:04 GMT  
		Size: 2.8 MB (2833443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35599651b4f0cdc382b9c7d513b3fd5e35824e7a6c12b885cbf120268e730a08`  
		Last Modified: Wed, 04 Sep 2024 23:10:04 GMT  
		Size: 33.5 KB (33545 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:0dee8c333792bdf4ae8bb45f90c537f93c93ead6c0746c991dbfbcbbcc9291f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.2 MB (162243946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3397d79b74503e0df0a037eb63b3d6eaca40d36a99d570483cafe6d5552cbfc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["bash"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV GOSU_VER=1.16
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=2.7.10
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 16 Aug 2024 20:18:45 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3788f6761354a8e34c9dee5aa1c5e266c9f7fb192ee67465d0b3381a6675dadd`  
		Last Modified: Thu, 05 Sep 2024 12:18:43 GMT  
		Size: 9.6 MB (9587108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607ee39df12476d4788e3aa8305639d96df0197a9826a2088f03b89ba769e349`  
		Last Modified: Thu, 05 Sep 2024 12:18:43 GMT  
		Size: 5.5 MB (5463801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d90eb06433b93420b11b1d6a090d6866dd1a61d72d8742b786199b56c20a09d`  
		Last Modified: Thu, 05 Sep 2024 12:18:42 GMT  
		Size: 3.2 KB (3226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bb7b9bd024f3c163fc1ec8c85baa5a0ecaaa6bf6e4fcc1705854b855a5bd73`  
		Last Modified: Thu, 05 Sep 2024 12:18:43 GMT  
		Size: 936.1 KB (936105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26df1b491b2829e3c2a79bf79ef065f479659639c8c6bcef909c5a0521a16963`  
		Last Modified: Thu, 05 Sep 2024 12:18:46 GMT  
		Size: 95.4 MB (95427914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67aef66159039be0863ad28aa66d7317c2af5505d5c9e89b4f5b799bb764cd04`  
		Last Modified: Thu, 05 Sep 2024 12:18:45 GMT  
		Size: 21.7 MB (21662519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2e701aaea336fdc9d97cb2ead500046df05e86c131199ad1ca8e67350a44c2`  
		Last Modified: Thu, 05 Sep 2024 12:18:44 GMT  
		Size: 207.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38bb9310aa18b0e075b702b3ef35d26ab7e0a2e66d526b5a1708577f6ffcc987`  
		Last Modified: Thu, 05 Sep 2024 12:18:44 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf751defaf44888faf018dfcc83f5490a231ce314117a56b7e25e985656cd86`  
		Last Modified: Thu, 05 Sep 2024 12:18:45 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:8bfe01d8dca857195cc81d6e1e452a5c8270cd1146a53cd47a948ed3c5a20c74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9488a1be5ce1441c26e77352b52a7ea839cabba20629d4560c4308f1ffe16c4`

```dockerfile
```

-	Layers:
	-	`sha256:a7b7f386f124d2d793ad5f4c9b797a20074563fdfb8b7b393b7dbf6a9f96c640`  
		Last Modified: Thu, 05 Sep 2024 12:18:43 GMT  
		Size: 2.8 MB (2832680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa9da7ba1e0fb5f1af48ead53d074eb281f5a557cfccb02b51cd097d034edcee`  
		Last Modified: Thu, 05 Sep 2024 12:18:42 GMT  
		Size: 33.8 KB (33848 bytes)  
		MIME: application/vnd.in-toto+json
