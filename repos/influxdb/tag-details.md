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
$ docker pull influxdb@sha256:24bc1364c9bc23766216617490f74d75ce73851a6b95d1e15c19a7662813e02d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.10-data` - linux; amd64

```console
$ docker pull influxdb@sha256:4083bfb90ce811b71080a025eae3b7fae85e58285078add1d6c9eaaebb5f09ba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.0 MB (111028255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0000062840bf2bd1cb2ad3fe248c873a33699159436df05903b7345987fff4a8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:32 GMT
ADD file:1bf1a123da85382e70ea251091b98fd8b4a1972e4c4e84d392443a4e20b7a135 in / 
# Tue, 13 Feb 2024 00:37:32 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:22:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:19:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 04:20:16 GMT
ENV INFLUXDB_VERSION=1.10.5-c1.10.5
# Tue, 13 Feb 2024 04:20:19 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb*
# Tue, 13 Feb 2024 04:20:20 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Tue, 13 Feb 2024 04:20:20 GMT
EXPOSE 8086
# Tue, 13 Feb 2024 04:20:20 GMT
VOLUME [/var/lib/influxdb]
# Tue, 13 Feb 2024 04:20:20 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Tue, 13 Feb 2024 04:20:20 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 13 Feb 2024 04:20:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 04:20:20 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:09e2bc8a597c33b54cccaf52f2e21798e2e0df79ab6cb33d3b1dfd4b33a57512`  
		Last Modified: Tue, 13 Feb 2024 00:42:21 GMT  
		Size: 55.1 MB (55084838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bbf2983642e080d705d575c1da8d4d8c35507576d88e44979b5c6229573d40`  
		Last Modified: Tue, 13 Feb 2024 01:31:47 GMT  
		Size: 15.8 MB (15763532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670ed7b83ea2bbde7dfba362fa83033db766fdb9e3721f9091229abbf0fafae7`  
		Last Modified: Tue, 13 Feb 2024 04:21:45 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2535204acfeb87be430d22f1f96fb1babe5b524715f0a83abe6a2b6fad86cce4`  
		Last Modified: Tue, 13 Feb 2024 04:22:30 GMT  
		Size: 40.2 MB (40176296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e09e34b464aa67ff02580c0283e401e02fea1b1db62654f01749fef3733527`  
		Last Modified: Tue, 13 Feb 2024 04:22:24 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eebbab0b63679ee777f80b4ec264c8fd5f2ad6652667a947205bc86ddbc20c94`  
		Last Modified: Tue, 13 Feb 2024 04:22:24 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60b6e82e169cb964245a02fbae6d7fad1590c7bd7966485f2a3a29be995bf7f`  
		Last Modified: Tue, 13 Feb 2024 04:22:25 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.10-data-alpine`

```console
$ docker pull influxdb@sha256:6dfc17ec066afcbe913da01f3c965d46b8b39a176f1f526abdaf6f02b41fe921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.10-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:d2dff4365aa609acd0249549c77a7f851430f77ace6a804357b068f25cf55846
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (44987577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99dc5421c026c1d0749f7ec30a7656b3fc85778669e25c4aebb8f64d39293c36`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:40:27 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 27 Jan 2024 05:49:36 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Sat, 27 Jan 2024 05:50:11 GMT
ENV INFLUXDB_VERSION=1.10.5-c1.10.5
# Sat, 27 Jan 2024 05:50:18 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 27 Jan 2024 05:50:18 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Sat, 27 Jan 2024 05:50:18 GMT
EXPOSE 8086
# Sat, 27 Jan 2024 05:50:18 GMT
VOLUME [/var/lib/influxdb]
# Sat, 27 Jan 2024 05:50:18 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Sat, 27 Jan 2024 05:50:18 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sat, 27 Jan 2024 05:50:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 05:50:18 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c332be88cb2898fd00957a6e5a3581893f9a14b30ec2470466897e8b246e9ad`  
		Last Modified: Sat, 27 Jan 2024 03:41:30 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23860728907803516673e82c6dbade4a15e2a3c8d5eb068dac0624d037ca63e`  
		Last Modified: Sat, 27 Jan 2024 05:51:38 GMT  
		Size: 1.5 MB (1472931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27fbb08d778550bb1c887aa19d84266e50cff8f28e9b4a8e3cf87d20f5f838a`  
		Last Modified: Sat, 27 Jan 2024 05:52:23 GMT  
		Size: 40.1 MB (40133166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8dd7fa45bcf36234301be17c9c691a7fccdaa0bde11e7ac60efc4c8a8e53824`  
		Last Modified: Sat, 27 Jan 2024 05:52:17 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76105e1e49ba6dfca3fc5ab0b35b181d117192eca770566d6ba5332023ec6e30`  
		Last Modified: Sat, 27 Jan 2024 05:52:18 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623a6ed184af2fac0feb8725ff46371ba52342c7be76eab853b484a4b796eec7`  
		Last Modified: Sat, 27 Jan 2024 05:52:17 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.10-meta`

```console
$ docker pull influxdb@sha256:fbd58010ff9639e8341aa9ca64953af5baca9cf0e645dc04dfa9fb99f5195b50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.10-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:ca13b09a76be02f422bb7b5df23a558712c878dedc290e59fe88445830b3b72e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91227729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae264f81e79af9845d765331c8a257245b0e630fd730e77fce83d1b79b3b5ccf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:32 GMT
ADD file:1bf1a123da85382e70ea251091b98fd8b4a1972e4c4e84d392443a4e20b7a135 in / 
# Tue, 13 Feb 2024 00:37:32 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:22:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:19:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 04:20:16 GMT
ENV INFLUXDB_VERSION=1.10.5-c1.10.5
# Tue, 13 Feb 2024 04:20:28 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb*
# Tue, 13 Feb 2024 04:20:29 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Tue, 13 Feb 2024 04:20:29 GMT
EXPOSE 8091
# Tue, 13 Feb 2024 04:20:29 GMT
VOLUME [/var/lib/influxdb]
# Tue, 13 Feb 2024 04:20:29 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Tue, 13 Feb 2024 04:20:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 04:20:29 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:09e2bc8a597c33b54cccaf52f2e21798e2e0df79ab6cb33d3b1dfd4b33a57512`  
		Last Modified: Tue, 13 Feb 2024 00:42:21 GMT  
		Size: 55.1 MB (55084838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bbf2983642e080d705d575c1da8d4d8c35507576d88e44979b5c6229573d40`  
		Last Modified: Tue, 13 Feb 2024 01:31:47 GMT  
		Size: 15.8 MB (15763532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670ed7b83ea2bbde7dfba362fa83033db766fdb9e3721f9091229abbf0fafae7`  
		Last Modified: Tue, 13 Feb 2024 04:21:45 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e1461f7f8f001d5f8a48927a411c9bc8a9f96646f0666f653f9fd87ef741c8`  
		Last Modified: Tue, 13 Feb 2024 04:22:43 GMT  
		Size: 20.4 MB (20376971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba33e04eb0c792d8fbd6c17afce7bf7d91dcdc60f6eaf52cd0e554de2e4163b8`  
		Last Modified: Tue, 13 Feb 2024 04:22:40 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ad6e7f2292c68a524d73eb4c5649e27f98ceee419c1d1c1bcecdc0d8a24a9d`  
		Last Modified: Tue, 13 Feb 2024 04:22:40 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.10-meta-alpine`

```console
$ docker pull influxdb@sha256:ec14a0d2534d329f069204a1f5ce749ccbfb8718f7aae2e12e6bfaf1d0390e3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.10-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:00ebde520e2620cae1b706f26e20492e56882ae047e3681766666a52f1b193a2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25196672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f72aaad2e430657443ac05ab2b72cc2cb22cd44a3794407ac89f1f1ad0a5066b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:40:27 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 27 Jan 2024 05:49:36 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Sat, 27 Jan 2024 05:50:11 GMT
ENV INFLUXDB_VERSION=1.10.5-c1.10.5
# Sat, 27 Jan 2024 05:50:28 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 27 Jan 2024 05:50:28 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Sat, 27 Jan 2024 05:50:28 GMT
EXPOSE 8091
# Sat, 27 Jan 2024 05:50:28 GMT
VOLUME [/var/lib/influxdb]
# Sat, 27 Jan 2024 05:50:29 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Sat, 27 Jan 2024 05:50:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 05:50:29 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c332be88cb2898fd00957a6e5a3581893f9a14b30ec2470466897e8b246e9ad`  
		Last Modified: Sat, 27 Jan 2024 03:41:30 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23860728907803516673e82c6dbade4a15e2a3c8d5eb068dac0624d037ca63e`  
		Last Modified: Sat, 27 Jan 2024 05:51:38 GMT  
		Size: 1.5 MB (1472931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1064b268e519b9acf7da4f68b271a37c7acf45f0da89bf4624c0e4d0d37976c3`  
		Last Modified: Sat, 27 Jan 2024 05:52:34 GMT  
		Size: 20.3 MB (20343465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf42a68d8917612c1241e283f8440a27477570dfda16e0ab0dab37c1efbbb8e1`  
		Last Modified: Sat, 27 Jan 2024 05:52:31 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c07195cec2209dbd50071dc2542111a910f97d12027924eb5083c7d26cf5b73`  
		Last Modified: Sat, 27 Jan 2024 05:52:31 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.10.5-data`

```console
$ docker pull influxdb@sha256:24bc1364c9bc23766216617490f74d75ce73851a6b95d1e15c19a7662813e02d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.10.5-data` - linux; amd64

```console
$ docker pull influxdb@sha256:4083bfb90ce811b71080a025eae3b7fae85e58285078add1d6c9eaaebb5f09ba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.0 MB (111028255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0000062840bf2bd1cb2ad3fe248c873a33699159436df05903b7345987fff4a8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:32 GMT
ADD file:1bf1a123da85382e70ea251091b98fd8b4a1972e4c4e84d392443a4e20b7a135 in / 
# Tue, 13 Feb 2024 00:37:32 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:22:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:19:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 04:20:16 GMT
ENV INFLUXDB_VERSION=1.10.5-c1.10.5
# Tue, 13 Feb 2024 04:20:19 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb*
# Tue, 13 Feb 2024 04:20:20 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Tue, 13 Feb 2024 04:20:20 GMT
EXPOSE 8086
# Tue, 13 Feb 2024 04:20:20 GMT
VOLUME [/var/lib/influxdb]
# Tue, 13 Feb 2024 04:20:20 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Tue, 13 Feb 2024 04:20:20 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 13 Feb 2024 04:20:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 04:20:20 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:09e2bc8a597c33b54cccaf52f2e21798e2e0df79ab6cb33d3b1dfd4b33a57512`  
		Last Modified: Tue, 13 Feb 2024 00:42:21 GMT  
		Size: 55.1 MB (55084838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bbf2983642e080d705d575c1da8d4d8c35507576d88e44979b5c6229573d40`  
		Last Modified: Tue, 13 Feb 2024 01:31:47 GMT  
		Size: 15.8 MB (15763532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670ed7b83ea2bbde7dfba362fa83033db766fdb9e3721f9091229abbf0fafae7`  
		Last Modified: Tue, 13 Feb 2024 04:21:45 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2535204acfeb87be430d22f1f96fb1babe5b524715f0a83abe6a2b6fad86cce4`  
		Last Modified: Tue, 13 Feb 2024 04:22:30 GMT  
		Size: 40.2 MB (40176296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e09e34b464aa67ff02580c0283e401e02fea1b1db62654f01749fef3733527`  
		Last Modified: Tue, 13 Feb 2024 04:22:24 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eebbab0b63679ee777f80b4ec264c8fd5f2ad6652667a947205bc86ddbc20c94`  
		Last Modified: Tue, 13 Feb 2024 04:22:24 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60b6e82e169cb964245a02fbae6d7fad1590c7bd7966485f2a3a29be995bf7f`  
		Last Modified: Tue, 13 Feb 2024 04:22:25 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.10.5-data-alpine`

```console
$ docker pull influxdb@sha256:6dfc17ec066afcbe913da01f3c965d46b8b39a176f1f526abdaf6f02b41fe921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.10.5-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:d2dff4365aa609acd0249549c77a7f851430f77ace6a804357b068f25cf55846
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (44987577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99dc5421c026c1d0749f7ec30a7656b3fc85778669e25c4aebb8f64d39293c36`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:40:27 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 27 Jan 2024 05:49:36 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Sat, 27 Jan 2024 05:50:11 GMT
ENV INFLUXDB_VERSION=1.10.5-c1.10.5
# Sat, 27 Jan 2024 05:50:18 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 27 Jan 2024 05:50:18 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Sat, 27 Jan 2024 05:50:18 GMT
EXPOSE 8086
# Sat, 27 Jan 2024 05:50:18 GMT
VOLUME [/var/lib/influxdb]
# Sat, 27 Jan 2024 05:50:18 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Sat, 27 Jan 2024 05:50:18 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sat, 27 Jan 2024 05:50:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 05:50:18 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c332be88cb2898fd00957a6e5a3581893f9a14b30ec2470466897e8b246e9ad`  
		Last Modified: Sat, 27 Jan 2024 03:41:30 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23860728907803516673e82c6dbade4a15e2a3c8d5eb068dac0624d037ca63e`  
		Last Modified: Sat, 27 Jan 2024 05:51:38 GMT  
		Size: 1.5 MB (1472931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27fbb08d778550bb1c887aa19d84266e50cff8f28e9b4a8e3cf87d20f5f838a`  
		Last Modified: Sat, 27 Jan 2024 05:52:23 GMT  
		Size: 40.1 MB (40133166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8dd7fa45bcf36234301be17c9c691a7fccdaa0bde11e7ac60efc4c8a8e53824`  
		Last Modified: Sat, 27 Jan 2024 05:52:17 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76105e1e49ba6dfca3fc5ab0b35b181d117192eca770566d6ba5332023ec6e30`  
		Last Modified: Sat, 27 Jan 2024 05:52:18 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623a6ed184af2fac0feb8725ff46371ba52342c7be76eab853b484a4b796eec7`  
		Last Modified: Sat, 27 Jan 2024 05:52:17 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.10.5-meta`

```console
$ docker pull influxdb@sha256:fbd58010ff9639e8341aa9ca64953af5baca9cf0e645dc04dfa9fb99f5195b50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.10.5-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:ca13b09a76be02f422bb7b5df23a558712c878dedc290e59fe88445830b3b72e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91227729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae264f81e79af9845d765331c8a257245b0e630fd730e77fce83d1b79b3b5ccf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:32 GMT
ADD file:1bf1a123da85382e70ea251091b98fd8b4a1972e4c4e84d392443a4e20b7a135 in / 
# Tue, 13 Feb 2024 00:37:32 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:22:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:19:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 04:20:16 GMT
ENV INFLUXDB_VERSION=1.10.5-c1.10.5
# Tue, 13 Feb 2024 04:20:28 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb*
# Tue, 13 Feb 2024 04:20:29 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Tue, 13 Feb 2024 04:20:29 GMT
EXPOSE 8091
# Tue, 13 Feb 2024 04:20:29 GMT
VOLUME [/var/lib/influxdb]
# Tue, 13 Feb 2024 04:20:29 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Tue, 13 Feb 2024 04:20:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 04:20:29 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:09e2bc8a597c33b54cccaf52f2e21798e2e0df79ab6cb33d3b1dfd4b33a57512`  
		Last Modified: Tue, 13 Feb 2024 00:42:21 GMT  
		Size: 55.1 MB (55084838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bbf2983642e080d705d575c1da8d4d8c35507576d88e44979b5c6229573d40`  
		Last Modified: Tue, 13 Feb 2024 01:31:47 GMT  
		Size: 15.8 MB (15763532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670ed7b83ea2bbde7dfba362fa83033db766fdb9e3721f9091229abbf0fafae7`  
		Last Modified: Tue, 13 Feb 2024 04:21:45 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e1461f7f8f001d5f8a48927a411c9bc8a9f96646f0666f653f9fd87ef741c8`  
		Last Modified: Tue, 13 Feb 2024 04:22:43 GMT  
		Size: 20.4 MB (20376971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba33e04eb0c792d8fbd6c17afce7bf7d91dcdc60f6eaf52cd0e554de2e4163b8`  
		Last Modified: Tue, 13 Feb 2024 04:22:40 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ad6e7f2292c68a524d73eb4c5649e27f98ceee419c1d1c1bcecdc0d8a24a9d`  
		Last Modified: Tue, 13 Feb 2024 04:22:40 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.10.5-meta-alpine`

```console
$ docker pull influxdb@sha256:ec14a0d2534d329f069204a1f5ce749ccbfb8718f7aae2e12e6bfaf1d0390e3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.10.5-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:00ebde520e2620cae1b706f26e20492e56882ae047e3681766666a52f1b193a2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25196672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f72aaad2e430657443ac05ab2b72cc2cb22cd44a3794407ac89f1f1ad0a5066b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:40:27 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 27 Jan 2024 05:49:36 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Sat, 27 Jan 2024 05:50:11 GMT
ENV INFLUXDB_VERSION=1.10.5-c1.10.5
# Sat, 27 Jan 2024 05:50:28 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 27 Jan 2024 05:50:28 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Sat, 27 Jan 2024 05:50:28 GMT
EXPOSE 8091
# Sat, 27 Jan 2024 05:50:28 GMT
VOLUME [/var/lib/influxdb]
# Sat, 27 Jan 2024 05:50:29 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Sat, 27 Jan 2024 05:50:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 05:50:29 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c332be88cb2898fd00957a6e5a3581893f9a14b30ec2470466897e8b246e9ad`  
		Last Modified: Sat, 27 Jan 2024 03:41:30 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23860728907803516673e82c6dbade4a15e2a3c8d5eb068dac0624d037ca63e`  
		Last Modified: Sat, 27 Jan 2024 05:51:38 GMT  
		Size: 1.5 MB (1472931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1064b268e519b9acf7da4f68b271a37c7acf45f0da89bf4624c0e4d0d37976c3`  
		Last Modified: Sat, 27 Jan 2024 05:52:34 GMT  
		Size: 20.3 MB (20343465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf42a68d8917612c1241e283f8440a27477570dfda16e0ab0dab37c1efbbb8e1`  
		Last Modified: Sat, 27 Jan 2024 05:52:31 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c07195cec2209dbd50071dc2542111a910f97d12027924eb5083c7d26cf5b73`  
		Last Modified: Sat, 27 Jan 2024 05:52:31 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.11-data`

```console
$ docker pull influxdb@sha256:941a05f83c9b591c011206c40d0d875c6ac962cbc0a7df5a548981acd3eb154a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.11-data` - linux; amd64

```console
$ docker pull influxdb@sha256:d32577d83e92b3e8efc3db4308490f068bbea6b5130606b78c5785a52e5da894
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.8 MB (113777286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77c757e99230d2a6f43fa30eb1814db3a4daa889ddae7db3e546d7f50e221274`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:09 GMT
ADD file:333b899a197a48b3333115a3b59efed559494808873943f606a9bc2b6e242c49 in / 
# Tue, 13 Feb 2024 00:37:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:20:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:20:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 04:20:36 GMT
ENV INFLUXDB_VERSION=1.11.3-c1.11.3
# Tue, 13 Feb 2024 04:20:39 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb*
# Tue, 13 Feb 2024 04:20:39 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Tue, 13 Feb 2024 04:20:40 GMT
EXPOSE 8086
# Tue, 13 Feb 2024 04:20:40 GMT
VOLUME [/var/lib/influxdb]
# Tue, 13 Feb 2024 04:20:40 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Tue, 13 Feb 2024 04:20:40 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 13 Feb 2024 04:20:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 04:20:40 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:7bb465c2914923b08ae03b7fc67b92a1ef9b09c4c1eb9d6711b22ee6bbb46a00`  
		Last Modified: Tue, 13 Feb 2024 00:41:39 GMT  
		Size: 49.6 MB (49552605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9b41aaa3c52ab268b47da303015b94ced04a1eb02e58860e58b283404974f4`  
		Last Modified: Tue, 13 Feb 2024 01:30:39 GMT  
		Size: 24.0 MB (24046577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:740a6ce16e8a72776b39a554659a3c36ebedca809a1f5d9a14e0ba87996f3df1`  
		Last Modified: Tue, 13 Feb 2024 04:22:52 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255d107284cfe6dcc82a9d1b8d6cf576f3e09726fdd87e7e08089903be3aabd5`  
		Last Modified: Tue, 13 Feb 2024 04:22:57 GMT  
		Size: 40.2 MB (40174515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:601f560d30520cffad906a4163170d83a888ff909a7db5e7f010306b7c3c2cbf`  
		Last Modified: Tue, 13 Feb 2024 04:22:52 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e649c8ea1edb753b46cc288b4ad1409c26869b26536bed38897a08c83d7054b4`  
		Last Modified: Tue, 13 Feb 2024 04:22:52 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8748fa7230f54a477a99402eeb32cea8e2cf7d6b221baa727e770b8e65ee5a55`  
		Last Modified: Tue, 13 Feb 2024 04:22:52 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.11-data-alpine`

```console
$ docker pull influxdb@sha256:f2296022446abab811be7f6e206d3f7be2b2a5376d04a1d00bc553a92fc59134
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.11-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:4c309f2e7fb98f43a609ea3d6f29272bbd6b1328fc15d2c09c6aa1a64d6bc6a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44943997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0c88b473aac4c6f34c4c0a1894ecfa4ca4561852c1ca4d1b65180f3ea5725c9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:11:20 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 27 Jan 2024 05:50:36 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Sat, 27 Jan 2024 05:50:36 GMT
ENV INFLUXDB_VERSION=1.11.3-c1.11.3
# Sat, 27 Jan 2024 05:50:43 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 27 Jan 2024 05:50:43 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Sat, 27 Jan 2024 05:50:43 GMT
EXPOSE 8086
# Sat, 27 Jan 2024 05:50:43 GMT
VOLUME [/var/lib/influxdb]
# Sat, 27 Jan 2024 05:50:43 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Sat, 27 Jan 2024 05:50:43 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sat, 27 Jan 2024 05:50:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 05:50:43 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27c0340c3b428b118deb541dd857e5413c0ea787e9ba56ae54589ea731c7730`  
		Last Modified: Sat, 27 Jan 2024 03:12:00 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65596c7081a343d23ddc1dc1de386b152b0c01655cb7804137c28389c01afdd0`  
		Last Modified: Sat, 27 Jan 2024 05:52:43 GMT  
		Size: 1.4 MB (1407743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:677d830768d377b164e6e0826afdd2478d4f3e3cd9280ca00e04b63629a007da`  
		Last Modified: Sat, 27 Jan 2024 05:52:49 GMT  
		Size: 40.1 MB (40131629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ddca33a09d3e38124fe2bcc73fe43a0b27298a5850d0e61b993dd8b7fe2879`  
		Last Modified: Sat, 27 Jan 2024 05:52:43 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe7e9e96379b34b30895818564529d9571cefe55726ebe2129513d78925b058`  
		Last Modified: Sat, 27 Jan 2024 05:52:43 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:118348fbf36b7001ad87dbab4cb27165c8b56275484b9e34ab5ba09e3a687dfc`  
		Last Modified: Sat, 27 Jan 2024 05:52:43 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.11-meta`

```console
$ docker pull influxdb@sha256:c69aecc1609848bfa01579ddba8d5d258d3ae3c24c7b6b6b89950d6499bd1907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.11-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:8116819acfecc870fe04bfd283dba61334fb1c01b49ef99142c16990365e4113
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.9 MB (93929028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dd38df12b4bfe85a101b8d417ed27bc7fd7d1482eef276d6934861bd424bdc0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:09 GMT
ADD file:333b899a197a48b3333115a3b59efed559494808873943f606a9bc2b6e242c49 in / 
# Tue, 13 Feb 2024 00:37:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:20:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:20:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 04:20:36 GMT
ENV INFLUXDB_VERSION=1.11.3-c1.11.3
# Tue, 13 Feb 2024 04:20:47 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb*
# Tue, 13 Feb 2024 04:20:47 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Tue, 13 Feb 2024 04:20:47 GMT
EXPOSE 8091
# Tue, 13 Feb 2024 04:20:47 GMT
VOLUME [/var/lib/influxdb]
# Tue, 13 Feb 2024 04:20:47 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Tue, 13 Feb 2024 04:20:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 04:20:48 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:7bb465c2914923b08ae03b7fc67b92a1ef9b09c4c1eb9d6711b22ee6bbb46a00`  
		Last Modified: Tue, 13 Feb 2024 00:41:39 GMT  
		Size: 49.6 MB (49552605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9b41aaa3c52ab268b47da303015b94ced04a1eb02e58860e58b283404974f4`  
		Last Modified: Tue, 13 Feb 2024 01:30:39 GMT  
		Size: 24.0 MB (24046577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:740a6ce16e8a72776b39a554659a3c36ebedca809a1f5d9a14e0ba87996f3df1`  
		Last Modified: Tue, 13 Feb 2024 04:22:52 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d004ee7d6de6c95be403ec7d6443e85b87dd113d0b86e36aa835deeab5b7ca2`  
		Last Modified: Tue, 13 Feb 2024 04:23:10 GMT  
		Size: 20.3 MB (20327463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bfbf9d9d65b8629b673b3e1d40ba58b803df822c1088ed3890765f19dd42186`  
		Last Modified: Tue, 13 Feb 2024 04:23:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50ec7e53b4c4d74234ae07a29c72615b0c99d6d772c21ddaec5e5960cb480acd`  
		Last Modified: Tue, 13 Feb 2024 04:23:07 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.11-meta-alpine`

```console
$ docker pull influxdb@sha256:f3dcd6b646549cd4304751b2f1f1dd3550fce5717a7cc15189351f8aca2972b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.11-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:73951ffbd385d17058059944c6c760b49b2334d50dda3b7d5fb85bfc26265adf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25100688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65bbc82c273de8b79c290657ffc0e9b88af185226e7afc7d571adae3bf759831`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:11:20 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 27 Jan 2024 05:50:36 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Sat, 27 Jan 2024 05:50:36 GMT
ENV INFLUXDB_VERSION=1.11.3-c1.11.3
# Sat, 27 Jan 2024 05:50:54 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 27 Jan 2024 05:50:55 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Sat, 27 Jan 2024 05:50:55 GMT
EXPOSE 8091
# Sat, 27 Jan 2024 05:50:55 GMT
VOLUME [/var/lib/influxdb]
# Sat, 27 Jan 2024 05:50:55 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Sat, 27 Jan 2024 05:50:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 05:50:55 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27c0340c3b428b118deb541dd857e5413c0ea787e9ba56ae54589ea731c7730`  
		Last Modified: Sat, 27 Jan 2024 03:12:00 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65596c7081a343d23ddc1dc1de386b152b0c01655cb7804137c28389c01afdd0`  
		Last Modified: Sat, 27 Jan 2024 05:52:43 GMT  
		Size: 1.4 MB (1407743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbfdca2c90210f747f127d14cf0df6409564ece4c4c973e754bc9f7ac5646c19`  
		Last Modified: Sat, 27 Jan 2024 05:53:01 GMT  
		Size: 20.3 MB (20289524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa279a27fb016f9a9a5eeef1bb16e8e1c3b3fc10f613269fbae81a0323a8ab5`  
		Last Modified: Sat, 27 Jan 2024 05:52:58 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a12e05ae5fef7f8126a5f70746bcbf8ff7b053d0daa407140050e55506c67319`  
		Last Modified: Sat, 27 Jan 2024 05:52:58 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.11.3-data`

```console
$ docker pull influxdb@sha256:941a05f83c9b591c011206c40d0d875c6ac962cbc0a7df5a548981acd3eb154a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.11.3-data` - linux; amd64

```console
$ docker pull influxdb@sha256:d32577d83e92b3e8efc3db4308490f068bbea6b5130606b78c5785a52e5da894
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.8 MB (113777286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77c757e99230d2a6f43fa30eb1814db3a4daa889ddae7db3e546d7f50e221274`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:09 GMT
ADD file:333b899a197a48b3333115a3b59efed559494808873943f606a9bc2b6e242c49 in / 
# Tue, 13 Feb 2024 00:37:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:20:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:20:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 04:20:36 GMT
ENV INFLUXDB_VERSION=1.11.3-c1.11.3
# Tue, 13 Feb 2024 04:20:39 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb*
# Tue, 13 Feb 2024 04:20:39 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Tue, 13 Feb 2024 04:20:40 GMT
EXPOSE 8086
# Tue, 13 Feb 2024 04:20:40 GMT
VOLUME [/var/lib/influxdb]
# Tue, 13 Feb 2024 04:20:40 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Tue, 13 Feb 2024 04:20:40 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 13 Feb 2024 04:20:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 04:20:40 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:7bb465c2914923b08ae03b7fc67b92a1ef9b09c4c1eb9d6711b22ee6bbb46a00`  
		Last Modified: Tue, 13 Feb 2024 00:41:39 GMT  
		Size: 49.6 MB (49552605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9b41aaa3c52ab268b47da303015b94ced04a1eb02e58860e58b283404974f4`  
		Last Modified: Tue, 13 Feb 2024 01:30:39 GMT  
		Size: 24.0 MB (24046577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:740a6ce16e8a72776b39a554659a3c36ebedca809a1f5d9a14e0ba87996f3df1`  
		Last Modified: Tue, 13 Feb 2024 04:22:52 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255d107284cfe6dcc82a9d1b8d6cf576f3e09726fdd87e7e08089903be3aabd5`  
		Last Modified: Tue, 13 Feb 2024 04:22:57 GMT  
		Size: 40.2 MB (40174515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:601f560d30520cffad906a4163170d83a888ff909a7db5e7f010306b7c3c2cbf`  
		Last Modified: Tue, 13 Feb 2024 04:22:52 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e649c8ea1edb753b46cc288b4ad1409c26869b26536bed38897a08c83d7054b4`  
		Last Modified: Tue, 13 Feb 2024 04:22:52 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8748fa7230f54a477a99402eeb32cea8e2cf7d6b221baa727e770b8e65ee5a55`  
		Last Modified: Tue, 13 Feb 2024 04:22:52 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.11.3-data-alpine`

```console
$ docker pull influxdb@sha256:f2296022446abab811be7f6e206d3f7be2b2a5376d04a1d00bc553a92fc59134
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.11.3-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:4c309f2e7fb98f43a609ea3d6f29272bbd6b1328fc15d2c09c6aa1a64d6bc6a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44943997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0c88b473aac4c6f34c4c0a1894ecfa4ca4561852c1ca4d1b65180f3ea5725c9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:11:20 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 27 Jan 2024 05:50:36 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Sat, 27 Jan 2024 05:50:36 GMT
ENV INFLUXDB_VERSION=1.11.3-c1.11.3
# Sat, 27 Jan 2024 05:50:43 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 27 Jan 2024 05:50:43 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Sat, 27 Jan 2024 05:50:43 GMT
EXPOSE 8086
# Sat, 27 Jan 2024 05:50:43 GMT
VOLUME [/var/lib/influxdb]
# Sat, 27 Jan 2024 05:50:43 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Sat, 27 Jan 2024 05:50:43 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sat, 27 Jan 2024 05:50:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 05:50:43 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27c0340c3b428b118deb541dd857e5413c0ea787e9ba56ae54589ea731c7730`  
		Last Modified: Sat, 27 Jan 2024 03:12:00 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65596c7081a343d23ddc1dc1de386b152b0c01655cb7804137c28389c01afdd0`  
		Last Modified: Sat, 27 Jan 2024 05:52:43 GMT  
		Size: 1.4 MB (1407743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:677d830768d377b164e6e0826afdd2478d4f3e3cd9280ca00e04b63629a007da`  
		Last Modified: Sat, 27 Jan 2024 05:52:49 GMT  
		Size: 40.1 MB (40131629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ddca33a09d3e38124fe2bcc73fe43a0b27298a5850d0e61b993dd8b7fe2879`  
		Last Modified: Sat, 27 Jan 2024 05:52:43 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe7e9e96379b34b30895818564529d9571cefe55726ebe2129513d78925b058`  
		Last Modified: Sat, 27 Jan 2024 05:52:43 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:118348fbf36b7001ad87dbab4cb27165c8b56275484b9e34ab5ba09e3a687dfc`  
		Last Modified: Sat, 27 Jan 2024 05:52:43 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.11.3-meta`

```console
$ docker pull influxdb@sha256:c69aecc1609848bfa01579ddba8d5d258d3ae3c24c7b6b6b89950d6499bd1907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.11.3-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:8116819acfecc870fe04bfd283dba61334fb1c01b49ef99142c16990365e4113
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.9 MB (93929028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dd38df12b4bfe85a101b8d417ed27bc7fd7d1482eef276d6934861bd424bdc0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:09 GMT
ADD file:333b899a197a48b3333115a3b59efed559494808873943f606a9bc2b6e242c49 in / 
# Tue, 13 Feb 2024 00:37:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:20:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:20:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 04:20:36 GMT
ENV INFLUXDB_VERSION=1.11.3-c1.11.3
# Tue, 13 Feb 2024 04:20:47 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb*
# Tue, 13 Feb 2024 04:20:47 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Tue, 13 Feb 2024 04:20:47 GMT
EXPOSE 8091
# Tue, 13 Feb 2024 04:20:47 GMT
VOLUME [/var/lib/influxdb]
# Tue, 13 Feb 2024 04:20:47 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Tue, 13 Feb 2024 04:20:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 04:20:48 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:7bb465c2914923b08ae03b7fc67b92a1ef9b09c4c1eb9d6711b22ee6bbb46a00`  
		Last Modified: Tue, 13 Feb 2024 00:41:39 GMT  
		Size: 49.6 MB (49552605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9b41aaa3c52ab268b47da303015b94ced04a1eb02e58860e58b283404974f4`  
		Last Modified: Tue, 13 Feb 2024 01:30:39 GMT  
		Size: 24.0 MB (24046577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:740a6ce16e8a72776b39a554659a3c36ebedca809a1f5d9a14e0ba87996f3df1`  
		Last Modified: Tue, 13 Feb 2024 04:22:52 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d004ee7d6de6c95be403ec7d6443e85b87dd113d0b86e36aa835deeab5b7ca2`  
		Last Modified: Tue, 13 Feb 2024 04:23:10 GMT  
		Size: 20.3 MB (20327463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bfbf9d9d65b8629b673b3e1d40ba58b803df822c1088ed3890765f19dd42186`  
		Last Modified: Tue, 13 Feb 2024 04:23:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50ec7e53b4c4d74234ae07a29c72615b0c99d6d772c21ddaec5e5960cb480acd`  
		Last Modified: Tue, 13 Feb 2024 04:23:07 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.11.3-meta-alpine`

```console
$ docker pull influxdb@sha256:f3dcd6b646549cd4304751b2f1f1dd3550fce5717a7cc15189351f8aca2972b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.11.3-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:73951ffbd385d17058059944c6c760b49b2334d50dda3b7d5fb85bfc26265adf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25100688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65bbc82c273de8b79c290657ffc0e9b88af185226e7afc7d571adae3bf759831`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:11:20 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 27 Jan 2024 05:50:36 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Sat, 27 Jan 2024 05:50:36 GMT
ENV INFLUXDB_VERSION=1.11.3-c1.11.3
# Sat, 27 Jan 2024 05:50:54 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 27 Jan 2024 05:50:55 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Sat, 27 Jan 2024 05:50:55 GMT
EXPOSE 8091
# Sat, 27 Jan 2024 05:50:55 GMT
VOLUME [/var/lib/influxdb]
# Sat, 27 Jan 2024 05:50:55 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Sat, 27 Jan 2024 05:50:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 05:50:55 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27c0340c3b428b118deb541dd857e5413c0ea787e9ba56ae54589ea731c7730`  
		Last Modified: Sat, 27 Jan 2024 03:12:00 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65596c7081a343d23ddc1dc1de386b152b0c01655cb7804137c28389c01afdd0`  
		Last Modified: Sat, 27 Jan 2024 05:52:43 GMT  
		Size: 1.4 MB (1407743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbfdca2c90210f747f127d14cf0df6409564ece4c4c973e754bc9f7ac5646c19`  
		Last Modified: Sat, 27 Jan 2024 05:53:01 GMT  
		Size: 20.3 MB (20289524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa279a27fb016f9a9a5eeef1bb16e8e1c3b3fc10f613269fbae81a0323a8ab5`  
		Last Modified: Sat, 27 Jan 2024 05:52:58 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a12e05ae5fef7f8126a5f70746bcbf8ff7b053d0daa407140050e55506c67319`  
		Last Modified: Sat, 27 Jan 2024 05:52:58 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8`

```console
$ docker pull influxdb@sha256:6264b88c8e8958125977d7b2d7967d725f808c865c06aa71bfc78d11b4149423
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.8` - linux; amd64

```console
$ docker pull influxdb@sha256:d3bb8adc34a9623e429c74408dca916b386c0fe5e57b3f2752c7f6a4e483d0f2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125737693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52538bd7e50e45e974ddb473966d9b388e6fe7cdd5c8c0b347a33f9e6dd6431f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:32 GMT
ADD file:1bf1a123da85382e70ea251091b98fd8b4a1972e4c4e84d392443a4e20b7a135 in / 
# Tue, 13 Feb 2024 00:37:32 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:22:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:19:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 04:19:48 GMT
ENV INFLUXDB_VERSION=1.8.10
# Tue, 13 Feb 2024 04:19:52 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Tue, 13 Feb 2024 04:19:52 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Tue, 13 Feb 2024 04:19:52 GMT
EXPOSE 8086
# Tue, 13 Feb 2024 04:19:52 GMT
VOLUME [/var/lib/influxdb]
# Tue, 13 Feb 2024 04:19:52 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Tue, 13 Feb 2024 04:19:52 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 13 Feb 2024 04:19:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 04:19:53 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:09e2bc8a597c33b54cccaf52f2e21798e2e0df79ab6cb33d3b1dfd4b33a57512`  
		Last Modified: Tue, 13 Feb 2024 00:42:21 GMT  
		Size: 55.1 MB (55084838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bbf2983642e080d705d575c1da8d4d8c35507576d88e44979b5c6229573d40`  
		Last Modified: Tue, 13 Feb 2024 01:31:47 GMT  
		Size: 15.8 MB (15763532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670ed7b83ea2bbde7dfba362fa83033db766fdb9e3721f9091229abbf0fafae7`  
		Last Modified: Tue, 13 Feb 2024 04:21:45 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f3de5c50aef4bc1e27b5bd824c495a00359cec3882488c2f564c922f44149d`  
		Last Modified: Tue, 13 Feb 2024 04:21:52 GMT  
		Size: 54.9 MB (54885785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4907e357621273b6178f12b1468879002f1954900f9a045afdd3dfabd853c2f4`  
		Last Modified: Tue, 13 Feb 2024 04:21:45 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da544e0a304fb9cc25d55b2851ee22d6c8dfe888f9d9129d4ccb5db4cb2a703`  
		Last Modified: Tue, 13 Feb 2024 04:21:45 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d19300c6b09941dacd3ad7c8ddfaa283e3fc8c1af68b1f922a42725496d3074`  
		Last Modified: Tue, 13 Feb 2024 04:21:45 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.8` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:83f4a2b04a490e2cdf4f10b4180889efc6ce32bf1fca3b0787841318cb063780
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.7 MB (116713519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e1201410ab3e8512704ee711905fa3870851b78534c45cdc8581b45d0d19ad`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:31 GMT
ADD file:7a3ca444fa582cdedade49cd6262ee982b6da86eafe22b1b77326c8eab3f88cf in / 
# Wed, 31 Jan 2024 22:44:31 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 02:49:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 06:35:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 01 Feb 2024 06:35:54 GMT
ENV INFLUXDB_VERSION=1.8.10
# Thu, 01 Feb 2024 06:36:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Thu, 01 Feb 2024 06:36:02 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Thu, 01 Feb 2024 06:36:02 GMT
EXPOSE 8086
# Thu, 01 Feb 2024 06:36:02 GMT
VOLUME [/var/lib/influxdb]
# Thu, 01 Feb 2024 06:36:03 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Thu, 01 Feb 2024 06:36:03 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 01 Feb 2024 06:36:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 01 Feb 2024 06:36:03 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:413453d204f637339c7a4727b614537000709bb2ff00a6307e262cf37237761c`  
		Last Modified: Wed, 31 Jan 2024 22:49:12 GMT  
		Size: 50.2 MB (50216178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1bf41a938a7614b6b4a47164d8e064bbe0014418bfb366d6fac331d52eb271`  
		Last Modified: Thu, 01 Feb 2024 02:59:37 GMT  
		Size: 14.9 MB (14880646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16253df4204184e378f8846f2ef099855f012ffbe37757551a452a9449c815bb`  
		Last Modified: Thu, 01 Feb 2024 06:36:09 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ea8d85cd7c8fd17ddb69b9e323eea2725cb53be1fbd9f366cc157802ebb3b9`  
		Last Modified: Thu, 01 Feb 2024 06:36:16 GMT  
		Size: 51.6 MB (51613159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1710ccd30a6ad21ff3475b5d0370525d368453aa507c481c60c50cf5c590c0d`  
		Last Modified: Thu, 01 Feb 2024 06:36:09 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a6e074b451c5641330cc2b9fc3b78ceddcd967557bdab758f7d115298acab7`  
		Last Modified: Thu, 01 Feb 2024 06:36:09 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c101f58a67da24d9173b39386ec7152e9ffd535f8769ff94746b88ce51aa857c`  
		Last Modified: Thu, 01 Feb 2024 06:36:09 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:3033a2aea3ab67e334f21ad73e91ce3e2c824e6ab95d6900f8a004383cb768f3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120704245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aec81e9869ad5a6a50df038f0753a0d7ad41e370882de90e453adba6489f2a1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:27 GMT
ADD file:46791e28a2eef97a17393ff5cf2928d2e721f9380340a34c7d2e85053edec7c1 in / 
# Tue, 13 Feb 2024 00:41:27 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:38:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 10:19:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 10:19:13 GMT
ENV INFLUXDB_VERSION=1.8.10
# Tue, 13 Feb 2024 10:19:16 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Tue, 13 Feb 2024 10:19:17 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Tue, 13 Feb 2024 10:19:17 GMT
EXPOSE 8086
# Tue, 13 Feb 2024 10:19:17 GMT
VOLUME [/var/lib/influxdb]
# Tue, 13 Feb 2024 10:19:17 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Tue, 13 Feb 2024 10:19:17 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 13 Feb 2024 10:19:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 10:19:17 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:4245faf914201feff648b048cbaf6c46414d24a56e29e4cff1f82ac1b151d326`  
		Last Modified: Tue, 13 Feb 2024 00:45:14 GMT  
		Size: 53.7 MB (53721486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d359f54bdf6c7734649777e288d4d317d49bd63e944dd5f852641a97b61527`  
		Last Modified: Tue, 13 Feb 2024 01:47:39 GMT  
		Size: 15.7 MB (15749141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77eb97d4ede724e4c398b272213051fe4780a2831dff072e3d681f19d648c8cd`  
		Last Modified: Tue, 13 Feb 2024 10:19:57 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a264f6675666185787424751ff5e4e09eefe0e6bccf0d4a913b646070241fbc`  
		Last Modified: Tue, 13 Feb 2024 10:20:02 GMT  
		Size: 51.2 MB (51230086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7fc328c2a834e9a461fca1972c31d0a023ab1c4412f5482242071d7028797b9`  
		Last Modified: Tue, 13 Feb 2024 10:19:57 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab53a30529e71f69f420aeec2ba1ab0f799c8d5ac6490fc26a8010f8527d72a`  
		Last Modified: Tue, 13 Feb 2024 10:19:57 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c6ca1a98fc074c74106ca2a20af38dde5308b7f8b0dba772ca7d71fa6035f0c`  
		Last Modified: Tue, 13 Feb 2024 10:19:57 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8-alpine`

```console
$ docker pull influxdb@sha256:a5f432ffd299697f7dc2e062dedeffb0669ed5c238e589ff90661c968803ec3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.8-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:dc1fc33268a7011fd4154b69f70185d65f10d739a5a9323857481f9941f2d4c8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59501088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd653fb19949f7fa0abeb5fd321450a58e441052109e3c9ecff14cc1150589c9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:40:27 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 27 Jan 2024 05:49:36 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Sat, 27 Jan 2024 05:49:36 GMT
ENV INFLUXDB_VERSION=1.8.10
# Sat, 27 Jan 2024 05:49:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     chmod +x /usr/src/influxdb-*/influx              /usr/src/influxdb-*/influx_inspect              /usr/src/influxdb-*/influx_stress              /usr/src/influxdb-*/influxd &&    mv /usr/src/influxdb-*/influx        /usr/src/influxdb-*/influx_inspect        /usr/src/influxdb-*/influx_stress         /usr/src/influxdb-*/influxd        /usr/bin/ &&    gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 27 Jan 2024 05:49:42 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Sat, 27 Jan 2024 05:49:42 GMT
EXPOSE 8086
# Sat, 27 Jan 2024 05:49:43 GMT
VOLUME [/var/lib/influxdb]
# Sat, 27 Jan 2024 05:49:43 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Sat, 27 Jan 2024 05:49:43 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sat, 27 Jan 2024 05:49:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 05:49:43 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c332be88cb2898fd00957a6e5a3581893f9a14b30ec2470466897e8b246e9ad`  
		Last Modified: Sat, 27 Jan 2024 03:41:30 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23860728907803516673e82c6dbade4a15e2a3c8d5eb068dac0624d037ca63e`  
		Last Modified: Sat, 27 Jan 2024 05:51:38 GMT  
		Size: 1.5 MB (1472931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2461a5b8da03141f6dde5783b86436ca6b6cdc0508c0b0d8371b6131174af4a6`  
		Last Modified: Sat, 27 Jan 2024 05:51:44 GMT  
		Size: 54.6 MB (54646736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:167d4e680f500d91450a4e287dd975a9a4b91c87ad6e5026ee19a1e8bde79520`  
		Last Modified: Sat, 27 Jan 2024 05:51:37 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e151e1055c996dbd10517d4a1f205af235ff1ec257642474fce90da643028f`  
		Last Modified: Sat, 27 Jan 2024 05:51:38 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce019f6857cd6e0525552edbbc1e3c7370e2974109a1956fbcce1407758989ce`  
		Last Modified: Sat, 27 Jan 2024 05:51:38 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.10`

```console
$ docker pull influxdb@sha256:6264b88c8e8958125977d7b2d7967d725f808c865c06aa71bfc78d11b4149423
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.8.10` - linux; amd64

```console
$ docker pull influxdb@sha256:d3bb8adc34a9623e429c74408dca916b386c0fe5e57b3f2752c7f6a4e483d0f2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125737693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52538bd7e50e45e974ddb473966d9b388e6fe7cdd5c8c0b347a33f9e6dd6431f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:32 GMT
ADD file:1bf1a123da85382e70ea251091b98fd8b4a1972e4c4e84d392443a4e20b7a135 in / 
# Tue, 13 Feb 2024 00:37:32 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:22:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:19:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 04:19:48 GMT
ENV INFLUXDB_VERSION=1.8.10
# Tue, 13 Feb 2024 04:19:52 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Tue, 13 Feb 2024 04:19:52 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Tue, 13 Feb 2024 04:19:52 GMT
EXPOSE 8086
# Tue, 13 Feb 2024 04:19:52 GMT
VOLUME [/var/lib/influxdb]
# Tue, 13 Feb 2024 04:19:52 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Tue, 13 Feb 2024 04:19:52 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 13 Feb 2024 04:19:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 04:19:53 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:09e2bc8a597c33b54cccaf52f2e21798e2e0df79ab6cb33d3b1dfd4b33a57512`  
		Last Modified: Tue, 13 Feb 2024 00:42:21 GMT  
		Size: 55.1 MB (55084838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bbf2983642e080d705d575c1da8d4d8c35507576d88e44979b5c6229573d40`  
		Last Modified: Tue, 13 Feb 2024 01:31:47 GMT  
		Size: 15.8 MB (15763532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670ed7b83ea2bbde7dfba362fa83033db766fdb9e3721f9091229abbf0fafae7`  
		Last Modified: Tue, 13 Feb 2024 04:21:45 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f3de5c50aef4bc1e27b5bd824c495a00359cec3882488c2f564c922f44149d`  
		Last Modified: Tue, 13 Feb 2024 04:21:52 GMT  
		Size: 54.9 MB (54885785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4907e357621273b6178f12b1468879002f1954900f9a045afdd3dfabd853c2f4`  
		Last Modified: Tue, 13 Feb 2024 04:21:45 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da544e0a304fb9cc25d55b2851ee22d6c8dfe888f9d9129d4ccb5db4cb2a703`  
		Last Modified: Tue, 13 Feb 2024 04:21:45 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d19300c6b09941dacd3ad7c8ddfaa283e3fc8c1af68b1f922a42725496d3074`  
		Last Modified: Tue, 13 Feb 2024 04:21:45 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.8.10` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:83f4a2b04a490e2cdf4f10b4180889efc6ce32bf1fca3b0787841318cb063780
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.7 MB (116713519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e1201410ab3e8512704ee711905fa3870851b78534c45cdc8581b45d0d19ad`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:31 GMT
ADD file:7a3ca444fa582cdedade49cd6262ee982b6da86eafe22b1b77326c8eab3f88cf in / 
# Wed, 31 Jan 2024 22:44:31 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 02:49:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 06:35:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 01 Feb 2024 06:35:54 GMT
ENV INFLUXDB_VERSION=1.8.10
# Thu, 01 Feb 2024 06:36:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Thu, 01 Feb 2024 06:36:02 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Thu, 01 Feb 2024 06:36:02 GMT
EXPOSE 8086
# Thu, 01 Feb 2024 06:36:02 GMT
VOLUME [/var/lib/influxdb]
# Thu, 01 Feb 2024 06:36:03 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Thu, 01 Feb 2024 06:36:03 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 01 Feb 2024 06:36:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 01 Feb 2024 06:36:03 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:413453d204f637339c7a4727b614537000709bb2ff00a6307e262cf37237761c`  
		Last Modified: Wed, 31 Jan 2024 22:49:12 GMT  
		Size: 50.2 MB (50216178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1bf41a938a7614b6b4a47164d8e064bbe0014418bfb366d6fac331d52eb271`  
		Last Modified: Thu, 01 Feb 2024 02:59:37 GMT  
		Size: 14.9 MB (14880646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16253df4204184e378f8846f2ef099855f012ffbe37757551a452a9449c815bb`  
		Last Modified: Thu, 01 Feb 2024 06:36:09 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ea8d85cd7c8fd17ddb69b9e323eea2725cb53be1fbd9f366cc157802ebb3b9`  
		Last Modified: Thu, 01 Feb 2024 06:36:16 GMT  
		Size: 51.6 MB (51613159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1710ccd30a6ad21ff3475b5d0370525d368453aa507c481c60c50cf5c590c0d`  
		Last Modified: Thu, 01 Feb 2024 06:36:09 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a6e074b451c5641330cc2b9fc3b78ceddcd967557bdab758f7d115298acab7`  
		Last Modified: Thu, 01 Feb 2024 06:36:09 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c101f58a67da24d9173b39386ec7152e9ffd535f8769ff94746b88ce51aa857c`  
		Last Modified: Thu, 01 Feb 2024 06:36:09 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.8.10` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:3033a2aea3ab67e334f21ad73e91ce3e2c824e6ab95d6900f8a004383cb768f3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120704245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aec81e9869ad5a6a50df038f0753a0d7ad41e370882de90e453adba6489f2a1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:27 GMT
ADD file:46791e28a2eef97a17393ff5cf2928d2e721f9380340a34c7d2e85053edec7c1 in / 
# Tue, 13 Feb 2024 00:41:27 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:38:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 10:19:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 10:19:13 GMT
ENV INFLUXDB_VERSION=1.8.10
# Tue, 13 Feb 2024 10:19:16 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Tue, 13 Feb 2024 10:19:17 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Tue, 13 Feb 2024 10:19:17 GMT
EXPOSE 8086
# Tue, 13 Feb 2024 10:19:17 GMT
VOLUME [/var/lib/influxdb]
# Tue, 13 Feb 2024 10:19:17 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Tue, 13 Feb 2024 10:19:17 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 13 Feb 2024 10:19:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 10:19:17 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:4245faf914201feff648b048cbaf6c46414d24a56e29e4cff1f82ac1b151d326`  
		Last Modified: Tue, 13 Feb 2024 00:45:14 GMT  
		Size: 53.7 MB (53721486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d359f54bdf6c7734649777e288d4d317d49bd63e944dd5f852641a97b61527`  
		Last Modified: Tue, 13 Feb 2024 01:47:39 GMT  
		Size: 15.7 MB (15749141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77eb97d4ede724e4c398b272213051fe4780a2831dff072e3d681f19d648c8cd`  
		Last Modified: Tue, 13 Feb 2024 10:19:57 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a264f6675666185787424751ff5e4e09eefe0e6bccf0d4a913b646070241fbc`  
		Last Modified: Tue, 13 Feb 2024 10:20:02 GMT  
		Size: 51.2 MB (51230086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7fc328c2a834e9a461fca1972c31d0a023ab1c4412f5482242071d7028797b9`  
		Last Modified: Tue, 13 Feb 2024 10:19:57 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab53a30529e71f69f420aeec2ba1ab0f799c8d5ac6490fc26a8010f8527d72a`  
		Last Modified: Tue, 13 Feb 2024 10:19:57 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c6ca1a98fc074c74106ca2a20af38dde5308b7f8b0dba772ca7d71fa6035f0c`  
		Last Modified: Tue, 13 Feb 2024 10:19:57 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.10-alpine`

```console
$ docker pull influxdb@sha256:a5f432ffd299697f7dc2e062dedeffb0669ed5c238e589ff90661c968803ec3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.8.10-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:dc1fc33268a7011fd4154b69f70185d65f10d739a5a9323857481f9941f2d4c8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59501088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd653fb19949f7fa0abeb5fd321450a58e441052109e3c9ecff14cc1150589c9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:40:27 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 27 Jan 2024 05:49:36 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Sat, 27 Jan 2024 05:49:36 GMT
ENV INFLUXDB_VERSION=1.8.10
# Sat, 27 Jan 2024 05:49:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     chmod +x /usr/src/influxdb-*/influx              /usr/src/influxdb-*/influx_inspect              /usr/src/influxdb-*/influx_stress              /usr/src/influxdb-*/influxd &&    mv /usr/src/influxdb-*/influx        /usr/src/influxdb-*/influx_inspect        /usr/src/influxdb-*/influx_stress         /usr/src/influxdb-*/influxd        /usr/bin/ &&    gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 27 Jan 2024 05:49:42 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Sat, 27 Jan 2024 05:49:42 GMT
EXPOSE 8086
# Sat, 27 Jan 2024 05:49:43 GMT
VOLUME [/var/lib/influxdb]
# Sat, 27 Jan 2024 05:49:43 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Sat, 27 Jan 2024 05:49:43 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sat, 27 Jan 2024 05:49:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 05:49:43 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c332be88cb2898fd00957a6e5a3581893f9a14b30ec2470466897e8b246e9ad`  
		Last Modified: Sat, 27 Jan 2024 03:41:30 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23860728907803516673e82c6dbade4a15e2a3c8d5eb068dac0624d037ca63e`  
		Last Modified: Sat, 27 Jan 2024 05:51:38 GMT  
		Size: 1.5 MB (1472931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2461a5b8da03141f6dde5783b86436ca6b6cdc0508c0b0d8371b6131174af4a6`  
		Last Modified: Sat, 27 Jan 2024 05:51:44 GMT  
		Size: 54.6 MB (54646736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:167d4e680f500d91450a4e287dd975a9a4b91c87ad6e5026ee19a1e8bde79520`  
		Last Modified: Sat, 27 Jan 2024 05:51:37 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e151e1055c996dbd10517d4a1f205af235ff1ec257642474fce90da643028f`  
		Last Modified: Sat, 27 Jan 2024 05:51:38 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce019f6857cd6e0525552edbbc1e3c7370e2974109a1956fbcce1407758989ce`  
		Last Modified: Sat, 27 Jan 2024 05:51:38 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.9-data`

```console
$ docker pull influxdb@sha256:c357ef2e7f4be16095d079214908cdbde6176ae8ab207bfeb847ff7f614e0702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.9-data` - linux; amd64

```console
$ docker pull influxdb@sha256:cc681b8d2cb7b0ef576c91daee9b4b2229712c84af5b2cb87fc587fac71d4891
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104141093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20b9e2d5640d872d96bbbc41e9dfc52f2e2af07ba2264ec0a1e10b06ae2b6211`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:32 GMT
ADD file:1bf1a123da85382e70ea251091b98fd8b4a1972e4c4e84d392443a4e20b7a135 in / 
# Tue, 13 Feb 2024 00:37:32 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:22:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:19:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 04:19:58 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Tue, 13 Feb 2024 04:20:02 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Tue, 13 Feb 2024 04:20:02 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Tue, 13 Feb 2024 04:20:02 GMT
EXPOSE 8086
# Tue, 13 Feb 2024 04:20:02 GMT
VOLUME [/var/lib/influxdb]
# Tue, 13 Feb 2024 04:20:02 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Tue, 13 Feb 2024 04:20:02 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 13 Feb 2024 04:20:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 04:20:02 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:09e2bc8a597c33b54cccaf52f2e21798e2e0df79ab6cb33d3b1dfd4b33a57512`  
		Last Modified: Tue, 13 Feb 2024 00:42:21 GMT  
		Size: 55.1 MB (55084838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bbf2983642e080d705d575c1da8d4d8c35507576d88e44979b5c6229573d40`  
		Last Modified: Tue, 13 Feb 2024 01:31:47 GMT  
		Size: 15.8 MB (15763532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670ed7b83ea2bbde7dfba362fa83033db766fdb9e3721f9091229abbf0fafae7`  
		Last Modified: Tue, 13 Feb 2024 04:21:45 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89dde1f20c5ceee235c652a40abd00ec804632d8bf0ea974f94d8523f650e583`  
		Last Modified: Tue, 13 Feb 2024 04:22:05 GMT  
		Size: 33.3 MB (33289130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bbbf570ce88698826cf151220437f0aaf15269fb3ba578b1dec142251115b89`  
		Last Modified: Tue, 13 Feb 2024 04:22:00 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d9bc1ed6eabfc0af5896b58bf5260a48ae6e880665b16105f5b772e0e6c539`  
		Last Modified: Tue, 13 Feb 2024 04:22:00 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03916ddfb747b035a292548044c817cdd27bbfedde35b029791002916cc5f3d2`  
		Last Modified: Tue, 13 Feb 2024 04:22:00 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.9-data-alpine`

```console
$ docker pull influxdb@sha256:b0e5d1b1a4ac70b20aca0ddea8e3ba8e0bb89fec46584bc1a30a9298d0e0dfab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.9-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:3beba3be6849c59cf3bcf8aa57b3a8a8869864ccd99a40e4c9e88baa5ce20ebc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 MB (38103160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bcc73a5398b5ff53b8ada6052aacc5c5f99c71886a98ae710b1f1a2d9683a72`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:40:27 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 27 Jan 2024 05:49:36 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Sat, 27 Jan 2024 05:49:48 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Sat, 27 Jan 2024 05:49:54 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/etc/influxdb/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 27 Jan 2024 05:49:55 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Sat, 27 Jan 2024 05:49:55 GMT
EXPOSE 8086
# Sat, 27 Jan 2024 05:49:55 GMT
VOLUME [/var/lib/influxdb]
# Sat, 27 Jan 2024 05:49:55 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Sat, 27 Jan 2024 05:49:55 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sat, 27 Jan 2024 05:49:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 05:49:55 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c332be88cb2898fd00957a6e5a3581893f9a14b30ec2470466897e8b246e9ad`  
		Last Modified: Sat, 27 Jan 2024 03:41:30 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23860728907803516673e82c6dbade4a15e2a3c8d5eb068dac0624d037ca63e`  
		Last Modified: Sat, 27 Jan 2024 05:51:38 GMT  
		Size: 1.5 MB (1472931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41dbab3a92f1d001e07dc6fb54de222a24e6c8dd327cbd3b9ff76492bb0a88bf`  
		Last Modified: Sat, 27 Jan 2024 05:51:58 GMT  
		Size: 33.2 MB (33248751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4c07bc517a54210e91f049d33d098f90aef5b0fb83397215bb2b5d45afd61da`  
		Last Modified: Sat, 27 Jan 2024 05:51:53 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a21e5dd20637b1b02d4cb447246a448d38e70c9821ff746b02fb530a999cb3`  
		Last Modified: Sat, 27 Jan 2024 05:51:53 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea9809d1b5b5adddd1ca21e5ae36f5ff06bdf4147cb14409b84536b436d8992f`  
		Last Modified: Sat, 27 Jan 2024 05:51:53 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.9-meta`

```console
$ docker pull influxdb@sha256:0f20c3223e62c375dfc47f82fd8a30db63244006576599d5ba6eda3f16df84c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.9-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:4137a252bf2565dd407d4a41128e314bbf1a4025a5501821a401d9d7d1a55f7e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83620571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5f8432c2b19411539b28e70b8a9cfa4f331d7886f7ff95aa6feceb298c23e0e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:32 GMT
ADD file:1bf1a123da85382e70ea251091b98fd8b4a1972e4c4e84d392443a4e20b7a135 in / 
# Tue, 13 Feb 2024 00:37:32 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:22:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:19:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 04:19:58 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Tue, 13 Feb 2024 04:20:10 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Tue, 13 Feb 2024 04:20:10 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Tue, 13 Feb 2024 04:20:10 GMT
EXPOSE 8091
# Tue, 13 Feb 2024 04:20:10 GMT
VOLUME [/var/lib/influxdb]
# Tue, 13 Feb 2024 04:20:10 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Tue, 13 Feb 2024 04:20:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 04:20:11 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:09e2bc8a597c33b54cccaf52f2e21798e2e0df79ab6cb33d3b1dfd4b33a57512`  
		Last Modified: Tue, 13 Feb 2024 00:42:21 GMT  
		Size: 55.1 MB (55084838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bbf2983642e080d705d575c1da8d4d8c35507576d88e44979b5c6229573d40`  
		Last Modified: Tue, 13 Feb 2024 01:31:47 GMT  
		Size: 15.8 MB (15763532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670ed7b83ea2bbde7dfba362fa83033db766fdb9e3721f9091229abbf0fafae7`  
		Last Modified: Tue, 13 Feb 2024 04:21:45 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc275cd09b4b0bf4b318b112c486e1b4348cd9103c5a46bc1bd885b52eff48cf`  
		Last Modified: Tue, 13 Feb 2024 04:22:16 GMT  
		Size: 12.8 MB (12769813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef68a6316f6f0f41e45091eb1313b1c2e68fbfc137ae1954d33c2c42036ca517`  
		Last Modified: Tue, 13 Feb 2024 04:22:14 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c36e200ae078b583ed845e0c64738a3816b17634bdd3efe9ee080a203c4d629`  
		Last Modified: Tue, 13 Feb 2024 04:22:15 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.9-meta-alpine`

```console
$ docker pull influxdb@sha256:b2417481cffba22ca7fc6eb5576be1b0b850483e860de71357b119be44177aa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.9-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:b73457a8ec3874796e55fae146c926eb54357e4169defc0966234e69979667bc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17587482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8321ec8111eda9eb9dd587fa1839d9941cb17ee3b4542fcbdc9656190394c334`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:40:27 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 27 Jan 2024 05:49:36 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Sat, 27 Jan 2024 05:49:48 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Sat, 27 Jan 2024 05:50:05 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/etc/influxdb/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 27 Jan 2024 05:50:05 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Sat, 27 Jan 2024 05:50:05 GMT
EXPOSE 8091
# Sat, 27 Jan 2024 05:50:05 GMT
VOLUME [/var/lib/influxdb]
# Sat, 27 Jan 2024 05:50:06 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Sat, 27 Jan 2024 05:50:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 05:50:06 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c332be88cb2898fd00957a6e5a3581893f9a14b30ec2470466897e8b246e9ad`  
		Last Modified: Sat, 27 Jan 2024 03:41:30 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23860728907803516673e82c6dbade4a15e2a3c8d5eb068dac0624d037ca63e`  
		Last Modified: Sat, 27 Jan 2024 05:51:38 GMT  
		Size: 1.5 MB (1472931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0f2675ebfd866fde3bc68c44e6dcfe11a79ab9ae5260d99baea66ee712873d`  
		Last Modified: Sat, 27 Jan 2024 05:52:09 GMT  
		Size: 12.7 MB (12734282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:618acef7e3f9802e623874f09cbf344bff7510bb12ecd8982dfdeff4964ab302`  
		Last Modified: Sat, 27 Jan 2024 05:52:06 GMT  
		Size: 216.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b3ca47192ec8dc8cd93761ceb85513ec25c39a4be443f9c4a7694572fe0bac`  
		Last Modified: Sat, 27 Jan 2024 05:52:07 GMT  
		Size: 372.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.9.13-data`

```console
$ docker pull influxdb@sha256:c357ef2e7f4be16095d079214908cdbde6176ae8ab207bfeb847ff7f614e0702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.9.13-data` - linux; amd64

```console
$ docker pull influxdb@sha256:cc681b8d2cb7b0ef576c91daee9b4b2229712c84af5b2cb87fc587fac71d4891
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104141093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20b9e2d5640d872d96bbbc41e9dfc52f2e2af07ba2264ec0a1e10b06ae2b6211`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:32 GMT
ADD file:1bf1a123da85382e70ea251091b98fd8b4a1972e4c4e84d392443a4e20b7a135 in / 
# Tue, 13 Feb 2024 00:37:32 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:22:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:19:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 04:19:58 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Tue, 13 Feb 2024 04:20:02 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Tue, 13 Feb 2024 04:20:02 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Tue, 13 Feb 2024 04:20:02 GMT
EXPOSE 8086
# Tue, 13 Feb 2024 04:20:02 GMT
VOLUME [/var/lib/influxdb]
# Tue, 13 Feb 2024 04:20:02 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Tue, 13 Feb 2024 04:20:02 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 13 Feb 2024 04:20:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 04:20:02 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:09e2bc8a597c33b54cccaf52f2e21798e2e0df79ab6cb33d3b1dfd4b33a57512`  
		Last Modified: Tue, 13 Feb 2024 00:42:21 GMT  
		Size: 55.1 MB (55084838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bbf2983642e080d705d575c1da8d4d8c35507576d88e44979b5c6229573d40`  
		Last Modified: Tue, 13 Feb 2024 01:31:47 GMT  
		Size: 15.8 MB (15763532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670ed7b83ea2bbde7dfba362fa83033db766fdb9e3721f9091229abbf0fafae7`  
		Last Modified: Tue, 13 Feb 2024 04:21:45 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89dde1f20c5ceee235c652a40abd00ec804632d8bf0ea974f94d8523f650e583`  
		Last Modified: Tue, 13 Feb 2024 04:22:05 GMT  
		Size: 33.3 MB (33289130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bbbf570ce88698826cf151220437f0aaf15269fb3ba578b1dec142251115b89`  
		Last Modified: Tue, 13 Feb 2024 04:22:00 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d9bc1ed6eabfc0af5896b58bf5260a48ae6e880665b16105f5b772e0e6c539`  
		Last Modified: Tue, 13 Feb 2024 04:22:00 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03916ddfb747b035a292548044c817cdd27bbfedde35b029791002916cc5f3d2`  
		Last Modified: Tue, 13 Feb 2024 04:22:00 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.9.13-data-alpine`

```console
$ docker pull influxdb@sha256:b0e5d1b1a4ac70b20aca0ddea8e3ba8e0bb89fec46584bc1a30a9298d0e0dfab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.9.13-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:3beba3be6849c59cf3bcf8aa57b3a8a8869864ccd99a40e4c9e88baa5ce20ebc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 MB (38103160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bcc73a5398b5ff53b8ada6052aacc5c5f99c71886a98ae710b1f1a2d9683a72`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:40:27 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 27 Jan 2024 05:49:36 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Sat, 27 Jan 2024 05:49:48 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Sat, 27 Jan 2024 05:49:54 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/etc/influxdb/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 27 Jan 2024 05:49:55 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Sat, 27 Jan 2024 05:49:55 GMT
EXPOSE 8086
# Sat, 27 Jan 2024 05:49:55 GMT
VOLUME [/var/lib/influxdb]
# Sat, 27 Jan 2024 05:49:55 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Sat, 27 Jan 2024 05:49:55 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sat, 27 Jan 2024 05:49:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 05:49:55 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c332be88cb2898fd00957a6e5a3581893f9a14b30ec2470466897e8b246e9ad`  
		Last Modified: Sat, 27 Jan 2024 03:41:30 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23860728907803516673e82c6dbade4a15e2a3c8d5eb068dac0624d037ca63e`  
		Last Modified: Sat, 27 Jan 2024 05:51:38 GMT  
		Size: 1.5 MB (1472931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41dbab3a92f1d001e07dc6fb54de222a24e6c8dd327cbd3b9ff76492bb0a88bf`  
		Last Modified: Sat, 27 Jan 2024 05:51:58 GMT  
		Size: 33.2 MB (33248751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4c07bc517a54210e91f049d33d098f90aef5b0fb83397215bb2b5d45afd61da`  
		Last Modified: Sat, 27 Jan 2024 05:51:53 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a21e5dd20637b1b02d4cb447246a448d38e70c9821ff746b02fb530a999cb3`  
		Last Modified: Sat, 27 Jan 2024 05:51:53 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea9809d1b5b5adddd1ca21e5ae36f5ff06bdf4147cb14409b84536b436d8992f`  
		Last Modified: Sat, 27 Jan 2024 05:51:53 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.9.13-meta`

```console
$ docker pull influxdb@sha256:0f20c3223e62c375dfc47f82fd8a30db63244006576599d5ba6eda3f16df84c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.9.13-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:4137a252bf2565dd407d4a41128e314bbf1a4025a5501821a401d9d7d1a55f7e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83620571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5f8432c2b19411539b28e70b8a9cfa4f331d7886f7ff95aa6feceb298c23e0e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:32 GMT
ADD file:1bf1a123da85382e70ea251091b98fd8b4a1972e4c4e84d392443a4e20b7a135 in / 
# Tue, 13 Feb 2024 00:37:32 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:22:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:19:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 04:19:58 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Tue, 13 Feb 2024 04:20:10 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Tue, 13 Feb 2024 04:20:10 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Tue, 13 Feb 2024 04:20:10 GMT
EXPOSE 8091
# Tue, 13 Feb 2024 04:20:10 GMT
VOLUME [/var/lib/influxdb]
# Tue, 13 Feb 2024 04:20:10 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Tue, 13 Feb 2024 04:20:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 04:20:11 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:09e2bc8a597c33b54cccaf52f2e21798e2e0df79ab6cb33d3b1dfd4b33a57512`  
		Last Modified: Tue, 13 Feb 2024 00:42:21 GMT  
		Size: 55.1 MB (55084838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bbf2983642e080d705d575c1da8d4d8c35507576d88e44979b5c6229573d40`  
		Last Modified: Tue, 13 Feb 2024 01:31:47 GMT  
		Size: 15.8 MB (15763532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670ed7b83ea2bbde7dfba362fa83033db766fdb9e3721f9091229abbf0fafae7`  
		Last Modified: Tue, 13 Feb 2024 04:21:45 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc275cd09b4b0bf4b318b112c486e1b4348cd9103c5a46bc1bd885b52eff48cf`  
		Last Modified: Tue, 13 Feb 2024 04:22:16 GMT  
		Size: 12.8 MB (12769813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef68a6316f6f0f41e45091eb1313b1c2e68fbfc137ae1954d33c2c42036ca517`  
		Last Modified: Tue, 13 Feb 2024 04:22:14 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c36e200ae078b583ed845e0c64738a3816b17634bdd3efe9ee080a203c4d629`  
		Last Modified: Tue, 13 Feb 2024 04:22:15 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.9.13-meta-alpine`

```console
$ docker pull influxdb@sha256:b2417481cffba22ca7fc6eb5576be1b0b850483e860de71357b119be44177aa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.9.13-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:b73457a8ec3874796e55fae146c926eb54357e4169defc0966234e69979667bc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17587482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8321ec8111eda9eb9dd587fa1839d9941cb17ee3b4542fcbdc9656190394c334`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:40:27 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 27 Jan 2024 05:49:36 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Sat, 27 Jan 2024 05:49:48 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Sat, 27 Jan 2024 05:50:05 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/etc/influxdb/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 27 Jan 2024 05:50:05 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Sat, 27 Jan 2024 05:50:05 GMT
EXPOSE 8091
# Sat, 27 Jan 2024 05:50:05 GMT
VOLUME [/var/lib/influxdb]
# Sat, 27 Jan 2024 05:50:06 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Sat, 27 Jan 2024 05:50:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 05:50:06 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c332be88cb2898fd00957a6e5a3581893f9a14b30ec2470466897e8b246e9ad`  
		Last Modified: Sat, 27 Jan 2024 03:41:30 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23860728907803516673e82c6dbade4a15e2a3c8d5eb068dac0624d037ca63e`  
		Last Modified: Sat, 27 Jan 2024 05:51:38 GMT  
		Size: 1.5 MB (1472931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0f2675ebfd866fde3bc68c44e6dcfe11a79ab9ae5260d99baea66ee712873d`  
		Last Modified: Sat, 27 Jan 2024 05:52:09 GMT  
		Size: 12.7 MB (12734282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:618acef7e3f9802e623874f09cbf344bff7510bb12ecd8982dfdeff4964ab302`  
		Last Modified: Sat, 27 Jan 2024 05:52:06 GMT  
		Size: 216.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b3ca47192ec8dc8cd93761ceb85513ec25c39a4be443f9c4a7694572fe0bac`  
		Last Modified: Sat, 27 Jan 2024 05:52:07 GMT  
		Size: 372.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.7`

```console
$ docker pull influxdb@sha256:24a503d8283c59bb741f77be3413c9068fc1dee6f5d9211d404ba90945f90e56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.7` - linux; amd64

```console
$ docker pull influxdb@sha256:7d3ddaa15b316a038eff3d9cb632b1a9cf7d894dcd14e2cbff559b2a3f8d4a1c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164678553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:546676123e5d8466d266ec33fb4b1579cc58238862aa3d37e70a67c5e23161da`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:21:03 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:21:04 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version
# Tue, 13 Feb 2024 04:21:05 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb
# Tue, 13 Feb 2024 04:21:05 GMT
ENV GOSU_VER=1.16
# Tue, 13 Feb 2024 04:21:07 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true
# Tue, 13 Feb 2024 04:21:07 GMT
ENV INFLUXDB_VERSION=2.7.5
# Tue, 13 Feb 2024 04:21:12 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version
# Tue, 13 Feb 2024 04:21:12 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Tue, 13 Feb 2024 04:21:15 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version
# Tue, 13 Feb 2024 04:21:15 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Tue, 13 Feb 2024 04:21:15 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 13 Feb 2024 04:21:15 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Tue, 13 Feb 2024 04:21:15 GMT
COPY file:b5520696339eadb7386055c1dc9487351aa145a79b0cf206d8b1a79699c4a7f1 in /entrypoint.sh 
# Tue, 13 Feb 2024 04:21:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 04:21:16 GMT
CMD ["influxd"]
# Tue, 13 Feb 2024 04:21:16 GMT
EXPOSE 8086
# Tue, 13 Feb 2024 04:21:16 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 13 Feb 2024 04:21:16 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 13 Feb 2024 04:21:16 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 13 Feb 2024 04:21:16 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cdfd97cf1da6c346a07342c682bcfc51c5fc10658b30c37e936daa90ab65a91`  
		Last Modified: Tue, 13 Feb 2024 04:23:24 GMT  
		Size: 9.8 MB (9784701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd4a9addae614e5a65effd762fe63d058be52830284f99befa27b485bb39d77d`  
		Last Modified: Tue, 13 Feb 2024 04:23:21 GMT  
		Size: 5.8 MB (5820925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2682f23af6c5af32faf625123e45692cd5f8046ce91c4bbd112cf45b1ba878f9`  
		Last Modified: Tue, 13 Feb 2024 04:23:21 GMT  
		Size: 3.3 KB (3275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0d19c1b23c49c3c721b8970e51c0c6aeb36e56602f1379f9f3c7fdee619a65`  
		Last Modified: Tue, 13 Feb 2024 04:23:21 GMT  
		Size: 1.0 MB (1006415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18c18a467354ba9cdec6b0a5868a858779109bca36f654015fb30e93a157156b`  
		Last Modified: Tue, 13 Feb 2024 04:23:29 GMT  
		Size: 95.8 MB (95803971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa424e376698506b8c453c03617885b8abbade552aad4de5f42c5e7f5f691d2`  
		Last Modified: Tue, 13 Feb 2024 04:23:21 GMT  
		Size: 23.1 MB (23128356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f00eaf16d113504247a89fa3e3a8a3312e3944a5e6d528a0ea57c6a01bcb512a`  
		Last Modified: Tue, 13 Feb 2024 04:23:18 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51bddb37abd6835e005b9654961995776b33d3a90f096c2b9dc9f599c07a1155`  
		Last Modified: Tue, 13 Feb 2024 04:23:18 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d4cdb66f197e98ed28ed50ab0bedfd1b2f0009ac1424cb991cb66919c4ff20f`  
		Last Modified: Tue, 13 Feb 2024 04:23:18 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.7` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:582e7df0fa5c4941c148e54e64be9f977b1b09d7d873edeb4dd0602abf21c306
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.9 MB (158896828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec5df16229a7e8f28f51b92c1bdac0988de08fc0cc85732ee5556249eb69b14`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:20 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Tue, 13 Feb 2024 00:41:20 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 10:19:27 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 10:19:29 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version
# Tue, 13 Feb 2024 10:19:29 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb
# Tue, 13 Feb 2024 10:19:29 GMT
ENV GOSU_VER=1.16
# Tue, 13 Feb 2024 10:19:32 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true
# Tue, 13 Feb 2024 10:19:32 GMT
ENV INFLUXDB_VERSION=2.7.5
# Tue, 13 Feb 2024 10:19:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version
# Tue, 13 Feb 2024 10:19:38 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Tue, 13 Feb 2024 10:19:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version
# Tue, 13 Feb 2024 10:19:42 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Tue, 13 Feb 2024 10:19:42 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 13 Feb 2024 10:19:42 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Tue, 13 Feb 2024 10:19:42 GMT
COPY file:b5520696339eadb7386055c1dc9487351aa145a79b0cf206d8b1a79699c4a7f1 in /entrypoint.sh 
# Tue, 13 Feb 2024 10:19:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 10:19:42 GMT
CMD ["influxd"]
# Tue, 13 Feb 2024 10:19:42 GMT
EXPOSE 8086
# Tue, 13 Feb 2024 10:19:42 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 13 Feb 2024 10:19:42 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 13 Feb 2024 10:19:42 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 13 Feb 2024 10:19:43 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7c23471dfddf803b1351ebb5b3d4fe3707e3ac3a7a3c9574ff29c4f051ad8b9`  
		Last Modified: Tue, 13 Feb 2024 10:20:16 GMT  
		Size: 9.6 MB (9581551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c083731976ebb51878cd8a78a3bc4f8291c326359194369224c90e386e8c652a`  
		Last Modified: Tue, 13 Feb 2024 10:20:13 GMT  
		Size: 5.5 MB (5463787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92022dec65d38eb8b9209992acb610dd55be10e4158d3cab9a587b362accb80d`  
		Last Modified: Tue, 13 Feb 2024 10:20:12 GMT  
		Size: 3.3 KB (3276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec78cb36cb163b713b768330e0c7a303246ab9ffe29743408a7dc8e82eca67c0`  
		Last Modified: Tue, 13 Feb 2024 10:20:13 GMT  
		Size: 936.1 KB (936113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b205968d00a4520c4bf78b3ca4fc6066e6f9e931a460894845dc6e45a1824d98`  
		Last Modified: Tue, 13 Feb 2024 10:20:18 GMT  
		Size: 92.1 MB (92086333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae6677d78716fbae2bad54c391131b9c86b6852a8df46439cad3058d3d5b7cf`  
		Last Modified: Tue, 13 Feb 2024 10:20:12 GMT  
		Size: 21.7 MB (21662585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ac9207e54c3a01b693d2f94e1beb51afadd5359682257c569b65b5e178f39b`  
		Last Modified: Tue, 13 Feb 2024 10:20:10 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e516d64e2dd7b9dbdf9a409f11ba5c10a1ee078b9bfd51b47516f102930f5e6`  
		Last Modified: Tue, 13 Feb 2024 10:20:10 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee8cdbfbd26da898bf48152a8d90896d41de757543164d7ff4ff0ebd77bb2aa1`  
		Last Modified: Tue, 13 Feb 2024 10:20:11 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.7-alpine`

```console
$ docker pull influxdb@sha256:22baba2a02c3da8b1634445ee9e716d29be49ea2e44ec85e1d04355b8ab76fe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.7-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:fc475192490358ddd34fb3978f17ed31202f5c17b754635c26ebb401e88cce98
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.2 MB (89171290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e4a628dd4e176cbd8cd33c6f73401f1287187f6145706c9dedaf6a86aa0f48a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:11:20 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 27 Jan 2024 05:51:02 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates
# Sat, 27 Jan 2024 05:51:04 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version
# Sat, 27 Jan 2024 05:51:05 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Sat, 27 Jan 2024 05:51:05 GMT
ENV INFLUXDB_VERSION=2.7.5
# Sat, 27 Jan 2024 05:51:09 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version
# Sat, 27 Jan 2024 05:51:09 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Sat, 27 Jan 2024 05:51:11 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version
# Sat, 27 Jan 2024 05:51:12 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Sat, 27 Jan 2024 05:51:12 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Sat, 27 Jan 2024 05:51:12 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Sat, 27 Jan 2024 05:51:12 GMT
COPY file:6341d1dd8e0763e797b79985007acd07a4686ed831d55018f6e390823bad9d07 in /entrypoint.sh 
# Sat, 27 Jan 2024 05:51:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 05:51:12 GMT
CMD ["influxd"]
# Sat, 27 Jan 2024 05:51:13 GMT
EXPOSE 8086
# Sat, 27 Jan 2024 05:51:13 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Sat, 27 Jan 2024 05:51:13 GMT
ENV INFLUXD_INIT_PORT=9999
# Sat, 27 Jan 2024 05:51:13 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Sat, 27 Jan 2024 05:51:13 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27c0340c3b428b118deb541dd857e5413c0ea787e9ba56ae54589ea731c7730`  
		Last Modified: Sat, 27 Jan 2024 03:12:00 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e090475e04f82c11956ced4d5422cce34c49e37b64295298f3d8b69bca3955b6`  
		Last Modified: Sat, 27 Jan 2024 05:53:14 GMT  
		Size: 8.9 MB (8914808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4043054f3715c7fa2d6fa47af1b3295295d3c2386e18aa16afcf97c7259aa03`  
		Last Modified: Sat, 27 Jan 2024 05:53:13 GMT  
		Size: 5.8 MB (5820954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d7999fbc447a43eb69e1dbeefe41a741f6d4e18de97e25420545619cb4539e`  
		Last Modified: Sat, 27 Jan 2024 05:53:12 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c45f20122481be6895a905989ab0f447cf2ca73f3f5b427aa9ba01769894118e`  
		Last Modified: Sat, 27 Jan 2024 05:53:15 GMT  
		Size: 47.9 MB (47896263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea626495f5d85aeff0490ef2959fba0755e8594b330a2d65f9a6018982e4d89f`  
		Last Modified: Sat, 27 Jan 2024 05:53:13 GMT  
		Size: 23.1 MB (23128352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d7b79338f919945e917a8db44d7df500097f6f0de4d1a838a028afe6f1f0f41`  
		Last Modified: Sat, 27 Jan 2024 05:53:10 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5299395c71f2fd5580afd8500e76fc3ef76ce772302ac323a3097de7d046126`  
		Last Modified: Sat, 27 Jan 2024 05:53:10 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f41b5d48ccad16b945789b3e0b167074f699b0d461a8e65e271166d6bcbc15b`  
		Last Modified: Sat, 27 Jan 2024 05:53:10 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.7-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:c0c921780c451aa8641606e1893f49d762346be61c9f6eb5112335c0ac248733
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.5 MB (85495690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c79652c7c18471e22699f3d4bc699e378c4643882fe878270b30cb0b0e6f3fd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:14:32 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 27 Jan 2024 04:14:34 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates
# Sat, 27 Jan 2024 04:14:36 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version
# Sat, 27 Jan 2024 04:14:36 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Sat, 27 Jan 2024 04:14:36 GMT
ENV INFLUXDB_VERSION=2.7.5
# Sat, 27 Jan 2024 04:14:40 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version
# Sat, 27 Jan 2024 04:14:40 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Sat, 27 Jan 2024 04:14:42 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version
# Sat, 27 Jan 2024 04:14:43 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Sat, 27 Jan 2024 04:14:43 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Sat, 27 Jan 2024 04:14:43 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Sat, 27 Jan 2024 04:14:43 GMT
COPY file:6341d1dd8e0763e797b79985007acd07a4686ed831d55018f6e390823bad9d07 in /entrypoint.sh 
# Sat, 27 Jan 2024 04:14:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 04:14:43 GMT
CMD ["influxd"]
# Sat, 27 Jan 2024 04:14:43 GMT
EXPOSE 8086
# Sat, 27 Jan 2024 04:14:43 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Sat, 27 Jan 2024 04:14:43 GMT
ENV INFLUXD_INIT_PORT=9999
# Sat, 27 Jan 2024 04:14:43 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Sat, 27 Jan 2024 04:14:43 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b10b365dc27fbcb456614696265123cb9aa34afefec8863e4cc7c7c90a506f5`  
		Last Modified: Sat, 27 Jan 2024 04:14:58 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3becfe46e4e069b375ed6387d54188f10a44739c32fbe7e2f69a7ee63fd796e7`  
		Last Modified: Sat, 27 Jan 2024 04:14:57 GMT  
		Size: 9.0 MB (8988358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a660b792b8fe64761d3d1c6c956d7679b60ea88ff5750bc3e3e65c7db16e2191`  
		Last Modified: Sat, 27 Jan 2024 04:14:56 GMT  
		Size: 5.5 MB (5463805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f0add489259035f03abe2e8d15e19ef4945130a6646fd5023218f8226c34966`  
		Last Modified: Sat, 27 Jan 2024 04:14:56 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76cb8b6c2b8f05e4c5a7f06c6b1821e54afbf82bac9517af84fffa6529ff2d81`  
		Last Modified: Sat, 27 Jan 2024 04:14:57 GMT  
		Size: 46.0 MB (46039216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4973f36cc68f67cbafca125ebbcf13c64a8efdc4f713c7aaab0fdb52b25883d0`  
		Last Modified: Sat, 27 Jan 2024 04:14:56 GMT  
		Size: 21.7 MB (21662583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36491cd7f019a6b4c8563a7db3f9591f5a06032d0e43a2741808f0d3ef629102`  
		Last Modified: Sat, 27 Jan 2024 04:14:54 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06d0bd834339cd6ab987f1b78e74f7dac8bba6f8bf93bdd25baf64676c474564`  
		Last Modified: Sat, 27 Jan 2024 04:14:54 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176a3c3e64bbe81b839d79064bce806e55ad573a942d9a9194523b8a8a5c85e0`  
		Last Modified: Sat, 27 Jan 2024 04:14:54 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.7.5`

```console
$ docker pull influxdb@sha256:24a503d8283c59bb741f77be3413c9068fc1dee6f5d9211d404ba90945f90e56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.7.5` - linux; amd64

```console
$ docker pull influxdb@sha256:7d3ddaa15b316a038eff3d9cb632b1a9cf7d894dcd14e2cbff559b2a3f8d4a1c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164678553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:546676123e5d8466d266ec33fb4b1579cc58238862aa3d37e70a67c5e23161da`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:21:03 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:21:04 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version
# Tue, 13 Feb 2024 04:21:05 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb
# Tue, 13 Feb 2024 04:21:05 GMT
ENV GOSU_VER=1.16
# Tue, 13 Feb 2024 04:21:07 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true
# Tue, 13 Feb 2024 04:21:07 GMT
ENV INFLUXDB_VERSION=2.7.5
# Tue, 13 Feb 2024 04:21:12 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version
# Tue, 13 Feb 2024 04:21:12 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Tue, 13 Feb 2024 04:21:15 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version
# Tue, 13 Feb 2024 04:21:15 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Tue, 13 Feb 2024 04:21:15 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 13 Feb 2024 04:21:15 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Tue, 13 Feb 2024 04:21:15 GMT
COPY file:b5520696339eadb7386055c1dc9487351aa145a79b0cf206d8b1a79699c4a7f1 in /entrypoint.sh 
# Tue, 13 Feb 2024 04:21:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 04:21:16 GMT
CMD ["influxd"]
# Tue, 13 Feb 2024 04:21:16 GMT
EXPOSE 8086
# Tue, 13 Feb 2024 04:21:16 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 13 Feb 2024 04:21:16 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 13 Feb 2024 04:21:16 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 13 Feb 2024 04:21:16 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cdfd97cf1da6c346a07342c682bcfc51c5fc10658b30c37e936daa90ab65a91`  
		Last Modified: Tue, 13 Feb 2024 04:23:24 GMT  
		Size: 9.8 MB (9784701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd4a9addae614e5a65effd762fe63d058be52830284f99befa27b485bb39d77d`  
		Last Modified: Tue, 13 Feb 2024 04:23:21 GMT  
		Size: 5.8 MB (5820925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2682f23af6c5af32faf625123e45692cd5f8046ce91c4bbd112cf45b1ba878f9`  
		Last Modified: Tue, 13 Feb 2024 04:23:21 GMT  
		Size: 3.3 KB (3275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0d19c1b23c49c3c721b8970e51c0c6aeb36e56602f1379f9f3c7fdee619a65`  
		Last Modified: Tue, 13 Feb 2024 04:23:21 GMT  
		Size: 1.0 MB (1006415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18c18a467354ba9cdec6b0a5868a858779109bca36f654015fb30e93a157156b`  
		Last Modified: Tue, 13 Feb 2024 04:23:29 GMT  
		Size: 95.8 MB (95803971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa424e376698506b8c453c03617885b8abbade552aad4de5f42c5e7f5f691d2`  
		Last Modified: Tue, 13 Feb 2024 04:23:21 GMT  
		Size: 23.1 MB (23128356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f00eaf16d113504247a89fa3e3a8a3312e3944a5e6d528a0ea57c6a01bcb512a`  
		Last Modified: Tue, 13 Feb 2024 04:23:18 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51bddb37abd6835e005b9654961995776b33d3a90f096c2b9dc9f599c07a1155`  
		Last Modified: Tue, 13 Feb 2024 04:23:18 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d4cdb66f197e98ed28ed50ab0bedfd1b2f0009ac1424cb991cb66919c4ff20f`  
		Last Modified: Tue, 13 Feb 2024 04:23:18 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.7.5` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:582e7df0fa5c4941c148e54e64be9f977b1b09d7d873edeb4dd0602abf21c306
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.9 MB (158896828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec5df16229a7e8f28f51b92c1bdac0988de08fc0cc85732ee5556249eb69b14`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:20 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Tue, 13 Feb 2024 00:41:20 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 10:19:27 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 10:19:29 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version
# Tue, 13 Feb 2024 10:19:29 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb
# Tue, 13 Feb 2024 10:19:29 GMT
ENV GOSU_VER=1.16
# Tue, 13 Feb 2024 10:19:32 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true
# Tue, 13 Feb 2024 10:19:32 GMT
ENV INFLUXDB_VERSION=2.7.5
# Tue, 13 Feb 2024 10:19:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version
# Tue, 13 Feb 2024 10:19:38 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Tue, 13 Feb 2024 10:19:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version
# Tue, 13 Feb 2024 10:19:42 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Tue, 13 Feb 2024 10:19:42 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 13 Feb 2024 10:19:42 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Tue, 13 Feb 2024 10:19:42 GMT
COPY file:b5520696339eadb7386055c1dc9487351aa145a79b0cf206d8b1a79699c4a7f1 in /entrypoint.sh 
# Tue, 13 Feb 2024 10:19:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 10:19:42 GMT
CMD ["influxd"]
# Tue, 13 Feb 2024 10:19:42 GMT
EXPOSE 8086
# Tue, 13 Feb 2024 10:19:42 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 13 Feb 2024 10:19:42 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 13 Feb 2024 10:19:42 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 13 Feb 2024 10:19:43 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7c23471dfddf803b1351ebb5b3d4fe3707e3ac3a7a3c9574ff29c4f051ad8b9`  
		Last Modified: Tue, 13 Feb 2024 10:20:16 GMT  
		Size: 9.6 MB (9581551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c083731976ebb51878cd8a78a3bc4f8291c326359194369224c90e386e8c652a`  
		Last Modified: Tue, 13 Feb 2024 10:20:13 GMT  
		Size: 5.5 MB (5463787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92022dec65d38eb8b9209992acb610dd55be10e4158d3cab9a587b362accb80d`  
		Last Modified: Tue, 13 Feb 2024 10:20:12 GMT  
		Size: 3.3 KB (3276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec78cb36cb163b713b768330e0c7a303246ab9ffe29743408a7dc8e82eca67c0`  
		Last Modified: Tue, 13 Feb 2024 10:20:13 GMT  
		Size: 936.1 KB (936113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b205968d00a4520c4bf78b3ca4fc6066e6f9e931a460894845dc6e45a1824d98`  
		Last Modified: Tue, 13 Feb 2024 10:20:18 GMT  
		Size: 92.1 MB (92086333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae6677d78716fbae2bad54c391131b9c86b6852a8df46439cad3058d3d5b7cf`  
		Last Modified: Tue, 13 Feb 2024 10:20:12 GMT  
		Size: 21.7 MB (21662585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ac9207e54c3a01b693d2f94e1beb51afadd5359682257c569b65b5e178f39b`  
		Last Modified: Tue, 13 Feb 2024 10:20:10 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e516d64e2dd7b9dbdf9a409f11ba5c10a1ee078b9bfd51b47516f102930f5e6`  
		Last Modified: Tue, 13 Feb 2024 10:20:10 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee8cdbfbd26da898bf48152a8d90896d41de757543164d7ff4ff0ebd77bb2aa1`  
		Last Modified: Tue, 13 Feb 2024 10:20:11 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.7.5-alpine`

```console
$ docker pull influxdb@sha256:22baba2a02c3da8b1634445ee9e716d29be49ea2e44ec85e1d04355b8ab76fe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.7.5-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:fc475192490358ddd34fb3978f17ed31202f5c17b754635c26ebb401e88cce98
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.2 MB (89171290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e4a628dd4e176cbd8cd33c6f73401f1287187f6145706c9dedaf6a86aa0f48a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:11:20 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 27 Jan 2024 05:51:02 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates
# Sat, 27 Jan 2024 05:51:04 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version
# Sat, 27 Jan 2024 05:51:05 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Sat, 27 Jan 2024 05:51:05 GMT
ENV INFLUXDB_VERSION=2.7.5
# Sat, 27 Jan 2024 05:51:09 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version
# Sat, 27 Jan 2024 05:51:09 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Sat, 27 Jan 2024 05:51:11 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version
# Sat, 27 Jan 2024 05:51:12 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Sat, 27 Jan 2024 05:51:12 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Sat, 27 Jan 2024 05:51:12 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Sat, 27 Jan 2024 05:51:12 GMT
COPY file:6341d1dd8e0763e797b79985007acd07a4686ed831d55018f6e390823bad9d07 in /entrypoint.sh 
# Sat, 27 Jan 2024 05:51:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 05:51:12 GMT
CMD ["influxd"]
# Sat, 27 Jan 2024 05:51:13 GMT
EXPOSE 8086
# Sat, 27 Jan 2024 05:51:13 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Sat, 27 Jan 2024 05:51:13 GMT
ENV INFLUXD_INIT_PORT=9999
# Sat, 27 Jan 2024 05:51:13 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Sat, 27 Jan 2024 05:51:13 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27c0340c3b428b118deb541dd857e5413c0ea787e9ba56ae54589ea731c7730`  
		Last Modified: Sat, 27 Jan 2024 03:12:00 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e090475e04f82c11956ced4d5422cce34c49e37b64295298f3d8b69bca3955b6`  
		Last Modified: Sat, 27 Jan 2024 05:53:14 GMT  
		Size: 8.9 MB (8914808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4043054f3715c7fa2d6fa47af1b3295295d3c2386e18aa16afcf97c7259aa03`  
		Last Modified: Sat, 27 Jan 2024 05:53:13 GMT  
		Size: 5.8 MB (5820954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d7999fbc447a43eb69e1dbeefe41a741f6d4e18de97e25420545619cb4539e`  
		Last Modified: Sat, 27 Jan 2024 05:53:12 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c45f20122481be6895a905989ab0f447cf2ca73f3f5b427aa9ba01769894118e`  
		Last Modified: Sat, 27 Jan 2024 05:53:15 GMT  
		Size: 47.9 MB (47896263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea626495f5d85aeff0490ef2959fba0755e8594b330a2d65f9a6018982e4d89f`  
		Last Modified: Sat, 27 Jan 2024 05:53:13 GMT  
		Size: 23.1 MB (23128352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d7b79338f919945e917a8db44d7df500097f6f0de4d1a838a028afe6f1f0f41`  
		Last Modified: Sat, 27 Jan 2024 05:53:10 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5299395c71f2fd5580afd8500e76fc3ef76ce772302ac323a3097de7d046126`  
		Last Modified: Sat, 27 Jan 2024 05:53:10 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f41b5d48ccad16b945789b3e0b167074f699b0d461a8e65e271166d6bcbc15b`  
		Last Modified: Sat, 27 Jan 2024 05:53:10 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.7.5-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:c0c921780c451aa8641606e1893f49d762346be61c9f6eb5112335c0ac248733
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.5 MB (85495690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c79652c7c18471e22699f3d4bc699e378c4643882fe878270b30cb0b0e6f3fd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:14:32 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 27 Jan 2024 04:14:34 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates
# Sat, 27 Jan 2024 04:14:36 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version
# Sat, 27 Jan 2024 04:14:36 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Sat, 27 Jan 2024 04:14:36 GMT
ENV INFLUXDB_VERSION=2.7.5
# Sat, 27 Jan 2024 04:14:40 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version
# Sat, 27 Jan 2024 04:14:40 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Sat, 27 Jan 2024 04:14:42 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version
# Sat, 27 Jan 2024 04:14:43 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Sat, 27 Jan 2024 04:14:43 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Sat, 27 Jan 2024 04:14:43 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Sat, 27 Jan 2024 04:14:43 GMT
COPY file:6341d1dd8e0763e797b79985007acd07a4686ed831d55018f6e390823bad9d07 in /entrypoint.sh 
# Sat, 27 Jan 2024 04:14:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 04:14:43 GMT
CMD ["influxd"]
# Sat, 27 Jan 2024 04:14:43 GMT
EXPOSE 8086
# Sat, 27 Jan 2024 04:14:43 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Sat, 27 Jan 2024 04:14:43 GMT
ENV INFLUXD_INIT_PORT=9999
# Sat, 27 Jan 2024 04:14:43 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Sat, 27 Jan 2024 04:14:43 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b10b365dc27fbcb456614696265123cb9aa34afefec8863e4cc7c7c90a506f5`  
		Last Modified: Sat, 27 Jan 2024 04:14:58 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3becfe46e4e069b375ed6387d54188f10a44739c32fbe7e2f69a7ee63fd796e7`  
		Last Modified: Sat, 27 Jan 2024 04:14:57 GMT  
		Size: 9.0 MB (8988358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a660b792b8fe64761d3d1c6c956d7679b60ea88ff5750bc3e3e65c7db16e2191`  
		Last Modified: Sat, 27 Jan 2024 04:14:56 GMT  
		Size: 5.5 MB (5463805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f0add489259035f03abe2e8d15e19ef4945130a6646fd5023218f8226c34966`  
		Last Modified: Sat, 27 Jan 2024 04:14:56 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76cb8b6c2b8f05e4c5a7f06c6b1821e54afbf82bac9517af84fffa6529ff2d81`  
		Last Modified: Sat, 27 Jan 2024 04:14:57 GMT  
		Size: 46.0 MB (46039216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4973f36cc68f67cbafca125ebbcf13c64a8efdc4f713c7aaab0fdb52b25883d0`  
		Last Modified: Sat, 27 Jan 2024 04:14:56 GMT  
		Size: 21.7 MB (21662583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36491cd7f019a6b4c8563a7db3f9591f5a06032d0e43a2741808f0d3ef629102`  
		Last Modified: Sat, 27 Jan 2024 04:14:54 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06d0bd834339cd6ab987f1b78e74f7dac8bba6f8bf93bdd25baf64676c474564`  
		Last Modified: Sat, 27 Jan 2024 04:14:54 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176a3c3e64bbe81b839d79064bce806e55ad573a942d9a9194523b8a8a5c85e0`  
		Last Modified: Sat, 27 Jan 2024 04:14:54 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:22baba2a02c3da8b1634445ee9e716d29be49ea2e44ec85e1d04355b8ab76fe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:fc475192490358ddd34fb3978f17ed31202f5c17b754635c26ebb401e88cce98
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.2 MB (89171290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e4a628dd4e176cbd8cd33c6f73401f1287187f6145706c9dedaf6a86aa0f48a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:11:20 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 27 Jan 2024 05:51:02 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates
# Sat, 27 Jan 2024 05:51:04 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version
# Sat, 27 Jan 2024 05:51:05 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Sat, 27 Jan 2024 05:51:05 GMT
ENV INFLUXDB_VERSION=2.7.5
# Sat, 27 Jan 2024 05:51:09 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version
# Sat, 27 Jan 2024 05:51:09 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Sat, 27 Jan 2024 05:51:11 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version
# Sat, 27 Jan 2024 05:51:12 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Sat, 27 Jan 2024 05:51:12 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Sat, 27 Jan 2024 05:51:12 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Sat, 27 Jan 2024 05:51:12 GMT
COPY file:6341d1dd8e0763e797b79985007acd07a4686ed831d55018f6e390823bad9d07 in /entrypoint.sh 
# Sat, 27 Jan 2024 05:51:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 05:51:12 GMT
CMD ["influxd"]
# Sat, 27 Jan 2024 05:51:13 GMT
EXPOSE 8086
# Sat, 27 Jan 2024 05:51:13 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Sat, 27 Jan 2024 05:51:13 GMT
ENV INFLUXD_INIT_PORT=9999
# Sat, 27 Jan 2024 05:51:13 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Sat, 27 Jan 2024 05:51:13 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27c0340c3b428b118deb541dd857e5413c0ea787e9ba56ae54589ea731c7730`  
		Last Modified: Sat, 27 Jan 2024 03:12:00 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e090475e04f82c11956ced4d5422cce34c49e37b64295298f3d8b69bca3955b6`  
		Last Modified: Sat, 27 Jan 2024 05:53:14 GMT  
		Size: 8.9 MB (8914808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4043054f3715c7fa2d6fa47af1b3295295d3c2386e18aa16afcf97c7259aa03`  
		Last Modified: Sat, 27 Jan 2024 05:53:13 GMT  
		Size: 5.8 MB (5820954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d7999fbc447a43eb69e1dbeefe41a741f6d4e18de97e25420545619cb4539e`  
		Last Modified: Sat, 27 Jan 2024 05:53:12 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c45f20122481be6895a905989ab0f447cf2ca73f3f5b427aa9ba01769894118e`  
		Last Modified: Sat, 27 Jan 2024 05:53:15 GMT  
		Size: 47.9 MB (47896263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea626495f5d85aeff0490ef2959fba0755e8594b330a2d65f9a6018982e4d89f`  
		Last Modified: Sat, 27 Jan 2024 05:53:13 GMT  
		Size: 23.1 MB (23128352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d7b79338f919945e917a8db44d7df500097f6f0de4d1a838a028afe6f1f0f41`  
		Last Modified: Sat, 27 Jan 2024 05:53:10 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5299395c71f2fd5580afd8500e76fc3ef76ce772302ac323a3097de7d046126`  
		Last Modified: Sat, 27 Jan 2024 05:53:10 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f41b5d48ccad16b945789b3e0b167074f699b0d461a8e65e271166d6bcbc15b`  
		Last Modified: Sat, 27 Jan 2024 05:53:10 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:c0c921780c451aa8641606e1893f49d762346be61c9f6eb5112335c0ac248733
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.5 MB (85495690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c79652c7c18471e22699f3d4bc699e378c4643882fe878270b30cb0b0e6f3fd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:14:32 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 27 Jan 2024 04:14:34 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates
# Sat, 27 Jan 2024 04:14:36 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version
# Sat, 27 Jan 2024 04:14:36 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Sat, 27 Jan 2024 04:14:36 GMT
ENV INFLUXDB_VERSION=2.7.5
# Sat, 27 Jan 2024 04:14:40 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version
# Sat, 27 Jan 2024 04:14:40 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Sat, 27 Jan 2024 04:14:42 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version
# Sat, 27 Jan 2024 04:14:43 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Sat, 27 Jan 2024 04:14:43 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Sat, 27 Jan 2024 04:14:43 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Sat, 27 Jan 2024 04:14:43 GMT
COPY file:6341d1dd8e0763e797b79985007acd07a4686ed831d55018f6e390823bad9d07 in /entrypoint.sh 
# Sat, 27 Jan 2024 04:14:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 04:14:43 GMT
CMD ["influxd"]
# Sat, 27 Jan 2024 04:14:43 GMT
EXPOSE 8086
# Sat, 27 Jan 2024 04:14:43 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Sat, 27 Jan 2024 04:14:43 GMT
ENV INFLUXD_INIT_PORT=9999
# Sat, 27 Jan 2024 04:14:43 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Sat, 27 Jan 2024 04:14:43 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b10b365dc27fbcb456614696265123cb9aa34afefec8863e4cc7c7c90a506f5`  
		Last Modified: Sat, 27 Jan 2024 04:14:58 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3becfe46e4e069b375ed6387d54188f10a44739c32fbe7e2f69a7ee63fd796e7`  
		Last Modified: Sat, 27 Jan 2024 04:14:57 GMT  
		Size: 9.0 MB (8988358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a660b792b8fe64761d3d1c6c956d7679b60ea88ff5750bc3e3e65c7db16e2191`  
		Last Modified: Sat, 27 Jan 2024 04:14:56 GMT  
		Size: 5.5 MB (5463805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f0add489259035f03abe2e8d15e19ef4945130a6646fd5023218f8226c34966`  
		Last Modified: Sat, 27 Jan 2024 04:14:56 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76cb8b6c2b8f05e4c5a7f06c6b1821e54afbf82bac9517af84fffa6529ff2d81`  
		Last Modified: Sat, 27 Jan 2024 04:14:57 GMT  
		Size: 46.0 MB (46039216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4973f36cc68f67cbafca125ebbcf13c64a8efdc4f713c7aaab0fdb52b25883d0`  
		Last Modified: Sat, 27 Jan 2024 04:14:56 GMT  
		Size: 21.7 MB (21662583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36491cd7f019a6b4c8563a7db3f9591f5a06032d0e43a2741808f0d3ef629102`  
		Last Modified: Sat, 27 Jan 2024 04:14:54 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06d0bd834339cd6ab987f1b78e74f7dac8bba6f8bf93bdd25baf64676c474564`  
		Last Modified: Sat, 27 Jan 2024 04:14:54 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176a3c3e64bbe81b839d79064bce806e55ad573a942d9a9194523b8a8a5c85e0`  
		Last Modified: Sat, 27 Jan 2024 04:14:54 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:latest`

```console
$ docker pull influxdb@sha256:24a503d8283c59bb741f77be3413c9068fc1dee6f5d9211d404ba90945f90e56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:7d3ddaa15b316a038eff3d9cb632b1a9cf7d894dcd14e2cbff559b2a3f8d4a1c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164678553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:546676123e5d8466d266ec33fb4b1579cc58238862aa3d37e70a67c5e23161da`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:21:03 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:21:04 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version
# Tue, 13 Feb 2024 04:21:05 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb
# Tue, 13 Feb 2024 04:21:05 GMT
ENV GOSU_VER=1.16
# Tue, 13 Feb 2024 04:21:07 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true
# Tue, 13 Feb 2024 04:21:07 GMT
ENV INFLUXDB_VERSION=2.7.5
# Tue, 13 Feb 2024 04:21:12 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version
# Tue, 13 Feb 2024 04:21:12 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Tue, 13 Feb 2024 04:21:15 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version
# Tue, 13 Feb 2024 04:21:15 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Tue, 13 Feb 2024 04:21:15 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 13 Feb 2024 04:21:15 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Tue, 13 Feb 2024 04:21:15 GMT
COPY file:b5520696339eadb7386055c1dc9487351aa145a79b0cf206d8b1a79699c4a7f1 in /entrypoint.sh 
# Tue, 13 Feb 2024 04:21:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 04:21:16 GMT
CMD ["influxd"]
# Tue, 13 Feb 2024 04:21:16 GMT
EXPOSE 8086
# Tue, 13 Feb 2024 04:21:16 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 13 Feb 2024 04:21:16 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 13 Feb 2024 04:21:16 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 13 Feb 2024 04:21:16 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cdfd97cf1da6c346a07342c682bcfc51c5fc10658b30c37e936daa90ab65a91`  
		Last Modified: Tue, 13 Feb 2024 04:23:24 GMT  
		Size: 9.8 MB (9784701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd4a9addae614e5a65effd762fe63d058be52830284f99befa27b485bb39d77d`  
		Last Modified: Tue, 13 Feb 2024 04:23:21 GMT  
		Size: 5.8 MB (5820925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2682f23af6c5af32faf625123e45692cd5f8046ce91c4bbd112cf45b1ba878f9`  
		Last Modified: Tue, 13 Feb 2024 04:23:21 GMT  
		Size: 3.3 KB (3275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0d19c1b23c49c3c721b8970e51c0c6aeb36e56602f1379f9f3c7fdee619a65`  
		Last Modified: Tue, 13 Feb 2024 04:23:21 GMT  
		Size: 1.0 MB (1006415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18c18a467354ba9cdec6b0a5868a858779109bca36f654015fb30e93a157156b`  
		Last Modified: Tue, 13 Feb 2024 04:23:29 GMT  
		Size: 95.8 MB (95803971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa424e376698506b8c453c03617885b8abbade552aad4de5f42c5e7f5f691d2`  
		Last Modified: Tue, 13 Feb 2024 04:23:21 GMT  
		Size: 23.1 MB (23128356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f00eaf16d113504247a89fa3e3a8a3312e3944a5e6d528a0ea57c6a01bcb512a`  
		Last Modified: Tue, 13 Feb 2024 04:23:18 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51bddb37abd6835e005b9654961995776b33d3a90f096c2b9dc9f599c07a1155`  
		Last Modified: Tue, 13 Feb 2024 04:23:18 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d4cdb66f197e98ed28ed50ab0bedfd1b2f0009ac1424cb991cb66919c4ff20f`  
		Last Modified: Tue, 13 Feb 2024 04:23:18 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:582e7df0fa5c4941c148e54e64be9f977b1b09d7d873edeb4dd0602abf21c306
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.9 MB (158896828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec5df16229a7e8f28f51b92c1bdac0988de08fc0cc85732ee5556249eb69b14`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:20 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Tue, 13 Feb 2024 00:41:20 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 10:19:27 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 10:19:29 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version
# Tue, 13 Feb 2024 10:19:29 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb
# Tue, 13 Feb 2024 10:19:29 GMT
ENV GOSU_VER=1.16
# Tue, 13 Feb 2024 10:19:32 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true
# Tue, 13 Feb 2024 10:19:32 GMT
ENV INFLUXDB_VERSION=2.7.5
# Tue, 13 Feb 2024 10:19:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version
# Tue, 13 Feb 2024 10:19:38 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Tue, 13 Feb 2024 10:19:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version
# Tue, 13 Feb 2024 10:19:42 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Tue, 13 Feb 2024 10:19:42 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 13 Feb 2024 10:19:42 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Tue, 13 Feb 2024 10:19:42 GMT
COPY file:b5520696339eadb7386055c1dc9487351aa145a79b0cf206d8b1a79699c4a7f1 in /entrypoint.sh 
# Tue, 13 Feb 2024 10:19:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 10:19:42 GMT
CMD ["influxd"]
# Tue, 13 Feb 2024 10:19:42 GMT
EXPOSE 8086
# Tue, 13 Feb 2024 10:19:42 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 13 Feb 2024 10:19:42 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 13 Feb 2024 10:19:42 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 13 Feb 2024 10:19:43 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7c23471dfddf803b1351ebb5b3d4fe3707e3ac3a7a3c9574ff29c4f051ad8b9`  
		Last Modified: Tue, 13 Feb 2024 10:20:16 GMT  
		Size: 9.6 MB (9581551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c083731976ebb51878cd8a78a3bc4f8291c326359194369224c90e386e8c652a`  
		Last Modified: Tue, 13 Feb 2024 10:20:13 GMT  
		Size: 5.5 MB (5463787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92022dec65d38eb8b9209992acb610dd55be10e4158d3cab9a587b362accb80d`  
		Last Modified: Tue, 13 Feb 2024 10:20:12 GMT  
		Size: 3.3 KB (3276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec78cb36cb163b713b768330e0c7a303246ab9ffe29743408a7dc8e82eca67c0`  
		Last Modified: Tue, 13 Feb 2024 10:20:13 GMT  
		Size: 936.1 KB (936113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b205968d00a4520c4bf78b3ca4fc6066e6f9e931a460894845dc6e45a1824d98`  
		Last Modified: Tue, 13 Feb 2024 10:20:18 GMT  
		Size: 92.1 MB (92086333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae6677d78716fbae2bad54c391131b9c86b6852a8df46439cad3058d3d5b7cf`  
		Last Modified: Tue, 13 Feb 2024 10:20:12 GMT  
		Size: 21.7 MB (21662585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ac9207e54c3a01b693d2f94e1beb51afadd5359682257c569b65b5e178f39b`  
		Last Modified: Tue, 13 Feb 2024 10:20:10 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e516d64e2dd7b9dbdf9a409f11ba5c10a1ee078b9bfd51b47516f102930f5e6`  
		Last Modified: Tue, 13 Feb 2024 10:20:10 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee8cdbfbd26da898bf48152a8d90896d41de757543164d7ff4ff0ebd77bb2aa1`  
		Last Modified: Tue, 13 Feb 2024 10:20:11 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
