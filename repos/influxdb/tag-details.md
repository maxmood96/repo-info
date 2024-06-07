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
$ docker pull influxdb@sha256:7dcd2b410ad7367985b1ffd3b16d34b78b5f3ec3ca662d86d4bafff46b0262f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-data` - linux; amd64

```console
$ docker pull influxdb@sha256:276af3d063062c0287f04f3721c43b12d827957499e379ffa72a7034f826dfac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112245550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce389eeddfef97f017a8d9b54f945aa208c9a1165c92190da36b026f8b00d624`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 14 May 2024 01:28:14 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Tue, 14 May 2024 01:28:14 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:56:07 GMT
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
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f0bf643eb6745d5c7e9bada33de1786ab2350240206a1956fa506a1b47b129`  
		Last Modified: Tue, 14 May 2024 03:05:14 GMT  
		Size: 15.8 MB (15764867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434101e3e9c96213149fa0c388a472dc21206701eb3aa8a1d852341d20e8bbe6`  
		Last Modified: Thu, 06 Jun 2024 21:56:37 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b85310671b22718a284fb4129bbd0537a94cb8b384a7d878a25b6fbffbcfda`  
		Last Modified: Thu, 06 Jun 2024 21:56:38 GMT  
		Size: 41.4 MB (41377729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1dbbaef9d7068895fc037aec247b6f90761ceb0960f70a8a3ce58ed1c386e6a`  
		Last Modified: Thu, 06 Jun 2024 21:56:37 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6140dbede20e6e7fd9c9ede9998f7fe1aa6e12e01a8d30b5c517acb15e25c33`  
		Last Modified: Thu, 06 Jun 2024 21:56:31 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e73028f77aac2fa3b46bc35582c8d6816fe1fc934e09731fc2e497c2c4a040`  
		Last Modified: Thu, 06 Jun 2024 21:56:32 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:17e7df6b39149b28b62c9de9c1ff69fa18a75f40022842d37173e7bf38e25924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4593883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b9d1aa12a6827b227ca5268274e593add1a5ccbbe6fceea0059f0542fa094d6`

```dockerfile
```

-	Layers:
	-	`sha256:d993e6fd9fc398b1fba70c069e88a573a2f7d090e973f94b52609cc4e9cdc22b`  
		Last Modified: Thu, 06 Jun 2024 21:56:37 GMT  
		Size: 4.6 MB (4579309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96e510bc3307967df07fc2294f62706be6e57271bd5843dfd12f73afbea56fe5`  
		Last Modified: Thu, 06 Jun 2024 21:56:37 GMT  
		Size: 14.6 KB (14574 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10-data-alpine`

```console
$ docker pull influxdb@sha256:82dbe88ce511d1e82766fc9c8dffa36a6e5df809879d4d2662a08999cae97619
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:f26b553900ce1858479a83a57bc7fe7e8bf3da393f0affeb4e062c7bc02715ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46177238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b6bd49ace02e032d44906f1bb4699694687ca1cef2c52d80647d1b8c49fccf8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
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
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2284974491a6901d5a66daad9c850c24f6400ec3536c9d2ebad76cb03b731d6`  
		Last Modified: Thu, 06 Jun 2024 21:56:29 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8f6e6b6f873cf27293143b9e38672eb9ac2be7ea0d7ece04ee4b4a07cad94a`  
		Last Modified: Thu, 06 Jun 2024 21:56:29 GMT  
		Size: 1.2 MB (1231162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e97f0e3f871221e418f4b5f6ba09172ea9c8ae9873da311479efabb72ba861a`  
		Last Modified: Thu, 06 Jun 2024 21:56:30 GMT  
		Size: 41.3 MB (41321931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a7e8e25125db82d5694d85cf2de1a239c73e3411dcfe9bcc14da24ba0162c5`  
		Last Modified: Thu, 06 Jun 2024 21:56:29 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b18d3754c72aa6a7ba01fe23cbb06d46af758b76082dd636547c65bc35da6731`  
		Last Modified: Thu, 06 Jun 2024 21:56:30 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7b7e8a2bb8e8e9a80fc0bd5e42b8407ff8d7c7737503511940ae843682b9e2`  
		Last Modified: Thu, 06 Jun 2024 21:56:30 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:a785b97c0df21d517e739406a03dd6cfa80de9aaea4409103ce9658faa77187c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **744.4 KB (744413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15639e0017302fbbd2ecb05a45a1daee75c4ac2505f7fafbcb5e6fdbfbf1175e`

```dockerfile
```

-	Layers:
	-	`sha256:84a7ba3c9004f2d362810cf7b6d9ad080827777ed1a3a0d975947e53f5e8c97b`  
		Last Modified: Thu, 06 Jun 2024 21:56:29 GMT  
		Size: 728.0 KB (727989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b102390a0e6ce368130954848656074611b4b7f1f29aa6e116bb519063da56b1`  
		Last Modified: Thu, 06 Jun 2024 21:56:29 GMT  
		Size: 16.4 KB (16424 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10-meta`

```console
$ docker pull influxdb@sha256:a9be20b78979a208693fca07969d348c354531b481528477a32940faa0595ae2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:460dd596e7b607a869bdd29bc11f953297948756af55265290f1ab271f95a23a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.0 MB (90962132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d5265bcd9e4569e510966627d2a2b3c6ccae3f349377ed1d456b19bd79904e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 14 May 2024 01:28:14 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Tue, 14 May 2024 01:28:14 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:56:07 GMT
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
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f0bf643eb6745d5c7e9bada33de1786ab2350240206a1956fa506a1b47b129`  
		Last Modified: Tue, 14 May 2024 03:05:14 GMT  
		Size: 15.8 MB (15764867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a7d23667c74dc59b4b04873fce3a1cf3bed5b3f7d0e64fc2878ad2b44dd088`  
		Last Modified: Thu, 06 Jun 2024 21:56:32 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa9ab9e1898874a026d70ca13df9a769dcf7d2f32ffc7e264dfb83b565b0577`  
		Last Modified: Thu, 06 Jun 2024 21:56:33 GMT  
		Size: 20.1 MB (20095532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d78463457702eb8cc8a7f0191949de8d504c07eacf710bd2178647b75e913a`  
		Last Modified: Thu, 06 Jun 2024 21:56:32 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70b8d13cb020b8a970405678624130b08847cadb6344c90daa40727f57bc0ba`  
		Last Modified: Thu, 06 Jun 2024 21:56:32 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:e3ff19ba089e74d463d2bba0f09f27f42226091f41c7cad6ebc67a0aa498f2c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4529115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bddee5b35ce608af0df02a2b2c7aba81f0c304a6c79700fc06c1cf92592bd6e5`

```dockerfile
```

-	Layers:
	-	`sha256:b4e888b214838f41ab93cd216cd9326f2437590fc2b78ed86ebfdda0aaebe9a2`  
		Last Modified: Thu, 06 Jun 2024 21:56:33 GMT  
		Size: 4.5 MB (4516194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c270fcb3de29175d45f2665c7f7f6deb4052bf4ee184e9a59da8b84cb9767c7`  
		Last Modified: Thu, 06 Jun 2024 21:56:32 GMT  
		Size: 12.9 KB (12921 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10-meta-alpine`

```console
$ docker pull influxdb@sha256:aef5f72ff02d611180dd14a7b642e0be908711c1b34be5a0e8e03ab2fedac8e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:cdcba1a2d84708d6cc0a196257968136cf1fd6678c0ef8f6023afabe030cabea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.9 MB (24896212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a3c26c9c86df010e5d4a687a47f91dcc4fd03f748ac3322665d18a2bd6e796`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
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
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add49343fc55d2f6606751192a99955e557bdf2fbf187b9f496ebf652a930d7d`  
		Last Modified: Thu, 06 Jun 2024 21:56:29 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c04b9b056eb6ed78c191900752590b6eeac62fb265ce1355b387b1f8e225cb9`  
		Last Modified: Thu, 06 Jun 2024 21:56:29 GMT  
		Size: 1.2 MB (1231162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b92feb1683c48d36eab756da22a43affed657ce67772e0f74715beabcb8a8b`  
		Last Modified: Thu, 06 Jun 2024 21:56:29 GMT  
		Size: 20.0 MB (20042110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b5c4eed12698239c9012f6459d894a1e5f257292b2af354adf791ebc1f2c62d`  
		Last Modified: Thu, 06 Jun 2024 21:56:29 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16bda331172dd8504154fef1b6dc9bcbd808c222bad6557ce86131364c1d2968`  
		Last Modified: Thu, 06 Jun 2024 21:56:30 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:07edd3bd52c8c17cf11d19d3e115aef86b61d6ba0e76c2eb74bc83e66c391365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **679.9 KB (679923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99fa662d3b91538dd46613645bdb5fe77016070282c2a937f47842499091afdb`

```dockerfile
```

-	Layers:
	-	`sha256:fea6e8c0b253bf8985c6ab911b31efb96d9209ae9488ed19b80f743f7032af31`  
		Last Modified: Thu, 06 Jun 2024 21:56:29 GMT  
		Size: 665.1 KB (665136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf739b2a8aad94ca9d8d0d929cf2f20dd09f15f50365af04fd8d18c1ba524a3e`  
		Last Modified: Thu, 06 Jun 2024 21:56:29 GMT  
		Size: 14.8 KB (14787 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10.7-data`

```console
$ docker pull influxdb@sha256:7dcd2b410ad7367985b1ffd3b16d34b78b5f3ec3ca662d86d4bafff46b0262f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.7-data` - linux; amd64

```console
$ docker pull influxdb@sha256:276af3d063062c0287f04f3721c43b12d827957499e379ffa72a7034f826dfac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112245550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce389eeddfef97f017a8d9b54f945aa208c9a1165c92190da36b026f8b00d624`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 14 May 2024 01:28:14 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Tue, 14 May 2024 01:28:14 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:56:07 GMT
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
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f0bf643eb6745d5c7e9bada33de1786ab2350240206a1956fa506a1b47b129`  
		Last Modified: Tue, 14 May 2024 03:05:14 GMT  
		Size: 15.8 MB (15764867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434101e3e9c96213149fa0c388a472dc21206701eb3aa8a1d852341d20e8bbe6`  
		Last Modified: Thu, 06 Jun 2024 21:56:37 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b85310671b22718a284fb4129bbd0537a94cb8b384a7d878a25b6fbffbcfda`  
		Last Modified: Thu, 06 Jun 2024 21:56:38 GMT  
		Size: 41.4 MB (41377729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1dbbaef9d7068895fc037aec247b6f90761ceb0960f70a8a3ce58ed1c386e6a`  
		Last Modified: Thu, 06 Jun 2024 21:56:37 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6140dbede20e6e7fd9c9ede9998f7fe1aa6e12e01a8d30b5c517acb15e25c33`  
		Last Modified: Thu, 06 Jun 2024 21:56:31 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e73028f77aac2fa3b46bc35582c8d6816fe1fc934e09731fc2e497c2c4a040`  
		Last Modified: Thu, 06 Jun 2024 21:56:32 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.7-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:17e7df6b39149b28b62c9de9c1ff69fa18a75f40022842d37173e7bf38e25924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4593883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b9d1aa12a6827b227ca5268274e593add1a5ccbbe6fceea0059f0542fa094d6`

```dockerfile
```

-	Layers:
	-	`sha256:d993e6fd9fc398b1fba70c069e88a573a2f7d090e973f94b52609cc4e9cdc22b`  
		Last Modified: Thu, 06 Jun 2024 21:56:37 GMT  
		Size: 4.6 MB (4579309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96e510bc3307967df07fc2294f62706be6e57271bd5843dfd12f73afbea56fe5`  
		Last Modified: Thu, 06 Jun 2024 21:56:37 GMT  
		Size: 14.6 KB (14574 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10.7-data-alpine`

```console
$ docker pull influxdb@sha256:82dbe88ce511d1e82766fc9c8dffa36a6e5df809879d4d2662a08999cae97619
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.7-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:f26b553900ce1858479a83a57bc7fe7e8bf3da393f0affeb4e062c7bc02715ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46177238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b6bd49ace02e032d44906f1bb4699694687ca1cef2c52d80647d1b8c49fccf8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
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
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2284974491a6901d5a66daad9c850c24f6400ec3536c9d2ebad76cb03b731d6`  
		Last Modified: Thu, 06 Jun 2024 21:56:29 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8f6e6b6f873cf27293143b9e38672eb9ac2be7ea0d7ece04ee4b4a07cad94a`  
		Last Modified: Thu, 06 Jun 2024 21:56:29 GMT  
		Size: 1.2 MB (1231162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e97f0e3f871221e418f4b5f6ba09172ea9c8ae9873da311479efabb72ba861a`  
		Last Modified: Thu, 06 Jun 2024 21:56:30 GMT  
		Size: 41.3 MB (41321931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a7e8e25125db82d5694d85cf2de1a239c73e3411dcfe9bcc14da24ba0162c5`  
		Last Modified: Thu, 06 Jun 2024 21:56:29 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b18d3754c72aa6a7ba01fe23cbb06d46af758b76082dd636547c65bc35da6731`  
		Last Modified: Thu, 06 Jun 2024 21:56:30 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7b7e8a2bb8e8e9a80fc0bd5e42b8407ff8d7c7737503511940ae843682b9e2`  
		Last Modified: Thu, 06 Jun 2024 21:56:30 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.7-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:a785b97c0df21d517e739406a03dd6cfa80de9aaea4409103ce9658faa77187c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **744.4 KB (744413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15639e0017302fbbd2ecb05a45a1daee75c4ac2505f7fafbcb5e6fdbfbf1175e`

```dockerfile
```

-	Layers:
	-	`sha256:84a7ba3c9004f2d362810cf7b6d9ad080827777ed1a3a0d975947e53f5e8c97b`  
		Last Modified: Thu, 06 Jun 2024 21:56:29 GMT  
		Size: 728.0 KB (727989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b102390a0e6ce368130954848656074611b4b7f1f29aa6e116bb519063da56b1`  
		Last Modified: Thu, 06 Jun 2024 21:56:29 GMT  
		Size: 16.4 KB (16424 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10.7-meta`

```console
$ docker pull influxdb@sha256:a9be20b78979a208693fca07969d348c354531b481528477a32940faa0595ae2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.7-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:460dd596e7b607a869bdd29bc11f953297948756af55265290f1ab271f95a23a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.0 MB (90962132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d5265bcd9e4569e510966627d2a2b3c6ccae3f349377ed1d456b19bd79904e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 14 May 2024 01:28:14 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Tue, 14 May 2024 01:28:14 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:56:07 GMT
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
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f0bf643eb6745d5c7e9bada33de1786ab2350240206a1956fa506a1b47b129`  
		Last Modified: Tue, 14 May 2024 03:05:14 GMT  
		Size: 15.8 MB (15764867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a7d23667c74dc59b4b04873fce3a1cf3bed5b3f7d0e64fc2878ad2b44dd088`  
		Last Modified: Thu, 06 Jun 2024 21:56:32 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa9ab9e1898874a026d70ca13df9a769dcf7d2f32ffc7e264dfb83b565b0577`  
		Last Modified: Thu, 06 Jun 2024 21:56:33 GMT  
		Size: 20.1 MB (20095532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d78463457702eb8cc8a7f0191949de8d504c07eacf710bd2178647b75e913a`  
		Last Modified: Thu, 06 Jun 2024 21:56:32 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70b8d13cb020b8a970405678624130b08847cadb6344c90daa40727f57bc0ba`  
		Last Modified: Thu, 06 Jun 2024 21:56:32 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.7-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:e3ff19ba089e74d463d2bba0f09f27f42226091f41c7cad6ebc67a0aa498f2c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4529115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bddee5b35ce608af0df02a2b2c7aba81f0c304a6c79700fc06c1cf92592bd6e5`

```dockerfile
```

-	Layers:
	-	`sha256:b4e888b214838f41ab93cd216cd9326f2437590fc2b78ed86ebfdda0aaebe9a2`  
		Last Modified: Thu, 06 Jun 2024 21:56:33 GMT  
		Size: 4.5 MB (4516194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c270fcb3de29175d45f2665c7f7f6deb4052bf4ee184e9a59da8b84cb9767c7`  
		Last Modified: Thu, 06 Jun 2024 21:56:32 GMT  
		Size: 12.9 KB (12921 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10.7-meta-alpine`

```console
$ docker pull influxdb@sha256:aef5f72ff02d611180dd14a7b642e0be908711c1b34be5a0e8e03ab2fedac8e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.7-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:cdcba1a2d84708d6cc0a196257968136cf1fd6678c0ef8f6023afabe030cabea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.9 MB (24896212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a3c26c9c86df010e5d4a687a47f91dcc4fd03f748ac3322665d18a2bd6e796`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
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
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add49343fc55d2f6606751192a99955e557bdf2fbf187b9f496ebf652a930d7d`  
		Last Modified: Thu, 06 Jun 2024 21:56:29 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c04b9b056eb6ed78c191900752590b6eeac62fb265ce1355b387b1f8e225cb9`  
		Last Modified: Thu, 06 Jun 2024 21:56:29 GMT  
		Size: 1.2 MB (1231162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b92feb1683c48d36eab756da22a43affed657ce67772e0f74715beabcb8a8b`  
		Last Modified: Thu, 06 Jun 2024 21:56:29 GMT  
		Size: 20.0 MB (20042110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b5c4eed12698239c9012f6459d894a1e5f257292b2af354adf791ebc1f2c62d`  
		Last Modified: Thu, 06 Jun 2024 21:56:29 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16bda331172dd8504154fef1b6dc9bcbd808c222bad6557ce86131364c1d2968`  
		Last Modified: Thu, 06 Jun 2024 21:56:30 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.7-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:07edd3bd52c8c17cf11d19d3e115aef86b61d6ba0e76c2eb74bc83e66c391365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **679.9 KB (679923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99fa662d3b91538dd46613645bdb5fe77016070282c2a937f47842499091afdb`

```dockerfile
```

-	Layers:
	-	`sha256:fea6e8c0b253bf8985c6ab911b31efb96d9209ae9488ed19b80f743f7032af31`  
		Last Modified: Thu, 06 Jun 2024 21:56:29 GMT  
		Size: 665.1 KB (665136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf739b2a8aad94ca9d8d0d929cf2f20dd09f15f50365af04fd8d18c1ba524a3e`  
		Last Modified: Thu, 06 Jun 2024 21:56:29 GMT  
		Size: 14.8 KB (14787 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-data`

```console
$ docker pull influxdb@sha256:26146a7f23278781cd4e61c60c2721d822c7c92ad748d0a21d1b2c1ab4b95229
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data` - linux; amd64

```console
$ docker pull influxdb@sha256:b30661746ab2e7003de6122049e5d40845dd196fcdca2432e198e180723aa55b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115452734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a571e5ed944f5e210f1bc7bb8d0e699b87e6f6b313acf00ec96dda50530fbce`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 14 May 2024 01:27:51 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 14 May 2024 01:27:51 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:54:40 GMT
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
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891494355808bdd3db5552f0d3723fd0fa826675f774853796fafa221d850d42`  
		Last Modified: Tue, 14 May 2024 03:04:06 GMT  
		Size: 24.1 MB (24050100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af2c6d02abdcc7ec0b2175ca14cd9f229dd59dbb478b959dda203927ea0de45`  
		Last Modified: Thu, 06 Jun 2024 21:56:33 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aff66de57fbc80888c0d0671442cb60a88d8d5ffcf84cf8b3dba007b4901875`  
		Last Modified: Thu, 06 Jun 2024 21:56:34 GMT  
		Size: 41.8 MB (41822701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a7e8e25125db82d5694d85cf2de1a239c73e3411dcfe9bcc14da24ba0162c5`  
		Last Modified: Thu, 06 Jun 2024 21:56:29 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b18d3754c72aa6a7ba01fe23cbb06d46af758b76082dd636547c65bc35da6731`  
		Last Modified: Thu, 06 Jun 2024 21:56:30 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7b7e8a2bb8e8e9a80fc0bd5e42b8407ff8d7c7737503511940ae843682b9e2`  
		Last Modified: Thu, 06 Jun 2024 21:56:30 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:a92154232e03161e1ab993a46036a593e419f156b1dba18247d50dee3745d876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4469120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c0ca5da93758b3875b92751cb634e5a512e6d7995848035240f8777c890d20f`

```dockerfile
```

-	Layers:
	-	`sha256:93d70164e55302a2adaa9d5d926cefd4be0ed3f5ef1b44fb2490c5be3d5f35f9`  
		Last Modified: Thu, 06 Jun 2024 21:56:33 GMT  
		Size: 4.5 MB (4454546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b0d4af90b546b29c21212558d0491ba764dec52e0eeeca99470afb4d91170ac`  
		Last Modified: Thu, 06 Jun 2024 21:56:33 GMT  
		Size: 14.6 KB (14574 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-data-alpine`

```console
$ docker pull influxdb@sha256:10347cdc44d1021944da150e1b37621afc1c2322f0b827b65acecc607ae94cac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:46fd52516bb145642c781a860535d31aa97ac601573f98688a50137bf5b858e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46629791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ce115663f7b549ac95016d0fc96155f4e63c64b075a5fc53b2643149b3523b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
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
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5465a51397ea3eaced4b36f85aa661b9d42b79c6c14d51cfc51ba043689fdb`  
		Last Modified: Thu, 06 Jun 2024 21:56:27 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbaa2b2dc60a82d6d473406d8e2aa752e20a11dd0342067ba4971fc217d73ad`  
		Last Modified: Thu, 06 Jun 2024 21:56:31 GMT  
		Size: 1.2 MB (1231161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c953b4a7cec1eee954ab26c9ec75b8c8fbc1b5814703f6f438cd15837f43a6`  
		Last Modified: Thu, 06 Jun 2024 21:56:32 GMT  
		Size: 41.8 MB (41774485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a59fef432ae186ac3fabed896a5d8361c4f64d829f8fba5d0d704e0ae8e221`  
		Last Modified: Thu, 06 Jun 2024 21:56:31 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6140dbede20e6e7fd9c9ede9998f7fe1aa6e12e01a8d30b5c517acb15e25c33`  
		Last Modified: Thu, 06 Jun 2024 21:56:31 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e73028f77aac2fa3b46bc35582c8d6816fe1fc934e09731fc2e497c2c4a040`  
		Last Modified: Thu, 06 Jun 2024 21:56:32 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:7d6a509182619f250e17c1cfe4ca2b443bc22313b89c192bfb7be60bd322dfaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **744.1 KB (744101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:534d77225de5fcc8282a85481fa894360df24fefaa6fc44693bfc81075c2ad33`

```dockerfile
```

-	Layers:
	-	`sha256:d6a08932ee1fda6a84cabe4695b2d7c5392c7759762e991321ece4c324c82642`  
		Last Modified: Thu, 06 Jun 2024 21:56:31 GMT  
		Size: 727.7 KB (727677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7944243a54df737969e062b596fa6febf361b28c97790e27a2e5c91c3b3df8e5`  
		Last Modified: Thu, 06 Jun 2024 21:56:31 GMT  
		Size: 16.4 KB (16424 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-meta`

```console
$ docker pull influxdb@sha256:7f7aa7ec6ae88677deb93503b738b42bd5ebf3fec370feabf34bdbbf067793b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:2e30d06caddb37acbb0e0c7bd230bb83d91fd12459c26b7ec31daf9ecc12ccae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (94021859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0425bf322ee892f6676dba2cdc3209ef556360d08d6fa59b49b1f98725f7f691`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 14 May 2024 01:27:51 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 14 May 2024 01:27:51 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:54:40 GMT
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
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891494355808bdd3db5552f0d3723fd0fa826675f774853796fafa221d850d42`  
		Last Modified: Tue, 14 May 2024 03:04:06 GMT  
		Size: 24.1 MB (24050100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a7d23667c74dc59b4b04873fce3a1cf3bed5b3f7d0e64fc2878ad2b44dd088`  
		Last Modified: Thu, 06 Jun 2024 21:56:32 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe797f143f3e2a40246308c072b22fc675f3dfd9b871d7117d30e5b0eb46b38`  
		Last Modified: Thu, 06 Jun 2024 21:56:32 GMT  
		Size: 20.4 MB (20393032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb834e2b449baed0d9d3f7a3c9035eee7d44d33bbbc533fb73b0bc1f02ded6d`  
		Last Modified: Thu, 06 Jun 2024 21:56:32 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20dfb34e747912d3593151e5c76d35843030410daeffffa5833aa4477b84b5fd`  
		Last Modified: Thu, 06 Jun 2024 21:56:28 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:927a2fdb1ba28be9a842a737885dbdcc683e5a4eeab489db0cd596e725b4458e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4404907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77f98770eb73b4f7b40d3d57cb812e4dfb8450008c4845d8c309cd0b28979bba`

```dockerfile
```

-	Layers:
	-	`sha256:78e1d9ad343e7d7703de655cd4290c2a67f90cd80d5cc1a0b9a8b461c20b8e0b`  
		Last Modified: Thu, 06 Jun 2024 21:56:32 GMT  
		Size: 4.4 MB (4391986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:195b2ef5864880b1b47a09c2303c9d830d61dec75d6769267b8fed9113c0aecc`  
		Last Modified: Thu, 06 Jun 2024 21:56:32 GMT  
		Size: 12.9 KB (12921 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-meta-alpine`

```console
$ docker pull influxdb@sha256:3f9cb9a9d759b42c183833963a1e8b0df60b5a3ae819d4fb02fb299f3b7384cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:bc17c0a02e313b286e811b166e491ebcffd7794e5155e7e76c6eb9a08d061f1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25199485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:949d73240e1037bf36eacf00e87f55744f4365d7b83c6e42bc15046167389eef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
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
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5465a51397ea3eaced4b36f85aa661b9d42b79c6c14d51cfc51ba043689fdb`  
		Last Modified: Thu, 06 Jun 2024 21:56:27 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de23102befc785708548d111e6cc1c9a36faeb324b4c5c54ed3a66a7723f1647`  
		Last Modified: Thu, 06 Jun 2024 21:56:27 GMT  
		Size: 1.2 MB (1231178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86bedbe2a4646c1cc1b2ba84e5f0506e7fd014831332da3b29e279f558f0790`  
		Last Modified: Thu, 06 Jun 2024 21:56:27 GMT  
		Size: 20.3 MB (20345367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54fcc6b4e7b1450a084f83a18acefd947866d1abd97cc960d32ec1b1cba1f996`  
		Last Modified: Thu, 06 Jun 2024 21:56:27 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20dfb34e747912d3593151e5c76d35843030410daeffffa5833aa4477b84b5fd`  
		Last Modified: Thu, 06 Jun 2024 21:56:28 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:dddd5c49bb7f165c9f7fcb94646aeb7f8653b2c46280a855c54f497c0905943c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **680.8 KB (680798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15541ce468bab39e1369cdad03bca71892675fa2b2070987e314c98c0e32e592`

```dockerfile
```

-	Layers:
	-	`sha256:c1ec890aa98566f94e3c934b954aec9b21437d101ccd72e04833a6b8b1757f73`  
		Last Modified: Thu, 06 Jun 2024 21:56:27 GMT  
		Size: 666.0 KB (666010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c1194a449822fdbfc5c2de358308f1abbb4567f55c3d3e2412cb52ccd8c212a`  
		Last Modified: Thu, 06 Jun 2024 21:56:27 GMT  
		Size: 14.8 KB (14788 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.5-data`

```console
$ docker pull influxdb@sha256:26146a7f23278781cd4e61c60c2721d822c7c92ad748d0a21d1b2c1ab4b95229
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.5-data` - linux; amd64

```console
$ docker pull influxdb@sha256:b30661746ab2e7003de6122049e5d40845dd196fcdca2432e198e180723aa55b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115452734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a571e5ed944f5e210f1bc7bb8d0e699b87e6f6b313acf00ec96dda50530fbce`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 14 May 2024 01:27:51 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 14 May 2024 01:27:51 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:54:40 GMT
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
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891494355808bdd3db5552f0d3723fd0fa826675f774853796fafa221d850d42`  
		Last Modified: Tue, 14 May 2024 03:04:06 GMT  
		Size: 24.1 MB (24050100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af2c6d02abdcc7ec0b2175ca14cd9f229dd59dbb478b959dda203927ea0de45`  
		Last Modified: Thu, 06 Jun 2024 21:56:33 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aff66de57fbc80888c0d0671442cb60a88d8d5ffcf84cf8b3dba007b4901875`  
		Last Modified: Thu, 06 Jun 2024 21:56:34 GMT  
		Size: 41.8 MB (41822701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a7e8e25125db82d5694d85cf2de1a239c73e3411dcfe9bcc14da24ba0162c5`  
		Last Modified: Thu, 06 Jun 2024 21:56:29 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b18d3754c72aa6a7ba01fe23cbb06d46af758b76082dd636547c65bc35da6731`  
		Last Modified: Thu, 06 Jun 2024 21:56:30 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7b7e8a2bb8e8e9a80fc0bd5e42b8407ff8d7c7737503511940ae843682b9e2`  
		Last Modified: Thu, 06 Jun 2024 21:56:30 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.5-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:a92154232e03161e1ab993a46036a593e419f156b1dba18247d50dee3745d876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4469120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c0ca5da93758b3875b92751cb634e5a512e6d7995848035240f8777c890d20f`

```dockerfile
```

-	Layers:
	-	`sha256:93d70164e55302a2adaa9d5d926cefd4be0ed3f5ef1b44fb2490c5be3d5f35f9`  
		Last Modified: Thu, 06 Jun 2024 21:56:33 GMT  
		Size: 4.5 MB (4454546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b0d4af90b546b29c21212558d0491ba764dec52e0eeeca99470afb4d91170ac`  
		Last Modified: Thu, 06 Jun 2024 21:56:33 GMT  
		Size: 14.6 KB (14574 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.5-data-alpine`

```console
$ docker pull influxdb@sha256:10347cdc44d1021944da150e1b37621afc1c2322f0b827b65acecc607ae94cac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.5-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:46fd52516bb145642c781a860535d31aa97ac601573f98688a50137bf5b858e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46629791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ce115663f7b549ac95016d0fc96155f4e63c64b075a5fc53b2643149b3523b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
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
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5465a51397ea3eaced4b36f85aa661b9d42b79c6c14d51cfc51ba043689fdb`  
		Last Modified: Thu, 06 Jun 2024 21:56:27 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbaa2b2dc60a82d6d473406d8e2aa752e20a11dd0342067ba4971fc217d73ad`  
		Last Modified: Thu, 06 Jun 2024 21:56:31 GMT  
		Size: 1.2 MB (1231161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c953b4a7cec1eee954ab26c9ec75b8c8fbc1b5814703f6f438cd15837f43a6`  
		Last Modified: Thu, 06 Jun 2024 21:56:32 GMT  
		Size: 41.8 MB (41774485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a59fef432ae186ac3fabed896a5d8361c4f64d829f8fba5d0d704e0ae8e221`  
		Last Modified: Thu, 06 Jun 2024 21:56:31 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6140dbede20e6e7fd9c9ede9998f7fe1aa6e12e01a8d30b5c517acb15e25c33`  
		Last Modified: Thu, 06 Jun 2024 21:56:31 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e73028f77aac2fa3b46bc35582c8d6816fe1fc934e09731fc2e497c2c4a040`  
		Last Modified: Thu, 06 Jun 2024 21:56:32 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.5-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:7d6a509182619f250e17c1cfe4ca2b443bc22313b89c192bfb7be60bd322dfaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **744.1 KB (744101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:534d77225de5fcc8282a85481fa894360df24fefaa6fc44693bfc81075c2ad33`

```dockerfile
```

-	Layers:
	-	`sha256:d6a08932ee1fda6a84cabe4695b2d7c5392c7759762e991321ece4c324c82642`  
		Last Modified: Thu, 06 Jun 2024 21:56:31 GMT  
		Size: 727.7 KB (727677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7944243a54df737969e062b596fa6febf361b28c97790e27a2e5c91c3b3df8e5`  
		Last Modified: Thu, 06 Jun 2024 21:56:31 GMT  
		Size: 16.4 KB (16424 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.5-meta`

```console
$ docker pull influxdb@sha256:7f7aa7ec6ae88677deb93503b738b42bd5ebf3fec370feabf34bdbbf067793b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.5-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:2e30d06caddb37acbb0e0c7bd230bb83d91fd12459c26b7ec31daf9ecc12ccae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (94021859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0425bf322ee892f6676dba2cdc3209ef556360d08d6fa59b49b1f98725f7f691`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 14 May 2024 01:27:51 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 14 May 2024 01:27:51 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:54:40 GMT
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
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891494355808bdd3db5552f0d3723fd0fa826675f774853796fafa221d850d42`  
		Last Modified: Tue, 14 May 2024 03:04:06 GMT  
		Size: 24.1 MB (24050100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a7d23667c74dc59b4b04873fce3a1cf3bed5b3f7d0e64fc2878ad2b44dd088`  
		Last Modified: Thu, 06 Jun 2024 21:56:32 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe797f143f3e2a40246308c072b22fc675f3dfd9b871d7117d30e5b0eb46b38`  
		Last Modified: Thu, 06 Jun 2024 21:56:32 GMT  
		Size: 20.4 MB (20393032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb834e2b449baed0d9d3f7a3c9035eee7d44d33bbbc533fb73b0bc1f02ded6d`  
		Last Modified: Thu, 06 Jun 2024 21:56:32 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20dfb34e747912d3593151e5c76d35843030410daeffffa5833aa4477b84b5fd`  
		Last Modified: Thu, 06 Jun 2024 21:56:28 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.5-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:927a2fdb1ba28be9a842a737885dbdcc683e5a4eeab489db0cd596e725b4458e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4404907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77f98770eb73b4f7b40d3d57cb812e4dfb8450008c4845d8c309cd0b28979bba`

```dockerfile
```

-	Layers:
	-	`sha256:78e1d9ad343e7d7703de655cd4290c2a67f90cd80d5cc1a0b9a8b461c20b8e0b`  
		Last Modified: Thu, 06 Jun 2024 21:56:32 GMT  
		Size: 4.4 MB (4391986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:195b2ef5864880b1b47a09c2303c9d830d61dec75d6769267b8fed9113c0aecc`  
		Last Modified: Thu, 06 Jun 2024 21:56:32 GMT  
		Size: 12.9 KB (12921 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.5-meta-alpine`

```console
$ docker pull influxdb@sha256:3f9cb9a9d759b42c183833963a1e8b0df60b5a3ae819d4fb02fb299f3b7384cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.5-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:bc17c0a02e313b286e811b166e491ebcffd7794e5155e7e76c6eb9a08d061f1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25199485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:949d73240e1037bf36eacf00e87f55744f4365d7b83c6e42bc15046167389eef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
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
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5465a51397ea3eaced4b36f85aa661b9d42b79c6c14d51cfc51ba043689fdb`  
		Last Modified: Thu, 06 Jun 2024 21:56:27 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de23102befc785708548d111e6cc1c9a36faeb324b4c5c54ed3a66a7723f1647`  
		Last Modified: Thu, 06 Jun 2024 21:56:27 GMT  
		Size: 1.2 MB (1231178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86bedbe2a4646c1cc1b2ba84e5f0506e7fd014831332da3b29e279f558f0790`  
		Last Modified: Thu, 06 Jun 2024 21:56:27 GMT  
		Size: 20.3 MB (20345367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54fcc6b4e7b1450a084f83a18acefd947866d1abd97cc960d32ec1b1cba1f996`  
		Last Modified: Thu, 06 Jun 2024 21:56:27 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20dfb34e747912d3593151e5c76d35843030410daeffffa5833aa4477b84b5fd`  
		Last Modified: Thu, 06 Jun 2024 21:56:28 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.5-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:dddd5c49bb7f165c9f7fcb94646aeb7f8653b2c46280a855c54f497c0905943c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **680.8 KB (680798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15541ce468bab39e1369cdad03bca71892675fa2b2070987e314c98c0e32e592`

```dockerfile
```

-	Layers:
	-	`sha256:c1ec890aa98566f94e3c934b954aec9b21437d101ccd72e04833a6b8b1757f73`  
		Last Modified: Thu, 06 Jun 2024 21:56:27 GMT  
		Size: 666.0 KB (666010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c1194a449822fdbfc5c2de358308f1abbb4567f55c3d3e2412cb52ccd8c212a`  
		Last Modified: Thu, 06 Jun 2024 21:56:27 GMT  
		Size: 14.8 KB (14788 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.8`

```console
$ docker pull influxdb@sha256:29c4e3fac2812551342527632be9ac3b2829f13678fdade247a0ba3982bc7513
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
$ docker pull influxdb@sha256:d4d40ae941faa645d37df6f98e189be91da80bc005272efc359b09b5cb099d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125753194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2357db11646d0645c9c20880060e04e7b9dadaccf083c3b7ac9cfd6e48923879`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 14 May 2024 01:28:14 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Tue, 14 May 2024 01:28:14 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:56:07 GMT
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
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f0bf643eb6745d5c7e9bada33de1786ab2350240206a1956fa506a1b47b129`  
		Last Modified: Tue, 14 May 2024 03:05:14 GMT  
		Size: 15.8 MB (15764867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa7bd5ba4f20866b189db6c707e9e8f0433bb15472e668c649bdc5239512619`  
		Last Modified: Thu, 06 Jun 2024 21:56:33 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea21890576bbdd4e82e7752993808fa2febf6ddf10c52624df0e13c24860270b`  
		Last Modified: Thu, 06 Jun 2024 21:56:34 GMT  
		Size: 54.9 MB (54885429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b112a19f35fb5435492869648e2b62f07b1887d23ada0e076027c4be71b053`  
		Last Modified: Thu, 06 Jun 2024 21:56:33 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7ab70378500d0af9349f443b8ec2ade7f793338df3ae52f70670c1ef74b969`  
		Last Modified: Thu, 06 Jun 2024 21:56:33 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3da46e48dabe22874150185e11f3939f469006272ef5854673045f4267294f`  
		Last Modified: Thu, 06 Jun 2024 21:56:34 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:c9bfcb4fb16942db08b5401637e7f76ac0e6842f8c4983599a6556c036dc94a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4478485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ccbf5d0ff5b76410887dd709c286da8fe10532aa51a121a85393f2579d7fbd2`

```dockerfile
```

-	Layers:
	-	`sha256:6f8d9ae5c1305b6692a768c7a2ab98f4d522c4d7b3266e50ade789d7fb6a18ae`  
		Last Modified: Thu, 06 Jun 2024 21:56:33 GMT  
		Size: 4.5 MB (4463023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8e3e4a2648f453a5fdb91b388d75090a84c1f3761c5ee3158663c33fac8ac72`  
		Last Modified: Thu, 06 Jun 2024 21:56:33 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.8` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:31c228295914f3ae217aa2edf7ebeaa6940a2141f468ea1dfc75be397974f617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116753146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:091f4444417e36da60765f35810ab3d6553b7dc001dbdb4599d70bae92997b62`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 14 May 2024 01:08:54 GMT
ADD file:e0e66bc918a84b9ec6caaae1380270276be179a5864b6234a18c001b3e94f855 in / 
# Tue, 14 May 2024 01:08:54 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:37:12 GMT
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
	-	`sha256:ebc97a184476667a6a83dfc0759e34e05bc66d258ece39a010b6273982b4dc57`  
		Last Modified: Tue, 14 May 2024 01:13:05 GMT  
		Size: 50.3 MB (50256445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f46483bc34de5be97fb9e8af88e9cf41c36db4eecccc529cc7904ee92a32f72`  
		Last Modified: Tue, 14 May 2024 01:48:02 GMT  
		Size: 14.9 MB (14880295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cac70e08f1e28bd696b53fb566ab397d2b5c19e4c3fa9e912fc13552ef3f27e`  
		Last Modified: Thu, 06 Jun 2024 22:07:07 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e90718085425239de8da2fff1b207675e749d78eac10d10285ca7913a26a63`  
		Last Modified: Thu, 06 Jun 2024 22:07:09 GMT  
		Size: 51.6 MB (51612902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2d1235cae6ff64aada5454ff49119cab9afcac830b7203ea6bff43c059c4ed`  
		Last Modified: Thu, 06 Jun 2024 22:07:08 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c418aff24054589483bfe563b33d28101a121896d31acedb6a866547099e6222`  
		Last Modified: Thu, 06 Jun 2024 22:07:08 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7504fbfb38d8ba5fa9fb1248bf9a853166bd3a5f0637e083f22a1f895018a7`  
		Last Modified: Thu, 06 Jun 2024 22:07:08 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:b08d69f4dab81307846ae6db4f896f411e4466721828003dcdd3dbacafa00318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4480186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04168a0a154908ad1d63fdaa1688fb7280a4cba4f3bcb5f2b67c8ade252d9225`

```dockerfile
```

-	Layers:
	-	`sha256:dd757d383950034e437fe5d7e531e15f73effe70effeca06dd541088f51c3a24`  
		Last Modified: Thu, 06 Jun 2024 22:07:08 GMT  
		Size: 4.5 MB (4464657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13246f5d6fbb94e49db303b644a9e4b0760e9a456855093f683e043d57676592`  
		Last Modified: Thu, 06 Jun 2024 22:07:07 GMT  
		Size: 15.5 KB (15529 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:ed7da84d66ed893d1f4d9820705a34d0a97bff63951ad987fb7326503e862b19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120722918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c93cf83723c98b3e2dfe274145852bf0832a6cc49d31071abe2c84fbadbc1ef9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Apr 2024 14:27:41 GMT
ADD file:43721c605da3f74f0c3f71384780fc0e57e2478b88197672caaf4baa3eddab23 in / 
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=1.8.10
# Tue, 30 Apr 2024 14:27:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb* # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:078d9526cc72763b2db16388f6b511c18a73e3e7f9d229364b3b85a6b5277bc8`  
		Last Modified: Tue, 14 May 2024 00:43:13 GMT  
		Size: 53.7 MB (53738990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691cb555e773cb93573d3bc043d7cf17af1d4819163089dfddab3f4cc971718e`  
		Last Modified: Tue, 14 May 2024 01:53:53 GMT  
		Size: 15.8 MB (15750525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2262e06ef8042a165821b6784ae33c5d70f476d554cf389c6abc35d3570e1faf`  
		Last Modified: Wed, 15 May 2024 10:30:27 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a603a55186a716d56071f71438f076793c5d8aefe1b881a11bdad83d419208`  
		Last Modified: Wed, 15 May 2024 10:30:28 GMT  
		Size: 51.2 MB (51229901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa05cf835851cef9136db0277a84cfddcc6acc72210c7a9884fcea3917cfe8f`  
		Last Modified: Wed, 15 May 2024 10:30:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb02d2aa86c305a962f70559440d76b924eddd7d128782d05c05e021aa7badc0`  
		Last Modified: Wed, 15 May 2024 10:30:27 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d28f6f0235c6a370b10ff479d90afdd26203b3226a701751ba8d51c92a36c4`  
		Last Modified: Wed, 15 May 2024 10:30:28 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:b4e8bc875fcd8451323f2de3328b85365b042a482064d3ecd8ded999e7e62105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4478362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512c0d9b7fb0d29f2a3ae8b900791181ec77f15ef9a3616bcb22ee46ac337d61`

```dockerfile
```

-	Layers:
	-	`sha256:1f78ed01a2f50b1b70184c27144ec58fef1019247b5741b9be13eeb4227d6887`  
		Last Modified: Wed, 15 May 2024 10:30:27 GMT  
		Size: 4.5 MB (4462611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4def6cfd8269618f707e147179c0e05a5c749d69d6eb72f8391c05968378ab3`  
		Last Modified: Wed, 15 May 2024 10:30:27 GMT  
		Size: 15.8 KB (15751 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.8-alpine`

```console
$ docker pull influxdb@sha256:ff68a78c2613757cc137ec48f7a862c6edb0f5a6a1e3fc52d604cb3e036ddd0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.8-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:8da7b4c9ea4e1290de176a2bc593b08de1c53e678db9858a49c3d8754e4fdfc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59507670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65603081c7d10c6afa775ed78364a34f726d21ef37ef8c6c58e28410b3886a4a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=1.8.10
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     chmod +x /usr/src/influxdb-*/influx              /usr/src/influxdb-*/influx_inspect              /usr/src/influxdb-*/influx_stress              /usr/src/influxdb-*/influxd &&    mv /usr/src/influxdb-*/influx        /usr/src/influxdb-*/influx_inspect        /usr/src/influxdb-*/influx_stress         /usr/src/influxdb-*/influxd        /usr/bin/ &&    gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d66e26ed51acf4d96c08bb777b841268e106a7712b3862519b5d7507d4f189`  
		Last Modified: Wed, 01 May 2024 21:52:30 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f1f494dad6160af22c1dc31566a1be8f66250e86a9a9ffcdfbf66c4721973d`  
		Last Modified: Wed, 01 May 2024 21:52:31 GMT  
		Size: 1.5 MB (1479571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead4cfe8a0866f27bab617e5f96f856f1e54bc3c33772f0166fd144e546954d4`  
		Last Modified: Wed, 01 May 2024 21:52:32 GMT  
		Size: 54.6 MB (54646698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba6dd6e0aa4ab870a6f13c45453e45ed0884669946fea824deba36caf1f1f81`  
		Last Modified: Wed, 01 May 2024 21:52:31 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50167d227c71947421041efc1934d2c71aa0be90637fabd044b4649e9b57e25f`  
		Last Modified: Wed, 01 May 2024 21:52:32 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09888d5454928396ab82fa3ccd4f6acfe5853a7f21ef57cbb36fd2cf15fe4632`  
		Last Modified: Wed, 01 May 2024 21:52:32 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:004a0352a5399a0749e2871e2f4a07d65d4623992bf220a1734b7bc140c399dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1001318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dfc61e7b8b3073e626ae1040b147a7bf23356fb904652d854e8d2db80126c42`

```dockerfile
```

-	Layers:
	-	`sha256:a34439932d7458286af23f31a01a9f738f9b8afd789a17d697f9eec6f18e02ff`  
		Last Modified: Wed, 01 May 2024 21:52:31 GMT  
		Size: 983.8 KB (983839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96000468ba486d74f19b0155419e78110d366cf9dba2ea7bf86c977c1475c321`  
		Last Modified: Wed, 01 May 2024 21:52:31 GMT  
		Size: 17.5 KB (17479 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.8.10`

```console
$ docker pull influxdb@sha256:29c4e3fac2812551342527632be9ac3b2829f13678fdade247a0ba3982bc7513
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
$ docker pull influxdb@sha256:d4d40ae941faa645d37df6f98e189be91da80bc005272efc359b09b5cb099d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125753194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2357db11646d0645c9c20880060e04e7b9dadaccf083c3b7ac9cfd6e48923879`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 14 May 2024 01:28:14 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Tue, 14 May 2024 01:28:14 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:56:07 GMT
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
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f0bf643eb6745d5c7e9bada33de1786ab2350240206a1956fa506a1b47b129`  
		Last Modified: Tue, 14 May 2024 03:05:14 GMT  
		Size: 15.8 MB (15764867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa7bd5ba4f20866b189db6c707e9e8f0433bb15472e668c649bdc5239512619`  
		Last Modified: Thu, 06 Jun 2024 21:56:33 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea21890576bbdd4e82e7752993808fa2febf6ddf10c52624df0e13c24860270b`  
		Last Modified: Thu, 06 Jun 2024 21:56:34 GMT  
		Size: 54.9 MB (54885429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b112a19f35fb5435492869648e2b62f07b1887d23ada0e076027c4be71b053`  
		Last Modified: Thu, 06 Jun 2024 21:56:33 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7ab70378500d0af9349f443b8ec2ade7f793338df3ae52f70670c1ef74b969`  
		Last Modified: Thu, 06 Jun 2024 21:56:33 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3da46e48dabe22874150185e11f3939f469006272ef5854673045f4267294f`  
		Last Modified: Thu, 06 Jun 2024 21:56:34 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8.10` - unknown; unknown

```console
$ docker pull influxdb@sha256:c9bfcb4fb16942db08b5401637e7f76ac0e6842f8c4983599a6556c036dc94a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4478485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ccbf5d0ff5b76410887dd709c286da8fe10532aa51a121a85393f2579d7fbd2`

```dockerfile
```

-	Layers:
	-	`sha256:6f8d9ae5c1305b6692a768c7a2ab98f4d522c4d7b3266e50ade789d7fb6a18ae`  
		Last Modified: Thu, 06 Jun 2024 21:56:33 GMT  
		Size: 4.5 MB (4463023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8e3e4a2648f453a5fdb91b388d75090a84c1f3761c5ee3158663c33fac8ac72`  
		Last Modified: Thu, 06 Jun 2024 21:56:33 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.8.10` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:31c228295914f3ae217aa2edf7ebeaa6940a2141f468ea1dfc75be397974f617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116753146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:091f4444417e36da60765f35810ab3d6553b7dc001dbdb4599d70bae92997b62`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 14 May 2024 01:08:54 GMT
ADD file:e0e66bc918a84b9ec6caaae1380270276be179a5864b6234a18c001b3e94f855 in / 
# Tue, 14 May 2024 01:08:54 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:37:12 GMT
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
	-	`sha256:ebc97a184476667a6a83dfc0759e34e05bc66d258ece39a010b6273982b4dc57`  
		Last Modified: Tue, 14 May 2024 01:13:05 GMT  
		Size: 50.3 MB (50256445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f46483bc34de5be97fb9e8af88e9cf41c36db4eecccc529cc7904ee92a32f72`  
		Last Modified: Tue, 14 May 2024 01:48:02 GMT  
		Size: 14.9 MB (14880295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cac70e08f1e28bd696b53fb566ab397d2b5c19e4c3fa9e912fc13552ef3f27e`  
		Last Modified: Thu, 06 Jun 2024 22:07:07 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e90718085425239de8da2fff1b207675e749d78eac10d10285ca7913a26a63`  
		Last Modified: Thu, 06 Jun 2024 22:07:09 GMT  
		Size: 51.6 MB (51612902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2d1235cae6ff64aada5454ff49119cab9afcac830b7203ea6bff43c059c4ed`  
		Last Modified: Thu, 06 Jun 2024 22:07:08 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c418aff24054589483bfe563b33d28101a121896d31acedb6a866547099e6222`  
		Last Modified: Thu, 06 Jun 2024 22:07:08 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7504fbfb38d8ba5fa9fb1248bf9a853166bd3a5f0637e083f22a1f895018a7`  
		Last Modified: Thu, 06 Jun 2024 22:07:08 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8.10` - unknown; unknown

```console
$ docker pull influxdb@sha256:b08d69f4dab81307846ae6db4f896f411e4466721828003dcdd3dbacafa00318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4480186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04168a0a154908ad1d63fdaa1688fb7280a4cba4f3bcb5f2b67c8ade252d9225`

```dockerfile
```

-	Layers:
	-	`sha256:dd757d383950034e437fe5d7e531e15f73effe70effeca06dd541088f51c3a24`  
		Last Modified: Thu, 06 Jun 2024 22:07:08 GMT  
		Size: 4.5 MB (4464657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13246f5d6fbb94e49db303b644a9e4b0760e9a456855093f683e043d57676592`  
		Last Modified: Thu, 06 Jun 2024 22:07:07 GMT  
		Size: 15.5 KB (15529 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.8.10` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:ed7da84d66ed893d1f4d9820705a34d0a97bff63951ad987fb7326503e862b19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120722918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c93cf83723c98b3e2dfe274145852bf0832a6cc49d31071abe2c84fbadbc1ef9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Apr 2024 14:27:41 GMT
ADD file:43721c605da3f74f0c3f71384780fc0e57e2478b88197672caaf4baa3eddab23 in / 
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=1.8.10
# Tue, 30 Apr 2024 14:27:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb* # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:078d9526cc72763b2db16388f6b511c18a73e3e7f9d229364b3b85a6b5277bc8`  
		Last Modified: Tue, 14 May 2024 00:43:13 GMT  
		Size: 53.7 MB (53738990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691cb555e773cb93573d3bc043d7cf17af1d4819163089dfddab3f4cc971718e`  
		Last Modified: Tue, 14 May 2024 01:53:53 GMT  
		Size: 15.8 MB (15750525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2262e06ef8042a165821b6784ae33c5d70f476d554cf389c6abc35d3570e1faf`  
		Last Modified: Wed, 15 May 2024 10:30:27 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a603a55186a716d56071f71438f076793c5d8aefe1b881a11bdad83d419208`  
		Last Modified: Wed, 15 May 2024 10:30:28 GMT  
		Size: 51.2 MB (51229901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa05cf835851cef9136db0277a84cfddcc6acc72210c7a9884fcea3917cfe8f`  
		Last Modified: Wed, 15 May 2024 10:30:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb02d2aa86c305a962f70559440d76b924eddd7d128782d05c05e021aa7badc0`  
		Last Modified: Wed, 15 May 2024 10:30:27 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d28f6f0235c6a370b10ff479d90afdd26203b3226a701751ba8d51c92a36c4`  
		Last Modified: Wed, 15 May 2024 10:30:28 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8.10` - unknown; unknown

```console
$ docker pull influxdb@sha256:b4e8bc875fcd8451323f2de3328b85365b042a482064d3ecd8ded999e7e62105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4478362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512c0d9b7fb0d29f2a3ae8b900791181ec77f15ef9a3616bcb22ee46ac337d61`

```dockerfile
```

-	Layers:
	-	`sha256:1f78ed01a2f50b1b70184c27144ec58fef1019247b5741b9be13eeb4227d6887`  
		Last Modified: Wed, 15 May 2024 10:30:27 GMT  
		Size: 4.5 MB (4462611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4def6cfd8269618f707e147179c0e05a5c749d69d6eb72f8391c05968378ab3`  
		Last Modified: Wed, 15 May 2024 10:30:27 GMT  
		Size: 15.8 KB (15751 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.8.10-alpine`

```console
$ docker pull influxdb@sha256:ff68a78c2613757cc137ec48f7a862c6edb0f5a6a1e3fc52d604cb3e036ddd0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.8.10-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:8da7b4c9ea4e1290de176a2bc593b08de1c53e678db9858a49c3d8754e4fdfc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59507670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65603081c7d10c6afa775ed78364a34f726d21ef37ef8c6c58e28410b3886a4a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=1.8.10
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     chmod +x /usr/src/influxdb-*/influx              /usr/src/influxdb-*/influx_inspect              /usr/src/influxdb-*/influx_stress              /usr/src/influxdb-*/influxd &&    mv /usr/src/influxdb-*/influx        /usr/src/influxdb-*/influx_inspect        /usr/src/influxdb-*/influx_stress         /usr/src/influxdb-*/influxd        /usr/bin/ &&    gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d66e26ed51acf4d96c08bb777b841268e106a7712b3862519b5d7507d4f189`  
		Last Modified: Wed, 01 May 2024 21:52:30 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f1f494dad6160af22c1dc31566a1be8f66250e86a9a9ffcdfbf66c4721973d`  
		Last Modified: Wed, 01 May 2024 21:52:31 GMT  
		Size: 1.5 MB (1479571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead4cfe8a0866f27bab617e5f96f856f1e54bc3c33772f0166fd144e546954d4`  
		Last Modified: Wed, 01 May 2024 21:52:32 GMT  
		Size: 54.6 MB (54646698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba6dd6e0aa4ab870a6f13c45453e45ed0884669946fea824deba36caf1f1f81`  
		Last Modified: Wed, 01 May 2024 21:52:31 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50167d227c71947421041efc1934d2c71aa0be90637fabd044b4649e9b57e25f`  
		Last Modified: Wed, 01 May 2024 21:52:32 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09888d5454928396ab82fa3ccd4f6acfe5853a7f21ef57cbb36fd2cf15fe4632`  
		Last Modified: Wed, 01 May 2024 21:52:32 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8.10-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:004a0352a5399a0749e2871e2f4a07d65d4623992bf220a1734b7bc140c399dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1001318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dfc61e7b8b3073e626ae1040b147a7bf23356fb904652d854e8d2db80126c42`

```dockerfile
```

-	Layers:
	-	`sha256:a34439932d7458286af23f31a01a9f738f9b8afd789a17d697f9eec6f18e02ff`  
		Last Modified: Wed, 01 May 2024 21:52:31 GMT  
		Size: 983.8 KB (983839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96000468ba486d74f19b0155419e78110d366cf9dba2ea7bf86c977c1475c321`  
		Last Modified: Wed, 01 May 2024 21:52:31 GMT  
		Size: 17.5 KB (17479 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.9-data`

```console
$ docker pull influxdb@sha256:7e10ad79a8651d64f63f54fe9f88f9493ca08a32751af6ce226a062d8435d9da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9-data` - linux; amd64

```console
$ docker pull influxdb@sha256:97f42220f0690f2794acffd5969809695c6e382d0d6dcec5856ef1c4384d949e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 MB (104156782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6611bfa4aa15c73bda80038fac5370eafd763bdbbfecd83c677c9a795e010d5a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Apr 2024 14:27:41 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Tue, 30 Apr 2024 14:27:41 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb* # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f0bf643eb6745d5c7e9bada33de1786ab2350240206a1956fa506a1b47b129`  
		Last Modified: Tue, 14 May 2024 03:05:14 GMT  
		Size: 15.8 MB (15764867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c32c4d98fbd052f0f4a536efb88d9b2e144b4bf79cd4cd33df103e28f050341`  
		Last Modified: Tue, 14 May 2024 03:56:37 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a111da990975546bc1bc10a4f3a2f3fc9aed6e72b04c956f60022f23c57c0e4d`  
		Last Modified: Tue, 14 May 2024 03:56:38 GMT  
		Size: 33.3 MB (33288968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c576a03d546526c7fa9ddbd91a423bb7fa7ae9e9d2efd283b823f879cfcd03`  
		Last Modified: Tue, 14 May 2024 03:56:38 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a95386436e7bc24e7c1bc7a1ea073da71f18baace1f0d3ad15b7146d5b8280`  
		Last Modified: Tue, 14 May 2024 03:56:38 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66dad3b6cf1fa9fce1e05e97e5ea30ce4c2ffabf7a5285a5f0d94d4e9a146299`  
		Last Modified: Tue, 14 May 2024 03:56:39 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:dd381bfd53f5fe143e8f84744ff5b8d59cc52efdb5200baac1cf914311ae7321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4584852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4563fe0dd49891093819431100b74d9f46668fb32ab02c6e2420be699231b1d`

```dockerfile
```

-	Layers:
	-	`sha256:7f7d78ef7b467d8de8dc1259a340005af876ee8a55c109b013d499a6374bf522`  
		Last Modified: Tue, 14 May 2024 03:56:38 GMT  
		Size: 4.6 MB (4570028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e6f79ae8daae8946fb6f7554932337202306ff4b540224418a6ad96b3eb94a3`  
		Last Modified: Tue, 14 May 2024 03:56:37 GMT  
		Size: 14.8 KB (14824 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.9-data-alpine`

```console
$ docker pull influxdb@sha256:15d7365e6227e9431db5579e8f141482364c3046af6a1d6be52af335fcbafc07
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:9a0c681e6b278f2e194fbe5452b3459f922d3cb3f2a6d31bfbb90a714ade5e23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 MB (38109822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffbab36ed44522c8d2dec80d16a7ed5a4ffd9e6a44a84054eef7fe7e9637b391`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/etc/influxdb/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a317c2aa42265d50e848acb3635467a3773abf72ae2c7c2b504afe418a10834`  
		Last Modified: Wed, 01 May 2024 21:52:18 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e369ee0d89881d654f2528406cf92ff7a8d541ba7266124369ec2bd44d4c0634`  
		Last Modified: Wed, 01 May 2024 21:52:19 GMT  
		Size: 1.5 MB (1479528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db38a39344c06c8e1a02dbbf4a37994d0eee0ed0b6f584d8b60956915632f20`  
		Last Modified: Wed, 01 May 2024 21:52:19 GMT  
		Size: 33.2 MB (33248839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ae21f968fc95d3825832158c8041d2855e592424710eaf8b5c0b885652f9bc`  
		Last Modified: Wed, 01 May 2024 21:52:18 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483336b199da361cc41931239143ff402ef984b7f73c096c0477f984749bd073`  
		Last Modified: Wed, 01 May 2024 21:52:19 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7b27961f871f2793f18147681fef6f317a0770678efdbb10fb5bea9520dddf`  
		Last Modified: Wed, 01 May 2024 21:52:19 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:cb120e160467668a6e67f9f7b4c95a286948b5ed2166e8aab1294f5bc0c4b26d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1115209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47692d0f47733e5825af244b172ca4816fb810d11cb8b4db2cbefaf8fd3e3a94`

```dockerfile
```

-	Layers:
	-	`sha256:e67d6e6010f71f6a83aa9d1ce76511d4d3203364f25080bd6d2f637a58678ce0`  
		Last Modified: Wed, 01 May 2024 21:52:18 GMT  
		Size: 1.1 MB (1098644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c01e8a120720019fadacc05b56d4022f3247730ee5b0c399b93e61f30bf2151`  
		Last Modified: Wed, 01 May 2024 21:52:18 GMT  
		Size: 16.6 KB (16565 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.9-meta`

```console
$ docker pull influxdb@sha256:6d8de46bca6e9f539c33a887fd934d46a68256eb0df6c919bc576d6c03edbe3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:8a59c5d723c171d1d4dab6dfa0342a746e989c9cc366a565aa98a6111dd73436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83635975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:753bcdee79d21b54f419e45aca96850565deaa1bf32f203b7fe3a591b276f626`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 14 May 2024 01:28:14 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Tue, 14 May 2024 01:28:14 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:56:07 GMT
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
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f0bf643eb6745d5c7e9bada33de1786ab2350240206a1956fa506a1b47b129`  
		Last Modified: Tue, 14 May 2024 03:05:14 GMT  
		Size: 15.8 MB (15764867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1319d1cdbca5b0d4971fe6cf8724ea35750324cbae1993b60d725e8bf8c7f5`  
		Last Modified: Thu, 06 Jun 2024 21:56:24 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f12a346283feab44d210ad18587a239b64fcc9beb5a80c4e157ec7beb4cdb09`  
		Last Modified: Thu, 06 Jun 2024 21:56:25 GMT  
		Size: 12.8 MB (12769358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d2756328981ae4b880150d71896183dde9e45d44fe6e59d8304ec7194b9960`  
		Last Modified: Thu, 06 Jun 2024 21:56:24 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ccecf4da9cb77da188eb67ce52cb890d429e08ac7575a0cc32e84c3c989438e`  
		Last Modified: Thu, 06 Jun 2024 21:56:24 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:c52f273546eb51611718a1899dd61422fc77a13fd4f4025b067a6f9c1ca36969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4529046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88cc486afea8d7fc4087db16104b0068bc842a9f3dc0e4d61ffeb97ba077862a`

```dockerfile
```

-	Layers:
	-	`sha256:727f614bcb9de5e7cd2b689edcf42471bda0daec7dca981ec850bba32ed40f10`  
		Last Modified: Thu, 06 Jun 2024 21:56:24 GMT  
		Size: 4.5 MB (4516158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b124c84d987cd9ec6ebed1320a50eb0f9ae3843f48fbc5b81c56a1e8927cc125`  
		Last Modified: Thu, 06 Jun 2024 21:56:24 GMT  
		Size: 12.9 KB (12888 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.9-meta-alpine`

```console
$ docker pull influxdb@sha256:1b988a39553029f0bdd6abc331bf13dc70ca359a7f570573f5ed597c8cfe2f7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:d28e68f771b23f1a42ccc0c5a41d51f6fc26e18a8a5b4d097df1cfbce92b409c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17575143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c330ed5ebe2d5f5c13a339f8660db7fce3609a6ad5dae0b52844e70befd9c7a6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
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
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ca6dd7051ee7f68a65b6f526c520d7748a90caa86cbdffd6b5c0587146eff3`  
		Last Modified: Thu, 06 Jun 2024 21:56:24 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7049e1fb7b4e8eaa01278c751bafb8a2741ff71e0fa3b0a313eb5548dac9f8c5`  
		Last Modified: Thu, 06 Jun 2024 21:56:24 GMT  
		Size: 1.2 MB (1231172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190ac27b31bcd850f607a58866ce468cdd30626775496c6c5a18168cbe3bde43`  
		Last Modified: Thu, 06 Jun 2024 21:56:24 GMT  
		Size: 12.7 MB (12721034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5969988800f5af670dd7a82fc89ef02efa8ba006a5f37752a933398a6f6df6`  
		Last Modified: Thu, 06 Jun 2024 21:56:24 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354dcac742097e22fa8705281d1416f95fb9565d0ec7875d0145d8abcf653ddb`  
		Last Modified: Thu, 06 Jun 2024 21:56:25 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:96170d06a9ac04fb15e1943cf2a34158a7c240ca2a92552a080b8fd3a4de88b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **679.9 KB (679881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3001c8af2bcc056c0ad7c31848d3f4f924b5d2f89ca8989a9a4564a06388b9c5`

```dockerfile
```

-	Layers:
	-	`sha256:d43dfb2e96983635dd31adde7770bc168a3861bb57b7423ee15d9bffa5842716`  
		Last Modified: Thu, 06 Jun 2024 21:56:24 GMT  
		Size: 665.1 KB (665068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:865bc2bd8f03c533ef8761666da59cdd3a3e7fb3fe59582a708bfe30357b7153`  
		Last Modified: Thu, 06 Jun 2024 21:56:24 GMT  
		Size: 14.8 KB (14813 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.9.13-data`

```console
$ docker pull influxdb@sha256:7e10ad79a8651d64f63f54fe9f88f9493ca08a32751af6ce226a062d8435d9da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9.13-data` - linux; amd64

```console
$ docker pull influxdb@sha256:97f42220f0690f2794acffd5969809695c6e382d0d6dcec5856ef1c4384d949e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 MB (104156782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6611bfa4aa15c73bda80038fac5370eafd763bdbbfecd83c677c9a795e010d5a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Apr 2024 14:27:41 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Tue, 30 Apr 2024 14:27:41 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb* # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f0bf643eb6745d5c7e9bada33de1786ab2350240206a1956fa506a1b47b129`  
		Last Modified: Tue, 14 May 2024 03:05:14 GMT  
		Size: 15.8 MB (15764867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c32c4d98fbd052f0f4a536efb88d9b2e144b4bf79cd4cd33df103e28f050341`  
		Last Modified: Tue, 14 May 2024 03:56:37 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a111da990975546bc1bc10a4f3a2f3fc9aed6e72b04c956f60022f23c57c0e4d`  
		Last Modified: Tue, 14 May 2024 03:56:38 GMT  
		Size: 33.3 MB (33288968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c576a03d546526c7fa9ddbd91a423bb7fa7ae9e9d2efd283b823f879cfcd03`  
		Last Modified: Tue, 14 May 2024 03:56:38 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a95386436e7bc24e7c1bc7a1ea073da71f18baace1f0d3ad15b7146d5b8280`  
		Last Modified: Tue, 14 May 2024 03:56:38 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66dad3b6cf1fa9fce1e05e97e5ea30ce4c2ffabf7a5285a5f0d94d4e9a146299`  
		Last Modified: Tue, 14 May 2024 03:56:39 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9.13-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:dd381bfd53f5fe143e8f84744ff5b8d59cc52efdb5200baac1cf914311ae7321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4584852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4563fe0dd49891093819431100b74d9f46668fb32ab02c6e2420be699231b1d`

```dockerfile
```

-	Layers:
	-	`sha256:7f7d78ef7b467d8de8dc1259a340005af876ee8a55c109b013d499a6374bf522`  
		Last Modified: Tue, 14 May 2024 03:56:38 GMT  
		Size: 4.6 MB (4570028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e6f79ae8daae8946fb6f7554932337202306ff4b540224418a6ad96b3eb94a3`  
		Last Modified: Tue, 14 May 2024 03:56:37 GMT  
		Size: 14.8 KB (14824 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.9.13-data-alpine`

```console
$ docker pull influxdb@sha256:15d7365e6227e9431db5579e8f141482364c3046af6a1d6be52af335fcbafc07
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9.13-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:9a0c681e6b278f2e194fbe5452b3459f922d3cb3f2a6d31bfbb90a714ade5e23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 MB (38109822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffbab36ed44522c8d2dec80d16a7ed5a4ffd9e6a44a84054eef7fe7e9637b391`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/etc/influxdb/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a317c2aa42265d50e848acb3635467a3773abf72ae2c7c2b504afe418a10834`  
		Last Modified: Wed, 01 May 2024 21:52:18 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e369ee0d89881d654f2528406cf92ff7a8d541ba7266124369ec2bd44d4c0634`  
		Last Modified: Wed, 01 May 2024 21:52:19 GMT  
		Size: 1.5 MB (1479528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db38a39344c06c8e1a02dbbf4a37994d0eee0ed0b6f584d8b60956915632f20`  
		Last Modified: Wed, 01 May 2024 21:52:19 GMT  
		Size: 33.2 MB (33248839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ae21f968fc95d3825832158c8041d2855e592424710eaf8b5c0b885652f9bc`  
		Last Modified: Wed, 01 May 2024 21:52:18 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483336b199da361cc41931239143ff402ef984b7f73c096c0477f984749bd073`  
		Last Modified: Wed, 01 May 2024 21:52:19 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7b27961f871f2793f18147681fef6f317a0770678efdbb10fb5bea9520dddf`  
		Last Modified: Wed, 01 May 2024 21:52:19 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9.13-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:cb120e160467668a6e67f9f7b4c95a286948b5ed2166e8aab1294f5bc0c4b26d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1115209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47692d0f47733e5825af244b172ca4816fb810d11cb8b4db2cbefaf8fd3e3a94`

```dockerfile
```

-	Layers:
	-	`sha256:e67d6e6010f71f6a83aa9d1ce76511d4d3203364f25080bd6d2f637a58678ce0`  
		Last Modified: Wed, 01 May 2024 21:52:18 GMT  
		Size: 1.1 MB (1098644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c01e8a120720019fadacc05b56d4022f3247730ee5b0c399b93e61f30bf2151`  
		Last Modified: Wed, 01 May 2024 21:52:18 GMT  
		Size: 16.6 KB (16565 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.9.13-meta`

```console
$ docker pull influxdb@sha256:6d8de46bca6e9f539c33a887fd934d46a68256eb0df6c919bc576d6c03edbe3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9.13-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:8a59c5d723c171d1d4dab6dfa0342a746e989c9cc366a565aa98a6111dd73436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83635975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:753bcdee79d21b54f419e45aca96850565deaa1bf32f203b7fe3a591b276f626`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 14 May 2024 01:28:14 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Tue, 14 May 2024 01:28:14 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:56:07 GMT
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
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f0bf643eb6745d5c7e9bada33de1786ab2350240206a1956fa506a1b47b129`  
		Last Modified: Tue, 14 May 2024 03:05:14 GMT  
		Size: 15.8 MB (15764867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1319d1cdbca5b0d4971fe6cf8724ea35750324cbae1993b60d725e8bf8c7f5`  
		Last Modified: Thu, 06 Jun 2024 21:56:24 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f12a346283feab44d210ad18587a239b64fcc9beb5a80c4e157ec7beb4cdb09`  
		Last Modified: Thu, 06 Jun 2024 21:56:25 GMT  
		Size: 12.8 MB (12769358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d2756328981ae4b880150d71896183dde9e45d44fe6e59d8304ec7194b9960`  
		Last Modified: Thu, 06 Jun 2024 21:56:24 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ccecf4da9cb77da188eb67ce52cb890d429e08ac7575a0cc32e84c3c989438e`  
		Last Modified: Thu, 06 Jun 2024 21:56:24 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9.13-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:c52f273546eb51611718a1899dd61422fc77a13fd4f4025b067a6f9c1ca36969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4529046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88cc486afea8d7fc4087db16104b0068bc842a9f3dc0e4d61ffeb97ba077862a`

```dockerfile
```

-	Layers:
	-	`sha256:727f614bcb9de5e7cd2b689edcf42471bda0daec7dca981ec850bba32ed40f10`  
		Last Modified: Thu, 06 Jun 2024 21:56:24 GMT  
		Size: 4.5 MB (4516158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b124c84d987cd9ec6ebed1320a50eb0f9ae3843f48fbc5b81c56a1e8927cc125`  
		Last Modified: Thu, 06 Jun 2024 21:56:24 GMT  
		Size: 12.9 KB (12888 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.9.13-meta-alpine`

```console
$ docker pull influxdb@sha256:1b988a39553029f0bdd6abc331bf13dc70ca359a7f570573f5ed597c8cfe2f7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9.13-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:d28e68f771b23f1a42ccc0c5a41d51f6fc26e18a8a5b4d097df1cfbce92b409c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17575143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c330ed5ebe2d5f5c13a339f8660db7fce3609a6ad5dae0b52844e70befd9c7a6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
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
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ca6dd7051ee7f68a65b6f526c520d7748a90caa86cbdffd6b5c0587146eff3`  
		Last Modified: Thu, 06 Jun 2024 21:56:24 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7049e1fb7b4e8eaa01278c751bafb8a2741ff71e0fa3b0a313eb5548dac9f8c5`  
		Last Modified: Thu, 06 Jun 2024 21:56:24 GMT  
		Size: 1.2 MB (1231172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190ac27b31bcd850f607a58866ce468cdd30626775496c6c5a18168cbe3bde43`  
		Last Modified: Thu, 06 Jun 2024 21:56:24 GMT  
		Size: 12.7 MB (12721034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5969988800f5af670dd7a82fc89ef02efa8ba006a5f37752a933398a6f6df6`  
		Last Modified: Thu, 06 Jun 2024 21:56:24 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354dcac742097e22fa8705281d1416f95fb9565d0ec7875d0145d8abcf653ddb`  
		Last Modified: Thu, 06 Jun 2024 21:56:25 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9.13-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:96170d06a9ac04fb15e1943cf2a34158a7c240ca2a92552a080b8fd3a4de88b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **679.9 KB (679881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3001c8af2bcc056c0ad7c31848d3f4f924b5d2f89ca8989a9a4564a06388b9c5`

```dockerfile
```

-	Layers:
	-	`sha256:d43dfb2e96983635dd31adde7770bc168a3861bb57b7423ee15d9bffa5842716`  
		Last Modified: Thu, 06 Jun 2024 21:56:24 GMT  
		Size: 665.1 KB (665068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:865bc2bd8f03c533ef8761666da59cdd3a3e7fb3fe59582a708bfe30357b7153`  
		Last Modified: Thu, 06 Jun 2024 21:56:24 GMT  
		Size: 14.8 KB (14813 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2`

```console
$ docker pull influxdb@sha256:c100cf47c4a4e73394826d916e4cb6f8226216c74d86cd6ef5ae1aee3e453485
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2` - linux; amd64

```console
$ docker pull influxdb@sha256:a19cbf37238b732db0715d16c96b5978b1d80ca719f8418139da3b351b15411f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (163963584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26438989c210c2bedb4cc8a4466a650408fec02e41057305b81bbf5e057d5ad5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
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
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f0d0f077f13fa063e6da0176bf1375edd05740ecd91eedd945127a151d8b8d`  
		Last Modified: Thu, 06 Jun 2024 21:56:58 GMT  
		Size: 9.6 MB (9592084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16f5f908077287a06fe76585fd4d160299c93f1a744f62a677424d9d7d1c938`  
		Last Modified: Thu, 06 Jun 2024 21:56:58 GMT  
		Size: 5.8 MB (5820944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01d93328ab43de901f13df07174ef010b6c48a5e522e5b05baff5d8b2aa6a95`  
		Last Modified: Thu, 06 Jun 2024 21:56:57 GMT  
		Size: 3.2 KB (3231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af97c04a7b1dd23460d0f01cee8d5a3524094084e19dcaf9558f64bfe45bcefb`  
		Last Modified: Thu, 06 Jun 2024 21:56:58 GMT  
		Size: 1.0 MB (1006376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed9916e56c29240e5d9e628a385fd242becc2c2536ea8089722cde78bc7006c`  
		Last Modified: Thu, 06 Jun 2024 21:57:01 GMT  
		Size: 95.3 MB (95255495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfb47e74479e213cfaee5aade3a8aa9297e09c349c4ceabcd9559a3109f0948`  
		Last Modified: Thu, 06 Jun 2024 21:57:00 GMT  
		Size: 23.1 MB (23128313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d2f7d5230c8efd76a054466810c17cddd2c41d015a46ce4043a6a35b3e425f`  
		Last Modified: Thu, 06 Jun 2024 21:56:59 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89523b1178add4dd32a8e8209e26d2fc7abb2b3d6bf30bad743a8dcfd0778a6`  
		Last Modified: Thu, 06 Jun 2024 21:56:59 GMT  
		Size: 235.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5142485a7686c153aa1944eae3b94bb8225961b74f9f2cd311802f9b6dfd4b3c`  
		Last Modified: Thu, 06 Jun 2024 21:57:00 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:2664cc8335bb944811926d7389cc5031cfc45c8191204534b28d7b840c89f008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2788702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aafcdaafa9bc9a15d537922cdc513793985642bcc8f7fa49571910e310fd984`

```dockerfile
```

-	Layers:
	-	`sha256:96efee604f5c0474379af9c0cda5e467463f54b0c229094f81c91885f8204a9b`  
		Last Modified: Thu, 06 Jun 2024 21:56:58 GMT  
		Size: 2.8 MB (2755162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d69b5ac6d6088d91582ad47cb3163b980b190325db7bb9570850eda7e61155a`  
		Last Modified: Thu, 06 Jun 2024 21:56:57 GMT  
		Size: 33.5 KB (33540 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:3b699dc75f2a75f81e057a047085b6c016dc575e1acf48a3320af878d5589a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 MB (158094032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8acfacfc83128f2e92d41bea9c1bb8e15e8ff7027b39dcef185e22ab6fbe197`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Apr 2024 14:27:41 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV GOSU_VER=1.16
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=2.7.6
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 30 Apr 2024 14:27:41 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98167288b15823502ff3c008c1bebe0312b59afc732eaf2dec0e61340c46635`  
		Last Modified: Tue, 14 May 2024 17:29:50 GMT  
		Size: 9.4 MB (9388812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91a101ca6ad0fddf0d58a75e2aa3bb06ec6478360acf2382b7e6541b8acce87`  
		Last Modified: Tue, 14 May 2024 17:29:50 GMT  
		Size: 5.5 MB (5463799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85934a06a541a67e972990b0c86ca48db4f2193900c938ac37ff7781246b491`  
		Last Modified: Tue, 14 May 2024 17:29:49 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76eac9bf03788d128473d4585c76d733f0fa758a7a6c6030be6e41d679f4a109`  
		Last Modified: Tue, 14 May 2024 17:29:50 GMT  
		Size: 936.1 KB (936105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2bd9f7fe580a2e35e6ea5dc4651d37e5a7efca901a7771bc3dcc3fcaaa8f03b`  
		Last Modified: Tue, 14 May 2024 17:29:53 GMT  
		Size: 91.5 MB (91453341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1724f8117c2e536d58a8b35800242451c4200dc0e76515c3d8004f5749ea454f`  
		Last Modified: Tue, 14 May 2024 17:29:52 GMT  
		Size: 21.7 MB (21662520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87030b6e2eb8ed62a2f9eec98a69f009a24ca821fa253e7d294609a815139927`  
		Last Modified: Tue, 14 May 2024 17:29:51 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6692a03c0e61ca71e99d6d173185294196b720fcc30dd72bcd1a4b54527bdf9b`  
		Last Modified: Tue, 14 May 2024 17:29:51 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95596ef02d9b608a1e30a9fe24fa90955cc15b2d96d3e8393f0297ae95c173e3`  
		Last Modified: Tue, 14 May 2024 17:29:52 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:86f1191ef06a948e5bacffa42e23b84ebf6cf9e1c0a8258ff8d4b2d7d7a0d7ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2788037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed888077f2bca79d4b912479ff9f356e6f2430ff82f6ed778039f16f8c47918`

```dockerfile
```

-	Layers:
	-	`sha256:19d119d867f247c4f3d37761b112c7335a36f67ce31a2f99fba848e75cce5a13`  
		Last Modified: Tue, 14 May 2024 17:29:50 GMT  
		Size: 2.8 MB (2754542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63537c3dbb581b34d88d4a7c800055a2d489f9d10f6b1adbad109b606ae59a22`  
		Last Modified: Tue, 14 May 2024 17:29:49 GMT  
		Size: 33.5 KB (33495 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2-alpine`

```console
$ docker pull influxdb@sha256:b1abc54ef6c8e2aa60a58c76b7f572e8a180045ecfc8b40e6d6e9799d4c37415
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:7ed3fc60737404a0315136d2a4cf99d746851942d023fcfb83604027cf6c2240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89831672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc18789d716a86c5baac818b929ef561a7a9ff4f1fd745fe14fbd60d1e88df17`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
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
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47248402b3e64f2df827941ec3a7dfd92267f99eb59d46b20dc1b6925af5104`  
		Last Modified: Thu, 06 Jun 2024 21:56:36 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c259972c40947eae7e21c8a803f38759499f6a6c86ec1ad536fdcce7af8d159`  
		Last Modified: Thu, 06 Jun 2024 21:56:36 GMT  
		Size: 9.6 MB (9630583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209e8c5aeb1496e85e6be25ad4e4721c7d1c98693edefe936fab6678bf951bdc`  
		Last Modified: Thu, 06 Jun 2024 21:56:36 GMT  
		Size: 5.8 MB (5820947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30584664dad1325b32a5d8807f4e6f4c6be4609b6f286940e1d0949081a4877b`  
		Last Modified: Thu, 06 Jun 2024 21:56:36 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfe06acd4aae9b282431a51b05b235d4d6a180213a7596dec693bb657919dde`  
		Last Modified: Thu, 06 Jun 2024 21:56:37 GMT  
		Size: 47.6 MB (47621801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1645489aaee50f2ed10b4b5e8d57ef53b2f425790ad3222c51c8c49df67ede13`  
		Last Modified: Thu, 06 Jun 2024 21:56:37 GMT  
		Size: 23.1 MB (23128280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c959b6d1b2ee7931c938ba1e1921252fc4398393c59c41222acb814abaadea93`  
		Last Modified: Thu, 06 Jun 2024 21:56:37 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6701de9f30f251a1c40a4819fb93a1511299282dd73b07839a8ecf6326162b`  
		Last Modified: Thu, 06 Jun 2024 21:56:37 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad646e75626fa638d2893fc3e64a9b9031f18f69553389030ac422cbc19b7498`  
		Last Modified: Thu, 06 Jun 2024 21:56:38 GMT  
		Size: 6.3 KB (6281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:135fef8b4c86fc6348b54aec0de52f8c7e4815f159407c41da8d6dfe2b9dc66e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **887.1 KB (887126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd15ceb5c879375b88d3e2e6f6394d36cf3914d5a22a9cd6a513f77024f6f28`

```dockerfile
```

-	Layers:
	-	`sha256:5f9475980c8c1d912174f5a6b99d3b92c34bee43a9a46b928cd37f5160c178ac`  
		Last Modified: Thu, 06 Jun 2024 21:56:36 GMT  
		Size: 856.4 KB (856379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bb51c962ad6cca24236a7eb3210985b01fbc184d4f224b2690855a705980d4b`  
		Last Modified: Thu, 06 Jun 2024 21:56:36 GMT  
		Size: 30.7 KB (30747 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:a447c7691118e4b944fc4253646a85bdc4dd5d85bc67053aa00407799be5eb98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.2 MB (85195071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88b59f2ea0e777f58a286b6868c8b9c651068837f807657799f230a35d803fec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=2.7.6
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 30 Apr 2024 14:27:41 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e74179715305742e7954518090dcbbc3c0add9c427eeb0a7ae2a70233db410`  
		Last Modified: Wed, 01 May 2024 22:30:24 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c2caa740ce1bd53f19359065530c9b61190044a34f9b68851fb0b76883eeec`  
		Last Modified: Wed, 01 May 2024 22:30:24 GMT  
		Size: 9.0 MB (9005097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc8e03f34f4b44aaeef0577844e031669b08a49e4ad60844581665284bd27b5`  
		Last Modified: Wed, 01 May 2024 22:30:24 GMT  
		Size: 5.5 MB (5463799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f301d47f64728dbf02749d5a89a4276afd3091dfcf5025175626d0549e9966`  
		Last Modified: Wed, 01 May 2024 22:30:24 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e707164649a9968ab55dbd0a9c6b9a40236fc07af816ab780a67c95b06a24dc2`  
		Last Modified: Wed, 01 May 2024 22:30:27 GMT  
		Size: 45.7 MB (45722044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a75ebcf248502332725da8073f88cd2962b663a00d89c4cb4ff08474819278`  
		Last Modified: Wed, 01 May 2024 22:30:26 GMT  
		Size: 21.7 MB (21662519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b005b15de8f90ca32745124d3daacfe3d25494e5c0d920cb284a941018b8c4`  
		Last Modified: Wed, 01 May 2024 22:30:25 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd62367cd346c2f5a62be762cba4e2766a0c0c4b47e90ccf503f3ebcc490e63`  
		Last Modified: Wed, 01 May 2024 22:30:25 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a931c6d2672f2b420e8716757f669bf6c04d82edff90c6c3d2143c3f2b1aee`  
		Last Modified: Wed, 01 May 2024 22:30:26 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:55b507eedf67d40c2aa038c77fb348a7ffa09e8a49a1e5182d434aa2619fec0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1259219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55488d110c8e420ffb50282e47c31d05394a3c5a4810555a149197f4308115e1`

```dockerfile
```

-	Layers:
	-	`sha256:a251dff465e4fd6d762a0530cc733e8edb351699632df99091cc1a1abdc80e8e`  
		Last Modified: Wed, 01 May 2024 22:30:24 GMT  
		Size: 1.2 MB (1228505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dfc68710136fe415ffc99b514fc089af11e92a2f8b5bcef9c5f4309c11ca24d`  
		Last Modified: Wed, 01 May 2024 22:30:24 GMT  
		Size: 30.7 KB (30714 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7`

```console
$ docker pull influxdb@sha256:c100cf47c4a4e73394826d916e4cb6f8226216c74d86cd6ef5ae1aee3e453485
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7` - linux; amd64

```console
$ docker pull influxdb@sha256:a19cbf37238b732db0715d16c96b5978b1d80ca719f8418139da3b351b15411f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (163963584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26438989c210c2bedb4cc8a4466a650408fec02e41057305b81bbf5e057d5ad5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
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
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f0d0f077f13fa063e6da0176bf1375edd05740ecd91eedd945127a151d8b8d`  
		Last Modified: Thu, 06 Jun 2024 21:56:58 GMT  
		Size: 9.6 MB (9592084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16f5f908077287a06fe76585fd4d160299c93f1a744f62a677424d9d7d1c938`  
		Last Modified: Thu, 06 Jun 2024 21:56:58 GMT  
		Size: 5.8 MB (5820944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01d93328ab43de901f13df07174ef010b6c48a5e522e5b05baff5d8b2aa6a95`  
		Last Modified: Thu, 06 Jun 2024 21:56:57 GMT  
		Size: 3.2 KB (3231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af97c04a7b1dd23460d0f01cee8d5a3524094084e19dcaf9558f64bfe45bcefb`  
		Last Modified: Thu, 06 Jun 2024 21:56:58 GMT  
		Size: 1.0 MB (1006376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed9916e56c29240e5d9e628a385fd242becc2c2536ea8089722cde78bc7006c`  
		Last Modified: Thu, 06 Jun 2024 21:57:01 GMT  
		Size: 95.3 MB (95255495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfb47e74479e213cfaee5aade3a8aa9297e09c349c4ceabcd9559a3109f0948`  
		Last Modified: Thu, 06 Jun 2024 21:57:00 GMT  
		Size: 23.1 MB (23128313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d2f7d5230c8efd76a054466810c17cddd2c41d015a46ce4043a6a35b3e425f`  
		Last Modified: Thu, 06 Jun 2024 21:56:59 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89523b1178add4dd32a8e8209e26d2fc7abb2b3d6bf30bad743a8dcfd0778a6`  
		Last Modified: Thu, 06 Jun 2024 21:56:59 GMT  
		Size: 235.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5142485a7686c153aa1944eae3b94bb8225961b74f9f2cd311802f9b6dfd4b3c`  
		Last Modified: Thu, 06 Jun 2024 21:57:00 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:2664cc8335bb944811926d7389cc5031cfc45c8191204534b28d7b840c89f008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2788702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aafcdaafa9bc9a15d537922cdc513793985642bcc8f7fa49571910e310fd984`

```dockerfile
```

-	Layers:
	-	`sha256:96efee604f5c0474379af9c0cda5e467463f54b0c229094f81c91885f8204a9b`  
		Last Modified: Thu, 06 Jun 2024 21:56:58 GMT  
		Size: 2.8 MB (2755162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d69b5ac6d6088d91582ad47cb3163b980b190325db7bb9570850eda7e61155a`  
		Last Modified: Thu, 06 Jun 2024 21:56:57 GMT  
		Size: 33.5 KB (33540 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:3b699dc75f2a75f81e057a047085b6c016dc575e1acf48a3320af878d5589a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 MB (158094032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8acfacfc83128f2e92d41bea9c1bb8e15e8ff7027b39dcef185e22ab6fbe197`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Apr 2024 14:27:41 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV GOSU_VER=1.16
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=2.7.6
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 30 Apr 2024 14:27:41 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98167288b15823502ff3c008c1bebe0312b59afc732eaf2dec0e61340c46635`  
		Last Modified: Tue, 14 May 2024 17:29:50 GMT  
		Size: 9.4 MB (9388812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91a101ca6ad0fddf0d58a75e2aa3bb06ec6478360acf2382b7e6541b8acce87`  
		Last Modified: Tue, 14 May 2024 17:29:50 GMT  
		Size: 5.5 MB (5463799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85934a06a541a67e972990b0c86ca48db4f2193900c938ac37ff7781246b491`  
		Last Modified: Tue, 14 May 2024 17:29:49 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76eac9bf03788d128473d4585c76d733f0fa758a7a6c6030be6e41d679f4a109`  
		Last Modified: Tue, 14 May 2024 17:29:50 GMT  
		Size: 936.1 KB (936105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2bd9f7fe580a2e35e6ea5dc4651d37e5a7efca901a7771bc3dcc3fcaaa8f03b`  
		Last Modified: Tue, 14 May 2024 17:29:53 GMT  
		Size: 91.5 MB (91453341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1724f8117c2e536d58a8b35800242451c4200dc0e76515c3d8004f5749ea454f`  
		Last Modified: Tue, 14 May 2024 17:29:52 GMT  
		Size: 21.7 MB (21662520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87030b6e2eb8ed62a2f9eec98a69f009a24ca821fa253e7d294609a815139927`  
		Last Modified: Tue, 14 May 2024 17:29:51 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6692a03c0e61ca71e99d6d173185294196b720fcc30dd72bcd1a4b54527bdf9b`  
		Last Modified: Tue, 14 May 2024 17:29:51 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95596ef02d9b608a1e30a9fe24fa90955cc15b2d96d3e8393f0297ae95c173e3`  
		Last Modified: Tue, 14 May 2024 17:29:52 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:86f1191ef06a948e5bacffa42e23b84ebf6cf9e1c0a8258ff8d4b2d7d7a0d7ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2788037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed888077f2bca79d4b912479ff9f356e6f2430ff82f6ed778039f16f8c47918`

```dockerfile
```

-	Layers:
	-	`sha256:19d119d867f247c4f3d37761b112c7335a36f67ce31a2f99fba848e75cce5a13`  
		Last Modified: Tue, 14 May 2024 17:29:50 GMT  
		Size: 2.8 MB (2754542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63537c3dbb581b34d88d4a7c800055a2d489f9d10f6b1adbad109b606ae59a22`  
		Last Modified: Tue, 14 May 2024 17:29:49 GMT  
		Size: 33.5 KB (33495 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7-alpine`

```console
$ docker pull influxdb@sha256:b1abc54ef6c8e2aa60a58c76b7f572e8a180045ecfc8b40e6d6e9799d4c37415
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:7ed3fc60737404a0315136d2a4cf99d746851942d023fcfb83604027cf6c2240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89831672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc18789d716a86c5baac818b929ef561a7a9ff4f1fd745fe14fbd60d1e88df17`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
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
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47248402b3e64f2df827941ec3a7dfd92267f99eb59d46b20dc1b6925af5104`  
		Last Modified: Thu, 06 Jun 2024 21:56:36 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c259972c40947eae7e21c8a803f38759499f6a6c86ec1ad536fdcce7af8d159`  
		Last Modified: Thu, 06 Jun 2024 21:56:36 GMT  
		Size: 9.6 MB (9630583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209e8c5aeb1496e85e6be25ad4e4721c7d1c98693edefe936fab6678bf951bdc`  
		Last Modified: Thu, 06 Jun 2024 21:56:36 GMT  
		Size: 5.8 MB (5820947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30584664dad1325b32a5d8807f4e6f4c6be4609b6f286940e1d0949081a4877b`  
		Last Modified: Thu, 06 Jun 2024 21:56:36 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfe06acd4aae9b282431a51b05b235d4d6a180213a7596dec693bb657919dde`  
		Last Modified: Thu, 06 Jun 2024 21:56:37 GMT  
		Size: 47.6 MB (47621801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1645489aaee50f2ed10b4b5e8d57ef53b2f425790ad3222c51c8c49df67ede13`  
		Last Modified: Thu, 06 Jun 2024 21:56:37 GMT  
		Size: 23.1 MB (23128280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c959b6d1b2ee7931c938ba1e1921252fc4398393c59c41222acb814abaadea93`  
		Last Modified: Thu, 06 Jun 2024 21:56:37 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6701de9f30f251a1c40a4819fb93a1511299282dd73b07839a8ecf6326162b`  
		Last Modified: Thu, 06 Jun 2024 21:56:37 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad646e75626fa638d2893fc3e64a9b9031f18f69553389030ac422cbc19b7498`  
		Last Modified: Thu, 06 Jun 2024 21:56:38 GMT  
		Size: 6.3 KB (6281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:135fef8b4c86fc6348b54aec0de52f8c7e4815f159407c41da8d6dfe2b9dc66e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **887.1 KB (887126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd15ceb5c879375b88d3e2e6f6394d36cf3914d5a22a9cd6a513f77024f6f28`

```dockerfile
```

-	Layers:
	-	`sha256:5f9475980c8c1d912174f5a6b99d3b92c34bee43a9a46b928cd37f5160c178ac`  
		Last Modified: Thu, 06 Jun 2024 21:56:36 GMT  
		Size: 856.4 KB (856379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bb51c962ad6cca24236a7eb3210985b01fbc184d4f224b2690855a705980d4b`  
		Last Modified: Thu, 06 Jun 2024 21:56:36 GMT  
		Size: 30.7 KB (30747 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:a447c7691118e4b944fc4253646a85bdc4dd5d85bc67053aa00407799be5eb98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.2 MB (85195071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88b59f2ea0e777f58a286b6868c8b9c651068837f807657799f230a35d803fec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=2.7.6
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 30 Apr 2024 14:27:41 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e74179715305742e7954518090dcbbc3c0add9c427eeb0a7ae2a70233db410`  
		Last Modified: Wed, 01 May 2024 22:30:24 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c2caa740ce1bd53f19359065530c9b61190044a34f9b68851fb0b76883eeec`  
		Last Modified: Wed, 01 May 2024 22:30:24 GMT  
		Size: 9.0 MB (9005097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc8e03f34f4b44aaeef0577844e031669b08a49e4ad60844581665284bd27b5`  
		Last Modified: Wed, 01 May 2024 22:30:24 GMT  
		Size: 5.5 MB (5463799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f301d47f64728dbf02749d5a89a4276afd3091dfcf5025175626d0549e9966`  
		Last Modified: Wed, 01 May 2024 22:30:24 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e707164649a9968ab55dbd0a9c6b9a40236fc07af816ab780a67c95b06a24dc2`  
		Last Modified: Wed, 01 May 2024 22:30:27 GMT  
		Size: 45.7 MB (45722044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a75ebcf248502332725da8073f88cd2962b663a00d89c4cb4ff08474819278`  
		Last Modified: Wed, 01 May 2024 22:30:26 GMT  
		Size: 21.7 MB (21662519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b005b15de8f90ca32745124d3daacfe3d25494e5c0d920cb284a941018b8c4`  
		Last Modified: Wed, 01 May 2024 22:30:25 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd62367cd346c2f5a62be762cba4e2766a0c0c4b47e90ccf503f3ebcc490e63`  
		Last Modified: Wed, 01 May 2024 22:30:25 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a931c6d2672f2b420e8716757f669bf6c04d82edff90c6c3d2143c3f2b1aee`  
		Last Modified: Wed, 01 May 2024 22:30:26 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:55b507eedf67d40c2aa038c77fb348a7ffa09e8a49a1e5182d434aa2619fec0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1259219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55488d110c8e420ffb50282e47c31d05394a3c5a4810555a149197f4308115e1`

```dockerfile
```

-	Layers:
	-	`sha256:a251dff465e4fd6d762a0530cc733e8edb351699632df99091cc1a1abdc80e8e`  
		Last Modified: Wed, 01 May 2024 22:30:24 GMT  
		Size: 1.2 MB (1228505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dfc68710136fe415ffc99b514fc089af11e92a2f8b5bcef9c5f4309c11ca24d`  
		Last Modified: Wed, 01 May 2024 22:30:24 GMT  
		Size: 30.7 KB (30714 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7.6`

```console
$ docker pull influxdb@sha256:c100cf47c4a4e73394826d916e4cb6f8226216c74d86cd6ef5ae1aee3e453485
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7.6` - linux; amd64

```console
$ docker pull influxdb@sha256:a19cbf37238b732db0715d16c96b5978b1d80ca719f8418139da3b351b15411f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (163963584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26438989c210c2bedb4cc8a4466a650408fec02e41057305b81bbf5e057d5ad5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
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
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f0d0f077f13fa063e6da0176bf1375edd05740ecd91eedd945127a151d8b8d`  
		Last Modified: Thu, 06 Jun 2024 21:56:58 GMT  
		Size: 9.6 MB (9592084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16f5f908077287a06fe76585fd4d160299c93f1a744f62a677424d9d7d1c938`  
		Last Modified: Thu, 06 Jun 2024 21:56:58 GMT  
		Size: 5.8 MB (5820944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01d93328ab43de901f13df07174ef010b6c48a5e522e5b05baff5d8b2aa6a95`  
		Last Modified: Thu, 06 Jun 2024 21:56:57 GMT  
		Size: 3.2 KB (3231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af97c04a7b1dd23460d0f01cee8d5a3524094084e19dcaf9558f64bfe45bcefb`  
		Last Modified: Thu, 06 Jun 2024 21:56:58 GMT  
		Size: 1.0 MB (1006376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed9916e56c29240e5d9e628a385fd242becc2c2536ea8089722cde78bc7006c`  
		Last Modified: Thu, 06 Jun 2024 21:57:01 GMT  
		Size: 95.3 MB (95255495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfb47e74479e213cfaee5aade3a8aa9297e09c349c4ceabcd9559a3109f0948`  
		Last Modified: Thu, 06 Jun 2024 21:57:00 GMT  
		Size: 23.1 MB (23128313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d2f7d5230c8efd76a054466810c17cddd2c41d015a46ce4043a6a35b3e425f`  
		Last Modified: Thu, 06 Jun 2024 21:56:59 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89523b1178add4dd32a8e8209e26d2fc7abb2b3d6bf30bad743a8dcfd0778a6`  
		Last Modified: Thu, 06 Jun 2024 21:56:59 GMT  
		Size: 235.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5142485a7686c153aa1944eae3b94bb8225961b74f9f2cd311802f9b6dfd4b3c`  
		Last Modified: Thu, 06 Jun 2024 21:57:00 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.6` - unknown; unknown

```console
$ docker pull influxdb@sha256:2664cc8335bb944811926d7389cc5031cfc45c8191204534b28d7b840c89f008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2788702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aafcdaafa9bc9a15d537922cdc513793985642bcc8f7fa49571910e310fd984`

```dockerfile
```

-	Layers:
	-	`sha256:96efee604f5c0474379af9c0cda5e467463f54b0c229094f81c91885f8204a9b`  
		Last Modified: Thu, 06 Jun 2024 21:56:58 GMT  
		Size: 2.8 MB (2755162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d69b5ac6d6088d91582ad47cb3163b980b190325db7bb9570850eda7e61155a`  
		Last Modified: Thu, 06 Jun 2024 21:56:57 GMT  
		Size: 33.5 KB (33540 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7.6` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:3b699dc75f2a75f81e057a047085b6c016dc575e1acf48a3320af878d5589a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 MB (158094032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8acfacfc83128f2e92d41bea9c1bb8e15e8ff7027b39dcef185e22ab6fbe197`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Apr 2024 14:27:41 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV GOSU_VER=1.16
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=2.7.6
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 30 Apr 2024 14:27:41 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98167288b15823502ff3c008c1bebe0312b59afc732eaf2dec0e61340c46635`  
		Last Modified: Tue, 14 May 2024 17:29:50 GMT  
		Size: 9.4 MB (9388812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91a101ca6ad0fddf0d58a75e2aa3bb06ec6478360acf2382b7e6541b8acce87`  
		Last Modified: Tue, 14 May 2024 17:29:50 GMT  
		Size: 5.5 MB (5463799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85934a06a541a67e972990b0c86ca48db4f2193900c938ac37ff7781246b491`  
		Last Modified: Tue, 14 May 2024 17:29:49 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76eac9bf03788d128473d4585c76d733f0fa758a7a6c6030be6e41d679f4a109`  
		Last Modified: Tue, 14 May 2024 17:29:50 GMT  
		Size: 936.1 KB (936105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2bd9f7fe580a2e35e6ea5dc4651d37e5a7efca901a7771bc3dcc3fcaaa8f03b`  
		Last Modified: Tue, 14 May 2024 17:29:53 GMT  
		Size: 91.5 MB (91453341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1724f8117c2e536d58a8b35800242451c4200dc0e76515c3d8004f5749ea454f`  
		Last Modified: Tue, 14 May 2024 17:29:52 GMT  
		Size: 21.7 MB (21662520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87030b6e2eb8ed62a2f9eec98a69f009a24ca821fa253e7d294609a815139927`  
		Last Modified: Tue, 14 May 2024 17:29:51 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6692a03c0e61ca71e99d6d173185294196b720fcc30dd72bcd1a4b54527bdf9b`  
		Last Modified: Tue, 14 May 2024 17:29:51 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95596ef02d9b608a1e30a9fe24fa90955cc15b2d96d3e8393f0297ae95c173e3`  
		Last Modified: Tue, 14 May 2024 17:29:52 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.6` - unknown; unknown

```console
$ docker pull influxdb@sha256:86f1191ef06a948e5bacffa42e23b84ebf6cf9e1c0a8258ff8d4b2d7d7a0d7ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2788037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed888077f2bca79d4b912479ff9f356e6f2430ff82f6ed778039f16f8c47918`

```dockerfile
```

-	Layers:
	-	`sha256:19d119d867f247c4f3d37761b112c7335a36f67ce31a2f99fba848e75cce5a13`  
		Last Modified: Tue, 14 May 2024 17:29:50 GMT  
		Size: 2.8 MB (2754542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63537c3dbb581b34d88d4a7c800055a2d489f9d10f6b1adbad109b606ae59a22`  
		Last Modified: Tue, 14 May 2024 17:29:49 GMT  
		Size: 33.5 KB (33495 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7.6-alpine`

```console
$ docker pull influxdb@sha256:b1abc54ef6c8e2aa60a58c76b7f572e8a180045ecfc8b40e6d6e9799d4c37415
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7.6-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:7ed3fc60737404a0315136d2a4cf99d746851942d023fcfb83604027cf6c2240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89831672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc18789d716a86c5baac818b929ef561a7a9ff4f1fd745fe14fbd60d1e88df17`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
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
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47248402b3e64f2df827941ec3a7dfd92267f99eb59d46b20dc1b6925af5104`  
		Last Modified: Thu, 06 Jun 2024 21:56:36 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c259972c40947eae7e21c8a803f38759499f6a6c86ec1ad536fdcce7af8d159`  
		Last Modified: Thu, 06 Jun 2024 21:56:36 GMT  
		Size: 9.6 MB (9630583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209e8c5aeb1496e85e6be25ad4e4721c7d1c98693edefe936fab6678bf951bdc`  
		Last Modified: Thu, 06 Jun 2024 21:56:36 GMT  
		Size: 5.8 MB (5820947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30584664dad1325b32a5d8807f4e6f4c6be4609b6f286940e1d0949081a4877b`  
		Last Modified: Thu, 06 Jun 2024 21:56:36 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfe06acd4aae9b282431a51b05b235d4d6a180213a7596dec693bb657919dde`  
		Last Modified: Thu, 06 Jun 2024 21:56:37 GMT  
		Size: 47.6 MB (47621801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1645489aaee50f2ed10b4b5e8d57ef53b2f425790ad3222c51c8c49df67ede13`  
		Last Modified: Thu, 06 Jun 2024 21:56:37 GMT  
		Size: 23.1 MB (23128280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c959b6d1b2ee7931c938ba1e1921252fc4398393c59c41222acb814abaadea93`  
		Last Modified: Thu, 06 Jun 2024 21:56:37 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6701de9f30f251a1c40a4819fb93a1511299282dd73b07839a8ecf6326162b`  
		Last Modified: Thu, 06 Jun 2024 21:56:37 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad646e75626fa638d2893fc3e64a9b9031f18f69553389030ac422cbc19b7498`  
		Last Modified: Thu, 06 Jun 2024 21:56:38 GMT  
		Size: 6.3 KB (6281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.6-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:135fef8b4c86fc6348b54aec0de52f8c7e4815f159407c41da8d6dfe2b9dc66e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **887.1 KB (887126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd15ceb5c879375b88d3e2e6f6394d36cf3914d5a22a9cd6a513f77024f6f28`

```dockerfile
```

-	Layers:
	-	`sha256:5f9475980c8c1d912174f5a6b99d3b92c34bee43a9a46b928cd37f5160c178ac`  
		Last Modified: Thu, 06 Jun 2024 21:56:36 GMT  
		Size: 856.4 KB (856379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bb51c962ad6cca24236a7eb3210985b01fbc184d4f224b2690855a705980d4b`  
		Last Modified: Thu, 06 Jun 2024 21:56:36 GMT  
		Size: 30.7 KB (30747 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7.6-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:a447c7691118e4b944fc4253646a85bdc4dd5d85bc67053aa00407799be5eb98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.2 MB (85195071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88b59f2ea0e777f58a286b6868c8b9c651068837f807657799f230a35d803fec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=2.7.6
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 30 Apr 2024 14:27:41 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e74179715305742e7954518090dcbbc3c0add9c427eeb0a7ae2a70233db410`  
		Last Modified: Wed, 01 May 2024 22:30:24 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c2caa740ce1bd53f19359065530c9b61190044a34f9b68851fb0b76883eeec`  
		Last Modified: Wed, 01 May 2024 22:30:24 GMT  
		Size: 9.0 MB (9005097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc8e03f34f4b44aaeef0577844e031669b08a49e4ad60844581665284bd27b5`  
		Last Modified: Wed, 01 May 2024 22:30:24 GMT  
		Size: 5.5 MB (5463799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f301d47f64728dbf02749d5a89a4276afd3091dfcf5025175626d0549e9966`  
		Last Modified: Wed, 01 May 2024 22:30:24 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e707164649a9968ab55dbd0a9c6b9a40236fc07af816ab780a67c95b06a24dc2`  
		Last Modified: Wed, 01 May 2024 22:30:27 GMT  
		Size: 45.7 MB (45722044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a75ebcf248502332725da8073f88cd2962b663a00d89c4cb4ff08474819278`  
		Last Modified: Wed, 01 May 2024 22:30:26 GMT  
		Size: 21.7 MB (21662519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b005b15de8f90ca32745124d3daacfe3d25494e5c0d920cb284a941018b8c4`  
		Last Modified: Wed, 01 May 2024 22:30:25 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd62367cd346c2f5a62be762cba4e2766a0c0c4b47e90ccf503f3ebcc490e63`  
		Last Modified: Wed, 01 May 2024 22:30:25 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a931c6d2672f2b420e8716757f669bf6c04d82edff90c6c3d2143c3f2b1aee`  
		Last Modified: Wed, 01 May 2024 22:30:26 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.6-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:55b507eedf67d40c2aa038c77fb348a7ffa09e8a49a1e5182d434aa2619fec0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1259219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55488d110c8e420ffb50282e47c31d05394a3c5a4810555a149197f4308115e1`

```dockerfile
```

-	Layers:
	-	`sha256:a251dff465e4fd6d762a0530cc733e8edb351699632df99091cc1a1abdc80e8e`  
		Last Modified: Wed, 01 May 2024 22:30:24 GMT  
		Size: 1.2 MB (1228505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dfc68710136fe415ffc99b514fc089af11e92a2f8b5bcef9c5f4309c11ca24d`  
		Last Modified: Wed, 01 May 2024 22:30:24 GMT  
		Size: 30.7 KB (30714 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:b1abc54ef6c8e2aa60a58c76b7f572e8a180045ecfc8b40e6d6e9799d4c37415
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:7ed3fc60737404a0315136d2a4cf99d746851942d023fcfb83604027cf6c2240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89831672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc18789d716a86c5baac818b929ef561a7a9ff4f1fd745fe14fbd60d1e88df17`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
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
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47248402b3e64f2df827941ec3a7dfd92267f99eb59d46b20dc1b6925af5104`  
		Last Modified: Thu, 06 Jun 2024 21:56:36 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c259972c40947eae7e21c8a803f38759499f6a6c86ec1ad536fdcce7af8d159`  
		Last Modified: Thu, 06 Jun 2024 21:56:36 GMT  
		Size: 9.6 MB (9630583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209e8c5aeb1496e85e6be25ad4e4721c7d1c98693edefe936fab6678bf951bdc`  
		Last Modified: Thu, 06 Jun 2024 21:56:36 GMT  
		Size: 5.8 MB (5820947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30584664dad1325b32a5d8807f4e6f4c6be4609b6f286940e1d0949081a4877b`  
		Last Modified: Thu, 06 Jun 2024 21:56:36 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfe06acd4aae9b282431a51b05b235d4d6a180213a7596dec693bb657919dde`  
		Last Modified: Thu, 06 Jun 2024 21:56:37 GMT  
		Size: 47.6 MB (47621801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1645489aaee50f2ed10b4b5e8d57ef53b2f425790ad3222c51c8c49df67ede13`  
		Last Modified: Thu, 06 Jun 2024 21:56:37 GMT  
		Size: 23.1 MB (23128280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c959b6d1b2ee7931c938ba1e1921252fc4398393c59c41222acb814abaadea93`  
		Last Modified: Thu, 06 Jun 2024 21:56:37 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6701de9f30f251a1c40a4819fb93a1511299282dd73b07839a8ecf6326162b`  
		Last Modified: Thu, 06 Jun 2024 21:56:37 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad646e75626fa638d2893fc3e64a9b9031f18f69553389030ac422cbc19b7498`  
		Last Modified: Thu, 06 Jun 2024 21:56:38 GMT  
		Size: 6.3 KB (6281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:135fef8b4c86fc6348b54aec0de52f8c7e4815f159407c41da8d6dfe2b9dc66e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **887.1 KB (887126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd15ceb5c879375b88d3e2e6f6394d36cf3914d5a22a9cd6a513f77024f6f28`

```dockerfile
```

-	Layers:
	-	`sha256:5f9475980c8c1d912174f5a6b99d3b92c34bee43a9a46b928cd37f5160c178ac`  
		Last Modified: Thu, 06 Jun 2024 21:56:36 GMT  
		Size: 856.4 KB (856379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bb51c962ad6cca24236a7eb3210985b01fbc184d4f224b2690855a705980d4b`  
		Last Modified: Thu, 06 Jun 2024 21:56:36 GMT  
		Size: 30.7 KB (30747 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:a447c7691118e4b944fc4253646a85bdc4dd5d85bc67053aa00407799be5eb98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.2 MB (85195071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88b59f2ea0e777f58a286b6868c8b9c651068837f807657799f230a35d803fec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=2.7.6
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 30 Apr 2024 14:27:41 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e74179715305742e7954518090dcbbc3c0add9c427eeb0a7ae2a70233db410`  
		Last Modified: Wed, 01 May 2024 22:30:24 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c2caa740ce1bd53f19359065530c9b61190044a34f9b68851fb0b76883eeec`  
		Last Modified: Wed, 01 May 2024 22:30:24 GMT  
		Size: 9.0 MB (9005097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc8e03f34f4b44aaeef0577844e031669b08a49e4ad60844581665284bd27b5`  
		Last Modified: Wed, 01 May 2024 22:30:24 GMT  
		Size: 5.5 MB (5463799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f301d47f64728dbf02749d5a89a4276afd3091dfcf5025175626d0549e9966`  
		Last Modified: Wed, 01 May 2024 22:30:24 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e707164649a9968ab55dbd0a9c6b9a40236fc07af816ab780a67c95b06a24dc2`  
		Last Modified: Wed, 01 May 2024 22:30:27 GMT  
		Size: 45.7 MB (45722044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a75ebcf248502332725da8073f88cd2962b663a00d89c4cb4ff08474819278`  
		Last Modified: Wed, 01 May 2024 22:30:26 GMT  
		Size: 21.7 MB (21662519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b005b15de8f90ca32745124d3daacfe3d25494e5c0d920cb284a941018b8c4`  
		Last Modified: Wed, 01 May 2024 22:30:25 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd62367cd346c2f5a62be762cba4e2766a0c0c4b47e90ccf503f3ebcc490e63`  
		Last Modified: Wed, 01 May 2024 22:30:25 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a931c6d2672f2b420e8716757f669bf6c04d82edff90c6c3d2143c3f2b1aee`  
		Last Modified: Wed, 01 May 2024 22:30:26 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:55b507eedf67d40c2aa038c77fb348a7ffa09e8a49a1e5182d434aa2619fec0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1259219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55488d110c8e420ffb50282e47c31d05394a3c5a4810555a149197f4308115e1`

```dockerfile
```

-	Layers:
	-	`sha256:a251dff465e4fd6d762a0530cc733e8edb351699632df99091cc1a1abdc80e8e`  
		Last Modified: Wed, 01 May 2024 22:30:24 GMT  
		Size: 1.2 MB (1228505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dfc68710136fe415ffc99b514fc089af11e92a2f8b5bcef9c5f4309c11ca24d`  
		Last Modified: Wed, 01 May 2024 22:30:24 GMT  
		Size: 30.7 KB (30714 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:latest`

```console
$ docker pull influxdb@sha256:c100cf47c4a4e73394826d916e4cb6f8226216c74d86cd6ef5ae1aee3e453485
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:a19cbf37238b732db0715d16c96b5978b1d80ca719f8418139da3b351b15411f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (163963584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26438989c210c2bedb4cc8a4466a650408fec02e41057305b81bbf5e057d5ad5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
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
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f0d0f077f13fa063e6da0176bf1375edd05740ecd91eedd945127a151d8b8d`  
		Last Modified: Thu, 06 Jun 2024 21:56:58 GMT  
		Size: 9.6 MB (9592084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16f5f908077287a06fe76585fd4d160299c93f1a744f62a677424d9d7d1c938`  
		Last Modified: Thu, 06 Jun 2024 21:56:58 GMT  
		Size: 5.8 MB (5820944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01d93328ab43de901f13df07174ef010b6c48a5e522e5b05baff5d8b2aa6a95`  
		Last Modified: Thu, 06 Jun 2024 21:56:57 GMT  
		Size: 3.2 KB (3231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af97c04a7b1dd23460d0f01cee8d5a3524094084e19dcaf9558f64bfe45bcefb`  
		Last Modified: Thu, 06 Jun 2024 21:56:58 GMT  
		Size: 1.0 MB (1006376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed9916e56c29240e5d9e628a385fd242becc2c2536ea8089722cde78bc7006c`  
		Last Modified: Thu, 06 Jun 2024 21:57:01 GMT  
		Size: 95.3 MB (95255495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfb47e74479e213cfaee5aade3a8aa9297e09c349c4ceabcd9559a3109f0948`  
		Last Modified: Thu, 06 Jun 2024 21:57:00 GMT  
		Size: 23.1 MB (23128313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d2f7d5230c8efd76a054466810c17cddd2c41d015a46ce4043a6a35b3e425f`  
		Last Modified: Thu, 06 Jun 2024 21:56:59 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89523b1178add4dd32a8e8209e26d2fc7abb2b3d6bf30bad743a8dcfd0778a6`  
		Last Modified: Thu, 06 Jun 2024 21:56:59 GMT  
		Size: 235.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5142485a7686c153aa1944eae3b94bb8225961b74f9f2cd311802f9b6dfd4b3c`  
		Last Modified: Thu, 06 Jun 2024 21:57:00 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:2664cc8335bb944811926d7389cc5031cfc45c8191204534b28d7b840c89f008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2788702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aafcdaafa9bc9a15d537922cdc513793985642bcc8f7fa49571910e310fd984`

```dockerfile
```

-	Layers:
	-	`sha256:96efee604f5c0474379af9c0cda5e467463f54b0c229094f81c91885f8204a9b`  
		Last Modified: Thu, 06 Jun 2024 21:56:58 GMT  
		Size: 2.8 MB (2755162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d69b5ac6d6088d91582ad47cb3163b980b190325db7bb9570850eda7e61155a`  
		Last Modified: Thu, 06 Jun 2024 21:56:57 GMT  
		Size: 33.5 KB (33540 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:3b699dc75f2a75f81e057a047085b6c016dc575e1acf48a3320af878d5589a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 MB (158094032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8acfacfc83128f2e92d41bea9c1bb8e15e8ff7027b39dcef185e22ab6fbe197`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Apr 2024 14:27:41 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV GOSU_VER=1.16
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=2.7.6
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 30 Apr 2024 14:27:41 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98167288b15823502ff3c008c1bebe0312b59afc732eaf2dec0e61340c46635`  
		Last Modified: Tue, 14 May 2024 17:29:50 GMT  
		Size: 9.4 MB (9388812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91a101ca6ad0fddf0d58a75e2aa3bb06ec6478360acf2382b7e6541b8acce87`  
		Last Modified: Tue, 14 May 2024 17:29:50 GMT  
		Size: 5.5 MB (5463799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85934a06a541a67e972990b0c86ca48db4f2193900c938ac37ff7781246b491`  
		Last Modified: Tue, 14 May 2024 17:29:49 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76eac9bf03788d128473d4585c76d733f0fa758a7a6c6030be6e41d679f4a109`  
		Last Modified: Tue, 14 May 2024 17:29:50 GMT  
		Size: 936.1 KB (936105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2bd9f7fe580a2e35e6ea5dc4651d37e5a7efca901a7771bc3dcc3fcaaa8f03b`  
		Last Modified: Tue, 14 May 2024 17:29:53 GMT  
		Size: 91.5 MB (91453341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1724f8117c2e536d58a8b35800242451c4200dc0e76515c3d8004f5749ea454f`  
		Last Modified: Tue, 14 May 2024 17:29:52 GMT  
		Size: 21.7 MB (21662520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87030b6e2eb8ed62a2f9eec98a69f009a24ca821fa253e7d294609a815139927`  
		Last Modified: Tue, 14 May 2024 17:29:51 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6692a03c0e61ca71e99d6d173185294196b720fcc30dd72bcd1a4b54527bdf9b`  
		Last Modified: Tue, 14 May 2024 17:29:51 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95596ef02d9b608a1e30a9fe24fa90955cc15b2d96d3e8393f0297ae95c173e3`  
		Last Modified: Tue, 14 May 2024 17:29:52 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:86f1191ef06a948e5bacffa42e23b84ebf6cf9e1c0a8258ff8d4b2d7d7a0d7ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2788037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed888077f2bca79d4b912479ff9f356e6f2430ff82f6ed778039f16f8c47918`

```dockerfile
```

-	Layers:
	-	`sha256:19d119d867f247c4f3d37761b112c7335a36f67ce31a2f99fba848e75cce5a13`  
		Last Modified: Tue, 14 May 2024 17:29:50 GMT  
		Size: 2.8 MB (2754542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63537c3dbb581b34d88d4a7c800055a2d489f9d10f6b1adbad109b606ae59a22`  
		Last Modified: Tue, 14 May 2024 17:29:49 GMT  
		Size: 33.5 KB (33495 bytes)  
		MIME: application/vnd.in-toto+json
