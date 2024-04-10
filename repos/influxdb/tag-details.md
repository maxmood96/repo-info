<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `influxdb`

-	[`influxdb:1.10-data`](#influxdb110-data)
-	[`influxdb:1.10-data-alpine`](#influxdb110-data-alpine)
-	[`influxdb:1.10-meta`](#influxdb110-meta)
-	[`influxdb:1.10-meta-alpine`](#influxdb110-meta-alpine)
-	[`influxdb:1.10.5-data`](#influxdb1105-data)
-	[`influxdb:1.10.5-data-alpine`](#influxdb1105-data-alpine)
-	[`influxdb:1.10.5-meta`](#influxdb1105-meta)
-	[`influxdb:1.10.5-meta-alpine`](#influxdb1105-meta-alpine)
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
-	[`influxdb:2.7.5`](#influxdb275)
-	[`influxdb:2.7.5-alpine`](#influxdb275-alpine)
-	[`influxdb:alpine`](#influxdbalpine)
-	[`influxdb:latest`](#influxdblatest)

## `influxdb:1.10-data`

```console
$ docker pull influxdb@sha256:d33dcb61b53f993119043c1bc216274a7948130111d8d88f344dbac56d7a5c86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.10-data` - linux; amd64

```console
$ docker pull influxdb@sha256:f23f4db942625f3ca2fa316e0d7cc579fad08bf6cb0871d3bbf127f57c8cadd4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.0 MB (111033682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec8403a00dde8cb346d847a113339fbe06902a71da8a6ac5c02adbb0b92083f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:59 GMT
ADD file:8efdcc3201e79c8a09fc9c1ade08492ea33f838047332a7c61988f6357339dee in / 
# Wed, 10 Apr 2024 01:50:59 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:43:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 05:43:57 GMT
ENV INFLUXDB_VERSION=1.10.5-c1.10.5
# Wed, 10 Apr 2024 05:44:02 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb*
# Wed, 10 Apr 2024 05:44:02 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 10 Apr 2024 05:44:02 GMT
EXPOSE 8086
# Wed, 10 Apr 2024 05:44:02 GMT
VOLUME [/var/lib/influxdb]
# Wed, 10 Apr 2024 05:44:03 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 10 Apr 2024 05:44:03 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 10 Apr 2024 05:44:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 05:44:03 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:ac323bdaa10f869bd9e7adecd8f5326e44acc4c59168868108b1cdf3891089cc`  
		Last Modified: Wed, 10 Apr 2024 01:55:52 GMT  
		Size: 55.1 MB (55090264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84811b2a563b9003abbd1c06f6e45a857315b931855030bdd0443d13d950a996`  
		Last Modified: Wed, 10 Apr 2024 05:36:00 GMT  
		Size: 15.8 MB (15763518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f109c707be2928b7b5cb0f6cd61dba161e7b02c280e743ac20347edd14fd394e`  
		Last Modified: Wed, 10 Apr 2024 05:45:31 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81c0c7a4a4d4bd89ba63c5ffc9489634842f2e0cb2c44ff5ccb9af0181c785e0`  
		Last Modified: Wed, 10 Apr 2024 05:46:17 GMT  
		Size: 40.2 MB (40176309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9360bffa7d213301723b35902323c8dd265ed2b00fe7f99afdbcb242eafbf991`  
		Last Modified: Wed, 10 Apr 2024 05:46:11 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c308f66ac3fff7a6166e652db5fa9455ff06f44faa41eee50592a926c3dfc777`  
		Last Modified: Wed, 10 Apr 2024 05:46:11 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:784520651675d155257442f4af17787e2b3434cd4b7343f4244eb5ae617ebb91`  
		Last Modified: Wed, 10 Apr 2024 05:46:11 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.10-data-alpine`

```console
$ docker pull influxdb@sha256:0df971794bf04f92619b1ad3d5cb886ce92a53a59bbde02b76af78d0f169a820
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.10-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:6e47da72db07d8d568c8a88927785dd57837660a09e764d1c97f9ceb62c612ca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (44985259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e515cc1ad08809bed1cef610a1f67d31d816571978bf14d37fe5fb129fc352df`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:20:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 07:54:19 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Sat, 16 Mar 2024 07:54:55 GMT
ENV INFLUXDB_VERSION=1.10.5-c1.10.5
# Sat, 16 Mar 2024 07:55:06 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 16 Mar 2024 07:55:06 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Sat, 16 Mar 2024 07:55:06 GMT
EXPOSE 8086
# Sat, 16 Mar 2024 07:55:06 GMT
VOLUME [/var/lib/influxdb]
# Sat, 16 Mar 2024 07:55:06 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Sat, 16 Mar 2024 07:55:06 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sat, 16 Mar 2024 07:55:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 07:55:07 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:485cfb0fb6cd4129a6e7d303f3ebec56b5c133689199b5426db52a97cdafd15a`  
		Last Modified: Sat, 16 Mar 2024 03:21:13 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36314c9e553b2628ec2b88878449957443671f3e9bdf1ac3142d78358c5c95cd`  
		Last Modified: Sat, 16 Mar 2024 07:56:23 GMT  
		Size: 1.5 MB (1470621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b26344ec21a18de3d9a13f9bb90d3c45b03988de5c7495c613dafc2bca0cd518`  
		Last Modified: Sat, 16 Mar 2024 07:57:05 GMT  
		Size: 40.1 MB (40133159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:917aa8bd48012b3768b71d498b6e929cbe9dd090d850a36df141105149425e6e`  
		Last Modified: Sat, 16 Mar 2024 07:57:00 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a5b5fdd02347eccf3ad623f87462e4bfeae378236a62f93fec08f164289b0a`  
		Last Modified: Sat, 16 Mar 2024 07:57:00 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e95cdba8c096783757cda0d20542034451cc5544d3add08bc7492bc25414fa0`  
		Last Modified: Sat, 16 Mar 2024 07:57:00 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.10-meta`

```console
$ docker pull influxdb@sha256:fc2e0715f995fd3865f79f0f3eeac36d359b91325700ed7ea3d13537eb72ef66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.10-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:7d17cd2ab554aadf13786dcf22d7e7c42b1cebddfff77cac1334f93c3d84aec3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91233139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6065ca188c7ede7761c844bcd5c37f4c1cc7b81797e8503b3eedf3b9b86d2688`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:59 GMT
ADD file:8efdcc3201e79c8a09fc9c1ade08492ea33f838047332a7c61988f6357339dee in / 
# Wed, 10 Apr 2024 01:50:59 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:43:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 05:43:57 GMT
ENV INFLUXDB_VERSION=1.10.5-c1.10.5
# Wed, 10 Apr 2024 05:44:12 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb*
# Wed, 10 Apr 2024 05:44:12 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 10 Apr 2024 05:44:12 GMT
EXPOSE 8091
# Wed, 10 Apr 2024 05:44:12 GMT
VOLUME [/var/lib/influxdb]
# Wed, 10 Apr 2024 05:44:12 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 10 Apr 2024 05:44:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 05:44:13 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:ac323bdaa10f869bd9e7adecd8f5326e44acc4c59168868108b1cdf3891089cc`  
		Last Modified: Wed, 10 Apr 2024 01:55:52 GMT  
		Size: 55.1 MB (55090264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84811b2a563b9003abbd1c06f6e45a857315b931855030bdd0443d13d950a996`  
		Last Modified: Wed, 10 Apr 2024 05:36:00 GMT  
		Size: 15.8 MB (15763518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f109c707be2928b7b5cb0f6cd61dba161e7b02c280e743ac20347edd14fd394e`  
		Last Modified: Wed, 10 Apr 2024 05:45:31 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:483a08364fbe0e0e9f7f8d7fa4088a69cc322ff49d455bb02f7476083f21e071`  
		Last Modified: Wed, 10 Apr 2024 05:46:29 GMT  
		Size: 20.4 MB (20376970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea0d33c965d33b5756192a1921456e7e8415ffdf2cc943befc139d8b86c6341`  
		Last Modified: Wed, 10 Apr 2024 05:46:26 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98aac2e9ac504acf9f3fd3fdd571f4c24ddd1c8b77d50d1584b4b56e00a28f2a`  
		Last Modified: Wed, 10 Apr 2024 05:46:26 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.10-meta-alpine`

```console
$ docker pull influxdb@sha256:47b8526c9b9e2b41bc77357a5969faea561a0f20f3b66aab1e0a920c42fb6143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.10-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:dcb846d06d314e43c18dbe62f4e03b49c0ed08c2e5f1cf2eb653ba8a4b0d7b44
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25194389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a536b3b0d15d5dfc12ab1cb129829b538b116fd18a531044aca7dacb7b6187d9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:20:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 07:54:19 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Sat, 16 Mar 2024 07:54:55 GMT
ENV INFLUXDB_VERSION=1.10.5-c1.10.5
# Sat, 16 Mar 2024 07:55:18 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 16 Mar 2024 07:55:18 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Sat, 16 Mar 2024 07:55:18 GMT
EXPOSE 8091
# Sat, 16 Mar 2024 07:55:18 GMT
VOLUME [/var/lib/influxdb]
# Sat, 16 Mar 2024 07:55:18 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Sat, 16 Mar 2024 07:55:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 07:55:19 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:485cfb0fb6cd4129a6e7d303f3ebec56b5c133689199b5426db52a97cdafd15a`  
		Last Modified: Sat, 16 Mar 2024 03:21:13 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36314c9e553b2628ec2b88878449957443671f3e9bdf1ac3142d78358c5c95cd`  
		Last Modified: Sat, 16 Mar 2024 07:56:23 GMT  
		Size: 1.5 MB (1470621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1f6ceb15b042d68232e0e6da8cbb800e744dfc1dc7c1d74fb0fb616dda3cb04`  
		Last Modified: Sat, 16 Mar 2024 07:57:17 GMT  
		Size: 20.3 MB (20343496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e643707bf15117d88879726bc8bfc26be16ac5037fa52ad62aff4dc3f7b7f2`  
		Last Modified: Sat, 16 Mar 2024 07:57:14 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d75f88729bfacec3b3ce39587d58bf11246ac55364c9e5370acddb319deb709`  
		Last Modified: Sat, 16 Mar 2024 07:57:14 GMT  
		Size: 372.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.10.5-data`

```console
$ docker pull influxdb@sha256:d33dcb61b53f993119043c1bc216274a7948130111d8d88f344dbac56d7a5c86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.10.5-data` - linux; amd64

```console
$ docker pull influxdb@sha256:f23f4db942625f3ca2fa316e0d7cc579fad08bf6cb0871d3bbf127f57c8cadd4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.0 MB (111033682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec8403a00dde8cb346d847a113339fbe06902a71da8a6ac5c02adbb0b92083f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:59 GMT
ADD file:8efdcc3201e79c8a09fc9c1ade08492ea33f838047332a7c61988f6357339dee in / 
# Wed, 10 Apr 2024 01:50:59 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:43:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 05:43:57 GMT
ENV INFLUXDB_VERSION=1.10.5-c1.10.5
# Wed, 10 Apr 2024 05:44:02 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb*
# Wed, 10 Apr 2024 05:44:02 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 10 Apr 2024 05:44:02 GMT
EXPOSE 8086
# Wed, 10 Apr 2024 05:44:02 GMT
VOLUME [/var/lib/influxdb]
# Wed, 10 Apr 2024 05:44:03 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 10 Apr 2024 05:44:03 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 10 Apr 2024 05:44:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 05:44:03 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:ac323bdaa10f869bd9e7adecd8f5326e44acc4c59168868108b1cdf3891089cc`  
		Last Modified: Wed, 10 Apr 2024 01:55:52 GMT  
		Size: 55.1 MB (55090264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84811b2a563b9003abbd1c06f6e45a857315b931855030bdd0443d13d950a996`  
		Last Modified: Wed, 10 Apr 2024 05:36:00 GMT  
		Size: 15.8 MB (15763518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f109c707be2928b7b5cb0f6cd61dba161e7b02c280e743ac20347edd14fd394e`  
		Last Modified: Wed, 10 Apr 2024 05:45:31 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81c0c7a4a4d4bd89ba63c5ffc9489634842f2e0cb2c44ff5ccb9af0181c785e0`  
		Last Modified: Wed, 10 Apr 2024 05:46:17 GMT  
		Size: 40.2 MB (40176309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9360bffa7d213301723b35902323c8dd265ed2b00fe7f99afdbcb242eafbf991`  
		Last Modified: Wed, 10 Apr 2024 05:46:11 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c308f66ac3fff7a6166e652db5fa9455ff06f44faa41eee50592a926c3dfc777`  
		Last Modified: Wed, 10 Apr 2024 05:46:11 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:784520651675d155257442f4af17787e2b3434cd4b7343f4244eb5ae617ebb91`  
		Last Modified: Wed, 10 Apr 2024 05:46:11 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.10.5-data-alpine`

```console
$ docker pull influxdb@sha256:0df971794bf04f92619b1ad3d5cb886ce92a53a59bbde02b76af78d0f169a820
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.10.5-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:6e47da72db07d8d568c8a88927785dd57837660a09e764d1c97f9ceb62c612ca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (44985259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e515cc1ad08809bed1cef610a1f67d31d816571978bf14d37fe5fb129fc352df`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:20:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 07:54:19 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Sat, 16 Mar 2024 07:54:55 GMT
ENV INFLUXDB_VERSION=1.10.5-c1.10.5
# Sat, 16 Mar 2024 07:55:06 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 16 Mar 2024 07:55:06 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Sat, 16 Mar 2024 07:55:06 GMT
EXPOSE 8086
# Sat, 16 Mar 2024 07:55:06 GMT
VOLUME [/var/lib/influxdb]
# Sat, 16 Mar 2024 07:55:06 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Sat, 16 Mar 2024 07:55:06 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sat, 16 Mar 2024 07:55:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 07:55:07 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:485cfb0fb6cd4129a6e7d303f3ebec56b5c133689199b5426db52a97cdafd15a`  
		Last Modified: Sat, 16 Mar 2024 03:21:13 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36314c9e553b2628ec2b88878449957443671f3e9bdf1ac3142d78358c5c95cd`  
		Last Modified: Sat, 16 Mar 2024 07:56:23 GMT  
		Size: 1.5 MB (1470621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b26344ec21a18de3d9a13f9bb90d3c45b03988de5c7495c613dafc2bca0cd518`  
		Last Modified: Sat, 16 Mar 2024 07:57:05 GMT  
		Size: 40.1 MB (40133159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:917aa8bd48012b3768b71d498b6e929cbe9dd090d850a36df141105149425e6e`  
		Last Modified: Sat, 16 Mar 2024 07:57:00 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a5b5fdd02347eccf3ad623f87462e4bfeae378236a62f93fec08f164289b0a`  
		Last Modified: Sat, 16 Mar 2024 07:57:00 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e95cdba8c096783757cda0d20542034451cc5544d3add08bc7492bc25414fa0`  
		Last Modified: Sat, 16 Mar 2024 07:57:00 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.10.5-meta`

```console
$ docker pull influxdb@sha256:fc2e0715f995fd3865f79f0f3eeac36d359b91325700ed7ea3d13537eb72ef66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.10.5-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:7d17cd2ab554aadf13786dcf22d7e7c42b1cebddfff77cac1334f93c3d84aec3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91233139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6065ca188c7ede7761c844bcd5c37f4c1cc7b81797e8503b3eedf3b9b86d2688`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:59 GMT
ADD file:8efdcc3201e79c8a09fc9c1ade08492ea33f838047332a7c61988f6357339dee in / 
# Wed, 10 Apr 2024 01:50:59 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:43:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 05:43:57 GMT
ENV INFLUXDB_VERSION=1.10.5-c1.10.5
# Wed, 10 Apr 2024 05:44:12 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb*
# Wed, 10 Apr 2024 05:44:12 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 10 Apr 2024 05:44:12 GMT
EXPOSE 8091
# Wed, 10 Apr 2024 05:44:12 GMT
VOLUME [/var/lib/influxdb]
# Wed, 10 Apr 2024 05:44:12 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 10 Apr 2024 05:44:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 05:44:13 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:ac323bdaa10f869bd9e7adecd8f5326e44acc4c59168868108b1cdf3891089cc`  
		Last Modified: Wed, 10 Apr 2024 01:55:52 GMT  
		Size: 55.1 MB (55090264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84811b2a563b9003abbd1c06f6e45a857315b931855030bdd0443d13d950a996`  
		Last Modified: Wed, 10 Apr 2024 05:36:00 GMT  
		Size: 15.8 MB (15763518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f109c707be2928b7b5cb0f6cd61dba161e7b02c280e743ac20347edd14fd394e`  
		Last Modified: Wed, 10 Apr 2024 05:45:31 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:483a08364fbe0e0e9f7f8d7fa4088a69cc322ff49d455bb02f7476083f21e071`  
		Last Modified: Wed, 10 Apr 2024 05:46:29 GMT  
		Size: 20.4 MB (20376970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea0d33c965d33b5756192a1921456e7e8415ffdf2cc943befc139d8b86c6341`  
		Last Modified: Wed, 10 Apr 2024 05:46:26 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98aac2e9ac504acf9f3fd3fdd571f4c24ddd1c8b77d50d1584b4b56e00a28f2a`  
		Last Modified: Wed, 10 Apr 2024 05:46:26 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.10.5-meta-alpine`

```console
$ docker pull influxdb@sha256:47b8526c9b9e2b41bc77357a5969faea561a0f20f3b66aab1e0a920c42fb6143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.10.5-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:dcb846d06d314e43c18dbe62f4e03b49c0ed08c2e5f1cf2eb653ba8a4b0d7b44
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25194389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a536b3b0d15d5dfc12ab1cb129829b538b116fd18a531044aca7dacb7b6187d9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:20:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 07:54:19 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Sat, 16 Mar 2024 07:54:55 GMT
ENV INFLUXDB_VERSION=1.10.5-c1.10.5
# Sat, 16 Mar 2024 07:55:18 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 16 Mar 2024 07:55:18 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Sat, 16 Mar 2024 07:55:18 GMT
EXPOSE 8091
# Sat, 16 Mar 2024 07:55:18 GMT
VOLUME [/var/lib/influxdb]
# Sat, 16 Mar 2024 07:55:18 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Sat, 16 Mar 2024 07:55:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 07:55:19 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:485cfb0fb6cd4129a6e7d303f3ebec56b5c133689199b5426db52a97cdafd15a`  
		Last Modified: Sat, 16 Mar 2024 03:21:13 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36314c9e553b2628ec2b88878449957443671f3e9bdf1ac3142d78358c5c95cd`  
		Last Modified: Sat, 16 Mar 2024 07:56:23 GMT  
		Size: 1.5 MB (1470621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1f6ceb15b042d68232e0e6da8cbb800e744dfc1dc7c1d74fb0fb616dda3cb04`  
		Last Modified: Sat, 16 Mar 2024 07:57:17 GMT  
		Size: 20.3 MB (20343496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e643707bf15117d88879726bc8bfc26be16ac5037fa52ad62aff4dc3f7b7f2`  
		Last Modified: Sat, 16 Mar 2024 07:57:14 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d75f88729bfacec3b3ce39587d58bf11246ac55364c9e5370acddb319deb709`  
		Last Modified: Sat, 16 Mar 2024 07:57:14 GMT  
		Size: 372.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.11-data`

```console
$ docker pull influxdb@sha256:96639e470a3eb04bb0f13d9d2eb274dae3aab464554a92d4143ebf6aec17378a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.11-data` - linux; amd64

```console
$ docker pull influxdb@sha256:9ad72bb81d3a8b5edf36a5798f5caa3c5f82f7c2be20d9b9af8b6941e0c35ad4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 MB (115433622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:333d4b818e97d342d45e6f92595ad5351ecd0a7e1d3774656b11eccec16f13e3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:34 GMT
ADD file:ca6d1f0f80dd6c91b8ba1d1adf77d7af6d0e5f2f493a2858e384c11874314395 in / 
# Wed, 10 Apr 2024 01:50:35 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:24:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:44:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 05:44:20 GMT
ENV INFLUXDB_VERSION=1.11.5-c1.11.5
# Wed, 10 Apr 2024 05:44:23 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb*
# Wed, 10 Apr 2024 05:44:24 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 10 Apr 2024 05:44:24 GMT
EXPOSE 8086
# Wed, 10 Apr 2024 05:44:24 GMT
VOLUME [/var/lib/influxdb]
# Wed, 10 Apr 2024 05:44:24 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 10 Apr 2024 05:44:24 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 10 Apr 2024 05:44:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 05:44:24 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:609c73876867487da051ad470002217da69bb052e2538710ade0730d893ff51f`  
		Last Modified: Wed, 10 Apr 2024 01:55:11 GMT  
		Size: 49.6 MB (49560360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7247ea8d81e671d079d67f3a9909315ef4641b45db90d62a1b18e3430c1937d4`  
		Last Modified: Wed, 10 Apr 2024 05:34:49 GMT  
		Size: 24.0 MB (24046793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5625af29a1f0e4335c9d043d29228f4fec2382939e04b29f128d984c37d9ba82`  
		Last Modified: Wed, 10 Apr 2024 05:46:38 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51596ec548773e5e7915087379ab7315182cf0d5fbff199457aeebf9eeefc096`  
		Last Modified: Wed, 10 Apr 2024 05:46:44 GMT  
		Size: 41.8 MB (41822879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daadd3bb4af8c29ff4a4e84383d23bfc06a79a03a67f115765e91d662d255efd`  
		Last Modified: Wed, 10 Apr 2024 05:46:38 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab8abb817214fc64526537001ae5f4630630039a90702a272cdde0dd41b9c07`  
		Last Modified: Wed, 10 Apr 2024 05:46:38 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cfa2ec18d8f7729d2ce25cf69fc560af96759fa339e4f4c6fba5e14ed239782`  
		Last Modified: Wed, 10 Apr 2024 05:46:38 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.11-data-alpine`

```console
$ docker pull influxdb@sha256:8dda1e8551b294d545a03a9e70ba8a55674e253a1703402eefd0299148d124b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.11-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:50e87b56f3f0543e905ffc863135ad81e653cb14690f2c7439ccbc29107e0aa3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46588192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de595a73206133556cb4d9e13af63149481c4ee660dbaebe718a37a393a4401c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:20:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 07:55:25 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Sat, 16 Mar 2024 07:55:26 GMT
ENV INFLUXDB_VERSION=1.11.5-c1.11.5
# Sat, 16 Mar 2024 07:55:32 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 16 Mar 2024 07:55:32 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Sat, 16 Mar 2024 07:55:32 GMT
EXPOSE 8086
# Sat, 16 Mar 2024 07:55:32 GMT
VOLUME [/var/lib/influxdb]
# Sat, 16 Mar 2024 07:55:32 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Sat, 16 Mar 2024 07:55:32 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sat, 16 Mar 2024 07:55:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 07:55:33 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec84f8c4b4c91fcb32de58f4c3ad4f074277a222c69804bc60e3dc52fb9edb0`  
		Last Modified: Sat, 16 Mar 2024 03:21:48 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3adebce6b02445cbe2d9b92bb12b7aae314cb855f6a7015c3fab761d59f227d2`  
		Last Modified: Sat, 16 Mar 2024 07:57:25 GMT  
		Size: 1.4 MB (1405350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8150c06867b7013756ce6b5f9ad75397b3f73c0b5abbb74c841eead139b0857`  
		Last Modified: Sat, 16 Mar 2024 07:57:31 GMT  
		Size: 41.8 MB (41778218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe25992d57ea93c2fcf6be8c7a4ad471f1d10f48b5d588ad178be2782f881958`  
		Last Modified: Sat, 16 Mar 2024 07:57:25 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6077ab3a7bdf2f11fffd1a6d9083348eac956730f2dfd146c41ad146246483ac`  
		Last Modified: Sat, 16 Mar 2024 07:57:24 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c069a82a587b62511eb7b9fa735101b0e4791c49c4d1744bb4865a9f93ba218a`  
		Last Modified: Sat, 16 Mar 2024 07:57:25 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.11-meta`

```console
$ docker pull influxdb@sha256:3102564900517bd01eccb7cf13e95d5dec4690263c4df3bb097cdca5d7a912fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.11-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:8b976368aca9db677c1c1767f597a20cb311eae33d0365195465d1b6079426f5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (94003048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4463f0746bd153d861808564b3e7045b23bda541c995a4ea185072162e2592dc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:34 GMT
ADD file:ca6d1f0f80dd6c91b8ba1d1adf77d7af6d0e5f2f493a2858e384c11874314395 in / 
# Wed, 10 Apr 2024 01:50:35 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:24:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:44:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 05:44:20 GMT
ENV INFLUXDB_VERSION=1.11.5-c1.11.5
# Wed, 10 Apr 2024 05:44:34 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb*
# Wed, 10 Apr 2024 05:44:34 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 10 Apr 2024 05:44:34 GMT
EXPOSE 8091
# Wed, 10 Apr 2024 05:44:34 GMT
VOLUME [/var/lib/influxdb]
# Wed, 10 Apr 2024 05:44:34 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 10 Apr 2024 05:44:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 05:44:34 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:609c73876867487da051ad470002217da69bb052e2538710ade0730d893ff51f`  
		Last Modified: Wed, 10 Apr 2024 01:55:11 GMT  
		Size: 49.6 MB (49560360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7247ea8d81e671d079d67f3a9909315ef4641b45db90d62a1b18e3430c1937d4`  
		Last Modified: Wed, 10 Apr 2024 05:34:49 GMT  
		Size: 24.0 MB (24046793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5625af29a1f0e4335c9d043d29228f4fec2382939e04b29f128d984c37d9ba82`  
		Last Modified: Wed, 10 Apr 2024 05:46:38 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:253e1d7b3ec66b75df050caf7a78eec7f69fde3964f20f9723650bbd22651317`  
		Last Modified: Wed, 10 Apr 2024 05:46:55 GMT  
		Size: 20.4 MB (20393507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528e301eac3e5de5576bff242c8c2606bcc90ddc2589e7ee78d66a7e86e815c7`  
		Last Modified: Wed, 10 Apr 2024 05:46:52 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2a6ed08fff1fd6d70191daaec73b221ad14b77dedd5112e588faa6a97a2f41b`  
		Last Modified: Wed, 10 Apr 2024 05:46:52 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.11-meta-alpine`

```console
$ docker pull influxdb@sha256:1dbbdf507bbbdcb36fa36ca0d373e947b5beaa6f87bec60ca4fc8048c964e227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.11-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:319be42324443b67f14174f151cb5691ea78ced65a652653acc8889471e60449
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25168448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5051d38bb864ee6ba5145bc7c3c724e368ab9d09990a5814c00805aeffa229d3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:20:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 07:55:25 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Sat, 16 Mar 2024 07:55:26 GMT
ENV INFLUXDB_VERSION=1.11.5-c1.11.5
# Sat, 16 Mar 2024 07:55:43 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 16 Mar 2024 07:55:43 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Sat, 16 Mar 2024 07:55:43 GMT
EXPOSE 8091
# Sat, 16 Mar 2024 07:55:43 GMT
VOLUME [/var/lib/influxdb]
# Sat, 16 Mar 2024 07:55:43 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Sat, 16 Mar 2024 07:55:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 07:55:43 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec84f8c4b4c91fcb32de58f4c3ad4f074277a222c69804bc60e3dc52fb9edb0`  
		Last Modified: Sat, 16 Mar 2024 03:21:48 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3adebce6b02445cbe2d9b92bb12b7aae314cb855f6a7015c3fab761d59f227d2`  
		Last Modified: Sat, 16 Mar 2024 07:57:25 GMT  
		Size: 1.4 MB (1405350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:980c1cbd683caaba1b736d1d3b954c67110e531a957acaa1b04d2c30d40bbb3c`  
		Last Modified: Sat, 16 Mar 2024 07:57:43 GMT  
		Size: 20.4 MB (20359680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed5ae858bb68b0c03c6378581bb6a5212796bcc5f4a35dad4fc4119f3b7d413`  
		Last Modified: Sat, 16 Mar 2024 07:57:39 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbbe51116a269cbfebf6b6a7a6d24dafd26845f3211f6a22b988f2583016ba06`  
		Last Modified: Sat, 16 Mar 2024 07:57:39 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.11.5-data`

```console
$ docker pull influxdb@sha256:96639e470a3eb04bb0f13d9d2eb274dae3aab464554a92d4143ebf6aec17378a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.11.5-data` - linux; amd64

```console
$ docker pull influxdb@sha256:9ad72bb81d3a8b5edf36a5798f5caa3c5f82f7c2be20d9b9af8b6941e0c35ad4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 MB (115433622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:333d4b818e97d342d45e6f92595ad5351ecd0a7e1d3774656b11eccec16f13e3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:34 GMT
ADD file:ca6d1f0f80dd6c91b8ba1d1adf77d7af6d0e5f2f493a2858e384c11874314395 in / 
# Wed, 10 Apr 2024 01:50:35 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:24:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:44:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 05:44:20 GMT
ENV INFLUXDB_VERSION=1.11.5-c1.11.5
# Wed, 10 Apr 2024 05:44:23 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb*
# Wed, 10 Apr 2024 05:44:24 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 10 Apr 2024 05:44:24 GMT
EXPOSE 8086
# Wed, 10 Apr 2024 05:44:24 GMT
VOLUME [/var/lib/influxdb]
# Wed, 10 Apr 2024 05:44:24 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 10 Apr 2024 05:44:24 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 10 Apr 2024 05:44:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 05:44:24 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:609c73876867487da051ad470002217da69bb052e2538710ade0730d893ff51f`  
		Last Modified: Wed, 10 Apr 2024 01:55:11 GMT  
		Size: 49.6 MB (49560360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7247ea8d81e671d079d67f3a9909315ef4641b45db90d62a1b18e3430c1937d4`  
		Last Modified: Wed, 10 Apr 2024 05:34:49 GMT  
		Size: 24.0 MB (24046793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5625af29a1f0e4335c9d043d29228f4fec2382939e04b29f128d984c37d9ba82`  
		Last Modified: Wed, 10 Apr 2024 05:46:38 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51596ec548773e5e7915087379ab7315182cf0d5fbff199457aeebf9eeefc096`  
		Last Modified: Wed, 10 Apr 2024 05:46:44 GMT  
		Size: 41.8 MB (41822879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daadd3bb4af8c29ff4a4e84383d23bfc06a79a03a67f115765e91d662d255efd`  
		Last Modified: Wed, 10 Apr 2024 05:46:38 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab8abb817214fc64526537001ae5f4630630039a90702a272cdde0dd41b9c07`  
		Last Modified: Wed, 10 Apr 2024 05:46:38 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cfa2ec18d8f7729d2ce25cf69fc560af96759fa339e4f4c6fba5e14ed239782`  
		Last Modified: Wed, 10 Apr 2024 05:46:38 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.11.5-data-alpine`

```console
$ docker pull influxdb@sha256:8dda1e8551b294d545a03a9e70ba8a55674e253a1703402eefd0299148d124b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.11.5-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:50e87b56f3f0543e905ffc863135ad81e653cb14690f2c7439ccbc29107e0aa3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46588192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de595a73206133556cb4d9e13af63149481c4ee660dbaebe718a37a393a4401c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:20:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 07:55:25 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Sat, 16 Mar 2024 07:55:26 GMT
ENV INFLUXDB_VERSION=1.11.5-c1.11.5
# Sat, 16 Mar 2024 07:55:32 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 16 Mar 2024 07:55:32 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Sat, 16 Mar 2024 07:55:32 GMT
EXPOSE 8086
# Sat, 16 Mar 2024 07:55:32 GMT
VOLUME [/var/lib/influxdb]
# Sat, 16 Mar 2024 07:55:32 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Sat, 16 Mar 2024 07:55:32 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sat, 16 Mar 2024 07:55:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 07:55:33 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec84f8c4b4c91fcb32de58f4c3ad4f074277a222c69804bc60e3dc52fb9edb0`  
		Last Modified: Sat, 16 Mar 2024 03:21:48 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3adebce6b02445cbe2d9b92bb12b7aae314cb855f6a7015c3fab761d59f227d2`  
		Last Modified: Sat, 16 Mar 2024 07:57:25 GMT  
		Size: 1.4 MB (1405350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8150c06867b7013756ce6b5f9ad75397b3f73c0b5abbb74c841eead139b0857`  
		Last Modified: Sat, 16 Mar 2024 07:57:31 GMT  
		Size: 41.8 MB (41778218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe25992d57ea93c2fcf6be8c7a4ad471f1d10f48b5d588ad178be2782f881958`  
		Last Modified: Sat, 16 Mar 2024 07:57:25 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6077ab3a7bdf2f11fffd1a6d9083348eac956730f2dfd146c41ad146246483ac`  
		Last Modified: Sat, 16 Mar 2024 07:57:24 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c069a82a587b62511eb7b9fa735101b0e4791c49c4d1744bb4865a9f93ba218a`  
		Last Modified: Sat, 16 Mar 2024 07:57:25 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.11.5-meta`

```console
$ docker pull influxdb@sha256:3102564900517bd01eccb7cf13e95d5dec4690263c4df3bb097cdca5d7a912fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.11.5-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:8b976368aca9db677c1c1767f597a20cb311eae33d0365195465d1b6079426f5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (94003048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4463f0746bd153d861808564b3e7045b23bda541c995a4ea185072162e2592dc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:34 GMT
ADD file:ca6d1f0f80dd6c91b8ba1d1adf77d7af6d0e5f2f493a2858e384c11874314395 in / 
# Wed, 10 Apr 2024 01:50:35 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:24:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:44:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 05:44:20 GMT
ENV INFLUXDB_VERSION=1.11.5-c1.11.5
# Wed, 10 Apr 2024 05:44:34 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb*
# Wed, 10 Apr 2024 05:44:34 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 10 Apr 2024 05:44:34 GMT
EXPOSE 8091
# Wed, 10 Apr 2024 05:44:34 GMT
VOLUME [/var/lib/influxdb]
# Wed, 10 Apr 2024 05:44:34 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 10 Apr 2024 05:44:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 05:44:34 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:609c73876867487da051ad470002217da69bb052e2538710ade0730d893ff51f`  
		Last Modified: Wed, 10 Apr 2024 01:55:11 GMT  
		Size: 49.6 MB (49560360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7247ea8d81e671d079d67f3a9909315ef4641b45db90d62a1b18e3430c1937d4`  
		Last Modified: Wed, 10 Apr 2024 05:34:49 GMT  
		Size: 24.0 MB (24046793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5625af29a1f0e4335c9d043d29228f4fec2382939e04b29f128d984c37d9ba82`  
		Last Modified: Wed, 10 Apr 2024 05:46:38 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:253e1d7b3ec66b75df050caf7a78eec7f69fde3964f20f9723650bbd22651317`  
		Last Modified: Wed, 10 Apr 2024 05:46:55 GMT  
		Size: 20.4 MB (20393507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528e301eac3e5de5576bff242c8c2606bcc90ddc2589e7ee78d66a7e86e815c7`  
		Last Modified: Wed, 10 Apr 2024 05:46:52 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2a6ed08fff1fd6d70191daaec73b221ad14b77dedd5112e588faa6a97a2f41b`  
		Last Modified: Wed, 10 Apr 2024 05:46:52 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.11.5-meta-alpine`

```console
$ docker pull influxdb@sha256:1dbbdf507bbbdcb36fa36ca0d373e947b5beaa6f87bec60ca4fc8048c964e227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.11.5-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:319be42324443b67f14174f151cb5691ea78ced65a652653acc8889471e60449
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25168448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5051d38bb864ee6ba5145bc7c3c724e368ab9d09990a5814c00805aeffa229d3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:20:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 07:55:25 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Sat, 16 Mar 2024 07:55:26 GMT
ENV INFLUXDB_VERSION=1.11.5-c1.11.5
# Sat, 16 Mar 2024 07:55:43 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 16 Mar 2024 07:55:43 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Sat, 16 Mar 2024 07:55:43 GMT
EXPOSE 8091
# Sat, 16 Mar 2024 07:55:43 GMT
VOLUME [/var/lib/influxdb]
# Sat, 16 Mar 2024 07:55:43 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Sat, 16 Mar 2024 07:55:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 07:55:43 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec84f8c4b4c91fcb32de58f4c3ad4f074277a222c69804bc60e3dc52fb9edb0`  
		Last Modified: Sat, 16 Mar 2024 03:21:48 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3adebce6b02445cbe2d9b92bb12b7aae314cb855f6a7015c3fab761d59f227d2`  
		Last Modified: Sat, 16 Mar 2024 07:57:25 GMT  
		Size: 1.4 MB (1405350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:980c1cbd683caaba1b736d1d3b954c67110e531a957acaa1b04d2c30d40bbb3c`  
		Last Modified: Sat, 16 Mar 2024 07:57:43 GMT  
		Size: 20.4 MB (20359680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed5ae858bb68b0c03c6378581bb6a5212796bcc5f4a35dad4fc4119f3b7d413`  
		Last Modified: Sat, 16 Mar 2024 07:57:39 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbbe51116a269cbfebf6b6a7a6d24dafd26845f3211f6a22b988f2583016ba06`  
		Last Modified: Sat, 16 Mar 2024 07:57:39 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8`

```console
$ docker pull influxdb@sha256:8e3ed6d1759d62a63c185462f5f9c8e2aa45dfe3e3876ea0c2eeaa71e6b70a43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.8` - linux; amd64

```console
$ docker pull influxdb@sha256:a926322b479d834d3116ac42ed0628c3f0ef53c0d2602fabf05336a41569321b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125743092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d70d18a4f33c42288af45a24e650d937b965e046f24e9dceca9c2390051e86e2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:59 GMT
ADD file:8efdcc3201e79c8a09fc9c1ade08492ea33f838047332a7c61988f6357339dee in / 
# Wed, 10 Apr 2024 01:50:59 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:43:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 05:43:24 GMT
ENV INFLUXDB_VERSION=1.8.10
# Wed, 10 Apr 2024 05:43:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 10 Apr 2024 05:43:28 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 10 Apr 2024 05:43:28 GMT
EXPOSE 8086
# Wed, 10 Apr 2024 05:43:28 GMT
VOLUME [/var/lib/influxdb]
# Wed, 10 Apr 2024 05:43:28 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 10 Apr 2024 05:43:28 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 10 Apr 2024 05:43:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 05:43:28 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:ac323bdaa10f869bd9e7adecd8f5326e44acc4c59168868108b1cdf3891089cc`  
		Last Modified: Wed, 10 Apr 2024 01:55:52 GMT  
		Size: 55.1 MB (55090264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84811b2a563b9003abbd1c06f6e45a857315b931855030bdd0443d13d950a996`  
		Last Modified: Wed, 10 Apr 2024 05:36:00 GMT  
		Size: 15.8 MB (15763518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f109c707be2928b7b5cb0f6cd61dba161e7b02c280e743ac20347edd14fd394e`  
		Last Modified: Wed, 10 Apr 2024 05:45:31 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41b856fd29333e9775e0968595a670257bdb23daea8ed7d2c6d48c8a2e7389b`  
		Last Modified: Wed, 10 Apr 2024 05:45:38 GMT  
		Size: 54.9 MB (54885780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f2aa2c549d95442b82244af45cd8db303c94e58a51e1238e7222679e6270ef3`  
		Last Modified: Wed, 10 Apr 2024 05:45:31 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e266a884a8700ece065e589c01cc3bf276fa912f04d1f780de617e3143b23171`  
		Last Modified: Wed, 10 Apr 2024 05:45:31 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2bfc97b82b1cf4d472b29c2e91108b7c0bfe0c88d088940fb1be332f56d8dca`  
		Last Modified: Wed, 10 Apr 2024 05:45:31 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.8` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:ae070171d706cb16f4b851e6624d297008dcf82cfd4a3956a55e6cd6e3427851
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.7 MB (116742442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97c01227be24a8bf2b16b7db80eb43e0b27409040585c18198044f2a01ee8555`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 Apr 2024 00:58:28 GMT
ADD file:eb53aade3ed19f72413045948cad3084902fe630cc20789d2c2b5bc334679575 in / 
# Wed, 10 Apr 2024 00:58:29 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:45:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 21:06:14 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 21:06:14 GMT
ENV INFLUXDB_VERSION=1.8.10
# Wed, 10 Apr 2024 21:06:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 10 Apr 2024 21:06:26 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 10 Apr 2024 21:06:26 GMT
EXPOSE 8086
# Wed, 10 Apr 2024 21:06:27 GMT
VOLUME [/var/lib/influxdb]
# Wed, 10 Apr 2024 21:06:27 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 10 Apr 2024 21:06:27 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 10 Apr 2024 21:06:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 21:06:28 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:23ca580217f1a6b17dba868e7ec34ae7fff221e07640fca532510daca8ed46f6`  
		Last Modified: Wed, 10 Apr 2024 01:04:48 GMT  
		Size: 50.2 MB (50246481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab89b030e474718221560707f98fb967bd582bc0f355ca5caf120fc5f25b2d58`  
		Last Modified: Wed, 10 Apr 2024 07:01:21 GMT  
		Size: 14.9 MB (14879245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8581faf8837b4ad398511687d8ca4c40b9590252b90098261c40fbb443626a54`  
		Last Modified: Wed, 10 Apr 2024 21:06:38 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4744f648eabd6ca078cae01a921cdb3799d5881a2d8dcc076c25286e1ef7b5`  
		Last Modified: Wed, 10 Apr 2024 21:06:47 GMT  
		Size: 51.6 MB (51613198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5830402abef610b9dbfe09340d431af4928314a3d9705ab61dbaec7c05fd9f`  
		Last Modified: Wed, 10 Apr 2024 21:06:38 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c362e85330b52cf9e6b72906fd4a060dd783ae4981f1a84352aa04f480ecb208`  
		Last Modified: Wed, 10 Apr 2024 21:06:38 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd6a6a2db86b463da0298f8df050137c6469761fc2d94824b3ebb87632ba930`  
		Last Modified: Wed, 10 Apr 2024 21:06:38 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:2564555bb4bdb9d07b2193440f1c7828ad6df8b1dc41321fa49a3446f88ebc1c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120712017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a88ac64efff7c84146257ee127e3950cd60b90e99201598d0c3a9b19cfcf20e3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:30 GMT
ADD file:6fedb173fe261ff0e13b004ca692b7edcc74dcc3c4384fee092b96ef9508992c in / 
# Wed, 10 Apr 2024 00:40:30 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:23:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:20:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 05:20:54 GMT
ENV INFLUXDB_VERSION=1.8.10
# Wed, 10 Apr 2024 05:20:58 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 10 Apr 2024 05:20:59 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 10 Apr 2024 05:20:59 GMT
EXPOSE 8086
# Wed, 10 Apr 2024 05:20:59 GMT
VOLUME [/var/lib/influxdb]
# Wed, 10 Apr 2024 05:20:59 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 10 Apr 2024 05:20:59 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 10 Apr 2024 05:20:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 05:20:59 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:197947a07d5f6c6ff020ca65dcea4e52671f85f67bee1b59af46cb0dc36580d9`  
		Last Modified: Wed, 10 Apr 2024 00:44:24 GMT  
		Size: 53.7 MB (53729176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31e3f4a530684a6d51e431d14164bdf20c7ad515e8948ddbfbf5f9c2c3680727`  
		Last Modified: Wed, 10 Apr 2024 04:33:00 GMT  
		Size: 15.7 MB (15749239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034353b4e1c0683e2dbbfaa981486cb5ffedd63c76926171b8793086b3c474ce`  
		Last Modified: Wed, 10 Apr 2024 05:21:39 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6d86175ec1e13d7d2c8ff3119c6557c9ecbb92aac76942dd51b97dd050e7d3`  
		Last Modified: Wed, 10 Apr 2024 05:21:44 GMT  
		Size: 51.2 MB (51230069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ffa7ab6f17b9a4279bba63f7da7549e893d1793cdb4797a57ae94c9e63defe`  
		Last Modified: Wed, 10 Apr 2024 05:21:39 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29b742c72cf8b87f10cba675a671535a415d5ca4dd0a6f2766cd3bfd6ddc3da`  
		Last Modified: Wed, 10 Apr 2024 05:21:39 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e15f89da6453fb59f5dae3eb49705334ce3ad4c1d6e7afce1ffcee93ae49cf1`  
		Last Modified: Wed, 10 Apr 2024 05:21:39 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8-alpine`

```console
$ docker pull influxdb@sha256:35a6fbfa06e567a3e6bad48110c5b6e5a60e3e06217e25e84de2f0d304ce89c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.8-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:b3dae3f53ca5155a80a5b1b55f5b1c7c66c7ee7b90c58756bb10a3c91ac1ace0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59498805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49d0c13e4198b457bb20ecf1eb5dcb96177886e2bcbe08279a8c142a4b24f921`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:20:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 07:54:19 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Sat, 16 Mar 2024 07:54:19 GMT
ENV INFLUXDB_VERSION=1.8.10
# Sat, 16 Mar 2024 07:54:25 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     chmod +x /usr/src/influxdb-*/influx              /usr/src/influxdb-*/influx_inspect              /usr/src/influxdb-*/influx_stress              /usr/src/influxdb-*/influxd &&    mv /usr/src/influxdb-*/influx        /usr/src/influxdb-*/influx_inspect        /usr/src/influxdb-*/influx_stress         /usr/src/influxdb-*/influxd        /usr/bin/ &&    gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 16 Mar 2024 07:54:25 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Sat, 16 Mar 2024 07:54:25 GMT
EXPOSE 8086
# Sat, 16 Mar 2024 07:54:25 GMT
VOLUME [/var/lib/influxdb]
# Sat, 16 Mar 2024 07:54:25 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Sat, 16 Mar 2024 07:54:25 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sat, 16 Mar 2024 07:54:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 07:54:25 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:485cfb0fb6cd4129a6e7d303f3ebec56b5c133689199b5426db52a97cdafd15a`  
		Last Modified: Sat, 16 Mar 2024 03:21:13 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36314c9e553b2628ec2b88878449957443671f3e9bdf1ac3142d78358c5c95cd`  
		Last Modified: Sat, 16 Mar 2024 07:56:23 GMT  
		Size: 1.5 MB (1470621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3695e6f8e79fa8345388db6fb9b279920ee1d86af5f54ce41c44eb44746e9f1e`  
		Last Modified: Sat, 16 Mar 2024 07:56:28 GMT  
		Size: 54.6 MB (54646761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:947e49326b786316aa75a554f280409135ffaf8f21012dc770f6a889e177fbbc`  
		Last Modified: Sat, 16 Mar 2024 07:56:22 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72c2d3919dbeeb1810bd89689cb4f435ee953d24c272e5257be50f962d251b47`  
		Last Modified: Sat, 16 Mar 2024 07:56:22 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e1db648121d5a4aa218a118f81d5dbf6f3749ef2279f940e07ba9fa58394e1e`  
		Last Modified: Sat, 16 Mar 2024 07:56:22 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.10`

```console
$ docker pull influxdb@sha256:8e3ed6d1759d62a63c185462f5f9c8e2aa45dfe3e3876ea0c2eeaa71e6b70a43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.8.10` - linux; amd64

```console
$ docker pull influxdb@sha256:a926322b479d834d3116ac42ed0628c3f0ef53c0d2602fabf05336a41569321b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125743092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d70d18a4f33c42288af45a24e650d937b965e046f24e9dceca9c2390051e86e2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:59 GMT
ADD file:8efdcc3201e79c8a09fc9c1ade08492ea33f838047332a7c61988f6357339dee in / 
# Wed, 10 Apr 2024 01:50:59 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:43:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 05:43:24 GMT
ENV INFLUXDB_VERSION=1.8.10
# Wed, 10 Apr 2024 05:43:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 10 Apr 2024 05:43:28 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 10 Apr 2024 05:43:28 GMT
EXPOSE 8086
# Wed, 10 Apr 2024 05:43:28 GMT
VOLUME [/var/lib/influxdb]
# Wed, 10 Apr 2024 05:43:28 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 10 Apr 2024 05:43:28 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 10 Apr 2024 05:43:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 05:43:28 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:ac323bdaa10f869bd9e7adecd8f5326e44acc4c59168868108b1cdf3891089cc`  
		Last Modified: Wed, 10 Apr 2024 01:55:52 GMT  
		Size: 55.1 MB (55090264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84811b2a563b9003abbd1c06f6e45a857315b931855030bdd0443d13d950a996`  
		Last Modified: Wed, 10 Apr 2024 05:36:00 GMT  
		Size: 15.8 MB (15763518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f109c707be2928b7b5cb0f6cd61dba161e7b02c280e743ac20347edd14fd394e`  
		Last Modified: Wed, 10 Apr 2024 05:45:31 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41b856fd29333e9775e0968595a670257bdb23daea8ed7d2c6d48c8a2e7389b`  
		Last Modified: Wed, 10 Apr 2024 05:45:38 GMT  
		Size: 54.9 MB (54885780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f2aa2c549d95442b82244af45cd8db303c94e58a51e1238e7222679e6270ef3`  
		Last Modified: Wed, 10 Apr 2024 05:45:31 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e266a884a8700ece065e589c01cc3bf276fa912f04d1f780de617e3143b23171`  
		Last Modified: Wed, 10 Apr 2024 05:45:31 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2bfc97b82b1cf4d472b29c2e91108b7c0bfe0c88d088940fb1be332f56d8dca`  
		Last Modified: Wed, 10 Apr 2024 05:45:31 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.8.10` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:ae070171d706cb16f4b851e6624d297008dcf82cfd4a3956a55e6cd6e3427851
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.7 MB (116742442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97c01227be24a8bf2b16b7db80eb43e0b27409040585c18198044f2a01ee8555`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 Apr 2024 00:58:28 GMT
ADD file:eb53aade3ed19f72413045948cad3084902fe630cc20789d2c2b5bc334679575 in / 
# Wed, 10 Apr 2024 00:58:29 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:45:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 21:06:14 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 21:06:14 GMT
ENV INFLUXDB_VERSION=1.8.10
# Wed, 10 Apr 2024 21:06:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 10 Apr 2024 21:06:26 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 10 Apr 2024 21:06:26 GMT
EXPOSE 8086
# Wed, 10 Apr 2024 21:06:27 GMT
VOLUME [/var/lib/influxdb]
# Wed, 10 Apr 2024 21:06:27 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 10 Apr 2024 21:06:27 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 10 Apr 2024 21:06:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 21:06:28 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:23ca580217f1a6b17dba868e7ec34ae7fff221e07640fca532510daca8ed46f6`  
		Last Modified: Wed, 10 Apr 2024 01:04:48 GMT  
		Size: 50.2 MB (50246481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab89b030e474718221560707f98fb967bd582bc0f355ca5caf120fc5f25b2d58`  
		Last Modified: Wed, 10 Apr 2024 07:01:21 GMT  
		Size: 14.9 MB (14879245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8581faf8837b4ad398511687d8ca4c40b9590252b90098261c40fbb443626a54`  
		Last Modified: Wed, 10 Apr 2024 21:06:38 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4744f648eabd6ca078cae01a921cdb3799d5881a2d8dcc076c25286e1ef7b5`  
		Last Modified: Wed, 10 Apr 2024 21:06:47 GMT  
		Size: 51.6 MB (51613198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5830402abef610b9dbfe09340d431af4928314a3d9705ab61dbaec7c05fd9f`  
		Last Modified: Wed, 10 Apr 2024 21:06:38 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c362e85330b52cf9e6b72906fd4a060dd783ae4981f1a84352aa04f480ecb208`  
		Last Modified: Wed, 10 Apr 2024 21:06:38 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd6a6a2db86b463da0298f8df050137c6469761fc2d94824b3ebb87632ba930`  
		Last Modified: Wed, 10 Apr 2024 21:06:38 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.8.10` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:2564555bb4bdb9d07b2193440f1c7828ad6df8b1dc41321fa49a3446f88ebc1c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120712017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a88ac64efff7c84146257ee127e3950cd60b90e99201598d0c3a9b19cfcf20e3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:30 GMT
ADD file:6fedb173fe261ff0e13b004ca692b7edcc74dcc3c4384fee092b96ef9508992c in / 
# Wed, 10 Apr 2024 00:40:30 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:23:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:20:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 05:20:54 GMT
ENV INFLUXDB_VERSION=1.8.10
# Wed, 10 Apr 2024 05:20:58 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 10 Apr 2024 05:20:59 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 10 Apr 2024 05:20:59 GMT
EXPOSE 8086
# Wed, 10 Apr 2024 05:20:59 GMT
VOLUME [/var/lib/influxdb]
# Wed, 10 Apr 2024 05:20:59 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 10 Apr 2024 05:20:59 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 10 Apr 2024 05:20:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 05:20:59 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:197947a07d5f6c6ff020ca65dcea4e52671f85f67bee1b59af46cb0dc36580d9`  
		Last Modified: Wed, 10 Apr 2024 00:44:24 GMT  
		Size: 53.7 MB (53729176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31e3f4a530684a6d51e431d14164bdf20c7ad515e8948ddbfbf5f9c2c3680727`  
		Last Modified: Wed, 10 Apr 2024 04:33:00 GMT  
		Size: 15.7 MB (15749239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034353b4e1c0683e2dbbfaa981486cb5ffedd63c76926171b8793086b3c474ce`  
		Last Modified: Wed, 10 Apr 2024 05:21:39 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6d86175ec1e13d7d2c8ff3119c6557c9ecbb92aac76942dd51b97dd050e7d3`  
		Last Modified: Wed, 10 Apr 2024 05:21:44 GMT  
		Size: 51.2 MB (51230069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ffa7ab6f17b9a4279bba63f7da7549e893d1793cdb4797a57ae94c9e63defe`  
		Last Modified: Wed, 10 Apr 2024 05:21:39 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29b742c72cf8b87f10cba675a671535a415d5ca4dd0a6f2766cd3bfd6ddc3da`  
		Last Modified: Wed, 10 Apr 2024 05:21:39 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e15f89da6453fb59f5dae3eb49705334ce3ad4c1d6e7afce1ffcee93ae49cf1`  
		Last Modified: Wed, 10 Apr 2024 05:21:39 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.10-alpine`

```console
$ docker pull influxdb@sha256:35a6fbfa06e567a3e6bad48110c5b6e5a60e3e06217e25e84de2f0d304ce89c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.8.10-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:b3dae3f53ca5155a80a5b1b55f5b1c7c66c7ee7b90c58756bb10a3c91ac1ace0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59498805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49d0c13e4198b457bb20ecf1eb5dcb96177886e2bcbe08279a8c142a4b24f921`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:20:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 07:54:19 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Sat, 16 Mar 2024 07:54:19 GMT
ENV INFLUXDB_VERSION=1.8.10
# Sat, 16 Mar 2024 07:54:25 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     chmod +x /usr/src/influxdb-*/influx              /usr/src/influxdb-*/influx_inspect              /usr/src/influxdb-*/influx_stress              /usr/src/influxdb-*/influxd &&    mv /usr/src/influxdb-*/influx        /usr/src/influxdb-*/influx_inspect        /usr/src/influxdb-*/influx_stress         /usr/src/influxdb-*/influxd        /usr/bin/ &&    gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 16 Mar 2024 07:54:25 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Sat, 16 Mar 2024 07:54:25 GMT
EXPOSE 8086
# Sat, 16 Mar 2024 07:54:25 GMT
VOLUME [/var/lib/influxdb]
# Sat, 16 Mar 2024 07:54:25 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Sat, 16 Mar 2024 07:54:25 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sat, 16 Mar 2024 07:54:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 07:54:25 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:485cfb0fb6cd4129a6e7d303f3ebec56b5c133689199b5426db52a97cdafd15a`  
		Last Modified: Sat, 16 Mar 2024 03:21:13 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36314c9e553b2628ec2b88878449957443671f3e9bdf1ac3142d78358c5c95cd`  
		Last Modified: Sat, 16 Mar 2024 07:56:23 GMT  
		Size: 1.5 MB (1470621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3695e6f8e79fa8345388db6fb9b279920ee1d86af5f54ce41c44eb44746e9f1e`  
		Last Modified: Sat, 16 Mar 2024 07:56:28 GMT  
		Size: 54.6 MB (54646761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:947e49326b786316aa75a554f280409135ffaf8f21012dc770f6a889e177fbbc`  
		Last Modified: Sat, 16 Mar 2024 07:56:22 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72c2d3919dbeeb1810bd89689cb4f435ee953d24c272e5257be50f962d251b47`  
		Last Modified: Sat, 16 Mar 2024 07:56:22 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e1db648121d5a4aa218a118f81d5dbf6f3749ef2279f940e07ba9fa58394e1e`  
		Last Modified: Sat, 16 Mar 2024 07:56:22 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.9-data`

```console
$ docker pull influxdb@sha256:f870e7b28e0ec990a22e8c53511a772e55d472d76512c0d1cc4a4d6ae15190f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.9-data` - linux; amd64

```console
$ docker pull influxdb@sha256:9800a787c438068e8bda2a63aaaa3223d1d32fe132ce49867f86e5e064215d91
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104146525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b566e17a8eb949469484e4ff3708457d8f0eb2f8b352ff40a514ba9adfbabac7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:59 GMT
ADD file:8efdcc3201e79c8a09fc9c1ade08492ea33f838047332a7c61988f6357339dee in / 
# Wed, 10 Apr 2024 01:50:59 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:43:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 05:43:34 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Wed, 10 Apr 2024 05:43:39 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 10 Apr 2024 05:43:39 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 10 Apr 2024 05:43:39 GMT
EXPOSE 8086
# Wed, 10 Apr 2024 05:43:39 GMT
VOLUME [/var/lib/influxdb]
# Wed, 10 Apr 2024 05:43:39 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 10 Apr 2024 05:43:39 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 10 Apr 2024 05:43:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 05:43:39 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:ac323bdaa10f869bd9e7adecd8f5326e44acc4c59168868108b1cdf3891089cc`  
		Last Modified: Wed, 10 Apr 2024 01:55:52 GMT  
		Size: 55.1 MB (55090264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84811b2a563b9003abbd1c06f6e45a857315b931855030bdd0443d13d950a996`  
		Last Modified: Wed, 10 Apr 2024 05:36:00 GMT  
		Size: 15.8 MB (15763518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f109c707be2928b7b5cb0f6cd61dba161e7b02c280e743ac20347edd14fd394e`  
		Last Modified: Wed, 10 Apr 2024 05:45:31 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e570c31f81ca0a33137dfe1771734d8d4c41f68ee91b5f0ab1cd3353adac54bf`  
		Last Modified: Wed, 10 Apr 2024 05:45:51 GMT  
		Size: 33.3 MB (33289153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd737c65061fd7c25055c7bca5178b63c7d0b8ea1482f8f952a947831089a582`  
		Last Modified: Wed, 10 Apr 2024 05:45:46 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8632754fe334b4bfffdefdcc73e8cc6dda99f42eefc381024ed5f4b2f48be1d`  
		Last Modified: Wed, 10 Apr 2024 05:45:46 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:333d4b4f2faaf89ee4cbd9ae4054797c59ea231d67d5467e4d3c1bf75a1ed5c4`  
		Last Modified: Wed, 10 Apr 2024 05:45:46 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.9-data-alpine`

```console
$ docker pull influxdb@sha256:7c94a0af5d82253a99309e0cbe091abf4a2c6a4bf86ca271e4f6168f4700b42d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.9-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:aac116c90debde4959bae06ca07706b6b5ce42ca258149b9c1b0750c02aaaa1e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 MB (38100901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:798dee14f7dcec4e41fb27dc6b3dab5deb0593cb22f073d7657b48c02ec7e079`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:20:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 07:54:19 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Sat, 16 Mar 2024 07:54:31 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Sat, 16 Mar 2024 07:54:40 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/etc/influxdb/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 16 Mar 2024 07:54:40 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Sat, 16 Mar 2024 07:54:40 GMT
EXPOSE 8086
# Sat, 16 Mar 2024 07:54:40 GMT
VOLUME [/var/lib/influxdb]
# Sat, 16 Mar 2024 07:54:40 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Sat, 16 Mar 2024 07:54:40 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sat, 16 Mar 2024 07:54:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 07:54:40 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:485cfb0fb6cd4129a6e7d303f3ebec56b5c133689199b5426db52a97cdafd15a`  
		Last Modified: Sat, 16 Mar 2024 03:21:13 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36314c9e553b2628ec2b88878449957443671f3e9bdf1ac3142d78358c5c95cd`  
		Last Modified: Sat, 16 Mar 2024 07:56:23 GMT  
		Size: 1.5 MB (1470621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8b4a007cedf49ff0e2d1febe627ad5a0d624ffe86cb5ec97ec0197788e9b72`  
		Last Modified: Sat, 16 Mar 2024 07:56:42 GMT  
		Size: 33.2 MB (33248801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c18ae1d26cd3b6d0414fe09f77ac2b152805050dd057d821b1e8c01ddb6ddd`  
		Last Modified: Sat, 16 Mar 2024 07:56:37 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2943afa3668397f16bed3c1449761591da5ffe11cee00ba03745bdb15bb63aaa`  
		Last Modified: Sat, 16 Mar 2024 07:56:37 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fcd3e2bb6e292c72f4ab1a2535cfa19a9066b28e26b0c45c3c859bc66707dff`  
		Last Modified: Sat, 16 Mar 2024 07:56:37 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.9-meta`

```console
$ docker pull influxdb@sha256:6d33fdf5e63bda689a6a039aaa4aa2e952c3bbafddfd95be3c887af3a285a732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.9-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:17d10528dcca1092c36c262523dd416f9d0cb42678e919bb9b3e6df5f7cf95e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83626005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6280d16df10e3919b02bf183e6cc1a9d7b1e4a5f61e4d185efc3c7372ca569c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:59 GMT
ADD file:8efdcc3201e79c8a09fc9c1ade08492ea33f838047332a7c61988f6357339dee in / 
# Wed, 10 Apr 2024 01:50:59 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:43:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 05:43:34 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Wed, 10 Apr 2024 05:43:50 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 10 Apr 2024 05:43:50 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 10 Apr 2024 05:43:50 GMT
EXPOSE 8091
# Wed, 10 Apr 2024 05:43:50 GMT
VOLUME [/var/lib/influxdb]
# Wed, 10 Apr 2024 05:43:50 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 10 Apr 2024 05:43:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 05:43:51 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:ac323bdaa10f869bd9e7adecd8f5326e44acc4c59168868108b1cdf3891089cc`  
		Last Modified: Wed, 10 Apr 2024 01:55:52 GMT  
		Size: 55.1 MB (55090264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84811b2a563b9003abbd1c06f6e45a857315b931855030bdd0443d13d950a996`  
		Last Modified: Wed, 10 Apr 2024 05:36:00 GMT  
		Size: 15.8 MB (15763518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f109c707be2928b7b5cb0f6cd61dba161e7b02c280e743ac20347edd14fd394e`  
		Last Modified: Wed, 10 Apr 2024 05:45:31 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac47e5c33192a49f9e11c79900a38156265be261819d35566248611e7eb4525`  
		Last Modified: Wed, 10 Apr 2024 05:46:02 GMT  
		Size: 12.8 MB (12769838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c88903556c27c8fe6abfa57fa7fdaa4982db86de0d22039caab874d928317a0`  
		Last Modified: Wed, 10 Apr 2024 05:46:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3b43975079472149d7236f7e35616fcf3dbb35edb3de594db0a5502b5984df`  
		Last Modified: Wed, 10 Apr 2024 05:46:00 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.9-meta-alpine`

```console
$ docker pull influxdb@sha256:bce75e4d0c04f7b140aec1ee4392f58ea3c79a2ff5a57ecc2f2e9b07e492674b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.9-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:a6e42fbb0ca38ec7b673fbc4cb0fc6251d04d6616a7500748b33f8b5f503500e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17585192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72df76a1b29a32b3f4702fcd36c4574f2f5783ff0086b6339a837e057625ff23`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:20:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 07:54:19 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Sat, 16 Mar 2024 07:54:31 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Sat, 16 Mar 2024 07:54:50 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/etc/influxdb/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 16 Mar 2024 07:54:50 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Sat, 16 Mar 2024 07:54:50 GMT
EXPOSE 8091
# Sat, 16 Mar 2024 07:54:50 GMT
VOLUME [/var/lib/influxdb]
# Sat, 16 Mar 2024 07:54:50 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Sat, 16 Mar 2024 07:54:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 07:54:50 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:485cfb0fb6cd4129a6e7d303f3ebec56b5c133689199b5426db52a97cdafd15a`  
		Last Modified: Sat, 16 Mar 2024 03:21:13 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36314c9e553b2628ec2b88878449957443671f3e9bdf1ac3142d78358c5c95cd`  
		Last Modified: Sat, 16 Mar 2024 07:56:23 GMT  
		Size: 1.5 MB (1470621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4da313b734dfa276796b0ccc90b67803a78d5ac4dbf82cde41f63c28a88f6291`  
		Last Modified: Sat, 16 Mar 2024 07:56:52 GMT  
		Size: 12.7 MB (12734300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce38657e820007e6ab0a3dec05e48ba794e7fcaa5c23e334728afa399457f55`  
		Last Modified: Sat, 16 Mar 2024 07:56:50 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b3613edf4bb5e12942718e5a08b8f1990e95c01334aa5a93c057d7e1c01325`  
		Last Modified: Sat, 16 Mar 2024 07:56:50 GMT  
		Size: 372.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.9.13-data`

```console
$ docker pull influxdb@sha256:f870e7b28e0ec990a22e8c53511a772e55d472d76512c0d1cc4a4d6ae15190f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.9.13-data` - linux; amd64

```console
$ docker pull influxdb@sha256:9800a787c438068e8bda2a63aaaa3223d1d32fe132ce49867f86e5e064215d91
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104146525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b566e17a8eb949469484e4ff3708457d8f0eb2f8b352ff40a514ba9adfbabac7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:59 GMT
ADD file:8efdcc3201e79c8a09fc9c1ade08492ea33f838047332a7c61988f6357339dee in / 
# Wed, 10 Apr 2024 01:50:59 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:43:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 05:43:34 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Wed, 10 Apr 2024 05:43:39 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 10 Apr 2024 05:43:39 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 10 Apr 2024 05:43:39 GMT
EXPOSE 8086
# Wed, 10 Apr 2024 05:43:39 GMT
VOLUME [/var/lib/influxdb]
# Wed, 10 Apr 2024 05:43:39 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 10 Apr 2024 05:43:39 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 10 Apr 2024 05:43:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 05:43:39 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:ac323bdaa10f869bd9e7adecd8f5326e44acc4c59168868108b1cdf3891089cc`  
		Last Modified: Wed, 10 Apr 2024 01:55:52 GMT  
		Size: 55.1 MB (55090264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84811b2a563b9003abbd1c06f6e45a857315b931855030bdd0443d13d950a996`  
		Last Modified: Wed, 10 Apr 2024 05:36:00 GMT  
		Size: 15.8 MB (15763518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f109c707be2928b7b5cb0f6cd61dba161e7b02c280e743ac20347edd14fd394e`  
		Last Modified: Wed, 10 Apr 2024 05:45:31 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e570c31f81ca0a33137dfe1771734d8d4c41f68ee91b5f0ab1cd3353adac54bf`  
		Last Modified: Wed, 10 Apr 2024 05:45:51 GMT  
		Size: 33.3 MB (33289153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd737c65061fd7c25055c7bca5178b63c7d0b8ea1482f8f952a947831089a582`  
		Last Modified: Wed, 10 Apr 2024 05:45:46 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8632754fe334b4bfffdefdcc73e8cc6dda99f42eefc381024ed5f4b2f48be1d`  
		Last Modified: Wed, 10 Apr 2024 05:45:46 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:333d4b4f2faaf89ee4cbd9ae4054797c59ea231d67d5467e4d3c1bf75a1ed5c4`  
		Last Modified: Wed, 10 Apr 2024 05:45:46 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.9.13-data-alpine`

```console
$ docker pull influxdb@sha256:7c94a0af5d82253a99309e0cbe091abf4a2c6a4bf86ca271e4f6168f4700b42d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.9.13-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:aac116c90debde4959bae06ca07706b6b5ce42ca258149b9c1b0750c02aaaa1e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 MB (38100901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:798dee14f7dcec4e41fb27dc6b3dab5deb0593cb22f073d7657b48c02ec7e079`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:20:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 07:54:19 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Sat, 16 Mar 2024 07:54:31 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Sat, 16 Mar 2024 07:54:40 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/etc/influxdb/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 16 Mar 2024 07:54:40 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Sat, 16 Mar 2024 07:54:40 GMT
EXPOSE 8086
# Sat, 16 Mar 2024 07:54:40 GMT
VOLUME [/var/lib/influxdb]
# Sat, 16 Mar 2024 07:54:40 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Sat, 16 Mar 2024 07:54:40 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sat, 16 Mar 2024 07:54:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 07:54:40 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:485cfb0fb6cd4129a6e7d303f3ebec56b5c133689199b5426db52a97cdafd15a`  
		Last Modified: Sat, 16 Mar 2024 03:21:13 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36314c9e553b2628ec2b88878449957443671f3e9bdf1ac3142d78358c5c95cd`  
		Last Modified: Sat, 16 Mar 2024 07:56:23 GMT  
		Size: 1.5 MB (1470621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8b4a007cedf49ff0e2d1febe627ad5a0d624ffe86cb5ec97ec0197788e9b72`  
		Last Modified: Sat, 16 Mar 2024 07:56:42 GMT  
		Size: 33.2 MB (33248801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c18ae1d26cd3b6d0414fe09f77ac2b152805050dd057d821b1e8c01ddb6ddd`  
		Last Modified: Sat, 16 Mar 2024 07:56:37 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2943afa3668397f16bed3c1449761591da5ffe11cee00ba03745bdb15bb63aaa`  
		Last Modified: Sat, 16 Mar 2024 07:56:37 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fcd3e2bb6e292c72f4ab1a2535cfa19a9066b28e26b0c45c3c859bc66707dff`  
		Last Modified: Sat, 16 Mar 2024 07:56:37 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.9.13-meta`

```console
$ docker pull influxdb@sha256:6d33fdf5e63bda689a6a039aaa4aa2e952c3bbafddfd95be3c887af3a285a732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.9.13-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:17d10528dcca1092c36c262523dd416f9d0cb42678e919bb9b3e6df5f7cf95e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83626005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6280d16df10e3919b02bf183e6cc1a9d7b1e4a5f61e4d185efc3c7372ca569c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:59 GMT
ADD file:8efdcc3201e79c8a09fc9c1ade08492ea33f838047332a7c61988f6357339dee in / 
# Wed, 10 Apr 2024 01:50:59 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:43:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 05:43:34 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Wed, 10 Apr 2024 05:43:50 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 10 Apr 2024 05:43:50 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 10 Apr 2024 05:43:50 GMT
EXPOSE 8091
# Wed, 10 Apr 2024 05:43:50 GMT
VOLUME [/var/lib/influxdb]
# Wed, 10 Apr 2024 05:43:50 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 10 Apr 2024 05:43:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 05:43:51 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:ac323bdaa10f869bd9e7adecd8f5326e44acc4c59168868108b1cdf3891089cc`  
		Last Modified: Wed, 10 Apr 2024 01:55:52 GMT  
		Size: 55.1 MB (55090264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84811b2a563b9003abbd1c06f6e45a857315b931855030bdd0443d13d950a996`  
		Last Modified: Wed, 10 Apr 2024 05:36:00 GMT  
		Size: 15.8 MB (15763518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f109c707be2928b7b5cb0f6cd61dba161e7b02c280e743ac20347edd14fd394e`  
		Last Modified: Wed, 10 Apr 2024 05:45:31 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac47e5c33192a49f9e11c79900a38156265be261819d35566248611e7eb4525`  
		Last Modified: Wed, 10 Apr 2024 05:46:02 GMT  
		Size: 12.8 MB (12769838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c88903556c27c8fe6abfa57fa7fdaa4982db86de0d22039caab874d928317a0`  
		Last Modified: Wed, 10 Apr 2024 05:46:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3b43975079472149d7236f7e35616fcf3dbb35edb3de594db0a5502b5984df`  
		Last Modified: Wed, 10 Apr 2024 05:46:00 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.9.13-meta-alpine`

```console
$ docker pull influxdb@sha256:bce75e4d0c04f7b140aec1ee4392f58ea3c79a2ff5a57ecc2f2e9b07e492674b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.9.13-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:a6e42fbb0ca38ec7b673fbc4cb0fc6251d04d6616a7500748b33f8b5f503500e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17585192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72df76a1b29a32b3f4702fcd36c4574f2f5783ff0086b6339a837e057625ff23`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:20:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 07:54:19 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Sat, 16 Mar 2024 07:54:31 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Sat, 16 Mar 2024 07:54:50 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/etc/influxdb/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 16 Mar 2024 07:54:50 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Sat, 16 Mar 2024 07:54:50 GMT
EXPOSE 8091
# Sat, 16 Mar 2024 07:54:50 GMT
VOLUME [/var/lib/influxdb]
# Sat, 16 Mar 2024 07:54:50 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Sat, 16 Mar 2024 07:54:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 07:54:50 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:485cfb0fb6cd4129a6e7d303f3ebec56b5c133689199b5426db52a97cdafd15a`  
		Last Modified: Sat, 16 Mar 2024 03:21:13 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36314c9e553b2628ec2b88878449957443671f3e9bdf1ac3142d78358c5c95cd`  
		Last Modified: Sat, 16 Mar 2024 07:56:23 GMT  
		Size: 1.5 MB (1470621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4da313b734dfa276796b0ccc90b67803a78d5ac4dbf82cde41f63c28a88f6291`  
		Last Modified: Sat, 16 Mar 2024 07:56:52 GMT  
		Size: 12.7 MB (12734300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce38657e820007e6ab0a3dec05e48ba794e7fcaa5c23e334728afa399457f55`  
		Last Modified: Sat, 16 Mar 2024 07:56:50 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b3613edf4bb5e12942718e5a08b8f1990e95c01334aa5a93c057d7e1c01325`  
		Last Modified: Sat, 16 Mar 2024 07:56:50 GMT  
		Size: 372.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2`

```console
$ docker pull influxdb@sha256:766904dcef641fa1491750b7b3e0dd948b30417f7ef0ac4d3f1d6ffed52a1fa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2` - linux; amd64

```console
$ docker pull influxdb@sha256:a79377dc0ac143f5ecf2ce889e090bff468c324212874d4d5c7a811c8fb5b9bb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164685785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69e1e1673bcf2becedda8a32a5b3c2baa87b68c06d2f310a7ce5d514fbf17fb5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:48 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Wed, 10 Apr 2024 01:50:48 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:44:50 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:44:51 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version
# Wed, 10 Apr 2024 05:44:52 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb
# Wed, 10 Apr 2024 05:44:52 GMT
ENV GOSU_VER=1.16
# Wed, 10 Apr 2024 05:44:55 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true
# Wed, 10 Apr 2024 05:44:55 GMT
ENV INFLUXDB_VERSION=2.7.5
# Wed, 10 Apr 2024 05:44:59 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version
# Wed, 10 Apr 2024 05:45:00 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Wed, 10 Apr 2024 05:45:02 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version
# Wed, 10 Apr 2024 05:45:02 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 10 Apr 2024 05:45:02 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 10 Apr 2024 05:45:02 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 10 Apr 2024 05:45:03 GMT
COPY file:b5520696339eadb7386055c1dc9487351aa145a79b0cf206d8b1a79699c4a7f1 in /entrypoint.sh 
# Wed, 10 Apr 2024 05:45:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 05:45:03 GMT
CMD ["influxd"]
# Wed, 10 Apr 2024 05:45:03 GMT
EXPOSE 8086
# Wed, 10 Apr 2024 05:45:03 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 10 Apr 2024 05:45:03 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 10 Apr 2024 05:45:03 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 10 Apr 2024 05:45:03 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9294b900aa832728712196b5b6ef7b95954cbd7e6ac2d2c3840babb4128647c9`  
		Last Modified: Wed, 10 Apr 2024 05:47:09 GMT  
		Size: 9.8 MB (9784694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:425f098c3e26f8250bb21e082e37566627a939347a6d788cd64bf327955c22e9`  
		Last Modified: Wed, 10 Apr 2024 05:47:06 GMT  
		Size: 5.8 MB (5820944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80ba552c178797635fea84bd0613688f23b019299cfd6c7c94e1fbfdf1f819c`  
		Last Modified: Wed, 10 Apr 2024 05:47:06 GMT  
		Size: 3.3 KB (3280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2f8eb3058c2906e30b0f6dcc625636f4072aba364303a4ffb5cc9188ca4103c`  
		Last Modified: Wed, 10 Apr 2024 05:47:06 GMT  
		Size: 1.0 MB (1006415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed7e751eeae0842d327bdd471ebb9980742bf95e5a8e651fee26e09c2c90bfc`  
		Last Modified: Wed, 10 Apr 2024 05:47:14 GMT  
		Size: 95.8 MB (95803925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded3ff1728a91eb77cb93172de6d0534f28d609cf13acb2f0881120e9e61815c`  
		Last Modified: Wed, 10 Apr 2024 05:47:06 GMT  
		Size: 23.1 MB (23128349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2ff3b182a0b730c10e86ba4322e8dcd3756de9a5422a8b827631bc4f55bd6e8`  
		Last Modified: Wed, 10 Apr 2024 05:47:04 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acb3ba01d573f786db866b75cb9e9ba38dffcbc9425ea0c64d02756f6588e822`  
		Last Modified: Wed, 10 Apr 2024 05:47:04 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0aed24831c353f63d0b8cb89672c273f9b59204f7f732778f8e01f49745dfa2`  
		Last Modified: Wed, 10 Apr 2024 05:47:04 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:b7fbcc20cf648a208b1971ae25ee08f34546e1d72ab9410415527623d662d884
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.9 MB (158902762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01a617cea425cf53790f5482a8378c200944e1b6609e1e1d7a850d6b5b1305b0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:23 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Wed, 10 Apr 2024 00:40:23 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:21:09 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:21:10 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version
# Wed, 10 Apr 2024 05:21:10 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb
# Wed, 10 Apr 2024 05:21:10 GMT
ENV GOSU_VER=1.16
# Wed, 10 Apr 2024 05:21:13 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true
# Wed, 10 Apr 2024 05:21:13 GMT
ENV INFLUXDB_VERSION=2.7.5
# Wed, 10 Apr 2024 05:21:19 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version
# Wed, 10 Apr 2024 05:21:21 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Wed, 10 Apr 2024 05:21:23 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version
# Wed, 10 Apr 2024 05:21:24 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 10 Apr 2024 05:21:24 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 10 Apr 2024 05:21:24 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 10 Apr 2024 05:21:24 GMT
COPY file:b5520696339eadb7386055c1dc9487351aa145a79b0cf206d8b1a79699c4a7f1 in /entrypoint.sh 
# Wed, 10 Apr 2024 05:21:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 05:21:24 GMT
CMD ["influxd"]
# Wed, 10 Apr 2024 05:21:24 GMT
EXPOSE 8086
# Wed, 10 Apr 2024 05:21:24 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 10 Apr 2024 05:21:24 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 10 Apr 2024 05:21:24 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 10 Apr 2024 05:21:25 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab984742598cff95bd5de2e52df20eeabf05fccfeaa8a235da31e0e29ac482b`  
		Last Modified: Wed, 10 Apr 2024 05:21:57 GMT  
		Size: 9.6 MB (9581645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ccb29a42d38c08a905851fc53e23904361f52e5d3848e2d7b42f371dcbb38d`  
		Last Modified: Wed, 10 Apr 2024 05:21:55 GMT  
		Size: 5.5 MB (5463799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f786470e92bb4dba4737427552f576121bd301af37d785393afb208e1d59045`  
		Last Modified: Wed, 10 Apr 2024 05:21:54 GMT  
		Size: 3.3 KB (3279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:223efb50d26dd6bedd713da9b618cc0171c3f0d0a532f27d53c069ddbea9140f`  
		Last Modified: Wed, 10 Apr 2024 05:21:54 GMT  
		Size: 936.1 KB (936119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc5b2adfe6d39b3ffe0284a7de5689494803b1021507fd0d486ce640157cb18e`  
		Last Modified: Wed, 10 Apr 2024 05:21:59 GMT  
		Size: 92.1 MB (92086343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:633c7190aa2688c173444ae72db53d0d121b37bbe8fd5304857e56119ef56370`  
		Last Modified: Wed, 10 Apr 2024 05:21:54 GMT  
		Size: 21.7 MB (21662598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a6919049ad8d79ca20911a1a23495e0c8e54273789911c1ffd65fb2d64992f9`  
		Last Modified: Wed, 10 Apr 2024 05:21:52 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:256ee5f12ab78fa725e633a85c6a3cd1c60f643822d0a28a2ec92c1fa5a67e3a`  
		Last Modified: Wed, 10 Apr 2024 05:21:52 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05766916b3e30a9771ecbec56e08d9b650d23f91617156cd17c2e5073bc6de4d`  
		Last Modified: Wed, 10 Apr 2024 05:21:52 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2-alpine`

```console
$ docker pull influxdb@sha256:fffdcab19393a354155d33f2eec1fca1e35c70989f6a804ecc9fa66e4919cfe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:44692a6cbbcd59bfedd97d293277985e6ce5f83706468905ab47738d539ef7d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.2 MB (89169146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db93938edb34f78ae0e3a78d4bbdcd2305c248822562c75676414d3b92ec3ff6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:20:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 07:55:50 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates
# Sat, 16 Mar 2024 07:55:52 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version
# Sat, 16 Mar 2024 07:55:52 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Sat, 16 Mar 2024 07:55:52 GMT
ENV INFLUXDB_VERSION=2.7.5
# Sat, 16 Mar 2024 07:55:56 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version
# Sat, 16 Mar 2024 07:55:56 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Sat, 16 Mar 2024 07:55:59 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version
# Sat, 16 Mar 2024 07:55:59 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Sat, 16 Mar 2024 07:55:59 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Sat, 16 Mar 2024 07:55:59 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Sat, 16 Mar 2024 07:56:00 GMT
COPY file:6341d1dd8e0763e797b79985007acd07a4686ed831d55018f6e390823bad9d07 in /entrypoint.sh 
# Sat, 16 Mar 2024 07:56:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 07:56:00 GMT
CMD ["influxd"]
# Sat, 16 Mar 2024 07:56:00 GMT
EXPOSE 8086
# Sat, 16 Mar 2024 07:56:00 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Sat, 16 Mar 2024 07:56:00 GMT
ENV INFLUXD_INIT_PORT=9999
# Sat, 16 Mar 2024 07:56:00 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Sat, 16 Mar 2024 07:56:00 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec84f8c4b4c91fcb32de58f4c3ad4f074277a222c69804bc60e3dc52fb9edb0`  
		Last Modified: Sat, 16 Mar 2024 03:21:48 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2c04cf0ad6cd12dd58027cb82ab7cd473cbaafb98a89b6c54de66d6a4d8ed83`  
		Last Modified: Sat, 16 Mar 2024 07:57:54 GMT  
		Size: 8.9 MB (8912683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca16da08321a8772547dcf8e6665bfef94faaba388f795fd2483d67d82020a82`  
		Last Modified: Sat, 16 Mar 2024 07:57:54 GMT  
		Size: 5.8 MB (5820944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52968b0e54d2578c678da2760200217bb58d6de4a8ca283e6265d398a6898cf2`  
		Last Modified: Sat, 16 Mar 2024 07:57:53 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fae947c895929bdc7a2e45255709f2a31d1204489a3cd9d8816f8edd2c629b17`  
		Last Modified: Sat, 16 Mar 2024 07:57:56 GMT  
		Size: 47.9 MB (47896252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6fec1079edb744dadbb8b277f72e112a90417f8c91d02cb266f3d9764d2803`  
		Last Modified: Sat, 16 Mar 2024 07:57:54 GMT  
		Size: 23.1 MB (23128349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eefcf12f64fd7d55edf131d783cf222248f980fd54d8935b93f6affef9f0023`  
		Last Modified: Sat, 16 Mar 2024 07:57:51 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4f9db83590fc9950a5c5515e90fd63198ce04a7d170f6cc5f2bbbe8a97881b`  
		Last Modified: Sat, 16 Mar 2024 07:57:51 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64dd05fe3732785c572ca2bd7c0424036b824d59e1e5a8b02d54a908dafb356e`  
		Last Modified: Sat, 16 Mar 2024 07:57:51 GMT  
		Size: 6.3 KB (6283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:6c86e02bad991301d86f7e65160783891fc0c4895a6e3a2dea7e9b1a262a7d70
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.5 MB (85493150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe6b76c75225ea11626f9d4e0471e2ea3d9e1467f8900b36101cca7931629bd5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:39:20 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 02:39:22 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates
# Sat, 16 Mar 2024 02:39:23 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version
# Sat, 16 Mar 2024 02:39:24 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Sat, 16 Mar 2024 02:39:24 GMT
ENV INFLUXDB_VERSION=2.7.5
# Sat, 16 Mar 2024 02:39:27 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version
# Sat, 16 Mar 2024 02:39:27 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Sat, 16 Mar 2024 02:39:31 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version
# Sat, 16 Mar 2024 02:39:31 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Sat, 16 Mar 2024 02:39:31 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Sat, 16 Mar 2024 02:39:31 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Sat, 16 Mar 2024 02:39:31 GMT
COPY file:6341d1dd8e0763e797b79985007acd07a4686ed831d55018f6e390823bad9d07 in /entrypoint.sh 
# Sat, 16 Mar 2024 02:39:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 02:39:32 GMT
CMD ["influxd"]
# Sat, 16 Mar 2024 02:39:32 GMT
EXPOSE 8086
# Sat, 16 Mar 2024 02:39:32 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Sat, 16 Mar 2024 02:39:32 GMT
ENV INFLUXD_INIT_PORT=9999
# Sat, 16 Mar 2024 02:39:32 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Sat, 16 Mar 2024 02:39:32 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1132aa3c0a1481b1692e9b990f21c14f20ca44dcb2da0b19d2ad1b1da1aa45`  
		Last Modified: Sat, 16 Mar 2024 02:39:49 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de22938878825528f4eae2fc8baa8a5204e8ed38b4707f471dc5ec6db9dd2ac`  
		Last Modified: Sat, 16 Mar 2024 02:39:48 GMT  
		Size: 9.0 MB (8985806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c0e99e68893411c24682e55031bc9aac5a3262516395475ba13b6e8458440a`  
		Last Modified: Sat, 16 Mar 2024 02:39:48 GMT  
		Size: 5.5 MB (5463807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be6479785d41c1030f1af86ff3c17c5379b78f22493b8b30e5f77d9384e6e293`  
		Last Modified: Sat, 16 Mar 2024 02:39:47 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae3cc6f92445b13786f5da7acbaa0b5021965c810e597de4e5a2828c99098576`  
		Last Modified: Sat, 16 Mar 2024 02:39:49 GMT  
		Size: 46.0 MB (46039199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd569f416b8d58dd93eb8408a9a0e5eef5b150f59ff7ec5a730074d996fd1f87`  
		Last Modified: Sat, 16 Mar 2024 02:39:47 GMT  
		Size: 21.7 MB (21662606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa4219aea43efd5b66769a8567a98f437c694c2605e62d10b63a80d30a12622`  
		Last Modified: Sat, 16 Mar 2024 02:39:45 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb7152cc70b2894f041312ecf2f225755aca678334a506ae1a5269e7b962483`  
		Last Modified: Sat, 16 Mar 2024 02:39:45 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a3d84bef4bb47c4a25d86a8602ae3b658a0f0e169f49a502032bb6885761c7`  
		Last Modified: Sat, 16 Mar 2024 02:39:45 GMT  
		Size: 6.3 KB (6283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.7`

```console
$ docker pull influxdb@sha256:766904dcef641fa1491750b7b3e0dd948b30417f7ef0ac4d3f1d6ffed52a1fa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.7` - linux; amd64

```console
$ docker pull influxdb@sha256:a79377dc0ac143f5ecf2ce889e090bff468c324212874d4d5c7a811c8fb5b9bb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164685785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69e1e1673bcf2becedda8a32a5b3c2baa87b68c06d2f310a7ce5d514fbf17fb5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:48 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Wed, 10 Apr 2024 01:50:48 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:44:50 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:44:51 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version
# Wed, 10 Apr 2024 05:44:52 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb
# Wed, 10 Apr 2024 05:44:52 GMT
ENV GOSU_VER=1.16
# Wed, 10 Apr 2024 05:44:55 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true
# Wed, 10 Apr 2024 05:44:55 GMT
ENV INFLUXDB_VERSION=2.7.5
# Wed, 10 Apr 2024 05:44:59 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version
# Wed, 10 Apr 2024 05:45:00 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Wed, 10 Apr 2024 05:45:02 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version
# Wed, 10 Apr 2024 05:45:02 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 10 Apr 2024 05:45:02 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 10 Apr 2024 05:45:02 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 10 Apr 2024 05:45:03 GMT
COPY file:b5520696339eadb7386055c1dc9487351aa145a79b0cf206d8b1a79699c4a7f1 in /entrypoint.sh 
# Wed, 10 Apr 2024 05:45:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 05:45:03 GMT
CMD ["influxd"]
# Wed, 10 Apr 2024 05:45:03 GMT
EXPOSE 8086
# Wed, 10 Apr 2024 05:45:03 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 10 Apr 2024 05:45:03 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 10 Apr 2024 05:45:03 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 10 Apr 2024 05:45:03 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9294b900aa832728712196b5b6ef7b95954cbd7e6ac2d2c3840babb4128647c9`  
		Last Modified: Wed, 10 Apr 2024 05:47:09 GMT  
		Size: 9.8 MB (9784694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:425f098c3e26f8250bb21e082e37566627a939347a6d788cd64bf327955c22e9`  
		Last Modified: Wed, 10 Apr 2024 05:47:06 GMT  
		Size: 5.8 MB (5820944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80ba552c178797635fea84bd0613688f23b019299cfd6c7c94e1fbfdf1f819c`  
		Last Modified: Wed, 10 Apr 2024 05:47:06 GMT  
		Size: 3.3 KB (3280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2f8eb3058c2906e30b0f6dcc625636f4072aba364303a4ffb5cc9188ca4103c`  
		Last Modified: Wed, 10 Apr 2024 05:47:06 GMT  
		Size: 1.0 MB (1006415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed7e751eeae0842d327bdd471ebb9980742bf95e5a8e651fee26e09c2c90bfc`  
		Last Modified: Wed, 10 Apr 2024 05:47:14 GMT  
		Size: 95.8 MB (95803925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded3ff1728a91eb77cb93172de6d0534f28d609cf13acb2f0881120e9e61815c`  
		Last Modified: Wed, 10 Apr 2024 05:47:06 GMT  
		Size: 23.1 MB (23128349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2ff3b182a0b730c10e86ba4322e8dcd3756de9a5422a8b827631bc4f55bd6e8`  
		Last Modified: Wed, 10 Apr 2024 05:47:04 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acb3ba01d573f786db866b75cb9e9ba38dffcbc9425ea0c64d02756f6588e822`  
		Last Modified: Wed, 10 Apr 2024 05:47:04 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0aed24831c353f63d0b8cb89672c273f9b59204f7f732778f8e01f49745dfa2`  
		Last Modified: Wed, 10 Apr 2024 05:47:04 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.7` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:b7fbcc20cf648a208b1971ae25ee08f34546e1d72ab9410415527623d662d884
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.9 MB (158902762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01a617cea425cf53790f5482a8378c200944e1b6609e1e1d7a850d6b5b1305b0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:23 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Wed, 10 Apr 2024 00:40:23 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:21:09 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:21:10 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version
# Wed, 10 Apr 2024 05:21:10 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb
# Wed, 10 Apr 2024 05:21:10 GMT
ENV GOSU_VER=1.16
# Wed, 10 Apr 2024 05:21:13 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true
# Wed, 10 Apr 2024 05:21:13 GMT
ENV INFLUXDB_VERSION=2.7.5
# Wed, 10 Apr 2024 05:21:19 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version
# Wed, 10 Apr 2024 05:21:21 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Wed, 10 Apr 2024 05:21:23 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version
# Wed, 10 Apr 2024 05:21:24 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 10 Apr 2024 05:21:24 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 10 Apr 2024 05:21:24 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 10 Apr 2024 05:21:24 GMT
COPY file:b5520696339eadb7386055c1dc9487351aa145a79b0cf206d8b1a79699c4a7f1 in /entrypoint.sh 
# Wed, 10 Apr 2024 05:21:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 05:21:24 GMT
CMD ["influxd"]
# Wed, 10 Apr 2024 05:21:24 GMT
EXPOSE 8086
# Wed, 10 Apr 2024 05:21:24 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 10 Apr 2024 05:21:24 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 10 Apr 2024 05:21:24 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 10 Apr 2024 05:21:25 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab984742598cff95bd5de2e52df20eeabf05fccfeaa8a235da31e0e29ac482b`  
		Last Modified: Wed, 10 Apr 2024 05:21:57 GMT  
		Size: 9.6 MB (9581645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ccb29a42d38c08a905851fc53e23904361f52e5d3848e2d7b42f371dcbb38d`  
		Last Modified: Wed, 10 Apr 2024 05:21:55 GMT  
		Size: 5.5 MB (5463799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f786470e92bb4dba4737427552f576121bd301af37d785393afb208e1d59045`  
		Last Modified: Wed, 10 Apr 2024 05:21:54 GMT  
		Size: 3.3 KB (3279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:223efb50d26dd6bedd713da9b618cc0171c3f0d0a532f27d53c069ddbea9140f`  
		Last Modified: Wed, 10 Apr 2024 05:21:54 GMT  
		Size: 936.1 KB (936119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc5b2adfe6d39b3ffe0284a7de5689494803b1021507fd0d486ce640157cb18e`  
		Last Modified: Wed, 10 Apr 2024 05:21:59 GMT  
		Size: 92.1 MB (92086343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:633c7190aa2688c173444ae72db53d0d121b37bbe8fd5304857e56119ef56370`  
		Last Modified: Wed, 10 Apr 2024 05:21:54 GMT  
		Size: 21.7 MB (21662598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a6919049ad8d79ca20911a1a23495e0c8e54273789911c1ffd65fb2d64992f9`  
		Last Modified: Wed, 10 Apr 2024 05:21:52 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:256ee5f12ab78fa725e633a85c6a3cd1c60f643822d0a28a2ec92c1fa5a67e3a`  
		Last Modified: Wed, 10 Apr 2024 05:21:52 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05766916b3e30a9771ecbec56e08d9b650d23f91617156cd17c2e5073bc6de4d`  
		Last Modified: Wed, 10 Apr 2024 05:21:52 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.7-alpine`

```console
$ docker pull influxdb@sha256:fffdcab19393a354155d33f2eec1fca1e35c70989f6a804ecc9fa66e4919cfe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.7-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:44692a6cbbcd59bfedd97d293277985e6ce5f83706468905ab47738d539ef7d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.2 MB (89169146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db93938edb34f78ae0e3a78d4bbdcd2305c248822562c75676414d3b92ec3ff6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:20:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 07:55:50 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates
# Sat, 16 Mar 2024 07:55:52 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version
# Sat, 16 Mar 2024 07:55:52 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Sat, 16 Mar 2024 07:55:52 GMT
ENV INFLUXDB_VERSION=2.7.5
# Sat, 16 Mar 2024 07:55:56 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version
# Sat, 16 Mar 2024 07:55:56 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Sat, 16 Mar 2024 07:55:59 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version
# Sat, 16 Mar 2024 07:55:59 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Sat, 16 Mar 2024 07:55:59 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Sat, 16 Mar 2024 07:55:59 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Sat, 16 Mar 2024 07:56:00 GMT
COPY file:6341d1dd8e0763e797b79985007acd07a4686ed831d55018f6e390823bad9d07 in /entrypoint.sh 
# Sat, 16 Mar 2024 07:56:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 07:56:00 GMT
CMD ["influxd"]
# Sat, 16 Mar 2024 07:56:00 GMT
EXPOSE 8086
# Sat, 16 Mar 2024 07:56:00 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Sat, 16 Mar 2024 07:56:00 GMT
ENV INFLUXD_INIT_PORT=9999
# Sat, 16 Mar 2024 07:56:00 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Sat, 16 Mar 2024 07:56:00 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec84f8c4b4c91fcb32de58f4c3ad4f074277a222c69804bc60e3dc52fb9edb0`  
		Last Modified: Sat, 16 Mar 2024 03:21:48 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2c04cf0ad6cd12dd58027cb82ab7cd473cbaafb98a89b6c54de66d6a4d8ed83`  
		Last Modified: Sat, 16 Mar 2024 07:57:54 GMT  
		Size: 8.9 MB (8912683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca16da08321a8772547dcf8e6665bfef94faaba388f795fd2483d67d82020a82`  
		Last Modified: Sat, 16 Mar 2024 07:57:54 GMT  
		Size: 5.8 MB (5820944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52968b0e54d2578c678da2760200217bb58d6de4a8ca283e6265d398a6898cf2`  
		Last Modified: Sat, 16 Mar 2024 07:57:53 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fae947c895929bdc7a2e45255709f2a31d1204489a3cd9d8816f8edd2c629b17`  
		Last Modified: Sat, 16 Mar 2024 07:57:56 GMT  
		Size: 47.9 MB (47896252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6fec1079edb744dadbb8b277f72e112a90417f8c91d02cb266f3d9764d2803`  
		Last Modified: Sat, 16 Mar 2024 07:57:54 GMT  
		Size: 23.1 MB (23128349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eefcf12f64fd7d55edf131d783cf222248f980fd54d8935b93f6affef9f0023`  
		Last Modified: Sat, 16 Mar 2024 07:57:51 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4f9db83590fc9950a5c5515e90fd63198ce04a7d170f6cc5f2bbbe8a97881b`  
		Last Modified: Sat, 16 Mar 2024 07:57:51 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64dd05fe3732785c572ca2bd7c0424036b824d59e1e5a8b02d54a908dafb356e`  
		Last Modified: Sat, 16 Mar 2024 07:57:51 GMT  
		Size: 6.3 KB (6283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.7-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:6c86e02bad991301d86f7e65160783891fc0c4895a6e3a2dea7e9b1a262a7d70
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.5 MB (85493150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe6b76c75225ea11626f9d4e0471e2ea3d9e1467f8900b36101cca7931629bd5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:39:20 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 02:39:22 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates
# Sat, 16 Mar 2024 02:39:23 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version
# Sat, 16 Mar 2024 02:39:24 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Sat, 16 Mar 2024 02:39:24 GMT
ENV INFLUXDB_VERSION=2.7.5
# Sat, 16 Mar 2024 02:39:27 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version
# Sat, 16 Mar 2024 02:39:27 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Sat, 16 Mar 2024 02:39:31 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version
# Sat, 16 Mar 2024 02:39:31 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Sat, 16 Mar 2024 02:39:31 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Sat, 16 Mar 2024 02:39:31 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Sat, 16 Mar 2024 02:39:31 GMT
COPY file:6341d1dd8e0763e797b79985007acd07a4686ed831d55018f6e390823bad9d07 in /entrypoint.sh 
# Sat, 16 Mar 2024 02:39:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 02:39:32 GMT
CMD ["influxd"]
# Sat, 16 Mar 2024 02:39:32 GMT
EXPOSE 8086
# Sat, 16 Mar 2024 02:39:32 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Sat, 16 Mar 2024 02:39:32 GMT
ENV INFLUXD_INIT_PORT=9999
# Sat, 16 Mar 2024 02:39:32 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Sat, 16 Mar 2024 02:39:32 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1132aa3c0a1481b1692e9b990f21c14f20ca44dcb2da0b19d2ad1b1da1aa45`  
		Last Modified: Sat, 16 Mar 2024 02:39:49 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de22938878825528f4eae2fc8baa8a5204e8ed38b4707f471dc5ec6db9dd2ac`  
		Last Modified: Sat, 16 Mar 2024 02:39:48 GMT  
		Size: 9.0 MB (8985806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c0e99e68893411c24682e55031bc9aac5a3262516395475ba13b6e8458440a`  
		Last Modified: Sat, 16 Mar 2024 02:39:48 GMT  
		Size: 5.5 MB (5463807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be6479785d41c1030f1af86ff3c17c5379b78f22493b8b30e5f77d9384e6e293`  
		Last Modified: Sat, 16 Mar 2024 02:39:47 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae3cc6f92445b13786f5da7acbaa0b5021965c810e597de4e5a2828c99098576`  
		Last Modified: Sat, 16 Mar 2024 02:39:49 GMT  
		Size: 46.0 MB (46039199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd569f416b8d58dd93eb8408a9a0e5eef5b150f59ff7ec5a730074d996fd1f87`  
		Last Modified: Sat, 16 Mar 2024 02:39:47 GMT  
		Size: 21.7 MB (21662606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa4219aea43efd5b66769a8567a98f437c694c2605e62d10b63a80d30a12622`  
		Last Modified: Sat, 16 Mar 2024 02:39:45 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb7152cc70b2894f041312ecf2f225755aca678334a506ae1a5269e7b962483`  
		Last Modified: Sat, 16 Mar 2024 02:39:45 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a3d84bef4bb47c4a25d86a8602ae3b658a0f0e169f49a502032bb6885761c7`  
		Last Modified: Sat, 16 Mar 2024 02:39:45 GMT  
		Size: 6.3 KB (6283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.7.5`

```console
$ docker pull influxdb@sha256:766904dcef641fa1491750b7b3e0dd948b30417f7ef0ac4d3f1d6ffed52a1fa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.7.5` - linux; amd64

```console
$ docker pull influxdb@sha256:a79377dc0ac143f5ecf2ce889e090bff468c324212874d4d5c7a811c8fb5b9bb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164685785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69e1e1673bcf2becedda8a32a5b3c2baa87b68c06d2f310a7ce5d514fbf17fb5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:48 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Wed, 10 Apr 2024 01:50:48 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:44:50 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:44:51 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version
# Wed, 10 Apr 2024 05:44:52 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb
# Wed, 10 Apr 2024 05:44:52 GMT
ENV GOSU_VER=1.16
# Wed, 10 Apr 2024 05:44:55 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true
# Wed, 10 Apr 2024 05:44:55 GMT
ENV INFLUXDB_VERSION=2.7.5
# Wed, 10 Apr 2024 05:44:59 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version
# Wed, 10 Apr 2024 05:45:00 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Wed, 10 Apr 2024 05:45:02 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version
# Wed, 10 Apr 2024 05:45:02 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 10 Apr 2024 05:45:02 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 10 Apr 2024 05:45:02 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 10 Apr 2024 05:45:03 GMT
COPY file:b5520696339eadb7386055c1dc9487351aa145a79b0cf206d8b1a79699c4a7f1 in /entrypoint.sh 
# Wed, 10 Apr 2024 05:45:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 05:45:03 GMT
CMD ["influxd"]
# Wed, 10 Apr 2024 05:45:03 GMT
EXPOSE 8086
# Wed, 10 Apr 2024 05:45:03 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 10 Apr 2024 05:45:03 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 10 Apr 2024 05:45:03 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 10 Apr 2024 05:45:03 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9294b900aa832728712196b5b6ef7b95954cbd7e6ac2d2c3840babb4128647c9`  
		Last Modified: Wed, 10 Apr 2024 05:47:09 GMT  
		Size: 9.8 MB (9784694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:425f098c3e26f8250bb21e082e37566627a939347a6d788cd64bf327955c22e9`  
		Last Modified: Wed, 10 Apr 2024 05:47:06 GMT  
		Size: 5.8 MB (5820944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80ba552c178797635fea84bd0613688f23b019299cfd6c7c94e1fbfdf1f819c`  
		Last Modified: Wed, 10 Apr 2024 05:47:06 GMT  
		Size: 3.3 KB (3280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2f8eb3058c2906e30b0f6dcc625636f4072aba364303a4ffb5cc9188ca4103c`  
		Last Modified: Wed, 10 Apr 2024 05:47:06 GMT  
		Size: 1.0 MB (1006415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed7e751eeae0842d327bdd471ebb9980742bf95e5a8e651fee26e09c2c90bfc`  
		Last Modified: Wed, 10 Apr 2024 05:47:14 GMT  
		Size: 95.8 MB (95803925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded3ff1728a91eb77cb93172de6d0534f28d609cf13acb2f0881120e9e61815c`  
		Last Modified: Wed, 10 Apr 2024 05:47:06 GMT  
		Size: 23.1 MB (23128349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2ff3b182a0b730c10e86ba4322e8dcd3756de9a5422a8b827631bc4f55bd6e8`  
		Last Modified: Wed, 10 Apr 2024 05:47:04 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acb3ba01d573f786db866b75cb9e9ba38dffcbc9425ea0c64d02756f6588e822`  
		Last Modified: Wed, 10 Apr 2024 05:47:04 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0aed24831c353f63d0b8cb89672c273f9b59204f7f732778f8e01f49745dfa2`  
		Last Modified: Wed, 10 Apr 2024 05:47:04 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.7.5` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:b7fbcc20cf648a208b1971ae25ee08f34546e1d72ab9410415527623d662d884
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.9 MB (158902762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01a617cea425cf53790f5482a8378c200944e1b6609e1e1d7a850d6b5b1305b0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:23 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Wed, 10 Apr 2024 00:40:23 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:21:09 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:21:10 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version
# Wed, 10 Apr 2024 05:21:10 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb
# Wed, 10 Apr 2024 05:21:10 GMT
ENV GOSU_VER=1.16
# Wed, 10 Apr 2024 05:21:13 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true
# Wed, 10 Apr 2024 05:21:13 GMT
ENV INFLUXDB_VERSION=2.7.5
# Wed, 10 Apr 2024 05:21:19 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version
# Wed, 10 Apr 2024 05:21:21 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Wed, 10 Apr 2024 05:21:23 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version
# Wed, 10 Apr 2024 05:21:24 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 10 Apr 2024 05:21:24 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 10 Apr 2024 05:21:24 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 10 Apr 2024 05:21:24 GMT
COPY file:b5520696339eadb7386055c1dc9487351aa145a79b0cf206d8b1a79699c4a7f1 in /entrypoint.sh 
# Wed, 10 Apr 2024 05:21:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 05:21:24 GMT
CMD ["influxd"]
# Wed, 10 Apr 2024 05:21:24 GMT
EXPOSE 8086
# Wed, 10 Apr 2024 05:21:24 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 10 Apr 2024 05:21:24 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 10 Apr 2024 05:21:24 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 10 Apr 2024 05:21:25 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab984742598cff95bd5de2e52df20eeabf05fccfeaa8a235da31e0e29ac482b`  
		Last Modified: Wed, 10 Apr 2024 05:21:57 GMT  
		Size: 9.6 MB (9581645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ccb29a42d38c08a905851fc53e23904361f52e5d3848e2d7b42f371dcbb38d`  
		Last Modified: Wed, 10 Apr 2024 05:21:55 GMT  
		Size: 5.5 MB (5463799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f786470e92bb4dba4737427552f576121bd301af37d785393afb208e1d59045`  
		Last Modified: Wed, 10 Apr 2024 05:21:54 GMT  
		Size: 3.3 KB (3279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:223efb50d26dd6bedd713da9b618cc0171c3f0d0a532f27d53c069ddbea9140f`  
		Last Modified: Wed, 10 Apr 2024 05:21:54 GMT  
		Size: 936.1 KB (936119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc5b2adfe6d39b3ffe0284a7de5689494803b1021507fd0d486ce640157cb18e`  
		Last Modified: Wed, 10 Apr 2024 05:21:59 GMT  
		Size: 92.1 MB (92086343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:633c7190aa2688c173444ae72db53d0d121b37bbe8fd5304857e56119ef56370`  
		Last Modified: Wed, 10 Apr 2024 05:21:54 GMT  
		Size: 21.7 MB (21662598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a6919049ad8d79ca20911a1a23495e0c8e54273789911c1ffd65fb2d64992f9`  
		Last Modified: Wed, 10 Apr 2024 05:21:52 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:256ee5f12ab78fa725e633a85c6a3cd1c60f643822d0a28a2ec92c1fa5a67e3a`  
		Last Modified: Wed, 10 Apr 2024 05:21:52 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05766916b3e30a9771ecbec56e08d9b650d23f91617156cd17c2e5073bc6de4d`  
		Last Modified: Wed, 10 Apr 2024 05:21:52 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.7.5-alpine`

```console
$ docker pull influxdb@sha256:fffdcab19393a354155d33f2eec1fca1e35c70989f6a804ecc9fa66e4919cfe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.7.5-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:44692a6cbbcd59bfedd97d293277985e6ce5f83706468905ab47738d539ef7d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.2 MB (89169146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db93938edb34f78ae0e3a78d4bbdcd2305c248822562c75676414d3b92ec3ff6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:20:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 07:55:50 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates
# Sat, 16 Mar 2024 07:55:52 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version
# Sat, 16 Mar 2024 07:55:52 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Sat, 16 Mar 2024 07:55:52 GMT
ENV INFLUXDB_VERSION=2.7.5
# Sat, 16 Mar 2024 07:55:56 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version
# Sat, 16 Mar 2024 07:55:56 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Sat, 16 Mar 2024 07:55:59 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version
# Sat, 16 Mar 2024 07:55:59 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Sat, 16 Mar 2024 07:55:59 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Sat, 16 Mar 2024 07:55:59 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Sat, 16 Mar 2024 07:56:00 GMT
COPY file:6341d1dd8e0763e797b79985007acd07a4686ed831d55018f6e390823bad9d07 in /entrypoint.sh 
# Sat, 16 Mar 2024 07:56:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 07:56:00 GMT
CMD ["influxd"]
# Sat, 16 Mar 2024 07:56:00 GMT
EXPOSE 8086
# Sat, 16 Mar 2024 07:56:00 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Sat, 16 Mar 2024 07:56:00 GMT
ENV INFLUXD_INIT_PORT=9999
# Sat, 16 Mar 2024 07:56:00 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Sat, 16 Mar 2024 07:56:00 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec84f8c4b4c91fcb32de58f4c3ad4f074277a222c69804bc60e3dc52fb9edb0`  
		Last Modified: Sat, 16 Mar 2024 03:21:48 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2c04cf0ad6cd12dd58027cb82ab7cd473cbaafb98a89b6c54de66d6a4d8ed83`  
		Last Modified: Sat, 16 Mar 2024 07:57:54 GMT  
		Size: 8.9 MB (8912683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca16da08321a8772547dcf8e6665bfef94faaba388f795fd2483d67d82020a82`  
		Last Modified: Sat, 16 Mar 2024 07:57:54 GMT  
		Size: 5.8 MB (5820944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52968b0e54d2578c678da2760200217bb58d6de4a8ca283e6265d398a6898cf2`  
		Last Modified: Sat, 16 Mar 2024 07:57:53 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fae947c895929bdc7a2e45255709f2a31d1204489a3cd9d8816f8edd2c629b17`  
		Last Modified: Sat, 16 Mar 2024 07:57:56 GMT  
		Size: 47.9 MB (47896252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6fec1079edb744dadbb8b277f72e112a90417f8c91d02cb266f3d9764d2803`  
		Last Modified: Sat, 16 Mar 2024 07:57:54 GMT  
		Size: 23.1 MB (23128349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eefcf12f64fd7d55edf131d783cf222248f980fd54d8935b93f6affef9f0023`  
		Last Modified: Sat, 16 Mar 2024 07:57:51 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4f9db83590fc9950a5c5515e90fd63198ce04a7d170f6cc5f2bbbe8a97881b`  
		Last Modified: Sat, 16 Mar 2024 07:57:51 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64dd05fe3732785c572ca2bd7c0424036b824d59e1e5a8b02d54a908dafb356e`  
		Last Modified: Sat, 16 Mar 2024 07:57:51 GMT  
		Size: 6.3 KB (6283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.7.5-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:6c86e02bad991301d86f7e65160783891fc0c4895a6e3a2dea7e9b1a262a7d70
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.5 MB (85493150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe6b76c75225ea11626f9d4e0471e2ea3d9e1467f8900b36101cca7931629bd5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:39:20 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 02:39:22 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates
# Sat, 16 Mar 2024 02:39:23 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version
# Sat, 16 Mar 2024 02:39:24 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Sat, 16 Mar 2024 02:39:24 GMT
ENV INFLUXDB_VERSION=2.7.5
# Sat, 16 Mar 2024 02:39:27 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version
# Sat, 16 Mar 2024 02:39:27 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Sat, 16 Mar 2024 02:39:31 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version
# Sat, 16 Mar 2024 02:39:31 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Sat, 16 Mar 2024 02:39:31 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Sat, 16 Mar 2024 02:39:31 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Sat, 16 Mar 2024 02:39:31 GMT
COPY file:6341d1dd8e0763e797b79985007acd07a4686ed831d55018f6e390823bad9d07 in /entrypoint.sh 
# Sat, 16 Mar 2024 02:39:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 02:39:32 GMT
CMD ["influxd"]
# Sat, 16 Mar 2024 02:39:32 GMT
EXPOSE 8086
# Sat, 16 Mar 2024 02:39:32 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Sat, 16 Mar 2024 02:39:32 GMT
ENV INFLUXD_INIT_PORT=9999
# Sat, 16 Mar 2024 02:39:32 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Sat, 16 Mar 2024 02:39:32 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1132aa3c0a1481b1692e9b990f21c14f20ca44dcb2da0b19d2ad1b1da1aa45`  
		Last Modified: Sat, 16 Mar 2024 02:39:49 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de22938878825528f4eae2fc8baa8a5204e8ed38b4707f471dc5ec6db9dd2ac`  
		Last Modified: Sat, 16 Mar 2024 02:39:48 GMT  
		Size: 9.0 MB (8985806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c0e99e68893411c24682e55031bc9aac5a3262516395475ba13b6e8458440a`  
		Last Modified: Sat, 16 Mar 2024 02:39:48 GMT  
		Size: 5.5 MB (5463807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be6479785d41c1030f1af86ff3c17c5379b78f22493b8b30e5f77d9384e6e293`  
		Last Modified: Sat, 16 Mar 2024 02:39:47 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae3cc6f92445b13786f5da7acbaa0b5021965c810e597de4e5a2828c99098576`  
		Last Modified: Sat, 16 Mar 2024 02:39:49 GMT  
		Size: 46.0 MB (46039199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd569f416b8d58dd93eb8408a9a0e5eef5b150f59ff7ec5a730074d996fd1f87`  
		Last Modified: Sat, 16 Mar 2024 02:39:47 GMT  
		Size: 21.7 MB (21662606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa4219aea43efd5b66769a8567a98f437c694c2605e62d10b63a80d30a12622`  
		Last Modified: Sat, 16 Mar 2024 02:39:45 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb7152cc70b2894f041312ecf2f225755aca678334a506ae1a5269e7b962483`  
		Last Modified: Sat, 16 Mar 2024 02:39:45 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a3d84bef4bb47c4a25d86a8602ae3b658a0f0e169f49a502032bb6885761c7`  
		Last Modified: Sat, 16 Mar 2024 02:39:45 GMT  
		Size: 6.3 KB (6283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:fffdcab19393a354155d33f2eec1fca1e35c70989f6a804ecc9fa66e4919cfe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:44692a6cbbcd59bfedd97d293277985e6ce5f83706468905ab47738d539ef7d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.2 MB (89169146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db93938edb34f78ae0e3a78d4bbdcd2305c248822562c75676414d3b92ec3ff6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:20:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 07:55:50 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates
# Sat, 16 Mar 2024 07:55:52 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version
# Sat, 16 Mar 2024 07:55:52 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Sat, 16 Mar 2024 07:55:52 GMT
ENV INFLUXDB_VERSION=2.7.5
# Sat, 16 Mar 2024 07:55:56 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version
# Sat, 16 Mar 2024 07:55:56 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Sat, 16 Mar 2024 07:55:59 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version
# Sat, 16 Mar 2024 07:55:59 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Sat, 16 Mar 2024 07:55:59 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Sat, 16 Mar 2024 07:55:59 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Sat, 16 Mar 2024 07:56:00 GMT
COPY file:6341d1dd8e0763e797b79985007acd07a4686ed831d55018f6e390823bad9d07 in /entrypoint.sh 
# Sat, 16 Mar 2024 07:56:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 07:56:00 GMT
CMD ["influxd"]
# Sat, 16 Mar 2024 07:56:00 GMT
EXPOSE 8086
# Sat, 16 Mar 2024 07:56:00 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Sat, 16 Mar 2024 07:56:00 GMT
ENV INFLUXD_INIT_PORT=9999
# Sat, 16 Mar 2024 07:56:00 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Sat, 16 Mar 2024 07:56:00 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec84f8c4b4c91fcb32de58f4c3ad4f074277a222c69804bc60e3dc52fb9edb0`  
		Last Modified: Sat, 16 Mar 2024 03:21:48 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2c04cf0ad6cd12dd58027cb82ab7cd473cbaafb98a89b6c54de66d6a4d8ed83`  
		Last Modified: Sat, 16 Mar 2024 07:57:54 GMT  
		Size: 8.9 MB (8912683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca16da08321a8772547dcf8e6665bfef94faaba388f795fd2483d67d82020a82`  
		Last Modified: Sat, 16 Mar 2024 07:57:54 GMT  
		Size: 5.8 MB (5820944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52968b0e54d2578c678da2760200217bb58d6de4a8ca283e6265d398a6898cf2`  
		Last Modified: Sat, 16 Mar 2024 07:57:53 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fae947c895929bdc7a2e45255709f2a31d1204489a3cd9d8816f8edd2c629b17`  
		Last Modified: Sat, 16 Mar 2024 07:57:56 GMT  
		Size: 47.9 MB (47896252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6fec1079edb744dadbb8b277f72e112a90417f8c91d02cb266f3d9764d2803`  
		Last Modified: Sat, 16 Mar 2024 07:57:54 GMT  
		Size: 23.1 MB (23128349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eefcf12f64fd7d55edf131d783cf222248f980fd54d8935b93f6affef9f0023`  
		Last Modified: Sat, 16 Mar 2024 07:57:51 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4f9db83590fc9950a5c5515e90fd63198ce04a7d170f6cc5f2bbbe8a97881b`  
		Last Modified: Sat, 16 Mar 2024 07:57:51 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64dd05fe3732785c572ca2bd7c0424036b824d59e1e5a8b02d54a908dafb356e`  
		Last Modified: Sat, 16 Mar 2024 07:57:51 GMT  
		Size: 6.3 KB (6283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:6c86e02bad991301d86f7e65160783891fc0c4895a6e3a2dea7e9b1a262a7d70
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.5 MB (85493150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe6b76c75225ea11626f9d4e0471e2ea3d9e1467f8900b36101cca7931629bd5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:39:20 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 02:39:22 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates
# Sat, 16 Mar 2024 02:39:23 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version
# Sat, 16 Mar 2024 02:39:24 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Sat, 16 Mar 2024 02:39:24 GMT
ENV INFLUXDB_VERSION=2.7.5
# Sat, 16 Mar 2024 02:39:27 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version
# Sat, 16 Mar 2024 02:39:27 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Sat, 16 Mar 2024 02:39:31 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version
# Sat, 16 Mar 2024 02:39:31 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Sat, 16 Mar 2024 02:39:31 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Sat, 16 Mar 2024 02:39:31 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Sat, 16 Mar 2024 02:39:31 GMT
COPY file:6341d1dd8e0763e797b79985007acd07a4686ed831d55018f6e390823bad9d07 in /entrypoint.sh 
# Sat, 16 Mar 2024 02:39:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 02:39:32 GMT
CMD ["influxd"]
# Sat, 16 Mar 2024 02:39:32 GMT
EXPOSE 8086
# Sat, 16 Mar 2024 02:39:32 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Sat, 16 Mar 2024 02:39:32 GMT
ENV INFLUXD_INIT_PORT=9999
# Sat, 16 Mar 2024 02:39:32 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Sat, 16 Mar 2024 02:39:32 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1132aa3c0a1481b1692e9b990f21c14f20ca44dcb2da0b19d2ad1b1da1aa45`  
		Last Modified: Sat, 16 Mar 2024 02:39:49 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de22938878825528f4eae2fc8baa8a5204e8ed38b4707f471dc5ec6db9dd2ac`  
		Last Modified: Sat, 16 Mar 2024 02:39:48 GMT  
		Size: 9.0 MB (8985806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c0e99e68893411c24682e55031bc9aac5a3262516395475ba13b6e8458440a`  
		Last Modified: Sat, 16 Mar 2024 02:39:48 GMT  
		Size: 5.5 MB (5463807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be6479785d41c1030f1af86ff3c17c5379b78f22493b8b30e5f77d9384e6e293`  
		Last Modified: Sat, 16 Mar 2024 02:39:47 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae3cc6f92445b13786f5da7acbaa0b5021965c810e597de4e5a2828c99098576`  
		Last Modified: Sat, 16 Mar 2024 02:39:49 GMT  
		Size: 46.0 MB (46039199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd569f416b8d58dd93eb8408a9a0e5eef5b150f59ff7ec5a730074d996fd1f87`  
		Last Modified: Sat, 16 Mar 2024 02:39:47 GMT  
		Size: 21.7 MB (21662606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa4219aea43efd5b66769a8567a98f437c694c2605e62d10b63a80d30a12622`  
		Last Modified: Sat, 16 Mar 2024 02:39:45 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb7152cc70b2894f041312ecf2f225755aca678334a506ae1a5269e7b962483`  
		Last Modified: Sat, 16 Mar 2024 02:39:45 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a3d84bef4bb47c4a25d86a8602ae3b658a0f0e169f49a502032bb6885761c7`  
		Last Modified: Sat, 16 Mar 2024 02:39:45 GMT  
		Size: 6.3 KB (6283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:latest`

```console
$ docker pull influxdb@sha256:766904dcef641fa1491750b7b3e0dd948b30417f7ef0ac4d3f1d6ffed52a1fa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:a79377dc0ac143f5ecf2ce889e090bff468c324212874d4d5c7a811c8fb5b9bb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164685785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69e1e1673bcf2becedda8a32a5b3c2baa87b68c06d2f310a7ce5d514fbf17fb5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:48 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Wed, 10 Apr 2024 01:50:48 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:44:50 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:44:51 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version
# Wed, 10 Apr 2024 05:44:52 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb
# Wed, 10 Apr 2024 05:44:52 GMT
ENV GOSU_VER=1.16
# Wed, 10 Apr 2024 05:44:55 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true
# Wed, 10 Apr 2024 05:44:55 GMT
ENV INFLUXDB_VERSION=2.7.5
# Wed, 10 Apr 2024 05:44:59 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version
# Wed, 10 Apr 2024 05:45:00 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Wed, 10 Apr 2024 05:45:02 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version
# Wed, 10 Apr 2024 05:45:02 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 10 Apr 2024 05:45:02 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 10 Apr 2024 05:45:02 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 10 Apr 2024 05:45:03 GMT
COPY file:b5520696339eadb7386055c1dc9487351aa145a79b0cf206d8b1a79699c4a7f1 in /entrypoint.sh 
# Wed, 10 Apr 2024 05:45:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 05:45:03 GMT
CMD ["influxd"]
# Wed, 10 Apr 2024 05:45:03 GMT
EXPOSE 8086
# Wed, 10 Apr 2024 05:45:03 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 10 Apr 2024 05:45:03 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 10 Apr 2024 05:45:03 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 10 Apr 2024 05:45:03 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9294b900aa832728712196b5b6ef7b95954cbd7e6ac2d2c3840babb4128647c9`  
		Last Modified: Wed, 10 Apr 2024 05:47:09 GMT  
		Size: 9.8 MB (9784694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:425f098c3e26f8250bb21e082e37566627a939347a6d788cd64bf327955c22e9`  
		Last Modified: Wed, 10 Apr 2024 05:47:06 GMT  
		Size: 5.8 MB (5820944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80ba552c178797635fea84bd0613688f23b019299cfd6c7c94e1fbfdf1f819c`  
		Last Modified: Wed, 10 Apr 2024 05:47:06 GMT  
		Size: 3.3 KB (3280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2f8eb3058c2906e30b0f6dcc625636f4072aba364303a4ffb5cc9188ca4103c`  
		Last Modified: Wed, 10 Apr 2024 05:47:06 GMT  
		Size: 1.0 MB (1006415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed7e751eeae0842d327bdd471ebb9980742bf95e5a8e651fee26e09c2c90bfc`  
		Last Modified: Wed, 10 Apr 2024 05:47:14 GMT  
		Size: 95.8 MB (95803925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded3ff1728a91eb77cb93172de6d0534f28d609cf13acb2f0881120e9e61815c`  
		Last Modified: Wed, 10 Apr 2024 05:47:06 GMT  
		Size: 23.1 MB (23128349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2ff3b182a0b730c10e86ba4322e8dcd3756de9a5422a8b827631bc4f55bd6e8`  
		Last Modified: Wed, 10 Apr 2024 05:47:04 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acb3ba01d573f786db866b75cb9e9ba38dffcbc9425ea0c64d02756f6588e822`  
		Last Modified: Wed, 10 Apr 2024 05:47:04 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0aed24831c353f63d0b8cb89672c273f9b59204f7f732778f8e01f49745dfa2`  
		Last Modified: Wed, 10 Apr 2024 05:47:04 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:b7fbcc20cf648a208b1971ae25ee08f34546e1d72ab9410415527623d662d884
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.9 MB (158902762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01a617cea425cf53790f5482a8378c200944e1b6609e1e1d7a850d6b5b1305b0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:23 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Wed, 10 Apr 2024 00:40:23 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:21:09 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:21:10 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version
# Wed, 10 Apr 2024 05:21:10 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb
# Wed, 10 Apr 2024 05:21:10 GMT
ENV GOSU_VER=1.16
# Wed, 10 Apr 2024 05:21:13 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true
# Wed, 10 Apr 2024 05:21:13 GMT
ENV INFLUXDB_VERSION=2.7.5
# Wed, 10 Apr 2024 05:21:19 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version
# Wed, 10 Apr 2024 05:21:21 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Wed, 10 Apr 2024 05:21:23 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version
# Wed, 10 Apr 2024 05:21:24 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 10 Apr 2024 05:21:24 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 10 Apr 2024 05:21:24 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 10 Apr 2024 05:21:24 GMT
COPY file:b5520696339eadb7386055c1dc9487351aa145a79b0cf206d8b1a79699c4a7f1 in /entrypoint.sh 
# Wed, 10 Apr 2024 05:21:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 05:21:24 GMT
CMD ["influxd"]
# Wed, 10 Apr 2024 05:21:24 GMT
EXPOSE 8086
# Wed, 10 Apr 2024 05:21:24 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 10 Apr 2024 05:21:24 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 10 Apr 2024 05:21:24 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 10 Apr 2024 05:21:25 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab984742598cff95bd5de2e52df20eeabf05fccfeaa8a235da31e0e29ac482b`  
		Last Modified: Wed, 10 Apr 2024 05:21:57 GMT  
		Size: 9.6 MB (9581645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ccb29a42d38c08a905851fc53e23904361f52e5d3848e2d7b42f371dcbb38d`  
		Last Modified: Wed, 10 Apr 2024 05:21:55 GMT  
		Size: 5.5 MB (5463799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f786470e92bb4dba4737427552f576121bd301af37d785393afb208e1d59045`  
		Last Modified: Wed, 10 Apr 2024 05:21:54 GMT  
		Size: 3.3 KB (3279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:223efb50d26dd6bedd713da9b618cc0171c3f0d0a532f27d53c069ddbea9140f`  
		Last Modified: Wed, 10 Apr 2024 05:21:54 GMT  
		Size: 936.1 KB (936119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc5b2adfe6d39b3ffe0284a7de5689494803b1021507fd0d486ce640157cb18e`  
		Last Modified: Wed, 10 Apr 2024 05:21:59 GMT  
		Size: 92.1 MB (92086343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:633c7190aa2688c173444ae72db53d0d121b37bbe8fd5304857e56119ef56370`  
		Last Modified: Wed, 10 Apr 2024 05:21:54 GMT  
		Size: 21.7 MB (21662598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a6919049ad8d79ca20911a1a23495e0c8e54273789911c1ffd65fb2d64992f9`  
		Last Modified: Wed, 10 Apr 2024 05:21:52 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:256ee5f12ab78fa725e633a85c6a3cd1c60f643822d0a28a2ec92c1fa5a67e3a`  
		Last Modified: Wed, 10 Apr 2024 05:21:52 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05766916b3e30a9771ecbec56e08d9b650d23f91617156cd17c2e5073bc6de4d`  
		Last Modified: Wed, 10 Apr 2024 05:21:52 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
