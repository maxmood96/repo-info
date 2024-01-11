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
-	[`influxdb:1.11.3-data`](#influxdb1113-data)
-	[`influxdb:1.11.3-data-alpine`](#influxdb1113-data-alpine)
-	[`influxdb:1.11.3-meta`](#influxdb1113-meta)
-	[`influxdb:1.11.3-meta-alpine`](#influxdb1113-meta-alpine)
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
-	[`influxdb:2.7`](#influxdb27)
-	[`influxdb:2.7-alpine`](#influxdb27-alpine)
-	[`influxdb:2.7.5`](#influxdb275)
-	[`influxdb:2.7.5-alpine`](#influxdb275-alpine)
-	[`influxdb:alpine`](#influxdbalpine)
-	[`influxdb:latest`](#influxdblatest)

## `influxdb:1.10-data`

```console
$ docker pull influxdb@sha256:13c4385d515a821012e54f24b76eb8846546b1ac8b7398236fff2c486f556c64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.10-data` - linux; amd64

```console
$ docker pull influxdb@sha256:787e4a9c2839d48627e0d746d626a754b13a0632f2c1ca2c05fcf10271d86ed7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.0 MB (111002715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d87488851bcb341a966dcbf8b43e39ca51a0079127511618ab3958f0114aa4c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:04 GMT
ADD file:35f7caaedc3b6f725dee87eb8d1f2727c04cb21062b5eb7f59801dafced61993 in / 
# Thu, 11 Jan 2024 02:38:05 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:36:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 16:39:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 16:39:30 GMT
ENV INFLUXDB_VERSION=1.10.5-c1.10.5
# Thu, 11 Jan 2024 16:39:40 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb*
# Thu, 11 Jan 2024 16:39:41 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Thu, 11 Jan 2024 16:39:41 GMT
EXPOSE 8086
# Thu, 11 Jan 2024 16:39:41 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jan 2024 16:39:41 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Thu, 11 Jan 2024 16:39:41 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 11 Jan 2024 16:39:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 16:39:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:e455cf41eadb2f19f014361006086cdc5b3de16f3d13bd1d586be63e66c7fc63`  
		Last Modified: Thu, 11 Jan 2024 02:42:47 GMT  
		Size: 55.1 MB (55057723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4531da2f06f2911a5e67446c1ec507acb336afe7130741c6ed12ce442b730f`  
		Last Modified: Thu, 11 Jan 2024 04:45:42 GMT  
		Size: 15.8 MB (15765113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14fb060119b49def67db8ec15d6ffc47c094d5675101637e97e7f06d38aa3fe0`  
		Last Modified: Thu, 11 Jan 2024 16:40:43 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cbae3f13bd83a1e1e8490e41d7c9c1178bfe10bf6e62d7f8c66cdfe4581cb84`  
		Last Modified: Thu, 11 Jan 2024 16:41:31 GMT  
		Size: 40.2 MB (40176292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37765368a964e30ea1acee39a6a8eefc7f3c83d15264c6d14c37d4723c8dd6c5`  
		Last Modified: Thu, 11 Jan 2024 16:41:25 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:863a0da84099146fdc5f70c5e8532cf41d3027e9364b0021e88ba903068b62fa`  
		Last Modified: Thu, 11 Jan 2024 16:41:25 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a2b4327a0b556a9510cf0dde4ea90b848594b15c53419eac41a45c8c29e9ead`  
		Last Modified: Thu, 11 Jan 2024 16:41:25 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.10-data-alpine`

```console
$ docker pull influxdb@sha256:2117575b93381be200ddd8ce5a157b8054779e53f106994d10a4f537844c3151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.10-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:b2274bb9a14dd05391b921875676302516acdf1ba1bc95dc1b2731a1e4487566
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (44986916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4669f9422cfb1a2783f9a2171e992cf3cdcdd6933edea40131e6436ae11649f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:58 GMT
ADD file:80331a5d882ac8a70763f4b19e06f2e04ea3dca34ae6d92810815b170b3c806c in / 
# Thu, 30 Nov 2023 23:22:59 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 05:22:09 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 01 Dec 2023 05:22:10 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Fri, 01 Dec 2023 05:22:47 GMT
ENV INFLUXDB_VERSION=1.10.5-c1.10.5
# Fri, 01 Dec 2023 05:22:55 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 01 Dec 2023 05:22:55 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Fri, 01 Dec 2023 05:22:55 GMT
EXPOSE 8086
# Fri, 01 Dec 2023 05:22:56 GMT
VOLUME [/var/lib/influxdb]
# Fri, 01 Dec 2023 05:22:56 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Fri, 01 Dec 2023 05:22:56 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Fri, 01 Dec 2023 05:22:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Dec 2023 05:22:56 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:1207c741d8c9b028d98c4006013f9de959da3c55f85b91ed5e4583438a0112ca`  
		Last Modified: Thu, 30 Nov 2023 23:23:40 GMT  
		Size: 3.4 MB (3379323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae43a7dfb488bfdf09941272691a16afeb9a0ec5f2aeb3afb906b9e61d0eea0`  
		Last Modified: Fri, 01 Dec 2023 05:24:18 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8414376f36c8ce530795b6f714715e47f66e1bc7cb691ab3238a1f754acff0`  
		Last Modified: Fri, 01 Dec 2023 05:24:16 GMT  
		Size: 1.5 MB (1472464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4040553c9c4bfc1e84707ed35934a581848951de238f0e2cda33654f4924283`  
		Last Modified: Fri, 01 Dec 2023 05:25:05 GMT  
		Size: 40.1 MB (40133053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71a763104a99899d4d80f18aeab3093f53fc0de2c31e200274764c203be4cfb6`  
		Last Modified: Fri, 01 Dec 2023 05:24:58 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267fb35b58ade3e29f48cd35502ba2842dd86488daa4b941a3561c059f7485df`  
		Last Modified: Fri, 01 Dec 2023 05:24:58 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72ff4725b950867c0001a8e947beddaf7e4cd023407eb75c02e9f716de39dfaa`  
		Last Modified: Fri, 01 Dec 2023 05:24:58 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.10-meta`

```console
$ docker pull influxdb@sha256:dc70ca29f4ee113e1c460d7e392414d3f82a5ae240efe0dd2f6f1325b65380e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.10-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:97879a03b3a98086d139722c2891877636c6c5b5a37d3c18fec8ce236e740d6a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91202175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8391d280ec8b16479ba90a79f5eed4ed80d1a45de82b7522e9e57331945d0c3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:04 GMT
ADD file:35f7caaedc3b6f725dee87eb8d1f2727c04cb21062b5eb7f59801dafced61993 in / 
# Thu, 11 Jan 2024 02:38:05 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:36:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 16:39:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 16:39:30 GMT
ENV INFLUXDB_VERSION=1.10.5-c1.10.5
# Thu, 11 Jan 2024 16:39:54 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb*
# Thu, 11 Jan 2024 16:39:54 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Thu, 11 Jan 2024 16:39:54 GMT
EXPOSE 8091
# Thu, 11 Jan 2024 16:39:54 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jan 2024 16:39:54 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Thu, 11 Jan 2024 16:39:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 16:39:55 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:e455cf41eadb2f19f014361006086cdc5b3de16f3d13bd1d586be63e66c7fc63`  
		Last Modified: Thu, 11 Jan 2024 02:42:47 GMT  
		Size: 55.1 MB (55057723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4531da2f06f2911a5e67446c1ec507acb336afe7130741c6ed12ce442b730f`  
		Last Modified: Thu, 11 Jan 2024 04:45:42 GMT  
		Size: 15.8 MB (15765113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14fb060119b49def67db8ec15d6ffc47c094d5675101637e97e7f06d38aa3fe0`  
		Last Modified: Thu, 11 Jan 2024 16:40:43 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c154a1dc6c72cd5fc8688e4d19add5818d66369dc39be6391afe15e17acf450d`  
		Last Modified: Thu, 11 Jan 2024 16:41:43 GMT  
		Size: 20.4 MB (20376954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3890e2dabf99776cf28ca1cddf448fa1046ebb37f0a1689e1c4bacb6c5b0e43`  
		Last Modified: Thu, 11 Jan 2024 16:41:40 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:044fdfac94f2536682efb484559f98ba70538541a9dc1380b5af316529c4ae42`  
		Last Modified: Thu, 11 Jan 2024 16:41:40 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.10-meta-alpine`

```console
$ docker pull influxdb@sha256:fd3c051c03348866a2698a575e78d630c420aa759c96b417a4297bcc5cf4b8a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.10-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:c142d33c1b2c956d693f0b6dc486724956053151e8977511f708991200128c1b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25196081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556704a29b056fc7cba5a69cadbb1360795209c5ee02f318e42d607bd4ec55d9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:58 GMT
ADD file:80331a5d882ac8a70763f4b19e06f2e04ea3dca34ae6d92810815b170b3c806c in / 
# Thu, 30 Nov 2023 23:22:59 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 05:22:09 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 01 Dec 2023 05:22:10 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Fri, 01 Dec 2023 05:22:47 GMT
ENV INFLUXDB_VERSION=1.10.5-c1.10.5
# Fri, 01 Dec 2023 05:23:07 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 01 Dec 2023 05:23:07 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Fri, 01 Dec 2023 05:23:07 GMT
EXPOSE 8091
# Fri, 01 Dec 2023 05:23:07 GMT
VOLUME [/var/lib/influxdb]
# Fri, 01 Dec 2023 05:23:07 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Fri, 01 Dec 2023 05:23:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Dec 2023 05:23:07 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:1207c741d8c9b028d98c4006013f9de959da3c55f85b91ed5e4583438a0112ca`  
		Last Modified: Thu, 30 Nov 2023 23:23:40 GMT  
		Size: 3.4 MB (3379323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae43a7dfb488bfdf09941272691a16afeb9a0ec5f2aeb3afb906b9e61d0eea0`  
		Last Modified: Fri, 01 Dec 2023 05:24:18 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8414376f36c8ce530795b6f714715e47f66e1bc7cb691ab3238a1f754acff0`  
		Last Modified: Fri, 01 Dec 2023 05:24:16 GMT  
		Size: 1.5 MB (1472464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fd5188481a93b1bec9a5a4e84c2174bc313afece09bfe0aebe6cb409134d9d7`  
		Last Modified: Fri, 01 Dec 2023 05:25:18 GMT  
		Size: 20.3 MB (20343422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5aeb5fa9d247ed91d69eeca826e1a4c64b267d5610a0b6e043d9114923d6850`  
		Last Modified: Fri, 01 Dec 2023 05:25:15 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1886cc87970999d0a5000856891c3a278d4cbfda201ed058e8e73ba5b3df47f9`  
		Last Modified: Fri, 01 Dec 2023 05:25:15 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.10.5-data`

```console
$ docker pull influxdb@sha256:13c4385d515a821012e54f24b76eb8846546b1ac8b7398236fff2c486f556c64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.10.5-data` - linux; amd64

```console
$ docker pull influxdb@sha256:787e4a9c2839d48627e0d746d626a754b13a0632f2c1ca2c05fcf10271d86ed7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.0 MB (111002715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d87488851bcb341a966dcbf8b43e39ca51a0079127511618ab3958f0114aa4c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:04 GMT
ADD file:35f7caaedc3b6f725dee87eb8d1f2727c04cb21062b5eb7f59801dafced61993 in / 
# Thu, 11 Jan 2024 02:38:05 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:36:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 16:39:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 16:39:30 GMT
ENV INFLUXDB_VERSION=1.10.5-c1.10.5
# Thu, 11 Jan 2024 16:39:40 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb*
# Thu, 11 Jan 2024 16:39:41 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Thu, 11 Jan 2024 16:39:41 GMT
EXPOSE 8086
# Thu, 11 Jan 2024 16:39:41 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jan 2024 16:39:41 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Thu, 11 Jan 2024 16:39:41 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 11 Jan 2024 16:39:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 16:39:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:e455cf41eadb2f19f014361006086cdc5b3de16f3d13bd1d586be63e66c7fc63`  
		Last Modified: Thu, 11 Jan 2024 02:42:47 GMT  
		Size: 55.1 MB (55057723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4531da2f06f2911a5e67446c1ec507acb336afe7130741c6ed12ce442b730f`  
		Last Modified: Thu, 11 Jan 2024 04:45:42 GMT  
		Size: 15.8 MB (15765113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14fb060119b49def67db8ec15d6ffc47c094d5675101637e97e7f06d38aa3fe0`  
		Last Modified: Thu, 11 Jan 2024 16:40:43 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cbae3f13bd83a1e1e8490e41d7c9c1178bfe10bf6e62d7f8c66cdfe4581cb84`  
		Last Modified: Thu, 11 Jan 2024 16:41:31 GMT  
		Size: 40.2 MB (40176292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37765368a964e30ea1acee39a6a8eefc7f3c83d15264c6d14c37d4723c8dd6c5`  
		Last Modified: Thu, 11 Jan 2024 16:41:25 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:863a0da84099146fdc5f70c5e8532cf41d3027e9364b0021e88ba903068b62fa`  
		Last Modified: Thu, 11 Jan 2024 16:41:25 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a2b4327a0b556a9510cf0dde4ea90b848594b15c53419eac41a45c8c29e9ead`  
		Last Modified: Thu, 11 Jan 2024 16:41:25 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.10.5-data-alpine`

```console
$ docker pull influxdb@sha256:2117575b93381be200ddd8ce5a157b8054779e53f106994d10a4f537844c3151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.10.5-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:b2274bb9a14dd05391b921875676302516acdf1ba1bc95dc1b2731a1e4487566
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (44986916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4669f9422cfb1a2783f9a2171e992cf3cdcdd6933edea40131e6436ae11649f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:58 GMT
ADD file:80331a5d882ac8a70763f4b19e06f2e04ea3dca34ae6d92810815b170b3c806c in / 
# Thu, 30 Nov 2023 23:22:59 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 05:22:09 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 01 Dec 2023 05:22:10 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Fri, 01 Dec 2023 05:22:47 GMT
ENV INFLUXDB_VERSION=1.10.5-c1.10.5
# Fri, 01 Dec 2023 05:22:55 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 01 Dec 2023 05:22:55 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Fri, 01 Dec 2023 05:22:55 GMT
EXPOSE 8086
# Fri, 01 Dec 2023 05:22:56 GMT
VOLUME [/var/lib/influxdb]
# Fri, 01 Dec 2023 05:22:56 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Fri, 01 Dec 2023 05:22:56 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Fri, 01 Dec 2023 05:22:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Dec 2023 05:22:56 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:1207c741d8c9b028d98c4006013f9de959da3c55f85b91ed5e4583438a0112ca`  
		Last Modified: Thu, 30 Nov 2023 23:23:40 GMT  
		Size: 3.4 MB (3379323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae43a7dfb488bfdf09941272691a16afeb9a0ec5f2aeb3afb906b9e61d0eea0`  
		Last Modified: Fri, 01 Dec 2023 05:24:18 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8414376f36c8ce530795b6f714715e47f66e1bc7cb691ab3238a1f754acff0`  
		Last Modified: Fri, 01 Dec 2023 05:24:16 GMT  
		Size: 1.5 MB (1472464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4040553c9c4bfc1e84707ed35934a581848951de238f0e2cda33654f4924283`  
		Last Modified: Fri, 01 Dec 2023 05:25:05 GMT  
		Size: 40.1 MB (40133053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71a763104a99899d4d80f18aeab3093f53fc0de2c31e200274764c203be4cfb6`  
		Last Modified: Fri, 01 Dec 2023 05:24:58 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267fb35b58ade3e29f48cd35502ba2842dd86488daa4b941a3561c059f7485df`  
		Last Modified: Fri, 01 Dec 2023 05:24:58 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72ff4725b950867c0001a8e947beddaf7e4cd023407eb75c02e9f716de39dfaa`  
		Last Modified: Fri, 01 Dec 2023 05:24:58 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.10.5-meta`

```console
$ docker pull influxdb@sha256:dc70ca29f4ee113e1c460d7e392414d3f82a5ae240efe0dd2f6f1325b65380e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.10.5-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:97879a03b3a98086d139722c2891877636c6c5b5a37d3c18fec8ce236e740d6a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91202175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8391d280ec8b16479ba90a79f5eed4ed80d1a45de82b7522e9e57331945d0c3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:04 GMT
ADD file:35f7caaedc3b6f725dee87eb8d1f2727c04cb21062b5eb7f59801dafced61993 in / 
# Thu, 11 Jan 2024 02:38:05 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:36:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 16:39:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 16:39:30 GMT
ENV INFLUXDB_VERSION=1.10.5-c1.10.5
# Thu, 11 Jan 2024 16:39:54 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb*
# Thu, 11 Jan 2024 16:39:54 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Thu, 11 Jan 2024 16:39:54 GMT
EXPOSE 8091
# Thu, 11 Jan 2024 16:39:54 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jan 2024 16:39:54 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Thu, 11 Jan 2024 16:39:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 16:39:55 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:e455cf41eadb2f19f014361006086cdc5b3de16f3d13bd1d586be63e66c7fc63`  
		Last Modified: Thu, 11 Jan 2024 02:42:47 GMT  
		Size: 55.1 MB (55057723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4531da2f06f2911a5e67446c1ec507acb336afe7130741c6ed12ce442b730f`  
		Last Modified: Thu, 11 Jan 2024 04:45:42 GMT  
		Size: 15.8 MB (15765113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14fb060119b49def67db8ec15d6ffc47c094d5675101637e97e7f06d38aa3fe0`  
		Last Modified: Thu, 11 Jan 2024 16:40:43 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c154a1dc6c72cd5fc8688e4d19add5818d66369dc39be6391afe15e17acf450d`  
		Last Modified: Thu, 11 Jan 2024 16:41:43 GMT  
		Size: 20.4 MB (20376954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3890e2dabf99776cf28ca1cddf448fa1046ebb37f0a1689e1c4bacb6c5b0e43`  
		Last Modified: Thu, 11 Jan 2024 16:41:40 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:044fdfac94f2536682efb484559f98ba70538541a9dc1380b5af316529c4ae42`  
		Last Modified: Thu, 11 Jan 2024 16:41:40 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.10.5-meta-alpine`

```console
$ docker pull influxdb@sha256:fd3c051c03348866a2698a575e78d630c420aa759c96b417a4297bcc5cf4b8a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.10.5-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:c142d33c1b2c956d693f0b6dc486724956053151e8977511f708991200128c1b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25196081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556704a29b056fc7cba5a69cadbb1360795209c5ee02f318e42d607bd4ec55d9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:58 GMT
ADD file:80331a5d882ac8a70763f4b19e06f2e04ea3dca34ae6d92810815b170b3c806c in / 
# Thu, 30 Nov 2023 23:22:59 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 05:22:09 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 01 Dec 2023 05:22:10 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Fri, 01 Dec 2023 05:22:47 GMT
ENV INFLUXDB_VERSION=1.10.5-c1.10.5
# Fri, 01 Dec 2023 05:23:07 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 01 Dec 2023 05:23:07 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Fri, 01 Dec 2023 05:23:07 GMT
EXPOSE 8091
# Fri, 01 Dec 2023 05:23:07 GMT
VOLUME [/var/lib/influxdb]
# Fri, 01 Dec 2023 05:23:07 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Fri, 01 Dec 2023 05:23:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Dec 2023 05:23:07 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:1207c741d8c9b028d98c4006013f9de959da3c55f85b91ed5e4583438a0112ca`  
		Last Modified: Thu, 30 Nov 2023 23:23:40 GMT  
		Size: 3.4 MB (3379323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae43a7dfb488bfdf09941272691a16afeb9a0ec5f2aeb3afb906b9e61d0eea0`  
		Last Modified: Fri, 01 Dec 2023 05:24:18 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8414376f36c8ce530795b6f714715e47f66e1bc7cb691ab3238a1f754acff0`  
		Last Modified: Fri, 01 Dec 2023 05:24:16 GMT  
		Size: 1.5 MB (1472464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fd5188481a93b1bec9a5a4e84c2174bc313afece09bfe0aebe6cb409134d9d7`  
		Last Modified: Fri, 01 Dec 2023 05:25:18 GMT  
		Size: 20.3 MB (20343422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5aeb5fa9d247ed91d69eeca826e1a4c64b267d5610a0b6e043d9114923d6850`  
		Last Modified: Fri, 01 Dec 2023 05:25:15 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1886cc87970999d0a5000856891c3a278d4cbfda201ed058e8e73ba5b3df47f9`  
		Last Modified: Fri, 01 Dec 2023 05:25:15 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.11-data`

```console
$ docker pull influxdb@sha256:8707498f7e6e5295ff43edded344ca7632da9ef9c1ea235814e7e1acdd42f290
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.11-data` - linux; amd64

```console
$ docker pull influxdb@sha256:17dfecbb163c68108f43ac5c23f265cce16ea6fed04bb1048b14960d73ca744a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.8 MB (113786103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa6a2cf010444640834b611393c9a3b5814f06ced850544b423e18a616cc75c7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:42 GMT
ADD file:077a3156bd8271f26498ae6ac3800e68a42b9277581bc81eea31fec1a123dca5 in / 
# Thu, 11 Jan 2024 02:37:43 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:35:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 16:40:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 16:40:01 GMT
ENV INFLUXDB_VERSION=1.11.3-c1.11.3
# Thu, 11 Jan 2024 16:40:05 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb*
# Thu, 11 Jan 2024 16:40:05 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Thu, 11 Jan 2024 16:40:05 GMT
EXPOSE 8086
# Thu, 11 Jan 2024 16:40:06 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jan 2024 16:40:06 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Thu, 11 Jan 2024 16:40:06 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 11 Jan 2024 16:40:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 16:40:06 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:1b13d4e1a46e5e969702ec92b7c787c1b6891bff7c21ad378ff6dbc9e751d5d4`  
		Last Modified: Thu, 11 Jan 2024 02:42:04 GMT  
		Size: 49.6 MB (49561490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c74526957fc2157e8b0989072dc99b9582b398c12d1dcd40270fd76231bab0c`  
		Last Modified: Thu, 11 Jan 2024 04:44:35 GMT  
		Size: 24.0 MB (24046494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5958415e0d1d6072b599869a9b58a873d1ee96f6aa362f92e7bc2ecf9da8c0`  
		Last Modified: Thu, 11 Jan 2024 16:41:52 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee37828be18ed73d0047ce2501ed393f76a2c13ea2c598f65da79c681d315d58`  
		Last Modified: Thu, 11 Jan 2024 16:41:59 GMT  
		Size: 40.2 MB (40174530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4f1b075dee1464e4ae1249f3cd96481fb71fd2081a6a2a204e4b0254a55535`  
		Last Modified: Thu, 11 Jan 2024 16:41:52 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7247dcdea2257063c803dc4a356c0e9daf50ffa5da23e2562c137262c0d05ab1`  
		Last Modified: Thu, 11 Jan 2024 16:41:52 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906b1749c4be297bbaa8985ae59f5b8132603068eb6ab345d859e589e046753e`  
		Last Modified: Thu, 11 Jan 2024 16:41:52 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.11-data-alpine`

```console
$ docker pull influxdb@sha256:5d2e41d03599107c1b7bb8e93d98be9decedba33cf00bc6270bd179aa348062f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.11-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:accf78709bf197ec85c484344ae50e3c4e2e262b5e08cc84051a509ce4d29dce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44943531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d14085875c021a12bc72c5b3a486b8727e7da20ed9691bf0fc9c51d401563a3d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 05:23:13 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 01 Dec 2023 05:23:14 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Fri, 01 Dec 2023 05:23:14 GMT
ENV INFLUXDB_VERSION=1.11.3-c1.11.3
# Fri, 01 Dec 2023 05:23:22 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 01 Dec 2023 05:23:22 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Fri, 01 Dec 2023 05:23:22 GMT
EXPOSE 8086
# Fri, 01 Dec 2023 05:23:22 GMT
VOLUME [/var/lib/influxdb]
# Fri, 01 Dec 2023 05:23:22 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Fri, 01 Dec 2023 05:23:22 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Fri, 01 Dec 2023 05:23:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Dec 2023 05:23:22 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703e958f39c4082f015dd7de32b1c116ef56e1e54010a31e991ec0c10e7feecc`  
		Last Modified: Fri, 01 Dec 2023 05:25:29 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21403be5081e983bab2b48d88aa092a687b44d464799ea2033b584e61ec6de09`  
		Last Modified: Fri, 01 Dec 2023 05:25:28 GMT  
		Size: 1.4 MB (1407317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b397ebab285ba671c9f5fa0861b0e0a9d824e16299cedbcbf07b15952030a8`  
		Last Modified: Fri, 01 Dec 2023 05:25:33 GMT  
		Size: 40.1 MB (40131720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29b0088fecc6eb721680a958af57057f2d7183f9475855d8cd4717d25021664`  
		Last Modified: Fri, 01 Dec 2023 05:25:27 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4858a056e3961006449273013b35996658e2ecaf7b7cc3a09bb3c120fe25ee0c`  
		Last Modified: Fri, 01 Dec 2023 05:25:27 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ce439f9a08f0e2af550f08b78998c66ed4e0980a265cdaecb5fda255d0b265`  
		Last Modified: Fri, 01 Dec 2023 05:25:27 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.11-meta`

```console
$ docker pull influxdb@sha256:39491e0d78014ece14e241ad0395da24a80f1b6739b8d7045a849e2bbb7544a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.11-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:3085acab4cd3a44b26c6d4b1d08e9088d31dbc8e137fb6f90aafd957045368c4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.9 MB (93937741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7087f9d9fbc50da7323c5413683b11aca3e7edade5fd7bf9e2bc33d407650346`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:42 GMT
ADD file:077a3156bd8271f26498ae6ac3800e68a42b9277581bc81eea31fec1a123dca5 in / 
# Thu, 11 Jan 2024 02:37:43 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:35:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 16:40:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 16:40:01 GMT
ENV INFLUXDB_VERSION=1.11.3-c1.11.3
# Thu, 11 Jan 2024 16:40:14 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb*
# Thu, 11 Jan 2024 16:40:14 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Thu, 11 Jan 2024 16:40:14 GMT
EXPOSE 8091
# Thu, 11 Jan 2024 16:40:14 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jan 2024 16:40:14 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Thu, 11 Jan 2024 16:40:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 16:40:14 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:1b13d4e1a46e5e969702ec92b7c787c1b6891bff7c21ad378ff6dbc9e751d5d4`  
		Last Modified: Thu, 11 Jan 2024 02:42:04 GMT  
		Size: 49.6 MB (49561490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c74526957fc2157e8b0989072dc99b9582b398c12d1dcd40270fd76231bab0c`  
		Last Modified: Thu, 11 Jan 2024 04:44:35 GMT  
		Size: 24.0 MB (24046494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5958415e0d1d6072b599869a9b58a873d1ee96f6aa362f92e7bc2ecf9da8c0`  
		Last Modified: Thu, 11 Jan 2024 16:41:52 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dec5217bfb321df005c6329d68a5ea610254de07acb3a0c4db8418d6abf83b99`  
		Last Modified: Thu, 11 Jan 2024 16:42:13 GMT  
		Size: 20.3 MB (20327375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:042744dc62403c05d718f00cba1cdaa54773499e11735aae72e532cd9d96db6a`  
		Last Modified: Thu, 11 Jan 2024 16:42:10 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c0975294d218a13fb142be9984117157ead3ebe89b433c3c8822fb707170651`  
		Last Modified: Thu, 11 Jan 2024 16:42:10 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.11-meta-alpine`

```console
$ docker pull influxdb@sha256:8f9f348b110f0a12099a449f768a2993d3ffab9596fc8f545c3c814882d3248a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.11-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:1abaf2e0481c3b6176b43b5620552963ad59b92197e354b5eea6775b3b06500d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25099941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c132f5cebcf3c9ed13437b287eae518238bd887eae2135bbff4b82ce19a2333`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 05:23:13 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 01 Dec 2023 05:23:14 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Fri, 01 Dec 2023 05:23:14 GMT
ENV INFLUXDB_VERSION=1.11.3-c1.11.3
# Fri, 01 Dec 2023 05:23:35 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 01 Dec 2023 05:23:35 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Fri, 01 Dec 2023 05:23:35 GMT
EXPOSE 8091
# Fri, 01 Dec 2023 05:23:35 GMT
VOLUME [/var/lib/influxdb]
# Fri, 01 Dec 2023 05:23:35 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Fri, 01 Dec 2023 05:23:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Dec 2023 05:23:35 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703e958f39c4082f015dd7de32b1c116ef56e1e54010a31e991ec0c10e7feecc`  
		Last Modified: Fri, 01 Dec 2023 05:25:29 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21403be5081e983bab2b48d88aa092a687b44d464799ea2033b584e61ec6de09`  
		Last Modified: Fri, 01 Dec 2023 05:25:28 GMT  
		Size: 1.4 MB (1407317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdcfb1196e9a462be1d0a83f526ed43192b36f99d9b16538258a10fe9c2b7a60`  
		Last Modified: Fri, 01 Dec 2023 05:25:47 GMT  
		Size: 20.3 MB (20289329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f3f0c25e3bd05ca81684a24557be6338728f987476999d17fe3c62693d1efc8`  
		Last Modified: Fri, 01 Dec 2023 05:25:43 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af910e4fa040e0a72ea11e4391eb85320430043f85cf72170a886fff9f4c3671`  
		Last Modified: Fri, 01 Dec 2023 05:25:43 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.11.3-data`

```console
$ docker pull influxdb@sha256:8707498f7e6e5295ff43edded344ca7632da9ef9c1ea235814e7e1acdd42f290
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.11.3-data` - linux; amd64

```console
$ docker pull influxdb@sha256:17dfecbb163c68108f43ac5c23f265cce16ea6fed04bb1048b14960d73ca744a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.8 MB (113786103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa6a2cf010444640834b611393c9a3b5814f06ced850544b423e18a616cc75c7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:42 GMT
ADD file:077a3156bd8271f26498ae6ac3800e68a42b9277581bc81eea31fec1a123dca5 in / 
# Thu, 11 Jan 2024 02:37:43 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:35:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 16:40:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 16:40:01 GMT
ENV INFLUXDB_VERSION=1.11.3-c1.11.3
# Thu, 11 Jan 2024 16:40:05 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb*
# Thu, 11 Jan 2024 16:40:05 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Thu, 11 Jan 2024 16:40:05 GMT
EXPOSE 8086
# Thu, 11 Jan 2024 16:40:06 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jan 2024 16:40:06 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Thu, 11 Jan 2024 16:40:06 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 11 Jan 2024 16:40:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 16:40:06 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:1b13d4e1a46e5e969702ec92b7c787c1b6891bff7c21ad378ff6dbc9e751d5d4`  
		Last Modified: Thu, 11 Jan 2024 02:42:04 GMT  
		Size: 49.6 MB (49561490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c74526957fc2157e8b0989072dc99b9582b398c12d1dcd40270fd76231bab0c`  
		Last Modified: Thu, 11 Jan 2024 04:44:35 GMT  
		Size: 24.0 MB (24046494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5958415e0d1d6072b599869a9b58a873d1ee96f6aa362f92e7bc2ecf9da8c0`  
		Last Modified: Thu, 11 Jan 2024 16:41:52 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee37828be18ed73d0047ce2501ed393f76a2c13ea2c598f65da79c681d315d58`  
		Last Modified: Thu, 11 Jan 2024 16:41:59 GMT  
		Size: 40.2 MB (40174530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4f1b075dee1464e4ae1249f3cd96481fb71fd2081a6a2a204e4b0254a55535`  
		Last Modified: Thu, 11 Jan 2024 16:41:52 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7247dcdea2257063c803dc4a356c0e9daf50ffa5da23e2562c137262c0d05ab1`  
		Last Modified: Thu, 11 Jan 2024 16:41:52 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906b1749c4be297bbaa8985ae59f5b8132603068eb6ab345d859e589e046753e`  
		Last Modified: Thu, 11 Jan 2024 16:41:52 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.11.3-data-alpine`

```console
$ docker pull influxdb@sha256:5d2e41d03599107c1b7bb8e93d98be9decedba33cf00bc6270bd179aa348062f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.11.3-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:accf78709bf197ec85c484344ae50e3c4e2e262b5e08cc84051a509ce4d29dce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44943531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d14085875c021a12bc72c5b3a486b8727e7da20ed9691bf0fc9c51d401563a3d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 05:23:13 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 01 Dec 2023 05:23:14 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Fri, 01 Dec 2023 05:23:14 GMT
ENV INFLUXDB_VERSION=1.11.3-c1.11.3
# Fri, 01 Dec 2023 05:23:22 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 01 Dec 2023 05:23:22 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Fri, 01 Dec 2023 05:23:22 GMT
EXPOSE 8086
# Fri, 01 Dec 2023 05:23:22 GMT
VOLUME [/var/lib/influxdb]
# Fri, 01 Dec 2023 05:23:22 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Fri, 01 Dec 2023 05:23:22 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Fri, 01 Dec 2023 05:23:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Dec 2023 05:23:22 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703e958f39c4082f015dd7de32b1c116ef56e1e54010a31e991ec0c10e7feecc`  
		Last Modified: Fri, 01 Dec 2023 05:25:29 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21403be5081e983bab2b48d88aa092a687b44d464799ea2033b584e61ec6de09`  
		Last Modified: Fri, 01 Dec 2023 05:25:28 GMT  
		Size: 1.4 MB (1407317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b397ebab285ba671c9f5fa0861b0e0a9d824e16299cedbcbf07b15952030a8`  
		Last Modified: Fri, 01 Dec 2023 05:25:33 GMT  
		Size: 40.1 MB (40131720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29b0088fecc6eb721680a958af57057f2d7183f9475855d8cd4717d25021664`  
		Last Modified: Fri, 01 Dec 2023 05:25:27 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4858a056e3961006449273013b35996658e2ecaf7b7cc3a09bb3c120fe25ee0c`  
		Last Modified: Fri, 01 Dec 2023 05:25:27 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ce439f9a08f0e2af550f08b78998c66ed4e0980a265cdaecb5fda255d0b265`  
		Last Modified: Fri, 01 Dec 2023 05:25:27 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.11.3-meta`

```console
$ docker pull influxdb@sha256:39491e0d78014ece14e241ad0395da24a80f1b6739b8d7045a849e2bbb7544a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.11.3-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:3085acab4cd3a44b26c6d4b1d08e9088d31dbc8e137fb6f90aafd957045368c4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.9 MB (93937741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7087f9d9fbc50da7323c5413683b11aca3e7edade5fd7bf9e2bc33d407650346`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:42 GMT
ADD file:077a3156bd8271f26498ae6ac3800e68a42b9277581bc81eea31fec1a123dca5 in / 
# Thu, 11 Jan 2024 02:37:43 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:35:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 16:40:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 16:40:01 GMT
ENV INFLUXDB_VERSION=1.11.3-c1.11.3
# Thu, 11 Jan 2024 16:40:14 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb*
# Thu, 11 Jan 2024 16:40:14 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Thu, 11 Jan 2024 16:40:14 GMT
EXPOSE 8091
# Thu, 11 Jan 2024 16:40:14 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jan 2024 16:40:14 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Thu, 11 Jan 2024 16:40:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 16:40:14 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:1b13d4e1a46e5e969702ec92b7c787c1b6891bff7c21ad378ff6dbc9e751d5d4`  
		Last Modified: Thu, 11 Jan 2024 02:42:04 GMT  
		Size: 49.6 MB (49561490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c74526957fc2157e8b0989072dc99b9582b398c12d1dcd40270fd76231bab0c`  
		Last Modified: Thu, 11 Jan 2024 04:44:35 GMT  
		Size: 24.0 MB (24046494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5958415e0d1d6072b599869a9b58a873d1ee96f6aa362f92e7bc2ecf9da8c0`  
		Last Modified: Thu, 11 Jan 2024 16:41:52 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dec5217bfb321df005c6329d68a5ea610254de07acb3a0c4db8418d6abf83b99`  
		Last Modified: Thu, 11 Jan 2024 16:42:13 GMT  
		Size: 20.3 MB (20327375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:042744dc62403c05d718f00cba1cdaa54773499e11735aae72e532cd9d96db6a`  
		Last Modified: Thu, 11 Jan 2024 16:42:10 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c0975294d218a13fb142be9984117157ead3ebe89b433c3c8822fb707170651`  
		Last Modified: Thu, 11 Jan 2024 16:42:10 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.11.3-meta-alpine`

```console
$ docker pull influxdb@sha256:8f9f348b110f0a12099a449f768a2993d3ffab9596fc8f545c3c814882d3248a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.11.3-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:1abaf2e0481c3b6176b43b5620552963ad59b92197e354b5eea6775b3b06500d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25099941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c132f5cebcf3c9ed13437b287eae518238bd887eae2135bbff4b82ce19a2333`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 05:23:13 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 01 Dec 2023 05:23:14 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Fri, 01 Dec 2023 05:23:14 GMT
ENV INFLUXDB_VERSION=1.11.3-c1.11.3
# Fri, 01 Dec 2023 05:23:35 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 01 Dec 2023 05:23:35 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Fri, 01 Dec 2023 05:23:35 GMT
EXPOSE 8091
# Fri, 01 Dec 2023 05:23:35 GMT
VOLUME [/var/lib/influxdb]
# Fri, 01 Dec 2023 05:23:35 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Fri, 01 Dec 2023 05:23:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Dec 2023 05:23:35 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703e958f39c4082f015dd7de32b1c116ef56e1e54010a31e991ec0c10e7feecc`  
		Last Modified: Fri, 01 Dec 2023 05:25:29 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21403be5081e983bab2b48d88aa092a687b44d464799ea2033b584e61ec6de09`  
		Last Modified: Fri, 01 Dec 2023 05:25:28 GMT  
		Size: 1.4 MB (1407317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdcfb1196e9a462be1d0a83f526ed43192b36f99d9b16538258a10fe9c2b7a60`  
		Last Modified: Fri, 01 Dec 2023 05:25:47 GMT  
		Size: 20.3 MB (20289329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f3f0c25e3bd05ca81684a24557be6338728f987476999d17fe3c62693d1efc8`  
		Last Modified: Fri, 01 Dec 2023 05:25:43 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af910e4fa040e0a72ea11e4391eb85320430043f85cf72170a886fff9f4c3671`  
		Last Modified: Fri, 01 Dec 2023 05:25:43 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8`

```console
$ docker pull influxdb@sha256:54ef9c1b5c0f4f803c4fa712592b61f0e3294eadb9d6b8d7259e50344e412cd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.8` - linux; amd64

```console
$ docker pull influxdb@sha256:7540b4a77734e385d34baef27ad92ac86790b1c21de4fb464563e9acf4390f12
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125712153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:102ea8b9b6007ee4ba155a622136a2e6fed152d785d765721b819d534c50cb3c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:04 GMT
ADD file:35f7caaedc3b6f725dee87eb8d1f2727c04cb21062b5eb7f59801dafced61993 in / 
# Thu, 11 Jan 2024 02:38:05 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:36:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 16:39:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 16:39:00 GMT
ENV INFLUXDB_VERSION=1.8.10
# Thu, 11 Jan 2024 16:39:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Thu, 11 Jan 2024 16:39:05 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Thu, 11 Jan 2024 16:39:05 GMT
EXPOSE 8086
# Thu, 11 Jan 2024 16:39:05 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jan 2024 16:39:05 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Thu, 11 Jan 2024 16:39:05 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 11 Jan 2024 16:39:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 16:39:05 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:e455cf41eadb2f19f014361006086cdc5b3de16f3d13bd1d586be63e66c7fc63`  
		Last Modified: Thu, 11 Jan 2024 02:42:47 GMT  
		Size: 55.1 MB (55057723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4531da2f06f2911a5e67446c1ec507acb336afe7130741c6ed12ce442b730f`  
		Last Modified: Thu, 11 Jan 2024 04:45:42 GMT  
		Size: 15.8 MB (15765113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14fb060119b49def67db8ec15d6ffc47c094d5675101637e97e7f06d38aa3fe0`  
		Last Modified: Thu, 11 Jan 2024 16:40:43 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d92d5e56ddc08be007cb601208ee9573f206fc7edd6b1d452a43724fb27305ad`  
		Last Modified: Thu, 11 Jan 2024 16:40:50 GMT  
		Size: 54.9 MB (54885784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b74d89cfc2c5aa038fea30844e3c1abe1f1f15351037d06e593ba8b10c2183a`  
		Last Modified: Thu, 11 Jan 2024 16:40:43 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5108252030e8040d7078d1d7cdcf9307d8a0339b944c06e0a6bef2210a5cf9`  
		Last Modified: Thu, 11 Jan 2024 16:40:43 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e8e0968724fea8f49fa0a3ddb7195021f56b6395db57e58fd7b91f9efd98b9b`  
		Last Modified: Thu, 11 Jan 2024 16:40:44 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.8` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:0970ff171a37e4bfff6bae2f2128544b19da4fc1248db2f3573588f1f4705b48
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.7 MB (116712702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eba452362d4b437e31a38b5561b83c65a87feae0ba3c7cd10ef153202772e9db`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 11 Jan 2024 02:42:21 GMT
ADD file:06c355196a858f2594c761bea3314e053018c78a4b06eabe168db940f6c18e26 in / 
# Thu, 11 Jan 2024 02:42:21 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:16:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 20:29:43 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 20:29:43 GMT
ENV INFLUXDB_VERSION=1.8.10
# Thu, 11 Jan 2024 20:29:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Thu, 11 Jan 2024 20:29:55 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Thu, 11 Jan 2024 20:29:56 GMT
EXPOSE 8086
# Thu, 11 Jan 2024 20:29:56 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jan 2024 20:29:57 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Thu, 11 Jan 2024 20:29:57 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 11 Jan 2024 20:29:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 20:29:58 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:6c8fc6a3ed50d9d1c829e556b5efd4ca23cd5d51d5dcdec2a7a70b583673ef89`  
		Last Modified: Thu, 11 Jan 2024 02:49:02 GMT  
		Size: 50.2 MB (50215530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc92f863388ea7a660a09ac1581e426ed098ac1fe970d4ad13e7ac5a7d728ee3`  
		Last Modified: Thu, 11 Jan 2024 03:30:20 GMT  
		Size: 14.9 MB (14880496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e4e3086bc30519aade8c9e8d7966109d9345b83d8e2fd35c8ff632f5f92669`  
		Last Modified: Thu, 11 Jan 2024 20:30:10 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66d83b40a5be6e594300f2608c49180f9c74569c45a9ff435c87db8fc1a73107`  
		Last Modified: Thu, 11 Jan 2024 20:30:19 GMT  
		Size: 51.6 MB (51613142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866b3d7b21c383d22352547c1f4bdded407e281d4c73e4af84df3c024c26cbbb`  
		Last Modified: Thu, 11 Jan 2024 20:30:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7652e50611f93562a2d44eaeafacc2eda302e2a9f58986a328a72336fca98ae`  
		Last Modified: Thu, 11 Jan 2024 20:30:10 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0383ae6beac915b86b63cbe74fef1cb7190db185f88713e8ae30f0dafa9580ea`  
		Last Modified: Thu, 11 Jan 2024 20:30:11 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:9a4158968544f57284caec0181a28d17d38c8d35594a8863ab3391f6c8962178
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120692186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:385886da20d2deee189b11edf75e1f98373ef056e7b46099570ce8a32d5830ee`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:51 GMT
ADD file:8fb65cadfd211811589ee046d0fbd69d1fe11461b0c0c154a7650bf97307b857 in / 
# Thu, 11 Jan 2024 02:40:51 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 09:26:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 12:57:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 12:57:28 GMT
ENV INFLUXDB_VERSION=1.8.10
# Thu, 11 Jan 2024 12:57:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Thu, 11 Jan 2024 12:57:32 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Thu, 11 Jan 2024 12:57:32 GMT
EXPOSE 8086
# Thu, 11 Jan 2024 12:57:33 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jan 2024 12:57:33 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Thu, 11 Jan 2024 12:57:33 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 11 Jan 2024 12:57:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 12:57:33 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:cf83973c4a096cce9f37c421ad6f19cf1ebf7ae4d8ea98dac4913bd2aef08d1c`  
		Last Modified: Thu, 11 Jan 2024 02:44:25 GMT  
		Size: 53.7 MB (53707847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aebf2a961043d6b9dd703d0a485e216a2e302edf2e2525f7f410987d26905e71`  
		Last Modified: Thu, 11 Jan 2024 09:35:03 GMT  
		Size: 15.8 MB (15750711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc3fb2c81869796eb5cf4f89f67d3497cd3cd7b1523b9701902a8543d45d624e`  
		Last Modified: Thu, 11 Jan 2024 12:57:45 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c259eee1defb898bd61f51278feae5028c4db31c5c8cd04597cc6ae059e77c2`  
		Last Modified: Thu, 11 Jan 2024 12:57:50 GMT  
		Size: 51.2 MB (51230096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca69065a2c11a59549e100dcefb6c67f8cc0b959684cf46c6feb0f93a77f7fcf`  
		Last Modified: Thu, 11 Jan 2024 12:57:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff63496fe55e3c05d9e31677ec3245c5f9707bf9ec54ff423fd1a06586055b3e`  
		Last Modified: Thu, 11 Jan 2024 12:57:45 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:546db9d17eb60dfbdc6a81dc9c1f8b08992d8bf4255088bb45f21aaaeeb84373`  
		Last Modified: Thu, 11 Jan 2024 12:57:45 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8-alpine`

```console
$ docker pull influxdb@sha256:d29e9e5a816afcc5ab2cc62f82e86b72089339a35d80dd9f72a0754343d30817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.8-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:83571dac44bd2bc8a8ac8dcb65d011361026083bfb2e3bd991fd8792fe429750
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59500484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06975d300c41b2b50a1e5c0666d30bdabacbeb03a9adb48fee4490dcb673f4af`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:58 GMT
ADD file:80331a5d882ac8a70763f4b19e06f2e04ea3dca34ae6d92810815b170b3c806c in / 
# Thu, 30 Nov 2023 23:22:59 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 05:22:09 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 01 Dec 2023 05:22:10 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Fri, 01 Dec 2023 05:22:10 GMT
ENV INFLUXDB_VERSION=1.8.10
# Fri, 01 Dec 2023 05:22:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     chmod +x /usr/src/influxdb-*/influx              /usr/src/influxdb-*/influx_inspect              /usr/src/influxdb-*/influx_stress              /usr/src/influxdb-*/influxd &&    mv /usr/src/influxdb-*/influx        /usr/src/influxdb-*/influx_inspect        /usr/src/influxdb-*/influx_stress         /usr/src/influxdb-*/influxd        /usr/bin/ &&    gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 01 Dec 2023 05:22:16 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Fri, 01 Dec 2023 05:22:16 GMT
EXPOSE 8086
# Fri, 01 Dec 2023 05:22:16 GMT
VOLUME [/var/lib/influxdb]
# Fri, 01 Dec 2023 05:22:16 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Fri, 01 Dec 2023 05:22:16 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Fri, 01 Dec 2023 05:22:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Dec 2023 05:22:16 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:1207c741d8c9b028d98c4006013f9de959da3c55f85b91ed5e4583438a0112ca`  
		Last Modified: Thu, 30 Nov 2023 23:23:40 GMT  
		Size: 3.4 MB (3379323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae43a7dfb488bfdf09941272691a16afeb9a0ec5f2aeb3afb906b9e61d0eea0`  
		Last Modified: Fri, 01 Dec 2023 05:24:18 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8414376f36c8ce530795b6f714715e47f66e1bc7cb691ab3238a1f754acff0`  
		Last Modified: Fri, 01 Dec 2023 05:24:16 GMT  
		Size: 1.5 MB (1472464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d71b51e5d30bc3ced7a7d0e8decbb28c57920dd18985367fdf870c64c9e94533`  
		Last Modified: Fri, 01 Dec 2023 05:24:24 GMT  
		Size: 54.6 MB (54646682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de6bcb56167953acb95e96c9fab8e4ea8cc8ddbdec2d5b3427ba3875607cdce`  
		Last Modified: Fri, 01 Dec 2023 05:24:16 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ccc2ba70e548cfa1950081f6cfe9cdb0355ccefcf958dc77539528bf5cfa5eb`  
		Last Modified: Fri, 01 Dec 2023 05:24:16 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae809d1684b67ab4c53382693c4ff531062ee6710212cd357bc7d60fd6adc576`  
		Last Modified: Fri, 01 Dec 2023 05:24:18 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.10`

```console
$ docker pull influxdb@sha256:54ef9c1b5c0f4f803c4fa712592b61f0e3294eadb9d6b8d7259e50344e412cd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.8.10` - linux; amd64

```console
$ docker pull influxdb@sha256:7540b4a77734e385d34baef27ad92ac86790b1c21de4fb464563e9acf4390f12
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125712153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:102ea8b9b6007ee4ba155a622136a2e6fed152d785d765721b819d534c50cb3c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:04 GMT
ADD file:35f7caaedc3b6f725dee87eb8d1f2727c04cb21062b5eb7f59801dafced61993 in / 
# Thu, 11 Jan 2024 02:38:05 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:36:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 16:39:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 16:39:00 GMT
ENV INFLUXDB_VERSION=1.8.10
# Thu, 11 Jan 2024 16:39:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Thu, 11 Jan 2024 16:39:05 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Thu, 11 Jan 2024 16:39:05 GMT
EXPOSE 8086
# Thu, 11 Jan 2024 16:39:05 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jan 2024 16:39:05 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Thu, 11 Jan 2024 16:39:05 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 11 Jan 2024 16:39:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 16:39:05 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:e455cf41eadb2f19f014361006086cdc5b3de16f3d13bd1d586be63e66c7fc63`  
		Last Modified: Thu, 11 Jan 2024 02:42:47 GMT  
		Size: 55.1 MB (55057723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4531da2f06f2911a5e67446c1ec507acb336afe7130741c6ed12ce442b730f`  
		Last Modified: Thu, 11 Jan 2024 04:45:42 GMT  
		Size: 15.8 MB (15765113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14fb060119b49def67db8ec15d6ffc47c094d5675101637e97e7f06d38aa3fe0`  
		Last Modified: Thu, 11 Jan 2024 16:40:43 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d92d5e56ddc08be007cb601208ee9573f206fc7edd6b1d452a43724fb27305ad`  
		Last Modified: Thu, 11 Jan 2024 16:40:50 GMT  
		Size: 54.9 MB (54885784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b74d89cfc2c5aa038fea30844e3c1abe1f1f15351037d06e593ba8b10c2183a`  
		Last Modified: Thu, 11 Jan 2024 16:40:43 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5108252030e8040d7078d1d7cdcf9307d8a0339b944c06e0a6bef2210a5cf9`  
		Last Modified: Thu, 11 Jan 2024 16:40:43 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e8e0968724fea8f49fa0a3ddb7195021f56b6395db57e58fd7b91f9efd98b9b`  
		Last Modified: Thu, 11 Jan 2024 16:40:44 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.8.10` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:0970ff171a37e4bfff6bae2f2128544b19da4fc1248db2f3573588f1f4705b48
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.7 MB (116712702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eba452362d4b437e31a38b5561b83c65a87feae0ba3c7cd10ef153202772e9db`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 11 Jan 2024 02:42:21 GMT
ADD file:06c355196a858f2594c761bea3314e053018c78a4b06eabe168db940f6c18e26 in / 
# Thu, 11 Jan 2024 02:42:21 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:16:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 20:29:43 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 20:29:43 GMT
ENV INFLUXDB_VERSION=1.8.10
# Thu, 11 Jan 2024 20:29:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Thu, 11 Jan 2024 20:29:55 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Thu, 11 Jan 2024 20:29:56 GMT
EXPOSE 8086
# Thu, 11 Jan 2024 20:29:56 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jan 2024 20:29:57 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Thu, 11 Jan 2024 20:29:57 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 11 Jan 2024 20:29:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 20:29:58 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:6c8fc6a3ed50d9d1c829e556b5efd4ca23cd5d51d5dcdec2a7a70b583673ef89`  
		Last Modified: Thu, 11 Jan 2024 02:49:02 GMT  
		Size: 50.2 MB (50215530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc92f863388ea7a660a09ac1581e426ed098ac1fe970d4ad13e7ac5a7d728ee3`  
		Last Modified: Thu, 11 Jan 2024 03:30:20 GMT  
		Size: 14.9 MB (14880496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e4e3086bc30519aade8c9e8d7966109d9345b83d8e2fd35c8ff632f5f92669`  
		Last Modified: Thu, 11 Jan 2024 20:30:10 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66d83b40a5be6e594300f2608c49180f9c74569c45a9ff435c87db8fc1a73107`  
		Last Modified: Thu, 11 Jan 2024 20:30:19 GMT  
		Size: 51.6 MB (51613142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866b3d7b21c383d22352547c1f4bdded407e281d4c73e4af84df3c024c26cbbb`  
		Last Modified: Thu, 11 Jan 2024 20:30:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7652e50611f93562a2d44eaeafacc2eda302e2a9f58986a328a72336fca98ae`  
		Last Modified: Thu, 11 Jan 2024 20:30:10 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0383ae6beac915b86b63cbe74fef1cb7190db185f88713e8ae30f0dafa9580ea`  
		Last Modified: Thu, 11 Jan 2024 20:30:11 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.8.10` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:9a4158968544f57284caec0181a28d17d38c8d35594a8863ab3391f6c8962178
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120692186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:385886da20d2deee189b11edf75e1f98373ef056e7b46099570ce8a32d5830ee`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:51 GMT
ADD file:8fb65cadfd211811589ee046d0fbd69d1fe11461b0c0c154a7650bf97307b857 in / 
# Thu, 11 Jan 2024 02:40:51 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 09:26:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 12:57:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 12:57:28 GMT
ENV INFLUXDB_VERSION=1.8.10
# Thu, 11 Jan 2024 12:57:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Thu, 11 Jan 2024 12:57:32 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Thu, 11 Jan 2024 12:57:32 GMT
EXPOSE 8086
# Thu, 11 Jan 2024 12:57:33 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jan 2024 12:57:33 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Thu, 11 Jan 2024 12:57:33 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 11 Jan 2024 12:57:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 12:57:33 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:cf83973c4a096cce9f37c421ad6f19cf1ebf7ae4d8ea98dac4913bd2aef08d1c`  
		Last Modified: Thu, 11 Jan 2024 02:44:25 GMT  
		Size: 53.7 MB (53707847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aebf2a961043d6b9dd703d0a485e216a2e302edf2e2525f7f410987d26905e71`  
		Last Modified: Thu, 11 Jan 2024 09:35:03 GMT  
		Size: 15.8 MB (15750711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc3fb2c81869796eb5cf4f89f67d3497cd3cd7b1523b9701902a8543d45d624e`  
		Last Modified: Thu, 11 Jan 2024 12:57:45 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c259eee1defb898bd61f51278feae5028c4db31c5c8cd04597cc6ae059e77c2`  
		Last Modified: Thu, 11 Jan 2024 12:57:50 GMT  
		Size: 51.2 MB (51230096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca69065a2c11a59549e100dcefb6c67f8cc0b959684cf46c6feb0f93a77f7fcf`  
		Last Modified: Thu, 11 Jan 2024 12:57:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff63496fe55e3c05d9e31677ec3245c5f9707bf9ec54ff423fd1a06586055b3e`  
		Last Modified: Thu, 11 Jan 2024 12:57:45 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:546db9d17eb60dfbdc6a81dc9c1f8b08992d8bf4255088bb45f21aaaeeb84373`  
		Last Modified: Thu, 11 Jan 2024 12:57:45 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.10-alpine`

```console
$ docker pull influxdb@sha256:d29e9e5a816afcc5ab2cc62f82e86b72089339a35d80dd9f72a0754343d30817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.8.10-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:83571dac44bd2bc8a8ac8dcb65d011361026083bfb2e3bd991fd8792fe429750
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59500484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06975d300c41b2b50a1e5c0666d30bdabacbeb03a9adb48fee4490dcb673f4af`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:58 GMT
ADD file:80331a5d882ac8a70763f4b19e06f2e04ea3dca34ae6d92810815b170b3c806c in / 
# Thu, 30 Nov 2023 23:22:59 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 05:22:09 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 01 Dec 2023 05:22:10 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Fri, 01 Dec 2023 05:22:10 GMT
ENV INFLUXDB_VERSION=1.8.10
# Fri, 01 Dec 2023 05:22:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     chmod +x /usr/src/influxdb-*/influx              /usr/src/influxdb-*/influx_inspect              /usr/src/influxdb-*/influx_stress              /usr/src/influxdb-*/influxd &&    mv /usr/src/influxdb-*/influx        /usr/src/influxdb-*/influx_inspect        /usr/src/influxdb-*/influx_stress         /usr/src/influxdb-*/influxd        /usr/bin/ &&    gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 01 Dec 2023 05:22:16 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Fri, 01 Dec 2023 05:22:16 GMT
EXPOSE 8086
# Fri, 01 Dec 2023 05:22:16 GMT
VOLUME [/var/lib/influxdb]
# Fri, 01 Dec 2023 05:22:16 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Fri, 01 Dec 2023 05:22:16 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Fri, 01 Dec 2023 05:22:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Dec 2023 05:22:16 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:1207c741d8c9b028d98c4006013f9de959da3c55f85b91ed5e4583438a0112ca`  
		Last Modified: Thu, 30 Nov 2023 23:23:40 GMT  
		Size: 3.4 MB (3379323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae43a7dfb488bfdf09941272691a16afeb9a0ec5f2aeb3afb906b9e61d0eea0`  
		Last Modified: Fri, 01 Dec 2023 05:24:18 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8414376f36c8ce530795b6f714715e47f66e1bc7cb691ab3238a1f754acff0`  
		Last Modified: Fri, 01 Dec 2023 05:24:16 GMT  
		Size: 1.5 MB (1472464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d71b51e5d30bc3ced7a7d0e8decbb28c57920dd18985367fdf870c64c9e94533`  
		Last Modified: Fri, 01 Dec 2023 05:24:24 GMT  
		Size: 54.6 MB (54646682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de6bcb56167953acb95e96c9fab8e4ea8cc8ddbdec2d5b3427ba3875607cdce`  
		Last Modified: Fri, 01 Dec 2023 05:24:16 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ccc2ba70e548cfa1950081f6cfe9cdb0355ccefcf958dc77539528bf5cfa5eb`  
		Last Modified: Fri, 01 Dec 2023 05:24:16 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae809d1684b67ab4c53382693c4ff531062ee6710212cd357bc7d60fd6adc576`  
		Last Modified: Fri, 01 Dec 2023 05:24:18 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.9-data`

```console
$ docker pull influxdb@sha256:701754bb3a0ec5ee66d8987327729cb8fd778ed93ee879d2afbc7c2f14e72a8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.9-data` - linux; amd64

```console
$ docker pull influxdb@sha256:31c60f0a6f13286b5d89c2f6f5870bb736970ae3374abb5d3fc88bc108063e34
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104115549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3a55e68cba94a79997b7b6ffe9b07ed0f8dd178a0abf2a1abfeec8a58b9adc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:04 GMT
ADD file:35f7caaedc3b6f725dee87eb8d1f2727c04cb21062b5eb7f59801dafced61993 in / 
# Thu, 11 Jan 2024 02:38:05 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:36:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 16:39:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 16:39:10 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Thu, 11 Jan 2024 16:39:15 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Thu, 11 Jan 2024 16:39:15 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Thu, 11 Jan 2024 16:39:15 GMT
EXPOSE 8086
# Thu, 11 Jan 2024 16:39:15 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jan 2024 16:39:16 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Thu, 11 Jan 2024 16:39:16 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 11 Jan 2024 16:39:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 16:39:16 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:e455cf41eadb2f19f014361006086cdc5b3de16f3d13bd1d586be63e66c7fc63`  
		Last Modified: Thu, 11 Jan 2024 02:42:47 GMT  
		Size: 55.1 MB (55057723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4531da2f06f2911a5e67446c1ec507acb336afe7130741c6ed12ce442b730f`  
		Last Modified: Thu, 11 Jan 2024 04:45:42 GMT  
		Size: 15.8 MB (15765113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14fb060119b49def67db8ec15d6ffc47c094d5675101637e97e7f06d38aa3fe0`  
		Last Modified: Thu, 11 Jan 2024 16:40:43 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:669854585cfbf99ce4ef1b741b2cb35c2d244d32882b2baadaf0b911450d9078`  
		Last Modified: Thu, 11 Jan 2024 16:41:06 GMT  
		Size: 33.3 MB (33289125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af864f5545d02f3883793e3a999306e4cd81a2648f896427efd1e6ebe56b241`  
		Last Modified: Thu, 11 Jan 2024 16:41:00 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972bb62e6aa8c836b722e5c9547021319cfbffebc730b05261bfabf28a96994e`  
		Last Modified: Thu, 11 Jan 2024 16:41:00 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b96d7ff4f628bceb93e341cf73c4c087452c69a547c10ef61bd69dc7299c10`  
		Last Modified: Thu, 11 Jan 2024 16:41:00 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.9-data-alpine`

```console
$ docker pull influxdb@sha256:adeb0cf38e6218d7355b854340dbe1abeace99204d20c719c3cb4100dc428788
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.9-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:7f97706ea642422a81fe5e5844306841bccbdce45323f938b71070d494dca046
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 MB (38102540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5381b54e146d8876ad693d26cb84c2e1dc158dcaadd6efa65841f96c4a9c92f1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:58 GMT
ADD file:80331a5d882ac8a70763f4b19e06f2e04ea3dca34ae6d92810815b170b3c806c in / 
# Thu, 30 Nov 2023 23:22:59 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 05:22:09 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 01 Dec 2023 05:22:10 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Fri, 01 Dec 2023 05:22:23 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Fri, 01 Dec 2023 05:22:30 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/etc/influxdb/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 01 Dec 2023 05:22:30 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Fri, 01 Dec 2023 05:22:30 GMT
EXPOSE 8086
# Fri, 01 Dec 2023 05:22:30 GMT
VOLUME [/var/lib/influxdb]
# Fri, 01 Dec 2023 05:22:30 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Fri, 01 Dec 2023 05:22:30 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Fri, 01 Dec 2023 05:22:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Dec 2023 05:22:31 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:1207c741d8c9b028d98c4006013f9de959da3c55f85b91ed5e4583438a0112ca`  
		Last Modified: Thu, 30 Nov 2023 23:23:40 GMT  
		Size: 3.4 MB (3379323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae43a7dfb488bfdf09941272691a16afeb9a0ec5f2aeb3afb906b9e61d0eea0`  
		Last Modified: Fri, 01 Dec 2023 05:24:18 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8414376f36c8ce530795b6f714715e47f66e1bc7cb691ab3238a1f754acff0`  
		Last Modified: Fri, 01 Dec 2023 05:24:16 GMT  
		Size: 1.5 MB (1472464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a070b43e211ae31d65720654ee8ea7805061344e90ca915551f928063ecdf440`  
		Last Modified: Fri, 01 Dec 2023 05:24:38 GMT  
		Size: 33.2 MB (33248679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2643f8d5e2dff17ab618ccf8af38eaa96ce8fb897742613d8b3c20b4ed6858`  
		Last Modified: Fri, 01 Dec 2023 05:24:33 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6142bca6012c8a569ed136d04b7376df74f3eed662deaf71c5829c86faa5fec`  
		Last Modified: Fri, 01 Dec 2023 05:24:34 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e7f4d9734b51787b3252bb621b16d79bdb2d294ef86f7280de6dfbe748d2dd`  
		Last Modified: Fri, 01 Dec 2023 05:24:33 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.9-meta`

```console
$ docker pull influxdb@sha256:f43981e2d9fec98b23cafcd587797c8626fd06a172ebe39a8b872adb2ff04e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.9-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:4b6645a337347cd574dca34d13a7d42210bb83f6056081a6a5e808e97a5080a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83595025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:622f6f9cc7c484d952d13f101da1cd3eb8d44def53fa579dd6edc493381a55fa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:04 GMT
ADD file:35f7caaedc3b6f725dee87eb8d1f2727c04cb21062b5eb7f59801dafced61993 in / 
# Thu, 11 Jan 2024 02:38:05 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:36:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 16:39:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 16:39:10 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Thu, 11 Jan 2024 16:39:25 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Thu, 11 Jan 2024 16:39:25 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Thu, 11 Jan 2024 16:39:25 GMT
EXPOSE 8091
# Thu, 11 Jan 2024 16:39:25 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jan 2024 16:39:25 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Thu, 11 Jan 2024 16:39:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 16:39:25 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:e455cf41eadb2f19f014361006086cdc5b3de16f3d13bd1d586be63e66c7fc63`  
		Last Modified: Thu, 11 Jan 2024 02:42:47 GMT  
		Size: 55.1 MB (55057723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4531da2f06f2911a5e67446c1ec507acb336afe7130741c6ed12ce442b730f`  
		Last Modified: Thu, 11 Jan 2024 04:45:42 GMT  
		Size: 15.8 MB (15765113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14fb060119b49def67db8ec15d6ffc47c094d5675101637e97e7f06d38aa3fe0`  
		Last Modified: Thu, 11 Jan 2024 16:40:43 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222114bdb7fe2b3f91709caf2a93dd6cc5342111930d5c2cba40cd9b7d8c4cc1`  
		Last Modified: Thu, 11 Jan 2024 16:41:16 GMT  
		Size: 12.8 MB (12769807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba668b951769d0326fedfca47620fc55863d772a576845ab7182b6b4126d64b`  
		Last Modified: Thu, 11 Jan 2024 16:41:14 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e76ba2ef0de394aa9bb97d1fa3fcd3cb73b079844e18f8f32476575c12307c`  
		Last Modified: Thu, 11 Jan 2024 16:41:14 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.9-meta-alpine`

```console
$ docker pull influxdb@sha256:ca666b3aaf56171453bf39ac768cd27175b1d2976b466ec045c396908f3a51ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.9-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:3c4607a75b1ec3c8984d30dc674fb8f9b616bc406dd1d5bbb15a9258da682679
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17586859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:960735aa4ad9e0fe0196cbfcb26f0975789d18d05dec7d6fc31c58e0710a9689`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:58 GMT
ADD file:80331a5d882ac8a70763f4b19e06f2e04ea3dca34ae6d92810815b170b3c806c in / 
# Thu, 30 Nov 2023 23:22:59 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 05:22:09 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 01 Dec 2023 05:22:10 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Fri, 01 Dec 2023 05:22:23 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Fri, 01 Dec 2023 05:22:42 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/etc/influxdb/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 01 Dec 2023 05:22:42 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Fri, 01 Dec 2023 05:22:42 GMT
EXPOSE 8091
# Fri, 01 Dec 2023 05:22:42 GMT
VOLUME [/var/lib/influxdb]
# Fri, 01 Dec 2023 05:22:42 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Fri, 01 Dec 2023 05:22:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Dec 2023 05:22:42 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:1207c741d8c9b028d98c4006013f9de959da3c55f85b91ed5e4583438a0112ca`  
		Last Modified: Thu, 30 Nov 2023 23:23:40 GMT  
		Size: 3.4 MB (3379323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae43a7dfb488bfdf09941272691a16afeb9a0ec5f2aeb3afb906b9e61d0eea0`  
		Last Modified: Fri, 01 Dec 2023 05:24:18 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8414376f36c8ce530795b6f714715e47f66e1bc7cb691ab3238a1f754acff0`  
		Last Modified: Fri, 01 Dec 2023 05:24:16 GMT  
		Size: 1.5 MB (1472464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea386feadacd05635b13a79d5e79cfc29c0c150f41325bfb21a3269a5e2ba0fd`  
		Last Modified: Fri, 01 Dec 2023 05:24:49 GMT  
		Size: 12.7 MB (12734204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60e1b5b09694a944260e6a69f278c6f905093a0d4006bc363a1ec18c56cd774d`  
		Last Modified: Fri, 01 Dec 2023 05:24:47 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b2cc61d91e987cd5a835c96513e830d90e2118feacd8d9fa9535f10c4989a99`  
		Last Modified: Fri, 01 Dec 2023 05:24:47 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.9.13-data`

```console
$ docker pull influxdb@sha256:701754bb3a0ec5ee66d8987327729cb8fd778ed93ee879d2afbc7c2f14e72a8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.9.13-data` - linux; amd64

```console
$ docker pull influxdb@sha256:31c60f0a6f13286b5d89c2f6f5870bb736970ae3374abb5d3fc88bc108063e34
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104115549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3a55e68cba94a79997b7b6ffe9b07ed0f8dd178a0abf2a1abfeec8a58b9adc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:04 GMT
ADD file:35f7caaedc3b6f725dee87eb8d1f2727c04cb21062b5eb7f59801dafced61993 in / 
# Thu, 11 Jan 2024 02:38:05 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:36:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 16:39:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 16:39:10 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Thu, 11 Jan 2024 16:39:15 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Thu, 11 Jan 2024 16:39:15 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Thu, 11 Jan 2024 16:39:15 GMT
EXPOSE 8086
# Thu, 11 Jan 2024 16:39:15 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jan 2024 16:39:16 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Thu, 11 Jan 2024 16:39:16 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 11 Jan 2024 16:39:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 16:39:16 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:e455cf41eadb2f19f014361006086cdc5b3de16f3d13bd1d586be63e66c7fc63`  
		Last Modified: Thu, 11 Jan 2024 02:42:47 GMT  
		Size: 55.1 MB (55057723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4531da2f06f2911a5e67446c1ec507acb336afe7130741c6ed12ce442b730f`  
		Last Modified: Thu, 11 Jan 2024 04:45:42 GMT  
		Size: 15.8 MB (15765113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14fb060119b49def67db8ec15d6ffc47c094d5675101637e97e7f06d38aa3fe0`  
		Last Modified: Thu, 11 Jan 2024 16:40:43 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:669854585cfbf99ce4ef1b741b2cb35c2d244d32882b2baadaf0b911450d9078`  
		Last Modified: Thu, 11 Jan 2024 16:41:06 GMT  
		Size: 33.3 MB (33289125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af864f5545d02f3883793e3a999306e4cd81a2648f896427efd1e6ebe56b241`  
		Last Modified: Thu, 11 Jan 2024 16:41:00 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972bb62e6aa8c836b722e5c9547021319cfbffebc730b05261bfabf28a96994e`  
		Last Modified: Thu, 11 Jan 2024 16:41:00 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b96d7ff4f628bceb93e341cf73c4c087452c69a547c10ef61bd69dc7299c10`  
		Last Modified: Thu, 11 Jan 2024 16:41:00 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.9.13-data-alpine`

```console
$ docker pull influxdb@sha256:adeb0cf38e6218d7355b854340dbe1abeace99204d20c719c3cb4100dc428788
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.9.13-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:7f97706ea642422a81fe5e5844306841bccbdce45323f938b71070d494dca046
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 MB (38102540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5381b54e146d8876ad693d26cb84c2e1dc158dcaadd6efa65841f96c4a9c92f1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:58 GMT
ADD file:80331a5d882ac8a70763f4b19e06f2e04ea3dca34ae6d92810815b170b3c806c in / 
# Thu, 30 Nov 2023 23:22:59 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 05:22:09 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 01 Dec 2023 05:22:10 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Fri, 01 Dec 2023 05:22:23 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Fri, 01 Dec 2023 05:22:30 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/etc/influxdb/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 01 Dec 2023 05:22:30 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Fri, 01 Dec 2023 05:22:30 GMT
EXPOSE 8086
# Fri, 01 Dec 2023 05:22:30 GMT
VOLUME [/var/lib/influxdb]
# Fri, 01 Dec 2023 05:22:30 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Fri, 01 Dec 2023 05:22:30 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Fri, 01 Dec 2023 05:22:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Dec 2023 05:22:31 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:1207c741d8c9b028d98c4006013f9de959da3c55f85b91ed5e4583438a0112ca`  
		Last Modified: Thu, 30 Nov 2023 23:23:40 GMT  
		Size: 3.4 MB (3379323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae43a7dfb488bfdf09941272691a16afeb9a0ec5f2aeb3afb906b9e61d0eea0`  
		Last Modified: Fri, 01 Dec 2023 05:24:18 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8414376f36c8ce530795b6f714715e47f66e1bc7cb691ab3238a1f754acff0`  
		Last Modified: Fri, 01 Dec 2023 05:24:16 GMT  
		Size: 1.5 MB (1472464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a070b43e211ae31d65720654ee8ea7805061344e90ca915551f928063ecdf440`  
		Last Modified: Fri, 01 Dec 2023 05:24:38 GMT  
		Size: 33.2 MB (33248679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2643f8d5e2dff17ab618ccf8af38eaa96ce8fb897742613d8b3c20b4ed6858`  
		Last Modified: Fri, 01 Dec 2023 05:24:33 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6142bca6012c8a569ed136d04b7376df74f3eed662deaf71c5829c86faa5fec`  
		Last Modified: Fri, 01 Dec 2023 05:24:34 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e7f4d9734b51787b3252bb621b16d79bdb2d294ef86f7280de6dfbe748d2dd`  
		Last Modified: Fri, 01 Dec 2023 05:24:33 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.9.13-meta`

```console
$ docker pull influxdb@sha256:f43981e2d9fec98b23cafcd587797c8626fd06a172ebe39a8b872adb2ff04e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.9.13-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:4b6645a337347cd574dca34d13a7d42210bb83f6056081a6a5e808e97a5080a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83595025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:622f6f9cc7c484d952d13f101da1cd3eb8d44def53fa579dd6edc493381a55fa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:04 GMT
ADD file:35f7caaedc3b6f725dee87eb8d1f2727c04cb21062b5eb7f59801dafced61993 in / 
# Thu, 11 Jan 2024 02:38:05 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:36:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 16:39:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 16:39:10 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Thu, 11 Jan 2024 16:39:25 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Thu, 11 Jan 2024 16:39:25 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Thu, 11 Jan 2024 16:39:25 GMT
EXPOSE 8091
# Thu, 11 Jan 2024 16:39:25 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jan 2024 16:39:25 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Thu, 11 Jan 2024 16:39:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 16:39:25 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:e455cf41eadb2f19f014361006086cdc5b3de16f3d13bd1d586be63e66c7fc63`  
		Last Modified: Thu, 11 Jan 2024 02:42:47 GMT  
		Size: 55.1 MB (55057723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4531da2f06f2911a5e67446c1ec507acb336afe7130741c6ed12ce442b730f`  
		Last Modified: Thu, 11 Jan 2024 04:45:42 GMT  
		Size: 15.8 MB (15765113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14fb060119b49def67db8ec15d6ffc47c094d5675101637e97e7f06d38aa3fe0`  
		Last Modified: Thu, 11 Jan 2024 16:40:43 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222114bdb7fe2b3f91709caf2a93dd6cc5342111930d5c2cba40cd9b7d8c4cc1`  
		Last Modified: Thu, 11 Jan 2024 16:41:16 GMT  
		Size: 12.8 MB (12769807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba668b951769d0326fedfca47620fc55863d772a576845ab7182b6b4126d64b`  
		Last Modified: Thu, 11 Jan 2024 16:41:14 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e76ba2ef0de394aa9bb97d1fa3fcd3cb73b079844e18f8f32476575c12307c`  
		Last Modified: Thu, 11 Jan 2024 16:41:14 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.9.13-meta-alpine`

```console
$ docker pull influxdb@sha256:ca666b3aaf56171453bf39ac768cd27175b1d2976b466ec045c396908f3a51ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.9.13-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:3c4607a75b1ec3c8984d30dc674fb8f9b616bc406dd1d5bbb15a9258da682679
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17586859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:960735aa4ad9e0fe0196cbfcb26f0975789d18d05dec7d6fc31c58e0710a9689`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:58 GMT
ADD file:80331a5d882ac8a70763f4b19e06f2e04ea3dca34ae6d92810815b170b3c806c in / 
# Thu, 30 Nov 2023 23:22:59 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 05:22:09 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 01 Dec 2023 05:22:10 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Fri, 01 Dec 2023 05:22:23 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Fri, 01 Dec 2023 05:22:42 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/etc/influxdb/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 01 Dec 2023 05:22:42 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Fri, 01 Dec 2023 05:22:42 GMT
EXPOSE 8091
# Fri, 01 Dec 2023 05:22:42 GMT
VOLUME [/var/lib/influxdb]
# Fri, 01 Dec 2023 05:22:42 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Fri, 01 Dec 2023 05:22:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Dec 2023 05:22:42 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:1207c741d8c9b028d98c4006013f9de959da3c55f85b91ed5e4583438a0112ca`  
		Last Modified: Thu, 30 Nov 2023 23:23:40 GMT  
		Size: 3.4 MB (3379323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae43a7dfb488bfdf09941272691a16afeb9a0ec5f2aeb3afb906b9e61d0eea0`  
		Last Modified: Fri, 01 Dec 2023 05:24:18 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8414376f36c8ce530795b6f714715e47f66e1bc7cb691ab3238a1f754acff0`  
		Last Modified: Fri, 01 Dec 2023 05:24:16 GMT  
		Size: 1.5 MB (1472464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea386feadacd05635b13a79d5e79cfc29c0c150f41325bfb21a3269a5e2ba0fd`  
		Last Modified: Fri, 01 Dec 2023 05:24:49 GMT  
		Size: 12.7 MB (12734204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60e1b5b09694a944260e6a69f278c6f905093a0d4006bc363a1ec18c56cd774d`  
		Last Modified: Fri, 01 Dec 2023 05:24:47 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b2cc61d91e987cd5a835c96513e830d90e2118feacd8d9fa9535f10c4989a99`  
		Last Modified: Fri, 01 Dec 2023 05:24:47 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.7`

```console
$ docker pull influxdb@sha256:f3765ab8ae6c9fddebe36b95ce1a85097c92146573d1a809dfe7bed60920a2d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.7` - linux; amd64

```console
$ docker pull influxdb@sha256:ec5d16059e3bab61d11c556ca6ab17601c32163f084605d7e6787aeb36b78e8a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164680218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a1b63100937139a749eef826781458bb4e3418e51481a02483b8d91891a6115`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:54 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Thu, 11 Jan 2024 02:37:54 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:09:41 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 04:09:43 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version
# Thu, 11 Jan 2024 04:09:44 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb
# Thu, 11 Jan 2024 04:09:44 GMT
ENV GOSU_VER=1.16
# Thu, 11 Jan 2024 04:09:47 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true
# Thu, 11 Jan 2024 04:09:47 GMT
ENV INFLUXDB_VERSION=2.7.5
# Thu, 11 Jan 2024 04:09:52 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version
# Thu, 11 Jan 2024 04:09:52 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 11 Jan 2024 04:09:54 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version
# Thu, 11 Jan 2024 04:09:55 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Thu, 11 Jan 2024 04:09:55 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 11 Jan 2024 04:09:55 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Thu, 11 Jan 2024 04:09:55 GMT
COPY file:b5520696339eadb7386055c1dc9487351aa145a79b0cf206d8b1a79699c4a7f1 in /entrypoint.sh 
# Thu, 11 Jan 2024 04:09:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 04:09:55 GMT
CMD ["influxd"]
# Thu, 11 Jan 2024 04:09:56 GMT
EXPOSE 8086
# Thu, 11 Jan 2024 04:09:56 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 11 Jan 2024 04:09:56 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 11 Jan 2024 04:09:56 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 11 Jan 2024 04:09:56 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b879f7f0b97813db2ab558426c6245d7493ec849b5c6af62bae7b50557a079`  
		Last Modified: Thu, 11 Jan 2024 04:10:39 GMT  
		Size: 9.8 MB (9784548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:391f2a95149104db5eaf7dbe8761c8a7c58af0a0ecee1872febe45d407b6bbfb`  
		Last Modified: Thu, 11 Jan 2024 04:10:36 GMT  
		Size: 5.8 MB (5820928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc0f8d17c9bcf98af54ddd62f93ee6c90fef24a7c33149fb2e49dfb19791ca43`  
		Last Modified: Thu, 11 Jan 2024 04:10:36 GMT  
		Size: 3.3 KB (3279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eea0149521594e79d232332b04ff4dd56e9e9a290f087f52e6fc59bbe8baf33`  
		Last Modified: Thu, 11 Jan 2024 04:10:36 GMT  
		Size: 1.0 MB (1006418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c74718bd32e2b889be8c94b089e9d388f009188f6c1dfda5ec4509cce504e45d`  
		Last Modified: Thu, 11 Jan 2024 04:10:44 GMT  
		Size: 95.8 MB (95803956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab287bfba4b08c4fc84caa53c34ca8abf0e7c77cb2ab01ef3a47b560be60a843`  
		Last Modified: Thu, 11 Jan 2024 04:10:36 GMT  
		Size: 23.1 MB (23128347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f5135083ba7e52dd2ef5fd0312e737a280b3571aa04d6e3a29dceff332b9e5`  
		Last Modified: Thu, 11 Jan 2024 04:10:34 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8acfea7e99e37cfd1049d98a07b95312addf03bb176a003941d5406bc6c08bb6`  
		Last Modified: Thu, 11 Jan 2024 04:10:34 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c3fd5840e752ea1c9222f0db53080b5b73d5405b82bc84dc23843ff4b7eec54`  
		Last Modified: Thu, 11 Jan 2024 04:10:34 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.7` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:832eece17bb962f211cdf029f6155c7f8e1cd4cacd724cedb2a7750107f6bb7f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.9 MB (158897627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007c75ff8554e420da151e20acab90e091664c8eb0fd542f6b436f2a75af5274`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:44 GMT
ADD file:70e4f0c71f88c97c8db279b998c10d4943954d304ff9f51875c3699a4dc5ee4e in / 
# Thu, 11 Jan 2024 02:40:45 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:26:57 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 06:26:59 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version
# Thu, 11 Jan 2024 06:26:59 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb
# Thu, 11 Jan 2024 06:26:59 GMT
ENV GOSU_VER=1.16
# Thu, 11 Jan 2024 06:27:02 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true
# Thu, 11 Jan 2024 06:27:02 GMT
ENV INFLUXDB_VERSION=2.7.5
# Thu, 11 Jan 2024 06:27:07 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version
# Thu, 11 Jan 2024 06:27:08 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 11 Jan 2024 06:27:10 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version
# Thu, 11 Jan 2024 06:27:10 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Thu, 11 Jan 2024 06:27:10 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 11 Jan 2024 06:27:10 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Thu, 11 Jan 2024 06:27:10 GMT
COPY file:b5520696339eadb7386055c1dc9487351aa145a79b0cf206d8b1a79699c4a7f1 in /entrypoint.sh 
# Thu, 11 Jan 2024 06:27:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 06:27:11 GMT
CMD ["influxd"]
# Thu, 11 Jan 2024 06:27:11 GMT
EXPOSE 8086
# Thu, 11 Jan 2024 06:27:11 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 11 Jan 2024 06:27:11 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 11 Jan 2024 06:27:11 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 11 Jan 2024 06:27:11 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:a5573528b1f0cf2f5d87c94fe0aee9d8967d5de98258be9303c3c6fa477824ec`  
		Last Modified: Thu, 11 Jan 2024 02:44:04 GMT  
		Size: 29.2 MB (29157335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c543f2ded9d87bd3e5368772a656ec9fb9b23ec5ee4f05f71f1c8f1360986cb4`  
		Last Modified: Thu, 11 Jan 2024 06:27:27 GMT  
		Size: 9.6 MB (9581384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b2acc1b1088cec4796cd50c6c115abf7a1743d6e99eae37f1c6d9e53169cb3`  
		Last Modified: Thu, 11 Jan 2024 06:27:25 GMT  
		Size: 5.5 MB (5463785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b127df0dcec919697c30c0bd266c00db0a975dd94dd9a063b6379aeb2ae83611`  
		Last Modified: Thu, 11 Jan 2024 06:27:24 GMT  
		Size: 3.3 KB (3281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b420d207f0e0e7a91b25f8dfa4a01b17f5a2bd19cf8ee824cf4668bc0c2dc098`  
		Last Modified: Thu, 11 Jan 2024 06:27:24 GMT  
		Size: 936.1 KB (936110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95615c5c923baa13098b8ca4486f8c22c80d43fa26c52f7e193db8698ec6b08e`  
		Last Modified: Thu, 11 Jan 2024 06:27:29 GMT  
		Size: 92.1 MB (92086314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe791de1db4830776f0821dd1cdc1582a6d62b94081a3deb9b03674488e7a72`  
		Last Modified: Thu, 11 Jan 2024 06:27:25 GMT  
		Size: 21.7 MB (21662599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2529595ecc4ff3cb1b2beaeba3882be93bd2993e6df3b89b5171e6a47d3a8efb`  
		Last Modified: Thu, 11 Jan 2024 06:27:22 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2075d0de8ccfa8a6e386a205b6923de74cf542b584d725d5e056b44a51a95704`  
		Last Modified: Thu, 11 Jan 2024 06:27:22 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0464a5461d0b1958c954d476b3ebcf76f1787c78f1958f84363aac3168a78aa`  
		Last Modified: Thu, 11 Jan 2024 06:27:22 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.7-alpine`

```console
$ docker pull influxdb@sha256:2ec0745cc2eed5444c599e274e59580162c840f43d917a493cab07ee9d41f746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.7-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:2acd355bf573d74a5e1c3d8ef231e7c2be9648d5668c73efc5650b9be3d3cb90
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.1 MB (89124590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94581e2f6f0477acafd2456164003a49646f48c93702251d6a4f2689b4b101fd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 05:23:13 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 01 Dec 2023 05:23:42 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates
# Fri, 01 Dec 2023 05:23:43 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version
# Fri, 01 Dec 2023 05:23:44 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Sat, 06 Jan 2024 00:52:43 GMT
ENV INFLUXDB_VERSION=2.7.5
# Sat, 06 Jan 2024 00:52:47 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version
# Sat, 06 Jan 2024 00:52:47 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Sat, 06 Jan 2024 00:52:49 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version
# Sat, 06 Jan 2024 00:52:50 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Sat, 06 Jan 2024 00:52:50 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Sat, 06 Jan 2024 00:52:50 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Sat, 06 Jan 2024 00:52:50 GMT
COPY file:6341d1dd8e0763e797b79985007acd07a4686ed831d55018f6e390823bad9d07 in /entrypoint.sh 
# Sat, 06 Jan 2024 00:52:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 06 Jan 2024 00:52:50 GMT
CMD ["influxd"]
# Sat, 06 Jan 2024 00:52:50 GMT
EXPOSE 8086
# Sat, 06 Jan 2024 00:52:50 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Sat, 06 Jan 2024 00:52:50 GMT
ENV INFLUXD_INIT_PORT=9999
# Sat, 06 Jan 2024 00:52:50 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Sat, 06 Jan 2024 00:52:50 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703e958f39c4082f015dd7de32b1c116ef56e1e54010a31e991ec0c10e7feecc`  
		Last Modified: Fri, 01 Dec 2023 05:25:29 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c7a2a064178d0a8f1606e8349aeb873d4ccf794630219d4987058d3e3b2403`  
		Last Modified: Fri, 01 Dec 2023 05:26:00 GMT  
		Size: 8.9 MB (8868241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec9837ae77681e83d32d6fcc47a5563b56f9576cb8b9631c34a3d04cd56202ee`  
		Last Modified: Fri, 01 Dec 2023 05:25:59 GMT  
		Size: 5.8 MB (5820949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94bdcf91f553c62f44965ccd8de465bd7dd6795310fe044bfc5323ab7b46d13f`  
		Last Modified: Fri, 01 Dec 2023 05:25:59 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb4449c1fa8da9a58539f00b7b9ae449cfcb6229c80c18bae30dfa0e21196e4`  
		Last Modified: Sat, 06 Jan 2024 00:54:18 GMT  
		Size: 47.9 MB (47896258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd452affe098ae91a54e425ec0e5dcdb24d6fb187328fd1da494bea1abdf3dd3`  
		Last Modified: Sat, 06 Jan 2024 00:54:16 GMT  
		Size: 23.1 MB (23128352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a38b6f6d1307746511f9fe1b8ec684d1b41d896e050dd66626c279ed46c183e`  
		Last Modified: Sat, 06 Jan 2024 00:54:13 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510e6aedd69eda4ce77938b12a19be0b3d5826c11afdc80d5d20cbda489437fc`  
		Last Modified: Sat, 06 Jan 2024 00:54:13 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c370875bed35d8a2fece85a8c0afde3e90be18da8df0f6a68c51b81f483315ca`  
		Last Modified: Sat, 06 Jan 2024 00:54:13 GMT  
		Size: 6.3 KB (6280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.7-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:bcfee76e082284dc07444a355953f5cd195ebef0be92569807ba37ea42e11270
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.5 MB (85469356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157c2fa3e01c07071962d495fea8cd925b82787d13575557aad43261fd561fdd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 02:38:30 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 01 Dec 2023 02:38:32 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates
# Fri, 01 Dec 2023 02:38:33 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version
# Fri, 01 Dec 2023 02:38:34 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Sat, 06 Jan 2024 01:03:47 GMT
ENV INFLUXDB_VERSION=2.7.5
# Sat, 06 Jan 2024 01:03:50 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version
# Sat, 06 Jan 2024 01:03:51 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Sat, 06 Jan 2024 01:03:53 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version
# Sat, 06 Jan 2024 01:03:53 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Sat, 06 Jan 2024 01:03:53 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Sat, 06 Jan 2024 01:03:53 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Sat, 06 Jan 2024 01:03:53 GMT
COPY file:6341d1dd8e0763e797b79985007acd07a4686ed831d55018f6e390823bad9d07 in /entrypoint.sh 
# Sat, 06 Jan 2024 01:03:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 06 Jan 2024 01:03:54 GMT
CMD ["influxd"]
# Sat, 06 Jan 2024 01:03:54 GMT
EXPOSE 8086
# Sat, 06 Jan 2024 01:03:54 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Sat, 06 Jan 2024 01:03:54 GMT
ENV INFLUXD_INIT_PORT=9999
# Sat, 06 Jan 2024 01:03:54 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Sat, 06 Jan 2024 01:03:54 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00f6ef2d119bdc2b844474b1941025c80c2a28072d415011a971ae3decceb4b8`  
		Last Modified: Fri, 01 Dec 2023 02:38:57 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:219bc19aefdfdc9e712e2ec3f522b6c95b46d8dae4636b4b03232218da21c862`  
		Last Modified: Fri, 01 Dec 2023 02:38:56 GMT  
		Size: 9.0 MB (8962300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ab1ea2040c57ec0c558d867e958ce9b8a15733f2326db44f915514e5470c78`  
		Last Modified: Fri, 01 Dec 2023 02:38:56 GMT  
		Size: 5.5 MB (5463804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53259412624c68cecc9445d0b50dbc35bf444a2c697cbdc53b52ed4780636169`  
		Last Modified: Fri, 01 Dec 2023 02:38:55 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87145c6e0372946a30c8245655c2702467816aa41e25f49c2a121bb6c61dabae`  
		Last Modified: Sat, 06 Jan 2024 01:04:29 GMT  
		Size: 46.0 MB (46039229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae80be9a96244e3849f5578aa655d3227024f56f32caf6fa82717a7a9ce31c5c`  
		Last Modified: Sat, 06 Jan 2024 01:04:27 GMT  
		Size: 21.7 MB (21662623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:051246ccae3512022888f9d8a2a9510cbf7967f60b1d73d911066c7ae9c2d1e1`  
		Last Modified: Sat, 06 Jan 2024 01:04:25 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7043070bf5663305c763d0c98fdc6868951caed4094ae4e5559d8289fad4342e`  
		Last Modified: Sat, 06 Jan 2024 01:04:25 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c3efb09d292ab2a4a5afd4fd35adcf0d268cf56aa84e05dfde023e2728f491`  
		Last Modified: Sat, 06 Jan 2024 01:04:25 GMT  
		Size: 6.3 KB (6280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.7.5`

```console
$ docker pull influxdb@sha256:f3765ab8ae6c9fddebe36b95ce1a85097c92146573d1a809dfe7bed60920a2d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.7.5` - linux; amd64

```console
$ docker pull influxdb@sha256:ec5d16059e3bab61d11c556ca6ab17601c32163f084605d7e6787aeb36b78e8a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164680218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a1b63100937139a749eef826781458bb4e3418e51481a02483b8d91891a6115`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:54 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Thu, 11 Jan 2024 02:37:54 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:09:41 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 04:09:43 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version
# Thu, 11 Jan 2024 04:09:44 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb
# Thu, 11 Jan 2024 04:09:44 GMT
ENV GOSU_VER=1.16
# Thu, 11 Jan 2024 04:09:47 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true
# Thu, 11 Jan 2024 04:09:47 GMT
ENV INFLUXDB_VERSION=2.7.5
# Thu, 11 Jan 2024 04:09:52 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version
# Thu, 11 Jan 2024 04:09:52 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 11 Jan 2024 04:09:54 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version
# Thu, 11 Jan 2024 04:09:55 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Thu, 11 Jan 2024 04:09:55 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 11 Jan 2024 04:09:55 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Thu, 11 Jan 2024 04:09:55 GMT
COPY file:b5520696339eadb7386055c1dc9487351aa145a79b0cf206d8b1a79699c4a7f1 in /entrypoint.sh 
# Thu, 11 Jan 2024 04:09:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 04:09:55 GMT
CMD ["influxd"]
# Thu, 11 Jan 2024 04:09:56 GMT
EXPOSE 8086
# Thu, 11 Jan 2024 04:09:56 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 11 Jan 2024 04:09:56 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 11 Jan 2024 04:09:56 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 11 Jan 2024 04:09:56 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b879f7f0b97813db2ab558426c6245d7493ec849b5c6af62bae7b50557a079`  
		Last Modified: Thu, 11 Jan 2024 04:10:39 GMT  
		Size: 9.8 MB (9784548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:391f2a95149104db5eaf7dbe8761c8a7c58af0a0ecee1872febe45d407b6bbfb`  
		Last Modified: Thu, 11 Jan 2024 04:10:36 GMT  
		Size: 5.8 MB (5820928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc0f8d17c9bcf98af54ddd62f93ee6c90fef24a7c33149fb2e49dfb19791ca43`  
		Last Modified: Thu, 11 Jan 2024 04:10:36 GMT  
		Size: 3.3 KB (3279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eea0149521594e79d232332b04ff4dd56e9e9a290f087f52e6fc59bbe8baf33`  
		Last Modified: Thu, 11 Jan 2024 04:10:36 GMT  
		Size: 1.0 MB (1006418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c74718bd32e2b889be8c94b089e9d388f009188f6c1dfda5ec4509cce504e45d`  
		Last Modified: Thu, 11 Jan 2024 04:10:44 GMT  
		Size: 95.8 MB (95803956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab287bfba4b08c4fc84caa53c34ca8abf0e7c77cb2ab01ef3a47b560be60a843`  
		Last Modified: Thu, 11 Jan 2024 04:10:36 GMT  
		Size: 23.1 MB (23128347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f5135083ba7e52dd2ef5fd0312e737a280b3571aa04d6e3a29dceff332b9e5`  
		Last Modified: Thu, 11 Jan 2024 04:10:34 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8acfea7e99e37cfd1049d98a07b95312addf03bb176a003941d5406bc6c08bb6`  
		Last Modified: Thu, 11 Jan 2024 04:10:34 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c3fd5840e752ea1c9222f0db53080b5b73d5405b82bc84dc23843ff4b7eec54`  
		Last Modified: Thu, 11 Jan 2024 04:10:34 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.7.5` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:832eece17bb962f211cdf029f6155c7f8e1cd4cacd724cedb2a7750107f6bb7f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.9 MB (158897627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007c75ff8554e420da151e20acab90e091664c8eb0fd542f6b436f2a75af5274`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:44 GMT
ADD file:70e4f0c71f88c97c8db279b998c10d4943954d304ff9f51875c3699a4dc5ee4e in / 
# Thu, 11 Jan 2024 02:40:45 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:26:57 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 06:26:59 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version
# Thu, 11 Jan 2024 06:26:59 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb
# Thu, 11 Jan 2024 06:26:59 GMT
ENV GOSU_VER=1.16
# Thu, 11 Jan 2024 06:27:02 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true
# Thu, 11 Jan 2024 06:27:02 GMT
ENV INFLUXDB_VERSION=2.7.5
# Thu, 11 Jan 2024 06:27:07 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version
# Thu, 11 Jan 2024 06:27:08 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 11 Jan 2024 06:27:10 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version
# Thu, 11 Jan 2024 06:27:10 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Thu, 11 Jan 2024 06:27:10 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 11 Jan 2024 06:27:10 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Thu, 11 Jan 2024 06:27:10 GMT
COPY file:b5520696339eadb7386055c1dc9487351aa145a79b0cf206d8b1a79699c4a7f1 in /entrypoint.sh 
# Thu, 11 Jan 2024 06:27:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 06:27:11 GMT
CMD ["influxd"]
# Thu, 11 Jan 2024 06:27:11 GMT
EXPOSE 8086
# Thu, 11 Jan 2024 06:27:11 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 11 Jan 2024 06:27:11 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 11 Jan 2024 06:27:11 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 11 Jan 2024 06:27:11 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:a5573528b1f0cf2f5d87c94fe0aee9d8967d5de98258be9303c3c6fa477824ec`  
		Last Modified: Thu, 11 Jan 2024 02:44:04 GMT  
		Size: 29.2 MB (29157335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c543f2ded9d87bd3e5368772a656ec9fb9b23ec5ee4f05f71f1c8f1360986cb4`  
		Last Modified: Thu, 11 Jan 2024 06:27:27 GMT  
		Size: 9.6 MB (9581384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b2acc1b1088cec4796cd50c6c115abf7a1743d6e99eae37f1c6d9e53169cb3`  
		Last Modified: Thu, 11 Jan 2024 06:27:25 GMT  
		Size: 5.5 MB (5463785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b127df0dcec919697c30c0bd266c00db0a975dd94dd9a063b6379aeb2ae83611`  
		Last Modified: Thu, 11 Jan 2024 06:27:24 GMT  
		Size: 3.3 KB (3281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b420d207f0e0e7a91b25f8dfa4a01b17f5a2bd19cf8ee824cf4668bc0c2dc098`  
		Last Modified: Thu, 11 Jan 2024 06:27:24 GMT  
		Size: 936.1 KB (936110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95615c5c923baa13098b8ca4486f8c22c80d43fa26c52f7e193db8698ec6b08e`  
		Last Modified: Thu, 11 Jan 2024 06:27:29 GMT  
		Size: 92.1 MB (92086314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe791de1db4830776f0821dd1cdc1582a6d62b94081a3deb9b03674488e7a72`  
		Last Modified: Thu, 11 Jan 2024 06:27:25 GMT  
		Size: 21.7 MB (21662599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2529595ecc4ff3cb1b2beaeba3882be93bd2993e6df3b89b5171e6a47d3a8efb`  
		Last Modified: Thu, 11 Jan 2024 06:27:22 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2075d0de8ccfa8a6e386a205b6923de74cf542b584d725d5e056b44a51a95704`  
		Last Modified: Thu, 11 Jan 2024 06:27:22 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0464a5461d0b1958c954d476b3ebcf76f1787c78f1958f84363aac3168a78aa`  
		Last Modified: Thu, 11 Jan 2024 06:27:22 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.7.5-alpine`

```console
$ docker pull influxdb@sha256:2ec0745cc2eed5444c599e274e59580162c840f43d917a493cab07ee9d41f746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.7.5-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:2acd355bf573d74a5e1c3d8ef231e7c2be9648d5668c73efc5650b9be3d3cb90
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.1 MB (89124590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94581e2f6f0477acafd2456164003a49646f48c93702251d6a4f2689b4b101fd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 05:23:13 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 01 Dec 2023 05:23:42 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates
# Fri, 01 Dec 2023 05:23:43 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version
# Fri, 01 Dec 2023 05:23:44 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Sat, 06 Jan 2024 00:52:43 GMT
ENV INFLUXDB_VERSION=2.7.5
# Sat, 06 Jan 2024 00:52:47 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version
# Sat, 06 Jan 2024 00:52:47 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Sat, 06 Jan 2024 00:52:49 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version
# Sat, 06 Jan 2024 00:52:50 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Sat, 06 Jan 2024 00:52:50 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Sat, 06 Jan 2024 00:52:50 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Sat, 06 Jan 2024 00:52:50 GMT
COPY file:6341d1dd8e0763e797b79985007acd07a4686ed831d55018f6e390823bad9d07 in /entrypoint.sh 
# Sat, 06 Jan 2024 00:52:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 06 Jan 2024 00:52:50 GMT
CMD ["influxd"]
# Sat, 06 Jan 2024 00:52:50 GMT
EXPOSE 8086
# Sat, 06 Jan 2024 00:52:50 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Sat, 06 Jan 2024 00:52:50 GMT
ENV INFLUXD_INIT_PORT=9999
# Sat, 06 Jan 2024 00:52:50 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Sat, 06 Jan 2024 00:52:50 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703e958f39c4082f015dd7de32b1c116ef56e1e54010a31e991ec0c10e7feecc`  
		Last Modified: Fri, 01 Dec 2023 05:25:29 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c7a2a064178d0a8f1606e8349aeb873d4ccf794630219d4987058d3e3b2403`  
		Last Modified: Fri, 01 Dec 2023 05:26:00 GMT  
		Size: 8.9 MB (8868241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec9837ae77681e83d32d6fcc47a5563b56f9576cb8b9631c34a3d04cd56202ee`  
		Last Modified: Fri, 01 Dec 2023 05:25:59 GMT  
		Size: 5.8 MB (5820949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94bdcf91f553c62f44965ccd8de465bd7dd6795310fe044bfc5323ab7b46d13f`  
		Last Modified: Fri, 01 Dec 2023 05:25:59 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb4449c1fa8da9a58539f00b7b9ae449cfcb6229c80c18bae30dfa0e21196e4`  
		Last Modified: Sat, 06 Jan 2024 00:54:18 GMT  
		Size: 47.9 MB (47896258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd452affe098ae91a54e425ec0e5dcdb24d6fb187328fd1da494bea1abdf3dd3`  
		Last Modified: Sat, 06 Jan 2024 00:54:16 GMT  
		Size: 23.1 MB (23128352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a38b6f6d1307746511f9fe1b8ec684d1b41d896e050dd66626c279ed46c183e`  
		Last Modified: Sat, 06 Jan 2024 00:54:13 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510e6aedd69eda4ce77938b12a19be0b3d5826c11afdc80d5d20cbda489437fc`  
		Last Modified: Sat, 06 Jan 2024 00:54:13 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c370875bed35d8a2fece85a8c0afde3e90be18da8df0f6a68c51b81f483315ca`  
		Last Modified: Sat, 06 Jan 2024 00:54:13 GMT  
		Size: 6.3 KB (6280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.7.5-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:bcfee76e082284dc07444a355953f5cd195ebef0be92569807ba37ea42e11270
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.5 MB (85469356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157c2fa3e01c07071962d495fea8cd925b82787d13575557aad43261fd561fdd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 02:38:30 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 01 Dec 2023 02:38:32 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates
# Fri, 01 Dec 2023 02:38:33 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version
# Fri, 01 Dec 2023 02:38:34 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Sat, 06 Jan 2024 01:03:47 GMT
ENV INFLUXDB_VERSION=2.7.5
# Sat, 06 Jan 2024 01:03:50 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version
# Sat, 06 Jan 2024 01:03:51 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Sat, 06 Jan 2024 01:03:53 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version
# Sat, 06 Jan 2024 01:03:53 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Sat, 06 Jan 2024 01:03:53 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Sat, 06 Jan 2024 01:03:53 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Sat, 06 Jan 2024 01:03:53 GMT
COPY file:6341d1dd8e0763e797b79985007acd07a4686ed831d55018f6e390823bad9d07 in /entrypoint.sh 
# Sat, 06 Jan 2024 01:03:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 06 Jan 2024 01:03:54 GMT
CMD ["influxd"]
# Sat, 06 Jan 2024 01:03:54 GMT
EXPOSE 8086
# Sat, 06 Jan 2024 01:03:54 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Sat, 06 Jan 2024 01:03:54 GMT
ENV INFLUXD_INIT_PORT=9999
# Sat, 06 Jan 2024 01:03:54 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Sat, 06 Jan 2024 01:03:54 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00f6ef2d119bdc2b844474b1941025c80c2a28072d415011a971ae3decceb4b8`  
		Last Modified: Fri, 01 Dec 2023 02:38:57 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:219bc19aefdfdc9e712e2ec3f522b6c95b46d8dae4636b4b03232218da21c862`  
		Last Modified: Fri, 01 Dec 2023 02:38:56 GMT  
		Size: 9.0 MB (8962300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ab1ea2040c57ec0c558d867e958ce9b8a15733f2326db44f915514e5470c78`  
		Last Modified: Fri, 01 Dec 2023 02:38:56 GMT  
		Size: 5.5 MB (5463804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53259412624c68cecc9445d0b50dbc35bf444a2c697cbdc53b52ed4780636169`  
		Last Modified: Fri, 01 Dec 2023 02:38:55 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87145c6e0372946a30c8245655c2702467816aa41e25f49c2a121bb6c61dabae`  
		Last Modified: Sat, 06 Jan 2024 01:04:29 GMT  
		Size: 46.0 MB (46039229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae80be9a96244e3849f5578aa655d3227024f56f32caf6fa82717a7a9ce31c5c`  
		Last Modified: Sat, 06 Jan 2024 01:04:27 GMT  
		Size: 21.7 MB (21662623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:051246ccae3512022888f9d8a2a9510cbf7967f60b1d73d911066c7ae9c2d1e1`  
		Last Modified: Sat, 06 Jan 2024 01:04:25 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7043070bf5663305c763d0c98fdc6868951caed4094ae4e5559d8289fad4342e`  
		Last Modified: Sat, 06 Jan 2024 01:04:25 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c3efb09d292ab2a4a5afd4fd35adcf0d268cf56aa84e05dfde023e2728f491`  
		Last Modified: Sat, 06 Jan 2024 01:04:25 GMT  
		Size: 6.3 KB (6280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:2ec0745cc2eed5444c599e274e59580162c840f43d917a493cab07ee9d41f746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:2acd355bf573d74a5e1c3d8ef231e7c2be9648d5668c73efc5650b9be3d3cb90
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.1 MB (89124590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94581e2f6f0477acafd2456164003a49646f48c93702251d6a4f2689b4b101fd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 05:23:13 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 01 Dec 2023 05:23:42 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates
# Fri, 01 Dec 2023 05:23:43 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version
# Fri, 01 Dec 2023 05:23:44 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Sat, 06 Jan 2024 00:52:43 GMT
ENV INFLUXDB_VERSION=2.7.5
# Sat, 06 Jan 2024 00:52:47 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version
# Sat, 06 Jan 2024 00:52:47 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Sat, 06 Jan 2024 00:52:49 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version
# Sat, 06 Jan 2024 00:52:50 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Sat, 06 Jan 2024 00:52:50 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Sat, 06 Jan 2024 00:52:50 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Sat, 06 Jan 2024 00:52:50 GMT
COPY file:6341d1dd8e0763e797b79985007acd07a4686ed831d55018f6e390823bad9d07 in /entrypoint.sh 
# Sat, 06 Jan 2024 00:52:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 06 Jan 2024 00:52:50 GMT
CMD ["influxd"]
# Sat, 06 Jan 2024 00:52:50 GMT
EXPOSE 8086
# Sat, 06 Jan 2024 00:52:50 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Sat, 06 Jan 2024 00:52:50 GMT
ENV INFLUXD_INIT_PORT=9999
# Sat, 06 Jan 2024 00:52:50 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Sat, 06 Jan 2024 00:52:50 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703e958f39c4082f015dd7de32b1c116ef56e1e54010a31e991ec0c10e7feecc`  
		Last Modified: Fri, 01 Dec 2023 05:25:29 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c7a2a064178d0a8f1606e8349aeb873d4ccf794630219d4987058d3e3b2403`  
		Last Modified: Fri, 01 Dec 2023 05:26:00 GMT  
		Size: 8.9 MB (8868241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec9837ae77681e83d32d6fcc47a5563b56f9576cb8b9631c34a3d04cd56202ee`  
		Last Modified: Fri, 01 Dec 2023 05:25:59 GMT  
		Size: 5.8 MB (5820949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94bdcf91f553c62f44965ccd8de465bd7dd6795310fe044bfc5323ab7b46d13f`  
		Last Modified: Fri, 01 Dec 2023 05:25:59 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb4449c1fa8da9a58539f00b7b9ae449cfcb6229c80c18bae30dfa0e21196e4`  
		Last Modified: Sat, 06 Jan 2024 00:54:18 GMT  
		Size: 47.9 MB (47896258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd452affe098ae91a54e425ec0e5dcdb24d6fb187328fd1da494bea1abdf3dd3`  
		Last Modified: Sat, 06 Jan 2024 00:54:16 GMT  
		Size: 23.1 MB (23128352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a38b6f6d1307746511f9fe1b8ec684d1b41d896e050dd66626c279ed46c183e`  
		Last Modified: Sat, 06 Jan 2024 00:54:13 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510e6aedd69eda4ce77938b12a19be0b3d5826c11afdc80d5d20cbda489437fc`  
		Last Modified: Sat, 06 Jan 2024 00:54:13 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c370875bed35d8a2fece85a8c0afde3e90be18da8df0f6a68c51b81f483315ca`  
		Last Modified: Sat, 06 Jan 2024 00:54:13 GMT  
		Size: 6.3 KB (6280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:bcfee76e082284dc07444a355953f5cd195ebef0be92569807ba37ea42e11270
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.5 MB (85469356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157c2fa3e01c07071962d495fea8cd925b82787d13575557aad43261fd561fdd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 02:38:30 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 01 Dec 2023 02:38:32 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates
# Fri, 01 Dec 2023 02:38:33 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version
# Fri, 01 Dec 2023 02:38:34 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Sat, 06 Jan 2024 01:03:47 GMT
ENV INFLUXDB_VERSION=2.7.5
# Sat, 06 Jan 2024 01:03:50 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version
# Sat, 06 Jan 2024 01:03:51 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Sat, 06 Jan 2024 01:03:53 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version
# Sat, 06 Jan 2024 01:03:53 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Sat, 06 Jan 2024 01:03:53 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Sat, 06 Jan 2024 01:03:53 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Sat, 06 Jan 2024 01:03:53 GMT
COPY file:6341d1dd8e0763e797b79985007acd07a4686ed831d55018f6e390823bad9d07 in /entrypoint.sh 
# Sat, 06 Jan 2024 01:03:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 06 Jan 2024 01:03:54 GMT
CMD ["influxd"]
# Sat, 06 Jan 2024 01:03:54 GMT
EXPOSE 8086
# Sat, 06 Jan 2024 01:03:54 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Sat, 06 Jan 2024 01:03:54 GMT
ENV INFLUXD_INIT_PORT=9999
# Sat, 06 Jan 2024 01:03:54 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Sat, 06 Jan 2024 01:03:54 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00f6ef2d119bdc2b844474b1941025c80c2a28072d415011a971ae3decceb4b8`  
		Last Modified: Fri, 01 Dec 2023 02:38:57 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:219bc19aefdfdc9e712e2ec3f522b6c95b46d8dae4636b4b03232218da21c862`  
		Last Modified: Fri, 01 Dec 2023 02:38:56 GMT  
		Size: 9.0 MB (8962300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ab1ea2040c57ec0c558d867e958ce9b8a15733f2326db44f915514e5470c78`  
		Last Modified: Fri, 01 Dec 2023 02:38:56 GMT  
		Size: 5.5 MB (5463804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53259412624c68cecc9445d0b50dbc35bf444a2c697cbdc53b52ed4780636169`  
		Last Modified: Fri, 01 Dec 2023 02:38:55 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87145c6e0372946a30c8245655c2702467816aa41e25f49c2a121bb6c61dabae`  
		Last Modified: Sat, 06 Jan 2024 01:04:29 GMT  
		Size: 46.0 MB (46039229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae80be9a96244e3849f5578aa655d3227024f56f32caf6fa82717a7a9ce31c5c`  
		Last Modified: Sat, 06 Jan 2024 01:04:27 GMT  
		Size: 21.7 MB (21662623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:051246ccae3512022888f9d8a2a9510cbf7967f60b1d73d911066c7ae9c2d1e1`  
		Last Modified: Sat, 06 Jan 2024 01:04:25 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7043070bf5663305c763d0c98fdc6868951caed4094ae4e5559d8289fad4342e`  
		Last Modified: Sat, 06 Jan 2024 01:04:25 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c3efb09d292ab2a4a5afd4fd35adcf0d268cf56aa84e05dfde023e2728f491`  
		Last Modified: Sat, 06 Jan 2024 01:04:25 GMT  
		Size: 6.3 KB (6280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:latest`

```console
$ docker pull influxdb@sha256:f3765ab8ae6c9fddebe36b95ce1a85097c92146573d1a809dfe7bed60920a2d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:ec5d16059e3bab61d11c556ca6ab17601c32163f084605d7e6787aeb36b78e8a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164680218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a1b63100937139a749eef826781458bb4e3418e51481a02483b8d91891a6115`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:54 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Thu, 11 Jan 2024 02:37:54 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:09:41 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 04:09:43 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version
# Thu, 11 Jan 2024 04:09:44 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb
# Thu, 11 Jan 2024 04:09:44 GMT
ENV GOSU_VER=1.16
# Thu, 11 Jan 2024 04:09:47 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true
# Thu, 11 Jan 2024 04:09:47 GMT
ENV INFLUXDB_VERSION=2.7.5
# Thu, 11 Jan 2024 04:09:52 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version
# Thu, 11 Jan 2024 04:09:52 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 11 Jan 2024 04:09:54 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version
# Thu, 11 Jan 2024 04:09:55 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Thu, 11 Jan 2024 04:09:55 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 11 Jan 2024 04:09:55 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Thu, 11 Jan 2024 04:09:55 GMT
COPY file:b5520696339eadb7386055c1dc9487351aa145a79b0cf206d8b1a79699c4a7f1 in /entrypoint.sh 
# Thu, 11 Jan 2024 04:09:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 04:09:55 GMT
CMD ["influxd"]
# Thu, 11 Jan 2024 04:09:56 GMT
EXPOSE 8086
# Thu, 11 Jan 2024 04:09:56 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 11 Jan 2024 04:09:56 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 11 Jan 2024 04:09:56 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 11 Jan 2024 04:09:56 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b879f7f0b97813db2ab558426c6245d7493ec849b5c6af62bae7b50557a079`  
		Last Modified: Thu, 11 Jan 2024 04:10:39 GMT  
		Size: 9.8 MB (9784548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:391f2a95149104db5eaf7dbe8761c8a7c58af0a0ecee1872febe45d407b6bbfb`  
		Last Modified: Thu, 11 Jan 2024 04:10:36 GMT  
		Size: 5.8 MB (5820928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc0f8d17c9bcf98af54ddd62f93ee6c90fef24a7c33149fb2e49dfb19791ca43`  
		Last Modified: Thu, 11 Jan 2024 04:10:36 GMT  
		Size: 3.3 KB (3279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eea0149521594e79d232332b04ff4dd56e9e9a290f087f52e6fc59bbe8baf33`  
		Last Modified: Thu, 11 Jan 2024 04:10:36 GMT  
		Size: 1.0 MB (1006418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c74718bd32e2b889be8c94b089e9d388f009188f6c1dfda5ec4509cce504e45d`  
		Last Modified: Thu, 11 Jan 2024 04:10:44 GMT  
		Size: 95.8 MB (95803956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab287bfba4b08c4fc84caa53c34ca8abf0e7c77cb2ab01ef3a47b560be60a843`  
		Last Modified: Thu, 11 Jan 2024 04:10:36 GMT  
		Size: 23.1 MB (23128347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f5135083ba7e52dd2ef5fd0312e737a280b3571aa04d6e3a29dceff332b9e5`  
		Last Modified: Thu, 11 Jan 2024 04:10:34 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8acfea7e99e37cfd1049d98a07b95312addf03bb176a003941d5406bc6c08bb6`  
		Last Modified: Thu, 11 Jan 2024 04:10:34 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c3fd5840e752ea1c9222f0db53080b5b73d5405b82bc84dc23843ff4b7eec54`  
		Last Modified: Thu, 11 Jan 2024 04:10:34 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:832eece17bb962f211cdf029f6155c7f8e1cd4cacd724cedb2a7750107f6bb7f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.9 MB (158897627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007c75ff8554e420da151e20acab90e091664c8eb0fd542f6b436f2a75af5274`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:44 GMT
ADD file:70e4f0c71f88c97c8db279b998c10d4943954d304ff9f51875c3699a4dc5ee4e in / 
# Thu, 11 Jan 2024 02:40:45 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:26:57 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 06:26:59 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version
# Thu, 11 Jan 2024 06:26:59 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb
# Thu, 11 Jan 2024 06:26:59 GMT
ENV GOSU_VER=1.16
# Thu, 11 Jan 2024 06:27:02 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true
# Thu, 11 Jan 2024 06:27:02 GMT
ENV INFLUXDB_VERSION=2.7.5
# Thu, 11 Jan 2024 06:27:07 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version
# Thu, 11 Jan 2024 06:27:08 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 11 Jan 2024 06:27:10 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version
# Thu, 11 Jan 2024 06:27:10 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Thu, 11 Jan 2024 06:27:10 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 11 Jan 2024 06:27:10 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Thu, 11 Jan 2024 06:27:10 GMT
COPY file:b5520696339eadb7386055c1dc9487351aa145a79b0cf206d8b1a79699c4a7f1 in /entrypoint.sh 
# Thu, 11 Jan 2024 06:27:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 06:27:11 GMT
CMD ["influxd"]
# Thu, 11 Jan 2024 06:27:11 GMT
EXPOSE 8086
# Thu, 11 Jan 2024 06:27:11 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 11 Jan 2024 06:27:11 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 11 Jan 2024 06:27:11 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 11 Jan 2024 06:27:11 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:a5573528b1f0cf2f5d87c94fe0aee9d8967d5de98258be9303c3c6fa477824ec`  
		Last Modified: Thu, 11 Jan 2024 02:44:04 GMT  
		Size: 29.2 MB (29157335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c543f2ded9d87bd3e5368772a656ec9fb9b23ec5ee4f05f71f1c8f1360986cb4`  
		Last Modified: Thu, 11 Jan 2024 06:27:27 GMT  
		Size: 9.6 MB (9581384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b2acc1b1088cec4796cd50c6c115abf7a1743d6e99eae37f1c6d9e53169cb3`  
		Last Modified: Thu, 11 Jan 2024 06:27:25 GMT  
		Size: 5.5 MB (5463785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b127df0dcec919697c30c0bd266c00db0a975dd94dd9a063b6379aeb2ae83611`  
		Last Modified: Thu, 11 Jan 2024 06:27:24 GMT  
		Size: 3.3 KB (3281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b420d207f0e0e7a91b25f8dfa4a01b17f5a2bd19cf8ee824cf4668bc0c2dc098`  
		Last Modified: Thu, 11 Jan 2024 06:27:24 GMT  
		Size: 936.1 KB (936110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95615c5c923baa13098b8ca4486f8c22c80d43fa26c52f7e193db8698ec6b08e`  
		Last Modified: Thu, 11 Jan 2024 06:27:29 GMT  
		Size: 92.1 MB (92086314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe791de1db4830776f0821dd1cdc1582a6d62b94081a3deb9b03674488e7a72`  
		Last Modified: Thu, 11 Jan 2024 06:27:25 GMT  
		Size: 21.7 MB (21662599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2529595ecc4ff3cb1b2beaeba3882be93bd2993e6df3b89b5171e6a47d3a8efb`  
		Last Modified: Thu, 11 Jan 2024 06:27:22 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2075d0de8ccfa8a6e386a205b6923de74cf542b584d725d5e056b44a51a95704`  
		Last Modified: Thu, 11 Jan 2024 06:27:22 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0464a5461d0b1958c954d476b3ebcf76f1787c78f1958f84363aac3168a78aa`  
		Last Modified: Thu, 11 Jan 2024 06:27:22 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
