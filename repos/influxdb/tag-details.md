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
-	[`influxdb:1.11.7`](#influxdb1117)
-	[`influxdb:1.11.7-alpine`](#influxdb1117-alpine)
-	[`influxdb:1.11.7-data`](#influxdb1117-data)
-	[`influxdb:1.11.7-data-alpine`](#influxdb1117-data-alpine)
-	[`influxdb:1.11.7-meta`](#influxdb1117-meta)
-	[`influxdb:1.11.7-meta-alpine`](#influxdb1117-meta-alpine)
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
$ docker pull influxdb@sha256:200232d77ed6efc06db2e514e0da4426601577700aae3b7164412b2c06d8e93a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11` - linux; amd64

```console
$ docker pull influxdb@sha256:fce87665015043ae7cc75ccdb873f9f8dc00ef92dee50e2e7a08ddf7825cea31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.3 MB (117286270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d02473da4f26853abaf94ee1cdb4a7fd402e69d06f7f5f1fbd4f7b6d7d503934`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ARG INFLUXDB_VERSION=1.11.7
# Sat, 26 Oct 2024 00:18:17 GMT
# ARGS: INFLUXDB_VERSION=1.11.7
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
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
USER influxdb
# Sat, 26 Oct 2024 00:18:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 26 Oct 2024 00:18:17 GMT
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
	-	`sha256:d1a683cb677917f570dd15854dc6823793c99f935156cbb5f2d2b403d9be867a`  
		Last Modified: Tue, 12 Nov 2024 03:14:24 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:167aba5b317025bb8927325814fe1e358e8bf953070ed0939e4ea2a1d20dffb7`  
		Last Modified: Tue, 12 Nov 2024 03:14:24 GMT  
		Size: 43.6 MB (43649316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad040ea3f07fdc575b52dc19571d397e6f819c2efb97a47934e9d95e4069e81`  
		Last Modified: Tue, 12 Nov 2024 03:14:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc7a6d4123d188202e71f4446010b0ed37125366f9fb09afac53d94c49cddbef`  
		Last Modified: Tue, 12 Nov 2024 03:14:24 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df020ff2a521aae398dec31b1fbcac439aad9e1eb576ee9c922767401d172e6`  
		Last Modified: Tue, 12 Nov 2024 03:14:24 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11` - unknown; unknown

```console
$ docker pull influxdb@sha256:6d63ea8ffbbe69a1f5fa2c07774d41cee507661772a71dc8985723cadfba59d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4906987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c8a2681953ebaf7f935a068bac7cf6c90389e937230469b89280d5975fbb8b6`

```dockerfile
```

-	Layers:
	-	`sha256:db5902a56293c791d5fd153417a19eef14b472fa30124505ccfab0b216fae020`  
		Last Modified: Tue, 12 Nov 2024 03:14:24 GMT  
		Size: 4.9 MB (4891458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cf0ab89723e3a9e346da8b47af9c770ab54dcbdf83aa2e434457385d0a0e9ce`  
		Last Modified: Tue, 12 Nov 2024 03:14:24 GMT  
		Size: 15.5 KB (15529 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:58e9c36d23c8390c8e7f2907d3632ddef461829b77d1ff075edc06ec2d346a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114307283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f61ce3e3698d7018fd179b41f36d6dabc135fc523c5b8fbe9c877d42fd328c27`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ARG INFLUXDB_VERSION=1.11.7
# Sat, 26 Oct 2024 00:18:17 GMT
# ARGS: INFLUXDB_VERSION=1.11.7
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
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
USER influxdb
# Sat, 26 Oct 2024 00:18:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 26 Oct 2024 00:18:17 GMT
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
	-	`sha256:e275fd9ca63ca0cd3a204b4099c6190f479d5109c92539929dcfe36b6233433d`  
		Last Modified: Wed, 13 Nov 2024 03:48:13 GMT  
		Size: 1.2 KB (1197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8a9aca765fda46c9af2db8499bd395b16721982fa017f449d36201af7ec268`  
		Last Modified: Wed, 13 Nov 2024 03:48:15 GMT  
		Size: 41.1 MB (41118918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049e08c5dcbca65c2fdb4a34c87cb93ced6ab1db1428069f1f32fa0240893ac0`  
		Last Modified: Wed, 13 Nov 2024 03:48:13 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509e3c0468d626d1c584a419f76c522a2f01cfe0ba4592821af532f42e30e4b5`  
		Last Modified: Wed, 13 Nov 2024 03:48:13 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6833312ddd1da13e65a045c9f912464b112608851709f74d8e9c02d1f3b8baed`  
		Last Modified: Wed, 13 Nov 2024 03:48:14 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11` - unknown; unknown

```console
$ docker pull influxdb@sha256:892de43323e8f188480097db8b58dad0f54e346ef25e16e9226259753e78f068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4906556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d8c72a14900fa2b0b6b2812ec71cf26fc88d6e1b61277327b3443258768d0b`

```dockerfile
```

-	Layers:
	-	`sha256:ace3aea0952afb93167497bf7ab64b3fc657dc0053e7d7ac7372c1ac4e8cf8b6`  
		Last Modified: Wed, 13 Nov 2024 03:48:13 GMT  
		Size: 4.9 MB (4890932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cc1394972d873d91c45d68adf5b9ea3100b3856be80a99d78fc85cdfc0d9e66`  
		Last Modified: Wed, 13 Nov 2024 03:48:13 GMT  
		Size: 15.6 KB (15624 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-alpine`

```console
$ docker pull influxdb@sha256:f45ec61ec739762ecec383ba5d55ca86e82f907b7bbb5d69123d6f3660b4dfe9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:a002e201c3271a3d4151ec562d7c324efc34e97e3ecec5796e257b32a7eefae8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42918520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec1330db84072017bd79252f180862af357247ac5df6746a3867899790201d74`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Sat, 26 Oct 2024 00:18:17 GMT
RUN apk add --no-cache       bash       ca-certificates       tzdata &&     update-ca-certificates # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ARG INFLUXDB_VERSION=1.11.7
# Sat, 26 Oct 2024 00:18:17 GMT
# ARGS: INFLUXDB_VERSION=1.11.7
RUN apk add --no-cache --virtual .build-deps       curl       gnupg       tar &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     case "$(apk --print-arch)" in       x86_64)  ARCH=amd64 ;;       aarch64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_TAR=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_TAR}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_TAR}" &&     tar -xf "${INFLUXDB_TAR}" -C /usr/bin       ./influx       ./influx_inspect       ./influxd &&     rm -rf "${INFLUXDB_TAR}"            "${INFLUXDB_ASC}" &&     apk del .build-deps # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
# ARGS: INFLUXDB_VERSION=1.11.7
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
EXPOSE map[8086/tcp:{}]
# Sat, 26 Oct 2024 00:18:17 GMT
VOLUME [/var/lib/influxdb]
# Sat, 26 Oct 2024 00:18:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
USER influxdb
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
	-	`sha256:a9131a5e337034b2686216b1985739ffe0a3bd9460b1b7e03204f6e1f9fb01f6`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 1.2 MB (1223720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7ac88a5dd9aa44481ae4cf0a115b46b6e4153527cc1571fbf9ef0886d38928`  
		Last Modified: Tue, 12 Nov 2024 02:14:06 GMT  
		Size: 38.1 MB (38068174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209ce40a5607b135768df20a51419f0c37767ceb4f50d0e80b2b8860105f18da`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b245756632fb1961b2b2462edfe8b61fb69542805c6118497a7d004f37691be`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 1.0 KB (1004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2341371d0a37156eaf7c3323b908aacd0b3a2fb28a5581941947b51143fe1c2e`  
		Last Modified: Tue, 12 Nov 2024 02:14:05 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a509ec9266b86e1e7da3b0f48703fe450469f4b4e9c41fb9bfb7b03e57012a`  
		Last Modified: Tue, 12 Nov 2024 02:14:05 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:0e7646f6b0ad95b87867c4798ee98e3e3ae02acbbbab07cb8d6f9bd388f95754
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.5 KB (759543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c4d7ead3029e3a5bc34766babdb461d9be2704045cd365a76a1128fc95a2f1d`

```dockerfile
```

-	Layers:
	-	`sha256:f2b40641ff42fba9e705fa83f820e7c61083af4e3622ed988258a3de0f17b57e`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 741.7 KB (741652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33ccbef209d8dc99809be1b9eb71d7b2838b972761318888e09f5b924d17fe93`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 17.9 KB (17891 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:669a5cbd19065c425d34e45863127c6cc91257cb669e974e45c1b50ab076a274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40939427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:300478891b750b6448512bffe4a4739873f9bb32b8fb4a5786a39318d90aa212`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Sat, 26 Oct 2024 00:18:17 GMT
RUN apk add --no-cache       bash       ca-certificates       tzdata &&     update-ca-certificates # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ARG INFLUXDB_VERSION=1.11.7
# Sat, 26 Oct 2024 00:18:17 GMT
# ARGS: INFLUXDB_VERSION=1.11.7
RUN apk add --no-cache --virtual .build-deps       curl       gnupg       tar &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     case "$(apk --print-arch)" in       x86_64)  ARCH=amd64 ;;       aarch64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_TAR=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_TAR}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_TAR}" &&     tar -xf "${INFLUXDB_TAR}" -C /usr/bin       ./influx       ./influx_inspect       ./influxd &&     rm -rf "${INFLUXDB_TAR}"            "${INFLUXDB_ASC}" &&     apk del .build-deps # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
# ARGS: INFLUXDB_VERSION=1.11.7
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
EXPOSE map[8086/tcp:{}]
# Sat, 26 Oct 2024 00:18:17 GMT
VOLUME [/var/lib/influxdb]
# Sat, 26 Oct 2024 00:18:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
USER influxdb
# Sat, 26 Oct 2024 00:18:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 26 Oct 2024 00:18:17 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8f287b86ae4c647eb35dd030b8e4042d2b44180d6d1a27b52bf9a59bec42e0`  
		Last Modified: Tue, 12 Nov 2024 13:15:55 GMT  
		Size: 1.3 MB (1303113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e689ad96aab1d62c0e59b33100802e058e548629107cca0847892ff5e523935`  
		Last Modified: Tue, 12 Nov 2024 13:15:56 GMT  
		Size: 35.5 MB (35545864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa1acf46015873a52480e13cb3a08a0a58cc3e0e1af92d0a02fb5cb74e4849e8`  
		Last Modified: Tue, 12 Nov 2024 13:15:55 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a1ac7e07541a81e77a67f21fb1d0cd5836bd9b586e0e76d2966b9d7898c0e1`  
		Last Modified: Tue, 12 Nov 2024 13:15:55 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278d98183d3ce9f462893cd16d98322b970e91573385b44f969cef9b2c211ff7`  
		Last Modified: Tue, 12 Nov 2024 13:15:56 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af121b4e095d9ddbcc01189cfb376b3b2a83c45fd60100d1b128da0d0850aa25`  
		Last Modified: Tue, 12 Nov 2024 13:15:56 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:9f515b5a2d1e71fce72883c59443735f967802b6dbba4c16bf5d58fa73cfddbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **758.9 KB (758890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8de59b8cb1d80d581e7ed9c1adb0faabbca6ecd463c9263b7fb8cf9d96e63708`

```dockerfile
```

-	Layers:
	-	`sha256:b9b62cd0e33182567f41a7ac8c320a45e7db40347eea79d623fd93f77f3508c4`  
		Last Modified: Tue, 12 Nov 2024 13:15:55 GMT  
		Size: 740.9 KB (740889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:914e6e9731883d2e86c946f2b2dece936da015a4b1844b08968d3827a7754f00`  
		Last Modified: Tue, 12 Nov 2024 13:15:55 GMT  
		Size: 18.0 KB (18001 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-data`

```console
$ docker pull influxdb@sha256:04e674cdb05e3ee8d24a5d62130524ba4aa8743bd4a67762a7f6cec87bf2a11a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data` - linux; amd64

```console
$ docker pull influxdb@sha256:5a4988cd82c27016567c01c6d6f81db0f54d836fec75a26bfe6c25184e2f5873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.8 MB (112818961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6242ec624e6a3d80bf6f8188f60b7342e4a0fd9c94449a3f9cf04e731d81a886`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUXDB_VERSION=1.11.7-c1.11.7
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
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc7b6f04730c072f8b292917e0d95bb886096a2b2b1781196170965161cd27`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 24.1 MB (24058346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea66878a914b603ec998a158f5bb4235c71725432fbf2538ceb1f64826ad435c`  
		Last Modified: Tue, 12 Nov 2024 03:14:33 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30be7053d899e7993d29205410b6bede655733c79fcc817f088b807aacc98d1b`  
		Last Modified: Tue, 12 Nov 2024 03:14:35 GMT  
		Size: 39.2 MB (39181360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4b720aebdd6c4f49d25de1e103c9e1e7d093b03d5e0e91c59633ec7b736908`  
		Last Modified: Tue, 12 Nov 2024 03:14:33 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562a1cc973c07a8d57075f683bebb71ec5f477fb6183a14b662e0033528d053a`  
		Last Modified: Tue, 12 Nov 2024 03:14:33 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f707a087719f669007b0b0d415a892ea143a559055877a1d166ea222bca31bd`  
		Last Modified: Tue, 12 Nov 2024 03:14:34 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:a34fb3e27b905c5b1029a72ffe0345ab4711727c19cd6eba5999477f79f5ed3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4530827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49aec9c427731d24d04a605f1b76b26c07070970517ef08365a59cdd09f4a14f`

```dockerfile
```

-	Layers:
	-	`sha256:7c643fdb8b542f8fb6fefb87ce2eb7a80a819a61eedbb9a95867388b6e785212`  
		Last Modified: Tue, 12 Nov 2024 03:14:34 GMT  
		Size: 4.5 MB (4516119 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7acd10b440b89445a3b4de90178c8a20d63223b7cfffa138c50f5dcaa67bc09e`  
		Last Modified: Tue, 12 Nov 2024 03:14:33 GMT  
		Size: 14.7 KB (14708 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-data-alpine`

```console
$ docker pull influxdb@sha256:66ba5d6d20a870a47c21a7e64fb6a4f30089316903deb44173476156f854edad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:e0dde1946425b2fdb0444e975b3eed8520161d1129e2a55ef3a9bd9335577e49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (43973912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc17b73a40842f489c26cbf33bafbe239320354c6615e7e928bdebf73a9b29a`
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
ENV INFLUXDB_VERSION=1.11.7-c1.11.7
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
	-	`sha256:b8359fb22721bda65d61d3b3f43f9ef0bb4da1e7a89cf9bef3befc9dcd7d5c88`  
		Last Modified: Tue, 12 Nov 2024 02:13:58 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e4fa5be5bcbc133931311823895c8a9631c3bfc36b408219870173e78cd3f6`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 1.2 MB (1223725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87449b5d116aaef4c2cf6556ce8feb62ed4025d7f8eadcf19090b91c255f96b4`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 39.1 MB (39124228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9f72a6247fdbc445d27b5286866dbbc81c501491eab865bd51e559d0240e1dd`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734371ec66c7665a18dfa979a2a6b58162fe98fbb67f01c2c5840fa80c1c668c`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b8723d51623cdfb63f2338d2d26a2a4e6e59f8abebd3e614d57c75a6da0cf6`  
		Last Modified: Tue, 12 Nov 2024 02:14:05 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:e2ee8b0429a38773195725a8c59bea3002d5816cb786cd227fe01be12a3a7f14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **768.8 KB (768766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d115344b9cd8bc5cc8b9bcd099dd600de8d928a000716046df8b2c2b014240c2`

```dockerfile
```

-	Layers:
	-	`sha256:98b8b56949b661cb603e7a62a896717985762b311a1965e86b61967b0e5f6988`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 752.1 KB (752127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2f0859fedd477c7c4244a806d9286e1ef1cdf919e26e697f77a55accd1f4831`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-meta`

```console
$ docker pull influxdb@sha256:a99e247df55e515510d4ffd12e7812934d9fde1b1f9d41d51d9b4d090477f8f2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:5301a4df390fa6b803ee52add90dee3b1f30543f2f1876ed18dcc4d26f74f523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (91974831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05d8ec46b19efc5b453cb723a196ca6f64c4c8f7e40af6c50b2e56884200520b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUXDB_VERSION=1.11.7-c1.11.7
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
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc7b6f04730c072f8b292917e0d95bb886096a2b2b1781196170965161cd27`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 24.1 MB (24058346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3815d10d94129dbe2c0391239c2924feac1dee02a65a2ae82df43746c4bbdef`  
		Last Modified: Tue, 12 Nov 2024 03:14:25 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab82b1d09c80c57644d6bc5c8a78a01497bec0f9e6b4c073cfdf8d3abf213e5`  
		Last Modified: Tue, 12 Nov 2024 03:14:26 GMT  
		Size: 18.3 MB (18338441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:815bf657ade04f5a6b1618b296822a78a9accee3ab76a4ad8cd5598629b3d6a2`  
		Last Modified: Tue, 12 Nov 2024 03:14:25 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8953b200e03c4f392dd626922f9ca877502ca2b2e5a40f8b87f30a0c5b4cde6`  
		Last Modified: Tue, 12 Nov 2024 03:14:25 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:49812fbf92cff478b9ed5839854bb385387ae4d5c06b0dcd8f13ac60a3752e95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4454753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:463826e264fe321c8a156bbcefc70aa6cad5a0a16d2082f2e57455c7ce182910`

```dockerfile
```

-	Layers:
	-	`sha256:0120178e04aaa69b0de3da7ce0c076a3a772cc208e9b0ac74c0e899d8c1ae331`  
		Last Modified: Tue, 12 Nov 2024 03:14:25 GMT  
		Size: 4.4 MB (4441686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54efb80efa8cffd004d5446693349924ac23530e2ccc68792c43e4793803e6ee`  
		Last Modified: Tue, 12 Nov 2024 03:14:25 GMT  
		Size: 13.1 KB (13067 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-meta-alpine`

```console
$ docker pull influxdb@sha256:1549bbb0e55e90d70cca1c147da750f70f9fcd3c2bb8aec96c69bcecbdd6b783
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:d837afb02818a9f4d4d1febce43f32c9062d5bc9f6f15757bebc7baeb7643cce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23140481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f017c3f9b98a38aceeb1f7a76bf9d291e483026fa906a1aed904448e8f224116`
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
ENV INFLUXDB_VERSION=1.11.7-c1.11.7
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
	-	`sha256:f5500a9ba2dc5cb166b0771fab2f3f789f884e3d9f2180c4a81c2e82a343c381`  
		Last Modified: Tue, 12 Nov 2024 02:13:58 GMT  
		Size: 1.2 MB (1223720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ef9a39a778950824d2e1102f97241ccaf462668f9538b7c887c99d72a5fe74`  
		Last Modified: Tue, 12 Nov 2024 02:13:59 GMT  
		Size: 18.3 MB (18292011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afe355e739584b4f545ac8dbaafe003c128f5a72fa829c06febf87a21b66686`  
		Last Modified: Tue, 12 Nov 2024 02:13:58 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ac8a742b468f3c02e888dd1adbd00a8fd8101c0eedab738dc6ed9d27d2f319`  
		Last Modified: Tue, 12 Nov 2024 02:13:59 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:6a21e7bde65a50a40f594bb83fcd6886d2debe86b0f3031c4ee61bcca5526111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **693.5 KB (693491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1656e0378f152a9777b29a376059df5a0def977eee8ffbe7d56f9e3d7fc85ae1`

```dockerfile
```

-	Layers:
	-	`sha256:a8ce92d26a0fa3c7573b7c57a74c3395e4a517b9b7f451e2b9253504edcd5b53`  
		Last Modified: Tue, 12 Nov 2024 02:13:59 GMT  
		Size: 678.5 KB (678481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9d36d12dedc814e91f58f183ecbdafa170831616ea21b5a8c5104f017ffc395`  
		Last Modified: Tue, 12 Nov 2024 02:13:58 GMT  
		Size: 15.0 KB (15010 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.7`

```console
$ docker pull influxdb@sha256:200232d77ed6efc06db2e514e0da4426601577700aae3b7164412b2c06d8e93a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11.7` - linux; amd64

```console
$ docker pull influxdb@sha256:fce87665015043ae7cc75ccdb873f9f8dc00ef92dee50e2e7a08ddf7825cea31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.3 MB (117286270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d02473da4f26853abaf94ee1cdb4a7fd402e69d06f7f5f1fbd4f7b6d7d503934`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ARG INFLUXDB_VERSION=1.11.7
# Sat, 26 Oct 2024 00:18:17 GMT
# ARGS: INFLUXDB_VERSION=1.11.7
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
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
USER influxdb
# Sat, 26 Oct 2024 00:18:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 26 Oct 2024 00:18:17 GMT
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
	-	`sha256:d1a683cb677917f570dd15854dc6823793c99f935156cbb5f2d2b403d9be867a`  
		Last Modified: Tue, 12 Nov 2024 03:14:24 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:167aba5b317025bb8927325814fe1e358e8bf953070ed0939e4ea2a1d20dffb7`  
		Last Modified: Tue, 12 Nov 2024 03:14:24 GMT  
		Size: 43.6 MB (43649316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad040ea3f07fdc575b52dc19571d397e6f819c2efb97a47934e9d95e4069e81`  
		Last Modified: Tue, 12 Nov 2024 03:14:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc7a6d4123d188202e71f4446010b0ed37125366f9fb09afac53d94c49cddbef`  
		Last Modified: Tue, 12 Nov 2024 03:14:24 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df020ff2a521aae398dec31b1fbcac439aad9e1eb576ee9c922767401d172e6`  
		Last Modified: Tue, 12 Nov 2024 03:14:24 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:6d63ea8ffbbe69a1f5fa2c07774d41cee507661772a71dc8985723cadfba59d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4906987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c8a2681953ebaf7f935a068bac7cf6c90389e937230469b89280d5975fbb8b6`

```dockerfile
```

-	Layers:
	-	`sha256:db5902a56293c791d5fd153417a19eef14b472fa30124505ccfab0b216fae020`  
		Last Modified: Tue, 12 Nov 2024 03:14:24 GMT  
		Size: 4.9 MB (4891458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cf0ab89723e3a9e346da8b47af9c770ab54dcbdf83aa2e434457385d0a0e9ce`  
		Last Modified: Tue, 12 Nov 2024 03:14:24 GMT  
		Size: 15.5 KB (15529 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11.7` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:58e9c36d23c8390c8e7f2907d3632ddef461829b77d1ff075edc06ec2d346a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114307283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f61ce3e3698d7018fd179b41f36d6dabc135fc523c5b8fbe9c877d42fd328c27`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ARG INFLUXDB_VERSION=1.11.7
# Sat, 26 Oct 2024 00:18:17 GMT
# ARGS: INFLUXDB_VERSION=1.11.7
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
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
USER influxdb
# Sat, 26 Oct 2024 00:18:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 26 Oct 2024 00:18:17 GMT
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
	-	`sha256:e275fd9ca63ca0cd3a204b4099c6190f479d5109c92539929dcfe36b6233433d`  
		Last Modified: Wed, 13 Nov 2024 03:48:13 GMT  
		Size: 1.2 KB (1197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8a9aca765fda46c9af2db8499bd395b16721982fa017f449d36201af7ec268`  
		Last Modified: Wed, 13 Nov 2024 03:48:15 GMT  
		Size: 41.1 MB (41118918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049e08c5dcbca65c2fdb4a34c87cb93ced6ab1db1428069f1f32fa0240893ac0`  
		Last Modified: Wed, 13 Nov 2024 03:48:13 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509e3c0468d626d1c584a419f76c522a2f01cfe0ba4592821af532f42e30e4b5`  
		Last Modified: Wed, 13 Nov 2024 03:48:13 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6833312ddd1da13e65a045c9f912464b112608851709f74d8e9c02d1f3b8baed`  
		Last Modified: Wed, 13 Nov 2024 03:48:14 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:892de43323e8f188480097db8b58dad0f54e346ef25e16e9226259753e78f068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4906556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d8c72a14900fa2b0b6b2812ec71cf26fc88d6e1b61277327b3443258768d0b`

```dockerfile
```

-	Layers:
	-	`sha256:ace3aea0952afb93167497bf7ab64b3fc657dc0053e7d7ac7372c1ac4e8cf8b6`  
		Last Modified: Wed, 13 Nov 2024 03:48:13 GMT  
		Size: 4.9 MB (4890932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cc1394972d873d91c45d68adf5b9ea3100b3856be80a99d78fc85cdfc0d9e66`  
		Last Modified: Wed, 13 Nov 2024 03:48:13 GMT  
		Size: 15.6 KB (15624 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.7-alpine`

```console
$ docker pull influxdb@sha256:f45ec61ec739762ecec383ba5d55ca86e82f907b7bbb5d69123d6f3660b4dfe9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11.7-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:a002e201c3271a3d4151ec562d7c324efc34e97e3ecec5796e257b32a7eefae8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42918520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec1330db84072017bd79252f180862af357247ac5df6746a3867899790201d74`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Sat, 26 Oct 2024 00:18:17 GMT
RUN apk add --no-cache       bash       ca-certificates       tzdata &&     update-ca-certificates # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ARG INFLUXDB_VERSION=1.11.7
# Sat, 26 Oct 2024 00:18:17 GMT
# ARGS: INFLUXDB_VERSION=1.11.7
RUN apk add --no-cache --virtual .build-deps       curl       gnupg       tar &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     case "$(apk --print-arch)" in       x86_64)  ARCH=amd64 ;;       aarch64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_TAR=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_TAR}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_TAR}" &&     tar -xf "${INFLUXDB_TAR}" -C /usr/bin       ./influx       ./influx_inspect       ./influxd &&     rm -rf "${INFLUXDB_TAR}"            "${INFLUXDB_ASC}" &&     apk del .build-deps # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
# ARGS: INFLUXDB_VERSION=1.11.7
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
EXPOSE map[8086/tcp:{}]
# Sat, 26 Oct 2024 00:18:17 GMT
VOLUME [/var/lib/influxdb]
# Sat, 26 Oct 2024 00:18:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
USER influxdb
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
	-	`sha256:a9131a5e337034b2686216b1985739ffe0a3bd9460b1b7e03204f6e1f9fb01f6`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 1.2 MB (1223720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7ac88a5dd9aa44481ae4cf0a115b46b6e4153527cc1571fbf9ef0886d38928`  
		Last Modified: Tue, 12 Nov 2024 02:14:06 GMT  
		Size: 38.1 MB (38068174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209ce40a5607b135768df20a51419f0c37767ceb4f50d0e80b2b8860105f18da`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b245756632fb1961b2b2462edfe8b61fb69542805c6118497a7d004f37691be`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 1.0 KB (1004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2341371d0a37156eaf7c3323b908aacd0b3a2fb28a5581941947b51143fe1c2e`  
		Last Modified: Tue, 12 Nov 2024 02:14:05 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a509ec9266b86e1e7da3b0f48703fe450469f4b4e9c41fb9bfb7b03e57012a`  
		Last Modified: Tue, 12 Nov 2024 02:14:05 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.7-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:0e7646f6b0ad95b87867c4798ee98e3e3ae02acbbbab07cb8d6f9bd388f95754
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.5 KB (759543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c4d7ead3029e3a5bc34766babdb461d9be2704045cd365a76a1128fc95a2f1d`

```dockerfile
```

-	Layers:
	-	`sha256:f2b40641ff42fba9e705fa83f820e7c61083af4e3622ed988258a3de0f17b57e`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 741.7 KB (741652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33ccbef209d8dc99809be1b9eb71d7b2838b972761318888e09f5b924d17fe93`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 17.9 KB (17891 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11.7-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:669a5cbd19065c425d34e45863127c6cc91257cb669e974e45c1b50ab076a274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40939427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:300478891b750b6448512bffe4a4739873f9bb32b8fb4a5786a39318d90aa212`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Sat, 26 Oct 2024 00:18:17 GMT
RUN apk add --no-cache       bash       ca-certificates       tzdata &&     update-ca-certificates # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ARG INFLUXDB_VERSION=1.11.7
# Sat, 26 Oct 2024 00:18:17 GMT
# ARGS: INFLUXDB_VERSION=1.11.7
RUN apk add --no-cache --virtual .build-deps       curl       gnupg       tar &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     case "$(apk --print-arch)" in       x86_64)  ARCH=amd64 ;;       aarch64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_TAR=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_TAR}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_TAR}" &&     tar -xf "${INFLUXDB_TAR}" -C /usr/bin       ./influx       ./influx_inspect       ./influxd &&     rm -rf "${INFLUXDB_TAR}"            "${INFLUXDB_ASC}" &&     apk del .build-deps # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
# ARGS: INFLUXDB_VERSION=1.11.7
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
EXPOSE map[8086/tcp:{}]
# Sat, 26 Oct 2024 00:18:17 GMT
VOLUME [/var/lib/influxdb]
# Sat, 26 Oct 2024 00:18:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
USER influxdb
# Sat, 26 Oct 2024 00:18:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 26 Oct 2024 00:18:17 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8f287b86ae4c647eb35dd030b8e4042d2b44180d6d1a27b52bf9a59bec42e0`  
		Last Modified: Tue, 12 Nov 2024 13:15:55 GMT  
		Size: 1.3 MB (1303113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e689ad96aab1d62c0e59b33100802e058e548629107cca0847892ff5e523935`  
		Last Modified: Tue, 12 Nov 2024 13:15:56 GMT  
		Size: 35.5 MB (35545864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa1acf46015873a52480e13cb3a08a0a58cc3e0e1af92d0a02fb5cb74e4849e8`  
		Last Modified: Tue, 12 Nov 2024 13:15:55 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a1ac7e07541a81e77a67f21fb1d0cd5836bd9b586e0e76d2966b9d7898c0e1`  
		Last Modified: Tue, 12 Nov 2024 13:15:55 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278d98183d3ce9f462893cd16d98322b970e91573385b44f969cef9b2c211ff7`  
		Last Modified: Tue, 12 Nov 2024 13:15:56 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af121b4e095d9ddbcc01189cfb376b3b2a83c45fd60100d1b128da0d0850aa25`  
		Last Modified: Tue, 12 Nov 2024 13:15:56 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.7-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:9f515b5a2d1e71fce72883c59443735f967802b6dbba4c16bf5d58fa73cfddbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **758.9 KB (758890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8de59b8cb1d80d581e7ed9c1adb0faabbca6ecd463c9263b7fb8cf9d96e63708`

```dockerfile
```

-	Layers:
	-	`sha256:b9b62cd0e33182567f41a7ac8c320a45e7db40347eea79d623fd93f77f3508c4`  
		Last Modified: Tue, 12 Nov 2024 13:15:55 GMT  
		Size: 740.9 KB (740889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:914e6e9731883d2e86c946f2b2dece936da015a4b1844b08968d3827a7754f00`  
		Last Modified: Tue, 12 Nov 2024 13:15:55 GMT  
		Size: 18.0 KB (18001 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.7-data`

```console
$ docker pull influxdb@sha256:04e674cdb05e3ee8d24a5d62130524ba4aa8743bd4a67762a7f6cec87bf2a11a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.7-data` - linux; amd64

```console
$ docker pull influxdb@sha256:5a4988cd82c27016567c01c6d6f81db0f54d836fec75a26bfe6c25184e2f5873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.8 MB (112818961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6242ec624e6a3d80bf6f8188f60b7342e4a0fd9c94449a3f9cf04e731d81a886`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUXDB_VERSION=1.11.7-c1.11.7
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
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc7b6f04730c072f8b292917e0d95bb886096a2b2b1781196170965161cd27`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 24.1 MB (24058346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea66878a914b603ec998a158f5bb4235c71725432fbf2538ceb1f64826ad435c`  
		Last Modified: Tue, 12 Nov 2024 03:14:33 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30be7053d899e7993d29205410b6bede655733c79fcc817f088b807aacc98d1b`  
		Last Modified: Tue, 12 Nov 2024 03:14:35 GMT  
		Size: 39.2 MB (39181360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4b720aebdd6c4f49d25de1e103c9e1e7d093b03d5e0e91c59633ec7b736908`  
		Last Modified: Tue, 12 Nov 2024 03:14:33 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562a1cc973c07a8d57075f683bebb71ec5f477fb6183a14b662e0033528d053a`  
		Last Modified: Tue, 12 Nov 2024 03:14:33 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f707a087719f669007b0b0d415a892ea143a559055877a1d166ea222bca31bd`  
		Last Modified: Tue, 12 Nov 2024 03:14:34 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.7-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:a34fb3e27b905c5b1029a72ffe0345ab4711727c19cd6eba5999477f79f5ed3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4530827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49aec9c427731d24d04a605f1b76b26c07070970517ef08365a59cdd09f4a14f`

```dockerfile
```

-	Layers:
	-	`sha256:7c643fdb8b542f8fb6fefb87ce2eb7a80a819a61eedbb9a95867388b6e785212`  
		Last Modified: Tue, 12 Nov 2024 03:14:34 GMT  
		Size: 4.5 MB (4516119 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7acd10b440b89445a3b4de90178c8a20d63223b7cfffa138c50f5dcaa67bc09e`  
		Last Modified: Tue, 12 Nov 2024 03:14:33 GMT  
		Size: 14.7 KB (14708 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.7-data-alpine`

```console
$ docker pull influxdb@sha256:66ba5d6d20a870a47c21a7e64fb6a4f30089316903deb44173476156f854edad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.7-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:e0dde1946425b2fdb0444e975b3eed8520161d1129e2a55ef3a9bd9335577e49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (43973912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc17b73a40842f489c26cbf33bafbe239320354c6615e7e928bdebf73a9b29a`
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
ENV INFLUXDB_VERSION=1.11.7-c1.11.7
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
	-	`sha256:b8359fb22721bda65d61d3b3f43f9ef0bb4da1e7a89cf9bef3befc9dcd7d5c88`  
		Last Modified: Tue, 12 Nov 2024 02:13:58 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e4fa5be5bcbc133931311823895c8a9631c3bfc36b408219870173e78cd3f6`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 1.2 MB (1223725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87449b5d116aaef4c2cf6556ce8feb62ed4025d7f8eadcf19090b91c255f96b4`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 39.1 MB (39124228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9f72a6247fdbc445d27b5286866dbbc81c501491eab865bd51e559d0240e1dd`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734371ec66c7665a18dfa979a2a6b58162fe98fbb67f01c2c5840fa80c1c668c`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b8723d51623cdfb63f2338d2d26a2a4e6e59f8abebd3e614d57c75a6da0cf6`  
		Last Modified: Tue, 12 Nov 2024 02:14:05 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.7-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:e2ee8b0429a38773195725a8c59bea3002d5816cb786cd227fe01be12a3a7f14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **768.8 KB (768766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d115344b9cd8bc5cc8b9bcd099dd600de8d928a000716046df8b2c2b014240c2`

```dockerfile
```

-	Layers:
	-	`sha256:98b8b56949b661cb603e7a62a896717985762b311a1965e86b61967b0e5f6988`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 752.1 KB (752127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2f0859fedd477c7c4244a806d9286e1ef1cdf919e26e697f77a55accd1f4831`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.7-meta`

```console
$ docker pull influxdb@sha256:a99e247df55e515510d4ffd12e7812934d9fde1b1f9d41d51d9b4d090477f8f2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.7-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:5301a4df390fa6b803ee52add90dee3b1f30543f2f1876ed18dcc4d26f74f523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (91974831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05d8ec46b19efc5b453cb723a196ca6f64c4c8f7e40af6c50b2e56884200520b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUXDB_VERSION=1.11.7-c1.11.7
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
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc7b6f04730c072f8b292917e0d95bb886096a2b2b1781196170965161cd27`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 24.1 MB (24058346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3815d10d94129dbe2c0391239c2924feac1dee02a65a2ae82df43746c4bbdef`  
		Last Modified: Tue, 12 Nov 2024 03:14:25 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab82b1d09c80c57644d6bc5c8a78a01497bec0f9e6b4c073cfdf8d3abf213e5`  
		Last Modified: Tue, 12 Nov 2024 03:14:26 GMT  
		Size: 18.3 MB (18338441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:815bf657ade04f5a6b1618b296822a78a9accee3ab76a4ad8cd5598629b3d6a2`  
		Last Modified: Tue, 12 Nov 2024 03:14:25 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8953b200e03c4f392dd626922f9ca877502ca2b2e5a40f8b87f30a0c5b4cde6`  
		Last Modified: Tue, 12 Nov 2024 03:14:25 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.7-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:49812fbf92cff478b9ed5839854bb385387ae4d5c06b0dcd8f13ac60a3752e95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4454753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:463826e264fe321c8a156bbcefc70aa6cad5a0a16d2082f2e57455c7ce182910`

```dockerfile
```

-	Layers:
	-	`sha256:0120178e04aaa69b0de3da7ce0c076a3a772cc208e9b0ac74c0e899d8c1ae331`  
		Last Modified: Tue, 12 Nov 2024 03:14:25 GMT  
		Size: 4.4 MB (4441686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54efb80efa8cffd004d5446693349924ac23530e2ccc68792c43e4793803e6ee`  
		Last Modified: Tue, 12 Nov 2024 03:14:25 GMT  
		Size: 13.1 KB (13067 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.7-meta-alpine`

```console
$ docker pull influxdb@sha256:1549bbb0e55e90d70cca1c147da750f70f9fcd3c2bb8aec96c69bcecbdd6b783
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.7-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:d837afb02818a9f4d4d1febce43f32c9062d5bc9f6f15757bebc7baeb7643cce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23140481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f017c3f9b98a38aceeb1f7a76bf9d291e483026fa906a1aed904448e8f224116`
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
ENV INFLUXDB_VERSION=1.11.7-c1.11.7
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
	-	`sha256:f5500a9ba2dc5cb166b0771fab2f3f789f884e3d9f2180c4a81c2e82a343c381`  
		Last Modified: Tue, 12 Nov 2024 02:13:58 GMT  
		Size: 1.2 MB (1223720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ef9a39a778950824d2e1102f97241ccaf462668f9538b7c887c99d72a5fe74`  
		Last Modified: Tue, 12 Nov 2024 02:13:59 GMT  
		Size: 18.3 MB (18292011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afe355e739584b4f545ac8dbaafe003c128f5a72fa829c06febf87a21b66686`  
		Last Modified: Tue, 12 Nov 2024 02:13:58 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ac8a742b468f3c02e888dd1adbd00a8fd8101c0eedab738dc6ed9d27d2f319`  
		Last Modified: Tue, 12 Nov 2024 02:13:59 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.7-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:6a21e7bde65a50a40f594bb83fcd6886d2debe86b0f3031c4ee61bcca5526111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **693.5 KB (693491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1656e0378f152a9777b29a376059df5a0def977eee8ffbe7d56f9e3d7fc85ae1`

```dockerfile
```

-	Layers:
	-	`sha256:a8ce92d26a0fa3c7573b7c57a74c3395e4a517b9b7f451e2b9253504edcd5b53`  
		Last Modified: Tue, 12 Nov 2024 02:13:59 GMT  
		Size: 678.5 KB (678481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9d36d12dedc814e91f58f183ecbdafa170831616ea21b5a8c5104f017ffc395`  
		Last Modified: Tue, 12 Nov 2024 02:13:58 GMT  
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

## `influxdb:2.7.10`

```console
$ docker pull influxdb@sha256:b4cd4b71bc8528c5cb6b9dede79091a234f9f565a3177b8fc4c2cc835bf5c142
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7.10` - linux; amd64

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

### `influxdb:2.7.10` - unknown; unknown

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

### `influxdb:2.7.10` - linux; arm64 variant v8

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

### `influxdb:2.7.10` - unknown; unknown

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

## `influxdb:2.7.10-alpine`

```console
$ docker pull influxdb@sha256:c5fcf0f3e6fc4d30646666ce9466e5022f2d35ab30ee56fc254da7b00897ac90
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7.10-alpine` - linux; amd64

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

### `influxdb:2.7.10-alpine` - unknown; unknown

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

### `influxdb:2.7.10-alpine` - linux; arm64 variant v8

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

### `influxdb:2.7.10-alpine` - unknown; unknown

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
