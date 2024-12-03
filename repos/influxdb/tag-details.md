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
-	[`influxdb:1.11`](#influxdb111)
-	[`influxdb:1.11-alpine`](#influxdb111-alpine)
-	[`influxdb:1.11-data`](#influxdb111-data)
-	[`influxdb:1.11-data-alpine`](#influxdb111-data-alpine)
-	[`influxdb:1.11-meta`](#influxdb111-meta)
-	[`influxdb:1.11-meta-alpine`](#influxdb111-meta-alpine)
-	[`influxdb:1.11.8`](#influxdb1118)
-	[`influxdb:1.11.8-alpine`](#influxdb1118-alpine)
-	[`influxdb:1.11.8-data`](#influxdb1118-data)
-	[`influxdb:1.11.8-data-alpine`](#influxdb1118-data-alpine)
-	[`influxdb:1.11.8-meta`](#influxdb1118-meta)
-	[`influxdb:1.11.8-meta-alpine`](#influxdb1118-meta-alpine)
-	[`influxdb:2`](#influxdb2)
-	[`influxdb:2-alpine`](#influxdb2-alpine)
-	[`influxdb:2.7`](#influxdb27)
-	[`influxdb:2.7-alpine`](#influxdb27-alpine)
-	[`influxdb:2.7.11`](#influxdb2711)
-	[`influxdb:2.7.11-alpine`](#influxdb2711-alpine)
-	[`influxdb:alpine`](#influxdbalpine)
-	[`influxdb:latest`](#influxdblatest)

## `influxdb:1.10-data`

```console
$ docker pull influxdb@sha256:f6a9fc983640c0f1f0fc1ef7134e5bcd1d2b68a5afde90571b6447e90916b968
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-data` - linux; amd64

```console
$ docker pull influxdb@sha256:cdd69cab0cd83ba2160bad916834f7851dcc3984aebaeeb08273b2525676b560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.0 MB (112048025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d231fe7fa8caa8678705da62faac16b1dafae109f24a86ce7239d8290cdbb1cc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Sat, 26 Oct 2024 00:18:17 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
EXPOSE map[8086/tcp:{}]
# Sat, 26 Oct 2024 00:18:17 GMT
VOLUME [/var/lib/influxdb]
# Sat, 26 Oct 2024 00:18:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 26 Oct 2024 00:18:17 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c2056d933cd629f55ac55802dda223f122286bf60ec42a24f0d0f6ae2615315c`  
		Last Modified: Tue, 12 Nov 2024 00:55:16 GMT  
		Size: 55.1 MB (55108780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f895247ac53f8ccaff2388685ac5288e243187f243654f4af6205a31f8b693`  
		Last Modified: Tue, 12 Nov 2024 02:37:53 GMT  
		Size: 15.6 MB (15557923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a6d8e13902a341896f44034e166050809b17a587fb089ed7732301e1cbe2ab`  
		Last Modified: Tue, 12 Nov 2024 03:14:28 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fded2204f511397e5169b70982f3243ca0abd90110da412a044a64484254806a`  
		Last Modified: Tue, 12 Nov 2024 03:14:29 GMT  
		Size: 41.4 MB (41377774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69fad4af65cbd10e30c45b6aa124f2234637a21490ec59f17859262fddf8fdb2`  
		Last Modified: Tue, 12 Nov 2024 03:14:29 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca80afa8166f33c957a60f1afa84467dd8eb92ec784f7a143894867cd026591`  
		Last Modified: Tue, 12 Nov 2024 03:14:29 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6f8f747a186b99c711029e0da24dca9ad5d3bc94bd20e3f86b188fab2d974b`  
		Last Modified: Tue, 12 Nov 2024 03:14:29 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:a6bd9fbf01574a6e928230c11ac36e4188d449451783e451e05e5d0ac954da46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4659065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67b2ce7dda7a7199152d2af21df164e25020ff89b2df31f4fd80ead2b0a41e64`

```dockerfile
```

-	Layers:
	-	`sha256:070dd3d36579863bfcc8559558f11c6af72a59355546e9ba0849423859b8192f`  
		Last Modified: Tue, 12 Nov 2024 03:14:29 GMT  
		Size: 4.6 MB (4644357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:482a235cfdf1a4d10966720d2205b343ef81a02c7287ae4a96536c093c129bb6`  
		Last Modified: Tue, 12 Nov 2024 03:14:29 GMT  
		Size: 14.7 KB (14708 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10-data-alpine`

```console
$ docker pull influxdb@sha256:eee81d783a38e077c9fec8dad612c126e702e4656fb7752aa24f6bdc7abecf04
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:35823a7882624aa20d5669dd02a5cbd54cccd3cb13dc28383e2ded982eda2d4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46172346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6c4b07b762feeda93b79ec8342fc0048393c8b42e4a47479055ffa66d14ad2f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Sat, 26 Oct 2024 00:18:17 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Sat, 26 Oct 2024 00:18:17 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
EXPOSE map[8086/tcp:{}]
# Sat, 26 Oct 2024 00:18:17 GMT
VOLUME [/var/lib/influxdb]
# Sat, 26 Oct 2024 00:18:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 26 Oct 2024 00:18:17 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832efc79eb2e8f7bbf4686f340aca032adaf1a693ccf7487d85276ae0210a9a3`  
		Last Modified: Tue, 12 Nov 2024 02:13:56 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d248baf933848bcc776a4463e3b08107f77d32dca939f04a202d83fedbfe01`  
		Last Modified: Tue, 12 Nov 2024 02:13:56 GMT  
		Size: 1.2 MB (1223726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a19aad79d7aa454c7216711056c0693f9209929f4ab726db0b29a52f9998b02`  
		Last Modified: Tue, 12 Nov 2024 02:13:57 GMT  
		Size: 41.3 MB (41322662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7668202f1e22a5df78cd8b57845dff8409e40357eb886feb8318cbd79397c43a`  
		Last Modified: Tue, 12 Nov 2024 02:13:56 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc04841e72c153311305356dd0e73d69f6765231f29d2a80ed9d5ed8c9dda22`  
		Last Modified: Tue, 12 Nov 2024 02:13:57 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2e1e59bb95f0c858a590f633f3b93c1bab619214946005e099870dee05091b`  
		Last Modified: Tue, 12 Nov 2024 02:13:57 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:a461e4fbcaa4b456b4bdd4ba46ee1becc2f6cf59010bf2302a243ae89ea88154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **770.5 KB (770460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d57b227e238bdfbc0ad4339f7024dd656f0e0e17a90b48232f33e1fd0573a714`

```dockerfile
```

-	Layers:
	-	`sha256:3fb366e475b46727356dedfd602ea98fa9dd3af189dfad284d61afe611357683`  
		Last Modified: Tue, 12 Nov 2024 02:13:56 GMT  
		Size: 753.8 KB (753822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f472b03a01bf56d4c3e8c3edd94a394ab837ebd354f1200b93178b02a82ecc6c`  
		Last Modified: Tue, 12 Nov 2024 02:13:56 GMT  
		Size: 16.6 KB (16638 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10-meta`

```console
$ docker pull influxdb@sha256:c22ea2644fad053077e1dc1c4d1b9ca1e01415dc764c9361ffe318202849a3ac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:c09f7a94f7aa8d82e017ae03c9cbfbf07eb6e72db0c6b35c999e7e0108688f4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.8 MB (90764624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:535d743d036954731d846bd32828608eb510fd3d2c8a09f41c0d73e634849d40`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Sat, 26 Oct 2024 00:18:17 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
EXPOSE map[8091/tcp:{}]
# Sat, 26 Oct 2024 00:18:17 GMT
VOLUME [/var/lib/influxdb]
# Sat, 26 Oct 2024 00:18:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 26 Oct 2024 00:18:17 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:c2056d933cd629f55ac55802dda223f122286bf60ec42a24f0d0f6ae2615315c`  
		Last Modified: Tue, 12 Nov 2024 00:55:16 GMT  
		Size: 55.1 MB (55108780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f895247ac53f8ccaff2388685ac5288e243187f243654f4af6205a31f8b693`  
		Last Modified: Tue, 12 Nov 2024 02:37:53 GMT  
		Size: 15.6 MB (15557923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3815d10d94129dbe2c0391239c2924feac1dee02a65a2ae82df43746c4bbdef`  
		Last Modified: Tue, 12 Nov 2024 03:14:25 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70af44e985b2c2a21660e0e91bc5a3784cde40767a13bb58180508b3b90e35b`  
		Last Modified: Tue, 12 Nov 2024 03:14:27 GMT  
		Size: 20.1 MB (20095571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1c583ec06ddaa49c7ff366bb97d15067e0d8b58f54c27cf4ab37e7db178cfc`  
		Last Modified: Tue, 12 Nov 2024 03:14:26 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8953b200e03c4f392dd626922f9ca877502ca2b2e5a40f8b87f30a0c5b4cde6`  
		Last Modified: Tue, 12 Nov 2024 03:14:25 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:024d2b0915885a0e91eb3bc72ec384279b9cdd142fac2e58be16ce841c93749f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4582011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e53c396287ec2a2b5cb51e39573b216aafeb047a8bb75e579ecc10005e7c3e1`

```dockerfile
```

-	Layers:
	-	`sha256:015086d6fbd1b706968111b7d781072240ddd53fc6bf58147a3a19684df0d43a`  
		Last Modified: Tue, 12 Nov 2024 03:14:26 GMT  
		Size: 4.6 MB (4568944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be5e2b27f02fbce16ecdc208f143385fa558efe478ec783c86a36f3141326693`  
		Last Modified: Tue, 12 Nov 2024 03:14:26 GMT  
		Size: 13.1 KB (13067 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10-meta-alpine`

```console
$ docker pull influxdb@sha256:87435d3f4fd949047ddbc915d3411b5023e60434d09652ffacc49cbf2923d397
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:882e8a13b101bd8e407789658a3bb4bf3fd2c5e1a6b2562809174c502250b221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.9 MB (24890556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2b92ebf5cdf243c5061bb796e7b4ed3a221ea884988df4515d8248cfc3ea3d4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Sat, 26 Oct 2024 00:18:17 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Sat, 26 Oct 2024 00:18:17 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
EXPOSE map[8091/tcp:{}]
# Sat, 26 Oct 2024 00:18:17 GMT
VOLUME [/var/lib/influxdb]
# Sat, 26 Oct 2024 00:18:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 26 Oct 2024 00:18:17 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8359fb22721bda65d61d3b3f43f9ef0bb4da1e7a89cf9bef3befc9dcd7d5c88`  
		Last Modified: Tue, 12 Nov 2024 02:13:58 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e4fa5be5bcbc133931311823895c8a9631c3bfc36b408219870173e78cd3f6`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 1.2 MB (1223725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aab0e75d4cc704b59ae8f224fc0878b1c294b912bab547f50dadb3f9b16eeee`  
		Last Modified: Tue, 12 Nov 2024 02:14:05 GMT  
		Size: 20.0 MB (20042081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e164402425990ff9b8ee202e28127f8bde685bc48d14eccce238b807f498c62f`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e70c603787aa058d11d76ad1556b160380b0da6c5bfe086ee06bd8bdb091e2b`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:d634a48656250cd109ec159741743a5f45a90cac2da999b9fe6ddde3f0330964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **693.6 KB (693575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324dbf8d99ef457bb8f6543b7d797ab1c81b99f92a765b599b942d2d0867a97f`

```dockerfile
```

-	Layers:
	-	`sha256:1f0a8bbb9b95d79cdd9a6e22d20809b4be93407345477745c4605aa07cfbb7a4`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 678.6 KB (678565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:805d6815075842407019641044c39e5cdcf1ae3d7e54775dc245065cfd6d5a1e`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 15.0 KB (15010 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10.7-data`

```console
$ docker pull influxdb@sha256:f6a9fc983640c0f1f0fc1ef7134e5bcd1d2b68a5afde90571b6447e90916b968
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.7-data` - linux; amd64

```console
$ docker pull influxdb@sha256:cdd69cab0cd83ba2160bad916834f7851dcc3984aebaeeb08273b2525676b560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.0 MB (112048025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d231fe7fa8caa8678705da62faac16b1dafae109f24a86ce7239d8290cdbb1cc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Sat, 26 Oct 2024 00:18:17 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
EXPOSE map[8086/tcp:{}]
# Sat, 26 Oct 2024 00:18:17 GMT
VOLUME [/var/lib/influxdb]
# Sat, 26 Oct 2024 00:18:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 26 Oct 2024 00:18:17 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c2056d933cd629f55ac55802dda223f122286bf60ec42a24f0d0f6ae2615315c`  
		Last Modified: Tue, 12 Nov 2024 00:55:16 GMT  
		Size: 55.1 MB (55108780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f895247ac53f8ccaff2388685ac5288e243187f243654f4af6205a31f8b693`  
		Last Modified: Tue, 12 Nov 2024 02:37:53 GMT  
		Size: 15.6 MB (15557923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a6d8e13902a341896f44034e166050809b17a587fb089ed7732301e1cbe2ab`  
		Last Modified: Tue, 12 Nov 2024 03:14:28 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fded2204f511397e5169b70982f3243ca0abd90110da412a044a64484254806a`  
		Last Modified: Tue, 12 Nov 2024 03:14:29 GMT  
		Size: 41.4 MB (41377774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69fad4af65cbd10e30c45b6aa124f2234637a21490ec59f17859262fddf8fdb2`  
		Last Modified: Tue, 12 Nov 2024 03:14:29 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca80afa8166f33c957a60f1afa84467dd8eb92ec784f7a143894867cd026591`  
		Last Modified: Tue, 12 Nov 2024 03:14:29 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6f8f747a186b99c711029e0da24dca9ad5d3bc94bd20e3f86b188fab2d974b`  
		Last Modified: Tue, 12 Nov 2024 03:14:29 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.7-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:a6bd9fbf01574a6e928230c11ac36e4188d449451783e451e05e5d0ac954da46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4659065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67b2ce7dda7a7199152d2af21df164e25020ff89b2df31f4fd80ead2b0a41e64`

```dockerfile
```

-	Layers:
	-	`sha256:070dd3d36579863bfcc8559558f11c6af72a59355546e9ba0849423859b8192f`  
		Last Modified: Tue, 12 Nov 2024 03:14:29 GMT  
		Size: 4.6 MB (4644357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:482a235cfdf1a4d10966720d2205b343ef81a02c7287ae4a96536c093c129bb6`  
		Last Modified: Tue, 12 Nov 2024 03:14:29 GMT  
		Size: 14.7 KB (14708 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10.7-data-alpine`

```console
$ docker pull influxdb@sha256:eee81d783a38e077c9fec8dad612c126e702e4656fb7752aa24f6bdc7abecf04
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.7-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:35823a7882624aa20d5669dd02a5cbd54cccd3cb13dc28383e2ded982eda2d4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46172346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6c4b07b762feeda93b79ec8342fc0048393c8b42e4a47479055ffa66d14ad2f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Sat, 26 Oct 2024 00:18:17 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Sat, 26 Oct 2024 00:18:17 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
EXPOSE map[8086/tcp:{}]
# Sat, 26 Oct 2024 00:18:17 GMT
VOLUME [/var/lib/influxdb]
# Sat, 26 Oct 2024 00:18:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 26 Oct 2024 00:18:17 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832efc79eb2e8f7bbf4686f340aca032adaf1a693ccf7487d85276ae0210a9a3`  
		Last Modified: Tue, 12 Nov 2024 02:13:56 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d248baf933848bcc776a4463e3b08107f77d32dca939f04a202d83fedbfe01`  
		Last Modified: Tue, 12 Nov 2024 02:13:56 GMT  
		Size: 1.2 MB (1223726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a19aad79d7aa454c7216711056c0693f9209929f4ab726db0b29a52f9998b02`  
		Last Modified: Tue, 12 Nov 2024 02:13:57 GMT  
		Size: 41.3 MB (41322662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7668202f1e22a5df78cd8b57845dff8409e40357eb886feb8318cbd79397c43a`  
		Last Modified: Tue, 12 Nov 2024 02:13:56 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc04841e72c153311305356dd0e73d69f6765231f29d2a80ed9d5ed8c9dda22`  
		Last Modified: Tue, 12 Nov 2024 02:13:57 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2e1e59bb95f0c858a590f633f3b93c1bab619214946005e099870dee05091b`  
		Last Modified: Tue, 12 Nov 2024 02:13:57 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.7-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:a461e4fbcaa4b456b4bdd4ba46ee1becc2f6cf59010bf2302a243ae89ea88154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **770.5 KB (770460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d57b227e238bdfbc0ad4339f7024dd656f0e0e17a90b48232f33e1fd0573a714`

```dockerfile
```

-	Layers:
	-	`sha256:3fb366e475b46727356dedfd602ea98fa9dd3af189dfad284d61afe611357683`  
		Last Modified: Tue, 12 Nov 2024 02:13:56 GMT  
		Size: 753.8 KB (753822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f472b03a01bf56d4c3e8c3edd94a394ab837ebd354f1200b93178b02a82ecc6c`  
		Last Modified: Tue, 12 Nov 2024 02:13:56 GMT  
		Size: 16.6 KB (16638 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10.7-meta`

```console
$ docker pull influxdb@sha256:c22ea2644fad053077e1dc1c4d1b9ca1e01415dc764c9361ffe318202849a3ac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.7-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:c09f7a94f7aa8d82e017ae03c9cbfbf07eb6e72db0c6b35c999e7e0108688f4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.8 MB (90764624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:535d743d036954731d846bd32828608eb510fd3d2c8a09f41c0d73e634849d40`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Sat, 26 Oct 2024 00:18:17 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
EXPOSE map[8091/tcp:{}]
# Sat, 26 Oct 2024 00:18:17 GMT
VOLUME [/var/lib/influxdb]
# Sat, 26 Oct 2024 00:18:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 26 Oct 2024 00:18:17 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:c2056d933cd629f55ac55802dda223f122286bf60ec42a24f0d0f6ae2615315c`  
		Last Modified: Tue, 12 Nov 2024 00:55:16 GMT  
		Size: 55.1 MB (55108780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f895247ac53f8ccaff2388685ac5288e243187f243654f4af6205a31f8b693`  
		Last Modified: Tue, 12 Nov 2024 02:37:53 GMT  
		Size: 15.6 MB (15557923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3815d10d94129dbe2c0391239c2924feac1dee02a65a2ae82df43746c4bbdef`  
		Last Modified: Tue, 12 Nov 2024 03:14:25 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70af44e985b2c2a21660e0e91bc5a3784cde40767a13bb58180508b3b90e35b`  
		Last Modified: Tue, 12 Nov 2024 03:14:27 GMT  
		Size: 20.1 MB (20095571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1c583ec06ddaa49c7ff366bb97d15067e0d8b58f54c27cf4ab37e7db178cfc`  
		Last Modified: Tue, 12 Nov 2024 03:14:26 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8953b200e03c4f392dd626922f9ca877502ca2b2e5a40f8b87f30a0c5b4cde6`  
		Last Modified: Tue, 12 Nov 2024 03:14:25 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.7-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:024d2b0915885a0e91eb3bc72ec384279b9cdd142fac2e58be16ce841c93749f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4582011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e53c396287ec2a2b5cb51e39573b216aafeb047a8bb75e579ecc10005e7c3e1`

```dockerfile
```

-	Layers:
	-	`sha256:015086d6fbd1b706968111b7d781072240ddd53fc6bf58147a3a19684df0d43a`  
		Last Modified: Tue, 12 Nov 2024 03:14:26 GMT  
		Size: 4.6 MB (4568944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be5e2b27f02fbce16ecdc208f143385fa558efe478ec783c86a36f3141326693`  
		Last Modified: Tue, 12 Nov 2024 03:14:26 GMT  
		Size: 13.1 KB (13067 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10.7-meta-alpine`

```console
$ docker pull influxdb@sha256:87435d3f4fd949047ddbc915d3411b5023e60434d09652ffacc49cbf2923d397
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.7-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:882e8a13b101bd8e407789658a3bb4bf3fd2c5e1a6b2562809174c502250b221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.9 MB (24890556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2b92ebf5cdf243c5061bb796e7b4ed3a221ea884988df4515d8248cfc3ea3d4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Sat, 26 Oct 2024 00:18:17 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Sat, 26 Oct 2024 00:18:17 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
EXPOSE map[8091/tcp:{}]
# Sat, 26 Oct 2024 00:18:17 GMT
VOLUME [/var/lib/influxdb]
# Sat, 26 Oct 2024 00:18:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 26 Oct 2024 00:18:17 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8359fb22721bda65d61d3b3f43f9ef0bb4da1e7a89cf9bef3befc9dcd7d5c88`  
		Last Modified: Tue, 12 Nov 2024 02:13:58 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e4fa5be5bcbc133931311823895c8a9631c3bfc36b408219870173e78cd3f6`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 1.2 MB (1223725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aab0e75d4cc704b59ae8f224fc0878b1c294b912bab547f50dadb3f9b16eeee`  
		Last Modified: Tue, 12 Nov 2024 02:14:05 GMT  
		Size: 20.0 MB (20042081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e164402425990ff9b8ee202e28127f8bde685bc48d14eccce238b807f498c62f`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e70c603787aa058d11d76ad1556b160380b0da6c5bfe086ee06bd8bdb091e2b`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.7-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:d634a48656250cd109ec159741743a5f45a90cac2da999b9fe6ddde3f0330964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **693.6 KB (693575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324dbf8d99ef457bb8f6543b7d797ab1c81b99f92a765b599b942d2d0867a97f`

```dockerfile
```

-	Layers:
	-	`sha256:1f0a8bbb9b95d79cdd9a6e22d20809b4be93407345477745c4605aa07cfbb7a4`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 678.6 KB (678565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:805d6815075842407019641044c39e5cdcf1ae3d7e54775dc245065cfd6d5a1e`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 15.0 KB (15010 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11`

```console
$ docker pull influxdb@sha256:1cf6803dbe060ef285aa4a2b0ace6f759b8aa98da5e136d11200827a33aa8731
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11` - linux; amd64

```console
$ docker pull influxdb@sha256:c29184a6cb6109fb0ecf4202996233512439863bb71f151cad8be6179bc6f8f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.3 MB (117286971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ce6e4e606214e06002de59bbe0c652b0f56d6028563dcbb976278fd08ce2989`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
ARG INFLUXDB_VERSION=1.11.8
# Tue, 19 Nov 2024 19:31:41 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 19 Nov 2024 19:31:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 19 Nov 2024 19:31:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
USER influxdb
# Tue, 19 Nov 2024 19:31:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Nov 2024 19:31:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc7b6f04730c072f8b292917e0d95bb886096a2b2b1781196170965161cd27`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 24.1 MB (24058346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4805b68130959baf8f935efed7e681b7a35ed0cf98b46e585b3339aec739485`  
		Last Modified: Wed, 20 Nov 2024 00:25:20 GMT  
		Size: 1.2 KB (1197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd30bb8a1fa389c195db2c919ace20c10eb8ad8a0aa98a385e143ebf63a5141d`  
		Last Modified: Wed, 20 Nov 2024 00:25:22 GMT  
		Size: 43.7 MB (43650018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377235991185d7d28198929ca76e5f606540a426dccbb12a98a6781697c927d1`  
		Last Modified: Wed, 20 Nov 2024 00:25:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32eb31848b11c8cc1c408f8675fad75175b8a571189581ee1028787c80de6a20`  
		Last Modified: Wed, 20 Nov 2024 00:25:20 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8b0393c812e45b9b5380103b5431619342e5355ca244305b4f34475738ec74`  
		Last Modified: Wed, 20 Nov 2024 00:25:21 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11` - unknown; unknown

```console
$ docker pull influxdb@sha256:ee6915e993489a3bb035a9bc535f8e3805d981784b2eeefafa269f28eb790142
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4906987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11f8d46958e4503f34ba17f712d4cf26f118842f6b736e51978e2a0da2c27463`

```dockerfile
```

-	Layers:
	-	`sha256:ed75718ef00881e65076272c57ac4f2d65428897d98527d95e197bece290e132`  
		Last Modified: Wed, 20 Nov 2024 00:25:21 GMT  
		Size: 4.9 MB (4891458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28efaf0036a4098f006996d3b728f7c764d78bc063a3d6912674579b8d436338`  
		Last Modified: Wed, 20 Nov 2024 00:25:20 GMT  
		Size: 15.5 KB (15529 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:fd38e6b09953a135d7573ea05965752c1637b7a15f9f5ddad73ca989f1d3d450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114307342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e3829498304a4db6e4d63edd3a62b614c665ce846c245cb0659568fa51639e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
ARG INFLUXDB_VERSION=1.11.8
# Tue, 19 Nov 2024 19:31:41 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 19 Nov 2024 19:31:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 19 Nov 2024 19:31:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
USER influxdb
# Tue, 19 Nov 2024 19:31:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Nov 2024 19:31:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:1a3f1864ec54b1398987bbe673e93d8b09842ecd51e86ab87d64857b70d188b1`  
		Last Modified: Tue, 12 Nov 2024 00:56:20 GMT  
		Size: 49.6 MB (49587201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464f864cfaa846fbe1b8a889827404e18374f805d29d77c288a813ae8c4f6d91`  
		Last Modified: Tue, 12 Nov 2024 11:16:03 GMT  
		Size: 23.6 MB (23598253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2982cbcc0143caa5c3b10fd9b2b39a6a6f75d39fc8b09e4386d84508665689`  
		Last Modified: Wed, 20 Nov 2024 00:27:19 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6cefe59b37a495176c3f0e9a86970cd9267e3331de679b1191ef00ee2e7d4fc`  
		Last Modified: Wed, 20 Nov 2024 00:27:20 GMT  
		Size: 41.1 MB (41118979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ef103a168f6122e92c679311d6594615621e1cd76484abf3916fd9c8851779`  
		Last Modified: Wed, 20 Nov 2024 00:27:19 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390c4da15947e0d8cb60494c8e028f32d334d80486357871b7a73c02c28a2a2a`  
		Last Modified: Wed, 20 Nov 2024 00:27:19 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc12a91fefd48000113a1e7f161e4706a5547892df9dfb205fc451433fb2c78`  
		Last Modified: Wed, 20 Nov 2024 00:27:20 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11` - unknown; unknown

```console
$ docker pull influxdb@sha256:468a008305a1f3a3a534e4746c771f0fb7fb523d14c4c65a5f7622602bfa7508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4906555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b525b11a5610d88616999879df1551018663c98c8ed2126507ca3dbfb8a5270`

```dockerfile
```

-	Layers:
	-	`sha256:bbe8a2b27bd5d971e3419879d68deeb7556d188c27e642934b9c59e5fcd39215`  
		Last Modified: Wed, 20 Nov 2024 00:27:19 GMT  
		Size: 4.9 MB (4890932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:736833f64375ccdf3b3b16fc4edad41956c8f41737878ceaff95e2352d7d82fa`  
		Last Modified: Wed, 20 Nov 2024 00:27:19 GMT  
		Size: 15.6 KB (15623 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-alpine`

```console
$ docker pull influxdb@sha256:ed211b5ec624c9ba035e0c87f213da207c244b0c09c496fdbf2b78d8987d04f8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:4dedd2b1a4953def0324b230cf81d2b0eae1752bd1da3f9a8bc83a673129a53a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42918525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17469727bbc0aeb0f24bf7f297ba7c7bd654325f849f3aa2ea39c99ecd519118`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 19 Nov 2024 19:31:41 GMT
RUN apk add --no-cache       bash       ca-certificates       tzdata &&     update-ca-certificates # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
ARG INFLUXDB_VERSION=1.11.8
# Tue, 19 Nov 2024 19:31:41 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN apk add --no-cache --virtual .build-deps       curl       gnupg       tar &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     case "$(apk --print-arch)" in       x86_64)  ARCH=amd64 ;;       aarch64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_TAR=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_TAR}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_TAR}" &&     tar -xf "${INFLUXDB_TAR}" -C /usr/bin       influx       influx_inspect       influxd &&     rm -rf "${INFLUXDB_TAR}"            "${INFLUXDB_ASC}" &&     apk del .build-deps # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 19 Nov 2024 19:31:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 19 Nov 2024 19:31:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
USER influxdb
# Tue, 19 Nov 2024 19:31:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Nov 2024 19:31:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2793272d884821435771c99841d1ca8ff8ecfca52dd78dfb6fbfa2ebb74eccfd`  
		Last Modified: Wed, 20 Nov 2024 00:25:02 GMT  
		Size: 1.2 MB (1223733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d2d868e1ee46051f87a8ab223e92957b23561da0b5d11081f3f25ed9d26a27`  
		Last Modified: Wed, 20 Nov 2024 00:25:03 GMT  
		Size: 38.1 MB (38068172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1757fc067058bd2a294ffa84a09e17388bfbe75ee440ccb0fade9ceb45d3853e`  
		Last Modified: Wed, 20 Nov 2024 00:25:02 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7279ca50b6e30592d1cbf15341b477df4e373b48799baee189de8fe767e4a62`  
		Last Modified: Wed, 20 Nov 2024 00:25:02 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969453f510b42b35553198ac427e6216591a10ddeecc987aa21633e7fc820ec5`  
		Last Modified: Wed, 20 Nov 2024 00:25:03 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3225b51e7a8c4cbee0c655692e7bd3421ad01e110a82c14959ef7e4234e916a5`  
		Last Modified: Wed, 20 Nov 2024 00:25:03 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:9eed1e66b4f319a27ca52a19d4316f2015509f2215e3a8ddbba8408e80514379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.5 KB (759529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1880ce4830e437f0aa58337a983b3594e42ce7dada8eea7e76eda143b1d95fb5`

```dockerfile
```

-	Layers:
	-	`sha256:75fe1ae13c267c3e7c6ffaae46b71425490b014a023d7d8abbf9462faf4ccb30`  
		Last Modified: Wed, 20 Nov 2024 00:25:02 GMT  
		Size: 741.7 KB (741652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:067dd82376ee3e3c0a4e4ec09cecdd421b823b14c3d9311719aa36e88763bc03`  
		Last Modified: Wed, 20 Nov 2024 00:25:02 GMT  
		Size: 17.9 KB (17877 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:190b720840638bfbd5d3c528cddbed4f95ad31246f2d44c36df5dca148a89125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40939034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b342a55f784f854f3da72a7affc16cff60b51dada18d6981ce25eb3a90efe947`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 19 Nov 2024 19:31:41 GMT
RUN apk add --no-cache       bash       ca-certificates       tzdata &&     update-ca-certificates # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
ARG INFLUXDB_VERSION=1.11.8
# Tue, 19 Nov 2024 19:31:41 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN apk add --no-cache --virtual .build-deps       curl       gnupg       tar &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     case "$(apk --print-arch)" in       x86_64)  ARCH=amd64 ;;       aarch64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_TAR=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_TAR}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_TAR}" &&     tar -xf "${INFLUXDB_TAR}" -C /usr/bin       influx       influx_inspect       influxd &&     rm -rf "${INFLUXDB_TAR}"            "${INFLUXDB_ASC}" &&     apk del .build-deps # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 19 Nov 2024 19:31:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 19 Nov 2024 19:31:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
USER influxdb
# Tue, 19 Nov 2024 19:31:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Nov 2024 19:31:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f9fa33afbb704fe83e860e0ae0055706616de1db8054776ba772bbb2b6ef7f`  
		Last Modified: Wed, 20 Nov 2024 00:28:00 GMT  
		Size: 1.3 MB (1303113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b92b2b4f217d6fc6583176acb74b3ba4831b3a7580a8e33232e4b8ecb1615a`  
		Last Modified: Wed, 20 Nov 2024 00:28:00 GMT  
		Size: 35.5 MB (35545472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa8fbc7b8e59995519cb14a58f73ae8a2e8df346f77a21d1bf3e4e5ebdfdcff`  
		Last Modified: Wed, 20 Nov 2024 00:27:59 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579c4c0d23065d326e5fc90cca349de50739cf17e954c489ddb1421125a8a3b2`  
		Last Modified: Wed, 20 Nov 2024 00:27:59 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf86b4f1c9152aa4f4f503a509c56e1b5e0c97a96fc78c80c7d15661101b516`  
		Last Modified: Wed, 20 Nov 2024 00:28:00 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f121dadcfa53fe0402bab5c0776c909f6768897033c8bbeceb45e729e9ae2a`  
		Last Modified: Wed, 20 Nov 2024 00:28:00 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:3d2e39c8ca4245a1e625ce8ef7279846d806d1b62eb5eb68a8b3c4392eadd596
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **758.9 KB (758876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da139cd58b5bdad8aa305c2e58a685f34b7ec1d76b9ef2f0ff834e62439b8103`

```dockerfile
```

-	Layers:
	-	`sha256:b42326533f84dfafe26ac54cd44920409aff668b578393dd883e14a3bdf05735`  
		Last Modified: Wed, 20 Nov 2024 00:28:00 GMT  
		Size: 740.9 KB (740889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d05e76b19d9a4e9ffc2575bb31d716bd95844acf2087db6ce50ca2c77f0c5efb`  
		Last Modified: Wed, 20 Nov 2024 00:27:59 GMT  
		Size: 18.0 KB (17987 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-data`

```console
$ docker pull influxdb@sha256:6986137e924653d40a91082be84a964ddae4d7defe0a4ca5287bf2e98c838350
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data` - linux; amd64

```console
$ docker pull influxdb@sha256:3ba39fa6f5abd05fe5bc02c8d3f131868d2b94e0672236ff1a327584a4725875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.8 MB (112816885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e88aceaf569b4835540c732b702be91e31899de8879ee20efac6ce0333245aa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
ENV INFLUXDB_VERSION=1.11.8-c1.11.8
# Tue, 19 Nov 2024 19:31:41 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 19 Nov 2024 19:31:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 19 Nov 2024 19:31:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Nov 2024 19:31:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc7b6f04730c072f8b292917e0d95bb886096a2b2b1781196170965161cd27`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 24.1 MB (24058346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60baeca0315dbd2a3ad3300cdbd1f616c52244c2b3912dab48440df0535896e`  
		Last Modified: Wed, 20 Nov 2024 00:25:02 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5759aea903a967583738e0d49769a005cb39ea06a3e15016c56e41128131b1fd`  
		Last Modified: Wed, 20 Nov 2024 00:25:02 GMT  
		Size: 39.2 MB (39179299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b38c98256f458b595c7b022f187c34d2daf20dd3e3acdc1896f4d5b6110eb18e`  
		Last Modified: Wed, 20 Nov 2024 00:25:02 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e271acaa2e0b501f40dd6834334b327c9acef338a507914e8f9f9314319a65`  
		Last Modified: Wed, 20 Nov 2024 00:25:02 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4bbcdebeffbeccd1460a0341926c7f1627d7f6a93b359b49515c493745440b`  
		Last Modified: Wed, 20 Nov 2024 00:25:02 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:28496e3836cc23820e68f0374b15bfa039528a6a3dbaa8f5dfd9f980da901369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4530767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fcfe04b650b75e0478d7210133f10041d0b086599d04c15aafbfdc2612aac62`

```dockerfile
```

-	Layers:
	-	`sha256:5e4f39c3db551d2d76ce119ced1c77f9edbca0a9f7e6e61eab93f918b9845fa6`  
		Last Modified: Wed, 20 Nov 2024 00:25:02 GMT  
		Size: 4.5 MB (4516059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da601bc8cf6c76bebafd451bfe7d78475f7b922f41fd8dfe0ab42174f9b199fe`  
		Last Modified: Wed, 20 Nov 2024 00:25:02 GMT  
		Size: 14.7 KB (14708 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-data-alpine`

```console
$ docker pull influxdb@sha256:288f736379506940654a8e47ebaf95b5e87e20fc0fdad1c74724e3f7460bde56
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:4cb5721ebf584c040f68be523e91508d6205c2a73e65d8d2cb03588fd73038c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (43973338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d6248dc814037b21f9eb05b292035f8da11c8ffd39c00a7d55a58ec2895449d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 19 Nov 2024 19:31:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
ENV INFLUXDB_VERSION=1.11.8-c1.11.8
# Tue, 19 Nov 2024 19:31:41 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 19 Nov 2024 19:31:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 19 Nov 2024 19:31:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Nov 2024 19:31:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d80acf73fb8fea9aeaadb2463e5a9f671d02927cebe445f1d8cbb1d18a675c`  
		Last Modified: Wed, 20 Nov 2024 00:24:56 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd13b8e8a1c80d9f42ad85fbace5682369a0c0024f10ff6af5f4ff83fc005f9`  
		Last Modified: Wed, 20 Nov 2024 00:24:56 GMT  
		Size: 1.2 MB (1223730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9051474aac3e1b76da927a305d29d391d6267dcf5515c860c654fbc076d9e057`  
		Last Modified: Wed, 20 Nov 2024 00:24:57 GMT  
		Size: 39.1 MB (39123651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a2dcb246ea6696fb0e0a14532fcd19846488063bed04b8801876d8a9f8b8b0`  
		Last Modified: Wed, 20 Nov 2024 00:24:56 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7eabf1d0989b4f74a59a1877d125fbbc523b6e6371051dd0ab03ecac1ca617`  
		Last Modified: Wed, 20 Nov 2024 00:24:57 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21c236bb0e55f72aaa0e1dbbba56b1392398097631e132b8033cb24fae6e4e0`  
		Last Modified: Wed, 20 Nov 2024 00:24:57 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:4fb7e6509f3517b30f0abfb315a6cd7746efa2831f42980a233c7927dc238af9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **768.7 KB (768706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc6f52e07c7dfdc1be965ae2450fa531bb283310e60c557ea43662ea8ed66f01`

```dockerfile
```

-	Layers:
	-	`sha256:0def192ebc1e9811ca5b8ca3c1d51b3d124f561d2517dd8d50969755b5eec371`  
		Last Modified: Wed, 20 Nov 2024 00:24:56 GMT  
		Size: 752.1 KB (752067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fb21b1f76dad1d0a636e6d7ad353ae908eed29d8f039391087e486723fe55dc`  
		Last Modified: Wed, 20 Nov 2024 00:24:56 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-meta`

```console
$ docker pull influxdb@sha256:c6cb9c93a94a3a4bf6965c5335853bc0413c75bde77d959a829d6ee935a9ffd5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:32c1e9bb59619eef76306ee325176f9c39c8e031f27c23b0268e8951c1b4b130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (91972946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed49731bdf3bf4e4bc0aa2fe4f894d7bb583a3889dda0e90629a8020717ff6ba`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
ENV INFLUXDB_VERSION=1.11.8-c1.11.8
# Tue, 19 Nov 2024 19:31:41 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 19 Nov 2024 19:31:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 19 Nov 2024 19:31:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Nov 2024 19:31:41 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc7b6f04730c072f8b292917e0d95bb886096a2b2b1781196170965161cd27`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 24.1 MB (24058346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a0888703b42021e4a68d7cecddfc40215e66eb38e41cd72b478705caafed80`  
		Last Modified: Wed, 20 Nov 2024 00:24:57 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a034dcb4c43a9ef0eae8e1b2e81bd27c20dc32276f3e65fd192b63d4fe6852`  
		Last Modified: Wed, 20 Nov 2024 00:24:58 GMT  
		Size: 18.3 MB (18336566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f2ab4dcdd5db578662f0e334346ff5033e7b5b413544b4fef8e25bde0fc403`  
		Last Modified: Wed, 20 Nov 2024 00:24:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9bb235be4e258e8ce13912959c3aea0f0687f38392ce930f35b2a7d4c5b1424`  
		Last Modified: Wed, 20 Nov 2024 00:24:57 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:18087de731c6645ad44e6638cecb0fc4fdb530e431f98a3a4b6a174a92b317b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4454692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27279256cc97913622802880cb5c20259aefe1c0f5d6df292e1f2e73fcfba676`

```dockerfile
```

-	Layers:
	-	`sha256:38589865714c0100bf82b7afec5a63ba52285630844eff5795aaf20a0956b711`  
		Last Modified: Wed, 20 Nov 2024 00:24:57 GMT  
		Size: 4.4 MB (4441626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53ba8f1b2a19cd030219742808bb03a8b1fd0336686d4ac8aa9c77a67197ad1b`  
		Last Modified: Wed, 20 Nov 2024 00:24:57 GMT  
		Size: 13.1 KB (13066 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-meta-alpine`

```console
$ docker pull influxdb@sha256:c8d54f52ebaf36b6f9a1dbdd4ef70d1b1f47576cdf43d5fb1188d34eee94b448
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:48940da7720f465b2481c0b1155a99714376d961382d5efa2a46b5f5ea89661a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23138445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1adc4b3962abde1fe47f8250497101fd8ca9b022648d5a5f24164ecded3f093`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 19 Nov 2024 19:31:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
ENV INFLUXDB_VERSION=1.11.8-c1.11.8
# Tue, 19 Nov 2024 19:31:41 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 19 Nov 2024 19:31:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 19 Nov 2024 19:31:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Nov 2024 19:31:41 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0438db35e61425aedea3743f2915dc31159fd22a62ce36c485c9c7573e596506`  
		Last Modified: Wed, 20 Nov 2024 00:25:00 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777ba3e191739e8b0a9bfb9aea7d18d578b9f3babc7fef147b0fbd28cdf89c55`  
		Last Modified: Wed, 20 Nov 2024 00:25:00 GMT  
		Size: 1.2 MB (1223735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b81d02fd773a9efce7e9f927510a54dd62d06333c919c1d34f605831895fd37`  
		Last Modified: Wed, 20 Nov 2024 00:25:00 GMT  
		Size: 18.3 MB (18289962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36fb0fe55fa0844db679db1e623ce0f636160818b153bfcbc1ff0a33c0654347`  
		Last Modified: Wed, 20 Nov 2024 00:25:00 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30456092fceaf011a18abfd64e9effcb5582f29154a0e11df88b27230b428e9`  
		Last Modified: Wed, 20 Nov 2024 00:25:00 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:9e5eabc4b08db9294fb88b27fa2d0cfa8f8f7152adf488e80043f02ff4403f23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **693.4 KB (693431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d38465e4fec86919ff2fb5c96060831ce9cce737b9175603cc109ab3085e61f9`

```dockerfile
```

-	Layers:
	-	`sha256:8920a1255dd0e846042c4dc32732b011a942fd0811eeeef9b8aa48215a7926ee`  
		Last Modified: Wed, 20 Nov 2024 00:24:59 GMT  
		Size: 678.4 KB (678421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90ebba546e122029bf650e9faf1659849b554ded3881979ac774d19a5f8a0225`  
		Last Modified: Wed, 20 Nov 2024 00:25:00 GMT  
		Size: 15.0 KB (15010 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.8`

```console
$ docker pull influxdb@sha256:1cf6803dbe060ef285aa4a2b0ace6f759b8aa98da5e136d11200827a33aa8731
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11.8` - linux; amd64

```console
$ docker pull influxdb@sha256:c29184a6cb6109fb0ecf4202996233512439863bb71f151cad8be6179bc6f8f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.3 MB (117286971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ce6e4e606214e06002de59bbe0c652b0f56d6028563dcbb976278fd08ce2989`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
ARG INFLUXDB_VERSION=1.11.8
# Tue, 19 Nov 2024 19:31:41 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 19 Nov 2024 19:31:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 19 Nov 2024 19:31:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
USER influxdb
# Tue, 19 Nov 2024 19:31:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Nov 2024 19:31:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc7b6f04730c072f8b292917e0d95bb886096a2b2b1781196170965161cd27`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 24.1 MB (24058346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4805b68130959baf8f935efed7e681b7a35ed0cf98b46e585b3339aec739485`  
		Last Modified: Wed, 20 Nov 2024 00:25:20 GMT  
		Size: 1.2 KB (1197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd30bb8a1fa389c195db2c919ace20c10eb8ad8a0aa98a385e143ebf63a5141d`  
		Last Modified: Wed, 20 Nov 2024 00:25:22 GMT  
		Size: 43.7 MB (43650018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377235991185d7d28198929ca76e5f606540a426dccbb12a98a6781697c927d1`  
		Last Modified: Wed, 20 Nov 2024 00:25:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32eb31848b11c8cc1c408f8675fad75175b8a571189581ee1028787c80de6a20`  
		Last Modified: Wed, 20 Nov 2024 00:25:20 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8b0393c812e45b9b5380103b5431619342e5355ca244305b4f34475738ec74`  
		Last Modified: Wed, 20 Nov 2024 00:25:21 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:ee6915e993489a3bb035a9bc535f8e3805d981784b2eeefafa269f28eb790142
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4906987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11f8d46958e4503f34ba17f712d4cf26f118842f6b736e51978e2a0da2c27463`

```dockerfile
```

-	Layers:
	-	`sha256:ed75718ef00881e65076272c57ac4f2d65428897d98527d95e197bece290e132`  
		Last Modified: Wed, 20 Nov 2024 00:25:21 GMT  
		Size: 4.9 MB (4891458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28efaf0036a4098f006996d3b728f7c764d78bc063a3d6912674579b8d436338`  
		Last Modified: Wed, 20 Nov 2024 00:25:20 GMT  
		Size: 15.5 KB (15529 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:fd38e6b09953a135d7573ea05965752c1637b7a15f9f5ddad73ca989f1d3d450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114307342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e3829498304a4db6e4d63edd3a62b614c665ce846c245cb0659568fa51639e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
ARG INFLUXDB_VERSION=1.11.8
# Tue, 19 Nov 2024 19:31:41 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 19 Nov 2024 19:31:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 19 Nov 2024 19:31:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
USER influxdb
# Tue, 19 Nov 2024 19:31:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Nov 2024 19:31:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:1a3f1864ec54b1398987bbe673e93d8b09842ecd51e86ab87d64857b70d188b1`  
		Last Modified: Tue, 12 Nov 2024 00:56:20 GMT  
		Size: 49.6 MB (49587201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464f864cfaa846fbe1b8a889827404e18374f805d29d77c288a813ae8c4f6d91`  
		Last Modified: Tue, 12 Nov 2024 11:16:03 GMT  
		Size: 23.6 MB (23598253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2982cbcc0143caa5c3b10fd9b2b39a6a6f75d39fc8b09e4386d84508665689`  
		Last Modified: Wed, 20 Nov 2024 00:27:19 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6cefe59b37a495176c3f0e9a86970cd9267e3331de679b1191ef00ee2e7d4fc`  
		Last Modified: Wed, 20 Nov 2024 00:27:20 GMT  
		Size: 41.1 MB (41118979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ef103a168f6122e92c679311d6594615621e1cd76484abf3916fd9c8851779`  
		Last Modified: Wed, 20 Nov 2024 00:27:19 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390c4da15947e0d8cb60494c8e028f32d334d80486357871b7a73c02c28a2a2a`  
		Last Modified: Wed, 20 Nov 2024 00:27:19 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc12a91fefd48000113a1e7f161e4706a5547892df9dfb205fc451433fb2c78`  
		Last Modified: Wed, 20 Nov 2024 00:27:20 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:468a008305a1f3a3a534e4746c771f0fb7fb523d14c4c65a5f7622602bfa7508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4906555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b525b11a5610d88616999879df1551018663c98c8ed2126507ca3dbfb8a5270`

```dockerfile
```

-	Layers:
	-	`sha256:bbe8a2b27bd5d971e3419879d68deeb7556d188c27e642934b9c59e5fcd39215`  
		Last Modified: Wed, 20 Nov 2024 00:27:19 GMT  
		Size: 4.9 MB (4890932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:736833f64375ccdf3b3b16fc4edad41956c8f41737878ceaff95e2352d7d82fa`  
		Last Modified: Wed, 20 Nov 2024 00:27:19 GMT  
		Size: 15.6 KB (15623 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.8-alpine`

```console
$ docker pull influxdb@sha256:ed211b5ec624c9ba035e0c87f213da207c244b0c09c496fdbf2b78d8987d04f8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11.8-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:4dedd2b1a4953def0324b230cf81d2b0eae1752bd1da3f9a8bc83a673129a53a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42918525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17469727bbc0aeb0f24bf7f297ba7c7bd654325f849f3aa2ea39c99ecd519118`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 19 Nov 2024 19:31:41 GMT
RUN apk add --no-cache       bash       ca-certificates       tzdata &&     update-ca-certificates # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
ARG INFLUXDB_VERSION=1.11.8
# Tue, 19 Nov 2024 19:31:41 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN apk add --no-cache --virtual .build-deps       curl       gnupg       tar &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     case "$(apk --print-arch)" in       x86_64)  ARCH=amd64 ;;       aarch64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_TAR=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_TAR}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_TAR}" &&     tar -xf "${INFLUXDB_TAR}" -C /usr/bin       influx       influx_inspect       influxd &&     rm -rf "${INFLUXDB_TAR}"            "${INFLUXDB_ASC}" &&     apk del .build-deps # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 19 Nov 2024 19:31:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 19 Nov 2024 19:31:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
USER influxdb
# Tue, 19 Nov 2024 19:31:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Nov 2024 19:31:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2793272d884821435771c99841d1ca8ff8ecfca52dd78dfb6fbfa2ebb74eccfd`  
		Last Modified: Wed, 20 Nov 2024 00:25:02 GMT  
		Size: 1.2 MB (1223733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d2d868e1ee46051f87a8ab223e92957b23561da0b5d11081f3f25ed9d26a27`  
		Last Modified: Wed, 20 Nov 2024 00:25:03 GMT  
		Size: 38.1 MB (38068172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1757fc067058bd2a294ffa84a09e17388bfbe75ee440ccb0fade9ceb45d3853e`  
		Last Modified: Wed, 20 Nov 2024 00:25:02 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7279ca50b6e30592d1cbf15341b477df4e373b48799baee189de8fe767e4a62`  
		Last Modified: Wed, 20 Nov 2024 00:25:02 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969453f510b42b35553198ac427e6216591a10ddeecc987aa21633e7fc820ec5`  
		Last Modified: Wed, 20 Nov 2024 00:25:03 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3225b51e7a8c4cbee0c655692e7bd3421ad01e110a82c14959ef7e4234e916a5`  
		Last Modified: Wed, 20 Nov 2024 00:25:03 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:9eed1e66b4f319a27ca52a19d4316f2015509f2215e3a8ddbba8408e80514379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.5 KB (759529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1880ce4830e437f0aa58337a983b3594e42ce7dada8eea7e76eda143b1d95fb5`

```dockerfile
```

-	Layers:
	-	`sha256:75fe1ae13c267c3e7c6ffaae46b71425490b014a023d7d8abbf9462faf4ccb30`  
		Last Modified: Wed, 20 Nov 2024 00:25:02 GMT  
		Size: 741.7 KB (741652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:067dd82376ee3e3c0a4e4ec09cecdd421b823b14c3d9311719aa36e88763bc03`  
		Last Modified: Wed, 20 Nov 2024 00:25:02 GMT  
		Size: 17.9 KB (17877 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11.8-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:190b720840638bfbd5d3c528cddbed4f95ad31246f2d44c36df5dca148a89125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40939034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b342a55f784f854f3da72a7affc16cff60b51dada18d6981ce25eb3a90efe947`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 19 Nov 2024 19:31:41 GMT
RUN apk add --no-cache       bash       ca-certificates       tzdata &&     update-ca-certificates # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
ARG INFLUXDB_VERSION=1.11.8
# Tue, 19 Nov 2024 19:31:41 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN apk add --no-cache --virtual .build-deps       curl       gnupg       tar &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     case "$(apk --print-arch)" in       x86_64)  ARCH=amd64 ;;       aarch64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_TAR=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_TAR}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_TAR}" &&     tar -xf "${INFLUXDB_TAR}" -C /usr/bin       influx       influx_inspect       influxd &&     rm -rf "${INFLUXDB_TAR}"            "${INFLUXDB_ASC}" &&     apk del .build-deps # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 19 Nov 2024 19:31:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 19 Nov 2024 19:31:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
USER influxdb
# Tue, 19 Nov 2024 19:31:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Nov 2024 19:31:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f9fa33afbb704fe83e860e0ae0055706616de1db8054776ba772bbb2b6ef7f`  
		Last Modified: Wed, 20 Nov 2024 00:28:00 GMT  
		Size: 1.3 MB (1303113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b92b2b4f217d6fc6583176acb74b3ba4831b3a7580a8e33232e4b8ecb1615a`  
		Last Modified: Wed, 20 Nov 2024 00:28:00 GMT  
		Size: 35.5 MB (35545472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa8fbc7b8e59995519cb14a58f73ae8a2e8df346f77a21d1bf3e4e5ebdfdcff`  
		Last Modified: Wed, 20 Nov 2024 00:27:59 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579c4c0d23065d326e5fc90cca349de50739cf17e954c489ddb1421125a8a3b2`  
		Last Modified: Wed, 20 Nov 2024 00:27:59 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf86b4f1c9152aa4f4f503a509c56e1b5e0c97a96fc78c80c7d15661101b516`  
		Last Modified: Wed, 20 Nov 2024 00:28:00 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f121dadcfa53fe0402bab5c0776c909f6768897033c8bbeceb45e729e9ae2a`  
		Last Modified: Wed, 20 Nov 2024 00:28:00 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:3d2e39c8ca4245a1e625ce8ef7279846d806d1b62eb5eb68a8b3c4392eadd596
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **758.9 KB (758876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da139cd58b5bdad8aa305c2e58a685f34b7ec1d76b9ef2f0ff834e62439b8103`

```dockerfile
```

-	Layers:
	-	`sha256:b42326533f84dfafe26ac54cd44920409aff668b578393dd883e14a3bdf05735`  
		Last Modified: Wed, 20 Nov 2024 00:28:00 GMT  
		Size: 740.9 KB (740889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d05e76b19d9a4e9ffc2575bb31d716bd95844acf2087db6ce50ca2c77f0c5efb`  
		Last Modified: Wed, 20 Nov 2024 00:27:59 GMT  
		Size: 18.0 KB (17987 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.8-data`

```console
$ docker pull influxdb@sha256:6986137e924653d40a91082be84a964ddae4d7defe0a4ca5287bf2e98c838350
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.8-data` - linux; amd64

```console
$ docker pull influxdb@sha256:3ba39fa6f5abd05fe5bc02c8d3f131868d2b94e0672236ff1a327584a4725875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.8 MB (112816885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e88aceaf569b4835540c732b702be91e31899de8879ee20efac6ce0333245aa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
ENV INFLUXDB_VERSION=1.11.8-c1.11.8
# Tue, 19 Nov 2024 19:31:41 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 19 Nov 2024 19:31:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 19 Nov 2024 19:31:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Nov 2024 19:31:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc7b6f04730c072f8b292917e0d95bb886096a2b2b1781196170965161cd27`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 24.1 MB (24058346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60baeca0315dbd2a3ad3300cdbd1f616c52244c2b3912dab48440df0535896e`  
		Last Modified: Wed, 20 Nov 2024 00:25:02 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5759aea903a967583738e0d49769a005cb39ea06a3e15016c56e41128131b1fd`  
		Last Modified: Wed, 20 Nov 2024 00:25:02 GMT  
		Size: 39.2 MB (39179299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b38c98256f458b595c7b022f187c34d2daf20dd3e3acdc1896f4d5b6110eb18e`  
		Last Modified: Wed, 20 Nov 2024 00:25:02 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e271acaa2e0b501f40dd6834334b327c9acef338a507914e8f9f9314319a65`  
		Last Modified: Wed, 20 Nov 2024 00:25:02 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4bbcdebeffbeccd1460a0341926c7f1627d7f6a93b359b49515c493745440b`  
		Last Modified: Wed, 20 Nov 2024 00:25:02 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:28496e3836cc23820e68f0374b15bfa039528a6a3dbaa8f5dfd9f980da901369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4530767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fcfe04b650b75e0478d7210133f10041d0b086599d04c15aafbfdc2612aac62`

```dockerfile
```

-	Layers:
	-	`sha256:5e4f39c3db551d2d76ce119ced1c77f9edbca0a9f7e6e61eab93f918b9845fa6`  
		Last Modified: Wed, 20 Nov 2024 00:25:02 GMT  
		Size: 4.5 MB (4516059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da601bc8cf6c76bebafd451bfe7d78475f7b922f41fd8dfe0ab42174f9b199fe`  
		Last Modified: Wed, 20 Nov 2024 00:25:02 GMT  
		Size: 14.7 KB (14708 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.8-data-alpine`

```console
$ docker pull influxdb@sha256:288f736379506940654a8e47ebaf95b5e87e20fc0fdad1c74724e3f7460bde56
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.8-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:4cb5721ebf584c040f68be523e91508d6205c2a73e65d8d2cb03588fd73038c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (43973338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d6248dc814037b21f9eb05b292035f8da11c8ffd39c00a7d55a58ec2895449d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 19 Nov 2024 19:31:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
ENV INFLUXDB_VERSION=1.11.8-c1.11.8
# Tue, 19 Nov 2024 19:31:41 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 19 Nov 2024 19:31:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 19 Nov 2024 19:31:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Nov 2024 19:31:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d80acf73fb8fea9aeaadb2463e5a9f671d02927cebe445f1d8cbb1d18a675c`  
		Last Modified: Wed, 20 Nov 2024 00:24:56 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd13b8e8a1c80d9f42ad85fbace5682369a0c0024f10ff6af5f4ff83fc005f9`  
		Last Modified: Wed, 20 Nov 2024 00:24:56 GMT  
		Size: 1.2 MB (1223730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9051474aac3e1b76da927a305d29d391d6267dcf5515c860c654fbc076d9e057`  
		Last Modified: Wed, 20 Nov 2024 00:24:57 GMT  
		Size: 39.1 MB (39123651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a2dcb246ea6696fb0e0a14532fcd19846488063bed04b8801876d8a9f8b8b0`  
		Last Modified: Wed, 20 Nov 2024 00:24:56 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7eabf1d0989b4f74a59a1877d125fbbc523b6e6371051dd0ab03ecac1ca617`  
		Last Modified: Wed, 20 Nov 2024 00:24:57 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21c236bb0e55f72aaa0e1dbbba56b1392398097631e132b8033cb24fae6e4e0`  
		Last Modified: Wed, 20 Nov 2024 00:24:57 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:4fb7e6509f3517b30f0abfb315a6cd7746efa2831f42980a233c7927dc238af9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **768.7 KB (768706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc6f52e07c7dfdc1be965ae2450fa531bb283310e60c557ea43662ea8ed66f01`

```dockerfile
```

-	Layers:
	-	`sha256:0def192ebc1e9811ca5b8ca3c1d51b3d124f561d2517dd8d50969755b5eec371`  
		Last Modified: Wed, 20 Nov 2024 00:24:56 GMT  
		Size: 752.1 KB (752067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fb21b1f76dad1d0a636e6d7ad353ae908eed29d8f039391087e486723fe55dc`  
		Last Modified: Wed, 20 Nov 2024 00:24:56 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.8-meta`

```console
$ docker pull influxdb@sha256:c6cb9c93a94a3a4bf6965c5335853bc0413c75bde77d959a829d6ee935a9ffd5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.8-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:32c1e9bb59619eef76306ee325176f9c39c8e031f27c23b0268e8951c1b4b130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (91972946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed49731bdf3bf4e4bc0aa2fe4f894d7bb583a3889dda0e90629a8020717ff6ba`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
ENV INFLUXDB_VERSION=1.11.8-c1.11.8
# Tue, 19 Nov 2024 19:31:41 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 19 Nov 2024 19:31:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 19 Nov 2024 19:31:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Nov 2024 19:31:41 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc7b6f04730c072f8b292917e0d95bb886096a2b2b1781196170965161cd27`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 24.1 MB (24058346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a0888703b42021e4a68d7cecddfc40215e66eb38e41cd72b478705caafed80`  
		Last Modified: Wed, 20 Nov 2024 00:24:57 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a034dcb4c43a9ef0eae8e1b2e81bd27c20dc32276f3e65fd192b63d4fe6852`  
		Last Modified: Wed, 20 Nov 2024 00:24:58 GMT  
		Size: 18.3 MB (18336566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f2ab4dcdd5db578662f0e334346ff5033e7b5b413544b4fef8e25bde0fc403`  
		Last Modified: Wed, 20 Nov 2024 00:24:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9bb235be4e258e8ce13912959c3aea0f0687f38392ce930f35b2a7d4c5b1424`  
		Last Modified: Wed, 20 Nov 2024 00:24:57 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:18087de731c6645ad44e6638cecb0fc4fdb530e431f98a3a4b6a174a92b317b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4454692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27279256cc97913622802880cb5c20259aefe1c0f5d6df292e1f2e73fcfba676`

```dockerfile
```

-	Layers:
	-	`sha256:38589865714c0100bf82b7afec5a63ba52285630844eff5795aaf20a0956b711`  
		Last Modified: Wed, 20 Nov 2024 00:24:57 GMT  
		Size: 4.4 MB (4441626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53ba8f1b2a19cd030219742808bb03a8b1fd0336686d4ac8aa9c77a67197ad1b`  
		Last Modified: Wed, 20 Nov 2024 00:24:57 GMT  
		Size: 13.1 KB (13066 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.8-meta-alpine`

```console
$ docker pull influxdb@sha256:c8d54f52ebaf36b6f9a1dbdd4ef70d1b1f47576cdf43d5fb1188d34eee94b448
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.8-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:48940da7720f465b2481c0b1155a99714376d961382d5efa2a46b5f5ea89661a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23138445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1adc4b3962abde1fe47f8250497101fd8ca9b022648d5a5f24164ecded3f093`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 19 Nov 2024 19:31:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
ENV INFLUXDB_VERSION=1.11.8-c1.11.8
# Tue, 19 Nov 2024 19:31:41 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 19 Nov 2024 19:31:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 19 Nov 2024 19:31:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Nov 2024 19:31:41 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0438db35e61425aedea3743f2915dc31159fd22a62ce36c485c9c7573e596506`  
		Last Modified: Wed, 20 Nov 2024 00:25:00 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777ba3e191739e8b0a9bfb9aea7d18d578b9f3babc7fef147b0fbd28cdf89c55`  
		Last Modified: Wed, 20 Nov 2024 00:25:00 GMT  
		Size: 1.2 MB (1223735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b81d02fd773a9efce7e9f927510a54dd62d06333c919c1d34f605831895fd37`  
		Last Modified: Wed, 20 Nov 2024 00:25:00 GMT  
		Size: 18.3 MB (18289962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36fb0fe55fa0844db679db1e623ce0f636160818b153bfcbc1ff0a33c0654347`  
		Last Modified: Wed, 20 Nov 2024 00:25:00 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30456092fceaf011a18abfd64e9effcb5582f29154a0e11df88b27230b428e9`  
		Last Modified: Wed, 20 Nov 2024 00:25:00 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:9e5eabc4b08db9294fb88b27fa2d0cfa8f8f7152adf488e80043f02ff4403f23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **693.4 KB (693431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d38465e4fec86919ff2fb5c96060831ce9cce737b9175603cc109ab3085e61f9`

```dockerfile
```

-	Layers:
	-	`sha256:8920a1255dd0e846042c4dc32732b011a942fd0811eeeef9b8aa48215a7926ee`  
		Last Modified: Wed, 20 Nov 2024 00:24:59 GMT  
		Size: 678.4 KB (678421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90ebba546e122029bf650e9faf1659849b554ded3881979ac774d19a5f8a0225`  
		Last Modified: Wed, 20 Nov 2024 00:25:00 GMT  
		Size: 15.0 KB (15010 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2`

```console
$ docker pull influxdb@sha256:b4cd4b71bc8528c5cb6b9dede79091a234f9f565a3177b8fc4c2cc835bf5c142
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2` - linux; amd64

```console
$ docker pull influxdb@sha256:450032dcb9a8be857925f6b31c9a7b8f7bcb96c0bb6f115f8eb82cf51b7c729c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168895689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a60d0aedd5f23a0fb95890915094c12b36751c32e86a274f0ef554a76679a034`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 26 Oct 2024 00:18:17 GMT
ADD rootfs.tar.xz / # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
CMD ["bash"]
# Sat, 26 Oct 2024 00:18:17 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENV GOSU_VER=1.16
# Sat, 26 Oct 2024 00:18:17 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUXDB_VERSION=2.7.10
# Sat, 26 Oct 2024 00:18:17 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Sat, 26 Oct 2024 00:18:17 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Sat, 26 Oct 2024 00:18:17 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 26 Oct 2024 00:18:17 GMT
CMD ["influxd"]
# Sat, 26 Oct 2024 00:18:17 GMT
EXPOSE map[8086/tcp:{}]
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUXD_INIT_PORT=9999
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Sat, 26 Oct 2024 00:18:17 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e959f4013d8c177358438f498ffc044996c4cac251ba23fd5b108ef6f25e97`  
		Last Modified: Tue, 12 Nov 2024 02:14:29 GMT  
		Size: 9.8 MB (9790012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e86ca6b555a1c00c023a841efc25fe24f8dfadc0908872a792117b88345e65`  
		Last Modified: Tue, 12 Nov 2024 02:14:28 GMT  
		Size: 5.8 MB (5820924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c8080722f2ed544b9a74b2b7be7921245568d909c880898a25778444582a95`  
		Last Modified: Tue, 12 Nov 2024 02:14:28 GMT  
		Size: 3.2 KB (3228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126cf3d2a60ca27b8153a8ae8835b0e9e7168a0d193ef389e986ac358f628422`  
		Last Modified: Tue, 12 Nov 2024 02:14:29 GMT  
		Size: 1.0 MB (1006367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894c8b454d70e5f74d972cd1c5c22de1fa88f99146956e5e3c1e8c92c99f087f`  
		Last Modified: Tue, 12 Nov 2024 02:14:31 GMT  
		Size: 99.6 MB (99594018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad939cc86bc2f86fe6be975b47c46c6021a58c8b6dbc48a9b95a0e40a19f0a39`  
		Last Modified: Tue, 12 Nov 2024 02:14:30 GMT  
		Size: 23.5 MB (23546416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d730e00abb4f1168bea2cfae58aa8141637921a085d9ec2d0f2dcff551a0b131`  
		Last Modified: Tue, 12 Nov 2024 02:14:30 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac68206e130783961070fd07cc680c84e8b84b8196b4d9414735b662648008fe`  
		Last Modified: Tue, 12 Nov 2024 02:14:30 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:484fb89dfe471004e4d320b04c44ecee2a1eed2e73fb3f0651f2bb855c3c9cd9`  
		Last Modified: Tue, 12 Nov 2024 02:14:31 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:ac49cc2ec9ed3f92e78d5b3a75ca30198054624139702fd862f7f79dc13f70f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2883412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd94dd604ec6c3070720c56667d9271be44a31037d9f0f5be983fc947d0524e`

```dockerfile
```

-	Layers:
	-	`sha256:0014ad8cd7bb8f47956c367706123ed19a9bd00129122e6d3c2e9591eb10601e`  
		Last Modified: Tue, 12 Nov 2024 02:14:28 GMT  
		Size: 2.8 MB (2849697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ad8c14a09584477c71577ecbe969ddbdda39e54d7273ac097246cf11ec0ffbd`  
		Last Modified: Tue, 12 Nov 2024 02:14:28 GMT  
		Size: 33.7 KB (33715 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:09e9642e6de3a65af977c234ab0247a9e055695c4a94f9702d37a32fdac46482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.8 MB (162780456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48f139d859e68a182d3606a3443802e0c1558ffba1f52d4b3c4b83620545ca1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 26 Oct 2024 00:18:17 GMT
ADD rootfs.tar.xz / # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
CMD ["bash"]
# Sat, 26 Oct 2024 00:18:17 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENV GOSU_VER=1.16
# Sat, 26 Oct 2024 00:18:17 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUXDB_VERSION=2.7.10
# Sat, 26 Oct 2024 00:18:17 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Sat, 26 Oct 2024 00:18:17 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Sat, 26 Oct 2024 00:18:17 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 26 Oct 2024 00:18:17 GMT
CMD ["influxd"]
# Sat, 26 Oct 2024 00:18:17 GMT
EXPOSE map[8086/tcp:{}]
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUXD_INIT_PORT=9999
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Sat, 26 Oct 2024 00:18:17 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3a642d5023c08a13d7e46adf1e20b91c0dd511b302c6b6aad4048cd848cb4b`  
		Last Modified: Tue, 12 Nov 2024 13:16:42 GMT  
		Size: 9.6 MB (9587384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731f20af9837960d52c351be1e5d55d40fdcc0f2a4b97a802fc53a2124e85464`  
		Last Modified: Tue, 12 Nov 2024 13:16:41 GMT  
		Size: 5.5 MB (5463803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f25e64a0d5b010a44ecf7d4c17c28339bf5f160c674df809e959319fafc3051`  
		Last Modified: Tue, 12 Nov 2024 13:16:41 GMT  
		Size: 3.2 KB (3229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6396271bc680bb75186064fddcc653b8467d5b392e3bff302cfb7967f8d1ac`  
		Last Modified: Tue, 12 Nov 2024 13:16:41 GMT  
		Size: 936.1 KB (936107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9014ea0ef031959de88323f77a2fe0369539e1bc3b6199b3a2fe7181582f7e39`  
		Last Modified: Tue, 12 Nov 2024 13:16:45 GMT  
		Size: 95.4 MB (95427910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d5a42298ac70e33cecff554e70fbfbc62971285c007845ec763c0d6fc6be78`  
		Last Modified: Tue, 12 Nov 2024 13:16:43 GMT  
		Size: 22.2 MB (22197937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1537f59d496eeb7153378960a1b6508e6d8db7e1228d8ff57e287a2df3233a07`  
		Last Modified: Tue, 12 Nov 2024 13:16:42 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790fce02ac9721a8ed762cb9a64976d90e0ae6892c169fd69242f1df4a2d3565`  
		Last Modified: Tue, 12 Nov 2024 13:16:43 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315f2c6d4520efa5c5e7cd192fe752432cd37ce05e360bb6c06025b7491b785f`  
		Last Modified: Tue, 12 Nov 2024 13:16:43 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:536654c011c2d4c0ff295051d57ef6055c865962ee390ad4d2e4c1075eb69926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2882837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0382841cdea4a7397839653508492d4ca6639436f7aaad3e62bfa03d9e48cb`

```dockerfile
```

-	Layers:
	-	`sha256:32c1f9baa6bb19e8563a747a2a422fabe13d66589035dc45e801a287b6fd0b66`  
		Last Modified: Tue, 12 Nov 2024 13:16:41 GMT  
		Size: 2.8 MB (2848934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4591157c8a4e5cb8e9ac28ed1c1bac6459f461c4673123cc5391c59512dcc9f`  
		Last Modified: Tue, 12 Nov 2024 13:16:41 GMT  
		Size: 33.9 KB (33903 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2-alpine`

```console
$ docker pull influxdb@sha256:c5fcf0f3e6fc4d30646666ce9466e5022f2d35ab30ee56fc254da7b00897ac90
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:016696f871af9501d2bc8de125412ea11d6b06255c94b7072116ff9bdbf75565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.4 MB (92447366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94c1600abc60dd628161036525341fdf5f9bffdd371e2f579beaaca306c6bab9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Sat, 26 Oct 2024 00:18:17 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUXDB_VERSION=2.7.10
# Sat, 26 Oct 2024 00:18:17 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Sat, 26 Oct 2024 00:18:17 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Sat, 26 Oct 2024 00:18:17 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 26 Oct 2024 00:18:17 GMT
CMD ["influxd"]
# Sat, 26 Oct 2024 00:18:17 GMT
EXPOSE map[8086/tcp:{}]
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUXD_INIT_PORT=9999
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Sat, 26 Oct 2024 00:18:17 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28ca4e78c51cf4f32aee0112b39eee90ec5adad51bf06d230cf84703a7c6d95`  
		Last Modified: Tue, 12 Nov 2024 02:14:03 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58b67e284d401e7fd4d54596f90f54c3cdd037874acc84cb4f8077d1702a9e9`  
		Last Modified: Tue, 12 Nov 2024 02:14:03 GMT  
		Size: 9.7 MB (9657640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c539d32573f2c3a568d8156ef3011bf685fb1ae318fc0e22b00b8c5af5da06`  
		Last Modified: Tue, 12 Nov 2024 02:14:03 GMT  
		Size: 5.8 MB (5820948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69a09b073184b319d09b27a4a9ffd399f213b4f726be4aa212abf8875f42080`  
		Last Modified: Tue, 12 Nov 2024 02:14:03 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30b2a00406ce3e77a88383b59693aa6cf6964e5e5a40889f5b3c7bf5563495a`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 49.8 MB (49790503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b47d751c1de460253085b2b61ce94f5c4b6c2fba2aec50ddc52c75ec5697c38`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 23.5 MB (23546399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c61e966ba5d507be2689f099daab5a6d576aa8ce6b913d29d5241116f14e68f6`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f8df45b28aaa2017245994d083bc1c4f4c458a94ad4d15fd70700bf13ec6ca8`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91ae1b04c1b23614536b52471d7a6c4f80897a884d06a9979559eeca7ff1eeb`  
		Last Modified: Tue, 12 Nov 2024 02:14:05 GMT  
		Size: 6.3 KB (6284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:a5f3b51d4f67e7f4944706ce0671151da9ed28c56d76261b6e75550f7decea16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **945.6 KB (945575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1d4fd40043261f88c2e90979cbb077235817d36456620aaf121c7562f4f6904`

```dockerfile
```

-	Layers:
	-	`sha256:fcf01541daa9f52095830599da571f955b900cce93bf6a02a6eec5c47799166a`  
		Last Modified: Tue, 12 Nov 2024 02:14:03 GMT  
		Size: 914.6 KB (914627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b910bcc341ba0f74ad9281164a23e1c102c09a5aa16cfd7a2d21069a13c536c`  
		Last Modified: Tue, 12 Nov 2024 02:14:03 GMT  
		Size: 30.9 KB (30948 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:683574882337d89ba55b47ec2239c9304ffbdb2a9b5d500a4e10149d0ca3607f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.2 MB (89246784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6939dca89d326a57786860064203b8e7d1b373094a310fa5d27e6fe1cbbf35f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Sat, 26 Oct 2024 00:18:17 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUXDB_VERSION=2.7.10
# Sat, 26 Oct 2024 00:18:17 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Sat, 26 Oct 2024 00:18:17 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Sat, 26 Oct 2024 00:18:17 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 26 Oct 2024 00:18:17 GMT
CMD ["influxd"]
# Sat, 26 Oct 2024 00:18:17 GMT
EXPOSE map[8086/tcp:{}]
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUXD_INIT_PORT=9999
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Sat, 26 Oct 2024 00:18:17 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9de63ce930d0f77f6402e61ee732ad4f784c59fd26df033bb1b7d6a0b87a2f4`  
		Last Modified: Tue, 12 Nov 2024 13:17:18 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca3884ecb2e01cc65615fbe7048afa29c9c999de55aa88e1d6b387145dcd94f`  
		Last Modified: Tue, 12 Nov 2024 13:17:19 GMT  
		Size: 9.8 MB (9779862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9bfe4e135f18780a8d70c200e6244ef50d4311f2d786b210cce82c9afcf4b51`  
		Last Modified: Tue, 12 Nov 2024 13:17:19 GMT  
		Size: 5.5 MB (5463799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49cd5ee8b73fbef9d7556ef226315ce8a0aa6839f5120dad8b3c7c54ac9089b3`  
		Last Modified: Tue, 12 Nov 2024 13:17:18 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581641f4c063dbaf1e6608dfc65fcbd8cf4d88834c016ff89bd1a60a5cff3b73`  
		Last Modified: Tue, 12 Nov 2024 13:17:21 GMT  
		Size: 47.7 MB (47709508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20dfa20b1284e4022b9d82bb6648314f82cedeac1aefc7fb5eb6a449c3425040`  
		Last Modified: Tue, 12 Nov 2024 13:17:21 GMT  
		Size: 22.2 MB (22197919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eefb802b10b14779184170266c3cdc56aa734880d5612242e2708507587d79f`  
		Last Modified: Tue, 12 Nov 2024 13:17:20 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf6276080857087ce5c820eff3e3050daf134e85ce8a4b99cda5b1d0c863016`  
		Last Modified: Tue, 12 Nov 2024 13:17:20 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328ab936fb2b98bc25b20b1ce89e9db5116ac84e88abc2ba1f7adeaed3eb8968`  
		Last Modified: Tue, 12 Nov 2024 13:17:21 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:a79f6e8d0e4c420a240b72bd4d1f88411ecec4dbcfd37f6a237d6d4b3786ccdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **945.0 KB (945031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d64762a01a3fc2611c65a4ff9832a72540bd540b6908c89c2bf9bf0c6c270702`

```dockerfile
```

-	Layers:
	-	`sha256:f5a82395e10d447f3421cac787c8be250079fed545ae107342063bb886cb56af`  
		Last Modified: Tue, 12 Nov 2024 13:17:19 GMT  
		Size: 913.9 KB (913888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cd070e7c1391a788b25bf86f5dd27f01597ce5b01a48117f40afcf4fbebed3e`  
		Last Modified: Tue, 12 Nov 2024 13:17:18 GMT  
		Size: 31.1 KB (31143 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7`

```console
$ docker pull influxdb@sha256:b4cd4b71bc8528c5cb6b9dede79091a234f9f565a3177b8fc4c2cc835bf5c142
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7` - linux; amd64

```console
$ docker pull influxdb@sha256:450032dcb9a8be857925f6b31c9a7b8f7bcb96c0bb6f115f8eb82cf51b7c729c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168895689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a60d0aedd5f23a0fb95890915094c12b36751c32e86a274f0ef554a76679a034`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 26 Oct 2024 00:18:17 GMT
ADD rootfs.tar.xz / # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
CMD ["bash"]
# Sat, 26 Oct 2024 00:18:17 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENV GOSU_VER=1.16
# Sat, 26 Oct 2024 00:18:17 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUXDB_VERSION=2.7.10
# Sat, 26 Oct 2024 00:18:17 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Sat, 26 Oct 2024 00:18:17 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Sat, 26 Oct 2024 00:18:17 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 26 Oct 2024 00:18:17 GMT
CMD ["influxd"]
# Sat, 26 Oct 2024 00:18:17 GMT
EXPOSE map[8086/tcp:{}]
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUXD_INIT_PORT=9999
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Sat, 26 Oct 2024 00:18:17 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e959f4013d8c177358438f498ffc044996c4cac251ba23fd5b108ef6f25e97`  
		Last Modified: Tue, 12 Nov 2024 02:14:29 GMT  
		Size: 9.8 MB (9790012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e86ca6b555a1c00c023a841efc25fe24f8dfadc0908872a792117b88345e65`  
		Last Modified: Tue, 12 Nov 2024 02:14:28 GMT  
		Size: 5.8 MB (5820924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c8080722f2ed544b9a74b2b7be7921245568d909c880898a25778444582a95`  
		Last Modified: Tue, 12 Nov 2024 02:14:28 GMT  
		Size: 3.2 KB (3228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126cf3d2a60ca27b8153a8ae8835b0e9e7168a0d193ef389e986ac358f628422`  
		Last Modified: Tue, 12 Nov 2024 02:14:29 GMT  
		Size: 1.0 MB (1006367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894c8b454d70e5f74d972cd1c5c22de1fa88f99146956e5e3c1e8c92c99f087f`  
		Last Modified: Tue, 12 Nov 2024 02:14:31 GMT  
		Size: 99.6 MB (99594018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad939cc86bc2f86fe6be975b47c46c6021a58c8b6dbc48a9b95a0e40a19f0a39`  
		Last Modified: Tue, 12 Nov 2024 02:14:30 GMT  
		Size: 23.5 MB (23546416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d730e00abb4f1168bea2cfae58aa8141637921a085d9ec2d0f2dcff551a0b131`  
		Last Modified: Tue, 12 Nov 2024 02:14:30 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac68206e130783961070fd07cc680c84e8b84b8196b4d9414735b662648008fe`  
		Last Modified: Tue, 12 Nov 2024 02:14:30 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:484fb89dfe471004e4d320b04c44ecee2a1eed2e73fb3f0651f2bb855c3c9cd9`  
		Last Modified: Tue, 12 Nov 2024 02:14:31 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:ac49cc2ec9ed3f92e78d5b3a75ca30198054624139702fd862f7f79dc13f70f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2883412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd94dd604ec6c3070720c56667d9271be44a31037d9f0f5be983fc947d0524e`

```dockerfile
```

-	Layers:
	-	`sha256:0014ad8cd7bb8f47956c367706123ed19a9bd00129122e6d3c2e9591eb10601e`  
		Last Modified: Tue, 12 Nov 2024 02:14:28 GMT  
		Size: 2.8 MB (2849697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ad8c14a09584477c71577ecbe969ddbdda39e54d7273ac097246cf11ec0ffbd`  
		Last Modified: Tue, 12 Nov 2024 02:14:28 GMT  
		Size: 33.7 KB (33715 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:09e9642e6de3a65af977c234ab0247a9e055695c4a94f9702d37a32fdac46482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.8 MB (162780456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48f139d859e68a182d3606a3443802e0c1558ffba1f52d4b3c4b83620545ca1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 26 Oct 2024 00:18:17 GMT
ADD rootfs.tar.xz / # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
CMD ["bash"]
# Sat, 26 Oct 2024 00:18:17 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENV GOSU_VER=1.16
# Sat, 26 Oct 2024 00:18:17 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUXDB_VERSION=2.7.10
# Sat, 26 Oct 2024 00:18:17 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Sat, 26 Oct 2024 00:18:17 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Sat, 26 Oct 2024 00:18:17 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 26 Oct 2024 00:18:17 GMT
CMD ["influxd"]
# Sat, 26 Oct 2024 00:18:17 GMT
EXPOSE map[8086/tcp:{}]
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUXD_INIT_PORT=9999
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Sat, 26 Oct 2024 00:18:17 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3a642d5023c08a13d7e46adf1e20b91c0dd511b302c6b6aad4048cd848cb4b`  
		Last Modified: Tue, 12 Nov 2024 13:16:42 GMT  
		Size: 9.6 MB (9587384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731f20af9837960d52c351be1e5d55d40fdcc0f2a4b97a802fc53a2124e85464`  
		Last Modified: Tue, 12 Nov 2024 13:16:41 GMT  
		Size: 5.5 MB (5463803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f25e64a0d5b010a44ecf7d4c17c28339bf5f160c674df809e959319fafc3051`  
		Last Modified: Tue, 12 Nov 2024 13:16:41 GMT  
		Size: 3.2 KB (3229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6396271bc680bb75186064fddcc653b8467d5b392e3bff302cfb7967f8d1ac`  
		Last Modified: Tue, 12 Nov 2024 13:16:41 GMT  
		Size: 936.1 KB (936107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9014ea0ef031959de88323f77a2fe0369539e1bc3b6199b3a2fe7181582f7e39`  
		Last Modified: Tue, 12 Nov 2024 13:16:45 GMT  
		Size: 95.4 MB (95427910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d5a42298ac70e33cecff554e70fbfbc62971285c007845ec763c0d6fc6be78`  
		Last Modified: Tue, 12 Nov 2024 13:16:43 GMT  
		Size: 22.2 MB (22197937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1537f59d496eeb7153378960a1b6508e6d8db7e1228d8ff57e287a2df3233a07`  
		Last Modified: Tue, 12 Nov 2024 13:16:42 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790fce02ac9721a8ed762cb9a64976d90e0ae6892c169fd69242f1df4a2d3565`  
		Last Modified: Tue, 12 Nov 2024 13:16:43 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315f2c6d4520efa5c5e7cd192fe752432cd37ce05e360bb6c06025b7491b785f`  
		Last Modified: Tue, 12 Nov 2024 13:16:43 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:536654c011c2d4c0ff295051d57ef6055c865962ee390ad4d2e4c1075eb69926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2882837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0382841cdea4a7397839653508492d4ca6639436f7aaad3e62bfa03d9e48cb`

```dockerfile
```

-	Layers:
	-	`sha256:32c1f9baa6bb19e8563a747a2a422fabe13d66589035dc45e801a287b6fd0b66`  
		Last Modified: Tue, 12 Nov 2024 13:16:41 GMT  
		Size: 2.8 MB (2848934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4591157c8a4e5cb8e9ac28ed1c1bac6459f461c4673123cc5391c59512dcc9f`  
		Last Modified: Tue, 12 Nov 2024 13:16:41 GMT  
		Size: 33.9 KB (33903 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7-alpine`

```console
$ docker pull influxdb@sha256:c5fcf0f3e6fc4d30646666ce9466e5022f2d35ab30ee56fc254da7b00897ac90
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:016696f871af9501d2bc8de125412ea11d6b06255c94b7072116ff9bdbf75565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.4 MB (92447366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94c1600abc60dd628161036525341fdf5f9bffdd371e2f579beaaca306c6bab9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Sat, 26 Oct 2024 00:18:17 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUXDB_VERSION=2.7.10
# Sat, 26 Oct 2024 00:18:17 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Sat, 26 Oct 2024 00:18:17 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Sat, 26 Oct 2024 00:18:17 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 26 Oct 2024 00:18:17 GMT
CMD ["influxd"]
# Sat, 26 Oct 2024 00:18:17 GMT
EXPOSE map[8086/tcp:{}]
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUXD_INIT_PORT=9999
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Sat, 26 Oct 2024 00:18:17 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28ca4e78c51cf4f32aee0112b39eee90ec5adad51bf06d230cf84703a7c6d95`  
		Last Modified: Tue, 12 Nov 2024 02:14:03 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58b67e284d401e7fd4d54596f90f54c3cdd037874acc84cb4f8077d1702a9e9`  
		Last Modified: Tue, 12 Nov 2024 02:14:03 GMT  
		Size: 9.7 MB (9657640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c539d32573f2c3a568d8156ef3011bf685fb1ae318fc0e22b00b8c5af5da06`  
		Last Modified: Tue, 12 Nov 2024 02:14:03 GMT  
		Size: 5.8 MB (5820948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69a09b073184b319d09b27a4a9ffd399f213b4f726be4aa212abf8875f42080`  
		Last Modified: Tue, 12 Nov 2024 02:14:03 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30b2a00406ce3e77a88383b59693aa6cf6964e5e5a40889f5b3c7bf5563495a`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 49.8 MB (49790503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b47d751c1de460253085b2b61ce94f5c4b6c2fba2aec50ddc52c75ec5697c38`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 23.5 MB (23546399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c61e966ba5d507be2689f099daab5a6d576aa8ce6b913d29d5241116f14e68f6`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f8df45b28aaa2017245994d083bc1c4f4c458a94ad4d15fd70700bf13ec6ca8`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91ae1b04c1b23614536b52471d7a6c4f80897a884d06a9979559eeca7ff1eeb`  
		Last Modified: Tue, 12 Nov 2024 02:14:05 GMT  
		Size: 6.3 KB (6284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:a5f3b51d4f67e7f4944706ce0671151da9ed28c56d76261b6e75550f7decea16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **945.6 KB (945575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1d4fd40043261f88c2e90979cbb077235817d36456620aaf121c7562f4f6904`

```dockerfile
```

-	Layers:
	-	`sha256:fcf01541daa9f52095830599da571f955b900cce93bf6a02a6eec5c47799166a`  
		Last Modified: Tue, 12 Nov 2024 02:14:03 GMT  
		Size: 914.6 KB (914627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b910bcc341ba0f74ad9281164a23e1c102c09a5aa16cfd7a2d21069a13c536c`  
		Last Modified: Tue, 12 Nov 2024 02:14:03 GMT  
		Size: 30.9 KB (30948 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:683574882337d89ba55b47ec2239c9304ffbdb2a9b5d500a4e10149d0ca3607f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.2 MB (89246784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6939dca89d326a57786860064203b8e7d1b373094a310fa5d27e6fe1cbbf35f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Sat, 26 Oct 2024 00:18:17 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUXDB_VERSION=2.7.10
# Sat, 26 Oct 2024 00:18:17 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Sat, 26 Oct 2024 00:18:17 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Sat, 26 Oct 2024 00:18:17 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 26 Oct 2024 00:18:17 GMT
CMD ["influxd"]
# Sat, 26 Oct 2024 00:18:17 GMT
EXPOSE map[8086/tcp:{}]
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUXD_INIT_PORT=9999
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Sat, 26 Oct 2024 00:18:17 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9de63ce930d0f77f6402e61ee732ad4f784c59fd26df033bb1b7d6a0b87a2f4`  
		Last Modified: Tue, 12 Nov 2024 13:17:18 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca3884ecb2e01cc65615fbe7048afa29c9c999de55aa88e1d6b387145dcd94f`  
		Last Modified: Tue, 12 Nov 2024 13:17:19 GMT  
		Size: 9.8 MB (9779862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9bfe4e135f18780a8d70c200e6244ef50d4311f2d786b210cce82c9afcf4b51`  
		Last Modified: Tue, 12 Nov 2024 13:17:19 GMT  
		Size: 5.5 MB (5463799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49cd5ee8b73fbef9d7556ef226315ce8a0aa6839f5120dad8b3c7c54ac9089b3`  
		Last Modified: Tue, 12 Nov 2024 13:17:18 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581641f4c063dbaf1e6608dfc65fcbd8cf4d88834c016ff89bd1a60a5cff3b73`  
		Last Modified: Tue, 12 Nov 2024 13:17:21 GMT  
		Size: 47.7 MB (47709508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20dfa20b1284e4022b9d82bb6648314f82cedeac1aefc7fb5eb6a449c3425040`  
		Last Modified: Tue, 12 Nov 2024 13:17:21 GMT  
		Size: 22.2 MB (22197919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eefb802b10b14779184170266c3cdc56aa734880d5612242e2708507587d79f`  
		Last Modified: Tue, 12 Nov 2024 13:17:20 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf6276080857087ce5c820eff3e3050daf134e85ce8a4b99cda5b1d0c863016`  
		Last Modified: Tue, 12 Nov 2024 13:17:20 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328ab936fb2b98bc25b20b1ce89e9db5116ac84e88abc2ba1f7adeaed3eb8968`  
		Last Modified: Tue, 12 Nov 2024 13:17:21 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:a79f6e8d0e4c420a240b72bd4d1f88411ecec4dbcfd37f6a237d6d4b3786ccdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **945.0 KB (945031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d64762a01a3fc2611c65a4ff9832a72540bd540b6908c89c2bf9bf0c6c270702`

```dockerfile
```

-	Layers:
	-	`sha256:f5a82395e10d447f3421cac787c8be250079fed545ae107342063bb886cb56af`  
		Last Modified: Tue, 12 Nov 2024 13:17:19 GMT  
		Size: 913.9 KB (913888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cd070e7c1391a788b25bf86f5dd27f01597ce5b01a48117f40afcf4fbebed3e`  
		Last Modified: Tue, 12 Nov 2024 13:17:18 GMT  
		Size: 31.1 KB (31143 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7.11`

**does not exist** (yet?)

## `influxdb:2.7.11-alpine`

**does not exist** (yet?)

## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:c5fcf0f3e6fc4d30646666ce9466e5022f2d35ab30ee56fc254da7b00897ac90
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:016696f871af9501d2bc8de125412ea11d6b06255c94b7072116ff9bdbf75565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.4 MB (92447366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94c1600abc60dd628161036525341fdf5f9bffdd371e2f579beaaca306c6bab9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Sat, 26 Oct 2024 00:18:17 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUXDB_VERSION=2.7.10
# Sat, 26 Oct 2024 00:18:17 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Sat, 26 Oct 2024 00:18:17 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Sat, 26 Oct 2024 00:18:17 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 26 Oct 2024 00:18:17 GMT
CMD ["influxd"]
# Sat, 26 Oct 2024 00:18:17 GMT
EXPOSE map[8086/tcp:{}]
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUXD_INIT_PORT=9999
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Sat, 26 Oct 2024 00:18:17 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28ca4e78c51cf4f32aee0112b39eee90ec5adad51bf06d230cf84703a7c6d95`  
		Last Modified: Tue, 12 Nov 2024 02:14:03 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58b67e284d401e7fd4d54596f90f54c3cdd037874acc84cb4f8077d1702a9e9`  
		Last Modified: Tue, 12 Nov 2024 02:14:03 GMT  
		Size: 9.7 MB (9657640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c539d32573f2c3a568d8156ef3011bf685fb1ae318fc0e22b00b8c5af5da06`  
		Last Modified: Tue, 12 Nov 2024 02:14:03 GMT  
		Size: 5.8 MB (5820948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69a09b073184b319d09b27a4a9ffd399f213b4f726be4aa212abf8875f42080`  
		Last Modified: Tue, 12 Nov 2024 02:14:03 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30b2a00406ce3e77a88383b59693aa6cf6964e5e5a40889f5b3c7bf5563495a`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 49.8 MB (49790503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b47d751c1de460253085b2b61ce94f5c4b6c2fba2aec50ddc52c75ec5697c38`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 23.5 MB (23546399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c61e966ba5d507be2689f099daab5a6d576aa8ce6b913d29d5241116f14e68f6`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f8df45b28aaa2017245994d083bc1c4f4c458a94ad4d15fd70700bf13ec6ca8`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91ae1b04c1b23614536b52471d7a6c4f80897a884d06a9979559eeca7ff1eeb`  
		Last Modified: Tue, 12 Nov 2024 02:14:05 GMT  
		Size: 6.3 KB (6284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:a5f3b51d4f67e7f4944706ce0671151da9ed28c56d76261b6e75550f7decea16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **945.6 KB (945575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1d4fd40043261f88c2e90979cbb077235817d36456620aaf121c7562f4f6904`

```dockerfile
```

-	Layers:
	-	`sha256:fcf01541daa9f52095830599da571f955b900cce93bf6a02a6eec5c47799166a`  
		Last Modified: Tue, 12 Nov 2024 02:14:03 GMT  
		Size: 914.6 KB (914627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b910bcc341ba0f74ad9281164a23e1c102c09a5aa16cfd7a2d21069a13c536c`  
		Last Modified: Tue, 12 Nov 2024 02:14:03 GMT  
		Size: 30.9 KB (30948 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:683574882337d89ba55b47ec2239c9304ffbdb2a9b5d500a4e10149d0ca3607f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.2 MB (89246784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6939dca89d326a57786860064203b8e7d1b373094a310fa5d27e6fe1cbbf35f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Sat, 26 Oct 2024 00:18:17 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUXDB_VERSION=2.7.10
# Sat, 26 Oct 2024 00:18:17 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Sat, 26 Oct 2024 00:18:17 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Sat, 26 Oct 2024 00:18:17 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 26 Oct 2024 00:18:17 GMT
CMD ["influxd"]
# Sat, 26 Oct 2024 00:18:17 GMT
EXPOSE map[8086/tcp:{}]
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUXD_INIT_PORT=9999
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Sat, 26 Oct 2024 00:18:17 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9de63ce930d0f77f6402e61ee732ad4f784c59fd26df033bb1b7d6a0b87a2f4`  
		Last Modified: Tue, 12 Nov 2024 13:17:18 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca3884ecb2e01cc65615fbe7048afa29c9c999de55aa88e1d6b387145dcd94f`  
		Last Modified: Tue, 12 Nov 2024 13:17:19 GMT  
		Size: 9.8 MB (9779862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9bfe4e135f18780a8d70c200e6244ef50d4311f2d786b210cce82c9afcf4b51`  
		Last Modified: Tue, 12 Nov 2024 13:17:19 GMT  
		Size: 5.5 MB (5463799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49cd5ee8b73fbef9d7556ef226315ce8a0aa6839f5120dad8b3c7c54ac9089b3`  
		Last Modified: Tue, 12 Nov 2024 13:17:18 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581641f4c063dbaf1e6608dfc65fcbd8cf4d88834c016ff89bd1a60a5cff3b73`  
		Last Modified: Tue, 12 Nov 2024 13:17:21 GMT  
		Size: 47.7 MB (47709508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20dfa20b1284e4022b9d82bb6648314f82cedeac1aefc7fb5eb6a449c3425040`  
		Last Modified: Tue, 12 Nov 2024 13:17:21 GMT  
		Size: 22.2 MB (22197919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eefb802b10b14779184170266c3cdc56aa734880d5612242e2708507587d79f`  
		Last Modified: Tue, 12 Nov 2024 13:17:20 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf6276080857087ce5c820eff3e3050daf134e85ce8a4b99cda5b1d0c863016`  
		Last Modified: Tue, 12 Nov 2024 13:17:20 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328ab936fb2b98bc25b20b1ce89e9db5116ac84e88abc2ba1f7adeaed3eb8968`  
		Last Modified: Tue, 12 Nov 2024 13:17:21 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:a79f6e8d0e4c420a240b72bd4d1f88411ecec4dbcfd37f6a237d6d4b3786ccdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **945.0 KB (945031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d64762a01a3fc2611c65a4ff9832a72540bd540b6908c89c2bf9bf0c6c270702`

```dockerfile
```

-	Layers:
	-	`sha256:f5a82395e10d447f3421cac787c8be250079fed545ae107342063bb886cb56af`  
		Last Modified: Tue, 12 Nov 2024 13:17:19 GMT  
		Size: 913.9 KB (913888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cd070e7c1391a788b25bf86f5dd27f01597ce5b01a48117f40afcf4fbebed3e`  
		Last Modified: Tue, 12 Nov 2024 13:17:18 GMT  
		Size: 31.1 KB (31143 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:latest`

```console
$ docker pull influxdb@sha256:b4cd4b71bc8528c5cb6b9dede79091a234f9f565a3177b8fc4c2cc835bf5c142
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:450032dcb9a8be857925f6b31c9a7b8f7bcb96c0bb6f115f8eb82cf51b7c729c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168895689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a60d0aedd5f23a0fb95890915094c12b36751c32e86a274f0ef554a76679a034`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 26 Oct 2024 00:18:17 GMT
ADD rootfs.tar.xz / # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
CMD ["bash"]
# Sat, 26 Oct 2024 00:18:17 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENV GOSU_VER=1.16
# Sat, 26 Oct 2024 00:18:17 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUXDB_VERSION=2.7.10
# Sat, 26 Oct 2024 00:18:17 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Sat, 26 Oct 2024 00:18:17 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Sat, 26 Oct 2024 00:18:17 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 26 Oct 2024 00:18:17 GMT
CMD ["influxd"]
# Sat, 26 Oct 2024 00:18:17 GMT
EXPOSE map[8086/tcp:{}]
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUXD_INIT_PORT=9999
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Sat, 26 Oct 2024 00:18:17 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e959f4013d8c177358438f498ffc044996c4cac251ba23fd5b108ef6f25e97`  
		Last Modified: Tue, 12 Nov 2024 02:14:29 GMT  
		Size: 9.8 MB (9790012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e86ca6b555a1c00c023a841efc25fe24f8dfadc0908872a792117b88345e65`  
		Last Modified: Tue, 12 Nov 2024 02:14:28 GMT  
		Size: 5.8 MB (5820924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c8080722f2ed544b9a74b2b7be7921245568d909c880898a25778444582a95`  
		Last Modified: Tue, 12 Nov 2024 02:14:28 GMT  
		Size: 3.2 KB (3228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126cf3d2a60ca27b8153a8ae8835b0e9e7168a0d193ef389e986ac358f628422`  
		Last Modified: Tue, 12 Nov 2024 02:14:29 GMT  
		Size: 1.0 MB (1006367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894c8b454d70e5f74d972cd1c5c22de1fa88f99146956e5e3c1e8c92c99f087f`  
		Last Modified: Tue, 12 Nov 2024 02:14:31 GMT  
		Size: 99.6 MB (99594018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad939cc86bc2f86fe6be975b47c46c6021a58c8b6dbc48a9b95a0e40a19f0a39`  
		Last Modified: Tue, 12 Nov 2024 02:14:30 GMT  
		Size: 23.5 MB (23546416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d730e00abb4f1168bea2cfae58aa8141637921a085d9ec2d0f2dcff551a0b131`  
		Last Modified: Tue, 12 Nov 2024 02:14:30 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac68206e130783961070fd07cc680c84e8b84b8196b4d9414735b662648008fe`  
		Last Modified: Tue, 12 Nov 2024 02:14:30 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:484fb89dfe471004e4d320b04c44ecee2a1eed2e73fb3f0651f2bb855c3c9cd9`  
		Last Modified: Tue, 12 Nov 2024 02:14:31 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:ac49cc2ec9ed3f92e78d5b3a75ca30198054624139702fd862f7f79dc13f70f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2883412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd94dd604ec6c3070720c56667d9271be44a31037d9f0f5be983fc947d0524e`

```dockerfile
```

-	Layers:
	-	`sha256:0014ad8cd7bb8f47956c367706123ed19a9bd00129122e6d3c2e9591eb10601e`  
		Last Modified: Tue, 12 Nov 2024 02:14:28 GMT  
		Size: 2.8 MB (2849697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ad8c14a09584477c71577ecbe969ddbdda39e54d7273ac097246cf11ec0ffbd`  
		Last Modified: Tue, 12 Nov 2024 02:14:28 GMT  
		Size: 33.7 KB (33715 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:09e9642e6de3a65af977c234ab0247a9e055695c4a94f9702d37a32fdac46482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.8 MB (162780456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48f139d859e68a182d3606a3443802e0c1558ffba1f52d4b3c4b83620545ca1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 26 Oct 2024 00:18:17 GMT
ADD rootfs.tar.xz / # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
CMD ["bash"]
# Sat, 26 Oct 2024 00:18:17 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENV GOSU_VER=1.16
# Sat, 26 Oct 2024 00:18:17 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUXDB_VERSION=2.7.10
# Sat, 26 Oct 2024 00:18:17 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Sat, 26 Oct 2024 00:18:17 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Sat, 26 Oct 2024 00:18:17 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 26 Oct 2024 00:18:17 GMT
CMD ["influxd"]
# Sat, 26 Oct 2024 00:18:17 GMT
EXPOSE map[8086/tcp:{}]
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUXD_INIT_PORT=9999
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Sat, 26 Oct 2024 00:18:17 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3a642d5023c08a13d7e46adf1e20b91c0dd511b302c6b6aad4048cd848cb4b`  
		Last Modified: Tue, 12 Nov 2024 13:16:42 GMT  
		Size: 9.6 MB (9587384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731f20af9837960d52c351be1e5d55d40fdcc0f2a4b97a802fc53a2124e85464`  
		Last Modified: Tue, 12 Nov 2024 13:16:41 GMT  
		Size: 5.5 MB (5463803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f25e64a0d5b010a44ecf7d4c17c28339bf5f160c674df809e959319fafc3051`  
		Last Modified: Tue, 12 Nov 2024 13:16:41 GMT  
		Size: 3.2 KB (3229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6396271bc680bb75186064fddcc653b8467d5b392e3bff302cfb7967f8d1ac`  
		Last Modified: Tue, 12 Nov 2024 13:16:41 GMT  
		Size: 936.1 KB (936107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9014ea0ef031959de88323f77a2fe0369539e1bc3b6199b3a2fe7181582f7e39`  
		Last Modified: Tue, 12 Nov 2024 13:16:45 GMT  
		Size: 95.4 MB (95427910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d5a42298ac70e33cecff554e70fbfbc62971285c007845ec763c0d6fc6be78`  
		Last Modified: Tue, 12 Nov 2024 13:16:43 GMT  
		Size: 22.2 MB (22197937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1537f59d496eeb7153378960a1b6508e6d8db7e1228d8ff57e287a2df3233a07`  
		Last Modified: Tue, 12 Nov 2024 13:16:42 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790fce02ac9721a8ed762cb9a64976d90e0ae6892c169fd69242f1df4a2d3565`  
		Last Modified: Tue, 12 Nov 2024 13:16:43 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315f2c6d4520efa5c5e7cd192fe752432cd37ce05e360bb6c06025b7491b785f`  
		Last Modified: Tue, 12 Nov 2024 13:16:43 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:536654c011c2d4c0ff295051d57ef6055c865962ee390ad4d2e4c1075eb69926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2882837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0382841cdea4a7397839653508492d4ca6639436f7aaad3e62bfa03d9e48cb`

```dockerfile
```

-	Layers:
	-	`sha256:32c1f9baa6bb19e8563a747a2a422fabe13d66589035dc45e801a287b6fd0b66`  
		Last Modified: Tue, 12 Nov 2024 13:16:41 GMT  
		Size: 2.8 MB (2848934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4591157c8a4e5cb8e9ac28ed1c1bac6459f461c4673123cc5391c59512dcc9f`  
		Last Modified: Tue, 12 Nov 2024 13:16:41 GMT  
		Size: 33.9 KB (33903 bytes)  
		MIME: application/vnd.in-toto+json
